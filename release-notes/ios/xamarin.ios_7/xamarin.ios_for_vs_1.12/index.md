---
id: 55F5D5AC-836B-46A6-80ED-C6C8CF0CA505
title: "Xamarin.iOS for Visual Studio 1.12"
---

Xamarin for Visual Studio 1.12 contains several bug fixes and new features.

# Xamarin for Visual Studio 1.12.278

Xamarin for Visual Studio 1.12.278 is a hotfix release to address a bug that occurred when using the new Android SDK Tools 22.6.3

## Fixes

-  15374 - Unable to edit layouts in the Android Designer using Android SDK Tools 22.6.3


# Xamarin for Visual Studio 1.12.275

## Compatibility Notes

-  To use the Xamarin.iOS for Visual Studio Alpha release, you must install the Xamarin.iOS 7.2.2.2, on your build server.
-  If you wish to roll back to the previous Stable, you will need to uninstall this version and re-install the previous stable from scratch.


## Major Changes

-  iOS and Android addins have been merged. This change will fix many compatibility issues that customers had experienced in the past. Before this change, users were required to install specific corresponding versions of the iOS and Android for VS extensions. When you didn’t, you would be prompted with an unfriendly dialog and, in some cases, some very strange or broken behavior.


## Fixes

-  Crash with VS FRA
-  NRE when Error Messages are being cleared.
-  17633 - Crash when starting logging on Android Device Log
-  17520 - Unable to create iOS App
-  17372 - Unable to open IPA in Finder
-  17457 - Error when opening android designer.
-  17065 - iOS build in Visual Studio gets stuck and cannot be aborted if build host was not found
-  17176 - Visual Studio does not include Build field on iOS Application properties screen
