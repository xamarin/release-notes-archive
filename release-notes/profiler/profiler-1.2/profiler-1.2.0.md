---
id: D6D55D97-249D-4951-9F6F-8BFBAF2209BE
title: "Profiler 1.2.0"
dateupdated: 2017-02-22
---


The new release is available now for download:

* [Xamarin Profiler for Mac](https://dl.xamarin.com/profiler/profiler-mac-1.2.0-6.pkg)
* [Xamarin Profiler for Windows](https://dl.xamarin.com/profiler/XamarinProfiler.Windows.Installer.1.2.0-6.msi)

# Release notes

This 1.2.0 release is the 2nd stable release of the Xamarin Profiler, a tool to profile the behavior of your applications, ensuring they are free from performance and memory-related issues.

For this new stable release, the focus has been on stabilizing the current code, fixing bugs and starting to introduce internal changes that will lead to the addition of new cool features.

## Common:

* Improve performance when drawing per-thread charts
* Improvements on iOS profiling for both Mac and Windows
* Fix automatic snapshots

## Mac:

* Lots of UI tweaks and fixes

## Windows:

* Better error reporting on iOS profiling
* Fix support for profiling on Windows iOS simulator

## Bugs fixed:

* [45362](https://bugzilla.xamarin.com/show_bug.cgi?id=45362) - Popup window not getting hidden
* [47581](https://bugzilla.xamarin.com/show_bug.cgi?id=47581) - Can't choose target after canceling new session dialog
* [46568](https://bugzilla.xamarin.com/show_bug.cgi?id=46568) - Chart not being cleared
* [44884](https://bugzilla.xamarin.com/show_bug.cgi?id=44884) - MLPD file opened on separate window
* [47438](https://bugzilla.xamarin.com/show_bug.cgi?id=47438) - Use correct mono/mono64 when profiling .exe
* [44684](https://bugzilla.xamarin.com/show_bug.cgi?id=44684) - Triangles in call tree getting mad
* [44107](https://bugzilla.xamarin.com/show_bug.cgi?id=44107) - Spaces not allowed in search box
* [47648](https://bugzilla.xamarin.com/show_bug.cgi?id=47648) - Crash when grouping allocations by method
* [48541](https://bugzilla.xamarin.com/show_bug.cgi?id=48541) - Instrument selection broken when selecting XM apps
* [49431](https://bugzilla.xamarin.com/show_bug.cgi?id=49431) - Crash in New Session dialog
* [49790](https://bugzilla.xamarin.com/show_bug.cgi?id=49790) - Clarify tab sections titles
* [49796](https://bugzilla.xamarin.com/show_bug.cgi?id=49796) - Missing tooltip in toolbar button
* [40994](https://bugzilla.xamarin.com/show_bug.cgi?id=40994) - Can't stop apps when profiling on Windows iOS simulator
* [41058](https://bugzilla.xamarin.com/show_bug.cgi?id=41058) - Can't profile apps on Windows iOS simulator
* [46119](https://bugzilla.xamarin.com/show_bug.cgi?id=46119) - Mac main window not saving correctly its size
* [49800](https://bugzilla.xamarin.com/show_bug.cgi?id=49800) - AddInstrument dialog tweaks
* [46989](https://bugzilla.xamarin.com/show_bug.cgi?id=46989) - Missing error message when Xcode not installed
* [46475](https://bugzilla.xamarin.com/show_bug.cgi?id=46475) - Auto snapshots not working
* [49791](https://bugzilla.xamarin.com/show_bug.cgi?id=49791) - Target not selectable on first run
* [49803](https://bugzilla.xamarin.com/show_bug.cgi?id=49803) - Search box hard to see in the bottom
* [49804](https://bugzilla.xamarin.com/show_bug.cgi?id=49804) - Allocations pie chart visual improvements
* [49802](https://bugzilla.xamarin.com/show_bug.cgi?id=49802) - Wrong column alignments
* [49801](https://bugzilla.xamarin.com/show_bug.cgi?id=49801) - Inspector tab icons look blurry
* [49669](https://bugzilla.xamarin.com/show_bug.cgi?id=49669) - Snapshots filtering not working
* [46472](https://bugzilla.xamarin.com/show_bug.cgi?id=46472) - Unable to group allocations by class/method
* [51237](https://bugzilla.xamarin.com/show_bug.cgi?id=51237) - Unable to check 'only live objects'
* [49033](https://bugzilla.xamarin.com/show_bug.cgi?id=49033) - Start button disabled after profiling stopped
* [51265](https://bugzilla.xamarin.com/show_bug.cgi?id=51265) - Unable to save snapshot setting
* [51349](https://bugzilla.xamarin.com/show_bug.cgi?id=51349) - NRE crash when opening new session dialog
* [51171](https://bugzilla.xamarin.com/show_bug.cgi?id=51171) - Too many snapshots taken when automatic snapshots enabled
* [50198](https://bugzilla.xamarin.com/show_bug.cgi?id=50198) - Timer goes backwards
* [47635](https://bugzilla.xamarin.com/show_bug.cgi?id=47635) - Can't downgrade to stable version
* [43459](https://bugzilla.xamarin.com/show_bug.cgi?id=43459) - Search filter doesn't match UI
* [44824](https://bugzilla.xamarin.com/show_bug.cgi?id=44824) - Search box dropdown not working properly
* [45822](https://bugzilla.xamarin.com/show_bug.cgi?id=45822) - Use correct mono binary depending on exe bitness
* [51304](https://bugzilla.xamarin.com/show_bug.cgi?id=51304) - Window header disappears when shrinking
* [48643](https://bugzilla.xamarin.com/show_bug.cgi?id=48643) - Uncaught exception when mlaunch fails with XCode not installed
* [49797](https://bugzilla.xamarin.com/show_bug.cgi?id=49797) - Switching instruments is slow
* [44684](https://bugzilla.xamarin.com/show_bug.cgi?id=44684) - Triangles in call tree getting misplaced
* [49167](https://bugzilla.xamarin.com/show_bug.cgi?id=49167) - Status bar stuck in 'Stopping remote app...'
* [51761](https://bugzilla.xamarin.com/show_bug.cgi?id=51761) - Auto snapshots not working on Windows
* [46119](https://bugzilla.xamarin.com/show_bug.cgi?id=46119) - Window position not saved correctly
* [52321](https://bugzilla.xamarin.com/show_bug.cgi?id=52321) - Can't profile iOS from VS
* [51558](https://bugzilla.xamarin.com/show_bug.cgi?id=51558) - Xam.Mac app not killed when stopping profiler

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

