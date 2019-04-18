---
id: B110EC29-BEA5-490B-9D1E-84B9F8860D38
title: "Workbooks & Inspector Preview 0.8.0"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector-0.8.0.0.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector-0.8.0.0.msi)

This is a feature release that offers iOS Workbook support on Windows that
utilizes the new remoted iOS Simulator.

NuGet and PCL support is vastly improved as well on both Mac and for the
first time on Windows. A few other features and fixes are included as well.
Many thanks for your feedback in [bugzilla][bugs] and [our forums][forums]!

## NEW

* iOS Workbooks are now supported on Windows.
* NuGet is now supported on Windows and is vastly improved on Mac.
* iOS, Mac, and WPF Workbooks have their current working directory set to
the directory of the `.workbook` file. As such those Workbooks can load
files relative to the `.workbook` file.

## FIXED

* iOS and Mac Workbooks now use the Apple TLS provider by
default for TLS 1.2 support.
* iOS and Mac Workbooks set the App Transport Security key
`NSAllowsArbitraryLoads` to `true` by default.

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

