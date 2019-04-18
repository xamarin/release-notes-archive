---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.17"
---

This is the 10th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Fix call tree generation
* Fix metadata retrieval when paused
* Fix flat chart for Android profiling
* Support MLPD v10 format
* Display relative percentages in call tree views

Windows:

* Use radio buttons for call tree display settings
* Fix enabling of console view for live runs
* Fix resizing of right-side panel view

Mac:

* Prettify NSAlert-based dialogs
* Fix problems with spaces for MLPD directory setting
* Use radio buttons for snapshots preferences and call tree display settings
* Improve toolbar on Yosemite
* Improve tabs look
* Reflect correct default sorting on default views
* Display percentages graphically for samples list view

Bugs fixed:

* [30948](https://bugzilla.xamarin.com/show_bug.cgi?id=30948) - Profiler is getting crashed when user is trying to start profiler
* [30036](https://bugzilla.xamarin.com/show_bug.cgi?id=30036) - Xam.Mac app is not getting closed when user click on Stop button in profiler window
* [30225](https://bugzilla.xamarin.com/show_bug.cgi?id=30225) - Console output is not displaying for Xam.Mac app
* [30683](https://bugzilla.xamarin.com/show_bug.cgi?id=30683) - Snapshot data is not getting reset
* [31096](https://bugzilla.xamarin.com/show_bug.cgi?id=31096) - Memory profiler tracks total allocations
* [28846](https://bugzilla.xamarin.com/show_bug.cgi?id=28846) - Profiler does not generate data and chart for the android app and after sometime it throws error
* [27479](https://bugzilla.xamarin.com/show_bug.cgi?id=27479) - Profiler shows "Unknown" nodes in call tree
* [27944](https://bugzilla.xamarin.com/show_bug.cgi?id=27944) - Profiler does not generate and display data properly for instruments Allocations and Time Profiler in details pan
* [29743](https://bugzilla.xamarin.com/show_bug.cgi?id=29743) - Instrument selection dialog is not getting closed
* [30283](https://bugzilla.xamarin.com/show_bug.cgi?id=30283) - Taking a snapshot causes the profiler to crash with an out of memory exception
* [29386](https://bugzilla.xamarin.com/show_bug.cgi?id=29386) - Functionality of Right panel is not working properly
* [28411](https://bugzilla.xamarin.com/show_bug.cgi?id=28411) - On selecting any instrument, focus should move on that instrument along with its graph/chart
* [30585](https://bugzilla.xamarin.com/show_bug.cgi?id=30585) - Expand/collapse icon is not working properly for right-side panel
* [31125](https://bugzilla.xamarin.com/show_bug.cgi?id=31125) - Allocation List and Snapshot view default sorting is not by Time
* [30671](https://bugzilla.xamarin.com/show_bug.cgi?id=30671) - User is not able to save profiler session

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

