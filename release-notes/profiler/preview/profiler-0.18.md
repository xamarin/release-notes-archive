---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.18"
---

This is the 11th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Group allocations summary items by stack trace
* Reduce memory usage
* Allow filtering allocations by persistent state
* Allow searching allocations by address
* Make filter/time range not be mutually exclusive in searches

Windows:

* Improve tabs look
* Improve look of snapshots/exceptions popups
* Use icons for allocations summary groups
* Format numbers correctly in Summary and Snapshots views’ columns

Mac:

* Set a correct minimum size for timestamp column in AllocationsListView

Bugs fixed:

* [31297](https://bugzilla.xamarin.com/show_bug.cgi?id=31297) - Profiler is getting crashed when we select mlpd-v10 file in profiler windows via 'File > Open...'
* [31317](https://bugzilla.xamarin.com/show_bug.cgi?id=31317) - 'Take Snapshot' button is not disable when click on 'Pause' button
* [31101](https://bugzilla.xamarin.com/show_bug.cgi?id=31101) - Profiler is getting crashed when user is trying to navigate on next/previous snapshot/exception
* [31195](https://bugzilla.xamarin.com/show_bug.cgi?id=31195) - In drill down mode 'Allocations Summary' data is order be size but first row is not selected by default
* [30053](https://bugzilla.xamarin.com/show_bug.cgi?id=30053) - Profiler doesn't work at all

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

