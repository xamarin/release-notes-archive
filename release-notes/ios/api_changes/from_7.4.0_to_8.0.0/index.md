---
id: 9605B130-FEA1-4C53-B49D-E6C693A2C1E2
title: "From 7.4.0 to 8.0.0"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string CoreServicesLibrary = "/System/Library/Frameworks/CoreServices.framework/CoreServices";
	public static const string Version = "7.4.0";
```

Added fields:

```
public static const string AVKitLibrary = "/System/Library/Frameworks/AVKit.framework/AVKit";
	public static const string CloudKitLibrary = "/System/Library/Frameworks/CloudKit.framework/CloudKit";
	public static const string CoreAudioKitLibrary = "/System/Library/Frameworks/CoreAudioKit.framework/CoreAudioKit";
	public static const string CoreMotionLibrary = "System/Library/Frameworks/CoreMotion.framework/CoreMotion";
	public static const string CoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
	public static const string HealthKitLibrary = "/System/Library/Frameworks/HealthKit.framework/HealthKit";
	public static const string HomeKitLibrary = "/System/Library/Frameworks/HomeKit.framework/HomeKit";
	public static const string LocalAuthenticationLibrary = "/System/Library/Frameworks/LocalAuthentication.framework/LocalAuthentication";
	public static const string MetalLibrary = "/System/Library/Frameworks/Metal.framework/Metal";
	public static const string PhotosLibrary = "/System/Library/Frameworks/Photos.framework/Photos";
	public static const string PhotosUILibrary = "/System/Library/Frameworks/PhotosUI.framework/PhotosUI";
	public static const string PushKitLibrary = "/System/Library/Frameworks/PushKit.framework/PushKit";
	public static const string SceneKitLibrary = "/System/Library/Frameworks/SceneKit.framework/SceneKit";
	public static const string Version = "8.0.0";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
```

## Namespace MonoTouch.Accounts

### Type Changed: MonoTouch.Accounts.ACErrorCode

Added values:

```
CoreDataSaveFailed = 18,
	DeniedByPlugin = 17,
	FailedSerializingAccountInfo = 19,
	InvalidCommand = 20,
	MissingMessageID = 21,
```

## Namespace MonoTouch.AddressBook

### Type Changed: MonoTouch.AddressBook.ABPerson

Added methods:

```
public static ABPropertyType GetPropertyType (int propertyId);
	public static string LocalizedPropertyName (int propertyId);
```

### Type Changed: MonoTouch.AddressBook.ABRecord

Added method:

```
public static ABRecord FromHandle (System.IntPtr handle);
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added properties:

```
public virtual MonoTouch.Foundation.NSPredicate PredicateForEnablingPerson { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate PredicateForSelectionOfPerson { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate PredicateForSelectionOfProperty { get; set; }
```

Added methods:

```
public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate

Added methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson);
	public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions

Added methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson);
	public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABPerson selectedPerson, int propertyId, System.IntPtr abMultiValueIdentifier);
```

### Type Changed: MonoTouch.AddressBookUI.ABPersonViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.AddressBookUI.IABPeoplePickerNavigationControllerDelegate

Added interface:

```
MonoTouch.UIKit.IUINavigationControllerDelegate
```

### New Type MonoTouch.AddressBookUI.ABPersonPredicateKey

```
public static class ABPersonPredicateKey {
	// properties
	public static MonoTouch.Foundation.NSString Birthday { get; }
	public static MonoTouch.Foundation.NSString Dates { get; }
	public static MonoTouch.Foundation.NSString DepartmentName { get; }
	public static MonoTouch.Foundation.NSString EmailAddresses { get; }
	public static MonoTouch.Foundation.NSString FamilyName { get; }
	public static MonoTouch.Foundation.NSString GivenName { get; }
	public static MonoTouch.Foundation.NSString InstantMessageAddresses { get; }
	public static MonoTouch.Foundation.NSString JobTitle { get; }
	public static MonoTouch.Foundation.NSString MiddleName { get; }
	public static MonoTouch.Foundation.NSString NamePrefix { get; }
	public static MonoTouch.Foundation.NSString NameSuffix { get; }
	public static MonoTouch.Foundation.NSString Nickname { get; }
	public static MonoTouch.Foundation.NSString Note { get; }
	public static MonoTouch.Foundation.NSString OrganizationName { get; }
	public static MonoTouch.Foundation.NSString PhoneNumbers { get; }
	public static MonoTouch.Foundation.NSString PhoneticFamilyName { get; }
	public static MonoTouch.Foundation.NSString PhoneticGivenName { get; }
	public static MonoTouch.Foundation.NSString PhoneticMiddleName { get; }
	public static MonoTouch.Foundation.NSString PostalAddresses { get; }
	public static MonoTouch.Foundation.NSString PreviousFamilyName { get; }
	public static MonoTouch.Foundation.NSString RelatedNames { get; }
	public static MonoTouch.Foundation.NSString SocialProfiles { get; }
	public static MonoTouch.Foundation.NSString UrlAddresses { get; }
}
```

## Namespace MonoTouch.AudioToolbox

### Type Changed: MonoTouch.AudioToolbox.AudioFile

Obsoleted method:

```
[Obsolete ("Use ReadPacketData instead")]
	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, System.IntPtr buffer);
```

### Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added value:

```
AMRWideBand = 1935767394,
```

### Type Changed: MonoTouch.AudioToolbox.AudioQueueStatus

Added value:

```
BufferEnqueuedTwice = -66666,
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

### Type Changed: MonoTouch.AudioUnit.AudioTypeEffect

Added value:

```
SampleDelay = 1935961209,
```

### Type Changed: MonoTouch.AudioUnit.AudioTypeMixer

Added value:

```
Spacial = 862217581,
```

Obsoleted field:

```
[Obsolete ("Replaced by Spacial")]
	Embedded3D = 862217581,
```

### Type Changed: MonoTouch.AudioUnit.AudioTypeMusicDevice

Added value:

```
MidiSynth = 1836284270,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitParameterFlag

Added value:

```
OmitFromPresets = 8192,
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
	ReverbFilterEnable = 18,
	ReverbFilterType = 17,
	RoundTripAacEncodingStrategy = 1,
	RoundTripAacFormat = 0,
	RoundTripAacRateOrQuality = 2,
	SpacialMixerAzimuth = 0,
	SpatialAzimuth = 0,
	SpatialDistance = 2,
	SpatialElevation = 1,
	SpatialEnable = 5,
	SpatialGain = 3,
	SpatialGlobalReverbGain = 9,
	SpatialMaxGain = 7,
	SpatialMinGain = 6,
	SpatialObstructionAttenuation = 11,
	SpatialOcclusionAttenuation = 10,
	SpatialPlaybackRate = 4,
	SpatialReverbBlend = 8,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added values:

```
AttenuationCurve = 3013,
	BankName = 1007,
	DistanceParams = 3010,
	InstrumentCount = 1000,
	InstrumentName = 1001,
	InstrumentNumber = 1004,
	MidiSynthEnablePreload = 4119,
	ParameterIDName = 34,
	ParameterStringFromValue = 33,
	ParameterValueFromString = 38,
	RenderingFlags = 3003,
	ReverbRoomType = 10,
	SoundBankURL = 1100,
	SpatializationAlgorithm = 3000,
	UsesInternalReverb = 1005,
```

### New Type MonoTouch.AudioUnit.AudioComponentDescriptionNative

```
public struct AudioComponentDescriptionNative {
	// constructors
	public AudioComponentDescriptionNative (AudioComponentDescription other);
	// fields
	public AudioComponentFlag ComponentFlags;
	public int ComponentFlagsMask;
	public AudioComponentManufacturerType ComponentManufacturer;
	public int ComponentSubType;
	public AudioComponentType ComponentType;
}
```

### New Type MonoTouch.AudioUnit.ScheduledAudioSliceFlag

```
[Serializable]
[Flags]
public enum ScheduledAudioSliceFlag {
	BeganToRender = 2,
	BeganToRenderLate = 4,
	Complete = 1,
	Interrupt = 16,
	InterruptAtLoop = 32,
	Loop = 8,
}
```

### New Type MonoTouch.AudioUnit.SpatialMixerAttenuation

```
[Serializable]
public enum SpatialMixerAttenuation {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
```

### New Type MonoTouch.AudioUnit.SpatialMixerRenderingFlags

```
[Serializable]
[Flags]
public enum SpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAsset

Added property:

```
public virtual AVMetadataItem[] Metadata { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

Added properties:

```
public virtual bool CanPerformMultiplePassesOverSourceMediaData { get; set; }
	public virtual MonoTouch.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVAssetReaderOutput

Added property:

```
public virtual bool SupportsRandomAccess { get; set; }
```

Added methods:

```
public virtual void MarkConfigurationAsFinal ();
	public virtual void ResetForReadingTimeRanges (MonoTouch.Foundation.NSValue[] timeRanges);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate

Added methods:

```
public virtual void DidCancelAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoTouch.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public virtual bool ShouldWaitForRenewalOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public virtual bool ShouldWaitForResponseToAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoTouch.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added methods:

```
public static void DidCancelAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoTouch.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public static bool ShouldWaitForRenewalOfRequestedResource (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public static bool ShouldWaitForResponseToAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoTouch.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingContentInformationRequest

Added property:

```
public virtual MonoTouch.Foundation.NSDate RenewalDate { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingDataRequest

Obsoleted constructor:

```
[Obsolete ("Type is not meant to be created by user code")]
	public AVAssetResourceLoadingDataRequest ();
```

### Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Added properties:

```
public virtual AVMetadataItem[] Metadata { get; }
	public virtual bool RequiresFrameReordering { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAssetTrackTrackAssociation

Added property:

```
public static MonoTouch.Foundation.NSString MetadataReferent { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAssetWriter

Added properties:

```
public virtual MonoTouch.Foundation.NSString[] AvailableMediaTypes { get; }
	public virtual MonoTouch.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

Added properties:

```
public virtual bool CanPerformMultiplePasses { get; }
	public virtual AVAssetWriterInputPassDescription CurrentPassDescription { get; }
	public virtual bool PerformsMultiPassEncodingIfSupported { get; set; }
	public virtual int PreferredMediaChunkAlignment { get; set; }
	public virtual MonoTouch.CoreMedia.CMTime PreferredMediaChunkDuration { get; set; }
	public virtual MonoTouch.Foundation.NSUrl SampleReferenceBaseUrl { get; set; }
```

Added methods:

```
public virtual void MarkCurrentPassAsFinished ();
	public virtual void SetPassHandler (MonoTouch.CoreFoundation.DispatchQueue queue, System.Action passHandler);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Added properties:

```
public virtual AVAudioSessionRecordPermission RecordPermission { get; }
	public virtual bool SecondaryAudioShouldBeSilencedHint { get; }
	public static MonoTouch.Foundation.NSString SilenceSecondaryAudioHintNotification { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSession.Notifications

Added method:

```
public static MonoTouch.Foundation.NSObject ObserveSilenceSecondaryAudioHint (System.EventHandler<AVAudioSessionSecondaryAudioHintEventArgs> handler);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSessionErrorCode

Added value:

```
InsufficientPriority = 561017449,
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

Added constructors:

```
public AVCaptureConnection (AVCaptureInputPort[] inputPorts, AVCaptureOutput output);
	public AVCaptureConnection (AVCaptureInputPort inputPort, AVCaptureVideoPreviewLayer layer);
```

Added properties:

```
public virtual AVCaptureVideoStabilizationMode ActiveVideoStabilizationMode { get; }
	public virtual AVCaptureVideoStabilizationMode PreferredVideoStabilizationMode { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added properties:

```
public virtual bool AutomaticallyAdjustsVideoHdrEnabled { get; set; }
	public virtual AVCaptureWhiteBalanceGains DeviceWhiteBalanceGains { get; }
	public virtual MonoTouch.CoreMedia.CMTime ExposureDuration { get; }
	public static MonoTouch.CoreMedia.CMTime ExposureDurationCurrent { get; }
	public virtual float ExposureTargetBias { get; }
	public static float ExposureTargetBiasCurrent { get; }
	public virtual float ExposureTargetOffset { get; }
	public static float FocusModeLensPositionCurrent { get; }
	public virtual AVCaptureWhiteBalanceGains GrayWorldDeviceWhiteBalanceGains { get; }
	public virtual float ISO { get; }
	public static float ISOCurrent { get; }
	public virtual float LensAperture { get; }
	public virtual float LensPosition { get; }
	public static float LensPositionCurrent { get; }
	public virtual float MaxExposureTargetBias { get; }
	public virtual float MaxWhiteBalanceGain { get; }
	public virtual float MinExposureTargetBias { get; }
	public virtual bool SubjectAreaChangeMonitoringEnabled { get; set; }
	public virtual bool VideoHdrEnabled { get; set; }
	public static AVCaptureWhiteBalanceGains WhiteBalanceGainsCurrent { get; }
```

Added methods:

```
public virtual AVCaptureWhiteBalanceChromaticityValues GetChromaticityValues (AVCaptureWhiteBalanceGains whiteBalanceGains);
	public virtual AVCaptureWhiteBalanceGains GetDeviceWhiteBalanceGains (AVCaptureWhiteBalanceChromaticityValues chromaticityValues);
	public virtual AVCaptureWhiteBalanceGains GetDeviceWhiteBalanceGains (AVCaptureWhiteBalanceTemperatureAndTintValues tempAndTintValues);
	public virtual AVCaptureWhiteBalanceTemperatureAndTintValues GetTemperatureAndTintValues (AVCaptureWhiteBalanceGains whiteBalanceGains);
	public virtual void LockExposure (MonoTouch.CoreMedia.CMTime duration, float ISO, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> LockExposureAsync (MonoTouch.CoreMedia.CMTime duration, float ISO);
	public virtual void SetExposureTargetBias (float bias, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetExposureTargetBiasAsync (float bias);
	public virtual void SetFocusModeLocked (float lensPosition, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetFocusModeLockedAsync (float lensPosition);
	public virtual void SetWhiteBalanceModeLockedWithDeviceWhiteBalanceGains (AVCaptureWhiteBalanceGains whiteBalanceGains, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetWhiteBalanceModeLockedWithDeviceWhiteBalanceGainsAsync (AVCaptureWhiteBalanceGains whiteBalanceGains);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceFormat

Added properties:

```
public virtual AVCaptureAutoFocusSystem AutoFocusSystem { get; }
	public virtual System.Drawing.Size HighResolutionStillImageDimensions { get; }
	public virtual MonoTouch.CoreMedia.CMTime MaxExposureDuration { get; }
	public virtual float MaxISO { get; }
	public virtual MonoTouch.CoreMedia.CMTime MinExposureDuration { get; }
	public virtual float MinISO { get; }
	public virtual bool videoHDRSupportedVideoHDREnabled { get; }
```

Added method:

```
public virtual bool IsVideoStabilizationModeSupported (AVCaptureVideoStabilizationMode mode);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDevicePosition

Added value:

```
Unspecified = 0,
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureExposureMode

Added value:

```
Custom = 3,
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureFileOutput

Added method:

```
public void StartRecordingToOutputFile (MonoTouch.Foundation.NSUrl outputFileUrl, System.Action<MonoTouch.Foundation.NSObject[]> startRecordingFromConnections, System.Action<MonoTouch.Foundation.NSObject[],MonoTouch.Foundation.NSError> finishedRecording);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureFocusMode

Added values:

```
AutoFocus = 1,
	ContinuousAutoFocus = 2,
	Locked = 0,
```

Obsoleted fields:

```
[Obsolete ("use AutoFocus instead")]
	ModeAutoFocus = 1,

	[Obsolete ("use ContinuousAutoFocus instead")]
	ModeContinuousAutoFocus = 2,

	[Obsolete ("use Locked instead")]
	ModeLocked = 0,
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureSession

Added methods:

```
public virtual void AddConnection (AVCaptureConnection connection);
	public virtual void AddInputWithNoConnections (AVCaptureInput input);
	public virtual void AddOutputWithNoConnections (AVCaptureOutput output);
	public virtual bool CanAddConnection (AVCaptureConnection connection);
	public virtual void RemoveConnection (AVCaptureConnection connection);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput

Added properties:

```
public virtual bool HighResolutionStillImageOutputEnabled { get; set; }
	public virtual uint MaxBracketedCaptureStillImageCount { get; }
```

Added methods:

```
public virtual void CaptureStillImageBracket (AVCaptureConnection connection, AVCaptureBracketedStillImageSettings[] settings, System.Action<MonoTouch.CoreMedia.CMSampleBuffer,MonoTouch.AVFoundation.AVCaptureBracketedStillImageSettings,MonoTouch.Foundation.NSError> imageHandler);
	public virtual void PrepareToCaptureStillImageBracket (AVCaptureConnection connection, AVCaptureBracketedStillImageSettings[] settings, System.Action<System.Boolean,MonoTouch.Foundation.NSError> handler);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer

Added methods:

```
public static AVCaptureVideoPreviewLayer CreateWithNoConnection (AVCaptureSession session);
	public virtual void SetSessionWithNoConnection (AVCaptureSession session);
```

### Type Changed: MonoTouch.AVFoundation.AVError

Added values:

```
FailedToParse2 = -11853,
	FileTypeDoesNotSupportSampleReferences = -11854,
	UndecodableMediaData = -11855,
```

### Type Changed: MonoTouch.AVFoundation.AVMediaSelectionGroup

Added property:

```
public virtual AVMediaSelectionOption DefaultOption { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVMetadata

Added properties:

```
public static MonoTouch.Foundation.NSString FormatHlsMetadata { get; }
	public static MonoTouch.Foundation.NSString IcyMetadataKeyStreamTitle { get; }
	public static MonoTouch.Foundation.NSString IcyMetadataKeyStreamUrl { get; }
	public static MonoTouch.Foundation.NSString IsoUserDataKeyTaggedCharacteristic { get; }
	public static MonoTouch.Foundation.NSString KeySpaceIcy { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVMetadataFaceObject

Added interface:

```
MonoTouch.Foundation.INSCopying
```

Added method:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVMetadataItem

Removed properties:

```
public virtual MonoTouch.CoreMedia.CMTime Duration { get; }
	public virtual MonoTouch.Foundation.NSDictionary ExtraAttributes { get; }
	public virtual string KeySpace { get; }
	public virtual MonoTouch.Foundation.NSLocale Locale { get; }
	public virtual MonoTouch.CoreMedia.CMTime Time { get; }
	public virtual MonoTouch.Foundation.NSObject Value { get; }
```

Added properties:

```
public virtual MonoTouch.Foundation.NSString DataType { get; set; }
	public virtual MonoTouch.CoreMedia.CMTime Duration { get; set; }
	public virtual string ExtendedLanguageTag { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual MonoTouch.Foundation.NSLocale Locale { get; set; }
	public virtual MonoTouch.Foundation.NSString MetadataIdentifier { get; set; }
	public virtual MonoTouch.CoreMedia.CMTime Time { get; set; }
	public virtual MonoTouch.Foundation.NSObject Value { get; set; }
```

Added methods:

```
public static AVMetadataItem[] FilterWithIdentifier (AVMetadataItem[] metadataItems, MonoTouch.Foundation.NSString metadataIdentifer);
	public static MonoTouch.Foundation.NSObject GetKeyForIdentifier (MonoTouch.Foundation.NSString identifier);
	public static MonoTouch.Foundation.NSString GetKeySpaceForIdentifier (MonoTouch.Foundation.NSString identifier);
	public static MonoTouch.Foundation.NSString GetMetadataIdentifier (MonoTouch.Foundation.NSObject key, MonoTouch.Foundation.NSString keySpace);
```

### Type Changed: MonoTouch.AVFoundation.AVMetadataObject

Added properties:

```
public static MonoTouch.Foundation.NSString TypeDataMatrixCode { get; }
	public static MonoTouch.Foundation.NSString TypeInterleaved2of5Code { get; }
	public static MonoTouch.Foundation.NSString TypeITF14Code { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVMutableMetadataItem

Removed properties:

```
public virtual MonoTouch.CoreMedia.CMTime Duration { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual MonoTouch.Foundation.NSLocale Locale { get; set; }
	public virtual MonoTouch.CoreMedia.CMTime Time { get; set; }
	public virtual MonoTouch.Foundation.NSObject Value { get; set; }
```

Added properties:

```
public override MonoTouch.Foundation.NSString DataType { get; set; }
	public override MonoTouch.CoreMedia.CMTime Duration { get; set; }
	public override string ExtendedLanguageTag { get; set; }
	public override MonoTouch.Foundation.NSDictionary ExtraAttributes { get; set; }
	public override string KeySpace { get; set; }
	public override MonoTouch.Foundation.NSLocale Locale { get; set; }
	public override MonoTouch.Foundation.NSString MetadataIdentifier { get; set; }
	public override MonoTouch.CoreMedia.CMTime Time { get; set; }
	public override MonoTouch.Foundation.NSObject Value { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Added property:

```
public virtual double PreferredPeakBitRate { get; set; }
```

### Type Changed: MonoTouch.AVFoundation.AVTimedMetadataGroup

Added constructor:

```
public AVTimedMetadataGroup (MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer);
```

Added method:

```
public virtual MonoTouch.CoreMedia.CMFormatDescription CopyFormatDescription ();
```

### Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Removed constructor:

```
public AVUrlAsset (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
```

Added constructor:

```
public AVUrlAsset (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
```

Added property:

```
public static MonoTouch.Foundation.NSString HttpCookiesKey { get; }
```

Removed method:

```
public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
```

Added method:

```
public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
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

### New Type MonoTouch.AVFoundation.AVAssetReaderOutputMetadataAdaptor

```
public class AVAssetReaderOutputMetadataAdaptor : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderOutputMetadataAdaptor (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderOutputMetadataAdaptor (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderOutputMetadataAdaptor (System.IntPtr handle);
	public AVAssetReaderOutputMetadataAdaptor (AVAssetReaderTrackOutput trackOutput);
	// properties
	public virtual AVAssetReaderTrackOutput AssetReaderTrackOutput { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static AVAssetReaderOutputMetadataAdaptor Create (AVAssetReaderTrackOutput trackOutput);
	protected override void Dispose (bool disposing);
	public virtual AVTimedMetadataGroup NextTimedMetadataGroup ();
}
```

### New Type MonoTouch.AVFoundation.AVAssetReaderSampleReferenceOutput

```
public class AVAssetReaderSampleReferenceOutput : MonoTouch.AVFoundation.AVAssetReaderOutput, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderSampleReferenceOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderSampleReferenceOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderSampleReferenceOutput (System.IntPtr handle);
	public AVAssetReaderSampleReferenceOutput (AVAssetTrack track);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAssetTrack Track { get; }
	// methods
	public static AVAssetReaderSampleReferenceOutput Create (AVAssetTrack track);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.AVFoundation.AVAssetResourceRenewalRequest

```
public class AVAssetResourceRenewalRequest : MonoTouch.AVFoundation.AVAssetResourceLoadingRequest, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceRenewalRequest (MonoTouch.Foundation.NSCoder coder);
	public AVAssetResourceRenewalRequest (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetResourceRenewalRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAssetWriterInputMetadataAdaptor

```
public class AVAssetWriterInputMetadataAdaptor : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputMetadataAdaptor (MonoTouch.Foundation.NSCoder coder);
	public AVAssetWriterInputMetadataAdaptor (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetWriterInputMetadataAdaptor (System.IntPtr handle);
	public AVAssetWriterInputMetadataAdaptor (AVAssetWriterInput assetWriterInput);
	// properties
	public virtual AVAssetWriterInput AssetWriterInput { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual bool AppendTimedMetadataGroup (AVTimedMetadataGroup timedMetadataGroup);
	public static AVAssetWriterInputMetadataAdaptor Create (AVAssetWriterInput input);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.AVFoundation.AVAssetWriterInputPassDescription

```
public class AVAssetWriterInputPassDescription : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputPassDescription ();
	public AVAssetWriterInputPassDescription (MonoTouch.Foundation.NSCoder coder);
	public AVAssetWriterInputPassDescription (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetWriterInputPassDescription (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSValue[] SourceTimeRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.AVFoundation.AVAudio3DAngularOrientation

```
public struct AVAudio3DAngularOrientation {
	// fields
	public float Pitch;
	public float Roll;
	public float Yaw;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DAngularOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DAngularOrientation left, AVAudio3DAngularOrientation right);
	public static bool op_Inequality (AVAudio3DAngularOrientation left, AVAudio3DAngularOrientation right);
	public override string ToString ();
}
```

### New Type MonoTouch.AVFoundation.AVAudio3DMixing

```
public abstract class AVAudio3DMixing : MonoTouch.Foundation.NSObject, IAVAudio3DMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudio3DMixing ();
	public AVAudio3DMixing (MonoTouch.Foundation.NSCoder coder);
	public AVAudio3DMixing (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudio3DMixing (System.IntPtr handle);
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudio3DMixing_Extensions

```
public static class AVAudio3DMixing_Extensions {
}
```

### New Type MonoTouch.AVFoundation.AVAudio3DMixingRenderingAlgorithm

```
[Serializable]
public enum AVAudio3DMixingRenderingAlgorithm {
	EqualPowerPanning = 0,
	HRTF = 2,
	SoundField = 3,
	SphericalHead = 1,
	StereoPassThrough = 5,
}
```

### New Type MonoTouch.AVFoundation.AVAudio3DVectorOrientation

```
public struct AVAudio3DVectorOrientation {
	// constructors
	public AVAudio3DVectorOrientation (OpenTK.Vector3 forward, OpenTK.Vector3 up);
	// fields
	public OpenTK.Vector3 Forward;
	public OpenTK.Vector3 Up;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DVectorOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public static bool op_Inequality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public override string ToString ();
}
```

### New Type MonoTouch.AVFoundation.AVAudioBuffer

```
public class AVAudioBuffer : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioBuffer (MonoTouch.Foundation.NSCoder coder);
	public AVAudioBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioBuffer (System.IntPtr handle);
	// properties
	public MonoTouch.AudioToolbox.AudioBuffers AudioBufferList { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat Format { get; }
	public MonoTouch.AudioToolbox.AudioBuffers MutableAudioBufferList { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.AVFoundation.AVAudioChannelLayout

```
public class AVAudioChannelLayout : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioChannelLayout (MonoTouch.AudioToolbox.AudioChannelLayout layout);
	public AVAudioChannelLayout ();
	public AVAudioChannelLayout (MonoTouch.Foundation.NSCoder coder);
	public AVAudioChannelLayout (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioChannelLayout (System.IntPtr handle);
	public AVAudioChannelLayout (uint layoutTag);
	// properties
	public virtual uint ChannelCount { get; }
	public override System.IntPtr ClassHandle { get; }
	public MonoTouch.AudioToolbox.AudioChannelLayout Layout { get; }
	public virtual uint LayoutTag { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioChannelLayout a, AVAudioChannelLayout b);
	public static bool op_Inequality (AVAudioChannelLayout a, AVAudioChannelLayout b);
}
```

### New Type MonoTouch.AVFoundation.AVAudioCommonFormat

```
[Serializable]
public enum AVAudioCommonFormat {
	Other = 0,
	PCMFloat32 = 1,
	PCMFloat64 = 2,
	PCMInt16 = 3,
	PCMInt32 = 4,
}
```

### New Type MonoTouch.AVFoundation.AVAudioEngine

```
public class AVAudioEngine : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEngine ();
	public AVAudioEngine (MonoTouch.Foundation.NSCoder coder);
	public AVAudioEngine (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioEngine (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual AVAudioInputNode InputNode { get; }
	public virtual AVAudioMixerNode MainMixerNode { get; }
	public virtual MonoTouch.AudioToolbox.MusicSequence MusicSequence { get; set; }
	public virtual AVAudioOutputNode OutputNode { get; }
	public virtual bool Running { get; }
	// methods
	public virtual void AttachNode (AVAudioNode node);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, uint sourceBus, uint targetBus, AVAudioFormat format);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, AVAudioFormat format);
	public virtual void DetachNode (AVAudioNode node);
	public virtual void DisconnectNodeInput (AVAudioNode node, uint bus);
	public virtual void DisconnectNodeInput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node, uint bus);
	protected override void Dispose (bool disposing);
	public virtual void Pause ();
	public virtual void Prepare ();
	public virtual void Reset ();
	public virtual bool StartAndReturnError (out MonoTouch.Foundation.NSError outError);
	public virtual void Stop ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoTouch.Foundation.NSObject ObserveConfigurationChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type MonoTouch.AVFoundation.AVAudioEnvironmentDistanceAttenuationModel

```
[Serializable]
public enum AVAudioEnvironmentDistanceAttenuationModel {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
}
```

### New Type MonoTouch.AVFoundation.AVAudioEnvironmentDistanceAttenuationParameters

```
public class AVAudioEnvironmentDistanceAttenuationParameters : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoTouch.Foundation.NSCoder coder);
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentDistanceAttenuationParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationModel DistanceAttenuationModel { get; set; }
	public virtual float MaximumDistance { get; set; }
	public virtual float ReferenceDistance { get; set; }
	public virtual float RolloffFactor { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioEnvironmentNode

```
public class AVAudioEnvironmentNode : MonoTouch.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentNode ();
	public AVAudioEnvironmentNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioEnvironmentNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationParameters DistanceAttenuationParameters { get; }
	public virtual AVAudio3DAngularOrientation ListenerAngularOrientation { get; set; }
	public virtual OpenTK.Vector3 ListenerPosition { get; set; }
	public virtual AVAudio3DVectorOrientation ListenerVectorOrientation { get; set; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual AVAudioEnvironmentReverbParameters ReverbParameters { get; }
	public virtual float Volume { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject[] ApplicableRenderingAlgorithms ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.AVFoundation.AVAudioEnvironmentReverbParameters

```
public class AVAudioEnvironmentReverbParameters : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentReverbParameters (MonoTouch.Foundation.NSCoder coder);
	public AVAudioEnvironmentReverbParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentReverbParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enable { get; set; }
	public virtual AVAudioUnitEQFilterParameters FilterParameters { get; }
	public virtual float Level { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void LoadFactoryReverbPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type MonoTouch.AVFoundation.AVAudioFile

```
public class AVAudioFile : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFile ();
	public AVAudioFile (MonoTouch.Foundation.NSUrl fileUrl, AudioSettings settings, out MonoTouch.Foundation.NSError outError);
	public AVAudioFile (MonoTouch.Foundation.NSUrl fileUrl, AVAudioCommonFormat format, bool interleaved, out MonoTouch.Foundation.NSError outError);
	public AVAudioFile (MonoTouch.Foundation.NSUrl fileUrl, out MonoTouch.Foundation.NSError outError);
	public AVAudioFile (System.IntPtr handle);
	public AVAudioFile (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioFile (MonoTouch.Foundation.NSCoder coder);
	public AVAudioFile (MonoTouch.Foundation.NSUrl fileUrl, AudioSettings settings, AVAudioCommonFormat format, bool interleaved, out MonoTouch.Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat FileFormat { get; }
	public virtual long FramePosition { get; set; }
	public virtual long Length { get; }
	public virtual AVAudioFormat ProcessingFormat { get; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, out MonoTouch.Foundation.NSError outError);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, uint frames, out MonoTouch.Foundation.NSError outError);
	public virtual bool WriteFromBuffer (AVAudioPcmBuffer buffer, out MonoTouch.Foundation.NSError outError);
}
```

### New Type MonoTouch.AVFoundation.AVAudioFormat

```
public class AVAudioFormat : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFormat ();
	public AVAudioFormat (MonoTouch.Foundation.NSDictionary settings);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, bool interleaved, AVAudioChannelLayout layout);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, uint channels, bool interleaved);
	public AVAudioFormat (double sampleRate, AVAudioChannelLayout layout);
	public AVAudioFormat (double sampleRate, uint channels);
	public AVAudioFormat (ref MonoTouch.AudioToolbox.AudioStreamBasicDescription description, AVAudioChannelLayout layout);
	public AVAudioFormat (ref MonoTouch.AudioToolbox.AudioStreamBasicDescription description);
	public AVAudioFormat (System.IntPtr handle);
	public AVAudioFormat (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioFormat (MonoTouch.Foundation.NSCoder coder);
	public AVAudioFormat (AudioSettings settings);
	// properties
	public virtual uint ChannelCount { get; }
	public virtual AVAudioChannelLayout ChannelLayout { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioCommonFormat CommonFormat { get; }
	public virtual bool Interleaved { get; }
	public virtual double SampleRate { get; }
	public AudioSettings Settings { get; }
	public virtual bool Standard { get; }
	public virtual MonoTouch.AudioToolbox.AudioStreamBasicDescription StreamDescription { get; }
	public virtual MonoTouch.Foundation.NSDictionary WeakSettings { get; }
	// methods
	protected override void Dispose (bool disposing);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioFormat a, AVAudioFormat b);
	public static bool op_Inequality (AVAudioFormat a, AVAudioFormat b);
}
```

### New Type MonoTouch.AVFoundation.AVAudioInputNode

```
public class AVAudioInputNode : MonoTouch.AVFoundation.AVAudioIONode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioInputNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioInputNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioInputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioIONode

```
public class AVAudioIONode : MonoTouch.AVFoundation.AVAudioNode, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioIONode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioIONode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioIONode (System.IntPtr handle);
	// properties
	public virtual MonoTouch.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual double PresentationLatency { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioMixerNode

```
public class AVAudioMixerNode : MonoTouch.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioMixerNode ();
	public AVAudioMixerNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioMixerNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioMixerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioMixing_Extensions

```
public static class AVAudioMixing_Extensions {
}
```

### New Type MonoTouch.AVFoundation.AVAudioNode

```
public class AVAudioNode : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEngine Engine { get; }
	public virtual AVAudioTime LastRenderTime { get; }
	public virtual uint NumberOfInputs { get; }
	public virtual uint NumberOfOutputs { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual AVAudioFormat GetBusInputFormat (uint bus);
	public virtual AVAudioFormat GetBusOutputFormat (uint bus);
	public virtual string GetNameForInputBus (uint bus);
	public virtual string GetNameForOutputBus (uint bus);
	public virtual void InstallTapOnBus (uint bus, uint bufferSize, AVAudioFormat format, AVAudioNodeTapBlock tapBlock);
	public virtual void RemoveTapOnBus (uint bus);
	public virtual void Reset ();
}
```

### New Type MonoTouch.AVFoundation.AVAudioNodeTapBlock

```
public sealed delegate AVAudioNodeTapBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public AVAudioNodeTapBlock (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AVAudioPcmBuffer buffer, AVAudioTime when, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (AVAudioPcmBuffer buffer, AVAudioTime when);
}
```

### New Type MonoTouch.AVFoundation.AVAudioOutputNode

```
public class AVAudioOutputNode : MonoTouch.AVFoundation.AVAudioIONode, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioOutputNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioOutputNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioOutputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioPcmBuffer

```
public class AVAudioPcmBuffer : MonoTouch.AVFoundation.AVAudioBuffer, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPcmBuffer (MonoTouch.Foundation.NSCoder coder);
	public AVAudioPcmBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioPcmBuffer (System.IntPtr handle);
	public AVAudioPcmBuffer (AVAudioFormat format, uint frameCapacity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.IntPtr FloatChannelData { get; }
	public virtual uint FrameCapacity { get; }
	public virtual uint FrameLength { get; set; }
	public virtual System.IntPtr Int16ChannelData { get; }
	public virtual System.IntPtr Int32ChannelData { get; }
	public virtual uint Stride { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioPlayerNode

```
public class AVAudioPlayerNode : MonoTouch.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPlayerNode ();
	public AVAudioPlayerNode (MonoTouch.Foundation.NSCoder coder);
	public AVAudioPlayerNode (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioPlayerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual bool Playing { get; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
	// methods
	public virtual AVAudioTime GetNodeTimeFromPlayerTime (AVAudioTime playerTime);
	public virtual AVAudioTime GetPlayerTimeFromNodeTime (AVAudioTime nodeTime);
	public virtual void Pause ();
	public virtual void Play ();
	public virtual void PlayAtTime (AVAudioTime when);
	public virtual void PrepareWithFrameCount (uint frameCount);
	public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, System.Action completionHandler);
	public virtual void ScheduleBuffer (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options, System.Action completionHandler);
	public virtual void ScheduleFile (AVAudioFile file, AVAudioTime when, System.Action completionHandler);
	public virtual void ScheduleSegment (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when, System.Action completionHandler);
	public virtual void Stop ();
}
```

### New Type MonoTouch.AVFoundation.AVAudioPlayerNodeBufferOptions

```
[Serializable]
[Flags]
public enum AVAudioPlayerNodeBufferOptions {
	Interrupts = 2,
	InterruptsAtLoop = 4,
	Loops = 1,
}
```

### New Type MonoTouch.AVFoundation.AVAudioSessionRecordPermission

```
[Serializable]
public enum AVAudioSessionRecordPermission {
	Denied = 1684369017,
	Granted = 1735552628,
	Undetermined = 1970168948,
}
```

### New Type MonoTouch.AVFoundation.AVAudioSessionSecondaryAudioHintEventArgs

```
public class AVAudioSessionSecondaryAudioHintEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	// constructors
	public AVAudioSessionSecondaryAudioHintEventArgs (MonoTouch.Foundation.NSNotification notification);
	// properties
	public AVAudioSessionSilenceSecondaryAudioHintType Hint { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioSessionSilenceSecondaryAudioHintType

```
[Serializable]
public enum AVAudioSessionSilenceSecondaryAudioHintType {
	Begin = 1,
	End = 0,
}
```

### New Type MonoTouch.AVFoundation.AVAudioStereoMixing

```
public abstract class AVAudioStereoMixing : MonoTouch.Foundation.NSObject, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioStereoMixing ();
	public AVAudioStereoMixing (MonoTouch.Foundation.NSCoder coder);
	public AVAudioStereoMixing (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioStereoMixing (System.IntPtr handle);
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioStereoMixing_Extensions

```
public static class AVAudioStereoMixing_Extensions {
}
```

### New Type MonoTouch.AVFoundation.AVAudioTime

```
public class AVAudioTime : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioTime ();
	public AVAudioTime (long sampleTime, double sampleRate);
	public AVAudioTime (ulong hostTime);
	public AVAudioTime (ref MonoTouch.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public AVAudioTime (System.IntPtr handle);
	public AVAudioTime (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioTime (MonoTouch.Foundation.NSCoder coder);
	public AVAudioTime (ulong hostTime, long sampleTime, double sampleRate);
	// properties
	public virtual MonoTouch.AudioToolbox.AudioTimeStamp AudioTimeStamp { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual ulong HostTime { get; }
	public virtual bool HostTimeValid { get; }
	public virtual double SampleRate { get; }
	public virtual long SampleTime { get; }
	public virtual bool SampleTimeValid { get; }
	// methods
	public virtual AVAudioTime ExtrapolateTimeFromAnchor (AVAudioTime anchorTime);
	public static AVAudioTime FromAudioTimeStamp (ref MonoTouch.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public static AVAudioTime FromHostTime (ulong hostTime);
	public static AVAudioTime FromHostTime (ulong hostTime, long sampleTime, double sampleRate);
	public static AVAudioTime FromSampleTime (long sampleTime, double sampleRate);
	public static ulong HostTimeForSeconds (double seconds);
	public static double SecondsForHostTime (ulong hostTime);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnit

```
public class AVAudioUnit : MonoTouch.AVFoundation.AVAudioNode, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnit (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnit (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnit (System.IntPtr handle);
	// properties
	public virtual MonoTouch.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual uint Version { get; }
	// methods
	public virtual bool LoadAudioUnitPreset (MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitDelay

```
public class AVAudioUnitDelay : MonoTouch.AVFoundation.AVAudioUnitEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDelay ();
	public AVAudioUnitDelay (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitDelay (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitDelay (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DelayTime { get; set; }
	public virtual float Feedback { get; set; }
	public virtual float LowPassCutoff { get; set; }
	public virtual float WetDryMix { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitDistortion

```
public class AVAudioUnitDistortion : MonoTouch.AVFoundation.AVAudioUnitEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDistortion ();
	public AVAudioUnitDistortion (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitDistortion (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitDistortion (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PreGain { get; set; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitDistortionPreset preset);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitDistortionPreset

```
[Serializable]
public enum AVAudioUnitDistortionPreset {
	DrumsBitBrush = 0,
	DrumsBufferBeats = 1,
	DrumsLoFi = 2,
	MultiBrokenSpeaker = 3,
	MultiCellphoneConcert = 4,
	MultiDecimated1 = 5,
	MultiDecimated2 = 6,
	MultiDecimated3 = 7,
	MultiDecimated4 = 8,
	MultiDistortedCubed = 10,
	MultiDistortedFunk = 9,
	MultiDistortedSquared = 11,
	MultiEcho1 = 12,
	MultiEcho2 = 13,
	MultiEchoTight1 = 14,
	MultiEchoTight2 = 15,
	MultiEverythingIsBroken = 16,
	SpeechAlienChatter = 17,
	SpeechCosmicInterference = 18,
	SpeechGoldenPi = 19,
	SpeechRadioTower = 20,
	SpeechWaves = 21,
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitEffect

```
public class AVAudioUnitEffect : MonoTouch.AVFoundation.AVAudioUnit, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEffect (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitEffect (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitEffect (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitEffect (System.IntPtr handle);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitEQ

```
public class AVAudioUnitEQ : MonoTouch.AVFoundation.AVAudioUnitEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQ ();
	public AVAudioUnitEQ (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitEQ (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitEQ (System.IntPtr handle);
	public AVAudioUnitEQ (uint numberOfBands);
	// properties
	public virtual AVAudioUnitEQFilterParameters[] Bands { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalGain { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitEQFilterParameters

```
public class AVAudioUnitEQFilterParameters : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQFilterParameters (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitEQFilterParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitEQFilterParameters (System.IntPtr handle);
	// properties
	public virtual float Bandwidth { get; set; }
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioUnitEQFilterType FilterType { get; set; }
	public virtual float Frequency { get; set; }
	public virtual float Gain { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitEQFilterType

```
[Serializable]
public enum AVAudioUnitEQFilterType {
	BandPass = 5,
	BandStop = 6,
	HighPass = 2,
	HighShelf = 8,
	LowPass = 1,
	LowShelf = 7,
	Parametric = 0,
	ResonantHighPass = 4,
	ResonantHighShelf = 10,
	ResonantLowPass = 3,
	ResonantLowShelf = 9,
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitGenerator

```
public class AVAudioUnitGenerator : MonoTouch.AVFoundation.AVAudioUnit, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitGenerator (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitGenerator (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitGenerator (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitGenerator (System.IntPtr handle);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitMidiInstrument

```
public class AVAudioUnitMidiInstrument : MonoTouch.AVFoundation.AVAudioUnit, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitMidiInstrument (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitMidiInstrument (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitMidiInstrument (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitMidiInstrument (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void SendController (byte controller, byte value, byte channel);
	public virtual void SendMidiEvent (byte midiStatus, byte data1, byte data2);
	public virtual void SendMidiEvent (byte midiStatus, byte data1);
	public virtual void SendMidiSysExEvent (MonoTouch.Foundation.NSData midiData);
	public virtual void SendPitchBend (ushort pitchbend, byte channel);
	public virtual void SendPressure (byte pressure, byte channel);
	public virtual void SendPressureForKey (byte key, byte value, byte channel);
	public virtual void SendProgramChange (byte program, byte channel);
	public virtual void SendProgramChange (byte program, byte bankMSB, byte bankLSB, byte channel);
	public virtual void StartNote (byte note, byte velocity, byte channel);
	public virtual void StopNote (byte note, byte channel);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitReverb

```
public class AVAudioUnitReverb : MonoTouch.AVFoundation.AVAudioUnitEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitReverb ();
	public AVAudioUnitReverb (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitReverb (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitReverb (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitReverbPreset

```
[Serializable]
public enum AVAudioUnitReverbPreset {
	Cathedral = 8,
	LargeChamber = 7,
	LargeHall = 4,
	LargeHall2 = 12,
	LargeRoom = 2,
	LargeRoom2 = 9,
	MediumChamber = 6,
	MediumHall = 3,
	MediumHall2 = 10,
	MediumHall3 = 11,
	MediumRoom = 1,
	Plate = 5,
	SmallRoom = 0,
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitSampler

```
public class AVAudioUnitSampler : MonoTouch.AVFoundation.AVAudioUnitMidiInstrument, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitSampler ();
	public AVAudioUnitSampler (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitSampler (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitSampler (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalTuning { get; set; }
	public virtual float MasterGain { get; set; }
	public virtual float StereoPan { get; set; }
	// methods
	public virtual bool LoadAudioFiles (MonoTouch.Foundation.NSUrl[] audioFiles, out MonoTouch.Foundation.NSError outError);
	public virtual bool LoadInstrument (MonoTouch.Foundation.NSUrl instrumentUrl, out MonoTouch.Foundation.NSError outError);
	public virtual bool LoadSoundBank (MonoTouch.Foundation.NSUrl bankUrl, byte program, byte bankMSB, byte bankLSB, out MonoTouch.Foundation.NSError outError);
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitTimeEffect

```
public class AVAudioUnitTimeEffect : MonoTouch.AVFoundation.AVAudioUnit, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimeEffect (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitTimeEffect (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitTimeEffect (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitTimeEffect (System.IntPtr handle);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitTimePitch

```
public class AVAudioUnitTimePitch : MonoTouch.AVFoundation.AVAudioUnitTimeEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimePitch (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitTimePitch ();
	public AVAudioUnitTimePitch (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitTimePitch (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitTimePitch (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Overlap { get; set; }
	public virtual float Pitch { get; set; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVAudioUnitVarispeed

```
public class AVAudioUnitVarispeed : MonoTouch.AVFoundation.AVAudioUnitTimeEffect, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitVarispeed (MonoTouch.AudioUnit.AudioComponentDescription desc);
	public AVAudioUnitVarispeed ();
	public AVAudioUnitVarispeed (MonoTouch.Foundation.NSCoder coder);
	public AVAudioUnitVarispeed (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioUnitVarispeed (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoTouch.AVFoundation.AVCaptureAutoExposureBracketedStillImageSettings

```
public class AVCaptureAutoExposureBracketedStillImageSettings : MonoTouch.AVFoundation.AVCaptureBracketedStillImageSettings, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureAutoExposureBracketedStillImageSettings ();
	public AVCaptureAutoExposureBracketedStillImageSettings (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAutoExposureBracketedStillImageSettings (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAutoExposureBracketedStillImageSettings (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float ExposureTargetBias { get; }
	// methods
	public static AVCaptureAutoExposureBracketedStillImageSettings Create (float exposureTargetBias);
}
```

### New Type MonoTouch.AVFoundation.AVCaptureAutoFocusSystem

```
[Serializable]
public enum AVCaptureAutoFocusSystem {
	ContrastDetection = 1,
	None = 0,
	PhaseDetection = 2,
}
```

### New Type MonoTouch.AVFoundation.AVCaptureBracketedStillImageSettings

```
public class AVCaptureBracketedStillImageSettings : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureBracketedStillImageSettings (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureBracketedStillImageSettings (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureBracketedStillImageSettings (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.AVFoundation.AVCaptureManualExposureBracketedStillImageSettings

```
public class AVCaptureManualExposureBracketedStillImageSettings : MonoTouch.AVFoundation.AVCaptureBracketedStillImageSettings, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureManualExposureBracketedStillImageSettings ();
	public AVCaptureManualExposureBracketedStillImageSettings (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureManualExposureBracketedStillImageSettings (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureManualExposureBracketedStillImageSettings (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.CoreMedia.CMTime ExposureDuration { get; }
	public virtual float ISO { get; }
	// methods
	public static AVCaptureManualExposureBracketedStillImageSettings Create (MonoTouch.CoreMedia.CMTime duration, float ISO);
}
```

### New Type MonoTouch.AVFoundation.AVCaptureVideoStabilizationMode

```
[Serializable]
public enum AVCaptureVideoStabilizationMode {
	Auto = 3,
	Cinematic = 2,
	Off = 0,
	Standard = 1,
}
```

### New Type MonoTouch.AVFoundation.AVCaptureWhiteBalanceChromaticityValues

```
public struct AVCaptureWhiteBalanceChromaticityValues {
	// constructors
	public AVCaptureWhiteBalanceChromaticityValues (float x, float y);
	// fields
	public float X;
	public float Y;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.AVFoundation.AVCaptureWhiteBalanceGains

```
public struct AVCaptureWhiteBalanceGains {
	// constructors
	public AVCaptureWhiteBalanceGains (float redGain, float greenGain, float blueGain);
	// fields
	public float BlueGain;
	public float GreenGain;
	public float RedGain;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues

```
public struct AVCaptureWhiteBalanceTemperatureAndTintValues {
	// constructors
	public AVCaptureWhiteBalanceTemperatureAndTintValues (float temperature, float tint);
	// fields
	public float Temperature;
	public float Tint;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.AVFoundation.AVMetadataIdentifiers

```
public static class AVMetadataIdentifiers {

	// inner types
	public static class CommonIdentifier {
		// properties
		public static MonoTouch.Foundation.NSString AlbumName { get; }
		public static MonoTouch.Foundation.NSString Artist { get; }
		public static MonoTouch.Foundation.NSString Artwork { get; }
		public static MonoTouch.Foundation.NSString AssetIdentifier { get; }
		public static MonoTouch.Foundation.NSString Author { get; }
		public static MonoTouch.Foundation.NSString Contributor { get; }
		public static MonoTouch.Foundation.NSString Copyrights { get; }
		public static MonoTouch.Foundation.NSString CreationDate { get; }
		public static MonoTouch.Foundation.NSString Creator { get; }
		public static MonoTouch.Foundation.NSString Description { get; }
		public static MonoTouch.Foundation.NSString Format { get; }
		public static MonoTouch.Foundation.NSString Language { get; }
		public static MonoTouch.Foundation.NSString LastModifiedDate { get; }
		public static MonoTouch.Foundation.NSString Location { get; }
		public static MonoTouch.Foundation.NSString Make { get; }
		public static MonoTouch.Foundation.NSString Model { get; }
		public static MonoTouch.Foundation.NSString Publisher { get; }
		public static MonoTouch.Foundation.NSString Relation { get; }
		public static MonoTouch.Foundation.NSString Software { get; }
		public static MonoTouch.Foundation.NSString Source { get; }
		public static MonoTouch.Foundation.NSString Subject { get; }
		public static MonoTouch.Foundation.NSString Title { get; }
		public static MonoTouch.Foundation.NSString Type { get; }
	}
	public static class QuickTime {
		// properties
		public static MonoTouch.Foundation.NSString UserDataAlbum { get; }
		public static MonoTouch.Foundation.NSString UserDataArranger { get; }
		public static MonoTouch.Foundation.NSString UserDataArtist { get; }
		public static MonoTouch.Foundation.NSString UserDataAuthor { get; }
		public static MonoTouch.Foundation.NSString UserDataChapter { get; }
		public static MonoTouch.Foundation.NSString UserDataComment { get; }
		public static MonoTouch.Foundation.NSString UserDataComposer { get; }
		public static MonoTouch.Foundation.NSString UserDataCopyright { get; }
		public static MonoTouch.Foundation.NSString UserDataCreationDate { get; }
		public static MonoTouch.Foundation.NSString UserDataCredits { get; }
		public static MonoTouch.Foundation.NSString UserDataDescription { get; }
		public static MonoTouch.Foundation.NSString UserDataDirector { get; }
		public static MonoTouch.Foundation.NSString UserDataDisclaimer { get; }
		public static MonoTouch.Foundation.NSString UserDataEncodedBy { get; }
		public static MonoTouch.Foundation.NSString UserDataFullName { get; }
		public static MonoTouch.Foundation.NSString UserDataGenre { get; }
		public static MonoTouch.Foundation.NSString UserDataHostComputer { get; }
		public static MonoTouch.Foundation.NSString UserDataInformation { get; }
		public static MonoTouch.Foundation.NSString UserDataKeywords { get; }
		public static MonoTouch.Foundation.NSString UserDataLocationISO6709 { get; }
		public static MonoTouch.Foundation.NSString UserDataMake { get; }
		public static MonoTouch.Foundation.NSString UserDataModel { get; }
		public static MonoTouch.Foundation.NSString UserDataOriginalArtist { get; }
		public static MonoTouch.Foundation.NSString UserDataOriginalFormat { get; }
		public static MonoTouch.Foundation.NSString UserDataOriginalSource { get; }
		public static MonoTouch.Foundation.NSString UserDataPerformers { get; }
		public static MonoTouch.Foundation.NSString UserDataPhonogramRights { get; }
		public static MonoTouch.Foundation.NSString UserDataProducer { get; }
		public static MonoTouch.Foundation.NSString UserDataProduct { get; }
		public static MonoTouch.Foundation.NSString UserDataPublisher { get; }
		public static MonoTouch.Foundation.NSString UserDataSoftware { get; }
		public static MonoTouch.Foundation.NSString UserDataSpecialPlaybackRequirements { get; }
		public static MonoTouch.Foundation.NSString UserDataTaggedCharacteristic { get; }
		public static MonoTouch.Foundation.NSString UserDataTrack { get; }
		public static MonoTouch.Foundation.NSString UserDataTrackName { get; }
		public static MonoTouch.Foundation.NSString UserDataUrlLink { get; }
		public static MonoTouch.Foundation.NSString UserDataWarning { get; }
		public static MonoTouch.Foundation.NSString UserDataWriter { get; }
	}
	public static class Iso {
		// properties
		public static MonoTouch.Foundation.NSString UserDataCopyright { get; }
		public static MonoTouch.Foundation.NSString UserDataTaggedCharacteristic { get; }
	}
	public static class ThreeGP {
		// properties
		public static MonoTouch.Foundation.NSString UserDataAlbumAndTrack { get; }
		public static MonoTouch.Foundation.NSString UserDataAuthor { get; }
		public static MonoTouch.Foundation.NSString UserDataCollection { get; }
		public static MonoTouch.Foundation.NSString UserDataCopyright { get; }
		public static MonoTouch.Foundation.NSString UserDataDescription { get; }
		public static MonoTouch.Foundation.NSString UserDataGenre { get; }
		public static MonoTouch.Foundation.NSString UserDataKeywordList { get; }
		public static MonoTouch.Foundation.NSString UserDataLocation { get; }
		public static MonoTouch.Foundation.NSString UserDataMediaClassification { get; }
		public static MonoTouch.Foundation.NSString UserDataMediaRating { get; }
		public static MonoTouch.Foundation.NSString UserDataPerformer { get; }
		public static MonoTouch.Foundation.NSString UserDataRecordingYear { get; }
		public static MonoTouch.Foundation.NSString UserDataThumbnail { get; }
		public static MonoTouch.Foundation.NSString UserDataTitle { get; }
		public static MonoTouch.Foundation.NSString UserDataUserRating { get; }
	}
	public static class QuickTimeMetadata {
		// properties
		public static MonoTouch.Foundation.NSString Album { get; }
		public static MonoTouch.Foundation.NSString Arranger { get; }
		public static MonoTouch.Foundation.NSString Artist { get; }
		public static MonoTouch.Foundation.NSString Artwork { get; }
		public static MonoTouch.Foundation.NSString Author { get; }
		public static MonoTouch.Foundation.NSString CameraFrameReadoutTime { get; }
		public static MonoTouch.Foundation.NSString CameraIdentifier { get; }
		public static MonoTouch.Foundation.NSString CollectionUser { get; }
		public static MonoTouch.Foundation.NSString Comment { get; }
		public static MonoTouch.Foundation.NSString Composer { get; }
		public static MonoTouch.Foundation.NSString Copyright { get; }
		public static MonoTouch.Foundation.NSString CreationDate { get; }
		public static MonoTouch.Foundation.NSString Credits { get; }
		public static MonoTouch.Foundation.NSString Description { get; }
		public static MonoTouch.Foundation.NSString DirectionFacing { get; }
		public static MonoTouch.Foundation.NSString DirectionMotion { get; }
		public static MonoTouch.Foundation.NSString Director { get; }
		public static MonoTouch.Foundation.NSString DisplayName { get; }
		public static MonoTouch.Foundation.NSString EncodedBy { get; }
		public static MonoTouch.Foundation.NSString Genre { get; }
		public static MonoTouch.Foundation.NSString Information { get; }
		public static MonoTouch.Foundation.NSString iXML { get; }
		public static MonoTouch.Foundation.NSString Keywords { get; }
		public static MonoTouch.Foundation.NSString LocationBody { get; }
		public static MonoTouch.Foundation.NSString LocationDate { get; }
		public static MonoTouch.Foundation.NSString LocationISO6709 { get; }
		public static MonoTouch.Foundation.NSString LocationName { get; }
		public static MonoTouch.Foundation.NSString LocationNote { get; }
		public static MonoTouch.Foundation.NSString LocationRole { get; }
		public static MonoTouch.Foundation.NSString Make { get; }
		public static MonoTouch.Foundation.NSString Model { get; }
		public static MonoTouch.Foundation.NSString OriginalArtist { get; }
		public static MonoTouch.Foundation.NSString Performer { get; }
		public static MonoTouch.Foundation.NSString PhonogramRights { get; }
		public static MonoTouch.Foundation.NSString PreferredAffineTransform { get; }
		public static MonoTouch.Foundation.NSString Producer { get; }
		public static MonoTouch.Foundation.NSString Publisher { get; }
		public static MonoTouch.Foundation.NSString RatingUser { get; }
		public static MonoTouch.Foundation.NSString Software { get; }
		public static MonoTouch.Foundation.NSString Title { get; }
		public static MonoTouch.Foundation.NSString Year { get; }
	}
	public static class iTunesMetadata {
		// properties
		public static MonoTouch.Foundation.NSString AccountKind { get; }
		public static MonoTouch.Foundation.NSString Acknowledgement { get; }
		public static MonoTouch.Foundation.NSString Album { get; }
		public static MonoTouch.Foundation.NSString AlbumArtist { get; }
		public static MonoTouch.Foundation.NSString AppleID { get; }
		public static MonoTouch.Foundation.NSString Arranger { get; }
		public static MonoTouch.Foundation.NSString ArtDirector { get; }
		public static MonoTouch.Foundation.NSString Artist { get; }
		public static MonoTouch.Foundation.NSString ArtistID { get; }
		public static MonoTouch.Foundation.NSString Author { get; }
		public static MonoTouch.Foundation.NSString BeatsPerMin { get; }
		public static MonoTouch.Foundation.NSString Composer { get; }
		public static MonoTouch.Foundation.NSString Conductor { get; }
		public static MonoTouch.Foundation.NSString ContentRating { get; }
		public static MonoTouch.Foundation.NSString Copyright { get; }
		public static MonoTouch.Foundation.NSString CoverArt { get; }
		public static MonoTouch.Foundation.NSString Credits { get; }
		public static MonoTouch.Foundation.NSString Description { get; }
		public static MonoTouch.Foundation.NSString Director { get; }
		public static MonoTouch.Foundation.NSString DiscCompilation { get; }
		public static MonoTouch.Foundation.NSString DiscNumber { get; }
		public static MonoTouch.Foundation.NSString EncodedBy { get; }
		public static MonoTouch.Foundation.NSString EncodingTool { get; }
		public static MonoTouch.Foundation.NSString EQ { get; }
		public static MonoTouch.Foundation.NSString ExecProducer { get; }
		public static MonoTouch.Foundation.NSString GenreID { get; }
		public static MonoTouch.Foundation.NSString Grouping { get; }
		public static MonoTouch.Foundation.NSString LinerNotes { get; }
		public static MonoTouch.Foundation.NSString Lyrics { get; }
		public static MonoTouch.Foundation.NSString OnlineExtras { get; }
		public static MonoTouch.Foundation.NSString OriginalArtist { get; }
		public static MonoTouch.Foundation.NSString Performer { get; }
		public static MonoTouch.Foundation.NSString PhonogramRights { get; }
		public static MonoTouch.Foundation.NSString PlaylistID { get; }
		public static MonoTouch.Foundation.NSString PredefinedGenre { get; }
		public static MonoTouch.Foundation.NSString Producer { get; }
		public static MonoTouch.Foundation.NSString Publisher { get; }
		public static MonoTouch.Foundation.NSString RecordCompany { get; }
		public static MonoTouch.Foundation.NSString ReleaseDate { get; }
		public static MonoTouch.Foundation.NSString Soloist { get; }
		public static MonoTouch.Foundation.NSString SongID { get; }
		public static MonoTouch.Foundation.NSString SongName { get; }
		public static MonoTouch.Foundation.NSString SoundEngineer { get; }
		public static MonoTouch.Foundation.NSString Thanks { get; }
		public static MonoTouch.Foundation.NSString TrackNumber { get; }
		public static MonoTouch.Foundation.NSString TrackSubTitle { get; }
		public static MonoTouch.Foundation.NSString UserComment { get; }
		public static MonoTouch.Foundation.NSString UserGenre { get; }
	}
	public static class ID3Metadata {
		// properties
		public static MonoTouch.Foundation.NSString AlbumSortOrder { get; }
		public static MonoTouch.Foundation.NSString AlbumTitle { get; }
		public static MonoTouch.Foundation.NSString AttachedPicture { get; }
		public static MonoTouch.Foundation.NSString AudioEncryption { get; }
		public static MonoTouch.Foundation.NSString AudioSeekPointIndex { get; }
		public static MonoTouch.Foundation.NSString Band { get; }
		public static MonoTouch.Foundation.NSString BeatsPerMinute { get; }
		public static MonoTouch.Foundation.NSString Comments { get; }
		public static MonoTouch.Foundation.NSString CommercialInformation { get; }
		public static MonoTouch.Foundation.NSString Commerical { get; }
		public static MonoTouch.Foundation.NSString Composer { get; }
		public static MonoTouch.Foundation.NSString Conductor { get; }
		public static MonoTouch.Foundation.NSString ContentGroupDescription { get; }
		public static MonoTouch.Foundation.NSString ContentType { get; }
		public static MonoTouch.Foundation.NSString Copyright { get; }
		public static MonoTouch.Foundation.NSString CopyrightInformation { get; }
		public static MonoTouch.Foundation.NSString Date { get; }
		public static MonoTouch.Foundation.NSString EncodedBy { get; }
		public static MonoTouch.Foundation.NSString EncodedWith { get; }
		public static MonoTouch.Foundation.NSString EncodingTime { get; }
		public static MonoTouch.Foundation.NSString Encryption { get; }
		public static MonoTouch.Foundation.NSString Equalization { get; }
		public static MonoTouch.Foundation.NSString Equalization2 { get; }
		public static MonoTouch.Foundation.NSString EventTimingCodes { get; }
		public static MonoTouch.Foundation.NSString FileOwner { get; }
		public static MonoTouch.Foundation.NSString FileType { get; }
		public static MonoTouch.Foundation.NSString GeneralEncapsulatedObject { get; }
		public static MonoTouch.Foundation.NSString GroupIdentifier { get; }
		public static MonoTouch.Foundation.NSString InitialKey { get; }
		public static MonoTouch.Foundation.NSString InternationalStandardRecordingCode { get; }
		public static MonoTouch.Foundation.NSString InternetRadioStationName { get; }
		public static MonoTouch.Foundation.NSString InternetRadioStationOwner { get; }
		public static MonoTouch.Foundation.NSString InvolvedPeopleList_v23 { get; }
		public static MonoTouch.Foundation.NSString InvolvedPeopleList_v24 { get; }
		public static MonoTouch.Foundation.NSString Language { get; }
		public static MonoTouch.Foundation.NSString LeadPerformer { get; }
		public static MonoTouch.Foundation.NSString Length { get; }
		public static MonoTouch.Foundation.NSString Link { get; }
		public static MonoTouch.Foundation.NSString Lyricist { get; }
		public static MonoTouch.Foundation.NSString MediaType { get; }
		public static MonoTouch.Foundation.NSString ModifiedBy { get; }
		public static MonoTouch.Foundation.NSString Mood { get; }
		public static MonoTouch.Foundation.NSString MpegLocationLookupTable { get; }
		public static MonoTouch.Foundation.NSString MusicCDIdentifier { get; }
		public static MonoTouch.Foundation.NSString MusicianCreditsList { get; }
		public static MonoTouch.Foundation.NSString OfficialArtistWebpage { get; }
		public static MonoTouch.Foundation.NSString OfficialAudioFileWebpage { get; }
		public static MonoTouch.Foundation.NSString OfficialAudioSourceWebpage { get; }
		public static MonoTouch.Foundation.NSString OfficialInternetRadioStationHomepage { get; }
		public static MonoTouch.Foundation.NSString OfficialPublisherWebpage { get; }
		public static MonoTouch.Foundation.NSString OriginalAlbumTitle { get; }
		public static MonoTouch.Foundation.NSString OriginalArtist { get; }
		public static MonoTouch.Foundation.NSString OriginalFilename { get; }
		public static MonoTouch.Foundation.NSString OriginalLyricist { get; }
		public static MonoTouch.Foundation.NSString OriginalReleaseTime { get; }
		public static MonoTouch.Foundation.NSString OriginalReleaseYear { get; }
		public static MonoTouch.Foundation.NSString Ownership { get; }
		public static MonoTouch.Foundation.NSString PartOfASet { get; }
		public static MonoTouch.Foundation.NSString Payment { get; }
		public static MonoTouch.Foundation.NSString PerformerSortOrder { get; }
		public static MonoTouch.Foundation.NSString PlayCounter { get; }
		public static MonoTouch.Foundation.NSString PlaylistDelay { get; }
		public static MonoTouch.Foundation.NSString Popularimeter { get; }
		public static MonoTouch.Foundation.NSString PositionSynchronization { get; }
		public static MonoTouch.Foundation.NSString Private { get; }
		public static MonoTouch.Foundation.NSString ProducedNotice { get; }
		public static MonoTouch.Foundation.NSString Publisher { get; }
		public static MonoTouch.Foundation.NSString RecommendedBufferSize { get; }
		public static MonoTouch.Foundation.NSString RecordingDates { get; }
		public static MonoTouch.Foundation.NSString RecordingTime { get; }
		public static MonoTouch.Foundation.NSString RelativeVolumeAdjustment { get; }
		public static MonoTouch.Foundation.NSString RelativeVolumeAdjustment2 { get; }
		public static MonoTouch.Foundation.NSString ReleaseTime { get; }
		public static MonoTouch.Foundation.NSString Reverb { get; }
		public static MonoTouch.Foundation.NSString Seek { get; }
		public static MonoTouch.Foundation.NSString SetSubtitle { get; }
		public static MonoTouch.Foundation.NSString Signature { get; }
		public static MonoTouch.Foundation.NSString Size { get; }
		public static MonoTouch.Foundation.NSString SubTitle { get; }
		public static MonoTouch.Foundation.NSString SynchronizedLyric { get; }
		public static MonoTouch.Foundation.NSString SynchronizedTempoCodes { get; }
		public static MonoTouch.Foundation.NSString TaggingTime { get; }
		public static MonoTouch.Foundation.NSString TermsOfUse { get; }
		public static MonoTouch.Foundation.NSString Time { get; }
		public static MonoTouch.Foundation.NSString TitleDescription { get; }
		public static MonoTouch.Foundation.NSString TitleSortOrder { get; }
		public static MonoTouch.Foundation.NSString TrackNumber { get; }
		public static MonoTouch.Foundation.NSString UniqueFileIdentifier { get; }
		public static MonoTouch.Foundation.NSString UnsynchronizedLyric { get; }
		public static MonoTouch.Foundation.NSString UserText { get; }
		public static MonoTouch.Foundation.NSString UserUrl { get; }
		public static MonoTouch.Foundation.NSString Year { get; }
	}
	public static class IcyMetadata {
		// properties
		public static MonoTouch.Foundation.NSString StreamTitle { get; }
		public static MonoTouch.Foundation.NSString StreamUrl { get; }
	}
}
```

### New Type MonoTouch.AVFoundation.AVMidiPlayer

```
public class AVMidiPlayer : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMidiPlayer ();
	public AVMidiPlayer (MonoTouch.Foundation.NSCoder coder);
	public AVMidiPlayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVMidiPlayer (System.IntPtr handle);
	public AVMidiPlayer (MonoTouch.Foundation.NSUrl contentsUrl, MonoTouch.Foundation.NSUrl soundBankUrl, out MonoTouch.Foundation.NSError outError);
	public AVMidiPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSUrl sounddBankUrl, out MonoTouch.Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double CurrentPosition { get; set; }
	public virtual double Duration { get; }
	public virtual bool Playing { get; }
	public virtual float Rate { get; set; }
	// methods
	public virtual void Play (System.Action completionHandler);
	public virtual System.Threading.Tasks.Task PlayAsync ();
	public virtual void PrepareToPlay ();
	public virtual void Stop ();
}
```

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataOutput

```
public class AVPlayerItemMetadataOutput : MonoTouch.AVFoundation.AVPlayerItemOutput, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutput ();
	public AVPlayerItemMetadataOutput (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutput (System.IntPtr handle);
	public AVPlayerItemMetadataOutput (MonoTouch.Foundation.NSString[] metadataIdentifiers);
	// properties
	public virtual double AdvanceIntervalForDelegateInvocation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public AVPlayerItemMetadataOutputPushDelegate Delegate { get; }
	public virtual MonoTouch.CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemMetadataOutputPushDelegate pushDelegate, MonoTouch.CoreFoundation.DispatchQueue delegateQueue);
}
```

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataOutputPushDelegate

```
public class AVPlayerItemMetadataOutputPushDelegate : MonoTouch.Foundation.NSObject, IAVPlayerItemMetadataOutputPushDelegate, IAVPlayerItemOutputPushDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutputPushDelegate ();
	public AVPlayerItemMetadataOutputPushDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutputPushDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void DidOutputTimedMetadataGroups (AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
```

### New Type MonoTouch.AVFoundation.AVPlayerItemMetadataOutputPushDelegate_Extensions

```
public static class AVPlayerItemMetadataOutputPushDelegate_Extensions {
	// methods
	public static void DidOutputTimedMetadataGroups (IAVPlayerItemMetadataOutputPushDelegate This, AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
}
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

### New Type MonoTouch.AVFoundation.AVSampleBufferDisplayLayer

```
public class AVSampleBufferDisplayLayer : MonoTouch.CoreAnimation.CALayer, MonoTouch.CoreAnimation.ICAMediaTiming, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVSampleBufferDisplayLayer ();
	public AVSampleBufferDisplayLayer (MonoTouch.Foundation.NSCoder coder);
	public AVSampleBufferDisplayLayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVSampleBufferDisplayLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.CoreMedia.CMTimebase ControlTimebase { get; set; }
	public virtual MonoTouch.Foundation.NSError Error { get; }
	public virtual bool ReadyForMoreMediaData { get; }
	public virtual AVQueuedSampleBufferRenderingStatus Status { get; }
	public virtual string VideoGravity { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnqueueSampleBuffer (MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer);
	public virtual void Flush ();
	public virtual void FlushAndRemoveImage ();
	public virtual void RequestMediaDataWhenReadyOnQueue (MonoTouch.CoreFoundation.DispatchQueue queue, System.Action enqueuer);
	public virtual void StopRequestingMediaData ();
}
```

### New Type MonoTouch.AVFoundation.AVUtilities

```
public static class AVUtilities {
	// methods
	public static System.Drawing.RectangleF WithAspectRatio (System.Drawing.RectangleF self, System.Drawing.SizeF aspectRatio);
}
```

### New Type MonoTouch.AVFoundation.IAVAudio3DMixing

```
public interface IAVAudio3DMixing : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual OpenTK.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoTouch.AVFoundation.IAVAudioMixing

```
public interface IAVAudioMixing : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IAVAudio3DMixing, IAVAudioStereoMixing {
	// properties
	public virtual float Volume { get; set; }
}
```

### New Type MonoTouch.AVFoundation.IAVAudioStereoMixing

```
public interface IAVAudioStereoMixing : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoTouch.AVFoundation.IAVPlayerItemMetadataOutputPushDelegate

```
public interface IAVPlayerItemMetadataOutputPushDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IAVPlayerItemOutputPushDelegate {
}
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
	public virtual MonoTouch.Foundation.NSObject CompositingFilter { get; set; }
	public virtual MonoTouch.CoreImage.CIFilter[] Filters { get; set; }
	public virtual float MinificationFilterBias { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary Style { get; set; }
```

### Type Changed: MonoTouch.CoreAnimation.CATransition

Removed property:

```
public virtual MonoTouch.Foundation.NSObject filter { get; set; }
```

Added properties:

```
[Obsolete ("The name has been fixed, use Filter instead")]
	public MonoTouch.Foundation.NSObject filter { get; set; }
	public virtual MonoTouch.Foundation.NSObject Filter { get; set; }
```

### New Type MonoTouch.CoreAnimation.CAMetalDrawable_Extensions

```
public static class CAMetalDrawable_Extensions {
}
```

### New Type MonoTouch.CoreAnimation.CAMetalLayer

```
public class CAMetalLayer : MonoTouch.CoreAnimation.CALayer, ICAMediaTiming, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAMetalLayer ();
	public CAMetalLayer (MonoTouch.Foundation.NSCoder coder);
	public CAMetalLayer (MonoTouch.Foundation.NSObjectFlag t);
	public CAMetalLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Metal.IMTLDevice Device { get; set; }
	public virtual System.Drawing.SizeF DrawableSize { get; set; }
	public virtual bool FramebufferOnly { get; set; }
	public virtual MonoTouch.Metal.MTLPixelFormat PixelFormat { get; set; }
	public virtual bool PresentsWithTransaction { get; set; }
	// methods
	public virtual ICAMetalDrawable CreateDrawable ();
	protected override void Dispose (bool disposing);
	public virtual ICAMetalDrawable NextDrawable ();
}
```

### New Type MonoTouch.CoreAnimation.ICAMetalDrawable

```
public interface ICAMetalDrawable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Metal.IMTLDrawable {
	// properties
	public virtual CAMetalLayer Layer { get; }
	public virtual MonoTouch.Metal.IMTLTexture Texture { get; }
}
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
public virtual CBUUID UUID { get; set; }
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
	public virtual CBUUID UUID { get; set; }
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

Obsoleted constructor:

```
[Obsolete ("Use .ctor(NSManagedObjectModel)")]
	public NSPersistentStoreCoordinator ();
```

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

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.CFStream

### Type Changed: MonoTouch.CoreFoundation.CFStream.CFStreamCallback

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr s, CFStreamEventType type, System.IntPtr info, System.AsyncCallback callback, object object);
	public virtual void Invoke (System.IntPtr s, CFStreamEventType type, System.IntPtr info);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr s, int type, System.IntPtr info, System.AsyncCallback callback, object object);
	public virtual void Invoke (System.IntPtr s, int type, System.IntPtr info);
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGVector

Added method:

```
public static CGVector FromString (string s);
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIAutoAdjustmentFilterOptions

Added fields:

```
public bool? AutoAdjustCrop;
	public bool? AutoAdjustLevel;
```

### Type Changed: MonoTouch.CoreImage.CIColor

Added property:

```
public float[] Components { get; }
```

### Type Changed: MonoTouch.CoreImage.CIContextOptions

Added properties:

```
public int? CIImageFormat { get; set; }
	public bool? PriorityRequestLow { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIDetector

Added properties:

```
public static MonoTouch.Foundation.NSString AspectRatio { get; }
	public static MonoTouch.Foundation.NSString FocalLength { get; }
	public static MonoTouch.Foundation.NSString TypeQRCode { get; }
	public static MonoTouch.Foundation.NSString TypeRectangle { get; }
```

Added methods:

```
public static CIDetector CreateQRDetector (CIContext context, CIDetectorOptions detectorOptions);
	public static CIDetector CreateRectangleDetector (CIContext context, CIDetectorOptions detectorOptions);
```

### Type Changed: MonoTouch.CoreImage.CIDetectorOptions

Added properties:

```
public float? AspectRatio { get; set; }
	public float? FocalLength { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIFilter

Added constructor:

```
protected CIFilter ();
```

Added method:

```
public static CIFilter GetFilter (string name, MonoTouch.Foundation.NSDictionary inputParameters);
```

### Type Changed: MonoTouch.CoreImage.CIImage

Added property:

```
public static int FormatRGBAf { get; }
```

Added methods:

```
public virtual CIImage CreateByClampingToExtent ();
	public virtual CIImage CreateByCompositingOverImage (CIImage dest);
	public virtual CIImage CreateByFiltering (string filterName, MonoTouch.Foundation.NSDictionary inputParameters);
	public virtual CIImage CreateWithOrientation (CIImageOrientation orientation);
	public virtual MonoTouch.CoreGraphics.CGAffineTransform GetImageTransform (CIImageOrientation orientation);
	public static CIImage ImageWithTexture (uint glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace colorspace);
```

### Type Changed: MonoTouch.CoreImage.CIVector

Added constructors:

```
public CIVector (MonoTouch.CoreGraphics.CGAffineTransform r);
	public CIVector (System.Drawing.RectangleF r);
	public CIVector (System.Drawing.PointF p);
```

### New Type MonoTouch.CoreImage.CIAccordionFoldTransition

```
public class CIAccordionFoldTransition : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAccordionFoldTransition ();
	public CIAccordionFoldTransition (System.IntPtr handle);
	// properties
	public float BottomHeight { get; set; }
	public float FoldShadowAmount { get; set; }
	public int NumberOfFolds { get; set; }
	public CIImage TargetImage { get; set; }
	public float Time { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIAreaHistogram

```
public class CIAreaHistogram : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAreaHistogram ();
	public CIAreaHistogram (System.IntPtr handle);
	// properties
	public float Count { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIAztecCodeGenerator

```
public class CIAztecCodeGenerator : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAztecCodeGenerator ();
	public CIAztecCodeGenerator (System.IntPtr handle);
	// properties
	public bool CompactStyle { get; set; }
	public float CorrectionLevel { get; set; }
	public int Layers { get; set; }
	public MonoTouch.Foundation.NSData Message { get; set; }
}
```

### New Type MonoTouch.CoreImage.CICode128BarcodeGenerator

```
public class CICode128BarcodeGenerator : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CICode128BarcodeGenerator ();
	public CICode128BarcodeGenerator (System.IntPtr handle);
	// properties
	public MonoTouch.Foundation.NSData Message { get; set; }
	public float QuietSpace { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIColorKernel

```
public class CIColorKernel : MonoTouch.CoreImage.CIKernel, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorKernel (MonoTouch.Foundation.NSCoder coder);
	public CIColorKernel (MonoTouch.Foundation.NSObjectFlag t);
	public CIColorKernel (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (System.Drawing.RectangleF extent, MonoTouch.Foundation.NSObject[] args);
}
```

### New Type MonoTouch.CoreImage.CIDivideBlendMode

```
public class CIDivideBlendMode : MonoTouch.CoreImage.CIBlendFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIDivideBlendMode ();
	public CIDivideBlendMode (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CIGlassDistortion

```
public class CIGlassDistortion : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIGlassDistortion ();
	public CIGlassDistortion (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Scale { get; set; }
	public CIImage Texture { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIHistogramDisplayFilter

```
public class CIHistogramDisplayFilter : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIHistogramDisplayFilter ();
	public CIHistogramDisplayFilter (System.IntPtr handle);
	// properties
	public float Height { get; set; }
	public float HighLimit { get; set; }
	public float LowLimit { get; set; }
}
```

### New Type MonoTouch.CoreImage.CIKernel

```
public class CIKernel : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIKernel (MonoTouch.Foundation.NSCoder coder);
	public CIKernel (MonoTouch.Foundation.NSObjectFlag t);
	public CIKernel (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	// methods
	public virtual CIImage ApplyWithExtent (System.Drawing.RectangleF extent, CIKernelRoiCallback callback, MonoTouch.Foundation.NSObject[] args);
	public static CIKernel FromProgram (string coreImageShaderProgram);
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
}
```

### New Type MonoTouch.CoreImage.CIKernelRoiCallback

```
public sealed delegate CIKernelRoiCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CIKernelRoiCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (int index, System.Drawing.RectangleF rect, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF EndInvoke (System.IAsyncResult result);
	public virtual System.Drawing.RectangleF Invoke (int index, System.Drawing.RectangleF rect);
}
```

### New Type MonoTouch.CoreImage.CILinearBurnBlendMode

```
public class CILinearBurnBlendMode : MonoTouch.CoreImage.CIBlendFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearBurnBlendMode ();
	public CILinearBurnBlendMode (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CILinearDodgeBlendMode

```
public class CILinearDodgeBlendMode : MonoTouch.CoreImage.CIBlendFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearDodgeBlendMode ();
	public CILinearDodgeBlendMode (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CIPerspectiveCorrection

```
public class CIPerspectiveCorrection : MonoTouch.CoreImage.CIPerspectiveTransform, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPerspectiveCorrection ();
	public CIPerspectiveCorrection (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CIPinLightBlendMode

```
public class CIPinLightBlendMode : MonoTouch.CoreImage.CIBlendFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPinLightBlendMode ();
	public CIPinLightBlendMode (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CIQRCodeFeature

```
public class CIQRCodeFeature : MonoTouch.CoreImage.CIFeature, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIQRCodeFeature ();
	public CIQRCodeFeature (MonoTouch.Foundation.NSCoder coder);
	public CIQRCodeFeature (MonoTouch.Foundation.NSObjectFlag t);
	public CIQRCodeFeature (System.IntPtr handle);
	// properties
	public virtual System.Drawing.PointF BottomLeft { get; }
	public virtual System.Drawing.PointF BottomRight { get; }
	public virtual System.Drawing.RectangleF Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string MessageString { get; }
	public virtual System.Drawing.PointF TopLeft { get; }
	public virtual System.Drawing.PointF TopRight { get; }
}
```

### New Type MonoTouch.CoreImage.CIRectangleFeature

```
public class CIRectangleFeature : MonoTouch.CoreImage.CIFeature, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIRectangleFeature ();
	public CIRectangleFeature (MonoTouch.Foundation.NSCoder coder);
	public CIRectangleFeature (MonoTouch.Foundation.NSObjectFlag t);
	public CIRectangleFeature (System.IntPtr handle);
	// properties
	public virtual System.Drawing.PointF BottomLeft { get; }
	public virtual System.Drawing.PointF BottomRight { get; }
	public virtual System.Drawing.RectangleF Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Drawing.PointF TopLeft { get; }
	public virtual System.Drawing.PointF TopRight { get; }
}
```

### New Type MonoTouch.CoreImage.CISubtractBlendMode

```
public class CISubtractBlendMode : MonoTouch.CoreImage.CIBlendFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CISubtractBlendMode ();
	public CISubtractBlendMode (System.IntPtr handle);
}
```

### New Type MonoTouch.CoreImage.CIWarpKernel

```
public class CIWarpKernel : MonoTouch.CoreImage.CIKernel, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIWarpKernel (MonoTouch.Foundation.NSCoder coder);
	public CIWarpKernel (MonoTouch.Foundation.NSObjectFlag t);
	public CIWarpKernel (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (System.Drawing.RectangleF extent, CIKernelRoiCallback callback, CIImage image, MonoTouch.Foundation.NSObject[] args);
}
```

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLAuthorizationStatus

Added values:

```
AuthorizedAlways = 3,
	AuthorizedWhenInUse = 4,
```

Obsoleted field:

```
[Obsolete ("Value obsoleted, use AuthorizedAlways instead")]
	Authorized = 3,
```

### Type Changed: MonoTouch.CoreLocation.CLBeaconRegion

Obsoleted constructor:

```
[Obsolete ("Does not return a valid instance on iOS8")]
	public CLBeaconRegion ();
```

### Type Changed: MonoTouch.CoreLocation.CLLocation

Added property:

```
public virtual CLFloor Floor { get; }
```

### Type Changed: MonoTouch.CoreLocation.CLLocationManager

Added property:

```
public static bool IsRangingAvailable { get; }
```

Added event:

```
public event System.EventHandler<CLVisitedEventArgs> DidVisit;
```

Added methods:

```
public virtual void RequestAlwaysAuthorization ();
	public virtual void RequestWhenInUseAuthorization ();
	public virtual void StartMonitoringVisits ();
	public virtual void StopMonitoringVisits ();
```

### Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

Added method:

```
public virtual void DidVisit (CLLocationManager manager, CLVisit visit);
```

### Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate_Extensions

Added method:

```
public static void DidVisit (ICLLocationManagerDelegate This, CLLocationManager manager, CLVisit visit);
```

### New Type MonoTouch.CoreLocation.CLFloor

```
public class CLFloor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CLFloor ();
	public CLFloor (MonoTouch.Foundation.NSCoder coder);
	public CLFloor (MonoTouch.Foundation.NSObjectFlag t);
	public CLFloor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int Level { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CoreLocation.CLVisit

```
public class CLVisit : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CLVisit ();
	public CLVisit (MonoTouch.Foundation.NSCoder coder);
	public CLVisit (MonoTouch.Foundation.NSObjectFlag t);
	public CLVisit (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSDate ArrivalDate { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CLLocationCoordinate2D Coordinate { get; }
	public virtual MonoTouch.Foundation.NSDate DepartureDate { get; }
	public virtual double HorizontalAccuracy { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreLocation.CLVisitedEventArgs

```
public class CLVisitedEventArgs : System.EventArgs {
	// constructors
	public CLVisitedEventArgs (CLVisit visit);
	// properties
	public CLVisit Visit { get; set; }
}
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

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMMotionActivity

Added property:

```
public virtual bool Cycling { get; }
```

### New Type MonoTouch.CoreMotion.CMAltimeter

```
public class CMAltimeter : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CMAltimeter ();
	public CMAltimeter (MonoTouch.Foundation.NSCoder coder);
	public CMAltimeter (MonoTouch.Foundation.NSObjectFlag t);
	public CMAltimeter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static bool IsRelativeAltitudeAvailable { get; }
	// methods
	public virtual void StartRelativeAltitudeUpdates (MonoTouch.Foundation.NSOperationQueue queue, System.Action<CMAltitudeData,MonoTouch.Foundation.NSError> handler);
	public virtual void StopRelativeAltitudeUpdates ();
}
```

### New Type MonoTouch.CoreMotion.CMAltitudeData

```
public class CMAltitudeData : MonoTouch.CoreMotion.CMLogItem, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CMAltitudeData (MonoTouch.Foundation.NSCoder coder);
	public CMAltitudeData (MonoTouch.Foundation.NSObjectFlag t);
	public CMAltitudeData (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSNumber Pressure { get; }
	public virtual MonoTouch.Foundation.NSNumber RelativeAltitude { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CoreMotion.CMPedometer

```
public class CMPedometer : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CMPedometer ();
	public CMPedometer (MonoTouch.Foundation.NSCoder coder);
	public CMPedometer (MonoTouch.Foundation.NSObjectFlag t);
	public CMPedometer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static bool IsDistanceAvailable { get; }
	public static bool IsFloorCountingAvailable { get; }
	public static bool IsStepCountingAvailable { get; }
	// methods
	public virtual void QueryPedometerData (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, System.Action<CMPedometerData,MonoTouch.Foundation.NSError> handler);
	public virtual System.Threading.Tasks.Task<CMPedometerData> QueryPedometerDataAsync (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end);
	public virtual void StartPedometerUpdates (MonoTouch.Foundation.NSDate start, System.Action<CMPedometerData,MonoTouch.Foundation.NSError> handler);
	public virtual void StopPedometerUpdates ();
}
```

### New Type MonoTouch.CoreMotion.CMPedometerData

```
public class CMPedometerData : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CMPedometerData ();
	public CMPedometerData (MonoTouch.Foundation.NSCoder coder);
	public CMPedometerData (MonoTouch.Foundation.NSObjectFlag t);
	public CMPedometerData (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSNumber Distance { get; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; }
	public virtual MonoTouch.Foundation.NSNumber FloorsAscended { get; }
	public virtual MonoTouch.Foundation.NSNumber FloorsDescended { get; }
	public virtual MonoTouch.Foundation.NSNumber NumberOfSteps { get; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

## Namespace MonoTouch.CoreText

### Type Changed: MonoTouch.CoreText.CTLineBoundsOptions

Added value:

```
IncludeLanguageExtents = 32,
```

## Namespace MonoTouch.CoreVideo

### Type Changed: MonoTouch.CoreVideo.CVImageBuffer

Added field:

```
public static MonoTouch.Foundation.NSString AlphaChannelIsOpaque;
```

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

### Type Changed: MonoTouch.CoreVideo.CVPixelFormatDescription

Added fields:

```
public static MonoTouch.Foundation.NSString ContainsRgb;
	public static MonoTouch.Foundation.NSString ContainsYCbCr;
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

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.EventKitUI.EKEventViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

## Namespace MonoTouch.ExternalAccessory

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessory

```
public class EAWiFiUnconfiguredAccessory : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public EAWiFiUnconfiguredAccessory ();
	public EAWiFiUnconfiguredAccessory (MonoTouch.Foundation.NSCoder coder);
	public EAWiFiUnconfiguredAccessory (MonoTouch.Foundation.NSObjectFlag t);
	public EAWiFiUnconfiguredAccessory (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string MacAddress { get; }
	public virtual string Manufacturer { get; }
	public virtual string Model { get; }
	public virtual string Name { get; }
	public virtual EAWiFiUnconfiguredAccessoryProperties Properties { get; }
	public virtual string Ssid { get; }
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser

```
public class EAWiFiUnconfiguredAccessoryBrowser : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public EAWiFiUnconfiguredAccessoryBrowser ();
	public EAWiFiUnconfiguredAccessoryBrowser (MonoTouch.Foundation.NSCoder coder);
	public EAWiFiUnconfiguredAccessoryBrowser (MonoTouch.Foundation.NSObjectFlag t);
	public EAWiFiUnconfiguredAccessoryBrowser (System.IntPtr handle);
	public EAWiFiUnconfiguredAccessoryBrowser (IEAWiFiUnconfiguredAccessoryBrowserDelegate accessoryBrowserDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public EAWiFiUnconfiguredAccessoryBrowserDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSSet UnconfiguredAccessories { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<EAWiFiUnconfiguredAccessoryBrowserEventArgs> DidFindUnconfiguredAccessories;
	public event System.EventHandler<EAWiFiUnconfiguredAccessoryDidFinishEventArgs> DidFinishConfiguringAccessory;
	public event System.EventHandler<EAWiFiUnconfiguredAccessoryBrowserEventArgs> DidRemoveUnconfiguredAccessories;
	public event System.EventHandler<EAWiFiUnconfiguredAccessoryEventArgs> DidUpdateState;
	// methods
	protected override void Dispose (bool disposing);
	public virtual void StartSearchingForUnconfiguredAccessories (MonoTouch.Foundation.NSPredicate predicate);
	public virtual void StopSearchingForUnconfiguredAccessories ();
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate

```
public class EAWiFiUnconfiguredAccessoryBrowserDelegate : MonoTouch.Foundation.NSObject, IEAWiFiUnconfiguredAccessoryBrowserDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public EAWiFiUnconfiguredAccessoryBrowserDelegate ();
	public EAWiFiUnconfiguredAccessoryBrowserDelegate (MonoTouch.Foundation.NSCoder coder);
	public EAWiFiUnconfiguredAccessoryBrowserDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EAWiFiUnconfiguredAccessoryBrowserDelegate (System.IntPtr handle);
	// methods
	public virtual void DidFindUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, MonoTouch.Foundation.NSSet accessories);
	public virtual void DidFinishConfiguringAccessory (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
	public virtual void DidRemoveUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, MonoTouch.Foundation.NSSet accessories);
	public virtual void DidUpdateState (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessoryBrowserState state);
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate_Extensions

```
public static class EAWiFiUnconfiguredAccessoryBrowserDelegate_Extensions {
	// methods
	public static void DidFindUnconfiguredAccessories (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, MonoTouch.Foundation.NSSet accessories);
	public static void DidFinishConfiguringAccessory (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
	public static void DidRemoveUnconfiguredAccessories (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, MonoTouch.Foundation.NSSet accessories);
	public static void DidUpdateState (IEAWiFiUnconfiguredAccessoryBrowserDelegate This, EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessoryBrowserState state);
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserEventArgs

```
public class EAWiFiUnconfiguredAccessoryBrowserEventArgs : System.EventArgs {
	// constructors
	public EAWiFiUnconfiguredAccessoryBrowserEventArgs (MonoTouch.Foundation.NSSet accessories);
	// properties
	public MonoTouch.Foundation.NSSet Accessories { get; set; }
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserState

```
[Serializable]
public enum EAWiFiUnconfiguredAccessoryBrowserState {
	Configuring = 3,
	Searching = 2,
	Stopped = 1,
	WiFiUnavailable = 0,
}
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

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryDidFinishEventArgs

```
public class EAWiFiUnconfiguredAccessoryDidFinishEventArgs : System.EventArgs {
	// constructors
	public EAWiFiUnconfiguredAccessoryDidFinishEventArgs (EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
	// properties
	public EAWiFiUnconfiguredAccessory Accessory { get; set; }
	public EAWiFiUnconfiguredAccessoryConfigurationStatus Status { get; set; }
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryEventArgs

```
public class EAWiFiUnconfiguredAccessoryEventArgs : System.EventArgs {
	// constructors
	public EAWiFiUnconfiguredAccessoryEventArgs (EAWiFiUnconfiguredAccessoryBrowserState state);
	// properties
	public EAWiFiUnconfiguredAccessoryBrowserState State { get; set; }
}
```

### New Type MonoTouch.ExternalAccessory.EAWiFiUnconfiguredAccessoryProperties

```
[Serializable]
[Flags]
public enum EAWiFiUnconfiguredAccessoryProperties {
	SupportsAirPlay = 1,
	SupportsAirPrint = 2,
	SupportsHomeKit = 4,
}
```

### New Type MonoTouch.ExternalAccessory.IEAWiFiUnconfiguredAccessoryBrowserDelegate

```
public interface IEAWiFiUnconfiguredAccessoryBrowserDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added methods:

```
protected uint? GetUInt32Value (NSString key);
	protected void SetArrayValue<T> (NSString key, T[] values);
```

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

### Type Changed: MonoTouch.Foundation.NSAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoTouch.Foundation.NSByteCountFormatter

Added property:

```
public virtual NSFormattingContext FormattingContext { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoTouch.Foundation.NSCalendar

Added properties:

```
public virtual string AMSymbol { get; }
	public static NSString DayChangedNotification { get; }
	public virtual string[] EraSymbols { get; }
	public virtual string[] LongEraSymbols { get; }
	public virtual string[] MonthSymbols { get; }
	public virtual string PMSymbol { get; }
	public virtual string[] QuarterSymbols { get; }
	public virtual string[] ShortMonthSymbols { get; }
	public virtual string[] ShortQuarterSymbols { get; }
	public virtual string[] ShortStandaloneMonthSymbols { get; }
	public virtual string[] ShortStandaloneQuarterSymbols { get; }
	public virtual string[] ShortStandaloneWeekdaySymbols { get; }
	public virtual string[] ShortWeekdaySymbols { get; }
	public virtual string[] StandaloneMonthSymbols { get; }
	public virtual string[] StandaloneQuarterSymbols { get; }
	public virtual string[] StandaloneWeekdaySymbols { get; }
	public virtual string[] VeryShortMonthSymbols { get; }
	public virtual string[] VeryShortStandaloneMonthSymbols { get; }
	public virtual string[] VeryShortStandaloneWeekdaySymbols { get; }
	public virtual string[] VeryShortWeekdaySymbols { get; }
	public virtual string[] WeekdaySymbols { get; }
```

Added methods:

```
public virtual NSComparisonResult CompareDate (NSDate date1, NSDate date2, NSCalendarUnit granularity);
	public virtual NSDateComponents ComponentsFromDateToDate (NSCalendarUnit unitFlags, NSDateComponents startingDate, NSDateComponents resultDate, NSCalendarOptions options);
	public virtual NSDateComponents ComponentsInTimeZone (NSTimeZone timezone, NSDate date);
	public virtual NSDate Date (int era, int year, int month, int date, int hour, int minute, int second, int nanosecond);
	public virtual NSDate DateByAddingUnit (NSCalendarUnit unit, int value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingsHour (int hour, int minute, int second, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingUnit (NSCalendarUnit unit, int value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateForWeekOfYear (int era, int year, int week, int weekday, int hour, int minute, int second, int nanosecond);
	public virtual void EnumerateDatesStartingAfterDate (NSDate start, NSDateComponents matchingComponents, NSCalendarOptions options, EnumerateDatesCallback callback);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSDateComponents components, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSCalendarUnit unit, int value, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, int hour, int minute, int second, NSCalendarOptions options);
	public virtual bool FindNextWeekend (out NSDate date, out double interval, NSCalendarOptions options, NSDate afterDate);
	public virtual int GetComponentFromDate (NSCalendarUnit unit, NSDate date);
	public virtual void GetComponentsFromDate (out int era, out int year, out int month, out int day, NSDate date);
	public virtual void GetComponentsFromDateForWeekOfYear (out int era, out int year, out int weekOfYear, out int weekday, NSDate date);
	public virtual void GetHourComponentsFromDate (out int hour, out int minute, out int second, out int nanosecond, NSDate date);
	public virtual bool IsDateInToday (NSDate date);
	public virtual bool IsDateInTomorrow (NSDate date);
	public virtual bool IsDateInWeekend (NSDate date);
	public virtual bool IsDateInYesterday (NSDate date);
	public virtual bool IsEqualToUnitGranularity (NSDate date1, NSDate date2, NSCalendarUnit unit);
	public virtual bool IsInSameDay (NSDate date1, NSDate date2);
	public virtual bool Matches (NSDate date, NSDateComponents components);
	public virtual bool RangeOfWeekendContainingDate (out NSDate weekendStartDate, out double interval, NSDate date);
	public virtual NSDate StartOfDayForDate (NSDate date);
```

### Type Changed: MonoTouch.Foundation.NSCalendarType

Added values:

```
Coptic = 11,
	EthiopicAmeteAlem = 12,
	EthiopicAmeteMihret = 13,
	IslamicTabular = 14,
	IslamicUmmAlQura = 15,
```

### Type Changed: MonoTouch.Foundation.NSCalendarUnit

Added value:

```
Nanosecond = 32768,
```

### Type Changed: MonoTouch.Foundation.NSComparisonPredicate

Removed methods:

```
public static NSPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
```

Added methods:

```
public static NSComparisonPredicate Create (NSExpression leftExpression, NSExpression rightExpression, NSComparisonPredicateModifier comparisonModifier, NSPredicateOperatorType operatorType, NSComparisonPredicateOptions comparisonOptions);
	public static NSComparisonPredicate FromSelector (NSExpression leftExpression, NSExpression rightExpression, MonoTouch.ObjCRuntime.Selector selector);
```

### Type Changed: MonoTouch.Foundation.NSCompoundPredicate

Removed methods:

```
public static NSPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

Added methods:

```
public static NSCompoundPredicate CreateAndPredicate (NSPredicate[] subpredicates);
	public static NSCompoundPredicate CreateNotPredicate (NSPredicate predicate);
	public static NSCompoundPredicate CreateOrPredicate (NSPredicate[] subpredicates);
```

### Type Changed: MonoTouch.Foundation.NSDateComponents

Added properties:

```
public virtual bool IsValidDate { get; }
	public virtual int Nanosecond { get; set; }
```

Added methods:

```
public virtual int GetValueForComponent (NSCalendarUnit unit);
	public virtual bool IsValidDateInCalendar (NSCalendar calendar);
	public virtual void SetValueForComponent (int value, NSCalendarUnit unit);
```

### Type Changed: MonoTouch.Foundation.NSDateFormatter

Added method:

```
public virtual void SetLocalizedDateFormatFromTemplate (string dateFormatTemplate);
```

### Type Changed: MonoTouch.Foundation.NSError

Added properties:

```
public static NSString CoreLocationErrorDomain { get; }
	public static NSString CoreMotionErrorDomain { get; }
	public static NSString EABluetoothAccessoryPickerErrorDomain { get; }
	public virtual string HelpAnchor { get; }
	public virtual string LocalizedFailureReason { get; }
	public virtual string[] LocalizedRecoveryOptions { get; }
	public virtual string LocalizedRecoverySuggestion { get; }
	public static NSString MapKitErrorDomain { get; }
	public static NSString NSNetServicesErrorDomain { get; }
	public static NSString NSStreamSocketSSLErrorDomain { get; }
	public static NSString NSStreamSOCKSErrorDomain { get; }
```

### Type Changed: MonoTouch.Foundation.NSFileCoordinator

Added property:

```
public virtual string PurposeIdentifier { get; set; }
```

Added method:

```
public virtual void CoordinateAccess (NSFileAccessIntent[] intents, NSOperationQueue executionQueue, System.Action<NSError> accessor);
```

### Type Changed: MonoTouch.Foundation.NSFileCoordinatorReadingOptions

Added values:

```
ForUploading = 8,
	ImmediatelyAvailableMetadataOnly = 4,
	ResolvesSymbolicLink = 2,
```

### Type Changed: MonoTouch.Foundation.NSFileManager

Added methods:

```
public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
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

### Type Changed: MonoTouch.Foundation.NSHttpCookieStorage

Added methods:

```
public virtual void GetCookiesForTask (NSUrlSessionTask task, System.Action<NSHttpCookie[]> completionHandler);
	public virtual void RemoveCookiesSinceDate (NSDate date);
	public virtual void StoreCookies (NSHttpCookie[] cookies, NSUrlSessionTask task);
```

### Type Changed: MonoTouch.Foundation.NSIndexPath

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoTouch.Foundation.NSIndexSet

Added interface:

```
INSSecureCoding
```

Added methods:

```
public virtual void EnumerateIndexes (NSRange range, NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (NSEnumerationOptions opts, EnumerateIndexSetCallback enumeratorCallback);
	public virtual void EnumerateIndexes (EnumerateIndexSetCallback enumeratorCallback);
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
public static NSString AccessibleUbiquitousExternalDocumentsScope { get; }
	public static NSString ContentTypeKey { get; }
	public static NSString ContentTypeTreeKey { get; }
	public static NSString UbiquitousDataScope { get; }
	public static NSString UbiquitousDocumentsScope { get; }
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

### Type Changed: MonoTouch.Foundation.NSMutableCharacterSet

Added properties:

```
public static NSCharacterSet Alphanumerics { get; }
	public static NSCharacterSet Capitalized { get; }
	public static NSCharacterSet Controls { get; }
	public static NSCharacterSet DecimalDigits { get; }
	public static NSCharacterSet Decomposables { get; }
	public static NSCharacterSet Illegals { get; }
	public static NSCharacterSet Letters { get; }
	public static NSCharacterSet LowercaseLetters { get; }
	public static NSCharacterSet Marks { get; }
	public static NSCharacterSet Newlines { get; }
	public static NSCharacterSet Punctuation { get; }
	public static NSCharacterSet Symbols { get; }
	public static NSCharacterSet UppercaseLetters { get; }
	public static NSCharacterSet WhitespaceAndNewlines { get; }
	public static NSCharacterSet Whitespaces { get; }
```

Added methods:

```
public static NSCharacterSet FromBitmapRepresentation (NSData data);
	public static NSCharacterSet FromFile (string path);
	public static NSCharacterSet FromRange (NSRange aRange);
	public static NSCharacterSet FromString (string aString);
```

### Type Changed: MonoTouch.Foundation.NSMutableIndexSet

Added interface:

```
INSSecureCoding
```

Added methods:

```
public virtual void AddIndexesInRange (NSRange range);
	public virtual void RemoveIndexesInRange (NSRange range);
```

### Type Changed: MonoTouch.Foundation.NSObject

Added methods:

```
public System.IDisposable AddObserver (string key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public System.IDisposable AddObserver (NSString key, NSKeyValueObservingOptions options, System.Action<NSObservedChange> observer);
	public void AddObserver (NSObject observer, string keyPath, NSKeyValueObservingOptions options, System.IntPtr context);
	public void RemoveObserver (NSObject observer, string keyPath, System.IntPtr context);
	public void RemoveObserver (NSObject observer, string keyPath);
	public virtual void RemoveObserver (NSObject observer, NSString keyPath, System.IntPtr context);
```

### Type Changed: MonoTouch.Foundation.NSOperation

Added properties:

```
public virtual bool Asynchronous { get; }
	public virtual string Name { get; set; }
	public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSOperationQueue

Added properties:

```
public virtual NSQualityOfService QualityOfService { get; set; }
	public virtual MonoTouch.CoreFoundation.DispatchQueue UnderlyingQueue { get; set; }
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
	public virtual void GetLineStart (out uint startPtr, out uint lineEndPtr, out uint contentsEndPtr, NSRange range);
	public virtual NSRange LineRangeForRange (NSRange range);
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
	public virtual string LastPathComponent { get; }
	public virtual string[] PathComponents { get; }
	public static NSString ThumbnailDictionaryKey { get; }
	public static NSString UbiquitousItemContainerDisplayNameKey { get; }
	public static NSString UbiquitousItemDownloadRequestedKey { get; }
```

Added methods:

```
public virtual NSUrl AppendPathExtension (string extension);
	public static NSUrl CreateFileUrl (string[] pathComponents);
	public virtual NSUrl RemoveLastPathComponent ();
	public virtual NSUrl RemovePathExtension ();
	public static NSUrl ResolveAlias (NSUrl aliasFileUrl, NSUrlBookmarkResolutionOptions options, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value);
	public virtual bool StartAccessingSecurityScopedResource ();
	public virtual void StopAccessingSecurityScopedResource ();
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
public virtual string AsString ();
```

### Type Changed: MonoTouch.Foundation.NSUrlCredentialStorage

Added methods:

```
public virtual void GetCredentials (NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task, System.Action<NSDictionary> completionHandler);
	public virtual void GetDefaultCredential (NSUrlProtectionSpace space, NSUrlSessionTask task, System.Action<NSUrlCredential> completionHandler);
	public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSDictionary options, NSUrlSessionTask task);
	public virtual void SetCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
	public virtual void SetDefaultCredential (NSUrlCredential credential, NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);
```

### Type Changed: MonoTouch.Foundation.NSUrlError

Added values:

```
BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionRequiresSharedContainer = -995,
	BackgroundSessionWasDisconnected = -997,
```

### Type Changed: MonoTouch.Foundation.NSUrlErrorCancelledReason

Added value:

```
InsufficientSystemResources = 2,
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionConfiguration

Added property:

```
public virtual string SharedContainerIdentifier { get; set; }
```

Added method:

```
public static NSUrlSessionConfiguration CreateBackgroundSessionConfiguration (string identifier);
```

Obsoleted method:

```
[Obsolete ("Starting with iOS 8, use CreateBackgroundSessionConfiguration")]
	public static NSUrlSessionConfiguration BackgroundSessionConfiguration (string identifier);
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

Added property:

```
public virtual float Priority { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionUploadTask

Removed interface:

```
INSCoding
```

### Type Changed: MonoTouch.Foundation.NSValue

Added properties:

```
public virtual MonoTouch.CoreGraphics.CGVector CGVectorValue { get; }
	public virtual MonoTouch.SceneKit.SCNMatrix4 SCNMatrix4Value { get; }
	public virtual MonoTouch.SceneKit.SCNVector3 Vector3Value { get; }
	public virtual MonoTouch.SceneKit.SCNVector4 Vector4Value { get; }
```

Added methods:

```
public static NSValue FromCGVector (MonoTouch.CoreGraphics.CGVector vector);
	public static NSValue FromSCNMatrix4 (MonoTouch.SceneKit.SCNMatrix4 matrix);
	public static NSValue FromVector (MonoTouch.SceneKit.SCNVector3 vector);
	public static NSValue FromVector (MonoTouch.SceneKit.SCNVector4 vector);
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

### New Type MonoTouch.Foundation.EnumerateDatesCallback

```
public sealed delegate EnumerateDatesCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public EnumerateDatesCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSDate date, bool exactMatch, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSDate date, bool exactMatch, ref bool stop);
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

### New Type MonoTouch.Foundation.INSUserActivityDelegate

```
public interface INSUserActivityDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
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

### New Type MonoTouch.Foundation.NSDateComponentsFormatter

```
public class NSDateComponentsFormatter : MonoTouch.Foundation.NSFormatter, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSDateComponentsFormatter ();
	public NSDateComponentsFormatter (NSCoder coder);
	public NSDateComponentsFormatter (NSObjectFlag t);
	public NSDateComponentsFormatter (System.IntPtr handle);
	// properties
	public virtual NSCalendarUnit AllowedUnits { get; set; }
	public virtual bool AllowsFractionalUnits { get; set; }
	public virtual NSCalendar Calendar { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool CollapsesLargestUnit { get; set; }
	public virtual NSFormattingContext FormattingContext { get; set; }
	public virtual bool IncludesApproximationPhrase { get; set; }
	public virtual bool IncludesTimeRemainingPhrase { get; set; }
	public virtual int MaximumUnitCount { get; set; }
	public virtual NSDateComponentsFormatterUnitsStyle UnitsStyle { get; set; }
	public virtual NSDateComponentsFormatterZeroFormattingBehavior ZeroFormattingBehavior { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public static string LocalizedStringFromDateComponents (NSDateComponents components, NSDateComponentsFormatterUnitsStyle unitsStyle);
	public virtual string StringForObjectValue (NSObject obj);
	public virtual string StringFromDate (NSDate startDate, NSDate endDate);
	public virtual string StringFromDateComponents (NSDateComponents components);
	public virtual string StringFromTimeInterval (double ti);
}
```

### New Type MonoTouch.Foundation.NSDateComponentsFormatterUnitsStyle

```
[Serializable]
public enum NSDateComponentsFormatterUnitsStyle {
	Abbreviated = 1,
	Full = 3,
	Positional = 0,
	Short = 2,
	SpellOut = 4,
}
```

### New Type MonoTouch.Foundation.NSDateComponentsFormatterZeroFormattingBehavior

```
[Serializable]
public enum NSDateComponentsFormatterZeroFormattingBehavior {
	Default = 1,
	DropAll = 14,
	DropLeading = 2,
	DropMiddle = 4,
	DropTrailing = 8,
	None = 0,
	Pad = 65536,
}
```

### New Type MonoTouch.Foundation.NSDateIntervalFormatter

```
public class NSDateIntervalFormatter : MonoTouch.Foundation.NSFormatter, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSDateIntervalFormatter ();
	public NSDateIntervalFormatter (NSCoder coder);
	public NSDateIntervalFormatter (NSObjectFlag t);
	public NSDateIntervalFormatter (System.IntPtr handle);
	// properties
	public virtual NSCalendar Calendar { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSDateIntervalFormatterStyle DateStyle { get; set; }
	public virtual string DateTemplate { get; set; }
	public virtual NSLocale Locale { get; set; }
	public virtual NSDateIntervalFormatterStyle TimeStyle { get; set; }
	public virtual NSTimeZone TimeZone { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual string StringFromDate (NSDate fromDate, NSDate toDate);
}
```

### New Type MonoTouch.Foundation.NSDateIntervalFormatterStyle

```
[Serializable]
public enum NSDateIntervalFormatterStyle {
	Full = 4,
	Long = 3,
	Medium = 2,
	None = 0,
	Short = 1,
}
```

### New Type MonoTouch.Foundation.NSEnergyFormatter

```
public class NSEnergyFormatter : MonoTouch.Foundation.NSFormatter, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSEnergyFormatter ();
	public NSEnergyFormatter (NSCoder coder);
	public NSEnergyFormatter (NSObjectFlag t);
	public NSEnergyFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForFoodEnergyUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromJoules (double numberInJoules);
	public virtual string StringFromValue (double value, NSEnergyFormatterUnit unit);
	public virtual string UnitStringFromJoules (double numberInJoules, out NSEnergyFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSEnergyFormatterUnit unit);
}
```

### New Type MonoTouch.Foundation.NSEnergyFormatterUnit

```
[Serializable]
public enum NSEnergyFormatterUnit {
	Calorie = 1793,
	Joule = 11,
	Kilocalorie = 1794,
	Kilojoule = 14,
}
```

### New Type MonoTouch.Foundation.NSExtension

```
public class NSExtension {
	// methods
	public static void Initialize ();
}
```

### New Type MonoTouch.Foundation.NSExtensionContext

```
public class NSExtensionContext : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionContext ();
	public NSExtensionContext (NSCoder coder);
	public NSExtensionContext (NSObjectFlag t);
	public NSExtensionContext (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSExtensionItem[] InputItems { get; }
	public static NSString ItemsAndErrorsKey { get; }
	// methods
	public virtual void CancelRequest (NSError error);
	public virtual void CompleteRequest (NSExtensionItem[] returningItems, System.Action<bool> completionHandler);
	protected override void Dispose (bool disposing);
	public virtual void OpenUrl (NSUrl url, System.Action<bool> completionHandler);
	public virtual System.Threading.Tasks.Task<bool> OpenUrlAsync (NSUrl url);
}
```

### New Type MonoTouch.Foundation.NSExtensionItem

```
public class NSExtensionItem : MonoTouch.Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionItem ();
	public NSExtensionItem (NSCoder coder);
	public NSExtensionItem (NSObjectFlag t);
	public NSExtensionItem (System.IntPtr handle);
	// properties
	public virtual NSItemProvider[] Attachments { get; set; }
	public static NSString AttachmentsKey { get; }
	public virtual NSAttributedString AttributedContentText { get; set; }
	public static NSString AttributedContentTextKey { get; }
	public virtual NSAttributedString AttributedTitle { get; set; }
	public static NSString AttributedTitleKey { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSDictionary UserInfo { get; set; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Foundation.NSExtensionRequestHandling

```
public abstract class NSExtensionRequestHandling : MonoTouch.Foundation.NSObject, INSExtensionRequestHandling, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionRequestHandling ();
	public NSExtensionRequestHandling (NSCoder coder);
	public NSExtensionRequestHandling (NSObjectFlag t);
	public NSExtensionRequestHandling (System.IntPtr handle);
	// methods
	public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
}
```

### New Type MonoTouch.Foundation.NSExtensionRequestHandling_Extensions

```
public static class NSExtensionRequestHandling_Extensions {
}
```

### New Type MonoTouch.Foundation.NSFileAccessIntent

```
public class NSFileAccessIntent : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSFileAccessIntent (NSCoder coder);
	public NSFileAccessIntent (NSObjectFlag t);
	public NSFileAccessIntent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrl Url { get; }
	// methods
	public static NSFileAccessIntent CreateReadingIntent (NSUrl url, NSFileCoordinatorReadingOptions options);
	public static NSFileAccessIntent CreateWritingIntent (NSUrl url, NSFileCoordinatorWritingOptions options);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Foundation.NSFormattingContext

```
[Serializable]
public enum NSFormattingContext {
	BeginningOfSentence = 4,
	Dynamic = 1,
	ListItem = 3,
	MiddleOfSentence = 5,
	Standalone = 2,
	Unknown = 0,
}
```

### New Type MonoTouch.Foundation.NSFormattingUnitStyle

```
[Serializable]
public enum NSFormattingUnitStyle {
	Long = 3,
	Medium = 2,
	Short = 1,
}
```

### New Type MonoTouch.Foundation.NSItemProvider

```
public class NSItemProvider : MonoTouch.Foundation.NSObject, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSItemProvider ();
	public NSItemProvider (NSCoder coder);
	public NSItemProvider (NSObjectFlag t);
	public NSItemProvider (System.IntPtr handle);
	public NSItemProvider (NSObject item, string typeIdentifier);
	public NSItemProvider (NSUrl fileUrl);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static NSString ErrorDomain { get; }
	public static NSString PreferredImageSizeKey { get; }
	public virtual string[] RegisteredTypeIdentifiers { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	public virtual bool HasItemConformingTo (string typeIdentifier);
	public virtual void LoadItem (string typeIdentifier, NSDictionary options, System.Action<NSObject,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void LoadPreviewImage (NSDictionary options, System.Action<NSObject,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void RegisterItemForTypeIdentifier (string typeIdentifier, NSItemProviderLoadHandler loadHandler);
	public virtual void SetPreviewImageHandler (NSItemProviderLoadHandler handler);
}
```

### New Type MonoTouch.Foundation.NSItemProviderCompletionHandler

```
public sealed delegate NSItemProviderCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSItemProviderCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSObject itemBeingLoaded, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSObject itemBeingLoaded, NSError error);
}
```

### New Type MonoTouch.Foundation.NSItemProviderErrorCode

```
[Serializable]
public enum NSItemProviderErrorCode {
	ItemUnavailable = -1000,
	None = 0,
	UnexpectedValueClass = -1100,
	Unknown = -1,
}
```

### New Type MonoTouch.Foundation.NSItemProviderLoadHandler

```
public sealed delegate NSItemProviderLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSItemProviderLoadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSItemProviderCompletionHandler completionHandler, MonoTouch.ObjCRuntime.Class expectedValueClass, NSDictionary options, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSItemProviderCompletionHandler completionHandler, MonoTouch.ObjCRuntime.Class expectedValueClass, NSDictionary options);
}
```

### New Type MonoTouch.Foundation.NSLengthFormatter

```
public class NSLengthFormatter : MonoTouch.Foundation.NSFormatter, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSLengthFormatter ();
	public NSLengthFormatter (NSCoder coder);
	public NSLengthFormatter (NSObjectFlag t);
	public NSLengthFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForPersonHeightUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromMeters (double numberInMeters);
	public virtual string StringFromValue (double value, NSLengthFormatterUnit unit);
	public virtual string UnitStringFromMeters (double numberInMeters, ref NSLengthFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSLengthFormatterUnit unit);
}
```

### New Type MonoTouch.Foundation.NSLengthFormatterUnit

```
[Serializable]
public enum NSLengthFormatterUnit {
	Centimeter = 9,
	Foot = 1282,
	Inch = 1281,
	Kilometer = 14,
	Meter = 11,
	Mile = 1284,
	Millimeter = 8,
	Yard = 1283,
}
```

### New Type MonoTouch.Foundation.NSMassFormatter

```
public class NSMassFormatter : MonoTouch.Foundation.NSFormatter, INSCoding, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSMassFormatter ();
	public NSMassFormatter (NSCoder coder);
	public NSMassFormatter (NSObjectFlag t);
	public NSMassFormatter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ForPersonMassUse { get; set; }
	public virtual NSNumberFormatter NumberFormatter { get; set; }
	public virtual NSFormattingUnitStyle UnitStyle { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool GetObjectValue (out NSObject obj, string str, out string error);
	public virtual string StringFromKilograms (double numberInKilograms);
	public virtual string StringFromValue (double value, NSMassFormatterUnit unit);
	public virtual string UnitStringFromKilograms (double numberInKilograms, ref NSMassFormatterUnit unitp);
	public virtual string UnitStringFromValue (double value, NSMassFormatterUnit unit);
}
```

### New Type MonoTouch.Foundation.NSMassFormatterUnit

```
[Serializable]
public enum NSMassFormatterUnit {
	Gram = 11,
	Kilogram = 14,
	Ounce = 1537,
	Pound = 1538,
	Stone = 1539,
}
```

### New Type MonoTouch.Foundation.NSObservedChange

```
public class NSObservedChange {
	// properties
	public NSKeyValueChange Change { get; }
	public NSIndexSet Indexes { get; }
	public bool IsPrior { get; }
	public NSObject NewValue { get; }
	public NSObject OldValue { get; }
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

### New Type MonoTouch.Foundation.NSQualityOfService

```
[Serializable]
public enum NSQualityOfService {
	Background = 9,
	Default = -1,
	UserInitiated = 25,
	UserInteractive = 33,
	Utility = 17,
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

### New Type MonoTouch.Foundation.NSURLSessionTaskPriority

```
public static class NSURLSessionTaskPriority {
	// properties
	public static float Default { get; }
	public static float High { get; }
	public static float Low { get; }
}
```

### New Type MonoTouch.Foundation.NSUserActivity

```
public class NSUserActivity : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUserActivity ();
	public NSUserActivity (NSCoder coder);
	public NSUserActivity (NSObjectFlag t);
	public NSUserActivity (System.IntPtr handle);
	public NSUserActivity (NSString activityType);
	// properties
	public virtual string ActivityType { get; }
	public override System.IntPtr ClassHandle { get; }
	public NSUserActivityDelegate Delegate { get; set; }
	public virtual bool NeedsSave { get; set; }
	public virtual bool SupportsContinuationStreams { get; set; }
	public virtual string Title { get; set; }
	public virtual NSDictionary UserInfo { get; set; }
	public virtual NSObject WeakDelegate { get; set; }
	public virtual NSUrl WebPageUrl { get; set; }
	// methods
	public virtual void AddUserInfoEntries (NSDictionary otherDictionary);
	public virtual void BecomeCurrent ();
	protected override void Dispose (bool disposing);
	public virtual void GetContinuationStreams (System.Action<NSInputStream,MonoTouch.Foundation.NSOutputStream,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<NSUserActivityContinuation> GetContinuationStreamsAsync ();
	public virtual void Invalidate ();
}
```

### New Type MonoTouch.Foundation.NSUserActivityContinuation

```
public class NSUserActivityContinuation {
	// constructors
	public NSUserActivityContinuation (NSInputStream arg1, NSOutputStream arg2);
	// properties
	public NSInputStream Arg1 { get; set; }
	public NSOutputStream Arg2 { get; set; }
}
```

### New Type MonoTouch.Foundation.NSUserActivityDelegate

```
public class NSUserActivityDelegate : MonoTouch.Foundation.NSObject, INSUserActivityDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUserActivityDelegate ();
	public NSUserActivityDelegate (NSCoder coder);
	public NSUserActivityDelegate (NSObjectFlag t);
	public NSUserActivityDelegate (System.IntPtr handle);
	// methods
	public virtual void UserActivityReceivedData (NSUserActivity userActivity, NSInputStream inputStream, NSOutputStream outputStream);
	public virtual void UserActivityWasContinued (NSUserActivity userActivity);
	public virtual void UserActivityWillSave (NSUserActivity userActivity);
}
```

### New Type MonoTouch.Foundation.NSUserActivityDelegate_Extensions

```
public static class NSUserActivityDelegate_Extensions {
	// methods
	public static void UserActivityReceivedData (INSUserActivityDelegate This, NSUserActivity userActivity, NSInputStream inputStream, NSOutputStream outputStream);
	public static void UserActivityWasContinued (INSUserActivityDelegate This, NSUserActivity userActivity);
	public static void UserActivityWillSave (INSUserActivityDelegate This, NSUserActivity userActivity);
}
```

### New Type MonoTouch.Foundation.NSUserActivityType

```
public static class NSUserActivityType {
	// properties
	public static NSString BrowsingWeb { get; }
}
```

## Namespace MonoTouch.GameController

### Type Changed: MonoTouch.GameController.GCController

Added property:

```
public virtual GCMotion Motion { get; }
```

### Type Changed: MonoTouch.GameController.GCControllerButtonInput

Removed property:

```
public virtual GCControllerButtonValueChangedHandler ValueChangedHandler { get; set; }
```

Added methods:

```
public virtual void SetPressedChangedHandler (GCControllerButtonValueChanged handler);
	public virtual void SetValueChangedHandler (GCControllerButtonValueChanged handler);
```

### Removed Type MonoTouch.GameController.GCControllerButtonValueChangedHandler ### New Type MonoTouch.GameController.GCControllerButtonValueChanged

```
public sealed delegate GCControllerButtonValueChanged : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GCControllerButtonValueChanged (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (GCControllerButtonInput button, float buttonValue, bool pressed, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (GCControllerButtonInput button, float buttonValue, bool pressed);
}
```

### New Type MonoTouch.GameController.GCMotion

```
public class GCMotion : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GCMotion (MonoTouch.Foundation.NSCoder coder);
	public GCMotion (MonoTouch.Foundation.NSObjectFlag t);
	public GCMotion (System.IntPtr handle);
	// properties
	public virtual OpenTK.Quaterniond Attitude { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual GCController Controller { get; }
	public virtual OpenTK.Vector3d Gravity { get; }
	public virtual OpenTK.Vector3d RotationRate { get; }
	public virtual OpenTK.Vector3d UserAcceleration { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetValueChangedHandler (System.Action<GCMotion> handler);
}
```



## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievement

Added constructor:

```
public GKAchievement (string identifier, GKPlayer player);
```

Added property:

```
public virtual GKPlayer Player { get; }
```

Added methods:

```
public virtual MonoTouch.UIKit.UIViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
	public virtual MonoTouch.UIKit.UIViewController ChallengeComposeController (GKPlayer[] playerIDs, string message, GKChallengeComposeHandler completionHandler);
	public virtual void SelectChallengeablePlayers (GKPlayer[] players, System.Action<GKPlayer[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> SelectChallengeablePlayersAsync (GKPlayer[] players);
```

### Type Changed: MonoTouch.GameKit.GKAchievementDescription

Obsoleted property:

```
[Obsolete ("Deprecated in iOS 7.0")]
	public virtual MonoTouch.UIKit.UIImage Image { get; }
```

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKChallenge

Added properties:

```
public virtual GKPlayer IssuingPlayer { get; }
	public virtual GKPlayer ReceivingPlayer { get; }
```

### Type Changed: MonoTouch.GameKit.GKError

Added values:

```
PlayerPhotoFailure = 26,
	UbiquityContainerUnavailable = 27,
```

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public virtual void AddRecipientPlayers (GKPlayer[] players);
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKGameCenterViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

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

### Type Changed: MonoTouch.GameKit.GKLeaderboard

Added constructor:

```
public GKLeaderboard (GKPlayer[] players);
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKLocalPlayer

Added methods:

```
public virtual void DeleteSavedGames (string name, System.Action<MonoTouch.Foundation.NSError> handler);
	public virtual void FetchSavedGames (System.Action<GKSavedGame[],MonoTouch.Foundation.NSError> handler);
	public virtual void LoadFriendPlayers (System.Action<GKPlayer[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> LoadFriendPlayersAsync ();
	public virtual void ResolveConflictingSavedGames (GKSavedGame[] conflictingSavedGames, MonoTouch.Foundation.NSData data, System.Action<GKSavedGame[],MonoTouch.Foundation.NSError> handler);
	public virtual void SaveGameData (MonoTouch.Foundation.NSData data, string name, System.Action<GKSavedGame,MonoTouch.Foundation.NSError> handler);
```

### Type Changed: MonoTouch.GameKit.GKLocalPlayerListener

Added interface:

```
IGKSavedGameListener
```

Added methods:

```
public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
	public virtual void HasConflictingSavedGames (GKPlayer player, GKSavedGame[] savedGames);
```

### Type Changed: MonoTouch.GameKit.GKMatch

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public GKMatchReinvitationForDisconnectedPlayer ShouldReinviteDisconnectedPlayer { get; set; }
```

Added events:

```
public event System.EventHandler<GKMatchReceivedDataFromRemotePlayerEventArgs> DataReceivedFromPlayer;
	public event System.EventHandler<GKMatchConnectionChangedEventArgs> StateChangedForPlayer;
```

Removed method:

```
public virtual bool SendDataToAllPlayers (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, System.IntPtr ptrToNSErrorHandle);
```

Added methods:

```
public virtual void ChooseBestHostingPlayer (System.Action<GKPlayer> completionHandler);
	public virtual bool SendData (MonoTouch.Foundation.NSData data, string[] players, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
	public virtual bool SendData (MonoTouch.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
	public virtual bool SendDataToAllPlayer (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate

Added methods:

```
public virtual void DataReceivedFromPlayer (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
	public virtual bool ShouldReinviteDisconnectedPlayer (GKMatch match, GKPlayer player);
	public virtual void StateChangedForPlayer (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
```

### Type Changed: MonoTouch.GameKit.GKMatchDelegate_Extensions

Added methods:

```
public static void DataReceived (IGKMatchDelegate This, GKMatch match, MonoTouch.Foundation.NSData data, string playerId);
	public static void DataReceivedFromPlayer (IGKMatchDelegate This, GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
	public static bool ShouldReinviteDisconnectedPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player);
	public static void StateChangedForPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player, GKPlayerConnectionState state);
```

### Type Changed: MonoTouch.GameKit.GKMatchmaker

Added methods:

```
public virtual void CancelPendingInvite (GKPlayer player);
	public virtual void FindPlayersForHostedRequest (GKMatchRequest request, System.Action<GKPlayer[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> FindPlayersForHostedRequestAsync (GKMatchRequest request);
	public virtual void StartBrowsingForNearbyPlayers (System.Action<GKPlayer,System.Boolean> handler);
```

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added events:

```
public event System.EventHandler<GKMatchmakingPlayersEventArgs> DidFindHostedPlayers;
	public event System.EventHandler<GKMatchmakingPlayerEventArgs> HostedPlayerDidAccept;
```

Added method:

```
public virtual void SetHostedPlayerConnected (GKPlayer playerID, bool connected);
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

Added property:

```
public virtual GKPlayer[] Recipients { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetRecipientResponseHandler (System.Action<GKPlayer,MonoTouch.GameKit.GKInviteRecipientResponse> handler);
```

### Type Changed: MonoTouch.GameKit.GKScore

Added constructor:

```
public GKScore (string identifier, GKPlayer player);
```

Added property:

```
public virtual GKPlayer GamePlayer { get; }
```

Added method:

```
public virtual MonoTouch.UIKit.UIViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
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

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedParticipant

Added property:

```
public virtual GKPlayer Player { get; }
```

### Type Changed: MonoTouch.GameKit.GKVoiceChat

Added property:

```
public virtual GKPlayer[] Players { get; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetMuteStatus (GKPlayer player, bool isMuted);
	public virtual void SetPlayerVoiceChatStateChangeHandler (System.Action<GKPlayer,MonoTouch.GameKit.GKVoiceChatPlayerState> handler);
```

### Type Changed: MonoTouch.GameKit.IGKLocalPlayerListener

Added interface:

```
IGKSavedGameListener
```

### Type Changed: MonoTouch.GameKit.IGKMatchDelegate

Removed method:

```
public virtual void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, string playerId);
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
	public virtual void LoadData (System.Action<MonoTouch.Foundation.NSData,MonoTouch.Foundation.NSError> handler);
	public virtual System.Threading.Tasks.Task<MonoTouch.Foundation.NSData> LoadDataAsync ();
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
	public virtual void HasConflictingSavedGames (GKPlayer player, GKSavedGame[] savedGames);
}
```

### New Type MonoTouch.GameKit.GKSavedGameListener_Extensions

```
public static class GKSavedGameListener_Extensions {
	// methods
	public static void DidModifySavedGame (IGKSavedGameListener This, GKPlayer player, GKSavedGame savedGame);
	public static void HasConflictingSavedGames (IGKSavedGameListener This, GKPlayer player, GKSavedGame[] savedGames);
}
```

### New Type MonoTouch.GameKit.IGKSavedGameListener

```
public interface IGKSavedGameListener : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GLKit.GLKViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static ADBannerView.ADBannerViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.iAd.ADClient

Added methods:

```
public virtual void AddClientToSegments (string[] segmentIdentifiers, bool replaceExisting);
	public virtual void LookupAdConversionDetails (ADConversionDetails onCompleted);
	public virtual System.Threading.Tasks.Task<ADClientConversionDetailsResult> LookupAdConversionDetailsAsync ();
```

### Type Changed: MonoTouch.iAd.IAdPreroll

Added method:

```
public static void CancelPreroll (MonoTouch.MediaPlayer.MPMoviePlayerController This);
```

### New Type MonoTouch.iAd.ADClientConversionDetailsResult

```
public class ADClientConversionDetailsResult {
	// constructors
	public ADClientConversionDetailsResult (MonoTouch.Foundation.NSDate appPurchaseDate, MonoTouch.Foundation.NSDate iAdImpressionDate);
	// properties
	public MonoTouch.Foundation.NSDate AppPurchaseDate { get; set; }
	public MonoTouch.Foundation.NSDate IAdImpressionDate { get; set; }
}
```

### New Type MonoTouch.iAd.ADConversionDetails

```
public sealed delegate ADConversionDetails : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public ADConversionDetails (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDate appPurchaseDate, MonoTouch.Foundation.NSDate iAdImpressionDate, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDate appPurchaseDate, MonoTouch.Foundation.NSDate iAdImpressionDate);
}
```

### New Type MonoTouch.iAd.iAdPreroll_AVPlayerViewController

```
public static class iAdPreroll_AVPlayerViewController {
	// methods
	public static void CancelPreroll (MonoTouch.AVKit.AVPlayerViewController This);
	public static void PlayPrerollAd (MonoTouch.AVKit.AVPlayerViewController This, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public static void PreparePrerollAds (MonoTouch.AVKit.AVPlayerViewController This);
}
```

## Namespace MonoTouch.ImageIO

### Type Changed: MonoTouch.ImageIO.CGImageDestinationOptions

Added properties:

```
public bool EmbedThumbnail { get; set; }
	public int? ImageMaxPixelSize { get; set; }
	public bool ShouldExcludeGPS { get; set; }
```

### Type Changed: MonoTouch.ImageIO.CGImageProperties

Added properties:

```
public static MonoTouch.Foundation.NSString GPSHPositioningError { get; }
	public static MonoTouch.Foundation.NSString PNGDelayTime { get; }
	public static MonoTouch.Foundation.NSString PNGLoopCount { get; }
	public static MonoTouch.Foundation.NSString PNGUnclampedDelayTime { get; }
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

Added properties:

```
public static JSValue CurrentCallee { get; }
	public virtual System.IntPtr JSGlobalContextRefPtr { get; }
	public virtual string Name { get; set; }
```

Added methods:

```
public virtual JSValue EvaluateScript (string script, MonoTouch.Foundation.NSUrl sourceUrl);
	public static JSContext FromJSGlobalContextRef (System.IntPtr nativeJsGlobalContextRef);
```

### Type Changed: MonoTouch.JavaScriptCore.JSManagedValue

Added method:

```
public static JSManagedValue Get (JSValue value, MonoTouch.Foundation.NSObject owner);
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

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.IMKOverlay

Added interface:

```
IMKAnnotation
```

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKLaunchOptions

Added property:

```
public MKMapCamera Camera { get; set; }
```

### Type Changed: MonoTouch.MapKit.MKLocalSearch

Obsoleted constructor:

```
[Obsolete ("This will not work on iOS8+")]
	public MKLocalSearch ();
```

### Type Changed: MonoTouch.MapKit.MKMapView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPinAnnotationView.MKPinAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPlacemark

Added constructor:

```
public MKPlacemark (MonoTouch.CoreLocation.CLLocationCoordinate2D coordinate, MKPlacemarkAddress addressDictionary);
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKTileOverlayRenderer

Obsoleted constructor:

```
[Obsolete ("This will not work on iOS8+")]
	public MKTileOverlayRenderer ();
```

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Added methods:

```
public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKUserTrackingBarButtonItem.MKUserTrackingBarButtonItemAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### New Type MonoTouch.MapKit.MKPlacemarkAddress

```
public class MKPlacemarkAddress : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public MKPlacemarkAddress ();
	public MKPlacemarkAddress (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public string City { get; set; }
	public string Country { get; set; }
	public string CountryCode { get; set; }
	public string State { get; set; }
	public string Street { get; set; }
	public string Zip { get; set; }
}
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylist

Added properties:

```
public virtual string Name { get; }
	public virtual ulong PersistentID { get; }
	public virtual MPMediaPlaylistAttribute PlaylistAttributes { get; }
	public virtual MPMediaItem[] SeedItems { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaQuery

Added methods:

```
public MPMediaItemCollection GetCollection (int index);
	public MPMediaItem GetItem (int index);
	public MPMediaQuerySection GetSection (int index);
```

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Removed methods:

```
public virtual MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations ();
	public virtual bool ShouldAutorotate ();
```

### Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added property:

```
public static MPMusicPlayerController SystemMusicPlayer { get; }
```

### Type Changed: MonoTouch.MediaPlayer.MPNowPlayingInfo

Added field:

```
public double? DefaultPlaybackRate;
```

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Removed method:

```
public virtual System.Drawing.SizeF SizeThatFits (System.Drawing.SizeF f);
```

Added methods:

```
public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static MPVolumeView.MPVolumeViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.IMFMailComposeViewControllerDelegate

Added interface:

```
MonoTouch.UIKit.IUINavigationControllerDelegate
```

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added methods:

```
public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.MobileCoreServices

### Type Changed: MonoTouch.MobileCoreServices.UTType

Removed fields:

```
public static MonoTouch.Foundation.NSString AliasFile;
	public static MonoTouch.Foundation.NSString AliasRecord;
	public static MonoTouch.Foundation.NSString AppleICNS;
	public static MonoTouch.Foundation.NSString AppleProtectedMPEG4Audio;
	public static MonoTouch.Foundation.NSString Application;
	public static MonoTouch.Foundation.NSString ApplicationBundle;
	public static MonoTouch.Foundation.NSString ApplicationFile;
	public static MonoTouch.Foundation.NSString Archive;
	public static MonoTouch.Foundation.NSString Audio;
	public static MonoTouch.Foundation.NSString AudiovisualContent;
	public static MonoTouch.Foundation.NSString BMP;
	public static MonoTouch.Foundation.NSString Bundle;
	public static MonoTouch.Foundation.NSString CHeader;
	public static MonoTouch.Foundation.NSString CompositeContent;
	public static MonoTouch.Foundation.NSString ConformsToKey;
	public static MonoTouch.Foundation.NSString Contact;
	public static MonoTouch.Foundation.NSString Content;
	public static MonoTouch.Foundation.NSString CPlusPlusHeader;
	public static MonoTouch.Foundation.NSString CPlusPlusSource;
	public static MonoTouch.Foundation.NSString CSource;
	public static MonoTouch.Foundation.NSString Data;
	public static MonoTouch.Foundation.NSString DescriptionKey;
	public static MonoTouch.Foundation.NSString Directory;
	public static MonoTouch.Foundation.NSString DiskImage;
	public static MonoTouch.Foundation.NSString ExportedTypeDeclarationsKey;
	public static MonoTouch.Foundation.NSString FileURL;
	public static MonoTouch.Foundation.NSString FlatRTFD;
	public static MonoTouch.Foundation.NSString Folder;
	public static MonoTouch.Foundation.NSString Framework;
	public static MonoTouch.Foundation.NSString GIF;
	public static MonoTouch.Foundation.NSString HTML;
	public static MonoTouch.Foundation.NSString ICO;
	public static MonoTouch.Foundation.NSString IconFileKey;
	public static MonoTouch.Foundation.NSString IdentifierKey;
	public static MonoTouch.Foundation.NSString Image;
	public static MonoTouch.Foundation.NSString ImportedTypeDeclarationsKey;
	public static MonoTouch.Foundation.NSString InkText;
	public static MonoTouch.Foundation.NSString Item;
	public static MonoTouch.Foundation.NSString JavaSource;
	public static MonoTouch.Foundation.NSString JPEG;
	public static MonoTouch.Foundation.NSString JPEG2000;
	public static MonoTouch.Foundation.NSString Message;
	public static MonoTouch.Foundation.NSString MountPoint;
	public static MonoTouch.Foundation.NSString Movie;
	public static MonoTouch.Foundation.NSString MP3;
	public static MonoTouch.Foundation.NSString MPEG;
	public static MonoTouch.Foundation.NSString MPEG4;
	public static MonoTouch.Foundation.NSString MPEG4Audio;
	public static MonoTouch.Foundation.NSString ObjectiveCPlusPlusSource;
	public static MonoTouch.Foundation.NSString ObjectiveCSource;
	public static MonoTouch.Foundation.NSString Package;
	public static MonoTouch.Foundation.NSString PDF;
	public static MonoTouch.Foundation.NSString PICT;
	public static MonoTouch.Foundation.NSString PlainText;
	public static MonoTouch.Foundation.NSString PNG;
	public static MonoTouch.Foundation.NSString QuickTimeImage;
	public static MonoTouch.Foundation.NSString QuickTimeMovie;
	public static MonoTouch.Foundation.NSString ReferenceURLKey;
	public static MonoTouch.Foundation.NSString Resolvable;
	public static MonoTouch.Foundation.NSString RTF;
	public static MonoTouch.Foundation.NSString RTFD;
	public static MonoTouch.Foundation.NSString SourceCode;
	public static MonoTouch.Foundation.NSString SymLink;
	public static MonoTouch.Foundation.NSString TagClassFilenameExtension;
	public static MonoTouch.Foundation.NSString TagClassMIMEType;
	public static MonoTouch.Foundation.NSString TagSpecificationKey;
	public static MonoTouch.Foundation.NSString Text;
	public static MonoTouch.Foundation.NSString TIFF;
	public static MonoTouch.Foundation.NSString TXNTextAndMultimediaData;
	public static MonoTouch.Foundation.NSString URL;
	public static MonoTouch.Foundation.NSString UTF16ExternalPlainText;
	public static MonoTouch.Foundation.NSString UTF16PlainText;
	public static MonoTouch.Foundation.NSString UTF8PlainText;
	public static MonoTouch.Foundation.NSString VCard;
	public static MonoTouch.Foundation.NSString VersionKey;
	public static MonoTouch.Foundation.NSString Video;
	public static MonoTouch.Foundation.NSString Volume;
	public static MonoTouch.Foundation.NSString WebArchive;
	public static MonoTouch.Foundation.NSString XML;
```

Added properties:

```
public static MonoTouch.Foundation.NSString AliasFile { get; }
	public static MonoTouch.Foundation.NSString AliasRecord { get; }
	public static MonoTouch.Foundation.NSString AppleICNS { get; }
	public static MonoTouch.Foundation.NSString AppleProtectedMPEG4Audio { get; }
	public static MonoTouch.Foundation.NSString AppleProtectedMPEG4Video { get; }
	public static MonoTouch.Foundation.NSString AppleScript { get; }
	public static MonoTouch.Foundation.NSString Application { get; }
	public static MonoTouch.Foundation.NSString ApplicationBundle { get; }
	public static MonoTouch.Foundation.NSString ApplicationFile { get; }
	public static MonoTouch.Foundation.NSString Archive { get; }
	public static MonoTouch.Foundation.NSString AssemblyLanguageSource { get; }
	public static MonoTouch.Foundation.NSString Audio { get; }
	public static MonoTouch.Foundation.NSString AudioInterchangeFileFormat { get; }
	public static MonoTouch.Foundation.NSString AudiovisualContent { get; }
	public static MonoTouch.Foundation.NSString AVIMovie { get; }
	public static MonoTouch.Foundation.NSString BinaryPropertyList { get; }
	public static MonoTouch.Foundation.NSString BMP { get; }
	public static MonoTouch.Foundation.NSString Bookmark { get; }
	public static MonoTouch.Foundation.NSString Bundle { get; }
	public static MonoTouch.Foundation.NSString Bzip2Archive { get; }
	public static MonoTouch.Foundation.NSString CalendarEvent { get; }
	public static MonoTouch.Foundation.NSString CHeader { get; }
	public static MonoTouch.Foundation.NSString CommaSeparatedText { get; }
	public static MonoTouch.Foundation.NSString CompositeContent { get; }
	public static MonoTouch.Foundation.NSString ConformsToKey { get; }
	public static MonoTouch.Foundation.NSString Contact { get; }
	public static MonoTouch.Foundation.NSString Content { get; }
	public static MonoTouch.Foundation.NSString CPlusPlusHeader { get; }
	public static MonoTouch.Foundation.NSString CPlusPlusSource { get; }
	public static MonoTouch.Foundation.NSString CSource { get; }
	public static MonoTouch.Foundation.NSString Data { get; }
	public static MonoTouch.Foundation.NSString Database { get; }
	public static MonoTouch.Foundation.NSString DelimitedText { get; }
	public static MonoTouch.Foundation.NSString DescriptionKey { get; }
	public static MonoTouch.Foundation.NSString Directory { get; }
	public static MonoTouch.Foundation.NSString DiskImage { get; }
	public static MonoTouch.Foundation.NSString ElectronicPublication { get; }
	public static MonoTouch.Foundation.NSString EmailMessage { get; }
	public static MonoTouch.Foundation.NSString Executable { get; }
	public static MonoTouch.Foundation.NSString ExportedTypeDeclarationsKey { get; }
	public static MonoTouch.Foundation.NSString FileURL { get; }
	public static MonoTouch.Foundation.NSString FlatRTFD { get; }
	public static MonoTouch.Foundation.NSString Folder { get; }
	public static MonoTouch.Foundation.NSString Font { get; }
	public static MonoTouch.Foundation.NSString Framework { get; }
	public static MonoTouch.Foundation.NSString GIF { get; }
	public static MonoTouch.Foundation.NSString GNUZipArchive { get; }
	public static MonoTouch.Foundation.NSString HTML { get; }
	public static MonoTouch.Foundation.NSString ICO { get; }
	public static MonoTouch.Foundation.NSString IconFileKey { get; }
	public static MonoTouch.Foundation.NSString IdentifierKey { get; }
	public static MonoTouch.Foundation.NSString Image { get; }
	public static MonoTouch.Foundation.NSString ImportedTypeDeclarationsKey { get; }
	public static MonoTouch.Foundation.NSString InkText { get; }
	public static MonoTouch.Foundation.NSString InternetLocation { get; }
	public static MonoTouch.Foundation.NSString Item { get; }
	public static MonoTouch.Foundation.NSString JavaArchive { get; }
	public static MonoTouch.Foundation.NSString JavaClass { get; }
	public static MonoTouch.Foundation.NSString JavaScript { get; }
	public static MonoTouch.Foundation.NSString JavaSource { get; }
	public static MonoTouch.Foundation.NSString JPEG { get; }
	public static MonoTouch.Foundation.NSString JPEG2000 { get; }
	public static MonoTouch.Foundation.NSString JSON { get; }
	public static MonoTouch.Foundation.NSString Log { get; }
	public static MonoTouch.Foundation.NSString M3UPlaylist { get; }
	public static MonoTouch.Foundation.NSString Message { get; }
	public static MonoTouch.Foundation.NSString MIDIAudio { get; }
	public static MonoTouch.Foundation.NSString MountPoint { get; }
	public static MonoTouch.Foundation.NSString Movie { get; }
	public static MonoTouch.Foundation.NSString MP3 { get; }
	public static MonoTouch.Foundation.NSString MPEG { get; }
	public static MonoTouch.Foundation.NSString MPEG2TransportStream { get; }
	public static MonoTouch.Foundation.NSString MPEG2Video { get; }
	public static MonoTouch.Foundation.NSString MPEG4 { get; }
	public static MonoTouch.Foundation.NSString MPEG4Audio { get; }
	public static MonoTouch.Foundation.NSString ObjectiveCPlusPlusSource { get; }
	public static MonoTouch.Foundation.NSString ObjectiveCSource { get; }
	public static MonoTouch.Foundation.NSString OSAScript { get; }
	public static MonoTouch.Foundation.NSString OSAScriptBundle { get; }
	public static MonoTouch.Foundation.NSString Package { get; }
	public static MonoTouch.Foundation.NSString PDF { get; }
	public static MonoTouch.Foundation.NSString PerlScript { get; }
	public static MonoTouch.Foundation.NSString PHPScript { get; }
	public static MonoTouch.Foundation.NSString PICT { get; }
	public static MonoTouch.Foundation.NSString PKCS12 { get; }
	public static MonoTouch.Foundation.NSString PlainText { get; }
	public static MonoTouch.Foundation.NSString Playlist { get; }
	public static MonoTouch.Foundation.NSString PluginBundle { get; }
	public static MonoTouch.Foundation.NSString PNG { get; }
	public static MonoTouch.Foundation.NSString Presentation { get; }
	public static MonoTouch.Foundation.NSString PropertyList { get; }
	public static MonoTouch.Foundation.NSString PythonScript { get; }
	public static MonoTouch.Foundation.NSString QuickLookGenerator { get; }
	public static MonoTouch.Foundation.NSString QuickTimeImage { get; }
	public static MonoTouch.Foundation.NSString QuickTimeMovie { get; }
	public static MonoTouch.Foundation.NSString RawImage { get; }
	public static MonoTouch.Foundation.NSString ReferenceURLKey { get; }
	public static MonoTouch.Foundation.NSString Resolvable { get; }
	public static MonoTouch.Foundation.NSString RTF { get; }
	public static MonoTouch.Foundation.NSString RTFD { get; }
	public static MonoTouch.Foundation.NSString RubyScript { get; }
	public static MonoTouch.Foundation.NSString ScalableVectorGraphics { get; }
	public static MonoTouch.Foundation.NSString Script { get; }
	public static MonoTouch.Foundation.NSString ShellScript { get; }
	public static MonoTouch.Foundation.NSString SourceCode { get; }
	public static MonoTouch.Foundation.NSString SpotlightImporter { get; }
	public static MonoTouch.Foundation.NSString Spreadsheet { get; }
	public static MonoTouch.Foundation.NSString SymLink { get; }
	public static MonoTouch.Foundation.NSString SystemPreferencesPane { get; }
	public static MonoTouch.Foundation.NSString TabSeparatedText { get; }
	public static MonoTouch.Foundation.NSString TagClassFilenameExtension { get; }
	public static MonoTouch.Foundation.NSString TagClassMIMEType { get; }
	public static MonoTouch.Foundation.NSString TagSpecificationKey { get; }
	public static MonoTouch.Foundation.NSString Text { get; }
	public static MonoTouch.Foundation.NSString ThreeDContent { get; }
	public static MonoTouch.Foundation.NSString TIFF { get; }
	public static MonoTouch.Foundation.NSString ToDoItem { get; }
	public static MonoTouch.Foundation.NSString TXNTextAndMultimediaData { get; }
	public static MonoTouch.Foundation.NSString UnixExecutable { get; }
	public static MonoTouch.Foundation.NSString URL { get; }
	public static MonoTouch.Foundation.NSString URLBookmarkData { get; }
	public static MonoTouch.Foundation.NSString UTF16ExternalPlainText { get; }
	public static MonoTouch.Foundation.NSString UTF16PlainText { get; }
	public static MonoTouch.Foundation.NSString UTF8PlainText { get; }
	public static MonoTouch.Foundation.NSString UTF8TabSeparatedText { get; }
	public static MonoTouch.Foundation.NSString VCard { get; }
	public static MonoTouch.Foundation.NSString VersionKey { get; }
	public static MonoTouch.Foundation.NSString Video { get; }
	public static MonoTouch.Foundation.NSString Volume { get; }
	public static MonoTouch.Foundation.NSString WaveformAudio { get; }
	public static MonoTouch.Foundation.NSString WebArchive { get; }
	public static MonoTouch.Foundation.NSString WindowsExecutable { get; }
	public static MonoTouch.Foundation.NSString X509Certificate { get; }
	public static MonoTouch.Foundation.NSString XML { get; }
	public static MonoTouch.Foundation.NSString XMLPropertyList { get; }
	public static MonoTouch.Foundation.NSString XPCService { get; }
	public static MonoTouch.Foundation.NSString ZipArchive { get; }
```

Added methods:

```
public bool ConformsTo (string uti, string conformsToUti);
	public string[] CopyAllTags (string uti, string tagClass);
	public string[] CreateAllIdentifiers (string tagClass, string tag, string conformingToUti);
	public static string CreatePreferredIdentifier (string tagClass, string tag, string conformingToUti);
	public string GetDescription (string uti);
	public static bool IsDeclared (string utType);
	public static bool IsDynamic (string utType);
```

## Namespace MonoTouch.MultipeerConnectivity

### Type Changed: MonoTouch.MultipeerConnectivity.MCBrowserViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKAddPassesViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

Added property:

```
public static bool CanAddPasses { get; }
```

### Type Changed: MonoTouch.PassKit.PKPass

Added properties:

```
public virtual PKPassType PassType { get; }
	public virtual PKPaymentPass PaymentPass { get; }
```

### Type Changed: MonoTouch.PassKit.PKPassKitErrorCode

Added value:

```
NotEntitled = 4,
```

### Type Changed: MonoTouch.PassKit.PKPassLibrary

Added property:

```
public static bool IsPaymentPassActivationAvailable { get; }
```

Added methods:

```
public virtual void ActivatePaymentPass (PKPaymentPass paymentPass, MonoTouch.Foundation.NSData activationData, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual void ActivatePaymentPass (PKPaymentPass paymentPass, string activationCode, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual PKPass[] GetPasses (PKPassType passType);
```

### New Type MonoTouch.PassKit.IPKPaymentAuthorizationViewControllerDelegate

```
public interface IPKPaymentAuthorizationViewControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, PKPaymentAuthorizationHandler completion);
	public virtual void PaymentAuthorizationViewControllerDidFinish (PKPaymentAuthorizationViewController controller);
}
```

### New Type MonoTouch.PassKit.PKAddressField

```
[Serializable]
[Flags]
public enum PKAddressField {
	All = 7,
	Email = 4,
	None = 0,
	Phone = 2,
	PostalAddress = 1,
}
```

### New Type MonoTouch.PassKit.PKMerchantCapability

```
[Serializable]
public enum PKMerchantCapability {
	EMV = 2,
	ThreeDS = 1,
}
```

### New Type MonoTouch.PassKit.PKObject

```
public class PKObject : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKObject ();
	public PKObject (MonoTouch.Foundation.NSCoder coder);
	public PKObject (MonoTouch.Foundation.NSObjectFlag t);
	public PKObject (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.PassKit.PKPassType

```
[Serializable]
public enum PKPassType {
	Barcode = 0,
	Payment = 1,
}
```

### New Type MonoTouch.PassKit.PKPayment

```
public class PKPayment : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPayment ();
	public PKPayment (MonoTouch.Foundation.NSCoder coder);
	public PKPayment (MonoTouch.Foundation.NSObjectFlag t);
	public PKPayment (System.IntPtr handle);
	// properties
	public virtual MonoTouch.AddressBook.ABRecord BillingAddress { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.AddressBook.ABRecord ShippingAddress { get; }
	public virtual PKShippingMethod ShippingMethod { get; }
	public virtual PKPaymentToken Token { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationEventArgs

```
public class PKPaymentAuthorizationEventArgs : System.EventArgs {
	// constructors
	public PKPaymentAuthorizationEventArgs (PKPayment payment, PKPaymentAuthorizationHandler completion);
	// properties
	public PKPaymentAuthorizationHandler Completion { get; set; }
	public PKPayment Payment { get; set; }
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationHandler

```
public sealed delegate PKPaymentAuthorizationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PKPaymentAuthorizationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PKPaymentAuthorizationStatus status, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PKPaymentAuthorizationStatus status);
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationStatus

```
[Serializable]
public enum PKPaymentAuthorizationStatus {
	Failure = 1,
	InvalidBillingPostalAddress = 2,
	InvalidShippingContact = 4,
	InvalidShippingPostalAddress = 3,
	Success = 0,
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationViewController

```
public class PKPaymentAuthorizationViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentAuthorizationViewController ();
	public PKPaymentAuthorizationViewController (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentAuthorizationViewController (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentAuthorizationViewController (System.IntPtr handle);
	public PKPaymentAuthorizationViewController (PKPaymentRequest request);
	// properties
	public static bool CanMakePayments { get; }
	public override System.IntPtr ClassHandle { get; }
	public PKPaymentAuthorizationViewControllerDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<PKPaymentAuthorizationEventArgs> DidAuthorizePayment;
	public event System.EventHandler<PKPaymentShippingAddressSelectedEventArgs> DidSelectShippingAddress;
	public event System.EventHandler<PKPaymentShippingMethodSelectedEventArgs> DidSelectShippingMethod;
	public event System.EventHandler PaymentAuthorizationViewControllerDidFinish;
	// methods
	public static bool CanMakePaymentsUsingNetworks (MonoTouch.Foundation.NSString[] paymentNetworks);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationViewControllerDelegate

```
public abstract class PKPaymentAuthorizationViewControllerDelegate : MonoTouch.Foundation.NSObject, IPKPaymentAuthorizationViewControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentAuthorizationViewControllerDelegate ();
	public PKPaymentAuthorizationViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentAuthorizationViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentAuthorizationViewControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, PKPaymentAuthorizationHandler completion);
	public virtual void DidSelectShippingAddress (PKPaymentAuthorizationViewController controller, MonoTouch.AddressBook.ABRecord address, PKPaymentShippingAddressSelected completion);
	public virtual void DidSelectShippingMethod (PKPaymentAuthorizationViewController controller, PKShippingMethod shippingMethod, PKPaymentShippingMethodSelected completion);
	public virtual void PaymentAuthorizationViewControllerDidFinish (PKPaymentAuthorizationViewController controller);
}
```

### New Type MonoTouch.PassKit.PKPaymentAuthorizationViewControllerDelegate_Extensions

```
public static class PKPaymentAuthorizationViewControllerDelegate_Extensions {
	// methods
	public static void DidSelectShippingAddress (IPKPaymentAuthorizationViewControllerDelegate This, PKPaymentAuthorizationViewController controller, MonoTouch.AddressBook.ABRecord address, PKPaymentShippingAddressSelected completion);
	public static void DidSelectShippingMethod (IPKPaymentAuthorizationViewControllerDelegate This, PKPaymentAuthorizationViewController controller, PKShippingMethod shippingMethod, PKPaymentShippingMethodSelected completion);
}
```

### New Type MonoTouch.PassKit.PKPaymentNetwork

```
public static class PKPaymentNetwork {
	// properties
	public static MonoTouch.Foundation.NSString Amex { get; }
	public static MonoTouch.Foundation.NSString MasterCard { get; }
	public static MonoTouch.Foundation.NSString Visa { get; }
}
```

### New Type MonoTouch.PassKit.PKPaymentPass

```
public class PKPaymentPass : MonoTouch.PassKit.PKPass, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentPass ();
	public PKPaymentPass (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentPass (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentPass (System.IntPtr handle);
	// properties
	public virtual PKPaymentPassActivationState ActivationState { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string DeviceAccountIdentifier { get; }
	public virtual string DeviceAccountNumberSuffix { get; }
	public virtual string PrimaryAccountIdentifier { get; }
	public virtual string PrimaryAccountNumberSuffix { get; }
}
```

### New Type MonoTouch.PassKit.PKPaymentPassActivationState

```
[Serializable]
public enum PKPaymentPassActivationState {
	Activated = 0,
	Activating = 2,
	Deactivated = 4,
	RequiresActivation = 1,
	Suspended = 3,
}
```

### New Type MonoTouch.PassKit.PKPaymentRequest

```
public class PKPaymentRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentRequest ();
	public PKPaymentRequest (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentRequest (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentRequest (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSData ApplicationData { get; set; }
	public virtual MonoTouch.AddressBook.ABRecord BillingAddress { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string CountryCode { get; set; }
	public virtual string CurrencyCode { get; set; }
	public virtual PKMerchantCapability MerchantCapabilities { get; set; }
	public virtual string MerchantIdentifier { get; set; }
	public virtual PKPaymentSummaryItem[] PaymentSummaryItems { get; set; }
	public virtual PKAddressField RequiredBillingAddressFields { get; set; }
	public virtual PKAddressField RequiredShippingAddressFields { get; set; }
	public virtual MonoTouch.AddressBook.ABRecord ShippingAddress { get; set; }
	public virtual PKShippingMethod[] ShippingMethods { get; set; }
	public virtual MonoTouch.Foundation.NSString[] SupportedNetworks { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PassKit.PKPaymentShippingAddressSelected

```
public sealed delegate PKPaymentShippingAddressSelected : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PKPaymentShippingAddressSelected (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PKPaymentAuthorizationStatus status, PKShippingMethod[] shippingMethods, PKPaymentSummaryItem[] summaryItems, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PKPaymentAuthorizationStatus status, PKShippingMethod[] shippingMethods, PKPaymentSummaryItem[] summaryItems);
}
```

### New Type MonoTouch.PassKit.PKPaymentShippingAddressSelectedEventArgs

```
public class PKPaymentShippingAddressSelectedEventArgs : System.EventArgs {
	// constructors
	public PKPaymentShippingAddressSelectedEventArgs (MonoTouch.AddressBook.ABRecord address, PKPaymentShippingAddressSelected completion);
	// properties
	public MonoTouch.AddressBook.ABRecord Address { get; set; }
	public PKPaymentShippingAddressSelected Completion { get; set; }
}
```

### New Type MonoTouch.PassKit.PKPaymentShippingMethodSelected

```
public sealed delegate PKPaymentShippingMethodSelected : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PKPaymentShippingMethodSelected (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PKPaymentAuthorizationStatus status, PKPaymentSummaryItem[] summaryItems, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PKPaymentAuthorizationStatus status, PKPaymentSummaryItem[] summaryItems);
}
```

### New Type MonoTouch.PassKit.PKPaymentShippingMethodSelectedEventArgs

```
public class PKPaymentShippingMethodSelectedEventArgs : System.EventArgs {
	// constructors
	public PKPaymentShippingMethodSelectedEventArgs (PKShippingMethod shippingMethod, PKPaymentShippingMethodSelected completion);
	// properties
	public PKPaymentShippingMethodSelected Completion { get; set; }
	public PKShippingMethod ShippingMethod { get; set; }
}
```

### New Type MonoTouch.PassKit.PKPaymentSummaryItem

```
public class PKPaymentSummaryItem : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentSummaryItem ();
	public PKPaymentSummaryItem (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentSummaryItem (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentSummaryItem (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSDecimalNumber Amount { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Label { get; set; }
	// methods
	public static PKPaymentSummaryItem Create (string label, MonoTouch.Foundation.NSDecimalNumber amount);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PassKit.PKPaymentToken

```
public class PKPaymentToken : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPaymentToken ();
	public PKPaymentToken (MonoTouch.Foundation.NSCoder coder);
	public PKPaymentToken (MonoTouch.Foundation.NSObjectFlag t);
	public PKPaymentToken (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData PaymentData { get; }
	public virtual string PaymentInstrumentName { get; }
	public virtual string PaymentNetwork { get; }
	public virtual string TransactionIdentifier { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PassKit.PKShippingMethod

```
public class PKShippingMethod : MonoTouch.PassKit.PKPaymentSummaryItem, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKShippingMethod ();
	public PKShippingMethod (MonoTouch.Foundation.NSCoder coder);
	public PKShippingMethod (MonoTouch.Foundation.NSObjectFlag t);
	public PKShippingMethod (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Detail { get; set; }
	public virtual string Identifier { get; set; }
}
```

## Namespace MonoTouch.QuickLook

### Type Changed: MonoTouch.QuickLook.QLPreviewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecAccessible

Added value:

```
WhenPasscodeSetThisDeviceOnly = 6,
```

### Type Changed: MonoTouch.Security.SecRecord

Added properties:

```
public SecAccessControl AccessControl { get; set; }
	public bool UseNoAuthenticationUI { get; set; }
	public string UseOperationPrompt { get; set; }
```

### New Type MonoTouch.Security.SecAccessControl

```
public class SecAccessControl {
	// constructors
	public SecAccessControl (SecAccessible accessible, SecAccessControlCreateFlags flags);
	// properties
	public SecAccessible Accessible { get; }
	public SecAccessControlCreateFlags Flags { get; }
}
```

### New Type MonoTouch.Security.SecAccessControlCreateFlags

```
[Serializable]
[Flags]
public enum SecAccessControlCreateFlags {
	UserPresence = 1,
}
```

## Namespace MonoTouch.Social

### Type Changed: MonoTouch.Social.SLComposeViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### New Type MonoTouch.Social.SLComposeServiceViewController

```
public class SLComposeServiceViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SLComposeServiceViewController ();
	public SLComposeServiceViewController (MonoTouch.Foundation.NSCoder coder);
	public SLComposeServiceViewController (MonoTouch.Foundation.NSObjectFlag t);
	public SLComposeServiceViewController (System.IntPtr handle);
	// properties
	public virtual MonoTouch.UIKit.UIViewController AutoCompletionViewController { get; set; }
	public virtual MonoTouch.Foundation.NSNumber CharactersRemaining { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContentText { get; }
	public virtual string Placeholder { get; set; }
	public virtual MonoTouch.UIKit.UITextView TextView { get; }
	// methods
	public virtual void Cancel ();
	public virtual void DidSelectCancel ();
	public virtual void DidSelectPost ();
	protected override void Dispose (bool disposing);
	public virtual SLComposeSheetConfigurationItem[] GetConfigurationItems ();
	public virtual bool IsContentValid ();
	public virtual MonoTouch.UIKit.UIView LoadPreviewView ();
	public virtual void PopConfigurationViewController ();
	public virtual void PresentationAnimationDidFinish ();
	public virtual void PushConfigurationViewController (MonoTouch.UIKit.UIViewController viewController);
	public virtual void ReloadConfigurationItems ();
	public virtual void ValidateContent ();
}
```

### New Type MonoTouch.Social.SLComposeSheetConfigurationItem

```
public class SLComposeSheetConfigurationItem : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SLComposeSheetConfigurationItem ();
	public SLComposeSheetConfigurationItem (MonoTouch.Foundation.NSCoder coder);
	public SLComposeSheetConfigurationItem (MonoTouch.Foundation.NSObjectFlag t);
	public SLComposeSheetConfigurationItem (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Title { get; set; }
	public virtual string Value { get; set; }
	public virtual bool ValuePending { get; set; }
	// methods
	public virtual void SetTapHandler (System.Action tapHandler);
}
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKAction

Added methods:

```
public static SKAction Falloff (float to, double duration);
	public static SKAction FollowPath (MonoTouch.CoreGraphics.CGPath path, bool offset, bool orient, float speed);
	public static SKAction FollowPath (MonoTouch.CoreGraphics.CGPath path, float speed);
	public static SKAction Hide ();
	public static SKAction ReachTo (System.Drawing.PointF position, SKNode rootNode, double secs);
	public static SKAction ReachTo (System.Drawing.PointF position, SKNode rootNode, float velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, float velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, double sec);
	public static SKAction Run (System.Action block, MonoTouch.CoreFoundation.DispatchQueue queue);
	public static SKAction Run (System.Action block);
	public virtual void SetTimingFunction (SKActionTimingFunction timingFunction);
	public static SKAction StrengthBy (float strength, double sec);
	public static SKAction StrengthTo (float strength, double sec);
	public static SKAction Unhide ();
```

Obsoleted methods:

```
[Obsolete ("Use Run(Action) instead")]
	public static SKAction RunBlock (System.Action block);

	[Obsolete ("Use Run(Action,DispatchQueue) instead")]
	public static SKAction RunBlock (System.Action block, MonoTouch.CoreFoundation.DispatchQueue queue);
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

Added property:

```
public virtual SKShader Shader { get; set; }
```

### Type Changed: MonoTouch.SpriteKit.SKEmitterNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public virtual uint FieldBitMask { get; set; }
	public virtual float ParticleZPositionSpeed { get; set; }
	public virtual SKShader Shader { get; set; }
```

### Type Changed: MonoTouch.SpriteKit.SKLabelNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added method:

```
public static SKLabelNode FromText (string text);
```

### Type Changed: MonoTouch.SpriteKit.SKNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public virtual SKConstraint[] Constraints { get; set; }
	public virtual SKReachConstraints ReachConstraints { get; set; }
```

Added methods:

```
public void Add (SKNode node);
	public void AddNodes (SKNode[] nodes);
	public static T FromFile<T> (string file);
	public virtual System.Collections.Generic.IEnumerator<SKNode> GetEnumerator ();
	public virtual SKNode GetObjectsMatching (string nameExpression);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsBody

Added properties:

```
public virtual float Charge { get; set; }
	public virtual uint FieldBitMask { get; set; }
	public virtual bool Pinned { get; set; }
```

Added methods:

```
public static SKPhysicsBody Create (SKTexture texture, float alphaThreshold, System.Drawing.SizeF size);
	public static SKPhysicsBody Create (SKTexture texture, System.Drawing.SizeF size);
	public static SKPhysicsBody CreateBodyFromPath (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateCircularBody (float radius);
	public static SKPhysicsBody CreateCircularBody (float radius, System.Drawing.PointF center);
	public static SKPhysicsBody CreateEdge (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);
	public static SKPhysicsBody CreateEdgeChain (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateEdgeLoop (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateEdgeLoop (System.Drawing.RectangleF rect);
	public static SKPhysicsBody CreateRectangularBody (System.Drawing.SizeF size);
	public static SKPhysicsBody CreateRectangularBody (System.Drawing.SizeF size, System.Drawing.PointF center);
	public static SKPhysicsBody FromBodies (SKPhysicsBody[] bodies);
```

Obsoleted methods:

```
[Obsolete ("Use the method FromBodies instead")]
	public static SKPhysicsBody BodyWithBodies (SKPhysicsBody[] bodies);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius, System.Drawing.PointF center);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius);

	[Obsolete ("Use the CreateEdgeChain method instead")]
	public static SKPhysicsBody BodyWithEdgeChainFromPath (MonoTouch.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdge method instead")]
	public static SKPhysicsBody BodyWithEdgeFromPoint (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromPath (MonoTouch.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromRect (System.Drawing.RectangleF rect);

	[Obsolete ("Use the CreateBodyFromPath method instead")]
	public static SKPhysicsBody BodyWithPolygonFromPath (MonoTouch.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size, System.Drawing.PointF center);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsContact

Added property:

```
public virtual MonoTouch.CoreGraphics.CGVector ContactNormal { get; }
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJoint

Added properties:

```
public virtual MonoTouch.CoreGraphics.CGVector ReactionForce { get; }
	public virtual float ReactionTorque { get; }
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointPin

Added property:

```
public virtual float RotationSpeed { get; set; }
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsWorld

Added method:

```
public virtual OpenTK.Vector3 SampleFields (OpenTK.Vector3 position);
```

### Type Changed: MonoTouch.SpriteKit.SKScene

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public SKSceneDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
```

Added methods:

```
public virtual void DidApplyConstraints ();
	public virtual void DidFinishUpdate ();
```

### Type Changed: MonoTouch.SpriteKit.SKShapeNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public virtual SKShader FillShader { get; set; }
	public virtual SKTexture FillTexture { get; set; }
	public virtual MonoTouch.CoreGraphics.CGLineCap LineCap { get; set; }
	public virtual MonoTouch.CoreGraphics.CGLineJoin LineJoin { get; set; }
	public virtual float LineLength { get; }
	public virtual float MiterLimit { get; set; }
	public virtual SKShader StrokeShader { get; set; }
	public virtual SKTexture StrokeTexture { get; set; }
```

Added methods:

```
public static SKShapeNode FromCircle (float radius);
	public static SKShapeNode FromEllipse (System.Drawing.SizeF size);
	public static SKShapeNode FromEllipse (System.Drawing.RectangleF rect);
	public static SKShapeNode FromPath (MonoTouch.CoreGraphics.CGPath path);
	public static SKShapeNode FromPath (MonoTouch.CoreGraphics.CGPath path, bool centered);
	public static SKShapeNode FromPoints (ref System.Drawing.PointF points, uint numPoints);
	public static SKShapeNode FromRect (System.Drawing.SizeF size);
	public static SKShapeNode FromRect (System.Drawing.RectangleF rect, float cornerRadius);
	public static SKShapeNode FromRect (System.Drawing.SizeF size, float cornerRadius);
	public static SKShapeNode FromRect (System.Drawing.RectangleF rect);
	public static SKShapeNode FromSplinePoints (ref System.Drawing.PointF points, uint numPoints);
```

### Type Changed: MonoTouch.SpriteKit.SKSpriteNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

Added properties:

```
public virtual uint LightingBitMask { get; set; }
	public virtual SKTexture NormalTexture { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual uint ShadowCastBitMask { get; set; }
	public virtual uint ShadowedBitMask { get; set; }
```

Added methods:

```
public static SKSpriteNode Create (SKTexture texture, SKTexture normalMap);
	public static SKSpriteNode Create (string imageName, bool generateNormalMap);
```

### Type Changed: MonoTouch.SpriteKit.SKTexture

Added methods:

```
public virtual SKTexture CreateTextureByGeneratingNormalMap ();
	public virtual SKTexture CreateTextureByGeneratingNormalMap (float smoothness, float contrast);
	public static SKTexture FromData (MonoTouch.Foundation.NSData pixelData, System.Drawing.SizeF size, bool flipped);
	public static SKTexture FromTextureNoise (float smoothness, System.Drawing.SizeF size, bool grayscale);
	public static SKTexture FromTextureVectorNoise (float smoothness, System.Drawing.SizeF size);
```

### Type Changed: MonoTouch.SpriteKit.SKTextureAtlas

Added method:

```
public static SKTextureAtlas FromDictionary (MonoTouch.Foundation.NSDictionary properties);
```

### Type Changed: MonoTouch.SpriteKit.SKVideoNode

Added interfaces:

```
System.Collections.IEnumerable
	System.Collections.Generic.IEnumerable<SKNode>
```

### Type Changed: MonoTouch.SpriteKit.SKView

Added interfaces:

```
MonoTouch.UIKit.IUICoordinateSpace
	MonoTouch.UIKit.IUITraitEnvironment
```

Added properties:

```
public virtual bool AllowsTransparency { get; set; }
	public virtual bool ShouldCullNonVisibleNodes { get; set; }
	public virtual bool ShowsFields { get; set; }
	public virtual bool ShowsQuadCount { get; set; }
```

Added methods:

```
public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual SKTexture TextureFromNode (SKNode node, System.Drawing.RectangleF crop);
```

### New Type MonoTouch.SpriteKit.ISKSceneDelegate

```
public interface ISKSceneDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SpriteKit.SK3DNode

```
public class SK3DNode : MonoTouch.SpriteKit.SKNode, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SK3DNode ();
	public SK3DNode (MonoTouch.Foundation.NSCoder coder);
	public SK3DNode (MonoTouch.Foundation.NSObjectFlag t);
	public SK3DNode (System.IntPtr handle);
	public SK3DNode (System.Drawing.SizeF viewportSize);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Loops { get; set; }
	public virtual bool Playing { get; set; }
	public virtual MonoTouch.SceneKit.SCNNode PointOfView { get; set; }
	public virtual double SceneTime { get; set; }
	public virtual MonoTouch.SceneKit.SCNScene ScnScene { get; set; }
	public virtual System.Drawing.SizeF ViewportSize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SK3DNode FromViewportSize (System.Drawing.SizeF viewportSize);
	public virtual MonoTouch.SceneKit.SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.Foundation.NSDictionary options);
	public MonoTouch.SceneKit.SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.SceneKit.SCNHitTestOptions options);
	public virtual OpenTK.Vector3 ProjectPoint (OpenTK.Vector3 point);
	public virtual OpenTK.Vector3 UnprojectPoint (OpenTK.Vector3 point);
}
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

### New Type MonoTouch.SpriteKit.SKConstraint

```
public class SKConstraint : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKConstraint ();
	public SKConstraint (MonoTouch.Foundation.NSCoder coder);
	public SKConstraint (MonoTouch.Foundation.NSObjectFlag t);
	public SKConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual SKNode ReferenceNode { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SKConstraint CreateDistance (SKRange range, SKNode node);
	public static SKConstraint CreateDistance (SKRange range, System.Drawing.PointF point);
	public static SKConstraint CreateDistance (SKRange range, System.Drawing.PointF point, SKNode node);
	public static SKConstraint CreateOrientToNode (SKNode node, SKRange radians);
	public static SKConstraint CreateOrientToPoint (System.Drawing.PointF point, SKNode node, SKRange radians);
	public static SKConstraint CreateOrientToPoint (System.Drawing.PointF point, SKRange radians);
	public static SKConstraint CreateRestriction (SKRange xRange, SKRange yRange);
	public static SKConstraint CreateXRestriction (SKRange range);
	public static SKConstraint CreateYRestriction (SKRange range);
	public static SKConstraint CreateZRotation (SKRange zRange);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SpriteKit.SKFieldForceEvaluator

```
public sealed delegate SKFieldForceEvaluator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKFieldForceEvaluator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (OpenTK.Vector4 position, OpenTK.Vector4 velocity, float mass, float charge, double time, System.AsyncCallback callback, object object);
	public virtual OpenTK.Vector3 EndInvoke (System.IAsyncResult result);
	public virtual OpenTK.Vector3 Invoke (OpenTK.Vector4 position, OpenTK.Vector4 velocity, float mass, float charge, double time);
}
```

### New Type MonoTouch.SpriteKit.SKFieldNode

```
public class SKFieldNode : MonoTouch.SpriteKit.SKNode, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKFieldNode ();
	public SKFieldNode (MonoTouch.Foundation.NSCoder coder);
	public SKFieldNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKFieldNode (System.IntPtr handle);
	// properties
	public virtual float AnimationSpeed { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenTK.Vector4 Direction { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual bool Exclusive { get; set; }
	public virtual float Falloff { get; set; }
	public virtual float MinimumRadius { get; set; }
	public virtual SKRegion Region { get; set; }
	public virtual float Smoothness { get; set; }
	public virtual float Strength { get; set; }
	public virtual SKTexture Texture { get; set; }
	// methods
	public static SKFieldNode CraeteVortexField ();
	public static SKFieldNode CreateCustomField (SKFieldForceEvaluator evaluator);
	public static SKFieldNode CreateDragField ();
	public static SKFieldNode CreateElectricField ();
	public static SKFieldNode CreateLinearGravityField (OpenTK.Vector4 direction);
	public static SKFieldNode CreateMagneticField ();
	public static SKFieldNode CreateNoiseField (float smoothness, float speed);
	public static SKFieldNode CreateRadialGravityField ();
	public static SKFieldNode CreateSpringField ();
	public static SKFieldNode CreateTurbulenceField (float smoothness, float speed);
	public static SKFieldNode CreateVelocityField (OpenTK.Vector4 direction);
	public static SKFieldNode CreateVelocityField (SKTexture velocityTexture);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SpriteKit.SKLightNode

```
public class SKLightNode : MonoTouch.SpriteKit.SKNode, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKLightNode ();
	public SKLightNode (MonoTouch.Foundation.NSCoder coder);
	public SKLightNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKLightNode (System.IntPtr handle);
	// properties
	public virtual MonoTouch.UIKit.UIColor AmbientColor { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual float Falloff { get; set; }
	public virtual MonoTouch.UIKit.UIColor LightColor { get; set; }
	public virtual MonoTouch.UIKit.UIColor ShadowColor { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SpriteKit.SKMutableTexture

```
public class SKMutableTexture : MonoTouch.SpriteKit.SKTexture, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKMutableTexture (MonoTouch.Foundation.NSCoder coder);
	public SKMutableTexture (MonoTouch.Foundation.NSObjectFlag t);
	public SKMutableTexture (System.IntPtr handle);
	public SKMutableTexture (System.Drawing.SizeF size);
	public SKMutableTexture (System.Drawing.SizeF size, MonoTouch.CoreVideo.CVPixelFormatType pixelFormat);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SKMutableTexture Create (System.Drawing.SizeF size);
	public virtual void ModifyPixelData (SKTextureModify modifyMethod);
}
```

### New Type MonoTouch.SpriteKit.SKRange

```
public class SKRange : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRange ();
	public SKRange (MonoTouch.Foundation.NSCoder coder);
	public SKRange (MonoTouch.Foundation.NSObjectFlag t);
	public SKRange (System.IntPtr handle);
	public SKRange (float lowerLimit, float upperLimier);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float LowerLimit { get; set; }
	public virtual float UpperLimit { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SKRange Create (float lower, float upper);
	public static SKRange CreateConstant (float value);
	public static SKRange CreateUnlimited ();
	public static SKRange CreateWithLowerLimit (float lower);
	public static SKRange CreateWithUpperLimit (float upper);
	public static SKRange CreateWithVariance (float value, float variance);
}
```

### New Type MonoTouch.SpriteKit.SKReachConstraints

```
public class SKReachConstraints : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKReachConstraints ();
	public SKReachConstraints (MonoTouch.Foundation.NSCoder coder);
	public SKReachConstraints (MonoTouch.Foundation.NSObjectFlag t);
	public SKReachConstraints (System.IntPtr handle);
	public SKReachConstraints (float lowerAngleLimit, float upperAngleLimit);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float LowerAngleLimit { get; set; }
	public virtual float UpperAngleLimit { get; set; }
}
```

### New Type MonoTouch.SpriteKit.SKRegion

```
public class SKRegion : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRegion ();
	public SKRegion (MonoTouch.Foundation.NSCoder coder);
	public SKRegion (MonoTouch.Foundation.NSObjectFlag t);
	public SKRegion (System.IntPtr handle);
	public SKRegion (float radius);
	public SKRegion (System.Drawing.SizeF size);
	public SKRegion (MonoTouch.CoreGraphics.CGPath path);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static SKRegion InfiniteRegion { get; }
	public virtual MonoTouch.CoreGraphics.CGPath Path { get; }
	// methods
	public virtual bool ContainsPoint (System.Drawing.PointF point);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual SKRegion CreateDifference (SKRegion region);
	public virtual SKRegion CreateIntersection (SKRegion region);
	public virtual SKRegion CreateUnion (SKRegion region);
	public virtual SKRegion InverseRegion ();
}
```

### New Type MonoTouch.SpriteKit.SKSceneDelegate

```
public class SKSceneDelegate : MonoTouch.Foundation.NSObject, ISKSceneDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKSceneDelegate ();
	public SKSceneDelegate (MonoTouch.Foundation.NSCoder coder);
	public SKSceneDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SKSceneDelegate (System.IntPtr handle);
	// methods
	public virtual void DidApplyConstraints (SKScene scene);
	public virtual void DidEvaluateActions (SKScene scene);
	public virtual void DidFinishUpdate (SKScene scene);
	public virtual void DidSimulatePhysics (SKScene scene);
	public virtual void Update (double currentTime, SKScene scene);
}
```

### New Type MonoTouch.SpriteKit.SKSceneDelegate_Extensions

```
public static class SKSceneDelegate_Extensions {
	// methods
	public static void DidApplyConstraints (ISKSceneDelegate This, SKScene scene);
	public static void DidEvaluateActions (ISKSceneDelegate This, SKScene scene);
	public static void DidFinishUpdate (ISKSceneDelegate This, SKScene scene);
	public static void DidSimulatePhysics (ISKSceneDelegate This, SKScene scene);
	public static void Update (ISKSceneDelegate This, double currentTime, SKScene scene);
}
```

### New Type MonoTouch.SpriteKit.SKShader

```
public class SKShader : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKShader ();
	public SKShader (MonoTouch.Foundation.NSCoder coder);
	public SKShader (MonoTouch.Foundation.NSObjectFlag t);
	public SKShader (System.IntPtr handle);
	public SKShader (string shaderSourceCode);
	public SKShader (string sharedSourceCode, SKUniform[] uniforms);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Source { get; set; }
	public virtual SKUniform[] Uniforms { get; set; }
	// methods
	public virtual void AddUniform (SKUniform uniform);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SKShader Create ();
	protected override void Dispose (bool disposing);
	public static SKShader FromFile (string name);
	public static SKShader FromShaderSourceCode (string source, SKUniform[] uniforms);
	public static SKShader FromShaderSourceCode (string source);
	public virtual SKUniform GetUniform (string uniformName);
	public virtual void RemoveUniform (string uniforName);
}
```

### New Type MonoTouch.SpriteKit.SKTextureModify

```
public sealed delegate SKTextureModify : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKTextureModify (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr pixelData, uint lengthInBytes, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr pixelData, uint lengthInBytes);
}
```

### New Type MonoTouch.SpriteKit.SKUniform

```
public class SKUniform : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKUniform ();
	public SKUniform (string name, OpenTK.Matrix3 value);
	public SKUniform (string name, OpenTK.Matrix2 value);
	public SKUniform (string name, OpenTK.Vector4 value);
	public SKUniform (string name, OpenTK.Vector3 value);
	public SKUniform (string name, OpenTK.Vector2 value);
	public SKUniform (string name, float value);
	public SKUniform (string name, SKTexture texture);
	public SKUniform (string name);
	public SKUniform (System.IntPtr handle);
	public SKUniform (MonoTouch.Foundation.NSObjectFlag t);
	public SKUniform (MonoTouch.Foundation.NSCoder coder);
	public SKUniform (string name, OpenTK.Matrix4 value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenTK.Matrix2 FloatMatrix2Value { get; set; }
	public virtual OpenTK.Matrix3 FloatMatrix3Value { get; set; }
	public virtual OpenTK.Matrix4 FloatMatrix4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual OpenTK.Vector2 FloatVector2Value { get; set; }
	public virtual OpenTK.Vector3 FloatVector3Value { get; set; }
	public virtual OpenTK.Vector4 FloatVector4Value { get; set; }
	public virtual string Name { get; }
	public virtual SKTexture TextureValue { get; set; }
	public virtual SKUniformType UniformType { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SpriteKit.SKUniformType

```
[Serializable]
public enum SKUniformType {
	Float = 1,
	FloatMatrix2 = 5,
	FloatMatrix3 = 6,
	FloatMatrix4 = 7,
	FloatVector2 = 2,
	FloatVector3 = 3,
	FloatVector4 = 4,
	None = 0,
	Texture = 8,
}
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.ISKProductsRequestDelegate

Added interface:

```
ISKRequestDelegate
```

### Type Changed: MonoTouch.StoreKit.SKPaymentTransactionState

Added value:

```
Deferred = 4,
```

### Type Changed: MonoTouch.StoreKit.SKStoreProductParameterKey

Added properties:

```
public static MonoTouch.Foundation.NSString AffiliateToken { get; }
	public static MonoTouch.Foundation.NSString CampaignToken { get; }
```

### Type Changed: MonoTouch.StoreKit.SKStoreProductViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
```

### Type Changed: MonoTouch.StoreKit.StoreProductParameters

Added properties:

```
public string AffiliateToken { get; set; }
	public string CampaignToken { get; set; }
```

## Namespace MonoTouch.Twitter

### Type Changed: MonoTouch.Twitter.TWTweetComposeViewController

Added interfaces:

```
MonoTouch.UIKit.IUIContentContainer
	MonoTouch.UIKit.IUITraitEnvironment
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

### Type Changed: MonoTouch.UIKit.NSLayoutAttribute

Added values:

```
BottomMargin = 16,
	CenterXWithinMargins = 19,
	CenterYWithinMargins = 20,
	FirstBaseline = 12,
	LastBaseline = 11,
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
	public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, object[] viewsAndMetrics);
```

### Type Changed: MonoTouch.UIKit.NSLayoutFormatOptions

Added values:

```
AlignAllFirstBaseline = 4096,
	AlignAllLastBaseline = 2048,
```

### Type Changed: MonoTouch.UIKit.NSTextStorage

Added interface:

```
MonoTouch.Foundation.INSSecureCoding
```

### Type Changed: MonoTouch.UIKit.UIAccessibility

Added properties:

```
public static bool DarkerSystemColosEnabled { get; }
	public static bool IsBoldTextEnabled { get; }
	public static bool IsGrayscaleEnabled { get; }
	public static bool IsReduceMotionEnabled { get; }
	public static bool IsReduceTransparencyEnabled { get; }
	public static bool IsSpeakScreenEnabled { get; }
	public static bool IsSpeakSelectionEnabled { get; }
	public static bool IsSwitchControlRunning { get; }
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIActivityViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added method:

```
public virtual void SetCompletionHandler (UIActivityViewControllerCompletion completionHandler);
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIAlertView.UIAlertViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIAppearance

Added methods:

```
public static System.IntPtr GetAppearance (System.IntPtr class_ptr, UITraitCollection traits, System.Type[] whenFoundIn);
	public static System.IntPtr GetAppearance (System.IntPtr class_ptr, UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIApplication

Added properties:

```
public virtual UIUserNotificationSettings CurrentUserNotificationSettings { get; }
	public virtual bool IsRegisteredForRemoteNotifications { get; }
	public static MonoTouch.Foundation.NSString LaunchOptionsUserActivityDictionaryKey { get; }
	public static MonoTouch.Foundation.NSString LaunchOptionsUserActivityTypeKey { get; }
	public static MonoTouch.Foundation.NSString OpenSettingsUrlString { get; }
```

Added methods:

```
public virtual void RegisterForRemoteNotifications ();
	public virtual void RegisterUserNotificationSettings (UIUserNotificationSettings notificationSettings);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added methods:

```
public virtual bool ContinueUserActivity (UIApplication application, MonoTouch.Foundation.NSUserActivity userActivity, UIApplicationRestorationHandler completionHandler);
	public virtual void DidFailToContinueUserActivitiy (UIApplication application, string userActivityType, MonoTouch.Foundation.NSError error);
	public virtual void DidRegisterUserNotificationSettings (UIApplication application, UIUserNotificationSettings notificationSettings);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, UILocalNotification localNotification, System.Action completionHandler);
	public virtual void HandleAction (UIApplication application, string actionIdentifier, MonoTouch.Foundation.NSDictionary remoteNotificationInfo, System.Action completionHandler);
	public virtual bool ShouldAllowExtensionPointIdentifier (UIApplication application, MonoTouch.Foundation.NSString extensionPointIdentifier);
	public virtual void UserActivityUpdated (MonoTouch.Foundation.NSUserActivity userActivity);
	public virtual bool WillContinueUserActivity (UIApplication application, string userActivityType);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Added methods:

```
public static bool ContinueUserActivity (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUserActivity userActivity, UIApplicationRestorationHandler completionHandler);
	public static void DidFailToContinueUserActivitiy (IUIApplicationDelegate This, UIApplication application, string userActivityType, MonoTouch.Foundation.NSError error);
	public static void DidRegisterUserNotificationSettings (IUIApplicationDelegate This, UIApplication application, UIUserNotificationSettings notificationSettings);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, MonoTouch.Foundation.NSDictionary remoteNotificationInfo, System.Action completionHandler);
	public static void HandleAction (IUIApplicationDelegate This, UIApplication application, string actionIdentifier, UILocalNotification localNotification, System.Action completionHandler);
	public static bool ShouldAllowExtensionPointIdentifier (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSString extensionPointIdentifier);
	public static void UserActivityUpdated (IUIApplicationDelegate This, MonoTouch.Foundation.NSUserActivity userActivity);
	public static bool WillContinueUserActivity (IUIApplicationDelegate This, UIApplication application, string userActivityType);
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added methods:

```
public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItemStyle

Obsoleted field:

```
[Obsolete ("Use UIBarButtonItemStyle.Plain when the minimum deployment target is iOS 7")]
	Bordered = 1,
```

### Type Changed: MonoTouch.UIKit.UIBarItem

Added properties:

```
public virtual UIAccessibilityNavigationStyle AccessibilityNavigationStyle { get; set; }
	public static MonoTouch.Foundation.NSString BoldTextStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString DarkerSystemColorsStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString GrayscaleStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString NotificationSwitchControlIdentifier { get; }
	public static int PauseAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString ReduceMotionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString ReduceTransparencyStatusDidChangeNotification { get; }
	public static int ResumeAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakScreenStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakSelectionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SwitchControlStatusDidChangeNotification { get; }
```

Added methods:

```
public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIBarItem.Notifications

Added methods:

```
public static MonoTouch.Foundation.NSObject ObserveBoldTextStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveGrayscaleStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceMotionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceTransparencyStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakScreenStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakSelectionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSwitchControlStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

### Type Changed: MonoTouch.UIKit.UIBarMetrics

Added values:

```
Compact = 1,
	CompactPrompt = 102,
```

Obsoleted fields:

```
[Obsolete ("Use UIBarMetrics.Compact instead")]
	LandscapePhone = 1,

	[Obsolete ("Use UIBarMetrics.CompactPrompt instead")]
	LandscapePhonePrompt = 102,
```

### Type Changed: MonoTouch.UIKit.UIButton

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public virtual UICollectionViewLayoutAttributes PreferredLayoutAttributesFittingAttributes (UICollectionViewLayoutAttributes layoutAttributes);
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added methods:

```
public virtual void WillDisplayCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (UICollectionView collectionView, UICollectionReusableView view, string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegate

Added methods:

```
public virtual void WillDisplayCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (UICollectionView collectionView, UICollectionReusableView view, string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegate_Extensions

Added methods:

```
public static void WillDisplayCell (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void WillDisplaySupplementaryView (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionReusableView view, string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout

Added methods:

```
public override void WillDisplayCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public override void WillDisplaySupplementaryView (UICollectionView collectionView, UICollectionReusableView view, string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewFlowLayout

Added property:

```
public virtual System.Drawing.SizeF EstimatedItemSize { get; set; }
```

### Type Changed: MonoTouch.UIKit.UICollectionViewLayout

Added methods:

```
public virtual UICollectionViewLayoutInvalidationContext GetInvalidationContext (UICollectionViewLayoutAttributes preferredAttributes, UICollectionViewLayoutAttributes originalAttributes);
	public virtual bool ShouldInvalidateLayout (UICollectionViewLayoutAttributes preferredAttributes, UICollectionViewLayoutAttributes originalAttributes);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewLayoutInvalidationContext

Added properties:

```
public virtual System.Drawing.PointF ContentOffsetAdjustment { get; set; }
	public virtual System.Drawing.SizeF ContentSizeAdjustment { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary InvalidatedDecorationIndexPaths { get; }
	public virtual MonoTouch.Foundation.NSIndexPath[] InvalidatedItemIndexPaths { get; }
	public virtual MonoTouch.Foundation.NSDictionary InvalidatedSupplementaryIndexPaths { get; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void InvalidateDecorationElements (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath[] indexPaths);
	public virtual void InvalidateItems (MonoTouch.Foundation.NSIndexPath[] indexPaths);
	public virtual void InvalidateSupplementaryElements (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath[] indexPaths);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewSource

Added methods:

```
public virtual void WillDisplayCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (UICollectionView collectionView, UICollectionReusableView view, string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
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

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
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
	public virtual MonoTouch.Foundation.NSUserActivity UserActivity { get; set; }
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
	public virtual void RestoreUserActivityState (MonoTouch.Foundation.NSUserActivity userActivity);
	public virtual void SavePresentedItemChanges (System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual void UpdateUserActivityState (MonoTouch.Foundation.NSUserActivity userActivity);
```

### Type Changed: MonoTouch.UIKit.UIGestureRecognizer

Added methods:

```
public virtual bool ShouldBeRequiredToFailByGestureRecognizer (UIGestureRecognizer otherGestureRecognizer);
	public virtual bool ShouldRequireFailureOfGestureRecognizer (UIGestureRecognizer otherGestureRecognizer);
```

### Type Changed: MonoTouch.UIKit.UIImage

Added properties:

```
public virtual System.Drawing.PointF AccessibilityActivationPoint { get; set; }
	public virtual bool AccessibilityElementsHidden { get; set; }
	public virtual System.Drawing.RectangleF AccessibilityFrame { get; set; }
	public virtual string AccessibilityHint { get; set; }
	public virtual string AccessibilityLabel { get; set; }
	public virtual string AccessibilityLanguage { get; set; }
	public virtual UIAccessibilityNavigationStyle AccessibilityNavigationStyle { get; set; }
	public virtual UIBezierPath AccessibilityPath { get; set; }
	public virtual UIAccessibilityTrait AccessibilityTraits { get; set; }
	public virtual string AccessibilityValue { get; set; }
	public virtual bool AccessibilityViewIsModal { get; set; }
	public static MonoTouch.Foundation.NSString AnnouncementDidFinishNotification { get; }
	public static int AnnouncementNotification { get; }
	public static MonoTouch.Foundation.NSString BoldTextStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString ClosedCaptioningStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString DarkerSystemColorsStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString GrayscaleStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString GuidedAccessStatusDidChangeNotification { get; }
	public virtual UIImageAsset ImageAsset { get; }
	public static MonoTouch.Foundation.NSString InvertColorsStatusDidChangeNotification { get; }
	public virtual bool IsAccessibilityElement { get; set; }
	public static int LayoutChangedNotification { get; }
	public static MonoTouch.Foundation.NSString MonoAudioStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString NotificationSwitchControlIdentifier { get; }
	public static int PageScrolledNotification { get; }
	public static int PauseAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString ReduceMotionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString ReduceTransparencyStatusDidChangeNotification { get; }
	public static int ResumeAssistiveTechnologyNotification { get; }
	public static int ScreenChangedNotification { get; }
	public virtual bool ShouldGroupAccessibilityChildren { get; set; }
	public static MonoTouch.Foundation.NSString SpeakScreenStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakSelectionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeechAttributeLanguage { get; }
	public static MonoTouch.Foundation.NSString SpeechAttributePitch { get; }
	public static MonoTouch.Foundation.NSString SpeechAttributePunctuation { get; }
	public static MonoTouch.Foundation.NSString SwitchControlStatusDidChangeNotification { get; }
	public static long TraitAdjustable { get; }
	public static long TraitAllowsDirectInteraction { get; }
	public static long TraitButton { get; }
	public static long TraitCausesPageTurn { get; }
	public virtual UITraitCollection TraitCollection { get; }
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

Added methods:

```
public virtual bool AccessibilityActivate ();
	public static UIImage FromBundle (string name, MonoTouch.Foundation.NSBundle bundle, UITraitCollection traitCollection);
```

### New Type MonoTouch.UIKit.Notifications

```
public static class Notifications {
	// methods
	public static MonoTouch.Foundation.NSObject ObserveAnnouncementDidFinish (System.EventHandler<UIAccessibilityAnnouncementFinishedEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveBoldTextStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveClosedCaptioningStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveGrayscaleStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveGuidedAccessStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveInvertColorsStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveMonoAudioStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceMotionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceTransparencyStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakScreenStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakSelectionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSwitchControlStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
}
```

### Type Changed: MonoTouch.UIKit.UIImagePickerController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

### Type Changed: MonoTouch.UIKit.UIImageView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIInputView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIInterfaceOrientation

Added value:

```
Unknown = 0,
```

### Type Changed: MonoTouch.UIKit.UILabel

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits);
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UILocalNotification

Added properties:

```
public virtual string Category { get; set; }
	public virtual MonoTouch.CoreLocation.CLRegion Region { get; set; }
	public virtual bool RegionTriggersOnce { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIManagedDocument

Added interface:

```
MonoTouch.Foundation.INSFilePresenter
```

### Type Changed: MonoTouch.UIKit.UIModalPresentationStyle

Added values:

```
OverCurrentContext = 6,
	OverFullScreen = 5,
	Popover = 7,
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interfaces:

```
IUIBarPositioning
	IUICoordinateSpace
	IUITraitEnvironment
```

Added properties:

```
public virtual UIBarPosition BarPosition { get; }
	public UIStringAttributes TitleTextAttributes { get; set; }
```

Added methods:

```
public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits);
```

Obsoleted methods:

```
[Obsolete ("Use TitleTextAttributes property with UIStringAttributes")]
	public UITextAttributes GetTitleTextAttributes ();

	[Obsolete ("Use TitleTextAttributes with UIStringAttributes")]
	public void SetTitleTextAttributes (UITextAttributes attributes);
```

### Type Changed: MonoTouch.UIKit.UINavigationBar.UINavigationBarAppearance

Added property:

```
public UIStringAttributes TitleTextAttributes { get; set; }
```

### Type Changed: MonoTouch.UIKit.UINavigationController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added properties:

```
public virtual UIPanGestureRecognizer BarHideOnSwipeGestureRecognizer { get; }
	public virtual UITapGestureRecognizer BarHideOnTapGestureRecognizer { get; }
	public virtual bool HidesBarsOnSwipe { get; set; }
	public virtual bool HidesBarsOnTap { get; set; }
	public virtual bool HidesBarsWhenKeyboardAppears { get; set; }
	public virtual bool HidesBarsWhenVerticallyCompact { get; set; }
```

Added method:

```
public virtual void ShowViewController (UIViewController vc, MonoTouch.Foundation.NSObject sender);
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIPageViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIPrintFormatter

Added property:

```
public virtual UIEdgeInsets PerPageContentInsets { get; set; }
```

### Type Changed: MonoTouch.UIKit.UIPrintInteractionController

Added property:

```
public virtual bool ShowsPaperSelectionForLoadedPapers { get; set; }
```

Added method:

```
public virtual bool PrintToPrinter (UIPrinter printer, UIPrintInteractionCompletionHandler completion);
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIResponder

Added properties:

```
public virtual UIAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }
	public virtual UIInputViewController InputAccessoryViewController { get; }
	public virtual UIInputViewController InputViewController { get; }
	public virtual MonoTouch.Foundation.NSUserActivity UserActivity { get; set; }
```

Added methods:

```
public virtual void AccessibilityElementDidBecomeFocused ();
	public virtual void AccessibilityElementDidLoseFocus ();
	public virtual bool AccessibilityElementIsFocused ();
	public virtual void RestoreUserActivityState (MonoTouch.Foundation.NSUserActivity activity);
	public virtual void UpdateUserActivityState (MonoTouch.Foundation.NSUserActivity activity);
```

### Type Changed: MonoTouch.UIKit.UIScreen

Added interface:

```
IUITraitEnvironment
```

Added properties:

```
public virtual IUICoordinateSpace CoordinateSpace { get; }
	public virtual IUICoordinateSpace FixedCoordinateSpace { get; }
	public virtual System.Drawing.RectangleF NativeBounds { get; }
	public virtual float NativeScale { get; }
	public virtual UITraitCollection TraitCollection { get; }
```

Added method:

```
public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interfaces:

```
IUIBarPositioning
	IUITextInputTraits
	IUICoordinateSpace
	IUITraitEnvironment
```

Added properties:

```
public virtual UIBarPosition BarPosition { get; }
	public virtual bool EnablesReturnKeyAutomatically { get; set; }
	public virtual UIKeyboardAppearance KeyboardAppearance { get; set; }
	public virtual UIReturnKeyType ReturnKeyType { get; set; }
	public virtual bool SecureTextEntry { get; set; }
```

Added methods:

```
public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISlider

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISplitViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added properties:

```
public static float AutomaticDimension { get; }
	public virtual bool Collapsed { get; }
	public UISplitViewControllerCanCollapsePredicate CollapseSecondViewController { get; set; }
	public virtual UISplitViewControllerDisplayMode DisplayMode { get; }
	public virtual UIBarButtonItem DisplayModeButtonItem { get; }
	public UISplitViewControllerDisplayEvent EventShowDetailViewController { get; set; }
	public UISplitViewControllerDisplayEvent EventShowViewController { get; set; }
	public UISplitViewControllerGetViewController GetPrimaryViewControllerForCollapsingSplitViewController { get; set; }
	public UISplitViewControllerGetViewController GetPrimaryViewControllerForExpandingSplitViewController { get; set; }
	public System.Func<UISplitViewController,MonoTouch.UIKit.UIInterfaceOrientationMask> SupportedInterfaceOrientations { get; set; }
	public UISplitViewControllerFetchTargetForActionHandler GetTargetDisplayModeForAction { get; set; }
	public virtual float MaximumPrimaryColumnWidth { get; set; }
	public virtual float MinimumPrimaryColumnWidth { get; set; }
	public virtual UISplitViewControllerDisplayMode PreferredDisplayMode { get; set; }
	public System.Func<UISplitViewController,MonoTouch.UIKit.UIInterfaceOrientation> GetPreferredInterfaceOrientationForPresentation { get; set; }
	public virtual float PreferredPrimaryColumnWidthFraction { get; set; }
	public virtual float PrimaryColumnWidth { get; }
	public UISplitViewControllerGetSecondaryViewController SeparateSecondaryViewController { get; set; }
```

Added event:

```
public event System.EventHandler<UISplitViewControllerDisplayModeEventArgs> WillChangeDisplayMode;
```

Removed methods:

```
public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UISplitViewController splitViewController);
	public virtual UIInterfaceOrientation PreferredInterfaceOrientationForPresentation (UISplitViewController splitViewController);
```

Added methods:

```
public virtual void ShowDetailViewController (UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public virtual void ShowViewController (UIViewController vc, MonoTouch.Foundation.NSObject sender);
```

### Type Changed: MonoTouch.UIKit.UISplitViewControllerDelegate

Added methods:

```
public virtual bool CollapseSecondViewController (UISplitViewController splitViewController, UIViewController secondaryViewController, UIViewController primaryViewController);
	public virtual bool EventShowDetailViewController (UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public virtual bool EventShowViewController (UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public virtual UIViewController GetPrimaryViewControllerForCollapsingSplitViewController (UISplitViewController splitViewController);
	public virtual UIViewController GetPrimaryViewControllerForExpandingSplitViewController (UISplitViewController splitViewController);
	public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UISplitViewController splitViewController);
	public virtual UISplitViewControllerDisplayMode GetTargetDisplayModeForAction (UISplitViewController svc);
	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (UISplitViewController splitViewController);
	public virtual UIViewController SeparateSecondaryViewController (UISplitViewController splitViewController, UIViewController primaryViewController);
	public virtual void WillChangeDisplayMode (UISplitViewController svc, UISplitViewControllerDisplayMode displayMode);
```

### Type Changed: MonoTouch.UIKit.UISplitViewControllerDelegate_Extensions

Added methods:

```
public static bool CollapseSecondViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController, UIViewController secondaryViewController, UIViewController primaryViewController);
	public static bool EventShowDetailViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public static bool EventShowViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public static UIViewController GetPrimaryViewControllerForCollapsingSplitViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);
	public static UIViewController GetPrimaryViewControllerForExpandingSplitViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);
	public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);
	public static UISplitViewControllerDisplayMode GetTargetDisplayModeForAction (IUISplitViewControllerDelegate This, UISplitViewController svc);
	public static UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (IUISplitViewControllerDelegate This, UISplitViewController splitViewController);
	public static UIViewController SeparateSecondaryViewController (IUISplitViewControllerDelegate This, UISplitViewController splitViewController, UIViewController primaryViewController);
	public static void WillChangeDisplayMode (IUISplitViewControllerDelegate This, UISplitViewController svc, UISplitViewControllerDisplayMode displayMode);
```

### Type Changed: MonoTouch.UIKit.UIStepper

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISwitch

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits);
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITabBar

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITabBarController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

### Type Changed: MonoTouch.UIKit.UITabBarItem

Added methods:

```
public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added property:

```
public virtual UIVisualEffect SeparatorEffect { get; set; }
```

Added methods:

```
public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITableView.UITableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableView.UITableViewAppearance

Added properties:

```
public virtual UIColor SeparatorColor { get; set; }
	public virtual UIVisualEffect SeparatorEffect { get; set; }
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added method:

```
public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UITableViewDelegate

Added method:

```
public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UITableViewDelegate_Extensions

Added method:

```
public static UITableViewRowAction[] EditActionsForRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITableViewHeaderFooterView.UITableViewHeaderFooterViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableViewSource

Added method:

```
public virtual UITableViewRowAction[] EditActionsForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
```

### Type Changed: MonoTouch.UIKit.UITextField

Added interfaces:

```
IUIKeyInput
	IUITextInput
	IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITextField.UITextFieldAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITextRange

Added properties:

```
public UITextPosition End { get; }
	public UITextPosition Start { get; }
```

Obsoleted properties:

```
[Obsolete ("Use End instead")]
	public virtual UITextPosition end { get; }

	[Obsolete ("Use Start instead")]
	public virtual UITextPosition start { get; }
```

### Type Changed: MonoTouch.UIKit.UITextView

Added interfaces:

```
IUIKeyInput
	IUITextInput
	IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interfaces:

```
IUIBarPositioning
	IUICoordinateSpace
	IUITraitEnvironment
```

Added property:

```
public virtual UIBarPosition BarPosition { get; }
```

Added methods:

```
public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITouch

Added properties:

```
public virtual float MajorRadius { get; }
	public virtual float MajorRadiusTolerance { get; }
```

### Type Changed: MonoTouch.UIKit.UITransitionContext

Added properties:

```
public static MonoTouch.Foundation.NSString FromViewKey { get; }
	public static MonoTouch.Foundation.NSString ToViewKey { get; }
```

### Type Changed: MonoTouch.UIKit.UIUserInterfaceIdiom

Added value:

```
Unspecified = -1,
```

### Type Changed: MonoTouch.UIKit.UIVideoEditorController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

### Type Changed: MonoTouch.UIKit.UIView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added properties:

```
public virtual UIAccessibilityNavigationStyle AccessibilityNavigationStyle { get; set; }
	public static MonoTouch.Foundation.NSString BoldTextStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString DarkerSystemColorsStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString GrayscaleStatusDidChangeNotification { get; }
	public virtual UIEdgeInsets LayoutMargins { get; set; }
	public virtual UIView MaskView { get; set; }
	public static MonoTouch.Foundation.NSString NotificationSwitchControlIdentifier { get; }
	public static int PauseAssistiveTechnologyNotification { get; }
	public virtual bool PreservesSuperviewLayoutMargins { get; set; }
	public static MonoTouch.Foundation.NSString ReduceMotionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString ReduceTransparencyStatusDidChangeNotification { get; }
	public static int ResumeAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakScreenStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakSelectionStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SwitchControlStatusDidChangeNotification { get; }
	public virtual UITraitCollection TraitCollection { get; }
```

Added methods:

```
public virtual System.Drawing.PointF ConvertPointFromCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.PointF ConvertPointToCoordinateSpace (System.Drawing.PointF point, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectFromCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
	public virtual System.Drawing.RectangleF ConvertRectToCoordinateSpace (System.Drawing.RectangleF rect, IUICoordinateSpace coordinateSpace);
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public virtual void LayoutMarginsDidChange ();
	public virtual System.Drawing.SizeF SystemLayoutSizeFittingSize (System.Drawing.SizeF targetSize, float horizontalFittingPriority, float verticalFittingPriority);
	public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
```

### Type Changed: MonoTouch.UIKit.UIView.Notifications

Added methods:

```
public static MonoTouch.Foundation.NSObject ObserveBoldTextStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveDarkerSystemColorsStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveGrayscaleStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceMotionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveReduceTransparencyStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakScreenStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakSelectionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSwitchControlStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

### Type Changed: MonoTouch.UIKit.UIViewController

Added interfaces:

```
IUIContentContainer
	IUITraitEnvironment
```

Added properties:

```
public virtual MonoTouch.Foundation.NSExtensionContext ExtensionContext { get; }
	public virtual UIPopoverPresentationController PopoverPresentationController { get; }
	public virtual UIPresentationController PresentationController { get; }
	public static MonoTouch.Foundation.NSString ShowDetailTargetDidChangeNotification { get; }
	public virtual UITraitCollection TraitCollection { get; }
```

Added methods:

```
public virtual UITraitCollection GetOverrideTraitCollectionForChildViewController (UIViewController childViewController);
	public virtual System.Drawing.SizeF GetSizeForChildContentContainer (IUIContentContainer contentContainer, System.Drawing.SizeF parentContainerSize);
	public virtual UIViewController GetTargetViewControllerForAction (MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSObject sender);
	public virtual void PreferredContentSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void SetOverrideTraitCollection (UITraitCollection collection, UIViewController childViewController);
	public virtual void ShowDetailViewController (UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public virtual void ShowViewController (UIViewController vc, MonoTouch.Foundation.NSObject sender);
	public virtual void SystemLayoutFittingSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
	public virtual void ViewWillTransitionToSize (System.Drawing.SizeF toSize, IUIViewControllerTransitionCoordinator coordinator);
	public virtual void WillTransitionToTraitCollection (UITraitCollection traitCollection, IUIViewControllerTransitionCoordinator coordinator);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerContextTransitioning

Added property:

```
public virtual MonoTouch.CoreGraphics.CGAffineTransform TargetTransform { get; }
```

Added method:

```
public virtual UIView GetViewFor (MonoTouch.Foundation.NSString uiTransitionContextToOrFromKey);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerContextTransitioning_Extensions

Added method:

```
public static UIView GetViewFor (IUIViewControllerContextTransitioning This, MonoTouch.Foundation.NSString uiTransitionContextToOrFromKey);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext_Extensions

Added methods:

```
public static UIView GetTransitionViewController (IUIViewControllerTransitionCoordinatorContext This, UITransitionViewControllerKind kind);
	public static UIView GetTransitionViewControllerForKey (IUIViewControllerTransitionCoordinatorContext This, MonoTouch.Foundation.NSString key);
	public static MonoTouch.CoreGraphics.CGAffineTransform TargetTransform (IUIViewControllerTransitionCoordinatorContext This);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerTransitioningDelegate

Added method:

```
public virtual UIPresentationController GetPresentationControllerForPresentedViewController (UIViewController presentedViewController, UIViewController presentingViewController, UIViewController sourceViewController);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerTransitioningDelegate_Extensions

Added method:

```
public static UIPresentationController GetPresentationControllerForPresentedViewController (IUIViewControllerTransitioningDelegate This, UIViewController presentedViewController, UIViewController presentingViewController, UIViewController sourceViewController);
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIWindow

Added interfaces:

```
IUICoordinateSpace
	IUITraitEnvironment
```

Added methods:

```
public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIWindow.UIWindowAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### New Type MonoTouch.UIKit.IUIAccessibilityContainer

```
public interface IUIAccessibilityContainer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIAdaptivePresentationControllerDelegate

```
public interface IUIAdaptivePresentationControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIAppearanceContainer

```
public interface IUIAppearanceContainer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIContentContainer

```
public interface IUIContentContainer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual System.Drawing.SizeF PreferredContentSize { get; }
	// methods
	public virtual System.Drawing.SizeF GetSizeForChildContentContainer (IUIContentContainer contentContainer, System.Drawing.SizeF parentContainerSize);
	public virtual void PreferredContentSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void SystemLayoutFittingSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void ViewWillTransitionToSize (System.Drawing.SizeF toSize, IUIViewControllerTransitionCoordinator coordinator);
	public virtual void WillTransitionToTraitCollection (UITraitCollection traitCollection, IUIViewControllerTransitionCoordinator coordinator);
}
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

### New Type MonoTouch.UIKit.IUIDocumentMenuDelegate

```
public interface IUIDocumentMenuDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidPickDocumentPicker (UIDocumentMenuViewController documentMenu, UIDocumentPickerViewController documentPicker);
	public virtual void WasCancelled (UIDocumentMenuViewController documentMenu);
}
```

### New Type MonoTouch.UIKit.IUIDocumentPickerDelegate

```
public interface IUIDocumentPickerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidPickDocument (UIDocumentPickerViewController controller, MonoTouch.Foundation.NSUrl url);
}
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

### New Type MonoTouch.UIKit.IUIPickerViewAccessibilityDelegate

```
public interface IUIPickerViewAccessibilityDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIPickerViewDelegate {
}
```

### New Type MonoTouch.UIKit.IUIPopoverPresentationControllerDelegate

```
public interface IUIPopoverPresentationControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIAdaptivePresentationControllerDelegate {
}
```

### New Type MonoTouch.UIKit.IUIPrinterPickerControllerDelegate

```
public interface IUIPrinterPickerControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIScrollViewAccessibilityDelegate

```
public interface IUIScrollViewAccessibilityDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIScrollViewDelegate {
}
```

### New Type MonoTouch.UIKit.IUISearchControllerDelegate

```
public interface IUISearchControllerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUISearchResultsUpdating

```
public interface IUISearchResultsUpdating : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUITextDocumentProxy

```
public interface IUITextDocumentProxy : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIKeyInput, IUITextInputTraits {
	// properties
	public virtual string DocumentContextAfterInput { get; }
	public virtual string DocumentContextBeforeInput { get; }
	// methods
	public virtual void AdjustTextPositionByCharacterOffset (int offset);
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

### New Type MonoTouch.UIKit.IUITraitEnvironment

```
public interface IUITraitEnvironment : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.NSCoder_UIGeometryKeyedCoding

```
public static class NSCoder_UIGeometryKeyedCoding {
	// methods
	public static MonoTouch.CoreGraphics.CGAffineTransform DecodeCGAffineTransform (MonoTouch.Foundation.NSCoder This, string key);
	public static System.Drawing.PointF DecodeCGPoint (MonoTouch.Foundation.NSCoder This, string key);
	public static System.Drawing.RectangleF DecodeCGRect (MonoTouch.Foundation.NSCoder This, string key);
	public static System.Drawing.SizeF DecodeCGSize (MonoTouch.Foundation.NSCoder This, string key);
	public static MonoTouch.CoreGraphics.CGVector DecodeCGVector (MonoTouch.Foundation.NSCoder This, string key);
	public static UIEdgeInsets DecodeUIEdgeInsets (MonoTouch.Foundation.NSCoder This, string key);
	public static UIOffset DecodeUIOffsetForKey (MonoTouch.Foundation.NSCoder This, string key);
	public static void Encode (MonoTouch.Foundation.NSCoder This, UIEdgeInsets edgeInsets, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, MonoTouch.CoreGraphics.CGAffineTransform transform, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, System.Drawing.RectangleF rect, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, System.Drawing.SizeF size, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, MonoTouch.CoreGraphics.CGVector vector, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, System.Drawing.PointF point, string forKey);
	public static void Encode (MonoTouch.Foundation.NSCoder This, UIOffset uiOffset, string forKey);
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

### New Type MonoTouch.UIKit.NSFileProviderExtension

```
public class NSFileProviderExtension : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSFileProviderExtension ();
	public NSFileProviderExtension (MonoTouch.Foundation.NSCoder coder);
	public NSFileProviderExtension (MonoTouch.Foundation.NSObjectFlag t);
	public NSFileProviderExtension (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUrl DocumentStorageUrl { get; }
	public virtual string ProviderIdentifier { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual string GetPersistentIdentifier (MonoTouch.Foundation.NSUrl itemUrl);
	public static MonoTouch.Foundation.NSUrl GetPlaceholderUrl (MonoTouch.Foundation.NSUrl url);
	public virtual MonoTouch.Foundation.NSUrl GetUrlForItem (string persistentIdentifier);
	public virtual void ItemChangedAtUrl (MonoTouch.Foundation.NSUrl url);
	public virtual void ProvidePlaceholderAtUrl (MonoTouch.Foundation.NSUrl url, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task ProvidePlaceholderAtUrlAsync (MonoTouch.Foundation.NSUrl url);
	public virtual void StartProvidingItemAtUrl (MonoTouch.Foundation.NSUrl url, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task StartProvidingItemAtUrlAsync (MonoTouch.Foundation.NSUrl url);
	public virtual void StopProvidingItemAtUrl (MonoTouch.Foundation.NSUrl url);
	public static bool WritePlaceholder (MonoTouch.Foundation.NSUrl placeholderUrl, MonoTouch.Foundation.NSDictionary metadata, ref MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.UIKit.NSIdentifier

```
public static class NSIdentifier {
	// methods
	public static string Identifier (NSLayoutConstraint This);
}
```

### New Type MonoTouch.UIKit.UIAccessibilityContainer_Extensions

```
public static class UIAccessibilityContainer_Extensions {
	// methods
	public static int AccessibilityElementCount (IUIAccessibilityContainer This);
	public static MonoTouch.Foundation.NSObject GetAccessibilityElementAt (IUIAccessibilityContainer This, int index);
	public static MonoTouch.Foundation.NSObject GetAccessibilityElements (IUIAccessibilityContainer This);
	public static int GetIndexOfAccessibilityElement (IUIAccessibilityContainer This, MonoTouch.Foundation.NSObject element);
	public static void SetAccessibilityElements (IUIAccessibilityContainer This, MonoTouch.Foundation.NSObject elements);
}
```

### New Type MonoTouch.UIKit.UIAccessibilityCustomAction

```
public class UIAccessibilityCustomAction : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAccessibilityCustomAction (string name, System.Func<UIAccessibilityCustomAction,System.Boolean> probe);
	public UIAccessibilityCustomAction ();
	public UIAccessibilityCustomAction (MonoTouch.Foundation.NSCoder coder);
	public UIAccessibilityCustomAction (MonoTouch.Foundation.NSObjectFlag t);
	public UIAccessibilityCustomAction (System.IntPtr handle);
	public UIAccessibilityCustomAction (string name, MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector selector);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	public virtual MonoTouch.ObjCRuntime.Selector Selector { get; set; }
	public virtual MonoTouch.Foundation.NSObject Target { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIAccessibilityElement

```
public class UIAccessibilityElement : MonoTouch.Foundation.NSObject, IUIAccessibilityIdentification, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAccessibilityElement ();
	public UIAccessibilityElement (MonoTouch.Foundation.NSCoder coder);
	public UIAccessibilityElement (MonoTouch.Foundation.NSObjectFlag t);
	public UIAccessibilityElement (System.IntPtr handle);
	public UIAccessibilityElement (MonoTouch.Foundation.NSObject container);
	// properties
	public virtual MonoTouch.Foundation.NSObject AccessibilityContainer { get; set; }
	public virtual System.Drawing.RectangleF AccessibilityFrame { get; set; }
	public virtual string AccessibilityHint { get; set; }
	public virtual string AccessibilityIdentifier { get; set; }
	public virtual string AccessibilityLabel { get; set; }
	public virtual ulong AccessibilityTraits { get; set; }
	public virtual string AccessibilityValue { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsAccessibilityElement { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIAccessibilityNavigationStyle

```
[Serializable]
public enum UIAccessibilityNavigationStyle {
	Automatic = 0,
	Combined = 2,
	Separate = 1,
}
```

### New Type MonoTouch.UIKit.UIActivityViewControllerCompletion

```
public sealed delegate UIActivityViewControllerCompletion : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIActivityViewControllerCompletion (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSExtensionItem[] returnedItems, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSString activityType, bool completed, MonoTouch.Foundation.NSExtensionItem[] returnedItems, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate

```
public class UIAdaptivePresentationControllerDelegate : MonoTouch.Foundation.NSObject, IUIAdaptivePresentationControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAdaptivePresentationControllerDelegate ();
	public UIAdaptivePresentationControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIAdaptivePresentationControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIAdaptivePresentationControllerDelegate (System.IntPtr handle);
	// methods
	public virtual UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController forPresentationController);
	public virtual UIViewController GetViewControllerForAdaptivePresentation (UIPresentationController controller, UIModalPresentationStyle style);
}
```

### New Type MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate_Extensions

```
public static class UIAdaptivePresentationControllerDelegate_Extensions {
	// methods
	public static UIModalPresentationStyle GetAdaptivePresentationStyle (IUIAdaptivePresentationControllerDelegate This, UIPresentationController forPresentationController);
	public static UIViewController GetViewControllerForAdaptivePresentation (IUIAdaptivePresentationControllerDelegate This, UIPresentationController controller, UIModalPresentationStyle style);
}
```

### New Type MonoTouch.UIKit.UIAlertAction

```
public class UIAlertAction : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAlertAction ();
	public UIAlertAction (MonoTouch.Foundation.NSCoder coder);
	public UIAlertAction (MonoTouch.Foundation.NSObjectFlag t);
	public UIAlertAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual UIAlertActionStyle Style { get; }
	public virtual string Title { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static UIAlertAction Create (string title, UIAlertActionStyle style, System.Action<UIAlertAction> handler);
}
```

### New Type MonoTouch.UIKit.UIAlertActionStyle

```
[Serializable]
public enum UIAlertActionStyle {
	Cancel = 1,
	Default = 0,
	Destructive = 2,
}
```

### New Type MonoTouch.UIKit.UIAlertController

```
public class UIAlertController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAlertController ();
	public UIAlertController (MonoTouch.Foundation.NSCoder coder);
	public UIAlertController (MonoTouch.Foundation.NSObjectFlag t);
	public UIAlertController (System.IntPtr handle);
	// properties
	public virtual UIAlertAction[] Actions { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Message { get; set; }
	public virtual UIAlertControllerStyle PreferredStyle { get; }
	public virtual UITextField[] TextFields { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual void AddAction (UIAlertAction action);
	public virtual void AddTextField (System.Action<UITextField> configurationHandler);
	public static UIAlertController Create (string title, string message, UIAlertControllerStyle preferredStyle);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIAlertControllerStyle

```
[Serializable]
public enum UIAlertControllerStyle {
	ActionSheet = 0,
	Alert = 1,
}
```

### New Type MonoTouch.UIKit.UIAppearanceContainer

```
public class UIAppearanceContainer : MonoTouch.Foundation.NSObject, IUIAppearanceContainer, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIAppearanceContainer ();
	public UIAppearanceContainer (MonoTouch.Foundation.NSCoder coder);
	public UIAppearanceContainer (MonoTouch.Foundation.NSObjectFlag t);
	public UIAppearanceContainer (System.IntPtr handle);
}
```

### New Type MonoTouch.UIKit.UIAppearanceContainer_Extensions

```
public static class UIAppearanceContainer_Extensions {
}
```

### New Type MonoTouch.UIKit.UIApplicationRestorationHandler

```
public sealed delegate UIApplicationRestorationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIApplicationRestorationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSObject[] uidocumentOrResponderObjects, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSObject[] uidocumentOrResponderObjects);
}
```

### New Type MonoTouch.UIKit.UIBlurEffect

```
public class UIBlurEffect : MonoTouch.UIKit.UIVisualEffect, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIBlurEffect ();
	public UIBlurEffect (MonoTouch.Foundation.NSCoder coder);
	public UIBlurEffect (MonoTouch.Foundation.NSObjectFlag t);
	public UIBlurEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static UIBlurEffect FromStyle (UIBlurEffectStyle style);
}
```

### New Type MonoTouch.UIKit.UIBlurEffectStyle

```
[Serializable]
public enum UIBlurEffectStyle {
	Dark = 2,
	ExtraLight = 0,
	Light = 1,
}
```

### New Type MonoTouch.UIKit.UIContentContainer

```
public abstract class UIContentContainer : MonoTouch.Foundation.NSObject, IUIContentContainer, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIContentContainer ();
	public UIContentContainer (MonoTouch.Foundation.NSCoder coder);
	public UIContentContainer (MonoTouch.Foundation.NSObjectFlag t);
	public UIContentContainer (System.IntPtr handle);
	// properties
	public virtual System.Drawing.SizeF PreferredContentSize { get; }
	// methods
	public virtual System.Drawing.SizeF GetSizeForChildContentContainer (IUIContentContainer contentContainer, System.Drawing.SizeF parentContainerSize);
	public virtual void PreferredContentSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void SystemLayoutFittingSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void ViewWillTransitionToSize (System.Drawing.SizeF toSize, IUIViewControllerTransitionCoordinator coordinator);
	public virtual void WillTransitionToTraitCollection (UITraitCollection traitCollection, IUIViewControllerTransitionCoordinator coordinator);
}
```

### New Type MonoTouch.UIKit.UIContentContainer_Extensions

```
public static class UIContentContainer_Extensions {
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

### New Type MonoTouch.UIKit.UIDocumentMenuDelegate

```
public abstract class UIDocumentMenuDelegate : MonoTouch.Foundation.NSObject, IUIDocumentMenuDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIDocumentMenuDelegate ();
	public UIDocumentMenuDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIDocumentMenuDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIDocumentMenuDelegate (System.IntPtr handle);
	// methods
	public virtual void DidPickDocumentPicker (UIDocumentMenuViewController documentMenu, UIDocumentPickerViewController documentPicker);
	public virtual void WasCancelled (UIDocumentMenuViewController documentMenu);
}
```

### New Type MonoTouch.UIKit.UIDocumentMenuDelegate_Extensions

```
public static class UIDocumentMenuDelegate_Extensions {
}
```

### New Type MonoTouch.UIKit.UIDocumentMenuDocumentPickedEventArgs

```
public class UIDocumentMenuDocumentPickedEventArgs : System.EventArgs {
	// constructors
	public UIDocumentMenuDocumentPickedEventArgs (UIDocumentPickerViewController documentPicker);
	// properties
	public UIDocumentPickerViewController DocumentPicker { get; set; }
}
```

### New Type MonoTouch.UIKit.UIDocumentMenuOrder

```
[Serializable]
public enum UIDocumentMenuOrder {
	First = 0,
	Last = 1,
}
```

### New Type MonoTouch.UIKit.UIDocumentMenuViewController

```
public class UIDocumentMenuViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIDocumentMenuViewController ();
	public UIDocumentMenuViewController (MonoTouch.Foundation.NSCoder coder);
	public UIDocumentMenuViewController (MonoTouch.Foundation.NSObjectFlag t);
	public UIDocumentMenuViewController (System.IntPtr handle);
	public UIDocumentMenuViewController (string[] allowedUTIs, UIDocumentPickerMode mode);
	public UIDocumentMenuViewController (MonoTouch.Foundation.NSUrl url, UIDocumentPickerMode mode);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public UIDocumentMenuDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<UIDocumentMenuDocumentPickedEventArgs> DidPickDocumentPicker;
	public event System.EventHandler WasCancelled;
	// methods
	public virtual void AddOption (string title, UIImage image, UIDocumentMenuOrder order, System.Action completionHandler);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIDocumentPickedEventArgs

```
public class UIDocumentPickedEventArgs : System.EventArgs {
	// constructors
	public UIDocumentPickedEventArgs (MonoTouch.Foundation.NSUrl url);
	// properties
	public MonoTouch.Foundation.NSUrl Url { get; set; }
}
```

### New Type MonoTouch.UIKit.UIDocumentPickerDelegate

```
public abstract class UIDocumentPickerDelegate : MonoTouch.Foundation.NSObject, IUIDocumentPickerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIDocumentPickerDelegate ();
	public UIDocumentPickerDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIDocumentPickerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIDocumentPickerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidPickDocument (UIDocumentPickerViewController controller, MonoTouch.Foundation.NSUrl url);
	public virtual void WasCancelled (UIDocumentPickerViewController controller);
}
```

### New Type MonoTouch.UIKit.UIDocumentPickerDelegate_Extensions

```
public static class UIDocumentPickerDelegate_Extensions {
	// methods
	public static void WasCancelled (IUIDocumentPickerDelegate This, UIDocumentPickerViewController controller);
}
```

### New Type MonoTouch.UIKit.UIDocumentPickerExtensionViewController

```
public class UIDocumentPickerExtensionViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIDocumentPickerExtensionViewController ();
	public UIDocumentPickerExtensionViewController (MonoTouch.Foundation.NSCoder coder);
	public UIDocumentPickerExtensionViewController (MonoTouch.Foundation.NSObjectFlag t);
	public UIDocumentPickerExtensionViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual UIDocumentPickerMode DocumentPickerMode { get; }
	public virtual MonoTouch.Foundation.NSUrl DocumentStorageUrl { get; }
	public virtual MonoTouch.Foundation.NSUrl OriginalUrl { get; }
	public virtual string ProviderIdentifier { get; }
	public virtual string[] ValidTypes { get; }
	// methods
	public virtual void DismissGrantingAccess (MonoTouch.Foundation.NSUrl url);
	protected override void Dispose (bool disposing);
	public virtual void PrepareForPresentation (UIDocumentPickerMode mode);
}
```

### New Type MonoTouch.UIKit.UIDocumentPickerMode

```
[Serializable]
public enum UIDocumentPickerMode {
	ExportToService = 2,
	Import = 0,
	MoveToService = 3,
	Open = 1,
}
```

### New Type MonoTouch.UIKit.UIDocumentPickerViewController

```
public class UIDocumentPickerViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIDocumentPickerViewController ();
	public UIDocumentPickerViewController (MonoTouch.Foundation.NSCoder coder);
	public UIDocumentPickerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public UIDocumentPickerViewController (System.IntPtr handle);
	public UIDocumentPickerViewController (string[] allowedUTIs, UIDocumentPickerMode mode);
	public UIDocumentPickerViewController (MonoTouch.Foundation.NSUrl url, UIDocumentPickerMode mode);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public UIDocumentPickerDelegate Delegate { get; set; }
	public virtual UIDocumentPickerMode DocumentPickerMode { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<UIDocumentPickedEventArgs> DidPickDocument;
	public event System.EventHandler WasCancelled;
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIExtensionPointIdentifier

```
public static class UIExtensionPointIdentifier {
	// properties
	public static MonoTouch.Foundation.NSString Keyboard { get; }
}
```

### New Type MonoTouch.UIKit.UIImageAsset

```
public class UIImageAsset : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIImageAsset ();
	public UIImageAsset (MonoTouch.Foundation.NSCoder coder);
	public UIImageAsset (MonoTouch.Foundation.NSObjectFlag t);
	public UIImageAsset (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual UIImage FromTraitCollection (UITraitCollection traitCollection);
	public virtual void RegisterImage (UIImage image, UITraitCollection traitCollection);
	public virtual void UnregisterImageWithTraitCollection (UITraitCollection traitCollection);
}
```

### New Type MonoTouch.UIKit.UIInputViewController

```
public class UIInputViewController : MonoTouch.UIKit.UIViewController, IUITextInputDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment {
	// constructors
	public UIInputViewController ();
	public UIInputViewController (MonoTouch.Foundation.NSCoder coder);
	public UIInputViewController (MonoTouch.Foundation.NSObjectFlag t);
	public UIInputViewController (System.IntPtr handle);
	public UIInputViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual UIInputView InputView { get; set; }
	public virtual string PrimaryLanguage { get; set; }
	public virtual IUITextDocumentProxy TextDocumentProxy { get; }
	// methods
	public virtual void AdvanceToNextInputMode ();
	public virtual void DismissKeyboard ();
	protected override void Dispose (bool disposing);
	public virtual void RequestSupplementaryLexicon (System.Action<UILexicon> completionHandler);
	public virtual System.Threading.Tasks.Task<UILexicon> RequestSupplementaryLexiconAsync ();
	public virtual void SelectionDidChange (MonoTouch.Foundation.NSObject uiTextInput);
	public virtual void SelectionWillChange (MonoTouch.Foundation.NSObject uiTextInput);
	public virtual void TextDidChange (MonoTouch.Foundation.NSObject textInput);
	public virtual void TextWillChange (MonoTouch.Foundation.NSObject textInput);
}
```

### New Type MonoTouch.UIKit.UIKeyInput_Extensions

```
public static class UIKeyInput_Extensions {
}
```

### New Type MonoTouch.UIKit.UILexicon

```
public class UILexicon : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UILexicon ();
	public UILexicon (MonoTouch.Foundation.NSCoder coder);
	public UILexicon (MonoTouch.Foundation.NSObjectFlag t);
	public UILexicon (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual UILexiconEntry[] Entries { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UILexiconEntry

```
public class UILexiconEntry : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UILexiconEntry ();
	public UILexiconEntry (MonoTouch.Foundation.NSCoder coder);
	public UILexiconEntry (MonoTouch.Foundation.NSObjectFlag t);
	public UILexiconEntry (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DocumentText { get; }
	public virtual string UserInput { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.UIKit.UIMutableUserNotificationAction

```
public class UIMutableUserNotificationAction : MonoTouch.UIKit.UIUserNotificationAction, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIMutableUserNotificationAction ();
	public UIMutableUserNotificationAction (MonoTouch.Foundation.NSCoder coder);
	public UIMutableUserNotificationAction (MonoTouch.Foundation.NSObjectFlag t);
	public UIMutableUserNotificationAction (System.IntPtr handle);
	// properties
	public virtual UIUserNotificationActivationMode ActivationMode { get; set; }
	public virtual bool AuthenticationRequired { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Destructive { get; set; }
	public virtual string Identifier { get; set; }
	public virtual string Title { get; set; }
}
```

### New Type MonoTouch.UIKit.UIMutableUserNotificationCategory

```
public class UIMutableUserNotificationCategory : MonoTouch.UIKit.UIUserNotificationCategory, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIMutableUserNotificationCategory ();
	public UIMutableUserNotificationCategory (MonoTouch.Foundation.NSCoder coder);
	public UIMutableUserNotificationCategory (MonoTouch.Foundation.NSObjectFlag t);
	public UIMutableUserNotificationCategory (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Identifier { get; set; }
	// methods
	public virtual void SetActions (UIUserNotificationAction[] actions, UIUserNotificationActionContext context);
}
```

### New Type MonoTouch.UIKit.UIPickerViewAccessibilityDelegate

```
public class UIPickerViewAccessibilityDelegate : MonoTouch.UIKit.UIPickerViewDelegate, IUIPickerViewAccessibilityDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIPickerViewDelegate {
	// constructors
	public UIPickerViewAccessibilityDelegate ();
	public UIPickerViewAccessibilityDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIPickerViewAccessibilityDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIPickerViewAccessibilityDelegate (System.IntPtr handle);
	// methods
	public virtual string GetAccessibilityHint (UIPickerView pickerView, int component);
	public virtual string GetAccessibilityLabel (UIPickerView pickerView, int acessibilityLabelForComponent);
	public override MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIPickerView pickerView, int row, int component);
	public override float GetComponentWidth (UIPickerView pickerView, int component);
	public override float GetRowHeight (UIPickerView pickerView, int component);
	public override string GetTitle (UIPickerView pickerView, int row, int component);
	public override UIView GetView (UIPickerView pickerView, int row, int component, UIView view);
	public override void Selected (UIPickerView pickerView, int row, int component);
}
```

### New Type MonoTouch.UIKit.UIPickerViewAccessibilityDelegate_Extensions

```
public static class UIPickerViewAccessibilityDelegate_Extensions {
	// methods
	public static string GetAccessibilityHint (IUIPickerViewAccessibilityDelegate This, UIPickerView pickerView, int component);
	public static string GetAccessibilityLabel (IUIPickerViewAccessibilityDelegate This, UIPickerView pickerView, int acessibilityLabelForComponent);
}
```

### New Type MonoTouch.UIKit.UIPopoverPresentationController

```
public class UIPopoverPresentationController : MonoTouch.UIKit.UIPresentationController, IUIAppearanceContainer, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIPopoverPresentationController (MonoTouch.Foundation.NSCoder coder);
	public UIPopoverPresentationController (MonoTouch.Foundation.NSObjectFlag t);
	public UIPopoverPresentationController (System.IntPtr handle);
	// properties
	public virtual UIPopoverArrowDirection ArrowDirection { get; }
	public virtual UIColor BackgroundColor { get; set; }
	public virtual UIBarButtonItem BarButtonItem { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public UIPopoverPresentationControllerDelegate Delegat { get; set; }
	public virtual UIView[] PassthroughViews { get; set; }
	public virtual UIPopoverArrowDirection PermittedArrowDirections { get; set; }
	public virtual UIEdgeInsets PopoverLayoutMargins { get; set; }
	public virtual System.Drawing.RectangleF SourceRect { get; set; }
	public virtual UIView SourceView { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UIPopoverPresentationControllerDelegate

```
public class UIPopoverPresentationControllerDelegate : MonoTouch.UIKit.UIAdaptivePresentationControllerDelegate, IUIPopoverPresentationControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIAdaptivePresentationControllerDelegate {
	// constructors
	public UIPopoverPresentationControllerDelegate ();
	public UIPopoverPresentationControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIPopoverPresentationControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIPopoverPresentationControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidDismissPopover (UIPopoverPresentationController popoverPresentationController);
	public override UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController forPresentationController);
	public override UIViewController GetViewControllerForAdaptivePresentation (UIPresentationController controller, UIModalPresentationStyle style);
	public virtual void PrepareForPopoverPresentation (UIPopoverPresentationController popoverPresentationController);
	public virtual bool ShouldDismissPopover (UIPopoverPresentationController popoverPresentationController);
	public virtual void WillRepositionPopover (UIPopoverPresentationController popoverPresentationController, System.Drawing.RectangleF targetRect, UIView inView);
}
```

### New Type MonoTouch.UIKit.UIPopoverPresentationControllerDelegate_Extensions

```
public static class UIPopoverPresentationControllerDelegate_Extensions {
	// methods
	public static void DidDismissPopover (IUIPopoverPresentationControllerDelegate This, UIPopoverPresentationController popoverPresentationController);
	public static void PrepareForPopoverPresentation (IUIPopoverPresentationControllerDelegate This, UIPopoverPresentationController popoverPresentationController);
	public static bool ShouldDismissPopover (IUIPopoverPresentationControllerDelegate This, UIPopoverPresentationController popoverPresentationController);
	public static void WillRepositionPopover (IUIPopoverPresentationControllerDelegate This, UIPopoverPresentationController popoverPresentationController, System.Drawing.RectangleF targetRect, UIView inView);
}
```

### New Type MonoTouch.UIKit.UIPresentationController

```
public class UIPresentationController : MonoTouch.Foundation.NSObject, IUIAppearanceContainer, IUIContentContainer, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIPresentationController ();
	public UIPresentationController (MonoTouch.Foundation.NSCoder coder);
	public UIPresentationController (MonoTouch.Foundation.NSObjectFlag t);
	public UIPresentationController (System.IntPtr handle);
	public UIPresentationController (UIViewController presentedViewController, UIViewController presentingViewController);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual UIView ContainerView { get; }
	public UIAdaptivePresentationControllerDelegate Delegate { get; set; }
	public virtual System.Drawing.RectangleF FrameOfPresentedViewInContainerView { get; }
	public virtual UITraitCollection OverrideTraitCollection { get; set; }
	public virtual System.Drawing.SizeF PreferredContentSize { get; }
	public virtual UIModalPresentationStyle PresentationStyle { get; }
	public virtual UIView PresentedView { get; }
	public virtual UIViewController PresentedViewController { get; }
	public virtual UIViewController PresentingViewController { get; }
	public virtual bool ShouldPresentInFullscreen { get; }
	public virtual bool ShouldRemovePresentersView { get; }
	public virtual UITraitCollection TraitCollection { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual UIModalPresentationStyle AdaptivePresentationStyle ();
	public virtual void ContainerViewDidLayoutSubviews ();
	public virtual void ContainerViewWillLayoutSubviews ();
	public virtual void DismissalTransitionDidEnd (bool completed);
	public virtual void DismissalTransitionWillBegin ();
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.SizeF GetSizeForChildContentContainer (IUIContentContainer contentContainer, System.Drawing.SizeF parentContainerSize);
	public virtual void PreferredContentSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void PresentationTransitionDidEnd (bool completed);
	public virtual void PresentationTransitionWillBegin ();
	public virtual void SystemLayoutFittingSizeDidChangeForChildContentContainer (IUIContentContainer container);
	public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
	public virtual void ViewWillTransitionToSize (System.Drawing.SizeF toSize, IUIViewControllerTransitionCoordinator coordinator);
	public virtual void WillTransitionToTraitCollection (UITraitCollection traitCollection, IUIViewControllerTransitionCoordinator coordinator);
}
```

### New Type MonoTouch.UIKit.UIPrinter

```
public class UIPrinter : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIPrinter (MonoTouch.Foundation.NSCoder coder);
	public UIPrinter (MonoTouch.Foundation.NSObjectFlag t);
	public UIPrinter (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DisplayLocation { get; }
	public virtual string DisplayName { get; }
	public virtual string MakeAndModel { get; }
	public virtual UIPrinterJobTypes SupportedJobTypes { get; }
	public virtual bool SupportsColor { get; }
	public virtual bool SupportsDuplex { get; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; }
	// methods
	public virtual void ContactPrinter (UIPrinterContactPrinterHandler completionHandler);
	protected override void Dispose (bool disposing);
	public static UIPrinter FromUrl (MonoTouch.Foundation.NSUrl url);
}
```

### New Type MonoTouch.UIKit.UIPrinterContactPrinterHandler

```
public sealed delegate UIPrinterContactPrinterHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIPrinterContactPrinterHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool available, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool available);
}
```

### New Type MonoTouch.UIKit.UIPrinterJobTypes

```
[Serializable]
public enum UIPrinterJobTypes {
	Document = 1,
	Envelope = 2,
	Label = 4,
	LargeFormat = 64,
	Photo = 8,
	Postcard = 128,
	Receipt = 16,
	Roll = 32,
	Unknown = 0,
}
```

### New Type MonoTouch.UIKit.UIPrinterPickerCompletionHandler

```
public sealed delegate UIPrinterPickerCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UIPrinterPickerCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UIPrinterPickerController printerPickerController, bool userDidSelect, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (UIPrinterPickerController printerPickerController, bool userDidSelect, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.UIKit.UIPrinterPickerController

```
public class UIPrinterPickerController : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIPrinterPickerController (MonoTouch.Foundation.NSCoder coder);
	public UIPrinterPickerController (MonoTouch.Foundation.NSObjectFlag t);
	public UIPrinterPickerController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public UIPrinterPickerControllerDelegate Delegate { get; set; }
	public virtual UIPrinter SelectedPrinter { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual void Dismiss (bool animated);
	protected override void Dispose (bool disposing);
	public static UIPrinterPickerController FromPrinter (UIPrinter printer);
	public virtual bool Present (bool animated, UIPrinterPickerCompletionHandler completion);
	public virtual bool PresentFromBarButtonItem (UIBarButtonItem item, bool animated, UIPrinterPickerCompletionHandler completion);
	public virtual bool PresentFromRect (System.Drawing.RectangleF rect, UIView view, bool animated, UIPrinterPickerCompletionHandler completion);
}
```

### New Type MonoTouch.UIKit.UIPrinterPickerControllerDelegate

```
public class UIPrinterPickerControllerDelegate : MonoTouch.Foundation.NSObject, IUIPrinterPickerControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIPrinterPickerControllerDelegate ();
	public UIPrinterPickerControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIPrinterPickerControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIPrinterPickerControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidDismiss (UIPrinterPickerController printerPickerController);
	public virtual void DidPresent (UIPrinterPickerController printerPickerController);
	public virtual void DidSelectPrinter (UIPrinterPickerController printerPickerController);
	public virtual UIViewController GetParentViewController (UIPrinterPickerController printerPickerController);
	public virtual bool ShouldShowPrinter (UIPrinterPickerController printerPickerController, UIPrinter printer);
	public virtual void WillDismiss (UIPrinterPickerController printerPickerController);
	public virtual void WillPresent (UIPrinterPickerController printerPickerController);
}
```

### New Type MonoTouch.UIKit.UIPrinterPickerControllerDelegate_Extensions

```
public static class UIPrinterPickerControllerDelegate_Extensions {
	// methods
	public static void DidDismiss (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
	public static void DidPresent (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
	public static void DidSelectPrinter (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
	public static UIViewController GetParentViewController (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
	public static bool ShouldShowPrinter (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController, UIPrinter printer);
	public static void WillDismiss (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
	public static void WillPresent (IUIPrinterPickerControllerDelegate This, UIPrinterPickerController printerPickerController);
}
```

### New Type MonoTouch.UIKit.UIScrollViewAccessibilityDelegate

```
public class UIScrollViewAccessibilityDelegate : MonoTouch.UIKit.UIScrollViewDelegate, IUIScrollViewAccessibilityDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IUIScrollViewDelegate {
	// constructors
	public UIScrollViewAccessibilityDelegate ();
	public UIScrollViewAccessibilityDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIScrollViewAccessibilityDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIScrollViewAccessibilityDelegate (System.IntPtr handle);
	// methods
	public override void DecelerationEnded (UIScrollView scrollView);
	public override void DecelerationStarted (UIScrollView scrollView);
	public override void DidZoom (UIScrollView scrollView);
	public override void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
	public override void DraggingStarted (UIScrollView scrollView);
	public virtual string GetAccessibilityScrollStatus (UIScrollView scrollView);
	public override void ScrollAnimationEnded (UIScrollView scrollView);
	public override void Scrolled (UIScrollView scrollView);
	public override void ScrolledToTop (UIScrollView scrollView);
	public override bool ShouldScrollToTop (UIScrollView scrollView);
	public override UIView ViewForZoomingInScrollView (UIScrollView scrollView);
	public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public override void ZoomingStarted (UIScrollView scrollView, UIView view);
}
```

### New Type MonoTouch.UIKit.UIScrollViewAccessibilityDelegate_Extensions

```
public static class UIScrollViewAccessibilityDelegate_Extensions {
	// methods
	public static string GetAccessibilityScrollStatus (IUIScrollViewAccessibilityDelegate This, UIScrollView scrollView);
}
```

### New Type MonoTouch.UIKit.UISearchController

```
public class UISearchController : MonoTouch.UIKit.UIViewController, IUIViewControllerAnimatedTransitioning, IUIViewControllerTransitioningDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, IUIContentContainer, IUITraitEnvironment {
	// constructors
	public UISearchController ();
	public UISearchController (MonoTouch.Foundation.NSCoder coder);
	public UISearchController (MonoTouch.Foundation.NSObjectFlag t);
	public UISearchController (System.IntPtr handle);
	public UISearchController (UIViewController searchResultsController);
	// properties
	public virtual bool Active { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public UISearchControllerDelegate Delegate { get; set; }
	public virtual bool DimsBackgroundDuringPresentation { get; set; }
	public virtual bool HidesNavigationBarDuringPresentation { get; set; }
	public virtual UISearchBar SearchBar { get; }
	public virtual UIViewController SearchResultsController { get; }
	public UISearchResultsUpdating SearchResultsUpdater { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakSearchResultsUpdater { get; set; }
	// methods
	public virtual void AnimateTransition (IUIViewControllerContextTransitioning transitionContext);
	public virtual void AnimationEnded (bool transitionCompleted);
	protected override void Dispose (bool disposing);
	public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForDismissedController (UIViewController dismissed);
	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForDismissal (IUIViewControllerAnimatedTransitioning animator);
	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForPresentation (IUIViewControllerAnimatedTransitioning animator);
	public virtual UIPresentationController GetPresentationControllerForPresentedViewController (UIViewController presentedViewController, UIViewController presentingViewController, UIViewController sourceViewController);
	public virtual IUIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
	public void SetSearchResultsUpdater (System.Action<UISearchController> updateSearchResults);
	public virtual double TransitionDuration (IUIViewControllerContextTransitioning transitionContext);
}
```

### New Type MonoTouch.UIKit.UISearchControllerDelegate

```
public class UISearchControllerDelegate : MonoTouch.Foundation.NSObject, IUISearchControllerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UISearchControllerDelegate ();
	public UISearchControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public UISearchControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UISearchControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidDismissSearchController (UISearchController searchController);
	public virtual void DidPresentSearchController (UISearchController searchController);
	public virtual void PresentSearchController (UISearchController searchController);
	public virtual void WillDismissSearchController (UISearchController searchController);
	public virtual void WillPresentSearchController (UISearchController searchController);
}
```

### New Type MonoTouch.UIKit.UISearchControllerDelegate_Extensions

```
public static class UISearchControllerDelegate_Extensions {
	// methods
	public static void DidDismissSearchController (IUISearchControllerDelegate This, UISearchController searchController);
	public static void DidPresentSearchController (IUISearchControllerDelegate This, UISearchController searchController);
	public static void PresentSearchController (IUISearchControllerDelegate This, UISearchController searchController);
	public static void WillDismissSearchController (IUISearchControllerDelegate This, UISearchController searchController);
	public static void WillPresentSearchController (IUISearchControllerDelegate This, UISearchController searchController);
}
```

### New Type MonoTouch.UIKit.UISearchResultsUpdating

```
public class UISearchResultsUpdating : MonoTouch.Foundation.NSObject, IUISearchResultsUpdating, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UISearchResultsUpdating ();
	public UISearchResultsUpdating (MonoTouch.Foundation.NSCoder coder);
	public UISearchResultsUpdating (MonoTouch.Foundation.NSObjectFlag t);
	public UISearchResultsUpdating (System.IntPtr handle);
	// methods
	public virtual void UpdateSearchResultsForSearchController (UISearchController searchController);
}
```

### New Type MonoTouch.UIKit.UISearchResultsUpdating_Extensions

```
public static class UISearchResultsUpdating_Extensions {
	// methods
	public static void UpdateSearchResultsForSearchController (IUISearchResultsUpdating This, UISearchController searchController);
}
```

### New Type MonoTouch.UIKit.UISplitViewController_UIViewController

```
public static class UISplitViewController_UIViewController {
	// methods
	public static void CollapseSecondaryViewController (UIViewController This, UIViewController secondaryViewController, UISplitViewController splitViewController);
	public static UISplitViewController GetSplitViewController (UIViewController This);
	public static UIViewController SeparateSecondaryViewControllerForSplitViewController (UIViewController This, UISplitViewController splitViewController);
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerCanCollapsePredicate

```
public sealed delegate UISplitViewControllerCanCollapsePredicate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UISplitViewControllerCanCollapsePredicate (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UISplitViewController splitViewController, UIViewController secondaryViewController, UIViewController primaryViewController, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (UISplitViewController splitViewController, UIViewController secondaryViewController, UIViewController primaryViewController);
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerDisplayEvent

```
public sealed delegate UISplitViewControllerDisplayEvent : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UISplitViewControllerDisplayEvent (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (UISplitViewController splitViewController, UIViewController vc, MonoTouch.Foundation.NSObject sender);
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerDisplayMode

```
[Serializable]
public enum UISplitViewControllerDisplayMode {
	AllVisible = 2,
	Automatic = 0,
	PrimaryHidden = 1,
	PrimaryOverlay = 3,
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerDisplayModeEventArgs

```
public class UISplitViewControllerDisplayModeEventArgs : System.EventArgs {
	// constructors
	public UISplitViewControllerDisplayModeEventArgs (UISplitViewControllerDisplayMode displayMode);
	// properties
	public UISplitViewControllerDisplayMode DisplayMode { get; set; }
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerFetchTargetForActionHandler

```
public sealed delegate UISplitViewControllerFetchTargetForActionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UISplitViewControllerFetchTargetForActionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UISplitViewController svc, System.AsyncCallback callback, object object);
	public virtual UISplitViewControllerDisplayMode EndInvoke (System.IAsyncResult result);
	public virtual UISplitViewControllerDisplayMode Invoke (UISplitViewController svc);
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerGetSecondaryViewController

```
public sealed delegate UISplitViewControllerGetSecondaryViewController : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UISplitViewControllerGetSecondaryViewController (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UISplitViewController splitViewController, UIViewController primaryViewController, System.AsyncCallback callback, object object);
	public virtual UIViewController EndInvoke (System.IAsyncResult result);
	public virtual UIViewController Invoke (UISplitViewController splitViewController, UIViewController primaryViewController);
}
```

### New Type MonoTouch.UIKit.UISplitViewControllerGetViewController

```
public sealed delegate UISplitViewControllerGetViewController : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public UISplitViewControllerGetViewController (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (UISplitViewController splitViewController, System.AsyncCallback callback, object object);
	public virtual UIViewController EndInvoke (System.IAsyncResult result);
	public virtual UIViewController Invoke (UISplitViewController splitViewController);
}
```

### New Type MonoTouch.UIKit.UITableViewRowAction

```
public class UITableViewRowAction : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UITableViewRowAction ();
	public UITableViewRowAction (MonoTouch.Foundation.NSCoder coder);
	public UITableViewRowAction (MonoTouch.Foundation.NSObjectFlag t);
	public UITableViewRowAction (System.IntPtr handle);
	// properties
	public virtual UIColor BackgroundColor { get; set; }
	public virtual UIVisualEffect BackgroundEffect { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual UITableViewRowActionStyle Style { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static UITableViewRowAction Create (UITableViewRowActionStyle style, string title, System.Action<UITableViewRowAction,MonoTouch.Foundation.NSIndexPath> handler);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.UIKit.UITableViewRowActionStyle

```
[Serializable]
public enum UITableViewRowActionStyle {
	Default = 0,
	Destructive = 0,
	Normal = 1,
}
```

### New Type MonoTouch.UIKit.UITextDocumentProxy

```
public abstract class UITextDocumentProxy : MonoTouch.Foundation.NSObject, IUITextDocumentProxy, IUIKeyInput, IUITextInputTraits, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UITextDocumentProxy ();
	public UITextDocumentProxy (MonoTouch.Foundation.NSCoder coder);
	public UITextDocumentProxy (MonoTouch.Foundation.NSObjectFlag t);
	public UITextDocumentProxy (System.IntPtr handle);
	// properties
	public virtual UITextAutocapitalizationType AutocapitalizationType { get; set; }
	public virtual UITextAutocorrectionType AutocorrectionType { get; set; }
	public virtual string DocumentContextAfterInput { get; }
	public virtual string DocumentContextBeforeInput { get; }
	public virtual bool EnablesReturnKeyAutomatically { get; set; }
	public virtual bool HasText { get; }
	public virtual UIKeyboardAppearance KeyboardAppearance { get; set; }
	public virtual UIKeyboardType KeyboardType { get; set; }
	public virtual UIReturnKeyType ReturnKeyType { get; set; }
	public virtual bool SecureTextEntry { get; set; }
	public virtual UITextSpellCheckingType SpellCheckingType { get; set; }
	// methods
	public virtual void AdjustTextPositionByCharacterOffset (int offset);
	public virtual void DeleteBackward ();
	public virtual void InsertText (string text);
}
```

### New Type MonoTouch.UIKit.UITextDocumentProxy_Extensions

```
public static class UITextDocumentProxy_Extensions {
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

### New Type MonoTouch.UIKit.UITraitCollection

```
public class UITraitCollection : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UITraitCollection ();
	public UITraitCollection (MonoTouch.Foundation.NSCoder coder);
	public UITraitCollection (MonoTouch.Foundation.NSObjectFlag t);
	public UITraitCollection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float DisplayScale { get; }
	public virtual UIUserInterfaceSizeClass HorizontalSizeClass { get; }
	public virtual UIUserInterfaceIdiom UserInterfaceIdiom { get; }
	public virtual UIUserInterfaceSizeClass VerticalSizeClass { get; }
	// methods
	public virtual bool Contains (UITraitCollection trait);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static UITraitCollection FromDisplayScale (float scale);
	public static UITraitCollection FromHorizontalSizeClass (UIUserInterfaceSizeClass horizontalSizeClass);
	public static UITraitCollection FromTraitsFromCollections (UITraitCollection[] traitCollections);
	public static UITraitCollection FromUserInterfaceIdiom (UIUserInterfaceIdiom idiom);
	public static UITraitCollection FromVerticalSizeClass (UIUserInterfaceSizeClass verticalSizeClass);
}
```

### New Type MonoTouch.UIKit.UITraitEnvironment

```
public class UITraitEnvironment : MonoTouch.Foundation.NSObject, IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UITraitEnvironment ();
	public UITraitEnvironment (MonoTouch.Foundation.NSCoder coder);
	public UITraitEnvironment (MonoTouch.Foundation.NSObjectFlag t);
	public UITraitEnvironment (System.IntPtr handle);
	// properties
	public virtual UITraitCollection TraitCollection { get; }
	// methods
	public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
}
```

### New Type MonoTouch.UIKit.UITraitEnvironment_Extensions

```
public static class UITraitEnvironment_Extensions {
	// methods
	public static void TraitCollectionDidChange (IUITraitEnvironment This, UITraitCollection previousTraitCollection);
}
```

### New Type MonoTouch.UIKit.UITransitionViewControllerKind

```
[Serializable]
public enum UITransitionViewControllerKind {
	FromView = 1,
	ToView = 0,
}
```

### New Type MonoTouch.UIKit.UIUserInterfaceSizeClass

```
[Serializable]
public enum UIUserInterfaceSizeClass {
	Compact = 1,
	Regular = 2,
	Unspecified = 0,
}
```

### New Type MonoTouch.UIKit.UIUserNotificationAction

```
public class UIUserNotificationAction : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIUserNotificationAction ();
	public UIUserNotificationAction (MonoTouch.Foundation.NSCoder coder);
	public UIUserNotificationAction (MonoTouch.Foundation.NSObjectFlag t);
	public UIUserNotificationAction (System.IntPtr handle);
	// properties
	public virtual UIUserNotificationActivationMode ActivationMode { get; }
	public virtual bool AuthenticationRequired { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Destructive { get; }
	public virtual string Identifier { get; }
	public virtual string Title { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.UIKit.UIUserNotificationActionContext

```
[Serializable]
public enum UIUserNotificationActionContext {
	Default = 0,
	Minimal = 1,
}
```

### New Type MonoTouch.UIKit.UIUserNotificationActivationMode

```
[Serializable]
public enum UIUserNotificationActivationMode {
	Background = 1,
	Foreground = 0,
}
```

### New Type MonoTouch.UIKit.UIUserNotificationCategory

```
public class UIUserNotificationCategory : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSMutableCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIUserNotificationCategory ();
	public UIUserNotificationCategory (MonoTouch.Foundation.NSCoder coder);
	public UIUserNotificationCategory (MonoTouch.Foundation.NSObjectFlag t);
	public UIUserNotificationCategory (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual UIUserNotificationAction[] GetActionsForContext (UIUserNotificationActionContext context);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.UIKit.UIUserNotificationSettings

```
public class UIUserNotificationSettings : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIUserNotificationSettings ();
	public UIUserNotificationSettings (MonoTouch.Foundation.NSCoder coder);
	public UIUserNotificationSettings (MonoTouch.Foundation.NSObjectFlag t);
	public UIUserNotificationSettings (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSSet Categories { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual UIUserNotificationType Types { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static UIUserNotificationSettings GetSettingsForTypes (UIUserNotificationType types, MonoTouch.Foundation.NSSet categories);
}
```

### New Type MonoTouch.UIKit.UIUserNotificationType

```
[Serializable]
[Flags]
public enum UIUserNotificationType {
	Alert = 4,
	Badge = 1,
	None = 0,
	Sound = 2,
}
```

### New Type MonoTouch.UIKit.UIVibrancyEffect

```
public class UIVibrancyEffect : MonoTouch.UIKit.UIVisualEffect, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIVibrancyEffect ();
	public UIVibrancyEffect (MonoTouch.Foundation.NSCoder coder);
	public UIVibrancyEffect (MonoTouch.Foundation.NSObjectFlag t);
	public UIVibrancyEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static UIVibrancyEffect FromBlurEffect (UIBlurEffect blurEffect);
}
```

### New Type MonoTouch.UIKit.UIVisualEffect

```
public class UIVisualEffect : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public UIVisualEffect ();
	public UIVisualEffect (MonoTouch.Foundation.NSCoder coder);
	public UIVisualEffect (MonoTouch.Foundation.NSObjectFlag t);
	public UIVisualEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.UIKit.UIVisualEffectView

```
public class UIVisualEffectView : MonoTouch.UIKit.UIView, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, System.Collections.IEnumerable, IUIAccessibilityIdentification, IUICoordinateSpace, IUIDynamicItem, IUITraitEnvironment {
	// constructors
	public UIVisualEffectView ();
	public UIVisualEffectView (MonoTouch.Foundation.NSCoder coder);
	public UIVisualEffectView (MonoTouch.Foundation.NSObjectFlag t);
	public UIVisualEffectView (System.IntPtr handle);
	public UIVisualEffectView (UIVisualEffect effect);
	// properties
	public static UIVisualEffectView.UIVisualEffectViewAppearance Appearance { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual UIView ContentView { get; }
	public virtual UIVisualEffect Effect { get; }
	// methods
	public static UIVisualEffectView.UIVisualEffectViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> ();
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);

	// inner types
	public class UIVisualEffectViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	}
}
```

## New Namespace MonoTouch.AVKit

### New Type MonoTouch.AVKit.AVPlayerViewController

```
public class AVPlayerViewController : MonoTouch.UIKit.UIViewController, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIContentContainer, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerViewController ();
	public AVPlayerViewController (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.UIKit.UIView ContentOverlayView { get; }
	public virtual MonoTouch.AVFoundation.AVPlayer Player { get; set; }
	public virtual bool ReadyForDisplay { get; }
	public virtual bool ShowsPlaybackControls { get; set; }
	public virtual System.Drawing.RectangleF VideoBounds { get; }
	public MonoTouch.AVFoundation.AVLayerVideoGravity VideoGravity { get; set; }
	public virtual MonoTouch.Foundation.NSString WeakVideoGravity { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

## New Namespace MonoTouch.CloudKit

### New Type MonoTouch.CloudKit.CKAccountStatus

```
[Serializable]
public enum CKAccountStatus {
	Available = 1,
	CouldNotDetermine = 0,
	NoAccount = 3,
	Restricted = 2,
}
```

### New Type MonoTouch.CloudKit.CKApplicationPermissions

```
[Serializable]
[Flags]
public enum CKApplicationPermissions {
	UserDiscoverability = 1,
}
```

### New Type MonoTouch.CloudKit.CKApplicationPermissionStatus

```
[Serializable]
public enum CKApplicationPermissionStatus {
	CouldNotComplete = 1,
	Denied = 2,
	Granted = 3,
	InitialState = 0,
}
```

### New Type MonoTouch.CloudKit.CKAsset

```
public class CKAsset : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKAsset (MonoTouch.Foundation.NSCoder coder);
	public CKAsset (MonoTouch.Foundation.NSObjectFlag t);
	public CKAsset (System.IntPtr handle);
	public CKAsset (MonoTouch.Foundation.NSUrl fileUrl);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUrl FileUrl { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKContainer

```
public class CKContainer : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKContainer (MonoTouch.Foundation.NSCoder coder);
	public CKContainer (MonoTouch.Foundation.NSObjectFlag t);
	public CKContainer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public static CKContainer DefaultContainer { get; }
	public static MonoTouch.Foundation.NSString OwnerDefaultName { get; }
	public virtual CKDatabase PrivateCloudDatabase { get; }
	public virtual CKDatabase PublicCloudDatabase { get; }
	// methods
	public virtual void AddOperation (CKOperation operation);
	public virtual void DiscoverAllContactUserInfos (System.Action<CKDiscoveredUserInfo[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo[]> DiscoverAllContactUserInfosAsync ();
	public virtual void DiscoverUserInfo (CKRecordID userRecordId, System.Action<CKDiscoveredUserInfo,MonoTouch.Foundation.NSError> completionHandler);
	public virtual void DiscoverUserInfo (string email, System.Action<CKDiscoveredUserInfo,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (string email);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (CKRecordID userRecordId);
	protected override void Dispose (bool disposing);
	public virtual void FetchUserRecordId (System.Action<CKRecordID,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> FetchUserRecordIdAsync ();
	public static CKContainer FromIdentifier (string containerIdentifier);
	public virtual void GetAccountStatus (System.Action<CKAccountStatus,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKAccountStatus> GetAccountStatusAsync ();
	public virtual void RequestApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> RequestApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
	public virtual void StatusForApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> StatusForApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
}
```

### New Type MonoTouch.CloudKit.CKDatabase

```
public class CKDatabase : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabase (MonoTouch.Foundation.NSCoder coder);
	public CKDatabase (MonoTouch.Foundation.NSObjectFlag t);
	public CKDatabase (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void AddOperation (CKDatabaseOperation operation);
	public virtual void DeleteRecord (CKRecordID recordId, System.Action<CKRecordID,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> DeleteRecordAsync (CKRecordID recordId);
	public virtual void DeleteRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZoneID,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZoneID> DeleteRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void DeleteSubscription (string subscriptionID, CKDatabaseDeleteSubscriptionHandler completionHandler);
	public virtual System.Threading.Tasks.Task<string> DeleteSubscriptionAsync (string subscriptionID);
	public virtual void FetchAllRecordZones (System.Action<CKRecordZone[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone[]> FetchAllRecordZonesAsync ();
	public virtual void FetchAllSubscriptions (System.Action<CKSubscription[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription[]> FetchAllSubscriptionsAsync ();
	public virtual void FetchRecord (CKRecordID recordId, System.Action<CKRecord,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> FetchRecordAsync (CKRecordID recordId);
	public virtual void FetchRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZone,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> FetchRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void FetchSubscription (string subscriptionId, System.Action<CKSubscription,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> FetchSubscriptionAsync (string subscriptionId);
	public virtual void PerformQuery (CKQuery query, CKRecordZoneID zoneId, System.Action<CKRecord[],MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord[]> PerformQueryAsync (CKQuery query, CKRecordZoneID zoneId);
	public virtual void SaveRecord (CKRecord record, System.Action<CKRecord,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> SaveRecordAsync (CKRecord record);
	public virtual void SaveRecordZone (CKRecordZone zone, System.Action<CKRecordZone,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> SaveRecordZoneAsync (CKRecordZone zone);
	public virtual void SaveSubscription (CKSubscription subscription, System.Action<CKSubscription,MonoTouch.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> SaveSubscriptionAsync (CKSubscription subscription);
}
```

### New Type MonoTouch.CloudKit.CKDatabaseDeleteSubscriptionHandler

```
public sealed delegate CKDatabaseDeleteSubscriptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDatabaseDeleteSubscriptionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (string subscriptionId, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (string subscriptionId, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.CloudKit.CKDatabaseOperation

```
public class CKDatabaseOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabaseOperation (MonoTouch.Foundation.NSCoder coder);
	public CKDatabaseOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKDatabaseOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKDatabase Database { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKDiscoverAllContactsOperation

```
public class CKDiscoverAllContactsOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverAllContactsOperation ();
	public CKDiscoverAllContactsOperation (MonoTouch.Foundation.NSCoder coder);
	public CKDiscoverAllContactsOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKDiscoverAllContactsOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKDiscoveredUserInfo[],MonoTouch.Foundation.NSError> DiscoverAllContactsHandler { get; set; }
}
```

### New Type MonoTouch.CloudKit.CKDiscoveredUserInfo

```
public class CKDiscoveredUserInfo : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoveredUserInfo ();
	public CKDiscoveredUserInfo (MonoTouch.Foundation.NSCoder coder);
	public CKDiscoveredUserInfo (MonoTouch.Foundation.NSObjectFlag t);
	public CKDiscoveredUserInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string FirstName { get; }
	public virtual string LastName { get; }
	public virtual CKRecordID UserRecordId { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKDiscoverUserInfosCompletionHandler

```
public sealed delegate CKDiscoverUserInfosCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDiscoverUserInfosCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDictionary emailsToUserInfos, MonoTouch.Foundation.NSDictionary userRecordIdsToUserInfos, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDictionary emailsToUserInfos, MonoTouch.Foundation.NSDictionary userRecordIdsToUserInfos, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKDiscoverUserInfosOperation

```
public class CKDiscoverUserInfosOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverUserInfosOperation ();
	public CKDiscoverUserInfosOperation (MonoTouch.Foundation.NSCoder coder);
	public CKDiscoverUserInfosOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKDiscoverUserInfosOperation (System.IntPtr handle);
	public CKDiscoverUserInfosOperation (string[] emailAddresses, CKRecordID[] userRecordIDs);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKDiscoverUserInfosCompletionHandler Completed { set; }
	public virtual string[] EmailAddresses { get; set; }
	public virtual CKRecordID[] UserRecordIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKErrorCode

```
[Serializable]
public enum CKErrorCode {
	AssetFileModified = 17,
	AssetFileNotFound = 16,
	BadContainer = 5,
	BadDatabase = 24,
	BatchRequestFailed = 22,
	ChangeTokenExpired = 21,
	ConstraintViolation = 19,
	IncompatibleVersion = 18,
	InternalError = 1,
	InvalidArguments = 12,
	LimitExceeded = 27,
	MissingEntitlement = 8,
	NetworkFailure = 4,
	NetworkUnavailable = 3,
	None = 0,
	NotAuthenticated = 9,
	OperationCancelled = 20,
	PartialFailure = 2,
	PermissionFailure = 10,
	QuotaExceeded = 25,
	RequestRateLimited = 7,
	ResultsTruncated = 13,
	ServerRecordChanged = 14,
	ServerRejectedRequest = 15,
	ServiceUnavailable = 6,
	UnknownItem = 11,
	UserDeletedZone = 28,
	ZoneBusy = 23,
	ZoneNotFound = 26,
}
```

### New Type MonoTouch.CloudKit.CKErrorFields

```
public static class CKErrorFields {
	// properties
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public static MonoTouch.Foundation.NSString ErrorRetryAfterKey { get; }
	public static MonoTouch.Foundation.NSString PartialErrorsByItemIdKey { get; }
	public static MonoTouch.Foundation.NSString RecordChangedErrorAncestorRecordKey { get; }
	public static MonoTouch.Foundation.NSString RecordChangedErrorClientRecordKey { get; }
	public static MonoTouch.Foundation.NSString RecordChangedErrorServerRecordKey { get; }
}
```

### New Type MonoTouch.CloudKit.CKFetchNotificationChangesOperation

```
public class CKFetchNotificationChangesOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchNotificationChangesOperation ();
	public CKFetchNotificationChangesOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchNotificationChangesOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchNotificationChangesOperation (System.IntPtr handle);
	public CKFetchNotificationChangesOperation (CKServerChangeToken previousServerChangeToken);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKServerChangeToken,MonoTouch.Foundation.NSError> Completed { set; }
	public virtual bool MoreComing { get; }
	public virtual System.Action<CKNotification> NotificationChanged { set; }
	public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }
	public virtual uint ResultsLimit { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKFetchRecordChangesHandler

```
public sealed delegate CKFetchRecordChangesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordChangesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKServerChangeToken serverChangeToken, MonoTouch.Foundation.NSData clientChangeTokenData, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKServerChangeToken serverChangeToken, MonoTouch.Foundation.NSData clientChangeTokenData, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKFetchRecordChangesOperation

```
public class CKFetchRecordChangesOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordChangesOperation ();
	public CKFetchRecordChangesOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchRecordChangesOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchRecordChangesOperation (System.IntPtr handle);
	public CKFetchRecordChangesOperation (CKRecordZoneID recordZoneID, CKServerChangeToken previousServerChangeToken);
	// properties
	public virtual CKFetchRecordChangesHandler AllChangesReported { set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual bool MoreComing { get; }
	public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }
	public virtual System.Action<CKRecord> RecordChanged { set; }
	public virtual System.Action<CKRecordID> RecordDeleted { set; }
	public virtual CKRecordZoneID RecordZoneId { get; set; }
	public virtual uint ResultsLimit { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKFetchRecordsCompletedHandler

```
public sealed delegate CKFetchRecordsCompletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordsCompletedHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDictionary recordsByRecordId, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDictionary recordsByRecordId, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.CloudKit.CKFetchRecordsOperation

```
public class CKFetchRecordsOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordsOperation ();
	public CKFetchRecordsOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchRecordsOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchRecordsOperation (System.IntPtr handle);
	public CKFetchRecordsOperation (CKRecordID[] recordIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKFetchRecordsCompletedHandler Completed { set; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual System.Action<CKRecord,MonoTouch.CloudKit.CKRecordID,MonoTouch.Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecordID,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKFetchRecordsOperation FetchCurrentUserRecordOperation ();
}
```

### New Type MonoTouch.CloudKit.CKFetchRecordZonesOperation

```
public class CKFetchRecordZonesOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordZonesOperation ();
	public CKFetchRecordZonesOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchRecordZonesOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchRecordZonesOperation (System.IntPtr handle);
	public CKFetchRecordZonesOperation (CKRecordZoneID[] zoneIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordZoneCompleteHandler Completed { set; }
	public virtual CKRecordZoneID[] RecordZoneIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKFetchRecordZonesOperation FetchAllRecordZonesOperation ();
}
```

### New Type MonoTouch.CloudKit.CKFetchSubscriptionsCompleteHandler

```
public sealed delegate CKFetchSubscriptionsCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchSubscriptionsCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDictionary subscriptionsBySubscriptionId, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDictionary subscriptionsBySubscriptionId, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKFetchSubscriptionsOperation

```
public class CKFetchSubscriptionsOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchSubscriptionsOperation ();
	public CKFetchSubscriptionsOperation (MonoTouch.Foundation.NSCoder coder);
	public CKFetchSubscriptionsOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKFetchSubscriptionsOperation (System.IntPtr handle);
	public CKFetchSubscriptionsOperation (string[] subscriptionIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKFetchSubscriptionsCompleteHandler Completed { set; }
	public virtual string[] SubscriptionIds { get; set; }
	// methods
	public static CKFetchSubscriptionsOperation FetchAllSubscriptionsOperation ();
}
```

### New Type MonoTouch.CloudKit.CKLocationSortDescriptor

```
public class CKLocationSortDescriptor : MonoTouch.Foundation.NSSortDescriptor, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, MonoTouch.Foundation.INSCopying {
	// constructors
	public CKLocationSortDescriptor ();
	public CKLocationSortDescriptor (MonoTouch.Foundation.NSCoder coder);
	public CKLocationSortDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public CKLocationSortDescriptor (System.IntPtr handle);
	public CKLocationSortDescriptor (string key, MonoTouch.CoreLocation.CLLocation relativeLocation);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.CoreLocation.CLLocation RelativeLocation { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKMarkNotificationsReadHandler

```
public sealed delegate CKMarkNotificationsReadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKMarkNotificationsReadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKNotificationID[] notificationIDsMarkedRead, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKNotificationID[] notificationIDsMarkedRead, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKMarkNotificationsReadOperation

```
public class CKMarkNotificationsReadOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKMarkNotificationsReadOperation (MonoTouch.Foundation.NSCoder coder);
	public CKMarkNotificationsReadOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKMarkNotificationsReadOperation (System.IntPtr handle);
	public CKMarkNotificationsReadOperation (CKNotificationID[] notificationIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKMarkNotificationsReadHandler Completed { set; }
	public virtual CKNotificationID[] NotificationIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKModifyBadgeOperation

```
public class CKModifyBadgeOperation : MonoTouch.CloudKit.CKOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyBadgeOperation ();
	public CKModifyBadgeOperation (MonoTouch.Foundation.NSCoder coder);
	public CKModifyBadgeOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKModifyBadgeOperation (System.IntPtr handle);
	public CKModifyBadgeOperation (uint badgeValue);
	// properties
	public virtual uint BadgeValue { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<MonoTouch.Foundation.NSError> Completed { set; }
}
```

### New Type MonoTouch.CloudKit.CKModifyRecordsOperation

```
public class CKModifyRecordsOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordsOperation ();
	public CKModifyRecordsOperation (MonoTouch.Foundation.NSCoder coder);
	public CKModifyRecordsOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKModifyRecordsOperation (System.IntPtr handle);
	public CKModifyRecordsOperation (CKRecord[] records, CKRecordID[] recordIds);
	// properties
	public virtual bool Atomic { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData ClientChangeTokenData { get; set; }
	public virtual CKModifyRecordsOperationHandler Completed { set; }
	public virtual System.Action<CKRecord,MonoTouch.Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecord,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIdsToDelete { get; set; }
	public virtual CKRecord[] RecordsToSave { get; set; }
	public virtual CKRecordSavePolicy SavePolicy { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKModifyRecordsOperationHandler

```
public sealed delegate CKModifyRecordsOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordsOperationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKModifyRecordZonesHandler

```
public sealed delegate CKModifyRecordZonesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordZonesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKModifyRecordZonesOperation

```
public class CKModifyRecordZonesOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordZonesOperation ();
	public CKModifyRecordZonesOperation (MonoTouch.Foundation.NSCoder coder);
	public CKModifyRecordZonesOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKModifyRecordZonesOperation (System.IntPtr handle);
	public CKModifyRecordZonesOperation (CKRecordZone[] recordZonesToSave, CKRecordZoneID[] recordZoneIdsToDelete);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKModifyRecordZonesHandler Completed { set; }
	public virtual CKRecordZoneID[] RecordZoneIdsToDelete { get; set; }
	public virtual CKRecordZone[] RecordZonesToSave { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKModifySubscriptionsHandler

```
public sealed delegate CKModifySubscriptionsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifySubscriptionsHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKModifySubscriptionsOperation

```
public class CKModifySubscriptionsOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifySubscriptionsOperation ();
	public CKModifySubscriptionsOperation (MonoTouch.Foundation.NSCoder coder);
	public CKModifySubscriptionsOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKModifySubscriptionsOperation (System.IntPtr handle);
	public CKModifySubscriptionsOperation (CKSubscription[] subscriptionsToSave, string[] subscriptionIdsToDelete);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKModifySubscriptionsHandler Completed { set; }
	public virtual string[] SubscriptionIdsToDelete { get; set; }
	public virtual CKSubscription[] SubscriptionsToSave { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKNotification

```
public class CKNotification : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotification (MonoTouch.Foundation.NSCoder coder);
	public CKNotification (MonoTouch.Foundation.NSObjectFlag t);
	public CKNotification (System.IntPtr handle);
	// properties
	public virtual string AlertActionLocalizationKey { get; }
	public virtual string AlertBody { get; }
	public virtual string AlertLaunchImage { get; }
	public virtual string[] AlertLocalizationArgs { get; }
	public virtual string AlertLocalizationKey { get; }
	public virtual MonoTouch.Foundation.NSNumber Badge { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public virtual bool IsPruned { get; }
	public virtual CKNotificationID NotificationId { get; }
	public virtual CKNotificationType NotificationType { get; }
	public virtual string SoundName { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKNotification FromRemoteNotificationDictionary (MonoTouch.Foundation.NSDictionary notificationDictionary);
}
```

### New Type MonoTouch.CloudKit.CKNotificationID

```
public class CKNotificationID : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationID ();
	public CKNotificationID (MonoTouch.Foundation.NSCoder coder);
	public CKNotificationID (MonoTouch.Foundation.NSObjectFlag t);
	public CKNotificationID (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CloudKit.CKNotificationInfo

```
public class CKNotificationInfo : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationInfo ();
	public CKNotificationInfo (MonoTouch.Foundation.NSCoder coder);
	public CKNotificationInfo (MonoTouch.Foundation.NSObjectFlag t);
	public CKNotificationInfo (System.IntPtr handle);
	// properties
	public virtual string AlertActionLocalizationKey { get; set; }
	public virtual string AlertBody { get; set; }
	public virtual string AlertLaunchImage { get; set; }
	public virtual string[] AlertLocalizationArgs { get; set; }
	public virtual string AlertLocalizationKey { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual bool ShouldBadge { get; set; }
	public virtual bool ShouldSendContentAvailable { get; set; }
	public virtual string SoundName { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CloudKit.CKNotificationType

```
[Serializable]
public enum CKNotificationType {
	Query = 1,
	ReadNotification = 3,
	RecordZone = 2,
}
```

### New Type MonoTouch.CloudKit.CKOperation

```
public class CKOperation : MonoTouch.Foundation.NSOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKOperation (MonoTouch.Foundation.NSCoder coder);
	public CKOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKOperation (System.IntPtr handle);
	// properties
	public virtual bool AllowsCellularAccess { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CKContainer Container { get; set; }
	public virtual bool UsesBackgroundSession { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKQuery

```
public class CKQuery : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQuery (MonoTouch.Foundation.NSCoder coder);
	public CKQuery (MonoTouch.Foundation.NSObjectFlag t);
	public CKQuery (System.IntPtr handle);
	public CKQuery (string recordType, MonoTouch.Foundation.NSPredicate predicate);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual MonoTouch.Foundation.NSSortDescriptor[] SortDescriptors { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKQueryCursor

```
public class CKQueryCursor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryCursor (MonoTouch.Foundation.NSCoder coder);
	public CKQueryCursor (MonoTouch.Foundation.NSObjectFlag t);
	public CKQueryCursor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CloudKit.CKQueryNotification

```
public class CKQueryNotification : MonoTouch.CloudKit.CKNotification, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryNotification (MonoTouch.Foundation.NSCoder coder);
	public CKQueryNotification (MonoTouch.Foundation.NSObjectFlag t);
	public CKQueryNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsPublicDatabase { get; }
	public virtual CKQueryNotificationReason QueryNotificationReason { get; }
	public virtual MonoTouch.Foundation.NSDictionary RecordFields { get; }
	public virtual CKRecordID RecordId { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKQueryNotificationReason

```
[Serializable]
public enum CKQueryNotificationReason {
	RecordCreated = 1,
	RecordDeleted = 3,
	RecordUpdated = 2,
}
```

### New Type MonoTouch.CloudKit.CKQueryOperation

```
public class CKQueryOperation : MonoTouch.CloudKit.CKDatabaseOperation, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryOperation ();
	public CKQueryOperation (MonoTouch.Foundation.NSCoder coder);
	public CKQueryOperation (MonoTouch.Foundation.NSObjectFlag t);
	public CKQueryOperation (System.IntPtr handle);
	public CKQueryOperation (CKQuery query);
	public CKQueryOperation (CKQueryCursor cursor);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKQueryCursor,MonoTouch.Foundation.NSError> Completed { set; }
	public virtual CKQueryCursor Cursor { get; set; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual CKQuery Query { get; set; }
	public virtual System.Action<CKRecord> RecordFetched { set; }
	public virtual uint ResultsLimit { get; set; }
	public virtual CKRecordZoneID ZoneId { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKRecord

```
public class CKRecord : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecord (MonoTouch.Foundation.NSCoder coder);
	public CKRecord (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecord (System.IntPtr handle);
	public CKRecord (string recordType);
	public CKRecord (string recordType, CKRecordID recordId);
	public CKRecord (string recordType, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate CreationDate { get; }
	public virtual CKRecordID CreatorUserRecordId { get; }
	public MonoTouch.Foundation.NSObject Item { get; set; }
	public virtual CKRecordID LastModifiedUserRecordId { get; }
	public virtual MonoTouch.Foundation.NSDate ModificationDate { get; }
	public virtual string RecordChangeTag { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual string RecordType { get; }
	public static MonoTouch.Foundation.NSString TypeUserRecord { get; }
	// methods
	public virtual string[] AllKeys ();
	public virtual string[] AllTokens ();
	public virtual string[] ChangedKeys ();
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeSystemFields (MonoTouch.Foundation.NSCoder coder);
}
```

### New Type MonoTouch.CloudKit.CKRecordID

```
public class CKRecordID : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordID ();
	public CKRecordID (MonoTouch.Foundation.NSCoder coder);
	public CKRecordID (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecordID (System.IntPtr handle);
	public CKRecordID (string recordName);
	public CKRecordID (string recordName, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string RecordName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKRecordSavePolicy

```
[Serializable]
public enum CKRecordSavePolicy {
	SaveAllKeys = 2,
	SaveChangedKeys = 1,
	SaveIfServerRecordUnchanged = 0,
}
```

### New Type MonoTouch.CloudKit.CKRecordValue

```
public class CKRecordValue : MonoTouch.Foundation.NSObject, ICKRecordValue, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordValue ();
	public CKRecordValue (MonoTouch.Foundation.NSCoder coder);
	public CKRecordValue (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecordValue (System.IntPtr handle);
}
```

### New Type MonoTouch.CloudKit.CKRecordValue_Extensions

```
public static class CKRecordValue_Extensions {
}
```

### New Type MonoTouch.CloudKit.CKRecordZone

```
public class CKRecordZone : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZone ();
	public CKRecordZone (MonoTouch.Foundation.NSCoder coder);
	public CKRecordZone (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecordZone (System.IntPtr handle);
	public CKRecordZone (string zoneName);
	public CKRecordZone (CKRecordZoneID zoneId);
	// properties
	public virtual CKRecordZoneCapabilities Capabilities { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString DefaultName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static CKRecordZone DefaultRecordZone ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKRecordZoneCapabilities

```
[Serializable]
[Flags]
public enum CKRecordZoneCapabilities {
	Atomic = 2,
	FetchChanges = 1,
}
```

### New Type MonoTouch.CloudKit.CKRecordZoneCompleteHandler

```
public sealed delegate CKRecordZoneCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKRecordZoneCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSDictionary recordZonesByZoneId, MonoTouch.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSDictionary recordZonesByZoneId, MonoTouch.Foundation.NSError operationError);
}
```

### New Type MonoTouch.CloudKit.CKRecordZoneID

```
public class CKRecordZoneID : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneID ();
	public CKRecordZoneID (MonoTouch.Foundation.NSCoder coder);
	public CKRecordZoneID (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecordZoneID (System.IntPtr handle);
	public CKRecordZoneID (string zoneName, string ownerName);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string OwnerName { get; }
	public virtual string ZoneName { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CloudKit.CKRecordZoneNotification

```
public class CKRecordZoneNotification : MonoTouch.CloudKit.CKNotification, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneNotification (MonoTouch.Foundation.NSCoder coder);
	public CKRecordZoneNotification (MonoTouch.Foundation.NSObjectFlag t);
	public CKRecordZoneNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordZoneID RecordZoneId { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKReference

```
public class CKReference : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKReference (MonoTouch.Foundation.NSCoder coder);
	public CKReference (MonoTouch.Foundation.NSObjectFlag t);
	public CKReference (System.IntPtr handle);
	public CKReference (CKRecordID recordId, CKReferenceAction action);
	public CKReference (CKRecord record, CKReferenceAction action);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual CKReferenceAction ReferenceAction { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKReferenceAction

```
[Serializable]
public enum CKReferenceAction {
	DeleteSelf = 1,
	None = 0,
}
```

### New Type MonoTouch.CloudKit.CKServerChangeToken

```
public class CKServerChangeToken : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKServerChangeToken (MonoTouch.Foundation.NSCoder coder);
	public CKServerChangeToken (MonoTouch.Foundation.NSObjectFlag t);
	public CKServerChangeToken (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.CloudKit.CKSubscription

```
public class CKSubscription : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKSubscription (MonoTouch.Foundation.NSCoder coder);
	public CKSubscription (MonoTouch.Foundation.NSObjectFlag t);
	public CKSubscription (System.IntPtr handle);
	public CKSubscription (string recordType, MonoTouch.Foundation.NSPredicate predicate, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (string recordType, MonoTouch.Foundation.NSPredicate predicate, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKNotificationInfo NotificationInfo { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual string SubscriptionId { get; }
	public virtual CKSubscriptionOptions SubscriptionOptions { get; }
	public virtual CKSubscriptionType SubscriptionType { get; }
	public virtual CKRecordZoneID ZoneID { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.CloudKit.CKSubscriptionOptions

```
[Serializable]
[Flags]
public enum CKSubscriptionOptions {
	FiresOnce = 8,
	FiresOnRecordCreation = 1,
	FiresOnRecordDeletion = 4,
	FiresOnRecordUpdate = 2,
}
```

### New Type MonoTouch.CloudKit.CKSubscriptionType

```
[Serializable]
public enum CKSubscriptionType {
	Query = 1,
	RecordZone = 2,
}
```

### New Type MonoTouch.CloudKit.ICKRecordValue

```
public interface ICKRecordValue : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
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

## New Namespace MonoTouch.HealthKit

### New Type MonoTouch.HealthKit.HKAnchoredObjectQuery

```
public class HKAnchoredObjectQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKAnchoredObjectQuery (MonoTouch.Foundation.NSCoder coder);
	public HKAnchoredObjectQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKAnchoredObjectQuery (System.IntPtr handle);
	public HKAnchoredObjectQuery (HKSampleType type, MonoTouch.Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectResultHandler completion);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKAnchoredObjectResultHandler

```
public sealed delegate HKAnchoredObjectResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKAnchoredObjectResultHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKAnchoredObjectQuery query, MonoTouch.Foundation.NSObject[] results, uint newAnchor, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKAnchoredObjectQuery query, MonoTouch.Foundation.NSObject[] results, uint newAnchor, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.HealthKit.HKAuthorizationStatus

```
[Serializable]
public enum HKAuthorizationStatus {
	NotDetermined = 0,
	SharingAuthorized = 2,
	SharingDenied = 1,
}
```

### New Type MonoTouch.HealthKit.HKBiologicalSex

```
[Serializable]
public enum HKBiologicalSex {
	Female = 1,
	Male = 2,
	NotSet = 0,
}
```

### New Type MonoTouch.HealthKit.HKBiologicalSexObject

```
public class HKBiologicalSexObject : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKBiologicalSexObject ();
	public HKBiologicalSexObject (MonoTouch.Foundation.NSCoder coder);
	public HKBiologicalSexObject (MonoTouch.Foundation.NSObjectFlag t);
	public HKBiologicalSexObject (System.IntPtr handle);
	// properties
	public virtual HKBiologicalSex BiologicalSex { get; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKBloodType

```
[Serializable]
public enum HKBloodType {
	ABNegative = 6,
	ABPositive = 5,
	ANegative = 2,
	APositive = 1,
	BNegative = 4,
	BPositive = 3,
	NotSet = 0,
	ONegative = 8,
	OPositive = 7,
}
```

### New Type MonoTouch.HealthKit.HKBloodTypeObject

```
public class HKBloodTypeObject : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKBloodTypeObject ();
	public HKBloodTypeObject (MonoTouch.Foundation.NSCoder coder);
	public HKBloodTypeObject (MonoTouch.Foundation.NSObjectFlag t);
	public HKBloodTypeObject (System.IntPtr handle);
	// properties
	public virtual HKBloodType BloodType { get; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKBodyTemperatureSensorLocation

```
[Serializable]
public enum HKBodyTemperatureSensorLocation {
	Armpit = 1,
	Body = 2,
	Ear = 3,
	EarDrum = 9,
	Finger = 4,
	Forehead = 11,
	GastroIntestinal = 5,
	Mouth = 6,
	Other = 0,
	Rectum = 7,
	TemporalArtery = 10,
	Toe = 8,
}
```

### New Type MonoTouch.HealthKit.HKCategorySample

```
public class HKCategorySample : MonoTouch.HealthKit.HKSample, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCategorySample (MonoTouch.Foundation.NSCoder coder);
	public HKCategorySample (MonoTouch.Foundation.NSObjectFlag t);
	public HKCategorySample (System.IntPtr handle);
	// properties
	public virtual HKCategoryType CategoryType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int Value { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static HKCategorySample FromType (HKCategoryType type, int value, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSDictionary metadata);
	public static HKCategorySample FromType (HKCategoryType type, int value, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKMetadata metadata);
	public static HKCategorySample FromType (HKCategoryType type, int value, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate);
}
```

### New Type MonoTouch.HealthKit.HKCategoryType

```
public class HKCategoryType : MonoTouch.HealthKit.HKSampleType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCategoryType (MonoTouch.Foundation.NSCoder coder);
	public HKCategoryType (MonoTouch.Foundation.NSObjectFlag t);
	public HKCategoryType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static HKCategoryType Create (HKCategoryTypeIdentifier kind);
}
```

### New Type MonoTouch.HealthKit.HKCategoryTypeIdentifier

```
[Serializable]
public enum HKCategoryTypeIdentifier {
	SleepAnalysis = 0,
}
```

### New Type MonoTouch.HealthKit.HKCategoryTypeIdentifierKey

```
public static class HKCategoryTypeIdentifierKey {
	// properties
	public static MonoTouch.Foundation.NSString SleepAnalysis { get; }
}
```

### New Type MonoTouch.HealthKit.HKCategoryValueSleepAnalysis

```
[Serializable]
public enum HKCategoryValueSleepAnalysis {
	Asleep = 1,
	InBed = 0,
}
```

### New Type MonoTouch.HealthKit.HKCharacteristicType

```
public class HKCharacteristicType : MonoTouch.HealthKit.HKObjectType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCharacteristicType (MonoTouch.Foundation.NSCoder coder);
	public HKCharacteristicType (MonoTouch.Foundation.NSObjectFlag t);
	public HKCharacteristicType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static HKCharacteristicType Create (HKCharacteristicTypeIdentifier kind);
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

### New Type MonoTouch.HealthKit.HKCharacteristicTypeIdentifierKey

```
public static class HKCharacteristicTypeIdentifierKey {
	// properties
	public static MonoTouch.Foundation.NSString BiologicalSex { get; }
	public static MonoTouch.Foundation.NSString BloodType { get; }
	public static MonoTouch.Foundation.NSString DateOfBirth { get; }
}
```

### New Type MonoTouch.HealthKit.HKCorrelation

```
public class HKCorrelation : MonoTouch.HealthKit.HKSample, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCorrelation (MonoTouch.Foundation.NSCoder coder);
	public HKCorrelation (MonoTouch.Foundation.NSObjectFlag t);
	public HKCorrelation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual HKCorrelationType CorrelationType { get; }
	public virtual MonoTouch.Foundation.NSSet Objects { get; }
	// methods
	public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects, MonoTouch.Foundation.NSDictionary metadata);
	public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects, HKMetadata metadata);
	public static HKCorrelation Create (HKCorrelationType correlationType, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSSet objects);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSSet GetObjects (HKObjectType objectType);
}
```

### New Type MonoTouch.HealthKit.HKCorrelationQuery

```
public class HKCorrelationQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKCorrelationQuery (MonoTouch.Foundation.NSCoder coder);
	public HKCorrelationQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKCorrelationQuery (System.IntPtr handle);
	public HKCorrelationQuery (HKCorrelationType correlationType, MonoTouch.Foundation.NSPredicate predicate, MonoTouch.Foundation.NSDictionary samplePredicates, HKCorrelationQueryResultHandler completion);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual HKCorrelationType CorrelationType { get; }
	public virtual MonoTouch.Foundation.NSDictionary SamplePredicates { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKCorrelationQueryResultHandler

```
public sealed delegate HKCorrelationQueryResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKCorrelationQueryResultHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKCorrelationQuery query, HKCorrelation[] correlations, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKCorrelationQuery query, HKCorrelation[] correlations, MonoTouch.Foundation.NSError error);
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

### New Type MonoTouch.HealthKit.HKCorrelationTypeKey

```
public static class HKCorrelationTypeKey {
	// properties
	public static MonoTouch.Foundation.NSString IdentifierBloodPressure { get; }
	public static MonoTouch.Foundation.NSString IdentifierFood { get; }
}
```

### New Type MonoTouch.HealthKit.HKErrorCode

```
[Serializable]
public enum HKErrorCode {
	AuthorizationDenied = 4,
	AuthorizationNotDetermined = 5,
	DatabaseInaccessible = 6,
	HealthDataRestricted = 2,
	HealthDataUnavailable = 1,
	InvalidArgument = 3,
	NoError = 0,
	UserCanceled = 7,
}
```

### New Type MonoTouch.HealthKit.HKHealthStore

```
public class HKHealthStore : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKHealthStore ();
	public HKHealthStore (MonoTouch.Foundation.NSCoder coder);
	public HKHealthStore (MonoTouch.Foundation.NSObjectFlag t);
	public HKHealthStore (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static bool IsHealthDataAvailable { get; }
	// methods
	public virtual void AddSamples (HKSample[] samples, HKWorkout workout, HKStoreSampleAddedCallback callback);
	public virtual void DeleteObject (HKObject obj, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<bool> DeleteObjectAsync (HKObject obj);
	public virtual void DisableAllBackgroundDelivery (System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual void DisableBackgroundDelivery (HKObjectType type, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual void EnableBackgroundDelivery (HKObjectType type, HKUpdateFrequency frequency, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual void ExecuteQuery (HKQuery query);
	public virtual HKAuthorizationStatus GetAuthorizationStatus (HKObjectType type);
	public virtual HKBiologicalSexObject GetBiologicalSex (out MonoTouch.Foundation.NSError error);
	public virtual HKBloodTypeObject GetBloodType (out MonoTouch.Foundation.NSError error);
	public virtual MonoTouch.Foundation.NSDate GetDateOfBirth (out MonoTouch.Foundation.NSError error);
	public virtual void RequestAuthorizationToShare (MonoTouch.Foundation.NSSet typesToShare, MonoTouch.Foundation.NSSet typesToRead, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<bool> RequestAuthorizationToShareAsync (MonoTouch.Foundation.NSSet typesToShare, MonoTouch.Foundation.NSSet typesToRead);
	public virtual void SaveObject (HKObject obj, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<bool> SaveObjectAsync (HKObject obj);
	public virtual void SaveObjects (HKObject[] objects, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<bool> SaveObjectsAsync (HKObject[] objects);
	public virtual void StopQuery (HKQuery query);
}
```

### New Type MonoTouch.HealthKit.HKHeartRateSensorLocation

```
[Serializable]
public enum HKHeartRateSensorLocation {
	Chest = 1,
	EarLobe = 5,
	Finger = 3,
	Foot = 6,
	Hand = 4,
	Other = 0,
	Wrist = 2,
}
```

### New Type MonoTouch.HealthKit.HKMetadata

```
public class HKMetadata : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public HKMetadata ();
	public HKMetadata (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public HKBodyTemperatureSensorLocation? BodyTemperatureSensorLocation { get; set; }
	public bool? CoachedWorkout { get; set; }
	public string DeviceManufacturerName { get; set; }
	public string DeviceName { get; set; }
	public string DeviceSerialNumber { get; set; }
	public string DigitalSignature { get; set; }
	public string ExternalUuid { get; set; }
	public string FoodType { get; set; }
	public bool? GroupFitness { get; set; }
	public HKHeartRateSensorLocation? HeartRateSensorLocation { get; set; }
	public bool? IndoorWorkout { get; set; }
	public MonoTouch.Foundation.NSNumber ReferenceRangeLowerLimit { get; set; }
	public MonoTouch.Foundation.NSNumber ReferenceRangeUpperLimit { get; set; }
	public MonoTouch.Foundation.NSTimeZone TimeZone { get; set; }
	public string UdiDeviceIdentifier { get; set; }
	public string UdiProductionIdentifier { get; set; }
	public bool? WasTakenInLab { get; set; }
	public bool? WasUserEntered { get; set; }
	public string WorkoutBrandName { get; set; }
}
```

### New Type MonoTouch.HealthKit.HKMetadataKey

```
public static class HKMetadataKey {
	// properties
	public static MonoTouch.Foundation.NSString BodyTemperatureSensorLocation { get; }
	public static MonoTouch.Foundation.NSString CoachedWorkout { get; }
	public static MonoTouch.Foundation.NSString DeviceManufacturerName { get; }
	public static MonoTouch.Foundation.NSString DeviceName { get; }
	public static MonoTouch.Foundation.NSString DeviceSerialNumber { get; }
	public static MonoTouch.Foundation.NSString DigitalSignature { get; }
	public static MonoTouch.Foundation.NSString ExternalUuid { get; }
	public static MonoTouch.Foundation.NSString FoodType { get; }
	public static MonoTouch.Foundation.NSString GroupFitness { get; }
	public static MonoTouch.Foundation.NSString HeartRateSensorLocation { get; }
	public static MonoTouch.Foundation.NSString IndoorWorkout { get; }
	public static MonoTouch.Foundation.NSString ReferenceRangeLowerLimit { get; }
	public static MonoTouch.Foundation.NSString ReferenceRangeUpperLimit { get; }
	public static MonoTouch.Foundation.NSString TimeZone { get; }
	public static MonoTouch.Foundation.NSString UdiDeviceIdentifier { get; }
	public static MonoTouch.Foundation.NSString UdiProductionIdentifier { get; }
	public static MonoTouch.Foundation.NSString WasTakenInLab { get; }
	public static MonoTouch.Foundation.NSString WasUserEntered { get; }
	public static MonoTouch.Foundation.NSString WorkoutBrandName { get; }
}
```

### New Type MonoTouch.HealthKit.HKMetricPrefix

```
[Serializable]
public enum HKMetricPrefix {
	Centi = 5,
	Deca = 7,
	Deci = 6,
	Giga = 11,
	Hecto = 8,
	Kilo = 9,
	Mega = 10,
	Micro = 3,
	Milli = 4,
	Nano = 2,
	None = 0,
	Pico = 1,
	Tera = 12,
}
```

### New Type MonoTouch.HealthKit.HKObject

```
public class HKObject : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKObject (MonoTouch.Foundation.NSCoder coder);
	public HKObject (MonoTouch.Foundation.NSObjectFlag t);
	public HKObject (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public HKMetadata Metadata { get; }
	public virtual HKSource Source { get; }
	public virtual MonoTouch.Foundation.NSUuid Uuid { get; }
	public virtual MonoTouch.Foundation.NSDictionary WeakMetadata { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKObjectType

```
public class HKObjectType : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKObjectType (MonoTouch.Foundation.NSCoder coder);
	public HKObjectType (MonoTouch.Foundation.NSObjectFlag t);
	public HKObjectType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSString Identifier { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static HKCategoryType GetCategoryType (MonoTouch.Foundation.NSString hkCategoryTypeIdentifier);
	public static HKCharacteristicType GetCharacteristicType (MonoTouch.Foundation.NSString hkCharacteristicTypeIdentifier);
	public static HKCorrelationType GetCorrelationType (MonoTouch.Foundation.NSString hkCorrelationTypeIdentifier);
	public static HKQuantityType GetQuantityType (MonoTouch.Foundation.NSString hkTypeIdentifier);
	public static HKWorkout WorkoutType ();
}
```

### New Type MonoTouch.HealthKit.HKObserverQuery

```
public class HKObserverQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKObserverQuery (MonoTouch.Foundation.NSCoder coder);
	public HKObserverQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKObserverQuery (System.IntPtr handle);
	public HKObserverQuery (HKSampleType sampleType, MonoTouch.Foundation.NSPredicate predicate, HKObserverQueryUpdateHandler updateHandler);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKObserverQueryCompletionHandler

```
public sealed delegate HKObserverQueryCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKObserverQueryCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke ();
}
```

### New Type MonoTouch.HealthKit.HKObserverQueryUpdateHandler

```
public sealed delegate HKObserverQueryUpdateHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKObserverQueryUpdateHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, MonoTouch.Foundation.NSError error);
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

### New Type MonoTouch.HealthKit.HKQuantity

```
public class HKQuantity : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKQuantity (MonoTouch.Foundation.NSCoder coder);
	public HKQuantity (MonoTouch.Foundation.NSObjectFlag t);
	public HKQuantity (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSComparisonResult Compare (HKQuantity quantity);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static HKQuantity FromQuantity (HKUnit unit, double value);
	public virtual double GetDoubleValue (HKUnit unit);
	public virtual bool IsCompatible (HKUnit unit);
}
```

### New Type MonoTouch.HealthKit.HKQuantityAggregationStyle

```
[Serializable]
public enum HKQuantityAggregationStyle {
	Cumulative = 0,
	Discrete = 1,
}
```

### New Type MonoTouch.HealthKit.HKQuantitySample

```
public class HKQuantitySample : MonoTouch.HealthKit.HKSample, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKQuantitySample (MonoTouch.Foundation.NSCoder coder);
	public HKQuantitySample (MonoTouch.Foundation.NSObjectFlag t);
	public HKQuantitySample (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual HKQuantity Quantity { get; }
	public virtual HKQuantityType QuantityType { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static HKQuantitySample FromType (HKQuantityType quantityType, HKQuantity quantity, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, MonoTouch.Foundation.NSDictionary metadata);
	public static HKQuantitySample FromType (HKQuantityType quantityType, HKQuantity quantity, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKMetadata metadata);
}
```

### New Type MonoTouch.HealthKit.HKQuantityType

```
public class HKQuantityType : MonoTouch.HealthKit.HKSampleType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKQuantityType (MonoTouch.Foundation.NSCoder coder);
	public HKQuantityType (MonoTouch.Foundation.NSObjectFlag t);
	public HKQuantityType (System.IntPtr handle);
	// properties
	public virtual HKQuantityAggregationStyle AggregationStyle { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static HKQuantityType Create (HKQuantityTypeIdentifier kind);
	public virtual bool IsCompatible (HKUnit unit);
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
	BodyTemperature = 25,
	DietaryBiotin = 50,
	DietaryCaffeine = 63,
	DietaryCalcium = 44,
	DietaryCarbohydrates = 32,
	DietaryChloride = 61,
	DietaryCholesterol = 30,
	DietaryChromium = 59,
	DietaryCopper = 57,
	DietaryEnergyConsumed = 35,
	DietaryFatMonounsaturated = 28,
	DietaryFatPolyunsaturated = 27,
	DietaryFatSaturated = 29,
	DietaryFatTotal = 26,
	DietaryFiber = 33,
	DietaryFolate = 49,
	DietaryIodine = 53,
	DietaryIron = 45,
	DietaryMagnesium = 54,
	DietaryManganese = 58,
	DietaryMolybdenum = 60,
	DietaryNiacin = 48,
	DietaryPantothenicAcid = 51,
	DietaryPhosphorus = 52,
	DietaryPotassium = 62,
	DietaryProtein = 36,
	DietaryRiboflavin = 47,
	DietarySelenium = 56,
	DietarySodium = 31,
	DietarySugar = 34,
	DietaryThiamin = 46,
	DietaryVitaminA = 37,
	DietaryVitaminB12 = 39,
	DietaryVitaminB6 = 38,
	DietaryVitaminC = 40,
	DietaryVitaminD = 41,
	DietaryVitaminE = 42,
	DietaryVitaminK = 43,
	DietaryZinc = 55,
	DistanceCycling = 8,
	DistanceWalkingRunning = 7,
	FlightsClimbed = 11,
	ForcedExpiratoryVolume1 = 20,
	ForcedVitalCapacity = 19,
	HeartRate = 5,
	Height = 2,
	InhalerUsage = 23,
	LeanBodyMass = 4,
	NikeFuel = 12,
	NumberOfTimesFallen = 22,
	OxygenSaturation = 13,
	PeakExpiratoryFlowRate = 21,
	PeripheralPerfusionIndex = 18,
	RespiratoryRate = 24,
	StepCount = 6,
}
```

### New Type MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

```
public static class HKQuantityTypeIdentifierKey {
	// properties
	public static MonoTouch.Foundation.NSString ActiveEnergyBurned { get; }
	public static MonoTouch.Foundation.NSString BasalEnergyBurned { get; }
	public static MonoTouch.Foundation.NSString BloodAlcoholContent { get; }
	public static MonoTouch.Foundation.NSString BloodGlucose { get; }
	public static MonoTouch.Foundation.NSString BloodPressureDiastolic { get; }
	public static MonoTouch.Foundation.NSString BloodPressureSystolic { get; }
	public static MonoTouch.Foundation.NSString BodyFatPercentage { get; }
	public static MonoTouch.Foundation.NSString BodyMass { get; }
	public static MonoTouch.Foundation.NSString BodyMassIndex { get; }
	public static MonoTouch.Foundation.NSString BodyTemperature { get; }
	public static MonoTouch.Foundation.NSString DietaryBiotin { get; }
	public static MonoTouch.Foundation.NSString DietaryCaffeine { get; }
	public static MonoTouch.Foundation.NSString DietaryCalcium { get; }
	public static MonoTouch.Foundation.NSString DietaryCarbohydrates { get; }
	public static MonoTouch.Foundation.NSString DietaryChloride { get; }
	public static MonoTouch.Foundation.NSString DietaryCholesterol { get; }
	public static MonoTouch.Foundation.NSString DietaryChromium { get; }
	public static MonoTouch.Foundation.NSString DietaryCopper { get; }
	public static MonoTouch.Foundation.NSString DietaryEnergyConsumed { get; }
	public static MonoTouch.Foundation.NSString DietaryFatMonounsaturated { get; }
	public static MonoTouch.Foundation.NSString DietaryFatPolyunsaturated { get; }
	public static MonoTouch.Foundation.NSString DietaryFatSaturated { get; }
	public static MonoTouch.Foundation.NSString DietaryFatTotal { get; }
	public static MonoTouch.Foundation.NSString DietaryFiber { get; }
	public static MonoTouch.Foundation.NSString DietaryFolate { get; }
	public static MonoTouch.Foundation.NSString DietaryIodine { get; }
	public static MonoTouch.Foundation.NSString DietaryIron { get; }
	public static MonoTouch.Foundation.NSString DietaryMagnesium { get; }
	public static MonoTouch.Foundation.NSString DietaryManganese { get; }
	public static MonoTouch.Foundation.NSString DietaryMolybdenum { get; }
	public static MonoTouch.Foundation.NSString DietaryNiacin { get; }
	public static MonoTouch.Foundation.NSString DietaryPantothenicAcid { get; }
	public static MonoTouch.Foundation.NSString DietaryPhosphorus { get; }
	public static MonoTouch.Foundation.NSString DietaryPotassium { get; }
	public static MonoTouch.Foundation.NSString DietaryProtein { get; }
	public static MonoTouch.Foundation.NSString DietaryRiboflavin { get; }
	public static MonoTouch.Foundation.NSString DietarySelenium { get; }
	public static MonoTouch.Foundation.NSString DietarySodium { get; }
	public static MonoTouch.Foundation.NSString DietarySugar { get; }
	public static MonoTouch.Foundation.NSString DietaryThiamin { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminA { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminB12 { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminB6 { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminC { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminD { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminE { get; }
	public static MonoTouch.Foundation.NSString DietaryVitaminK { get; }
	public static MonoTouch.Foundation.NSString DietaryZinc { get; }
	public static MonoTouch.Foundation.NSString DistanceCycling { get; }
	public static MonoTouch.Foundation.NSString DistanceWalkingRunning { get; }
	public static MonoTouch.Foundation.NSString FlightsClimbed { get; }
	public static MonoTouch.Foundation.NSString ForcedExpiratoryVolume1 { get; }
	public static MonoTouch.Foundation.NSString ForcedVitalCapacity { get; }
	public static MonoTouch.Foundation.NSString HeartRate { get; }
	public static MonoTouch.Foundation.NSString Height { get; }
	public static MonoTouch.Foundation.NSString InhalerUsage { get; }
	public static MonoTouch.Foundation.NSString LeanBodyMass { get; }
	public static MonoTouch.Foundation.NSString NikeFuel { get; }
	public static MonoTouch.Foundation.NSString NumberOfTimesFallen { get; }
	public static MonoTouch.Foundation.NSString OxygenSaturation { get; }
	public static MonoTouch.Foundation.NSString PeakExpiratoryFlowRate { get; }
	public static MonoTouch.Foundation.NSString PeripheralPerfusionIndex { get; }
	public static MonoTouch.Foundation.NSString RespiratoryRate { get; }
	public static MonoTouch.Foundation.NSString StepCount { get; }
}
```

### New Type MonoTouch.HealthKit.HKQuery

```
public class HKQuery : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKQuery (MonoTouch.Foundation.NSCoder coder);
	public HKQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKQuery (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; }
	public virtual HKSampleType SampleType { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForCategorySamples (MonoTouch.Foundation.NSPredicateOperatorType operatorType, int value);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForDuration (MonoTouch.Foundation.NSPredicateOperatorType operatorType, double duration);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey, MonoTouch.Foundation.NSObject[] allowedValues);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey, MonoTouch.Foundation.NSPredicateOperatorType operatorType, MonoTouch.Foundation.NSObject value);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObject (MonoTouch.Foundation.NSUuid objectUuid);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjects (MonoTouch.Foundation.NSSet objectUuids);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromSource (HKSource source);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromSources (MonoTouch.Foundation.NSSet sources);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromWorkout (HKWorkout workout);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForQuantitySamples (MonoTouch.Foundation.NSPredicateOperatorType operatorType, HKQuantity quantity);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForSamples (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKQueryOptions options);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForTotalDistance (MonoTouch.Foundation.NSPredicateOperatorType operatorType, HKQuantity totalDistance);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForTotalEnergyBurned (MonoTouch.Foundation.NSPredicateOperatorType operatorType, HKQuantity totalEnergyBurned);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForWorkouts (HKWorkoutActivityType workoutActivityType);
	public static MonoTouch.Foundation.NSPredicate PredicateForObjectsWithNoCorrelation ();
}
```

### New Type MonoTouch.HealthKit.HKQueryOptions

```
[Serializable]
[Flags]
public enum HKQueryOptions {
	None = 0,
	StrictEndDate = 2,
	StrictStartDate = 1,
}
```

### New Type MonoTouch.HealthKit.HKSample

```
public class HKSample : MonoTouch.HealthKit.HKObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKSample (MonoTouch.Foundation.NSCoder coder);
	public HKSample (MonoTouch.Foundation.NSObjectFlag t);
	public HKSample (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; }
	public virtual HKSampleType SampleType { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierEndDate { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierStartDate { get; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKSampleQuery

```
public class HKSampleQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKSampleQuery (MonoTouch.Foundation.NSCoder coder);
	public HKSampleQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKSampleQuery (System.IntPtr handle);
	public HKSampleQuery (HKSampleType sampleType, MonoTouch.Foundation.NSPredicate predicate, uint limit, MonoTouch.Foundation.NSSortDescriptor[] sortDescriptors, HKSampleQueryResultsHandler resultsHandler);
	// fields
	public static const int NoLimit;
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint Limit { get; }
	public virtual MonoTouch.Foundation.NSSortDescriptor[] SortDescriptors { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HealthKit.HKSampleQueryResultsHandler

```
public sealed delegate HKSampleQueryResultsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKSampleQueryResultsHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKSampleQuery query, HKSample[] results, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKSampleQuery query, HKSample[] results, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.HealthKit.HKSampleType

```
public class HKSampleType : MonoTouch.HealthKit.HKObjectType, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKSampleType (MonoTouch.Foundation.NSCoder coder);
	public HKSampleType (MonoTouch.Foundation.NSObjectFlag t);
	public HKSampleType (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKSource

```
public class HKSource : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKSource (MonoTouch.Foundation.NSCoder coder);
	public HKSource (MonoTouch.Foundation.NSObjectFlag t);
	public HKSource (System.IntPtr handle);
	// properties
	public virtual string BundleIdentifier { get; }
	public override System.IntPtr ClassHandle { get; }
	public static HKSource GetDefaultSource { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.HealthKit.HKSourceQuery

```
public class HKSourceQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKSourceQuery (MonoTouch.Foundation.NSCoder coder);
	public HKSourceQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKSourceQuery (System.IntPtr handle);
	public HKSourceQuery (HKSampleType sampleType, MonoTouch.Foundation.NSPredicate objectPredicate, HKSourceQueryCompletionHandler completionHandler);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKSourceQueryCompletionHandler

```
public sealed delegate HKSourceQueryCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKSourceQueryCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKSourceQuery query, MonoTouch.Foundation.NSSet sources, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKSourceQuery query, MonoTouch.Foundation.NSSet sources, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.HealthKit.HKStatistics

```
public class HKStatistics : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKStatistics (MonoTouch.Foundation.NSCoder coder);
	public HKStatistics (MonoTouch.Foundation.NSObjectFlag t);
	public HKStatistics (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; }
	public virtual HKQuantityType QuantityType { get; }
	public virtual HKSource[] Sources { get; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; }
	// methods
	public virtual HKQuantity AverageQuantity (HKSource source);
	public virtual HKQuantity AverageQuantity ();
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual HKQuantity MaximumQuantity (HKSource source);
	public virtual HKQuantity MaximumQuantity ();
	public virtual HKQuantity MinimumQuantity (HKSource source);
	public virtual HKQuantity MinimumQuantity ();
	public virtual HKQuantity SumQuantity (HKSource source);
	public virtual HKQuantity SumQuantity ();
}
```

### New Type MonoTouch.HealthKit.HKStatisticsCollection

```
public class HKStatisticsCollection : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKStatisticsCollection (MonoTouch.Foundation.NSCoder coder);
	public HKStatisticsCollection (MonoTouch.Foundation.NSObjectFlag t);
	public HKStatisticsCollection (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSSet Sources { get; }
	public virtual HKStatistics[] Statistics { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnumerateStatistics (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKStatisticsCollectionEnumerator handler);
	public virtual HKStatistics GetStatistics (MonoTouch.Foundation.NSDate date);
}
```

### New Type MonoTouch.HealthKit.HKStatisticsCollectionEnumerator

```
public sealed delegate HKStatisticsCollectionEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKStatisticsCollectionEnumerator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKStatistics result, bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKStatistics result, bool stop);
}
```

### New Type MonoTouch.HealthKit.HKStatisticsCollectionQuery

```
public class HKStatisticsCollectionQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKStatisticsCollectionQuery (MonoTouch.Foundation.NSCoder coder);
	public HKStatisticsCollectionQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKStatisticsCollectionQuery (System.IntPtr handle);
	public HKStatisticsCollectionQuery (HKQuantityType quantityType, MonoTouch.Foundation.NSPredicate quantitySamplePredicate, HKStatisticsOptions options, MonoTouch.Foundation.NSDate anchorDate, MonoTouch.Foundation.NSDateComponents intervalComponents);
	// properties
	public virtual MonoTouch.Foundation.NSDate AnchorDate { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDateComponents IntervalComponents { get; }
	public virtual HKStatisticsOptions Options { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetInitialResultsHandler (HKStatisticsCollectionQueryInitialResultsHandler handler);
	public virtual void SetStatisticsUpdateHandler (HKStatisticsCollectionQueryInitialResultsHandler handler);
}
```

### New Type MonoTouch.HealthKit.HKStatisticsCollectionQueryInitialResultsHandler

```
public sealed delegate HKStatisticsCollectionQueryInitialResultsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKStatisticsCollectionQueryInitialResultsHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKStatisticsCollectionQuery query, HKStatisticsCollection result, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKStatisticsCollectionQuery query, HKStatisticsCollection result, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.HealthKit.HKStatisticsOptions

```
[Serializable]
[Flags]
public enum HKStatisticsOptions {
	CumulativeSum = 16,
	DiscreteAverage = 2,
	DiscreteMax = 8,
	DiscreteMin = 4,
	None = 0,
	SeparateBySource = 1,
}
```

### New Type MonoTouch.HealthKit.HKStatisticsQuery

```
public class HKStatisticsQuery : MonoTouch.HealthKit.HKQuery, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKStatisticsQuery (MonoTouch.Foundation.NSCoder coder);
	public HKStatisticsQuery (MonoTouch.Foundation.NSObjectFlag t);
	public HKStatisticsQuery (System.IntPtr handle);
	public HKStatisticsQuery (HKQuantityType quantityType, MonoTouch.Foundation.NSPredicate quantitySamplePredicate, HKStatisticsOptions options, HKStatisticsQueryHandler handler);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HealthKit.HKStatisticsQueryHandler

```
public sealed delegate HKStatisticsQueryHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HKStatisticsQueryHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (HKStatisticsQuery query, HKStatistics result, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (HKStatisticsQuery query, HKStatistics result, MonoTouch.Foundation.NSError error);
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

### New Type MonoTouch.HealthKit.HKUnit

```
public class HKUnit : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HKUnit (MonoTouch.Foundation.NSCoder coder);
	public HKUnit (MonoTouch.Foundation.NSObjectFlag t);
	public HKUnit (System.IntPtr handle);
	// fields
	public static const double MolarMassBloodGlucose;
	// properties
	public static HKUnit Atmosphere { get; }
	public static HKUnit Calorie { get; }
	public static HKUnit CentimeterOfWater { get; }
	public override System.IntPtr ClassHandle { get; }
	public static HKUnit Count { get; }
	public static HKUnit Day { get; }
	public static HKUnit DegreeCelsius { get; }
	public static HKUnit DegreeFahrenheit { get; }
	public static HKUnit FluidOunceImperialUnit { get; }
	public static HKUnit FluidOunceUSUnit { get; }
	public static HKUnit Foot { get; }
	public static HKUnit Gram { get; }
	public static HKUnit Hour { get; }
	public static HKUnit Inch { get; }
	public virtual bool IsNull { get; }
	public static HKUnit Joule { get; }
	public static HKUnit Kelvin { get; }
	public static HKUnit Kilocalorie { get; }
	public static HKUnit Liter { get; }
	public static HKUnit Meter { get; }
	public static HKUnit Mile { get; }
	public static HKUnit MillimeterOfMercury { get; }
	public static HKUnit Minute { get; }
	public static HKUnit Ounce { get; }
	public static HKUnit Pascal { get; }
	public static HKUnit Percent { get; }
	public static HKUnit PintImperialUnit { get; }
	public static HKUnit PintUSUnit { get; }
	public static HKUnit Pound { get; }
	public static HKUnit Second { get; }
	public static HKUnit Siemen { get; }
	public static HKUnit Stone { get; }
	public virtual string UnitString { get; }
	// methods
	public static HKUnit CreateJouleUnit (HKMetricPrefix prefix);
	public static HKUnit CreateLiterUnit (HKMetricPrefix prefix);
	public static HKUnit CreateMeterUnit (HKMetricPrefix prefix);
	public static HKUnit CreateMoleUnit (double gramsPerMole);
	public static HKUnit CreateMoleUnit (HKMetricPrefix prefix, double gramsPerMole);
	public static HKUnit CreatePascalUnit (HKMetricPrefix prefix);
	public static HKUnit CreateSecondUnit (HKMetricPrefix prefix);
	public static HKUnit CreateSiemenUnit (HKMetricPrefix prefix);
	public static HKUnit FromEnergyFormatterUnit (MonoTouch.Foundation.NSEnergyFormatterUnit energyFormatterUnit);
	public static HKUnit FromGramUnit (HKMetricPrefix prefix);
	public static HKUnit FromLengthFormatterUnit (MonoTouch.Foundation.NSLengthFormatterUnit lengthFormatterUnit);
	public static HKUnit FromMassFormatterUnit (MonoTouch.Foundation.NSMassFormatterUnit massFormatterUnit);
	public static HKUnit FromString (string aString);
	public static MonoTouch.Foundation.NSEnergyFormatterUnit GetEnergyFormatterUnit (HKUnit unit);
	public static MonoTouch.Foundation.NSLengthFormatterUnit GetLengthFormatterUnit (HKUnit unit);
	public static MonoTouch.Foundation.NSMassFormatterUnit GetMassFormatterUnit (HKUnit unit);
	public virtual HKUnit ReciprocalUnit ();
	public virtual HKUnit UnitDividedBy (HKUnit unit);
	public virtual HKUnit UnitMultipliedBy (HKUnit unit);
	public virtual HKUnit UnitRaisedToPower (int power);
}
```

### New Type MonoTouch.HealthKit.HKUpdateFrequency

```
[Serializable]
public enum HKUpdateFrequency {
	Daily = 3,
	Hourly = 2,
	Immediate = 1,
	Weekly = 4,
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
	TrackAndField = 49,
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
	public static MonoTouch.Foundation.NSString Identifier { get; }
}
```

## New Namespace MonoTouch.HomeKit

### New Type MonoTouch.HomeKit.HMAccessory

```
public class HMAccessory : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMAccessory ();
	public HMAccessory (MonoTouch.Foundation.NSCoder coder);
	public HMAccessory (MonoTouch.Foundation.NSObjectFlag t);
	public HMAccessory (System.IntPtr handle);
	// properties
	public virtual bool Blocked { get; }
	public virtual bool Bridged { get; }
	public override System.IntPtr ClassHandle { get; }
	public HMAccessoryDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSUuid Identifier { get; }
	public virtual MonoTouch.Foundation.NSUuid[] IdentifiersForBridgedAccessories { get; }
	public virtual string Name { get; }
	public virtual bool Reachable { get; }
	public virtual HMRoom Room { get; }
	public virtual HMService[] Services { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<HMAccessoryUpdateEventArgs> DidUpdateAssociatedServiceType;
	public event System.EventHandler DidUpdateName;
	public event System.EventHandler<HMAccessoryUpdateEventArgs> DidUpdateNameForService;
	public event System.EventHandler DidUpdateReachability;
	public event System.EventHandler DidUpdateServices;
	public event System.EventHandler<HMAccessoryServiceUpdateCharacteristicEventArgs> DidUpdateValueForCharacteristic;
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Identify (System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task IdentifyAsync ();
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMAccessoryBrowser

```
public class HMAccessoryBrowser : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMAccessoryBrowser ();
	public HMAccessoryBrowser (MonoTouch.Foundation.NSCoder coder);
	public HMAccessoryBrowser (MonoTouch.Foundation.NSObjectFlag t);
	public HMAccessoryBrowser (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public HMAccessoryBrowserDelegate Delegate { get; set; }
	public virtual HMAccessory[] DiscoveredAccessories { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<HMAccessoryBrowserEventArgs> DidFindNewAccessory;
	public event System.EventHandler<HMAccessoryBrowserEventArgs> DidRemoveNewAccessory;
	// methods
	protected override void Dispose (bool disposing);
	public virtual void StartSearchingForNewAccessories ();
	public virtual void StopSearchingForNewAccessories ();
}
```

### New Type MonoTouch.HomeKit.HMAccessoryBrowserDelegate

```
public class HMAccessoryBrowserDelegate : MonoTouch.Foundation.NSObject, IHMAccessoryBrowserDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMAccessoryBrowserDelegate ();
	public HMAccessoryBrowserDelegate (MonoTouch.Foundation.NSCoder coder);
	public HMAccessoryBrowserDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public HMAccessoryBrowserDelegate (System.IntPtr handle);
	// methods
	public virtual void DidFindNewAccessory (HMAccessoryBrowser browser, HMAccessory accessory);
	public virtual void DidRemoveNewAccessory (HMAccessoryBrowser browser, HMAccessory accessory);
}
```

### New Type MonoTouch.HomeKit.HMAccessoryBrowserDelegate_Extensions

```
public static class HMAccessoryBrowserDelegate_Extensions {
	// methods
	public static void DidFindNewAccessory (IHMAccessoryBrowserDelegate This, HMAccessoryBrowser browser, HMAccessory accessory);
	public static void DidRemoveNewAccessory (IHMAccessoryBrowserDelegate This, HMAccessoryBrowser browser, HMAccessory accessory);
}
```

### New Type MonoTouch.HomeKit.HMAccessoryBrowserEventArgs

```
public class HMAccessoryBrowserEventArgs : System.EventArgs {
	// constructors
	public HMAccessoryBrowserEventArgs (HMAccessory accessory);
	// properties
	public HMAccessory Accessory { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMAccessoryDelegate

```
public class HMAccessoryDelegate : MonoTouch.Foundation.NSObject, IHMAccessoryDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMAccessoryDelegate ();
	public HMAccessoryDelegate (MonoTouch.Foundation.NSCoder coder);
	public HMAccessoryDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public HMAccessoryDelegate (System.IntPtr handle);
	// methods
	public virtual void DidUpdateAssociatedServiceType (HMAccessory accessory, HMService service);
	public virtual void DidUpdateName (HMAccessory accessory);
	public virtual void DidUpdateNameForService (HMAccessory accessory, HMService service);
	public virtual void DidUpdateReachability (HMAccessory accessory);
	public virtual void DidUpdateServices (HMAccessory accessory);
	public virtual void DidUpdateValueForCharacteristic (HMAccessory accessory, HMService service, HMCharacteristic characteristic);
}
```

### New Type MonoTouch.HomeKit.HMAccessoryDelegate_Extensions

```
public static class HMAccessoryDelegate_Extensions {
	// methods
	public static void DidUpdateAssociatedServiceType (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);
	public static void DidUpdateName (IHMAccessoryDelegate This, HMAccessory accessory);
	public static void DidUpdateNameForService (IHMAccessoryDelegate This, HMAccessory accessory, HMService service);
	public static void DidUpdateReachability (IHMAccessoryDelegate This, HMAccessory accessory);
	public static void DidUpdateServices (IHMAccessoryDelegate This, HMAccessory accessory);
	public static void DidUpdateValueForCharacteristic (IHMAccessoryDelegate This, HMAccessory accessory, HMService service, HMCharacteristic characteristic);
}
```

### New Type MonoTouch.HomeKit.HMAccessoryServiceUpdateCharacteristicEventArgs

```
public class HMAccessoryServiceUpdateCharacteristicEventArgs : System.EventArgs {
	// constructors
	public HMAccessoryServiceUpdateCharacteristicEventArgs (HMService service, HMCharacteristic characteristic);
	// properties
	public HMCharacteristic Characteristic { get; set; }
	public HMService Service { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMAccessoryUpdateEventArgs

```
public class HMAccessoryUpdateEventArgs : System.EventArgs {
	// constructors
	public HMAccessoryUpdateEventArgs (HMService service);
	// properties
	public HMService Service { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMAction

```
public class HMAction : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMAction ();
	public HMAction (MonoTouch.Foundation.NSCoder coder);
	public HMAction (MonoTouch.Foundation.NSObjectFlag t);
	public HMAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.HomeKit.HMActionSet

```
public class HMActionSet : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMActionSet (MonoTouch.Foundation.NSCoder coder);
	public HMActionSet (MonoTouch.Foundation.NSObjectFlag t);
	public HMActionSet (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSSet Actions { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Executing { get; }
	public virtual string Name { get; }
	// methods
	public virtual void AddAction (HMAction action, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddActionAsync (HMAction action);
	protected override void Dispose (bool disposing);
	public virtual void RemoveAction (HMAction action, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveActionAsync (HMAction action);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMCharacteristic

```
public class HMCharacteristic : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMCharacteristic ();
	public HMCharacteristic (MonoTouch.Foundation.NSCoder coder);
	public HMCharacteristic (MonoTouch.Foundation.NSObjectFlag t);
	public HMCharacteristic (System.IntPtr handle);
	// properties
	public HMCharacteristicType CharacteristicType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual HMCharacteristicMetadata Metadata { get; }
	public virtual bool NotificationEnabled { get; }
	public virtual MonoTouch.Foundation.NSString[] Properties { get; }
	public bool Readable { get; }
	public virtual HMService Service { get; }
	public bool SupportsEventNotification { get; }
	public virtual MonoTouch.Foundation.NSObject Value { get; }
	public bool Writable { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnableNotification (bool enable, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task EnableNotificationAsync (bool enable);
	public virtual void ReadValue (System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task ReadValueAsync ();
	public virtual void UpdateAuthorizationData (MonoTouch.Foundation.NSData data, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateAuthorizationDataAsync (MonoTouch.Foundation.NSData data);
	public virtual void WriteValue (MonoTouch.Foundation.NSObject value, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task WriteValueAsync (MonoTouch.Foundation.NSObject value);
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicMetadata

```
public class HMCharacteristicMetadata : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMCharacteristicMetadata ();
	public HMCharacteristicMetadata (MonoTouch.Foundation.NSCoder coder);
	public HMCharacteristicMetadata (MonoTouch.Foundation.NSObjectFlag t);
	public HMCharacteristicMetadata (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public HMCharacteristicMetadataFormat Format { get; }
	public virtual string ManufacturerDescription { get; }
	public virtual MonoTouch.Foundation.NSNumber MaximumValue { get; }
	public virtual MonoTouch.Foundation.NSNumber MaxLength { get; }
	public virtual MonoTouch.Foundation.NSNumber MinimumValue { get; }
	public virtual MonoTouch.Foundation.NSNumber StepValue { get; }
	public HMCharacteristicMetadataUnits Units { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicMetadataFormat

```
[Serializable]
public enum HMCharacteristicMetadataFormat {
	Array = 5,
	Bool = 1,
	Data = 11,
	Dictionary = 6,
	Float = 3,
	Int = 2,
	None = 0,
	String = 4,
	Tlv8 = 12,
	UInt16 = 8,
	UInt32 = 9,
	UInt64 = 10,
	UInt8 = 7,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicMetadataUnits

```
[Serializable]
public enum HMCharacteristicMetadataUnits {
	ArcDegree = 4,
	Celsius = 1,
	Fahrenheit = 2,
	None = 0,
	Percentage = 3,
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicProperties

```
public class HMCharacteristicProperties {
	// constructors
	public HMCharacteristicProperties ();
	// properties
	public bool Readable { get; set; }
	public bool SupportsBonjourNotification { get; set; }
	public bool SupportsChangeNumber { get; set; }
	public bool SupportsEventNotification { get; set; }
	public bool Writable { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMCharacteristicType

```
[Serializable]
public enum HMCharacteristicType {
	AdminOnlyAccess = 29,
	AudioFeedback = 28,
	Brightness = 4,
	CoolingThreshold = 10,
	CurrentDoorState = 15,
	CurrentHeatingCooling = 8,
	CurrentLockMechanismState = 31,
	CurrentRelativeHumidity = 13,
	CurrentTemperature = 6,
	HeatingCoolingStatus = 12,
	HeatingThreshold = 11,
	Hue = 2,
	Identify = 22,
	LockManagementAutoSecureTimeout = 35,
	LockManagementControlPoint = 34,
	LockMechanismLastKnownAction = 33,
	Logs = 27,
	Manufacturer = 19,
	Model = 20,
	MotionDetected = 30,
	Name = 18,
	None = 0,
	ObstructionDetected = 17,
	OutletInUse = 25,
	PowerState = 1,
	RotationDirection = 23,
	RotationSpeed = 24,
	Saturation = 3,
	SerialNumber = 21,
	TargetDoorState = 16,
	TargetHeatingCooling = 9,
	TargetLockMechanismState = 32,
	TargetRelativeHumidity = 14,
	TargetTemperature = 7,
	TemperatureUnits = 5,
	Version = 26,
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

### New Type MonoTouch.HomeKit.HMCharacteristicWriteAction

```
public class HMCharacteristicWriteAction : MonoTouch.HomeKit.HMAction, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMCharacteristicWriteAction (MonoTouch.Foundation.NSCoder coder);
	public HMCharacteristicWriteAction (MonoTouch.Foundation.NSObjectFlag t);
	public HMCharacteristicWriteAction (System.IntPtr handle);
	public HMCharacteristicWriteAction (HMCharacteristic characteristic, MonoTouch.Foundation.NSObject targetValue);
	// properties
	public virtual HMCharacteristic Characteristic { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject TargetValue { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void UpdateTargetValue (MonoTouch.Foundation.NSObject targetValue, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateTargetValueAsync (MonoTouch.Foundation.NSObject targetValue);
}
```

### New Type MonoTouch.HomeKit.HMError

```
[Serializable]
public enum HMError {
	AccessDenied = 10,
	AccessoryDiscoveryFailed = 57,
	AccessoryIsBlocked = 61,
	AccessoryIsBusy = 14,
	AccessoryNotReachable = 4,
	AccessoryOutOfCompliance = 66,
	AccessoryOutOfResources = 16,
	AccessoryPairingFailed = 18,
	AccessoryPoweredOff = 9,
	AccessoryResponseError = 59,
	AccessorySentInvalidResponse = 50,
	ActionInAnotherActionSet = 30,
	ActionSetExecutionFailed = 63,
	ActionSetExecutionInProgress = 65,
	ActionSetExecutionPartialSuccess = 64,
	AddAccessoryFailed = 79,
	AlreadyExists = 1,
	CannotActivateTriggerTooFarInFuture = 71,
	CannotRemoveNonBridgeAccessory = 34,
	ClientRequestError = 58,
	CloudDataSyncInProgress = 77,
	CommunicationFailure = 54,
	DataResetFailure = 67,
	DateMustBeOnSpecifiedBoundaries = 70,
	FireDateInPast = 28,
	GenericError = 52,
	HomeAccessNotAuthorized = 47,
	HomeWithSimilarNameExists = 32,
	InsufficientPrivileges = 17,
	InvalidAssociatedServiceType = 62,
	InvalidClass = 22,
	InvalidDataFormatSpecified = 19,
	InvalidMessageSize = 56,
	InvalidParameter = 3,
	InvalidValueType = 43,
	KeychainSyncNotEnabled = 76,
	MaximumObjectLimitReached = 49,
	MessageAuthenticationFailed = 55,
	MissingEntitlement = 80,
	MissingParameter = 27,
	NameContainsProhibitedCharacters = 35,
	NameDoesNotEndWithValidCharacters = 60,
	NameDoesNotStartWithValidCharacters = 36,
	NetworkUnavailable = 78,
	NilParameter = 20,
	NoActionsInActionSet = 25,
	NoRegisteredActionSets = 26,
	NotFound = 2,
	NotificationAlreadyEnabled = 68,
	NotificationNotSupported = 7,
	NotSignedIntoiCloud = 75,
	ObjectAlreadyAssociatedToHome = 13,
	ObjectAssociatedToAnotherHome = 11,
	ObjectNotAssociatedToAnyHome = 12,
	ObjectWithSimilarNameExistsInHome = 31,
	OperationCancelled = 23,
	OperationInProgress = 15,
	OperationNotSupported = 48,
	OperationTimedOut = 8,
	ReadOnlyCharacteristic = 5,
	ReadWriteFailure = 74,
	ReadWritePartialSuccess = 73,
	RecurrenceMustBeOnSpecifiedBoundaries = 69,
	RecurrenceTooLarge = 72,
	RecurrenceTooSmall = 42,
	RenameWithSimilarName = 33,
	RoomForHomeCannotBeInZone = 24,
	RoomForHomeCannotBeUpdated = 29,
	SecurityFailure = 53,
	StringLongerThanMaximum = 46,
	StringShorterThanMinimum = 51,
	UnconfiguredParameter = 21,
	UserDeclinedAddingUser = 38,
	UserDeclinedInvite = 40,
	UserDeclinedRemovingUser = 39,
	UserIDNotEmailAddress = 37,
	UserManagementFailed = 41,
	ValueHigherThanMaximum = 45,
	ValueLowerThanMinimum = 44,
	WriteOnlyCharacteristic = 6,
}
```

### New Type MonoTouch.HomeKit.HMErrors

```
public static class HMErrors {
	// properties
	public static MonoTouch.Foundation.NSString HMErrorDomain { get; }
}
```

### New Type MonoTouch.HomeKit.HMHome

```
public class HMHome : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMHome (MonoTouch.Foundation.NSCoder coder);
	public HMHome (MonoTouch.Foundation.NSObjectFlag t);
	public HMHome (System.IntPtr handle);
	// properties
	public virtual HMAccessory[] Accessories { get; }
	public virtual HMActionSet[] ActionSets { get; }
	public override System.IntPtr ClassHandle { get; }
	public HMHomeDelegate Delegate { get; set; }
	public virtual string Name { get; }
	public virtual bool Primary { get; }
	public virtual HMRoom[] Rooms { get; }
	public virtual HMServiceGroup[] ServiceGroups { get; }
	public virtual HMTrigger[] Triggers { get; }
	public static MonoTouch.Foundation.NSString UserFailedAccessoriesKey { get; }
	public virtual HMUser[] Users { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	public virtual HMZone[] Zones { get; }
	// events
	public event System.EventHandler<HMHomeAccessoryEventArgs> DidAddAccessory;
	public event System.EventHandler<HMHomeActionSetEventArgs> DidAddActionSet;
	public event System.EventHandler<HMHomeRoomEventArgs> DidAddRoom;
	public event System.EventHandler<HMHomeRoomZoneEventArgs> DidAddRoomToZone;
	public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidAddService;
	public event System.EventHandler<HMHomeServiceGroupEventArgs> DidAddServiceGroup;
	public event System.EventHandler<HMHomeTriggerEventArgs> DidAddTrigger;
	public event System.EventHandler<HMHomeUserEventArgs> DidAddUser;
	public event System.EventHandler<HMHomeZoneEventArgs> DidAddZone;
	public event System.EventHandler<HMHomeErrorAccessoryEventArgs> DidEncounterError;
	public event System.EventHandler<HMHomeAccessoryEventArgs> DidRemoveAccessory;
	public event System.EventHandler<HMHomeActionSetEventArgs> DidRemoveActionSet;
	public event System.EventHandler<HMHomeRoomEventArgs> DidRemoveRoom;
	public event System.EventHandler<HMHomeRoomZoneEventArgs> DidRemoveRoomFromZone;
	public event System.EventHandler<HMHomeServiceServiceGroupEventArgs> DidRemoveService;
	public event System.EventHandler<HMHomeServiceGroupEventArgs> DidRemoveServiceGroup;
	public event System.EventHandler<HMHomeTriggerEventArgs> DidRemoveTrigger;
	public event System.EventHandler<HMHomeUserEventArgs> DidRemoveUser;
	public event System.EventHandler<HMHomeZoneEventArgs> DidRemoveZone;
	public event System.EventHandler<HMHomeAccessoryEventArgs> DidUnblockAccessory;
	public event System.EventHandler<HMHomeActionSetEventArgs> DidUpdateActionsForActionSet;
	public event System.EventHandler<HMHomeActionSetEventArgs> DidUpdateNameForActionSet;
	public event System.EventHandler DidUpdateNameForHome;
	public event System.EventHandler<HMHomeRoomEventArgs> DidUpdateNameForRoom;
	public event System.EventHandler<HMHomeServiceGroupEventArgs> DidUpdateNameForServiceGroup;
	public event System.EventHandler<HMHomeTriggerEventArgs> DidUpdateNameForTrigger;
	public event System.EventHandler<HMHomeZoneEventArgs> DidUpdateNameForZone;
	public event System.EventHandler<HMHomeRoomAccessoryEventArgs> DidUpdateRoom;
	public event System.EventHandler<HMHomeTriggerEventArgs> DidUpdateTrigger;
	// methods
	public virtual void AddAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddAccessoryAsync (HMAccessory accessory);
	public virtual void AddActionSet (string actionSetName, System.Action<HMActionSet,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMActionSet> AddActionSetAsync (string actionSetName);
	public virtual void AddRoom (string roomName, System.Action<HMRoom,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMRoom> AddRoomAsync (string roomName);
	public virtual void AddServiceGroup (string serviceGroupName, System.Action<HMServiceGroup,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMServiceGroup> AddServiceGroupAsync (string serviceGroupName);
	public virtual void AddTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddTriggerAsync (HMTrigger trigger);
	public virtual void AddUser (System.Action<HMUser,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMUser> AddUserAsync ();
	public virtual void AddZone (string zoneName, System.Action<HMZone,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMZone> AddZoneAsync (string zoneName);
	public virtual void AssignAccessory (HMAccessory accessory, HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AssignAccessoryAsync (HMAccessory accessory, HMRoom room);
	protected override void Dispose (bool disposing);
	public virtual void ExecuteActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task ExecuteActionSetAsync (HMActionSet actionSet);
	public virtual HMRoom GetRoomForEntireHome ();
	public HMService[] GetServices (HMServiceType serviceTypes);
	public virtual void RemoveAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveAccessoryAsync (HMAccessory accessory);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveActionSetAsync (HMActionSet actionSet);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveRoomAsync (HMRoom room);
	public virtual void RemoveServiceGroup (HMServiceGroup group, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveServiceGroupAsync (HMServiceGroup group);
	public virtual void RemoveTrigger (HMTrigger trigger, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveTriggerAsync (HMTrigger trigger);
	public virtual void RemoveUser (HMUser user, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveUserAsync (HMUser user);
	public virtual void RemoveZone (HMZone zone, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveZoneAsync (HMZone zone);
	public virtual void UnblockAccessory (HMAccessory accessory, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UnblockAccessoryAsync (HMAccessory accessory);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMHomeAccessoryEventArgs

```
public class HMHomeAccessoryEventArgs : System.EventArgs {
	// constructors
	public HMHomeAccessoryEventArgs (HMAccessory accessory);
	// properties
	public HMAccessory Accessory { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeActionSetEventArgs

```
public class HMHomeActionSetEventArgs : System.EventArgs {
	// constructors
	public HMHomeActionSetEventArgs (HMActionSet actionSet);
	// properties
	public HMActionSet ActionSet { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeDelegate

```
public class HMHomeDelegate : MonoTouch.Foundation.NSObject, IHMHomeDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMHomeDelegate ();
	public HMHomeDelegate (MonoTouch.Foundation.NSCoder coder);
	public HMHomeDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public HMHomeDelegate (System.IntPtr handle);
	// methods
	public virtual void DidAddAccessory (HMHome home, HMAccessory accessory);
	public virtual void DidAddActionSet (HMHome home, HMActionSet actionSet);
	public virtual void DidAddRoom (HMHome home, HMRoom room);
	public virtual void DidAddRoomToZone (HMHome home, HMRoom room, HMZone zone);
	public virtual void DidAddService (HMHome home, HMService service, HMServiceGroup group);
	public virtual void DidAddServiceGroup (HMHome home, HMServiceGroup group);
	public virtual void DidAddTrigger (HMHome home, HMTrigger trigger);
	public virtual void DidAddUser (HMHome home, HMUser user);
	public virtual void DidAddZone (HMHome home, HMZone zone);
	public virtual void DidEncounterError (HMHome home, MonoTouch.Foundation.NSError error, HMAccessory accessory);
	public virtual void DidRemoveAccessory (HMHome home, HMAccessory accessory);
	public virtual void DidRemoveActionSet (HMHome home, HMActionSet actionSet);
	public virtual void DidRemoveRoom (HMHome home, HMRoom room);
	public virtual void DidRemoveRoomFromZone (HMHome home, HMRoom room, HMZone zone);
	public virtual void DidRemoveService (HMHome home, HMService service, HMServiceGroup group);
	public virtual void DidRemoveServiceGroup (HMHome home, HMServiceGroup group);
	public virtual void DidRemoveTrigger (HMHome home, HMTrigger trigger);
	public virtual void DidRemoveUser (HMHome home, HMUser user);
	public virtual void DidRemoveZone (HMHome home, HMZone zone);
	public virtual void DidUnblockAccessory (HMHome home, HMAccessory accessory);
	public virtual void DidUpdateActionsForActionSet (HMHome home, HMActionSet actionSet);
	public virtual void DidUpdateNameForActionSet (HMHome home, HMActionSet actionSet);
	public virtual void DidUpdateNameForHome (HMHome home);
	public virtual void DidUpdateNameForRoom (HMHome home, HMRoom room);
	public virtual void DidUpdateNameForServiceGroup (HMHome home, HMServiceGroup group);
	public virtual void DidUpdateNameForTrigger (HMHome home, HMTrigger trigger);
	public virtual void DidUpdateNameForZone (HMHome home, HMZone zone);
	public virtual void DidUpdateRoom (HMHome home, HMRoom room, HMAccessory accessory);
	public virtual void DidUpdateTrigger (HMHome home, HMTrigger trigger);
}
```

### New Type MonoTouch.HomeKit.HMHomeDelegate_Extensions

```
public static class HMHomeDelegate_Extensions {
	// methods
	public static void DidAddAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);
	public static void DidAddActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);
	public static void DidAddRoom (IHMHomeDelegate This, HMHome home, HMRoom room);
	public static void DidAddRoomToZone (IHMHomeDelegate This, HMHome home, HMRoom room, HMZone zone);
	public static void DidAddService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);
	public static void DidAddServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
	public static void DidAddTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);
	public static void DidAddUser (IHMHomeDelegate This, HMHome home, HMUser user);
	public static void DidAddZone (IHMHomeDelegate This, HMHome home, HMZone zone);
	public static void DidEncounterError (IHMHomeDelegate This, HMHome home, MonoTouch.Foundation.NSError error, HMAccessory accessory);
	public static void DidRemoveAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);
	public static void DidRemoveActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);
	public static void DidRemoveRoom (IHMHomeDelegate This, HMHome home, HMRoom room);
	public static void DidRemoveRoomFromZone (IHMHomeDelegate This, HMHome home, HMRoom room, HMZone zone);
	public static void DidRemoveService (IHMHomeDelegate This, HMHome home, HMService service, HMServiceGroup group);
	public static void DidRemoveServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
	public static void DidRemoveTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);
	public static void DidRemoveUser (IHMHomeDelegate This, HMHome home, HMUser user);
	public static void DidRemoveZone (IHMHomeDelegate This, HMHome home, HMZone zone);
	public static void DidUnblockAccessory (IHMHomeDelegate This, HMHome home, HMAccessory accessory);
	public static void DidUpdateActionsForActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);
	public static void DidUpdateNameForActionSet (IHMHomeDelegate This, HMHome home, HMActionSet actionSet);
	public static void DidUpdateNameForHome (IHMHomeDelegate This, HMHome home);
	public static void DidUpdateNameForRoom (IHMHomeDelegate This, HMHome home, HMRoom room);
	public static void DidUpdateNameForServiceGroup (IHMHomeDelegate This, HMHome home, HMServiceGroup group);
	public static void DidUpdateNameForTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);
	public static void DidUpdateNameForZone (IHMHomeDelegate This, HMHome home, HMZone zone);
	public static void DidUpdateRoom (IHMHomeDelegate This, HMHome home, HMRoom room, HMAccessory accessory);
	public static void DidUpdateTrigger (IHMHomeDelegate This, HMHome home, HMTrigger trigger);
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

### New Type MonoTouch.HomeKit.HMHomeManager

```
public class HMHomeManager : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMHomeManager ();
	public HMHomeManager (MonoTouch.Foundation.NSCoder coder);
	public HMHomeManager (MonoTouch.Foundation.NSObjectFlag t);
	public HMHomeManager (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public HMHomeManagerDelegate Delegate { get; set; }
	public virtual HMHome[] Homes { get; }
	public virtual HMHome PrimaryHome { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler<HMHomeManagerEventArgs> DidAddHome;
	public event System.EventHandler<HMHomeManagerEventArgs> DidRemoveHome;
	public event System.EventHandler DidUpdateHomes;
	public event System.EventHandler DidUpdatePrimaryHome;
	// methods
	public virtual void AddHome (string homeName, System.Action<HMHome,MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task<HMHome> AddHomeAsync (string homeName);
	protected override void Dispose (bool disposing);
	public virtual void RemoveHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveHomeAsync (HMHome home);
	public virtual void UpdatePrimaryHome (HMHome home, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdatePrimaryHomeAsync (HMHome home);
}
```

### New Type MonoTouch.HomeKit.HMHomeManagerDelegate

```
public class HMHomeManagerDelegate : MonoTouch.Foundation.NSObject, IHMHomeManagerDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMHomeManagerDelegate ();
	public HMHomeManagerDelegate (MonoTouch.Foundation.NSCoder coder);
	public HMHomeManagerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public HMHomeManagerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidAddHome (HMHomeManager manager, HMHome home);
	public virtual void DidRemoveHome (HMHomeManager manager, HMHome home);
	public virtual void DidUpdateHomes (HMHomeManager manager);
	public virtual void DidUpdatePrimaryHome (HMHomeManager manager);
}
```

### New Type MonoTouch.HomeKit.HMHomeManagerDelegate_Extensions

```
public static class HMHomeManagerDelegate_Extensions {
	// methods
	public static void DidAddHome (IHMHomeManagerDelegate This, HMHomeManager manager, HMHome home);
	public static void DidRemoveHome (IHMHomeManagerDelegate This, HMHomeManager manager, HMHome home);
	public static void DidUpdateHomes (IHMHomeManagerDelegate This, HMHomeManager manager);
	public static void DidUpdatePrimaryHome (IHMHomeManagerDelegate This, HMHomeManager manager);
}
```

### New Type MonoTouch.HomeKit.HMHomeManagerEventArgs

```
public class HMHomeManagerEventArgs : System.EventArgs {
	// constructors
	public HMHomeManagerEventArgs (HMHome home);
	// properties
	public HMHome Home { get; set; }
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

### New Type MonoTouch.HomeKit.HMHomeRoomEventArgs

```
public class HMHomeRoomEventArgs : System.EventArgs {
	// constructors
	public HMHomeRoomEventArgs (HMRoom room);
	// properties
	public HMRoom Room { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeRoomZoneEventArgs

```
public class HMHomeRoomZoneEventArgs : System.EventArgs {
	// constructors
	public HMHomeRoomZoneEventArgs (HMRoom room, HMZone zone);
	// properties
	public HMRoom Room { get; set; }
	public HMZone Zone { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeServiceGroupEventArgs

```
public class HMHomeServiceGroupEventArgs : System.EventArgs {
	// constructors
	public HMHomeServiceGroupEventArgs (HMServiceGroup group);
	// properties
	public HMServiceGroup Group { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeServiceServiceGroupEventArgs

```
public class HMHomeServiceServiceGroupEventArgs : System.EventArgs {
	// constructors
	public HMHomeServiceServiceGroupEventArgs (HMService service, HMServiceGroup group);
	// properties
	public HMServiceGroup Group { get; set; }
	public HMService Service { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeTriggerEventArgs

```
public class HMHomeTriggerEventArgs : System.EventArgs {
	// constructors
	public HMHomeTriggerEventArgs (HMTrigger trigger);
	// properties
	public HMTrigger Trigger { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeUserEventArgs

```
public class HMHomeUserEventArgs : System.EventArgs {
	// constructors
	public HMHomeUserEventArgs (HMUser user);
	// properties
	public HMUser User { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMHomeZoneEventArgs

```
public class HMHomeZoneEventArgs : System.EventArgs {
	// constructors
	public HMHomeZoneEventArgs (HMZone zone);
	// properties
	public HMZone Zone { get; set; }
}
```

### New Type MonoTouch.HomeKit.HMRoom

```
public class HMRoom : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMRoom (MonoTouch.Foundation.NSCoder coder);
	public HMRoom (MonoTouch.Foundation.NSObjectFlag t);
	public HMRoom (System.IntPtr handle);
	// properties
	public virtual HMAccessory[] Accessories { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMService

```
public class HMService : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMService ();
	public HMService (MonoTouch.Foundation.NSCoder coder);
	public HMService (MonoTouch.Foundation.NSObjectFlag t);
	public HMService (System.IntPtr handle);
	// properties
	public virtual HMAccessory Accessory { get; }
	public virtual string AssociatedServiceType { get; }
	public virtual HMCharacteristic[] Characteristics { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public HMServiceType ServiceType { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void UpdateAssociatedServiceType (string serviceType, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateAssociatedServiceTypeAsync (string serviceType);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMServiceGroup

```
public class HMServiceGroup : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMServiceGroup (MonoTouch.Foundation.NSCoder coder);
	public HMServiceGroup (MonoTouch.Foundation.NSObjectFlag t);
	public HMServiceGroup (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public virtual HMService[] Services { get; }
	// methods
	public virtual void AddService (HMService service, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddServiceAsync (HMService service);
	protected override void Dispose (bool disposing);
	public virtual void RemoveService (HMService service, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveServiceAsync (HMService service);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMServiceType

```
[Serializable]
[Flags]
public enum HMServiceType {
	AccessoryInformation = 5,
	Fan = 6,
	GarageDoorOpener = 4,
	LightBulb = 1,
	LockManagement = 9,
	LockMechanism = 8,
	None = 0,
	Outlet = 7,
	Switch = 2,
	Thermostat = 3,
}
```

### New Type MonoTouch.HomeKit.HMTimerTrigger

```
public class HMTimerTrigger : MonoTouch.HomeKit.HMTrigger, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMTimerTrigger (MonoTouch.Foundation.NSCoder coder);
	public HMTimerTrigger (MonoTouch.Foundation.NSObjectFlag t);
	public HMTimerTrigger (System.IntPtr handle);
	public HMTimerTrigger (string name, MonoTouch.Foundation.NSDate fireDate, MonoTouch.Foundation.NSTimeZone timeZone, MonoTouch.Foundation.NSDateComponents recurrence, MonoTouch.Foundation.NSCalendar recurrenceCalendar);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate FireDate { get; }
	public virtual MonoTouch.Foundation.NSDateComponents Recurrence { get; }
	public virtual MonoTouch.Foundation.NSCalendar RecurrenceCalendar { get; }
	public virtual MonoTouch.Foundation.NSTimeZone TimeZone { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void UpdateFireDate (MonoTouch.Foundation.NSDate fireDate, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateFireDateAsync (MonoTouch.Foundation.NSDate fireDate);
	public virtual void UpdateRecurrence (MonoTouch.Foundation.NSDateComponents recurrence, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateRecurrenceAsync (MonoTouch.Foundation.NSDateComponents recurrence);
	public virtual void UpdateTimeZone (MonoTouch.Foundation.NSTimeZone timeZone, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateTimeZoneAsync (MonoTouch.Foundation.NSTimeZone timeZone);
}
```

### New Type MonoTouch.HomeKit.HMTrigger

```
public class HMTrigger : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMTrigger (MonoTouch.Foundation.NSCoder coder);
	public HMTrigger (MonoTouch.Foundation.NSObjectFlag t);
	public HMTrigger (System.IntPtr handle);
	// properties
	public virtual HMActionSet[] ActionSets { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; }
	public virtual MonoTouch.Foundation.NSDate LastFireDate { get; }
	public virtual string Name { get; }
	// methods
	public virtual void AddActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddActionSetAsync (HMActionSet actionSet);
	protected override void Dispose (bool disposing);
	public virtual void Enable (bool enable, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task EnableAsync (bool enable);
	public virtual void RemoveActionSet (HMActionSet actionSet, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveActionSetAsync (HMActionSet actionSet);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.HMUser

```
public class HMUser : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMUser (MonoTouch.Foundation.NSCoder coder);
	public HMUser (MonoTouch.Foundation.NSObjectFlag t);
	public HMUser (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
}
```

### New Type MonoTouch.HomeKit.HMZone

```
public class HMZone : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public HMZone (MonoTouch.Foundation.NSCoder coder);
	public HMZone (MonoTouch.Foundation.NSObjectFlag t);
	public HMZone (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Name { get; }
	public virtual HMRoom[] Rooms { get; }
	// methods
	public virtual void AddRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task AddRoomAsync (HMRoom room);
	protected override void Dispose (bool disposing);
	public virtual void RemoveRoom (HMRoom room, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task RemoveRoomAsync (HMRoom room);
	public virtual void UpdateName (string name, System.Action<MonoTouch.Foundation.NSError> completion);
	public virtual System.Threading.Tasks.Task UpdateNameAsync (string name);
}
```

### New Type MonoTouch.HomeKit.IHMAccessoryBrowserDelegate

```
public interface IHMAccessoryBrowserDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.HomeKit.IHMAccessoryDelegate

```
public interface IHMAccessoryDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.HomeKit.IHMHomeDelegate

```
public interface IHMHomeDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.HomeKit.IHMHomeManagerDelegate

```
public interface IHMHomeManagerDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## New Namespace MonoTouch.LocalAuthentication

### New Type MonoTouch.LocalAuthentication.LAContext

```
public class LAContext : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public LAContext ();
	public LAContext (MonoTouch.Foundation.NSCoder coder);
	public LAContext (MonoTouch.Foundation.NSObjectFlag t);
	public LAContext (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedFallbackTitle { get; set; }
	// methods
	public virtual bool CanEvaluatePolicy (LAPolicy policy, out MonoTouch.Foundation.NSError error);
	public virtual void EvaluatePolicy (LAPolicy policy, string localizedReason, LAContextReplyHandler reply);
	public virtual System.Threading.Tasks.Task<bool> EvaluatePolicyAsync (LAPolicy policy, string localizedReason);
}
```

### New Type MonoTouch.LocalAuthentication.LAContextReplyHandler

```
public sealed delegate LAContextReplyHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public LAContextReplyHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool success, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool success, MonoTouch.Foundation.NSError error);
}
```

### New Type MonoTouch.LocalAuthentication.LAPolicy

```
[Serializable]
public enum LAPolicy {
	DeviceOwnerAuthenticationWithBiometrics = 1,
}
```

### New Type MonoTouch.LocalAuthentication.LAStatus

```
[Serializable]
public enum LAStatus {
	AuthenticationFailed = -1,
	PasscodeNotSet = -5,
	Success = 0,
	SystemCancel = -4,
	TouchIDNotAvailable = -6,
	TouchIDNotEnrolled = -7,
	UserCancel = -2,
	UserFallback = -3,
}
```

## New Namespace MonoTouch.Metal

### New Type MonoTouch.Metal.IMTLBlitCommandEncoder

```
public interface IMTLBlitCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLCommandEncoder {
	// methods
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceBytesPerRow, uint sourceBytesPerImage, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, IMTLBuffer destinationBuffer, uint destinationOffset, uint size);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinatinBytesPerRow, uint destinationBytesPerImage);
	public virtual void FillBuffer (IMTLBuffer buffer, MonoTouch.Foundation.NSRange range, byte value);
	public virtual void GenerateMipmapsForTexture (IMTLTexture texture);
}
```

### New Type MonoTouch.Metal.IMTLBuffer

```
public interface IMTLBuffer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLResource {
	// properties
	public virtual System.IntPtr Contents { get; }
	public virtual uint Length { get; }
	// methods
	public virtual IMTLTexture CreateTexture (MTLTextureDescriptor descriptor, uint offset, uint bytesPerRow);
}
```

### New Type MonoTouch.Metal.IMTLCommandBuffer

```
public interface IMTLCommandBuffer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLBlitCommandEncoder BlitCommandEncoder { get; }
	public virtual IMTLCommandQueue CommandQueue { get; }
	public virtual IMTLComputeCommandEncoder ComputeCommandEncoder { get; }
	public virtual IMTLDevice Device { get; }
	public virtual MonoTouch.Foundation.NSError Error { get; }
	public virtual string Label { get; set; }
	public virtual bool RetainedReferences { get; }
	public virtual MTLCommandBufferStatus Status { get; }
	// methods
	public virtual void AddCompletedHandler (System.Action<IMTLCommandBuffer> block);
	public virtual void AddScheduledHandler (System.Action<IMTLCommandBuffer> block);
	public virtual void Commit ();
	public virtual void Enqueue ();
	public virtual void WaitUntilCompleted ();
	public virtual void WaitUntilScheduled ();
}
```

### New Type MonoTouch.Metal.IMTLCommandEncoder

```
public interface IMTLCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual void EndEncoding ();
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
}
```

### New Type MonoTouch.Metal.IMTLCommandQueue

```
public interface IMTLCommandQueue : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLCommandBuffer CommandBuffer ();
	public virtual IMTLCommandBuffer CommandBufferWithUnretainedReferences ();
	public virtual void InsertDebugCaptureBoundary ();
}
```

### New Type MonoTouch.Metal.IMTLComputeCommandEncoder

```
public interface IMTLComputeCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLCommandEncoder {
	// methods
	public virtual void SetBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetComputePipelineState (IMTLComputePipelineState state);
	public virtual void SetSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetTexture (IMTLTexture texture, uint index);
	public virtual void SetThreadgroupMemoryLength (uint length, uint index);
	public virtual void SispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
}
```

### New Type MonoTouch.Metal.IMTLComputePipelineState

```
public interface IMTLComputePipelineState : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual uint MaxTotalThreadsPerThreadgroup { get; }
	public virtual uint ThreadExecutionWidth { get; }
}
```

### New Type MonoTouch.Metal.IMTLDepthStencilState

```
public interface IMTLDepthStencilState : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.Metal.IMTLDevice

```
public interface IMTLDevice : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual string Name { get; }
	// methods
	public virtual IMTLBuffer CreateBuffer (System.IntPtr pointer, uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBuffer (uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBufferNoCopy (System.IntPtr pointer, uint length, MTLResourceOptions options, MTLDeallocator deallocator);
	public virtual IMTLCommandQueue CreateCommandQueue ();
	public virtual IMTLCommandQueue CreateCommandQueue (uint maxCommandBufferCount);
	public virtual void CreateComputePipelineState (IMTLFunction computeFunction, MTLPipelineOption options, System.Action<IMTLComputePipelineState,MonoTouch.Metal.MTLComputePipelineReflection,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, out MonoTouch.Foundation.NSError error);
	public virtual IMTLLibrary CreateDefaultLibrary ();
	public virtual IMTLDepthStencilState CreateDepthStencilState (MTLDepthStencilDescriptor descriptor);
	public virtual void CreateLibrary (string source, MTLCompileOptions options, System.Action<IMTLLibrary,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLLibrary CreateLibrary (string source, MTLCompileOptions options, out MonoTouch.Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (MonoTouch.Foundation.NSObject data, out MonoTouch.Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (string filepath, out MonoTouch.Foundation.NSError error);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, System.Action<IMTLRenderPipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, out MonoTouch.Foundation.NSError error);
	public virtual IMTLSamplerState CreateSamplerState (MTLSamplerDescriptor descriptor);
	public virtual IMTLTexture CreateTexture (MTLTextureDescriptor descriptor);
	public virtual bool SupportsFeatureSet (MTLFeatureSet featureSet);
}
```

### New Type MonoTouch.Metal.IMTLDrawable

```
public interface IMTLDrawable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Present ();
	public virtual void Present (double presentationTime);
}
```

### New Type MonoTouch.Metal.IMTLFunction

```
public interface IMTLFunction : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual MTLFunctionType FunctionType { get; }
	public virtual string Name { get; }
	public virtual MTLVertexAttribute[] VertexAttributes { get; }
}
```

### New Type MonoTouch.Metal.IMTLLibrary

```
public interface IMTLLibrary : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string[] FunctionNames { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLFunction CreateFunction (string functionName);
}
```

### New Type MonoTouch.Metal.IMTLParallelRenderCommandEncoder

```
public interface IMTLParallelRenderCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLCommandEncoder {
	// methods
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder ();
}
```

### New Type MonoTouch.Metal.IMTLRenderCommandEncoder

```
public interface IMTLRenderCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLCommandEncoder {
	// methods
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset);
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset, uint instanceCount);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount, uint instanceCount);
	public virtual void SetBlendColor (float red, float green, float blue, float alpha);
	public virtual void SetCullMode (MTLCullMode cullMode);
	public virtual void SetDepthBias (float depthBias, float slopeScale, float clamp);
	public virtual void SetDepthStencilState (IMTLDepthStencilState depthStencilState);
	public virtual void SetFragmentBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetFragmentBuffers (IMTLBuffer buffers, System.IntPtr IntPtrOffsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentTexture (IMTLTexture texture, uint index);
	public virtual void SetFragmentTextures (IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
	public virtual void SetFrontFacingWinding (MTLWinding frontFacingWinding);
	public virtual void SetRenderPipelineState (IMTLRenderPipelineState pipelineState);
	public virtual void SetScissorRect (MTLScissorRect rect);
	public virtual void SetStencilReferenceValue (uint referenceValue);
	public virtual void SetTriangleFillMode (MTLTriangleFillMode fillMode);
	public virtual void SetVertexBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetVertexBuffers (IMTLBuffer[] buffers, System.IntPtr uintArrayPtrOffsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetVertexSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexTexture (IMTLTexture texture, uint index);
	public virtual void SetViewport (MTLViewport viewport);
	public virtual void SetVisibilityResultMode (MTLVisibilityResultMode mode, uint offset);
}
```

### New Type MonoTouch.Metal.IMTLRenderPipelineState

```
public interface IMTLRenderPipelineState : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
```

### New Type MonoTouch.Metal.IMTLResource

```
public interface IMTLResource : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual MTLCpuCacheMode CpuCacheMode { get; }
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);
}
```

### New Type MonoTouch.Metal.IMTLSamplerState

```
public interface IMTLSamplerState : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
```

### New Type MonoTouch.Metal.IMTLTexture

```
public interface IMTLTexture : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLResource {
	// properties
	public virtual uint ArrayLength { get; }
	public virtual uint Depth { get; }
	public virtual bool FramebufferOnly { get; }
	public virtual uint Height { get; }
	public virtual uint MipmapLevelCount { get; }
	public virtual MTLPixelFormat PixelFormat { get; }
	public virtual IMTLResource RootResource { get; }
	public virtual uint SampleCount { get; }
	public virtual MTLTextureType TextureType { get; }
	public virtual uint Width { get; }
	// methods
	public virtual IMTLTexture CreateTextureView (MTLPixelFormat pixelFormat);
}
```

### New Type MonoTouch.Metal.MTLArgument

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

### New Type MonoTouch.Metal.MTLArgumentType

```
[Serializable]
public enum MTLArgumentType {
	Buffer = 0,
	Sampler = 3,
	Texture = 2,
	ThreadgroupMemory = 1,
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

### New Type MonoTouch.Metal.MTLBlendFactor

```
[Serializable]
public enum MTLBlendFactor {
	BlendAlpha = 13,
	BlendColor = 11,
	DestinationAlpha = 8,
	DestinationColor = 6,
	One = 1,
	OneMinusBlendAlpha = 14,
	OneMinusBlendColor = 12,
	OneMinusDestinationAlpha = 9,
	OneMinusDestinationColor = 7,
	OneMinusSourceAlpha = 5,
	OneMinusSourceColor = 3,
	SourceAlpha = 4,
	SourceAlphaSaturated = 10,
	SourceColor = 2,
	Zero = 0,
}
```

### New Type MonoTouch.Metal.MTLBlendOperation

```
[Serializable]
public enum MTLBlendOperation {
	Add = 0,
	Max = 4,
	Min = 3,
	ReverseSubtract = 2,
	Subtract = 1,
}
```

### New Type MonoTouch.Metal.MTLBlitCommandEncoder_Extensions

```
public static class MTLBlitCommandEncoder_Extensions {
}
```

### New Type MonoTouch.Metal.MTLBuffer_Extensions

```
public static class MTLBuffer_Extensions {
}
```

### New Type MonoTouch.Metal.MTLClearColor

```
public struct MTLClearColor {
	// constructors
	public MTLClearColor (double red, double green, double blue, double alpha);
	// fields
	public double Alpha;
	public double Blue;
	public double Green;
	public double Red;
}
```

### New Type MonoTouch.Metal.MTLClearValue

```
public struct MTLClearValue {
	// constructors
	public MTLClearValue (MTLClearColor color);
	public MTLClearValue (double depth);
	public MTLClearValue (ulong stencil);
	// fields
	public MTLClearColor Color;
	public double Depth;
	public ulong Stencil;
}
```

### New Type MonoTouch.Metal.MTLColorWriteMask

```
[Serializable]
[Flags]
public enum MTLColorWriteMask {
	All = 15,
	Alpha = 1,
	Blue = 2,
	Green = 4,
	None = 0,
	Red = 8,
}
```

### New Type MonoTouch.Metal.MTLCommandBuffer_Extensions

```
public static class MTLCommandBuffer_Extensions {
	// methods
	public static IMTLParallelRenderCommandEncoder CreateParallelRenderCommandEncoder (IMTLCommandBuffer This, MTLRenderPassDescriptor renderPassDescriptor);
	public static IMTLRenderCommandEncoder CreateRenderCommandEncoder (IMTLCommandBuffer This, MTLRenderPassDescriptor renderPassDescriptor);
	public static void PresentDrawable (IMTLCommandBuffer This, IMTLDrawable drawable);
	public static void PresentDrawable (IMTLCommandBuffer This, IMTLDrawable drawable, double presentationTime);
}
```

### New Type MonoTouch.Metal.MTLCommandBufferError

```
[Serializable]
public enum MTLCommandBufferError {
	Blacklisted = 4,
	Internal = 1,
	InvalidResource = 9,
	None = 0,
	NotPermitted = 7,
	OutOfMemory = 8,
	PageFault = 3,
	Timeout = 2,
}
```

### New Type MonoTouch.Metal.MTLCommandBufferStatus

```
[Serializable]
public enum MTLCommandBufferStatus {
	Committed = 2,
	Completed = 4,
	Enqueued = 1,
	Error = 5,
	NotEnqueued = 0,
	Scheduled = 3,
}
```

### New Type MonoTouch.Metal.MTLCommandEncoder_Extensions

```
public static class MTLCommandEncoder_Extensions {
}
```

### New Type MonoTouch.Metal.MTLCommandQueue_Extensions

```
public static class MTLCommandQueue_Extensions {
}
```

### New Type MonoTouch.Metal.MTLCompareFunction

```
[Serializable]
public enum MTLCompareFunction {
	Always = 7,
	Equal = 2,
	Greater = 4,
	GreaterEqual = 6,
	Less = 1,
	LessEqual = 3,
	Never = 0,
	NotEqual = 5,
}
```

### New Type MonoTouch.Metal.MTLCompileOptions

```
public class MTLCompileOptions : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLCompileOptions ();
	public MTLCompileOptions (MonoTouch.Foundation.NSCoder coder);
	public MTLCompileOptions (MonoTouch.Foundation.NSObjectFlag t);
	public MTLCompileOptions (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool FastMathEnabled { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary PreprocessorMacros { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLComputeCommandEncoder_Extensions

```
public static class MTLComputeCommandEncoder_Extensions {
	// methods
	public static void SetBuffers (IMTLComputeCommandEncoder This, IMTLBuffer[] buffers, System.IntPtr offsets, MonoTouch.Foundation.NSRange range);
	public static void SetSamplerStates (IMTLComputeCommandEncoder This, IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public static void SetSamplerStates (IMTLComputeCommandEncoder This, IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public static void SetTextures (IMTLComputeCommandEncoder This, IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
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

### New Type MonoTouch.Metal.MTLComputePipelineState_Extensions

```
public static class MTLComputePipelineState_Extensions {
}
```

### New Type MonoTouch.Metal.MTLCpuCacheMode

```
[Serializable]
public enum MTLCpuCacheMode {
	DefaultCache = 0,
	WriteCombined = 1,
}
```

### New Type MonoTouch.Metal.MTLCullMode

```
[Serializable]
public enum MTLCullMode {
	Back = 2,
	Front = 1,
	None = 0,
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

### New Type MonoTouch.Metal.MTLDeallocator

```
public sealed delegate MTLDeallocator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public MTLDeallocator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr pointer, uint lenght, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr pointer, uint lenght);
}
```

### New Type MonoTouch.Metal.MTLDepthStencilDescriptor

```
public class MTLDepthStencilDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLDepthStencilDescriptor ();
	public MTLDepthStencilDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLDepthStencilDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLDepthStencilDescriptor (System.IntPtr handle);
	// properties
	public virtual MTLStencilDescriptor BackFaceStencil { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLCompareFunction DepthCompareFunction { get; set; }
	public virtual bool DepthWriteEnabled { get; set; }
	public virtual MTLStencilDescriptor FrontFaceStencil { get; set; }
	public virtual string Label { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLDepthStencilState_Extensions

```
public static class MTLDepthStencilState_Extensions {
}
```

### New Type MonoTouch.Metal.MTLDevice

```
public static class MTLDevice {
	// properties
	public static IMTLDevice SystemDefault { get; }
}
```

### New Type MonoTouch.Metal.MTLDevice_Extensions

```
public static class MTLDevice_Extensions {
	// methods
	public static IMTLBuffer CreateBuffer<T> (IMTLDevice This, T[] data, MTLResourceOptions options);
	public static IMTLBuffer CreateBufferNoCopy<T> (IMTLDevice This, T[] data, MTLResourceOptions options, MTLDeallocator deallocator);
	public static IMTLComputePipelineState CreateComputePipelineState (IMTLDevice This, IMTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out MonoTouch.Foundation.NSError error);
	public static void CreateComputePipelineState (IMTLDevice This, IMTLFunction computeFunction, System.Action<IMTLComputePipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public static IMTLRenderPipelineState CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out MonoTouch.Foundation.NSError error);
	public static void CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action<IMTLRenderPipelineState,MonoTouch.Metal.MTLRenderPipelineReflection,MonoTouch.Foundation.NSError> completionHandler);
}
```

### New Type MonoTouch.Metal.MTLDrawable

```
public abstract class MTLDrawable : MonoTouch.Foundation.NSObject, IMTLDrawable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLDrawable ();
	public MTLDrawable (MonoTouch.Foundation.NSCoder coder);
	public MTLDrawable (MonoTouch.Foundation.NSObjectFlag t);
	public MTLDrawable (System.IntPtr handle);
	// methods
	public virtual void Present ();
	public virtual void Present (double presentationTime);
}
```

### New Type MonoTouch.Metal.MTLDrawable_Extensions

```
public static class MTLDrawable_Extensions {
}
```

### New Type MonoTouch.Metal.MTLFeatureSet

```
[Serializable]
public enum MTLFeatureSet {
	iOS_GPUFamily1_v1 = 0,
	iOS_GPUFamily2_v1 = 1,
}
```

### New Type MonoTouch.Metal.MTLFunction_Extensions

```
public static class MTLFunction_Extensions {
}
```

### New Type MonoTouch.Metal.MTLFunctionType

```
[Serializable]
public enum MTLFunctionType {
	Fragment = 2,
	Kernel = 3,
	Vertex = 1,
}
```

### New Type MonoTouch.Metal.MTLIndexType

```
[Serializable]
public enum MTLIndexType {
	UInt16 = 0,
	UInt32 = 1,
}
```

### New Type MonoTouch.Metal.MTLLibrary_Extensions

```
public static class MTLLibrary_Extensions {
}
```

### New Type MonoTouch.Metal.MTLLibraryError

```
[Serializable]
public enum MTLLibraryError {
	CompileFailure = 3,
	CompileWarning = 4,
	Internal = 2,
	Unsupported = 1,
}
```

### New Type MonoTouch.Metal.MTLLoadAction

```
[Serializable]
public enum MTLLoadAction {
	Clear = 2,
	DontCare = 0,
	Load = 1,
}
```

### New Type MonoTouch.Metal.MTLOrigin

```
public struct MTLOrigin {
	// constructors
	public MTLOrigin (int x, int y, int z);
	// fields
	public int X;
	public int Y;
	public int Z;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.Metal.MTLParallelRenderCommandEncoder_Extensions

```
public static class MTLParallelRenderCommandEncoder_Extensions {
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

### New Type MonoTouch.Metal.MTLPixelFormat

```
[Serializable]
public enum MTLPixelFormat {
	A1BGR5Unorm = 41,
	A8Unorm = 1,
	ABGR4Unorm = 42,
	ASTC_10x10_LDR = 216,
	ASTC_10x10_sRGB = 198,
	ASTC_10x5_LDR = 213,
	ASTC_10x5_sRGB = 195,
	ASTC_10x6_LDR = 214,
	ASTC_10x6_sRGB = 196,
	ASTC_10x8_LDR = 215,
	ASTC_10x8_sRGB = 197,
	ASTC_12x10_LDR = 217,
	ASTC_12x10_sRGB = 199,
	ASTC_12x12_LDR = 218,
	ASTC_12x12_sRGB = 200,
	ASTC_4x4_LDR = 204,
	ASTC_4x4_sRGB = 186,
	ASTC_5x4_LDR = 205,
	ASTC_5x4_sRGB = 187,
	ASTC_5x5_LDR = 206,
	ASTC_5x5_sRGB = 188,
	ASTC_6x5_LDR = 207,
	ASTC_6x5_sRGB = 189,
	ASTC_6x6_LDR = 208,
	ASTC_6x6_sRGB = 190,
	ASTC_8x5_LDR = 210,
	ASTC_8x5_sRGB = 192,
	ASTC_8x6_LDR = 211,
	ASTC_8x6_sRGB = 193,
	ASTC_8x8_LDR = 212,
	ASTC_8x8_sRGB = 194,
	B5G6R5Unorm = 40,
	BGRA8Unorm = 80,
	BGRA8Unorm_sRGB = 81,
	BGRG422 = 241,
	Depth32Float = 252,
	EAC_R11Snorm = 172,
	EAC_R11Unorm = 170,
	EAC_RG11Snorm = 176,
	EAC_RG11Unorm = 174,
	EAC_RGBA8 = 178,
	EAC_RGBA8_sRGB = 179,
	ETC2_RGB8 = 180,
	ETC2_RGB8_sRGB = 181,
	ETC2_RGB8A1 = 182,
	ETC2_RGB8A1_sRGB = 183,
	GBGR422 = 240,
	Invalid = 0,
	PVRTC_RGB_2BPP = 160,
	PVRTC_RGB_2BPP_sRGB = 161,
	PVRTC_RGB_4BPP = 162,
	PVRTC_RGB_4BPP_sRGB = 163,
	PVRTC_RGBA_2BPP = 164,
	PVRTC_RGBA_2BPP_sRGB = 165,
	PVRTC_RGBA_4BPP = 166,
	PVRTC_RGBA_4BPP_sRGB = 167,
	R16Float = 25,
	R16Sint = 24,
	R16Snorm = 22,
	R16Uint = 23,
	R16Unorm = 20,
	R32Float = 55,
	R32Sint = 54,
	R32Uint = 53,
	R8Sint = 14,
	R8Snorm = 12,
	R8Uint = 13,
	R8Unorm = 10,
	R8Unorm_sRGB = 11,
	RG11B10Float = 92,
	RG16Float = 65,
	RG16Sint = 64,
	RG16Snorm = 62,
	RG16Uint = 63,
	RG16Unorm = 60,
	RG32Float = 105,
	RG32Sint = 104,
	RG32Uint = 103,
	RG8Sint = 34,
	RG8Snorm = 32,
	RG8Uint = 33,
	RG8Unorm = 30,
	RG8Unorm_sRGB = 31,
	RGB10A2Uint = 91,
	RGB10A2Unorm = 90,
	RGB9E5Float = 93,
	RGBA16Float = 115,
	RGBA16Sint = 114,
	RGBA16Snorm = 112,
	RGBA16Uint = 113,
	RGBA16Unorm = 110,
	RGBA32Float = 125,
	RGBA32Sint = 124,
	RGBA32Uint = 123,
	RGBA8Sint = 74,
	RGBA8Snorm = 72,
	RGBA8Uint = 73,
	RGBA8Unorm = 70,
	RGBA8Unorm_sRGB = 71,
	Stencil8 = 253,
}
```

### New Type MonoTouch.Metal.MTLPrimitiveType

```
[Serializable]
public enum MTLPrimitiveType {
	Line = 1,
	LineStrip = 2,
	Point = 0,
	Triangle = 3,
	TriangleStrip = 4,
}
```

### New Type MonoTouch.Metal.MTLPurgeableState

```
[Serializable]
public enum MTLPurgeableState {
	Empty = 4,
	KeepCurrent = 1,
	NonVolatile = 2,
	Volatile = 3,
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

### New Type MonoTouch.Metal.MTLRenderCommandEncoder_Extensions

```
public static class MTLRenderCommandEncoder_Extensions {
	// methods
	public static void SetVertexTextures (IMTLRenderCommandEncoder This, IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
}
```

### New Type MonoTouch.Metal.MTLRenderPassAttachmentDescriptor

```
public class MTLRenderPassAttachmentDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassAttachmentDescriptor ();
	public MTLRenderPassAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassAttachmentDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint DepthPlane { get; set; }
	public virtual uint Level { get; set; }
	public virtual MTLLoadAction LoadAction { get; set; }
	public virtual uint ResolveDepthPlane { get; set; }
	public virtual uint ResolveLevel { get; set; }
	public virtual uint ResolveSlice { get; set; }
	public virtual IMTLTexture ResolveTexture { get; set; }
	public virtual uint Slice { get; set; }
	public virtual MTLStoreAction StoreAction { get; set; }
	public virtual IMTLTexture Texture { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
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

### New Type MonoTouch.Metal.MTLRenderPassDescriptor

```
public class MTLRenderPassDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassDescriptor ();
	public MTLRenderPassDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLRenderPassColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLRenderPassDepthAttachmentDescriptor DepthAttachment { get; set; }
	public virtual MTLRenderPassStencilAttachmentDescriptor StencilAttachment { get; set; }
	public virtual IMTLBuffer VisibilityResultBuffer { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static MTLRenderPassDescriptor CreateRenderPassDescriptor ();
	protected override void Dispose (bool disposing);
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
	public MTLRenderPipelineColorAttachmentDescriptor Item { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineDescriptor

```
public class MTLRenderPipelineDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineDescriptor ();
	public MTLRenderPipelineDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineDescriptor (System.IntPtr handle);
	// properties
	public virtual bool AlphaToCoverageEnabled { get; set; }
	public virtual bool AlphaToOneEnabled { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLRenderPipelineColorAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLPixelFormat DepthAttachmentPixelFormat { get; set; }
	public virtual IMTLFunction FragmentFunction { get; set; }
	public virtual string Label { get; set; }
	public virtual bool RasterizationEnabled { get; set; }
	public virtual uint SampleCount { get; set; }
	public virtual MTLPixelFormat StencilAttachmentPixelFormat { get; set; }
	public virtual MTLVertexDescriptor VertexDescriptor { get; set; }
	public virtual IMTLFunction VertexFunction { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineError

```
[Serializable]
public enum MTLRenderPipelineError {
	Internal = 1,
	InvalidInput = 3,
	Unsupported = 2,
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

### New Type MonoTouch.Metal.MTLRenderPipelineState_Extensions

```
public static class MTLRenderPipelineState_Extensions {
}
```

### New Type MonoTouch.Metal.MTLResource_Extensions

```
public static class MTLResource_Extensions {
}
```

### New Type MonoTouch.Metal.MTLResourceOptions

```
[Serializable]
[Flags]
public enum MTLResourceOptions {
	CpuCacheModeDefault = 0,
	CpuCacheModeWriteCombined = 1,
}
```

### New Type MonoTouch.Metal.MTLSamplerAddressMode

```
[Serializable]
public enum MTLSamplerAddressMode {
	ClampToEdge = 0,
	ClampToZero = 4,
	MirrorRepeat = 3,
	Repeat = 2,
}
```

### New Type MonoTouch.Metal.MTLSamplerDescriptor

```
public class MTLSamplerDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLSamplerDescriptor ();
	public MTLSamplerDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLSamplerDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLSamplerDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Label { get; set; }
	public virtual float LodMaxClamp { get; set; }
	public virtual float LodMinClamp { get; set; }
	public virtual MTLSamplerMinMagFilter MagFilter { get; set; }
	public virtual uint MaxAnisotropy { get; set; }
	public virtual MTLSamplerMinMagFilter MinFilter { get; set; }
	public virtual MTLSamplerMipFilter MipFilter { get; set; }
	public virtual bool NormalizedCoordinates { get; set; }
	public virtual MTLSamplerAddressMode RAddressMode { get; set; }
	public virtual MTLSamplerAddressMode SAddressMode { get; set; }
	public virtual MTLSamplerAddressMode TAddressMode { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLSamplerMinMagFilter

```
[Serializable]
public enum MTLSamplerMinMagFilter {
	Linear = 1,
	Nearest = 0,
}
```

### New Type MonoTouch.Metal.MTLSamplerMipFilter

```
[Serializable]
public enum MTLSamplerMipFilter {
	Linear = 2,
	Nearest = 1,
	NotMipmapped = 0,
}
```

### New Type MonoTouch.Metal.MTLSamplerState_Extensions

```
public static class MTLSamplerState_Extensions {
}
```

### New Type MonoTouch.Metal.MTLScissorRect

```
public struct MTLScissorRect {
	// constructors
	public MTLScissorRect (uint x, uint y, uint width, uint height);
	// fields
	public uint Height;
	public uint Width;
	public uint X;
	public uint Y;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.Metal.MTLSize

```
public struct MTLSize {
	// constructors
	public MTLSize (int width, int height, int depth);
	// fields
	public int Depth;
	public int Height;
	public int Width;
}
```

### New Type MonoTouch.Metal.MTLStencilDescriptor

```
public class MTLStencilDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLStencilDescriptor ();
	public MTLStencilDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLStencilDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLStencilDescriptor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLStencilOperation DepthFailureOperation { get; set; }
	public virtual MTLStencilOperation DepthStencilPassOperation { get; set; }
	public virtual uint ReadMask { get; set; }
	public virtual MTLCompareFunction StencilCompareFunction { get; set; }
	public virtual MTLStencilOperation StencilFailureOperation { get; set; }
	public virtual uint WriteMask { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLStencilOperation

```
[Serializable]
public enum MTLStencilOperation {
	DecrementClamp = 4,
	DecrementWrap = 7,
	IncrementClamp = 3,
	IncrementWrap = 6,
	Invert = 5,
	Keep = 0,
	Replace = 2,
	Zero = 1,
}
```

### New Type MonoTouch.Metal.MTLStoreAction

```
[Serializable]
public enum MTLStoreAction {
	DontCare = 0,
	MultisampleResolve = 2,
	Store = 1,
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

### New Type MonoTouch.Metal.MTLTexture_Extensions

```
public static class MTLTexture_Extensions {
	// methods
	public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLRegion region, uint level, uint slice);
	public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, MTLRegion region, uint level);
	public static void ReplaceRegion (IMTLTexture This, MTLRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public static void ReplaceRegion (IMTLTexture This, MTLRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
}
```

### New Type MonoTouch.Metal.MTLTextureDescriptor

```
public class MTLTextureDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLTextureDescriptor ();
	public MTLTextureDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLTextureDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLTextureDescriptor (System.IntPtr handle);
	// properties
	public virtual uint ArrayLength { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint Depth { get; set; }
	public virtual uint Height { get; set; }
	public virtual uint MipmapLevelCount { get; set; }
	public virtual MTLPixelFormat PixelFormat { get; set; }
	public virtual MTLResourceOptions ResourceOptions { get; set; }
	public virtual uint SampleCount { get; set; }
	public virtual MTLTextureType TextureType { get; set; }
	public virtual uint Width { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static MTLTextureDescriptor CreateTexture2DDescriptor (MTLPixelFormat pixelFormat, uint width, uint height, bool mipmapped);
	public static MTLTextureDescriptor CreateTextureCubeDescriptor (MTLPixelFormat pixelFormat, uint size, bool mipmapped);
}
```

### New Type MonoTouch.Metal.MTLTextureType

```
[Serializable]
public enum MTLTextureType {
	k1D = 0,
	k1DArray = 1,
	k2D = 2,
	k2DArray = 3,
	k2DMultisample = 4,
	k3D = 6,
	kCube = 5,
}
```

### New Type MonoTouch.Metal.MTLTriangleFillMode

```
[Serializable]
public enum MTLTriangleFillMode {
	Fill = 0,
	Lines = 1,
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

### New Type MonoTouch.Metal.MTLVertexDescriptor

```
public class MTLVertexDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLVertexDescriptor ();
	public MTLVertexDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLVertexDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLVertexDescriptor (System.IntPtr handle);
	// properties
	public virtual MTLVertexAttributeDescriptorArray Attributes { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLVertexBufferLayoutDescriptorArray Layouts { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static MTLVertexDescriptor Create ();
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
```

### New Type MonoTouch.Metal.MTLVertexFormat

```
[Serializable]
public enum MTLVertexFormat {
	Char2 = 4,
	Char2Normalized = 10,
	Char3 = 5,
	Char3Normalized = 11,
	Char4 = 6,
	Char4Normalized = 12,
	Float = 28,
	Float2 = 29,
	Float3 = 30,
	Float4 = 31,
	Half2 = 25,
	Half3 = 26,
	Half4 = 27,
	Int = 32,
	Int1010102Normalized = 40,
	Int2 = 33,
	Int3 = 34,
	Int4 = 35,
	Invalid = 0,
	Short2 = 16,
	Short2Normalized = 22,
	Short3 = 17,
	Short3Normalized = 23,
	Short4 = 18,
	Short4Normalized = 24,
	UChar2 = 1,
	UChar2Normalized = 7,
	UChar3 = 2,
	UChar3Normalized = 8,
	UChar4 = 3,
	UChar4Normalized = 9,
	UInt = 36,
	UInt1010102Normalized = 41,
	UInt2 = 37,
	UInt3 = 38,
	UInt4 = 39,
	UShort2 = 13,
	UShort2Normalized = 19,
	UShort3 = 14,
	UShort3Normalized = 20,
	UShort4 = 15,
	UShort4Normalized = 21,
}
```

### New Type MonoTouch.Metal.MTLVertexStepFunction

```
[Serializable]
public enum MTLVertexStepFunction {
	Constant = 0,
	PerInstance = 2,
	PerVertex = 1,
}
```

### New Type MonoTouch.Metal.MTLViewport

```
public struct MTLViewport {
	// constructors
	public MTLViewport (double originX, double originY, double width, double height, double znear, double zfar);
	// fields
	public double Height;
	public double OriginX;
	public double OriginY;
	public double Width;
	public double ZFar;
	public double ZNear;
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.Metal.MTLVisibilityResultMode

```
[Serializable]
public enum MTLVisibilityResultMode {
	Boolean = 1,
	Disabled = 0,
}
```

### New Type MonoTouch.Metal.MTLWinding

```
[Serializable]
public enum MTLWinding {
	Clockwise = 0,
	CounterClockwise = 1,
}
```

## New Namespace MonoTouch.NotificationCenter

### New Type MonoTouch.NotificationCenter.INCWidgetProviding

```
public interface INCWidgetProviding : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.NotificationCenter.NCUpdateResult

```
[Serializable]
public enum NCUpdateResult {
	Failed = 2,
	NewData = 0,
	NoData = 1,
}
```

### New Type MonoTouch.NotificationCenter.NCWidgetController

```
public class NCWidgetController : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NCWidgetController (MonoTouch.Foundation.NSCoder coder);
	public NCWidgetController (MonoTouch.Foundation.NSObjectFlag t);
	public NCWidgetController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static NCWidgetController GetWidgetController ();
	public virtual void SetHasContent (bool flag, string bundleID);
}
```

### New Type MonoTouch.NotificationCenter.NCWidgetProviding

```
public class NCWidgetProviding : MonoTouch.Foundation.NSObject, INCWidgetProviding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NCWidgetProviding ();
	public NCWidgetProviding (MonoTouch.Foundation.NSCoder coder);
	public NCWidgetProviding (MonoTouch.Foundation.NSObjectFlag t);
	public NCWidgetProviding (System.IntPtr handle);
	// methods
	public virtual MonoTouch.UIKit.UIEdgeInsets GetWidgetMarginInsets (MonoTouch.UIKit.UIEdgeInsets defaultMarginInsets);
	public virtual void WidgetPerformUpdate (System.Action<NCUpdateResult> completionHandler);
}
```

### New Type MonoTouch.NotificationCenter.NCWidgetProviding_Extensions

```
public static class NCWidgetProviding_Extensions {
	// methods
	public static MonoTouch.UIKit.UIEdgeInsets GetWidgetMarginInsets (INCWidgetProviding This, MonoTouch.UIKit.UIEdgeInsets defaultMarginInsets);
	public static void WidgetPerformUpdate (INCWidgetProviding This, System.Action<NCUpdateResult> completionHandler);
}
```

### New Type MonoTouch.NotificationCenter.UIVibrancyEffect_NotificationCenter

```
public static class UIVibrancyEffect_NotificationCenter {
	// methods
	public static MonoTouch.UIKit.UIVibrancyEffect NotificationCenterVibrancyEffect (MonoTouch.UIKit.UIVibrancyEffect This);
}
```

## New Namespace MonoTouch.Photos

### New Type MonoTouch.Photos.IPHPhotoLibraryChangeObserver

```
public interface IPHPhotoLibraryChangeObserver : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.Photos.PHAdjustmentData

```
public class PHAdjustmentData : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHAdjustmentData ();
	public PHAdjustmentData (MonoTouch.Foundation.NSCoder coder);
	public PHAdjustmentData (MonoTouch.Foundation.NSObjectFlag t);
	public PHAdjustmentData (System.IntPtr handle);
	public PHAdjustmentData (string formatIdentifier, string formatVersion, MonoTouch.Foundation.NSData data);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData Data { get; }
	public virtual string FormatIdentifier { get; }
	public virtual string FormatVersion { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Photos.PHAsset

```
public class PHAsset : MonoTouch.Photos.PHObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHAsset ();
	public PHAsset (MonoTouch.Foundation.NSCoder coder);
	public PHAsset (MonoTouch.Foundation.NSObjectFlag t);
	public PHAsset (System.IntPtr handle);
	// properties
	public virtual string BurstIdentifier { get; }
	public virtual PHAssetBurstSelectionType BurstSelectionTypes { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate CreationDate { get; }
	public virtual double Duration { get; }
	public virtual bool Favorite { get; }
	public virtual bool Hidden { get; }
	public virtual MonoTouch.CoreLocation.CLLocation Location { get; }
	public virtual PHAssetMediaSubtype MediaSubtypes { get; }
	public virtual PHAssetMediaType MediaType { get; }
	public virtual MonoTouch.Foundation.NSDate ModificationDate { get; }
	public virtual uint PixelHeight { get; }
	public virtual uint PixelWidth { get; }
	public virtual bool RepresentsBurst { get; }
	// methods
	public virtual bool CanPerformEditOperation (PHAssetEditOperation editOperation);
	protected override void Dispose (bool disposing);
	public static PHFetchResult FetchAssets (PHAssetMediaType mediaType, PHFetchOptions options);
	public static PHFetchResult FetchAssets (string burstIdentifier, PHFetchOptions options);
	public static PHFetchResult FetchAssets (PHAssetCollection assetCollection, PHFetchOptions options);
	public static PHFetchResult FetchAssets (MonoTouch.Foundation.NSUrl[] assetUrls, PHFetchOptions options);
	public static PHFetchResult FetchAssets (PHFetchOptions options);
	public static PHFetchResult FetchAssetsUsingLocalIdentifiers (string[] identifiers, PHFetchOptions options);
	public static PHFetchResult FetchKeyAssets (PHAssetCollection assetCollection, PHFetchOptions options);
}
```

### New Type MonoTouch.Photos.PHAssetBurstSelectionType

```
[Serializable]
[Flags]
public enum PHAssetBurstSelectionType {
	AutoPick = 1,
	None = 0,
	UserPick = 2,
}
```

### New Type MonoTouch.Photos.PHAssetChangeRequest

```
public class PHAssetChangeRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHAssetChangeRequest ();
	public PHAssetChangeRequest (MonoTouch.Foundation.NSCoder coder);
	public PHAssetChangeRequest (MonoTouch.Foundation.NSObjectFlag t);
	public PHAssetChangeRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHContentEditingOutput ContentEditingOutput { get; set; }
	public virtual MonoTouch.Foundation.NSDate CreationDate { get; set; }
	public virtual bool Favorite { get; set; }
	public virtual bool Hidden { get; set; }
	public virtual MonoTouch.CoreLocation.CLLocation Location { get; set; }
	public virtual PHObjectPlaceholder PlaceholderForCreatedAsset { get; }
	// methods
	public static PHAssetChangeRequest ChangeRequest (PHAsset asset);
	public static void DeleteAssets (PHAsset[] assets);
	protected override void Dispose (bool disposing);
	public static PHAssetChangeRequest FromImage (MonoTouch.UIKit.UIImage image);
	public static PHAssetChangeRequest FromImage (MonoTouch.Foundation.NSUrl fileUrl);
	public static PHAssetChangeRequest FromVideo (MonoTouch.Foundation.NSUrl fileUrl);
	public virtual void RevertAssetContentToOriginal ();
}
```

### New Type MonoTouch.Photos.PHAssetCollection

```
public class PHAssetCollection : MonoTouch.Photos.PHCollection, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHAssetCollection ();
	public PHAssetCollection (MonoTouch.Foundation.NSCoder coder);
	public PHAssetCollection (MonoTouch.Foundation.NSObjectFlag t);
	public PHAssetCollection (System.IntPtr handle);
	// properties
	public virtual MonoTouch.CoreLocation.CLLocation ApproximateLocation { get; }
	public virtual PHAssetCollectionSubtype AssetCollectionSubtype { get; }
	public virtual PHAssetCollectionType AssetCollectionType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; }
	public virtual uint EstimatedAssetCount { get; }
	public virtual string[] LocalizedLocationNames { get; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static PHFetchResult FetchAssetCollections (string[] identifiers, PHFetchOptions options);
	public static PHFetchResult FetchAssetCollections (MonoTouch.Foundation.NSUrl[] assetGroupUrls, PHFetchOptions options);
	public static PHFetchResult FetchAssetCollections (PHAsset asset, PHAssetCollectionType type, PHFetchOptions options);
	public static PHFetchResult FetchAssetCollections (PHAssetCollectionType type, PHAssetCollectionSubtype subtype, PHFetchOptions options);
	public static PHFetchResult FetchMoments (PHFetchOptions options);
	public static PHFetchResult FetchMoments (PHCollectionList momentList, PHFetchOptions options);
	public static PHAssetCollection GetTransientAssetCollection (PHAsset[] assets, string title);
	public static PHAssetCollection GetTransientAssetCollection (PHFetchResult fetchResult, string title);
}
```

### New Type MonoTouch.Photos.PHAssetCollectionChangeRequest

```
public class PHAssetCollectionChangeRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHAssetCollectionChangeRequest (MonoTouch.Foundation.NSCoder coder);
	public PHAssetCollectionChangeRequest (MonoTouch.Foundation.NSObjectFlag t);
	public PHAssetCollectionChangeRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHObjectPlaceholder PlaceholderForCreatedAssetCollection { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual void AddAssets (PHObject[] assets);
	public static PHAssetCollectionChangeRequest ChangeRequest (PHAssetCollection assetCollection);
	public static PHAssetCollectionChangeRequest ChangeRequest (PHAssetCollection assetCollection, PHFetchResult assets);
	public static PHAssetCollectionChangeRequest CreateAssetCollection (string title);
	public static void DeleteAssetCollections (PHAssetCollection[] assetCollections);
	protected override void Dispose (bool disposing);
	public virtual void InsertAssets (PHObject[] assets, MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void MoveAssets (MonoTouch.Foundation.NSIndexSet fromIndexes, uint toIndex);
	public virtual void RemoveAssets (PHObject[] assets);
	public virtual void RemoveAssets (MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void ReplaceAssets (MonoTouch.Foundation.NSIndexSet indexes, PHObject[] assets);
}
```

### New Type MonoTouch.Photos.PHAssetCollectionSubtype

```
[Serializable]
public enum PHAssetCollectionSubtype {
	AlbumCloudShared = 101,
	AlbumImported = 6,
	AlbumRegular = 2,
	AlbumSyncedAlbum = 5,
	AlbumSyncedEvent = 3,
	AlbumSyncedFaces = 4,
	Any = 2147483647,
	SmartAlbumAllHidden = 205,
	SmartAlbumBursts = 207,
	SmartAlbumFavorites = 203,
	SmartAlbumGeneric = 200,
	SmartAlbumPanoramas = 201,
	SmartAlbumRecentlyAdded = 206,
	SmartAlbumSlomoVideos = 208,
	SmartAlbumTimelapses = 204,
	SmartAlbumVideos = 202,
}
```

### New Type MonoTouch.Photos.PHAssetCollectionType

```
[Serializable]
public enum PHAssetCollectionType {
	Album = 1,
	Moment = 3,
	SmartAlbum = 2,
}
```

### New Type MonoTouch.Photos.PHAssetContentEditingInputExtensions

```
public static class PHAssetContentEditingInputExtensions {
	// methods
	public static void CancelContentEditingInputRequest (PHAsset This, uint requestID);
	public static uint RequestContentEditingInput (PHAsset This, PHContentEditingInputRequestOptions options, PHContentEditingHandler completionHandler);
}
```

### New Type MonoTouch.Photos.PHAssetEditOperation

```
[Serializable]
public enum PHAssetEditOperation {
	Content = 2,
	Delete = 1,
	None = 0,
	Properties = 3,
}
```

### New Type MonoTouch.Photos.PHAssetImageProgressHandler

```
public sealed delegate PHAssetImageProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHAssetImageProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHAssetMediaSubtype

```
[Serializable]
[Flags]
public enum PHAssetMediaSubtype {
	None = 0,
	PhotoHDR = 2,
	PhotoPanorama = 1,
	VideoHighFrameRate = 131072,
	VideoStreamed = 65536,
	VideoTimelapse = 262144,
}
```

### New Type MonoTouch.Photos.PHAssetMediaType

```
[Serializable]
public enum PHAssetMediaType {
	Audio = 3,
	Image = 1,
	Unknown = 0,
	Video = 2,
}
```

### New Type MonoTouch.Photos.PHAssetVideoProgressHandler

```
public sealed delegate PHAssetVideoProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHAssetVideoProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (double progress, MonoTouch.Foundation.NSError error, out bool stop, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHAuthorizationStatus

```
[Serializable]
public enum PHAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
```

### New Type MonoTouch.Photos.PHCachingImageManager

```
public class PHCachingImageManager : MonoTouch.Photos.PHImageManager, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHCachingImageManager ();
	public PHCachingImageManager (MonoTouch.Foundation.NSCoder coder);
	public PHCachingImageManager (MonoTouch.Foundation.NSObjectFlag t);
	public PHCachingImageManager (System.IntPtr handle);
	// properties
	public virtual bool AllowsCachingHighQualityImages { get; set; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void StartCaching (PHAsset[] assets, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHImageRequestOptions options);
	public virtual void StopCaching (PHAsset[] assets, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHImageRequestOptions options);
	public virtual void StopCaching ();
}
```

### New Type MonoTouch.Photos.PHChange

```
public class PHChange : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHChange ();
	public PHChange (MonoTouch.Foundation.NSCoder coder);
	public PHChange (MonoTouch.Foundation.NSObjectFlag t);
	public PHChange (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual PHFetchResultChangeDetails GetFetchResultChangeDetails (PHFetchResult obj);
	public virtual PHObjectChangeDetails GetObjectChangeDetails (PHObject obj);
}
```

### New Type MonoTouch.Photos.PHChangeDetailEnumerator

```
public sealed delegate PHChangeDetailEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHChangeDetailEnumerator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint fromIndex, uint toIndex, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (uint fromIndex, uint toIndex);
}
```

### New Type MonoTouch.Photos.PHCollection

```
public class PHCollection : MonoTouch.Photos.PHObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHCollection (MonoTouch.Foundation.NSCoder coder);
	public PHCollection (MonoTouch.Foundation.NSObjectFlag t);
	public PHCollection (System.IntPtr handle);
	// properties
	public virtual bool CanContainAssets { get; }
	public virtual bool CanContainCollections { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string LocalizedTitle { get; }
	// methods
	public virtual bool CanPerformEditOperation (PHCollectionEditOperation anOperation);
	public static PHFetchResult FetchCollections (PHCollectionList collectionList, PHFetchOptions options);
	public static PHFetchResult FetchTopLevelUserCollections (PHFetchOptions options);
}
```

### New Type MonoTouch.Photos.PHCollectionEditOperation

```
[Serializable]
public enum PHCollectionEditOperation {
	AddContent = 3,
	CreateContent = 4,
	Delete = 6,
	DeleteContent = 1,
	None = 0,
	RearrangeContent = 5,
	RemoveContent = 2,
	Rename = 7,
}
```

### New Type MonoTouch.Photos.PHCollectionList

```
public class PHCollectionList : MonoTouch.Photos.PHCollection, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHCollectionList ();
	public PHCollectionList (MonoTouch.Foundation.NSCoder coder);
	public PHCollectionList (MonoTouch.Foundation.NSObjectFlag t);
	public PHCollectionList (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHCollectionListSubtype CollectionListSubtype { get; }
	public virtual PHCollectionListType CollectionListType { get; }
	public virtual MonoTouch.Foundation.NSDate EndDate { get; }
	public virtual string[] LocalizedLocationNames { get; }
	public virtual MonoTouch.Foundation.NSDate StartDate { get; }
	// methods
	public static PHCollectionList CreateTransientCollectionList (PHAssetCollection[] collections, string title);
	public static PHCollectionList CreateTransientCollectionList (PHFetchResult fetchResult, string title);
	protected override void Dispose (bool disposing);
	public static PHFetchResult FetchCollectionLists (PHCollection collection, PHFetchOptions options);
	public static PHFetchResult FetchCollectionLists (PHCollectionListType type, PHCollectionListSubtype subType, PHFetchOptions options);
	public static PHFetchResult FetchCollectionLists (string[] identifiers, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHAssetCollection moment, PHFetchOptions options);
	public static PHFetchResult FetchMomentLists (PHCollectionListSubtype subType, PHFetchOptions options);
}
```

### New Type MonoTouch.Photos.PHCollectionListChangeRequest

```
public class PHCollectionListChangeRequest : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHCollectionListChangeRequest (MonoTouch.Foundation.NSCoder coder);
	public PHCollectionListChangeRequest (MonoTouch.Foundation.NSObjectFlag t);
	public PHCollectionListChangeRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHObjectPlaceholder PlaceholderForCreatedCollectionList { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual void AddChildCollections (PHCollection[] collections);
	public static PHCollectionListChangeRequest ChangeRequest (PHCollectionList collectionList);
	public static PHCollectionListChangeRequest ChangeRequest (PHCollectionList collectionList, PHFetchResult childCollections);
	public static PHCollectionListChangeRequest CreateAssetCollection (string title);
	public static void DeleteCollectionLists (PHCollectionList[] collectionLists);
	protected override void Dispose (bool disposing);
	public virtual void InsertChildCollections (PHCollection[] collections, MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void MoveChildCollections (MonoTouch.Foundation.NSIndexSet indexes, uint toIndex);
	public virtual void RemoveChildCollections (PHCollection[] collections);
	public virtual void RemoveChildCollections (MonoTouch.Foundation.NSIndexSet indexes);
	public virtual void ReplaceChildCollection (MonoTouch.Foundation.NSIndexSet indexes, PHCollection[] collections);
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

### New Type MonoTouch.Photos.PHCollectionListType

```
[Serializable]
public enum PHCollectionListType {
	Folder = 2,
	MomentList = 1,
	SmartFolder = 3,
}
```

### New Type MonoTouch.Photos.PHContentEditingHandler

```
public sealed delegate PHContentEditingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHContentEditingHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (PHContentEditingInput contentEditingInput, MonoTouch.Foundation.NSDictionary requestStatusInfo, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (PHContentEditingInput contentEditingInput, MonoTouch.Foundation.NSDictionary requestStatusInfo);
}
```

### New Type MonoTouch.Photos.PHContentEditingInput

```
public class PHContentEditingInput : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHContentEditingInput ();
	public PHContentEditingInput (MonoTouch.Foundation.NSCoder coder);
	public PHContentEditingInput (MonoTouch.Foundation.NSObjectFlag t);
	public PHContentEditingInput (System.IntPtr handle);
	// properties
	public virtual PHAdjustmentData AdjustmentData { get; }
	public virtual MonoTouch.AVFoundation.AVAsset AvAsset { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDate CreationDate { get; }
	public virtual MonoTouch.UIKit.UIImage DisplaySizeImage { get; }
	public virtual MonoTouch.CoreImage.CIImageOrientation FullSizeImageOrientation { get; }
	public virtual MonoTouch.Foundation.NSUrl FullSizeImageUrl { get; }
	public virtual MonoTouch.CoreLocation.CLLocation Location { get; }
	public virtual PHAssetMediaSubtype MediaSubtypes { get; }
	public virtual PHAssetMediaType MediaType { get; }
	public virtual string UniformTypeIdentifier { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Photos.PHContentEditingInputRequestOptions

```
public class PHContentEditingInputRequestOptions : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHContentEditingInputRequestOptions ();
	public PHContentEditingInputRequestOptions (MonoTouch.Foundation.NSCoder coder);
	public PHContentEditingInputRequestOptions (MonoTouch.Foundation.NSObjectFlag t);
	public PHContentEditingInputRequestOptions (System.IntPtr handle);
	// properties
	public static MonoTouch.Foundation.NSString CancelledKey { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString InputErrorKey { get; }
	public virtual bool NetworkAccessAllowed { get; set; }
	public static MonoTouch.Foundation.NSString ResultIsInCloudKey { get; }
	// methods
	public virtual void SetCanHandleAdjustmentDataHandler (System.Func<PHAdjustmentData,System.Boolean> canHandleAdjustmentDataPredicate);
	public virtual void SetProgressHandler (PHProgressHandler progressHandler);
}
```

### New Type MonoTouch.Photos.PHContentEditingOutput

```
public class PHContentEditingOutput : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHContentEditingOutput ();
	public PHContentEditingOutput (MonoTouch.Foundation.NSCoder coder);
	public PHContentEditingOutput (MonoTouch.Foundation.NSObjectFlag t);
	public PHContentEditingOutput (System.IntPtr handle);
	public PHContentEditingOutput (PHContentEditingInput contentEditingInput);
	public PHContentEditingOutput (PHObjectPlaceholder placeholderForCreatedAsset);
	// properties
	public virtual PHAdjustmentData AdjustmentData { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUrl RenderedContentUrl { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Photos.PHFetchOptions

```
public class PHFetchOptions : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHFetchOptions ();
	public PHFetchOptions (MonoTouch.Foundation.NSCoder coder);
	public PHFetchOptions (MonoTouch.Foundation.NSObjectFlag t);
	public PHFetchOptions (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IncludeAllBurstAssets { get; set; }
	public virtual bool IncludeHiddenAssets { get; set; }
	public virtual MonoTouch.Foundation.NSPredicate Predicate { get; set; }
	public virtual MonoTouch.Foundation.NSSortDescriptor[] SortDescriptors { get; set; }
	public virtual bool WantsIncrementalChangeDetails { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Photos.PHFetchResult

```
public class PHFetchResult : MonoTouch.Foundation.NSObject, System.Collections.Generic.IEnumerable<MonoTouch.Foundation.NSObject>, MonoTouch.Foundation.INSCopying, System.Collections.IEnumerable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHFetchResult (MonoTouch.Foundation.NSCoder coder);
	public PHFetchResult (MonoTouch.Foundation.NSObjectFlag t);
	public PHFetchResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int Count { get; }
	public virtual MonoTouch.Foundation.NSObject firstObject { get; }
	public MonoTouch.Foundation.NSObject Item { get; }
	public virtual MonoTouch.Foundation.NSObject LastObject { get; }
	// methods
	public virtual bool Contains (MonoTouch.Foundation.NSObject id);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);
	protected override void Dispose (bool disposing);
	public virtual void Enumerate (MonoTouch.Foundation.NSIndexSet idx, MonoTouch.Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);
	public virtual void Enumerate (MonoTouch.Foundation.NSEnumerationOptions opts, PHFetchResultEnumerator handler);
	public virtual void Enumerate (PHFetchResultEnumerator handler);
	public virtual System.Collections.Generic.IEnumerator<MonoTouch.Foundation.NSObject> GetEnumerator ();
	public virtual int IndexOf (MonoTouch.Foundation.NSObject id);
	public virtual int IndexOf (MonoTouch.Foundation.NSObject id, MonoTouch.Foundation.NSRange range);
	public virtual MonoTouch.Foundation.NSObject ObjectAt (int index);
	public T[] ObjectsAt<T> (MonoTouch.Foundation.NSIndexSet indexes);
}
```

### New Type MonoTouch.Photos.PHFetchResultChangeDetails

```
public class PHFetchResultChangeDetails : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHFetchResultChangeDetails ();
	public PHFetchResultChangeDetails (MonoTouch.Foundation.NSCoder coder);
	public PHFetchResultChangeDetails (MonoTouch.Foundation.NSObjectFlag t);
	public PHFetchResultChangeDetails (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSIndexSet ChangedIndexes { get; }
	public virtual PHObject[] ChangedObjects { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual PHFetchResult FetchResultAfterChanges { get; }
	public virtual PHFetchResult FetchResultBeforeChanges { get; }
	public virtual bool HasIncrementalChanges { get; }
	public virtual bool HasMoves { get; }
	public virtual MonoTouch.Foundation.NSIndexSet InsertedIndexes { get; }
	public virtual PHObject[] InsertedObjects { get; }
	public virtual MonoTouch.Foundation.NSIndexSet RemovedIndexes { get; }
	public virtual PHObject[] RemovedObjects { get; }
	// methods
	public static PHFetchResultChangeDetails ChangeDetails (PHFetchResult fromResult, PHFetchResult toResult, PHObject[] changedObjects);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateMoves (PHChangeDetailEnumerator handler);
}
```

### New Type MonoTouch.Photos.PHFetchResultEnumerator

```
public sealed delegate PHFetchResultEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHFetchResultEnumerator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.Foundation.NSObject element, uint elementIndex, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.Foundation.NSObject element, uint elementIndex, out bool stop);
}
```

### New Type MonoTouch.Photos.PHImageContentMode

```
[Serializable]
public enum PHImageContentMode {
	AspectFill = 1,
	AspectFit = 0,
	Default = 0,
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

### New Type MonoTouch.Photos.PHImageKeys

```
public static class PHImageKeys {
	// properties
	public static MonoTouch.Foundation.NSString Cancelled { get; }
	public static MonoTouch.Foundation.NSString Error { get; }
	public static MonoTouch.Foundation.NSString ResultIsDegraded { get; }
	public static MonoTouch.Foundation.NSString ResultIsInCloud { get; }
	public static MonoTouch.Foundation.NSString ResultRequestID { get; }
}
```

### New Type MonoTouch.Photos.PHImageManager

```
public class PHImageManager : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHImageManager ();
	public PHImageManager (MonoTouch.Foundation.NSCoder coder);
	public PHImageManager (MonoTouch.Foundation.NSObjectFlag t);
	public PHImageManager (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static PHImageManager DefaultManager { get; }
	public static System.Drawing.SizeF MaximumSize { get; }
	// methods
	public virtual void CancelImageRequest (int requestID);
	public virtual int RequestAvAsset (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestAvAssetHandler resultHandler);
	public virtual int RequestExportSession (PHAsset asset, PHVideoRequestOptions options, string exportPreset, PHImageManagerRequestExportHandler resultHandler);
	public virtual int RequestImageData (PHAsset asset, PHImageRequestOptions options, PHImageDataHandler handler);
	public virtual int RequestImageForAsset (PHAsset asset, System.Drawing.SizeF targetSize, PHImageContentMode contentMode, PHImageRequestOptions options, PHImageResultHandler resultHandler);
	public virtual int RequestPlayerItem (PHAsset asset, PHVideoRequestOptions options, PHImageManagerRequestPlayerHandler resultHandler);
}
```

### New Type MonoTouch.Photos.PHImageManagerRequestAvAssetHandler

```
public sealed delegate PHImageManagerRequestAvAssetHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageManagerRequestAvAssetHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.AVFoundation.AVAsset asset, MonoTouch.AVFoundation.AVAudioMix audioMix, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.AVFoundation.AVAsset asset, MonoTouch.AVFoundation.AVAudioMix audioMix, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHImageManagerRequestExportHandler

```
public sealed delegate PHImageManagerRequestExportHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageManagerRequestExportHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.AVFoundation.AVAssetExportSession exportSession, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.AVFoundation.AVAssetExportSession exportSession, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHImageManagerRequestPlayerHandler

```
public sealed delegate PHImageManagerRequestPlayerHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageManagerRequestPlayerHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.AVFoundation.AVPlayerItem playerItem, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.AVFoundation.AVPlayerItem playerItem, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHImageRequestOptions

```
public class PHImageRequestOptions : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHImageRequestOptions ();
	public PHImageRequestOptions (MonoTouch.Foundation.NSCoder coder);
	public PHImageRequestOptions (MonoTouch.Foundation.NSObjectFlag t);
	public PHImageRequestOptions (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHImageRequestOptionsDeliveryMode DeliveryMode { get; set; }
	public virtual bool NetworkAccessAllowed { get; set; }
	public virtual System.Drawing.RectangleF NormalizedCropRect { get; set; }
	public virtual PHAssetImageProgressHandler ProgressHandler { get; set; }
	public virtual PHImageRequestOptionsResizeMode ResizeMode { get; set; }
	public virtual bool Synchronous { get; set; }
	public virtual PHImageRequestOptionsVersion Version { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Photos.PHImageRequestOptionsDeliveryMode

```
[Serializable]
public enum PHImageRequestOptionsDeliveryMode {
	FastFormat = 2,
	HighQualityFormat = 1,
	Opportunistic = 0,
}
```

### New Type MonoTouch.Photos.PHImageRequestOptionsResizeMode

```
[Serializable]
public enum PHImageRequestOptionsResizeMode {
	Exact = 2,
	Fast = 1,
	None = 0,
}
```

### New Type MonoTouch.Photos.PHImageRequestOptionsVersion

```
[Serializable]
public enum PHImageRequestOptionsVersion {
	Current = 0,
	Original = 2,
	Unadjusted = 1,
}
```

### New Type MonoTouch.Photos.PHImageResultHandler

```
public sealed delegate PHImageResultHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHImageResultHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.UIKit.UIImage result, MonoTouch.Foundation.NSDictionary info, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.UIKit.UIImage result, MonoTouch.Foundation.NSDictionary info);
}
```

### New Type MonoTouch.Photos.PHObject

```
public class PHObject : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHObject (MonoTouch.Foundation.NSCoder coder);
	public PHObject (MonoTouch.Foundation.NSObjectFlag t);
	public PHObject (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string LocalIdentifier { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Photos.PHObjectChangeDetails

```
public class PHObjectChangeDetails : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHObjectChangeDetails ();
	public PHObjectChangeDetails (MonoTouch.Foundation.NSCoder coder);
	public PHObjectChangeDetails (MonoTouch.Foundation.NSObjectFlag t);
	public PHObjectChangeDetails (System.IntPtr handle);
	// properties
	public virtual bool AssetContentChanged { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSObject ObjectAfterChanges { get; }
	public virtual MonoTouch.Foundation.NSObject ObjectBeforeChanges { get; }
	public virtual bool ObjectWasDeleted { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Photos.PHObjectPlaceholder

```
public class PHObjectPlaceholder : MonoTouch.Photos.PHObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHObjectPlaceholder ();
	public PHObjectPlaceholder (MonoTouch.Foundation.NSCoder coder);
	public PHObjectPlaceholder (MonoTouch.Foundation.NSObjectFlag t);
	public PHObjectPlaceholder (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.Photos.PHPhotoLibrary

```
public class PHPhotoLibrary : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHPhotoLibrary (MonoTouch.Foundation.NSCoder coder);
	public PHPhotoLibrary (MonoTouch.Foundation.NSObjectFlag t);
	public PHPhotoLibrary (System.IntPtr handle);
	// properties
	public static PHAuthorizationStatus AuthorizationStatus { get; }
	public override System.IntPtr ClassHandle { get; }
	public static PHPhotoLibrary SharedPhotoLibrary { get; }
	// methods
	public virtual void PerformChanges (System.Action changeHandler, System.Action<System.Boolean,MonoTouch.Foundation.NSError> completionHandler);
	public virtual bool PerformChangesAndWait (System.Action changeHandler, out MonoTouch.Foundation.NSError error);
	public object RegisterChangeObserver (System.Action<PHChange> changeObserver);
	public virtual void RegisterChangeObserver (PHPhotoLibraryChangeObserver observer);
	public static void RequestAuthorization (System.Action<PHAuthorizationStatus> handler);
	public void UnregisterChangeObserver (object registeredToken);
	public virtual void UnregisterChangeObserver (PHPhotoLibraryChangeObserver observer);
}
```

### New Type MonoTouch.Photos.PHPhotoLibraryChangeObserver

```
public class PHPhotoLibraryChangeObserver : MonoTouch.Foundation.NSObject, IPHPhotoLibraryChangeObserver, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHPhotoLibraryChangeObserver ();
	public PHPhotoLibraryChangeObserver (MonoTouch.Foundation.NSCoder coder);
	public PHPhotoLibraryChangeObserver (MonoTouch.Foundation.NSObjectFlag t);
	public PHPhotoLibraryChangeObserver (System.IntPtr handle);
	// methods
	public virtual void PhotoLibraryDidChange (PHChange changeInstance);
}
```

### New Type MonoTouch.Photos.PHPhotoLibraryChangeObserver_Extensions

```
public static class PHPhotoLibraryChangeObserver_Extensions {
	// methods
	public static void PhotoLibraryDidChange (IPHPhotoLibraryChangeObserver This, PHChange changeInstance);
}
```

### New Type MonoTouch.Photos.PHProgressHandler

```
public sealed delegate PHProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public PHProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (double progress, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (double progress, ref bool stop);
}
```

### New Type MonoTouch.Photos.PHVideoRequestOptions

```
public class PHVideoRequestOptions : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHVideoRequestOptions ();
	public PHVideoRequestOptions (MonoTouch.Foundation.NSCoder coder);
	public PHVideoRequestOptions (MonoTouch.Foundation.NSObjectFlag t);
	public PHVideoRequestOptions (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual PHVideoRequestOptionsDeliveryMode DeliveryMode { get; set; }
	public virtual bool NetworkAccessAllowed { get; set; }
	public virtual PHAssetVideoProgressHandler ProgressHandler { get; set; }
	public virtual PHVideoRequestOptionsVersion Version { get; set; }
}
```

### New Type MonoTouch.Photos.PHVideoRequestOptionsDeliveryMode

```
[Serializable]
public enum PHVideoRequestOptionsDeliveryMode {
	Automatic = 0,
	FastFormat = 3,
	HighQualityFormat = 1,
	MediumQualityFormat = 2,
}
```

### New Type MonoTouch.Photos.PHVideoRequestOptionsVersion

```
[Serializable]
public enum PHVideoRequestOptionsVersion {
	Current = 0,
	Original = 1,
}
```

## New Namespace MonoTouch.PhotosUI

### New Type MonoTouch.PhotosUI.IPHContentEditingController

```
public interface IPHContentEditingController : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool ShouldShowCancelConfirmation { get; }
	// methods
	public virtual void CancelContentEditing ();
	public virtual bool CanHandleAdjustmentData (MonoTouch.Photos.PHAdjustmentData adjustmentData);
	public virtual void FinishContentEditing (System.Action<MonoTouch.Photos.PHContentEditingOutput> completionHandler);
	public virtual void StartContentEditing (MonoTouch.Photos.PHContentEditingInput contentEditingInput, MonoTouch.UIKit.UIImage placeholderImage);
}
```

### New Type MonoTouch.PhotosUI.PHContentEditingController

```
public abstract class PHContentEditingController : MonoTouch.Foundation.NSObject, IPHContentEditingController, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PHContentEditingController ();
	public PHContentEditingController (MonoTouch.Foundation.NSCoder coder);
	public PHContentEditingController (MonoTouch.Foundation.NSObjectFlag t);
	public PHContentEditingController (System.IntPtr handle);
	// properties
	public virtual bool ShouldShowCancelConfirmation { get; }
	// methods
	public virtual void CancelContentEditing ();
	public virtual bool CanHandleAdjustmentData (MonoTouch.Photos.PHAdjustmentData adjustmentData);
	public virtual void FinishContentEditing (System.Action<MonoTouch.Photos.PHContentEditingOutput> completionHandler);
	public virtual void StartContentEditing (MonoTouch.Photos.PHContentEditingInput contentEditingInput, MonoTouch.UIKit.UIImage placeholderImage);
}
```

### New Type MonoTouch.PhotosUI.PHContentEditingController_Extensions

```
public static class PHContentEditingController_Extensions {
}
```

## New Namespace MonoTouch.PushKit

### New Type MonoTouch.PushKit.IPKPushRegistryDelegate

```
public interface IPKPushRegistryDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidReceiveIncomingPush (PKPushRegistry registry, PKPushPayload payload, string type);
	public virtual void DidUpdatePushCredentials (PKPushRegistry registry, PKPushCredentials credentials, string type);
}
```

### New Type MonoTouch.PushKit.PKPushCredentials

```
public class PKPushCredentials : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPushCredentials (MonoTouch.Foundation.NSCoder coder);
	public PKPushCredentials (MonoTouch.Foundation.NSObjectFlag t);
	public PKPushCredentials (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData Token { get; }
	public virtual string Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PushKit.PKPushPayload

```
public class PKPushPayload : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPushPayload (MonoTouch.Foundation.NSCoder coder);
	public PKPushPayload (MonoTouch.Foundation.NSObjectFlag t);
	public PKPushPayload (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDictionary DictionaryPayload { get; }
	public virtual string Type { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.PushKit.PKPushRegistry

```
public class PKPushRegistry : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPushRegistry (MonoTouch.Foundation.NSCoder coder);
	public PKPushRegistry (MonoTouch.Foundation.NSObjectFlag t);
	public PKPushRegistry (System.IntPtr handle);
	public PKPushRegistry (MonoTouch.CoreFoundation.DispatchQueue queue);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public PKPushRegistryDelegate Delegate { get; set; }
	public virtual MonoTouch.Foundation.NSSet DesiredPushTypes { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSData PushToken (string type);
}
```

### New Type MonoTouch.PushKit.PKPushRegistryDelegate

```
public abstract class PKPushRegistryDelegate : MonoTouch.Foundation.NSObject, IPKPushRegistryDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public PKPushRegistryDelegate ();
	public PKPushRegistryDelegate (MonoTouch.Foundation.NSCoder coder);
	public PKPushRegistryDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public PKPushRegistryDelegate (System.IntPtr handle);
	// methods
	public virtual void DidInvalidatePushToken (PKPushRegistry registry, string type);
	public virtual void DidReceiveIncomingPush (PKPushRegistry registry, PKPushPayload payload, string type);
	public virtual void DidUpdatePushCredentials (PKPushRegistry registry, PKPushCredentials credentials, string type);
}
```

### New Type MonoTouch.PushKit.PKPushRegistryDelegate_Extensions

```
public static class PKPushRegistryDelegate_Extensions {
	// methods
	public static void DidInvalidatePushToken (IPKPushRegistryDelegate This, PKPushRegistry registry, string type);
}
```

### New Type MonoTouch.PushKit.PKPushType

```
public static class PKPushType {
	// properties
	public static MonoTouch.Foundation.NSString Voip { get; }
}
```

## New Namespace MonoTouch.SceneKit

### New Type MonoTouch.SceneKit._SCNShaderModifiers

```
public static class _SCNShaderModifiers {
}
```

### New Type MonoTouch.SceneKit.ISCNActionable

```
public interface ISCNActionable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNAnimatable

```
public interface ISCNAnimatable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNBoundingVolume

```
public interface ISCNBoundingVolume : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNNodeRendererDelegate

```
public interface ISCNNodeRendererDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNPhysicsContactDelegate

```
public interface ISCNPhysicsContactDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNProgramDelegate

```
public interface ISCNProgramDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNSceneRenderer

```
public interface ISCNSceneRenderer : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.Foundation.NSDictionary options);
}
```

### New Type MonoTouch.SceneKit.ISCNSceneRendererDelegate

```
public interface ISCNSceneRendererDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNShadable

```
public interface ISCNShadable : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.SceneKit.ISCNTechniqueSupport

```
public interface ISCNTechniqueSupport : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNAction

```
public class SCNAction : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAction ();
	public SCNAction (MonoTouch.Foundation.NSCoder coder);
	public SCNAction (MonoTouch.Foundation.NSObjectFlag t);
	public SCNAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DurationInSeconds { get; set; }
	public virtual float Speed { get; set; }
	public virtual SCNActionTimingMode TimingMode { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNAction CustomAction (double seconds, SCNActionNodeWithElapsedTimeHandler handler);
	public static SCNAction FadeIn (double durationInSeconds);
	public static SCNAction FadeOpacityBy (float factor, double durationInSeconds);
	public static SCNAction FadeOpacityTo (float opacity, double durationInSeconds);
	public static SCNAction FadeOut (double durationInSeconds);
	public static SCNAction FromJavascript (string script, double seconds);
	public static SCNAction Group (SCNAction[] actions);
	public static SCNAction MoveBy (SCNVector3 delta, double durationInSeconds);
	public static SCNAction MoveBy (float deltaX, float deltaY, float deltaZ, double durationInSeconds);
	public static SCNAction MoveTo (SCNVector3 location, double durationInSeconds);
	public static SCNAction RemoveFromParentNode ();
	public static SCNAction RepeatAction (SCNAction action, uint count);
	public static SCNAction RepeatActionForever (SCNAction action);
	public virtual SCNAction ReversedAction ();
	public static SCNAction RotateBy (float angle, SCNVector3 axis, double durationInSeconds);
	public static SCNAction RotateBy (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds, bool shortestUnitArc);
	public static SCNAction RotateTo (SCNVector4 axisAngle, double durationInSeconds);
	public static SCNAction Run (System.Action<SCNNode> handler, MonoTouch.CoreFoundation.DispatchQueue queue);
	public static SCNAction Run (System.Action<SCNNode> handler);
	public static SCNAction ScaleBy (float scale, double durationInSeconds);
	public static SCNAction ScaleTo (float scale, double durationInSeconds);
	public static SCNAction Sequence (SCNAction[] actions);
	public virtual void SetTimingFunction (System.Action<float> timingFunction);
	public static SCNAction Wait (double durationInSeconds);
	public static SCNAction Wait (double durationInSeconds, double durationRange);
}
```

### New Type MonoTouch.SceneKit.SCNActionable

```
public class SCNActionable : MonoTouch.Foundation.NSObject, ISCNActionable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNActionable ();
	public SCNActionable (MonoTouch.Foundation.NSCoder coder);
	public SCNActionable (MonoTouch.Foundation.NSObjectFlag t);
	public SCNActionable (System.IntPtr handle);
	// methods
	public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
}
```

### New Type MonoTouch.SceneKit.SCNActionable_Extensions

```
public static class SCNActionable_Extensions {
	// methods
	public static SCNAction GetAction (ISCNActionable This, string key);
	public static bool HasActions (ISCNActionable This);
	public static void RemoveAction (ISCNActionable This, string key);
	public static void RemoveAllActions (ISCNActionable This);
	public static void RunAction (ISCNActionable This, SCNAction action);
	public static void RunAction (ISCNActionable This, SCNAction action, string key);
	public static void RunAction (ISCNActionable This, SCNAction action, System.Action block);
	public static void RunAction (ISCNActionable This, SCNAction action, string key, System.Action block);
}
```

### New Type MonoTouch.SceneKit.SCNActionNodeWithElapsedTimeHandler

```
public sealed delegate SCNActionNodeWithElapsedTimeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNActionNodeWithElapsedTimeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, float elapsedTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (SCNNode node, float elapsedTime);
}
```

### New Type MonoTouch.SceneKit.SCNActionTimingMode

```
[Serializable]
public enum SCNActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type MonoTouch.SceneKit.SCNAnimatable

```
public class SCNAnimatable : MonoTouch.Foundation.NSObject, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAnimatable ();
	public SCNAnimatable (MonoTouch.Foundation.NSCoder coder);
	public SCNAnimatable (MonoTouch.Foundation.NSObjectFlag t);
	public SCNAnimatable (System.IntPtr handle);
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNAnimatable_Extensions

```
public static class SCNAnimatable_Extensions {
	// methods
	public static void AddAnimation (ISCNAnimatable This, MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public static MonoTouch.CoreAnimation.CAAnimation GetAnimation (ISCNAnimatable This, MonoTouch.Foundation.NSString key);
	public static MonoTouch.Foundation.NSString[] GetAnimationKeys (ISCNAnimatable This);
	public static bool IsAnimationPaused (ISCNAnimatable This, MonoTouch.Foundation.NSString key);
	public static void PauseAnimation (ISCNAnimatable This, MonoTouch.Foundation.NSString key);
	public static void RemoveAllAnimations (ISCNAnimatable This);
	public static void RemoveAnimation (ISCNAnimatable This, MonoTouch.Foundation.NSString key);
	public static void RemoveAnimation (ISCNAnimatable This, MonoTouch.Foundation.NSString key, float duration);
	public static void ResumeAnimation (ISCNAnimatable This, MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNAnimationEvent

```
public class SCNAnimationEvent : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAnimationEvent (MonoTouch.Foundation.NSCoder coder);
	public SCNAnimationEvent (MonoTouch.Foundation.NSObjectFlag t);
	public SCNAnimationEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNAnimationEvent Create (float keyTime, SCNAnimationEventHandler eventHandler);
}
```

### New Type MonoTouch.SceneKit.SCNAnimationEventHandler

```
public sealed delegate SCNAnimationEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNAnimationEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSObject animatedObject, bool playingBackward, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSObject animatedObject, bool playingBackward);
}
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

### New Type MonoTouch.SceneKit.SCNBindingHandler

```
public sealed delegate SCNBindingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNBindingHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint programId, uint location, SCNNode renderedNode, SCNRenderer renderer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (uint programId, uint location, SCNNode renderedNode, SCNRenderer renderer);
}
```

### New Type MonoTouch.SceneKit.SCNBoundingVolume

```
public class SCNBoundingVolume : MonoTouch.Foundation.NSObject, ISCNBoundingVolume, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNBoundingVolume ();
	public SCNBoundingVolume (MonoTouch.Foundation.NSCoder coder);
	public SCNBoundingVolume (MonoTouch.Foundation.NSObjectFlag t);
	public SCNBoundingVolume (System.IntPtr handle);
	// methods
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
}
```

### New Type MonoTouch.SceneKit.SCNBoundingVolume_Extensions

```
public static class SCNBoundingVolume_Extensions {
	// methods
	public static bool GetBoundingBox (ISCNBoundingVolume This, ref SCNVector3 min, ref SCNVector3 max);
	public static bool GetBoundingSphere (ISCNBoundingVolume This, ref SCNVector3 center, ref float radius);
}
```

### New Type MonoTouch.SceneKit.SCNBox

```
public class SCNBox : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNBox ();
	public SCNBox (MonoTouch.Foundation.NSCoder coder);
	public SCNBox (MonoTouch.Foundation.NSObjectFlag t);
	public SCNBox (System.IntPtr handle);
	// properties
	public virtual float ChamferRadius { get; set; }
	public virtual int ChamferSegmentCount { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual float Length { get; set; }
	public virtual int LengthSegmentCount { get; set; }
	public virtual float Width { get; set; }
	public virtual int WidthSegmentCount { get; set; }
	// methods
	public static SCNBox Create (float width, float height, float length, float chamferRadius);
}
```

### New Type MonoTouch.SceneKit.SCNCamera

```
public class SCNCamera : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNTechniqueSupport, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNCamera ();
	public SCNCamera (MonoTouch.Foundation.NSCoder coder);
	public SCNCamera (MonoTouch.Foundation.NSObjectFlag t);
	public SCNCamera (System.IntPtr handle);
	// properties
	public virtual float Aperture { get; set; }
	public virtual bool AutomaticallyAdjustsZRange { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float FocalBlurRadius { get; set; }
	public virtual float FocalDistance { get; set; }
	public virtual float FocalSize { get; set; }
	public virtual string Name { get; set; }
	public virtual double OrthographicScale { get; set; }
	public virtual SCNMatrix4 ProjectionTransform { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual bool UsesOrthographicProjection { get; set; }
	public virtual double XFov { get; set; }
	public virtual double YFov { get; set; }
	public virtual double ZFar { get; set; }
	public virtual double ZNear { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNCamera Create ();
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNCapsule

```
public class SCNCapsule : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNCapsule ();
	public SCNCapsule (MonoTouch.Foundation.NSCoder coder);
	public SCNCapsule (MonoTouch.Foundation.NSObjectFlag t);
	public SCNCapsule (System.IntPtr handle);
	// properties
	public virtual float CapRadius { get; set; }
	public virtual int CapSegmentCount { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual int RadialSegmentCount { get; set; }
	// methods
	public static SCNCapsule Create (float capRadius, float height);
}
```

### New Type MonoTouch.SceneKit.SCNChamferMode

```
[Serializable]
public enum SCNChamferMode {
	Back = 2,
	Both = 0,
	Front = 1,
}
```

### New Type MonoTouch.SceneKit.SCNCone

```
public class SCNCone : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNCone ();
	public SCNCone (MonoTouch.Foundation.NSCoder coder);
	public SCNCone (MonoTouch.Foundation.NSObjectFlag t);
	public SCNCone (System.IntPtr handle);
	// properties
	public virtual float BottomRadius { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual int RadialSegmentCount { get; set; }
	public virtual float TopRadius { get; set; }
	// methods
	public static SCNCone Create (float topRadius, float bottomRadius, float height);
}
```

### New Type MonoTouch.SceneKit.SCNConstraint

```
public class SCNConstraint : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNConstraint (MonoTouch.Foundation.NSCoder coder);
	public SCNConstraint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float InfluenceFactor { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNCullMode

```
[Serializable]
public enum SCNCullMode {
	Back = 0,
	Front = 1,
}
```

### New Type MonoTouch.SceneKit.SCNCylinder

```
public class SCNCylinder : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNCylinder ();
	public SCNCylinder (MonoTouch.Foundation.NSCoder coder);
	public SCNCylinder (MonoTouch.Foundation.NSObjectFlag t);
	public SCNCylinder (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual int RadialSegmentCount { get; set; }
	public virtual float Radius { get; set; }
	// methods
	public static SCNCylinder Create (float radius, float height);
}
```

### New Type MonoTouch.SceneKit.SCNFieldForceEvaluator

```
public sealed delegate SCNFieldForceEvaluator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNFieldForceEvaluator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNVector3 position, SCNVector3 velocity, float mass, float charge, double timeInSeconds, System.AsyncCallback callback, object object);
	public virtual SCNVector3 EndInvoke (System.IAsyncResult result);
	public virtual SCNVector3 Invoke (SCNVector3 position, SCNVector3 velocity, float mass, float charge, double timeInSeconds);
}
```

### New Type MonoTouch.SceneKit.SCNFilterMode

```
[Serializable]
public enum SCNFilterMode {
	Linear = 2,
	Nearest = 1,
	None = 0,
}
```

### New Type MonoTouch.SceneKit.SCNFloor

```
public class SCNFloor : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNFloor ();
	public SCNFloor (MonoTouch.Foundation.NSCoder coder);
	public SCNFloor (MonoTouch.Foundation.NSObjectFlag t);
	public SCNFloor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float ReflectionFalloffEnd { get; set; }
	public virtual float ReflectionFalloffStart { get; set; }
	public virtual float ReflectionResolutionScaleFactor { get; set; }
	public virtual float Reflectivity { get; set; }
	// methods
	public static SCNFloor Create ();
}
```

### New Type MonoTouch.SceneKit.SCNGeometry

```
public class SCNGeometry : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNGeometry (MonoTouch.Foundation.NSCoder coder);
	public SCNGeometry (MonoTouch.Foundation.NSObjectFlag t);
	public SCNGeometry (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNGeometryElement EdgeCreasesElement { get; set; }
	public virtual SCNGeometrySource EdgeCreasesSource { get; set; }
	public virtual SCNMaterial FirstMaterial { get; set; }
	public virtual int GeometryElementCount { get; }
	public virtual SCNLevelOfDetail[] LevelsOfDetail { get; set; }
	public virtual SCNMaterial[] Materials { get; set; }
	public virtual string Name { get; set; }
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual uint SubdivisionLevel { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNGeometry Create ();
	protected override void Dispose (bool disposing);
	public static MonoTouch.Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
	public virtual SCNGeometryElement GetGeometryElement (int elementIndex);
	public virtual SCNGeometrySource[] GetGeometrySourcesForSemantic (string semantic);
	public virtual SCNMaterial GetMaterial (string name);
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual void InsertMaterial (SCNMaterial material, int index);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveMaterial (int index);
	public virtual void ReplaceMaterial (int materialIndex, SCNMaterial newMaterial);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNGeometryElement

```
public class SCNGeometryElement : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNGeometryElement ();
	public SCNGeometryElement (MonoTouch.Foundation.NSCoder coder);
	public SCNGeometryElement (MonoTouch.Foundation.NSObjectFlag t);
	public SCNGeometryElement (System.IntPtr handle);
	// properties
	public virtual int BytesPerIndex { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData Data { get; }
	public virtual int PrimitiveCount { get; }
	public virtual SCNGeometryPrimitiveType PrimitiveType { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static SCNGeometryElement FromData (MonoTouch.Foundation.NSData data, SCNGeometryPrimitiveType primitiveType, int primitiveCount, int bytesPerIndex);
}
```

### New Type MonoTouch.SceneKit.SCNGeometryPrimitiveType

```
[Serializable]
public enum SCNGeometryPrimitiveType {
	Line = 2,
	Point = 3,
	Triangles = 0,
	TriangleStrip = 1,
}
```

### New Type MonoTouch.SceneKit.SCNGeometrySource

```
public class SCNGeometrySource : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNGeometrySource ();
	public SCNGeometrySource (MonoTouch.Foundation.NSCoder coder);
	public SCNGeometrySource (MonoTouch.Foundation.NSObjectFlag t);
	public SCNGeometrySource (System.IntPtr handle);
	// properties
	public virtual int BytesPerComponent { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int ComponentsPerVector { get; }
	public virtual MonoTouch.Foundation.NSData Data { get; }
	public virtual int DataOffset { get; }
	public virtual int DataStride { get; }
	public virtual bool FloatComponents { get; }
	public virtual MonoTouch.Foundation.NSString Semantic { get; }
	public virtual int VectorCount { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static SCNGeometrySource FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSString geometrySourceSemantic, int vectorCount, bool floatComponents, int componentsPerVector, int bytesPerComponent, int offset, int stride);
	public static SCNGeometrySource FromNormals (SCNVector3[] normals);
	public static SCNGeometrySource FromTextureCoordinates (System.Drawing.PointF[] texcoords);
	public static SCNGeometrySource FromVertices (SCNVector3[] vertices);
}
```

### New Type MonoTouch.SceneKit.SCNGeometrySourceSemantic

```
public static class SCNGeometrySourceSemantic {
	// properties
	public static MonoTouch.Foundation.NSString BoneIndices { get; }
	public static MonoTouch.Foundation.NSString BoneWeights { get; }
	public static MonoTouch.Foundation.NSString Color { get; }
	public static MonoTouch.Foundation.NSString EdgeCrease { get; }
	public static MonoTouch.Foundation.NSString Normal { get; }
	public static MonoTouch.Foundation.NSString Texcoord { get; }
	public static MonoTouch.Foundation.NSString Vertex { get; }
	public static MonoTouch.Foundation.NSString VertexCrease { get; }
}
```

### New Type MonoTouch.SceneKit.SCNHitTest

```
public static class SCNHitTest {
	// properties
	public static MonoTouch.Foundation.NSString BackFaceCullingKey { get; }
	public static MonoTouch.Foundation.NSString BoundingBoxOnlyKey { get; }
	public static MonoTouch.Foundation.NSString ClipToZRangeKey { get; }
	public static MonoTouch.Foundation.NSString FirstFoundOnlyKey { get; }
	public static MonoTouch.Foundation.NSString IgnoreChildNodesKey { get; }
	public static MonoTouch.Foundation.NSString IgnoreHiddenNodesKey { get; }
	public static MonoTouch.Foundation.NSString RootNodeKey { get; }
	public static MonoTouch.Foundation.NSString SortResultsKey { get; }
}
```

### New Type MonoTouch.SceneKit.SCNHitTestOptions

```
public class SCNHitTestOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public SCNHitTestOptions ();
	public SCNHitTestOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? BackFaceCulling { get; set; }
	public bool? BoundingBoxOnly { get; set; }
	public bool? FirstFoundOnly { get; set; }
	public bool? IgnoreChildNodes { get; set; }
	public bool? IgnoreHiddenNodes { get; set; }
	public SCNNode RootNode { get; set; }
	public bool? SortResults { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNHitTestResult

```
public class SCNHitTestResult : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNHitTestResult (MonoTouch.Foundation.NSCoder coder);
	public SCNHitTestResult (MonoTouch.Foundation.NSObjectFlag t);
	public SCNHitTestResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual int FaceIndex { get; }
	public virtual int GeometryIndex { get; }
	public virtual SCNVector3 LocalCoordinates { get; }
	public virtual SCNVector3 LocalNormal { get; }
	public virtual SCNMatrix4 ModelTransform { get; }
	public virtual SCNNode Node { get; }
	public virtual SCNVector3 WorldCoordinates { get; }
	public virtual SCNVector3 WorldNormal { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.PointF GetTextureCoordinatesWithMappingChannel (int channel);
}
```

### New Type MonoTouch.SceneKit.SCNIKConstraint

```
public class SCNIKConstraint : MonoTouch.SceneKit.SCNConstraint, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNIKConstraint (MonoTouch.Foundation.NSCoder coder);
	public SCNIKConstraint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNIKConstraint (System.IntPtr handle);
	// properties
	public virtual SCNNode ChainRootNode { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 TargetPosition { get; set; }
	// methods
	public static SCNIKConstraint Create (SCNNode chainRootNode);
	protected override void Dispose (bool disposing);
	public virtual float GetMaxAllowedRotationAngle (SCNNode node);
	public virtual void SetMaxAllowedRotationAnglet (float angle, SCNNode node);
}
```

### New Type MonoTouch.SceneKit.SCNJavaScript

```
public static class SCNJavaScript {
	// methods
	public static void ExportModule (MonoTouch.JavaScriptCore.JSContext context);
}
```

### New Type MonoTouch.SceneKit.SCNLevelOfDetail

```
public class SCNLevelOfDetail : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNLevelOfDetail (MonoTouch.Foundation.NSCoder coder);
	public SCNLevelOfDetail (MonoTouch.Foundation.NSObjectFlag t);
	public SCNLevelOfDetail (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNGeometry Geometry { get; }
	public virtual float ScreenSpaceRadius { get; }
	public virtual float WorldSpaceDistance { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNLevelOfDetail CreateWithScreenSpaceRadius (SCNGeometry geometry, float screenSpaceRadius);
	public static SCNLevelOfDetail CreateWithWorldSpaceDistance (SCNGeometry geometry, float worldSpaceDistance);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNLight

```
public class SCNLight : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNTechniqueSupport, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNLight ();
	public SCNLight (MonoTouch.Foundation.NSCoder coder);
	public SCNLight (MonoTouch.Foundation.NSObjectFlag t);
	public SCNLight (System.IntPtr handle);
	// properties
	public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationFalloffExponent { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public virtual bool CastsShadow { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public MonoTouch.UIKit.UIColor Color { get; set; }
	public virtual SCNMaterialProperty Gobo { get; }
	public virtual MonoTouch.Foundation.NSString LightType { get; set; }
	public virtual string Name { get; set; }
	public virtual float OrthographicScale { get; set; }
	public virtual float ShadowBias { get; set; }
	public MonoTouch.UIKit.UIColor ShadowColor { get; set; }
	public virtual System.Drawing.SizeF ShadowMapSize { get; set; }
	public virtual SCNShadowMode ShadowMode { get; set; }
	public virtual float ShadowRadius { get; set; }
	public virtual uint ShadowSampleCount { get; set; }
	public virtual float SpotInnerAngle { get; set; }
	public virtual float SpotOuterAngle { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakColor { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakShadowColor { get; set; }
	public virtual float ZFar { get; set; }
	public virtual float ZNear { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNLight Create ();
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual MonoTouch.Foundation.NSObject GetAttribute (MonoTouch.Foundation.NSString lightAttribute);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
	public virtual void SetAttribute (MonoTouch.Foundation.NSObject value, MonoTouch.Foundation.NSString attribuetKey);
}
```

### New Type MonoTouch.SceneKit.SCNLightingModel

```
public static class SCNLightingModel {
	// properties
	public static MonoTouch.Foundation.NSString Blinn { get; }
	public static MonoTouch.Foundation.NSString Constant { get; }
	public static MonoTouch.Foundation.NSString Lambert { get; }
	public static MonoTouch.Foundation.NSString Phong { get; }
}
```

### New Type MonoTouch.SceneKit.SCNLightType

```
public static class SCNLightType {
	// properties
	public static MonoTouch.Foundation.NSString Ambient { get; }
	public static MonoTouch.Foundation.NSString Directional { get; }
	public static MonoTouch.Foundation.NSString Omni { get; }
	public static MonoTouch.Foundation.NSString Spot { get; }
}
```

### New Type MonoTouch.SceneKit.SCNLookAtConstraint

```
public class SCNLookAtConstraint : MonoTouch.SceneKit.SCNConstraint, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNLookAtConstraint (MonoTouch.Foundation.NSCoder coder);
	public SCNLookAtConstraint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNLookAtConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool GimbalLockEnabled { get; set; }
	public virtual SCNNode Target { get; }
	// methods
	public static SCNLookAtConstraint Create (SCNNode target);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNMaterial

```
public class SCNMaterial : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNMaterial ();
	public SCNMaterial (MonoTouch.Foundation.NSCoder coder);
	public SCNMaterial (MonoTouch.Foundation.NSObjectFlag t);
	public SCNMaterial (System.IntPtr handle);
	// properties
	public virtual SCNMaterialProperty Ambient { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNCullMode CullMode { get; set; }
	public virtual SCNMaterialProperty Diffuse { get; }
	public virtual bool DoubleSided { get; set; }
	public virtual SCNMaterialProperty Emission { get; }
	public virtual float FresnelExponent { get; set; }
	public virtual MonoTouch.Foundation.NSString LightingModelName { get; set; }
	public virtual bool LitPerPixel { get; set; }
	public virtual bool LocksAmbientWithDiffuse { get; set; }
	public virtual SCNMaterialProperty Multiply { get; }
	public virtual string Name { get; set; }
	public virtual SCNMaterialProperty Normal { get; }
	public virtual SCNProgram Program { get; set; }
	public virtual bool ReadsFromDepthBuffer { get; set; }
	public virtual SCNMaterialProperty Reflective { get; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual float Shininess { get; set; }
	public virtual SCNMaterialProperty Specular { get; }
	public virtual float Transparency { get; set; }
	public virtual SCNTransparencyMode TransparencyMode { get; set; }
	public virtual SCNMaterialProperty Transparent { get; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
	public virtual bool WritesToDepthBuffer { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNMaterial Create ();
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNMaterialProperty

```
public class SCNMaterialProperty : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNMaterialProperty (MonoTouch.Foundation.NSCoder coder);
	public SCNMaterialProperty (MonoTouch.Foundation.NSObjectFlag t);
	public SCNMaterialProperty (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSObject BorderColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public MonoTouch.UIKit.UIColor ContentColor { get; set; }
	public MonoTouch.UIKit.UIImage ContentImage { get; set; }
	public MonoTouch.UIKit.UIImage[] ContentImageCube { get; set; }
	public MonoTouch.CoreAnimation.CALayer ContentLayer { get; set; }
	public MonoTouch.Foundation.NSString ContentPath { get; set; }
	public virtual MonoTouch.Foundation.NSObject Contents { get; set; }
	public MonoTouch.SpriteKit.SKScene ContentScene { get; set; }
	public virtual SCNMatrix4 ContentsTransform { get; set; }
	public MonoTouch.SpriteKit.SKTexture ContentTexture { get; set; }
	public MonoTouch.Foundation.NSUrl ContentUrl { get; set; }
	public virtual float Intensity { get; set; }
	public virtual SCNFilterMode MagnificationFilter { get; set; }
	public virtual int MappingChannel { get; set; }
	public virtual float MaxAnisotropy { get; set; }
	public virtual SCNFilterMode MinificationFilter { get; set; }
	public virtual SCNFilterMode MipFilter { get; set; }
	public virtual SCNWrapMode WrapS { get; set; }
	public virtual SCNWrapMode WrapT { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public static SCNMaterialProperty Create (MonoTouch.Foundation.NSObject contents);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNMatrix4

```
[Serializable]
public struct SCNMatrix4, System.IEquatable<SCNMatrix4> {
	// constructors
	public SCNMatrix4 (SCNVector4 row0, SCNVector4 row1, SCNVector4 row2, SCNVector4 row3);
	public SCNMatrix4 (float m00, float m01, float m02, float m03, float m10, float m11, float m12, float m13, float m20, float m21, float m22, float m23, float m30, float m31, float m32, float m33);
	public SCNMatrix4 (MonoTouch.CoreAnimation.CATransform3D transform);
	// fields
	public static SCNMatrix4 Identity;
	public SCNVector4 Row0;
	public SCNVector4 Row1;
	public SCNVector4 Row2;
	public SCNVector4 Row3;
	// properties
	public SCNVector4 Column0 { get; }
	public SCNVector4 Column1 { get; }
	public SCNVector4 Column2 { get; }
	public SCNVector4 Column3 { get; }
	public float Determinant { get; }
	public float M11 { get; set; }
	public float M12 { get; set; }
	public float M13 { get; set; }
	public float M14 { get; set; }
	public float M21 { get; set; }
	public float M22 { get; set; }
	public float M23 { get; set; }
	public float M24 { get; set; }
	public float M31 { get; set; }
	public float M32 { get; set; }
	public float M33 { get; set; }
	public float M34 { get; set; }
	public float M41 { get; set; }
	public float M42 { get; set; }
	public float M43 { get; set; }
	public float M44 { get; set; }
	// methods
	public static void CreateFromAxisAngle (OpenTK.Vector3d axis, double angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateFromAxisAngle (SCNVector3 axis, float angle);
	public static void CreateFromAxisAngle (SCNVector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateFromAxisAngle (OpenTK.Vector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateOrthographic (float width, float height, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographic (float width, float height, float zNear, float zFar);
	public static void CreateOrthographicOffCenter (float left, float right, float bottom, float top, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographicOffCenter (float left, float right, float bottom, float top, float zNear, float zFar);
	public static void CreatePerspectiveFieldOfView (float fovy, float aspect, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveFieldOfView (float fovy, float aspect, float zNear, float zFar);
	public static void CreatePerspectiveOffCenter (float left, float right, float bottom, float top, float zNear, float zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveOffCenter (float left, float right, float bottom, float top, float zNear, float zFar);
	public static void CreateRotationX (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationX (float angle);
	public static SCNMatrix4 CreateRotationY (float angle);
	public static void CreateRotationY (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationZ (float angle);
	public static void CreateRotationZ (float angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateTranslation (SCNVector3 vector);
	public static SCNMatrix4 CreateTranslation (float x, float y, float z);
	public static void CreateTranslation (float x, float y, float z, out SCNMatrix4 result);
	public static void CreateTranslation (ref SCNVector3 vector, out SCNMatrix4 result);
	public virtual bool Equals (SCNMatrix4 other);
	public override bool Equals (object obj);

	[Obsolete ("Use CreatePerspectiveOffCenter instead.")]
	public static SCNMatrix4 Frustum (float left, float right, float bottom, float top, float near, float far);
	public override int GetHashCode ();
	public static SCNMatrix4 Invert (SCNMatrix4 mat);
	public void Invert ();
	public static SCNMatrix4 LookAt (SCNVector3 eye, SCNVector3 target, SCNVector3 up);
	public static SCNMatrix4 LookAt (float eyeX, float eyeY, float eyeZ, float targetX, float targetY, float targetZ, float upX, float upY, float upZ);
	public static SCNMatrix4 Mult (SCNMatrix4 left, SCNMatrix4 right);
	public static void Mult (ref SCNMatrix4 left, ref SCNMatrix4 right, out SCNMatrix4 result);
	public static bool op_Equality (SCNMatrix4 left, SCNMatrix4 right);
	public static bool op_Inequality (SCNMatrix4 left, SCNMatrix4 right);
	public static SCNMatrix4 op_Multiply (SCNMatrix4 left, SCNMatrix4 right);

	[Obsolete ("Use CreatePerspectiveFieldOfView instead.")]
	public static SCNMatrix4 Perspective (float fovy, float aspect, float near, float far);

	[Obsolete ("Use CreateFromAxisAngle instead.")]
	public static SCNMatrix4 Rotate (SCNVector3 axis, float angle);
	public static SCNMatrix4 Rotate (OpenTK.Quaternion q);
	public static SCNMatrix4 Rotate (OpenTK.Quaterniond q);

	[Obsolete ("Use CreateRotationX instead.")]
	public static SCNMatrix4 RotateX (float angle);

	[Obsolete ("Use CreateRotationY instead.")]
	public static SCNMatrix4 RotateY (float angle);

	[Obsolete ("Use CreateRotationZ instead.")]
	public static SCNMatrix4 RotateZ (float angle);
	public static SCNMatrix4 Scale (float x, float y, float z);
	public static SCNMatrix4 Scale (SCNVector3 scale);
	public static SCNMatrix4 Scale (float scale);
	public override string ToString ();

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (SCNVector3 trans);

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (float x, float y, float z);
	public static void Transpose (ref SCNMatrix4 mat, out SCNMatrix4 result);
	public void Transpose ();
	public static SCNMatrix4 Transpose (SCNMatrix4 mat);
}
```

### New Type MonoTouch.SceneKit.SCNMorpher

```
public class SCNMorpher : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNMorpher ();
	public SCNMorpher (MonoTouch.Foundation.NSCoder coder);
	public SCNMorpher (MonoTouch.Foundation.NSObjectFlag t);
	public SCNMorpher (System.IntPtr handle);
	// properties
	public virtual SCNMorpherCalculationMode CalculationMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNGeometry[] Targets { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual float GetWeight (uint targetIndex);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
	public virtual void SetWeight (float weight, uint targetIndex);
}
```

### New Type MonoTouch.SceneKit.SCNMorpherCalculationMode

```
[Serializable]
public enum SCNMorpherCalculationMode {
	Additive = 1,
	Normalized = 0,
}
```

### New Type MonoTouch.SceneKit.SCNNode

```
public class SCNNode : MonoTouch.Foundation.NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SCNNode>, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNActionable, ISCNAnimatable, ISCNBoundingVolume, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNNode ();
	public SCNNode (MonoTouch.Foundation.NSCoder coder);
	public SCNNode (MonoTouch.Foundation.NSObjectFlag t);
	public SCNNode (System.IntPtr handle);
	// properties
	public virtual SCNCamera Camera { get; set; }
	public virtual bool CastsShadow { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual SCNNode[] ChildNodes { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNConstraint[] Constraints { get; set; }
	public virtual SCNVector3 EulerAngles { get; set; }
	public virtual MonoTouch.CoreImage.CIFilter[] Filters { get; set; }
	public virtual SCNGeometry Geometry { get; set; }
	public virtual bool Hidden { get; set; }
	public virtual SCNLight Light { get; set; }
	public virtual SCNMorpher Morpher { get; set; }
	public virtual string Name { get; set; }
	public virtual float Opacity { get; set; }
	public virtual SCNQuaternion Orientation { get; set; }
	public virtual SCNNode ParentNode { get; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsBody PhysicsBody { get; set; }
	public virtual SCNPhysicsField PhysicsField { get; set; }
	public virtual SCNMatrix4 Pivot { get; set; }
	public virtual SCNVector3 Position { get; set; }
	public virtual SCNNode PresentationNode { get; }
	public SCNNodeRendererDelegate RendererDelegate { get; set; }
	public virtual int RenderingOrder { get; set; }
	public virtual SCNVector4 Rotation { get; set; }
	public virtual SCNVector3 Scale { get; set; }
	public virtual SCNSkinner Skinner { get; set; }
	public virtual SCNMatrix4 Transform { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakRendererDelegate { get; set; }
	public virtual SCNMatrix4 WorldTransform { get; }
	// methods
	public void Add (SCNNode node);
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual void AddChildNode (SCNNode child);
	public void AddNodes (SCNNode[] nodes);
	public virtual void AddParticleSystem (SCNParticleSystem system);
	public virtual SCNNode Clone ();
	public virtual SCNVector3 ConvertPositionFromNode (SCNVector3 position, SCNNode node);
	public virtual SCNVector3 ConvertPositionToNode (SCNVector3 position, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformFromNode (SCNMatrix4 transform, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformToNode (SCNMatrix4 transform, SCNNode node);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNNode Create ();
	protected override void Dispose (bool disposing);
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);
	public virtual SCNNode FindChildNode (string childName, bool recursively);
	public virtual SCNNode[] FindNodes (SCNNodePredicate predicate);
	public virtual SCNNode FlattenedClone ();
	public static SCNNode FromGeometry (SCNGeometry geometry);
	public virtual SCNAction GetAction (string key);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
	public virtual System.Collections.Generic.IEnumerator<SCNNode> GetEnumerator ();
	public virtual bool HasActions ();
	public virtual SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, SCNHitTestOptions options);
	public virtual void InsertChildNode (SCNNode child, int index);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveFromParentNode ();
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual void ReplaceChildNode (SCNNode child, SCNNode child2);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
}
```

### New Type MonoTouch.SceneKit.SCNNodePredicate

```
public sealed delegate SCNNodePredicate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNNodePredicate (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, out bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual bool Invoke (SCNNode node, out bool stop);
}
```

### New Type MonoTouch.SceneKit.SCNNodeRendererDelegate

```
public class SCNNodeRendererDelegate : MonoTouch.Foundation.NSObject, ISCNNodeRendererDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNNodeRendererDelegate ();
	public SCNNodeRendererDelegate (MonoTouch.Foundation.NSCoder coder);
	public SCNNodeRendererDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SCNNodeRendererDelegate (System.IntPtr handle);
	// methods
	public virtual void Render (SCNNode node, SCNRenderer renderer, MonoTouch.Foundation.NSDictionary arguments);
}
```

### New Type MonoTouch.SceneKit.SCNNodeRendererDelegate_Extensions

```
public static class SCNNodeRendererDelegate_Extensions {
	// methods
	public static void Render (ISCNNodeRendererDelegate This, SCNNode node, SCNRenderer renderer, MonoTouch.Foundation.NSDictionary arguments);
}
```

### New Type MonoTouch.SceneKit.SCNParticleBirthDirection

```
[Serializable]
public enum SCNParticleBirthDirection {
	Constant = 0,
	Random = 2,
	SurfaceNormal = 1,
}
```

### New Type MonoTouch.SceneKit.SCNParticleBirthLocation

```
[Serializable]
public enum SCNParticleBirthLocation {
	Surface = 0,
	Vertex = 2,
	Volume = 1,
}
```

### New Type MonoTouch.SceneKit.SCNParticleBlendMode

```
[Serializable]
public enum SCNParticleBlendMode {
	Additive = 0,
	Alpha = 4,
	Multiply = 2,
	Replace = 5,
	Screen = 3,
	Subtract = 1,
}
```

### New Type MonoTouch.SceneKit.SCNParticleEvent

```
[Serializable]
public enum SCNParticleEvent {
	Birth = 0,
	Collision = 2,
	Death = 1,
}
```

### New Type MonoTouch.SceneKit.SCNParticleEventHandler

```
public sealed delegate SCNParticleEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, int count, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, int count);
}
```

### New Type MonoTouch.SceneKit.SCNParticleImageSequenceAnimationMode

```
[Serializable]
public enum SCNParticleImageSequenceAnimationMode {
	AutoReverse = 2,
	Clamp = 1,
	Repeat = 0,
}
```

### New Type MonoTouch.SceneKit.SCNParticleInputMode

```
[Serializable]
public enum SCNParticleInputMode {
	OverDistance = 1,
	OverLife = 0,
	OverOtherProperty = 2,
}
```

### New Type MonoTouch.SceneKit.SCNParticleModifierHandler

```
public sealed delegate SCNParticleModifierHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleModifierHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, int start, int end, float deltaTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, int start, int end, float deltaTime);
}
```

### New Type MonoTouch.SceneKit.SCNParticleModifierStage

```
[Serializable]
public enum SCNParticleModifierStage {
	PostCollision = 3,
	PostDynamics = 1,
	PreCollision = 2,
	PreDynamics = 0,
}
```

### New Type MonoTouch.SceneKit.SCNParticleOrientationMode

```
[Serializable]
public enum SCNParticleOrientationMode {
	BillboardScreenAligned = 0,
	BillboardViewAligned = 1,
	BillboardYAligned = 3,
	Free = 2,
}
```

### New Type MonoTouch.SceneKit.SCNParticlePropertyController

```
public class SCNParticlePropertyController : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticlePropertyController (MonoTouch.Foundation.NSCoder coder);
	public SCNParticlePropertyController (MonoTouch.Foundation.NSObjectFlag t);
	public SCNParticlePropertyController (System.IntPtr handle);
	// properties
	public virtual MonoTouch.CoreAnimation.CAAnimation Animation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float InputBias { get; set; }
	public virtual SCNParticleInputMode InputMode { get; set; }
	public virtual SCNNode InputOrigin { get; set; }
	public virtual MonoTouch.Foundation.NSString InputProperty { get; set; }
	public virtual float InputScale { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNParticlePropertyController Create (MonoTouch.CoreAnimation.CAAnimation animation);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNParticleSortingMode

```
[Serializable]
public enum SCNParticleSortingMode {
	Distance = 2,
	None = 0,
	OldestFirst = 3,
	ProjectedDepth = 1,
	YoungestFirst = 4,
}
```

### New Type MonoTouch.SceneKit.SCNParticleSystem

```
public class SCNParticleSystem : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticleSystem (MonoTouch.Foundation.NSCoder coder);
	public SCNParticleSystem (MonoTouch.Foundation.NSObjectFlag t);
	public SCNParticleSystem (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Acceleration { get; set; }
	public virtual bool AffectedByGravity { get; set; }
	public virtual bool AffectedByPhysicsFields { get; set; }
	public virtual SCNParticleBirthDirection BirthDirection { get; set; }
	public virtual SCNParticleBirthLocation BirthLocation { get; set; }
	public virtual float BirthRate { get; set; }
	public virtual float BirthRateVariation { get; set; }
	public virtual bool BlackPassEnabled { get; set; }
	public virtual SCNParticleBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNNode[] ColliderNodes { get; set; }
	public virtual float DampingFactor { get; set; }
	public virtual float EmissionDuration { get; set; }
	public virtual float EmissionDurationVariation { get; set; }
	public virtual SCNGeometry EmitterShape { get; set; }
	public virtual SCNVector3 EmittingDirection { get; set; }
	public virtual float FresnelExponent { get; set; }
	public virtual float IdleDuration { get; set; }
	public virtual float IdleDurationVariation { get; set; }
	public virtual SCNParticleImageSequenceAnimationMode ImageSequenceAnimationMode { get; set; }
	public virtual uint ImageSequenceColumnCount { get; set; }
	public virtual float ImageSequenceFrameRate { get; set; }
	public virtual float ImageSequenceFrameRateVariation { get; set; }
	public virtual float ImageSequenceInitialFrame { get; set; }
	public virtual float ImageSequenceInitialFrameVariation { get; set; }
	public virtual uint ImageSequenceRowCount { get; set; }
	public virtual bool LightingEnabled { get; set; }
	public virtual bool Local { get; set; }
	public virtual bool Loops { get; set; }
	public virtual SCNParticleOrientationMode OrientationMode { get; set; }
	public virtual float ParticleAngle { get; set; }
	public virtual float ParticleAngleVariation { get; set; }
	public virtual float ParticleAngularVelocity { get; set; }
	public virtual float ParticleAngularVelocityVariation { get; set; }
	public virtual float ParticleBounce { get; set; }
	public virtual float ParticleBounceVariation { get; set; }
	public virtual float ParticleCharge { get; set; }
	public virtual float ParticleChargeVariation { get; set; }
	public virtual MonoTouch.UIKit.UIColor ParticleColor { get; set; }
	public virtual SCNVector4 ParticleColorVariation { get; set; }
	public virtual bool ParticleDiesOnCollision { get; set; }
	public virtual float ParticleFriction { get; set; }
	public virtual float ParticleFrictionVariation { get; set; }
	public virtual MonoTouch.Foundation.NSObject ParticleImage { get; set; }
	public virtual float ParticleLifeSpan { get; set; }
	public virtual float ParticleLifeSpanVariation { get; set; }
	public virtual float ParticleMass { get; set; }
	public virtual float ParticleMassVariation { get; set; }
	public virtual float ParticleSize { get; set; }
	public virtual float ParticleSizeVariation { get; set; }
	public virtual float ParticleVelocity { get; set; }
	public virtual float ParticleVelocityVariation { get; set; }
	public virtual SCNParticleSortingMode SortingMode { get; set; }
	public virtual float SpeedFactor { get; set; }
	public virtual float SpreadingAngle { get; set; }
	public virtual float StretchFactor { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnCollision { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnDying { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnLiving { get; set; }
	public virtual float WarmupDuration { get; set; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual void AddModifier (MonoTouch.Foundation.NSString[] properties, SCNParticleModifierStage stage, SCNParticleModifierHandler handler);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNParticleSystem Create ();
	public static SCNParticleSystem Create (string name, string directory);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleEvent (SCNParticleEvent evnt, MonoTouch.Foundation.NSString[] properties, SCNParticleEventHandler handler);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAllModifiers ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void RemoveModifiers (SCNParticleModifierStage stage);
	public virtual void Reset ();
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsBallSocketJoint

```
public class SCNPhysicsBallSocketJoint : MonoTouch.SceneKit.SCNPhysicsBehavior, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBallSocketJoint (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsBallSocketJoint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsBallSocketJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNPhysicsBallSocketJoint Create (SCNPhysicsBody bodyA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 anchorB);
	public static SCNPhysicsBallSocketJoint Create (SCNPhysicsBody body, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsBehavior

```
public class SCNPhysicsBehavior : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBehavior (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsBehavior (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsBody

```
public class SCNPhysicsBody : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBody (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsBody (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsBody (System.IntPtr handle);
	// properties
	public virtual bool AllowsResting { get; set; }
	public virtual float AngularDamping { get; set; }
	public virtual SCNVector4 AngularVelocity { get; set; }
	public virtual SCNVector3 AngularVelocityFactor { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float Charge { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint CollisionBitMask { get; set; }
	public virtual float Damping { get; set; }
	public virtual float Friction { get; set; }
	public virtual bool IsResting { get; }
	public virtual float Mass { get; set; }
	public virtual SCNPhysicsShape PhysicsShape { get; set; }
	public virtual float Restitution { get; set; }
	public virtual float RollingFriction { get; set; }
	public virtual SCNPhysicsBodyType Type { get; set; }
	public virtual SCNVector3 Velocity { get; set; }
	public virtual SCNVector3 VelocityFactor { get; set; }
	// methods
	public virtual void ApplyForce (SCNVector3 direction, bool impulse);
	public virtual void ApplyForce (SCNVector3 direction, SCNVector3 position, bool impulse);
	public virtual void ApplyTorque (SCNVector4 torque, bool impulse);
	public virtual void ClearAllForces ();
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNPhysicsBody CreateBody (SCNPhysicsBodyType type, SCNPhysicsShape shape);
	public static SCNPhysicsBody CreateDynamicBody ();
	public static SCNPhysicsBody CreateKinematicBody ();
	public static SCNPhysicsBody CreateStaticBody ();
	protected override void Dispose (bool disposing);
	public virtual void ResetTransform ();
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsBodyType

```
[Serializable]
public enum SCNPhysicsBodyType {
	Dynamic = 1,
	Kinematic = 2,
	Static = 0,
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsContact

```
public class SCNPhysicsContact : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContact (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsContact (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsContact (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float CollisionImpulse { get; }
	public virtual SCNVector3 ContactNormal { get; }
	public virtual SCNVector3 ContactPoint { get; }
	public virtual SCNNode NodeA { get; }
	public virtual SCNNode NodeB { get; }
	public virtual float PenetrationDistance { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsContactDelegate

```
public class SCNPhysicsContactDelegate : MonoTouch.Foundation.NSObject, ISCNPhysicsContactDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContactDelegate ();
	public SCNPhysicsContactDelegate (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsContactDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidEndContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidUpdateContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsContactDelegate_Extensions

```
public static class SCNPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidEndContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidUpdateContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsContactEventArgs

```
public class SCNPhysicsContactEventArgs : System.EventArgs {
	// constructors
	public SCNPhysicsContactEventArgs (SCNPhysicsContact contact);
	// properties
	public SCNPhysicsContact Contact { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsField

```
public class SCNPhysicsField : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsField (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsField (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsField (System.IntPtr handle);
	// properties
	public virtual bool Active { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 Direction { get; set; }
	public virtual bool Exclusive { get; set; }
	public virtual float FalloffExponent { get; set; }
	public virtual SCNVector3 HalfExtent { get; set; }
	public virtual float MinimumDistance { get; set; }
	public virtual SCNVector3 Offset { get; set; }
	public virtual SCNPhysicsFieldScope Scope { get; set; }
	public virtual float Strength { get; set; }
	public virtual bool UsesEllipsoidalExtent { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNPhysicsField CreateDragField ();
	public static SCNPhysicsField CreateElectricField ();
	public static SCNPhysicsField CreateLinearGravityField ();
	public static SCNPhysicsField CreateMagneticField ();
	public static SCNPhysicsField CreateNoiseField (float smoothness, float speed);
	public static SCNPhysicsField CreateRadialGravityField ();
	public static SCNPhysicsField CreateSpringField ();
	public static SCNPhysicsField CreateTurbulenceField (float smoothness, float speed);
	public static SCNPhysicsField CreateVortexField ();
	public static SCNPhysicsField CustomField (SCNFieldForceEvaluator evaluator);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsFieldScope

```
[Serializable]
public enum SCNPhysicsFieldScope {
	InsideExtent = 0,
	OutsideExtent = 1,
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsHingeJoint

```
public class SCNPhysicsHingeJoint : MonoTouch.SceneKit.SCNPhysicsBehavior, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsHingeJoint (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsHingeJoint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsHingeJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNVector3 AxisA { get; set; }
	public virtual SCNVector3 AxisB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNPhysicsHingeJoint Create (SCNPhysicsBody bodyA, SCNVector3 axisA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 axisB, SCNVector3 anchorB);
	public static SCNPhysicsHingeJoint Create (SCNPhysicsBody body, SCNVector3 axis, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsSearchMode

```
[Serializable]
public enum SCNPhysicsSearchMode {
	All = 2,
	Any = 0,
	Closest = 1,
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsShape

```
public class SCNPhysicsShape : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsShape (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsShape (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsShape (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNPhysicsShape Create (SCNPhysicsShape[] shapes, SCNVector3[] transforms);
	public static SCNPhysicsShape Create (SCNGeometry geometry, MonoTouch.Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeOptions options);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeOptions options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNNode node, MonoTouch.Foundation.NSDictionary options);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsShapeOptions

```
public class SCNPhysicsShapeOptions {
	// constructors
	public SCNPhysicsShapeOptions ();
	// properties
	public bool? KeepAsCompound { get; set; }
	public SCNVector3? Scale { get; set; }
	public SCNPhysicsShapeType? ShapeType { get; set; }
	// methods
	public MonoTouch.Foundation.NSDictionary ToDictionary ();
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsShapeOptionsKeys

```
public static class SCNPhysicsShapeOptionsKeys {
	// properties
	public static MonoTouch.Foundation.NSString KeepAsCompound { get; }
	public static MonoTouch.Foundation.NSString Scale { get; }
	public static MonoTouch.Foundation.NSString Type { get; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsShapeOptionsTypes

```
public static class SCNPhysicsShapeOptionsTypes {
	// properties
	public static MonoTouch.Foundation.NSString BoundingBox { get; }
	public static MonoTouch.Foundation.NSString ConcavePolyhedron { get; }
	public static MonoTouch.Foundation.NSString ConvexHull { get; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsShapeType

```
[Serializable]
public enum SCNPhysicsShapeType {
	BoundingBox = 1,
	ConcavePolyhedron = 2,
	ConvexHull = 0,
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsSliderJoint

```
public class SCNPhysicsSliderJoint : MonoTouch.SceneKit.SCNPhysicsBehavior, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsSliderJoint (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsSliderJoint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsSliderJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNVector3 AxisA { get; set; }
	public virtual SCNVector3 AxisB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float MaximumAngularLimit { get; set; }
	public virtual float MaximumLinearLimit { get; set; }
	public virtual float MinimumAngularLimit { get; set; }
	public virtual float MinimumLinearLimit { get; set; }
	public virtual float MotorMaximumForce { get; set; }
	public virtual float MotorMaximumTorque { get; set; }
	public virtual float MotorTargetAngularVelocity { get; set; }
	public virtual float MotorTargetLinearVelocity { get; set; }
	// methods
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody bodyA, SCNVector3 axisA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 axisB, SCNVector3 anchorB);
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody body, SCNVector3 axis, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsTest

```
public class SCNPhysicsTest : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public SCNPhysicsTest ();
	public SCNPhysicsTest (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public bool? BackfaceCulling { get; set; }
	public uint? CollisionBitMask { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsTestKeys

```
public static class SCNPhysicsTestKeys {
	// properties
	public static MonoTouch.Foundation.NSString BackfaceCullingKey { get; }
	public static MonoTouch.Foundation.NSString CollisionBitMaskKey { get; }
	public static MonoTouch.Foundation.NSString SearchModeKey { get; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsTestSearchModeKeys

```
public static class SCNPhysicsTestSearchModeKeys {
	// properties
	public static MonoTouch.Foundation.NSString All { get; }
	public static MonoTouch.Foundation.NSString Any { get; }
	public static MonoTouch.Foundation.NSString Closest { get; }
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsVehicle

```
public class SCNPhysicsVehicle : MonoTouch.SceneKit.SCNPhysicsBehavior, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicle (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsVehicle (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsVehicle (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBody ChassisBody { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float SpeedInKilometersPerHour { get; }
	public virtual SCNPhysicsVehicleWheel[] Wheels { get; }
	// methods
	public virtual void ApplyBrakingForce (float value, int index);
	public virtual void ApplyEngineForce (float value, int index);
	public static SCNPhysicsVehicle Create (SCNPhysicsBody chassisBody, SCNPhysicsVehicleWheel[] wheels);
	protected override void Dispose (bool disposing);
	public virtual void SetSteeringAngle (float value, int index);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsVehicleWheel

```
public class SCNPhysicsVehicleWheel : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicleWheel (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsVehicleWheel (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsVehicleWheel (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Axle { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 ConnectionPosition { get; set; }
	public virtual float FrictionSlip { get; set; }
	public virtual float MaximumSuspensionForce { get; set; }
	public virtual float MaximumSuspensionTravel { get; set; }
	public virtual SCNNode Node { get; }
	public virtual float Radius { get; set; }
	public virtual SCNVector3 SteeringAxis { get; set; }
	public virtual float SuspensionCompression { get; set; }
	public virtual float SuspensionDamping { get; set; }
	public virtual float SuspensionRestLength { get; set; }
	public virtual float SuspensionStiffness { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNPhysicsVehicleWheel Create (SCNNode node);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNPhysicsWorld

```
public class SCNPhysicsWorld : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsWorld (MonoTouch.Foundation.NSCoder coder);
	public SCNPhysicsWorld (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPhysicsWorld (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBehavior[] AllBehaviors { get; }
	public override System.IntPtr ClassHandle { get; }
	public SCNPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual SCNVector3 Gravity { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeStep { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidBeginContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidEndContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidUpdateContact;
	// methods
	public virtual void AddBehavior (SCNPhysicsBehavior behavior);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, MonoTouch.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, MonoTouch.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, SCNPhysicsTest options);
	public SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, MonoTouch.Foundation.NSDictionary options);
	protected override void Dispose (bool disposing);
	public virtual SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, SCNPhysicsTest options);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (SCNPhysicsBehavior behavior);
	public virtual void UpdateCollisionPairs ();
}
```

### New Type MonoTouch.SceneKit.SCNPlane

```
public class SCNPlane : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPlane ();
	public SCNPlane (MonoTouch.Foundation.NSCoder coder);
	public SCNPlane (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPlane (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float CornerRadius { get; set; }
	public virtual int CornerSegmentCount { get; set; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual float Width { get; set; }
	public virtual int WidthSegmentCount { get; set; }
	// methods
	public static SCNPlane Create (float width, float height);
}
```

### New Type MonoTouch.SceneKit.SCNProgram

```
public class SCNProgram : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNProgram ();
	public SCNProgram (MonoTouch.Foundation.NSCoder coder);
	public SCNProgram (MonoTouch.Foundation.NSObjectFlag t);
	public SCNProgram (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public SCNProgramDelegate Delegate { get; set; }
	public virtual string FragmentShader { get; set; }
	public static MonoTouch.Foundation.NSString MappingChannelKey { get; }
	public virtual bool Opaque { get; set; }
	public virtual string VertexShader { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNProgram Create ();
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSString GetSemanticForSymbol (string symbol);
	public virtual void SetSemantic (MonoTouch.Foundation.NSString geometrySourceSemantic, string symbol, MonoTouch.Foundation.NSDictionary options);
	public void SetSemantic (MonoTouch.Foundation.NSString geometrySourceSemantic, string symbol, SCNProgramSemanticOptions options);
}
```

### New Type MonoTouch.SceneKit.SCNProgramDelegate

```
public class SCNProgramDelegate : MonoTouch.Foundation.NSObject, ISCNProgramDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNProgramDelegate ();
	public SCNProgramDelegate (MonoTouch.Foundation.NSCoder coder);
	public SCNProgramDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SCNProgramDelegate (System.IntPtr handle);
	// methods
	public virtual bool BindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public virtual void HandleError (SCNProgram program, MonoTouch.Foundation.NSError error);
	public virtual bool IsProgramOpaque (SCNProgram program);
	public virtual void UnbindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
}
```

### New Type MonoTouch.SceneKit.SCNProgramDelegate_Extensions

```
public static class SCNProgramDelegate_Extensions {
	// methods
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public static void HandleError (ISCNProgramDelegate This, SCNProgram program, MonoTouch.Foundation.NSError error);
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
}
```

### New Type MonoTouch.SceneKit.SCNProgramSemanticOptions

```
public class SCNProgramSemanticOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public SCNProgramSemanticOptions ();
	public SCNProgramSemanticOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public uint? MappingChannel { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNPyramid

```
public class SCNPyramid : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPyramid ();
	public SCNPyramid (MonoTouch.Foundation.NSCoder coder);
	public SCNPyramid (MonoTouch.Foundation.NSObjectFlag t);
	public SCNPyramid (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual float Length { get; set; }
	public virtual int LengthSegmentCount { get; set; }
	public virtual float Width { get; set; }
	public virtual int WidthSegmentCount { get; set; }
	// methods
	public static SCNPyramid Create (float width, float height, float length);
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

### New Type MonoTouch.SceneKit.SCNRenderer

```
public class SCNRenderer : MonoTouch.Foundation.NSObject, ISCNSceneRenderer, ISCNTechniqueSupport, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNRenderer (MonoTouch.Foundation.NSCoder coder);
	public SCNRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public SCNRenderer (System.IntPtr handle);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.IntPtr Context { get; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual double NextFrameTimeInSeconds { get; }
	public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public virtual SCNScene Scene { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SCNRenderer FromContext (System.IntPtr context, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.Foundation.NSDictionary options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoTouch.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoTouch.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual void Render ();
	public virtual void Render (double timeInSeconds);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
}
```

### New Type MonoTouch.SceneKit.SCNRenderingArguments

```
public static class SCNRenderingArguments {
	// properties
	public static MonoTouch.Foundation.NSString ModelTransform { get; }
	public static MonoTouch.Foundation.NSString ModelViewProjectionTransform { get; }
	public static MonoTouch.Foundation.NSString ModelViewTransform { get; }
	public static MonoTouch.Foundation.NSString NormalTransform { get; }
	public static MonoTouch.Foundation.NSString ProjectionTransform { get; }
	public static MonoTouch.Foundation.NSString ViewTransform { get; }
}
```

### New Type MonoTouch.SceneKit.SCNScene

```
public class SCNScene : MonoTouch.Foundation.NSObject, System.Collections.Generic.IEnumerable<SCNNode>, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, System.Collections.IEnumerable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNScene ();
	public SCNScene (MonoTouch.Foundation.NSCoder coder);
	public SCNScene (MonoTouch.Foundation.NSObjectFlag t);
	public SCNScene (System.IntPtr handle);
	// properties
	public virtual SCNMaterialProperty Background { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoTouch.Foundation.NSString EndTimeAttributeKey { get; }
	public static MonoTouch.Foundation.NSString ExportDestinationUrl { get; }
	public virtual MonoTouch.Foundation.NSObject FogColor { get; set; }
	public virtual float FogDensityExponent { get; set; }
	public virtual float FogEndDistance { get; set; }
	public virtual float FogStartDistance { get; set; }
	public static MonoTouch.Foundation.NSString FrameRateAttributeKey { get; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsWorld PhysicsWorld { get; }
	public virtual SCNNode RootNode { get; }
	public static MonoTouch.Foundation.NSString StartTimeAttributeKey { get; }
	public static MonoTouch.Foundation.NSString UpAxisAttributeKey { get; }
	// methods
	public void Add (SCNNode node);
	public virtual void AddParticleSystem (SCNParticleSystem system, SCNMatrix4 transform);
	public static SCNScene Create ();
	protected override void Dispose (bool disposing);
	public static SCNScene FromFile (string name);
	public static SCNScene FromFile (string name, string directory, SCNSceneLoadingOptions options);
	public static SCNScene FromFile (string name, string directory, MonoTouch.Foundation.NSDictionary options);
	public static SCNScene FromUrl (MonoTouch.Foundation.NSUrl url, SCNSceneLoadingOptions options, out MonoTouch.Foundation.NSError error);
	public static SCNScene FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
	public virtual MonoTouch.Foundation.NSObject GetAttribute (MonoTouch.Foundation.NSString key);
	public virtual System.Collections.Generic.IEnumerator<SCNNode> GetEnumerator ();
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual void SetAttribute (MonoTouch.Foundation.NSObject attribute, MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNSceneLoadingOptions

```
public class SCNSceneLoadingOptions : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public SCNSceneLoadingOptions ();
	public SCNSceneLoadingOptions (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public MonoTouch.Foundation.NSUrl[] AssetDirectoryUrls { get; set; }
	public bool? CheckConsistency { get; set; }
	public bool? ConvertToYUp { get; set; }
	public float? ConvertUnitsToMeters { get; set; }
	public bool? CreateNormalsIfAbsent { get; set; }
	public bool? FlattenScene { get; set; }
	public bool? OverrideAssetUrls { get; set; }
	public bool? StrictConformance { get; set; }
	public bool? UseSafeMode { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNSceneRenderer

```
public abstract class SCNSceneRenderer : MonoTouch.Foundation.NSObject, ISCNSceneRenderer, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneRenderer ();
	public SCNSceneRenderer (MonoTouch.Foundation.NSCoder coder);
	public SCNSceneRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSceneRenderer (System.IntPtr handle);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public virtual System.IntPtr Context { get; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual bool Prepare (MonoTouch.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual void Prepare (MonoTouch.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
}
```

### New Type MonoTouch.SceneKit.SCNSceneRenderer_Extensions

```
public static class SCNSceneRenderer_Extensions {
	// methods
	public static SCNHitTestResult[] HitTest (ISCNSceneRenderer This, System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public static bool IsNodeInsideFrustum (ISCNSceneRenderer This, SCNNode node, SCNNode pointOfView);
	public static bool Prepare (ISCNSceneRenderer This, MonoTouch.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public static void Prepare (ISCNSceneRenderer This, MonoTouch.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public static SCNVector3 ProjectPoint (ISCNSceneRenderer This, SCNVector3 point);
	public static SCNVector3 UnprojectPoint (ISCNSceneRenderer This, SCNVector3 point);
}
```

### New Type MonoTouch.SceneKit.SCNSceneRendererDelegate

```
public class SCNSceneRendererDelegate : MonoTouch.Foundation.NSObject, ISCNSceneRendererDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneRendererDelegate ();
	public SCNSceneRendererDelegate (MonoTouch.Foundation.NSCoder coder);
	public SCNSceneRendererDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSceneRendererDelegate (System.IntPtr handle);
	// methods
	public virtual void DidApplyAnimations (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
}
```

### New Type MonoTouch.SceneKit.SCNSceneRendererDelegate_Extensions

```
public static class SCNSceneRendererDelegate_Extensions {
	// methods
	public static void DidApplyAnimations (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void DidRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public static void DidSimulatePhysics (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void Update (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void WillRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
}
```

### New Type MonoTouch.SceneKit.SCNSceneSource

```
public class SCNSceneSource : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneSource (MonoTouch.Foundation.NSCoder coder);
	public SCNSceneSource (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSceneSource (System.IntPtr handle);
	public SCNSceneSource (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
	public SCNSceneSource (MonoTouch.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNSceneSource (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary options);
	public SCNSceneSource (MonoTouch.Foundation.NSData data, SCNSceneLoadingOptions options);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSData Data { get; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSObject[] EntriesPassingTest (SCNSceneSourceFilter predicate);
	public static SCNSceneSource FromData (MonoTouch.Foundation.NSData data, SCNSceneLoadingOptions options);
	public static SCNSceneSource FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary options);
	public static SCNSceneSource FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
	public SCNSceneSource FromUrl (MonoTouch.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public virtual MonoTouch.Foundation.NSObject GetEntryWithIdentifier (string uid, MonoTouch.ObjCRuntime.Class entryClass);
	public virtual MonoTouch.Foundation.NSObject GetProperty (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject[] IdentifiersOfEntriesWithClass (MonoTouch.ObjCRuntime.Class entryClass);
	public virtual SCNScene SceneFromOptions (MonoTouch.Foundation.NSDictionary options, SCNSceneSourceStatusHandler statusHandler);
	public SCNScene SceneFromOptions (SCNSceneLoadingOptions options, SCNSceneSourceStatusHandler statusHandler);
	public virtual SCNScene SceneWithOption (MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
	public SCNScene SceneWithOption (SCNSceneLoadingOptions options, out MonoTouch.Foundation.NSError error);
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

### New Type MonoTouch.SceneKit.SCNSceneSourceLoadErrors

```
public static class SCNSceneSourceLoadErrors {
	// properties
	public static MonoTouch.Foundation.NSString ConsistencyElementIDErrorKey { get; }
	public static MonoTouch.Foundation.NSString ConsistencyElementTypeErrorKey { get; }
	public static MonoTouch.Foundation.NSString ConsistencyLineNumberErrorKey { get; }
	public static MonoTouch.Foundation.NSString DetailedErrorsKey { get; }
}
```

### New Type MonoTouch.SceneKit.SCNSceneSourceLoading

```
public static class SCNSceneSourceLoading {
	// properties
	public static MonoTouch.Foundation.NSString AnimationImportPolicyDoNotPlay { get; }
	public static MonoTouch.Foundation.NSString AnimationImportPolicyKey { get; }
	public static MonoTouch.Foundation.NSString AnimationImportPolicyPlay { get; }
	public static MonoTouch.Foundation.NSString AnimationImportPolicyPlayRepeatedly { get; }
	public static MonoTouch.Foundation.NSString AnimationImportPolicyPlayUsingSceneTimeBase { get; }
	public static MonoTouch.Foundation.NSString AssetDirectoryUrlsKey { get; }
	public static MonoTouch.Foundation.NSString CheckConsistencyKey { get; }
	public static MonoTouch.Foundation.NSString ConvertToYUpKey { get; }
	public static MonoTouch.Foundation.NSString ConvertUnitsToMetersKey { get; }
	public static MonoTouch.Foundation.NSString CreateNormalsIfAbsentKey { get; }
	public static MonoTouch.Foundation.NSString FlattenSceneKey { get; }
	public static MonoTouch.Foundation.NSString OverrideAssetUrlsKey { get; }
	public static MonoTouch.Foundation.NSString StrictConformanceKey { get; }
	public static MonoTouch.Foundation.NSString UseSafeModeKey { get; }
}
```

### New Type MonoTouch.SceneKit.SCNSceneSourceProperties

```
public static class SCNSceneSourceProperties {
	// properties
	public static MonoTouch.Foundation.NSString AssetContributorsKey { get; }
	public static MonoTouch.Foundation.NSString AssetCreatedDateKey { get; }
	public static MonoTouch.Foundation.NSString AssetModifiedDateKey { get; }
	public static MonoTouch.Foundation.NSString AssetUnitKey { get; }
	public static MonoTouch.Foundation.NSString AssetUpAxisKey { get; }
}
```

### New Type MonoTouch.SceneKit.SCNSceneSourceStatus

```
[Serializable]
public enum SCNSceneSourceStatus {
	Complete = 16,
	Error = -1,
	Parsing = 4,
	Processing = 12,
	Validating = 8,
}
```

### New Type MonoTouch.SceneKit.SCNSceneSourceStatusHandler

```
public sealed delegate SCNSceneSourceStatusHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneSourceStatusHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (float totalProgress, SCNSceneSourceStatus status, MonoTouch.Foundation.NSError error, ref bool stopLoading, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stopLoading, System.IAsyncResult result);
	public virtual void Invoke (float totalProgress, SCNSceneSourceStatus status, MonoTouch.Foundation.NSError error, ref bool stopLoading);
}
```

### New Type MonoTouch.SceneKit.SCNShadable

```
public class SCNShadable : MonoTouch.Foundation.NSObject, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNShadable ();
	public SCNShadable (MonoTouch.Foundation.NSCoder coder);
	public SCNShadable (MonoTouch.Foundation.NSObjectFlag t);
	public SCNShadable (System.IntPtr handle);
	// properties
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
	// methods
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
}
```

### New Type MonoTouch.SceneKit.SCNShadable_Extensions

```
public static class SCNShadable_Extensions {
	// methods
	public static void HandleBinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
	public static void HandleUnbinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
}
```

### New Type MonoTouch.SceneKit.SCNShaderModifiers

```
public class SCNShaderModifiers : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public SCNShaderModifiers ();
	public SCNShaderModifiers (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public string EntryPointFragment { get; set; }
	public string EntryPointGeometry { get; set; }
	public string EntryPointLightingModel { get; set; }
	public string EntryPointSurface { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNShadowMode

```
[Serializable]
public enum SCNShadowMode {
	Deferred = 1,
	Forward = 0,
	Modulated = 2,
}
```

### New Type MonoTouch.SceneKit.SCNShape

```
public class SCNShape : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNShape ();
	public SCNShape (MonoTouch.Foundation.NSCoder coder);
	public SCNShape (MonoTouch.Foundation.NSObjectFlag t);
	public SCNShape (System.IntPtr handle);
	// properties
	public virtual SCNChamferMode ChamferMode { get; set; }
	public virtual MonoTouch.UIKit.UIBezierPath ChamferProfile { get; set; }
	public virtual float ChamferRadius { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float ExtrusionDepth { get; set; }
	public virtual MonoTouch.UIKit.UIBezierPath Path { get; set; }
	// methods
	public static SCNShape Create (MonoTouch.UIKit.UIBezierPath path, float extrusionDepth);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNSkinner

```
public class SCNSkinner : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSSecureCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSkinner (MonoTouch.Foundation.NSCoder coder);
	public SCNSkinner (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSkinner (System.IntPtr handle);
	// properties
	public virtual SCNGeometry BaseGeometry { get; set; }
	public virtual SCNMatrix4 BaseGeometryBindTransform { get; set; }
	public virtual SCNGeometrySource BoneIndices { get; }
	public SCNMatrix4[] BoneInverseBindTransforms { get; }
	public virtual SCNNode[] Bones { get; }
	public virtual SCNGeometrySource BoneWeights { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNNode Skeleton { get; set; }
	// methods
	public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, SCNMatrix4[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNSphere

```
public class SCNSphere : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSphere (MonoTouch.Foundation.NSCoder coder);
	public SCNSphere (MonoTouch.Foundation.NSObjectFlag t);
	public SCNSphere (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Geodesic { get; set; }
	public virtual float Radius { get; set; }
	public virtual int SegmentCount { get; set; }
	// methods
	public static SCNSphere Create (float radius);
}
```

### New Type MonoTouch.SceneKit.SCNTechnique

```
public class SCNTechnique : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechnique (MonoTouch.Foundation.NSCoder coder);
	public SCNTechnique (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTechnique (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSDictionary DictionaryRepresentation { get; }
	// methods
	public virtual void AddAnimation (MonoTouch.CoreAnimation.CAAnimation animation, MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static SCNTechnique Create (MonoTouch.Foundation.NSDictionary dictionary);
	public static SCNTechnique Create (SCNTechnique[] techniques);
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.CoreAnimation.CAAnimation GetAnimation (MonoTouch.Foundation.NSString key);
	public virtual MonoTouch.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoTouch.Foundation.NSString key);
	public virtual void PauseAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoTouch.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNTechniqueSupport

```
public abstract class SCNTechniqueSupport : MonoTouch.Foundation.NSObject, ISCNTechniqueSupport, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechniqueSupport ();
	public SCNTechniqueSupport (MonoTouch.Foundation.NSCoder coder);
	public SCNTechniqueSupport (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTechniqueSupport (System.IntPtr handle);
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoTouch.SceneKit.SCNTechniqueSupport_Extensions

```
public static class SCNTechniqueSupport_Extensions {
}
```

### New Type MonoTouch.SceneKit.SCNText

```
public class SCNText : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNText (MonoTouch.Foundation.NSCoder coder);
	public SCNText (MonoTouch.Foundation.NSObjectFlag t);
	public SCNText (System.IntPtr handle);
	// properties
	public virtual string AlignmentMode { get; set; }
	public virtual MonoTouch.UIKit.UIBezierPath ChamferProfile { get; set; }
	public virtual float ChamferRadius { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF ContainerFrame { get; set; }
	public virtual float ExtrusionDepth { get; set; }
	public virtual float Flatness { get; set; }
	public virtual MonoTouch.UIKit.UIFont Font { get; set; }
	public virtual MonoTouch.Foundation.NSObject String { get; set; }
	public virtual string TruncationMode { get; set; }
	public virtual bool Wrapped { get; set; }
	// methods
	public static SCNText Create (string str, float extrusionDepth);
	public static SCNText Create (MonoTouch.Foundation.NSAttributedString attributedString, float extrusionDepth);
	public static SCNText Create (MonoTouch.Foundation.NSObject str, float extrusionDepth);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.SceneKit.SCNTorus

```
public class SCNTorus : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTorus (MonoTouch.Foundation.NSCoder coder);
	public SCNTorus (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTorus (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PipeRadius { get; set; }
	public virtual int PipeSegmentCount { get; set; }
	public virtual float RingRadius { get; set; }
	public virtual int RingSegmentCount { get; set; }
	// methods
	public static SCNTorus Create (float ringRadius, float pipeRadius);
}
```

### New Type MonoTouch.SceneKit.SCNTransaction

```
public class SCNTransaction : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTransaction ();
	public SCNTransaction (MonoTouch.Foundation.NSCoder coder);
	public SCNTransaction (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTransaction (System.IntPtr handle);
	// properties
	public static double AnimationDuration { get; set; }
	public static MonoTouch.CoreAnimation.CAMediaTimingFunction AnimationTimingFunction { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public static bool DisableActions { get; set; }
	// methods
	public static void Begin ();
	public static void Commit ();
	public static void Flush ();
	public static void Lock ();
	public static void SetCompletionBlock (MonoTouch.Foundation.NSAction completion);
	public static void SetValueForKey (MonoTouch.Foundation.NSObject value, MonoTouch.Foundation.NSString key);
	public static void Unlock ();
	public virtual MonoTouch.Foundation.NSObject ValueForKey (MonoTouch.Foundation.NSString key);
}
```

### New Type MonoTouch.SceneKit.SCNTransformConstraint

```
public class SCNTransformConstraint : MonoTouch.SceneKit.SCNConstraint, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTransformConstraint (MonoTouch.Foundation.NSCoder coder);
	public SCNTransformConstraint (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTransformConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNTransformConstraint Create (bool inWorldSpace, SCNTransformConstraintHandler transformHandler);
}
```

### New Type MonoTouch.SceneKit.SCNTransformConstraintHandler

```
public sealed delegate SCNTransformConstraintHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNTransformConstraintHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, SCNMatrix4 transform, System.AsyncCallback callback, object object);
	public virtual SCNMatrix4 EndInvoke (System.IAsyncResult result);
	public virtual SCNMatrix4 Invoke (SCNNode node, SCNMatrix4 transform);
}
```

### New Type MonoTouch.SceneKit.SCNTransparencyMode

```
[Serializable]
public enum SCNTransparencyMode {
	AOne = 0,
	RgbZero = 1,
}
```

### New Type MonoTouch.SceneKit.SCNTube

```
public class SCNTube : MonoTouch.SceneKit.SCNGeometry, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.Foundation.INSSecureCoding, ISCNAnimatable, ISCNBoundingVolume, ISCNShadable, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTube ();
	public SCNTube (MonoTouch.Foundation.NSCoder coder);
	public SCNTube (MonoTouch.Foundation.NSObjectFlag t);
	public SCNTube (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Height { get; set; }
	public virtual int HeightSegmentCount { get; set; }
	public virtual float InnerRadius { get; set; }
	public virtual float OuterRadius { get; set; }
	public virtual int RadialSegmentCount { get; set; }
	// methods
	public static SCNTube Create (float innerRadius, float outerRadius, float height);
}
```

### New Type MonoTouch.SceneKit.SCNVector3

```
[Serializable]
public struct SCNVector3, System.IEquatable<SCNVector3> {
	// constructors
	public SCNVector3 (float x, float y, float z);
	public SCNVector3 (OpenTK.Vector3 v);
	public SCNVector3 (SCNVector3 v);
	public SCNVector3 (SCNVector4 v);
	// fields
	public static SCNVector3 One;
	public static int SizeInBytes;
	public static SCNVector3 UnitX;
	public static SCNVector3 UnitY;
	public static SCNVector3 UnitZ;
	public float X;
	public float Y;
	public float Z;
	public static SCNVector3 Zero;
	// properties
	public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public OpenTK.Vector2 Xy { get; set; }
	// methods

	[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector3 right);
	public static void Add (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Add (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector3 right);
	public static SCNVector3 BaryCentric (SCNVector3 a, SCNVector3 b, SCNVector3 c, float u, float v);
	public static void BaryCentric (ref SCNVector3 a, ref SCNVector3 b, ref SCNVector3 c, float u, float v, out SCNVector3 result);
	public static float CalculateAngle (SCNVector3 first, SCNVector3 second);
	public static void CalculateAngle (ref SCNVector3 first, ref SCNVector3 second, out float result);
	public static void Clamp (ref SCNVector3 vec, ref SCNVector3 min, ref SCNVector3 max, out SCNVector3 result);
	public static SCNVector3 Clamp (SCNVector3 vec, SCNVector3 min, SCNVector3 max);
	public static SCNVector3 ComponentMax (SCNVector3 a, SCNVector3 b);
	public static void ComponentMax (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 ComponentMin (SCNVector3 a, SCNVector3 b);
	public static void ComponentMin (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Cross (SCNVector3 left, SCNVector3 right);
	public static void Cross (ref SCNVector3 left, ref SCNVector3 right, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static void Div (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static SCNVector3 Div (SCNVector3 a, float f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);
	public static SCNVector3 Divide (SCNVector3 vector, float scale);
	public static void Divide (ref SCNVector3 vector, float scale, out SCNVector3 result);
	public static SCNVector3 Divide (SCNVector3 vector, SCNVector3 scale);
	public static void Divide (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static float Dot (SCNVector3 left, SCNVector3 right);
	public static void Dot (ref SCNVector3 left, ref SCNVector3 right, out float result);
	public virtual bool Equals (SCNVector3 other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static SCNVector3 Lerp (SCNVector3 a, SCNVector3 b, float blend);
	public static void Lerp (ref SCNVector3 a, ref SCNVector3 b, float blend, out SCNVector3 result);
	public static SCNVector3 Max (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 Min (SCNVector3 left, SCNVector3 right);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public static void Mult (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public static SCNVector3 Mult (SCNVector3 a, float f);
	public static SCNVector3 Multiply (SCNVector3 vector, SCNVector3 scale);
	public static SCNVector3 Multiply (SCNVector3 vector, float scale);
	public static void Multiply (ref SCNVector3 vector, float scale, out SCNVector3 result);
	public static void Multiply (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static SCNVector3 Normalize (SCNVector3 vec);
	public static void Normalize (ref SCNVector3 vec, out SCNVector3 result);
	public void Normalize ();
	public void NormalizeFast ();
	public static SCNVector3 NormalizeFast (SCNVector3 vec);
	public static void NormalizeFast (ref SCNVector3 vec, out SCNVector3 result);
	public static SCNVector3 op_Addition (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Division (SCNVector3 vec, float scale);
	public static bool op_Equality (SCNVector3 left, SCNVector3 right);
	public static OpenTK.Vector3 op_Explicit (SCNVector3 source);
	public static SCNVector3 op_Implicit (OpenTK.Vector3 vector);
	public static bool op_Inequality (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Multiply (SCNVector3 vec, float scale);
	public static SCNVector3 op_Multiply (float scale, SCNVector3 vec);
	public static SCNVector3 op_Subtraction (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_UnaryNegation (SCNVector3 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector3 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector3 scale);

	[Obsolete ("Use static Subtract() method instead.")]
	public static void Sub (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);

	[Obsolete ("Use static Subtract() method instead.")]
	public static SCNVector3 Sub (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector3 right);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector3 right);
	public static void Subtract (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Subtract (SCNVector3 a, SCNVector3 b);
	public override string ToString ();
	public static void Transform (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector4 result);
	public static SCNVector4 Transform (SCNVector3 vec, SCNMatrix4 mat);
	public static SCNVector3 TransformNormal (SCNVector3 norm, SCNMatrix4 mat);
	public static void TransformNormal (ref SCNVector3 norm, ref SCNMatrix4 mat, out SCNVector3 result);
	public static void TransformNormalInverse (ref SCNVector3 norm, ref SCNMatrix4 invMat, out SCNVector3 result);
	public static SCNVector3 TransformNormalInverse (SCNVector3 norm, SCNMatrix4 invMat);
	public static void TransformPerspective (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector3 result);
	public static SCNVector3 TransformPerspective (SCNVector3 vec, SCNMatrix4 mat);
	public static SCNVector3 TransformPosition (SCNVector3 pos, SCNMatrix4 mat);
	public static void TransformPosition (ref SCNVector3 pos, ref SCNMatrix4 mat, out SCNVector3 result);
	public static void TransformVector (ref SCNVector3 vec, ref SCNMatrix4 mat, out SCNVector3 result);
	public static SCNVector3 TransformVector (SCNVector3 vec, SCNMatrix4 mat);
}
```

### New Type MonoTouch.SceneKit.SCNVector4

```
[Serializable]
public struct SCNVector4, System.IEquatable<SCNVector4> {
	// constructors
	public SCNVector4 (float x, float y, float z, float w);
	public SCNVector4 (OpenTK.Vector2 v);
	public SCNVector4 (SCNVector3 v);
	public SCNVector4 (OpenTK.Vector3 v);
	public SCNVector4 (OpenTK.Vector4 v);
	public SCNVector4 (SCNVector3 v, float w);
	public SCNVector4 (SCNVector4 v);
	// fields
	public static SCNVector4 One;
	public static int SizeInBytes;
	public static SCNVector4 UnitW;
	public static SCNVector4 UnitX;
	public static SCNVector4 UnitY;
	public static SCNVector4 UnitZ;
	public float W;
	public float X;
	public float Y;
	public float Z;
	public static SCNVector4 Zero;
	// properties
	public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public OpenTK.Vector2 Xy { get; set; }
	public SCNVector3 Xyz { get; set; }
	// methods

	[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector4 right);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector4 right);
	public static void Add (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Add (SCNVector4 a, SCNVector4 b);
	public static SCNVector4 BaryCentric (SCNVector4 a, SCNVector4 b, SCNVector4 c, float u, float v);
	public static void BaryCentric (ref SCNVector4 a, ref SCNVector4 b, ref SCNVector4 c, float u, float v, out SCNVector4 result);
	public static void Clamp (ref SCNVector4 vec, ref SCNVector4 min, ref SCNVector4 max, out SCNVector4 result);
	public static SCNVector4 Clamp (SCNVector4 vec, SCNVector4 min, SCNVector4 max);
	public static void Div (ref SCNVector4 a, float f, out SCNVector4 result);
	public static SCNVector4 Div (SCNVector4 a, float f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);
	public static SCNVector4 Divide (SCNVector4 vector, SCNVector4 scale);
	public static void Divide (ref SCNVector4 vector, float scale, out SCNVector4 result);
	public static void Divide (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Divide (SCNVector4 vector, float scale);
	public static float Dot (SCNVector4 left, SCNVector4 right);
	public static void Dot (ref SCNVector4 left, ref SCNVector4 right, out float result);
	public override bool Equals (object obj);
	public virtual bool Equals (SCNVector4 other);
	public override int GetHashCode ();
	public static void Lerp (ref SCNVector4 a, ref SCNVector4 b, float blend, out SCNVector4 result);
	public static SCNVector4 Lerp (SCNVector4 a, SCNVector4 b, float blend);
	public static SCNVector4 Max (SCNVector4 a, SCNVector4 b);
	public static void Max (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static void Min (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Min (SCNVector4 a, SCNVector4 b);
	public static SCNVector4 Mult (SCNVector4 a, float f);
	public static void Mult (ref SCNVector4 a, float f, out SCNVector4 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);
	public static void Multiply (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, SCNVector4 scale);
	public static void Multiply (ref SCNVector4 vector, float scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, float scale);
	public void Normalize ();
	public static SCNVector4 Normalize (SCNVector4 vec);
	public static void Normalize (ref SCNVector4 vec, out SCNVector4 result);
	public void NormalizeFast ();
	public static void NormalizeFast (ref SCNVector4 vec, out SCNVector4 result);
	public static SCNVector4 NormalizeFast (SCNVector4 vec);
	public static SCNVector4 op_Addition (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Division (SCNVector4 vec, float scale);
	public static bool op_Equality (SCNVector4 left, SCNVector4 right);
	public static float* op_Explicit (SCNVector4 v);
	public static OpenTK.Vector4 op_Explicit (SCNVector4 source);
	public static System.IntPtr op_Explicit (SCNVector4 v);
	public static SCNVector4 op_Implicit (OpenTK.Vector4 vector);
	public static bool op_Inequality (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Multiply (float scale, SCNVector4 vec);
	public static SCNVector4 op_Multiply (SCNVector4 vec, float scale);
	public static SCNVector4 op_Subtraction (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_UnaryNegation (SCNVector4 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz, float sw);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector4 right);
	public static SCNVector4 Sub (SCNVector4 a, SCNVector4 b);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector4 right);
	public static void Sub (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static void Subtract (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Subtract (SCNVector4 a, SCNVector4 b);
	public override string ToString ();
	public static void Transform (ref SCNVector4 vec, ref SCNMatrix4 mat, out SCNVector4 result);
	public static SCNVector4 Transform (SCNVector4 vec, SCNMatrix4 mat);
}
```

### New Type MonoTouch.SceneKit.SCNView

```
public class SCNView : MonoTouch.UIKit.UIView, ISCNSceneRenderer, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUITraitEnvironment {
	// constructors
	public SCNView (MonoTouch.Foundation.NSCoder coder);
	public SCNView (MonoTouch.Foundation.NSObjectFlag t);
	public SCNView (System.IntPtr handle);
	public SCNView (System.Drawing.RectangleF frame, MonoTouch.Foundation.NSDictionary options);
	public SCNView (System.Drawing.RectangleF frame);
	// properties
	public virtual bool AllowsCameraControl { get; set; }
	public virtual SCNAntialiasingMode AntialiasingMode { get; set; }
	public static SCNView.SCNViewAppearance Appearance { get; }
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.OpenGLES.EAGLContext Context { get; set; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual MonoTouch.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public virtual int PreferredFramesPerSecond { get; set; }
	public virtual SCNScene Scene { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	public static SCNView.SCNViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static SCNView.SCNViewAppearance GetAppearance<T> ();
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Pause (MonoTouch.Foundation.NSObject sender);
	public virtual void Play (MonoTouch.Foundation.NSObject sender);
	public virtual void Prepare (MonoTouch.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoTouch.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual MonoTouch.UIKit.UIImage Snapshot ();
	public virtual void Stop (MonoTouch.Foundation.NSObject sender);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);

	// inner types
	public class SCNViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	}
}
```

### New Type MonoTouch.SceneKit.SCNWrapMode

```
[Serializable]
public enum SCNWrapMode {
	Clamp = 1,
	ClampToBorder = 3,
	Mirror = 4,
	Repeat = 2,
}
```

## New Namespace MonoTouch.WebKit

### New Type MonoTouch.WebKit.IWKNavigationDelegate

```
public interface IWKNavigationDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.WebKit.IWKScriptMessageHandler

```
public interface IWKScriptMessageHandler : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type MonoTouch.WebKit.IWKUIDelegate

```
public interface IWKUIDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.WebKit.WKBackForwardList

```
public class WKBackForwardList : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardList (MonoTouch.Foundation.NSCoder coder);
	public WKBackForwardList (MonoTouch.Foundation.NSObjectFlag t);
	public WKBackForwardList (System.IntPtr handle);
	// properties
	public virtual WKBackForwardListItem BackItem { get; }
	public virtual WKBackForwardListItem[] BackList { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKBackForwardListItem CurrentItem { get; }
	public virtual WKBackForwardListItem ForwardItem { get; }
	public virtual WKBackForwardListItem[] ForwardList { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual WKBackForwardListItem ItemAtIndex (int index);
}
```

### New Type MonoTouch.WebKit.WKBackForwardListItem

```
public class WKBackForwardListItem : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardListItem (MonoTouch.Foundation.NSCoder coder);
	public WKBackForwardListItem (MonoTouch.Foundation.NSObjectFlag t);
	public WKBackForwardListItem (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSUrl InitialUrl { get; }
	public virtual string Title { get; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
}
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

### New Type MonoTouch.WebKit.WKFrameInfo

```
public class WKFrameInfo : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKFrameInfo ();
	public WKFrameInfo (MonoTouch.Foundation.NSCoder coder);
	public WKFrameInfo (MonoTouch.Foundation.NSObjectFlag t);
	public WKFrameInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool MainFrame { get; }
	public virtual MonoTouch.Foundation.NSUrlRequest Request { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
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

### New Type MonoTouch.WebKit.WKNavigation

```
public class WKNavigation : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigation ();
	public WKNavigation (MonoTouch.Foundation.NSCoder coder);
	public WKNavigation (MonoTouch.Foundation.NSObjectFlag t);
	public WKNavigation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.WebKit.WKNavigationAction

```
public class WKNavigationAction : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationAction ();
	public WKNavigationAction (MonoTouch.Foundation.NSCoder coder);
	public WKNavigationAction (MonoTouch.Foundation.NSObjectFlag t);
	public WKNavigationAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKNavigationType NavigationType { get; }
	public virtual MonoTouch.Foundation.NSUrlRequest Request { get; }
	public virtual WKFrameInfo SourceFrame { get; }
	public virtual WKFrameInfo TargetFrame { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.WebKit.WKNavigationActionPolicy

```
[Serializable]
public enum WKNavigationActionPolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoTouch.WebKit.WKNavigationDelegate

```
public class WKNavigationDelegate : MonoTouch.Foundation.NSObject, IWKNavigationDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationDelegate ();
	public WKNavigationDelegate (MonoTouch.Foundation.NSCoder coder);
	public WKNavigationDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public WKNavigationDelegate (System.IntPtr handle);
	// methods
	public virtual void DecidePolicy (WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public virtual void DecidePolicy (WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public virtual void DidCommitNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidFailNavigation (WKWebView webView, WKNavigation navigation, MonoTouch.Foundation.NSError error);
	public virtual void DidFailProvisionalNavigation (WKWebView webView, WKNavigation navigation, MonoTouch.Foundation.NSError error);
	public virtual void DidFinishNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidReceiveAuthenticationChallenge (WKWebView webView, MonoTouch.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoTouch.Foundation.NSUrlSessionAuthChallengeDisposition,MonoTouch.Foundation.NSUrlCredential> completionHandler);
	public virtual void DidReceiveServerRedirectForProvisionalNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidStartProvisionalNavigation (WKWebView webView, WKNavigation navigation);
}
```

### New Type MonoTouch.WebKit.WKNavigationDelegate_Extensions

```
public static class WKNavigationDelegate_Extensions {
	// methods
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public static void DidCommitNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidFailNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, MonoTouch.Foundation.NSError error);
	public static void DidFailProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, MonoTouch.Foundation.NSError error);
	public static void DidFinishNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidReceiveAuthenticationChallenge (IWKNavigationDelegate This, WKWebView webView, MonoTouch.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoTouch.Foundation.NSUrlSessionAuthChallengeDisposition,MonoTouch.Foundation.NSUrlCredential> completionHandler);
	public static void DidReceiveServerRedirectForProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidStartProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
}
```

### New Type MonoTouch.WebKit.WKNavigationResponse

```
public class WKNavigationResponse : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationResponse ();
	public WKNavigationResponse (MonoTouch.Foundation.NSCoder coder);
	public WKNavigationResponse (MonoTouch.Foundation.NSObjectFlag t);
	public WKNavigationResponse (System.IntPtr handle);
	// properties
	public virtual bool CanShowMimeType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsForMainFrame { get; }
	public virtual MonoTouch.Foundation.NSUrlResponse Response { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.WebKit.WKNavigationResponsePolicy

```
[Serializable]
public enum WKNavigationResponsePolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoTouch.WebKit.WKNavigationType

```
[Serializable]
public enum WKNavigationType {
	BackForward = 2,
	FormResubmitted = 4,
	FormSubmitted = 1,
	LinkActivated = 0,
	Other = -1,
	Reload = 3,
}
```

### New Type MonoTouch.WebKit.WKPreferences

```
public class WKPreferences : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKPreferences ();
	public WKPreferences (MonoTouch.Foundation.NSCoder coder);
	public WKPreferences (MonoTouch.Foundation.NSObjectFlag t);
	public WKPreferences (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool JavaScriptCanOpenWindowsAutomatically { get; set; }
	public virtual bool JavaScriptEnabled { get; set; }
	public virtual float MinimumFontSize { get; set; }
}
```

### New Type MonoTouch.WebKit.WKProcessPool

```
public class WKProcessPool : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKProcessPool ();
	public WKProcessPool (MonoTouch.Foundation.NSCoder coder);
	public WKProcessPool (MonoTouch.Foundation.NSObjectFlag t);
	public WKProcessPool (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoTouch.WebKit.WKScriptMessage

```
public class WKScriptMessage : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessage ();
	public WKScriptMessage (MonoTouch.Foundation.NSCoder coder);
	public WKScriptMessage (MonoTouch.Foundation.NSObjectFlag t);
	public WKScriptMessage (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSObject Body { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKFrameInfo FrameInfo { get; }
	public virtual string Name { get; }
	public virtual WKWebView WebView { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.WebKit.WKScriptMessageHandler

```
public abstract class WKScriptMessageHandler : MonoTouch.Foundation.NSObject, IWKScriptMessageHandler, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessageHandler ();
	public WKScriptMessageHandler (MonoTouch.Foundation.NSCoder coder);
	public WKScriptMessageHandler (MonoTouch.Foundation.NSObjectFlag t);
	public WKScriptMessageHandler (System.IntPtr handle);
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type MonoTouch.WebKit.WKScriptMessageHandler_Extensions

```
public static class WKScriptMessageHandler_Extensions {
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

### New Type MonoTouch.WebKit.WKUIDelegate

```
public class WKUIDelegate : MonoTouch.Foundation.NSObject, IWKUIDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUIDelegate ();
	public WKUIDelegate (MonoTouch.Foundation.NSCoder coder);
	public WKUIDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public WKUIDelegate (System.IntPtr handle);
	// methods
	public virtual WKWebView CreateWebView (WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public virtual void RunJavaScriptAlertPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public virtual void RunJavaScriptConfirmPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public virtual void RunJavaScriptTextInputPanel (WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type MonoTouch.WebKit.WKUIDelegate_Extensions

```
public static class WKUIDelegate_Extensions {
	// methods
	public static WKWebView CreateWebView (IWKUIDelegate This, WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public static void RunJavaScriptAlertPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public static void RunJavaScriptConfirmPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public static void RunJavaScriptTextInputPanel (IWKUIDelegate This, WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type MonoTouch.WebKit.WKUserContentController

```
public class WKUserContentController : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserContentController ();
	public WKUserContentController (MonoTouch.Foundation.NSCoder coder);
	public WKUserContentController (MonoTouch.Foundation.NSObjectFlag t);
	public WKUserContentController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKUserScript[] UserScripts { get; }
	// methods
	public virtual void AddScriptMessageHandler (WKScriptMessageHandler scriptMessageHandler, string name);
	public virtual void AddUserScript (WKUserScript userScript);
	protected override void Dispose (bool disposing);
	public virtual void RemoveAllUserScripts ();
	public virtual void RemoveScriptMessageHandler (string name);
}
```

### New Type MonoTouch.WebKit.WKUserScript

```
public class WKUserScript : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserScript (MonoTouch.Foundation.NSCoder coder);
	public WKUserScript (MonoTouch.Foundation.NSObjectFlag t);
	public WKUserScript (System.IntPtr handle);
	public WKUserScript (MonoTouch.Foundation.NSString source, WKUserScriptInjectionTime injectionTime, bool isForMainFrameOnly);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKUserScriptInjectionTime InjectionTime { get; }
	public virtual bool IsForMainFrameOnly { get; }
	public virtual MonoTouch.Foundation.NSString Source { get; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.WebKit.WKUserScriptInjectionTime

```
[Serializable]
public enum WKUserScriptInjectionTime {
	AtDocumentEnd = 1,
	AtDocumentStart = 0,
}
```

### New Type MonoTouch.WebKit.WKWebView

```
public class WKWebView : MonoTouch.UIKit.UIView, System.Collections.IEnumerable, MonoTouch.Foundation.INSCoding, MonoTouch.UIKit.IUIAccessibilityIdentification, MonoTouch.UIKit.IUICoordinateSpace, MonoTouch.UIKit.IUIDynamicItem, MonoTouch.UIKit.IUITraitEnvironment, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebView (MonoTouch.Foundation.NSCoder coder);
	public WKWebView (MonoTouch.Foundation.NSObjectFlag t);
	public WKWebView (System.IntPtr handle);
	public WKWebView (System.Drawing.RectangleF frame, WKWebViewConfiguration configuration);
	// properties
	public virtual bool AllowsBackForwardNavigationGestures { get; set; }
	public static WKWebView.WKWebViewAppearance Appearance { get; }
	public virtual WKBackForwardList BackForwardList { get; }
	public virtual bool CanGoBack { get; }
	public virtual bool CanGoForward { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKWebViewConfiguration Configuration { get; }
	public virtual double EstimatedProgress { get; }
	public virtual bool HasOnlySecureContent { get; }
	public virtual bool IsLoading { get; }
	public WKNavigationDelegate NavigationDelegate { get; set; }
	public virtual MonoTouch.UIKit.UIScrollView ScrollView { get; }
	public virtual string Title { get; }
	public WKUIDelegate UIDelegate { get; set; }
	public virtual MonoTouch.Foundation.NSUrl Url { get; }
	public virtual MonoTouch.Foundation.NSObject WeakNavigationDelegate { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakUIDelegate { get; set; }
	// methods
	public static WKWebView.WKWebViewAppearance AppearanceWhenContainedIn (System.Type[] containers);
	protected override void Dispose (bool disposing);
	public virtual void EvaluateJavaScript (MonoTouch.Foundation.NSString javascript, WKJavascriptEvaluationResult completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.Foundation.NSObject> EvaluateJavaScriptAsync (MonoTouch.Foundation.NSString javascript);
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static WKWebView.WKWebViewAppearance GetAppearance<T> ();
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public virtual WKNavigation GoBack ();
	public virtual WKNavigation GoForward ();
	public virtual WKNavigation GoTo (WKBackForwardListItem item);
	public virtual WKNavigation LoadHtmlString (MonoTouch.Foundation.NSString htmlString, MonoTouch.Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadRequest (MonoTouch.Foundation.NSUrlRequest request);
	public virtual WKNavigation Reload ();
	public virtual WKNavigation ReloadFromOrigin ();
	public virtual void StopLoading ();

	// inner types
	public class WKWebViewAppearance : MonoTouch.UIKit.UIView+UIViewAppearance, MonoTouch.UIKit.IUIAppearance, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	}
}
```

### New Type MonoTouch.WebKit.WKWebViewConfiguration

```
public class WKWebViewConfiguration : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebViewConfiguration ();
	public WKWebViewConfiguration (MonoTouch.Foundation.NSCoder coder);
	public WKWebViewConfiguration (MonoTouch.Foundation.NSObjectFlag t);
	public WKWebViewConfiguration (System.IntPtr handle);
	// properties
	public virtual bool AllowsInlineMediaPlayback { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool MediaPlaybackAllowsAirPlay { get; set; }
	public virtual bool MediaPlaybackRequiresUserAction { get; set; }
	public virtual WKPreferences Preferences { get; set; }
	public virtual WKProcessPool ProcessPool { get; set; }
	public virtual WKSelectionGranularity SelectionGranularity { get; set; }
	public virtual bool SuppressesIncrementalRendering { get; set; }
	public virtual WKUserContentController UserContentController { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.WebKit.WKWindowFeatures

```
public class WKWindowFeatures : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWindowFeatures ();
	public WKWindowFeatures (MonoTouch.Foundation.NSCoder coder);
	public WKWindowFeatures (MonoTouch.Foundation.NSObjectFlag t);
	public WKWindowFeatures (System.IntPtr handle);
	// properties
	public bool? AllowsResizing { get; }
	public override System.IntPtr ClassHandle { get; }
	public float? Height { get; }
	public bool? MenuBarVisibility { get; }
	public bool? StatusBarVisibility { get; }
	public bool? ToolbarsVisibility { get; }
	public float? Width { get; }
	public float? X { get; }
	public float? Y { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```
