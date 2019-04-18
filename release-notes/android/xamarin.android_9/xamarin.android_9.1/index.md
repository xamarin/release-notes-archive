---
id: 3D9131A9-A192-4B7C-A7E9-7AB780536CE3
title: "Xamarin.Android 9.1"
---

Last Update 2018-Dec-11

[System Requirements](https://docs.microsoft.com/xamarin/cross-platform/get-started/requirements)
| [What's New](#whats-new)
| [Blogs](https://blog.xamarin.com/tag/android/)
| [Open Source](#oss)

## Installing

* Visual Studio 2017 version 15.9 – [Visual Studio Installer](https://www.visualstudio.com/vs/)
* Visual Studio 2017 for Mac version 7.7 – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)

<a name="whats-new" />

## What's New in this Release

> ⚠️ **Important**
>
> [Xamarin.Android 9.1.4.2 Security Advisory Notices](#9-1-4-2)

* * *

  * [Build and Deployment Performance Improvements](#build-performance)

<a name="build-performance" />

### Build and Deployment Performance Improvements

This release includes several improvements to incremental build and deployment
times.  For example, in a test development environment, the incremental build
time after modifying one XAML page in the [SmartHotel360 sample
app][smart-hotel] has dropped from 11 seconds to 9 seconds, and the
corresponding deployment time has dropped from 9 seconds to 5 seconds.

[smart-hotel]: https://github.com/jonathanpeppers/SmartHotel360-mobile-desktop-apps/tree/msbuild-timing

  * See the [Build Performance Results][performance-wiki] page on the project
    wiki for additional comparisons as well as updates about the on-going work
    to continue to improve performance.
  * Follow along with the [latest numbers][continuous-performance] from the
    continuous integration builds.

[performance-wiki]: https://github.com/xamarin/xamarin-android/wiki/Build-Performance-Results

[continuous-performance]: https://jenkins.xamarin.com/view/Xamarin.Android/job/xamarin-android/plot/Build%20times/

#### Specific Improvements

  * [GitHub PR 1938](https://github.com/xamarin/xamarin-android/pull/1938):
    `ResolveSdks` now caches the output of `java -version` and `javac -version`
    in memory, speeding up builds with multiple Xamarin.Android projects.
  * [GitHub PR 1957](https://github.com/xamarin/xamarin-android/pull/1957):
    Design-time builds were preventing future *full* builds from building
    incrementally.
  * [GitHub PR 2088](https://github.com/xamarin/xamarin-android/pull/2088):
    Fix incremental builds for Xamarin.Forms projects.
  * [GitHub PR 2093](https://github.com/xamarin/xamarin-android/pull/2093):
    Improve LINQ usage in `ConvertResourcesCases`
  * [GitHub PR 2130](https://github.com/xamarin/xamarin-android/pull/2130):
    Move inline C# MSBuild task to a compiled assembly
  * [GitHub PR 2131](https://github.com/xamarin/xamarin-android/pull/2131):
    Remove unnecessary MSBuild target, simplify inputs to `_CompileToDalvik` 
  * [GitHub PR 2132](https://github.com/xamarin/xamarin-android/pull/2132):
    The `_BuildLibraryImportsCache` target was *always* running
  * [GitHub PR 2140](https://github.com/xamarin/xamarin-android/pull/2140):
    Leave `classes.zip` uncompressed, to speed up `javac` and `dx`
  * [GitHub PR 2157](https://github.com/xamarin/xamarin-android/pull/2157):
    Build Xamarin [Java.Interop](https://github.com/xamarin/java.interop) as a
    Xamarin.Android class library rather than a Portable Class Library.  This
    reduces the number of assemblies references that need to be resolved during
    app builds.

## Release History

  * [December 11, 2018](#9-1-4-2) - Xamarin.Android 9.1.4.2
  * [November 28, 2018](#9-1-0-38) - Xamarin.Android 9.1.0.38 in Visual Studio 2017 for Mac version 7.7
  * [November 13, 2018](#9-1-0-38) - Xamarin.Android 9.1.0.38 in Visual Studio 2017 version 15.9

You can learn more about how we ship our releases in the
[Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/productinfo/vs2017-release-rhythm)
document.

<a name="9-1-4-2" />

## December 11, 2018 - Xamarin.Android 9.1.4.2

> This version is included in the Visual Studio 2017 version 15.9.4 and Visual
> Studio 2017 for Mac version 7.7 releases.

### Security Advisory Notices

[CVE-2018-8292 Xamarin.Android Information Disclosure Vulnerability][cve-2018-8292]

An information disclosure vulnerability exists in Xamarin.Android when
authentication information is inadvertently exposed in a redirect when the
`AndroidClientHandler` for `HttpClient` is used.  The managed
`HttpClientHandler` is not affected.  An attacker who successfully exploited
this vulnerability could use the information to further compromise the web
application.  This latest Xamarin.Android update addresses the vulnerability by
correcting how `AndroidClientHandler` handles redirects.

[cve-2018-8292]: https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2018-8292

### Issues Fixed

  * [GitHub 1923](https://github.com/xamarin/xamarin-android/issues/1923):
    HTTP redirects to relative URLs caused "System.InvalidCastException: Unable
    to convert instance of type 'Java.Net.URLConnectionInvoker' to type
    'Java.Net.HttpURLConnection'" exceptions when `HttpClient` was set to use
    `AndroidClientHandler`.
  * [GitHub 1924](https://github.com/xamarin/xamarin-android/issues/1924):
    HTTP authorization headers were not cleared after HTTP redirects when
    `HttpClient` was set to use `AndroidClientHandler`
    ([CVE-2018-8292][cve-2018-8292]).  `HttpClient` uses `AndroidClientHandler`
    if an instance of `AndroidClientHandler` is passed to the `HttpClient`
    constructor or if the [`$(AndroidHttpClientHandlerType)`][build-process]
    MSBuild property or `XA_HTTP_CLIENT_HANDLER_TYPE` environment variable is
    set to `Xamarin.Android.Net.AndroidClientHandler` and the `HttpClient`
    constructor is called with no arguments.

[build-process]: https://docs.microsoft.com/xamarin/android/deploy-test/building-apps/build-process

### Integrated Mono Features/Fixes

Xamarin.Android uses
[Mono 5.14](http://www.mono-project.com/docs/about-mono/releases/5.14.0/)
[Commit 000780ca](https://github.com/mono/mono/commit/000780ca82c87316227f1da94314587022d02f70)

  * [GitHub 11731](https://github.com/mono/mono/issues/11731):
    The non-generic versions of a few types related to `ValueTask` were not yet
    available in Xamarin.Android's *mscorlib.dll*.  Those non-generic types are
    now available.  The corresponding *System.Threading.Tasks.Extensions.dll*
    facade assembly will be added in the next Xamarin.Android feature release.

<a name="9-1-0-38" />

## November 13, 2018 - Xamarin.Android 9.1.0.38

> This version is included in the Visual Studio 2017 version 15.9 and Visual
> Studio 2017 for Mac version 7.7 releases.

### Issues Fixed

  * [GitHub 1584](https://github.com/xamarin/xamarin-android/issues/1584):
    The Xamarin.Android developer tools in Visual Studio 2017 on Windows
    included a separate copy of the fairly large API documentation .xml file for
    each target Android API level.  A new capability in the latest Visual Studio
    2017 release means that now only one copy of the file is needed.
  * [GitHub 1766](https://github.com/xamarin/xamarin-android/issues/1766):
    Builds did not provide a warning to caution users that Google Play now
    [requires][targetsdk] new apps and app updates to target at least Android
    8.0 (API level 26).
  * [GitHub 1770](https://github.com/xamarin/xamarin-android/issues/1770):
    Some warnings from AAPT were being treated as errors in projects using the
    new [experimental support for AAPT2][aapt2].
  * [GitHub 1828](https://github.com/xamarin/xamarin-android/issues/1828):
    Updating NuGet packages could leave intermediate build files in a state
    where a `Rebuild` was required.
  * [GitHub 1931](https://github.com/xamarin/xamarin-android/issues/1931):
    `AndroidClientHandler` was using commas rather than spaces in the HTTP
    `User-Agent` header.
  * [GitHub 1958](https://github.com/xamarin/xamarin-android/issues/1958):
    Design-time builds were preventing future *full* builds from building
    incrementally.
  * [GitHub 1960](https://github.com/xamarin/xamarin-android/issues/1960):
    Building two or more Xamarin.Android projects at the same time could lead to
    unexpected warnings due to a shared temporary file.
  * [GitHub PR 1971](https://github.com/xamarin/xamarin-android/pull/1971):
    Invalid Android resource files caused a generic exception message during
    design-time builds rather than a more informative error message.
  * [GitHub PR 1973](https://github.com/xamarin/xamarin-android/pull/1973):
    Apps would exit due to an exception if built with `$(AndroidEnableDesugar)`
    enabled, unless ProGuard or multidex was also enabled.
  * [GitHub PR 1984](https://github.com/xamarin/xamarin-android/pull/1984):
    Apps deployed via fast deployment would crash during startup if
    Xamarin.Android had been updated or if the Mono shared runtime had been
    manually uninstalled between deployments.
  * [GitHub 1985](https://github.com/xamarin/xamarin-android/issues/1985):
    The `$(AndroidResgenExtraArgs)` MSBuild property caused unclear error
    message in projects using the new [experimental support for AAPT2][aapt2]
    rather than indicating that the property was no longer applicable.  Also,
    new `aapt2` properties `$(AndroidAapt2CompileExtraArgs)` and
    `$(AndroidAapt2LinkExtraArgs)` were not yet available.
  * [GitHub 2047](https://github.com/xamarin/xamarin-android/issues/2047):
    Only one resource ID was being generated when two resources had names that
    were the same except for capitalization in projects using the new
    [experimental support for AAPT2][aapt2].
  * [GitHub 2060](https://github.com/xamarin/xamarin-android/issues/2060):
    Per-ABI APKs from projects that had both `$(AndroidUseApkSigner)` and
    `$(AndroidCreatePackagePerAbi)` enabled were not signed.
  * [GitHub PR 2084](https://github.com/xamarin/xamarin-android/pull/2084):
    The chances of hitting a `PathTooLongException` increased in Xamarin.Android
    9.0 due to the new subdirectories that preserve outputs from previously
    selected target frameworks ([GitHub PR
    1628](https://github.com/xamarin/xamarin-android/pull/1628)).
  * [GitHub 2183](https://github.com/xamarin/xamarin-android/issues/2183):
    Builds could fail on a ".../obj/Release/lp/ is not empty" error if the
    *Updating Resources* background build step was running when a build was
    started.
  * [GitHub 2205](https://github.com/xamarin/xamarin-android/issues/2205):
    Android resource conflicts could occur after rebuilds in projects
    referencing the Xamarin.GooglePlayServices.Basement NuGet package if the
    projects included a *google-services.json* file and had [experimental
    `aapt2` support][aapt2] enabled.
  * [GitHub PR 2249](https://github.com/xamarin/xamarin-android/pull/2249):
    Builds did not provide a warning to caution users that support for the
    `armeabi` value in `$(AndroidSupportedAbis)` would be removed in the next
    releases after Visual Studio 2017 version 15.9 and Visual Studio 2017 for
    Mac version 7.7.
  * [GitHub PR 2258](https://github.com/xamarin/xamarin-android/pull/2258):
    A few build tasks were generating warnings that did not include numbered
    warning codes.  A few other tasks were emitting diagnostic information as
    warnings rather than debug messages.
  * [GitHub PR 2329](https://github.com/xamarin/xamarin-android/pull/2329):
    Builds did not provide compilation warnings on individual types to caution
    users that support for the `v2.3`, `v4.0.3`, `v4.1`, `v4.2`, and `v4.3`
    values in `$(TargetFrameworkVersion)` would be removed in the next releases
    after Visual Studio 2017 version 15.9 and Visual Studio 2017 for Mac version
    7.7.
  * A few different incompatibility issues and unclear error messages could
    happen when using the Microsoft [Mobile OpenJDK Distribution
    Preview](https://docs.microsoft.com/xamarin/android/get-started/installation/openjdk)
    or when no JDK was installed.
  * Changing the `android:versionCode` app manifest attribute to a lower number
    would lead to an "\[INSTALL\_FAILED\_VERSION\_DOWNGRADE\]" error during
    deployment.
  * `cmd.exe` windows were opening in some cases for steps that launched tools
    from the Android toolchain.

[aapt2]: https://developer.xamarin.com/releases/android/xamarin.android_9/xamarin.android_9.0/#aapt2
[targetsdk]: https://support.google.com/googleplay/android-developer/answer/113469#targetsdk

### Integrated Mono Features/Fixes

Xamarin.Android uses
[Mono 5.14](http://www.mono-project.com/docs/about-mono/releases/5.14.0/)
[Commit 969357ac](https://github.com/mono/mono/commit/969357ac02b2c08a43ef89d98aca550d3648bf00)

## Feedback

Your feedback is important to us.  If there are any problems with this release, check our
[GitHub Issues](https://github.com/xamarin/xamarin-android/issues),
[Xamarin.Android Community Forums](https://forums.xamarin.com/categories/android) and
[Visual Studio Developer Community](https://developercommunity.visualstudio.com/)
for existing issues.  For new issues within the Xamarin.Android SDK, please report a
[GitHub Issue](https://github.com/xamarin/xamarin-android/issues/new).
For general Xamarin.Android experience issues, let us know via the
[Report a Problem](https://docs.microsoft.com/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017)
option found in your favorite IDE via **Help &gt; Report a Problem**.

<a name="oss" />

## Contributors

A big ***Thank You!*** to contributors who made improvements in this release:

  * [Ruben Buniatyan](https://github.com/rubo): 
    `AndroidClientHandler` was using commas rather than spaces in the HTTP
    `User-Agent` header.
    [GitHub PR 2017](https://github.com/xamarin/xamarin-android/pull/2071).

## OSS Core

Xamarin.Android 9.1 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-9) repo
* Android bindings and MSBuild tooling are in the [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-9) repo.
* Chat is in the [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).
