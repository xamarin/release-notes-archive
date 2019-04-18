---
id: 6572C83D-5481-4CD4-9C33-B96251B0D099
title: "Workbooks & Inspector Preview 0.9.0"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInteractive-0.9.0.14.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInteractive-0.9.0.14.msi)

This update brings minor changes to the `.workbook` file format, improves
the Workbook editing experience on Windows, and addresses various issues
from 0.8.1.

It also brings a more clear split between the Workbooks client and the
Inspector client, including some new branding.

Feedback in [the forums][forums] has been invaluable, and please keep filing
[bugs][bugs] too!

## NEW

* Code cells now feature a run button below the cell editor.
* The `.workbook` file format has changed slightly. The metadata at the top of
  each file is now familiar [YAML Front Matter][yamlfm] instead of obnoxious
  JSON. The old format is still supported and will migrate to the new one on
  save.
* Workbooks and Inspector clients are now separate apps with distinct
  branding.
* Workbooks markdown can now reference images and other files relative to the
  .workbook file.
* iOS workbooks and app inspection now expose the `RootViewController`
  convenience API.
* Android workbooks on Windows will now do a better job of creating firewall
  exceptions needed in order to connect to the app in the emulator.
* http://xmn.io/workbooks-help provides guidance for some common problems.

[yamlfm]: https://jekyllrb.com/docs/frontmatter/

## IMPROVED

* The Windows client now looks _amazing_ on HiDPI screens.
* Improved execution keyboard shortcuts
  - <kbd>Cmd/Ctrl+Return</kbd> executes the current code cell.
  - <kbd>Shift+Return</kbd> always inserts a new line.
  - <kbd>Cmd/Ctrl+R</kbd> executes the entire workbook from top
    to bottom ("Run All").
  - More details are available [in our documentation][keybindings].
* Markdown editing on Windows is _much_ improved.
* Windows clients now remember preferred font size.

[keybindings]: https://developer.xamarin.com/guides/cross-platform/workbooks/keybindings/

## FIXED

* [#41707][bxc41707]: inline images in markdown now load on Mac over HTTP
* Fixed error in VS extension when opening a solution with unsupported project
  types.
* <kbd>Ctrl+Up</kbd> and <kbd>Ctrl+Down</kbd> in a code cell now move to the
  beginning or end of the cell, respectively, on Windows.

[bxc41707]: https://bugzilla.xamarin.com/show_bug.cgi?id=41707
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

