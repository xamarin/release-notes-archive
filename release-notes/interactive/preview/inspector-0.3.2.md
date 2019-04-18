---
id: 4359E70F-9D9C-4954-9D6B-33ED27F5E0FB
title: "Inspector Preview 0.3.2"
---

* [Download for Mac](https://download.xamarin.com/inspector/XamarinInspector.pkg)
* [Download for Windows](https://download.xamarin.com/inspector/XamarinInspector.msi)

This is a bugfix release for the
[Xamarin Inspector preview](http://developer.xamarin.com/releases/inspector/preview/inspector-0.3.1/),
fixing several issues reported by customers in the first release. We were excited
to receive so much feedback and look forward to all that is yet to come!

Check out
[the initial release notes](http://developer.xamarin.com/releases/inspector/preview/inspector-0.3.1/#What_does_it_do)
or
[our documentation](https://developer.xamarin.com/guides/cross-platform/inspector/)
for more details on the Inspector.

Also be sure to ask questions on the [Inspector forum](http://forums.xamarin.com/categories/inspector)
and [file any bugs](https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector) you may encounter.

# Changes Since 0.3.1

* Nicer rendering of exceptions. Stack frames are now shown in syntax highlighted
  C# instead of CIL representation making them easier to read and understand. If
  a frame's source code is accessible on disk, clicking the file name for the frame
  will open it and jump to the appropriate line in Xamarin Studio. This can be very
  powerful for debugging via experimentation in the Inspector. Inner exceptions are
  also collapsible.

* Prevent smart quotes and other text substitutions from happening in REPL on
  first run (#[35554][35554]).

* Prevent Inspector attempting to reach disposed objects from crashing app
  (#[35592][35592]).

* Disabling the Xamarin Studio addin no longer requires a restart afterward.

* Xamarin Inspector support can now be disabled on a per-project basis.

* IDE About dialogs now include Inspector version information.

* When Inspector addin impacts a build, details will be included in the build
  output.

* Inspect button in the debug toolbar in Xamarin Studio will always be shown when
  debugging if a project flavor is potentially supported. In cases where a project
  is not, the button will be disabled and a tooltip will offer details as to why
  Inspector is not supported, such as:
    * Explicitly disabled for the project/configuration
    * Unsupported target platform or framework (e.g. iOS supports only the simulator)
    * iOS, Mac, or Android linker is enabled (#[35569][35569])
    * Android deployment target is too old

* The Visual Studio extension now produces log files in the same directory as
  other Xamarin extensions.

# Other Notes

Please make sure you are using Xamarin.iOS 9.2.1.51 or greater to avoid
[crashes when using HTTPS][35555].

# Known Issues

* When inspecting WPF apps, exceptions may have [missing stack frames][35838]. This
appears to be an issue with the .NET (Microsoft) runtime. iOS, Mac, and Android
applications are not affected since they use the Mono runtime.

[35554]: https://bugzilla.xamarin.com/show_bug.cgi?id=35554
[35555]: https://bugzilla.xamarin.com/show_bug.cgi?id=35555
[35569]: https://bugzilla.xamarin.com/show_bug.cgi?id=35569
[35592]: https://bugzilla.xamarin.com/show_bug.cgi?id=35592
[35838]: https://bugzilla.xamarin.com/show_bug.cgi?id=35838

[bugs]: https://bugzilla.xamarin.com/enter_bug.cgi?product=Workbooks%20%26%20Inspector

