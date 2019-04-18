---
id: 87F10978-4CE6-C66E-DE0F-10027AE3F39D
title: "MonoTouch 1.4.99"
---

&nbsp;

This is a beta for MonoTouch 1.5.

 <a name="Fixes:" class="injected"></a>


# Fixes:

-  Bug #573750: Running on device with the registrar and external bindings causes a crash 
-  Bug #577754: UIVideoEditorController should inherit from UIViewController 
-  Fixed case where the linker was improperly removing attributes from SOAP requests in some cases 
-  Fixed the AVAudioPlayer.FromData methods to be static.
-  Fixed crash disposing UIWebView from the wrong thread.
-  Fixed a possible leak when assigning user types to certain properties


 <a name="" class="injected"></a>


#    
   
API Additions:

-  UIImagePickerController.AvailableMediaTypes
-  Added NSData.AsStream
-  Removed NSUrlAuthenticationChallengeSender
-  Added NSUrlAuthenticationChallengeSender protocol to NSUrlConnection
-  NSString methods to measure strings with a UIFont.   
    



 <a name="Size_reductions:" class="injected"></a>


# Size reductions:

-  Smaller executables: -   Small executables 250k to 500k 
-   Some users are reporting 1.3 meg savings


 
-  Reduced the size of libmono.a in every application.
-  Greatly improved the linker result when linking monotouch.dll
-  Reduced memory usage for every type.
