---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.9-29"
---

This is the 2nd preview release of the Xamarin Profiler. Changes since last release include:

* Sort heapshot view by timestamp by default
* Show backtrace for snapshot objects
* Fix resizing of ‘Take snapshot’ button
* Make backtrace view resize correctly to fit contents
* Fix dynamic resizing of Backtrace view
* Use ‘Snapshot’ instead of ‘Generation’ in UI strings
* Only change position of detail view's divider if extended area is collapsed
* Fix profiling on iOS devices
* Some small performance improvements
* Quote iOS .app paths, in case it has spaces
* Fix displaying of ‘running time’ in Instruments summary
* Fix “peaks” in allocations chart plot

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* Profiling Mac apps is not yet available.
* No official support for profiling Release builds
* Snapshots, call tree sorting not implemented on Windows
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* No support for comparing/seeing delta of snapshots in this version
* Samples list not available on Android
* Live/Dead object status not yet supported - profiler always shows live

We encourage users to get in touch and file bug reports so we can continue to make this tool more useful and more stable.

