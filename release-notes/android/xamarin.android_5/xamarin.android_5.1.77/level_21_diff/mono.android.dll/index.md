---
id: 36872E54-8560-4D53-ABEE-0ED6B88B0B1C
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
</pre>

## Namespace Android.App.Admin

### Type Changed: Android.App.Admin.WipeDataFlags

Added value:

<pre style='color: green'>
	WipeResetProtectionData = 2,
</pre>

## Namespace Android.Content

### Type Changed: Android.Content.IntentUriType

Added values:

<pre style='color: green'>
	AllowUnsafe = 4,
	AndroidAppScheme = 2,
</pre>

## Namespace Android.Hardware.Camera2

### Type Changed: Android.Hardware.Camera2.ControlSceneMode

Added value:

<pre style='color: green'>
	Hdr = 18,
</pre>

### Type Changed: Android.Hardware.Camera2.RequestAvailableCapabilities

Added values:

<pre style='color: green'>
	BurstCapture = 6,
	ReadSensorSettings = 5,
</pre>

## Namespace Android.Media

### Type Changed: Android.Media.AudioAttributes

Added property:

<pre style='color: green'>
	public AudioUsageKind Usage { get; }
</pre>

### Type Changed: Android.Media.AudioAttributes.Builder

Added method:

<pre style='color: green'>
	public virtual AudioAttributes.Builder SetUsage (AudioUsageKind usage);
</pre>

## Namespace Android.Net.Wifi.P2p

### Type Changed: Android.Net.Wifi.P2p.WifiP2pManager

Added method:

<pre style='color: green'>
	public virtual void SetServiceResponseListener (WifiP2pManager.Channel c, WifiP2pManager.IServiceResponseListener listener);
</pre>

### New Type Android.Net.Wifi.P2p.IServiceResponseListener

<pre style='color: green'>
public interface IServiceResponseListener : Android.Runtime.IJavaObject, System.IDisposable {
	// methods
	public virtual void OnServiceAvailable (Nsd.ServiceType protocolType, byte[] responseData, WifiP2pDevice srcDevice);
}
</pre>

### New Type Android.Net.Wifi.P2p.ServiceResponseEventArgs

<pre style='color: green'>
public class ServiceResponseEventArgs : System.EventArgs {
	// constructors
	public WifiP2pManager (Nsd.ServiceType protocolType, byte[] responseData, WifiP2pDevice srcDevice);
	// properties
	public Nsd.ServiceType ProtocolType { get; }
	public byte[] ResponseData { get; }
	public WifiP2pDevice SrcDevice { get; }
}
</pre>

## Namespace Android.Net.Wifi.P2p.Nsd

### Type Changed: Android.Net.Wifi.P2p.Nsd.WifiP2pServiceInfo

Obsoleted fields:

```
[Obsolete (]
	public static const ServiceType ServiceTypeAll;
	[Obsolete (]
	public static const ServiceType ServiceTypeBonjour;
	[Obsolete (]
	public static const ServiceType ServiceTypeUpnp;
	[Obsolete (]
	public static const ServiceType ServiceTypeVendorSpecific;
```

Modified fields:

```
public const int ServiceType ServiceTypeAll = 0;
	public const int ServiceType ServiceTypeBonjour = 1;
	public const int ServiceType ServiceTypeUpnp = 2;
	public const int ServiceType ServiceTypeVendorSpecific = 255;
```

### Type Changed: Android.Net.Wifi.P2p.Nsd.WifiP2pServiceRequest

Added methods:

<pre style='color: green'>
	public static WifiP2pServiceRequest NewInstance (ServiceType protocolType);
	public static WifiP2pServiceRequest NewInstance (ServiceType protocolType, string queryData);
</pre>

### New Type Android.Net.Wifi.P2p.Nsd.ServiceType

<pre style='color: green'>
[Serializable]
public enum ServiceType {
	All = 0,
	Bonjour = 1,
	Upnp = 2,
	VendorSpecific = 255,
}
</pre>

## Namespace Android.OS

### Type Changed: Android.OS.Build

### Type Changed: Android.OS.Build.VERSION_CODES

Modified fields:

```
public const BuildVersionCodes int L = 21;
```

### Type Changed: Android.OS.BuildVersionCodes

Removed value:

<pre style='color: red'>
	L = 21,
</pre>

Added value:

<pre style='color: green'>
	LollipopMr1 = 22,
</pre>

## Namespace Android.Service.Voice

### Type Changed: Android.Service.Voice.AlwaysOnHotwordDetector

Added property:

<pre style='color: green'>
	public virtual RecognitionMode SupportedRecognitionModes { get; }
</pre>

### Type Changed: Android.Service.Voice.RecognitionMode

Added value:

<pre style='color: green'>
	None = 0,
</pre>

## Namespace Android.Telephony

### Type Changed: Android.Telephony.MmsError

Added value:

<pre style='color: green'>
	NoDataNetwork = 8,
</pre>

### New Type Android.Telephony.DataRoamingMode

<pre style='color: green'>
[Serializable]
public enum DataRoamingMode {
	Disable = 0,
	Enable = 1,
}
</pre>

## Namespace Android.Util

### Type Changed: Android.Util.DisplayMetricsDensity

Added value:

<pre style='color: green'>
	D280 = 280,
</pre>

## Namespace Android.Views

### Type Changed: Android.Views.WindowManagerFlags

Added value:

<pre style='color: green'>
	LayoutAttachedInDecor = 1073741824,
</pre>

### Type Changed: Android.Views.WindowManagerTypes

Added value:

<pre style='color: green'>
	AccessibilityOverlay = 2032,
</pre>

## Namespace Android.Views.Accessibility

### Type Changed: Android.Views.Accessibility.AccessibilityWindowType

Added value:

<pre style='color: green'>
	AccessibilityOverlay = 4,
</pre>

## New Namespace Android.Service.Carrier

### New Type Android.Service.Carrier.MessageDownloadStatus

<pre style='color: green'>
[Serializable]
public enum MessageDownloadStatus {
	Error = 2,
	Ok = 0,
	RetryOnCarrierNetwork = 1,
}
</pre>

### New Type Android.Service.Carrier.MessageSendStatus

<pre style='color: green'>
[Serializable]
public enum MessageSendStatus {
	Error = 2,
	Ok = 0,
	RetryOnCarrierNetwork = 1,
}
</pre>
