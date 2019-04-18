---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.6"
---

version:10.6.0
releasedate:2017-02-27

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;
- Xamarin Studio 6.2.x (stable) is needed to deploy on devices;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode8.3` branch, and include some additional IDE integration tools.

It is based on the current XI 10.4 stable release (cycle 9) with additional support for Xcode 8.3 tools and API.


Breaking Changes
----------------

Xcode 8.3 contains some **breaking changes** from Apple.

- Apple swapped the values of HomeKit's `HMCharacteristicValueContactState` enum. `None` => `Detected`; `Detected` => `None`.

If you used this enum then you might need to adapt your code.
Keep in mind that [constants](https://msdn.microsoft.com/en-us/library/sbbt4032.aspx#Anchor_0), including enum values, are converted to numeric literals at compile time. You might have to recompile existing assemblies using the incorrect values.


### iOS 10.3

Some minor API addition were made in:

* AudioToolbox
* AVFoundation
* CallKit
* CFNetwork
* Contacts
* CoreVideo
* Foundation
* HomeKit
* iAd
* ImageIO
* Intents
* LocalAuthentication
* MediaPlayer
* Metal
* ModelIO
* OpenGLES
* PassKit
* Photos
* Security
* SpriteKit
* StoreKit
* UIKit
* VideoToolbox
* WatchKit
* WebKit

### tvOS 10.2

The biggest change to tvOS is the inclusion of the `VideoToolbox.framework`, already part of iOS, into the platform.

Other minor API addition were made in:

* AudioToolbox
* AVFoundation
* CFNetwork
* CoreVideo
* Foundation
* HomeKit
* ImageIO
* Metal
* ModelIO
* OpenGLES
* Photos
* Security
* SpriteKit
* StoreKit
* UIKit


### watchOS 3.2

The biggest change to watchOS is the support for SiriKit using the `Intents.framework`. This is the first use of application extensions inside watchOS and templates to support it are not available in the current IDE. In the mean time please use the following [instructions](https://github.com/dalexsoto/XamarinSiriWatchExtension) to manually add the SiriKit extension project inside your watch application.

Other minor API addition were made in:

* AVFoundation
* CloudKit
* Contacts
* Foundation
* HomeKit
* ImageIO
* PassKit
* Security
* SpriteKit
* WatchKit


### Bug Fixes

* [51423](https://bugzilla.xamarin.com/show_bug.cgi?id=51423) - [foundation] Honor the cancellation token win the async requests in `NSUrlSessionHandler`
* [53794](https://bugzilla.xamarin.com/show_bug.cgi?id=53794) - [foundation] Ensure that if a request is canceled we cancel the `NSUrlSessionTask`


### API diff

The following documents contains a complete list of the API changes since our latest stable release: XI 10.4.0 (C9)

* [iOS](/releases/ios/api_changes/ios_10.4.0_to_10.6.0);
* [tvOS](/releases/ios/api_changes/tvos_10.4.0_to_10.6.0);
* [watchOS](/releases/ios/api_changes/watchos_10.4.0_to_10.6.0)

