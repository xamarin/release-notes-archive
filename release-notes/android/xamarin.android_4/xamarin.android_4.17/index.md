---
id: 3E27E898-405F-4D0A-9DED-BCDF1B3D2EFD
title: "Xamarin.Android 4.17"
---

The Xamarin.Android 4.17 series is an alpha-only release on the
path to a future Xamarin.Android 5.0 release, providing
support for [Android Wear apps](https://developer.android.com/design/wear/structure.html) and preview bindings for [Android API-L](https://developer.android.com/preview/api-overview.html).

 **Note:** Xamarin.Android 4.17 is the first release that
requires [JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html). JDK 1.7 is required to use Wear and API-L types;
JDK 1.6 may be used with previous API levels.

 <a name="0"></a>


 <a name="Xamarin.Android_4.17.0"></a>


#  [Xamarin.Android 4.17.0](#Xamarin.Android_4.16.0)

### New Features

-  Android Wear support.
-  Bindings for API-L.


### Breaking Changes

-  The default  `//uses-sdk/@android:minSdkVersion` value in previous releases defaulted to  `$(TargetFrameworkVersion)` . It now defaults to API-11.  This change should make it easier to create new projects and deploy them to "older" devices without first visiting Project Options.




 <a name="API_Changes" class="injected"></a>


### API Changes

-  API Level 4:  [Mono.Android.dll](xamarin.android_4.14/level_4_diff/mono.android.dll) ,  [Mono.Android.GoogleMaps.dll](xamarin.android_4.14/level_4_diff/mono.android.googlemaps.dll) ,  [Mono.Android.Support.v4.dll](xamarin.android_4.14/level_4_diff/mono.android.support.v4.dll) ,  [OpenTK.dll](xamarin.android_4.14/level_4_diff/opentk.dll) ,  [OpenTK-1.0.dll](xamarin.android_4.14/level_4_diff/opentk-1.0.dll) 
-  API Level 7:  [Mono.Android.dll](xamarin.android_4.14/level_7_diff/mono.android.dll) 
-  API Level 8:  [Mono.Android.dll](xamarin.android_4.14/level_8_diff/mono.android.dll) 
-  API Level 10:  [Mono.Android.dll](xamarin.android_4.14/level_10_diff/mono.android.dll) 
-  API Level 12:  [Mono.Android.dll](xamarin.android_4.14/level_12_diff/mono.android.dll) 
-  API Level 14:  [Mono.Android.dll](xamarin.android_4.14/level_14_diff/mono.android.dll) ,  [Mono.Android.Support.v13.dll](xamarin.android_4.14/level_14_diff/mono.android.support.v13.dll) 
-  API Level 15:  [Mono.Android.dll](xamarin.android_4.14/level_15_diff/mono.android.dll) 
-  API Level 16:  [Mono.Android.dll](xamarin.android_4.14/level_16_diff/mono.android.dll) 
-  API Level 17:  [Mono.Android.dll](xamarin.android_4.14/level_17_diff/mono.android.dll) 
-  API Level 18:  [Mono.Android.dll](xamarin.android_4.14/level_18_diff/mono.android.dll) 
-  API Level 19:  [Mono.Android.dll](xamarin.android_4.14/level_19_diff/mono.android.dll)
