---
id: A9565034-D340-4775-96A6-7459052C4064
title: "From 8.6.0 to 8.6.1"
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
public const string Version = "8.6.0" "8.6.1";
```

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.6.0" "8.6.1";
```

## Namespace System

### Type Changed: System.nfloat

Added constructors:

```
public nfloat (float v);
	public nfloat (double v);
```

### Type Changed: System.nint

Added constructors:

```
public nint (int v);
	public nint (long v);
```

### Type Changed: System.nuint

Added constructors:

```
public nuint (uint v);
	public nuint (ulong v);
```

   


 <hr>
