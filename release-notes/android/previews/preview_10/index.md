---
id: 098747EC-B220-6EA7-DC66-9A036FC1A196
title: "Preview 10"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

Beginning with preview 9, you will need the following two packages in the
Android SDK:

-  Android SDK Tools, revision 8
-  Android SDK Platform-tools, revision 1


It is highly suggested that you delete your existing C:\android-sdk-windows
directory and use the new Android SDK Windows installer. See [Installation](http://android.xamarin.com/Installation) for more details.

 <a name="Enhancements" class="injected"></a>


# Enhancements

 <a name="Return_of_Debugging" class="injected"></a>


## Return of Debugging

The main change for this preview is debugging, which was broken in preview 9,
is now fixed.

 <a name="GC_Disabled" class="injected"></a>


## GC Disabled

To ensure people can play with MonoDroid over the holidays without running
into GC issues, the GC is disabled for this preview. We will resume tweaking it
in the next preview.

 <a name="Experimental_Intellisense_for_Layout_Files" class="injected"></a>


## Experimental Intellisense for Layout Files

We now ship an experimental schema for layout files. To turn it on for a
layout file:

-  Open your layout file in Visual Studio.
-  Click " **Schemas** " in the  **Properties** window. 
-  Find the schema called " **android-layout-xml.xsd** ".
-   **Right-click** and select " **Use selected schemas** ". 
-  Click  **OK** .


Intellisense should now be enabled for the layout file.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [637846](https://bugzilla.novell.com/show_bug.cgi?id=637846) - Provide 'Deploy' option from MonoDroid Application Project 
-   [649393](https://bugzilla.novell.com/show_bug.cgi?id=649393) - aresgen.exe doesn't support arrays 
-   [656309](https://bugzilla.novell.com/show_bug.cgi?id=656309) - embedding the runtime in an application cuases a failure 
-   [656553](https://bugzilla.novell.com/show_bug.cgi?id=656553) - Calling NumberKeyListener.Filter method from derived class crash 
-   [657609](https://bugzilla.novell.com/show_bug.cgi?id=657609) - System.TimeZoneNotFoundException when accessing TimeZoneInfo.Local in Emulator and on Device 
-   [657820](https://bugzilla.novell.com/show_bug.cgi?id=657820) - ReferenceTable overflow (max=512) scrolling GridView at GetView() 
-   [658096](https://bugzilla.novell.com/show_bug.cgi?id=658096) - UNHANDED EXCEPTION: System.NullReferenceException 


&nbsp;
