---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.8"
---

<html>
<head>
<meta content="text/html; charset=ISO-8859-1" http-equiv="content-type">
<title></title>
</head>
<body>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">



<h2><a name="0" id="0">Xamarin 3.8</a></h2>
<p>
<a name="0" id="0">Xamarin 3.8 updates
</a><a href="/releases/ios/xamarin.ios_8/xamarin.ios_8.4/#6">Xamarin.iOS
8.4</a> and
<a href="/releases/android/xamarin.android_4/xamarin.android_4.20/">Xamarin.Android
4.20</a> releases,
and support for iOS 8.1 development.
</p>

<h3>New Features</h3>
<ul>
<li>Support for Xamarin.Android 4.20</li>
<li>Integrated support for Xamarin Profiler:</li>
<ul>


</ul><li>Enable an Android Project to be instrumented from Visual Studio
Project Properties - Android Options.<br>
</li><li>Start a profiling session from Visual Studio. It's required to
have the Xamarin Profiler install path configured.<br>
</li>
<li>Do not copy unnecessary files from Visual Studio to the Build
Host during build.</li>
<li>Improved compatibility support for Xamarin.Forms templates:</li>
<ul>





</ul><li>Do not unfold the Windows Phone client app if the WP SDK 8.0 is
not installed (or if using VS 2010, which cannot create WP 8.0
applications) </li><li>In incompatible scenarios, change the target Portable Profile
to "Profile7" instead of "Profile78" to have a working solution. </li><li>Do not install Xamarin.Forms Shared Projects templates into
VS2012 and VS2010 where it's not supported.</li><li>On VS2010, if the Portable Tools are not installed, we're now
informing the user that it needs to be installed in order to create a
Xamarin.Forms project (otherwise PCL projects are not supported). </li><li>On VS2013, only unfold the Xamarin.Forms Shared Project
template if it's supported, otherwise we let the user know the need of
updating Visual Studio.</li>
</ul>
<ul>
</ul>

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
  </li><li>The freeform size metrics editor can now set Width/Height values greater than 1.
  </li><li>Images being rendered on the design surface will no longer vanish if other images are added/removed from the project
  </li><li>Several stability enhancements have been committed to make the designer more robust when Xcode 6 is selected.
</li></ul>

<h3>Bug Fixes</h3>
<ul>
<li>Rename of entitlements Key and Prefix for iCloud Containers on
projects targeting iOS 8 and later.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23743">Bug 23743</a>
- Illegal Character in Path when trying to open iOS Application panel
on iOS project properties.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23731">Bug 23731</a>
- Absent Info.plist causes Visual Studio to crash when switching
between iOS project property tabs.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23733">Bug 23733</a>
- Visual Studio crashes when Entitlements.plist is checked into TFS.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23353">Bug 23353</a>
- "No Devices Attached" shows in Visual Studio's iOS Toolbar when iOS
device is connected to computer.</li>
<li>Fixed "IBToolTask" error on Mac Build Host due to an Ibtool
warning
"The connection to service named com.apple.nsurlstorage-cache was
invalidated."</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=21202">Bug 21202</a>
- Build Host pairing issue in the Mac due to an invalid System_Profiler
addin (most cases reported after updating to Yosemite).</li>
<li>Fixed Bug - Detect and inform if the configured XCode SDK path in
Visual Studio doesn't match the path on the Mac.&nbsp;</li>
<li>Fixed Bug - Visual Studio does not show warning, if Target
Android version is lower than minimum android version.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=21284">Bug 21284</a>
- Make license refresh process delete
licenses in %LOCALAPPDATA%\VirtualStore\ProgramData\Mono*</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23868">Bug 23868</a>
- Incorrect values in UIScreen.MainScreen.Bounds</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23635">Bug 23635</a>
- Unified build folder sandboxing for MacOSX build host files copy.</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=24492">Bug 24492</a>
- Storyboard not rendered in iOS Designer</li>
<li>Fixed <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=19312">Bug 19312</a>
- iOS Project supported architecture dropdown is greyed out.</li>
</ul>

<h3>Known Issues</h3>
<ul>
<li>If your Android project was targeting the Android L Preview,
you'll
need to update your Android XML manifest to change version information
from L to 21. Additionally, you should retarget your project's
framework to use version 5.0 or, alternatively, set it to use the
latest available framework version.</li>
</ul>
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
<p><br>
</p>
</body>
</html>
