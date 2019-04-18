---
id: 8B1578BE-2D7A-23EC-1A5A-87C0DB55DBD8
title: "Preview 8"
---

&nbsp;

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

&nbsp;

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless.

 <a name="Bug_Fixes_/_Enhancements" class="injected"></a>


# Bug Fixes / Enhancements

 <a name="Joint_Mono/Java_GC" class="injected"></a>


## Joint Mono/Java GC

This is one of the last major features required to ship MonoDroid. Before
this preview, cycles caused by Mono objects holding Java objects and Java
objects holding Mono objects kept all these objects alive. With this release we
have developed a joint garbage collection system that will properly dispose
unreferenced objects and avoid keeping objects in memory due to cycles.

Beginning with this preview, objects with corresponding java objects should
now be garbage collected when they are no longer held by other java objects. We
also are more aggressively releasing jni local refs to avoid many of the table
overflows failures people have experienced in previous previews.

 <a name="Java.Lang.Class_Methods" class="injected"></a>


## Java.Lang.Class Methods

The [Java.Lang.Class.Cast()](http://docs.monodroid.net/index.aspx?link=M%3aJava.Lang.Class.Cast%28Java.Lang.Object%29) and [Java.Lang.Class.NewInstance()](http://docs.monodroid.net/index.aspx?link=M%3aJava.Lang.Class.NewInstance) methods are now exposed.

 <a name="Mono_Initialization" class="injected"></a>


## Mono Initialization

In [Preview 7](/releases/android/previews/preview_7), Mono
initialization was performed within [Application.OnCreate()](http://docs.monodroid.net/index.aspx?link=M%3aAndroid.App.Application.OnCreate). It turns out that this wasn't early
enough, as [ContentProvider](http://docs.monodroid.net/index.aspx?link=T%3aAndroid.Content.ContentProvider)s listed within `AndroidManifest.xml` are created
before `Application.OnCreate()` is invoked.

Mono is now initialized via a dedicated `ContentProvider` with a
very high [initOrder](http://developer.android.com/guide/topics/manifest/provider-element.html#init) to ensure it's invoked first. This allows `ContentProvider`s to be supported.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

 <a name="JavaInputStream" class="injected"></a>


### JavaInputStream

The wrapper type that supported passing System.IO.Streams as
Java.IO.InputStreams has been renamed to Android.Runtime.InputStreamAdapter, and
we have added a corresponding OutputStreamAdapter, as well as Invokers to
support returning java streams as System.IO.Streams. In the next preview, these
will be utilized to expose all stream API in the binding as
System.IO.Streams.

 <a name="TelephonyManager.Listen" class="injected"></a>


### TelephonyManager.Listen

The [TelephonyManager.Listen()](http://docs.monodroid.net/index.aspx?link=M%3aAndroid.Telephony.TelephonyManager.Listen%28Android.Telephony.PhoneStateListener%2cAndroid.Telephony.PhoneStateListenerFlags%29) `events` parameter is
now an enumeration type.

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-   [654535](https://bugzilla.novell.com/show_bug.cgi?id=654535) - RemoveUnknownFiles task fails when compiling some AndroidAsset files. 
-   [654527](https://bugzilla.novell.com/show_bug.cgi?id=654527) - IOE When Inheriting From JavaDictionary&lt;K, V&gt;. 
-   [654522](https://bugzilla.novell.com/show_bug.cgi?id=654522) - Application dies with ContentProvider in AndroidManifest.xml. 
-   [655342](https://bugzilla.novell.com/show_bug.cgi?id=655342) - Only check for default constructors for types within  `AndroidManifest.xml` ; add a default constructor to  [Android.App.IntentService](http://docs.monodroid.net/index.aspx?link=T%3aAndroid.App.IntentService) .
