---
id: 596C31C1-8224-6CBF-5D94-A03A713289A0
title: "MonoTouch 3.2.2"
---

&nbsp;

 <a name="Major_Highlights_-_Runtime" class="injected"></a>


# Major Highlights - Runtime

-  Tracks the iOS 4.2 APIs, and supports
-  New stacks bound: -   Security stack (keychain, certificates, key signing) 
-   ImageIO
-   Preview only, subject to changes in the API: -    AudioUnit bindings, based on the work of ReinfoceLabs and Joe Matt 


  


 
-  Improved bindings for: -   AssetLibrary (completed)
-   AVAsset APIs in AVFoundation
-   CoreGraphics now has PDF bindings
-   CoreLocation now has C# style events
-   More C# style events for UIKit classes
-   KeyValue observing is now supported
-   NSObject now has KeyValue observing and Accessibility support
-   NSString now has Drawing methods (previously we hosted those on the contexts, similar to what you expect from Objective-C) 
-   MapKit hierarchy has been fixed: most high-level objects derive from MKAnnotation 


 
-  The AOT compiler now properly detects where GenericComparer&lt;T&gt; and GenericEqualityComparer&lt;T&gt; were required and emits the required code. This greatly improves LINQ support for OrderBy and other similar conditions. 
-  The  **btouch** generator properly supports marshalling delegates as blocks (previously it only worked with monotouch.dll provided delegates, but did not work for user-bound code). 
-  Completed support for AssetLibrary
-  Fixed a potential debugging on device regression with SDK 4.2


 <a name="Major_Highlights_-_MonoDevelop" class="injected"></a>


# Major Highlights - MonoDevelop

There are many [new features in MonoDevelop 2.4.1](http://monodevelop.com/Download/MonoDevelop_2.4.1_Released) the following are the new
features specific to MonoTouch:

-  Add "Zip Bundle" command, so you can simplify the process to upload your applications to the AppStore. 
-  Automatic compilation with the latest SDK if the required SDK is missing: -   If you upgrade your XCode and older iPhone SDKs are removed, MonoDevelop will automatically compile with the latest iPhone SDK. You will no longer need to upgrade your project files when you upgrade XCode manually. 
-   New "Default" SDK mode can be used to explicitly inform MonoDevelop to build with the latest, as opposed to producing a warning. 


 



See the [2.4.1 release notes](http://monodevelop.com/Download/MonoDevelop_2.4.1_Released)

 for details about other fixes and
improvements. <a name="Minor_Improvements" class="injected"></a>


# Minor Improvements

-  Debug builds now initialize the symbol tables, even if they are not being ran under the debugger, providing stack traces with line numbers. This consumes a little more memory as the debugging information is kept in memory. 
-  Added C# events to StoreKit
