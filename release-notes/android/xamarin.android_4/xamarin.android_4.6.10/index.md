---
id: 803A73C7-8C4E-4B48-9320-14221BD27D52
title: "Xamarin.Android 4.6.10"
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

-  Generated binding files now get  `Metadata.xml` XPath info.
-  Add  `Java.Interop.Runtime.GetSurfacedObjects()` , and  `Java.Interop.Runtime.MaxGlobalReferenceCount` ,  `Java.Interop.Runtime.GlobalReferenceCount` , and  `Java.Interop.Runtime.LocalReferenceCount` properties. These are for diagnostic purposes and should not be relied upon. 
-  `$(AndroidUseLatestPlatformSdk)` : new MSBuild property; if  `True` , cause the build process to use the latest (highest numbered) Android Platform SDK. [Infrastructure]
-  Accessing the e.g.  [TextView.Text](http://androidapi.xamarin.com/?link=P%3aAndroid.Widget.TextView.Text) property getter should now dispose of the intermediate GREF. 


# Bug fixes

-  Fix preservation of  `AesCryptoServiceProvider` .
-  Add  `[Flags]` to various enumerations.
-  Generate  `XA42303` for  `[Activity(Name=".Foo")]` .
-   [360](https://bugzilla.xamarin.com/show_bug.cgi?id=360) : Generate property setters for array fields. 
-   [5980](https://bugzilla.xamarin.com/show_bug.cgi?id=5980) : Marshal non- `Java.Lang.Object` types as  `java.lang.Object` . 
-   [6459](https://bugzilla.xamarin.com/show_bug.cgi?id=6459) : Add a  `__MOBILE__`  `#define` when compiling code. 
-   [7774](https://bugzilla.xamarin.com/show_bug.cgi?id=7774) : Date property for DatePicker 
-   [8369](https://bugzilla.xamarin.com/show_bug.cgi?id=8369) : BindingsGenerator couldn't not handle ApiXmlInput containing empty spaces. 
-   [8428](https://bugzilla.xamarin.com/show_bug.cgi?id=8428) : Linker needs to preserve IntentService default constructor. 
-   [10135](https://bugzilla.xamarin.com/show_bug.cgi?id=10135) : Generate XA4207 when a C# generic class (indirectly) subclasses  `Java.Lang.Object` and uses  `[Export]` or  `[ExportField]` . 
-   [10580](https://bugzilla.xamarin.com/show_bug.cgi?id=10580) : Always preserve Mono.Runtime. 
-   [10963](https://bugzilla.xamarin.com/show_bug.cgi?id=10963) : Disable serialziation assembly generation in Release builds. 
-   [11797](https://bugzilla.xamarin.com/show_bug.cgi?id=11797) : Starter edition should support Android Library projects which use Android Resources. 
-   [12254](https://bugzilla.xamarin.com/show_bug.cgi?id=12254) : Fix event de-registration involving  `Add` and  `Remove` methods. 
-   [12370](https://bugzilla.xamarin.com/show_bug.cgi?id=12370) : Fix detection of  `dx` on Windows. 
-   [12594](https://bugzilla.xamarin.com/show_bug.cgi?id=12594) : Fix the "Build failure, register the machine, build failure" loop. 


 <a name="API_Changes" class="injected"></a>


# API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.6.10/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.6.10/level_7_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_7_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_7_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_7_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_4_diff/opentk-1.0.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.6.10/level_8_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_8_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_8_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_8_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_8_diff/opentk-1.0.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.6.10/level_10_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_10_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_10_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_10_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_10_diff/opentk-1.0.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.6.10/level_12_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_12_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_12_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_12_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_12_diff/opentk-1.0.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.6.10/level_14_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_14_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_14_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.10/level_14_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_14_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_14_diff/opentk-1.0.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.6.10/level_15_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_15_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_15_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.10/level_15_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_15_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_15_diff/opentk-1.0.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.6.10/level_16_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_16_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_16_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.10/level_16_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_16_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_16_diff/opentk-1.0.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.6.10/level_17_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.6.10/level_17_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.6.10/level_17_diff/mono.android.support.v4.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.6.10/level_17_diff/mono.android.support.v13.dll) ,  [OpenTK.dll](xamarin.android_4.6.10/level_17_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.6.10/level_17_diff/opentk-1.0.dll)
