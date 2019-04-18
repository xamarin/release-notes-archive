---
id: BD7C1B18-6F1D-47F6-9850-729F8E58C4C6
title: "Profiler Preview 0.31.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* Reduce CPU usage
* Add visual cue to Call Tree view
* Unify progress report messages on all platforms
* Only display thrown exceptions

Windows:

* Improve Options dialog look
* Add autocompletion to search boxes
* Add searching to Console tab

Mac:

* Fix typo in full method name in drill down label (missing ‘.’)

Bugs fixed:

* [37146](https://bugzilla.xamarin.com/show_bug.cgi?id=37146) - No console output on iOS runs on Windows
* [37230](https://bugzilla.xamarin.com/show_bug.cgi?id=37230) - Filtering call tree by time doesn’t work as expected
* [36058](https://bugzilla.xamarin.com/show_bug.cgi?id=36058) - Previous run’s snapshots show in detail popup
* [37018](https://bugzilla.xamarin.com/show_bug.cgi?id=37018) - Wrong version in control panel
* [35901](https://bugzilla.xamarin.com/show_bug.cgi?id=35901) - Crash on iOS profiling
* [37128](https://bugzilla.xamarin.com/show_bug.cgi?id=37128) - iOS profiling on Windows not working
* [36210](https://bugzilla.xamarin.com/show_bug.cgi?id=36210) - Can’t open .exe for profiling
* [36429](https://bugzilla.xamarin.com/show_bug.cgi?id=36429) - Stats labels are trimmed weirdly
* [36409](https://bugzilla.xamarin.com/show_bug.cgi?id=36409) - Can’t open .exe via File->Open menu
* [35518](https://bugzilla.xamarin.com/show_bug.cgi?id=35518) - Profiler starts saved session instead of allowing new one
* [28943](https://bugzilla.xamarin.com/show_bug.cgi?id=28943) - Application selected even when pressing Cancel
* [37793](https://bugzilla.xamarin.com/show_bug.cgi?id=37793) - Crash when inverting call tree
* [34154](https://bugzilla.xamarin.com/show_bug.cgi?id=34154) - ‘Only persistent objects’ checkbox affects all views
* [31381](https://bugzilla.xamarin.com/show_bug.cgi?id=31381) - Negative numbers not red coloured
* [37735](https://bugzilla.xamarin.com/show_bug.cgi?id=37735) - Instruments not re-enabled when changing target in New Session dialog
* [37654](https://bugzilla.xamarin.com/show_bug.cgi?id=37654) - Children not sorted in call tree view
* [34627](https://bugzilla.xamarin.com/show_bug.cgi?id=34627) - Stats not being updated
* [37838](https://bugzilla.xamarin.com/show_bug.cgi?id=37838) - Siblings not highlighted in call tree
* [37797](https://bugzilla.xamarin.com/show_bug.cgi?id=37797) - UI freezes

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for Android and tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

