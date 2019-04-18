---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.7"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.7"></head><body>
  
  

<h2><a name="2" id="2">Xamarin Studio 5.7.2</a></h2>

<h3>iOS Designer</h3>
<ul>
  <li>Fixed one cause of the designer not reliably starting the first time a storyboard is opened.</li>
</ul>

<h3>Android Designer</h3>
<ul>
  <li>The default memory settings for the rendering process have been updated. 
  Addresses <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26026">#26026</a>.</li>
  <li>Added a way to adjust the memory settings for the rendering process. Please refer to the 
  <a href="/guides/android/troubleshooting/questions/android-designer-java-memory/">FAQ article</a> for more information.</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 5.7.1</a></h2>

<h3>iOS Designer</h3>
<ul>
  <li>Deleting an event handler from the 'Events' section of the property panel now removes it from the UI immediately</li>
  <li>We are compatible with the latest release of Xcode 6.2</li>
  <li>Fixed a renderer issue with UIToolBar which could cause ViewControllers to not appear on the design surface</li>
</ul>

<h3>iOS</h3>
<ul>
  <li>Fixed an issue with deploying to simulator</li>
  <li>Fixed an issue with Xcode sync that added incorrect using statement for Foundation when using a Unified template</li>
</ul>

<h3>Android</h3>
<ul>
  <li>Fixed an issue where debug deployment attempts from XS will crash if the project has no TargetFrameworkVersion element in the csproj file</li>
  <li>Fixed an issue with the latest Xamarin Android Player not updating the list of known emulators</li>
</ul>

<h3>Xamarin.Forms</h3>
<ul>
  <li>Fixed an issue with intellisense not recognizing XAML and .g.cs items</li>
</ul>

<h3>Mac</h3>
<ul>
  <li>Fixed an issue in unified full profile projects that allowed framework versions < 4.5</li>
  <li>Clean projects as part of migration step to prevent XamMac and Xamarin.Mac mismatches</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.7</a></h2>

<h3>General</h3>
<ul>
<li>Xamarin Studio on Windows now uses the Taskbar icon to display global task progress.
</li><li>Improved organization of global preferences. The C# options for source analysis have
been moved from the Soruce Code section to a node below Text Editor / Source Analysis.
</li><li>Improved the edit reference dialog. The tab for selecting an assembly now shows a
list of recently selected assemblies instead of the file selector. There is now a Browse
button which can be used to select new assemblies.
</li><li>The startup project name is now stored in the user solution settings file instead of
the .sln file.
</li><li>Find in Files command is now much faster and uses less memory when there are many hits.
</li><li>Application output (and other output pads) now have a Search command.
</li></ul>

<h3>Android</h3>

<h4>Android Package Signing - Property Page</h4>
<p>Package signing properties for an Android application project can now be set
without having to manually edit the .csproj. This is only for Release
configurations, as the “Create Android Package” and “Publish Android Application”
commands are only available for Release configs.</p>

<h4>Android Designer Improvements</h4>
<ul>
<li>Auto-completion support for layout XML files.
</li><li>Preview support for some XML layout attributes.
</li><li>Rendering support Wear round.
</li><li>Fixed crash when opening a lot of layout files.
</li><li>Fix “jumping” visual glitches when selecting items.
</li><li>Aapt errors are now correctly handled and double-clicking them will bring you to the right file/line combination
</li><li>Version chooser will now show values between manifest's minimum API level and target API level
</li></ul>

<h4>Other Android fixes and improvements</h4>
<ul>
<li>Android Apps fail to launch on Lollipop devices when in Release mode with Shared Runtime/FastDevelopment on.
</li></ul>

<p>Known issues:</p>
<ul>
<li>Debug deployment attempts of projects with no Target Framework set will crash. You may experience this issue if your Target Framework is set to either v2.2 or v2.3. The workaround is to set the Target Framework to a different value for debug builds.</li>
<li>Building Classic API projects for the simulator fails if you are not properly provisioned for iOS code-signing. The workaround is to enable the MSBuild build engine for the project in Project Options -> General. <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=25841">#25841</a></li>
</ul>

<h3>Classic to Unified API code migration tool</h3>

<p>The Project / Migrate to Xamarin.iOS and Xamarin.Mac Unified API menu item now also (partially)
migrates project source code to the new API. The following types of changes will be made to the project source code:</p>
<ul>
<li>Statements such as ‘using MonoTouch.Foundation;’ will be modified to ‘using Foundation;’.
</li><li>Usage of System.Drawing types (RectangleF, PointF, and SizeF) will be migrated to their
        respective CoreGraphics equivalents (CGRect, CGPoint, and CGSize).
</li><li>Method overrides on subclasses of MonoTouch classes will be migrated to match their new prototypes.
</li><li>CFRunLoop constants will be migrated to their new names.
</li><li>Calls to DismissModalViewControllerAnimated() will be updated to call DismissModalViewController().
</li><li>Calls to PopViewControllerAnimated() will be updated to call PopViewController().
</li><li>Calls to CGContext.SetShadowWithColor() will be updated to call CGContext.SetShadow().
</li><li>Calls to CGContext.SetRGBFillColor() will be updated to call CGContext.SetFillColor().
</li></ul>

<h3>iOS</h3>

<ul>
<li>Fixed archiving of iOS apps with App Extensions (dSYMs and the archived-expanded-entitlements.xcent files are both archived now).
</li><li>iOS Simulator configurations now default to i386-only for Unified API projects rather than i386+x86_64 to improve build times.
</li><li>Added support for choosing vector images (.pdf’s) for Image Assets.
</li><li>The Info.plist LaunchImage editor now defaults to requesting full-screen images for iOS >= 7.0 instead of the image sizes with room for the status bar.
</li><li>When syncing back from Xcode, *.build directories are now ignored.
</li><li>Fixed Asset Catalog compilation for iOS Library Projects w/o an Info.plist
</li><li>Fixed archiving to pick the correct icon to use in the Archive Organizer window.
</li><li>Fixed the Asset Catalog editor to properly serialize the json for image sizes. (bug #24164)
</li><li>Fixed the Info.plist scheme for NSExtension (for use with the Source tab of the Info.plist editor).
</li><li>Launch file dropdown in project properties is now alphabetically sorted.
</li><li>Application bundle names and the native executable names now use the AssemblyName value (from the .csproj file) as opposed to a sanitized version of the MSBuildProjectName value. This means that if the AssemblyName has periods, then so will the application bundle directory name and the native executable name within the app bundle. (bug #1532)
</li></ul>

<h4>iOS Designer Improvements</h4>
<ul>
  <li>Full support for Xamarin.iOS Unified projects.
  </li><li>SCNView, UIScreenEdgePanGestureRecognizer, UIVisualEffectView, UISplitViewController are all fully supported now.
  </li><li>Significantly improved support for UICollectionView and UICollectionViewLayout.
  </li><li>Added support for aspect ratio based constraints.
  </li><li>UITabBarController will no longer randomly disappear when creating new Tab segues.
  </li><li>Removed the ability to delete the NavigationBar from a UINavigationController. iOS will crash at runtime if you try this. 
  </li><li>Constraints can now be exposed as an Outlet or custom class. 
  </li><li>Fixed an issue changing the style of a UITableViewCell when constraints are disabled. 
  </li><li>Fixed several issues where the property panel would write incorrect Xml to the storyboard.
  </li><li>Custom fonts are fully supported by the design surface and font picker.
  </li><li>Fixed a case where old assemblies were sometimes used to render custom controls.
  </li><li>Embed segues can now be created from Container Views.
  </li><li>Fixed an rare issue where views with zero width or zero height could break the designer.
  </li><li>Fixed a crash when deleting the segments inside a Segmented Control.
  </li><li>Custom properties of type 'float' and 'double' should work now.
  </li><li>Elements inside a UIScrollView will no longer change their position every time we render the storyboard.
  </li><li>Added support for UITextAlignment.Justified and UITextAlignment.Natural
  </li><li>Fixed an exception when right clicking on a Size constraint
  </li><li>The localization ID for UIView/UIViewController is displayed in the property panel now.
  </li><li>Improved support for UIViewController.PreferredStatusBarStyle.
</li></ul>


<h3>Mac</h3>

<h4>Full framework support for Xamarin.Mac</h4>
<p>Unified API applications now support building against full desktop .NET frameworks in
addition to the default Xamarin.Mac mobile framework. <b>Full frameworks/profiles
are completely unsupported by Xamarin</b>, but this option now exists to help legacy
applications port to the mobile framework while still taking advantage of all
the new features in Unified API.</p>

<p>The target framework can be changed from Xamarin.Mac mobile to full desktop .NET under
the regular Project Options → Build → General → Target Framework UI.</p>

<h4>Other Mac fixes and improvements</h4>
<ul>
<li>Fixed Info.plist editor to allow setting storyboard files as the Main Interface (bug #23997)
</li><li>Added UI for using the new ref-counting mechanism in the Mac Build Settings.
</li></ul>

<h3>Sketches</h3>

<p><b>Note that Sketches is still considered an early preview. It is by no means complete or
necessarily stable, even though we have made scores of stability and feature improvements
since the Evolve release. Sketches will be an ongoing preview bundled within Xamarin Studio
for many months to come.</b></p>

<h4>New visualizations</h4>
<p>Many new quick look visualizations are supported:</p>
<ul>
<li><b>Mac/iOS</b>: CGPoint, CGRect, CGSize, CGPath, NSBezierPath, NSFont, CGFont, NSColor, CGColor, NSUrl, NSAttributedString, NSGradient, CGGradient, CGLineCap, CGLineJoin, CGImage, NSImage, NSView, NSButtonType, CIColor, CIImage, CICrop, UIImage, UIView
</li><li><b>System.Drawing</b>: Point, PointF, Size, SizeF, Rectangle, RectangleF, Color, Image, Brush, Font, Pen
</li><li><b>Android</b>: Point, PointF, Rect, RectF
</li><li><b>BCL</b>: Uri, enums
</li></ul>

<h4>Resource bundling</h4>
<p>Resource bundling is now supported. Resources can be accessed in iOS and Mac directly
from the main NSBundle (e.g. direct use of say NSImage.ImageNamed is now supported).</p>

<p>There is not yet a UI available for embedding resources, however if a Sketch has
the name MySketch.sketchcs, then you can create a directory next to the file
called MySketch.sketchcs.Resources, and any files in that directory will be
available within the sketch. A general purpose API for all platforms is
GetResourcePath(string resourceName). This will return a full path to a
resource, and is the only way to access a named resource on Android currently.
NSBundle.MainBundle can be used as expected on Mac and iOS.</p>

<h4>File format changed to Markdown</h4>
<p>The file format for a Sketch is now Markdown. While there is no immediate
benefit to this, we will be taking advantage of Markdown features in the future
and wanted to stabilize sooner than later on the basic file format.</p>

<p>Metadata (e.g. resource information) is stored within an XML code fence,
followed by C# or F# in respective code fences. While arbitrary Markdown content
outside of fences should be preserved, it will not be displayed inside
Xamarin Studio. We still recommend only editing Sketch files in Xamarin Studio.</p>

<h4>Classic iOS API not supported</h4>

<p>The Classic iOS API is no longer supported. Sketches will focus only on the
Xamarin iOS and Mac Unified API going forward as Apple will be phasing out 32-bit
iOS applications completely soon. Xamarin.Forms sketches are now available under
the Unified iOS API.</p>

<h4>Other fixes and improvements</h4>

<ul>
<li>Android support is much more stable: we fixed a networking issue that was
very apparent under Android while much less so under Mac and iOS.
</li><li>Mac support now has a RootWindow property defined for exploring live Cocoa UI.
</li><li>Multiple Sketches with the same platform target (e.g. iOS) may now be opened
at the same time within Xamarin Studio
</li><li>.sketchcs and .sketchfs files are now registered to open with Xamarin Studio
</li></ul>

Many other bug fixes and stability improvements have been introduced since the Xamarin Studio 5.6 Evolve preview.

<h3>Version Control</h3>

<ul>
<li>Fixed crash when opening a project that uses an incompatible Subversion Working Copy format.
</li><li>Several optimization and fixes in the Version Control status view.
</li><li>Version Control Log view now displays a default icon for emails which aren’t linked on Gravatar.
</li><li>Fixed: Xamarin Studio crashes when viewing SVN log on Mac OS.X 10.10.
</li></ul>

<h3>NuGet</h3>
<ul>
<li>Menu options for add-in NuGet packages have been renamed to make them easier to discover, so for
example instead of "Add Package" we now have "Add NuGet Package".
</li><li>Error and warning icons applied to packages are now more consistent with other icons in the solution pad.
</li><li>Fixed: Xamarin Studio doesn't recognize that files exist after NuGet Update.
</li><li>Fixed: Update all Packages in Solution not Updating Dependencies.
</li><li>Fixed: Unable to add NuGet package again after removing it.
</li></ul>

<h3>Profiler</h3>
<ul>
<li>Profiling works for F# apps
</li><li>Integration with Xamarin Profiler has been added for iOS and Android applications.
To start profiling an application, you can use either the Run menu or Right click on a
project and select Start Profiling. You can also launch the profile as a standalone application from Tools -> Launch Profiler.
</li><li>New options to enable developer instrumentation have been added into Android and iOS projects’ Build Options.
These are not retroactive and you will be asked to enable them if the project’s build configuration doesn’t have them when profiling is requested for it.
</li></ul>

<h3>Debugger</h3>

<ul>
<li>Hex debugger visualizer now shows a wider range of characters.
</li><li>Fixed: Cannot use typeof operator with type parameters.
</li><li>Fixed: New breakpoint dialog shows Unix filepath example on Windows.
</li><li>Fixed: Debugger reports a 'System.NotSupportedException' exception when using Set Next Statement command.
</li><li>Fixed: Variable called dynamic confuses debugger.
</li></ul>

<h3>Source Code Editing</h3>
<ul>
<li>Fixed: Unable to remove custom code template.
</li><li>Fixed: Semicolon is put at the end of line instead at the position of cursor.
</li><li>Fixed: Sort usings yields strange result
</li><li>Fixed: Navigate Forward/Backward may cause a crash when used in rapid succession.
</li><li>Fixed: Editor tooltips overlay new windows.
</li><li>Fixed: Completion is not working for 'is' statement.
</li><li>Fixed: Rename refactoring command fails with InvalidCastException on generic class name after 'new'.
</li><li>Fixed: Xamarin Studio not recognizing reflection extensions in PCL when Microsoft.Net.Http is present.
</li><li>Fixed: #define code showing as comments if symbol is not declared in build options.
</li><li>Fixed: Folding markers not correctly shown when the columns for #region and #endregion differ.
</li><li>Fixed: C# string property in object initializer autocompletes to #if.
</li><li>Fixed: Cannot open .cshtml files.
</li></ul>

<h3>Other fixes and improvements</h3>
<ul>
<li>Fixed: After the Update was installed, Windows did a forced restart.
</li><li>Fixed delay when opening the project context menu.
</li><li>Fixed: Deleting a folder in the solution pad does not result in the folder being removed from the tree.
</li><li>Fixed occasional crash when deleting a solution folder while the properties pad is visible.
</li><li>Fixed: Copying info in the test output window results in wrong text being copied.
</li><li>Fixed: Xamarin Studio throws exception on doing Export Policy to specific file.
</li><li>Fixed exception while creating VBNet->NUnit Library Project.
</li><li>Fixed: Cannot change font of the Test Results pad (e.g. to monospace font).
</li><li>Fixed: Nunit runner has trouble when class with TestFixture is defined without a namespace.
</li><li>Fixed: Time summary not correctly shown in Unit Tests pad.
</li><li>Fixed T4 TextTransformation interface issue with Initialize.
</li><li>Fixed: T4 ignores output directive if PreprocessTemplate() is used.
</li><li>Fixed: 'Load previous solution on startup' option breaks loading projects from the command line.
</li><li>Fixed: Removing reference to a shared project from project references causes UI freeze.
</li><li>Fixed: Enabling MSBuild Support in a Xamarin.Forms Shared Project doesn't build.
</li><li>Fixed: [Windows] Xamarin Studio Updater window displays wrong number of installing updates.
</li><li>Fixed: Go to Definition opens the assembly browser, but does not show the correct type.
</li><li>Fixed: File appears twice when searching.
</li><li>Fixed: "Add Package Source" popup window should remain at top.
</li></ul>

</body></html>
