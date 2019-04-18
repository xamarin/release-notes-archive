---
id: A402345C-FDF4-485C-BBD7-562579BCC3A2
title: "Profiler Preview 0.36.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:


Common:

* Per-thread charts for allocations and samples
* Allocations summary pie chart

Windows:

* Unify behavior in DrillDown area for different views

Bugs fixed:

* [42256](https://bugzilla.xamarin.com/show_bug.cgi?id=42256) - Weird double clicking behavior
* [42913](https://bugzilla.xamarin.com/show_bug.cgi?id=42913) - Missing autocompletion in Mac search boxes
* [43458](https://bugzilla.xamarin.com/show_bug.cgi?id=43458) - Out of place focus ring in search field
* [43605](https://bugzilla.xamarin.com/show_bug.cgi?id=43605) - Misnamed columns in allocations list
* [43971](https://bugzilla.xamarin.com/show_bug.cgi?id=43971) - Window mis-sized on low resolutions
* [44243](https://bugzilla.xamarin.com/show_bug.cgi?id=44243) - Missing scrollbar in charts section
* [44244](https://bugzilla.xamarin.com/show_bug.cgi?id=44244) - Missing information in chart tooltip

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

