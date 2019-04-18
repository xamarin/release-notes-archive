---
id: 8D6E050A-B282-4B61-B18A-FB4E296400F6
title: "Mono for Android 4.2.5"
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

-  Deployment to API Level 16 ("Jelly Bean") hardware devices works.
-  API Level 16 binding. We would appreciate any review of the updated bindings. -    *Note*  : When deploying a Debug build of an existing project to a Jelly Bean device, you  *must*  clean and rebuild the project first. Failure to do so will result in Permission Denied errors during installation. 
-   If you continue to get Permission Denied failures after rebuilding the project, application data is being preserved across package removal and reinstall. Either manually uninstall the package from the Settings app, remove the app using ` *adb uninstall package.name*  `, or disable the Preserve application data/cache between device deploys option. 


 
-  The NDK &lt;android/bitmap.h&gt; header is now bound and exposed in Android.Graphics.Bitmap. 


 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Don't lookup base types on Annotations.  [Email thread](http://lists.ximian.com/pipermail/monodroid/2012-July/011392.html) . 
-  Fix missing R class issue in Android library project support in Java binding project. It involves some design changes explained later. 
-  Remove Regex dependency from UriParser.
-  Fix HttpWebRequest so that the buffered request isn't sent until GetResponse() is called. 
-  Add NetworkStream.ReceiveTimeout, NetworkStream.SendTimeout.
-  Fix HTTP cookie parsing.
-  Improve Socket and Thread.Abort() interaction.
-  Enable IPv6 support.
-   [1553](https://bugzilla.xamarin.com/show_bug.cgi?id=1553) : NullReferenceExceptions in WebConnectionStream &amp; WebConnection 
-   [2663](https://bugzilla.xamarin.com/show_bug.cgi?id=2663) : Regular Expressions bug 
-   [2965](https://bugzilla.xamarin.com/show_bug.cgi?id=2965) : Socket.SendToAsync loses operations when called too quickly, followed by runtime crash 
-   [4385](https://bugzilla.xamarin.com/show_bug.cgi?id=4385) : Cannot set value of a nullable from immediate window 
-   [4640](https://bugzilla.xamarin.com/show_bug.cgi?id=4640) :  <span>WebRequest::GetRequestStream blocks indefinitely
    (up to timeout)</span> 
-   [4659](https://bugzilla.xamarin.com/show_bug.cgi?id=4659) : Error in soft debugger method call thread 
-   [5577](https://bugzilla.xamarin.com/show_bug.cgi?id=5577) : Mono.Data.Sqlite: column types aren't preserved 
-   [5617](https://bugzilla.xamarin.com/show_bug.cgi?id=5617) : Mono.Facebook usage 
-   [5697](https://bugzilla.xamarin.com/show_bug.cgi?id=5697) : DateTime.ToFileTimeUtc should convert to UTC if needed 
-   [5710](https://bugzilla.xamarin.com/show_bug.cgi?id=5710) : HttpWebRequest::Abort does not release socket 
-   [5768](https://bugzilla.xamarin.com/show_bug.cgi?id=5768) : InvalidCastException when retrieving a boolean value from sqlite reader 
-   [5868](https://bugzilla.xamarin.com/show_bug.cgi?id=5868) : Java Binding Project cannot reference a library project 
-   [5979](https://bugzilla.xamarin.com/show_bug.cgi?id=5979) : List support in generic method instantiation in binding got broken by JavaObjectExtensions.JavaCast() 
-   [5985](https://bugzilla.xamarin.com/show_bug.cgi?id=5985) : RectangleF.Contains() 
-   [6117](https://bugzilla.xamarin.com/show_bug.cgi?id=6117) : When deploying to Android 4.1, you get "Data at the root level is invalid. Line 1, position 1." 
-   [6126](https://bugzilla.xamarin.com/show_bug.cgi?id=6126) : Support package: ViewPager PageScrolled NoClassDefFoundError 
-   [6186](https://bugzilla.xamarin.com/show_bug.cgi?id=6186) : Android library project binding needs to generate Resource.designer.cs and avoid conflicts 
-   [6236](https://bugzilla.xamarin.com/show_bug.cgi?id=6236) : Application does not Run/Debug through VS 2010 and VS 2012 
-   [6255](https://bugzilla.xamarin.com/show_bug.cgi?id=6255) : Unable to run the MFA application using MonoDevelop 3.1.0 
-   [6256](https://bugzilla.xamarin.com/show_bug.cgi?id=6256) : Stylable resource ids gets messed up in Resource.Designer file 
-   [6475](https://bugzilla.xamarin.com/show_bug.cgi?id=6475) : GC runs constantly on API &lt;= 7 targets 
-   [6482]() : Deploy to device can get frozen when trying to detect packages 
-   [6645](https://bugzilla.xamarin.com/show_bug.cgi?id=6645) : For 'Button' Application,one build error displayed "System.IO.DirectoryNotFoundException" 
-   [6654](https://bugzilla.xamarin.com/show_bug.cgi?id=6654) : AutoResetEvent state is getting corrupted 


 <a name="Layout_Designer_fixes" class="injected"></a>


# Layout Designer fixes

 **Visual Studio Users**: The Layout Designer is installed with
Mono for Android.

 **MonoDevelop Users**: The Layout Designer is not included in
the Mono for Android installer; the layout designer fixes are included in
MonoDevelop 3.0.4.

 <a name="" class="injected"></a>


# Changes needed to Android Library project support in Java binding project 

This version fixes the issue that Android library project Jar binding could
not generate R classes with the expected package name. Through this fix, we
noticed that "bin" directory contents in Eclipse/Ant project packaged as
AndroidLibraryZip is not enough. This directory contains only whatever required
by the library itself.

To fix this issue, we have to make some requirement changes to
AndroidLibraryZip: it has to contain top-level "res" and whatever required, as
well as the jar itself in "bin", packaged into AndroidLibraryZip. Typically you
can select "res" and "bin" and compress them into a zip, then add it to the
project as AndroidLibraryZip.

Note that Android Library Project does not support "assets". For details, see [http://developer.android.com/tools/projects/index.html#LibraryProjects](http://developer.android.com/tools/projects/index.html#LibraryProjects).

 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
