---
id: 78604B51-3CAC-4A4A-A0BC-2E1640B0B200
title: "Xamarin.Android 7.3"
---

Xamarin.Android 7.3: Yay, more fixes!

# OSS Core

Xamarin.Android 7.0 is the first release to use the open-source
repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-2) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-2) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).

# System Requirements

Xamarin.Android 7.3 requires
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

<!--
  JONP: 7.3.1.2 last updated from commit:
    monodroid/d15-2/9dbc4c53c2c3911aeb21776164379181122344ba
    xamarin-android/d15-2/32597a4e9b7695822ef86d937e0c6e698b5180f5
-->

<a name="1"/>
<a name="Xamarin.Android_7.3.1.2"/>

# Xamarin.Android 7.3.1.2

Xamarin.Android 7.3.1.2 is a hotfix release which fixes
`$(BundleAssemblies)` support.

<a name="Bug_Fixes-7.3.1.2"/>

## Bug Fixes

* [56786](https://bugzilla.xamarin.com/show_bug.cgi?id=56786):
    Command line build fails: `fatal error: mono/metadata/mono-config.h: No such file or directory`


<!--
  JONP: 7.3.1 last updated from commit:
    monodroid/d15-2/bc2464555765688415b15e56f88c2abd21e98568
    xamarin-android/d15-2/32597a4e9b7695822ef86d937e0c6e698b5180f5
-->

<a name="1"/>
<a name="Xamarin.Android_7.3.1"/>

# Xamarin.Android 7.3.1

Xamarin.Android 7.3.1 contains bug fixes.

In particular,
[fixes a bug responsible for a large slowdown in Xamarin.Forms apps](https://bugzilla.xamarin.com/show_bug.cgi?id=56240).

<a name="Bug_Fixes-7.3.1"/>

## Bug Fixes

* [56238](https://bugzilla.xamarin.com/show_bug.cgi?id=56238):
    Could not connect to debugger after upgrading to VS 2017 15.2
* [56275](https://bugzilla.xamarin.com/show_bug.cgi?id=56275):
    **Partial**: Unable to copy appname.dll from obj to bin because it is being used by another process.  
    *A* cause of file sharing within `pdb2mdb` is fixed, but there are other known issues.

<!-- Access Denied bugs:
* [55053](https://bugzilla.xamarin.com/show_bug.cgi?id=55053):
* [51340](https://bugzilla.xamarin.com/show_bug.cgi?id=51340):
 -->


<a name="integrated-mono-7.3.1" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.0.0](http://www.mono-project.com/docs/about-mono/releases/5.0.0/)
[commit 5077205](https://github.com/mono/mono/commit/5077205a44a7dc97edf6b67072bea53f043cf815).

* [54448](https://bugzilla.xamarin.com/show_bug.cgi?id=54448):
    Unable to revert to thread-local storage for `CurrentThread.CultureInfo`
* [55041](https://bugzilla.xamarin.com/show_bug.cgi?id=55041):
    Stripping `mscorlib` in simple example changes `IntPtr (5)` behavior?
* [55087](https://bugzilla.xamarin.com/show_bug.cgi?id=55087):
    `System.NotSupportedException`: Stack walks are not supported on this platform - `System.Reflection.MethodBase.GetCurrentMethod`
* [55681](https://bugzilla.xamarin.com/show_bug.cgi?id=55681):
    `System.Reflection.Emit.ModuleBuilder.build_metadata` bug when running FAKE's test suite
* [56240](https://bugzilla.xamarin.com/show_bug.cgi?id=56240):
    Performance Degradation When Using Expressions
* [56260](https://bugzilla.xamarin.com/show_bug.cgi?id=56260):
    Possible regression: This stream does not support writing   at System.IO.Compression.DeflateStream.BeginWrite


<!--
  JONP: 7.3.0 last updated from commit:
    monodroid/d15-2/448f54fdbef91ef7e61800043d549e2cb8754100
    xamarin-android/d15-2/7716c28eecbe395da848db0e658061fbddd759ec
-->

<a name="0"/>
<a name="Xamarin.Android_7.3.0"/>

# Xamarin.Android 7.3

The Xamarin.Android 7.3 release primarily includes bug fixes.

<a name="new-features-7.3"/>

## New Features

* [Bundled ProGuard](#proguard)

<a name="proguard" />

### Bundled ProGuard

Previous releases would use the copy of ProGuard included with the Android SDK
in order to use
[`@(ProguardConfiguration)` files](/guides/android/under_the_hood/build_process/#ProguardConfiguration)
and various other features which rely on ProGuard.

Unfortunately the Android SDK distributes a version of ProGuard which doesn't
support Java 8-generated bytecode, resulting in pain and suffering when
attempting to use later API levels (which require a Java 8 compiler).

The Xamarin.Android 7.3 release includes its own copy of ProGuard 5.3.2,
supporting use of the Java 8 compiler with Xamarin.Android projects.


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


<a name="Known_Issues"/>

## Known Issues


<a name="Bug_Fixes"/>

## Bug Fixes

* [129](https://github.com/xamarin/java.interop/issues/129):
    Fix `class-parse` to use `InvariantCulture` to format floating-point values.
* [12935](https://bugzilla.xamarin.com/show_bug.cgi?id=12935):
    `sensorPortrait` should be `sensorPortait`
* [36079](https://bugzilla.xamarin.com/show_bug.cgi?id=36079):
    `$(AndroidExplicitCrunch)` does not parallelize calls to `aapt`
* [50587](https://bugzilla.xamarin.com/show_bug.cgi?id=50587):
    `AndroidClientHandler.AllowAutoRedirect = false` makes HTTPS requests fail as no body returned
* [51804](https://bugzilla.xamarin.com/show_bug.cgi?id=51804):
    `AndroidClientHandler` has unobserved aggregate exception and `Java.IO` Exceptions in place of `WebException`
* [52521](https://bugzilla.xamarin.com/show_bug.cgi?id=52521):
    `AndroidClientHandler` does not support 304 redirect
* [53054](https://bugzilla.xamarin.com/show_bug.cgi?id=53054):
    AAPT packaging error ignored
* [53787](https://bugzilla.xamarin.com/show_bug.cgi?id=53787):
    Application crashes onto the Simulator and Physical device when running on Debug mode

<!-- Access Denied bugs:
* [52644](https://bugzilla.xamarin.com/show_bug.cgi?id=52644):
* [52928](https://bugzilla.xamarin.com/show_bug.cgi?id=52928):
* [53122](https://bugzilla.xamarin.com/show_bug.cgi?id=53122):
* [53163](https://bugzilla.xamarin.com/show_bug.cgi?id=53163):
* [53413](https://bugzilla.xamarin.com/show_bug.cgi?id=53413):
* [53884](https://bugzilla.xamarin.com/show_bug.cgi?id=53884):
* [53884](https://bugzilla.xamarin.com/show_bug.cgi?id=53884):
* [54353](https://bugzilla.xamarin.com/show_bug.cgi?id=54353):
* [54785](https://bugzilla.xamarin.com/show_bug.cgi?id=54785):
* [55053](https://bugzilla.xamarin.com/show_bug.cgi?id=55053):
* [55402](https://bugzilla.xamarin.com/show_bug.cgi?id=55402):
* [55687](https://bugzilla.xamarin.com/show_bug.cgi?id=55687):
* [55687](https://bugzilla.xamarin.com/show_bug.cgi?id=55687):
 -->


<a name="integrated-mono" />

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.0](http://www.mono-project.com/docs/about-mono/releases/5.0.0/)
[commit e464ddae](https://github.com/mono/mono/commit/71cc0a16c9cf3cb75810dab28e6fd05fa194ba13).

Among the many highlights in Mono 5.0 is support for Portable `.pdb` files.


* [7467](https://bugzilla.xamarin.com/show_bug.cgi?id=7467):
    DefaultNonPersistentConnectionLimit is to low
* [12571](https://bugzilla.xamarin.com/show_bug.cgi?id=12571):
    Usage of XElement with XmlAnyElementAttribute is not supported by XmlSerializer
* [16628](https://bugzilla.xamarin.com/show_bug.cgi?id=16628):
    ilasm crashes on input file
* [19594](https://bugzilla.xamarin.com/show_bug.cgi?id=19594):
    WebException.Response is null when https request needs proxy authentication
* [34715](https://bugzilla.xamarin.com/show_bug.cgi?id=34715):
    HttpClient incorrectly works with multiple headers
* [34802](https://bugzilla.xamarin.com/show_bug.cgi?id=34802):
    Debugger crash on break-all, step into sequence.
* [35536](https://bugzilla.xamarin.com/show_bug.cgi?id=35536):
    Dns.GetHostEntry no longer supports IPv6
* [35662](https://bugzilla.xamarin.com/show_bug.cgi?id=35662):
    Type System.ServiceModel.Security.Tokens.BinarySecretSecurityToken is missing in assembly System.IdentityModel
* [39444](https://bugzilla.xamarin.com/show_bug.cgi?id=39444):
    Action ReflectedType differs from Delegate ReflectedType for virutal methods
* [39832](https://bugzilla.xamarin.com/show_bug.cgi?id=39832):
    SIGSEGV when running roslyn
* [40603](https://bugzilla.xamarin.com/show_bug.cgi?id=40603):
    Mono can't parse Date in DB wich is in format: &quot;2016-02-04 10:39:11Z&quot;
* [41133](https://bugzilla.xamarin.com/show_bug.cgi?id=41133):
    System.MethodAccessException: Method `System.Net.WebHeaderCollection:AddValue (string,string)' is inaccessible from method `System.Net.Http.HttpClientHandler
* [41914](https://bugzilla.xamarin.com/show_bug.cgi?id=41914):
    Race condition in named mutex
* [42226](https://bugzilla.xamarin.com/show_bug.cgi?id=42226):
    WCF client Expecting FaultException&lt;TDetail&gt; raising NotImplemented Exception instead When &lt;FaultActor&gt; element is provided.
* [42271](https://bugzilla.xamarin.com/show_bug.cgi?id=42271):
    COOP: gc unsafe mode when printing native backtrace causes crash if GC is triggered
* [42584](https://bugzilla.xamarin.com/show_bug.cgi?id=42584):
    InternalError / Crash when using System.Net.Http and PCL library
* [42715](https://bugzilla.xamarin.com/show_bug.cgi?id=42715):
    Directory.GetFiles &amp; AllDirectories might fail
* [42843](https://bugzilla.xamarin.com/show_bug.cgi?id=42843):
    XmlSerializer does not deserialize UTC Time values on Xamarin.Android but works well on windows.
* [43921](https://bugzilla.xamarin.com/show_bug.cgi?id=43921):
    System.Threading.ThreadHelper.ThreadStart_Context tries to allocate, crashes
* [44025](https://bugzilla.xamarin.com/show_bug.cgi?id=44025):
    FTP download issue with IPv6
* [44109](https://bugzilla.xamarin.com/show_bug.cgi?id=44109):
    NetworkCredential does not convert SecureString
* [44164](https://bugzilla.xamarin.com/show_bug.cgi?id=44164):
    gosharp-regexp benchmark triggers unwinding crash when profiling
* [44168](https://bugzilla.xamarin.com/show_bug.cgi?id=44168):
    Can use non-accessible member with nameof
* [44296](https://bugzilla.xamarin.com/show_bug.cgi?id=44296):
    Multicast not working on Android 7.0 devices
* [44341](https://bugzilla.xamarin.com/show_bug.cgi?id=44341):
    No way of updating async method local variables
* [44381](https://bugzilla.xamarin.com/show_bug.cgi?id=44381):
    Debugger crash with domain unloading and VSTU
* [44402](https://bugzilla.xamarin.com/show_bug.cgi?id=44402):
    Array doesn't implement non-generic IEnumerable
* [44406](https://bugzilla.xamarin.com/show_bug.cgi?id=44406):
    Xamarin.Mac.Socket exception:An address incompatible with the requested protocol was used
* [44413](https://bugzilla.xamarin.com/show_bug.cgi?id=44413):
    HttpHeaders.TryAddWithoutValidation behaves differently from .NET
* [44440](https://bugzilla.xamarin.com/show_bug.cgi?id=44440):
    Attempting to JIT error in function with pointer arithmetic
* [44549](https://bugzilla.xamarin.com/show_bug.cgi?id=44549):
    Ide Shuts down: System.ArgumentException: Item has already been added. Key in dictionary: 'XamlG'  Key being added: 'XamlG'
* [44552](https://bugzilla.xamarin.com/show_bug.cgi?id=44552):
    Domain end unload event arrives before start unload event
* [44624](https://bugzilla.xamarin.com/show_bug.cgi?id=44624):
    Connecting to SQL Server using IPv4 exception.
* [44707](https://bugzilla.xamarin.com/show_bug.cgi?id=44707):
    RemotingConfiguration.Configure() Throws RemotingException Because it Cannot Load 'machine.config'
* [44714](https://bugzilla.xamarin.com/show_bug.cgi?id=44714):
    xbuild fails to find VB.NET compiler
* [44729](https://bugzilla.xamarin.com/show_bug.cgi?id=44729):
    Type.GetType(&quot;blah&quot;,true,false) throws TypeLoadException without message
* [44751](https://bugzilla.xamarin.com/show_bug.cgi?id=44751):
    Incorrect code flow analysis with goto and out parameter causes CS0177
* [44843](https://bugzilla.xamarin.com/show_bug.cgi?id=44843):
    SqlCommand.ExecuteReaderAsync throws NotImplementedException
* [44937](https://bugzilla.xamarin.com/show_bug.cgi?id=44937):
    System.Diagnostics.StartProcess does not detect dotnetcore compiled assemblies as managed
* [44974](https://bugzilla.xamarin.com/show_bug.cgi?id=44974):
    [pdb] stepping over is not working
* [44978](https://bugzilla.xamarin.com/show_bug.cgi?id=44978):
    HttpClientHandler.SendAsync should throw HttpRequestException for proxy auth failure
* [44982](https://bugzilla.xamarin.com/show_bug.cgi?id=44982):
    SourceFileFilter does not filter on specific file when static ctor exists
* [44994](https://bugzilla.xamarin.com/show_bug.cgi?id=44994):
    DeflateStream decompression is incomplete if reading byte-by-byte
* [45108](https://bugzilla.xamarin.com/show_bug.cgi?id=45108):
    Proxy credentials not used for https url
* [45129](https://bugzilla.xamarin.com/show_bug.cgi?id=45129):
    Uri.IsWellFormedUriString returns incorrect result for relative uris beginning with slash
* [45131](https://bugzilla.xamarin.com/show_bug.cgi?id=45131):
    Array of double*[] being treated as non-blittable when marshaled
* [45137](https://bugzilla.xamarin.com/show_bug.cgi?id=45137):
    Seeing new AAPT0000 errors when building certain projects against master
* [45286](https://bugzilla.xamarin.com/show_bug.cgi?id=45286):
    C# string interpolation line does not compile on OSX but does on MSBuild
* [45371](https://bugzilla.xamarin.com/show_bug.cgi?id=45371):
    SIGSEGV occurs when making call from native to managed code
* [45683](https://bugzilla.xamarin.com/show_bug.cgi?id=45683):
    Add fallback implementation to compile with glibc that lacks CPU_COUNT
* [45761](https://bugzilla.xamarin.com/show_bug.cgi?id=45761):
    After network reconnected, web request fails for a couple of minutes with a NameResolutionFailure
* [45774](https://bugzilla.xamarin.com/show_bug.cgi?id=45774):
    Wrong scopes in .mdb in case of foreach loop
* [45788](https://bugzilla.xamarin.com/show_bug.cgi?id=45788):
    Marshaling a native NULL pointer to a managed array creates a new zero sized array
* [45841](https://bugzilla.xamarin.com/show_bug.cgi?id=45841):
    x86 codegen produces wrong result for float operation
* [45994](https://bugzilla.xamarin.com/show_bug.cgi?id=45994):
    TLS connections on non-standard ports result in incorrect Server Name Indication value
* [46175](https://bugzilla.xamarin.com/show_bug.cgi?id=46175):
    If the RSA will be used by multiple threads, it has a variety of exceptions.
* [46190](https://bugzilla.xamarin.com/show_bug.cgi?id=46190):
    Overload resolution fails in a case where methods use a named parameter in different positions
* [46250](https://bugzilla.xamarin.com/show_bug.cgi?id=46250):
    Type.GetType with throwOnError true doesn't throw for a generic instance type with too few generic arguments
* [46288](https://bugzilla.xamarin.com/show_bug.cgi?id=46288):
    function mono_string_to_byvalwstr may cause access violation
* [46456](https://bugzilla.xamarin.com/show_bug.cgi?id=46456):
    CultureInfo(&quot;ug-CN&quot;) not found in Xamarin.Android and Xamarin.iOS
* [46536](https://bugzilla.xamarin.com/show_bug.cgi?id=46536):
    [coop] mono_os_mutex_destroy: pthread_mutex_destroy failed with &quot;Device or resource busy&quot; (16)
* [46538](https://bugzilla.xamarin.com/show_bug.cgi?id=46538):
    System.Net.WebClient.OpenReadAsync/OpenReadTaskAsync do not work for file:// URLs
* [46602](https://bugzilla.xamarin.com/show_bug.cgi?id=46602):
    MobileAuthenticatedStream.AuthenticateAsServer() via EndPointListener
* [46712](https://bugzilla.xamarin.com/show_bug.cgi?id=46712):
    btls fails to build with gcc is v4.4.7 or earlier as they lack alignof/alignas
* [46739](https://bugzilla.xamarin.com/show_bug.cgi?id=46739):
    Assembly::Evidence property crashes for unbaked assembly
* [46806](https://bugzilla.xamarin.com/show_bug.cgi?id=46806):
    opspecial011.Program.DynamicCSharpRunTest test in ms-test-suite fails with &quot;Operator '+' cannot be applied to operands&quot;
* [46929](https://bugzilla.xamarin.com/show_bug.cgi?id=46929):
    Datetime error on Mono.data.Sqlite
* [47152](https://bugzilla.xamarin.com/show_bug.cgi?id=47152):
    AOT attempts at Xamarin.Mac.dll crash mono
* [47156](https://bugzilla.xamarin.com/show_bug.cgi?id=47156):
    * Assertion at class.c:2093
* [47205](https://bugzilla.xamarin.com/show_bug.cgi?id=47205):
    Uri.TryCreate throws exception
* [47221](https://bugzilla.xamarin.com/show_bug.cgi?id=47221):
    Thread.Name can only be set once inside async callback
* [47353](https://bugzilla.xamarin.com/show_bug.cgi?id=47353):
    Mono.CSharp.MetadataImporter.set_IgnoreCompilerGeneratedField not found when running Cake on Mono 4.8
* [47549](https://bugzilla.xamarin.com/show_bug.cgi?id=47549):
    Chunked encoding error when writing zero buffer
* [47672](https://bugzilla.xamarin.com/show_bug.cgi?id=47672):
    Invalid error CS0314
* [47762](https://bugzilla.xamarin.com/show_bug.cgi?id=47762):
    EXC_BAD_ACCESS when unloading assembly
* [47867](https://bugzilla.xamarin.com/show_bug.cgi?id=47867):
    assert at sre.c:1553 in System.Reflection.Emit.TypeBuilder.create_runtime_class
* [48016](https://bugzilla.xamarin.com/show_bug.cgi?id=48016):
    System.Net.NetworkInformation.DnsAddresses is always empty. Fix included.
* [48429](https://bugzilla.xamarin.com/show_bug.cgi?id=48429):
    Mono fails to marshal fixed buffer fields as unicode
* [48516](https://bugzilla.xamarin.com/show_bug.cgi?id=48516):
    ZipArchive.Save attempts to set position and seek non-seekable streams
* [49056](https://bugzilla.xamarin.com/show_bug.cgi?id=49056):
    Assertion at /Users/builder/data/lanes/3969/44931ae8/source/xamarin-macios/external/mono/mono/mini/mini-generic-sharing.c:2351, condition `info' not met
* [49686](https://bugzilla.xamarin.com/show_bug.cgi?id=49686):
    System.NotImplementedException at System.Reflection.Emit.DynamicMethod.GetCustomAttributes (System.Type attributeType, Boolean inherit)
* [50242](https://bugzilla.xamarin.com/show_bug.cgi?id=50242):
    Cannot use MSXSL format-date/format-time XPath extension functions on non-Windows platforms
* [50789](https://bugzilla.xamarin.com/show_bug.cgi?id=50789):
    JITting large method fails (condition lvregs_len &lt; 1024 not met)
* [51166](https://bugzilla.xamarin.com/show_bug.cgi?id=51166):
    mcs converts new T[0] into Array.Empty&lt;T&gt;() which is not conform C# spec
* [51219](https://bugzilla.xamarin.com/show_bug.cgi?id=51219):
    ves_icall_System_Threading_ThreadPool_RequestWorkerThread called after threadpool cleanup
* [51330](https://bugzilla.xamarin.com/show_bug.cgi?id=51330):
    Inline Enum::GetHashCode implementation
* [51506](https://bugzilla.xamarin.com/show_bug.cgi?id=51506):
    C# compiler fails for constrained generics with yield return
* [51545](https://bugzilla.xamarin.com/show_bug.cgi?id=51545):
    [Crash] mono_threads_platform_set_priority: unknown policy 3
* [51562](https://bugzilla.xamarin.com/show_bug.cgi?id=51562):
    NullReferenceException in BTLS X509CertificateImplBtls.Import()
* [51653](https://bugzilla.xamarin.com/show_bug.cgi?id=51653):
    mono_thread_info_wait_one_handle ignored alertable argument
* [52157](https://bugzilla.xamarin.com/show_bug.cgi?id=52157):
    SocketTest.ConnectedProperty test fails in FullAOT Linux runs
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
* [52549](https://bugzilla.xamarin.com/show_bug.cgi?id=52549):
    error: mono_w32socket_convert_error: no translation into winsock error for (41) &quot;Protocol wrong type for socket&quot;
* [52600](https://bugzilla.xamarin.com/show_bug.cgi?id=52600):
    Full AOT: Strange combination of structs, generics, and enums causes runtime failure
* [52845](https://bugzilla.xamarin.com/show_bug.cgi?id=52845):
    [Cycle 9] Satellite assemblies not bundled when using &quot;Bundle assemblies into native code&quot; due to &quot;unknown escape sequence&quot; error from gcc during mkbundle step
* [52866](https://bugzilla.xamarin.com/show_bug.cgi?id=52866):
    F# sprintf AOT bug still exists
* [52899](https://bugzilla.xamarin.com/show_bug.cgi?id=52899):
    mprof-report missing filenames in coverage xml output when using portable pdbs
* [53066](https://bugzilla.xamarin.com/show_bug.cgi?id=53066):
    Can't Build Project in Debug with &quot;Could not AOT the assembly&quot;
* [53231](https://bugzilla.xamarin.com/show_bug.cgi?id=53231):
    csc doesn't unify same file passed multiple times when one path is relative
* [53278](https://bugzilla.xamarin.com/show_bug.cgi?id=53278):
    Two coreclr SIMD test failures (one regression from 4.8)
* [53481](https://bugzilla.xamarin.com/show_bug.cgi?id=53481):
    The threadpool crashes on XS CI
* [53684](https://bugzilla.xamarin.com/show_bug.cgi?id=53684):
    Crash when enumerating directory and selecting the first file
* [53689](https://bugzilla.xamarin.com/show_bug.cgi?id=53689):
    [Test] Certificate7 disabled due to SecCertificateCreateWithData does different things on 10.11 vs 10.12 with invalid certificates
* [53843](https://bugzilla.xamarin.com/show_bug.cgi?id=53843):
    Mono deadlocks on shutdown while waiting for a process which has died
* [53890](https://bugzilla.xamarin.com/show_bug.cgi?id=53890):
    Regression: Native crash while running tests with xunit with mono 2017-02 branch, works with 4.8.0.520
* [55148](https://bugzilla.xamarin.com/show_bug.cgi?id=55148):
    Debugger checks type which is possibly never used

<!-- Access Denied bugs:
* [27061](https://bugzilla.xamarin.com/show_bug.cgi?id=27061):
* [42903](https://bugzilla.xamarin.com/show_bug.cgi?id=42903):
* [44212](https://bugzilla.xamarin.com/show_bug.cgi?id=44212):
* [44757](https://bugzilla.xamarin.com/show_bug.cgi?id=44757):
* [45140](https://bugzilla.xamarin.com/show_bug.cgi?id=45140):
* [45223](https://bugzilla.xamarin.com/show_bug.cgi?id=45223):
* [45369](https://bugzilla.xamarin.com/show_bug.cgi?id=45369):
* [45687](https://bugzilla.xamarin.com/show_bug.cgi?id=45687):
* [45847](https://bugzilla.xamarin.com/show_bug.cgi?id=45847):
* [45950](https://bugzilla.xamarin.com/show_bug.cgi?id=45950):
* [46375](https://bugzilla.xamarin.com/show_bug.cgi?id=46375):
* [46479](https://bugzilla.xamarin.com/show_bug.cgi?id=46479):
* [46549](https://bugzilla.xamarin.com/show_bug.cgi?id=46549):
* [49423](https://bugzilla.xamarin.com/show_bug.cgi?id=49423):
* [50117](https://bugzilla.xamarin.com/show_bug.cgi?id=50117):
* [50710](https://bugzilla.xamarin.com/show_bug.cgi?id=50710):
* [51206](https://bugzilla.xamarin.com/show_bug.cgi?id=51206):
* [51625](https://bugzilla.xamarin.com/show_bug.cgi?id=51625):
* [52548](https://bugzilla.xamarin.com/show_bug.cgi?id=52548):
* [52846](https://bugzilla.xamarin.com/show_bug.cgi?id=52846):
* [53015](https://bugzilla.xamarin.com/show_bug.cgi?id=53015):
* [53958](https://bugzilla.xamarin.com/show_bug.cgi?id=53958):
* [54976](https://bugzilla.xamarin.com/show_bug.cgi?id=54976):
* [55095](https://bugzilla.xamarin.com/show_bug.cgi?id=55095):
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

