---
id: B0CDA3EA-CC3C-455F-AF15-CBD10F295630
title: "From 7.9.1 to 7.9.2"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "7.9.1";
```

Added fields:

```
public static const string CoreAudioKitLibrary = "/System/Library/Frameworks/CoreAudioKit.framework/CoreAudioKit";
	public static const string Version = "7.9.2";
```

## Namespace MonoTouch.Accounts

### Type Changed: MonoTouch.Accounts.ACErrorCode

Added values:

```
CoreDataSaveFailed = 18,
	FailedSerializingAccountInfo = 19,
	InvalidCommand = 20,
	MissingMessageID = 21,
```

## Namespace MonoTouch.AddressBook

### Type Changed: MonoTouch.AddressBook.ABRecord

Added method:

```
public static ABRecord FromHandle (System.IntPtr handle);
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate

Removed method:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, System.IntPtr abMultiValueIdentifier);
```

Added method:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions

Removed method:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, System.IntPtr abMultiValueIdentifier);
```

Added method:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added value:

```
AMRWideBand = 1935767394,
```

### Type Changed: MonoTouch.AudioToolbox.AudioStreamBasicDescription

Added fields:

```
public static AudioFormatFlags AudioFormatFlagsAudioUnitNativeFloat;
	public static AudioFormatFlags AudioFormatFlagsNativeFloat;
```

Obsoleted field:

```
[Obsolete ("Canonical is no longer encouraged, since fixed-point no longer provides a performance advantage over floating point.   AudioFormatFlagsNativeFloatPacked is preffered instead")]
	public static AudioFormatFlags AudioFormatFlagsAudioUnitCanonical;
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioTypeConverter

Added value:

```
RoundTripAAC = 1918984547,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitParameterType

Added values:

```
Distance = 2,
	Elevation = 1,
	Enable = 5,
	Gain = 3,
	GlobalReverbGain = 9,
	MaxGain = 7,
	MinGain = 6,
	ObstructionAttenuation = 11,
	OcclussionAttenuation = 10,
	PlaybackRate = 4,
	ReverbBlend = 8,
	RoundTripAacEncodingStrategy = 1,
	RoundTripAacFormat = 0,
	RoundTripAacRateOrQuality = 2,
	SpacialMixerAzimuth = 0,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added value:

```
MidiSynthEnablePreload = 4119,
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAssetWriter

Added property:

```
public virtual MonoTouch.Foundation.NSString[] AvailableMediaTypes { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAudioChannelLayout

Removed property:

```
public virtual System.IntPtr _Layout { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAudioEnvironmentNode

Added property:

```
public virtual float OutputVolume { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSessionErrorCode

Added value:

```
InsufficientPriority = 561017449,
```

### Type Changed: MonoTouch.AVFoundation.AVAudioUnitSampler

Removed method:

```
public virtual bool LoadSoundBank (MonoTouch.Foundation.NSUrl bankUrl, out MonoTouch.Foundation.NSError outError);
```

Added method:

```
public virtual bool LoadSoundBank (MonoTouch.Foundation.NSUrl bankUrl, byte program, byte bankMSB, byte bankLSB, out MonoTouch.Foundation.NSError outError);
```

### Type Changed: MonoTouch.AVFoundation.AVSampleBufferDisplayLayer

Added properties:

```
public virtual MonoTouch.Foundation.NSError Error { get; }
	public virtual AVQueuedSampleBufferRenderingStatus Status { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### New Type MonoTouch.AVFoundation.AVQueuedSampleBufferRenderingStatus

```
[Serializable]
public enum AVQueuedSampleBufferRenderingStatus {
	Failed = 2,
	Rendering = 1,
	Unknown = 0,
}
```

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKDatabaseOperation

Removed constructor:

```
public CKDatabaseOperation ();
```

### Type Changed: MonoTouch.CloudKit.CKErrorCode

Added values:

```
LimitExceeded = 27,
	UserDeletedZone = 28,
```

### Type Changed: MonoTouch.CloudKit.CKFetchNotificationChangesOperation

Added property:

```
public virtual bool MoreComing { get; }
```

### Type Changed: MonoTouch.CloudKit.CKModifyBadgeOperation

Removed property:

```
public virtual bool ThisDeviceOnly { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKNotificationInfo

Added property:

```
public virtual bool ShouldSendContentAvailable { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKSubscriptionOptions

Removed value:

```
ThisClientOnly = 16,
```

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Added properties:

```
public virtual MonoTouch.Foundation.NSNumber[] BiasValues { get; set; }
	public virtual MonoTouch.Foundation.NSNumber[] ContinuityValues { get; set; }
	public virtual MonoTouch.Foundation.NSNumber[] TensionValues { get; set; }
```

### Type Changed: MonoTouch.CoreAnimation.CALayer

Added properties:

```
public virtual MonoTouch.CoreImage.CIFilter[] BackgroundFilters { get; set; }
	public virtual MonoTouch.CoreImage.CIFilter[] Filters { get; set; }
	public virtual float MinificationFilterBias { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary Style { get; set; }
```

### Type Changed: MonoTouch.CoreAnimation.CAMetalLayer

Removed property:

```
public virtual System.Drawing.RectangleF DrawableSize { get; set; }
```

Added property:

```
public virtual System.Drawing.SizeF DrawableSize { get; set; }
```

Added method:

```
public virtual ICAMetalDrawable NextDrawable ();
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCentral

Removed property:

```
public virtual MonoTouch.Foundation.NSUuid Identifier { get; }
```

Removed method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.CoreBluetooth.CBCharacteristic

Removed property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBDescriptor

Removed property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Removed properties:

```
public virtual MonoTouch.Foundation.NSUuid Identifier { get; }

	[Obsolete ("Deprecated in iOS7")]
	public virtual System.IntPtr UUID { get; }
```

### Type Changed: MonoTouch.CoreBluetooth.CBService

Removed property:

```
public virtual CBUUID UUID { get; }
```

### New Type MonoTouch.CoreBluetooth.CBAttribute

```
public class CBAttribute : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBAttribute ();
	public CBAttribute (MonoTouch.Foundation.NSCoder coder);
	public CBAttribute (MonoTouch.Foundation.NSObjectFlag t);
	public CBAttribute (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CBUUID UUID { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreBluetooth.CBPeer

```
public class CBPeer : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CBPeer ();
	public CBPeer (MonoTouch.Foundation.NSCoder coder);
	public CBPeer (MonoTouch.Foundation.NSObjectFlag t);
	public CBPeer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUuid Identifier { get; }
	public virtual CBUUID UUID { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added property:

```
public virtual string Name { get; set; }
```

Added method:

```
public virtual NSPersistentStoreResult ExecuteRequest (NSPersistentStoreRequest request, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

Added property:

```
public virtual string Name { get; set; }
```

Added methods:

```
public virtual void Perform (System.Action code);
	public virtual void PerformAndWait (System.Action code);
```

### Type Changed: MonoTouch.CoreData.NSPersistentStoreRequestType

Added value:

```
BatchUpdate = 6,
```

### New Type MonoTouch.CoreData.NSAsynchronousFetchRequest

```
public class NSAsynchronousFetchRequest : MonoTouch.CoreData.NSPersistentStoreRequest, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchRequest ();
	public NSAsynchronousFetchRequest (MonoTouch.Foundation.NSCoder coder);
	public NSAsynchronousFetchRequest (MonoTouch.Foundation.NSObjectFlag t);
	public NSAsynchronousFetchRequest (System.IntPtr handle);
	public NSAsynchronousFetchRequest (NSFetchRequest request, System.Action<NSAsynchronousFetchResult> completion);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int EstimatedResultCount { get; set; }
	public virtual NSFetchRequest FetchRequest { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreData.NSAsynchronousFetchResult

```
public class NSAsynchronousFetchResult : MonoTouch.CoreData.NSPersistentStoreAsynchronousResult, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchResult ();
	public NSAsynchronousFetchResult (MonoTouch.Foundation.NSCoder coder);
	public NSAsynchronousFetchResult (MonoTouch.Foundation.NSObjectFlag t);
	public NSAsynchronousFetchResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSAsynchronousFetchRequest FetchRequest { get; }
	public virtual MonoTouch.Foundation.NSObject[] FinalResult { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreData.NSBatchUpdateRequest

```
public class NSBatchUpdateRequest : MonoTouch.CoreData.NSPersistentStoreRequest, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateRequest ();
	public NSBatchUpdateRequest (MonoTouch.Foundation.NSCoder coder);
	public NSBatchUpdateRequest (MonoTouch.Foundation.NSObjectFlag t);
	public NSBatchUpdateRequest (System.IntPtr handle);
	public NSBatchUpdateRequest (string entityName);
	public NSBatchUpdateRequest (NSEntityDescription entity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSEntityDescription Entity { get; }
	public virtual string EntityName { get; }
	public virtual bool IncludesSubentities { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary PropertiesToUpdate { get; set; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; set; }
	// methods
	public static NSBatchUpdateRequest BatchUpdateRequestWithEntityName (string entityName);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreData.NSBatchUpdateRequestResultType

```
[Serializable]
public enum NSBatchUpdateRequestResultType {
	StatusOnly = 0,
	UpdatedObjectIDs = 1,
	UpdatedObjectsCount = 2,
}
```

### New Type MonoTouch.CoreData.NSBatchUpdateResult

```
public class NSBatchUpdateResult : MonoTouch.CoreData.NSPersistentStoreResult, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateResult ();
	public NSBatchUpdateResult (MonoTouch.Foundation.NSCoder coder);
	public NSBatchUpdateResult (MonoTouch.Foundation.NSObjectFlag t);
	public NSBatchUpdateResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject Result { get; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreData.NSPersistentStoreAsynchronousResult

```
public class NSPersistentStoreAsynchronousResult : MonoTouch.CoreData.NSPersistentStoreResult, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreAsynchronousResult ();
	public NSPersistentStoreAsynchronousResult (MonoTouch.Foundation.NSCoder coder);
	public NSPersistentStoreAsynchronousResult (MonoTouch.Foundation.NSObjectFlag t);
	public NSPersistentStoreAsynchronousResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSManagedObjectContext ManagedObjectContext { get; }
	public virtual MonoTouch.Foundation.NSError OperationError { get; }
	public virtual MonoTouch.Foundation.NSProgress Progress { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreData.NSPersistentStoreResult

```
public class NSPersistentStoreResult : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreResult ();
	public NSPersistentStoreResult (MonoTouch.Foundation.NSCoder coder);
	public NSPersistentStoreResult (MonoTouch.Foundation.NSObjectFlag t);
	public NSPersistentStoreResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIColor

Added property:

```
public float[] Components { get; }
```

### Type Changed: MonoTouch.CoreImage.CIImage

Added method:

```
public static CIImage ImageWithTexture (uint glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace colorspace);
```

### Type Changed: MonoTouch.CoreImage.CIVector

Added constructors:

```
public CIVector (MonoTouch.CoreGraphics.CGAffineTransform r);
	public CIVector (System.Drawing.RectangleF r);
	public CIVector (System.Drawing.PointF p);
```

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLFloor

Removed property:

```
public virtual uint Level { get; }
```

Added property:

```
public virtual int Level { get; }
```

### Type Changed: MonoTouch.CoreLocation.CLLocationManager

Added property:

```
public static bool IsRangingAvailable { get; }
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added method:

```
protected void SetArrayValue<T> (NSString key, T[] values);
```

### Type Changed: MonoTouch.Foundation.NSAttributedString

Added interface:

```
INSSecureCoding
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

### Type Changed: MonoTouch.Foundation.NSByteCountFormatter

Added property:

```
public virtual NSFormattingContext FormattingContext { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSData

Added methods:

```
public virtual bool Save (string path, bool atomically);
	public virtual bool Save (NSUrl url, bool atomically);
```

### Type Changed: MonoTouch.Foundation.NSDateFormatter

Added method:

```
public virtual void SetLocalizedDateFormatFromTemplate (string dateFormatTemplate);
```

### Type Changed: MonoTouch.Foundation.NSError

Added properties:

```
public virtual string HelpAnchor { get; }
	public virtual string LocalizedFailureReason { get; }
	public virtual string[] LocalizedRecoveryOptions { get; }
	public virtual string LocalizedRecoverySuggestion { get; }
```

### Type Changed: MonoTouch.Foundation.NSFileManager

Added methods:

```
public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
```

### Type Changed: MonoTouch.Foundation.NSIndexSet

Added methods:

```
public virtual void EnumerateIndexes (NSRange range, NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (EnumerateIndexSetCallback enumeratorCallback);
```

### Type Changed: MonoTouch.Foundation.NSLengthFormatter

Added property:

```
public virtual bool ForPersonHeightUse { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSMachPort

Added constructors:

```
public NSMachPort (uint machPort);
	public NSMachPort (uint machPort, NSMachPortRights options);
```

### Type Changed: MonoTouch.Foundation.NSMetadataQuery

Added properties:

```
public static NSString ContentTypeKey { get; }
	public static NSString ContentTypeTreeKey { get; }
	public static NSString QueryAccessibleUbiquitousExternalDocumentsScope { get; }
	public static NSString UbiquitousItemContainerDisplayNameKey { get; }
	public static NSString UbiquitousItemDownloadRequestedKey { get; }
	public static NSString UbiquitousItemIsExternalDocumentKey { get; }
	public static NSString UbiquitousItemURLInLocalContainerKey { get; }
```

### Type Changed: MonoTouch.Foundation.NSMethodSignature

Added property:

```
public virtual System.IntPtr MethodReturnType { get; }
```

Added methods:

```
public static NSMethodSignature FromObjcTypes (System.IntPtr utf8objctypes);
	public virtual System.IntPtr GetArgumentType (uint index);
```

### Type Changed: MonoTouch.Foundation.NSMutableArray

Added methods:

```
public static NSMutableArray FromFile (string path);
	public static NSMutableArray FromUrl (NSUrl url);
```

### Type Changed: MonoTouch.Foundation.NSMutableAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoTouch.Foundation.NSObject

Added method:

```
public virtual void RemoveObserver (NSObject observer, NSString keyPath, System.IntPtr context);
```

### Type Changed: MonoTouch.Foundation.NSPort

Added methods:

```
public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual bool SendBeforeDate (NSDate limitDate, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
	public virtual bool SendBeforeDate (NSDate limitDate, uint msgID, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
```

### Type Changed: MonoTouch.Foundation.NSProcessInfo

Added property:

```
public virtual NSOperatingSystemVersion OperatingSystemVersion { get; }
```

Added method:

```
public virtual bool IsOperatingSystemAtLeastVersion (NSOperatingSystemVersion version);
```

### Type Changed: MonoTouch.Foundation.NSSet

Added method:

```
public virtual NSObject LookupMember (NSObject probe);
```

### Type Changed: MonoTouch.Foundation.NSStream

Added methods:

```
public static void GetBoundStreams (uint bufferSize, out NSInputStream inputStream, out NSOutputStream outputStream);
	public static void GetStreamsToHost (string hostname, int port, out NSInputStream inputStream, out NSOutputStream outputStream);
```

### Type Changed: MonoTouch.Foundation.NSString

Added methods:

```
public virtual bool Contains (NSString str);
	public static uint DetectStringEncoding (NSData rawData, NSDictionary options, out string convertedString, out bool usedLossyConversion);
	public static uint DetectStringEncoding (NSData rawData, EncodingDetectionOptions options, out string convertedString, out bool usedLossyConversion);
	public virtual bool LocalizedCaseInsensitiveContains (NSString str);
```

### Type Changed: MonoTouch.Foundation.NSThread

Added property:

```
public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSUrl

Added properties:

```
public static NSString AddedToDirectoryDateKey { get; }
	public static NSString DocumentIdentifierKey { get; }
	public static NSString GenerationIdentifierKey { get; }
	public static NSString ThumbnailDictionaryKey { get; }
	public static NSString UbiquitousItemContainerDisplayNameKey { get; }
	public static NSString UbiquitousItemDownloadRequestedKey { get; }
```

Added methods:

```
public bool SetResource (NSString nsUrlResourceKey, NSObject value, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value, out NSError error);
```

### Type Changed: MonoTouch.Foundation.NSUrlCache

Added methods:

```
public virtual void GetCachedResponse (NSUrlSessionDataTask dataTask, System.Action<NSCachedUrlResponse> completionHandler);
	public virtual System.Threading.Tasks.Task<NSCachedUrlResponse> GetCachedResponseAsync (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponse (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponsesSinceDate (NSDate date);
	public virtual void StoreCachedResponse (NSCachedUrlResponse cachedResponse, NSUrlSessionDataTask dataTask);
```

### Type Changed: MonoTouch.Foundation.NSUrlComponents

Added property:

```
public virtual NSUrlQueryItem[] QueryItems { get; set; }
```

Added method:

```
public override string ToString ();
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDataTask

Removed interface:

```
INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTask

Removed interface:

```
INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionTask

Removed interface:

```
INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionUploadTask

Removed interface:

```
INSCoding
```

### New Type MonoTouch.Foundation.EncodingDetectionOptions

```
public class EncodingDetectionOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public EncodingDetectionOptions ();
	public EncodingDetectionOptions (NSDictionary dictionary);
	// properties
	public bool? EncodingDetectionAllowLossy { get; set; }
	public NSStringEncoding[] EncodingDetectionDisallowedEncodings { get; set; }
	public bool? EncodingDetectionFromWindows { get; set; }
	public NSString EncodingDetectionLikelyLanguage { get; set; }
	public NSString EncodingDetectionLossySubstitution { get; set; }
	public NSStringEncoding[] EncodingDetectionSuggestedEncodings { get; set; }
	public bool? EncodingDetectionUseOnlySuggestedEncodings { get; set; }
}
```

### New Type MonoTouch.Foundation.EnumerateIndexSetCallback

```
public sealed delegate EnumerateIndexSetCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public EnumerateIndexSetCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint idx, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (uint idx, ref bool stop);
}
```

### New Type MonoTouch.Foundation.NSOperatingSystemVersion

```
public struct NSOperatingSystemVersion {
	// constructors
	public NSOperatingSystemVersion (int major, int minor, int patchVersion);
	// fields
	public int Major;
	public int Minor;
	public int PatchVersion;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.Foundation.NSUrl_PromisedItems

```
public static class NSUrl_PromisedItems {
	// methods
	public static bool CheckPromisedItemIsReachable (NSUrl This, out NSError error);
	public static bool GetPromisedItemResourceValue (NSUrl This, NSObject value, NSString key, out NSError error);
	public static NSDictionary GetPromisedItemResourceValues (NSUrl This, NSString[] keys, out NSError error);
}
```

### New Type MonoTouch.Foundation.NSUrlQueryItem

```
public class NSUrlQueryItem : MonoTouch.Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlQueryItem ();
	public NSUrlQueryItem (NSCoder coder);
	public NSUrlQueryItem (NSObjectFlag t);
	public NSUrlQueryItem (System.IntPtr handle);
	public NSUrlQueryItem (string name, string value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public virtual string Value { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
}
```

### New Type MonoTouch.Foundation.NSURLRelationship

```
[Serializable]
public enum NSURLRelationship {
	Contains = 0,
	Other = 2,
	Same = 1,
}
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKInvite

Added property:

```
public virtual GKPlayer Sender { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.GameKit.GKInviteEventListener

Added method:

```
public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
```

### Type Changed: MonoTouch.GameKit.GKInviteEventListener_Extensions

Added method:

```
public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, GKPlayer[] recipientPlayers);
```

### Type Changed: MonoTouch.GameKit.GKLocalPlayer

Added methods:

```
public virtual void DeleteSavedGamesWithName (string name, System.Action<MonoTouch.Foundation.NSError> handler);
	public virtual void FetchSavedGamesWithCompletionHandler (System.Action<MonoTouch.Foundation.NSArray,MonoTouch.Foundation.NSError> handler);
	public virtual void ResolveConflictingSavedGames (MonoTouch.Foundation.NSObject[] conflictingSavedGames, MonoTouch.Foundation.NSData data, System.Action<MonoTouch.Foundation.NSArray,MonoTouch.Foundation.NSError> handler);
	public virtual void SaveGameData (MonoTouch.Foundation.NSData data, string name, System.Action<GKSavedGame,MonoTouch.Foundation.NSError> handler);
```

### Type Changed: MonoTouch.GameKit.GKLocalPlayerListener

Added methods:

```
public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
```

### Type Changed: MonoTouch.GameKit.GKMatch

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public GKMatchReinvitationForDisconnectedPlayer ShouldReinviteDisconnectedPlayer { get; set; }
```

Added events:

```
public event System.EventHandler<GKMatchConnectionChangedEventArgs> ChangedConnectionState;
	public event System.EventHandler<GKMatchReceivedDataFromRemotePlayerEventArgs> ReceivedDataFromRemotePlayer;
```

Added methods:

```
public virtual void ChooseBestHostingPlayer (System.Action<GKPlayer> completionHandler);
	public virtual bool SendData (MonoTouch.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate

Added methods:

```
public virtual void ChangedConnectionState (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public virtual void ReceivedDataFromRemotePlayer (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
	public virtual bool ShouldReinviteDisconnectedPlayer (GKMatch match, GKPlayer player);
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate_Extensions

Added methods:

```
public static void ChangedConnectionState (IGKMatchDelegate This, GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public static void ReceivedDataFromRemotePlayer (IGKMatchDelegate This, GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
	public static bool ShouldReinviteDisconnectedPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player);
```

### Type Changed: MonoTouch.GameKit.GKMatchmaker

Added methods:

```
public virtual void CancelPendingInvite (GKPlayer player);
	public virtual void FindPlayersForHostedRequest (GKMatchRequest request, System.Action<GKPlayer[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> FindPlayersForHostedRequestAsync (GKMatchRequest request);
	public virtual void StartBrowsingForNearbyPlayersWithHandler (System.Action<GKPlayer,System.Boolean> reachableHandler);
```

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Added events:

```
public event System.EventHandler<GKMatchmakingPlayersEventArgs> DidFindHostedPlayers;
	public event System.EventHandler<GKMatchmakingPlayerEventArgs> HostedPlayerDidAccept;
```

Added method:

```
public virtual void SetHostedPlayerDidConnect (GKPlayer playerID, bool connected);
```

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate

Added methods:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
	public virtual void HostedPlayerDidAccept (GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate_Extensions

Added method:

```
public static void HostedPlayerDidAccept (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoTouch.GameKit.GKMatchRequest

Added properties:

```
public virtual System.Action<GKPlayer,MonoTouch.GameKit.GKInviteRecipientResponse> RecipientResponseHandler { get; set; }
	public virtual GKPlayer[] Recipients { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.GameKit.GKScore

Added constructor:

```
public GKScore (string identifier, GKPlayer player);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventListener

Added method:

```
public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedEventListener_Extensions

Added method:

```
public static void DidRequestMatchWithOtherPlayers (IGKTurnBasedEventListener This, GKPlayer player, GKPlayer[] playersToInvite);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedExchangeReply

Added property:

```
public virtual MonoTouch.Foundation.NSDate ReplyDate { get; }
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedParticipant

Added property:

```
public virtual GKPlayer Player { get; }
```

### Type Changed: MonoTouch.GameKit.GKVoiceChat

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public virtual System.Action<GKPlayer,MonoTouch.GameKit.GKVoiceChatPlayerState> PlayerVoiceChatStateDidChangeHandler { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetMuteStatus (GKPlayer player, bool isMuted);
```

### Type Changed: MonoTouch.GameKit.IGKMatchmakerViewControllerDelegate

Added method:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
```

### New Type MonoTouch.GameKit.GKInviteRecipientResponse

```
[Serializable]
public enum GKInviteRecipientResponse {
	Accepted = 0,
	Declined = 1,
	Failed = 2,
	Incompatible = 3,
	NoAnswer = 5,
	UnableToConnect = 4,
}
```

### New Type MonoTouch.GameKit.GKMatchConnectionChangedEventArgs

```
public class GKMatchConnectionChangedEventArgs : System.EventArgs {
	// constructors
	public GKMatchConnectionChangedEventArgs (GKPlayer player, GKPlayerConnectionState state);
	// properties
	public GKPlayer Player { get; set; }
	public GKPlayerConnectionState State { get; set; }
}
```

### New Type MonoTouch.GameKit.GKMatchmakingPlayerEventArgs

```
public class GKMatchmakingPlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayerEventArgs (GKPlayer playerID);
	// properties
	public GKPlayer PlayerID { get; set; }
}
```

### New Type MonoTouch.GameKit.GKMatchmakingPlayersEventArgs

```
public class GKMatchmakingPlayersEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayersEventArgs (GKPlayer[] playerIDs);
	// properties
	public GKPlayer[] PlayerIDs { get; set; }
}
```

### New Type MonoTouch.GameKit.GKMatchReceivedDataFromRemotePlayerEventArgs

```
public class GKMatchReceivedDataFromRemotePlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchReceivedDataFromRemotePlayerEventArgs (MonoTouch.Foundation.NSData data, GKPlayer player);
	// properties
	public MonoTouch.Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
}
```

### New Type MonoTouch.GameKit.GKMatchReinvitationForDisconnectedPlayer

```
public sealed delegate GKMatchReinvitationForDisconnectedPlayer : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKMatchReinvitationForDisconnectedPlayer (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (GKMatch match, GKPlayer player, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (GKMatch match, GKPlayer player);
}
```

### New Type MonoTouch.GameKit.GKSavedGame

```
public class GKSavedGame : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGame ();
	public GKSavedGame (MonoTouch.Foundation.NSCoder coder);
	public GKSavedGame (MonoTouch.Foundation.NSObjectFlag t);
	public GKSavedGame (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DeviceName { get; }
	public virtual MonoTouch.Foundation.NSDate ModificationDate { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void LoadDataWithCompletionHandler (System.Action<MonoTouch.Foundation.NSData,MonoTouch.Foundation.NSError> handler);
}
```

### New Type MonoTouch.GameKit.GKSavedGameListener

```
public class GKSavedGameListener : MonoTouch.Foundation.NSObject, IGKSavedGameListener, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGameListener ();
	public GKSavedGameListener (MonoTouch.Foundation.NSCoder coder);
	public GKSavedGameListener (MonoTouch.Foundation.NSObjectFlag t);
	public GKSavedGameListener (System.IntPtr handle);
	// methods
	public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void HasConflictingSavedGames (GKPlayer player, MonoTouch.Foundation.NSObject[] savedGames);
}
```

### New Type MonoTouch.GameKit.GKSavedGameListener_Extensions

```
public static class GKSavedGameListener_Extensions {
	// methods
	public static void DidModifySavedGame (IGKSavedGameListener This, GKPlayer player, GKSavedGame savedGame);
	public static void HasConflictingSavedGames (IGKSavedGameListener This, GKPlayer player, MonoTouch.Foundation.NSObject[] savedGames);
}
```

### New Type MonoTouch.GameKit.IGKSavedGameListener

```
public interface IGKSavedGameListener : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKCategoryType

Added method:

```
public static HKCategoryType Create (HKCategoryTypeIdentifier kind);
```

### Type Changed: MonoTouch.HealthKit.HKCharacteristicType

Added method:

```
public static HKCharacteristicType Create (HKCharacteristicTypeIdentifier kind);
```

### Type Changed: MonoTouch.HealthKit.HKCorrelation

Added property:

```
public virtual HKCorrelationType CorrelationType { get; }
```

Removed methods:

```
public static HKCorrelation FromObjects (MonoTouch.Foundation.NSSet objects);
	public static HKCorrelation FromObjects (MonoTouch.Foundation.NSSet objects, MonoTouch.Foundation.NSDictionary metadata);
	public static HKCorrelation FromObjects (MonoTouch.Foundation.NSSet objects, HKMetadata metadata);
```

Added methods:

```
public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects, MonoTouch.Foundation.NSDictionary metadata);
	public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects, HKMetadata metadata);
	public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects);
	public virtual MonoTouch.Foundation.NSSet GetObjects (HKObjectType objectType);
```

### Type Changed: MonoTouch.HealthKit.HKCorrelationQuery

Removed constructor:

```
public HKCorrelationQuery (MonoTouch.Foundation.NSObject[] types, MonoTouch.Foundation.NSPredicate predicate, MonoTouch.Foundation.NSPredicate samplePredicate, HKCorrelationQueryResultHandler completion);
```

Added constructor:

```
public HKCorrelationQuery (HKCorrelationType correlationType, MonoTouch.Foundation.NSPredicate predicate, MonoTouch.Foundation.NSDictionary samplePredicates, HKCorrelationQueryResultHandler completion);
```

Removed properties:

```
public virtual MonoTouch.Foundation.NSPredicate SamplePredicate { get; }
	public virtual MonoTouch.Foundation.NSObject[] Types { get; }
```

Added properties:

```
public virtual HKCorrelationType CorrelationType { get; }
	public virtual MonoTouch.Foundation.NSDictionary SamplePredicates { get; }
```

### Type Changed: MonoTouch.HealthKit.HKErrorCode

Removed values:

```
AuthorizationDenied = 3,
	AuthorizationNotDetermined = 4,
	DatabaseInaccessible = 5,
	InvalidArgument = 2,
```

Added values:

```
AuthorizationDenied = 4,
	AuthorizationNotDetermined = 5,
	DatabaseInaccessible = 6,
	HealthDataRestricted = 2,
	InvalidArgument = 3,
```

### Type Changed: MonoTouch.HealthKit.HKHealthStore

Added method:

```
public virtual void AddSamples (HKSample[] samples, HKWorkout workout, HKStoreSampleAddedCallback callback);
```

### Type Changed: MonoTouch.HealthKit.HKMetadata

Added properties:

```
public bool? CoachedWorkout { get; set; }
	public string DeviceManufacturerName { get; set; }
	public string DeviceName { get; set; }
	public string ExternalUuid { get; set; }
	public bool? GroupFitness { get; set; }
	public bool? IndoorWorkout { get; set; }
	public HKMovementType? MovementType { get; set; }
	public MonoTouch.Foundation.NSTimeZone TimeZone { get; set; }
	public bool? WasTakenInLab { get; set; }
	public bool? WasUserEntered { get; set; }
	public string WorkoutBrandName { get; set; }
```

### Type Changed: MonoTouch.HealthKit.HKMetadataKey

Added properties:

```
public static MonoTouch.Foundation.NSString CoachedWorkout { get; }
	public static MonoTouch.Foundation.NSString DeviceManufacturerName { get; }
	public static MonoTouch.Foundation.NSString DeviceName { get; }
	public static MonoTouch.Foundation.NSString ExternalUuid { get; }
	public static MonoTouch.Foundation.NSString GroupFitness { get; }
	public static MonoTouch.Foundation.NSString IndoorWorkout { get; }
	public static MonoTouch.Foundation.NSString MovementType { get; }
	public static MonoTouch.Foundation.NSString TimeZone { get; }
	public static MonoTouch.Foundation.NSString WasTakenInLab { get; }
	public static MonoTouch.Foundation.NSString WasUserEntered { get; }
	public static MonoTouch.Foundation.NSString WorkoutBrandName { get; }
```

### Type Changed: MonoTouch.HealthKit.HKObjectType

Added methods:

```
public static HKCorrelationType GetCorrelationType (MonoTouch.Foundation.NSString hkCorrelationTypeIdentifier);
	public static HKWorkout WorkoutType ();
```

### Type Changed: MonoTouch.HealthKit.HKQuantityType

Added method:

```
public static HKQuantityType Create (HKQuantityTypeIdentifier kind);
```

### Type Changed: MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

Removed properties:

```
public static MonoTouch.Foundation.NSString ActivityCount { get; }
	public static MonoTouch.Foundation.NSString DietaryCalories { get; }
	public static MonoTouch.Foundation.NSString GalvanicSkinResponse { get; }
	public static MonoTouch.Foundation.NSString PerfusionIndex { get; }
```

Added properties:

```
public static MonoTouch.Foundation.NSString DietaryCaffeine { get; }
	public static MonoTouch.Foundation.NSString PeripheralPerfusionIndex { get; }
```

### Type Changed: MonoTouch.HealthKit.HKQuery

Added methods:

```
public static MonoTouch.Foundation.NSPredicate GetPredicateForDuration (MonoTouch.Foundation.NSPredicateOperatorType operatorType, double duration);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObject (MonoTouch.Foundation.NSUuid objectUuid);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjects (MonoTouch.Foundation.NSSet objectUuids);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromWorkout (HKWorkout workout);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForTotalDistance (MonoTouch.Foundation.NSPredicateOperatorType operatorType, HKQuantity totalDistance);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForTotalEnergyBurned (MonoTouch.Foundation.NSPredicateOperatorType operatorType, HKQuantity totalEnergyBurned);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForWorkouts (HKWorkoutActivityType workoutActivityType);
	public static MonoTouch.Foundation.NSPredicate PredicateForObjectsWithNoCorrelation ();
```

### Type Changed: MonoTouch.HealthKit.HKUnit

Added properties:

```
public static HKUnit FluidOunceImperialUnit { get; }
	public static HKUnit FluidOunceUSUnit { get; }
	public static HKUnit PintImperialUnit { get; }
	public static HKUnit PintUSUnit { get; }
```

Removed method:

```
public static HKUnit CreateLeterUnit (HKMetricPrefix prefix);
```

Added method:

```
public static HKUnit CreateLiterUnit (HKMetricPrefix prefix);
```

### Removed Type MonoTouch.HealthKit.HKPrediateKeyPath ### New Type MonoTouch.HealthKit.HKCategoryTypeIdentifier

```
[Serializable]
public enum HKCategoryTypeIdentifier {
	SleepAnalysis = 0,
}
```

### New Type MonoTouch.HealthKit.HKCharacteristicTypeIdentifier

```
[Serializable]
public enum HKCharacteristicTypeIdentifier {
	BiologicalSex = 0,
	BloodType = 1,
	DateOfBirth = 2,
}
```

### New Type MonoTouch.HealthKit.HKCorrelatinTypeKey

```
public static class HKCorrelatinTypeKey {
	// properties
	public static MonoTouch.Foundation.NSString IdentifierBloodPressure { get; }
	public static MonoTouch.Foundation.NSString IdentifierFood { get; }
	public static MonoTouch.Foundation.NSString IdentifierHeartRateReading { get; }
}
```

### New Type MonoTouch.HealthKit.HKCorrelationType

```
public class HKCorrelationType : MonoTouch.HealthKit.HKSampleType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCorrelationType (MonoTouch.Foundation.NSCoder coder);
	public HKCorrelationType (MonoTouch.Foundation.NSObjectFlag t);
	public HKCorrelationType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKMovementType

```
[Serializable]
public enum HKMovementType {
	Cycling = 3,
	Other = 0,
	Running = 2,
	Walking = 1,
}
```

### New Type MonoTouch.HealthKit.HKPredicateKeyPath

```
public static class HKPredicateKeyPath {
	// properties
	public static MonoTouch.Foundation.NSString CategoryValue { get; }
	public static MonoTouch.Foundation.NSString Correlation { get; }
	public static MonoTouch.Foundation.NSString EndDate { get; }
	public static MonoTouch.Foundation.NSString Metadata { get; }
	public static MonoTouch.Foundation.NSString Quantity { get; }
	public static MonoTouch.Foundation.NSString Source { get; }
	public static MonoTouch.Foundation.NSString StartDate { get; }
	public static MonoTouch.Foundation.NSString Uuid { get; }
	public static MonoTouch.Foundation.NSString Workout { get; }
	public static MonoTouch.Foundation.NSString WorkoutDuration { get; }
	public static MonoTouch.Foundation.NSString WorkoutTotalDistance { get; }
	public static MonoTouch.Foundation.NSString WorkoutTotalEnergyBurned { get; }
	public static MonoTouch.Foundation.NSString WorkoutType { get; }
}
```

### New Type MonoTouch.HealthKit.HKQuantityTypeIdentifier

```
[Serializable]
public enum HKQuantityTypeIdentifier {
	ActiveEnergyBurned = 10,
	BasalEnergyBurned = 9,
	BloodAlcoholContent = 17,
	BloodGlucose = 14,
	BloodPressureDiastolic = 16,
	BloodPressureSystolic = 15,
	BodyFatPercentage = 1,
	BodyMass = 3,
	BodyMassIndex = 0,
	BodyTemperature = 23,
	DietaryBiotin = 48,
	DietaryCaffeine = 61,
	DietaryCalcium = 42,
	DietaryCarbohydrates = 30,
	DietaryChloride = 59,
	DietaryCholesterol = 28,
	DietaryChromium = 57,
	DietaryCopper = 55,
	DietaryEnergyConsumed = 33,
	DietaryFatMonounsaturated = 26,
	DietaryFatPolyunsaturated = 25,
	DietaryFatSaturated = 27,
	DietaryFatTotal = 24,
	DietaryFiber = 31,
	DietaryFolate = 47,
	DietaryIodine = 51,
	DietaryIron = 43,
	DietaryMagnesium = 52,
	DietaryManganese = 56,
	DietaryMolybdenum = 58,
	DietaryNiacin = 46,
	DietaryPantothenicAcid = 49,
	DietaryPhosphorus = 50,
	DietaryPotassium = 60,
	DietaryProtein = 34,
	DietaryRiboflavin = 45,
	DietarySelenium = 54,
	DietarySodium = 29,
	DietarySugar = 32,
	DietaryThiamin = 44,
	DietaryVitaminA = 35,
	DietaryVitaminB12 = 37,
	DietaryVitaminB6 = 36,
	DietaryVitaminC = 38,
	DietaryVitaminD = 39,
	DietaryVitaminE = 40,
	DietaryVitaminK = 41,
	DietaryZinc = 53,
	Distance = 8,
	FlightsClimbed = 11,
	HeartRate = 5,
	HeatFlux = 20,
	Height = 2,
	InhalerUsage = 21,
	LeanBodyMass = 4,
	NikeFuel = 12,
	NumberOfTimesFallen = 19,
	OxygenSaturation = 13,
	PeripheralPerfusionIndex = 18,
	RespiratoryRate = 22,
	RRInterval = 6,
	StepCount = 7,
}
```

### New Type MonoTouch.HealthKit.HKStoreSampleAddedCallback

```
public sealed delegate HKStoreSampleAddedCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKStoreSampleAddedCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool success, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool success, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.HealthKit.HKWorkout

```
public class HKWorkout : MonoTouch.HealthKit.HKSample, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKWorkout (MonoTouch.Foundation.NSCoder coder);
	public HKWorkout (MonoTouch.Foundation.NSObjectFlag t);
	public HKWorkout (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double Duration { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierDuration { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierTotalDistance { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierTotalEnergyBurned { get; }
	public virtual HKQuantity TotalDistance { get; }
	public virtual HKQuantity TotalEnergyBurned { get; }
	public virtual HKWorkoutActivityType WorkoutActivityType { get; }
	public virtual HKWorkoutEvent[] WorkoutEvents { get; }
	// methods
	public static HKWorkout Create (HKWorkoutActivityType workoutActivityType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate);
	public static HKWorkout Create (HKWorkoutActivityType workoutActivityType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKWorkoutEvent[] workoutEvents, HKQuantity totalEnergyBurned, HKQuantity totalDistance, MonoTouch.Foundation.NSDictionary metadata);
	public static HKWorkout Create (HKWorkoutActivityType workoutActivityType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKWorkoutEvent[] workoutEvents, HKQuantity totalEnergyBurned, HKQuantity totalDistance, HKMetadata metadata);
	public static HKWorkout Create (HKWorkoutActivityType workoutActivityType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, double duration, HKQuantity totalEnergyBurned, HKQuantity totalDistance, MonoTouch.Foundation.NSDictionary metadata);
	public static HKWorkout Create (HKWorkoutActivityType workoutActivityType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, double duration, HKQuantity totalEnergyBurned, HKQuantity totalDistance, HKMetadata metadata);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKWorkoutActivityType

```
[Serializable]
public enum HKWorkoutActivityType {
	AmericanFootball = 1,
	Archery = 2,
	AustralianFootball = 3,
	Badminton = 4,
	Baseball = 5,
	Basketball = 6,
	Bowling = 7,
	Boxing = 8,
	Climbing = 9,
	Cricket = 10,
	CrossTraining = 11,
	Curling = 12,
	Cycling = 13,
	Dance = 14,
	DanceInspiredTraining = 15,
	Elliptical = 16,
	EquestrianSports = 17,
	Fencing = 18,
	Fishing = 19,
	FunctionalStrengthTraining = 20,
	Golf = 21,
	Gymnastics = 22,
	Handball = 23,
	Hiking = 24,
	Hockey = 25,
	Hunting = 26,
	Lacrosse = 27,
	MartialArts = 28,
	MindAndBody = 29,
	MixedMetabolicCardioTraining = 30,
	PaddleSports = 31,
	Play = 32,
	PreparationAndRecovery = 33,
	Racquetball = 34,
	Rowing = 35,
	Rugby = 36,
	Running = 37,
	Sailing = 38,
	SkatingSports = 39,
	SnowSports = 40,
	Soccer = 41,
	Softball = 42,
	Squash = 43,
	StairClimbing = 44,
	SurfingSports = 45,
	Swimming = 46,
	TableTennis = 47,
	Tennis = 48,
	TrackandField = 49,
	TraditionalStrengthTraining = 50,
	Volleyball = 51,
	Walking = 52,
	WaterFitness = 53,
	WaterPolo = 54,
	WaterSports = 55,
	Wrestling = 56,
	Yoga = 57,
}
```

### New Type MonoTouch.HealthKit.HKWorkoutEvent

```
public class HKWorkoutEvent : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKWorkoutEvent (MonoTouch.Foundation.NSCoder coder);
	public HKWorkoutEvent (MonoTouch.Foundation.NSObjectFlag t);
	public HKWorkoutEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate Date { get; }
	public virtual HKWorkoutEventType Type { get; }
	// methods
	public static HKWorkoutEvent Create (HKWorkoutEventType type, MonoTouch.Foundation.NSDate date);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKWorkoutEventType

```
[Serializable]
public enum HKWorkoutEventType {
	Pause = 1,
	Resume = 2,
}
```

### New Type MonoTouch.HealthKit.HKWorkoutType

```
public class HKWorkoutType : MonoTouch.HealthKit.HKSampleType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKWorkoutType (MonoTouch.Foundation.NSCoder coder);
	public HKWorkoutType (MonoTouch.Foundation.NSObjectFlag t);
	public HKWorkoutType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```



## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMCharacteristicMetadata

Added properties:

```
public HMCharacteristicMetadataFormat Format { get; }
	public virtual MonoTouch.Foundation.NSNumber MaxLength { get; }
	public virtual MonoTouch.Foundation.NSNumber Precision { get; }
```

### Type Changed: MonoTouch.HomeKit.HMError

Removed values:

```
CannotRemoveNonBridgeAccessory = -70779,
	HomeWithSameNameExists = -70881,
	NameContainsProhibitedCharacters = -70778,
	NameDoesNotStartWithValidCharacters = -70777,
	ObjectWithSameNameExistsInHome = -70882,
	ReadonlyCharacterisitic = -70908,
	RenameWithSameName = -70880,
	WriteOnlyCharacterisitic = -70907,
```

Added values:

```
AccessoryDiscoveryFailed = -70855,
	AccessoryIsBlocked = -70851,
	AccessoryOutOfCompliance = -70846,
	AccessoryResponseError = -70853,
	AccessorySentInvalidResponse = -70863,
	ActionSetExecutionFailed = -70849,
	ActionSetExecutionInProgress = -70847,
	ActionSetExecutionPartialSuccess = -70848,
	CannotActivateTriggerTooFarInFuture = -70839,
	CannotRemoveNonBridgeAccessory = -70879,
	ClientRequestError = -70854,
	CommunicationFailure = -70859,
	DateMustBeOnSpecifiedBoundaries = -70840,
	GenericError = -70861,
	HomeAccessNotAuthorized = -70866,
	HomeWithSimilarNameExists = -70881,
	InvalidAccessory = -70856,
	InvalidAssociatedServiceType = -70850,
	InvalidMessageSize = -70857,
	InvalidStringValue = -70862,
	InvalidUserAccount = -70844,
	InvalidUserAccountSpecified = -70876,
	InvalidValueType = -70870,
	MaximumObjectLimitReached = -70864,
	MessageAuthenticationFailed = -70858,
	NameContainsProhibitedCharacters = -70878,
	NameDoesNotEndWithValidCharacters = -70852,
	NameDoesNotStartWithValidCharacters = -70877,
	NotificationAlreadyEnabled = -70843,
	ObjectWithSimilarNameExistsInHome = -70882,
	OperationNotSupported = -70865,
	ReadOnlyCharacteristic = -70908,
	ReadWriteFailure = -70836,
	ReadWritePartialSuccess = -70837,
	RecurrenceMustBeOnSpecifiedBoundaries = -70841,
	RecurrenceTooLarge = -70838,
	RecurrenceTooSmall = -70871,
	RenameWithSimilarName = -70880,
	SecurityFailure = -70860,
	StringLongerThanMaximum = -70867,
	UnableToContactUser = -70875,
	UserCanceledDelete = -70845,
	UserDeclinedAddingUser = -70874,
	UserDeclinedInvite = -70872,
	UserDeclinedRemovingUser = -70873,
	UserManagementFailed = -70842,
	ValueHigherThanMaximum = -70868,
	ValueLowerThanMinimum = -70869,
	WriteOnlyCharacteristic = -70907,
```

### Type Changed: MonoTouch.HomeKit.HMHome

Added properties:

```
public static MonoTouch.Foundation.NSString UserFailedAccessoriesKey { get; }
	public virtual MonoTouch.Foundation.NSString[] Users { get; }
```

Removed events:

```
public event System.EventHandler<HMHomeActionSetTriggerEventArgs> DidStartExecutingActionSet;
	public event System.EventHandler<HMHomeActionSetErrorEventArgs> DidStopExecutingActionSet;
```

Added event:

```
public event System.EventHandler<HMHomeErrorEventArgs> DidEncounterError;
```

Removed method:

```
public virtual void StartExecutingActionSet (HMActionSet actionSet);
```

Added methods:

```
public virtual void AddUser (MonoTouch.Foundation.NSString userID, HMHomeUserPrivilege privilege, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task AddUserAsync (MonoTouch.Foundation.NSString userID, HMHomeUserPrivilege privilege);
	public virtual void ExecuteActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task ExecuteActionSetAsync (HMActionSet actionSet);
	public virtual void GetPrivilegeForUser (MonoTouch.Foundation.NSString userID, System.Action<HMHomeUserPrivilege,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<HMHomeUserPrivilege> GetPrivilegeForUserAsync (MonoTouch.Foundation.NSString userID);
	public virtual void RemoveUser (MonoTouch.Foundation.NSString userID, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task RemoveUserAsync (MonoTouch.Foundation.NSString userID);
```

### Type Changed: MonoTouch.HomeKit.HMHomeDelegate

Removed methods:

```
public virtual void DidStartExecutingActionSet (HMHome home, HMActionSet actionSet, HMTrigger trigger);
	public virtual void DidStopExecutingActionSet (HMHome home, HMActionSet actionSet, MonoTouch.Foundation.NSError error);
```

Added method:

```
public virtual void DidEncounterError (HMHome home, MonoTouch.Foundation.NSError error, HMAccessory accessory);
```

### Type Changed: MonoTouch.HomeKit.HMHomeDelegate_Extensions

Removed methods:

```
public static void DidStartExecutingActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet, HMTrigger trigger);
	public static void DidStopExecutingActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet, MonoTouch.Foundation.NSError error);
```

Added method:

```
public static void DidEncounterError (IHMHomeDelegate This, HMHome home, MonoTouch.Foundation.NSError error, HMAccessory accessory);
```

### Type Changed: MonoTouch.HomeKit.HMTimerTrigger

Removed methods:

```
public virtual void UpdateRecurrenceCalendar (MonoTouch.Foundation.NSCalendar recurrenceCalendar, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task UpdateRecurrenceCalendarAsync (MonoTouch.Foundation.NSCalendar recurrenceCalendar);
```

### Removed Type MonoTouch.HomeKit.HMHomeActionSetErrorEventArgs ### Removed Type MonoTouch.HomeKit.HMHomeActionSetTriggerEventArgs ### New Type MonoTouch.HomeKit.HMCharacteristicMetadataFormat

```
[Serializable]
public enum HMCharacteristicMetadataFormat {
	Array = 5,
	Bool = 1,
	Float = 3,
	Int = 2,
	None = 0,
	Object = 6,
	String = 4,
}
```

### New Type MonoTouch.HomeKit.HMHomeErrorEventArgs

```
public class HMHomeErrorEventArgs : System.EventArgs {
	// constructors
	public HMHomeErrorEventArgs (MonoTouch.Foundation.NSError error, HMAccessory accessory);
	// properties
	public HMAccessory Accessory { get; set; }
	public MonoTouch.Foundation.NSError Error { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeUserPrivilege

```
[Serializable]
public enum HMHomeUserPrivilege {
	Administrator = 1,
	Regular = 0,
}
```





## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

## Namespace MonoTouch.ImageIO

### Type Changed: MonoTouch.ImageIO.CGImageProperties

Added property:

```
public static MonoTouch.Foundation.NSString GPSHPositioningError { get; }
```

### New Type MonoTouch.ImageIO.CGImagePropertyOrientation

```
[Serializable]
public enum CGImagePropertyOrientation {
	Down = 3,
	DownMirrored = 4,
	Left = 8,
	LeftMirrored = 5,
	Right = 6,
	RightMirrored = 7,
	Up = 1,
	UpMirrored = 2,
}
```

## Namespace MonoTouch.JavaScriptCore

### Type Changed: MonoTouch.JavaScriptCore.JSContext

Added property:

```
public virtual System.IntPtr JSGlobalContextRefPtr { get; }
```

Added method:

```
public static JSContext FromJSGlobalContextRef (System.IntPtr nativeJsGlobalContextRef);
```

### Type Changed: MonoTouch.JavaScriptCore.JSValue

Added property:

```
public virtual System.IntPtr JSValueRefPtr { get; }
```

Added method:

```
public static JSValue FromJSJSValueRef (System.IntPtr nativeJsValueRefvalue, JSContext context);
```

## Namespace MonoTouch.LocalAuthentication

### Type Changed: MonoTouch.LocalAuthentication.LAContext

Removed properties:

```
public virtual bool CancelButtonVisible { get; set; }
	public virtual bool FallbackButtonVisible { get; set; }
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKMapView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPNowPlayingInfo

Added field:

```
public double? DefaultPlaybackRate;
```

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

## Namespace MonoTouch.Metal

### Type Changed: MonoTouch.Metal.IMTLComputeCommandEncoder

Removed methods:

```
public virtual void ExecuteKernelWithWorkGroupSize (MTLSize workGroupSize, MTLSize workGroupCount);
	public virtual void SetLocalMemorySize (uint localMemorySize, uint index);
```

Added methods:

```
public virtual void SetThreadgroupMemoryLength (uint length, uint index);
	public virtual void SispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
```

### Type Changed: MonoTouch.Metal.IMTLComputePipelineState

Removed properties:

```
public virtual uint MaxWorkGroupSize { get; }
	public virtual uint PreferredWorkGroupFactor { get; }
```

Added properties:

```
public virtual uint MaxTotalThreadsPerThreadgroup { get; }
	public virtual uint ThreadExecutionWidth { get; }
```

### Type Changed: MonoTouch.Metal.IMTLDrawable

Added method:

```
public virtual void Present (double presentationTime);
```

### Type Changed: MonoTouch.Metal.IMTLFunction

Removed property:

```
public virtual IMTLFunctionArgument[] FunctionArguments { get; }
```

Added property:

```
public virtual MTLVertexAttribute[] VertexAttributes { get; }
```

### Type Changed: MonoTouch.Metal.IMTLTexture

Removed methods:

```
[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromPixels (System.IntPtr pixels, uint rowBytes, uint imageBytes, uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size);

	[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromSlice (uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size, System.IntPtr destination, uint rowBytes, uint imageBytes);
```

### Type Changed: MonoTouch.Metal.MTLArgumentType

Removed values:

```
LocalMemory = 2,
	ReadWriteBuffer = 1,
	ReadWriteTexture = 4,
	Sampler = 5,
	Texture = 3,
```

Added values:

```
Sampler = 3,
	Texture = 2,
	ThreadgroupMemory = 1,
```

### Type Changed: MonoTouch.Metal.MTLCommandBuffer

Added method:

```
public virtual void PresentDrawable (IMTLDrawable drawable, double presentationTime);
```

### Type Changed: MonoTouch.Metal.MTLCommandBuffer_Extensions

Added method:

```
public static void PresentDrawable (IMTLCommandBuffer This, IMTLDrawable drawable, double presentationTime);
```

### Type Changed: MonoTouch.Metal.MTLComputeCommandEncoder

Removed methods:

```
public virtual void ExecuteKernelWithWorkGroupSize (MTLSize workGroupSize, MTLSize workGroupCount);
	public virtual void SetLocalMemorySize (uint localMemorySize, uint index);
```

Added methods:

```
public virtual void SetThreadgroupMemoryLength (uint length, uint index);
	public virtual void SispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
```

### Type Changed: MonoTouch.Metal.MTLComputePipelineState

Removed properties:

```
public virtual uint MaxWorkGroupSize { get; }
	public virtual uint PreferredWorkGroupFactor { get; }
```

Added properties:

```
public virtual uint MaxTotalThreadsPerThreadgroup { get; }
	public virtual uint ThreadExecutionWidth { get; }
```

### Type Changed: MonoTouch.Metal.MTLDevice

Added methods:

```
public virtual void CreateComputePipelineState (MTLFunction computeFunction, System.Action<MTLComputePipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public virtual MTLComputePipelineState CreateComputePipelineState (MTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out MonoTouch.Foundation.NSError error);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action<IMTLRenderPipelineState,MonoTouch.Metal.MTLRenderPipelineReflection,MonoTouch.Foundation.NSError> completionHandler);
	public virtual MTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.Metal.MTLDevice_Extensions

Added methods:

```
public static MTLComputePipelineState CreateComputePipelineState (IMTLDevice This, MTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out MonoTouch.Foundation.NSError error);
	public static void CreateComputePipelineState (IMTLDevice This, MTLFunction computeFunction, System.Action<MTLComputePipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public static MTLRenderPipelineState CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out MonoTouch.Foundation.NSError error);
	public static void CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action<IMTLRenderPipelineState,MonoTouch.Metal.MTLRenderPipelineReflection,MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.Metal.MTLDrawable

Added method:

```
public virtual void Present (double presentationTime);
```

### Type Changed: MonoTouch.Metal.MTLFunction

Removed property:

```
public virtual IMTLFunctionArgument[] FunctionArguments { get; }
```

Added property:

```
public virtual MTLVertexAttribute[] VertexAttributes { get; }
```

### Type Changed: MonoTouch.Metal.MTLPixelFormat

Removed values:

```
A2BGR10Uint = 91,
	A2BGR10Unorm = 90,
	B10GR11Float = 92,
	k422_BGRG = 241,
	k422_GBGR = 240,
	RGB565Unorm = 40,
	RGB5A1Unorm = 41,
	RGBA4Unorm = 42,
	SE5BGR9Float = 93,
```

Added values:

```
A1BGR5Unorm = 41,
	ABGR4Unorm = 42,
	B5G6R5Unorm = 40,
	BGRG422 = 241,
	GBGR422 = 240,
	RG11B10Float = 92,
	RGB10A2Uint = 91,
	RGB10A2Unorm = 90,
	RGB9E5Float = 93,
```

### Type Changed: MonoTouch.Metal.MTLRenderPassAttachmentDescriptor

Removed properties:

```
public virtual MTLClearValue ClearValue { get; set; }
	public virtual IMTLTexture ResolveTexture { get; set; }
	public virtual IMTLTexture Texture { get; set; }
```

Added properties:

```
public virtual MTLTexture ResolveTexture { get; set; }
	public virtual MTLTexture Texture { get; set; }
```

### Type Changed: MonoTouch.Metal.MTLRenderPassDescriptor

Removed properties:

```
public virtual MTLRenderPassAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLRenderPassAttachmentDescriptor DepthAttachment { get; set; }
	public virtual MTLRenderPassAttachmentDescriptor StencilAttachment { get; set; }
```

Added properties:

```
public virtual MTLRenderPassColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLRenderPassDepthAttachmentDescriptor DepthAttachment { get; set; }
	public virtual MTLRenderPassStencilAttachmentDescriptor StencilAttachment { get; set; }
```

### Type Changed: MonoTouch.Metal.MTLRenderPipelineDescriptor

Removed properties:

```
public virtual MTLRenderPipelineAttachmentDescriptorArray ColorAttachments { get; }
	public virtual bool DepthWriteEnabled { get; set; }
	public virtual float SampleCoverage { get; set; }
	public virtual uint SampleMask { get; set; }
	public virtual bool StencilWriteEnabled { get; set; }
	public virtual bool VisibilityResultEnabled { get; set; }
```

Added properties:

```
public virtual MTLRenderPipelineColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual bool RasterizationEnabled { get; set; }
```

### Type Changed: MonoTouch.Metal.MTLTexture

Removed methods:

```
[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromPixels (System.IntPtr pixels, uint rowBytes, uint imageBytes, uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size);

	[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromSlice (uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size, System.IntPtr destination, uint rowBytes, uint imageBytes);
	public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, MTLTextureRegion region, uint level);
	public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLTextureRegion region, uint level, uint slice);
	public virtual void ReplaceRegion (MTLTextureRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public virtual void ReplaceRegion (MTLTextureRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
```

Added methods:

```
public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLRegion region, uint level, uint slice);
	public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, MTLRegion region, uint level);
	public virtual void ReplaceRegion (MTLRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public virtual void ReplaceRegion (MTLRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
```

### Type Changed: MonoTouch.Metal.MTLTexture_Extensions

Removed methods:

```
public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLTextureRegion region, uint level, uint slice);
	public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, MTLTextureRegion region, uint level);
	public static void ReplaceRegion (IMTLTexture This, MTLTextureRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public static void ReplaceRegion (IMTLTexture This, MTLTextureRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
```

Added methods:

```
public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLRegion region, uint level, uint slice);
	public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, MTLRegion region, uint level);
	public static void ReplaceRegion (IMTLTexture This, MTLRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public static void ReplaceRegion (IMTLTexture This, MTLRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
```

### Type Changed: MonoTouch.Metal.MTLVertexDescriptor

Added properties:

```
public virtual MTLVertexAttributeDescriptorArray Attributes { get; }
	public virtual MTLVertexBufferLayoutDescriptorArray Layouts { get; }
```

Removed methods:

```
public virtual uint GetOffset (uint attributeIndex);
	public virtual MTLVertexStepFunction GetStepFunction (uint vertexBufferIndex);
	public virtual uint GetStepRate (uint vertexBufferIndex);
	public virtual uint GetStride (uint vertexBufferIndex);
	public virtual uint GetVertexBufferIndex (uint attributeIndex);
	public virtual MTLVertexFormat GetVertexFormat (uint attributeIndex);
	public virtual void SetStride (uint stride, uint vertexBufferIndex);
	public virtual void SetStride (uint stride, MTLVertexStepFunction stepFunction, uint instanceStepRate, uint vertexBufferIndex);
	public virtual void SetVertexFormat (MTLVertexFormat vertexFormat, uint offset, uint vertexBufferIndex, uint attributeIndex);
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.Metal.MTLVertexFormat

Removed values:

```
Int2101010Normalized = 40,
	UInt2101010Normalized = 41,
```

Added values:

```
Int1010102Normalized = 40,
	UInt1010102Normalized = 41,
```

### Removed Type MonoTouch.Metal.IMTLFunctionArgument ### Removed Type MonoTouch.Metal.MTLFunctionArgument ### Removed Type MonoTouch.Metal.MTLFunctionArgument_Extensions ### Removed Type MonoTouch.Metal.MTLRenderPassAttachmentDescriptorArray ### Removed Type MonoTouch.Metal.MTLRenderPipelineAttachmentDescriptor ### Removed Type MonoTouch.Metal.MTLRenderPipelineAttachmentDescriptorArray ### Removed Type MonoTouch.Metal.MTLTextureRegion ### New Type MonoTouch.Metal.MTLArgument

```
public class MTLArgument : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLArgument ();
	public MTLArgument (MonoTouch.Foundation.NSCoder coder);
	public MTLArgument (MonoTouch.Foundation.NSObjectFlag t);
	public MTLArgument (System.IntPtr handle);
	// properties
	public virtual MTLArgumentAccess Access { get; }
	public virtual bool Active { get; }
	public virtual uint BufferAlignment { get; }
	public virtual uint BufferDataSize { get; }
	public virtual MTLDataType BufferDataType { get; }
	public virtual MTLStructType BufferStructType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint Index { get; }
	public virtual string Name { get; }
	public virtual MTLDataType TextureDataType { get; }
	public virtual MTLTextureType TextureType { get; }
	public virtual uint ThreadgroupMemoryAlignment { get; }
	public virtual uint ThreadgroupMemoryDataSize { get; }
	public virtual MTLArgumentType Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLArgumentAccess

```
[Serializable]
public enum MTLArgumentAccess {
	ReadOnly = 0,
	ReadWrite = 1,
	WriteOnly = 2,
}
```

### New Type MonoTouch.Metal.MTLArrayType

```
public class MTLArrayType : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLArrayType ();
	public MTLArrayType (MonoTouch.Foundation.NSCoder coder);
	public MTLArrayType (MonoTouch.Foundation.NSObjectFlag t);
	public MTLArrayType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLDataType ElementType { get; }
	public virtual uint Length { get; }
	public virtual uint Stride { get; }
	// methods
	public virtual MTLArrayType ElementArrayType ();
	public virtual MTLStructType ElementStructType ();
}
```

### New Type MonoTouch.Metal.MTLComputePipelineReflection

```
public class MTLComputePipelineReflection : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLComputePipelineReflection ();
	public MTLComputePipelineReflection (MonoTouch.Foundation.NSCoder coder);
	public MTLComputePipelineReflection (MonoTouch.Foundation.NSObjectFlag t);
	public MTLComputePipelineReflection (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSObject[] Arguments { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLDataType

```
[Serializable]
public enum MTLDataType {
	Array = 2,
	Bool = 53,
	Bool2 = 54,
	Bool3 = 55,
	Bool4 = 56,
	Char = 45,
	Char2 = 46,
	Char3 = 47,
	Char4 = 48,
	Float = 3,
	Float2 = 4,
	Float2x2 = 7,
	Float2x3 = 8,
	Float2x4 = 9,
	Float3 = 5,
	Float3x2 = 10,
	Float3x3 = 11,
	Float3x4 = 12,
	Float4 = 6,
	Float4x2 = 13,
	Float4x3 = 14,
	Float4x4 = 15,
	Half = 16,
	Half2 = 17,
	Half2x2 = 20,
	Half2x3 = 21,
	Half2x4 = 22,
	Half3 = 18,
	Half3x2 = 23,
	Half3x3 = 24,
	Half3x4 = 25,
	Half4 = 19,
	Half4x2 = 26,
	Half4x3 = 27,
	Half4x4 = 28,
	Int = 29,
	Int2 = 30,
	Int3 = 31,
	Int4 = 32,
	None = 0,
	Short = 37,
	Short2 = 38,
	Short3 = 39,
	Short4 = 40,
	Struct = 1,
	UChar = 49,
	UChar2 = 50,
	UChar3 = 51,
	UChar4 = 52,
	UInt = 33,
	UInt2 = 34,
	UInt3 = 35,
	UInt4 = 36,
	UShort = 41,
	UShort2 = 42,
	UShort3 = 43,
	UShort4 = 44,
}
```

### New Type MonoTouch.Metal.MTLPipelineOption

```
[Serializable]
[Flags]
public enum MTLPipelineOption {
	ArgumentInfo = 1,
	BufferTypeInfo = 2,
	None = 0,
}
```

### New Type MonoTouch.Metal.MTLRegion

```
public struct MTLRegion {
	// constructors
	public MTLRegion (MTLOrigin origin, MTLSize size);
	// fields
	public MTLOrigin Origin;
	public MTLSize Size;
	// methods
	public static MTLRegion Create1D (uint x, uint width);
	public static MTLRegion Create2D (uint x, uint y, uint width, uint height);
	public static MTLRegion Create3D (uint x, uint y, uint z, uint width, uint height, uint depth);
}
```

### New Type MonoTouch.Metal.MTLRenderPassColorAttachmentDescriptor

```
public class MTLRenderPassColorAttachmentDescriptor : MonoTouch.Metal.MTLRenderPassAttachmentDescriptor, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassColorAttachmentDescriptor ();
	public MTLRenderPassColorAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassColorAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassColorAttachmentDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLClearColor ClearColor { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPassColorAttachmentDescriptorArray

```
public class MTLRenderPassColorAttachmentDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassColorAttachmentDescriptorArray ();
	public MTLRenderPassColorAttachmentDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassColorAttachmentDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassColorAttachmentDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MTLRenderPassColorAttachmentDescriptor Item { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPassDepthAttachmentDescriptor

```
public class MTLRenderPassDepthAttachmentDescriptor : MonoTouch.Metal.MTLRenderPassAttachmentDescriptor, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassDepthAttachmentDescriptor ();
	public MTLRenderPassDepthAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassDepthAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassDepthAttachmentDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double ClearDepth { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPassStencilAttachmentDescriptor

```
public class MTLRenderPassStencilAttachmentDescriptor : MonoTouch.Metal.MTLRenderPassAttachmentDescriptor, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassStencilAttachmentDescriptor ();
	public MTLRenderPassStencilAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassStencilAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassStencilAttachmentDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint ClearStencil { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineColorAttachmentDescriptor

```
public class MTLRenderPipelineColorAttachmentDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineColorAttachmentDescriptor ();
	public MTLRenderPipelineColorAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineColorAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineColorAttachmentDescriptor (System.IntPtr handle);
	// properties
	public virtual MTLBlendOperation AlphaBlendOperation { get; set; }
	public virtual bool BlendingEnabled { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLBlendFactor DestinationAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor DestinationRgbBlendFactor { get; set; }
	public virtual MTLPixelFormat PixelFormat { get; set; }
	public virtual MTLBlendOperation RgbBlendOperation { get; set; }
	public virtual MTLBlendFactor SourceAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor SourceRgbBlendFactor { get; set; }
	public virtual MTLColorWriteMask WriteMask { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineColorAttachmentDescriptorArray

```
public class MTLRenderPipelineColorAttachmentDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineColorAttachmentDescriptorArray ();
	public MTLRenderPipelineColorAttachmentDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineColorAttachmentDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineColorAttachmentDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineReflection

```
public class MTLRenderPipelineReflection : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineReflection ();
	public MTLRenderPipelineReflection (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineReflection (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineReflection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject[] FragmentArguments { get; }
	public virtual MonoTouch.Foundation.NSObject[] VertexArguments { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLStructMember

```
public class MTLStructMember : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLStructMember ();
	public MTLStructMember (MonoTouch.Foundation.NSCoder coder);
	public MTLStructMember (MonoTouch.Foundation.NSObjectFlag t);
	public MTLStructMember (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLDataType DataType { get; }
	public virtual string Name { get; }
	public virtual uint Offset { get; }
	// methods
	public virtual MTLArrayType ArrayType ();
	public virtual MTLStructType StructType ();
}
```

### New Type MonoTouch.Metal.MTLStructType

```
public class MTLStructType : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLStructType ();
	public MTLStructType (MonoTouch.Foundation.NSCoder coder);
	public MTLStructType (MonoTouch.Foundation.NSObjectFlag t);
	public MTLStructType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLStructMember[] Members { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MTLStructMember Lookup (string name);
}
```

### New Type MonoTouch.Metal.MTLVertexAttribute

```
public class MTLVertexAttribute : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexAttribute ();
	public MTLVertexAttribute (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexAttribute (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexAttribute (System.IntPtr handle);
	// properties
	public virtual bool Active { get; }
	public virtual uint AttributeIndex { get; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.Metal.MTLVertexAttributeDescriptor

```
public class MTLVertexAttributeDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexAttributeDescriptor ();
	public MTLVertexAttributeDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexAttributeDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexAttributeDescriptor (System.IntPtr handle);
	// properties
	public virtual uint BufferIndex { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLVertexFormat Format { get; set; }
	public virtual uint Offset { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLVertexAttributeDescriptorArray

```
public class MTLVertexAttributeDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexAttributeDescriptorArray ();
	public MTLVertexAttributeDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexAttributeDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexAttributeDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MTLVertexAttributeDescriptor Item { get; set; }
}
```

### New Type MonoTouch.Metal.MTLVertexBufferLayoutDescriptor

```
public class MTLVertexBufferLayoutDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexBufferLayoutDescriptor ();
	public MTLVertexBufferLayoutDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexBufferLayoutDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexBufferLayoutDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLVertexStepFunction StepFunction { get; set; }
	public virtual uint StepRate { get; set; }
	public virtual uint Stride { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLVertexBufferLayoutDescriptorArray

```
public class MTLVertexBufferLayoutDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexBufferLayoutDescriptorArray ();
	public MTLVertexBufferLayoutDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexBufferLayoutDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexBufferLayoutDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MTLVertexBufferLayoutDescriptor Item { get; set; }
}
```





## Namespace MonoTouch.Photos



### Type Changed: MonoTouch.Photos.PHAsset

Removed property:

```
public virtual PHAssetSource AssetSource { get; }
```

### Type Changed: MonoTouch.Photos.PHAssetChangeRequest

Removed method:

```
public virtual void RevertAssetToOriginal ();
```

Added method:

```
public virtual void RevertAssetContentToOriginal ();
```

### Type Changed: MonoTouch.Photos.PHAssetCollectionSubtype

Removed values:

```
AlbumImported = 5,
	AlbumMyPhotoStream = 100,
	AlbumSynced = 3,
```

Added values:

```
AlbumImported = 6,
	AlbumSyncedAlbum = 5,
	AlbumSyncedEvent = 3,
```

### Type Changed: MonoTouch.Photos.PHAssetEditOperation

Removed value:

```
Properties = 4,
```

Added value:

```
Properties = 3,
```

### Type Changed: MonoTouch.Photos.PHAssetImageProgressHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (bool degraded, double progress, MonoTouch.Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);
	public virtual void Invoke (bool degraded, double progress, MonoTouch.Foundation.NSError error, out bool stop);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void Invoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info);
```

### Type Changed: MonoTouch.Photos.PHAssetVideoProgressHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);
	public virtual void Invoke (double progress, MonoTouch.Foundation.NSError error, out bool stop);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void Invoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info);
```

### Type Changed: MonoTouch.Photos.PHCollectionEditOperation

Removed values:

```
AddContent = 4,
	CreateContent = 8,
	Delete = 32,
	RearrangeContent = 16,
	Rename = 64,
```

Added values:

```
AddContent = 3,
	CreateContent = 4,
	Delete = 6,
	RearrangeContent = 5,
	Rename = 7,
```

### Type Changed: MonoTouch.Photos.PHCollectionList

Added property:

```
public virtual PHCollectionListSubtype CollectionListSubtype { get; }
```

Removed methods:

```
public static PHFetchResult FetchCollectionList (PHCollection collection, PHFetchOptions options);
	public static PHFetchResult FetchCollectionLists (PHCollectionListType collectionListType, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListType momentListType, PHAssetCollection moment, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListType momentListType, PHFetchOptions options);
```

Added methods:

```
public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);
	public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);
```

### Type Changed: MonoTouch.Photos.PHCollectionListType

Removed values:

```
Folder = 3,
	MomentCluster = 1,
	MomentYear = 2,
```

Added values:

```
Folder = 2,
	MomentList = 1,
	SmartFolder = 3,
```

### Type Changed: MonoTouch.Photos.PHContentEditingInput

Removed property:

```
public virtual int FullSizeImageOrientation { get; }
```

Added property:

```
public virtual MonoTouch.CoreImage.CIImageOrientation FullSizeImageOrientation { get; }
```

### Type Changed: MonoTouch.Photos.PHContentEditingOutput

Added constructor:

```
public PHContentEditingOutput (PHObjectPlaceholder placeholderForCreatedAsset);
```

### Type Changed: MonoTouch.Photos.PHFetchOptions

Added property:

```
public virtual bool IncludeHiddenAssets { get; set; }
```

### Type Changed: MonoTouch.Photos.PHImageKeys

Removed properties:

```
public static MonoTouch.Foundation.NSString FileData { get; }
	public static MonoTouch.Foundation.NSString FileOrientation { get; }
	public static MonoTouch.Foundation.NSString FileUti { get; }
```

Added property:

```
public static MonoTouch.Foundation.NSString ResultRequestID { get; }
```

### Type Changed: MonoTouch.Photos.PHImageManager

Removed property:

```
public static PHImageManager GetDefaultManager { get; }
```

Added property:

```
public static PHImageManager DefaultManager { get; }
```

Removed methods:

```
public virtual void CancelImageRequest (uint requestID);
	public virtual uint RequestAvAsset (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestAvAssetHandler resultHandler);
	public virtual uint RequestExportSession (PHAsset asset, PHVideoRequestOptions options, string exportPreset, PHImageManagerRequestExportHandler resultHandler);
	public virtual uint RequestImageForAsset (PHAsset asset, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);
	public virtual uint RequestPlayerItem (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestPlayerHandler resultHandler);
```

Added methods:

```
public virtual void CancelImageRequest (int requestID);
	public virtual int RequestAvAsset (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestAvAssetHandler resultHandler);
	public virtual int RequestExportSession (PHAsset asset, PHVideoRequestOptions options, string exportPreset, PHImageManagerRequestExportHandler resultHandler);
	public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);
	public virtual int RequestImageForAsset (PHAsset asset, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);
	public virtual int RequestPlayerItem (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestPlayerHandler resultHandler);
```

### Type Changed: MonoTouch.Photos.PHImageRequestOptions

Removed property:

```
public virtual PHImageRequestOptionsLoadingMode LoadingMode { get; set; }
```

### Type Changed: MonoTouch.Photos.PHPhotoLibrary

Removed property:

```
public static PHPhotoLibrary GetSharedPhotoLibrary { get; }
```

Added properties:

```
public static PHAuthorizationStatus AuthorizationStatus { get; }
	public static PHPhotoLibrary SharedPhotoLibrary { get; }
```

Added methods:

```
public object RegisterChangeObserver (System.Action<PHChange> changeObserver);
	public static void RequestAuthorization (System.Action<PHAuthorizationStatus> handler);
	public void UnregisterChangeObserver (object registeredToken);
```

### Removed Type MonoTouch.Photos.PHAssetSource ### Removed Type MonoTouch.Photos.PHImageRequestOptionsLoadingMode ### New Type MonoTouch.Photos.PHAuthorizationStatus

```
[Serializable]
public enum PHAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
```

### New Type MonoTouch.Photos.PHCollectionListSubtype

```
[Serializable]
public enum PHCollectionListSubtype {
	Any = 2147483647,
	MomentListCluster = 1,
	MomentListYear = 2,
	RegularFolder = 100,
	SmartFolderEvents = 200,
	SmartFolderFaces = 201,
}
```

### New Type MonoTouch.Photos.PHImageDataHandler

```
public sealed delegate PHImageDataHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageDataHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSString dataUti, MonoTouch.UIKit.UIImageOrientation orientation, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSString dataUti, MonoTouch.UIKit.UIImageOrientation orientation, MonoTouch.Foundation.NSDictionary info);
}
```





## Namespace MonoTouch.SceneKit



### Type Changed: MonoTouch.SceneKit.ISCNTechniqueSupport

Added property:

```
public virtual SCNTechnique Technique { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNAction

Removed methods:

```
public static SCNAction JavaScriptAction (string script, double seconds);
	public static SCNAction Run (System.Action handler);
	public static SCNAction Run (System.Action handler, MonoTouch.CoreFoundation.DispatchQueue queue);
```

Added methods:

```
public static SCNAction FromJavascript (string script, double seconds);
	public static SCNAction Run (System.Action<SCNNode> handler, MonoTouch.CoreFoundation.DispatchQueue queue);
	public static SCNAction Run (System.Action<SCNNode> handler);
	public virtual void SetTimingFunction (System.Action<float> timingFunction);
```

### Type Changed: MonoTouch.SceneKit.SCNCamera

Added properties:

```
public virtual float Aperture { get; set; }
	public virtual bool AutomaticallyAdjustsZRange { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float FocalBlurRadius { get; set; }
	public virtual float FocalDistance { get; set; }
	public virtual float FocalSize { get; set; }
	public virtual double OrthographicScale { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNLight

Added property:

```
public virtual uint CategoryBitMask { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNMaterial

Added properties:

```
public virtual float FresnelExponent { get; set; }
	public virtual bool ReadsFromDepthBuffer { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNNode

Removed property:

```
public virtual SCNVector4 Orientation { get; set; }
```

Added property:

```
public virtual SCNQuaternion Orientation { get; set; }
```

Added method:

```
public void AddNodes (SCNNode[] nodes);
```

### Type Changed: MonoTouch.SceneKit.SCNParticleSystem

Added properties:

```
public virtual float ParticleCharge { get; set; }
	public virtual float ParticleChargeVariation { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsBehavior

Removed constructor:

```
public SCNPhysicsBehavior ();
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsBody

Added property:

```
public virtual float Charge { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsField

Removed methods:

```
public static SCNPhysicsField CreateNoiseField (float smoothness, float scale, float speed);
	public static SCNPhysicsField CreateTurbulenceField ();
```

Added methods:

```
public static SCNPhysicsField CreateNoiseField (float smoothness, float speed);
	public static SCNPhysicsField CreateTurbulenceField (float smoothness, float speed);
```

### Type Changed: MonoTouch.SceneKit.SCNPlane

Added properties:

```
public virtual float CornerRadius { get; set; }
	public virtual int CornerSegmentCount { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNRenderer

Added property:

```
public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNScene

Added properties:

```
public static MonoTouch.Foundation.NSString EndTimeAttributeKey { get; }
	public static MonoTouch.Foundation.NSString FrameRateAttributeKey { get; }
	public static MonoTouch.Foundation.NSString StartTimeAttributeKey { get; }
	public static MonoTouch.Foundation.NSString UpAxisAttributeKey { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNSceneRenderer

Added property:

```
public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNSceneSource

Added method:

```
public virtual MonoTouch.Foundation.NSObject[] EntriesPassingTest (SCNSceneSourceFilter predicate);
```

### Type Changed: MonoTouch.SceneKit.SCNShadowMode

Removed value:

```
Projected = 2,
```

Added value:

```
Modulated = 2,
```

### Type Changed: MonoTouch.SceneKit.SCNTechnique

Removed methods:

```
public static SCNTechnique From (MonoTouch.Foundation.NSObject[] techniques);
	public static SCNTechnique From (MonoTouch.Foundation.NSDictionary dictionary);
```

Added methods:

```
public static SCNTechnique Create (MonoTouch.Foundation.NSDictionary dictionary);
	public static SCNTechnique Create (SCNTechnique[] techniques);
```

### Type Changed: MonoTouch.SceneKit.SCNVector3

Added constructor:

```
public SCNVector3 (OpenTK.Vector3 v);
```

### Type Changed: MonoTouch.SceneKit.SCNVector4

Removed constructor:

```
public SCNVector4 (OpenTK.Vector4 source);
```

Added constructors:

```
public SCNVector4 (OpenTK.Vector3 v);
	public SCNVector4 (OpenTK.Vector4 v);
```

### Type Changed: MonoTouch.SceneKit.SCNView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

Removed property:

```
public virtual MonoTouch.UIKit.UIColor BackgroundColor { get; set; }
```

Added properties:

```
public virtual SCNAntialiasingMode AntialiasingMode { get; set; }
	public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual int PreferredFramesPerSecond { get; set; }
```

### New Type MonoTouch.SceneKit.SCNAntialiasingMode

```
[Serializable]
public enum SCNAntialiasingMode {
	Multisampling2X = 1,
	Multisampling4X = 2,
	None = 0,
}
```

### New Type MonoTouch.SceneKit.SCNQuaternion

```
[Serializable]
public struct SCNQuaternion, System.IEquatable<SCNQuaternion> {
	// constructors
	public SCNQuaternion (SCNVector3 v, float w);
	public SCNQuaternion (float x, float y, float z, float w);
	public SCNQuaternion (ref OpenTK.Matrix3 matrix);
	public SCNQuaternion (OpenTK.Quaternion openTkQuaternion);
	// fields
	public static SCNQuaternion Identity;
	// properties
	public float Length { get; }
	public float LengthSquared { get; }
	public float W { get; set; }
	public float X { get; set; }
	public SCNVector3 Xyz { get; set; }

	[Obsolete ("Use Xyz property instead.")]
	public SCNVector3 XYZ { get; set; }
	public float Y { get; set; }
	public float Z { get; set; }
	// methods
	public static void Add (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Add (SCNQuaternion left, SCNQuaternion right);
	public static void Conjugate (ref SCNQuaternion q, out SCNQuaternion result);
	public static SCNQuaternion Conjugate (SCNQuaternion q);
	public void Conjugate ();
	public virtual bool Equals (SCNQuaternion other);
	public override bool Equals (object other);
	public static SCNQuaternion FromAxisAngle (SCNVector3 axis, float angle);
	public override int GetHashCode ();
	public static SCNQuaternion Invert (SCNQuaternion q);
	public static void Invert (ref SCNQuaternion q, out SCNQuaternion result);

	[Obsolete ("Use Multiply instead.")]
	public static SCNQuaternion Mult (SCNQuaternion left, SCNQuaternion right);

	[Obsolete ("Use Multiply instead.")]
	public static void Mult (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static void Multiply (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Multiply (SCNQuaternion quaternion, float scale);

	[Obsolete ("Use the overload without the ref float scale")]
	public static void Multiply (ref SCNQuaternion quaternion, ref float scale, out SCNQuaternion result);
	public static SCNQuaternion Multiply (SCNQuaternion left, SCNQuaternion right);
	public static void Multiply (ref SCNQuaternion quaternion, float scale, out SCNQuaternion result);
	public static SCNQuaternion Normalize (SCNQuaternion q);
	public static void Normalize (ref SCNQuaternion q, out SCNQuaternion result);
	public void Normalize ();
	public static SCNQuaternion op_Addition (SCNQuaternion left, SCNQuaternion right);
	public static bool op_Equality (SCNQuaternion left, SCNQuaternion right);
	public static bool op_Inequality (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion op_Multiply (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion op_Multiply (SCNQuaternion quaternion, float scale);
	public static SCNQuaternion op_Multiply (float scale, SCNQuaternion quaternion);
	public static SCNQuaternion op_Subtraction (SCNQuaternion left, SCNQuaternion right);
	public static SCNQuaternion Slerp (SCNQuaternion q1, SCNQuaternion q2, float blend);
	public static void Sub (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);
	public static SCNQuaternion Sub (SCNQuaternion left, SCNQuaternion right);
	public SCNVector4 ToAxisAngle ();
	public void ToAxisAngle (out SCNVector3 axis, out float angle);
	public override string ToString ();
}
```

### New Type MonoTouch.SceneKit.SCNSceneSourceFilter

```
public sealed delegate SCNSceneSourceFilter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneSourceFilter (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSObject entry, MonoTouch.Foundation.NSString identifier, ref bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual bool Invoke (MonoTouch.Foundation.NSObject entry, MonoTouch.Foundation.NSString identifier, ref bool stop);
}
```

## Namespace MonoTouch.SpriteKit



### Type Changed: MonoTouch.SpriteKit.SK3DNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKAction

Added methods:

```
public static SKAction Falloff (float to, double duration);
	public virtual void SetTimingFunction (SKActionTimingFunction timingFunction);
```

### Type Changed: MonoTouch.SpriteKit.SKCropNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKEffectNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKEmitterNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKFieldNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Removed method:

```
public static SKFieldNode CreeateElectricField ();
```

Added method:

```
public static SKFieldNode CreateElectricField ();
```

### Type Changed: MonoTouch.SpriteKit.SKLabelNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKLightNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added methods:

```
public void Add (SKNode node);
	public void AddNodes (SKNode[] nodes);
	public static SKNode FromFile (string file);
	public virtual System.Collections.Generic.IEnumerator<SKNode> GetEnumerator ();
	public virtual SKNode GetObjectsMatching (string nameExpression);
```

### Type Changed: MonoTouch.SpriteKit.SKScene

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Removed method:

```
public virtual void DidApplyConstriants ();
```

Added method:

```
public virtual void DidApplyConstraints ();
```

### Type Changed: MonoTouch.SpriteKit.SKShader

Removed method:

```
public virtual bool IsValid ();
```

### Type Changed: MonoTouch.SpriteKit.SKShapeNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public virtual MonoTouch.CoreGraphics.CGLineCap LineCap { get; set; }
	public virtual MonoTouch.CoreGraphics.CGLineJoin LineJoin { get; set; }
	public virtual float LineLength { get; }
	public virtual float MiterLimit { get; set; }
```

### Type Changed: MonoTouch.SpriteKit.SKSpriteNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKUniform

Added constructor:

```
public SKUniform (string name, OpenTK.Matrix2 value);
```

Added property:

```
public virtual OpenTK.Matrix2 FloatMatrix2Value { get; set; }
```

### Type Changed: MonoTouch.SpriteKit.SKVideoNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### New Type MonoTouch.SpriteKit.SKActionTimingFunction

```
public sealed delegate SKActionTimingFunction : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKActionTimingFunction (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (float time, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (float time);
}
```

## Namespace MonoTouch.UIKit



### Type Changed: MonoTouch.UIKit.IUITextDocumentProxy

Added method:

```
public virtual void AdjustTextPositionByCharacterOffset (int offset);
```

### Type Changed: MonoTouch.UIKit.NSLayoutAttribute

Added values:

```
BottomMargin = 16,
	CenterXWithinMargins = 19,
	CenterYWithinMargins = 20,
	LeadingMargin = 17,
	LeftMargin = 13,
	RightMargin = 14,
	TopMargin = 15,
	TrailingMargin = 18,
```

### Type Changed: MonoTouch.UIKit.NSLayoutConstraint

Added property:

```
public virtual bool Active { get; set; }
```

Added methods:

```
public static void ActivateConstraints (NSLayoutConstraint[] constraints);
	public static void DeactivateConstraints (NSLayoutConstraint[] constraints);
```

### Type Changed: MonoTouch.UIKit.NSTextStorage

Added interface:

```
MonoTouch.Foundation.INSSecureCoding
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIApplication

Added properties:

```
public static MonoTouch.Foundation.NSString LaunchOptionsUserActivityDictionaryKey { get; }
	public static MonoTouch.Foundation.NSString LaunchOptionsUserActivityTypeKey { get; }
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added method:

```
public virtual bool ShouldAllowExtensionPointIdentifier (UIApplication application, MonoTouch.Foundation.NSString extensionPointIdentifier);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Added method:

```
public static bool ShouldAllowExtensionPointIdentifier (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSString extensionPointIdentifier);
```

### Type Changed: MonoTouch.UIKit.UIBarMetrics

Removed value:

```
Condensed = 2,
```

### Type Changed: MonoTouch.UIKit.UIButton

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIColor

Added property:

```
public virtual MonoTouch.CoreImage.CIColor CIColor { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.UIKit.UIControl

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIImage

Removed method:

```
public static UIImage ImageBundle (string name, MonoTouch.Foundation.NSBundle bundle, UITraitCollection traitCollection);
```

Added method:

```
public static UIImage FromBundle (string name, MonoTouch.Foundation.NSBundle bundle, UITraitCollection traitCollection);
```

### Type Changed: MonoTouch.UIKit.UIImageView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIInputView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIInputViewController

Added property:

```
public virtual string PrimaryLanguage { get; set; }
```

### Type Changed: MonoTouch.UIKit.UILabel

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UINavigationController

Removed properties:

```
public virtual UIPanGestureRecognizer BarCondenseGestureRecognizer { get; }
	public virtual UITapGestureRecognizer BarHideGestureRecognizer { get; }
	public virtual bool CondensesBarsOnSwipe { get; set; }
	public virtual bool CondensesBarsWhenKeyboardAppears { get; set; }
	public virtual bool NavigationBarCondensed { get; set; }
```

Added properties:

```
public virtual UIPanGestureRecognizer BarHideOnSwipeGestureRecognizer { get; }
	public virtual UITapGestureRecognizer BarHideOnTapGestureRecognizer { get; }
	public virtual bool HidesBarsOnSwipe { get; set; }
	public virtual bool HidesBarsWhenKeyboardAppears { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIPresentationController

Removed constructor:

```
public UIPresentationController (UIViewController presentingViewController, UIViewController presentedViewController);
```

Added constructor:

```
public UIPresentationController (UIViewController presentedViewController, UIViewController presentingViewController);
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIScreen

Added properties:

```
public virtual IUICoordinateSpace CoordinateSpace { get; }
	public virtual IUICoordinateSpace FixedCoordinateSpace { get; }
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UISlider

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIStepper

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UISwitch

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITabBar

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITableView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITextDocumentProxy

Added method:

```
public virtual void AdjustTextPositionByCharacterOffset (int offset);
```

### Type Changed: MonoTouch.UIKit.UITextField

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITextView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UITraitCollection

Removed method:

```
public static UITraitCollection FromTraitsFromCollections (MonoTouch.Foundation.NSObject[] traitCollections);
```

Added method:

```
public static UITraitCollection FromTraitsFromCollections (UITraitCollection[] traitCollections);
```

### Type Changed: MonoTouch.UIKit.UIView

Added interface:

```
IUICoordinateSpace
```

Added methods:

```
public virtual System.Drawing.PointF ConvertPointFromCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.PointF ConvertPointToCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectFromCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectToCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext_Extensions

Removed methods:

```
public static UIViewController GetTransitionViewController (IUIViewControllerTransitionCoordinatorContext This, UITransitionViewControllerKind kind);
	public static UIViewController GetTransitionViewControllerForKey (IUIViewControllerTransitionCoordinatorContext This, MonoTouch.Foundation.NSString key);
```

Added methods:

```
public static UIView GetTransitionViewController (IUIViewControllerTransitionCoordinatorContext This, UITransitionViewControllerKind kind);
	public static UIView GetTransitionViewControllerForKey (IUIViewControllerTransitionCoordinatorContext This, MonoTouch.Foundation.NSString key);
```

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added interface:

```
IUICoordinateSpace
```

### Type Changed: MonoTouch.UIKit.UIWindow

Added interface:

```
IUICoordinateSpace
```

### New Type MonoTouch.UIKit.IUICoordinateSpace

```
public interface IUICoordinateSpace : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual System.Drawing.RectangleF Bounds { get; }
	// methods
	public virtual System.Drawing.PointF ConvertPointFromCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.PointF ConvertPointToCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectFromCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectToCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
}
```

### New Type MonoTouch.UIKit.UICoordinateSpace

```
public abstract class UICoordinateSpace : MonoTouch.Foundation.NSObject, IUICoordinateSpace, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UICoordinateSpace ();
	public UICoordinateSpace (MonoTouch.Foundation.NSCoder coder);
	public UICoordinateSpace (MonoTouch.Foundation.NSObjectFlag t);
	public UICoordinateSpace (System.IntPtr handle);
	// properties
	public virtual System.Drawing.RectangleF Bounds { get; }
	// methods
	public virtual System.Drawing.PointF ConvertPointFromCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.PointF ConvertPointToCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectFromCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectToCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
}
```

### New Type MonoTouch.UIKit.UICoordinateSpace_Extensions

```
public static class UICoordinateSpace_Extensions {
}
```

### New Type MonoTouch.UIKit.UIDeviceOrientationExtensions

```
public static class UIDeviceOrientationExtensions {
	// methods
	public static bool IsFlat (UIDeviceOrientation orientation);
	public static bool IsLandscape (UIDeviceOrientation orientation);
	public static bool IsPortrait (UIDeviceOrientation orientation);
}
```

### New Type MonoTouch.UIKit.UIExtensionPointIdentifier

```
public static class UIExtensionPointIdentifier {
	// properties
	public static MonoTouch.Foundation.NSString Keyboard { get; }
}
```

## Namespace MonoTouch.WebKit



### Type Changed: MonoTouch.WebKit.WKFrameInfo

Added interface:

```
MonoTouch.Foundation.INSCopying
```

Added method:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.WebKit.WKNavigationDelegate

Added method:

```
public virtual void DidReceiveAuthenticationChallenge (WKWebView webView, MonoTouch.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoTouch.Foundation.NSUrlSessionAuthChallengeDisposition,MonoTouch.Foundation.NSUrlCredential> completionHandler);
```

### Type Changed: MonoTouch.WebKit.WKNavigationDelegate_Extensions

Added method:

```
public static void DidReceiveAuthenticationChallenge (IWKNavigationDelegate This, WKWebView webView, MonoTouch.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoTouch.Foundation.NSUrlSessionAuthChallengeDisposition,MonoTouch.Foundation.NSUrlCredential> completionHandler);
```

### Type Changed: MonoTouch.WebKit.WKPreferences

Removed constructor:

```
public WKPreferences (string userDefaultsKeyPrefix);
```

Removed properties:

```
public virtual bool AllowsInlineMediaPlayback { get; set; }
	public virtual bool MediaPlaybackAllowsAirPlay { get; set; }
	public virtual bool MediaPlaybackRequiresUserAction { get; set; }
	public virtual bool SuppressesIncrementalRendering { get; set; }
	public virtual string UserDefaultsKeyPrefix { get; }
```

### Type Changed: MonoTouch.WebKit.WKScriptMessage

Added property:

```
public virtual WKFrameInfo FrameInfo { get; }
```

### Type Changed: MonoTouch.WebKit.WKUserScript

Removed constructor:

```
public WKUserScript (string source, WKUserScriptInjectionTime injectionTime, bool isForMainFrameOnly);
```

Added constructor:

```
public WKUserScript (MonoTouch.Foundation.NSString source, WKUserScriptInjectionTime injectionTime, bool isForMainFrameOnly);
```

Removed property:

```
public virtual string Source { get; }
```

Added property:

```
public virtual MonoTouch.Foundation.NSString Source { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.WebKit.WKWebView

Added interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

Added property:

```
public virtual MonoTouch.UIKit.UIScrollView ScrollView { get; }
```

Added methods:

```
public virtual void EvaluateJavaScript (MonoTouch.Foundation.NSString javascript, WKJavascriptEvaluationResult completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.Foundation.NSObject> EvaluateJavaScriptAsync (MonoTouch.Foundation.NSString javascript);
	public virtual WKNavigation LoadHtmlString (MonoTouch.Foundation.NSString htmlString, MonoTouch.Foundation.NSUrl baseUrl);
```

### Type Changed: MonoTouch.WebKit.WKWebViewConfiguration

Added properties:

```
public virtual bool AllowsInlineMediaPlayback { get; set; }
	public virtual bool MediaPlaybackAllowsAirPlay { get; set; }
	public virtual bool MediaPlaybackRequiresUserAction { get; set; }
	public virtual WKSelectionGranularity SelectionGranularity { get; set; }
	public virtual bool SuppressesIncrementalRendering { get; set; }
```

### New Type MonoTouch.WebKit.WKErrorCode

```
[Serializable]
public enum WKErrorCode {
	JavaScriptExceptionOccurred = 4,
	None = 0,
	Unknown = 1,
	WebContentProcessTerminated = 2,
	WebViewInvalidated = 3,
}
```

### New Type MonoTouch.WebKit.WKJavascriptEvaluationResult

```
public sealed delegate WKJavascriptEvaluationResult : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WKJavascriptEvaluationResult (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSObject result, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSObject result, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.WebKit.WKSelectionGranularity

```
[Serializable]
public enum WKSelectionGranularity {
	Character = 1,
	Dynamic = 0,
}
```

## New Namespace MonoTouch.CoreAudioKit

### New Type MonoTouch.CoreAudioKit.CABTMidiCentralViewController

```
public class CABTMidiCentralViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CABTMidiCentralViewController ();
	public CABTMidiCentralViewController (MonoTouch.Foundation.NSCoder coder);
	public CABTMidiCentralViewController (MonoTouch.Foundation.NSObjectFlag t);
	public CABTMidiCentralViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.CoreAudioKit.CABTMidiLocalPeripheralViewController

```
public class CABTMidiLocalPeripheralViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CABTMidiLocalPeripheralViewController ();
	public CABTMidiLocalPeripheralViewController (MonoTouch.Foundation.NSCoder coder);
	public CABTMidiLocalPeripheralViewController (MonoTouch.Foundation.NSObjectFlag t);
	public CABTMidiLocalPeripheralViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.CoreAudioKit.CAInterAppAudioSwitcherView

```
public class CAInterAppAudioSwitcherView : MonoTouch.UIKit.UIView, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAInterAppAudioSwitcherView ();
	public CAInterAppAudioSwitcherView (MonoTouch.Foundation.NSCoder coder);
	public CAInterAppAudioSwitcherView (MonoTouch.Foundation.NSObjectFlag t);
	public CAInterAppAudioSwitcherView (System.IntPtr handle);
	public CAInterAppAudioSwitcherView (System.Drawing.RectangleF bounds);
	// properties
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance Appearance { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ShowingAppNames { get; set; }
	// methods
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	public virtual float ContentWidth ();
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> ();
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static CAInterAppAudioSwitcherView.CAInterAppAudioSwitcherViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual void SetOutputAudioUnit (MonoTouch.AudioUnit.AudioUnit audioUnit);

	// inner types
	public class CAInterAppAudioSwitcherViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	}
}
```

### New Type MonoTouch.CoreAudioKit.CAInterAppAudioTransportView

```
public class CAInterAppAudioTransportView : MonoTouch.UIKit.UIView, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAInterAppAudioTransportView ();
	public CAInterAppAudioTransportView (MonoTouch.Foundation.NSCoder coder);
	public CAInterAppAudioTransportView (MonoTouch.Foundation.NSObjectFlag t);
	public CAInterAppAudioTransportView (System.IntPtr handle);
	public CAInterAppAudioTransportView (System.Drawing.RectangleF bounds);
	// properties
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance Appearance { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Connected { get; }
	public virtual MonoTouch.UIKit.UIFont CurrentTimeLabelFont { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual MonoTouch.UIKit.UIColor LabelColor { get; set; }
	public virtual MonoTouch.UIKit.UIColor PauseButtonColor { get; set; }
	public virtual MonoTouch.UIKit.UIColor PlayButtonColor { get; set; }
	public virtual bool Playing { get; }
	public virtual MonoTouch.UIKit.UIColor RecordButtonColor { get; set; }
	public virtual bool Recording { get; }
	public virtual MonoTouch.UIKit.UIColor RewindButtonColor { get; set; }
	// methods
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> ();
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static CAInterAppAudioTransportView.CAInterAppAudioTransportViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual void SetOutputAudioUnit (MonoTouch.AudioUnit.AudioUnit audioUnit);

	// inner types
	public class CAInterAppAudioTransportViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	}
}
```

   


 <hr>

# MonoTouch.Dialog-1.dll

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.Dialog.GlassButton

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

   


 <hr>

# OpenTK.dll

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

   


 <hr>

# OpenTK-1.0.dll

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Removed interface:

```
MonoTouch.UIKit.IUICoordinateSpace
```

   


 <hr>
