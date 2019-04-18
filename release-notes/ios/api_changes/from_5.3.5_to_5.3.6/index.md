---
id: BBC50A4E-1792-444F-A5B0-68148E9285FA
title: "From 5.3.5 to 5.3.6"
---

## Namespace: MonoTouch

### Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.3.5";
```

Added:

```
public const string Version = "5.3.6";
```

## Namespace: MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVCaptureOutput

Removed:

```
public virtual MonoTouch.Foundation.NSObject[] Connections {
```

Added:

```
public virtual AVCaptureConnection[] Connections {
```

## Namespace: MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Added:

```
public void RetrievePeripherals (CBUUID[] peripheralUuids);
 	public void ScanForPeripherals (CBUUID[] peripheralUuids, MonoTouch.Foundation.NSDictionary options);
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Added:

```
public void DiscoverCharacteristics (CBUUID[] charactersticUUIDs, CBService forService);
 	public void DiscoverIncludedServices (CBUUID[] includedServiceUUIDs, CBService forService);
 	public void DiscoverServices (CBUUID[] services);
```

## Namespace: MonoTouch.CoreFoundation

### New Type: MonoTouch.CoreFoundation.CFIndex

```
public struct CFIndex {
	
	public static implicit operator int (CFIndex index);
	public static implicit operator CFIndex (int value);
	public static implicit operator long (CFIndex index);
}
```

### New Type: MonoTouch.CoreFoundation.CFReadStream

```
public class CFReadStream : CFStream {
	
	public CFReadStream (IntPtr handle);
	
	protected override void DoClose ();
	protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected override CFStreamStatus DoGetStatus ();
	protected override bool DoOpen ();
	protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public override CFException GetError ();
	public bool HasBytesAvailable ();
	public int Read (byte [] buffer);
	public int Read (byte [] buffer, int offset, int count);
	protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
}
```

### Type Changed: MonoTouch.CoreFoundation.CFRunLoop

Added:

```
public void AddSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
 	public bool ContainsSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
 	public bool RemoveSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
```

### New Type: MonoTouch.CoreFoundation.CFRunLoopSource

```
public class CFRunLoopSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public void Dispose ();
	public virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public void Invalidate ();
	public void Signal ();
	
	public IntPtr Handle {
		get;
	}
	public bool IsValid {
		get;
	}
	public int Order {
		get;
	}
}
```

### New Type: MonoTouch.CoreFoundation.CFRunLoopSourceCustom

```
public abstract class CFRunLoopSourceCustom : CFRunLoopSource {
	
	protected CFRunLoopSourceCustom ();
	
	public override void Dispose (bool disposing);
	protected abstract void OnCancel (CFRunLoop loop, string mode);
	protected abstract void OnPerform ();
	protected abstract void OnSchedule (CFRunLoop loop, string mode);
}
```

### New Type: MonoTouch.CoreFoundation.CFSocket

```
public class CFSocket : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public CFSocket ();
	public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto);
	public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, CFRunLoop loop);
	
	public static CFSocket CreateConnectedToSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, double timeout);
	public void Connect (System.Net.IPAddress address, int port, double timeout);
	public void Connect (System.Net.IPEndPoint endpoint, double timeout);
	public void DisableCallBacks (CFSocketCallBackType types);
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void EnableCallBacks (CFSocketCallBackType types);
	protected override void Finalize ();
	public CFSocketFlags GetSocketFlags ();
	public void SendData (byte [] data, double timeout);
	public void SetAddress (System.Net.IPAddress address, int port);
	public void SetAddress (System.Net.IPEndPoint endpoint);
	public void SetSocketFlags (CFSocketFlags flags);
	
	public IntPtr Handle {
		get;
	}
	
	public event EventHandler AcceptEvent;
	public event EventHandler ConnectEvent;
	
	public class CFSocketAcceptEventArgs : EventArgs {
		
		public CFSocketAcceptEventArgs (CFSocketNativeHandle handle, System.Net.IPEndPoint remote);
		
		public CFSocket CreateSocket ();
		public override string ToString ();
		
		public System.Net.IPEndPoint RemoteEndPoint {
			get;
		}
	}
	public class CFSocketConnectEventArgs : EventArgs {
		
		public CFSocketConnectEventArgs (CFSocketError result);
		
		public override string ToString ();
		
		public CFSocketError Result {
			get;
		}
	}
}
```

### New Type: MonoTouch.CoreFoundation.CFSocketCallBackType

```
[Serializable]
[Flags]
public enum CFSocketCallBackType {
	NoCallBack,
	ReadCallBack,
	AcceptCallBack,
	DataCallBack,
	ConnectCallBack,
	WriteCallBack
}
```

### New Type: MonoTouch.CoreFoundation.CFSocketError

```
[Serializable]
public enum CFSocketError {
	Success,
	Error,
	Timeout
}
```

### New Type: MonoTouch.CoreFoundation.CFSocketException

```
public class CFSocketException : Exception {
	
	public CFSocketException (CFSocketError error);
	
	public CFSocketError Error {
		get;
	}
}
```

### New Type: MonoTouch.CoreFoundation.CFSocketFlags

```
[Serializable]
[Flags]
public enum CFSocketFlags {
	AutomaticallyReenableReadCallBack,
	AutomaticallyReenableAcceptCallBack,
	AutomaticallyReenableDataCallBack,
	AutomaticallyReenableWriteCallBack,
	LeaveErrors,
	CloseOnInvalidate
}
```

### New Type: MonoTouch.CoreFoundation.CFSocketNativeHandle

```
public struct CFSocketNativeHandle {
	
	public override string ToString ();
}
```

### New Type: MonoTouch.CoreFoundation.CFStream

```
public abstract class CFStream : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	protected CFStream (IntPtr handle);
	
	public static void CreateBoundPair (out CFReadStream readStream, out CFWriteStream writeStream, int bufferSize);
	public static MonoTouch.CoreServices.CFHTTPStream CreateForHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request);
	public static MonoTouch.CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request, CFReadStream body);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
	public static void CreatePairWithSocket (CFSocket socket, out CFReadStream readStream, out CFWriteStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
	protected void CheckError ();
	protected void CheckHandle ();
	public void Close ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected abstract void DoClose ();
	protected abstract IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected abstract CFStreamStatus DoGetStatus ();
	protected abstract bool DoOpen ();
	protected abstract bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected abstract bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public void EnableEvents (CFRunLoop runLoop, MonoTouch.Foundation.NSString runLoopMode);
	protected override void Finalize ();
	public abstract CFException GetError ();
	public CFStreamStatus GetStatus ();
	protected virtual void OnCallback (CFStreamEventType type);
	protected virtual void OnCanAcceptBytesEvent (StreamEventArgs args);
	protected virtual void OnClosedEvent (StreamEventArgs args);
	protected virtual void OnErrorEvent (StreamEventArgs args);
	protected virtual void OnHasBytesAvailableEvent (StreamEventArgs args);
	protected virtual void OnOpenCompleted (StreamEventArgs args);
	public void Open ();
	protected abstract void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected abstract void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	
	public IntPtr Handle {
		get;
	}
	
	public event EventHandler CanAcceptBytesEvent;
	public event EventHandler ClosedEvent;
	public event EventHandler ErrorEvent;
	public event EventHandler HasBytesAvailableEvent;
	public event EventHandler OpenCompletedEvent;
	
	[Serializable]
	protected delegate void CFStreamCallback (IntPtr s, CFStreamEventType type, IntPtr info);
	public class StreamEventArgs : EventArgs {
		
		public StreamEventArgs (CFStreamEventType type);
		
		public override string ToString ();
		
		public CFStreamEventType EventType {
			get;
		}
	}
}
```

### New Type: MonoTouch.CoreFoundation.CFStreamStatus

```
[Serializable]
public enum CFStreamStatus {
	NotOpen,
	Opening,
	Open,
	Reading,
	Writing,
	AtEnd,
	Closed,
	Error
}
```

### Type Changed: MonoTouch.CoreFoundation.CFUrl

Removed:

```
public class CFUrl : IDisposable {
```

Added:

```
public class CFUrl : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
 	public static int GetTypeID ();
```

### New Type: MonoTouch.CoreFoundation.CFWriteStream

```
public class CFWriteStream : CFStream {
	
	public bool CanAcceptBytes ();
	protected override void DoClose ();
	protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
	protected override CFStreamStatus DoGetStatus ();
	protected override bool DoOpen ();
	protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
	protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
	public override CFException GetError ();
	protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
	public int Write (byte [] buffer);
	public int Write (byte [] buffer, int offset, int count);
}
```

## Namespace: MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIContext

Removed:

```
public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx);
 	public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx, CIContextOptions options);
 	public MonoTouch.CoreGraphics.CGLayer CreateCGLayer (System.Drawing.SizeF size);
```

## Namespace: MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLError

Added:

```
RegionMonitoringResponseDelayed,
 	GeocodeFoundNoResult,
 	GeocodeFoundPartialResult,
 	GeocodeCanceled
```

## Namespace: MonoTouch.CoreServices

### New Type: MonoTouch.CoreServices.CFHTTPAuthentication

```
public class CFHTTPAuthentication : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public static CFHTTPAuthentication CreateFromResponse (CFHTTPMessage response);
	public static int GetTypeID ();
	public bool AppliesToRequest (CFHTTPMessage request);
	protected void CheckHandle ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public string GetMethod ();
	
	public IntPtr Handle {
		get;
	}
	public bool IsValid {
		get;
	}
	public bool RequiresAccountDomain {
		get;
	}
	public bool RequiresOrderedRequests {
		get;
	}
	public bool RequiresUserNameAndPassword {
		get;
	}
}
```

### New Type: MonoTouch.CoreServices.CFHTTPMessage

```
public class CFHTTPMessage : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public static CFHTTPMessage CreateRequest (MonoTouch.CoreFoundation.CFUrl url, MonoTouch.Foundation.NSString method, Version version);
	public static CFHTTPMessage CreateRequest (Uri uri, string method);
	public static CFHTTPMessage CreateRequest (Uri uri, string method, Version version);
	public static int GetTypeID ();
	public bool AddAuthentication (CFHTTPMessage failureResponse, MonoTouch.Foundation.NSString username, MonoTouch.Foundation.NSString password, AuthenticationScheme scheme, bool forProxy);
	public void ApplyCredentialDictionary (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
	public void ApplyCredentials (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
	protected void CheckHandle ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public MonoTouch.Foundation.NSDictionary GetAllHeaderFields ();
	public void SetBody (byte [] buffer);
	public void SetHeaderFieldValue (string name, string value);
	
	public IntPtr Handle {
		get;
	}
	public bool IsHeaderComplete {
		get;
	}
	public bool IsRequest {
		get;
	}
	public System.Net.HttpStatusCode ResponseStatusCode {
		get;
	}
	public string ResponseStatusLine {
		get;
	}
	public Version Version {
		get;
	}
	
	[Serializable]
	public enum AuthenticationScheme {
		Default,
		Basic,
		Negotiate,
		NTLM,
		Digest
	}
}
```

### New Type: MonoTouch.CoreServices.CFHTTPStream

```
public class CFHTTPStream : MonoTouch.CoreFoundation.CFReadStream {
	
	public CFHTTPMessage GetFinalRequest ();
	public CFHTTPMessage GetResponseHeader ();
	
	public bool AttemptPersistentConnection {
		get;
		set;
	}
	public Uri FinalURL {
		get;
	}
	public int RequestBytesWrittenCount {
		get;
	}
	public bool ShouldAutoredirect {
		get;
		set;
	}
}
```

## Namespace: MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSSet

Removed:

```
public class NSSet : NSObject {
```

Added:

```
public class NSSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<NSObject> {
 	public System.Collections.Generic.IEnumerator<NSObject> GetEnumerator ();
 	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
```

## Namespace: MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKOverlay

Added:

```
public MKOverlay ();
```

## Namespace: MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

Added:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
```

## Namespace: MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UINib

Removed:

```
public virtual MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
```

Added:

```
public virtual MonoTouch.Foundation.NSObject[] Instantiate (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
 	[Obsolete("Use Instantiate method")]
	public MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
```

   


 <hr>
