---
id: F6CA81AF-3D83-931F-42D5-301D889D14E3
title: "Mono For Android 4.0.0"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: If you're running Mono for Android
1.9.1 or later, you should be prompted to update. Otherwise, download [monoandroid-4.0.0.msi](http://download.xamarin.com/MonoforAndroid/Windows/monoandroid-4.0.0-r1.msi) and install.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help-&gt;Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

 **Honeycomb and Ice Cream Sandwich support**: Honeycomb (Android
v3.x) and Ice Cream Sandwich (Android v4.0) are now supported, and APIs
introduced in those API levels can now be used from C#.

 **Google Maps API bindings**: We now provide a
Mono.Android.GoogleMaps.dll assembly to allow use of the Google Maps API from
C#.

 **Reduced startup performance**. The startup overhead for the
default template has been reduced by over 50%, as measured on a Nexus One (from
2.451s to 1.141s).

 **GC Fixes**. This release contains additional GC fixes.

 **Fast Deployment**. A new Fast Deployment mode allows for
faster development times by cutting down on the time it takes to deploy your
application to an emulator or device when no resources or java stubs have
changed.

 <a name="Changes_since_1.2.0" class="injected"></a>


# Changes since 1.2.0

 **Honeycomb and Ice Cream Sandwich Support:** We are now
providing a Mono.Android.dll for API levels 12 and 14.

We have also ported Honeycomb Gallery sample.

 **Google Maps API Binding:** There is now a managed binding to
the Google Maps API that ships with Android. To use this, simply add a reference
to the Mono.Android.GoogleMaps.dll assembly. This will automatically add the
needed java library reference and the INTERNET permission to your
application.

An example project using the Google Maps API is available.

To use the GoogleMaps API, you will need to [obtain an API key](/guides/android/platform_features/maps_and_location/obtaining_a_google_maps_api_key).

 **Interface Constant Binding Improvements**: The way that
constants within Java interfaces is exposed has been overhauled. This should
simplify porting Java code which uses interface constants.

 **Improved string handling:** Extension methods are now
generated for interface methods which take [Java.Lang.ICharSequence](http://androidapi.xamarin.com/?link=T:Java.Lang.ICharSequence) and [Java.Lang.String](http://androidapi.xamarin.com/?link=T:Java.Lang.String). This allows providing [System.String](http://androidapi.xamarin.com/?link=T:System.String)-constants when invoking these interface methods.

 **Java 7 Support:** We now correctly build, sign and deploy
packages built with Java 7. Note that if you have both installed, we still will
use Java 6 as it's more tested by the Android community.

 **Smaller Application Packages:** mono.android.jar contains
Android Callable Wrappers for many types internal to Mono.Android.dll, and is
included in every Mono for Android application package. We have rearchitected
how mono.android.jar is produced, greatly shrinking its size. The size
reductions are also visible in Mono.Android.dll and application packages.

 **Better Incremental Builds:** More of the build system is
implemented as MSBuild tasks. This allows us to have better incremental builds,
letting us skip pieces that don't need to be rebuilt.

&nbsp;

<table border="0" cellpadding="1" cellspacing="10">
  <caption>
    &nbsp;
  </caption>
  <tbody>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
    </tr>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        <strong>1.2.0</strong>
      </td>
      <td>
        <strong>1.9.0</strong>
      </td>
    </tr>
    <tr>
      <td>
        First Build:
      </td>
      <td>
        8.66s
      </td>
      <td>
        8.19s
      </td>
    </tr>
    <tr>
      <td>
        Code Changes:
      </td>
      <td>
        5.78s
      </td>
      <td>
        1.71s
      </td>
    </tr>
    <tr>
      <td>
        Code Changes Requiring New Java Stubs:
      </td>
      <td>
        5.78s
      </td>
      <td>
        2.50s
      </td>
    </tr>
    <tr>
      <td>
        Resource Changes:
      </td>
      <td>
        8.18s
      </td>
      <td>
        6.10s
      </td>
    </tr>
  </tbody>
</table>

(Tests are run using the Debug profile of [JetBoy](https://github.com/xamarin/monodroid-samples).)

 **Fast Deployment**. A new Fast Deployment mode allows for
faster development times by cutting down on the time it takes to deploy your
application to an emulator or device when no resources or java stubs have
changed.

This option is enabled by default and can be toggled via the Mono for Android
Build (MD) / Mono for Android Options (VS) options panel. For an optimal use of
this mode, your assembly version (on AssemblyInfo.cs) should not be set to
automatically change on every build.

<table border="0" cellpadding="1" cellspacing="10">
  <caption>
    &nbsp;
  </caption>
  <tbody>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
    </tr>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        <strong>Normal</strong>
      </td>
      <td>
        <strong>Fast Deployment</strong>
      </td>
    </tr>
    <tr>
      <td>
        Full build and install:
      </td>
      <td>
        15.6s
      </td>
      <td>
        15.6s
      </td>
    </tr>
    <tr>
      <td>
        No changes, build and install:
      </td>
      <td>
        1.8s
      </td>
      <td>
        2.5s
      </td>
    </tr>
    <tr>
      <td>
        Resource change, build and install:
      </td>
      <td>
        10.8s
      </td>
      <td>
        10.8s
      </td>
    </tr>
    <tr>
      <td>
        Code change, build and install:
      </td>
      <td>
        14.7s
      </td>
      <td>
        3.9s
      </td>
    </tr>
  </tbody>
</table>

(Tests are run using the Debug profile of the Honeycomb Gallery sample, with
the Runtime and Platform packages already installed on an emulator running basic
api level 14.)

 **Smarter Linker:** Our linker spent the summer at linker
community college and came away a bit smarter about what your application really
needs in order to run, resulting in a significant release .apk size
reduction.

<table border="0" cellpadding="1" cellspacing="1">
  <tbody>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
      <td>
        &nbsp;
      </td>
    </tr>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        <strong>1.2.0 Size</strong>
      </td>
      <td>
        <strong>4.0 Size</strong>
      </td>
    </tr>
    <tr>
      <td>
        Default Template Release .apk
      </td>
      <td>
        4.21 MB
      </td>
      <td>
        2.8 MB
      </td>
    </tr>
  </tbody>
</table>

 **Update Notifications for Visual Studio:** Visual Studio will
now check for Mono for Android updates automatically and notify you if a new
release is available:

 ![](mono_for_android_4.0.0/Images/update1.png)

To turn this off, or to subscribe to beta release notifications, go to
Tools-&gt;Options-&gt;Mono for Android:

 ![](mono_for_android_4.0.0/Images/update2.png)

 **System.Numerics**: The System.Numerics.dll assembly is now
included with Mono for Android, bringing support for System.Numerics.BigInteger
and related types.

 **[UsesPermission] attribute:** You can now specify the Android
permissions your app requires with an assembly level attribute. This is
analogous to adding a &lt;uses-permission&gt; element to the
AndroidManifest.xml.

```
[assembly:UsesPermission (Name = Android.Manifest.Permission.Internet)]
```

 **[UsesLibrary] attribute**: You can now specify the Android
extra libraries your app requires with an assembly level attribute. This is
analagous to adding a &lt;uses-library&gt; element to the
AndroidManifest.xml.

```
[assembly:UsesLibrary (Name = "com.google.android.maps")]
```

 **Unhandled Exception Support in VS:** When you hit an unhandled
exception in your application while debugging, VS will now let you know what the
exception is instead of just stopping with a green line.

 **System.Console messages are copied to the Android Debug Log**:
Output generated to System.Console.Out and System.Console.Error are now copied
to the [Android Debug Log](/guides/android/deployment%2C_testing%2C_and_metrics/android_debug_log).

 **Java add*Listener() methods are now bound as events**. This
reduces the number of instances in which Java interfaces need to be implemented
for event handling.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  Every method that takes an (IntPtr handle) parameter has been changed to take an(IntPtr handle,  [JniHandleOwnership](http://androidapi.xamarin.com/index.aspx?link=T%3aAndroid.Runtime.JniHandleOwnership) transfer) parameter pair. This includes *all constructors* . -   Anyone using JNI and creating wrapper objects will need to update their code, probably by using  [JniHandleOwnership.DoNotTransfer](http://androidapi.xamarin.com/index.aspx?link=F%3aAndroid.Runtime.JniHandleOwnership.DoNotTransfer)  . 
-   Existing (IntPtr) constructors should be changed similar to:


 


```
//old
TypeName(IntPtr handle) : base (handle) {}
```

```
//new
TypeName(IntPtr handle, JniHandleOwnership transfer) : base(handle, transfer) {}
```

-  Java.Lang.Object.Dispose() is no longer virtual, and instead the  [IDisposable pattern](http://msdn.microsoft.com/en-us/library/system.idisposable.aspx) is propertly implemented. Developers overriding the Dispose() method should now override the Dispose(bool) method. -    *Note*  : It is  *very*  important that you update any base.Dispose() calls tobase.Dispose(disposing). Failure to do so will result in a stack overflow. Unfortunately, stack overflows aren't handled very well at present, so it will  *actually*  result in your application dying without any stack trace at all. 


 
-  Additional int to enumeration parameter and return type conversions.
-  Java event handling methods which return boolean (e.g. [android.app.Dialog.setOnKeyListener()](http://developer.android.com/reference/android/app/Dialog.html#setOnKeyListener%28android.content.DialogInterface.OnKeyListener%29) and [android.contentDialogInterface.OnKeyListener.onKey()](http://developer.android.com/reference/android/content/DialogInterface.OnKeyListener.html) ) are now mapped to events instead of properties, e.g. Android.App.Dialog.KeyPress is now an event, not a property. 
-  Enumeration types and members only exist in the API levels for which they actually exist in Java. 


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.0/level_4_diff/monoandroid.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.0/level_4_diff/opentk.dll) 
-  API Level 7:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.0/level_7_diff/monoandroid.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.0/level_7_diff/opentk.dll) 
-  API Level 8:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.0/level_8_diff/monoandroid.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.0/level_8_diff/opentk.dll) 
-  API Level 10:  [Mono.Android.dll](/guides//android_api_changes/release_4.0.0/level_10_diff/monoandroid.dll) ,  [OpenTK.dll](/guides//android_api_changes/release_4.0.0/level_10_diff/opentk.dll) 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [281](http://bugzilla.xamarin.com/show_bug.cgi?id=281) : Tie armeabi libmono to a single core. This allows apps that only bundle armeabi (and not armeabi-v7a) to safely run on SMP devices. 
-   [619](http://bugzilla.xamarin.com/show_bug.cgi?id=619) :  <span><span>LinearLayout.SetGravity( int ) should be
    GravityFlags.</span></span> 
-   [669](http://bugzilla.xamarin.com/show_bug.cgi?id=669) : EditText.ImeOptions should be of type Android.Views.InputMethods.ImeAction. 
-   [1048](http://bugzilla.xamarin.com/show_bug.cgi?id=1048) Fix that stops Visual Studio from crashing from a FormatException. 
-   [1052](http://bugzilla.xamarin.com/show_bug.cgi?id=1052) : Race condition in the VS plugin would cause an exception while deploying. 
-   [1114](http://bugzilla.xamarin.com/show_bug.cgi?id=1114) : Generate array parameters in Android Callable Wrappers. 
-   [1115](http://bugzilla.xamarin.com/show_bug.cgi?id=1115) :  <span><span>DeflateStream doesn't work</span></span> 
-   [1140](http://bugzilla.xamarin.com/show_bug.cgi?id=1140) : Embed Mono for Android version number into License.rtf. 
-   [1148](http://bugzilla.xamarin.com/show_bug.cgi?id=1148) : EditText.IOnKeyListener.OnKey keyCode parameter should be of Keycode type. 
-   [1522](http://bugzilla.xamarin.com/show_bug.cgi?id=1522) : Fix  <span><span>JNIEnv.GetArray&lt;byte&gt;(IntPtr);
    improve array marshaling support.</span></span> 
-   [1534](http://bugzilla.xamarin.com/show_bug.cgi?id=1534) Fix to stop applications from freezing up due to Garbage Collection usage 
-   [1703](http://bugzilla.xamarin.com/show_bug.cgi?id=1703) : Install License.rtf so it can be viewed after installation. 
-   [1710](http://bugzilla.xamarin.com/show_bug.cgi?id=1710) : Embed &lt;since/&gt; information in the extracted documentation. Android type and member documentation at  [http://androidapi.xamarin.com](http://androidapi.xamarin.com/) now shows the API level that the type/member was introduced, e.g. in the  **Requirements** section for the  [Android.App.Dialog](http://androidapi.xamarin.com/?link=T:Android.App.Dialog) docs, it says:  **Since:** API Level 1. 
-   [1726](http://bugzilla.xamarin.com/show_bug.cgi?id=1726) : Add events on  [Android.Animation.Animator](http://androidapi.xamarin.com/?link=T:Android.Animation.Animator/*) ,  [Android.App.ActionBar.Tab](http://androidapi.xamarin.com/?link=T%3aAndroid.App.ActionBar%2bTab/*) . 
-   [1730](http://bugzilla.xamarin.com/show_bug.cgi?id=1730) :  <span><span>ValueAnimatorRepeatMode.Infinite should not
    be an enum value</span></span> 
-   [1731](http://bugzilla.xamarin.com/show_bug.cgi?id=1731) : Preserve the  [Android.Animation.ValueAnimator.SetEvaluator](http://androidapi.xamarin.com/?link=M%3aAndroid.Animation.ValueAnimator.SetEvaluator%28Android.Animation.ITypeEvaluator%29) method in API level 14. 
-   [1733](http://bugzilla.xamarin.com/show_bug.cgi?id=1733) :  [ActionBar.LayoutParams.Gravity](http://androidapi.xamarin.com/?link=P%3aAndroid.App.ActionBar.LayoutParams.Gravity) should be of enum type. 
-   [1738](http://bugzilla.xamarin.com/show_bug.cgi?id=1738) : Java events which return boolean are transformed into events with an EventArgssubclass containing a Handled property instead of being a property. 
-   [1740](http://bugzilla.xamarin.com/show_bug.cgi?id=1740) :  [TextView.SetImeAction()](http://androidapi.xamarin.com/?link=M:Android.Widget.TextView.SetImeActionLabel) takes an enum. 
-   [1773](http://bugzilla.xamarin.com/show_bug.cgi?id=1773) : More int-&gt;enum changes. 
-   [1775](http://bugzilla.xamarin.com/show_bug.cgi?id=1775) :  [ILocationListener.OnStatusChanged()](http://androidapi.xamarin.com/?link=M%3aAndroid.Locations.ILocationListener.OnStatusChanged%28System.String%2cAndroid.Locations.Availability%2cAndroid.OS.Bundle%29) takes an enum parameter. 
-   [1776](http://bugzilla.xamarin.com/show_bug.cgi?id=1776) : Add  [Android.OS.Handler(Action&lt;Message&gt;)](http://android.xamarin.com/http%3a%2f%2fandroidapi.xamarin.com?link=C%3aAndroid.OS.Handler%28System.Action{Android.OS.Message}%29) constructor. 
-   [1781](http://bugzilla.xamarin.com/show_bug.cgi?id=1781) : Fix exception when processing [ContentProvider] attribute. 
-   [1787](http://bugzilla.xamarin.com/show_bug.cgi?id=1787) : int-&gt;enum changes. 
-   [1804](http://bugzilla.xamarin.com/show_bug.cgi?id=1804) : Add  [ItemizedOverlay.CreateItem()](http://androidapi.xamarin.com/?link=M%3aAndroid.GoogleMaps.ItemizedOverlay.CreateItem%28System.Int32%29) method. 
-   [1927](http://bugzilla.xamarin.com/show_bug.cgi?id=1927) : Better expose  [InputStream.Available()](http://androidapi.xamarin.com/?link=M%3aJava.IO.InputStream.Available) from wrappers. Add  [Stream.IsDataAvailable()](http://androidapi.xamarin.com/?link=M%3aSystem.IO.AndroidExtensions.IsDataAvailable%28System.IO.Stream%29) extension method. 
-   [2004](http://bugzilla.xamarin.com/show_bug.cgi?id=2004) : Fix execution of GLCube sample. 
-   [660400](https://bugzilla.novell.com/show_bug.cgi?id=660400) : Support jagged array types in method declarations. 
-   [691188](https://bugzilla.novell.com/show_bug.cgi?id=691188) : int-&gt;enum in Android.Media.SoundPool constructor. 
-  Correctly handle projects that do not contain Resources.
-  It should now be possible to target API level 10 (Android v2.3.3).
-  Fixed InvalidCastException that would result from subscribing to AndroidEnvironment.UnhandledExceptionRaiser. 
-  Fix End-Of-Stream translation in Android.Runtime.InputStreamAdapter and related types. 
-  Attach Mono's finalizer thread to Dalvik
-  Improve merging of [Application] attribute and &lt;application/&gt; AndroidManifest.xml element. 
-  `msbuild /t:Clean` will no longer remove the debug keystore.
-  Android.App.ActivityAttribute-related enumerations have been updated to API level 13. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
