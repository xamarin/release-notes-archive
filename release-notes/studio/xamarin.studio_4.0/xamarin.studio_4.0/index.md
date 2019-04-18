---
id: 8A8AC5AA-1841-2BB1-C2AB-23D01ED9F86B
title: "Xamarin Studio 4.0"
---

##  <a name="14" id="14">Xamarin Studio 4.0.14</a>


This is a hot fix release.

 **iOS**

-  Fixes an issue parsing xcent files while using the Archive tool for users still using Xcode’s older than 4.4.1 


 **Android**

-  Fixes the designer for users with the Android SDK installed in C:\Program Files


 **General**

-  Add support for Xcode 5 Apple documentation merging.


##  <a name="13" id="13">Xamarin Studio 4.0.13</a>




This release contains many new features and bug fixes.

There were a number of themes for this release in addition
	to the regular bug fixing: Android Designer improvements, iOS
	7 support and improving Version Control.### Android Improvements



Many small tune ups and fixes to the Android designer.

Added support for Android Jelly Bean to the UI designer.

The Android Log Pad now supports filtering the data
	received from your Android device or simulator.  This should
	help users deal with all the information Android outputs.

Testflight support: Android users can now use
	Project->Publish to Testflight to publish their Android
	applications to TestFlight for distribution.### iOS Improvements: Automatic Configuration



Xamarin Studio got a big upgrade on its iOS capabilities on
	this release, matching the new features introduced in Xcode 5
	to simplify the development of iOS applications.

We start with an Account Manager that you use to track your
	Apple developer accounts (you can have multiple accounts and
	belong to multiple teams):<center>
	<img src="accounts.png">
	</center>



Xamarin Studio will automatically download any new
	provisioning profilers, app ids and certificates from the
	Apple Developer portal.

This simplifies the workflow when working with teams and
	you no longer need to use Xcode to do this synchronization for
	you.

Tasks that used to take a few trips to the iOS Developer
	portal are now possible by either editing
	your `Info.plist`

 file or your `Entitlements.plist`


	file.

When you edit your `Info.plist`

 file, you can now enable
	GameKit, configure background operation modes and provide data
	to the Maps app with a single click.  You no longer need to go
	back and forth between your project and the Apple Development
	Portal:<center>
	<img src="info.plist.png">
	</center>



It also now has support for specifying the new icon sizes
	introduced in iOS 7:<center>
	<img src="icons.png">
	</center>



The following features are also available when you add or
	edit the `Entitlements.plist`

 file which allows you to easily
	configure iCloud, Passbook, In-App Purchases, Inter-App Audio,
	Keychain and Data Protection.  Again, all within the IDE and
	removing the cumbersome back and forth with the Apple
	Developer portal:<center>
	<img src="entitlements.png">
	</center>

### iOS 7 Support: Asset Catalogs



 [Asset Catalogs are a new feature in iOS 7](https://developer.apple.com/library/ios/recipes/xcode_help-image_catalog-1.0/Recipe.html)

 that helps you
	organize your image and icon assets.

Asset catalogs can be useful to make sure that you ship all
	the assets that you need for all resolutions.   It starts with
	the simple manager for your own application icons (when you
	double click `info.plist`

 to edit your icons).   You can migrate
	your existing artwork easily from the IDE:<center>
	<img src="info-icons.png">
	</center>



And can also be used to manage your own collections of
	icons and image assets.    To manage your image assets, select
	"Add New File" on your project and select the "Asset Catalog"
	template:<center>
	<img src="asset-template.png">
	</center>



This will create an `Images.xcassets`

 folder in either the
	top-level folder (or within a Resources folder, depending on
	what you had selected in the Solution Tree). Within that `Images.xcassets`

 folder, there will be 2 other folders:
	AppIcons.appiconset and LaunchImages.launchimage. You can add
	more of these types of folders by right-clicking on the
	Images.xcassets folder and choosing Add -> New File which will
	sense that an asset catalog folder is selected and offer
	templates for AppIcons, LaunchImages, or Images (which will
	create the corresponding asset catalog subfolder).

Once you do that, you can then edit the `Contents.json`


	file, which will bring up the Asset Editor:<center>
	<img src="asset-editor.png">
	</center>



You can then drag and drop images into the individual tiles
	in your asset manager.

To load the images at runtime, merely use the asset name,
	like this:```
var image = UIImage.FromBundle ("Images");
```

### iOS 7 Support: Texture Atlases



iOS7 also
	introduce [Texture Atlases](https://developer.apple.com/library/ios/recipes/xcode_help-texture_atlas/AboutTextureAtlases/AboutTextureAtlases.html#//apple_ref/doc/uid/TP40013290-CH2-SW1)

 a mechanism used by developers to improve the
	performance of their application by combining multiple
	independent images into a single image.

To create Texture Atlases in Xamarin Studio, you just need
	to create a folder with a .atlas extension (for example
	"Textures.atlas"). Then fill this directory with the image
	textures that you want to compile into a texture atlas.

To load an image from the atlas, merely specify the name,
	and iOS 7 will load it for you from the atlas:```
var robot = SKSpriteNode.FromImageNamed ("robot.png");
```

### Version Control Updates



As mentioned previously, a big theme for this release was
	to fix many of the outstanding bugs and user interface
	problems in Version Control in Xamarin Studio.   Here are the
	major user visible changes:

Reduced the memory usage significantly (in particular for
	Git).

Blame view is now more compact for Git.

The Commit command and Review Changes have been squashed
	into the same handler. You can no longer directly invoke the
	Commit dialog by right clicking on a solution tree node.

Status View now allows diff copy-pasting.

Added a way to fix project/solution files that are in
	conflicted state. A right click option has been added.

Implemented Progress Monitoring for Subversion Commands.

Implemented cancelling of Version Control Checkout/Clone command.### Bug Fixes



iOS: Selecting a different device size will now affect the
	simulator size.

iOS: Fixed debugging when multiple devices are connected to
	the host.

iOS: Preseves [Outlet] property accessibility (public/private/protected) when syncing back from Xcode

Version Control: it now always properly initializes, not
	having issues with loading overlay icons on nodes anymore.

Version Control: Fixed issues with submodule update usage.

Version Control: Fixed many issues with wrong detection of
	repository type

Version Control: Fixed many issues with Subversion
	"Operation is in Progress".

Version Control: Fixed issues where localization was not
	culture invariant for stashes

Version Control: Fixed issues with Git pushing new branches
	to remote.### Debugger Improvements



Introduced a number of visualizers:-  Added a c-string visualizer for byte[] 
-  Added a hex visualizer for string, byte[] and char[] 
-  Added support for char[] to the default text visualizer 
-  Added basic code-completion support to the Immediate Window 


##  <a name="12" id="12">Xamarin Studio 4.0.12</a>


This is a hot fix release.

 **Fixes**

-  Allow Android projects to be opened that could not be opened in previous releases.
-  Allow iOS projects to be debugged with more than one iOS device attached.


##  <a name="11" id="11">Xamarin Studio 4.0.11</a>


 **General**

-  Improved speed & memory usage


 **Source code editing**

-  Format items in strings now are highlighted and get completion
-  Improved parsing error recovery (completion is now much less likely to break while typing)
-  Reworked completion options
-    
-  Automatic bracket insertion for methods and constructors
-  Completion list may now contain items from other namespaces and import them
-  Usage highlighting has now indicators if a usage is changing the value or not
-  New message bubble design
-  Improved speed & memory usage


 **Version Control**

-  Added support for Subversion 1.7.
-  Improved user experience with Subversion commands.
-  Revert on Project/Solution nodes no longer recursively reverts containing items.
-  Added support for adding and removing items from ignore lists.
-  Improved user experience with committing and updating.
-  Fixes to Subversion Log view when handling items which have been deleted/added in the selected revision
-  Fixes to Subversion Blame view regarding line numbers.
-  Fixed Git merging/rebasing to a remote branch.
-  Files opened in the IDE are automatically reloaded after doing a version control update.
-  Git Checkout will now also clone submodules
-  Git branches with invalid names can no longer be created.
-  The version control Remove command no longer deletes the files from disk, only removes them from the repo.
-  Review Changes will now update itself, not open another tab if it’s used on the same node.
-  It is possible to copy-paste diffs from the Log Widget.
-  A warning is now shown when trying to commit unsaved files.


 **Android**

-  Fixed several performance and rendering issues in the designer


 **NUnit**

-  The tests pad now shows results from previous runs


##  <a name="10" id="10">Xamarin Studio 4.0.10</a>


 **Text Editor**

-  Mac menu should no longer update with each keystroke.
-  Added proper new line support.


 **Debugger**

-  Added an icon to represent variables in the debugger
-  Fixed debugger tooltips for multi-level properties
-  Fixed debugger tooltips for class members when used in methods


 **iOS**

-  Set the minimum OS version for new projects to 6.0
-  Added the ability to enable the Incremental Build feature added in Xamarin.iOS 6.3.7 from project options. 
-  When the Incremental Build option is enabled, we will now only compile the assemblies that were modified, and only upload the delta. Notice that when using incremental builds, the resulting binary must be connected to your Mac. Binaries compiled with the incremental support are not able to run when your device is unplugged.


##  <a name="9" id="9">Xamarin Studio 4.0.9</a>


 **General**

-  Global performance improvements when building solutions with many projects.
-  Fixed loading of projects with wildcards on Windows
-  Build errors and warnings are not accumulated anymore between builds


 **Source code editing**

-  Fixed several issues when editing HTML files.
-  Improvements in the vi editing mode


 **Debugger**

-  It is now possible to add and remove watch expressions to the Watch window even while not debugging. 
-  Fixed debugger tooltips for ‘value’ in property setters and for method parameters with default values. 
-  Adding and removing breakpoints should always work now.


 **Android**

-  New editor for AndroidManifest.xml
-  Added command for opening the Android SDK manager
-  Fixed several designer loading issues


 **iOS**

-  When using Xcode integration, the automatically generated Outlets and Actions are now sorted alphabetically when the corresponding .designer.cs file is generated. This will help minimise modifications to the .designer.cs file. 
-  When generating Objective-C headers to be synced out to Xcode, the #import statements are now based upon the types referenced in the file rather than being hard-coded. 
-  Fixed parsing of Outlets as @interface members when re-importing Objective-C headers. 
-  Fixed the Info.plist parser to handle ‘&lt;array&gt;&lt;/array&gt;’ as opposed to the typical ‘&lt;array/&gt;’ syntax for empty arrays. 
-  Now avoids importing Xcode’s temporary build files & directories if the user has chosen to output these files into their Xcode project directory. 


 **NUnit**

-  Added Debug Test command in the context menu of the test tree.


##  <a name="8" id="8">Xamarin Studio 4.0.8</a>


This is a hot fix release for Xamarin Studio.

This release removes a NullReferenceException when running mdtool
  to clean a solution from the command line.

##  <a name="7" id="7">Xamarin Studio 4.0.7</a>


This is a hot fix release for Xamarin Studio.

This release adds critical improvements to the Updater service.

##  <a name="6" id="6">Xamarin Studio 4.0.6</a>


This is a hot fix release for Xamarin Studio.

 **Documentation browser**

With this Xamarin Studio release, the included documentation browser
will correctly process newer documentation from Apple.

 **Android Designer**

Fixes to layout loading and other improvements.

 **General**



The Find in File functionality in the editor has been improved as well.##  <a name="5" id="5">Xamarin Studio 4.0.5</a>


 **General**

-  Added support for file wildcards in project files (for example, to include all files in a directory).
-  Added initial support for arbitrary project dependencies. There is no user interface for defining them, but dependencies set using Visual Studio will be honored.
-  Fixed issue that caused solutions to be duplicated in the solution tree when opening directly from the file explorer.
-  Project folders can now be expanded/collapsed with double-click.
-  Global search now returns commands which are specific to the current selection.
-  Improved behavior of "build before run" option. Instead of building the whole solution, we just now build the startup project and any dependency of that project.


 **Source code editing**

-  Gutter font can now be changed
-  New smart tag system for code actions
-  Namespaces can now be renamed and find namespace references works now
-  VI mode status area has now a line, column indicator
-  Resolve namespace imports can now fix project references


 **Activation**

-  Improved trial experience
-  Fixed a potential issue that could cause multiple activations to be used up by the same machine


 **Components**

-  Added support for component trials
-  Improved rendering of component documentation
-  Component samples that Xamarin Studio cannot open are now greyed out


 **Debugger**

-  Fixed issue where Xamarin Studio would sometimes fail to debug apps in the Simulator
-  Improved Breakpoint Hit Count functionality to support all of the functionality that Visual Studio provides (and more!)
-  Improved Breakpoint Pad to allow multi-selection
-  Allow users to search in the Call Stack Pad in the debugger
-  Added support for dragging & dropping code snippets from the Text Editor into the debugger’s Watch Pad
-  Many other fixes to the debugger


 **Android**

-  Fixed several issues when loading layouts in the Android Designer.
-  Fixed file locking issues in the Android Designer
-  Fixed PCL support for Xamarin.Android projects
-  Fixed issue where Xamarin Studio would launch the wrong Simulator from the drop-down menu


 **iOS**

-  Allow adding 22x29, 44x58, 64x64 and 320x320 icons to Document Types in Info.plists for iOS projects
-  Fixed some bugs in USB debugging for iOS projects
-  Fixed the UIStatusBar section of the Info.plist editor in iOS projects
