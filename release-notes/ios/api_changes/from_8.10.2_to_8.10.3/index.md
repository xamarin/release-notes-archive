---
id: 6351B8E3-57A4-4235-B28E-57878583AE72
title: "From 8.10.2 to 8.10.3"
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
public const string Version = "8.10.2" "8.10.3";
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public virtual void PlayableContentManager (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void ContextUpdated (MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.MediaPlayer.MPPlayableContentDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public static void PlayableContentManager (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public static void ContextUpdated (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
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

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public virtual void PlayableContentManager (MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void ContextUpdated (MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
	public virtual void InitiatePlaybackOfContentItem (MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: MediaPlayer.MPPlayableContentDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use InitiatePlaybackOfContentItem instead"]
	public static void PlayableContentManager (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, Foundation.NSIndexPath indexPath, System.Action<Foundation.NSError> completionHandler);
```

Added methods:

```
public static void ContextUpdated (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MPPlayableContentManagerContext context);
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
public const string Version = "8.10.2" "8.10.3";
```

### Type Changed: ObjCRuntime.Platform

Added value:

```
iOS_8_4 = 525312,
```

   


 <hr>
