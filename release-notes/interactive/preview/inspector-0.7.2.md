---
id: F4AEE9FD-C57C-457E-9F21-C8353D6E76C5
title: "Workbooks & Inspector Preview 0.7.2"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector-0.7.2.0.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector-0.7.2.0.msi)

This is a bugfix release to address app inspection breaking with the latest
Xamarin update in the alpha and beta channels. A few other features and fixes
are included as well. Many thanks for your feedback in [bugzilla][bugs] and
[our forums][forums]!

## NEW

* Inspecting 64-bit WPF apps is now supported (#[37134][37134]).
* You can now open multiple workbooks of the same framework type on Windows.

## FIXED

* Fixed live app inspection, following an underlying API change in Xamarin
  Studio and Xamarin for Visual Studio.
* Fixed opening Android workbooks on Mac.
* Fixed null result for methods called with trailing semicolon (#[40056][40056]).
* iOS and Mac Mobile workbooks should now be able to resolve more framework assemblies via `#r`

[40056]: https://bugzilla.xamarin.com/show_bug.cgi?id=40056
[37134]: https://bugzilla.xamarin.com/show_bug.cgi?id=37134

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector
[forums]: https://forums.xamarin.com/categories/inspector

## KNOWN ISSUES

* The CommonMark Markdown editor has various selection bugs on Windows.

