---
id: 6B7294F4-F84E-47BF-9D23-EA815A0B8E35
title: "Mono.Android.GoogleMaps.dll"
---

<a name="Mono.Android.GoogleMaps.dll" class="injected"></a>


# Mono.Android.GoogleMaps.dll

 <a name="Namespace:_Android.GoogleMaps" class="injected"></a>


<h2 id='Android.GoogleMaps'>Namespace: Android.GoogleMaps</h2>

 <a name="Type_Changed:_Android.GoogleMaps.MapView" class="injected"></a>


<h3 id='Android.GoogleMaps.MapView'>Type Changed: Android.GoogleMaps.MapView</h3>

Removed:

```
protected override void OnDraw (Android.Graphics.Canvas canvas);
 	protected override void OnMeasure (int widthMeasureSpec, int heightMeasureSpec);
```

Added:

```
protected void OnDraw (Android.Graphics.Canvas canvas);
 	protected void OnMeasure (int widthMeasureSpec, int heightMeasureSpec);
```
