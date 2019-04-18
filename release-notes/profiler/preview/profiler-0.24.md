---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.24"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* ‘Show in call tree’ popup menu in Allocations list

Windows:

* Correctly place marker popups below marker
* Display correct device name in UI when available
* Fix keyboard expanding/collapsing of rows in call tree
* Close marker popups when mouse clicking outside them

Mac:

* Fix crash on Mavericks when changing NSTableView column titles

Bugs fixed:

* [34605](https://bugzilla.xamarin.com/show_bug.cgi?id=34605) / [34692](https://bugzilla.xamarin.com/show_bug.cgi?id=34692) - Crash on startup
* [34160](https://bugzilla.xamarin.com/show_bug.cgi?id=34160) - Live objects count not updated
* [34624](https://bugzilla.xamarin.com/show_bug.cgi?id=34624) - Missing ‘Stack trace’ tab in allocations summary
* [34623](https://bugzilla.xamarin.com/show_bug.cgi?id=34623) - Crash when selecting rows in allocations list
* [32693](https://bugzilla.xamarin.com/show_bug.cgi?id=32693) - Missing horizontal scrolling in Call Tree view
* [34627](https://bugzilla.xamarin.com/show_bug.cgi?id=34627) - UI confusion when filtering on persistent objects when no snapshots have been taken
* [34860](https://bugzilla.xamarin.com/show_bug.cgi?id=34860) - Fix sorting on Mac Time profiler’s call tree

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

