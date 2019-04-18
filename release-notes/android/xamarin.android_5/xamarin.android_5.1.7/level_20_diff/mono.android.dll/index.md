---
id: 4D062CFC-AD6A-4D7F-8874-5A8194A708BF
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.WipeDataFlags

Removed value:

<pre style='color: red'>
	WipeResetProtectionData = 2,
</pre>

## Namespace Android.Content

### Type Changed: Android.Content.IntentUriType

Removed values:

<pre style='color: red'>
	AllowUnsafe = 4,
	AndroidAppScheme = 2,
</pre>

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

### Type Changed: Android.OS.BuildVersionCodes

Removed value:

<pre style='color: red'>
	LollipopMr1 = 22,
</pre>

### Type Changed: Android.OS.Bundle

Modified methods:

```
public bool ContainsKey (string p0 key)
	public Java.Lang.Object Get (string p0 key)
	public double GetDouble (string p0 key, double p1 defaultValue)
	public double GetDouble (string p0 key)
	public double[] GetDoubleArray (string p0 key)
	public int GetInt (string p0 key, int p1 defaultValue)
	public int GetInt (string p0 key)
	public int[] GetIntArray (string p0 key)
	public long GetLong (string p0 key)
	public long GetLong (string p0 key, long p1 defaultValue)
	public long[] GetLongArray (string p0 key)
	public string GetString (string p0 key)
	public string GetString (string p0 key, string p1 defaultValue)
	public string[] GetStringArray (string p0 key)
	public void PutDouble (string p0 key, double p1 value)
	public void PutDoubleArray (string p0 key, double[] p1 value)
	public void PutInt (string p0 key, int p1 value)
	public void PutIntArray (string p0 key, int[] p1 value)
	public void PutLong (string p0 key, long p1 value)
	public void PutLongArray (string p0 key, long[] p1 value)
	public void PutString (string p0 key, string p1 value)
	public void PutStringArray (string p0 key, string[] p1 value)
	public void Remove (string p0 key)
```

### Type Changed: Android.OS.Parcel

Modified methods:

```
protected Parcel Obtain (int p0 obj)
```

## Namespace Android.Telephony

### Removed Type  <span style='color: red'>Android.Telephony.DataRoamingMode</span>

### Removed Type  <span style='color: red'>Android.Telephony.MmsError</span>

## Namespace Android.Util

### Type Changed: Android.Util.DisplayMetricsDensity

Removed value:

<pre style='color: red'>
	D280 = 280,
</pre>

## Namespace Android.Views

### Type Changed: Android.Views.HapticFeedbackConstants

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

Added properties:

<pre style='color: green'>
	protected override IntPtr ThresholdClass { get; }
	protected override System.Type ThresholdType { get; }
</pre>

### Type Changed: Android.Views.WindowManagerFlags

Removed value:

<pre style='color: red'>
	LayoutAttachedInDecor = 1073741824,
</pre>

### Type Changed: Android.Views.WindowManagerTypes

Removed value:

<pre style='color: red'>
	AccessibilityOverlay = 2032,
</pre>

## Namespace Android.Views.Accessibility

### Removed Type  <span style='color: red'>Android.Views.Accessibility.AccessibilityWindowType</span>

## Namespace Android.Widget

### Type Changed: Android.Widget.ListView

Modified methods:

```
public virtual void SetSelectionFromTop (int p0 position, int p1 y)
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

## Removed Namespace Android.Hardware.Camera2

### Removed Type  <span style='color: red'>Android.Hardware.Camera2.ControlSceneMode</span>

### Removed Type  <span style='color: red'>Android.Hardware.Camera2.RequestAvailableCapabilities</span>

## Removed Namespace Android.Service.Carrier

### Removed Type  <span style='color: red'>Android.Service.Carrier.MessageDownloadStatus</span>

### Removed Type  <span style='color: red'>Android.Service.Carrier.MessageSendStatus</span>

## New Namespace Android.Hardware.Fingerprints

### New Type Android.Hardware.Fingerprints.FingerprintAuthenticationFlags

<pre style='color: green'>
[Serializable]
public enum FingerprintAuthenticationFlags {
	None = 0,
}
</pre>
