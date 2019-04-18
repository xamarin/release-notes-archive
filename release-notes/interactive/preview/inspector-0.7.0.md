---
id: F4AEE9FD-C57C-457E-9F21-C8353D6E76C5
title: "Workbooks & Inspector Preview 0.7.0"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector.msi)

This is a bugfix and feature update of
[the last Xamarin Inspector preview](http://developer.xamarin.com/releases/inspector/preview/inspector-0.6.2/).

Check out
[the initial release notes](http://developer.xamarin.com/releases/inspector/preview/inspector-0.3.1/#What_does_it_do)
or
[our documentation](https://developer.xamarin.com/guides/cross-platform/inspector/)
for more details on the Inspector.

Also be sure to ask questions on the [Inspector forum](http://forums.xamarin.com/categories/inspector)
and [file any bugs][bugs] you may encounter.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector


# Changes Since 0.6.2

* REPL Improvements

  - REPL submission results now offer multiple representations, which can be
    selected via a friendly new drop-down menu. A full list of object members is
    now available for all types.

  - `#r` should now work in more scenarios. Absolute paths to arbitrary
    assemblies now work everywhere but Android.

  - Various editor bugfixes, especially regarding focus capturing.


* Workbook Updates

  - All code submissions can now be edited and re-executed as desired.

  - You can now open multiple workbooks of the same framework type
    simultaneously.

  - `#r` will now find assemblies in the same folder as the workbook.


* Inspector Updates

  - When inspecting an object's members, you can now quickly get a reference to
    any member with a single click.

  - Live app inspection is available for enterprise customers.


* Mac Client

  - Very early NuGet package support for workbooks (Mac and iOS only for now).
    Only very simple packages are currently supported. Try `SkiaSharp` on iOS,
    or `Newtonsoft.Json` on Mac/iOS. Package dependencies are recorded in the
    workbook metadata and restored as necessary.

  - Automatic update notification.

  - Just for fun, `MKPolyline` properties in selected objects can now be edited
    graphically directly in the the REPL.


* Windows Client

  - The Visual Studio Android Emulator is now supported for workbooks, and is
    the preferred emulator on Windows (**NOTE:** requires firewall exceptions
    for both public and private networks; you will be prompted on first run of
    an Android workbook).

  - The Live Visual Tree and Property View are now dockable in the session
    window.


# Known Issues

* The CommonMark Markdown editor has various selection bugs on Windows.
* Inspecting 64-bit WPF apps is not supported (#[37134][37134])

[37134]: https://bugzilla.xamarin.com/show_bug.cgi?id=37134

