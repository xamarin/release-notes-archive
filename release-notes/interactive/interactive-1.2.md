---
id: C33B2620-E528-48F5-B5B1-828781CCE0F7
title: "Workbooks & Inspector 1.2"
---

* [Download for Mac](https://dl.xamarin.com/interactive/XamarinInteractive-1.2.2.pkg)
* [Download for Windows](https://dl.xamarin.com/interactive/XamarinInteractive-1.2.2.msi)

Xamarin Workbooks & Inspector provide interactive tools for learning,
experimenting, and even modifying your running app.

* [Learn More about Xamarin Workbooks & Inspector](/releases/interactive/interactive-1.0.0)
* [Discuss Xamarin Workbooks & Inspector][forums]
* [File a bug][bugs]

Refer to full product documentation for more details:

* [Workbooks][docs-workbooks]
* [Inspector][docs-inspector]

This is a significant update to the [1.1](/releases/interactive/interactive-1.1.2)
release with some new features and bug fixes. An overview of changes since the
1.1 release is below.

## FIXED IN 1.2.2

* Markdown text on Windows now properly reacts to font size preference
  changes.

* Launching the Inspector will no longer bring up multiple instances
  per target application.

* The visual tree will now refresh on Windows as it does on Mac when
  switching between different Workbook target platforms.

* Fixed a regression where the property editor on Windows could only
  update a value once.

* Typing into the REPL in Inspector mode was broken after using
  the `clear` command.

* `Capture(UIView)` for iOS now renders the view's subviews, matching
  the behavior of other target platforms.

* The Mac package now comes with a command line tool to completely
  uninstall Workbooks & Inspector, located at
  `/Library/Frameworks/Xamarin.Interactive.framework/Versions/Current/uninstall`

* When reading release notes in the Mac updater, links will now
  open in the default browser as one would expect.

## FIXED IN 1.2.1

* When adding the Newtonsoft.Json NuGet to a workbook, the version will
  be fixed to 9.0.1 to work around a compatibility issue with 10.0 or
  newer. Full compatibility with 10.0 and newer will come in a subsequent
  major update to Workbooks. [More details][njs-workaround].

* Setting `System.Threading.CurrentThread.CurrentCulture` or
  `System.Globalization.CultureInfo.CurrentCulture` will again persist across
  cells. [More details][culture].

* Code tooltip text now renders properly on macOS 10.12 and later.

## NEW FOR 1.2

* Workbooks and Inspector are now powered by Roslyn 2.0 with support for C# 7,
  including built-in support for tuples via `System.ValueTuple`. Be sure to
  try the ["What's new in C# 7"][csharp7] workbook!

* Inspector now supports complex spatial view transforms, including rotation
  and scaling in 3D, when supported by the underlying platform. The
  3D representation has also been extended to visualize these transforms.

* Support for sublayers on iOS and macOS. Inspector now descends deeper into
  layer hierarchy and allows you to visualize sublayers in the 3D
  representation.

* Xamarin.Forms integration for Workbooks is much improved. The integration
  will now initialize Xamarin.Forms for you, set up a base `Application.Current`,
  and set a blank `ContentPage` as its main page. Xamarin.Forms workbooks are
  now cross-platform, as we've trimmed the set of generated references
  and you no longer need platform-specific initialization code.

* A new `Image` function is available that can accept a URL or a path relative
  to the Workbook's current directory to display the contents of the image
  as the result of the cell.

* Code cells now show cell-relative line numbers to be of assistance when
  reading error and warning diagnostics. This feature is enabled by default
  and can be disabled in the Preferences dialog.

* All cell executions are now timed using a `Stopwatch` and displayed nicely
  at the top right of the cell editor in either seconds, milliseconds, or
  microseconds. This feature is disabled by default and can be enabled in
  the Preferences dialog.

* Console output is now pushed asynchronously and can render _during_ cell
  execution. Previously all captured console output was batched and rendered
  only when execution completed. This is particularly useful for long-running
  `async` cells.

* In the Inspector, REPL history saving can be turned off in the Preferences
  dialog. History can also now be cleared. Saving is now supported on Windows.

* Android workbooks now require an Android virtual device targeting at least
  Android 5.0. Previously, Android 4.4 devices were supported.

## IMPROVED

* NuGet packages are now supported for Android Workbooks and iOS Workbooks
  on Windows.

* C# `dynamic` is now supported without having to explicitly reference
  `Microsoft.CSharp`.

* Code cells that `await` a non-generic `Task` will no longer show `null`
  as a result.

* The Windows installer now bundles its own iOS support for Workbooks.
  It is no longer necessary to have a matching version of Workbooks installed
  on the Mac build host for supporting iOS Workbooks from Windows. Live
  iOS app inspection from Visual Studio still requires a matching install
  on the Mac build host, though.

* Result object introspection is now deferred until the "Object Members"
  result renderer is selected. This speeds up sending the default
  representation of a result for very large objects.

* Xamarin.Forms integration for iOS inspection and Workbooks is now
  available on Windows clients.

* The modal stack in Xamarin.Forms is now properly represented in the
  view inspector, in addition to the navigation stack.

* Package manager list items can now be activated via double-click.

* ARM-based Android emulators will no longer be tried for Android workbooks.
  This will greatly improve Android emulator startup time if many ARM emulators
  were installed.

* You can now set how frequently Workbooks and Inspector will check for updates.
  Additionally, on Windows, you can now specify your preferred update channel
  in the Preferences dialog; on Mac however, this setting is still driven by
  the IDE.

## FIXED

* Any non-Workbooks YAML metadata in workbook manifests will now be
  semantically preserved when saving.

* Framework assemblies can now be referenced from Android workbooks.

* NuGet packages now restore properly when changing agents while a workbook is
  open.

* Getting the visual tree could sometimes cause the app to crash on Android when
  inspecting a Xamarin.Forms app.

* Fixed a reconnect issue for iOS Workbooks on Windows.

* Workbooks' working directories should now stay in sync even when multiple
  workbooks of the same type are open.

## KNOWN ISSUES

* NuGet Limitations
  - Native libraries are supported only on iOS, and only when linked with
    the managed library.
  - Packages which depend on `.targets` files or PowerShell scripts will likely
    fail to work as expected.
  - To remove or modify a package dependency, edit the workbook's manifest with
    a text editor. Proper package management is on the way.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector
[forums]: https://forums.xamarin.com/categories/inspector
[sdk]: https://developer.xamarin.com/guides/cross-platform/workbooks/sdk/
[docs-workbooks]: https://developer.xamarin.com/guides/cross-platform/workbooks/
[docs-inspector]: https://developer.xamarin.com/guides/cross-platform/inspector/
[csharp7]: https://developer.xamarin.com/workbooks/#csharp-csharp-7
[njs-workaround]: https://developer.xamarin.com/guides/cross-platform/workbooks/troubleshooting/general/#Unable_to_use_Newtonsoft.Json
[culture]: https://developer.xamarin.com/guides/cross-platform/workbooks/troubleshooting/general/#Persistence_of_CultureInfo_across_cells

