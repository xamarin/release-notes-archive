---
id: F372B4F3-0B88-4C3D-A3B0-8F3BFB917928
title: "Profiler 1.3.3"
dateupdated: 2017-03-16
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.3.3-6.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.3.3-6.msi)

# Release notes

## Common:

* Don't recalculate samples timing, so that they match timing in call tree
* Fix processing of unordered MLPD events, which makes allocation address changes, as well as other data, work reliably
* Avoid adding duplicate objects to Snapshots

## Bugs fixed:

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

