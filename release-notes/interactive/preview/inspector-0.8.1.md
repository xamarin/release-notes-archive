---
id: 6B77C2F5-6EAB-4EA9-8089-CF15EAE05B83
title: "Workbooks & Inspector Preview 0.8.1"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInteractive-0.8.1.0.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInteractive-0.8.1.0.msi)

This is a bug fix release that addresses issues found in 0.8.0, and adds a few
new features as well.

Notably, NuGet support is much improved, the `#load` directive is now supported,
and we also now support the version of Xamarin shipping in the alpha channel.

Feedback in [the forums][forums] has been invaluable, and please keep filing
[bugs][bugs] too!

## NEW

* `#load` support to execute `.csx` script files.
* When re-executing a workbook from the top, the UI in the agent app is reset.
* Framework dependency resolution for PCL NuGets now works properly.
* Fewer `#r` statements are generated for most NuGet references now.
* Alpha channel Xamarin is now supported.

## FIXED

* NuGet package dependencies will now be installed as expected.
* Loading assemblies relative to the workbook file with `#r` is fixed.
* Workbook load errors display immediately now.
* Run button and workbook title are no longer duplicated in workbook windows on
  Mac.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector
[forums]: https://forums.xamarin.com/categories/inspector

## KNOWN ISSUES

* NuGet Limitations
  - Android Workbooks are not yet supported.
  - iOS Workbooks on Windows are not yet supported.
  - Native libraries are not yet supported.
  - Packages which depend on `.target` files or PowerShell scripts will likely
    fail to work as expected.
  - To remove or modify a package dependency, edit the workbook's manifest with
    a text editor. Proper package management is on the way.
* The CommonMark Markdown editor has various selection bugs on Windows.

