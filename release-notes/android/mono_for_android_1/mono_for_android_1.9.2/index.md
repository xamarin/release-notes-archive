---
id: 2F1B50A4-4A92-7804-7041-2CA7256C831D
title: "Mono For Android 1.9.2"
---

&nbsp;

This is a ** *preview*** release for the 2.0 series. If
you are feeling adventurous, try it out and file bugs if anything goes wrong. If
you find something that impedes your work, you can uninstall this release and
the shared runtime / platform packages on your Android device, and reinstall [Mono for Android 1.2](/releases/android/mono_for_android_1/mono_for_android_1.2.0).

 <a name="Installation:" class="injected"></a>


# Installation:

 **Visual Studio Users:** Download [monoandroid-1.9.2.msi](http://download.xamarin.com/MonoforAndroid/Windows/monoandroid-1.9.2.msi) and install.

 **MonoDevelop Users:** To be prompted about beta updates, go to
Help-&gt;Check for Updates and set the Update Level to Beta. You should be
prompted with beta updates.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

This release features the following major highlights:

-  Ice Cream Sandwich Support (Android v4.0) -   New APIs supported 
-   Fixed to support Google's JNI breaking changes


 
-  Google Maps API bindings -    [Obtaining a Maps API key](/guides/android/platform_features/maps_and_location/obtaining_a_google_maps_api_key)  


 
-  System.Numerics is now part of Mono for Android -   Complex data type 
-   BigInteger data type.


 
-  Assembly Attributes for: -   Declaratively listing required Android permissions 
-   Declaratively request dependencies on libraries


 
-  Unhandled Exception Support in Visual Studio
-  System.Console output is redirected to the Android Debug Log


In addition, these are the new features since Mono for Android 1.2, for
details see the 1.9.0 and 1.9.1 release notes.

-  Honeycomb Support (Android 3.x)
-  Smarter linker produces smaller executables
-  Updated notifications for Visual Studio
-  Java 7 support
-  Incremental builds
-  Listener classes are mapped to C# events


 <a name="Changes_Since_Mono_for_Android_1.9.1" class="injected"></a>


# Changes Since Mono for Android 1.9.1

-  See 1.9.0 Release Notes for changes since 1.2.0.
-  See 1.9.1 Release Notes for changes since 1.9.0.


 **Ice Cream Sandwich Support (Android v4.0)**: Mono.Android.dll
is now provided for API level 14, allowing targeting of ICS devices.

 **Google Maps API Binding:** There is now a managed binding to
the Google Maps API that ships with Android. To use this, simply add a reference
to the Mono.Android.GoogleMaps.dll assembly. This will automatically add the
needed java library reference and the INTERNET permission to your
application.

An example project using the Google Maps API is available [here].

 **[UsesPermission] attribute:** You can now specify the Android
permissions your app requires with an assembly level attribute. This is
analogous to adding a &lt;uses-permission&gt; element to the
AndroidManifest.xml.

```
[assembly:UsesPermission (Android.Manifest.Permission.Internet)]
```

 **[UsesLibrary] attribute**: You can now specify the Android
extra libraries your app requires with an assembly level attribute. This is
analagous to adding a &lt;uses-library&gt; element to the
AndroidManifest.xml.

```
[assembly:UsesLibrary ("com.google.android.maps")]
```

 **Unhandled Exception Support in VS:** When you hit an unhandled
exception in your application while debugging, VS will now let you know what the
exception is instead of just stopping with a green line.

 **System.Console messages are copied to the Android Debug Log**:
Output generated to System.Console.Out and System.Console.Error are now copied
to the [Android Debug Log](/guides/android/deployment%2C_testing%2C_and_metrics/android_debug_log).

 **System.Numerics.dll has been added to the Mono for Android profile**.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  Every method that takes an (IntPtr handle) parameter has been changed to take an(IntPtr handle,  [JniHandleOwnership](http://androidapi.xamarin.com/index.aspx?link=T%3aAndroid.Runtime.JniHandleOwnership) transfer) parameter pair. This includes *all constructors* . Anyone using JNI and creating wrapper objects will need to update their code, probably by using  [JniHandleOwnership.DoNotTransfer](http://androidapi.xamarin.com/index.aspx?link=F%3aAndroid.Runtime.JniHandleOwnership.DoNotTransfer) . 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-  Android.App.ActivityAttribute-related enumerations have been updated to API level 13. 
-   [1115](http://bugzilla.xamarin.com/show_bug.cgi?id=1115) :  <span><span>DeflateStream doesn't work</span></span> 
-   [660400](https://bugzilla.novell.com/show_bug.cgi?id=660400) : Support jagged array types in method declarations. 
-  Improve merging of [Application] attribute and &lt;application/&gt; AndroidManifest.xml element. 
-  `msbuild /t:Clean` will no longer remove the debug keystore.


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
