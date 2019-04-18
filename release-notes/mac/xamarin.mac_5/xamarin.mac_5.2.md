---
id: 46da5cd4-3f29-4672-9ec4-d9b2c9470502
title: "Xamarin.Mac 5.2"
---

# Xamarin.Mac 5.2
Last Update: 12/11/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and APIs require Xcode 10.1 and the bundled macOS SDK
* Apple Xcode 10.1 requires a Mac running macOS 10.13.6 (High Sierra) or newer

## What's New in this Release

There are two major improvements worth calling out:

- Improved 10.14 support - In some cases drawing corruptions could occur in AppKit, causing rather strange behavior.
- Improved build performance - In many cases actool was running every build, unnecessarily forcing rebuilds in common cases. By caching these results, build times after no changes are significantly improved.


## Release History

This version of Xamarin.Mac corresponds to our **15.9** (`d15-9`) milestone.

* December 11, 2018 - Xamarin.Mac 5.2.1.12
* November 28, 2018 - Xamarin.Mac 5.2.1.11
* November 7, 2018 - Xamarin.Mac 5.2.1.10
* October 24, 2018 - Xamarin.Mac 5.2.1.9
* October 2, 2018 - Xamarin.Mac 5.2.0.0
* September 11, 2018 - Xamarin.Mac 4.8.0.22
* August 21, 2018 - Xamarin.Mac 4.8.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## December 11, 2018 - Xamarin.Mac 5.2.1.12

> This version is included in the Visual Studio 2017 version 15.9 SR4 release.

### Issues Fixed

[CVE-2018-8292 | Xamarin.Mac Information Disclosure Vulnerability](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2018-8292)

An information disclosure vulnerability exists in Xamarin.Mac when authentication information is inadvertently exposed in a redirect when the CFNetworkHandler or MessageHandler for HttpClient are used. The NSUrlSessionHandler and the managed HttpMessageHandler are not affected.

An attacker who successfully exploited this vulnerability could use the information to further compromise the web application.

The security update addresses the vulnerability by correcting how Xamarin.Mac handles redirects.

## November 28, 2018 - Xamarin.Mac 5.2.1.11

> This version is included in the Visual Studio for Mac 7.7 (15.9) RTW release.

### Issues Fixed

* [5158](https://github.com/xamarin/xamarin-macios/issues/5158) -  [bcl] Incomplete `System.Threading.Tasks.Extensions` Facade

## November 7, 2018 - Xamarin.Mac 5.2.1.10

> This version is included in the Visual Studio 2017 version 15.9 Preview 5 release.

This version includes support for Xcode 10.1.

## October 24, 2018 - Xamarin.Mac 5.2.1.9

> This version is included in the Visual Studio 2017 version 15.9 Preview 4 release.

### Issues Fixed

* [4848](https://github.com/xamarin/xamarin-macios/issues/4848) - [runtime] NSAlertView on Mojave appears blank
* [4509](https://github.com/xamarin/xamarin-macios/issues/4509) - [runtime] Close button disappeared

### Enhancements

* [3584](https://github.com/xamarin/xamarin-macios/issues/3584) - [msbuild] Cache actool results


## October 2, 2018 - Xamarin.Mac 5.2.0.0

> This version is included in the Visual Studio 2017 version 15.9 Preview 3 release.

### Enhancements

* [693034](https://devdiv.visualstudio.com/DevDiv/_workitems/edit/693034) -  Include Xcode 10 support (SDK, API and tools) from Xamarin.Mac 5.0

### Issues Fixed

* [3976](https://github.com/xamarin/xamarin-macios/issues/3976) -  [mmp] Add automatic detection of `NetworkExtension.framework` usage


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

This [document](/releases/mac/api_changes/macos-5-0-0-5-2-1) contains a complete list of the API changes since the Xamarin.Mac 5.0 stable release.

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-9`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`
