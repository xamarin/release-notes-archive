---
id: 9B7DE83F-EB7B-4074-83B3-C8E69E454FB2
title: "Xamarin Studio 5.1"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.1"></head><body>
  
  

<h2><a name="4" id="4">Xamarin Studio 5.1.4</a></h2>

<p>
Xamarin Studio 5.1.4 is a hotfix release based off of Xamarin Studio 5.1.3.
</p>

<h3>Fixes</h3>
<ul>
    <li>Fixed: Xamarin Studio is randomly wiping out the .csproj and leaving an empty project file (Android).</li>
</ul>

<h2><a name="3" id="3">Xamarin Studio 5.1.3</a></h2>

<p>
Xamarin Studio 5.1.3 is a hotfix release based off of Xamarin Studio 5.1.2.
</p>

<h3>Fixes</h3>
<ul>
    <li>The iOS Designer was misgenerating partial methods associated with Actions. The bug caused them to semi-randomly appear/disappear from the .designer file.</li>
</ul>

<h2><a name="2" id="2">Xamarin Studio 5.1.2</a></h2>

<p>
Xamarin Studio 5.1.2 is a hotfix release based off of Xamarin Studio 5.1.0. It does not contain the fixes in the Xamarin Studio 5.1.1 Alpha.
</p>

<h3>Fixes</h3>
<ul>
    <li>Fixes a regression introduced by Android SDK Tools r23 and Android Build-tools r20 that changed the path of the zipalign tool.</li>
</ul>

<h2><a name="1" id="1">Xamarin Studio 5.1.1</a></h2>
<ul>
    <li>Preview of Xcode 6 iOS designer support. Using Xcode 6 also requires Xamarin.iOS 7.9.1.</li>
</ul>

<h3>Fixes</h3>
<ul>
   <li>Fixed rendering on Yosemite.</li>
   <li>Fixed opening of projects on Yosemite.</li>
   <li>Fixed scrolling in the Edit Reference window on Yosemite.</li>
   <li>Fixed misplaced context menus on Yosemite.</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.1</a></h2>

<h3>Android</h3>

<p>The target selector in the main toolbar now allows selecting the emulator or device to be used for running the application. The old Project / Android Device Target menu is gone and devices are shown in the main toolbar:</p>

<img src="target-selector.png">

<p>To be able to disambiguate between emulators that are running and non-running, they are grouped in the target dropdown. Physical devices are grouped together with running emulators. If an emulator doesn't support the SDK level that the project requires, it will still be shown in the list, but it will be disabled.</p>
<p>Besides the devices and emulators, the target selector also has an option for starting the device manager.</p>

<p>When the user executes or starts debugging, the selected device or emulator will be used as the target. In the event of there being no emulators defined or devices connected then the user will be
prompted to create an emulator and start it up. If the selected target is an emulator that is not currently running then that emulator will be started and the execution will block until the emulator has started up.</p>

<p>If the user stops execution while the emulator is starting up then the IDE stops waiting for the emulator but the emulator will continue to start up.
If the emulator is already running then the emulator window will be brought to the front</p>

<p>The Uninstalling Package command will now uninstall from the selected device if it is running or connected - it doesn’t start up the emulator in order to uninstall it.</p>

<p>The Manage Devices dialog also have some small changes. If there are no suitable devices connected or emulators to execute the target, the devices dialog will be shown in “selector mode”.
All emulators and devices will be shown, but devices that do not meet the minimum android version required will be labeled as such.</p>

<h3>Debugger</h3>
<ul>
        <li>Big performance improvements. Some debugger operations are now as much as 4x faster.
        </li><li>Added support for support for DebuggerNonUserCodeAttribute (if the developer has enabled “Debug project code only” in their debugger settings), DebuggerHiddenAttribute, and DebuggerStepThroughAttribute. The debugger will no longer stop in code with any of the aforementioned attributes.
        </li><li>Added support for the DebuggerStepperBoundaryMethodAttribute which causes the debugger to resume execution when code with this attribute is encountered.
        </li><li>Added a “Set Next Statement” command in the editor’s context menu which sets the next statement to be executed when the program resumes execution, allowing developers to re-run previous statements or jump over statements in the current method.
        </li><li>Added a “Show Next Statement” command in the editor’s context menu which will jump to the next statement that will execute when the program resumes (useful if you’ve scrolled in the file and/or switched to another file tab).
        </li><li>Added a “Run To Cursor” command to the editor’s context menu which will resume (or build &amp; start) execution of the program, stopping when it reaches the cursor (it will stop sooner if a breakpoint is reached before it reaches the cursor).
        </li><li>Added support for client-side evaluation of simple properties (e.g. properties that essentially just manually implemented auto-properties).
        </li><li>Fixed usage of DebuggerTypeProxyAttributes.
        </li><li>You can now invoke generic methods in the Immediate Pad (and Watch Pad) w/o needing to explicitly provide generic type args assuming that the generic type arguments can be deduced based on the parameter types. In other words, if you have a method such as `int MethodName<t> (T item)`, entering the expression `MethodName (5)` will now resolve this to `int MethodName<int> (int item)` and will successfully invoke the method.
</int></t></li></ul>

<h3>Xamarin Designer for iOS</h3>

<ul>
  <li>Fixed several issues where storyboards could not be loaded.</li>
  <li>The 'custom controls have been disabled' warning message was incorrectly being activated after building/rebuilding a solution under certain circumstances. This has now been fixed and so should appear less frequently.</li>
  <li>Improve UISlider, UIStepper and UIPageController min/max/current properties behavior.</li>
  <li>Improve display of floating point values in property entries.</li>
  <li>Fixed cases where UIViews were incorrectly marked as under-constrained.</li>
  <li>Improved handling of Headers and Footers inside UITableView.</li>
  <li>Fixed an issue with the UITableViewController.Refreshing property.</li>
  <li>Improved error handling when an incompatible type is used as the 'customClass' for a UIView or UIViewController.</li>
  <li>Honour the setting to hide UINavigationBars and UIToolBars in all cases.</li>
  <li>Several issues with UIBarButtonItem have been fixed. We now allow seguing from these and exposing them as outlets.</li>
  <li>Improved handling of UIToolBars on UINavigationControllers.</li>
  <li>Fixed an issue where the badge in UITabBarItem was not always removed when the badge text was removed.</li>
  <li>Fix hint text being sometimes incorrectly committed as a value on Windows</li>
  <li>Fix text entries clipped incorrectly with long values on Mac.</li>
  <li>Adjust property panel animations to be smoother and less intrusive.</li>
  <li>Visual refresh of several icons.</li>
</ul>

<h4>Changes to Actions and Outlets</h4>
<p>User defined outlets (outlets which do not have the [GeneratedCode] attribute) inside the .designer.cs file will be retained as-is on a best-effort basis. Previously the iOS Designer would attempt to regenerate some of these which could result in the signatures of Actions changing.</p>

<p>The iOS Designer typically generates Actions of the form</p>
<pre><code class=" syntax brush-C#">[Action ("onClicked:")]
[GeneratedCode ("iOSDesigner", "1.0")]
partial void OnClicked (UIButton button) { }</code></pre>
<p>There are times when you may want to use the same method for multiple different NSObject subclasses. If you wish to do this, you can move the declaration of this action to your main code file (not the designer one) and then modify the signature to read</p>
<pre><code class=" syntax brush-C#">[Action ("onClicked:")]
[GeneratedCode ("iOSDesigner", "1.0")]
partial void OnClicked (NSObject button) { }</code></pre>
<p>The designer will understand this and will not auto-generate a 'UIButton' overload.</p>

<p>The designer also supports generating actions with no parameter. If your storyboard file contains an action which has a selector name with no trailing ':', then the Designer will create an action of the form</p>
<pre><code class=" syntax brush-C#">[Action ("onClicked")]
[GeneratedCode ("iOSDesigner", "1.0")]
partial void OnClicked () { }</code></pre>

<h3>NuGet</h3>

<h4>Added support for searching and installing a specific version of a NuGet package</h4>

<p>The Add Packages dialog and Xamarin Studio’s unified search can now be used to search for all versions, a range of versions, or a specific version of a NuGet package. The search syntax is:</p>

<blockquote>PackageId version:VersionNumber</blockquote>

<p>Examples:</p>

<blockquote>
AutoMapper version:2.1<br>
AutoMapper version:2.1.0<br>
AutoMapper version:*
</blockquote>

<h4>Added support for solution specific NuGet.config files</h4>

<p>NuGet will <a href="http://docs.nuget.org/docs/reference/nuget-config-file">chain together multiple configuration files</a> allowing a solution to define its own configuration by including a NuGet.Config file.
The main use of this is to define package sources that are available when a particular solution is opened in Xamarin Studio.</p>

<h4>Other Fixes</h4>
<ul>
<li>Fixed proxy credentials not requested for https package source
</li><li>Fixed Web.config transforms not being applied when installing NuGet packages (e.g. Nancy.Hosting.Aspnet)
</li><li>Fixed XDT remove transforms (Xml Document Transformations) on Mono (used in  Microsoft.AspNet.Mvc NuGet package).
</li></ul>

<h3>Version Control</h3>
<ul>
<li>Improved speed for loading projects that are under Git and status operations.
</li><li>Decreased memory usage for Git.
</li><li>Fixed several issues in the Push Changes… dialog.
</li><li>Fixed Revert To Revision command. This new unwinds the selected files to the selected commit.
</li><li>Fixed Subversion issues with files being locked.
</li><li>Windows Subversion client is now loaded on demand.
</li><li>Fixed issues with Ignored items in Version Control showing up as Unversioned.
</li><li>Fixed issues with multiple updates in Review Changes and Commit view.
</li></ul>

<h3>Shell Improvements</h3>
<ul>
<li>Native file dialogs are now used for file system interactions on Windows.
</li><li>Several icon updates
</li><li>Find in Files now shows the project to which a file belongs in the results pad.
</li><li>Improved general look of Xamarin Studio for Windows in HDPI displays.
</li></ul>

<h3>Other Improvements and Bug Fixes</h3>
<ul>
<li>Fixed issue that caused context menus to not behave properly on Mac (test instructions).
</li><li>Fixed: Out-of-solution exceptions are not visualized.
</li><li>Fix issue when saving file links in shared projects
</li><li>Fixed Move To Class and Create Class/Interface commands when used in shared projects.
</li><li>Fixed issue that caused files to be incorrectly added to projects referencing a shared project.
</li><li>Allow standard .net build actions in shared projects.
</li><li>Fixed rendering of the region section in text editor breadcrumb
</li></ul>

</body></html>
