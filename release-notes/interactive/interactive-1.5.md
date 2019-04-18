---
id: 9ACA1EE6-D6F8-490C-B6B8-58FC7A9126D4
title: "Workbooks & Inspector 1.5"
article:
  - title: Workbooks Documentation
    url: /guides/cross-platform/workbooks/
  - title: Inspector Documentation
    url: /guides/cross-platform/inspector/
  - title: Discuss in Forums
    url: https://forums.xamarin.com/categories/inspector
  - title: File a Workbooks Bug
    url: /guides/cross-platform/workbooks/install/#Reporting_Bugs
  - title: File an Inspector Bug
    url: /guides/cross-platform/inspector/install/#Reporting_Bugs
---

* [Download for Windows](https://github.com/Microsoft/workbooks/releases/download/v1.5.0/XamarinInteractive-1.5.0.msi)
* [Download for Mac](https://github.com/Microsoft/workbooks/releases/download/v1.5.0/XamarinInteractive-1.5.0.pkg)

Xamarin Workbooks & Inspector provide interactive tools for learning,
experimenting, and even modifying your running app.

This is a minor update to the [1.4 series][14-series], adding support for the
latest SDKs.

## New & Improved

* Add support for iOS 12, Xcode 10, and macOS 10.13 SDKs.

* Prefer iPhone X to iPhone 5s for running iOS workbooks.

* Bump .NET Core support to the 2.2 preview SDK.

* Add support for C# 7.3.

* Bump NuGet to 4.8.0 for increased package support.

## Notable Bug Fixes

* Support launching emulators with latest Android SDK.

## Known Issues

* NuGet Limitations
  - Native libraries are supported only on iOS, and only when linked with
    the managed library.
  - Packages which depend on `.targets` files or PowerShell scripts will likely
    fail to work as expected.
  - To modify a package dependency, edit the workbook's manifest with
    a text editor. A more complete package management UI is on the way.

[14-series]: /releases/interactive/interactive-1.4
