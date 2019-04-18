---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.0"
---

Xamarin 3.0 contains several bug fixes and new features.

## Compatibility Notes

-  Xamarin 3.0 is not compatible with Visual Studio 2013 Update 2 RC. Please upgrade to the final version of Update 2.
-  Xamarin.Forms Shared template requires Visual Studio 2013 with Update 2.
-  Xamarin.Forms PCL template on Visual Studio 2010 requires the  [](http://visualstudiogallery.msdn.microsoft.com/b0e0b5e9-e138-410b-ad10-00cb3caf4981/) Portable Library Tools by Microsoft
-  All Xamarin.Forms templates require the appropriate Windows Phone SDK.


## Major Changes

-  Xamarin.Forms templates for PCL and Shared projects.
-  Added WebView templates for Android/iOS.
-  Razor Template Preprocessor.
-  iOS and Android addins have been merged. This change will fix many compatibility issues that customers had experienced in the past. Before this change, users were required to install specific corresponding versions of the iOS and Android for VS extensions. When you didn’t, you would be prompted with an unfriendly dialog and, in some cases, some very strange or broken behavior.
-  Allow Setting of an Apple SDK path with the iOS Settings page
-  Added support for the newest PCL profiles released with Visual Studio 2013 Update 2.


## Xamarin Designer for iOS

-  The Xamarin Designer for iOS is a visual designer for the iOS Storyboard format which is fully integrated into Visual Studio. The iOS Designer maintains full compatibility with the Storyboard format, so that files can be edited in either Xamarin Studio or Visual Studio in addition to Xcode's Interface Builder. Additionally, the Xamarin Designer for iOS supports advanced features such as custom controls that render at design-time in the editor.   
 ![](http://docs.xamarin.com/releases/vs/xamarin.vs_3/xamarin.vs_3.0/Images/designer_vs.png)


## Fixes

-  More responsive detection of iOS devices being plugged in on the Mac host.
-  Fixed long wait times when building iOS applications
