---
id: D8BF06E1-7ECB-494D-8067-54909BEFEDA4
title: "Mono.Android.dll"
---

# Mono.Android.dll

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

## New Namespace Android.Hardware.Fingerprints

### New Type Android.Hardware.Fingerprints.FingerprintAuthenticationFlags

<pre style='color: green'>
[Serializable]
public enum FingerprintAuthenticationFlags {
	None = 0,
}
</pre>
