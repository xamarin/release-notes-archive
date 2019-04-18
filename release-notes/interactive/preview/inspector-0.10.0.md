---
id: 0C8C786B-D8D8-465F-8DDF-1D211BD7E6EB
title: "Workbooks & Inspector Preview 0.10.0"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInteractive-0.10.0.0.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInteractive-0.10.0.0.msi)

This release complements iOS 10 support now available via the Xamarin beta and
alpha release channels.

Live app inspection in this release now requires the latest Xamarin beta
or alpha channel releases. Xamarin Workbooks continue to work with Xamarin
stable releases.

For iOS 10 workbooks, Xamarin Studio must be configured to use Xcode 8 Beta 5 or
newer.

Feedback in [the forums][forums] has been invaluable, and please keep filing
[bugs][bugs] too!

## NEW

* Support for latest iOS 10 and macOS 10.12 APIs in your workbooks.
  - For iOS 10 workbooks, make sure you are using Xcode 8 Beta 5 or newer.
* Android live app inspection from Visual Studio now requires Xamarin 4.2.
* Android workbooks now have better compatibility with the latest VS Android
  Emulator releases.
* Workbooks & Inspector for Mac now require at least OS X 10.11 El Capitan.

## IMPROVED

* Updated [keybindings][keybindings] in Markdown blocks.

[keybindings]: https://developer.xamarin.com/guides/cross-platform/workbooks/keybindings/

## FIXED

* [#43152][bxc43152]: do not try to connect to physical Android devices.
* Fixed bug on Windows preventing Android workbooks from using Android APIs.

[bxc43152]: https://bugzilla.xamarin.com/show_bug.cgi?id=43152
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

