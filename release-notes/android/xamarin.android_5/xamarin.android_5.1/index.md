---
id: 47FA9AD3-5CA3-41B7-8ADA-B34B79261020
title: "Xamarin.Android 5.1"
---

The Xamarin.Android 5.1 series provides improved support for
[Android Wear apps](https://developer.android.com/design/wear/structure.html).

**Note:** Xamarin.Android 5.1 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21.
JDK 1.6 may be used when targeting previous API levels.


<!--
  JONP: 5.1.7 last updated from commit monodroid/monodroid-5.1-series/e995785a7de1e4b5a28727ddb116367e2819a5ca
-->

<a name="7"/>
<a name="Xamarin.Android_5.1.7"/>
# Xamarin.Android 5.1.7

Xamarin.Android 5.1.7 adds support for [Android 6.0 Marshmallow (API-23)][api-23].

Please see the separate [Xamarin.Android 5.1.7 release notes][xa-5.1.7] for API diffs.

[xa-5.1.7]: /releases/android/xamarin.android_5/xamarin.android_5.1.7/

<!--
  JONP: 5.1.6 last updated from commit monodroid/monodroid-5.1-series-c5sr4/58099c5358da3488b0e7fb0bb4af47aca7cc61d6
-->

<a name="6"/>
<a name="Xamarin.Android_5.1.6"/>
# Xamarin.Android 5.1.6

Xamarin.Android 5.1.6 improves reliability and stability.

## Bug Fixes

* [31705](https://bugzilla.xamarin.com/show_bug.cgi?id=31705):
    Embedded resources are not being fast deployed from the IDE in XA 5.1.4+
* [32025](https://bugzilla.xamarin.com/show_bug.cgi?id=32025):
    Android library assets in subfolders not added to apk.
* [33554](https://bugzilla.xamarin.com/show_bug.cgi?id=33554):
    monodroid error XA0000: Reason: An element with the same key already exists in the dictionary

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.3/)
[commit 5ab4c0d0](https://github.com/mono/mono/commit/5ab4c0d099a69de2a2ef5d1cf8d83e78df4d6af8).

* [28777](https://bugzilla.xamarin.com/show_bug.cgi?id=28777):
    `GZipStream` (`DeflateStreamNative`) native exception after `Flush()` with
    no buffer data: Internal error (no progress possible) Flush
* [30043](https://bugzilla.xamarin.com/show_bug.cgi?id=30043):
    Disposing a `FileSystemWatcher` object causes `ArgumentOutOfRangeException`
* [30868](https://bugzilla.xamarin.com/show_bug.cgi?id=30868):
    `ObjectDisposedException` in mono 4.0.1.28, but not mono 3.12.1
* [30869](https://bugzilla.xamarin.com/show_bug.cgi?id=30869):
    `HttpClient` authentication not working

<!--
  JONP: 5.1.5 last updated from commit monodroid/monodroid-5.1-series-c5sr3/f98871a95a479f6d71b3067b7e5834d41fcb2118
-->

<a name="5"/>
<a name="Xamarin.Android_5.1.5"/>
# Xamarin.Android 5.1.5

Xamarin.Android 5.1.5 improves reliability and stability, and adds bindings for
[Android v5.1 (API-22)][api-22].

[api-22]: https://developer.android.com/about/versions/android-5.1.html

## Bug Fixes

* [28114](https://bugzilla.xamarin.com/show_bug.cgi?id=28114):
    Fatal signal 6 (SIGABRT) if `Keyboard.CreateKeyFromXml()` is overriden.
* [28721](https://bugzilla.xamarin.com/show_bug.cgi?id=28721):
    aapt error item with same key
* [29571](https://bugzilla.xamarin.com/show_bug.cgi?id=29571):
    Custom `[Preserve]` attribute only works under the `Android.Runtime`
    namespace on Android
* [30823](https://bugzilla.xamarin.com/show_bug.cgi?id=30823):
    Aot task fails when the linker is disabled
* [31527](https://bugzilla.xamarin.com/show_bug.cgi?id=31527):
    Unable to load file or assembly `System.Runtime` in project with both
    shared runtime and Link SDK enabled.
* [31597](https://bugzilla.xamarin.com/show_bug.cgi?id=31597):
    Xamarin.Android Breakpoints in certain projects no longer work after
    upgrading to 5.1.4.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit 5f447f9d](https://github.com/mono/mono/commit/5f447f9df5f2d239aa5a8d3b6ea1b6ecffb757fa).

* [26205](https://bugzilla.xamarin.com/show_bug.cgi?id=26205):
    `System.IO.Package.LoadRelationships` throws `NullReferenceException` for
    some NuGet packages with PCLs generated on Windows.

<!--
  JONP: 5.1.4 last updated from commit monodroid/monodroid-5.1-series-c5sr2/a2c4ca8317212fcc54f2c92572a6049fc85806bd
-->

<a name="4"/>
<a name="Xamarin.Android_5.1.4"/>
# Xamarin.Android 5.1.4

Xamarin.Android 5.1.4 improves reliability and stability.

## Bug Fixes

* Various AOT-related fixes.
* [29130](https://bugzilla.xamarin.com/show_bug.cgi?id=29130):
    Fix loading of `libmonosgen-2.0.so` when loading the shared runtime within
    a Release build.
* [29939](https://bugzilla.xamarin.com/show_bug.cgi?id=29939):
    Fix build error when building android application which references a file
    with an UPPER_CASE letter in `styles.xml`.
* [30318](https://bugzilla.xamarin.com/show_bug.cgi?id=30318),
    Xamarin.Android Breakpoints in Forms PCL project do not work after cleaning
    solution, redeploying, and restarting debugging.
* [30670](https://bugzilla.xamarin.com/show_bug.cgi?id=30670),
    [30827](https://bugzilla.xamarin.com/show_bug.cgi?id=30827):
    Support binding Java libraries with package names that end in `.system`.
* [30823](https://bugzilla.xamarin.com/show_bug.cgi?id=30823):
    Support AOT compilation when linking is disabled.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit 046a4260](https://github.com/mono/mono/commit/046a4260654ddac5b05d322486053d9557bc52de).

* Fixes `TimeZoneInfo.IsDaylightSavingTime` returning `false` when
    `TimeZoneInfo.SupportsDaylightSavingTime` was set to false because the
    `TimeZoneInfo` was created with no `AdjustmentRules`.

* [28747](https://bugzilla.xamarin.com/show_bug.cgi?id=28747):
    Nexus 9 sample apps crashing on launch.
* [28961](https://bugzilla.xamarin.com/show_bug.cgi?id=28961):
    Avoid duplicate plt symbols for plt entries for synchronized methods.
* [29935](https://bugzilla.xamarin.com/show_bug.cgi?id=29935):
    XAttribute.ToString() outputs wrong result if attribute contains namespace.

<!--
  JONP: 5.1.3 last updated from commit monodroid/monodroid-5.1-series/d419c934e6ce2113653ff4c40214e3a5d5a69440
-->

<a name="3"/>
<a name="Xamarin.Android_5.1.3"/>
# Xamarin.Android 5.1.3

Xamarin.Android 5.1.3 improves compatibility with the latest Android SDK
Build-tools `23.0.0_rc1` and the Android-M preview.

## Bug Fixes


* [30653](https://bugzilla.xamarin.com/show_bug.cgi?id=30653),
    [30555](https://bugzilla.xamarin.com/show_bug.cgi?id=30555),
    [30562](https://bugzilla.xamarin.com/show_bug.cgi?id=30562):
    Check for new Build-tools `23.0.0_rc1` location of `aapt`.
* [30566](https://bugzilla.xamarin.com/show_bug.cgi?id=30566):
    Creating `Java.Lang.String` instances on the Android-M preview
    results in an `UnsupportedOperationException: Use StringFactory instead`.
    ([Related Android bug](https://code.google.com/p/android-developer-preview/issues/detail?id=2073))

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit ed1d3ec5](https://github.com/mono/mono/commit/ed1d3ec5260b613849b9af27c9dbcb6566c1637c).

* [29667](https://bugzilla.xamarin.com/show_bug.cgi?id=29667):
    Mono v4.0 crashes after a while.
* [30171](https://bugzilla.xamarin.com/show_bug.cgi?id=30171):
    `BinaryReader.ReadChar()` returns incorrect result on 8.10


<!--
  JONP: 5.1.2 last updated from commit monodroid/monodroid-5.1-series/2485523223ffb88567f101866d5f73da7a37ca53
-->

<a name="2"/>
<a name="Xamarin.Android_5.1.2"/>
# Xamarin.Android 5.1.2

Xamarin.Android 5.1.2 contains stability fixes.

## Bug Fixes

* Improve legacy type name fixing within `AndroidManifest.xml`.
* [28198](https://bugzilla.xamarin.com/show_bug.cgi?id=28198):
    `LinkAssemblies` task failed with a `NotImplementedException`.
* [29263](https://bugzilla.xamarin.com/show_bug.cgi?id=29263):
    `android.view.InflateException` when defining a custom preference .
* [29568](https://bugzilla.xamarin.com/show_bug.cgi?id=29568):
    Android 5.1 AppCompat 22.1.1 unable to find theme resources.


## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit d7f9ffaa](https://github.com/mono/mono/commit/d7f9ffaa25d45316db27df4892c4c30533ed646e).

* [26998](https://bugzilla.xamarin.com/show_bug.cgi?id=26998):
    Issue with `DataContractJsonSerializer`.
* [29039](https://bugzilla.xamarin.com/show_bug.cgi?id=29039):
    `CultureInfo.GetCultures(CultureTypes.SpecificCultures)` returns
    broken `ar-SA` culture.
* [29177](https://bugzilla.xamarin.com/show_bug.cgi?id=29177):
    Check SP on thread suspend correctly.

<!--
  JONP: 5.1.1 last updated from commit monodroid/monodroid-5.1.1-hotfix-29570-branch/3518c4ceb984ffea1f5d972ea9c09eb27738d565
-->

<a name="1"/>
<a name="Xamarin.Android_5.1.1"/>
# Xamarin.Android 5.1.1

Xamarin.Android 5.1.1 is a hotfix release to fix operations on `System.Decimal`.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit d5e006eb](https://github.com/mono/mono/commit/d5e006eb1fc8e8b85f80826746eb8df661f1927c).

* [29570](https://bugzilla.xamarin.com/show_bug.cgi?id=29570):
    `decimal` comparisons look to be broken.


<!--
  JONP: 5.1.0 last updated from commit monodroid/monodroid-5.1-series/180ccc70d17d9fd4adc2ff2bcc43f956aa72b293
-->

<a name="0"/>
<a name="Xamarin.Android_5.1.0"/>
# Xamarin.Android 5.1

<a name="new-features-5.1" />
## New Features

* [Simpler Android Wear support](#Simpler_Android_Wear_Support).
* [64-bit runtime support](#64-bit_Runtime_Support).
* [System app support](#System_App_Support).
* [Proguard support](#Proguard_Support).
* [Multi-Dex support](#Multi-Dex_Support).
* [GC-free method invocations](#GC-free-Method_Invocations).
* [AppDomain.UnhandledException event raised for Java exceptions](#AppDomain.UnhandledException_Event_Raised_For_Java_Exceptions)
* OpenGLES 3.1 Support
* New tool, `logcat-parse`, for investigating GREF use.
* F# bumped to [3.1.1.31](https://github.com/fsharp/fsharp/tree/3.1.1.31).
* New `$(JavacTargetVersion)` and `$(JavacSourceVersion)` MSBuild properties
    can control the `javac -target` and `javac -source` values.
* New `debug.mono.max_grefc` system property, allows overriding the default
    detected maximum GREF count value.


<a name="Simpler_Android_Wear_Support" />
### Simpler Android Wear Support

Previously, Android Wear apps were supported, but required lots of extra manual
intervention in order to follow the
[Android Wear app structure](https://developer.android.com/design/wear/structure.html)
and the
[manual packaging instructions](https://developer.android.com/training/wearables/apps/packaging.html#PackageManually):

1. Ensure that your Wearable project and Handheld projects had the *same* version number *and package name*.
2. Manually build the Wearable project *as a Release build*
3. Manually add (2) into the `Resources\raw` directory of the Handheld project.
4. Manually write an XML blob within the Handheld project which refers to (3).
5. Manually add a `<meta-data/>` element to the Handheld project's `AndroidManifest.xml`.

Starting in Xamarin.Android 5.0, there is a new, simpler, workflow:

1. Add the Wear project as a Project Reference to the Handheld project.

This will automatically package the Wear app and include it as a resource
when building the Handheld project.

The package name of the Wear project and the Handheld project *must* have the
same package name. If they don't, then an `XA5304` error will be reported.

<a name="System_App_Support" />
### System App Support

Many customers have requested that Xamarin.Android be usable as "system apps"
on custom AOSP builds. This should now be supported.


<a name="Proguard_Support"></a>
### Proguard Support

[Proguard][proguard] is used to link Java bytecode, allowing `.apk` files
to be smaller.

[proguard]: http://developer.android.com/tools/help/proguard.html

Proguard support can be enabled by using the new `$(EnableProguard)`
MSBuild property, which is also available via Visual Studio and Xamarin Studio.

Additionally, a new `@(ProguardConfiguration)` **Build action** has been added.
Files with a Build action of `@(ProguardConfiguration)` are used as values to
the `proguard -include` option.

The *contents* of a `@(ProguardConfiguration)` file contain additional
[proguard options](http://proguard.sourceforge.net/manual/usage.html).


<a name="Multi-Dex_Support"></a>
### Multi-Dex support

Android apps may have at most 65k methods within the `.apk`.
[Multi-dex][multidex] is a way to increase this method limit.

[multidex]: http://developer.android.com/tools/building/multidex.html

Multi-dex support can be enabled by using the new `$(AndroidEnableMultiDex)`
MSBuild property, which is also available via Visual Studio and Xamarin Studio.


<a name="GC-free-Method_Invocations"></a>
### GC-free Method Invocations

In previous versions of Xamarin.Android, when invoking Java methods that had
one or more parameters, a `JNIEnv` method would be invoked with a
`params JValue[]` parameter. This resulted in array allocations on every such
method invocation, increasing GC allocations and memory pressure.

Starting with Xamarin.Android 5.1, there are new `JNIEnv` method overloads
which instead take a `JValue*` (unsafe pointer), and the bindings have been
updated to make use of the new overloads instead of using the previous
`params JValue[]` overload.

Existing Java library bindings must be rebuilt to make use of the new
methods, and Java library bindings built against Xamarin.Android 5.1
will not be usable in previous versions.


<a name="AppDomain.UnhandledException_Event_Raised_For_Java_Exceptions"></a>

### AppDomain.UnhandledException Event Raised For Java Exceptions

In previous versions of Xamarin.Android, the `AppDomain.UnhandledException`
event would only be raised for exceptions thrown from managed code, and not
for unhandled Java exceptions thrown on Java threads.

Starting with Xamarin.Android 5.1, the `AppDomain.UnhandledException` event
should be raised for any and all unhandled exceptions, whether raised from
managed code or from Java code.


<a name="experimental-features" />
## Experimental Features

Xamarin.Android 5.1 introduces several experimental features:

* [64-bit Runtime Support](#64-bit_Runtime_Support)
* [AOT Support](#AOT_Support)


<a name="64-bit_Runtime_Support"> </a>
### 64-bit Runtime Support

Xamarin.Android now provides runtimes for `arm64-v8a` and `x86_64`. This allows
Xamarin.Android apps to run as 64-bit apps on supported hardware.

*Note*: 64-bit runtimes are *not* required in order to run on 64-bit hardware.
64-bit devices such as the [Nexus 9][nexus9] are capable of running 32-bit
processes as well. 64-bit runtimes merely allow the process to access more
memory, as long as Android grants access to it.

[nexus9]: http://www.google.com/nexus/9/


<a name="AOT_Support"> </a>
### AOT support

Xamarin.Android now supports Ahead-of-Time (AOT) compilation of assemblies,
allowing some JIT overhead to be avoided. This can result in shorter
startup times, at the cost of increased .apk sizes.

AOT may be enabled by using the new `$(AotAssemblies)` MSBuild property,
and the LLVM Optimizing Compiler may be used by enabling the new `$(EnableLLVM)`
MSBuild property,
both of which will be available via Visual Studio and Xamarin Studio.

TODO: Table comparing startup times, .apk sizes.

Unfortunately, AOT support is *experimental* at the moment:

* LLVM can't be used when building for `x86_64`, because of an
    [Android NDK bug](https://code.google.com/p/android/issues/detail?id=161422).
* AOT and AOT+LLVM on `x86` are known to be unstable.
* AOT+LLVM on `arm64-v8a` is known to be unstable.


<a name="workflow-changes-5.1" /> </a>
## Workflow Changes

There are several changes which may alter the development workflow in this release.

* [Change `minSdkVersion` Default Value](#Change_minSdkVersion_Default_Value).
* [Cross-VM Exception Propagation](#Cross-VM_Exception_Propagation).
* [`JNIEnv.NewObjectArray()` Array Type](#JNIEnv.NewObjectArray_Array_Type).
* [`ApplicationInfo.nativeLibraryDir` Use](#ApplicationInfo.nativeLibraryDir_Use).
* [GREF Logging Changes](#GREF_Logging_Changes).

<!--
Fun fact: e.g. Android.OS.Debug.MemoryInfo.Creator could be set to e.g. null,
and the Java-side value would be changed! Imagine the havoc this would cause
if/when Java needed MemoryInfo.CREATOR...
  -->

<a name="Change_minSdkVersion_Default_Value" />
### Change minSdkVersion Default Value

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


<a name="Cross-VM_Exception_Propagation" />
### Cross-VM Exception Propagation

Exceptions which cross VM boundaries now participate in Java stack unwinding.
Behavior of unhandled C# exceptions within the debugger is now different;
*if* an unhandled exception is reported -- and it may not be when thrown
from the UI thread -- then the debugger will "break" on the last entry
into managed code, *not* from where the exception was originally thrown.

The previous behavior may be enabled by exporting the
`XA_BROKEN_EXCEPTION_TRANSITIONS` environment variable with the value
`true`.


<a name="JNIEnv.NewObjectArray_Array_Type" />
### `JNIEnv.NewObjectArray()` Array Type

`JNIEnv.NewObjectArray<T>(T[])` now consistently generates a Java array
based on `typeof(T)`, instead of probing the runtime type of the first
non-`null` value within the provided array.

<!-- I have no idea what I was thinking with using the runtime type... -->


<a name="ApplicationInfo.nativeLibraryDir_Use" />
### `ApplicationInfo.nativeLibraryDir` Use

Previously, native libraries were assumed to be in
[`ApplicationInfo.dataDir + "/lib"`](http://developer.android.com/reference/android/content/pm/ApplicationInfo.html#dataDir)...
because that was the only thing that would work on API-4.

Unfortunately, that logic no longer works for 64-bit platforms, as native
libraries for 64-bit platforms are in a different (variable) location.
64-bit runtime support instead requires searching for native libraries
within the directory stored in
[`ApplicationInfo.nativeLibraryDir`](http://developer.android.com/reference/android/content/pm/ApplicationInfo.html#nativeLibraryDir).

To support 64-bit runtimes, when `AndroidManifest.xml` contains a `//uses-sdk`
element with an `android:minSdkVersion` attribute value that is 10 or later,
then native libraries will instead be searched within
`ApplicationInfo.nativeLibraryDir`. If the `android:minSdkVersion` attribute
value is less than 10, then the previous behavior will be used.

As a consequence of this, *it is not possible* for applications to contain
*both* an `android:minSdkVersion` value that is less than 10 *and* 
provide 64-bit runtime support.


<a name="GREF_Logging_Changes" />
### GREF Logging Changes

It was recently discovered that `adb logcat` on Android 5.0 Lollipop will
*drop* messages if "too many" are written. (Previously, `adb logcat` was
documented as using a ring buffer, which would cause the *oldest* messages
to be dropped if "too many" are written. What we've observed is that *recent*
messages will be dropped on Lollipop, not the oldest.)

As a result of this, JNI Global Reference (GREF) logging is nearly worthless
when running on Lollipop, as important GREF handle lifetime messages may be
lost, resulting in loss of hair and sanity as JNI handle values
"appear out of nowhere".

To address this, GREF logging is *changing* with Xamarin.Android 5.1. It is
still enabled via the `debug.mono.log` system property
(e.g. `adb shell setprop debug.mono.log gref`), but now when it's
enabled there are two changes of note:

1. `adb logcat` messages *will not* contain full stack traces.
    These messages will only be useful at providing a "current" value
    of the number of GREFs which exist as the app runs, and not analysis.
2. Full JNI handle information will now be written to the package's
    `files/.__override__/grefs.txt` file.

Once the app is running or has finished running (after closing the app or a
crash), GREF information may be copied via:

    adb shell run-as @PACKAGE_NAME@ cat files/.__override__/grefs.txt

in which `@PACKAGE_NAME@` is the package name of the app.

The `debug.mono.log` system property may also contain a path name for where
the GREF logging information should be written:

    adb shell setprop debug.mono.log gref=/path/to/grefs.txt

*Note*: To perform the above `adb shell run-as` command, the app must also be
[debuggable](http://developer.android.com/guide/topics/manifest/application-element.html#debug).
Debug configuration builds are debuggable by default; Release builds are not.
If a Release build needs to log GREF and provide information, it can be made
debuggable by doing one of the following:

1. Edit `Properties\AndroidManifest.xml` and edit the `<application/>`
    element to add the attribute content:

        android:debuggable="true"

2. Edit `Properties\AssemblyInfo.cs` and add the following custom attribute:

        [assembly: Application (Debuggable=true)]

*Note*: `grefs.txt` can get *very* large, and may consume lots of disk space
on the target device.

*Note*: `grefs.txt` is deleted on app startup.


<a name="breaking-changes-5.1" /> </a>
## Breaking Changes

There are several breaking changes in this release, many of which have been
hinted at previously via `[Obsolete]` messages, some of which are *semantic*
changes which won't break compilation but *may* affect runtime behavior.

* [Removal Of Property Setters for `final` Fields](#Removal_Of_Property_Setters_for_final_Fields).
* [Removal of API Levels](#Removal_of_API_Levels).
* [Removal of Obsolete Assemblies](#Removal_of_Obsolete_Assemblies).
* [Android Callable Wrapper Naming](#Android_Callable_Wrapper_Naming).


<a name="Removal_Of_Property_Setters_for_final_Fields" />
### Removal Of Property Setters for `final` Fields

Property setters are no longer generated for Java `final` fields.
(This accounts for *most* of changes in the API Changes, below.)
The property setters were present due to oversight, and should not
have been used.

<a name="Removal_of_API_Levels" />
### Removal of API Levels

Binding assemblies for Android v1.6 (API-4), Android v2.1 (API-7),
Android v2.2 (API-8), Android v3.1 (API-12), and Android v4.0 (API-14)
has been dropped.

Xamarin.Android applications can still *run* on these platforms, but
the compiler will no longer assist you in ensuring that types and members
which do not exist in those API levels are not referenced.

<a name="Removal_of_Obsolete_Assemblies" />
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

<a name="Android_Callable_Wrapper_Naming" />
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

To assist with the transition, `AndroidManifest.xml` will be checked
for references to previously generated type names and all such references
will be automatically fixed up to use the new convention. This only affects
the contents of `AndroidManifest.xml`.


<a name="Bug_Fixes"/>
## Bug Fixes

* Numerious MSBuild target cleanup and improvements
* Fix `System.Linq.Expressions` linking
* Add `Android.App.ActivityAttribute.Immersive` property value, which sets the
    [`//activity/@android:immersive` attribute value](http://stackoverflow.com/questions/21450077/what-is-androidimmersive-attribute-in-android-manifest-file).
* Generate XA0101 warning if the `@(Content)` **Build action** is used, as the
    `@(Content)` Build action can't be supported.
* Improve display of `aapt` errors within the IDE errors panel.
* [2461](https://bugzilla.xamarin.com/show_bug.cgi?id=2461)
    The `AppDomain.UnhandledException` event doesn't work.
* [7634](https://bugzilla.xamarin.com/show_bug.cgi?id=7634):
    Managed > Java > Managed Exception Propoagation is broken.
* [8470](https://bugzilla.xamarin.com/show_bug.cgi?id=8470):
    Support Deploying to Android 4.2+ with non-admin current user.
* [10268](https://bugzilla.xamarin.com/show_bug.cgi?id=10268):
    Linker issue with horizontallistview project in release mode.
* [11270](https://bugzilla.xamarin.com/show_bug.cgi?id=11270):
    Linker failure.
* [12935](https://bugzilla.xamarin.com/show_bug.cgi?id=12935):
    `sensorPortrait` should be `sensorPortait` on API < 16
* [13154](https://bugzilla.xamarin.com/show_bug.cgi?id=13154):
    Display SHA1 fingerprint of the keystore that was used to sign an `.apk`.
* [15205#c1](https://bugzilla.xamarin.com/show_bug.cgi?id=15205#c1), [16826](https://bugzilla.xamarin.com/show_bug.cgi?id=16826), [21147](https://bugzilla.xamarin.com/show_bug.cgi?id=21147):
    Support same namespace+type in separate assemblies for `Java.Lang.Object` subclasses.
* [16409](https://bugzilla.xamarin.com/show_bug.cgi?id=16409):
    Fix `InvalidOperationException` from `AndroidEnvironment._Proxy.Credentials` property.
* [16805](https://bugzilla.xamarin.com/show_bug.cgi?id=16805):
    Allow `<fragment class="...">` to contain assembly-qualified type names.
* [16826](https://bugzilla.xamarin.com/show_bug.cgi?id=16826):
    ACWs: Create unique package names instead of lowercasing the namespace.
* [17257](https://bugzilla.xamarin.com/show_bug.cgi?id=17257):
    `NoSuchMethodError` when using `TreeViewObserver.GlobalLayout` on targets
    before API level 16.
* [17313](https://bugzilla.xamarin.com/show_bug.cgi?id=17313):
    Properly generate `XPath method reference` comments within generated bindings code.
* [19391](https://bugzilla.xamarin.com/show_bug.cgi?id=19391):
    `[Preserve(AllMembers=true)]` not working when `[DataContract]` is after it.
* [21034](https://bugzilla.xamarin.com/show_bug.cgi?id=21034):
    `mandroid` generates `XA0000` for `Out of memory`.
* [21159](https://bugzilla.xamarin.com/show_bug.cgi?id=21159):
    Incorrect `super()` constructor invocation generated in
    Android Callable Wrappers for `Android.Graphics.Canvas` subclasses.
* [21361](https://bugzilla.xamarin.com/show_bug.cgi?id=21361):
    Attribute *name* has already been defined, when having attributes defined
    in a Android Class Library and using Android Binding component
* [21578](https://bugzilla.xamarin.com/show_bug.cgi?id=21578):
    `System.Net.Sockets.Socket.SetSocketOption` removed by the linker.
* [22155](https://bugzilla.xamarin.com/show_bug.cgi?id=22155):
    Fix `jar2xml` to properly emit generic type constraints.
* [22218](https://bugzilla.xamarin.com/show_bug.cgi?id=22218):
    [generator] Parameter marshaling is not exception-safe.
* [22670](https://bugzilla.xamarin.com/show_bug.cgi?id=22670):
    Build warnings after referencing Microsoft.Net.Http NuGet package in Xamarin.Android app project.
* [22912](https://bugzilla.xamarin.com/show_bug.cgi?id=22912):
    `DateTime.Now` gives `NullReferenceException` in other `AppDomain`s.
* [22955](https://bugzilla.xamarin.com/show_bug.cgi?id=22955):
    Basic DateTime calcutions are now throwing exceptions.
* [22959](https://bugzilla.xamarin.com/show_bug.cgi?id=22959):
    `javac` generates `no suitable constructor found for RuntimeException(String,Throwable,boolean,boolean)`
    message when inheriting from `Java.Lang.RuntimeException`.
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
* [23950](https://bugzilla.xamarin.com/show_bug.cgi?id=23950):
    `TimeZone.CurrentTimeZone.GetDaylightChanges()` contains the wrong End value for AEDT.
* [23990](https://bugzilla.xamarin.com/show_bug.cgi?id=23990):
    Error when building a project with a TargetFramework < v2.3 should be improved and standardized.
* [24086](https://bugzilla.xamarin.com/show_bug.cgi?id=24086):
    Fix `TimeZoneInfo` transitions for Asia/Amman.
* [24193](https://bugzilla.xamarin.com/show_bug.cgi?id=24193):
    `generator` generates a `.JavaCast<byte[]>()` expression, which doesn't compile.
* [24206](https://bugzilla.xamarin.com/show_bug.cgi?id=24206):
    "Access to the path `...\obj\Debug\__library_projects__\...\library_project_imports\assets\...` is denied"
    when asset files in class library are marked as read-only
* [24405](https://bugzilla.xamarin.com/show_bug.cgi?id=24405):
    `org.apache.http.impl.auth.BasicScheme` not bound.
* [24497](https://bugzilla.xamarin.com/show_bug.cgi?id=24497):
    Certain APIs break linking due to inter-API-level differences.
* [24612](https://bugzilla.xamarin.com/show_bug.cgi?id=24612):
    Referencing a library project's resources with upper case letters in filenames does not work.
* [24809](https://bugzilla.xamarin.com/show_bug.cgi?id=24809):
    Add support for manifest merging when using Android libraries.
* [24820](https://bugzilla.xamarin.com/show_bug.cgi?id=24820):
    Make temp files for Xamarin.Android that are automatically cleaned.
* [24947](https://bugzilla.xamarin.com/show_bug.cgi?id=24947):
    Current TimeZone is not updated after the system timezone is changed by a java call.
* [25022](https://bugzilla.xamarin.com/show_bug.cgi?id=25022):
    License fails if no network connection.
* [25157](https://bugzilla.xamarin.com/show_bug.cgi?id=25157):
    SierpinskiTetrahedron sample doesn't appear and has loop of output on some devices.
* [25443#c8](https://bugzilla.xamarin.com/show_bug.cgi?id=25443#c8):
    Don't call `JNIEnv::GetObjectRefType()` with a `NULL` JNI handle, to avoid an
    [Android bug](https://code.google.com/p/android/issues/detail?id=83194).
* [25508](https://bugzilla.xamarin.com/show_bug.cgi?id=25508):
    `android.net.wifi.WifiConfiguration.status` not bound.
* [25990](https://bugzilla.xamarin.com/show_bug.cgi?id=25990):
    JIT Crash on Lollipop with SIGSEGV error because Android Callable Wrapper
    static constructor executed from unregistered thread.
* [26074](https://bugzilla.xamarin.com/show_bug.cgi?id=26074):
    `InvalidCastException` from `JNIEnv.GetArray<Java.Lang.Object>(byteArrayArray)`.
* [26617](https://bugzilla.xamarin.com/show_bug.cgi?id=26617):
    `Android.Graphics.Color.Green` isn't really green.
* [26864](https://bugzilla.xamarin.com/show_bug.cgi?id=26864):
    Preserve type reference targets within custom attributes for linking.
* [27408](https://bugzilla.xamarin.com/show_bug.cgi?id=27408):
    Crash in `SynchronizationContext.Post()`.
* [28781](https://bugzilla.xamarin.com/show_bug.cgi?id=28781):
    PCL MDB files are not generated and PCL breakpoints don't work.


<a name="integrated-mono-5.1" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/)
[commit fe127993](https://github.com/mono/mono/commit/fe1279932f36225e0824aa864592a68195891672).

* [1849](https://bugzilla.xamarin.com/show_bug.cgi?id=1849):
    `TimeZoneInfo.ConvertTime()` gives wrong result when converting from UTC to UTC.
* [1852](https://bugzilla.xamarin.com/show_bug.cgi?id=1852):
    XmlSerialization ignores `ShouldSerialize*` and `*Specified`
* [6512](https://bugzilla.xamarin.com/show_bug.cgi?id=6512):
    Don't parse JSON when using GET
* [7716](https://bugzilla.xamarin.com/show_bug.cgi?id=7716):
    Cannot validate signed XML generated on Windows in Linux, and vice versa.
* [14277](https://bugzilla.xamarin.com/show_bug.cgi?id=14277):
    Stepping in static constructor exits.
* [17944](https://bugzilla.xamarin.com/show_bug.cgi?id=17944):
    `mini-amd64.c:492: amd64_patch: Assertion `0' failed.` with
    jagged array ctors which create an array of arrays.
* [18422](https://bugzilla.xamarin.com/show_bug.cgi?id=18422):
    `HttpClient` doesn't support 'name[]' header field name format
* [18800](https://bugzilla.xamarin.com/show_bug.cgi?id=18800):
    `IndexOutOfRangeException` when `MultipartFormDataContent` filename value contains whitespace.
* [19012](https://bugzilla.xamarin.com/show_bug.cgi?id=19012):
    `XmlArrayItemAttribute.IsNullable` default does not match MS.NET default.
* [19039](https://bugzilla.xamarin.com/show_bug.cgi?id=19039):
    Runtime crashes when evaluating `FieldInfo.MetadataToken` in Dynamic Assembly.
* [19334](https://bugzilla.xamarin.com/show_bug.cgi?id=19334):
    Failure at `System.Net.Sockets.NetworkStream.BeginWrite()`.
* [19823](https://bugzilla.xamarin.com/show_bug.cgi?id=19823):
    `InvalidOperationException` in `ServicePoint.RemoveConnectionGroup()`.
* [19881](https://bugzilla.xamarin.com/show_bug.cgi?id=19881):
    `ProductInfoHeaderValue` fails to parse User-Agent string without version
* [20403](https://bugzilla.xamarin.com/show_bug.cgi?id=20403):
    `InvalidOperationException` when XML-serializing `System.Drawing.Color`
* [20764](https://bugzilla.xamarin.com/show_bug.cgi?id=20764):
    `WebMessageFormatter` crashes with `void` return type `OperationContract`
* [21072](https://bugzilla.xamarin.com/show_bug.cgi?id=21072):
    `DataContractSerializer` does not serialize enum flags the same as .net 4.
* [21135](https://bugzilla.xamarin.com/show_bug.cgi?id=21135):
    Deadlock in `WebConnectionStream`.
* [21172](https://bugzilla.xamarin.com/show_bug.cgi?id=21172):
    text field type `nvarchar(max)` is truncated to 4000 chars.
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
* [22346](https://bugzilla.xamarin.com/show_bug.cgi?id=22346):
    Fixed `DeflateStream` native error when handling empty input.
* [22501](https://bugzilla.xamarin.com/show_bug.cgi?id=22501):
    `XmlSchema.Read()` raises `InvalidElementError` for certain inputs which work fine in MS.NET
* [22775](https://bugzilla.xamarin.com/show_bug.cgi?id=22775):
    `BlockingCollection<T>.AddToAny()` only blocks on first collection.
* [22968](https://bugzilla.xamarin.com/show_bug.cgi?id=22968):
    Crash when lazy loading assemblies.
* [23058](https://bugzilla.xamarin.com/show_bug.cgi?id=23058):
    `DataContractJsonSerializer` - Deserialize type incorrect on iOS.
* [23242](https://bugzilla.xamarin.com/show_bug.cgi?id=23242):
    `NullReferenceException` occurs after the call to `int.ToString()` from multiple threads
* [23401](https://bugzilla.xamarin.com/show_bug.cgi?id=23401):
    Sgen's marksweep-conc fails under load test.
* [23423](https://bugzilla.xamarin.com/show_bug.cgi?id=23423):
    `SIGABRT` and crash in `System.Diagnostics.Process`
* [23594](https://bugzilla.xamarin.com/show_bug.cgi?id=23594):
    A task will not complete if an exception is thrown in an attached child task with
    a task continuation that specifies `TaskContinuationOptions.NotOnFaulted`
* [23769](https://bugzilla.xamarin.com/show_bug.cgi?id=23769):
    Getting `NotSupportedException`s when performing reflection on generic types defined in dynamic assemblies
* [23771](https://bugzilla.xamarin.com/show_bug.cgi?id=23771):
    UTF8 Decoder's `Convert()` does not keep internal state between calls when 'flush' parameter is false
* [23808](https://bugzilla.xamarin.com/show_bug.cgi?id=23808):
    HMACSHA256 default ctor creates 64-bit key, expected 64-byte.
* [23954](https://bugzilla.xamarin.com/show_bug.cgi?id=23954):
    Missing checks for overlapping reference and non-reference fields.
* [23966](https://bugzilla.xamarin.com/show_bug.cgi?id=23966):
    `HttpClient.GetStreamAsync()` behaves differently from .NET.
* [24084](https://bugzilla.xamarin.com/show_bug.cgi?id=24084):
    sgen assert in `sgen_obj_get_descriptor()` when frequently allocating
    with `FormatterServices.GetUninitializedObject()`
* [24213](https://bugzilla.xamarin.com/show_bug.cgi?id=24213):
    `ConcurrentBag.TryTake()` returns the same instance twice...
* [24419](https://bugzilla.xamarin.com/show_bug.cgi?id=24419):
    Synchronized static methods of generic classes lock on the open type instead of the closed one
* [24431](https://bugzilla.xamarin.com/show_bug.cgi?id=24431):
    `CultureInfo` constructor error message decimal and hex lcid should be different.
* [24577](https://bugzilla.xamarin.com/show_bug.cgi?id=24577):
    Fatal Unhandled Exсeption: `System.FormatException`
* [24611](https://bugzilla.xamarin.com/show_bug.cgi?id=24611):
    `System.Net.WebException` when using the `FtpWebRequest` with non-ASCII characters in the URL.
* [24704](https://bugzilla.xamarin.com/show_bug.cgi?id=24704):
    `System.Net.Http.HttpClient.PostAsync()` ignores timeout if webproxy isn't accessible.
* [24757](https://bugzilla.xamarin.com/show_bug.cgi?id=24757):
    `LogicalCallContext` not flowing with async calls.
* [24775](https://bugzilla.xamarin.com/show_bug.cgi?id=24775):
    `List<T>.ForEach()` does not throw `InvalidOperationException` when collection was modified.
* [24891](https://bugzilla.xamarin.com/show_bug.cgi?id=24891):
    `Parallel.ForEach()` overload always sets -1 as current element index.
* [25059](https://bugzilla.xamarin.com/show_bug.cgi?id=25059):
    `StructLayout.Pack` >= 16 throws `TypeLoadException` at runtime
* [25087](https://bugzilla.xamarin.com/show_bug.cgi?id=25087):
    `System.Uri` constructor throws an exception when parsing an HTTP URI with
    a username or password that contains certain escaped characters
* [25132](https://bugzilla.xamarin.com/show_bug.cgi?id=25132):
    `SafeHandle` always called with `Dispose(true)`.
* [25158](https://bugzilla.xamarin.com/show_bug.cgi?id=25158):
    `TypeDescriptor.GetConverter(typeof(DateTimeOffset))` do not return `DateTimeOffsetConverter`.
* [25224](https://bugzilla.xamarin.com/show_bug.cgi?id=25224):
    stack overflow after printfn something.
* [25498](https://bugzilla.xamarin.com/show_bug.cgi?id=25498):
    `System.IO.SynchronizedStream` does not call `Close` on wrapped `Stream`.
* [25664](https://bugzilla.xamarin.com/show_bug.cgi?id=25664):
    `FieldInfo.GetValue()` causes segmentation fault when field is of pointer type
* [25679](https://bugzilla.xamarin.com/show_bug.cgi?id=25679):
    Memory leak and buffer overflow in `get_gsharedvt_type()`.
* [25720](https://bugzilla.xamarin.com/show_bug.cgi?id=25720):
    Runtime crashing when evaluating `System.Diagnostics.Process.HasExited` property
* [25808](https://bugzilla.xamarin.com/show_bug.cgi?id=25808):
    `DataContractJsonSerializer` cannot deserialize array to `IEnumerable<T>`.
* [25850](https://bugzilla.xamarin.com/show_bug.cgi?id=25850):
    `SafeHandle.Close()` is not idempotent.
* [25895](https://bugzilla.xamarin.com/show_bug.cgi?id=25895):
    Wrong exception is thrown when calling
    `System.Globalization.CharUnicodeInfo.GetNumericValue(string s, int index)`
    with invalid index
* [25928](https://bugzilla.xamarin.com/show_bug.cgi?id=25928):
    `Barrier` constructed with 0 participants will hang on `AddParticipant`.
* [26008](https://bugzilla.xamarin.com/show_bug.cgi?id=26008):
    Wrong DST when `TimeZoneInfo` has floating date rules.
* [26033](https://bugzilla.xamarin.com/show_bug.cgi?id=26033):
    Set next statement(`CMD_THREAD_SET_IP`) + stepping doesn't work as expected
* [26109](https://bugzilla.xamarin.com/show_bug.cgi?id=26109):
    `System.Net.Http.Headers.RangeHeaderValue` fails to parse with large byte range
* [26127](https://bugzilla.xamarin.com/show_bug.cgi?id=26127):
    `SafeHandle` types + Delegates + `Marshal.GetDelegateForFunctionPointer()` == Possible crash
* [26312](https://bugzilla.xamarin.com/show_bug.cgi?id=26312):
    `webClient.UploadFile(ftpPath, filePath)` adds some header information to the uploaded file..
* [26412](https://bugzilla.xamarin.com/show_bug.cgi?id=26412):
    `ConstructorInfo.ContainsGenericParameters` behaves differently to MS.NET
* [27010](https://bugzilla.xamarin.com/show_bug.cgi?id=27010):
    Difference in `Assembly.GetExportedTypes()` with .NET
* [27036](https://bugzilla.xamarin.com/show_bug.cgi?id=27036):
    Adding the user-agent header to `HttpClient` object throws a `System.FormatException: Invalid format`.
* [27086](https://bugzilla.xamarin.com/show_bug.cgi?id=27086):
    Writing in asynchronous `FileStream` adds 0 bytes at the beginning of the file.
* [27352](https://bugzilla.xamarin.com/show_bug.cgi?id=27352):
    `HttpRequestMessage`: adding Accept header with multiple values fails
* [27386](https://bugzilla.xamarin.com/show_bug.cgi?id=27386):
    `HttpClient` doesn't honor `BaseAddress` with the `Get*Async()` methods.
* [27697](https://bugzilla.xamarin.com/show_bug.cgi?id=27697):
    Debugger crash: error:
    <code>* Assertion at ../../../../../mono/mono/mini/debugger-agent.c:2475, condition `tls' not met</code>
* [28331](https://bugzilla.xamarin.com/show_bug.cgi?id=28331):
    Custom Attributes incompatability
* [28383](https://bugzilla.xamarin.com/show_bug.cgi?id=28383):
    `Marshal.AllocCoTaskMem(0)` incorrectly returns `IntPtr.Zero`.


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

