---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.23"
---

This is the 16th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Allow displaying of all/new objects in snapshots view
* Some more performance improvements
* Refresh allocations summary when snapshots are taken, for stats to display correct numbers
* Fix filtering of persistent objects in allocations summary
* Display more memory stats
* Display GC stats in Snapshots info inspector
* Display CPU load stats in Samples info inspector
* Highlight parent sections in drill down area
* Remove UI locks when retrieving inverse references

Windows:

* New chart control
* Fix sorting by name on Snapshots view

Mac:

* Resize labels to fit correctly in stats area in inspectors
* UI fixes and tweaks for El Capitan

Bugs fixed:

* [33186](https://bugzilla.xamarin.com/show_bug.cgi?id=33186) - [Profiler - Mac] Extended Detail pan is not become gray in drill-down mode for Call-Tree view
* [33974](https://bugzilla.xamarin.com/show_bug.cgi?id=33974) - [Profiler - Mac] On opening saved .mlpd file label 'Working set', 'Max 58.5 MB' (for allocation instrument) and 'Total 00:22.460' (for instrument time profiler) is not displaying
* [32405](https://bugzilla.xamarin.com/show_bug.cgi?id=32405) - [Profiler - Mac] Unknown classes are present in 'Summary' and 'Allocations List' view
* [34390](https://bugzilla.xamarin.com/show_bug.cgi?id=34390) - [Profiler - Windows] User unable to select graph with running profiler

## Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

