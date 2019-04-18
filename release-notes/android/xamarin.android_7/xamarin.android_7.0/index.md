---
id: F8F75B53-E72A-479D-AA11-31176348FE47
title: "Xamarin.Android 7.0"
---

Xamarin.Android 7.0: Let's try this open-source thing, right?

Xamarin.Android 7.0 is the first release to use the open-source
repositories

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android?at=57c487782dcc4f312942a519).

Android v7.0 Nougat adds support for the
[Vulkan API](https://developer.android.com/ndk/guides/graphics/index.html).
Vulkan support will *not* be distributed as part of the core Xamarin.Android
binding. Instead, please use the
[VulkanSharp](https://www.nuget.org/packages/VulkanSharp/) NuGet package, and the
[XLogo sample app](https://github.com/mono/VulkanSharp/tree/master/samples/XLogo).

**Note:** Xamarin.Android 7.0 requires
[JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
to use the Android Nougat (API 24) APIs. You can continue to use earlier
versions of the JDK if targeting earlier Android API levels:

* [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) - up to API 24+

* [JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) - up to API 23

* [JDK 1.6](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase6-419409.html) - up to API 20

Additionally, a 64-bit version of the JDK is required to use [custom controls
in the Android
designer](https://developer.xamarin.com/releases/vs/xamarin.vs_4/xamarin.vs_4.2/#androiddesignercustomcontrols).

**The simplest option is to install the 64-bit version of JDK 1.8 since it is
backwards compatible with all of the previous API levels and supports the new
Android designer features.**

(One unfortunate complication with JDK 1.8 is that is **not** compatible with
the outdated version of Proguard that is included in the Android SDK. Currently
this will cause an error "Unsupported class version number \[52.0\]" when
attempting to use the Proguard or Multidex features in Xamarin.Android. See
[44187](https://bugzilla.xamarin.com/show_bug.cgi?id=44187).)

***Note:***
Due to a change by Google, [Android N will now only permit linking to NDK-provided native libraries][ndk].
`libsqlite.so` is *not* an NDK-provided native library. Consequently,
existing apps using e.g. `Mono.Data.Sqlite.dll` *will* ***crash*** when
running on Android N. This may include other SQLite-using assemblies,
not distributed with Xamarin.Android.

[ndk]: https://developer.android.com/about/versions/nougat/android-7.0-changes.html#ndk

Xamarin.Android 7.0, which is part of [Cycle 8][cycle8],
[updates `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to include
a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

**All Developers** need to audit their code for P/Invoke and ensure that referenced
native libraries are either included in the Android NDK, or are included within
the `app.apk` itself. The only Xamarin.Android-provided assembly impacted by
this change is `Mono.Data.Sqlite.dll`.

[cycle8]: https://releases.xamarin.com/stable-release-cycle-8-service-release-1/

# Known Issues

Xamarin.Android [changed the default GC Bridge](#gc-bridge-tarjan) from
`old` to `tarjan`.

Unfortunately, a [few bugs](https://bugzilla.xamarin.com/show_bug.cgi?id=47577)
have been reported which suggest a bug within the Tarjan GC bridge.

If this happens, [create an `@(AndroidEnvironment)` file](/guides/android/advanced_topics/environment/)
and add the following line:

    MONO_GC_PARAMS=bridge-implementation=old

This will cause the app to use the previous GC bridge.

<!--
  JONP: 7.0.2 last updated from commit monodroid/cycle8/ce955cc0476f5d4821066f7a04ff5660caccaa4b
-->

<a name="2"/>
<a name="Xamarin.Android_7.0.2"/>
# Xamarin.Android 7.0.2

Xamarin.Android 7.0.2 contains bug fixes.

<a name="Bug_Fixes-7.0.2"/>
## Bug Fixes

* [41665](https://bugzilla.xamarin.com/show_bug.cgi?id=41665),
    [44535](https://bugzilla.xamarin.com/show_bug.cgi?id=44535):
    `System.ComponentModel.INotifyPropertyChanged`'` is defined in an assembly
    that is not referenced. You must add a reference to assembly
    `System.ObjectModel` for Android projects that reference
    PCLs that use `INotifyPropertyChanged`.
* [43500](https://bugzilla.xamarin.com/show_bug.cgi?id=43500):
    Add support for `$(AndroidAotAdditionalArguments)` MSBuild property.
* [44184](https://bugzilla.xamarin.com/show_bug.cgi?id=44184):
    Debug deploy always fails: `ZipException`: Entry has been changed
* [44193](https://bugzilla.xamarin.com/show_bug.cgi?id=44193):
    MSB3247 warning when building Xamarin.Forms app.
* [44268](https://bugzilla.xamarin.com/show_bug.cgi?id=44268):
    &quot;Unexpected libzip error: Inval&quot; when building project that
    references Android Support Libraries on Windows if user name contains
    any accented characters
* [44633](https://bugzilla.xamarin.com/show_bug.cgi?id=44633):
    Enabling `<AndroidUseSharedRuntime/>` in some projects causes `classes.dex`
    to not deploy to device when using Xamarin Studio.
* [44685](https://bugzilla.xamarin.com/show_bug.cgi?id=44685):
    VS2015 freeze for a few minutes when trying to start a debug session
* [45018](https://bugzilla.xamarin.com/show_bug.cgi?id=45018):
    Possible memory leak of whole Task chain for SDK resolving
* [45113](https://bugzilla.xamarin.com/show_bug.cgi?id=45113):
    Can't run a C# android app using an FSharp 4.0 Library
* [45543](https://bugzilla.xamarin.com/show_bug.cgi?id=45543):
    Android application fails to launch and crashes on device/simulator.


<a name="integrated-mono-7.0.2" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.6.2](http://www.mono-project.com/docs/about-mono/releases/4.6.0/)
[commit 2f4c98b3](https://github.com/mono/mono/commit/db6986665292f1cd91763c32667929842d25b1db).

* [39832](https://bugzilla.xamarin.com/show_bug.cgi?id=39832):
    SIGSEGV when running roslyn
* [44132](https://bugzilla.xamarin.com/show_bug.cgi?id=44132):
    `Thread.Sleep()` overhead too big
* [44708](https://bugzilla.xamarin.com/show_bug.cgi?id=44708):
    `TrustFailure (The authentication or decryption has failed.)` ...
    `Invalid certificate received from server.` with `Error code: 0x5` or
    `Error code: 0xffffffff800b010f` when attempting to access HTTPS servers on
    ports other than 443.
* [45379](https://bugzilla.xamarin.com/show_bug.cgi?id=45379):
    Assert in `sgen-scan-object.h`.

<!--
  JONP: 7.0.1 last updated from commit monodroid/cycle8-sr0/96c7ba6c844dac58d02210688d879b794602c3db
-->

<a name="1"/>
<a name="Xamarin.Android_7.0.1"/>
# Xamarin.Android 7.0.1

Xamarin.Android 7.0.1 contains bug fixes.

<a name="Bug_Fixes-7.0.1"/>
## Bug Fixes


* [43411](https://bugzilla.xamarin.com/show_bug.cgi?id=43411):
    HTTP Bad Request (400) when encoding space (%20) in URL with `AndroidClientHandler`
* [44184](https://bugzilla.xamarin.com/show_bug.cgi?id=44184):
    Debug deploy always fails: `ZipException: Entry has been changed`
* [44268](https://bugzilla.xamarin.com/show_bug.cgi?id=44268):
    [Cycle 8] &quot;Unexpected libzip error: Inval&quot; when building project that references Android Support Libraries on Windows if user name contains any accented characters
* [44448](https://bugzilla.xamarin.com/show_bug.cgi?id=44448):
    SIGSEGV during process startup.


<a name="integrated-mono-7.0.1" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.6](http://www.mono-project.com/docs/about-mono/releases/4.6.0/)
[commit 8c9e3406](https://github.com/mono/mono/commit/8c9e34069f63e516038cd12a237d648079789622).

* Send all data to the socket before exiting from `Socket.Send()`.
* [39859](https://bugzilla.xamarin.com/show_bug.cgi?id=39859):
    Xamarin.Android apps on the Samsung Galaxy S7 fails to start with the error `System.ExecutionEngineException` SIGILL
* [44708](https://bugzilla.xamarin.com/show_bug.cgi?id=44708):
    `Invalid certificate received from server` when accessing HTTPS servers
    on ports other than 443.


<!--
  JONP: 7.0.0 last updated from commit monodroid/cycle8/0e59c3628c30b17fd3874743b26b900f3c3894a4
-->

<a name="0"/>
<a name="Xamarin.Android_7.0.0"/>
# Xamarin.Android 7.0

<a name="new-features-7.0" />
## New Features

* Bindings for
    [Android 7.0 Nougat](https://developer.android.com/about/versions/nougat/android-7.0.html)
    via the new `$(TargetFrameworkVersion)` of `v7.0`.
* [`Mono.Data.Sqlite.dll` bundles SQLite](#mono-data-sqlite)
* [Default GC bridge changed to **Tarjan**](#gc-bridge-tarjan)


<a name="mono-data-sqlite" />
### `Mono.Data.Sqlite.dll` and `libsqlite.so`

In previous releases, `Mono.Data.Sqlite.dll` would P/Invoke into the
OS-provided `/system/lib/libsqlite.so` native library.
[Starting with Android N][ndk], Android will no longer permit this behavior,
so previous versions of `Mono.Data.Sqlite.dll` will throw a
`DllNotFoundException` when attempting to use SQLite functionality
when executing on Android N.

`Mono.Data.Sqlite.dll` will now bundle and distribute a custom SQLite,
named `libsqlite3_xamarin.so`, which will automatically be bundled into
the `app.apk` when `Mono.Data.Sqlite.dll` is referenced.

*Existing users of `Mono.Data.Sqlite.dll` need only rebuild their app.*

*However*, if *any other assembly* is P/Invoking `sqlite`, `sqlite3`,
or variations thereof, these SQLite uses will *not* be updated.
Those other assemblies will need to be updated.
For example,
[SQLitePCL.raw 0.6.0](https://www.nuget.org/packages/SQLitePCL.raw_basic/0.6.0)
*will not* work on Android N, while the updated 
[SQLitePCL.raw 0.8.6](https://www.nuget.org/packages/SQLitePCL.raw_basic/)
has been updated to distribute its own copy of SQLite, and *will* work
on Android N.


<a name="gc-bridge-tarjan" />
### Default GC bridge changed to **Tarjan**

The default [GC Bridge][gc-bridge] has been changed to **tarjan**,
from **old**.

[gc-bridge]: https://developer.xamarin.com/guides/android/advanced_topics/garbage_collection/#GC_Bridge_Options

This change may introduce GC bugs.

<a name="experimental-features" />
## Experimental Features

Xamarin.Android 7.0 introduces several experimental features:

* [Improved Fast Deployment](#Fast_Deployment)

<a name="Fast_Deployment" />
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

```
<AndroidFastDeploymentType>Assemblies:Dexes</AndroidFastDeploymentType>
```

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

<a name="Known_Issues"/>
## Known Issues

* [43838](https://bugzilla.xamarin.com/show_bug.cgi?id=43838):
    "error CS1929: Type \`System.Array' does not contain a member \`OfType' and
    the best extension method overload ... requires an instance of type
    \`System.Collections.IEnumerable'" when certain portable class libraries
    are referenced (such as the MathNet.Numerics NuGet package).

* [44184](https://bugzilla.xamarin.com/show_bug.cgi?id=44184):
    "The "BuildApk" task failed unexpectedly. Xamarin.Tools.Zip.ZipException:
    Entry has been changed" when attempting to archive or deploy apps that use
    certain NuGet packages.

    * **Workaround**: Copy [this patched version of
      _libZipSharp.dll_](https://bugzilla.xamarin.com/attachment.cgi?id=17586)
      from the Xamarin.Android team into _C:\\Program Files
      (x86)\\MSBuild\\Xamarin\\Android\\_ on Windows or
      _/Library/Frameworks/Xamarin.Android.framework/Versions/Current/lib/xbuild/Xamarin/Android/_
      on Mac, overwriting the existing file. (From [Comment 33 on the bug
      report](https://bugzilla.xamarin.com/show_bug.cgi?id=44184#c33).)

* [44268](https://bugzilla.xamarin.com/show_bug.cgi?id=44268):
    "Unexpected libzip error: Inval" when building projects that reference any
    of the Android Support Libraries on Windows if the user name contains any
    accented characters.

    * **Temporary workaround**: Create and log in with a Windows user account
      that has only ASCII letters in the user name.

    * **Alternate workaround**: Add a _XAMARIN\_CACHEPATH_ environment
      variable under _Control Panel > System > Advanced system settings >
      Environment Variables_, and set it to a path that uses only ASCII
      letters in the directory names.

<a name="Bug_Fixes"/>
## Bug Fixes

* [14918](https://bugzilla.xamarin.com/show_bug.cgi?id=14918):
    mandroid daemon not supporting reading accented characters.
    (The mandroid daemon is dead! Dead!!!!!)
* [31763](https://bugzilla.xamarin.com/show_bug.cgi?id=31763):
    Adding an Android Library Project to an Android Binding project causes referencing app project's build to fail.
* [35739](https://bugzilla.xamarin.com/show_bug.cgi?id=35739),
    [35798](https://bugzilla.xamarin.com/show_bug.cgi?id=35798)
    Debugger exits with `art/runtime/fault_handler.cc:117] Check failed: !initialized_`
* [39980](https://bugzilla.xamarin.com/show_bug.cgi?id=39980):
    `ActivityFlags.LaunchAdjacent` is missing
* [40239](https://bugzilla.xamarin.com/show_bug.cgi?id=40239):
    SIGSEGV with the Bug 27408 repro.
* [40749](https://bugzilla.xamarin.com/show_bug.cgi?id=40749):
    [Regression] Translation with resx files is broken (version 6.1.0.48)
* [40976](https://bugzilla.xamarin.com/show_bug.cgi?id=40976):
    Custom Application subclass does not extend MultiDexApplication when MultiDex is enabled
* [40982](https://bugzilla.xamarin.com/show_bug.cgi?id=40982):
    [XVS 4.0] VS hangs/freezes when opening solutions containing Android Bindings Libraries that reference other libraries, during `GetAdditionalResourcesFromAssemblies.Execute()`
* [42082](https://bugzilla.xamarin.com/show_bug.cgi?id=42082):
    "Ionic.Zip.ZipException ... \_\_AndroidLibraryProjects\_\_.zip is not a
    valid zip file ---> System.TimeZoneNotFoundException" when building Android
    projects in certain Windows time zones.
* [42168](https://bugzilla.xamarin.com/show_bug.cgi?id=42168):
    A numeric comparison was attempted on `$(_DeviceSdkVersion)` that evaluates
    to `&quot;&quot;` instead of a number, in condition
    `&quot;$(_DeviceSdkVersion) &gt;= 21&quot;`.
* [42566](https://bugzilla.xamarin.com/show_bug.cgi?id=42566):
    Xamarin can't find NDK 12b because `ndk-stack.exe` is now `ndk-stack.cmd`
* [42643](https://bugzilla.xamarin.com/show_bug.cgi?id=42643):
    [AndroidPublishing] VS crashes randomly while Archiving the application.
* [43151](https://bugzilla.xamarin.com/show_bug.cgi?id=43151):
    [AndroidClientHandler] Doesn't support redirect to-from https/http


<a name="breaking-changes" />
## Breaking Changes

The venerable mandroid daemon no longer exists. Consequently, it can't
be used to obtain the product version:

    # This no longer works
    $ /Developer/MonoAndroid/usr/bin/mandroid --version

The Xamarin.Android version information can be obtained from Visual Studio
and Xamarin Studio, or on macOS the following files may be used to determine
version information:

* `Version`: The Xamarin.Android version number, as a major.minor.build.
* `Version.rev`: The revision number; the number of commits since `Version`
    was changed.
* `Version.commit`: The branch and commit hash that generated the build.

<a name="integrated-mono" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.6](http://www.mono-project.com/docs/about-mono/releases/4.6.0/)
[commit 51a3c93f](https://github.com/mono/mono/commit/51a3c93f67949bb1c277b9cb33a48c220bf1307f).

* [4242](https://bugzilla.xamarin.com/show_bug.cgi?id=4242):
    JavaScriptSerializer should use invariant culture
* [5644](https://bugzilla.xamarin.com/show_bug.cgi?id=5644):
    Mono allows to access not accessible method
* [6057](https://bugzilla.xamarin.com/show_bug.cgi?id=6057):
    UdpClient IPv6 Receive throws ArgumentException
* [8554](https://bugzilla.xamarin.com/show_bug.cgi?id=8554):
    System.Net.NetworkInformation.Ping - SendPingAsync operation fails
* [10108](https://bugzilla.xamarin.com/show_bug.cgi?id=10108):
    `mono_jit_cleanup` asserts/aborts on shutdown if soft debugging
* [11699](https://bugzilla.xamarin.com/show_bug.cgi?id=11699):
    FileStream writing incorrectly (some internal position is wrong)
* [12205](https://bugzilla.xamarin.com/show_bug.cgi?id=12205):
    MethodInfo.ReflectedType returns declaring type for generic base classes
* [13538](https://bugzilla.xamarin.com/show_bug.cgi?id=13538):
    Extraneous lines in Application Output for Debug.WriteLine
* [13957](https://bugzilla.xamarin.com/show_bug.cgi?id=13957):
    Xamarin.Android Apps are crashing on dual core x86 Devices
* [18361](https://bugzilla.xamarin.com/show_bug.cgi?id=18361):
    FileInfo.MoveTo does not work with absolute paths
* [20186](https://bugzilla.xamarin.com/show_bug.cgi?id=20186):
    Another AOT bug
* [23206](https://bugzilla.xamarin.com/show_bug.cgi?id=23206):
    MS allows threadpool threads to be renamed multiple times
* [24641](https://bugzilla.xamarin.com/show_bug.cgi?id=24641):
    CompareInfo.Compare() does not recognize ignorable characters when CompareOptions.Ordinal is specified
* [24974](https://bugzilla.xamarin.com/show_bug.cgi?id=24974):
    Exception occurs in __ComObject finalizer when shutting down process
* [27303](https://bugzilla.xamarin.com/show_bug.cgi?id=27303):
    NullReferenceException with ARMv7
* [29585](https://bugzilla.xamarin.com/show_bug.cgi?id=29585):
    Type.GetMethods returns generic method that cannot be specialized
* [29916](https://bugzilla.xamarin.com/show_bug.cgi?id=29916):
    System.Reflection.ParameterInfo.GetCustomAttributes always throws NullReference exception.
* [30686](https://bugzilla.xamarin.com/show_bug.cgi?id=30686):
    ZipArchive ctor throws InvalidDataException for WebConnectionStream
* [32374](https://bugzilla.xamarin.com/show_bug.cgi?id=32374):
    `WebRequest::BeginGetRequestStream()` incorrectly sets `IAsyncResult::CompletedSynchronously` to always `true`
* [33183](https://bugzilla.xamarin.com/show_bug.cgi?id=33183):
    Unexpected behavior can occur when horizontal or vertical scrollbar value changes in TreeView
* [33551](https://bugzilla.xamarin.com/show_bug.cgi?id=33551):
    &ndash; System.Net.SmtpClient uses an invalid HELO name
* [33553](https://bugzilla.xamarin.com/show_bug.cgi?id=33553):
    System.IO.Compression.ZipArchive produces bad archive files
* [33809](https://bugzilla.xamarin.com/show_bug.cgi?id=33809):
    Exception with SignalR 2.2 and Mono 4.2.0
* [35004](https://bugzilla.xamarin.com/show_bug.cgi?id=35004):
    Filename returned by LocalEndpoint of UnixListener has null characters appended to the end which causes the socket file to not be deleted when the UnixListener is disposed
* [35872](https://bugzilla.xamarin.com/show_bug.cgi?id=35872):
    Cultureinfo -&gt; numinfo internal field is NonSerialized on Mono, but not on Windows
* [35876](https://bugzilla.xamarin.com/show_bug.cgi?id=35876):
    Incorrect return of DateTime.ToUniversalTime method for DateTime.MaxValue.
* [36080](https://bugzilla.xamarin.com/show_bug.cgi?id=36080):
    [Mono 4.2] &quot;'System.ServiceModel.EndpointAddress10' does not have a static method 'GetSchema' that takes a parameter of type 'System.Xml.Schema.XmlSchemaSet'&quot; when using the Xamarin Mobile profile with some WCF client apps
* [36192](https://bugzilla.xamarin.com/show_bug.cgi?id=36192):
    Error binding Socket to Loopback
* [36388](https://bugzilla.xamarin.com/show_bug.cgi?id=36388):
    Application settings produce extra XML headers during saving
* [36560](https://bugzilla.xamarin.com/show_bug.cgi?id=36560):
    Unhandled exceptions outside the main execution context are ignored
* [36786](https://bugzilla.xamarin.com/show_bug.cgi?id=36786):
    Dictionary constructed with StringComparer.OrdinalIgnoreCase malfunctions if culture is changed after adding values
* [36829](https://bugzilla.xamarin.com/show_bug.cgi?id=36829):
    XmlSerializer does not support subclasses when serializing sequences of items
* [37583](https://bugzilla.xamarin.com/show_bug.cgi?id=37583):
    MAJOR performance decrease between 4.0.5.1 and 4.2.1
* [37681](https://bugzilla.xamarin.com/show_bug.cgi?id=37681):
    Fails to parse negative integers with Hebrew region set
* [37695](https://bugzilla.xamarin.com/show_bug.cgi?id=37695):
    Delegate references an overridden method in derived class misbehaves when marshalled as a parameter to native C function.
* [37848](https://bugzilla.xamarin.com/show_bug.cgi?id=37848):
    CultureInfo.GetCultureInfo(0) should throw ArgumentOutOfRangeException instead of CultureNotFoundException
* [37891](https://bugzilla.xamarin.com/show_bug.cgi?id=37891):
    System.Net.Configuration/SmtpSection.cs missing 'deliveryFormat'
* [38012](https://bugzilla.xamarin.com/show_bug.cgi?id=38012):
    Using Task's under memory pressure leads to unexpected crashes inside the TPL on iOS
* [38025](https://bugzilla.xamarin.com/show_bug.cgi?id=38025):
    &quot;Step Out&quot; gets confused by nested code
* [38161](https://bugzilla.xamarin.com/show_bug.cgi?id=38161):
    instability/crash when using DateTime under cpu load
* [38223](https://bugzilla.xamarin.com/show_bug.cgi?id=38223):
    missing package in arm64 build
* [38250](https://bugzilla.xamarin.com/show_bug.cgi?id=38250):
    Stack Corruption in mono involving tailcalls (where code is fine on Windows)
* [38322](https://bugzilla.xamarin.com/show_bug.cgi?id=38322):
    HttpListenerRequest.IsLocal isn't good enough
* [38408](https://bugzilla.xamarin.com/show_bug.cgi?id=38408):
    Error disposing of Filestream when leaving using statement
* [38553](https://bugzilla.xamarin.com/show_bug.cgi?id=38553):
    FileVersionInfo.ProductVersion is not populated from AssemblyVersion
* [38599](https://bugzilla.xamarin.com/show_bug.cgi?id=38599):
    Regression: SynchronizationContext.Current returns wrong value in delegate run by SynchronizationContext.Send.
* [38600](https://bugzilla.xamarin.com/show_bug.cgi?id=38600):
    mkbundle Doesn't support assemblies with spaces in their names.
* [38712](https://bugzilla.xamarin.com/show_bug.cgi?id=38712):
    Mono 4.3 Cryptography.ProtectedData fails to decrypt data from Mono 4.2
* [38796](https://bugzilla.xamarin.com/show_bug.cgi?id=38796):
    FileInfo.ToString misbehaving after MoveTo
* [38818](https://bugzilla.xamarin.com/show_bug.cgi?id=38818):
    linked apps with Java.Interop.dll crash on device
* [38825](https://bugzilla.xamarin.com/show_bug.cgi?id=38825):
    `mono_image_open()` does not check header anymore
* [38933](https://bugzilla.xamarin.com/show_bug.cgi?id=38933):
    CryptographicException from ProtectedData in multi-threaded execution
* [39077](https://bugzilla.xamarin.com/show_bug.cgi?id=39077):
    AppDomain.CurrentDomain.UnhandledException prevents exceptions in ThreadPool from crashing the application
* [39279](https://bugzilla.xamarin.com/show_bug.cgi?id=39279):
    Thread pool sizes are incorrect on linux when processor affinity is set, which complicates running mono applications in docker containers
* [39282](https://bugzilla.xamarin.com/show_bug.cgi?id=39282):
    [System.IO.Compression] issues with ZipArchiveEntry streams
* [39307](https://bugzilla.xamarin.com/show_bug.cgi?id=39307):
    HTTPS connections broken in recent Linux snapshot builds
* [39347](https://bugzilla.xamarin.com/show_bug.cgi?id=39347):
    Assertion when passing delegate of icall method to p/invoke
* [39568](https://bugzilla.xamarin.com/show_bug.cgi?id=39568):
    Unmanaged crash: `icall.c:5484: Could not resolve type with token 01000008 assembly:System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089 type:System.IdentityModel.Tokens.IssuerTokenResolver member:&lt;none&gt;`
* [39569](https://bugzilla.xamarin.com/show_bug.cgi?id=39569):
    Validation of ETag by HttpHeaders.Add is too strict
* [39631](https://bugzilla.xamarin.com/show_bug.cgi?id=39631):
    PPDB support fails to load any pdb when verifier is involved
* [39644](https://bugzilla.xamarin.com/show_bug.cgi?id=39644):
    `* Assertion at image.c:512, condition 'image-&gt;heap_guid.size &gt;= 16' not met`
* [39669](https://bugzilla.xamarin.com/show_bug.cgi?id=39669):
    System.Configuration.DictionarySectionHandler is missing
* [39715](https://bugzilla.xamarin.com/show_bug.cgi?id=39715):
    ppdb support causes crash at shutdown
* [39746](https://bugzilla.xamarin.com/show_bug.cgi?id=39746):
    `Assertion at method-to-ir.c:11652` when using mono master/ca7b692f4 and nuget
* [39824](https://bugzilla.xamarin.com/show_bug.cgi?id=39824):
    SerializationException thrown when serializing an Exception that uses SerializeObjectState
* [39911](https://bugzilla.xamarin.com/show_bug.cgi?id=39911):
    System.Reflection.Emit.DerivedType isn't an IReflectableType so GetTypeInfo throws
* [40040](https://bugzilla.xamarin.com/show_bug.cgi?id=40040):
    `* Assertion: should not be reached at mini.c:4403`
* [40060](https://bugzilla.xamarin.com/show_bug.cgi?id=40060):
    System.TypeSpec.Parse cannot parse generics + anonymous type name
* [40175](https://bugzilla.xamarin.com/show_bug.cgi?id=40175):
    Runtime crashes on '-v --version'
* [40187](https://bugzilla.xamarin.com/show_bug.cgi?id=40187):
    System.IO.Directory.CreateDirectory on Linux does not handle /.. in the path
* [40239](https://bugzilla.xamarin.com/show_bug.cgi?id=40239):
    SIGSEGV 27408 repro
* [40368](https://bugzilla.xamarin.com/show_bug.cgi?id=40368):
    Setting FileInfo.LastWriteTime has different results with mono32 and mono64
* [40536](https://bugzilla.xamarin.com/show_bug.cgi?id=40536):
    Compiler crash when attaching an event of a templated delegate with wrong template type
* [40568](https://bugzilla.xamarin.com/show_bug.cgi?id=40568):
    Runtime crashing on System.Enum.GetValues on char enums with F#
* [40603](https://bugzilla.xamarin.com/show_bug.cgi?id=40603):
    Mono can't parse Date in DB wich is in format: &quot;2016-02-04 10:39:11Z&quot;
* [40643](https://bugzilla.xamarin.com/show_bug.cgi?id=40643):
    Process leaking handles leads to &quot;too many open files&quot;
* [40646](https://bugzilla.xamarin.com/show_bug.cgi?id=40646):
    Oid and FriendlyName for sha384
* [40697](https://bugzilla.xamarin.com/show_bug.cgi?id=40697):
    Some NumberFormat have wrong GroupSeparator
* [40758](https://bugzilla.xamarin.com/show_bug.cgi?id=40758):
    [Regression] Remoting instance is not proxied
* [40916](https://bugzilla.xamarin.com/show_bug.cgi?id=40916):
    [System.IO.Compression] ZipArchive can create an ZipArchiveEntry that has a modified time of DateTime.MinValue
* [40953](https://bugzilla.xamarin.com/show_bug.cgi?id=40953):
    Bad performance using TypeBuilder
* [41035](https://bugzilla.xamarin.com/show_bug.cgi?id=41035):
    DataViewTest2.DataView_ListChangedEventTest occasionally fails with llvm+sgen
* [41224](https://bugzilla.xamarin.com/show_bug.cgi?id=41224):
    HttpClientHandler.UseProxy = false setting is ignored.
* [41280](https://bugzilla.xamarin.com/show_bug.cgi?id=41280):
    System.MethodAccessException is thrown from wrong frame
* [41431](https://bugzilla.xamarin.com/show_bug.cgi?id=41431):
    [aot] Build fails due to 'Sgen STW requires a working mono-context' error
* [41492](https://bugzilla.xamarin.com/show_bug.cgi?id=41492):
    DateTimeOffset.ToLocalTime() throwing erroneous error
* [41509](https://bugzilla.xamarin.com/show_bug.cgi?id=41509):
    41509 &ndash; DLR crashes when trying to convert a object to null.
* [41552](https://bugzilla.xamarin.com/show_bug.cgi?id=41552):
    HttpResponseMessage does not support multiple Links header entries
* [41616](https://bugzilla.xamarin.com/show_bug.cgi?id=41616):
    Mono 4.4.0 crashes when using Socket.ConnectAsync to a unix domain socket if the path doesn't exist
* [41623](https://bugzilla.xamarin.com/show_bug.cgi?id=41623):
    &quot;Step Over&quot; on an Android App deployed to a physical/virtual device crashes the app
* [41667](https://bugzilla.xamarin.com/show_bug.cgi?id=41667):
    new DateTime().ToLocalTime() results in an exception
* [41775](https://bugzilla.xamarin.com/show_bug.cgi?id=41775):
    Zip version needed to extract not correct in System.IO.Compression
* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782):
    [Cycle 7] &quot;System.Net.WebException: Error: NameResolutionFailure&quot; when attempting web requests with certain raw IP addresses
* [41833](https://bugzilla.xamarin.com/show_bug.cgi?id=41833):
    [SGEN?] XS crashed. error: `* Assertion at gc.c:867, condition 'finalizer_thread_exited' not met`
* [41874](https://bugzilla.xamarin.com/show_bug.cgi?id=41874):
    Reflection throws AmbiguousMatchException when calling GetProperty on a class that inherits from a generic base class.
* [41897](https://bugzilla.xamarin.com/show_bug.cgi?id=41897):
    NotSupportedException thrown from IPInterfaceProperties.UnicastAddresses
* [42219](https://bugzilla.xamarin.com/show_bug.cgi?id=42219):
    [System.IO.Compression] Cannot create ZipArchive with duplicate entries with same name
* [42274](https://bugzilla.xamarin.com/show_bug.cgi?id=42274):
    System.IO.Compression.ZipArchive vs System.Xml.XmlReader
* [42413](https://bugzilla.xamarin.com/show_bug.cgi?id=42413):
    Volatile fields don't enforce acquire - release semantics like Volatile.Read() and Volatile.Write()
* [42625](https://bugzilla.xamarin.com/show_bug.cgi?id=42625):
    coop: crash with watchos system tests
* [42688](https://bugzilla.xamarin.com/show_bug.cgi?id=42688):
    Can't wait for more than 429496 ms (429s)
* [42864](https://bugzilla.xamarin.com/show_bug.cgi?id=42864):
    `System.Net.WebException: Error: NameResolutionFailure` on second web request to certain raw IP addresses with `HttpClient`
* [43032](https://bugzilla.xamarin.com/show_bug.cgi?id=43032):
    `System.Uri` cannot parse url with underscore at start
* [43291](https://bugzilla.xamarin.com/show_bug.cgi?id=43291):
    Runtime crash at `reflection.c:mono_custom_attrs_construct_by_type` while calling GetCustomAttributes for a proxy class
* [43512](https://bugzilla.xamarin.com/show_bug.cgi?id=43512):
    `TimeZoneInfo.ConvertTimeBySystemTimeZoneId` ArgumentException
* [43636](https://bugzilla.xamarin.com/show_bug.cgi?id=43636):
    Index was out of range. Must be non-negative and less than the size of the collection&quot; in `System.Collections.Generic.List`1[T].set_Item()` when attempting to compile certain C# code involving tasks, async/await, and try/catch/finally
* [42408](https://bugzilla.xamarin.com/show_bug.cgi?id=42408):
    `WebClient.DownloadString()` returns 401 Unauthorized when using Basic authentication
* [42584](https://bugzilla.xamarin.com/show_bug.cgi?id=42584):
    InternalError / Crash when using System.Net.Http and PCL library
* [42606](https://bugzilla.xamarin.com/show_bug.cgi?id=42606):
    [Regression] Compact seq point enabled by default causes 100% CPU usage
* [42887](https://bugzilla.xamarin.com/show_bug.cgi?id=42887):
    Encoding iso-8859-1 throws IndexOutOfRangeException for Unicode surrogate pairs


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
* **NEW** API Level 24 (vs. API-23):
    [Mono.Android.dll](level_24_diff/mono.android.dll)

