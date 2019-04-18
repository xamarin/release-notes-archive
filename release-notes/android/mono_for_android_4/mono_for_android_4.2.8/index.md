---
id: D829682F-5F35-0F45-A29F-69D50836E02F
title: "Mono for Android 4.2.8"
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

 <a name="New_Features" class="injected"></a>


# New Features

-  armeabi-v7a is the default ABI.
-  Add ActivityAttribute.ParentActivity property.
-  Add ServiceAttribute.IsolatedStorage property.
-  Binding Projects now embed the bound .jar into the binding assembly.
-  Library Projects can now contain Android Resources.


 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Theoretical GC bug involving a race condition between Mono &amp; Android GC's. Note: we've never seen this in the wild, and have no repro. 
-  Improve product activation on Windows.
-  Throw TypeLoadException if a Type can't be loaded instead of throwing a NullReferenceException. 
-   [6249](https://bugzilla.xamarin.com/show_bug.cgi?id=6249) : Assets not included in package when IntermediateOutputPath is specified to an absolute path. 
-   [7013#c15](https://bugzilla.xamarin.com/show_bug.cgi?id=7013#c15) : Add native libraries to .apks in the right order to improve support for Android 4.0-4.0.3. 
-   [7309](https://bugzilla.xamarin.com/show_bug.cgi?id=7309) : Resources.GetXml - XmlReader.Name property Hangs without exception 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
