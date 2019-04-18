---
id: F4AEE9FD-C57C-457E-9F21-C8353D6E76C5
title: "Workbooks & Inspector Preview 0.6.2"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector.msi)

This is a bugfix and feature update of
[the last Xamarin Inspector preview](http://developer.xamarin.com/releases/inspector/preview/inspector-0.6.1/).

Check out
[the initial release notes](http://developer.xamarin.com/releases/inspector/preview/inspector-0.3.1/#What_does_it_do)
or
[our documentation](https://developer.xamarin.com/guides/cross-platform/inspector/)
for more details on the Inspector.

Also be sure to ask questions on the [Inspector forum](http://forums.xamarin.com/categories/inspector)
and [file any bugs][bugs] you may encounter.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector


# Changes Since 0.6.1

* Workbooks

  - Notebooks are now called workbooks. The file extension has changed from
    `.ximd` to `.workbook`, and the file format manifest has changed to be more
    future-proof. `.ximd` files are no longer supported.

  - Many fixes have been made to the care and handling of workbook documents.
    New/Open/Save behavior should be much more predictable now. For example,
    double-clicking a workbook file in Finder or Explorer will now open the
    workbook in Xamarin Inspector.


* Alpha Channel Support

  - Support for inspecting apps from the IDE now requires Xamarin to be
    installed from the alpha channel.

  - However, Xamarin Inspector no longer requires any IDE to be installed
    since Workbook support does not require it.


* CommonMark Markdown Editor improvements

  - An updated editor now features a formatting toolbar while editing.
  [ ![](Images/inspector-0.6.2-editing.gif)](Images/inspector-0.6.2-editing.gif)

* Fixed selection bug in visual tree (#[39232][39232])


# Known Issues

* The CommonMark Markdown editor has various selection bugs on Windows.
* Inspecting 64-bit WPF apps is not supported (#[37134][37134])

[37134]: https://bugzilla.xamarin.com/show_bug.cgi?id=37134
[39232]: https://bugzilla.xamarin.com/show_bug.cgi?id=39232

