---
id: E8A1C133-7A0C-4629-8AAC-920C6A150811
title: "From 8.10.4 to 8.10.5"
---

# API diff

 [System.Data.dll](#System.Data)

   


 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='System.Data'>System.Data.dll</h1>

## Namespace System.Data.SqlClient

### Removed Type System.Data.SqlClient.SortOrder    
 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.10.4" "8.10.5";
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSData

Added methods:

```
public virtual void GetBytes (IntPtr buffer, uint length);
	public virtual void GetBytes (IntPtr buffer, NSRange range);
	public virtual NSData Subdata (NSRange range);
```

### Type Changed: MonoTouch.Foundation.NSMutableData

Added methods:

```
public virtual void ReplaceBytes (NSRange range, IntPtr buffer);
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
	public virtual void ResetBytes (NSRange range);
```

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace Foundation

### Type Changed: Foundation.NSData

Added methods:

```
public virtual void GetBytes (IntPtr buffer, uint length);
	public virtual void GetBytes (IntPtr buffer, NSRange range);
	public virtual NSData Subdata (NSRange range);
```

### Type Changed: Foundation.NSMutableData

Added methods:

```
public virtual void ReplaceBytes (NSRange range, IntPtr buffer);
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
	public virtual void ResetBytes (NSRange range);
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.10.4" "8.10.5";
```

   


 <hr>
