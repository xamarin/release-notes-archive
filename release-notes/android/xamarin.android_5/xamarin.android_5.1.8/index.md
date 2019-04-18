---
id: 1F765063-0C23-42F3-AAD8-54F347694275
title: "Xamarin.Android 5.1.8"
---

The Xamarin.Android 5.1 series provides improved support for
[Android Wear apps](https://developer.android.com/design/wear/structure.html).

**Note:** Xamarin.Android 5.1 requires
[JDK 1.7](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
to use Android Wear and API-21.
JDK 1.6 may be used when targeting previous API levels.


<!--
  JONP: 5.1.8 last updated from commit monodroid/monodroid-5.1-series-android-mnc/146daa26c9d1cecf5fe7426083d88ceef56e8d51
-->

<a name="8"/>
<a name="Xamarin.Android_5.1.8"/>
# Xamarin.Android 5.1.8

Xamarin.Android 5.1.8 is a *hotfix release* over [Xamarin.Android 5.1.7][xa-5.1.7]
to fix a crash within `mandroid`.

[xa-5.1.7]: /releases/android/xamarin.android_5/xamarin.android_5.1.7/


<a name="Bug_Fixes" />
# Bug Fixes

* [35006](https://bugzilla.xamarin.com/show_bug.cgi?id=35006):
    `mandroid --datafile` command sometimes fails in
    `System.Text.Encoding.GetDataItem()`.


