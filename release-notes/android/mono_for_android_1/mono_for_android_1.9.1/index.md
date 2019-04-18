---
id: 39543963-8418-2026-72D3-FF827DCC5C80
title: "Mono For Android 1.9.1"
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

 **Visual Studio Users:** Download [monoandroid-1.9.1.r2-2.msi](http://download.xamarin.com/MonoforAndroid/Windows/monoandroid-1.9.1.r2.msi) and install.

 **MonoDevelop Users:** To be prompted about beta updates, go to
Help-&gt;Check for Updates and set the Update Level to Beta. You should be
prompted with beta updates.

 <a name="" class="injected"></a>


#    
   
Changes Since Mono for Android 1.9.0

(See 1.9.0 Release Notes for changes since 1.2.0.)

 **Smarter Linker:** Our linker spent the summer at linker
community college and came away a bit smarter about what your application really
needs in order to run, resulting in a significant release .apk size
reduction.

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
        1.9.1 Size
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        Default Template Release .apk
      </td>
      <td>
        4.21 MB
      </td>
      <td>
        2.89 MB
      </td>
    </tr>
  </tbody>
</table>

&nbsp;

 **Update Notifications for Visual Studio:** Visual Studio will
now check for Mono for Android updates automatically and notify you if a new
release is available:

 ![](mono_for_android_1.9.1/Images/update1.png)

To turn this off, or to subscribe to beta release notifications, go to
Tools-&gt;Options-&gt;Mono for Android:

 ![](mono_for_android_1.9.1/Images/update2.png)

 <a name="Bug_Fixes" class="injected"></a>


# Bug Fixes

-  Fixed InvalidCastException that would result from subscribing to AndroidEnvironment.UnhandledExceptionRaiser. 
-  Fix End-Of-Stream translation in Android.Runtime.InputStreamAdapter and related types. 
-   [669](http://bugzilla.xamarin.com/show_bug.cgi?id=669) : EditText.ImeOptions should be of type Android.Views.InputMethods.ImeAction. 
-   [1052](http://bugzilla.xamarin.com/show_bug.cgi?id=1052) : Race condition in the VS plugin would cause an exception while deploying. 
-   [1148](http://bugzilla.xamarin.com/show_bug.cgi?id=1148) : EditText.IOnKeyListener.OnKey keyCode parameter should be of Keycode type. 


 <a name="Warnings" class="injected"></a>


# Warnings

Warning: Samsung shipped a broken kernel with Android 2.1, which is not able
to support JIT compilation. If you possess a Galaxy-class device with Android
2.1, you will get unexpected results, this is caused by a kernel bug that breaks
cache coherency, rendering any engine doing JIT compilation useless. Check with
your manufacturer/carrier for an Android 2.2 update.
