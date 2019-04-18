---
id: BF9EDE0A-6EFC-4A23-8C34-6600241B0F44
title: "Xamarin.Mac 3.6"
---

version:3.6.0
releasedate:2017-08-21

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled macOS SDK;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-3` branch, and include some additional IDE integration tools.

### Target Framework Renaming

Since Xamarin.Mac 2.0 multiple target frameworks have been offered, optimized for different use cases. 

While technically accurate at the time, their naming left much to be desired, however.

In Xamarin.Mac 3.6 they are being renamed to:

- Modern (Optimized profile also powering Xamarin.iOS) replace Mobile.
- Full (Extended desktop API compatibility) replaces XM 4.5.

The Modern and Full target frameworks behave exactly the same as before, and existing projects will require zero changes.

### Framework linkage improvements

Previous versions of Xamarin.Mac did not correctly pass -framework and -weak_framework arguments to clang based upon bindings.

This prevented some APIs, such as LocalAuthentication from working correctly without work around.

While this change should be transparent to a majority of users, due to the possibility of breakage cause it is being documented here.

Please report any issues via [bugzilla](https://bugzilla.xamarin.com/).

### Miscellaneous Enhancements

**Tools**

* [pr2096](https://github.com/xamarin/xamarin-macios/pull/2096) - Fix target framework detection issues in mmp
* [43780](https://bugzilla.xamarin.com/show_bug.cgi?id=43780) - Implement support for removing IsInformal from a protocol in a specific SDK version
* [pr2139](https://github.com/xamarin/xamarin-macios/pull/2139) - [mtouch/mmp] Print assembly references in verbose mode
* [52664](https://bugzilla.xamarin.com/show_bug.cgi?id=52664) -  [generator] Deriving from certain protocol interfaces causes the generator to throw a BI0000: NullReferenceException
* [52665](https://bugzilla.xamarin.com/show_bug.cgi?id=52665) - [generator] Deriving from certain protocol interfaces generates uncompilable code

**API**

* [pr1946](https://github.com/xamarin/xamarin-macios/pull/2232) - NSActivityOptions.IdleDisplaySleepDisabled had wrong value
* [pr1946](https://github.com/xamarin/xamarin-macios/pull/1946) - Add NSFileManager.UnmountVolume
* [pr1672](https://github.com/xamarin/xamarin-macios/pull/1672) - [Mac] Update numerous availability tags from 10.12.1 to 10.12.2
* [pr2042](https://github.com/xamarin/xamarin-macios/pull/2042) - Fix casting in NSApplication.NextEvent on 64-bit systems
* [pr2050](https://github.com/xamarin/xamarin-macios/pull/2050) - Decorate NSWindow and NSSegmentedControl methods with NullAllowed attribute.
* [32612](https://bugzilla.xamarin.com/show_bug.cgi?id=32612) - WebView.SetSelectedDomRange

### Bug Fixes

* [57780](https://bugzilla.xamarin.com/show_bug.cgi?id=57780) - [aot] Could not inflate generic type
* [55147](https://bugzilla.xamarin.com/show_bug.cgi?id=55147) - "Content" Build Action does not copy file into .app bundle when project is built with `msbuild` rather than `xbuild`
* [pr1977](https://github.com/xamarin/xamarin-macios/pull/1977) -  [msbuild] Fix running bgen for Xamarin.Mac. (#1977)
* [53927](https://bugzilla.xamarin.com/show_bug.cgi?id=53927) - MMP should ship debugging symbols just like mtouch
* [54914](https://bugzilla.xamarin.com/show_bug.cgi?id=54914) - Error executing task IBTool: An item with the same key has already been added
* [36258](https://bugzilla.xamarin.com/show_bug.cgi?id=36258) - There is no __MAC__ pre-processor directive
* [51753](https://bugzilla.xamarin.com/show_bug.cgi?id=51753) - [msbuild] Add support for passing extra args to btouch
* [53420](https://bugzilla.xamarin.com/show_bug.cgi?id=53420) -  Add unusual checks necessary to process obfuscated code
* [54919](https://bugzilla.xamarin.com/show_bug.cgi?id=54919) - Bug 54919 - NSFormatter subclass sample does not work in static registrar
* [57119](https://bugzilla.xamarin.com/show_bug.cgi?id=57119) - Code signing no longer expands wildcards * in distribution provisioning profiles
* [55857](https://bugzilla.xamarin.com/show_bug.cgi?id=55857) - Code that works in DEBUG; System.NotSupportedException in RELEASE 
* [55870](https://bugzilla.xamarin.com/show_bug.cgi?id=55870) - Partial static registrar can't be used with custom managed exception marshaling


### Xamarin.Mac 3.6.0.19

Additional fixes were released in Xamarin.Mac 3.6.0.19, including:

* [57919](https://bugzilla.xamarin.com/show_bug.cgi?id=57919) - [bcl] `IsComObject()` throws `PlatformNotSupportedException` and breaks uses of dynamic / SLE **[3.6.0.19+]**
* [58834](https://bugzilla.xamarin.com/show_bug.cgi?id=58834) - [cecil] Fix MT2102 due to incorrect cecil throws ANE for some debugging symbols **[3.6.0.19+]**


### Xamarin.Mac 3.6.3.3

Additional fixes were released in Xamarin.Mac 3.6.3.3, including:

* [44027](https://bugzilla.xamarin.com/show_bug.cgi?id=44027) - [System.Net.Http] Chunked HTTP PUT times out. **[3.6.3.3+]**
* [58829](https://bugzilla.xamarin.com/show_bug.cgi?id=58829) - [runtime] Many "[Mono] worker parking, [Mono] worker unparking" messages appearing in application output. **[3.6.3.3+]**


### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 3.4 (15.2)

* [macOS](/releases/mac/api_changes/mac_3.4_to_3.6);

