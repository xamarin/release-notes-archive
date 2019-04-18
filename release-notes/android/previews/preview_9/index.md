---
id: 65936FC7-CF40-766D-8FF2-10F1CAEFF339
title: "Preview 9"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

Beginning with this preview, you will need the following two packages in the
Android SDK:

-  Android SDK Tools, revision 8
-  Android SDK Platform-tools, revision 1


It is highly suggested that you delete your existing C:\android-sdk-windows
directory and use the new Android SDK Windows installer. See [Installation](http://android.xamarin.com/Installation) for more details.

 <a name="Enhancements" class="injected"></a>


# Enhancements

 <a name="Android_SDK_Tool_Revision_8_Support" class="injected"></a>


## Android SDK Tool Revision 8 Support

Preview 9 supports (and requires) the new Android SDK Tools, revision 8. You
will need to upgrade your tools as listed above.

 <a name="JNI_Support" class="injected"></a>


## JNI Support

The [Android.Runtime.JNIEnv](http://docs.monodroid.net/index.aspx?link=T:Android.Runtime.JNIEnv) type can be used to perform various
low-level JNI operations, such as creating new Java types and invoking methods
on Java types and instances.

 <a name="Breaking_Changes" class="injected"></a>


# Breaking Changes

 <a name="&lt;AndroidApplication&gt;" class="injected"></a>


## &lt;AndroidApplication&gt;

MonoDroid .csproj files are now required to have:

```
<AndroidApplication>true</AndroidApplication>
```

This enables the tooling to know it is working with a MonoDroid project. The
templates have been updated to include this. When you open an existing project,
this * **should*** be automatically added for you. You should
not have to do anything to support this change.

 <a name="Removal_of_Javax.Xml" class="injected"></a>


## Removal of Javax.Xml

The `Javax.Xml` and related (nested) namespaces have been removed.
As far as we could determine (via XPath queries on the Android API definition),
these types were not used by the rest of Android, and thus was entirely
duplicative of [System.Xml](http://docs.monodroid.net/index.aspx?link=N:System.Xml).

 <a name="Streams_Change" class="injected"></a>


## Streams Change

Any API which previously used a [Java.IO.InputStream](http://docs.monodroid.net/index.aspx?link=T:Java.IO.InputStream) or [Java.IO.OutputStream](http://docs.monodroid.net/index.aspx?link=T:Java.IO.OutputStream) should now use a .NET [System.IO.Stream](http://docs.monodroid.net/index.aspx?link=T:System.IO.Stream). This is a continuation of our "hide Java-isms"
work.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [639560](https://bugzilla.novell.com/show_bug.cgi?id=639560) - Global ref table overflows due to GC issues 
-   [652296](https://bugzilla.novell.com/show_bug.cgi?id=652296) - crash if i try to download an image from the internet when i read the urlConnection's InputStream value 
-   [655765](https://bugzilla.novell.com/show_bug.cgi?id=655765) - Preview 8 requires Android 2.2 for OpenGL Application 
-   [655872](https://bugzilla.novell.com/show_bug.cgi?id=655872) - Passing null for string[] Parameters in Activity.ManagedQuery and ContentProvider.Query Causes System.ArgumentNullException 
-   [656309](https://bugzilla.novell.com/show_bug.cgi?id=656309) -  `monodroid --noshared` doesn't work. 
-   [656469](https://bugzilla.novell.com/show_bug.cgi?id=656469)  <span title="Runtime">-</span> Inserting Multiple Records in SQLite Database From Text File Causes ReferenceTable Overflow Error 
-   [656955](https://bugzilla.novell.com/show_bug.cgi?id=656955) - Regression: [DllImport] doesn't work on bundled libraries.
