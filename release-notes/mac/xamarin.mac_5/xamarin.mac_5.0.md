---
id: 4a11681a-125a-4c0b-a576-7ade8cbbc811
title: "Xamarin.Mac 5.0"
---

# Xamarin.Mac 5.0
Last Update: 9/27/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

This version of Xamarin.Mac corresponds to our xcode10 milestone. This is based on our stable d15-8 milestone, i.e. Xamarin.Mac 4.6.x.

### Requirements

* The latest features and APIs require Xcode 10 and the bundled macOS SDK
* Apple Xcode 10 requires a Mac running macOS 10.13.6 (High Sierra) or newer

## What's New in this Release

* [Support for Xcode 10]()
* [Support for macOS 10.14]()
* [Other Changes]()

### Support for Xcode 10

For more information you can consult the [Xcode 10](https://developer.apple.com/documentation/xcode_release_notes/xcode_10_release_notes) release notes from Apple.

### Support for macOS 10.14

The following new frameworks were added in macOS 10.14:

* NaturalLanguage
* Network

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the latest changes.

For more information you can consult the [macOS 10.14](https://developer.apple.com/documentation/macos_release_notes/macos_mojave_10_14_release_notes) release notes from Apple.

### Other Changes

* Apple is deprecating OpenGL and related API in favor of Metal;
* Apple **removed** support for `stdlibc++`. Using C++ code now requires the use of `libc++`.

## Release History

* October 1, 2018 - Xamarin.Mac 5.0.0.0

## October 1, 2018 - Xamarin.Mac 5.0.0.0

This is the first release based on the Xcode 10. It contains bindings to the new APIs introduced in macOS 10.14 and Xcode10.

### New frameworks

This includes the following frameworks

* Network ([sample](https://github.com/migueldeicaza/NetCatNetwork))
* iTunesLibrary

### New CoreImage filters

New CoreImage filters includes:

* `CIAreaMinMax`
* `CICameraCalibrationLensCorrection`
* `CICoreMLModelFilter`
* `CIDither`
* `CIGuidedFilter`
* `CIMeshGenerator`
* `CIMix`
* `CISaliencyMapFilter`
* `CISampleNearest`

## Known Issues

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MM0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MM4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).


## API Diff

The following documents contains a complete list of the API changes since our (4.4) stable release:

* [macOS](/releases/mac/api_changes/macos-4-6-0-5-0-0)

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [xamarin-macios Issue Tracker](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode10`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`
