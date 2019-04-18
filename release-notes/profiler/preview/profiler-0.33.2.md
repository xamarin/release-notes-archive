---
id: C231E51E-4179-4929-9487-B8D3E63D3E9A
title: "Profiler Preview 0.33.2"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Windows:

* Support profiling on iOS Windows simulator

Bugs fixed:

* [39763](https://bugzilla.xamarin.com/show_bug.cgi?id=39763) - Old Xamarin.Mac used for building the package
* [40944](https://bugzilla.xamarin.com/show_bug.cgi?id=40944) - Crash when selecting time range with no instruments
* [40451](https://bugzilla.xamarin.com/show_bug.cgi?id=40451) - Remove dependency on XS
* [40345](https://bugzilla.xamarin.com/show_bug.cgi?id=40345) - Time range selection enabled when just clicking on the chart
* [41248](https://bugzilla.xamarin.com/show_bug.cgi?id=41248) - Wrong caption when drilling down allocations summary
* [41284](https://bugzilla.xamarin.com/show_bug.cgi?id=41284) - Exception when stopping Android run
* [41293](https://bugzilla.xamarin.com/show_bug.cgi?id=41293) - Call tree nodes getting collapsed
* [41210](https://bugzilla.xamarin.com/show_bug.cgi?id=41210) - Call tree options don’t work when time range selected
* [40595](https://bugzilla.xamarin.com/show_bug.cgi?id=40595) - Missing loading spinner
* [41427](https://bugzilla.xamarin.com/show_bug.cgi?id=41427) - Unhandled exception
* [41137](https://bugzilla.xamarin.com/show_bug.cgi?id=41137) - Can’t profile on iOS devices

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Installation on Windows with previous versions (>= 0.24) fails, so old versions need to be uninstalled first

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

