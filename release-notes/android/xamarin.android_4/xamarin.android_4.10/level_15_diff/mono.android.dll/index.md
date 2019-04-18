---
id: 53DA4291-28D7-4F1B-91D1-F0AA0BBEA480
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
