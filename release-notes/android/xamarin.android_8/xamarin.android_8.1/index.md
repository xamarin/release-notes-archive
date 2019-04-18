---
id: E16B0A45-3390-4D01-B59D-95C638562168
title: "Xamarin.Android 8.1"
---

Last Update: 1/25/2018

<a class="action-button" href="https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/">System Requirements</a><a class="action-button" href="#whats-new">What's New</a><a class="action-button" href="#known-issues">Known Issues</a><a class="action-button" href="https://blog.xamarin.com/tag/android/">Blogs</a><a class="action-button" href="#oss">Open Source</a>

### Installing

* Visual Studio 2017 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)
* Visual Studio 2015 Tools for Xamarin – [Stable updater channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/#visualstudio)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Android Forums](https://forums.xamarin.com/categories/android), [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi?product=Android) and [Visual Studio Developer Community](https://developercommunity.visualstudio.com/) for existing issues. For new issues, let us know via the [Report a Problem](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) option found in your favorite IDE via `Help -> Report a Problem`.

### Release History

* [January 25th, 2018](#8-1-5-0) - Xamarin.Android 8.1.5.0
* [January 9th, 2018](#8-1-3-0) - Xamarin.Android 8.1.3.0
* [December 14th, 2017](#8-1-0-25) - Xamarin.Android 8.1.0.25
* [December 4th, 2017](#8-1-0-24) - Xamarin.Android 8.1.0.24

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

<a name="8-1-5-0" />

## January 25th, 2018 - Xamarin.Android 8.1.5.0

> This version is included in the Visual Studio 2017 version 15.5.5 release.

### Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.4](http://www.mono-project.com/docs/about-mono/releases/5.4.0/)
[commit 6fcdbac8](https://github.com/mono/mono/commit/6fcdbac8447604fb0a56cd866ad45e8f1916e7f2).

### Issues Fixed

* [Bugzilla #61073](https://bugzilla.xamarin.com/show_bug.cgi?id=61073):
    fix classes-zip inception
* [Bugzilla #61002](https://bugzilla.xamarin.com/show_bug.cgi?id=61002):
    Runtime exception: Cannot access a disposed object. Object name: 'MobileAuthenticatedStream'.

<a name="8-1-3-0" />

## January 9th, 2018 - Xamarin.Android 8.1.3.0

> This version is included in the Visual Studio 2017 version 15.5.3 release.

### Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.4](http://www.mono-project.com/docs/about-mono/releases/5.4.0/)
[commit b293f453](https://github.com/mono/mono/commit/b293f453027bc075ce636988b383451e5c346347).

### Issues Fixed

* [60625](https://bugzilla.xamarin.com/show_bug.cgi?id=60625):
    local-propagation.c:562, condition `ins->opcode > MONO_CEE_LAST' not met

<a name="8-1-0-25" />

## December 14th, 2017 - Xamarin.Android 8.1.0.25

> This version is included in the Visual Studio 2017 version 15.5.2 release.

### Issues Fixed

* [Developer Community #155693](https://developercommunity.visualstudio.com/content/problem/155693/xamarin-android-project-cannot-build-because-ranim.html):
    Xamarin Android project cannot build because R$anim.class is in use

<a name="8-1-0-24" />

## December 4th, 2017 - Xamarin.Android 8.1.0.24

> This version is included in the Visual Studio 2017 version 15.5 release.

### Issues Fixed

* [51664](https://bugzilla.xamarin.com/show_bug.cgi?id=51664):
    View.PerformAccessibilityAction and other AccessibilityAction methods map to the incorrect enum?
* [51689](https://bugzilla.xamarin.com/show_bug.cgi?id=51689):
    Xamarin does not handle "${applicationId}" build variable
* [56648](https://bugzilla.xamarin.com/show_bug.cgi?id=56648):
    warning XA0105: The $(TargetFrameworkVersion) for Mono.Android.Export.dll (v7.1) is greater than the $(TargetFrameworkVersion) for your project (v6.0). You need to increase the $(TargetFrameworkVersion) for your project.
* [56819](https://bugzilla.xamarin.com/show_bug.cgi?id=56819):
    Implementing java interfaces without inheriting Java.Lang.Object should fail early
* [56859](https://bugzilla.xamarin.com/show_bug.cgi?id=56859):
    Android Designer does not render Spinner correctly.
* [57342](https://bugzilla.xamarin.com/show_bug.cgi?id=57342):
    Crash - NetStandard library - could not load assembly during startup registration.
* [57849](https://bugzilla.xamarin.com/show_bug.cgi?id=57849):
    Getting "CSC : error CS1703: Multiple assemblies with equivalent identity have been imported" errors when installing nuget dependencies
* [57991](https://bugzilla.xamarin.com/show_bug.cgi?id=57991):
    Intellisense for a class library project in same solution fails to load in Xamarin.Android
* [58403](https://bugzilla.xamarin.com/show_bug.cgi?id=58403):
    Mismatching listener types/members generated broken event name
* [58740](https://bugzilla.xamarin.com/show_bug.cgi?id=58740):
    Building default Android project after adding Fsharp.core from nuget with 'link SDK assemblies only' dies with exception
* [59045](https://bugzilla.xamarin.com/show_bug.cgi?id=59045):
    JNI ERROR (app bug): attempt to use stale Local 0x19 (should be 0x100019)
* [59235](https://bugzilla.xamarin.com/show_bug.cgi?id=59235):
    [mono-2017-06] android.runtime.JavaProxyThrowable: System.ObjectDisposedException: Cannot access a disposed object.
* [59355](https://bugzilla.xamarin.com/show_bug.cgi?id=59355):
    Adding a control to a ViewGroup in the Document Outline creates two visual controls on the designer surface/xml.
* [59516](https://bugzilla.xamarin.com/show_bug.cgi?id=59516):
    Add fix from Bug 59015 - SIGABRT after executing async method
* [59651](https://bugzilla.xamarin.com/show_bug.cgi?id=59651):
    Xamarin.Forms build fails with command line overflow.
* [59714](https://bugzilla.xamarin.com/show_bug.cgi?id=59714):
    AndroidComponentInfoSystemImage.Abi reads Default for an x86 image
* [59764](https://bugzilla.xamarin.com/show_bug.cgi?id=59764):
    error APT0000: libpng warning: iCCP: Not recognizing known sRGB profile that has been edited with Android SDK Build Tools 23.0.2
* [59822](https://bugzilla.xamarin.com/show_bug.cgi?id=59822):
    Building an Android solution in Release mode that references a net standard project with a Microsoft.Identity reference results in a linker error.
* [59867](https://bugzilla.xamarin.com/show_bug.cgi?id=59867):
    Trying to build with an 'obsolete' target framework version produces a different error code in 15.5
* [60080](https://bugzilla.xamarin.com/show_bug.cgi?id=60080):
    After upgrading to latest Xamarin- Visual Studio stuck/hangs at initialization of xamarin.andorid project while loading projects
* [60179](https://bugzilla.xamarin.com/show_bug.cgi?id=60179):
    The APK includes x86_64 when targeting x86
* [60343](https://bugzilla.xamarin.com/show_bug.cgi?id=60343):
    Fixes an `aapt` error that occurs because DesignTime builds did not have their own set of cache files. DesignTime builds now have their own set of cache files which do not conflict with the main build's cache files.

<a name="integrated-mono" />

### Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.4](http://www.mono-project.com/docs/about-mono/releases/5.4.0/)
[commit 950ea65c](https://github.com/mono/mono/commits/950ea65c3ba571cd139dc34b48d7101a2e894993).

<a name="whats-new"/>

## What's New in this Release

* [Design-Time Builds on Windows using the Managed Resource Parser](#design-time-builds-managed-resource-parser)

<a name="design-time-builds-managed-resource-parser" />

### Design-Time Builds on Windows using the Managed Resource Parser (Experimental)

Xamarin.Android 8.1 brings support for design-time builds using a managed resource parser on Windows. Design-time builds are special builds that are launched by the project system to gather information to populate language services and project services. Design-time builds are indirectly launched in response to a user action such as changing project items by adding/removing files, modifying references, switching configurations or altering build settings.

This behavior is disabled by default. You can opt-in to this feature by setting the `$(AndroidUseManagedDesignTimeResourceGenerator)` property to `True` inside your project's `.csproj`:

```
<PropertyGroup>
  <AndroidUseManagedDesignTimeResourceGenerator>True</AndroidUseManagedDesignTimeResourceGenerator>
</PropertyGroup>
```

This will enable the managed resource parser rather than `aapt`. This will not disable other design-time build features.

For more information about design-time builds, please see the following documentation:

[https://github.com/dotnet/project-system/blob/master/docs/design-time-builds.md#design-time-builds](https://github.com/dotnet/project-system/blob/master/docs/design-time-builds.md#design-time-builds)

<a name="known-issues" />

## Known Issues

<a name="jdk9" />

### JDK 9

Xamarin.Android does not currently support JDK 9. It is recommended to use JDK 8 until Android officially supports JDK 9.

For more information on this topic, please see our documentation on this topic:

[https://developer.xamarin.com/guides/android/troubleshooting/questions/jdk9-errors/](https://developer.xamarin.com/guides/android/troubleshooting/questions/jdk9-errors/)

<a name="class-not-found" />

### Java.lang.ClassNotFoundException

We have had multiple reports regarding applications running into a "Java.Lang.ClassNotFoundException: Didn't find class <md5.ClassName> on path: DexPathList" exception.

[Developer Community](https://developercommunity.visualstudio.com/content/problem/171375/javalangclassnotfoundexception-is-thrown-after-run.html)

<a name="known-issue-managed-resource-parser" />

### Managed Resource Parser

By opting-into the Managed Resource Parser, we have discovered that the Android Designer is incompatible for the following reasons:

* [60878](https://bugzilla.xamarin.com/show_bug.cgi?id=60878):
    Android design-time intellisense doesn't process global cache AARs
* [60880](https://bugzilla.xamarin.com/show_bug.cgi?id=60880):
    Android design-time intellisense gets deleted by IncrementalClean 
* [60881](https://bugzilla.xamarin.com/show_bug.cgi?id=60881):
    Android design-time intellisense prevents designer from working with support libraries other custom controls

<a name="oss" />
    
## OSS Core

Xamarin.Android 8.1 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-5) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-5) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).

