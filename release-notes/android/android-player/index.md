---
id: D8855128-79AE-4DCB-9A3E-CE76D128842B
title: "Xamarin Android Player"
subtitle: "Release Notes"
---

**Please note that the Xamarin Android Player is now discontinued. See our [blog post](https://blog.xamarin.com/live-from-dotnetconf-cycle-7-xamarin-studio-6-and-more/) and our [documentation page](https://developer.xamarin.com/guides/android/deployment,_testing,_and_metrics/debug-on-emulator/) for more information.**

# 0.6.5

**Released: November 4th, 2015**

## Download

* Windows (64bit) - [Xamarin Android Player x64.exe](http://xamarin-android-player.s3.amazonaws.com/player/win/0.6.5/XAP-Beta-15.43-v0.6.5-amd64.exe)
* Windows (32bit) - [Xamarin Android Player x32.exe](http://xamarin-android-player.s3.amazonaws.com/player/win/0.6.5/XAP-Beta-15.43-v0.6.5-i386.exe)
* Mac - [Xamarin Android Player.dmg](http://xamarin-android-player.s3.amazonaws.com/player/mac/0.6.5/XAP-Beta-15.43-v0.6.5.dmg)

## New Features

* VirtualBox updated to 5.0.4.
* Android M preview images.

## Fixed

* Fixes related to adb shell escaping changes that prevented devices from
  launching in XS/VS correctly.
* Setting longitude and bearing now works as expected (0.5.5 regression).
* [Mac] UI fixes in preparation of El Capitan.
* [Win] Catch exception when failing to find suitable adb binary.
* [Mac] XAP no longer downloads 101% of updates.
* [Win] If an instance of adb is already running, use that.
* Prevent device deletion resulting in inaccessible VMs.
* VMs being inaccessible could crash the device manager.
* Battery having a fixed value of 0 on some machines.

# v0.6.1

**Released: September 22nd, 2015**

## New Features

* VirtualBox updated to 5.0.4.

## Fixed

* Fixes related to adb shell escaping changes that prevented devices from
  launching in XS/VS correctly.
* Changing longitude no longer changes latitude instead (0.5.5 regression).
* [Mac] UI fixes in preparation of El Capitan.
* [Win] Catch exception when failing to find suitable adb binary.
* [Mac] XAP no longer downloads 101% of updates.
* [Win] If an instance of adb is already running, use that.

# v0.5.6

## Fixed:

* [Win] Add full path to powershell.exe for systems that don't have it on PATH.
* [Win] Windows 10 host-only network creation.
* UTC and TimeZone will now mirror the host on boot.
* Calls to VBoxManage now make use of device UUIDs instead of names.
* [Mac] Reduce delay of IPC between the device manager and player instances.
* [Win] Fix InvalidOperationException when resizing before OpenGL has been initialized.
* Starting and stopping of devices is a lot less error prone.
* Failure to get/set/clear device IP no longer throws an exception.
* [Win] Pop up message when a player instance is already running.
* Devices are now created with the number of cores
* [Win] Logs moved to AppData.
* [Mac] Hide Clear button when textbox is empty.
* [Mac] Add count to device list headers.
* GPS values now persist on device power off.
* [Mac] Hide Installed Devices header when section empty.
* [Win] Check vboxdrv state at startup.
* [Mac] Repeated firewall acceptance request during player launch.
* [Mac] Enable cancel button in device creation dialog.
* [Win] Fix bug where no GL was displayed after restoring from minimized.


# v0.4.4

## New Features

* Only requires downloading each API level once to install different devices
* Multiple new device form factors supported
* Log gathering tool for bug reporting
* VirtualBox updated to 4.3.28


## Fixed

* XAP is now compatible with installed versions of VirtualBox 5.0
* Prevent invalid device names
* No alert when device name is duplicated
* Certain non-US keyboard characters were unsupported
* Support character input using Alt key
* Visual issues on rotation when maximized
* Inverted touch input when rotated anti-clockwise on OS X
* Inverted touch input when closed and relaunched in landscape mode
* Prevent rotation before device is ready
* Ensure orientation is correct on startup
* Support for UNC paths
* No devices shown when disk space is low
* Fall to GetDiskFreeSpaceEx if DriveInfo fails
* Screenshots saved to incorrect location on localised versions of Windows
* "Do not display" option for Hyper-V warning
* Unsupported CodePage error on zip extraction
* Support touch scrolling in the device manager on touchscreen devices
* Screenshot typo
* Windows graphical improvements
* Prevent failed single instance loading of device manager
* Lollipop devices fail to load if Hyper-V is enabled
* Updated launcher in Lollipop devices
* Display on screen keyboard in Lollipop devices by default
* Prevent repeated "Optimizing applications" process in Lollipop devices
* Use snapshots for factory reset on OSX
* DPI values were incorrect for some devices
* Improvements to host-only network setup
* Prevent crash and alert user if VirtualBox is not installed or inaccessible
* Cleanup and refactoring
* Threads without IsBackground set to true preventing application exit
* Installing multiple devices simultaneously could result in only one being added to installeddevices.json
* Adapter mask explicitly set to 255.255.255.0


# v0.4.3

## Features

* VT-x & AMD-V hardware accelerated virtualization
* OpenGL ES 2.0
* Android Lollipop 5.1.0 (API 22)
* Android KitKat 4.4.2 (API 19)
* Android Jellybean 4.4.1 (API 16)
* Battery & GPS settings simulation
* Screenshot function
* Drag & drop apk installation
* Device auto-connects with adb
* Native user interface on both Windows and Mac
* Error diagnostic tool

## Known Issues

### Windows:

* Cannot be run inside most Virtual Machines, or over RDP
* Camera not supported
* With certain video cards, suspending and resuming PC or changing monitor configuration may crash the Player

### Mac:

* Cannot be run inside most Virtual Machines, or over RDP
* Camera not supported


-----


# v0.2.5

* [Changelog](http://xamarin-android-player.s3.amazonaws.com/player/mac/0.2.5/changelog.zip)

## Features

* VT-x & AMD-V hardware accelerated virtualization
* OpenGL ES 2.0
* Android Lollipop 5.1.0 (API 21)
* Android KitKat 4.4.2 (API 19)
* Android Jellybean 4.4.1 (API 16)
* Battery & GPS settings simulation
* Screenshot function
* Drag & drop apk installation
* Device auto-connects with adb
* Native user interface on both Windows and Mac

## Known Issues

### Windows

* Cannot be run inside most Virtual Machines, or over RDP
* Camera not supported
* Landscape screenshots are saved in portrait
* With certain video cards, suspending and resuming PC or changing monitor configuration may crash the Player
* Can currently only be run by the user who installed it

### Mac

* Cannot be run inside most Virtual Machines, or over RDP
* Camera not supported
* Landscape screenshots are saved in portrait
* Can only be run by the user who installed it

