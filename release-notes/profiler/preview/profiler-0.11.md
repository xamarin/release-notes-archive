---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.11"
---

This is the 4th preview release of the Xamarin Profiler. Changes since last release include:

Common:

* Improve data refresh speed
* Check MLPD format version

Windows frontend:

* Get rid of single instance restriction
* Display allocations data, not timing data, in Allocations’ Call Tree

Mac frontend:

* Fix PathSelectorView’s popup menu
* Check .app bundles are OS X apps before profiling

Bugs fixed:

* [25269](https://bugzilla.xamarin.com/show_bug.cgi?id=25269) - Double clicking on the row (detail pan data) backtrace data does not show for windows profiler.
* [25279](https://bugzilla.xamarin.com/show_bug.cgi?id=25279) - Profiler does not start profiling an app, if profiler window is already opened
* [25271](https://bugzilla.xamarin.com/show_bug.cgi?id=25271) - Vertical scroll bar is displaying in 'Sample List' detail pan for Time Profiler
* [25941](https://bugzilla.xamarin.com/show_bug.cgi?id=25941) - Flags and snapshots markers are misaligned
* [26142](https://bugzilla.xamarin.com/show_bug.cgi?id=26142) - Data is inconsistent when sorting
* [25777](https://bugzilla.xamarin.com/show_bug.cgi?id=25777) - Profiler is getting hanged/unresponsive sometimes when user double click on rows
* [25834](https://bugzilla.xamarin.com/show_bug.cgi?id=25834) - Flags are not getting added when we click on button 'Take Snapshot'
* [25318](https://bugzilla.xamarin.com/show_bug.cgi?id=25318) - 'Take snapshot' button is not working properly for iOS app with simulator
* [26623](https://bugzilla.xamarin.com/show_bug.cgi?id=26623) - Crashes when opening an apk
* [26646](https://bugzilla.xamarin.com/show_bug.cgi?id=26646) - When user takes snapshot then Allocations List view is not displaying objects (alive, dead, disposed) under column 'Live'

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

