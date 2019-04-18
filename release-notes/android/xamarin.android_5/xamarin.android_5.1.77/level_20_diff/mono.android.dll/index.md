---
id: 00192C09-53A2-417F-9B84-9A05351B4689
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

### Type Changed: Android.OS.BuildVersionCodes

Added value:

<pre style='color: green'>
	LollipopMr1 = 22,
</pre>

## Namespace Android.Service.Voice

### New Type Android.Service.Voice.RecognitionMode

<pre style='color: green'>
[Serializable]
public enum RecognitionMode {
	None = 0,
}
</pre>

## Namespace Android.Telephony

### New Type Android.Telephony.DataRoamingMode

<pre style='color: green'>
[Serializable]
public enum DataRoamingMode {
	Disable = 0,
	Enable = 1,
}
</pre>

### New Type Android.Telephony.MmsError

<pre style='color: green'>
[Serializable]
public enum MmsError {
	NoDataNetwork = 8,
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

### New Type Android.Views.Accessibility.AccessibilityWindowType

<pre style='color: green'>
[Serializable]
public enum AccessibilityWindowType {
	AccessibilityOverlay = 4,
}
</pre>

## New Namespace Android.Hardware.Camera2

### New Type Android.Hardware.Camera2.ControlSceneMode

<pre style='color: green'>
[Serializable]
public enum ControlSceneMode {
	Hdr = 18,
}
</pre>

### New Type Android.Hardware.Camera2.RequestAvailableCapabilities

<pre style='color: green'>
[Serializable]
public enum RequestAvailableCapabilities {
	BurstCapture = 6,
	ReadSensorSettings = 5,
}
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
