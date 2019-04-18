---
id: 11B48FB4-51C0-4776-809A-77B1DDF79EA5
title: "Xamarin.iOS 10.12"
---

version:10.12.0
releasedate:2017-08-21

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-3` branch, and is based on Mono 5.0.

### Mono Embeddinator-4000 support

Our tooling has been updated to allow the creation of standalone frameworks when used in conjunction with the new [Embeddinator-4000](https://mono.github.io/Embeddinator-4000/) tool. This means you can now use Xamarin.iOS to create native frameworks reusable from Objective-C applications, even your managed subclasses of `NSObject` will be available.

### Xamarin Analysis

We added a new rule to our project analysis tool which recommends the use of the float 32 option on device. Not using it leads to hefty performance cost, specially on mobile, where double precision math is measurably slower.  
_Note that .NET uses double precision internally, even for float, so enabling this option affects precision and, possibly, compatibility._

*As a reminder you can run the Xamarin Analysis rules from Xamarin Studio's menu bar by selecting Project > Run Code Analysis.*

### Miscellaneous Enhancements

**Tools**

* [51753](https://bugzilla.xamarin.com/show_bug.cgi?id=51753) - [msbuild] Add support for passing extra args to btouch
* [55256](https://bugzilla.xamarin.com/show_bug.cgi?id=55256) - [mtouch] Add support for stripping bitcode from frameworks when not needed. This dramatically decreases the size of watchOS apps built for debug when using frameworks, because it ends up removing all the bitcode from `Mono.framework`.
* [55712](https://bugzilla.xamarin.com/show_bug.cgi?id=55712) - [mtouch] Disable incremental builds for the simulator (not helpful for the JIT)
* [43780](https://bugzilla.xamarin.com/show_bug.cgi?id=43780) - Implement support for removing IsInformal from a protocol in a specific SDK version
* [pr2139](https://github.com/xamarin/xamarin-macios/pull/2139) - [mtouch/mmp] Print assembly references in verbose mode
* [52664](https://bugzilla.xamarin.com/show_bug.cgi?id=52664) -  [generator] Deriving from certain protocol interfaces causes the generator to throw a BI0000: NullReferenceException
* [56513](https://bugzilla.xamarin.com/show_bug.cgi?id=56513) - Code sharing: allow identical assemblies from different paths
* [52665](https://bugzilla.xamarin.com/show_bug.cgi?id=52665) - [generator] Deriving from certain protocol interfaces generates uncompilable code
* [51776](https://bugzilla.xamarin.com/show_bug.cgi?id=51776) - Show a nice error (MT4168) if the user registers a managed class with an Objective-C keyword
* [55568](https://bugzilla.xamarin.com/show_bug.cgi?id=55568) - [registrar] Detect more invalid characters in selectors so that we can report better errors
* [57070](https://bugzilla.xamarin.com/show_bug.cgi?id=57070) - [generator] Improve error reporting for api definition that uses the deprecated availability attributes

**API**

* [pr1946](https://github.com/xamarin/xamarin-macios/pull/2232) - NSActivityOptions.IdleDisplaySleepDisabled had wrong value

### Bug Fixes

* [4037359](https://support.microsoft.com/en-ca/help/4037359/title)[CVE-2017-8665](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-8665) - **[vulnerability]** Elevation Of Privilege in apple-doc-wizard script **[10.12.0.18+]**
* [57780](https://bugzilla.xamarin.com/show_bug.cgi?id=57780) - [aot] Could not inflate generic type **[10.12.0.15+]**
* [56808](https://bugzilla.xamarin.com/show_bug.cgi?id=56808) - Cannot debug referenced iOS Class library in Visual Studio 2015/2017
* [54658](https://bugzilla.xamarin.com/show_bug.cgi?id=54658) - [aot] Fix `"condition `!async' not met"` and `"condition `unwind_options == MONO_UNWIND_NONE' not met"` asserts
* [54976](https://bugzilla.xamarin.com/show_bug.cgi?id=54976) - [aot] Fix `"mini-arm-gsharedvt.c:220, condition src_slot < 16' not met""` assert
* [55870](https://bugzilla.xamarin.com/show_bug.cgi?id=55870) - Partial static registrar can't be used with custom managed exception marshaling
* [55553](https://bugzilla.xamarin.com/show_bug.cgi?id=55553) - [llvm] LLVM causes Assertion failed: ((instructionAddress & 0x3) == 0), function makeLDR_literal
* [56862](https://bugzilla.xamarin.com/show_bug.cgi?id=56862) - [Apple Watch][release mode] Unable to play audio file using AVFoundation in apple watch
* [56876](https://bugzilla.xamarin.com/show_bug.cgi?id=56876) - [mtouch] Handle non-ascii characters when converting assembly to bitcode assembly 
* [54973](https://bugzilla.xamarin.com/show_bug.cgi?id=54973) - [iOS] Bcl/Non Bcl tests fail to run on 64 bit devices with condition 
* [54417](https://bugzilla.xamarin.com/show_bug.cgi?id=54417) - Native linker fails when linking framework with large number of exported functions (Also [51710](https://bugzilla.xamarin.com/show_bug.cgi?id=51710)) 
* [57119](https://bugzilla.xamarin.com/show_bug.cgi?id=57119) - Code signing no longer expands wildcards * in distribution provisioning profiles
* [56679](https://bugzilla.xamarin.com/show_bug.cgi?id=56679) - Fix condition to detect a mix of dylibs and frameworks for the same library
* [56317](https://bugzilla.xamarin.com/show_bug.cgi?id=56317) - BTOUCH : error CS1704: An assembly with the same name has already been imported
* [54919](https://bugzilla.xamarin.com/show_bug.cgi?id=54919) - NSFormatter subclass sample does not work in static registrar
* [56635](https://bugzilla.xamarin.com/show_bug.cgi?id=56635) - [mtouch] Fix linking with the same third-party framework from both extension and container app
* [57063](https://bugzilla.xamarin.com/show_bug.cgi?id=57063) - Can't strip debug builds


### Xamarin.iOS 10.12.0.20

Additional fixes were released in Xamarin.iOS 10.12.0.20, including:

* [57919](https://bugzilla.xamarin.com/show_bug.cgi?id=57919) - [bcl] `IsComObject()` throws `PlatformNotSupportedException` and breaks uses of dynamic / SLE **[10.12.0.20+]**
* [58789](https://bugzilla.xamarin.com/show_bug.cgi?id=58789) - [mtouch] NRE in error message causing general MT0000 instead of MT2102 **[10.12.0.20+]**
* [58834](https://bugzilla.xamarin.com/show_bug.cgi?id=58834) - [cecil] Fix MT2102 due to incorrect cecil throws ANE for some debugging symbols **[10.12.0.20+]**


### Xamarin.iOS 10.12.3.3

Additional fixes were released in Xamarin.iOS 10.12.3.3, including:

* [44027](https://bugzilla.xamarin.com/show_bug.cgi?id=44027) - [System.Net.Http] Chunked HTTP PUT times out. **[10.12.3.3+]**
* [58778](https://bugzilla.xamarin.com/show_bug.cgi?id=58778) - [mtouch] Profiling is unsuccessful when **Strip native debugging symbols** is enabled. **[10.12.3.3+]**
* [58829](https://bugzilla.xamarin.com/show_bug.cgi?id=58829) - [runtime] Many "[Mono] worker parking, [Mono] worker unparking" messages appearing in application output. **[10.12.3.3+]**


### API diff

The following documents contains a complete list of the API changes since our previous stable 10.10 release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.12.0);
* [tvOS](/releases/ios/api_changes/tvos_10.10.0_to_10.12.0);
* [watchOS](/releases/ios/api_changes/watchos_10.10.0_to_10.12.0)

