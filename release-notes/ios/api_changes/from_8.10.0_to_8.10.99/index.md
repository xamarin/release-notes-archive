---
id: 14749EB5-9715-48B2-A1E4-8C113E203596
title: "From 8.10.0 to 8.10.99"
---

# API diff

 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.10.0" "8.10.99";
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate

Added method:

```
public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate_Extensions

Added method:

```
public static void InitiatePlaybackOfContentItem (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentManager

Added property:

```
public virtual MPPlayableContentManagerContext Context { get; }
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentManagerContext

```
public class MPPlayableContentManagerContext : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public MPPlayableContentManagerContext ();
	public MPPlayableContentManagerContext (MonoTouch.Foundation.NSCoder coder);
	public MPPlayableContentManagerContext (MonoTouch.Foundation.NSObjectFlag t);
	public MPPlayableContentManagerContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ContentLimitsEnabled { get; }
	public virtual bool EndpointAvailable { get; }
	public virtual int EnforcedContentItemsCount { get; }
	public virtual int EnforcedContentTreeDepth { get; }
}
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added value:

```
iOS_8_4 = 525312,
```

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace MediaPlayer

### Type Changed: MediaPlayer.MPPlayableContentDelegate

Added method:

```
public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: MediaPlayer.MPPlayableContentDelegate_Extensions

Added method:

```
public static void InitiatePlaybackOfContentItem (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: MediaPlayer.MPPlayableContentManager

Added property:

```
public virtual MPPlayableContentManagerContext Context { get; }
```

### New Type MediaPlayer.MPPlayableContentManagerContext

```
public class MPPlayableContentManagerContext : Foundation.NSObject, System.IEquatable<Foundation.NSObject>, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol {
	// constructors
	public MPPlayableContentManagerContext ();
	protected MPPlayableContentManagerContext (Foundation.NSObjectFlag t);
	protected MPPlayableContentManagerContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ContentLimitsEnabled { get; }
	public virtual bool EndpointAvailable { get; }
	public virtual nint EnforcedContentItemsCount { get; }
	public virtual nint EnforcedContentTreeDepth { get; }
}
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.10.0" "8.10.99";
```

### Type Changed: ObjCRuntime.Platform

Added value:

```
iOS_8_4 = 525312,
```

   


 <hr>
