---
id: E5EC8BB8-4B7F-BEF8-4975-4475F6C1761C
title: "Mono for Android 4.1.2"
---

<a name="Installation" class="injected"></a>


# Installation

 **The 4.1.x series will be a series of alphas and betas leading up to the next big stable release, 4.2.**

 **To see these updates, you have to switch to the Alpha channel in your IDE.**

 **Visual Studio Users**: You should be prompted with this update
when you open a MfA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 2.8.4.1.

 <a name="" class="injected"></a>


# Changes since  [4.1.1](/releases/android/mono_for_android_4/mono_for_android_4.1.1)

Bug fixes only.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

-   Various  `ToJniHandle()` methods have been renamed to  `ToLocalJniHandle()` , and now always return a JNI local reference.

 


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-  Unsubscribing from an event will now remove the Java-side Listener implementation, reducing gref count. Previously the entire object graph would need to be collectable and a full GC would be required to collect the Listener implementation.  [Mailing list reference](http://lists.ximian.com/pipermail/monodroid/2012-April/009780.html) . 
-   [2147](https://bugzilla.xamarin.com/show_bug.cgi?id=2147) :  `Android.Runtime.JavaObject` instances should no longer be returned to developer code. It should be automatically "unwrapped" to provide the original instance. 
-   [2347](https://bugzilla.xamarin.com/show_bug.cgi?id=2347) : The  [ArrayAdapter&lt;T&gt;(..., T[])](http://androidapi.xamarin.com?link=c%3aandroid.widget.arrayadapter%601%28android.content.context%2csystem.int32%2c%600[]%29) constructors do not support value types. 
-   [4571](https://bugzilla.xamarin.com/show_bug.cgi?id=4571) : .jar library binding doesn't work with  `GoogleAdMobAdsSdk-6.0.0.jar` . 
-   [4592](https://bugzilla.xamarin.com/show_bug.cgi?id=4592) : Preserve  `FromJniHandle()` ,  `ToLocalJniHandle()` methods in Release builds. 
-   [4783](https://bugzilla.xamarin.com/show_bug.cgi?id=4783) : Check types when marshaling arrays. 
-   [4821](https://bugzilla.xamarin.com/show_bug.cgi?id=4821) : Support marshaling arrays of enum types. 
-   [4822](https://bugzilla.xamarin.com/show_bug.cgi?id=4822) :  `ResolveLibraryProjectImports` can't find assembly via  `HintPath` . 


 <a name="Warnings:" class="injected"></a>


# Warnings:

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
