---
id: 3AE790E4-9E5B-40FB-9236-1551A7BCA78D
title: "Xamarin.Android 8.3"
---

Last Update 5/31/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/android/) | [Open Source](#oss)

### Installing

* Visual Studio 2017 version 15.7 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)

### Feedback

Your feedback is important to us. If there are any problems with this release, check our [GitHub Issues](https://github.com/xamarin/xamarin-android/issues), [Xamarin.Android Community Forums](https://forums.xamarin.com/categories/android) and [Visual Studio Developer Community](https://developercommunity.visualstudio.com/) for existing issues. For new issues within the Xamarin.Android SDK, please report a [GitHub Issue](https://github.com/xamarin/xamarin-android/issues/new). For general Xamarin.Android experience issues, let us know via the [Report a Problem](https://docs.microsoft.com/en-us/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) option found in your favorite IDE via `Help -> Report a Problem`.

### Release History

* [May 31st, 2018](#8-3-3-2) - Xamarin.Android 8.3.3.2
* [May 7th, 2018](#8-3-0-19) - Xamarin.Android 8.3.0.19

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

<a name="8-3-3-2" />

#### May 31st, 2018 - Xamarin.Android 8.3.3.2

> This version is included in the Visual Studio 2017 version 15.7.3 release.

##### Issues Fixed

* [GitHub 1651](https://github.com/xamarin/xamarin-android/issues/1651)
    Bundled app initialization error (vs 15.7 preview)
* [GitHub 1657](https://github.com/xamarin/xamarin-android/pull/1657)
    [Xamarin.Android.Build.Tasks] Designer items should be const for apps.
* [GitHub 1679](https://github.com/xamarin/xamarin-android/issues/1679)
    System.Memory facade is missing from the installation
* [GitHub 1731](https://github.com/xamarin/xamarin-android/pull/1731)
    [Xamarin.Android.Build.Tasks] Fix Intellisense errors for switch statements

<a name="8-3-0-19" />

#### May 7th, 2018 - Xamarin.Android 8.3.0.19

> This version is included in the Visual Studio 2017 version 15.7 release.

##### Issues Fixed

* [Bugzilla 58413](https://bugzilla.xamarin.com/show_bug.cgi?id=58413)
    Environment.Tickcount is changed when the date is changed in android.
* [GitHub 1498](https://github.com/xamarin/xamarin-android/issues/1498)
    Unable to build against preview Android API levels.
* [GitHub 1541](https://github.com/xamarin/xamarin-android/issues/1541)
    Aapt2 Task fails with Error Access to the path `obj\Debug\monoandroid81\android\src` is denied.
* [GitHub 1511](https://github.com/xamarin/xamarin-android/issues/1511)
    Unstable framework versions are used when `$(AndroidUselatestPlatformSDK)=true`.
* [GitHub 1474](https://github.com/xamarin/xamarin-android/pull/1474)
    Fix an issue where the 'ref' nuget is not found on windows.
* [GitHub 1262](https://github.com/xamarin/xamarin-android/issues/1262)
    Managed Resource Parser is not aware of some Resource types, and fails to provide intellisense for them.
* [DevCom 202643](https://developercommunity.visualstudio.com/content/problem/202643/the-convertresourcescases-task-failed-unexpectedly.html)
    The "ConvertResourcesCases" task failed unexpectedly.
* [GitHub 1323](https://github.com/xamarin/xamarin-android/pull/1323)
    Updates `CalculateProjectDependencies` to match new spec.
* [GitHub 1327](https://github.com/xamarin/xamarin-android/pull/1327)
    Adds support for Generated Resources via VSForMac.
* [GitHub 1321](https://github.com/xamarin/xamarin-android/pull/1321)
    Adds tests for `<ResolveSdks/>`
* [GitHub 1221](https://github.com/xamarin/xamarin-android/issues/1221)
    Prevents `$(AndroidUseLatestPlatformSdk)` from using Unstable APIs
* [GitHub 1287](https://github.com/xamarin/xamarin-android/issues/1287)
    Adds Default Metadata for `@(AndroidResource)` Items.
* [GitHub 1154](https://github.com/xamarin/xamarin-android/issues/1154)
    Improves .NET Standard support.
* [GitHub 1331](https://github.com/xamarin/xamarin-android/issues/1331)
    Fixes Proguard crash on startup - preserves ManagedPeer class.

##### Integrated Mono Featues/Fixes

Xamarin.Android uses [Mono 5.10](http://www.mono-project.com/docs/about-mono/releases/5.10.0/)
[Commit ea8a24b1](https://github.com/mono/mono/commit/ea8a24b1)

<a name="whats-new" />

### What's New in this Release

* [TLS 1.2+ Support by Default](#tls-1-2)

<a name="tls-1-2" />

#### TLS 1.2+ Support by Default

[Xamarin.Android introduces BTLS as default TLS 1.2+ provider.](https://developer.xamarin.com/guides/android/application_fundamentals/http-stack/)

### OSS Core

Xamarin.Android 8.3 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-7) repo
* Android bindings and MSBuild tooling are in the [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-7) repo.
* Chat is in the [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).
