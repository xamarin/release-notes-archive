---
id: 265E8C2D-37EA-4588-940C-22221283D944
title: "Xamarin.iOS 11.6"
---

# Xamarin.iOS 11.6
Last Update: 1/23/2018 [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)

 [What's New](#Whats_New_in_this_Release)

 [Known Issues](#Known_Issues)

 [Blogs](https://blog.xamarin.com/tag/ios/)

 [Open Source](#Open_Source)



### Installing

* Visual Studio 2017 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)
* Visual Studio 2015 Tools for Xamarin – [Stable updater channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/#visualstudio)

#### Requirements

* The latest features and API requires Xcode 9.2 and the bundled iOS, tvOS and watchOS SDKs;
* Apple Xcode 9.2 requires a Mac running OSX 10.12.6 (Sierra) or newer;

### Feedback

We'd love to hear from you! If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios), [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi?product=iOS) and [GitHub](https://github.com/xamarin/xamarin-macios/issues) for existing issues. Report new issues and suggestions [on GitHub](https://github.com/xamarin/xamarin-macios/issues). 

### Release History

This release of Xamarin.iOS will follow shortly after the official release of Xcode 9.2 by Apple.

* January 16th, 2018 - Xamarin.iOS 11.6.1.4
* January 9th, 2018 - Xamarin.iOS 11.6.1.3
* December 4th, 2017 - Xamarin.iOS 11.6.1.2

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## January 16th, 2018 - Xamarin.iOS 11.6.1.4

> This version is included in the Visual Studio 2017 version 15.5.5 release.

### Issues Fixed
* [61002:](https://bugzilla.xamarin.com/show_bug.cgi?id=61002) [bcl] Runtime exception: Cannot access a disposed object. Object name: 'MobileAuthenticatedStream'

## January 9th, 2018 - Xamarin.iOS 11.6.1.3

> This version is included in the Visual Studio 2017 version 15.5.3 release.

### Issues Fixed
* [60625:](https://bugzilla.xamarin.com/show_bug.cgi?id=60625) [runtime] Assertion at local-propagation.c:562, condition `ins->opcode > MONO_CEE_LAST` not met

## December 4th, 2017 - Xamarin.iOS 11.6.1.2

> This version is included in the Visual Studio 2017 version 15.5.1 release.

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 5.4](https://github.com/mono/mono/commits/d15-5-2017-06) ([950ea65c3ba](https://github.com/mono/mono/commit/950ea65c3ba571cd139dc34b48d7101a2e894993)).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.4.0/).

## What's New in this Release

This release is built upon our [open sourced SDK](#open-source) and is based on our [Xamarin.iOS 11.4](https://developer.xamarin.com/releases/ios/xamarin.ios_11/xamarin.ios_11.4/)
release (d15-5).

* [Support for Xcode 9.2](#support-for-xcode-92)
* [New API for iOS 11.2, tvOS 11.2 and watchOS 4.2](#new-api-for-ios-112-tvos-112-and-watchos-42)
* [New API for iOS 11, tvOS 11 and watchOS 4](#new-api-for-ios-11-tvos-11-and-watchos-4)

### Support for Xcode 9.2

Our tooling (e.g. simulator and device support) was updated to ensure compatibility with the latest libraries.

Additional information can be found in Xcode [release notes](https://developer.apple.com/library/content/releasenotes/DeveloperTools/RN-Xcode/Chapters/Introduction.html#//apple_ref/doc/uid/TP40001051-CH1-SW936).

### New API for iOS 11.2, tvOS 11.2 and watchOS 4.2

There were very few changes, split across most frameworks, in the SDKs. Bindings for the following frameworks have been updated for iOS 11.2, tvOS 11.2 and watchOS 4.2:

* AVFoundation
* AVKit
* Contacts
* CoreAnimation (QuartzCore)
* CoreBluetooth
* CoreML
* HealthKit
* HomeKit
* Intents
* LocalAuthentication
* MediaPlayer
* PassKit
* PDFKit
* ReplayKit
* SceneKit
* StoreKit, adding **Introductory Pricing for Auto-Renewable Subscriptions**
* UIKit
* WatchKit

Additional information can be found in [iOS](https://developer.apple.com/go/?id=ios-11.2-sdk-rn), [tvOS](https://developer.apple.com/go/?id=tvos-11.2-sdk-rn) and [watchOS](https://developer.apple.com/go/?id=watchos-4.2-sdk-rn) release notes.


### New API for iOS 11, tvOS 11 and watchOS 4

Additional API from Xcode 9 are also included in this release, in particular:

* CoreImage filters
	* CIAreaMinMaxRed
	* CIAttributedTextImageGenerator
	* CIBarcodeGenerator
	* CIBicubicScaleTransform
	* CIBlendWithBlueMask
	* CIBlendWithRedMask
	* CIBokehBlur
	* CIColorCubesMixedWithMask
	* CIColorCurves
	* CIDepthBlurEffect
	* CIDepthToDisparity
	* CIDisparityToDepth
	* CIEdgePreserveUpsampleFilter
	* CILabDeltaE
	* CIMorphologyGradient
	* CIMorphologyMaximum
	* CIMorphologyMinimum
	* CITextImageGenerator
* Bindings for Security.framework
* Bindings for MetalPerformanceShaders.framework

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might requires workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.


## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.4 stable release:

* [iOS](/releases/ios/api_changes/ios_11.4.0_to_11.6.1);
* [tvOS](/releases/ios/api_changes/tvos_11.4.0_to_11.6.1);
* [watchOS](/releases/ios/api_changes/watchos_11.4.0_to_11.6.1)

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios/tree/xcode9.2) branch `xcode9.2`
* [mono](https://github.com/mono/mono/commits/d15-5-2017-06) branch `d15-5-2017-06`
