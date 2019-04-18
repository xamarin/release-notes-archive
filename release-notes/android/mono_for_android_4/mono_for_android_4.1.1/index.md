---
id: 9A97FA04-4290-E080-16AD-CA8DD02B408B
title: "Mono for Android 4.1.1"
---

<a name="Installation" class="injected"></a>


# Installation

 **The 4.1.x series will be a series of alphas and betas leading up to the next big stable release, 4.2.**

 **To see these updates, you have to switch to the Alpha channel in your IDE.**

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="" class="injected"></a>


# Changes since  [4.1.0](/releases/android/mono_for_android_4/mono_for_android_4.1.0)

 <a name="Layout_Designer" class="injected"></a>


## Layout Designer


We are extremely pleased to introduce our graphical designer for producing
Android layout files. This should make designing views for applications much
easier.   


   


   


   



Available for both MonoDevelop:   


   


 [ ![](mono_for_android_4.1.1/Images/walkthrough2.png)](mono_for_android_4.1.1/Images/walkthrough2.png)

   


   


   


   



And Visual Studio:   


   


 [ ![](mono_for_android_4.1.1/Images/vs-designer.png)](mono_for_android_4.1.1/Images/vs-designer.png)

   


   


   


   



We think this will be the best designer available for Android, so please file
any bugs you find in the designer!   


   


 <a name="x86_emulator_support" class="injected"></a>


## x86 emulator support

x86 emulators are now fuly supported in the trial and full MfA editions. This
release includes fixes for library loading errors with logcat messages such as
"java.lang.UnsatisfiedLinkError: Cannot load library: reloc_library[1311]: 799
cannot locate 'atexit'..."

 <a name="More_event_listener_methods_are_bound_to_events" class="injected"></a>


## More event listener methods are bound to events

Previously, event listener methods would only be mapped to events if the
event listener interface contained only one method. We now support event
listener interfaces that have more than one method, generating one event per
event listener interface method.

 <a name="Improved_API_level_support" class="injected"></a>


## Improved API level support

Historically, Applications (and Debug Platform packages) would target a
"minimum" API level, and could only be installed on targets running that API
level or later. For example, if an Application was built against Android v2.3
(API level 10), it couldn't reliably run on a lower API level (e.g. API level 8)
(" [the MotionEvent problem](http://lists.ximian.com/pipermail/monodroid/2011-November/007350.html)").

This has been fixed so that it is now possible to sanely target an API level
that is higher than the target's API level (e.g. target API 14 and run on API
8). Care must still be taken to only use types and members that exist on the
target.

 <a name="Earlier_error_checking" class="injected"></a>


## Earlier error checking

Build steps that used to be done at package creation time are now done as
part of the normal build process, allowing errors to be flagged earlier. This
includes Android Callable Wrapper generation and linking.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-  Due to the event listener change, we had to replace  *ItemEventArgs* which was used in some limited classes with  *AdapterView.ItemClickEventArgs* which is used everywhere applicable.  *ItemEventArgs* still exists, but since event signature has changed, your delegating methods need to be changed as well. For those who used signature-less lambdas it wouldn't affect. 
-  Various  *ToNative()* methods were renamed to  *ToJniHandle()* . Any .jar bindings may need to be regenerated and rebuilt. 
-  Additional int-&gt;enum changes.
-  Various  *int* to  [Color](http://androidapi.xamarin.com/?link=T:Android.Graphics.Color) changes on properties, method return types, and constructor and method parameters. 
-  The various  * *Foo*EventArgs.E* properties are now named  * *Foo*EventArgs.Event* . 
-  The various  * *Foo*EventArgs.V* properties have been removed, and their value is now the sender parameter of the  *EventHandler* delegate. 
-  Rename  *ViewAttachedToWindowEventArgs.V* to  *ViewAttachedToWindowEventArgs.AttachedView* and  *ViewDetachedFromWindowEventArgs.V* to  *ViewDetachedFromWindowEventArgs.DetachedView* . 
-  RemoteViews.SetViewVisibility() now takes ViewStates enum, not SystemUiFlags enum. 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-  Fix  [Java.Lang.Object deserialization for JSON](https://github.com/xamarin/monodroid-samples/blob/0cd9b3e3/SanityTests/Hello.cs#L412) in Release builds. 
-  Duplicate  *&lt;uses-library/&gt;* elements within  *AndroidManifest.xml* are removed. 
-  Emit  *&lt;uses-sdk/&gt;* before  *&lt;application/&gt;* within AndroidManifest.xml. (Failure to do so results in Android ignoring themes.) 
-  The  [Java.Lang.Throwable.StackTrace](http://androidapi.xamarin.com/?link=P:Java.Lang.Throwable.StackTrace) property no longer returns  *null* . 
-  .jar binding is now more intelligent about int-&gt;enum mappings, and should greatly reduce the need to manually fixup new bindings. 
-  We now validate at build-time that the package name contains a period ('.'). If the package name doesn't contain a period, then Android will give a  *INSTALL_FAILED_INVALID_APK* when installing the package. 
-  Mono for Andorid assemblies are now strong-named.
-  Building a Release build twice in a row no longer generates javac errors. 
-   [210](https://bugzilla.xamarin.com/show_bug.cgi?id=210) : Fixup package names so that Android will accept them 
-   [374](https://bugzilla.xamarin.com/show_bug.cgi?id=374) :  [Paint.Color](http://androidapi.xamarin.com/?link=P%3aAndroid.Graphics.Paint.Color) should be of type  *Android.Graphics.Color* , not  *int* . 
-   [2422](https://bugzilla.xamarin.com/show_bug.cgi?id=2422) : OpenTK.FrameEventArgs.set_Time crash 
-   [3641](https://bugzilla.xamarin.com/show_bug.cgi?id=3641) : Mono 2.11 make check failures on Cygwin 
-   [4441](https://bugzilla.xamarin.com/show_bug.cgi?id=4441) : Compatibility library should be called Support Packages 
-   [4485](https://bugzilla.xamarin.com/show_bug.cgi?id=4485) : Java Binding Library generates C# code that does not build 
-   [4592](https://bugzilla.xamarin.com/show_bug.cgi?id=4592) : [Export] + Release builds == TargetInvocationException 
-   [4594](https://bugzilla.xamarin.com/show_bug.cgi?id=4594) : API Demo exception thrown on Graphics-&gt;Alpha Bitmap on Release configuration 
-   [4605](https://bugzilla.xamarin.com/show_bug.cgi?id=4605) : Android.Widget.RemoteViews.SetViewVisibility does not exist for all API versions 


 <a name="Warnings:" class="injected"></a>


# Warnings:

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
