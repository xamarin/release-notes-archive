---
id: 71D8DEC9-DD81-44CF-8FEF-8DF65C34696B
title: "Xamarin.Android 9.0"
---

Last Update 2018-Sep-24

[System Requirements](https://docs.microsoft.com/xamarin/cross-platform/get-started/requirements)
| [What's New](#whats-new)
| [Blogs](https://blog.xamarin.com/tag/android/)
| [Open Source](#oss)

### Installing

* Visual Studio 2017 version 15.8 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac version 7.6 – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)

### Feedback

Your feedback is important to us. If there are any problems with this release, check our
[GitHub Issues](https://github.com/xamarin/xamarin-android/issues),
[Xamarin.Android Community Forums](https://forums.xamarin.com/categories/android) and
[Visual Studio Developer Community](https://developercommunity.visualstudio.com/)
for existing issues.  For new issues within the Xamarin.Android SDK, please report a
[GitHub Issue](https://github.com/xamarin/xamarin-android/issues/new).
For general Xamarin.Android experience issues, let us know via the
[Report a Problem](https://docs.microsoft.com/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017)
option found in your favorite IDE via `Help -> Report a Problem`.

### Release History

  * [August 29, 2018](#9-0-0-20) - Xamarin.Android 9.0.0.20 (Visual Studio 2017 version 15.8.2)
  * [August 23, 2018](#9-0-0-19) - Xamarin.Android 9.0.0.19 (Visual Studio 2017 for Mac version 7.6.1)
  * [August 14, 2018](#9-0-0-18) - Xamarin.Android 9.0.0.18 (Visual Studio 2017 version 15.8)

You can learn more about how we ship our releases in the
[Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/productinfo/vs2017-release-rhythm)
document.


<a name="9-0-0-20" />

#### August 29, 2018 - Xamarin.Android 9.0.0.20

> This version is included in the Visual Studio 2017 version 15.8.2 Servicing Update

##### Issues Fixed

  * [Mono 8627](https://github.com/mono/mono/issues/8627):
    The instruction pointer of the currently executing method is not on the recorded stack
  * [Mono 8848](https://github.com/mono/mono/issues/8848):
    Error when debugging.
  * [Mono 9262](https://github.com/mono/mono/issues/9262):
    App terminates : "Failed to Stop app: An error occured on client IDB4100448 while executing a reply for topic xvs/idb/4.10.0.448/stop-app"

##### Integrated Mono Features/Fixes

Xamarin.Android uses
[Mono 5.12](http://www.mono-project.com/docs/about-mono/releases/5.12.0/)
[Commit c5b8988d](https://github.com/mono/mono/commit/c5b8988d)


<a name="9-0-0-19" />

#### August 23, 2018 - Xamarin.Android 9.0.0.19

> This version is included in the Visual Studio 2017 for Mac version 7.6.1 release.

##### Issues Fixed

  * [GitHub 2007](https://github.com/xamarin/xamarin-android/issues/2007):
    Release build with Proguard on Mac fails on `PROGUARD : warning : there
    were 38 unresolved references to classes or interfaces.` and `"java"
    exited with code 1.`


<a name="9-0-0-18" />

#### August 14, 2018 - Xamarin.Android 9.0.0.18

> This version is included in the Visual Studio 2017 version 15.8 release.

##### Issues Fixed

  * [Bugzilla 7505](https://bugzilla.xamarin.com/show_bug.cgi?id=7505)
    `FileNotFoundException` when probing assemblies should provide more context.
  * [Bugzilla 59046](https://bugzilla.xamarin.com/show_bug.cgi?id=59046)
    Bindings Generator fails with `[ERROR] FATAL UNHANDLED EXCEPTION: System.ArgumentNullException: Value cannot be null.`
  * [GitHub 1374](https://github.com/xamarin/xamarin-android/issues/1374)
    Xamarin Android Lint checks fail on Windows when ran against a very simple app
  * [GitHub 1400](https://github.com/xamarin/xamarin-android/issues/1400)
    BCL test `TaskSchedulerTests.GetTaskSchedulersForDebugger_ReturnsDefaultScheduler()` fails when the linker is enabled.
  * [GitHub 1405](https://github.com/xamarin/xamarin-android/issues/1405):
    When "Use Shared Runtime" is unchecked, any code changes aren't picked up.
  * [GitHub 1438](https://github.com/xamarin/xamarin-android/issues/1438):
    Cannot find FSharp.Core or one of its dependencies during testing
  * [GitHub 1511](https://github.com/xamarin/xamarin-android/issues/1511)
    Unstable framework versions are used when `$(AndroidUselatestPlatformSDK)`=true
  * [GitHub 1519](https://github.com/xamarin/xamarin-android/issues/1519)
    Deploying to Android fails with zipalign error
  * [GitHub 1532](https://github.com/xamarin/xamarin-android/issues/1532)
    Error: Exception while loading assemblies: System.IO.FileNotFoundException: Could not load assembly 'Microsoft.Azure.Services.AppAuthentication, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'. Perhaps it doesn't exist in the Mono for Android profile?
  * [GitHub 1541](https://github.com/xamarin/xamarin-android/issues/1541)
    Aapt2 Task fails with `Error Access to the path 'obj\Debug\monoandroid81\android\src' is denied`.
  * [GitHub 1544](https://github.com/xamarin/xamarin-android/issues/1544):
    `Android.Runtime.ResourceIdManager.UpdateIdValues()` called multiple times, adds 23 seconds to application startup.
  * [GitHub 1651](https://github.com/xamarin/xamarin-android/issues/1651):
    Bundled app initialization error
  * [GitHub 1642](https://github.com/xamarin/xamarin-android/issues/1642)
    `ValidateJavaVersion` should check both java and javac version
  * [GitHub 1652](https://github.com/xamarin/xamarin-android/issues/1652)
    Links against ABI-unstable system `Mono.Cecil`
  * [GitHub 1669](https://github.com/xamarin/xamarin-android/issues/1669)
    Getting build failure for Cheesesquare sample in both debug and release mode
  * [GitHub 1670](https://github.com/xamarin/xamarin-android/issues/1670) (workaround):
    Updating to Visual Studio Community 7.5 on macOS causes ambiguous resource layouts
  * [GitHub 1678](https://github.com/xamarin/xamarin-android/issues/1678):
    New `error CS2001: Source file '...\obj\Debug\generated\' could not be found.`
    errors on rebuilding projects.
  * [GitHub 1698](https://github.com/xamarin/xamarin-android/issues/1698):
    Build warning: Name cannot begin with the '$' character
  * [GitHub 1711](https://github.com/xamarin/xamarin-android/issues/1711):
    Unable to inflate a layout which has custom controls with mixed naming
    casing and is included through a library project reference
  * [GitHub 1727](https://github.com/xamarin/xamarin-android/issues/1727):
    Deployment failures throw instead of declaring an Error + ErrorCode.
  * [GitHub 1748](https://github.com/xamarin/xamarin-android/issues/1748):
    `_CreateAapt2VersionCache` target always runs on master
  * [GitHub 1770](https://github.com/xamarin/xamarin-android/issues/1770):
    Unable to build project with a `$(TargetFrameworkVersion)` less than Android 5.0 on Windows with `$(AndroidUseAapt2)`=True.
  * [GitHub 1824](https://github.com/xamarin/xamarin-android/issues/1824):
    Cleaning no longer removes app project assembly and `.pdb` files from `$(IntermediateOutputPath)` on macOS.
  * [GitHub 1831](https://github.com/xamarin/xamarin-android/issues/1831):
    `TypeManager.RegisterType()` doesn't use type mappings.
  * [GitHub 1832](https://github.com/xamarin/xamarin-android/issues/1832):
    `JNINativeWrapper` shouldn't use Guids.
  * [GitHub 1888](https://github.com/xamarin/xamarin-android/issues/1888):
    Large libraries in binding causing dx error with too large of main dex file.
  * [GitHub 1962](https://github.com/xamarin/xamarin-android/issues/1962):
  * [GitHub 1780](https://github.com/xamarin/xamarin-android/issues/1780):
    Aapt2 throws an error if a `Resources/values/*` file contains a dash
  * [GitHub 1784](https://github.com/xamarin/xamarin-android/issues/1784):
    Intellisense can't recongize 'Resource.Dimension' definition.
  * [GitHub 1814](https://github.com/xamarin/xamarin-android/issues/1814):
    Secondary builds after touching .cs files in an app and library project
    are now slower in 15.8.
  * [GitHub 1816](https://github.com/xamarin/xamarin-android/issues/1816):
    No longer able to compile Mono.Android-Tests.csproj on macOS against d15-8.
  * [GitHub 1822](https://github.com/xamarin/xamarin-android/issues/1822):
    Allow storing native libs uncompressed in the `.apk`.
  * [Mono 8282](https://github.com/mono/mono/issues/8282):
    respect maximum length of a message when using `__android_log_write()`
  * [(community link)](https://developercommunity.visualstudio.com/content/problem/268148/jni-local-reference-table-overflow-issue-in-xamari.html):
    JNI local reference table overflow issue in Xamarin Android and `NetworkInterface.OperationalStatus`.
  * [(community link)](https://developercommunity.visualstudio.com/content/problem/218603/msbuild-failure-in-resolvelibraryprojectimports-ta.html):
    MSBuild failure in `<ResolveLibraryProjectImports/>` task.
  * Fix Code-Behind code generation for layouts with non-element root nodes, e.g. XML comments.


##### Integrated Mono Features/Fixes

Xamarin.Android uses
[Mono 5.12](http://www.mono-project.com/docs/about-mono/releases/5.12.0/)
[Commit 4fe3280b](https://github.com/mono/mono/commit/4fe3280b)

<a name="whats-new" />

### What's New in this Release

  * [Android Pie Support](#android-pie)
  * [Aapt2](#aapt2)
  * [Binding Assemblies and `$(AndroidCodegenTarget)`](#codegen-ji)
  * [Code Behind](#code-behind)


<a name="android-pie" />

#### Android Pie Support (API 28)

We're excited to announce Xamarin.Android support for Android Pie (API 28).
Android Pie introduces new features including display cutout support,
notification enhancements, multi-camera support, `AnimatedImageDrawable`, and
much more.

<a name="aapt2" />

#### Aapt2

Xamarin.Android has ***Experimental*** support for the
[Android Asset Packaging Tool v2.0](https://android.googlesource.com/platform/frameworks/base/+/master/tools/aapt2/readme.md).
`aapt2` allows for faster project *rebuilds* when an Android Resource
or Android Asset changes.  This will not help with *initial* project builds:

<table>
  <thead>
    <tr>
      <th>Tool</th>
      <th>Clean Build</th>
      <th>Build Touching only C#</th>
      <th>Build Touching only Resources</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">Aapt</td>
      <td style="text-align: right">00:00:51.74</td>
      <td style="text-align: right">00:00:08.91</td>
      <td style="text-align: right">00:00:25.26</td>
    </tr>
    <tr>
      <td style="text-align: left">Aapt2</td>
      <td style="text-align: right">00:00:50.70</td>
      <td style="text-align: right">00:00:08.64</td>
      <td style="text-align: right">00:00:08.44</td>
    </tr>
  </tbody>
</table>

Aapt2 support is currently disabled by default.  To enable it, please set
the `$(AndroidUseAapt2)` MSBuild property to True within your `.csproj`:

```xml
<PropertyGroup>
  <AndroidUseAapt2>True</AndroidUseAapt2>
</PropertyGroup>
```

Enabling Aapt2 support requires that Aapt2 be installed; it is included in the
Android SDK build-tools 25.0.2 package or later.  If `aapt2` cannot be found,
then an XA0112 warning will be logged, and `aapt` will be used instead.

If `aapt2 version` returns an unrecognized value, then `aapt2` support will be
disabled, an XA0111 warning will be logged, and `aapt` will be used instead.


<a name="codegen-ji" />

#### Binding Assemblies and `$(AndroidCodegenTarget)`

Xamarin.Android 9.0 changes the default value of the `$(AndroidCodegenTarget)`
MSBuild property within Bindings Libraries to `XAJavaInterop1`, from
`XamarinAndroid`.

This change results in binding assemblies which are smaller, faster, and
generate less garbage during invocations.

Unfortunately, this change means that the resulting binding assemblies cannot
be used with [Xamarin.Android 6.0][xa-6] and earlier.  Xamarin.Android 6.0 is
over 2.5 years old at this point, so we do not believe that this will be a
significant problem.

[xa-6]: https://developer.xamarin.com/releases/android/xamarin.android_6/xamarin.android_6.0/


<a name="code-behind" />

#### Bindings and Code-Behind

To make Android development more pleasant when working with Android Resources,
we've provided two new features known as bindings and code-behind.

To enable these new features, set the `$(AndroidGenerateLayoutBindings)` MSBuild
property to `True` in your .csproj file:

```xml
<PropertyGroup>
    <AndroidGenerateLayoutBindings>true</AndroidGenerateLayoutBindings>
</PropertyGroup>
```

##### Bindings

Bindings generates a class per each Android layout file which contains strongly
typed properties for all of the Android Resource Ids in the layout file.  This
allows you to instantiate a new `Binding` to then access your respective `View`
classes in your resource file without calling `FindViewById()`.

For example, take the following layout file:

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:xamarin="http://schemas.xamarin.com/android/xamarin/tools">
  <Button android:id="@+id/myButton" />
  <fragment
      android:id="@+id/log_fragment"
      android:name="commonsamplelibrary.LogFragment"
      xamarin:managedType="CommonSampleLibrary.LogFragment"
  />
  <fragment
      android:id="@+id/secondary_log_fragment"
      android:name="CommonSampleLibrary.LogFragment"
  />
</LinearLayout>
```

You would then access the binding in your Activity to provide your Views:

```csharp
partial class MainActivity : Activity {
  protected override void OnCreate (Bundle savedInstanceState)
  {
    base.OnCreate (savedInstanceState);

    SetContentView (Resource.Layout.Main);
    var binding     = new Binding.Main (this);
    Button button   = binding.myButton;
    button.Click   += delegate {
        button.Text = $"{count++} clicks!";
    };
  }
}
```

##### Code-Behind

Code-behind generates a `partial` class that contains strongly typed properties
for all of the Android Resource Ids in the layout file.  Code-behind builds
on-top of the Binding mechanism in which you can opt-in to Code-Behind
generation using our new `xamarin:classes` XML attribute which is a `;`
separated list of full class names to be generated.

For example, take the following layout file:

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:xamarin="http://schemas.xamarin.com/android/xamarin/tools"
    xamarin:classes="Example.MainActivity">
  <Button android:id="@+id/myButton" />
  <fragment
      android:id="@+id/log_fragment"
      android:name="commonsamplelibrary.LogFragment"
      xamarin:managedType="CommonSampleLibrary.LogFragment"
  />
  <fragment
      android:id="@+id/secondary_log_fragment"
      android:name="CommonSampleLibrary.LogFragment"
  />
</LinearLayout>
```

You would then access Views in your Activity directly:

```csharp
partial class MainActivity : Activity {
  protected override void OnCreate (Bundle savedInstanceState)
  {
    base.OnCreate (savedInstanceState);

    SetContentView (Resource.Layout.Main);

    myButton.Click += delegate {
        button.Text = $"{count++} clicks!";
    };
  }
}
```

For more information about this feature, please see our documentation here:
[https://github.com/xamarin/xamarin-android/blob/master/Documentation/guides/LayoutCodeBehind.md](https://github.com/xamarin/xamarin-android/blob/master/Documentation/guides/LayoutCodeBehind.md)


<a name="oss" />

### OSS Core

Xamarin.Android 9.0 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-8) repo
* Android bindings and MSBuild tooling are in the [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-8) repo.
* Chat is in the [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).
