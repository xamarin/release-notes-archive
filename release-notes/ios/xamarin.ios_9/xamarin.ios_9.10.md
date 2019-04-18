---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 9.10"
---

version:9.10.0
releasedate:2016-09-07

<div class="note">
	<b>Classic Profile Deprecation:</b>
	As new platforms are added in Xamarin.iOS we are starting to gradually deprecate features from the classic profile (monotouch.dll).
	In this release the Boehm garbage collector has been removed (it was never an option available to unified applications).
	The complete removal of classic support is scheduled for next fall with the release of Xamarin.iOS 10.0.
</div>

Requirements
============

- The latest features and API requires Xcode 7.3 and the bundled iOS 9.3 SDK;
- Apple Xcode 7.3 requires a Mac running OSX 10.11 (El Capitan)

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
made available at [Evolve 2016](https://evolve.xamarin.com), and include some additional
IDE integration tools.

This release is based on Mono 4.6 which continues to adopt more code from 
Microsoft's open sourced .NET code (reference source) to improve the conformance,
speed and memory usage of our base class libraries (BCL).

### watchOS 2.x

Xamarin.iOS 9.10 introduce **preview** support for **native watchOS 2.x** applications running on both the simulator and devices. This is still early support and we appreciate your feedback and bug reports. Please report any issues on [bugzilla](https://bugzilla.xamarin.com/).

Note that, as a preview, we are not committed to binary compatibility for future releases and, while nothing drastic is planned, a few things might change to accomodate the platform limits and restrictions.

### Enhanced netstandard support

This release includes enhanced conformance to [netstandard](https://github.com/dotnet/corefx/blob/master/Documentation/architecture/net-platform-standard.md#list-of-net-corefx-apis-and-their-associated-net-platform-standard-version) that was introduced in Xamarin.iOS 9.8.2 (SR1)

### Analysis Rules

This release includes our first (of many) analysis rule. Try it on your solutions by using **Project**, **Run Code Analysis** from Xamarin Studio menu.

### API diff

The following documents contains a complete list of the API changes in:

* [iOS](/releases/ios/api_changes/ios_9.8.0_to_9.10.0);
* [tvOS](/releases/ios/api_changes/tvos_9.8.0_to_9.10.0);
* note: The watchOS API are new in 9.10 and remains a **preview without a stable API**


Known issues
============

* **Issue:** watchOS 2.x does not offer direct access to sockets. Most of our managed network stack won't work without them.
	* **Workaround** Use native API for networking usage

* **Issue:** Debugging on watchOS devices can be slow and unreliable
	* **Workaround** This [document](https://github.com/xamarin/xamarin-macios/wiki/Debugging-on-watchOS-device) provides some tips to help you.
	
* **Issue:** Different TLS handlers behave differently and some iOS changes can throw in different places leading to crashes [42443](https://bugzilla.xamarin.com/show_bug.cgi?id=42443) [43794](https://bugzilla.xamarin.com/show_bug.cgi?id=43794) [42796](https://bugzilla.xamarin.com/show_bug.cgi?id=42796)
	* **Workaround** Try a different handler (e.g. Mono vs Apple TLS) to see if this solves the issue.

Bug Fixes
=========

* [24078](https://bugzilla.xamarin.com/show_bug.cgi?id=24078) - [uikit] Add events for UIPresentationController
* [34816](https://bugzilla.xamarin.com/show_bug.cgi?id=34816) - [foundation] Overload the == and != operators of the NSUrl class
* [35012](https://bugzilla.xamarin.com/show_bug.cgi?id=35012) - [foundation] Add missing API for NSExpression and ensure properties work with the correct expression types
* [40583](https://bugzilla.xamarin.com/show_bug.cgi?id=40583) - [msbuild] Link storyboards as part of the IBTool task if Xcode >= 7.0
* [40606](https://bugzilla.xamarin.com/show_bug.cgi?id=40606) - [mtouch] Tweak error message for MT0073 and MT0074
* [40933](https://bugzilla.xamarin.com/show_bug.cgi?id=40933) - [installer] After installing Xamarin Studio, a copy of an installer script is left at the root of the system volume
* [41083](https://bugzilla.xamarin.com/show_bug.cgi?id=41083) - [mlaunch] Set a default simulator if nothing is provided to mlaunch
* [41083](https://bugzilla.xamarin.com/show_bug.cgi?id=41083) - [mtouch] Fix --sdkroot not to report a default to /Developer/
* [41083](https://bugzilla.xamarin.com/show_bug.cgi?id=41083) - [mtouch] Look where XS 6.1+ has installed mlaunch
* [41132](https://bugzilla.xamarin.com/show_bug.cgi?id=41132) - [runtime] Support binding NSObjects as IntPtr
* [41204](https://bugzilla.xamarin.com/show_bug.cgi?id=41204) - [msbuild] Remove empty UIDeviceRequiredCapabilities array
* [41329](https://bugzilla.xamarin.com/show_bug.cgi?id=41329) - [mlaunch] User need to disable then enable the 'Show app on apple watch' option on iPhone to install WatchKit app on watch device
* [41343](https://bugzilla.xamarin.com/show_bug.cgi?id=41343) - [foundation] NSDictionary<TKey, TValue>.FromObjectsAndKeys keys and values are twisted up 
* [41428](https://bugzilla.xamarin.com/show_bug.cgi?id=41428) - [mtouch] Disable fastdev if profiling+fastdev is enabled on a bitcode-capable platform
* [41666](https://bugzilla.xamarin.com/show_bug.cgi?id=41666) - [mtouch] Make sure to reference mono_profiler_startup_log so that the native linker doesn't remove the symbol
* [41684](https://bugzilla.xamarin.com/show_bug.cgi?id=41684) - [CoreGraphics] Fix CGRect.Inflate to work correctly, and add tests
* [41762](https://bugzilla.xamarin.com/show_bug.cgi?id=41762) - [msbuild] Properly archive projects containing WatchOS2 apps
* [41947](https://bugzilla.xamarin.com/show_bug.cgi?id=41947) - [aot] Could not AOT assembly error on building System.Numerics with Release config
* [42006](https://bugzilla.xamarin.com/show_bug.cgi?id=42006) - [mtouch] Quote the .dylib used for incremental builds
* [42015](https://bugzilla.xamarin.com/show_bug.cgi?id=42015) - [foundation] Add missing MutableString binding (#246)
* [42125](https://bugzilla.xamarin.com/show_bug.cgi?id=42125) - [cloudkit] Fix missing [NullAllowed] on CKDatabase.PerformQuery
* [42163](https://bugzilla.xamarin.com/show_bug.cgi?id=42163) - [cloudkit] Fix missing [NullAllowed] on CKFetchRecordChangesOperation .ctor
* [42452](https://bugzilla.xamarin.com/show_bug.cgi?id=42452) - [runtime] Parse unions in objc encodings correctly
* [42454](https://bugzilla.xamarin.com/show_bug.cgi?id=42454) - [registrar] Forward-declare ObjC classes
* [42489](https://bugzilla.xamarin.com/show_bug.cgi?id=42489) - [registrar] Use the correct parameters when generating category methods

* [39236](https://bugzilla.xamarin.com/show_bug.cgi?id=39236) - [runtime] Fix a crash that occurs when Objective-C holds weak references **(9.10.0.38+)**
* [42750](https://bugzilla.xamarin.com/show_bug.cgi?id=42750) - [sdb] Explicitly encode in the JIT debug info whenever there is precise information about variable locations instead of checking whenever the method has seq points **(9.10.0.38+)**
* [42780](https://bugzilla.xamarin.com/show_bug.cgi?id=42780) - [runtime] Make sure to call mono_gc_init_finalizer_thread for watchOS **(9.10.0.38+)**
* [42784](https://bugzilla.xamarin.com/show_bug.cgi?id=42784) - [runtime] Set base directory and config file name for extensions **(9.10.0.38+)**

* [42033](https://bugzilla.xamarin.com/show_bug.cgi?id=42033) - [foundation] NSErrorException should not accept null error, as it will throw later  **(9.10.0.57+)**

* [43099](https://bugzilla.xamarin.com/show_bug.cgi?id=43099) - [watchOS][coop] Cannot enter GC safe region if the thread is not attached **(9.10.0.65+)**

* [32374](https://bugzilla.xamarin.com/show_bug.cgi?id=32374) - [System] Change WebRequest::BeginGetRequestStream driven IAsyncResult::CompletedSynchronously to match .net. **(9.10.0.67+)**
* [43356](https://bugzilla.xamarin.com/show_bug.cgi?id=43099) - [fsharp] Fix fsharp targets to detect 'F#' language **(9.10.0.67+)**

* [34513](https://bugzilla.xamarin.com/show_bug.cgi?id=34513) - [runtime] Take target type into account when caching delegates for blocks **(9.10.0.81+)**
* [43264](https://bugzilla.xamarin.com/show_bug.cgi?id=43264) - [msbuild] Always codesign iOS frameworks on simulator builds **(9.10.0.81+)**
* [43264](https://bugzilla.xamarin.com/show_bug.cgi?id=43264) - [msbuild] Always codesign *.dylibs, even for simulator builds **(9.10.0.81+)**
* [43357](https://bugzilla.xamarin.com/show_bug.cgi?id=43357) - [aot] WCSessionReplyHandler crashes WatchKit app **(9.10.0.81+)**
* [43408](https://bugzilla.xamarin.com/show_bug.cgi?id=43408) - [linker] Ensure we do not devirtualize methods that needs to be called from a base class to satisfy an interface **(9.10.0.81+)**
* [43489](https://bugzilla.xamarin.com/show_bug.cgi?id=43489) - [msbuild] Add the Insights API Key to the iOS archive manifest **(9.10.0.81+)**

* [41554](https://bugzilla.xamarin.com/show_bug.cgi?id=41554) - [watchos][debugger] The debugger does not connect to watch devices **(9.10.0.99+)**
* [41723](https://bugzilla.xamarin.com/show_bug.cgi?id=41723) - [bcl] Fix Mono.Data.Sqlite fix on old iOS versions **(9.10.0.99+)**
* [41956](https://bugzilla.xamarin.com/show_bug.cgi?id=41556) - [watchos][llvm] Type.GetType () call to a tail call optimization issue **(9.10.0.99+)**
* [41961](https://bugzilla.xamarin.com/show_bug.cgi?id=41961) - [watchos][llvm] Exceptions in Delegate.BeginInvoke callbacks are not handled on the threadpool thread **(9.10.0.99+)**
* [43999](https://bugzilla.xamarin.com/show_bug.cgi?id=43999) - [profiler] Unable to start profiling **(9.10.0.99+)**
* [43582](https://bugzilla.xamarin.com/show_bug.cgi?id=43582) - [coremidi] MidiEndpoint throws, bad dispose of GCHandle **(9.10.0.99+)**

