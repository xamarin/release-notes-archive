---
id: 3B5BCFF3-B36B-A1C5-A3B2-B1F594D12A9B
title: "Mono for Android 4.2.6"
---

<a name="Installation" class="injected"></a>


# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Mono for Android projects. Please restart MonoDevelop again if
you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0. Layout Designer fixes require MonoDevelop
3.0.4.

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-   [Fix SSL/https](http://lists.ximian.com/pipermail/monodroid/2012-September/012213.html) . 
-   [275](https://bugzilla.xamarin.com/show_bug.cgi?id=275) : Net.Tcp doesn't listen on 0.0.0.0 or ::0 
-   [6501](https://bugzilla.xamarin.com/show_bug.cgi?id=6501) : Unexpected invalid certificate exception 
-   [6531](https://bugzilla.xamarin.com/show_bug.cgi?id=6531) : generator: field property setters leak JNI local references 
-   [6766](https://bugzilla.xamarin.com/show_bug.cgi?id=6766) : Java.Security.KeyStore.Load wraps null streams 
-   [6899](https://bugzilla.xamarin.com/show_bug.cgi?id=6899) : When user stops a debug session in VS 2010 and 2012, it takes several seconds (&gt;10) to return to a useable state 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
