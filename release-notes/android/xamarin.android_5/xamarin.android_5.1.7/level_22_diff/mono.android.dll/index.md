---
id: AC282C98-07ED-49A9-828D-E603977A5B9F
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.Protection

Modified fields:

```
MaskFlags = 240 4080
```

## Namespace Android.Opengl

### Type Changed: Android.Opengl.GLES20

Modified methods:

```
public void GlGetActiveAttrib (int p0 program, int p1 index, int p2 bufsize, Java.Nio.IntBuffer p3 length, Java.Nio.IntBuffer p4 size, Java.Nio.IntBuffer p5 type, sbyte p6 name)
	public void GlGetActiveUniform (int p0 program, int p1 index, int p2 bufsize, Java.Nio.IntBuffer p3 length, Java.Nio.IntBuffer p4 size, Java.Nio.IntBuffer p5 type, sbyte p6 name)
	public void GlGetShaderSource (int p0 shader, int p1 bufsize, Java.Nio.IntBuffer p2 length, sbyte p3 source)
```

## Namespace Android.OS

### Type Changed: Android.OS.Bundle

Modified methods:

```
public override bool ContainsKey (string p0 key)
	public override Java.Lang.Object Get (string p0 key)
	public override double GetDouble (string p0 key)
	public override double GetDouble (string p0 key, double p1 defaultValue)
	public override double[] GetDoubleArray (string p0 key)
	public override int GetInt (string p0 key)
	public override int GetInt (string p0 key, int p1 defaultValue)
	public override int[] GetIntArray (string p0 key)
	public override long GetLong (string p0 key)
	public override long GetLong (string p0 key, long p1 defaultValue)
	public override long[] GetLongArray (string p0 key)
	public override string GetString (string p0 key)
	public override string GetString (string p0 key, string p1 defaultValue)
	public override string[] GetStringArray (string p0 key)
	public override void PutDouble (string p0 key, double p1 value)
	public override void PutDoubleArray (string p0 key, double[] p1 value)
	public override void PutInt (string p0 key, int p1 value)
	public override void PutIntArray (string p0 key, int[] p1 value)
	public override void PutLong (string p0 key, long p1 value)
	public override void PutLongArray (string p0 key, long[] p1 value)
	public override void PutString (string p0 key, string p1 value)
	public override void PutStringArray (string p0 key, string[] p1 value)
	public override void Remove (string p0 key)
```

### Type Changed: Android.OS.Parcel

Modified methods:

```
protected Parcel Obtain (int p0 obj)
```

## Namespace Android.Views

### Type Changed: Android.Views.FeedbackConstants

Added value:

<pre style='color: green'>
	ClockTick = 4,
</pre>

### Type Changed: Android.Views.HapticFeedbackConstants

Obsoleted fields:

```
[Obsolete ()]
	public static const FeedbackConstants ClockTick;
```

Modified fields:

```
public const int FeedbackConstants ClockTick = 4;
```

Added fields:

<pre style='color: green'>
	[Obsolete]
	public static const FeedbackFlags FlagIgnoreGlobalSetting;

	[Obsolete]
	public static const FeedbackFlags FlagIgnoreViewSetting;

	[Obsolete]
	public static const FeedbackConstants KeyboardTap;

	[Obsolete]
	public static const FeedbackConstants LongPress;

	[Obsolete]
	public static const FeedbackConstants VirtualKey;
</pre>

## Namespace Android.Widget

### Type Changed: Android.Widget.ListView

Modified methods:

```
public override void SetSelectionFromTop (int p0 position, int p1 y)
```

## Namespace Java.IO

### Type Changed: Java.IO.FilePermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

## Namespace Java.Net

### Type Changed: Java.Net.SocketPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 other)
```

## Namespace Java.Security

### Type Changed: Java.Security.AllPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.BasicPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.Permission

Modified methods:

```
public abstract bool Equals (Java.Lang.Object p0 obj)
```

### Type Changed: Java.Security.UnresolvedPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

## Namespace Javax.Security.Auth

### Type Changed: Javax.Security.Auth.PrivateCredentialPermission

Modified methods:

```
public override bool Equals (Java.Lang.Object p0 obj)
```

## New Namespace Android.Hardware.Fingerprints

### New Type Android.Hardware.Fingerprints.FingerprintAuthenticationFlags

<pre style='color: green'>
[Serializable]
public enum FingerprintAuthenticationFlags {
	None = 0,
}
</pre>
