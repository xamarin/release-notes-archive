---
id: 68D917C4-5FB7-4879-AA3D-DFBFF8C5C68F
title: "From 7.1.1 to 7.1.2"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.1.1";
```

Added fields:

```
public static const string Version = "7.1.2";
```

## Namespace MonoTouch.MediaPlayer

### New Type MonoTouch.MediaPlayer.MPFeedbackCommandEvent

```
public class MPFeedbackCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPFeedbackCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPFeedbackCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPFeedbackCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Negative { get; }
}
```

   


 <hr>
