---
id: E52232FD-FEC9-4724-BF61-434C51ED6836
title: "Xamarin Studio 5.3"
---

<html><head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

  <link rel="legacy" href="http://docs.xamarin.com/mac/releases/xamarin.studio_5/xamarin.studio_5.3"></head><body>
  
  

<h2><a name="0" id="0">Xamarin Studio 5.3</a></h2>

<h3>NuGet Support</h3>
<ul>
        <li>Improved status messages when restoring packages before update
        </li><li>Do not check for updated packages if project has no packages
        </li><li>When opening a solution, missing packages are restored before updating
        </li><li>Add Packages dialog - Package sources could not be reached. Previously when All Sources was selected
        and if any package source could not be reached then no packages would be displayed.
        Now a warning message will be displayed and packages will be displayed even if one package source could not be reached.
        </li><li>Restore packages for selected project instead of the solution. When the Packages folder is selected in the Solution pad
        the Restore menu option now restores just the packages for the selected project.
        </li><li>NuGet package restore no longer uses NuGet.exe. The NuGet package restore is now a part of the NuGet addin.
        This allows the package restore to integrate with the Xamarin Studio credential provider.
        </li><li>Show packages added to solution in Add Packages dialog. Opening the Add Packages dialog will show the packages added to all projects in the current solution.
        </li><li>No updates found but warnings logged status bar message. When one of the package sources is unavailable or invalid then NuGet will report
        a warning when checking for updates and no updates are found.
        </li><li>Show "packages up to date" message in status bar. When the user updates a single package, all packages in the project or all packages
        in the solution, and all packages are already up to date then the status bar now displays a message indicating that the package or packages are up to date.
        </li><li>Fix empty source being selected in Add Packages dialog when package source disabled and All Sources selected.
        </li><li>Restore packages for single project when updating that project
        </li><li>Fix version shown as download count in Add Packages dialog when searching for package versions.
        </li><li>Fixed: Updating packages can mark packages.config as deleted by Git
</li></ul>

<h3>Preview of Android L Support</h3>

<p>This release includes preliminary support for Android L preview and for Android Wear. Xamarin.Android 4.17+ is required for Android L and Android Wear support.</p>
<p>Java 1.7 is now required to be able to use the previews. It’s also required if using some of the new support libraries that were part of the same release.</p>

<h4>Android Designer</h4>
<ul>
        <li>Added API level 20 (Wear) and 21 (L preview) rendering.
        </li><li>Support for Theme.Micro (Wear) and the new Theme.Material for L.
        </li><li>Support Wear Square, Wear Round device and TV device types.
        </li><li>Support for Action Bar menu icons and navigation style via the menu and actionBarNavMode XML attributes. More information on those attributes can be found at <a href="http://tools.android.com/tech-docs/tools-attributes#TOC-tools:menu">http://tools.android.com/tech-docs/tools-attributes#TOC-tools:menu</a>.
</li></ul>

<h4>iOS Designer</h4>
<ul>
        <li>Made Xcode6 support much more robust. The designer should render reliably under all circumstances now. Support has been added for most of the new properties in iOS8.</li>
        <li>Fixed an issue where the automatic reload of the design surface after rebuilding the solution could complain about custom controls causing errors.</li>
        <li>Fixed an issue where UIViewControllers would sometimes render at the wrong size. i.e. one that should render as iPhone 4" might change to iPhone 3.5".</li>  
        <li>Optimised rendering is now working correctly when scenes are set to iPhone 4" size. This should improve drawing performance for large storyboards.</li>
        <li>UITableViewCell.Style now always writes the correct value to the storyboard file.</li>
        <li>The KeyboardType property of UITextField now works correctly.</li>
        <li>Fixed many rendering issues with the Outline panel.</li>
        <li>Added support for NSUnderline in attributed strings.</li>
        <li>If a UIView inside a UICollectionViewCell is made an outlet, that outlet will be correctly generated on the UICollectionViewCell.</li>
        <li>The drag images for items in the toolbox will now match the SDK set for the storyboard. For example if the storyboard is set to view as iOS6.1, the drag images will be themed using iOS 6.1.</li>
        <li>Code generation will only generate C# code when in C# projects now.</li>
        <li>A Deployment Target combobox has been added to the Storyboard properties so you can choose the minimum supported iOS version for each storyboard.</li>
</ul>

<p>Known issues:</p>
<ul>
<li>No support yet for distributing Wear apps via normal phone/tablet apps.
</li><li>Switching between 4.4W and L rendering in the designer may cause an “error 33” because of fonts issues.
</li><li>Wear Round won’t display as a circle in the designer.
</li><li>Overflow menu for Action Bar can’t be triggered yet.
</li></ul>

<h3>Other improvements and bug fixes</h3>
<ul>
        <li>Fixed crash when building a project that makes use of custom tools.
        </li><li>Fixed issue that caused projects unloaded to be removed from solutions.
        </li><li>(Android) Changed the default value of "Preserve data/cache between application deploys" to true.
        </li><li>Fixed crash when selecting “Run with” for an android project when an iOS project is the start up project of the solution.
        </li><li>Fixed an issue where Xamarin Studio would launch a second instance of an Android emulator after changing projects.
        </li><li>Fixed an issue where Xamarin Studio would no longer see a connected Sndroid device after changing projects.
        </li><li>Fixed an issue where Xamarin Studio would not detect that an Android emulator had started up.
        </li><li>Fixed text truncation issue for “Manage Android Devices” command in target selection combo.
        </li><li>New commands “New Function Breakpoint” and “New Exception Catchpoint” which are under Run menu and inside Breakpoints pad.
        </li><li>Fixed Version Control issues with file renaming.
        </li><li>Fixed trimmed text in Version Control Log diff cell.
        </li><li>Fixed issue when parsing conditions in .csproj files.
        </li><li>Fixed an issue where Xamarin Studio would open a solution twice in the solution pad.
        </li><li>Fixed crash when double clicking on an axml file if it was already opened.
        </li><li>Fixed crash or hand when running custom tools on items of a .csproj file.
        </li><li>Fixed: Cannot change the case of folder names in OSX.
</li></ul>
</body></html>
