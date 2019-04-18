---
id: 7D673027-48FF-4C06-80FD-7716C4E185DE
title: "Xamarin.Mac 2.10"
---

version:2.10.0
releasedate:2016-09-08

<div class="note">
	**Classic Profile Deprecation:**
	As new features are added in Xamarin.Mac we are starting to gradually deprecate features from the classic profile (xammac.dll).
	In this release the non-NRC (new-ref-count) option was removed. NRC has always been enabled for all unified applications (i.e. non-NRC was never an option) and has no known issues.
</div>

Requirements
============

- The latest features and API requires Xcode 7.2 and the bundled macosx10.11 SDK;
- Apple Xcode 7.2 requires a Mac running OSX 10.10 (Yosemite) or 10.11 (El Capitan)

What's New
==========

Xamarin.Mac Extensions - Xamarin.Mac 2.10 brings preview support for building OS X extensions. 

The following extensions are currently supported:

- Finder
- Share
- Today

More information, including details on limitations and work arounds can be found [here](https://developer.xamarin.com/guides/mac/platform-features/extensions/).

In addition:

- NSAccessibility - NSAccessibility related protocols have been bound and existiting classes such as NSApplication and NSButton now expose them.
- System.Runtime.Remoting has been added to the XM 4.5 target framework BCL.

### Known Issues

Xamarin.Mac 2.10 does not have full support Xcode 8 when the static registrar is in use. This means projects with --registrar=static or Xamarin.Mac Extension projects must be built against Xcode 7.3 for now.

In macOS 10.12, Apple changed the implementation of NSLog in such a way that it will crash if p/invoked into from managed code. There is a tracking bug [here](https://bugzilla.xamarin.com/show_bug.cgi?id=44429) and two known work arounds:

- Use System.Console.WriteLine instead of NSLog directly
- Create a small C static library which invokes NSLog for you, link it into your application, and invoke it instead.

A bug report has been opened with Apple.

### Releases

- 2.10.0.110

Cycle 8 SR 1

Bug Fixes
=========

* [44378](https://bugzilla.xamarin.com/show_bug.cgi?id=44378) - Mac Migration Tool Not Working
* [44285](https://bugzilla.xamarin.com/show_bug.cgi?id=44285) - Xcode interface builder quits every time I open Xamarin studio
* [43579](https://bugzilla.xamarin.com/show_bug.cgi?id=43579) - Generator emits invalid code when using the same method name (overload) in @delegates using events and C# delegates


- 2.10.0.103 - 2.10.0.104

Cycle 8 SR 0 is a compatibility release aligning with the rest of the Xamarin Platform.

Bug Fixes
=========

* [42443](https://bugzilla.xamarin.com/show_bug.cgi?id=42443) - [AppleTLS] Fix hangs with some web sites when using macOS 10.12
* [44708](https://bugzilla.xamarin.com/show_bug.cgi?id=44708) - [System] ChainValidationHelper: ignore port number when validating a certificate's host name **(10.0.1.10+)**


- 2.10.0.99

Cycle 8 Initial release.

* [43890](https://bugzilla.xamarin.com/show_bug.cgi?id=43890) - [msbuild] Only include *.dylibs from the app bundle for codesigning (i.e. not from child PlugIns) 


- 2.10.0.81

Third beta release.

* [registrar] Adjust the static registrar to work with Xcode 8 (where QT headers were removed)
* [43364](https://bugzilla.xamarin.com/show_bug.cgi?id=43364) - [mmp] Fix native dependency processing when linker is disabled

- 2.10.0.68

XM 2.10.0.68 is a compatibility release aligning with the rest of the Xamarin Platform. No XM specific fixes have been included as part of this release.

- 2.10.0.65

Fixes:

- Disable (unsupported) linking requests in extension projects, as it currently will break execution.
- Add fobjc-runtime=macosx to 64-bit build clang invocations to improve static registrar support with newer SDKs.
- Improve bundled native framework support to set rpath to the bundle's Framework directory. This should prevent the need for manually adding in via additional mmp arguments in most cases now.
- Improve F# support for Xamarin.Mac.

- 2.10.0.33

Updated C8 preview with full preview extension support.

### API diff

The following documents contains a complete list of the API changes since our latest stable release: XM 2.8.2 (C7SR1)

* [macOS](/releases/mac/api_changes/mac_2.8.2_to_2.10.0);

