---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.6"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.6</a>




This gives access to the new Xamarin SDKs: [Xamarin.iOS 10.12](/releases/ios/xamarin.ios_10/xamarin.ios_10.12/) and [Xamarin.Android 7.4](/releases/android/xamarin.android_7/xamarin.android_7.4/).

Content:

-  [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)
-  [Property Pages and Manifest redesign ](#props) -  [New Entitlements Editor](#entitlements)
-   Several improvements and bug fixes.


 
-  [Bug Fixes.](#bugfixes)
-  [Known Issues.](#knownissues)






## Included in this release:

###  <a id="props"></a>
Property Pages and Manifests redesign

In Xamarin 4.6 we are continuing working on the redesign of our Property Pages and Manifest editors adding a new editor: the Entitlements Editor.

####  <a id="entitlements"></a>
New Entitlements Editor

The new editor is now a stand-alone editor. It was designed in a way it's simpler and effective and can be launched
    by double clicking your entitlements.plist file. It provides a user-friendly UI which can be easily browsed, keeping a familiar look and feel for editting manifests.

 ![](entitlements.png)

###  <a id="bugfixes"></a>
Bug fixes.

This release includes the following fixes:

-  iOS device list simulator list does not get updated when changing iOS version to lower. **(4.6.0.289)**
-  Fixed VS hang on Zeroconf during build host discovery. **(4.6.0.289)**
-  The SayGoodbye target fails when building an iOS Library. **(4.6.0.279)**
-  MSBuild process produces high CPU usage due to XMA monitoring. **(4.6.0.279)**
-  Mac Agent icon doesn't update after reconnection in some scenarios. **(4.6.0.279)**
-  Cannot manually select the Xcode path in settings. **(4.6.0.279)**
-  Android Archive - Warn the user about keystore backup needed and facilitates copying it to a different location. **(4.6.0.279)**
-  Cannot open Assets Catalogs named "Assets" in Visual Studio 2017. **(4.6.0.279)**
-  VS doesn't set the MinimumOSVersion key in the .plist file for a new iOS project. **(4.6.0.279)**
-  "Linker Behavior" drop-down shows inaccurate default value of "Don't Lin" for MtouchLink property. **(4.6.0.279)**
-  Show Xamarin.iOS compatibility errors on the Mac Server connection dialog. **(4.6.0.279)**
-  User is able to drag .png files to Vector section of image assets. **(4.6.0.279)**
-  Supported Families and Complication Group is not disabled when Data Source Class is not selected. **(4.6.0.279)**
-  Change connection flow to not show any dialog when auto connecting like when openning a solution. **(4.6.0.279)**
-  Set the correct configuration platform when a UWP project is set as startup project. **(4.6.0.279)**
-  tvOS binding project build fails with multiple errors. **(4.6.0.279)**
-  Visual Studio hangs on ZeroConf in some scenarios **(4.6.0.279)**
-  MSBuild process produces high CPU usage due to incorrect parent process monitor on XMA. **(4.6.0.240)**
-  The SayGoobye target fails when building an iOS library. **(4.6.0.240)**
-  Unhandled exception on Debugging File Provider Extension app. **(4.6.0.240)**
-  VS crashes clicking on "Add to app" while adding free app component twice. **(4.6.0.240)**
-  Typos on iOS Icons Visual Assets editor. **(4.6.0.240)**
-  Native Static Reference (.a) source file ends up with 0 Kb after build. **(4.6.0.240)**
-  Typos on Android Property pages. **(4.6.0.240)**
-  F# Android project fails to build with multiple errors. **(4.6.0.240)**
-  System.IO.FileNotFoundException on deploying WatchOS application. **(4.6.0.240)**
-  tvOS C# of SpriteKit Game template fails in building application.. **(4.6.0.240)**
-  Several connection reliability Mac agent fixes. **(4.6.0.240)**
-  Android Library template includes Resource files. **(4.6.0.240)**
-  Android project template doesn't generate mipmap icons. **(4.6.0.240)**
-  Unable to depoly tvOS extension app[TV Services Extension] in debug mode. No tvOS simulators in device dropdown. **(4.6.0.240)**
-  "Xamarin for Visual Studio Updates" dialog does not give the user a way to get past "This installation package could not be opened" if one of the .msi files has an incorrect MD5 checksum after it finishes downloading. **(4.6.0.240)**
-  Visual Studio Crash trying to start an Android app without activities. **(4.6.0.240)**
-  Sets watchOS on Default mode as default simulator. **(4.6.0.240)**
-  Native breakpoint does not hit, with Microsoft debugger. **(4.6.0.240)**


###  <a id="knownissues"></a>
Known issues

#### Build canceled with error: Project ' *project_name*' requires the following components installed on your machine: ...

Building Android applications can require installing additional components. This can be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine.

Xamarin for Visual Studio detects the lack of those missing resources, and  shows an error informing it requires to download and install them:

 ![](missingresources.png)

Double click on that error in the list to start downloading and installing the missing components.

Please keep in mind that you need to have Intellisense errors visible in the list, otherwise you won't be able to see that error.

If you try to build any project in the solution without installing the missing components, the build will be canceled. You cannot build without installing those components. Please ensure Intellisense errors are visible to be able to start installing them.

An optional way to install missing components is to build from the command-line.

#### Other Known issues

The 15.3 installer MSI may remove the Xamarin extension from Visual Studio 2013. If you need to use Xamarin with Visual Studio 2013, you can download a valid installer [here](https://dl.xamarin.com/XamarinforVisualStudio/Windows/Xamarin.VisualStudio_4.5.0.486.msi).

If you downgrade to Xamarin 4.2 or older versions after using this release, you will need to re-register your known Mac servers in the Mac Server dialog. Please use the Forget Mac option, and configure your server connection again.

### Xamarin for Visual Studio 4.6.3

Additional fixes were released in Xamarin for Visual Studio 4.6.3, including:

-  "MonoTouch.Design.Client.DesignerRemoteException: System.NotSupportedException: Could not parse xml" when attempting to open a storyboard or .xib file. **(4.6.3.4)**


### Xamarin for Visual Studio 4.7.9

Xamarin for Visual Studio 4.7.9 adds IDE compatibility for iOS 11 simulators and Xcode 9 and gives access to updated Xamarin SDKs: [Xamarin.iOS 11.0](/releases/ios/xamarin.ios_11/xamarin.ios_11.0/) and [Xamarin.Android 7.4.5](/releases/android/xamarin.android_7/xamarin.android_7.4/#Xamarin.Android_7.4.5-1).

Note that the IDE features in this version are part of the Xamarin for Visual Studio 4.6 release series. Version 4.7.9 adds IDE compatibility for Xcode 9, but it does not yet include any additional features from the Visual Studio Tools for Xamarin [4.7.0 previews](/releases/vs/xamarin.vs_4/xamarin.vs_4.7/).
