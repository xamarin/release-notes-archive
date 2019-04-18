---
id: 708493BD-54F7-427D-84F2-5D21E0E964B9
title: "From 7.1.3 to 7.1.5"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.1.3";
```

Added fields:

```
public static const string Version = "7.1.5";
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPRemoteCommand

Removed methods:

```
public virtual MonoTouch.Foundation.NSObject AddTarget (System.Action<MPRemoteCommandEvent> handler);
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject AddTarget (System.Func<MPRemoteCommandEvent,MonoTouch.MediaPlayer.MPRemoteCommandHandlerStatus> handler);
```

   


 <hr>
