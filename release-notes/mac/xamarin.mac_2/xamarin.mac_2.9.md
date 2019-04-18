---
id: 7D673027-48FF-4C06-80FD-7716C4E185DE
title: "Xamarin.Mac 2.9"
---

version:2.8.0
releasedate:2016-03-31

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

- NSAccessibility - NSAccessibility related protocols have been bound and existiting classes such as NSApplication and NSButton now expose them
- System.Runtime.Remoting has been added to the XM 4.5 target framework BCL

### Releases

- 2.9.0.719

Preview released at Evolve 2016

### API diff

Will be published at a later date.

