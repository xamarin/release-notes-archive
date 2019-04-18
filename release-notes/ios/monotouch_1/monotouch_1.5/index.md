---
id: EFD9B136-E3AD-95BE-FC32-C10E0AC75529
title: "MonoTouch 1.5"
---

&nbsp;

 <a name="New_features_in_this_release:" class="injected"></a>


# New features in this release:

-   Profiling is now supported. You can now profile your MonoTouch applications using Shark and Instruments. For details see  [http://monotouch.net/Documentation/Profiling](http://monotouch.net/Documentation/Profiling)

 


 <a name="API_Additions:" class="injected"></a>


# API Additions:

-  UIImagePickerController.AvailableMediaTypes


-  Added NSData.AsStream


-  Removed NSUrlAuthenticationChallengeSender


-   Added NSUrlAuthenticationChallengeSender protocol to NSUrlConnection

 
-   NSString methods to measure strings with a UIFont.

 
-  Added DataDetectorTypes property to UITextView




 <a name="Size_reductions:" class="injected"></a>


# Size reductions:

-  Smaller executables: -   Small executables 250k to 500k 
-   Some users are reporting 1.3 meg savings


 
-  Reduced the size of libmono.a in every application.
-  Greatly improved the linker result when linking monotouch.dll
-  Reduced memory usage for every type.


 <a name="Performance:" class="injected"></a>


# Performance:

-  Reduced the time it takes to start the runtime by 10-15%.
-  Reduced the time it takes to build simulator builds when not linking significantly. 
-  Reduced the time project builds take by 3-5 seconds.
-  Multiple other optimizations thru the entire engine.


 <a name="Fixes:" class="injected"></a>


# Fixes:

-  Fixed #573750: Running on device with the registrar and external bindings causes a crash 
-  Fixed #577754: UIVideoEditorController should inherit from UIViewController 
-  Fixed #579844 - Fixed crash using UIVideo.IsCompatibleWithSavedPhotosAlbum 
-  Fixed #564301 - CALayerDelegate locks up the simulator
-  Fixed #579997 - NSHTTPCookie.Name is missing
-  Fixed #574235 - Various values not accepting null
-  Fixed #579292 - Mono.Data.Sqlite crashes when using DataAdapters
-  Fixed #578150 - Add binding for NSProcessInfo
-  Fixed #555952 - Mono.Data.Sqlite doesn't work on leopard
-  Fixed #580277 - UISearchDisplayController should accept a UITableViewSource 
-  Fixed #562052 - UITableViewSource does not inherit from UIScrollViewDelegate 
-  Fixed #579373 - Can't set FillMode property on CAAnimation
-  Fixed #553783 - Full-AOT issues with DateTime / TimeSpan / Guid
-  Fixed #558604 - CultureInfo.CurrentCulture does not return the correct culture of the device 
-  Fixed #581666 - Crash with UIAlertView in latest beta 1.4.100
-  Fixed #560243 - Application crashes on device when compiled with MonoTouch 1.3.1.4429 
-  Fixed #579899 - mtouch error when inheriting from a ViewCOntroller in a library 
-  Fixed #553637 - Breakpoints cause app to crash while running in simulator for active OpenGL apps 
-   Fixed #584278 - Crash in Video Media Player Example

 
-  Fixed #548988 - Cannot bind Web Service Type from return XML on Monotouch 
-  Fixed #584888 - Linked away error in Stream.Read
-  Fixed regression in btouch leading to uncompilable bindings
-  Fixed crash using UISaveVideoAtPathToSavedPhotosAlbum
-  Fixed crash trying to use the simulator on Leopard
-  Fixed ArgumentException thrown by ABPerson.Get*() if the native data is null 
-  Fixed need to use ServicePointManager.ServerCertificateValidationCallback to access HTTPS sites. 
-  Fixed a linker issue with XmlArrayItemAttribute on fields with -linksdkonly 
-  Fixed case where the linker was improperly removing attributes from SOAP requests in some cases 
-  Fixed the AVAudioPlayer.FromData methods to be static.
-  Fixed crash disposing UIWebView from the wrong thread.
-  Fixed a possible leak when assigning user types to certain properties
-  Fixes a registrar bug improperly registering methods
-  Fixed the case where UIBarButtonItem managed proxy could be leaked cause callbacks to fail
