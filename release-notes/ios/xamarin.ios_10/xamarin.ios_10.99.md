---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.99"
---

version:10.99.8
releasedate:2017-09-13

<div class="note">
	<b>Xcode9 based preview</b>
	This version of Xamarin.iOS will ship as part of Xamarin <b>xcode9</b> releases.
</div>

Requirements
============

- Xcode 9.0 GM and the bundled iOS, tvOS and watchOS SDKs, Using an older Xcode version is possible but some features are not available, in particular:
	- The static registrar requires Xcode 9 headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors;
	- Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless Xcode9 toolchain is used;

- Apple Xcode 9.0 requires a Mac running macOS 10.12 (Sierra) or newer;


What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode9` branch, and is based on our latest stable [Xamarin.iOS 10.12 release](https://developer.xamarin.com/releases/ios/xamarin.ios_10/xamarin.ios_10.12/).

This last preview is based on Apple's GM and can be used to submit applications to the App Store.
However this is not our final/stable versions and some additional changes are planned, e.g. new API were introduced in the GM.


### iOS 11

The following new frameworks were added in iOS 11:

* ARKit.framework (Augmented Reality)
* CoreML.framework (Machine Learning)
* CoreNFC.framework (Near Field Communication)
* DeviceCheck.framework
* FileProvider.framework
* FileProviderUI.framework
* IdentityLookup.framework
* IOSurface.framework
* PDFKit.framework (new in iOS, exists in macOS)
* Vision.framework

Most other frameworks were also updated, e.g. drag-n-drop support is part of UIKit.

### tvOS 11

The following new frameworks were added in tvOS 11:

* CoreML.framework (Machine Learning)
* DeviceCheck.framework
* IOSurface.framework
* Vision.framework

Most other frameworks were also updated.

### watchOS 4

The following new frameworks were added in watchOS 4:

* CoreBluetooth.framework (new on watchOS)
* CoreML.framework (Machine Learning)
* CoreVideo.framework (new on watchOS)
* Vision.framework

Most other frameworks were also updated.


### Xamarin.iOS 10.99.x (continuous builds)

All of our builds are also available for [download](https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode9/) directly. A bit of warning, they come from our build bots and receice **no** QA. Verified builds will be made available as web preview duing summer.

Our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce the **API diff** for every commit that is being built. Pick a build based on `xcode9` and look for the **API diff** link on the left column.

You can track the latest status of our API work on the [wiki](https://github.com/xamarin/xamarin-macios/wiki/xcode9-Bindings-Status).


### Xamarin.iOS 10.99.8

This ninth preview is based on Xcode 9 GM.
It adds new API for CloudKit and UIKit frameworks.
Bindings for the following frameworks are still in progress and not _yet_ updated with the GM changes.

* CoreAudio
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo _partially bound_
* GamePlayKit
* HealthKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our new (10.12) stable release:

* [iOS](/releases/ios/api_changes/ios_10.12.0_to_10.99.8);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.8);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.8)


### Xamarin.iOS 10.99.7

This eighth preview is based on beta 6 (Xcode/SDK) and works with beta 8 (watchOS) and 9 (iOS and tvOS) devices.
It adds new API for AVFoundation, IOSurface and Metal frameworks.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* CloudKit
* CoreAudio
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo _partially bound_
* GamePlayKit
* HealthKit
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* UIKit _partially bound_
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our new (10.12) stable release:

* [iOS](/releases/ios/api_changes/ios_10.12.0_to_10.99.7);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.7);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.7)


### Xamarin.iOS 10.99.6

This seventh preview is based on beta 6 (Xcode/SDK) and works with beta 8 devices.
It adds new API for CoreBluetooth and enables CoreVideo on watchOS.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AVFoundation
* CloudKit
* CoreAudio
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo _partially bound_
* GamePlayKit
* HealthKit
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* UIKit _partially bound_
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our new (10.12) stable release:

* [iOS](/releases/ios/api_changes/ios_10.12.0_to_10.99.6);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.6);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.6)


### Xamarin.iOS 10.99.5

This sixth preview is based on beta 6 (Xcode/SDK) and works with beta 7 devices.
It adds new API for IntentsUI and VideoSubscriberAccount frameworks and updates existing frameworks to beta 6 SDK (unless noted below).
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* GamePlayKit
* HealthKit
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* UIKit _partially bound_
* VideoToolbox
* Vision (up to beta 5)

#### API diff

The following documents contains a complete list of the API changes since our new (10.12) stable release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.99.5);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.5);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.5)


### Xamarin.iOS 10.99.4

This fifth preview is based on beta 5 (Xcode/SDK) and works with beta 5 and 6 devices.
It adds new API for AudioToolbox, Foundation, Intents, PassKit and ReplayKit frameworks.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* GamePlayKit
* HealthKit
* IntentsUI
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* UIKit _partially bound_
* VideoSubscriberAccount
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our new (10.12) stable release:

* [iOS](/releases/ios/api_changes/ios_10.12.0_to_10.99.4);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.4);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.4)


### Xamarin.iOS 10.99.3

This fourth preview is based on beta 5. 
It adds new API for MediaPlayer, PDFKit and WatchKit and updates existing frameworks to beta 5 (unless noted below).
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreData _up to beta 4_
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* Foundation _partially bound_
* GamePlayKit
* HealthKit
* HomeKit _up to beta 4_
* Intents
* IntentsUI
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* PassKit
* ReplayKit
* SceneKit
* Security
* UIKit _partially bound_
* VideoSubscriberAccount
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our last (10.10) release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.99.3);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.99.3);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.99.3)


### Xamarin.iOS 10.99.2

This third preview is based on beta 4.
It adds new API for ImageIO, QuartzCore (CoreAnimation), QuickLook, SafariServices and StoreKit.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* Foundation _partially bound_
* GamePlayKit
* HealthKit
* Intents
* IntentsUI
* IOSurface
* MediaPlayer
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* PassKit
* PDFKit
* ReplayKit
* SceneKit
* Security
* UIKit _partially bound_
* VideoSubscriberAccount
* VideoToolbox
* WatchKit

#### API diff

The following documents contains a complete list of the API changes since our last (10.10) release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.99.2);
* [tvOS](/releases/ios/api_changes/tvos_10.10.0_to_10.99.2);
* [watchOS](/releases/ios/api_changes/watchos_10.10.0_to_10.99.2)


### Xamarin.iOS 10.99.1

This second preview is based on beta 4.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* ARKit _updated to beta 3_
* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage
* CoreMedia
* CoreML _updated to beta 3_
* CoreText
* CoreVideo
* ExternalAccessory
* Foundation _partially bound_
* GamePlayKit
* HealthKit
* ImageIO
* Intents
* IntentsUI
* IOSurface
* MediaPlayer
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* PassKit
* PDFKit
* QuartzCore / CoreAnimation
* QuickLook
* ReplayKit
* SafariServices
* SceneKit
* Security
* StoreKit
* UIKit _partially bound_
* VideoSubscriberAccount
* VideoToolbox
* WatchKit

#### API diff

The following documents contains a complete list of the API changes since the 10.12 release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.99.1);
* [tvOS](/releases/ios/api_changes/tvos_10.10.0_to_10.99.1);
* [watchOS](/releases/ios/api_changes/watchos_10.10.0_to_10.99.1)


### Xamarin.iOS 10.99.0

This first preview, based on beta 3, includes the new API for the following platforms/frameworks:

### iOS 11

* Accounts _updated to beta 3_
* ARKit **new** _updated to beta 3_
* AVKit _updated to beta 3_
* CallKit _updated to beta 3_
* Contacts _updated to beta 3_
* CoreAudioKit _updated to beta 3_
* CoreData _updated to beta 3_
* CoreLocation _updated to beta 3_
* CoreMotion _updated to beta 3_
* CoreNFC _updated to beta 3_
* CoreTelephony _updated to beta 2_
* DeviceCheck **new** _updated to beta 3_
* EventKit _updated to beta 3_
* EventKitUI _updated to beta 3_
* GameController _updated to beta 3_
* GameKit _updated to beta 3_
* HomeKit _updated to beta 3_
* iAd _updated to beta 3_
* IdentifyLookup _updated to beta 3_
* MultiPeerConnectivity _updated to beta 3_
* OpenGLES _updated to beta 3_
* Photos _updated to beta 3_
* PushKit _updated to beta 3_
* Social _updated to beta 3_
* UserNotifications _updated to beta 3_
* WKWebKit _updated to beta 3_

Other frameworks are in progress and might be partially available.

### tvOS 11

* AVKit _updated to beta 3_
* CoreData _updated to beta 3_
* CoreLocation _updated to beta 3_
* DeviceCheck **new** _updated to beta 3_
* GameController _updated to beta 3_
* GameKit _updated to beta 3_
* HomeKit _updated to beta 3_
* MultiPeerConnectivity _updated to beta 3_
* OpenGLES _updated to beta 3_
* Photos _updated to beta 3_
* TBMLKit _updated to beta 3_
* TVServices _updated to beta 3_
* UserNotifications _updated to beta 3_

Other frameworks are in progress and might be partially available.

### watchOS 4

* ClockKit _updated to beta 3_
* Contacts _updated to beta 3_
* CoreData _updated to beta 3_
* CoreLocation _updated to beta 3_
* CoreMotion _updated to beta 3_
* CoreNFC _updated to beta 3_
* GameKit _updated to beta 3_
* HomeKit _updated to beta 3_
* MultiPeerConnectivity _updated to beta 3_
* UserNotifications _updated to beta 3_

Other frameworks are in progress and might be partially available.


#### API diff

The following documents contains a complete list of the API changes since the 10.12 release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.99.0);
* [tvOS](/releases/ios/api_changes/tvos_10.10.0_to_10.99.0);
* [watchOS](/releases/ios/api_changes/watchos_10.10.0_to_10.99.0)

