---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin.Mac 2.0"
---

# Xamarin.Mac 2.0.2.84 - Xamarin.Mac 2.0.2.111

Add support for running Xamarin.Mac applications on 10.11 (Fixes TLS offset hangs). Developing on 10.11 machines will be addressed in a future release.

Fixes multiple issues with the new Xamarin.Mac 4.5 Framework, including errors loading System.ServiceModel and other related assemblies.

Fixes issue where with newest Xcode Xamarin.Mac builds can error out with "do not support target device type "iphone".

# Xamarin.Mac 2.0.2.17 - Xamarin.Mac 2.0.2.35

Fixed a build issue that caused the "missing Info.plist" errors.

29801 - Fixed an issue causing "Unable to cast object of type X to type Y" at runtime for some cases.

# Xamarin.Mac 2.0.1.64 - Xamarin.Mac 2.0.1.56 

Fixed issue where 64-bit Xamarin.Mac.dll would be incorrectly copied into application bundle. Bug 29447

Fixed codesigning issue: "Error executing task CompileEntitlements: Required property 'ProvisioningProfile' not set"

Fixed issue preventing native debugger use on Xamarin.Mac application with non-trial license.

# Xamarin.Mac 2.0.0.0 

Xamarin.Mac 2.0 promotes the Unified API to the same API stability 
	as Classic and introduces a new framework you can target your Unified 
	projects against.

Explore our [Roadmap](/releases/mac/roadmap) to
	learn where Xamarin.Mac is headed.

### Highlights

-  Xamarin.Mac Unified has graduated to the same API stability level as Classic.
-  The new "Xamarin.Mac .NET 4.5 Framework" allows Unified projects to consume "desktop" targetted assemblies while targetting a supported subset of the .NET class library.


 ![](images/XM45Dialog.png)

-  A major focus has been fixing reported issues in our backlog. This focus will continue in the next release.
-  (Unified only) Support for C# events that expose Delegate "events" has been improved. This will allow events from both a base class and a derived class to subscribed to at the same time successfully now and conflicts to be better detected. This detection can be disabled by setting NSApplication.CheckForEventAndDelegateMismatches to false.
-  Improved support for native references in Xamarin.Mac projects. 
-  Xamarin.Mac F# unified build support and templates have been improved. This is considered preview quality for this release.
-  Unified projects now are always build with SGen and New Ref Count options enabled. The project options have thus been removed.
-  Due to the move to a unified runtime with Xamarin.iOS (in 1.12), we've improved validation on exported selectors. Incorrect selectors, such as ones with a missing/extra ':' may need to be manually fixed in source code and associated nib files. 
-  OS X 10.6 is no longer a supported / tested version to target with Xamarin.Mac. 


#### New Framework APIs

-  QuickLook UI
-  VideoToolbox


### Important Notes

The new "Xamarin.Mac 4.5 Framework" that Unified targets can target currently does not ship an OpenTK assembly. This will be added in future releases.

After migrating to Unified, you may the following error "Version mismatch between the native Xamarin.Mac runtime and XamMac.dll. Please reinstall Xamarin.Mac" until you clean the project in question. This will be automated in future releases.

In some cases, native debuggers may have trouble attaching to Xamarin.Mac 2.0 applications. This will be fixed in a future release. Please contact support if this is a blocking issue for you.

In a few cases API has been broken where it has made most sense and
		when the existing incorrect API could not have been marked as obsolete.
		When rebuilding with Xamarin.Mac 2.0, many of these cases should not
		even surface, but in cases that do, the changes that need to be made
		should be obvious with a more desirable end result. Some notable
		breaking changes:

-  `NSAlert` and  `NSAnimations` 's Delegate property is now not virtual as it wraps a newly exposed WeakDelegate.
-  `NSObjectController.NewObject` now correctly returns an  `NSObject` .


### Bug Fixes

-  5849 - NSFileManager.GetMountedVolume() falsely requires an NSArray instead of string[]
-  7770 - InvalidProgramException when using GenericObject <t> to derive from NSView</t>
-  8550 - Struct marshaling results in EXC_BAD_ACCESS crash
-  8679 - NSTableView fails to render when subscribing to events that internally assign Delegate
-  10204 - NSTextView dodgy delegate situation
-  12467 - NSTableView.SelectionDidChange problem
-  12543 - NSObject.Invoke ends up crashing the app
-  12763 - View property of NSStatusItem instance doesn't accept NULL
-  16505 - linker drops NSPrintPreviewGraphicsContext, causing a crash
-  16514 - Property setter for NSMenuItem.Submenu does not allow null values to be assigned
-  17483 - Add binding for applicationUsername property for SKPayment
-  18454 - Can't add an event handler to a button after removing an event handler from that button
-  20668 - NSOutlineView SelectionDidChange does not work
-  21238 - NewItemForRepresentedObject items on NSCollectionView aren't kept in memory, if GC'ed crashes can happen on scrolling \ API change
-  21530 - CABasicAnimation From/To isn't necessarily an NSObject
-  21554 - [Core Animation] - It seems that the CalculationMode property is ignored
-  22015 - Some NSKey uses wrong constant
-  22045 - The event for change on a combobox does not trigger
-  22478 - [NSColor] - Throws thread assertion but equivalent obj-c from apple sample works fine
-  22554 - SceneKit.SCNGeometry.FromSources() should return SCNGeometry not NSObject
-  22555 - CALayer property AutoresizinMask should be AutoresizingMask
-  22590 - NSTextStorage missing base class constructor
-  24058 - NSControl.Activated event delegate is only accepting one event handle
-  24144 - NSView does not implement NSAppearanceCustomization protocol
-  24176 - NSWindow does not implement NSAppearanceCustomization protocol
-  24344 - List <t>.IndexOf seems to have an issue or different behavior on Mac</t>
-  24451 - NSIndexSet construtor is missing nint as parameter
-  24545 - Unified launcher does not launch when assembly name != bundle name
-  24665 - We need to override copyWithZone: for INSCopying classes
-  24707 - [Xamarin.Mac]Unified mac samples gives build error when Xcode.app is named different
-  25438 - NSString.FromData incorrect behaviour
-  25620 - NSArrayController.NewObject throws InvalidCastException
-  25660 - Missing SecStatusCode value
-  25725 - No F# Unified Template
-  25873 - Unified API NSWindow Adding a WillClose Event Causes Resizing to Fail
-  26059 - Getting build error with latest ReactiveUI package
-  26076 - NSEventPhase enum missing MayBegin value
-  26414 - XM should not set DYLD_FALLBACK_LIBRARY_PATH
-  26419 - MapKit not working on OS X
-  26928 - [Missing API] NSModalResponse OK and Cancel are missing
-  26941 - BeginDraggingSource third parameter should be INSDraggingSource instead of NSDraggingSource
-  28058 - Xam.Mac QTRecorder throws exception on changing/Selecting 'Video Preview' under 'Recording Options'
-  28219 - CIImage: ImageWithTexture method can get null colorspace
-  28294 - Bug when overridding NSView.SetFrameSize
-  28336 - GetCompletions crash on 64-bit Unified only
-  28377 - System.Guid.NewGuid fails on OS X 10.6 (We dropped 10.6 support after this commit had landed


### API Changes

-  Classic API:  [1.12.0 to 2.0.0](/releases/mac/api_changes/from_1.12.0_to_2.0.0)
-  Unified API:  [1.12.0 to 2.0.0](/releases/mac/api_changes/from_1.12.0_to_2.0.0_unified)


## Community

 [Connect with other Xamarin.Mac](http://forums.xamarin.com/categories/mac) users on our forums.

Join us at our [Live Chat](http://chat.xamarin.com) for live support and discussions.
