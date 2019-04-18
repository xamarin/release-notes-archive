---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.20"
---

This is the 13th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Windows:

* Fix WPF bindings warnings

Bugs fixed:

* [32459](https://bugzilla.xamarin.com/show_bug.cgi?id=32459) - Profiler 0.18 always launches app in iPhone 4s simulator
* [32915](https://bugzilla.xamarin.com/show_bug.cgi?id=32915) - [Profiler - Windows] Call Tree data is not sorted by Running Time desc for instrument Time Profiler
* [32916](https://bugzilla.xamarin.com/show_bug.cgi?id=32916) - [Profiler - Windows] Extended Detail pan is not working properly for Windows profiler
* [31477](https://bugzilla.xamarin.com/show_bug.cgi?id=31477) - [Profiler - Windows] Profiler is getting crashed when user try to sort Snapshot data by Name after expending snapshot nodes

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

