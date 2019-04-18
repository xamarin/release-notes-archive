---
id: 0581AAFB-B4AD-499C-9B2C-D494C2C08A54
title: "Xamarin.iOS for Visual Studio 1.8"
---

Xamarin.iOS for Visual Studio 1.8 contains several bug fixes and new features.

## Compatibility notes

-  Xamarin.iOS 7.0.4 or higher is required to use this version of Xamarin.iOS for VS.
-  Xamarin.iOS for VS 1.8 is compatible with Xamarin.Android 4.10.1.
-  **Older versions of the Visual Studio extensions may fail to update both extensions correctly.** If you have updated and are seeing error messages, please ensure you have Xamarin.Android 4.10.1 installed. Here's a  [direct link to 4.10.1](http://download.xamarin.com/MonoforAndroid/Windows/mono-android-4.10.01073_signed.msi) .


## Portable Class Library support added

-  You can now select Xamarin.iOS and Xamarin.Android as target frameworks for Portable Class Libraries 
-  For more information, check out our new  [Portable Class Library document](http://docs.xamarin.com/guides/cross-platform/application_fundamentals/pcl/) . 


## Pairing feature added

-  There is now a Xamarin.iOS Build Host application. This application will need to be running on your Mac during Xamarin.iOS for Visual Studio use. 
-  Pairing is initiated from Visual Studio. Connecting to your Build Host will prompt for a code that is generated using the Xamarin.iOS Build Host application. Please see our  [updated Windows Installation guide](http://docs.xamarin.com/guides/ios/getting_started/installation/windows) for additional details. 


## Account Management

-  You can log into your Xamarin account directly through Visual Studio from the Xamarin Account dialog.
-  More details about your current account state are available in Xamarin Account dialog.
-  You can access the Xamarin Account dialog from the Visual Studio Tools menu.


## SDK Sync

-  Improved UI for SDK/API Docs synchronizing processes.
-  Sync notifications will now appear in the Taskbar.
-  You can now manually initiate the SDK sync from Xamarin.iOS Options.


## Documentation

-  Added MS Help Viewer support for VS 2010/12/13.
-  Documentation update notifications will now appear in the Taskbar.


## Updater

-  The updater workflow has significantly changed.
-  You will no longer be able to download individual updates for the Visual Studio extensions, they must be updated together.
-  Update notifications will now appear in the Taskbar.
-  Please note: Downgrading through the updater continues to be unsupported.


## Fixes

-  Adds support for VS2013.
-  IPhoneResourcePrefix support has been added.
-  MfA device chooser removed.
-  Dropdown now includes simulators and attached devices. When selected, simulator will transition from [A]=Available to [S] Starting to just the name when running. 
-  [iOS-VS] Unable to close VS to finish Xamarin.iOS sdk update
-  Distribution Profiles should sync correctly to the server
-  Xamarin Updates actions lock entire UI
