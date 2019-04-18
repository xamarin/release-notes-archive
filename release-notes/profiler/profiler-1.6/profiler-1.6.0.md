---
id: 5E7A2B6E-63EB-4423-A1A4-A8A12D7F3DAF
title: "Profiler 1.6.0"
dateupdated: 2018-01-05
---

# 1.6.0-27 (2018-01-05)

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.0-27.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.0-27.msi)

## Windows

- Fix breakage with activation of Windows local iOS simulator

## Bugs fixed

- [60963](https://bugzilla.xamarin.com/show_bug.cgi?id=60963) - Mono runtime not found on some devices

# 1.6.0-25 (2017-11-29)

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.0-25.pkg)

## Bugs fixed

* [60822](https://bugzilla.xamarin.com/show_bug.cgi?id=60822) - Broken XamarinProfiler.Mac package

# 1.6.0-21 (2017-11-29)

* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.0-21.msi)

## Bugs fixed

* [60709](https://bugzilla.xamarin.com/show_bug.cgi?id=60709) - Starts profiling when user cancels New Session dialog

# 1.6.0-16 (2017-10-23)

**This is a beta of the upcoming Xamarin Profiler 1.6.0 release. These previews are unsupported builds to allow
developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.0-16.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.0-16.msi)

## Mac

* Fix app icon on High Sierra

## Windows

* Stability improvements for iOS profiling

# 1.6.0-3 (2017-10-12)

**This is a beta of the upcoming Xamarin Profiler 1.6.0 release. These previews are unsupported builds to allow
developers to test the new features, and to gather feedback and bug reports. Your help is very appreciated!**

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.6.0-3.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.6.0-3.msi)

## Common

* Performance improvements
* Allow allocations to be grouped by thread
* Charts performance and UI improvements
* Allow selection of sampling mode
* Display allocations groups' averages
* Fix a bug in object roots processing that was displaying roots of the wrong type
* Translations for Czech (cs), German (de), Spanish (es), French (fr), Italian (it), Japanese (ja), Korean (ko), Polish (pl), Portuguese (pt), Russian (ru), Turkish (tr), Traditional Chinese (zh)

## Mac

* Use generic colors in most places, for a better support of theme-oriented user customisations
* Add % bar to sizes columns, for a better visual indication
* Lots of small UI tweaks and improvements for a much better UI

## Windows

* Remove empty space in Console tab view
* Fix column sorting in instrument detail views
* Fix displaying of classes and methods without namespaces
* Fix scroll bar behavior in per-thread charts
* Fix usage of user-provided settings in New Session dialog
* Performance and full accessibility support in data lists

## Bugs fixed

* [59226](https://bugzilla.xamarin.com/show_bug.cgi?id=59226) - Can't profile iOS and tvOS apps
* [51920](https://bugzilla.xamarin.com/show_bug.cgi?id=51920) - HighContrast theme problems on Windows
