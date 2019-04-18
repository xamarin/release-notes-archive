---
id: B4C3BC02-5645-4EF7-ADCD-2767974A3DFB
title: "Xamarin.Android 4.18"
---

The Xamarin.Android 4.18 series contains various bug fixes.

 <a name="1"></a>


 <a name="Xamarin.Android_4.18.1"></a>


#  [Xamarin.Android 4.18.1](#Xamarin.Android_4.18.1)

### Known Issues

-  Fixing  [bug 23823](https://bugzilla.xamarin.com/show_bug.cgi?id=23823) involved reverting some build-time performance improvements. Users may see a drop in repeated build performance when compared to 4.18.0. The performance enhancements will be re-worked and re-released in a future update.


### Bug fixes

-   [13686](https://bugzilla.xamarin.com/show_bug.cgi?id=13686) : Problems with System.TimeZoneInfo. 
-   [20172](https://bugzilla.xamarin.com/show_bug.cgi?id=20172) :  `System.TimeZone.CurrentTimeZone.GetUtcOffset(DateTime.Now)` returns wrong value. 
-   [21550](https://bugzilla.xamarin.com/show_bug.cgi?id=21550) : Crash on startup on Intel Atom x86 for MvvmCross app. 
-   [22955](https://bugzilla.xamarin.com/show_bug.cgi?id=22955) : Basic DateTime calculations are throwing execptions since last update. 
-   [22991](https://bugzilla.xamarin.com/show_bug.cgi?id=22991) : System.DateTime implementation should not use native objects. 
-   [23405](https://bugzilla.xamarin.com/show_bug.cgi?id=23405) : DateTime.Now returns time off by 1 hour. 
-   [23653](https://bugzilla.xamarin.com/show_bug.cgi?id=23653) : "Access to the path ...obj\Debug\res\... is denied" when resource files are marked as read-only. 
-   [23823](https://bugzilla.xamarin.com/show_bug.cgi?id=23823) : Error rendering views with AppCompat. 
-   [23880](https://bugzilla.xamarin.com/show_bug.cgi?id=23880) : Binary XML file line #1 Error inflating class when namespace is not lowercase in AXML. 


 <a name="0"></a>


 <a name="Xamarin.Android_4.18.0"></a>


#  [Xamarin.Android 4.18.0](#Xamarin.Android_4.18.0)

### New Features



<h3 id="known-issues-30">Known Issues in 4.18.0.30</h3>

-   [23167](https://bugzilla.xamarin.com/show_bug.cgi?id=23167) : XML View names not updated. In previous releases, if a Library project contained resource XML which referenced C# View types, the Library project's XML would be updated at build time to use the correct  [ACW's](http://developer.xamarin.com/guides/android/advanced_topics/java_integration_overview/android_callable_wrappers/) . That was accidentally broken.  **Workaround** : Use ACW names in Layout .axml, not C# type names.

  This will be fixed in 4.18.0.32.

 


### Bug fixes

-   [1969](https://bugzilla.xamarin.com/show_bug.cgi?id=1969) :  `System.Net.NetworkInformation.GetAllNetworkInterfaces()` Fails. 
-   [9770](https://bugzilla.xamarin.com/show_bug.cgi?id=9770) : Generator produces incorrect connector for the RegisterAttribute. 
-   [18692](https://bugzilla.xamarin.com/show_bug.cgi?id=18692) : Including large numbers of Resources result in really slow build times. 
-   [18763](https://bugzilla.xamarin.com/show_bug.cgi?id=18763) : Native SIGSEGVs don't invoke Android's SIGSEGV handler [Take 2!]. Thanks to 14 T.J. Purtell. 
-   [21351](https://bugzilla.xamarin.com/show_bug.cgi?id=21351) : Attribute  *name* has already been defined.    
 Fixed in Xamarin.Android 4.18.0.32. 
-   [21747](https://bugzilla.xamarin.com/show_bug.cgi?id=21747) : Returning  `long[]` as inout parameter from Android service doesn't result in expected values. 
-   [22057](https://bugzilla.xamarin.com/show_bug.cgi?id=22057) : Capital letters in Java package names cause java.lang.NoClassDefFoundError for resources. 
-   [22061](https://bugzilla.xamarin.com/show_bug.cgi?id=22061) : Assets within Class Libraries are wrong embbeded in the Application referencing the class library. 
-   [22155](https://bugzilla.xamarin.com/show_bug.cgi?id=22155) : GoogleApiClientBuilder.AddApi(Api, Object) throws Java.Lang.NoSuchMethodError Exception. 
-   [22271](https://bugzilla.xamarin.com/show_bug.cgi?id=22271) : Stepping over breakpoints results in crash. 
-   [22286](https://bugzilla.xamarin.com/show_bug.cgi?id=22286) : VMSafeMode (and others, i.e. AllowBackup) missing in ApplicationAttribute. 
-   [23167](https://bugzilla.xamarin.com/show_bug.cgi?id=23167) :  **Regression** involving Layout XML within Library projects.    
 Fixed in Xamarin.Android 4.18.0.31. 


### Integrated Mono features/fixes

Based on [Mono 3.10.0](http://www.mono-project.com/Release_Notes_Mono_3.10) [commit 5d07b77a](https://github.com/mono/mono/commit/5d07b77a67f61576318a30e8b1c5f65f7f26b1cf).

-   [833](https://bugzilla.xamarin.com/show_bug.cgi?id=833) : Path.GetFullPath returns duplicate DirectorySeparatorStr if Directory.GetCurrentDirectory() == DirectorySeparatorStr. 
-   [3211](https://bugzilla.xamarin.com/show_bug.cgi?id=3211) : Race condition when XmlAnyElement is applied to a XmlNode field 
-   [6913](https://bugzilla.xamarin.com/show_bug.cgi?id=6913) : Error creating XmlSerializer on mono (on .NET is ok) when target's parent[!] class don't have parameterless constructor. 
-   [10163](https://bugzilla.xamarin.com/show_bug.cgi?id=10163) : System.Net.WebClient.OpenWrite not working. 
-   [11916](https://bugzilla.xamarin.com/show_bug.cgi?id=11916) : System.Xml.Linq.XElement cannot be de/serialized. 
-   [18482](https://bugzilla.xamarin.com/show_bug.cgi?id=18482) : RSA - Import Public Key Bug. 
-   [19097](https://bugzilla.xamarin.com/show_bug.cgi?id=19097) : Remove assert about condition param_count not met. 
-   [19313](https://bugzilla.xamarin.com/show_bug.cgi?id=19313) : DeflateStream incorrectly blocks, whereas Microsoft's runtime works fine. 
-   [20359](https://bugzilla.xamarin.com/show_bug.cgi?id=20359) : System.Net.WebClient.UploadValuesTaskAsync doesn't set Content-Type. 
-   [21771](https://bugzilla.xamarin.com/show_bug.cgi?id=21771) : XmlReader.Dispose() calls Dispose(false) 
-   [21960](https://bugzilla.xamarin.com/show_bug.cgi?id=21960) : HttpWebRequest NameValueHeaderValue does not allow quotes in key / values. 
-   [21982](https://bugzilla.xamarin.com/show_bug.cgi?id=21982) : .net 4.5 constructor overloads for GzipStream/DeflateStream are still not implemented 
-   [22059](https://bugzilla.xamarin.com/show_bug.cgi?id=22059) : Missing TypeLoadException for TypeBuilder.CreateType() with private interface 
-   [22114](https://bugzilla.xamarin.com/show_bug.cgi?id=22114) : String.Format() incorrectly parses {{{0:C}}} 
-   [22282](https://bugzilla.xamarin.com/show_bug.cgi?id=22282) : Mono 3.6.0 ClaimsPrincipal and ClaimsIdentity constructors fail and/or do not match .net 4.5. 


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
