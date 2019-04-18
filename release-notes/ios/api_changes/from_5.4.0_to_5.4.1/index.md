---
id: 25245466-8499-F1A6-637F-DA116CB33EAE
title: "From 5.4.0 to 5.4.1"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.4.0";
```

Added:

```
public const string Version = "5.4.1";
```

 <a name="Namespace:_MonoTouch.CoreBluetooth" class="injected"></a>


# Namespace: MonoTouch.CoreBluetooth

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentralManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate

Removed:

```
public abstract void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
```

Added:

```
public abstract void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimer" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimer

Added:

```
[Obsolete("This instance of NSTimer would be unusable. Symbol kept for binary compatibility")]
        public NSTimer ();
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
```

Added:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="New_Type:_MonoTouch.ObjCRuntime.MountainLionAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.MountainLionAttribute

```
public class MountainLionAttribute : Attribute {
        
        public MountainLionAttribute ();
}
```
