---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 9.99"
---

version:9.99.5
releasedate:2016-08-17

<div class="note">
	<b>Unstable Software:</b>
	This SDK is based on Xcode 8 <b>beta</b> and cannot be used to submit application to Apple's
	AppStore. Continue using the stable release (9.8) or an cycle8 (9.10) beta if you need to submit
	applications before Apple release a stable version of Xcode 8.
	<br/>
	<b>Classic Profile Deprecation:</b>
	This version of Xamarin.iOS does <b>not</b> ship with classic support (i.e. `monotouch.dll`).
	The last version supporting classic is Xamarin.iOS 9.10, which is nearly identical to 9.99,
	but does not include the new API added in Xcode 8 SDKs.
</div>

Requirements
============

- The latest features and API requires Xcode 8.0 beta 6 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.0 requires a Mac running OSX 10.11.5 (El Capitan) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode8` branch, and include some additional IDE integratin tools.

This release is based on our **cycle 8** (XI 9.10.x) work, 
more [details and bug fixes](releases/ios/xamarin.ios_9/xamarin.ios_9.10.md) can be found on it's release notes.

### iOS 10

The following new frameworks were added in iOS 10:

* CallKit (available, beta 6)
* Intents (available, beta 6)
* IntentsUI (available, beta 6)
* Message (available, beta 6)
* Speech (available, beta 6)
* UserNotification (available, beta 6)
* UserNotificationUI (available, beta 6)
* VideoSubscriberAccount (available, beta 6)

### tvOS 10

The following new frameworks were added in tvOS 10:

* ExternalAccessory (available, beta 6)
* HomeKit (available, beta 6)
* MultipeerConnectivity (available, beta 6)
* Photos (available, beta 6)
* PhotosUI (available, beta 6)
* ReplayKit (available, beta 6)
* UserNotification (available, beta 6)
* VideoSubscriberAccount (available, beta 6)

Note: New frameworks for tvOS are new to the platform, but already exists (or were just added) in iOS.

Bindings are also update for the exising frameworks:

* TVMLKit (available, beta 6)
* Several new API are also available (see **API diff**)

### watchOS 3

The following new frameworks were added in watchOS 3:

* AVFoundation (available, beta 6)
* CloudKit (available, beta 6)
* CoreAudio (available, beta 6)
* GameKit (available, beta 6)
* SceneKit (available, beta 6)
* SpriteKit (available, beta 6)
* UserNotification (available, beta 6)

Note: New frameworks for watchOS are new to the platform, but already exists (or were just added) in iOS.

Bindings are also update for the exising frameworks:

* ClockKit (up to beta 6)
* WatchKit (up to beta 6)
* Several new API are also available (see **API diff**)

Other Notable Changes
=====================

* Some enum values were found to be incorrect and were fixed in this release. This include members of `AVError`, `NSEntityMappingType` and `UIContentSizeCategory`. You can see them in our API diff documents.

### Xamarin.iOS 9.99.5

Testing of the sixth release was done against Xcode 8 beta 6, iOS beta 8 and tvOS 10 beta 7. This release includes all the new API from Xcode 8 SDKs and we're now focusing ourselves on bugs, reviews and auditing the API.

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_9.99.5);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_9.99.5);
* [watchOS](/releases/ios/api_changes/watchos_9.9.0_to_9.99.5) note: not part of XI 9.8 (stable) and the alpha API (from 9.9+) is not yet frozen;

### Xamarin.iOS 9.99.4

Testing of the fifth release was done against Xcode 8 beta 6 (and iOS beta 7). The new API from following frameworks are **not** completely bound at this time.

* AudioToolbox
* AudioUnit
* GameplayKit
* Metal
* Security

Future preview releases will include those API / framework updates. You can track the [progress of our bindings](https://github.com/xamarin/xamarin-macios/wiki/Bindings) from our wiki.

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_9.99.4);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_9.99.4);
* [watchOS](/releases/ios/api_changes/watchos_9.9.0_to_9.99.4) note: not part of XI 9.8 (stable) and the alpha API (from 9.9+) is not yet frozen;

### Xamarin.iOS 9.99.3

Testing of the fourth release was done against Xcode 8 beta 6. The new API from following frameworks are **not** completely bound at this time.

* AVFoundation
* AudioToolbox
* AudioUnit
* CoreMedia
* GameplayKit
* JavaScriptCore
* Metal
* ModelIO
* Security
* UIKit

Future preview releases will include those API / framework updates. You can track the [progress of our bindings](https://github.com/xamarin/xamarin-macios/wiki/Bindings) from our wiki.

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_9.99.3);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_9.99.3);
* [watchOS](/releases/ios/api_changes/watchos_9.9.0_to_9.99.3) note: not part of XI 9.8 (stable) and the alpha API (from 9.9+) is not yet frozen;

### Xamarin.iOS 9.99.2

Testing of the third release was done against Xcode 8 beta 5. The new API from following frameworks are **not** completely bound at this time.

* AVFoundation
* AudioToolbox
* AudioUnit
* CoreGraphics
* CoreMedia
* Foundation
* GameplayKit
* JavaScriptCore
* LocalAuthentication
* Metal
* MetalPerformanceShaders
* ModelIO
* Security
* UIKit

Future preview releases will include those API / framework updates. You can track the [progress of our bindings](https://github.com/xamarin/xamarin-macios/wiki/Bindings) from our wiki.

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_9.99.2);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_9.99.2);
* [watchOS](/releases/ios/api_changes/watchos_9.9.0_to_9.99.2) note: not part of XI 9.8 (stable) and the alpha API (from 9.9+) is not yet frozen;

### Xamarin.iOS 9.99.1

Testing of the second preview was done against Xcode 8 beta 4. The new API from following frameworks are **not** completely bound at this time.

* AVFoundation
* AudioToolbox
* AudioUnit
* CloudKit
* CoreFoundation
* CoreGraphics
* CoreMedia
* Foundation
* GameplayKit
* HealthKit
* JavaScriptCore
* LocalAuthentication
* Metal
* MetalPerformanceShaders
* ModelIO
* SceneKit
* Security
* UIKit

Future preview releases will include those API / framework updates. You can track the [progress of our bindings](https://github.com/xamarin/xamarin-macios/wiki/Bindings) from our wiki.

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_9.99.1);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_9.99.1);
* [watchOS](/releases/ios/api_changes/watchos_9.9.0_to_9.99.1) note: not part of XI 9.8 (stable) and the alpha API (from 9.9+) is not yet frozen;

### Xamarin.iOS 9.99.0

**Most of the testing was done against Xcode 8 beta 2. Some things might not work on newer beta releases until a newer preview is available.**

This first preview contains several updates to the existing frameworks that shipped in earlier versions of iOS, tvOS and watchOS.

* AVKit: updated to beta 2
* AddressBook: no change
* CFNetwork: no change
* Contacts: updated to beta 2
* CoreAudio: updated to beta 2
* CoreBluetooth: updated to beta 2
* CoreGraphics: updated to beta 1
* CoreImage: updated to beta 2
* CoreLocation: updated to beta 2
* CoreMIDI: - no change
* CoreMotion: updated to beta 2
* CoreSpotlight: updated to beta 2
* CoreTelephony: updated to beta 2
* CoreText: updated to beta 2
* CoreVideo: updated to beta 2
* EventKit: updated to beta 2
* ExternalAccessory: updated to beta 2
* GLKit: updated to beta 2
* GameController: updated to beta 2
* GameKit: updated to beta 2
* HomeKit: updated to beta 2
* ImageIO: updated to beta 2
* MapKit: updated to beta 2
* MediaPlayer: updated to beta 1
* MetalKit: updated to beta 2
* MultipeerConnectivity: updated to beta 2
* NetworkExtension: updated to beta 2
* NotificationCenter: updated to beta 2
* OpenGLES: updated to beta 2
* Photos: updated to beta 2
* PhotosUI: updated to beta 1
* PushKit: updated to beta 2
* QuartzCore: updated to beta 2
* QuickLook: updated to beta 2
* ReplayKit: updated to beta 2
* SafariServices: updated to beta 2
* SystemConfiguration: updated to beta 2
* UIKit: in progress (some beta 1)
* TVMLKit (tvOS only): updated to beta 2
* VideoToolbox: updated to beta 2
* WatchConnectivity: updated to beta 2
* WebKit: updated to beta 2
* iAd: updated to beta 2

Other, non mentioned, frameworks are being updated and will be available in future previews. If you're curious you can track the [progress of our bindings](https://github.com/xamarin/xamarin-macios/wiki/Bindings) from our wiki. Our SDK is open source so everything is done publicly on github.

Changes for tvOS and watchOS might not be complete and will be audited later.

The following document contains a complete list of the
[API changes from 9.8.0 to 9.99.0](/releases/ios/api_changes/from_9.8.0_to_9.99.0).

### Known Issues

* **Issue:** our watchOS 3.x support has the same limitations our watchOS 2.x support in the current [XI 9.10 beta](releases/ios/xamarin.ios_9/xamarin.ios_9.10). The same version of mono (code and tooling) are shared between **cycle8** and **xcode8** branches;

* **watchOS glances** has been removed in watchOS 3.x / Xcode 8. Trying to start a watchOS app, from the IDE, in glance mode will show a blank screen;

* **App not optimized for iOS10** warning: This happens when a 32bit-only application executes on a 64 bits capable platform, e.g. a i386 build running on a iPhone6 simulator (capable of 64bit). The warning simply means you're not using the optimal build for the platform. This can be normal when testing and, by default, simulator builds are only 32 or 64 bits (to make them faster). You can change your project settings to remove the warning. Application submitted to the app store should have both 32 and 64 bits, in general, or be 64 bits only.

* The known issues from [XI 9.10 / cycle 8](releases/ios/xamarin.ios_9/xamarin.ios_9.10.md) also applies to XI 9.99.

