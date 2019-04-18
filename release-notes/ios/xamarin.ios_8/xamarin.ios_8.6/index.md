---
id: D6035302-1161-4EA8-911B-2C6332B6A0BB
title: "Xamarin.iOS 8.6"
---

# Xamarin.iOS 8.6

Xamarin.iOS 8.6 is our first release to **fully support** the new **unified** API that allows fat 32/64 bits applications to be built
	from the same source/project files.



Additional IDE support comes from the [new Xamarin Studio (5.7)](../../../studio/xamarin.studio_5.7/xamarin.studio_5.7)


	and [updated (3.9) VS support](../../../vs/xamarin.vs_3/xamarin.vs_3.9)

.The following document contains a list of the API changes from [API changes from 8.4 to 8.6](/releases/ios/api_changes/from_8.4.0_to_8.6.0).

## Major features

-  The new  ** [32/64 bits unified API ](http://developer.xamarin.com/guides/cross-platform/macios/unified/)** is now stable and supported; 
-  Mono runtime/BCL updated to  [3.12](http://www.mono-project.com/docs/about-mono/releases/3.12.0/) ; 
-  F# updated to  [3.1.1.27](https://github.com/fsharp/fsharp/blob/3.1.1.27/CHANGES.txt) 


## Unified API

Over the last year Xamarin invested a lot of time and energy to 
	producing the new **unified API** and our [main document](“http://developer.xamarin.com/guides/cross-platform/macios/unified/)
	on the subject has been updated with the latest information.

Note that building **classic** API application is still supported 
	by Xamarin.iOS. However [starting February 1st, 2015 Apple will require that all new iOS submissions to the App Store must include 64-bits support and be built using the iOS8 SDK (part of Xcode 6) or a later, stable release](https://developer.apple.com/news/?id=10202014a).
	To create such a fat application, including both 32bits and 64bits 
	slices, you’ll need to update your application to use the new 
	Xamarin.iOS **unified** API.

For references a list of the changes, minus namespaces, between our [ **classic**and  **unified**](/releases/ios/api_changes/classic-vs-unified-8.6.0) API is available.

 <a name="3"></a>


#  [Xamarin.iOS 8.6.3](#3)

Xamarin.iOS 8.6.3 is a security update including important fixes for
	vulnerabilities and stability in the SSL/TLS networking stack. 
	There is no API change in this release.

## Bug fixes

-  [ssl/tls] Additional state validation for handshake (SKIP-TLS vulnerability) for both client/server code
-  [ssl/tls] Removal of _EXPORT_ ciphers (FREAK vulnerability) for both client/server code
-  [ssl/tls] Removal of SSLv2 fallback (client side only, it was never supported on the server side)
-  [ssl/tls] Prevent crashes when a SSL/TLS connection is closed [#19334]


 <a name="2"></a>


#  [Xamarin.iOS 8.6.2](#2)

Xamarin.iOS 8.6.2 is a service release. The following document contains a
	list of the [API changes from 8.6.1 to 8.6.2](/releases/ios/api_changes/from_8.6.1_to_8.6.2)

## Enhancements

-  [msbuild] Faster DetectCodeSigningIdenty when several several provisioning profiles are available


## Bug fixes

-  [audiotoolbox] Fix AudioConverter memory corruption [#21940]
-  [foundation] Fix unable to cast object of type NSUrlSessionTask to NSUrlSessionUploadTask [#24961]
-  [x86_64] Fix double to int conversion (some cases were different from MS.NET) [#26219]
-  [linker] Bad optimization that could remove finally clause in bindings on ARM64 [#26256]
-  [uikit] Fix UIAppearance proxy class creation on ARM64 [#26353]
-  [arm64] Fix the loading of i1/i2/i4 arguments passed on the stack into registers [#26506]
-  [aot] Fix compile time assertion (liveness.c:637) on ARM64 [#26732]
-  [arm64] Fix float structs getting aligned to 8 bytes [#26900]
-  [registrar] Add support for arrays of INativeObjects to the static registrar [#26927]
-  [arm64] Fix NullReferenceException when using Rx on ARM64 [#26961]
-  [arm64] Remove dependence on private symbol _NSGetEnviron [#27456]


 <a name="1"></a>


#  [Xamarin.iOS 8.6.1](#1)

Xamarin.iOS 8.6.1 is a service release. The following document contains a 
	list of the [API changes from 8.6.0 to 8.6.1](/releases/ios/api_changes/from_8.6.0_to_8.6.1)

## Enhancements

-  [fsharp] Several constructors for native types are now public to ease their usage in F#


## Bug fixes

-  [arm64] LLVM fix for reserved registers [#23885]
-  [msbuild] Some (storyboads/images) files might be missing from the app bundle [#25569][#26015][#26134][#26137]
-  [runtime] Fix for custom marshaler [#25891]
-  [x86_64] UIView.PointInside parameters bug on simulator only [#26002]
-  [arm64] Fix passing of vtypebyref arguments in gsharedvt trampolines [#26184]


 <a name="0"></a>


#  [Xamarin.iOS 8.6.0](#0)

## Enhancements

-  [assetslibrary] Add parameters for ALAssetsLibrary.ChangedNotification
-  [coreanimation] Add CAAnimation.AnimationEvents property [#23803]
-  [coreanimation] SceneKit additions are available on iOS8 [#23820]
-  [corebluetooth] Add missing 'peripheral:didReadRSSI:error:' in CBPeripheralDelegate
-  [corefoundation] Add missing CFSocket callbacks [#17713]
-  [corefoundation] Add DispatchTime.WallTime property
-  [coregraphics] Add CGAffineTransform.TransformSize method
-  [coremedia] Add operator overloads for CMTime
-  [extensions] Extensions may be fat (32/64) even if the main app isn't [#23291]
-  [extensions] Set soft-heap-limit=8m for Today-type extensions
-  [foundation] Add support for passing INativeObjects to NSLayoutConstraint.FromVisualFormat [#23102]
-  [foundation] Add NSString.Empty constant [#23932]
-  [foundation] Add helper methods to NSMetadataItem to make it more pleasant to use
-  [foundation] NSDirectoryEnumerator: implement IEnumerable of string, NSString and plain
-  [generator] Produce better API for *Async method that uses an NSError [#21322]
-  [msbuild] Add -Xlinker flags for simulator builds to enable entitlements [#20448]
-  [msbuild] Add support for referencing other assemblies in binding projects [#23674]
-  [runtime] Use the new logging facilities in Mono to redirect log output to NSLog [#24021]
-  [scenekit] Add a 'string' overload for SCNNode.AddAnimation [#23223]
-  [scenekit] Add SceneKit additions to CAAnimation, e.g. Fade[In|Out]Duration properties [#23820]
-  [uikit] Add UIPopoverPresentationController.PopoverBackgroundViewType [#23372]
-  [uikit] Add [Protocol] on UIPopoverBackgroundViewMethods [#23372]
-  [uikit] UIDynamicAnimator now implements IEnumerable&lt;UIDynamicBehavior&gt;
-  Many more ObjC protocols types (including NSObjectProtocol) are now exposed


## Bug fixes

-  [coreanimation] Workaround race condition during CALayer[Delegate] destruction [#15316]
-  [addressbookui] Preserve RespondsToSelector so this works on device [#16072][#23374]
-  [corlib] Add some missing memory barriers to the ConcurrentQueue methods to order memory operations [#22788]
-  [uikit] Fix binding for UIImage's animatedResizableImageNamed:capInsets:duration: [#23305]
-  [msbuild] Make sure to always collect generated files for compilation [#23328]
-  [addressbookui] Fix SelectPerson and PerformAction events on iOS8 [#23374]
-  [jit] Make each CASTCLASS_CACHE patch unique [#23478]
-  [linker] Preserve more dynamic caching infrastructure methods [#23483]
-  [objcruntime] Find BlockProxy attributes for optional members as well [#23540]
-  [jit] Implement #23021 fix for calls made from NEWOBJ too [#23557]
-  [mtouch] Do not throw an NRE on missing assemblies for Starter/Indie licences [#23602]
-  [uikit] Fix binding for UIApplicationDelegate application:didUpdateUserActivity: [#23672]
-  [mtouch] Fix path-with-space handling in the retro simulator support [#23766]
-  [corebluetooth] Fixed non toll-free bridge issue between CFUUIDRef and CBUUID [#23793]
-  Use zlib-helper.c from mono [#23798]
-  [mtouch] fat 32/64 (unified) applications must be strip'ped after being lipo'ed [#24116]
-  [mtouch] Fix linker (ld) error when assembly name doesn't match filename [desk #90367]
-  [llvm] Rewrite the way direct calls are made between llvm methods [#23976]
-  [mtouch] When for a missing symbol, only look in the current target [#24346]
-  [uikit] Mark UIApplication.BeginBackgroundTask (string, NSAction) as ThreadSafe [#24353]
-  [uikit] Add missing [iOS(6,0)] on some UILayoutFitting* constants [#24557]
-  [multipeerconnectivity] Enable the MCSession ctor when multiple certificates are supplied
-  [audiounit] Provide correct Find[Next]Component APIs (using ref)
-  Several fixes to the msbuild tasks used for unified an iOS8 features, including signing extensions


## Important Notes



Apple Xcode 6.1 requires Mac OSX 10.9.4+ (Mavericks) or 10.10 (Yosemite).
