---
id: 7D673027-48FF-4C06-80FD-7716C4E185DE
title: "Xamarin.Mac 3.0"
---

version:3.0.0
releasedate:2016-09-21

<div class="note">
	<b>Mono TLS Deprecation:</b>
	This version of Xamarin.Mac (C9) is the last one to ship with the optional Mono (managed) SSL/TLS provider.
	This old provider only supports the SSLv3 and TLSv1 standards, which several servers don't support anymore.
	Support for the newer TLSv1.1 and 1.2 is only available using the newer AppleTLS provider. 
	This new provider is already used, by default, when building applications (since C7).
</div>

Requirements
============

- The latest features and API requires Xcode 8.1 and the bundled macosx10.12 SDK;
- Apple Xcode 8.0 requires a Mac running macOS 10.11 (El Capitan) or 10.12 (Sierra).

What's New
==========

The Xamarin.Mac 3.0 release includes the new APIs that Apple added in the latest SDK (macosx10.12) shipped with Xcode 8.

Please note that the new MediaPlayer framework was changed to 64-bit only.

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `cycle9` branch, and based on Mono 4.8.0.

### New NSUrlSessionHandler implementation

A new implementation of `NSUrlSessionHandler` was [contributed](https://github.com/xamarin/xamarin-macios/pull/31) by Nick Berardi. The new version offers the same features as the previous one but requires less memory and, by reusing it, less time spent in the garbage collector;

### Other Enhancements

* String optimizations inside the binding generator, i.e. `bmac`, makes it 10% faster than previous releases;
* Additional caching in the registrar makes it about 4% faster than previous releases;
* Several fixes to allow the use of `msbuild` over `xbuild` in many cases. Applications using the Xamarin.Mac 4.5 Target framework can not use xbuild yet due to [this bug](https://bugzilla.xamarin.com/show_bug.cgi?id=52050).

### Releases

- 3.0.0.398

Cycle 9 service release 0.

* Fixed multiple issues preventing use of nugets that depend upon netstandard13 facades. For now this will require modifying the TargetFrameworkVersion in your csproj to 4.6 with a text editor.
* [52437](https://bugzilla.xamarin.com/show_bug.cgi?id=52437) - Random NullReferenceExceptions in StringBuilder.ThreadSafeCopy
* [46929](https://bugzilla.xamarin.com/show_bug.cgi?id=46929) - Datetime error on Mono.data.Sqlite


- 3.0.0.393

Cycle 9 initial release.

- 3.0.0.391

* [51148](https://bugzilla.xamarin.com/show_bug.cgi?id=51148) - [msbuild] .mdb files not copied for F# projects **(10.4.0.121+)**

- 3.0.0.384

* Fixed NSSliderTouchBarItem.ValueAccesoryWidth to be nfloat, not double

- 3.0.0.367

* [51530](https://bugzilla.xamarin.com/show_bug.cgi?id=51530) - [debugger] Ensure that we use the correct paths in the mono mdb files **(10.4.0.97+)**

- 3.0.0.343

Release canidate of Cycle 9.

Adds TouchBar API support. See https://github.com/xamarin/mac-samples/tree/master/TouchBarExample for a sample.

- 3.0.0.337

Alpha refresh of Cycle 9,  our next major feature release.

Improves Xcode 8.2 support, in particular when the static registrar is used (--registrar=static or macOS extensions).

- 3.0.0.274 - 3.0.0.311

Alpha release of Cycle 9, our next major feature release.

- 3.0.0.12

macOS 10.12 "preview" release. This release is based off of the same stack as C8 Xamarin.iOS.

A full stable release of Xamarin.Mac 3.0 will occur in the C9 timeframe.

### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 2.10 (C8)

* [macOS](/releases/mac/api_changes/mac_2.10_to_3.0);

