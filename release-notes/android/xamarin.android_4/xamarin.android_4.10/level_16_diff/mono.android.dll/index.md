---
id: D6139EB7-A2EC-4592-B306-8DBA913F10AF
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android

### Type Changed: Android.IncludeAndroidResourcesFromAttribute

Added properties:

```
public string SourceUrl { get; set; }
	public string Version { get; set; }
```

## Namespace Android.AccessibilityServices

### New Type Android.AccessibilityServices.AccessibilityServiceCapabilities

```
[Serializable]
public enum AccessibilityServiceCapabilities {
	None = 0,
}
```

## Namespace Android.App

### Type Changed: Android.App.FragmentManager

Added methods:

```
public T FindFragmentByTag<T> (string tag);
	public T GetFragment<T> (Android.OS.Bundle bundle, string key);
```

### Type Changed: Android.App.MediaRouteActionProvider

Added methods:

```
public virtual void SetRouteTypes (Android.Media.MediaRouteType types);
```

### Type Changed: Android.App.MediaRouteButton

Added properties:

```
public virtual Android.Media.MediaRouteType RouteTypes { get; set; }
```

## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.ActivityInfoFlags

Added values:

```
None = 0,
```

## Namespace Android.Hardware.Usb

### Type Changed: Android.Hardware.Usb.UsbDeviceConnection

Added methods:

```
public System.Threading.Tasks.Task<int> ControlTransferAsync (UsbAddressing requestType, int request, int value, int index, System.Byte[] buffer, int length, int timeout);
```

## Namespace Android.Media

### Type Changed: Android.Media.MediaRouter

### Type Changed: Android.Media.MediaRouter.UserRouteInfo

Removed methods:

```
public virtual void SetPlaybackStream (int stream);
```

Added methods:

```
[Obsolete ("Use SetPlaybackStream(Android.Media.Stream)")]
	public void SetPlaybackStream (int stream);

	public virtual void SetPlaybackStream (Stream stream);
```

## Namespace Android.Media.Audiofx

### Type Changed: Android.Media.Audiofx.Visualizer

Added properties:

```
public virtual VisualizerScalingMode ScalingMode { get; }
```

Added methods:

```
public virtual int SetScalingMode (VisualizerScalingMode mode);
```

## Namespace Android.Runtime

### Type Changed: Android.Runtime.JNIEnv

Added methods:

```
public static void CheckHandle (System.IntPtr jnienv);
	public static System.IntPtr GetObjectArrayElement (System.IntPtr array, int index);
	public static void SetObjectArrayElement (System.IntPtr array, int index, System.IntPtr value);
```

## Namespace Android.Telephony

### Type Changed: Android.Telephony.PhoneNumberUtils

Removed fields:

```
public static const int TOAInternational;
	public static const int TOAUnknown;
```

Added fields:

```
[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.PhoneNumberToa enum directly instead of this field.")]
	public static const PhoneNumberToa TOAInternational;

	[Obsolete ("This constant will be removed in the future version. Use Android.Telephony.PhoneNumberToa enum directly instead of this field.")]
	public static const PhoneNumberToa TOAUnknown;
```

Removed methods:

```
public static string StringFromStringAndTOA (string s, int TOA);
```

Added methods:

```
public static string StringFromStringAndTOA (string s, PhoneNumberToa TOA);
```

### New Type Android.Telephony.PhoneNumberToa

```
[Serializable]
public enum PhoneNumberToa {
	International = 145,
	Unknown = 129,
}
```

## Namespace Android.Widget

### Type Changed: Android.Widget.AbsListView

Added properties:

```
public override IListAdapter Adapter { get; set; }
```

Removed methods:

```
public virtual void SetAdapter (IListAdapter adapter);
```

Added methods:

```
[Obsolete ("Please use the Adapter property setter")]
	public virtual void SetAdapter (IListAdapter adapter);
```

### Type Changed: Android.Widget.GridLayout

Added properties:

```
public static GridLayout.Alignment BaselineAlighment { get; set; }
	public static GridLayout.Alignment BottomAlighment { get; set; }
	public static GridLayout.Alignment LeftAlighment { get; set; }
	public static GridLayout.Alignment RightAlighment { get; set; }
	public static GridLayout.Alignment TopAlighment { get; set; }
```

## Namespace Java.Interop

### Type Changed: Java.Interop.ExportAttribute

Added properties:

```
public string SuperArgumentsString { get; set; }
```

### Type Changed: Java.Interop.JavaLibraryReferenceAttribute

Added properties:

```
public string SourceUrl { get; set; }
	public string Version { get; set; }
```

## Namespace Java.Lang

### Type Changed: Java.Lang.Object

Added methods:

```
public static T GetObject<T> (System.IntPtr jnienv, System.IntPtr handle, Android.Runtime.JniHandleOwnership transfer);
```

### Type Changed: Java.Lang.Throwable

Added properties:

```
public Class Class { get; }
```
