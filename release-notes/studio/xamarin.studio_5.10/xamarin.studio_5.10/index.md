---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.10"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.10"></head><body>
  
  
  
<h2><a name="3" id="3">Xamarin Studio 5.10.3</a></h2>
<h3>Xamarin Studio has a new licensing model.</h3>
<ul>
	<li>Introducing Xamarin Studio Community Edition. A new, freely available version of Xamarin Studio for indie developers available under similar terms to Visual Studio Community.</li>
	<li>Existing Xamarin Indie, Business and Enterprise licenses will continue to work and have the features that are entitled under the existing license.</li>
	<li>Windows users with Visual Studio Professional or Visual Studio Enterprise installed, or linked to their Xamarin account will be able to use Xamarin Studio at the Professional or Enterprise level.</li>
	<li>Mac users with Visual Studio Professional or Visual Studio Enterprise linked to their Xamarin account will be able to use Xamarin Studio at the Professional or Enterprise level.</li>
	<li>Other users who have either Visual Studio Community or no Visual Studio edition installed will be able to use Xamarin Studio at the Community level. The same applies to users who also do not have a Visual Studio license linked with their Xamarin Account.</li>
	<li>Xamarin Studio on Windows will no longer support trials. Any existing trial will no longer work. To continue to trial Xamarin on Windows users should start a Visual Studio trial and use Xamarin within Visual Studio instead.</li>
</ul>

<h3>iOS</h3>
<ul>
	<li>Fixed: UnhandledException when publishing AdHoc build (iTunesMetadata.plist already exists).</li>
	<li>Fixed: Xamarin Studio would lock up periodically when querying iOS devices.</li>
	<li>Fixed: Device specific builds would fail for specific iPad versions.</li>
</ul>

<h3>Other</h3>
<ul>
	<li>Fixed: Crash in debugger after pausing.</li>
	<li>Fixed: Using the open files selector to change file would not update the text editor.</li>
	<li>Fixed: Xamarin Studio could crash when displaying tooltips.</li>
	<li>Updated: Licence information - see About Xamarin Studio.</li>
</ul>

<h2><a name="2" id="2">Xamarin Studio 5.10.2</a></h2>
<h3>iOS</h3>
<ul>
	<li>Fixed: iPad Pro support.</li>
	<li>Fixed: Asset placeholders for iPad Pro launcher images were missing.</li>
	<li>Fixed: NSLocationAlwaysUsageDescription and NSLocationWhenInUseUsageDescription were not displayed correctly in the Info.plist.</li>
	<li>Fixed: IpaIncludeArtwork was set incorrectly in the project file.</li>
	<li>Fixed: The new project dialog and plist editor combos don't show iOS 9.1 with the latest Xcode 7.2.</li>
	<li>Fixed: Device specific builds could fail if the project was configured for 64bit only.</li>
</ul>

<h3>Android</h3>
<ul>
	<li>Fixed: When creating a new Xamarin.Forms app the initialization call was missing from the Android app.</li>
	<li>Fixed: The AOT checkbox in Android build settings should be marked as experimental.</li>
</ul>

<h3>Insights</h3>
<ul>
	<li>Fixed: When adding Insights to a new Xamarin.Forms app the Insights NuGet was not added to the PCL project.</li>
	<li>Fixed: When publishing an app that did not have Insights enabled the publishing wizard would fail with "Could not Upload to Xamarin Insights".</li>
	<li>Fixed: Initialization code for Xamarin.Insights should fully qualify the API key identifier.</li>
	<li>Fixed: mdtool would fail to build a project that had Xamarin.Insights enabled.</li>
	<li>Fixed: Xamarin.Insights support is now disabled by default in the new project dialog.</li>
	<li>Fixed: Xamarin.Insights documentation links in the new project dialog.</li>
</ul>
<h3>Version Control</h3>
<ul>
	<li>Fixed: Using the Blame context menu was awkward and unreliable.</li>
	<li>Fixed: Some Version control options were disabled even though they were available in the context menu.</li>
	<li>Fixed: [Git] Commits are reordered when rebasing.</li>
</ul>
<h3>Other</h3>
<ul>
	<li>Improved: UITest NuGets are now updated for new projects.</li>
	<li>Fixed: The Task Pad can no longer be sorted by Completed.</li>
	<li>Fixed: Editing user tasks in tasks pad when sorted modifies wrong task.</li>
	<li>Fixed: Projects on Windows with C# 6.0 features would fail to compile.</li>
	<li>Fixed: F# Mac apps were not setting the Application Name and Bundle Identifier correctly.</li>
	<li>Fixed: Rendering issues in the status bar of the Test Results Pad.</li>
	<li>Fixed: The Locals Pad would append duplicate items when the Call Stack was doubled clicked.</li>
	<li>Fixed: Importing a .mdpolicy file with no name would throw an exception.</li>
	<li>Fixed: Rendering issue with checkboxes in settings.</li>
	<li>Fixed: Xamarin Studio would crash under certain circumstances when using Global Search.</li>
	<li>Fixed: Rendering issue with toolbar icons when running on El Capitan.</li>
	<li>Fixed: Xamarin Studio could not create a project in a directory with certain characters in it.</li>
	<li>Fixed: A packaging issue could cause Xamarin Studio to crash.</li>
	<li>Fixed: Menu items remain disabled after showing a dialog in some circumstances.</li>
	<li>Fixed: Multiple copies of the same modal dialog can be made visible at the same time.</li>
	<li>Fixed: Event Args or Event Handlers are not created when adding a Web Reference.</li>
	<li>Fixed: Certain unsupported or invalid C# construct cause Xamarin Studio to hang.</li>
	<li>Fixed: Xamarin Studio may crash if custom builds of libraries used by Mono are installed in the system.</li>
	<li>Fixed: The "open files" drop down selector in the document tab bar does not correctly switch files.</li>
	<li>Fixed: Xamarin Studio would query the java version excessively.</li>
	<li>Fixed: An issue where editing user tasks in tasks pad could modify the wrong task when the tasks were sorted .</li>
</ul>
<ul>
	<li>Fixed: The 'Content Stretch' property did not work reliably. Now it does.</li>
	<li>Fixed: ViewControllers should always have the correct Simulated Metrics applied now.</li>
	<li>Fixed: Sometimes deleting a View from a ViewController would not delete the corresponding 'Outlet', if one existed.</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 5.10.1</a></h2>
<ul>
	<li>Fixed: The iOS Designer was unable to open iPad xib files. Now these files will be correctly detected as 'xib' files and will render in the surface.</li>
	<li>Fixed: Fixed an issue where some storyboards would not render when iOS9 or newer was selected.</li>
	<li>Fixed: The Z-Order for individual ViewControllers was not being set/maintained correctly. It will be now!</li>
	<li>Fixed: Incorrect (CloudKit) entitlement prevents distribution when using “Archive for Publishing”</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.10</a></h2>

<h3>Index</h3>

<ul>
	<li><a href="#ios">iOS</a>
		<ul>
			<li><a href="#ios-wizard">New extension project creation wizard</a></li>
			<li><a href="#ios-dev">Device-specific builds</a></li>
			<li><a href="#ios-organization-identifier">New Organization Identifier field</a></li>
			<li><a href="#ios-wizard-project-templates">Changes to iOS Project Templates</a></li>
			<li><a href="#ios-wizard-file-templates">Changes to iOS File Templates</a></li>
		</ul>
	</li>
	<li><a href="#ios-designer">iOS Designer</a>
		<ul>
			<li><a href="#ios-designer-xib">Full Xib and Xib Splash Screen support</a></li>
			<li><a href="#ios-designer-surf">Faster hi-dpi design surface</a></li>
			<li><a href="#ios-designer-ini">Faster initialization</a></li>
			<li><a href="#ios-designer-other">Other changes</a></li>
		</ul>
	</li>
	<li><a href="#android">Android</a>
		<ul>
			<li><a href="#android-organization-identifier">New Organization Identifier field</a></li>
			<li><a href="#android-other">Other changes</a></li>
		</ul>
	</li>
	<li><a href="#android-designer">Android Designer</a>
		<ul>
		  <li><a href="#android-designer-surf">Faster hi-dpi design surface</a></li>
		  <li><a href="#android-designer-material">Material design helpers</a></li>
		  <li><a href="#android-designer-ppanel">Property panel improvements</a></li>
		  <li><a href="#android-designer-toolbar">Refreshed toolbar</a></li>
		  <li><a href="#android-designer-other">Other changes</a></li>
		</ul>
	</li>
	<li><a href="#mac">Xamarin.Mac</a>
		<ul>
			<li><a href="#mac-wizard">New project creation wizard</a></li>
			<li><a href="#mac-wizard-templates">Changes to Mac Templates</a></li>
		</ul>
	</li>
	<li><a href="#cross-platform">Cross Platform</a>
		<ul>
			<li><a href="#cross-platform-templates">New Cross platform Games template</a></li>
			<li><a href="#cross-platform-organization-identifier">New Organization Identifier field</a></li>
		</ul>
	</li>
	<li><a href="#insights">Xamarin Insights</a>
	</li>
	<li><a href="#test-cloud">Xamarin Test Cloud</a>
	</li>
	<li><a href="#profiler">Profiler</a>
	</li>
	<li><a href="#shell">Shell</a>
	</li>
	<li><a href="#code-analysis">Code Analysis</a>
	</li>
	<li><a href="#version-control">Version Control</a>
		<ul>
			<li><a href="#version-control-git">New Git backend based on libgit2</a></li>
			<li><a href="#version-control-other">Other changes</a></li>
		</ul>
	</li>
	<li><a href="#debugger">Debugger</a>
	</li>
	<li><a href="#nuget">NuGet</a>
	</li>
	<li><a href="#editor">Source Code Editing</a>
	</li>
	<li><a href="#nunit">Unit Testing</a>
	</li>
	<li><a href="#other">Other bug fixes and improvements</a>
	</li>
	<li><a href="#known-issues">Known Issues</a>
	</li>
</ul>

<h3 id="ios">iOS</h3>
<h4 id="ios-wizard">New extension project creation wizard</h4>

<p>This wizard can be used to create an extension project and bind it to an existing iOS app project.</p>

<img src="extension-wizard.png">

<h4 id="ios-dev">Device-specific builds</h4>

<p>iOS apps are typically built for multiple architectures so that they can run on a range of devices.
However, each additional architecture substantially increases the time taken by the AOT compilation,
and increases the size of the app bundle and hence the deployment time.</p>

<p>At development time, users usually iterate using a single target device. The new <b>Device specific builds</b> option
causes the build to be optimized for that device, substantially improving the development experience, while preserving
existing multi-architecture behaviour for release builds, and ensuring everything works correctly if the user
switches device at development time.</p>

<p>This option can be set in the project options dialog, and it is enabled by default for Debug builds.</p>

<h4 id="ios-organization-identifier">New Organization Identifier field</h4>

<p>On iOS the bundle identifier is now generated from the organization identifier which is shared across all wizards and saved every time. This allows projects to be created with an always valid identifier.</p>

<h4 id="ios-wizard-project-templates">Changes to iOS Project Templates</h4>

<p>All the iOS Classic API templates and the Unified API Empty Project template have been removed. The names of iOS Tests templates have been changed.</p>

<h4 id="ios-wizard-file-templates">Changes to iOS File Templates</h4>

<p>The iOS File Templates are now using size classes.</p>

<h3 id="ios-designer">iOS Designer</h3>
<h4 id="ios-designer-xib">Full Xib and Xib Splash Screen support</h4>
<p> We're pretty excited to finally ship full support for Xib files in this release. You can edit and interact with
xib files just like you already could with storyboard files. This includes full support for designing xib splash screens.</p>

<h4 id="ios-designer-surf">Faster hi-dpi design surface</h4>
<p>Just like the Android Designer, the design surface has been rewritten to take advantage of high performance,
hardware accelerated APIs. When a hi-dpi display is attached, the design surface will switch to hi-dpi mode and
will render higher quality images. The new surface should use less memory, feature much smoother scaling/zooming
and also be significantly faster when panning around a large storyboard. If you are using a touchpad you can zoom
and pan using the standard gestures. If you are still on a lo-dpi display you should still notice an improvement
in the quality of the images on the design surface.</p>

<h4 id="ios-designer-ini">Faster initialization</h4>
<p>We've worked hard on tweaking every aspect of the initialization process so that the time between double
clicking a storyboard and seeing it display on-screen is as short as possible. Both the first launch time and
subsequent re-launch times should be noticably shorter, especially with large storyboards. We have also fixed many
cases which would cause initialization to time out and display an error.</p>

<h4 id="ios-designer-other">Other changes</h4>
<ul>
  <li>Faster refreshing when an item is modified on the design surface.</li>
  <li>Fixed several cases where the design surface would not react when the mouse button was released.</li>
  <li>Fixed several cases where simulated metrics were not being set correctly.</li>
  <li>Significantly improved support for property variations in the property panel.</li>
  <li>All accessibility properties are supported.</li>
  <li>Improved support for Unwind and Embed segues.</li>
  <li>Retina image resources should be handled correctly now.</li>
  <li>Fixed many cases where the property panel would not write the correct value to the storyboard/xib file.</li>
  <li>Fixed several places where the wrong default value was showing up in the property panel.</li>
  <li>Improved support for changing between Plain text and Attributed text for properties supporting both.</li>
  <li>Resize handles will only appear when they can modify the size of the View they're attached to.</li>
  <li>Custom properties of type nint and nfloat are now supported by the property panel.</li>
  <li>All performance issues associated with the Outline panel have been fully resolved.</li>
  <li>Constraints are now grouped in the Outline panel.</li>
  <li>Fixed several issues with copy/paste which could corrupt the storyboard.</li>
  <li>Improved support for fixing the frame for underconstrained items.</li>
  <li>AwakeFromNib should be reliably invoked for custom controls in the design surface.</li>
  <li>Improved misplacement handling for under-constrained/over-constrained items and when changing size classes.</li>
  <li>The designer should never overwrite existing files when generating new classes.</li>
  <li>Full support for WatchOS2 rendering as of the latest Xcode 7 beta release.</li>
  <li>Dozens more under the hood changes to fix crashes, exceptions and quirks</li>
</ul>

<h3 id="android">Android</h3>

<h4 id="android-organization-identifier">New Organization Identifier field</h4>

<p>On Android the package name is now generated from the organization identifier which is shared across all wizards and saved every time. This allows projects to be created with an always valid identifier.</p>

<h4 id="android-other">Other changes</h4>
<ul>
<li>Allow choosing supported ABIs in Debug builds.</li>
<li>Allow debugging of Android Application with no activities. This allows debugging of Watch faces in
Android Wear.</li>
<li>Added UI to enter TSA url when signing the package during distribution (the signing page of the
distribution wizard)</li>
<li>Added command for opening the folder where an archive is located.</li>
<li>Added a "Reveal in Finder" button for the keystore in preferences, and
a new context menu action to show the alias details, so that the user can copy whatever is needed for the Google API console.</li>
<li>Project templates updated to use mipmaps instead of drawables for application icons.</li>
<li>Fixed: Signing packages with a keystore with SHA1withDSA fails.</li>
<li>Fixed: Minimum Android Version and Target Android Version combobox settings do not work.</li>
<li>Fixed crash when signing Android app.</li>
<li>Fixed: Properties/AssemblyInfo.cs missing from Android Library.</li>
<li>Fixed: Android axml templates use deprecated "fill_parent" instead of "match_parent".</li>
<li>Fixed: App Identifier should be created by using App Name after stripping off leading and trailing whitespaces.</li>
<li>Fixed: "Xamarin Android Player is already running" message keeps showing up for every test being run.</li>
<li>Fixed: Unable to reference main project classes in Unit Tests.</li>
<li>Fixed: Android log pad behaves strangely when device is disconnected. Clear the device if it is no longer connected to ABD.</li>
</ul>

<h3 id="android-designer">Android Designer</h3>
<h4 id="android-designer-surf">Faster hi-dpi design surface</h4>
<p>Just like the iOS designer, the design surface has been rewritten to take advantage of high performance, hardware
accelerated APIs. When a hi-dpi display is attached, the design surface will switch to hi-dpi mode and will render
higher quality images. The new surface should use less memory and feature much smoother scaling/zooming. If you are
using a touchpad you can zoom and pan using the standard gestures. If you are still on a lo-dpi display you should
 still notice an improvement in the quality of the images on the design surface.</p>

<h4 id="android-designer-material">Material Design helpers</h4>

<p>A new set of design tools has been added to ease creating layouts that follow Google's <a href="//www.google.com/design/spec/material-design/introduction.html">Material Design specification</a>. Those tools are only available or most complete when the designer rendering target is at least Lollipop (i.e. Android 5.0 / API level 21). Support for appcompat-based layout will come in a future release.</p>

<h5>Grid</h5>
<img src="android-designer-grid.png">
<p>There is now an option to create a grid with a set size that will be overlayed on your layout for easier individual widget placements. Custom spacings and keylines can also be defined depending on your layout requirements.</p>

<h5>Color palette</h5>
<img src="android-designer-colors.png">
<p>Entries in the property panel that accept a color value possess an extra action button to pick a color straight from Google's <a href="//www.google.com/design/spec/style/color.html">Material color palette</a>.</p>

<h5>Typographic scale</h5>
<img src="android-designer-typography.png">
<p>Similarly, you can also pick up a pre-defined text appearance following Google recommendation for legibility and text harmony in the corresponding property entry. The text variants are displayed using the currently selected theme information for better previewing.</p>

<h5>Theme editor</h5>
<img src="android-designer-theme.png">
<p>You can edit and visualize the dominant colors of your Material-derived theme directly from the designer and save the result in your theme resource file.</p>

<h4 id="android-designer-ppanel">Property panel improvements</h4>

<img src="android-designer-ppanel.png">

<p>The property panel will warn you when incompatible values are provided for a property or when the resource it references is invalid or doesn't exist. It will now also offer autocompletion for compatible resource references.</p>

<h4 id="android-designer-toolbar">Refreshed toolbar</h4>

<p>The toolbar has been refreshed to be more compact and streamlined with the rest of the IDE experience.</p>

<h4 id="android-designer-other">Other changes</h4>
<ul>
  <li>Support for Lollipop new widgets and attributes</li>
  <li>Support for Marshmallow rendering</li>
  <li>The designer displays a warning if resources errors could prevent correct rendering</li>
  <li>Editing text entries on the surface will try to use the same font and text style as on Android</li>
</ul>

<h3 id="mac">Xamarin.Mac</h3>
<h4 id="mac-wizard">New project creation wizard</h4>
<p>The new mac wizard comes with a new Cocoa App template including storyboard and NSDocument support.
The wizard allows you to do several things:</p>
<ul>
<li>Use a different application name for the dock’s app icon. Once the checkbox “Use a Different Application Name in Dock”
is checked the UI will let you use different names and show them on the right side of the wizard.</li>
<li>Create a Document-Based Application. When the option is checked, the wizard will let you name your document extension and add NSDocument support to the new project. 
You can see the extension name in the advanced category of the Info.plist file.</li>
<li>Select the minimum target you want to support. Note that the list has very explicit names for each version.</li>
<li>The bundle identifier is now generated from the organization identifier which is shared across all wizards and saved every time. This allows projects to be created with an always valid identifier.</li>
</ul>

<img src="mac-wizard.png">

<h4 id="mac-wizard-templates">Changes to Mac Templates</h4>
<p>All the Mac Classic API templates and the Unified API Empty Project template have been removed. Note that you can still access the Classic API templates when adding a new project to an existing solution.</p>

<h3 id="cross-platform">Cross Platform</h3>
<h4 id="cross-platform-templates">New Cross platform Games template</h4>

<p>There are two new Cross Platform templates targeting iOS and Mac - SpriteKit Game and SceneKit Game</p>

<h4 id="cross-platform-organization-identifier">New Organization Identifier field</h4>

<p>The Android package name and iOS bundle identifier are now generated from the organization identifier which is shared across all wizards and saved every time. This allows projects to be created with an always valid identifier.</p>

<h3 id="insights">Xamarin Insights</h3>

<p>Integrating Insights into a Xamarin app is currently a manual process.
Developers must manually add the Insights NuGet package to their app project,
create an app ID on the Insights website, and copy the app’s API key from the
website into initialization calls in their app’s source code. Then, in order
to get stack traces for errors, they must manually upload debug symbols to the
Insights website for each binary build of their app that that they release to users</p>

<p>This Xamarin Studio release includes integrated support for Xamarin Insights.
This integration aims to fix these problems by making it trivially easy to add Insights support
to new and existing apps, and to upload debug symbols.</p>

<p>Insights support can be enabled when creating a project by just checking a checkbox in the
project creation wizard. For existing projects, Insights support can be enabled in the project options.
Xamarin Studio will automatically register new applications in Insights, and
will generate and configure the app with the new API key.</p>

<p>When an application is archived in Xamarin Studio, if the app project has Insights enabled,
the API key will be embedded into the archive manifest. The archive details panel in the archive list view
shows a field with a timestamp of when debug symbols were last uploaded to Insights (or not).</p>

<p>When publishing an archive, if the archive has an Insights key, the debug symbols of the app will also
be published.</p>

<img src="insights.png">

<h3 id="test-cloud">Test Cloud</h3>
<ul>
<li>The final page of the New Project dialog now has a Xamarin Test Cloud check box for those projects that support Test Cloud.
This check box can be used to enable or disable the creation of the UITest project when creating a new solution or project.</li>
<li>The UITest project templates have been updated to use Xamarin.UITest 1.0.</li>
<li>Fixed: Run in Test Cloud failing when iOS project has different the build version (CFBundleVersion) and application version (CFBundleShortVersionString) are different.</li>
</ul>

<h3 id="profiler">Profiler</h3>
<ul>
<li>Xamarin Studio can now pass Xamarin.Mac applications to the Profiler to be profiled using Run -> Start Profiling or right clicking on a solution/project and using Start Profiling Item.</li>
<li>The profiler version and location is now shown in the About dialog.</li>
</ul>

<h3 id="shell">Shell</h3>
<ul>
<li>The search bar can now be focused when the search hotkey (ctrl+, cmd+.) is invoked in a detached editor tab.</li>
<li>Fixed the toolbar not being draggable close to the debug bar.</li>
<li>Fixed issues with the statusbar tooltips where it would stay on screen or have misaligned text.</li>
</ul>

<h3 id="code-analysis">Code Analysis</h3>
<p>Xamarin Studio now provides a built-in way to set and invoke the same MSBuild
"RunCodeAnalysis" target and property that are commonly used by code analysis
tools in Visual Studio.

<p>Two new commands have been added: “Run Code Analysis on project” and “Run Code Analysis on solution”.
Invoking those commands sets the “RunCodeAnalysis” MSBuild property and executes “Build” target, it’s job of “RunCodeAnalysis” target to depend on “Build” target to be executed.

<p>With this first release of the feature, users must provide their own
"RunCodeAnalysis" targets to analyze project code or settings.

<p>Those commands are intended to be used by future releases of Xamarin.Android, Xamarin.iOS and Xamarin.Mac
to do analysis of project settings and show warnings and errors about misconfigurations of projects.</p>
<p>A new section in the project settings has been added where this functionality can be enabled on every build.</p>

<h3 id="version-control">Version Control</h3>
<h4 id="version-control-git">New Git backend based on libgit2</h4>
<p>Switched Git provider from NGit to LibGit2. This fixes a whole suite of bugs that were affecting repositories
under Git. Main highlights are: performance increase in all commands, fixed issues with loss of data, corrected
behaviour of git update and stash, improved usage of the git index and sane file staging, improved status update
of actions.</p>

<h4 id="version-control-other">Other changes</h4>
<ul>
<li>Invalid passwords are no longer remembered.</li>
<li>Fixed a bug where some old .svn repository was found when a .git repository was closer to the Solution file, or vice-versa.</li>
<li>Added a button to Fetch remotes in the Manage Branches and Remotes dialog.</li>
<li>Commit comments can now be copied to clipboard.</li>
<li>Binary detection of files should now match the underlying system’s binary detection, then tries a mime-type check.</li>
<li>Performance and memory consumption optimizations.</li>
<li>TFS via Git is now supported.</li>
<li>Known issue: Blame doesn’t take into account local changes to the file</li>
</ul>

<h3 id="debugger">Debugger</h3>
<ul>
<li>Improved StackTrace pad to give user option to show/hide columns, parameter type, parameter name, parameter value,
module and line number.</li>
<li>Added support for visualizing objects of type System.IO.MemoryStream and NSData.</li>
<li>Improved display of multiline strings in call stack pad.</li>
<li>Added "User code only" support for catchpoints.</li>
<li>Fixed: locals not shown if the window is not currently focused when a breakpoint is hit.</li>
<li>Fixed: Calling functions in the watch window results in autocomplete appending the first entry.</li>
<li>Fixed: If debugee crashed during evaluating value in ImmediatePad, it kept printing dots for "Evaluating..."</li>
<li>Fixed: NUnit view resets to Solution view after debugging test.</li>
<li>Fixed annoying flicker in debugger tooltip.</li>
<li>Fixed deselection of multiple lines selection on right-click so user can Copy multiple values from DebuggerTreeView.</li>
<li>Fixed: Inline editor does not fetch whole string.</li>
<li>Fixed: Watch window: three clicks required to add a new watch.</li>
<li>Fixed: Select All command when editing watch selects the whole watches list.</li>
<li>Fixed: Variables in Locals and Watch window collapse every time you step through code.</li>
<li>Fixed: Debugger locks pdb file after aborting on Windows</li>
<li>Fixed: Exception popup can't be closed.</li>
<li>Fixed: Windows debugger ignores non-zero based arrays.</li>
<li>Fixed: Debugger type proxies don't work for F#.</li>
<li>Fixed: Incorrect resolving of virtual property in watch view.</li>
<li>Fixed: Cannot evaluate decimal in immediate window.</li>
<li>Fixed: Enabling the Android linker causes breakpoints set on newly added lines of code in PCLs to be ignored by Xamarin Studio until they are re-set.</li>
<li>Fixed: Invalid cast of nint type in immediate window.</li>
<li>Fixed issues when trying to Debug on a 64 bit Android device.</li>
<li>Fixed: IntPtr display issue when debugging 64bits applications</li>
<li>Fixed: User is not able to see Hex value in value visualizer window.</li>
</ul>

<h3 id="nuget">NuGet</h3>
<ul>
<li>Readme.txt will be opened when installing NuGet package if it exists.</li>
<li>Preserve Local Copy setting for references when updating packages.</li>
<li>Support packages.Config files named after the project (e.g. packages.ProjectName.config).</li>
<li>Do not show warning in the status bar if NuGet package have PowerShell scripts.</li>
<li>Do not show Checking for package updates message in status bar <b>(not in the first alpha release)</b>.</li>
<li>Update to NuGet 2.8.7 <b>(not in the first alpha release)</b>.</li>
<li>Prevent packages.config file being marked as deleted by Git after updating the Xamarin.Forms NuGet package.</li>
<li>Prevent the solution being closed whilst NuGet packages are being added and the solution is not fully created.</li>
<li>Fixed: Removing a NuGet package does not update the list of packages when multiple solutions are open.</li>
</ul>

<h3 id="editor">Source Code Editing</h3>
<ul>
<li>Improved visual style of code generation popup.</li>
<li>Add an action to delete from the caret to the start of the line.</li>
<li>Fixed: Context menu does not appear at correct position by using ALT+SHIFT+F10 shortcut keys.</li>
<li>Fixed: Editor is slow when displaying very long lines.</li>
<li>Fixed: Formatting doesn't trigger on save for xaml or xml files.</li>
<li>Fixed: "Toggle Line Comment(s)" in XML Editor affects selected lines plus one more line.</li>
</ul>

<h3 id="nunit">Unit Testing</h3>
<ul>
<li>Do not clear the test results when changing the currently selected project configuration.</li>
<li>Fixed: Test result info not cleared from bottom toolbar in Test Results pad after closing solution</li>
<li>Run command is now disabled in the Test pad context menu when a test is running.</li>
</ul>

<h3 id="other">Other bug fixes and improvements</h3>
<ul>
<li>Use of WCF classes is now allowed for Indie and Starter licenses.</li>
<li>The Windows taskbar icon no longer needs repinning.</li>
<li>The Windows taskbar icon now supports Recent Files/Solutions.</li>
<li>Removed files will no longer appear in Recent Files/Projects.</li>
<li>The properties pad now shows the tooltip when hovering anywhere on the row, not just the row’s first item.</li>
<li>Windows version is now properly reported for Operating Systems newer than Windows 8.1.</li>
<li>Fixed error initializing task FixedCreateCSharpManifestResourceName when updating Xamarin.Forms NuGet package.</li>
<li>MSBuild diagnostic log displayed after log verbosity changed from diagnostic back to quiet on Windows.</li>
<li>Prevent the reference to unknown project ignored message being displayed when creating new Xamarin.Forms project if Xamarin.Android is not installed.</li>
<li>Add View menu now working with ASP.NET MVC projects.</li>
</ul>

<h3 id="known-issues">Known Issues</h3>
<ul>
<li>Some UITest templates contain references to old NuGets.</li>
<li>Mac updater may fail when used in a non-english locale.</li>
<li>AOT Checkmark in Android settings is not correctly marked as “experimental”.</li>
<li>[Mac] NSLocation.* in Info.plist does not have readable names.</li>
<li>[iOS] iPad Pro is not yet supported.</li>
<li>[iOS] The UI for "Perform all 32-bit float operations as 64-bit float" does not actually enable the option.
	Workaround: manually provide the option `--aot-options=-O=float32` in the "Additional mtouch arguments" of the project's options (iOS build).</li>
<li>System.Reflection.TargetInvocationException error is displayed when adding any other application .mdpolicy file.</li>
<li>Bogus libraries in /usr/local/lib may sometimes cause XS crashes.</li>
<li>The Task Pad cannot be sorted by the "completed" checkbox column.</li>
</ul>


</body></html>
