---
id: 52DD011A-6910-E46C-17CC-1A05D1FF3623
title: "from 6.0.2 to 6.0.3"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.2";
```

Added:

```
public const string Version = "6.0.3";
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

Removed:

```
public virtual MKMapRect visibleMapRect {
```

Added:

```
[Obsolete("Use VisibleMapRect")]
        public virtual MKMapRect visibleMapRect {
                get;
                set;
        }
        public virtual MKMapRect VisibleMapRect {
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

Added:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
```
