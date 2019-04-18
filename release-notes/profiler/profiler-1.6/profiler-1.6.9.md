---
id: a032683d-1340-4c37-b7fb-f0287f13115f
title: "Profiler 1.6.9"
dateupdated: 2018-12-04
---

**This is a preview of the upcoming Xamarin Profiler 1.6.9 release. These previews are unsupported builds to allow
developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.9-390.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.9-390.msi)

# What's New in 1.6.9

## Releases

* [December 4, 2018](#1.6.9-390)

## Release Highlights

For 1.6.9, our focus has been on improving the current UI, to make it more intuitive and easier to discover the operations that are available to users. More specifically:

* We have added all available operations to context menus, so that they are easily discoverable
* We have greatly improved the Snapshots view, not only to make it look cleaner and better, but also to display all the interesting information, which would help users in finding where to start looking for problems. For this, we now display nice charts, which allow to spot "problematic" snapshots very easily, and also improve the snapshots comparison, to allow users to easily see new and persistent objects given two snapshots.
* We have made the UI much more dynamic, just enabling some UI bits only after data displayed on that specific UI is available, not before, to avoid confusion.

Also, we have added a new mode for time profiling, the Tracing mode, which, using Mono's Profiler's method enter/leave feature, allows users to get an exact picture of what their applications are doing, as it records every single method call in the application being profiled. Of course, this affects the performance of the profiled app, as it needs to record a lot of data, so it's a great help for most mobile applications, but might greatly affect the performance, not only of the profiled app, but of the Xamarin Profiler itself, if used on a desktop or greatly misbehaving applications, so use wisely. But, as mentioned, for iOS/Android applications, it should be a great improvement over the previous sampling-based Time profiler mode(s).

And, as usual, we have fixed hundreds of bugs, too many to list here!

## 1.6.9-390

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.9-390.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.9-390.msi)

### What's New in 1.6.9-390

* Improve Snapshots view
* Make UI more dynamic, just enabling bits only when data is available
* Added new tracing mode for the Time Profiler

And hundreds of bug fixes, of which the most notorious are:

* Fixes sorting descriptors when restarting a new session
* Display exceptions also when using the Allocations instrument alone
* Several Accessibility-related issues
* Add more operations to context menus, so that they are easily discoverable
* Work around bug in Mono when multiplying longs by 100
* Fix Windows UI to behave better on small screen resolutions
* Fix crash when selecting an empty range in Samples view
* Fix starting of remote Windows simulator
* Fix missing redraws when window's size changed
* Fix crash when selecting "Show in call tree" in Snapshots view
* Fix crash when collapsing Filter section on Windows UI
* Fix Pause/Resume toolbar buttons' tooltips
* Fix scrolling via keyboard on Console view