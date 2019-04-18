---
id: 243CE8CA-9287-4C80-9AF8-D7E4778EB82E
title: "Xamarin.Android 4.99"
---

The Xamarin.Android 4.99 series is an alpha-only release on the path to a
future Xamarin.Android 5.0 release, providing support for 
[Android Wear apps](https://developer.android.com/design/wear/structure.html)
and preview bindings for
[Android API-L](https://developer.android.com/preview/api-overview.html).

**Note:** Xamarin.Android 4.99 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-L.
JDK 1.6 may be used when targeting previous API levels.

<!--
  JONP: 4.99.0 last updated from commit monodroid/master/598da706b3b2507b218aa28b4b503ce6694cbad0
-->

<a name="0"/>
<a name="Xamarin.Android_4.99.0"/>
# Xamarin.Android 4.99.0

Xamarin.Android 4.99 is a continuation of
[Xamarin.Android 4.17](/releases/android/xamarin.android_4/xamarin.android_4.17/).

## New Features

* OpenGLES 3.1 Support
* [Android API-L](https://developer.android.com/preview/api-overview.html) Support.
* [Android Wear](https://developer.android.com/design/wear/structure.html) Support.
* New tool, `logcat-parse`, for investigating GREF use.
* New tool, `class-parse`, for binding `.jar` files.

## Breaking Changes

* Property setters are no longer generated for Java `final` fields.
    (This accounts for *most* of changes in the API Changes, below.)

* The default `//uses-sdk/@android:minSdkVersion` value in previous releases
    defaulted to `$(TargetFrameworkVersion)`. It now defaults to API-11.

    This change should make it easier to create new projects and deploy them
    to "older" devices without first visiting Project Options.</p></li>

* Exceptions which cross VM boundaries now participate in Java stack unwinding.
    Behavior of unhandled C# exceptions within the debugger is now different;
    *if* an unhandled exception is reported -- and it may not be when thrown
    from the UI thread -- then the debugger will "break" on the last entry
    into managed code, *not* from where the exception was originally thrown.
    
    The previous behavior may be enabled by exporting the
    `XA_BROKEN_EXCEPTION_TRANSITIONS` environment variable with the value
    `true`.

* Support for `Mono.Android.GoogleMaps.dll`, `Mono.Android.Support.v4.dll`,
    and `Mono.Android.Support.v13.dll` has been removed.
    (All types in these assemblies were obsoleted in
    [Xamarin.Android 4.14](/releases/android/xamarin.android_4/xamarin.android_4.14/))
    
    Please migrate to Xamarin Components:

    * `Mono.Android.GoogleMaps`: Please use the
        [Google Play Services](http://components.xamarin.com/view/googleplayservices)
        component.
    * `Mono.Android.Support.v4.dll`: Please use the
        [Android Support Library v4](http://components.xamarin.com/view/xamandroidsupportv4-18)
        component.
    * `Mono.Android.Support.v13.dll`: Please use the
        [Android Support Library v13](http://components.xamarin.com/view/xamandroidsupportv13-18)
        component.

* Binding assemblies for Android v1.6 (API-4), Android v2.1 (API-7), and
    Android v2.2 (API-8) has been dropped.
    
    Xamarin.Android applications can stil *run* on these platforms, but
    the compiler will no longer assist you in ensuring that types and members
    which do not exist in those API levels are not referenced.

* `JNIEnv.NewObjectArray<T>(T[])` now consistely generates a Java array
    based on `typeof(T)`, instead of probing the runtime type of the first
    non-`null` value within the provided array.
    
* The `$(TargetFrameworkVersion)` scheme is changing. Previously, the
    `$(TargetFrameworkVersion)` values were the Android versions, e.g.
    a `$(TargetFrameworkVersion)` value of `v2.3` was used to target API-10.
    In order to ease the path for future possible API improvements
    (e.g. [Bug #6085](https://bugzilla.xamarin.com/show_bug.cgi?id=6085)),
    we will begin *prefixing* the Android version with the Xamarin.Android
    version. For example, the *new* `$(TargetFrameworkVersion)` for API-10
    will be `v5.2.3`.

## Bug Fixes

* [7634](https://bugzilla.xamarin.com/show_bug.cgi?id=7634):
    Managed > Java > Managed Exception Propoagation is broken.
* [11270](https://bugzilla.xamarin.com/show_bug.cgi?id=11270):
    Linker failure.
* [17257](https://bugzilla.xamarin.com/show_bug.cgi?id=17257):
    `NoSuchMethodError` when using `TreeViewObserver.GlobalLayout` on targets
    before API level 16.
* [21361](https://bugzilla.xamarin.com/show_bug.cgi?id=21361):
    Attribute *name* has already been defined, when having attributes defined
    in a Android Class Library and using Android Binding component
* [22218](https://bugzilla.xamarin.com/show_bug.cgi?id=22218):
    [generator] Parameter marshaling is not exception-safe.
* [22955](https://bugzilla.xamarin.com/show_bug.cgi?id=22955):
    Basic DateTime calcutions are now throwing exceptions.
* [22962](https://bugzilla.xamarin.com/show_bug.cgi?id=22962):
    `@deprecated` annotations aren't mapped to C#'s `[Obsolete]` attribute.
* [22991](https://bugzilla.xamarin.com/show_bug.cgi?id=22991):
    System.DateTime uses too many GREFs.
* [23077](https://bugzilla.xamarin.com/show_bug.cgi?id=23077):
    Wrap DriveInfo to StatFs.
* [23167](https://bugzilla.xamarin.com/show_bug.cgi?id=23167):
    XML View names not updated.
* [23564](https://bugzilla.xamarin.com/show_bug.cgi?id=23564):
    Setting `WindowSoftInputMode` to `SoftInput.AdjustNothing` on `Activity`
    generates an out of range exception on compilation.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 3.10](http://www.mono-project.com/Release_Notes_Mono_3.10)
[commit 1e709688](https://github.com/mono/mono/commit/1e709688bb2dd61aa6a040456d689742bf755ed8).

* [1852](https://bugzilla.xamarin.com/show_bug.cgi?id=1852):
    XmlSerialization ignores `ShouldSerialize` and `Specified`.
* [6512](https://bugzilla.xamarin.com/show_bug.cgi?id=6512):
    Don't parse JSON when using GET.
* [15514](https://bugzilla.xamarin.com/show_bug.cgi?id=15514):
    Catch exceptions thrown by SerialPortStream.Dispose () when
    called from the finalizer.
* [18422](https://bugzilla.xamarin.com/show_bug.cgi?id=18422):
    `HttpClient` doesn't support 'name[]' header field name format
* [19012](https://bugzilla.xamarin.com/show_bug.cgi?id=19012):
    `XmlArrayItemAttribute.IsNullable` default does not match .NET default
* [20403](https://bugzilla.xamarin.com/show_bug.cgi?id=20403):
    `InvalidOperationException` when XML-serializing `System.Drawing.Color`.
* [21571](https://bugzilla.xamarin.com/show_bug.cgi?id=21571):
    `Uri.GetComponents()` should allow `UriComponents.SerializationInfoString`
    on relative Uri
* [21653](https://bugzilla.xamarin.com/show_bug.cgi?id=21653):
    App crashed attempting to debug: Assertion, `mono_error_ok (&error)` not met.
* [21930](https://bugzilla.xamarin.com/show_bug.cgi?id=21930):
    UmAlQuraCalendar fundamentally broken.
* [22129](https://bugzilla.xamarin.com/show_bug.cgi?id=22129):
    web reference working correctly in windows type project but not in android.
* [22212](https://bugzilla.xamarin.com/show_bug.cgi?id=22212):
    Error parsing DateTime string in New Zealand Culture.
* [22383](https://bugzilla.xamarin.com/show_bug.cgi?id=22383):
    `HttpClient`'s `RequestMessage.RequestUri.AbsoluteUri` don't automatically
    point to right ones on 302.
* [22417](https://bugzilla.xamarin.com/show_bug.cgi?id=22417):
    `DateTime.Parse()` does not correctly recognize the date with correct format.
* [22558](https://bugzilla.xamarin.com/show_bug.cgi?id=22558):
    `DateTimeOffset.Parse()` can't handle the dateTime string without time part.
* [22591](https://bugzilla.xamarin.com/show_bug.cgi?id=22591):
    Default `BigInteger()` causes exceptions and incorrect answers
* [22685](https://bugzilla.xamarin.com/show_bug.cgi?id=22685):
    <code>Assertion at mini.c:4656, condition `cfg->code_size - 
    cfg->epilog_begin < 0xffff' not met</code>
* [22704](https://bugzilla.xamarin.com/show_bug.cgi?id=22704):
    ClientWebSocket cannot handle reading subsets of the payload.
* [22724](https://bugzilla.xamarin.com/show_bug.cgi?id=22724):
    Mono `HttpClientHandler` does not support concurrent requests (Corrupts state).
* [22764](https://bugzilla.xamarin.com/show_bug.cgi?id=22764):
    HTTP POST ContentType is null instead of one sent by client in case of
    MultipartFormDataContent.
* [22851](https://bugzilla.xamarin.com/show_bug.cgi?id=22851):
    `DateTimeOffset.Parse()` doesn't handle RFC1123 formatted timestamps correctly.
* [22857](https://bugzilla.xamarin.com/show_bug.cgi?id=22857):
    `DirectoryInfo.EnumerateFileSystemInfos()` with
    `SearchOption.AllDirectories` does not return all subdirectories.
* [23021](https://bugzilla.xamarin.com/show_bug.cgi?id=23021):
    Calls from generic shared methods not always patched.
* [23206](https://bugzilla.xamarin.com/show_bug.cgi?id=23206):
    MS allows threadpool threads to be renamed multiple times.
* [23318](https://bugzilla.xamarin.com/show_bug.cgi?id=23318):
    `XComment` throws an exception with some inputs
* [23376](https://bugzilla.xamarin.com/show_bug.cgi?id=23376):
    TimeSpan returns incorrect result.
* [23438](https://bugzilla.xamarin.com/show_bug.cgi?id=23438):
    ECMA-335 Type layout attributes and atomic operations: a generic type shall
    not have explicit layout - NUnit test cases are attached, written in F#

<a name="API_Changes" />
# API Changes

* API Level 10:
    [Mono.Android.dll](xamarin.android_4.99/level_10_diff/mono.android.dll),
    [OpenTK.dll](xamarin.android_4.99/level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](xamarin.android_4.99/level_10_diff/opentk-1.0.dll)
* API Level 12:
    [Mono.Android.dll](xamarin.android_4.99/level_12_diff/mono.android.dll),
* API Level 14:
    [Mono.Android.dll](xamarin.android_4.99/level_14_diff/mono.android.dll),
* API Level 15:
    [Mono.Android.dll](xamarin.android_4.99/level_15_diff/mono.android.dll),
* API Level 16:
    [Mono.Android.dll](xamarin.android_4.99/level_16_diff/mono.android.dll),
* API Level 17:
    [Mono.Android.dll](xamarin.android_4.99/level_17_diff/mono.android.dll),
* API Level 18:
    [Mono.Android.dll](xamarin.android_4.99/level_18_diff/mono.android.dll),
* API Level 19:
    [Mono.Android.dll](xamarin.android_4.99/level_19_diff/mono.android.dll),

