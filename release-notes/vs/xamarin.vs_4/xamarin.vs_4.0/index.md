---
id: 12E30FDC-58DC-4D63-95DF-3D483F063F50
title: "Xamarin 4.0"
---

##  <a name="0" id="0">Xamarin 4.0</a>


Xamarin 4.0 updates [Xamarin.iOS 9.4](/releases/ios/xamarin.ios_9/xamarin.ios_9.4/) and [Xamarin.Android 6.0](/releases/android/xamarin.android_6/xamarin.android_6.0/) releases. This version also introduces the new **Xamarin Mac Agent** which replaces the old **Xamarin Build Host **with a new approach taking advantage of the built-in MacOS Remote Login feature based on SSH for a faster and more reliable connectivity.

### Xcode 7.2 support

XamarinVS 4.0 now includes support for Xcode 7.2.

### Xamarin Mac Agent

Our new design focuses on avoiding the pain points of the original Xamarin.iOS build host that we are no longer shipping.

#### Key Benefits

##### Simplicity and Security

-  We have done away with the PIN-based Mac pairing process. The new Xamarin Mac Agent only requires that Remote Login (aka SSH) is enabled on the Mac.
-  The new Connection Manager in Visual Studio will discover, authenticate, and remember your Mac. Moreover, since all communication is tunneled securely through SSH, you only have to open one, well-known port (i.e., port 22) on your router or firewall.
-  There’s no longer an app to start on the Mac. If you have a compatible version of Xamarin.iOS installed, VS will automatically deploy and start the new agent.


##### Improved Reliability

-  There were several cases where VS would hang when connecting the debugger via the original build host. The new Mac agent substantially improves the connection reliability, so these problems should be gone.
-  If the agent crashes or disconnects for any reason, VS will automatically attempt to restart the agent and re-establish connectivity without requiring user intervention or interrupting the Visual Studio experience.


##### Simultaneous Sessions

-  With the original Xamarin.iOS build host, only a single Visual Studio instance could be connected to the Mac. This made it frustratingly difficult to keep multiple iOS solutions open at once. The new Mac agent allows multiple instances of VS to connect to the agent simultaneously.


##### Offline Support

-  We’ve made it easier to work without a connection to your Mac. VS will no longer prompt you to connect to your Mac unless you are performing some operation for which the Mac is required, such as debugging or using the designer.


#### Limitations

The new Mac Agent requires an active session on the Mac for the user configured on Visual Studio while connecting to the Mac.

### iOS Designer

#### Full Xib and Xib Splash Screen support

We're pretty excited to finally ship full support for Xib files in this release. You can edit and interact with xib files just like you already could with storyboard files. This includes full support for designing xib splash screens.

#### Faster hi-dpi design surface

Just like the Android Designer, the design surface has been rewritten to take advantage of high performance, hardware accelerated APIs. When a hi-dpi display is attached, the design surface will switch to hi-dpi mode and will render higher quality images. The new surface should use less memory, feature much smoother scaling/zooming and also be significantly faster when panning around a large storyboard. If you are using a touchpad you can zoom and pan using the standard gestures. If you are still on a lo-dpi display you should still notice an improvement in the quality of the images on the design surface.

#### Faster initialization

We've worked hard on tweakinge every aspect of the initialization process so that the time between double clicking a storyboard and seeing it display on-screen is as short as possible. Both the first launch time and subsequent re-launch times should be noticably shorter, especially with large storyboards. We have also fixed many cases which would cause initialization to time out and display an error.

Other changes

-  Faster refreshing when an item is modified on the design surface.
-  Fixed several cases where the design surface would not react when the mouse button was released.
-  Fixed several cases where simulated metrics were not being set correctly.
-  Significantly improved support for property variations in the property panel.
-  All accessibility properties are supported.
-  Improved support for Unwind and Embed segues.
-  Retina image resources should be handled correctly now.
-  Fixed many cases where the property panel would not write the correct value to the storyboard/xib file.
-  Fixed several places where the wrong default value was showing up in the property panel.
-  Improved support for changing between Plain text and Attributed text for properties supporting both.
-  Resize handles will only appear when they can modify the size of the View they're attached to.
-  Custom properties of type nint and nfloat are now supported by the property panel.
-  All performance issues associated with the Outline panel have been fully resolved.
-  Constraints are now grouped in the Outline panel.
-  The property panel in Visual Studio is now beautifully baseline aligned.
-  Fixed several issues with copy/paste which could corrupt the storyboard.
-  Improved support for fixing the frame for underconstrained items.
-  AwakeFromNib should be reliably invoked for custom controls in the design surface.
-  Improved misplacement handling for under-constrained/over-constrained items and when changing size classes.
-  The designer should never overwrite existing files when generating new classes.
-  Full support for WatchOS2 rendering as of the latest Xcode 7 beta release.
-  Dozens more under the hood changes to fix crashes, exceptions and quirks


### Android Designer

#### Faster hi-dpi design surface

Just like the iOS designer, the design surface has been rewritten to take advantage of high performance, hardware accelerated APIs. When a hi-dpi display is attached, the design surface will switch to hi-dpi mode and will render higher quality images. The new surface should use less memory and feature much smoother scaling/zooming. If you are using a touchpad you can zoom and pan using the standard gestures. If you are still on a lo-dpi display you should still notice an improvement in the quality of the images on the design surface.

### Bug fixes and Changes

This release includes the following bug fixes and changes:

#### XVS 4.0.4.4

-  Added support for latest MS Android Emulator.
-  Fixed "Tools - Xamarin Account" asks for login, instead of showing VS license.
-  Fixed xUnit Test Runner hangs when a breakpoint is set in a test.
-  Clicking on "Xamarin for Visual Studio Update Available" notification toolbar icon has no effect.
-  "System.NullReferenceException: Object reference not set to an instance of an object" at AD7Events.cs line 433 thrown by the IDE extension when processing AD7DebugExceptionEvent debugger events from the Android application.


#### XVS 4.0.3.214

-  A Xamarin Account is no longer required to use Xamarin on Visual Studio 2013, Visual Studio 2015 or newer.
-  Added Visual Studio Dev15 support.
-  No more remote Mac activation from Visual Studio (Not required anymore).
-  Removed Designer landing pages when Xamarin cannot be used on VS 2012.
-  Removed Welcome to Xamarin page creating new solutions.
-  Removed license Upgrade Workflows.
-  Removed Xamarin.iOS Crash Reporting property page
-  Removed Xamarin analytics consent (now it's part of the VS analytics consent).
-  Android AOT assemblies and Enable LLVM checkboxes are hidden if license level doesn't support them.
-  Visual Studio 2012 support is only available for Xamarin Business and Xamarin Enterprise accounts.
-  Visual Studio 2012 will close Solutions containing a Xamarin project if there is no Xamarin Business or Enterprise account.


#### XVS 4.0.1.147

-  Bug 39655 - iOS 6 and iOS 7 devices are not displayed in the devices drop-down menu, device logs show repeating error "set_response_error: handle_get_value GetProhibited".


#### XVS 4.0.1.145

-  Bug 38585 - Enterprise "In House" provisioning profiles do not appear in the drop-down menu in the iOS project settings editor
-  Bug 36059 - "The application UnifiedSingleViewIphone1 needs to be rebuilt due to an inconsistency between the connected Mac and the local app. Please rebuild the application and try again." when attempting to deploy to device or simulator.
-  Bug 37674 - "Could not authenticate the user using the existing ssh keys" warning message could be more descriptive for the particular case where the user home folder on the Mac has incorrect permissions.
-  Bug 37600 - "The application UnifiedSingleViewIphone1 needs to be rebuilt due to an inconsistency between the connected Mac and the local app" due to warning "Could not authenticate the user using the existing ssh keys" during build.


#### XVS 4.0.1.96

-  Bug 38433 - The Info.plist editor does not display any tabs if it is opened with a window width below a certain minimum
-  Bug 38401 - "The "PackLibraryResources" task failed unexpectedly." when an iOS library project contains any bundle resources in the root folder other than images


#### XVS 4.0.1.93

-  Bug 38240 - Breakpoints in library projects fail to pause the debugger if the Visual Studio UI is set to a language other than English


#### XVS 4.0.1.87

-  Bug 37224 - [VS only] User is unable to check/uncheck the checkbox "Use LLVM Optimizing Compiler"


#### XVS 4.0.1.81 (Beta, Alpha)

-  Bug 37502 - Xamarin.Forms cross-template project creates wrong PCL project type.
-  Bug 37429 - No "Source" tab shown in .axml editor when a .axml file is opened in Android Designer.


#### XVS 4.0.1.74 (Alpha)

-  Bug 37319 - Android devices / emulators not getting updated in dropdown list if wrongly configured virtual device is found. 
-  Bug 37141 - User is not able to launch watch app in notification mode.
-  Bug 36403 - The default value of "iOS IPA Options -> Include Artwork in IPA" needs to be updated.
-  Bug 36797 - Unsolvable warning in the "Xamarin" section of the "Output" window: "There is a mismatch between the installed Xamarin.iOS ... and the local Xamarin.iOS"
-  Bug 36430 - Unable to upload iPA to app store having iCloud enable.


#### XVS 4.0.1.60 (Alpha)



Adds the following bug fixes to our Xamarin 4 Service Release Preview: <pi>
<ul>
	<li>Bug 36633 - 167 x 167 App icons are not appearing for ipad pro. </li>
	<li>Bug 35858 - VS2015 does not show contents of local variables during debug (RC3)</li>
	<li>Bug 36667 - Getting build error while building Watch Kit application</li>
	<li>Bugs 35615, 36117 - Can't see most distribution identities or provisioning profiles</li>
	<li>Bug 37115 - "The "SayGoodbye" task failed unexpectedly" when attempting to build any iOS bindings project</li>
	<li>Bug 36645 - Somewhat misleading "Failed to execute 'ls /usr/bin/mono'" warning message in Ide log with OS X 10.11 El Capitan build hosts</li>
</ul>
<h4>XVS 4.0.0.1717</h4>
<ul>
	<li>Adds Xcode 7.2 support.</li>
	<li>Includes iPad Pro icon sizes support.</li>
</ul>
<h4>XVS 4.0.1.37 (Alpha)</h4>
<ul>
	<li>Adds Xcode 7.2 support to our Xamarin 4 Service Release Preview.</li>
	<li>Includes iPad Pro simulator support.</li>
</ul>
<h4>XVS 4.0.1.32 (Alpha)</h4>
<ul>
	<li>Previews several improvements to be available in the next Xamarin 4 Service Release.</li>
</ul>
<h4>XVS 4.0.0.1712</h4>
<ul>
	<li>Bug 36185 - Hang/freeze when opening or working on a solution that contains an Android project, during background Xamarin.Android "GetAdditionalResourcesFromAssemblies" Task.</li>
	<li>Bug 36525 - Missing iPad pro simulator in device dropdown for iPad application.</li>
</ul>
<h4>XVS 4.0.0.1697</h4>
<ul>
	<li>Fixes minor installer issue.</li>
	<li>Brings to the stable channel fixes from XVS 4.0.0.1694.</li>
</ul>
<h4>XVS 4.0.0.1694 (Alpha)</h4>
<ul>
	<li>Bug 35859 - Unable to connect to OS X due to invalid generated ClientId (computer username has non-ascii character).</li>
	<li>Bug 35833 - Provide a better error message when the project is on a network share.</li>
	<li>Bug 36190 - [XVS 4.0] Could not write lines to file "obj\Debug\MyLib.csproj.FileListAbsolute.txt". The process cannot access the file 'C:\MyLib\obj\Debug\MyLib.csproj.FileListAbsolute.txt' because it is being used by another process.</li>
	<li>Fixed: The iOS Designer was unable to open iPad xib files. Now these files will be correctly detected as 'xib' files and will render in the surface.</li>
	<li>Fixed: Fixed an issue where some storyboards would not render when iOS9 or newer was selected.</li>
	<li>Fixed: The Z-Order for individual ViewControllers was not being set/maintained correctly. It will be now!</li>
</ul>
<h4>XVS 4.0.0.1689</h4>
<ul>
	<li>Bug 35797 - New project creation hangs indefinitely for templates that reference Xamarin Nugets that aren't already cached.</li>
</ul>
<h4>XVS 4.0.0.1685</h4>
<ul>
	<li>Bug 35077 - Improved iOS build performance.</li>
	<li>Bug 35643 - Does not deploy to Android simulator even when deployment selected.</li>
	<li>Bug 34676 - Breakpoints do not trigger in an async RelayCommand. Issue also present with any PCL referenced at second or higher level.</li>
	<li>Bug 35475 - Fixed OpenGL templates to make the projects build successfully.</li>
	<li>Bug 35633 - Getting rejection after uploading IPA of WK extension project.</li>
	<li>Bug 35642 - When deploying app from VS frequently get old build.</li>
</ul>
<h4>XVS 4.0.0.1649</h4>
<ul>
	<li>Removed Complications from Unsupported Devices on watchOS simulators.</li>
	<li>Bug 34578 - [XMA] Visual Studio crashes if you disconnect Mac VM host from internet, allow VS to re-pair, then re-connect the VM to the internet.</li>
	<li>Bug 34690 - Permissions on the API docs XML files is missing on non-english OS.</li>
	<li>Bug 34178 - Installer fails on Windows PC set to a language other than English.</li>
	<li>Bug 34585 - Checksum verification assumes bash as shell; connection to Mac fails with different shell.</li>
	<li>Bug 33599 - [XMA] After disabling network or unplugging network cable of an unknown agent, it does not get disappear from the Mac agent list.</li>
	<li>Bug 34543 - Right clicking build host in XMA connection dialog does not successfully open context menu.</li>
	<li>Bug 34578 - [XMA] Visual Studio crashes if you disconnect Mac VM host from internet, allow VS to re-pair, then re-connect the VM to the internet.</li>
	<li>DocSync improvements.</li>
	<li>Bug 34706 - Explicitly setting the mac agent by IP gets forgotten when VS restarts.</li>
	<li>Bug 35039 - User is not prompted for 'AppleID Sign in Dialog' on clicking Find button under passes in VS.</li>
	<li>Bug 34397 - Behaviour of Unsupported device list name 'suffix (Complication) and heading Dynamic List root' is not clear.</li>
	<li>Bug 33195 - [XMA] Can't dismiss license window.</li>
	<li>Bug 34925 - [Cycle 6] Visual Studio hangs after activation when the activation workflow is run while opening a solution that contains an iOS app project.</li>
	<li>Bug 34902 - Unable to remote build iOS app from Visual Studio command line  </li>
	<li>Bug 34970 - Error build from msBuild command line: The Mac license edition 'Business' is higher than the Win dows license edition.</li>
	<li>Bug 34737 - "Run in Test Cloud" Results in an Upload Failed Error.</li>
	<li>Bug 31695 - Startup project in Xamarin.Forms solutions is a library.</li>
	<li>Bug 35168 - Assemblies duplicated on remote build into user folder.</li>
	<li>Bug 35125 - References to large pre-built assemblies (over 16 MB) cause creation of "C:" directory in top-level user home directory on Mac build host.</li>
	<li>Bug 35196 - Publish Android Application window is not responding when publishing the android application. </li>
	<li>Bug 35140 - server list showing duplicated machines.</li>
	<li>Bug 35267 - [XVS] iOS Binding Project Fails to build with XCode 7 on Yosemite Access to the path \ios\ObjCRuntime' is denied. The "BTouch" task failed unexpectedly.</li>
	<li>Bug 35347 - Unable to retrieve iOS SDK when Xcode is 7.1</li>
</ul>
<h4>XVS 4.0.0.1566</h4>
<ul>
	<li>Bug 34329 - DocSync is crashing on startup caused by BufferOverflow.</li>
	<li>Bug 34454 - LinkAssemblies task now fails on windows when targeting v4.5 while $(AndroidUseLatestPlatformSdk) is true.</li>
	<li>Bug 34456 - XVS Installer no longer creates MonoAndroid framework symlink from v5.0 -> v4.5.</li>
	<li>Bug 34541 - XMA leaves several TAIL processes running on the Mac which are never killed.</li>
	<li>Bug 34065 - Getting exception on opening interface.storyboard file of WatchKit project in VS with Xcode 7.</li>
	<li>Bug 18251 - TFS can't do a command-line build of iOS projects.</li>
	<li>Bug 19860 - [Intermittent] Unable to create Xamarin iOS/Android application in VS 2013.</li>
	<li>Bug 22080 - Exceptions thrown by mtbserver are incomplete in "Mac Server Log".</li>
	<li>Bug 34393 - Show only paired simulatos when a WK Extension project is the startup one.</li>
	<li>Bug 34144 - All resources included from iOS library project except for the modified file are replaced with 0-byte files when redeploying without cleaning after modifying one of the resources. </li>
	<li>Bug 34163 - XIB files and BundleResources within iOS Class Libraries where project name contains "." period characters cause build error</li>
	<li>Bug 34202 - Getting build error when we add iOS library project in iOS single view template application. </li>
	<li>Removed restriction for adding WCF references using starter license.</li>
	<li>Allow setting the $(AndroidSupportedAbis) MSBuild property in Debug builds as well as Release builds.</li>
	<li>Improved zip logs commands from Visual Studio: "Zip Logs" gets the current session logs from Windows and Mac, and "Zip Logs (last 7 days)" gets the last 7 days logs from Windows and Mac.</li>
</ul>
<h4>XVS 4.0.0.1505</h4>
<ul>
	<li>Bug 32342 - Cant open storyboards in Visual Studio.</li>
	<li>Bug 31965 - System.ArgumentException: An item with the same key has already been added.</li>
	<li>Bug 31600 - [XVS] Unable to hit breakpoint in iOS Forms PCL project consistently</li>
	<li>Bug 31423 - [XVS] Locked .dll files: Could not copy "... PortableClassLibrary1.dll" to "bin\Debug\PortableClassLibrary1.dll". Exceeded retry count of 10. Failed.</li>
	<li>Bug 30563 - VS debugger error when hitting iOS breakpoint.</li>
	<li>Bug 28027 - [XVS.iOS 3.9.483] VS never connects to the soft debugger on physical iOS devices.</li>
	<li>Bug 23035 - No "Text Visualizers" when debugging Android and watching a string variable.</li>
	<li>Bug 22422 - Windows Updater force-restarts VS.</li>
	<li>Bug 21191 - Missing feature: Setting iOS background modes is not possible in VS.</li>
	<li>Bug 21010 - Conditional breakpoint still hit if condition is changed while the app is being debugged.</li>
	<li>Bug 20449 - Clicking "Stop Debugging" does not always attempt to kill the app.</li>
</ul>
<h4>XVS 4.0.0.1111</h4>
<ul>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=20309">Bug 20309</a> - Rendering delay with larger storyboard.</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=33123">Bug 33123</a> - SpriteKit template cannot deploy to simulator – missing info.plist.</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26079">Bug 26079</a> - Setting $(AndroidUseLatestPlatformSdk)=True should NOT clear $(TargetFrameworkVersion).</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=18468">Bug 18468</a> - Frequent 'Debugger Connection Lost'</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=17902">Bug 17902</a> - Not seeing 'PNGCrush' in build output after selecting 'Optimize PNG image files for iOS'</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=18617">Bug 18617</a> - Rebuilding Project with PCL causes Reference Exceptions</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=18656">Bug 18656</a> - Build Host connectivity is a problem.  Sometimes it thinks there is another instance of visual studio connected to it.</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=26429">Bug 26429</a> - Cannot deploy or debug on iOS devices with "+" characters in their names</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=18943">Bug 18943</a> - Missing 58x58 icon in Project Properties</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=15983">Bug 15983</a> - We need a better workflow for the Connect To Build Server dialog</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=17415">Bug 17415</a> - Remove the "Are you sure you want to quit?" dialog for Xamarin.iOS Build Host</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=13389">Bug 13389</a> - [XA VS] "Start without debugging" should be the default deployment method in release configuration</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32392">Bug 32392</a> - Show iOS Simulator is not working</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=15564">Bug 15564</a> - Creating a new iOS project doesn't add simulator configurations</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=30738">Bug 30738</a> - ADB fails to launch and throws VS exception dialogue</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=31203">Bug 31203</a> - Command did not execute successfully due to an unexpected exception."" whening launching ADB via Visual Studio</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=32143">Bug 32143</a> - Can't disconnect if one agent is not able to be started.</li>
	<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=17467">Bug 17467</a> - Error list panel doesn't get cleared between builds</li>
</ul>

<h3>Known Issues</h3>
<ul>
<li>The new Xamarin Mac Agent uses SSH to create a remote session on your Mac. In order to create that connection you should use the SSH username provided by the Mac on the Remote Login configuration Dialog. This username might not match the account full name. For instance, it won't if the full username contains special characters.</li><li>Incompatibility issues with MacOS X <strong>Mavericks</strong>. Xamarin.iOS applications cannot be launched / debugged from Visual Studio using a Mac Agent with Mavericks.</li>
<li>The first attempt to deploy an Android project in VS might fail, subsequent attempts succeed.</li>
<li>Xamarin.iOS apps can be closed while waiting on a breakpoint at launch. The application on device will die if the app does not return from the "FinishedLaunching" method in around 15 seconds. This includes the debugger.</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=12606">Bug 12606</a> - Visual Studio Threads window only work in one debug session. Restarting Visual Studio works around the issue.</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35786">Bug 35786</a> - iOS applications referencing a high number of assemblies (97 ->1000) fails to build from VS since file descriptor limit is hit. VS will get a "Could not strip assembly" error.</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35750">Bug 35750</a> - Installing from within VS2015 can fail as it uses largest hd it can find instead of temp on c:</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35424">Bug 35424</a> - UITest may not detect android package.</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35858">Bug 35858</a> - Visual Studio might not show contents of local variables during debug</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35850">Bug 35850</a> - Compile error: Could not write lines to file "obj\Debug\......csproj.FileListAbsolute.txt".</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35859">Bug 35859</a> - Unable to connect to OS X due to invalid generated ClientId (computer username has non-ascii character).</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=35882">Bug 35882</a> - User is getting an error message while creating Xamarin.forms portable application in VS 2013.</li>
<li><a href="https://bugzilla.xamarin.com/show_bug.cgi?id=37860">Bug 35882</a> - Missing rename options of UI for Asset Catalogs.</li>
</ul>

<h4>Update to latest NuGet Package Manager is required<br>
</h4>
<p>Updating to the latest version of&nbsp; Microsoft NuGet Package
Manager, which is compatible with Xamarin.iOS Unified API, is required.
It can be updated from the Visual Studio Extension Manager.<br>
More information is available in the following Visual Studio Gallery's
links:</p>
<ul>
<li>VS 2015:<a href="https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d">
https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d</a></li>
<li>VS 2013:<a href="https://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca">
https://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca</a></li>
<li>VS 2012: <a href="https://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c">https://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c</a></li>
</ul>


</pi>
