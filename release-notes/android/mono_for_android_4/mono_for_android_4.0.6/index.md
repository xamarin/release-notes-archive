---
id: 4784A31E-04E4-9ADC-E58F-1587D6E1CD7B
title: "Mono For Android 4.0.6"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="" class="injected"></a>


# Changes since  [4.0.5](/releases/android/mono_for_android_4/mono_for_android_4.0.4)

This release includes fixes to the OpenTK/Android backend.

It also includes x86 support for full versions of Mono for Android (not
trial)

 <a name="Improvements_to_OpenTK/Android" class="injected"></a>


## Improvements to OpenTK/Android

The run loop has been rewritten to obey the requested fps as closely as
possible and to minimize locking and thread switching.

By default, the egl configuration selected is a best match for a 16-bit RGB
frame buffer with a 16-bit depth buffer. AndroidGameView exposes a new property,
GraphicsMode, which can be set by user code with a GraphicsMode or
AndroidGraphicsMode instance to select a desired configuration before context
creation.

EGL objects bound to the current context can be accessed via the WindowInfo
property (now a AndroidWindow instance).

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-   [Android.App.LoadManager.InitLoader()](http://androidapi.xamarin.com/index.aspx?link=M%3aAndroid.App.LoaderManager.InitLoader(System.Int32%2cAndroid.OS.Bundle%2cAndroid.App.LoaderManager.ILoaderCallbacks)) and  [Android.App.LoadManager.RestartLoader()](http://androidapi.xamarin.com/?link=M%3aAndroid.App.LoaderManager.RestartLoader(System.Int32%2cAndroid.OS.Bundle%2cAndroid.App.LoaderManager.ILoaderCallbacks)) are now bound. 
-   [2313](https://bugzilla.xamarin.com/show_bug.cgi?id=2313) : Resource name capitalization is inconsistent. This regressed in 4.0.5. 
-   [2140](https://bugzilla.xamarin.com/show_bug.cgi?id=2140) : OpenGL Depth Buffer is always off 
-   [1918](https://bugzilla.xamarin.com/show_bug.cgi?id=1918) : Rotating OpenGL app dies with egl.EglMakeCurrent failed: 0x3009 
-  Render loop now obeys the requested fps
-  eglConfig selection now respects user values


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
