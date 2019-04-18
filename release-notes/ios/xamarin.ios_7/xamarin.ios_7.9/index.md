---
id: E7B7FE5F-12FB-4348-8192-27489D2C6CEA
title: "Xamarin.iOS 7.9"
brief: "Xamarin's support for the iOS 8 Beta Releases"
---

# Xamarin.iOS 7.9



The Xamarin.iOS 7.9.x series is based on our latest release (7.4.0)
	and introduces support for Apple's iOS 8.0 APIs.

These versions are designed to rapidly track the changes on
	Apple's iOS 8 betas and have the same limitations and API
	guarantees that a standard Apple iOS beta has.   APIs will
	change and will be updated continuously as the beta process
	moves.## Important Notes

Apple Xcode 6 beta requires Mac OSX 10.9.3+ (Mavericks) or 10.10 (Yosemite). 
	OSX 10.8 (Mountain Lion) is **not** supported.

Apple releases notes contains a list of changes and pending issues for both [iOS 8](https://developer.apple.com/library/prerelease/ios/releasenotes/General/RN-iOSSDK-8.0/)
	and [Xcode 6](https://developer.apple.com/library/prerelease/ios/releasenotes/DeveloperTools/RN-Xcode/xc6_release_notes/xc6_release_notes.html)
	that you should review.

# Xamarin iOS 7.9.4



The biggest change in this update is that it was rebased on 
	the [Xamarin 7.4.0](xamarin.ios_7.4)

 release (including
	the update to Mono 3.8). Previous 7.9.x releases were based on [Xamarin 7.2.6](xamarin.ios_7.2#6)

.

It also targets Xcode 6 beta 6 (new) and iOS 8 beta 5 
	(unchanged) since beta 6 was not released to developers.The following document contains a list of the iOS [API changes from 7.9.3 to 7.9.4](/releases/ios/api_changes/from_7.9.3_to_7.9.4).
	A list of the BCL [API changes from 7.2.6 to 7.4.0](/releases/ios/api_changes/from_7.2.6_to_7.4.0) is also available.

# Xamarin iOS 7.9.3



This update includes more bindings and API enhancements
	for iOS 8 beta 5.The following documents contains a list of the [API changes from 7.9.2 to 7.9.3](/releases/ios/api_changes/from_7.9.2_to_7.9.3).



Note: Xcode 6 beta 5 seems to have fixed the remaining issues
	(e.g. timeouts) when starting applications on the simulators# Xamarin iOS 7.9.2



This update includes several more bindings and API enhancements
	for iOS 8 beta 4.The following documents contains a list of the [API changes from 7.2.6 to 7.9.2](/releases/ios/api_changes/from_7.2.6_to_7.9.2) and [API changes from 7.9.1 to 7.9.2](/releases/ios/api_changes/from_7.9.1_to_7.9.2).



Note: Using the iOS designer, from Visual Studio, has
	some issues when using Xcode 6 beta 4.# Xamarin iOS 7.9.1



This update includes several more bindings and API enhancements
	for iOS 8 beta 2.The following documents contains a list of the [API changes from 7.2.6 to 7.9.1](/releases/ios/api_changes/from_7.2.6_to_7.9.1) and [API changes from 7.9.0 to 7.9.1](/releases/ios/api_changes/from_7.9.0_to_7.9.1).

# Xamarin iOS 7.9.0



This version is focused on the initial support of iOS 8
	Beta 2 and contains the following elements:-  iOS Designer support: you will need to update Xamarin Studio and Visual Studio to their Alpha components to be able to use the iOS Designer with the Xcode6-Beta2 
-  APIs: About 70% of the new APIs have been turned into idiomatic strongly-typed APIs with support for Async and events where appropriate. 




The following are the known limitations of this release:The following document contains a list of the [API changes from 7.2.6 to 7.9.0](/releases/ios/api_changes/from_7.2.6_to_7.9.0)

# Known Issues in 7.9.xx

Some features are not implemented in the current versions of
	Xamarin Studio. E.g.

-  iOS 8 Extensions: while the APIs are in place, the IDE support to package them is not. But it is still possible to create those with command line tools. 
-  SceneKit assets: there is no built-in support in the IDEs to compile SceneKit assets for you. You will have to manually invoke scntool in your custom build steps to support it. 
-  Debugging of extensions: not currently supported out of the box on the IDE.
