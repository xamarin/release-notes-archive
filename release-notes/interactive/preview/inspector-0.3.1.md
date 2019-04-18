---
id: EF53AD5F-2611-42D7-814C-F266CE2CEA68
title: "Inspector Preview 0.3.1"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector-0.3.2.1.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector.0.3.2.1.msi)

This is the initial preview release of the Xamarin Inspector. It
consists of a Xamarin Studio add-in, a Visual Studio extension, and rich clients
for Mac and Windows. Xamarin iOS, Android, and Mac apps can be inspected,
as well as WPF.

This is an early preview. Give it a try and let us know what you think, or if
you [run into any bugs][bugs]!

# What does it do?

1. The Xamarin Studio add-in and the Visual Studio extension inject Inspector
   Support assemblies into your app when it launches.
2. A lightweight loop is run in the background of your app, waiting for you to
   press the Inspect button in the IDE.
3. Once the Inspect button is pressed, an Inspector agent starts running inside
   of your app. This agent exposes your visual tree, provides support for
   evaluating C# code, etc.
4. The Inspector client app launches and connects to the agent inside your app.

Please note that for iOS apps, we also have to swap in platform assemblies that
support System.Reflection.Emit (for use by Mono.CSharp, which powers the C#
REPL). This happens even if you don't press the Inspect button.

If you start noticing any odd app behavior, you should disable or uninstall
the Inspector add-in (or extension), restart your IDE, do a clean rebuild, and
try again. If this fixes it, we'd greatly appreciate
[a bug report][bugs].

# Features

* Browse the visual tree
* Inspect and modify properties on visual elements
* Evaluate C# code in your app using the REPL (Read-Eval-Print Loop)
* 3D exploded view of the screen (Mac client only)

Please check out
[our documentation](https://developer.xamarin.com/guides/cross-platform/inspector/)
to get started.

# Known Limitations

* View selection is only supported on your main display.
* 3D view is not available on Windows
* Property grid editing is not available for Mac, and on Windows is limited to
  a few data types. Use the REPL for more powerful editing.
* As long as the Inspector addin/extension is installed and enabled in your IDE,
  we are injecting code into your app every time it starts in Debug mode. If you
  notice any strange behavior in your app, please try disabling or uninstalling
  the Inspector addin/extension, restarting the IDE, and rechecking. And please
  [file bugs][bugs] to let us know!
* If inspecting a UI element causes it to change in anyway, please
  [let us know][bugs], as this may indicate a bug.

# Reporting Bugs

Please [report bugs to bugzilla][bugs], and include log files.

<table>
<thead>
  <tr>
    <th>Component</th>
    <th>Mac Log File</th>
    <th>Windows Log File</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Inspector Client</td>
    <td>~/Library/Logs/Xamarin/Inspector/Xamarin Inspector {date}.log
</td>
    <td>%LOCALAPPDATA%\Xamarin\Inspector\logs\Xamarin Inspector {date}.log</td>
  </tr>
  <tr>
    <td>Xamarin Studio</td>
    <td>~/Library/Logs/XamarinStudio-5.0/Ide.log</td>
    <td>%LOCALAPPDATA%\XamarinStudio-5.0\Ide.log</td>
  </tr>
  <tr>
    <td>Visual Studio</td>
    <td/>
    <td>Copy the contents of the Output pane (proper logging will be added
      in a future release)</td>
  </tr>
</tbody>
</table>

# Requirements

#### Supported Operating Systems

* **Mac** - OS X 10.10 or greater
* **Windows** - Windows 7 or greater

#### Supported IDEs

* Xamarin Studio 5.10
* Visual Studio 2013/2015 with Xamarin 4 or later

#### Supported App Platforms

<table>
<thead>
  <tr>
    <th>App Platform</th>
    <th>IDE Support</th>
    <th>Notes</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Mac (Unified)</td>
    <td>Only supported in XS on Mac</td>
    <td></td>
  </tr>
  <tr>
    <td>iOS (Unified)</td>
    <td>Only supported in XS on Mac</td>
    <td/>
  </tr>
  <tr>
    <td>Android</td>
    <td>Supported in XS and VS</td>
    <td>
      <ul>
        <li>Must target Android >= 4.0.3</li>
        <li>Must have fastdev enabled</li>
        <li>Must use XAP or VS Android Emulator</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>WPF</td>
    <td>Only supported in VS on Windows</td>
    <td/>
  </tr>
</tbody>
</table>

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector

