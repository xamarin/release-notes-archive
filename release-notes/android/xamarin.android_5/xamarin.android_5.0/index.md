---
id: C9DE46D6-F914-4697-BBC8-43D40CC44269
title: "Xamarin.Android 5.0"
---

The Xamarin.Android 5.0 series provides support for 
[Android Wear apps](https://developer.android.com/design/wear/structure.html).

**Note:** Xamarin.Android 5.0 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21.
JDK 1.6 may be used when targeting previous API levels.

<!--
  JONP: 5.0.0 last updated from commit monodroid/master/598da706b3b2507b218aa28b4b503ce6694cbad0
-->

<a name="0"/>
<a name="Xamarin.Android_5.0.0"/>
# Xamarin.Android 5.0

<a name="new-features-5.0" />
## New Features

* OpenGLES 3.1 Support
* [Android Wear](https://developer.android.com/design/wear/structure.html) Support.
* New tool, `logcat-parse`, for investigating GREF use.

<a name="breaking-changes-5.0" />
## Breaking Changes

There are several breaking changes in this release, many of which have been
hinted at previously via `[Obsolete]` messages, some of which are *semantic*
changes which won't break compilation but *may* affect runtime behavior.

<a name="remove-property-setters" />
### Removal Of Property Setters for `final` Fields

Property setters are no longer generated for Java `final` fields.
(This accounts for *most* of changes in the API Changes, below.)
The property setters were present due to oversight, and should not
have been used.

<!--
Fun fact: e.g. Android.OS.Debug.MemoryInfo.Creator could be set to e.g. null,
and the Java-side value would be changed! Imagine the havoc this would cause
if/when Java needed MemoryInfo.CREATOR...
  -->

<a name="mindskversion-default-value" />
### Change minSdkVersion default value

The default `//uses-sdk/@android:minSdkVersion` value within `AndroidManifest.xml`
in previous releases defaulted to `$(TargetFrameworkVersion)`.
It now defaults to API-11 unless `$(TargetFrameworkVersion)` is `v2.3`, in which
case it's API-10.

This change should make it easier to create new projects and deploy them
to "older" devices without first visiting Project Options.

**Note**: The *default* `minSdkVersion` may change in the future with minimal
or no notice. API-11 was chosen because that was the minimum required to make
[Activity.ActionBar](/api/property/Android.App.Activity.ActionBar/)
not return `null` (it's value depends upon `minSdkVersion`). If we find other
Android functionality which is dependent upon `minSdkVersion`, we may bump
`minSdkVersion` higher so that default projects may more easily make use of it.

<a name="cross-vm-exceptions" />
### Cross-VM Exception Propagation 

Exceptions which cross VM boundaries now participate in Java stack unwinding.
Behavior of unhandled C# exceptions within the debugger is now different;
*if* an unhandled exception is reported -- and it may not be when thrown
from the UI thread -- then the debugger will "break" on the last entry
into managed code, *not* from where the exception was originally thrown.

The previous behavior may be enabled by exporting the
`XA_BROKEN_EXCEPTION_TRANSITIONS` environment variable with the value
`true`.

<a name="drop-obsolete-bindings" />
### Removal Of API Levels

Binding assemblies for Android v1.6 (API-4), Android v2.1 (API-7),
Android v2.2 (API-8), Android v3.1 (API-12), and Android v4.0 (API-14)
has been dropped.

Xamarin.Android applications can still *run* on these platforms, but
the compiler will no longer assist you in ensuring that types and members
which do not exist in those API levels are not referenced.

<a name="drop-obsolete-apis" />
### Removal of Obsolete Assemblies

The `Mono.Android.GoogleMaps.dll`, `Mono.Android.Support.v4.dll`,
and `Mono.Android.Support.v13.dll` assemblies have been removed.
(All types in these assemblies were obsoleted in
[Xamarin.Android 4.14](/releases/android/xamarin.android_4/xamarin.android_4.14/))

Please migrate to the corresponding Xamarin Components:

* `Mono.Android.GoogleMaps`: Please use the
    [Google Play Services](http://components.xamarin.com/view/googleplayservices)
    component.
* `Mono.Android.Support.v4.dll`: Please use the
    [Android Support Library v4](http://components.xamarin.com/view/xamandroidsupportv4-18)
    component.
* `Mono.Android.Support.v13.dll`: Please use the
    [Android Support Library v13](http://components.xamarin.com/view/xamandroidsupportv13-18)
    component.

<a name="newobjectarray" />
### JNIEnv.NewObjectArray

`JNIEnv.NewObjectArray<T>(T[])` now consistently generates a Java array
based on `typeof(T)`, instead of probing the runtime type of the first
non-`null` value within the provided array.

<!-- I have no idea what I was thinking with using the runtime type... -->

<a name="acw-naming" />
### Android Callable Wrapper Naming
The [name mangling scheme for Android Callable Wrappers](http://developer.xamarin.com/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers/)
is changing. Previously, the Android Callable Wrapper package name was
constructed by lowercasing the namespace name, [which would result in
packaging failures if more than one assembly contained a type with the same
fully-qualified name](https://bugzilla.xamarin.com/show_bug.cgi?id=16826).

With the 5.0 release, the *default* package names for Android Callable
Wrappers will be based on the MD5SUM of the assembly-qualified name of the
type being exported. This allows the same fully-qualified name to be
provided from two different assemblies and *not* get a packaging error.

This change *can* cause compatibility problems. For example, if you have a
script which relies on the Android Callable Wrapper name:

    adb shell am start -n My.Package.Name/my.ActivityType

Such a script will fail because the type `my.ActivityType` will no longer
be generated (by default).

I **strongly** recommend that you **do not** update such scripts to use
the new generated type name, as the new name names are ugly.

Instead, I would suggest that you use
[RegisterAttribute](/api/type/Android.Runtime.RegisterAttribute/),
[BroadcastReceiverAttribute.Name](/api/property/Android.Content.BroadcastReceiverAttribute.Name/),
[ContentProviderAttribute.Name](/api/property/Android.Content.ContentProviderAttribute.Name/),
[ActivityAttribute.Name](/api/property/Android.App.ActivityAttribute.Name/),
[ApplicationAttribute.Name](/api/property/Android.App.ApplicationAttribute.Name/), or
[ServiceAttribute.Name](/api/property/Android.App.ServiceAttribute.Name/).

For example, if you previously had:

    namespace My {
        [Activity]
        public partial class ActivityType : Activity {
            /* ... */
        }
    }

Then to maintain compatibility with your scripts/external code, set the
`ActivityAttribute.Name` property:

    namespace My {
        [Activity(Name="my.ActivityType")]
        public partial class ActivityType : Activity {
            /* ... */
        }
    }

For a more complete example, this change was responsible for
[causing the `ApiDemo` sample to crash on startup](https://bugzilla.xamarin.com/show_bug.cgi?id=24967)
because
[`ApiDemo` used `//activity/@android:name` instead of the `[Activity] custom attribute`](https://github.com/xamarin/monodroid-samples/blob/214de0a952c87255b368f5a63458210ecead3e61/ApiDemo/Properties/AndroidManifest.xml#L27)
in several locations, and in Xamarin.Android 5.0 this resulted in an
"inconsistency" between `AndroidManifest.xml` and the actual Java files.
[The fix for `ApiDemo`](https://github.com/xamarin/monodroid-samples/commit/397b52b0c27c073f38ba8957d648d5b25275ca7b)
involves using `ActivityAttribute.Name` and removing the XML fragments
from `AndroidManifest.xml`, as deemed appropriate.

<a name="bugs"/>
## Bug Fixes

* Fix `System.Linq.Expressions` linking
* [7634](https://bugzilla.xamarin.com/show_bug.cgi?id=7634):
    Managed > Java > Managed Exception Propoagation is broken.
* [10268](https://bugzilla.xamarin.com/show_bug.cgi?id=10268):
    Linker issue with horizontallistview project in release mode.
* [11270](https://bugzilla.xamarin.com/show_bug.cgi?id=11270):
    Linker failure.
* [17257](https://bugzilla.xamarin.com/show_bug.cgi?id=17257):
    `NoSuchMethodError` when using `TreeViewObserver.GlobalLayout` on targets
    before API level 16.
* [16805](https://bugzilla.xamarin.com/show_bug.cgi?id=16805):
    `<fragment class=""/>` now supports assembly-qualified type names.
* [16826](https://bugzilla.xamarin.com/show_bug.cgi?id=16826):
    ACWs: Create unique package names instead of lowercasing the namespace.
* [21159](https://bugzilla.xamarin.com/show_bug.cgi?id=21159):
    Incorrect `super` constructor in generated Java in class that inherits `android.graphics.Canvas`.
* [21361](https://bugzilla.xamarin.com/show_bug.cgi?id=21361):
    Attribute *name* has already been defined, when having attributes defined
    in a Android Class Library and using Android Binding component
* [21578](https://bugzilla.xamarin.com/show_bug.cgi?id=21578):
    App crashes in Release builds. System.Net.Sockets.Socket.SetSocketOption getting stripped by linker?
* [22218](https://bugzilla.xamarin.com/show_bug.cgi?id=22218):
    [generator] Parameter marshaling is not exception-safe.
* [22912](https://bugzilla.xamarin.com/show_bug.cgi?id=22912):
    `DateTime.Now` gives `NullReferenceException` in other `AppDomain`s.
* [22955](https://bugzilla.xamarin.com/show_bug.cgi?id=22955):
    Basic DateTime calcutions are now throwing exceptions.
* [22959](https://bugzilla.xamarin.com/show_bug.cgi?id=22959):
    Cannot find symbol exception when inheriting from `Java.Lang.RuntimeException`.
* [22962](https://bugzilla.xamarin.com/show_bug.cgi?id=22962):
    `@deprecated` annotations aren't mapped to C#'s `[Obsolete]` attribute.
* [22968](https://bugzilla.xamarin.com/show_bug.cgi?id=22968):
    Crash when lazy loading assemblies.
* [23077](https://bugzilla.xamarin.com/show_bug.cgi?id=23077):
    Wrap DriveInfo to StatFs.
* [23405](https://bugzilla.xamarin.com/show_bug.cgi?id=23405):
    `DateTime.Now` returns time off by 1 hour
* [23564](https://bugzilla.xamarin.com/show_bug.cgi?id=23564):
    Setting `WindowSoftInputMode` to `SoftInput.AdjustNothing` on `Activity`
    generates an out of range exception on compilation.
* [23617](https://bugzilla.xamarin.com/show_bug.cgi?id=23617):
    Can't build in Release mode: Error executing task GenerateJavaStubs:
    Could not load assembly 'Xamarin.Android.Support.v4'
* [24497](https://bugzilla.xamarin.com/show_bug.cgi?id=24497):
    Certain APIs break linking due to inter-API-level differences.


<a name="integrated-mono-5.0" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 3.12](http://www.mono-project.com/docs/about-mono/releases/3.12.0/)
[commit 92be1aeb](https://github.com/mono/mono/commit/92be1aebdb4e768d377145fd0c5273fa78195cbb).

* [1852](https://bugzilla.xamarin.com/show_bug.cgi?id=1852):
    XmlSerialization ignores `ShouldSerialize*` and `*Specified`
* [6512](https://bugzilla.xamarin.com/show_bug.cgi?id=6512):
    Don't parse JSON when using GET
* [18422](https://bugzilla.xamarin.com/show_bug.cgi?id=18422):
    `HttpClient` doesn't support 'name[]' header field name format
* [19012](https://bugzilla.xamarin.com/show_bug.cgi?id=19012):
    `XmlArrayItemAttribute.IsNullable` default does not match MS.NET default.
* [19039](https://bugzilla.xamarin.com/show_bug.cgi?id=19039):
    Runtime crashes when evaluating `FieldInfo.MetadataToken` in Dynamic Assembly
* [20403](https://bugzilla.xamarin.com/show_bug.cgi?id=20403):
    `InvalidOperationException` when XML-serializing `System.Drawing.Color`
* [21571](https://bugzilla.xamarin.com/show_bug.cgi?id=21571):
    `Uri.GetComponents()` should allow `UriComponents.SerializationInfoString` on relative `Uri`
* [21653](https://bugzilla.xamarin.com/show_bug.cgi?id=21653):
    App crashed attempting to debug: Assertion, `mono_error_ok (&error)` not met. 
* [22212](https://bugzilla.xamarin.com/show_bug.cgi?id=22212):
    Error parsing `DateTime` string in New Zealand Culture.
* [22383](https://bugzilla.xamarin.com/show_bug.cgi?id=22383):
    `HttpClient`'s `RequestMessage.RequestUri.AbsoluteUri` don't automatically point to right ones on 302
* [22417](https://bugzilla.xamarin.com/show_bug.cgi?id=22417):
    `DateTime.Parse()` does not correctly recognize the date with correct format
* [22557](https://bugzilla.xamarin.com/show_bug.cgi?id=22557):
    `HttpValueCollection` does not properly url encode values in `ToString()` method
* [22558](https://bugzilla.xamarin.com/show_bug.cgi?id=22558):
    `DateTimeOffset.Parse()` can't handle the dateTime string without time part.
* [22591](https://bugzilla.xamarin.com/show_bug.cgi?id=22591):
    Default `BigInteger` causes exceptions and incorrect answers
* [22685](https://bugzilla.xamarin.com/show_bug.cgi?id=22685):
    Assertion at mini.c:4656, condition `cfg->code_size - cfg->epilog_begin < 0xffff` not met
* [22704](https://bugzilla.xamarin.com/show_bug.cgi?id=22704):
    `ClientWebSocket` cannot handle reading subsets of the payload
* [22764](https://bugzilla.xamarin.com/show_bug.cgi?id=22764):
    HTTP POST ContentType is null instead of one sent by client in case of `MultipartFormDataContent`
* [22775](https://bugzilla.xamarin.com/show_bug.cgi?id=22775):
    Flawed implementation of `BlockingCollection(T).AddToAny` - Only blocks on first collection
* [22851](https://bugzilla.xamarin.com/show_bug.cgi?id=22851):
    `DateTimeOffset.Parse()` doesn't handle RFC1123 formatted timestamps correctly
* [22857](https://bugzilla.xamarin.com/show_bug.cgi?id=22857):
    `DirectoryInfo.EnumerateFileSystemInfos()` with `SearchOption.AllDirectories` does not return all subdirectories
* [23021](https://bugzilla.xamarin.com/show_bug.cgi?id=23021):
    Calls from generic shared methods not always patched.
* [23077](https://bugzilla.xamarin.com/show_bug.cgi?id=23077):
    Wrap `DriveInfo` to `StatFs`.
* [23206](https://bugzilla.xamarin.com/show_bug.cgi?id=23206):
    Microsoft allows threadpool threads to be renamed multiple times
* [23242](https://bugzilla.xamarin.com/show_bug.cgi?id=23242):
    Null reference exception occurs after the call to `int.ToString()` from multiple threads
* [23318](https://bugzilla.xamarin.com/show_bug.cgi?id=23318):
    `XComment` throws an exception with some inputs
* [23376](https://bugzilla.xamarin.com/show_bug.cgi?id=23376):
    `TimeSpan` returns incorrect result.
* [23392](https://bugzilla.xamarin.com/show_bug.cgi?id=23392):
    Assertion at mini-codegen.c:2307, condition `sp < 8` not met
* [23423](https://bugzilla.xamarin.com/show_bug.cgi?id=23423):
    SIGABRT and crash in `System.Diagnostics.Process`
* [23438](https://bugzilla.xamarin.com/show_bug.cgi?id=23438):
    ECMA-335 Type layout attributes and atomic operations: a generic type shall not have explicit layout
* [23594](https://bugzilla.xamarin.com/show_bug.cgi?id=23594):
    A task will not complete if an exception is thrown in an attached child task with a task continuation that specifies `TaskContinuationOptions.NotOnFaulted`
* [23700](https://bugzilla.xamarin.com/show_bug.cgi?id=23700):
    App using `SocketAsyncEventArgs` sometimes crash with `ObjectDisposedException`, stacktrace starts in `DispatcherCB`
* [23769](https://bugzilla.xamarin.com/show_bug.cgi?id=23769):
    Getting `NotSupportedException`s when performing reflection on generic types defined in dynamic assemblies
* [24109](https://bugzilla.xamarin.com/show_bug.cgi?id=24109):
    `SoundPlayer` corrupts memory, leading to crashes
* [24221](https://bugzilla.xamarin.com/show_bug.cgi?id=24221):
    Sorting of large structs with wrong result.
* [24340](https://bugzilla.xamarin.com/show_bug.cgi?id=24340):
    Some WebSocket unit tests (System) fails *silently*
* [24577](https://bugzilla.xamarin.com/show_bug.cgi?id=24577):
    Fatal Unhandled Exсeption: `System.FormatException`


<a name="API_Changes" />
# API Changes

* API Level 10:
    [Mono.Android.dll](level_10_diff/mono.android.dll),
    [OpenTK.dll](level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](level_10_diff/opentk-1.0.dll)
* API Level 15:
    [Mono.Android.dll](level_15_diff/mono.android.dll)
* API Level 16:
    [Mono.Android.dll](level_16_diff/mono.android.dll)
* API Level 17:
    [Mono.Android.dll](level_17_diff/mono.android.dll)
* API Level 18:
    [Mono.Android.dll](level_18_diff/mono.android.dll)
* API Level 19:
    [Mono.Android.dll](level_19_diff/mono.android.dll)
* API Level 20:
    [Mono.Android.dll](level_20_diff/mono.android.dll)
* API Level 21:
    [Mono.Android.dll](level_21_diff/mono.android.dll)

