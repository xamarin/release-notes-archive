---
id: 584C7285-1E6C-403E-8088-292EAF1DEF39
title: "Xamarin.Android 7.1"
---

Xamarin.Android 7.1: Yay, fixes!

# OSS Core

Xamarin.Android 7.0 is the first release to use the open-source
repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android?at=57c487782dcc4f312942a519).

# System Requirements

Xamarin.Android 7.1 requires
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

(One unfortunate complication with JDK 1.8 is that is **not** compatible with
the outdated version of Proguard that is included in the Android SDK. Currently
this will cause an error "Unsupported class version number \[52.0\]" when
attempting to use the Proguard or Multidex features in Xamarin.Android. See
[44187](https://bugzilla.xamarin.com/show_bug.cgi?id=44187).)


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

Xamarin.Android 7.0, which is part of Cycle 8,
[updates `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to include
a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

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
  JONP: 7.1.0 last updated from commit monodroid/cycle9/3a62f1ea1f66df7d11edb8a049e923f20b38fc1a
-->

<a name="0"/>
<a name="Xamarin.Android_7.1.0"/>
# Xamarin.Android 7.1.0-43

(We forgot to bump the micro version. Oops.)

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.8](http://www.mono-project.com/docs/about-mono/releases/4.8.0/)
[commit 8f6d0f67](https://github.com/mono/mono/commit/8f6d0f67f7b80e03f7fc5c9b695531948ede0410).

* [46929](https://bugzilla.xamarin.com/show_bug.cgi?id=46929):
    Datetime error on Mono.data.Sqlite
* [52437](https://bugzilla.xamarin.com/show_bug.cgi?id=52437):
    Random NullReferenceExceptions in StringBuilder.ThreadSafeCopy
* [52590](https://bugzilla.xamarin.com/show_bug.cgi?id=52590):
    Cannot compile for iOS, TypeBuilder exists in two places.
* [52845](https://bugzilla.xamarin.com/show_bug.cgi?id=52845):
    Satellite assemblies not bundled when using &quot;Bundle assemblies into native code&quot; due to &quot;unknown escape sequence&quot; error from gcc during mkbundle step
* [53066](https://bugzilla.xamarin.com/show_bug.cgi?id=53066):
    Can't Build Project in Debug with &quot;Could not AOT the assembly&quot;

<!-- Access Denied bugs:
* [52300](https://bugzilla.xamarin.com/show_bug.cgi?id=52300):
* [52846](https://bugzilla.xamarin.com/show_bug.cgi?id=52846):
 -->


<a name="0"/>
<a name="Xamarin.Android_7.1.0"/>
# Xamarin.Android 7.1

The Xamarin.Android 7.1 release primarily includes bug fixes.

<a name="new-features-7.1"/>
## New Features

* Bindings for [API-25, Android v7.1][api-25].
* Support for providing [Android circular icons][round-icons], e.g. through
    the new `Android.App.ActivityAttribute.RoundIcon` property.
* [Linker improvements](#linker-improvements)
* Visual Studio 2017 Support for side-by-side installations.

[api-25]: https://developer.android.com/sdk/api_diff/25/changes/changes-summary.html
[round-icons]: https://developer.android.com/about/versions/nougat/android-7.1.html#circular-icons

<a name="linker-improvements" />
### Linker Improvements

<!--
https://bugzilla.xamarin.com/show_bug.cgi?id=51419#c5
-->

Previously, if all type references to a given assembly were removed,
the assembly reference would remain. Starting in Xamarin.Android 7.1,
the assembly reference will be removed.

For example, `System.dll`
contains a reference to `System.Xml.Serialization.XmlIgnoreAttribute`,
located in `System.Xml.dll`. If `XmlIgnoreAttribute` isn't used by the
application, the *type reference* within `System.dll` will be removed.

However, in Xamarin.Android 7.0 and prior releases, even though there
there may be no remaining references to `System.Xml.dll`,
`System.Xml.dll` would still be packaged and distributed within the
application package (`.apk` file).

Starting in Xamarin.Android 7.1, in this scenario `System.dll` will be
modified to *no longer contain* an assembly reference to
`System.Xml.dll`, allowing `System.Xml.dll` to be removed from the package.

This change should result in smaller application packages without
breaking compatibility.

*However*, if an assembly was being loaded *dynamically*, for example
through [`Assembly.Load("System.Xml")`][assembly-load], then an exception may
now be thrown. If this is the case, you can use the
[`$(AndroidLinkSkip)`](guides/android/advanced_topics/linking/#linkskip)
MSBuild property to explicitly preserve the referenced assembly.

[assembly-load]: https://msdn.microsoft.com/en-us/library/system.reflection.assembly.load(v=vs.110).aspx


<a name="experimental-features"/>
## Experimental Features

Xamarin.Android 7.0 introduces several experimental features, which are still experimental:

* [TLS 1.2 support in `WebRequest`](#btls)
* [Improved Fast Deployment](#Fast_Deployment)

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


<a name="Bug_Fixes"/>
## Bug Fixes

* [37263](https://bugzilla.xamarin.com/show_bug.cgi?id=37263):
    Preserve application data no longer works
* [37491](https://bugzilla.xamarin.com/show_bug.cgi?id=37491):
    App crashes in Release config on device with `System.Runtime.Serialization.InvalidDataContractException`
* [42091](https://bugzilla.xamarin.com/show_bug.cgi?id=42091):
    Latest update breaks `InputJar` bindings
* [42366](https://bugzilla.xamarin.com/show_bug.cgi?id=42366):
    Exception doesn't include Java native stacktrace anymore
* [43287](https://bugzilla.xamarin.com/show_bug.cgi?id=43287):
    System modal windows during release build
* [44447](https://bugzilla.xamarin.com/show_bug.cgi?id=44447):
    Android symbolication uses wrong property
* [44531](https://bugzilla.xamarin.com/show_bug.cgi?id=44531):
    [Generator] new error CS0533: $(CHILD) hides inherited abstract member from $(PARENT)
* [44961](https://bugzilla.xamarin.com/show_bug.cgi?id=44961):
    AndroidClientHandler throws NetworkOnMainThreadException
* [45137](https://bugzilla.xamarin.com/show_bug.cgi?id=45137):
    Seeing new AAPT0000 errors when building certain projects against master
* [45311](https://bugzilla.xamarin.com/show_bug.cgi?id=45311):
    Bug in constructor of AndroidHttpResponseMessage
* [46344](https://bugzilla.xamarin.com/show_bug.cgi?id=46344):
    Unhandled Exception in `class-parse` when processing nested generic types.
* [48508](https://bugzilla.xamarin.com/show_bug.cgi?id=48508):
    Archiving Android application is archiving old builds
* [51356](https://bugzilla.xamarin.com/show_bug.cgi?id=51356):
    Unable to run Multi-Dex

<!-- Access Denied bugs:
* [32457](https://bugzilla.xamarin.com/show_bug.cgi?id=32457):
* [39002](https://bugzilla.xamarin.com/show_bug.cgi?id=39002):
* [40172](https://bugzilla.xamarin.com/show_bug.cgi?id=40172):
* [40179](https://bugzilla.xamarin.com/show_bug.cgi?id=40179):
* [40275](https://bugzilla.xamarin.com/show_bug.cgi?id=40275):
* [41860](https://bugzilla.xamarin.com/show_bug.cgi?id=41860):
* [42360](https://bugzilla.xamarin.com/show_bug.cgi?id=42360):
* [42521](https://bugzilla.xamarin.com/show_bug.cgi?id=42521):
* [42788](http://bugzilla.xamarin.com/show_bug.cgi?id=42788):
* [42835](https://bugzilla.xamarin.com/show_bug.cgi?id=42835):
* [43381](https://bugzilla.xamarin.com/show_bug.cgi?id=43381):
* [43487](https://bugzilla.xamarin.com/show_bug.cgi?id=43487):
* [43549](https://bugzilla.xamarin.com/show_bug.cgi?id=43549):
* [43550](https://bugzilla.xamarin.com/show_bug.cgi?id=43550):
* [43551](https://bugzilla.xamarin.com/show_bug.cgi?id=43551):
* [43661](https://bugzilla.xamarin.com/show_bug.cgi?id=43661):
* [43880](https://bugzilla.xamarin.com/show_bug.cgi?id=43880):
* [43910](https://bugzilla.xamarin.com/show_bug.cgi?id=43910):
* [43915](https://bugzilla.xamarin.com/show_bug.cgi?id=43915):
* [44217](https://bugzilla.xamarin.com/show_bug.cgi?id=44217):
* [44448](https://bugzilla.xamarin.com/show_bug.cgi?id=44448):
* [44528](https://bugzilla.xamarin.com/show_bug.cgi?id=44528):
* [45543](https://bugzilla.xamarin.com/show_bug.cgi?id=45543):
* [46509](https://bugzilla.xamarin.com/show_bug.cgi?id=46509):
* [48213](https://bugzilla.xamarin.com/show_bug.cgi?id=48213):
* [51337](https://bugzilla.xamarin.com/show_bug.cgi?id=51337):
* [51339](https://bugzilla.xamarin.com/show_bug.cgi?id=51636):
* [51340](https://bugzilla.xamarin.com/show_bug.cgi?id=51636):
* [51636](https://bugzilla.xamarin.com/show_bug.cgi?id=51636):
 -->


<a name="breaking-changes" />
## Breaking Changes

* [Removal of interface default methods in API-24](#iface-default-removal)

<a name="iface-default-removal" />
### Removal of interface default methods in API-24

API-24 introduced support for Java 1.8 and a number of new Java language
features such as [interface default methods](https://github.com/xamarin/java.interop/issues/25).

Interface default methods were originally bound as "normal" interface methods,
which resulted in many interface bindings containing methods that, in retrospect,
we feel shouldn't be there.

We feel that this breakage is acceptable because:

1. It only impacts API-24, which at present is used on 0.3% of Android devices.

2. Only impacts 3 interfaces: `Java.Util.IPrimitiveIteratorOfDouble`,
    `Java.Util.IPrimitiveIteratorOfInt`, and `Java.Util.IPrimitiveIteratorOfLong`.

3. The above interfaces are extremely unlikely to be *implemented* by anyone.

<a name="integrated-mono" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.8](http://www.mono-project.com/docs/about-mono/releases/4.8.0/)
[commit ed0fb9de](https://github.com/mono/mono/commit/ed0fb9dea072737e74a5c2302d14dd3ccd5cb23a).

* [5644](https://bugzilla.xamarin.com/show_bug.cgi?id=5644):
    Mono allows to access not accessible method
* [7467](https://bugzilla.xamarin.com/show_bug.cgi?id=7467):
    DefaultNonPersistentConnectionLimit is to low
* [12571](https://bugzilla.xamarin.com/show_bug.cgi?id=12571):
    Usage of XElement with XmlAnyElementAttribute is not supported by XmlSerializer
* [19594](https://bugzilla.xamarin.com/show_bug.cgi?id=19594):
    WebException.Response is null when https request needs proxy authentication
* [29189](https://bugzilla.xamarin.com/show_bug.cgi?id=29189):
    Compiling class referencing corefx facade/contract assemblies raises error &quot;Reference to type `System.SByte' claims it is defined assembly `mscorlib,..` but couldn't be found&quot;
* [30146](https://bugzilla.xamarin.com/show_bug.cgi?id=30146):
    stack imbalance in DllImport with CallingConvention.StdCall
* [30686](https://bugzilla.xamarin.com/show_bug.cgi?id=30686):
    ZipArchive ctor throws InvalidDataException for WebConnectionStream
* [30821](https://bugzilla.xamarin.com/show_bug.cgi?id=30821):
    Compilation generates CS1701 warning
* [32374](https://bugzilla.xamarin.com/show_bug.cgi?id=32374):
    WebRequest::BeginGetRequestStream incorrectly sets IAsyncResult::CompletedSynchronously to always true
* [33571](https://bugzilla.xamarin.com/show_bug.cgi?id=33571):
    Mono crashes when marshalling fixed arrays
* [34715](https://bugzilla.xamarin.com/show_bug.cgi?id=34715):
    HttpClient incorrectly works with multiple headers
* [34802](https://bugzilla.xamarin.com/show_bug.cgi?id=34802):
    Debugger crash on break-all, step into sequence.
* [35536](https://bugzilla.xamarin.com/show_bug.cgi?id=35536):
    Dns.GetHostEntry no longer supports IPv6
* [35662](https://bugzilla.xamarin.com/show_bug.cgi?id=35662):
    Type System.ServiceModel.Security.Tokens.BinarySecretSecurityToken is missing in assembly System.IdentityModel
* [38025](https://bugzilla.xamarin.com/show_bug.cgi?id=38025):
    &quot;Step Out&quot; gets confused by nested code
* [39282](https://bugzilla.xamarin.com/show_bug.cgi?id=39282):
    [System.IO.Compression] issues with ZipArchiveEntry streams
* [39832](https://bugzilla.xamarin.com/show_bug.cgi?id=39832):
    SIGSEGV when running roslyn
* [39859](https://bugzilla.xamarin.com/show_bug.cgi?id=39859):
    Xamarin.Android apps on the Samsung Galaxy S7 fails to start with the error System.ExecutionEngineException SIGILL
* [40603](https://bugzilla.xamarin.com/show_bug.cgi?id=40603):
    Mono can't parse Date in DB wich is in format: &quot;2016-02-04 10:39:11Z&quot;
* [40916](https://bugzilla.xamarin.com/show_bug.cgi?id=40916):
    [System.IO.Compression] ZipArchive can create an ZipArchiveEntry that has a modified time of DateTime.MinValue
* [41133](https://bugzilla.xamarin.com/show_bug.cgi?id=41133):
    System.MethodAccessException: Method `System.Net.WebHeaderCollection:AddValue (string,string)` is inaccessible from method `System.Net.Http.HttpClientHandler`
* [41035](https://bugzilla.xamarin.com/show_bug.cgi?id=41035):
    DataViewTest2.DataView_ListChangedEventTest occasionally fails with llvm+sgen
* [41349](https://bugzilla.xamarin.com/show_bug.cgi?id=41349):
    System.TimeZoneInfo.IsDaylightSavingTime (DateTimeOffset dateTimeOffset) Not Implemented Exception
* [41393](https://bugzilla.xamarin.com/show_bug.cgi?id=41393):
    [WatchOS 2] Incorrect calling convention for P/Invokes taking structures
* [41431](https://bugzilla.xamarin.com/show_bug.cgi?id=41431):
    [aot] Build fails due to 'Sgen STW requires a working mono-context' error
* [41466](https://bugzilla.xamarin.com/show_bug.cgi?id=41466):
    mono_class_is_subclass_of return incorrect value by assuming mono_class_init has been called on parameters
* [41477](https://bugzilla.xamarin.com/show_bug.cgi?id=41477):
    SafeSocketHandle ObjectDisposedException 'handle' exception with linked CancellationTokenSource
* [41492](https://bugzilla.xamarin.com/show_bug.cgi?id=41492):
    DateTimeOffset.ToLocalTime() throwing erroneous error
* [41509](https://bugzilla.xamarin.com/show_bug.cgi?id=41509):
    DLR crashes when trying to convert a object to null.
* [41530](https://bugzilla.xamarin.com/show_bug.cgi?id=41530):
    [iOS]TimerTest failing randomly on devices,
* [41552](https://bugzilla.xamarin.com/show_bug.cgi?id=41552):
    HttpResponseMessage does not support multiple Links header entries
* [41575](https://bugzilla.xamarin.com/show_bug.cgi?id=41575):
    A Method That Accepts a FormattableString Object Is Not Called
* [41602](https://bugzilla.xamarin.com/show_bug.cgi?id=41602):
    Compiler fails to recognize Indexer
* [41616](https://bugzilla.xamarin.com/show_bug.cgi?id=41616):
    Mono 4.4.0 crashes when using Socket.ConnectAsync to a unix domain socket if the path doesn't exist
* [41623](https://bugzilla.xamarin.com/show_bug.cgi?id=41623):
    &quot;Step Over&quot; on an Android App deployed to a physical/virtual device crashes the app
* [41667](https://bugzilla.xamarin.com/show_bug.cgi?id=41667):
    new DateTime().ToLocalTime() results in an exception
* [41705](https://bugzilla.xamarin.com/show_bug.cgi?id=41705):
    MonoTests.System.Threading.MonitorTest.Enter_Null crashes test runtime with assertion
* [41775](https://bugzilla.xamarin.com/show_bug.cgi?id=41775):
    Zip version needed to extract not correct in System.IO.Compression
* [41782](https://bugzilla.xamarin.com/show_bug.cgi?id=41782):
    [Cycle 7] &quot;System.Net.WebException: Error: NameResolutionFailure&quot; when attempting web requests with certain raw IP addresses
* [41786](https://bugzilla.xamarin.com/show_bug.cgi?id=41786):
    Mono is broken when building with the macOS 10.12 SDK
* [41833](https://bugzilla.xamarin.com/show_bug.cgi?id=41833):
    [SGEN?] XS crashed. error: * Assertion at gc.c:867, condition `finalizer_thread_exited' not met
* [41874](https://bugzilla.xamarin.com/show_bug.cgi?id=41874):
    Reflection throws AmbiguousMatchException when calling GetProperty on a class that inherits from a generic base class.
* [41897](https://bugzilla.xamarin.com/show_bug.cgi?id=41897):
    NotSupportedException thrown from IPInterfaceProperties.UnicastAddresses
* [41937](https://bugzilla.xamarin.com/show_bug.cgi?id=41937):
    invoke.exe test asserts on bitcode
* [41955](https://bugzilla.xamarin.com/show_bug.cgi?id=41955):
    Bitcode &quot;missing image did not probe corlib&quot; exception thrown
* [41979](https://bugzilla.xamarin.com/show_bug.cgi?id=41979):
    CodeDom cannot call mcs because of invalid encoding configuration
* [42057](https://bugzilla.xamarin.com/show_bug.cgi?id=42057):
    error CS0121: The call is ambiguous
* [42169](https://bugzilla.xamarin.com/show_bug.cgi?id=42169):
    (managed_alloc) Fatal: Managed allocator missing for (mkbundle) in Mono 4.4.X
* [42191](https://bugzilla.xamarin.com/show_bug.cgi?id=42191):
    sdb deadlocks all the time while XS debugs XS
* [42198](https://bugzilla.xamarin.com/show_bug.cgi?id=42198):
    error CS0529: Inherited interface causes a cycle in the interface hierarchy.
* [42219](https://bugzilla.xamarin.com/show_bug.cgi?id=42219):
    [System.IO.Compression] Cannot create ZipArchive with duplicate entries with same name
* [42224](https://bugzilla.xamarin.com/show_bug.cgi?id=42224):
    Compiler crashed with code: 1, &quot;Await yields with non-empty stack&quot; from AssertEmptyStack ()
* [42226](https://bugzilla.xamarin.com/show_bug.cgi?id=42226):
    WCF client Expecting FaultException&lt;TDetail&gt; raising NotImplemented Exception instead When &lt;FaultActor&gt; element is provided.
* [42271](https://bugzilla.xamarin.com/show_bug.cgi?id=42271):
    COOP: gc unsafe mode when printing native backtrace causes crash if GC is triggered
* [42274](https://bugzilla.xamarin.com/show_bug.cgi?id=42274):
    System.IO.Compression.ZipArchive vs System.Xml.XmlReader
* [42395](https://bugzilla.xamarin.com/show_bug.cgi?id=42395):
    Build runs indefinitely and never finishes
* [42408](https://bugzilla.xamarin.com/show_bug.cgi?id=42408):
    WebClient.DownloadString returns 401 Unauthorized when using Basic authentication
* [42410](https://bugzilla.xamarin.com/show_bug.cgi?id=42410):
    String Interpolation available even when langversion &lt; 6
* [42413](https://bugzilla.xamarin.com/show_bug.cgi?id=42413):
    Volatile fields don't enforce acquire - release semantics like Volatile.Read() and Volatile.Write()
* [42584](https://bugzilla.xamarin.com/show_bug.cgi?id=42584):
    InternalError / Crash when using System.Net.Http and PCL library
* [42585](https://bugzilla.xamarin.com/show_bug.cgi?id=42585):
    Switch fall-through not rejected
* [42611](https://bugzilla.xamarin.com/show_bug.cgi?id=42611):
    wrong compiler error when using IEnumerable.Sum
* [42625](https://bugzilla.xamarin.com/show_bug.cgi?id=42625):
    coop: crash with watchos system tests
* [42688](https://bugzilla.xamarin.com/show_bug.cgi?id=42688):
    Can't wait for more than 429496 ms (429s)
* [42702](https://bugzilla.xamarin.com/show_bug.cgi?id=42702):
    Unnecessary dependency checks
* [42750](https://bugzilla.xamarin.com/show_bug.cgi?id=42750):
    Deploying an iOS app to iPhone 6S crashes when a breakpoint is set
* [42843](https://bugzilla.xamarin.com/show_bug.cgi?id=42843):
    XmlSerializer does not deserialize UTC Time values on Xamarin.Android but works well on windows.
* [42864](https://bugzilla.xamarin.com/show_bug.cgi?id=42864):
    [Cycle 7] &quot;System.Net.WebException: Error: NameResolutionFailure&quot; on second web request to certain raw IP addresses with HttpClient
* [42887](https://bugzilla.xamarin.com/show_bug.cgi?id=42887):
    Encoding iso-8859-1 throws IndexOutOfRangeException for Unicode surrogate pairs
* [43022](https://bugzilla.xamarin.com/show_bug.cgi?id=43022):
    ZipArchive.Entries is not updated when ZipArchiveEntry is deleted
* [43032](https://bugzilla.xamarin.com/show_bug.cgi?id=43032):
    System.Uri cannot parse url with underscore at start
* [43099](https://bugzilla.xamarin.com/show_bug.cgi?id=43099):
    [watchOS] Cannot enter GC safe region if the thread is not attached
* [43193](https://bugzilla.xamarin.com/show_bug.cgi?id=43193):
    Keep CurrentCulture in async/await
* [43265](https://bugzilla.xamarin.com/show_bug.cgi?id=43265):
    Inconsistency in Compilation of Async Code Compared to MSFT Compilers
* [43291](https://bugzilla.xamarin.com/show_bug.cgi?id=43291):
    Runtime crash at reflection.c:mono_custom_attrs_construct_by_type while calling GetCustomAttributes for a proxy class
* [43320](https://bugzilla.xamarin.com/show_bug.cgi?id=43320):
    Thread aborts in the middle of .cctor and hell break loose
* [43357](https://bugzilla.xamarin.com/show_bug.cgi?id=43357):
    WCSessionReplyHandler crashes WatchKit app
* [43400](https://bugzilla.xamarin.com/show_bug.cgi?id=43400):
    &quot;using static&quot; dependent on compile order
* [43410](https://bugzilla.xamarin.com/show_bug.cgi?id=43410):
    Nested exception trying to figure out what went wrong
* [43471](https://bugzilla.xamarin.com/show_bug.cgi?id=43471):
    pragma warning disable still shows warnings in &quot;Errors&quot; pad
* [43512](https://bugzilla.xamarin.com/show_bug.cgi?id=43512):
    TimeZoneInfo.ConvertTimeBySystemTimeZoneId ArgumentException
* [43636](https://bugzilla.xamarin.com/show_bug.cgi?id=43636):
    [Cycle 8] &quot;Index was out of range. Must be non-negative and less than the size of the collection&quot; in `System.Collections.Generic.List`1[T].set_Item()` when attempting to compile certain C# code involving tasks, async/await, and try/catch/finally
* [43645](https://bugzilla.xamarin.com/show_bug.cgi?id=43645):
    Items and properties not emitted for up to date targets
* [43695](https://bugzilla.xamarin.com/show_bug.cgi?id=43695):
    Nuget resolves .netstandard &lt;= 1.3 when Xamarin.IOS does not support it
* [43696](https://bugzilla.xamarin.com/show_bug.cgi?id=43696):
    Delegate caching can invoke unrelated implementation leading to strange results
* [43718](https://bugzilla.xamarin.com/show_bug.cgi?id=43718):
    mcs crashes when unable to resolve type inside lambda using the 'as' operator
* [43786](https://bugzilla.xamarin.com/show_bug.cgi?id=43786):
    peverify is broken again
* [43921](https://bugzilla.xamarin.com/show_bug.cgi?id=43921):
    System.Threading.ThreadHelper.ThreadStart_Context tries to allocate, crashes
* [44025](https://bugzilla.xamarin.com/show_bug.cgi?id=44025):
    FTP download issue with IPv6
* [44109](https://bugzilla.xamarin.com/show_bug.cgi?id=44109):
    NetworkCredential does not convert SecureString
* [44132](https://bugzilla.xamarin.com/show_bug.cgi?id=44132):
    Thread.Sleep () overhead too big
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
* [44918](https://bugzilla.xamarin.com/show_bug.cgi?id=44918):
    &quot;Assertion mini-arm.c:434, condition `lmf_addr_tls_offset != -1' not met&quot; prevent mono to run on ARM
* [44937](https://bugzilla.xamarin.com/show_bug.cgi?id=44937):
    System.Diagnostics.StartProcess does not detect dotnetcore compiled assemblies as managed
* [44978](https://bugzilla.xamarin.com/show_bug.cgi?id=44978):
    HttpClientHandler.SendAsync should throw HttpRequestException for proxy auth failure
* [44994](https://bugzilla.xamarin.com/show_bug.cgi?id=44994):
    DeflateStream decompression is incomplete if reading byte-by-byte
* [45108](https://bugzilla.xamarin.com/show_bug.cgi?id=45108):
    Proxy credentials not used for https url
* [45137](https://bugzilla.xamarin.com/show_bug.cgi?id=45137):
    Seeing new AAPT0000 errors when building certain projects against master
* [45129](https://bugzilla.xamarin.com/show_bug.cgi?id=45129):
    Uri.IsWellFormedUriString returns incorrect result for relative uris beginning with slash
* [45131](https://bugzilla.xamarin.com/show_bug.cgi?id=45131):
    Array of double*[] being treated as non-blittable when marshaled
* [45286](https://bugzilla.xamarin.com/show_bug.cgi?id=45286):
    C# string interpolation line does not compile on OSX but does on MSBuild
* [45371](https://bugzilla.xamarin.com/show_bug.cgi?id=45371):
    SIGSEGV occurs when making call from native to managed code
* [45761](https://bugzilla.xamarin.com/show_bug.cgi?id=45761):
    After network reconnected, web request fails for a couple of minutes with a NameResolutionFailure
* [45774](https://bugzilla.xamarin.com/show_bug.cgi?id=45774):
    Wrong scopes in .mdb in case of foreach loop
* [45788](https://bugzilla.xamarin.com/show_bug.cgi?id=45788):
    Marshaling a native NULL pointer to a managed array creates a new zero sized array
* [45994](https://bugzilla.xamarin.com/show_bug.cgi?id=45994):
    TLS connections on non-standard ports result in incorrect Server Name Indication value
* [46175](https://bugzilla.xamarin.com/show_bug.cgi?id=46175):
    If the RSA will be used by multiple threads, it has a variety of exceptions.
* [46190](https://bugzilla.xamarin.com/show_bug.cgi?id=46190):
    Overload resolution fails in a case where methods use a named parameter in different positions
* [46250](https://bugzilla.xamarin.com/show_bug.cgi?id=46250):
    Type.GetType with throwOnError true doesn't throw for a generic instance type with too few generic arguments
* [46602](https://bugzilla.xamarin.com/show_bug.cgi?id=46602):
    MobileAuthenticatedStream.AuthenticateAsServer() via EndPointListener
* [46712](https://bugzilla.xamarin.com/show_bug.cgi?id=46712):
    btls fails to build with gcc is v4.4.7 or earlier as they lack alignof/alignas
* [47205](https://bugzilla.xamarin.com/show_bug.cgi?id=47205):
    Uri.TryCreate throws exception
* [47353](https://bugzilla.xamarin.com/show_bug.cgi?id=47353):
    Mono.CSharp.MetadataImporter.set_IgnoreCompilerGeneratedField not found when running Cake on Mono 4.8
* [48016](https://bugzilla.xamarin.com/show_bug.cgi?id=48016):
    System.Net.NetworkInformation.DnsAddresses is always empty. Fix included.
* [48516](https://bugzilla.xamarin.com/show_bug.cgi?id=48516):
    ZipArchive.Save attempts to set position and seek non-seekable streams
* [49056](https://bugzilla.xamarin.com/show_bug.cgi?id=49056):
    Assertion at /Users/builder/data/lanes/3969/44931ae8/source/xamarin-macios/external/mono/mono/mini/mini-generic-sharing.c:2351, condition `info' not met
* [49686](https://bugzilla.xamarin.com/show_bug.cgi?id=49686):
    System.NotImplementedException at System.Reflection.Emit.DynamicMethod.GetCustomAttributes (System.Type attributeType, Boolean inherit)
* [50242](https://bugzilla.xamarin.com/show_bug.cgi?id=50242):
    Cannot use MSXSL format-date/format-time XPath extension functions on non-Windows platforms
* [51562](https://bugzilla.xamarin.com/show_bug.cgi?id=51562):
    NullReferenceException in BTLS X509CertificateImplBtls.Import()
* [51805](https://bugzilla.xamarin.com/show_bug.cgi?id=51805):
    [iOS]error MT6002: Could not strip assembly System.Net.Http.Primitives.dll while building  ToDoAzure with Release|iPhone


<!-- Access Denied bugs:
* [27061](https://bugzilla.xamarin.com/show_bug.cgi?id=27061):
* [34498](https://bugzilla.xamarin.com/show_bug.cgi?id=34498):
* [34883](https://bugzilla.xamarin.com/show_bug.cgi?id=34883):
* [40860](https://bugzilla.xamarin.com/show_bug.cgi?id=40860):
* [41264](https://bugzilla.xamarin.com/show_bug.cgi?id=41264):
* [41290](https://bugzilla.xamarin.com/show_bug.cgi?id=41290):
* [41564](https://bugzilla.xamarin.com/show_bug.cgi?id=41564):
* [41644](https://bugzilla.xamarin.com/show_bug.cgi?id=41644):
* [41671](https://bugzilla.xamarin.com/show_bug.cgi?id=41671):
* [41724](https://bugzilla.xamarin.com/show_bug.cgi?id=41724):
* [41747](https://bugzilla.xamarin.com/show_bug.cgi?id=41747):
* [41947](https://bugzilla.xamarin.com/show_bug.cgi?id=41947):
* [41956](https://bugzilla.xamarin.com/show_bug.cgi?id=41956):
* [41961](https://bugzilla.xamarin.com/show_bug.cgi?id=41961):
* [42469](https://bugzilla.xamarin.com/show_bug.cgi?id=42469):
* [42903](https://bugzilla.xamarin.com/show_bug.cgi?id=42903):
* [42938](https://bugzilla.xamarin.com/show_bug.cgi?id=42938):
* [43658](https://bugzilla.xamarin.com/show_bug.cgi?id=43658):
* [44212](https://bugzilla.xamarin.com/show_bug.cgi?id=44212):
* [44757](https://bugzilla.xamarin.com/show_bug.cgi?id=44757):
* [45140](https://bugzilla.xamarin.com/show_bug.cgi?id=45140):
* [45223](https://bugzilla.xamarin.com/show_bug.cgi?id=45223):
* [45232](https://bugzilla.xamarin.com/show_bug.cgi?id=45232):
* [45369](https://bugzilla.xamarin.com/show_bug.cgi?id=45369):
* [45687](https://bugzilla.xamarin.com/show_bug.cgi?id=45687):
* [45847](https://bugzilla.xamarin.com/show_bug.cgi?id=45847):
* [46375](https://bugzilla.xamarin.com/show_bug.cgi?id=46375):
* [46479](https://bugzilla.xamarin.com/show_bug.cgi?id=46479):
* [46549](https://bugzilla.xamarin.com/show_bug.cgi?id=46549):
* [47064](https://bugzilla.xamarin.com/show_bug.cgi?id=47064):
* [47167](https://bugzilla.xamarin.com/show_bug.cgi?id=47167):
* [50117](https://bugzilla.xamarin.com/show_bug.cgi?id=50117):
* [51206](https://bugzilla.xamarin.com/show_bug.cgi?id=51206):
* [51336](https://bugzilla.xamarin.com/show_bug.cgi?id=51336):
* [51625](https://bugzilla.xamarin.com/show_bug.cgi?id=51625):
* [51636](https://bugzilla.xamarin.com/show_bug.cgi?id=51636):
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
* API Level 25 (vs. API Level 24):
    [Mono.Android.dll](level_25_diff/mono.android.dll)

