---
id: E16B0A45-3390-4D01-B59D-95C638562168
title: "Xamarin.Android 8.2"
---

Last Update: 3/20/2018

<a class="action-button" href="https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/">System Requirements</a><a class="action-button" href="#whats-new">What's New</a><a class="action-button" href="#known-issues">Known Issues</a><a class="action-button" href="https://blog.xamarin.com/tag/android/">Blogs</a><a class="action-button" href="#oss">Open Source</a>

### Installing

* Visual Studio 2017 version 15.6 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)
* Visual Studio 2015 Tools for Xamarin – [Stable updater channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/#visualstudio)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Android Forums](https://forums.xamarin.com/categories/android), [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi?product=Android) and [Visual Studio Developer Community](https://developercommunity.visualstudio.com/) for existing issues. For new issues, let us know via the [Report a Problem](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) option found in your favorite IDE via `Help -> Report a Problem`.

### Release History

* [March 20th, 2018](#8-2-0-16) - Xamarin.Android 8.2.0.16
* [March 5th, 2018](#8-2-0-15) - Xamarin.Android 8.2.0.15

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

<a name="8-2-0-16" />

## March 20th, 2018 - Xamarin.Android 8.2.0.16

> This version is included in the Visual Studio 2017 version 15.6.3 release.

### Integrated Mono Features / Fixes

* [GitHub #7472](https://github.com/mono/mono/issues/7472)
    `NullReferenceException` when trying to use an extension method on a `null` object as an assignment value for an `Action` or `Func` variable

Xamarin.Android uses [Mono 5.8](http://www.mono-project.com/docs/about-mono/releases/5.8.0/)
[Commit 145ca63](https://github.com/mono/mono/commit/145ca63)

<a name="8-2-0-15" />

## March 5th, 2018 - Xamarin.Android 8.2.0.15

> This version is included in the Visual Studio 2017 version 15.6 release.

### Issues Fixed

* [Github #1164](https://github.com/xamarin/xamarin-android/issues/1164)
    Referenced dll's get deleted
* [Github #1286](https://github.com/xamarin/xamarin-android/issues/1286)
    Resource related intellisense breaks after Rebuilding
* [Github #1248](https://github.com/xamarin/xamarin-android/issues/1248):
    Generate error when JDK 9 is used.
* [Github #1149](https://github.com/xamarin/xamarin-android/issues/1149):
    Can not Export CREATOR Field for IParcelable instance
* [Github #1087](https://github.com/xamarin/xamarin-android/issues/1087):
    `Android.Telecom.RemoteConference` has wrong type
* [Github #1134](https://github.com/xamarin/xamarin-android/issues/1134):
    New APT0000 msbuild errors are being reported from aapt output parsing
* [Github #1135](https://github.com/xamarin/xamarin-android/issues/1135):
    Encountering new path escaping issues when using multidex/proguard on Windows
* [Github #1136](https://github.com/xamarin/xamarin-android/issues/1136):
    There is no longer an informative error message printed when building against a platform SDK version that is not installed
* [Bugzilla #56834](https://bugzilla.xamarin.com/show_bug.cgi?id=56834):
    Can't write resource Multidex warnings with VS for Mac 
* [Bugzilla #59804](https://bugzilla.xamarin.com/show_bug.cgi?id=59804):
    GC too aggressive on certain Android callbacks
* [Bugzilla #60236](https://bugzilla.xamarin.com/show_bug.cgi?id=60236):
    Cannot deploy to Android Oreo (Failure [INSTALL_FAILED_ALREADY_EXISTS: Attempt to re-install Mono.Android.DebugRuntime without first uninstalling.])
* [Bugzilla #60336](https://bugzilla.xamarin.com/show_bug.cgi?id=60336):
    Add support to `desugar` Java 8 .class files to be converted to Java 7 compatible .class files before dex 
* [Bugzilla #60444](https://bugzilla.xamarin.com/show_bug.cgi?id=60444):
    Apksigner fails to sign certain projects that define a low targetSdkVersion in their manifests
* [Bugzilla #60445](https://bugzilla.xamarin.com/show_bug.cgi?id=60445):
    Aapt MSBuild Task treats no default translation warnings as MSBuild errors
* [Bugzilla #60878](https://bugzilla.xamarin.com/show_bug.cgi?id=60878):
    Android design-time intellisense doesn't process global cache AARs
* [Bugzilla #60880](https://bugzilla.xamarin.com/show_bug.cgi?id=60880):
    Android design-time intellisense gets deleted by IncrementalClean
* [Bugzilla #60901](https://bugzilla.xamarin.com/show_bug.cgi?id=60901):
    Error on bundle.targets with the Zip task
* [Bugzilla #60940](https://bugzilla.xamarin.com/show_bug.cgi?id=60940):
    BroadcastReveicerAttribute is missing the Description property

### Integrated Mono Features / Fixes

Xamarin.Android uses [Mono 5.8](http://www.mono-project.com/docs/about-mono/releases/5.8.0/)
[commit da1e498](https://github.com/mono/mono/commit/da1e498).

<a name="whats-new"/>

## What's New in this Release

* [Android Oreo 8.1 Support](#android-oreo-8-1)

<a name="android-oreo-8-1" />

### Android Oreo 8.1 Support

Xamarin.Android brings binding support for Android Oreo 8.1 (API 27). See our documentation for more information on Android Oreo:

[https://developer.xamarin.com/guides/android/platform_features/introduction-to-oreo/](https://developer.xamarin.com/guides/android/platform_features/introduction-to-oreo/)

<a name="known-issues" />

## Known Issues

<a name="jdk9" />

### JDK 9

Xamarin.Android does not currently support JDK 9. It is recommended to use JDK 8 until Android officially supports JDK 9.

For more information on this topic, please see our documentation on this topic:

[https://developer.xamarin.com/guides/android/troubleshooting/questions/jdk9-errors/](https://developer.xamarin.com/guides/android/troubleshooting/questions/jdk9-errors/)

### AAPT MSBuild Errors

It has been found that specific `aapt` warnings are being promoted to MSBuild errors and thus the `Aapt` MSBuild task will fail.

[https://github.com/xamarin/xamarin-android/issues/1134](https://github.com/xamarin/xamarin-android/issues/1134)

<a name="oss" />
    
## OSS Core

Xamarin.Android 8.2 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-6) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-6) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).

