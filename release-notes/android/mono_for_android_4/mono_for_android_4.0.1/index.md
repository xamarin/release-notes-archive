---
id: A75096C2-3301-BACF-D3A8-12BE8DE1B4E7
title: "Mono For Android 4.0.1"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: If you're running Mono for Android
1.9.1 or later, you should be prompted to update. Otherwise, download [monoandroid-4.0.1.msi](http://download.xamarin.com/MonoforAndroid/Windows/monoandroid-4.0.1.msi) and install.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

 **GC Stability Improvements**: We've fixed an assert within the
GC and improved stability when invoking [GC.Collect()](http://androidapi.xamarin.com/?link=M:System.GC.Collect).

 <a name="Changes_since_4.0.0" class="injected"></a>


# Changes since 4.0.0

 **UsesLibraryAttribute and UsesPermissionAttribute constructor parameters**: In 4.0.0, [UsesLibraryAttribute](http://androidapi.xamarin.com/?link=T:Android.App.UsesLibraryAttribute)and [UsesPermissionAttribute](http://androidapi.xamarin.com/?link=T:Android.App.UsesPermissionAttribute) required that you use the Name
property. Now you may use the constructor:

```
[assembly: UsesLibrary (Android.Manifest.Permission.Internet)]
```

 **Library project defines**: Library projects now get the same
set of __ANDROID__ defines as Application projects.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  Additional int to enumeration parameter and return type conversions.


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_4_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_4_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_4_diff/opentk.dll) 
-  API Level 7:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_7_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_7_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_7_diff/opentk.dll) 
-  API Level 8:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_8_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_8_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_8_diff/opentk.dll) 
-  API Level 10:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_10_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_10_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_10_diff/opentk.dll) 
-  API Level 12:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_12_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_12_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_12_diff/opentk.dll) 
-  API Level 14:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.1/level_14_diff/monoandroid.dll) ,  [Mono.Android.GoogleMaps.dll](/guides//android_api_changes/release_4.0.1/level_14_diff/mono.android.googlemaps.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.1/level_14_diff/opentk.dll) 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [2091](http://bugzilla.xamarin.com/show_bug.cgi?id=2091) :  <span><span>Assertion at
    ../../../../mono/metadata/sgen-bridge.c:426, condition
    `!entry-&gt;is_bridge' not met</span></span> 
-   [2137](http://bugzilla.xamarin.com/show_bug.cgi?id=2137) :  <span><span>Provide ANDROID defines for class
    libraries</span></span> 
-   [2206](http://bugzilla.xamarin.com/show_bug.cgi?id=2206) :  <span><span>DataContractJsonSerializer does not
    work</span></span> 
-   [2326](http://bugzilla.xamarin.com/show_bug.cgi?id=2326) :  <span><span>Calling GC.Collect() repeatedly hangs
    app</span></span> 
-   [2349](http://bugzilla.xamarin.com/show_bug.cgi?id=2349) :  <span><span>Assertion at
    ../../../../mono/metadata/sgen-bridge.c:426, condition
    `!entry-&gt;is_bridge' not met</span></span> 
-   [2367](http://bugzilla.xamarin.com/show_bug.cgi?id=2367) :  <span><span>Invalid Java generated for constructors that
    call base with different parameters</span></span> 
-  Fixed java.lang.NoClassDefFoundError when creating arrays of various types. 
-  The &lt;AndroidResgenFile/&gt; element no longer requires a directory to be specified. 
-  Several Android Callable Wrapper constructor generation fixes.


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
