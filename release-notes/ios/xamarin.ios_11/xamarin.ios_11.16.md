---
id: ca54591e-f09d-4059-a60d-6a4a8c461116
title: "Xamarin.iOS 11.16"
---

# Xamarin.iOS 11.16
Last Update: 9/11/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and APIs requires Xcode 9.4 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 9.4 requires a Mac running OSX 10.13.2 (High Sierra) or newer

## What's New in this Release

### Release History

This version of Xamarin.iOS corresponds to our **15.9** (`d15-9`) milestone.

* September 11, 2018 - Xamarin.iOS 11.16.0.22
* August 21, 2018 - Xamarin.iOS 11.16.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## September 11, 2018 - Xamarin.iOS 11.16.0.22

> This version is included in the Visual Studio 2017 version 15.9 Preview 2 release.

### Enhancements

* [4133](https://github.com/xamarin/xamarin-macios/issues/4133) -  [foundation] Add more useful information inside `NSErrorException.Message` property
* [4308](https://github.com/xamarin/xamarin-macios/issues/4308) -  [open source] Fix resetting a README dependency when the hash exists, but the branch does not
* [4442](https://github.com/xamarin/xamarin-macios/issues/4442) -  [open source] Update `runtime.h` to fix build errors with Embeddinator 4000

### Issues Fixed

* [3724](https://github.com/xamarin/xamarin-macios/issues/3724) -  [debugger] Cannot step into the `NSUrlSessionHandler.cs` code
* [4130](https://github.com/xamarin/xamarin-macios/issues/4130) -  [runtime] Always release blocks on the main thread (crash in `WKWebView`)
* [4235](https://github.com/xamarin/xamarin-macios/issues/4235) -  [msbuild] Fix `error MT0099 : Internal error : Not all assemblies for Xamarin.Sdk have link tasks`
* [4237](https://github.com/xamarin/xamarin-macios/issues/4237) -  [msbuild] Fix `MT2002: Failed to resolve assembly: ...`
* [4254](https://github.com/xamarin/xamarin-macios/issues/4254) -  [objcruntime] `Class.GetHandle` not handle byref types (crash linked to becomeFirstResponder)
* [4384](https://github.com/xamarin/xamarin-macios/issues/4384) -  [mtouch] Fix `MissingMethodException` when mono 5.12 is used
* [4422](https://github.com/xamarin/xamarin-macios/issues/4422) -  [moutch] Fix `no type or protocol named 'MTKViewDelegate'` after adding `mtouch` argument `--registrar:static`
* [4467](https://github.com/xamarin/xamarin-macios/issues/4467) -  [msbuild] Fix build failures when a project contains '.ktx' file(s)
* [4594](https://github.com/xamarin/xamarin-macios/issues/4594) -  [mtouch] Ensure additional arguments are last (and can override msbuild arguments from response file)


### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 2018-04](https://github.com/mono/mono/commits/2018-04).

## August 21, 2018 - Xamarin.iOS 11.16.0.1

> This version is included in the Visual Studio 2017 version 15.9 Preview 1 release.

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 2018-02](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.10/).

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if APIs are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.14 stable release:

* [iOS](/releases/ios/api_changes/ios-11-14-0-11-16-0)
* [tvOS](/releases/ios/api_changes/tvos-11-14-0-11-16-0)
* [watchOS](/releases/ios/api_changes/watchos-11-14-0-11-16-0)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-9`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`
