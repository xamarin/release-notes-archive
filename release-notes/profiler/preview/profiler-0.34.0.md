---
id: 03E8B901-68A8-4CC7-89EB-94195132F7DA
title: "Profiler Preview 0.34.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* New icons
* Merge allocations summary and list views
* Improve snapshots view

Windows:

* New About dialog

Mac:

* New About dialog

Bugs fixed:

* [42056](https://bugzilla.xamarin.com/show_bug.cgi?id=42056) - NRE when stopping .exe profiling
* [42140](https://bugzilla.xamarin.com/show_bug.cgi?id=42140) - Don’t override user’s snapshots settings
* [42143](https://bugzilla.xamarin.com/show_bug.cgi?id=42143) - Search doesn’t work in snapshots view
* [42142](https://bugzilla.xamarin.com/show_bug.cgi?id=42142) - Search spinner never goes away
* [42204](https://bugzilla.xamarin.com/show_bug.cgi?id=42204) - Crash when sorting
* [38280](https://bugzilla.xamarin.com/show_bug.cgi?id=38280) - Not disabling Time instrument for tvOS profiling
* [42316](https://bugzilla.xamarin.com/show_bug.cgi?id=42316) - Can’t select all instruments for iOS profiling
* [40990](https://bugzilla.xamarin.com/show_bug.cgi?id=40990) - Snapshot button always disabled
* [39298](https://bugzilla.xamarin.com/show_bug.cgi?id=39298) - Inconsistent column heights
* [42467](https://bugzilla.xamarin.com/show_bug.cgi?id=42467) - Crash when restarting MLPD
* [42250](https://bugzilla.xamarin.com/show_bug.cgi?id=42250) - Can’t select instruments
* [42147](https://bugzilla.xamarin.com/show_bug.cgi?id=42147) - Search box missing in snapshots view
* [40668](https://bugzilla.xamarin.com/show_bug.cgi?id=40668) - Weird selection changes when resizing window
* [42462](https://bugzilla.xamarin.com/show_bug.cgi?id=42462) - Crash when restarting runs
* [40601](https://bugzilla.xamarin.com/show_bug.cgi?id=40601) - Console does not scroll down
* [42463](https://bugzilla.xamarin.com/show_bug.cgi?id=42463) -  ProfilerAgent crash
* [42734](https://bugzilla.xamarin.com/show_bug.cgi?id=42734) - Crash when zooming chart
* [42731](https://bugzilla.xamarin.com/show_bug.cgi?id=42731) - Selection in chart going wild
* [40567](https://bugzilla.xamarin.com/show_bug.cgi?id=40567) - Can't profile on iOS device
* [41187](https://bugzilla.xamarin.com/show_bug.cgi?id=41187) - Windows installer can't upgrade minor updates
* [42460](https://bugzilla.xamarin.com/show_bug.cgi?id=42460) - Missing tooltips
* [40999](https://bugzilla.xamarin.com/show_bug.cgi?id=40999) - iOS profiling on Windows works only every second time


This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Installation on Windows with previous versions (>= 0.24) fails, so old versions need to be uninstalled first

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

