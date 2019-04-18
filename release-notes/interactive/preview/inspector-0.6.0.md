---
id: F4AEE9FD-C57C-457E-9F21-C8353D6E76C5
title: "Inspector Preview 0.6.0"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector.msi)

This is a major bugfix and feature update of
[the last Xamarin Inspector preview](http://developer.xamarin.com/releases/inspector/preview/inspector-0.5.0/).

Check out
[the initial release notes](http://developer.xamarin.com/releases/inspector/preview/inspector-0.3.1/#What_does_it_do)
or
[our documentation](https://developer.xamarin.com/guides/cross-platform/inspector/)
for more details on the Inspector.

Also be sure to ask questions on the [Inspector forum](http://forums.xamarin.com/categories/inspector)
and [file any bugs][bugs] you may encounter.

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector


# Changes Since 0.5.0

* Xamarin Inspector is now powered by
  [Roslyn](https://github.com/dotnet/roslyn/), Microsoft's open source compiler
  platform.

  - Compilation now happens on the client instead of in your app. This leads to:

    * Instant semantic feedback, code completion, and error reporting.

    * Less complexity in what we inject into your app to support inspection.

    * The same lightning fast execution times as before.

  - Member completion is vastly superior to previous releases. As it is based on
    Roslyn, you can expect similar behavior to Visual Studio 2015. More advanced
    completion features (such as parameter completion) are on the roadmap, too.

* Improved editing:

  - Multiline editing

  - Syntax highlighting

  - Auto-indent

  - Bracket matching

* New "standalone" mode targets: Android and WPF (in addition to iOS and Mac).

  - Open the Xamarin Inspector client app directly to launch an Inspector window
    that connects to an agent app we've bundled (like in Sketches).

  - On Mac, use `File → New` to show standalone choices.

  - On Windows, click the `new standalone` button in the titlebar.

  - Quick access to a C# REPL in any supported environment.


# Known Issues

* Inspecting 64-bit WPF apps is not supported (#[37134][37134])

[37134]: https://bugzilla.xamarin.com/show_bug.cgi?id=37134

