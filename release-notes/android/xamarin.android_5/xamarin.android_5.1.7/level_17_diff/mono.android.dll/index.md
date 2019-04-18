---
id: E2E11CD0-E481-411B-8539-F7BF92223E90
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.Protection

Modified fields:

```
MaskFlags = 240 4080
```

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
