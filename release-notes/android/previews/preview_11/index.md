---
id: 5729828D-9C25-3DC0-4E2A-FCD0E0210E96
title: "Preview 11"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

&nbsp;

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

&nbsp;

Beginning with preview 9, you will need the following two packages in the
Android SDK:

-  Android SDK Tools, revision 8
-  Android SDK Platform-tools, revision 1


It is highly suggested that you delete your existing C:\android-sdk-windows
directory and use the new Android SDK Windows installer. See [Installation](http://android.xamarin.com/Installation) for more details.

 <a name="General_Enhancements" class="injected"></a>


# General Enhancements

 <a name="Linking" class="injected"></a>


## Linking

This preview introduces our first step in enabling linking. Linking is
currently very conservative, and should not cause any problems. It is turned on
by default. Please file a bug if you find a case where linking is causing an
issue.

The .apk for the default MonoDroid application template is now 3.3 MB, down
from 12.0 MB. The same stand-alone application (no shared runtime) is now 6.3
MB, down from 19.0 MB. We expect to keep tuning it to be more aggressive for
better savings.

If you do not want linking, you can turn it off in your project's property
pages.

 <a name="Android_2.3_Profile" class="injected"></a>


## Android 2.3 Profile

While fixing reported crashers on Android 2.3, we realized that some of the
Android ABI changed between 2.2 and 2.3. This requires us to have different
profiles to support new 2.3 functionality.

In the project property page, you can set your application's target framework
as "Android 2.2" or "Android 2.3".

Applications targetting Android 2.2 should work on all versions of Android
1.6-2.3, however functionality added in 2.3 is not available. Applications
targetting Android 2.3 will have access to new 2.3 functionality, but depending
on usage, * **may*** not work on previous versions.

 <a name="Layout_File_Extension" class="injected"></a>


## Layout File Extension

The default file extension for a layout file is now .axml. This allows it to
be automatically associated with the layout schema for IntelliSense. Layout
files can still be .xml and will work the same, however they will not have
IntelliSense by default. Therefore, you do not have to update existing projects
if you don't want to.

&nbsp;

 <a name="Visual_Studio_Plugin_Enhancements" class="injected"></a>


# Visual Studio Plugin Enhancements

 <a name="Automatically_Set_AndroidResource/AndroidAsset" class="injected"></a>


## Automatically Set AndroidResource/AndroidAsset

When a file is added to the Resources or Assets directory, its Build Action
will now be set automatically.

 <a name="MonoDevelop_Addin_Enhancements" class="injected"></a>


# MonoDevelop Addin Enhancements

The addin now requires MonoDevelop 2.4.2, which can be downloaded from the
MonoDevelop website.

This release contains the following improvements and fixes:

-  There is code completion for "axml" GUI layout files.
-  Tracking of attached devices and emulators is more reliable.
-  The device picker dialog no longer goes behind the main window.
-  MSBuild support is more reliable. It automatically picks up changes to project files without manually reloading the project, and can build non-default project configurations. 
-  MonoDevelop attempts to track the running process on the device, ensure it quits when stopped, and collect its output. 
-  Project templates have been updated to match resource naming changes.
-  ADB interactions are faster and more reliable.
-  There is a "Refresh" button in the device picker dialog that can be used to restart the ADB server. 
-  MonoDevelop no longer opens the MSBuild targets file when there is an error. 
-  There is a GUI for the shared runtime and linker options.


Note that MonoDevelop only supports the 2.2 SDK in this release. Other API
levels will be supported in a future release.

 <a name="Breaking_API_Changes" class="injected"></a>


# Breaking API Changes

 <a name="Resource_Changes" class="injected"></a>


## Resource Changes

The `Android.R` type has been renamed to [Android.Resource](http://docs.monodroid.net/index.aspx?link=T:Android.Resource), and the names of some Android.Resource nested
types have been changed to remove abbreviations, e.g. `Android.R.Attr` type is now the [Android.Resource.Attribute](http://docs.monodroid.net/index.aspx?link=T:Android.Resource%2bAttribute) type.

Likewise, aresgen will now generate PascalCased and unabbreviated nested
names, thus generating `Resource.Attribute` instead of `Resource.attr` and `Resource.String` instead of `Resource.string` ( *and C# programmers rejoiced!*). aresgen
also supports mixed-case filenames for resources, removing a common source of
compiler errors.

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [643246](https://bugzilla.novell.com/show_bug.cgi?id=643246) - Automatically set Build Action on XML files to AndroidResource. 
-   [643958](https://bugzilla.novell.com/show_bug.cgi?id=643958) - Improve Resource handling and filename casing. 
-   [649465](https://bugzilla.novell.com/show_bug.cgi?id=649465) - RunOnUThread crashes 
-   [650335](https://bugzilla.novell.com/show_bug.cgi?id=650335) - Keyboard shortcut does not work for SaveAll when code editor is active 
-   [656584](https://bugzilla.novell.com/show_bug.cgi?id=656584) - AutoCompleteTextView missing SetAdapter 
-   [656759](https://bugzilla.novell.com/show_bug.cgi?id=656759) - Paint.Reset is crashing with NullPointerException 
-   [658552](https://bugzilla.novell.com/show_bug.cgi?id=658552) - ContactsContract.ContactsColumn is not bound. 
-   [658958](https://bugzilla.novell.com/show_bug.cgi?id=658958) - If you have a custom [Application] and use &lt;application&gt; in AndroidManifest.xml, //application/@android:name isn't set. 
-   [660928](https://bugzilla.novell.com/show_bug.cgi?id=660928) - Creating GZipStream causes a crash. 
-   [661517](https://bugzilla.novell.com/show_bug.cgi?id=661517) - Rename Android.R to Android.Resource. 
-   [661518](https://bugzilla.novell.com/show_bug.cgi?id=661518) - Rename Log.D() to Log.Debug(), etc. 
-   [661965](https://bugzilla.novell.com/show_bug.cgi?id=661965) - Adding required permissions is backwards. 
-   [662228](https://bugzilla.novell.com/show_bug.cgi?id=662228) - Allow some files to be stored uncompressed within the .apk 
-   [662315](https://bugzilla.novell.com/show_bug.cgi?id=662315) - Encoding.Default generates SIGILL 
-   [662814](https://bugzilla.novell.com/show_bug.cgi?id=662814) - Change Android.Views.Display.Rotation to an enum type. 
-   [664573](https://bugzilla.novell.com/show_bug.cgi?id=664573) - MonoDroid doesn't use the appropriate current culture. 
-   [665340](https://bugzilla.novell.com/show_bug.cgi?id=665340) - Add a Notification constructor which has a default `when` value. 
-   [665532](https://bugzilla.novell.com/show_bug.cgi?id=665532) - TextChanged in EditText's controller is not working  &nbsp;
