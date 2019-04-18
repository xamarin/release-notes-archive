---
id: 23E82B9C-09E5-428F-9AAB-196687FB6EBD
title: "Xamarin.Mac 3.99"
---

version:3.99.7
releasedate:2017-09-07


<div class="note">
	<b>Xcode9 based preview</b>
</div>

Requirements
============

- The latest features and API requires Xcode 9.0 beta 6 and the bundled macOS SDKs;
- Apple Xcode 9.0 requires a Mac running macOS 10.12 (Sierra) or newer;

Important Issues
==============

- Xamarin.Mac applications using the static registrar will fail to compile with Xcode 9 beta 4 due to a [broken AVFoundation header](http://www.openradar.me/radar?id=5033378961162240). This is default setting for Release builds. Passing --registrar:dynamic via "Additional MMP arguments" is the workaround until Apple fixes the header.
- Xamarin.Mac 32-bit applications (Unified or Classic) will crash on 10.13 beta 3. This is due to a bug in the GeoServices private framework and is [filed](http://www.openradar.me/radar?id=6183645291216896). This is fixed in 10.13 beta 4.

What's New
==========

This release is built upon our [open sourced SDK](https://github.com/xamarin/xamarin-macios),
using the `xcode9` branch, and is based on our upcoming [Xamarin.Mac 3.6 release](https://developer.xamarin.com/releases/mac/xamarin.mac_3/xamarin.mac_3.6/).

### macOS 10.13

The following new frameworks were added in macOS 10.13:

- CoreML.framework (Machine Learning)


### Xamarin.Mac 3.99.x (continuous builds)

All of our builds are also available for [download](https://jenkins.mono-project.com/view/Xamarin.MaciOS/job/xamarin-macios-builds-xcode9/) directly. A bit of warning, they come from our build bots and receive **no** QA. Verified builds will be made available as web preview during summer.

Our [Jenkins bots](https://jenkins.mono-project.com/job/xamarin-macios-pr-builder/) produce the **API diff** for every commit that is being built. Pick a build based on `xcode9` and look for the **API diff** link on the left column.

You can track the latest status of our API work on the [wiki](https://github.com/xamarin/xamarin-macios/wiki/xcode9-Bindings-Status).


### Xamarin.Mac 3.99.7

This eight preview is based on beta 6.
It adds new API for AVFoundation, IOSurface and Metal frameworks.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* CloudKit
* CoreAudio
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* GamePlayKit
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/api_changes/mac_3.6_to_3.99.7) contains a complete list of the API changes since the 3.6 release.


### Xamarin.Mac 3.99.6

This seventh preview is based on beta 6. It includes new bindings for CoreBluetooth, which has been greatly updated to reach parity with iOS in macOS 10.13.

Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* GamePlayKit
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/api_changes/mac_3.6_to_3.99.6) contains a complete list of the API changes since the 3.6 release.


### Xamarin.Mac 3.99.5

This sixth preview is based on beta 6.

Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* GamePlayKit
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.6_to_3.99.1.html) contains a complete list of the API changes since the 3.6 release.


### Xamarin.Mac 3.99.4

This fifth preview is based on beta 5. 

Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* GamePlayKit
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit _partially bound_
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.6_to_3.99.html) contains a complete list of the API changes since the 3.6 release.


### Xamarin.Mac 3.99.3

This fourth preview is based on beta 5. 
It adds new API for MediaPlayer and PDFKit and updates existing frameworks to beta 5 (unless noted below).

Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreData _up to beta 4_
* CoreFoundation
* CoreGraphics
* CoreImage _partially bound_
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* Foundation _partially bound_
* GamePlayKit
* Intents
* IOSurface
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* SceneKit
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.4_to_3.99.3.html) contains a complete list of the API changes since the 3.4 release.

### Xamarin.Mac 3.99.2

This third preview is based on beta 4.
Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AppKit
* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage
* CoreMedia
* CoreText
* CoreVideo
* ExternalAccessory
* Foundation _partially bound_
* GamePlayKit
* Intents
* MediaPlayer
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* PDFKit
* SceneKit
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.4_to_3.99.2.html) contains a complete list of the API changes since the 3.4 release.

### Xamarin.Mac 3.99.1

This second preview is based on beta 4.

Bindings for the following frameworks are still in progress and not _yet_ updated with the latest beta changes.

* AudioToolbox
* AVFoundation
* CloudKit
* CoreAudio
* CoreBluetooth
* CoreFoundation
* CoreGraphics
* CoreImage
* CoreMedia
* CoreML _updated to beta 3_
* CoreVideo
* CoreWLAN
* FinderSync _updated to beta 3_
* Foundation _partially bound_
* GamePlayKit
* ImageIO
* Intents
* IOSurface
* MediaPlayer
* Metal
* MetalKit
* MetalPerformanceShaders
* ModelIO
* NetworkExtension
* QuartzCore / CoreAnimation
* SafariServices
* SceneKit
* Security
* VideoToolbox

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.4_to_3.99.1.html) contains a complete list of the API changes since the 3.4 release.


### Xamarin.Mac 3.99.0

This first preview includes the new API for the following frameworks:

- Accounts updated to beta 3
- AVKit updated to beta 3
- Contacts updated to beta 3
- CoreAudioKit updated to beta 3
- CoreData updated to beta 3
- CoreLocation updated to beta 3
- Social updated to beta 3

#### API diff

The following [document](/releases/mac/xamarin.mac_3/api_changes/mac_3.4_to_3.99.html) contains a complete list of the API changes since the 3.4 release.

