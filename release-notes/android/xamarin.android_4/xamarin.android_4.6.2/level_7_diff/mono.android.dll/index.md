---
id: E08D2796-2B6F-4549-83D3-1D98A0937432
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
