---
id: 79658C0F-3C6E-49DA-B2F8-8631E83E1071
title: "From 8.4.0 to 8.6.0"
---

# mscorlib.dll

## Namespace System

### Type Changed: System.AppDomain

Added event:

```
public event System.EventHandler<FirstChanceExceptionEventArgs> FirstChanceException;
```

   


 <hr>

# System.dll

## Namespace System.IO

### New Type System.IO.InternalBufferOverflowException

```
[Serializable]
public class InternalBufferOverflowException : System.SystemException, System.Runtime.Serialization.ISerializable {
	// constructors
	public InternalBufferOverflowException ();
	public InternalBufferOverflowException (string message);
	protected InternalBufferOverflowException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	public InternalBufferOverflowException (string message, System.Exception inner);
}
```

## Namespace System.Net.Sockets

### Type Changed: System.Net.Sockets.Socket

Added constructor:

```
public Socket (SocketType socketType, ProtocolType protocolType);
```

   


 <hr>

# System.Data.dll

## Namespace System.Data.SqlClient

### Type Changed: System.Data.SqlClient.SqlConnection

Added constructor:

```
public SqlConnection (string connectionString, SqlCredential cred);
```

Added property:

```
public SqlCredential Credentials { get; set; }
```

### New Type System.Data.SqlClient.SqlCredential

```
[Serializable]
public sealed class SqlCredential {
	// constructors
	public SqlCredential (string user, System.Security.SecureString password);
	// properties
	public System.Security.SecureString Password { get; }
	public string UserId { get; }
}
```

   


 <hr>

# System.Xml.dll

## Namespace System.Xml

### Type Changed: System.Xml.XmlTextReader

Added property:

```
public DtdProcessing DtdProcessing { get; set; }
```

   


 <hr>

# Mono.Data.Tds.dll

## Namespace Mono.Data.Tds.Protocol

### Type Changed: Mono.Data.Tds.Protocol.Tds

Added method:

```
public static string GetPlainPassword (System.Security.SecureString secPass);
```

### Type Changed: Mono.Data.Tds.Protocol.TdsConnectionParameters

Modified fields:

```
public string System.Security.SecureString Password;
```

Added field:

```
public bool PasswordSet;
```

   


 <hr>

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Modified fields:

```
public const string Version = "8.4.0" "8.6.0";
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Obsoleted events:

```
[Obsolete ("In addition to subscribing to this event, also subscribe to PerformAction2 to handle things in iOS 8 and above"]
	public event System.EventHandler<ABPeoplePickerPerformActionEventArgs> PerformAction;
	[Obsolete ("In addition to subscribing to this event, also subscribe to SelectPerson2 to handle things in iOS 8 and above"]
	public event System.EventHandler<ABPeoplePickerSelectPersonEventArgs> SelectPerson;
```

Added events:

```
public event System.EventHandler<ABPeoplePickerPerformAction2EventArgs> PerformAction2;
	public event System.EventHandler<ABPeoplePickerSelectPerson2EventArgs> SelectPerson2;
```

Added methods:

```
protected virtual void OnPerformAction2 (ABPeoplePickerPerformAction2EventArgs e);
	protected virtual void OnSelectPerson2 (ABPeoplePickerSelectPerson2EventArgs e);
```

### New Type MonoTouch.AddressBookUI.ABPeoplePickerPerformAction2EventArgs

```
public class ABPeoplePickerPerformAction2EventArgs : MonoTouch.AddressBookUI.ABPeoplePickerSelectPerson2EventArgs {
	// constructors
	public ABPeoplePickerPerformAction2EventArgs (MonoTouch.AddressBook.ABPerson person, MonoTouch.AddressBook.ABPersonProperty property, int? identifier);
	// properties
	public int? Identifier { get; }
	public MonoTouch.AddressBook.ABPersonProperty Property { get; }
}
```

### New Type MonoTouch.AddressBookUI.ABPeoplePickerSelectPerson2EventArgs

```
public class ABPeoplePickerSelectPerson2EventArgs : System.EventArgs {
	// constructors
	public ABPeoplePickerSelectPerson2EventArgs (MonoTouch.AddressBook.ABPerson person);
	// properties
	public MonoTouch.AddressBook.ABPerson Person { get; }
}
```

## Namespace MonoTouch.AssetsLibrary

### Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

### Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary.Notifications

Added method:

```
public static MonoTouch.Foundation.NSObject ObserveChanged (System.EventHandler<ALAssetLibraryChangedEventArgs> handler);
```

### New Type MonoTouch.AssetsLibrary.ALAssetLibraryChangedEventArgs

```
public class ALAssetLibraryChangedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	// constructors
	public ALAssetLibraryChangedEventArgs (MonoTouch.Foundation.NSNotification notification);
	// properties
	public MonoTouch.Foundation.NSSet DeletedAssetGroupsKey { get; }
	public MonoTouch.Foundation.NSSet InsertedAssetGroups { get; }
	public MonoTouch.Foundation.NSSet UpdatedAssetGroups { get; }
	public MonoTouch.Foundation.NSSet UpdatedAssets { get; }
}
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioFile

Added interface:

```
MonoTouch.ObjCRuntime.INativeObject
```

### Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added method:

```
protected override void ~AudioQueue ();
```

### Type Changed: MonoTouch.AudioToolbox.AudioSource

Added interface:

```
MonoTouch.ObjCRuntime.INativeObject
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioComponent

Obsoleted methods:

```
[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter"]
	public static AudioComponent FindComponent (AudioComponentDescription cd);
	[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter"]
	public static AudioComponent FindNextComponent (AudioComponent cmp, AudioComponentDescription cd);
```

Added methods:

```
public static AudioComponent FindComponent (ref AudioComponentDescription cd);
	public static AudioComponent FindNextComponent (AudioComponent cmp, ref AudioComponentDescription cd);
```

### Type Changed: MonoTouch.AudioUnit.AudioComponentDescriptionNative

Added method:

```
public void CopyTo (AudioComponentDescription cd);
```

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Added methods:

```
public uint GetCurrentDevice (AudioUnitScopeType scope, uint audioUnitElement);
	public static uint GetCurrentInputDevice ();
	public AudioUnitStatus SetCurrentDevice (uint inputDevice, AudioUnitScopeType scope, uint audioUnitElement);
```

### Type Changed: MonoTouch.AudioUnit.AUGraph

Obsoleted properties:

```
[Obsolete ("Use Handle property instead"]
	public IntPtr Handler { get; }
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction

Modified properties:

```
public virtual override MonoTouch.CoreGraphics.CGColor BackgroundColor { get; set; }
	public virtual override bool EnablePostProcessing { get; set; }
	public virtual override AVVideoCompositionLayerInstruction[] LayerInstructions { get; set; }
	public virtual override MonoTouch.CoreMedia.CMTimeRange TimeRange { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVVideoCompositionInstruction

Modified properties:

```
public virtual bool EnablePostProcessing { get; set; }
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions { get; set; }
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange { get; set; }
```

### New Type MonoTouch.AVFoundation.AVMetadataObjectType

```
[Serializable]
[Flags]
public enum AVMetadataObjectType {
	AztecCode = 2,
	Code128Code = 4,
	Code39Code = 8,
	Code39Mod43Code = 16,
	Code93Code = 32,
	DataMatrixCode = 8192,
	EAN13Code = 64,
	EAN8Code = 128,
	Face = 1,
	Interleaved2of5Code = 2048,
	ITF14Code = 4096,
	None = 0,
	PDF417Code = 256,
	QRCode = 512,
	UPCECode = 1024,
}
```

## Namespace MonoTouch.AVKit

### Type Changed: MonoTouch.AVKit.AVPlayerViewController

Added method:

```
public static void PrepareForPrerollAds ();
```

### New Type MonoTouch.AVKit.AVPlayerViewControlsStyle

```
[Serializable]
public enum AVPlayerViewControlsStyle {
	Default = 1,
	Floating = 2,
	Inline = 1,
	Minimal = 3,
	None = 0,
}
```

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKDiscoverUserInfosOperation

Modified properties:

```
public virtual CKDiscoverUserInfosCompletionHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKFetchNotificationChangesOperation

Modified properties:

```
public virtual System.Action<CKServerChangeToken,MonoTouch.Foundation.NSError> Completed { get; set; }
	public virtual System.Action<CKNotification> NotificationChanged { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKFetchRecordChangesOperation

Modified properties:

```
public virtual CKFetchRecordChangesHandler AllChangesReported { get; set; }
	public virtual System.Action<CKRecord> RecordChanged { get; set; }
	public virtual System.Action<CKRecordID> RecordDeleted { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKFetchRecordsOperation

Modified properties:

```
public virtual CKFetchRecordsCompletedHandler Completed { get; set; }
	public virtual System.Action<CKRecord,MonoTouch.CloudKit.CKRecordID,MonoTouch.Foundation.NSError> PerRecordCompletion { get; set; }
	public virtual System.Action<CKRecordID,System.Double> PerRecordProgress { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKFetchRecordZonesOperation

Modified properties:

```
public virtual CKRecordZoneCompleteHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKFetchSubscriptionsOperation

Modified properties:

```
public virtual CKFetchSubscriptionsCompleteHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKMarkNotificationsReadOperation

Modified properties:

```
public virtual CKMarkNotificationsReadHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKModifyBadgeOperation

Modified properties:

```
public virtual System.Action<MonoTouch.Foundation.NSError> Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKModifyRecordsOperation

Modified constructors:

```
public CKModifyRecordsOperation (CKRecord[] records recordsToSave, CKRecordID[] recordIds recordsToDelete)
```

Modified properties:

```
public virtual CKModifyRecordsOperationHandler Completed { get; set; }
	public virtual System.Action<CKRecord,MonoTouch.Foundation.NSError> PerRecordCompletion { get; set; }
	public virtual System.Action<CKRecord,System.Double> PerRecordProgress { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKModifyRecordZonesOperation

Modified properties:

```
public virtual CKModifyRecordZonesHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKModifySubscriptionsOperation

Modified properties:

```
public virtual CKModifySubscriptionsHandler Completed { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKQueryOperation

Modified properties:

```
public virtual System.Action<CKQueryCursor,MonoTouch.Foundation.NSError> Completed { get; set; }
	public virtual System.Action<CKRecord> RecordFetched { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKRecord

Obsoleted properties:

```
[Obsolete ("Use Id instead"]
	public virtual CKRecordID RecordId { get; }
```

Added property:

```
public CKRecordID Id { get; }
```

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CAAnimation

Added properties:

```
public virtual MonoTouch.SceneKit.SCNAnimationEvent[] AnimationEvents { get; set; }
	public virtual float FadeInDuration { get; set; }
	public virtual float FadeOutDuration { get; set; }
	public virtual bool UsesSceneTimeBase { get; set; }
```

### Type Changed: MonoTouch.CoreAnimation.CADisplayLink

Added method:

```
public void AddToRunLoop (MonoTouch.Foundation.NSRunLoop runloop, MonoTouch.Foundation.NSRunLoopMode mode);
```

### Type Changed: MonoTouch.CoreAnimation.CAEAGLLayer

Added interfaces:

```
MonoTouch.OpenGLES.IEAGLDrawable
```

### Type Changed: MonoTouch.CoreAnimation.CALayerDelegate

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.CoreAnimation.CAMediaTiming_Extensions

Added methods:

```
public static bool GetAutoReverses (ICAMediaTiming This);
	public static double GetBeginTime (ICAMediaTiming This);
	public static double GetDuration (ICAMediaTiming This);
	public static string GetFillMode (ICAMediaTiming This);
	public static float GetRepeatCount (ICAMediaTiming This);
	public static double GetRepeatDuration (ICAMediaTiming This);
	public static float GetSpeed (ICAMediaTiming This);
	public static double GetTimeOffset (ICAMediaTiming This);
	public static void SetAutoReverses (ICAMediaTiming This, bool value);
	public static void SetBeginTime (ICAMediaTiming This, double value);
	public static void SetDuration (ICAMediaTiming This, double value);
	public static void SetFillMode (ICAMediaTiming This, string value);
	public static void SetRepeatCount (ICAMediaTiming This, float value);
	public static void SetRepeatDuration (ICAMediaTiming This, double value);
	public static void SetSpeed (ICAMediaTiming This, float value);
	public static void SetTimeOffset (ICAMediaTiming This, double value);
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Added constructor:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue, CBCentralInitOptions options);
```

### Type Changed: MonoTouch.CoreBluetooth.CBCharacteristic

Modified properties:

```
public virtual CBDescriptor[] Descriptors { get; set; }
	public virtual CBCharacteristicProperties Properties { get; set; }
	public virtual MonoTouch.Foundation.NSData Value { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBMutableCharacteristic

Modified properties:

```
public virtual override CBDescriptor[] Descriptors { get; set; }
	public virtual override CBCharacteristicProperties Properties { get; set; }
	public virtual override MonoTouch.Foundation.NSData Value { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBMutableService

Modified properties:

```
public virtual override CBCharacteristic[] Characteristics { get; set; }
	public virtual override CBService[] IncludedServices { get; set; }
	public virtual override bool Primary { get; set; }
	public virtual override CBUUID UUID { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Added property:

```
public virtual IntPtr UUID { get; }
```

Added event:

```
public event System.EventHandler<CBRssiEventArgs> RssiRead;
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate

Added method:

```
public virtual void RssiRead (CBPeripheral peripheral, MonoTouch.Foundation.NSNumber rssi, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate_Extensions

Added method:

```
public static void RssiRead (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoTouch.Foundation.NSNumber rssi, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.CoreBluetooth.CBService

Modified properties:

```
public virtual CBCharacteristic[] Characteristics { get; set; }
	public virtual CBService[] IncludedServices { get; set; }
	public virtual bool Primary { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.PeripheralScanningOptions

Modified properties:

```
public bool AllowDuplicatesKey { get; set; }
```

### Type Changed: MonoTouch.CoreBluetooth.StartAdvertisingOptions

Modified properties:

```
public CBUUID[] ServicesUUID { get; set; }
```

### New Type MonoTouch.CoreBluetooth.CBCentralInitOptions

```
public class CBCentralInitOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public CBCentralInitOptions ();
	public CBCentralInitOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public string RestoreIdentifier { get; set; }
	public bool? ShowPowerAlert { get; set; }
}
```

### New Type MonoTouch.CoreBluetooth.CBRssiEventArgs

```
public class CBRssiEventArgs : System.EventArgs {
	// constructors
	public CBRssiEventArgs (MonoTouch.Foundation.NSNumber rssi, MonoTouch.Foundation.NSError error);
	// properties
	public MonoTouch.Foundation.NSError Error { get; set; }
	public MonoTouch.Foundation.NSNumber Rssi { get; set; }
}
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added interfaces:

```
MonoTouch.Foundation.INSLocking
```

### Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

Added interfaces:

```
MonoTouch.Foundation.INSLocking
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFSocket

Added events:

```
public event System.EventHandler<CFSocket.CFSocketDataEventArgs> DataEvent;
	public event System.EventHandler<CFSocket.CFSocketReadEventArgs> ReadEvent;
	public event System.EventHandler<CFSocket.CFSocketWriteEventArgs> WriteEvent;
```

### New Type MonoTouch.CoreFoundation.CFSocketDataEventArgs

```
public class CFSocketDataEventArgs : System.EventArgs {
	// constructors
	public CFSocket (System.Net.IPEndPoint remote, byte[] data);
	// properties
	public byte[] Data { get; }
	public System.Net.IPEndPoint RemoteEndPoint { get; }
}
```

### New Type MonoTouch.CoreFoundation.CFSocketReadEventArgs

```
public class CFSocketReadEventArgs : System.EventArgs {
	// constructors
	public CFSocket ();
}
```

### New Type MonoTouch.CoreFoundation.CFSocketWriteEventArgs

```
public class CFSocketWriteEventArgs : System.EventArgs {
	// constructors
	public CFSocket ();
}
```

### Type Changed: MonoTouch.CoreFoundation.DispatchTime

Added property:

```
public DispatchTime WallTime { get; }
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGAffineTransform

Added method:

```
public System.Drawing.SizeF TransformSize (System.Drawing.SizeF size);
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIImage

Obsoleted methods:

```
[Obsolete ("Use the overload acceping a CIFormat enum (instead of an int) for pixelFormat"]
	public static CIImage FromData (MonoTouch.Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, int pixelFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
```

Added method:

```
public static CIImage FromData (MonoTouch.Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, CIFormat pixelFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
```

### Type Changed: MonoTouch.CoreImage.CIImageInitializationOptions

Modified properties:

```
public MonoTouch.CoreGraphics.CGColorSpace ColorSpace { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIImageInitializationOptionsWithMetadata

Modified properties:

```
public MonoTouch.CoreGraphics.CGImageProperties Properties { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIKernel

Obsoleted methods:

```
[Obsolete ("Use FromProgramSingle"]
	public static CIKernel FromProgram (string coreImageShaderProgram);
	[Obsolete ("Use FromProgramMultiple"]
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
```

Added methods:

```
public static CIKernel[] FromProgramMultiple (string coreImageShaderProgram);
	public static CIKernel FromProgramSingle (string coreImageShaderProgram);
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMFormatDescription

Added method:

```
public static CMFormatDescription Create (IntPtr handle);
```

### Type Changed: MonoTouch.CoreMedia.CMTime

Obsoleted properties:

```
[Obsolete ("Use ToDictionary instead"]
	public IntPtr AsDictionary { get; }
```

Obsoleted methods:

```
[Obsolete ("Use FromDictionary (NSDictionary) instead"]
	public static CMTime FromDictionary (IntPtr dict);
```

Added methods:

```
public static CMTime FromDictionary (MonoTouch.Foundation.NSDictionary dict);
	public static bool op_GreaterThan (CMTime time1, CMTime time2);
	public static bool op_GreaterThanOrEqual (CMTime time1, CMTime time2);
	public static bool op_LessThan (CMTime time1, CMTime time2);
	public static bool op_LessThanOrEqual (CMTime time1, CMTime time2);
	public MonoTouch.Foundation.NSDictionary ToDictionary ();
```

## Namespace MonoTouch.CoreMidi

### Type Changed: MonoTouch.CoreMidi.MidiPacket

Added methods:

```
protected override void ~MidiPacket ();
	protected virtual void Dispose (bool disposing);
```

### Type Changed: MonoTouch.CoreMidi.MidiPacketsEventArgs

Added methods:

```
protected override void ~MidiPacketsEventArgs ();
	protected virtual void Dispose (bool disposing);
```

## Namespace MonoTouch.CoreText

### Type Changed: MonoTouch.CoreText.CTFontFeatureKey

Removed fields:

```
public static MonoTouch.Foundation.NSString Exclusive;
	public static MonoTouch.Foundation.NSString Identifier;
	public static MonoTouch.Foundation.NSString Name;
	public static MonoTouch.Foundation.NSString Selectors;
```

Added properties:

```
public static MonoTouch.Foundation.NSString Exclusive { get; }
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString Name { get; }
	public static MonoTouch.Foundation.NSString Selectors { get; }
```

### Type Changed: MonoTouch.CoreText.CTFontFeatureSelectorKey

Removed fields:

```
public static MonoTouch.Foundation.NSString Default;
	public static MonoTouch.Foundation.NSString Identifier;
	public static MonoTouch.Foundation.NSString Name;
	public static MonoTouch.Foundation.NSString Setting;
```

Added properties:

```
public static MonoTouch.Foundation.NSString Default { get; }
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString Name { get; }
	public static MonoTouch.Foundation.NSString Setting { get; }
```

### Type Changed: MonoTouch.CoreText.CTFontVariationAxisKey

Removed fields:

```
public static MonoTouch.Foundation.NSString DefaultValue;
	public static MonoTouch.Foundation.NSString Identifier;
	public static MonoTouch.Foundation.NSString MaximumValue;
	public static MonoTouch.Foundation.NSString MinimumValue;
	public static MonoTouch.Foundation.NSString Name;
```

Added properties:

```
public static MonoTouch.Foundation.NSString DefaultValue { get; }
	public static MonoTouch.Foundation.NSString Identifier { get; }
	public static MonoTouch.Foundation.NSString MaximumValue { get; }
	public static MonoTouch.Foundation.NSString MinimumValue { get; }
	public static MonoTouch.Foundation.NSString Name { get; }
```

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVPixelBufferAttributes

Modified properties:

```
public MonoTouch.CoreFoundation.CFAllocator MemoryAllocator { get; set; }
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added methods:

```
protected T GetNativeValue<T> (NSString key);
	protected T GetStrongDictionary<T> (NSString key);
```

### Type Changed: MonoTouch.Foundation.NSDecimalNumber

Modified properties:

```
public virtual override double DoubleValue { get; }
```

Modified methods:

```
public virtual override int Compare (NSNumber other)
	public virtual override string DescriptionWithLocale (NSLocale locale)
```

### Type Changed: MonoTouch.Foundation.NSDictionary

Added method:

```
public NSFileAttributes ToFileAttributes ();
```

### Type Changed: MonoTouch.Foundation.NSDirectoryEnumerator

Added property:

```
public virtual int Level { get; }
```

### Type Changed: MonoTouch.Foundation.NSFileAttributes

Obsoleted properties:

```
[Obsolete ("Use ExtensionHidden instead"]
	public bool? FileExtensionHidden { get; set; }
	[Obsolete ("Use GroupOwnerAccountID instead"]
	public uint? FileGroupOwnerAccountID { get; set; }
	[Obsolete ("Use GroupOwnerAccountID instead"]
	public uint? FileOwnerAccountID { get; set; }
	[Obsolete ("Use ReferenceCount instead"]
	public uint? FileReferenceCount { get; set; }
	[Obsolete ("Use Size instead"]
	public ulong? FileSize { get; set; }
	[Obsolete ("Use SystemFileNumber instead"]
	public uint? FileSystemFileNumber { get; set; }
	[Obsolete ("Use Type instead"]
	public NSFileType? FileType { get; set; }
```

Added properties:

```
public bool? ExtensionHidden { get; set; }
	public uint? GroupOwnerAccountID { get; set; }
	public string GroupOwnerAccountName { get; set; }
	public uint? HfsCreatorCode { get; set; }
	public uint? OwnerAccountID { get; set; }
	public NSFileProtection? ProtectionKey { get; set; }
	public uint? ReferenceCount { get; set; }
	public ulong? Size { get; set; }
	public uint? SystemFileNumber { get; set; }
	public int? SystemNumber { get; set; }
	public NSFileType? Type { get; set; }
```

Obsoleted methods:

```
[Obsolete ("Use FromDictionary instead"]
	public static NSFileAttributes FromDict (NSDictionary dict);
```

Added method:

```
public static NSFileAttributes FromDictionary (NSDictionary dict);
```

### Type Changed: MonoTouch.Foundation.NSFileManagerDelegate

Added methods:

```
public virtual bool ShouldCopyItemAtUrl (NSFileManager fm, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldLinkItemAtUrl (NSFileManager fileManager, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldMoveItemAtUrl (NSFileManager fileManager, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldProceedAfterErrorCopyingItem (NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldProceedAfterErrorLinkingItem (NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldProceedAfterErrorMovingItem (NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public virtual bool ShouldProceedAfterErrorRemovingItem (NSFileManager fileManager, NSError error, NSUrl url);
	public virtual bool ShouldRemoveItemAtUrl (NSFileManager fileManager, NSUrl url);
```

### Type Changed: MonoTouch.Foundation.NSFileManagerDelegate_Extensions

Added methods:

```
public static bool ShouldCopyItemAtUrl (INSFileManagerDelegate This, NSFileManager fm, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldLinkItemAtUrl (INSFileManagerDelegate This, NSFileManager fileManager, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldMoveItemAtUrl (INSFileManagerDelegate This, NSFileManager fileManager, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldProceedAfterErrorCopyingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldProceedAfterErrorLinkingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldProceedAfterErrorMovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, NSUrl srcUrl, NSUrl dstUrl);
	public static bool ShouldProceedAfterErrorRemovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, NSUrl url);
	public static bool ShouldRemoveItemAtUrl (INSFileManagerDelegate This, NSFileManager fileManager, NSUrl url);
```

### Type Changed: MonoTouch.Foundation.NSFilePresenter_Extensions

Added method:

```
public static NSOperationQueue GetPesentedItemOperationQueue (INSFilePresenter This);
```

### Type Changed: MonoTouch.Foundation.NSJsonSerialization

Obsoleted methods:

```
[Obsolete ("Use the Deserialize(NSData,NSJsonReadingOptions,out NSError) overload instead"]
	public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, NSError error);
```

Added method:

```
public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, out NSError error);
```

### Type Changed: MonoTouch.Foundation.NSMachPort

Modified properties:

```
public virtual override NSObject WeakDelegate { get; set; }
```

Modified methods:

```
public virtual override void RemoveFromRunLoop (NSRunLoop runLoop, NSString mode)
	public virtual override void ScheduleInRunLoop (NSRunLoop runLoop, NSString mode)
```

### Type Changed: MonoTouch.Foundation.NSMetadataItem

Added properties:

```
public NSString DisplayName { get; }
	public NSItemDownloadingStatus DownloadingStatus { get; }
	public NSDate FileSystemContentChangeDate { get; }
	public NSDate FileSystemCreationDate { get; }
	public NSString FileSystemName { get; }
	public NSNumber FileSystemSize { get; }
	public bool IsUbiquitous { get; }
	public NSString Path { get; }
	public NSError UbiquitousItemDownloadingError { get; }
	public bool UbiquitousItemHasUnresolvedConflicts { get; }
	public bool UbiquitousItemIsDownloading { get; }
	public bool UbiquitousItemIsUploaded { get; }
	public bool UbiquitousItemIsUploading { get; }
	public double UbiquitousItemPercentDownloaded { get; }
	public double UbiquitousItemPercentUploaded { get; }
	public NSError UbiquitousItemUploadingError { get; }
	public NSUrl Url { get; }
```

### Type Changed: MonoTouch.Foundation.NSMetadataQuery

Added properties:

```
public static NSString UbiquitousItemDownloadingErrorKey { get; }
	public static NSString UbiquitousItemDownloadingStatusKey { get; }
	public static NSString UbiquitousItemUploadingErrorKey { get; }
```

### Type Changed: MonoTouch.Foundation.NSMutableData

Obsoleted methods:

```
[Obsolete ("Use the Length property setter"]
	public virtual void SetLength (uint len);
```

### Type Changed: MonoTouch.Foundation.NSObject

Added properties:

```
public virtual MonoTouch.ObjCRuntime.Class Class { get; }
	public virtual bool IsProxy { get; }
	public virtual NSObject Self { get; }
	public virtual MonoTouch.ObjCRuntime.Class Superclass { get; }
	public virtual NSZone Zone { get; }
```

Added methods:

```
public virtual uint GetNativeHash ();
	public virtual bool IsEqual (NSObject anObject);
	public virtual bool IsKindOfClass (MonoTouch.ObjCRuntime.Class aClass);
	public virtual bool IsMemberOfClass (MonoTouch.ObjCRuntime.Class aClass);
	public virtual NSObject PerformSelector (MonoTouch.ObjCRuntime.Selector aSelector);
	public virtual NSObject PerformSelector (MonoTouch.ObjCRuntime.Selector aSelector, NSObject anObject);
	public virtual NSObject PerformSelector (MonoTouch.ObjCRuntime.Selector aSelector, NSObject object1, NSObject object2);
```

### Type Changed: MonoTouch.Foundation.NSObservedChange

Added constructor:

```
public NSObservedChange (NSDictionary source);
```

### Type Changed: MonoTouch.Foundation.NSString

Added field:

```
public static NSString Empty;
```

### Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStore

Obsoleted methods:

```
[Obsolete ("Use ToDictionary instead"]
	public virtual NSDictionary DictionaryRepresentation ();
```

Added method:

```
public NSDictionary ToDictionary ();
```

### Type Changed: MonoTouch.Foundation.NSUrl

Modified constructors:

```
public NSUrl (string path urlString, NSUrl relativeToUrl)
	public NSUrl (string path urlString)
```

Added interfaces:

```
System.IEquatable<NSUrl>
```

Obsoleted methods:

```
[Obsolete ("Use the overload with a NSString constant"]
	public bool SetResource (string key, NSObject value);
	[Obsolete ("Use the overload with a NSString constant"]
	public bool SetResource (string key, NSObject value, out NSError error);
	[Obsolete ("Use the overload with a NSString constant"]
	public bool TryGetResource (string key, out NSObject value);
	[Obsolete ("Use the overload with a NSString constant"]
	public bool TryGetResource (string key, out NSObject value, out NSError error);
```

Added method:

```
public virtual bool Equals (NSUrl url);
```

### Type Changed: MonoTouch.Foundation.NSUrlConnection

Added interfaces:

```
INSURLAuthenticationChallengeSender
```

### Type Changed: MonoTouch.Foundation.NSUserDefaults

Obsoleted methods:

```
[Obsolete ("Use ToDictionary instead"]
	public virtual NSDictionary AsDictionary ();
```

Added method:

```
public NSDictionary ToDictionary ();
```

### Type Changed: MonoTouch.Foundation.NSZone

Added constructor:

```
public NSZone (IntPtr handle, bool owns);
```

### New Type MonoTouch.Foundation.INSLocking

```
public interface INSLocking : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Lock ();
	public virtual void Unlock ();
}
```

### New Type MonoTouch.Foundation.INSURLAuthenticationChallengeSender

```
public interface INSURLAuthenticationChallengeSender : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void CancelAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
}
```

### New Type MonoTouch.Foundation.NSFileProtection

```
[Serializable]
public enum NSFileProtection {
	Complete = 1,
	CompleteUnlessOpen = 2,
	CompleteUntilFirstUserAuthentication = 3,
	None = 0,
}
```

### New Type MonoTouch.Foundation.NSItemDownloadingStatus

```
[Serializable]
public enum NSItemDownloadingStatus {
	Current = 0,
	Downloaded = 1,
	NotDownloaded = 2,
	Unknown = -1,
}
```

### New Type MonoTouch.Foundation.NSLocking_Extensions

```
public static class NSLocking_Extensions {
}
```

### New Type MonoTouch.Foundation.NSObjectProtocol_Extensions

```
public static class NSObjectProtocol_Extensions {
	// methods
	public static string GetDebugDescription (INSObjectProtocol This);
}
```

### New Type MonoTouch.Foundation.NSURLAuthenticationChallengeSender

```
public abstract class NSURLAuthenticationChallengeSender : MonoTouch.Foundation.NSObject, INSURLAuthenticationChallengeSender, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSURLAuthenticationChallengeSender ();
	public NSURLAuthenticationChallengeSender (NSCoder coder);
	public NSURLAuthenticationChallengeSender (NSObjectFlag t);
	public NSURLAuthenticationChallengeSender (IntPtr handle);
	// methods
	public virtual void CancelAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
}
```

### New Type MonoTouch.Foundation.NSURLAuthenticationChallengeSender_Extensions

```
public static class NSURLAuthenticationChallengeSender_Extensions {
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Modified properties:

```
public virtual override MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoTouch.GameKit.GKMatch

Obsoleted methods:

```
[Obsolete ("Use SendDataToAllPlayers"]
	public virtual bool SendDataToAllPlayer (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
```

Added method:

```
public virtual bool SendDataToAllPlayers (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.GameKit.GKScore

Added property:

```
public string Category { get; set; }
```

## Namespace MonoTouch.ImageIO

### Type Changed: MonoTouch.ImageIO.CGImageDestination

Added methods:

```
public void AddImage (MonoTouch.CoreGraphics.CGImage image, CGImageDestinationOptions options);
	public void AddImage (CGImageSource source, int index, CGImageDestinationOptions options);
```

## Namespace MonoTouch.JavaScriptCore

### Type Changed: MonoTouch.JavaScriptCore.JSValue

Modified methods:

```
public JSValue From (int value ivalue, JSContext context)
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotation_Extensions

Added methods:

```
public static string GetSubtitle (IMKAnnotation This);
	public static string GetTitle (IMKAnnotation This);
```

### Type Changed: MonoTouch.MapKit.MKLocalSearch_Extensions

Added method:

```
public static bool GetIsSearching (IMKLocalSearch This);
```

### Type Changed: MonoTouch.MapKit.MKLocalSearchRequest_Extensions

Added methods:

```
public static string GetNaturalLanguageQuery (IMKLocalSearchRequest This);
	public static MKCoordinateRegion GetRegion (IMKLocalSearchRequest This);
	public static void SetNaturalLanguageQuery (IMKLocalSearchRequest This, string value);
	public static void SetRegion (IMKLocalSearchRequest This, MKCoordinateRegion value);
```

### Type Changed: MonoTouch.MapKit.MKLocalSearchResponse_Extensions

Added methods:

```
public static MKMapItem[] GetMapItems (IMKLocalSearchResponse This);
	public static MKCoordinateRegion GetRegion (IMKLocalSearchResponse This);
```

### Type Changed: MonoTouch.MapKit.MKOverlay_Extensions

Added method:

```
public static MKMapRect GetBoundingMapRect (IMKOverlay This);
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Added interfaces:

```
IMPMediaPlayback
```

Added method:

```
public static void PrepareForPrerollAds ();
```

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController.Notifications

Added method:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
```

### Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added interfaces:

```
IMPMediaPlayback
```

### New Type MonoTouch.MediaPlayer.IMPMediaPlayback

```
public interface IMPMediaPlayback : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float CurrentPlaybackRate { get; set; }
	public virtual double CurrentPlaybackTime { get; set; }
	public virtual bool IsPreparedToPlay { get; }
	// methods
	public virtual void BeginSeekingBackward ();
	public virtual void BeginSeekingForward ();
	public virtual void EndSeeking ();
	public virtual void Pause ();
	public virtual void Play ();
	public virtual void PrepareToPlay ();
	public virtual void Stop ();
}
```

### New Type MonoTouch.MediaPlayer.MPMediaPlayback_Extensions

```
public static class MPMediaPlayback_Extensions {
}
```

## Namespace MonoTouch.MediaToolbox

### Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTap

Obsoleted methods:

```
[Obsolete ("Use GetSourceAudio(int,AudioBuffers,out MTAudioProcessingTapFlags, out CMTimeRange, out int) instead"]
	public MTAudioProcessingTapError GetSourceAudio (long frames, MonoTouch.AudioToolbox.AudioBuffers bufferList, out MTAudioProcessingTapFlags flags, out MonoTouch.CoreMedia.CMTimeRange timeRange, long framesProvided);
```

Added method:

```
public MTAudioProcessingTapError GetSourceAudio (int frames, MonoTouch.AudioToolbox.AudioBuffers bufferList, out MTAudioProcessingTapFlags flags, out MonoTouch.CoreMedia.CMTimeRange timeRange, out int framesProvided);
```

## Namespace MonoTouch.Metal

### Type Changed: MonoTouch.Metal.MTLDeallocator

Modified methods:

```
public virtual System.IAsyncResult BeginInvoke (IntPtr pointer, uint lenght length, System.AsyncCallback callback, object object)
	public virtual void Invoke (IntPtr pointer, uint lenght length)
```

### Type Changed: MonoTouch.Metal.MTLDepthStencilState_Extensions

Added methods:

```
public static IMTLDevice GetDevice (IMTLDepthStencilState This);
	public static string GetLabel (IMTLDepthStencilState This);
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static int int_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static int int_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static void void_objc_msgSend_ref_SCNVector3_ref_SCNVector3 (IntPtr receiver, IntPtr selector, ref MonoTouch.SceneKit.SCNVector3 arg1, ref MonoTouch.SceneKit.SCNVector3 arg2);
	public static void void_objc_msgSendSuper_ref_SCNVector3_ref_SCNVector3 (IntPtr receiver, IntPtr selector, ref MonoTouch.SceneKit.SCNVector3 arg1, ref MonoTouch.SceneKit.SCNVector3 arg2);
```

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added values:

```
iOS_2_2 = 131584,
	iOS_3_1 = 196864,
	iOS_8_1 = 524544,
	iOS_8_2 = 524800,
```

### Type Changed: MonoTouch.ObjCRuntime.Selector

Obsoleted constructors:

```
[Obsolete ("Use the (string) constructor."]
	public Selector (string name, bool alloc);
```

Added interface:

```
INativeObject
```

## Namespace MonoTouch.OpenGLES

### New Type MonoTouch.OpenGLES.EAGLDrawable_Extensions

```
public static class EAGLDrawable_Extensions {
}
```

### New Type MonoTouch.OpenGLES.IEAGLDrawable

```
public interface IEAGLDrawable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MonoTouch.Foundation.NSDictionary DrawableProperties { get; set; }
}
```

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.ISCNBoundingVolume

Added method:

```
public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoTouch.SceneKit.SCNAnimatable

Added method:

```
public void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, string key);
```

### Type Changed: MonoTouch.SceneKit.SCNBoundingVolume

Added method:

```
public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoTouch.SceneKit.SCNGeometry

Added method:

```
public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoTouch.SceneKit.SCNGeometrySource

Added method:

```
public static SCNGeometrySource FromData (MonoTouch.Foundation.NSData data, SCNGeometrySourceSemantics geometrySourceSemantic, int vectorCount, bool floatComponents, int componentsPerVector, int bytesPerComponent, int offset, int stride);
```

### Type Changed: MonoTouch.SceneKit.SCNHitTest

Added property:

```
public static MonoTouch.Foundation.NSString IgnoreHiddenNodes { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNNode

Added methods:

```
public void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, string key);
	public virtual void SetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsSearchMode

Added value:

```
Unknown = -1,
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsTest

Added property:

```
public SCNPhysicsSearchMode SearchMode { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNProgramDelegate

Obsoleted methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public virtual bool BindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public virtual bool IsProgramOpaque (SCNProgram program);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public virtual void UnbindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
```

### Type Changed: MonoTouch.SceneKit.SCNProgramDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	[Obsolete ("Do not use; this method only exist in OSX, not in iOS"]
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
```

### Type Changed: MonoTouch.SceneKit.SCNSceneLoadingOptions

Added property:

```
public SCNAnimationImportPolicy AnimationImportPolicy { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNSceneRenderer

Added property:

```
public virtual SCNScene Scene { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNSceneRenderer_Extensions

Added methods:

```
public static bool GetAutoenablesDefaultLighting (ISCNSceneRenderer This);
	public static IntPtr GetContext (ISCNSceneRenderer This);
	public static bool GetJitteringEnabled (ISCNSceneRenderer This);
	public static bool GetLoops (ISCNSceneRenderer This);
	public static MonoTouch.SpriteKit.SKScene GetOverlayScene (ISCNSceneRenderer This);
	public static bool GetPlaying (ISCNSceneRenderer This);
	public static SCNNode GetPointOfView (ISCNSceneRenderer This);
	public static SCNScene GetScene (ISCNSceneRenderer This);
	public static double GetSceneTimeInSeconds (ISCNSceneRenderer This);
	public static bool GetShowsStatistics (ISCNSceneRenderer This);
	public static MonoTouch.Foundation.NSObject GetWeakSceneRendererDelegate (ISCNSceneRenderer This);
	public static void SetAutoenablesDefaultLighting (ISCNSceneRenderer This, bool value);
	public static void SetJitteringEnabled (ISCNSceneRenderer This, bool value);
	public static void SetLoops (ISCNSceneRenderer This, bool value);
	public static void SetOverlayScene (ISCNSceneRenderer This, MonoTouch.SpriteKit.SKScene value);
	public static void SetPlaying (ISCNSceneRenderer This, bool value);
	public static void SetPointOfView (ISCNSceneRenderer This, SCNNode value);
	public static void SetScene (ISCNSceneRenderer This, SCNScene value);
	public static void SetSceneTimeInSeconds (ISCNSceneRenderer This, double value);
	public static void SetShowsStatistics (ISCNSceneRenderer This, bool value);
	public static void SetWeakSceneRendererDelegate (ISCNSceneRenderer This, MonoTouch.Foundation.NSObject value);
```

### Type Changed: MonoTouch.SceneKit.SCNSceneSource

Added methods:

```
public MonoTouch.Foundation.NSObject GetEntryWithIdentifier<T> (string uid);
	public string[] GetIdentifiersOfEntries<T> ();
```

### Type Changed: MonoTouch.SceneKit.SCNShadable_Extensions

Added methods:

```
public static SCNProgram GetProgram (ISCNShadable This);
	public static MonoTouch.Foundation.NSDictionary GetWeakShaderModifiers (ISCNShadable This);
	public static void SetProgram (ISCNShadable This, SCNProgram value);
	public static void SetWeakShaderModifiers (ISCNShadable This, MonoTouch.Foundation.NSDictionary value);
```

### Type Changed: MonoTouch.SceneKit.SCNTechnique

Obsoleted properties:

```
[Obsolete ("Use ToDictionary () instead"]
	public virtual MonoTouch.Foundation.NSDictionary DictionaryRepresentation { get; }
```

Added method:

```
public MonoTouch.Foundation.NSDictionary ToDictionary ();
```

### Type Changed: MonoTouch.SceneKit.SCNView

Added interfaces:

```
ISCNTechniqueSupport
```

Added property:

```
public virtual SCNTechnique Technique { get; set; }
```

### New Type MonoTouch.SceneKit.ISCNSceneExportDelegate

```
public interface ISCNSceneExportDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.SCNAnimationImportPolicy

```
[Serializable]
public enum SCNAnimationImportPolicy {
	DoNotPlay = 3,
	Play = 1,
	PlayRepeatedly = 2,
	PlayUsingSceneTimeBase = 4,
	Unknown = 0,
}
```

### New Type MonoTouch.SceneKit.SCNGeometrySourceSemantics

```
[Serializable]
public enum SCNGeometrySourceSemantics {
	BoneIndices = 7,
	BoneWeights = 6,
	Color = 2,
	EdgeCrease = 5,
	Normal = 1,
	Texcoord = 3,
	Vertex = 0,
	VertexCrease = 4,
}
```

### New Type MonoTouch.SceneKit.SCNSceneExportDelegate

```
public class SCNSceneExportDelegate : MonoTouch.Foundation.NSObject, ISCNSceneExportDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public SCNSceneExportDelegate ();
	public SCNSceneExportDelegate (MonoTouch.Foundation.NSCoder coder);
	public SCNSceneExportDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSceneExportDelegate (IntPtr handle);
	// methods
	public virtual MonoTouch.Foundation.NSUrl WriteImage (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSUrl documentURL, MonoTouch.Foundation.NSUrl originalImageURL);
}
```

### New Type MonoTouch.SceneKit.SCNSceneExportDelegate_Extensions

```
public static class SCNSceneExportDelegate_Extensions {
	// methods
	public static MonoTouch.Foundation.NSUrl WriteImage (ISCNSceneExportDelegate This, MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSUrl documentURL, MonoTouch.Foundation.NSUrl originalImageURL);
}
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecRecord

Modified properties:

```
public MonoTouch.Foundation.NSData[] MatchIssuers { get; set; }
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKMutablePayment

Modified properties:

```
public virtual override MonoTouch.Foundation.NSData RequestData { get; set; }
```

### Type Changed: MonoTouch.StoreKit.SKPayment

Modified properties:

```
public virtual MonoTouch.Foundation.NSData RequestData { get; set; }
```

## Namespace MonoTouch.SystemConfiguration

### Type Changed: MonoTouch.SystemConfiguration.CaptiveNetwork

Obsoleted methods:

```
[Obsolete ("Replaced by TryCopyCurrentNetworkInfo"]
	public static MonoTouch.Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);
	[Obsolete ("Replaced by TryGetSupportedInterfaces"]
	public static string[] GetSupportedInterfaces ();
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.NSLayoutManager

Added method:

```
public uint GetLineFragmentInsertionPoints (uint charIndex, bool alternatePosition, bool inDisplayOrder, float[] positions, int[] charIndexes);
```

### Type Changed: MonoTouch.UIKit.NSTextContainer

Added interfaces:

```
INSTextLayoutOrientationProvider
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Obsoleted methods:

```
[Obsolete ("Override the overload accepting an UIApplication argument"]
	public virtual void UserActivityUpdated (MonoTouch.Foundation.NSUserActivity userActivity);
```

Added method:

```
public virtual void UserActivityUpdated (UIApplication application, MonoTouch.Foundation.NSUserActivity userActivity);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Override the overload accepting an UIApplication argument"]
	public static void UserActivityUpdated (IUIApplicationDelegate This, MonoTouch.Foundation.NSUserActivity userActivity);
```

Added methods:

```
public static UIWindow GetWindow (IUIApplicationDelegate This);
	public static void SetWindow (IUIApplicationDelegate This, UIWindow value);
	public static void UserActivityUpdated (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUserActivity userActivity);
```

### Type Changed: MonoTouch.UIKit.UIBarPositioning_Extensions

Added method:

```
public static UIBarPosition GetBarPosition (IUIBarPositioning This);
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Modified methods:

```
public MonoTouch.Foundation.NSObject DequeueReusableSupplementaryView (UICollectionElementKindSection section, MonoTouch.Foundation.NSString identifier reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath)
```

Added methods:

```
public UICollectionReusableView DequeueReusableCell (string reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
	public UICollectionReusableView DequeueReusableSupplementaryView (MonoTouch.Foundation.NSString kind, string reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
	public UICollectionReusableView DequeueReusableSupplementaryView (UICollectionElementKindSection kind, string reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
	public void RegisterClassForCell (System.Type cellType, string reuseIdentifier);
	public void RegisterClassForSupplementaryView (System.Type cellType, MonoTouch.Foundation.NSString kind, string reuseIdentifier);
	public void RegisterClassForSupplementaryView (System.Type cellType, UICollectionElementKindSection section, string reuseIdentifier);
	public void RegisterNibForCell (UINib nib, string reuseIdentifier);
	public void RegisterNibForSupplementaryView (UINib nib, UICollectionElementKindSection section, string reuseIdentifier);
```

### Type Changed: MonoTouch.UIKit.UIDynamicAnimator

Added interfaces:

```
System.Collections.Generic.IEnumerable<UIDynamicBehavior>
```

### Type Changed: MonoTouch.UIKit.UIGestureRecognizer

Obsoleted fields:

```
[Obsolete ("Don't use, this field has been removed the Unified API. Use 'Selector.GetHandle ()' instead."]
	public static MonoTouch.ObjCRuntime.Selector ParametrizedSelector;
```

### Type Changed: MonoTouch.UIKit.UIImage

Obsoleted methods:

```
[Obsolete ("This always returns null. Use the overload that accept a System.String 'name' instead."]
	public static UIImage CreateAnimatedImage (UIImage[] images, UIEdgeInsets capInsets, double duration);
```

Added method:

```
public static UIImage CreateAnimatedImage (string name, UIEdgeInsets capInsets, double duration);
```

### Type Changed: MonoTouch.UIKit.UIPasteboard

Modified methods:

```
public virtual bool Contains (string[] pasteboadTypes pasteboardTypes, MonoTouch.Foundation.NSIndexSet itemSet)
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Obsoleted properties:

```
[Obsolete ("Use Model instead"]
	public UIPickerViewModel Source { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIPickerViewModel

Added constructors:

```
public UIPickerViewModel (MonoTouch.Foundation.NSCoder coder);
	public UIPickerViewModel (MonoTouch.Foundation.NSObjectFlag t);
	public UIPickerViewModel (IntPtr handle);
```

Added interfaces:

```
IUIPickerViewModel
	IUIPickerViewDataSource
	IUIPickerViewDelegate
```

Modified methods:

```
public virtual int GetComponentCount (UIPickerView picker pickerView)
	public virtual float GetComponentWidth (UIPickerView picker pickerView, int component)
	public virtual float GetRowHeight (UIPickerView picker pickerView, int component)
	public virtual int GetRowsInComponent (UIPickerView picker pickerView, int component)
	public virtual string GetTitle (UIPickerView picker pickerView, int row, int component)
	public virtual UIView GetView (UIPickerView picker pickerView, int row, int component, UIView view)
	public virtual void Selected (UIPickerView picker pickerView, int row, int component)
```

Added method:

```
public virtual MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIPickerView pickerView, int row, int component);
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interfaces:

```
IUIPopoverBackgroundViewMethods
```

### Type Changed: MonoTouch.UIKit.UIPopoverPresentationController

Added constructor:

```
public UIPopoverPresentationController (UIViewController presentedViewController, UIViewController presentingViewController);
```

Obsoleted properties:

```
[Obsolete ("Use the Delegate property"]
	public UIPopoverPresentationControllerDelegate Delegat { get; set; }
```

Added properties:

```
public UIPopoverPresentationControllerDelegate Delegate { get; set; }
	public virtual System.Type PopoverBackgroundViewType { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIStateRestoring_Extensions

Added methods:

```
public static MonoTouch.ObjCRuntime.Class GetObjectRestorationClass (IUIStateRestoring This);
	public static IUIStateRestoring GetRestorationParent (IUIStateRestoring This);
```

### Type Changed: MonoTouch.UIKit.UITableView

Modified methods:

```
public virtual void RegisterNibForHeaderFooterViewReuse (UINib nib, string identifier reuseIdentifier)
```

Added methods:

```
public UITableViewCell DequeueReusableCell (string reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
	public UITableViewHeaderFooterView DequeueReusableHeaderFooterView (string reuseIdentifier);
	public void RegisterClassForCellReuse (System.Type cellType, string reuseIdentifier);
	public void RegisterClassForHeaderFooterViewReuse (System.Type cellType, string reuseIdentifier);
	public void RegisterNibForCellReuse (UINib nib, MonoTouch.Foundation.NSString reuseIdentifier);
	public virtual void RegisterNibForHeaderFooterViewReuse (UINib nib, MonoTouch.Foundation.NSString reuseIdentifier);
```

### Type Changed: MonoTouch.UIKit.UITextInput_Extensions

Added method:

```
public static UIView GetTextInputView (IUITextInput This);
```

### Type Changed: MonoTouch.UIKit.UITraitEnvironment_Extensions

Added method:

```
public static UITraitCollection GetTraitCollection (IUITraitEnvironment This);
```

### Type Changed: MonoTouch.UIKit.UIVibrancyEffect

Added method:

```
public static UIVibrancyEffect CreateForNotificationCenter ();
```

### Type Changed: MonoTouch.UIKit.UIViewControllerContextTransitioning_Extensions

Added method:

```
public static MonoTouch.CoreGraphics.CGAffineTransform GetTargetTransform (IUIViewControllerContextTransitioning This);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerInteractiveTransitioning_Extensions

Added methods:

```
public static UIViewAnimationCurve GetCompletionCurve (IUIViewControllerInteractiveTransitioning This);
	public static float GetCompletionSpeed (IUIViewControllerInteractiveTransitioning This);
```

### New Type MonoTouch.UIKit.INSTextLayoutOrientationProvider

```
public interface INSTextLayoutOrientationProvider : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual NSTextLayoutOrientation LayoutOrientation { get; set; }
}
```

### New Type MonoTouch.UIKit.IUIAccessibilityReadingContent

```
public interface IUIAccessibilityReadingContent : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual string GetAccessibilityContent (int lineNumber);
	public virtual System.Drawing.RectangleF GetAccessibilityFrame (int lineNumber);
	public virtual int GetAccessibilityLineNumber (System.Drawing.PointF point);
	public virtual string GetAccessibilityPageContent ();
}
```

### New Type MonoTouch.UIKit.IUIDataSourceModelAssociation

```
public interface IUIDataSourceModelAssociation : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual MonoTouch.Foundation.NSIndexPath GetIndexPath (string identifier, UIView view);
	public virtual string GetModelIdentifier (MonoTouch.Foundation.NSIndexPath idx, UIView view);
}
```

### New Type MonoTouch.UIKit.IUIGuidedAccessRestrictionDelegate

```
public interface IUIGuidedAccessRestrictionDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual string[] GetGuidedAccessRestrictionIdentifiers { get; }
	// methods
	public virtual string GetTextForGuidedAccessRestriction (string restrictionIdentifier);
	public virtual void GuidedAccessRestrictionChangedState (string restrictionIdentifier, UIGuidedAccessRestrictionState newRestrictionState);
}
```

### New Type MonoTouch.UIKit.IUIObjectRestoration

```
public interface IUIObjectRestoration : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIPickerViewModel

```
public interface IUIPickerViewModel : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIPickerViewDataSource, IUIPickerViewDelegate {
}
```

### New Type MonoTouch.UIKit.IUIPopoverBackgroundViewMethods

```
public interface IUIPopoverBackgroundViewMethods : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.NSTextLayoutOrientationProvider_Extensions

```
public static class NSTextLayoutOrientationProvider_Extensions {
}
```

### New Type MonoTouch.UIKit.UIAccessibilityReadingContent_Extensions

```
public static class UIAccessibilityReadingContent_Extensions {
}
```

### New Type MonoTouch.UIKit.UIDataSourceModelAssociation_Extensions

```
public static class UIDataSourceModelAssociation_Extensions {
}
```

### New Type MonoTouch.UIKit.UIGuidedAccessRestrictionDelegate_Extensions

```
public static class UIGuidedAccessRestrictionDelegate_Extensions {
	// methods
	public static string GetDetailTextForGuidedAccessRestriction (IUIGuidedAccessRestrictionDelegate This, string restrictionIdentifier);
}
```

### New Type MonoTouch.UIKit.UIObjectRestoration

```
public class UIObjectRestoration : MonoTouch.Foundation.NSObject, IUIObjectRestoration, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSObjectProtocol {
	// constructors
	public UIObjectRestoration ();
	public UIObjectRestoration (MonoTouch.Foundation.NSCoder coder);
	public UIObjectRestoration (MonoTouch.Foundation.NSObjectFlag t);
	public UIObjectRestoration (IntPtr handle);
}
```

### New Type MonoTouch.UIKit.UIObjectRestoration_Extensions

```
public static class UIObjectRestoration_Extensions {
}
```

### New Type MonoTouch.UIKit.UIPickerViewModel_Extensions

```
public static class UIPickerViewModel_Extensions {
}
```

### New Type MonoTouch.UIKit.UIPopoverBackgroundViewMethods_Extensions

```
public static class UIPopoverBackgroundViewMethods_Extensions {
}
```

### New Type MonoTouch.UIKit.UIStringDrawing

```
public static class UIStringDrawing {
	// methods
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.PointF point, UIFont font);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode, UITextAlignment alignment);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, UIFont font);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, float width, UIFont font, UILineBreakMode breakMode);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, float width, UIFont font, float fontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, float width, UIFont font, float minFontSize, ref float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, UIFont font);
	public static System.Drawing.SizeF DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.PointF point, float width, UIFont font, UILineBreakMode breakMode);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.PointF point, float width, UIFont font, float fontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.PointF point, float width, UIFont font, float minFontSize, ref float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.RectangleF rect, UIFont font);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode);
	public static System.Drawing.SizeF DrawString (string This, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode, UITextAlignment alignment);
	public static System.Drawing.SizeF StringSize (MonoTouch.Foundation.NSString This, UIFont font);
	public static System.Drawing.SizeF StringSize (MonoTouch.Foundation.NSString This, UIFont font, float forWidth, UILineBreakMode breakMode);
	public static System.Drawing.SizeF StringSize (MonoTouch.Foundation.NSString This, UIFont font, System.Drawing.SizeF constrainedToSize, UILineBreakMode lineBreakMode);
	public static System.Drawing.SizeF StringSize (MonoTouch.Foundation.NSString This, UIFont font, System.Drawing.SizeF constrainedToSize);
	public static System.Drawing.SizeF StringSize (string This, UIFont font, float minFontSize, ref float actualFontSize, float forWidth, UILineBreakMode lineBreakMode);
	public static System.Drawing.SizeF StringSize (string This, UIFont font, System.Drawing.SizeF constrainedToSize, UILineBreakMode lineBreakMode);
	public static System.Drawing.SizeF StringSize (string This, UIFont font, System.Drawing.SizeF constrainedToSize);
	public static System.Drawing.SizeF StringSize (string This, UIFont font, float forWidth, UILineBreakMode breakMode);
	public static System.Drawing.SizeF StringSize (string This, UIFont font);
	public static System.Drawing.SizeF StringSize (MonoTouch.Foundation.NSString This, UIFont font, float minFontSize, ref float actualFontSize, float forWidth, UILineBreakMode lineBreakMode);
}
```

### New Type MonoTouch.UIKit.UIView_UITextField

```
public static class UIView_UITextField {
	// methods
	public static bool EndEditing (UIView This, bool force);
}
```

   


 <hr>

# OpenTK.dll

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVOpenGLESTexture

Obsoleted methods:

```
[Obsolete ("Use GetCleanTexCoords instead"]
	public void GetCleanTextCoords (out float[] lowerLeft, out float[] lowerRight, out float[] upperRight, out float[] upperLeft);
```

Added method:

```
public void GetCleanTexCoords (out float[] lowerLeft, out float[] lowerRight, out float[] upperRight, out float[] upperLeft);
```

   


 <hr>

# OpenTK-1.0.dll

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVOpenGLESTexture

Obsoleted methods:

```
[Obsolete ("Use GetCleanTexCoords instead"]
	public void GetCleanTextCoords (out float[] lowerLeft, out float[] lowerRight, out float[] upperRight, out float[] upperLeft);
```

Added method:

```
public void GetCleanTexCoords (out float[] lowerLeft, out float[] lowerRight, out float[] upperRight, out float[] upperLeft);
```

   


 <hr>

# MonoTouch.Dialog-1.dll

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.DialogViewController.Source

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.DialogViewController.SizingSource

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.GlassButton

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

   


 <hr>

# MonoTouch.NUnitLite.dll

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

   


 <hr>

# OpenTK-1.0.dll

## Namespace CoreVideo

### Type Changed: CoreVideo.CVOpenGLESTextureCache

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

```
System.IEquatable<Foundation.NSObject>
```

   


 <hr>
