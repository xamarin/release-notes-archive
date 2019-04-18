---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 3.11"
---

<html>
<head>
<meta content="text/html; charset=ISO-8859-1" http-equiv="content-type">
<title></title>
</head>
<body>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">



<h2><a name="0" id="0">Xamarin 3.11</a></h2>
<p>
<a name="0" id="0">Xamarin 3.11 includes support for the 
</a><a href="/releases/ios/xamarin.ios_8/xamarin.ios_8.10/">Xamarin.iOS
8.10</a> and
<a href="/releases/android/xamarin.android_5/xamarin.android_5.1/">Xamarin.Android
5.1</a> releases.
</p>
<p>
<b>Xamarin.Android 5.1 introduces several <a href="/releases/android/xamarin.android_5/xamarin.android_5.1/#Breaking_Changes">breaking changes</a>.</b> Please read through the entire <a href="/releases/android/xamarin.android_5/xamarin.android_5.1/">release notes</a>. 
</p>
<h3>v3.11.1594</h3>
<ul>
<li>Fixes issue causing Watch IPA files to be rejected on submission due to missing WatchKit Support folder. </li>
</ul>
<h3>v3.11.1589</h3>
<ul>
<li>Adds critical support for iOS 9.1.</li>
<li>Fixed Bug 35234 - Timing-dependent error when building iOS Binding projects: "The "BTouch" task failed unexpectedly ... Access to the path '... obj\Debug\ios\ObjCRuntime' is denied" </li>
</ul>
<h3>v3.11.1585 (Beta)</h3>
<ul>
<li>Adds critical support for iOS 9.1.</li>
</ul>
<h3>v3.11.1537</h3>
<ul>
<li>Add support for Android Marshmallow.</li>
</ul>
<h3>v3.11.1450 (Beta)</h3>
<ul>
<li>Fixes Bug 34144 - All resources included from iOS library project except for the modified file are replaced with 0-byte files when redeploying without cleaning after modifying one of the resources. </li>
<li>Fixes Bug 34163 - XIB files and BundleResources within iOS Class Libraries where project name contains "." period characters cause build error</li>
<li>Fixes Bug 34202 - Getting build error when we add iOS library project in iOS single view template application. </li>
</ul>
<h3>v3.11.1443</h3>
<ul>
<li> Adds critical support for Xcode7 and iOS9 GM. </li>
<li>Fixes issue causing build errors with strings resources in iOS class libraries project </li>
<li>Fixes wrong platform set on iOS Class Library projects.</li>
</ul>
<h3>v3.11.1439</h3>
<ul>
<li> Beta Refresh with critical support for Xcode7 and iOS9 GM. </li>
<li>Fixes issue causing WatchKit app getting crashed as soon as it launch on Watch App Simulator. </li>
<li> <strong>Known Issue: </strong>Getting build errors with strings resources in iOS class libraries project
</li></ul>
<h3>v.3.11.1433</h3>
<p>Beta build to add critical support for Apple's iOS 9 GM and Xcode 7.</p>
<h3>v.3.11.894
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=33554">Bug 33554</a> - Monodroid error XA0000: Reason: An element with the same key already exists in the dictionary. </li>
<h3>v.3.11.893</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32909">Bug 32909</a> and <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32912">Bug 32912</a>  - VS 2015 issues with XAML intellisense. </li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32622">Bug 32622</a> - Creating VS2013 project and opening in 2015 causes error CS0012 (Assembly reference issues, including bcl). </li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32767">Bug 32767</a> - Watch App Info.plist UIDeviceFamily array is incorrect. </li>
</ul>

<h3>v.3.11.837</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=33174">Bug 33174</a> - SDK Tools v24.3.4 Breaks the Android Designer. </li>
</ul>
<h3>v.3.11.836</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32514">Bug 32514</a> - User is unable to add a component in Visual Studio. </li>
</ul>
<h3>v.3.11.816</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=31893">Bug 31893</a> - VS gets hang when user Deploy Watchkit application on Simulator. </li>
</ul>
<h3>v.3.11.785</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=31009">Bug 31009</a> - AOT of Cirrious.MvvmCross.Binding.dll with verbose logging causes System.ArgumentOutOfRangeException".</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26079">Bug 26079</a> - Setting $(AndroidUseLatestPlatformSdk)=True should NOT clear $(TargetFrameworkVersion).</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29398">Bug 29398</a> - "Xamarin.VisualStudio.iOS.Documents" process holds open a reference to the project folder after Visual Studio has exited.</li>
<li>Fixes Automated Feedback pop-up appearing on unrelated projects.</li>
<li>Improved Xamarin.iOS API Doc Sync experience.</li>
</ul>
<h3>v.3.11.666</h3>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=28728">Bug 28728</a> - Unable to find AndroidManifest.xml when click on 'Run in Test Cloud' option for Xamarin.Forms Android.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26841">Bug 26841</a> - Cannot build: The last access/last write time on file "bin\Debug\Sensus.Android.dll.mdb" cannot be set.</li>
</ul>
<h3>v.3.11.658</h3>
<ul>
<li>Fixes an issue with Xamarin.Android projects debugging not hitting breakpoints unless Shared Runtime is used and Linker is disabled.</li>
<li>Fixes an issue causing facade assemblies to be copied to the Mac while building Xamarin.iOS projects.</li>
<li>Removes unsupported UI Test project template for VS 2010.</li>
<li>Fixes an issue with Xamarin.Forms Android apps not hitting breakpoints in PCL projects.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=30100">Bug 30100</a> - Cannot set Xamarin Profiler location path because menu option is disabled.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29849">Bug 29849</a> - Forms iOS Project Template adds Entitlements.plist to iPhoneSimulator configurations.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=30371">Bug 30371</a> - Project Properties display incorrect default values for "BundleAssemblies" and "EmbedAssembliesIntoApk" if they are not explicitly specified.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29654">Bug 29654</a> - "Project properties -> iOS Bundle Signing" shows "This page is valid only for hardware platforms" when targeting Simulator.</li>
<li>Xamarin VS now uses Rx .NET 4.5 assemblies for VS 2012 and newer versions.</li>
</ul>
<h3>v.3.11.590 (Stable)</h3>
<ul>
<p>3.11.590 is a hotfix release meant to improve compatibility with the latest Android SDK Build-tools 23.0.0_rc1 and the Android-M preview. Additional information can be found in the <a href="/releases/android/xamarin.android_5/xamarin.android_5.1/">Xamarin.Android 5.1.3</a> release notes.</p>
</ul>
<h3>v.3.11.586</h3>
<ul>
<p>Fixed a <strong>Xamarin.iOS </strong>issue causing <strong>Visual Studio</strong> to not remove the .MDB files for Portable Class Library projects referenced from a <strong>Xamarin.iOS</strong> application executing a <strong>"Clean"</strong> command.</p>
</ul>
<h3>v.3.11.576 </h3>
<ul>
<p>Fixed a Xamarin.iOS debugging issue, allowing VS to nicely disconnect after a failing debugger session start. The fixed previous behavior was intermittently not being able to hit breakpoints on physical iOS devices, and VS hangs trying to stop the debugging session.</p>
</ul>
<h3>v.3.11.570</h3>
</h3><h4>Bug Fixes</h4>
<ul>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29628">Bug 29628</a> - MDB files are not generated for PCLs and breakpoints in PCLs don't work.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29703">Bug 29703</a> - "Show IPA File In Build Server" fails if "Build" number is different from "Version" number.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29839">Bug 29839</a> - [3.11] Native Linking Error when trying to link a static library in iOS.</li>
<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=29220">Bug 29220</a> - Test Cloud throws error in output window of Visual Studio</li>
<li>Fixes "Not implemented (Exception from HRESULT: 0x80004001 (E_NOTIMPL))" error when user unloads and reloads project in some scenarios.</li>
<li>Fixes some issues found during IPA creation causing submission errors.</li>
</ul>
<h4>Known Issues</h4>
<p>There is now an explicit <strong>IpaIncludeArtwork</strong> checkbox on the <strong>IPA Options</strong> section of the project properties. It's required for AppStore configurations to uncheck that option before building the IPA file for submission.</p>
<h3>v.3.11.458</h3>
<ul>
<p>Xamarin for Visual Studio version 3.11.456 is a <strong>Hotfix</strong> released to address some issues creating proper IPA files suitable for uploading to the AppStore.</p>
<p>As introduced on Xamarin VS 3.11.570, in this hotfix there is now an explicit <strong>IpaIncludeArtwork</strong> checkbox on the <strong>IPA Options</strong> section of the project properties. It's required for AppStore configurations to uncheck that option before building the IPA file for submission.</p>
</ul>
<h3>v.3.11.446</h3>
<ul>
	<li>3.11.446 is a hotfix release to fix operations on 'System.Decimal' in Xamarin.Android. Additional information can be found in the <a href="/releases/android/xamarin.android_5/xamarin.android_5.1/">Xamarin.Android 5.1.1</a> release notes.</li>
</ul>
<h3>v.3.11.445</h3>
<h4>General</h4>
<ul>
	<li>New Project Templates for Mobile cross-platform Native apps were added. You can find them as "Visual C# - Blank App (Native Portable)" and "Visual C# - Blank App (Native Shared)" if supported.</li>
	<li>Adds support for Xamarin.iOS Binding Projects from Visual Studio for Unified API projects.</li>
	<li>Integrates a Xamarin Test Cloud cross-platform project template.</li>
	<li>You can now submit apps directly to Test Cloud from the IDE. See our guide <a href="/guides/testcloud/uitest/working-with/submitting-tests-to-xamarin-test-cloud/">here</a>. Make sure to select the Visual Studio version of the document.</li>
	<li>Xamarin Starter Edition now enables development using Visual Studio.</li>
	<li>Includes Xamarin.Forms intellisense for XAML files.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=27805">Bug 27805</a> - Certain storyboards lead to "The connection was closed unexpectedly" build server disconnect during IBToolTask.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=27672">Bug 27672</a> - For a F# iOS Template application, when right click and click on properties, VS crashes.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26308">Bug 26308</a> - "Linker behavior" project option displays incorrect value compared to the "MtouchLink" property.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26484">Bug 26484</a> - Only the first SayHelloTask run by a command-line MSBuild process successfully negotiates a connection with the build server.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=23106">Bug 23106</a> - Error MT0024: Could not find required file.</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26079">Bug 26079</a> - Setting $(AndroidUseLatestPlatformSdk)=True should NOT clear $(TargetFrameworkVersion).</li>
	<li>Fixes <a href="https://bugzilla.xamarin.com/show_bug.cgi?id=25551">Bug 25551</a> - Error: Failed to load output manifest for ibtool.</li>
</ul>

<h3>iOS Designer</h3>
<ul>
  <li>Fixed an exception triggered by interacting with the 'Priority' editor for constraints</li>
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
