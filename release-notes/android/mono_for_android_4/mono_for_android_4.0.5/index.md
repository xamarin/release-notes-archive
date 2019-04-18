---
id: 4F6D668F-5E08-C2DA-EC0E-DB43A7BAB3D5
title: "Mono For Android 4.0.5"
---

&nbsp;

 <a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="Changes_since_4.0.4" class="injected"></a>


# Changes since 4.0.4

This release brings an overhauled OpenTK/Android backend, with support for
all Android versions, including Ice Cream Sandwich, as well as improved multiple
context support, streamlined loading and other fixes and improvements.

 <a name="Behavior_changes" class="injected"></a>


# Behavior changes

 <a name="CreateFrameBuffer_should_not_be_called_in_OnLoad." class="injected"></a>


### CreateFrameBuffer should not be called in OnLoad.

By the time OnLoad is called, a context is already created, so user code
should not call CreateFrameBuffer in OnLoad. Instead, user code can optionally
override CreateFrameBuffer, which gets called when the context is about to be
created, to set up the OpenGL version and other settings, and then call base()
to allow the context to be created.

 <a name="Custom_context_support" class="injected"></a>


### Custom context support

All surface, display and context destruction activity happens in
GraphicsContext.Dispose (). Custom contexts can hook up this method for their
own destruction needs.

The Update method in IGraphicsContext objects is now called whenever the
surface changes. Custom contexts can hook up this method for resetting the
current context or other operations.

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-   [1918](http://bugzilla.xamarin.com/show_bug.cgi?id=1918) : Rotating OpenGL app dies with egl.EglMakeCurrent failed: 0x3009 
-   [2210](http://bugzilla.xamarin.com/show_bug.cgi?id=2210) : GLCube fails on ICS with egl.EglMakeCurrent failed 
-  Better multiple context support.
-  Fixes crashes when using custom contexts and swapping buffers.


 <a name="Regressions" class="injected"></a>


# Regressions

-   [2313](https://bugzilla.xamarin.com/show_bug.cgi?id=2313) : Resource name capitalization is inconsistent. This was fixed in 4.0.4 but not in 4.0.5. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
