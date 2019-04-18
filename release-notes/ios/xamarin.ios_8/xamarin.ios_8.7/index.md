---
id: 4A0E7C95-F691-45BD-90D7-78BC429EF91B
title: "Xamarin.iOS 8.7"
---

# Xamarin.iOS 8.7



The Xamarin.iOS 8.7 **preview**

 releases adds support for Apple's 
	iOS 8.2 APIs (including the	new [WatchKit](https://developer.apple.com/watchkit/)

 
	framework) and Xcode 6.2, while it remains identical to the current [8.6.x](xamarin.ios_8.6)


	stable release in other aspects.### Important Notes



Apple Xcode 6.2 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite).Apple releases notes contains a list of changes and known issues for both [iOS 8.2](https://developer.apple.com/library/prerelease/ios/releasenotes/General/RN-iOSSDK-8.2/index.html)
	and [Xcode 6.2](http://adcdownload.apple.com//Developer_Tools/Xcode_6.2_beta_5/Xcode_6.2_beta_5_Release_Notes.pdf)
	that you should review.

You need to [install a special build of Xamarin Studio 5.7 to build and launch WatchKit applications](/guides/ios/watch/installation/).

 <a name="2"></a>


#  [Xamarin.iOS 8.7.2](#2)

This third release match the tools and API provided with Xcode 6.2 **beta 5** and iOS 8.2 **beta 5** and includes the fixes of
	the second service release of XI 8.6 (8.6.2).

The following document contains a list of the API changes from [API changes from 8.6.2 to 8.7.2](/releases/ios/api_changes/from_8.6.2_to_8.7.2).

### Enhancements

-  [watchkit] Added WKInterfaceController.AddMenuItem overloads using System.Action
-  [watchkit] WKInterfaceController methods documented to be called from the main thread will now throw a managed exception if called from a background thread


### Bug fixes

-  [objcruntime] Fix Runtime.ConnectMethod in the new registrars [#24861]


 <a name="1"></a>


#  [Xamarin.iOS 8.7.1](#1)

This second release match the tools and API provided with Xcode 6.2 **beta 5** and iOS 8.2 **beta 5**.

The following document contains a list of the API changes from [API changes from 8.6.0 to 8.7.1](/releases/ios/api_changes/from_8.6.0_to_8.7.1).

### Enhancements

-  Added bindings for  `CFNotificationCenter` to ease communication between the host application and the watch extension; 


 <a name="0"></a>


#  [Xamarin.iOS 8.7.0](#0)

This first release match the tools and API provided with Xcode 6.2 **beta 4** and iOS 8.2 **beta 4**.

The following document contains a list of the API changes from [API changes from 8.6.0 to 8.7.0](/releases/ios/api_changes/from_8.6.0_to_8.7.0).

### Major features

-  Adds new iOS 8.2 API and Xcode 6.2 support; 
-  Support for the  [WatchKit.framework](https://developer.apple.com/watchkit/) 


### Known Issues

-  **Can't launch application on Watch simulator.** This seems to be an issue with the iOS Simulator hanging when trying to install an app that has changed. Xcode release notes (beta 4) includes a similar known issue:  *If the issue persists, reset the Simulator (iOS Simulator > Reset Content and Settings...)*
