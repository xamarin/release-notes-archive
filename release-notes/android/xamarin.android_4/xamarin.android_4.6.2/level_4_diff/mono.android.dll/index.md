---
id: BB098AAF-AC26-45F5-A8F5-09CE66279EC3
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android.Runtime'>Namespace: Android.Runtime</h2>

<h3 id='Android.Runtime.JNIEnv'>Type Changed: Android.Runtime.JNIEnv</h3>

Added:

```
public static IntPtr Handle {
 		get;
 	}
```

<h2 id='Android.Views'>Namespace: Android.Views</h2>

<h3 id='Android.Views.View'>Type Changed: Android.Views.View</h3>

Removed:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
```
