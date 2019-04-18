---
id: 638ED8CF-6A74-4C0F-8CD2-91DA74D2A592
title: "Xamarin.Android 4.12"
---

The Xamarin.Android 4.11 adds bindings for [Android 4.4 KitKat](http://www.android.com/versions/kit-kat-4-4/).

 <a name="0"></a>


 <a name="Xamarin.Android_4.11.0"></a>


#  [Xamarin.Android 4.11.0](#Xamarin.Android_4.11.0)

### New Features

-  `Xamarin.Android.NUniteLite.dll` now binds NUniteLite 1.0.


### Bug fixes

-  Multithreading fixes when looking up  `Java.Lang.Object` mappings.
-  PCL fixes.
-   [5590](https://bugzilla.xamarin.com/show_bug.cgi?id=5590) ,  [16075](https://bugzilla.xamarin.com/show_bug.cgi?id=16075) : Interface dispatch bug fixes. 
-   [13019](https://bugzilla.xamarin.com/show_bug.cgi?id=13019) : Visual Studio: ABI's getting serialized incorrectly into .csproj file using  `%3b` instead of comma. 
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
-   [16622](https://bugzilla.xamarin.com/show_bug.cgi?id=16622) : Cascading Rebuild due to using Libraries with  `IncludeAndroidResourcesFromAttribute` 
-   [16679](https://bugzilla.xamarin.com/show_bug.cgi?id=16679) :  `Android.App.SyncContext.Post()` is synchronous when invoked from the Main/UI thread. 


### Integrated Mono features/fixes

Based on [Mono 3.2.5](http://www.mono-project.com/Release_Notes_Mono_3.2#New_in_Mono_3.2.5) [commit 17867123](https://github.com/mono/mono/commit/178671233141aae5e9f9a3fa5f67b564d287051a).

-   [5700](https://bugzilla.xamarin.com/show_bug.cgi?id=5700) : Step over stopping too early in recursive call. 
-   [12754](https://bugzilla.xamarin.com/show_bug.cgi?id=12754) : Linux bug in  `_wapi_setsockopt` implementation 
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
-   [16526](https://bugzilla.xamarin.com/show_bug.cgi?id=16526) : Mono's  `BigInteger` converts a large negative to a positive int64. 
-   [16529](https://bugzilla.xamarin.com/show_bug.cgi?id=16529) : F#  `unativeint` conversion from  `Double` to  `UIntPtr` generates  `conv.u<>/code> instruction which is not implemented by Mono. </li> <li> <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=16530" target="_blank">16530</a>: Bug in LINQ Join over IEnumerable data when both rows have a <code>null` key. 
-   [16587](https://bugzilla.xamarin.com/show_bug.cgi?id=16587) : Task implementation does not run continuations on correct TaskScheduler. 
-   [16634](https://bugzilla.xamarin.com/show_bug.cgi?id=16634) :  `System.Net.Http.Headers.HttpContentHeaders.TryGetValues()` throws exception. 
-   [16647](https://bugzilla.xamarin.com/show_bug.cgi?id=16647) : Performance improvements in  `Join<T> (string separator, IEnumerable<T> values)` 
-   [16670](https://bugzilla.xamarin.com/show_bug.cgi?id=16670) :  `System.Net.Http.HttpClient.PutAsync` method sends the request as GET method. 


 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.11/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.11/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.11/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.11/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.11/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.11/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.11/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.11/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.11/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.11/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.11/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.11/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.11/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_17_diff/opentk-1.0.dll) 
-  API Level 18:  [Mono.Android.dll](xamarin.android_4.11/level_18_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.11/level_18_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.11/level_18_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.11/level_18_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.11/level_18_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.11/level_18_diff/opentk-1.0.dll)
