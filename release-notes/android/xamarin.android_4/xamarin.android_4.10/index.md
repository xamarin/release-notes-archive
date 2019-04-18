---
id: 90510E91-4B54-4A71-8DEC-A4318285C49D
title: "Xamarin.Android 4.10"
---

The Xamarin.Android 4.10 series provides a number of stability fixes and
improvements, and introduces [.NET Portable Class Libraries](http://msdn.microsoft.com/en-us/library/vstudio/gg597391.aspx) support.

In **Debug** builds, Xamarin.Android 4.10 also changes the default log
level of the Mono runtime to `info` (from nothing). This will
result in additional log messages printed to the Application Output panel or `adb logcat` within **Debug** builds.. This can be disabled by
adding an [environment](/guides/android/advanced_topics/environment)
file and adding a line containing:

<blockquote><pre>
MONO_LOG_LEVEL=</pre></blockquote>

 <a name="2"></a>


 <a name="Xamarin.Android_4.10.2"></a>


#  [Xamarin.Android 4.10.2](#Xamarin.Android_4.10.2)

## Bug fixes

-  Fixes an activation error that occurred after installing Android 19 when the target framework of the project was set to the 'Use Latest' setting
-  Fixes a crash that could occur when clearing the Android device log in VS2010.


## New Features

-  Toggle for switching between layout and source view in the Android designer in VS2013


 <a name="1"></a>


 <a name="Xamarin.Android_4.10.1"></a>


#  [Xamarin.Android 4.10.1](#Xamarin.Android_4.10.1)

## Visual Studio compatibility notes

-  The Xamarin.Android 4.10.1 Visual Studio extension is compatible with Xamarin.iOS for VS 1.8
-  **Older versions of the Visual Studio extensions may fail to update both extensions correctly.** If you have updated and are seeing error messages, please ensure you have Xamarin.iOS for VS 1.8 installed. Here's a  [direct link to Xamarin.iOS for VS 1.8](http://download.xamarin.com/MonoTouchforVisualStudio/Windows/Xamarin.iOS_Setup-1.8.365.0_signed.msi) .


## Portable Class Library support added

-  You can now select Xamarin.iOS and Xamarin.Android as target frameworks for Portable Class Libraries 
-  For more information, check out our new  [Portable Class Library document](http://docs.xamarin.com/guides/cross-platform/application_fundamentals/pcl/) . 


### Bug Fixes

-   [14129](https://bugzilla.xamarin.com/show_bug.cgi?id=14129) : SIGILL or SIGSEGV when executing on Krait CPUs. 
-   [15542](https://bugzilla.xamarin.com/show_bug.cgi?id=15542) : Default sample fails on pre-Honeycomb devices with a  `CloneNotSupportedException` . 


### Integrated Mono features/fixes

Based on [Mono 3.2.3](http://www.mono-project.com/Release_Notes_Mono_3.2#New_in_Mono_3.2.1) [commit 433017c0](https://github.com/mono/mono/commit/433017c01185739599deb2fd8293b015892452be).

 <a name="0"></a>


 <a name="Xamarin.Android_4.10.0"></a>


#  [Xamarin.Android 4.10.0](#Xamarin.Android_4.10.0)

### New Features

-  Visual Studio 2013 Support
-  Visual Studio changes:
-    
-  The device chooser dialog (which would appear from Debug > Start Debugging) has been removed. Use the Xamarin.Android toolbar (View > Toolbars > Xamarin.Android).
-  The Toolbar now includes simulators and attached devices. When selected, simulators will transition from  **A** (Available) to  **S** (Starting) to just then name when finished running.
-  Added  `Java.Interop.JavaLibraryReferenceAttribute.SourceUrl` property. 
-  Add  `FragmentManager.FindFragment*<T>()` utility methods. 
-  Add  `Java.Lang.Throwable.Class` property. 
-  Generate a warning if  `IJavaObject` is implemented without inheriting from  `Java.Lang.Object` . 
-  Java Binding project can import javadoc and generate .NET XML documentation with new  **Build action**  `JavaDocIndex` on the JavaDoc's  `index.html` . Note that this works only for standard default doclets. 
-   `AndroidEnvironment` files now can be embedded in Android libraries. They are automatically extracted at application build time. 
-  OpenGL ES 3.0 support added to OpenTK. 


### Known Issues

-  Packages built with Xamarin.Android 4.10.0 will not run on pre-Honeycomb Android devices. This will be fixed in 4.10.1.


### Bug fixes

-   [10948](https://bugzilla.xamarin.com/show_bug.cgi?id=10948) : Need to allow overriding Reference Assemblies path. 
-   [11179](https://bugzilla.xamarin.com/show_bug.cgi?id=11179) : BINDINGSGENERATOR unknown parameter type warnings need more context. 
-   [12739](https://bugzilla.xamarin.com/show_bug.cgi?id=12739) :  `System.IO.MemoryMappedFile` implementation nonfunctional (cannot p/invoke to  `getpagesize()` ). 
-   [12995](https://bugzilla.xamarin.com/show_bug.cgi?id=12995) : SIGSEGV in MonoIO sample. 
-   [13388](https://bugzilla.xamarin.com/show_bug.cgi?id=13388) : Support  `$(AndroidUseLastetPlatformSdk)` on Windows. 
-   [13480](https://bugzilla.xamarin.com/show_bug.cgi?id=13480) : Better disambiguiate string marshaling. 
-   [13741](https://bugzilla.xamarin.com/show_bug.cgi?id=13741) : Properly marshal null strings. 
-   [13858](https://bugzilla.xamarin.com/show_bug.cgi?id=13858) : SIGSEGV from Dalvik when the GC prematurely collects an object. 
-   [13861](https://bugzilla.xamarin.com/show_bug.cgi?id=13861) : Add linker script to handle  `IReadOnlyCollection` . 
-   [13926](https://bugzilla.xamarin.com/show_bug.cgi?id=13926) : NUnitLite text wrapping, output not readable. 
-   [14033](https://bugzilla.xamarin.com/show_bug.cgi?id=14033) : Cannot build Android project due to recursive activation. 
-   [14048](https://bugzilla.xamarin.com/show_bug.cgi?id=14048) : [VS] Application Icon missing - and no warning when publishing 
-   [14106](https://bugzilla.xamarin.com/show_bug.cgi?id=14106) : Add  `Assert.Throws<T>()` /etc. to  `Xamarin.Android.NUnitLite.dll` . 
-   [14316](https://bugzilla.xamarin.com/show_bug.cgi?id=14316) :  `System.Data.Services.Client.DataServiceContext` doesn't work reliably when linker is enabled. 
-   [14210](https://bugzilla.xamarin.com/show_bug.cgi?id=14210) : Some  `GridLayout.Alignment` properties are not static or missing. 
-   [14255](https://bugzilla.xamarin.com/show_bug.cgi?id=14255) : App using Component with bundled resources fails to compile on Windows / VS. 
-   [14314](https://bugzilla.xamarin.com/show_bug.cgi?id=14314) : Trial Splash Screen Issue. 
-   [14436](https://bugzilla.xamarin.com/show_bug.cgi?id=14436) : Xamarin.Android.NUnitLite StackTrace goes out of the window (no scrolling bar). 
-   [14442](https://bugzilla.xamarin.com/show_bug.cgi?id=14442) : Xamarin.Android.NUnitLite "RunTests" button goes out of screen (no scrolling bar). 
-   [14542](https://bugzilla.xamarin.com/show_bug.cgi?id=14542) : Library projects should not have Trial resources embedded. 
-   [14677](https://bugzilla.xamarin.com/show_bug.cgi?id=14677) :  `javac` error when overriding  `AbsListView.Adapter` . 
-   [14820](https://bugzilla.xamarin.com/show_bug.cgi?id=14820) :  `NullReferenceException` when binding a  `.jar` file. 
-   [14942](https://bugzilla.xamarin.com/show_bug.cgi?id=14942) : debugger errors with "Incorrect number or types of arguments" on showing .ToString() of value type containing nested value types 
-   [14968](https://bugzilla.xamarin.com/show_bug.cgi?id=14968) : Proxy detection throws  `URISyntaxException` . 
-   [14999](https://bugzilla.xamarin.com/show_bug.cgi?id=14999) : Fix instance mapping. 
-   [15050](https://bugzilla.xamarin.com/show_bug.cgi?id=15050) : Don't die with a SIGSEGV when invoking methods on null Java methods. 
-   [15119](https://bugzilla.xamarin.com/show_bug.cgi?id=15119) : Build error uses wrong product name. 
-   [15129](https://bugzilla.xamarin.com/show_bug.cgi?id=15129) : GooglePlayServices'  `GooglePlayServicesUtil.GetErrorDialog` throws ResourceNotFound Exception. 
-   [15162](https://bugzilla.xamarin.com/show_bug.cgi?id=15162) : Rebuild solution rebuilds everything when Android Resources are used in Library projects. 
-   [15214](https://bugzilla.xamarin.com/show_bug.cgi?id=15214) : Retrieving System.Globalization Culture info returns Invariant info. 
-   [15297](https://bugzilla.xamarin.com/show_bug.cgi?id=15297) : expected return type 'L' calling  `Landroid/text/SpannableString;.getSpanFlags` . 
-   [15301](https://bugzilla.xamarin.com/show_bug.cgi?id=15301) : [VS] Devices do not show in the new device drop down. 


### Integrated Mono features/fixes

Based on [Mono 3.2.3](http://www.mono-project.com/Release_Notes_Mono_3.2#New_in_Mono_3.2.1) [commit a812e9a24](https://github.com/mono/mono/commit/a812e9a24b8550fa9d57442ab87225d9c34a60b7).

-   [1540](https://bugzilla.xamarin.com/show_bug.cgi?id=1540) : Debugger occasionally crashes on break. 
-   [4668](https://bugzilla.xamarin.com/show_bug.cgi?id=4668) : xsd does not handle defaults for decimal types correctly 
-   [6095](https://bugzilla.xamarin.com/show_bug.cgi?id=6095) : Flawed  `BlockingCollection(T).TakeFromAny` Implementation - Only Blocks On First Collection 
-   [7126](https://bugzilla.xamarin.com/show_bug.cgi?id=7126) : Violating the rules of  `AssemblyBuilderAccess.Save` results in assertion failure 
-   [7829](https://bugzilla.xamarin.com/show_bug.cgi?id=7829) :  `DynamicILInfo.GetTokenFor()` throws  `InvalidCastException` for Constructor. 
-   [8637](https://bugzilla.xamarin.com/show_bug.cgi?id=8637) :  `XDocument` doesn't honor  `XDeclaration.Encoding` . 
-   [8719](https://bugzilla.xamarin.com/show_bug.cgi?id=8719) : User-Agent parsing incorrectly via  `ProductInfoHeaderValue` in  `System.Net.Http.HttpRequestMessage` . 
-   [10001](https://bugzilla.xamarin.com/show_bug.cgi?id=10001) : Bug in  `HttpResponse.TransmitFile` involving Chuncked transfer encoding. 
-   [10194](https://bugzilla.xamarin.com/show_bug.cgi?id=10194) :  `XElement.SetElementValue` doesn't handle the case where the element doesn't exist AND value == null. 
-   [10782](https://bugzilla.xamarin.com/show_bug.cgi?id=10782) : Step out and step in steps over outside call. 
-   [11294](https://bugzilla.xamarin.com/show_bug.cgi?id=11294) : Mono ignores  `TypeForwardedFrom` when serializing. 
-   [11298](https://bugzilla.xamarin.com/show_bug.cgi?id=11298) :  `XElement.ReplaceAttributes` acts incorrectly. 
-   [11910](https://bugzilla.xamarin.com/show_bug.cgi?id=11910) :  `XmlConvert.VerifyXmlChars` throws  `NotImplementedException` . 
-   [12035](https://bugzilla.xamarin.com/show_bug.cgi?id=12035) :  `XmlSchema` error with inheritance and nillable elements. 
-   [12469](https://bugzilla.xamarin.com/show_bug.cgi?id=12469) : Processing of atomic datatypes in XML schema not working. 
-   [12640](https://bugzilla.xamarin.com/show_bug.cgi?id=12640) : Switch from Wifi with Proxy > 3G causes issue, as does 3G > Proxy. 
-   [12745](https://bugzilla.xamarin.com/show_bug.cgi?id=12745) :  `TaskAwaiter.GetResult()` throws an exception if the task hasn't completed. 
-   [12777](https://bugzilla.xamarin.com/show_bug.cgi?id=12777) :  `FileStream.BeginWrite` maxing out CPU with no progress on second callr 
-   [13110](https://bugzilla.xamarin.com/show_bug.cgi?id=13110) :  `StructuralComparisons.StructuralEqualityComparer` doesn't compare array of integers correctly. 
-   [13200](https://bugzilla.xamarin.com/show_bug.cgi?id=13200) :  `System.Net.Http.HttpClient` Timeout seems to be ignored. 
-   [13318](https://bugzilla.xamarin.com/show_bug.cgi?id=13318) :  `Task.Delay` hangs with custom  `TaskScheduler` . 
-   [13336](https://bugzilla.xamarin.com/show_bug.cgi?id=13336) : Default value of indexer parameter is not read. 
-   [13435](https://bugzilla.xamarin.com/show_bug.cgi?id=13435) : SIGSEGV instead of  `CustomAttributeFormatException` . 
-   [13485](https://bugzilla.xamarin.com/show_bug.cgi?id=13485) :  `DataContractJsonSerializer` Does Not Deserialize Private Properties. 
-   [13501](https://bugzilla.xamarin.com/show_bug.cgi?id=13501) : Pragma header parsing incorrectly on  `HttpResponseHeaders` . 
-   [13552](https://bugzilla.xamarin.com/show_bug.cgi?id=13552) : Memory leak in  `CyclicDeque` class when growing. 
-   [13626](https://bugzilla.xamarin.com/show_bug.cgi?id=13626) :  `System.Reflection.RuntimeReflectionExtensions` wrong content all methods. 
-   [13716](https://bugzilla.xamarin.com/show_bug.cgi?id=13716) :  `XmlResolver` (via  `XmlReaderSettings` ) is not invoked. 
-   [13742](https://bugzilla.xamarin.com/show_bug.cgi?id=13742) :  `SynchronizationContext.SetWaitNotificationRequired` not implemented. 
-   [13767](https://bugzilla.xamarin.com/show_bug.cgi?id=13767) : Assertion: should not be reached at  `class.c:6253` . 
-   [13813](https://bugzilla.xamarin.com/show_bug.cgi?id=13813) : Mono crashes when AppDomains are created in parallel (few). 
-   [13817](https://bugzilla.xamarin.com/show_bug.cgi?id=13817) :  `BindingFlags.OptionalParamBinding` behaves differently to .NET. 
-   [13927](https://bugzilla.xamarin.com/show_bug.cgi?id=13927) : Wrong result of double cast conversion. 
-   [13951](https://bugzilla.xamarin.com/show_bug.cgi?id=13951) : Threads stuck in suspend state with sgen on stack. 
-   [13953](https://bugzilla.xamarin.com/show_bug.cgi?id=13953) :  `RSACryptoServiceProvider.SignData()` doesn't support OID providers. 
-   [13970](https://bugzilla.xamarin.com/show_bug.cgi?id=13970) :  `Guid.Parse` does not throw  `FormatException<code> when missing single trailing char in segment. </li> <li> <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=14032" target="_blank">14032</a>: Closing <code>GZipStream` raises  `ObjectDisposedException` . 
-   [14058](https://bugzilla.xamarin.com/show_bug.cgi?id=14058) : Assertion at  `debugger-agent.c:5101` , condition  ``tls->context.valid'` not met. 
-   [14069](https://bugzilla.xamarin.com/show_bug.cgi?id=14069) :  `NullReferenceException` thrown when calling a callback from an Interop (signature decorated with InAttribute). 
-   [14073](https://bugzilla.xamarin.com/show_bug.cgi?id=14073) : Mono hangs running mono/tests/gsharing-valuetype-layout.exe. 
-   [14077](https://bugzilla.xamarin.com/show_bug.cgi?id=14077) :  `HashSet` capacity increases on every deserialization. 
-   [14168](https://bugzilla.xamarin.com/show_bug.cgi?id=14168) :  `TypeInfo` is not correct for a generic type. 
-   [14185](https://bugzilla.xamarin.com/show_bug.cgi?id=14185) : Swedish  `CultureInfo` has incorrect negative number sign. 
-   [14339](https://bugzilla.xamarin.com/show_bug.cgi?id=14339) : SGEN: Assertion: should not be reached at  `sgen-scan-object.h:111` . 
-   [14515](https://bugzilla.xamarin.com/show_bug.cgi?id=14515) :  `ParallelEnumerable.Range()` yields incorrect values when "start" parameter &gt; 1. 
-   [14585](https://bugzilla.xamarin.com/show_bug.cgi?id=14585) : Incorrect  `Task.WhenAny()` behavior with  `Task.Delay` . 
-   [14632](https://bugzilla.xamarin.com/show_bug.cgi?id=14632) :  `Array.FindLastIndex` is not equal to .NET Array.FindLastIndex. 
-   [14644](https://bugzilla.xamarin.com/show_bug.cgi?id=14644) : Simultaneous web requests. 
-   [14783](https://bugzilla.xamarin.com/show_bug.cgi?id=14783) :  `HttpClient` fails on result 302. 
-   [14824](https://bugzilla.xamarin.com/show_bug.cgi?id=14824) :  `AggregateException.GetBaseException` differs in Mono and .net 4.5. 
-   [14834](https://bugzilla.xamarin.com/show_bug.cgi?id=14834) : SIGSEGV in mono-sgen caused by __GNU_C__ optimization of OBJ_BITMAP_FOREACH_PTR (__builtin_ctz). 
-   [14839](https://bugzilla.xamarin.com/show_bug.cgi?id=14839) :  `TaskFactory.ContinueWhenAny` is broken. 
-   [14951](https://bugzilla.xamarin.com/show_bug.cgi?id=14951) :  `System.Text.Encoding` for ISO-2022-JP is broken. 
-   [15036](https://bugzilla.xamarin.com/show_bug.cgi?id=15036) : Entire  `Task.ContinueWith` chains remain kept alive by final reference. 
-   [15169](https://bugzilla.xamarin.com/show_bug.cgi?id=15169) :  `DataContractJsonSerializer` doesn't support deserializing relative Uris. 
-   [15289](https://bugzilla.xamarin.com/show_bug.cgi?id=15289) :  `IConvertibale` interface method error. 


 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.10/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.10/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.10/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.10/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.10/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.10/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.10/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.10/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.10/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.10/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.10/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.10/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.10/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.10/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.10/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.10/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.10/level_17_diff/opentk-1.0.dll)
