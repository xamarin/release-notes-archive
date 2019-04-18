---
id: AC71184D-C81D-77F2-C701-40EE4C8D5845
title: "Preview 4"
---

**This preview has a new shared runtime. To ensure you are using it, you will need to delete the old shared runtime from your emulator/device:**

 **Settings -&gt; Applications -&gt; Manage Applications -&gt; MonoDroid Runtime -&gt; Uninstall**

 **The new runtime will be deployed to the device the next time an application is deployed.**

 <a name="Bug_Fixes_/_Enhancements" class="injected"></a>


# Bug Fixes / Enhancements

 <a name="Debugging_on_a_Device" class="injected"></a>


## Debugging on a Device

MonoDroid now supports debugging on a physical device. The deployment is
still done via the USB cable, but the actual debugging is done over WiFi.
Therefore, your device must be able to connect to your computer via WiFi.

MonoDroid attempts to send the device a routeable IP address for it to use,
but due to various networking conditions, this may not be possible. You can
override the IP address sent to the device with
Tools-&gt;Options-&gt;MonoDroid-&gt;Override Host IP Address

 <a name="Multi-ABI_Support" class="injected"></a>


## Multi-ABI Support

The `MonoRuntimeService.apk` package contains `libmono-2.0.so` binaries for both `armeabi` and `armeabi-v7a`. This means that on platforms which support `armeabi-v7a`, the appropriate binaries will be used. This will
permit, among other things, hardware floating-point operations on armeabi-v7a
hardware. ( *Note*: the emulator is `armeabi`, not `armeabi-v7a`, and does not support hardware-accelerated floating
point operations.)

 <a name="Bug_Fixes" class="injected"></a>


## Bug Fixes

-  633466 - Visual Studio generated web references won't compile (Settings designer) 
-  633506 - F5 when debugging displays dialog instead of continuing
-  634125 - generator needs to support abstract members
-  634492 - Open solution, try to run project  *before* build, error occurs 
-  634790 - Nasty finalizer crash related either to exception being thrown in HttpWebRequest, or problems AlertDialog 
-  637968 - RghtClick-&gt;Debug-&gt;Start New Instance
-  638067  <span title="Debugger">-</span> Support debugging to a device
-  638358  <span title="Debugger">-</span> Must have Application project selected when running in debug mode with Class Libraries 
-  640194 - Cannot override TextView.Text
-  640673 - &lt;activity&gt; icon needs to be copied to the proxy
-  640679  <span title="Runtime">-</span> Error : 'keytool' cannot be found when running with debugging 
-  640852  <span title="Tools">-</span> A Project of Type Class Library cannot be started. 
-  641112 - Strange behavoiur using the Tag attribute of Android.View
-  641170  <span title="Class Libraries">-</span> Cannot set LayoutParams in LinearLayout (and maybe other views) 
-  641677 - Attempt to change the default namespace of a project in Visual Studio causes exception 
-  641911  <span title="Tools">-</span> Debugger Fails to Attach Without Error When AndroidManifest Contains Incorrect Activity Name 
-  642758  <span title="Class Libraries">-</span> API Enhancement: Replace some magic ints with available enum value 
-  642760 - Support more types in Android.Content.ContentValues.Put()


 <a name="Breaking_API_Changes" class="injected"></a>


# Breaking API Changes

On top of the usual bug fixes, we are slowly making changes to the
Mono.Android API to make it more .NET-ish and easier to use. Unfortunately, as
pre-release users, this means you may be forced to change your code to the new
API.

 <a name="Renamed_Namespaces" class="injected"></a>


## Renamed Namespaces

-  Android.Accessibilityservices -&gt; Android.AccessibilityServices.
-  Android.Inputmethodservices -&gt; Android.InputMethodServices.
-  Android.Views.Inputmethods -&gt; Android.Views.InputMethods.
