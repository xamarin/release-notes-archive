---
id: 907E6C80-D7D0-4DC9-853F-016A3469E95E
title: "Profiler Preview 0.32.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* Add missing keyboard shortcuts
* Cycle detector instrument
* Show activity spinner for long running operations
* Add ‘Memory’ and ‘Performance’ templates

Windows:

* Fix crash when ‘Separate by thread’ is selected
* Improve look of Stack Trace view(s)

Mac:

* Add searching to Console tab
* Dynamically resize instrument area based on number of instruments

Bugs fixed:

* [38689](https://bugzilla.xamarin.com/show_bug.cgi?id=38689) - Chart area shrinks when instruments are selected
* [38302](https://bugzilla.xamarin.com/show_bug.cgi?id=38302) - Unable to check ‘Only persistent objects’ checkbox
* [37908](https://bugzilla.xamarin.com/show_bug.cgi?id=37908) - Statistics text being trimmed
* [38854](https://bugzilla.xamarin.com/show_bug.cgi?id=38854) - Progress indicator never goes away
* [38549](https://bugzilla.xamarin.com/show_bug.cgi?id=38549) - Stack trace empty on exception markers popup

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for Android and tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some
* Installation on Windows with previous versions (>= 0.24) fails, so old versions need to be uninstalled first.

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

