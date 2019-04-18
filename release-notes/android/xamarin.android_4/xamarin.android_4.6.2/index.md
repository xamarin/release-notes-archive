---
id: 99EBDCE3-C330-4A77-8307-C13CB6EB756F
title: "Xamarin.Android 4.6.2"
---

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Mono for Android project. You can also check manually in Tools
&gt; Options &gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

# New Features

-  `System.Runtime.Serialization.dll` can now be used by Starter edition projects.
-  Starter addition projects can now use any assembly that is signed with the Xamarin key.
-  Xamarin.Android on OS X now installs into  `/Library/Frameworks/Xamarin.Android.framework/Versions` . Previously installed versions are moved into an appropriate subdirectory.  `/Developer/MonoAndroid` is preserved as a symlink. (Primary rationale: Xcode is prone to removing the  `/Developer/MonoAndroid` directory, which would wipe out Xamarin.Android installs.) 


# Bug fixes

-  [Android designer] Properly resize margin handles when zooming
-  Fix GC bug for objects larger than 64KB.
-   [9340](https://bugzilla.xamarin.com/show_bug.cgi?id=9340) : Debug symbols are distributed  *only* when  `$(DebugSymbols)` is  `True`  *and*  `$(DebugType)` is  `Full` . 
-   [9370](https://bugzilla.xamarin.com/show_bug.cgi?id=9370) : AndroidResource in managed library needs to prohibit uppercase names or give decent naming 
-   [9433](https://bugzilla.xamarin.com/show_bug.cgi?id=9433) : Breakpoint not hit when disable fastdebug and linking sdk assemblies only 
-   [10061](https://bugzilla.xamarin.com/show_bug.cgi?id=10061) : Toolbar buttons disabled on Windows 8 + Visual Studio 2012 
-   [10078](https://bugzilla.xamarin.com/show_bug.cgi?id=10078) : More complicated Resource designer update is required for dependencies 
-   [10127](https://bugzilla.xamarin.com/show_bug.cgi?id=10127) : WeakReference.Target can be garbage with SGEN? 
-   [10364](https://bugzilla.xamarin.com/show_bug.cgi?id=10364) : UI lockup on start debugging 
-   [10390](https://bugzilla.xamarin.com/show_bug.cgi?id=10390) : User shown INVALID workflow when they have entitlements on disk created by Visual Studio being run as Administrator. 
-   [10530](https://bugzilla.xamarin.com/show_bug.cgi?id=10530) : Package APK option disabled 
-   [10669](https://bugzilla.xamarin.com/show_bug.cgi?id=10669) : mandroid doesn't work if %CD% contains non-ASCII characters 
-   [10770](https://bugzilla.xamarin.com/show_bug.cgi?id=10770) : MakeBundleNativeCodeExternal task needs to capture and log mkbundle stdout &amp; stderr 
-   [10828](https://bugzilla.xamarin.com/show_bug.cgi?id=10828) : android-support-v4.jar should be whitelisted 
-   [10851](https://bugzilla.xamarin.com/show_bug.cgi?id=10851) : Cannot build any projects with a clean installation 
-   [10927](https://bugzilla.xamarin.com/show_bug.cgi?id=10927) : MandroidDaemon hangs 
-   [11115](https://bugzilla.xamarin.com/show_bug.cgi?id=11115) : Inspecting object in debugger throws exception. 


# API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.6.2/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.6.2/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.6.2/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.6.2/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.6.2/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.6.2/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.2/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.6.2/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.2/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.6.2/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.2/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.6.2/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.2/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.2/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.2/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.2/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.2/level_17_diff/opentk-1.0.dll) 


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
