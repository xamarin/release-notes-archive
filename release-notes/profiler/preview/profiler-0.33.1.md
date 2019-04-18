---
id: 742710EA-2370-4369-B446-4F66285FB777
title: "Profiler Preview 0.33.1"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* More performance improvements

Windows:

Mac:

Bugs fixed:

* [39556](https://bugzilla.xamarin.com/show_bug.cgi?id=39556) - Placeholder text misbehaves when zooming
* [40713](https://bugzilla.xamarin.com/show_bug.cgi?id=40713) - Old Xamarin.Mac used for building the package
* [40715](https://bugzilla.xamarin.com/show_bug.cgi?id=40715) - Old Xamarin.Mac used for building the package

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some
* Installation on Windows with previous versions (>= 0.24) fails, so old versions need to be uninstalled first

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

