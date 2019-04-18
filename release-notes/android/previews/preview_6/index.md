---
id: 469D9570-617F-8D3D-DA76-D50F21BD74A8
title: "Preview 6"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless.

 <a name="Bug_Fixes_/_Enhancements" class="injected"></a>


# Bug Fixes / Enhancements

 <a name="Asset_Support" class="injected"></a>


### Asset Support

Android "Assets" are now supported. Assets are basically any files you want
to include and access in your application, like music, fonts, data, etc. Use
these in your application in a way that is very similar to Android resources.
The MonoDroid application template now creates a folder called Assets, which you
can put subfolders and your data in. Set the build action on each data file to
AndroidAsset.

You can then reference it in Android via the AssetManager or other Asset
aware API:

```
InputStream input = Assets.Open ("read_asset.txt");  
var tf = Typeface.CreateFromAsset (Context.Assets, "fonts/samplefont.ttf");
```

 <a name="Faster_Redeploy" class="injected"></a>


### Faster Redeploy

The Visual Studio plugin now detects whether your application has changed
since the last time it was deployed. If it hasn't, it will re-launch the
existing one rather than starting over.

 <a name="Java_Source_Support" class="injected"></a>


### Java Source Support

You can now provide additional Java source files to monodroid, e.g. to
provide custom non-MonoDroid activities for splash screens.

Java source files are added to the build by setting their **Build Action** to **AndroidJavaSource**.

 <a name="Native_Library_Support" class="injected"></a>


### Native Library Support

You can now bundle additional native libraries into your .apk.

Native libraries are added to the build by setting their **Build Action** to **AndroidNativeLibrary**.

Note that since Android supports multiple Application Binary Interfaces
(ABIs), `monodroid` must know which ABI the native library is built
for. There are two ways this can be done:

1.  Path "sniffing"
1.  Using a  `//AndroidNativeLibrary/Abi` element within the project file 


With path sniffing, the parent directory name of the native library is used
to specify the ABI that the library targets. Thus, if you add `lib/armeabi/libfoo.so` to the build, then the ABI will be "sniffed"
as `armeabi`.

Alternatively, you can edit your project file to explicitly specify the ABI
to use:

```
<ItemGroup>
<AndroidNativeLibrary Include="path/to/libfoo.so">  
<Abi>armeabi</Abi>  
</AndroidNativeLibrary>  
</ItemGroup>
```

 <a name="Random_Debugger_Ports" class="injected"></a>


### Random Debugger Ports

The debugger now grabs available ports from the system and uses them, so you
should no longer see "port in use" errors. If you have firewalls or complex
network routing in place, you can still specify the ports to use in
Tools-&gt;Options-&gt;MonoDroid.

 <a name="Bug_Fixes" class="injected"></a>


### Bug Fixes

-   [633465](https://bugzilla.novell.com/show_bug.cgi?id=633465%20) - Timing problem in "Select Device" dialog 
-   [633480](https://bugzilla.novell.com/show_bug.cgi?id=633480) - Debug.Writelin adds question marks to ouput text 
-   [640619](https://bugzilla.novell.com/show_bug.cgi?id=640619) - Ability to use AssetManager to access files deployed with project 
-   [645833](https://bugzilla.novell.com/show_bug.cgi?id=645833) - Renaming layout file excludes it from aresgen 
-   [648898](https://bugzilla.novell.com/show_bug.cgi?id=648898) - Missing feature constants in Window class 
-   [634817](https://bugzilla.novell.com/show_bug.cgi?id=634817) - HttpWebRequest fails on HTTPS resources 
-   [639679](https://bugzilla.novell.com/show_bug.cgi?id=639679) - StartActivity() requiring intent to have FLAG_ACTIVITY_NEW_TASK and not assuming the caller's task affinity 
-   [643202](https://bugzilla.novell.com/show_bug.cgi?id=643202) - monodroid+javac error when inheriting from an Activity that comes from a Class Library 
-   [644317](https://bugzilla.novell.com/show_bug.cgi?id=644317) - monodroid should ignore @values when generating //activity/@android:label values 
-   [645213](https://bugzilla.novell.com/show_bug.cgi?id=645213) - Cannot build project that has no activities 
-   [645255](https://bugzilla.novell.com/show_bug.cgi?id=645255) - Inheriting from Java.Lang.Object and implementing interface in abstract class won't compile 
-   [646224](https://bugzilla.novell.com/show_bug.cgi?id=646224) - TabLayout demo doesn't work 
-   [646263](https://bugzilla.novell.com/show_bug.cgi?id=646263) - Back button Force Close - Unable to stop activity 
-   [646797](https://bugzilla.novell.com/show_bug.cgi?id=646797) - Application crashes when using Async webclient call 
-   [648893](https://bugzilla.novell.com/show_bug.cgi?id=648893) - EditText.Text.ToString() doesn't give you the contents of the text field 
-   [648896](https://bugzilla.novell.com/show_bug.cgi?id=648896) - KeyEventArgs.KeyCode should use Keycode enum instead of int 
-   [640839](https://bugzilla.novell.com/show_bug.cgi?id=640839) - PreferencesActivity crash 
-   [645985](https://bugzilla.novell.com/show_bug.cgi?id=645985) - monodroid needs to support -nf=path/to/native-libs and bundle additional native libs 
-   [646424](https://bugzilla.novell.com/show_bug.cgi?id=646424) - Multiple thread pool threads cause VM crash 


&nbsp;
