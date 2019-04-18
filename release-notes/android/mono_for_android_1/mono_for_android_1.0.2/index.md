---
id: 221B1AC0-2402-A2E9-3466-BE866A751C2F
title: "Mono For Android 1.0.2"
---

&nbsp;

 *Mono for Android 1.0.21515 is the first release done by Xamarin.*

 **Visual Studio Users:** Download [monoandroid-1.0.2.msi](http://c227137.r37.cf1.rackcdn.com/monoandroid-1.0.2.msi) and install.

 **MonoDevelop Users:** You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help-&gt;Check for Updates.

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

 <a name="API_Changes" class="injected"></a>


## API Changes

The System.Data.Services.Client.dll assembly is now included.

System.IO.IsolatedStorage is now available, making it easier to share code
with Windows Phone 7.

 <a name="Garbage_Collection" class="injected"></a>


## Garbage Collection

The runtime (including GC) was rebuilt, and includes a number of GC fixes.
Hopefully this will resolve some of the outstanding GC issues, though it does *not* resolve all outstanding GC issues such as TouchTest.

 <a name="Installation" class="injected"></a>


## Installation

The installer will actually work on Mac OS X Lion.

When installing on Mac OS X Lion, we now prompt to install Java if Java
hasn't already been installed.

 <a name="Activation" class="injected"></a>


## Activation

On Windows, if activation fails then a MfaActivation.dat file will be created
within the Documents folder. You will be able to email us this file so that we
can return a license file for activation if you're unable to activate online
(e.g. behind corporate firewall, etc.). See the Offline Activation page for more
information.

 <a name="MonoDevelop_Add-in" class="injected"></a>


# MonoDevelop Add-in

Version 2.6.5 of the Mono for Android Addin has been released. This release
includes debugging and stability fixes, and we recommend all users update to
this version via the Add-in Manager.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [690406](https://bugzilla.novell.com/show_bug.cgi?id=690406) : Additional int-&gt;enumeration conversions. 
-   [13](http://bugzilla.xamarin.com/show_bug.cgi?id=13) : When deploying my first simple app to the emulator, I get an Unhandled Exception 
-   [33](http://bugzilla.xamarin.com/show_bug.cgi?id=33) : mandroid generates a Java method override for members that match by name, but aren't actually overrides. 
-   [102](http://bugzilla.xamarin.com/show_bug.cgi?id=102) : mandroid doesn't properly capture javac error messages. 
-  Custom attributes and AndroidManifest.xml can now contain "properly cased" resource references; they will be lowercased by mandroid in the resulting AndroidManifest.xml (as required by Android). 
-  Initialize Runtime.init() arguments separately within MonoPackageManager.java. (This file is generated at build time, and is placed at e.g.obj\Debug\android\src\mono\MonoPackageManager.java.) This will hopefully narrow down (but not fix) some reported issues with ajava.lang.NullPointerException within the Runtime.init() call on some devices. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
