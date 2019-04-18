---
id: 59493568-35C8-4C1A-A9FF-37466EE9E215
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







## Namespace Android.Bluetooth.LE

### Type Changed: Android.Bluetooth.LE.ScanRecord

Modified properties:

```
public AdvertiseTx int TxPowerLevel { get; }
```





## Namespace Android.Content.PM

### Type Changed: Android.Content.PM.Protection

Modified fields:

```
MaskFlags = 4080 65520
```





## Namespace Android.Content.Res

### Type Changed: Android.Content.Res.AssetManager

Added interface:

```
Java.Lang.IAutoCloseable
```







## Namespace Android.Graphics.Pdf

### Type Changed: Android.Graphics.Pdf.PdfRenderer

Added interface:

```
Java.Lang.IAutoCloseable
```



### Type Changed: Android.Graphics.Pdf.PdfRenderer.Page

Added interface:

```
Java.Lang.IAutoCloseable
```









## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.CameraCaptureSession

Added interface:

```
Java.Lang.IAutoCloseable
```





### Type Changed: Android.Hardware.Camera2.CameraDevice

Added interface:

```
Java.Lang.IAutoCloseable
```





### Type Changed: Android.Hardware.Camera2.DngCreator

Added interface:

```
Java.Lang.IAutoCloseable
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





### Type Changed: Android.Media.VolumeProvider

Added constructor:

```
public VolumeProvider (VolumeControl volumeControl, int maxVolume, int currentVolume);
```



Added property:

```
public VolumeControl VolumeControl { get; }
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
