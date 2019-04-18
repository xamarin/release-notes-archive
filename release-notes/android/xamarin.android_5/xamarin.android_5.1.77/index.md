---
id: 08A83F19-5B8C-42AF-ABA9-2CF710BB2AA2
title: "Xamarin.Android 5.1.77"
---

**Note:**: The Xamarin.Android 5.1.77 series has been *superseded* by
[Xamarin.Android 5.1.7][xa-5.1.7], which contains a binding of the final
Android M preview, which Google says is final and stable.

[xa-5.1.7]: http://developer.xamarin.com/releases/android/xamarin.android_5/xamarin.android_5.1/#7


**THE Xamarin.Android 5.1.77 SERIES IS OBSOLETE**

The Xamarin.Android 5.1.77 series contains preview bindings for
[Android 5.1][api-22] and the [Android M Developer Preview][api-mnc].

[api-22]: https://developer.android.com/about/versions/android-5.1.html
[api-mnc]: https://developer.android.com/preview/api-overview.html

**Note:** Xamarin.Android 5.1.77 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html).
JDK 1.6 may be used when targeting API-19 and lower.

In order to deploy to an Android MNC device and use Android MNC APIs,
`Properties\AndroidManifest.xml` must be updated to set the
`android:minSdkVersion` and `android:minSdkVersion` values to `MNC`:

	<uses-sdk android:minSdkVersion="MNC" android:targetSdkVersion="MNC" />

There is currently no IDE support for setting this; it may be provided in a future IDE release.

**Note**: Xamarin.Android 5.1.77 *will never be* a stable release, so don't
wait for it. I have little faith that there won't be API changes to API-M
before it becomes stable...*whenever* it becomes stable...

The v5.2 target framework API is *unstable*, and *will* change until API-M becomes a
properly stable API-23.

<!--
  JONP: 5.1.77-8 last updated from commit monodroid/monodroid-5.1-api-mnc-preview-c5sr2/09ca6e83c7265c5f3a4e4f2eda6cf6a61407478c
-->

# Xamarin.Android 5.1.77-8

Xamarin.Android 5.1.77-8 updates the bindings to use
[Android M Developer Preview 2](https://developer.android.com/preview/overview.html).

<!--
  JONP: 5.1.77-0 last updated from commit monodroid/monodroid-5.1-api-mnc-preview-c5sr2/fceb3959b3eddc2612e416a1e071515c15c4fcd5
-->

# Xamarin.Android 5.1.77-0

Xamarin.Android 5.1.77-0 is based on [Xamarin.Android 5.1.4][c5sr2], and binds
[Android M Developer Preview 1][m1]

[c5sr2]: http://developer.xamarin.com/releases/android/xamarin.android_5/xamarin.android_5.1/#4
[m1]: https://developer.android.com/preview/download_mp1.html

## New Features


* Preview support for [Android 5.1][api-22] by setting
    `$(TargetFrameworkVersion)` to `v5.1`.
* Preview support for [Android M Developer Preview][api-mnc] by setting
    `$(TargetFrameworkVersion)` to `v5.2` and updating the `<uses-sdk/>` value.


<a name="API_Changes" />
# API Changes

* API Level 10:
    [Mono.Android.dll](level_10_diff/mono.android.dll),
    [OpenTK.dll](level_10_diff/opentk.dll),
    [OpenTK-1.0.dll](level_10_diff/opentk-1.0.dll)
* API Level 15:
    [Mono.Android.dll](level_15_diff/mono.android.dll)
* API Level 16:
    [Mono.Android.dll](level_16_diff/mono.android.dll)
* API Level 17:
    [Mono.Android.dll](level_17_diff/mono.android.dll)
* API Level 18:
    [Mono.Android.dll](level_18_diff/mono.android.dll)
* API Level 19:
    [Mono.Android.dll](level_19_diff/mono.android.dll)
* API Level 20:
    [Mono.Android.dll](level_20_diff/mono.android.dll)
* API Level 21:
    [Mono.Android.dll](level_21_diff/mono.android.dll)
* API Level 22 (vs. API-21):
    [Mono.Android.dll](level_22_diff/mono.android.dll)
* API Level 23 (vs. API-22):
    [Mono.Android.dll](level_23_diff/mono.android.dll)

