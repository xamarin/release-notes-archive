---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.10"
---

This is the 3rd preview release of the Xamarin Profiler. Changes since last release include:

Common:

* Fix sorting/filtering bugs
* Live/Dead object status when using snapshots
* Time range selection in instrument charts
* Support automatic snapshots
* Display memory snapshots' deltas rather than totals
* Full search/sorting in tree views (Call tree, snapshots)
* Huge performance improvements
* Preferences dialog
* Recording settings are now remembered between sessions
* Support for user-specified folder for profiler output files
* (Signed) Installer for both Mac and Windows

Windows frontend:

* Drill down feature for Call Tree and Allocations Summary
* Memory snapshots support
* Timeline in charts header
* .mlpd files associated with the profiler by the installer
* Improve Call Tree data performance
* New toolbar icons
* Jumps list support
* Drag&Drop of .mlpd files

Mac frontend:

* Initial support for profiling Xamarin.Mac apps
* Full support for iOS devices via USB or WiFi
* Use correct image representations on retina/non-retina switching
* Yosemite-style toolbar
* Improve UI responsiveness when profiling
* Use correct text color on method names when row is selected
* Remove redundant instrument selector in instrument detail area

Bugs fixed:

* [22878](https://bugzilla.xamarin.com/show_bug.cgi?id=22878) - Timing is not displaying for profiler run in LCD view
* [24530](https://bugzilla.xamarin.com/show_bug.cgi?id=24530) - Time profiler call tree running time column sorting not working
* [25266](https://bugzilla.xamarin.com/show_bug.cgi?id=25266) - Not able to take snapshot with Windows profiler

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Sorting snapshots is slow
* Call tree not supported for iOS devices
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

