---
id: 8BE5923C-5065-162B-0131-3AFA2334613B
title: "Mono For Android 4.0.3"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

 **GC Stability Improvements**: We've fixed an assert within the
GC and improved stability.

 <a name="Changes_since_4.0.1" class="injected"></a>


# Changes since 4.0.1

TargetFrameworkVersion no longer controls which android.jar is used when
building packages. (This is particularly useful for AdMob users, which must use
an API level 13+ android.jar.)TargetFrameworkVersion will set the
AndroidManifest.xml //uses-sdk/@android:minSdkVersion attribute and is the [JNI ABI your application will reference.](http://lists.ximian.com/pipermail/monodroid/2011-November/007350.html)
The//uses-sdk/@android:targetSdkVersion attribute controls which android.jar the
app is built against; if not specified, this defaults to
TargetFrameworkVersion.

There is now a System.Threading.SynchronizationContext: [Application.SynchronizationContext](http://androidapi.xamarin.com/?link=P:Android.App.Application.SynchronizationContext), for easier marshalling
back to a UI thread.

Added [ApplicationAttribute.UiOptions](http://androidapi.xamarin.com/?link=P:Android.App.ApplicationAttribute.UiOptions) property to generate the [//application/@android:uiOptions attribute](http://developer.android.com/guide/topics/manifest/application-element.html#uioptions).

Add [JNIEnv.GetDirectBufferAddress()](http://androidapi.xamarin.com/?link=M%3aAndroid.Runtime.JNIEnv.GetDirectBufferAddress) JNI method, [Java.Nio.Buffer.GetDirectBufferAddress()](http://androidapi.xamarin.com/?link=M%3aJava.Nio.Buffer.GetDirectBufferAddress) method.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  Additional int to enumeration parameter and return type conversions.
-  Mono.Cairo.dll is no longer distributed. (It never should have been distributed, as it doesn't work.) 


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_4_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_4_diff/mono.android.googledocs.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_4_diff/opentk.dll) 
-  API Level 7:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_7_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_7_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_7_diff/opentk.dll) 
-  API Level 8:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_8_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_8_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_8_diff/opentk.dll) 
-  API Level 10:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_10_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_10_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_10_diff/opentk.dll) 
-  API Level 12:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_12_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_12_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_12_diff/opentk.dll) 
-  API Level 14:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.3/level_14_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.3/level_14_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.3/level_14_diff/opentk.dll) 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [329](http://bugzilla.xamarin.com/show_bug.cgi?id=329) : Add support to serialize nullable types when the XmlElement has explicity set the DataType. 
-   [1147](http://bugzilla.xamarin.com/show_bug.cgi?id=1147) :  <span><span>Generic method failing "at
    mini-generic-sharing.c:407, condition `!(*oti)-&gt;data' not
    met".</span></span> 
-   [2169](http://bugzilla.xamarin.com/show_bug.cgi?id=2169) : Implement the  [ObservableCollection&lt;T&gt;](http://androidapi.xamarin.com/?link=T%3aSystem.Collections.ObjectModel.ObservableCollection%601) constructor to now throwNotImplementedException. 
-   [2440](http://bugzilla.xamarin.com/show_bug.cgi?id=2440) :  <span><span>System.UnauthorizedAccessException with fast
    deployment to emulator.</span></span> 
-   [2432](http://bugzilla.xamarin.com/show_bug.cgi?id=2432) : Re-enable -linkskip functionality. 
-   [2473](http://bugzilla.xamarin.com/show_bug.cgi?id=2473) :  <span><span>Webservices 2.0 Async download: memory is
    not released, app gets stuck or is running OOM.</span></span> 
-   [2482](http://bugzilla.xamarin.com/show_bug.cgi?id=2482) :  <span><span>DownloadProgressChanged's BytesReceived does
    not increment.</span></span> 
-   [2582](http://bugzilla.xamarin.com/show_bug.cgi?id=2582) :  <span><span>Android.Util.TypedValue.ApplyDimension
    should take enum parameter.</span></span> 
-   [2688](http://bugzilla.xamarin.com/show_bug.cgi?id=2688) : Fix the [Obsolete] message text on  *Consts* -suffixed types. 
-   [2609](http://bugzilla.xamarin.com/show_bug.cgi?id=2609) : Don't generate duplicate ACW constructors. 
-  Allow null collections instances to be passed into Java;  [email](http://lists.ximian.com/pipermail/monodroid/2011-December/007752.html)  [thread](http://lists.ximian.com/pipermail/monodroid/2011-December/007777.html) . 
-  The AndroidStoreUncompressedFileExtensions MSBuild property now behaves as documented. ( [Email thread](http://lists.ximian.com/pipermail/monodroid/2011-December/007819.html) .) 
-  Fast Deployment-enabled installs to the emulator should no longer throwUnauthorizedAccesException when creating files. ( [Email thread](http://lists.ximian.com/pipermail/monodroid/2011-December/007721.html) .) 
-  Fix the value of  [Android.Graphics.Color.Transparent](http://androidapi.xamarin.com/?link=P%3aAndroid.Graphics.Color.Transparent) . 
-  Make sure MD Android addin stops if it hits a deployment failure.
-  Fix inheriting from JavaList&lt;T&gt;.
-   [Support opening SQLite databases in read-only mode](http://stackoverflow.com/q/8602726/220643) . 
-   [JSON](http://androidapi.xamarin.com/?link=T%3aSystem.Runtime.Serialization.Json.DataContractJsonSerializer) : Support deserializing null for DateTime? fields. 
-   [JSON](http://androidapi.xamarin.com/?link=T%3aSystem.Runtime.Serialization.Json.DataContractJsonSerializer) : Fix array deserialization. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
