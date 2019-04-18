---
id: 4a11681a-125a-4c0b-a576-7ade8cbbc501
title: "Xamarin.Mac 5.1"
---

# Xamarin.Mac 5.1
Last Update: 10/22/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

### Requirements

* The latest features and APIs require Xcode 10.1 beta 3 and the bundled macOS SDK
* Apple Xcode 10.1 requires a Mac running macOS 10.13.6 (High Sierra) or newer

## What's New in this Release

* [Support for Xcode 10.1]()
* [Support for macOS 10.14.1]()
* [Other Changes]()

### Support for Xcode 10,.1

For more information you can consult the [Xcode 10.1](https://developer.apple.com/go/?id=xcode-10.1-beta-rn) release notes from Apple.

### Support for macOS 10.14.1

For more information you can consult the [macOS 10.14.1](https://developer.apple.com/go/?id=macos-10.14.1-beta-rn) release notes from Apple.

## Release History

This version of Xamarin.iOS correspond to our `xcode10.1` milestone and is based of the stable **15.8** release.

* October 22, 2018 - Xamarin.Mac 5.1.0.14

## October 1, 2018 - Xamarin.Mac 5.1.0.14

This release is based on the Xcode 10.1 beta 3 release.

### Issue Fixed

* [4988](https://github.com/xamarin/xamarin-macios/pull/4988) - [mediaplayer] Fix NRE in `MPNowPlayingInfoCenter` wrt null dictionary entries

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MM0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MM4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).


## API Diff

The following documents contains a complete list of the API changes since our (5.0) stable release:

* [macOS](/releases/mac/api_changes/macos-5-0-0-5-1-0)

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [xamarin-macios Issue Tracker](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode10.1`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
