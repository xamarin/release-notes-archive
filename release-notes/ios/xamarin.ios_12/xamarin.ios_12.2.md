---
id: ca54591e-f09d-4059-a60d-6a4a8c461202
title: "Xamarin.iOS 12.2"
---

# Xamarin.iOS 12.2
Last Update: 12/11/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

#### Requirements

* The latest features and APIs requires Xcode 10.1 and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 10.1 requires a Mac running OSX 10.13.6 (High Sierra) or newer

## What's New in this Release

### Release History

This version of Xamarin.iOS corresponds to our **15.9** (`d15-9`) milestone.

* December 11, 2018 - Xamarin.iOS 12.2.1.12
* November 28, 2018 - Xamarin.iOS 12.2.1.11
* November 7, 2018 - Xamarin.iOS 12.2.1.10
* October 24, 2018 - Xamarin.iOS 12.2.1.9
* October 2, 2018 - Xamarin.iOS 12.2.0.26
* September 11, 2018 - Xamarin.iOS 11.16.0.22
* August 21, 2018 - Xamarin.iOS 11.16.0.1

You can learn more about how we ship our releases in the [Visual Studio 2017 Release Rhythm](https://www.visualstudio.com/en-us/productinfo/vs2017-release-rhythm) document.

## December 11, 2018 - Xamarin.iOS 12.2.1.12

> This version is included in the Visual Studio 2017 version 15.9 SR4 release.

### Issues Fixed

[CVE-2018-8292 | Xamarin.iOS Information Disclosure Vulnerability](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2018-8292)

An information disclosure vulnerability exists in Xamarin.iOS when authentication information is inadvertently exposed in a redirect when the CFNetworkHandler for HttpClient are used. The NSUrlSessionHandler and the managed HttpMessageHandler are not affected.

An attacker who successfully exploited this vulnerability could use the information to further compromise the web application.

The security update addresses the vulnerability by correcting how Xamarin.iOS handles redirects.

## November 28, 2018 - Xamarin.iOS 12.2.1.11

> This version is included in the Visual Studio 2017 version 15.9 SR3 release.

### Issues Fixed

* [5158](https://github.com/xamarin/xamarin-macios/issues/5158) -  [bcl] Incomplete `System.Threading.Tasks.Extensions` Facade

## November 7, 2018 - Xamarin.iOS 12.2.1.10

> This version is included in the Visual Studio 2017 version 15.9 Preview 5 release.

This version includes support for Xcode 10.1.

## October 24, 2018 - Xamarin.iOS 12.2.1.9

> This version is included in the Visual Studio 2017 version 15.9 Preview 4 release.

### Issues Fixed

* [3766](https://github.com/xamarin/xamarin-macios/issues/3766) -  [tvOS] Fix SceneKit asset compilation
* [4810](https://github.com/xamarin/xamarin-macios/issues/4810) -  [watchOS] AppStore upload fails with an error "Binary uploaded is invalid"
* [4895](https://github.com/xamarin/xamarin-macios/issues/4895) -  [mtouch] Fix [InternalsVisibleTo] attribute parsing.


## October 2, 2018 - Xamarin.iOS 12.2.0.26

> This version is included in the Visual Studio 2017 version 15.9 Preview 3 release.

### Enhancements

* [684099](https://devdiv.visualstudio.com/DevDiv/_workitems/edit/684099) -  Include Xcode 10 support (SDK, API and tools) from Xamarin.iOS 12.0
* [4735](https://github.com/xamarin/xamarin-macios/issues/4735) -  [mtouch] Avoid warnings such as `ld: Warning: -read_only_relocs cannot be used with arm64`


## September 11, 2018 - Xamarin.iOS 11.16.0.22

> This version is included in the Visual Studio 2017 version 15.9 Preview 2 release.

### Enhancements

* [4133](https://github.com/xamarin/xamarin-macios/issues/4133) -  [foundation] Add more useful information inside `NSErrorException.Message` property
* [4308](https://github.com/xamarin/xamarin-macios/issues/4308) -  [open source] Fix resetting a README dependency when the hash exists, but the branch does not
* [4442](https://github.com/xamarin/xamarin-macios/issues/4442) -  [open source] Update `runtime.h` to fix build errors with Embeddinator 4000

### Issues Fixed

* [3724](https://github.com/xamarin/xamarin-macios/issues/3724) -  [debugger] Cannot step into the `NSUrlSessionHandler.cs` code
* [4130](https://github.com/xamarin/xamarin-macios/issues/4130) -  [runtime] Always release blocks on the main thread (crash in `WKWebView`)
* [4235](https://github.com/xamarin/xamarin-macios/issues/4235) -  [msbuild] Fix `error MT0099 : Internal error : Not all assemblies for Xamarin.Sdk have link tasks`
* [4237](https://github.com/xamarin/xamarin-macios/issues/4237) -  [msbuild] Fix `MT2002: Failed to resolve assembly: ...`
* [4254](https://github.com/xamarin/xamarin-macios/issues/4254) -  [objcruntime] `Class.GetHandle` not handle byref types (crash linked to becomeFirstResponder)
* [4384](https://github.com/xamarin/xamarin-macios/issues/4384) -  [mtouch] Fix `MissingMethodException` when mono 5.12 is used
* [4422](https://github.com/xamarin/xamarin-macios/issues/4422) -  [moutch] Fix `no type or protocol named 'MTKViewDelegate'` after adding `mtouch` argument `--registrar:static`
* [4467](https://github.com/xamarin/xamarin-macios/issues/4467) -  [msbuild] Fix build failures when a project contains '.ktx' file(s)
* [4594](https://github.com/xamarin/xamarin-macios/issues/4594) -  [mtouch] Ensure additional arguments are last (and can override msbuild arguments from response file)


### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 2018-04](https://github.com/mono/mono/commits/2018-04).

## August 21, 2018 - Xamarin.iOS 11.16.0.1

> This version is included in the Visual Studio 2017 version 15.9 Preview 1 release.

### Integrated Mono Features/Fixes

Xamarin.iOS uses a customized runtime and base class libraries (BCL) from [Mono 2018-02](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.10/).

## Known Issues

* [5129](https://github.com/xamarin/xamarin-macios/issues/5129) - Build error for library project with SceneKit asset.

    Library projects with SceneKit assets may fail to compile due to an
    MSBuild variable not being set:

        error MSB4044: The "CompileSceneKitAssets" task was not given a value for the required parameter "AppBundleDir".

    The workaround is to manually set the variable by adding the following
    line to the library project's .csproj file:

        <AppBundleDir>$(IntermediateOutputPath)MyAppName.app</AppBundleDir>

### 64 bits watchOS support

* Xcode 10 GM added support for 64 bits watch application, aka `arm64_32`. The current app store submission process **requires** this architecture to be included in your application when including watch support. You can workaround this with [https://github.com/xamarin/xamarin-macios/issues/4810#issuecomment-421338365](these instructions).

* Trying to run a watch app on the new Series 4 Apple Watch will fail with this error:

        IncorrectArchitecture: Failed to find matching arch for 32-bit Mach-O input file ...
        error MT1006: Could not install the application 'MyTestApp.app' on the device 'MyDevice': AMDeviceSecureInstallApplicationBundle returned: 0xe8000087 (kAMDIncorrectArchitectureError).

     This is because the S4 device can only execute native `arm64_32` code, not `armv7k` like previous watches.

     Please read https://github.com/xamarin/xamarin-macios/issues/4864 for more information and a workaround.

### Apple Breaking Changes

* [rdar://41123682]() Apple changed `TVElementUpdateType*` enum values. Please test your application if you're using this type.
* [rdar://43425168]() Apple changed `IN*WorkoutIntentResponseCode` enum values. Please test your application if you're using this type.

### Apple Non-Breaking Issues

* [rdar://41135211]() `RPBroadcastPickerView` symbol is not present in simulator. If needed you'll need to test this on devices.

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#Requirements)) is often possible, but some features may not be available. Also some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if APIs are missing. In most cases enabling the managed linker will help (by removing the API).
* Bitcode builds (for tvOS and watchOS) can fail submission to the App Store unless an Xcode 9.0+ toolchain is used.

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 12.1 stable release:

* [iOS](/releases/ios/api_changes/ios-12-1-0-12-2-1)
* [tvOS](/releases/ios/api_changes/tvos-12-1-0-12-2-1)
* [watchOS](/releases/ios/api_changes/watchos-12-1-0-12-2-1)

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/) and [Xamarin Mac/iOS Github Repository](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `d15-9`
* [mono](https://github.com/mono/mono/tree/2018-04) branch `2018-04`
