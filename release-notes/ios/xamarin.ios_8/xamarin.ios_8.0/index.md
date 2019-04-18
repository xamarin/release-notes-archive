---
id: 9E994372-5272-4D82-AE33-1659596A3A84
title: "Xamarin.iOS 8.0"
---

# Xamarin.iOS 8.0



The Xamarin.iOS 8.x series introduces support for Apple's iOS 8.0 APIs.
	This version is based on the final release of Apple's Xcode 6 and
	includes support for the iOS8 SDK API.

Check
	our [Introduction to iOS 8.0](http://developer.xamarin.com/guides/ios/platform_features/introduction_to_ios_8/)

 to learn about the new features introduced.

Xamarin.iOS 8.0 is based on the recently release [7.4 version](../../xamarin.ios_7/xamarin.ios_7.4)

 with an [updated (3.6) VS support](../../../vs/xamarin.vs_3/xamarin.vs_3.6)

 and a [new Xamarin Studio (5.4)](../../../studio/xamarin.studio_5.4/xamarin.studio_5.4)


	to add IDE support for the new iOS 8 features.

For references the release notes for the Xamarin.iOS 7.9.x previews
	(iOS 8 betas) are available [here](../../xamarin.ios_7/xamarin.ios_7.9)

.## Major features

### New iOS 8.0 API



We have bound the new iOS 8 APIs for you, both the
	improvements to the existing frameworks as well as bindings
	for the new and exciting iOS 8 frameworks (AVKit, CloudKit,
	CoreAudioKit, HealthKit, HomeKit, LocalAuthentication, Metal,
	NotificationCenter, Photos, PhotosUI, SceneKit, WebKit)Several existing frameworks were also enhanced with new types
	and API.
	The following document contains a list of the API changes from [API changes from 7.4 to 8.0](/releases/ios/api_changes/from_7.4.0_to_8.0.0).

### Xcode 6.0 support



This release adds support for Apple Xcode 6.0.  All new
	iOS8 features require Xcode 6 (or later) to work.  Earlier
	versions of Xcode (5.x) are supported but Apple do require
	using the latest stable Xcode and SDK to publish to the App
	Store.## Enhancements

-  [mtouch] Add support for selecting simulator by UDID, allowing the use of the new iPhone6 and iPhone6 Plus simulators; 
-  [fsharp] Added F# assemblies to the unified API; 
-  Updated  [unified](/guides/cross-platform/macios/unified/) support to include the new iOS8 API; 
-  `xbuild` is now used to build new iOS8 projects (along with unified projects). 


## Bug fixes

-  [msbuild] Fix Starter/Indeix builds using  `xbuild` [#22556] 
-  [uikit] Fix (beta only regression) GetSupportedInterfaceOrientations [#22899] 
-  [aot] Only AOT-compile the ABIs for each target [#22933] 
-  [unified] NMath.Min incorrect implementation [#22957] 
-  [security] Fix mutating method sent to immutable object (&lt; iOS7) [desk #83099] 
-  [runtime] Add support for objects posing as instances of other types [desk #86994] 
-  [llvm] Some ARM64 fixes (unified) for the LLVM backend 


## Important Notes

Apple Xcode 6 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite). 
	Earlier versions, e.g. OSX 10.8 (Mountain Lion), are **not** supported.

Apple releases notes contains a list of changes and known issues for both [iOS 8](https://developer.apple.com/library/prerelease/ios/releasenotes/General/RN-iOSSDK-8.0/)
	and [Xcode 6](http://adcdownload.apple.com//Developer_Tools/xcode_6_beta_7_apzr94/xcode_6__beta_7_release_notes.pdf)
	that you should review.

## Known Issues

Using the iOS 7.0 and 7.1 simulators included with Xcode 6 is not currently supported. The issue is being tracked in [bug 22750](https://bugzilla.xamarin.com/show_bug.cgi?id=22750) and will be fixed in the 8.2.0 release.
