---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "Xamarin.iOS 7.0"
---

# Xamarin.iOS 7.0



The Xamarin.iOS 7.0.x series introduces support for Apple's
	iOS 7.0 APIs. This version is based on the final release of 
	Apple's Xcode 5 and includes support for the iOS7 SDK API.

Don't miss the [introduction](/guides/ios/platform_features/introduction_to_ios_7)


	to iOS7 new features, including the [user interface](/guides/ios/platform_features/ios7_ui)


	changes. New documents will guide you to other new features,
	including the enhanced [background tasks](/guides/cross-platform/application_fundamentals/backgrounding)


	support, while others were [updated](/guides/ios/getting_started/device_provisioning)


	to help you move to Xcode5.## New features

### iOS7 Support



iOS7 adds many new frameworks for developers, including:-  SpriteKit, 
-  MultipeerConnectivity, 
-  GameController 
-  JavaScriptCore, and 
-  SafariServices. 


Several other API additions have been made to existing frameworks.
	For a detailed list of the changes in the API, see our document [API changes from 6.4.5 to 7.0.0](/releases/ios/api_changes/from_6.4.5_to_7.0.0).



New samples were also added to show you how to use the new
	features added in this release.### Based on Xamarin.iOS async and Mono 3.2



Xamarin.iOS 7.0 is based on the [6.4 series](http://docs.xamarin.com/releases/ios/xamarin.ios_6/xamarin.ios_6.4)


	and includes Async, 
	C# 5 as well as many other features from [Mono 3.2](http://www.mono-project.com/Release_Notes_Mono_3.2)

.### Enhanced protocol support



This release provides enhanced support for better bridging
	Objective-C protocols in our API and on third party
	bindings. Several new API are now easier to use since they
	do not  have to expose `NSObject`

 when a protocol is
	fneeded.   They can now expose a strongly typed interface that
	matches the Objective-C protocol.

See
	the [updated documentation](http://docs.xamarin.com/guides/ios/advanced_topics/binding_objective-c/binding_objc_libs#iOS7ProtocolSupport)

 for details on how this new feature works.### NUnitLite 0.9 support



This version of Xamarin.iOS ships with an updated Touch.Unit
	based on the [NUnitLite 0.9](https://launchpad.net/nunitlite/+milestone/0.9)

 release. It is backward compatible with 
	earlier versions and support async tests.## Important Notes



Apple iOS7 SDK is available only with Xcode 5 and
	requires OS X Mountain Lion 10.8.4 or later (i.e. OS X Lion 
	is **not**

 supported by Xcode 5). Still Xamarin.iOS 7+ **can be**

 used on OS X Lion with
	an older Xcode (e.g. 4.6) and an older SDK (e.g. iOS 6.1)

Apple has some pending issues for both [iOS7](https://developer.apple.com/library/ios/releasenotes/General/RN-iOSSDK-7.0/index.html#//apple_ref/doc/uid/TP40013202)

 and [Xcode5](https://developer.apple.com/library/ios/releasenotes/DeveloperTools/RN-Xcode/index.html#//apple_ref/doc/uid/TP40001051-SW241)


	that you should review. <a name="1"></a>


#  [Xamarin.iOS 7.0.1](#1)


7.0.1 is an hotfix for customers experiencing issues with type forwarders, commonly used in PCL assemblies, that results in AOT compile-time errors. <a name="2"></a>


#  [Xamarin.iOS 7.0.2](#2)


Xamarin.iOS 7.0.2 is an hotfix which:-  removes the "setShowingDeleteConfirmation" private selector from monotouch.dll.
-  fix a System.Net.Http redirection bug [#14783]
-  Note: The email and credit card validations inside System.ComponentModel.DataAnnotations are not presently working.


 <a name="3"></a>


#  [Xamarin.iOS 7.0.3](#3)


Xamarin.iOS 7.0.3 is a maintenance release. [API changes from 7.0.2 to 7.0.3](/releases/ios/api_changes/from_7.0.2_to_7.0.3).

## New features

-  Includes Xamarin.iOS for Visual Studio 1.6 server components 
-  Additional AudioUnit bindings 
-  Added Accelerate framework bindings for vImage* 
-  Added DispatchQueue.DispatchAfter API [#15111] 
-  Added NSMutableString to ease binding some native libraries 
-  Added AVCaptureDevice HasTorsh and HasFlash properties 
-  Added some CoreData missing properties 
-  NUnitOutputTextWriter now built-in into MonoTouch.NUnitLite.dll 


## Bug fixes

-  Fix WindowsIdentity name deserialization [#12789] 
-  CTFontCreateUIFontForLanguage: language can be null [#13346] 
-  Use a native wrapper object in NSThread's initWithTarget:selector:object: implementation [#13612] 
-  Fix simulator issues when running on OS X Mavericks [#13636] 
-  MacNetworkChange: implement using managed code [#13642] 
-  Keep track of whether assemblies whose resources are removed have changed between builds [#13945] 
-  [linker] Include uncommon calendars when the matching i18n option is specified [#13977] 
-  Debugger errors with "Incorrect number or types of arguments" [#14942] 
-  [linker] Preserve Dictionary <tkkey,tvalue>.get_Keys when JsonSerializationWriter is used (thru reflection) [#15027]
<li>Obsolete CoreBluetooth API using System.Guid [#15056]
<li>Obsolete AVAudioSession default ctor since it's a singleton class and the static SharedInstance property should be used [#15154]
<li>AVQueuePlayer.[Can]Insert[Item]'s 'afterItem' parameter can be null [#15194]
<li>Fix CGImage.ScreenImage (black in iOS7) to use UIScreen.Capture [#15199]
<li>[linker] Fix uncommon type encoding issue [#15220]
<li>Add [Autorelease] to ALAssetRepresentation.Get*Image methods [#15234]
<li>Fix retain/copy/release on blocks [#15250]
<li>Fix copying read-only assemblies [#15254]
<li>Fix NSData.ToString memory leak [#15272]
<li>Return values may need wrappers even if some parameters need to be disposed [#15283]
<li>Fix btouch [Protocol] support when using interface types from monotouch.dll [#15307]
<li>Obsolete the default ctor on AVMetadataItemFilter [#15308]
<li>[aot] Only use an AOT shortcut in the trampoline code if its safe to do so [#15345]
<li>Fix UIBezierPath base class
<li>Fix wrong compiler selection even if IsCxx was true
<li>Fix wrong events in CMMotionActivityManager bindings
<li>Fix running lipo with path containing spaces
<li>Fix marshalling of 'out string' parameters
<li>Fix iOS7 documentation downloading/merging
<li><b>7.0.3.215+</b> Fix missing (stripped) symbol affecting release (only) builds [#15506, #15585, #15628, #15669, #15797, #15846]
</li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></li></tkkey,tvalue>


 <a name="4"></a>


#  [Xamarin.iOS 7.0.4](#3)


Xamarin.iOS 7.0.4 is a maintenance release. [API changes from 7.0.3 to 7.0.4](/releases/ios/api_changes/from_7.0.3_to_7.0.4).

## New features

-  Includes Xamarin.iOS for Visual Studio 1.8 server components 
-  Added CoreGraphics's CGDataConsumer 


## Bug fixes

-  Support the [Transient] attribute on parameters [#13966] 
-  [btouch] Methods might need to be unsafe if it returns a delegate [#15503] 
-  NS[Mutable]ParagraphStyle.TabStops returns an array of NSTextTab 
-  Fixed CTParagraphStyle LineBreakMode and BaseWritingDirection properties 


 <a name="5"></a>


#  [Xamarin.iOS 7.0.5](#5)


Xamarin.iOS 7.0.5 is a maintenance release.## New features

-  Includes Xamarin.iOS for Visual Studio 1.10 server components 


## Bug fixes

-  Fix AOT compilation for very large methods [#16239]


 <a name="6"></a>


#  [Xamarin.iOS 7.0.6](#6)


Xamarin.iOS 7.0.6 is a maintenance release. [API changes from 7.0.4/5 to 7.0.6](/releases/ios/api_changes/from_7.0.4_to_7.0.6).

## New features

-  [runtime] Optimize registrar to merge duplicated method bodies [#15454]  The (static) registrar will create an Objective-C method for every exported C# method, and many of those Objective-C methods were very similar. This change will reduce the amount of code generated by merging many method bodies like this:

  `void foo () { /* 20 lines of code */ }<br> void bar {} { /* 20 lines of code */ }`  to

  `void zap () { /* 20 lines of code */ }<br> void foo () { zap (); }<br> void bar () { zap (); }`  The improvement can be significant, in the test case from the bug report the amount of generated registrar code was cut to less than a third.


-  [runtime] Implement the delegate ctor optimization in AOT mode.  This is a optimization that existed only the JIT previously and it is now enabled for AOT. LINQ and RX makes great use of features that benefits from this optimization.

 
-  [foundation] Typed  `NSCoding` and  `NSSecureCoding` protocol support.  Every  `NSObject` subclass provide a  `.ctor(NSCoder)` but types that do not conform to  `NS[Secure]Coding` would throw a native exception when either the constructor or  `NSObject.EncodeTo` were used. Now that the protocol is exposed a managed (easier to catch)  `InvalidOperationException` will be thrown.

 
-  [foundation] Typed NSCopying and NSMutableCopying protocol support [#6250]  Types that conform to the procotols now export  `Copy(NSZone)` or  `MutableCopy(NSZone)` methods. Also the  `NSObject.Copy()` method will now throw a managed  `InvalidOperationException` (instead of a native exception) if the type does not conform to  `NS[Secure]Copying` .

 
-  System.Dynamic.Runtime.dll and System.Dynamic.Runtime.dll PCL facade assemblies were added allowing Reactive Extensions NuGet PCL package to work;
-  [audiounit] Additional bindings


## Bug fixes

-  [mtouch] Remove --keeptemp option to fix possible activation loop [#12122] 
-  [foundation] ThrowOnInitFailure now catch `init*` not just `alloc` failures [#14399] 
-  [mtouch] Report invalid parameters like -v-v-v correctly [#14794] 
-  [btouch] Fix containing type when generating method signatures [#15799] 
-  [runtime] Ensure retain/release trampolines are thread-safe [#15838] 
-  [uikit] UIApplicationDelegate.HandleOpenURL is deprecated and OpenUrl should be used/proposed [#15862] 
-  [linker] Process XML files earlier since it can be used to add new assemblies [#15878] 
-  [mtouch] Fix GameController and MediaAccessibility frameworks issues on OS X Mavericks [#15950] 
-  [btouch] Avoid generating duplicated parameter names in async methods [#16036] 
-  [runtime] Fix write-back code in the trampolines to calculate current parameter location correctly [#16078] 
-  [coreimage] Fix some CIImage constructors that are not available on iOS [#16135] 
-  [linker] Fixed SweepStep not to re-add removed assemblies [#16213] 
-  [uikit] Add a NSLayoutConstraint.Create overload taking INativeObjects [#16279] 
-  [uikit] Add missing [NullAllowed] attributes on UITabBarItem and UIBarButtonItem [#16335] 
-  [runtime] Remove limit of five (5) `-app-arg=` arguments [#16386] 
-  [mscorlib] Better fallback for non-existent (in .NET) cultures [#16417] 
-  [uikit] Expose constants from (float-based enum) UIWindowLevel [#16469] 
-  [linker] Preserve System.Runtime.InteropServices.ICustomMarshaler members [#16485] 
-  [foundation] Mark [Obsolete] some NSNetService members [#16499] 
-  [uikit] UIControl.Add|RemoveTarget: support adding/removing the same target more than once for each event [#16565] 
-  [externalaccessory] ShowBluetoothAccessoryPicker allows null for both parameters [#16566] 
-  [coredata] Accept null for NSManagedObjectContext setUndoManager [#16623] 
-  [linker]Fix for System.Web.Services.dll reflection usage of ExtensionManager type [#16629] 
-  [uikit] Allow null for UIApplication.SendAction [#16633] 
-  [mapkit] Special case the selector '_original_setBoundingBox:' [#16638] 
-  [coreanimation] Properly introduce CAMediaTiming protocol and add it (missing) on CAEmitterCell [desk #52127] 
-  [spritekit] Add missing [NullAllowed] on SKSpriteNode APIs [desk #53182] 
-  [tools] Workaround for `ld64` issue [http://openradar.appspot.com/15358055] 
-  [mapkit] Add missing constructors for MKOverlayPathRenderer 
-  [uikit] Remove some duplicated selectors in UIPrintFormatter 
-  [uikit] UISeachBar also expose 'spellCheckingType' since 5.0 
-  [coremedia] Fix CMFormatDescription crash [forum] 
-  [mtouch] Fix case where C++ compiler was used (even if not specified) 
-  [aot] Avoid emitting two debug_line sections when using the GAS .file and .loc directives. 
-  [btouch] Fixed [MarshalNativeExceptions] support in 3rd party binding projects (was ignored). 
-  [runtime] Crash reports no longer contain file/line number information [#15202] 


 <a name="7"></a>


#  [Xamarin.iOS 7.0.7](#7)


Xamarin.iOS 7.0.7 contains fixes for specific issues affecting 7.0.6 - but is otherwise identical.## Bug fixes

-  [vs-addin] Fix a typo which causes NullReferenceException to be thrown in StartLogProxy [#17611] 
-  [arm] Fix issues found on UIPickerView related to ARM FP scratch registers change [#17597][#17612] 
-  [arm] Additional fix for ARM registers in 7.0.7.2 [#17793] 
-  [coremedia] Fix CMBufferQueue.CreateUnsorted not to depend on the managed CMBufferCallbacks2 since the OS structure might differ by iOS versions [#17330] 
-  [bcl] Null values on nullable value types were not handled in DataContractJsonSerializer [#16744] 
-  [bcl] Fix a NullReferenceException in Task.ContinueWith [#17498]
