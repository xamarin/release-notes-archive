---
id: 98b08969-abad-4016-9038-80e7991c0ff1
title: "Xamarin.iOS 11.8"
---

# Xamarin.iOS 11.8
Last Update: 3/5/2018 [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)

 [What's New](#Whats_New_in_this_Release)

 [Known Issues](#Known_Issues)

 [Blogs](https://blog.xamarin.com/tag/ios/)

 [Open Source](#Open_Source)



### Installing

* Visual Studio 2017 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)
* Visual Studio 2015 Tools for Xamarin – [Stable updater channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/#visualstudio)

#### Requirements

* The latest features and API requires Xcode 9.2 and the bundled iOS, tvOS and watchOS SDKs;
* Apple Xcode 9.2 requires a Mac running OSX 10.12.6 (Sierra) or newer;

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [GitHub Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

### Release History

This version Xamarin.iOS correspond to our **15.6** (`d15-6`) milestone.

* March 26, 2018 - Xamarin.iOS 11.8.1.28
* February 23, 2018 - Xamarin.iOS 11.8.0.20
* February 7, 2018 - Xamarin.iOS 11.8.0.19
* January 24, 2018 - Xamarin.iOS 11.8.0.8
* January 10, 2018 - Xamarin.iOS 11.8.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## March 26, 2018 - Xamarin.iOS 11.8.1.28

> This version is included in the Visual Studio 2017 version 15.6 Service Release 3.

### Issues Fixed

* [3289](https://github.com/xamarin/xamarin-macios/issues/3289) - [msbuild] "dyld: Library not loaded: @rpath/Mono.framework/Mono" when debugging tvOS
* [7472](https://github.com/mono/mono/issues/7472) - [runtime]  `NullReferenceException` when trying to use an extension method on a `null` object as an assignment value for an `Action` or `Func` variable

## February 23, 2018 - Xamarin.iOS 11.8.0.20

> This version is included in the Visual Studio 2017 version 15.6 RTW release.

### Issue Fixed

* [3241](https://github.com/xamarin/xamarin-macios/issues/3241) -  [llvm] Revert "[mini] Align stack when resuming to catch handler"


## February 7, 2018 - Xamarin.iOS 11.8.0.19

> This version is included in the Visual Studio 2017 version 15.6 Preview 4 release.

### Issues Fixed

* [3089](https://github.com/xamarin/xamarin-macios/issues/3089) -  [coregraphics] Fix `CGPath.MakeMutable` reference count
* [3215](https://github.com/xamarin/xamarin-macios/issues/3215) -  [linker] Fix general `MT2001` to report a useful `MT2002` error 
* [3241](https://github.com/xamarin/xamarin-macios/issues/3241) -  [mono] Fix runtime crash in `armv7/llvm` builds


## January 24, 2018 - Xamarin.iOS 11.8.0.8

> This version is included in the Visual Studio 2017 version 15.6 Preview 3 release.

### Issues Fixed

* [3140](https://github.com/xamarin/xamarin-macios/issues/3140) -  [vision] Removes incorrect `[Abstract]` from `VNDetectBarcodesRequest`
* [3145](https://github.com/xamarin/xamarin-macios/issues/3145) -  [scenekit] Crashes if `SCNAnimation.AnimationEvents` isn't empty
* [3146](https://github.com/xamarin/xamarin-macios/issues/3146) -  [scenekit] `SCNPhysicsWorld.ConvexSweepTest` method doesn't work
* [6428](https://github.com/mono/mono/issues/6428) -  [bcl] `DnsCallback` as async callback causing unhandled exception
* [52729](https://bugzilla.xamarin.com/show_bug.cgi?id=52729) -  [msbuild] Xamarin.Mac and Xamarin.iOS load mismatched assemblies in one build process


## January 10, 2018 - Xamarin.iOS 11.8.0.1

> This version is included in the Visual Studio 2017 version 15.6 Preview 2 release.

### Issues Fixed

* [32022](https://bugzilla.xamarin.com/show_bug.cgi?id=32022) -  [foundation] Fix `DateTime` from `NSDate` seconds (decimal) precision loss when converting
* [37527](https://bugzilla.xamarin.com/show_bug.cgi?id=37527) -  [generator] Incorrect `BI1029 Internal error` reported (instead of `BI1113`)
* [58227](https://bugzilla.xamarin.com/show_bug.cgi?id=58227) -  [photos] Fix incorrect `SDPHLivePhotoFrameProcessingBlock` signature
* [58544](https://bugzilla.xamarin.com/show_bug.cgi?id=58544) -  [msbuild] Set the target architecture in the Info.plist `UIRequiredDeviceCapabilities`
* [58792](https://bugzilla.xamarin.com/show_bug.cgi?id=58792) -  [generator] Disallow the use of `[Async]` when the signature contains ref/out parameters
* [59196](https://bugzilla.xamarin.com/show_bug.cgi?id=59196) -  [uikit] `UIAccessibility.RequestGuidedAccessSession` completion handler is an ObjC block
* [59379](https://bugzilla.xamarin.com/show_bug.cgi?id=59379) -  [msbuild] Codesign iOS Simulator builds using the '-' key. Fix 'App Groups' support on simulator for iOS11
* [59547](https://bugzilla.xamarin.com/show_bug.cgi?id=59547) -  [metalperformanceshaders] Premature collection possible in some bindings
* [59617](https://bugzilla.xamarin.com/show_bug.cgi?id=59617) -  [registrar] Fix static registrar to detect invalid type usage
* [59697](https://bugzilla.xamarin.com/show_bug.cgi?id=59697) -  [msbuild] Don't run Xamarin.Analysis on library projects
* [59756](https://bugzilla.xamarin.com/show_bug.cgi?id=59756) -  [msbuild] Force-Init AppleSdkSettings in `DetectSdkLocationsTaskBase`
* [59798](https://bugzilla.xamarin.com/show_bug.cgi?id=59798) -  [mtouch] Show `MT0123` if the executable assembly does not reference the product assembly
* [59848](https://bugzilla.xamarin.com/show_bug.cgi?id=59848) -  [msbuild] Fixed ObjC binding targets to delete target zip files before re-zipping
* [59911](https://bugzilla.xamarin.com/show_bug.cgi?id=59911) -  [audiotoolbox] Free the right `GCHandle` when failing to create an `InputAudioQueue`
* [59928](https://bugzilla.xamarin.com/show_bug.cgi?id=59928) -  [storekit] Fix `SKCloudServiceSetupOptions` strong dictionary's `Action`
* [59947](https://bugzilla.xamarin.com/show_bug.cgi?id=59947) -  [llvm][bitcode] Attempting to JIT compile method 'ExceptionTests:test_1_basic_filter_catch ()' while running in aot-only mode.
* [59994](https://bugzilla.xamarin.com/show_bug.cgi?id=59994) -  [runtime] Don't hold the framework lock when running managed code
* [60176](https://bugzilla.xamarin.com/show_bug.cgi?id=60176) -  [linker] Handle `ParameterInfo` preserved from XML definitions
* [60303](https://bugzilla.xamarin.com/show_bug.cgi?id=60303) -  [homekit] Expose weakly-typed API since the constants are extensible
* [60377](https://bugzilla.xamarin.com/show_bug.cgi?id=60377) -  [msbuild] Fix possible confusion by similar provisioning profiles
* [60423](https://bugzilla.xamarin.com/show_bug.cgi?id=60423) -  [security] Add `RequestSharedWebCredential` overload fixing `[__NSCFDictionary UTF8String]: unrecognized selector sent to instance`
* [60536](https://bugzilla.xamarin.com/show_bug.cgi?id=60536) -  [msbuild] Catch json parser exceptions to provide better error reporting
* [60545](https://bugzilla.xamarin.com/show_bug.cgi?id=60545) -  [mono] Multiple argument generic with contravariant interface as an argument causes MissingMethodException
* [60771](https://bugzilla.xamarin.com/show_bug.cgi?id=60771) -  [aot] Attempting to JIT compile method 'System.Runtime.CompilerServices.Unsafe:Add (byte&,int)' while running in aot-only mode
* [61039](https://bugzilla.xamarin.com/show_bug.cgi?id=61039) -  [mtouch] Fix `Xamarin.Sdk.framework` not to link with private frameworks when trying to support older OS where they were not yet available
* [61056](https://bugzilla.xamarin.com/show_bug.cgi?id=61056) -  [arkit] Fix `Vertices`, 'TextureCoordinates' and 'TriangleIndices' types in `ARFaceGeometry`
* [3089](https://github.com/xamarin/xamarin-macios/issues/3089) -  [coreanimation] Ensure that we increase the handle reference count in MakeMutable

### Breaking Changes

* [59572](https://bugzilla.xamarin.com/show_bug.cgi?id=59572) -  [msbuild] Emit a build error when `CFBundleIdentifier` is null or empty

### Enhancements

* [52570](https://bugzilla.xamarin.com/show_bug.cgi?id=52570) -  [generator] warn when `[Static]` is used in a `[Category]`
* [53076](https://bugzilla.xamarin.com/show_bug.cgi?id=53076) -  [generator] Lack of error when [`Async]` is used inside a type decorated with `[Protocol]`
* [57094](https://bugzilla.xamarin.com/show_bug.cgi?id=57094) -  [generator] Improve `BI1014` to include the name of unsupported field and valid types
* [57795](https://bugzilla.xamarin.com/show_bug.cgi?id=57795) -  [generator] Allow `[BindAs]` attribute for smart enum used in multidimensional arrays
* [57797](https://bugzilla.xamarin.com/show_bug.cgi?id=57797) -  [generator] Support `[BindAs]` attribute for smart enums of an array of nullable types
* [57804](https://bugzilla.xamarin.com/show_bug.cgi?id=57804) -  [generator] Slightly incorrect error message when trying to use ref/out parameters with `[BindAs]` attributes
* [58251](https://bugzilla.xamarin.com/show_bug.cgi?id=58251) -  [msbuild] Add support for optionally explaining why inapplicable certificates are not applicable
* [59278](https://bugzilla.xamarin.com/show_bug.cgi?id=59278) -  [security] Add missing item in `SecStatusCode` enum
* [59296](https://bugzilla.xamarin.com/show_bug.cgi?id=59296) -  [coreimage] Some `kCI*`keys are missing
* [59537](https://bugzilla.xamarin.com/show_bug.cgi?id=59537) -  [coreanimation] `CATextLayer.Alignment*` strings should be `CATextLayerAlignment` enum
* [60280](https://bugzilla.xamarin.com/show_bug.cgi?id=60280) -  [mtouch][mmp] Allow the use of major-only version numbers in arguments
* [60537](https://bugzilla.xamarin.com/show_bug.cgi?id=60537) -  [localauthentication] `LABiometryType.TypeFaceId` enum name is not consistent
* [60541](https://bugzilla.xamarin.com/show_bug.cgi?id=60541) -  [foundation] Expose `initWithDictionary:copyItems:` in `NS[Mutable]Array`

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 5.11](https://github.com/mono/mono/commits/2017-10) ([hash](https://github.com/mono/mono/commit/hash)).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.11/).


## What's New in this Release

This release is built upon our [open sourced SDK](#open-source) and offers the following new features:

* [Support for wireless deployment and debugging]()
* [Base Class Libraries (BCL) Debugging]()
* [mtouch support for response file]()
* [Xamarin.Analysis HttpClient handler rule]()

### Support for wireless deployment and debugging

The new Apple TV 4K (5th generation) does not have an USB (C) connector, which is the usual way for developers to install and debug applications on devices.

Xamarin.iOS now has the capability to detect devices connected via network (Wi-Fi or Ethernet) and in combination with our latest Visual Studio for Mac release (Version 7.4 Preview 2) debugging over network is also possible.

Please take a look at the Visual Studio for Mac [release notes](https://www.visualstudio.com/en-us/news/releasenotes/vs2017-mac-preview-relnotes#release-date-january-10-2018---visual-studio-2017-version-74-preview-2-740839) for more details.

### Base Class Libraries (BCL) Debugging

Developers can now step into the Base Class Libraries code as well as the Xamarin SDK source code while debugging their application. In order to be able to step into the BCL and Xamarin SDK in a project the following has to be configured:

Visual Studio for Mac

* Un-check the "Debug code project only; do not step into framework code" option via the Preferences > Debugger menu. 

Visual Studio

* Un-check the "Enable Just My Code" option via the Tools > Options > Debugging menu.
  
For iOS Simulator builds, the above steps are all that is required. To debug BCL or Xamarin SDK source on a device, add the `--debug:all` flag as an extra mtouch argument. Open the Project > Properties ("Options" in Visual Studio for Mac) menu. New flags can be added to mtouch in the "iOS Build" panel via the textbox labeled "Additional mtouch arguments:". This flag should only be set when debugging is required and should be removed for production applications since it will greatly increase the size of the application. 

### mtouch support for response file

The `mtouch` tool has a new option that accept arguments inside a response file.

* [56501](https://bugzilla.xamarin.com/show_bug.cgi?id=56501) -  MSB6002 command-line for MTouch task is too long, > 32000 characters / [mtouch/mmp/bgen] Add support for response files. (#2808)

The mentioned limit is for Windows and the default one for macOS is quite larger.


### Xamarin.Analysis HttpClient handler rule

We added a new rule to our project analysis tool which recommends using a native `HttpClientHandler` instead of the managed one for better performance, smaller executable size, and to easily support the newer standards.

As a reminder to run the rules, in Visual Studio for Mac's menu, select **Project > Run Code Analysis**.

*Note: all existing rules are documented [here](https://developer.xamarin.com/guides/ios/troubleshooting/xamarin-ios-analysis).*

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might requires workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.6 stable release:

* [iOS](/releases/ios/api_changes/ios_11.6.1_to_11.8.0);
* [tvOS](/releases/ios/api_changes/tvos_11.6.1_to_11.8.0);
* [watchOS](/releases/ios/api_changes/watchos_11.6.1_to_11.8.0)

## Open Source

Xamarin.iOS is based on the following open-source repositories:
* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-6`
* [mono](https://github.com/mono/mono/tree/2017-10) branch `2017-10`
