---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.5"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.5</a>




This Xamarin for Visual Studio 4.5 release gives access to the new Xamarin SDKs: [Xamarin.iOS 10.10](/releases/ios/xamarin.ios_10/xamarin.ios_10.10/) and [Xamarin.Android 7.3](/releases/android/xamarin.android_7/xamarin.android_7.3/).

Content:

-  [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)
-  [Property Pages and Manifest redesign ](#props) -  [New iOS Project Property Pages ](#iosprops)
-  [Better iOS Info.plist Manifest Editor](#infoplist)
-  [New Android Project Property pages](#androidprops)


 
-  [Bug Fixes.](#bugfixes)
-  [Known Issues.](#knownissues)






## Features included in this release:

###  <a id="props"></a>
Property Pages and Manifests redesign

In Xamarin 4.5 we've started a redesign of our Property Pages and Manifest editors. Looking for consistency with Visual Studio itself and Visual Studio for Mac, our new property pages were reorganized and simplified, supporting high-DPI displays. We've also split editors in more natural way. Now you can keep editing csproj options from the Property Pages, and manifest options from the manifest editor.

####  <a id="iosprops"></a>
New iOS Project Property pages

The new iOS property pages provide all the options stored on the csproj file required to build and run the project correctly. It was redesigned in a way it's simpler and effective.

 ![](xvs45iosprops.gif)

####  <a id="infoplist"></a>
Better iOS Info.plist Manifest Editor

Our iOS Manifest editor (info.plist) was also re-structured. It's now a stand-alone editor, which can be launched by double clicking your info.plist file. It provides a user-friendly UI which can be easily browsed, keeping a familiar look and feel for editting manifests.

 ![](xvs45iosmanifest.gif)

It includes editors for Application version, supported orientation, status bar style, Visual Assets, Capabilities like Game Center, Maps integration or Background Modes, as well as advanced features like editting document types, UTIs, and URL Types.

####  <a id="androidprops"></a>
New Android Project Property pages

We've redesigned the Android project options pages! A simplified design with all the options you need.

 ![](xvs45androidprops.gif)

The advanced Android options have been grouped into a separate Dialog you can open by pressing the "Advanced" button on the Options page

###  <a id="bugfixes"></a>
Bug fixes.

This release includes the following fixes:

-  Resolves Visual Studio crash on some network environments while discovering Mac hosts.  **(4.5.0.486)**
-  Sets right default values for Android Property pages like in "Use Shared Runtime". **(4.5.0.486)**
-  Updates Xamarin Android to fix Command line build "fatal error: mono/metadata/mono-config.h: No such file or directory. **(4.5.0.476)**
-  Fixes Android and iOS Inspection. **(4.5.0.475)**
-  Breakpoint is not hitting in iOS real device in iOS project via Xamarin Forms project. **(4.5.0.475)**
-  Typo on property stored on .csproj for AndroidEnableMultiDex on new Property Pages. **(4.5.0.475)**
-  Fixes wrong CFBundleVersion property used in new info.plist editor for field Build. **(4.5.0.475)**
-  Visual Studio hangs on network disconnect. **(4.5.0.475)**
-  Location of linked files in build directory on Mac build host has changed.  **(4.5.0.475)**
-  Unable to copy appname.dll from obj to bin because it is being used by another process **(4.5.0.475)**
-  Fixes debugging issues with iOS/tvOS/watchOS device-specific builds. **(4.5.0.440)**
-  Improved Bonjour SSH discovery implementation. **(4.5.0.440)**
-  OpenGL Game (Android) Template now uses OpenTK-1.0. **(4.5.0.440)**
-  Android Archive Manager now uses regional settings to show Archive dates. **(4.5.0.440)**
-  Fixes second-level iOS Reference debugging. **(4.5.0.415)**
-  Errors creating F# Blank Android project. **(4.5.0.415)**
-  Ensure tooltips are visible if controls are disabled on Property pages. **(4.5.0.415)**
-  Unable to create IPA even after checking the "Build iTunes Package Archive (IPA)". **(4.5.0.415)**
-  Analyze-Xamarin Profiler option Is disabled for some configutations. **(4.5.0.415)**
-  Adds Android Option for using the concurrent garbage collector (Experimental). **(4.5.0.415)**
-  Explicitly marks iOS Option for using the concurrent SGen Garbage collector as Experimental. **(4.5.0.415)**
-  Adds several missing tooltips and help links for Android property pages. **(4.5.0.415)**
-  Adds Enable Bitcode option for tvOS / watchOS Extension projects. **(4.5.0.415)**
-  Cannot open iOS Manifest editor if the solution contains a shared project. **(4.5.0.415)**
-  Android msbuild: Always set the $(TargetFrameworkRootPath) in props. **(4.5.0.415)**
-  Fixes Main Interface drop-down not setting selected value in iOS. **(4.5.0.415)**
-  Unable to reference PCL in a tvOS or watchOS Project. **(4.5.0.387)**
-  Minor fixes to Xamarin.Android property pages. **(4.5.0.387)**
-  IPA checkbox is disabled in Property page. **(4.5.0.387)**
-  Added missing tooltips to iOS Manifest editor. **(4.5.0.387)**
-  Visual studio-Output window is showing an error “Child node "2" exited prematurely. Shutting down. **(4.5.0.387)**
-  Improvements on F# templates. **(4.5.0.387)**
-  Getting Suppression State Error "The value, constructor, namespace or type 'take' is not defined" when using Array.take in new F# template. **(4.5.0.387)**
-  iOS debugging not working on main app and first level references. **(4.5.0.387)**
-  Breakpoint not getting hit when app is deployed in debug mode in iOS Device. **(4.5.0.341)**
-  Project Options are truncated when resizing VS. **(4.5.0.341)**
-  Unable to deploy tvOS application on AppleTV device from VS. **(4.5.0.341)**
-  Spelling of Implementation in HTTP/TLS. **(4.5.0.341)**
-  Incorrect namespace in added Master Detail Page. **(4.5.0.341)**


###  <a id="knownissues"></a>
Known issues

#### Assets Catalog Editor cannot open catalogs named "Assets" in VS2017

The Assets Catalog Editor in Visual Studio 2017 is not be able to open catalogs named "Assets".
This issue affects the default tvOS Assets catalog created as part of the template. The workaround is to delete that "Assets" catalog and create a new one with the default name "Media".

#### Build canceled with error: Project ' *project_name*' requires the following components installed on your machine: ...

Building Android applications can require installing additional components. This can be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine.

Xamarin for Visual Studio detects the lack of those missing resources, and  shows an error informing it requires to download and install them:

 ![](missingresources.png)

Double click on that error in the list to start downloading and installing the missing components.

Please keep in mind that you need to have Intellisense errors visible in the list, otherwise you won't be able to see that error.

If you try to build any project in the solution without installing the missing components, the build will be canceled. You cannot build without installing those components. Please ensure Intellisense errors are visible to be able to start installing them.

An optional way to install missing components is to build from the command-line.

#### iOS Info.plist Manifest Editor limited Entitlements Support

The new Manifest Editor does not currently support every Entitlement that the previous UI included. Support for more Entitlements in this editor will come in a future release. To add an Entitlement that is not available in the UI yet, right-click on the info.plist file and
choose "Open With". Then, select the "Generic Plist Editor" option. Entitlement keys and values can be added manually in this editor. For a reference of keys and their appropriate values, please visit the [Apple Documentation on Entitlements](https://developer.apple.com/library/content/documentation/Miscellaneous/Reference/EntitlementKeyReference/Chapters/AboutEntitlements.html).

#### Other Known issues

Installing Xamarin 4.5 on a machine with only Visual Studio 2013 where Xamarin was never installed before might end up on a broken installation. In such case, no iOS or Android templates are visible, and trying to load Xamarin project results in Xamarin init failure.

If you downgrade to Xamarin 4.2 or older versions after using this release, you will need to re-register your known Mac servers in the Mac Server dialog. Please use the Forget Mac option, and configure your server connection again.
