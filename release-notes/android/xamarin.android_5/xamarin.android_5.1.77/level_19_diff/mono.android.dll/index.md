---
id: D318D6A1-9C0D-4F58-9A76-F8E4892C3A4C
title: "Mono.Android.dll"
---

# Mono.Android.dll

## Namespace Android.AccessibilityServices

### Type Changed: Android.AccessibilityServices.AccessibilityServiceInfo

Added method:

<pre style='color: green'>
	public static string FeedbackTypeToString (FeedbackFlags feedbackType);
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

## Namespace Android.Service.Voice

### New Type Android.Service.Voice.RecognitionMode

<pre style='color: green'>
[Serializable]
public enum RecognitionMode {
	None = 0,
}
</pre>
