---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.16"
---

This is the 9th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Display exceptions in charts
* Display popovers for snapshots in charts
* Better identify negative numbers in Snapshots view
* Display hottest stack trace for allocations summary/samples views

Windows:

* Fix several issues with the New Session dialog
* Fix crash when recent list is empty
* Cleanup stack trace view for allocations summary
* Use current scale when adding new instruments
* Use same default sorting than on Mac
* Fix UI lockups

Mac:

* Detect application not being launched on locked iOS device
* Toolbar improvements
* Improve installer
* Switch to 64bit build

Bugs fixed:

* [30053](https://bugzilla.xamarin.com/show_bug.cgi?id=30053) - Profiler doesn't work at all
* [30184](https://bugzilla.xamarin.com/show_bug.cgi?id=30184) - On selecting any item in detail pan, its title displays twice in breadcrumbs
* [30220](https://bugzilla.xamarin.com/show_bug.cgi?id=30220) - Functionality of button Pause/Resume is not working properly
* [27182](https://bugzilla.xamarin.com/show_bug.cgi?id=27182) - Profiler is getting hanged when we click on Stop button for an iOS app with iOS device
* [30014](https://bugzilla.xamarin.com/show_bug.cgi?id=30014) - Time Profiler Crashes
* [30578](https://bugzilla.xamarin.com/show_bug.cgi?id=30578) - 'Take Snapshots' button is disabled in windows profiler
* [30628](https://bugzilla.xamarin.com/show_bug.cgi?id=30628) - Profiler is not generating correct data in details pan and extended details pan
* [30219](https://bugzilla.xamarin.com/show_bug.cgi?id=30219) - Search string is getting removed from textbox
* [30283](https://bugzilla.xamarin.com/show_bug.cgi?id=30283) - Taking a snapshot causes the profiler to crash with an out of memory exception
* [30903](https://bugzilla.xamarin.com/show_bug.cgi?id=30903) - Triangles are not displaying in 'Call Tree' tab for Allocations

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

