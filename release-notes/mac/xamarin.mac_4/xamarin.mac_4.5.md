---
id: 46da5cd4-3f29-4672-9ec4-d9b2c947b851
title: "Xamarin.Mac 4.5"
---

# Xamarin.Mac 4.5
Last Update: 5/31/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#Whats_New_in_this_Release) | [Known Issues](#Known_Issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#Open_Source)

#### Requirements

* The latest features and API requires Xcode 9.3 and the bundled macOS SDKs;
* Apple Xcode 9.3 requires a Mac running macOS 10.13 (High Sierra) or newer;

## What's New in this Release

* [API Enhancements](#API_Enhancements)
* [Tooling Enhancements](#Tooling_Enhancements)

### API Enhancements

* [3544](https://github.com/xamarin/xamarin-macios/pull/3544) -  [foundation] Avoid unnecessary native calls for `NSNull.Null`
* [3968](https://github.com/xamarin/xamarin-macios/pull/3968) -  [foundation] Implement NSUrlProtocolClient properly on macOS
* [4001](https://github.com/xamarin/xamarin-macios/pull/4001) -  [security] Enable `SSL[Get|Set]AlpnProtocols` since it's now available in macOS 10.13.4

### Tooling Enhancements

* [3525](https://github.com/xamarin/xamarin-macios/pull/3525) -  Build assemblies we ship deterministically, i.e. `csc -deterministic`
* [3926](https://github.com/xamarin/xamarin-macios/issues/3926) -  [msbuild] Use a response file in `MmpTaskBase`
* [3869](https://github.com/xamarin/xamarin-macios/issues/3869) -  [generator] Allow `[WrapAttribute]` usage with interface protocols

## Release History

This version Xamarin.Mac correspond to our **15.8** (`d15-8`) milestone.

* May 31, 2018 - Xamarin.Mac 4.5.0.280
* May 7, 2018 - Xamarin.Mac 4.5.0.280

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## May 31, 2018 - Xamarin.Mac 4.5.0.331

> This version is included in the Visual Studio 2017 version 15.8 Preview 2 release.

### Issues Fixed

* [4030](https://github.com/xamarin/xamarin-macios/issues/4030) -  [scenekit] `SCNPhysicsShape.Create` transforms parameter is bound incorrectly
* [4031](https://github.com/xamarin/xamarin-macios/issues/4031) -  [scenekit] `SCNHitTestOptions SearchMode` bound incorrectly
* [4067](https://github.com/xamarin/xamarin-macios/issues/4067) -  [msbuild] Unable to build CocoaApp with Modern target after adding .NET Standard 2.0 library
* [4072](https://github.com/xamarin/xamarin-macios/issues/4072) -  [mtouch][mmp] `BlockProxy` attribute with invalid type will cause `MT0000` build error
* [4087](https://github.com/xamarin/xamarin-macios/issues/4087) -  [scenekit] Crash when setting RenderingApi on `SCNRenderingOptions`

## May 7, 2018 - Xamarin.Mac 4.5.0.280

> This version is included in the Visual Studio 2017 version 15.8 Preview 1 release.

### Issues Fixed

* [3199](https://github.com/xamarin/xamarin-macios/issues/3199) - [msbuild] Skip reference assemblies passed to `mmp`
* [3674](https://github.com/xamarin/xamarin-macios/issues/3674) - [msbuild] Correctly determine whenther Xamarin.Mac builds require a provisioning profile
* [3716](https://github.com/xamarin/xamarin-macios/issues/3716) - [gameplaykit] Fix naming of `GKNoise.DisplaceX`
* [3778](https://github.com/xamarin/xamarin-macios/issues/3778) - [appkit] Adds `[NullAllowed]` to `NSTableView.RegisterNib`
* [3779](https://github.com/xamarin/xamarin-macios/issues/3779) - [appkit] Adds `[NullAllowed]` to `NSGridCell.ContentView`
* [3792](https://github.com/xamarin/xamarin-macios/issues/3792) - [appkit] Adds `[NullAllowed]` to `NSTableCellView.ObjectValue`
* [3824](https://github.com/xamarin/xamarin-macios/issues/3824) - [appkit] Fix default values for touchbar APIs in `NSTextViewDelegate`
* [3830](https://github.com/xamarin/xamarin-macios/issues/3830) - [runtime] Don't throw exceptions when checking if a token reference exists (and not finding any)
* [3868](https://github.com/xamarin/xamarin-macios/issues/3868) - [appkit] Fix stack overflow in `NSApplication.NextEvent` binding
* [3871](https://github.com/xamarin/xamarin-macios/pull/3871) - [coretext] Fix `GetMatchingFontDescriptors` overload with sort callback
* [3905](https://github.com/xamarin/xamarin-macios/pull/3905) - [msbuild] Catch `ArgumentException` if `IBToolTask` fails to load plist output
* [3922](https://github.com/xamarin/xamarin-macios/issues/3922) - [msbuild] Fixed `TargetDevice` typo
* [3943](https://github.com/xamarin/xamarin-macios/issues/3943) - [runtime] Don't lock while calling selectors that can up calling managed code
* [3944](https://github.com/xamarin/xamarin-macios/issues/3944) - [spritekit] Fix `SKActionTimingFunction` delegate signature

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

## Known Issues
<!---
// These should be defined as a [KNOWN ISSUE](https://devdiv.visualstudio.com/DevDiv/_wiki?pagePath=%2FXamarin%2FPM-Team%2FRelease-Notes-Reform%2FGuide-to-Release-Notes).
### {Title}
{Paragraph detailing known issue}
{Links to respective bug or devcom item}
-->

## API Diff

This [document](/releases/mac/api_changes/macos-4-4-99-4-5-0) contains a complete list of the API changes since the Xamarin.Mac 4.4 stable release.

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://bugzilla.xamarin.com/enter_bug.cgi?product=Xamarin.Mac).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `master`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
