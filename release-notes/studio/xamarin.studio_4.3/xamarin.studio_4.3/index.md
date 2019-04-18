---
id: DB7C60FE-5E81-4849-8C78-75CD49B0CC9B
title: "Xamarin Studio 4.3"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_4/xamarin.studio_4.2"></head><body>
  
  

<p style='color:red'>The 4.3.x release series is only available in the Alpha update channel for Mac. The main purpose of this release series is to give a preview of the iOS designer.</p>

<h2><a name="5" id="5">Xamarin Studio 4.3.4</a></h2>
<ul>
<li>Add support for Xcode 5.1.</li>
</ul>

<h2><a name="4" id="4">Xamarin Studio 4.3.3</a></h2>
<ul>
<li><b>The iOS Designer needs to be manually enabled in Xamarin Studio 4.3.3 and higher</b>
  <p>
	In order to enable the iOS Designer the new 'Enable experimental iOS Designer' option must be selected. This can be found in the iOS section of the Xamarin Studio preferences.<br>
	<img src="Images/preferences.png">
  </p>
</li>
<li>Adding a new UIPageViewController to the storyboard now shows up in the expected location.</li>
<li>Improved error handling for opening the design surface</li>
<li>Improved support for layout guides</li>
<li>Conflicting or missing constraints are detected in a more reliable way</li>
<li>In constraint mode, selecting multiple items will now display several pinning options<br>
<img src="Images/2014-02-18-1528.png" alt="constraint-snap-bar"></li>
<li>UINavigationBar title text style is now properly rendered and editable<br>
<img src="Images/2014-02-18-1532.png" alt="navigationbar-title-style"></li>
<li>Added support for UITabBarItem.Offset</li>
<li>Newly generated classes will now contain an IntPtr constructor</li>
</ul>

<h2><a name="3" id="3">Xamarin Studio 4.3.2</a></h2>
<ul>
<li><b>Xcode 5.0 is now the minimum supported version of Xcode when using the iOS Designer.</b></li>
<li>Vastly improved experience when designing storyboards in constraint mode.</li>
<li>Added support for asset catalogs inside the design surface.</li>
<li>Images which have both retina and non-retina versions do not show up twice in the image selector.</li>
<li>Improved handling when a property is exported on a class and also on it's super class.</li>
<li>Fixed an issue where the design surface would sometimes throw an exception on startup and could not render any storyboards.</li>
<li>Fixed a regression where UIBarButtonItems could no longer be dropped on UINavigationItems</li>
<li>Custom Controls are now instantiated using their 'IntPtr' constructor instead of the paramterless constructor. This mimics what iOS does at runtime, giving a more consistent experience between the designer and the simulator/device.</li>
</ul>

<h2><a name="2" id="2">Xamarin Studio 4.3.1 (build 5)</a></h2>
<ul>
<li>Fixed a rare (non-fatal) error when opening a storyboard for the first time in a brand new project.</li>
<li>Fixed a code generation regression where the selector name was not being set in Action attributes</li>
<li>Fixed a code generation regression where new classes were not being automatically added to the project</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 4.3.1 (build 3)</a></h2>
<ul>
<li>Improved performance for most editing operations.</li>
<li>Added support for custom UITableViewCell heights.</li>
<li>Added size indicator overlay when resizing items.</li>
<li>Added support for the "Remove at build time" option for constraints.</li>
<li>Added support for setting a name (creating an outlet) for gesture recognizers and custom objects so they can be accessed from code.</li>
<li>Restored ability to add UITabBarItems to UINavigationControllers.</li>
<li>The individual tabs are now rendered on the UITabBarController.</li>
<li>Fixed an issue where deleting an item would throw an exception.</li>
<li>Fixed handling of "button" and "label" font size values that are found in older storyboards.</li>
<li>Fixed calculation of simulated metrics for segues from buttons in a navigation item.</li>
<li>Fixed the custom view exception icon not being clickable right after the view is dropped from the toolbox.</li>
<li>Fixed building iOS projects with mdtool [#16897].</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 4.3.0</a></h2>
<ul>
<li>Full support for all Xcode releases up to 5.0.2</li>
<li>Fixed an issue where items in a UITableView cannot be selected or the selection rectangle appears offset.</li>
<li>Fixed error when adding UITableView header and footer views.</li>
<li>Fixed adding subviews to a UIScrollView.</li>
<li>Better support for custom controls that throw exceptions in their constructors or static constructors.</li>
<li>Support actions with no parameters that are generated by Xcode.</li>
<li>Add support for the iOS 7 Extend Edges property.</li>
<li>Autolayout improvements:
  <ul>
	<li>
	  You can now edit constraints inline from the designer surface:<br>
	  <img src="Images/2013-11-19_1208.png">
	</li>
	<li>When an underconstrained system is detected, constraints guides will turn orange:<br>
	  <img src="Images/2013-11-19_1342.png">
	</li>
	<li>Conflicting size constraints are now shown with the real length they account for:<br>
	  <img src="Images/2013-11-19_1419.png">
	</li>
	<li>Intrinsinc sizes are now correctly taken into account. Default constraints won't be generated when the control has a correct intrinsic size.</li>
	<li>Default constraints should no longer change to 'User' constraints when dragging/dropping.</li>
	<li>Partial support for <a href="https://developer.apple.com/library/ios/qa/qa1797/_index.html">layout guides</a> although editing support of those constraints is not available in this release.</li>
	<li>Fix UITableView footer/header processing in constraint mode.</li>
	<li>Improve constraint markers and dialog appearance.</li>
  </ul>
</li>
</ul>

</body></html>