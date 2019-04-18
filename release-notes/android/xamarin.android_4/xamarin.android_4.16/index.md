---
id: 7173B5EB-4990-47B6-9D86-BE43FF3E3DBC
title: "Xamarin.Android 4.16"
---

The Xamarin.Android 4.16 series contains various bug fixes.

 **Note:** Xamarin.Android 4.16 is the first release that was
tested with and recommends [JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html). JDK 1.6 can continue to be used.

 <a name="0"></a>


 <a name="Xamarin.Android_4.16.0"></a>


#  [Xamarin.Android 4.16.0](#Xamarin.Android_4.16.0)

### New Features

-  Automatically building a separate  `.apk` for each ABI works.
-  OpenTK AndroidGameView can now run rendering loop on non-UI thread to achieve more fluent rendering.


### Known Issues

-  This release unfortunately broke  [ `debug.mono.log`handling](http://developer.xamarin.com/guides/android/troubleshooting/troubleshooting/#Xamarin.Android_System_Properties) ; the  `debug.mono.log` system property is ignored. Within Xamarin.Android 4.16, set the  `debug.mono.debug` system property instead. The  `debug.mono.log` system property will be fixed in Xamarin.Android 4.18. 


### Bug fixes

-   [2139](https://bugzilla.xamarin.com/show_bug.cgi?id=2139) : Support opengl context sharing across threads. 
-   [2257](https://bugzilla.xamarin.com/show_bug.cgi?id=2257) : Unable to reference a  `<color>` element if its name contains an upper case. 
-   [8182](https://bugzilla.xamarin.com/show_bug.cgi?id=8182) : OpenTK app +  `Intent.CreateChooser()` crashes. 
-   [13974](https://bugzilla.xamarin.com/show_bug.cgi?id=13974) : CopyMdbFiles task in Xamarin.Android.Common.targets doesn't work for read-only files. 
-   [17146](https://bugzilla.xamarin.com/show_bug.cgi?id=17146) : Reference jars from referenced dlls are not passed to jar2xml with JavaLibraryReference. 
-   [18798](https://bugzilla.xamarin.com/show_bug.cgi?id=18798) : Root element within .axml is not "fixed up"/replaced with ACW name. 
-   [19748](https://bugzilla.xamarin.com/show_bug.cgi?id=19748) : Android build tools should use  `aapt --max-res-version` , with the API level that the app is compiled against. 
-   [20084](https://bugzilla.xamarin.com/show_bug.cgi?id=20084) : Error executing task BuildApk: Out of memory. 
-   [20172](https://bugzilla.xamarin.com/show_bug.cgi?id=20172) :  `System.TimeZone.CurrentTimeZone.GetUtcOffset(DateTime.Now)` returns wrong value. 
-   [20179](https://bugzilla.xamarin.com/show_bug.cgi?id=20179) : PCLv2 facade assemblies aren't installed when required. 
-   [20555](https://bugzilla.xamarin.com/show_bug.cgi?id=20555) : Xamarin.Android.NUnitLite also implements System.SerializableAttribute that causes ambiguous reference with System.SerializableAttribute in System.dll. 
-   [20605](https://bugzilla.xamarin.com/show_bug.cgi?id=20605) : Xam 3.1 Alpha: AIDL using android.os.Bundle gets bad case translation to Android.Os.Bundle (should be Android.OS.Bundle). 
-   [20624](https://bugzilla.xamarin.com/show_bug.cgi?id=20624) : [Deploy] Xamarin.Android.Platform.apk generation hardcodes android-8. 
-   [20631](https://bugzilla.xamarin.com/show_bug.cgi?id=20631) : Xamarin.Android.Platform.apk signing is failing due to (NO_CERTIFICATES). 
-   [20748](https://bugzilla.xamarin.com/show_bug.cgi?id=20748) : Last stack trace entry truncated. 
-   [20926](https://bugzilla.xamarin.com/show_bug.cgi?id=20926) : GooglePlayServices component sample and others are failing to build. 
-   [22032](https://bugzilla.xamarin.com/show_bug.cgi?id=22032) :  `BuildApk` task fails on Windows due to a path being too long. 
-   [22074](https://bugzilla.xamarin.com/show_bug.cgi?id=22074) : System.TypeLoadException: Could not load type 'Net.Sqlcipher.ICursorInvoker' from assembly 'SQLCipherBindingLibrary 
-   [22125](https://bugzilla.xamarin.com/show_bug.cgi?id=22125) : Two component sample build regressions due to resource issues. 


### Integrated Mono features/fixes

Based on [Mono 3.8.0](http://www.mono-project.com/Release_Notes_Mono_3.8) [commit 21112244](https://github.com/mono/mono/commit/21112244e0822c9265d4456686d6a451d793e2fc).

-   [358](https://bugzilla.xamarin.com/show_bug.cgi?id=358) : Registry's UserStore hardcodes a path in user's home directory. 
-   [16439](https://bugzilla.xamarin.com/show_bug.cgi?id=16439) : Exception thrown in async call is bypassing catch block. 
-   [16990](https://bugzilla.xamarin.com/show_bug.cgi?id=16990) : ConcurrentDictionary lacks proper support for  `Contains(KeyValuePair<TKey, TValue>` . 
-   [18371](https://bugzilla.xamarin.com/show_bug.cgi?id=18371) : Incorrect Object not compatible with constrained type at 0x000a. 
-   [19058](https://bugzilla.xamarin.com/show_bug.cgi?id=19058) : SIGSEGV signal in mono_signature_hash. 
-   [19287](https://bugzilla.xamarin.com/show_bug.cgi?id=19287) : JavaScriptSerializer deserializes nullable enum as always null. 
-   [19343](https://bugzilla.xamarin.com/show_bug.cgi?id=19343) : SIGSEGV crash in garbage collector. 
-   [19460](https://bugzilla.xamarin.com/show_bug.cgi?id=19460) : View Accessor for Zero byte file MemoryMappedFile. 
-   [19924](https://bugzilla.xamarin.com/show_bug.cgi?id=19924) : Step over AppDomain.Unload results into continued execution. 
-   [20020](https://bugzilla.xamarin.com/show_bug.cgi?id=20020) : CustomMarshaler in referenced assembly. 
-   [20108](https://bugzilla.xamarin.com/show_bug.cgi?id=20108) : System.IO.FileNotFoundException: Could not load assembly 'System.ServiceModel.Security, Version=3.9.0.0, Culture=. 
-   [20244](https://bugzilla.xamarin.com/show_bug.cgi?id=20244) : isinf() check fails when compiling with CLANG. 
-   [20360](https://bugzilla.xamarin.com/show_bug.cgi?id=20360) : FileStream Read on created Thread hangs the app after time. 
-   [20412](https://bugzilla.xamarin.com/show_bug.cgi?id=20412) :  `* Assertion at method-to-ir.c:12061, condition `handler_offset != -1' not met` 
-   [20456](https://bugzilla.xamarin.com/show_bug.cgi?id=20456) : System.Numerics : BigInteger construction from byte array. 
-   [20503](https://bugzilla.xamarin.com/show_bug.cgi?id=20503) : GC.WaitForPendingFinalizers() doesn't wait for pending finalizers. 
-   [20582](https://bugzilla.xamarin.com/show_bug.cgi?id=20582) : Compute method of System.Data.DataTable not using Invariant Culture to evaluate expressions. 
-   [20583](https://bugzilla.xamarin.com/show_bug.cgi?id=20583) : ReadAsStreamAsync returns 0 length stream over SSL. 
-   [20591](https://bugzilla.xamarin.com/show_bug.cgi?id=20591) : MemoryMappedFile CreateNew aborts on using statement. 
-   [20616](https://bugzilla.xamarin.com/show_bug.cgi?id=20616) : Segmentation fault when running System.ServiceModel tests. 
-   [20672](https://bugzilla.xamarin.com/show_bug.cgi?id=20672) : ListChangedEventArgs.PropertyDescriptor is always null in BindingList.ListChanged event args. 
-   [20674](https://bugzilla.xamarin.com/show_bug.cgi?id=20674) : Marshalling structs with strings fails. 
-   [20788](https://bugzilla.xamarin.com/show_bug.cgi?id=20788) : marshal7: test hardcodes the wrong structure size for 32-bit Intel Linux 
-   [20818](https://bugzilla.xamarin.com/show_bug.cgi?id=20818) : System.Net.Http.DelegatingHandler.Dispose() throws NullReferenceException if InnerHandler not assigned. 
-   [20870](https://bugzilla.xamarin.com/show_bug.cgi?id=20870) : Enum.TryParse does not work with leading whitespace. 
-   [20922](https://bugzilla.xamarin.com/show_bug.cgi?id=20922) : Array.Sort() GeneratesGarbage. 
-   [21017](https://bugzilla.xamarin.com/show_bug.cgi?id=21017) : ConnectCallback needs to call EndConnect. 
-   [21069](https://bugzilla.xamarin.com/show_bug.cgi?id=21069) : CloseTest and OpenTest4 in CustomPeerResolverServiceTest occasionally time out. 
-   [21196](https://bugzilla.xamarin.com/show_bug.cgi?id=21196) : newobj does not recognise closed delegate. 
-   [21375](https://bugzilla.xamarin.com/show_bug.cgi?id=21375) :  `Dictionary<GUID, float>` uses more memory with Mono vs .NET 
-   [21388](https://bugzilla.xamarin.com/show_bug.cgi?id=21388) : DeclaringType property getter on a GenericParameter crashes the VM (in certain cases) 
-   [21645](https://bugzilla.xamarin.com/show_bug.cgi?id=21645) : Slow invocation of generic method on value type. 


 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.14/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.14/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.14/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.14/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.14/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.14/level_7_diff/mono.android.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.14/level_8_diff/mono.android.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.14/level_10_diff/mono.android.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.14/level_12_diff/mono.android.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.14/level_14_diff/mono.android.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.14/level_14_diff/mono.android.support.v13.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.14/level_15_diff/mono.android.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.14/level_16_diff/mono.android.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.14/level_17_diff/mono.android.dll) 
-  API Level 18:  [Mono.Android.dll](xamarin.android_4.14/level_18_diff/mono.android.dll) 
-  API Level 19:  [Mono.Android.dll](xamarin.android_4.14/level_19_diff/mono.android.dll)
