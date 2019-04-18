---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.3"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.3</a>


This Xamarin for Visual Studio 4.3 release updates

 [Xamarin.iOS 10.4](/releases/ios/xamarin.ios_10/xamarin.ios_10.4/)

 and [Xamarin.Android 7.1](/releases/android/xamarin.android_7/xamarin.android_7.1/)

 releases. Content:

-  [System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/)
-  [Improved iOS Assets Catalog support](#assetscatalog)
-  [Generic Plist Editor](#plisteditor)
-  [Multi-process debugging](#mpdebugging)
-  [New Project Templates.](#templates)
-  [Bug Fixes.](#bugfixes)
-  [Known Issues.](#knownissues)
-  [Preview for Xamarin VS 4.3.1](#xvs4_3_1)






## Features included in this release:

###  <a id="assetscatalog"></a>
Improved iOS Assets Catalog support

Our Assets Catalog editor got several additions on this release including Stickers support.

It also adds several improvements around stability using Assets Catalog with solutions in source control systems (like TFS).

###  <a id="plisteditor"></a>
Generic Plist Editor

We're introducing a new Plist editor in Xamarin for Visual Studio 4.3. This new editor allows you to edit any .plist file 
    without having to change the complex XML inner structure, by using a friendly hierarchical edition UI.

This new editor removes the need to switch to the Mac for making those little tweaks in your manifest files.

 ![](plisteditor.png)

The editor includes schema support for the more common scenarios as the Info.plist iOS file, or Root.plist Bundle Settings.

It also provides Search capabilities along the plist file:

 ![](plisteditorsearch.png)

###  <a id="mpdebugging"></a>
Multi-process debugging

This new release includes the ability to debug from the same solution different Xamarin projects running on different devices or simulators.

###  <a id="templates"></a>
New Project Templates 

We're now including some new templates:

-  watchOS Class Library
-  watchOS SceneKit game
-  watchOS SpriteKit game
-  iOS Broadcast UI Extension
-  iOS Broadcast Upload Extension
-  iOS Call Directory Extension
-  iOS iMessage Extension
-  iOS Intents Extension
-  iOS Intents UI Extension
-  iOS Notification Content Extension
-  iOS Notification Service Extension
-  tvOS Broadcast UI Extension
-  tvOS Broadcast Upload Extension


###  <a id="androidxml"></a>
Android XML Editor

Under the "Source" tab IntelliSense has received various improvements and enhancements including:

-  Custom controls element and attribute completion
-  Tools namespace completion


###  <a id="bugfixes"></a>
Bug fixes.

#### 4.3.0.795

-  Adds support for Xcode 8.3.


#### 4.3.0.789

-  Visual Studio hangs loading a cross-platform solution in some environments.
-  Debugging Xamarin Projects cannot hit breakpoints on second-level referenced PCLs.


#### 4.3.0.784

-  Unable to build/Run WatchOS template application with Visual Studio 2017 with error message "Can't get real path for Source...".
-  UI delay on project system events when the Android designer needs to be notified.
-  Fixes debugger support on Visual Studio 2017 if the only installed workload is Xamarin.
-  Xamarin Profiler menu option is now included in the Tools menu.
-  Fixes build error on Android Binding Library projects with Visual Studio 2017.
-  ProjectReference to multi-targeted project fails build.
-  Improved SxS support for VS2017, VS2013 and VS2015.
-  Microsoft.CSharp not referenced in VS project templates.
-  Old JDK paths in sdks cache prevent users from building and resolving project error when updating JDKs.
-  Improved error message when PPDB can't be converted to MDB.
-  Fixes Xamarin reporting VS Community edition if installed on a machine with VS 2017 only even if it's Professional or Enterprise.
-  Several Cross-Platform templates fixes.


#### 4.3.0.738

-  Fixes issue trying to deploy to ARM Android emulator before it's ready.
-  Removes unsupported Master Detail templates from Visual Studio 2013.


#### 4.3.0.636

-  Fixed build signature error on iOS when signature file names are localized
-  Fixed bug on Android ARM emulator deployment
-  Fixed compatibility with newer C++ Android references
-  Fixed bug where logs were being lost on some circunstances
-  Fixed compatibility with Visual Studio 2017 (26127.03)
-  Filtered Unknown tasks in Android Logger
-  Made our setup not remove configuration from the registry on uninstall


#### 4.3.0.621

-  Use the standard folder browser dialog to choose the Java SDK, Android SDK and Android NDK paths.
-  Fixes typo on Login required message for SSH Mac connection.
-  Improvements on how the Host In Cloud dialog for the new templates is loaded.


#### 4.3.0.609

-  Fixed issue trying to Login with a Xamarin Account showing the following message: "Unhandled activation error. Cannot load machine data.".
-  Improvements on Xamarin Inspector.


#### 4.3.0.598

-  Some improvements on Xamarin.Forms Previewer integration.
-  Added 'default' option on 'Code generation target' for Binding Projects Application property page.
-  Resolved 'Frame not in module' issue while debugging some projects.
-  Can't open Mac Agent connection dialog on some non-US locales.
-  Error trying to add a new item to an Asset Catalog after deleting all its items.
-  New Icon types not being added to existing Asset Catalogs.
-  Extra new icon is created in existing "Message Extension icon" when a new "Message Extension icon" is added.
-  Integrated Xamarin Inspector as part of the Xamarin for Visual Studio Extension.
-  Surface error message when the user is trying to connect to a Mac not having an active session.


#### 4.3.0.550 (RC)

-  Fixes threading issues in our extension.
-  Missing property page for tvOS extensions.
-  Includes Xamarin Inspector integration (VS 2015+).
-  Templates now point to Xamarin.Forms 2.3.3.180.


#### 4.3.0.525

-  Fixes some Visual Studio 2013 Connectivity issues with the Mac.
-  Fixes issue making Device Log non-functional menu item in VS 2013 (This is a VS2015+ feature).
-  Path for IPA on Mac is incorrect in the Properties Window.
-  Trying to connect to a Mac with an older Xamarin.iOS error message doesn't show the Mac Agent dialog on double click.
-  Android Archive fails with an error trying to find mono-symbolicate.
-  "An error ocurred trying to load this page" opening iOS project properties not connected to the Mac.
-  Notify the user if Xamarin for VS cannot launch Android Emulator because elevation can be needed.


#### 4.3.0.490

-  Fixes an issue deploying Android apps when iOS and Android projects are configured as StartUp projects at the same time.
-  Adds support for Xcode 8.2.


#### 4.3.0.472

This XVS 4.3 alpha refresh includes fixes for the following issues:

-  Includes some fixes for the new cross-platform templates (preview).
-  CodeSigning profiles needed when building for the iPhoneSimulator solution platform.
-  Linker options appears duplicated in Linker Behavior property page.


#### 4.3.0.458

This XVS 4.3 alpha refresh includes fixes for the following issues:

-  It adds support for Visual Studio 2017 at the same time than VS 2013 and VS 2015.
-  Cleans up old Mac cache files.
-  Removes annoying repetitive toast for iOS Doc Sync.
-  Windows 7 issues with Dark theme on Generic PList editor causing some values to not being visible.
-  There is no Mac Agent icon for iOS Binding Library projects.
-  Removes GLKView from the F# Single View app template.
-  Properly generating mdb for device specific iOS builds.
-  Fixes connectivity issues with SSH on VS 2013.
-  Fixes background color of F# storyboard.
-  Includes new cross-platform templates (preview).


#### 4.3.0.405

This XVS 4.3 alpha refresh includes fixes for the following issues:

-  Adds support for AVD manager and SDK manager installed by Android Studio.
-  Missing component erros are now included as Build errors if detected trying to build for better discoverability.
-  Fixes wrong Java Max Heap Size guidance.
-  Allows Xamarin.Mac projects to build when using PCLs.
-  Adds Generic PList editor first preview.
-  Adds iOS Extensions Debugging support.
-  Updates Android Symbolication MSBuild property usage.


#### 4.3.0.254

Our first XVS 4.3 alpha refresh includes fixes for some known issues included on the first preview:

-  Fixed missing java folder making Xamarin Android Designer to not work in some environments.
-  Fixed issue loading some Android projects causing Visual Studio to hang.
-  This version included the stable cross-platform templates to avoid issues incuded on the one in progress. We'll include the updated templates in future previews.
-  Doesn't set focus on Mac Simulator while using Windows Remote Simulator.


###  <a id="knownissues"></a>
Known issues

#### Installing Xamarin for Visual Studio 2017

At this time, as a result of VS 2017 moving away from msi packaging toward utilization of the Visual Studio Installer system, Xamarin for Visual Studio 2017 is installed as part of the Visual Studio installer itself.
    For Visual Studio 2015/2013 you can use the XamarinVS MSI or the built-in updater.

#### Build canceled with error: Project ' *project_name*' requires the following components installed on your machine: ...

Building Android applications can require installing additional components. This can be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine.

Xamarin for Visual Studio 4.3 detects the lack of those missing resources, and  shows an error informing it requires to download and install them:

 ![](missingresources.png)

Double click on that error in the list to start downloading and installing the missing components.

 **Keep in mind that you need to have Intellisense errors visible in the list, otherwise you won't be able to see that error.**

If you try to build any project in the solution without installing the missing components, the build will be canceled. You cannot build without installing those components. Please ensure Intellisense errors are visible to be able to start installing them.

An optional way to install missing components is to build from the command-line.

#### Other Known issues

If you downgrade to Xamarin 4.2 or older versions after using XVS 4.3, you will need to re-register your known Mac servers in the Mac Server dialog. Please use the Forget Mac option, and configure your server connection again.

###  <a id="xvs4_3_1"></a>
Preview for Xamarin VS 4.3.1.

This preview includes the following fixes:

#### 4.3.1.39 (Beta / Alpha)

-  Android deployment fails if solution also contains a WiX project.
-  Deadlock opening some iOS projects.
-  Breakpoints won't hit on second-level PCL references.
-  Fixes iOS issue due to missing CodeSignNativeLibraries task.
-  Error opening storyboard after connecting to Mac server.
-  Android class library project should only include "Compile using Android Version" on Property page.
-  Visual Studio hangs when going to the "Tools->Options->Xamarin->Other" tab.


#### 4.3.1.2 (Alpha)

-  Updates Xamarin.Android SDKs.


#### 4.3.1.1 (Alpha)

-  Visual Studio hangs loading a cross-platform solution in some environments.
-  Microsoft.Csharp not referenced in VS Project Templates.
-  Cannot connect to Mac server if configured User Shell doesn't use `bash` syntax.
-  Submit to Test Cloud option missing (fixed on VS2013 and VS2015).
-  Debugger gets confused when Variable/Property name is same as Class name of something else.
-  Image set from asset catalog can't be renamed.
-  The 'Resources' folder is being forcibly hidden in watch Extension projects.
-  "Assets.xcasset" folder within "Resources" is not being hidden for tvOS projects.
