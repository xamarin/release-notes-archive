---
id: 4A0E7C95-F691-45BD-90D7-78BC429EF91B
title: "Xamarin.iOS 8.10"
---

# Xamarin.iOS 8.10



The Xamarin.iOS 8.10 is the first major update since the introduction of the unified
	API. It contains several new features and fixes.## Major features

-  The Mono runtime/BCL updated to  [Mono 4.0](http://www.mono-project.com/docs/about-mono/releases/4.0.0/) . This include several updates to include MS.NET (reference sources) code into Mono's BCL. This is still a work in progress, future versions of XI will include more of MS.NET reference sources. 
-  Deeper ObjC interoperability. It is now possible to  **export** .NET defined  [protocols](/guides/ios/advanced_topics/registrar/#Protocols) and  [categories](/guides/ios/advanced_topics/registrar/#Categories) to Objective-C;
-  Better  `float` performance with the support for 32bits single precision floating point arithmetic (see Mono 4.0 release notes for some  [numbers](http://www.mono-project.com/docs/about-mono/releases/4.0.0/) . 
-  Bindings for  [VideoToolbox.framework](http://iosapi.xamarin.com/?link=N%3aVideoToolbox) . You can see them in action in our new  [sample](https://github.com/xamarin/monotouch-samples/tree/master/ios8/VideoTimeLine) <a>;
		</a>

-  F# updated to  [3.1.1.31](https://github.com/fsharp/fsharp/blob/3.1.1.27/CHANGES.txt) 


### Important Notes

-  **Deprecation:** From this version XI does not include an ARMv6 AOT compiler. No recent devices uses an ARMv6 CPU, the last one being the iPhone 3G.


-  **Deprecation:** The  **Generic value type sharing** setting is not optional anymore. It is now always enabled (which was the default). Turning it off caused several runtime issues when the code (application, 3rd party and even the BCL) was not ready to support it.


### Floating Point Performance



By default, Xamarin.iOS will use 64-bit floating points
	for its computations, even for values involving 32-bit
	floating point values (the `System.Single`

 .NET
	data type). This means that the following code snippet is
	executed entirely with 64-bit floats:```
float a = 1f;
	float b = 2f;
	float c = a*b;
```



While the higher precision is useful for certain class of
	applications, some applications will benefit (faster but less
	precise) from running 32-bit only operations in 32-bit mode.

To change the above behavior to use 32-bit float, in
	Xamarin.iOS 8.10 and higher, make sure that your **Additional mtouch arguments**

 in your iOS Build properties page to include
	the following command:```
--aot-options=-O=float32
```



By setting this option, the compiler will generate 32-bit
	floating point operations for 32-bit math instead. <a name="5"></a>


#  [Xamarin.iOS 8.10.5](#5)

Xamarin.iOS 8.10.5 is our fourth service release.
	The following document contains a list of the API changes from [API changes from 8.10.4 to 8.10.5](/releases/ios/api_changes/from_8.10.4_to_8.10.5).

## Bug fixes

-  [bcl] HttpClient authentication not working [ [#30869](https://bugzilla.xamarin.com/show_bug.cgi?id=30869) ]
-  [aot] Allow more than one --aot-options argument [ [#31245](https://bugzilla.xamarin.com/show_bug.cgi?id=31245) ]
-  [msbuild] Unable to upload ipa file from application loader w/watchkit extension [ [#33269](https://bugzilla.xamarin.com/show_bug.cgi?id=33269) ]


## Enhancements

-  [foundation] Added missing NSData API [ [#32848](https://bugzilla.xamarin.com/show_bug.cgi?id=32848) ]
-  [mono] Updated mono (runtime and BCL) to 4.0 service release 4


 <a name="4"></a>


#  [Xamarin.iOS 8.10.4](#4)

Xamarin.iOS 8.10.4 is a service release.
	The following document contains a list of the API changes from [API changes from 8.10.3 to 8.10.4](/releases/ios/api_changes/from_8.10.3_to_8.10.4).

## Bug fixes

-  [aot] Fix problem with F# methods that take many arguments [ [#31060](https://bugzilla.xamarin.com/show_bug.cgi?id=31060) ]
-  [msbuild] Allow more than one dot in the name of the executable assembly [ [#30348](https://bugzilla.xamarin.com/show_bug.cgi?id=30348) ]
-  [aot] Fix crash in AOT compiler [ [#26699](https://bugzilla.xamarin.com/show_bug.cgi?id=26699) ]
-  [avfoundation] Fix incorrect enum value in AVCaptureVideoStabilizationMode [ [#31518](https://bugzilla.xamarin.com/show_bug.cgi?id=31518) ]
-  [aot] Improve native code size with many async methods [ [#29615](https://bugzilla.xamarin.com/show_bug.cgi?id=29615) ]
-  [aot] Fix float -> nfloat conversion with 32-bit floating point math [ [#31846](https://bugzilla.xamarin.com/show_bug.cgi?id=31846) ]
-  [aot] Fix float -> long conversion with 32-bit floating point math [ [#31582](https://bugzilla.xamarin.com/show_bug.cgi?id=31582)
-  [runtime] Improve startup performance with a large number of types [ [#31491](https://bugzilla.xamarin.com/show_bug.cgi?id=31491) ]
-  [msbuild] Fix build failure due to incorrect parsing of external tool output [ [#31009](https://bugzilla.xamarin.com/show_bug.cgi?id=31009) ]
-  [msbuild] Watch application Info.plist UIDeviceFamily array is incorrect [ [#30958](https://bugzilla.xamarin.com/show_bug.cgi?id=30958) ]


 <a name="3"></a>


#  [Xamarin.iOS 8.10.3](#2)

Xamarin.iOS 8.10.3 add support for Xcode 6.4 and iOS 8.4 SDK.
	The following document contains a list of the API changes from [API changes from 8.10.2 to 8.10.3](/releases/ios/api_changes/from_8.10.2_to_8.10.3).

## Enhancements

-  Support for Xcode 6.4; 
-  Support for new iOS 8.4 SDK API 


 <a name="2"></a>


#  [Xamarin.iOS 8.10.2](#2)

Xamarin.iOS 8.10.2 is a service release.
	The following document contains a list of the API changes from [API changes from 8.10.1 to 8.10.2](/releases/ios/api_changes/from_8.10.1_to_8.10.2).

## Bug fixes

-  [runtime] Fix uncommon crash in dealloc [#25056] 
-  [addressbook] Fix AddressBook.ABPerson.GetEmails() crash in simulator [#28739] 
-  [aot] Avoid duplicate plt symbols for plt entries for synchronized methods [#28961] 
-  [linker] Resolve AssemblyName[Reference] when sweeping [#29211] 
-  [msbuild] Fix missing Info.plist build error [#29579] 
-  [arm] Fix the handling of callee saved fp registers during unwinding [#29726] 
-  [sprikekit] Fix inspection of SKFieldNode in the debugger [#29846] 
-  [corefoundation] Fixes for CFNotificationCenter [#29885] 
-  [corlib] Use UTF8 as the default encoding (like previous XI) [#29928] 
-  [aot] Fix the signature of native-func-aot wrappers [#29970] 
-  [arm64] Fix issue for Action/Func with 8 arguments [#30177] 
-  [aot] Avoid MT3001 errors for some assembly format errors [#30488] 
-  [aot] Build option --aot-options=-O=float32 can fail [#30698] 


## Notes

-  Some random InvalidCastExceptions at runtime [#29801] forced us to temporarily revert the existing fix for bug #24609. A different fix is presently being tested for XI 8.12. 


 <a name="1.74"></a>


#  [Xamarin.iOS 8.10.1.74](#1.74)

This release include fixes to ensure applications can work fine on the first iOS9 beta.
There is no API change for this release.

## Bug fixes

-  [coregraphics] Fixed CGColorSpace (missing) retain on some API 
-  [msbuild] Worked around dsymutil bug in Xcode 7 with armv7 arch [radar #21299754] 
-  [runtime] Fixed crashes on iOS9 by using 16kb trampoline pages 
-  [runtime] Always specify the full path to system libraries when using dlopen [#31001] 
-  [runtime] Fixed GCHandle issue and leak [#30420] 


 <a name="1"></a>


#  [Xamarin.iOS 8.10.1](#1)

Xamarin.iOS 8.10.1 is a service release.
	The following document contains a list of the API changes from [API changes from 8.10.0 to 8.10.1](/releases/ios/api_changes/from_8.10.0_to_8.10.1).

## Bug fixes

-  [registrar] Fixed base classes check when looking for methods implementing protocol members [#28757]
-  [debugger] Fixed debugger crash on device [#28847]
-  [linker] Added marking for SecurityDeclarations (different encoding than attributes) [#28918]
-  [msbuild] Allow skiping native strip / dsymutil in release builds [#29112]
-  [sgen] Fixed check on thread suspend [#29177]
-  [msbuild] Fixed a Log.LogWarning() call to use the correct overload [#29605]
-  [registrar] Properly skip encoding flags in method argument encodings [#29720]
-  [msbuild>}]>}] Microsoft.Bcl.Build NuGet breaks the build [#28752]
-  [profiler] Fixed performance counters on iOS device
-  [msbuild] Fixed creation of IPA files to not include iTunesMetadata/Artwork


 <a name="0"></a>


#  [Xamarin.iOS 8.10.0](#0)

The following document contains a list of the API changes from [API changes from 8.9.1 to 8.10.0](/releases/ios/api_changes/from_8.9.1_to_8.10.0).

## Enhancements

-  [externalaccessory] Added missing ConfigureAccessory binding [#26610]
-  [corefoundation] Added new Dispatch methods (e.g. DispatchBarrierAsync), concurrent DispatchQueue and DispatchSource.* types
-  [foundation] Added convenience methods to NSStream to create input/output stream (like CFStream)
-  [foundation] Added NSTextCheckingResult[Type] API [#26376]
-  [linker] Added support to allow [Preserve (Type)] with or without all members which allows an assembly to preserve types from any referenced assembly (including SDK assemblies) [#11883]
-  [llvm] Emit LLVM code into separate files to generate debug information
-  [opentk] Added new UniformMatrix[23] methods [#26926]
-  [registrar] Added support for arrays of INativeObjects to the static registrar [#26927]
-  [uikit] Added [Advice] on some UIView methods to help select the best API [#27334]
-  [uikit] Added missing NSUserActivityDocumentURLKey field [#27189]


## Bug fixes

-  [msbuild] Fixes error while uploading to appstore "ITMS-90047: "Disallowed paths ( "iTunesMetadata.plist" )..." [#29829][8.10.0.303]
-  [foundation] Fixed NSObject.Invoke to happen on the correct instance [#12543]
-  [rutime] Do not try to load anything from .monotouch-[32|64] for Classic apps [#22418]
-  [scenekit] SCNGeometry introduce Create method to provide strong typed return [#22554]
-  [security] Fixed querying keychain for SecIdentity on iOS 7+ [#24972]
-  [uikit] Fixed UIFont methods that are factory-like [#25511]
-  [linker] Preserve types given to custom attributes - even if they are inside an array [#26030]
-  [runtime] Fixed mono_thread_info_attach (mono-threads.c:159) assertion [#26222]
-  [btouch] Fix multi-level events on bound APIs to work under unified [#26432][#26784]
-  [coretext] Fixed CTFontManager font (un)registration [#26516]
-  [coreanimation] Fixed retains and releases of CALayer subclasses [#26532]
-  [msbuild] Replaced usage of the standard Copy task with SmartCopy [#26556]
-  [mapkit] MKUserLocation conforms to MKAnnotation [#26613]
-  [linker] Preserve QueryableEnumerable`1 if System.Linq.Queryable is used [#26683]
-  [linker] Fixed custom attributes referencing types in facade assemblies [#26752]
-  [bindings] Always build with all [LinkWith] libraries irrespective of specified architecture [#26804]
-  [registrar] ObjC BOOL is a real 'bool' in 64-bit iOS, and an 'unsigned char' otherwise [#26931]
-  [generator] Fixed creating bindings for INativeObject, e.g. CGContext [#27040]
-  [mtouch] Added MT0054 error checking for uncanonicalizable paths [#27047]
-  [generator] Fix rendering of delegates even if some are not inside a namespace [#27058]
-  [foundation] Allow some NSUrlSessionConfiguration properties to be set to null [#27156]
-  [arm64] Missing generic invoke method causing crash with ARM64 [#27201][#27324]
-  [coremedia] Fixed CMFormatDescription.Create (IntPtr) to assume owns=false [#27205]
-  [foundation] Added NSUrl.PathExtension [#27211]
-  [foundation] Fixed NSObject.Observer.Dispose [#27220]
-  [arm64] Fixed assertion on ARM64 / mini-arm64-gsharedvt.c:91 [#27244]
-  [healthkit] Fixed HKAnchoredObjectQuery delegate signature [#27275]
-  Removed internal Utils namespace to avoid conflicts with user code [#27279]
-  [arm64] Fixed performance degredation ARM64 compared to ARM7 [#27306]
-  [foundation] NSObject/Observer:ObserveValue must not be linked away [#27330]
-  [runtime] "Enable Generic Value Type Sharing" setting causes event not to fire [#27332]
-  [mtouch] Avoid downloading unrequired .dtd files from the web [#27340]
-  [msbuild] Do not allow executables with more than one dot [#27401]
-  [msbuild] Fixed archiving dSYM for unified API builds [#27419]
