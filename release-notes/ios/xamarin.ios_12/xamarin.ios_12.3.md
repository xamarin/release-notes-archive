---
id: ca54591e-f09d-4059-a60d-6a4a8c461203
title: "Xamarin.iOS 12.3"
---

# Xamarin.iOS 12.3
Last Update: 12/4/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and APIs requires Xcode 10.1 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 10.1 requires a Mac running OSX 10.13.6 (High Sierra) or newer

## What's New in this Release

## Release History

This version of Xamarin.iOS corresponds to our **16.0** (`d16-0`) milestone.

* December 4, 2018 - Xamarin.iOS 12.3.1.28

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## December 4, 2018 - Xamarin.iOS 12.3.1.28

> This version is **not** installed by default with Visual Studio 2019 version 16.0 preview 1 release. To install it please follow the instructions from this [document](https://docs.microsoft.com/xamarin/ios/get-started/installation/windows/connecting-to-mac/2019-preview).

### Enhancements

* [4255](https://github.com/xamarin/xamarin-macios/issues/4255) - [registrar] Ignore availability warnings from clang
* [4430](https://github.com/xamarin/xamarin-macios/issues/4430) - [debugger] Wireless Debugging Warning Still Appears After Disabled in VS and XCode
* [4525](https://github.com/xamarin/xamarin-macios/issues/4525) - [scenekit] Add advice to `SCNMatrix4` about it's row major representation
* [4549](https://github.com/xamarin/xamarin-macios/issues/4549) - [mtouch/mmp/docs] Improve MT0091 to include how to enable the linker
* [4688](https://github.com/xamarin/xamarin-macios/issues/4688) - [coremedia] Expose the `CMSampleAttachmentKey` interface.
* [4813](https://github.com/xamarin/xamarin-macios/issues/4813) - [foundation] Add bindings for `NSMutableDictionary addEntriesFromDictionary:`
* [4893](https://github.com/xamarin/xamarin-macios/issues/4893) - [uikit] Duplicate bindings for 'UIScrollView.ContentOffset' to get correct availability information

### Issues Fixed

* [4102](https://github.com/xamarin/xamarin-macios/issues/4102) - [runtime] Add support for delegates as return values in protocol members
* [4611](https://github.com/xamarin/xamarin-macios/issues/4611) - [metal] Fix incorrect structure sizes in `Metal/Defs.cs`
* [4988](https://github.com/xamarin/xamarin-macios/issues/4988) - [mediaplayer] Fix NRE in `MPNowPlayingInfoCenter` wrt `null` dictionary entries

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from 
[Mono 5.14](http://www.mono-project.com/docs/about-mono/releases/5.14.0/)
[Commit 969357ac](https://github.com/mono/mono/commit/969357ac02b2c08a43ef89d98aca550d3648bf00)

## Known Issues

* [5129](https://github.com/xamarin/xamarin-macios/issues/5129) - Build error for library project with SceneKit asset.

    Library projects with SceneKit assets may fail to compile due to an
    MSBuild variable not being set:

        error MSB4044: The "CompileSceneKitAssets" task was not given a value for the required parameter "AppBundleDir".

    The workaround is to manually set the variable by adding the following
    line to the library project's .csproj file:

        <AppBundleDir>$(IntermediateOutputPath)MyAppName.app</AppBundleDir>

### 64 bits watchOS support

* Xcode 10 GM added support for 64 bits watch application, aka `arm64_32`. The current app store submission process **requires** this architecture to be included in your application when including watch support. You can workaround this with [https://github.com/xamarin/xamarin-macios/issues/4810#issuecomment-421338365](these instructions).

* Trying to run a watch app on the new Series 4 Apple Watch will fail with this error:

        IncorrectArchitecture: Failed to find matching arch for 32-bit Mach-O input file ...
        error MT1006: Could not install the application 'MyTestApp.app' on the device 'MyDevice': AMDeviceSecureInstallApplicationBundle returned: 0xe8000087 (kAMDIncorrectArchitectureError).

     This is because the S4 device can only execute native `arm64_32` code, not `armv7k` like previous watches.

     Please read https://github.com/xamarin/xamarin-macios/issues/4864 for more information and a workaround.

### Apple Breaking Changes

* [rdar://41123682]() Apple changed `TVElementUpdateType*` enum values. Please test your application if you're using this type.
* [rdar://43425168]() Apple changed `IN*WorkoutIntentResponseCode` enum values. Please test your application if you're using this type.

### Apple Non-Breaking Issues

* [rdar://41135211]() `RPBroadcastPickerView` symbol is not present in simulator. If needed you'll need to test this on devices.

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if APIs are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 12.2 stable release:

* [iOS](/releases/ios/api_changes/ios-12-2-1-12-3-1)
* [tvOS](/releases/ios/api_changes/tvos-12-2-1-12-3-1)
* [watchOS](/releases/ios/api_changes/watchos-12-2-1-12-3-1)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d16-0-p1`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`

### Contributors

A big ***Thank You!*** to contributors who made improvements in this release:

* [Michał Żołnieruk](https://github.com/miszu): [Added two missing NSString method bindings for splitting text](https://github.com/xamarin/xamarin-macios/pull/4828)
