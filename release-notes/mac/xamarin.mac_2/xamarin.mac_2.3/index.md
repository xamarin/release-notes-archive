---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 2.3"
---

# Xamarin.Mac 2.3

The Xamarin.Mac 2.3 series upgrades the Mono stack from
	the Mono 4.0.xx
	series to the [Mono 4.2.xx](http://www.mono-project.com/docs/about-mono/releases/4.2.0/) series.   One of the major themes in
	Mono 4.2.xx series is the continued adoption of Microsoft's
	open sourced .NET code to improve the conformance, speed and
	memory usage of our stack.

### Highlights

Preview El Capitan support for running and building applications. This is ongoing, as we track changes (some breaking) from Apple until release.



 Major improvements in our new project wizard and templates for Xamarin.Mac. We now have Storyboard support and Unified NSDocument based applications. See the Xamarin Studio release notes for additional details.

Improved OpenTK support under Unified Xamarin.Mac 4.5 profile and F#. See caveat in Important Notes for a workaround in adding the actual reference.

Improvements in our binding and testing technology tracked down and fixed a significant number of ArgumentSemetics issues in our binding that could cause crashes.

Improved F# support for Unified Xamarin.4.5 profile.

Some new 10.10 APIs have bindings.

#### New Framework APIs

SearchKit

### Important Notes

Due to [30682](https://bugzilla.xamarin.com/show_bug.cgi?id=30682) OpenTK.dll won't correctly show up in the reference list in Xamarin.Studio. You can browse to /Library/Frameworks/Xamarin.Mac.framework/Versions/Current/lib/mono/4.5/OpenTK.dll to add the reference.

The new project template for Xamarin.Mac applications targetting 10.10 and later is storyboard based, however not all documentation has been updated yet. You can target 10.9 and before to get the older xib template.

There have been a few stable API breaks to fix issues unfixable in other ways:

-  NSPasteboard CanReadObjectForClasses and ReadObjectsForClasses prototype was changed to be usable.
-  Many GetCompletions methods on AppKit classes have had their prototype changed to allow setting the index.
-  A few classes (NSUrlSessionUploadTask, GKAchievementViewController, GKLeaderboardViewController) had their base type changed to better reflect reality.


### API Changes

-  Classic API:  [2.0.0 to 2.3.0](/releases/mac/api_changes/from_2.0.0_to_2.3.0)
-  Unified API:  [2.0.0 to 2.3.0](/releases/mac/api_changes/from_2.0.0_to_2.3.0_unified)


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
