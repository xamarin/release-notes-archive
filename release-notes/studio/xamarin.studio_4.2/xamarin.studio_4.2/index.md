---
id: DB7C60FE-5E81-4849-8C78-75CD49B0CC9B
title: "Xamarin Studio 4.2"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_4/xamarin.studio_4.2"></head><body>
  
  

 
<h2><a name="5" id="5">Xamarin Studio 4.2.5</a></h2>

<p>The 4.2.5 update fixes the Android designer for users who have upgraded to Android SDK Tools 22.6.3.</p>

<h2><a name="4" id="4">Xamarin Studio 4.2.4</a></h2>

<h3>Project Management</h3>
	<ul>
		<li>Added new Project Unload command, which can be used to disable a project in a solution.
		To unload a project, right-click on the project in the solution pad and click on Unload.
		An unloaded project will remain disabled until it is explicitly loaded using the Reload command.</li>
		<li>Improved roundtripping of ProductVersion/ToolsVersion in project files, for better compatibility with Visual Studio.</li>
		<li>Improved the naming convention configuration dialog.</li>
	</ul>
<h3>Debugger</h3>
	<ul>
		<li>Correctly compare null values in the evaluator.</li>
		<li>Fixed loading of strings into the hex editor visualizer.</li>
		<li>Don't scroll to the top when adding new expressions/watches.</li>
		<li>Several improvements to the Win32 debugger engine. Immediate window now offers auto-completion.</li>
	</ul>
<h3>iOS</h3>
	<ul>
		<li>Project templates based on the old Xib format have been removed. All project templates ('iPad', 'iPhone' and
'Universal') are now based on storyboards. They work exactly as they did before.
The single file Xib templates are all still there, except the Xib files in the
single file templates have been upgraded to Xcode 5 format. This means that
they cannot be opened/used/compiled with Xcode 4.x. The single file templates
should also act exactly as they did before, but they will only work with Xcode
5.0 or higher.</li>
		<li>The iOS Designer preview is now shipping on every version of Xamarin Studio. Users interested in using the built-in designer to edit their storyboard files should enable in the Xamarin Studio preferences dialog.</li>
		<li>Added prerendered checkbox in the Asset Catalog editor for App Icons.</li>
		<li>Added support for simulating a background fetch (no support for launching as a background fetch yet).</li>
		<li>Fixed the iTunes Art work selectors to work after unsetting the image.</li>
		<li>Moved the WiFi debugging checkbox out of the Debugger preferences panel and into a new iOS preferences panel.</li>
	</ul>
<h3>GIT</h3>
	<ul>
		<li>Added command for converting a stash to a branch. To use this feature, access Version Control -> Manage Stashes -> Convert to branch.</li>
		<li>Improvements in the Checkout dialog. When the target checkout directory is not empty Xamarin Studio now ask whether to delete the contents or not.</li>
		<li>Fixed some e-mail overriding issues in the commit dialog.</li>
	</ul>
<h3>Source Code Editing</h3>
	<ul>
		<li>Improved text editor performance and memory usage, especially on Windows or when working with large C# files.</li>
		<li>New code issues:</li>
		<ul>
			
			
			
		</ul><li>Field never assigned</li><li>Usage of obsolete members</li><li>Check that event handlers got removed from static events to prevent memory leaks</li>
		<li>Added smart indentation support for .json files.</li>
	</ul>
<h3>Android Designer</h3>
	<ul>
		<li>Added support for Android KitKat (with Android SDK tools 22.3 or upper).</li>
		<li>Fixed crash when trying to add a .cs file to the Android layouts folder.</li>
		<li>Fixed: button for deleting alternative layouts in the Android designer can’t be clicked.</li>
		<li>Fixed random crashes when opening an axml file.</li>
	</ul>
<h3>Other improvements and bug fixes</h3>
	<ul>
		<li>The NUnit addin now recognizes the ‘Explicit’ attribute</li>
		<li>Web service references now show map and proxy file as their children</li>
	</ul>
<h3>Known issues</h3>
  <p>Documented <a href=" https://bugzilla.xamarin.com/buglist.cgi?query_format=advanced&bug_status=NEW&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=IN_PROGRESS&bug_status=NEEDINFO&">here</a></p>


<h2><a name="3" id="3">Xamarin Studio 4.2.3</a></h2>

<h3>4.2.3.60 Update</h3>
<p>The 4.2.3.60 update fixes the Android designer for users who have upgraded to Android SDK Tools 22.6.</p>
<p>4.2.3.60 requires the updated Android SDK Tools 22.6 to use the Android Designer, and will prompt you to upgrade if you are on an older version.</p>

<h3>Source Editing</h3>
	<ul>
		<li>Fixed performance issue when opening very large files</li>
		<li>Fixed excessive CPU usage in some cases</li>
		<li>Added support for detecting simplified chinese encoding</li>
		<li>Improved automatic code formatting</li>
		<li>Code Issues Pad now supports File and Project grouping</li>
	</ul>
<h3>Razor and Hybrid applications</h3>
	<ul>
		<li>Added new templates for Razor Hybrid applications. These are new project types for Android and iOS (Storyboard) which use a WebView (through a Razor Preprocessed template).</li>
		<li>Preprocessed Razor templates now support conditional attributes</li>
	</ul>
<h3>Projects</h3>
	<ul>
		<li>Add support for local-copying package assembly references</li>
		<li>Added support for reading projects created by Visual Studio 2013. However, they can currently only be built on Windows, not Mac.</li>
		<li>Moved the ‘Use MSBuild engine’ option to the Build panel for Projects</li>
	</ul>
<h3>Debugger</h3>
	<ul>
		<li>Improved the Exception Caught dialog</li>
		<li>Implemented support for evaluating null references in the Immediate and Watch windows.</li>
	</ul>
<h3>iOS</h3>
	<ul>
		<li>There are now a total of 6 new Project Templates for iOS:</li>
		<ul>
			
			
			
			
			
			
		</ul><li>iPhone Page-Based Storyboard</li><li>iPad Page-Based Storyboard</li><li>Universal Page-Based Storyboard</li><li>iPhone SpriteKit Storyboard</li><li>iPad SpriteKit Storyboard</li><li>Universal SpriteKit Storyboard</li>

		<li>When zipping an app bundle, Xamarin Studio now prompts for the output filename <b>before</b> building (in cases where the app bundle hasn’t yet been built).</li>
		<li>Added refresh button to the Developer Accounts’ “View Details” dialog.</li>
		<li>Fixed the Developer Portal web requests to better handle error cases that have been reported on the forums and to the Support Team.</li>
		<li>Fixed accuracy of the “Signing Identities” list in the Developer Accounts’ “View Details” dialog.</li>
		<li>Always loads mobile provisioning profiles from ~/Library/MobileDevice/Provisioning Profiles/ so that developers are able to manually install their own provisioning profiles (and/or manage their Provisioning Profiles using Xcode) instead of using the Developer Accounts feature.</li>
		<li>Improved merging of the Asset Catalog plists in order to preserve the UIPrerenderedIcon settings in the app’s Info.plist.</li>
		<li>Now exports Asset Catalogs to Xcode when editing xib and storyboard files.</li>
		<li>When syncing back from Xcode, Outlets and Actions are now parsed from both the .m and .h files (since Xcode5 now seems to default to displaying the .m file in the side-by-side editor view).</li>
	</ul>
<h3>Mac</h3>
	<ul>
		<li>Allow building without specifying a Provisioning Profile.</li>
		<li>Fixed code-signing to not merge the Keychain Access Groups entitlement from the specified Provisioning Profile.</li>
		<li>Fixed the “Downloads” File Access checkbox to set the proper Entitlements.plist key.</li>
	</ul>
<h3>Android</h3>
	<ul>
		<li>Allow targeting the Android KitKat framework</li>
		<li>Android Designer</li>
		<ul>
			
			
			
			
		</ul><li>Fixed several issues with string resources</li><li>Allow using uppercase letters in resource folders</li><li>Added command in context menu for showing the property pad</li><li>Added context menu options for creating and deleting alternative layouts</li>
	</ul>
<h3>Web References</h3>
	<ul>
		<li>Added possibility to choose visibility for generated proxies.</li>
		<li>Fixed issues with proxy namespace generation when URLs contained dashes</li>
	</ul>
<h3>Version Control</h3>
	<ul>
		<li>Fixed issues with Keychain storage for Git.</li>
		<li>Added a way to disable Version Control per solution basis. It is accessed by right clicking a solution -> Options -> Version Control -> General -> ticking the Disable Version Control for this Solution.</li>
		<li>Updated Windows Subversion to 1.8.</li>
		<li>Fixed entries in Commit Dialog being doubled</li>
	</ul>
<h3>Miscellaneous bug fixes and improvements</h3>
	<ul>
		<li>The status bar now displays the relative path of the opened file</li>
		<li>Fixed: all menu items are disabled when Xamarin Studio is in fullscreen mode</li>
		<li>Fixed: changing desktop wallpaper causes UI misbehavior</li>
		<li>Disabled Add-ins are no longer re-enabled after Xamarin Studio Upgrade</li>
		<li>Fixed error adding references to iOS/Android projects using Indie/Starter edition</li>
		<li>Fixed memory leak caused by the code completion database</li>
	</ul>




<h2><a name="2" id="2">Xamarin Studio 4.2.2</a></h2>
<ul>
    <li>Re-added a fallback to the XCode database for provisioning profiles. You will no longer be required to log into your Apple developer account in Xamarin Studio unless you are using entitlements.</li>
    <li>Fixed Subversion support on Mavericks.</li>
    <li>Fixed an issue seeing some toolbar options in the Android designer when using custom device definitions.</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 4.2</a></h2>

<h3>iOS Developer Account login required</h3>
<ul>
   <li>Starting with Xamarin Studio 4.2, you will be required to log into your Apple Developer Account in Xamarin Studio</li>
   <p>
   You can access the Developer Account settings page by navigating to Xamarin Studio -> Preferences -> Developer Accounts:
   </p>
   <p>
   <img src="http://docs.xamarin.com/releases/studio/xamarin.studio_4.0/xamarin.studio_4.0/accounts.png">
   </p>
</ul>

<h3>Source Code Editing</h3>
<ul>
<li>Improved support for on-the-fly formatting and indenting.</li>
  <li>Improved source analysis (beta), with better performance, memory use and stability.</li>
  <li>Fixed several issues when editing aspx and xml files.</li>
  <li>Improved handling of files with mixed line endings.</li>
  <li>Improved the look of in-line error bubbles.</li>
  <li>Reloading a modified file from disk and restoring from Autosave are now undo-able actions.</li>
<!---  <li>Fixed issue that caused certain keyboard layouts to not work correctly on Windows.</li>-->
  <li>Fixed F# syntax highlighting issues</li>
  <li>Improved the speed and user experience of the import symbol completion</li>
</ul>
<h3>iOS</h3>
<ul>
  <li>Added right-click context menu on *.xcassets directories to add
individual asset catalogs for images, app icons, and launch images.</li>
  <li>Added an “archive” command for mdtool which does the same thing as the Build / Archive menu item in Xamarin Studio.</li>
  <li>Updated all of the iOS project Storyboard templates to default to the new Xcode 5 format.</li>

  <li>Added code completion support for the new Xamarin.iOS protocol
support in C#. Xamarin Studio is now aware of bindings to Objective-C
protocols. This means that when your class implements one of the C#
interfaces that map to an Objective-C protocol, when you use the
“override” keyword it will offer not only to complete the methods
inherited from base classes and interfaces, but will offer also the
optional methods from the Objective-C protocol. More information about the
new protocol support in Xamarin.iOS is available in the <a href="http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c/binding_objc_libs#Binding_Protocols" target="_blank">Binding Objective-C Libraries document</a>.</li>

</ul>
<h3>Android Designer</h3>
<p>The Android Designer is now better in handling
layouts with multiple alternative versions. When opening a layout that
has multiple versions, those are shown as thumbnails in a side bar. The
designer now has two operation modes. In the default mode,
changes done to a layout version are particular to that version and
won’t have any effect on the other versions. When in multi-edit mode,
several layouts can be selected for synchronized editing. Changes done
in one layout will be propagated to all selected layouts. Support for
change conflict resolution when in multi-edit mode has also been
improved.</p>

<img style="width: 698px; height: 435px;" alt="" src="Images/android-designer.png"><br>

<p>Other improvements include:</p>
<ul>
  <li>Several improvements in the toolbar and property grid.</li>
  <li>The stock device list available in the toolbar now shows the
devices defined in the Android SDK. Those devices can be configured in
the Android Emulator manager. <br>
  </li>
  <li>Improved performance. The designer is now more responsive when working with big layouts.</li>
</ul>
<h3>Version Control</h3>
<ul>
  <li>Added commands for tagging branches, removing and push tags (Git).</li>
  <li>Fixed incorrect repository detection issue (Git).</li>
  <li>Fixed error when adding Web References in a Subversion repository.</li>
  <li>Improved progress monitoring and notifying for Subversion on Windows.</li>
  <li>Added option for disabling version control support globally.</li>
</ul>
<h3>Debugger</h3>
<ul>
  <li>Improved support for visualizing big arrays using the hex visualizer (data is now incrementally fetched)</li>
  <li>Allow stepping into autogenerated enumerators in user assemblies</li>
  <li>Improved stability when debugging on the Microsoft .NET CLR.</li>
</ul>
<h3>Project System</h3>
<ul>
  <li>Xamarin Studio now can properly load and interpret projects which
make use of properties and environment variables in the definition of
project items.</li>
  <li>Fixed bug that caused classes from System.Core and PCL framework assemblies to not be shown in code completion</li>
  <li>Improved PCL profile selection panel</li>
  <li>Implicit PCL framework references are now shown in the solution pad.</li>
</ul>
<h3>Xamarin Account Management</h3>
<ul>
  <li>The license activation process has been greatly improved.</li>
  <li>There is no need anymore to log-in using a web browser.</li>
</ul>

</body></html>
