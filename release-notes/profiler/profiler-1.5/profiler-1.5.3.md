---
id: 450B8BDA-4421-475C-9348-F9776E066202
title: "Profiler 1.5.3"
dateupdated: 2017-04-18
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.5.3-10.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.5.3-10.msi)

# Release notes

## Common:

* Allow changing profiling options between runs

## Mac:

* Fix quoting of .exe process arguments

## Windows

* Provide keyboard support to most chart features

## Bugs fixed:

* [52930](https://bugzilla.xamarin.com/show_bug.cgi?id=52930) - Pie chart is too small on default window size
* [51932](https://bugzilla.xamarin.com/show_bug.cgi?id=51932) - Windows chart keyboard navigation
* [51933](https://bugzilla.xamarin.com/show_bug.cgi?id=51933)
* [51839](https://bugzilla.xamarin.com/show_bug.cgi?id=51839) - No visual indication of focus in instruments list
* [46124](https://bugzilla.xamarin.com/show_bug.cgi?id=46124) - More precise time selection

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

