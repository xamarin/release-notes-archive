---
id: 11B48FB4-51C0-4776-809A-77B1DDF79EA5
title: "Xamarin.iOS 10.11"
---

version:10.11.0
releasedate:2017-05-11

<div class="note">
	This is a preview version of Xamarin.iOS, it will eventually become version 10.12.
</div>

Requirements
============

- The latest features and API requires Xcode 8.3 and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.3 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `master` branch, and is based on Mono 5.0.

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

### Bug Fixes

* [54658](https://bugzilla.xamarin.com/show_bug.cgi?id=54658) - [aot] Fix `"condition `!async' not met" and "condition `unwind_options == MONO_UNWIND_NONE' not met" asserts
* [54976](https://bugzilla.xamarin.com/show_bug.cgi?id=54976) - [aot] Fix "mini-arm-gsharedvt.c:220, condition `src_slot < 16' not met"" assert
* [55553](https://bugzilla.xamarin.com/show_bug.cgi?id=55553) - [llvm] LLVM causes Assertion failed: ((instructionAddress & 0x3) == 0), function makeLDR_literal

### API diff

The following documents contains a complete list of the API changes since our previous stable 10.10 release:

* [iOS](/releases/ios/api_changes/ios_10.10.0_to_10.11.0);
* [tvOS](/releases/ios/api_changes/tvos_10.10.0_to_10.11.0);
* [watchOS](/releases/ios/api_changes/watchos_10.10.0_to_10.11.0)

