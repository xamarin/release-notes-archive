---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 1.11"
---

# Xamarin.Mac 1.11.3.0 

1.11.3.0 is another preview release of the upcoming runtime unification, tracking changes as we stabilize towards a release.

-  Fix issue preventing creation of unified full profile Xamarin.Mac application in Xamarin Studio
-  Fix NSCell issue (Bug 24665).


# Xamarin.Mac 1.11.1.201 

1.11.1.201 is another preview release of the upcoming runtime unification, tracking changes as we stabilize towards a release. It contains bugs fixes and internal improvements.

-  In Unified builds, AppDelegate.FinishedLaunching (Foundation.NSObject) has been removed in favor of its more strongly typed AppDelegate.DidFinishLaunching (NSNotification notification)
-  New projects created with Xamarin Studio 5.7 will have the correct code, but existing Unified projects and projects created in previous versions will need to be updated.


# Xamarin.Mac 1.11.1.89 

1.11.1.89 is a preview release of the upcoming runtime unification. It also provides additional APIs.

-  Runtime unification gives us the same runtime powering our Mac and iOS products. This will bring bug fixes and performance work done on iOS to OS X and enable many of the features that were pioneered in iOS to come to the Mac platform. 
-  This brings the  [new refcount](http://developer.xamarin.com/guides/ios/advanced_topics/newrefcount/) to Xamarin.Mac.
-  Check “Use the reference counting extension” in the project settings with Xamarin Studio 5.7 or pass --new-refcount as an additional mmp argument to try it out.


#### New Framework APIs

-  Accounts
-  GameController
-  EventKit
-  MapKit
-  MediaAccessibility


# Xamarin.Mac 1.11.1.3 

1.11.1.3 continues our tracking of the Yosemite APIs and provides additional APIs.

-  Added initial code signing support to unified projects.
-  Pulled in a number of bug fixes from the stable and beta releases. 
-  Fixed a libgdiplus+ regression that comes with mono 3.10.0.28. Xamarin Bug 23553.


# Xamarin.Mac 1.11.0 



The Xamarin.Mac 1.11.x series is based on
	our latest release (1.10) and introduces support for the new APIs in
	Apple's Yosemite OS X.The 1.11.xx series is designed to rapidly track the changes
	on Apple's OS X 10.10 betas and have the same limitations and
	API guarantees that a standard Apple OS X beta has. APIs will
	change and will be updated continuously as the beta process
	moves.

### Highlights



This release not only brings new APIs introduced with
	Yosemite, but like its 1.10 peer, it introduces support for
	Xamarin's new 32 and 64
	bit [Unified APIs](/guides/cross-platform/macios/unified)

.#### Important Notes

Apple Xcode 6 beta requires Mac OSX 10.9.3+ (Mavericks) or
	10.10 (Yosemite). OSX 10.8 (Mountain Lion) is not supported.
	Apple releases notes contains a list of changes and pending
	issues for both OS X 10.10 and Xcode 6 that you should
	review.

#### New Framework APIs

New 64-bit only framework APIs (only available to [unified projects](/guides/cross-platform/macios/unified))

-  JavaScriptCore
-  GLKit
-  SpriteKit


New 32 and 64-bit framework APIs (only available to unified projects)

-  CloudKit
-  LocalAuthentication


### Known Issues 

-  SpriteKit currently does not work. This will be fixed in a future update. 


### API Changes



You can see the changes from:-  Classic API:  [Our Stable Release to the Yosemite Preview Release](/releases/mac/api_changes/from_1.10.0_to_1.11.0) (1.10.0 to 1.11.0)  
-  Unified API:  [Our Stable Release to the Yosemite Preview Release](/releases/mac/api_changes/from_1.10.0_to_1.11.0_unified) (1.10.0 to 1.11.0


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
