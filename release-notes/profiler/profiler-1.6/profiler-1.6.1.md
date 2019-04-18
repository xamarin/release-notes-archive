---
id: 5E7A2B6E-63EB-4423-A1A4-A8A12D7F3DAF
title: "Profiler 1.6.1"
dateupdated: 2018-02-07
---

# 1.6.1-483 (2018-02-07)

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.1-483.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.1-483.msi)

## Mac

* Fix profiling Mac apps built with Mono 5.8 and higher
* Fix several glitches in Cycles and Path to Roots views
* Fix crash when selecting snapshots in Snapshots view

## Windows

* Fix crash when profiling iOS app without the iOS Windows simulator installed
* Fix crash in Mac ProfilerAgent because of missing CoreML.dll
* Fix several glitches in New Session dialog

# 1.6.1-469 (2018-01-19)

**This is a beta of the upcoming Xamarin Profiler 1.6.1 release. These previews are unsupported builds to allow
developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.1-469.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.1-468.msi)

## Common

* Display count of current live objects in allocations and snapshots views
* Add a better visual indication of where context actions are available to the user
* Fix light allocations profiling mode

# 1.6.1-462 (2018-01-08)

**This is a beta of the upcoming Xamarin Profiler 1.6.1 release. These previews are unsupported builds to allow
developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.1-462.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.1-462.msi)

## Common

* Support latest GC roots reporting from Mono runtime profiler
* Stability improvements
* Convert New Session dialog to a wizard, for a better UX
* Merge Allocations and Cycles instruments
* Improve look&feel of Size and Count columns (columns with a % indicator)
* Allow light allocations profiling mode
* Add a better visual indication of where context actions are available to the user
* Improve roots&cycles view and information

## Bugs fixed

- [51925](https://bugzilla.xamarin.com/show_bug.cgi?id=51925) - A11Y usability fixes
- [51926](https://bugzilla.xamarin.com/show_bug.cgi?id=51926) -
- [51929](https://bugzilla.xamarin.com/show_bug.cgi?id=51929) -
- [51931](https://bugzilla.xamarin.com/show_bug.cgi?id=51931) -
- [51922](https://bugzilla.xamarin.com/show_bug.cgi?id=51922) -
- [51911](https://bugzilla.xamarin.com/show_bug.cgi?id=51911) -
- [51891](https://bugzilla.xamarin.com/show_bug.cgi?id=51891) - VoiceOver usage fixes

## Windows

- Fix weird behaviour of Search entry's completion popup menu
- Huge performance improvements in tree views (Call Tree and Roots&Cycles views)
