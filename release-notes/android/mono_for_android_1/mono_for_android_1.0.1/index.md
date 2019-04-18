---
id: 2CB4FC1C-6591-DBD7-A413-5C8C568CA82F
title: "Mono For Android 1.0.1"
---

&nbsp;

 <a name="Visual_Studio_Plugin_Enhancements" class="injected"></a>


# Visual Studio Plugin Enhancements

 <a name="USB_Debugging" class="injected"></a>


## USB Debugging

By default, Visual Studio now uses the USB connection to debug on physical
devices instead of requiring a wifi connection. If you would prefer to use wifi
debugging, there is a new option to enabled it in Tools-&gt;Options-&gt;Mono for
Android.

 <a name="Preserve_User_Data_Between_Deploys" class="injected"></a>


## Preserve User Data Between Deploys

Each time your application is changed and redeployed, the previous version is
uninstalled and the new version is installed. This also removes the data the
previous version stored in /data or /cache. There is now an option in
Tools-&gt;Options-&gt;Mono for Android that will preserve this data between
deploys.

 <a name="Resource_(Resx)_Support" class="injected"></a>


## Resource (Resx) Support

Added a .resx template for using .NET resources in Mono for Android.

 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [634603](https://bugzilla.novell.com/show_bug.cgi?id=634603) : debugger doesn't notify the user if it can't connect the listening ports 
-   [643367](https://bugzilla.novell.com/show_bug.cgi?id=643367) : Android.OS.AsyncTask missing abstract doInBackground method 
-   [671537](https://bugzilla.novell.com/show_bug.cgi?id=671537) : monodroid : error 1: Mono.Linker.ResolutionException: Can not resolve reference: System.Func`2" 
-   [675528](https://bugzilla.novell.com/show_bug.cgi?id=675528) : Visual studio crashes when deploying to device 
-   [675566](https://bugzilla.novell.com/show_bug.cgi?id=675566) : Need to support bundling I18N assemblies 
-   [678234](https://bugzilla.novell.com/show_bug.cgi?id=678234) : Crash while debugging on a real device 
-   [682042](https://bugzilla.novell.com/show_bug.cgi?id=682042) : long_click issue w/ linking 
-   [683642](https://bugzilla.novell.com/show_bug.cgi?id=683642) : GetProperty&lt;T&gt; on Binding does not return the proper result 
-   [684940](https://bugzilla.novell.com/show_bug.cgi?id=684940) : SimpleAdapter ClassCastException 
-   [685050](https://bugzilla.novell.com/show_bug.cgi?id=685050) : device selector stays in trial mode after activation 
-   [685584](https://bugzilla.novell.com/show_bug.cgi?id=685584) : Using SDB on the HTC Desire HD 
-   [686656](https://bugzilla.novell.com/show_bug.cgi?id=686656) : packing process failed during deployment 
-   [687521](https://bugzilla.novell.com/show_bug.cgi?id=687521) : VS 2010 Debugger Detaches - Exit Code 255 (0xff) 
-   [688006](https://bugzilla.novell.com/show_bug.cgi?id=688006) : Error message dialog for packaging not readable 
-  OSX installer properly updates MSBuild support
