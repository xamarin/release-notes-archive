---
id: E83019F9-F694-451B-BF12-3BB960C54ED6
title: "Xamarin.Android 7.4"
---

Xamarin.Android 7.4: Something something fixes?

# OSS Core

Xamarin.Android 7.0 is the first release to use the open-source
repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-3) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-3) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).

# System Requirements

Xamarin.Android 7.4 requires
[JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
to use the Android Nougat (API 24) APIs. Using the Android build-tools r24+ package may also
require using JDK 1.8.
You can continue to use earlier versions of the JDK when using earlier build-tools packages
and when targeting earlier Android API levels:

* [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) - up to API 24+

* [JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) - up to API 23

* [JDK 1.6](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase6-419409.html) - up to API 20

Additionally, a 64-bit version of the JDK is required to use
[custom controls in the Android designer][gui-designer].

[gui-designer]: https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.2/#androiddesignercustomcontrols

**The simplest option is to install the 64-bit version of JDK 1.8 since it is
backwards compatible with all of the previous API levels and supports the new
Android designer features.**


# Vulkan Support

Android v7.0 Nougat adds support for the
[Vulkan API](https://developer.android.com/ndk/guides/graphics/index.html).
Vulkan support will *not* be distributed as part of the core Xamarin.Android
binding. Instead, please use the
[VulkanSharp](https://www.nuget.org/packages/VulkanSharp/) NuGet package, and the
[XLogo sample app](https://github.com/mono/VulkanSharp/tree/master/samples/XLogo).


# Native Library Use

Due to a change by Google,
[Android N will now only permit linking to NDK-provided native libraries][ndk].
`libsqlite.so` is *not* an NDK-provided native library. Consequently,
existing apps using e.g. `Mono.Data.Sqlite.dll` *will* ***crash*** when
running on Android N. This may include other SQLite-using assemblies,
not distributed with Xamarin.Android.

[ndk]: https://developer.android.com/about/versions/nougat/android-7.0-changes.html#ndk

Xamarin.Android 7.0 [updated `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to
include a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

**All Developers** need to audit their code for P/Invoke and ensure that referenced
native libraries are either included in the Android NDK, or are included within
the `app.apk` itself. The only Xamarin.Android-provided assembly impacted by
this change is `Mono.Data.Sqlite.dll`.


# Known Issues

Xamarin.Android [changed the default GC Bridge](#gc-bridge-tarjan) from
`old` to `tarjan`.

Unfortunately, a [few bugs](https://bugzilla.xamarin.com/show_bug.cgi?id=47577)
have been reported which suggest a bug within the Tarjan GC bridge.

If this happens, [create an `@(AndroidEnvironment)` file](/guides/android/advanced_topics/environment/)
and add the following line:

    MONO_GC_PARAMS=bridge-implementation=old

This will cause the app to use the previous GC bridge.

<a name="Xamarin.Android_7.4.5-1"/>

# Xamarin.Android 7.4.5-1

Xamarin.Android 7.4.5-1 contains bug fixes.

<a name="bug-fixes-7.4.5-1" />

## Bug Fixes

* [57645](https://bugzilla.xamarin.com/show_bug.cgi?id=57645):
    The "LinkAssemblies" task failed unexpectedly due to a NullReferenceException in Mono.Linker's `ProcessLibrary()` method. **[7.4.5-1+]**

<a name="Xamarin.Android_7.4.3-1"/>

# Xamarin.Android 7.4.3-1

Xamarin.Android 7.4.3-1 contains bug fixes.

<a name="integrated-mono-7.4.3-1" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.2](http://www.mono-project.com/docs/about-mono/releases/5.2.0/) [commit 14f2c81](https://github.com/mono/mono/commit/14f2c814ccc4b98f11dae3074ba6a081956e9079).

* [44027](https://bugzilla.xamarin.com/show_bug.cgi?id=44027):
    Chunked HTTP PUT times out. **[7.4.3-1+]**
* [58829](https://bugzilla.xamarin.com/show_bug.cgi?id=58829):
    Many "[Mono] worker parking, [Mono] worker unparking" messages appearing in application output. **[7.4.3-1+]**


<a name="Xamarin.Android_7.4.0-21"/>

# Xamarin.Android 7.4.0-21

Xamarin.Android 7.4.0-21 contains bug fixes.

<a name="integrated-mono-7.4.0-21" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.2](http://www.mono-project.com/docs/about-mono/releases/5.2.0/)
[commit 2a6502c](https://github.com/mono/mono/commit/2a6502cee0df9de5198eafe7c8b5f6ac25106f34).

* [58625](https://bugzilla.xamarin.com/show_bug.cgi?id=58625):
    `IsComObject()` throws `PlatformNotSupportedException` and breaks uses of dynamic / SLE **[7.4.0-21]**


<!--
  JONP: 7.4.0 last updated from commit:
    monodroid/d15-3/0cd0214a3a6a133f861651dd85a539e5b901e3aa
    xamarin-android/d15-3/895db8c2
-->

<a name="0"/>
<a name="Xamarin.Android_7.4.0"/>

# Xamarin.Android 7.4

The Xamarin.Android 7.4 release primarily includes bug fixes.

<a name="new-features-7.4"/>

## New Features

* Beuller?


<a name="experimental-features"/>

## Experimental Features

Xamarin.Android 7.3 retains the experimental features from previous releases:

* [TLS 1.2 support in `WebRequest`](#btls)
* [Concurrent GC Support](#concurrent-gc)
* [Improved Fast Deployment](#Fast_Deployment)
* [File name and line number information in release builds](#Release_Stack_Traces)

<a name="btls" />

### TLS 1.2 support in `WebRequest`

[Xamarin.Android 7.1 added `AndroidClientHandler`][xa71-AndroidClientHandler],
which uses the native Java APIs to provide TLS 1.2 support. However, there are
two problems with `AndroidClientHandler`:

1. It can only be used with [`HttpClient`][httpclient], and
2. It requires Android 5.0 and later to operate. (Prior Android versions might
    not support TLS 1.2, and since `AndroidClientHandler` uses the native Java
    TLS stack...)

[xa71-AndroidClientHandler]: /releases/android/xamarin.android_6/xamarin.android_6.1/#Native_HttpClientHandler
[httpclient]: https://msdn.microsoft.com/en-us/library/system.net.http.httpclient(v=vs.118).aspx

To solve these problems, [Boring SSL][boring-ssl] can be used as the
lowest-level TLS implementation. Originally announced
[last September][btls-announce], Boring SSL can be embedded within
a Xamarin.Android application, allowing [`HttpWebRequest`][HttpWebRequest]
to communicate with TLS 1.2 endpoints. When enabled, the normal
`HttpClient` stack also uses Boring SSL.

[boring-ssl]: https://boringssl.googlesource.com/boringssl/
[btls-announce]: http://tirania.org/blog/archive/2016/Sep-30.html
[HttpWebRequest]: https://msdn.microsoft.com/en-us/library/system.net.httpwebrequest.aspx

To enable use of BoringSSL, add the `$(AndroidTlsProvider)` MSBuild property
to the application project, with a value of `btls`:

    <PropertyGroup>
      <AndroidTlsProvider>btls</AndroidTlsProvider>
    </PropertyGroup>

When enabled, a new `libmono-btls-shared.so` shared library will be present
within the `.apk`.

The default value of the `$(AndroidTlsProvider)` MSBuild property is the empty
string, i.e. not set, which will use the managed TLS implementation, which
*does not* support TLS 1.2.

The default value may change in a future release.

<a name="concurrent-gc">

### Concurrent GC Support

The new `$(AndroidEnableSGenConcurrent)` MSBuild property which controls
whether or not the concurrent GC is enabled.

`$(AndroidEnableSGenConcurrent)` is a boolean value. When `True`, then
Mono's GC is set to `marksweep-conc`; when `False`, then
Mono's GC is set to `marksweep`.

The default value is `False`.

See [Mono's **ConcurrentSGen** documentation][mono-marksweep-conc]
for more information.

[mono-marksweep-conc]: http://www.mono-project.com/docs/about-mono/releases/4.8.0/#concurrent-sgen

<a name="Fast_Deployment"/>

### Improved Fast Deployment

[Fast Deployment](https://developer.xamarin.com/guides/android/under_the_hood/build_process/#Fast_Deployment)
is a way to avoid rebuilding and redeploying Android Packages (`.apk` files)
when assemblies have changed in a way that doesn’t require changing the generated
[Android Callable Wrappers](https://developer.xamarin.com/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers/)
or altered any included Android Assets and Resources.

Xamarin.Android 7.0 will optionally allow Android Assets, Resources, and
compiled Java libraries to particpate in fast deployment as well, further
reducing the number of situations in which a possibly slow `.apk` rebuild
and redeploy will be required.

This new behavior is disabled by default.
It will be enabled by default in the Xamarin.Android 7.1 series.

To enable this new functionality, set the `$(AndroidFastDeploymentType)`
MSBuild property to `Assemblies:Dexes`:

    <AndroidFastDeploymentType>Assemblies:Dexes</AndroidFastDeploymentType>


#### Adding Resources to the Default Project

For example, assume a new (default) Application project which has already been
deployed to a target device.

1. Copy `Resources\layout\Main.axml` to `Resources\layout\Another.axml`,
    and add `Resources\layout\Another.axml` to the project.
2. Run the project.

(2) will require that the `.apk` be rebuilt and re-deployed to the target.
In previous versions, (2) could take 16 seconds.

With the new system


TODO:

Add some small benchmarks about what happens during dev when code changes,
or a resource changes, numbers before/after


<a name="Release_Stack_Traces" />

### File name and line number information in release builds

File name and line number information in Release builds is supported through
the build-time generation of `.pdb` files (and `.msym` files for AOT builds). The generation of
the sequence points is controlled by the new `$(MonoSymbolArchive)` MSBuild
property, which must be set to True to enable generation:

    <MonoSymbolArchive>True</MonoSymbolArchive>


You also need to set `$(DebugSymbols)` to True and `$(Optimize)` to True
for your release build. This will ensure that your assemblies *do not* contain
debug information but that the required data is stored in the `.pdb`/`.mSYM` files.

When enabled, a new `$(OutputPath)\@PACKAGE_NAME@.mSYM` directory will be
created which contains all information required to correlate IL offset
information (found in stack traces) back to file name and line number
information through the use of the `mono-symbolicate` tool.

Next, grab a crash log which an unhandled exception

	adb logcat -d > errors.txt

Finally, use `mono-symbolicate` to convert the errors to contain file and
line numbers:

	mono-symbolicate path-to-dll-in-.mSYM-directory path-to-errors.txt

`mono-symbolicate` can be found at:

* **macOS**: `/Library/Frameworks/Xamarin.Android.framework/Commands/mono-symbolicate`
* **Windows**: `%ProgramFiles(x86)%\MSBuild\Xamarin\Android\mono-symbolicate.exe`

For example, given an `errors.txt` with the contents:

	I/MonoDroid( 1545): System.Exception: wow it broke
	I/MonoDroid( 1545):   at CrashApp.MainActivity+<OnCreate>c__AnonStorey0.<>m__0 (System.Object , System.EventArgs ) [0x00030] in <filename unknown>:0
	I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerImplementor.OnClick (Android.Views.View v) [0x00014] in <filename unknown>:0
	I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerInvoker.n_OnClick_Landroid_view_View_ (IntPtr jnienv, IntPtr native__this, IntPtr native_v) [0x00011] in <filename unknown>:0
	I/MonoDroid( 1545):   at (wrapper dynamic-method) System.Object:5616285d-461b-4005-a31b-d4637a8cdddc (intptr,intptr,intptr)

`mono-symbolicate` will translate the above into:

	I/MonoDroid( 1545): System.Exception: wow it broke
	I/MonoDroid( 1545):   at CrashApp.MainActivity+<OnCreate>c__AnonStorey0.<>m__0 (System.Object , System.EventArgs ) [0x00030] in /Users/dean/Projects/CrashApp/CrashApp/MainActivity.cs:30
	I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerImplementor.OnClick (Android.Views.View v) [0x00014] in /Users/dean/Documents/Sandbox/Xamarin/dellismonodroid/src/Mono.Android/platforms/android-19/src/generated/Android.Webkit.WebBackForwardList.cs:68
	I/MonoDroid( 1545):   at Android.Views.View+IOnClickListenerInvoker.n_OnClick_Landroid_view_View_ (IntPtr jnienv, IntPtr native__this, IntPtr native_v) [0x00011] in /Users/dean/Documents/Sandbox/Xamarin/dellismonodroid/src/Mono.Android/platforms/android-19/src/generated/Android.Webkit.WebBackForwardList.cs:23
	I/MonoDroid( 1545):   at (wrapper dynamic-method) System.Object:5616285d-461b-4005-a31b-d4637a8cdddc (intptr,intptr,intptr)

Notice that the `<filename unknown>:0` messages were translated into
appropriate filename and line number information.

<a name="Breaking_Changes" />

## Breaking Changes

There are some deprecations and removals in Xamarin.Android 7.4.

* [API-10 is obsolete](#API-10).
* [`FSharp.Core.dll` has been removed](#FSharpCore).


<a name="API-10" />

### API-10 is Obsolete

Google Play Services [deprecated support for API-10][play-deprecation]
Android "Gingerbread" v2.3.x in February, 2017. The June 2017 release
of Google Play Services has removed support for Gingerbread.

[play-deprecation]: https://developers.google.com/android/guides/releases#february_2017_-_version_102

Xamarin.Android is following suit: Xamarin.Android 7.4 is the last
version that will include an API-10 binding assembly for `Mono.Android.dll`,
with a `$(TargetFrameworkVersion)` of v2.3. Developers should migrate their
projects to use a later `$(TargetFrameworkVersion)` value.


<a name="FSharpCore" />

### `FSharp.Core.dll` has been removed

Many years ago, when Mono for Android was new, the easiest way to support
F# was for the Xamarin team to compile `FSharp.Core.dll` from source, so
that it would be built against the correct `mscorlib.dll` and other
dependencies.

That is no longer the case.
The [FSharp.Core NuGet package](https://www.nuget.org/packages/FSharp.Core/)
has shipped Xamarin.Android compatible assemblies since at least 3.0.2,
released in *2014*. There is thus no need for Xamarin.Android to provide
an `FSharp.Core.dll` assembly: the Xamarin team is not actively following
the F# community, doesn't know when the F# team will have a new release,
and is not able to distribute a new F# release in a fast and reliable manner.

Use the NuGet package.

This is also the core of
[Bug #41262](https://bugzilla.xamarin.com/show_bug.cgi?id=41262): F#
projects should use the `FSharp.Core` NuGet package.

Additionally, in the Xamarin.Android 7.1 timeframe, the IDEs were updated
so that new projects defaulted to using the NuGet package.

I was perfectly happy with a world in which Xamarin.Android continued
distributing an *ancient* `FSharp.Core.dll` assembly (v3.x!). Existing
projects would continue to build, and if newer F# features were required,
the FSharp.Core NuGet package was available.

Unfortunately, due to not-entirely-understood build system changes,
the `FSharp.Core.dll` distributed with Xamarin.Android is now being used
*in preference to* the NuGet package, through no changes on the
Xamarin.Android side of things. This means that the NuGet package *cannot*
be used, which is a very unfortunate state of affairs.

The Xamarin.Android 7.4 release no longer distributes the `FSharp.Core.dll`
assembly. Please update your projects to use the NuGet package.


<a name="Bug_Fixes"/>

## Bug Fixes

* [12935](https://bugzilla.xamarin.com/show_bug.cgi?id=12935):
    sensorPortrait should be sensorPortait
* [32861](https://bugzilla.xamarin.com/show_bug.cgi?id=32861):
    [Smoke] ProGuard fails with &quot;error ... (Access is denied)&quot; if Android SDK path contains a space
* [33052](https://bugzilla.xamarin.com/show_bug.cgi?id=33052):
    The option for multi-dex fails when the path to the Android SDK contains a space
* [38693](https://bugzilla.xamarin.com/show_bug.cgi?id=38693):
    Call of mainDexClasses.bat does not produce records in multidex.keep
* [55305](https://bugzilla.xamarin.com/show_bug.cgi?id=55305):
    AndroidClientHandler ignores timeout value when trying to connect on misconfigured networks.
* [55477](https://bugzilla.xamarin.com/show_bug.cgi?id=55477):
    Stream Closed Exception thrown in AndroidClientHandler during redirected HTTP POST call.
* [56537](https://bugzilla.xamarin.com/show_bug.cgi?id=56537):
    InetAddress.HostAddress is empty for IPv4 addresses on Nougat
* [56653](https://bugzilla.xamarin.com/show_bug.cgi?id=56653):
    Zygote crashes
* [56808](https://bugzilla.xamarin.com/show_bug.cgi?id=56808):
    Cannot debug referenced iOS Class library in Visual Studio 2015/2017
* [56815](https://bugzilla.xamarin.com/show_bug.cgi?id=56815):
    HAVE_LARGE_FILE_SUPPORT broken on monodroid/master w/ mono/2017-04
* [56864](https://bugzilla.xamarin.com/show_bug.cgi?id=56864):
    [VS 2017 XA Self Hosted VSIX] Getting exception &quot;System.ArgumentNullException: Value cannot be null&quot; when deploying android App
* [56867](https://bugzilla.xamarin.com/show_bug.cgi?id=56867):
    [VS 2017 XA Self Hosted VSIX] Xamarin.Android version is not displayed in &quot;help &gt; About Microsoft Visual studio&quot;
* [56966](https://bugzilla.xamarin.com/show_bug.cgi?id=56966):
    Unable to Run Cheesesquare app in Release mode on HTC One X
* [56976](https://bugzilla.xamarin.com/show_bug.cgi?id=56976):
    F# is missing `__ANDROID__` define (regression)
* [57027](https://bugzilla.xamarin.com/show_bug.cgi?id=57027):
    Follow-up to Bug 33052: &quot;Invalid option&quot; causes java.exe failure during build with multidex if username contains spaces
* [57692](https://bugzilla.xamarin.com/show_bug.cgi?id=57692):
    Encountering build error when `android-26/android.jar` is installed and `$(AndroidUseLatestPlatformSdk)` is true

<!-- Access Denied bugs:
* [53355](https://bugzilla.xamarin.com/show_bug.cgi?id=53355):
* [53418](https://bugzilla.xamarin.com/show_bug.cgi?id=53418):
* [53884](https://bugzilla.xamarin.com/show_bug.cgi?id=53884):
* [54352](https://bugzilla.xamarin.com/show_bug.cgi?id=54352):
* [54353](https://bugzilla.xamarin.com/show_bug.cgi?id=54353):
* [54785](https://bugzilla.xamarin.com/show_bug.cgi?id=54785):
* [54982](https://bugzilla.xamarin.com/show_bug.cgi?id=54982):
* [55053](https://bugzilla.xamarin.com/show_bug.cgi?id=55053):
* [55407](https://bugzilla.xamarin.com/show_bug.cgi?id=55407):
* [55687](https://bugzilla.xamarin.com/show_bug.cgi?id=55687):
* [56168](https://bugzilla.xamarin.com/show_bug.cgi?id=56168):
* [56485](https://bugzilla.xamarin.com/show_bug.cgi?id=56485):
* [56874](https://bugzilla.xamarin.com/show_bug.cgi?id=56874):
* [56882](https://bugzilla.xamarin.com/show_bug.cgi?id=56882):
* [57532](https://bugzilla.xamarin.com/show_bug.cgi?id=57532):
* [57675](https://bugzilla.xamarin.com/show_bug.cgi?id=57675):
* [57808](https://bugzilla.xamarin.com/show_bug.cgi?id=57808):
* [57889](https://bugzilla.xamarin.com/show_bug.cgi?id=57889):
 -->


<a name="integrated-mono" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.2](http://www.mono-project.com/docs/about-mono/releases/5.2.0/)
[commit 30e73d4](https://github.com/mono/mono/commit/30e73d4d45b8b9e55e3846f5823e3be4a7123d0b).

* [580](https://bugzilla.xamarin.com/show_bug.cgi?id=580):
    Type.Load loads strong type despite version mismatch
* [39444](https://bugzilla.xamarin.com/show_bug.cgi?id=39444):
    Action ReflectedType differs from Delegate ReflectedType for virutal methods
* [40969](https://bugzilla.xamarin.com/show_bug.cgi?id=40969):
    HttpListener does not work with IPV6
* [43805](https://bugzilla.xamarin.com/show_bug.cgi?id=43805):
    Output of DateTime.Now() differs on Mono for ambiguous time period
* [43988](https://bugzilla.xamarin.com/show_bug.cgi?id=43988):
    Stack overflow in System.Text.Encoding.Default
* [46661](https://bugzilla.xamarin.com/show_bug.cgi?id=46661):
    Runtime exception filters truncate exception stack traces on NSLog
* [46929](https://bugzilla.xamarin.com/show_bug.cgi?id=46929):
    Datetime error on Mono.data.Sqlite
* [47221](https://bugzilla.xamarin.com/show_bug.cgi?id=47221):
    Thread.Name can only be set once inside async callback
* [47599](https://bugzilla.xamarin.com/show_bug.cgi?id=47599):
    HttpClient Transfer-Encoding:chunked is not added to the header - not able to transfer large files
* [49721](https://bugzilla.xamarin.com/show_bug.cgi?id=49721):
    Assembly binder uses wrong strongly named assembly when same assembly with different version exists in local folder
* [51522](https://bugzilla.xamarin.com/show_bug.cgi?id=51522):
    Overload resolution fails for referenced assembly
* [51561](https://bugzilla.xamarin.com/show_bug.cgi?id=51561):
    Getting process name of process running under higher privilege user throws exception
* [51653](https://bugzilla.xamarin.com/show_bug.cgi?id=51653):
    mono_thread_info_wait_one_handle ignored alertable argument
* [52086](https://bugzilla.xamarin.com/show_bug.cgi?id=52086):
    Nullable structs with implicit operators generate invalid IL code when compiling with Mono
* [52294](https://bugzilla.xamarin.com/show_bug.cgi?id=52294):
    C# compiler reports an incorrect error in a lambda with generic constraints
* [52340](https://bugzilla.xamarin.com/show_bug.cgi?id=52340):
    Compiler crashes with FATAL UNHANDLED EXCEPTION (nullref)
* [52345](https://bugzilla.xamarin.com/show_bug.cgi?id=52345):
    Process has exited, so the requested information is not available
* [52429](https://bugzilla.xamarin.com/show_bug.cgi?id=52429):
    Shutdown hang then crash in Finalizer thread
* [52437](https://bugzilla.xamarin.com/show_bug.cgi?id=52437):
    Random NullReferenceExceptions in StringBuilder.ThreadSafeCopy
* [52448](https://bugzilla.xamarin.com/show_bug.cgi?id=52448):
    StreamContent apparently needs to rewind stream before sending it
* [52475](https://bugzilla.xamarin.com/show_bug.cgi?id=52475):
    MTOUCH: error MT3001: Could not AOT the assembly
* [52508](https://bugzilla.xamarin.com/show_bug.cgi?id=52508):
    TLS SignalR Self-host Hang
* [52511](https://bugzilla.xamarin.com/show_bug.cgi?id=52511):
    configure script doen't detect bad configuration
* [52549](https://bugzilla.xamarin.com/show_bug.cgi?id=52549):
    error: mono_w32socket_convert_error: no translation into winsock error for (41) &quot;Protocol wrong type for socket&quot;
* [52590](https://bugzilla.xamarin.com/show_bug.cgi?id=52590):
    Cannot compile for iOS, TypeBuilder exists in two places.
* [52599](https://bugzilla.xamarin.com/show_bug.cgi?id=52599):
    await in finally clause prevents disposal of enclosing using statement
* [52600](https://bugzilla.xamarin.com/show_bug.cgi?id=52600):
    Full AOT: Strange combination of structs, generics, and enums causes runtime failure
* [52795](https://bugzilla.xamarin.com/show_bug.cgi?id=52795):
    Infinite loop on MySqlDataReader.ReadAsync() causing 100% CPU usage - regression
* [52845](https://bugzilla.xamarin.com/show_bug.cgi?id=52845):
    [Cycle 9] Satellite assemblies not bundled when using &quot;Bundle assemblies into native code&quot; due to &quot;unknown escape sequence&quot; error from gcc during mkbundle step
* [52866](https://bugzilla.xamarin.com/show_bug.cgi?id=52866):
    F# sprintf AOT bug still exists
* [52899](https://bugzilla.xamarin.com/show_bug.cgi?id=52899):
    mprof-report missing filenames in coverage xml output when using portable pdbs
* [53066](https://bugzilla.xamarin.com/show_bug.cgi?id=53066):
    Can't Build Project in Debug with &quot;Could not AOT the assembly&quot;
* [53131](https://bugzilla.xamarin.com/show_bug.cgi?id=53131):
    Calling MakeArray() on a type with a rank that is too big does not throw an exception.
* [53153](https://bugzilla.xamarin.com/show_bug.cgi?id=53153):
    Implement RuntimeHelpers::IsReferenceOrContainsReferences
* [53166](https://bugzilla.xamarin.com/show_bug.cgi?id=53166):
    Application crashes when setting a get-only property in constructor
* [53196](https://bugzilla.xamarin.com/show_bug.cgi?id=53196):
    List&lt;&gt;.Sort() using insertion sort does not sort all values when equality isn't checked.
* [53202](https://bugzilla.xamarin.com/show_bug.cgi?id=53202):
    Number minus Enum gives wrong value
* [53278](https://bugzilla.xamarin.com/show_bug.cgi?id=53278):
    Two coreclr SIMD test failures (one regression from 4.8)
* [53334](https://bugzilla.xamarin.com/show_bug.cgi?id=53334):
    es-US Culture wrong number formatting
* [53684](https://bugzilla.xamarin.com/show_bug.cgi?id=53684):
    Crash when enumerating directory and selecting the first file
* [53689](https://bugzilla.xamarin.com/show_bug.cgi?id=53689):
    [Test] Certificate7 disabled due to SecCertificateCreateWithData does different things on 10.11 vs 10.12 with invalid certificates
* [53792](https://bugzilla.xamarin.com/show_bug.cgi?id=53792):
    CFNetworkHandler reports correct download when internet connection is lost during request
* [53843](https://bugzilla.xamarin.com/show_bug.cgi?id=53843):
    Mono deadlocks on shutdown while waiting for a process which has died
* [53890](https://bugzilla.xamarin.com/show_bug.cgi?id=53890):
    Regression: Native crash while running tests with xunit with mono 2017-02 branch, works with 4.8.0.520
* [54212](https://bugzilla.xamarin.com/show_bug.cgi?id=54212):
    Mono allows casts of non-zero bound array to zero bound array
* [54322](https://bugzilla.xamarin.com/show_bug.cgi?id=54322):
    await in catch-block inside a loop causes the same exception to be caught multiple times
* [54448](https://bugzilla.xamarin.com/show_bug.cgi?id=54448):
    Unable to revert to thread-local storage for CurrentThread.CultureInfo
* [54485](https://bugzilla.xamarin.com/show_bug.cgi?id=54485):
    Creating an open generic type with recurrent constraint fails
* [54991](https://bugzilla.xamarin.com/show_bug.cgi?id=54991):
    Cannot compile get =&gt; _text
* [55041](https://bugzilla.xamarin.com/show_bug.cgi?id=55041):
    Stripping mscorlib in simple example changes IntPtr (5) behavior?
* [55083](https://bugzilla.xamarin.com/show_bug.cgi?id=55083):
    coreclr test b353858.il fails after 6f33b62f39a273fccb78f71513cb5e0dfb987c70
* [55148](https://bugzilla.xamarin.com/show_bug.cgi?id=55148):
    Debugger checks type which is possibly never used
* [55577](https://bugzilla.xamarin.com/show_bug.cgi?id=55577):
    SIMD instructions with System.Numerics.Vectors do not work
* [55603](https://bugzilla.xamarin.com/show_bug.cgi?id=55603):
    Follow-up to bug 52845: Satellite assemblies not loaded by app when using &quot;Bundle assemblies into native code&quot; even though they are now successfully mkbundled
* [55681](https://bugzilla.xamarin.com/show_bug.cgi?id=55681):
    System.Reflection.Emit.ModuleBuilder.build_metadata bug when running FAKE's test suite
* [56081](https://bugzilla.xamarin.com/show_bug.cgi?id=56081):
    Returning a valuetype from an async method with an awaited parameter yields a Mono.CSharp.InternalErrorException: Await yields with non-empty stack
* [56247](https://bugzilla.xamarin.com/show_bug.cgi?id=56247):
    Enumerable.OrderByDescending behaves differently on LLVM FullAOT
* [56493](https://bugzilla.xamarin.com/show_bug.cgi?id=56493):
    Windows MMAP doesn't release file
* [56499](https://bugzilla.xamarin.com/show_bug.cgi?id=56499):
    DateTime.Now throws exception if /etc/localtime symlink destination missing
* [56567](https://bugzilla.xamarin.com/show_bug.cgi?id=56567):
    Passing large struct into exception filter method crashes runtime with SIGSEGV
* [56611](https://bugzilla.xamarin.com/show_bug.cgi?id=56611):
    Regression: ArrayTypeMismatchException when running F# script
* [56694](https://bugzilla.xamarin.com/show_bug.cgi?id=56694):
    Assertion: should not be reached at d:\j\workspace\v\repos\mono\mono\sgen\sgen-scan-object.h:91
* [56821](https://bugzilla.xamarin.com/show_bug.cgi?id=56821):
    Static ctor of MarshalByRefObject runs in primary AppDomain
* [56824](https://bugzilla.xamarin.com/show_bug.cgi?id=56824):
    Runtime crash with VSMEF
* [57222](https://bugzilla.xamarin.com/show_bug.cgi?id=57222):
    System.Reflection.AmbiguousMatchException for two fields with same name but different types

<!-- Access Denied bugs:
* [44907](https://bugzilla.xamarin.com/show_bug.cgi?id=44907):
* [46482](https://bugzilla.xamarin.com/show_bug.cgi?id=46482):
* [51791](https://bugzilla.xamarin.com/show_bug.cgi?id=51791):
* [52548](https://bugzilla.xamarin.com/show_bug.cgi?id=52548):
* [52578](https://bugzilla.xamarin.com/show_bug.cgi?id=52578):
* [52846](https://bugzilla.xamarin.com/show_bug.cgi?id=52846):
* [53015](https://bugzilla.xamarin.com/show_bug.cgi?id=53015):
* [53958](https://bugzilla.xamarin.com/show_bug.cgi?id=53958):
* [54976](https://bugzilla.xamarin.com/show_bug.cgi?id=54976):
* [55095](https://bugzilla.xamarin.com/show_bug.cgi?id=55095):
* [56202](https://bugzilla.xamarin.com/show_bug.cgi?id=56202):
* [56452](https://bugzilla.xamarin.com/show_bug.cgi?id=56452):
 -->


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
* API Level 22:
    [Mono.Android.dll](level_22_diff/mono.android.dll)
* API Level 23:
    [Mono.Android.dll](level_23_diff/mono.android.dll)
* API Level 24:
    [Mono.Android.dll](level_24_diff/mono.android.dll)
* API Level 25:
    [Mono.Android.dll](level_25_diff/mono.android.dll)

