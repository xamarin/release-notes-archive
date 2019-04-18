---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.15"
---

This is the 8th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Always display drilled down objects, even when filtering
* Fix lookup of Google Android emulators
* Fix crash when trying to stop already stopped iOS application on device
* Add pause/resume functionality

Windows:

* Show correctly caller column in Allocations Summary (drill down mode) and List views
* Fix crash when loading only the time instrument
* Disable snapshot button when no instruments support displaying snapshots
* Draw snapshot markers in all instruments, even if they have no data

Mac:

* Prevent user from quickly clicking Run button several times
* Change expand/collapse icon as right-side panel is expanded/collapsed
* Improve Xamarin.Mac app profiling
* Improve look&feel of the charts

Bugs fixed:

* [27238](https://bugzilla.xamarin.com/show_bug.cgi?id=27238) - Starting to profile Xamarin Studio and nothing happens
* [27718](https://bugzilla.xamarin.com/show_bug.cgi?id=27718) - Clean up markers for Generics
* [26431](https://bugzilla.xamarin.com/show_bug.cgi?id=26431) - Xamarin Profiler hangs on OSX 10.10.1 for Xamarin.Mac applciation
* [29468](https://bugzilla.xamarin.com/show_bug.cgi?id=29468) - User is not able to copy console tab data in windows profiler
* [29655](https://bugzilla.xamarin.com/show_bug.cgi?id=29655) - Display option for 'Call Tree' is not getting reset when we start profiler
* [27547](https://bugzilla.xamarin.com/show_bug.cgi?id=27547) - Profiler becomes unresponsive/hanged for a while when I run the profiler
* [29709](https://bugzilla.xamarin.com/show_bug.cgi?id=29709) - Profiler getting crashed
* [29384](https://bugzilla.xamarin.com/show_bug.cgi?id=29384) - Selected row info is lost for Call Tree view in extended detail pan
* [29623](https://bugzilla.xamarin.com/show_bug.cgi?id=29623) - Profiler window does not displaying correct application name
* [27674](https://bugzilla.xamarin.com/show_bug.cgi?id=27674) - Profiler does not generate chart and data for instrument 'Time Profiler' for iOS app with iOS device
* [29743](https://bugzilla.xamarin.com/show_bug.cgi?id=29743) - Instrument selection dialog is not getting closed

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

