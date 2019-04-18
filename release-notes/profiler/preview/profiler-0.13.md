---
id: 64C3706B-7A0A-4CAE-B76C-9DE236C289DA
title: "Profiler Preview 0.13"
---

This is the 6th preview release of the Xamarin Profiler. Changes since last release include:

Common:

* Remove “Enable snapshots” setting in Preferences dialog
* Add ‘Open logs’ to Help menu
* Improve memory usage
* Add help menu item
* Improve performance when processing snapshots
* Hide Count column in Call Tree when not using method enter/leave
* Fix event reading crash in Windows VMs
* Store all object references in Snapshot events
* Add inverse references right side panel for allocations list and snapshots views

Windows:

* Fix drill down on several levels
* Fix crash when clicking on instrument area with no instruments
* Deal correctly with empty data sets
* Allow profiling as soon as a target and at least 1 instrument are selected
* Fix instrument registration
* Remove icons in drill down area
* Disable target selector when profiling
* Add dynamic right side panels based on the left side view
* Resize right-side panel columns to fit content
* Display Self allocations time in Allocations call tree (instead of Self time)

Mac:

* Fix MLPD location setting
* New UI design
* Don’t expand inspector area when double clicking a column
* Fix ascending/descending indicators in detail views
* Don’t flicker when switching selection in instrument selector
* Disable call tree display options when in drill down mode
* Add icons to allocations summary
* Remove row number column in allocations list
* Improve look of timeline header
* Add collapse/expand button for right side panel
* Fix Stop button responsiveness

Bugs fixed:

* [27944](https://bugzilla.xamarin.com/show_bug.cgi?id=27944) - Profiler does not generate and display data properly for instruments Allocations and Time Profiler in details pan
* [28161](https://bugzilla.xamarin.com/show_bug.cgi?id=28161) - User is not able to profile an android app
* [27718](https://bugzilla.xamarin.com/show_bug.cgi?id=27718) - Clean up markers for Generics
* [28408](https://bugzilla.xamarin.com/show_bug.cgi?id=28408) - Console tab is displaying for Time Profiler and got disappeared for Allocations
* [28458](https://bugzilla.xamarin.com/show_bug.cgi?id=28458) - Profiler crash on filtering items
* [28233](https://bugzilla.xamarin.com/show_bug.cgi?id=28233) - Objects not showing up in snapshots delta
* [28237](https://bugzilla.xamarin.com/show_bug.cgi?id=28237) - Missing Help->Open Log Directory like in XS
* [27215](https://bugzilla.xamarin.com/show_bug.cgi?id=27215) - Profiler does not generate identical graph for newly added instrument when we re-run the profiler for already saved .mlpd file
* [28421](https://bugzilla.xamarin.com/show_bug.cgi?id=28421) - Play button should be disabled when user does not select any instrument and does not select anything in target dropdown
* [27552](https://bugzilla.xamarin.com/show_bug.cgi?id=27552) - Sorting on column 'Name' is not working properly for Snapshots
* [27875](https://bugzilla.xamarin.com/show_bug.cgi?id=27875) - Profiler does not generate graph and data on second profiler run
* [27420](https://bugzilla.xamarin.com/show_bug.cgi?id=27420) - Android app is getting crashed when user is trying to start profiler

#Limitations

This is a preview release and there are definite limitations, including but not limited to:

* No official support for profiling Release builds
* Data sets are correct at time of collection but data mining and representation is preliminary. This will improve in future releases.
* Samples list not available on Android
* Support for Xamarin.Mac app profiling is preliminary
* Enabling Boehm for iOS builds results in no useful data on devices, as allocations and calls need to be disabled
* Performance with large apps has been improved, but still lacking some
* Android profiling doesn't work with Xamarin.Android update from Alpha channel

We encourage users to get in touch and [file bug reports](https://bugzilla.xamarin.com/enter_bug.cgi?product=Profiler) so we can continue to make this tool more useful and more stable.

