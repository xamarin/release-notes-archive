---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.7"
---

##  <a name="0" id="0">Xamarin 3.7</a>


Xamarin 3.7 updates [Xamarin.iOS 8.2](/releases/ios/xamarin.ios_8/xamarin.ios_8.2/#6) and [Xamarin.Android 4.18](/releases/android/xamarin.android_4/xamarin.android_4.18/) releases,
    and support for iOS8 development.

### Xamarin Designer for iOS

-  Actions, Outlets and new types are now generated for projects based on the Xamarin.iOS Unified API. 
-  Custom properties should always show up in the correct section in the property panel. 
-  The PreferredStatusBarStyle value for custom UIViewControllers is respected by the designer. 
-  Much improved support for constraints made against the margin of a superview/sibling view. 
-  Changing the 'Breaking mode' in WebView should work correctly now 
-  Altering the text traints in UITextField should work correctly now 
-  Setting the 'selectedImage' property of UITabBarItem correctly updates the storyboard 
-  Fixed an issue where images would display in the designer or the app but not both 


#### Changes to custom control rendering

Over the last several months we have realised that the majority of custom controls are
  unsafe to execute by default inside the designer. They typically rely on data provided by
  the application, but that data is not available when run inside the designer and so they just throw exceptions.

To provide a better experience for people we have made custom control support opt-in rather than
  than enabled by default. To load up a specific UIView or UIViewController as a custom control you
  must either implement```
System.ComponentModel.IComponent
```

or annotate the class with```
[DesignTimeVisible (true)]
```



### New Features

-  Support for Xamarin Components with Nuget Packages dependencies.
-  Allow to load, create and browse Xamarin projects with starter license. However, build is not allowed. This version includes a new landing page which allows the user to login or go to the store to enable project build.


### Xamarin Android Player integration

Xamarin 3.7 introduces support for Xamarin Android Player. It will get enabled only if you have Xamarin Android Player installed on your machine. In that case you will be able to:

-  Launch the Xamarin Android Player Device Manager from the "Tools - Android - Manage Virtual Devices" menu in Visual Studio.
-  Xamarin Android Player virtual devices are now part of the Visual Studio device list (even if they're not running). You can now select any of them and use it to deploy or debug your Android application.


### Bug Fixes

-  Bug fix for error when trying to load Xamarin projects saying the project is "Unsupported"
-  Fixes unsolvable warning "There is a minor mismatch between the Build Host and Xamarin Visual Studio".
-  Fix for iOS Activation Dialog appearing on each Android project load, create or build when the user has a Xamarin Android Business License but not a Xamarin.iOS.
-  Try to automatically reconnect to Build Host after disconnection if it was not explicitly disconnected.


### Known Issues

#### Xamarin.iOS Unified API compatibility with Portable Libraries and NuGet Packages

Xamarin 3.6 introduces a new Xamarin.iOS Unified API framework in addition to the classic Xamarin.iOS one (MonoTouch). As the current stable version of Microsoft NuGet Package Manager (2.8.2) does not support this framework yet, we're not registering the framework in the compatible Portable Profiles to avoid breaking the existing NuGet behavior for PCL projects.

To enable .Net Portable Libraries compatibility with the new Xamarin.iOS Unified API framework before the official stable 2.8.3 release of NuGet is available from Microsoft, we're providing a separate installer, which registers the framework in the compatible profiles, and installs an Alpha version of Microsoft NuGet Package Manager (2.8.3 Alpha), to avoid breaking NuGet support in your projects.

You can download this additional installer from the following link: [http://xvs.xamarin.com/Xamarin.iOS.PortableNuGet.msi](http://xvs.xamarin.com/Xamarin.iOS.PortableNuGet.msi)
