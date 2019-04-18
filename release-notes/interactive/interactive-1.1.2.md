---
id: B814B934-CE10-45E5-880D-43D1939EA878
title: "Workbooks & Inspector 1.1"
---

* [Download for Mac](https://dl.xamarin.com/interactive/XamarinInteractive-1.1.2.0.pkg)
* [Download for Windows](https://dl.xamarin.com/interactive/XamarinInteractive-1.1.2.0.msi)

Xamarin Workbooks & Inspector provide interactive tools for learning,
experimenting, and even modifying your running app.

* [Learn More about Xamarin Workbooks & Inspector](/releases/interactive/interactive-1.0.0)
* [Discuss Xamarin Workbooks & Inspector](https://forums.xamarin.com/categories/inspector)

This is a minor update to our [1.0 release](/releases/interactive/interactive-1.0.0)
with some features and bug fixes.

## NEW

* Hovering the mouse cursor over code will show symbol information in a tooltip.

* WPF workbooks now import some default namespaces (`System.Windows`,
  `System.Windows.Controls`, and `System.Windows.Media`).

* On Mac, the new `workbook` command line tool allows for quickly creating and
  opening workbooks from the terminal. The workbook will have its working
  directory set to the working directory of the terminal.

## IMPROVED

* More accurate view representations for Android in the 3D view.

* Hidden Xamarin.Forms views will no longer render in the 3D view.

* Archived workbooks will now re-save as archives instead of as directories.
  There is now also a UI option to choose between saving applicable workbooks
  as either directories or archives.

* Native HTTP/TLS support when using `System.Net.Http.HttpClient` in console
  workbooks running on Mac. Further, an API hook is provided for agent
  integrations to provide their own. See [SDK documentation](/guides/cross-platform/workbooks/sdk/) for details.

* Workbooks & Inspector is now fully updatable via the normal Xamarin update
  channels. We will begin taking advantage of the alpha, beta, and stable
  channels.

* If Internet Explorer 11 is not installed, a better error message will display
  at startup. Some users reported this when running Windows 7 or 8 without
  the IE 11 update.

## FIXED

* Workbooks and Inspector are now compatible with [Xamarin Cycle 9](https://releases.xamarin.com/release-candidate-cycle-9-rc5-refresh/).

* Fixed rendering of arrays of types deriving from UIKit types.

* Object members table width is now appropriately sized on Windows. Previously
  it was clipped for enumerables.

* Android and iOS projects can now be inspected in Visual Studio Enterprise
  without an explicit Xamarin license.

* Faster assembly resolution when typing in a `#r` directive, which was mostly
  noticeable in WPF and Console workbooks on Windows.

* Various rendering issues have been fixed on Mac in the code cell editor
  (Monaco).

* Fixed an issue on Mac where window titles were empty in some cases.

* Fixed the Mac workbook app not rendering properly on retina displays.

* Dismiss suggestion tooltips when a code cell loses focus.

* Native dependencies extracted from iOS NuGet assemblies are now supported.

* Opening invalid URIs via markdown links will no longer crash the Mac client.

* For iOS workbooks on Windows, mismatches between installed versions on Windows
  and the Mac build host will now be detected and recommend updating either
  the Mac or the Windows installation to match.

* Xamarin.Forms applications with a top-level page that is not a container
  will now have their view hierarchy correctly captured.

* Framework assemblies can now be correctly referenced in Workbooks from
  iOS/Windows.

* Fixed issue on Mac where deleting code cells could break Workbook interaction.

* Fixed issue where log spew could sometimes show up in the console output
  area in a code cell.

* Fixed Windows install so that Workbooks can run without Visual Studio present.

* [Fixed a bug](https://bugzilla.xamarin.com/show_bug.cgi?id=52537) that
  resulted in an error dialog on Windows if the Workbook window was resized
  after deleting a code cell.

## KNOWN ISSUES

* Xamarin.Forms features are not yet supported for iOS on Windows.
* The same version of Workbooks must be installed on both the Windows client
  and the Mac build host for iOS on Windows.
* NuGet Limitations
  - Android Workbooks are not yet supported.
  - iOS Workbooks on Windows are not yet supported.
  - Native libraries are supported only on iOS, and only when linked with
    the managed library.
  - Packages which depend on `.targets` files or PowerShell scripts will likely
    fail to work as expected.
  - To remove or modify a package dependency, edit the workbook's manifest with
    a text editor. Proper package management is on the way.

