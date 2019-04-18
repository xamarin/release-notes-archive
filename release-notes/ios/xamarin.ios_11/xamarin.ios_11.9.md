---
id: 5C04A916-2BCF-4FC4-B5D4-D215851CD219
title: "Xamarin.iOS 11.9"
---

Last Update: 4/2/2018

[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Feedback](#feedback) | [Open Source](#open-source)

This version of Xamarin.iOS corresponds to our **xcode9.3** (`xcode9.3`) milestone. This is based on our stable `d15-6` milestone, i.e. Xamarin.iOS 11.8.x.

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled iOS, tvOS and watchOS SDKs;
* Apple Xcode 9.3 requires a Mac running OSX 10.13.2 (High Sierra) or newer;

## What's New in this Release

* [Support for Xcode 9.3](#support-for-xcode-93)
* [Additional API](#additional-api)

### Support for Xcode 9.3

The SDK tooling has been updated to

* Support the new OS from simulators: iOS 11.3, tvOS 11.3 and watchOS 4.3;
* Support launching to devices;

### Additional API

There were very few changes in the SDK but it's worth mentioning:

* an improved [ARKit](https://developer.apple.com/arkit/) version 1.5; and
* a new **BusinessChat** framework for both iOS and macOS.

Other changes can be seen in the [API diff](#API Diff) section of this document.

## Release History

* April 2, 2018 - Xamarin.iOS 11.9.1.24
* March 9, 2018 - Xamarin.iOS 11.9.0.7
* February 15, 2018 - Xamarin.iOS 11.6.99.33

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## April 2, 2018 - Xamarin.iOS 11.9.1.24

This is the initial, stable release with support for Xcode 9.3. There were no _late_ API change in the final release of Xcode 9.3. This version includes all the fixes from the recently released 11.8 service release 3.


## March 9, 2018 - Xamarin.iOS 11.9.0.7

This version is available as a *web preview*. It is the successor of the [11.6.99.x releases](xamarin.ios_11.6.99) which were based on our earlier stable (15.5) release.

Bindings for the new **BusinessChat** framework are now available along API additions in beta 3 and 4.


## February 15, 2018 - Xamarin.iOS 11.6.99.33

This version is available as a *web preview*. It will work correctly with the current stable Visual Studio for Mac (7.3) and Visual Studio 2017 (15.5) on Windows.

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

### MetalPerformanceShaders Bindings

Changes introduced to MPS in Xcode 9.3 are marked as experimental, we will wait for Apple to make the API stable before [binding them](https://github.com/xamarin/xamarin-macios/issues/3553) so we do not introduce unnecessary breaking changes later.


## API Diff

The following documents contains a complete list of the API changes since our (11.6) stable release:

* [iOS](/releases/ios/api_changes/ios_11.8.0_to_11.9.0)
* [tvOS](/releases/ios/api_changes/tvos_11.8.0_to_11.9.0)
* [watchOS](/releases/ios/api_changes/watchos_11.8.0_to_11.9.0)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode9.3`
* [mono](https://github.com/mono/mono/tree/d15-6-2017-10) branch `d15-6-2017-10`
