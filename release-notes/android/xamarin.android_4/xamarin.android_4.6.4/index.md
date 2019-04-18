---
id: C2CC2405-7DAD-4191-A226-BF1F8C2497F3
title: "Xamarin.Android 4.6.4"
---

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Xamarin.Android project. You can also check manually in Tools
&gt; Options &gt; Xamarin.Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

# Bug fixes

-   [11697](https://bugzilla.xamarin.com/show_bug.cgi?id=11697) : Libraries no longer compile 


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
