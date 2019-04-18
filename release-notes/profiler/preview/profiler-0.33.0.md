---
id: B74C959F-7BE9-46C7-A854-00CA135054DB
title: "Profiler Preview 0.33.0"
---

Another preview release of the Xamarin Profiler is [available](http://xamarin.com/profiler). Changes since last release
include:

Common:

* Display heaviest stack trace in Call Tree’s stack trace view
* Performance and stability improvements
* Re-enable Time instrument for Android profiling

Windows:

* Use icons for right-side tabs
* Change colors to match dark theme
* Display timing information in Time instrument’s Call Tree view, not memory

Mac:

* Improve look of right-side tabs
* Remember window size and position
* Remember inspector area’s divider position

Bugs fixed:

* [39412](https://bugzilla.xamarin.com/show_bug.cgi?id=39412) - Scrolling problems in Call Tree view
* [39810](https://bugzilla.xamarin.com/show_bug.cgi?id=39810) - Scrolling problems in Stack Trace view
* [39656](https://bugzilla.xamarin.com/show_bug.cgi?id=39656) - Unable to start profiling with Trial license
* [38300](https://bugzilla.xamarin.com/show_bug.cgi?id=38300) - Missing keyboard support in template selector dialog
* [40397](https://bugzilla.xamarin.com/show_bug.cgi?id=40397) - Invalid license checks
* [40598](https://bugzilla.xamarin.com/show_bug.cgi?id=40598) - Drill down area not reset when restarting runs
* [40600](https://bugzilla.xamarin.com/show_bug.cgi?id=40600)- Wrong scrolling when ‘Show in call tree'

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Time instrument not available for tvOS profiling
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some
* Installation on Windows with previous versions (>= 0.24) fails, so old versions need to be uninstalled first

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

