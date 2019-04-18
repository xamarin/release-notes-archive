---
id: 5C126AA9-3331-66CB-30D5-B05C856454C9
title: "Mono For Android 4.0.4"
---

&nbsp;

 <a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Changes_since_4.0.3" class="injected"></a>


# Changes since 4.0.3

A global reference leak when marshaling exception types has been fixed.

 [Android.App.Application.SynchronizationContext](http://androidapi.xamarin.com/?link=P%3aAndroid.App.Application.SynchronizationContext). [Send()](http://androidapi.xamarin.com/?link=M%3aSystem.Threading.SynchronizationContext.Send(System.Threading.SendOrPostCallback%2cSystem.Object)) will now block until the callback has been executed,
instead of acting like [SynchronizationContext.Post()](http://androidapi.xamarin.com/?link=M%3aSystem.Threading.SynchronizationContext.Post(System.Threading.SendOrPostCallback%2cSystem.Object)).

 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_4_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_4_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_4_diff/opentk.dll) 
-  API Level 7:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_7_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_7_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_7_diff/opentk.dll) 
-  API Level 8:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_8_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_8_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_8_diff/opentk.dll) 
-  API Level 10:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_10_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_10_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_10_diff/opentk.dll) 
-  API Level 12:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_12_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_12_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_12_diff/opentk.dll) 
-  API Level 14:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.4/level_14_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.4/level_14_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.4/level_14_diff/opentk.dll) 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [2313](https://bugzilla.xamarin.com/show_bug.cgi?id=2313) : Resource name capitalization is inconsistent. 
-  Fix global reference leak in exception handling.
-  Fix SynchronizationContext.Send() so that it blocks until the message has been sent. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
