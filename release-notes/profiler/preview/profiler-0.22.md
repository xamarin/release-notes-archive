---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.22"
---

This is the 15th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Fix crash on startup when setting up a run
* Add preview warning to main window(s)
* Show memory stats for allocations summary/list
* Show JIT stats for call tree
* Fix duplicated allocations when filtering allocations lists
* Fix snapshots’ deltas retrieval
* Fix UI thread locks when filtering services’ data

Windows:

* Cleanup markers when processing consecutive runs
* Register MLPD extension in installer
* Check Mono.Posix is installed in installer
* Make right-side panel behave like on Mac (no auto hiding/showing)
* Fix class names in inverse references view

Mac:

* Only use icons in inspector area tabs
* iOS9 support

Bugs fixed:

* [31915](https://bugzilla.xamarin.com/show_bug.cgi?id=31915) - [Profiler - Windows] Profiler is getting crashed when user is trying to navigate on next/previous snapshot/exception
* [32659](https://bugzilla.xamarin.com/show_bug.cgi?id=32659) - The Camera Icon in the menu for taking snapshots is always disabled
* [31320](https://bugzilla.xamarin.com/show_bug.cgi?id=31320) - [Profiler - Mac & Windows] A large portion of chart for allocations on Android looks flat
* [33766](https://bugzilla.xamarin.com/show_bug.cgi?id=33766) - [Profiler - Windows] Profiler is getting crashed when user select radio button 'Invert call tree'
* [33523](https://bugzilla.xamarin.com/show_bug.cgi?id=33532) - [Profiler - Windows] All objects are displaying as live in 'Allocations List' view without taking any snapshot
* [33778](https://bugzilla.xamarin.com/show_bug.cgi?id=33778) - [Profiler - Mac] Right-side panel tabs are not displaying properly
* [31707](https://bugzilla.xamarin.com/show_bug.cgi?id=31707) - [Profiler] Persistent Objects checkbox does not work properly

## Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

