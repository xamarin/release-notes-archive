---
id: BDDB6E02-49EA-42B5-BAD2-941222457056
title: "Xamarin.iOS 9.6"
---

version:9.6.1
releasedate:2016-03-31

Requirements
============

- Most new features and API require Xcode 7.3 and the bundled iOS 9.3 SDK;
- Apple Xcode 7.3 requires a Mac running OSX 10.11 (El Capitan)

What's New
==========

This release is an update to our latest Xamarin.iOS 9.4 stable release. 
It adds support for Xcode 7.3 and the new API introduced in the iOS 9.3 SDK.

### iOS 9.3

The 9.6 release is an update to our latest Xamarin.iOS 9.4 stable release. 
It adds support for Xcode 7.3 and the new API introduced in the iOS 9.3 SDK.

### Xamarin.iOS 9.6.2

This service release (the 4th for C6) includes some fixes from mono.

Bug Fixes
=========

* [36080](https://bugzilla.xamarin.com/show_bug.cgi?id=36080) - [system.servicemodel] SIGSEGV within VideoToolbox **[9.6.2+]**
* [37273](https://bugzilla.xamarin.com/show_bug.cgi?id=37273) - [llvm] Disable support for nested clauses **[9.6.2+]**
* [37846](https://bugzilla.xamarin.com/show_bug.cgi?id=37846) - [jit] Fix the reference type detection for Volatile:Read/Write **[9.6.2+]**
* [-] - [mini] Add missing gsharedvt write barrier **[9.6.2+]**

### Xamarin.iOS 9.6.1

This service release (the 3rd for C6) adds support for **Visual Studio Community Edition**

Also **all** editions may now make use of these features which were previously restricted:

- Command-line builds, including headless builds;
- All types and assemblies may now be used, including `System.Data.SqlClient`;
- P/Invoke; and
- No more application size limits;

Finally it removes the splash screen which was shown at launch for applications built with the **Trial** edition.

### Xamarin.iOS 9.6: iOS 9.3 support

The major new features of iOS 9.3 (e.g. night shift) are not exposed thru API.
Still a some new API were added, including:

- New HealthKitUI.framework with `HKActivityRingView`;
- HealthKit's `HKActivitySummary` and friends;
- CoreImage's `CIMaskedVariableBlur` bringing full filters parity between iOS and OSX;

The following document contains a complete list of the
[API changes from 9.4.2 to 9.6.0](/releases/ios/api_changes/from_9.4.2_to_9.6.0).

Breaking Changes
----------------

The iOS 9.3 SDK contains some **breaking changes** from Apple. A few API were
removed or modified without being marked deprecated or obsoleted in the header
files.

- `CKOperation.ActivityStart` was removed (native) and the managed API now returnd `0` [24720736]

The corresponding managed API are still present (to avoid breaking any binary
assembly or component) but if you used those functionalities then you might 
need to adapt your code.

Some `CMSensorRecorder` API originally added in iOS 9 will only works in iOS 9.3+
[24231250]. The affected API are:

- `CMSensorRecorder.IsAccelerometerRecordingAvailable`
- `CMSensorRecorder.GetAccelerometerData`
- `CMSensorRecorder.RecordAccelerometer`

The API `CMSensorRecorder.GetAccelerometerDataSince` is obsoleted as it does
not exists anymore in iOS.

Bug Fixes
=========

* [39338](https://bugzilla.xamarin.com/show_bug.cgi?id=39338) - [videotoolbox] SIGSEGV within VideoToolbox **[9.6.1+]**

