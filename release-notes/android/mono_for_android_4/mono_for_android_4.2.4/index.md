---
id: EAB38655-2713-355E-A639-D18C1E9431B1
title: "Mono for Android 4.2.4"
---

<a name="Installation" class="injected"></a>


# Installation

 **Visual Studio Users**: You should be prompted with this update
when you open a MFA project. You can also check manually in Tools &gt; Options
&gt; Mono for Android.

 **MonoDevelop Users**: You should be prompted to upgrade next
time you open MonoDevelop, or you can use Help &gt; Check for Updates. IDE
support requires MonoDevelop 3.0. Layout Designer fixes require MonoDevelop
3.0.3.3.

 <a name="New_Features" class="injected"></a>


# New Features

 <a name="Bug_fixes" class="injected"></a>


# Bug fixes

-  Use AndroidManifest.xml //uses-sdk/@android:targetSdkVersion when validating /manifest/@android:installLocation.  [Email thread](/guides/ios/advanced_topics/threading) . 
-  Don't create $HOME/.__override__ in Release apps.
-   [763](https://bugzilla.xamarin.com/show_bug.cgi?id=763) : Monodroid: Marking a service to run in new process causes exception 
-   [2057](https://bugzilla.xamarin.com/show_bug.cgi?id=2057) : Attempting to edit the manifest under source control fails if the file is not checked out 
-   [3328](https://bugzilla.xamarin.com/show_bug.cgi?id=3328) : Cannot deploy projects with dot in project name. 
-   [4111](https://bugzilla.xamarin.com/show_bug.cgi?id=4111) : Unable to downgrade MFA using MonoDevelop updater 
-   [4593](https://bugzilla.xamarin.com/show_bug.cgi?id=4593) : No UI for &lt;AndroidLinkSkip&gt; 
-   [4725](https://bugzilla.xamarin.com/show_bug.cgi?id=4725) : M4A Debugger exits silently without exceptions 
-   [4794](https://bugzilla.xamarin.com/show_bug.cgi?id=4794) : DataContractSerializer throws an InvalidOperationException when two different types with the same namespace and data contract name are used to create a serializer 
-   [5519](https://bugzilla.xamarin.com/show_bug.cgi?id=5519) : XElement.ToString() adding p1 prefix 
-   [5556](https://bugzilla.xamarin.com/show_bug.cgi?id=5556) : javaBinding project generator.exe newline in xml - exception 
-   [5608](https://bugzilla.xamarin.com/show_bug.cgi?id=5608) : Can't access [projectname].dll.mdb 
-   [5748](https://bugzilla.xamarin.com/show_bug.cgi?id=5748) : [Regression?] Not all native libraries are extracted on installation 


&nbsp;

 <a name="Layout_Designer_fixes" class="injected"></a>


# Layout Designer fixes

 **Visual Studio Users**: The Layout Designer is installed with
Mono for Android.

 **MonoDevelop Users**: The Layout Designer is not included in
the Mono for Android installer; the layout designer fixes are included in
MonoDevelop 3.0.3.3.

-  No longer crashes if API level 16 is installed.
-   [5551](https://bugzilla.xamarin.com/show_bug.cgi?id=5551) : Cannot drag a widget to the designer from toolbox in windows MonoDevelop 
-   [5766](https://bugzilla.xamarin.com/show_bug.cgi?id=5766) : Moving LinearLayout around breaks the designer 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
