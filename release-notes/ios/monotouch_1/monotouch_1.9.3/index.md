---
id: CAC4375C-1F48-08FE-4888-3585F56666C3
title: "MonoTouch 1.9.3"
---

&nbsp;

This is a bugfix release in our bet series as we prepare for 2.0

-  Fixed the case where UIBarButtonItem managed proxy could be leaked cause callbacks to fail 
-  Fixed issue with the new GC methodology where we only retained objects but not arrays in the object graph 
-  Fixed a crash using CGPDFDocument.GetPage ()
-  Fixed #579844 - Fixed crash using UIVideo.IsCompatibleWithSavedPhotosAlbum 
-  Fixed #564301 - CALayerDelegate locks up the simulator
-  Fixed #579997 - NSHTTPCookie.Name is missing
-  Fixed #574235 - Various values not accepting null
-  Fixed #579292 - Mono.Data.Sqlite crashes when using DataAdapters
-  Fixed #578150 - Add binding for NSProcessInfo
-  Fixed #555952 - Mono.Data.Sqlite doesn't work on snow leopard
-  Fixed #580277 - UISearchDisplayController should accept a UITableViewSource 
-  Fixed #562052 - UITableViewSource does not inherit from UIScrollViewDelegate 
-  Fixed #579373 - Can't set FillMode property on CAAnimation
-  Fixed #553783 - Full-AOT issues with DateTime / TimeSpan / Guid
-  Fixed #558604 - CultureInfo.CurrentCulture does not return the correct culture of the device 
-  Fixed #581666 - Crash with UIAlertView in latest beta 1.4.100
-  Fixed #560243 - Application crashes on device when compiled with MonoTouch 1.3.1.4429 
-  Fixed #579899 - mtouch error when inheriting from a ViewCOntroller in a library 
-   Fixed #553637 - Breakpoints cause app to crash while running in simulator for active OpenGL apps

 
-  Fixed a linker issue with XmlArrayItemAttribute on fields with -linksdkonly
