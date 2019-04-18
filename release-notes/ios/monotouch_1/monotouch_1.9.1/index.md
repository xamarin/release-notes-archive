---
id: 7D0EBFD4-1583-F20B-491B-195825D5E66B
title: "MonoTouch 1.9.1"
---

&nbsp;

This is an alpha preview for MonoTouch 2.0. It includes iPad APIs from the
earlier 1.9.0 preview.

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

-  Smaller executables (250k to 500k)
-  Reduced the size of libmono.a in every application.
-  Greatly improved the linker result when linking monotouch.dll
-  Reduced memory usage for every type.
