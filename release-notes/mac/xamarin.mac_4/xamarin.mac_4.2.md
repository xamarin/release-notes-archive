---
id: A8296468-C9A7-42F1-A5CE-C6BD1792E2B1
title: "Xamarin.Mac 4.2"
---

# Xamarin.Mac 4.2
Last Update: 3/5/2018 [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)

 [What's New](#Whats_New_in_this_Release)

 [Known Issues](#Known_Issues)

 [Blogs](https://blog.xamarin.com/tag/xamarin-platform/)

 [Open Source](#Open_Source)



### Installing

* Visual Studio 2017 for Mac – Stable updater channel

#### Requirements

* The latest features and API requires Xcode 9.2 and the bundled macOS SDKs;
* Apple Xcode 9.2 requires a Mac running macOS 10.12.6 (Sierra) or newer;

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [GitHub Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

### Release History

This version Xamarin.Mac correspond to our **15.6** (`d15-6`) milestone.

* April 16, 2018 - Xamarin.Mac 4.2.1.29
* March 26, 2018 - Xamarin.Mac 4.2.1.28
* February 23, 2018 - Xamarin.Mac 4.2.0.20
* February 7, 2018 - Xamarin.Mac 4.2.0.19
* January 24, 2018 - Xamarin.Mac 4.2.0.8
* January 10, 2018 - Xamarin.Mac 4.2.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## April 16, 2018 - Xamarin.Mac 4.2.1.29

> This version is included in the Visual Studio 2017 version 15.6 Service Release 6.

### Issue Fixed

* [3674](https://github.com/xamarin/xamarin-macios/issues/3674) -  [msbuild] Correctly determine when a Xamarin.Mac build require a provisioning profile

## March 26, 2018 - Xamarin.Mac 4.2.1.28

> This version is included in the Visual Studio 2017 version 15.6 Service Release 3.

### Issue Fixed

* [7472](https://github.com/mono/mono/issues/7472) - [runtime]  `NullReferenceException` when trying to use an extension method on a `null` object as an assignment value for an `Action` or `Func` variable

## February 23, 2018 - Xamarin.Mac 4.2.0.20

> This version is included in the Visual Studio 2017 version 15.6 RTW release.

### Issue Fixed

* [3241](https://github.com/xamarin/xamarin-macios/issues/3241) -  [llvm] Revert "[mini] Align stack when resuming to catch handler"

## February 7, 2018 - Xamarin.Mac 4.2.0.19

> This version is included in the Visual Studio 2017 version 15.6 Preview 4 release.

### Issues Fixed

* [3089](https://github.com/xamarin/xamarin-macios/issues/3089) -  [coregraphics] Fix `CGPath.MakeMutable` reference count


## January 24, 2018 - Xamarin.Mac 4.2.0.8

> This version is included in the Visual Studio 2017 version 15.6 Preview 3 release.

### Issues Fixed

* [3140](https://github.com/xamarin/xamarin-macios/issues/3140) -  [vision] Removes incorrect `[Abstract]` from `VNDetectBarcodesRequest`
* [3145](https://github.com/xamarin/xamarin-macios/issues/3145) -  [scenekit] Crashes if `SCNAnimation.AnimationEvents` isn't empty
* [3146](https://github.com/xamarin/xamarin-macios/issues/3146) -  [scenekit] `SCNPhysicsWorld.ConvexSweepTest` method doesn't work
* [6428](https://github.com/mono/mono/issues/6428) -  [bcl] `DnsCallback` as async callback causing unhandled exception
* [52729](https://bugzilla.xamarin.com/show_bug.cgi?id=52729) -  [msbuild] Xamarin.Mac and Xamarin.iOS load mismatched assemblies in one build process


## January 10, 2018 - Xamarin.Mac 4.2.0.1

> This version is included in the Visual Studio 2017 version 15.6 Preview 2 release.

### Issues Fixed


* [32022](https://bugzilla.xamarin.com/show_bug.cgi?id=32022) -  [foundation] Fix DateTime from NSDate seconds (decimal) precision loss when converting.
* [51263](https://bugzilla.xamarin.com/show_bug.cgi?id=51263) -  [corefoundation] Fix CFMessagePort crash when returning data from callback
* [51343](https://bugzilla.xamarin.com/show_bug.cgi?id=51343) -  [appkit] validateMenuItem not called for menu items with c# events for the action
* [59537](https://bugzilla.xamarin.com/show_bug.cgi?id=59537) -  [coreanimation] CATextLayer.Alignment\* strings should be CATextLayerAlignment enum / type
* [59635](https://bugzilla.xamarin.com/show_bug.cgi?id=59635) -  [appkit] Window.Toolbar cannot be set to null
* [59647](https://bugzilla.xamarin.com/show_bug.cgi?id=59647) -  [mmp] Release mode AOT should delete dSYM files
* [59911](https://bugzilla.xamarin.com/show_bug.cgi?id=59911) -  [AudioToolbox] Handle is not initialized when trying to create instance of InputAudioQueue
* [59994](https://bugzilla.xamarin.com/show_bug.cgi?id=59994) -  [runtime] Deadlock in the runtime when the GC runs and the XI runtime is releasing managed refs
* [60233](https://bugzilla.xamarin.com/show_bug.cgi?id=60233) -  [runtime] Assertion in dynamic-image.c
* [60277](https://bugzilla.xamarin.com/show_bug.cgi?id=60277) -  [mmp] Fix broken debugging in cases due to stale symbols
* [60294](https://bugzilla.xamarin.com/show_bug.cgi?id=60294) -  [mmp] Add registrar option to help
* [60416](https://bugzilla.xamarin.com/show_bug.cgi?id=60416) -  [appkit] NSCollectionView.ValidateDrop should use 'ref', not 'out'.
* [61101](https://bugzilla.xamarin.com/show_bug.cgi?id=61101) -  NSView.LocationInView does not accept null
* [60935](https://bugzilla.xamarin.com/show_bug.cgi?id=60935) -  NSGestureRecognizer.State binding incorrect causing issues with custom recognizers
* [60821](https://bugzilla.xamarin.com/show_bug.cgi?id=60821) -  ArgumentNullException due to wrong binding in NSWorkspace.SharedWorkspace.OpenFile
* [60377](https://bugzilla.xamarin.com/show_bug.cgi?id=60377) -  MSBuild is getting confused by similar provisioning profiles
* [60545](https://bugzilla.xamarin.com/show_bug.cgi?id=60545) -  Multiple argument generic with contravariant interface as an argument causes MissingMethodException.
* [60771](https://bugzilla.xamarin.com/show_bug.cgi?id=60771) -  Attempting to JIT compile method 'System.Runtime.CompilerServices.Unsafe:Add (byte&,int)' while running in aot-only mode

### Breaking Changes
### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono 5.x](https://github.com/mono/mono/commits/2017-10) ([hash](https://github.com/mono/mono/commit/hash)).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

## What's New in this Release

### Base Class Libraries (BCL) Debugging

Developers can now step into the Base Class Libraries code as well as the Xamarin SDK source code while debugging their application. In order to be able to step into the BCL and Xamarin SDK in a project the following has to be configured:

Visual Studio for Mac
* Un-check the "Debug code project only; do not step into framework code" option via the Preferences > Debugger menu. 

Visual Studio
* Un-check the "Enable Just My Code" option via the Tools > Options > Debugging menu.

### mmp support for response file

The `mmp` tool has a new option that accept arguments inside a response file.

* [56501](https://bugzilla.xamarin.com/show_bug.cgi?id=56501) -  MSB6002 command-line for MTouch task is too long, > 32000 characters / [mtouch/mmp/bgen] Add support for response files. (#2808)

The mentioned limit is for Windows and the default one for macOS is quite larger.

### Enhancements

* [57094](https://bugzilla.xamarin.com/show_bug.cgi?id=57094) -  [generator] Improve BI1014 - include name of unsupported field and valid types
* [58243](https://bugzilla.xamarin.com/show_bug.cgi?id=58243) -  [appkit] Add NSApplicationLaunchUserNotificationKey in more obvious location
* [58251](https://bugzilla.xamarin.com/show_bug.cgi?id=58251) -  [msbuild] When looking for valid signing certificates, print out each invalid certificate and state why it's not valid
* [59186](https://bugzilla.xamarin.com/show_bug.cgi?id=59186) -  [mmp] Improve multiple MM4162 error use case by adding MM0091 error
* [58583](https://bugzilla.xamarin.com/show_bug.cgi?id=58583) -  [mmp] Improve error message when handling mixed-mode assembly references
* [60423](https://bugzilla.xamarin.com/show_bug.cgi?id=60423) -  [security] Add RequestSharedWebCredential overload.
* [60541](https://bugzilla.xamarin.com/show_bug.cgi?id=60541) -  [foundation] Expose initWithDictionary:copyItems: in NS[Mutable]Dictionary
* [57797](https://bugzilla.xamarin.com/show_bug.cgi?id=57797) -  [generator] BindAs support for array of nullable values 
* [58792](https://bugzilla.xamarin.com/show_bug.cgi?id=58792) -  [generator] Disallow the use of [Async] when the signature contains ref/out parameters
* [57804](https://bugzilla.xamarin.com/show_bug.cgi?id=57804) -  [generator] Fix slightly incorrect error message when trying to use ref/out parameters with BindAs attributes.
* [57795](https://bugzilla.xamarin.com/show_bug.cgi?id=57795) -  [generator] BindAs attribute for smart enum to multidimensional array generates code that doesn't compile



## Known Issues

## API Diff

This [document](/releases/mac/api_changes/mac_4.0_to_4.2) contains a complete list of the API changes since the Xamarin.Mac 4.0 stable release.

## Open Source

Xamarin.Mac is based on the following open-source repositories:
* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-6`
* [mono](https://github.com/mono/mono/tree/2017-10) branch `2017-10`
