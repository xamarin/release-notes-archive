---
id: C703135E-AC08-498D-90FF-5BDC67DE08C2
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android.App'>Namespace: Android.App</h2>

<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Removed:

```
public class Dialog : Java.Lang.Object, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Dialog : Java.Lang.Object, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

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
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, ICallback, Drawable.Android.Graphics.Drawables.ICallback {
```

Added:

```
public class View : Java.Lang.Object, Android.Views.Accessibility.IAccessibilityEventSource, Drawable.Android.Graphics.Drawables.ICallback, ICallback {
```
