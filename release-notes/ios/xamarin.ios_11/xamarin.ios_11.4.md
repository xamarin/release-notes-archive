---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 11.4"
---

version:11.4
releasedate:2017-11-14

Requirements
============

- Xcode 9.1 and the bundled iOS, tvOS and watchOS SDKs. Using an older Xcode version is possible, but some features are not available, in particular:
	- The static registrar requires Xcode 9.1 headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors;
	- Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9 toolchain is used;

- Apple Xcode 9.1 requires a Mac running macOS 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-5` branch and is based on Mono 5.4 (2017-06).

### Miscellaneous Enhancements

**Generator**

* [57535](https://bugzilla.xamarin.com/show_bug.cgi?id=57535) -  [generator] Add enum support for `[FieldAttribute]`
* [57537](https://bugzilla.xamarin.com/show_bug.cgi?id=57537) -  [generator] `[BindAs]` support on Fields

### Bug Fixes

* [58720](https://bugzilla.xamarin.com/show_bug.cgi?id=58720) -  [security] `SecKeychain.QueryAsData` returns invalid data type
* [59247](https://bugzilla.xamarin.com/show_bug.cgi?id=59247) -  [webkit] `WKNSURLAuthenticationChallenge` could not be registered
* [59617](https://bugzilla.xamarin.com/show_bug.cgi?id=59617) -  [registrar] Fix static registrar to detect invalid type usage
* [44027](https://bugzilla.xamarin.com/show_bug.cgi?id=44027) -  [bcl] Chunked HTTP PUT times out
* [58849](https://bugzilla.xamarin.com/show_bug.cgi?id=58849) -  [mmp][mtouch] Print verbosity using an invariant culture
* [59364](https://bugzilla.xamarin.com/show_bug.cgi?id=59364) -  [runtime] Assertion at dynamic-image.c:209, condition `prev == MONO_HANDLE_RAW (obj)` not met
* [59956](https://bugzilla.xamarin.com/show_bug.cgi?id=59956) -  [aot] Bitcode failure on watchOS
* [60317](https://bugzilla.xamarin.com/show_bug.cgi?id=60317) -  [bcl] `WebRequest` hangs on TLS/SSL usage (**11.4.0.214+**)

#### API diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.3 stable release:

* [iOS](/releases/ios/api_changes/ios_11.3.0_to_11.4.0);
* [tvOS](/releases/ios/api_changes/tvos_11.3.0_to_11.4.0);
* [watchOS](/releases/ios/api_changes/watchos_11.3.0_to_11.4.0)

