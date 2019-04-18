---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 11.2"
---

version:11.2
releasedate:2017-09-25

Requirements
============

- Xcode 9.0 and the bundled iOS, tvOS and watchOS SDKs, Using an older Xcode version is possible but some features are not available, in particular:
	- The static registrar requires Xcode 9 headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors;
	- Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless Xcode9 toolchain is used;

- Apple Xcode 9.0 requires a Mac running macOS 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-4`-xi branch and is based on Mono 5.2 (2017-04).

This is the Xcode9 enabled version of the previous [XI 10.14](/release/ios/xamarin.ios_10/xamarin.ios_10.14) beta releases.


### Xamarin.iOS 11.2.1

This version was shipped along the service release 2 (SR2) of Visual Studio 2017 (15.4.2) but, beside a new version number, is identical to the previous version.


### Xamarin.iOS 11.2.0

#### Miscellaneous Enhancements

**Tools**

* [msbuild] Strip frameworks better. This can save a significant amount of space when using code-sharing: the PIX app saved ~11mb in release mode (when stripping)
	
#### Bug Fixes

* [58411](https://bugzilla.xamarin.com/show_bug.cgi?id=58411) - [bcl] TrustFailure (CertificateUnknown) when using user-installed root certificates
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


#### API diff

The following documents contains a complete list of the API changes since the 11.0 release:

* [iOS](/releases/ios/api_changes/ios_11.0.0_to_11.2.0);
* [tvOS](/releases/ios/api_changes/tvos_11.0.0_to_11.2.0);
* [watchOS](/releases/ios/api_changes/watchos_11.0.0_to_11.2.0)

