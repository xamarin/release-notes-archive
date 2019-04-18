---
id: BF38F4D0-56F5-476F-826F-2A6A2FB9D8E9
title: "Xamarin.Mac 4.1.99"
---

# Xamarin.Mac 4.1.99
Last Update: 02/15/2018

[Getting Started](https://developer.xamarin.com/guides/mac/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Feedback](#feedback) | [Open Source](#open-source)

This version of Xamarin.Mac corresponds to our xcode9.3 (xcode9.3) milestone. This is presently based on our stable d15-5 milestone, i.e. Xamarin.Mac 4.0.x.

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled macOS SDKs;
* Apple Xcode 9.3 requires a Mac running macOS 10.13.2 (High Sierra) or newer;

## What's New in this Release

There were very few changes in the SDK. Beta 2 introduced **BusinessChat** for macOS (and iOS) and this will be included in a future preview.

Other changes can be seen in the [API diff](#api-diff) section of this document.

## Release History
* February 15, 2018 - Xamarin.Mac 4.1.99.84

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## February 15, 2018 - Xamarin.Mac 4.1.99.84

This version is available as a *web preview*. It will work correctly with the current stable Visual Studio for Mac (7.3).

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MM0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MM4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).


## API Diff

The following documents contains a complete list of the API changes since our (4.0) stable release:

* [macOS](/releases/mac/api_changes/mac_4.0_to_4.1.99.84)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode9.3`
* [mono](https://github.com/mono/mono/tree/2017-10) branch `d15-5-2017-06`

### Continuous Builds 
All of our builds are also available for [download on Jenkins](https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode9.3/). Note: these builds come from our build bots and receive **no** QA testing. Verified builds are periodically made available.

Our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce the **API diff** for every commit that is being built.

You can track the latest status of our API work from our [wiki](https://github.com/xamarin/xamarin-macios/wiki/xcode9.3-Bindings-Status).
