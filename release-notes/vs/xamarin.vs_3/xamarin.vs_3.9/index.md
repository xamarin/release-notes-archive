---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.9"
---

<html>
<head>
<meta content="text/html; charset=ISO-8859-1" http-equiv="content-type">
<title></title>
</head>
<body>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">



<h2><a name="0" id="0">Xamarin 3.9</a></h2>
<p>
<a name="0" id="0">Xamarin 3.9 updates
</a><a href="/releases/ios/xamarin.ios_8/xamarin.ios_8.8/">Xamarin.iOS
8.8</a> and
<a href="/releases/android/xamarin.android_4/xamarin.android_4.20/">Xamarin.Android
4.20</a> releases,
and support for iOS 8.1 development.</p>

<p>

<a name="0" id="0">Xamarin 3.9.547 updates
</a><a href="/releases/ios/xamarin.ios_8/xamarin.ios_8.9/">Xamarin.iOS
8.9</a> and support for iOS 8.3 development.


</p>
<h4>v.3.9 Service Release 4</h4>
<h5>General</h5>
<ul>
  <li>Fixed issue making WatchKit applications created from VS template unable to run on notification mode.</li>
  <li>Fixed Build Signing identities disappearing when changing build configurations on iOS Bundle Signing project properties page.</li>
  <li>Resolved <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=28027">Bug 28027</a> : causing for some setups VS cannot debug on physical iOS devices.</li>
  <li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=27990">Bug 27990</a> Can't load NIB when XIB is in a subfolder of the project.</li>
</ul>
<h5>iOS Designer</h5>
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

<h5>Known issues for SR4</h5>
<ul>
  <li><b>Submission of WatchKit applications built from Visual Studio will fail with an "Invalid WatchKit Bundle" error.</b> Please refer to the <a href="guides/ios/watch/deployment/appstore/">WatchKit app submission guide</a>.</li>
  <li>Stop debugging the WatchApp will not kill the WatchApp process and it will still open.</li>
  <li>If there is no iOS App project referencing the WatchKit Extension, an "error MT1217: Could not load the app bundle at ..." is thrown at build time. To fix this error you need to add an iOS App project referencing the WatchKit extension.</li>
  <li>For a brief period of time, v3.11.536 was available in the updater channels. That version exhibited a regression when building WatchKit applications and was rolled back. If you are experiencing this issue and are using v3.9.536, please check for updates.</li>
</ul>
<h4>v.3.9 Service Release 3</h4>
<ul>
  <li>Fixed random crashes of Visual Studio on certain locales.</li>
  <li>Made physical devices always show in the dropdown for iOS.</li>
  <li>Fixed an issue causing the Info.plist editor layout to overlap for WatchKit projects in some displays.</li>
  <li>WatchKit template adds a reference from WK Extension project to Watch App on unfold.</li>
</ul>

<h4>v.3.9.483</h4>
<ul>
  <li>The Visual Studio 3.9.483 release adds full support for iOS 8.2 and WatchKit. You can now visually design, launch, and debug WatchKit apps in App, Glance, and Notifications mode.</li>
  <li>We've added full documentation in the <a href="/guides/ios/watch">Xamarin Developer Portal</a>. The Visual Studio toggle is available in the appropriate guides at the top right of the screen to customize your docs expereince for VS.</li>
  <li>Sample code for Xamarin Watch apps is available from the <a href="/samples/ios/Watch/">Xamarin Samples Repository</a>.</li>
</ul>
<p>Known issues:</p>
<ul>
  <li>A list of known issues and workarounds is available <a href="/guides/ios/watch/advanced/#knownissues">here</a>.</li>
</ul>

<h4>v.3.9.483</h4>
<ul>
  <li>The Visual Studio 3.9.483 release adds full support for iOS 8.2 and WatchKit. You can now visually design, launch, and debug WatchKit apps in App, Glance, and Notifications mode.</li>
  <li>We've added full documentation in the <a href="/guides/ios/watch">Xamarin Developer Portal</a>. The Visual Studio toggle is available in the appropriate guides at the top right of the screen to customize your docs expereince for VS.</li>
  <li>Sample code for Xamarin Watch apps is available from the <a href="/samples/ios/Watch/">Xamarin Samples Repository</a>.</li>
</ul>
<p>Known issues:</p>
<ul>
  <li>A list of known issues and workarounds is available <a href="/guides/ios/watch/advanced/#knownissues">here</a>.</li>
</ul>

<h4>v.3.9 Service Release 2</h4>
Bug Fixes:
<ul>
  <li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26122">Bug 26122</a> - Debugging Android project causes real time antivirus to spike CPU
  </li><li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26606">Bug 26606</a> - XIB files within iOS Class Libraries cause "Cannot copy ... /builds/$(BuildSessionId)/obj/ ... .nib ... as the source file doesn't exist"
  </li><li>Zip Log files command now includes one week of logs.
  </li><li>Fixed issue - Unable to deploy app to device directly using ad-hoc distribution profile.
  </li><li>Fixed an issue where the iOS Designer would restart frequently.
  </li><li>Fixed a crash editing constraints the iOS Designer property panel.
  </li><li>UISegmentedControls can now be added to UIToolbars.
  </li><li>An issue in the Outline panel which could crash Visual Studio was fixed.
  
  
</li><li>The default memory settings for the android designer rendering process have been updated.
  Addresses <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26026">Bug 26026</a>.</li><li>Added a way to adjust the memory settings for the android designer rendering process. Please refer to the
  <a href="/guides/android/troubleshooting/questions/android-designer-java-memory/">FAQ article</a> for more information.</li></ul>

<h4>v.3.9.302</h4>
<ul>
  <li>All ViewControllers should appear on the design surface now.
  </li><li>Custom Controls in Library projects will render and appear in the toolbox when using a Xamarin.iOS.dll based projects. Support for custom controls in the main project will be added in an upcoming release.
</li></ul>

<h3>VS 2015 Support</h3>
<ul>
<li>Support for Visual Studio Android emulator in Xamarin Android
projects.</li>
</ul>
<h3>Unified Devices</h3>
<ul>
<li>Xamarin VS now shows the devices list in the "Start" button inner
drop-down.</li>
<li>It shows devices that matches the device family defined in the
plist.</li>
<li>Select iPhoneSimulator platform by default when a new iOS project
is unfolded.</li>
</ul>
<h3>Other new features:</h3>
<ul>
<li>Xamarin.iOS projects now have support for XCode assets catalogs
from Visual Studio.</li>
<li>Added F# support: Templates for Xamarin.iOS (Unified API)and
Templates for Xamarin.Android </li>
<li>Option for migrating Xamarin.iOS projects Classic to Unified API</li>
</ul>
<h3>Bug Fixes</h3>
<h4>v.3.9.45-preview</h4>
<ul>
<li>Fixes bug causing a build error with message
"MergeApkRecipelists"
task was not given a value for the
required parameter "RecipeFiles" trying to build Android Projects.</li>
<li>Makes MSI installer to select all the detected compatible Visual
Studio versions by default, to avoid the need of manually picking VS
versions or changing features after install.</li>
</ul>
<h4>v.3.9.65-preview</h4>
<ul>
<li>Includes latest Xamarin.Forms 1.3 templates.</li>
<li>Fixes an issue causing Xamarin.iOS to not detect the right
Screen.Size in some devices.</li>
</ul>
<h4>v.3.9.141</h4>
<ul>
<li>Fixed Bug 23969 - Getting error on running iOS Unified API
application on device.</li>
<li>Bug 19312 - Supported architecture drop down menu greyed out when
iOS target version &gt;= 5.0, can't select ARMv7+ARMv7s </li>
<li>Fixed Bug 24150 - Opening the iOS Build properties changes the
MtouchArch on unmodified template projects</li>
<li>Fixed Bug [XAP] Already running player shows up twice in device
list</li>
<li>Fixed Bug 22494 - Application Loader fails with ERROR ITMS-9000:
Invalid Bundle Structure</li>
<li>Fixed Bug 22010 - Getting build error when I set android project
as a start up project in Xamarin.Forms</li>
<li>Fixed Bug - Getting error with 'Bundle Assemblies into native
code' option enable. </li>
<li> Fixed Bug 17062 - No provisioning profiles have been detected. </li>
<li> Fixed Bug [XAP] VS does not recognize when a player is stopped
or crashes </li>
<li> Fixed Bug At iOS Build&gt; Advanced section, in default view no
supported architectures displayed.</li>
<li> Fixed Bug 21300 - Updater details links open multiple tabs in
browser </li>
<li> Fixed Bug Debugging session ended on iOS device. </li>
<li> Fixed Bug 23076 - Exceptions thrown from async methods on device
cause "Debug information is not available for this frame"
.</li>
</ul>
<h4>iOS Designer Improvements</h4>
<ul>
<li>Full support for Xamarin.iOS Unified projects. </li>
<li>SCNView, UIScreenEdgePanGestureRecognizer, UIVisualEffectView,
UISplitViewController are all fully supported now. </li>
<li>Significantly improved support for UICollectionView and
UICollectionViewLayout. </li>
<li>Added support for aspect ratio based constraints. </li>
<li>UITabBarController will no longer randomly disappear when
creating new Tab segues. </li>
<li>Removed the ability to delete the NavigationBar from a
UINavigationController. iOS will crash at runtime if you try this. </li>
<li>Constraints can now be exposed as an Outlet or custom class. </li>
<li>Fixed an issue changing the style of a UITableViewCell when
constraints are disabled. </li>
<li>Fixed several issues where the property panel would write
incorrect Xml to the storyboard. </li>
<li>Custom fonts are fully supported by the design surface and font
picker. </li>
<li>Fixed a case where old assemblies were sometimes used to render
custom controls. </li>
<li>Embed segues can now be created from Container Views. </li>
<li>Fixed an rare issue where views with zero width or zero height
could break the designer. </li>
<li>Fixed a crash when deleting the segments inside a Segmented
Control. </li>
<li>Custom properties of type 'float' and 'double' should work now. </li>
<li>Elements inside a UIScrollView will no longer change their
position every time we render the storyboard. </li>
<li>Added support for UITextAlignment.Justified and
UITextAlignment.Natural </li>
<li>Fixed an exception when right clicking on a Size constraint </li>
<li>The localization ID for UIView/UIViewController is displayed in
the property panel now. </li>
<li>Improved support for UIViewController.PreferredStatusBarStyle. </li>
</ul>
<h3>Known Issues</h3>
<ul>
<li>When building a new Xamarin.iOS Unified Project, an error is
presented stating that the
code signing keys are invalid/don't match for the simulator if no valid
Signing Key is present. The workaround is to manually remove the "
&lt;CodesignEntitlements&gt;Entitlements.plist&lt;/CodesignEntitlements&gt;"
line on the "Debug|iPhoneSimulator" configuration included in the
.csproj file.</li>
<li>To Start debugging a Xamarin.iOS application in 'Release' Mode,
the "Enable Debugging" checkbox included in the "iOS Build" panel
of&nbsp; project properties should be checked. If not, you will get a
warning about it. <br>
</li>
<li> MtouchExtraArgs variables no longer expand, causing "Input
string was not in a correct format" error. Users who need the
"--gcc_flags" additional mtouch argument to link
native libraries into projects in Visual Studio will encounter a bug,
users who need the
"--xml" additional mtouch argument to specify a custom XML linker file.
There is a partial workaround replace the `${ProjectDir}` entries in
the MtouchExtraArgs with absolute paths, but the easiest option for now
is probably to downgrade [1] back to Xamarin 3.8.150 until a
fix for Xamarin 3.9 is available later this month.</li>
<li> Newly created Xamarin.Forms template projects fail to deploy
to iOS unless you first change the active build configuration
This is a side effect of the new "Unified Devices" feature in Xamarin
for
Visual Studio 3.9. The problem is that if you create a new
Xamarin.Forms
project using the built-in portable template under "Templates -&gt;
Visual C# -&gt;
Mobile Apps -&gt; Blank App (Xamarin.Forms Portable)", you will need to
adjust the
settings under the "Build -&gt; Configuration Manager" menu before
attempting to
run on an iOS device or simulator. Otherwise Visual Studio will hit a
build
error. </li>
<li> Deployment of App to iOS Device with incorrect Provisioning
Profile
When attempting to deploy to an iOS device with an incorrect configured
Provisioning
Profile, the user will see the error message in the output with:
"Failed to deploy application on the target device. Please try to
rebuild the solution and try again."
Visual Studio will hang and become unresponsive. The recommendation is
to ensure that
the provisioning profile is correctly configured with the specific iOS
device and to ensure that the physical device can have applications
deployed from XCODE </li>
</ul>
<h4>DWP handshake assertion</h4>
<p>Please make sure that the following project property is NOT checked:
Project -&gt; Properties -&gt; Android Options -&gt; "Use Fast
Deployment (debug mode only)"
</p>
<h4>Update to latest NuGet Package Manager (2.8.3+) is required<br>
</h4>
<p>Updating to the latest version of&nbsp; Microsoft NuGet Package
Manager, which is compatible with Xamarin.iOS Unified API, is required.
It can be updated from the Visual Studio Extension Manager.<br>
More information is available in the following Visual Studio Gallery's
links:</p>
<ul>
<li>VS 2013:<a href="https://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca">
https://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca</a></li>
<li>VS 2010, VS 2012: <a href="https://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c">https://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c</a></li>
</ul>
</body>
</html>
