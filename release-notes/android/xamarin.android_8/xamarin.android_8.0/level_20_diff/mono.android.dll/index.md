---
id: A615E8F6-0983-4702-A302-8E1E25AB0023
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.App

### Type Changed: Android.App.Importance

Modified fields:

```
Perceptible = 130 230
```





## Namespace Android.Bluetooth

### Type Changed: Android.Bluetooth.BluetoothGattServerCallback

Obsoleted methods:

```
[Obsolete ("Use OnServiceAdded(Android.Bluetooth.GattStatus, Android.Bluetooth.BluetoothGattService)")]
	public virtual void OnServiceAdded (ProfileState status, BluetoothGattService service);
```

Added method:

```
public virtual void OnServiceAdded (GattStatus status, BluetoothGattService service);
```







## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.Protection

Modified fields:

```
MaskFlags = 4080 65520
```





## Namespace Android.Media

### Type Changed: Android.Media.Image

Added interface:

```
Java.Lang.IAutoCloseable
```





### Type Changed: Android.Media.ImageReader

Added interface:

```
Java.Lang.IAutoCloseable
```







## Namespace Android.Views

### New Type Android.Views.AutofillFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum AutofillFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>





## Namespace Java.Nio.Channels

### Type Changed: Java.Nio.Channels.FileLock

Added interface:

```
Java.Lang.IAutoCloseable
```







## Removed Namespace Android.Service.Quicksettings

### Removed Type  <span class='breaking' data-is-breaking="">Android.Service.Quicksettings.TileState</span>



## New Namespace Android.Service.Autofill

### New Type Android.Service.Autofill.SaveFlags

<pre class='added' data-is-non-breaking="">
[Serializable]
public enum SaveFlags {
	<span class='added added-field ' data-is-non-breaking="">None = 0,</span>
}
</pre>
