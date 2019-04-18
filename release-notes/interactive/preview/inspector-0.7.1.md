---
id: F4AEE9FD-C57C-457E-9F21-C8353D6E76C5
title: "Workbooks & Inspector Preview 0.7.1"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector-0.7.1.0.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector-0.7.1.0.msi)

This release builds upon the work of the 0.7.0 release, bringing new
features and fixes to Xamarin Workbooks. Many thanks for your feedback
in [bugzilla][bugs] and [our forums][forums]!

## NEW

* It is now possible to insert new code submissions in workbooks,
  or delete existing ones.
* New "Run All" option to (re)execute an entire workbook.
* New "ToString" renderer option.
* Automatic update notification on Windows.

## IMPROVED

* Object Members will expand automatically when selected from the representation
  menu, but remain collapsed if they're the default representation.
* `GetVars ()` now expands by default.

## FIXED

* Fixed rendering regressions with enumerables and Object Members.
* Fixed bug allowing executed submissions to be edited during live app inspection.
* Fixed error loading workbook files (#[40047][40047]).
* Fixed REPL input with alternate keyboard layouts (#[40046][40046], #[38911][38911]).
* Fixed `clear` command.

[40046]: https://bugzilla.xamarin.com/show_bug.cgi?id=40046
[38911]: https://bugzilla.xamarin.com/show_bug.cgi?id=38911
[40047]: https://bugzilla.xamarin.com/show_bug.cgi?id=40047

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector
[forums]: https://forums.xamarin.com/categories/inspector

## KNOWN ISSUES

* Inspecting 64-bit WPF apps is not supported (#[37134][37134])
* The CommonMark Markdown editor has various selection bugs on Windows.

[37134]: https://bugzilla.xamarin.com/show_bug.cgi?id=37134

