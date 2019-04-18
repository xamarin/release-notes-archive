---
id: 9EF6D1BE-652F-D130-BD03-AE58FE226F14
title: "MonoTouch 5.3"
---

<a name="Cross-thread_UI_Checks" class="injected"></a>


## Cross-thread UI Checks

Many developers creating multi-threaded applications and using Grand Central
Dispatch have historically called methods on the UI thread from a background
thread accidentally corrupting the state of UIKit.

This leads to strange behavior in the best case and to hard to track down
crashes in the worst case.

MonoTouch will now check calls made to UIKit APIs that are not thread safe
are only performed from the main thread. This will help developer identify parts
of their code that should be using BeginInvokeOnMainThread.

The check is only performed on debug builds and is stripped out from release
binaries. This behavior can be changed by using the --force-thread-check and
--disable-thread-check to mtouch.

You can alter the behavior at runtime for debug builds by setting the
UIApplication.CheckForIllegalCrossThreadCalls which defaults to true.

 <a name="Parameters_to_Applications" class="injected"></a>


## Parameters to Applications

You can now pass parameters to applications by adding the parameters in the [Run/General section](http://screencast.com/t/YPg9Hy0e) in the project preferences as well as setting environment variables.
You can use this to set environment variables in your application as well, in
particular you can use this to control the behavior of the Mono runtime by using
the options documented in the mono manual page.

 <a name="CoreMIDI_APIs" class="injected"></a>


## CoreMIDI APIs

This release comes with a complete binding to the CoreMIDI APIs on iOS and
MacOS X.

 <a name="UIGestureRecognizer" class="injected"></a>


## UIGestureRecognizer

The API now allows a delegate that will be invoked upon a match to be passed
directly in the constructor instead of using the AddTarget method later or using
selectors/objects.

 <a name="Linker_Updates" class="injected"></a>


## Linker Updates

The linker is now able to rewrite the IL of the bindings libraries, including
it’s own, to [remove extraneous checks for Runtime.Arch](http://spouliot.wordpress.com/2012/02/29/linker-vs-bindings-and-runtime-arch/) and calls to
UIApplication.EnsureUIThread (see Cross-thread UI checks) [ as well as the
IsNewRefcountEnabled and MarkDirty methods.

 <a name="OpenTK" class="injected"></a>


## OpenTK

There is now a new OpenTK-1.0 assembly which provides the OpenTK 1.0 API. The
reason for this change is that the OpenTK 1.0 API is not backwards compatible
with our existing OpenTK.dll. In the future we will keep OpenTK.dll for
backwards compatibility, while OpenTK-1.0.dll should be used in new projects.
See the API differences document for details on the actual changes.

 <a name="API_Changes" class="injected"></a>


## API Changes

You can review the [API changes from MonoTouch 5.2.5 to MonoTouch 5.3.0](/releases/ios/api_changes/from_5.2.5_to_5.3.0) in our API differences page.

 []()

 <a name="MonoTouch_5.3.2" class="injected"></a>


# MonoTouch 5.3.2

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

This release incorporates the same set of bug fixes that were done for
MonoTouch 5.2.10.

 <a name="" class="injected"></a>


<h2 dir="ltr">
  Code Generation Optimizations
</h2>

We have improved the way that our generated code accesses Mono's built-in
functionality. This allows the native linker to eliminate unused code and
removes a level of indirection in the code. Savings can be as big as 250k with
simple applications, while larger applications, which require more parts of the
Mono runtime, tend to be about 100k smaller.

 <a name="" class="injected"></a>


<h2 dir="ltr">
  LINQ Improvements
</h2>

We continue to expand the set of LINQ operations that can be used on
device.

-  It is now possible to use orderby with reference types
-  Join support (#3627)
-  Support for Any on enumerations (#3735)


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
buffers to OpenGL textures, see the samples in the monotouch-5.4 branch:   
   
 [ <span>https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4</span>](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4)

For example the GLCameraRipple

 [https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/GLCameraRipple](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/GLCameraRipple)

 []()

 <a name="MonoTouch_5.3.3" class="injected"></a>


# MonoTouch 5.3.3

 <a name="Optimizations" class="injected"></a>


## Optimizations

 <a name="Common_Crypto" class="injected"></a>


### Common Crypto

MonoTouch will now use the iOS CommonCrypto libraries to provide some of the
functionality exposed by its APIs. This replaces our managed implementations
with the native versions. It is now used for for digest (hash) and symmetric
ciphers, leveraging the hardware acceleration for SHA-1 and AES under the right
circumstances.

 <a name="Size_Changes" class="injected"></a>


##### Size Changes

The effect of the use of CommonCrypto to replace the managed implementation
reduced the size of the generated binaries.

Our benchmarking application size compiled with LLVM, ARMv7 and in Release
mode is reduced by 99.5KB due to smaller `mscorlib.dll`, `System.Core.dll` and `Mono.Security.dll` assemblies.

The removal of some PRNG internal calls also reduce the application size.
With all other 5.3.x changes the application is 219KB smaller (compared to the
stable version of MonoTouch, 5.2.11) even considering the additional code
required for the new specialized trampolines.

 <a name="Performance_Gains" class="injected"></a>


##### Performance Gains

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

If you find a bug and need to disable the new trampolines, add `--noregistrar` to the additional `mtouch` arguments and [file a bug](http://bugzilla.xamarin.com).

 <a name="Improvements" class="injected"></a>


## Improvements

Console (Out and Error) output is now remapped to NSLog

Faster string marshaling: We no longer create temporary objects when passing
strings from C# to Objective-C, increasing the speed to pass strings up to 13
times.

Touch.Unit now loads the test suites asynchronously - allowing larger test
suites on devices (i.e. the iOS watchdog won’t interrupt their loading)

It’s now possible to use `NSUrlProtocol` to register custom url
protocols. A sample has been created to show how ( [ImageProtocol](https://github.com/xamarin/monotouch-samples/tree/master/ImageProtocol)).

Properties [Export]ed can now be animated by CoreAnimation. A sample [has been added](https://github.com/xamarin/monotouch-samples/tree/master/CustomPropertyAnimation).

 <a name="Linker_Optimizations" class="injected"></a>


## Linker Optimizations

The linker will now optimize the IsDirectBinding checks, from generated
bindings when a type is never subclassed in the application.

This removes a lot of checks/branch code (biggest gain) and it also reduce
the size of the executable a bit (e.g. 22 KB for TweetStation).

A new `--xml` options allow developers to provide their own
descriptors to be preserved. This can include types and methods inside the SDK
assemblies.

 <a name="Strongly_Typed_Notifications" class="injected"></a>


## Strongly Typed Notifications

MonoTouch now exposes a nested class "Notifications" that allows developers
to add observers to iOS notifications using strong types. The strongly typed
"AddObserver" method allows developers to take the guesswork out and reduce
their trips to the documentation. With strongly typed notifications the
parameters and their types are available to you from the IDE. This is how they
work:

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

 <a name="CoreMIDI_updates" class="injected"></a>


### CoreMIDI updates

The MidiObject class no longer exposes all of the properties that are common
to all of its subclasses. Instead specific properties are exposed on each kind
of MidiObject, this makes the API easier to navigate from the IDE, and
eliminates ugly displays in the debugger.   
   
   
   
 See our new [CoreMidiSample](https://github.com/xamarin/monotouch-samples/tree/monotouch-5.4/CoreMidiSample)

 <a name="API_Changes" class="injected"></a>


## API Changes

For a detailed list of the changes in the API, see our detailed [API changes from 5.3.2 to 5.3.3](/releases/ios/api_changes/from_5.3.2_to_5.3.3).

 []()

 <a name="MonoTouch_5.3.4" class="injected"></a>


# MonoTouch 5.3.4

 <a name="API_Changes" class="injected"></a>


### API Changes

For a detailed list of the changes in the API, see our detailed [API changes from 5.3.3 to 5.3.4](/releases/ios/api_changes/from_5.3.3_to_5.3.4).

 <a name="Bug_fixes" class="injected"></a>


### Bug fixes

The following bugs have been fixed:

-   []() [#3668](https://bugzilla.xamarin.com/show_bug.cgi?id=3668) 
-   [#3969](https://bugzilla.xamarin.com/show_bug.cgi?id=3969) 
-   [#4587](https://bugzilla.xamarin.com/show_bug.cgi?id=4587) 
-   [#4677](https://bugzilla.xamarin.com/show_bug.cgi?id=4677) 
-   [#4678](https://bugzilla.xamarin.com/show_bug.cgi?id=4678) 
-   [#4695](https://bugzilla.xamarin.com/show_bug.cgi?id=4695) 
-   [#4715](https://bugzilla.xamarin.com/show_bug.cgi?id=4715) 
-   [#4717](https://bugzilla.xamarin.com/show_bug.cgi?id=4717) 
-   [#4736](https://bugzilla.xamarin.com/show_bug.cgi?id=4736) 
-   [#4784](https://bugzilla.xamarin.com/show_bug.cgi?id=4784) 
-   [#4792](https://bugzilla.xamarin.com/show_bug.cgi?id=4792) 
-   [#4811](https://bugzilla.xamarin.com/show_bug.cgi?id=4811) 
-   [#4834](https://bugzilla.xamarin.com/show_bug.cgi?id=4834) 
-   [#4854](https://bugzilla.xamarin.com/show_bug.cgi?id=4854) 
-   [#4856](https://bugzilla.xamarin.com/show_bug.cgi?id=4856) 
-   [#4871](https://bugzilla.xamarin.com/show_bug.cgi?id=4871) 
-   [#4871](https://bugzilla.xamarin.com/show_bug.cgi?id=4871) 
-   [#4929](https://bugzilla.xamarin.com/show_bug.cgi?id=4929) 
-   [#4972](https://bugzilla.xamarin.com/show_bug.cgi?id=4972) 
-   [#4988](https://bugzilla.xamarin.com/show_bug.cgi?id=4988) 
-   [#4990](https://bugzilla.xamarin.com/show_bug.cgi?id=4990) 
-   [#4997](https://bugzilla.xamarin.com/show_bug.cgi?id=4997) 
-   [#5005](https://bugzilla.xamarin.com/show_bug.cgi?id=5005) 
-   [#5036](https://bugzilla.xamarin.com/show_bug.cgi?id=5036) 
-   [#5036](https://bugzilla.xamarin.com/show_bug.cgi?id=5036) 
-   [#5053](https://bugzilla.xamarin.com/show_bug.cgi?id=5053) 
-   [#5058](https://bugzilla.xamarin.com/show_bug.cgi?id=5058) 
-   [#5078](https://bugzilla.xamarin.com/show_bug.cgi?id=5078) 
-   [#5093](https://bugzilla.xamarin.com/show_bug.cgi?id=5093) 
-   [#5160](https://bugzilla.xamarin.com/show_bug.cgi?id=5160) 
-   [#992](https://bugzilla.xamarin.com/show_bug.cgi?id=992) 


 []()

 <a name="MonoTouch_5.3.5" class="injected"></a>


# MonoTouch 5.3.5

 <a name="New_APIs" class="injected"></a>


## New APIs

-  New methods for AVCaptureDevice
-  Added ipv6 support for NetworkReachability
-  NetworkReachability can now use IP address pairs
-  New strongly typed accessors for MPMediaItem


 <a name="Improvements" class="injected"></a>


## Improvements

<ul>
  <li>Improved linker error messages</li>
  <li>Registrar handles more types</li>
  <li>Extended the set of thread-safe UIKit methods based on new data from
  Apple:
    <ul>
      <li>
        <a href="http://iosapi.xamarin.com/?link=T%3aMonoTouch.UIKit.UIView%2fM%2fDrawString" target="_blank"><em>DrawString</em> on <em>UIView</em></a>
      </li>
      <li>
        <a href="http://iosapi.xamarin.com/?link=T%3aMonoTouch.UIKit.UIBezierPath" target="_blank"><em>UIBezierPath</em></a>
      </li>
      <li>
        <a href="http://iosapi.xamarin.com/?link=T%3aMonoTouch.UIKit.UIImage" target="_blank"><em>UIImage</em></a>
      </li>
    </ul>

  </li>
  <li>UISlider has new appearance properties, based on new data from Apple</li>
  <li>Allow null dictionary on MKPlacemark ctor and add Obsolete on (removed
  since 3.2) media player properties
  </li>
  <li>Removed some constructors that would lead to crashes (use factory
  methods)
  </li>
  <li>Lighter System.Uri parser that no longer uses regular expressions to
  parse expressions, making it faster and reducing the amount of code that
  needs to be imported from System,
  </li>
  <li>Bring a long standing Regex bug fix</li>
  <li>Improved web service interop for dates and times</li>
  <li>Support for newer iOS SDKs (no new APIs on this release)</li>
  <li>Support to turn unmanaged function pointers into managed delegates using
  <em>Marshal.GetDelegateForFunctionPointer (ptrToFunc, typeof
  (SomeDelegate))</em>.<br>
    <br>
    For this to work with Mono's static compiler, developers must decorate the
    delegate type with the <em>MonoNativeFunctionWrapper</em> attribute, like
    this:
    <pre><code class=" syntax brush-C#">[MonoNativeFunctionWrapper]
public delegate int SimpleDelegate (int a);</code></pre>

  </li>
  <li>The binding generator now supports delegates in delegates. This allows
  callbacks invoked by Objective-C to pass callbacks to C# that you can then
  invoke.<br>
    <br>
    For example:
    <pre><code class=" syntax brush-C#">delegate void PostFunc (int value);
delegate void Filter (PostFunc func)

[BaseType (typeof (NSObject)]
interface MyMapReduce {
    [Export ("callbackTakesCallback:")]
    void Run (Filter filterFunc);
}</code></pre>

  </li>
</ul>

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-   [3444 - JIT compile exception when using ConcurrentDictionary in SplitOrderedList ctor()](https://bugzilla.xamarin.com/show_bug.cgi?id=3444) 
-   [5231 - class_addProperty doesn't exist in iOS4](https://bugzilla.xamarin.com/show_bug.cgi?id=5231) 
-   [5272 - Monotouch does not correctly link referenced DLLs](https://bugzilla.xamarin.com/show_bug.cgi?id=5272) 
-   [5311 - LockRecursionException is defined in mscorlib and System.Core](https://bugzilla.xamarin.com/show_bug.cgi?id=5311) 
-   [5314 - MonoTouch.Dialog.StyledStringElement throws if cell has no imageview](https://bugzilla.xamarin.com/show_bug.cgi?id=5314) 
-   [5337 - INotifyPropertyChanging and PropertyChangingEventArgs not included in MonoTouch](https://bugzilla.xamarin.com/show_bug.cgi?id=5337) 
-   [5410 - AudioUnit Dispose method throws EntryPointNotFound exception](https://bugzilla.xamarin.com/show_bug.cgi?id=5410) 
-   [5543 - Linker fails with XmlElement attribute on generic type](https://bugzilla.xamarin.com/show_bug.cgi?id=5543) 
-   [5543 - Linker fails with XmlElement attribute on generic type](https://bugzilla.xamarin.com/show_bug.cgi?id=5543) 
-   [5546 - ServicePointManager.ServerCertificateValidationCallback does not validate certificate chain in MonoTouch](https://bugzilla.xamarin.com/show_bug.cgi?id=5546) 
-   [5567 - Enum.ToString behaves incorrectly in corner cases](https://bugzilla.xamarin.com/show_bug.cgi?id=5567) 
-   [5581 - UIDatePicker's MaximumDate/MinimumDate should allow null set](https://bugzilla.xamarin.com/show_bug.cgi?id=5581) 
-   [5610 - ADInterstitialAdDelegate - wrong Export](https://bugzilla.xamarin.com/show_bug.cgi?id=5610) 
-   [5615 - NSFileCoordinatorWritingOptions missing ForReplacing](https://bugzilla.xamarin.com/show_bug.cgi?id=5615) 
-   [5625 - Https Get results in System.NullReferenceException: Object reference not set to an instance of an object at Mono.Security.X509.X509Certificate.Parse (System.Byte[] data)](https://bugzilla.xamarin.com/show_bug.cgi?id=5625) 
-   [5638 - UITableViewSource::SectionIndexTitles trampoline call results in _sigtramp signalled.](https://bugzilla.xamarin.com/show_bug.cgi?id=5638) 
-   [5646 - UIAlertView showing params entry two times](https://bugzilla.xamarin.com/show_bug.cgi?id=5646) 
-   [5696 - App hangs on resume when calling CLLocationManager.StartMonitoringSignificantLocationChanges](https://bugzilla.xamarin.com/show_bug.cgi?id=5696) 
-   [5714 - Long compile times for very large methods when using LLVM.](https://bugzilla.xamarin.com/show_bug.cgi?id=5714) 
-   [5755 - Can't increase trampolines](https://bugzilla.xamarin.com/show_bug.cgi?id=5755) 
-   [5755 - Can't increase trampolines](https://bugzilla.xamarin.com/show_bug.cgi?id=5755) 
-   [5767 - Typo in CGPath.AddElipseInRect(...)](https://bugzilla.xamarin.com/show_bug.cgi?id=5767) 
-   [5768 - InvalidCastException when retrieving a boolean value from sqlite reader](https://bugzilla.xamarin.com/show_bug.cgi?id=5768) 
-   [5776 - AMDeviceTransferApplication returned: 0x0 (kAMDSuccess).](https://bugzilla.xamarin.com/show_bug.cgi?id=5776) 
-   [5805 - CoreMotion bug in StartDeviceMotionUpdates](https://bugzilla.xamarin.com/show_bug.cgi?id=5805) 
-   [5808 - CBCentralManager.ScanForPeripherals(null, null) not working as expected](https://bugzilla.xamarin.com/show_bug.cgi?id=5808) 
-   [5898 - UIButton -setTitle:forState: null ref exception](https://bugzilla.xamarin.com/show_bug.cgi?id=5898) 
-   [5903 - UITableView Source property is always null](https://bugzilla.xamarin.com/show_bug.cgi?id=5903) 
-   [6086 - GKSession constructor should allow null for sessionID and displayName](https://bugzilla.xamarin.com/show_bug.cgi?id=6086) 
-   [6118 - [OSX] File.GetCreationTime returns last modified time instead](https://bugzilla.xamarin.com/show_bug.cgi?id=6118) 
-   [6172 - For Application 'SharedResources' and 'MonoDevelop-MonoCatalog', 'Cancel' and 'Done buttons under 'Contacts' crashes the application and throw error in application output " MonoTouch.UIKit.UIApplication.Main"](https://bugzilla.xamarin.com/show_bug.cgi?id=6172) 


 <a name="API_Changes" class="injected"></a>


## API Changes

The [5.3.4 to 5.3.5](/releases/ios/api_changes/from_5.3.4_to_5.3.5) page contains the detailed API changes since the last beta
release.

 []()

 <a name="MonoTouch_5.3.6" class="injected"></a>


# MonoTouch 5.3.6

 <a name="Fixes" class="injected"></a>


## Fixes

This version contains the same fix that prevents applications from crashing
in iOS 6 that was released as part of MonoTouch 5.2.13. Details about this fix [are in our blog](http://blog.xamarin.com/2012/08/13/important-ios-6-information-for-monotouch-users/).

The CoreBluetooth APIs have been fixed and now allow
MonoTouch.CoreBluetooth.CBUUID objects to be used as UUIDs in addition to
System.UUID.

 <a name="Improvements" class="injected"></a>


## Improvements

 <a name="Library_Improvements" class="injected"></a>


### Library Improvements

UIPageViewController.SetViewController now allows null as a completion
handler.

AVCaptureOutput.Connections returns a strongly typed array instead of
NSObject [].

 <a name="Line_Number_Information" class="injected"></a>


### Line Number Information

Native debug builds now contain line number information that allows existing
C tools to map executable code to C# source code.

This is particularly useful when using Instruments and crashes.

 <a name="MonoTouch.Dialog" class="injected"></a>


### MonoTouch.Dialog

MonoTouch.Dialog no longer uses the System.Web stack for its JsonElement,
which drops a dependency on the entire System.Web stack and instead uses
NSUrlConnection, making your binaries smaller.

 <a name="API_Changes" class="injected"></a>


## API Changes

The [5.3.5 to 5.3.6 page](/guides//from_5.3.5_to_5.3.6) contains
the detailed API changes since the last beta release.
