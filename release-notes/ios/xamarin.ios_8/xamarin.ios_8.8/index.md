---
id: 4A0E7C95-F691-45BD-90D7-78BC429EF91B
title: "Xamarin.iOS 8.8"
---

# Xamarin.iOS 8.8



The Xamarin.iOS 8.8 releases adds support for Apple's 
	iOS 8.2 APIs (including the	new [WatchKit](https://developer.apple.com/watchkit/)

 
	framework) and Xcode 6.2.### Major features

-  Adds new iOS 8.2 API and Xcode 6.2 support; 
-  Support for the  [WatchKit.framework](https://developer.apple.com/watchkit/) 


 <a name="2"></a>


##  [Xamarin.iOS 8.8.2](#2)

Xamarin.iOS 8.8.2 is a service release including important fixes to
	the current stable release. There is no API change in this release.

## Bug fixes

-  [runtime] Fix random crash due to threading issue in new threadpool heuristics code [#26307]
-  [msbuild] Add the 'UIRequiredDeviceCapabilities' array (with 'watch-companion') for watchkit extensions [#28078]
-  [msbuild] Add missing files to allow support for WatchKit physical devices (8.8.2.3+) [#28324]
-  [runtime] Avoid use of internal types in WatchKit extension startup code (8.8.2.4+) [#28609]


 <a name="1"></a>


##  [Xamarin.iOS 8.8.1](#1)

Xamarin.iOS 8.8.1 is a service release including important fixes to
	the current stable release. There is no API change in this release.

## Bug fixes

-  [aot] Fixed full AOT crash (Instructions.cpp:281) that can affect F# [#26346]
-  [aot] Fixed copying non-metadata strings in MONO_PATCH_INFO_LDSTR_LIT [#26989]
-  [sgen] Fixed bug in 64 bit LOS cardtable scanning [#27147]
-  [arm64] Added support for byref vtypes returns to the dyn call code [#27201]
-  [coremedia] Fixed CMFormatDescription.Create(IntPtr) to assume owns=false [#27205]
-  [arm64] Fixed mini-arm64-gsharedvt.c:91 assertion [#27244]


 <a name="0"></a>


##  [Xamarin.iOS 8.8.0](#0)



Xamarin.iOS 8.8.0 adds support for Apple's 
	iOS 8.2 APIs (including the	new [WatchKit](https://developer.apple.com/watchkit/)

 
	framework) and Xcode 6.2, while it remains identical to the current [8.6.3](xamarin.ios_8.6)


	stable release in other aspects.The following document contains a list of the API changes from [API changes from 8.6.3 to 8.8.0](/releases/ios/api_changes/from_8.6.3_to_8.8.0).

### Enhancements

-  [corefoundation] Added bindings for  `CFNotificationCenter` to ease communication between the host application and the watch extension;  
-  [externalaccessory] Added missing EAWiFiUnconfiguredAccessoryBrowser.ConfigureAccessory [#26610]


### Bug fixes

-  [objcruntime] Fix Runtime.ConnectMethod in the new registrars [#24861]


### Important Notes



Apple Xcode 6.2 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite).Apple releases notes contains a list of changes and known issues for both [iOS 8.2](https://developer.apple.com/library/ios/releasenotes/General/RN-iOSSDK-8.2/index.html)
	and [Xcode 6.2](https://developer.apple.com/library/ios/releasenotes/DeveloperTools/RN-Xcode/Chapters/Introduction.html)
	that you should review.

Older release notes for the beta/previews versions of
	Xamarin.iOS WatchKit support can be read from the [8.7 release notes page](xamarin.ios_8.7).
