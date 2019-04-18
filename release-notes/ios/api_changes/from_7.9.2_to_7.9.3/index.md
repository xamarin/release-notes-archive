---
id: D5D2D76A-A4A1-4774-BF5A-8CC9509815A0
title: "From 7.9.2 to 7.9.3"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed field:

```
public static const string Version = "7.9.2";
```

Added fields:

```
public static const string CoreMotionLibrary = "System/Library/Frameworks/CoreMotion.framework/CoreMotion";
	public static const string Version = "7.9.3";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.IABPeoplePickerNavigationControllerDelegate

Added interface:

```
MonoTouch.UIKit.IUINavigationControllerDelegate
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVMetadata

Removed property:

```
public static MonoTouch.Foundation.NSString FormatIcyMetadata { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVVideoCodecSettings

Removed properties:

```
public AVVideoPixelAspectRatioSettings PixelAspectRatio { set; }
	public AVVideoCleanApertureSettings VideoCleanAperture { set; }
```

Added properties:

```
public AVVideoPixelAspectRatioSettings PixelAspectRatio { get; set; }
	public AVVideoCleanApertureSettings VideoCleanAperture { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVVideoSettingsCompressed

Removed properties:

```
public AVVideoCodec? Codec { set; }
	public AVVideoCodecSettings CodecSettings { set; }
	public AVVideoScalingMode? ScalingMode { set; }
```

Added properties:

```
public AVVideoCodec? Codec { get; set; }
	public AVVideoCodecSettings CodecSettings { get; set; }
	public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVVideoSettingsUncompressed

Removed property:

```
public AVVideoScalingMode? ScalingMode { set; }
```

Added property:

```
public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.IAVPlayerItemLegibleOutputPushDelegate

Added interface:

```
IAVPlayerItemOutputPushDelegate
```

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKDatabase

Removed methods:

```
public virtual void FetchAllSubscriptions (System.Action<MonoTouch.Foundation.NSArray,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.Foundation.NSArray> FetchAllSubscriptionsAsync ();
	public virtual void PerformQuery (CKQuery query, CKRecordZoneID zoneId, System.Action<CKRecordZone,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> PerformQueryAsync (CKQuery query, CKRecordZoneID zoneId);
```

Added methods:

```
public virtual void FetchAllSubscriptions (System.Action<CKSubscription[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription[]> FetchAllSubscriptionsAsync ();
	public virtual void PerformQuery (CKQuery query, CKRecordZoneID zoneId, System.Action<CKRecord[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord[]> PerformQueryAsync (CKQuery query, CKRecordZoneID zoneId);
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMFormatDescription

Added method:

```
public MonoTouch.Foundation.NSObject GetExtension (string extensionKey);
```

### Type Changed: MonoTouch.CoreMedia.CMSampleBuffer

Added methods:

```
public CMSampleBufferError CallForEachSample (System.Func<CMSampleBuffer,System.Int32,MonoTouch.CoreMedia.CMSampleBufferError> callback);
	public static CMSampleBuffer CreateReady (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMSampleTimingInfo[] sampleTimingArray, uint[] sampleSizeArray, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, CMFormatDescription formatDescription, CMSampleTimingInfo[] sampleTiming, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, MonoTouch.AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
	public CMSampleBufferError SetInvalidateCallback (System.Action<CMSampleBuffer> invalidateHandler);
```

### Type Changed: MonoTouch.CoreMedia.CMTime

Added properties:

```
public bool HasBeenRounded { get; }
	public bool IsNumeric { get; }
```

## Namespace MonoTouch.CoreText

### Type Changed: MonoTouch.CoreText.CTLineBoundsOptions

Added value:

```
IncludeLanguageExtents = 32,
```

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVPixelBuffer

Added field:

```
public static MonoTouch.Foundation.NSString MetalCompatibilityKey;
```

### Type Changed: MonoTouch.CoreVideo.CVPixelBufferAttributes

Added properties:

```
public bool? AllocateWithIOSurface { get; set; }
	public bool? MetalCompatibility { get; set; }
```

### Type Changed: MonoTouch.CoreVideo.CVReturn

Added value:

```
PixelBufferNotMetalCompatible = -6684,
```

### New Type MonoTouch.CoreVideo.CVMetalTexture

```
public class CVMetalTexture : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual System.IntPtr Handle { get; }
	public bool IsFlipped { get; }
	public MonoTouch.Metal.IMTLTexture Texture { get; }
	// methods
	protected override void ~CVMetalTexture ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void GetCleanTexCoords (out float[] lowerLeft, out float[] lowerRight, out float[] upperRight, out float[] upperLeft);
}
```

### New Type MonoTouch.CoreVideo.CVMetalTextureCache

```
public class CVMetalTextureCache : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CVMetalTextureCache (MonoTouch.Metal.IMTLDevice metalDevice);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CVMetalTextureCache ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void Flush (CVOptionFlags flags);
	public static CVMetalTextureCache FromDevice (MonoTouch.Metal.IMTLDevice metalDevice);
	public CVMetalTexture TextureFromImage (CVImageBuffer imageBuffer, MonoTouch.Metal.MTLPixelFormat format, int width, int height, int planeIndex, out CVReturn errorCode);
}
```

## Namespace MonoTouch.ExternalAccessory

### Type Changed: MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate

Removed method:

```
public virtual void DidFinishConfiguringAccessory (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, MonoTouch.Foundation.NSError error);
```

Added method:

```
public virtual void DidFinishConfiguringAccessory (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
```

### Type Changed: MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate_Extensions

Removed method:

```
public static void DidFinishConfiguringAccessory (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, MonoTouch.Foundation.NSError error);
```

Added method:

```
public static void DidFinishConfiguringAccessory (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
```

### Type Changed: MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryDidFinishEventArgs

Removed constructor:

```
public EAWiFiUnconfiguredAccessoryDidFinishEventArgs (EAWiFiUnconfiguredAccessory accessory, MonoTouch.Foundation.NSError error);
```

Added constructor:

```
public EAWiFiUnconfiguredAccessoryDidFinishEventArgs (EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
```

Removed property:

```
public MonoTouch.Foundation.NSError Error { get; set; }
```

Added property:

```
public EAWiFiUnconfiguredAccessoryConfigurationStatus Status { get; set; }
```

### Type Changed: MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryProperties

Added value:

```
SupportsHomeKit = 4,
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryConfigurationStatus

```
[Serializable]
public enum EAWiFiUnconfiguredAccessoryConfigurationStatus {
	Failed = 2,
	Success = 0,
	UserCancelledConfiguration = 1,
}
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.INSMachPortDelegate

Added interface:

```
INSPortDelegate
```

### Type Changed: MonoTouch.Foundation.INSUrlConnectionDownloadDelegate

Added interface:

```
INSUrlConnectionDelegate
```

### Type Changed: MonoTouch.Foundation.INSUrlSessionDataDelegate

Added interfaces:

```
INSUrlSessionTaskDelegate
	INSUrlSessionDelegate
```

### Type Changed: MonoTouch.Foundation.INSUrlSessionDownloadDelegate

Added interfaces:

```
INSUrlSessionTaskDelegate
	INSUrlSessionDelegate
```

### Type Changed: MonoTouch.Foundation.INSUrlSessionTaskDelegate

Added interface:

```
INSUrlSessionDelegate
```

### Type Changed: MonoTouch.Foundation.NSError

Added properties:

```
public static NSString CoreLocationErrorDomain { get; }
	public static NSString CoreMotionErrorDomain { get; }
	public static NSString EABluetoothAccessoryPickerErrorDomain { get; }
	public static NSString MapKitErrorDomain { get; }
	public static NSString NSNetServicesErrorDomain { get; }
	public static NSString NSStreamSocketSSLErrorDomain { get; }
	public static NSString NSStreamSOCKSErrorDomain { get; }
```

### Type Changed: MonoTouch.Foundation.NSFilePresenter

Added methods:

```
public virtual void AccommodatePresentedItemDeletion (System.Action<NSError> completionHandler);
	public virtual void AccommodatePresentedSubitemDeletion (NSUrl url, System.Action<NSError> completionHandler);
	public virtual void RelinquishPresentedItemToReader (MonoTouch.UIKit.NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (MonoTouch.UIKit.NSFilePresenterReacquirer writerAction);
	public virtual void SavePresentedItemChanges (System.Action<NSError> completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSFilePresenter_Extensions

Added methods:

```
public static void AccommodatePresentedItemDeletion (INSFilePresenter This, System.Action<NSError> completionHandler);
	public static void AccommodatePresentedSubitemDeletion (INSFilePresenter This, NSUrl url, System.Action<NSError> completionHandler);
	public static void RelinquishPresentedItemToReader (INSFilePresenter This, MonoTouch.UIKit.NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, MonoTouch.UIKit.NSFilePresenterReacquirer writerAction);
	public static void SavePresentedItemChanges (INSFilePresenter This, System.Action<NSError> completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSItemProvider

Removed methods:

```
public virtual bool HasItemConformingToTypeIdentifier (string typeIdentifier);
	public virtual void LoadItemForTypeIdentifier (string typeIdentifier, NSDictionary options, System.Action<NSObject,MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual bool HasItemConformingTo (string typeIdentifier);
	public virtual void LoadItem (string typeIdentifier, NSDictionary options, System.Action<NSObject,MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSMetadataQuery

Removed property:

```
public static NSString QueryAccessibleUbiquitousExternalDocumentsScope { get; }
```

Added properties:

```
public static NSString AccessibleUbiquitousExternalDocumentsScope { get; }
	public static NSString UbiquitousDataScope { get; }
	public static NSString UbiquitousDocumentsScope { get; }
```

### Type Changed: MonoTouch.Foundation.NSMutableIndexSet

Added methods:

```
public virtual void AddIndexesInRange (NSRange range);
	public virtual void RemoveIndexesInRange (NSRange range);
```

### Type Changed: MonoTouch.Foundation.NSUrlComponents

Removed method:

```
public override string ToString ();
```

Added method:

```
public virtual string AsString ();
```

### Type Changed: MonoTouch.Foundation.NSUserActivity

Removed constructor:

```
public NSUserActivity (string activityType);
```

Added constructor:

```
public NSUserActivity (NSString activityType);
```

### New Type MonoTouch.Foundation.NSCocoaError

```
[Serializable]
public enum NSCocoaError {
	ExecutableArchitectureMismatch = 3585,
	ExecutableErrorMaximum = 3839,
	ExecutableErrorMinimum = 3584,
	ExecutableLink = 3588,
	ExecutableLoad = 3587,
	ExecutableNotLoadable = 3584,
	ExecutableRuntimeMismatch = 3586,
	FeatureUnsupported = 3328,
	FileErrorMaximum = 1023,
	FileErrorMinimum = 0,
	FileLocking = 255,
	FileNoSuchFile = 4,
	FileReadCorruptFile = 259,
	FileReadInapplicableStringEncoding = 261,
	FileReadInvalidFileName = 258,
	FileReadNoPermission = 257,
	FileReadNoSuchFile = 260,
	FileReadTooLarge = 263,
	FileReadUnknown = 256,
	FileReadUnknownStringEncoding = 264,
	FileReadUnsupportedScheme = 262,
	FileWriteFileExists = 516,
	FileWriteInapplicableStringEncoding = 517,
	FileWriteInvalidFileName = 514,
	FileWriteNoPermission = 513,
	FileWriteOutOfSpace = 640,
	FileWriteUnknown = 512,
	FileWriteUnsupportedScheme = 518,
	FileWriteVolumeReadOnly = 642,
	Formatting = 2048,
	FormattingErrorMaximum = 2559,
	FormattingErrorMinimum = 2048,
	KeyValueValidation = 1024,
	None = 0,
	PropertyListErrorMaximum = 4095,
	PropertyListErrorMinimum = 3840,
	PropertyListReadCorrupt = 3840,
	PropertyListReadStream = 3842,
	PropertyListReadUnknownVersion = 3841,
	PropertyListWriteInvalid = 3852,
	PropertyListWriteStream = 3851,
	UbiquitousFileErrorMaximum = 4607,
	UbiquitousFileErrorMinimum = 4352,
	UbiquitousFileNotUploadedDueToQuota = 4354,
	UbiquitousFileUbiquityServerNotAvailable = 4355,
	UbiquitousFileUnavailable = 4353,
	UserCancelled = 3072,
	ValidationErrorMaximum = 2047,
	ValidationErrorMinimum = 1024,
	XpcConnectionErrorMaximum = 4224,
	XpcConnectionErrorMinimum = 4096,
	XpcConnectionInterrupted = 4097,
	XpcConnectionInvalid = 4099,
	XpcConnectionReplyInvalid = 4101,
}
```

### New Type MonoTouch.Foundation.NSUserActivityType

```
public static class NSUserActivityType {
	// properties
	public static NSString BrowsingWeb { get; }
}
```

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKQuantityTypeIdentifier

Removed values:

```
ActiveEnergyBurned = 10,
	BasalEnergyBurned = 9,
	BloodAlcoholContent = 17,
	BloodGlucose = 14,
	BloodPressureDiastolic = 16,
	BloodPressureSystolic = 15,
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
	HeatFlux = 20,
	InhalerUsage = 21,
	NikeFuel = 12,
	NumberOfTimesFallen = 19,
	OxygenSaturation = 13,
	PeripheralPerfusionIndex = 18,
	RespiratoryRate = 22,
	RRInterval = 6,
	StepCount = 7,
```

Added values:

```
ActiveEnergyBurned = 9,
	BasalEnergyBurned = 8,
	BloodAlcoholContent = 16,
	BloodGlucose = 13,
	BloodPressureDiastolic = 15,
	BloodPressureSystolic = 14,
	BodyTemperature = 24,
	DietaryBiotin = 49,
	DietaryCaffeine = 62,
	DietaryCalcium = 43,
	DietaryCarbohydrates = 31,
	DietaryChloride = 60,
	DietaryCholesterol = 29,
	DietaryChromium = 58,
	DietaryCopper = 56,
	DietaryEnergyConsumed = 34,
	DietaryFatMonounsaturated = 27,
	DietaryFatPolyunsaturated = 26,
	DietaryFatSaturated = 28,
	DietaryFatTotal = 25,
	DietaryFiber = 32,
	DietaryFolate = 48,
	DietaryIodine = 52,
	DietaryIron = 44,
	DietaryMagnesium = 53,
	DietaryManganese = 57,
	DietaryMolybdenum = 59,
	DietaryNiacin = 47,
	DietaryPantothenicAcid = 50,
	DietaryPhosphorus = 51,
	DietaryPotassium = 61,
	DietaryProtein = 35,
	DietaryRiboflavin = 46,
	DietarySelenium = 55,
	DietarySodium = 30,
	DietarySugar = 33,
	DietaryThiamin = 45,
	DietaryVitaminA = 36,
	DietaryVitaminB12 = 38,
	DietaryVitaminB6 = 37,
	DietaryVitaminC = 39,
	DietaryVitaminD = 40,
	DietaryVitaminE = 41,
	DietaryVitaminK = 42,
	DietaryZinc = 54,
	Distance = 7,
	FlightsClimbed = 10,
	ForcedExpiratoryVolume1 = 19,
	ForcedVitalCapacity = 18,
	InhalerUsage = 22,
	NikeFuel = 11,
	NumberOfTimesFallen = 21,
	OxygenSaturation = 12,
	PeakExpiratoryFlowRate = 20,
	PeripheralPerfusionIndex = 17,
	RespiratoryRate = 23,
	StepCount = 6,
```

### Type Changed: MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

Removed properties:

```
public static MonoTouch.Foundation.NSString HeatFlux { get; }
	public static MonoTouch.Foundation.NSString RRInterval { get; }
```

Added properties:

```
public static MonoTouch.Foundation.NSString ForcedExpiratoryVolume1 { get; }
	public static MonoTouch.Foundation.NSString ForcedVitalCapacity { get; }
	public static MonoTouch.Foundation.NSString PeakExpiratoryFlowRate { get; }
```

### Type Changed: MonoTouch.HealthKit.HKWorkoutType

Added property:

```
public static MonoTouch.Foundation.NSString Identifier { get; }
```

### Removed Type MonoTouch.HealthKit.HKCorrelatinTypeKey ### New Type MonoTouch.HealthKit.HKCorrelationTypeKey

```
public static class HKCorrelationTypeKey {
	// properties
	public static MonoTouch.Foundation.NSString IdentifierBloodPressure { get; }
	public static MonoTouch.Foundation.NSString IdentifierFood { get; }
}
```



## Namespace MonoTouch.HomeKit

### Type Changed: MonoTouch.HomeKit.HMAccessory

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed properties:

```
public virtual bool Configured { get; }
	public virtual MonoTouch.Foundation.NSUuid identifier { get; }
```

Added properties:

```
public virtual bool Blocked { get; }
	public virtual MonoTouch.Foundation.NSUuid Identifier { get; }
```

Removed event:

```
public event System.EventHandler<HMAccessoryUpdateForServiceEventArgs> DidUpdateNameForService;
```

Added events:

```
public event System.EventHandler<HMAccessoryUpdateEventArgs> DidUpdateAssociatedServiceType;
	public event System.EventHandler<HMAccessoryUpdateEventArgs> DidUpdateNameForService;
```

Removed method:

```
public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void Identify (System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task IdentifyAsync ();
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMAccessoryDelegate

Removed method:

```
public virtual void DidUpdateNameForService (HMAccessory accesssory, HMService service);
```

Added methods:

```
public virtual void DidUpdateAssociatedServiceType (HMAccessory accessory, HMService service);
	public virtual void DidUpdateNameForService (HMAccessory accessory, HMService service);
```

### Type Changed: MonoTouch.HomeKit.HMAccessoryDelegate_Extensions

Removed method:

```
public static void DidUpdateNameForService (IHMAccessoryDelegate This, HMAccessory accesssory, HMService service);
```

Added methods:

```
public static void DidUpdateAssociatedServiceType (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);
	public static void DidUpdateNameForService (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);
```

### Type Changed: MonoTouch.HomeKit.HMActionSet

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed properties:

```
public static MonoTouch.Foundation.NSString ExecutionFailedActionKey { get; }
	public virtual bool IsExecuting { get; }
```

Added property:

```
public virtual bool Executing { get; }
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristic

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Added property:

```
public virtual MonoTouch.Foundation.NSString[] _Properties { get; }
```

Removed methods:

```
public virtual void EnableNotification (bool enable, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void ReadValue (System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void WriteValue (MonoTouch.Foundation.NSObject value, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void EnableNotification (bool enable, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void ReadValue (System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateAuthorizationData (MonoTouch.Foundation.NSData data, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateAuthorizationDataAsync (MonoTouch.Foundation.NSData data);
	public virtual void WriteValue (MonoTouch.Foundation.NSObject value, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristicMetadata

Removed property:

```
public virtual MonoTouch.Foundation.NSNumber Precision { get; }
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristicMetadataFormat

Removed value:

```
Object = 6,
```

Added values:

```
Data = 11,
	Dictionary = 6,
	Tlv8 = 12,
	UInt16 = 8,
	UInt32 = 9,
	UInt64 = 10,
	UInt8 = 7,
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristicType

Removed values:

```
CurrentDoorState = 11,
	CurrentRelativeHumidity = 9,
	HeatingCoolingStatus = 8,
	Locked = 14,
	ObstructionDetected = 13,
	TargetDoorState = 12,
	TargetRelativeHumidity = 10,
```

Added values:

```
AdminOnlyAccess = 29,
	AudioFeedback = 28,
	CoolingThreshold = 10,
	CurrentDoorState = 15,
	CurrentHeatingCooling = 8,
	CurrentLockMechanismState = 31,
	CurrentRelativeHumidity = 13,
	HeatingCoolingStatus = 12,
	HeatingThreshold = 11,
	Identify = 22,
	LockManagementAutoSecureTimeout = 35,
	LockManagementControlPoint = 34,
	LockMechanismLastKnownAction = 33,
	Logs = 27,
	Manufacturer = 19,
	Model = 20,
	MotionDetected = 30,
	Name = 18,
	ObstructionDetected = 17,
	OutletInUse = 25,
	RotationDirection = 23,
	RotationSpeed = 24,
	SerialNumber = 21,
	TargetDoorState = 16,
	TargetHeatingCooling = 9,
	TargetLockMechanismState = 32,
	TargetRelativeHumidity = 14,
	Version = 26,
```

### Type Changed: MonoTouch.HomeKit.HMCharacteristicWriteAction

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed method:

```
public virtual void UpdateTargetValue (MonoTouch.Foundation.NSObject targetValue, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added method:

```
public virtual void UpdateTargetValue (MonoTouch.Foundation.NSObject targetValue, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMHome

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed property:

```
public virtual MonoTouch.Foundation.NSString[] Users { get; }
```

Added property:

```
public virtual string[] Users { get; }
```

Removed events:

```
public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidAddServiceToServiceGroup;
	public event System.EventHandler<HMHomeErrorEventArgs> DidEncounterError;
	public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidRemoveServiceFromServiceGroup;
	public event System.EventHandler DidUpdateName;
	public event System.EventHandler<HMomeRoomAccessoryEventArgs> DidUpdateRoom;
```

Added events:

```
public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidAddService;
	public event System.EventHandler<HMHomeUserEventArgs> DidAddUser;
	public event System.EventHandler<HMHomeErrorAccessoryEventArgs> DidEncounterError;
	public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidRemoveService;
	public event System.EventHandler<HMHomeUserEventArgs> DidRemoveUser;
	public event System.EventHandler<HMHomeAccessoryEventArgs> DidUnblockAccessory;
	public event System.EventHandler DidUpdateNameForHome;
	public event System.EventHandler<HMHomeRoomAccessoryEventArgs> DidUpdateRoom;
```

Removed methods:

```
public virtual void AddAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AddActionSet (string actionSetName, System.Action<HMActionSet,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AddRoom (string roomName, System.Action<HMRoom,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AddServiceGroup (string serviceGroupName, System.Action<HMServiceGroup,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AddTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AddUser (MonoTouch.Foundation.NSString userID, HMHomeUserPrivilege privilege, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task AddUserAsync (MonoTouch.Foundation.NSString userID, HMHomeUserPrivilege privilege);
	public virtual void AddZone (string zoneName, System.Action<HMZone,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AssignAccessory (HMAccessory accessory, HMRoom room, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void ExecuteActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void GetPrivilegeForUser (MonoTouch.Foundation.NSString userID, System.Action<HMHomeUserPrivilege,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<HMHomeUserPrivilege> GetPrivilegeForUserAsync (MonoTouch.Foundation.NSString userID);
	public virtual void RemoveAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveServiceGroup (HMServiceGroup serviceGroup, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task RemoveServiceGroupAsync (HMServiceGroup serviceGroup);
	public virtual void RemoveTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveUser (MonoTouch.Foundation.NSString userID, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task RemoveUserAsync (MonoTouch.Foundation.NSString userID);
	public virtual void RemoveZone (HMZone zone, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual HMRoom RoomForEntireHome ();
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void AddAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void AddActionSet (string actionSetName, System.Action<HMActionSet,MonoTouch.Foundation.NSError> completion);
	public virtual void AddRoom (string roomName, System.Action<HMRoom,MonoTouch.Foundation.NSError> completion);
	public virtual void AddServiceGroup (string serviceGroupName, System.Action<HMServiceGroup,MonoTouch.Foundation.NSError> completion);
	public virtual void AddTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void AddUser (string userId, HMHomeUserPrivilege privilege, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddUserAsync (string userId, HMHomeUserPrivilege privilege);
	public virtual void AddZone (string zoneName, System.Action<HMZone,MonoTouch.Foundation.NSError> completion);
	public virtual void AssignAccessory (HMAccessory accessory, HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void ExecuteActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual HMRoom GetRoomForEntireHome ();
	public virtual void GetUserPrivilege (string userId, System.Action<HMHomeUserPrivilege,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMHomeUserPrivilege> GetUserPrivilegeAsync (string userId);
	public virtual void RemoveAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveServiceGroup (HMServiceGroup group, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveServiceGroupAsync (HMServiceGroup group);
	public virtual void RemoveTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveUser (string userId, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveUserAsync (string userId);
	public virtual void RemoveZone (HMZone zone, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UnblockAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UnblockAccessoryAsync (HMAccessory accessory);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMHomeDelegate

Removed methods:

```
public virtual void DidAddServiceGroup (HMHome home, HMServiceGroup serviceGroup);
	public virtual void DidAddServiceToServiceGroup (HMHome home, HMService service, HMServiceGroup serviceGroup);
	public virtual void DidRemoveServiceFromServiceGroup (HMHome home, HMService service, HMServiceGroup serviceGroup);
	public virtual void DidRemoveServiceGroup (HMHome home, HMServiceGroup serviceGroup);
	public virtual void DidUpdateName (HMHome home);
	public virtual void DidUpdateNameForServiceGroup (HMHome home, HMServiceGroup serviceGroup);
```

Added methods:

```
public virtual void DidAddService (HMHome home, HMService service, HMServiceGroup group);
	public virtual void DidAddServiceGroup (HMHome home, HMServiceGroup group);
	public virtual void DidAddUser (HMHome home, string userId);
	public virtual void DidRemoveService (HMHome home, HMService service, HMServiceGroup group);
	public virtual void DidRemoveServiceGroup (HMHome home, HMServiceGroup group);
	public virtual void DidRemoveUser (HMHome home, string userId);
	public virtual void DidUnblockAccessory (HMHome home, HMAccessory accessory);
	public virtual void DidUpdateNameForHome (HMHome home);
	public virtual void DidUpdateNameForServiceGroup (HMHome home, HMServiceGroup group);
```

### Type Changed: MonoTouch.HomeKit.HMHomeDelegate_Extensions

Removed methods:

```
public static void DidAddServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup serviceGroup);
	public static void DidAddServiceToServiceGroup (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup serviceGroup);
	public static void DidRemoveServiceFromServiceGroup (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup serviceGroup);
	public static void DidRemoveServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup serviceGroup);
	public static void DidUpdateName (IHMHomeDelegate This, HMHome home);
	public static void DidUpdateNameForServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup serviceGroup);
```

Added methods:

```
public static void DidAddService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);
	public static void DidAddServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
	public static void DidAddUser (IHMHomeDelegate This, HMHome home, string userId);
	public static void DidRemoveService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);
	public static void DidRemoveServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
	public static void DidRemoveUser (IHMHomeDelegate This, HMHome home, string userId);
	public static void DidUnblockAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);
	public static void DidUpdateNameForHome (IHMHomeDelegate This, HMHome home);
	public static void DidUpdateNameForServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
```

### Type Changed: MonoTouch.HomeKit.HMHomeManager

Removed methods:

```
public virtual void AddHome (string homeName, System.Action<HMHome,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdatePrimaryHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void AddHome (string homeName, System.Action<HMHome,MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdatePrimaryHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMHomeServiceGroupEventArgs

Removed constructor:

```
public HMHomeServiceGroupEventArgs (HMServiceGroup serviceGroup);
```

Added constructor:

```
public HMHomeServiceGroupEventArgs (HMServiceGroup group);
```

Removed property:

```
public HMServiceGroup ServiceGroup { get; set; }
```

Added property:

```
public HMServiceGroup Group { get; set; }
```

### Type Changed: MonoTouch.HomeKit.HMHomeServiceServiceGroupEventArgs

Removed constructor:

```
public HMHomeServiceServiceGroupEventArgs (HMService service, HMServiceGroup serviceGroup);
```

Added constructor:

```
public HMHomeServiceServiceGroupEventArgs (HMService service, HMServiceGroup group);
```

Removed property:

```
public HMServiceGroup ServiceGroup { get; set; }
```

Added property:

```
public HMServiceGroup Group { get; set; }
```

### Type Changed: MonoTouch.HomeKit.HMRoom

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed method:

```
public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added method:

```
public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMService

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Added property:

```
public virtual string AssociatedServiceType { get; }
```

Removed method:

```
public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void UpdateAssociatedServiceType (string serviceType, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateAssociatedServiceTypeAsync (string serviceType);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMServiceGroup

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed methods:

```
public virtual void AddService (HMService service, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveService (HMService service, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void AddService (HMService service, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveService (HMService service, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMServiceType

Removed values:

```
GarageDoorOpener = 5,
	Lock = 4,
```

Added values:

```
AccessoryInformation = 5,
	Fan = 6,
	GarageDoorOpener = 4,
	LockManagement = 9,
	LockMechanism = 8,
	Outlet = 7,
```

### Type Changed: MonoTouch.HomeKit.HMTimerTrigger

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed property:

```
public virtual MonoTouch.Foundation.NSDate LastFireDate { get; }
```

Removed methods:

```
public virtual void UpdateFireDate (MonoTouch.Foundation.NSDate fireDate, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateRecurrence (MonoTouch.Foundation.NSDateComponents recurrence, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateTimeZone (MonoTouch.Foundation.NSTimeZone timeZone, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void UpdateFireDate (MonoTouch.Foundation.NSDate fireDate, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateRecurrence (MonoTouch.Foundation.NSDateComponents recurrence, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateTimeZone (MonoTouch.Foundation.NSTimeZone timeZone, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMTrigger

Removed constructor:

```
public HMTrigger (string name);
```

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Added property:

```
public virtual MonoTouch.Foundation.NSDate LastFireDate { get; }
```

Removed methods:

```
public virtual void AddActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void Enable (bool enable, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void AddActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void Enable (bool enable, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Type Changed: MonoTouch.HomeKit.HMZone

Removed interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSSecureCoding
```

Removed methods:

```
public virtual void AddRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

Added methods:

```
public virtual void AddRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
```

### Removed Type MonoTouch.HomeKit.HMAccessoryUpdateForServiceEventArgs ### Removed Type MonoTouch.HomeKit.HMHomeErrorEventArgs ### Removed Type MonoTouch.HomeKit.HMomeRoomAccessoryEventArgs ### New Type MonoTouch.HomeKit.HMAccessoryUpdateEventArgs

```
public class HMAccessoryUpdateEventArgs : System.EventArgs {
	// constructors
	public HMAccessoryUpdateEventArgs (HMService service);
	// properties
	public HMService Service { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueDoorState

```
[Serializable]
public enum HMCharacteristicValueDoorState {
	Closed = 1,
	Closing = 3,
	Open = 0,
	Opening = 2,
	Stopped = 4,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueHeatingCooling

```
[Serializable]
public enum HMCharacteristicValueHeatingCooling {
	Auto = 3,
	Cool = 2,
	Heat = 1,
	Off = 0,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueLockMechanism

```
[Serializable]
public enum HMCharacteristicValueLockMechanism {
	LastKnownActionSecuredRemotely = 6,
	LastKnownActionSecuredUsingPhysicalMovementExterior = 2,
	LastKnownActionSecuredUsingPhysicalMovementInterior = 0,
	LastKnownActionSecuredWithAutomaticSecureTimeout = 8,
	LastKnownActionSecuredWithKeypad = 4,
	LastKnownActionUnsecuredRemotely = 7,
	LastKnownActionUnsecuredUsingPhysicalMovementExterior = 3,
	LastKnownActionUnsecuredUsingPhysicalMovementInterior = 1,
	LastKnownActionUnsecuredWithKeypad = 5,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueLockMechanismState

```
[Serializable]
public enum HMCharacteristicValueLockMechanismState {
	Jammed = 2,
	Secured = 1,
	Unknown = 3,
	Unsecured = 0,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueRotationDirection

```
[Serializable]
public enum HMCharacteristicValueRotationDirection {
	Clockwise = 0,
	CounterClockwise = 1,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicValueTemperatureUnit

```
[Serializable]
public enum HMCharacteristicValueTemperatureUnit {
	Celsius = 0,
	Fahrenheit = 1,
}
```

### New Type MonoTouch.HomeKit.HMHomeErrorAccessoryEventArgs

```
public class HMHomeErrorAccessoryEventArgs : System.EventArgs {
	// constructors
	public HMHomeErrorAccessoryEventArgs (MonoTouch.Foundation.NSError error, HMAccessory accessory);
	// properties
	public HMAccessory Accessory { get; set; }
	public MonoTouch.Foundation.NSError Error { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeRoomAccessoryEventArgs

```
public class HMHomeRoomAccessoryEventArgs : System.EventArgs {
	// constructors
	public HMHomeRoomAccessoryEventArgs (HMRoom room, HMAccessory accessory);
	// properties
	public HMAccessory Accessory { get; set; }
	public HMRoom Room { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeUserEventArgs

```
public class HMHomeUserEventArgs : System.EventArgs {
	// constructors
	public HMHomeUserEventArgs (string userId);
	// properties
	public string UserId { get; set; }
}
```





## Namespace MonoTouch.MapKit



### Type Changed: MonoTouch.MapKit.IMKOverlay

Added interface:

```
IMKAnnotation
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.IMFMailComposeViewControllerDelegate

Added interface:

```
MonoTouch.UIKit.IUINavigationControllerDelegate
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Removed methods:

```
public static uint UInt32_objc_msgSend_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static uint UInt32_objc_msgSend_IntPtr_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoTouch.Foundation.NSRange arg2);
	public static uint UInt32_objc_msgSendSuper_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static uint UInt32_objc_msgSendSuper_IntPtr_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoTouch.Foundation.NSRange arg2);
```

Added methods:

```
public static int int_objc_msgSend_IntPtr_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoTouch.Foundation.NSRange arg2);
	public static int int_objc_msgSendSuper_IntPtr_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoTouch.Foundation.NSRange arg2);
```

## Namespace MonoTouch.Photos

### Type Changed: MonoTouch.Photos.PHAsset

Removed property:

```
public virtual string CloudIdentifier { get; }
```

Removed method:

```
public static PHFetchResult FetchAssetsUsingCloudIdentifiers (string[] identifiers, PHFetchOptions options);
```

### Type Changed: MonoTouch.Photos.PHAssetCollectionChangeRequest

Removed methods:

```
public virtual void AddAssets (PHAsset[] assets);
	public virtual void InsertAssets (PHAsset[] assets, MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void RemoveAssets (PHAsset[] assets);
	public virtual void ReplaceAssets (MonoTouch.Foundation.NSIndexSet indexes, PHAsset[] assets);
```

Added methods:

```
public virtual void AddAssets (PHObject[] assets);
	public virtual void InsertAssets (PHObject[] assets, MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void RemoveAssets (PHObject[] assets);
	public virtual void ReplaceAssets (MonoTouch.Foundation.NSIndexSet indexes, PHObject[] assets);
```

### Type Changed: MonoTouch.Photos.PHFetchResult

Removed properties:

```
public virtual uint Count { get; }
	public MonoTouch.Foundation.NSObject Item { get; }
```

Added properties:

```
public virtual int Count { get; }
	public MonoTouch.Foundation.NSObject Item { get; }
```

Removed methods:

```
public virtual uint IndexOf (MonoTouch.Foundation.NSObject id);
	public virtual uint IndexOf (MonoTouch.Foundation.NSObject id, MonoTouch.Foundation.NSRange range);
	public virtual MonoTouch.Foundation.NSObject ObjectAt (uint index);
```

Added methods:

```
public virtual int IndexOf (MonoTouch.Foundation.NSObject id);
	public virtual int IndexOf (MonoTouch.Foundation.NSObject id, MonoTouch.Foundation.NSRange range);
	public virtual MonoTouch.Foundation.NSObject ObjectAt (int index);
```

## Namespace MonoTouch.PhotosUI

### Type Changed: MonoTouch.PhotosUI.IPHContentEditingController

Added property:

```
public virtual bool ShouldShowCancelConfirmation { get; }
```

### Type Changed: MonoTouch.PhotosUI.PHContentEditingController

Added property:

```
public virtual bool ShouldShowCancelConfirmation { get; }
```

## Namespace MonoTouch.SceneKit

### Type Changed: MonoTouch.SceneKit.SCNMaterialProperty

Added properties:

```
public MonoTouch.UIKit.UIColor ContentColor { get; set; }
	public MonoTouch.UIKit.UIImage ContentImage { get; set; }
	public MonoTouch.UIKit.UIImage[] ContentImageCube { get; set; }
	public MonoTouch.CoreAnimation.CALayer ContentLayer { get; set; }
	public MonoTouch.Foundation.NSString ContentPath { get; set; }
	public MonoTouch.SpriteKit.SKScene ContentScene { get; set; }
	public MonoTouch.SpriteKit.SKTexture ContentTexture { get; set; }
	public MonoTouch.Foundation.NSUrl ContentUrl { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNNode

Removed method:

```
public virtual SCNNode FindNodes (SCNNodePredicate predicate);
```

Added method:

```
public virtual SCNNode[] FindNodes (SCNNodePredicate predicate);
```

### Type Changed: MonoTouch.SceneKit.SCNText

Removed property:

```
public virtual System.Drawing.SizeF TextSize { get; }
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKAction

Added methods:

```
public static SKAction Run (System.Action block, MonoTouch.CoreFoundation.DispatchQueue queue);
	public static SKAction Run (System.Action block);
```

Obsoleted methods:

```
[Obsolete ("Use Run(Action) instead")]
	public static SKAction RunBlock (System.Action block);

	[Obsolete ("Use Run(Action,DispatchQueue) instead")]
	public static SKAction RunBlock (System.Action block, MonoTouch.CoreFoundation.DispatchQueue queue);
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.ISKProductsRequestDelegate

Added interface:

```
ISKRequestDelegate
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.IUICollectionViewDelegateFlowLayout

Added interfaces:

```
IUICollectionViewDelegate
	IUIScrollViewDelegate
```

### Type Changed: MonoTouch.UIKit.IUIImagePickerControllerDelegate

Added interface:

```
IUINavigationControllerDelegate
```

### Type Changed: MonoTouch.UIKit.IUINavigationBarDelegate

Added interface:

```
IUIBarPositioningDelegate
```

### Type Changed: MonoTouch.UIKit.IUIPickerViewAccessibilityDelegate

Added interface:

```
IUIPickerViewDelegate
```

### Type Changed: MonoTouch.UIKit.IUIPopoverPresentationControllerDelegate

Added interface:

```
IUIAdaptivePresentationControllerDelegate
```

### Type Changed: MonoTouch.UIKit.IUIScrollViewAccessibilityDelegate

Added interface:

```
IUIScrollViewDelegate
```

### Type Changed: MonoTouch.UIKit.IUISearchBarDelegate

Added interface:

```
IUIBarPositioningDelegate
```

### Type Changed: MonoTouch.UIKit.IUITableViewDelegate

Added interface:

```
IUIScrollViewDelegate
```

### Type Changed: MonoTouch.UIKit.IUITextDocumentProxy

Added interfaces:

```
IUIKeyInput
	IUITextInputTraits
```

### Type Changed: MonoTouch.UIKit.IUITextInputTraits

Added interfaces:

```
MonoTouch.ObjCRuntime.INativeObject
	System.IDisposable
```

Added property:

```
public virtual UITextSpellCheckingType SpellCheckingType { get; set; }
```

### Type Changed: MonoTouch.UIKit.IUITextViewDelegate

Added interface:

```
IUIScrollViewDelegate
```

### Type Changed: MonoTouch.UIKit.IUIToolbarDelegate

Added interface:

```
IUIBarPositioningDelegate
```

### Type Changed: MonoTouch.UIKit.IUIVideoEditorControllerDelegate

Added interface:

```
IUINavigationControllerDelegate
```

### Type Changed: MonoTouch.UIKit.NSLayoutConstraint

Added method:

```
public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, object[] viewsAndMetrics);
```

### Type Changed: MonoTouch.UIKit.UIAccessibilityCustomAction

Added constructor:

```
public UIAccessibilityCustomAction (string name, System.Func<UIAccessibilityCustomAction,System.Boolean> probe);
```

### Type Changed: MonoTouch.UIKit.UIActivityViewControllerCompletion

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSObject[] FIXME_FIND_THE_RIGHT_STRONG_TYPE, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSObject[] FIXME_FIND_THE_RIGHT_STRONG_TYPE, MonoTouch.Foundation.NSError error);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSExtensionItem[] returnedItems, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSExtensionItem[] returnedItems, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.UIKit.UIDocument

Added interface:

```
MonoTouch.Foundation.INSFilePresenter
```

Added properties:

```
public virtual MonoTouch.Foundation.NSOperationQueue PesentedItemOperationQueue { get; }
	public virtual MonoTouch.Foundation.NSUrl PresentedItemURL { get; }
```

Added methods:

```
public virtual void AccommodatePresentedItemDeletion (System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void AccommodatePresentedSubitemDeletion (MonoTouch.Foundation.NSUrl url, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void PresentedItemChanged ();
	public virtual void PresentedItemGainedVersion (MonoTouch.Foundation.NSFileVersion version);
	public virtual void PresentedItemLostVersion (MonoTouch.Foundation.NSFileVersion version);
	public virtual void PresentedItemMoved (MonoTouch.Foundation.NSUrl newURL);
	public virtual void PresentedItemResolveConflictVersion (MonoTouch.Foundation.NSFileVersion version);
	public virtual void PresentedSubitemAppeared (MonoTouch.Foundation.NSUrl atUrl);
	public virtual void PresentedSubitemChanged (MonoTouch.Foundation.NSUrl url);
	public virtual void PresentedSubitemGainedVersion (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSFileVersion version);
	public virtual void PresentedSubitemLostVersion (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSFileVersion version);
	public virtual void PresentedSubitemMoved (MonoTouch.Foundation.NSUrl oldURL, MonoTouch.Foundation.NSUrl newURL);
	public virtual void PresentedSubitemResolvedConflictVersion (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSFileVersion version);
	public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
	public virtual void SavePresentedItemChanges (System.Action<MonoTouch.Foundation.NSError> completionHandler);
```

### Type Changed: MonoTouch.UIKit.UIManagedDocument

Added interface:

```
MonoTouch.Foundation.INSFilePresenter
```

### Type Changed: MonoTouch.UIKit.UIPopoverPresentationController

Removed property:

```
public virtual System.Drawing.SizeF PopoverContentSize { get; set; }
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interface:

```
IUITextInputTraits
```

### Type Changed: MonoTouch.UIKit.UITextDocumentProxy

Added interfaces:

```
IUIKeyInput
	IUITextInputTraits
```

### Type Changed: MonoTouch.UIKit.UITextField

Added interfaces:

```
IUIKeyInput
	IUITextInput
```

### Type Changed: MonoTouch.UIKit.UITextView

Added interfaces:

```
IUIKeyInput
	IUITextInput
```

### Type Changed: MonoTouch.UIKit.UIViewController

Removed properties:

```
public virtual UILayoutSupport LeftLayoutGuide { get; }
	public virtual UILayoutSupport RightLayoutGuide { get; }
```

### New Type MonoTouch.UIKit.IUIKeyInput

```
public interface IUIKeyInput : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUITextInputTraits {
	// properties
	public virtual bool HasText { get; }
	// methods
	public virtual void DeleteBackward ();
	public virtual void InsertText (string text);
}
```

### New Type MonoTouch.UIKit.IUITextInput

```
public interface IUITextInput : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIKeyInput, IUITextInputTraits {
	// properties
	public virtual UITextPosition BeginningOfDocument { get; }
	public virtual UITextPosition EndOfDocument { get; }
	public virtual UITextRange MarkedTextRange { get; }
	public virtual MonoTouch.Foundation.NSDictionary MarkedTextStyle { get; set; }
	public virtual UITextRange SelectedTextRange { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakInputDelegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakTokenizer { get; }
	// methods
	public virtual MonoTouch.Foundation.NSComparisonResult ComparePosition (UITextPosition first, UITextPosition second);
	public virtual UITextWritingDirection GetBaseWritingDirection (UITextPosition forPosition, UITextStorageDirection direction);
	public virtual System.Drawing.RectangleF GetCaretRectForPosition (UITextPosition position);
	public virtual UITextRange GetCharacterRange (UITextPosition byExtendingPosition, UITextLayoutDirection direction);
	public virtual UITextRange GetCharacterRangeAtPoint (System.Drawing.PointF point);
	public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point);
	public virtual UITextPosition GetClosestPositionToPoint (System.Drawing.PointF point, UITextRange withinRange);
	public virtual System.Drawing.RectangleF GetFirstRectForRange (UITextRange range);
	public virtual int GetOffsetFromPosition (UITextPosition fromPosition, UITextPosition toPosition);
	public virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextLayoutDirection inDirection, int offset);
	public virtual UITextPosition GetPosition (UITextPosition fromPosition, int offset);
	public virtual UITextPosition GetPositionWithinRange (UITextRange range, UITextLayoutDirection direction);
	public virtual UITextSelectionRect[] GetSelectionRects (UITextRange range);
	public virtual UITextRange GetTextRange (UITextPosition fromPosition, UITextPosition toPosition);
	public virtual void ReplaceText (UITextRange range, string text);
	public virtual void SetBaseWritingDirectionforRange (UITextWritingDirection writingDirection, UITextRange range);
	public virtual void SetMarkedText (string markedText, MonoTouch.Foundation.NSRange selectedRange);
	public virtual string TextInRange (UITextRange range);
	public virtual void UnmarkText ();
}
```

### New Type MonoTouch.UIKit.NSFilePresenterReacquirer

```
public sealed delegate NSFilePresenterReacquirer : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSFilePresenterReacquirer (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.Action reacquirer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.Action reacquirer);
}
```

### New Type MonoTouch.UIKit.UIKeyInput_Extensions

```
public static class UIKeyInput_Extensions {
}
```

### New Type MonoTouch.UIKit.UITextInput_Extensions

```
public static class UITextInput_Extensions {
	// methods
	public static void DictationRecognitionFailed (IUITextInput This);
	public static void DictationRecordingDidEnd (IUITextInput This);
	public static int GetCharacterOffsetOfPosition (IUITextInput This, UITextPosition position, UITextRange range);
	public static System.Drawing.RectangleF GetFrameForDictationResultPlaceholder (IUITextInput This, MonoTouch.Foundation.NSObject placeholder);
	public static UITextPosition GetPosition (IUITextInput This, UITextRange withinRange, int atCharacterOffset);
	public static MonoTouch.Foundation.NSDictionary GetTextStyling (IUITextInput This, UITextPosition atPosition, UITextStorageDirection inDirection);
	public static void InsertDictationResult (IUITextInput This, MonoTouch.Foundation.NSArray dictationResult);
	public static MonoTouch.Foundation.NSObject InsertDictationResultPlaceholder (IUITextInput This);
	public static void RemoveDictationResultPlaceholder (IUITextInput This, MonoTouch.Foundation.NSObject placeholder, bool willInsertResult);
	public static bool ShouldChangeTextInRange (IUITextInput This, UITextRange inRange, string replacementText);
}
```

### New Type MonoTouch.UIKit.UITextInputTraits_Extensions

```
public static class UITextInputTraits_Extensions {
}
```

   


 <hr>
