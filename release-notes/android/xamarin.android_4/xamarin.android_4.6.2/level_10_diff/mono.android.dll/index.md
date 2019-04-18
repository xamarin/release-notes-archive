---
id: EE30ECEB-B37B-412F-826F-464E97ED14B3
title: "Mono.Android.dll"
---

# Mono.Android.dll

<h2 id='Android.App'>Namespace: Android.App</h2>

<h3 id='Android.App.Activity'>Type Changed: Android.App.Activity</h3>

Removed:

```
public class Activity : Android.Views.ContextThemeWrapper, Window.Android.Views.ICallback, KeyEvent.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

Added:

```
public class Activity : Android.Views.ContextThemeWrapper, KeyEvent.Android.Views.ICallback, Window.Android.Views.ICallback, Android.Content.IComponentCallbacks, LayoutInflater.Android.Views.IFactory, View.Android.Views.IOnCreateContextMenuListener {
```

<h2 id='Android.Runtime'>Namespace: Android.Runtime</h2>

<h3 id='Android.Runtime.JNIEnv'>Type Changed: Android.Runtime.JNIEnv</h3>

Added:

```
public static IntPtr Handle {
 		get;
 	}
```
