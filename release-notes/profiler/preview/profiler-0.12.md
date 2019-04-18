---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.12"
---

This is the 5th preview release of the Xamarin Profiler. Changes since last release include:

Common:

* Support MLPD v8
* Support installed and relocated mono runtimes (via PROFILER\_MONO\_RUNTIME env var)
* Call tree without method enter/leave
* Big performance improvements
* Take into account method leave with exceptions
* Display current memory usage in Allocations’ chart (for runtimes with perf counters)
* Allow sorting of Allocations List by Caller
* Re-enable template selector
* Re-enable library dialog
* Detect when Android activities die
* Display console output for Android runs
* ‘Take snapshot’ button now in toolbar
* Clean up markers for generics and runtime wrapper methods

Windows:

* Get rid of single instance restriction
* Add about dialog
* Move Inverted/By thread call tree to right panel
* Display stack traces for snapshot allocations
* Improve list/tree views performance and look&feel
* Display full namespaces in Snapshots view
* Make Call Tree the default view for Time instrument
* Set window’s title when live profiling
* Make right side panel collapsable
* Toolbar icons are now all of the same size
* Ask for confirmation when closing a running session
* Enable console view when live profiling

Mac:

* Add tooltips to toolbar buttons
* Fix sorting in Snapshots view
* Highlight class names in views

Bugs fixed:

* [25285](https://bugzilla.xamarin.com/show_bug.cgi?id=25285) - Profiler does not remember the 'Snapshots' preference setting
* [25282](https://bugzilla.xamarin.com/show_bug.cgi?id=25282) - 'Auto Snapshots' textbox should enabled only if we select radio button 'Every' in tools/preferences
* [26458](https://bugzilla.xamarin.com/show_bug.cgi?id=26458) - Installer doesn't place Xamarin.Profiler to /Applications folder
* [26952](https://bugzilla.xamarin.com/show_bug.cgi?id=26952) - Profiler does not remember the 'General' preference setting
* [25765](https://bugzilla.xamarin.com/show_bug.cgi?id=25765) - Xamarin profiler for android crashes on multithreaded app
* [26947](https://bugzilla.xamarin.com/show_bug.cgi?id=26947) - Instrument section in windows profiler is not identical to mac profiler
* [26946](https://bugzilla.xamarin.com/show_bug.cgi?id=26946) - Profiler does not show correct version number in About
* [27393](https://bugzilla.xamarin.com/show_bug.cgi?id=27393) - Snapshot 0 is showing changes from snapshot 3
* [27221](https://bugzilla.xamarin.com/show_bug.cgi?id=27221) - Profiler does not generate graph and data when user select already saved .mlpd file in target dropdown
* [25827](https://bugzilla.xamarin.com/show_bug.cgi?id=25827) - Expended rows getting collapsed when user click on header to sort data in extended detail pan
* [26504](https://bugzilla.xamarin.com/show_bug.cgi?id=26504) - Windows profiler takes time to show data and graphs in profiler windows
* [27555](https://bugzilla.xamarin.com/show_bug.cgi?id=27555) - Already saved .mlpd file is open in same window, when user try to open it via 'File >Open...'
* [27552](https://bugzilla.xamarin.com/show_bug.cgi?id=27552) - Sorting on column 'Name' is not working properly for Snapshots
* [27554](https://bugzilla.xamarin.com/show_bug.cgi?id=27554) - Checkbox 'Separate by Thread' and 'Invert Call Tree' is not enable for 'Call Tree' for instrument 'Time Profiler'
* [27422](https://bugzilla.xamarin.com/show_bug.cgi?id=27422) - 'Auto Snapshots' textbox value is getting reset when user select checkbox 'On garbage collections'
* [27890](https://bugzilla.xamarin.com/show_bug.cgi?id=27890) - User is not able to select instrument in instrument selector dialog on first click of 'Choose' button
* [27892](https://bugzilla.xamarin.com/show_bug.cgi?id=27892) - App selected in instrument selector dialog is not selected in target dropdown on profiler main window
* [27880](https://bugzilla.xamarin.com/show_bug.cgi?id=27880) - Instrument and it's graph section is not aligned properly
* [27885](https://bugzilla.xamarin.com/show_bug.cgi?id=27885) - Profiler is getting crashed when user try to add instrument via button '+'
* [27884](https://bugzilla.xamarin.com/show_bug.cgi?id=27884) - Profiler is getting crashed when user click on button 'Cancel' in instrument selection dialog
* [26947](https://bugzilla.xamarin.com/show_bug.cgi?id=26947) - Instrument section in windows profiler is not identical to mac profiler
* [27949](https://bugzilla.xamarin.com/show_bug.cgi?id=27949) - Not able to add instruments to several open profiler windows
* [27948](https://bugzilla.xamarin.com/show_bug.cgi?id=27948) - Profiler does not show data and chart for already saved .mlpd file if a profiler window is already opened
* [27955](https://bugzilla.xamarin.com/show_bug.cgi?id=27955) - Enable-disable functionality of checkbox 'Separate by Thread' and 'Invert Call Tree' is not working correctally
* [27912](https://bugzilla.xamarin.com/show_bug.cgi?id=27912) - Profiler is getting crashed when we check-uncheck 'Invert call tree' check box
* [27222](https://bugzilla.xamarin.com/show_bug.cgi?id=27222) - When user scroll vertical scroll bar in track pan then instrument section does not scroll with chart

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

