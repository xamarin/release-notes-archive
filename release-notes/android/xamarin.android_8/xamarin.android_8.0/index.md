---
id: BE4C707F-397A-4E6B-AC0F-34DC8AA3E4B2
title: "Xamarin.Android 8.0"
---

Last Update: 10/31/2017

<a class="action-button" href="https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/">System Requirements</a><a class="action-button" href="#whats-new">What's New</a><a class="action-button" href="#known-issues">Known Issues</a><a class="action-button" href="https://blog.xamarin.com/tag/android/">Blogs</a><a class="action-button" href="#oss">Open Source</a>

### Installing

* Visual Studio 2017 – [Visual Studio Installer](https://docs.microsoft.com/visualstudio/install/update-visual-studio)
* Visual Studio 2017 for Mac – [Stable updater channel](https://docs.microsoft.com/visualstudio/mac/update)
* Visual Studio 2015 Tools for Xamarin – [Stable updater channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/#visualstudio)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Android Forums](https://forums.xamarin.com/categories/android) and [Xamarin Bugzilla Tracker](https://bugzilla.xamarin.com/query.cgi) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/android) and [report an issue](https://bugzilla.xamarin.com/enter_bug.cgi?product=Android).

### Release History

* [October 31st, 2017](#8-0-2-1) - Xamarin.Android 8.0.2.1
* [October 9th, 2017](#8-0-0-33) - Xamarin.Android 8.0.0.33

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

<a name="8-0-2-1" />

## October 31st, 2017 - Xamarin.Android 8.0.2.1

> This version is included in the Visual Studio 2017 version 15.4.2 release.

### Issues Fixed

* [59822](https://bugzilla.xamarin.com/show_bug.cgi?id=59822):
    Building an Android solution in Release mode that references a net standard project with a Microsoft.Identity reference results in a linker error.
* [60069](https://bugzilla.xamarin.com/show_bug.cgi?id=60069):
    Build.getSerial is not bound in Android API 26, causes conflict with Build.Serial, which is now deprecated
* [60080](https://bugzilla.xamarin.com/show_bug.cgi?id=60080):
    After upgrading to latest Xamarin- Visual Studio stuck/hangs at initialization of xamarin.andorid project while loading projects

<a name="8-0-0-33" />

## October 9th, 2017 - Xamarin.Android 8.0.0.33

> This version is included in the Visual Studio 2017 version 15.4 release.

### Issues Fixed

* [30147](https://bugzilla.xamarin.com/show_bug.cgi?id=30147):
    Path is too long
* [30909](https://bugzilla.xamarin.com/show_bug.cgi?id=30909):
    AssetManager.AssetInputStream is missing in Mono.Android.dll
* [36485](https://bugzilla.xamarin.com/show_bug.cgi?id=36485):
    Uninformative &quot;&quot;aapt.exe&quot; exited with code 1.&quot; and &quot;The file &quot;obj\Debug\android\bin\packaged_resources&quot; does not exist&quot; errors if drawable resource filename contains invalid character
* [51507](https://bugzilla.xamarin.com/show_bug.cgi?id=51507):
    Give a proper warning when JDK 1.8 is required but not installed
* [55473](https://bugzilla.xamarin.com/show_bug.cgi?id=55473):
    Incorrect generated enum for OnServiceAdded in BluetoothGattServerCallback
* [55477](https://bugzilla.xamarin.com/show_bug.cgi?id=55477):
    Stream Closed Exception thrown in AndroidClientHandler during redirected HTTP POST call.
* [55561](https://bugzilla.xamarin.com/show_bug.cgi?id=55561):
    "Processing" messages spam Android build output 
* [56311](https://bugzilla.xamarin.com/show_bug.cgi?id=56311):
    Intellisense breaks on ":" in axml files
* [56436](https://bugzilla.xamarin.com/show_bug.cgi?id=56436):
    BINDINGSGENERATOR:  warning BG8C00: For type Java.Util.IList, base interface Java.Util.ICollection does not exist.
* [56655](https://bugzilla.xamarin.com/show_bug.cgi?id=56655):
    Debugging on a new device doesn't deploy
* [56740](https://bugzilla.xamarin.com/show_bug.cgi?id=56740):
    Nexus 6p Android O Preview: Couldn't connect to logcat, GetProcessId returned: 0
* [56867](https://bugzilla.xamarin.com/show_bug.cgi?id=56867):
    [VS 2017 XA Self Hosted VSIX] Xamarin.Android version is not displayed in "help > About Microsoft Visual studio"
* [57279](https://bugzilla.xamarin.com/show_bug.cgi?id=57279):
    Sample for Microsoft Intune is failing - System.NullReferenceException at IntuneMAMSampleAndroid.EntryActivity.OnCreate
* [57281](https://bugzilla.xamarin.com/show_bug.cgi?id=57281):
    XAML IntelliSense only works when iOS target is set, not Android
* [57645](https://bugzilla.xamarin.com/show_bug.cgi?id=57645):
    &quot;The &quot;LinkAssemblies&quot; task failed unexpectedly&quot; due to a NullReferenceException in Mono.Linker's `ProcessLibrary()` method when project references certain assemblies, for example &quot;Mono.Data.Sqlite.Portable&quot; NuGet package
* [58029](https://bugzilla.xamarin.com/show_bug.cgi?id=58029):
    With NDK r12b+ AOT is successfull but JIT still happens and app as slow as w/o AOT
* [58169](https://bugzilla.xamarin.com/show_bug.cgi?id=58169):
    _UpdateAndroidResgen constantly being called
* [58178](https://bugzilla.xamarin.com/show_bug.cgi?id=58178):
    macOS installer on High Sierra will fail if javac is not available
* [58303](https://bugzilla.xamarin.com/show_bug.cgi?id=58303):
    Java.Util.HashMap is mapped to Android.Runtime.JavaDictionary in binding generator
* [58405](https://bugzilla.xamarin.com/show_bug.cgi?id=58405):
    Bundle getIntegerArrayList &amp; getStringArrayList throw InvalidCastException if Bundle.get is called first
* [58448](https://bugzilla.xamarin.com/show_bug.cgi?id=58448):
    IDE0006 warning on File -> New CrossPlatform App
* [58646](https://bugzilla.xamarin.com/show_bug.cgi?id=58646):
    _CleanGeneratedDebuggingFiles target removes ALL .pdbs
* [58711](https://bugzilla.xamarin.com/show_bug.cgi?id=58711):
    Linker fails randomly when processing a specific set dependencies
* [58829](https://bugzilla.xamarin.com/show_bug.cgi?id=58829):
    Application Output Window being flooded with "[Mono] worker parking, [Mono] worker unparking" messages when debugging agasint Android Emulator.
* [59036](https://bugzilla.xamarin.com/show_bug.cgi?id=59036):
    Multidex.keep file missing newlines
* [59532](https://bugzilla.xamarin.com/show_bug.cgi?id=59532):
    [API 26] Android.App.Assist.AssistStructure AutofillType/InputType Mapped Backwards
* [59655](https://bugzilla.xamarin.com/show_bug.cgi?id=59655):
    Android.Views.ViewStructure.SetAutofillType should accept enum type 'AutoFillType' over int
    
### Breaking Changes

* [51293](https://bugzilla.xamarin.com/show_bug.cgi?id=51293):
    ScanResult.txPowerLevel should return int 
    
<a name="integrated-mono" />

### Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 5.2](http://www.mono-project.com/docs/about-mono/releases/5.2.0/)
[commit 143421cb](https://github.com/mono/mono/commit/143421cb45f738defbfbcd477e96b8c58222eb37).

* [57744](https://bugzilla.xamarin.com/show_bug.cgi?id=57744):
    ReflectionTypeLoadException.LoaderExceptions has null exceptions / [reflection] Convert correct MonoError to an exn in Assembly.GetTypes ()

<a name="whats-new"/>

## What's New in this Release

* [Android Oreo](#oreo)
* [.NET Standard 2.0](#netstandard)
* [Shorter Internal Path Names](#shorterinternalpathnames)

<a name="oreo" />

### Android Oreo Support

Xamarin.Android 8.0 brings binding support for Android Oreo. See our documentation for more information on Android Oreo:

[https://developer.xamarin.com/guides/android/platform_features/introduction-to-oreo/](https://developer.xamarin.com/guides/android/platform_features/introduction-to-oreo/)

<a name="netstandard" />

### .NET Standard 2.0 Support

Xamarin.Android 8.0 is the first version to support .NET Standard 2.0.

[https://docs.microsoft.com/dotnet/standard/net-standard](https://docs.microsoft.com/dotnet/standard/net-standard)

<a name="shorterinternalpathnames" />

### Shorter Internal Path Names (Experimental)

Many generated path names in a Xamarin.Android project can be quite long, which on Windows may result in a `PathPathTooLongException`:

```
C:\Some\Directory\Solution\Project\obj\Debug\__library_projects__\Xamarin.Forms.Platform.Android\library_project_imports\assets
```

Xamarin.Android 8.0 introduces a new `$(UseShortFileNames)` MSBuild property. When `True` (the default is `False`), shorter path names will be used, which will hopefully reduce the likelihood of a `PathPathTooLongException`:

```
C:\Some\Directory\Solution\Project\obj\Debug\lp\1\jl\assets
```

<a name="known-issues" />

## Known Issues

### Stable Binding for Android API-26

A stable binding for Android API-26 is distributed in this release and is considered final. Future changes to this binding will be considered a breaking change.

## API Changes

* API Level 10:
    [Mono.Android.dll](level_10_diff/mono.android.dll),
    [OpenTK.dll](level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](level_10_diff/opentk-1.0.dll)
* API Level 15:
    [Mono.Android.dll](level_15_diff/mono.android.dll)
* API Level 16:
    [Mono.Android.dll](level_16_diff/mono.android.dll)
* API Level 17:
    [Mono.Android.dll](level_17_diff/mono.android.dll)
* API Level 18:
    [Mono.Android.dll](level_18_diff/mono.android.dll)
* API Level 19:
    [Mono.Android.dll](level_19_diff/mono.android.dll)
* API Level 20:
    [Mono.Android.dll](level_20_diff/mono.android.dll)
* API Level 21:
    [Mono.Android.dll](level_21_diff/mono.android.dll)
* API Level 22:
    [Mono.Android.dll](level_22_diff/mono.android.dll)
* API Level 23:
    [Mono.Android.dll](level_23_diff/mono.android.dll)
* API Level 24:
    [Mono.Android.dll](level_24_diff/mono.android.dll)
* API Level 25:
    [Mono.Android.dll](level_25_diff/mono.android.dll)
* API Level 26:
    [Mono.Android.dll](level_26_diff/mono.android.dll)

<a name="oss" />
    
## OSS Core

Xamarin.Android 8.0 is based on the open-source Xamarin.Android repositories:

* Core JNI interaction logic is in the
    [Java.Interop](https://github.com/xamarin/Java.Interop/tree/d15-4) repo
* Android bindings and MSBuild tooling are in the
    [xamarin-android](https://github.com/xamarin/xamarin-android/tree/d15-4) repo.
* Chat is in the
    [`xamarin/xamarin-android` Gitter channel](https://gitter.im/xamarin/xamarin-android).

