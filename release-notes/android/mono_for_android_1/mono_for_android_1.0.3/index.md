---
id: 79F40B34-8F93-742B-99B3-1B687F332161
title: "Mono For Android 1.0.3"
---

&nbsp;

 **Visual Studio Users:** Download [monoandroid-1.0.3.msi](http://c227137.r37.cf1.rackcdn.com/monoandroid-1.0.3.msi) and install.

 **MonoDevelop Users:** You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help-&gt;Check for Updates.

 <a name="Major_Highlights" class="injected"></a>


# Major Highlights

&nbsp;

 **Improved Debugger Performance:** both stepping over your .NET
code and examining variables is significantly faster. We eliminated some major
bottlenecks caused by roundtrips from Visual Studio to the device and this has
resulted in faster debugging and faster exploration of your variables.

 **Garbage Collection:** There are many important bug fixes to
the garbage collector specific to Android. Every Mono for Android user is
encouraged to upgrade to this release.

 <a name="Changes_Since_Mono_for_Android_1.0.2" class="injected"></a>


# Changes Since Mono for Android 1.0.2

 <a name="Garbage_Collection" class="injected"></a>


## Garbage Collection

Many garbage collection bugs have been fixed, the NullReferenceExceptions
class of errors from Java.Lang.Object.GetObject() should not happen anymore:

```
Unhandled Exception: System.NullReferenceException: Object reference not set to an 
  instance of an object
  at Java.Lang.Object.GetObject (IntPtr handle, System.Type type, Boolean owned) [0x00000] 
  at Java.Lang.Object._GetObject[IOnTouchListener] (IntPtr handle, Boolean owned) [0x00000]
  at Java.Lang.Object.GetObject[IOnTouchListener] (IntPtr handle, Boolean owned) [0x00000] 
  at Android.Views.View+IOnTouchListenerAdapter.
     n_OnTouch_Landroid_view_View_Landroid_view_MotionEvent_
    (IntPtr jnienv, IntPtr native__this, IntPtr native_v, IntPtr native_e) [0x00000] 
  at (wrapper dynamic-method) object:b039cbb0-15e9-4f47-87ce-442060701362 
  (intptr,intptr,intptr,intptr)
```

 [NullReferenceExceptions coming from RunnableImplementor.Run() should also be fixed](http://bugzilla.xamarin.com/show_bug.cgi?id=230):

```
UNHANDLED EXCEPTION: System.NullReferenceException: Object reference not set to an 
 instance of an object
 at Java.Lang.Thread/RunnableImplementor.Run () <0x000c4>
 at Java.Lang.IRunnableAdapter.n_Run (intptr,intptr) <0x00037>
 at (wrapper dynamic-method) object.b56fa1f4-8bcf-45b1-9d80-771daa7615b2 
    (intptr,intptr) <0x0002b>
```

 <a name="Installation_Fixes" class="injected"></a>


## Installation Fixes

-  If you have both Java 6 SDK and Java 7 SDK installed, Mono for Android will use Java 6. 
-  Give clear error message if Java 6 SDK is not found. (Java 7 SDK is currently not supported.) 


 <a name="Visual_Studio_Add-in" class="injected"></a>


## Visual Studio Add-in

-  Improved performance of stepping through code while debugging.
-  Improved performance of examining variables while debugging.


 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-   [667062](https://bugzilla.novell.com/show_bug.cgi?id=667062) - Signing fails if project path contains # character

 
-   [690795](https://bugzilla.novell.com/show_bug.cgi?id=690795) - Assertion at ../../../../mono/metadata/sgen-gc.c:4963, condition `info-&gt;stack_start &gt;= info-&gt;stack_start_limit &amp;&amp; info-&gt;stack_start &lt; info-&gt;stack_end' not met.

 
-   [685215](https://bugzilla.novell.com/show_bug.cgi?id=685215) - Odd SurfaceView Touch exception.

 
-   [686649](https://bugzilla.novell.com/show_bug.cgi?id=684649) - SIGSEGV in the Runtime when clearing an array

 
-   [711286](https://bugzilla.novell.com/show_bug.cgi?id=711286) - Garbage Collector has conflict with accelerometer

 
-   [229](http://bugzilla.xamarin.com/show_bug.cgi?id=229) - Fix a g_assert() within the GC.

 
-   [230](http://bugzilla.xamarin.com/show_bug.cgi?id=230) - Http connection to server with NTLM authentication timeouts very often

 
-   [245](http://bugzilla.xamarin.com/show_bug.cgi?id=245) - GC prematurely collecting instances.

 
-   Ensure we give a better error than "aresgen.exe exited with code 1"

 
-   ThreadPool bug fixes from Mono 2.10, this fixes a problem with unreliable HTTP and other components of Mono that used the ThreadPool internally.

 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
