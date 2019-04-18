---
id: C10B3CD2-1D87-4756-AFC0-BF78E41F3BF4
title: "Xamarin.Android 4.6.8"
---

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Xamarin.Android project. You can also check manually in Tools
&gt; Options &gt; Xamarin.Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

# New Features

-  Updated  `Mono.Android.Support.v4.dll` and  `Mono.Android.Support.v13.dll` to bind the  [Android Support Library](http://developer.android.com/tools/extras/support-library.html) , revision 13.
-  The Mono runtime is now built with the  [Android NDK](http://developer.android.com/tools/sdk/ndk/index.html) , revision 8e


# Bug fixes

-  Fix installation of the Visual Studio add-on when Visual Studio is installed into a non-default location. 
-   [11051](https://bugzilla.xamarin.com/show_bug.cgi?id=11051) : Provide non-exceptional error messages for ACW generation. 
-   [11950](https://bugzilla.xamarin.com/show_bug.cgi?id=11950) : Properly handle null array fields. 
-   [12432](https://bugzilla.xamarin.com/show_bug.cgi?id=12432) : Don't indiscriminately touch values.xml. 
-   [12479](https://bugzilla.xamarin.com/show_bug.cgi?id=12479) : Fix lref leak in  `JNIEnv.NewArray(Array, Type)`
