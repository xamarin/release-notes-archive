---
id: 45C5BBA3-5E61-4D13-85ED-8B316B69DF3B
title: "Workbooks & Inspector Preview 0.99.0"
---

* [Download for Mac](https://dl.xamarin.com/interactive/XamarinInteractive-0.99.0.0.pkg)
* [Download for Windows](https://dl.xamarin.com/interactive/XamarinInteractive-0.99.0.0.msi)

This release brings several new features to Xamarin Workbooks & Inspector.
It pairs best with Xamarin Cycle 8 SR1, available in the beta channel
as of this writing. For iOS, you will want to upgrade to Xcode 8.1.

Feedback in [the forums][forums] has been invaluable, and please keep filing
[bugs][bugs] too!

## NEW

* Xamarin.Forms hierarchy support.
* Improved 3D view on Mac, and now available on Windows, too.
* Google's Android emulator is now supported.
* Code editor now based on VS Code.

### Workbooks Updates

* Workbooks can now target multiple platforms, and easily switch between them.
* Workbooks load faster than ever, and can be read and edited while loading.
* If the workbook app crashes, it can be restarted without having to reopen
  the workbook.
* There is a new "Console" platform on both Mac and Windows for basic desktop
  C# usage, without being tied to any particular UI framework.
* WPF and Console workbook apps run in 64-bit mode on 64-bit operating systems.
* Workbooks downloaded from the internet will not execute until the user
  approves them.
* It is no longer necessary to have a firewall exception when using Android
  workbooks on Windows.
* iOS workbooks now have access to more APIs and permissions.

### Live App Inspection Updates

* iOS apps can now be inspected from Visual Studio on Windows.
* The Visual Studio extension now reports any issues connecting the Inspector
  the same way the Xamarin Studio add-in does, via hover tips on the Inspect
  button.
* Core app assemblies are no longer switched around when inspecting iOS apps.

## KNOWN ISSUES

* Xamarin.Forms features are not yet supported for iOS on Windows.
* When using Google's Android emulator, view select mode does not yet work.
* NuGet Limitations
  - Android Workbooks are not yet supported.
  - iOS Workbooks on Windows are not yet supported.
  - Native libraries are not yet supported.
  - Packages which depend on `.target` files or PowerShell scripts will likely
    fail to work as expected.
  - To remove or modify a package dependency, edit the workbook's manifest with
    a text editor. Proper package management is on the way.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector
[forums]: https://forums.xamarin.com/categories/inspector

