---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.6"
---

##  <a name="0" id="0">Xamarin 3.6</a>


Xamarin 3.6 updates [Xamarin.iOS 8.0](/releases/ios/xamarin.ios_8/xamarin.ios_8.0/#6) and [Xamarin.Android 4.16](/releases/android/xamarin.android_4/xamarin.android_4.16/) releases,
    and introduces support for iOS8 development.

### New Features

-  This new release includes support for iOS 8. 
-  Support to add new .metal files with a custom build action 'Metal'
-  BuildHost UI now shows the BuildHost version along with the Xamarin.iOS version 
-  Visual Studio disconnects from BuildHost if loca/Mac SDK versions ar not compatible to avoid misleading error messages.
-  If VS was explicitly disconnected from BuildHost it won't automatically try to reconnect until explicitly connected. This change facilitates work on disconnected build scenarios. 


#### New iOS 8 Project Templates

-  Action Extension
-  Custom Keyboard Extension
-  Document Picker Extension
-  Document Picker File Provider Extension
-  Photo Editing Extension
-  Share Extension
-  Today Extension
-  SceneKit Project
-  SpriteKit Project
-  Metal Project


#### SceneKit

-  New "BundleResource" file extensions: .doa, .scnp, .sks
-  SceneKit Assets (.scnassets)


#### iOS 8 Entitlements

For iOS8 Applications, Xamarin 3.6 includes support for the following entitlements:

-  iCloud Documents
-  CloudKit
-  Personal VPN
-  Associated Domains
-  App Groups
-  HomeKit
-  HealthKit
-  Wireless Accessory Configuration


#### Xamarin Designer for iOS

-  Improved support for Xcode6 GM 
-  Rendering support for the new 4.7" and 5.5" resolutions has been added 
-  Added support for the new @3x style images 
-  Images with ~iphone or ~ipad appended to their name should be handled correctly by the property panel image selector now. 
-  Fixed a crash when using Xcode 6 and selecting a UIActivityIndicatorView on the surface 
-  Fixed a rendering glitch where controls could not be made smaller than 88 pixels in height in certain circumstances. 
-  Fixed an issue whereby some ComboBoxs in the property panel did not save new values to the storyboard file. This affected things like Simulated Metrics. 
-  Initial support for unified storyboards. This is also known as 'Size Class' support. 
-  Fixed many property panel issues with UISearchBar, UITableView, AttributedStrings and more. 
-  Enhanced error logging when custom controls cause issues. 
-  Fixed a bug whereby autoresizingMask values could be incorrectly applied when in constraint mode 
-  Improved handling of 'Modal' segues when rendering simulated metrics 
-  The TabBar inside a ProxiedTabBarController is now selectable with the mouse 
-  A failed drag/drop of a view will correctly restore the ViewController to it's original state. This was just a cosmetic issue. 
-  TableView Headers/Footers do not set 'translatesAutoResizingMaskIntoConstraints' to false anymore. iOS does not support this at runtime. 
-  Double clicking on a Button to generate an action no longer makes the button jump around when you tab back to the design surface 
-  The design surface should no longer jump when selecting items, creating constraints or using the embedded constraint editor 
-  UITableViewSection elements can no longer be dropped in invalid locations 
-  Custom Controls work correctly when using MonoTouch 7.9 or higher 
-  'View As iOS6.1 and earlier' now works with Xcode6 
-  Some small rendering performance improvements 
-  Several repainting issues have been fixed on the design surface 
-  Implemented support for constraint multipliers in the form 1/2 or 4/9, etc. 
-  Fixed some minor layout issues with the designer toolbar 
-  The light style for UIStatusBar is now fully supported 


### Bug Fixes

-  XamarinVS  **3.6.253** fixes  [bug 22834](https://bugzilla.xamarin.com/show_bug.cgi?id=22834) : Addresses an issue that could prompt the user with an iOS activation dialog when using Android projects.
-  XamarinVS  **3.6.249** fixes  [bug 23220](https://bugzilla.xamarin.com/show_bug.cgi?id=23220) : Addresses an issue that would cause Visual Studio fail to recognize valid project types.
-  XamarinVS  **3.6.262** fixes  [bug 23353](https://bugzilla.xamarin.com/show_bug.cgi?id=23353) : Addresses a performance regression in connectivity to the build host. The iOS designer should be much more responsive. An issue where users would be unable to see their connected iOS devices is resolved..


### Known Issues on v.3.6.245

#### Xamarin.iOS Unified API compatibility with Portable Libraries and NuGet Packages

Xamarin 3.6 introduces a new Xamarin.iOS Unified API framework in addition to the classic Xamarin.iOS one (MonoTouch). As the current stable version of Microsoft NuGet Package Manager (2.8.2) does not support this framework yet, we're not registering the framework in the compatible Portable Profiles to avoid breaking the existing NuGet behavior for PCL projects.

To enable .Net Portable Libraries compatibility with the new Xamarin.iOS Unified API framework before the official stable 2.8.3 release of NuGet is available from Microsoft, we're providing a separate installer, which registers the framework in the compatible profiles, and installs an Alpha version of Microsoft NuGet Package Manager (2.8.3 Alpha), to avoid breaking NuGet support in your projects.

You can download this additional installer from the following link: [http://xvs.xamarin.com/Xamarin.iOS.PortableNuGet.msi](http://xvs.xamarin.com/Xamarin.iOS.PortableNuGet.msi)
