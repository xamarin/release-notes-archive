---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.19"
---

This is the 12th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Improve chart recorder performance
* Fix call tree timing display
* Remove special colouring of *Exception classes, more confusing than helpful
* Speed up loading of static MLPDs by reducing UI refreshes

Bugs fixed:

* [31297](https://bugzilla.xamarin.com/show_bug.cgi?id=31297) - [Profiler - Windows] Profiler is getting crashed when we select mlpd-v10 file in profiler windows via 'File > Open...'
* [31624](https://bugzilla.xamarin.com/show_bug.cgi?id=31634) - [Profiler - Mac] Profiler is getting crashed when user try to restart profiling
* [32233](https://bugzilla.xamarin.com/show_bug.cgi?id=32233) - [Profiler - Windows] Display tab is not getting disabled when user drill-down Call Tree data

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

