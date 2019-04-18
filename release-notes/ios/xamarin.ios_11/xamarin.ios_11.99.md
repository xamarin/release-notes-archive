---
id: ca54591e-f09d-4059-a60d-6a4a8c461199
title: "Xamarin.iOS 11.99"
---

# Xamarin.iOS 11.99
Last Update: 8/23/2018

[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](#release-blog) | [Feedback](#feedback) | [Open Source](#open-source)

### Requirements

* The latest features and APIs require Xcode 10 beta 6 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 10 requires a Mac running OSX 10.13.4 (High Sierra) or newer

## What's New in this Release

* [Support for Xcode 10]()
* [Support for iOS 12]()
* [Support for tvOS 12]()
* [Other Changes]()

### Support for Xcode 10

For more information you can consult the [Xcode 10](https://developer.apple.com/go/?id=xcode-10-beta-rn) release notes from Apple.

### Support for iOS 12

The following new frameworks were added in iOS 12:

* AuthenticationServices
* CarPlay
* IdentityLookup
* IdentityLookupUI
* NaturalLanguage
* Network

Most other frameworks were also updated, including ARKit 2.0 and Siri shortcuts. See our [API diff](#API_Diff) to browse the latest changes.

For more information you can consult the [iOS 12](https://developer.apple.com/go/?id=ios-12-beta-rn) release notes from Apple.

### Support for tvOS 12

The following new frameworks were added in tvOS 12:

* NaturalLanguage
* Network
* TVUIKit

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the latest changes.

For more information you can consult the [tvOS 12](https://developer.apple.com/go/?id=tvos-12-sdk-rn) release notes from Apple.

### Support for watchOS 5

The following new frameworks were added in watchOS 5:

* NaturalLanguage

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the latest changes.

For more information you can consult the [watchOS 5](https://developer.apple.com/go/?id=watchos-5-sdk-rn) release notes from Apple.

### Other Changes

* Apple is deprecating OpenGLES and related API in favor of Metal;
* Apple **removed** support for `stdlibc++`. Using C++ code now requires the use of `libc++`.

### Release History

This version of Xamarin.iOS correspond to our `xcode10` milestone and is based of the stable **15.8** release. Earlier versions (11.99.0-2) were based on our older **15.7** releases.

* August 23, 2018 - Xamarin.iOS 11.99.3.538
* August 6, 2018 - Xamarin.iOS 11.99.2.130
* July 4, 2018 - Xamarin.iOS 11.99.1.44
* June 27, 2018 - Xamarin.iOS 11.99.0.93

## August 23, 2018 - Xamarin.iOS 11.99.3.538

This fourth preview is based on Xcode 10 beta 6.

### New frameworks

This preview includes the following new frameworks

* iOS, tvOS: Network ([sample](https://github.com/migueldeicaza/NetCatNetwork))

### Updated frameworks

This preview includes the following updates to existing frameworks

* Shared frameworks: CoreServices, Metal

Other frameworks, except MetalPerformanceShaders, were updated with changes up to beta 6.


## August 6, 2018 - Xamarin.iOS 11.99.2.130

This third preview is based on Xcode 10 beta 5.

### New CoreImage filters

New CoreImage filters include:

* `CISaliencyMapFilter`

### Updated frameworks

This preview includes the following updates to existing frameworks (all API updated to beta 5)

* iOS specific: ARKit, CoreMotion, CoreMIDI, iAd, PDFKit
* tvOS specific: TVMLKit, TVUIKit
* Shared frameworks: AVFAudio, AVFoundation, AudioToolbox, Contacts, CoreGraphics, CoreImage, CoreMedia, CoreML, Foundation, HealthKit, Intents, MediaPlayer, ModelIO, Passkit, Photos, Scenekit, Storekit, UIKit, UserNotifications, Vision, WebKit

## July 4, 2018 - Xamarin.iOS 11.99.1.44

This second preview is based on Xcode 10 beta 3 and include support for watchOS 5.

### New frameworks

This preview includes the following new frameworks (all API updated to beta 3)

* tvOS: TVUIKit

### New CoreImage filters

New CoreImage filters includes:

* `CICameraCalibrationLensCorrection`
* `CICoreMLModelFilter`

### Updated frameworks

This preview includes the following updates to existing frameworks (all API updated to beta 3)

* tvOS specific: SystemConfiguration, TVMLKit
* watchOS specific: WatchKit
* Shared frameworks: CloudKit, CoreAudio, CoreML, CoreText, GameKit, HealthKit, HomeKit, ModelIO, OpenGLES, Photos, PhotosUI, StoreKit

## June 27, 2018 - Xamarin.iOS 11.99.0.93

This first preview is based on Xcode 10 beta 2. Many of the new API are already available. Future previews will include additional API as they become available.

### New frameworks

This preview includes the following new frameworks (all API updated to beta 2)

* iOS: AuthenticationServices, CarPlay, IdentityLookup, IdentityLookupUI and NaturalLanguage
* tvOS: NaturalLanguage

### New CoreImage filters

New CoreImage filters includes:

* `CIAreaMinMax`
* `CIDither`
* `CIGuidedFilter`
* `CIMeshGenerator`
* `CIMix`
* `CISampleNearest`

### Updated frameworks

This preview includes the following updates to existing frameworks (all API updated to beta 2)

* iOS specific: ARKit, CoreNFC, IntentsUI, Messages, UserNotificationUI
* watchOS specific: ClockKit
* Shared frameworks: Accounts, AdSupport, AVFoundation, AVKit, Contacts, CoreMotion, CoreVideo, GameplayKit, Intents, IOSurface, MapKit, ReplayKit, SafariServices, SceneKit, SpriteKit, UIKit, UserNotification, VideoSubscriberAccount, VideoToolbox, WatchConnectivity, WatchKit 

## Known Issues

* [4421](https://github.com/xamarin/xamarin-macios/issues/4421) Two Simulators are launching while deploying an iOS App with Xcode10-beta3
* [4532](https://github.com/xamarin/xamarin-macios/issues/4532) Simulator apps with Xcode 10 are not full screen and you can't interact
* [4305](https://github.com/xamarin/xamarin-macios/issues/4305) Default MasterDetail template crashes with Xcode 10 beta 2
* [4576](https://github.com/xamarin/xamarin-macios/issues/4576) 'Metal Game' fails to build 
* [4525](https://github.com/xamarin/xamarin-macios/issues/4525) [ARKit] different 'Transform' matrix presentation

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.12 stable release:

* [iOS](/releases/ios/api_changes/ios-11-12-0-11-99-3)
* [tvOS](/releases/ios/api_changes/tvos-11-12-0-11-99-3)
* [watchOS](/releases/ios/api_changes/watchos-11-12-0-11-99-3)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Github Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode10`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
