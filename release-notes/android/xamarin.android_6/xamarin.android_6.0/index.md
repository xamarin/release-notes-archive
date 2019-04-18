---
id: 185470A2-8137-44BA-9276-A8DF4F00C732
title: "Xamarin.Android 6.0"
---

Xamarin.Android 6.0 fixes numerous bugs and provides a binding for
[Android 6.0 Marshmallow][api-23].

[api-23]: https://developer.android.com/about/versions/marshmallow/android-6.0.html

**Note:** Xamarin.Android 6.0 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21+.
JDK 1.6 may be used when targeting previous API levels.

***Note:***
Due to a change by Google,
[Android N will now only permit linking to NDK-provided native libraries][ndk].
`libsqlite.so` is *not* an NDK-provided native library. Consequently,
existing apps using e.g. `Mono.Data.Sqlite.dll` *will* ***crash*** when
running on Android N. This may include other SQLite-using assemblies,
not distributed with Xamarin.Android.

[ndk]: http://developer.android.com/preview/behavior-changes.html#ndk

Xamarin.Android 6.0.4 ("C6SR4")
[updates `Mono.Data.Sqlite.dll`](#mono-data-sqlite) to include
a custom built version of `libsqlite.so`, named `libsqlite3_xamarin.so`.

**All Developers** need to audit their code for P/Invoke use and ensure that
referenced native libraries are either included in the Android NDK, or are
included within the `app.apk` itself. The only Xamarin.Android-provided
assembly impacted by this change is `Mono.Data.Sqlite.dll`.

<!--
  JONP: 6.0.4 last updated from commit monodroid/cycle6-c6sr4/ee215fc923a4650cfa49d4f38ff175c7441f8281
-->

<a name="4"/>
<a name="Xamarin.Android_6.0.4"/>
# Xamarin.Android 6.0.4

Xamarin.Android 6.0.4 fixes `Mono.Data.Sqlite.dll` for use on Android N.

<a name="new-features-6.0.4" />
## New Features

* [`Mono.Data.Sqlite.dll` bundles SQLite](#mono-data-sqlite)


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

<a name="integrated-mono-6.0.4" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)
[commit 7e2027e0](https://github.com/mono/mono/commit/7e2027e0e193b805b80d68285a22a3eaca67066d).

* [38161](https://bugzilla.xamarin.com/show_bug.cgi?id=38161):
    Instability/crash when using DateTime under cpu load


<!--
  JONP: 6.0.3 last updated from commit monodroid/cycle6-c6sr3/a94a03b5137c76552d675bed85203fa4b7a24955
-->

<a name="3"/>
<a name="Xamarin.Android_6.0.3"/>
# Xamarin.Android 6.0.3

<a name="new-features-6.0.3" />
## New Features

* Visual Studio Community Edition is now supported.
* All editions may now make use of these features which were previously restricted:

    * Command-line builds, including headless builds
    * All types and assemblies may now be used, including System.Data.SqlClient
    * P/Invoke
    * Java interop, including .jar binding assemblies
    * No more application size limits

* Removed the splash screen which was shown at launch for apps built with Trial edition.


<!--
  JONP: 6.0.2 last updated from commit monodroid/cycle6/46c3f7e0ec393c8caefb78b83612fde09170c88d
-->

<a name="2"/>
<a name="Xamarin.Android_6.0.2"/>
# Xamarin.Android 6.0.2

This is a bug-fix release.


<a name="Bug_Fixes_6.0.2"/>
## Bug Fixes

* [36036](https://bugzilla.xamarin.com/show_bug.cgi?id=36036):
    error MSB4018: The `GenerateJavaStubs` task failed unexpectedly, error MSB4018: System.InvalidOperationException: Sequence contains no matching element
* [37422](https://bugzilla.xamarin.com/show_bug.cgi?id=37422):
    Release Build Still Creates `.__override__` Directory

<a name="integrated-mono-6.0.2" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)
[commit d9d3a13c](https://github.com/mono/mono/commit/d9d3a13cdd4884a4f4e7842b101ed1b4ab6ce9c2).

* [38012](https://bugzilla.xamarin.com/show_bug.cgi?id=38012):
    Using Task's under memory pressure leads to unexpected crashes inside the TPL on iOS


<!--
  JONP: 6.0.1 last updated from commit monodroid/cycle6-c6sr1/e98e96277d8262dc1ce44c60e504de03eb15357d
-->

<a name="1"/>
<a name="Xamarin.Android_6.0.1"/>
# Xamarin.Android 6.0.1

<a name="new-features-6.0.1" />
## New Features

* `${applicationId}` may now be used within `AndroidManifest.xml` -- or any
    custom attributes that contribute to `AndroidManifest.xml` -- and will be
    replaced with the value of the `/manifest/@package` attribute value.

<a name="Bug_Fixes_6.0.1"/>
## Bug Fixes

* Fix Proguard config file generation issue which would prevent the GC from working.
* Fix `NullReferenceException` when linking because a custom attribute constructor has
    a `null` value for a `Type[]` parameter.
* Fix **@(LinkDescription)** processing so that when
    `/linker/assembly/type[@fullname='*']`, *all* types in the specified
    assembly are preserved, not just "toplevel" types. (Previously, nested
    types would still be linked away, contrary to all expectations.)
* [33514](https://bugzilla.xamarin.com/show_bug.cgi?id=33514):
    Add additional properties to `IntentFilterAttribute`.
* [34076](https://bugzilla.xamarin.com/show_bug.cgi?id=34076):
    `JavaCollection.CopyTo()` throws an `ArgumentException`.
* [34562](https://bugzilla.xamarin.com/show_bug.cgi?id=34562):
    Fix Visual Studio hang when installing NuGet packages.
* [34888](https://bugzilla.xamarin.com/show_bug.cgi?id=34888):
    Install all Facade assemblies on OS X.
* [36185](https://bugzilla.xamarin.com/show_bug.cgi?id=36185):
    Visual Studio may freeze when opening a solution as we download
    assembly dependencies.
* [36250](https://bugzilla.xamarin.com/show_bug.cgi?id=36250):
    Preserve constructors of CollectionDataContract nested types.

<a name="integrated-mono-6.0.1" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)
[commit 996df3cb](https://github.com/mono/mono/commit/996df3cb3b06afacf75adabfc63223b3e2471498).

* [20186](https://bugzilla.xamarin.com/show_bug.cgi?id=20186):
    Make sure ptr-to-structure and structure-to-ptr wrappers are unique for AOT.
* [30018](https://bugzilla.xamarin.com/show_bug.cgi?id=30018):
    Use &quot;Dns.GetHostEntry&quot; or &quot;Dns.GetHostByName&quot;,sometime throw error &quot;Cannot handle address family xxxxx&quot;
* [31432](https://bugzilla.xamarin.com/show_bug.cgi?id=31432):
    Fix `TimeZoneInfo.ParseTZBuffer()` abbreviations.
* [35545](https://bugzilla.xamarin.com/show_bug.cgi?id=35545):
    Mono cannot marshal a parameter that is a function pointer which takes a function pointer as a parameter
* [35828](https://bugzilla.xamarin.com/show_bug.cgi?id=35828):
    `Thread.CurrentThread` doesn't return correct object in appdomain
* [35857](https://bugzilla.xamarin.com/show_bug.cgi?id=35857):
    `NullReferenceException` in SqlDataReader.GetValues()
* [36100](https://bugzilla.xamarin.com/show_bug.cgi?id=36100):
    `DataContractSerializer` broke in XI 9.2.1.51 STABLE
* [36256](https://bugzilla.xamarin.com/show_bug.cgi?id=36256):
    Memory leak related to `KDTree.FromData&lt;int&gt;(points, distance):
* [36292](https://bugzilla.xamarin.com/show_bug.cgi?id=36292):
    Assignment operator (`+=`, `++`, etc.) on generic items crashes with `System.InvalidProgramException: Invalid IL code`
* [36383](https://bugzilla.xamarin.com/show_bug.cgi?id=36383):
    async / await - Custom awaiter crashing on device
* [36414](https://bugzilla.xamarin.com/show_bug.cgi?id=36414):
    [Mono 4.2 Regression]: `ThreadPool.SetMinThreads()` and `ThreadPool.GetAvailableThreads()` don't works as expected
* [36418](https://bugzilla.xamarin.com/show_bug.cgi?id=36418):
    GetProperty fails for indexer properties on instantiations of generic types
* [36436](https://bugzilla.xamarin.com/show_bug.cgi?id=36436):
    `XslCompiledTransform` causes hang during execution
* [36646](https://bugzilla.xamarin.com/show_bug.cgi?id=36646):
    `Delegate.Remove()` for combined delegate works different from Microsoft .Net
* [37171](https://bugzilla.xamarin.com/show_bug.cgi?id=37171):
    `DataContractSerializer` does not handle `ISerializable` at all


<!--
  JONP: 6.0.0 last updated from commit monodroid/cycle6/81fb408b0b4cd19c205f03ef327898ab2f026372
-->

<a name="0"/>
<a name="Xamarin.Android_6.0.0"/>
# Xamarin.Android 6.0

<a name="new-features-6.0" />
## New Features

* [Build system improvements](#Build_Improvements).
* [Add Mono.Posix.dll](#Add_Mono.Posix.dll).
* [Reduce generation of `NoClassDefFoundError` exceptions](#Reduced_NoClassDefFoundError_Generation).
* OpenTK Includes OpenGLES 2.0 API Extensions
* WCF assemblies (`System.ServiceModel*.dll`) are no longer restricted assemblies. All editions may use it.

<a name="Build_Improvements" />
### Build Improvements

The Xamarin.Android Build system has been reviewed to avoid executing
MSBuild targets more than is necessary.

<!--
    https://docs.google.com/spreadsheets/d/1ebYO-nrgJMWk1cfjWZUF2QpPrKYZTLv1IggSEpb4c3k/edit#gid=0
-->
<table>
    <tr>
        <th>Sample</th><th>5.1.4 Rebuild Time</th><th>5.1.99 Rebuild Time</th><th>Improvement</th>
    </tr>
    <tr>
        <td>
            <a href="https://github.com/xamarin/mobile-samples/tree/master/TipCalc/TipCalc.UI.Android">
                TipCalc.UI.Android
            </a>
        </td>
        <td>11.278727s</td>
        <td>1.892669s</td>
        <td>-9.386058s</td>
    </tr>
    <tr>
        <td>
            <a href="https://github.com/xamarin/monodroid-samples/tree/master/UrbanAirship/samples/PushSample">
                UrbanAirship PushSample
            </a>
        </td>
        <td>4.315072</td>
        <td>1.2243065</td>
        <td>-3.0907655</td>
    </tr>
    <tr>
        <td>
            <a href="https://github.com/xamarin/xamarin-forms-samples/tree/master/ScaleAndRotate">
                Xamarin.Forms ScaleAndRotate
            </a>
        </td>
        <td>9.3481605</td>
        <td>1.445299</td>
        <td>-7.9028615</td>
    </tr>
    <tr>
        <td>
            <i>Large proprietary application</i>
        </td>
        <td>97.479729</td>
        <td>25.099358</td>
        <td>-72.380371</td>
    </tr>
</table>

Changing build options will now consistently cause build outputs to be
rebuilt.

When using Visual Studio, MSBuild, or `xbuild`, a new
`$(InstallDependsOnTargets)` MSBuild property can now be overridden
to perform pre- and post-Install actions.
([Bug #16553](https://bugzilla.xamarin.com/show_bug.cgi?id=16553))


<a name="Add_Mono.Posix.dll" />
### Add Mono.Posix.dll

A version of `Mono.Posix.dll` (without the obsolete `Mono.Posix` namespace)
is now included, providing access to the [`Mono.Unix`](ns-mono-unix) and
[`Mono.Unix.Native`](ns-mono-unix-native) namespaces.

[ns-mono-unix]: http://docs.go-mono.com/?link=N%3aMono.Unix
[ns-mono-unix-native]: http://docs.go-mono.com/?link=N%3aMono.Unix.Native

*Note*: Android does not support Unix Real-time signals on
many architectures. Attempting to use them may result throwing
a `NotSupportedException`.

<a name="Reduced_NoClassDefFoundError_Generation" />
### Reduced `NoClassDefFoundError` Generation.

In order to avoid extra `NoClassDefFoundError` generation, and to support
properly looking up Java types located in assemblies other than
`Mono.Android.dll`, the packaging process now generates a mapping between
all bound Java types and their corresponding wrappers. This should reduce
the need to use the `.JavaCast<T>()` extension method.
([Bug #7459](https://bugzilla.xamarin.com/show_bug.cgi?id=7459))

Note, however, that this only works for *bound* types. If a Java method
returns e.g. an interface type, and the implementation returns a non-public
or otherwise unbound type, then the previous behavior of following an
algorithmically determined "best matching wrapper" is used.


<a name="Known_Issues" />
## Known Issues

<a name="Proguard_Broken" />
We have recently discovered that enabling **Proguard** will *break* the GC,
resulting in all manner of "weird" bugs. Proguard support will be fixed in
a future release.

<a name="Bug_Fixes"/>
## Bug Fixes

* [1969](https://bugzilla.xamarin.com/show_bug.cgi?id=1969):
    `System.Net.NetworkInformation.GetAllNetworkInterfaces()` fails.
* [18824](https://bugzilla.xamarin.com/show_bug.cgi?id=18824):
    For certain projects, setting the linker mode to a value other than "None"
    leads to incorrect line numbers when debugging
* [23771](https://bugzilla.xamarin.com/show_bug.cgi?id=23771):
    UTF8 Decoder's Convert does not keep internal state between calls when
    `flush` parameter is false
* [28538](https://bugzilla.xamarin.com/show_bug.cgi?id=28538):
    Android application crashed as soon as it launches on device/Emulator
* [28565](https://bugzilla.xamarin.com/show_bug.cgi?id=28565):
    `ClassNotFoundException` when instantiating `LayerDrawable`.
* [28789](https://bugzilla.xamarin.com/show_bug.cgi?id=28789):
    Generic fragments throw `TypeLoadException`.
    (Now they instead throw `NotSupportedException`.)
* [31497](https://bugzilla.xamarin.com/show_bug.cgi?id=31497):
    Multiple re-downloads of the same package.
* [31527](https://bugzilla.xamarin.com/show_bug.cgi?id=31527):
    Unable to load file or assembly 'System.Runtime' in project with both
    shared runtime and Link SDK enabled
* [31875](https://bugzilla.xamarin.com/show_bug.cgi?id=31875):
    `as` invocation fails if `dos2unix` is in `%PATH%`.
* [32418](https://bugzilla.xamarin.com/show_bug.cgi?id=32418):
    Need MSBuild output when downloading maven zip files and unzipping.
* [32696](https://bugzilla.xamarin.com/show_bug.cgi?id=32696):
    Android XML Resource reader tries to read extra attributes.
* [33305](https://bugzilla.xamarin.com/show_bug.cgi?id=33305):
    Exceptions thrown from void-returning `async` methods don't contain
    the full stack trace.
* [33349](https://bugzilla.xamarin.com/show_bug.cgi?id=33349):
    LinkAssemblies error from VS2015 compiled assemblies containing nested types.
* [33554](https://bugzilla.xamarin.com/show_bug.cgi?id=33554):
    monodroid error XA0000: Reason: An element with the same key already exists in the dictionary
* [34139](https://bugzilla.xamarin.com/show_bug.cgi?id=34139):
    GZipStream (DeflateStreamNative) native exception after Flush() with no buffer data: Internal error (no progress possible) Flush
* [34391](https://bugzilla.xamarin.com/show_bug.cgi?id=34391):
    System.DllNotFoundException: sqlcipher
* [34548](https://bugzilla.xamarin.com/show_bug.cgi?id=34548):
    Broken dependency chain when embedding wear applications


<a name="integrated-mono" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)
[commit 6dd2d0d5](https://github.com/mono/mono/commit/6dd2d0d52b8bc4262d67833f44bc1537c3d17a9e).

* [1856](https://bugzilla.xamarin.com/show_bug.cgi?id=1856):
    Wrong stack trace when exception is re-thrown
* [2917](https://bugzilla.xamarin.com/show_bug.cgi?id=2917):
    `XslCompiledTransform.Load()` ignoring `xsl:output` properties
* [4148](https://bugzilla.xamarin.com/show_bug.cgi?id=4148):
    `JavaScriptSerializer` invalid JSON primitive
* [10268](https://bugzilla.xamarin.com/show_bug.cgi?id=10268):
    Linker issue with horizontallistview project in release mode
* [16475](https://bugzilla.xamarin.com/show_bug.cgi?id=16475):
    Method not found: `System.Web.Routing.RouteCollection.get_AppendTrailingSlash`
* [17817](https://bugzilla.xamarin.com/show_bug.cgi?id=17817):
    `Convert.ToUInt64()` with base 10 does not check range
* [18171](https://bugzilla.xamarin.com/show_bug.cgi?id=18171):
    `XElement` implements `IXmlSerializable`, but lacks parameterless
    constructor, and has incorrect `QName` in `KnownTypeCollection`
* [18558](https://bugzilla.xamarin.com/show_bug.cgi?id=18558):
    XML Serializer does not match .NET behavior when using subclasses with
    multiple `XmlElement` tags
* [19334](https://bugzilla.xamarin.com/show_bug.cgi?id=19334):
    `BeginWrite` failure at `System.Net.Sockets.NetworkStream.BeginWrite`
* [19697](https://bugzilla.xamarin.com/show_bug.cgi?id=19697):
    WCF SendTimeout not working in Xamarin
* [19823](https://bugzilla.xamarin.com/show_bug.cgi?id=19823):
    `InvalidOperationException` in `ServicePoint.RemoveConnectionGroup()`
* [20048](https://bugzilla.xamarin.com/show_bug.cgi?id=20048):
    Socket ctor missing
* [20764](https://bugzilla.xamarin.com/show_bug.cgi?id=20764):
    `WebMessageFormatter` crashes with void return type OperationContract
* [21810](https://bugzilla.xamarin.com/show_bug.cgi?id=21810):
    Method not implemented `System.Web.HttpApplication.RegisterModule`
* [23119](https://bugzilla.xamarin.com/show_bug.cgi?id=23119):
    Remove npgsql from mono (or at least update)
* [24086](https://bugzilla.xamarin.com/show_bug.cgi?id=24086):
    Runtime test - TestDaylightSavingsTime fails against Asia/Amman for 2012 DateTimes
* [24647](https://bugzilla.xamarin.com/show_bug.cgi?id=24647):
    `ExceptionDispatchInfo::Throw()` does not replace capture stack trace
* [25717](https://bugzilla.xamarin.com/show_bug.cgi?id=25717):
    Calling a created delegate for value type fails in Mono but works in Windows
* [26205](https://bugzilla.xamarin.com/show_bug.cgi?id=26205):
    `System.IO.Package.LoadRelationships()` throws null reference for some
    NuGet packages with PCLs generated on Windows
* [26362](https://bugzilla.xamarin.com/show_bug.cgi?id=26362):
    [Process] Exited event raised while process still running
* [26546](https://bugzilla.xamarin.com/show_bug.cgi?id=26546):
    Issue when using null value for integer and datetime in `SqlParameter`
* [26858](https://bugzilla.xamarin.com/show_bug.cgi?id=26858):
    `HttpListener`s scheme parser is case sensitive
* [26998](https://bugzilla.xamarin.com/show_bug.cgi?id=26998):
    Issue with `DataContractJsonSerializer` - Deserialize type incorrect on iOS
* [27348](https://bugzilla.xamarin.com/show_bug.cgi?id=27348):
    Deadlock in `WebConnectionGroup.Close()` / `WebConnection.Close()`
* [27352](https://bugzilla.xamarin.com/show_bug.cgi?id=27352):
    `HttpRequestMessage`: adding Accept header with multiple values fails
* [27386](https://bugzilla.xamarin.com/show_bug.cgi?id=27386):
    `HttpClient` doesn't honor `BaseAddress` with the `Get*Async()` methods
* [27614](https://bugzilla.xamarin.com/show_bug.cgi?id=27614):
    Native interop: out `LPArray`s cause crash
* [27697](https://bugzilla.xamarin.com/show_bug.cgi?id=27697):
    Debugger crash: error: `* Assertion at ../../../../../mono/mono/mini/debugger-agent.c:2475, condition `tls' not met``
* [27725](https://bugzilla.xamarin.com/show_bug.cgi?id=27725):
    Missing day names in ar-EG culture
* [27982](https://bugzilla.xamarin.com/show_bug.cgi?id=27982):
    Inconsistent behavior in `DynamicAttribute.Equals()` method
* [28014](https://bugzilla.xamarin.com/show_bug.cgi?id=28014):
    Type is not serializable with a type-forwarded `SerializableAttribute`
* [28181](https://bugzilla.xamarin.com/show_bug.cgi?id=28181):
    `* Assertion: should not be reached at debugger-agent.c:5957`
* [28184](https://bugzilla.xamarin.com/show_bug.cgi?id=28184):
    `ParameterInfo.GetCustomAttributes()` returns `null` in some cases
* [28235](https://bugzilla.xamarin.com/show_bug.cgi?id=28235):
    `System.Type` change to reference source broke IronPython
* [28290](https://bugzilla.xamarin.com/show_bug.cgi?id=28290):
    `Marshal.AllocCoTaskMem()` does not throw `OutOfMemoryException`
    on alloc failure
* [28331](https://bugzilla.xamarin.com/show_bug.cgi?id=28331):
    Custom Attributes incompatability
* [28369](https://bugzilla.xamarin.com/show_bug.cgi?id=28369):
    mono runtime crash `assertion 'hash != NULL' failed`
* [28383](https://bugzilla.xamarin.com/show_bug.cgi?id=28383):
    `Marshal.AllocCoTaskMem(0)` incorrectly returns null
* [28398](https://bugzilla.xamarin.com/show_bug.cgi?id=28398):
    `* Assertion: should not be reached at class.c:6405`
* [28692](https://bugzilla.xamarin.com/show_bug.cgi?id=28692):
    `GetCustomAttributes()` seems to return attributes in a different order
    than in windows.
* [28777](https://bugzilla.xamarin.com/show_bug.cgi?id=28777):
    `GZipStream` (`DeflateStreamNative`) native exception after `Flush()` with
    no buffer data: Internal error (no progress possible) Flush
* [28793](https://bugzilla.xamarin.com/show_bug.cgi?id=28793):
    `SynchronizationContext.SetSynchronizationContext()` leaks back
    inappropriately into caller
* [28857](https://bugzilla.xamarin.com/show_bug.cgi?id=28857):
    Nursery-canaries and AOT causes assertion failure
* [28876](https://bugzilla.xamarin.com/show_bug.cgi?id=28876):
    Satellite assembly finder fails for memory-loaded assemblies with
    `GetDirectoryName()`: Invalid path
* [28961](https://bugzilla.xamarin.com/show_bug.cgi?id=28961):
    AOT error when upgrading to Unified API
* [29039](https://bugzilla.xamarin.com/show_bug.cgi?id=29039):
    `CultureInfo.GetCultures(CultureTypes.SpecificCultures)` returns broken
    ar-SA culture
* [29183](https://bugzilla.xamarin.com/show_bug.cgi?id=29183):
    Array constructor fails to construct multi bound array
* [29625](https://bugzilla.xamarin.com/show_bug.cgi?id=29625):
    Unable to extract certain archives using `ZipFile.ExtractToDirectory`
* [29667](https://bugzilla.xamarin.com/show_bug.cgi?id=29667):
    Mono v4.0 crashes after a while
* [29679](https://bugzilla.xamarin.com/show_bug.cgi?id=29679):
    Mono crashes with `Assertion at class.c:5748` when getting custom
    attributes from corefx contract assembly
* [29823](https://bugzilla.xamarin.com/show_bug.cgi?id=29823):
    4.0 Regression - `SqlConnectionBuilder` broken after migrating to
    System.Data reference source
* [29906](https://bugzilla.xamarin.com/show_bug.cgi?id=29906):
    Static method `TimeZoneInfo.GetSystemTimeZones()` is not thread safe.
* [29927](https://bugzilla.xamarin.com/show_bug.cgi?id=29927):
    Http Response doesn't UnescapeDataString
* [29970](https://bugzilla.xamarin.com/show_bug.cgi?id=29970):
    [MonoNativeFunctionWrapper] doesn't work with methods that return
    structures on 32bit device
* [30043](https://bugzilla.xamarin.com/show_bug.cgi?id=30043):
    Disposing a `FileSystemWatcher` object causes `ArgumentOutOfRangeException`
* [30171](https://bugzilla.xamarin.com/show_bug.cgi?id=30171):
    `BinaryReader.ReadChar()` returns incorrect result on 8.10
* [30502](https://bugzilla.xamarin.com/show_bug.cgi?id=30502):
    `AssemblyName.CultureName` implementation differs from .NET.
* [30551](https://bugzilla.xamarin.com/show_bug.cgi?id=30551):
    Potential race in do_rehash
* [30604](https://bugzilla.xamarin.com/show_bug.cgi?id=30604):
    HttpClient times out when redirected on a Post request
* [30617](https://bugzilla.xamarin.com/show_bug.cgi?id=30617):
    Stepping over foreach exits method
* [30698](https://bugzilla.xamarin.com/show_bug.cgi?id=30698):
    Build fails when building for device using --aot-options=-O=float32 and
    performing a calculation on float or nfloat variables
* [30741](https://bugzilla.xamarin.com/show_bug.cgi?id=30741):
    `MemoryMappedFiles` from reference source is causing segfaults
* [30825](https://bugzilla.xamarin.com/show_bug.cgi?id=30825):
    Null string to `mono_mmap_open_handle()` Regression between 4.1.0.1738 and 4.3.0.109
* [30851](https://bugzilla.xamarin.com/show_bug.cgi?id=30851):
    Incorrect (Swedish) date format since version 3.4.0
* [30868](https://bugzilla.xamarin.com/show_bug.cgi?id=30868):
    `ObjectDisposedException` in mono 4.0.1.28, but not mono 3.12.1
* [30869](https://bugzilla.xamarin.com/show_bug.cgi?id=30869):
    `HttpClient` authentication not working
* [30880](https://bugzilla.xamarin.com/show_bug.cgi?id=30880):
    IPv4Mask property produces a Not Implemented Exception
* [30897](https://bugzilla.xamarin.com/show_bug.cgi?id=30897):
    App crashes with Thai locale selected
* [30972](https://bugzilla.xamarin.com/show_bug.cgi?id=30972):
    `System.IO.Compression.ZipArchive` disregards provided encoding
* [31020](https://bugzilla.xamarin.com/show_bug.cgi?id=31020):
    Order of interfaces in `GetInterfaces()` is random
* [31231](https://bugzilla.xamarin.com/show_bug.cgi?id=31231):
    Crash with generics makeref
* [31336](https://bugzilla.xamarin.com/show_bug.cgi?id=31336):
    `HttpClient` adds comma in User-Agent
* [31398](https://bugzilla.xamarin.com/show_bug.cgi?id=31398):
    Cultures zh-Hans and zh-CHS are equal when they should not be
* [31451](https://bugzilla.xamarin.com/show_bug.cgi?id=31451):
    `mono_trace_set_printerr_handler()` calls `g_set_print_handler()` instead
    of `g_set_printerr_handler()`
* [31507](https://bugzilla.xamarin.com/show_bug.cgi?id=31507):
    `ObjectDisposedException` when canceling postAsync
* [31557](https://bugzilla.xamarin.com/show_bug.cgi?id=31557):
    Sockets with ReuseAddress does not seem to be working as expected
* [31635](https://bugzilla.xamarin.com/show_bug.cgi?id=31635):
    `UnixMarshal.PtrToString()` fails with UTF32Encoding
* [31877](https://bugzilla.xamarin.com/show_bug.cgi?id=31877):
    `SendChunked()` - &quot;Method must be implemented&quot;
* [31932](https://bugzilla.xamarin.com/show_bug.cgi?id=31932):
    Regression: Stack Overflow with native P/Invoke Callback
* [31996](https://bugzilla.xamarin.com/show_bug.cgi?id=31996):
    AOT compiler fails if path to project has a comma
* [32137](https://bugzilla.xamarin.com/show_bug.cgi?id=32137):
    `System.Text.Encoding.UTF8.EncodingName` not the returning human-readable
    description of the current encoding
* [32179](https://bugzilla.xamarin.com/show_bug.cgi?id=32179):
    Consistent crash in `mini-arm.c` when running FSharp on Raspberry Pi 2
* [32539](https://bugzilla.xamarin.com/show_bug.cgi?id=32539):
    `Process.ProcessName` value fetched using `Process.GetProcesses()` is
    trimmed to 15 characters
* [32579](https://bugzilla.xamarin.com/show_bug.cgi?id=32579):
    `System.Diagnostics.Process.MainModule.FileName` does not return full path
    of the executable and returns 15 chars trimmed value which is same as
    `Process.ProcessName`
* [32685](https://bugzilla.xamarin.com/show_bug.cgi?id=32685):
    `NullReferenceException` in `ServicePoint.CheckAvaliableForRecycling`
* [32815](https://bugzilla.xamarin.com/show_bug.cgi?id=32815):
    `PropertyInfo.Module` throws `System.NotImplementedException`
* [32886](https://bugzilla.xamarin.com/show_bug.cgi?id=32886):
    [Mono 3.12] Some WCF methods that do _not_ use `ref` parameters fail with
    `nvalidOperationException` during `ClientRuntimeChannel.EndProcess` when
    called via a ChannelFactory channel
* [32918](https://bugzilla.xamarin.com/show_bug.cgi?id=32918):
    StackTrace() missing original exception - ExceptionDispatchInfo
* [32931](https://bugzilla.xamarin.com/show_bug.cgi?id=32931):
    `NullReferenceException` in `KeyValuePair.get_Key` when using generic
    method and Linq
* [32955](https://bugzilla.xamarin.com/show_bug.cgi?id=32955):
    Random crash at aot-runtime.c:3144
* [33080](https://bugzilla.xamarin.com/show_bug.cgi?id=33080):
    JIT error only on ARMV7
* [33218](https://bugzilla.xamarin.com/show_bug.cgi?id=33218):
    Action ReflectedType differs from Delegate ReflectedType
* [33591](https://bugzilla.xamarin.com/show_bug.cgi?id=33591):
    AOT compilation fails with condition `field->type->attrs & FIELD_ATTRIBUTE_HAS_DEFAULT` not met
* [33723](https://bugzilla.xamarin.com/show_bug.cgi?id=33723):
    Null propagation operator produces incorrect IL
* [33754](https://bugzilla.xamarin.com/show_bug.cgi?id=33754):
    Invalid IL Code when using elvis operator to call extension struct methods
* [33952](https://bugzilla.xamarin.com/show_bug.cgi?id=33952):
    Debugger.Break() causes app to crash if Debugger is not attached,
* [34047](https://bugzilla.xamarin.com/show_bug.cgi?id=34047):
    `System.Globalization.CultureInfo.GetCultureInfo("es")` returns incorrect NumberFormatInfo.NumberGroupSeparator
* [34147](https://bugzilla.xamarin.com/show_bug.cgi?id=34147):
    Serious AOT bug
* [34334](https://bugzilla.xamarin.com/show_bug.cgi?id=34334):
    `System.NotImplementedException: The requested feature is not implemented` from
    `Microsoft.Scripting.Interpreter.EqualInstruction.Create (System.Type type)`
* [34604](https://bugzilla.xamarin.com/show_bug.cgi?id=34604):
    Compiler Crash in Mono.CSharp.CallEmitter.EmitPredefined with NRE
* [34750](https://bugzilla.xamarin.com/show_bug.cgi?id=34750):
    Debugger crash very often - `debugger-agent.c:2587, condition 'res' not met`
* [34926](https://bugzilla.xamarin.com/show_bug.cgi?id=34926):
    AOT issue with await Task&lt;bool&gt; on Visual Studio 2015


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

