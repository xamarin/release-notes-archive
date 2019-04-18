---
id: C1966BC9-78B8-40D0-8E36-4ACE720D3E47
title: "Xamarin.iOS 8.9"
---

# Xamarin.iOS 8.9



The Xamarin.iOS 8.9 releases adds support for Apple's 
	iOS 8.3 APIs and Xcode 6.3, while it remains identical to the current [8.8.x](/releases/ios/xamarin.ios_8/xamarin.ios_8.8)

 
	stable release in other aspects.### Major features

-  Adds new iOS 8.3 API and Xcode 6.3 support; 


### Important Notes



Apple Xcode 6.3 requires Mac OSX 10.10 (Yosemite).Apple releases notes contains a list of changes and known issues for both [iOS 8.3](https://developer.apple.com/library/ios/releasenotes/General/RN-iOSSDK-8.3/index.html)
	and [Xcode 6.3](https://developer.apple.com/library/ios/releasenotes/DeveloperTools/RN-Xcode/Chapters/Introduction.html)
	that you should review.

 <a name="1"></a>


#  [Xamarin.iOS 8.9.1](#1)

This release is the **stable** release that match the tools 
	and API provided with final releases of Xcode 6.3 and iOS 8.3.

The following document contains a list of the API changes from [API changes from 8.8.0 to 8.9.1](/releases/ios/api_changes/from_8.8.0_to_8.9.1). It is identical to the API that
	was shipped with our 8.9.0 preview.

 <a name="0"></a>


#  [Xamarin.iOS 8.9.0](#0)

This first release is a **preview** that match the tools and API 
	provided with Xcode 6.3 **beta 4** and iOS 8.3 **beta 4**.

The following document contains a list of the API changes from [API changes from 8.8.0 to 8.9.0](/releases/ios/api_changes/from_8.8.0_to_8.9.0).

### Known Issues

-  An iOS bug, affecting only on ARM64, might cause issues with MemoryMapFile [#27667] [radar 20095231]
-  Apple introduced a breaking change when it changed CMAttitudeReferenceFrame enum definition [radar 20295259]
