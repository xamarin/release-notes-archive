---
id: 243CE8CA-9287-4C80-9AF8-D7E4778EB82E
title: "Xamarin.Android 4.20"
---

The Xamarin.Android 4.20 series provides support for
[Android 5.0 Lollipop](https://developer.android.com/about/versions/android-5.0.html)
(API-21).

**Note:** Previous releases which included API-L support, such as
[Xamarin.Android 4.17](/releases/android/xamarin.android_4/xamarin.android_4.17/) and
[Xamarin.Android 4.99](/releases/android/xamarin.android_4/xamarin.android_4.99/),
allowed `L` to be used within `AndroidManifest.xml`, e.g. for the
`//uses-sdk/@android:targetSdkVersion` attribute:

    <!-- WRONG; must be corrected -->
    <uses-sdk android:minSdkVersion="4" android:targetSdkVersion="L" />

This must be *manually* updated to use `21`, as the Android SDK no longer supports
an API level of `L`:

    <!-- Please update your AndroidManifest.xml files to use 21, not L. -->
    <uses-sdk android:minSdkVersion="4" android:targetSdkVersion="21" />


**Note:** Xamarin.Android 4.20 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21.
JDK 1.6 may be used when targeting previous API levels.

<!--
  JONP: 4.20.2 last updated from commit monodroid/monodroid-4.21-series/86274adfc6418b4c3a9d67734eb871163859b51c
-->

<a name="2"/>
<a name="Xamarin.Android_4.20.2"/>
# Xamarin.Android 4.20.2

Xamarin.Android 4.20.2 fixes a crash encountered on certain devices running
Android 5.0.

## Bug Fixes

* [27408](https://bugzilla.xamarin.com/show_bug.cgi?id=27408):
    Crash in `SynchronizationContext.Post()`.


<a name="1"/>
<a name="Xamarin.Android_4.20.1"/>
# Xamarin.Android 4.20.1

Xamarin.Android 4.20.1 is a security update including important fixes for
vulnerabilities and stability in the SSL/TLS networking stack.

## Bug Fixes

* [25990](https://bugzilla.xamarin.com/show_bug.cgi?id=25990):
    JIT Crash on Lollipop with SIGSEGV error

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 3.10.1](http://www.mono-project.com/Release_Notes_Mono_3.10)
[commit f4495ef3](https://github.com/mono/mono/commit/f4495ef33e2616e6b21b1a27375e86c3df0b18af).

* [ssl/tls] Additional state validation for handshake (SKIP-TLS vulnerability) for both client/server code
* [ssl/tls] Removal of `EXPORT` ciphers (FREAK vulnerability) for both client/server code
* [ssl/tls] Removal of SSLv2 fallback (client side only, it was never supported on the server side)
* [19334](https://bugzilla.xamarin.com/show_bug.cgi?id=19334):
    Prevent crashes when a SSL/TLS connection is closed
* [23246](https://bugzilla.xamarin.com/show_bug.cgi?id=23246):
    Fix `UserInfo` string parsing.
* [22968](https://bugzilla.xamarin.com/show_bug.cgi?id=22968), [23987](https://bugzilla.xamarin.com/show_bug.cgi?id=23987):
    Crash when lazy-loading assemblies.

<!--
  JONP: 4.20.0 last updated from commit monodroid/monodroid-4.20-series/6442e95a6752fa33eca3a9ffaffbb6198ae72315
-->

<a name="0"/>
<a name="Xamarin.Android_4.20.0"/>
# Xamarin.Android 4.20.0


## New Features

* [Android 5.0 Lollipop](https://developer.android.com/about/versions/android-5.0.html)
    bindings.

## Bug Fixes

* [23804](https://bugzilla.xamarin.com/show_bug.cgi?id=23804):
    Android assets included as linked files in class libraries are not copied into the final APK bundle.
* [24147](https://bugzilla.xamarin.com/show_bug.cgi?id=24147):
    Fastdev is not fast for projects referencing android libraries, including
    support and google play services libraries

## Known Issues

* [23987](https://bugzilla.xamarin.com/show_bug.cgi?id=23987):
    Debugging *may* crash on Lollypop hardware.

## Integrated Mono Features/Fixes

Xamarin.Android uses [Mono 3.10](http://www.mono-project.com/Release_Notes_Mono_3.10)
[commit f28698ea](https://github.com/mono/mono/commit/f28698eaf362e5e0033e19e251dd699e4f09668a).

* [21653](https://bugzilla.xamarin.com/show_bug.cgi?id=21653)
    App crash when attempting to debug: Assertion, `mono_error_ok (&error)` not met.

<a name="API_Changes" />
# API Changes

* API Level 4:
    [Mono.Android.dll](xamarin.android_4.20/level_10_diff/mono.android.dll),
    [Mono.Android.GoogleMaps.dll](xamarin.android_4.20/level_10_diff/mono.android.googlemaps.dll),
    [Mono.Android.Support.v4.dll](xamarin.android_4.20/level_10_diff/mono.android.support.v4.dll),
    [OpenTK.dll](xamarin.android_4.20/level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](xamarin.android_4.20/level_10_diff/opentk-1.0.dll)
* API Level 7:
    [Mono.Android.dll](xamarin.android_4.20/level_7_diff/mono.android.dll)
* API Level 8:
    [Mono.Android.dll](xamarin.android_4.20/level_8_diff/mono.android.dll)
* API Level 10:
    [Mono.Android.dll](xamarin.android_4.20/level_10_diff/mono.android.dll)
* API Level 12:
    [Mono.Android.dll](xamarin.android_4.20/level_12_diff/mono.android.dll)
* API Level 14:
    [Mono.Android.dll](xamarin.android_4.20/level_14_diff/mono.android.dll),
    [Mono.Android.Support.v4.dll](xamarin.android_4.20/level_14_diff/mono.android.support.v13.dll)
* API Level 15:
    [Mono.Android.dll](xamarin.android_4.20/level_15_diff/mono.android.dll)
* API Level 16:
    [Mono.Android.dll](xamarin.android_4.20/level_16_diff/mono.android.dll)
* API Level 17:
    [Mono.Android.dll](xamarin.android_4.20/level_17_diff/mono.android.dll)
* API Level 18:
    [Mono.Android.dll](xamarin.android_4.20/level_18_diff/mono.android.dll)
* API Level 19:
    [Mono.Android.dll](xamarin.android_4.20/level_19_diff/mono.android.dll)
* API Level 20 vs. API Level 19:
    [Mono.Android.dll](xamarin.android_4.20/level_20_diff/mono.android.dll)
* API Level 21 vs. API Level 20:
    [Mono.Android.dll](xamarin.android_4.20/level_21_diff/mono.android.dll)

