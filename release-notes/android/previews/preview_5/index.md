---
id: F820A662-911F-32C1-D20B-14633BE5EB21
title: "Preview 5"
---

This preview has a new shared runtime. To ensure you are using it, you will
need to delete the old shared runtime from your emulator/device:

Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime
-&gt; Uninstall

The new runtime will be deployed to the device the next time an application
is deployed.

&nbsp;

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless.

 <a name="Bug_Fixes_/_Enhancements" class="injected"></a>


# Bug Fixes / Enhancements

 <a name="Improved_Application_Startup" class="injected"></a>


### Improved Application Startup

This should be considered experimental, as we're unsure of the long-term
ramifications. Short term, this is very, very, cool.

All times in the table below are from the emulator, and are for demonstration
purposes only. Your timing will vary, and hardware will vastly alter things.

<blockquote>
  <table border="1" cellpadding="1" cellspacing="1" width="90%">
    <tbody>
      <tr>
        <td>
          &nbsp;
        </td>
        <td>
          Preview 4
        </td>
        <td>
          Preview 5
        </td>
        <td>
          %
        </td>
      </tr>
      <tr>
        <td>
          After Runtime + App Install
        </td>
        <td>
          24.7s
        </td>
        <td>
          <p>&nbsp;</p>

          <p>8.5s</p>

        </td>
        <td>
          34%
        </td>
      </tr>
      <tr>
        <td>
          After App Install
        </td>
        <td>
          17.5s
        </td>
        <td>
          8.5s
        </td>
        <td>
          49%
        </td>
      </tr>
      <tr>
        <td>
          Kill + Start App
        </td>
        <td>
          8.3s
        </td>
        <td>
          6.6s
        </td>
        <td>
          80%
        </td>
      </tr>
    </tbody>
  </table>
</blockquote>

 *Background*: In previous releases, assemblies were distributed within
the `.apk` file in the "root" of the ZIP package. During the first
application launch, all of the assemblies would be extracted and placed into
the [$APPDIR/files](http://developer.android.com/reference/android/content/Context.html#getFilesDir%28%29) directory. Assembly extraction is *slow*, such that if you freshly install the shared runtime and an
application, launching the application would involve extracting files from both
the shared runtime and the application, to the tune of ~25s for launching the
first time. Subsequent launches would only require ~8.3s.

Preview 5 changes the above behavior by "fooling" the Android package
installer. The Android package installer will extract all `lib/<em>ABI</em>/lib*.so` files contained within the `.apk` file without ensuring that they're actually ELF shared library
files. To coerce the Android installer to extract assemlies at installation
time, assemblies are renamed to follow the `lib*.so` convention. For
example, the assembly `Mono.Android.dll`will be stored in the `.apk` file as `lib/armeabi/libMono.Android.dll.so`, and
will be extracted by the Android installer into `$APPDIR/lib/libMono.Android.dll.so`.

The result: if you freshly install the shared runtime and an application, the
application will launch in ~8.5s (down from ~24.7s). Subsequent launches will
occur in ~6.6s, down from ~8.3s. (All times from the emulator; hardware times
will vary significantly, and in one case resulted in a "reinstall shared runtime
+ app, launch app" time of ~3s.)

This is not without its downsides: multi-ABI packages will store *all*
assemblies in *each* ABI directory, so the `.apk` file size
will grow proportional to the number of ABIs that are supported.

 <a name="Improved_Multi-ABI_Support" class="injected"></a>


### Improved Multi-ABI Support

You can pass the `--abi=ABIS` option to monodroid.exe to specify
which ABIs for native libraries should be bundled with your application. `ABIS` is a comma-separated list of ABI names. The default is `--abi=armeabi`. To include all ABIs, use `--abi=all`.

You don't need to worrry about multi-ABI support when using the shared
runtime (as the shared runtime includes all ABIs and only the appropriate one is
installed). This is useful when using the static runtime (see below), allowing
you to include support for the armeabi-v7a ABI (which provides hardware
floating-point operations).

 <a name="Logcat_Viewer" class="injected"></a>


### Logcat Viewer

Output from a device (logcat) is now available within Visual Studio. To
enable this tool window, go to View -&gt; Other Windows -&gt; Android Device
Logging.

 ![](preview_5/Images/logging.png)

   
   
   
   
   
   
   
   


 <a name="Static_Runtime_Support" class="injected"></a>


### Static Runtime Support

It is now possible generate an application which doesn't rely upon the shared
runtime by passing the `--noshared` option to [monodroid.exe](http://android.xamarin.com/Documentation/Tools/Monodroid.exe).
There is currently no IDE support for this, so to make use of this functionality
you will need to edit your project file and add the following XML fragment:

```
<PropertyGroup>     
<MonoDroidExtraArgs>--noshared</MonoDroidExtraArgs>  
</PropertyGroup>
```

 <a name="Java.Lang.CharSequence_API_Changes" class="injected"></a>


### Java.Lang.CharSequence API Changes

The CharSequence type we exposed in previous previews has been removed, and
now all API that used to expose the type exposes IEnumerable&lt;char&gt;
instead. We have added IEnumerable&lt;char&gt; to the Java.Lang.ICharSequence
inheritance chain so that you can now pass both strings and ICharSequence
implementors to these APIs without any casting, implicit or explicit.

Just as with the Java API, any API which returns a value now exposed as
IEnumerable&lt;char&gt; will have to be converted to string with ToString (), or
cast to ISpanned or one of the Android.Text classes which implement formatted
strings to do anything interesting with it directly other than passing it to
another API member.

The most likely change required to adapt existing code will be the removal of
explicit CharSequence casts which were being used as workaround for strangeness
in the previous mechanism.

 <a name="Bug_Fixes" class="injected"></a>


### Bug Fixes

-  Garbage collection is now enabled (Thanks to  [Koushik Dutta](http://twitter.com/koush) for the patch to libgc!) 
-  Release builds no longer distribute  `.mdb` debug symbols.
-   [635912](https://bugzilla.novell.com/show_bug.cgi?id=635912) - Subsequent calls to web service return null reference. 
-   [638359](https://bugzilla.novell.com/show_bug.cgi?id=638359) - Invalid cast for ISpanned to CharSequence. 
-   [640657](https://bugzilla.novell.com/show_bug.cgi?id=640657) - Crash when using RunOnUiThread with a button 
-   [642758](https://bugzilla.novell.com/show_bug.cgi?id=642758) - Replace some magic ints with available enum values. 
-   [642760](https://bugzilla.novell.com/show_bug.cgi?id=642760) - Support more types in Android.Content.ContentValues.Put() 
-   [643017](https://bugzilla.novell.com/show_bug.cgi?id=643017) - TextView.SetTextColor(...) int-&gt;enum 
-   [643202](https://bugzilla.novell.com/show_bug.cgi?id=643202) - monodroid+javac error when inheriting from an Activity that comes from a Class Library 
-   [643348](https://bugzilla.novell.com/show_bug.cgi?id=643348) - TextChanged event EditText View doesn't exist. 
-   [643360](https://bugzilla.novell.com/show_bug.cgi?id=643360) - Creating intents from activities and launching them should be easier. 
-   [643660](https://bugzilla.novell.com/show_bug.cgi?id=643660) - Make VS Errors Useful. 
-   [643677](https://bugzilla.novell.com/show_bug.cgi?id=643677) - Attempting to play an he-aac file via MediaPlayer.Create() fails. 
-   [644003](https://bugzilla.novell.com/show_bug.cgi?id=644003) - SensorEvent class is missing values array. 
-   [644004](https://bugzilla.novell.com/show_bug.cgi?id=644004) - Add method overloads for SensorType where it expects an int. 
-   [644501](https://bugzilla.novell.com/show_bug.cgi?id=644501) - System.Net.ICredentialsByHost error. 
-   [645246](https://bugzilla.novell.com/show_bug.cgi?id=645246) - View.FindViewById doesn't have a generic overload: FindViewById&lt;T&gt; 
-   [645257](https://bugzilla.novell.com/show_bug.cgi?id=645257) - Support non-IJavaObject types as generic type parameters. 
-   [645569](https://bugzilla.novell.com/show_bug.cgi?id=645569) - Delegate Exception using DatePickerDialog.
