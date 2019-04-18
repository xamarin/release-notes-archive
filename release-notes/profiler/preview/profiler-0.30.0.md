---
id: 6742C8EB-BA20-4AC2-B89E-D42980D08982
title: "Profiler Preview 0.30.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* ‘Show in call tree’ popup menu for all detail views
* Fix timing display for samples
* Reduce data being displayed in Stack Trace inspector views
* More performance improvements
* Add progress reporting
* Keep selection when drilling down/up on call tree view
* Disable instruments based on platform availability

Windows:

* Add button to expand/collapse inspectors area
* Improve Console tab’s look & feel
* Fix sorting in Allocations Summary and Call Tree views
* Fix ‘Show in call tree’ feature to work like in Mac
* Better looking scrollbars
* Support remote iOS profiling via new Xamarin Mac Agent

Mac:

* Huge improvements on chart drawing/zooming performance
* Fix crash when getting huge code sizes when profiling Xam.Mac apps
* Fix weird color changing in NSTableView rows while changing selection
* Fix resizing of stats labels
* Fix remembering runs between sessions

Bugs fixed:

* [33768](https://bugzilla.xamarin.com/show_bug.cgi?id=33768) - Crash when inverting call tree
* [34911](https://bugzilla.xamarin.com/show_bug.cgi?id=34911) - Put ‘symbol’ column in call tree back to where it was
* [35544](https://bugzilla.xamarin.com/show_bug.cgi?id=35544) - Fix wrong version of NewtonSoft.dll
* [35987](https://bugzilla.xamarin.com/show_bug.cgi?id=35987) - Crash when stopping remote iOS run
* [35993](https://bugzilla.xamarin.com/show_bug.cgi?id=35993) - Remote profiling on iOS devices not working
* [36210](https://bugzilla.xamarin.com/show_bug.cgi?id=36210) - Fix profiling .exe's
* [35926](https://bugzilla.xamarin.com/show_bug.cgi?id=35926) - Fix double registration of services
* [36429](https://bugzilla.xamarin.com/show_bug.cgi?id=36429) - Stats labels are trimmed
* [36607](https://bugzilla.xamarin.com/show_bug.cgi?id=36607) - Can’t profile tvOS template app
* [36408](https://bugzilla.xamarin.com/show_bug.cgi?id=36408) - Can’t run a 2nd instance

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for Android and tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

