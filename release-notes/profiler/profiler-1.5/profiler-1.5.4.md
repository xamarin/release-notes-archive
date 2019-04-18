---
id: A57A565F-15B5-41EF-9240-1ECF7C2E398C
title: "Profiler 1.5.4"
dateupdated: 2017-05-02
---

# 1.5.4-19 (2017-05-02)

* [Mac](https://dl.xamarin.com/profiler/profiler-mac-1.5.4-19.pkg)
* [Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.5.4-19.msi)

## Windows:

* Display missing class name when grouping allocations by method

## Bugs fixed:

* [51916](https://bugzilla.xamarin.com/show_bug.cgi?id=51916) - Empty accessibility property
* [51915](https://bugzilla.xamarin.com/show_bug.cgi?id=51915) - Keyboard focus order wrong
* [51846](https://bugzilla.xamarin.com/show_bug.cgi?id=51846) - Inspector detail pane button not accessible with keyboard
* [51870](https://bugzilla.xamarin.com/show_bug.cgi?id=51870) - Inspector view not accessible with keyboard
* [51847](https://bugzilla.xamarin.com/show_bug.cgi?id=51847) - Focus jumps out of search box

# 1.5.4-11 (2017-04-24)

* [Mac](https://dl.xamarin.com/profiler/profiler-mac-1.5.4-11.pkg)
* [Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.5.4-11.msi)

## Mac:

* Right-align numeric text fields
* Fix storing of recent items list

## Bugs fixed:

* [53905](https://bugzilla.xamarin.com/show_bug.cgi?id=53905) - Crash when Xamarin.Android not installed
* [45826](https://bugzilla.xamarin.com/show_bug.cgi?id=45826) - Confusing relative % values in call tree
* [55262](https://bugzilla.xamarin.com/show_bug.cgi?id=55262) - Missing dependency in Windows installer
* [55163](https://bugzilla.xamarin.com/show_bug.cgi?id=55163) - Instruments list refreshed every second
* [51917](https://bugzilla.xamarin.com/show_bug.cgi?id=51917) - Can't close about dialog with keyboard
* [51927](https://bugzilla.xamarin.com/show_bug.cgi?id=51927) - Wrong focus order in 'Add instrument' dialog

# System Requirements

## Mac

* Xamarin Studio
* XCode 8.x for profiling iOS applications
* Xamarin.Android for profiling Android applications

## Windows

* Visual Studio
* Xamarin for Visual Studio
* A Mac, with XCode 8.x installed for profiling iOS applications
* Xamarin.Android for profiling Android applications

# Known issues

While this is a stable product now, and work is already underway to make the product better as well as
have shiny new features, there are still some known limitations:

* No official support for profiling Release builds
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful.

