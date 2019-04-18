---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 9.9"
---

version:9.9.0
releasedate:2016-06-08

<div class="note">
	<b>Classic Profile Deprecation:</b>
	As new platforms are added in Xamarin.iOS we are starting to gradually deprecate features from the classic profile (monotouch.dll).
	In this release the Boehm garbage collector has been removed (it was never an option available to unified applications).
	The complete removal of classic support is scheduled for next fall with the release of Xamarin.iOS 10.0.
</div>

Requirements
============

- The latest features and API requires Xcode 7.3 and the bundled iOS 9.3 SDK;
- Apple Xcode 7.3 requires a Mac running OSX 10.11 (El Capitan)

What's New
==========

**watchOS 2.x:** This build includes a **preview** of watchOS 2.x support for both
simulators and, for the first time, devices. Please report any issues on 
[bugzilla](https://bugzilla.xamarin.com/).

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
made available at [Evolve 2016](https://evolve.xamarin.com), and include some additional
IDE integration tools.

This release is based on Mono 4.5 which continues to adopt more code from 
Microsoft's open sourced .NET code (reference source) to improve the conformance,
speed and memory usage of our base class libraries (BCL).


### watchOS 2.x known issues

* **Issue:** watchOS 2.x does not offer direct access to sockets. Most of our managed network stack won't work without them.
	* **Workaround** Use native API for networking usage

* **Issue:** The debugger does not connect to watch devices
	* **Workaround** Debug using the simulator. Details in [41554](https://bugzilla.xamarin.com/show_bug.cgi?id=41554)


### API diff

The following document contains a complete list of the
[API changes from 9.8.0 to 9.9.0](/releases/ios/api_changes/from_9.8.0_to_9.9.0).


Bug Fixes
=========

* upcoming
