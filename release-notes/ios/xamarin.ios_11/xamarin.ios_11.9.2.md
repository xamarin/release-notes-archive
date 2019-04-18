---
id: 5C04A916-2BCF-4FC4-B5D4-D215851CD210
title: "Xamarin.iOS 11.9.2"
---

# Xamarin.iOS 11.9.2 
Last Update: 4/16/2018

[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](#release-blog) | [Feedback](#feedback) | [Open Source](#open-source)

This version of Xamarin.iOS corresponds to our **xcode9.4** (`xcode9.4`) milestone. This is presently based on our stable `d15-6` milestone, i.e. Xamarin.iOS 11.9.x.

### Requirements

* The latest features and API requires Xcode 9.4 beta 1 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 9.4 requires a Mac running OSX 10.13.2 (High Sierra) or newer

## What's New in this Release

* [ClassKit API](#classkit-api)
* [Support for Xcode 9.4](#support-for-xcode-94)

### ClassKit API

[ClassKit](https://developer.apple.com/documentation/classkit?language=objc) is the major reason for Xcode 9.4 and iOS 11.4. This preview adds complete bindings for the API provided in the ClassKit framework.

In order to develop ClassKit-enabled applications, you'll need extra resources, e.g. **Schoolwork**, from Apple. You can request access using this [form](https://developer.apple.com//contact/classkit/). More information about testing ClassKit-enabled application can be found in the [ClassKit documentation](https://developer.apple.com/documentation/classkit/testing_your_app_during_development?language=objc).

Building ClassKit-enabled applications also requires enabling a capability and a special entitlement. Our existing (stable) versions of Visual Studio (Windows and Mac) do not support this yet. See the [Known Issues](#known-issues) section for details and workaround.

For reference you can also look at our [C# port](https://github.com/xamarin/ios-samples/tree/xcode9.4/ios11/GreatPlays) of Apple's  [IncorporatingClassKitIntoAnEducationalApp](https://developer.apple.com/documentation/classkit/incorporating_classkit_into_an_educational_app?language=objc) sample on github.

### Support for Xcode 9.4

The SDK tooling has been updated to

* Support the new OS from simulators: iOS 11.4 and tvOS 11.4
* Support launching to devices

As usual for beta software please make sure to read the [Xcode](https://developer.apple.com/go/?id=xcode-9.4-beta-rn), operating system ([iOS](https://developer.apple.com/go/?id=ios-11.4-sdk-rn), [tvOS](https://developer.apple.com/go/?id=tvos-11.4-sdk-rn), and [watchOS](https://developer.apple.com/go/?id=watchos-4.3.1-sdk-rn)) release notes to learn about known issues and workarounds.

## Notable Changes

### Release History

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## Known Issues

### ClassKit Entitlements

ClassKit-enabled applications must be built with a special entitlement. Until the new release of Visual Studio (Windows or Mac) is available you must configure this manually. Complete instructions on how to add this entitlement are available on [this GitHub issue](https://github.com/xamarin/xamarin-macios/issues/3911).

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API is missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since our (11.6) stable release:

* [iOS](/releases/ios/api_changes/ios-11-9-1-11-9-2)
* [tvOS](/releases/ios/api_changes/tvos-11-9-1-11-9-2)
* [watchOS](/releases/ios/api_changes/watchos-11-9-1-11-9-2)

This is a live document so there's no static list to link to. However, our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce this information for every commit that is being built. Pick a build based on `master` and look for the **API diff** link in the left column.

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode9.4`
* [mono](https://github.com/mono/mono/tree/d15-5-2017-06) branch `d15-5-2017-06`

### Continuous Builds 

All of our builds are also available for [download on Jenkins](https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode9.4/). Note: these builds come from our build bots and receive **no** QA testing. Verified builds are periodically made available.

Our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce the **API diff** for every commit that is being built.

You can track the latest status of our API work from our [wiki](https://github.com/xamarin/xamarin-macios/wiki/xcode9.4-Bindings-Status).
