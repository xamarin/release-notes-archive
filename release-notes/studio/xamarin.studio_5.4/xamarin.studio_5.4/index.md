---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.4"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.4"></head><body>
  
  

<h2><a name="0" id="0">Xamarin Studio 5.4</a></h2>

<h3>Xamarin Designer for iOS</h3>
<ul>
  <li>Improved support for Xcode6 Beta GM
  </li><li>Rendering support for the new 4.7" and 5.5" resolutions has been added
  </li><li>Added support for the new @3x style images
  </li><li>Images with ~iphone or ~ipad appended to their name should be handled correctly by the property panel image selector now.
  </li><li>Fixed a crash when using Xcode 6 and selecting a UIActivityIndicatorView on the surface
  </li><li>Fixed a rendering glitch where controls could not be made smaller than 88 pixels in height in certain circumstances.
  </li><li>Initial support for unified storyboards. This is also known as 'Size Class' support.
  </li><li>Fixed many property panel issues with UISearchBar, UITableView, AttributedStrings and more.
  </li><li>Enhanced error logging when custom controls cause issues.
  </li><li>Fixed a bug whereby autoresizingMask values could be incorrectly applied when in constraint mode
  </li><li>Improved handling of 'Modal' segues when rendering simulated metrics
  </li><li>The TabBar inside a ProxiedTabBarController is now selectable with the mouse
  </li><li>A failed drag/drop of a view will correctly restore the ViewController to it's original state. This was just a cosmetic issue.
  </li><li>TableView Headers/Footers do not set 'translatesAutoResizingMaskIntoConstraints' to false anymore. iOS does not support this at runtime.
  </li><li>Double clicking on a Button to generate an action no longer makes the button jump around when you tab back to the design surface
  </li><li>The design surface should no longer jump when selecting items, creating constraints or using the embedded constraint editor
  </li><li>UITableViewSection elements can no longer be dropped in invalid locations
  </li><li>Custom Controls work correctly when using MonoTouch 7.9 or higher
  </li><li>'View As iOS6.1 and earlier' now works with Xcode6
  </li><li>Some small rendering performance improvements
  </li><li>Several repainting issues have been fixed on the design surface
  </li><li>Implemented support for constraint multipliers in the form 1/2 or 4/9, etc.
  </li><li>The light style for UIStatusBar is now fully supported
</li></ul>

<h3>iOS</h3>
<p>This release adds support for the iOS 8 SDK, including:
<ul>
<li>Support for the new 4.7" and 5.5" launch images has been added to the Asset Catalog editor.
</li><li>Support for the new iOS 8 icon sizes has been added to the Asset Catalog editor.
</li><li>Support for launch screen xibs and storyboards has been added to the Info.plist editor.
</li><li>Support for the new Unified API (see Xamarin.iOS release notes for more details).
</li><li>Support for iOS App Extensions. There are several new templates for creating extensions.
</li><li>Support for compiling *.scnassets directories (files within a *.scnassets folder should have their BuildAction set to “SceneKitAsset”).
</li><li>Support for compiling *.metal files (BuildAction set to “Metal”).
</li><li>Support for compiling standalone *.sks and *.scnp files (should all have their BuildActions set to “BundleResource”).
</li><li>Support for building *.doa files (BuildAction set to “Collada”).
</li><li>New file templates for creating *.metal files.
</li><li>New SceneKit and SpriteKit particle system file templates.
</li><li>Allow jpegs to be included in asset catalogs and also allow them to contain other folders
</li></ul>

<p>In order to build the new file types, the MSBuild engine must be enabled in the project options (Build/General section).</p>

<h3>Xamarin.Mac</h3>

<p>Xamarin Studio 5.4 includes support for the new Unified API. Please see the Xamarin.Mac release notes for more details.</p>

<h3>Components</h3>
<ul>
<li>Added support for installing Components that target the new Unified API for iOS or Mac.
</li></ul>

<h3>NuGet Support</h3>
<ul>
<li>Added support for the new Unified target frameworks for iOS (Xamarin.iOS) and Mac (Xamarin.Mac).
</li></ul>

<h3>Other Improvements and Bug Fixes</h3>
<ul>
<li>Fixed crash when running the "Go to Declaration" command on types defined in packages.
</li><li>Fixed Autocomplete (Intellisense) for XAML files in Xamarin.Forms project.
</li><li>Fixed several editing issues in the Hex debugger visualizer.
</li><li>Fixed display of list items in the debugger.
</li><li>Fixed: XML Format document removes all undo history.
</li><li>Control-shift-Z shortcut in the editor.
</li><li>Allow copying text from the Tests Results pad.
</li><li>Fixed "could not add packages" error while creating a Xamarin.Forms solution with a bad network connection.
</li></ul>

</body></html>
