---
id: 78B588F0-82F1-4E55-9E28-B40518B8839C
title: "Mono.Android.Support.v4.dll"
---

# Mono.Android.Support.v4.dll

## Namespace Android.Support.V4.Util

### Type Changed: Android.Support.V4.Util.LogWriter

Added interface:

```
Java.IO.ICloseable
```

## Namespace Android.Support.V4.Widget

### Type Changed: Android.Support.V4.Widget.DrawerLayout

Removed methods:

```
public virtual void CloseDrawer (int gravity);
	public virtual int GetDrawerLockMode (int edgeGravity);
	public virtual bool IsDrawerOpen (int drawerGravity);
	public virtual bool IsDrawerVisible (int drawerGravity);
	public virtual void OpenDrawer (int gravity);
	public virtual void SetDrawerShadow (Android.Graphics.Drawables.Drawable shadowDrawable, int gravity);
	public virtual void SetDrawerShadow (int resId, int gravity);
```

Added methods:

```
public virtual void CloseDrawer (Android.Views.GravityFlags gravity);
	public virtual int GetDrawerLockMode (Android.Views.GravityFlags edgeGravity);
	public virtual bool IsDrawerOpen (Android.Views.GravityFlags drawerGravity);
	public virtual bool IsDrawerVisible (Android.Views.GravityFlags drawerGravity);
	public virtual void OpenDrawer (Android.Views.GravityFlags gravity);
	public virtual void SetDrawerShadow (Android.Graphics.Drawables.Drawable shadowDrawable, Android.Views.GravityFlags gravity);
	public virtual void SetDrawerShadow (int resId, Android.Views.GravityFlags gravity);
```
