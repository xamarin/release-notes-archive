---
id: 77259859-F920-4E15-9421-E0ED79F54AD3
title: "Xamarin.iOS 9"
brief: "Xamarin's support for the iOS 9 Releases"
---

# Xamarin.iOS 9.0

The Xamarin.iOS 9.0.x series introduces support for Apple's iOS 9.0
	APIs and Xcode 7. It is based on the stable Mono 4.0 release.

## Important Notes

You will need to use Mac OSX 10.10.4 (Yosemite) to run this new 
	version of Xamarin.iOS along with Xcode 7. Until El Capitan is out of 
	preview we advise you to use Yosemite for your stable development
	environment.

Apple releases notes contains a list of changes and pending issues
	for both [iOS 9](https://developer.apple.com/library/prerelease/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS9.html#//apple_ref/doc/uid/TP40016198-SW1)
	and [Xcode 7](https://developer.apple.com/library/prerelease/ios/releasenotes/DeveloperTools/RN-Xcode/Chapters/xc7_release_notes.html#//apple_ref/doc/uid/TP40001051-CH5-DontLinkElementID_127)
	that you should review.

## New Features

### New iOS frameworks



Apple added several new frameworks in iOS 9, including:-  Contacts
-  ContactsUI
-  CoreSpotlight
-  GameplayKit
-  MetalPerformanceShaders
-  MetalKit
-  ModelIO
-  ReplayKit
-  WatchConnectivity


and Xamarin.iOS 9 includes bindings for all of them.

### Generic-based NS* collections



New API that uses (as parameters or return values) collections
	where the types are known are now bound to generic collection like:-  `NSSet<T>` , 
-  `NSMutableSet<T>` , 
-  `NSDictionary<TKey,TValue>` , 
-  `NSMutableDictionary<TKey,TValue>` 
-  `NSMutableArray<T>` 


### Support for Embedded Frameworks



It is now possible to use [Embedded Frameworks](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/ExtensionScenarios.html)


	in Xamarin.iOS projects. This is Apple's way of packaging shared
	libraries, they are useful for sharing native code between multiple
	components of your app (your main application and your extensions) or
	to easily add third party frameworks to an app [1].

There are several ways of including embedded frameworks in your app:-  Pass  `--framework /path/to/my.framework` as an  **Additional mtouch argument** .
-  In a future release of Xamarin Studio and Visual Studio it will be possible to add frameworks to the project using the UI; in the meantime project files can be edited manually to add the required sections. Examples can be found in the  [embedded-frameworks github repository](https://github.com/xamarin/embedded-frameworks) .
-  Frameworks can also be added to binding projects, although this also requires manual editing of project files (once again there are examples in the embedded-frameworks github repository).


Embedded frameworks **only work on iOS 8.0 and higher**.



Xamarin.iOS takes advantage of this to automatically bundle the Mono
	runtime as a framework when it detects it will be beneficial (this
	typically happens when using extensions, since otherwise the Mono runtime
	would be bundled once for the containing app and once for each extension).

This behavior can be controlled with the `--mono=`

 command 
	line option to mtouch, you can select `--mono=static`

 to force
	static linking or `--mono=framework`

 to force the use of a
	shared `Mono.framework`

 in your project. You’ll have to add the
	same option to the containing project and all extension projects, otherwise
	it’s possible to end up with an app where the extensions think there’s a `Mono.framework`

 in the app, but the containing app doesn’t
	bundle it because it’s statically linked.

More examples showing how this can be used for linking with native 
	frameworks and invoking manually, using it for C# bindings to Objective-C
	APIs and how this is used with many extensions can be found in [embedded-frameworks github repository](https://github.com/xamarin/embedded-frameworks)

.[1] While frameworks are convenient units of deployment, they are not
	processed by the native linker, so if you are merely using a limited set
	of features from a framework, you won’t get the size benefits that come
	from statically linking (which would only include the pieces of the static
	library that is actually used by the app).

## Improvements

### Simulator Launch Time Improvements



We’ve significantly improved the startup time in the simulator
	for certain scenarios by shipping all the Objective-C metadata in
	Xamarin.iOS.dll in a preprocessed form. This avoids having to process
	any metadata from Xamarin.iOS.dll at startup, and typically saves
	1-2 seconds.### Better nullability support



Our class libraries takes advantage of Apple’s addition of
	nullability information in their header files. The presence (or 
	absence) of null checks is now based on this information.
	Previously this was based on Apple's documentation, which was not
	always up to date.## Known Issues

### Breaking changes



Apple introduced a few breaking changes in the iOS9 SDK that you
	should be aware of:-  Changes in EventKit[UI] enum base types, now  `NSInteger` . Different sizes are now used in 32/64 bits [rdar://21375616]
-  Some  `EKError` enum values were re-numbered [rdar://22133323]


 <a name="2"></a>


##  [Xamarin.iOS 9.0.1.29](#2)



This is a service release fixing the following issues:### Bug fixes

-  [msbuild] Reduce XcodeCompilerToolTask verbosity [ [#33706](https://bugzilla.xamarin.com/show_bug.cgi?id=33706) ]
-  [registrar] Fix blocks registration [ [#34052](https://bugzilla.xamarin.com/show_bug.cgi?id=34052) ]
-  [runtime] Remove duplicated symbol in libmonotouch [ [#34186](https://bugzilla.xamarin.com/show_bug.cgi?id=34186) ]
-  [foundation] Remove INativeObject API in NS[Mutable]Dictionary [ [#34213](https://bugzilla.xamarin.com/show_bug.cgi?id=34213) ]
-  [replaykit] Fix StopRecording's handler signature [ [#34220](https://bugzilla.xamarin.com/show_bug.cgi?id=34220) ]
-  [registrar] Handle ref/out IntPtr in the registrars correctly [ [#34224](https://bugzilla.xamarin.com/show_bug.cgi?id=34224) ]
-  [fastdev] Ensure libraries we ship/produce for fastdev have deployment target 7.0 (or higher) [ [#34267](https://bugzilla.xamarin.com/show_bug.cgi?id=34267) ]


 <a name="1"></a>


##  [Xamarin.iOS 9.0.1](#1)



This is Xamarin's official release to support iOS9 SDK and, now that our
	audit and tests are completed, offers API stability with future release.
	Also our runtime was updated to our latest mono used in XI 8.10.5
	(Service Release 4).

The following document contains a complete list of the [API changes from 8.10.5 to 9.0.1](/releases/ios/api_changes/from_8.10.5_to_9.0.1)

.### Bug fixes

-  [cecil] Fix regression for async methods compiled with VS2013 [ [#33124](https://bugzilla.xamarin.com/show_bug.cgi?id=33124) ]  **9.0.1.20+**


 <a name="0"></a>


##  [Xamarin.iOS 9.0.0](#0)



This is a beta release based on Apple’s GM release of the Xcode7
	and iOS 9 SDK. We believe this to be complete and working but we’re
	still auditing the API and testing the changes in the latest bits.
	You can use this build to submit to the app store but it’s possible
	that the upcoming stable build might have some slight differences.

The following document contains a complete list of the [API changes from 8.10.3 to 9.0.0](/releases/ios/api_changes/from_8.10.3_to_9.0.0)

.
