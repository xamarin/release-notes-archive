---
id: BF9EDE0A-6EFC-4A23-8C34-6600241B0F44
title: "Xamarin.Mac 3.8"
---

version:3.8.0
releasedate:2017-07-27

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled macOS SDK;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-4` branch and is based on Mono 5.2 (2017-04).

This is mostly a bug fix releases. Xcode 9 APIs will be released in the next major release `d15-5`.


### Bug Fixes

* [56452](https://bugzilla.xamarin.com/show_bug.cgi?id=56452) - [jit] Optimize ldloc+ldfld operations for valuetypes, so they don't require making a copy of the valuetype
* [57919](https://bugzilla.xamarin.com/show_bug.cgi?id=57919) -  dynamic object is not supported
* [58367](https://bugzilla.xamarin.com/show_bug.cgi?id=58367) -  Xamarin.Mac crash when returning to native code of a binding library
* [58479](https://bugzilla.xamarin.com/show_bug.cgi?id=58479) -  Xamarin.Mac Extenions result in compile error: The OutputPath property is not set for project
* [58653](https://bugzilla.xamarin.com/show_bug.cgi?id=58653) -  NSApplication.SharedApplication.Terminate(null) throws exception
* [58415](https://bugzilla.xamarin.com/show_bug.cgi?id=58415) -  [mmp] Track all sub-frameworks of ApplicationServices and CoreServices. Fixes #58415 (#2381) (#2384)
* [57718](https://bugzilla.xamarin.com/show_bug.cgi?id=57718) -  Fix 5 methods on NSApplication which were added to the wrong type (#2470) (#2474)
* [58703](https://bugzilla.xamarin.com/show_bug.cgi?id=58703) -  XM System Mono profile not resolving assemblies correctly for Unsupported Framework
* [58504](https://bugzilla.xamarin.com/show_bug.cgi?id=58504) -  Unable to build mac / iOS project that references a NET Standard 2.0 library
* [58758](https://bugzilla.xamarin.com/show_bug.cgi?id=58758) -  WKUIDelegate is missing method runOpenPanelWith
* [58834](https://bugzilla.xamarin.com/show_bug.cgi?id=58834) -  "Error processing the method 'System.Void ...' Value cannot be null." due to ArgumentNullException for `instruction` parameter in Mono.Linker's `MarkException()` method when a referenced assembly has problematic debug symbols, for example "Couchbase.Lite"
* [57645](https://bugzilla.xamarin.com/show_bug.cgi?id=57645) -  "The "LinkAssemblies" task failed unexpectedly" due to a NullReferenceException in Mono.Linker's `ProcessLibrary()` method when project references certain assemblies, for example "Mono.Data.Sqlite.Portable" NuGet package
* [58411](https://bugzilla.xamarin.com/show_bug.cgi?id=58411) - System.Security.Cryptography.CryptographicException: Store root doesn't exist


### API diff

The following documents contains a complete list of the API changes since our previous stable release:

* [macOS](/releases/mac/api_changes/mac_3.4_to_3.8);

