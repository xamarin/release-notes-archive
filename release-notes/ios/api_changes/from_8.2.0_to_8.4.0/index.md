---
id: F017E3DF-E3C5-487D-B0AD-ED269A331154
title: "From 8.2.0 to 8.4.0"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "8.2.0";
```

Added fields:

```
public static const string NetworkExtensionLibrary = "/System/Library/Frameworks/NetworkExtension.framework/NetworkExtension";
	public static const string Version = "8.4.0";
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Added properties:

```
public static MonoTouch.Foundation.NSString OrientationLeft { get; }
	public static MonoTouch.Foundation.NSString OrientationRight { get; }
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSCocoaError

Added values:

```
UserActivityConnectionUnavailableError = 4609,
	UserActivityErrorMaximum = 4863,
	UserActivityErrorMinimum = 4608,
	UserActivityHandoffFailedError = 4608,
	UserActivityHandoffUserInfoTooLargeError = 4611,
	UserActivityRemoteApplicationTimedOutError = 4610,
```

## Namespace MonoTouch.Photos

### Type Changed: MonoTouch.Photos.PHAssetCollectionSubtype

Added values:

```
AlbumMyPhotoStream = 100,
	SmartAlbumUserLibrary = 209,
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SslSessionOption

Added value:

```
Fallback = 6,
```

## New Namespace MonoTouch.NetworkExtension

### New Type MonoTouch.NetworkExtension.NEEvaluateConnectionRule

```
public class NEEvaluateConnectionRule : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEEvaluateConnectionRule ();
	public NEEvaluateConnectionRule (MonoTouch.Foundation.NSCoder coder);
	public NEEvaluateConnectionRule (MonoTouch.Foundation.NSObjectFlag t);
	public NEEvaluateConnectionRule (System.IntPtr handle);
	public NEEvaluateConnectionRule (string[] domains, NEEvaluateConnectionRuleAction action);
	// properties
	public virtual NEEvaluateConnectionRuleAction Action { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] MatchDomains { get; }
	public virtual MonoTouch.Foundation.NSUrl ProbeUrl { get; set; }
	public virtual string[] UseDnsServers { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEEvaluateConnectionRuleAction

```
[Serializable]
public enum NEEvaluateConnectionRuleAction {
	ConnectIfNeeded = 1,
	NeverConnect = 2,
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRule

```
public class NEOnDemandRule : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEOnDemandRule ();
	public NEOnDemandRule (MonoTouch.Foundation.NSCoder coder);
	public NEOnDemandRule (MonoTouch.Foundation.NSObjectFlag t);
	public NEOnDemandRule (System.IntPtr handle);
	// properties
	public virtual NEOnDemandRuleAction Action { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] DnsSearchDomainMatch { get; set; }
	public virtual string[] DnsServerAddressMatch { get; set; }
	public virtual NEOnDemandRuleInterfaceType InterfaceTypeMatch { get; set; }
	public virtual MonoTouch.Foundation.NSUrl ProbeUrl { get; set; }
	public virtual string[] SsidMatch { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleAction

```
[Serializable]
public enum NEOnDemandRuleAction {
	Connect = 1,
	Disconnect = 2,
	EvaluateConnection = 3,
	Ignore = 4,
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleConnect

```
public class NEOnDemandRuleConnect : MonoTouch.NetworkExtension.NEOnDemandRule, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEOnDemandRuleConnect ();
	public NEOnDemandRuleConnect (MonoTouch.Foundation.NSCoder coder);
	public NEOnDemandRuleConnect (MonoTouch.Foundation.NSObjectFlag t);
	public NEOnDemandRuleConnect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleDisconnect

```
public class NEOnDemandRuleDisconnect : MonoTouch.NetworkExtension.NEOnDemandRule, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEOnDemandRuleDisconnect ();
	public NEOnDemandRuleDisconnect (MonoTouch.Foundation.NSCoder coder);
	public NEOnDemandRuleDisconnect (MonoTouch.Foundation.NSObjectFlag t);
	public NEOnDemandRuleDisconnect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleEvaluateConnection

```
public class NEOnDemandRuleEvaluateConnection : MonoTouch.NetworkExtension.NEOnDemandRule, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEOnDemandRuleEvaluateConnection ();
	public NEOnDemandRuleEvaluateConnection (MonoTouch.Foundation.NSCoder coder);
	public NEOnDemandRuleEvaluateConnection (MonoTouch.Foundation.NSObjectFlag t);
	public NEOnDemandRuleEvaluateConnection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NEEvaluateConnectionRule[] ConnectionRules { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleIgnore

```
public class NEOnDemandRuleIgnore : MonoTouch.NetworkExtension.NEOnDemandRule, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEOnDemandRuleIgnore ();
	public NEOnDemandRuleIgnore (MonoTouch.Foundation.NSCoder coder);
	public NEOnDemandRuleIgnore (MonoTouch.Foundation.NSObjectFlag t);
	public NEOnDemandRuleIgnore (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.NetworkExtension.NEOnDemandRuleInterfaceType

```
[Serializable]
public enum NEOnDemandRuleInterfaceType {
	Cellular = 3,
	Ethernet = 1,
	WiFi = 2,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnConnection

```
public class NEVpnConnection : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnConnection ();
	public NEVpnConnection (MonoTouch.Foundation.NSCoder coder);
	public NEVpnConnection (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnConnection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NEVpnStatus Status { get; }
	public static MonoTouch.Foundation.NSString StatusDidChangeNotification { get; }
	// methods
	public virtual bool StartVpnTunnel (out MonoTouch.Foundation.NSError error);
	public virtual void StopVpnTunnel ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type MonoTouch.NetworkExtension.NEVpnError

```
[Serializable]
public enum NEVpnError {
	ConfigurationDisabled = 2,
	ConfigurationInvalid = 1,
	ConfigurationStale = 4,
	ConnectionFailed = 3,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2DeadPeerDetectionRate

```
[Serializable]
public enum NEVpnIke2DeadPeerDetectionRate {
	High = 3,
	Low = 1,
	Medium = 2,
	None = 0,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2DiffieHellman

```
[Serializable]
public enum NEVpnIke2DiffieHellman {
	Group0 = 0,
	Group1 = 1,
	Group14 = 14,
	Group15 = 15,
	Group16 = 16,
	Group17 = 17,
	Group18 = 18,
	Group2 = 2,
	Group5 = 5,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2EncryptionAlgorithm

```
[Serializable]
public enum NEVpnIke2EncryptionAlgorithm {
	AES128 = 3,
	AES256 = 4,
	DES = 1,
	TripleDES = 2,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2IntegrityAlgorithm

```
[Serializable]
public enum NEVpnIke2IntegrityAlgorithm {
	SHA160 = 2,
	SHA256 = 3,
	SHA384 = 4,
	SHA512 = 5,
	SHA96 = 1,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIke2SecurityAssociationParameters

```
public class NEVpnIke2SecurityAssociationParameters : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnIke2SecurityAssociationParameters ();
	public NEVpnIke2SecurityAssociationParameters (MonoTouch.Foundation.NSCoder coder);
	public NEVpnIke2SecurityAssociationParameters (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnIke2SecurityAssociationParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NEVpnIke2DiffieHellman DiffieHellmanGroup { get; set; }
	public virtual NEVpnIke2EncryptionAlgorithm EncryptionAlgorithm { get; set; }
	public virtual NEVpnIke2IntegrityAlgorithm IntegrityAlgorithm { get; set; }
	public virtual int LifetimeMinutes { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.NetworkExtension.NEVpnIkeAuthenticationMethod

```
[Serializable]
public enum NEVpnIkeAuthenticationMethod {
	Certificate = 1,
	None = 0,
	SharedSecret = 2,
}
```

### New Type MonoTouch.NetworkExtension.NEVpnManager

```
public class NEVpnManager : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnManager (MonoTouch.Foundation.NSCoder coder);
	public NEVpnManager (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnManager (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual NEVpnConnection Connection { get; }
	public virtual bool Enabled { get; set; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedDescription { get; set; }
	public virtual bool OnDemandEnabled { get; set; }
	public virtual NEOnDemandRule[] OnDemandRules { get; set; }
	public virtual NEVpnProtocol Protocol { get; set; }
	public static NEVpnManager SharedManager { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void LoadFromPreferences (System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveFromPreferences (System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void SaveToPreferences (System.Action<MonoTouch.Foundation.NSError> completionHandler);

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveConfigurationChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type MonoTouch.NetworkExtension.NEVpnProtocol

```
public class NEVpnProtocol : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnProtocol ();
	public NEVpnProtocol (MonoTouch.Foundation.NSCoder coder);
	public NEVpnProtocol (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnProtocol (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool DisconnectOnSleep { get; set; }
	public virtual MonoTouch.Foundation.NSData IdentityData { get; set; }
	public virtual string IdentityDataPassword { get; set; }
	public virtual MonoTouch.Foundation.NSData PasswordReference { get; set; }
	public virtual string ServerAddress { get; set; }
	public virtual string Username { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEVpnProtocolIke2

```
public class NEVpnProtocolIke2 : MonoTouch.NetworkExtension.NEVpnProtocolIpSec, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnProtocolIke2 ();
	public NEVpnProtocolIke2 (MonoTouch.Foundation.NSCoder coder);
	public NEVpnProtocolIke2 (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnProtocolIke2 (System.IntPtr handle);
	// properties
	public virtual NEVpnIke2SecurityAssociationParameters ChildSecurityAssociationParameters { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NEVpnIke2DeadPeerDetectionRate DeadPeerDetectionRate { get; set; }
	public virtual NEVpnIke2SecurityAssociationParameters IKESecurityAssociationParameters { get; }
	public virtual string ServerCertificateCommonName { get; set; }
	public virtual string ServerCertificateIssuerCommonName { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEVpnProtocolIpSec

```
public class NEVpnProtocolIpSec : MonoTouch.NetworkExtension.NEVpnProtocol, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NEVpnProtocolIpSec ();
	public NEVpnProtocolIpSec (MonoTouch.Foundation.NSCoder coder);
	public NEVpnProtocolIpSec (MonoTouch.Foundation.NSObjectFlag t);
	public NEVpnProtocolIpSec (System.IntPtr handle);
	// properties
	public virtual NEVpnIkeAuthenticationMethod AuthenticationMethod { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string LocalIdentifier { get; set; }
	public virtual string RemoteIdentifier { get; set; }
	public virtual MonoTouch.Foundation.NSData SharedSecretReference { get; set; }
	public virtual bool UseExtendedAuthentication { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.NetworkExtension.NEVpnStatus

```
[Serializable]
public enum NEVpnStatus {
	Connected = 3,
	Connecting = 2,
	Disconnected = 1,
	Disconnecting = 5,
	Invalid = 0,
	Reasserting = 4,
}
```

   


 <hr>
