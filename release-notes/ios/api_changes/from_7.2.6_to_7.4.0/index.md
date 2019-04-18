---
id: 49C576E3-AF6E-4E8E-920E-1612D3920464
title: "From 7.2.6 to 7.4.0"
---

# mscorlib.dll

## Namespace System

### Type Changed: System.Environment

Added method:

```
public static void SetEnvironmentVariable (string variable, string value);
```

## Namespace System.IO

### Type Changed: System.IO.FileInfo

Added property:

```
public bool IsReadOnly { get; set; }
```

Added methods:

```
public void Decrypt ();
	public void Encrypt ();
```

## Namespace System.Security.Claims

### Type Changed: System.Security.Claims.ClaimsIdentity

Added constructor:

```
public ClaimsIdentity (System.Collections.Generic.IEnumerable<Claim> claims);
```

### Type Changed: System.Security.Claims.ClaimTypes

Removed field:

```
public static const string Email = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress";
```

Added fields:

```
public static const string Actor = "http://schemas.xmlsoap.org/ws/2009/09/identity/claims/actor";
	public static const string AuthenticationInstant = "http://schemas.microsoft.com/ws/2008/06/identity/claims/authenticationinstant";
	public static const string AuthenticationMethod = "http://schemas.microsoft.com/ws/2008/06/identity/claims/authenticationmethod";
	public static const string ClaimsType2005Namespace = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims";
	public static const string ClaimsType2009Namespace = "http://schemas.xmlsoap.org/ws/2009/09/identity/claims";
	public static const string ClaimsTypeNamespace = "http://schemas.microsoft.com/ws/2008/06/identity/claims";
	public static const string CookiePath = "http://schemas.microsoft.com/ws/2008/06/identity/claims/cookiepath";
	public static const string DenyOnlyPrimaryGroup = "http://schemas.microsoft.com/ws/2008/06/identity/claims/denyonlyprimarygroup";
	public static const string DenyOnlyPrimarySid = "http://schemas.microsoft.com/ws/2008/06/identity/claims/denyonlyprimarysid";
	public static const string Dsa = "http://schemas.microsoft.com/ws/2008/06/identity/claims/dsa";
	public static const string Email = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/email";
	public static const string Expiration = "http://schemas.microsoft.com/ws/2008/06/identity/claims/expiration";
	public static const string Expired = "http://schemas.microsoft.com/ws/2008/06/identity/claims/expired";
	public static const string GroupSid = "http://schemas.microsoft.com/ws/2008/06/identity/claims/groupsid";
	public static const string IsPersistent = "http://schemas.microsoft.com/ws/2008/06/identity/claims/ispersistent";
	public static const string PrimaryGroupSid = "http://schemas.microsoft.com/ws/2008/06/identity/claims/primarygroupsid";
	public static const string PrimarySid = "http://schemas.microsoft.com/ws/2008/06/identity/claims/primarysid";
	public static const string Role = "http://schemas.microsoft.com/ws/2008/06/identity/claims/role";
	public static const string SerialNumber = "http://schemas.microsoft.com/ws/2008/06/identity/claims/serialnumber";
	public static const string UserData = "http://schemas.microsoft.com/ws/2008/06/identity/claims/userdata";
	public static const string Version = "http://schemas.microsoft.com/ws/2008/06/identity/claims/version";
	public static const string WindowsAccountName = "http://schemas.microsoft.com/ws/2008/06/identity/claims/windowsaccountname";
```

   


 <hr>

# System.dll

## Namespace System.Net.WebSockets

### Type Changed: System.Net.WebSockets.WebSocketMessageType

Removed values:

```
Binary = 2,
	Close = 8,
	Text = 1,
```

Added values:

```
Binary = 1,
	Close = 2,
	Text = 0,
```

   


 <hr>

# System.Core.dll

## Namespace System.IO.MemoryMappedFiles

### Type Changed: System.IO.MemoryMappedFiles.MemoryMappedFile

Removed methods:

```
public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, System.IO.HandleInheritability inheritability, bool leaveOpen);
	public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability handleInheritability);
	public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, System.IO.HandleInheritability inheritability);
```

Added methods:

```
public static MemoryMappedFile CreateFromFile (System.IO.FileStream fileStream, string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability, bool leaveOpen);
	public static MemoryMappedFile CreateNew (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability);
	public static MemoryMappedFile CreateOrOpen (string mapName, long capacity, MemoryMappedFileAccess access, MemoryMappedFileOptions options, MemoryMappedFileSecurity memoryMappedFileSecurity, System.IO.HandleInheritability inheritability);
	public MemoryMappedFileSecurity GetAccessControl ();
	public void SetAccessControl (MemoryMappedFileSecurity memoryMappedFileSecurity);
```

### New Type System.IO.MemoryMappedFiles.MemoryMappedFileSecurity

```
public class MemoryMappedFileSecurity : System.Security.AccessControl.ObjectSecurity`1[System.IO.MemoryMappedFiles.MemoryMappedFileRights] {
	// constructors
	public MemoryMappedFileSecurity ();
}
```

   


 <hr>

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "7.2.6";
```

Added field:

```
public static const string Version = "7.4.0";
```

### Type Changed: MonoTouch.MonoNativeFunctionWrapperAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.MonoPInvokeCallbackAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Removed Type MonoTouch.MonoTouchException ### New Type MonoTouch.RuntimeException

```
public class RuntimeException : System.Exception, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	public RuntimeException (string message, object[] args);
	public RuntimeException (int code, string message, object[] args);
	public RuntimeException (int code, bool error, string message, object[] args);
	public RuntimeException (int code, bool error, System.Exception innerException, string message, object[] args);
	// properties
	public int Code { get; }
	public bool Error { get; }
}
```



## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioQueueException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.AudioToolbox.AudioSessionException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioUnitException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingDataRequest

Added method:

```
public override string ToString ();
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCharacteristic

Removed property:

```
public virtual CBUUID UUID { get; }
```

Added property:

```
public virtual CBUUID UUID { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBMutableCharacteristic

Removed property:

```
public virtual CBUUID UUID { get; }
```

Added property:

```
public override CBUUID UUID { get; set; }
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.CoreFoundation.CFSocketException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

Added interface:

```
ICLLocationManagerDelegate
```

### New Type MonoTouch.CoreLocation.CLLocationManagerDelegate_Extensions

```
public static class CLLocationManagerDelegate_Extensions {
	// methods
	public static void AuthorizationChanged (ICLLocationManagerDelegate This, CLLocationManager manager, CLAuthorizationStatus status);
	public static void DeferredUpdatesFinished (ICLLocationManagerDelegate This, CLLocationManager manager, MonoTouch.Foundation.NSError error);
	public static void DidDetermineState (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegionState state, CLRegion region);
	public static void DidRangeBeacons (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeacon[] beacons, CLBeaconRegion region);
	public static void DidStartMonitoringForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static void Failed (ICLLocationManagerDelegate This, CLLocationManager manager, MonoTouch.Foundation.NSError error);
	public static void LocationsUpdated (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation[] locations);
	public static void LocationUpdatesPaused (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void LocationUpdatesResumed (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void MonitoringFailed (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region, MonoTouch.Foundation.NSError error);
	public static void RangingBeaconsDidFailForRegion (ICLLocationManagerDelegate This, CLLocationManager manager, CLBeaconRegion region, MonoTouch.Foundation.NSError error);
	public static void RegionEntered (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static void RegionLeft (ICLLocationManagerDelegate This, CLLocationManager manager, CLRegion region);
	public static bool ShouldDisplayHeadingCalibration (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void UpdatedHeading (ICLLocationManagerDelegate This, CLLocationManager manager, CLHeading newHeading);

	[Obsolete ("Deprecated in iOS 6.0")]
	public static void UpdatedLocation (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
}
```

### New Type MonoTouch.CoreLocation.ICLLocationManagerDelegate

```
public interface ICLLocationManagerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.ActionAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.AdviceAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ConnectAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ExportAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.FieldAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.LinkerSafeAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ModelAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ModelNotImplementedException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.MonoTouchException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.NSBundle

Added methods:

```
public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, string localizationName);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension);
	public static NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, NSUrl bundleURL);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, string localizationName);
	public static NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, NSUrl bundleURL);
```

### Type Changed: MonoTouch.Foundation.NSData

Added methods:

```
public virtual bool Save (string path, bool atomically);
	public virtual bool Save (NSUrl url, bool atomically);
```

### Type Changed: MonoTouch.Foundation.NSErrorException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.Foundation.NSInputStream

Added method:

```
public int Read (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoTouch.Foundation.NSMetadataQuery

Removed property:

```
public virtual NSMetadataQueryDelegate WeakDelegate { get; set; }
```

Added property:

```
public virtual NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSOutputStream

Removed method:

```
public static NSObject OutputStreamToMemory ();
```

Added methods:

```
public static NSOutputStream OutputStreamToMemory ();
	public int Write (byte[] buffer);
	public int Write (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoTouch.Foundation.NSPortMessage

Removed constructor:

```
public NSPortMessage (NSPort sendPort, NSPort recvPort, NSArray components);
```

Removed property:

```
public virtual NSArray Components { get; }
```

Removed method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.Foundation.NSUrlSession

Added methods:

```
public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlDownloadSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlDownloadSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlDownloadSessionResponse completionHandler);
```

Obsoleted methods:

```
[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTaskRequest

Removed constructor:

```
public NSUrlSessionDownloadTaskRequest (NSData data, NSUrlResponse response);
```

Added constructor:

```
public NSUrlSessionDownloadTaskRequest (NSUrl location, NSUrlResponse response);
```

Added property:

```
public NSUrl Location { get; set; }
```

Obsoleted property:

```
[Obsolete ("Use the Location property")]
	public NSData Data { get; set; }
```

### Type Changed: MonoTouch.Foundation.OutletAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.PreserveAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.ProtocolAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.RegisterAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.Foundation.You_Should_Not_Call_base_In_This_Method

Added interface:

```
System.Runtime.InteropServices._Exception
```

### New Type MonoTouch.Foundation.NSUrlDownloadSessionResponse

```
public sealed delegate NSUrlDownloadSessionResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlDownloadSessionResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrl location, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrl location, NSUrlResponse response, NSError error);
}
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Added interface:

```
MonoTouch.UIKit.IUIAccessibilityIdentification
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.AdoptsAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.AlphaAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.AvailabilityAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.BlockProxyAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.LinkWithAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.LionAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.MavericksAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
```

### Type Changed: MonoTouch.ObjCRuntime.MountainLionAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.NativeAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.Platform

Removed values:

```
iOS_Arch = 1095216660480,
	iOS_Arch32 = 4294967296,
	iOS_Arch64 = 8589934592,
```

Added values:

```
iOS_Arch = 4278190080,
	iOS_Arch32 = 16777216,
	iOS_Arch64 = 33554432,
```

### Type Changed: MonoTouch.ObjCRuntime.ReleaseAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.Selector

Added interface:

```
System.IEquatable<Selector>
```

Removed method:

```
public bool Equals (Selector right);
```

Added methods:

```
public virtual bool Equals (Selector right);
	public static Selector Register (System.IntPtr handle);
```

### Type Changed: MonoTouch.ObjCRuntime.SinceAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.ThreadSafeAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### Type Changed: MonoTouch.ObjCRuntime.TransientAttribute

Added interface:

```
System.Runtime.InteropServices._Attribute
```

### New Type MonoTouch.ObjCRuntime.iOSAttribute

```
public sealed class iOSAttribute : MonoTouch.ObjCRuntime.AvailabilityAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public iOSAttribute (byte major, byte minor);
}
```

### New Type MonoTouch.ObjCRuntime.MacAttribute

```
public sealed class MacAttribute : MonoTouch.ObjCRuntime.AvailabilityAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public MacAttribute (byte major, byte minor, bool onlyOn64);
}
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecurityException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.SystemConfiguration

### Type Changed: MonoTouch.SystemConfiguration.SystemConfigurationException

Added interface:

```
System.Runtime.InteropServices._Exception
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added interface:

```
IUIAccessibilityIdentification
```

### Type Changed: MonoTouch.UIKit.UIBarItem

Added interface:

```
IUIAccessibilityIdentification
```

Added properties:

```
public virtual System.Drawing.PointF AccessibilityActivationPoint { get; set; }
	public virtual bool AccessibilityElementsHidden { get; set; }
	public virtual System.Drawing.RectangleF AccessibilityFrame { get; set; }
	public virtual string AccessibilityHint { get; set; }
	public virtual string AccessibilityIdentifier { get; set; }
	public virtual string AccessibilityLabel { get; set; }
	public virtual string AccessibilityLanguage { get; set; }
	public virtual UIBezierPath AccessibilityPath { get; set; }
	public virtual UIAccessibilityTrait AccessibilityTraits { get; set; }
	public virtual string AccessibilityValue { get; set; }
	public virtual bool AccessibilityViewIsModal { get; set; }
	public static MonoTouch.Foundation.NSString AnnouncementDidFinishNotification { get; }
	public static int AnnouncementNotification { get; }
	public static MonoTouch.Foundation.NSString ClosedCaptioningStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString GuidedAccessStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString InvertColorsStatusDidChangeNotification { get; }
	public virtual bool IsAccessibilityElement { get; set; }
	public static int LayoutChangedNotification { get; }
	public static MonoTouch.Foundation.NSString MonoAudioStatusDidChangeNotification { get; }
	public static int PageScrolledNotification { get; }
	public static int ScreenChangedNotification { get; }
	public virtual bool ShouldGroupAccessibilityChildren { get; set; }
	public static MonoTouch.Foundation.NSString SpeechAttributeLanguage { get; }
	public static MonoTouch.Foundation.NSString SpeechAttributePitch { get; }
	public static MonoTouch.Foundation.NSString SpeechAttributePunctuation { get; }
	public static long TraitAdjustable { get; }
	public static long TraitAllowsDirectInteraction { get; }
	public static long TraitButton { get; }
	public static long TraitCausesPageTurn { get; }
	public static long TraitHeader { get; }
	public static long TraitImage { get; }
	public static long TraitKeyboardKey { get; }
	public static long TraitLink { get; }
	public static long TraitNone { get; }
	public static long TraitNotEnabled { get; }
	public static long TraitPlaysSound { get; }
	public static long TraitSearchField { get; }
	public static long TraitSelected { get; }
	public static long TraitStartsMediaSession { get; }
	public static long TraitStaticText { get; }
	public static long TraitSummaryElement { get; }
	public static long TraitUpdatesFrequently { get; }
	public static MonoTouch.Foundation.NSString VoiceOverStatusChanged { get; }
```

Added method:

```
public virtual bool AccessibilityActivate ();
```

### New Type MonoTouch.UIKit.Notifications

```
public static class Notifications {
	// methods
	public static MonoTouch.Foundation.NSObject ObserveAnnouncementDidFinish (System.EventHandler<UIAccessibilityAnnouncementFinishedEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveClosedCaptioningStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveGuidedAccessStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveInvertColorsStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveMonoAudioStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
}
```

### Type Changed: MonoTouch.UIKit.UIImage

Added interface:

```
IUIAccessibilityIdentification
```

Added property:

```
public virtual string AccessibilityIdentifier { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIKitThreadAccessException

Added interface:

```
System.Runtime.InteropServices._Exception
```

### Type Changed: MonoTouch.UIKit.UITabBarItem

Added interface:

```
IUIAccessibilityIdentification
```

## Namespace OpenTK

### New Type OpenTK.Matrix2

```
[Serializable]
public struct Matrix2, System.IEquatable<Matrix2> {
	// constructors
	public Matrix2 (ref Matrix2 matrix);
	public Matrix2 (float r0c0, float r0c1, float r1c0, float r1c1);
	public Matrix2 (float[] floatArray);
	// fields
	public static Matrix2 Identity;
	public float R0C0;
	public float R0C1;
	public float R1C0;
	public float R1C1;
	public static Matrix2 Zero;
	// properties
	public float Determinant { get; }
	public float Item { get; set; }
	public float Item { get; set; }
	// methods
	public static void Add (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public void Add (ref Matrix2 matrix, out Matrix2 result);
	public void Add (ref Matrix2 matrix);
	public static bool Equals (ref Matrix2 left, ref Matrix2 right);
	public virtual bool Equals (Matrix2 matrix);
	public bool Equals (ref Matrix2 matrix);
	public bool EqualsApprox (ref Matrix2 matrix, float tolerance);
	public static bool EqualsApprox (ref Matrix2 left, ref Matrix2 right, float tolerance);
	public override int GetHashCode ();
	public void Multiply (float scalar);
	public void Multiply (ref Matrix2 matrix);
	public void Multiply (float scalar, out Matrix2 result);
	public static void Multiply (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public static void Multiply (ref Matrix2 matrix, float scalar, out Matrix2 result);
	public void Multiply (ref Matrix2 matrix, out Matrix2 result);
	public static System.IntPtr op_Explicit (Matrix2 matrix);
	public static float* op_Explicit (Matrix2 matrix);
	public static float[] op_Explicit (Matrix2 matrix);
	public void Rotate (float angle);
	public void Rotate (float angle, out Matrix2 result);
	public static void Rotate (ref Matrix2 matrix, float angle, out Matrix2 result);
	public static void RotateMatrix (float angle, out Matrix2 result);
	public void Subtract (ref Matrix2 matrix);
	public static void Subtract (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public void Subtract (ref Matrix2 matrix, out Matrix2 result);
	public override string ToString ();
	public void Transform (ref Vector2 vector, out Vector2 result);
	public static void Transform (ref Matrix2 matrix, ref Vector2 vector);
	public static void Transform (ref Matrix2 matrix, ref Vector2 vector, out Vector2 result);
	public void Transform (ref Vector2 vector);
	public static void Transpose (ref Matrix2 matrix, out Matrix2 result);
	public void Transpose (out Matrix2 result);
	public void Transpose ();
}
```

   


 <hr>
