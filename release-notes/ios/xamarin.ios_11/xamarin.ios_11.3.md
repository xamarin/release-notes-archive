---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 11.3"
---

version:11.3.0
releasedate:2017-11-08

Requirements
============

- Xcode 9.1 and the bundled iOS, tvOS and watchOS SDKs. Using an older Xcode version is possible, but some features may not be available, in particular:
	- The static registrar requires Xcode 9.1 headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if not used.
	- Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

- Xcode 9.1 requires a Mac running macOS 10.12.6 (Sierra) or newer

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode9.1` branch, and is based on our latest stable [Xamarin.iOS 11.2 release](https://developer.xamarin.com/releases/ios/xamarin.ios_11/xamarin.ios_11.2/).

There were very few changes in the SDK. Bindings for the following frameworks have been updated for iOS 11.1, tvOS 11.1 and watchOS 4.1:

* AVFoundation
* Intents
* MediaPlayer
* ReplayKit
* UIKit

Additional bindings for the following frameworks have been updated for iOS 11, tvOS 11 and watchOS 4:

* CoreGraphics
* GameplayKit
* HealthKit
* ModelIO
* VideoToolbox

#### API diff

The following documents contains a complete list of the API changes since our (11.2) stable release:

* [iOS](/releases/ios/api_changes/ios_11.2.0_to_11.3.0)
* [tvOS](/releases/ios/api_changes/tvos_11.2.0_to_11.3.0)
* [watchOS](/releases/ios/api_changes/watchos_11.2.0_to_11.3.0)

