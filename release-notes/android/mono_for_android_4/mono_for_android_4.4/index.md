---
id: 49A2512F-6A2A-CD94-9317-9FF02D944917
title: "Mono For Android 4.4"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a Mono for Android project. You can also check manually in Tools
&gt; Options &gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0. Layout Designer fixes require MonoDevelop
3.0.4.

 <a name="New_Features" class="injected"></a>


# New Features

-  Fixed an issue with the license check dialog during installation.
-  Provides preliminary API 17 (JellyBean 4.2) support.
-  armeabi-v7a is the default ABI for Release builds.
-  Debug .apk files include all ABIs by default. -   This will cause " [apparent regressions](https://bugzilla.xamarin.com/show_bug.cgi?id=5748)  "; this is By Design. 


 
-  Add&nbsp; [ActivityAttribute.ParentActivity](http://androidapi.xamarin.com/?link=P%3aAndroid.App.ActivityAttribute.ParentActivity) &nbsp;property. 
-  Add&nbsp; [ServiceAttribute.IsolatedProcess](http://androidapi.xamarin.com/?link=P%3aAndroid.App.ServiceAttribute.IsolatedProcess) &nbsp;property. 
-  Add&nbsp; [PermissionAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.PermissionAttribute) ,&nbsp; [PermissionGroupAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.PermissionGroupAttribute) , and&nbsp; [PermissionTreeAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.PermissionTreeAttribute) &nbsp;custom attributes. 
-  Now string literals in attributes ( <span>ActivityAttribute</span> ,&nbsp; <span>UsesPermissionAttribute</span> &nbsp;etc.) are scanned and&nbsp; * <span>@PACKAGE_NAME@</span>* &nbsp;is replaced&nbsp;with the actual package name at packaging time. (see&nbsp; [bug #7687](https://bugzilla.xamarin.com/show_bug.cgi?id=7687) ) 
-  Binding Projects now embed the bound&nbsp; <span>.jar</span> &nbsp;into the binding assembly. ( * <span>EmbeddedJar</span>* &nbsp;and&nbsp; * <span>EmbeddedReferenceJar</span>* &nbsp;build actions) 
-  Library Projects can now contain Android Resources.


 <a name="4.4.50_Fixes" class="injected"></a>


# 4.4.50 Fixes

-  Activation fix for Windows XP
-  Profiler support. (Beta!)
-  Removal of the dreaded UnhandledException handler from Visual Studio
-  .stamp files not being properly closed, leading to FileShare exceptions
-  UI designer improvements in the support for alternative layouts.
-   [7871](https://bugzilla.xamarin.com/show_bug.cgi?id=7871) :&nbsp;Saving a .axml file in a resource folder with qualifiers 
-   [8625](https://bugzilla.xamarin.com/show_bug.cgi?id=8625) :&nbsp;Color preview in Project Resources window showing wrong colours 
-   [8781](https://bugzilla.xamarin.com/show_bug.cgi?id=8781) :&nbsp;Fix Publish Android Application to pickup the correct PackageName 


 <a name="4.4.54_Fixes" class="injected"></a>


# 4.4.54 Fixes

-  Additional activation fix for users running on Windows XP with a&nbsp;wireless-only network connection. 


 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Theoretical GC bug involving a race condition between Mono &amp; Android GC's. Note: we've never seen this in the wild, and have no repro. 
-  GC weak reference fix.
-  .jar binding:&nbsp;do not generate overrides when it shouldn't for method variant property. 
-  .jar binding: improve obfuscated .jar handling
-  .jar binding: improved Annoation support.
-  Improve product activation on Windows.
-  Throw TypeLoadException if a Type can't be loaded instead of throwing a NullReferenceException. 
-   [WSDL import](http://stackoverflow.com/questions/12551090/monotouch-wcf-service-reference-cs-errors/12669880) . 
-  Improved WCF serialization support for collection types
-  Fix binding of&nbsp; [OverlayItem.GetMarker()](http://androidapi.xamarin.com/?link=M:Android.GoogleMaps.OverlayItem.GetMarker) &nbsp;and&nbsp; [MapActivity.OnGetMapDataSource()](http://androidapi.xamarin.com/?link=M%3aAndroid.GoogleMaps.MapActivity.OnGetMapDataSource) &nbsp;(reported by&nbsp; [Goncalo Oliveira](http://lists.ximian.com/pipermail/monodroid/2012-November/012759.html) ). 
-  Remove [DebuggerDisplay] attribute from KeyValuePair and DictionaryEntry. 
-  Support [OnSerializing] in System.Runtime.Serialization.Json
-   [3276](https://bugzilla.xamarin.com/show_bug.cgi?id=3276) :&nbsp;Mono implementation of HttpWebRequest eats the body of a DELETE request 
-   [5948](https://bugzilla.xamarin.com/show_bug.cgi?id=5948) :&nbsp;No color syntax for axml files in Designer/Source view in Visual Studio 2010 
-   [6249](https://bugzilla.xamarin.com/show_bug.cgi?id=6249) : Assets not included in package when IntermediateOutputPath is specified to an absolute path. 
-   [6329](https://bugzilla.xamarin.com/show_bug.cgi?id=6329) :&nbsp;Null refrence in WebConnectStream Ctor 
-   [6860](https://bugzilla.xamarin.com/show_bug.cgi?id=6860) :&nbsp;Inspecting properties results wrong value 
-   [7013#c15](https://bugzilla.xamarin.com/show_bug.cgi?id=7013#c15) : Add native libraries to .apks in the right order to improve support for Android 4.0-4.0.3. 
-   [7258](https://bugzilla.xamarin.com/show_bug.cgi?id=7258) :&nbsp;WebRequest.DefaultWebProxy with credentials fails 
-   [7309](https://bugzilla.xamarin.com/show_bug.cgi?id=7309) : Resources.GetXml - XmlReader.Name property Hangs without exception 
-   [7564](https://bugzilla.xamarin.com/show_bug.cgi?id=7564) :&nbsp;mono_aot_find_jit_info () is not signal safe (workaround) 
-   [7599](https://bugzilla.xamarin.com/show_bug.cgi?id=7599) :&nbsp;HttpWebRequest returns 404 because it reuses an old connection to a previous server 
-   [7637](https://bugzilla.xamarin.com/show_bug.cgi?id=7637) :&nbsp;HttpWebRequest::BeginGetResponse hangs when send request stream is empty 
-   [7686](https://bugzilla.xamarin.com/show_bug.cgi?id=7686) :&nbsp;Need a custom attribute [Permission] to generate &lt;permission ... /&gt; in AndroidManifest.xml 
-   [7687](https://bugzilla.xamarin.com/show_bug.cgi?id=7687) :&nbsp;Substitute package name in string literals 
-   [7837](https://bugzilla.xamarin.com/show_bug.cgi?id=7837) :&nbsp;Generate the //provider/@android:authorities attribute 
-   [7934](https://bugzilla.xamarin.com/show_bug.cgi?id=7934) :&nbsp;In MfA 4.2.8, Application.OnCreate doesn't get called anymore 
-   [7948](https://bugzilla.xamarin.com/show_bug.cgi?id=7948) :&nbsp; <span>Add support for EmbeddedReferenceJar</span> 
-   [7957](https://bugzilla.xamarin.com/show_bug.cgi?id=7957) :&nbsp;System.Xml.XmlException : 'Text' is an invalid node type 
-   [7966](http://bugzilla.xamarin.com/show_bug.cgi?id=7966) : TimeZoneInfo.FindSystemTimeZoneById returns null 
-   [8072](https://bugzilla.xamarin.com/show_bug.cgi?id=8072) :&nbsp;Avoid throwing exceptions from WeakReference.IsAlive after finalization when the underlying GCHandle is already finalized. 
-   [8104](https://bugzilla.xamarin.com/show_bug.cgi?id=8104) : Fix Notification.LedARGB to be of int type. 
-   [8134](https://bugzilla.xamarin.com/show_bug.cgi?id=8134) :&nbsp;JavaList needs to provide java.util.List methods to make it valid to derive from ArrayList 
-   [8312](http://bugzilla.xamarin.com/show_bug.cgi?id=8312) :&nbsp;SSL POST GetRequestStream gets exception 'authentication or decryption has failed' 
-   [8320](http://bugzilla.xamarin.com/show_bug.cgi?id=8320) :&nbsp;Runtime metadata bug with RX 
-   [8339](https://bugzilla.xamarin.com/show_bug.cgi?id=8339) :&nbsp;Remove Compiler Warnings in Resource.designer.cs 
-   [8405](https://bugzilla.xamarin.com/show_bug.cgi?id=8405) : OS X installer should not say "Activation Successful" if activation was not successful. 
-   [8406](https://bugzilla.xamarin.com/show_bug.cgi?id=8406) : Fix error messages generated by OS X installer. 
-   [8553](http://bugzilla.xamarin.com/show_bug.cgi?id=8553) :&nbsp;SSL Validation Issues 
-   [8559](http://bugzilla.xamarin.com/show_bug.cgi?id=8559) :&nbsp;TaskScheduler passed with parallel options to Parallel.ForEach not used correctly 


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_4_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_4_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_4_diff/mono.android.support.v4.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_4_diff/opentk.dll) &nbsp; [OpenTK-1.0.dll](mono_for_android_4.4/level_4_diff/opentk-1.0.dll) 
-  API Level 7:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_7_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_7_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_7_diff/mono.android.support.v4.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_7_diff/opentk.dll) 
-  API Level 8:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_8_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_8_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_8_diff/mono.android.support.v4.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_8_diff/opentk.dll) 
-  API Level 10:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_10_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_10_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_10_diff/mono.android.support.v4.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_10_diff/opentk.dll) 
-  API Level 12:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_12_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_12_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_12_diff/mono.android.support.v4.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_12_diff/opentk.dll) &nbsp; [OpenTK-1.0.dll](mono_for_android_4.4/level_12_diff/opentk-1.0.dll) 
-  API Level 14:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_14_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_14_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_14_diff/mono.android.support.v4.dll) ,&nbsp; [Mono.Android.Support.v13.dll](mono_for_android_4.4/level_14_diff/mono.android.support.v13.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_14_diff/opentk.dll) &nbsp; [OpenTK-1.0.dll](mono_for_android_4.4/level_14_diff/opentk-1.0.dll) 
-  API Level 15:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_15_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_15_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_15_diff/mono.android.support.v4.dll) ,&nbsp; [Mono.Android.Support.v13.dll](mono_for_android_4.4/level_15_diff/mono.android.support.v13.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_15_diff/opentk.dll) &nbsp; [OpenTK-1.0.dll](mono_for_android_4.4/level_15_diff/opentk-1.0.dll) 
-  API Level 16:&nbsp; [Mono.Android.dll](mono_for_android_4.4/level_16_diff/mono.android.dll) ,&nbsp; [Mono.Android.GoogleMaps.dll](mono_for_android_4.4/level_16_diff/mono.android.googlemaps.dll) ,&nbsp; [Mono.Android.Support.v4.dll](mono_for_android_4.4/level_16_diff/mono.android.support.v4.dll) ,&nbsp; [Mono.Android.Support.v13.dll](mono_for_android_4.4/level_16_diff/mono.android.support.v13.dll) ,&nbsp; [OpenTK.dll](mono_for_android_4.4/level_16_diff/opentk.dll) &nbsp; [OpenTK-1.0.dll](mono_for_android_4.4/level_16_diff/opentk-1.0.dll) 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
