---
id: 9EF43202-B3EA-7C4D-6731-F0C2F7B4D4C0
title: "MonoTouch 5.0"
---

MonoTouch 5.0 introduces support for the new APIs and features found on iOS
5.

We have prepared an [Introduction to MonoTouch 5.0 and the iOS5 bindings](/guides/ios/application_fundamentals/introduction_to_ios_5) to get
developers started with the new features in iOS 5.0 and how they can take
advantage of those with MonoTouch 5.0. In the coming days we will be blogging
specific features of MonoTouch and creating new documents that cover a
particular technology in detail.

If you are interested in the new API surface, check our:

-  API changes page that documents the changes between MonoTouch 4.2 and MonoTouch 5.0. Or you can check directly our  [online API documentation](http://docs.go-mono.com/index.aspx?link=root:/MonoTouch-lib) for MonoTouch 5.0. 
-  API changes from 5.0 to 5.0.1.


See our section on changes in 5.0.2 and 5.0.3

These are the new frameworks supported by MonoTouch 5.0 with strongly-typed
C# bindings:

-   **iCloud**   
    
 With iCloud you can access cloud storage to upload user files and automatically sync them, wirelessly, between other computers and devices. 


-   **Twitter Integration**   
    
 Take advantage of easy Twitter access, URL shortening, photo uploads, geolocation, and more, all with a simple and easy to use API. 


-   **AirPlay**   
    
 Stream audio, video and photos from iOS devices directly to an HDTV (via Apple TV) or take advantage of encrypted streams using HTTP Live Streaming. 


-   **Bluetooth**   
    
 Using the MonoTouch Bluetooth APIs you can easily access and communicate with external Bluetooth hardware devices and accessories. 


-   **Newsstand**   
    
 Use MonoTouch to interact with the new home screen folder Newsstand to publish and update magazines and newspaper subscriptions. Best of all, handle updates in the background without interrupting the user. 


-   **Core Image**   
    
 The new Core Image API allows access to many built-in features such as applying effects to photos and videos, auto-enhance, reduce red-eye, and facial recognition. 


And you get to enjoy all the new updates that Apple has done on iOS5 like
take advantage of Storyboards for building the workflow of your application,
support styling of your application using the new appearance framework and take
advantage of the new editing hooks in UIKit. Visit our MonoTouch Samples
repository to get started.

 <a name="MonoTouch_5.0.1" class="injected"></a>


# MonoTouch 5.0.1

MonoTouch 5.0.1 introduces the following new features:

-  Embedding of native libraries using the  [LinkWith attribute](/guides/ios/advanced_topics/binding_objective-c_types/binding_types_reference_guide#LinkWithAttribute) . 
-  Added AVFoundation extension methods for NSValue
-  Make it so users do not accidentally create empty NSError objects as those can crash applications 


The detailed API changes are documented in our 5.0 to 5.0.1 API changes
document.

These are the fixes introduced in 5.0.1:

-  Force Point[F], Size[F] and Rectangle[F] to use the properties setters so the linker won't eliminate them, e.g. xml serialization. Fix bug #1520 
-  Fix the binding for MKUserLocation. Fixes bug #1555
-  Fix the case where a ref/out parameter on an NSObject is set to null, fixes #1538 
-  Fix regression in iPhoneOSGameView.cs (bug #1497) caused by fix for bug #1366 
-  AVAssetReaderAudioMixOutput's ctor allows null audioSettings. Fixes bug #1552 
-  Fixed MapFromCGPdfObject() - enum values were shifted by 1
-  5.0.2 to 5.0.3 API changes document.


Added:

-  Support for iOS 5.0.1's skip file from being backed up to iCloud
-  Bring a monotonic Stopwatch to iOS. Fix #1366
-  Added new iOS5 AudioSession properties (Mode, OverrideCategoryDefaultToSpeaker, OverrideCategoryEnableBluetoothInput) 
-  Added NSFileWrapper APIs for iCloud package storage


Bug fixes:

-  Add missing constructors to MapKit
-  Fixes the bindings for ALAssetsLibrary.WriteImageToSavedPhotosAlbum (bug #2166). 
-  Registrar fixes for callback methods that use out or ref parameters
-  Fixes UIAppearance.WhenFoundIn API (bug #1978)
-  Fixes UIAppearance to work with subclasses
-  Fixes SQLite leak
-  Fixes iCloud callbacks
-  5.0.3 to 5.0.4 API changes document.


Added:

-  Added missing UISplitViewController method
-  Added convenience enumeration values for anchoring views
-  Added NSData. FromFile


Bug fixes:

-  Fix #2352 MKMapView with MKPinAnnotationView dragging crash
-  Fix #2336 Add MKOverlay and MKAnnotation support for MKPolygon
-  Fix #2318 Keep a reference to BarButtonItems
-  Fix missing setter for UISwitch.OnTintColor property
-  Fix #2310 Allow resetting the Mask for a CALayer
-  Fix #2059 which caused problems when adopting Objective-C protocols
-  Fix #1778 added missing constructors that take a RectangleF for ADBannerView, GLKView, MKCircleView, MKOverlayPathView, MKPolygonView, MKPolylineView, UIAlertView, UITableView, UITableViewCell, UIStepper 
-  Fix #1555 consistency of methods taking annotation arguments to take NSObjects. 
-  Fix #2190 prevent deadlock in SDB
-  Fixes #265 and #2059 crashes on simulator for some methods returning streets
