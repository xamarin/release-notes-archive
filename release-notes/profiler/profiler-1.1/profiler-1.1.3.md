---
id: 342345F3-6128-4F23-96DB-63CE86352240
title: "Profiler 1.1.3"
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.1.3-71.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.1.3-71.msi)

# Release notes

## Common:

* Fix automatic snapshots

## Mac:

* Fix LCD view resizing problems
* Beautify Preferences dialog

## Windows:

* Fix support for profiling on Windows iOS simulator

## Bugs fixed:

* [40994](https://bugzilla.xamarin.com/show_bug.cgi?id=40994) - Can't stop apps when profiling on Windows iOS simulator
* [41058](https://bugzilla.xamarin.com/show_bug.cgi?id=41058) - Can't profile apps on Windows iOS simulator
* [46119](https://bugzilla.xamarin.com/show_bug.cgi?id=46119) - Mac main window not saving correctly its size
* [49800](https://bugzilla.xamarin.com/show_bug.cgi?id=49800) - AddInstrument dialog tweaks
* [46989](https://bugzilla.xamarin.com/show_bug.cgi?id=46989) - Missing error message when Xcode not installed
* [46475](https://bugzilla.xamarin.com/show_bug.cgi?id=46475) - Auto snapshots not working
* [49791](https://bugzilla.xamarin.com/show_bug.cgi?id=49791) - Target not selectable on first run
* [49803](https://bugzilla.xamarin.com/show_bug.cgi?id=49803) - Search box hard to see in the bottom
* [49804](https://bugzilla.xamarin.com/show_bug.cgi?id=49804) - Allocations pie chart visual improvements


While this is a stable product now, and work is already underway to make the product better as well as
have shiny new features, there are still some known limitations:

* No official support for profiling Release builds
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful.

