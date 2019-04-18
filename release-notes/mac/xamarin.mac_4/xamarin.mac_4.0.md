---
id: 7D673027-48FF-4C06-80FD-7716C4E185DE
title: "Xamarin.Mac 4.0"
---

version:4.0.0
releasedate:2018-1-23

Requirements
============

- The latest features and API requires Xcode 9.1 and the bundled macOS SDK;
- Apple Xcode 9.1 requires a Mac running OSX 10.12 (Sierra) or newer;

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `d15-5` branch and is based on Mono 5.4 (2017-06).

This release introduces macOS APIs added in Xcode9 and Xcode 9.1.

### Miscellaneous Enhancements

**Generator**

* [57535](https://bugzilla.xamarin.com/show_bug.cgi?id=57535) -  [generator] Add enum support for `[FieldAttribute]`
* [57537](https://bugzilla.xamarin.com/show_bug.cgi?id=57537) -  [generator] `[BindAs]` support on Fields

### Bug Fixes

* [58411](https://bugzilla.xamarin.com/show_bug.cgi?id=58411) -  [bcl] TrustFailure (CertificateUnknown) when using user-installed root certificates
* [58720](https://bugzilla.xamarin.com/show_bug.cgi?id=58720) -  [security] `SecKeychain.QueryAsData` returns invalid data type
* [59247](https://bugzilla.xamarin.com/show_bug.cgi?id=59247) -  [webkit] `WKNSURLAuthenticationChallenge` could not be registered
* [59617](https://bugzilla.xamarin.com/show_bug.cgi?id=59617) -  [registrar] Fix static registrar to detect invalid type usage
* [44027](https://bugzilla.xamarin.com/show_bug.cgi?id=44027) -  [bcl] Chunked HTTP PUT times out
* [58826](https://bugzilla.xamarin.com/show_bug.cgi?id=58826) -  MMP does not handle platform assembly swapping when a dependency using XM comes first in 32-bit
* [58849](https://bugzilla.xamarin.com/show_bug.cgi?id=58849) -  [mmp][mtouch] Print verbosity using an invariant culture
* [58861](https://bugzilla.xamarin.com/show_bug.cgi?id=58861) -  dynamic-symbol-mode does not work with 32-bit mac libraries
* [59364](https://bugzilla.xamarin.com/show_bug.cgi?id=59364) -  [runtime] Assertion at dynamic-image.c:209, condition `prev == MONO_HANDLE_RAW (obj)` not met
* [60317](https://bugzilla.xamarin.com/show_bug.cgi?id=60317) -  [bcl] `WebRequest` hangs on TLS/SSL usage (**4.0.0.214+**)
* [60625](https://bugzilla.xamarin.com/show_bug.cgi?id=60625) -  [runtime] Assertion at local-propagation.c:562, condition `ins->opcode > MONO_CEE_LAST` not met (**4.0.0.215+**)
* [61002](https://bugzilla.xamarin.com/show_bug.cgi?id=61002) -  [bcl] Runtime exception: Cannot access a disposed object. Object name: 'MobileAuthenticatedStream' (**4.0.0.216+**)

### API diff

The following documents contains a complete list of the API changes since our previous stable release:

* [macOS](/releases/mac/api_changes/mac_3.8_to_4.0);

