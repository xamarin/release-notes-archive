---
id: 75C42A3D-AE17-4A8B-950C-46133849790F
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android.App'>Namespace: Android.App</h2>

<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, Android.Content.IComponentCallbacks2, LayoutInflater.Android.Views.IFactory, LayoutInflater.Android.Views.IFactory2, View.Android.Views.IOnCreateContextMenuListener {
```

<h3 id='Android.App.Dialog'>Type Changed: Android.App.Dialog</h3>

Removed:

```
public class Dialog : Java.Lang.Object, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Dialog : Java.Lang.Object, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IDialogInterface, View.Android.Views.IOnCreateContextMenuListener {
```

<h2 id='Android.Runtime'>Namespace: Android.Runtime</h2>

<h3 id='Android.Runtime.JNIEnv'>Type Changed: Android.Runtime.JNIEnv</h3>

Added:

```
public static IntPtr Handle {
 		get;
 	}
```
