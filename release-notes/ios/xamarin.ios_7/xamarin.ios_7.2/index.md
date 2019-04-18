---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 7.2"
---

# Xamarin.iOS 7.2



The Xamarin.iOS 7.2.x series is based on our latest stable release (7.0.7)
	and introduces support for Apple's iOS 7.1 APIs. 
	This version is based on the final release of 
	Apple's Xcode 5.1 and includes support for the iOS7.1 SDK API.## New features

### New iOS 7.1 API

There were no new frameworks added in iOS 7.1. 
	However there were many additions to the MediaPlayer framework (CarPlay)
	and a few additions in other frameworks.



The following document contains a list of the [API changes from 7.0.7 to 7.2.0](/releases/ios/api_changes/from_7.0.7_to_7.2.0)

### Xcode 5.1 support

This release adds support for Xcode 5.1. 
	Most of the changes are internal and are not visible to developers.
	Earlier versions of Xcode are still supported using Xamarin.iOS 7.2
	but Apple do require using the latest Xcode and SDK to publish to the App Store.

### NUnitLite 1.0 support



This version of Xamarin.iOS ships with an updated Touch.Unit
	based on the final [NUnitLite 1.0](http://nunitlite.org/index.php?p=releaseNotes)

 release. It is backward compatible with 
	earlier versions and supports async tests.

By default Touch.Unit runs every test case in the main (UI) thread.
	This is different from the *classic*

 NUnit console runner
	and some tests might depend on running on a background test.
	You can add a `[Timeout(Int32.MaxValue)]`

 attribute
	to such tests to have the Touch.Unit runner execute them on a 
	separate thread.## Important Notes



Apple iOS7.1 SDK is available only with Xcode 5.1 and
	requires OS X Mountain Lion 10.8.4 or later (i.e. OS X Lion 
	is **not**

 supported by Xcode 5.x). Still Xamarin.iOS 7+ **can be**

 used on OS X Lion with
	an older Xcode (e.g. 4.6) and an older SDK (e.g. iOS 6.1)

Apple has some pending issues for both [iOS7](https://developer.apple.com/library/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS7_1.html#//apple_ref/doc/uid/TP40013916-SW1)

 and [Xcode 5.1](https://developer.apple.com/library/mac/releasenotes/DeveloperTools/RN-Xcode/Introduction/Introduction.html)


	that you should review. <a name="6"></a>


#  [Xamarin.iOS 7.2.6](#6)

Xamarin.iOS 7.2.6 is a maintenance release. The following document contains a 
	list of the [API changes from 7.2.1 to 7.2.6](/releases/ios/api_changes/from_7.2.1_to_7.2.6)

## Major features

-  OpenGLES 3.0 support in OpenTK-1.dll 
-  Mono runtime/BCL updated to 3.6 
-  F# updated to 3.1.1.19 


## Enhancements

-  [audiounit] Add AUGraph.SetNodeInputCallback [#18598] 
-  [audiounit] Add GetElementCount method 
-  [avfoundation] Add AVCaptureSession.Preset1920x1080 [#18861] 
-  [avfoundation] Add missing Advance member in AVPlayerActionAtItemEnd enum [#19696] 
-  [avfoundation] Added missing AVAssetResourceLoadingDataRequest and AVAssetResourceLoadingContentInformationRequest 
-  [coregraphics] Add bindings for CGPDFContentStream, CGPDFOperatorTable and CGPDFScanner [#17393] 
-  [coregraphics] Add a CGAffineTransform.Scale|Rotate|Translate overloads identical to the native CGAffineTransform* methods [#19341] 
-  [foundation] Add helper methods for easier use of NSPredicate [#19442] 
-  [foundation] Add more conversion operators (casts) for NSDecimal [#20246] 
-  [foundation] Add NSTimeZone.GetLocalizedName [#20453] 
-  [generator] Support bindings without namespaces 
-  [generator] Report an BI1030 error when the type name is equal to the BaseType [#19751] 
-  [mtouch] Better error message (MT1015) if can't copy launcher [#18659] 
-  [mtouch] Report MT4141 for when apps try to register retain/release/dealloc and XI need to override them as well. 
-  [mtouch] Report MT5214 for when the native linker fails due to P/Invoke pointing to inexistent native method 
-  [System.Net.Http] Add cookies support to CFNetworkHandler 
-  [System.Net.Http] Add system proxy support for CFNetworkHandler [#19135] 
-  [System.ServiceModel.Primitives] Do not report MT9003 error when no actual types are used [#18664] 
-  [security] Bindings for SecTransport (low-level native SSL/TLS support) 
-  [uikit] Add UIAccessibilityIdentification protocol [#16492] 
-  [uikit] Add UIInputViewAudioFeedback protocol [#18550] 
-  [uikit] Mark UIActivityItemProvider as thread-safe [#18566] 


## Bug fixes

-  [registrar] Fix lookup of non-virtual properties in the dynamic registrar [#18604] 
-  [uikit] Allow null for UITableViewController.RefreshControl [#18744] 
-  [coregraphics] fix pinvoke declaration for CGPathCreateCopyByDashingPath [#18764] 
-  [generator] Do not throw ArgumentNullException in the generated Invoke methods of managed trampolines [#18846] 
-  [corevideo] Fix typo in CVPixelBufferGetWidthOfPlane [#18851] 
-  [System] Fix HttpWebRequest to correctly send body using authentication and POST [#19119] 
-  [runtime] Don't use the handle to lookup objects whose handle must be cleared [#19288] 
-  [runtime] Avoid joining attached threads [#19343] 
-  [coregraphics] Fix RectangleF.IsInfinite to call the right pinvoke [#19354] 
-  [gamekit] Fix GKTurnBasedEventHandlerDelegate.HandleInviteFromGameCenter [#19511] 
-  [registrar] We might not have a method_map entry if we're using the static registrar [#20013] 
-  [runtime] Fix a jit assertion on a class which contains an empty struct as a static field [#20349] 
-  [opentk] Remove duplicate System.ComponentModel.CancelEventArgs type [#20363] 
-  [System.Net.Http] Always add "Content-Length" in HttpClientHandler.SendAsync [forum #17770] 
-  [generator] Fix NSCoding detection for third-party libraries [forum #54078] 
-  [uikit] Fix typo in WeakDrawString selector [forum #49787] 
-  [linker] Fix processing attributes with null types [desk #68380] 
-  [coregraphics] Fix a race in CGPattern [desk #71902] 


## Known issues

-  Some files are not installed with the right permissions [ [#21474](https://bugzilla.xamarin.com/show_bug.cgi?id=21474) ]   
 This only affects systems where Xamarin.iOS is installed with a different user account than the developer's user account. The bug report contains  [a workaround](https://bugzilla.xamarin.com/show_bug.cgi?id=21474#c3) for affected systems.


 <a name="5"></a>


#  [Xamarin.iOS 7.2.5](#5)

Xamarin.iOS 7.2.5 is a compatibility release that includes support for [Xamarin 3.1.0](http://developer.xamarin.com/releases/vs/xamarin.vs_3/xamarin.vs_3.1/#0).

## Xamarin.iOS 7.2.5.5

Xamarin.iOS 7.2.5.5 is a hotfix release to address an issue deploying from Visual Studio while using a Trial license.

 <a name="4"></a>


#  [Xamarin.iOS 7.2.4](#4)

Xamarin.iOS 7.2.4 is an hotfix release with several fixes to the
	HTTP/web stack.

## Bug fixes

-  [System] Cleanup chained async operations [#19161] 
-  [System] Cleanup and simplify the ServicePoint's connection group list 
-  [System] Fix incorrect InvalidOperationException 
-  [System] Only recycle ServicePoints from the idle timer [#19823] 
-  [System] Fix a potential race condition in the WebConnectionGroup's connection list 


 <a name="3"></a>


#  [Xamarin.iOS 7.2.3](#3)



Xamarin.iOS 7.2.3 is a maintenance release that includes support for
	the [Xamarin Studio for VS 2.0](xamarin.ios_for_vs_2.0.html)

. <a name="2"></a>


#  [Xamarin.iOS 7.2.2](#2)



Xamarin.iOS 7.2.2 is a maintenance release that includes support for
	the [Xamarin Studio for VS 1.12](xamarin.ios_for_vs_1.12.html)

. <a name="1"></a>


#  [Xamarin.iOS 7.2.1](#1)

Xamarin.iOS 7.2.1 is a maintenance release. The following document contains a 
	list of the [API changes from 7.2.0 to 7.2.1](/releases/ios/api_changes/from_7.2.0_to_7.2.1)

## Major features

-  The new  [registrars](http://docs.xamarin.com/guides/ios/advanced_topics/registrar/) (first introduced in  [6.2.6](http://docs.xamarin.com/releases/ios/xamarin.ios_6/xamarin.ios_6.2/) ) are now  **enabled by default** . They catch many more errors and will prevent many bugs or undefined runtime behaviors. It is possible to fallback to the previous registrars by using  `--registrar:legacy` as an additional mtouch argument; 
-  Support for several scenarios for mixing  [NSObjects and generics](http://docs.xamarin.com/guides/ios/under_the_hood/api_design/nsobject_generics/) ; 
-  The  **sgen** garbage collector is now fully supported for iOS applications; 
-  The  ** [New Refcount](http://docs.xamarin.com/guides/ios/advanced_topics/newrefcount/)** extensions for GC (first introduced in  [5.2](http://docs.xamarin.com/releases/ios/monotouch_5/monotouch_5.2/) ) has been updated and enhanced. It is not an experimental feature anymore and can solve many memory management issues inside applications. It can now work with both Boehm and sgen garbage collectors; 
-  The  <c>WebSockets</c> API is now part of our  `System.dll` mobile profile; 
-  This release is based on the new Mono 3.4 release, including many HTTP stack improvements and SSL/TLS fixes and enhancements (Developers can now control which ciphers to use on a connection, this is an extension over Microsoft's .NET API). 


## Breaking Changes



To avoid code generation, which cannot be supported on iOS
	devices, the <c>System.Linq.Expressions</c>

 support was using
	our own Expression Visitor, which had some difference with the
	.NET API. The new interpreter implementation is now API
	compatible with .NET 4.5, breaking our previously exposed
	implementation.Previously our <c>ExpressionVisitor</c> class had
	all <c>VisitXXX</c> methods with <c>void</c> return type. E.g. <xmp>protected override void VisitParameter (ParameterExpression parameter)
{
	// Your code
}</xmp>

To match .NET <c>ExpressionVisitor</c> API all method
	signatures were changed to return same type as .NET API. This
	means user code overriding <c>VisitXXX</c> methods **must**
	be updated. E.g. The above code needs to be changed to: <xmp>protected override Expression VisitParameter (ParameterExpression parameter)
{
	// Your code
	return base.VisitParameter (parameter);
}</xmp>

## Enhancements

-  [btouch] Allow btouch building task to have multiple api definition files [desk #63279] 
-  [btouch] Enable debug mode, so we get file and line number information in stack traces 
-  [mtouch] Error messages from the registrar contain file name and line number information 
-  [mtouch] Allow --debugtrack (NSZombieEnabled) to work on devices 
-  [mtouch] The native strip is now execute on "non linked" release builds 
-  [mtouch] Ask native compiler to keep p/invokes and field to __Internal symbols when -dead_strip is used [desk #55195] 
-  [jit] Allow inlining of calls to method with the AggressiveInlining attribute in AOT mode 
-  [avfoundation] Add AVCaptureVideoDataOutputSampleBufferDelegate.DidDropSampleBuffer 
-  [avfoundation] Add convenience AVAudioSession.SetCategory methods 
-  [corefoundation] Add Background member to DispatchQueuePriority [#18188] 
-  [corefoundation] Add support for dispatch_group_notify_f 
-  [coremidi] Expose MIDIDestinationCreate 
-  [foundation] Lower memory requirements for any NSObject instance 
-  [foundation] Add NSMutableArray .NSSortDescriptorSorting category methods 
-  [foundation] Obsolete NSObject.Retain and Release and add Dangerous[Release|Retain] replacements [#17614] 
-  [uikit] Add two [UIAppearance] on UITableView properties (added in iOS7) 
-  [uikit] Add UIBezierPath.SetLineDash 
-  [uikit] Provide better alternative for [Category] + [Static] bindings (since extensions methods can't be static) [#15268] 
-  [System] Include IndentedTextWriter in the mobile profile 
-  [Mono.Data.Sqlite] Add support for custom collation functions [#16542][#17081] 
-  [System] Add HttpWebRequest.SupportsCookieContainer, WebRequest.CreateHttp [#18378] (in 7.2.1.31+) 


## Bug fixes

-  [System] Don't call CFNetworkCopyProxiesForAutoConfigurationScript from more than one thread [#7923 c21] 
-  [avfoundation] Make the API of AVCapture[Audio|Video]DataOutputSampleBufferDelegate more identical [#5997] 
-  [avfoundation] Add the interface/delegate for IAVCaptureVideoDataOutputSampleBufferDelegate [#5997] 
-  [gsharedvt] Add a wrapper to the mono_gsharedvt_constrained_call icall [#16439] 
-  [audiotoolbox] Bind AudioToolbox::TrackLength [#16600] 
-  [aot] Add runtime wrappers for methods of generic classes and generic methods [#16747] 
-  [corevideo] Fix CVPixelBufferPool.CreatePixelBuffer leak/retain [#16750] 
-  [avfoundation] Add a AVCaptureAudioDataOutput.SetSampleBufferDelegateQueue overload accepting a (protocol) interface [#16763] 
-  [gsharedvt] Fix memory leaks [#16787] 
-  [jit] Remove usage of mini_replace_type from mono_jit_runtime_invoke [#16830] 
-  [aot] Sanitize utf8 characters in symbol names [#16851] 
-  [System.Net.Http] Rework parts of CFNetworkHandler.HandleHasBytesAvailableEvent to avoid NULL crashes [#16862] 
-  [btouch] Fix the generator wrt implementing protocols in third-party bindings [#16948] 
-  [corlib] Mark all promise-style task exceptions observed [#17015] 
-  [gsharedvt] Avoid using the variable size code paths for non-variable size types with some array opcodes [#17023] 
-  [jit] Fix some checks in the arm dyn call code [#17101] 
-  [uikit] Surround UIGraphics.GetImageFromCurrentImageContext with an NSAutoreleasePool [#17213] 
-  [coredata] NSManagedObjectModel.IsConfiguration accept null for its configuration parameter [#17238] 
-  [coredata] Fix NSManagedObject.ValidateValue signature [#17267] 
-  [coredata] Add missing NSManagedObject.PrepareForDeletion API [#17268] 
-  [aot] Add the rgctx trampolines required by array helper wrappers [#17284] 
-  [mtouch] Recursively process nested types when checking for [DllImport (__Internal)] wrt strip [#17327] 
-  [uikit] Fix nullability of UILocalNotification and UIAnnotationView properties [#17377] 
-  [llvm] Load rgctx/imt arguments using a volatile load on arm [#17435] 
-  [mapkit] According to documentation MKOverlay conforming types should be thread safe [#17445] 
-  [mtouch] Fix fetching P/Invoke when the linker has not executed because of caching [#17506] 
-  [llvm] Disable llvm instead of asserting in some cases [#17527] 
-  [jit] Avoid running class cctors during AOT when using the AggressiveInlining attribute [#17558] 
-  [foundation] NS[Mutable]AttributedString accept a null NSDictionary when created [#17573] 
-  [mediaplayer] Make sure none of the MPMediaItem properties throw NRE [#17576] 
-  [security] SecAccessible, SecAuthenticationType and SecProtocol cannot be compared using IntPtr (opaque CFType) [#17579] 
-  [arm] Increase the length of the endfinally instruction [#17589] 
-  [mtouch] Avoid possible duplicates in the AssemblyResolver (e.g. different casing in XML files) [#17610] 
-  [uikit] Fetch TextShadowOffset when constructing UITextAttributes [#17646] 
-  [security] Fix SecProtocol and SecAuthenticationType equality checks [#17679] 
-  [eventkit] Add [NullAllowed] for EKRecurrenceRule constructors [#17680] 
-  [llvm] Disable the 'dse' optimization pass as it is buggy [#17616] 
-  [corlib] Xamarin Apps not running with Swiss German CultureInfo [#17690][#18116][#18230] 
-  [foundation] Ensure NSData.ToString() never throws an exception [#17693] 
-  [avfoundation] AVPlayerItem.FromAsset overloads accept null parameters [#17899] 
-  [uikit] UIPanGestureRecognizer accepts null for UIView in SetTranslation, TranslationInView and VelocityInView [#17979] 
-  [System.Net.Http] Schedule stream events on main-loop [#17990] 
-  [linker] Ensure XElement ConvertForAssignment (used thru reflection to fix #12571) gets preserved [#18093] 
-  [coredate] NSFetchRequest missing some [NullAllowed] attributes [#18152][#18153] 
-  [coredata] NSFetchedResultsControllerDelegate.DidChangeSection to use *I*NSFetchedResultsSectionInfo [#18173] 
-  [uikit] Add [NullAllowed] on NSString's drawing extensions [desk #60983] 
-  [uikit] UIPercentDrivenInteractiveTransition implement UIViewControllerInteractiveTransitioning protocol [desk #63597] 
-  [foundation] Fix mixup with initWithBase64Encoded[String|Data]:options: selectors/methods 
-  [audiotoolbox] Fix AudioBasicStreamDescription.IsVBR 
-  [mscorlib] Fix Arabic (ar-AE) locale issue [#18522] (in 7.2.1.31+) 
-  [foundation] Fixed crash using  <c>NSNotificationCenter</c> and NewRefCount [#18492][#18500] (in 7.2.1.31+) 
-  [vs] Fix mtbserver (System.Configuration) crash on some computers (in 7.2.1.31+) 
-  [registrar] Additional fixes to the new registrars [#18604][#18693] (in 7.2.1.31+) 
-  [btouch] Generator fix for [Protocol] and interface subclasses [desk #68380] (in 7.2.1.41+) 
-  [System] HTTP authentication timeouts [#19068][#19119] (in 7.2.1.42+) 


## Experimental



C# dynamic support. We made it possible to use C# dynamic
	with Xamarin.iOS but the feature is very complex and we need
	early adopters let us know what dynamic code they run on other
	platforms or would like to run on Xamarin.iOS.
