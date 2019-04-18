---
id: 1737F3E0-E5D0-D721-798B-F3B075A2CF8B
title: "Mono For Android 1.2.0"
---

&nbsp;

 **Visual Studio Users:** Download [monoandroid-1.2.0.msi](http://cdn1.xamarin.com/MonoForAndroid/monoandroid-1.2.0.msi) and install.

 **MonoDevelop Users:** You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help-&gt;Check for Updates.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

 **Garbage Collection:** There are many important bug fixes to
the garbage collector specific to Android. Every Mono for Android user is
encouraged to upgrade to this release.

 **Android SDK Fixes:** We now work around the Android SDK bug
which prevented the emulator from launching when the Android SDK directory
contained spaces.

 <a name="Changes_Since_Mono_for_Android_1.0.3" class="injected"></a>


# Changes Since Mono for Android 1.0.3

 <a name="Garbage_Collection" class="injected"></a>


## Garbage Collection

-  A significant slowdown during collection that could affect some users under some very specific cases was fixed. 
-  A bug related to object finalization and disposal was fixed.


 <a name="Visual_Studio_Add-in" class="injected"></a>


## Visual Studio Add-in

-  The Android Device Logging window (View-&gt;Other Windows-&gt;Android Device Logging) has been beefed up with features for sorting and filtering, and is automatically connected up to your device when you start debugging. 


 <a name="Runtime_Changes" class="injected"></a>


## Runtime Changes

-  Unhandled exceptions should now print a full stack trace on adb logcat, instead of silently killing the process. 


 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-   Fixed exception within Android.Runtime.JavaArray.Clear(), Android.Runtime.JavaList.Clear(), Android.Runtime.JavaSet.Clear().

 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
