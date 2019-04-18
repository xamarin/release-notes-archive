---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.4"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.4</a>


This Xamarin for Visual Studio 4.4 release updates [Xamarin.iOS 10.8](/releases/ios/xamarin.ios_10/xamarin.ios_10.8/) and [Xamarin.Android 7.2](/releases/android/xamarin.android_7/xamarin.android_7.2/) releases.

###  <a id="bugfixes"></a>
Bug fixes.

This release includes the following fixes:

-  iOS Extension apps fail to build with error "cannot read Entitlements data". **(4.4.0.31)**
-  Includes symbols for Watson reports. **(4.4.0.6)**
-  Android deployment fails if solution also contains a WiX project. **(4.3.1.39)**
-  Deadlock opening some iOS projects. **(4.3.1.39)**
-  Breakpoints won't hit on second-level PCL references. **(4.3.1.39)**
-  Fixes iOS issue due to missing CodeSignNativeLibraries task. **(4.3.1.39)**
-  Error opening storyboard after connecting to Mac server. **(4.3.1.39)**
-  Android class library project should only include "Compile using Android Version" on Property page. **(4.3.1.39)**
-  Visual Studio hangs when going to the "Tools->Options->Xamarin->Other" tab. **(4.3.1.39)**
-  Visual Studio hangs loading a cross-platform solution in some environments. **(4.3.1.1)**
-  Microsoft.Csharp not referenced in VS Project Templates. **(4.3.1.1)**
-  Cannot connect to Mac server if configured User Shell doesn't use `bash` syntax. **(4.3.1.1)**
-  Submit to Test Cloud option missing (fixed on VS2013 and VS2015). **(4.3.1.1)**
-  Debugger gets confused when Variable/Property name is same as Class name of something else. **(4.3.1.1)**
-  Image set from asset catalog can't be renamed. **(4.3.1.1)**
-  The 'Resources' folder is being forcibly hidden in watch Extension projects. **(4.3.1.1)**
-  "Assets.xcasset" folder within "Resources" is not being hidden for tvOS projects. **(4.3.1.1)**


###  <a id="knownissues"></a>
Known issues

#### Object reference not set to an instance of an object building iOS projects.

This is a random issue which is being investigated. If your iOS build fails with this message on the CodesignNativeLibraries Task, please try to rebuild your solution, as this is not a consistent build failure.

#### Installing Xamarin for Visual Studio 2017

At this time, as a result of VS 2017 moving away from msi packaging toward utilization of the Visual Studio Installer system, Xamarin for Visual Studio 2017 is installed as part of the Visual Studio installer itself.
    For Visual Studio 2015/2013 you can use the XamarinVS MSI or the built-in updater.

#### Build canceled with error: Project ' *project_name*' requires the following components installed on your machine: ...

Building Android applications can require installing additional components. This can be needed in several cases, like if you're using a new component, NuGet Package, or if it's the first Xamarin.Forms solution you're building on a given machine.

Xamarin for Visual Studio detects the lack of those missing resources, and  shows an error informing it requires to download and install them:

 ![](missingresources.png)

Double click on that error in the list to start downloading and installing the missing components.

Please keep in mind that you need to have Intellisense errors visible in the list, otherwise you won't be able to see that error.

If you try to build any project in the solution without installing the missing components, the build will be canceled. You cannot build without installing those components. Please ensure Intellisense errors are visible to be able to start installing them.

An optional way to install missing components is to build from the command-line.

#### Other Known issues

If you downgrade to Xamarin 4.2 or older versions after using this release, you will need to re-register your known Mac servers in the Mac Server dialog. Please use the Forget Mac option, and configure your server connection again.
