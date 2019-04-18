---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.5"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.5"></head><body>
  
  

<h2><a name="4" id="4">Xamarin Studio 5.5.4</a></h2>

<h3>Android</h3>
<ul>
<li>Android Lollipop support
</li><li>Fixed: when editing the android application settings via the property page it sets the manifest encoding to windows-1252.
</li></ul>

<p>If your Android project was targeting the Android L Preview, you'll need to update your Android XML manifest to change version information from L to 21. Additionally, you should retarget your project's framework to use version 5.0 or, alternatively, set it to use the latest available framework version.</p>

<h3>iOS</h3>
<ul>
<li>Fixed iCloud issue that caused failures when deploying to device.
</li><li>Fixed occasional crash in the assets editor.
</li><li>Fixed crash when opening image set.
</li><li>Fixed: Xcode quits when Xamarin Studio is trying to sync with Xcode.
</li><li>Fixed: size property in xcassets incorrectly created.
</li></ul>

<h3>Xamarin Designer for iOS</h3>
<ul>
  <li>Constraints can now be made 'Outlets' and they can also be made Custom Classes.
  </li><li>The 'Indicator Insets' property of UIScrollView can now be edited correctly in the property panel
  </li><li>Several property panel issues with UITextField have been fixed
  </li><li>Prevented selection markers from being left permanently on the design surface
  </li><li>Improved layout guide support in UIContainerView
  </li><li>Fixed an issue changing a segue to be 'Model' via the property panel
  </li><li>Fixed a bug where setting UITableViewCells to Left Detail, Right Detail or Subtitle would prevent Xcode from opening the storyboard.
  </li><li>Fixed a bug opening legacy storyboards which have not been upgraded to at least Xcode 5.0 format.
</li></ul>

<h3>Version Control</h3>
<ul>
<li>Fixed error when adding a new folder to a Subversion controlled project.
</li><li>Fix crash when opening a project with an unsupported Subversion working copy format.
</li><li>Fixed crash when creating a Subversion commit
</li></ul>


<h3>Other bug fixes and improvements</h3>
<ul>
<li>Fixed gravatar images not showing on retina screens
</li><li>Fixed: Really wide "The Debugger Is Busy" dialog
</li><li>Fixed: In External Tool, make ${FileName} resolve to the file name without extension, as in VS
</li><li>Fixed: Shared Projects do not work unless you readd reference (Windows)
</li><li>Fixed: Format XML document which has duplicated attributes removes all text
</li><li>Fixed crash in Assembly Browser
</li><li>Fixed occasional freeze when showing the editor context menu.
</li></ul>

<h2><a name="3" id="3">Xamarin Studio 5.5.3</a></h2>

<p>This is a hotfix release that includes the following fixes:</p>
<ul>
	<li>Fixes the inability to launch iOS 8.1 simulators installed by Xcode 6.1.</li>
	<li>Fixes a code signing issue on default classic Xamarin.Mac projects caused by changes in Gatekeeper.</li>
	<li>Fixes disabled menu items in full screen mode on Yosemite.</li>
	<li>Fixes an occasional crash when closing an iOS designer view.</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.5</a></h2>

<h3>Xamarin Android Player support</h3>

<p>When Xamarin Android Player is installed, downloaded emulator images
will be shown in the execution target selector in the toolbar. A new emulator
instance will be started if necessary when starting a debugging session.</p>

<h3>Components and NuGet Packages</h3>
<h4>Support NuGet package dependencies in Components</h4>

<p>A Component from <a href='https://components.xamarin.com/'>Xamarin's Component Store</a> can now declare a dependency on one or
more NuGet packages which will be installed into the project when the Component is installed.</p>

<p>The NuGet packages a Component depends on are displayed in the Packages tab on the Component
Details page in Xamarin Studio.</p>

<h4>Support package version constraints in NuGet packages.config file</h4>

<p>NuGet allows you to <a href='http://docs.nuget.org/docs/reference/versioning'>define a range of package versions that are allowed in your project</a>,
as shown below.<p>

<pre><code class=" syntax brush-C#">&lt;package
    id="jQuery"
    version="1.4.1"
    targetFramework="net40"
    allowedVersions="[1.4.1,1.8)" /&gt;</code></pre>

<p>Xamarin Studio now supports these constraints when updating your NuGet packages or
checking for package updates. Updating NuGet packages from the Solution window will now only
update to a NuGet package that meets the version constraints. Similarly the Solution window will
only show NuGet package updates being available for those updates that meet the constraints</p>

<h3>iOS</h3>
<ul>
<li>New SceneKit Game project templates.
</li><li>Basic migration support from Classic API projects to Unified API projects.
</li><li>Several fixes in iOS 8 project templates.

</li><li>Fixed iOS unit test projects referencing an iOS application project.</li></ul>

<h3>Android</h3>
<ul>
<li>Virtual devices are now shown in the Run With menu, so it is possible to launch the application with a specific device (just like if it was selected in the targets combo in the toolbar).
</li><li>Fix errors with launching emulators with spaces in the name.
</li><li>Fix for not being able to start emulators on Mac.
</li></ul>

<h3>Xamarin Designer for iOS</h3>
<ul>
  <li>Actions, Outlets and new types are now generated for projects based on the Xamarin.iOS Unified API.
  </li><li>Custom properties should always show up in the correct section in the property panel.
  </li><li>The PreferredStatusBarStyle value for custom UIViewControllers is respected by the designer.
  </li><li>Fixed a potential crash when changing a segue from a custom type to a built in type.
  </li><li>Much improved support for constraints made against the margin of a superview/sibling view.
  </li><li>Some checkbox based properties did not display the correct initial value in the property panel.
  </li><li>Changing the 'Breaking mode' in WebView should work correctly now
  </li><li>Altering the text traints in UITextField should work correctly now
  </li><li>Setting the 'selectedImage' property of UITabBarItem correctly updates the storyboard
</li></ul>

<h4>Changes to custom control rendering</h4>
<p>
  Over the last several months we have realised that the majority of custom controls are
  unsafe to execute by default inside the designer. They typically rely on data provided by
  the application, but that data is not available when run inside the designer and so they just throw exceptions.
</p>
<p>
  To provide a better experience for people we have made custom control support opt-in rather than
  than enabled by default. To load up a specific UIView or UIViewController as a custom control you
  must either implement <pre><code class=" syntax brush-C#">System.ComponentModel.IComponent</code></pre> or annotate the class with <pre><code class=" syntax brush-C#">[DesignTimeVisible (true)]</code></pre>
</p>

<h3>Other Improvements and Bug Fixes</h3>
<ul>
<li>[Mac] Menu items now show a description of the command in the tooltip.

</li><li>Fixed Xaml completion when using shared asset projects</li><li>Fixed crash in Subversion support ("Another Subversion operation is already in progress" error).



</li><li>Fixed an IndexOutOfRangeException when opening a file with custom added encoding.</li><li>Fixed an issue where shared asset project references would be forgotten between Xamarin Studio restarts.</li><li>Fixed an crash that would occur rarely when reloading a file that changed outside of XS.</li><li>The text editor doesn't lose focus anymore when switching shell layouts.
</li><li>Fixed occasinal crash when changing from 2 to 1-column mode.

</li><li>The full Xamarin.Android version is now available in the about box.</li></ul>

</body></html>
