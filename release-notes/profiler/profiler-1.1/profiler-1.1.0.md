---
id: FE698ADB-7F59-40A3-8A1D-35E17BF355A5
title: "Profiler 1.1.0"
---


The new release is [available](http://xamarin.com/profiler) now for download.

# Release notes

## Common:

* Improve performance when drawing per-thread charts
* Add tooltips to cycles' graph view

## Mac

* Improve resizing and positioning of allocations tooltip

## Windows

* Fix missing log entries in ProfilerAgent logs

## Bugs fixed:

* [45362](https://bugzilla.xamarin.com/show_bug.cgi?id=45362) - Popup window not getting hidden
* [47581](https://bugzilla.xamarin.com/show_bug.cgi?id=47581) - Can't choose target after canceling new session dialog
* [46568](https://bugzilla.xamarin.com/show_bug.cgi?id=46568) - Chart not being cleared
* [44884](https://bugzilla.xamarin.com/show_bug.cgi?id=44884) - MLPD file opened on separate window
* [47438](https://bugzilla.xamarin.com/show_bug.cgi?id=47438) - Use correct mono/mono64 when profiling .exe
* [44684](https://bugzilla.xamarin.com/show_bug.cgi?id=44684) - Triangles in call tree getting mad
* [44107](https://bugzilla.xamarin.com/show_bug.cgi?id=44107) - Spaces not allowed in search box
* [47648](https://bugzilla.xamarin.com/show_bug.cgi?id=47648) - Crash when grouping allocations by method

While this is a stable product now, and work is already underway to make the product better as well as
have shiny new features, there are still some known limitations:

* No official support for profiling Release builds
* Time instrument not available for tvOS profiling

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful.

