---
id: 1AD2E208-90DD-4553-B315-D8B876B8628A
title: "Xamarin.Android 5.1.99"
---

The Xamarin.Android 5.1.99 is an alpha for Xamarin.Android 6.0,
which fixes numerous bugs and provides a binding for
[Android 6.0 Marshmallow][api-23].

[api-23]: https://developer.android.com/preview/api-overview.html

**Note:** Xamarin.Android 5.1.99 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21+.
JDK 1.6 may be used when targeting previous API levels.


<!--
  JONP: 5.1.99 last updated from commit monodroid/master/cfa43bb5755c0c9f203a8ce3dc0bdedc4bf9d3a1
-->

<a name="99"/>
<a name="Xamarin.Android_5.1.99"/>
# Xamarin.Android 5.1

<a name="new-features-5.1" />
## New Features

* [Build system improvements](#Build_Improvements).
* [Line numbers from stack traces in Release builds](#Line_Numbers_and_Release_Builds).
* [Add Mono.Posix.dll](#Add_Mono.Posix.dll).
* [Reduce generation of `NoClassDefFoundError` exceptions](#Reduced_NoClassDefFoundError_Generation).
* OpenTK Includes OpenGLES 2.0 API Extensions

<a name="Build_Improvements" />
### Build Improvements

The Xamarin.Android Build system has been reviewed to avoid executing
MSBuild targets more than is necessary.

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
</table>

TODO: Build time improvements.

Changing build options will now consistently cause build outputs to be
rebuilt.

When using Visual Studio, MSBuild, or `xbuild`, a new
`$(InstallDependsOnTargets)` MSBuild property can now be overridden
to perform pre- and post-Install actions.
([Bug #16553](https://bugzilla.xamarin.com/show_bug.cgi?id=16553))


<a name="Line_Numbers_and_Release_Builds" />
### Line Numbers and Release Builds

TODO: How's this work?

* [18137](https://bugzilla.xamarin.com/show_bug.cgi?id=18137):
    Release builds do not include file name/line number in exception stack traces

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
* [29731](https://bugzilla.xamarin.com/show_bug.cgi?id=29731):
    [XA 5.1] `Android.Bluetooth.BluetoothAdapter.Enable` is incorrectly marked as `[Obsolete("deprecated")]`
* [29757](https://bugzilla.xamarin.com/show_bug.cgi?id=29757):
    Resource overriding with aapt is FUBAR
* [30318](https://bugzilla.xamarin.com/show_bug.cgi?id=30318):
    Xamarin.Android Breakpoints in Forms PCL project do not work after cleaning
    solution, redeploying, and restarting debugging
* [31497](https://bugzilla.xamarin.com/show_bug.cgi?id=31497):
    Multiple re-downloads of the same package.
* [31527](https://bugzilla.xamarin.com/show_bug.cgi?id=31527):
    Unable to load file or assembly 'System.Runtime' in project with both
    shared runtime and Link SDK enabled
* [31705](https://bugzilla.xamarin.com/show_bug.cgi?id=31705):
    Embedded resources are not being fast deployed from the IDE in XA 5.1.4+.
* [31875](https://bugzilla.xamarin.com/show_bug.cgi?id=31875):
    `as` invocation fails if `dos2unix` is in `%PATH%`.
* [32418](https://bugzilla.xamarin.com/show_bug.cgi?id=32418):
    Need MSBuild output when downloading maven zip files and unzipping.
* [32696](https://bugzilla.xamarin.com/show_bug.cgi?id=32696):
    Android XML Resource reader tries to read extra attributes.
* [33305](https://bugzilla.xamarin.com/show_bug.cgi?id=33305):
    Exceptions thrown from void-returning `async` methods don't contain
    the full stack trace.


<a name="integrated-mono" />
## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)
[commit 9b990f2b](https://github.com/mono/mono/commit/9b990f2b19b1a534925cce3ddaabb70654b76066).

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
* [33080](https://bugzilla.xamarin.com/show_bug.cgi?id=33080):
    JIT error only on ARMV7

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
* API Level 23 (vs. API-22):
    [Mono.Android.dll](level_23_diff/mono.android.dll)

