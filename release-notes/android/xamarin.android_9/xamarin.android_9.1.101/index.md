---
id: 8B577D8E-D311-47F6-BA85-A623ECA5B834
title: "Xamarin.Android 9.1.101 (Preview)"
---

Last Update 2018-Dec-04

[System Requirements](https://docs.microsoft.com/xamarin/cross-platform/get-started/requirements)
| [What's New](#whats-new)
| [Blogs](https://blog.xamarin.com/tag/android/)
| [Open Source](#oss)

## Installing

* Visual Studio 2019 Preview 1 – [Visual Studio Installer](https://www.visualstudio.com/vs/preview/)
* Visual Studio 2019 for Mac Preview 1 – [Visual Studio 2019 for Mac Preview Installer](https://www.visualstudio.com/vs/preview/) with the **Xamarin Preview** [updater channel](https://docs.microsoft.com/visualstudio/mac/update)

Additional information for the Visual Studio 2019 for Mac Preview: After
downloading and running the Visual Studio 2019 for Mac Preview installer,
launch the new Visual Studio 2019 for Mac Preview app and switch the [updater
channel](https://docs.microsoft.com/visualstudio/mac/update) to **Xamarin
Preview** to try the new Xamarin.Android preview version.  Note that this will
also change the Xamarin.Android and Xamarin.iOS versions used by any existing
Visual Studio 2017 for Mac installation.

<a name="whats-new" />

## What's New in this Release

  * [Build and Deployment Performance Improvements](#build-performance)
  * [App Performance Improvements](#app-performance)
  * [Preliminary Support for `android:extractNativeLibs="false"`](#unextracted-native-libs)
  * [Removal of armeabi Support](#armeabi-removal)

<a name="build-performance" />

### Build and Deployment Performance Improvements

This release includes several more improvements to build and deployment times.

  * [GitHub PR 2088](https://github.com/xamarin/xamarin-android/pull/2088):
    Adjust the `_CopyIntermediateAssemblies` target to replace a couple uses of
    the `Copy` task with `CopyIfChanged` and avoid calling the `Touch` task.
    This improved the incremental build time for a test project from roughly 7
    seconds to roughly 6.5 seconds.
  * [GitHub PR 2124](https://github.com/xamarin/xamarin-android/pull/2124):
    Add conditions and correct item wildcards for the `_CreateAapt2VersionCache`
    target to improve build times in projects [configured to use AAPT2][aapt2].
  * [GitHub PR 2129](https://github.com/xamarin/xamarin-android/pull/2129):
    Split part of the `ConvertResourcesCases` task into a new
    `ConvertCustomView` task to avoid repeating work later in the build.  This
    saves roughly half the time spent in the `ConvertResourcesCases` task, which
    can be several seconds or more for an initial clean build.
  * [GitHub PR 2148](https://github.com/xamarin/xamarin-android/pull/2148):
    Properly dispose `AssemblyDefinition` instances during the `BuildApk` task.
    This improved the overall build time for a test project by about 5%.
  * [GitHub PR 2162](https://github.com/xamarin/xamarin-android/pull/2162):
    Move the `StripEmbeddedLibraries` task to be a linker step to save one pass
    of loading the assemblies for writing and to avoid redundant work on
    assemblies that the linker would skip.  This improved the combined time of
    stripping and linking for a test project in the Release configuration from
    16.1 seconds to 15.4 seconds.
  * [GitHub PR 2168](https://github.com/xamarin/xamarin-android/pull/2168):
    Remove some redundant work the `ResolveAssemblies` build task was doing when
    iterating through assembly metadata.
  * [GitHub PR 2174](https://github.com/xamarin/xamarin-android/pull/2174):
    Combine the `CheckTargetFrameworks` task into the `ResolveAssemblies` task
    to save one pass of reading through assembly metadata.

[aapt2]: https://developer.xamarin.com/releases/android/xamarin.android_9/xamarin.android_9.0/#aapt2

See also:

  * The [Build Performance Results][performance-wiki] page on the project wiki
    for additional comparisons and updates about the on-going work to continue
    to improve performance.
  * The [latest numbers][continuous-performance] from the continuous integration
    builds.

[performance-wiki]: https://github.com/xamarin/xamarin-android/wiki/Build-Performance-Results
[continuous-performance]: https://jenkins.xamarin.com/view/Xamarin.Android/job/xamarin-android/plot/Build%20times/

<a name="app-performance" />

### App Performance Improvements

  * [GitHub PR 1886](https://github.com/xamarin/xamarin-android/pull/1886),
    [GitHub PR 2147](https://github.com/xamarin/xamarin-android/pull/2147):
    Avoid unnecessary string allocations during app startup.
  * [GitHub PR 2008](https://github.com/xamarin/xamarin-android/pull/2008),
    [GitHub PR 2126](https://github.com/xamarin/xamarin-android/pull/2126):
    Use a faster approach to register managed methods with the Android runtime
    during app startup.
  * [GitHub PR 2025](https://github.com/xamarin/xamarin-android/pull/2025):
    Slightly reduce the overhead of setting up managed method overrides and
    callback methods for types in or subclassed from Java bindings.

<a name="unextracted-native-libs" />

### Preliminary Support for `android:extractNativeLibs="false"`

Android 6.0 (API level 23) introduced a new way to handle native shared
libraries that are packaged as part of APKs.  Before that API level, the
libraries would always be extracted and placed in the application data
directory, consuming extra space on the file system.  API level 23 added a new
manifest [`<application>`][application-element] element attribute
`android:extractNativeLibs` to control whether the native libraries are
extracted during installation.  If the attribute is set to `false`, then Android
6.0 and higher will skip the extraction step and attempt to load the libraries
directly from the APK instead.

Xamarin.Android 9.1.101 adds preliminary compatibility support for this
functionality.  At the moment, enabling this mode requires a few manual steps:

  * Add the `android:extractNativeLibs="false"` attribute to the `<application>`
    element in the *Properties\\AndroidManifest.xml* file

  * Set the `$(AndroidStoreUncompressedFileExtensions)` MSBuild property to
    `.so` in your *.csproj* file:

    ```xml
    <PropertyGroup>
        <AndroidStoreUncompressedFileExtensions>.so</AndroidStoreUncompressedFileExtensions>
    </PropertyGroup>
    ```

  * Add an [android environment file][environment-file]
    to the project with the following contents:

    ```
    __XA_DSO_IN_APK=1
    ```

[application-element]: https://developer.android.com/guide/topics/manifest/application-element
[environment-file]: https://docs.microsoft.com/xamarin/android/deploy-test/building-apps/build-process#androidenvironment

<a name="armeabi-removal" />

### Removal of armeabi Support

Due to the [removal of armeabi support in Android NDK r17][ndk-guide],
Xamarin.Android 9.1.101 no longer supports the armeabi architecture.  Projects
that have this old ABI selected in the `$(AndroidSupportedAbis)` MSBuild
property will now need to remove it.  The newer armeabi-v7a ABI should be used
instead.  The `$(AndroidSupportedAbis)` setting can be found in the **Advanced**
section of the **Android Options** project properties in Visual Studio and the
**Android Build** project properties in Visual Studio for Mac.

[ndk-guide]: https://developer.android.com/ndk/guides/abis

## Release History

  * [December 04, 2018](#9-1-101-6) - Xamarin.Android 9.1.101.6

<a name="9-1-101-6" />

## December 04, 2018 - Xamarin.Android 9.1.101.6

> This version is included in the Visual Studio 2019 Preview 1 and Visual
> Studio 2019 for Mac Preview 1 releases.

### Issues Fixed

  * [GitHub 1615](https://github.com/xamarin/xamarin-android/issues/1615):
    `AndroidClientHandler` did not provide TLS 1.1 or TLS 1.2 support on Android
    versions 4.1 to 4.4.
  * [GitHub 2029](https://github.com/xamarin/xamarin-android/issues/2029),
    [GitHub 2218](https://github.com/xamarin/xamarin-android/issues/2218):
    Build errors could potentially occur in projects [configured to use
    AAPT2][aapt2] if they also referenced NuGet packages that provided custom
    values for `$(AndroidResgenExtraArgs)`.
  * [GitHub PR 2108](https://github.com/xamarin/xamarin-android/pull/2108):
    The built-in list of types, methods, and fields to preserve when linking
    *mscorlib* included some redundant and outdated items.
  * [GitHub PR 2117](https://github.com/xamarin/xamarin-android/pull/2117):
    A few build tasks were generating warnings or errors that did not include
    numbered codes.
  * [GitHub 2141](https://github.com/xamarin/xamarin-android/issues/2141):
    App deployment could fail due to an "INSTALL\_FAILED\_CONFLICTING\_PROVIDER"
    error when using certain recent Android libraries such as Crashlytics that
    contain their own *AndroidManifest.xml* file.
  * [GitHub 2143](https://github.com/xamarin/xamarin-android/issues/2143):
    The `Desugar` build task did not pass the `--classpath_entry` option to
    `desugar_deploy.jar`, resulting in build errors about missing types when
    desugaring certain *.jar* files.
  * [GitHub PR 2150](https://github.com/xamarin/xamarin-android/pull/2150):
    The `ConvertResourcesCases` and `CopyAndConvertResources` build tasks
    contained redundant try/catch blocks.
  * [GitHub PR 2187](https://github.com/xamarin/xamarin-android/pull/2187):
    The `CompileToDalvik` build task was passing individual input item names on
    the command line to `dx.jar` instead of combining the names into a file and
    using the `--input-list` option.  This could potentially cause issues with
    command line length limitations in cases where many inputs were given.
  * [GitHub 2193](https://github.com/xamarin/xamarin-android/issues/2193):
    Building, adding a new view to a *.axml* layout file, and then deploying an
    application could lead to an "Android.Views.InflateException... Attempt to
    invoke virtual method on a null object reference" error when running the app
    because the layout file updates were not deployed as expected.
  * [GitHub 2200](https://github.com/xamarin/xamarin-android/issues/2200):
    Builds could hit a new error in Xamarin.Android 9.1 instead of automatically
    using the default detected location as expected in projects that had a
    nonexistent custom path explicitly set in the `$(AndroidSdkDirectory)`
    MSBuild property.

### Integrated Mono Features/Fixes

This version of Xamarin.Android currently uses
[Mono 5.14](http://www.mono-project.com/docs/about-mono/releases/5.14.0/)
[Commit 969357ac](https://github.com/mono/mono/commit/969357ac02b2c08a43ef89d98aca550d3648bf00).
The embedded Mono version will be updated in the next Xamarin.Android version
9.1.101 preview.

### Known Issues

Due to source branching strategy, this first Xamarin.Android 9.1.101 preview
does not yet include the fix for the following issue:

  * [GitHub 2205](https://github.com/xamarin/xamarin-android/issues/2205):
    Android resource conflicts can occur after rebuilds in projects referencing
    the Xamarin.GooglePlayServices.Basement NuGet package if the projects
    include a *google-services.json* file and are [configured to use
    AAPT2][aapt2].

## Feedback

Your feedback is important to us.  If there are any problems with this release, check our
[GitHub Issues](https://github.com/xamarin/xamarin-android/issues),
[Xamarin.Android Community Forums](https://forums.xamarin.com/categories/android) and
[Visual Studio Developer Community](https://developercommunity.visualstudio.com/)
for existing issues.  For new issues within the Xamarin.Android SDK, please report a
[GitHub Issue](https://github.com/xamarin/xamarin-android/issues/new).
For general Xamarin.Android experience issues, let us know via the
[Report a Problem](https://docs.microsoft.com/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017)
option found in your favorite IDE under **Help &gt; Report a Problem**.

<a name="oss" />

## Contributors

A big ***Thank You!*** to contributors who made improvements in this release:

  * [Tim Wanders](https://github.com/tim241):
    Tidy up the *Makefile* used to build Xamarin.Android from source on macOS
    and Linux.
    [GitHub PR 1870](https://github.com/xamarin/xamarin-android/pull/1870).
  * [Tim Wanders](https://github.com/tim241):
    Improve compatibility for building Xamarin.Android from source on Arch
    Linux.
    [GitHub PR 1871](https://github.com/xamarin/xamarin-android/pull/1871).
  * [eric liu](https://github.com/erikpowa):
    Adjust the `Desugar` build task to pass the `--classpath_entry` option to
    `desugar_deploy.jar`.
    [GitHub PR 2158](https://github.com/xamarin/xamarin-android/pull/2158)

## OSS Core

Xamarin.Android 9.1.101 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d16-0-p1) repo
* Android bindings and MSBuild tooling are in the [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d16-0-p1) repo.
* Chat is in the [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).
