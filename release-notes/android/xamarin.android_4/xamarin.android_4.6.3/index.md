---
id: E4C87ACD-DB4B-4C19-913C-1CFD7AD7A517
title: "Xamarin.Android 4.6.3"
---

# Installation

 **Known issue**: Immediately after upgrading, users may have
trouble loading Xamarin.Android projects. Please restart Xamarin Studio again
if you experience this.

 **Visual Studio Users**: You should be prompted with this update
when you open a Mono for Android project. You can also check manually in Tools
&gt; Options &gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates.
IDE support requires Xamarin Studio 4.0.
Layout Designer fixes require MonoDevelop 3.0.4.

# Bug fixes

-  Fixes a  [Linker error](http://forums.xamarin.com/discussion/3114/release-mode-linker-error) which occurrs when building a Release build of a project which references  `Mono.Android.Support.V4.dll` . 
-   [5037](https://bugzilla.xamarin.com/show_bug.cgi?id=5037) : Support satellite assemblies.    
  *Note* : Deploying Debug+Fast Deployment builds which use satellite assemblies will require an updated Xamarin Studio to deploy the satellite assemblies. Using Release builds, disabling fast deployment, using Visual Studio, and command-line  `msbuild` / `xbuild` use will properly deploy satellite assemblies. 
-   [9572](https://bugzilla.xamarin.com/show_bug.cgi?id=9572) :  `adb logcat` is spammed during fast deployment process. 
-   [10840](https://bugzilla.xamarin.com/show_bug.cgi?id=10840) : Fast deployment option makes deployment slow... 


# Regressions

-   [9433](https://bugzilla.xamarin.com/show_bug.cgi?id=9433) : Reverted as this fix was indirectly responsible for an  `ArgumentOutOfRangeException` when linking a Release app which references  `Mono.Android.Support.v4.dll` . 


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
