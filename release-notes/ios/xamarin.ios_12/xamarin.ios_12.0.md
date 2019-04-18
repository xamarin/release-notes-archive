---
id: ca54591e-f09d-4059-a60d-6a4a8c461200
title: "Xamarin.iOS 12.0"
---

# Xamarin.iOS 12.0
Last Update: 9/14/2018

[Getting Started](https://developer.xamarin.com/guides/ios/getting_started/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](#release-blog) | [Feedback](#feedback) | [Open Source](#open-source)

### Requirements

* The latest features and APIs require Xcode 10 GM and the bundled iOS, tvOS and watchOS SDKs
* Apple Xcode 10 requires a Mac running OSX 10.13.6 (High Sierra) or newer

## What's New in this Release

* [Support for Xcode 10](#Support_for_Xcode_10)
* [Support for iOS 12](#Support_for_iOS_12)
* [Support for tvOS 12](#Support_for_tvOS_12)
* [Support for watchOS 5](#Support_for_watchOS_5)
* [Other Changes](#Other_Changes)

### Support for Xcode 10

For more information you can consult the [Xcode 10](https://developer.apple.com/go/?id=xcode-10-beta-rn) release notes from Apple.

### Support for iOS 12

The following new frameworks were added in iOS 12:

* AuthenticationServices
* CarPlay
* IdentityLookup
* IdentityLookupUI
* NaturalLanguage
* Network

Most other frameworks were also updated, including ARKit 2.0 and Siri (Intents) shortcuts. See our [API diff](#API_Diff) to browse the newest API.

For more information you can consult the [iOS 12](https://developer.apple.com/go/?id=ios-12-beta-rn) release notes from Apple.

### Support for tvOS 12

The following new frameworks were added in tvOS 12:

* NaturalLanguage
* Network
* TVUIKit

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the newest API.

For more information you can consult the [tvOS 12](https://developer.apple.com/go/?id=tvos-12-sdk-rn) release notes from Apple.

### Support for watchOS 5

The following new frameworks were added in watchOS 5:

* NaturalLanguage

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the newest API.

For more information you can consult the [watchOS 5](https://developer.apple.com/go/?id=watchos-5-sdk-rn) release notes from Apple.

### Other Changes

The **GC pump thread** used on simulator builds is now **disabled** by default. This feature was added, a long time ago, to help diagnose object instances without managed references, where the GC could collect them and cause randomly occuring, hard to diagnose crashes. However it can cause [https://github.com/xamarin/xamarin-macios/issues/4772](issues) when debugging applications. Since several changes over the years made this option less useful it is now **disabled** and, if needed, can be re-enabled by adding  `--debugtrack:true` to the **mtouch additional arguments** of your project's options.

## Release History

This version of Xamarin.iOS correspond to our `xcode10` milestone and is based of the stable **15.8** release.

* September 19, 2018 - Xamarin.iOS 12.0.0.15
* September 11, 2018 - Xamarin.iOS 12.0.0.10

Earlier release notes, for Xamarin.iOS previews for Xcode 10 betas, are located in [Xamarin.iOS 11.99](releases/ios/xamarin.ios_11/xamarin.ios_11.99).

## September 19, 2018 - Xamarin.iOS 12.0.0.15

This release is based on the Xcode 10 final release.

### Issue Fixed

* [4818](https://github.com/xamarin/xamarin-macios/pull/4818) -  [clockkit] Add missing 'CLKComplicationFamily' enum values

## September 11, 2018 - Xamarin.iOS 12.0.0.10

This release is based on the Xcode 10 GM seed.

## Known Issues

### 64 bits watchOS support

* Xcode 10 GM added support for 64 bits watch application, aka `arm64_32`. The current app store submission process **requires** this architecture to be included in your application when including watch support. You can workaround this with [https://github.com/xamarin/xamarin-macios/issues/4810#issuecomment-421338365](these instructions).

* Trying to run a watch app on the new Series 4 Apple Watch will fail with this error:

        IncorrectArchitecture: Failed to find matching arch for 32-bit Mach-O input file ...
        error MT1006: Could not install the application 'MyTestApp.app' on the device 'MyDevice': AMDeviceSecureInstallApplicationBundle returned: 0xe8000087 (kAMDIncorrectArchitectureError).

     This is because the S4 device can only execute native `arm64_32` code, not `armv7k` like previous watches.

     Please read https://github.com/xamarin/xamarin-macios/issues/4864 for more information and a workaround.

### Apple Breaking Changes

* Apple **removed** support for `stdlibc++`. Using C++ code now requires the use of `libc++`.
* Apple **removed** support to build watchOS 1.x applications.
* [rdar://41123682]() Apple changed `TVElementUpdateType*` enum values. Please test your application if you're using this type.
* [rdar://43425168]() Apple changed `IN*WorkoutIntentResponseCode` enum values. Please test your application if you're using this type.

### Apple Non-Breaking Issues

* Apple **deprecated** OpenGLES and related API in favor of Metal.
* [rdar://41135211]() `RPBroadcastPickerView` symbol is not present in simulator. If needed you'll need to test this on devices.

### 32bits limitations

* Disabling the managed linker for device builds can generate object files that are too big for the 32bits native linker `ld` to process properly. The workaround is to enable the managed linker (e.g. **Link SDK**) on your projects.

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MT0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MT4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).

## API Diff

The following documents contains a complete list of the API changes since the Xamarin.iOS 11.14 stable release:

* [iOS](/releases/ios/api_changes/ios-11-14-0-12-0-0)
* [tvOS](/releases/ios/api_changes/tvos-11-14-0-12-0-0)
* [watchOS](/releases/ios/api_changes/watchos-11-14-0-12-0-0)

## Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.iOS Forums](https://forums.xamarin.com/categories/ios) and [Github Issues](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/ios) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.iOS is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode10`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
