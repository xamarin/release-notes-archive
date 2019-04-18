---
id: B79E3042-9730-4B75-B249-9D3B24C478F6
title: "Xamarin.Android 4.12"
---

The Xamarin.Android 4.12 series adds bindings for [Android 4.4 KitKat](http://www.android.com/versions/kit-kat-4-4/)
and adds some workarounds for the [ART 4.4.2](http://source.android.com/devices/tech/dalvik/art.html)
runtime.

 <a name="6"></a>


 <a name="Xamarin.Android_4.12.6"></a>


#  <a ref="#Xamarin.Android_4.12.6"></a>
Xamarin.Android 4.12.6

### Bug fixes

-   [20911](https://bugzilla.xamarin.com/show_bug.cgi?id=20911) Fixes a regression introduced by Android SDK Tools r23 and Android Build-tools r20 that changed the path of the zipalign tool. 


 <a name="5"></a>


 <a name="Xamarin.Android_4.12.5"></a>


#  <a ref="#Xamarin.Android_4.12.5">Xamarin.Android 4.12.5</a>


### Bug fixes

-   [19161](https://bugzilla.xamarin.com/show_bug.cgi?id=19161) : Fix InvalidCastException in System.Net.WebConnectionStream.WriteRequestAsyncCB 


 <a name="4"></a>


 <a name="Xamarin.Android_4.12.4"></a>


#  <a ref="#Xamarin.Android_4.12.4">Xamarin.Android 4.12.4</a>


### New Features



### Bug fixes

-   [18016](https://bugzilla.xamarin.com/show_bug.cgi?id=18016) : First app startup when using Renderscript may result in GC deadlock. 
-   [18757](https://bugzilla.xamarin.com/show_bug.cgi?id=18757) : Error MSB3375 when attempting to debug PCL in VS. 


### Integrated Mono features/fixes

Based on [Mono 3.4](http://www.mono-project.com/Release_Notes_Mono_3.4) (-ish) [commit fcf29c0e](https://github.com/mono/mono/commit/fcf29c0e2f969eb777445a6d20eb007af9452c97).

-   [4510](https://bugzilla.xamarin.com/show_bug.cgi?id=4510) :  `Marshal.SizeOf` returning wrong size. 
-   [5835](https://bugzilla.xamarin.com/show_bug.cgi?id=5835) : Runtime crash with: "null ResolutionScope not yet handled". 
-   [6843](https://bugzilla.xamarin.com/show_bug.cgi?id=6843) : Allow a TLS1.1+ client to fallback to TLS1.0 when using  `System.dll` / `Mono.Security.dll` for server side SSL/TLS. 
-   [12571](https://bugzilla.xamarin.com/show_bug.cgi?id=12571) : Usage of  `XElement` with  `XmlAnyElementAttribute` is not supported by  `XmlSerializer` . 
-   [13281](https://bugzilla.xamarin.com/show_bug.cgi?id=13281) :  `HttpClient.GetAsync(string requestUri, CancellationToken cancellationToken)` does not pass cancellationToken to  `SendAsync` method. 
-   [15143](https://bugzilla.xamarin.com/show_bug.cgi?id=15143) :  `BinaryReader.ReadString` problems. 
-   [15293](https://bugzilla.xamarin.com/show_bug.cgi?id=15293) :  `System.Net.Security.SslStream` crashes. 
-   [15451](https://bugzilla.xamarin.com/show_bug.cgi?id=15451) :  `HttpWebRequest` performs blocking operations exhausting the threadpool when using SSL. 
-   [15463](https://bugzilla.xamarin.com/show_bug.cgi?id=15463) : mono converts float multiplication back to a float before casting to int. 
-   [15574](https://bugzilla.xamarin.com/show_bug.cgi?id=15574) : Recursive  `KnownType` (as output by  `slsvcutil.exe` ) causes stack overflow during  `DataContractSerializer` constructor. 
-   [16119](https://bugzilla.xamarin.com/show_bug.cgi?id=16119) :  `Process.Start` leaves stray "open" processes 
-   [16327](https://bugzilla.xamarin.com/show_bug.cgi?id=16327) : Mono needs to expose configuration for TLS. 
-   [16744](https://bugzilla.xamarin.com/show_bug.cgi?id=16744) :  `DataContractJSONSerializer` produces different result to Microsoft.Net version. 
-   [16807](https://bugzilla.xamarin.com/show_bug.cgi?id=16807) : Assertion should not be reached while run code from debugger. 
-   [17183](https://bugzilla.xamarin.com/show_bug.cgi?id=17183) :  `System.IO.Compression.DeflateStream` gives incorrect data after compress/decompress cycle. 
-   [17204](https://bugzilla.xamarin.com/show_bug.cgi?id=17204) :  `EndPointManager.GetEPListener()` binds to all IP addresses when given a host-name instead of looking one up. 
-   [17256](https://bugzilla.xamarin.com/show_bug.cgi?id=17256) :  `CancellationTokenSource.Cancel()` throws  `ObjectDisposedException` . 
-   [17290](https://bugzilla.xamarin.com/show_bug.cgi?id=17290) : Use of ThreadLocal with struct causes memory leaks. 
-   [17310](https://bugzilla.xamarin.com/show_bug.cgi?id=17310) : stepping through code breaks execution. 
-   [17318](https://bugzilla.xamarin.com/show_bug.cgi?id=17318) : TryValidateProperty returns true when property is nullable and required and the value is null. 
-   [17536](https://bugzilla.xamarin.com/show_bug.cgi?id=17536) : Incorrect rounding when real literal's precision is beyond decimal type (28+). 
-   [17577](https://bugzilla.xamarin.com/show_bug.cgi?id=17577) : Empty value-type hashcode is not constant. 
-   [17587](https://bugzilla.xamarin.com/show_bug.cgi?id=17587) : Unexpected  `System.ArgumentException` : Type  `Char*` cannot be marshaled as an unmanaged structure. 
-   [17590](https://bugzilla.xamarin.com/show_bug.cgi?id=17590) :  `* Assertion at sgen-alloc.c:425, condition `*p == NULL' not met` . 
-   [17628](https://bugzilla.xamarin.com/show_bug.cgi?id=17628) :  `"５５"` (or  `"\xFF15\xFF15"` ) is recognized as an integer. 
-   [17632](https://bugzilla.xamarin.com/show_bug.cgi?id=17632) : Incorrect  `ProcessorArchitecture` for MSIL assemblies 
-   [17636](https://bugzilla.xamarin.com/show_bug.cgi?id=17636) :  `int.Parse()` does not support negative exponents 
-   [17663](https://bugzilla.xamarin.com/show_bug.cgi?id=17663) :  `DataContractSerializer` does not correctly serialize  `System.Guid` or  `System.Char` 
-   [17699](https://bugzilla.xamarin.com/show_bug.cgi?id=17699) :  `TimeSpan.ToString()` format doesn't match the Microsoft spec. 
-   [17736](https://bugzilla.xamarin.com/show_bug.cgi?id=17736) : Mono adding extra Content-Length header to DELETE requests. 
-   [17760](https://bugzilla.xamarin.com/show_bug.cgi?id=17760) :  `System.Collection.Generic.List<T>.Enumerator.Reset()` does not reset 'current' field. 
-   [17805](https://bugzilla.xamarin.com/show_bug.cgi?id=17805) :  `* Assertion at mini.c:4157, condition `code' not met` 
-   [17861](https://bugzilla.xamarin.com/show_bug.cgi?id=17861) :  `HttpClient` 's ContentLength fails to be computed when return is gzip stream. 
-   [17897](https://bugzilla.xamarin.com/show_bug.cgi?id=17897) :  `MemoryCacheEntryPriorityQueue` throws out of bounds on resize. 
-   [17977](https://bugzilla.xamarin.com/show_bug.cgi?id=17977) : appdomain unload crash. 
-   [17987](https://bugzilla.xamarin.com/show_bug.cgi?id=17987) :  `* Assertion at mini.c:4167, condition `code' not met` 
-   [18000](https://bugzilla.xamarin.com/show_bug.cgi?id=18000) :  `* Assertion: should not be reached at mono-threads-posix.c:154` 
-   [18052](https://bugzilla.xamarin.com/show_bug.cgi?id=18052) :  `DateTime.Parse()` value stored incorrectly 
-   [18063](https://bugzilla.xamarin.com/show_bug.cgi?id=18063) : A dynamically allocated string is referenced after it has been freed in the internals of GetHostByName. 
-   [18068](https://bugzilla.xamarin.com/show_bug.cgi?id=18068) : locals init is forced to true, even when it is not set. 
-   [18100](https://bugzilla.xamarin.com/show_bug.cgi?id=18100) : Stepping failed due to ERR_UNLOADED. 
-   [18121](https://bugzilla.xamarin.com/show_bug.cgi?id=18121) :  `LocalCallContext` is not captured by ThreadPool and  `new Thread()` . 
-   [18131](https://bugzilla.xamarin.com/show_bug.cgi?id=18131) :  `DataContractJsonSerializer.ReadObject` of a  `double` returns invalid result in German Region. 
-   [18162](https://bugzilla.xamarin.com/show_bug.cgi?id=18162) :  `CultureInfo.ClearCachedData()` throws argument null exception. 
-   [594490](https://bugzilla.novell.com/show_bug.cgi?id=594490) :  `XmlAttributeAttribute` outputting ':' as _x003A_ differs from .NET behavior. 
-   [599689](hhttps://bugzilla.novell.com/show_bug.cgi?id=599689) :  `XmlScemaException.ToString()` doesn't exactly match .NET. 


 <a name="3"></a>


 <a name="Xamarin.Android_4.12.3"></a>


#  <a ref="#Xamarin.Android_4.12.3">Xamarin.Android 4.12.3</a>


### New Features

-  Support for ART Android runtime.


### Bug fixes

-  OpenTK context fixes
-   [17630](https://bugzilla.xamarin.com/show_bug.cgi?id=17630) : Fix nonvirtual method invocation when running on ART. 
-   [18024](https://bugzilla.xamarin.com/show_bug.cgi?id=18024) : Install  `System.Runtime.InteropServices.WindowsRuntime.dll` and  `System.IO.Compression.dll` on Windows. 
-   [18378](https://bugzilla.xamarin.com/show_bug.cgi?id=18378) : WebStack: Missing method implementations in  `HttpWebRequest` and  `WebRequest` . 


 <a name="2"></a>


 <a name="Xamarin.Android_4.12.2"></a>


#  <a ref="#Xamarin.Android_4.12.2">Xamarin.Android 4.12.2</a>


The 4.12.2 update is a Windows-only release that fixes the Android designer in Visual Studio for users who have upgraded to Android SDK Tools 22.6.

4.12.2 requires the updated Android SDK Tools 22.6 to use the Android Designer in Visual Studio, and will prompt you to upgrade if you are on an older version.

### Fixes

-   [18218](https://bugzilla.xamarin.com/show_bug.cgi?id=18218) : Unable to open Android designer when SDK tool version is below 22.6 


 <a name="1"></a>


 <a name="Xamarin.Android_4.12.1"></a>


#  [Xamarin.Android 4.12.1](#Xamarin.Android_4.12.1)

The Xamarin.Android 4.12.1 release is a hotfix release to address issues in Xamarin.Android 4.12.0.

### Fixes

-   [15572](https://bugzilla.xamarin.com/show_bug.cgi?id=15572) : Fixes an exception thrown when  `XmlFormatterDeserializer.GetTypeFromNamePair()` was deserializing a  `KnownType(typeof(string[]))` . 
-   [16801](https://bugzilla.xamarin.com/show_bug.cgi?id=16801) : Fixes an issue that was causing some projects using components to fail after cleaning and rebuilding. 
-   [18013](https://bugzilla.xamarin.com/show_bug.cgi?id=18013) : Install the Android API-19 platform apk on Windows. 


 <a name="0"></a>


 <a name="Xamarin.Android_4.12.0"></a>


#  [Xamarin.Android 4.12.0](#Xamarin.Android_4.12.0)

### New Features

-  `Xamarin.Android.NUniteLite.dll` now binds NUniteLite 1.0.
-   [ART 4.4.2](http://source.android.com/devices/tech/dalvik/art.html) weak global reference workaround support: When running on Android v4.4.2 when ART is enabled, the GC will now use  `java.lang.WeakReference` instances instead of JNI Weak GlobalReferences (which is the same behavior as when running on Android v2.1 and prior targets) in order to work around an  [ART bug](https://code.google.com/p/android/issues/detail?id=63929) . This workaround will  *not* be used on Android v4.4.3, on the hopes/assumption that the fix will be integrated by then. (This may be a mistake.) 


### Known Issues

-  Xamarin.Android is not supported on ART. Full ART support will be provided in a future release. Please see  [Bug #17630](https://bugzilla.xamarin.com/show_bug.cgi?id=17630) for details. 


 <a name="Behavior_Changes" class="injected"></a>


### Behavior Changes

-  OpenTK, AndroidGameView: We now call the MakeCurrent method before calling the OnRenderFrame method in the AndroidGameView class, so that the render frame callback is always called with the right GL context. In case you want to return to the original behavior, set your AndroidGameView's instance AutoSetContextOnRenderFrame property to false. 


### Bug fixes

-  Multithreading fixes when looking up  `Java.Lang.Object` mappings.
-  PCL fixes.
-   [5590](https://bugzilla.xamarin.com/show_bug.cgi?id=5590) ,  [16075](https://bugzilla.xamarin.com/show_bug.cgi?id=16075) : Interface dispatch bug fixes. 
-   [12048](https://bugzilla.xamarin.com/show_bug.cgi?id=12048) : Missing static methods from type  `Android.Graphics.Color` . 
-   [13019](https://bugzilla.xamarin.com/show_bug.cgi?id=13019) : Visual Studio: ABI's getting serialized incorrectly into .csproj file using  `%3b` instead of comma. 
-   [13370](https://bugzilla.xamarin.com/show_bug.cgi?id=13370) : Compiler complains I am using  `System.ServiceModel` when I am not. 
-   [13953](https://bugzilla.xamarin.com/show_bug.cgi?id=13953) :  `RSACryptoServiceProvider.SignData()` doesn't support OID providers. 
-   [14129](https://bugzilla.xamarin.com/show_bug.cgi?id=14129) : Krait CPU bug fixes. 
-   [15127](https://bugzilla.xamarin.com/show_bug.cgi?id=15127) : Enums: Invalid method signature for  `PackageManager.SetApplicationEnabledSetting()` and  `SetComponentEnabledSetting()` 
-   [15300](https://bugzilla.xamarin.com/show_bug.cgi?id=15300) : Visual Studio: Selecting an emulator from the drop-down starts it. 
-   [15559](https://bugzilla.xamarin.com/show_bug.cgi?id=15559) :  `javac` compilation failed is path contains accentuated characters. 
-   [15573](https://bugzilla.xamarin.com/show_bug.cgi?id=15573) : Two Android Binding Library together cause build error 
-   [15891](https://bugzilla.xamarin.com/show_bug.cgi?id=15891) : Android/Java methods that take a Set/Map/List as an argument cause various exceptions,  `IncompatibleClassChangeError` ,  `ArgumentNullException` . 
-   [15892](https://bugzilla.xamarin.com/show_bug.cgi?id=15892) : Enums:  `GattState` should be an enumeration, and overrides that have  `GattState` should use it 
-   [16137](https://bugzilla.xamarin.com/show_bug.cgi?id=16137) :  `InvalidCastException` from  `Camera.Parameters.SupportedPreviewFpsRange` 
-   [16147](https://bugzilla.xamarin.com/show_bug.cgi?id=16147) :  `Android.Text.InputTypes` enum is not marked with  `FlagsAttribute` 
-   [16285](https://bugzilla.xamarin.com/show_bug.cgi?id=16285) : Xamarin.Android emits spurious activation error when set to use latest SDK 
-   [16377](https://bugzilla.xamarin.com/show_bug.cgi?id=16377) : MCW subclass object instance activation only calls the  `(IntPtr handle, JniHandleOwnership transfer)` constructor 
-   [16434](https://bugzilla.xamarin.com/show_bug.cgi?id=16434) : Xamarin tools cause errors editing project properties in Visual Studio 2013. 
-   [16622](https://bugzilla.xamarin.com/show_bug.cgi?id=16622) : Cascading Rebuild due to using Libraries with  `IncludeAndroidResourcesFromAttribute` 
-   [16679](https://bugzilla.xamarin.com/show_bug.cgi?id=16679) :  `Android.App.SyncContext.Post()` is synchronous when invoked from the Main/UI thread. 
-   [16817](https://bugzilla.xamarin.com/show_bug.cgi?id=16817) : Fix Facebook sample compilation. 
-   [16766](https://bugzilla.xamarin.com/show_bug.cgi?id=16766) : Adding a reference to Nito.AsyncEx.Enlightenment.dll causes the incorrect System.dll to be used? 
-   [17068](https://bugzilla.xamarin.com/show_bug.cgi?id=17068) : Add support for  `DoNotPackageAttribute` . 
-   [17156](https://bugzilla.xamarin.com/show_bug.cgi?id=17156) : Prefer  `Build-tools` 19.0.1 so that the  `Resources\transition` directory is supported. 


### Integrated Mono features/fixes

Based on [Mono 3.2.5](http://www.mono-project.com/Release_Notes_Mono_3.2#New_in_Mono_3.2.5) [commit f624a395](https://github.com/mono/mono/commit/f624a39586b4d4d8358921f5ca239ab5dee89c88).

-   [3501](https://bugzilla.xamarin.com/show_bug.cgi?id=3501) : Fix  `File.GetAttributes()` for group-writable files. 
-   [5245](https://bugzilla.xamarin.com/show_bug.cgi?id=5245) :  `IEquatable<T>` ,  `IEqualityComparer<T>` are ignored by  `LinkedList<T>.Find()` . 
-   [5700](https://bugzilla.xamarin.com/show_bug.cgi?id=5700) : Step over stopping too early in recursive call. 
-   [10883](https://bugzilla.xamarin.com/show_bug.cgi?id=10883) : Exception when external process ends. 
-   [11335](https://bugzilla.xamarin.com/show_bug.cgi?id=11335) :  `WebOperationContext.Current.OutgoingRequest.Headers` is  `null` in  `OperationContextScope` . 
-   [11336](https://bugzilla.xamarin.com/show_bug.cgi?id=11336) :  `OperationContext.Current.OutgoingMessageProperties` not setting HTTP request headers. 
-   [12754](https://bugzilla.xamarin.com/show_bug.cgi?id=12754) : Linux bug in  `_wapi_setsockopt` implementation 
-   [12875](https://bugzilla.xamarin.com/show_bug.cgi?id=12875) : Using System.Net.HttpRequest::EndGetRequestStream. 
-   [14950](https://bugzilla.xamarin.com/show_bug.cgi?id=14950) : Assertion at debugger-agent.c:4154, condition `count > 0' not met 
-   [15124](https://bugzilla.xamarin.com/show_bug.cgi?id=15124) : TypeLoadException when resolving qualified names of generic, compiler-generated F# types. 
-   [15320](https://bugzilla.xamarin.com/show_bug.cgi?id=15320) : Debugger display attributes don't support inheritance 
-   [15347](https://bugzilla.xamarin.com/show_bug.cgi?id=15347) :  `AssemblyName.ProcessorArchitecture` always returns "None". 
-   [15425](https://bugzilla.xamarin.com/show_bug.cgi?id=15425) : CultureInfo problem cy-GB. 
-   [15552](https://bugzilla.xamarin.com/show_bug.cgi?id=15552) :  `System.Xml.Schema.Extensions` class missing. 
-   [15719](https://bugzilla.xamarin.com/show_bug.cgi?id=15719) : InvalidProgramException when executing async event handler that doesn't await. 
-   [15759](https://bugzilla.xamarin.com/show_bug.cgi?id=15759) : Mono GC deadlock. 
-   [15857](https://bugzilla.xamarin.com/show_bug.cgi?id=15857) :  `HttpClient` async cancellation of POST requests unreliable 
-   [15875](https://bugzilla.xamarin.com/show_bug.cgi?id=15875) :  `CultureInfo.CurrentCulture` needs more intelligent fallback. 
-   [15895](https://bugzilla.xamarin.com/show_bug.cgi?id=15895) :  `CultureInfo` for Indonesia shows incorrect currency decimal places 
-   [15956](https://bugzilla.xamarin.com/show_bug.cgi?id=15956) :  `Task.WhenAll<T>` task hangs when list of tasks to wait for is empty. 
-   [15969](https://bugzilla.xamarin.com/show_bug.cgi?id=15969) : Segmentation fault on thread abort 
-   [15987](https://bugzilla.xamarin.com/show_bug.cgi?id=15987) : Floating point results differ between .NET and mono. 
-   [16021](https://bugzilla.xamarin.com/show_bug.cgi?id=16021) : Setting  `ReceiveBufferSize` &amp;  `SendBufferSize` on  `TcpClient` or  `Socket` doesn't have the desired affect 
-   [16071](https://bugzilla.xamarin.com/show_bug.cgi?id=16071) :  `System.ComponentModel.Design.HelpKeywordAttribute` not implemented. 
-   [16113](https://bugzilla.xamarin.com/show_bug.cgi?id=16113) : Add support for letting the remote know about the inferior's exit code. 
-   [16267](https://bugzilla.xamarin.com/show_bug.cgi?id=16267) : Wrong  `SemaphoreSlim.Wait` busy-loop delay when no timeout. 
-   [16318](https://bugzilla.xamarin.com/show_bug.cgi?id=16318) :  `List<T>` initializes to different size than Microsoft compiled CIL 
-   [16334](https://bugzilla.xamarin.com/show_bug.cgi?id=16334) :  `ConcurrentBag.TryTake()` and  `TryPeek()` can return  `true` with no result. 
-   [16365](https://bugzilla.xamarin.com/show_bug.cgi?id=16365) :  `TextInfo.ToTitleCase()` differs from .Net implementation. 
-   [16432](https://bugzilla.xamarin.com/show_bug.cgi?id=16432) : Mono GC deadlock 2. 
-   [16449](https://bugzilla.xamarin.com/show_bug.cgi?id=16449) : SIGSEGV in Arrays. 
-   [16487](https://bugzilla.xamarin.com/show_bug.cgi?id=16487) :  `Assembly.CreateInstance` doesn't calls  `AssemblyResolve` if assembly not found. 
-   [16489](https://bugzilla.xamarin.com/show_bug.cgi?id=16489) :  `NullReferenceException` in  `System.NumberFormatter.ResetCharBuf` . 
-   [16526](https://bugzilla.xamarin.com/show_bug.cgi?id=16526) : Mono's  `BigInteger` converts a large negative to a positive int64. 
-   [16529](https://bugzilla.xamarin.com/show_bug.cgi?id=16529) : F#  `unativeint` conversion from  `Double` to  `UIntPtr` generates  `conv.u` instruction which is not implemented by Mono. 
-   [16530](https://bugzilla.xamarin.com/show_bug.cgi?id=16530) : Bug in LINQ Join over IEnumerable data when both rows have a  `null` key. 
-   [16548](https://bugzilla.xamarin.com/show_bug.cgi?id=16548) : async / await "finishes" running thread and resumes execution on main UI thread 
-   [16587](https://bugzilla.xamarin.com/show_bug.cgi?id=16587) : Task implementation does not run continuations on correct TaskScheduler. 
-   [16634](https://bugzilla.xamarin.com/show_bug.cgi?id=16634) :  `System.Net.Http.Headers.HttpContentHeaders.TryGetValues()` throws exception. 
-   [16647](https://bugzilla.xamarin.com/show_bug.cgi?id=16647) : Performance improvements in  `Join<T> (string separator, IEnumerable<T> values)` 
-   [16670](https://bugzilla.xamarin.com/show_bug.cgi?id=16670) :  `System.Net.Http.HttpClient.PutAsync` method sends the request as GET method. 
-   [16730](https://bugzilla.xamarin.com/show_bug.cgi?id=16730) : ConcurrentDictionary is not marked as Serializable. 
-   [16788](https://bugzilla.xamarin.com/show_bug.cgi?id=16788) :  `Thread.GetNamedDataSlot` incorrectly increments the slot id for each call. 
-   [16832](https://bugzilla.xamarin.com/show_bug.cgi?id=16832) :  `NetworkStream(bool)` constructor parameter should be "ownsSocket", not "owns_socket". 
-   [16857](https://bugzilla.xamarin.com/show_bug.cgi?id=16857) :  `webClient.DownloadStringTaskAsync(foo).Start()` is buggy. 
-   [16951](https://bugzilla.xamarin.com/show_bug.cgi?id=16951) : [PCL]  `ReadOnlyDictionary` is missing from the  `System.ObjectModel` facade. 
-   [16992](https://bugzilla.xamarin.com/show_bug.cgi?id=16992) :  `CancellationTokenSource.Cancel` calls callbacks in reverse order. 
-   [17009](https://bugzilla.xamarin.com/show_bug.cgi?id=17009) :  `File.Move()` wont honor  `FileShare.ReadWrite | FileShare.Delete` . 
-   [17015](https://bugzilla.xamarin.com/show_bug.cgi?id=17015) :  `TaskScheduler.UnobservedTaskException` raised for trapped exceptions. 
-   [17023](https://bugzilla.xamarin.com/show_bug.cgi?id=17023) :  `Assertion at ../../../../../mono/mono/mini/method-to-ir.c:12854, condition `var->opcode == OP_REGOFFSET' not met` 
-   [17044](https://bugzilla.xamarin.com/show_bug.cgi?id=17044) :  `System.DateTime.ToLongDateString()` returns wrong format in "en-CA" cultures 
-   [17128](https://bugzilla.xamarin.com/show_bug.cgi?id=17128) : Seek on  `FileStream` passed 2GB raises exception. 
-   [17132](https://bugzilla.xamarin.com/show_bug.cgi?id=17132) :  `HttpRequestMessage` fails in Xam.iOS and Xam.Android but works in .NET 4.5. 
-   [17151](https://bugzilla.xamarin.com/show_bug.cgi?id=17151) :  `DateTimeFormat.FirstDayOfWeek` returns wrong value. 
-   [17410](https://bugzilla.xamarin.com/show_bug.cgi?id=17410) : Application crash on x86 emulator when user hover mouse over breakpoint. 


 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.12/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.12/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.12/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.12/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.12/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.12/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.12/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.12/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.12/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.12/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.12/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.12/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.12/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_17_diff/opentk-1.0.dll) 
-  API Level 18:  [Mono.Android.dll](xamarin.android_4.12/level_18_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.12/level_18_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.12/level_18_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.12/level_18_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.12/level_18_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.12/level_18_diff/opentk-1.0.dll)
