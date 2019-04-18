---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.9-0"
---

This is the initial preview release of the Xamarin Profiler. The features include:

* Support for launching and profiling iOS (Mac only) and Android applications (Windows & Mac)
* Two instruments - Allocations & Time Profiler
* Summary of allocations with option to see callers and backtrace, as well as sorting and search on Mac
* Call tree for drilling down, with options to separate by thread and invert (supported on Mac only)
* Samples list and call tree for Time Profiler/performance.
* Generations to take and review memory snapshots (supported on Mac only)
* Allocations list with addresses/size/caller info on all allocated objects.
* Support for lightweight integration with Xamarin Studio on Mac and Windows and Visual Studio
* Support for profiling most build configs on Android and Debug build configuration in iOS.
* Support for Android devices and emulators, including Xamarin Android Player.
* Support for iOS Simulator.

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* Profiling Mac apps is not yet available.
* Limited support for iOS device profiling.
* No official support for profiling Release builds
* Snapshots, call tree sorting not implemented on Windows
* Can't search call tree on Mac or Windows
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Chart drawing is somewhat unstable, especially for allocations
* No support for comparing/seeing delta of snapshots in this version
* Samples list not available on Android
* Live/Dead object status not yet supported - profiler always shows live

We encourage users to get in touch and file bug reports so we can continue to make this tool more useful and more stable.

