---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.21"
---

This is the 14th preview release of the Xamarin Profiler. Changes since last release include:

Please note that the Mac app bundle has been renamed (from XamarinProfiler.Mac.app to "Xamarin Profiler.app"), so the old version needs to be removed before installing this new update, so that Xamarin Studio prompts the user for the new location.

Common:

* Performance improvements
* Use a better description for the data being drawn in Allocations chart
* New play/stop icons
* Support MLPD v11

Windows:

* Change snapshot icon back to camera one
* Display correctly inverted call tree
* Automatically scroll chart as it grows
* Prevent call tree options to fire event if already selected

Mac:

* Automatically scroll chart as it grows

Bugs fixed:

* [27551](https://bugzilla.xamarin.com/show_bug.cgi?id=27551) - [Profiler - Mac] Tooltips for toolbar buttons hides immediately after it displayed when profiler is in running state
* [33197](https://bugzilla.xamarin.com/show_bug.cgi?id=33197) - [Profiler - Windows] On clicking radio button 'Invert Call Tree' multiple times, call tree data is getting reloaded in detail pan
* [33356](https://bugzilla.xamarin.com/show_bug.cgi?id=33356) - [Profiler - Windows] Sorting doesn't work on column 'Caller' in view "Allocations List"
* [33365](https://bugzilla.xamarin.com/show_bug.cgi?id=33365) - [Profiler - Windows] Sorting arrow doesn't show for all the columns in view 'Summary' and 'Allocation List'
* [33187](https://bugzilla.xamarin.com/show_bug.cgi?id=33187) - [Profiler - Mac] "+" icon should disable when all instruments are already selected
* [31098](https://bugzilla.xamarin.com/show_bug.cgi?id=31098) - Taking snapshot takes too long
* [33188](https://bugzilla.xamarin.com/show_bug.cgi?id=33188) - [Profiler - Mac] "+" icon should disable when profiling process is in-progress
* [33358](https://bugzilla.xamarin.com/show_bug.cgi?id=33358) - [Profiler - Mac] Profiler is getting crashed when user click on column 'Caller' in view "Allocations List"
* [28935](https://bugzilla.xamarin.com/show_bug.cgi?id=28935) - [Profiler - Mac] Profiler is getting stop for iOS app
* [33364](https://bugzilla.xamarin.com/show_bug.cgi?id=33364) - [Profiler - Mac] 'Stack Trace' is not displaying for Snapshots view
* [31709](https://bugzilla.xamarin.com/show_bug.cgi?id=31709) - [Profiler] Text for Persistent Objects checkbox should same in both Windows and Mac profiler
* [31924](https://bugzilla.xamarin.com/show_bug.cgi?id=31924) - Profiler launches app in the wrong simulator OR times out and doesn't launch at all

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

