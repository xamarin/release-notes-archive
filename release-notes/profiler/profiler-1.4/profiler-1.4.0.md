---
id: 8D3F336B-0DB9-42A8-A01E-4246608A6DB0
title: "Profiler 1.4.0"
dateupdated: 2017-03-22
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.4.0-1.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.4.0-1.msi)

# Release notes

## Common:

* Stability improvements for iOS profiling
* Enable keyboard navigation in New Session dialog
* Provide well-known values for sampling cycle frequency instead of having the user guess what the correct value is
* Don't recalculate samples timing, so that they match timing in call tree
* Fix processing of unordered MLPD events, which makes allocation address changes, as well as other data, work reliably
* Avoid adding duplicate objects to Snapshots

## Mac:

* Fix floating scrollbar look & behavior in instrument charts
* Several UI tweaks and fixes

## Bugs fixed:

* [51965](https://bugzilla.xamarin.com/show_bug.cgi?id=51965) - .exe app exit not detected
* [51951](https://bugzilla.xamarin.com/show_bug.cgi?id=51951) - Keyboard navigation on Windows
* [51949](https://bugzilla.xamarin.com/show_bug.cgi?id=51949)
* [51828](https://bugzilla.xamarin.com/show_bug.cgi?id=51828)
* [51876](https://bugzilla.xamarin.com/show_bug.cgi?id=51876)
* [51896](https://bugzilla.xamarin.com/show_bug.cgi?id=51896)
* [51890](https://bugzilla.xamarin.com/show_bug.cgi?id=51890)
* [51899](https://bugzilla.xamarin.com/show_bug.cgi?id=51899)
* [51900](https://bugzilla.xamarin.com/show_bug.cgi?id=51900)
* [51905](https://bugzilla.xamarin.com/show_bug.cgi?id=51905)
* [51906](https://bugzilla.xamarin.com/show_bug.cgi?id=51906)
* [51907](https://bugzilla.xamarin.com/show_bug.cgi?id=51907)
* [51826](https://bugzilla.xamarin.com/show_bug.cgi?id=51826) - Keyboard navigation on Mac
* [51837](https://bugzilla.xamarin.com/show_bug.cgi?id=51837)
* [51871](https://bugzilla.xamarin.com/show_bug.cgi?id=51871)
* [44873](https://bugzilla.xamarin.com/show_bug.cgi?id=44873) - Thread charts disappears on small window sizes
* [44837](https://bugzilla.xamarin.com/show_bug.cgi?id=44837) - Scrollbar missing
* [44242](https://bugzilla.xamarin.com/show_bug.cgi?id=44242) - Allocations pie chart is small and distorted
* [49792](https://bugzilla.xamarin.com/show_bug.cgi?id=49792) - Side tabs in New Session dialog take a lot of space
* [43303](https://bugzilla.xamarin.com/show_bug.cgi?id=43303) - Use monospace font for detail area lists
* [52053](https://bugzilla.xamarin.com/show_bug.cgi?id=52053) - Drilling down/up allocations doesn't clear filters
* [51713](https://bugzilla.xamarin.com/show_bug.cgi?id=51713) - Crash when Xcode not installed
* [45551](https://bugzilla.xamarin.com/show_bug.cgi?id=45551) - Inverted call tree doesn't aggregate leaf nodes
* [53011](https://bugzilla.xamarin.com/show_bug.cgi?id=53011) - Crash when navigating to buttons with keyboard
* [40596](https://bugzilla.xamarin.com/show_bug.cgi?id=40596) - Snapshot markers are misplaced

# System Requirements

## Mac

* Xamarin Studio
* XCode 8.x for profiling iOS applications

## Windows

* Visual Studio
* Xamarin for Visual Studio
* A Mac, with XCode 8.x installed for profiling iOS applications

# Known issues

While this is a stable product now, and work is already underway to make the product better as well as
have shiny new features, there are still some known limitations:

* No official support for profiling Release builds
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful.

