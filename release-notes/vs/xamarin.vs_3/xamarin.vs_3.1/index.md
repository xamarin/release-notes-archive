---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.1"
---

##  <a name="228" id="228">Xamarin 3.1.228</a>


Xamarin 3.1.228 is a hotfix release based off of Xamarin 3.1.224.

### Fixes

-  SDK synchronization reporting "Unable to connect to server".


##  <a name="2" id="2">Xamarin 3.1.224</a>


Xamarin 3.1.224 is a hotfix release based off of Xamarin 3.1.223.

### Fixes

-  The iOS Designer was misgenerating partial methods associated with Actions. The bug caused them to semi-randomly appear/disappear from the .designer file.


##  <a name="1" id="1">Xamarin 3.1.223</a>


Xamarin 3.1.223 is a hotfix release based off of Xamarin 3.1.

### Fixes

-  Fixes a regression introduced by Android SDK Tools r23 and Android Build-tools r20 that changed the path of the zipalign tool.


##  <a name="0" id="0">Xamarin 3.1</a>


Xamarin 3.1 contains several bug fixes and minor improvements.

### Known Issues

-  The SDK Synchronization tool will fail to connect to the build server. This will be fixed in an upcoming release.
-  Visual Studio 2013 Update 2 RC is not supported. Please upgrade to Update 2 RTM.


### Fixes

-  Unable to deploy Android application in DEBUG mode.
-  App hangs when changing Android system time before installing an APK.
-  "Notify about updates" selection ignored.
-  Several issues when iOS app name contains dots.
-  Xamarin.Forms template not generating unique identities for WP projects.
-  VS 2013 Update 2 freezes frequently when packaging application.
-  VS crash when reloading a project fails.
-  Android Device Logging - List View - no autscroll to newest item.
-  Ensure that killing or closing the Android emulator does not hang VS.
-  On build cancel (Android) reset emulator string to Available (not Starting).
-  User is shown latest (Android) platform which is not installed on machine.
-  Remove all Android permissions from AssemblyInfo.cs
-  When the user intentionally stops the debugger, they are incorrectly shown the error "Debugger Connection Lost".
-  Diagnostic Tool should report the server and client time to help diagnose clock skew issues.
-  Added missing Razor iOS templates.
-  Prevent multiple simultaneous connection attempts to the build server.
-  Unable to build adhoc via Build->Build Adhoc IPA
-  At iOS project properties window, clicking Security or Publish option shows error "this method or operation not implemented'.
-  Add GUI for .apk/ABI
-  In french VS, platform and configuration drop down appears multiple times.
-  Refresh does not show new (iOS) simulators.
-  Problem with deploying application from Visual Studio when using embedded resources.
-  Supported Architecture setting is not saving in VS2010.
-  Unloaded projects is loaded again in Visual Studio 2013.
-  When using Hibernation to "shutdown" windows, when restored the client connection is not re-created
-  [Ad-hoc] Failed to start application on the target device
-  List of known simulators shows up at a random time
-  Killing the connection of the current server before creating a new one.
-  Resource (resx) files are not loaded when using Visual studio for iOS


### Improvements

-  Several improvements to logging (missing build server errors, properly parsing XML output from build server, etc.)
-  Several improvements and clean up in templates for consistency.
-  All projects are now easily identifiable by their icons.
