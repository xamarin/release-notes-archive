---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.iOS 10.0"
---

version: "10.0"
releasedate: 2016-09-07

<div class="note">
	<b>Classic Profile Deprecation:</b>
	This version of Xamarin.iOS does <b>not</b> support the classic profile (i.e. `monotouch.dll`).
	The last version supporting classic was Xamarin.iOS 9.10, which is nearly identical to 10.0,
	but does not include the new API added in Xcode 8 SDKs.
</div>

Requirements
============

- The latest features and API requires Xcode 8.0 **GM** and the bundled iOS, tvOS and watchOS SDKs;
- Apple Xcode 8.0 requires a Mac running OSX 10.11.5 (El Capitan) or newer;

What's New
==========

This release is based on our ([XI 9.10.x](/releases/ios/xamarin.ios_9/xamarin.ios_9.10.md))
work and, like our summer ([XI 9.99.x](/releases/ios/xamarin.ios_9/xamarin.ios_9.99.md)) previews, 
it includes the new API that Apple added in the latest SDK (iOS 10, tvOS 10 and watchOS 3) shipped with Xcode 8.

### iOS 10

The following new frameworks were added in iOS 10:

* CallKit
* Intents
* IntentsUI
* Message
* Speech
* UserNotification
* UserNotificationUI
* VideoSubscriberAccount

### tvOS 10

The following new frameworks were added in tvOS 10:

* ExternalAccessory
* HomeKit
* MultipeerConnectivity
* Photos
* PhotosUI
* ReplayKit
* UserNotification
* VideoSubscriberAccount

The above *new* frameworks for tvOS are new to the platform, but already exists (or were just added) in iOS. Several new API are also available in previously existing frameworks (see **API diff**).

### watchOS

[Xamarin.iOS 9.10](/releases/ios/xamarin.ios_9/xamarin.ios_9.10.md) introduced **preview** support for **native watchOS 2.x** applications running on both the simulator and devices. The version adds the new API added in watchOS 3.0. However this is still a **preview** and we appreciate your feedback and bug reports. Please report any issues on [bugzilla](https://bugzilla.xamarin.com/).

In Xamarin.iOS 10.0 the following new frameworks were added for watchOS 3:

* AVFoundation
* CloudKit
* CoreAudio
* GameKit
* SceneKit
* SpriteKit
* UserNotification

The above *new* frameworks for watchOS are new to the platform, but already exists (or were just added) in iOS. Several new API are also available in previously existing frameworks (see **API diff**).

Note that, as a preview, we are not committed to binary compatibility for future releases and, while nothing drastic is planned, a few things might change to accomodate the platform limits and restrictions (e.g. lack of socket support).


Other Notable Changes
=====================

* Some enum values were found to be incorrect and were fixed in this release. This include members of `AVError`, `NSEntityMappingType` and `UIContentSizeCategory`. You can see them in our API diff documents.

### Xamarin.iOS 10.0.2

This is a *beta* service release (SR1) for Xamarin.iOS 10.0. This is now superceded by XI 10.2.1.

Bug Fixes
=========

* [44701](https://bugzilla.xamarin.com/show_bug.cgi?id=44701) - [mtouch] Fix possible NRE when optimizing bindings
* [44349](https://bugzilla.xamarin.com/show_bug.cgi?id=44349) - [Mono.Data.Sqlite] Fails to store seconds in timestamp value to a table


### Xamarin.iOS 10.0.1

This is a service release (SR0) for Xamarin.iOS 10.0.

Bug Fixes
=========

* [44225](https://bugzilla.xamarin.com/show_bug.cgi?id=44225)[42796](https://bugzilla.xamarin.com/show_bug.cgi?id=42796)[43794](https://bugzilla.xamarin.com/show_bug.cgi?id=43794) - [monotls] Support for HTTPS server with virtual domains
* [42395](https://bugzilla.xamarin.com/show_bug.cgi?id=42395) - [llvm] build never finishes when enabling LLVM
* [44073](https://bugzilla.xamarin.com/show_bug.cgi?id=44073) - [videotoolbox] VTCompressionSession does not handle null sample buffer
* [44357](https://bugzilla.xamarin.com/show_bug.cgi?id=44357) - [msbuild] Do not require codesign certificate for iOS Simulator builds

* [44122](https://bugzilla.xamarin.com/show_bug.cgi?id=44122)[44518](https://bugzilla.xamarin.com/show_bug.cgi?id=44518)[44516](https://bugzilla.xamarin.com/show_bug.cgi?id=44516) - [mtouch] Fix MT2001 errors due to OoM condition **(10.0.1.7+)**
* [44666](https://bugzilla.xamarin.com/show_bug.cgi?id=44122) - [System] Send all data to a socket before exit from Socket.Send **(10.0.1.7+)**

* [42443](https://bugzilla.xamarin.com/show_bug.cgi?id=42443) - [AppleTLS] Fix hangs with some web sites when using iOS/tvOS 10.x **(10.0.1.9+)**
* [44708](https://bugzilla.xamarin.com/show_bug.cgi?id=44708) - [System] ChainValidationHelper: ignore port number when validating a certificate's host name **(10.0.1.10+)**

There is no public API changes in this release.


### Xamarin.iOS 10.0.0

The following documents contains a complete list of the API changes since our latest stable release: XI 9.8.2 (C7SR1)

* [iOS](/releases/ios/api_changes/ios_9.8.2_to_10.0.0);
* [tvOS](/releases/ios/api_changes/tvos_9.8.2_to_10.0.0);
* [watchOS](/releases/ios/api_changes/watchos_9.10.0_to_10.0.0)

Note: watchOS support was not part of the latest XI 9.8 (stable). The API diff is based on XI 9.10 which included preview support for watchOS 2.x API.

### Known Issues

* **Issue:** "Error MT0091: This version of Xamarin.iOS requires the iOS 10.0 SDK (shipped with Xcode 8.0) when the managed linker is disabled. Either upgrade Xcode, or enable the managed linker."  This message will appear when building using Xcode 7.3 or older with Xamarin.iOS 10.  The issue arises because Xamarin.iOS.dll includes API new in Xcode 8 and native compilation requires the corresponding header files.  When enabled, the Xamarin managed linker can help remove these symbols, if unused, to allow building successfully using older versions of Xcode.

    * **Workaround** Update to Xcode 8, or enable the Xamarin linker by choosing a setting other than _Don't link_ under _Project properties > iOS Build > Linker behavior_.

* **Issue:** watchOS 2+ does not offer direct access to sockets. Most of our managed network stack API won't work without them.
	* **Workaround** Use native API for networking or `HttpClient` with the `NSUrlSessionHandler`.

* **Issue:** Debugging on watchOS devices can be slow and unreliable
	* **Workaround** This [document](https://github.com/xamarin/xamarin-macios/wiki/Debugging-on-watchOS-device) provides some tips to help you.

* **Issue:** **watchOS glances** has been removed in watchOS 3.x / Xcode 8. Trying to start a watchOS application from the IDE, in glance mode, will show a blank screen.
	* **Workaround** None, Apple removed this feature. Future versions of our IDE will remove the feature as well.

* **Issue: App not optimized for iOS10** warning: This happens when a 32bit-only application executes on a 64 bits capable platform, e.g. a i386 build running on a iPhone6 simulator (capable of 64bit). The warning simply means you're not using the optimal build for the platform. This can be normal when testing and, by default, simulator builds are only 32 or 64 bits (to make them faster).
	* **Workaround** You can change your project settings to remove the warning. Application submitted to the app store should have both 32 and 64 bits, in general, or be 64 bits only.

* **Issue:** Applications re-compiled against the new iOS 10 SDK crash at startup. iOS 10 requires additional keys (in their Info.plist) to access some private resources (e.g. calendar, photos, music...). iOS will crash (by design) applications using the related API if those keys are missing. (The string "\_\_CRASHING\_DUE\_TO\_PRIVACY\_VIOLATION\_\_" can appear in the stack trace for the crash in these cases.)
	* **Workaround** Update your `Info.plist` with the required privacy keys. The required key (causing the crash) can be seen in the device logs.

* **Issue:** Different TLS handlers behave differently and some iOS changes can throw in different places leading to crashes [42443](https://bugzilla.xamarin.com/show_bug.cgi?id=42443) [43794](https://bugzilla.xamarin.com/show_bug.cgi?id=43794) [42796](https://bugzilla.xamarin.com/show_bug.cgi?id=42796)
	* **Workaround** Try a different handler (e.g. Mono vs Apple TLS) to see if this solves the issue.


### Downstream Issues

* **Issue:** Non-public UITest bug 1005 - **Xcode 8 removes the [UI Automation API](https://developer.apple.com/library/ios/documentation/DeveloperTools/Conceptual/InstrumentsUserGuide/UIAutomation.html)**, causing "SetUp : System.InvalidOperationException : Sequence contains no matching element ... at System.Linq.Enumerable.First[TSource] ... at Xamarin.UITest.iOS.Instruments.GetAutomationTemplatePath ()" when attempting to use UITest locally.

	* **Candidate fix** Update to the [Xamarin.UITest 2.0.0 Beta](https://www.nuget.org/packages/Xamarin.UITest/2.0.0-beta01) prerelease, which is based on [Calabash 0.20](https://github.com/calabash/calabash-ios/blob/4832650b6afb38c580d347d8504f5caf80702e7b/CHANGELOG.md) and includes a new API that uses XCUITest rather than UI Automation.

	* **Alternate temporary workaround** Keep using Xcode 7, or just keep Xcode 7 installed in the default location and unpack Xcode 8 side-by-side to a custom location.

* **Issue:** Mapbox SDK component version 4.1.1.0 causes device builds to fail with "Failed to compile the generated registrar code ... error: property with 'copy' attribute must be of object type". [44006](https://bugzilla.xamarin.com/show_bug.cgi?id=44006)
	* **Possible temporary workaround** Downgrade the Mapbox SDK component to version 4.1.0.0 or earlier.

### Upstream Issues (in Xcode)

* **Issue:** `SecKeyChain.Add()` returns -34018 on iOS 10 simulator unless an _Entitlements.plist_ has been added under _iOS Bundle Signing > Custom Entitlements_ for the _iPhoneSimulator_ configuration. See also <https://forums.developer.apple.com/thread/51071>. (Xamarin tracking bug with more details on how to add an _Entitlements.plist_: [44361](https://bugzilla.xamarin.com/show_bug.cgi?id=44361).)

* **Change:** The Today Extension widget renders at a different height when the extension is built using Xcode 8 as compared to Xcode 7. See <https://forums.developer.apple.com/thread/48930>.

