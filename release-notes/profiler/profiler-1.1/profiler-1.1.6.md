---
id: E26D5086-4FB5-404E-A220-B5445261FF32
title: "Profiler 1.1.6"
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.1.6-39.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.1.6-39.msi)

# Release notes

## Bugs fixed:

* [51349](https://bugzilla.xamarin.com/show_bug.cgi?id=51349) - NRE crash when opening new session dialog
* [51171](https://bugzilla.xamarin.com/show_bug.cgi?id=51171) - Too many snapshots taken when automatic snapshots enabled
* [50198](https://bugzilla.xamarin.com/show_bug.cgi?id=50198) - Timer goes backwards
* [47438](https://bugzilla.xamarin.com/show_bug.cgi?id=47438) - Use correct mono binary depending on exe bitness
* [47635](https://bugzilla.xamarin.com/show_bug.cgi?id=47635) - Can't downgrade to stable version
* [43459](https://bugzilla.xamarin.com/show_bug.cgi?id=43459) - Search filter doesn't match UI
* [44824](https://bugzilla.xamarin.com/show_bug.cgi?id=44824) - Search box dropdown not working properly
* [45822](https://bugzilla.xamarin.com/show_bug.cgi?id=45822) - Use correct mono binary depending on exe bitness
* [51304](https://bugzilla.xamarin.com/show_bug.cgi?id=51304) - Window header disappears when shrinking
* [48643](https://bugzilla.xamarin.com/show_bug.cgi?id=48643) - Uncaught exception when mlaunch fails with XCode not installed


While this is a stable product now, and work is already underway to make the product better as well as
have shiny new features, there are still some known limitations:

* No official support for profiling Release builds
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful.

