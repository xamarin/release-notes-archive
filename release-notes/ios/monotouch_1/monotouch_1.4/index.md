---
id: 8E423C48-4731-6C93-2545-770774672319
title: "MonoTouch 1.4"
---

<a name="MonoTouch_Improved_Startup_Times" class="injected"></a>


# MonoTouch Improved Startup Times

Startup times have been dramatically decreased. The time reduction is
anywhere from 60% to 40% depending on your application.

The MonoCatalog sample application went from 8.3 seconds on startup to 4.5 on
an original iPhone on a cold start (this sample application does load a lot of
NIB files on startup and does no attempt to delay-load any of the NIB files, so
it is an example of a badly behaved app).

Applications that have been tuned can get the first UIView up in 1.2 seconds
on 3GS.

 <a name="Reduced_Application_Sizes" class="injected"></a>


# Reduced Application Sizes


Applications compiled in release mode are now 30% smaller than in previous
releases. <a name="MonoDevelop_Performance_Improvements" class="injected"></a>


# MonoDevelop Performance Improvements

In some difficult-to-reproduce cases the MonoDevelop editor would be
extremely slow on first use. This has been fixed, and MonoDevelop editor speed
should now be normal for all users.

 <a name="Enhanced_Debugging_Experience" class="injected"></a>


# Enhanced Debugging Experience

We fixed dozens of usability problems in the MonoTouch debugger and
MonoDevelop that have been reported since we first unveiled the debugging
support.

 <a name="Debugging_Support_for_Core_Libraries" class="injected"></a>


# Debugging Support for Core Libraries

When compiling your code in Debug mode, the default has changed to not
include debug information for system libraries. This significantly reduces the
binary size as well as increasing the performance of applications running under
the "Debug" mode on the device.

If you want to step into system libraries, you will need to manually enable
this by either using the -debug:assemblyname or the -debug:all as an extra
argument to the mtouch command.

Additionally, you should unset "Debug project code only" in
Preferences/Debugger.

A new package [monotouch-source](http://download.monotouch.net/public/monotouch-source-1.4.pkg) contains the source code for the core Mono class
libraries, allowing developers to single step and see the source code for the
Mono class libraries.

 <a name="Binding_Generator_Support_for_Events" class="injected"></a>


# Binding Generator Support for Events

The binding generator (btouch) now supports binding delegates that are used
for notification and mapping those to C# events and C# properties. This vastly
simplifying the process of turning an Objective-C API into a C# API.

Details of this new feature are described in the "Event Handlers and
Callbacks" section of the Bindings New Objective-C Types document.

 <a name="Binding_Generator_Support_for_Unsafe_Code" class="injected"></a>


# Binding Generator Support for Unsafe Code

The binding generator now supports the -unsafe flag for code that needs to do
pointer arithmetic.

 <a name="Configurable_NRGCTX_Trampolines" class="injected"></a>


# Configurable NRGCTX Trampolines

In addition to a leak in the RGCTX trampoline reuse handling, we also made it
possible to configure the number of generic trampolines for generics-heavy
users.

You can create more trampolines by modifying your project options "iPhone
Build" section. You want to add extra arguments for the Device build
targets:

-aot "nrgctx-trampolines=2048"

The default number of trampolines is 1024. Try increasing this number until
you have enough for your usage of generics.

 <a name="AudioToolbox_Low-Level_APIs_have_been_bound." class="injected"></a>


# AudioToolbox Low-Level APIs have been bound.

The low-level APIs from AudioToolbox have been bound:

-  AudioFile: To decode and encode audio files. -   AudioSource: for callback-based encoding and decoding of audio files. 


 
-  AudioFileStream: To progressively decode audio files.
-  AudioQueue: for recording and playing back audio from raw audio data: -   OutputQueue for playback. 
-   InputQueue for recording.


 


 <a name="API_Breaking_Changes" class="injected"></a>


# API Breaking Changes

On UIScrollView the DraggingEnded event now is of type
EventHandler&lt;DraggingEventArgs&gt; instead of being an EventHandler, this was
an oversight in the original binding that prevented developers from accessing
the event information.

 <a name="API_Additions:" class="injected"></a>


# API Additions:

-   Bindings for NSNetService and NSNetServiceBrowser.

 
-  Bindings for CGDataProvider


-   New CGImage overloads that can consume CGDataProvider instances.

 
-   Added ReaderWriterLockSlim to MonoTouch API profile.

 
-   The NSKeyedArchived and NSKeyedUnarchiver got .NET style event handling.

 
-   Added NetworkReachability that takes IPAddress parameters in addition to hosts

 


 <a name="Samples" class="injected"></a>


# Samples

-  The reachability sample has been completed.


-   New StreamingAudio sample streams audio from an HTTP url using the new low-level AudioToolbox API bindings.

 
-  New Google Analytics Sample.




 <a name="Fixes" class="injected"></a>


# Fixes

The following bugs as reported on [http://bugzilla.novell.com](http://bugzilla.novell.com/) were fixed:

-   Fixed major issue with events in UIAccelerometer, and a bunch of other UIKit classes where the managed proxy could get GC'd and remove the event handler.

 
-   Fixed #553164 - MKMapView.SelectedAnnotations throws an InvalidCastException

 
-   Fixed #555420 - Cannot create ABAddressBook on iPod Touch

 
-   Fixed #557610 - P/Invoke calls on a 3G didn't always emit proper interwork code with thumb

 
-   Fixed #554701 - NSString comparisons use value equality of the underlying string now

 
-   Fixed #554768 - DrawString (..., RectangleF, ...) variants crashed on device.

 
-   Fixed #548491 - mdb files being copied to app in release mode

 
-   Fixed #551624 - mdb files missing from xcode project export

 
-   Fixed MPMediaPickerControllerDelegate to actually be a [Model]

 
-  Fixed export to Xcode with debug builds
