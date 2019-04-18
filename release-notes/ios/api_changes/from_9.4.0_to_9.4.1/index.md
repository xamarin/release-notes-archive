---
id: 361D3046-667F-4913-BC93-4ABE213F335D
title: "From 9.4.0 to 9.4.1"
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
public const string Version = "9.4.0" "9.4.1";
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGDataProvider

Obsoleted constructors:

```
[Obsolete ()]
	public CGDataProvider (IntPtr memoryBlock, int size);
```

Added constructors:

<pre style='color: green'>
	public CGDataProvider (byte[] buffer);
	public CGDataProvider (IntPtr memoryBlock, int size, System.Action&lt;IntPtr&gt; releaseMemoryBlockCallback);
</pre>

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_STRET = 536870912,
</pre>

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGDataProvider

Obsoleted constructors:

```
[Obsolete ()]
	public CGDataProvider (IntPtr memoryBlock, int size);
```

Added constructors:

<pre style='color: green'>
	public CGDataProvider (byte[] buffer);
	public CGDataProvider (IntPtr memoryBlock, int size, System.Action&lt;IntPtr&gt; releaseMemoryBlockCallback);
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_STRET = 536870912,
</pre>

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "9.4.0" "9.4.1";
```

   


 <hr>
