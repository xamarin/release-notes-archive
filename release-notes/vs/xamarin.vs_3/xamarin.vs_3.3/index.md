---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.3"
---

##  <a name="0" id="0">Xamarin 3.3</a>


Xamarin 3.3 is a minor release to support the new [Xamarin.iOS](/releases/ios/xamarin.ios_7/xamarin.ios_7.2/#6) and [Xamarin.Android](/releases/android/xamarin.android_4/xamarin.android_4.14/) releases,
    and includes minor features and bug fixes.

### Features

-  Enable disconnection from a build host. This allows easy switching between multiple instances of Visual Studio that need to interact with a single build host, without requiring IDE restarts.   
  ![](Images/disconnect_host.png) 


### iOS Designer

-  Views can now be rearranged using the new SendBackward, SendToBack, BringForward and BringToFront commands.
-  Improved the alignment marker logic so that mid/baseline drop areas are preferred over top/bottom/left/right alignment markers
-  Improved handling of UIViewController.LoadView/UIViewController.ViewDidLoad when rendering custom controls.
-  UIButton frames are now updated as expected when changing the type back to 'System'
-  Fixed an issue where some tristate properties would not change out of the 'indeterminate' state.
-  We now support generating [Action] methods with no sender parameter
-  Improved support for Xcode6 and Yosemite. Some crashes caused by Xcode 6 / iOS8 support have been resolved. 
-  An exception triggered by selecting a constraint which references a Top or Bottom layout guide has been fixed.
-  Fixed a case where we could generate invalid storyboard files when working with UITextView.
-  Fixed a crash triggered by disabling autolayout under certain circumstances.
-  The iOS Designer was misgenerating partial methods associated with Actions. The bug caused them to semi-randomly appear/disappear from the .designer file.


### Known Issues

-  Visual Studio 2013 Update 2 RC is not supported. Please upgrade to Update 2 RTM.


### Fixes

-  Enables and makes visible Publish context command for non Xamarin.iOS projects (if applicable)
-  Ensure Android project can be deployed before debugging
-  Debugger provides no information on exception that occurs when missing a permission (Android)
-  VS crashes when toggling Error / Warning / Message buttons on and off
-  Build error for WindowsPhone application on Xamarin.Forms solution
-  SDK synchronization broken in XamarinVS 3.1 "Unable to connect to server"
-  Unable to run iOS applications through VS, when paired Build Host has Trial account.
-  Do not force VS Standard toolbar visibility.


### Improvements

-  Improves context detection to automatically hide/show Xamarin commands.
-  Cleanup Tools menu by introducing Android and iOS grouping menus
-  Automatically make iOS toolbar visible only while there is at least one open iOS project (unless the user explicitly changes this behavior)
-  Automatically make Android toolbar visible only while there is at least one open Android project (unless the user explicitly changes this behavior)
