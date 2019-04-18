---
id: 77259859-F920-4E15-9421-E0ED79F54AD3
title: "Xamarin.iOS 9.2"
brief: "Xamarin 9.2.x Releases"
---

# Xamarin.iOS 9.2



The Xamarin.iOS 9.2 series upgrades the Mono stack from
	Mono 4.0 to [Mono 4.2](http://www.mono-project.com/docs/about-mono/releases/4.2.0/)

 
	One of the major themes in
	Mono 4.2.xx series is the continued adoption of Microsoft's
	open sourced .NET code to improve the conformance, speed and
	memory usage of our stack.Xamarin.iOS 9.2 is the successor of [9.0](xamarin.ios_9.0) which introduced
	support for iOS 9 API and Xcode 7.

## Important Notes

Due to non-backward compatible changes in Xcode7.x toolchain this
	version of Xamarin.iOS is only supported when used with Xcode 7.x or
	later. This indirectly means the oldest version of iOS that applications
	can be directly deployed (on devices) is iOS 6.

# New Features

## Visual Studio: New Mac Build Agent



We have rewritten the Mac Build agent that Visual Studio
	uses to connect to.

The user experience is vastly superior.   Not only because
	it is now easier, more convenient and more reliable to link
	your Windows and Mac computers, but because we have addressed
	many of the fundamental design limitations, shortcomings and
	bugs from our previous implementation.   This means more
	reliable builds, debugging and runs.

We have replaced our pairing and authentication system with
	one powered by SSH, which now encrypts all data transfers and
	uses the MacOS provided SSH server as the mechanism to connect
	your Windows and Mac computers.## WCF available for every license level



It is now possible to use System.ServiceModel.dll and
	System.ServiceModel.Web.dll assemblies with the **Starter**


	and **Indie**

 licenses.# Improvements

## Code Generation Optimizations



When compiling with LLVM, Xamarin.iOS will no longer
	generate intermediate files, and instead will generate object
	code directly.   This allowed us to generate more efficient
	code (in some large application scenarios, LLVM produced
	binaries are 3% smaller) and slightly improved build times.# Known issues

-  [insights] iOS apps fails to connect to debugger when Xamarin.Insights is enabled. In Forms templates, Xamarin.Insights is enabled by default [ [#34885](https://bugzilla.xamarin.com/show_bug.cgi?id=34885) ]


# Releases

 <a name="2"></a>


##  [Xamarin.iOS 9.2.2.29](#2)



The 9.2.2.x is a service release that fixes the following
	issues:### Bug fixes

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


 <a name="1"></a>


##  [Xamarin.iOS 9.2.1.52](#1)



The 9.2.1 release adds support for iOS 9.1 SDK and API
	and Xcode 7.1 to the previous 9.2.0 release along with some
	additional fixes.

The following document contains a complete list of the [API changes from 9.1.0 to 9.2.1](/releases/ios/api_changes/from_9.1.0_to_9.2.1)

.### Bug fixes

-  [uikit] Add a UIMutableApplicationShortcutItem.UserInfo setter [ [#35123](https://bugzilla.xamarin.com/show_bug.cgi?id=35123) ]
-  [modelkit] Fix MDLObject.GetBoundingBox crash [ [#35116](https://bugzilla.xamarin.com/show_bug.cgi?id=35116) ]
-  [llvm] Fix the handling of r4 arguments during calls [ [#35044](https://bugzilla.xamarin.com/show_bug.cgi?id=35044) ]
-  [runtime] Ensure blocks names are null-terminated C string [ [#34518](https://bugzilla.xamarin.com/show_bug.cgi?id=34518) ]
-  [linq] Fix NIE in Microsoft.Scripting.Interpreter.EqualInstruction.Create [ [#34334](https://bugzilla.xamarin.com/show_bug.cgi?id=34334) ]
-  [msbuild] Archive now shows wrong app name (Assembly instead of App Name) [ [#34981](https://bugzilla.xamarin.com/show_bug.cgi?id=34981) ]
-  [registrar] Fix threading issues in the dynamic registrar [ [#33981](https://bugzilla.xamarin.com/show_bug.cgi?id=33981) ]  **(9.2.1.50+)**
-  [msbuild] Fix IPA creation not to include artefacts from previous builds [ [#34793](https://bugzilla.xamarin.com/show_bug.cgi?id=34793) ]  **(9.2.1.50+)**
-  [linker] Don't remove external module references from non-linked assemblies [ [#35372](https://bugzilla.xamarin.com/show_bug.cgi?id=35372) ]  **(9.2.1.50+)**
-  [watchkit] Submission rejected with "Invalid WatchKit Support" [ [#35493](https://bugzilla.xamarin.com/show_bug.cgi?id=35493) ]  **(9.2.1.50+)**
-  [repl] Fix the REPL assemblies that Xamarin Inspector uses at runtime [ [#35695](https://bugzilla.xamarin.com/show_bug.cgi?id=35695) ]  **(9.2.1.51+)**
-  [jit] Fix memory leaks in the generic sharing code [ [#36000](https://bugzilla.xamarin.com/show_bug.cgi?id=36000) ]  **(9.2.1.52+)**
-  [cloudkit] Incorrect entitlement in archived for publishing prevents distribution [ [#36189](https://bugzilla.xamarin.com/show_bug.cgi?id=36189) ]  **(9.2.1.54+)**


 <a name="0"></a>


##  [Xamarin.iOS 9.2.0.84](#0)



This 9.2.x release includes all the fixes from the latest
	9.0 stable release along with additional fixes and features.

The following document contains a complete list of the [API changes from 9.0.1 to 9.2.0](/releases/ios/api_changes/from_9.0.1_to_9.2.0)

.### Bug fixes

-  [cecil] Fix regression for async methods compiled with VS2013 [ [#33124](https://bugzilla.xamarin.com/show_bug.cgi?id=33124) ]
-  [btouch] Fix namespace issue on *Appearance types [ [#34042](https://bugzilla.xamarin.com/show_bug.cgi?id=34042) ]
-  [aot] Fix AOT issue with obfuscated assembly [ [#34147](https://bugzilla.xamarin.com/show_bug.cgi?id=34147) ]  **9.2.0.84+**
