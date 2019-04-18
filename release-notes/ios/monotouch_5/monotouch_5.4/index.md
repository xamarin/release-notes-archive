---
id: 4E2D30AC-F562-F71B-1824-255C0A26E3F4
title: "MonoTouch 5.4"
---

<a name="Notice" class="injected"></a>


# Notice

MonoTouch 5.4.x will be the last versions to support Mac OS X 10.6 (Snow
Leopard). Future versions (5.5+) will require either OS X 10.7 (Lion) or OS X 10.8
(Mountain Lion).

 <a name="New_Samples" class="injected"></a>


# New Samples

The following samples show some of the new features in MonoTouch 5.4:

-   [AudioQueueOfflineRenderDemo](https://github.com/xamarin/monotouch-samples/tree/master/AudioQueueOfflineRenderDemo)   
    
  *An example demonstrating the Audio Queue offline rendering API. The sample produces LPCM output from an mp3 file, which is written to disk as a .caf file then subsequently played back to show the offline rendering is working as expected.*   
    
 
-   [BubbleCell](https://github.com/xamarin/monotouch-samples/tree/master/BubbleCell)   
    
  *This example has been update to show how to use the new strongly typed notifications.*   
    
 
-   [CoreImage](https://github.com/xamarin/monotouch-samples/tree/master/CoreImage)   
    
  *The sample has been updated to become a regression test suite for CoreImage effects.*   
    
 
-   [CoreMidiSample](https://github.com/xamarin/monotouch-samples/tree/master/CoreMidiSample)   
    
  *This sample shows how to probe the MIDI devices connected to your iOS device and send tones to them*   
    
 
-   [CustomInputStream](https://github.com/xamarin/monotouch-samples/tree/master/CustomInputStream)   
    
  *This sample illustrates how to derive from NSInputStream and create subclass that is toll-free bridged to CFReadStream that can be used with NSMutableUrlRequest.*   
    
 
-   [CustomPropertyAnimation](https://github.com/xamarin/monotouch-samples/tree/master/CustomPropertyAnimation)   
    
  *This example shows how CoreAnimation can be used to animate arbitrary C# properties.*   
    
 
-   [GLCameraRipple](https://github.com/xamarin/monotouch-samples/tree/master/GLCameraRipple)   
    
  *This sample shows how to use  [MonoTouch.GLKit](http://iosapi.xamarin.com/?link=N%3aMonoTouch.GLKit)to render OpenGL frames, AVFoundation to fetch live video from the camera and OpenTK's API to load a couple of shaders that simulate a water ripple effect when the user touches the display.*   
    
  *This uses the  [CVOpenGLESTextureCache](http://iosapi.xamarin.com/?link=T%3aMonoTouch.CoreVideo.CVOpenGLESTextureCache)class which was introduced in iOS 5.0 that binds CoreVideo buffers to OpenGL textures.*   
    
 
-   [ImageProtocol](https://github.com/xamarin/monotouch-samples/tree/master/ImageProtocol)   
    
  *This sample shows how to register a custom NSUrlProtocol.*   
    
 
-   [RosyWriter](https://github.com/xamarin/monotouch-samples/tree/master/RosyWriter)   
    
  *This sample shows how to use AVFoundation, GLKit, Grand Central Dispatch queues, CoreVideo and ALAssets. It captures video, process video frames (in this example, we remove the "green" component from each frame turning images rosy), show the resulting data and optionally save the resulting video and audio into the user's Photo storage.*   
    
 
-   [SimpleTextInput](https://github.com/xamarin/monotouch-samples/tree/master/SimpleTextInput) ,  [GestureRecognizers](https://github.com/xamarin/monotouch-samples/tree/master/Touches_GestureRecognizers) ,  [Touch](https://github.com/xamarin/monotouch-samples/tree/master/Touch)   
    
  *These samples were updated to show how to use the new simpler to use UIGestureRecognizer APIs.*   
    
 


 <a name="New_Library_Features" class="injected"></a>


# New Library Features

 <a name="Cross-thread_UI_Checks" class="injected"></a>


## Cross-thread UI Checks

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


## CoreMIDI APIs

This release comes with a complete binding to the CoreMIDI APIs on iOS and
MacOS X.

The new [CoreMidiSample](https://github.com/xamarin/monotouch-samples/tree/master/CoreMidiSample) shows how to use it.

 <a name="Strongly_Typed_Notifications" class="injected"></a>


## Strongly Typed Notifications

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


## UIGestureRecognizer

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


## OpenTK

There is now a new OpenTK-1.0 assembly which provides the OpenTK 1.0 API.

The reason for this change is that the OpenTK 1.0 API is not backwards
compatible with our existing OpenTK.dll. In the future we will keep OpenTK.dll
for backwards compatibility, while OpenTK-1.0.dll should be used in new
projects. See the API differences document for details on the actual
changes.

 <a name="" class="injected"></a>


<h2 dir="ltr">
  GLKit
</h2>

GLKViewController now exposes an "Update" method that is invoked to update
the display. This allows GLKit code to be smaller and not require a
GLKViewControllerDelegate implementation to exist.

 <a name="" class="injected"></a>


<h2 dir="ltr">
  CoreVideo
</h2>

Added CVOpenGLTextureCache support that allows binding CoreVideo pixel
buffers to OpenGL textures.

There are two new samples that illustrate the CoreVideo's OpenGLTextureCache: [GLCameraRipple](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/GLCameraRipple) and [RosyWriter](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/RosyWriter).

 <a name="NSUrlProtocol" class="injected"></a>


## NSUrlProtocol

It’s now possible to use `NSUrlProtocol` to register custom url
protocols. A sample has been created to show how ( [ImageProtocol](https://github.com/xamarin/monotouch-samples/tree/master/ImageProtocol)).

 <a name="Animating_C#_properties_with_CoreAnimation" class="injected"></a>


## Animating C# properties with CoreAnimation

C# properties that have been flagged with the [Export] attribute can now be
animated by CoreAnimation.

A sample [has been added](https://github.com/xamarin/monotouch-samples/tree/master/CustomPropertyAnimation) that shows how it works

 <a name="UIAppearance_support" class="injected"></a>


## UIAppearance support

Based on new documentation from Apple, the UISlider class now has support for
UIAppearance and more properties have been added to existing types that
supported UIAppearance.

 <a name="New_Tooling_Features" class="injected"></a>


# New Tooling Features

 <a name="Parameters_to_Applications" class="injected"></a>


## Parameters to Applications

You can now pass parameters to applications by adding the parameters in the [Run/General section](http://screencast.com/t/YPg9Hy0e) in the project preferences as well as setting environment variables.
You can use this to set environment variables in your application as well, in
particular you can use this to control the behavior of the Mono runtime by using
the options documented in the mono manual page.

 <a name="Linker_Optimizations" class="injected"></a>


## Linker Optimizations

 <a name="IL_Rewriting" class="injected"></a>


### IL Rewriting

The linker is now able to rewrite the IL of the bindings libraries, including
it’s own, to [remove extraneous checks for Runtime.Arch](http://spouliot.wordpress.com/2012/02/29/linker-vs-bindings-and-runtime-arch/), checks for
IsDirectBinding and calls to UIApplication.EnsureUIThread (see Cross-thread UI
checks) as well as the IsNewRefcountEnabled and MarkDirty methods.

This means that the decompiled output that you see on the assembly browser
does not actually match what is compiled down in your native code. All of that
code is eliminated.

This removes a lot of checks/branch code (biggest gain) and it also reduce
the size of the executable a bit (e.g. 22 KB for TweetStation).

 <a name="Preserving_Types" class="injected"></a>


### Preserving Types

A new `--xml` options allow developers to provide their own
descriptors to be preserved. This can include types and methods inside the SDK
assemblies. You can see the [mtouch(1) page](http://docs.go-mono.com/?link=man%3amtouch(1)) for more details.

 <a name="Async_Touch.Unit" class="injected"></a>


## Async Touch.Unit

Touch.Unit now loads the test suites asynchronously - allowing larger test
suites on devices. This prevents the iOS watchdog from killing the application
if you are using a very large test suite.

 <a name="" class="injected"></a>


<h2 dir="ltr">
  LINQ Improvements
</h2>

We continue to expand the set of LINQ operations that can be used on
device.

-  It is now possible to use orderby with reference types
-  Join support (#3627)
-  Support for Any on enumerations (#3735)


 <a name="Console_Output" class="injected"></a>


## Console Output

Console (Out and Error) output are now remapped to NSLog.

 <a name="Support_for_creating_Managed_Delegates_from_C_Function_Pointers" class="injected"></a>


## Support for creating Managed Delegates from C Function Pointers

Support to turn unmanaged function pointers into managed delegates using <span><a href="http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.marshal.getdelegateforfunctionpointer(v=vs.80).aspx" target="_blank">Marshal.GetDelegateForFunctionPointer</a>.</span>

For this to work with Mono's static compiler, developers must decorate the
delegate type with the <span>MonoNativeFunctionWrapper</span> attribute, like
this:

```
[MonoNativeFunctionWrapper]
public delegate int SimpleDelegate (int a);
```

   


   


 <a name="Binding_Generator:_Delegates_to_Delegates" class="injected"></a>


## Binding Generator: Delegates to Delegates

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


## Line Number Information

Native debug builds now contain line number information that allows existing
C tools to map executable code to C# source code.

This is particularly useful when using Instruments and crashes.

 <a name="Optimizations" class="injected"></a>


# Optimizations

 <a name="Code_Generation" class="injected"></a>


## Code Generation

We have improved the way that our generated code accesses Mono's built-in
functionality. This allows the native linker to eliminate unused code and
removes a level of indirection in the code. Savings can be as big as 250k with
simple applications, while larger applications, which require more parts of the
Mono runtime, tend to be about 100k smaller.

 <a name="Common_Crypto" class="injected"></a>


## Common Crypto

MonoTouch will now use the iOS CommonCrypto libraries to provide some of the
functionality exposed by its APIs. This replaces our managed implementations
with the native versions. It is now used for for digest (hash) and symmetric
ciphers, leveraging the hardware acceleration for SHA-1 and AES under the right
circumstances.

 <a name="Size_Changes" class="injected"></a>


### Size Changes

The effect of the use of CommonCrypto to replace the managed implementation
reduced the size of the generated binaries.

Our benchmarking application size compiled with LLVM, ARMv7 and in Release
mode is reduced by 99.5KB due to smaller `mscorlib.dll`, `System.Core.dll` and `Mono.Security.dll` assemblies.

The removal of some PRNG internal calls also reduce the application size.
With all other 5.3.x changes the application is 219KB smaller (compared to the
stable version of MonoTouch, 5.2.11) even considering the additional code
required for the new specialized trampolines.

 <a name="Performance_Gains" class="injected"></a>


### Performance Gains

The performance gains from MonoTouch 5.3.2 and 5.3.3 start at 2.1x and go up
to to 35.4x (the later likely unattainable in real life, an upcoming blog post
will discuss the topic).

 <a name="Specialized_Bridges" class="injected"></a>


## Specialized Bridges

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


## Fast String Marshaling

Faster string marshaling: We no longer create temporary objects when passing
strings from C# to Objective-C, increasing the speed to pass strings up to 13
times.

Strings no longer incurr any copying from C# to Objective-C, instead a
zero-copy approach is used.

 <a name="Lightweight_System.Uri" class="injected"></a>


## Lightweight System.Uri

The System.Uri class has gone on a diet. It used to depend on
System.Text.RegularExpressions class to parse Uri, which was heavyweight and
slow. We now have a minimal parser that drops the dependency and is also
faster.

 <a name="API_Changes" class="injected"></a>


# API Changes

You can check the detailed list of API changes from MonoTouch [5.2.13 to 5.4.0](/releases/ios/api_changes/from_5.2.13_to_5.4.0).

 <a name="MonoTouch_5.4.1" class="injected"></a>


#  [MonoTouch 5.4.1](#MonoTouch_5.4.1)

This is the first maintenance release for 5.4.

 <a name="Bug_fixes:" class="injected"></a>


## Bug fixes:

-  WCF fix for net.tcp (bug # [275](https://bugzilla.xamarin.com/show_bug.cgi?id=275) ) 
-  PLINQ support on devices (bug # [1922](https://bugzilla.xamarin.com/show_bug.cgi?id=1922) ) 
-  State corruption in ReaderWriterLockSlim (fix # [6635](https://bugzilla.xamarin.com/show_bug.cgi?id=6635) ) 
-  LLVM fix with nested clauses (bug # [6650](https://bugzilla.xamarin.com/show_bug.cgi?id=6650) ) 
-  Timeout in BlockingCollection (bug # [6732](https://bugzilla.xamarin.com/show_bug.cgi?id=6732) ) 
-  Thread Local Storage fix (bug # [6755](https://bugzilla.xamarin.com/show_bug.cgi?id=6755) ) 
-  Fix VBByRefStr marshaling (bug # [6908](https://bugzilla.xamarin.com/show_bug.cgi?id=6908) ) 
-  Two-keys (128 bits) TripleDES support fixed (bug # [6967](https://bugzilla.xamarin.com/show_bug.cgi?id=6967) ) 
-  Allow non-MacRoman characters on Console.Write* (bug # [6977](https://bugzilla.xamarin.com/show_bug.cgi?id=6977) ) 
-  NSTimer fix for Steema TeeChart (bug # [6987](https://bugzilla.xamarin.com/show_bug.cgi?id=6987) ) 
-  Registrar issue with CoreAnimation types (bug # [7060](https://bugzilla.xamarin.com/show_bug.cgi?id=7060) ) 
-  CoreBluetooth API fix (bug # [7069](https://bugzilla.xamarin.com/show_bug.cgi?id=7069) ) 
-  MKOverlayView helper methods are thread-safe (bug # [7036](https://bugzilla.xamarin.com/show_bug.cgi?id=7036) ) 
-  Added missing AVPlayerItem.Duration property
-  System.Net.Cookies fixes (closer to .NET 4.5)
-  sgen fixes


 <a name="API_Changes" class="injected"></a>


## API Changes

You can check the detailed list of API changes from MonoTouch [5.4.0 to 5.4.1](/releases/ios/api_changes/from_5.4.0_to_5.4.1).
