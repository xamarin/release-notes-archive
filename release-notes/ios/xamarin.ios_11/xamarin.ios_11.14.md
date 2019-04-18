---
id: ca54591e-f09d-4059-a60d-6a4a8c46316f
title: "Xamarin.iOS 11.14"
---

# Xamarin.iOS 11.14
Last Update: 8/20/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and API requires Xcode 9.4 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 9.4 requires a Mac running OSX 10.13.2 (High Sierra) or newer

## What's New in this Release

* [API Enhancements](#api-enhancements)
* [Tooling Enhancements](#tooling-enhancements)
* [Performance Enhancements](#performance-enhancements)

### API Enhancements

* [3544](https://github.com/xamarin/xamarin-macios/pull/3544) -  [foundation] Avoid unnecessary native calls for `NSNull.Null`
* [3870](https://github.com/xamarin/xamarin-macios/pull/3870) -  [arkit] Add missing `ARHitTestResultType.EstimatedVerticalPlane`

### Tooling Enhancements

* [3525](https://github.com/xamarin/xamarin-macios/pull/3525) -  Build assemblies we ship deterministically, i.e. `csc -deterministic`
* [3926](https://github.com/xamarin/xamarin-macios/issues/3926) -  [msbuild] Use a response file in `MmpTaskBase`
* [3869](https://github.com/xamarin/xamarin-macios/issues/3869) -  [generator] Allow `[WrapAttribute]` usage with interface protocols

### Performance Enhancements

- Optimize [IsCustomType](https://github.com/xamarin/xamarin-macios/pull/4161), which can dramatically improves creating new `NSObject` instances under the dynamic registrar. 
- Optimize [NSActionDispatcher](https://github.com/xamarin/xamarin-macios/pull/4162) to reduce allocations and number of indirections in event callbacks.
- Optimize [IsArchEnabled](https://github.com/xamarin/xamarin-macios/pull/4149) in `mtouch`.
- Optimize [ReaderParameters instances in CoreResolver](https://github.com/xamarin/xamarin-macios/pull/4151) which is used at build time by `mtouch`.

### Release History

This version Xamarin.iOS correspond to our **15.8** (`d15-8`) milestone.

* August 20, 2018 - Xamarin.iOS 11.14.0.13
* July 24, 2018 - Xamarin.iOS 11.14.0.11
* July 11, 2018 - Xamarin.iOS 11.14.0.10
* June 21, 2018 - Xamarin.iOS 11.14.0.4
* May 31, 2018 - Xamarin.iOS 11.11.0.331
* May 7, 2018 - Xamarin.iOS 11.11.0.280

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## August 20, 2018 - Xamarin.iOS 11.14.0.13

> This version is included in the Visual Studio 2017 version 15.8 stable release.

### Issue Fixed

* [649776](https://devdiv.visualstudio.com/DevDiv/_workitems/edit/649776) - [msbuild] Don't put gcc/linker flags in the response file, since Mono.Options doesn't support escaping quotes

## July 24, 2018 - Xamarin.iOS 11.14.0.11

> This version is included in the Visual Studio 2017 version 15.8 Preview 5 release.

## July 11, 2018 - Xamarin.iOS 11.14.0.10

> This version is included in the Visual Studio 2017 version 15.8 Preview 4 release.

### Issues Fixed

* [8866](https://github.com/mono/mono/issues/8866) - [profiler] Fix `jit` profiler crash

## June 21, 2018 - Xamarin.iOS 11.14.0.4

> This version is included in the Visual Studio 2017 version 15.8 Preview 3 release.

This preview includes Xcode 9.4 support (API and tooling) first made available in [Xamarin.iOS 11.12](xamarin.ios_11.12).

A number of performance enhancements are also new:

- Optimize [IsCustomType](https://github.com/xamarin/xamarin-macios/pull/4161), which can dramatically improves creating new `NSObject` instances under the dynamic registrar. 
- Optimize [NSActionDispatcher](https://github.com/xamarin/xamarin-macios/pull/4162) to reduce allocations and number of indirections in event callbacks.
- Optimize [IsArchEnabled](https://github.com/xamarin/xamarin-macios/pull/4149) in `mtouch`.
- Optimize [ReaderParameters instances in CoreResolver](https://github.com/xamarin/xamarin-macios/pull/4151) which is used at build time by `mtouch`.

### Issues Fixed

* [4129](https://github.com/xamarin/xamarin-macios/issues/4129) -  [compression] Use the correct linking flags for older OS versions
* [4147](https://github.com/xamarin/xamarin-macios/pull/4147) -  [mono] Removal of `System.Memory` facade due to incompatibilities
* [4187](https://github.com/xamarin/xamarin-macios/pull/4187) -  [msbuild] Fix builds when using Xcode 10 beta 1


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

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.12 stable release:

* [iOS](/releases/ios/api_changes/ios-11-12-0-11-14-0)
* [tvOS](/releases/ios/api_changes/tvos-11-12-0-11-14-0)
* [watchOS](/releases/ios/api_changes/watchos-11-12-0-11-14-0)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-8`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`

### A big Thank You! to the following folks that helped to make Xamarin.iOS and Xamarin.Mac even better:

* [@filipnavara](https://github.com/filipnavara)
* [@kunigaku](https://github.com/kunigaku)
* [@NickSpag](https://github.com/NickSpag)
