---
id: 11B48FB4-51C0-4776-809A-77B1DDF79EA5
title: "Xamarin.iOS 10.14"
---

version:10.14.0
releasedate:2017-08-24

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-4` branch and is based on Mono 5.2 (2017-04).

This is mostly a bug fix releases as most engineering efforts are to support Xcode 9 this fall.

### Miscellaneous Enhancements

**Tools**

* [msbuild] Strip frameworks better. This can save a significant amount of space when using code-sharing: the PIX app saved ~11mb in release mode (when stripping)
	
### Bug Fixes

* [56345](https://bugzilla.xamarin.com/show_bug.cgi?id=56345) - [msbuild] Properly generate dSYMs for WatchKit2 appex's
* [56452](https://bugzilla.xamarin.com/show_bug.cgi?id=56452) - [jit] Optimize ldloc+ldfld operations for valuetypes, so they don't require making a copy of the valuetype
* [57266](https://bugzilla.xamarin.com/show_bug.cgi?id=57266) - [mtouch] Normalize strings that refer to assemblies and their paths before comparing them
* [57764](https://bugzilla.xamarin.com/show_bug.cgi?id=57764) - [msbuild] Don't define __IOS__ for tvOS binding projects
* [57826](https://bugzilla.xamarin.com/show_bug.cgi?id=57826) - [mtouch] Fix same symbol used in assemblies with/without dlsym
* [57833](https://bugzilla.xamarin.com/show_bug.cgi?id=57833) - [mtouch] Check for __Internal p/invokes after processing for exception marshaling
* [57919](https://bugzilla.xamarin.com/show_bug.cgi?id=57919) - [bcl] Dynamic object is not supported
* [58114](https://bugzilla.xamarin.com/show_bug.cgi?id=58114) - [llvm] csc (Rolsyn) produce fault clauses that the llvm backend does not support

* [57919](https://bugzilla.xamarin.com/show_bug.cgi?id=57919) - [bcl] IsComObject() throws PlatformNotSupportedException and breaks uses of dynamic / SLE **[10.14.0.24+]**
* [58063](https://bugzilla.xamarin.com/show_bug.cgi?id=58063) - [linker] Fix reading assemblies with incorrect forwarders **[10.14.0.24+]**
* [58264](https://bugzilla.xamarin.com/show_bug.cgi?id=58264) - [llvm] Assertion: should not be reached at mono/mono/mini/unwind.c:623 **[10.14.0.24+]**
* [58446](https://bugzilla.xamarin.com/show_bug.cgi?id=58446) - [llvm] Fix the calling of fault clauses in llvm compiled code **[10.14.0.24+]**
* [58834](https://bugzilla.xamarin.com/show_bug.cgi?id=58834) - [cecil] Fix MT2102 due to incorrect cecil throws ANE for some debugging symbols **[10.14.0.24+]**
* [58367](https://bugzilla.xamarin.com/show_bug.cgi?id=58367) - [runtime] Parameters passed on the stack use at least 8 bytes on x86-64 **[10.14.0.24+]**
* [58778](https://bugzilla.xamarin.com/show_bug.cgi?id=58778) - [mtouch] Put 'mono_profiler_startup_log' in the symbol list (so it is not stripped) **[10.14.0.24+]**   

### API diff

The following documents contains a complete list of the API changes since our stable 10.12 (SR2) release:

* [iOS](/releases/ios/api_changes/ios_10.12.0_to_10.14.0);
* [tvOS](/releases/ios/api_changes/tvos_10.12.0_to_10.14.0);
* [watchOS](/releases/ios/api_changes/watchos_10.12.0_to_10.14.0)

