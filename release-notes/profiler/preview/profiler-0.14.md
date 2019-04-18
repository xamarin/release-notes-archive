---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.14"
---

This is the 7th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Avoid circular references for inverse references tree
* Trim search string
* Detect death of the correct Android activity
* Highlight class names correctly in methods for generic types
* Clear Android log when starting new application
* Better error catching/reporting for Android profiling

Windows:

* More memory usage reduction

Mac:

* Center snapshot icon over snapshot markers
* Cleanup markers for generics in drill down area
* Display all drill down levels in drill down area view
* Add percentage boxes to size and time columns
* Hide useless segmented control in toolbar
* Fix broken scrolling in Allocations List
* Only enable Snapshot button when there is an instrument that supports snapshots
* Fix UI lockup on heavy console output
* Add time range to selection box in charts

Bugs fixed:

* [29058](https://bugzilla.xamarin.com/show_bug.cgi?id=29058) - Profiler is getting crashed when user is trying to drill down in 'Call Tree'
* [29119](https://bugzilla.xamarin.com/show_bug.cgi?id=29119) - 'Call Tree' row is getting selected when we click several times on Call Tree header to sort the data
* [29117](https://bugzilla.xamarin.com/show_bug.cgi?id=29117) - References is not displaying for snapshots view in right side panel
* [27182](https://bugzilla.xamarin.com/show_bug.cgi?id=27182) - Profiler is getting hanged when we click on Stop button for an iOS app with iOS device
* [29259](https://bugzilla.xamarin.com/show_bug.cgi?id=29259) - Hard to reconcile numbers in Call Tree view
* [27871](https://bugzilla.xamarin.com/show_bug.cgi?id=27871) - Profiler does not reset Snapshots values on second profiler run
* [28414](https://bugzilla.xamarin.com/show_bug.cgi?id=28414) - Profiler does not generate data and graph for an android app
* [28675](https://bugzilla.xamarin.com/show_bug.cgi?id=28675) - When user open already saved .mlpd file in profiler window then profiler does not display chart and data every time
* [29118](https://bugzilla.xamarin.com/show_bug.cgi?id=29118) - Text is not updating according to the tab selected in extended detail pan
* [27967](https://bugzilla.xamarin.com/show_bug.cgi?id=27967) - Profiler writes some exception in log file
* [29260](https://bugzilla.xamarin.com/show_bug.cgi?id=29260) - Sorting Allocations View columns very slow
* [29387](https://bugzilla.xamarin.com/show_bug.cgi?id=29387) - Triangles are not displaying in right column for instrument Time Profiler in Call Tree view
* [28405](https://bugzilla.xamarin.com/show_bug.cgi?id=28405) - Profiler crash on startup

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

