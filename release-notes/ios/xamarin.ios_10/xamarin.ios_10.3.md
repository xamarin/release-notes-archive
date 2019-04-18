---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.3"
---

version:10.3.1
releasedate:2016-12-19

Requirements
============

- The latest features and API requires Xcode 8.2 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.2 requires a Mac running OSX 10.11.5 (El Capitan) or newer;

What's New
==========

This release adds support for the newly released Xcode 8.2 and it's API additions. 
It is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode8.2` branch, and include some additional IDE integration tools.

### iOS 10.2

Minor API additions were made to:

* AVFoundation
* CloudKit
* HomeKit
* Intents
* MediaPlayer
* Messages
* ModelIO
* PassKit
* Photos
* ReplayKit
* Security
* SpriteKit
* UIKit
* VideoSubscriberAccount
* WatchConnectivity
* WatchKit

### tvOS 10.1

Minor API additions were made to:

* AVFoundation
* AVKit
* CloudKit
* HomeKit
* MediaPlayer
* ModelIO
* Photos
* ReplayKit
* Security
* SpriteKit
* StoreKit
* UIKit
* VideoSubscriberAccount

### watchOS 3.1.1

There are no API addition for watchOS 3.1.1 in Xcode 8.2. A few adjustments were made using some clarifications in the header files.


Xamarin.iOS 10.3.1
==================

This is a service release (SR2) for Xamarin.iOS 10.3 (cycle 8).

There is no API diff for this release, the only public change is the version number update.

### Enhancements

* Better `UIScreen.Capture` implementation with support for `CALayer`, contributed by Christian Resma Helle

### Bug Fixes

* [41231](https://bugzilla.xamarin.com/show_bug.cgi?id=41231) - [msbuild] Don't rm -rf the .dSYM dir in the _CompileToNative target
* [45046](https://bugzilla.xamarin.com/show_bug.cgi?id=45046) - [runtime] Fix xamarin_log to not treat % as format specifiers
* [45140](https://bugzilla.xamarin.com/show_bug.cgi?id=45140) - [mono] Fix crashes at launch with `KERN_INVALID_ADDRESS`
* [45994](https://bugzilla.xamarin.com/show_bug.cgi?id=45994) - [security] Remove port number from TLS Server Name Identification (SNI)
* [48382](https://bugzilla.xamarin.com/show_bug.cgi?id=48382) - [avfoundation] Fix incorrect selector for AVPlayerItemVideoOutput .ctor
* [50207](https://bugzilla.xamarin.com/show_bug.cgi?id=50207) - [mono] Fix mono_mach_arch_get_thread_fpstate_size implementation
* [pr1239](https://github.com/xamarin/xamarin-macios/pull/1158) - [opentk] Remove p/invoke to obsoleted glGetQueryObjectivEXT API

* [50290](https://bugzilla.xamarin.com/show_bug.cgi?id=50290) - [linker] Update mscorlib.xml to preserve generic collection interfaces **(10.3.1.8+)**


Xamarin.iOS 10.3.0
==================

This release is based on our cycle 8 service release 1 ([XI 10.2.1](https://developer.xamarin.com/releases/ios/xamarin.ios_10/xamarin.ios_10.2/)) work, more details and a list of bug fixes can be found on it's release notes.

The following documents contains a complete list of the API changes since our latest stable release: XI 10.2.1 (C8SR1)

* [iOS](/releases/ios/api_changes/ios_10.2.1_to_10.3.0);
* [tvOS](/releases/ios/api_changes/tvos_10.2.1_to_10.3.0);
* [watchOS](/releases/ios/api_changes/watchos_10.2.1_to_10.3.0)

### Bug Fixes

* [44874](https://bugzilla.xamarin.com/show_bug.cgi?id=44874) - [networkextension] Problems with NetworkExtension.NETunnelProviderManager
* [pr1158](https://github.com/xamarin/xamarin-macios/pull/1158) - [networkextension] Contributed fixes to NEPacketTunnelNetworkSettings and NEPacketTunnelProvider
* [pr1239](https://github.com/xamarin/xamarin-macios/pull/1239) - [opentk] Deprecated `glGetQueryObjectivEXT` symbol was removed from iOS



