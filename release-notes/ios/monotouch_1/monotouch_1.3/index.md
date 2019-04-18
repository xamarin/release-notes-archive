---
id: 648B74BD-4A63-B61E-EC20-B80A9B5BE178
title: "MonoTouch 1.3"
---

This release is mostly a bug fix release, it contains fixes for the debugger
that was introduced in MonoTouch 1.2 and various smaller fixes.

 <a name="" class="injected"></a>


# New APIs [ <span class="icon"><img src="monotouch_1.3/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_1/MonoTouch_1.3#)

MonoTouch.Foundation.NSThread bindings for NSThread.

Common constants used by the UIImagePickerController are now included in the
class.

 <a name="Fixes" class="injected"></a>


# Fixes

-  Fixed bug #549941 - Step over breakpoint can deadlock debugger
-  Fixed bug #552263 - Typo in UISearchDisplayDelegate.ShouldReloadForSearchString 
-  Fixed bug #548168 - Added [NullAllowed] to UISearchBar and UITextView
-  Fixed bug #551498 - Crash when having a breakpoint at a invalid IL offset 
-  Fixed bug #551745 - Support https in WCF. Support OperationContext custom headers in WCF 
-  Fixed bug #553656 - The CAAnimation did not implement the CAMediaTiming interface, now it does 
-  Fixed bug #553888 - CABasicAnimation.BasicAnimation.FromKeyPath to return a CABasicAnimation 
-  Fixed MFMailComposeViewController.MailComposeDelegate to wrap WeakMailComposeDelegate instead of WeakDelegate 
-  Fixed GameKit.GKSession.Available selector typo
-  Fixed _NSGetEnviron() / exc_server private API usage: -   These APIs are used by Mono when running on OS X and were carried over to MonoTouch. It turns out that these are not recommended to be used by Apple on the iPhone so they have been replaced with the iPhone OS support variants.
