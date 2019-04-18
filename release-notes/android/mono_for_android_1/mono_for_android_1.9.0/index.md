---
id: 871B42F7-65D1-645F-2E7E-A0F75338DBDD
title: "Mono For Android 1.9.0"
---

&nbsp;

This is a ** *preview*** release for the 2.0 series. We
are doing previews for 2.0 due to the large number of big changes in it. If you
are feeling adventurous, try it out and file bugs if anything goes wrong. If you
find something that impedes your work, you can uninstall this release and the
shared runtime / platform packages on your Android device, and reinstall Mono
for Android 1.2.

 <a name="" class="injected"></a>


#    
   
Installation

 **Visual Studio Users:** Download [monoandroid-1.9.0.msi](http://bit.ly/osWnGg) and install.

 **MonoDevelop Users:** To be prompted about beta updates, go to
Help-&gt;Check for Updates and set the Update Level to Beta. You should be
prompted with beta updates.

 <a name="" class="injected"></a>


#    
   
Major Highlights

 **Honeycomb Support:** We are now providing a Mono.Android.dll
for API level 12. This is a preview version, so please give us your feedback on
them if it needs some tweaks.

We also ported Honeycomb Gallery sample.

 **Interface Constant Binding Improvements**: The way that
constants within Java interfaces is exposed has been overhauled.

 **Java 7 Support:** We now correctly build, sign and deploy
packages built with Java 7. Note that if you have both installed, we still will
use Java 6 as it's more tested by the Android community.

 **Smaller Application Packages:** mono.android.jar contains
Android Callable Wrappers for many types internal to Mono.Android.dll, and is
included in every Mono for Android application package. We have rearchitected
how mono.android.jar is produced, greatly shrinking its size. The size
reductions are also visible in Mono.Android.dll and application packages.

&nbsp;

<table border="0" cellpadding="1" cellspacing="1">
  <thead>
    <tr>
      <th scope="col">
        &nbsp;
      </th>
      <th scope="col">
        1.2.0 Size
      </th>
      <th scope="col">
        1.9.0 Size
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>Mono.Android.dll, API level 8:</p>

        <p>(Pre-linking, this usually shrinks extensively)</p>

      </td>
      <td>
        8.9 MB
      </td>
      <td>
        8.7 MB
      </td>
    </tr>
    <tr>
      <td>
        mono.android.jar:
      </td>
      <td>
        348 KB
      </td>
      <td>
        86 KB
      </td>
    </tr>
    <tr>
      <td>
        Application Template .apk:
      </td>
      <td>
        185 KB
      </td>
      <td>
        103 KB
      </td>
    </tr>
    <tr>
      <td>
        Installed Size:
      </td>
      <td>
        772 KB
      </td>
      <td>
        304 KB
      </td>
    </tr>
  </tbody>
</table>

&nbsp;

 **Better Incremental Builds:** More of the build system is
implemented as MSBuild tasks. This allows us to have better incremental builds,
letting us skip pieces that don't need to be rebuilt.

<table border="0" cellpadding="1" cellspacing="10">
  <tbody>
    <tr>
      <td>
        &nbsp;
      </td>
      <td>
        <strong>1.2.0</strong>
      </td>
      <td>
        <strong>1.9.0</strong>
      </td>
    </tr>
    <tr>
      <td>
        First Build:
      </td>
      <td>
        8.66s
      </td>
      <td>
        8.19s
      </td>
    </tr>
    <tr>
      <td>
        Code Changes:
      </td>
      <td>
        5.78s
      </td>
      <td>
        1.71s
      </td>
    </tr>
    <tr>
      <td>
        Code Changes Requiring New Java Stubs:
      </td>
      <td>
        5.78s
      </td>
      <td>
        2.50s
      </td>
    </tr>
    <tr>
      <td>
        Resource Changes:
      </td>
      <td>
        8.18s
      </td>
      <td>
        6.10s
      </td>
    </tr>
  </tbody>
</table>

(Tests are run using the Debug profile of JetBoy.)   
   


 <a name="Changes_Since_Mono_for_Android_1.2.0" class="injected"></a>


# Changes Since Mono for Android 1.2.0

 <a name="API_Binding_Improvements" class="injected"></a>


## API Binding Improvements

-  Java add*Listener() methods are now bound to events.


 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-   [619](http://bugzilla.xamarin.com/show_bug.cgi?id=619) :  <span><span>LinearLayout.SetGravity( int ) should be
    GravityFlags.</span></span> 
-  Correctly handle projects that do not contain Resources.
-  It should now be possible to target API level 10 (Android v2.3.3).


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
