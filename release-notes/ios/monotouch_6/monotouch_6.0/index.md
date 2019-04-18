---
id: B873CFAC-1C1C-58AE-737B-F6A1431A922E
title: "MonoTouch 6.0"
---

The MonoTouch 6.0 series introduces support for Apple's iOS 6.0 APIs and
requires Mac OS X Lion (10.7) or Mountain Lion (10.8).

 ![](monotouch_6.0/Images/ios6_large.jpeg)

 <a name="New_Docs" class="injected"></a>


## New Docs

To help you get running with iOS 6, we've prepared a slew of new guides and
articles. Checkout the [Introduction to iOS 6](/guides/ios/platform_features/introduction_to_ios_6) guide for more information.

 <a name="New_Samples" class="injected"></a>


## New Samples

The following samples show some of the new features in MonoTouch 6.0 that
utilitize iOS 6 APIs:

 <a name="" class="injected"></a>


###  [Calendars](https://github.com/xamarin/monotouch-samples/tree/master/Calendars)

Illustrates usage of the EventKit framework including Calendars and
Reminders. Shows how to create, retrieve, query, modify, and delete both
calendar events and reminders. Additionally, it illustrates how to use the
built-in controllers to create and modify calendar events.

 <a name="" class="injected"></a>


###  [CircleLayout](https://github.com/xamarin/monotouch-samples/tree/master/CircleLayout)

This is an introduction to the new UICollectionView types. This sample allows
you to add / remove cells that are displayed in a circle.

 <a name="" class="injected"></a>


###  [FrogScroller](https://github.com/xamarin/monotouch-samples/tree/master/FrogScroller)

This sample shows how to use the simpler scrolling features available when
using UIPageViewController, UIScrollView and CATiledLayer

 <a name="" class="injected"></a>


###  [LineLayout](https://github.com/xamarin/monotouch-samples/tree/master/LineLayout)

This is another UICollectionView sample that shows how to scroll cells
horizontally, including how to set the final scrolling position to the nearest
cell.

 <a name="" class="injected"></a>


###  [MotionGraphs](https://github.com/xamarin/monotouch-samples/tree/master/MotionGraphs)

This sample produce time-based graphs of the values (accelerometer, gyroscope
and device motion) coming from the different sensors exposed by CoreMotion.

 <a name="" class="injected"></a>


###  [OpenGLScroller](https://github.com/xamarin/monotouch-samples/tree/master/OpenGLScroller)

This sample demonstrates the usage of OpenGL in a scroll view.

 <a name="" class="injected"></a>


###  [PinchIt](https://github.com/xamarin/monotouch-samples/tree/master/PinchIt)

This is an introduction to Collection Views, and illustrates the use of a
flow layout to pinch and move cells.

 <a name="" class="injected"></a>


###  [Quotes](https://github.com/xamarin/monotouch-samples/tree/master/Quotes)

This sample demonstrates the capabilities of the new attributed string
drawing, showing various different usages and functionality of attributed
strings.

 <a name="" class="injected"></a>


###  [Stars](https://github.com/xamarin/monotouch-samples/tree/master/Stars)

This is an introduction to Core Motion, demonstrated by a virtual reality
where you can see stars and rotating cubes. The sample uses Core Motion to
determine which way the device is facing to display these elements correctly in
the virtual reality.

&nbsp;

Here are some additional new samples that highlight other new features in
MonoTouch 6:

 <a name="" class="injected"></a>


###  [AudioQueueOfflineRenderDemo](https://github.com/xamarin/monotouch-samples/tree/master/AudioQueueOfflineRenderDemo)

 *An example demonstrating the Audio Queue offline rendering API. The sample produces LPCM output from an mp3 file, which is written to disk as a .caf file then subsequently played back to show the offline rendering is working as expected.*

 <a name="" class="injected"></a>


###  [BubbleCell](https://github.com/xamarin/monotouch-samples/tree/master/BubbleCell)

 *This example has been update to show how to use the new strongly typed notifications.*

 <a name="" class="injected"></a>


###  [CoreImage](https://github.com/xamarin/monotouch-samples/tree/master/CoreImage)

 *The sample has been updated to become a regression test suite for CoreImage effects.*

 <a name="" class="injected"></a>


###  [CoreMidiSample](https://github.com/xamarin/monotouch-samples/tree/master/CoreMidiSample)

 *This sample shows how to probe the MIDI devices connected to your iOS device and send tones to them*

 <a name="" class="injected"></a>


###  [CustomInputStream](https://github.com/xamarin/monotouch-samples/tree/master/CustomInputStream)

 *This sample illustrates how to derive from NSInputStream and create subclass that is toll-free bridged to CFReadStream that can be used with NSMutableUrlRequest.*

 <a name="" class="injected"></a>


###  [CustomPropertyAnimation](https://github.com/xamarin/monotouch-samples/tree/master/CustomPropertyAnimation)

 *This example shows how CoreAnimation can be used to animate arbitrary C# properties.*

 <a name="" class="injected"></a>


###  [GLCameraRipple](https://github.com/xamarin/monotouch-samples/tree/master/GLCameraRipple)

 *This sample shows how to use  [MonoTouch.GLKit](http://iosapi.xamarin.com/?link=N%3aMonoTouch.GLKit)to render OpenGL frames, AVFoundation to fetch live video from the camera and OpenTK's API to load a couple of shaders that simulate a water ripple effect when the user touches the display.*   
   
 *This uses the  [CVOpenGLESTextureCache](http://iosapi.xamarin.com/?link=T%3aMonoTouch.CoreVideo.CVOpenGLESTextureCache)class which was introduced in iOS 5.0 that binds CoreVideo buffers to OpenGL textures.*

 <a name="" class="injected"></a>


###  [ImageProtocol](https://github.com/xamarin/monotouch-samples/tree/master/ImageProtocol)

 *This sample shows how to register a custom NSUrlProtocol.*

 <a name="" class="injected"></a>


###  [RosyWriter](https://github.com/xamarin/monotouch-samples/tree/master/RosyWriter)

 *This sample shows how to use AVFoundation, GLKit, Grand Central Dispatch queues, CoreVideo and ALAssets. It captures video, process video frames (in this example, we remove the "green" component from each frame turning images rosy), show the resulting data and optionally save the resulting video and audio into the user's Photo storage.*

 <a name="" class="injected"></a>


###  [SimpleTextInput](https://github.com/xamarin/monotouch-samples/tree/master/SimpleTextInput),  [GestureRecognizers](https://github.com/xamarin/monotouch-samples/tree/master/Touches_GestureRecognizers),  [Touch](https://github.com/xamarin/monotouch-samples/tree/master/Touch)

 *These samples were updated to show how to use the new simpler to use UIGestureRecognizer APIs.*

&nbsp;

 <a name="What's_new?" class="injected"></a>


# What's new?

iOS 6 introduced several new technologies, including new frameworks like:

-  PassKit;
-  Social (e.g. Facebook);
-  MediaToolbox; and
-  AdSupport


   
   
 and many enhancements to existing frameworks. MonoTouch 6.0
supports them with new, strongly-typed C# bindings. The following documents
contain a list of [5.4 to 6.0 API changes](/releases/ios/api_changes/from_5.4.0_to_6.0.0).

In addition we have updated some of the core APIs to simplify
development:

-  NSDictionary has a new constructor that takes a params object [] and one that takes params NSObject [], allowing users to create dictionaries from a list of objects. 
-  The NSSet API has been extended to better blend with C#.
-  NSAttributedString can now take UIKit-specific attributes (UIStringAttributes) and has a constructor that enables the simple creation of attributed strings for use with UIKit. 


   
   
 iOS 6 support requires you to use Xcode 4.5 and also requires the
latest stable version of MonoDevelop. Make sure that MonoDevelop's SDK location
is configured to point to the location of your Xcode 4.5 directory.

Note that iOS 5.x support is still possible using MonoTouch 6 and that you
can also use Xcode 4.4 for iOS 5.x support. If you are required to support older
versions or phones (e.g. armv6) then you should log into the [customer's service area](https://store.xamarin.com/account/products) and download the latest MonoTouch 5.4 release.

Visit our updated MonoTouch [samples repository](https://github.com/xamarin/monotouch-samples) to get started.

 <a name="New_enhancements_from_recent_MonoTouch_releases" class="injected"></a>


# New enhancements from recent MonoTouch releases

 <a name="New_Library_Features" class="injected"></a>


## New Library Features

 <a name="Cross-thread_UI_Checks" class="injected"></a>


### Cross-thread UI Checks

Many developers creating multi-threaded applications and using Grand Central
Dispatch have historically called methods on the UI thread from a background
thread accidentally corrupting the state of UIKit.

This leads to strange behavior in the best case and to hard to track down
crashes in the worst case.

In Debug mode, MonoTouch will now produce an exception if you try to call
UIKit thread unsafe APIs from a background thread. This will help developer
identify parts of their code that need to be modified. If you run into this
exception, chances are that you need to modify code that might look like
this:

```
void UpdateLabel (string progress)
{
    myUILabel.Text = progress;
}
```

To look like this:

```
void UpdateLabel (string progress)
{
    // Invoke the callback that sets the "Text" property on the main thread
    myUILabel.BeginInvokeOnMainThread (delegate {
        myUILabel.Text = progress;
    });
}
```

The check is only performed on debug builds and is stripped out from release
binaries. This behavior can be changed by using the --force-thread-check and
--disable-thread-check to mtouch.

If you want to disable this behavior at runtime, you can set the
UIApplication.CheckForIllegalCrossThreadCalls property to false.

 <a name="CoreMIDI_APIs" class="injected"></a>


### CoreMIDI APIs

This release comes with a complete binding to the CoreMIDI APIs on iOS and
MacOS X.

The new [CoreMidiSample](https://github.com/xamarin/monotouch-samples/tree/master/CoreMidiSample) shows how to use it.

 <a name="Strongly_Typed_Notifications" class="injected"></a>


### Strongly Typed Notifications

MonoTouch now exposes a nested class "Notifications" that allows developers
to add observers to iOS notifications using strong types. This reduces the need
to look up the documentation and writing tests to determine the keys and values
to get data out of a posted notification.

The strongly typed "AddObserver" method allows developers to take the
guesswork out and reduce their trips to the documentation. With strongly typed
notifications the parameters and their types are available to you from the IDE.
This is how they work:

Calling `Dispose()` on a notification token will now unregister
the notification.   
   
   
   
 Examples:

```
//
// Lambda style
//

// listening
notification = UIKeyboard.Notifications.ObserveObserveWillShow ((sender, args) => {
    /* Access strongly typed args */
    Console.WriteLine ("Notification: {0}", args.Notification);

    Console.WriteLine ("FrameBegin", args.FrameBegin);
    Console.WriteLine ("FrameEnd", args.FrameEnd);
    Console.WriteLine ("AnimationDuration", args.AnimationDuration);
    Console.WriteLine ("AnimationCurve", args.AnimationCurve);
});

// To stop listening:
notification.Dispose ();

//
//Method style
//
NSObject notification;
void Callback (object sender, ObserveWillShow args)
{
    // Access strongly typed args
    Console.WriteLine ("Notification: {0}", args.Notification);

    Console.WriteLine ("FrameBegin", args.FrameBegin);
    Console.WriteLine ("FrameEnd", args.FrameEnd);
    Console.WriteLine ("AnimationDuration", args.AnimationDuration);
    Console.WriteLine ("AnimationCurve", args.AnimationCurve);
}

void Setup ()
{
    notification = UIKeyboard.Notifications.ObserveObserveWillShow (Callback);
}

void Teardown ()
{
    notification.Dispose ();
}
```

 <a name="UIGestureRecognizer" class="injected"></a>


### UIGestureRecognizer

The UIGestureRecognizer APIs now have a strongly typed API that is easier to
use. Previously users needed to expose a selector, create a selector reference
and get the type right on their callback.

You can The API now allows a delegate that will be invoked upon a match to be
passed directly in the constructor instead of using the AddTarget method later
or using selectors/objects.

Previously you would write code like this:

&nbsp;

```
void Setup ()
{
    var panGesture = new UIPanGestureRecognizer (this, new Selector ("PanImage"));
    view.AddGestureRecognizer (panGesture);
}

[Export ("PanImage")]
void PanImage (UIPanGestureRecognizer gestureRecognizer)
{
    Console.WriteLine ("Image panned");
}
```

&nbsp;

Now you write code like this:

```
void Setup ()
{
    var panGesture = new UIPanGestureRecognizer (PanImage);
    view.AddGestureRecognizer (panGesture);
}

void PanImage (UIPanGestureRecognizer gestureRecognizer)
{
    Console.WriteLine ("Image panned");
}
```

Or even:

```
void Setup ()
{
    var panGesture = new UIPanGestureRecognizer ((recognizer) => {
       Console.WriteLine ("panned");
    });
    view.AddGestureRecognizer (panGesture);
}
```

 <a name="OpenTK" class="injected"></a>


### OpenTK

There is now a new OpenTK-1.0 assembly which provides the OpenTK 1.0 API.

The reason for this change is that the OpenTK 1.0 API is not backwards
compatible with our existing OpenTK.dll. In the future we will keep OpenTK.dll
for backwards compatibility, while OpenTK-1.0.dll should be used in new
projects. See the API differences document for details on the actual
changes.

 <a name="GLKit" class="injected"></a>


### GLKit

GLKViewController now exposes an "Update" method that is invoked to update
the display. This allows GLKit code to be smaller and not require a
GLKViewControllerDelegate implementation to exist.

 <a name="CoreVideo" class="injected"></a>


### CoreVideo

Added CVOpenGLTextureCache support that allows binding CoreVideo pixel
buffers to OpenGL textures.

There are two new samples that illustrate the CoreVideo's OpenGLTextureCache: [GLCameraRipple](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/GLCameraRipple) and [RosyWriter](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/RosyWriter).

 <a name="NSUrlProtocol" class="injected"></a>


### NSUrlProtocol

It’s now possible to use `NSUrlProtocol` to register custom url
protocols. A sample has been created to show how ( [ImageProtocol](https://github.com/xamarin/monotouch-samples/tree/master/ImageProtocol)).

 <a name="Animating_C#_properties_with_CoreAnimation" class="injected"></a>


### Animating C# properties with CoreAnimation

C# properties that have been flagged with the [Export] attribute can now be
animated by CoreAnimation.

A sample [has been added](https://github.com/xamarin/monotouch-samples/tree/master/CustomPropertyAnimation) that shows how it works

 <a name="UIAppearance_support" class="injected"></a>


### UIAppearance support

Based on new documentation from Apple, the UISlider class now has support for
UIAppearance and more properties have been added to existing types that
supported UIAppearance.

 <a name="New_Tooling_Features" class="injected"></a>


## New Tooling Features

 <a name="Parameters_to_Applications" class="injected"></a>


### Parameters to Applications

You can now pass parameters to applications by adding the parameters in the [Run/General section](http://screencast.com/t/YPg9Hy0e) in the project preferences as well as setting environment variables.
You can use this to set environment variables in your application as well, in
particular you can use this to control the behavior of the Mono runtime by using
the options documented in the mono manual page.

 <a name="Linker_Optimizations" class="injected"></a>


### Linker Optimizations

 **IL Rewriting**

The linker is now able to rewrite the IL of the bindings libraries, including
it’s own, to [remove extraneous checks for Runtime.Arch](http://spouliot.wordpress.com/2012/02/29/linker-vs-bindings-and-runtime-arch/), checks for
IsDirectBinding and calls to UIApplication.EnsureUIThread (see Cross-thread UI
checks) as well as the IsNewRefcountEnabled and MarkDirty methods.

This means that the decompiled output that you see on the assembly browser
does not actually match what is compiled down in your native code. All of that
code is eliminated.

This removes a lot of checks/branch code (biggest gain) and it also reduce
the size of the executable a bit (e.g. 22 KB for TweetStation).

 **Preserving Types**

A new `--xml` options allow developers to provide their own
descriptors to be preserved. This can include types and methods inside the SDK
assemblies. You can see the [mtouch(1) page](http://docs.go-mono.com/?link=man%3amtouch%281%29) for more details.

 <a name="Async_Touch.Unit" class="injected"></a>


### Async Touch.Unit

Touch.Unit now loads the test suites asynchronously - allowing larger test
suites on devices. This prevents the iOS watchdog from killing the application
if you are using a very large test suite.

 <a name="LINQ_Improvements" class="injected"></a>


### LINQ Improvements

We continue to expand the set of LINQ operations that can be used on
device.

-  It is now possible to use orderby with reference types
-  Join support (#3627)
-  Support for Any on enumerations (#3735)


 <a name="Console_Output" class="injected"></a>


### Console Output

Console (Out and Error) output are now remapped to NSLog.

 <a name="Support_for_creating_Managed_Delegates_from_C_Function_Pointers" class="injected"></a>


### Support for creating Managed Delegates from C Function Pointers

Support to turn unmanaged function pointers into managed delegates using <span><a href="http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.marshal.getdelegateforfunctionpointer%28v=vs.80%29.aspx" target="_blank">Marshal.GetDelegateForFunctionPointer</a>.</span>

For this to work with Mono's static compiler, developers must decorate the
delegate type with the <span>MonoNativeFunctionWrapper</span> attribute, like
this:

```
[MonoNativeFunctionWrapper]
public delegate int SimpleDelegate (int a);
```

 <a name="Binding_Generator:_Delegates_to_Delegates" class="injected"></a>


### Binding Generator: Delegates to Delegates

The binding generator now supports delegates in delegates. This allows
callbacks invoked by Objective-C to pass callbacks to C# that you can then
invoke.

For example:

```
delegate void PostFunc (int value);
delegate void Filter (PostFunc func)

[BaseType (typeof (NSObject)]
interface MyMapReduce {
    [Export ("callbackTakesCallback:")]
    void Run (Filter filterFunc);
}
```

 <a name="Line_Number_Information" class="injected"></a>


### Line Number Information

Native debug builds now contain line number information that allows existing
C tools to map executable code to C# source code.

This is particularly useful when using Instruments and crashes.

 <a name="Optimizations" class="injected"></a>


## Optimizations

 <a name="Code_Generation" class="injected"></a>


### Code Generation

We have improved the way that our generated code accesses Mono's built-in
functionality. This allows the native linker to eliminate unused code and
removes a level of indirection in the code. Savings can be as big as 250k with
simple applications, while larger applications, which require more parts of the
Mono runtime, tend to be about 100k smaller.

 <a name="Common_Crypto" class="injected"></a>


### Common Crypto

MonoTouch will now use the iOS CommonCrypto libraries to provide some of the
functionality exposed by its APIs. This replaces our managed implementations
with the native versions. It is now used for for digest (hash) and symmetric
ciphers, leveraging the hardware acceleration for SHA-1 and AES under the right
circumstances.

 **Size Changes**

The effect of the use of CommonCrypto to replace the managed implementation
reduced the size of the generated binaries.

Our benchmarking application size compiled with LLVM, ARMv7 and in Release
mode is reduced by 99.5KB due to smaller `mscorlib.dll`, `System.Core.dll` and `Mono.Security.dll` assemblies.

The removal of some PRNG internal calls also reduce the application size.
With all other 5.3.x changes the application is 219KB smaller (compared to the
stable version of MonoTouch, 5.2.11) even considering the additional code
required for the new specialized trampolines.

 **Performance Gains**

The performance gains from MonoTouch 5.3.2 and 5.3.3 start at 2.1x and go up
to to 35.4x (the later likely unattainable in real life, an upcoming blog post
will discuss the topic).

 <a name="Specialized_Bridges" class="injected"></a>


### Specialized Bridges

We now use specialized Objective-C to C# bridges instead of the previous
generics trampolines.

This lead to a significant speed increase when going from Objective-C to
Managed code (2-4x speedup, depending on the number and type of arguments to the
method).

The tradeoff is that the executable size is somewhat bigger, but this depends
significantly on the application type. For reference, this change added 49k to
the size to TweetStation.

If you find a bug and need to disable the new trampolines, add `--noregistrar` to the additional `mtouch` arguments and [file a bug](http://bugzilla.xamarin.com/).

 <a name="Fast_String_Marshaling" class="injected"></a>


### Fast String Marshaling

Faster string marshaling: We no longer create temporary objects when passing
strings from C# to Objective-C, increasing the speed to pass strings up to 13
times.

Strings no longer incurr any copying from C# to Objective-C, instead a
zero-copy approach is used.

 <a name="Lightweight_System.Uri" class="injected"></a>


### Lightweight System.Uri

The System.Uri class has gone on a diet. It used to depend on
System.Text.RegularExpressions class to parse Uri, which was heavyweight and
slow. We now have a minimal parser that drops the dependency and is also
faster.

 <a name="MonoTouch_6.0.1" class="injected"></a>


#  [MonoTouch 6.0.1](#MonoTouch_6.0.1)

This is the first maintenance release for 6.0.

 <a name="What's_new:" class="injected"></a>


### What's new:

-  Installer refuse to install on Snow Leopard (10.6)
-  Add several new CoreImage filters
-  Add missing NSThread.IsMain (#7347)
-  Add missing UIFont fontWithSize (#7368)
-  Add CAMediaTimingFunction.GetControlPoint
-  Obsolete some default constructors in CoreMotion and CoreLocation


 <a name="Bug_fixes:" class="injected"></a>


### Bug fixes:

-  Do not link with MediaToolbox to avoid crash in iOS 5.1 simulator (#6513, #7320) 
-  Fix GetNetworkInterfaces to work with Personal Hotspot (#7329)
-  Fix UIColor.ToString to never throw an exception (#7362)
-  Fix TimeZoneLocal.Info caching
-  Fix NSUrl binding for initWithString:relativeToURL:
-  Re-introduce removed API in MonoTouch.ObjCRuntime.Messaging


 <a name="API_changes:" class="injected"></a>


### API changes:

You can check the detailed list of API changes from MonoTouch [6.0.0 to 6.0.1](/releases/ios/api_changes/from_6.0.0_to_6.0.1).

&nbsp;

 <a name="MonoTouch_6.0.2" class="injected"></a>


#  [MonoTouch 6.0.2](#MonoTouch_6.0.2)

This releases fixes a few outstanding issues in our HTTP stack

 <a name="What's_new:" class="injected"></a>


### What's new:

-  Performance improvement for Math.Sqrt with LLVM compilers
-  Threadpool notification switched to the default implementation from kqueue. 


 <a name="Bug_fixes:" class="injected"></a>


### Bug fixes:

 <a name="Web_Services,_Serialization_and_WCF_Bug_Fixes" class="injected"></a>


#### Web Services, Serialization and WCF Bug Fixes

-  WCF NRE on invalid HTTP methods [#1340]
-  WCF DuplexClientBase channel initialization [#4511]
-  WebService without a &lt;output&gt; [#6041]&lt;/output&gt;
-  WCF Contract interface inheritance [#6187]
-  WCF NRE on missing client certificate [#6201]
-  SoapFormatter culture reset issue wrt events [#6489]
-  WCF Correctly handle derived FaultExceptions [#7177]
-  Collection serialization fixes and improvements [#7299]
-  BinaryFormatter serialization of generic arrays [#5935]
-  WCF Enable custom headers [#6515]


 <a name="Http_Stack_fixes:" class="injected"></a>


#### Http Stack fixes:

-  Always send HTTP headers for WebDAV methods [#5655]
-  Cookie, set port only for version 1 [#6122]
-  WebRequest returns result in another thread [#7200]
-  Fix Cookie regression in same-origin-check [#7424]
-  WebClient.*Async() now correctly builds the query string [#5899]


 <a name="General_fixes:" class="injected"></a>


#### General fixes:

-  Fix the computation of TLS reference bitmaps [#6755]
-  CIContext.CreateCGImage leaks returned CGImage [#7117]
-  Fix CFB for Rijndael / AES when buffers != block size [#7193]
-  Add support for [UnmanagedFunctionPointer] attribute [#7385]
-  Use of Appearance/TextShadow causing crash [#7443, #7446]
-  Registrar fixes for case sensitive file system


 <a name="API_changes:" class="injected"></a>


### API changes:

You can check the detailed list of API changes from MonoTouch [6.0.1 to 6.0.2](/releases/ios/api_changes/from_6.0.1_to_6.0.2).

 <a name="MonoTouch_6.0.3" class="injected"></a>


#  [MonoTouch 6.0.3](#MonoTouch_6.0.3)

This is a hot-fix release.

 <a name="Bug_fixes:" class="injected"></a>


### Bug fixes:

* Temporarily disable LLVM optimization (added in 6.0.2) for Math.Sqrt

* Linker support for System.Data.Services.Client reflection usage (#7354)

* Further fix wrt MediaToolsbox and iOS5.x simulators (#7380)

* Registration of generic types reports (MT4112) are now warnings (#7547)

 <a name="API_Changes:" class="injected"></a>


### API Changes:

You can check the detailed list of API changes from MonoTouch [6.0.2 to 6.0.3](/releases/ios/api_changes/from_6.0.2_to_6.0.3).

 <a name="MonoTouch_6.0.4" class="injected"></a>


#  [MonoTouch 6.0.4](#MonoTouch_6.0.4)

This release re-enables the LLVM optimization for Math.sqrt that was disabled
in 6.0.3. There are no additional API changes.

 <a name="MonoTouch_6.0.5" class="injected"></a>


#  [MonoTouch 6.0.5](#MonoTouch_6.0.5)

 <a name="New_features_and_API" class="injected"></a>


### New features and API

-  Support for ARMv7s (CPU used in the new iPhone5)
-  Hide the fact iOS6 does not return UIImage from UIPasteboard.Images [#7442] 
-  Add System.ComponentModel.BindingList&lt;t&gt; [#5673]&lt;/t&gt;
-  Allow custom ServicePointManager validation based on X509Chain [#7245]
-  New TLS support for 'server_name' extension [#7664]
-  New NSFetchedResultController (CoreData) support [#7769]
-  Add AVCaptureDevice.IsExposureModeSupported method [#7791]
-  Add NSIndexPath.Item property [#7806]
-  New bindings for SecCertificate, SecPolicy and SecTrust
-  New CTFont's FontFeatureGroup
-  New AudioToolbox bindings for AudioQueue, AudioBufferList...
-  Autorelease automatically in UIImage.AsPNG|JPEG to avoid high memory usage in loops. 


 <a name="Bug_fixes" class="injected"></a>


### Bug fixes

-  Fix debugger exception with `.ctor' not found in type `CollectionDebuggerView`1' [#1873] 
-  Fix generator possible confusion with namespace and type names [#5538]
-  Make registar to work with hidden inherited members [#6096]
-  Only use IPHONEOS_DEPLOYMENT_TARGET when no deployment target is available [#7380] 
-  Fix typo in UIView.TranslatesAutoresizingMaskIntoConstraints [#7693]
-  Fix iOS 4.3 compatibility UINavigationController [#7742]
-  Fix AVCaptureConnection.InputPorts typo [#7764]
-  Fix UICollectionViewDelegate base class [#7784]
-  Fix CGImageDestination crash when invalid ITU are used [#7793]
-  Fix AOT issue with multi-dimensional array [#7848]
-  Mark events as [Obsolete] when the Delegate methods are obsoleted [#7882] 
-  Fix refcount issue in ABAddressBook UI controllers [#7887]
-  Fix ExtAudioFile unmanaged calls involving AudioBufferList [#7906]
-  Fix Regular Expression regression [reverting fix for #2663]
-  Running individual test cases in Touch.Unit now update the UI
-  Fix CFNetwork object lifecycle problem in CFSocketAddress


 <a name="API_changes" class="injected"></a>


### API changes

You can check the detailed list of API changes from MonoTouch [6.0.4 to 6.0.5](/releases/ios/api_changes/from_6.0.4_to_6.0.5).

 <a name="" class="injected"></a>


<h1 id="6">
  <a href="#MonoTouch_6.0.6">MonoTouch 6.0.6</a>
</h1>

This release adds iOS 6.0.1 support on top of MonoTouch 6.0.5. There are no
additional API changes.

 <a name="" class="injected"></a>


<h1 id="7">
  <a href="#MonoTouch_6.0.7">MonoTouch 6.0.7</a>
</h1>

This beta release of MonoTouch explores a new way of releasing objects when
developers use Dispose. For more information see [http://bit.ly/monotouch-experimental-dispose](http://bit.ly/monotouch-experimental-dispose).

 <a name="" class="injected"></a>


<h1 id="8">
  <a href="#MonoTouch_6.0.8">MonoTouch 6.0.8</a>
</h1>

 <a name="Runtime_Features" class="injected"></a>


### Runtime Features

 **Runtime Trampolines**: It is no longer necessary to manually
manage trampolines in the Mono runtime, trampolines are now handled
dynamically.

 **New Dispose Semantics**: We have modified the behavior of
Dispose () on subclasses of NSObject to cope with scenarios where users
explicitly called Dispose() on objects that were currently held by unmanaged
code.&nbsp;&nbsp; This had the undesirable effect of producing errors when
unmanaged code used or cleaned up the resources but the managed object had been
destroyed.&nbsp;&nbsp; This fixes bugs #2886, #6000 and #8055: [http://bit.ly/monotouch-experimental-dispose](http://bit.ly/monotouch-experimental-dispose)

 **Generic Methods exported to Objective-C**: the compiler will
now report a warning (MT4113 warning) and an error (MT4114) when generic methods
are exported to Objective-C.&nbsp;&nbsp; Previously the runtime silently
exported the methods and silently routed the callbacks to one of the
methods.

 **Marshaling of Objective-C exceptions for un-archiving**: this
addresses bug #7696

 <a name="API_Bindings" class="injected"></a>


### API Bindings

 **New AudioToolbox’s AudioBuffers type**: the AudioBuffers
type replaces the old AudioBufferList structure to represent the collections of
AudioBuffers.&nbsp;&nbsp; Unlike AudioBufferList which was hard-coded to support
marshalling of two AudioBuffer structures, the new version supports one or more
AudioBuffers.&nbsp;&nbsp; Various AudioToolbox APIs have been updated to take
advantage of this lighter and better representation for AudioBuffer lists.

 **UIKit and OpenGL screen capture APIs**: convenience routines
to capture the contents of the screen while running with UIKit or OpenGL are now
provided.

UIKit applications

 *var screenshot = UIScreen.MainScreen.Capture ();*

GLKit applications

 *var screenshot = iPhoneOSGameView.Capture ();*

UIKit’s UIImage.Scale now uses a Retina-capable API (#8549)

 <a name="Binding_Generator" class="injected"></a>


### Binding Generator

The binding generator now support setting fields in unmanaged libraries, in
addition to lookinp up values.&nbsp;&nbsp; Merely declare a setter for a [Field]
in your API definition.&nbsp;&nbsp; This fixes #7970.

 <a name="Other" class="injected"></a>


### Other

-  Allow manually starting MonoTouch application on devices when no matching DeveloperDiskImage.dmg can be found to match a device. 
-  NTLMv2 session and authentication support for WebClient/HttpWebRequest[#7258] 
-  CFProxy support for NetworkCredentials


 <a name="Bug_fixes" class="injected"></a>


### Bug fixes

-  DELETE can have a request stream [#3276]
-  Fix abort race condition in WebConnection.ReadDone() [#6329]
-  Allow installing application to device from directories with special characters [#7180] 
-  Fix web proxy error when connection is reused [#7599]
-  Fix deserialization of empty dictionary (System.Runtime.Serialization) [#7957] 
-  Allow roundtripping CBUUID.FromString(uuid.ToString()) [#7986]
-  Avoid throwing exceptions from WeakReference.IsAlive after finalization when the underlying GCHandle is already finalized [#8072] 
-  Allow null image for UIStepper and UIBarButtonItem.SetBackgroundImage [#8086] 
-  Fix AVPlayerItem.Tracks property [#8288]
-  Add missing UITableViewSource members [#8298]
-  Fix metadata table to allow building Reactive Extensions [#8320]
-  Allow null characteristics on DiscoverIncludedServices and DiscoverCharacteristics [#8349] 
-  Remove server_name extension from SSLv3 (only TLSv1) [#8312] and disallow IP addresses [#8553] 
-  Fix native linker flags when a library is removed from the build [#8365] &nbsp; 
-  Fix BindingList&lt;T&gt; with ListChangedType.ItemChanged [#8366]
-  Handle instances implementing INativeObject from NSObject.FromObject [#8458] 
-  Don't free the GCHandle until AudioQueueDispose has been called [#8465]
-  Fix LLVM backend [#8502]
-  Allow null context in NSAttributeString GetBoundingRect and DrawString [#8543] 
-  Pass the right scheduler for worker number calculation [#8559] Add ABPersonViewController allowsActions [#8551] 
-  Allow null attributes on some NSFileManager API [#8703]
-  Fix GKFriendRequestComposeViewController.ComposeViewDelegate binding to wrap WeakComposeViewDelegate [MonoTouch.Dialog] Bring Entry size fix for iPad and resizing [#91] 
-  Support [OnSerializing] in System.Runtime.Serialization.Json
-  Many missing property setters were added.


 <a name="MonoTouch_6.0.9" class="injected"></a>


## MonoTouch 6.0.9

 <a name="New_Features" class="injected"></a>


### New Features

-  New [Advice] attribute, similar to [Obsolete] but without compiler warnings/errors
-  Several AudioToolbox API enhancements
-  Added NSObject PerformSelector and CancelPreviousPerformRequest overloads
-  Added CADisplayLink.Duration property
-  Added strongly-typed methods for GLKTextureLoader
-  Added GLKTextureLoader .GrayscaleAsAlpha property
-  Added bindings for NSPropertyListSerialization
-  Added bindings for DispatchGroup
-  [AOT] Added support for pointer types [#8766]
-  [WCF] Implement missing WsdlImporter pieces
-  [WCF] Fixed accessibility of ClientBase.ChannelBase
-  [WCF] Support embedded elements
-  [MonoTouch.Dialog] Added BackgroundColor to DateTimeElement
-  [btouch] Support for NSString setters in bound fields
-  [mtouch] Added support for specifying symbols to not strip.
-  [mtouch] Linker support for [assembly:Preserve] attribute [#7009]
-  [mtouch] Linker support for [assembly:LinkerSafe] attribute


 <a name="Fixes" class="injected"></a>


### Fixes

-  Avoid ObjectCollectedExceptions during debugging [#1446, [#2246](http://forums.xamarin.com/search?Search=%232246&amp;Mode=like) ,#6918]
-  Workaround for Parallel.ForEach AOT limitation [#8106]
-  Fixed overflow correctly in Timer to avoid spinning [#8782]
-  Fixed MemoryMappedFile.CreateFromFile in simulator [#8786]
-  UITableView.DequeueReusable[Cell|HeaderFooterView] returning NSObject [#8941]
-  Fixed support for large offsets in the OP_CALL_MEMBASE opcodes on ARM [#9087]
-  Fixed XmlSerialization not properly deserializing a List [#9193]
-  Fixed crash when inheriting from UIWebView [#9261]
-  Fixed PtrToStructure/StructureToPtr wrapperswhen using full-AOT [#9408]
-  Capped NSDate to DateTime.Min|MaxValue when doing implicit conversions [#9527]
-  Fixed segfault in fieldref_encode_signature [#9531]
-  [sgen] Avoid a race condition if we suspend in the middle [#9590]
-  Fixed GC issue when used under Instruments
-  Fixed CMTimeMapping structure
-  Several bindings (Foundation, AVFoundation, UIKit) were also fixed
-  [MonoTouch.Dialog] Fixed EntryElements to use a separate key for password entries
-  [MonoTouch.Dialog] Fixes to ImageLoader URL encoding and queues
-  [MonoTouch.Dialog] Fixed DatePicker location on iPad devices


 <a name="API_Differences" class="injected"></a>


### API Differences

Here is the detailed list of [API changes between 6.0.8 and 6.0.9](/releases/ios/API_Changes/from_6.0.8_to_6.0.9).

 <a name="MonoTouch_6.0.10" class="injected"></a>


## MonoTouch 6.0.10

This release introduces support for iOS 6.1 released on January 28th 2013.

 <a name="New_Features" class="injected"></a>


### New Features

-  Added the new iOS 6.1 APIs MKLocalSearchRequest and MKLocalSearchResponse.
-  New  [MapKitSearch](https://github.com/xamarin/monotouch-samples/tree/master/MapKitSearch) sample published.


 <a name="API_Differences" class="injected"></a>


### API Differences

Here is the detailed list of [API changes between 6.0.9 and 6.0.10](/ios/releases/API_Changes/from_6.0.9_to_6.0.10).
