---
id: A5C57258-09B4-4C8C-9683-72EB30EB880F
title: "Workbooks & Inspector 1.4"
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

* [Download for Windows](https://github.com/Microsoft/workbooks/releases/download/v1.4.3/XamarinInteractive-1.4.3.msi)
* [Download for Mac](https://github.com/Microsoft/workbooks/releases/download/v1.4.3/XamarinInteractive-1.4.3.pkg)

Xamarin Workbooks & Inspector provide interactive tools for learning,
experimenting, and even modifying your running app.

This is a significant update to the [1.3 series][13-series], with a number of
new features and bug fixes.

## Now Open Source!

Xamarin Workbooks has now been released as open source software
under the MIT license. Ongoing development will happen in the open on
GitHub. We invite interested users and developers to get involved with the
project. [Join us on GitHub!](https://github.com/Microsoft/workbooks)

## 1.4 Series Releases

* [1.4.3](#1.4.3_July_9_2018) _(July 9, 2018)_
* [1.4.2](#1.4.2_July_5_2018) _(July 5, 2018)_
* [1.4.1](#1.4.1_June_14_2018) _(June 14, 2018)_
* [1.4.0](#1.4.0_January_19_2018) _(January 19, 2018)_

## New & Improved

* Support for iOS 11 and Xcode 9.

* Camera controls on the 3D view inspector have been enhanced and now share
  functionality across macOS and Windows with support for Pan, Zoom and Rotate.

* The visual tree inspector is now more consistent between Windows and macOS
  and has improved view selection and navigation features.

* The property panel in the view inspector is now based on
  [Xamarin.PropertyEditing][proppy], which provides a number of improvements:
  - Properties can now be edited on macOS.
  - Performance improvements thanks to loading properties asynchronously.
  - Editing support for enum, size, and rectangle properties.

* Line-wrapping may be turned off for code cells via the preferences dialog.

* It is now possible for integrations to asynchronously post results to
  code cells. This is the groundwork for supporting `IObservable` and allows
  for [deeper integration with cell compilations][cell-compilations].

* It is now possible to use ASP.NET Core in your .NET Core workbooks.

* Signature help now behaves more like Visual Studio.

* Choose the new _Report an Issue_ menu item in the _Help_ menu to easily
  report issues, and _Reveal Log File_ to quickly find the latest log.

* Xamarin.Forms support has been bumped to 3.0.0.482510.

* The New Workbook dialog now defaults to the last selected type.

## Notable Bug Fixes

### 1.4.3 _(July 9, 2018)_

* Fix crash at startup on Windows with .NET Framework 4.7.1
  ([#488](https://github.com/Microsoft/workbooks/issues/488)).

* Fix an issue when rendering some exceptions with frames that contain multiple
  members in a type with the same name
  ([#405](https://github.com/Microsoft/workbooks/issues/405)).

* Fix an error loading Xamarin.Forms workbooks on iOS
  ([#486](https://github.com/Microsoft/workbooks/issues/486)).

* Fix a label clipping issue in the preferences dialog on macOS
  ([#191](https://github.com/Microsoft/workbooks/issues/191)).

### 1.4.2 _(July 5, 2018)_

* Fix setting `selectedView` in Inspector on Mac
  ([#456](https://github.com/Microsoft/workbooks/issues/456)).

* Fix possible crash when copying system info to clipboard on Windows.

### 1.4.1 _(June 14, 2018)_

* Add initial support for [ML.NET][ml-net] ([#303](https://github.com/Microsoft/workbooks/issues/303)).
  - See our new [sample workbooks][ml-net-workbooks].
  - Not yet supported on .NET Core on Mac.
  - Console support on Mac requires a Mono release with [this fix](https://github.com/mono/mono/issues/9033).

* Add 64-bit .NET Core support on Windows.

* Bump Xamarin.Forms support to 3.0.0.482510.

* Fix potential unresponsiveness when loading an iOS workbook.

* Change Xcode location behavior to match Visual Studio for Mac. ([#249](https://github.com/Microsoft/workbooks/issues/249))

* Fix expanding exception information in submission results.

### 1.4.0 _(January 19, 2018)_

* Additional accessibility fixes for High Contrast mode users on Windows,
  particularly for buttons and menus in the High Contrast White theme.

* The plain text formatter for strings now preserves whitespace in formatted
  output.

* Fix generic type name rendering.

* Fix rendering of emoji in C# string literals.

* Workbooks are now marked as dirty when cells are deleted, preventing possible
  stale workbook files on disk.

* Fixed a few minor issues with NuGet package restoration.

* Fixed a rendering issue in the Mac sidebar. Thank you to Yusuke Yamada
  (@yamachu) for our
  [first ever public contribution](https://github.com/Microsoft/workbooks/pull/97)!

* Fix user interface rendering issues after unlocking your computer on Windows.

* Fixed an SDK location bug that prevented Android workbooks from running.

* Add `workbook` tool to `PATH` using `/etc/paths.d` instead of writing a
  script to `/usr/local/bin`.

* Fix custom attributes using types defined in the workbook, enabling
  custom JSON deserialization.

## Other Notable Changes

[See the full documentation for details](/guides/cross-platform/workbooks/install/#Log_Files)
on the following changes:

* On macOS, `/Applications/Xamarin Workbooks.app` now has a bundle identifier
  of `com.xamarin.Workbooks` instead of `com.xamarin.Inspector`.

* The log file directory has changed to facilitate more fully splitting
  Inspector and Workbooks into separate distributables.

## Known Issues

* NuGet Limitations
  - Native libraries are supported only on iOS, and only when linked with
    the managed library.
  - Packages which depend on `.targets` files or PowerShell scripts will likely
    fail to work as expected.
  - To modify a package dependency, edit the workbook's manifest with
    a text editor. A more complete package management UI is on the way.

[ml-net]: https://github.com/dotnet/machinelearning/
[ml-net-workbooks]: https://github.com/xamarin/Workbooks/tree/master/machine-learning
[13-series]: /releases/interactive/interactive-1.3
[github]: https://github.com/Microsoft/workbooks
[proppy]: https://github.com/xamarin/Xamarin.PropertyEditing
[cell-compilations]: https://github.com/Microsoft/workbooks/blob/master/Samples/CompilationIntegration/AgentIntegration.cs <script async="" defer="" src="https://buttons.github.io/buttons.js"></script>
