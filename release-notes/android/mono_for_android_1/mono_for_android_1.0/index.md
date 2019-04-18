---
id: 41DDDAE8-E8F0-574E-35A0-C07092B9D5FA
title: "Mono For Android 1.0"
---

&nbsp;

 <a name="API_Changes" class="injected"></a>


# API Changes

Add [Android.App.ApplicationAttribute.BackupAgent](http://docs.mono-android.net/index.aspx?link=P%3aAndroid.App.ApplicationAttribute.BackupAgent) property. The
type assigned to this property must correspond to an [Android.App.Backup.BackupAgent](http://docs.mono-android.net/index.aspx?link=T%3aAndroid.App.Backup.BackupAgent) subclass.

 [Android.OS.AsyncTask](http://docs.mono-android.net/index.aspx?link=T%3aAndroid.OS.AsyncTask) should now work.

 [Java.IO.FileInputStream](http://docs.mono-android.net/index.aspx?link=T%3aJava.IO.FileInputStream) and [Java.IO.FileOutputStream](http://docs.mono-android.net/index.aspx?link=T%3aJava.IO.FileOutputStream) are now mapped to [System.IO.Stream](http://docs.mono-android.net/index.aspx?link=T%3aSystem.IO.Stream), which changes the prototype for several methods
such as [Android.Content.Context.OpenFileInput](http://docs.mono-android.net/index.aspx?link=M%3aAndroid.Content.Context.OpenFileInput%28System.String%29).

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

mandroid.exe and aresgen.exe are now built against the .NET 4.0 profile,
which should eliminate a number of errors users have seen.

The Debug runtime and platform packages now default to installing onto
internal storage instead of the SD card, but may be optionally moved to the SD
card by using e.g. Apps → Settings → Applications → Manage applications
→ Mono Shared Runtime → Move to SD card. This was done because execution
from the SD card was noticably slower on the emulator than execution from
internal storage.

Improved local reference table handling for strings.

 [Java.Lang.Throwable](http://docs.mono-android.net/index.aspx?link=T%3aJava.Lang.Throwable).ToString() will now print the Java-side
message and stack trace.

 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [658356](https://bugzilla.novell.com/show_bug.cgi?id=658356) : Overriding nested class must be in same java file as parent 
-   [667054](https://bugzilla.novell.com/show_bug.cgi?id=667054) : Soap WebServices stopped working in Preview 11 when using Async 
-   [667397](https://bugzilla.novell.com/show_bug.cgi?id=667397) : Error compiling template code 
-   [675179](https://bugzilla.novell.com/show_bug.cgi?id=675179) : javac error when generating proxy for type inheriting both ArrrayAdapter&lt;T&gt; and ISpinnerAdapter 
-   [675194](https://bugzilla.novell.com/show_bug.cgi?id=675194) : AlertDialog.Builder.SetMultiChoiceItems() doesn't show selection properly. 
-   [675718](https://bugzilla.novell.com/show_bug.cgi?id=675718) : If an assembly is linked to a non-MT component (i.e. System.EnterpriseServices) the linker fails with an unhelpful error message 
-   [675794](https://bugzilla.novell.com/show_bug.cgi?id=675794) : TypeLoadException when trying to hit a WCF service 
-   [679564](https://bugzilla.novell.com/show_bug.cgi?id=679564) : [generator] SmipleExpandableListAdapter generates ClassCastException 
-   [679599](https://bugzilla.novell.com/show_bug.cgi?id=679599) : Linker shouldn't remove constructors for types which are used by generic types/methods 'new' constraint 
-   [680001](https://bugzilla.novell.com/show_bug.cgi?id=680001) : Linker breaks ListActivity 
-   [680402](https://bugzilla.novell.com/show_bug.cgi?id=680402) : Unable to run an application from visual studio if I rename the Project
