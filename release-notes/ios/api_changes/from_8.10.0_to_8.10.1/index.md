---
id: 980A32D5-2DD1-410A-B927-1C37D13FCFF5
title: "From 8.10.0 to 8.10.1"
---

# API diff

 [mscorlib.dll](#mscorlib)

   


 [(Classic) monotouch.dll](#compat/monotouch)

   


 [(Unified) Xamarin.iOS.dll](#reference/Xamarin.iOS)

   


   


 <hr>

<h1 id='mscorlib'>mscorlib.dll</h1>

## Namespace System.Runtime.InteropServices

### New Type System.Runtime.InteropServices.DefaultDllImportSearchPathsAttribute

```
public sealed class DefaultDllImportSearchPathsAttribute : System.Attribute {
	// constructors
	public DefaultDllImportSearchPathsAttribute (DllImportSearchPath paths);
	// properties
	public DllImportSearchPath Paths { get; }
}
```

### New Type System.Runtime.InteropServices.DllImportSearchPath

```
[Serializable]
[Flags]
public enum DllImportSearchPath {
	ApplicationDirectory = 512,
	AssemblyDirectory = 2,
	LegacyBehavior = 0,
	SafeDirectories = 4096,
	System32 = 2048,
	UseDllDirectoryForDependencies = 256,
	UserDirectories = 1024,
}
```

   


 <hr>

<h1 id='compat/monotouch'>monotouch.dll</h1>

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.10.0" "8.10.1";
```

   


 <hr>

<h1 id='reference/Xamarin.iOS'>Xamarin.iOS.dll</h1>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "8.10.0" "8.10.1";
```

   


 <hr>
