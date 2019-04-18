---
id: 46da5cd4-3f29-4672-9ec4-d9b2c9470408
title: "Xamarin.Mac 4.8"
---

# Xamarin.Mac 4.8
Last Update: 9/11/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and API requires Xcode 9.4 and the bundled macOS SDKs
* Apple Xcode 9.4 requires a Mac running OSX 10.13.2 (High Sierra) or newer

## What's New in this Release

## Release History

This version of Xamarin.Mac corresponds to our **15.9** (`d15-9`) milestone.

* September 11, 2018 - Xamarin.Mac 4.8.0.22
* August 21, 2018 - Xamarin.Mac 4.8.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## September 11, 2018 - Xamarin.Mac 4.8.0.22

> This version is included in the Visual Studio 2017 version 15.9 Preview 2 release.

### Enhancements

* [4133](https://github.com/xamarin/xamarin-macios/issues/4133) -  [foundation] Add more useful information inside `NSErrorException.Message` property
* [4271](https://github.com/xamarin/xamarin-macios/issues/4271) -  [runtime] Make exception marshaling work with system mono
* [4308](https://github.com/xamarin/xamarin-macios/issues/4308) -  [open source] Fix resetting a README dependency when the hash exists, but the branch does not
* [4442](https://github.com/xamarin/xamarin-macios/issues/4442) -  [open source] Update `runtime.h` to fix build errors with Embeddinator 4000
* [4569](https://github.com/xamarin/xamarin-macios/issues/4569) -  [mmp] Show a nice error if user tries to build a 32-bit app with Xcode 10

### Issues Fixed

* [3724](https://github.com/xamarin/xamarin-macios/issues/3724) -  [debugger] Cannot step into the `NSUrlSessionHandler.cs` code
* [4130](https://github.com/xamarin/xamarin-macios/issues/4130) -  [runtime] Always release blocks on the main thread (crash in `WKWebView`)
* [4235](https://github.com/xamarin/xamarin-macios/issues/4235) -  [msbuild] Fix `error MT0099 : Internal error : Not all assemblies for Xamarin.Sdk have link tasks`
* [4237](https://github.com/xamarin/xamarin-macios/issues/4237) -  [msbuild] Fix `MT2002: Failed to resolve assembly: ...`
* [4254](https://github.com/xamarin/xamarin-macios/issues/4254) -  [objcruntime] `Class.GetHandle` not handle byref types (crash linked to becomeFirstResponder)
* [4384](https://github.com/xamarin/xamarin-macios/issues/4384) -  [mmp] Fix `MissingMethodException` when mono 5.12 is used
* [4422](https://github.com/xamarin/xamarin-macios/issues/4422) -  [mmp] Fix `no type or protocol named 'MTKViewDelegate'` after adding `mtouch` argument `--registrar:static`
* [4594](https://github.com/xamarin/xamarin-macios/issues/4594) -  [mmp] Ensure additional arguments are last (and can override msbuild arguments from response file)

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono 2018-04](https://github.com/mono/mono/commits/2018-04).


## August 21, 2018 - Xamarin.Mac 4.8.0.1

> This version is included in the Visual Studio 2017 version 15.9 Preview 1 release.

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono 2018-02](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

## API Diff

This [document](/releases/mac/api_changes/macos-4-6-0-4-8-0) contains a complete list of the API changes since the Xamarin.Mac 4.6 stable release.

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-9`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`
