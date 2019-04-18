---
id: E14D3476-3A69-6167-BDBD-C1C591BD9062
title: "MonoTouch 4.1.1.1"
---

MonoTouch 4.1.1.1 is part of our Beta Series that will lead up to MonoTouch
4.2.

As any other beta updates, you can install it by selecting the Beta channel
on MonoDevelop and installing your MonoTouch package.

 <a name="New_since_4.1.0" class="injected"></a>


# New since 4.1.0

-  Improves startup performance (we no longer probe the file system for assemblies that we ship with) 
-  iOS Proxy support: we now pick the system proxy settings and use those in .NET APIs. The new CFProxy type can be used to get to all the details. 
-  Added AVMutableComposition
-  New strongly typed UIGraphics.BeginPDFContext method.
-  New MKCoordinate.FromMapRect API
-  Improved mtouch diagnostic messages when deploying apps to the device


 <a name="Fixes_since_4.1.0" class="injected"></a>


# Fixes since 4.1.0

-  Fixes Application Output: Standard output and standard error are once again working. 
-  Works with the latest XCode beta release (xamarin bug #346)
-  If you are using our XCode4 support with MonoDevelop 2.8, fixes on device deployment
