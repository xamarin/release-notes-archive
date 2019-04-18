---
id: 46da5cd4-3f29-4672-9ec4-d9b2c9470503
title: "Xamarin.Mac 5.3"
---

# Xamarin.Mac 5.3
Last Update: 12/4/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and APIs require Xcode 10.1 and the bundled macOS SDK
* Apple Xcode 10.1 requires a Mac running macOS 10.13.6 (High Sierra) or newer

## What's New in this Release

## Release History

This version of Xamarin.Mac corresponds to our **16.0** (`d16-0`) milestone.

* December 4, 2018 - Xamarin.Mac 5.3.1.28

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## December 4, 2018 - Xamarin.Mac 5.3.1.28

> This version is **not** installed by default with Visual Studio 2019 version 16.0 preview 1 release. To install it please follow the instructions from this [document](https://docs.microsoft.com/xamarin/ios/get-started/installation/windows/connecting-to-mac/2019-preview).

### Enhancements

* [3675](https://github.com/xamarin/xamarin-macios/issues/3675) - [bgen] Remove unneeded bmac-mobile-mono from binding projects and stop shipping it
* [4255](https://github.com/xamarin/xamarin-macios/issues/4255) - [registrar] Ignore availability warnings from clang
* [4525](https://github.com/xamarin/xamarin-macios/issues/4525) - [scenekit] Add advice to `SCNMatrix4` about it's row major representation
* [4549](https://github.com/xamarin/xamarin-macios/issues/4549) - [mtouch/mmp/docs] Improve MT0091 to include how to enable the linker
* [4688](https://github.com/xamarin/xamarin-macios/issues/4688) - [coremedia] Expose the `CMSampleAttachmentKey` interface.
* [4813](https://github.com/xamarin/xamarin-macios/issues/4813) - [foundation] Add bindings for `NSMutableDictionary addEntriesFromDictionary:`

### Issues Fixed

* [4102](https://github.com/xamarin/xamarin-macios/issues/4102) - [runtime] Add support for delegates as return values in protocol members
* [4611](https://github.com/xamarin/xamarin-macios/issues/4611) - [metal] Fix incorrect structure sizes in `Metal/Defs.cs`
* [4988](https://github.com/xamarin/xamarin-macios/issues/4988) - [mediaplayer] Fix NRE in `MPNowPlayingInfoCenter` wrt `null` dictionary entries

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from 
[Mono 5.14](http://www.mono-project.com/docs/about-mono/releases/5.14.0/)
[Commit 969357ac](https://github.com/mono/mono/commit/969357ac02b2c08a43ef89d98aca550d3648bf00)

## API Diff

This [document](/releases/mac/api_changes/macos-5-2-1-5-3-1) contains a complete list of the API changes since the Xamarin.Mac 5.2 stable release.

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d16-0-p1`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`

### Contributors

A big ***Thank You!*** to contributors who made improvements in this release:

* [Michał Żołnieruk](https://github.com/miszu): [Added two missing NSString method bindings for splitting text](https://github.com/xamarin/xamarin-macios/pull/4828)
* [Curtis Wensley](https://github.com/cwensley): [Add NullAllowed for GetContentSizeForFrame and GetFrameSizeForContent parameters](https://github.com/xamarin/xamarin-macios/pull/4714)
