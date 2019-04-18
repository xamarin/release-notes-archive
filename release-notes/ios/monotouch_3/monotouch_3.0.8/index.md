---
id: B61D1F26-E85B-B165-8E15-AAF6D36A5607
title: "MonoTouch 3.0.8"
---

&nbsp;

MonoTouch 3.0.8 introduced support for Apple's iPhone 4 SDK and supports the
following platforms:

-  iOS 4 (iPhone and iPod devices)
-  iPhoneOS 3.2 (iPad)
-  iPhoneOS 3.0 (iPhone and iPod devices).


 <a name="What_is_new_in_this_release" class="injected"></a>


# What is new in this release

A detailed list of API changes from version 2.0 is available for developers
to explore what is new in MonoTouch 3.

 <a name="" class="injected"></a>


## Multitasking [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

MonoTouch 3.0 supports all the new APIs to allow your application to
multi-task on iOS 4.0. As part of this effort, we introduced bindings to Grand
Central Dispatch (see the class MonoTouch.CoreFoundation.Dispatch).

You can build applications that support:

-  Background Audio
-  Voice over IP
-  Background Location
-  Receive push notifications even if your app is sleeping
-  Local notification support, without requiring a server to push the data.
-  "Just one more minute" support, to let your application complete any critical task before it is put in the background. 
-  Fast App Switching support.


Multitasking support builds also on top of our new binding to the Blocks
API.

 <a name="Integration_Technologies" class="injected"></a>


##  <u>Integration Technologies</u>

All of the new iOS =4.0 ["Integration Technologies"](http://developer.apple.com/iphone/library/releasenotes/General/WhatsNewIniPhoneOS/Articles/iPhoneOS4.html#//apple_ref/doc/uid/TP40009559-SW6) features introduced by Apple are
supported in this edition of MonoTouch.

 <a name="" class="injected"></a>


## Location Notifications [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

Local notifications, provided by the MonoTouch.UIKit.UILocalNotification, for
more information see the [Local and Push Notifications Guide](http://developer.apple.com/iphone/library/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Introduction/Introduction.html#//apple_ref/doc/uid/TP40008194).

 <a name="" class="injected"></a>


## EventKit [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

EventKit framework, gives you access to the device calendar
(MonoTouch.EventKit).

 <a name="" class="injected"></a>


## CoreMotion [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

CoreMotion gives you access to the gyroscope and accelerometer
(MonoTouch.CoreMotion).

 <a name="" class="injected"></a>


## CoreTelephony [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

CoreTelephony gives you access to information about your cell provider
(MonoTouch.CoreTelephony).

 <a name="" class="injected"></a>


## Apple iAd [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

iAd allows developers to integrate advertisements into their applications
(MonoTouch.iAd)

 <a name="Graphics_and_Multimedia" class="injected"></a>


##  <u>Graphics and Multimedia</u>

 <a name="High_Resolution_APIs" class="injected"></a>


## High Resolution APIs

Support for iPhone 4's Retina Display is accomplished through various
extensions to the UIKit and CoreAnimation APIs. These new APIs are also exposed
to MonoTouch developers (MonoTouch.UIKit.UIScreen.Scale,
MonoTouch.UIKit.UIImage.CurrentScale,
MonoTouch.UIKit.UIView.ContentScaleFactor).

 <a name="" class="injected"></a>


## Quick Look Framework [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

This new API has been bound allowing your application to preview the contents
of foreign file formats. The APIs are available in MonoTouch.QuickLook.

 <a name="" class="injected"></a>


## AVFoundation [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

The AVFoundation framework gives developers more fine grainer control over
music and video playback and with iOS 4.0 it got a significant boost in terms of
functionality. The new classes are available under MonoTouch.AVFoundation.

These are some of the new additions:

-  Media asset management
-  Movie capture
-  Movie playback
-  Track management
-  Metadata management for media items
-  Stereo panning
-  Precise audio sync between sounds
-  APIs to query details about the media files including data format, sample rate and channels 


 <a name="" class="injected"></a>


# Core Services [ ![](monotouch_3.0.8/Images/icon-trans.gif)](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

 <a name="" class="injected"></a>


## Transparent access to the Blocks API [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

For those familiar with both Objective-C and C# we mapped C# delegates and
lambdas into Objective-C blocks, so all the new blocks-based API is available to
developers. Developers in C# can continue to use lambda functions as well as
anonymous methods, and those will be transparently exposed to Objective-C as
Objective-C blocks.

 <a name="" class="injected"></a>


## Grand Central Dispatch [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

This task queue management system is used in iPhone OS and MonoTouch now
exposes these APIs for application developers to use.

 <a name="" class="injected"></a>


## Accelerate Framework [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

This API is a flat C API and is only available to developers by manually
using P/Invoke to call into these routines. No object-oriented binding has been
provided for it.

 <a name="UIKit_and_UI_Improvements" class="injected"></a>


# UIKit and UI Improvements

All of the improvements that Apple introduced in iOS 4.0 for UIKit are
exposed in MonoTouch 3.0, this includes the new multi-tasking methods in
UIApplicationDelegate as well as its support for scheduling local
notifications.

 <a name="" class="injected"></a>


## Multithreading improvements [ <span class="icon"><img src="monotouch_3.0.8/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.8#)

In iOS4 it is possible to use a graphics context
(MonoTouch.CoreGraphics.CGContext) in a multi-threaded application. Access to
UIImage, UIColor and UIFont is now also thread safe.

 <a name="Block_Animations" class="injected"></a>


## Block Animations

The new Block-animation APIs in UIView which provide various callbacks for
custom animations are exposed in the API. Blocks in the UIView are merely C#
instances of NSAction, so you can just use delegates, anonymous methods or
lambda functions as your block values.

 <a name="Font_Smoothing_Support" class="injected"></a>


## Font Smoothing Support

CoreGraphics now supports fine grained control of font smoothing in
MonoTouch.CoreGraphics.CGContext.

 <a name="MessageUI" class="injected"></a>


## MessageUI

The new MFMessageComposeViewController now supports a compositing tool for
SMS messages without leaving your application.

 <a name="MapKit" class="injected"></a>


## MapKit

Map overlays and draggable map annotations are now supported.

 <a name="Foundation_Bindings" class="injected"></a>


# Foundation Bindings

Many new Foundation APIs were introduced with iOS 4.0, these have been bound,
and the most interesting include:

-  NSDateComponents
-  NSBlockOperation that allows adding lambdas/delegates to operation queues 
-  NSCache
-  All new features from CoreLocation (MonoTouch.CoreLocation)


 <a name="GameKit" class="injected"></a>


# GameKit

All the new APIs from GameKit (MonoTouch.GameKit) have been added.
