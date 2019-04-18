---
id: 8861242E-A1E3-5642-24E0-17E5FB7AD7F6
title: "MonoTouch 1.4.4"
---

**New APIs:**

-  Expose CGFont.CreateWithFontName (string name)


-  CGImage.ScreenImage () fixes 566901


-  NSDateFormatter, NSFormatter.


-  AudioSession bindings.


-  Audio Offline Render




 <a name="Improvements:" class="injected"></a>


# Improvements:

-  Strongly typed AudioBasicStreamDescription


-  MKMapView now has C# style events.


-   UIView.BackgroundColor can be assigned the null value

 
-  UIImageView.Image can be assigned a null value


-   Linker automatically detects more cases in which the crypto APIs are required (other Web API entry points).

 


 <a name="Fixes:" class="injected"></a>


# Fixes:

-   Fixed debugger deadlock caused when thread interrupted while holding the malloc/free lock

 
-   Fixed binding for UITabBarController.CustomizableViewControllers to deal with

 
-   UIViewControllers instead of UINavigationViewControllers, fixes bug reported by Manni.

 
-   Fixed #562094 - Dispose crash on AVAudioRecorder

 
-   Fixed #567351 - Cannot set nullable properties via reflections

 
-  Fixed #567455 - Cannot start new NSThread


-   Fixed typo in UIAlertView.FirstButtonInder -&gt; FirstButtonIndex

 
-  Fixed wake up WWAN bug.


-  Fixed NSNetServiceBrowser binding.


-   Fix deregistration of listeners in AudioQueue (they were always kept around, unless manually removed).

 
-  Fixed #554744 - Cannot make custom CALayer


-  Fixed unicode usages of NSString




 <a name="API_Breaking_Changes_for_1.4.4" class="injected"></a>


#  **API Breaking Changes for 1.4.4**

-   bool UINavigationController.SetToolbarHidden(bool,bool) --&gt; void UINavigationController.SetToolbarHidden(bool,bool)

 
-   bool UISwitch.SetState(bool,bool) --&gt; void UISwitch.SetState(bool,bool)

 
-   bool UIViewController.SetEditing(bool,bool) --&gt; void UIViewController.SetEditing(bool,bool)
