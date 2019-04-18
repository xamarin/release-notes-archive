---
id: ca54591e-f09d-4059-a60d-5a4a8c46316f
title: "Xamarin.iOS 11.11"
---

# Xamarin.iOS 11.11
Last Update: 5/31/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#Whats_New_in_this_Release) | [Known Issues](#Known_Issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#Open_Source)

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled iOS, tvOS and watchOS SDKs;
* Apple Xcode 9.3 requires a Mac running OSX 10.13 (High Sierra) or newer;

## What's New in this Release

* [API Enhancements](#API_Enhancements)
* [Tooling Enhancements](#Tooling_Enhancements)

### API Enhancements

* [3544](https://github.com/xamarin/xamarin-macios/pull/3544) -  [foundation] Avoid unnecessary native calls for `NSNull.Null`
* [3870](https://github.com/xamarin/xamarin-macios/pull/3870) -  [arkit] Add missing `ARHitTestResultType.EstimatedVerticalPlane`

### Tooling Enhancements

* [3525](https://github.com/xamarin/xamarin-macios/pull/3525) -  Build assemblies we ship deterministically, i.e. `csc -deterministic`
* [3926](https://github.com/xamarin/xamarin-macios/issues/3926) -  [msbuild] Use a response file in `MmpTaskBase`
* [3869](https://github.com/xamarin/xamarin-macios/issues/3869) -  [generator] Allow `[WrapAttribute]` usage with interface protocols

### Release History

This version Xamarin.iOS correspond to our **15.8** (`d15-8`) milestone.

* May 31, 2018 - Xamarin.iOS 11.11.0.331
* May 7, 2018 - Xamarin.iOS 11.11.0.280

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## May 31, 2018 - Xamarin.iOS 11.11.0.331

> This version is included in the Visual Studio 2017 version 15.8 Preview 2 release.

### Issues Fixed

* [4030](https://github.com/xamarin/xamarin-macios/issues/4030) -  [scenekit] `SCNPhysicsShape.Create` transforms parameter is bound incorrectly
* [4031](https://github.com/xamarin/xamarin-macios/issues/4031) -  [scenekit] `SCNHitTestOptions SearchMode` bound incorrectly
* [4072](https://github.com/xamarin/xamarin-macios/issues/4072) -  [mtouch][mmp] `BlockProxy` attribute with invalid type will cause `MT0000` build error
* [4087](https://github.com/xamarin/xamarin-macios/issues/4087) -  [scenekit] Crash when setting RenderingApi on `SCNRenderingOptions`

## May 7, 2018 - Xamarin.iOS 11.11.0.280

> This version is included in the Visual Studio 2017 version 15.8 Preview 1 release.

### Issues Fixed

* [3199](https://github.com/xamarin/xamarin-macios/issues/3199) - [msbuild] Skip reference assemblies passed to `mmp`
* [3716](https://github.com/xamarin/xamarin-macios/issues/3716) - [gameplaykit] Fix naming of `GKNoise.DisplaceX`
* [3781](https://github.com/xamarin/xamarin-macios/pull/3781) - [mtouch] Use full path to `mono-symbolicate` instead of `UseShellExecute`
* [3830](https://github.com/xamarin/xamarin-macios/issues/3830) - [runtime] Don't throw exceptions when checking if a token reference exists (and not finding any)
* [3871](https://github.com/xamarin/xamarin-macios/pull/3871) - [coretext] Fix `GetMatchingFontDescriptors` overload with sort callback
* [3905](https://github.com/xamarin/xamarin-macios/pull/3905) - [msbuild] Catch `ArgumentException` if `IBToolTask` fails to load plist output
* [3922](https://github.com/xamarin/xamarin-macios/issues/3922) - [msbuild] Fixed `TargetDevice` typo
* [3933](https://github.com/xamarin/xamarin-macios/pull/3933) - [mtouch] Fix parsing of `--root-assembly`
* [3943](https://github.com/xamarin/xamarin-macios/issues/3943) - [runtime] Don't lock while calling selectors that can up calling managed code
* [3944](https://github.com/xamarin/xamarin-macios/issues/3944) - [spritekit] Fix `SKActionTimingFunction` delegate signature
* [60624](https://bugzilla.xamarin.com/show_bug.cgi?id=60624) - [mtouch] Ignore `objc-missing-super-calls` warnings from clang when compiling registrar code

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.10/).

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might requires workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.10 stable release:

* [iOS](/releases/ios/api_changes/ios-11-10-1-11-11-0)
* [tvOS](/releases/ios/api_changes/tvos-11-10-1-11-11-0)
* [watchOS](/releases/ios/api_changes/watchos-11-10-1-11-11-0)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `master`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
