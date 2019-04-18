---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.2"
---

version:10.2.1
releasedate:2016-11-01

Requirements
============

- The latest features and API requires Xcode 8.1 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.1 requires a Mac running OSX 10.11.5 (El Capitan) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode8.1` branch, and include some additional IDE integration tools.

This release is based on our cycle 8 ([XI 10.0.x](https://developer.xamarin.com/releases/ios/xamarin.ios_10/xamarin.ios_10.0/)) work, more details and a list of bug fixes can be found on it's release notes.

### iOS 10.1

Minor API additions were made to:

* HomeKit
* MediaPlayer
* PassKit
* StoreKit

### tvOS 10.0.0.2

No API changes were made to the tvOS SDK shipping with Xcode 8.1.

### watchOS 3.1

Minor API additions were made to:

* HomeKit
* PassKit


Xamarin.iOS 10.2.1
==================

This is a service release (SR1) for Xamarin.iOS 10.2.

### Bug Fixes

* [44701](https://bugzilla.xamarin.com/show_bug.cgi?id=44701) - [mtouch] Fix possible NRE when optimizing bindings **(10.0.2+)**
* [44349](https://bugzilla.xamarin.com/show_bug.cgi?id=44349) - [Mono.Data.Sqlite] Fails to store seconds in timestamp value to a table **(10.0.2+)**

* [44257](https://bugzilla.xamarin.com/show_bug.cgi?id=44257) - [msbuild] Add watch-companion to UIRequiredDeviceCapabilities for watchOS1 extensions **(10.2.1+)**
* [45379](https://bugzilla.xamarin.com/show_bug.cgi?id=45379) - [sgen] Fix missing wbarrier for array generic setter **(10.2.1+)**
* [45847](https://bugzilla.xamarin.com/show_bug.cgi?id=45847) - [System] Remove any CFNetwork usage from the watchOS profile **(10.2.1+)**
* [profiler] Fix a regression that caused all buffers to have a zero thread ID **(10.2.1+)**


Xamarin.iOS 10.2.0
==================

The following documents contains a complete list of the API changes since our latest stable release: XI 10.0.1 (C8SR0)

* [iOS](/releases/ios/api_changes/ios_10.0.1_to_10.2.0);
* [tvOS](/releases/ios/api_changes/tvos_10.0.1_to_10.2.0);
* [watchOS](/releases/ios/api_changes/watchos_10.0.1_to_10.2.0)

### Known Issues

* Issue: Simulator (list/deploy) and device (deploy) does not work after updating to Xcode 8.1. Last minutes changes to Xcode 8.1 GM required changes in the IDE support.

	* Workaround: Update your IDE (Xamarin Studio and/or Visual Studio) to the latest version available.

* Unsolved issues from [XI 10.0.x](https://developer.xamarin.com/releases/ios/xamarin.ios_10/xamarin.ios_10.0/) are listed in the linked release notes.

### Upstream Issues (in Xcode)

* Issue: **"App" May Slow Down Your iPhone**: This happens when a 32bit-only application executes on a 64 bits capable platform, e.g. a i386 build running on a iPhone6 simulator (capable of 64bit). The warning simply means you're not using the optimal build for the platform. This can be normal when testing and, by default, simulator builds are only 32 or 64 bits (to make them faster).

	* Workaround: You can change your project settings to remove the warning. Application submitted to the app store should, in most cases, have both 32 and 64 bits slices or, at your choice, 64 bits only (but 32 bits only applications cannot be submitted anymore).

	* Note: this is a newer version of the **App not optimized for iOS10** warning shown during the iOS 10.0 betas.

