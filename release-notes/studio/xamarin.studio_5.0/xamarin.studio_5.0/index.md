---
id: DB7C60FE-5E81-4849-8C78-75CD49B0CC9B
title: "Xamarin Studio 5.0"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.0"></head><body>
  
  


<h2><a name="0" id="0">Xamarin Studio 5.0</a></h2>
<h3>Shell</h3>

        <p>The Xamarin Studio shell has been reviewed to make sure it looks awesome in retina displays.
	We have new beautiful icons and a number of other visual enhancements like the new welcome page,
        fine-tuned toolbar status bar, about dialog and Windows splash.</p>

        <img src="retina.png">


<h3>NuGet Support</h3>
        <p>NuGet support is now included by default in Xamarin Studio, with a brand new user interface.
        The new Add Packages dialog allows NuGet packages to be searched for and installed into a project.</p>

        <p>Add Packages Dialog can be opened using the <i>Project → Add Packages</i> menu option, or from the Solution pad by right
        clicking the project and selecting <i>Add → Add Packages</i>, or by right clicking the Packages folder
        and selecting Add Packages. Double clicking the Packages folder also opens the dialog.</p>

        <p>In the top right of the dialog is the search text box. The Add Packages dialog will search for packages as you type.
        Alongside the normal free text search, the search text box supports searching for packages by the ‘tags’, ‘id’, ‘description’
        properties if the package source supports these. For example: "id:NUnit", "tags:fsharp", "description:mono".
        Recently used packages are shown first in the packages list for the current Xamarin Studio session.</p>

        <p>NuGet packages installed in a project are shown in the new Packages folder, under the project node in the Solution pad.
        References added by packages are shown in the new "From Packages" folder under the References folder, under the project node.</p>

        <p>NuGet packages will be automatically restored on opening a solution. Automatic NuGet package restore can be enabled/disabled
        in Preferences / Packages / General. NuGet package restore can be started manually by selecting <i>Project → Restore Packages</i>,
        right clicking the solution and selecting Restore Packages, or right clicking the Packages folder and selecting Restore.</p>

        <p>Package sources can be configured in Preferences / Packages / Sources. Double click a package source to update an existing source.
        To reorder the packages, drag and drop a source in the list. Package source credentials can be configured for feeds that require authorization.
        Invalid credentials or package source urls will be highlighted in the list of sources.</p>

<img src="nuget.png">

<h3>Xamarin Designer for iOS</h3>
<p>The Xamarin Designer for iOS is a visual designer for the iOS Storyboard format which is fully integrated into Xamarin Studio.
The iOS Designer maintains full compatibility with the Storyboard format, so that files can be edited in either Xamarin Studio
or Visual Studio in addition to Xcode's Interface Builder. Additionally, the Xamarin Designer for iOS supports advanced features
such as custom controls that render at design-time in the editor.</p>

<img src="ios-designer.png">

<h3>F#</h3>
        <p>F# support is now included by default in Xamarin Studio, with all templates for building Android and iOS apps.
                No external add-ins are required.</p>

<h3>Projects</h3>
	<ul>
                <li>Added Xamarin.Forms project templates.
		</li><li>Added Shared Assets Projects support.
		</li><li>The default PCL profile has been changed to Profile78 (.NET 4.5, Windows Phone 8, Windows Store 8, Xamarin.Android, Xamarin.iOS).
		</li><li>Added support for loading (not building) Windows Phone 8 and iOS projects in Xamarin Studio on Windows.
		</li><li>The “search for new files on project load” feature has been removed in favor of MSBuild wildcards in project files.
		</li><li>The resx file template is now available for all .NET project types.
		</li><li>Fixed resx codebehind generation for PCL projects.
		</li><li>The VS2012 solution format is now used by default, compatible with Visual Studio 2010 SP1 and later.
	</li></ul>
<img src="forms.png">

<h3>Source Editing</h3>
	<ul>
		<li>Added simple code completion when editing MSBuild project files.
		</li><li>The source editor now recognizes defines set automatically by the build system such as __ANDROID__.
		</li><li>Improved visual appearance of Source Code Analysis.
		</li><li>Derived symbol finding is much faster now.
		</li><li>Usage highlighting is now displayed in source analysis bar.
	</li></ul>

<h3>Version Control</h3>
<ul>
	<li>Fixed ‘Subversion Operation is already in progress’ issues.
	</li><li>Fixed issues with being able to delete current branch in Git.
	</li><li>Fixed IDE hanging when managing tags in Git.
	</li><li>Added support for upgrading Subversion repositories and reporting if the Subversion working copy is too new to handle.
	</li><li>Fixed an exception thrown when double clicking on Log diff.
	</li><li>Improved experience with the Checkout Dialog when handling invalid URLs, non-empty checkout directories and invalid credentials.
	</li><li>Fixed an issue which allowed users to make a commit with an empty message.
	</li><li>Changed Version Control Remove command’s confirmation text to “Remove” instead of “Delete” to prevent confusion of what will happen.
	</li><li>Remote Status button has been removed from Review and Commit for Git.
	</li><li>Optimized Review and Commit diff loading.
	</li><li>Optimized switching to Changes View when double clicking a diff in the Log.
</li></ul>

<h3>Android</h3>
	<ul>
		<li>The AndroidAsset build action is now set correctly on new files.
		</li><li>Android Designer: Several fixes in alternative layout management.
		</li><li>The debugger now connects more reliably to the Android emulator.
	</li></ul>

<h3>iOS</h3>
	<ul>
		<li>Added support for simulating app launch via Background Fetch.
		</li><li>Added check to ensure that Content and BundleResource files don't conflict with the native exe.
	</li></ul>

<h3>Mac</h3>
	<ul>
		<li>Bundles are now codesigned with the Entitlements even if no provisioning profile has been specified.
	</li></ul>

<h3>Debugger</h3>
	<ul>
		<li>Generic methods now can be invoked in the Immediate Window.
		</li><li>Win32 debugger
			<ul>
				<li>Fixed evaluation of private fields.
				<li>Implemented "Step over properties and operators" setting.
				<li>Fixed unnecessary stepping at beginning and end of methods.
				<li>Fixed unnecessary step when step finished on line with breakpoint.
			</li></li></li></li></ul>
	</li></ul>

<h3>Web References</h3>
	<ul>
		<li>Added possibility to choose whether you want to generate Asynchronous methods when using Web References.
		</li><li>Fixed issues with PCL and Web References.
		</li><li>Added Delete All context action for Web References Folder.
		</li><li>Split Web References folder into Web References and Web Services.
	</li></ul>

<h3>Other Improvements and Bug Fixes</h3>
	<ul>
		<li>Fix execution target list unexpectedly changing.
		</li><li>The Test Pad now only shows tests that will be built in the active configuration.
		</li><li>Added PublicResXFileCodeGenerator custom build tool
		</li><li>Improved french translation
		</li><li>Fixed crash when using the Hex debugger visualizer
		</li><li>Files in the solution are now sorted by file name without extension.
		</li><li>When grouped files are ungrouped in the solution pad, this change will now be persisted correctly.
		</li><li>MSBuild project loading errors are now reported back to the build output pad.
		</li><li>The correct font is now used in custom UI elements on Windows.
		</li><li>ASP.NET file templates are now usable from ASP.NET MVC projects.
		</li><li>It’s no longer possible to create custom policies with null or invalid names.
		</li><li>Component references can now be removed from projects even when they are corrupt/invalid.
		</li><li>Downloaded updates are now kept in the cache when switching updater channels, and the cache is periodically pruned.
		</li><li>Files in the update download cache now have user-friendly names.
		</li><li>VI status area no longer hangs on some systems
	</li></ul>

</body></html>
