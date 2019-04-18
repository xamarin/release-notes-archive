---
id: AEED9C4E-02FB-4285-93E3-41F8B93691BB
title: "Xamarin.Android 4.6"
---

<a name="Installation" class="injected"></a>


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

 <a name="New_Features" class="injected"></a>


# New Features

-  New product name:  **Xamarin.Android** .
-  New License Editions -   Free Starter edition supports app packaging store deployment for applications up to 10KB in size.


 
-  AIDL support.
-  Environment information can be embedded into the  `.apk` . -   Allows setting diagnostic system properties or environment variables during process startup
-   New  `AndroidEnvironment`  build action.


 
-  New  `EmbeddedNativeLibrary`  **Build action** which causes native libraries ( `.so` files) to be embedded into assemblies. 
-  [DLL Mapping information](http://mono-project.com/DllMap) (within  `.dll.config` files) will now be automatically included into app packages. 
-  The OS X installer is now signed.


 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  GC bugfix for arrays of structs of a certain (unlikely) layout?
-  Sign Xamarin.Android SDK assemblies
-   [Expose](http://forums.xamarin.com/discussion/762/phonenumberformattingtextwatcher)  [PhoneNumberFormattingTextWatcher](http://androidapi.xamarin.com/?link=T%3aAndroid.Telephony.PhoneNumberFormattingTextWatcher) . 
-  Support  [PermissionAttribute.ProtectionLevel](http://androidapi.xamarin.com/?link=P%3aAndroid.App.PermissionAttribute.ProtectionLevel) . 
-  Support  `[OnSerializing]` in  `System.Runtime.Serialization.Json.dll` .  [[Context]](http://stackoverflow.com/questions/13362906/onserializing-method-not-called-in-mono-3-0-1) 
-  Fix accessibility of  [ClientBase&lt;TChannel>.ChannelBase&lt;T>](http://androidapi.xamarin.com/?link=T%3aSystem.ServiceModel.ClientBase%601.ChannelBase%601) .  [[Context]](http://stackoverflow.com/questions/13389652/how-to-override-clientbase-createchannel-in-mono-on-ios)                                                               
-   [1446](https://bugzilla.xamarin.com/show_bug.cgi?id=1446) :  `Mono.Debugger.Soft.ObjectCollectedException` : The requested operation cannot be completed because the object has been garbage collected. 
-   [1873](https://bugzilla.xamarin.com/show_bug.cgi?id=1873) : Regression:  `Mono.Debugging.Evaluation.EvaluatorException` : Method ` `.ctor` ' not found in type ` `CollectionDebuggerView`1` '. 
-   [2246](https://bugzilla.xamarin.com/show_bug.cgi?id=2246) : Exception when SDB calls  `ToString()` on an object. 
-   [2456](https://bugzilla.xamarin.com/show_bug.cgi?id=2456) : Resources do not get created when a user name contains @ character. 
-   [3276](https://bugzilla.xamarin.com/show_bug.cgi?id=3276) : Mono implementation of  `HttpWebRequest` eats the body of a DELETE request. 
-   [3477](https://bugzilla.xamarin.com/show_bug.cgi?id=3477) : native library ABI is now resolved based on Link, then ItemSpec. 
-   [3531](https://bugzilla.xamarin.com/show_bug.cgi?id=3531) :  `GlCullFace` ( `GL_CULL_FACE` ) is missing from  `Javax.Microeditions.Khronos.Opengles.GL10` . 
-   [4642](https://bugzilla.xamarin.com/show_bug.cgi?id=4642) : Sometimes things are rebuilt that aren't out of date. 
-   [4904](https://bugzilla.xamarin.com/show_bug.cgi?id=4904) : Improve  `managedReturn` support for  `.jar` binding. 
-   [5146](https://bugzilla.xamarin.com/show_bug.cgi?id=5146) : Linking issue when 2 applications share a project reference 
-   [5240](https://bugzilla.xamarin.com/show_bug.cgi?id=5240) : Binding output generates MSBuild-parseable error messages. 
-   [5397](https://bugzilla.xamarin.com/show_bug.cgi?id=5397) : Support registering the same ACW multiple times. 
-   [6312](https://bugzilla.xamarin.com/show_bug.cgi?id=6312) :  `System.Net.NetworkInformation.Ping.Send()` throws  `InvalidOperationException` . 
-   [6567](https://bugzilla.xamarin.com/show_bug.cgi?id=6567) : error MSB6006: "generator.exe" exited with code -532462766. 
-   [7258](https://bugzilla.xamarin.com/show_bug.cgi?id=7258) :  `WebRequest.DefaultWebProxy` with credentials fails. 
-   [7459#c2](https://bugzilla.xamarin.com/show_bug.cgi?id=7459#c2) : Invoke  `Java.Lang.__TypeRegistrations.RegisterPackages()` for additional framework assemblies. 
-   [7505](https://bugzilla.xamarin.com/show_bug.cgi?id=7505) (partial): Add diagnostic output in ResolveAssemblies assembly resolution hiearchy, i.e. "why is assembly A.dll being referenced?!". 
-   [7580](https://bugzilla.xamarin.com/show_bug.cgi?id=7580) : Binding a jar produces a casting error that can't be fixed with Metadata. 
-   [7599](https://bugzilla.xamarin.com/show_bug.cgi?id=7599) :  `HttpWebRequest` returns 404 because it reuses an old connection to a previous server. 
-   [7637](https://bugzilla.xamarin.com/show_bug.cgi?id=7637) :  `HttpWebRequest.BeginGetResponse()` hangs when send request stream is empty 
-   [7692](https://bugzilla.xamarin.com/show_bug.cgi?id=7692) :  <span id="short_desc_nonedit_display">Mono for Android is not detected by Studio.</span> 
-   [7762](https://bugzilla.xamarin.com/show_bug.cgi?id=7762) : Jmdns binding issue 
-   [7772](https://bugzilla.xamarin.com/show_bug.cgi?id=7772) : Add  `Dialog.FindViewById<T>(int)` ,  `Window.FindViewById<T>(int)` . 
-   [7865](https://bugzilla.xamarin.com/show_bug.cgi?id=7865) : Add  [UsesFeatureAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.UsesFeatureAttribute) . 
-   [7919](https://bugzilla.xamarin.com/show_bug.cgi?id=7919) : [Windows 7 and 8] The application does not builds successfully. 
-   [7957](https://bugzilla.xamarin.com/show_bug.cgi?id=7957) :  `System.Xml.XmlException` : 'Text' is an invalid node type. 
-   [7966](https://bugzilla.xamarin.com/show_bug.cgi?id=7966) :  `TimeZoneInfo.FindSystemTimeZoneById()` returns  `null` > 
-   [7969](https://bugzilla.xamarin.com/show_bug.cgi?id=7969) : do not generate overrides when it shouldn't for method variant property. 
-   [7973](https://bugzilla.xamarin.com/show_bug.cgi?id=7973) : Add  [ApplicationAttribute.LargeHeap](http://androidapi.xamarin.com/?link=P%3aAndroid.App.ApplicationAttribute.LargeHeap) property. 
-   [8072](https://bugzilla.xamarin.com/show_bug.cgi?id=8072) :  `WeakReference.Target` should return  `null`  `InvalidOperationException` after target has been collected. 
-   [8112](https://bugzilla.xamarin.com/show_bug.cgi?id=8112) : Unable to generate bindings for DroidText: Can't implement  `IComparable` . 
-   [8137](https://bugzilla.xamarin.com/show_bug.cgi?id=8137) : Add  `$(JavaOptions)` ,  `$(JavaMaximumHeapSize)` MSBuild properties. 
-   [8226](https://bugzilla.xamarin.com/show_bug.cgi?id=8226) : Properly bind Java  `@Override final` methods. 
-   [8242](https://bugzilla.xamarin.com/show_bug.cgi?id=8242) : Add  [SupportsGLTextureAttribute](http://androidapi.xamarin.com/?link=T%3aAndroid.App.SupportsGLTextureAttribute) . 
-   [8320](https://bugzilla.xamarin.com/show_bug.cgi?id=8320) : Runtime metadata bug with RX. 
-   [8339](https://bugzilla.xamarin.com/show_bug.cgi?id=8339) : Disable Compiler Warnings in generated code. 
-   [8376](https://bugzilla.xamarin.com/show_bug.cgi?id=8376) : Support Android Resource Aliases. 
-   [8406](https://bugzilla.xamarin.com/show_bug.cgi?id=8406) : If activation app fails, error message from installer is cryptic. 
-   [8559](https://bugzilla.xamarin.com/show_bug.cgi?id=8559) :  `TaskScheduler` passed with parallel options to  `Parallel.ForEach()` not used correctly. 
-   [8781](https://bugzilla.xamarin.com/show_bug.cgi?id=8781) : Publish Android Application not creating an APK. 
-   [9193](https://bugzilla.xamarin.com/show_bug.cgi?id=9193) : XmlSerialization not properly deserializing a List. 
-   [9340#c9](https://bugzilla.xamarin.com/show_bug.cgi?id=9340#c9) : Don't use  `aapt --debug-mode` . Don't ignore the  `//application/@android:debuggable` attribute in  `AndroidManifest.xml` . 
-   [9395](https://bugzilla.xamarin.com/show_bug.cgi?id=9395) : Resource LIbrary Id's. 
-   [9531](https://bugzilla.xamarin.com/show_bug.cgi?id=9531) : Segfault in fieldref_encode_signature. 
-   [9669](https://bugzilla.xamarin.com/show_bug.cgi?id=9669) : Publish Application in Visual Studio does not use the keystore key. 
-   [9696](https://bugzilla.xamarin.com/show_bug.cgi?id=9696) : Cannot bind library due to reference assembly already being used in an assembly. 
-   [9768](https://bugzilla.xamarin.com/show_bug.cgi?id=9768) : Enum binding mismatch?  `Android.Views.InputMethods.InputMethodManager.ToggleSoftInputFromWindow` . 
-   [585577](https://bugzilla.novell.com/show_bug.cgi?id=585577) :  `BindingSource` / `BindingList` do not hook to  `PropertyNotified` event of  `INotifyPropertyChanged` data sources. 


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.6/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.6/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.6/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.6/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.6/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.6/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.6/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.6/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.6/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6/level_17_diff/opentk-1.0.dll) 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
