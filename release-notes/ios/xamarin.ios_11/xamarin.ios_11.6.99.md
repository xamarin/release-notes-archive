---
id: 14CF4515-81E1-4E75-BBAE-4F83F5535C63
title: "Xamarin.iOS 11.6.99"
---

# Xamarin.iOS 11.6.99
Last Update: 2/14/2018

[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Feedback](#feedback) | [Open Source](#open-source)

This version of Xamarin.iOS corresponds to our **xcode9.3** (`xcode9.3`) milestone. This is presently based on our stable `d15-5` milestone, i.e. Xamarin.iOS 11.6.x.

#### Requirements

* The latest features and API requires Xcode 9.3 beta 2 and the bundled iOS, tvOS and watchOS SDKs;
* Apple Xcode 9.3 requires a Mac running OSX 10.13.2 (High Sierra) or newer;

## What's New in this Release

* [Support for Xcode 9.3](#support-for-xcode-93)
* [Additional API](#additional-api)

### Support for Xcode 9.3

The SDK tooling has been updated to

* Support the new OS from simulators: iOS 11.3, tvOS 11.3 and watchOS 4.3;
* Support launching to devices;

### Additional API

There were very few changes in the SDK. Beta 2 introduced **BusinessChat** for iOS (and macOS) and this will be included in a future preview.

Other changes can be seen in the [API diff](#API Diff) section of this document.

## Release History
* February 15, 2018 - Xamarin.iOS 11.6.99.33

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## February 15, 2018 - Xamarin.iOS 11.6.99.33

This version is available as a *web preview*. It will work correctly with the current stable Visual Studio for Mac (7.3) and Visual Studio 2017 (15.5) on Windows.

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since our (11.6) stable release:

* [iOS](/releases/ios/api_changes/ios_11.6.1_to_11.6.99)
* [tvOS](/releases/ios/api_changes/tvos_11.6.1_to_11.6.99)
* [watchOS](/releases/ios/api_changes/watchos_11.6.1_to_11.6.99)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode9.3`
* [mono](https://github.com/mono/mono/tree/d15-5-2017-06) branch `d15-5-2017-06`

### Continuous Builds 
All of our builds are also available for [download on Jenkins](https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode9.3/). Note: these builds come from our build bots and receive **no** QA testing. Verified builds are periodically made available.

Our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce the **API diff** for every commit that is being built.

You can track the latest status of our API work from our [wiki](https://github.com/xamarin/xamarin-macios/wiki/xcode9.3-Bindings-Status).
