---
id: e31b34b7-d899-4582-a73b-3a317f0234e7
title: "Xamarin.Mac 4.99"
---

# Xamarin.Mac 4.99
Last Update: 8/23/2018

[System Requirements](https://developer.xamarin.com/guides/cross-platform/getting_started/requirements/) | [What's New](#whats-new-in-this-release) | [Known Issues](#known-issues) | [Blogs](https://blog.xamarin.com/tag/ios/) | [Open Source](#open-source)

This version of Xamarin.Mac corresponds to our xcode10 milestone. This is presently based on our stable d15-7 milestone, i.e. Xamarin.Mac 4.4.x.

### Requirements

* The latest features and APIs require Xcode 10 beta 5 and the bundled macOS SDK
* Apple Xcode 10 requires a Mac running macOS 10.13.4 (High Sierra) or newer

## What's New in this Release

* [Support for Xcode 10]()
* [Support for macOS 10.14]()
* [Other Changes]()

### Support for Xcode 10

For more information you can consult the [Xcode 10](https://developer.apple.com/go/?id=xcode-10-beta-rn) release notes from Apple.

### Support for macOS 10.14

The following new frameworks were added in macOS 10.14:

* NaturalLanguage
* Network

Most other frameworks were also updated. See our [API diff](#API_Diff) to browse the latest changes.

For more information you can consult the [macOS 10.14](https://developer.apple.com/go/?id=macos-10.14-beta-rn) release notes from Apple.

### Other Changes

* Apple is deprecating OpenGL and related API in favor of Metal;
* Apple **removed** support for `stdlibc++`. Using C++ code now requires the use of `libc++`.

## Release History

This version of Xamarin.Mac correspond to our `xcode10` milestone and is based of the stable **15.8** release. Earlier versions (4.99.0-2) were based on our older **15.7** releases.

* August 23, 2018 - Xamarin.Mac 4.99.3.658
* August 6, 2018 - Xamarin.Mac 4.99.2.250
* July 4, 2018 - Xamarin.Mac 4.99.1.164
* June 27, 2018 - Xamarin.Mac 4.99.0.93

## August 23, 2018 - Xamarin.Mac 4.99.3.658

This fourth preview is based on Xcode 10 beta 6.

### New frameworks

This preview includes the following new frameworks

* Network ([sample](https://github.com/migueldeicaza/NetCatNetwork))
* iTunesLibrary

### Updated frameworks

This preview includes the following updates to existing frameworks

* Shared frameworks: CoreServices, Metal

Other frameworks, except MetalPerformanceShaders, were updated with changes up to beta 6.

## August 6, 2018 - Xamarin.Mac 4.99.2.250

This third preview is based on Xcode 10 beta 5.

### New CoreImage filters

New CoreImage filters include:

* `CISaliencyMapFilter`

### Updated frameworks

This preview includes the following updates to existing frameworks (all API updated to beta 5)

* AppKit, AVFAudio, AVFoundation, AudioToolbox, Contacts, CoreGraphics, CoreImage, CoreMedia, CoreML, FinderSync, Foundation, MediaPlayer, ModelIO, OpenGL, Photos, QuartzComposer, Scenekit, Storekit, UserNotifications, Vision, WebKit

## July 4, 2018 - Xamarin.Mac 4.99.1.164

This second preview is based on Xcode 10 beta 3 and includes the new AppKit bindings.

### New CoreImage filters

New CoreImage filters includes:

* `CICameraCalibrationLensCorrection`
* `CICoreMLModelFilter`

## June 27, 2018 - Xamarin.Mac 4.99.0.93

This is the first preview of Xcode 10 support. It will work correctly with the current stable Visual Studio for Mac (7.5).

### New CoreImage filters

New CoreImage filters includes:

* `CIAreaMinMax`
* `CIDither`
* `CIGuidedFilter`
* `CIMeshGenerator`
* `CIMix`
* `CISampleNearest`

### Updated frameworks

This preview includes the following updates to existing frameworks (all API updated to beta 2)

Accounts, AVFoundation, AVKit, Contacts, CoreVideo, GameplayKit, MapKit, SceneKit, SpriteKit, VideoToolbox

## Known Issues

* [4436](https://github.com/xamarin/xamarin-macios/issues/4436) - Metal Game Template app fails to build with MSB6003

### Using an older Xcode version

Using an older Xcode version (than the one mentioned in the above [requirements](#requirements)) is often possible, but some features may not be available. Also, some limitations might require workarounds, e.g.:

* The static registrar requires Xcode headers files to build applications, leading to [`MM0091`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT0091) or [`MM4109`](https://developer.xamarin.com/guides/ios/troubleshooting/mtouch-errors/#MT4109) errors if API are missing. In most cases enabling the managed linker will help (by removing the API).


## API Diff

The following documents contains a complete list of the API changes since our (4.4) stable release:

* [macOS](/releases/mac/api_changes/macos-4-4-99-4-99-3)

### Integrated Mono Features/Fixes

Xamarin.Mac uses a customized runtime and base class libraries (BCL) from [Mono](https://github.com/mono/mono/commits/2018-02).

Additional information can be found in Mono [release notes](http://www.mono-project.com/docs/about-mono/releases/5.x/).

### Feedback

Your feedback is important to us. If there are any problems with this release, check the [Xamarin.Mac Forums](https://forums.xamarin.com/categories/mac) and [xamarin-macios Issue Tracker](https://github.com/xamarin/xamarin-macios/issues) for existing issues. If you do not find any matching issue, please feel free to [start a new discussion](https://forums.xamarin.com/post/discussion/mac) and [report an issue](https://github.com/xamarin/xamarin-macios/issues/new).

## Open Source

Xamarin.Mac is based on the following open-source repositories:

* [xamarin-macios](https://github.com/xamarin/xamarin-macios) branch `xcode10`
* [mono](https://github.com/mono/mono/tree/2018-02) branch `2018-02`

### A big Thank You! to the following folks that helped to make Xamarin.iOS and Xamarin.Mac even better:

* [@equinox2k](https://github.com/equinox2k)
