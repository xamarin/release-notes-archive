---
id: 11D7A580-7958-4CC7-A09A-41D65E34BBB7
title: "From 7.9.0 to 7.9.1"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string CoreServicesLibrary = "/System/Library/Frameworks/CoreServices.framework/CoreServices";
	public static const string Version = "7.9.0";
```

Added fields:

```
public static const string AVKitLibrary = "/System/Library/Frameworks/AVKit.framework/AVKit";
	public static const string CoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
	public static const string Version = "7.9.1";
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Added methods:

```
public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static ABPeoplePickerNavigationController.ABPeoplePickerNavigationControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate

Removed methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, System.IntPtr selectedPerson);
	public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, System.IntPtr selectedPerson, System.IntPtr abMultiValueIdentifier);
```

Added methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson);
	public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, System.IntPtr abMultiValueIdentifier);
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions

Removed methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, System.IntPtr selectedPerson);
	public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, System.IntPtr selectedPerson, System.IntPtr abMultiValueIdentifier);
```

Added methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson);
	public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, MonoTouch.AddressBook.ABRecord selectedPerson, System.IntPtr abMultiValueIdentifier);
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

### Type Changed: MonoTouch.AudioToolbox.AudioQueueStatus

Added value:

```
BufferEnqueuedTwice = -66666,
```

## Namespace MonoTouch.AudioUnit

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

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAssetReaderOutputMetadataAdaptor

Removed method:

```
public static AVAssetReaderOutputMetadataAdaptor GetAssetReaderOutputMetadataAdapter (AVAssetReaderTrackOutput trackOutput);
```

Added method:

```
public static AVAssetReaderOutputMetadataAdaptor Create (AVAssetReaderTrackOutput trackOutput);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetReaderSampleReferenceOutput

Removed method:

```
public static AVAssetReaderSampleReferenceOutput GetAssetReaderSampleReferenceOutput (AVAssetTrack track);
```

Added method:

```
public static AVAssetReaderSampleReferenceOutput Create (AVAssetTrack track);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate

Added method:

```
public virtual bool ShouldWaitForRenewalOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added method:

```
public static bool ShouldWaitForRenewalOfRequestedResource (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

Removed method:

```
public virtual void RespondToEachPassDescription (MonoTouch.CoreFoundation.DispatchQueue queue, System.Action block);
```

Added method:

```
public virtual void SetPassHandler (MonoTouch.CoreFoundation.DispatchQueue queue, System.Action passHandler);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputMetadataAdaptor

Removed method:

```
public static AVAssetWriterInputMetadataAdaptor GetAssetWriterInputMetadataAdaptor (AVAssetWriterInput input);
```

Added method:

```
public static AVAssetWriterInputMetadataAdaptor Create (AVAssetWriterInput input);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioCommonFormat

Removed values:

```
OtherFormat = 0,
	PCMFormatFloat32 = 1,
	PCMFormatFloat64 = 2,
	PCMFormatInt16 = 3,
	PCMFormatInt32 = 4,
```

Added values:

```
Other = 0,
	PCMFloat32 = 1,
	PCMFloat64 = 2,
	PCMInt16 = 3,
	PCMInt32 = 4,
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

### Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

Added constructors:

```
public AVCaptureConnection (AVCaptureInputPort[] inputPorts, AVCaptureOutput output);
	public AVCaptureConnection (AVCaptureInputPort inputPort, AVCaptureVideoPreviewLayer layer);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added properties:

```
public virtual AVCaptureWhiteBalanceGains DeviceWhiteBalanceGains { get; }
	public static MonoTouch.CoreMedia.CMTime ExposureDurationCurrent { get; }
	public static float ExposureTargetBiasCurrent { get; }
	public virtual AVCaptureWhiteBalanceGains GrayWorldDeviceWhiteBalanceGains { get; }
	public static float ISOCurrent { get; }
	public virtual float LensPosition { get; }
	public static float LensPositionCurrent { get; }
	public virtual float MaxWhiteBalanceGain { get; }
	public virtual bool SubjectAreaChangeMonitoringEnabled { get; }
	public static AVCaptureWhiteBalanceGains WhiteBalanceGainsCurrent { get; }
```

Removed method:

```
public virtual void SetExposureModeCustom (MonoTouch.CoreMedia.CMTime duration, float ISO, System.Action<MonoTouch.CoreMedia.CMTime> completionHandlerr);
```

Added methods:

```
public virtual AVCaptureWhiteBalanceChromaticityValues GetChromaticityValues (AVCaptureWhiteBalanceGains whiteBalanceGains);
	public virtual AVCaptureWhiteBalanceGains GetDeviceWhiteBalanceGains (AVCaptureWhiteBalanceChromaticityValues chromaticityValues);
	public virtual AVCaptureWhiteBalanceGains GetDeviceWhiteBalanceGains (AVCaptureWhiteBalanceTemperatureAndTintValues tempAndTintValues);
	public virtual AVCaptureWhiteBalanceTemperatureAndTintValues GetTemperatureAndTintValues (AVCaptureWhiteBalanceGains whiteBalanceGains);
	public virtual void LockExposure (MonoTouch.CoreMedia.CMTime duration, float ISO, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> LockExposureAsync (MonoTouch.CoreMedia.CMTime duration, float ISO);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetExposureTargetBiasAsync (float bias);
	public virtual void SetFocusModeLocked (float lensPosition, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetFocusModeLockedAsync (float lensPosition);
	public virtual void SetWhiteBalanceModeLockedWithDeviceWhiteBalanceGains (AVCaptureWhiteBalanceGains whiteBalanceGains, System.Action<MonoTouch.CoreMedia.CMTime> completionHandler);
	public virtual System.Threading.Tasks.Task<MonoTouch.CoreMedia.CMTime> SetWhiteBalanceModeLockedWithDeviceWhiteBalanceGainsAsync (AVCaptureWhiteBalanceGains whiteBalanceGains);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceFormat

Added properties:

```
public virtual MonoTouch.CoreMedia.CMTime MaxExposureDuration { get; }
	public virtual float MaxISO { get; }
	public virtual MonoTouch.CoreMedia.CMTime MinExposureDuration { get; }
	public virtual float MinISO { get; }
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

Added property:

```
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
	public static MonoTouch.Foundation.NSString FormatIcyMetadata { get; }
	public static MonoTouch.Foundation.NSString IcyMetadataKeyStreamTitle { get; }
	public static MonoTouch.Foundation.NSString IcyMetadataKeyStreamUrl { get; }
	public static MonoTouch.Foundation.NSString IsoUserDataKeyTaggedCharacteristic { get; }
	public static MonoTouch.Foundation.NSString KeySpaceIcy { get; }
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

Removed method:

```
public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
```

Added method:

```
public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
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
	public virtual System.IntPtr _Layout { get; }
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
	public virtual bool LoadSoundBank (MonoTouch.Foundation.NSUrl bankUrl, out MonoTouch.Foundation.NSError outError);
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
	public virtual bool ReadyForMoreMediaData { get; }
	public virtual string VideoGravity { get; set; }
	// methods
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

## Namespace MonoTouch.CloudKit

### Type Changed: MonoTouch.CloudKit.CKAsset

Removed constructor:

```
public CKAsset (MonoTouch.Foundation.NSUrl fileURL);
```

Added constructor:

```
public CKAsset (MonoTouch.Foundation.NSUrl fileUrl);
```

### Type Changed: MonoTouch.CloudKit.CKDiscoverAllContactsOperation

Removed property:

```
public virtual System.Action<CKDiscoveredUserInfo[],MonoTouch.Foundation.NSError> DiscoverAllContactsHandler { get; }
```

Added property:

```
public virtual System.Action<CKDiscoveredUserInfo[],MonoTouch.Foundation.NSError> DiscoverAllContactsHandler { get; set; }
```

### Type Changed: MonoTouch.CloudKit.CKErrorCode

Added value:

```
None = 0,
```

### Type Changed: MonoTouch.CloudKit.CKModifyRecordsOperation

Added property:

```
public virtual bool Atomic { get; set; }
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIContextOptions

Added properties:

```
public int? CIImageFormat { get; set; }
	public bool? PriorityRequestLow { get; set; }
```

### Type Changed: MonoTouch.CoreImage.CIFilter

Added constructor:

```
protected CIFilter ();
```

### Type Changed: MonoTouch.CoreImage.CIImage

Removed methods:

```
public virtual CIImage GetImage (string filterName, MonoTouch.Foundation.NSDictionary inputParameters);
	public virtual CIImage GetImage (CIImageOrientation orientation);
	public virtual CIImage GetImageByClampingToExtent ();
```

Added methods:

```
public virtual CIImage CreateByClampingToExtent ();
	public virtual CIImage CreateByCompositingOverImage (CIImage dest);
	public virtual CIImage CreateByFiltering (string filterName, MonoTouch.Foundation.NSDictionary inputParameters);
	public virtual CIImage CreateWithOrientation (CIImageOrientation orientation);
```

### New Type MonoTouch.CoreImage.CIAccordionFoldTransition

```
public class CIAccordionFoldTransition : MonoTouch.CoreImage.CIFilter, MonoTouch.Foundation.INSCoding, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAccordionFoldTransition ();
	public CIAccordionFoldTransition (System.IntPtr handle);
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

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added methods:

```
public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static EKEventEditViewController.EKEventEditViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added method:

```
protected uint? GetUInt32Value (NSString key);
```

### Type Changed: MonoTouch.Foundation.INSExtensionRequestHandling

Added method:

```
public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
```

### Type Changed: MonoTouch.Foundation.NSCalendar

Removed property:

```
public static NSString CalendarDayChangedNotification { get; }
```

Added property:

```
public static NSString DayChangedNotification { get; }
```

### Type Changed: MonoTouch.Foundation.NSCalendar.Notifications

Removed method:

```
public static NSObject ObserveCalendarDayChanged (System.EventHandler<NSNotificationEventArgs> handler);
```

Added method:

```
public static NSObject ObserveDayChanged (System.EventHandler<NSNotificationEventArgs> handler);
```

### Type Changed: MonoTouch.Foundation.NSExtensionRequestHandling_Extensions

Removed method:

```
public static void BeginRequestWithExtensionContext (INSExtensionRequestHandling This, NSExtensionContext context);
```

### Type Changed: MonoTouch.Foundation.NSFileAccessIntent

Removed property:

```
public virtual NSUrl URL { get; }
```

Added property:

```
public virtual NSUrl Url { get; }
```

### Type Changed: MonoTouch.Foundation.NSHttpCookieStorage

Added methods:

```
public virtual void GetCookiesForTask (NSUrlSessionTask task, System.Action<NSHttpCookie[]> completionHandler);
	public virtual void RemoveCookiesSinceDate (NSDate date);
	public virtual void StoreCookies (NSHttpCookie[] cookies, NSUrlSessionTask task);
```

### Type Changed: MonoTouch.Foundation.NSMassFormatter

Removed method:

```
public virtual string UnitStringFromKilograms (double numberInKilograms, NSMassFormatterUnit unitp);
```

Added method:

```
public virtual string UnitStringFromKilograms (double numberInKilograms, ref NSMassFormatterUnit unitp);
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

### Type Changed: MonoTouch.Foundation.NSUrl

Added properties:

```
public virtual string LastPathComponent { get; }
	public virtual string[] PathComponents { get; }
```

### Type Changed: MonoTouch.Foundation.NSUrlSession

Removed methods:

```
public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
```

Added methods:

```
public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionDownloadResponse completionHandler);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTaskRequest

Removed constructor:

```
public NSUrlSessionDownloadTaskRequest (NSData data, NSUrlResponse response);
```

Added constructor:

```
public NSUrlSessionDownloadTaskRequest (NSUrl data, NSUrlResponse response);
```

Removed property:

```
public NSData Data { get; set; }
```

Added property:

```
public NSUrl Data { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionTask

Added property:

```
public virtual float Priority { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSValue

Added property:

```
public virtual MonoTouch.SceneKit.SCNMatrix4 SCNMatrix4Value { get; }
```

Added method:

```
public static NSValue FromSCNMatrix4 (MonoTouch.SceneKit.SCNMatrix4 matrix);
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

### New Type MonoTouch.Foundation.NSUrlSessionDownloadResponse

```
public sealed delegate NSUrlSessionDownloadResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionDownloadResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrl data, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrl data, NSUrlResponse response, NSError error);
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

## Namespace MonoTouch.GameController

### Type Changed: MonoTouch.GameController.GCMotion

Removed constructor:

```
public GCMotion ();
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievementDescription

Obsoleted property:

```
[Obsolete ("Deprecated in iOS 7.0")]
	public virtual MonoTouch.UIKit.UIImage Image { get; }
```

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added methods:

```
public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKAchievementViewController.GKAchievementViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added methods:

```
public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKFriendRequestComposeViewController.GKFriendRequestComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added methods:

```
public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKLeaderboardViewController.GKLeaderboardViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added methods:

```
public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GKTurnBasedMatchmakerViewController.GKTurnBasedMatchmakerViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKView

Added methods:

```
public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static GLKView.GLKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.HealthKit

### Type Changed: MonoTouch.HealthKit.HKAnchoredObjectQuery

Removed constructor:

```
public HKAnchoredObjectQuery (HKSampleType type, MonoTouch.Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectQueryCtorCompletionHandler handler);
```

Added constructor:

```
public HKAnchoredObjectQuery (HKSampleType type, MonoTouch.Foundation.NSPredicate predicate, uint anchor, uint limit, HKAnchoredObjectResultHandler completion);
```

### Type Changed: MonoTouch.HealthKit.HKCategorySample

Removed property:

```
public static MonoTouch.Foundation.NSString PredicateKeyPathCategoryValue { get; }
```

Added method:

```
public static HKCategorySample FromType (HKCategoryType type, int value, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKMetadata metadata);
```

### Type Changed: MonoTouch.HealthKit.HKCorrelation

Added method:

```
public static HKCorrelation FromObjects (MonoTouch.Foundation.NSSet objects, HKMetadata metadata);
```

### Type Changed: MonoTouch.HealthKit.HKCorrelationQuery

Removed constructor:

```
public HKCorrelationQuery (MonoTouch.Foundation.NSObject[] types, MonoTouch.Foundation.NSPredicate predicate, MonoTouch.Foundation.NSPredicate samplePredicate, HKCorrelationQueryCtorCompletionHandler handler);
```

Added constructor:

```
public HKCorrelationQuery (MonoTouch.Foundation.NSObject[] types, MonoTouch.Foundation.NSPredicate predicate, MonoTouch.Foundation.NSPredicate samplePredicate, HKCorrelationQueryResultHandler completion);
```

### Type Changed: MonoTouch.HealthKit.HKHealthStore

Removed methods:

```
public virtual HKAuthorizationStatus AuthorizationStatus (HKObjectType type);
	public virtual System.Threading.Tasks.Task<bool> DisableAllBackgroundDeliveryAsync ();
	public virtual System.Threading.Tasks.Task<bool> DisableBackgroundDeliveryAsync (HKObjectType type);
	public virtual System.Threading.Tasks.Task<bool> EnableBackgroundDeliveryAsync (HKObjectType type, HKUpdateFrequency frequency);
```

Added method:

```
public virtual HKAuthorizationStatus GetAuthorizationStatus (HKObjectType type);
```

### Type Changed: MonoTouch.HealthKit.HKObject

Removed properties:

```
public virtual MonoTouch.Foundation.NSDictionary Metadata { get; }
	public static MonoTouch.Foundation.NSString PredicateKeyPathMetadata { get; }
	public static MonoTouch.Foundation.NSString PredicateKeyPathSource { get; }
```

Added properties:

```
public HKMetadata Metadata { get; }
	public virtual MonoTouch.Foundation.NSDictionary WeakMetadata { get; }
```

### Type Changed: MonoTouch.HealthKit.HKObjectType

Removed methods:

```
public static HKCategoryType GetCategoryType (string identifier);
	public static HKCharacteristicType GetCharacteristicType (string identifier);
	public static HKQuantityType GetQuantityType (string identifier);
```

Added methods:

```
public static HKCategoryType GetCategoryType (MonoTouch.Foundation.NSString hkCategoryTypeIdentifier);
	public static HKCharacteristicType GetCharacteristicType (MonoTouch.Foundation.NSString hkCharacteristicTypeIdentifier);
	public static HKQuantityType GetQuantityType (MonoTouch.Foundation.NSString hkTypeIdentifier);
```

### Type Changed: MonoTouch.HealthKit.HKObserverQueryUpdateHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (HKObserverQuery query, HKObserverQueryCompletionHandler completionHandler, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKObserverQuery query, HKObserverQueryCompletionHandler completionHandler, MonoTouch.Foundation.NSError error);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.HealthKit.HKQuantitySample

Removed property:

```
public static MonoTouch.Foundation.NSString PredicateKeyPathQuantity { get; }
```

Added method:

```
public static HKQuantitySample FromType (HKQuantityType quantityType, HKQuantity quantity, MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKMetadata metadata);
```

### Type Changed: MonoTouch.HealthKit.HKQuery

Removed methods:

```
public static MonoTouch.Foundation.NSPredicate GetPredicate (MonoTouch.Foundation.NSSet sources);
	public static MonoTouch.Foundation.NSPredicate GetPredicate (string key);
	public static MonoTouch.Foundation.NSPredicate GetPredicate (string key, MonoTouch.Foundation.NSPredicateOperatorType operatorType, MonoTouch.Foundation.NSObject value);
	public static MonoTouch.Foundation.NSPredicate GetPredicate (string key, MonoTouch.Foundation.NSObject[] allowedValues);
	public static MonoTouch.Foundation.NSPredicate GetPredicate (HKSource source);
```

Added methods:

```
public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey, MonoTouch.Foundation.NSObject[] allowedValues);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey, MonoTouch.Foundation.NSPredicateOperatorType operatorType, MonoTouch.Foundation.NSObject value);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForMetadataKey (MonoTouch.Foundation.NSString metadataKey);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromSource (HKSource source);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForObjectsFromSources (MonoTouch.Foundation.NSSet sources);
	public static MonoTouch.Foundation.NSPredicate GetPredicateForSamples (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKQueryOptions options);
```

### Type Changed: MonoTouch.HealthKit.HKSample

Removed properties:

```
public static MonoTouch.Foundation.NSString PredicateKeyPathEndDate { get; }
	public static MonoTouch.Foundation.NSString PredicateKeyPathStartDate { get; }
	public static MonoTouch.Foundation.NSString SampleSortIdentifierEndDate { get; }
	public static MonoTouch.Foundation.NSString SampleSortIdentifierStartDate { get; }
```

Added properties:

```
public static MonoTouch.Foundation.NSString SortIdentifierEndDate { get; }
	public static MonoTouch.Foundation.NSString SortIdentifierStartDate { get; }
```

### Type Changed: MonoTouch.HealthKit.HKSampleQuery

Added field:

```
public static const int NoLimit;
```

### Type Changed: MonoTouch.HealthKit.HKSampleQueryResultsHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (HKSampleQuery query, MonoTouch.Foundation.NSObject[] results, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKSampleQuery query, MonoTouch.Foundation.NSObject[] results, MonoTouch.Foundation.NSError error);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (HKSampleQuery query, HKSample[] results, MonoTouch.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKSampleQuery query, HKSample[] results, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.HealthKit.HKStatistics

Removed property:

```
public virtual MonoTouch.Foundation.NSObject[] Sources { get; }
```

Added property:

```
public virtual HKSource[] Sources { get; }
```

### Type Changed: MonoTouch.HealthKit.HKStatisticsCollection

Removed method:

```
public virtual void EnumerateStatistics (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKStatisticsCollectionEnumerateStaticsHandler handler);
```

Added method:

```
public virtual void EnumerateStatistics (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, HKStatisticsCollectionEnumerator handler);
```

### Type Changed: MonoTouch.HealthKit.HKStatisticsQuery

Removed constructor:

```
public HKStatisticsQuery (HKQuantityType quantityType, MonoTouch.Foundation.NSPredicate quantitySamplePredicate, HKStatisticsOptions options, HKStatisticsQueryCompletionHandler completionHandler);
```

Added constructor:

```
public HKStatisticsQuery (HKQuantityType quantityType, MonoTouch.Foundation.NSPredicate quantitySamplePredicate, HKStatisticsOptions options, HKStatisticsQueryHandler handler);
```

### Type Changed: MonoTouch.HealthKit.HKUnit

Added field:

```
public static const double MolarMassBloodGlucose;
```

Added properties:

```
public static HKUnit Atmosphere { get; }
	public static HKUnit Calorie { get; }
	public static HKUnit CentimeterOfWater { get; }
	public static HKUnit Count { get; }
	public static HKUnit Day { get; }
	public static HKUnit DegreeCelsius { get; }
	public static HKUnit DegreeFahrenheit { get; }
	public static HKUnit Foot { get; }
	public static HKUnit Gram { get; }
	public static HKUnit Hour { get; }
	public static HKUnit Inch { get; }
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
	public static HKUnit Pound { get; }
	public static HKUnit Second { get; }
	public static HKUnit Siemen { get; }
	public static HKUnit Stone { get; }
```

Removed methods:

```
public static HKUnit FromAtmosphereUnit ();
	public static HKUnit FromCalorieUnit ();
	public static HKUnit FromCentimeterOfWaterUnit ();
	public static HKUnit FromCountUnit ();
	public static HKUnit FromDayUnit ();
	public static HKUnit FromDegreeCelsiusUnit ();
	public static HKUnit FromDegreeFahrenheitUnit ();
	public static HKUnit FromFootUnit ();
	public static HKUnit FromGramUnit ();
	public static HKUnit FromHourUnit ();
	public static HKUnit FromInchUnit ();
	public static HKUnit FromJouleUnit ();
	public static HKUnit FromJouleUnit (HKMetricPrefix prefix);
	public static HKUnit FromKelvinUnit ();
	public static HKUnit FromKilocalorieUnit ();
	public static HKUnit FromLiterUnit (HKMetricPrefix prefix);
	public static HKUnit FromLiterUnit ();
	public static HKUnit FromMeterUnit ();
	public static HKUnit FromMeterUnit (HKMetricPrefix prefix);
	public static HKUnit FromMileUnit ();
	public static HKUnit FromMillimeterOfMercuryUnit ();
	public static HKUnit FromMinuteUnit ();
	public static HKUnit FromMoleUnit (double gramsPerMole);
	public static HKUnit FromMoleUnit (HKMetricPrefix prefix, double gramsPerMole);
	public static HKUnit FromOunceUnit ();
	public static HKUnit FromPascalUnit (HKMetricPrefix prefix);
	public static HKUnit FromPascalUnit ();
	public static HKUnit FromPercentUnit ();
	public static HKUnit FromPoundUnit ();
	public static HKUnit FromSecondUnit (HKMetricPrefix prefix);
	public static HKUnit FromSecondUnit ();
	public static HKUnit FromSiemenUnit ();
	public static HKUnit FromSiemenUnit (HKMetricPrefix prefix);
	public static HKUnit FromStoneUnit ();
```

Added methods:

```
public static HKUnit CreateJouleUnit (HKMetricPrefix prefix);
	public static HKUnit CreateLeterUnit (HKMetricPrefix prefix);
	public static HKUnit CreateMeterUnit (HKMetricPrefix prefix);
	public static HKUnit CreateMoleUnit (double gramsPerMole);
	public static HKUnit CreateMoleUnit (HKMetricPrefix prefix, double gramsPerMole);
	public static HKUnit CreatePascalUnit (HKMetricPrefix prefix);
	public static HKUnit CreateSecondUnit (HKMetricPrefix prefix);
	public static HKUnit CreateSiemenUnit (HKMetricPrefix prefix);
	public static HKUnit FromEnergyFormatterUnit (MonoTouch.Foundation.NSEnergyFormatterUnit energyFormatterUnit);
	public static HKUnit FromLengthFormatterUnit (MonoTouch.Foundation.NSLengthFormatterUnit lengthFormatterUnit);
	public static HKUnit FromMassFormatterUnit (MonoTouch.Foundation.NSMassFormatterUnit massFormatterUnit);
	public static MonoTouch.Foundation.NSEnergyFormatterUnit GetEnergyFormatterUnit (HKUnit unit);
	public static MonoTouch.Foundation.NSLengthFormatterUnit GetLengthFormatterUnit (HKUnit unit);
	public static MonoTouch.Foundation.NSMassFormatterUnit GetMassFormatterUnit (HKUnit unit);
```

### Removed Type MonoTouch.HealthKit.HKAnchoredObjectQueryCtorCompletionHandler ### Removed Type MonoTouch.HealthKit.HKCategoryTypeIdentifier ### Removed Type MonoTouch.HealthKit.HKCharacteristicTypeIdentifier ### Removed Type MonoTouch.HealthKit.HKCorrelationQueryCtorCompletionHandler ### Removed Type MonoTouch.HealthKit.HKQuantityTypeIdentifier ### Removed Type MonoTouch.HealthKit.HKQuantityTypeIdentifierDietary ### Removed Type MonoTouch.HealthKit.HKStatisticsCollectionEnumerateStaticsHandler ### Removed Type MonoTouch.HealthKit.HKStatisticsQueryCompletionHandler ### New Type MonoTouch.HealthKit.HKAnchoredObjectResultHandler

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

### New Type MonoTouch.HealthKit.HKCategoryTypeIdentifierKey

```
public static class HKCategoryTypeIdentifierKey {
	// properties
	public static MonoTouch.Foundation.NSString SleepAnalysis { get; }
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

### New Type MonoTouch.HealthKit.HKMetadata

```
public class HKMetadata : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public HKMetadata ();
	public HKMetadata (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public HKBodyTemperatureSensorLocation? BodyTemperatureSensorLocation { get; set; }
	public string DeviceSerialNumber { get; set; }
	public string DigitalSignature { get; set; }
	public string FoodType { get; set; }
	public HKHeartRateSensorLocation? HeartRateSensorLocation { get; set; }
	public string UdiDeviceIdentifier { get; set; }
	public string UdiProductionIdentifier { get; set; }
}
```

### New Type MonoTouch.HealthKit.HKPrediateKeyPath

```
public static class HKPrediateKeyPath {
	// properties
	public static MonoTouch.Foundation.NSString CategoryValue { get; }
	public static MonoTouch.Foundation.NSString EndDate { get; }
	public static MonoTouch.Foundation.NSString Metadata { get; }
	public static MonoTouch.Foundation.NSString Quantity { get; }
	public static MonoTouch.Foundation.NSString Source { get; }
	public static MonoTouch.Foundation.NSString StartDate { get; }
}
```

### New Type MonoTouch.HealthKit.HKQuantityTypeIdentifierKey

```
public static class HKQuantityTypeIdentifierKey {
	// properties
	public static MonoTouch.Foundation.NSString ActiveEnergyBurned { get; }
	public static MonoTouch.Foundation.NSString ActivityCount { get; }
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
	public static MonoTouch.Foundation.NSString DietaryCalcium { get; }
	public static MonoTouch.Foundation.NSString DietaryCalories { get; }
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
	public static MonoTouch.Foundation.NSString Distance { get; }
	public static MonoTouch.Foundation.NSString FlightsClimbed { get; }
	public static MonoTouch.Foundation.NSString GalvanicSkinResponse { get; }
	public static MonoTouch.Foundation.NSString HeartRate { get; }
	public static MonoTouch.Foundation.NSString HeatFlux { get; }
	public static MonoTouch.Foundation.NSString Height { get; }
	public static MonoTouch.Foundation.NSString InhalerUsage { get; }
	public static MonoTouch.Foundation.NSString LeanBodyMass { get; }
	public static MonoTouch.Foundation.NSString NikeFuel { get; }
	public static MonoTouch.Foundation.NSString NumberOfTimesFallen { get; }
	public static MonoTouch.Foundation.NSString OxygenSaturation { get; }
	public static MonoTouch.Foundation.NSString PerfusionIndex { get; }
	public static MonoTouch.Foundation.NSString RespiratoryRate { get; }
	public static MonoTouch.Foundation.NSString RRInterval { get; }
	public static MonoTouch.Foundation.NSString StepCount { get; }
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





## Namespace MonoTouch.iAd



### Type Changed: MonoTouch.iAd.ADBannerView

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

## Namespace MonoTouch.LocalAuthentication



### Type Changed: MonoTouch.LocalAuthentication.LAContext

Added properties:

```
public virtual bool CancelButtonVisible { get; set; }
	public virtual bool FallbackButtonVisible { get; set; }
	public virtual string LocalizedFallbackTitle { get; set; }
```

### Removed Type MonoTouch.LocalAuthentication.LAOptions 

## Namespace MonoTouch.MapKit



### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added methods:

```
public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKAnnotationView.MKAnnotationViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added methods:

```
public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKCircleView.MKCircleViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKMapView

Added methods:

```
public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKMapView.MKMapViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added methods:

```
public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKOverlayPathView.MKOverlayPathViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added methods:

```
public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKOverlayView.MKOverlayViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

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

Added methods:

```
public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolygonView.MKPolygonViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added methods:

```
public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MKPolylineView.MKPolylineViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
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

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController

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

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

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



### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added methods:

```
public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MFMailComposeViewController.MFMailComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added methods:

```
public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static MFMessageComposeViewController.MFMessageComposeViewControllerAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.Metal



### Type Changed: MonoTouch.Metal.IMTLBlitCommandEncoder

Removed methods:

```
public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceRowBytes, uint sourceImageBytes, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinationRowBytes, uint destinationImageBytes);
```

Added methods:

```
public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceBytesPerRow, uint sourceBytesPerImage, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinatinBytesPerRow, uint destinationBytesPerImage);
```

### Type Changed: MonoTouch.Metal.IMTLCommandBuffer

Removed methods:

```
public virtual void AddScheduledPresent (IMTLDrawable drawable);
	public virtual IMTLParallelRenderPassEncoder ParallelRenderPassEncoder (IMTLFramebuffer framebuffer);
	public virtual IMTLRenderCommandEncoder RenderCommandEncoder (IMTLFramebuffer framebuffer);
```

### Type Changed: MonoTouch.Metal.IMTLDevice

Removed methods:

```
public virtual IMTLFramebuffer CreateFramebuffer (MTLFramebufferDescriptor descriptor);
	public virtual IMTLComputePipelineState NewComputePipelineStateWithFunction (IMTLFunction computeFunction, out MonoTouch.Foundation.NSError error);
```

Added method:

```
public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, out MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.Metal.IMTLFunctionArgument

Removed property:

```
public virtual MTLArgumentType ResourceType { get; }
```

Added property:

```
public virtual MTLArgumentType ArgumentType { get; }
```

### Type Changed: MonoTouch.Metal.IMTLRenderCommandEncoder

Added methods:

```
public virtual void SetFragmentBuffers (IMTLBuffer buffers, System.IntPtr IntPtrOffsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentTextures (IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexBuffers (IMTLBuffer[] buffers, System.IntPtr uintArrayPtrOffsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
```

### Type Changed: MonoTouch.Metal.IMTLTexture

Obsoleted methods:

```
[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromPixels (System.IntPtr pixels, uint rowBytes, uint imageBytes, uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size);

	[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromSlice (uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size, System.IntPtr destination, uint rowBytes, uint imageBytes);
```

### Type Changed: MonoTouch.Metal.MTLCommandBuffer_Extensions

Added methods:

```
public static MTLParallelRenderCommandEncoder CreateParallelRenderCommandEncoder (IMTLCommandBuffer This, MTLRenderPassDescriptor renderPassDescriptor);
	public static IMTLRenderCommandEncoder CreateRenderCommandEncoder (IMTLCommandBuffer This, MTLRenderPassDescriptor renderPassDescriptor);
	public static void PresentDrawable (IMTLCommandBuffer This, IMTLDrawable drawable);
```

### Type Changed: MonoTouch.Metal.MTLComputeCommandEncoder_Extensions

Added methods:

```
public static void SetBuffers (IMTLComputeCommandEncoder This, IMTLBuffer[] buffers, System.IntPtr offsets, MonoTouch.Foundation.NSRange range);
	public static void SetSamplerStates (IMTLComputeCommandEncoder This, IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public static void SetSamplerStates (IMTLComputeCommandEncoder This, IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public static void SetTextures (IMTLComputeCommandEncoder This, IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
```

### Type Changed: MonoTouch.Metal.MTLDepthStencilDescriptor

Removed properties:

```
public virtual MTLStencilDescriptor BackFaceStencilDescriptor { get; set; }
	public virtual MTLStencilDescriptor FrontFaceStencilDescriptor { get; set; }
```

Added properties:

```
public virtual MTLStencilDescriptor BackFaceStencil { get; set; }
	public virtual MTLStencilDescriptor FrontFaceStencil { get; set; }
```

### Type Changed: MonoTouch.Metal.MTLDevice

Added constructors:

```
public MTLDevice (MonoTouch.Foundation.NSCoder coder);
	public MTLDevice (MonoTouch.Foundation.NSObjectFlag t);
	public MTLDevice (System.IntPtr handle);
```

Added interfaces:

```
IMTLDevice
	MonoTouch.ObjCRuntime.INativeObject
	System.IDisposable
```

Added property:

```
public virtual string Name { get; }
```

Added methods:

```
public virtual IMTLBuffer CreateBuffer (uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBuffer (System.IntPtr pointer, uint length, MTLResourceOptions options);
	public virtual IMTLBuffer CreateBufferNoCopy (System.IntPtr pointer, uint length, MTLResourceOptions options, MTLDeallocator deallocator);
	public virtual IMTLCommandQueue CreateCommandQueue (uint maxCommandBufferCount);
	public virtual IMTLCommandQueue CreateCommandQueue ();
	public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, out MonoTouch.Foundation.NSError error);
	public virtual void CreateComputePipelineState (IMTLFunction computeFunction, System.Action<IMTLComputePipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLLibrary CreateDefaultLibrary ();
	public virtual IMTLDepthStencilState CreateDepthStencilState (MTLDepthStencilDescriptor descriptor);
	public virtual void CreateLibrary (string source, MTLCompileOptions options, System.Action<IMTLLibrary,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLLibrary CreateLibrary (string source, MTLCompileOptions options, out MonoTouch.Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (MonoTouch.Foundation.NSObject data, out MonoTouch.Foundation.NSError error);
	public virtual IMTLLibrary CreateLibrary (string filepath, out MonoTouch.Foundation.NSError error);
	public virtual IMTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, out MonoTouch.Foundation.NSError error);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, System.Action<IMTLRenderPipelineState,MonoTouch.Foundation.NSError> completionHandler);
	public virtual IMTLSamplerState CreateSamplerState (MTLSamplerDescriptor descriptor);
	public virtual IMTLTexture CreateTexture (MTLTextureDescriptor descriptor);
```

### Type Changed: MonoTouch.Metal.MTLPixelFormat

Added value:

```
A8Unorm = 1,
```

### Type Changed: MonoTouch.Metal.MTLRenderCommandEncoder_Extensions

Added method:

```
public static void SetVertexTextures (IMTLRenderCommandEncoder This, IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
```

### Type Changed: MonoTouch.Metal.MTLRenderPipelineDescriptor

Added properties:

```
public virtual MTLRenderPipelineAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLPixelFormat DepthAttachmentPixelFormat { get; set; }
	public virtual MTLPixelFormat StencilAttachmentPixelFormat { get; set; }
```

Removed methods:

```
public virtual MTLBlendDescriptor CopyBlendDescriptor (MTLFramebufferAttachmentIndex index);
	public virtual MTLPixelFormat GetPixelFormat (MTLFramebufferAttachmentIndex index);
	public virtual void SetBlendDescriptor (MTLBlendDescriptor blendDescriptor, MTLFramebufferAttachmentIndex index);
	public virtual void SetPixelFormat (MTLPixelFormat pixelFormat, MTLFramebufferAttachmentIndex index);
```

### Type Changed: MonoTouch.Metal.MTLTexture_Extensions

Added methods:

```
public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLTextureRegion region, uint level, uint slice);
	public static void GetBytes (IMTLTexture This, System.IntPtr pixelBytes, uint bytesPerRow, MTLTextureRegion region, uint level);
	public static void ReplaceRegion (IMTLTexture This, MTLTextureRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public static void ReplaceRegion (IMTLTexture This, MTLTextureRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
```

### Type Changed: MonoTouch.Metal.MTLVertexDescriptor

Removed methods:

```
public virtual uint GetInstanceStepRate (uint vertexBufferIndex);
	public virtual void SetStride (uint stride, uint instanceStepRate, uint vertexBufferIndex);
```

Added methods:

```
public virtual MTLVertexStepFunction GetStepFunction (uint vertexBufferIndex);
	public virtual uint GetStepRate (uint vertexBufferIndex);
	public virtual void SetStride (uint stride, uint vertexBufferIndex);
	public virtual void SetStride (uint stride, MTLVertexStepFunction stepFunction, uint instanceStepRate, uint vertexBufferIndex);
```

### Type Changed: MonoTouch.Metal.MTLVertexFormat

Removed values:

```
FormatInt = 32,
	FormatInt2 = 33,
	FormatInt2101010Normalized = 40,
	FormatInt3 = 34,
	FormatInt4 = 35,
	FormatUInt = 36,
	FormatUInt2 = 37,
	FormatUInt2101010Normalized = 41,
	FormatUInt3 = 38,
	FormatUInt4 = 39,
	SChar2 = 4,
	SChar2Normalized = 10,
	SChar3 = 5,
	SChar3Normalized = 11,
	SChar4 = 6,
	SChar4Normalized = 12,
```

Added values:

```
Char2 = 4,
	Char2Normalized = 10,
	Char3 = 5,
	Char3Normalized = 11,
	Char4 = 6,
	Char4Normalized = 12,
	Int = 32,
	Int2 = 33,
	Int2101010Normalized = 40,
	Int3 = 34,
	Int4 = 35,
	UInt = 36,
	UInt2 = 37,
	UInt2101010Normalized = 41,
	UInt3 = 38,
	UInt4 = 39,
```

### Removed Type MonoTouch.Metal.IMTLFramebuffer ### Removed Type MonoTouch.Metal.IMTLParallelRenderPassEncoder ### Removed Type MonoTouch.Metal.MTLAttachmentDescriptor ### Removed Type MonoTouch.Metal.MTLBlendDescriptor ### Removed Type MonoTouch.Metal.MTLFramebuffer_Extensions ### Removed Type MonoTouch.Metal.MTLFramebufferAttachmentIndex ### Removed Type MonoTouch.Metal.MTLFramebufferDescriptor ### Removed Type MonoTouch.Metal.MTLParallelRenderPassEncoder_Extensions ### New Type MonoTouch.Metal.IMTLParallelRenderCommandEncoder

```
public interface IMTLParallelRenderCommandEncoder : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, IMTLCommandEncoder {
	// methods
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder ();
}
```

### New Type MonoTouch.Metal.MTLBlitCommandEncoder

```
public abstract class MTLBlitCommandEncoder : MonoTouch.Foundation.NSObject, IMTLBlitCommandEncoder, IMTLCommandEncoder, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLBlitCommandEncoder ();
	public MTLBlitCommandEncoder (MonoTouch.Foundation.NSCoder coder);
	public MTLBlitCommandEncoder (MonoTouch.Foundation.NSObjectFlag t);
	public MTLBlitCommandEncoder (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, uint sourceBytesPerRow, uint sourceBytesPerImage, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromBuffer (IMTLBuffer sourceBuffer, uint sourceOffset, IMTLBuffer destinationBuffer, uint destinationOffset, uint size);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLTexture destinationTexture, uint destinationSlice, uint destinationLevel, MTLOrigin destinationOrigin);
	public virtual void CopyFromTexture (IMTLTexture sourceTexture, uint sourceSlice, uint sourceLevel, MTLOrigin sourceOrigin, MTLSize sourceSize, IMTLBuffer destinationBuffer, uint destinationOffset, uint destinatinBytesPerRow, uint destinationBytesPerImage);
	public virtual void EndEncoding ();
	public virtual void FillBuffer (IMTLBuffer buffer, MonoTouch.Foundation.NSRange range, byte value);
	public virtual void GenerateMipmapsForTexture (IMTLTexture texture);
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
}
```

### New Type MonoTouch.Metal.MTLBuffer

```
public abstract class MTLBuffer : MonoTouch.Foundation.NSObject, IMTLBuffer, IMTLResource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLBuffer ();
	public MTLBuffer (MonoTouch.Foundation.NSCoder coder);
	public MTLBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public MTLBuffer (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Contents { get; }
	public virtual MTLCpuCacheMode CpuCacheMode { get; }
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	public virtual uint Length { get; }
	// methods
	public virtual IMTLTexture CreateTexture (MTLTextureDescriptor descriptor, uint offset, uint bytesPerRow);
	public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);
}
```

### New Type MonoTouch.Metal.MTLCommandBuffer

```
public abstract class MTLCommandBuffer : MonoTouch.Foundation.NSObject, IMTLCommandBuffer, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLCommandBuffer ();
	public MTLCommandBuffer (MonoTouch.Foundation.NSCoder coder);
	public MTLCommandBuffer (MonoTouch.Foundation.NSObjectFlag t);
	public MTLCommandBuffer (System.IntPtr handle);
	// properties
	public virtual IMTLBlitCommandEncoder BlitCommandEncoder { get; }
	public virtual IMTLCommandQueue CommandQueue { get; }
	public virtual IMTLComputeCommandEncoder ComputeCommandEncoder { get; }
	public virtual IMTLDevice Device { get; }
	public virtual MonoTouch.Foundation.NSError Error { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public virtual string Label { get; set; }
	public virtual bool RetainedReferences { get; }
	public virtual MTLCommandBufferStatus Status { get; }
	// methods
	public virtual void AddCompletedHandler (System.Action<IMTLCommandBuffer> block);
	public virtual void AddScheduledHandler (System.Action<IMTLCommandBuffer> block);
	public virtual void Commit ();
	public virtual MTLParallelRenderCommandEncoder CreateParallelRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual void Enqueue ();
	public virtual void PresentDrawable (IMTLDrawable drawable);
	public virtual void WaitUntilCompleted ();
	public virtual void WaitUntilScheduled ();
}
```

### New Type MonoTouch.Metal.MTLCommandEncoder

```
public abstract class MTLCommandEncoder : MonoTouch.Foundation.NSObject, IMTLCommandEncoder, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLCommandEncoder ();
	public MTLCommandEncoder (MonoTouch.Foundation.NSCoder coder);
	public MTLCommandEncoder (MonoTouch.Foundation.NSObjectFlag t);
	public MTLCommandEncoder (System.IntPtr handle);
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

### New Type MonoTouch.Metal.MTLCommandQueue

```
public abstract class MTLCommandQueue : MonoTouch.Foundation.NSObject, IMTLCommandQueue, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLCommandQueue ();
	public MTLCommandQueue (MonoTouch.Foundation.NSCoder coder);
	public MTLCommandQueue (MonoTouch.Foundation.NSObjectFlag t);
	public MTLCommandQueue (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLCommandBuffer CommandBuffer ();
	public virtual IMTLCommandBuffer CommandBufferWithUnretainedReferences ();
	public virtual void InsertDebugCaptureBoundary ();
}
```

### New Type MonoTouch.Metal.MTLComputeCommandEncoder

```
public abstract class MTLComputeCommandEncoder : MonoTouch.Foundation.NSObject, IMTLComputeCommandEncoder, IMTLCommandEncoder, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLComputeCommandEncoder ();
	public MTLComputeCommandEncoder (MonoTouch.Foundation.NSCoder coder);
	public MTLComputeCommandEncoder (MonoTouch.Foundation.NSObjectFlag t);
	public MTLComputeCommandEncoder (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual void EndEncoding ();
	public virtual void ExecuteBarrier ();
	public virtual void ExecuteKernelWithWorkGroupSize (MTLSize workGroupSize, MTLSize workGroupCount);
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
	public virtual void SetBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetBuffers (IMTLBuffer[] buffers, System.IntPtr offsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetComputePipelineState (IMTLComputePipelineState state);
	public virtual void SetLocalMemorySize (uint localMemorySize, uint index);
	public virtual void SetSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetTexture (IMTLTexture texture, uint index);
	public virtual void SetTextures (IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
}
```

### New Type MonoTouch.Metal.MTLComputePipelineState

```
public abstract class MTLComputePipelineState : MonoTouch.Foundation.NSObject, IMTLComputePipelineState, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLComputePipelineState ();
	public MTLComputePipelineState (MonoTouch.Foundation.NSCoder coder);
	public MTLComputePipelineState (MonoTouch.Foundation.NSObjectFlag t);
	public MTLComputePipelineState (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual uint MaxWorkGroupSize { get; }
	public virtual uint PreferredWorkGroupFactor { get; }
}
```

### New Type MonoTouch.Metal.MTLDepthStencilState

```
public class MTLDepthStencilState : MonoTouch.Foundation.NSObject, IMTLDepthStencilState, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLDepthStencilState ();
	public MTLDepthStencilState (MonoTouch.Foundation.NSCoder coder);
	public MTLDepthStencilState (MonoTouch.Foundation.NSObjectFlag t);
	public MTLDepthStencilState (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
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
}
```

### New Type MonoTouch.Metal.MTLFunction

```
public abstract class MTLFunction : MonoTouch.Foundation.NSObject, IMTLFunction, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLFunction ();
	public MTLFunction (MonoTouch.Foundation.NSCoder coder);
	public MTLFunction (MonoTouch.Foundation.NSObjectFlag t);
	public MTLFunction (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual IMTLFunctionArgument[] FunctionArguments { get; }
	public virtual MTLFunctionType FunctionType { get; }
	public virtual string Name { get; }
}
```

### New Type MonoTouch.Metal.MTLFunctionArgument

```
public abstract class MTLFunctionArgument : MonoTouch.Foundation.NSObject, IMTLFunctionArgument, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLFunctionArgument ();
	public MTLFunctionArgument (MonoTouch.Foundation.NSCoder coder);
	public MTLFunctionArgument (MonoTouch.Foundation.NSObjectFlag t);
	public MTLFunctionArgument (System.IntPtr handle);
	// properties
	public virtual MTLArgumentType ArgumentType { get; }
	public virtual uint BindingIndex { get; }
	public virtual string Name { get; }
}
```

### New Type MonoTouch.Metal.MTLLibrary

```
public abstract class MTLLibrary : MonoTouch.Foundation.NSObject, IMTLLibrary, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLLibrary ();
	public MTLLibrary (MonoTouch.Foundation.NSCoder coder);
	public MTLLibrary (MonoTouch.Foundation.NSObjectFlag t);
	public MTLLibrary (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public static MonoTouch.Foundation.NSString ErrorDomain { get; }
	public virtual string[] FunctionNames { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLFunction CreateFunction (string functionName);
}
```

### New Type MonoTouch.Metal.MTLParallelRenderCommandEncoder

```
public abstract class MTLParallelRenderCommandEncoder : MonoTouch.Foundation.NSObject, IMTLParallelRenderCommandEncoder, IMTLCommandEncoder, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLParallelRenderCommandEncoder ();
	public MTLParallelRenderCommandEncoder (MonoTouch.Foundation.NSCoder coder);
	public MTLParallelRenderCommandEncoder (MonoTouch.Foundation.NSObjectFlag t);
	public MTLParallelRenderCommandEncoder (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder ();
	public virtual void EndEncoding ();
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
}
```

### New Type MonoTouch.Metal.MTLParallelRenderCommandEncoder_Extensions

```
public static class MTLParallelRenderCommandEncoder_Extensions {
}
```

### New Type MonoTouch.Metal.MTLRenderCommandEncoder

```
public abstract class MTLRenderCommandEncoder : MonoTouch.Foundation.NSObject, IMTLRenderCommandEncoder, IMTLCommandEncoder, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderCommandEncoder ();
	public MTLRenderCommandEncoder (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderCommandEncoder (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderCommandEncoder (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset, uint instanceCount);
	public virtual void DrawIndexedPrimitives (MTLPrimitiveType primitiveType, uint indexCount, MTLIndexType indexType, IMTLBuffer indexBuffer, uint indexBufferOffset);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount, uint instanceCount);
	public virtual void DrawPrimitives (MTLPrimitiveType primitiveType, uint vertexStart, uint vertexCount);
	public virtual void EndEncoding ();
	public virtual void InsertDebugSignpost (string signpost);
	public virtual void PopDebugGroup ();
	public virtual void PushDebugGroup (string debugGroup);
	public virtual void SetBlendColor (float red, float green, float blue, float alpha);
	public virtual void SetCullMode (MTLCullMode cullMode);
	public virtual void SetDepthBias (float depthBias, float slopeScale, float clamp);
	public virtual void SetDepthClipMode (MTLDepthClipMode depthClipMode);
	public virtual void SetDepthStencilState (IMTLDepthStencilState depthStencilState);
	public virtual void SetFragmentBuffer (IMTLBuffer buffer, uint offset, uint index);
	public virtual void SetFragmentBuffers (IMTLBuffer buffers, System.IntPtr IntPtrOffsets, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, uint index);
	public virtual void SetFragmentSamplerState (IMTLSamplerState sampler, float lodMinClamp, float lodMaxClamp, uint index);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetFragmentSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
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
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexSamplerStates (IMTLSamplerState[] samplers, System.IntPtr floatArrayPtrLodMinClamps, System.IntPtr floatArrayPtrLodMaxClamps, MonoTouch.Foundation.NSRange range);
	public virtual void SetVertexTexture (IMTLTexture texture, uint index);
	public virtual void SetVertexTextures (IMTLTexture[] textures, MonoTouch.Foundation.NSRange range);
	public virtual void SetViewport (MTLViewport viewport);
	public virtual void SetVisibilityResultMode (MTLVisibilityResultMode mode, uint offset);
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
	public virtual MTLClearValue ClearValue { get; set; }
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

### New Type MonoTouch.Metal.MTLRenderPassAttachmentDescriptorArray

```
public class MTLRenderPassAttachmentDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPassAttachmentDescriptorArray ();
	public MTLRenderPassAttachmentDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPassAttachmentDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPassAttachmentDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MTLRenderPassAttachmentDescriptor Item { get; set; }
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
	public virtual MTLRenderPassAttachmentDescriptorArray ColorAttachments { get; }
	public virtual MTLRenderPassAttachmentDescriptor DepthAttachment { get; set; }
	public virtual MTLRenderPassAttachmentDescriptor StencilAttachment { get; set; }
	public virtual IMTLBuffer VisibilityResultBuffer { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public static MTLRenderPassDescriptor CreateRenderPassDescriptor ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineAttachmentDescriptor

```
public class MTLRenderPipelineAttachmentDescriptor : MonoTouch.Foundation.NSObject, MonoTouch.Foundation.INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineAttachmentDescriptor ();
	public MTLRenderPipelineAttachmentDescriptor (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineAttachmentDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineAttachmentDescriptor (System.IntPtr handle);
	// properties
	public virtual MTLBlendOperation AlphaBlendOperation { get; set; }
	public virtual bool BlendingEnabled { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MTLBlendFactor DestinationAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor DestinationRGBBlendFactor { get; set; }
	public virtual MTLPixelFormat PixelFormat { get; set; }
	public virtual MTLBlendOperation RgbBlendOperation { get; set; }
	public virtual MTLBlendFactor SourceAlphaBlendFactor { get; set; }
	public virtual MTLBlendFactor SourceRGBBlendFactor { get; set; }
	public virtual MTLColorWriteMask WriteMask { get; set; }
	// methods
	public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineAttachmentDescriptorArray

```
public class MTLRenderPipelineAttachmentDescriptorArray : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineAttachmentDescriptorArray ();
	public MTLRenderPipelineAttachmentDescriptorArray (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineAttachmentDescriptorArray (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineAttachmentDescriptorArray (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MTLRenderPipelineAttachmentDescriptor Item { get; set; }
}
```

### New Type MonoTouch.Metal.MTLRenderPipelineState

```
public abstract class MTLRenderPipelineState : MonoTouch.Foundation.NSObject, IMTLRenderPipelineState, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLRenderPipelineState ();
	public MTLRenderPipelineState (MonoTouch.Foundation.NSCoder coder);
	public MTLRenderPipelineState (MonoTouch.Foundation.NSObjectFlag t);
	public MTLRenderPipelineState (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
```

### New Type MonoTouch.Metal.MTLResource

```
public abstract class MTLResource : MonoTouch.Foundation.NSObject, IMTLResource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLResource ();
	public MTLResource (MonoTouch.Foundation.NSCoder coder);
	public MTLResource (MonoTouch.Foundation.NSObjectFlag t);
	public MTLResource (System.IntPtr handle);
	// properties
	public virtual MTLCpuCacheMode CpuCacheMode { get; }
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; set; }
	// methods
	public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);
}
```

### New Type MonoTouch.Metal.MTLSamplerState

```
public abstract class MTLSamplerState : MonoTouch.Foundation.NSObject, IMTLSamplerState, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLSamplerState ();
	public MTLSamplerState (MonoTouch.Foundation.NSCoder coder);
	public MTLSamplerState (MonoTouch.Foundation.NSObjectFlag t);
	public MTLSamplerState (System.IntPtr handle);
	// properties
	public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
}
```

### New Type MonoTouch.Metal.MTLTexture

```
public abstract class MTLTexture : MonoTouch.Foundation.NSObject, IMTLTexture, IMTLResource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MTLTexture ();
	public MTLTexture (MonoTouch.Foundation.NSCoder coder);
	public MTLTexture (MonoTouch.Foundation.NSObjectFlag t);
	public MTLTexture (System.IntPtr handle);
	// properties
	public virtual uint ArrayLength { get; }
	public virtual MTLCpuCacheMode CpuCacheMode { get; }
	public virtual uint Depth { get; }
	public virtual IMTLDevice Device { get; }
	public virtual bool FramebufferOnly { get; }
	public virtual uint Height { get; }
	public virtual string Label { get; set; }
	public virtual uint MipmapLevelCount { get; }
	public virtual MTLPixelFormat PixelFormat { get; }
	public virtual IMTLResource RootResource { get; }
	public virtual uint SampleCount { get; }
	public virtual MTLTextureType TextureType { get; }
	public virtual uint Width { get; }
	// methods

	[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromPixels (System.IntPtr pixels, uint rowBytes, uint imageBytes, uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size);

	[Obsolete ("OBSOLETE, but needed for some samples for now")]
	public virtual void CopyFromSlice (uint slice, uint mipmapLevel, MTLOrigin origin, MTLSize size, System.IntPtr destination, uint rowBytes, uint imageBytes);
	public virtual IMTLTexture CreateTextureView (MTLPixelFormat pixelFormat);
	public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, MTLTextureRegion region, uint level);
	public virtual void GetBytes (System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLTextureRegion region, uint level, uint slice);
	public virtual void ReplaceRegion (MTLTextureRegion region, uint level, uint slice, System.IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public virtual void ReplaceRegion (MTLTextureRegion region, uint level, System.IntPtr pixelBytes, uint bytesPerRow);
	public virtual MTLPurgeableState SetPurgeableState (MTLPurgeableState state);
}
```

### New Type MonoTouch.Metal.MTLTextureRegion

```
public struct MTLTextureRegion {
	// constructors
	public MTLTextureRegion (MTLOrigin origin, MTLSize size);
	// fields
	public MTLOrigin Origin;
	public MTLSize Size;
	// methods
	public static MTLTextureRegion Create1D (uint x, uint width);
	public static MTLTextureRegion Create2D (uint x, uint y, uint width, uint height);
	public static MTLTextureRegion Create3D (uint x, uint y, uint z, uint width, uint height, uint depth);
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

## Namespace MonoTouch.NotificationCenter



### Type Changed: MonoTouch.NotificationCenter.NCWidgetController

Removed constructor:

```
public NCWidgetController ();
```

Removed method:

```
public static NCWidgetController WidgetController ();
```

Added method:

```
public static NCWidgetController GetWidgetController ();
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

### New Type MonoTouch.ObjCRuntime.iOSAttribute

```
public sealed class iOSAttribute : MonoTouch.ObjCRuntime.AvailabilityAttribute {
	// constructors
	public iOSAttribute (byte major, byte minor);
}
```

### New Type MonoTouch.ObjCRuntime.MacAttribute

```
public sealed class MacAttribute : MonoTouch.ObjCRuntime.AvailabilityAttribute {
	// constructors
	public MacAttribute (byte major, byte minor, bool onlyOn64);
}
```

## Namespace MonoTouch.Photos



### Type Changed: MonoTouch.Photos.PHAssetCollectionSubtype

Added values:

```
SmartAlbumBursts = 207,
	SmartAlbumSlomoVideos = 208,
```

### Type Changed: MonoTouch.Photos.PHFetchResult

Added method:

```
public virtual uint CountOfAssetsWithMediaType (PHAssetMediaType mediaType);
```

### Type Changed: MonoTouch.Photos.PHVideoRequestOptionsDeliveryMode

Removed value:

```
FastFormat = 2,
```

Added values:

```
FastFormat = 3,
	MediumQualityFormat = 2,
```

## Namespace MonoTouch.SceneKit



### Type Changed: MonoTouch.SceneKit.SCNAction

Added methods:

```
public static SCNAction CustomAction (double seconds, SCNActionNodeWithElapsedTimeHandler handler);
	public static SCNAction FadeIn (double durationInSeconds);
	public static SCNAction FadeOpacityBy (float factor, double durationInSeconds);
	public static SCNAction FadeOpacityTo (float opacity, double durationInSeconds);
	public static SCNAction FadeOut (double durationInSeconds);
	public static SCNAction Group (SCNAction[] actions);
	public static SCNAction JavaScriptAction (string script, double seconds);
	public static SCNAction MoveBy (SCNVector3 delta, double durationInSeconds);
	public static SCNAction MoveBy (float deltaX, float deltaY, float deltaZ, double durationInSeconds);
	public static SCNAction MoveTo (SCNVector3 location, double durationInSeconds);
	public static SCNAction RemoveFromParentNode ();
	public static SCNAction RepeatAction (SCNAction action, uint count);
	public static SCNAction RepeatActionForever (SCNAction action);
	public static SCNAction RotateBy (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction RotateBy (float angle, SCNVector3 axis, double durationInSeconds);
	public static SCNAction RotateTo (SCNVector4 axisAngle, double durationInSeconds);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds, bool shortestUnitArc);
	public static SCNAction RotateTo (float xAngle, float yAngle, float zAngle, double durationInSeconds);
	public static SCNAction Run (System.Action handler);
	public static SCNAction Run (System.Action handler, MonoTouch.CoreFoundation.DispatchQueue queue);
	public static SCNAction ScaleBy (float scale, double durationInSeconds);
	public static SCNAction ScaleTo (float scale, double durationInSeconds);
	public static SCNAction Sequence (SCNAction[] actions);
	public static SCNAction Wait (double durationInSeconds);
	public static SCNAction Wait (double durationInSeconds, double durationRange);
```

### Type Changed: MonoTouch.SceneKit.SCNCamera

Removed property:

```
public virtual MonoTouch.CoreAnimation.CATransform3D ProjectionTransform { get; set; }
```

Added property:

```
public virtual SCNMatrix4 ProjectionTransform { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNGeometry

Removed property:

```
public virtual MonoTouch.Foundation.NSDictionary ShaderModifiers { get; set; }
```

Added properties:

```
public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNHitTest

Removed property:

```
public static MonoTouch.Foundation.NSString IgnoreHiddenNodes { get; }
```

Added property:

```
public static MonoTouch.Foundation.NSString IgnoreHiddenNodesKey { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNHitTestOptions

Removed property:

```
public bool? ClipToZRange { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNHitTestResult

Removed property:

```
public virtual MonoTouch.CoreAnimation.CATransform3D ModelTransform { get; }
```

Added property:

```
public virtual SCNMatrix4 ModelTransform { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNMaterial

Removed property:

```
public virtual MonoTouch.Foundation.NSDictionary ShaderModifiers { get; set; }
```

Added properties:

```
public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNMaterialProperty

Removed property:

```
public virtual MonoTouch.CoreAnimation.CATransform3D ContentsTransform { get; set; }
```

Added properties:

```
public virtual SCNMatrix4 ContentsTransform { get; set; }
	public virtual float Intensity { get; set; }
	public virtual float MaxAnisotropy { get; set; }
```

Added method:

```
public static SCNMaterialProperty Create (MonoTouch.Foundation.NSObject contents);
```

### Type Changed: MonoTouch.SceneKit.SCNNode

Removed properties:

```
public virtual MonoTouch.CoreAnimation.CATransform3D Pivot { get; set; }
	public virtual MonoTouch.CoreAnimation.CATransform3D Transform { get; set; }
	public virtual MonoTouch.CoreAnimation.CATransform3D WorldTransform { get; }
```

Added properties:

```
public virtual SCNMatrix4 Pivot { get; set; }
	public virtual SCNMatrix4 Transform { get; set; }
	public virtual SCNMatrix4 WorldTransform { get; }
```

Removed methods:

```
public virtual SCNVector3 ConvertPosition (SCNVector3 position, SCNNode node);
	public virtual MonoTouch.CoreAnimation.CATransform3D ConvertTransform (MonoTouch.CoreAnimation.CATransform3D transform, SCNNode node);
```

Added methods:

```
public virtual SCNVector3 ConvertPositionFromNode (SCNVector3 position, SCNNode node);
	public virtual SCNVector3 ConvertPositionToNode (SCNVector3 position, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformFromNode (SCNMatrix4 transform, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformToNode (SCNMatrix4 transform, SCNNode node);
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsTestKeys

Removed properties:

```
public static MonoTouch.Foundation.NSString BackfaceCulling { get; }
	public static MonoTouch.Foundation.NSString CollisionBitMask { get; }
	public static MonoTouch.Foundation.NSString SearchMode { get; }
```

Added properties:

```
public static MonoTouch.Foundation.NSString BackfaceCullingKey { get; }
	public static MonoTouch.Foundation.NSString CollisionBitMaskKey { get; }
	public static MonoTouch.Foundation.NSString SearchModeKey { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNPhysicsWorld

Removed method:

```
public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, MonoTouch.CoreAnimation.CATransform3D from, MonoTouch.CoreAnimation.CATransform3D to, MonoTouch.Foundation.NSDictionary options);
```

Added methods:

```
public SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, SCNPhysicsTest options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, SCNPhysicsTest options);
	public SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, MonoTouch.Foundation.NSDictionary options);
	public SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, SCNPhysicsTest options);
```

### Type Changed: MonoTouch.SceneKit.SCNProgramSemanticOptions

Removed property:

```
public uint? ProgrammChannel { get; set; }
```

Added property:

```
public uint? MappingChannel { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNScene

Removed methods:

```
public virtual void AddParticleSystem (SCNParticleSystem system, MonoTouch.CoreAnimation.CATransform3D transform);
	public static SCNScene Create (string name, string directory, MonoTouch.Foundation.NSDictionary options);
	public static SCNScene Create (string name, string directory, SCNSceneLoadingOptions options);
```

Added methods:

```
public virtual void AddParticleSystem (SCNParticleSystem system, SCNMatrix4 transform);
	public static SCNScene FromFile (string name);
	public static SCNScene FromFile (string name, string directory, SCNSceneLoadingOptions options);
	public static SCNScene FromFile (string name, string directory, MonoTouch.Foundation.NSDictionary options);
```

### Type Changed: MonoTouch.SceneKit.SCNSceneLoadingOptions

Removed property:

```
public bool? OverrideAssetURLs { get; set; }
```

Added property:

```
public bool? OverrideAssetUrls { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNSceneSourceLoading

Removed properties:

```
public static MonoTouch.Foundation.NSString AssetDirectoryURLsKey { get; }
	public static MonoTouch.Foundation.NSString OverrideAssetURLsKey { get; }
```

Added properties:

```
public static MonoTouch.Foundation.NSString AssetDirectoryUrlsKey { get; }
	public static MonoTouch.Foundation.NSString OverrideAssetUrlsKey { get; }
```

### Type Changed: MonoTouch.SceneKit.SCNShadable

Removed property:

```
public virtual MonoTouch.Foundation.NSDictionary ShaderModifiers { get; set; }
```

Added properties:

```
public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoTouch.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNShaderModifiers

Added constructors:

```
public SCNShaderModifiers ();
	public SCNShaderModifiers (MonoTouch.Foundation.NSDictionary dictionary);
```

Removed properties:

```
public static MonoTouch.Foundation.NSString EntryPointFragment { get; }
	public static MonoTouch.Foundation.NSString EntryPointGeometry { get; }
	public static MonoTouch.Foundation.NSString EntryPointLightingModel { get; }
	public static MonoTouch.Foundation.NSString EntryPointSurface { get; }
```

Added properties:

```
public string EntryPointFragment { get; set; }
	public string EntryPointGeometry { get; set; }
	public string EntryPointLightingModel { get; set; }
	public string EntryPointSurface { get; set; }
```

### Type Changed: MonoTouch.SceneKit.SCNShadowMode

Removed value:

```
Modulated = 2,
```

Added value:

```
Projected = 2,
```

### Type Changed: MonoTouch.SceneKit.SCNSkinner

Removed properties:

```
public virtual MonoTouch.CoreAnimation.CATransform3D BaseGeometryBindTransform { get; set; }
	public MonoTouch.CoreAnimation.CATransform3D[] BoneInverseBindTransforms { get; }
```

Added properties:

```
public virtual SCNMatrix4 BaseGeometryBindTransform { get; set; }
	public SCNMatrix4[] BoneInverseBindTransforms { get; }
```

Removed method:

```
public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, MonoTouch.CoreAnimation.CATransform3D[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
```

Added method:

```
public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, SCNMatrix4[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
```

### Type Changed: MonoTouch.SceneKit.SCNTransformConstraintHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, MonoTouch.CoreAnimation.CATransform3D transform, System.AsyncCallback callback, object object);
	public virtual MonoTouch.CoreAnimation.CATransform3D EndInvoke (System.IAsyncResult result);
	public virtual MonoTouch.CoreAnimation.CATransform3D Invoke (SCNNode node, MonoTouch.CoreAnimation.CATransform3D transform);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, SCNMatrix4 transform, System.AsyncCallback callback, object object);
	public virtual SCNMatrix4 EndInvoke (System.IAsyncResult result);
	public virtual SCNMatrix4 Invoke (SCNNode node, SCNMatrix4 transform);
```

### Type Changed: MonoTouch.SceneKit.SCNVector3

Removed constructor:

```
public SCNVector3 (OpenTK.Vector3 vector);
```

Added constructors:

```
public SCNVector3 (SCNVector3 v);
	public SCNVector3 (SCNVector4 v);
```

Added interface:

```
System.IEquatable<SCNVector3>
```

Added fields:

```
public static SCNVector3 One;
	public static int SizeInBytes;
	public static SCNVector3 UnitX;
	public static SCNVector3 UnitY;
	public static SCNVector3 UnitZ;
	public static SCNVector3 Zero;
```

Added properties:

```
public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public OpenTK.Vector2 Xy { get; set; }
```

Added methods:

```
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
```

### Type Changed: MonoTouch.SceneKit.SCNVector4

Removed constructor:

```
public SCNVector4 (OpenTK.Vector4 vector);
```

Added constructors:

```
public SCNVector4 (OpenTK.Vector2 v);
	public SCNVector4 (SCNVector3 v);
	public SCNVector4 (SCNVector3 v, float w);
	public SCNVector4 (SCNVector4 v);
	public SCNVector4 (OpenTK.Vector4 source);
```

Added interface:

```
System.IEquatable<SCNVector4>
```

Added fields:

```
public static SCNVector4 One;
	public static int SizeInBytes;
	public static SCNVector4 UnitW;
	public static SCNVector4 UnitX;
	public static SCNVector4 UnitY;
	public static SCNVector4 UnitZ;
	public static SCNVector4 Zero;
```

Added properties:

```
public float Length { get; }
	public float LengthFast { get; }
	public float LengthSquared { get; }
	public OpenTK.Vector2 Xy { get; set; }
	public SCNVector3 Xyz { get; set; }
```

Added methods:

```
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
	public static System.IntPtr op_Explicit (SCNVector4 v);
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
```

### Type Changed: MonoTouch.SceneKit.SCNView

Added methods:

```
public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static SCNView.SCNViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.SceneKit.SCNWrapMode

Removed values:

```
Clamp = 0,
	ClampToBorder = 2,
	Mirror = 3,
	Repeat = 1,
```

Added values:

```
Clamp = 1,
	ClampToBorder = 3,
	Mirror = 4,
	Repeat = 2,
```

### Removed Type MonoTouch.SceneKit.SCNActions ### Removed Type MonoTouch.SceneKit.SCNLightAttribute ### Removed Type MonoTouch.SceneKit.SCNPhysicsTestSearchModeAny ### New Type MonoTouch.SceneKit._SCNShaderModifiers

```
public static class _SCNShaderModifiers {
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

### New Type MonoTouch.SceneKit.SCNPhysicsSearchMode

```
[Serializable]
public enum SCNPhysicsSearchMode {
	All = 2,
	Any = 0,
	Closest = 1,
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

### New Type MonoTouch.SceneKit.SCNPhysicsTestSearchModeKeys

```
public static class SCNPhysicsTestSearchModeKeys {
	// properties
	public static MonoTouch.Foundation.NSString All { get; }
	public static MonoTouch.Foundation.NSString Any { get; }
	public static MonoTouch.Foundation.NSString Closest { get; }
}
```





## Namespace MonoTouch.SpriteKit



### Type Changed: MonoTouch.SpriteKit.SKFieldForceEvaluator

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (OpenTK.Vector3 position, OpenTK.Vector3 velocity, float mass, float charge, double time, System.AsyncCallback callback, object object);
	public virtual OpenTK.Vector3 Invoke (OpenTK.Vector3 position, OpenTK.Vector3 velocity, float mass, float charge, double time);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (OpenTK.Vector4 position, OpenTK.Vector4 velocity, float mass, float charge, double time, System.AsyncCallback callback, object object);
	public virtual OpenTK.Vector3 Invoke (OpenTK.Vector4 position, OpenTK.Vector4 velocity, float mass, float charge, double time);
```

### Type Changed: MonoTouch.SpriteKit.SKFieldNode

Removed property:

```
public virtual OpenTK.Vector3 Direction { get; set; }
```

Added property:

```
public virtual OpenTK.Vector4 Direction { get; set; }
```

Removed methods:

```
public static SKFieldNode CreateLinearGravityField (OpenTK.Vector3 direction);
	public static SKFieldNode CreateVelocityField (OpenTK.Vector3 direction);
```

Added methods:

```
public static SKFieldNode CreateLinearGravityField (OpenTK.Vector4 direction);
	public static SKFieldNode CreateVelocityField (OpenTK.Vector4 direction);
```

### Type Changed: MonoTouch.SpriteKit.SKMutableTexture

Added constructor:

```
public SKMutableTexture (System.Drawing.SizeF size, MonoTouch.CoreVideo.CVPixelFormatType pixelFormat);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsWorld

Removed methods:

```
public virtual MonoTouch.CoreGraphics.CGVector SampleField (SKFieldNode field, System.Drawing.PointF position);
	public virtual MonoTouch.CoreGraphics.CGVector SampleFields (System.Drawing.PointF position);
```

Added method:

```
public virtual OpenTK.Vector3 SampleFields (OpenTK.Vector3 position);
```

### Type Changed: MonoTouch.SpriteKit.SKView

Added methods:

```
public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
	public static SKView.SKViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
```

## Namespace MonoTouch.UIKit



### Type Changed: MonoTouch.UIKit.UIAccessibility

Added properties:

```
public static bool IsSpeakScreenEnabled { get; }
	public static bool IsSpeakSelectionEnabled { get; }
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added methods:

```
public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIActionSheet.UIActionSheetAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added methods:

```
public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIActivityIndicatorView.UIActivityIndicatorViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIAlertAction

Removed methods:

```
public static System.Threading.Tasks.Task<UIAlertAction> CreateAsync (string title, UIAlertActionStyle style);
	public static System.Threading.Tasks.Task<UIAlertAction> CreateAsync (string title, UIAlertActionStyle style, out UIAlertAction result);
```

### Type Changed: MonoTouch.UIKit.UIAlertView

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

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added method:

```
public virtual void UserActivityUpdated (MonoTouch.Foundation.NSUserActivity userActivity);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Added method:

```
public static void UserActivityUpdated (IUIApplicationDelegate This, MonoTouch.Foundation.NSUserActivity userActivity);
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added methods:

```
public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIBarButtonItem.UIBarButtonItemAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIBarItem

Removed properties:

```
public static int UIAccessibilityPauseAssistiveTechnologyNotification { get; }
	public static int UIAccessibilityResumeAssistiveTechnologyNotification { get; }
```

Added properties:

```
public virtual UIAccessibilityNavigationStyle AccessibilityNavigationStyle { get; set; }
	public static int PauseAssistiveTechnologyNotification { get; }
	public static int ResumeAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakScreenStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakSelectionStatusDidChangeNotification { get; }
```

Added methods:

```
public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIBarItem.UIBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIBarItem.Notifications

Added methods:

```
public static MonoTouch.Foundation.NSObject ObserveSpeakScreenStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakSelectionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

### Type Changed: MonoTouch.UIKit.UIButton

Added methods:

```
public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIButton.UIButtonAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added methods:

```
public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UICollectionReusableView.UICollectionReusableViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Added methods:

```
public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UICollectionView.UICollectionViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added methods:

```
public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	public static UICollectionViewCell.UICollectionViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIControl

Added methods:

```
public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIControl.UIControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added methods:

```
public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIDatePicker.UIDatePickerAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
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

### Type Changed: MonoTouch.UIKit.UIImageView

Added methods:

```
public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIImageView.UIImageViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIInputView

Added methods:

```
public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIInputView.UIInputViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UILabel

Added methods:

```
public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits);
	public static UILabel.UILabelAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added methods:

```
public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UINavigationBar.UINavigationBarAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Added methods:

```
public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIPageControl.UIPageControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Added methods:

```
public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UIPickerView.UIPickerViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added methods:

```
public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIPopoverBackgroundView.UIPopoverBackgroundViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Added methods:

```
public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIProgressView.UIProgressViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added methods:

```
public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIRefreshControl.UIRefreshControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIResponder

Added property:

```
public virtual UIAccessibilityCustomAction[] AccessibilityCustomActions { get; set; }
```

Added methods:

```
public virtual void AccessibilityElementDidBecomeFocused ();
	public virtual void AccessibilityElementDidLoseFocus ();
	public virtual bool AccessibilityElementIsFocused ();
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Added methods:

```
public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIScrollView.UIScrollViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added methods:

```
public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISearchBar.UISearchBarAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added methods:

```
public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISegmentedControl.UISegmentedControlAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UISlider

Added methods:

```
public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UISlider.UISliderAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIStepper

Added methods:

```
public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIStepper.UIStepperAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UISwitch

Added methods:

```
public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits);
	public static UISwitch.UISwitchAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITabBar

Added methods:

```
public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITabBar.UITabBarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITabBarItem

Added methods:

```
public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITabBarItem.UITabBarItemAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableView

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

Added methods:

```
public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits);
	public static UITableViewCell.UITableViewCellAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UITableViewController

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

Added methods:

```
public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public static UITextView.UITextViewAppearance GetAppearance<T> (UITraitCollection traits);
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Added methods:

```
public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIToolbar.UIToolbarAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIView

Removed properties:

```
public static int UIAccessibilityPauseAssistiveTechnologyNotification { get; }
	public static int UIAccessibilityResumeAssistiveTechnologyNotification { get; }
```

Added properties:

```
public virtual UIAccessibilityNavigationStyle AccessibilityNavigationStyle { get; set; }
	public virtual UIEdgeInsets LayoutMargins { get; set; }
	public static int PauseAssistiveTechnologyNotification { get; }
	public virtual bool PreservesSuperviewLayoutMargins { get; set; }
	public static int ResumeAssistiveTechnologyNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakScreenStatusDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString SpeakSelectionStatusDidChangeNotification { get; }
```

Added methods:

```
public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIView.UIViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
	public virtual void LayoutMarginsDidChange ();
```

### Type Changed: MonoTouch.UIKit.UIView.Notifications

Added methods:

```
public static MonoTouch.Foundation.NSObject ObserveSpeakScreenStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
	public static MonoTouch.Foundation.NSObject ObserveSpeakSelectionStatusDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

### Type Changed: MonoTouch.UIKit.UIViewControllerContextTransitioning

Added property:

```
public virtual MonoTouch.CoreGraphics.CGAffineTransform TargetTransform { get; }
```

### Type Changed: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext_Extensions

Added methods:

```
public static UIViewController GetTransitionViewController (IUIViewControllerTransitionCoordinatorContext This, UITransitionViewControllerKind kind);
	public static UIViewController GetTransitionViewControllerForKey (IUIViewControllerTransitionCoordinatorContext This, MonoTouch.Foundation.NSString key);
```

### Type Changed: MonoTouch.UIKit.UIVisualEffectView

Added methods:

```
public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIVisualEffectView.UIVisualEffectViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added methods:

```
public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits);
	public static UIWebView.UIWebViewAppearance GetAppearance<T> (UITraitCollection traits, System.Type[] containers);
```

### Type Changed: MonoTouch.UIKit.UIWindow

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

### New Type MonoTouch.UIKit.IUIPickerViewAccessibilityDelegate

```
public interface IUIPickerViewAccessibilityDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.UIKit.IUIScrollViewAccessibilityDelegate

```
public interface IUIScrollViewAccessibilityDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoTouch.UIKit.UITransitionViewControllerKind

```
[Serializable]
public enum UITransitionViewControllerKind {
	FromView = 1,
	ToView = 0,
}
```

## Namespace MonoTouch.WebKit



### Type Changed: MonoTouch.WebKit.WKWebView

Added methods:

```
public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits, System.Type[] containers);
	public static WKWebView.WKWebViewAppearance GetAppearance<T> (MonoTouch.UIKit.UITraitCollection traits);
```

### Type Changed: MonoTouch.WebKit.WKWindowFeatures

Added properties:

```
public bool? AllowsResizing { get; }
	public float? Height { get; }
	public bool? MenuBarVisibility { get; }
	public bool? StatusBarVisibility { get; }
	public bool? ToolbarsVisibility { get; }
	public float? Width { get; }
	public float? X { get; }
	public float? Y { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

## Removed Namespace monotouch

### Removed Type monotouch.HKUnit 

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
