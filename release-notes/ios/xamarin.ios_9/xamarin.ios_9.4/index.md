---
id: 77259859-F920-4E15-9421-E0ED79F54AD3
title: "Xamarin.iOS 9.4"
brief: "Xamarin 9.4.x Releases"
---

# Xamarin.iOS 9.4



Xamarin.iOS 9.4 introduces support for iOS 9.2 and Xcode 7.2.
	This is not a large update from Apple so it's very close to our [9.2.x series](xamarin.ios_9.2)

.## Important Notes

Due to non-backwards compatible changes in Xcode 7 toolchain this
	version of Xamarin.iOS is only supported when used with Xcode 7 or
	later. This indirectly means the oldest version of iOS that applications
	can be directly deployed (on devices) is iOS 6.

# New Features

Support for iOS 9.2 and Xcode 7.2.

# Known issues

-  [insights] iOS apps fails to connect to debugger when Xamarin.Insights is enabled. In Forms templates, Xamarin.Insights is enabled by default [ [#34885](https://bugzilla.xamarin.com/show_bug.cgi?id=34885) ]


# Releases

 <a name="2"></a>


##  [Xamarin.iOS 9.4.2](#2)



The 9.4.2 is a service release including the following changes:### Bug fixes

-  [msbuild] Archiving for Publishing generates wrong value for CloudKit entitlement preventing distribution [ [#36189](https://bugzilla.xamarin.com/show_bug.cgi?id=36189) ]
-  [jit] Fix the support for gshared types in mini_emit_initobj [ [#37079](https://bugzilla.xamarin.com/show_bug.cgi?id=37079) ]
-  [generator] Be more defensive when converting pointers to CMSampleBuffers [ [#37187](https://bugzilla.xamarin.com/show_bug.cgi?id=37187) ]
-  [llvm] Disable support for nested clauses, it still doesn't work. Fixes #37273 [ [#37273](https://bugzilla.xamarin.com/show_bug.cgi?id=37273) ]  **[9.4.2.27+]**
-  [jit] Fix the reference type detection for Volatile:Read/Write [ [#37846](https://bugzilla.xamarin.com/show_bug.cgi?id=37846) ]  **[9.4.2.27+]**


 <a name="1"></a>


##  [Xamarin.iOS 9.4.1](#1)



The 9.4.1 release replace the, short-lived 9.2.2 service
	release. It's identical to the previous one but includes
	the iOS 9.2 API update and Xcode 7.2 support.

The following document contains a complete list of the [API changes from 9.4.0 to 9.4.1](/releases/ios/api_changes/from_9.4.0_to_9.4.1)

.### Bug fixes

-  [profiler] Create a static version of libmono-profiler-log which doesn't link against eglib [ [#29745](https://bugzilla.xamarin.com/show_bug.cgi?id=29745) ]
-  [msbuild] Make sure to touch the Watch App binary during a build [ [#34205](https://bugzilla.xamarin.com/show_bug.cgi?id=34205) ]
-  [registrar] Properly handle Selector and Class return values in the static registrar [ [#34440](https://bugzilla.xamarin.com/show_bug.cgi?id=34440) ]
-  [mtouch] Fix background fetch (Xcode change) [ [#34552](https://bugzilla.xamarin.com/show_bug.cgi?id=34552) ]
-  [linker] Fix generics usage inside custom attributes [ [#34609](https://bugzilla.xamarin.com/show_bug.cgi?id=34609) ]
-  [coregraphics] Fix CGDataProvider to not free GCHandles before the native code is done with the corresponding data [ [#34633](https://bugzilla.xamarin.com/show_bug.cgi?id=34633) ]
-  [msbuild] Fix Error reading framework definition '/Library/Frameworks/Mono.framework/External/xbuild-frameworks/Xamarin.TVOS/v1.0' [ [#35510](https://bugzilla.xamarin.com/show_bug.cgi?id=35510) ]
-  [mtouch] Set a max number of simultaneous strippers and AOT compilers [ [#35786](https://bugzilla.xamarin.com/show_bug.cgi?id=35786) ]
-  [btouch] Fix possible AmbiguousMatchException when finding properties [ [#35837](https://bugzilla.xamarin.com/show_bug.cgi?id=35837) ]
-  [arm64] Fix passing of vtypes by ref [ [#35959](https://bugzilla.xamarin.com/show_bug.cgi?id=35959) ]
-  [msbuild] Default IpaIncludeArtwork to False [ [#36238 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36238) ]
-  [runtime] Don't set the BLOCK_HAS_DESCRIPTOR flag for blocks [ [#36317](https://bugzilla.xamarin.com/show_bug.cgi?id=36317) ]
-  [msbuild] Find the correct architecture for device specific builds
-  [msbuild] msbuild does not pass the `float32` option to mtouch
-  [mscorlib] Invalid DateTime format for Norway, Serbia and Finland cultures [ [#36003 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36003) ]  **(9.4.1.12+)**
-  [System.Runtime.Serialization] Static serializer changed to avoid Nullable value-types [#36100 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36100) ]  **(9.4.1.12+)**
-  [aot] Cache inflated methods loaded from aot images to avoid repeating an expensive search [ [#36256 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36256) ]  **(9.4.1.12+)**
-  [gsharedvt] async / await - custom awaiter crashing on device [ [#36383 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36383) ][ [#36676 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36676) ]  **(9.4.1.12+)**
-  [System.Xml] Fix endless recursion in XmlCompiledTransform [ [#36436 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36436) ]  **(9.4.1.12+)**
-  [aot] MethodInfo.MakeGenericMethod(...).Invoke causes "Attempting to JIT compile method" exception [ [#36566 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36566) ]  **(9.4.1.12+)**
-  [aot] Make sure ptr-to-structure and structure-and-ptr wrappers are unique [ [#20186](https://bugzilla.xamarin.com/show_bug.cgi?id=20186) ]  **(9.4.1.23+)**
-  [aot] Don't hardcode the nursery size in aot write barriers [ [#35414](https://bugzilla.xamarin.com/show_bug.cgi?id=35414) ]  **(9.4.1.23+)**
-  [mono] Fix float32 support for native type operations [ [#36125](https://bugzilla.xamarin.com/show_bug.cgi?id=36125) ]  **(9.4.1.23+)**
-  [msbuild] Include com.apple.developer.icloud-container-environment in the whitelist [ [#36189 ](https://bugzilla.xamarin.com/show_bug.cgi?id=36189) ]  **(9.4.1.23+)**
-  [jit] Avoid a verification error in gsharedvt code with ldarga + gshared types [ [#36292](https://bugzilla.xamarin.com/show_bug.cgi?id=36292) ]  **(9.4.1.23+)**
-  XmlObjectSerialier: fix ISerializable for XmlObjectSerializer, DataContractSerializer... [ [#37171](https://bugzilla.xamarin.com/show_bug.cgi?id=37171) ]  **(9.4.1.23+)**
-  [uikit] NSTextLayoutOrientationProvider.LayoutOrientation is a readonly property [ [#37405](https://bugzilla.xamarin.com/show_bug.cgi?id=37405) ]  **(9.4.1.23+)**
-  [msbuild] Missing resources (storyboards, nibs...) inside .app [ [#38206](https://bugzilla.xamarin.com/show_bug.cgi?id=38206) ]  **(9.4.1.25+)**


 <a name="0"></a>


##  [Xamarin.iOS 9.4.0](#0)



This 9.4.x release includes all the fixes from the latest
	9.2 stable release along with support for the final releases
	of iOS 9.2 and Xcode 7.2.

The following document contains a complete list of the [API changes from 9.2.1 to 9.4.0](/releases/ios/api_changes/from_9.2.1_to_9.4.0)

.
