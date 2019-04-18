---
id: 1EA3E865-24AE-46F8-B982-1DA04C57D0F0
title: "Mono.Android.GoogleMaps.dll"
---

# Mono.Android.GoogleMaps.dll

## Namespace Android.GoogleMaps

### Type Changed: Android.GoogleMaps.MapView

Removed method:

```
public virtual void OnFocusChanged (bool hasFocus, int direction, Android.Graphics.Rect unused);
```

Added method:

```
public virtual void OnFocusChanged (bool hasFocus, Android.Views.FocusSearchDirection direction, Android.Graphics.Rect unused);
```
