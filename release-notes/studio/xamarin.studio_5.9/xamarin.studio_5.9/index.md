---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.9"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.9"></head><body>
  
  

<h2><a name="8" id="8">Xamarin Studio 5.9.8</a></h2>
<p>This release adds support for Apple iOS 9.1/Xcode 7.1, and also addresses some issues with El Capitan compatibility. Other fixes and improvements:</p>
<ul>
	<li>Fixed: During debugging, window asks "Where is iOS Simulator?"</li>
	<li>Fixed: Occasional error when Publishing to Google Play</li>
	<li>Fixed: Codesign fails with "invalid resource specification rule(s)" when building Classic API projects</li>
	<li>Fixed: Unable to create ipa file and Xamarin Studio shows publishing failed</li>
	<li>Fixed: Unable to execute unittests/apps on device with Xcode7 since the build fails by “cannot find code object on disk codesign exited with code 1”</li>
	<li>Fixed: Component page not loading on El Capitan</li>
	<li>Fixed: Occasional error when adding components to a project (message “Unable to connect to the component store.”)</li>
	<li>Fixed: “Android M/MNC” does not appear in “Supported Android versions” list</li>
	<li>Fixed: Apps eventually losing connection to the IDE after an indeterminate amount of time when running on Android M device</li>
	<li>Improved: The New Project dialog now selects by default the last project template used the last time a project was created.</li>
</ul>

<h2><a name="7" id="7">Xamarin Studio 5.9.7</a></h2>
<ul>
	<li>Added support for iOS 9 and Xcode 7</li>
	<li>Added support for the iPhone 6s and 6s+ simulators</li>
	<li>Added support for Android Marshmallow</li>
</ul>

<h2><a name="6" id="6">Xamarin Studio 5.9.6</a></h2>

<ul>
	<li>Fixed: [OSX El Capitan] File Open command crashes Xamarin Studio</li>
	<li>Fixed: [OSX El Capitan] Error in iOS designer Properties window when dropping control to an Storyboard</li>
	<li>Fixed: Updates to Xamarin Studio corrupt the .app on Mac</li>
	<li>Fixed: Hang in Xamarin Studio when trying to add layout file to Android app</li>
	<li>Fixed: Issue when building IPAs in classic iOS projects</li>
   	<li>Improved: The New Project dialog now selects by default the last project type that was created</li>
   	<li>Improved: A warning message is now shown when using refactoring operations since C# 6.0 is not yet fully supported</li>
</ul>

<h2><a name="5" id="5">Xamarin Studio 5.9.5</a></h2>

<ul>
    <li>Improved: Added support for projects created in Visual Studio 2015</li>
    	<li>Fixed: SDK Tools v24.3.4 breaks the Android Designer</li>
	<li>Fixed: Error creating iPhone Web View Classic project</li>
	<li>Fixed: Error on Publishing to Google Play (Task Cancelled exception)</li>
	<li>Fixed: Unable to create Xamarin.Forms project when Android support is disabled</li>
	<li>Fixed: Unable to reference main project classes in Unit Tests</li>
	<li>Fixed: Fixed GTK log spew that can potentially cause IDE slowness</li>
</ul>

<h2><a name="4" id="4">Xamarin Studio 5.9.4</a></h2>

<ul>
	<li>Fixed: Archives Doesn't show up in the archives view</li>
	<li>Fixed: Expressions in the Watch window are cleared each time debugging is stopped</li>
	<li>Fixed: Adding new WatchKit app extension for iOS does not work on big solutions (more than one iOS project)</li>
	<li>Fixed: SIGSEGV when attempting to "Start profiling" from Xamarin Studio on device</li>
	<li>Fixed: Archiving fails sometimes intermittantly</li>
	<li>Fixed: Unable to type some letters into global search bar</li>
	<li>Fixed: IPA Options panel not visible in Project Options</li>
	<li>Fixed: Position of breakpoint changed on debugging the android application</li>
	<li>Fixed: Google publication error messages not readable - dialog too small</li>
	<li>Fixed: Crash when signing Android app</li>
	<li>Fixed: Crash when launching Android Player</li>
</ul>

<h2><a name="3" id="3">Xamarin Studio 5.9.3</a></h2>

Improves compatibility with the latest Android SDK Build-tools 23.0.0_rc1.

<h2><a name="2" id="3">Xamarin Studio 5.9.2</a></h2>

<h3>General</h3>
<ul>
        <li>Improved: Nuget 2.8.5 support</li>
        <li>Improved: Formatting of nuget messages in Status Bar</li>
        <li>Improved: Use native menu for Test output context menu</li>
        <li>Improved: The toolbar is now smaller in height on Mavericks</li>
        <li>Improved: Add designer support for Android SDK 24.3</li>
        <li>Fixed: Debug over WiFi setting not saved in iOS Build settings</li>
        <li>Fixed: Focus issue in when searching in the SearchBar</li>
        <li>Fixed: Ability to expand and collapse the detail of the Exception dialog</li>
        <li>Fixed: Changes to .XIB files don't result in a project build</li>
        <li>Fixed: Crash in Toolbar</li>
        <li>Fixed: Duplicate 'Enable incremental builds' options</li>
        <li>Fixed: 'Set As StartUp Project'' option is missing for device builds</li>
        <li>Fixed: New Project dialog allows a Xamarin.Forms app to be created with no platforms selected</li>
        <li>Fixed: Unable to launch emulator when additional arguments were defined</li>
        <li>Fixed: Clicking Previous on 'Configure your new project' does not work for SpriteKit Game</li>
        <li>Fixed: New iOS Empty project template does not instantiate the Window</li>
        <li>Fixed: Uncaught exceptions from unit tests can bring down the test runner</li>
        <li>Fixed: Entering fullscreen mode in Xamarin Studio can crash on Mac OS X 10.10.3</li>
</ul>

<h3>Publishing</h3>
<ul>
        <li>Fixed: Android Publishing fails with 'Argument is out of range' Exception</li>
        <li>Fixed: Cannot publish iOS app for Ad-Hoc distribution</li>
        <li>Fixed: Unable to upload to AppStore due to iTuneMetadata.plist</li>
        <li>Fixed: iTunesMetadata.plist in IPA causes problems for AppStore distribution</li>
        <li>Fixed: 'Delete All Archives' enabled when it should not be</li>
        <li>Fixed: 'View Archive' option appearing in incorrect locations</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 5.9.1</a></h2>

The iOS Publishing Workflow has been fixed to create proper IPA files suitable for uploading
to the AppStore. The Publishing Workflow wizard has also been fixed to properly construct the
list of Signing Identities and Provisioning Profiles that can be used to re-sign the app bundle.

<h2><a name="0" id="0">Xamarin Studio 5.9</a></h2>

<h3>New Project Dialog</h3>

<p>The window for creating new projects has been redesigned in this release.
The new window has been designed as a wizard that allows creating a project
in several steps: template selection, platform-specific options and generic project settings.</p>

<h4>Template Selection</h4>

<p>The new window presents a new category hierarchy that makes it easier to find specific templates.
Template categories are organized in two columns. The first column allows selecting the platform
(iOS, Android, Mac or cross-platform) and also the kind of project (app, library or test).
The second column shows the list of templates.</p>

<img src="wizard.png">

<p>When a template is selected, a badge with the language name is shown in the template row.
If the template supports more than one language, the badge allows selecting the language to be
used for the new project:
</p>

<img src="language.png">

<p>The right side of the window shows an image and a description of the template.</p>

<h4>iOS Project Options</h4>

<p>Instead of having different sets of project templates for iPhone, iPad and Universal,
the new window presents a single set of templates which can be used for creating projects
for any device. The target device (or devices) can be selected in a configuration page of
the project creation wizard:</p>

<img src="ios-wizard.png">

<p>The wizard also allows selecting the target iOS version. Notice that the target version
may also have an effect on the new project. For example if iOS 8 is selected as the minimum
target, the code generated for the new project will use the new iOS 8 template using size classes.
This allows to have only one storyboard instead of our previous two storyboard (iPhone/iPad).
</p>

<h4>WatchKit Project Options</h4>

<p>The new WatchKit wizard allows you to select the parent iOS project that will reference the two
WatchKit templates created for you. Everything is now done automatically, from the references between
the projects to the bundle identifiers fixed for you.</p>

<img src="watchkit-wizard.png">

<p>You can also choose if you want to support Glance or Notification from the wizard.
That will generate the storyboard views as well as the controller files for the selected scenes.</p>

<h4>Android Project Options</h4>

<p>The Android wizard offers several configuration options, such as the target version and the
theme, and it also allows adding a predefined set of commonly used components.</p>

<img src="android-wizard.png">

<h4>Xamarin.Forms Project Options</h4>

<p>The Forms (or Cross-platform) wizard allows selecting the platforms we want to support,
as well as the kind of library to be used for sharing code.</p>

<img src="forms-wizard.png">

<h4>Project Creation</h4>

<p>The final page of the wizard allows entering the name of the project and the solution,
and its location on the hard disk. There are also options for initializing a local git
repository for the project. The Preview pane at the right shows how files will be organized
on disk after creating the project.</p>

<img src="final-wizard.png">

<h3>Publishing Workflow</h3>

<p>This Xamarin Studio Release includes a new integrated workflow for publishing iOS,
Android and Mac apps.</p>

<p>The main goal of this new workflow is to provide a simple, straightforward,
and consistent way to organize and publish app releases to the different app stores,
with support for ad-hoc and enterprise packages.</p>

<p>Another goal is to reduce the number of build configurations that users have to
manage by re-signing binaries instead of having to use a build configuration with
different signing options. This means that the AdHoc and AppStore iOS configurations
are not required anymore.</p>

<p>This new feature replaces the old iOS specific Archives view and the Publish to
TestFlight command.</p>

<h4>Creating an Archive</h4>

<p>The process of publishing an app starts by running the “Archive for Publishing” command on a project:</p>

<img src="creating-archive.png">

<p>This command is now available for iOS, Android and Mac projects. There is also an “Archive All” command
in the context menu of the solution, which can be used to create archives for all projects of the solution.
For this command to work, you must select a Release configuration.</p>

<p>The command will build the project and will create an archive, which will be shown in the new Archives View.</p>

<h4>Archives View</h4>

<p>The Archives view shows all archives that have been created, grouped by solution. By default this
view only shows the currently open solution. If you want to see all solutions that have archives,
click on the “Show all archives” option.</p>

<p>The view can be opened by right-clicking on a project or solution and selecting the “View Archives”
option, or using the same command from the Build menu in the main menu bar.</p>

<p>When a solution is selected, the view shows a list of all archives created for the solution, with
information about the target platform, version, creation date. There is also an editable comment column.</p>

<p>When an archive is selected, the bottom section of the view shows information about the archive, and
then the “Sign and Distribute” button can be used to publish the package.</p>

<p>The context menu of the archives list can also be used to distribute an archive, or to delete it.</p>

<p><img src="archives-view.png"></p>

<h4>Publishing an Archive</h4>

<div style="float:right">
	<img src="publish-distribution.png"><br>
	<img src="publish-sign.png"><br>
	<img src="publish-account.png"><br>
	<img src="publish-uploading.png">
</div>

<p>An archive can be published by selecting it in the archives list and clicking on the “Sign and
Distribute” command. You can also double-click on the archive.</p>

<p>The steps and information required for publishing a package depends on the target platform and
channel, but in general in process involves the steps described in the next sections.</p>

<h4>Channel Selection</h4>

<p>The following distribution channels are supported for iOS:</p>
<ul>
	<li>AppStore: generates a package.
	</li><li>AdHoc: generates an IPA.
	</li><li>Enterprise: generates an IPA.
</li></ul>
<p>Android distribution channels:</p>
<ul>
	<li>Google Play: generates a package and uploads it to a Google Play account.
	</li><li>AdHoc: generates an APK.
</li></ul>
<p>Mac distribution channels:</p>
<ul>
	<li>AppStore: generates an AppStore package.
	</li><li>Mac app bundle: generates a .app bundle.
	</li><li>Mac installer package: generates a .pkg installer.
</li></ul>

<h4>Package Signing</h4>

<p>The wizard will show a list of signatures or profiles that can be used to sign the package for
the selected distribution channel (notice that not all signatures are valid for all channels).</p>

<p>If the package is already signed, there will be an option for keeping the current signature.</p>

<p>For Android packages there is an option to create a new key, or add an existing key to the
Xamarin Studio key storage. Keys can also be managed in the Android Signing Keys options panel
in the Xamarin Studio preferences.</p>

<h4>Channel parameters</h4>

<p>Some distribution channels will require additional information.</p>

<p><b>Google Play</b> distribution requires a Google Play account. If a Google account has not yet
been registered, the wizard will ask for the account Id and secret, and this information will be
stored so that it can be reused when distributing other apps. Accounts can be managed at any time
in the Google Play Accounts options panel, in the Xamarin Studio Preferences.</p>

<p>It is also possible to select the track where to upload the package (Alpha, Beta, Rollout or Production).</p>

<h4>Package publication</h4>

<p>Some channels (such as Google Play) have support for package uploading to registered accounts,
so in this step the package will be generated and uploaded.</p>

<p>For channels that don’t have this possibility, the package will be generated and then saved
to disk. The user can then manually upload the package.</p>

<h3>Test Cloud</h3>

<ul>
<li>Standalone UITest project templates provided for Android, iOS and Cross-Platform.</li>
<li>Android, iOS, Xamarin.Forms and Cross-Platform project templates now include a UITest project with a UITest that tests the main application.</li>
<li>UITest projects can be run locally with the iOS and Android device or simulator with the test results shows in the Unit Tests window.</li>
<li>UITests will run with the device or simulator (Android or iOS) selected in Xamarin Studio.</li>
<li>Run in Test Cloud menu added to the Unit Tests window to allow UITests to be uploaded to Test Cloud.</li>
</ul>

<h3>Improved Debugger Experience</h3>

<h4>New Debugger Visualizers</h4>

<p>This release includes a new UI for quickly visualizing the value of a variable, field or property while
debugging. The new Preview popup is supported for some specific data structures: strings, points, sizes, rectangles,
colors, map locations, images, bézier curves, among others.</p>

<p>For example, this is how a color can be visualized:</p>

<p><img src="visualizer-color.png"></p>

<p>When moving the mouse near the field name, a new "preview" button is shown. When clicking on it, the Preview
popup is shown:</p>

<p><img src="visualizer-color2.png"></p>

<p>Those are the visualizers for image and location:</p>

<p><img src="visualizer-image.png"></p>

<p><img src="visualizer-map.png"></p>

<h4>IEnumerable Expansion</h4>

<p>It is now possible to see the values returned by objects that implement IEnumerable. A new IEnumerator node
is shown for those objects:</p>

<p><img src="visualizer-enumerator.png"></p>

<p>When this node is expanded, the enumerator is evaluated and the returned values are shown in the tree:</p>

<p><img src="visualizer-enumerator2.png"></p>

<h3>Xamarin.Android</h3>
<p>This release includes new build options for Xamarin.Android 5.1 features:</p>
<ul>
<li>AOT Support (Ahead Of Time compilation) to reduce JIT startup overheads.</li>
<li>Multi-Dex Support: Multi-Dex support enables use of new Android SDK tools ("jack" and "jill") to bypass the historical 64k method limit present within the .dex file format.</li>
<li>Arm64 Support: Xamarin.Android 5.1 adds support for targeting 64-bit Android platforms such as the Nexus 9.</li>
<li>ProGuard Support: ProGuard is an Android SDK tool which can be used to link and obfuscate Java code.
    The primary reason to provide ProGuard support is to permit smaller applications, so that gigantic
    libraries such as Google Play Services can be reduced in size.</li>
</ul>

<h3>Text Editor</h3>

<h4>Partial C# 6 Support</h4>

<p>Mono 4.0 includes support for C# 6, and although Xamarin Studio doesn't yet fully support code completion and
refactoring operations for all C# 6 constructs, it will now work for some of them.</p>

<h4>Preview of editor settings changes</h4>

<p>When changing the configuration of the text editor in global preferences (such as the font, color, visible markers, etc),
the changes will be immediately visible. This makes it easier to see what's the effect of some settings in the look of the editor.</p>

<h3>Native Mac toolbar</h3>

<p>Xamarin Studio on Mac now has a toolbar with a native look and behavior. On Yosemite, the new toolbar blends with
the title bar, thus providing more vertical space in the work area.</p>

<p><img src="toolbar.png"></p>

<h3>NuGet Support</h3>

<ul>
<li>The Packages folder is now always visible in Solution pad.</li>
<li>Target Framework changes are now detected on project reload. The iOS Classic to iOS Unified migration tool
  changes the project’s target framework in the project file. Xamarin Studio will now detect this has been
  changed and the NuGet packages will be checked for compatibility with the new target framework.</li>
<li>Updated to NuGet 2.8.3: it allows NuGet packages that explicitly target NuGet 2.8.3 or use the new ASP.NET Core target frameworks
to be installed into a project, such as xunit.</li>
</ul>

<h3>Configurable Components Directory</h3>

<p>A solution can now specify a directory where Xamarin Components will be extracted to before being referenced
by a project. This allows multiple solutions to use the same directory and prevents the assembly references
from being modified when a project is opened within the context different solutions.</p>

<p>To configure the components directory a components.config file should be created, as shown below.</p>

<pre><code class="syntax brush-XML syntax brush-C#">
&lt;components&gt;
    &lt;config&gt;
       &lt;add key="cachePath" value="..\Components"&gt;&lt;/add&gt;
   &lt;/config&gt;
&lt;/components&gt;
</code>
</pre>

<p>When a solution is opened Xamarin Studio will check for a components.config file in several locations based on the solution's directory. The full set of locations checked is as follows, assuming the solution directory is /a/b/c</p>

<ul>
<li>/a/b/c/.components/components.config</li>
<li>/a/b/c/components.config</li>
<li>/a/b/components.config</li>
<li>/a/components.config</li>
<li>/components.config</li>
<li>~/Library/Preferences/Xamarin/Components/components.config</li>
<li>On Windows: %AppData%\Xamarin\Components\components.config</li>
</ul>

<p>If the components.config file exists then Xamarin Studio will use the cachePath to determine the Components directory that the solution should use. The path specified can be a full path or a relative path. If it is a relative path then it is relative to the directory containing the components.config file.</p>

<h3>Sketches</h3>

<h4>New View Options</h4>

<ul>
  <li>There is a new "Sketch" layout available in the View menu, which includes
  the new Sketch Properties pad. The pad can also be toggled from <i>View →
  Pads → Sketch Properties</i>.</li>
  <li>You can toggle the display of the Console Output in the sketch timeline
  with <i>View → Sketches → Console Output</i>.</li>
  <li>You can restore all CaptureValue visualizers for a sketch with <i>View →
  Sketches → Restore CaptureValue Visualizers</i>.</li>
</ul>

<h4>Resource Management UI</h4>

<p>In Xamarin Studio 5.7, we introduced the ability to add resources to your sketch
files by creating a folder called "{yoursketch}.sketchcs.Resources". Now, this
can all be managed from within Xamarin Studio.</p>

<p>The Sketch Properties pad shows the contents of your sketch's resources folder.
You can add and remove resources right from the pad by right-clicking the
Resources folder, or by dragging and dropping files into the folder.</p>

<p>If your sketch is in a project, you can also manage your resources in the
solution explorer, by expanding the sketch file node to reveal the resources
folder node within it.

Be aware that if you delete a sketch in Xamarin Studio, the resources folder
will also be deleted.</p>

<p>On iOS and Mac, resources are exposed via <code>NSBundle.MainBundle</code>.
However, keep in mind that some Apple APIs cache resources. So, if you access an
image using <code>NSImage.ImageNamed(resourceName)</code>, and then modify the
image, you won't see the changes in the sketch, because NSImage caches by name.
To work around this, use
<code>NSBundle.MainBundle.ImageForResource(resourceName)</code>, or
<code>new NSImage(GetResourcePath(resourceName))</code>.</p>

<h4>Improved Security</h4>

<p>If you downloaded a sketch from the internet, we will not execute it until
you approve it.</p>

<h4>Xamarin.Forms Sketches Upgraded</h4>

<p>Xamarin.Forms 1.3.2 contains many bugfixes. Your Android and iOS Xamarin.Forms
sketches can now use new features like element styles.</p>

<h4>Other Changes</h4>

<p>When a Mac sketch file is open, a dock icon now appears from the agent app
(the process that actually evaluates sketch code). This makes it easy to bring
the RootWindow back to the foreground, or quit the process if it's causing
problems.</p>

<h3>iOS Designer</h3>
<ul>
  <li>Fixed a crash caused by clicking on the 'Events' tab of a custom control when the corresponding source code for that class is missing</li>
  <li>The labels have been restored to all the properties which were missing them</li>
  <li>Improved support for unwind segues in the property panel</li>
  <li>Improved the initial loading performance of large storyboards</li>
  <li>Fixed more cases where incorrect resize handles were showing</li>
  <li>Improved rendering accuracy when using NavigationBar or TabBar simulated metrics</li>
  <li>WKInterfaceSwitch and WKInterfaceSlider will now have default 'click' actions in the Events panel</li>
  <li>Improved property panel support for the 'Storyboard ID', 'Restoration ID' and 'Use storybosard id as restoration id' properties</li>
  <li>The 'Identity' panel shows up for Custom NSObjects again</li>
  <li>Many minor performance improvements for common situations like opening a storyboard, syncing the generated code and re-rendering after changing a property.</li>
  <li>Improved rendering accuracy for NSNotificationCategory</li>
  <li>It is now possible to use drag and drop on the design surface to re-order UITableViewCells</li>
</ul>

<h3>Other fixes and improvements</h3>

<ul>
	<li>The Welcome Page now shows a Start Trial button when a trial is available.</li>
	<li>The Help menu now has links to the release notes of every installed Xamarin product.</li>
	<li>Updated Japanese translation.</li>
</ul>

</body></html>
