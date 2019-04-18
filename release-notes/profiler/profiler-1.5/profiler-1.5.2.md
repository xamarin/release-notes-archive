---
id: F15ECAE1-1C17-438D-AE69-1E7FB101307D
title: "Profiler 1.5.2"
dateupdated: 2017-04-06
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.5.2-0.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.5.2-0.msi)

# Release notes

## Common:

* Show snapshots comparison in snapshots tooltips
* Allow allocations to be grouped by assembly also


## Mac:

* Improve charts

## Bugs fixed:

* [53842](https://bugzilla.xamarin.com/show_bug.cgi?id=53842) - Crash when displaying snapshot popup
* [53841](https://bugzilla.xamarin.com/show_bug.cgi?id=53841) - Snapshot popup showing randomly
* [53847](https://bugzilla.xamarin.com/show_bug.cgi?id=53847) - Missing comparison chart in 1st snapshot popup
* [53440](https://bugzilla.xamarin.com/show_bug.cgi?id=53440) - Crash when converting perf counter values
* [51883](https://bugzilla.xamarin.com/show_bug.cgi?id=51883) - VoiceOver focus wrong in New Session dialog
* [51887](https://bugzilla.xamarin.com/show_bug.cgi?id=51887) - VoiceOver focus wrong in New Session dialog
* [54259](https://bugzilla.xamarin.com/show_bug.cgi?id=54259) - Wrong selection when window resized
* [54260](https://bugzilla.xamarin.com/show_bug.cgi?id=54260) - Allocations not displayed when selecting time range
* [54263](https://bugzilla.xamarin.com/show_bug.cgi?id=54263) - Changing selection doesn't refresh allocations

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

