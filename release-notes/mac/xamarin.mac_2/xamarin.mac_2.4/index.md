---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 2.4"
---

# Xamarin.Mac 2.4

<div class="note">
	<p>See the important license changes found in <a href="#XM242">2.4.2</a> related with Visual Studio Community Edition support.</p>
</div>

The Xamarin.Mac 2.4 series is a continuation of the 2.3.x series of releases. It includes all of the releases of Cycle 6. It also includes a large number of new 10.11 APIs bindings.

The Xamarin.Mac 2.4 series upgrades the Mono stack from
	the Mono 4.0.xx
	series to the [Mono 4.2.xx](http://www.mono-project.com/docs/about-mono/releases/4.2.0/) series.   One of the major themes in
	Mono 4.2.xx series is the continued adoption of Microsoft's
	open sourced .NET code to improve the conformance, speed and
	memory usage of our stack.

Please note the API break on NSOutlineView noted in the Important Notes section.

### Highlights

El Capitan support for running and building applications.



 Major improvements in our new project wizard and templates for Xamarin.Mac. We now have Storyboard support and Unified NSDocument based applications. See the Xamarin Studio release notes for additional details.

Improved OpenTK support under Unified Xamarin.Mac 4.5 profile. See caveat in Important Notes for a workaround in adding the actual reference.

Improvements in our binding and testing technology tracked down and fixed a significant number of ArgumentSemetics issues in our binding that could cause crashes.

Some new 10.10 APIs have bindings.

#### New Framework APIs

-  Contacts 
-  CoreAudioKit 
-  GameplayKit 
-  Metal 
-  MetalKit 
-  ModelIO 
-  SearchKit 


### Important Notes

Improvements in our registrar found a serious issue with NSOutlineViewDelegate ( [35356](https://bugzilla.xamarin.com/show_bug.cgi?id=35356)) that unfortuntly required an API break to fix. Any overrides of NSOutlineViewDelegate.ViewForTableColumn will need to be changed to NSOutlineViewDelegate.GetView.

Due to [35017](https://bugzilla.xamarin.com/show_bug.cgi?id=35017) a handful of new APIs will crash with "System.ExecutionEngineException: SIGILL" when used. If you run into this, add --registrar=static to your additional mmp arguments to work around until fixed in Serivce Release 1.

Due to [30682](https://bugzilla.xamarin.com/show_bug.cgi?id=30682) OpenTK.dll won't correctly show up in the reference list in Xamarin.Studio. You can browse to /Library/Frameworks/Xamarin.Mac.framework/Versions/Current/lib/mono/4.5/OpenTK.dll to add the reference for Unified projects targetting XM 4.5.

The new project template for Xamarin.Mac applications targetting 10.10 and later is storyboard based, however not all documentation has been updated yet. You can target 10.9 and before to get the older xib template.

The Xamarin.Mac F# templates on OS X 10.11 are broken due to [35851](https://bugzilla.xamarin.com/show_bug.cgi?id=35851). A set of possible work arounds can be found [here](https://forums.xamarin.com/discussion/comment/164827/#Comment_164827).

There have been a few additional minor API breaks to fix issues unfixable in other ways:

-  NSPasteboard CanReadObjectForClasses and ReadObjectsForClasses prototype was changed to be usable.
-  Many GetCompletions methods on AppKit classes have had their prototype changed to allow setting the index.
-  A few classes (NSUrlSessionUploadTask, GKAchievementViewController, GKLeaderboardViewController) had their base type changed to better reflect reality.
-  A number of CoreImage filters had breaking changes to fix major binding errors.


### API Changes

-  Classic API:  [2.0.0 to 2.4.0](/releases/mac/api_changes/from_2.0.0_to_2.4.0)
-  Unified API:  [2.0.0 to 2.4.0](/releases/mac/api_changes/from_2.0.0_to_2.4.0_unified)


## Releases

 <a name="XM242"></a>


### Xamarin.Mac 2.4.2

This service release adds support for *Visual Studio Community Edition*

Also *all* editions may now make use of these features which were previously restricted:

-  Command-line builds, including headless builds
-  All types and assemblies may now be used, including `System.Data.SqlClient`
-  P/Invoke
-  No more application size limits


Finally it removes the splash screen which was shown at launch for applications built with the *Trial* edition.

### Xamarin.Mac 2.4.1.7

2.4.1.7 is a bugfix release.

### Bug fixes

-  System.Configuration.ConfigurationErrorsException: Failed to load configuration section for dataContractSerializer when using ChannelFactory with the Xamarin.Mac .NET 4.5 Framework [ [#36401](https://bugzilla.xamarin.com/show_bug.cgi?id=36401) ]


### Xamarin.Mac 2.4.2.3

XM 2.4.2.3 is a compatibility release aligning with the rest of the Xamarin Platform for the new set of Stable builds. No XM specific fixes have been included as part of this release.

### Xamarin.Mac 2.4.1.6

2.4.1.6 is a bugfix release, fixing a number of reported issues, including regressions related to F# support with Xamarin.Mac.

### Bug fixes

-  Mono cannot marshal a parameter that is a function pointer which takes a function pointer as a parameter [ [#35545](https://bugzilla.xamarin.com/show_bug.cgi?id=35545) ]
-  F# with Xamarin.Mac Broken on 10.11 [ [#35851](https://bugzilla.xamarin.com/show_bug.cgi?id=35851) ]


### Xamarin.Mac 2.4.0.112

2.4.0.112 is a bugfix release, fixing a number of reported issues. Issues related to F# will be fixed before this release arrives on stable.

### Bug fixes

-  [XI/XM] Bug 34633 - Broken CGDataProvider causes crashes [ [#34633](https://bugzilla.xamarin.com/show_bug.cgi?id=34633) ]
-  MonoMac.Registrar.SharedStatic.IsNativeObject NotSupportedException at Mono.Cecil.TypeReference.Resolve [ [#34609](https://bugzilla.xamarin.com/show_bug.cgi?id=34609) ]
-  ObjCRuntime.Runtime.GetNSObject <t> returns wrong object in [MonoPInvokeCallback]-attributed method on 64-bit devices when "Enable device-specific builds" is unchecked [<a href="https://bugzilla.xamarin.com/show_bug.cgi?id=36317">#36317</a>]</t>
-  Build error with static registrar when exporting function/property that returns a Selector [ [#34440](https://bugzilla.xamarin.com/show_bug.cgi?id=34440) ]


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
