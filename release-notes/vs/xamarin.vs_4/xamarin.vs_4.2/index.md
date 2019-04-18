---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.2"
---

##  <a name="0" id="0">Xamarin for Visual Studio 4.2</a>




This Xamarin for Visual Studio 4.2 release updates

 [Xamarin.iOS 10.2](/releases/ios/xamarin.ios_10/xamarin.ios_10.2/)

 and [Xamarin.Android 7.0](/releases/android/xamarin.android_7/xamarin.android_7.0/)

 releases. and includes several new features:

-  [Android Archive Manager and Publishing](#publishing)
-  [Integrated iOS/Android device log.](#devicelog)
-  [Xamarin.Mac minimum support.](#xammac)
-  [Remote iOS Simulator Preview](#iossimulator)
-  [Other changes and Bug Fixes.](#bugfixes)


###  <a id="publishing">Android Archive Manager and Publishing</a>


We're introducing a new Archive Manager for Android in Visual Studio. It allows you to keep track of your App apk files, signing, re-signing and publishing to **Google Play** directly from your IDE. You can open the **Archive Manager** with the **Tools - Archive Manager** menu option. Archive an Android project by right clicking on the project node in **Solution Explorer** and select **Archive**. (This command is also available under <span class="UIItem">Build &gt; Archive</span>.) The new **Archive** command replaces the old <span class="UIItem">Build &gt; Export Android Package (.apk)</span> and <span class="UIItem">Tools &gt; Android &gt; Publish Android App</span> commands.

 ![](archivemanager.png)

It includes an Android Key Manager, which keeps track of your keys making easier to add, delete or reuse an existing key.

 ![](createandroidkey.png)

Apps can be saved with the Ad-Hoc channel, or published to Google Play. For publishing to Google Play, the app should be manually uploaded to the Google Play site at least the first time. This requirement can be fulfilled creating an Ad-Hoc publishing package and upload it that very first time.

 ![](googleplay.png)

###  <a id="devicelog">Integrated iOS/Android device log.</a>


This release enables keeping track of your iOS device log from Visual Studio while connected to the Mac. This is a new feature that is only supported on **Visual Studio 2015 or newer** version.

 ![](devicelogios.png)

We're also integrating Android device log into this new Tool Window for a consistent experience.

 ![](devicelogandroid.png)

It's required to have a Xamarin iOS or Android project open to use this new feature, and have the device already detected in the devices dropdown.

 **Known issue:** We strongly recommend to update Visual Studio 2015 to the latest version (Update 3 or higher) for the best results. Older versions of Visual Studio 2015 (such as VS 2015 Update 1) render the integrated iOS/Android device log inefficiently, causing the UI to become non-responsive until all the log lines have been read.

###  <a id="xammac">Xamarin.Mac minimum support.</a>


Xamarin for Visual Studio has gained minimum support for Xamarin.Mac. This release enables Visual Studio to load and recognize Xamarin.Mac projects as supported. However, this minimum support allows only to build Xamarin.Mac projects without using the native Mac tool chain. The build process is performed locally on Windows, generating IL assemblies that cannot be used for running or debugging apps, and it doesn't create application bundles.

 ![](xamarinmac.png)

###  <a id="iossimulator">Remote iOS Simulator Preview</a>


The new simulator remoting feature allows you to launch and debug iOS applications directly on Windows. As this is a preview feature, it must be enabled using the new option in the `iOS Settings` section of the Visual Studio settings. This setting will only be visible when the remoted simulator has been installed.

 ![](ios_sim_settings.png)

Once it has been enabled, Visual Studio will launch the simulator on Windows instead of launching Apple's simulator on the Mac whenever you launch or debug your application.

 ![](sim.png)

<div class="note"><p><strong>Note:</strong> For Xcode 8 compatibility be sure to update the Remote iOS Simulator Preview to version <a href="https://releases.xamarin.com/preview-ios-simulator-for-windows-update-4/">0.10.0.5</a> or newer.</p></div>

For the full list of features and known issues, please visit our documentation page: https://developer.xamarin.com/guides/cross-platform/windows/ios-simulator

### ###  <a id="bugfixes"></a>
Other changes and Bug fixes



#### XVS 4.2.2.11

-  Bumps X.Forms templates to 2.3.3.180.
-  Fixes a crash on Xamarin Designer caused by an old XWT version.
-  Includes a Xamarin.iOS fix for build error "MTOUCH: error MT3001: Could not AOT the assembly..."


#### XVS 4.2.2.6

-  Adds Designer support for Xcode 8.2.1.


#### XVS 4.2.2.3 (Beta)

-  Bumps Cross platform templates to use Xamarin.Forms 2.3.3.175.
-  Adds minimal support for Xamarin.Mac projects referencing PCLs.


#### XVS 4.2.1.73 (Cycle 7 SR1 + Xcode 8.2)

-  Adds support for Xcode 8.2.
-  Updates default Cross platform templates to use Xamarin.Forms 2.2.0.45


#### XVS 4.2.1.62

-  Ensures application rebuilds with Profiler support if profiler is enabled.
-  Fixes issue deploying applications on iOS Simulator with VS 2013.


#### XVS 4.2.1.57

Fixes on top of 4.2.1.15 fixes:

-  Fixes Visual Studio crashing while disposing SSH Client.
-  Build error caused by 'Failed to read file attributes for "/Users/admin/Assets.xcassets"'.
-  'Launch Failed' issue trying to debug on iOS devices.
-  Fixes disconnection with Mac server caused by a compatibility issue related to modified times.
-  Allows launching iPhone/iPod apps on iPad devices.
-  Fixes error building with VS 2015 Update 3 and msbuild property IpaPackageDir is defined and custom solution profile.
-  Improved WatchOS project build process.
-  Added support for Xcode8.1
-  Issue updating Xamarin from Visual Studio when username contains special characters.


#### XVS 4.2.1.15

Fixes:

-  Issue saving iOS App Icons.
-  Import existing Android Keystore fails. Fields for "Password" and "Key Password" are swapped.
-  Cannot debug on device (iOS) Xamarin Forms app.
-  Selecting a file via the file browser for Custom entitlements delets the selected file.
-  Start button has no device list available.
-  Native References in iOS Binding projects do not build in VS.
-  "Could not install package..." error adding a new Xaml page into a Xamarin.Forms shared project.
-  Enititlements view doesn't save changes in plist file.
-  Unable to open Main.axml file in VS.
-  Android Designer with Custom Controls spins loading bar.
-  Two "Xamarin Mac Agent" dialog open automatically.
-  User is not getting "Top Shelf Image Wide" under Assets catalogs for tvOS.
-  Game Controller checkbox settings not remembered on tvOS.
-  Cannot load a new Android F# Blank App.
-  Unable to deploy to iOS 7.x devices.
-  Error on "iOS Build" page if not connected to a Mac.
-  Android Archive Manager and Distribution enhancements: -   Wizard path is now clickable.
-   Key details (accessible by double clicking on items) now include Key Path.


 


#### XVS 4.2.0.719

-  Adds support for Xamarin.iOS 10.2 and Xcode 8.1.


#### XVS 4.2.0.703

Fixes:

-  Improvements to avoid "Xamarin Android Projects are incompatible" or other Package loading issues due to broken Visual Studio MEF Component Cache.


#### XVS 4.2.0.695

Fixes:

-  Android: Debug deploy always fails: ZipException: Entry has been changed.
-  Run in Test Cloud context menu item missing.


 **Known issues:**

-  Android Distribution Wizard: Once you've selected a channel for your project, the Wizard will start always on that channel. If you want to change the channel, you'll need to press 'Back' to navigate to the Channel Selection step.


#### XVS 4.2.0.688 (Beta)

Fixes:

-  "GetFullVsVersionString must be called on the UI thread" when attempting to open "Manage NuGet Packages for Solution" on certain systems.
-  Selecting a file via the file browser for "Custom entitlements" _deletes_ the selected file from the file system rather than selecting it.
-  iOS Allow codesigning Simulator builds without the need of a developer certificate.
-  Google Play Publishing wizard fails after client id/secret are entered.


 **Known issues:**

-  Android Distribution Wizard: Once you've selected a channel for your project, the Wizard will start always on that channel. If you want to change the channel, you'll need to press 'Back' to navigate to the Channel Selection step.
-  "Run on Test Cloud" context menu option for UI Test projects is missing on this Release. It will be back in our next build.


#### XVS 4.2.0.680

-  Fixed .msi issue making installation to rollback before finishing.
-  **Intentional restriction:** "This version does not have support for files saved in Xcode 8 format." appears when attempting to use the Xamarin iOS Designer on a storyboard that has been saved in Xcode 8. Support for Xcode 8 storyboards will be added in a future version of the iOS Designer. -  **Workaround**  : Open the storyboard once more in Xcode 8, and then under the storyboard properties change  <span class="UIItem">Opens In</span>  to  <span class="UIItem">Xcode 7.x</span>  . After that use only the Xamarin iOS Designer to edit the storyboard.
-  **Alternate workaround**  : Avoid using the Xamarin iOS Designer for now and instead use only Xcode 8 to edit the storyboard.


 
-  **Known issues:**
-       
-  [43566](https://bugzilla.xamarin.com/show_bug.cgi?id=43566) - The iOS Designer initialization process will cause any running iOS 10 simulator to become non-responsive. The designer initialization happens when opening an iOS project in Xamarin Studio and during the connection to the remote Mac in Visual Studio. This issue does _not_ affect Xcode 7.3, iOS 9.3 (and lower) simulators. -  **Workaround**  : Quit and restart the simulator after the designer has initialized. You can then proceed to use the simulator again as normal.


 
-  [44108](https://bugzilla.xamarin.com/show_bug.cgi?id=44108) - "Can't load AMD 64-bit .dll on a IA 32-bit platform" when attempting to open .axml layout files that use custom controls. The fix for this bug will provide a fallback that skips rendering of custom controls (as in earlier versions of Xamarin) when using a 32-bit JDK. -  **Optional fix**  : Install a 64-bit version of the Java JDK, and then ensure it is selected under  <span class="UIItem">Tools &gt; Options &gt; Xamarin &gt; Android Settings &gt; Java Development Kit Location</span>  . This will enable the new  [custom controls support](#Android_Designer)  .


 
-  [Upstream non-standard behavior of NuGet Package Manager extension](https://github.com/NuGet/Home/issues/3419) (Xamarin tracking bug  [44146](https://bugzilla.xamarin.com/show_bug.cgi?id=44146) ) triggered by XamarinVS 4.2 - "GetFullVsVersionString must be called on the UI thread" error appears when attempting to open  *Manage NuGet Packages for Solution* , blocking the use of the NuGet package manager on certain systems -  **Temporary workaround**  : Install  [this small extension](https://visualstudiogallery.msdn.microsoft.com/77ffcb6d-3d94-47fa-8259-3112efac0a3e)  from the Xamarin VS team that will force the NuGet Package Manager to load before the Xamarin extensions.
-  **Alternate temporary workaround**  : Before opening any projects, open  *Tools &gt; NuGet Package Manager &gt; Package Manager Settings*  to force the NuGet Package Manager extension to load before the Xamarin extensions.


 
-  [44273](https://bugzilla.xamarin.com/show_bug.cgi?id=44273) - "An error occurred trying to load the page." appears in the  <span class="UIItem">Project Properties &gt; iOS Build</span> tab if Xamarin for Visual Studio is not connected to a Mac. -  **Workaround**  : Connect Xamarin for Visual Studio to a Mac, and then close and reopen the project properties.


 
-  Installing XVS 4.2.x into Visual Studio "15" Preview versions is not yet officially supported due to significant changes in how VS "15" installs extensions. -  **Workaround**  : For now, continue to use the XVS 4.1.x version that is installed by the Visual Studio "15" Preview installer.


 


#### XVS 4.2.0.675

-  Fixes issue preventing selection of iOS Simulator in device dropdown if VS is not connected to Mac Build Host.
-  Android NDK path is not automatically recognized by XVS if installed with Visual Studio 15.
-  Improved tracing for connectivity with Mac host.
-  Mac connectivity reliability fixes.
-  Android AvdWatcher integration logic now includes ANDROID_SDK_HOME environment variable.
-  Fixes always disabled Android Pro Guard option.
-  Fixes Android Archiving issue with Symbolication.


#### XVS 4.2.0.628

-  Improved Visual Studio and Mac SSH connectivity.
-  Uses Visual Studio Xaml intellisense for Xamarin.Forms intellisense in VS 2015+
-  Avoid failing detecting Jave if it's installed by Visual Studio setup.
-  Implements HttpClient selector for Android projects in Propertie pages.
-  Improvements on Visual Studio loading times.
-  Avoids to show warning if Xamarin Android Player is not installed.
-  Added additional launch arguments support for Android Emulator.
-  Cleans up iOS simulator list when disconnected from Mac server.


#### XVS 4.2.0.584

-  Adds missing cross-platform templates if Visual Studio 2012 is installed.
-  Fixes Intermittent VS disconnection from Mac while working on iOS application.
-  VS getting hang when Forms Previewer is open and user Build or Rebuild the project.
-  Fixes mispelling on DesignerAction elements.
-  Allows back period characters in iOS assembly names.
-  Fixes "No device operating system information found." error building iOS application creted on Mac XS.
-  Resolves issue getting error when iOS application launch on device.
-  Fixes code generation issue with iOS Designer.
-  Fixes issue not getting 'Managed Virtual Devices' option under Tools-Android with VS.
-  Forms Preview not reflecting changes on .xaml after building the project.
-  Fixes hangs on VS2015 builds.
-  Resolves issue with XCode8 Beta 6, not getting simulator for WatchKit OS1 in device dropdown.
-  Fixes iOS Designer not loading on VS 2012 and VS 2013.


#### XVS 4.2.0.508

-  Adds  [Xamarin.Mac minimum support.](#xammac)
-  Fixes issue building watchOS projects with Device config.
-  Fixes issue causing menu items not showing up until a Xamarin Project is loaded.
-  Adds Comments and VersionCode to Archives in Archive Manager.
-  Fixes issue making Visual Studio unable to reconnect with same Mac once disconnected in some environments.
-  Metal game iOS template now displays properly on device.
-  Fails explicitly if Android Key Store password is incorrect.
-  Fixes simulator not showing up with WatchKit application.
-  Enables Android AOT and LLVM options in Release Configuration.
-  **Known issues:**
-   
-  Cross-platform templates are not installed if Visual Studio 2012 is installed. To workaround the issue, just download and install this  [patched VSIX](http://xvs.xamarin.com/builds/bug43445/Xamarin.Forms.Templates.VisualStudio.0.5.34.vsix) (to be included in the next drop).


#### XVS 4.2.0.378

This build includes:

### New Project templates

Xamarin VS now includes a new template for creating a TV Services Extension.

Audio Unit Extensions.

### iOS Asset Catalog Updates

We've extended the Asset Catalog support to include:

-  Vector Image assets.
-  Complications assets.


###  <a id="androiddesignercustomcontrols">Android Designer</a>


 *Because of an Android upstream issue, support for rendering API 24 is not available in this release*

 **Custom controls support**

The Android designer now supports loading both Java-based and .NET based custom controls referenced in layout files.

Custom controls can be edited like any other control in the property panel, including custom properties defined in a `<declare-styleable />` resource entry of the same name. You can also drag and drop them directly from the toolbox where two new categories, *Custom Controls* and *Support Libraries*, have been added for convenience.

<div class="note"><p><strong>⚠️ Warning:</strong> as the designer runs in a constrained Android environment, your custom control code may or may not work as it does on a real device or emulator. You can use the <a href="https://developer.xamarin.com/api/property/Android.Views.View.IsInEditMode/">IsInEditMode</a> property to detect if your view is being rendered in the designer and dynamically adapt its behavior for the restricted designer environment.</p></div>

#### XVS 4.2.0.21

-  Changes enabling Open Sourcing of Xamarin.iOS and Xamarin.Android.
-  Simplified licensing checks, making any Xamarin License to prevail over running VS SKU.
-  **Known issues:**
-    
-  "Unable to connect to Address='192.168.1.2:22' with User='macuser'" or "Private key is encrypted but passphrase is empty." after downgrading back to the previous version Xamarin 4.0. This is an  *intentional* change due to a new security feature in Xamarin 4.1.  **Recommended fix** : Delete  **id_rsa** and  **id_rsa.pub** from  **%LOCALAPPDATA%\Xamarin\MonoTouch** , and then reconnect to the Mac build host.
-  After installing this version, connecting to the Mac might ask for Mac credentials once, even if it's a known Mac.
-  **New Requirements for iOS Designer:**
-  <u>Only if Visual Studio 2015 is not installed</u> on the same machine, and for using the iOS designer on Visual Studio 2012 or 2013, the following products are required:
-    
-  [Microsoft .Net 4.6.](https://www.microsoft.com/en-us/download/details.aspx?id=48137)
-  [Microsoft MSBuild Tools 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48159)
