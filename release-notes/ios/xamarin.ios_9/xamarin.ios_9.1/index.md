---
id: 77259859-F920-4E15-9421-E0ED79F54AD3
title: "Xamarin.iOS 9.1"
brief: "Xamarin's support for the iOS 9.1 Releases"
---

# Xamarin.iOS 9.1

The Xamarin.iOS 9.1.x series introduces support for Apple's iOS 9.1
	APIs and Xcode 7.1. It is based on existing [Xamarin.iOS 9.0.1](/releases/ios/xamarin.ios_9/xamarin.ios_9.0/) and 
	Mono 4.0 stable releases.

## Important Notes

Due to non-backward compatible changes in Xcode 7.x toolchain this
	version of Xamarin.iOS is only supported when used with Xcode 7.x or
	later, which requires the use Mac OSX 10.10.5 (Yosemite) or newer.

Apple releases notes contains a list of changes and pending issues
	for both [iOS 9.1](https://developer.apple.com/library/ios/releasenotes/General/RN-iOSSDK-9.1/)
	and [Xcode 7.1](https://developer.apple.com/library/ios/releasenotes/DeveloperTools/RN-Xcode/Chapters/Introduction.html)
	that you should review.



This version does **not**

 provide support for tvOS or watchOS in
	this release.
	Xamarin has previews (XI 9.3) available for both plaforms. See our [forums](http://forums.xamarin.com/categories/ios)


	for the latest information and download links.## New Features

### API bindings



There are no new frameworks in iOS 9.1. Existing frameworks were updated,
	mostly to add new API for the upcoming iPad Pro (and its optional pen)
	and LivePhotos.-  Updates to UIKit for presses, precise location (pen) and focus related API 
-  Updates to Photo[UI] frameworks for LivePhotos 
-  Updates to GameplayKit framework 


## Improvements

### Custom attributes for API availability



We added new custom attributes for API availability. The new
	types allow API to be marked for tvOS and watchOS (or any platform
	that Apple will introduce in the future). The new attributes are:-  `[Introduced]` 
-  `[Obsolete]` 
-  `[Deprecated]` 
-  `[Unavailable]` 




and the `PlatformName`

 enum currently support MacOSX,
	iOS, WatchOS and TvOS.### Binding generator support for enums



The binding generator (btouch) can now **optionally**

 process `enum`


	types inside binding files. This makes it possible to control
	code generation (e.g. with the `[Unavailable]`

 attribute)
	per platform with minimal use of conditional code and ease code sharing
	of bindings across iOS, Mac, tvOS and watchOS.

If you use this option then your bindings might duplicate
	some `enum`

 types, e.g. when used in
	both inside and outside of the binding interface files. In such cases
	you'll have to update your project to split enums into separate files. <a name="2"></a>


##  [Xamarin.iOS 9.1.0.31](#2)



This is an hotfix release.### Bug fixes

-  [watchkit] Submission rejected with "Invalid WatchKit Support" [ [#35493](https://bugzilla.xamarin.com/show_bug.cgi?id=35493) ]


 <a name="1"></a>


##  [Xamarin.iOS 9.1.0.27](#1)



This is the stable release based on Apple’s release of the Xcode 7.1
	and iOS 9.1 SDK.### Bug fixes

-  [generator] Make processing enum in binding optional [ [#35231](https://bugzilla.xamarin.com/show_bug.cgi?id=35231) ]
-  [generator] Use C# name for enum base type as MS csc does not suport .NET name [ [#35232](https://bugzilla.xamarin.com/show_bug.cgi?id=35232) ]
-  [generator] Remove UI thread checks in Photo (it was for PhotosUI) [ [#35276](https://bugzilla.xamarin.com/show_bug.cgi?id=35276) ]


 <a name="0"></a>


##  [Xamarin.iOS 9.1.0.18](#0)



This is a beta release based on Apple’s release of the Xcode 7.1
	and iOS 9.1 SDK.
	You can use this build to submit to the app store but it’s possible
	that the upcoming stable build might contains some slight differences.

This release is synchronized with Xamarin's C5SR5 (Cycle 5 Service
	Release 5) which main goal is to provide El Capitan support and fixes
	across all products.

The following document contains a complete list of the [API changes from 9.0.1 to 9.1.0](/releases/ios/api_changes/from_9.0.1_to_9.1.0)

.### El Capitan support fixes

-  [msbuild][xvs] Build C# iOS Native Library Project error [Failed to execute 'ls /usr/bin/mono': ExitStatus=1] [ [#34716](https://bugzilla.xamarin.com/show_bug.cgi?id=34716) ]
-  [msbuild][xvs] iOS Binding project fails to build after updating to Xamarin for VS 3.11.1450.0 [ [#34743](https://bugzilla.xamarin.com/show_bug.cgi?id=34743) ]


### Bug fixes

-  [corebluetooth] Add CBErrorDomain and CBATTErrorDomain support [ [#31201](https://bugzilla.xamarin.com/show_bug.cgi?id=31201) ]
-  [uikit] NSLayoutConstraint.FromVisualFormat issue [ [#34012](https://bugzilla.xamarin.com/show_bug.cgi?id=34012) ]
-  [healthkit] Expose HKErrorDomain [ [#34140](https://bugzilla.xamarin.com/show_bug.cgi?id=34140) ]
-  [foundation] Add a name for the NSURLAuthenticationChallengeSender protocol (case mismatch) [ [#34615](https://bugzilla.xamarin.com/show_bug.cgi?id=34615) ]
-  [registrar] Add support for returning delegates from methods and properties [ [#34874](https://bugzilla.xamarin.com/show_bug.cgi?id=34874) ]
