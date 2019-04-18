---
id: 9B7DE83F-EB7B-4074-83B3-C8E69E454FB2
title: "Xamarin Studio 5.2"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.2"></head><body>
  
  

<h2><a name="1" id="1">Xamarin Studio 5.2.1</a></h2>

<p>
Xamarin Studio 5.2.1 is a hotfix release based off of Xamarin Studio 5.2.0.
</p>

<h3>Fixes</h3>

<ul>
   <li>Fixed random hangs of Xamarin Studio.</li>
   <li>Fixed code completion in .xaml files.</li>
</ul>

<h2><a name="0" id="0">Xamarin Studio 5.2</a></h2>
<h3>Side-by-side editing support</h3>
<p>This release add support for placing text editors side-by-side and for detached floating editors.</p>

<p>2-column mode can be enabled by using the "2 columns" command (Command+Option+2 on Mac, Control+Shift+2 on Windows)
or by dragging an editor tab to one of the edges of the editor area.</p>

<img src="moving-side-by-side.png">

<p>Once the IDE is in 2-column mode, you can move editors between columns as you wish.</p>

<img src="side-by-side.png">

<p>Editor tabs can be dragged out of the document area to create floating editor windows. A floating
window can contain several editors.</p>

<img src="floating.png">

<h3>NuGet Support</h3>

<h4>Added framework retargeting support</h4>

<p>When the project’s target framework or PCL Profile is changed
in the Project Options, Xamarin Studio will check whether that new
project target framework / profile requires a different assembly
from the NuGet package to be installed or if the NuGet package is
incompatible with the new project framework. The results of this
compatibility check are displayed in the Package Console and affected
packages are highlighted with warning icon in the Solutions window.</p>

<p>To retarget the NuGet package, right click the package or Packages
folder and select Retarget. This will reinstall the NuGet package so the
correct assembly is referenced by the project.</p>

<h4>Automatic Package Update Check</h4>
<p>Xamarin Studio will check in the background for updated packages
when a solution is opened. This can be disabled in Preferences via
the Check for package updates when opening a solution option.</p>

<p>Updated package information is shown in the Solution window on the
Packages folder and on each Package inside the Packages.</p>

<h4>Support custom package repository path in NuGet.Config</h4>

<p>In the NuGet.config file, the standard directory used to install packages can now be overriden.
This can be useful if you have multiple solutions in different locations which you would like to
share the same packages directory. By default directory is “packages” inside the solution directory.</p>

<pre><code class="syntax brush-XML syntax brush-C#">
&lt;configuration&gt;
    &lt;config&gt;
       &lt;add key="repositoryPath" value="../../MyPackages"&gt;&lt;/add&gt;
   &lt;/config&gt;
&lt;/configuration&gt;
</code>
</pre>

<h4>Other NuGet improvements and fixes</h4>
<ul>
<li>Fixed Visual Studio compatibility for MSBuild imports added to a project with NuGet by adding a
condition to the import that checks the imported file exists. This allows a project created
by Xamarin Studio to be opened in Visual Studio when packages are missing.
</li><li>Fixed repositories.config file not being properly restored.
</li><li>All checked packages in Add Packages dialog are now installed even if they are not currently displayed.
</li><li>Improved status bar message when updating packages. Previously Xamarin Studio would show a message
        indicating that the packages were updated successfully even when no updates occurred.
        Now when no updates are available the status bar message will display
        "Packages are up to date".
</li><li>Fixed incorrect Add Packages button label when a single package checked in Add Packages dialog.
</li><li>Package dependencies are now resolved from all enabled package sources and not just the
        currently selected package source in the Add Packages dialog.
</li><li>Before updating NuGet packages Xamarin Studio will now check to see if any NuGet packages
        are missing for the project and restore them before attempting the update.
        Updating a package when packages are not restored can fail since the older NuGet
        package will need to exist so it can be uninstalled.
        Restoring missing packages before attempting to update the packages fixes this problem.
</li></ul>

<h3>Debugger</h3>
<h4>New unified exception, function and location breakpoints dialog</h4>

<p>All kinds of breakpoints (based on location, function or exception) can now be created
with the single command "New Breakpoint" in the Run menu. Also, all breakpoints can be managed
in the Breakpoints pad.</p>

<p>As a result of this unification, some features which were previously only available for location breakpoints, are now
also available for exception and function breakpoints, such as Hit count conditions, or the option to log a message
when the breakpoint is hit.</p>

<img src="breakpoints.png">

<h4>Other debugger improvements and bug fixes</h4>
<ul>
<li>Fixed a bug in resolving some variables in the debugger tooltips when “Allow implicit property evaluation and method invocation” is disabled.
Fixed a bug caused by the use of UseShellExecute when running an application under a custom SDB debugger command.
Fixed the completion-list logic to hide compiler-generated fields.
Fixed the bug that sometimes caused the exception popup from going away in the editor.
</li><li>Fixed the completion-list logic to hide compiler-generated fields.
</li><li>Fixed the bug that sometimes caused the exception popup from going away in the editor.
</li></ul>

<h3>Xamarin Designer for iOS</h3>
<ul>
  <li>Views can now be rearranged using the new SendBackward, SendToBack, BringForward and BringToFront commands.</li>
  <li>A project load error is no longer triggered if the designer cannot be initialized when opening a solution containing an iOS project.</li>
  <li>Improved the alignment marker logic so that mid/baseline drop areas are preferred over top/bottom/left/right alignment markers</li>
  <li>Improved handling of UIViewController.LoadView/UIViewController.ViewDidLoad when rendering custom controls.</li>
  <li>UIButton frames are now updated as expected when changing the type back to 'System'</li>
  <li>Fixed an issue where some tristate properties would not change out of the 'indeterminate' state.</li>
  <li>Duplicate files are no longer added to the solution if a UIView or UIViewController is made a custom class and a file of that name already exists.</li>
  <li>We now support generating [Action] methods with no sender parameter</li>
  <li>Improved support for Xcode6 and Yosemite. Some crashes caused by Xcode 6 / iOS8 support have been resolved. </li>
  <li>An exception triggered by selecting a constraint which references a Top or Bottom layout guide has been fixed.</li>
  <li>Fixed a case where we could generate invalid storyboard files when working with UITextView.</li>
  <li>Fixed a crash triggered by disabling autolayout under certain circumstances.</li>
  <li>The iOS Designer was misgenerating partial methods associated with Actions. The bug caused them to semi-randomly appear/disappear from the .designer file.</li>
</ul>

<h3>ASP.NET Support</h3>

<ul>
<li>ASP.NET MVC project templates have all been updated to ASP.NET 5.1.2.
</li><li>ASP.NET MVC project templates now use NuGet references.
</li><li>ASP.NET MVC projects are now compatible with VS2013.
</li><li>ASPX CodeBehind is now only updated on saving the ASPX file. It is not longer updated when building the project.
</li><li>HTML5 doctype is now used for new files.
</li></ul>

<h3>Other Improvements and Bug Fixes</h3>
<ul>
        <li>Simplified the options panel for choosing the IDE fonts.
        </li><li>F#: fixed bugs in Android fragment templates, which were producing invalid code.
                Tooltips now display in F# scripts that are not part of the current project
        </li><li>Xamarin.Mac: fixed a bug preventing custom “Document Types” in the Advanced section
        of the Info.plist editor from loading the CFBundleTypeIconFile icons that the
        user had previously specified.
        </li><li>Version control: fixed an interface corruption caused by the Commit Dialog.
        </li><li>Fixed memory leak when reloading solutions
        </li><li>Fixed context menu positioning issue on Macs with retina display (bug 20938)
        </li><li>Fixed exceptions thrown by Windows Native File dialogs when working with encodings.
</li></ul>

</body></html>
