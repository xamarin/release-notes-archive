---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 11.0"
---

version:11.0
releasedate:2017-09-19

Requirements
============

- Xcode 9.0 and the bundled iOS, tvOS and watchOS SDKs, Using an older Xcode version is possible but some features are not available, in particular:
	- The static registrar requires Xcode 9 headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors;
	- Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless Xcode9 toolchain is used;

- Apple Xcode 9.0 requires a Mac running macOS 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode9` branch, and is based on our stable [Xamarin.iOS 10.12 release](https://developer.xamarin.com/releases/ios/xamarin.ios_10/xamarin.ios_10.12/) (SR2).

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


#### API diff

The following documents contains a complete list of the API changes since the 10.12 release:

* [iOS](/releases/ios/api_changes/ios_10.12.3_to_11.0.0);
* [tvOS](/releases/ios/api_changes/tvos_10.12.3_to_11.0.0);
* [watchOS](/releases/ios/api_changes/watchos_10.12.3_to_11.0.0)

