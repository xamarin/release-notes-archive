---
id: 0581AAFB-B4AD-499C-9B2C-D494C2C08A54
title: "Xamarin.iOS for Visual Studio 1.6"
---

Xamarin.iOS for Visual Studio 1.6 contains several bug fixes.

## Updater

-  The updater workflow has significantly changed.
-  You will no longer be able to download individual updates for the Visual Studio extensions, they must be updated together.   
-  Update notifications will now appear in the Taskbar.
-  Please note: Downgrading through the updater continues to be unsupported.


## Documentation

-  Added MS Help Viewer support for VS 2010/12/13.
-  Documentation update notifications will now appear in the Taskbar.


## Pairing feature added

-  **Xamarin.iOS 7.0.3 or higher is required to use this version of Xamarin.iOS for VS.**
-  There is now a Xamarin.iOS Build Host application. This application will need to be running on your Mac during Xamarin.iOS for Visual Studio use. You will now be prompted to ‘pair’ your Visual Studio instance with your Xamarin.iOS Build Host. 
-  Pairing is initiated from the Visual Studio side. Connecting to your Build Host will prompt for a PIN (Personal Identification Number). From the Mac, you’ll need to copy the PIN into the dialog on Visual Studio. Please see our  [updated Windows Installation guide](http://docs.xamarin.com/guides/ios/getting_started/installation/windows/troubleshoot.html) for additional details. 


## SDK Sync

-  Improved UI for SDK/API Docs synchronizing processes.
-  SDK sync notifications will now appear in the Taskbar.
-  You can now manually initiate the SDK sync from Xamarin.iOS Options.


## Fixes

-  IPhoneResourcePrefix support has been added.
-  MfA device chooser removed.
-  Dropdown now includes simulators and attached devices. When selected, simulator will transition from [A]=Available to [S] Starting to just the name when running. 
-  [iOS-VS] Unable to close VS to finish Xamarin.iOS sdk update
-  Distribution Profiles should sync correctly to the server
-  Xamarin Updates actions lock entire UI
