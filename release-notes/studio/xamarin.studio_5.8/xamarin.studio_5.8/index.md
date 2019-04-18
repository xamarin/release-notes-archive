---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.8"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.8"></head><body>
  
  
  
<h2><a name="3" id="3">Xamarin Studio 5.8.3</a></h2>
<h3>General</h3>
<ul>
        <li>Fixed: WatchKit app submission fails. Please note that the submission process for WK apps currently requires creating an archive and submitting through Xcode. Submitting an .ipa directly is not yet supported.</li>
</ul>


<h2><a name="2" id="2">Xamarin Studio 5.8.2</a></h2>
<h3>General</h3>
<ul>
        <li>Fixed: Breakpoints cause iOS Simulator to freeze</li>
        <li>Fixed: Error while saving json when editing LaunchImage.launchimage</li>
        <li>Removed WatchKit launch images (not supported anymore in Xcode 6.2)</li>
        <li>Updated WatchApp App Icons asset catalog UI for Xcode 6.2 final</li>
        <li>Fixed: WatchKit app submission fails.</li>
</ul>

<h3>iOS Designer</h3>
<ul>
  <li>Fixed a performance regression which could cause reloads to take multiple seconds to complete</li>
  <li>Restored the 'Identity' panel for UIBarItem and several other widgets</li>
  <li>Fixed an issue triggered when using UISplitViewController on Yosemite and Xcode 6.2</li>
  <li>The editor for the Constraint 'Multiplier' property has much improved support for values in the form `1:2` or `3/4`</li>
  <li>Fixed several cases where incorrect resize handles appear when an item was selected on the design surface</li>
  <li>Several property panel related default values have been fixed for UIDatePicker and countdown timer</li>
  <li>Resizing a UITableViewCell now works as expected using either the resize handle or the property panel</li>
  <li>UISegmentedControl.ContentOffset is taken into account on the design surface</li>
  <li>WKGlanceControllers can now be made custom classes.</li>
  <li>WKInterfaceTimer now renders correctly when it's properties are changed</li>
  <li>The arrow representing the 'Notification Category' now shows up on the design surface</li>
  <li>WKInterfaceSwitch and WKInterfaceImage tint colours render on the surface now</li>
  <li>Added support for WKNotificationCategory sash color</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 5.8.1</a></h2>

<ul>
	<li>Added support for fast build checks. This feature reduces the time it takes to check if a project needs to be built,
	so starting an app is much faster when no code changes are made.</li>
	<li>Fixed issue that caused breakpoints to be ignored in some cases on Windows.</li>
	<li>Fixed: Tapping on a file or folder in the solution pad of a shared project causes the project to collapse</li>
	<li>Fixed: On adding a XAML file to a Forms Shared project, Xamarin Studio gives error message</li>
	<li>Fixed: Find and Replace in files changes the wrong strings</li>
	<li>Fixed: Publish Android package should sign with SHA1 on 4.2 and below</li>
	<li>Minor fixes in the WatchKit app templates</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.8</a></h2>

<ul>
  <li>The Xamarin Studio 5.8 release adds full support for iOS 8.2 and WatchKit. You can now visually design, launch, and debug WatchKit apps in App, Glance, and Notifications mode.</li>
  <li>We've added full documentation in the <a href="/guides/ios/watch">Xamarin Developer Portal</a>. The Visual Studio toggle is available in the appropriate guides at the top right of the screen to customize your docs experience for XS.</li>
  <li>Sample code for Xamarin Watch apps is available from the <a href="/samples/ios/Watch/">Xamarin Samples Repository</a>.</li>
</ul>
<h3>Known issues:</h3>
<ul>
  <li>A list of known issues and workarounds is available <a href="/guides/ios/watch/advanced/#knownissues">here</a>.</li>
</ul>

</body></html>
