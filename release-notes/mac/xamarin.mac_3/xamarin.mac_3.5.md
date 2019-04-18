---
id: BF9EDE0A-6EFC-4A23-8C34-6600241B0F44
title: "Xamarin.Mac 3.5"
---

version:3.5.0
releasedate:2017-05-09

<div class="note">
	<b>Xamarin.Mac Extensions Regression</b>
	The initial preview of 3.5 contains a regression breaking extensions from launching when built. This will be fixed in a future release.
	</div>


Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled macOS SDK;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `master` branch, and include some additional IDE integration tools.

### Target Framework Renaming

Since Xamarin.Mac 2.0 multiple target frameworks have been offered, optimized for different use cases. 

While technically accurate at the time, their naming left much to be desired, however.

In Xamarin.Mac 3.5 they are being renamed to:

- Modern (Optimized profile also powering Xamarin.iOS) replace Mobile.
- Full (Extended desktop API compatibility) replaces XM 4.5.

The Modern and Full target frameworks behave exactly the same as before, and existing projects will require zero changes.

### Framework linkage improvements

Previous versions of Xamarin.Mac did not correctly pass -framework and -weak_framework arguments to clang based upon bindings.

This prevented some APIs, such as LocalAuthentication from working correctly without work around.

While this change should be transparent to a majority of users, due to the possibility of breakage cause it is being documented here.

Please report any issues via [bugzilla](https://bugzilla.xamarin.com/).

### Miscellaneous Enhancements

**API**

* [pr1946](https://github.com/xamarin/xamarin-macios/pull/1946) - Add NSFileManager.UnmountVolume
* [pr1672](https://github.com/xamarin/xamarin-macios/pull/1672) - [Mac] Update numerous availability tags from 10.12.1 to 10.12.2
* [pr2042](https://github.com/xamarin/xamarin-macios/pull/2042) - Fix casting in NSApplication.NextEvent on 64-bit systems
* [pr2050](https://github.com/xamarin/xamarin-macios/pull/2050) - Decorate NSWindow and NSSegmentedControl methods with NullAllowed attribute.

### Bug Fixes

* [pr1977](https://github.com/xamarin/xamarin-macios/pull/1977) -  [msbuild] Fix running bgen for Xamarin.Mac. (#1977)
* [53927](https://bugzilla.xamarin.com/show_bug.cgi?id=53927) - MMP should ship debugging symbols just like mtouch
* [54914](https://bugzilla.xamarin.com/show_bug.cgi?id=54914) - Error executing task IBTool: An item with the same key has already been added
* [36258](https://bugzilla.xamarin.com/show_bug.cgi?id=36258) - There is no __MAC__ pre-processor directive
* [51753](https://bugzilla.xamarin.com/show_bug.cgi?id=51753) - [msbuild] Add support for passing extra args to btouch


### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 3.4 (15.2)

* [macOS](/releases/mac/api_changes/mac_3.4_to_3.5);

