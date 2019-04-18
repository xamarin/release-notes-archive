---
id: 7CB422A8-BAF1-482C-B17C-B345B200733E
title: "From 1.10.0 to 1.11.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Added fields:

```
public static const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
```

### Removed Type MonoMac.RuntimeException 

## Namespace MonoMac.AppKit

### Type Changed: MonoMac.AppKit.NSButton

Removed method:

```
public virtual void SetShowsBorderOnlyWhileMouseInside (bool showsBorder);
```

### Type Changed: MonoMac.AppKit.NSColor

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.AppKit.NSColorSpace

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.AppKit.NSComboBox

Removed property:

```
public NSComboBoxDelegate Delegate { get; set; }
```

Removed events:

```
public event System.EventHandler SelectionChanged;
	public event System.EventHandler SelectionIsChanging;
	public event System.EventHandler WillDismiss;
	public event System.EventHandler WillPopUp;
```

### Type Changed: MonoMac.AppKit.NSDocumentController

Removed property:

```
public static NSDocumentController SharedDocumentController { get; }
```

Added property:

```
public static MonoMac.Foundation.NSObject SharedDocumentController { get; }
```

### Type Changed: MonoMac.AppKit.NSGlyphInfo

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.AppKit.NSImage

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.AppKit.NSLayoutConstraint

Added method:

```
public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, object[] viewsAndMetrics);
```

### Type Changed: MonoMac.AppKit.NSTextStorage

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.AppKit.NSWindow

Added properties:

```
public virtual MonoMac.Foundation.NSObject ContentLayoutGuide { get; }
	public virtual System.Drawing.RectangleF ContentLayoutRect { get; }
	public virtual NSTitlebarAccessoryViewController[] TitlebarAccessoryViewControllers { get; set; }
	public virtual bool TitlebarAppearsTransparent { get; set; }
	public virtual NSWindowTitleVisibility TitleVisibility { get; set; }
```

Added methods:

```
public virtual void AddTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController);
	public static NSWindow GetWindowWithContentViewController (NSViewController contentViewController);
	public virtual void InsertTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController, int index);
	public virtual void RemoveTitlebarAccessoryViewControllerAtIndex (int index);
```

### Type Changed: MonoMac.AppKit.NSWindowController

Added property:

```
public virtual NSViewController ContentViewController { get; set; }
```

### Removed Type MonoMac.AppKit.INSComboBoxDelegate ### Removed Type MonoMac.AppKit.NSComboBoxDelegate ### Removed Type MonoMac.AppKit.NSComboBoxDelegate_Extensions ### New Type MonoMac.AppKit.NSTitlebarAccessoryViewController

```
public class NSTitlebarAccessoryViewController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTitlebarAccessoryViewController ();
	public NSTitlebarAccessoryViewController (MonoMac.Foundation.NSCoder coder);
	public NSTitlebarAccessoryViewController (MonoMac.Foundation.NSObjectFlag t);
	public NSTitlebarAccessoryViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float FullScreenMinHeight { get; set; }
	public virtual NSLayoutAttribute LayoutAttribute { get; set; }
	// methods
	public virtual void ViewDidAppear ();
	public virtual void ViewDidDisappear ();
	public virtual void ViewWillAppear ();
}
```

### New Type MonoMac.AppKit.NSWindowTitleVisibility

```
[Serializable]
public enum NSWindowTitleVisibility {
	Hidden = 1,
	HiddenWhenActive = 2,
	Visible = 0,
}
```





## Namespace MonoMac.AudioToolbox



### Type Changed: MonoMac.AudioToolbox.AudioFile

Obsoleted method:

```
[Obsolete ("Use ReadPacketData instead")]
	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, System.IntPtr buffer);
```

### Type Changed: MonoMac.AudioToolbox.AudioFormatType

Added value:

```
AMRWideBand = 1935767394,
```

### Type Changed: MonoMac.AudioToolbox.AudioQueueStatus

Added value:

```
BufferEnqueuedTwice = -66666,
```

### Type Changed: MonoMac.AudioToolbox.AudioStreamBasicDescription

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

## Namespace MonoMac.AudioUnit

### Type Changed: MonoMac.AudioUnit.AudioTypeMixer

Added value:

```
Spacial = 862217581,
```

Obsoleted field:

```
[Obsolete ("Replaced by Spacial")]
	ThreeD = 862219640,
```

### Type Changed: MonoMac.AudioUnit.AudioTypeMusicDevice

Added value:

```
MidiSynth = 1836284270,
```

### Type Changed: MonoMac.AudioUnit.AudioUnitParameterFlag

Added value:

```
OmitFromPresets = 8192,
```

### Type Changed: MonoMac.AudioUnit.AudioUnitParameterType

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

### Type Changed: MonoMac.AudioUnit.AudioUnitPropertyIDType

Added values:

```
AttenuationCurve = 3013,
	BankName = 1007,
	DistanceParams = 3010,
	InstrumentCount = 1000,
	InstrumentName = 1001,
	InstrumentNumber = 1004,
	MidiSynthEnablePreload = 4119,
	RenderingFlags = 3003,
	ReverbRoomType = 10,
	SoundBankURL = 1100,
	SpatializationAlgorithm = 3000,
	UsesInternalReverb = 1005,
```

### New Type MonoMac.AudioUnit.AudioComponentDescriptionNative

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

### New Type MonoMac.AudioUnit.ScheduledAudioSliceFlag

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

### New Type MonoMac.AudioUnit.SpatialMixerAttenuation

```
[Serializable]
public enum SpatialMixerAttenuation {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
```

### New Type MonoMac.AudioUnit.SpatialMixerRenderingFlags

```
[Serializable]
[Flags]
public enum SpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
```

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVAsset

Added property:

```
public virtual AVMetadataItem[] Metadata { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetExportSession

Added properties:

```
public virtual bool CanPerformMultiplePassesOverSourceMediaData { get; set; }
	public virtual MonoMac.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetReaderOutput

Added property:

```
public virtual bool SupportsRandomAccess { get; set; }
```

Added methods:

```
public virtual void MarkConfigurationAsFinal ();
	public virtual void ResetForReadingTimeRanges (MonoMac.Foundation.NSValue[] timeRanges);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate

Added methods:

```
public virtual void DidCancelAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public virtual bool ShouldWaitForRenewalOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public virtual bool ShouldWaitForResponseToAuthenticationChallenge (AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added methods:

```
public static void DidCancelAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public static bool ShouldWaitForRenewalOfRequestedResource (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public static bool ShouldWaitForResponseToAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, MonoMac.Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoadingContentInformationRequest

Added property:

```
public virtual MonoMac.Foundation.NSDate RenewalDate { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoadingDataRequest

Added constructor:

```
[Obsolete ("Type is not meant to be created by user code")]
	public AVAssetResourceLoadingDataRequest ();
```

Removed method:

```
public override string ToString ();
```

### Type Changed: MonoMac.AVFoundation.AVAssetTrack

Added properties:

```
public virtual AVMetadataItem[] Metadata { get; }
	public virtual bool RequiresFrameReordering { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetTrackTrackAssociation

Added property:

```
public static MonoMac.Foundation.NSString MetadataReferent { get; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriter

Added properties:

```
public virtual MonoMac.Foundation.NSString[] AvailableMediaTypes { get; }
	public virtual MonoMac.Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVAssetWriterInput

Added properties:

```
public virtual bool CanPerformMultiplePasses { get; }
	public virtual AVAssetWriterInputPassDescription CurrentPassDescription { get; }
	public virtual bool PerformsMultiPassEncodingIfSupported { get; set; }
	public virtual int PreferredMediaChunkAlignment { get; set; }
	public virtual MonoMac.CoreMedia.CMTime PreferredMediaChunkDuration { get; set; }
	public virtual MonoMac.Foundation.NSUrl SampleReferenceBaseUrl { get; set; }
```

Added methods:

```
public virtual void MarkCurrentPassAsFinished ();
	public virtual void SetPassHandler (MonoMac.CoreFoundation.DispatchQueue queue, System.Action passHandler);
```

### Type Changed: MonoMac.AVFoundation.AVAudioSessionErrorCode

Added value:

```
InsufficientPriority = 561017449,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureConnection

Added constructors:

```
public AVCaptureConnection (AVCaptureInputPort[] inputPorts, AVCaptureOutput output);
	public AVCaptureConnection (AVCaptureInputPort inputPort, AVCaptureVideoPreviewLayer layer);
```

### Type Changed: MonoMac.AVFoundation.AVCaptureDevicePosition

Added value:

```
Unspecified = 0,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureExposureMode

Added value:

```
Custom = 3,
```

### Type Changed: MonoMac.AVFoundation.AVCaptureFileOutput

Added method:

```
public void StartRecordingToOutputFile (MonoMac.Foundation.NSUrl outputFileUrl, System.Action<MonoMac.Foundation.NSObject[]> startRecordingFromConnections, System.Action<MonoMac.Foundation.NSObject[],MonoMac.Foundation.NSError> finishedRecording);
```

### Type Changed: MonoMac.AVFoundation.AVCaptureFocusMode

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

### Type Changed: MonoMac.AVFoundation.AVCaptureSession

Added property:

```
public virtual MonoMac.CoreMedia.CMClock MasterClock { get; }
```

Added methods:

```
public virtual void AddConnection (AVCaptureConnection connection);
	public virtual void AddInputWithNoConnections (AVCaptureInput input);
	public virtual void AddOutputWithNoConnections (AVCaptureOutput output);
	public virtual bool CanAddConnection (AVCaptureConnection connection);
	public virtual void RemoveConnection (AVCaptureConnection connection);
```

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoPreviewLayer

Added method:

```
public static AVCaptureVideoPreviewLayer CreateWithNoConnection (AVCaptureSession session);
```

### Type Changed: MonoMac.AVFoundation.AVError

Added values:

```
FailedToParse2 = -11853,
	FileTypeDoesNotSupportSampleReferences = -11854,
	UndecodableMediaData = -11855,
```

### Type Changed: MonoMac.AVFoundation.AVMediaSelectionGroup

Added property:

```
public virtual AVMediaSelectionOption DefaultOption { get; }
```

### Type Changed: MonoMac.AVFoundation.AVMetadata

Added properties:

```
public static MonoMac.Foundation.NSString FormatHlsMetadata { get; }
	public static MonoMac.Foundation.NSString IcyMetadataKeyStreamTitle { get; }
	public static MonoMac.Foundation.NSString IcyMetadataKeyStreamUrl { get; }
	public static MonoMac.Foundation.NSString IsoUserDataKeyTaggedCharacteristic { get; }
	public static MonoMac.Foundation.NSString KeySpaceIcy { get; }
```

### Type Changed: MonoMac.AVFoundation.AVMetadataItem

Removed properties:

```
public virtual MonoMac.CoreMedia.CMTime Duration { get; }
	public virtual MonoMac.Foundation.NSDictionary ExtraAttributes { get; }
	public virtual string KeySpace { get; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; }
	public virtual MonoMac.CoreMedia.CMTime Time { get; }
	public virtual MonoMac.Foundation.NSObject Value { get; }
```

Added properties:

```
public virtual MonoMac.Foundation.NSString DataType { get; set; }
	public virtual MonoMac.CoreMedia.CMTime Duration { get; set; }
	public virtual string ExtendedLanguageTag { get; set; }
	public virtual MonoMac.Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; set; }
	public virtual MonoMac.Foundation.NSString MetadataIdentifier { get; set; }
	public virtual MonoMac.CoreMedia.CMTime Time { get; set; }
	public virtual MonoMac.Foundation.NSObject Value { get; set; }
```

Added methods:

```
public static AVMetadataItem[] FilterWithIdentifier (AVMetadataItem[] metadataItems, MonoMac.Foundation.NSString metadataIdentifer);
	public static MonoMac.Foundation.NSObject GetKeyForIdentifier (MonoMac.Foundation.NSString identifier);
	public static MonoMac.Foundation.NSString GetKeySpaceForIdentifier (MonoMac.Foundation.NSString identifier);
	public static MonoMac.Foundation.NSString GetMetadataIdentifier (MonoMac.Foundation.NSObject key, MonoMac.Foundation.NSString keySpace);
```

### Type Changed: MonoMac.AVFoundation.AVMutableMetadataItem

Removed properties:

```
public virtual MonoMac.CoreMedia.CMTime Duration { get; set; }
	public virtual MonoMac.Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; set; }
	public virtual MonoMac.CoreMedia.CMTime Time { get; set; }
	public virtual MonoMac.Foundation.NSObject Value { get; set; }
```

Added properties:

```
public override MonoMac.Foundation.NSString DataType { get; set; }
	public override MonoMac.CoreMedia.CMTime Duration { get; set; }
	public override string ExtendedLanguageTag { get; set; }
	public override MonoMac.Foundation.NSDictionary ExtraAttributes { get; set; }
	public override string KeySpace { get; set; }
	public override MonoMac.Foundation.NSLocale Locale { get; set; }
	public override MonoMac.Foundation.NSString MetadataIdentifier { get; set; }
	public override MonoMac.CoreMedia.CMTime Time { get; set; }
	public override MonoMac.Foundation.NSObject Value { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVPlayerItem

Added property:

```
public virtual double PreferredPeakBitRate { get; set; }
```

### Type Changed: MonoMac.AVFoundation.AVTimedMetadataGroup

Added constructor:

```
public AVTimedMetadataGroup (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer);
```

Added method:

```
public virtual MonoMac.CoreMedia.CMFormatDescription CopyFormatDescription ();
```

### Type Changed: MonoMac.AVFoundation.AVUrlAsset

Removed constructor:

```
public AVUrlAsset (MonoMac.Foundation.NSUrl URL, MonoMac.Foundation.NSDictionary options);
```

Added constructor:

```
public AVUrlAsset (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
```

Removed method:

```
public static AVUrlAsset FromUrl (MonoMac.Foundation.NSUrl URL, MonoMac.Foundation.NSDictionary options);
```

Added method:

```
public static AVUrlAsset FromUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
```

### Type Changed: MonoMac.AVFoundation.AVVideoCodecSettings

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

### Type Changed: MonoMac.AVFoundation.AVVideoSettingsCompressed

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

### Type Changed: MonoMac.AVFoundation.AVVideoSettingsUncompressed

Removed property:

```
public AVVideoScalingMode? ScalingMode { set; }
```

Added property:

```
public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: MonoMac.AVFoundation.IAVPlayerItemLegibleOutputPushDelegate

Added interface:

```
IAVPlayerItemOutputPushDelegate
```

### New Type MonoMac.AVFoundation.AVAssetReaderOutputMetadataAdaptor

```
public class AVAssetReaderOutputMetadataAdaptor : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderOutputMetadataAdaptor (MonoMac.Foundation.NSCoder coder);
	public AVAssetReaderOutputMetadataAdaptor (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAssetReaderSampleReferenceOutput

```
public class AVAssetReaderSampleReferenceOutput : MonoMac.AVFoundation.AVAssetReaderOutput, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderSampleReferenceOutput (MonoMac.Foundation.NSCoder coder);
	public AVAssetReaderSampleReferenceOutput (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAssetResourceRenewalRequest

```
public class AVAssetResourceRenewalRequest : MonoMac.AVFoundation.AVAssetResourceLoadingRequest, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceRenewalRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceRenewalRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceRenewalRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAssetWriterInputMetadataAdaptor

```
public class AVAssetWriterInputMetadataAdaptor : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputMetadataAdaptor (MonoMac.Foundation.NSCoder coder);
	public AVAssetWriterInputMetadataAdaptor (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAssetWriterInputPassDescription

```
public class AVAssetWriterInputPassDescription : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputPassDescription ();
	public AVAssetWriterInputPassDescription (MonoMac.Foundation.NSCoder coder);
	public AVAssetWriterInputPassDescription (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetWriterInputPassDescription (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSValue[] SourceTimeRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAudio3DAngularOrientation

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

### New Type MonoMac.AVFoundation.AVAudio3DMixing

```
public abstract class AVAudio3DMixing : MonoMac.Foundation.NSObject, IAVAudio3DMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudio3DMixing ();
	public AVAudio3DMixing (MonoMac.Foundation.NSCoder coder);
	public AVAudio3DMixing (MonoMac.Foundation.NSObjectFlag t);
	public AVAudio3DMixing (System.IntPtr handle);
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudio3DMixing_Extensions

```
public static class AVAudio3DMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudio3DMixingRenderingAlgorithm

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

### New Type MonoMac.AVFoundation.AVAudio3DVectorOrientation

```
public struct AVAudio3DVectorOrientation {
	// constructors
	public AVAudio3DVectorOrientation (MonoMac.OpenGL.Vector3 forward, MonoMac.OpenGL.Vector3 up);
	// fields
	public MonoMac.OpenGL.Vector3 Forward;
	public MonoMac.OpenGL.Vector3 Up;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DVectorOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public static bool op_Inequality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public override string ToString ();
}
```

### New Type MonoMac.AVFoundation.AVAudioBuffer

```
public class AVAudioBuffer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioBuffer (MonoMac.Foundation.NSCoder coder);
	public AVAudioBuffer (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioBuffer (System.IntPtr handle);
	// properties
	public MonoMac.AudioToolbox.AudioBuffers AudioBufferList { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat Format { get; }
	public MonoMac.AudioToolbox.AudioBuffers MutableAudioBufferList { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.AVFoundation.AVAudioChannelLayout

```
public class AVAudioChannelLayout : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioChannelLayout ();
	public AVAudioChannelLayout (MonoMac.Foundation.NSCoder coder);
	public AVAudioChannelLayout (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioChannelLayout (System.IntPtr handle);
	public AVAudioChannelLayout (uint layoutTag);
	public AVAudioChannelLayout (MonoMac.AudioToolbox.AudioChannelLayout layout);
	// properties
	public virtual uint ChannelCount { get; }
	public override System.IntPtr ClassHandle { get; }
	public MonoMac.AudioToolbox.AudioChannelLayout Layout { get; }
	public virtual uint LayoutTag { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioChannelLayout a, AVAudioChannelLayout b);
	public static bool op_Inequality (AVAudioChannelLayout a, AVAudioChannelLayout b);
}
```

### New Type MonoMac.AVFoundation.AVAudioCommonFormat

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

### New Type MonoMac.AVFoundation.AVAudioEngine

```
public class AVAudioEngine : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEngine ();
	public AVAudioEngine (MonoMac.Foundation.NSCoder coder);
	public AVAudioEngine (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEngine (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual AVAudioInputNode InputNode { get; }
	public virtual AVAudioMixerNode MainMixerNode { get; }
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
	public virtual bool StartAndReturnError (out MonoMac.Foundation.NSError outError);
	public virtual void Stop ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoMac.Foundation.NSObject ObserveConfigurationChange (System.EventHandler<MonoMac.Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentDistanceAttenuationModel

```
[Serializable]
public enum AVAudioEnvironmentDistanceAttenuationModel {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentDistanceAttenuationParameters

```
public class AVAudioEnvironmentDistanceAttenuationParameters : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentDistanceAttenuationParameters (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentDistanceAttenuationParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationModel DistanceAttenuationModel { get; set; }
	public virtual float MaximumDistance { get; set; }
	public virtual float ReferenceDistance { get; set; }
	public virtual float RolloffFactor { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentNode

```
public class AVAudioEnvironmentNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentNode ();
	public AVAudioEnvironmentNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioEnvironmentNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationParameters DistanceAttenuationParameters { get; }
	public virtual AVAudio3DAngularOrientation ListenerAngularOrientation { get; set; }
	public virtual MonoMac.OpenGL.Vector3 ListenerPosition { get; set; }
	public virtual AVAudio3DVectorOrientation ListenerVectorOrientation { get; set; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual AVAudioEnvironmentReverbParameters ReverbParameters { get; }
	public virtual float Volume { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject[] ApplicableRenderingAlgorithms ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVAudioEnvironmentReverbParameters

```
public class AVAudioEnvironmentReverbParameters : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentReverbParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioEnvironmentReverbParameters (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAudioFile

```
public class AVAudioFile : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFile ();
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AudioSettings settings, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AVAudioCommonFormat format, bool interleaved, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, out MonoMac.Foundation.NSError outError);
	public AVAudioFile (System.IntPtr handle);
	public AVAudioFile (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioFile (MonoMac.Foundation.NSCoder coder);
	public AVAudioFile (MonoMac.Foundation.NSUrl fileUrl, AudioSettings settings, AVAudioCommonFormat format, bool interleaved, out MonoMac.Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat FileFormat { get; }
	public virtual long FramePosition { get; set; }
	public virtual long Length { get; }
	public virtual AVAudioFormat ProcessingFormat { get; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, out MonoMac.Foundation.NSError outError);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, uint frames, out MonoMac.Foundation.NSError outError);
	public virtual bool WriteFromBuffer (AVAudioPcmBuffer buffer, out MonoMac.Foundation.NSError outError);
}
```

### New Type MonoMac.AVFoundation.AVAudioFormat

```
public class AVAudioFormat : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFormat ();
	public AVAudioFormat (MonoMac.Foundation.NSDictionary settings);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, bool interleaved, AVAudioChannelLayout layout);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, uint channels, bool interleaved);
	public AVAudioFormat (double sampleRate, AVAudioChannelLayout layout);
	public AVAudioFormat (double sampleRate, uint channels);
	public AVAudioFormat (ref MonoMac.AudioToolbox.AudioStreamBasicDescription description, AVAudioChannelLayout layout);
	public AVAudioFormat (ref MonoMac.AudioToolbox.AudioStreamBasicDescription description);
	public AVAudioFormat (System.IntPtr handle);
	public AVAudioFormat (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioFormat (MonoMac.Foundation.NSCoder coder);
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
	public virtual MonoMac.AudioToolbox.AudioStreamBasicDescription StreamDescription { get; }
	public virtual MonoMac.Foundation.NSDictionary WeakSettings { get; }
	// methods
	protected override void Dispose (bool disposing);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioFormat a, AVAudioFormat b);
	public static bool op_Inequality (AVAudioFormat a, AVAudioFormat b);
}
```

### New Type MonoMac.AVFoundation.AVAudioInputNode

```
public class AVAudioInputNode : MonoMac.AVFoundation.AVAudioIONode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioInputNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioInputNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioInputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioIONode

```
public class AVAudioIONode : MonoMac.AVFoundation.AVAudioNode, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioIONode (MonoMac.Foundation.NSCoder coder);
	public AVAudioIONode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioIONode (System.IntPtr handle);
	// properties
	public virtual MonoMac.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual double PresentationLatency { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioMixerNode

```
public class AVAudioMixerNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioMixerNode ();
	public AVAudioMixerNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioMixerNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioMixerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioMixing_Extensions

```
public static class AVAudioMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudioNode

```
public class AVAudioNode : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioNode (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAudioNodeTapBlock

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

### New Type MonoMac.AVFoundation.AVAudioOutputNode

```
public class AVAudioOutputNode : MonoMac.AVFoundation.AVAudioIONode, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioOutputNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioOutputNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioOutputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioPcmBuffer

```
public class AVAudioPcmBuffer : MonoMac.AVFoundation.AVAudioBuffer, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPcmBuffer (MonoMac.Foundation.NSCoder coder);
	public AVAudioPcmBuffer (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAudioPlayerNode

```
public class AVAudioPlayerNode : MonoMac.AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPlayerNode ();
	public AVAudioPlayerNode (MonoMac.Foundation.NSCoder coder);
	public AVAudioPlayerNode (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioPlayerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual bool Playing { get; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
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

### New Type MonoMac.AVFoundation.AVAudioPlayerNodeBufferOptions

```
[Serializable]
[Flags]
public enum AVAudioPlayerNodeBufferOptions {
	Interrupts = 2,
	InterruptsAtLoop = 4,
	Loops = 1,
}
```

### New Type MonoMac.AVFoundation.AVAudioSessionRecordPermission

```
[Serializable]
public enum AVAudioSessionRecordPermission {
	Denied = 1684369017,
	Granted = 1735552628,
	Undetermined = 1970168948,
}
```

### New Type MonoMac.AVFoundation.AVAudioSessionSilenceSecondaryAudioHintType

```
[Serializable]
public enum AVAudioSessionSilenceSecondaryAudioHintType {
	Begin = 1,
	End = 0,
}
```

### New Type MonoMac.AVFoundation.AVAudioStereoMixing

```
public abstract class AVAudioStereoMixing : MonoMac.Foundation.NSObject, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioStereoMixing ();
	public AVAudioStereoMixing (MonoMac.Foundation.NSCoder coder);
	public AVAudioStereoMixing (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioStereoMixing (System.IntPtr handle);
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioStereoMixing_Extensions

```
public static class AVAudioStereoMixing_Extensions {
}
```

### New Type MonoMac.AVFoundation.AVAudioTime

```
public class AVAudioTime : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioTime ();
	public AVAudioTime (long sampleTime, double sampleRate);
	public AVAudioTime (ulong hostTime);
	public AVAudioTime (ref MonoMac.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public AVAudioTime (System.IntPtr handle);
	public AVAudioTime (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioTime (MonoMac.Foundation.NSCoder coder);
	public AVAudioTime (ulong hostTime, long sampleTime, double sampleRate);
	// properties
	public virtual MonoMac.AudioToolbox.AudioTimeStamp AudioTimeStamp { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual ulong HostTime { get; }
	public virtual bool HostTimeValid { get; }
	public virtual double SampleRate { get; }
	public virtual long SampleTime { get; }
	public virtual bool SampleTimeValid { get; }
	// methods
	public virtual AVAudioTime ExtrapolateTimeFromAnchor (AVAudioTime anchorTime);
	public static AVAudioTime FromAudioTimeStamp (ref MonoMac.AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public static AVAudioTime FromHostTime (ulong hostTime);
	public static AVAudioTime FromHostTime (ulong hostTime, long sampleTime, double sampleRate);
	public static AVAudioTime FromSampleTime (long sampleTime, double sampleRate);
	public static ulong HostTimeForSeconds (double seconds);
	public static double SecondsForHostTime (ulong hostTime);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnit

```
public class AVAudioUnit : MonoMac.AVFoundation.AVAudioNode, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnit (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnit (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnit (System.IntPtr handle);
	// properties
	public virtual MonoMac.AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual uint Version { get; }
	// methods
	public virtual bool LoadAudioUnitPreset (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDelay

```
public class AVAudioUnitDelay : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDelay ();
	public AVAudioUnitDelay (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitDelay (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitDelay (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DelayTime { get; set; }
	public virtual float Feedback { get; set; }
	public virtual float LowPassCutoff { get; set; }
	public virtual float WetDryMix { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDistortion

```
public class AVAudioUnitDistortion : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDistortion ();
	public AVAudioUnitDistortion (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitDistortion (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitDistortion (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PreGain { get; set; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitDistortionPreset preset);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitDistortionPreset

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

### New Type MonoMac.AVFoundation.AVAudioUnitEffect

```
public class AVAudioUnitEffect : MonoMac.AVFoundation.AVAudioUnit, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEffect (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEffect (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitEffect (System.IntPtr handle);
	public AVAudioUnitEffect (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitEQ

```
public class AVAudioUnitEQ : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQ ();
	public AVAudioUnitEQ (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEQ (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAudioUnitEQFilterParameters

```
public class AVAudioUnitEQFilterParameters : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQFilterParameters (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitEQFilterParameters (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.AVFoundation.AVAudioUnitEQFilterType

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

### New Type MonoMac.AVFoundation.AVAudioUnitGenerator

```
public class AVAudioUnitGenerator : MonoMac.AVFoundation.AVAudioUnit, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitGenerator (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitGenerator (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitGenerator (System.IntPtr handle);
	public AVAudioUnitGenerator (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitMidiInstrument

```
public class AVAudioUnitMidiInstrument : MonoMac.AVFoundation.AVAudioUnit, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitMidiInstrument (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitMidiInstrument (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitMidiInstrument (System.IntPtr handle);
	public AVAudioUnitMidiInstrument (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void SendController (byte controller, byte value, byte channel);
	public virtual void SendMidiEvent (byte midiStatus, byte data1, byte data2);
	public virtual void SendMidiEvent (byte midiStatus, byte data1);
	public virtual void SendMidiSysExEvent (MonoMac.Foundation.NSData midiData);
	public virtual void SendPitchBend (ushort pitchbend, byte channel);
	public virtual void SendPressure (byte pressure, byte channel);
	public virtual void SendPressureForKey (byte key, byte value, byte channel);
	public virtual void SendProgramChange (byte program, byte channel);
	public virtual void SendProgramChange (byte program, byte bankMSB, byte bankLSB, byte channel);
	public virtual void StartNote (byte note, byte velocity, byte channel);
	public virtual void StopNote (byte note, byte channel);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitReverb

```
public class AVAudioUnitReverb : MonoMac.AVFoundation.AVAudioUnitEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitReverb ();
	public AVAudioUnitReverb (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitReverb (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitReverb (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitReverbPreset

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

### New Type MonoMac.AVFoundation.AVAudioUnitSampler

```
public class AVAudioUnitSampler : MonoMac.AVFoundation.AVAudioUnitMidiInstrument, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitSampler ();
	public AVAudioUnitSampler (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitSampler (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitSampler (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalTuning { get; set; }
	public virtual float MasterGain { get; set; }
	public virtual float StereoPan { get; set; }
	// methods
	public virtual bool LoadAudioFiles (MonoMac.Foundation.NSUrl[] audioFiles, out MonoMac.Foundation.NSError outError);
	public virtual bool LoadInstrument (MonoMac.Foundation.NSUrl instrumentUrl, out MonoMac.Foundation.NSError outError);
	public virtual bool LoadSoundBank (MonoMac.Foundation.NSUrl bankUrl, byte program, byte bankMSB, byte bankLSB, out MonoMac.Foundation.NSError outError);
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitTimeEffect

```
public class AVAudioUnitTimeEffect : MonoMac.AVFoundation.AVAudioUnit, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimeEffect (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitTimeEffect (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitTimeEffect (System.IntPtr handle);
	public AVAudioUnitTimeEffect (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitTimePitch

```
public class AVAudioUnitTimePitch : MonoMac.AVFoundation.AVAudioUnitTimeEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimePitch ();
	public AVAudioUnitTimePitch (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitTimePitch (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitTimePitch (System.IntPtr handle);
	public AVAudioUnitTimePitch (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Overlap { get; set; }
	public virtual float Pitch { get; set; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAudioUnitVarispeed

```
public class AVAudioUnitVarispeed : MonoMac.AVFoundation.AVAudioUnitTimeEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitVarispeed ();
	public AVAudioUnitVarispeed (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitVarispeed (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitVarispeed (System.IntPtr handle);
	public AVAudioUnitVarispeed (MonoMac.AudioUnit.AudioComponentDescription desc);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rate { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVCaptureBracketedStillImageSettings

```
public class AVCaptureBracketedStillImageSettings : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureBracketedStillImageSettings (MonoMac.Foundation.NSCoder coder);
	public AVCaptureBracketedStillImageSettings (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureBracketedStillImageSettings (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.AVFoundation.AVCaptureDeviceFormat

```
public class AVCaptureDeviceFormat : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureDeviceFormat (MonoMac.Foundation.NSCoder coder);
	public AVCaptureDeviceFormat (MonoMac.Foundation.NSObjectFlag t);
	public AVCaptureDeviceFormat (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMFormatDescription FormatDescription { get; }
	public virtual MonoMac.Foundation.NSString MediaType { get; }
	public virtual AVFrameRateRange[] VideoSupportedFrameRateRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceChromaticityValues

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

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceGains

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

### New Type MonoMac.AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues

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

### New Type MonoMac.AVFoundation.AVMetadataIdentifiers

```
public static class AVMetadataIdentifiers {

	// inner types
	public static class CommonIdentifier {
		// properties
		public static MonoMac.Foundation.NSString AlbumName { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString Artwork { get; }
		public static MonoMac.Foundation.NSString AssetIdentifier { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString Contributor { get; }
		public static MonoMac.Foundation.NSString Copyrights { get; }
		public static MonoMac.Foundation.NSString CreationDate { get; }
		public static MonoMac.Foundation.NSString Creator { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString Format { get; }
		public static MonoMac.Foundation.NSString Language { get; }
		public static MonoMac.Foundation.NSString LastModifiedDate { get; }
		public static MonoMac.Foundation.NSString Location { get; }
		public static MonoMac.Foundation.NSString Make { get; }
		public static MonoMac.Foundation.NSString Model { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString Relation { get; }
		public static MonoMac.Foundation.NSString Software { get; }
		public static MonoMac.Foundation.NSString Source { get; }
		public static MonoMac.Foundation.NSString Subject { get; }
		public static MonoMac.Foundation.NSString Title { get; }
		public static MonoMac.Foundation.NSString Type { get; }
	}
	public static class QuickTime {
		// properties
		public static MonoMac.Foundation.NSString UserDataAlbum { get; }
		public static MonoMac.Foundation.NSString UserDataArranger { get; }
		public static MonoMac.Foundation.NSString UserDataArtist { get; }
		public static MonoMac.Foundation.NSString UserDataAuthor { get; }
		public static MonoMac.Foundation.NSString UserDataChapter { get; }
		public static MonoMac.Foundation.NSString UserDataComment { get; }
		public static MonoMac.Foundation.NSString UserDataComposer { get; }
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataCreationDate { get; }
		public static MonoMac.Foundation.NSString UserDataCredits { get; }
		public static MonoMac.Foundation.NSString UserDataDescription { get; }
		public static MonoMac.Foundation.NSString UserDataDirector { get; }
		public static MonoMac.Foundation.NSString UserDataDisclaimer { get; }
		public static MonoMac.Foundation.NSString UserDataEncodedBy { get; }
		public static MonoMac.Foundation.NSString UserDataFullName { get; }
		public static MonoMac.Foundation.NSString UserDataGenre { get; }
		public static MonoMac.Foundation.NSString UserDataHostComputer { get; }
		public static MonoMac.Foundation.NSString UserDataInformation { get; }
		public static MonoMac.Foundation.NSString UserDataKeywords { get; }
		public static MonoMac.Foundation.NSString UserDataLocationISO6709 { get; }
		public static MonoMac.Foundation.NSString UserDataMake { get; }
		public static MonoMac.Foundation.NSString UserDataModel { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalArtist { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalFormat { get; }
		public static MonoMac.Foundation.NSString UserDataOriginalSource { get; }
		public static MonoMac.Foundation.NSString UserDataPerformers { get; }
		public static MonoMac.Foundation.NSString UserDataPhonogramRights { get; }
		public static MonoMac.Foundation.NSString UserDataProducer { get; }
		public static MonoMac.Foundation.NSString UserDataProduct { get; }
		public static MonoMac.Foundation.NSString UserDataPublisher { get; }
		public static MonoMac.Foundation.NSString UserDataSoftware { get; }
		public static MonoMac.Foundation.NSString UserDataSpecialPlaybackRequirements { get; }
		public static MonoMac.Foundation.NSString UserDataTaggedCharacteristic { get; }
		public static MonoMac.Foundation.NSString UserDataTrack { get; }
		public static MonoMac.Foundation.NSString UserDataTrackName { get; }
		public static MonoMac.Foundation.NSString UserDataUrlLink { get; }
		public static MonoMac.Foundation.NSString UserDataWarning { get; }
		public static MonoMac.Foundation.NSString UserDataWriter { get; }
	}
	public static class Iso {
		// properties
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataTaggedCharacteristic { get; }
	}
	public static class ThreeGP {
		// properties
		public static MonoMac.Foundation.NSString UserDataAlbumAndTrack { get; }
		public static MonoMac.Foundation.NSString UserDataAuthor { get; }
		public static MonoMac.Foundation.NSString UserDataCollection { get; }
		public static MonoMac.Foundation.NSString UserDataCopyright { get; }
		public static MonoMac.Foundation.NSString UserDataDescription { get; }
		public static MonoMac.Foundation.NSString UserDataGenre { get; }
		public static MonoMac.Foundation.NSString UserDataKeywordList { get; }
		public static MonoMac.Foundation.NSString UserDataLocation { get; }
		public static MonoMac.Foundation.NSString UserDataMediaClassification { get; }
		public static MonoMac.Foundation.NSString UserDataMediaRating { get; }
		public static MonoMac.Foundation.NSString UserDataPerformer { get; }
		public static MonoMac.Foundation.NSString UserDataRecordingYear { get; }
		public static MonoMac.Foundation.NSString UserDataThumbnail { get; }
		public static MonoMac.Foundation.NSString UserDataTitle { get; }
		public static MonoMac.Foundation.NSString UserDataUserRating { get; }
	}
	public static class QuickTimeMetadata {
		// properties
		public static MonoMac.Foundation.NSString Album { get; }
		public static MonoMac.Foundation.NSString Arranger { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString Artwork { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString CameraFrameReadoutTime { get; }
		public static MonoMac.Foundation.NSString CameraIdentifier { get; }
		public static MonoMac.Foundation.NSString CollectionUser { get; }
		public static MonoMac.Foundation.NSString Comment { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CreationDate { get; }
		public static MonoMac.Foundation.NSString Credits { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString DirectionFacing { get; }
		public static MonoMac.Foundation.NSString DirectionMotion { get; }
		public static MonoMac.Foundation.NSString Director { get; }
		public static MonoMac.Foundation.NSString DisplayName { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString Genre { get; }
		public static MonoMac.Foundation.NSString Information { get; }
		public static MonoMac.Foundation.NSString iXML { get; }
		public static MonoMac.Foundation.NSString Keywords { get; }
		public static MonoMac.Foundation.NSString LocationBody { get; }
		public static MonoMac.Foundation.NSString LocationDate { get; }
		public static MonoMac.Foundation.NSString LocationISO6709 { get; }
		public static MonoMac.Foundation.NSString LocationName { get; }
		public static MonoMac.Foundation.NSString LocationNote { get; }
		public static MonoMac.Foundation.NSString LocationRole { get; }
		public static MonoMac.Foundation.NSString Make { get; }
		public static MonoMac.Foundation.NSString Model { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString Performer { get; }
		public static MonoMac.Foundation.NSString PhonogramRights { get; }
		public static MonoMac.Foundation.NSString PreferredAffineTransform { get; }
		public static MonoMac.Foundation.NSString Producer { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RatingUser { get; }
		public static MonoMac.Foundation.NSString Software { get; }
		public static MonoMac.Foundation.NSString Title { get; }
		public static MonoMac.Foundation.NSString Year { get; }
	}
	public static class iTunesMetadata {
		// properties
		public static MonoMac.Foundation.NSString AccountKind { get; }
		public static MonoMac.Foundation.NSString Acknowledgement { get; }
		public static MonoMac.Foundation.NSString Album { get; }
		public static MonoMac.Foundation.NSString AlbumArtist { get; }
		public static MonoMac.Foundation.NSString AppleID { get; }
		public static MonoMac.Foundation.NSString Arranger { get; }
		public static MonoMac.Foundation.NSString ArtDirector { get; }
		public static MonoMac.Foundation.NSString Artist { get; }
		public static MonoMac.Foundation.NSString ArtistID { get; }
		public static MonoMac.Foundation.NSString Author { get; }
		public static MonoMac.Foundation.NSString BeatsPerMin { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Conductor { get; }
		public static MonoMac.Foundation.NSString ContentRating { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CoverArt { get; }
		public static MonoMac.Foundation.NSString Credits { get; }
		public static MonoMac.Foundation.NSString Description { get; }
		public static MonoMac.Foundation.NSString Director { get; }
		public static MonoMac.Foundation.NSString DiscCompilation { get; }
		public static MonoMac.Foundation.NSString DiscNumber { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString EncodingTool { get; }
		public static MonoMac.Foundation.NSString EQ { get; }
		public static MonoMac.Foundation.NSString ExecProducer { get; }
		public static MonoMac.Foundation.NSString GenreID { get; }
		public static MonoMac.Foundation.NSString Grouping { get; }
		public static MonoMac.Foundation.NSString LinerNotes { get; }
		public static MonoMac.Foundation.NSString Lyrics { get; }
		public static MonoMac.Foundation.NSString OnlineExtras { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString Performer { get; }
		public static MonoMac.Foundation.NSString PhonogramRights { get; }
		public static MonoMac.Foundation.NSString PlaylistID { get; }
		public static MonoMac.Foundation.NSString PredefinedGenre { get; }
		public static MonoMac.Foundation.NSString Producer { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RecordCompany { get; }
		public static MonoMac.Foundation.NSString ReleaseDate { get; }
		public static MonoMac.Foundation.NSString Soloist { get; }
		public static MonoMac.Foundation.NSString SongID { get; }
		public static MonoMac.Foundation.NSString SongName { get; }
		public static MonoMac.Foundation.NSString SoundEngineer { get; }
		public static MonoMac.Foundation.NSString Thanks { get; }
		public static MonoMac.Foundation.NSString TrackNumber { get; }
		public static MonoMac.Foundation.NSString TrackSubTitle { get; }
		public static MonoMac.Foundation.NSString UserComment { get; }
		public static MonoMac.Foundation.NSString UserGenre { get; }
	}
	public static class ID3Metadata {
		// properties
		public static MonoMac.Foundation.NSString AlbumSortOrder { get; }
		public static MonoMac.Foundation.NSString AlbumTitle { get; }
		public static MonoMac.Foundation.NSString AttachedPicture { get; }
		public static MonoMac.Foundation.NSString AudioEncryption { get; }
		public static MonoMac.Foundation.NSString AudioSeekPointIndex { get; }
		public static MonoMac.Foundation.NSString Band { get; }
		public static MonoMac.Foundation.NSString BeatsPerMinute { get; }
		public static MonoMac.Foundation.NSString Comments { get; }
		public static MonoMac.Foundation.NSString CommercialInformation { get; }
		public static MonoMac.Foundation.NSString Commerical { get; }
		public static MonoMac.Foundation.NSString Composer { get; }
		public static MonoMac.Foundation.NSString Conductor { get; }
		public static MonoMac.Foundation.NSString ContentGroupDescription { get; }
		public static MonoMac.Foundation.NSString ContentType { get; }
		public static MonoMac.Foundation.NSString Copyright { get; }
		public static MonoMac.Foundation.NSString CopyrightInformation { get; }
		public static MonoMac.Foundation.NSString Date { get; }
		public static MonoMac.Foundation.NSString EncodedBy { get; }
		public static MonoMac.Foundation.NSString EncodedWith { get; }
		public static MonoMac.Foundation.NSString EncodingTime { get; }
		public static MonoMac.Foundation.NSString Encryption { get; }
		public static MonoMac.Foundation.NSString Equalization { get; }
		public static MonoMac.Foundation.NSString Equalization2 { get; }
		public static MonoMac.Foundation.NSString EventTimingCodes { get; }
		public static MonoMac.Foundation.NSString FileOwner { get; }
		public static MonoMac.Foundation.NSString FileType { get; }
		public static MonoMac.Foundation.NSString GeneralEncapsulatedObject { get; }
		public static MonoMac.Foundation.NSString GroupIdentifier { get; }
		public static MonoMac.Foundation.NSString InitialKey { get; }
		public static MonoMac.Foundation.NSString InternationalStandardRecordingCode { get; }
		public static MonoMac.Foundation.NSString InternetRadioStationName { get; }
		public static MonoMac.Foundation.NSString InternetRadioStationOwner { get; }
		public static MonoMac.Foundation.NSString InvolvedPeopleList_v23 { get; }
		public static MonoMac.Foundation.NSString InvolvedPeopleList_v24 { get; }
		public static MonoMac.Foundation.NSString Language { get; }
		public static MonoMac.Foundation.NSString LeadPerformer { get; }
		public static MonoMac.Foundation.NSString Length { get; }
		public static MonoMac.Foundation.NSString Link { get; }
		public static MonoMac.Foundation.NSString Lyricist { get; }
		public static MonoMac.Foundation.NSString MediaType { get; }
		public static MonoMac.Foundation.NSString ModifiedBy { get; }
		public static MonoMac.Foundation.NSString Mood { get; }
		public static MonoMac.Foundation.NSString MpegLocationLookupTable { get; }
		public static MonoMac.Foundation.NSString MusicCDIdentifier { get; }
		public static MonoMac.Foundation.NSString MusicianCreditsList { get; }
		public static MonoMac.Foundation.NSString OfficialArtistWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialAudioFileWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialAudioSourceWebpage { get; }
		public static MonoMac.Foundation.NSString OfficialInternetRadioStationHomepage { get; }
		public static MonoMac.Foundation.NSString OfficialPublisherWebpage { get; }
		public static MonoMac.Foundation.NSString OriginalAlbumTitle { get; }
		public static MonoMac.Foundation.NSString OriginalArtist { get; }
		public static MonoMac.Foundation.NSString OriginalFilename { get; }
		public static MonoMac.Foundation.NSString OriginalLyricist { get; }
		public static MonoMac.Foundation.NSString OriginalReleaseTime { get; }
		public static MonoMac.Foundation.NSString OriginalReleaseYear { get; }
		public static MonoMac.Foundation.NSString Ownership { get; }
		public static MonoMac.Foundation.NSString PartOfASet { get; }
		public static MonoMac.Foundation.NSString Payment { get; }
		public static MonoMac.Foundation.NSString PerformerSortOrder { get; }
		public static MonoMac.Foundation.NSString PlayCounter { get; }
		public static MonoMac.Foundation.NSString PlaylistDelay { get; }
		public static MonoMac.Foundation.NSString Popularimeter { get; }
		public static MonoMac.Foundation.NSString PositionSynchronization { get; }
		public static MonoMac.Foundation.NSString Private { get; }
		public static MonoMac.Foundation.NSString ProducedNotice { get; }
		public static MonoMac.Foundation.NSString Publisher { get; }
		public static MonoMac.Foundation.NSString RecommendedBufferSize { get; }
		public static MonoMac.Foundation.NSString RecordingDates { get; }
		public static MonoMac.Foundation.NSString RecordingTime { get; }
		public static MonoMac.Foundation.NSString RelativeVolumeAdjustment { get; }
		public static MonoMac.Foundation.NSString RelativeVolumeAdjustment2 { get; }
		public static MonoMac.Foundation.NSString ReleaseTime { get; }
		public static MonoMac.Foundation.NSString Reverb { get; }
		public static MonoMac.Foundation.NSString Seek { get; }
		public static MonoMac.Foundation.NSString SetSubtitle { get; }
		public static MonoMac.Foundation.NSString Signature { get; }
		public static MonoMac.Foundation.NSString Size { get; }
		public static MonoMac.Foundation.NSString SubTitle { get; }
		public static MonoMac.Foundation.NSString SynchronizedLyric { get; }
		public static MonoMac.Foundation.NSString SynchronizedTempoCodes { get; }
		public static MonoMac.Foundation.NSString TaggingTime { get; }
		public static MonoMac.Foundation.NSString TermsOfUse { get; }
		public static MonoMac.Foundation.NSString Time { get; }
		public static MonoMac.Foundation.NSString TitleDescription { get; }
		public static MonoMac.Foundation.NSString TitleSortOrder { get; }
		public static MonoMac.Foundation.NSString TrackNumber { get; }
		public static MonoMac.Foundation.NSString UniqueFileIdentifier { get; }
		public static MonoMac.Foundation.NSString UnsynchronizedLyric { get; }
		public static MonoMac.Foundation.NSString UserText { get; }
		public static MonoMac.Foundation.NSString UserUrl { get; }
		public static MonoMac.Foundation.NSString Year { get; }
	}
	public static class IcyMetadata {
		// properties
		public static MonoMac.Foundation.NSString StreamTitle { get; }
		public static MonoMac.Foundation.NSString StreamUrl { get; }
	}
}
```

### New Type MonoMac.AVFoundation.AVMidiPlayer

```
public class AVMidiPlayer : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMidiPlayer ();
	public AVMidiPlayer (MonoMac.Foundation.NSCoder coder);
	public AVMidiPlayer (MonoMac.Foundation.NSObjectFlag t);
	public AVMidiPlayer (System.IntPtr handle);
	public AVMidiPlayer (MonoMac.Foundation.NSUrl contentsUrl, MonoMac.Foundation.NSUrl soundBankUrl, out MonoMac.Foundation.NSError outError);
	public AVMidiPlayer (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSUrl sounddBankUrl, out MonoMac.Foundation.NSError outError);
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

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutput

```
public class AVPlayerItemMetadataOutput : MonoMac.AVFoundation.AVPlayerItemOutput, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutput ();
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutput (System.IntPtr handle);
	public AVPlayerItemMetadataOutput (MonoMac.Foundation.NSString[] metadataIdentifiers);
	// properties
	public virtual double AdvanceIntervalForDelegateInvocation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public AVPlayerItemMetadataOutputPushDelegate Delegate { get; }
	public virtual MonoMac.CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemMetadataOutputPushDelegate pushDelegate, MonoMac.CoreFoundation.DispatchQueue delegateQueue);
}
```

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutputPushDelegate

```
public class AVPlayerItemMetadataOutputPushDelegate : MonoMac.Foundation.NSObject, IAVPlayerItemMetadataOutputPushDelegate, IAVPlayerItemOutputPushDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutputPushDelegate ();
	public AVPlayerItemMetadataOutputPushDelegate (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemMetadataOutputPushDelegate (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void DidOutputTimedMetadataGroups (AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
```

### New Type MonoMac.AVFoundation.AVPlayerItemMetadataOutputPushDelegate_Extensions

```
public static class AVPlayerItemMetadataOutputPushDelegate_Extensions {
	// methods
	public static void DidOutputTimedMetadataGroups (IAVPlayerItemMetadataOutputPushDelegate This, AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
}
```

### New Type MonoMac.AVFoundation.AVQueuedSampleBufferRenderingStatus

```
[Serializable]
public enum AVQueuedSampleBufferRenderingStatus {
	Failed = 2,
	Rendering = 1,
	Unknown = 0,
}
```

### New Type MonoMac.AVFoundation.AVSampleBufferDisplayLayer

```
public class AVSampleBufferDisplayLayer : MonoMac.CoreAnimation.CALayer, MonoMac.CoreAnimation.ICAMediaTiming, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVSampleBufferDisplayLayer ();
	public AVSampleBufferDisplayLayer (MonoMac.Foundation.NSCoder coder);
	public AVSampleBufferDisplayLayer (MonoMac.Foundation.NSObjectFlag t);
	public AVSampleBufferDisplayLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMTimebase ControlTimebase { get; set; }
	public virtual MonoMac.Foundation.NSError Error { get; }
	public virtual bool ReadyForMoreMediaData { get; }
	public virtual AVQueuedSampleBufferRenderingStatus Status { get; }
	public virtual string VideoGravity { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnqueueSampleBuffer (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer);
	public virtual void Flush ();
	public virtual void FlushAndRemoveImage ();
	public virtual void RequestMediaDataWhenReadyOnQueue (MonoMac.CoreFoundation.DispatchQueue queue, System.Action enqueuer);
	public virtual void StopRequestingMediaData ();
}
```

### New Type MonoMac.AVFoundation.AVUtilities

```
public static class AVUtilities {
	// methods
	public static System.Drawing.RectangleF WithAspectRatio (System.Drawing.RectangleF self, System.Drawing.SizeF aspectRatio);
}
```

### New Type MonoMac.AVFoundation.IAVAudio3DMixing

```
public interface IAVAudio3DMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVAudioMixing

```
public interface IAVAudioMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IAVAudio3DMixing, IAVAudioStereoMixing {
	// properties
	public virtual float Volume { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVAudioStereoMixing

```
public interface IAVAudioStereoMixing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type MonoMac.AVFoundation.IAVPlayerItemMetadataOutputPushDelegate

```
public interface IAVPlayerItemMetadataOutputPushDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IAVPlayerItemOutputPushDelegate {
}
```

## Namespace MonoMac.CoreAnimation

### Type Changed: MonoMac.CoreAnimation.CAAnimation

Added properties:

```
public virtual MonoMac.SceneKit.SCNAnimationEvent[] AnimationEvents { get; set; }
	public virtual float FadeInDuration { get; set; }
	public virtual float FadeOutDuration { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation

Added properties:

```
public virtual MonoMac.Foundation.NSNumber[] BiasValues { get; set; }
	public virtual MonoMac.Foundation.NSNumber[] ContinuityValues { get; set; }
	public virtual MonoMac.Foundation.NSNumber[] TensionValues { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CALayer

Added properties:

```
public virtual MonoMac.CoreImage.CIFilter[] BackgroundFilters { get; set; }
	public virtual MonoMac.Foundation.NSObject CompositingFilter { get; set; }
	public virtual float MinificationFilterBias { get; set; }
	public virtual MonoMac.Foundation.NSDictionary Style { get; set; }
```

### Type Changed: MonoMac.CoreAnimation.CATransition

Removed property:

```
public virtual MonoMac.Foundation.NSObject filter { get; set; }
```

Added properties:

```
[Obsolete ("The name has been fixed, use Filter instead")]
	public MonoMac.Foundation.NSObject filter { get; set; }
	public virtual MonoMac.Foundation.NSObject Filter { get; set; }
```

## Namespace MonoMac.CoreBluetooth

### Type Changed: MonoMac.CoreBluetooth.CBAdvertisement

Removed properties:

```
public static MonoMac.Foundation.NSString DataOverflowServiceUUIDsKey { get; }
	public static MonoMac.Foundation.NSString DataSolicitedServiceUUIDsKey { get; }
	public static MonoMac.Foundation.NSString IsConnectable { get; }
```

### Type Changed: MonoMac.CoreBluetooth.CBCentralManager

Removed constructor:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoMac.CoreFoundation.DispatchQueue queue, MonoMac.Foundation.NSDictionary options);
```

Removed properties:

```
public static MonoMac.Foundation.NSString OptionShowPowerAlertKey { get; }
	public static MonoMac.Foundation.NSString ScanOptionSolicitedServiceUUIDsKey { get; }
```

Removed methods:

```
public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);
	public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (MonoMac.Foundation.NSUuid[] identifiers);
```

### Type Changed: MonoMac.CoreBluetooth.CBCharacteristic

Removed properties:

```
public virtual CBCentral[] SubscribedCentrals { get; }
	public virtual CBUUID UUID { get; set; }
```

Added property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: MonoMac.CoreBluetooth.CBPeripheral

Removed property:

```
[Obsolete ("Deprecated in iOS7")]
	public virtual System.IntPtr UUID { get; }
```

### Type Changed: MonoMac.CoreBluetooth.CBService

Removed property:

```
public virtual bool Primary { get; }
```

### Removed Type MonoMac.CoreBluetooth.CBATTRequest ### Removed Type MonoMac.CoreBluetooth.CBATTRequestEventArgs ### Removed Type MonoMac.CoreBluetooth.CBATTRequestsEventArgs ### Removed Type MonoMac.CoreBluetooth.CBCentral ### Removed Type MonoMac.CoreBluetooth.CBMutableCharacteristic ### Removed Type MonoMac.CoreBluetooth.CBMutableDescriptor ### Removed Type MonoMac.CoreBluetooth.CBMutableService ### Removed Type MonoMac.CoreBluetooth.CBPeripheralManager ### Removed Type MonoMac.CoreBluetooth.CBPeripheralManagerDelegate ### Removed Type MonoMac.CoreBluetooth.CBPeripheralManagerDelegate_Extensions ### Removed Type MonoMac.CoreBluetooth.CBPeripheralManagerServiceEventArgs ### Removed Type MonoMac.CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs ### Removed Type MonoMac.CoreBluetooth.ICBPeripheralManagerDelegate 



## Namespace MonoMac.CoreData



### Type Changed: MonoMac.CoreData.NSManagedObjectContext

Added property:

```
public virtual string Name { get; set; }
```

Added method:

```
public virtual NSPersistentStoreResult ExecuteRequest (NSPersistentStoreRequest request, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator

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

### Type Changed: MonoMac.CoreData.NSPersistentStoreRequestType

Added value:

```
BatchUpdate = 6,
```

### New Type MonoMac.CoreData.NSAsynchronousFetchRequest

```
public class NSAsynchronousFetchRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchRequest ();
	public NSAsynchronousFetchRequest (MonoMac.Foundation.NSCoder coder);
	public NSAsynchronousFetchRequest (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CoreData.NSAsynchronousFetchResult

```
public class NSAsynchronousFetchResult : MonoMac.CoreData.NSPersistentStoreAsynchronousResult, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchResult ();
	public NSAsynchronousFetchResult (MonoMac.Foundation.NSCoder coder);
	public NSAsynchronousFetchResult (MonoMac.Foundation.NSObjectFlag t);
	public NSAsynchronousFetchResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSAsynchronousFetchRequest FetchRequest { get; }
	public virtual MonoMac.Foundation.NSObject[] FinalResult { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSBatchUpdateRequest

```
public class NSBatchUpdateRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateRequest ();
	public NSBatchUpdateRequest (MonoMac.Foundation.NSCoder coder);
	public NSBatchUpdateRequest (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchUpdateRequest (System.IntPtr handle);
	public NSBatchUpdateRequest (string entityName);
	public NSBatchUpdateRequest (NSEntityDescription entity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSEntityDescription Entity { get; }
	public virtual string EntityName { get; }
	public virtual bool IncludesSubentities { get; set; }
	public virtual MonoMac.Foundation.NSPredicate Predicate { get; set; }
	public virtual MonoMac.Foundation.NSDictionary PropertiesToUpdate { get; set; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; set; }
	// methods
	public static NSBatchUpdateRequest BatchUpdateRequestWithEntityName (string entityName);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSBatchUpdateRequestResultType

```
[Serializable]
public enum NSBatchUpdateRequestResultType {
	StatusOnly = 0,
	UpdatedObjectIDs = 1,
	UpdatedObjectsCount = 2,
}
```

### New Type MonoMac.CoreData.NSBatchUpdateResult

```
public class NSBatchUpdateResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateResult ();
	public NSBatchUpdateResult (MonoMac.Foundation.NSCoder coder);
	public NSBatchUpdateResult (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchUpdateResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSObject Result { get; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSPersistentStoreAsynchronousResult

```
public class NSPersistentStoreAsynchronousResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreAsynchronousResult ();
	public NSPersistentStoreAsynchronousResult (MonoMac.Foundation.NSCoder coder);
	public NSPersistentStoreAsynchronousResult (MonoMac.Foundation.NSObjectFlag t);
	public NSPersistentStoreAsynchronousResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSManagedObjectContext ManagedObjectContext { get; }
	public virtual MonoMac.Foundation.NSError OperationError { get; }
	public virtual MonoMac.Foundation.NSProgress Progress { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreData.NSPersistentStoreResult

```
public class NSPersistentStoreResult : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreResult ();
	public NSPersistentStoreResult (MonoMac.Foundation.NSCoder coder);
	public NSPersistentStoreResult (MonoMac.Foundation.NSObjectFlag t);
	public NSPersistentStoreResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

## Namespace MonoMac.CoreGraphics



### Type Changed: MonoMac.CoreGraphics.CGEvent

Removed method:

```
public static System.IntPtr CGEventTapCreate (CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
```

### Type Changed: MonoMac.CoreGraphics.CGVector

Removed method:

```
public override string ToString ();
```

## Namespace MonoMac.CoreImage



### Type Changed: MonoMac.CoreImage.CIAutoAdjustmentFilterOptions

Added fields:

```
public bool? AutoAdjustCrop;
	public bool? AutoAdjustLevel;
```

### Type Changed: MonoMac.CoreImage.CIColor

Added property:

```
public float[] Components { get; }
```

### Type Changed: MonoMac.CoreImage.CIContextOptions

Added properties:

```
public int? CIImageFormat { get; set; }
	public bool? PriorityRequestLow { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDetector

Added properties:

```
public static MonoMac.Foundation.NSString AspectRatio { get; }
	public static MonoMac.Foundation.NSString FocalLength { get; }
	public static MonoMac.Foundation.NSString TypeQRCode { get; }
	public static MonoMac.Foundation.NSString TypeRectangle { get; }
```

Added methods:

```
public static CIDetector CreateQRDetector (CIContext context, CIDetectorOptions detectorOptions);
	public static CIDetector CreateRectangleDetector (CIContext context, CIDetectorOptions detectorOptions);
```

### Type Changed: MonoMac.CoreImage.CIDetectorOptions

Added properties:

```
public float? AspectRatio { get; set; }
	public float? FocalLength { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIFilter

Added constructor:

```
protected CIFilter ();
```

Removed property:

```
public virtual string Name { get; }
```

Added property:

```
public virtual string Name { get; set; }
```

Added method:

```
public static CIFilter GetFilter (string name, MonoMac.Foundation.NSDictionary inputParameters);
```

### Type Changed: MonoMac.CoreImage.CIImage

Added methods:

```
public virtual CIImage CreateByClampingToExtent ();
	public virtual CIImage CreateByCompositingOverImage (CIImage dest);
	public virtual CIImage CreateByFiltering (string filterName, MonoMac.Foundation.NSDictionary inputParameters);
	public virtual CIImage CreateWithOrientation (CIImageOrientation orientation);
	public virtual MonoMac.CoreGraphics.CGAffineTransform GetImageTransform (CIImageOrientation orientation);
```

### Type Changed: MonoMac.CoreImage.CIKernel

Removed method:

```
public static CIKernel[] FromProgram (string coreImageShaderProgram);
```

Added methods:

```
public static CIKernel FromProgram (string coreImageShaderProgram);
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
```

### Type Changed: MonoMac.CoreImage.CIVector

Added constructors:

```
public CIVector (MonoMac.CoreGraphics.CGAffineTransform r);
	public CIVector (System.Drawing.RectangleF r);
	public CIVector (System.Drawing.PointF p);
```

### New Type MonoMac.CoreImage.CIAccordionFoldTransition

```
public class CIAccordionFoldTransition : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAccordionFoldTransition ();
	public CIAccordionFoldTransition (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIAreaHistogram

```
public class CIAreaHistogram : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAreaHistogram ();
	public CIAreaHistogram (System.IntPtr handle);
	// properties
	public float Count { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
}
```

### New Type MonoMac.CoreImage.CIAztecCodeGenerator

```
public class CIAztecCodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAztecCodeGenerator ();
	public CIAztecCodeGenerator (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIBarcodeFeature

```
public class CIBarcodeFeature : MonoMac.CoreImage.CIFeature, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIBarcodeFeature ();
	public CIBarcodeFeature (MonoMac.Foundation.NSCoder coder);
	public CIBarcodeFeature (MonoMac.Foundation.NSObjectFlag t);
	public CIBarcodeFeature (System.IntPtr handle);
	// properties
	public virtual System.Drawing.PointF BottomLeft { get; }
	public virtual System.Drawing.PointF BottomRight { get; }
	public virtual System.Drawing.RectangleF Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSData CodeRawData { get; }
	public virtual string CodeString { get; }
	public virtual string CodeType { get; }
	public virtual MonoMac.Foundation.NSNumber ErrorCorrectionLevel { get; }
	public virtual System.Drawing.PointF TopLeft { get; }
	public virtual System.Drawing.PointF TopRight { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CoreImage.CICode128BarcodeGenerator

```
public class CICode128BarcodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CICode128BarcodeGenerator ();
	public CICode128BarcodeGenerator (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIDivideBlendMode

```
public class CIDivideBlendMode : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIDivideBlendMode ();
	public CIDivideBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIGlassDistortion

```
public class CIGlassDistortion : MonoMac.CoreImage.CIDistortionFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIGlassDistortion ();
	public CIGlassDistortion (System.IntPtr handle);
	// properties
	public float Scale { get; set; }
	public CIImage Texture { get; set; }
}
```

### New Type MonoMac.CoreImage.CIHistogramDisplayFilter

```
public class CIHistogramDisplayFilter : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIHistogramDisplayFilter ();
	public CIHistogramDisplayFilter (System.IntPtr handle);
	// properties
	public float Height { get; set; }
	public float HighLimit { get; set; }
	public float LowLimit { get; set; }
}
```

### New Type MonoMac.CoreImage.CILinearBurnBlendMode

```
public class CILinearBurnBlendMode : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearBurnBlendMode ();
	public CILinearBurnBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CILinearDodgeBlendMode

```
public class CILinearDodgeBlendMode : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearDodgeBlendMode ();
	public CILinearDodgeBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIPinLightBlendMode

```
public class CIPinLightBlendMode : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPinLightBlendMode ();
	public CIPinLightBlendMode (System.IntPtr handle);
}
```

### New Type MonoMac.CoreImage.CIRectangleFeature

```
public class CIRectangleFeature : MonoMac.CoreImage.CIFeature, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIRectangleFeature ();
	public CIRectangleFeature (MonoMac.Foundation.NSCoder coder);
	public CIRectangleFeature (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CoreImage.CISubtractBlendMode

```
public class CISubtractBlendMode : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CISubtractBlendMode ();
	public CISubtractBlendMode (System.IntPtr handle);
}
```

## Namespace MonoMac.CoreLocation



### Type Changed: MonoMac.CoreLocation.CLLocationManagerDelegate

Removed interface:

```
ICLLocationManagerDelegate
```

### Removed Type MonoMac.CoreLocation.CLLocationManagerDelegate_Extensions ### Removed Type MonoMac.CoreLocation.ICLLocationManagerDelegate ### New Type MonoMac.CoreLocation.CLBeaconRegion

```
public class CLBeaconRegion {
	// constructors

	[Obsolete ("Does not return a valid instance on iOS8")]
	public CLBeaconRegion ();
}
```





## Namespace MonoMac.CoreMedia



### Type Changed: MonoMac.CoreMedia.CMFormatDescription

Added method:

```
public MonoMac.Foundation.NSObject GetExtension (string extensionKey);
```

### Type Changed: MonoMac.CoreMedia.CMSampleBuffer

Added methods:

```
public CMSampleBufferError CallForEachSample (System.Func<CMSampleBuffer,System.Int32,MonoMac.CoreMedia.CMSampleBufferError> callback);
	public static CMSampleBuffer CreateReady (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMSampleTimingInfo[] sampleTimingArray, uint[] sampleSizeArray, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithImageBuffer (MonoMac.CoreVideo.CVImageBuffer imageBuffer, CMFormatDescription formatDescription, CMSampleTimingInfo[] sampleTiming, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, MonoMac.AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
	public CMSampleBufferError SetInvalidateCallback (System.Action<CMSampleBuffer> invalidateHandler);
```

### Type Changed: MonoMac.CoreMedia.CMTime

Added properties:

```
public bool HasBeenRounded { get; }
	public bool IsNumeric { get; }
```

## Namespace MonoMac.CoreText



### Type Changed: MonoMac.CoreText.CTLineBoundsOptions

Added value:

```
IncludeLanguageExtents = 32,
```

## Namespace MonoMac.CoreVideo



### Type Changed: MonoMac.CoreVideo.CVPixelBuffer

Removed field:

```
public static MonoMac.Foundation.NSString OpenGLESCompatibilityKey;
```

Added field:

```
public static MonoMac.Foundation.NSString MetalCompatibilityKey;
```

### Type Changed: MonoMac.CoreVideo.CVPixelBufferAttributes

Removed property:

```
public bool? OpenGLESCompatibility { get; set; }
```

Added property:

```
public bool? AllocateWithIOSurface { get; set; }
```

### Type Changed: MonoMac.CoreVideo.CVPixelFormatDescription

Added fields:

```
public static MonoMac.Foundation.NSString ContainsRgb;
	public static MonoMac.Foundation.NSString ContainsYCbCr;
```

### Type Changed: MonoMac.CoreVideo.CVReturn

Added value:

```
PixelBufferNotMetalCompatible = -6684,
```

## Namespace MonoMac.CoreWlan



### Type Changed: MonoMac.CoreWlan.CWChannel

Removed property:

```
public virtual uint ChannelNumber { get; }
```

Added property:

```
public virtual int ChannelNumber { get; }
```

### Type Changed: MonoMac.CoreWlan.CWInterface

Removed property:

```
public virtual uint TransmitPower { get; }
```

Added property:

```
public virtual int TransmitPower { get; }
```

Removed method:

```
public virtual bool SetWEPKey (MonoMac.Foundation.NSData key, CWCipherKeyFlags flags, uint index, out MonoMac.Foundation.NSError error);
```

Added method:

```
public virtual bool SetWEPKey (MonoMac.Foundation.NSData key, CWCipherKeyFlags flags, int index, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.CoreWlan.CWNetwork

Removed property:

```
public virtual uint BeaconInterval { get; }
```

Added property:

```
public virtual int BeaconInterval { get; }
```

## Namespace MonoMac.Foundation



### Type Changed: MonoMac.Foundation.DictionaryContainer

Added methods:

```
protected uint? GetUInt32Value (NSString key);
	protected void SetArrayValue<T> (NSString key, T[] values);
```

### Type Changed: MonoMac.Foundation.INSMachPortDelegate

Added interface:

```
INSPortDelegate
```

### Type Changed: MonoMac.Foundation.INSUrlConnectionDownloadDelegate

Added interface:

```
INSUrlConnectionDelegate
```

### Type Changed: MonoMac.Foundation.NSAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoMac.Foundation.NSBundle

Added methods:

```
public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, string localizationName);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory);
	public virtual NSUrl GetUrlForResource (string name, string fileExtension);
	public static NSUrl GetUrlForResource (string name, string fileExtension, string subdirectory, NSUrl bundleURL);
	public static NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, NSUrl bundleURL);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory);
	public virtual NSUrl[] GetUrlsForResourcesWithExtension (string fileExtension, string subdirectory, string localizationName);
```

### Type Changed: MonoMac.Foundation.NSByteCountFormatter

Added property:

```
public virtual NSFormattingContext FormattingContext { get; set; }
```

### Type Changed: MonoMac.Foundation.NSCachedUrlResponse

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoMac.Foundation.NSCalendar

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

### Type Changed: MonoMac.Foundation.NSCalendarType

Added values:

```
Coptic = 11,
	EthiopicAmeteAlem = 12,
	EthiopicAmeteMihret = 13,
	IslamicTabular = 14,
	IslamicUmmAlQura = 15,
```

### Type Changed: MonoMac.Foundation.NSCalendarUnit

Added value:

```
Nanosecond = 32768,
```

### Type Changed: MonoMac.Foundation.NSData

Added methods:

```
public virtual bool Save (string path, bool atomically);
	public virtual bool Save (NSUrl url, bool atomically);
```

### Type Changed: MonoMac.Foundation.NSDateComponents

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

### Type Changed: MonoMac.Foundation.NSDateFormatter

Added method:

```
public virtual void SetLocalizedDateFormatFromTemplate (string dateFormatTemplate);
```

### Type Changed: MonoMac.Foundation.NSError

Added properties:

```
public static NSString CoreLocationErrorDomain { get; }
	public virtual string HelpAnchor { get; }
	public virtual string LocalizedFailureReason { get; }
	public virtual string[] LocalizedRecoveryOptions { get; }
	public virtual string LocalizedRecoverySuggestion { get; }
	public static NSString MapKitErrorDomain { get; }
	public static NSString NSNetServicesErrorDomain { get; }
	public static NSString NSStreamSocketSSLErrorDomain { get; }
	public static NSString NSStreamSOCKSErrorDomain { get; }
```

### Type Changed: MonoMac.Foundation.NSFileCoordinator

Added property:

```
public virtual string PurposeIdentifier { get; set; }
```

Added method:

```
public virtual void CoordinateAccessWithIntents (NSFileAccessIntent[] intents, NSOperationQueue queue, System.Action<NSError> accessor);
```

### Type Changed: MonoMac.Foundation.NSFileCoordinatorReadingOptions

Added values:

```
ForUploading = 8,
	ImmediatelyAvailableMetadataOnly = 4,
	ResolvesSymbolicLink = 2,
```

### Type Changed: MonoMac.Foundation.NSFileManager

Added methods:

```
public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
```

### Type Changed: MonoMac.Foundation.NSFilePresenter

Added methods:

```
public virtual void AccommodatePresentedItemDeletion (System.Action<NSError> completionHandler);
	public virtual void AccommodatePresentedSubitemDeletion (NSUrl url, System.Action<NSError> completionHandler);
	public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
	public virtual void SavePresentedItemChanges (System.Action<NSError> completionHandler);
```

### Type Changed: MonoMac.Foundation.NSFilePresenter_Extensions

Added methods:

```
public static void AccommodatePresentedItemDeletion (INSFilePresenter This, System.Action<NSError> completionHandler);
	public static void AccommodatePresentedSubitemDeletion (INSFilePresenter This, NSUrl url, System.Action<NSError> completionHandler);
	public static void RelinquishPresentedItemToReader (INSFilePresenter This, NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, NSFilePresenterReacquirer writerAction);
	public static void SavePresentedItemChanges (INSFilePresenter This, System.Action<NSError> completionHandler);
```

### Type Changed: MonoMac.Foundation.NSHttpCookieStorage

Added method:

```
public virtual void RemoveCookiesSinceDate (NSDate date);
```

### Type Changed: MonoMac.Foundation.NSIndexPath

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoMac.Foundation.NSIndexSet

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

### Type Changed: MonoMac.Foundation.NSInputStream

Removed method:

```
public int Read (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoMac.Foundation.NSMachPort

Added constructors:

```
public NSMachPort (uint machPort);
	public NSMachPort (uint machPort, NSMachPortRights options);
```

### Type Changed: MonoMac.Foundation.NSMetadataQuery

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

### Type Changed: MonoMac.Foundation.NSMethodSignature

Added property:

```
public virtual System.IntPtr MethodReturnType { get; }
```

Added methods:

```
public static NSMethodSignature FromObjcTypes (System.IntPtr utf8objctypes);
	public virtual System.IntPtr GetArgumentType (uint index);
```

### Type Changed: MonoMac.Foundation.NSMutableArray

Added methods:

```
public static NSMutableArray FromFile (string path);
	public static NSMutableArray FromUrl (NSUrl url);
```

### Type Changed: MonoMac.Foundation.NSMutableAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: MonoMac.Foundation.NSMutableIndexSet

Added interface:

```
INSSecureCoding
```

Added methods:

```
public virtual void AddIndexesInRange (NSRange range);
	public virtual void RemoveIndexesInRange (NSRange range);
```

### Type Changed: MonoMac.Foundation.NSObject

Removed method:

```
public static bool IsNewRefcountEnabled ();
```

Added method:

```
public virtual void RemoveObserver (NSObject observer, NSString keyPath, System.IntPtr context);
```

### Type Changed: MonoMac.Foundation.NSOperation

Added properties:

```
public virtual bool Asynchronous { get; }
	public virtual string Name { get; set; }
	public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoMac.Foundation.NSOperationQueue

Added properties:

```
public virtual NSQualityOfService QualityOfService { get; set; }
	public virtual MonoMac.CoreFoundation.DispatchQueue UnderlyingQueue { get; set; }
```

### Type Changed: MonoMac.Foundation.NSOutputStream

Removed methods:

```
public static NSOutputStream OutputStreamToMemory ();
	public int Write (byte[] buffer);
	public int Write (byte[] buffer, int offset, uint len);
```

Added method:

```
public static NSObject OutputStreamToMemory ();
```

### Type Changed: MonoMac.Foundation.NSPort

Added methods:

```
public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual bool SendBeforeDate (NSDate limitDate, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
	public virtual bool SendBeforeDate (NSDate limitDate, uint msgID, NSMutableArray components, NSPort receivePort, uint headerSpaceReserved);
```

### Type Changed: MonoMac.Foundation.NSProcessInfo

Added property:

```
public virtual NSOperatingSystemVersion OperatingSystemVersion { get; }
```

Added method:

```
public virtual bool IsOperatingSystemAtLeastVersion (NSOperatingSystemVersion version);
```

### Type Changed: MonoMac.Foundation.NSSet

Added method:

```
public virtual NSObject LookupMember (NSObject probe);
```

### Type Changed: MonoMac.Foundation.NSStream

Added methods:

```
public static void GetBoundStreams (uint bufferSize, out NSInputStream inputStream, out NSOutputStream outputStream);
	public static void GetStreamsToHost (string hostname, int port, out NSInputStream inputStream, out NSOutputStream outputStream);
```

### Type Changed: MonoMac.Foundation.NSString

Added methods:

```
public virtual bool Contains (NSString str);
	public static uint DetectStringEncoding (NSData rawData, EncodingDetectionOptions options, out string convertedString, out bool usedLossyConversion);
	public static uint DetectStringEncoding (NSData rawData, NSDictionary options, out string convertedString, out bool usedLossyConversion);
	public virtual bool LocalizedCaseInsensitiveContains (NSString str);
```

### Type Changed: MonoMac.Foundation.NSThread

Added property:

```
public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: MonoMac.Foundation.NSUrl

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
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value, out NSError error);
```

### Type Changed: MonoMac.Foundation.NSUrlCache

Added methods:

```
public virtual void GetCachedResponse (NSUrlSessionDataTask dataTask, System.Action<NSCachedUrlResponse> completionHandler);
	public virtual System.Threading.Tasks.Task<NSCachedUrlResponse> GetCachedResponseAsync (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponse (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponsesSinceDate (NSDate date);
	public virtual void StoreCachedResponse (NSCachedUrlResponse cachedResponse, NSUrlSessionDataTask dataTask);
```

### Type Changed: MonoMac.Foundation.NSUrlComponents

Added property:

```
public virtual NSUrlQueryItem[] QueryItems { get; set; }
```

Added method:

```
public virtual string AsString ();
```

### Type Changed: MonoMac.Foundation.NSValue

Added properties:

```
public virtual MonoMac.CoreAnimation.CATransform3D CATransform3DValue { get; }
	public virtual MonoMac.SceneKit.SCNMatrix4 SCNMatrix4Value { get; }
```

Added methods:

```
public static NSValue FromCATransform3D (MonoMac.CoreAnimation.CATransform3D transform);
	public static NSValue FromSCNMatrix4 (MonoMac.SceneKit.SCNMatrix4 matrix);
```

### New Type MonoMac.Foundation.EncodingDetectionOptions

```
public class EncodingDetectionOptions : MonoMac.Foundation.DictionaryContainer {
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

### New Type MonoMac.Foundation.EnumerateDatesCallback

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

### New Type MonoMac.Foundation.EnumerateIndexSetCallback

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

### New Type MonoMac.Foundation.INSExtensionRequestHandling

```
public interface INSExtensionRequestHandling : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
}
```

### New Type MonoMac.Foundation.INSUrlSessionDataDelegate

```
public interface INSUrlSessionDataDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUrlSessionDelegate

```
public interface INSUrlSessionDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.INSUrlSessionDownloadDelegate

```
public interface INSUrlSessionDownloadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUrlSessionTaskDelegate

```
public interface INSUrlSessionTaskDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionDelegate {
}
```

### New Type MonoMac.Foundation.INSUserActivityDelegate

```
public interface INSUserActivityDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.Foundation.NSAppleScript

```
public class NSAppleScript : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAppleScript (NSCoder coder);
	public NSAppleScript (NSObjectFlag t);
	public NSAppleScript (System.IntPtr handle);
	public NSAppleScript (string source);
	public NSAppleScript (NSUrl url, out NSDictionary errorInfo);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Compiled { get; }
	public virtual string Source { get; }
	// methods
	public virtual bool CompileAndReturnError (out NSDictionary errorInfo);
	public virtual NSObject Copy (NSZone zone);
	public virtual NSAppleEventDescriptor ExecuteAndReturnError (out NSDictionary errorInfo);
	public virtual NSAppleEventDescriptor ExecuteAppleEvent (NSAppleEventDescriptor eventDescriptor, out NSDictionary errorInfo);
}
```

### New Type MonoMac.Foundation.NSCocoaError

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

### New Type MonoMac.Foundation.NSDateComponentsFormatter

```
public class NSDateComponentsFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSDateComponentsFormatterUnitsStyle

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

### New Type MonoMac.Foundation.NSDateComponentsFormatterZeroFormattingBehavior

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

### New Type MonoMac.Foundation.NSDateIntervalFormatter

```
public class NSDateIntervalFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSDateIntervalFormatterStyle

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

### New Type MonoMac.Foundation.NSEnergyFormatter

```
public class NSEnergyFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSEnergyFormatterUnit

```
[Serializable]
public enum NSEnergyFormatterUnit {
	Calorie = 1793,
	Joule = 11,
	Kilocalorie = 1794,
	Kilojoule = 14,
}
```

### New Type MonoMac.Foundation.NSExtensionContext

```
public class NSExtensionContext : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSExtensionItem

```
public class NSExtensionItem : MonoMac.Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSExtensionRequestHandling

```
public abstract class NSExtensionRequestHandling : MonoMac.Foundation.NSObject, INSExtensionRequestHandling, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionRequestHandling ();
	public NSExtensionRequestHandling (NSCoder coder);
	public NSExtensionRequestHandling (NSObjectFlag t);
	public NSExtensionRequestHandling (System.IntPtr handle);
	// methods
	public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
}
```

### New Type MonoMac.Foundation.NSExtensionRequestHandling_Extensions

```
public static class NSExtensionRequestHandling_Extensions {
}
```

### New Type MonoMac.Foundation.NSFileAccessIntent

```
public class NSFileAccessIntent : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSFileAccessIntent (NSCoder coder);
	public NSFileAccessIntent (NSObjectFlag t);
	public NSFileAccessIntent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static NSFileAccessIntent ReadingIntentWithURL (NSUrl url, NSFileCoordinatorReadingOptions options);
	public static NSFileAccessIntent WritingIntentWithURL (NSUrl url, NSFileCoordinatorWritingOptions options);
}
```

### New Type MonoMac.Foundation.NSFilePresenterReacquirer

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

### New Type MonoMac.Foundation.NSFormattingContext

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

### New Type MonoMac.Foundation.NSFormattingUnitStyle

```
[Serializable]
public enum NSFormattingUnitStyle {
	Long = 3,
	Medium = 2,
	Short = 1,
}
```

### New Type MonoMac.Foundation.NSItemProvider

```
public class NSItemProvider : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual void LoadItem (string typeIdentifier, NSDictionary options, System.Action<NSObject,MonoMac.Foundation.NSError> completionHandler);
	public virtual void LoadPreviewImage (NSDictionary options, System.Action<NSObject,MonoMac.Foundation.NSError> completionHandler);
	public virtual void RegisterItemForTypeIdentifier (string typeIdentifier, NSItemProviderLoadHandler loadHandler);
	public virtual void SetPreviewImageHandler (NSItemProviderLoadHandler handler);
}
```

### New Type MonoMac.Foundation.NSItemProviderCompletionHandler

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

### New Type MonoMac.Foundation.NSItemProviderErrorCode

```
[Serializable]
public enum NSItemProviderErrorCode {
	ItemUnavailable = -1000,
	None = 0,
	UnexpectedValueClass = -1100,
	Unknown = -1,
}
```

### New Type MonoMac.Foundation.NSItemProviderLoadHandler

```
public sealed delegate NSItemProviderLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSItemProviderLoadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSItemProviderCompletionHandler completionHandler, MonoMac.ObjCRuntime.Class expectedValueClass, NSDictionary options, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSItemProviderCompletionHandler completionHandler, MonoMac.ObjCRuntime.Class expectedValueClass, NSDictionary options);
}
```

### New Type MonoMac.Foundation.NSLengthFormatter

```
public class NSLengthFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSLengthFormatterUnit

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

### New Type MonoMac.Foundation.NSMassFormatter

```
public class NSMassFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSMassFormatterUnit

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

### New Type MonoMac.Foundation.NSOperatingSystemVersion

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

### New Type MonoMac.Foundation.NSQualityOfService

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

### New Type MonoMac.Foundation.NSUrl_PromisedItems

```
public static class NSUrl_PromisedItems {
	// methods
	public static bool CheckPromisedItemIsReachable (NSUrl This, out NSError error);
	public static bool GetPromisedItemResourceValue (NSUrl This, NSObject value, NSString key, out NSError error);
	public static NSDictionary GetPromisedItemResourceValues (NSUrl This, NSString[] keys, out NSError error);
}
```

### New Type MonoMac.Foundation.NSUrlQueryItem

```
public class NSUrlQueryItem : MonoMac.Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSURLRelationship

```
[Serializable]
public enum NSURLRelationship {
	Contains = 0,
	Other = 2,
	Same = 1,
}
```

### New Type MonoMac.Foundation.NSUrlSession

```
public class NSUrlSession : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSession ();
	public NSUrlSession (NSCoder coder);
	public NSUrlSession (NSObjectFlag t);
	public NSUrlSession (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrlSessionConfiguration Configuration { get; }
	public NSUrlSessionDelegate Delegate { get; }
	public virtual NSOperationQueue DelegateQueue { get; }
	public virtual string SessionDescription { get; set; }
	public static NSUrlSession SharedSession { get; }
	public virtual NSObject WeakDelegate { get; }
	// methods
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrl url, out NSUrlSessionDataTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrlRequest request, out NSUrlSessionDataTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateDataTaskAsync (NSUrlRequest request);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionDownloadResponse completionHandler);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSData resumeData);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url);
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrl url, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrl url);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrlRequest request, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskAsync (NSUrlRequest request);
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionDownloadResponse completionHandler);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskFromResumeDataAsync (NSData resumeData, out NSUrlSessionDownloadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDownloadTaskRequest> CreateDownloadTaskFromResumeDataAsync (NSData resumeData);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL, NSUrlSessionResponse completionHandler);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL);
	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL, out NSUrlSessionUploadTask result);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData);
	public virtual System.Threading.Tasks.Task<NSUrlSessionDataTaskRequest> CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData, out NSUrlSessionUploadTask result);
	protected override void Dispose (bool disposing);
	public virtual void FinishTasksAndInvalidate ();
	public virtual void Flush (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task FlushAsync ();
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration);
	public static NSUrlSession FromWeakConfiguration (NSUrlSessionConfiguration configuration, NSObject weakDelegate, NSOperationQueue delegateQueue);
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
	public virtual System.Threading.Tasks.Task<NSUrlSessionActiveTasks> GetTasksAsync ();
	public virtual void InvalidateAndCancel ();
	public virtual void Reset (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task ResetAsync ();
}
```

### New Type MonoMac.Foundation.NSUrlSessionActiveTasks

```
public class NSUrlSessionActiveTasks {
	// constructors
	public NSUrlSessionActiveTasks (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
	// properties
	public NSUrlSessionDataTask[] DataTasks { get; set; }
	public NSUrlSessionDownloadTask[] DownloadTasks { get; set; }
	public NSUrlSessionUploadTask[] UploadTasks { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionConfiguration

```
public class NSUrlSessionConfiguration : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionConfiguration ();
	public NSUrlSessionConfiguration (NSCoder coder);
	public NSUrlSessionConfiguration (NSObjectFlag t);
	public NSUrlSessionConfiguration (System.IntPtr handle);
	// properties
	public virtual bool AllowsCellularAccess { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSDictionary ConnectionProxyDictionary { get; set; }
	public static NSUrlSessionConfiguration DefaultSessionConfiguration { get; }
	public virtual bool Discretionary { get; set; }
	public static NSUrlSessionConfiguration EphemeralSessionConfiguration { get; }
	public virtual NSDictionary HttpAdditionalHeaders { get; set; }
	public virtual NSHttpCookieAcceptPolicy HttpCookieAcceptPolicy { get; set; }
	public virtual NSHttpCookieStorage HttpCookieStorage { get; set; }
	public virtual int HttpMaximumConnectionsPerHost { get; set; }
	public virtual bool HttpShouldSetCookies { get; set; }
	public virtual bool HttpShouldUsePipelining { get; set; }
	public virtual string Identifier { get; }
	public virtual NSUrlRequestNetworkServiceType NetworkServiceType { get; set; }
	public virtual NSUrlRequestCachePolicy RequestCachePolicy { get; set; }
	public virtual bool SessionSendsLaunchEvents { get; set; }
	public virtual double TimeoutIntervalForRequest { get; set; }
	public virtual double TimeoutIntervalForResource { get; set; }
	public virtual MonoMac.Security.SslProtocol TLSMaximumSupportedProtocol { get; set; }
	public virtual MonoMac.Security.SslProtocol TLSMinimumSupportedProtocol { get; set; }
	public virtual NSUrlCache URLCache { get; set; }
	public virtual NSUrlCredentialStorage URLCredentialStorage { get; set; }
	public virtual NSArray WeakProtocolClasses { get; set; }
	// methods
	public static NSUrlSessionConfiguration BackgroundSessionConfiguration (string identifier);
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataDelegate

```
public class NSUrlSessionDataDelegate : MonoMac.Foundation.NSUrlSessionTaskDelegate, INSUrlSessionDataDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
	// constructors
	public NSUrlSessionDataDelegate ();
	public NSUrlSessionDataDelegate (NSCoder coder);
	public NSUrlSessionDataDelegate (NSObjectFlag t);
	public NSUrlSessionDataDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBecomeDownloadTask (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public virtual void DidReceiveData (NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public virtual void DidReceiveResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, System.Action<NSUrlSessionResponseDisposition> completionHandler);
	public virtual void WillCacheResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, System.Action<NSCachedUrlResponse> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataDelegate_Extensions

```
public static class NSUrlSessionDataDelegate_Extensions {
	// methods
	public static void DidBecomeDownloadTask (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public static void DidReceiveData (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public static void DidReceiveResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, System.Action<NSUrlSessionResponseDisposition> completionHandler);
	public static void WillCacheResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, System.Action<NSCachedUrlResponse> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataTask

```
public class NSUrlSessionDataTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionDataTask ();
	public NSUrlSessionDataTask (NSCoder coder);
	public NSUrlSessionDataTask (NSObjectFlag t);
	public NSUrlSessionDataTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionDataTaskRequest

```
public class NSUrlSessionDataTaskRequest {
	// constructors
	public NSUrlSessionDataTaskRequest (NSData data, NSUrlResponse response);
	// properties
	public NSData Data { get; set; }
	public NSUrlResponse Response { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionDelegate

```
public class NSUrlSessionDelegate : MonoMac.Foundation.NSObject, INSUrlSessionDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionDelegate ();
	public NSUrlSessionDelegate (NSCoder coder);
	public NSUrlSessionDelegate (NSObjectFlag t);
	public NSUrlSessionDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBecomeInvalid (NSUrlSession session, NSError error);
	public virtual void DidFinishEventsForBackgroundSession (NSUrlSession session);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDelegate_Extensions

```
public static class NSUrlSessionDelegate_Extensions {
	// methods
	public static void DidBecomeInvalid (INSUrlSessionDelegate This, NSUrlSession session, NSError error);
	public static void DidFinishEventsForBackgroundSession (INSUrlSessionDelegate This, NSUrlSession session);
	public static void DidReceiveChallenge (INSUrlSessionDelegate This, NSUrlSession session, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadDelegate

```
public class NSUrlSessionDownloadDelegate : MonoMac.Foundation.NSUrlSessionTaskDelegate, INSUrlSessionDownloadDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionTaskDelegate, INSUrlSessionDelegate {
	// constructors
	public NSUrlSessionDownloadDelegate ();
	public NSUrlSessionDownloadDelegate (NSCoder coder);
	public NSUrlSessionDownloadDelegate (NSObjectFlag t);
	public NSUrlSessionDownloadDelegate (System.IntPtr handle);
	// properties
	public static NSString TaskResumeDataKey { get; }
	// methods
	public virtual void DidFinishDownloading (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public virtual void DidResume (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public virtual void DidWriteData (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadDelegate_Extensions

```
public static class NSUrlSessionDownloadDelegate_Extensions {
	// methods
	public static void DidFinishDownloading (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public static void DidResume (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public static void DidWriteData (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadResponse

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

### New Type MonoMac.Foundation.NSUrlSessionDownloadTask

```
public class NSUrlSessionDownloadTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionDownloadTask ();
	public NSUrlSessionDownloadTask (NSCoder coder);
	public NSUrlSessionDownloadTask (NSObjectFlag t);
	public NSUrlSessionDownloadTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void Cancel (System.Action<NSData> resumeCallback);
}
```

### New Type MonoMac.Foundation.NSUrlSessionDownloadTaskRequest

```
public class NSUrlSessionDownloadTaskRequest {
	// constructors
	public NSUrlSessionDownloadTaskRequest (NSUrl data, NSUrlResponse response);
	// properties
	public NSUrl Data { get; set; }
	public NSUrlResponse Response { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionPendingTasks

```
public sealed delegate NSUrlSessionPendingTasks : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionPendingTasks (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
}
```

### New Type MonoMac.Foundation.NSUrlSessionResponse

```
public sealed delegate NSUrlSessionResponse : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionResponse (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSData data, NSUrlResponse response, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSData data, NSUrlResponse response, NSError error);
}
```

### New Type MonoMac.Foundation.NSUrlSessionTask

```
public class NSUrlSessionTask : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionTask ();
	public NSUrlSessionTask (NSCoder coder);
	public NSUrlSessionTask (NSObjectFlag t);
	public NSUrlSessionTask (System.IntPtr handle);
	// properties
	public virtual long BytesExpectedToReceive { get; }
	public virtual long BytesExpectedToSend { get; }
	public virtual long BytesReceived { get; }
	public virtual long BytesSent { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual NSUrlRequest CurrentRequest { get; }
	public virtual NSError Error { get; }
	public virtual NSUrlRequest OriginalRequest { get; }
	public virtual float Priority { get; set; }
	public virtual NSUrlResponse Response { get; }
	public virtual NSUrlSessionTaskState State { get; }
	public virtual string TaskDescription { get; set; }
	public virtual uint TaskIdentifier { get; }
	public static long TransferSizeUnknown { get; }
	// methods
	public virtual void Cancel ();
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Resume ();
	public virtual void Suspend ();
}
```

### New Type MonoMac.Foundation.NSUrlSessionTaskDelegate

```
public class NSUrlSessionTaskDelegate : MonoMac.Foundation.NSUrlSessionDelegate, INSUrlSessionTaskDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSUrlSessionDelegate {
	// constructors
	public NSUrlSessionTaskDelegate ();
	public NSUrlSessionTaskDelegate (NSCoder coder);
	public NSUrlSessionTaskDelegate (NSObjectFlag t);
	public NSUrlSessionTaskDelegate (System.IntPtr handle);
	// methods
	public virtual void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public virtual void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public virtual void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public virtual void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
}
```

### New Type MonoMac.Foundation.NSUrlSessionTaskDelegate_Extensions

```
public static class NSUrlSessionTaskDelegate_Extensions {
	// methods
	public static void DidCompleteWithError (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSError error);
	public static void DidReceiveChallenge (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public static void DidSendBodyData (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public static void NeedNewBodyStream (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public static void WillPerformHttpRedirection (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
}
```

### New Type MonoMac.Foundation.NSURLSessionTaskPriority

```
public static class NSURLSessionTaskPriority {
	// properties
	public static float Default { get; }
	public static float High { get; }
	public static float Low { get; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionUploadTask

```
public class NSUrlSessionUploadTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionUploadTask ();
	public NSUrlSessionUploadTask (NSCoder coder);
	public NSUrlSessionUploadTask (NSObjectFlag t);
	public NSUrlSessionUploadTask (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.Foundation.NSUserActivity

```
public class NSUserActivity : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual void GetContinuationStreams (System.Action<NSInputStream,MonoMac.Foundation.NSOutputStream,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<NSUserActivityContinuation> GetContinuationStreamsAsync ();
	public virtual void Invalidate ();
}
```

### New Type MonoMac.Foundation.NSUserActivityContinuation

```
public class NSUserActivityContinuation {
	// constructors
	public NSUserActivityContinuation (NSInputStream arg1, NSOutputStream arg2);
	// properties
	public NSInputStream Arg1 { get; set; }
	public NSOutputStream Arg2 { get; set; }
}
```

### New Type MonoMac.Foundation.NSUserActivityDelegate

```
public class NSUserActivityDelegate : MonoMac.Foundation.NSObject, INSUserActivityDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSUserActivityDelegate_Extensions

```
public static class NSUserActivityDelegate_Extensions {
	// methods
	public static void UserActivityReceivedData (INSUserActivityDelegate This, NSUserActivity userActivity, NSInputStream inputStream, NSOutputStream outputStream);
	public static void UserActivityWasContinued (INSUserActivityDelegate This, NSUserActivity userActivity);
	public static void UserActivityWillSave (INSUserActivityDelegate This, NSUserActivity userActivity);
}
```

### New Type MonoMac.Foundation.NSUserActivityType

```
public static class NSUserActivityType {
	// properties
	public static NSString BrowsingWeb { get; }
}
```

## Namespace MonoMac.GameKit



### Type Changed: MonoMac.GameKit.GKAchievement

Added constructor:

```
public GKAchievement (string identifier, GKPlayer player);
```

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

Added property:

```
public virtual GKPlayer Player { get; }
```

Added methods:

```
public virtual MonoMac.AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
	public virtual void IssueChallengeToPlayers (string[] playerIDs, string message);
	public static void ReportAchievements (GKAchievement[] achievements, GKChallenge[] challenges, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements, GKChallenge[] challenges);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements);
	public virtual void SelectChallengeablePlayerIDs (string[] playerIDs, System.Action<System.String[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<System.String[]> SelectChallengeablePlayerIDsAsync (string[] playerIDs);
	public virtual void SelectChallengeablePlayers (GKPlayer[] players, System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> SelectChallengeablePlayersAsync (GKPlayer[] players);
```

### Type Changed: MonoMac.GameKit.GKAchievementChallenge

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.GameKit.GKAchievementDescription

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.GameKit.GKChallenge

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

Added properties:

```
public virtual GKPlayer IssuingPlayer { get; }
	public virtual GKPlayer ReceivingPlayer { get; }
```

### Type Changed: MonoMac.GameKit.GKFriendRequestComposeViewController

Added method:

```
public virtual void AddRecipientPlayers (GKPlayer[] players);
```

### Type Changed: MonoMac.GameKit.GKInvite

Added properties:

```
public virtual uint PlayerAttributes { get; }
	public virtual int PlayerGroup { get; }
	public virtual GKPlayer Sender { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.GameKit.GKLeaderboard

Added constructor:

```
public GKLeaderboard (GKPlayer[] players);
```

### Type Changed: MonoMac.GameKit.GKLocalPlayer

Added property:

```
public virtual System.Action<MonoMac.AppKit.NSViewController,MonoMac.Foundation.NSError> AuthenticateHandler { get; set; }
```

Added methods:

```
public virtual void DeleteSavedGamesWithName (string name, System.Action<MonoMac.Foundation.NSError> handler);
	public virtual void FetchSavedGamesWithCompletionHandler (System.Action<MonoMac.Foundation.NSArray,MonoMac.Foundation.NSError> handler);
	public virtual void GenerateIdentityVerificationSignature (GKIdentityVerificationSignatureHandler completionHandler);
	public virtual void LoadDefaultLeaderboardCategoryID (System.Action<System.String,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardCategoryIDAsync ();
	public virtual void LoadDefaultLeaderboardIdentifier (System.Action<System.String,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardIdentifierAsync ();
	public virtual void LoadFriendPlayers (System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> LoadFriendPlayersAsync ();
	public virtual void RegisterListener (GKLocalPlayerListener listener);
	public virtual void ResolveConflictingSavedGames (MonoMac.Foundation.NSObject[] conflictingSavedGames, MonoMac.Foundation.NSData data, System.Action<MonoMac.Foundation.NSArray,MonoMac.Foundation.NSError> handler);
	public virtual void SaveGameData (MonoMac.Foundation.NSData data, string name, System.Action<GKSavedGame,MonoMac.Foundation.NSError> handler);
	public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
	public virtual void SetDefaultLeaderboardIdentifier (string leaderboardIdentifier, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardIdentifierAsync (string leaderboardIdentifier);
	public virtual void UnregisterAllListeners ();
	public virtual void UnregisterListener (GKLocalPlayerListener listener);
```

### Type Changed: MonoMac.GameKit.GKMatch

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
	public virtual bool SendData (MonoMac.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.GameKit.GKMatchDelegate

Added methods:

```
public virtual void ChangedConnectionState (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public virtual void ReceivedDataFromRemotePlayer (GKMatch match, MonoMac.Foundation.NSData data, GKPlayer player);
	public virtual bool ShouldReinviteDisconnectedPlayer (GKMatch match, GKPlayer player);
```

### Type Changed: MonoMac.GameKit.GKMatchDelegate_Extensions

Added methods:

```
public static void ChangedConnectionState (IGKMatchDelegate This, GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public static void ReceivedDataFromRemotePlayer (IGKMatchDelegate This, GKMatch match, MonoMac.Foundation.NSData data, GKPlayer player);
	public static bool ShouldReinviteDisconnectedPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player);
```

### Type Changed: MonoMac.GameKit.GKMatchmaker

Added methods:

```
public virtual void CancelPendingInvite (GKPlayer player);
	public virtual void FindPlayersForHostedRequest (GKMatchRequest request, System.Action<GKPlayer[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> FindPlayersForHostedRequestAsync (GKMatchRequest request);
	public virtual void StartBrowsingForNearbyPlayersWithHandler (System.Action<GKPlayer,System.Boolean> reachableHandler);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewController

Added events:

```
public event System.EventHandler<GKMatchmakingPlayersEventArgs> DidFindHostedPlayers;
	public event System.EventHandler<GKMatchmakingPlayerEventArgs> HostedPlayerDidAccept;
```

Added method:

```
public virtual void SetHostedPlayerDidConnect (GKPlayer playerID, bool connected);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewControllerDelegate

Added methods:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
	public virtual void HostedPlayerDidAccept (GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoMac.GameKit.GKMatchmakerViewControllerDelegate_Extensions

Added method:

```
public static void HostedPlayerDidAccept (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: MonoMac.GameKit.GKMatchRequest

Added properties:

```
public virtual System.Action<GKPlayer,MonoMac.GameKit.GKInviteRecipientResponse> RecipientResponseHandler { get; set; }
	public virtual GKPlayer[] Recipients { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.GameKit.GKScore

Added constructor:

```
public GKScore (string identifier, GKPlayer player);
```

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

Added method:

```
public virtual MonoMac.AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
```

### Type Changed: MonoMac.GameKit.GKScoreChallenge

Added interface:

```
MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.GameKit.GKTurnBasedExchange

Added constructors:

```
public GKTurnBasedExchange (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedExchange (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedExchange (System.IntPtr handle);
```

Added interfaces:

```
MonoMac.ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDate CompletionDate { get; }
	public virtual MonoMac.Foundation.NSData Data { get; }
	public virtual string ExchangeID { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant[] Recipients { get; }
	public virtual GKTurnBasedExchangeReply[] Replies { get; }
	public virtual MonoMac.Foundation.NSDate SendDate { get; }
	public virtual GKTurnBasedParticipant Sender { get; }
	public virtual GKTurnBasedExchangeStatus Status { get; }
	public virtual MonoMac.Foundation.NSDate TimeoutDate { get; }
	public static double TimeoutDefault { get; }
	public static double TimeoutNone { get; }
```

Added methods:

```
public virtual void Cancel (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task CancelAsync (string localizableMessage, MonoMac.Foundation.NSObject[] arguments);
	protected override void Dispose (bool disposing);
	public virtual void Reply (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, MonoMac.Foundation.NSData data, System.Action<MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task ReplyAsync (string localizableMessage, MonoMac.Foundation.NSObject[] arguments, MonoMac.Foundation.NSData data);
```

### Type Changed: MonoMac.GameKit.GKTurnBasedExchangeReply

Added constructors:

```
public GKTurnBasedExchangeReply (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedExchangeReply (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedExchangeReply (System.IntPtr handle);
```

Added interfaces:

```
MonoMac.ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSData Data { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant Recipient { get; }
	public virtual MonoMac.Foundation.NSDate ReplyDate { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.GameKit.GKTurnBasedParticipant

Added property:

```
public virtual GKPlayer Player { get; }
```

### Type Changed: MonoMac.GameKit.GKVoiceChat

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public virtual System.Action<GKPlayer,MonoMac.GameKit.GKVoiceChatPlayerState> PlayerVoiceChatStateDidChangeHandler { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetMuteStatus (GKPlayer player, bool isMuted);
```

### Type Changed: MonoMac.GameKit.IGKMatchmakerViewControllerDelegate

Added method:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
```

### New Type MonoMac.GameKit.GKChallengeComposeHandler

```
public sealed delegate GKChallengeComposeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKChallengeComposeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs);
}
```

### New Type MonoMac.GameKit.GKChallengeListener

```
public class GKChallengeListener : MonoMac.Foundation.NSObject, IGKChallengeListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKChallengeListener ();
	public GKChallengeListener (MonoMac.Foundation.NSCoder coder);
	public GKChallengeListener (MonoMac.Foundation.NSObjectFlag t);
	public GKChallengeListener (System.IntPtr handle);
	// methods
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKChallengeListener_Extensions

```
public static class GKChallengeListener_Extensions {
	// methods
	public static void DidCompleteChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void DidReceiveChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
	public static void IssuedChallengeWasCompleted (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void WantsToPlayChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKGameCenterControllerDelegate

```
public class GKGameCenterControllerDelegate : MonoMac.Foundation.NSObject, IGKGameCenterControllerDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKGameCenterControllerDelegate ();
	public GKGameCenterControllerDelegate (MonoMac.Foundation.NSCoder coder);
	public GKGameCenterControllerDelegate (MonoMac.Foundation.NSObjectFlag t);
	public GKGameCenterControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void Finished (GKGameCenterViewController controller);
}
```

### New Type MonoMac.GameKit.GKGameCenterControllerDelegate_Extensions

```
public static class GKGameCenterControllerDelegate_Extensions {
	// methods
	public static void Finished (IGKGameCenterControllerDelegate This, GKGameCenterViewController controller);
}
```

### New Type MonoMac.GameKit.GKGameCenterViewController

```
public class GKGameCenterViewController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKGameCenterViewController ();
	public GKGameCenterViewController (MonoMac.Foundation.NSCoder coder);
	public GKGameCenterViewController (MonoMac.Foundation.NSObjectFlag t);
	public GKGameCenterViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public GKGameCenterControllerDelegate Delegate { get; set; }

	[Obsolete ("Use LeaderboardIdentifier instead")]
	public virtual string LeaderboardCategory { get; set; }
	public virtual string LeaderboardIdentifier { get; set; }

	[Obsolete ("This class no longer support Leaderboard Time Scopes, will always default to AllTime")]
	public virtual GKLeaderboardTimeScope LeaderboardTimeScope { get; set; }
	public virtual GKGameCenterViewControllerState ViewState { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler Finished;
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.GameKit.GKIdentityVerificationSignatureHandler

```
public sealed delegate GKIdentityVerificationSignatureHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKIdentityVerificationSignatureHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSUrl publicKeyUrl, MonoMac.Foundation.NSData signature, MonoMac.Foundation.NSData salt, ulong timestamp, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSUrl publicKeyUrl, MonoMac.Foundation.NSData signature, MonoMac.Foundation.NSData salt, ulong timestamp, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.GameKit.GKInviteEventListener

```
public class GKInviteEventListener : MonoMac.Foundation.NSObject, IGKInviteEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKInviteEventListener ();
	public GKInviteEventListener (MonoMac.Foundation.NSCoder coder);
	public GKInviteEventListener (MonoMac.Foundation.NSObjectFlag t);
	public GKInviteEventListener (System.IntPtr handle);
	// methods
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type MonoMac.GameKit.GKInviteEventListener_Extensions

```
public static class GKInviteEventListener_Extensions {
	// methods
	public static void DidAcceptInvite (IGKInviteEventListener This, GKPlayer player, GKInvite invite);
	public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type MonoMac.GameKit.GKInviteRecipientResponse

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

### New Type MonoMac.GameKit.GKLocalPlayerListener

```
public class GKLocalPlayerListener : MonoMac.Foundation.NSObject, IGKLocalPlayerListener, IGKChallengeListener, IGKInviteEventListener, IGKTurnBasedEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKLocalPlayerListener ();
	public GKLocalPlayerListener (MonoMac.Foundation.NSCoder coder);
	public GKLocalPlayerListener (MonoMac.Foundation.NSObjectFlag t);
	public GKLocalPlayerListener (System.IntPtr handle);
	// methods
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
```

### New Type MonoMac.GameKit.GKLocalPlayerListener_Extensions

```
public static class GKLocalPlayerListener_Extensions {
}
```

### New Type MonoMac.GameKit.GKMatchConnectionChangedEventArgs

```
public class GKMatchConnectionChangedEventArgs : System.EventArgs {
	// constructors
	public GKMatchConnectionChangedEventArgs (GKPlayer player, GKPlayerConnectionState state);
	// properties
	public GKPlayer Player { get; set; }
	public GKPlayerConnectionState State { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchmakingPlayerEventArgs

```
public class GKMatchmakingPlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayerEventArgs (GKPlayer playerID);
	// properties
	public GKPlayer PlayerID { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchmakingPlayersEventArgs

```
public class GKMatchmakingPlayersEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayersEventArgs (GKPlayer[] playerIDs);
	// properties
	public GKPlayer[] PlayerIDs { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchReceivedDataFromRemotePlayerEventArgs

```
public class GKMatchReceivedDataFromRemotePlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchReceivedDataFromRemotePlayerEventArgs (MonoMac.Foundation.NSData data, GKPlayer player);
	// properties
	public MonoMac.Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
}
```

### New Type MonoMac.GameKit.GKMatchReinvitationForDisconnectedPlayer

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

### New Type MonoMac.GameKit.GKSavedGame

```
public class GKSavedGame : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGame ();
	public GKSavedGame (MonoMac.Foundation.NSCoder coder);
	public GKSavedGame (MonoMac.Foundation.NSObjectFlag t);
	public GKSavedGame (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DeviceName { get; }
	public virtual MonoMac.Foundation.NSDate ModificationDate { get; }
	public virtual string Name { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void LoadDataWithCompletionHandler (System.Action<MonoMac.Foundation.NSData,MonoMac.Foundation.NSError> handler);
}
```

### New Type MonoMac.GameKit.GKSavedGameListener

```
public class GKSavedGameListener : MonoMac.Foundation.NSObject, IGKSavedGameListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGameListener ();
	public GKSavedGameListener (MonoMac.Foundation.NSCoder coder);
	public GKSavedGameListener (MonoMac.Foundation.NSObjectFlag t);
	public GKSavedGameListener (System.IntPtr handle);
	// methods
	public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void HasConflictingSavedGames (GKPlayer player, MonoMac.Foundation.NSObject[] savedGames);
}
```

### New Type MonoMac.GameKit.GKSavedGameListener_Extensions

```
public static class GKSavedGameListener_Extensions {
	// methods
	public static void DidModifySavedGame (IGKSavedGameListener This, GKPlayer player, GKSavedGame savedGame);
	public static void HasConflictingSavedGames (IGKSavedGameListener This, GKPlayer player, MonoMac.Foundation.NSObject[] savedGames);
}
```

### New Type MonoMac.GameKit.GKTurnBasedEventListener

```
public class GKTurnBasedEventListener : MonoMac.Foundation.NSObject, IGKTurnBasedEventListener, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKTurnBasedEventListener ();
	public GKTurnBasedEventListener (MonoMac.Foundation.NSCoder coder);
	public GKTurnBasedEventListener (MonoMac.Foundation.NSObjectFlag t);
	public GKTurnBasedEventListener (System.IntPtr handle);
	// methods
	public virtual void DidRequestMatchWithOtherPlayers (GKPlayer player, GKPlayer[] playersToInvite);
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string[] playerIDsToInvite);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
```

### New Type MonoMac.GameKit.GKTurnBasedEventListener_Extensions

```
public static class GKTurnBasedEventListener_Extensions {
	// methods
	public static void DidRequestMatchWithOtherPlayers (IGKTurnBasedEventListener This, GKPlayer player, GKPlayer[] playersToInvite);
	public static void DidRequestMatchWithPlayers (IGKTurnBasedEventListener This, GKPlayer player, string[] playerIDsToInvite);
	public static void MatchEnded (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
	public static void ReceivedExchangeCancellation (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeReplies (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeRequest (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedTurnEvent (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
```

### New Type MonoMac.GameKit.IGKChallengeListener

```
public interface IGKChallengeListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKGameCenterControllerDelegate

```
public interface IGKGameCenterControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKInviteEventListener

```
public interface IGKInviteEventListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKLocalPlayerListener

```
public interface IGKLocalPlayerListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IGKChallengeListener, IGKInviteEventListener, IGKTurnBasedEventListener {
}
```

### New Type MonoMac.GameKit.IGKSavedGameListener

```
public interface IGKSavedGameListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.GameKit.IGKTurnBasedEventListener

```
public interface IGKTurnBasedEventListener : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoMac.ImageIO



### Type Changed: MonoMac.ImageIO.CGImageDestinationOptions

Added properties:

```
public bool EmbedThumbnail { get; set; }
	public int? ImageMaxPixelSize { get; set; }
	public bool ShouldExcludeGPS { get; set; }
```

### Type Changed: MonoMac.ImageIO.CGImageProperties

Added properties:

```
public static MonoMac.Foundation.NSString GPSHPositioningError { get; }
	public static MonoMac.Foundation.NSString PNGDelayTime { get; }
	public static MonoMac.Foundation.NSString PNGLoopCount { get; }
	public static MonoMac.Foundation.NSString PNGUnclampedDelayTime { get; }
```

### New Type MonoMac.ImageIO.CGImagePropertyOrientation

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

## Namespace MonoMac.MobileCoreServices

### Type Changed: MonoMac.MobileCoreServices.UTType

Removed fields:

```
public static MonoMac.Foundation.NSString AliasFile;
	public static MonoMac.Foundation.NSString AliasRecord;
	public static MonoMac.Foundation.NSString AppleICNS;
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Audio;
	public static MonoMac.Foundation.NSString Application;
	public static MonoMac.Foundation.NSString ApplicationBundle;
	public static MonoMac.Foundation.NSString ApplicationFile;
	public static MonoMac.Foundation.NSString Archive;
	public static MonoMac.Foundation.NSString Audio;
	public static MonoMac.Foundation.NSString AudiovisualContent;
	public static MonoMac.Foundation.NSString BMP;
	public static MonoMac.Foundation.NSString Bundle;
	public static MonoMac.Foundation.NSString CHeader;
	public static MonoMac.Foundation.NSString CompositeContent;
	public static MonoMac.Foundation.NSString ConformsToKey;
	public static MonoMac.Foundation.NSString Contact;
	public static MonoMac.Foundation.NSString Content;
	public static MonoMac.Foundation.NSString CPlusPlusHeader;
	public static MonoMac.Foundation.NSString CPlusPlusSource;
	public static MonoMac.Foundation.NSString CSource;
	public static MonoMac.Foundation.NSString Data;
	public static MonoMac.Foundation.NSString DescriptionKey;
	public static MonoMac.Foundation.NSString Directory;
	public static MonoMac.Foundation.NSString DiskImage;
	public static MonoMac.Foundation.NSString ExportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString FileURL;
	public static MonoMac.Foundation.NSString FlatRTFD;
	public static MonoMac.Foundation.NSString Folder;
	public static MonoMac.Foundation.NSString Framework;
	public static MonoMac.Foundation.NSString GIF;
	public static MonoMac.Foundation.NSString HTML;
	public static MonoMac.Foundation.NSString ICO;
	public static MonoMac.Foundation.NSString IconFileKey;
	public static MonoMac.Foundation.NSString IdentifierKey;
	public static MonoMac.Foundation.NSString Image;
	public static MonoMac.Foundation.NSString ImportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString InkText;
	public static MonoMac.Foundation.NSString Item;
	public static MonoMac.Foundation.NSString JavaSource;
	public static MonoMac.Foundation.NSString JPEG;
	public static MonoMac.Foundation.NSString JPEG2000;
	public static MonoMac.Foundation.NSString Message;
	public static MonoMac.Foundation.NSString MountPoint;
	public static MonoMac.Foundation.NSString Movie;
	public static MonoMac.Foundation.NSString MP3;
	public static MonoMac.Foundation.NSString MPEG;
	public static MonoMac.Foundation.NSString MPEG4;
	public static MonoMac.Foundation.NSString MPEG4Audio;
	public static MonoMac.Foundation.NSString ObjectiveCPlusPlusSource;
	public static MonoMac.Foundation.NSString ObjectiveCSource;
	public static MonoMac.Foundation.NSString Package;
	public static MonoMac.Foundation.NSString PDF;
	public static MonoMac.Foundation.NSString PICT;
	public static MonoMac.Foundation.NSString PlainText;
	public static MonoMac.Foundation.NSString PNG;
	public static MonoMac.Foundation.NSString QuickTimeImage;
	public static MonoMac.Foundation.NSString QuickTimeMovie;
	public static MonoMac.Foundation.NSString ReferenceURLKey;
	public static MonoMac.Foundation.NSString Resolvable;
	public static MonoMac.Foundation.NSString RTF;
	public static MonoMac.Foundation.NSString RTFD;
	public static MonoMac.Foundation.NSString SourceCode;
	public static MonoMac.Foundation.NSString SymLink;
	public static MonoMac.Foundation.NSString TagClassFilenameExtension;
	public static MonoMac.Foundation.NSString TagClassMIMEType;
	public static MonoMac.Foundation.NSString TagClassNSPboardType;
	public static MonoMac.Foundation.NSString TagClassOSType;
	public static MonoMac.Foundation.NSString TagSpecificationKey;
	public static MonoMac.Foundation.NSString Text;
	public static MonoMac.Foundation.NSString TIFF;
	public static MonoMac.Foundation.NSString TXNTextAndMultimediaData;
	public static MonoMac.Foundation.NSString URL;
	public static MonoMac.Foundation.NSString UTF16ExternalPlainText;
	public static MonoMac.Foundation.NSString UTF16PlainText;
	public static MonoMac.Foundation.NSString UTF8PlainText;
	public static MonoMac.Foundation.NSString VCard;
	public static MonoMac.Foundation.NSString VersionKey;
	public static MonoMac.Foundation.NSString Video;
	public static MonoMac.Foundation.NSString Volume;
	public static MonoMac.Foundation.NSString WebArchive;
	public static MonoMac.Foundation.NSString XML;
```

Added properties:

```
public static MonoMac.Foundation.NSString AliasFile { get; }
	public static MonoMac.Foundation.NSString AliasRecord { get; }
	public static MonoMac.Foundation.NSString AppleICNS { get; }
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Audio { get; }
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Video { get; }
	public static MonoMac.Foundation.NSString AppleScript { get; }
	public static MonoMac.Foundation.NSString Application { get; }
	public static MonoMac.Foundation.NSString ApplicationBundle { get; }
	public static MonoMac.Foundation.NSString ApplicationFile { get; }
	public static MonoMac.Foundation.NSString Archive { get; }
	public static MonoMac.Foundation.NSString AssemblyLanguageSource { get; }
	public static MonoMac.Foundation.NSString Audio { get; }
	public static MonoMac.Foundation.NSString AudioInterchangeFileFormat { get; }
	public static MonoMac.Foundation.NSString AudiovisualContent { get; }
	public static MonoMac.Foundation.NSString AVIMovie { get; }
	public static MonoMac.Foundation.NSString BinaryPropertyList { get; }
	public static MonoMac.Foundation.NSString BMP { get; }
	public static MonoMac.Foundation.NSString Bookmark { get; }
	public static MonoMac.Foundation.NSString Bundle { get; }
	public static MonoMac.Foundation.NSString Bzip2Archive { get; }
	public static MonoMac.Foundation.NSString CalendarEvent { get; }
	public static MonoMac.Foundation.NSString CHeader { get; }
	public static MonoMac.Foundation.NSString CommaSeparatedText { get; }
	public static MonoMac.Foundation.NSString CompositeContent { get; }
	public static MonoMac.Foundation.NSString ConformsToKey { get; }
	public static MonoMac.Foundation.NSString Contact { get; }
	public static MonoMac.Foundation.NSString Content { get; }
	public static MonoMac.Foundation.NSString CPlusPlusHeader { get; }
	public static MonoMac.Foundation.NSString CPlusPlusSource { get; }
	public static MonoMac.Foundation.NSString CSource { get; }
	public static MonoMac.Foundation.NSString Data { get; }
	public static MonoMac.Foundation.NSString Database { get; }
	public static MonoMac.Foundation.NSString DelimitedText { get; }
	public static MonoMac.Foundation.NSString DescriptionKey { get; }
	public static MonoMac.Foundation.NSString Directory { get; }
	public static MonoMac.Foundation.NSString DiskImage { get; }
	public static MonoMac.Foundation.NSString ElectronicPublication { get; }
	public static MonoMac.Foundation.NSString EmailMessage { get; }
	public static MonoMac.Foundation.NSString Executable { get; }
	public static MonoMac.Foundation.NSString ExportedTypeDeclarationsKey { get; }
	public static MonoMac.Foundation.NSString FileURL { get; }
	public static MonoMac.Foundation.NSString FlatRTFD { get; }
	public static MonoMac.Foundation.NSString Folder { get; }
	public static MonoMac.Foundation.NSString Font { get; }
	public static MonoMac.Foundation.NSString Framework { get; }
	public static MonoMac.Foundation.NSString GIF { get; }
	public static MonoMac.Foundation.NSString GNUZipArchive { get; }
	public static MonoMac.Foundation.NSString HTML { get; }
	public static MonoMac.Foundation.NSString ICO { get; }
	public static MonoMac.Foundation.NSString IconFileKey { get; }
	public static MonoMac.Foundation.NSString IdentifierKey { get; }
	public static MonoMac.Foundation.NSString Image { get; }
	public static MonoMac.Foundation.NSString ImportedTypeDeclarationsKey { get; }
	public static MonoMac.Foundation.NSString InkText { get; }
	public static MonoMac.Foundation.NSString InternetLocation { get; }
	public static MonoMac.Foundation.NSString Item { get; }
	public static MonoMac.Foundation.NSString JavaArchive { get; }
	public static MonoMac.Foundation.NSString JavaClass { get; }
	public static MonoMac.Foundation.NSString JavaScript { get; }
	public static MonoMac.Foundation.NSString JavaSource { get; }
	public static MonoMac.Foundation.NSString JPEG { get; }
	public static MonoMac.Foundation.NSString JPEG2000 { get; }
	public static MonoMac.Foundation.NSString JSON { get; }
	public static MonoMac.Foundation.NSString Log { get; }
	public static MonoMac.Foundation.NSString M3UPlaylist { get; }
	public static MonoMac.Foundation.NSString Message { get; }
	public static MonoMac.Foundation.NSString MIDIAudio { get; }
	public static MonoMac.Foundation.NSString MountPoint { get; }
	public static MonoMac.Foundation.NSString Movie { get; }
	public static MonoMac.Foundation.NSString MP3 { get; }
	public static MonoMac.Foundation.NSString MPEG { get; }
	public static MonoMac.Foundation.NSString MPEG2TransportStream { get; }
	public static MonoMac.Foundation.NSString MPEG2Video { get; }
	public static MonoMac.Foundation.NSString MPEG4 { get; }
	public static MonoMac.Foundation.NSString MPEG4Audio { get; }
	public static MonoMac.Foundation.NSString ObjectiveCPlusPlusSource { get; }
	public static MonoMac.Foundation.NSString ObjectiveCSource { get; }
	public static MonoMac.Foundation.NSString OSAScript { get; }
	public static MonoMac.Foundation.NSString OSAScriptBundle { get; }
	public static MonoMac.Foundation.NSString Package { get; }
	public static MonoMac.Foundation.NSString PDF { get; }
	public static MonoMac.Foundation.NSString PerlScript { get; }
	public static MonoMac.Foundation.NSString PHPScript { get; }
	public static MonoMac.Foundation.NSString PICT { get; }
	public static MonoMac.Foundation.NSString PKCS12 { get; }
	public static MonoMac.Foundation.NSString PlainText { get; }
	public static MonoMac.Foundation.NSString Playlist { get; }
	public static MonoMac.Foundation.NSString PluginBundle { get; }
	public static MonoMac.Foundation.NSString PNG { get; }
	public static MonoMac.Foundation.NSString Presentation { get; }
	public static MonoMac.Foundation.NSString PropertyList { get; }
	public static MonoMac.Foundation.NSString PythonScript { get; }
	public static MonoMac.Foundation.NSString QuickLookGenerator { get; }
	public static MonoMac.Foundation.NSString QuickTimeImage { get; }
	public static MonoMac.Foundation.NSString QuickTimeMovie { get; }
	public static MonoMac.Foundation.NSString RawImage { get; }
	public static MonoMac.Foundation.NSString ReferenceURLKey { get; }
	public static MonoMac.Foundation.NSString Resolvable { get; }
	public static MonoMac.Foundation.NSString RTF { get; }
	public static MonoMac.Foundation.NSString RTFD { get; }
	public static MonoMac.Foundation.NSString RubyScript { get; }
	public static MonoMac.Foundation.NSString ScalableVectorGraphics { get; }
	public static MonoMac.Foundation.NSString Script { get; }
	public static MonoMac.Foundation.NSString ShellScript { get; }
	public static MonoMac.Foundation.NSString SourceCode { get; }
	public static MonoMac.Foundation.NSString SpotlightImporter { get; }
	public static MonoMac.Foundation.NSString Spreadsheet { get; }
	public static MonoMac.Foundation.NSString SymLink { get; }
	public static MonoMac.Foundation.NSString SystemPreferencesPane { get; }
	public static MonoMac.Foundation.NSString TabSeparatedText { get; }
	public static MonoMac.Foundation.NSString TagClassFilenameExtension { get; }
	public static MonoMac.Foundation.NSString TagClassMIMEType { get; }
	public static MonoMac.Foundation.NSString TagClassNSPboardType { get; }
	public static MonoMac.Foundation.NSString TagClassOSType { get; }
	public static MonoMac.Foundation.NSString TagSpecificationKey { get; }
	public static MonoMac.Foundation.NSString Text { get; }
	public static MonoMac.Foundation.NSString ThreeDContent { get; }
	public static MonoMac.Foundation.NSString TIFF { get; }
	public static MonoMac.Foundation.NSString ToDoItem { get; }
	public static MonoMac.Foundation.NSString TXNTextAndMultimediaData { get; }
	public static MonoMac.Foundation.NSString UnixExecutable { get; }
	public static MonoMac.Foundation.NSString URL { get; }
	public static MonoMac.Foundation.NSString URLBookmarkData { get; }
	public static MonoMac.Foundation.NSString UTF16ExternalPlainText { get; }
	public static MonoMac.Foundation.NSString UTF16PlainText { get; }
	public static MonoMac.Foundation.NSString UTF8PlainText { get; }
	public static MonoMac.Foundation.NSString UTF8TabSeparatedText { get; }
	public static MonoMac.Foundation.NSString VCard { get; }
	public static MonoMac.Foundation.NSString VersionKey { get; }
	public static MonoMac.Foundation.NSString Video { get; }
	public static MonoMac.Foundation.NSString Volume { get; }
	public static MonoMac.Foundation.NSString WaveformAudio { get; }
	public static MonoMac.Foundation.NSString WebArchive { get; }
	public static MonoMac.Foundation.NSString WindowsExecutable { get; }
	public static MonoMac.Foundation.NSString X509Certificate { get; }
	public static MonoMac.Foundation.NSString XML { get; }
	public static MonoMac.Foundation.NSString XMLPropertyList { get; }
	public static MonoMac.Foundation.NSString XPCService { get; }
	public static MonoMac.Foundation.NSString ZipArchive { get; }
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

## Namespace MonoMac.ObjCRuntime

### Type Changed: MonoMac.ObjCRuntime.Class

Removed method:

```
public static System.IntPtr GetHandleIntrinsic (string name);
```

### Type Changed: MonoMac.ObjCRuntime.Messaging

Removed methods:

```
public static bool bool_objc_msgSend_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2);
	public static bool bool_objc_msgSend_bool_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_CMTimeRange_IntPtr_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_bool_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, System.IntPtr arg8);
	public static bool bool_objc_msgSend_IntPtr_out_Boolean_out_Boolean_out_Boolean_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_SecIdentity_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Security.SecIdentity arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static bool bool_objc_msgSend_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_bool_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_CMTimeRange_IntPtr_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, System.IntPtr arg8);
	public static bool bool_objc_msgSendSuper_IntPtr_out_Boolean_out_Boolean_out_Boolean_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_SecIdentity_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Security.SecIdentity arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, System.IntPtr arg2);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, System.IntPtr arg5);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, System.IntPtr arg5);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_out_Boolean_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_NSPropertyListFormat_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_NSRange_UInt64_IntPtr_int_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_QTTimeRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_QTTime_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_QTTimeRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_out_Boolean_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_NSPropertyListFormat_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_NSRange_UInt64_IntPtr_int_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_QTTimeRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTime_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTimeRange_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, System.IntPtr arg2);
	public static void void_objc_msgSend_IntPtr_int_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSend_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out float arg2, int arg3);
	public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out float arg2, int arg3);
	public static float xamarin_float_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static float xamarin_float_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
```

Added methods:

```
public static void AudioComponentDescriptionNative_objc_msgSend_stret (out MonoMac.AudioUnit.AudioComponentDescriptionNative retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioComponentDescriptionNative_objc_msgSendSuper_stret (out MonoMac.AudioUnit.AudioComponentDescriptionNative retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioStreamBasicDescription_objc_msgSend_stret (out MonoMac.AudioToolbox.AudioStreamBasicDescription retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioStreamBasicDescription_objc_msgSendSuper_stret (out MonoMac.AudioToolbox.AudioStreamBasicDescription retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioTimeStamp_objc_msgSend_stret (out MonoMac.AudioToolbox.AudioTimeStamp retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AudioTimeStamp_objc_msgSendSuper_stret (out MonoMac.AudioToolbox.AudioTimeStamp retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DAngularOrientation_objc_msgSend_stret (out MonoMac.AVFoundation.AVAudio3DAngularOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DAngularOrientation_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVAudio3DAngularOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.AVFoundation.AVAudio3DVectorOrientation AVAudio3DVectorOrientation_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DVectorOrientation_objc_msgSend_stret (out MonoMac.AVFoundation.AVAudio3DVectorOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.AVFoundation.AVAudio3DVectorOrientation AVAudio3DVectorOrientation_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static void AVAudio3DVectorOrientation_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVAudio3DVectorOrientation retval, System.IntPtr receiver, System.IntPtr selector);
	public static bool bool_objc_msgSend_IntPtr_byte_byte_byte_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, byte arg2, byte arg3, byte arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, uint arg4);
	public static bool bool_objc_msgSend_IntPtr_UInt32_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4, uint arg5);
	public static bool bool_objc_msgSend_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_NSOperatingSystemVersion (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSOperatingSystemVersion arg1);
	public static bool bool_objc_msgSend_out_NSURLRelationship_int_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, int arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_out_NSURLRelationship_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_ref_IntPtr_out_Double_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, int arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSend_ref_IntPtr_out_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_byte_byte_byte_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, byte arg2, byte arg3, byte arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, uint arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_UInt32_IntPtr_IntPtr_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4, uint arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_NSOperatingSystemVersion (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSOperatingSystemVersion arg1);
	public static bool bool_objc_msgSendSuper_out_NSURLRelationship_int_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, int arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_out_NSURLRelationship_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, out MonoMac.Foundation.NSURLRelationship arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_Double_int_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, int arg3, System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out double arg2, System.IntPtr arg3);
	public static void CGAffineTransform_objc_msgSend_stret_int (out MonoMac.CoreGraphics.CGAffineTransform retval, System.IntPtr receiver, System.IntPtr selector, int arg1);
	public static void CGAffineTransform_objc_msgSendSuper_stret_int (out MonoMac.CoreGraphics.CGAffineTransform retval, System.IntPtr receiver, System.IntPtr selector, int arg1);
	public static MonoMac.CoreGraphics.CGVector CGVector_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static void CGVector_objc_msgSend_stret (out MonoMac.CoreGraphics.CGVector retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.CoreGraphics.CGVector CGVector_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static void CGVector_objc_msgSendSuper_stret (out MonoMac.CoreGraphics.CGVector retval, System.IntPtr receiver, System.IntPtr selector);
	public static double Double_objc_msgSend_UInt64 (System.IntPtr receiver, System.IntPtr selector, ulong arg1);
	public static double Double_objc_msgSendSuper_UInt64 (System.IntPtr receiver, System.IntPtr selector, ulong arg1);
	public static System.IntPtr IntPtr_objc_msgSend_AudioComponentDescriptionNative (System.IntPtr receiver, System.IntPtr selector, MonoMac.AudioUnit.AudioComponentDescriptionNative arg1);
	public static System.IntPtr IntPtr_objc_msgSend_CATransform3D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreAnimation.CATransform3D arg1);
	public static System.IntPtr IntPtr_objc_msgSend_CGVector_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_out_NSEnergyFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, out MonoMac.Foundation.NSEnergyFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_ref_NSLengthFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSLengthFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_ref_NSMassFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSMassFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSend_Double_UInt32 (System.IntPtr receiver, System.IntPtr selector, double arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSend_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_float_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSend_float_float_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4, bool arg5);
	public static System.IntPtr IntPtr_objc_msgSend_float_PointF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, MonoMac.SceneKit.SCNVector3 arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_float_SizeF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.SizeF arg2);
	public static System.IntPtr IntPtr_objc_msgSend_float_SizeF_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.SizeF arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSend_int_Double (System.IntPtr receiver, System.IntPtr selector, int arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6, int arg7, int arg8);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, System.IntPtr arg4, int arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4);
	public static System.IntPtr IntPtr_objc_msgSend_Int64_Double (System.IntPtr receiver, System.IntPtr selector, long arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, float arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Double_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2, bool arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_float_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_float_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, System.Drawing.SizeF arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, float arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_CGVector (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3, MonoMac.CoreGraphics.CGVector arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.SizeF arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Matrix2 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix2 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Matrix3d (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix3d arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Matrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix4 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_PointF_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.PointF arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNMatrix4_SCNMatrix4_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2, MonoMac.SceneKit.SCNMatrix4 arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3, MonoMac.SceneKit.SCNVector3 arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SCNVector3_SCNVector3_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3, System.IntPtr arg4, MonoMac.SceneKit.SCNVector3 arg5, MonoMac.SceneKit.SCNVector3 arg6);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SizeF_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.SizeF arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_SizeF_UInt32_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, bool arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Vector2 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector2 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Vector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_Vector4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector4 arg2);
	public static System.IntPtr IntPtr_objc_msgSend_PointF_Double (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_PointF_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_PointF_IntPtr_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, float arg3);
	public static System.IntPtr IntPtr_objc_msgSend_PointF_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_RectangleF_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, float arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioStreamBasicDescription (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioStreamBasicDescription_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_AudioTimeStamp_Double (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioTimeStamp arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_PointF_UInt32 (System.IntPtr receiver, System.IntPtr selector, ref System.Drawing.PointF arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector3_SCNVector3_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_SCNVector4_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SizeF_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, float arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SizeF_PointF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SizeF_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, uint arg2);
	public static void IntPtr_objc_msgSend_stret (System.IntPtr retval, System.IntPtr receiver, System.IntPtr selector);
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_Double_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, bool arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_UInt32_Double_UInt32_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, uint arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSend_UInt64_Int64_Double (System.IntPtr receiver, System.IntPtr selector, ulong arg1, long arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSend_Vector4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector4 arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_AudioComponentDescriptionNative (System.IntPtr receiver, System.IntPtr selector, MonoMac.AudioUnit.AudioComponentDescriptionNative arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CATransform3D (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreAnimation.CATransform3D arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CGVector_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr (System.IntPtr receiver, System.IntPtr selector, double arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_out_NSEnergyFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, out MonoMac.Foundation.NSEnergyFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_ref_NSLengthFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSLengthFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_ref_NSMassFormatterUnit (System.IntPtr receiver, System.IntPtr selector, double arg1, ref MonoMac.Foundation.NSMassFormatterUnit arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Double_UInt32 (System.IntPtr receiver, System.IntPtr selector, double arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, double arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_float_float_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_float_float_Double_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, float arg2, float arg3, double arg4, bool arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_PointF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, float arg1, MonoMac.SceneKit.SCNVector3 arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_SizeF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.SizeF arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_SizeF_bool (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.SizeF arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_Double (System.IntPtr receiver, System.IntPtr selector, int arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_int_int_int_int_int_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, int arg4, int arg5, int arg6, int arg7, int arg8);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, int arg3, System.IntPtr arg4, int arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_int (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, int arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Int64_Double (System.IntPtr receiver, System.IntPtr selector, long arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, double arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, bool arg3, float arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double_bool_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, double arg2, bool arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, System.Drawing.SizeF arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_float (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, float arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_CGVector (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3, MonoMac.CoreGraphics.CGVector arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_PointF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_SizeF (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.Drawing.SizeF arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Matrix2 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix2 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Matrix3d (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix3d arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Matrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Matrix4 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.PointF arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNMatrix4_SCNMatrix4_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2, MonoMac.SceneKit.SCNMatrix4 arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_IntPtr_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3, MonoMac.SceneKit.SCNVector3 arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SCNVector3_SCNVector3_IntPtr_SCNVector3_SCNVector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNVector3 arg2, MonoMac.SceneKit.SCNVector3 arg3, System.IntPtr arg4, MonoMac.SceneKit.SCNVector3 arg5, MonoMac.SceneKit.SCNVector3 arg6);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF_bool (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.SizeF arg2, bool arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF_UInt32_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, bool arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Vector2 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector2 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Vector3 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector3 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_Vector4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.OpenGL.Vector4 arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_PointF_Double (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_PointF_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_PointF_IntPtr_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, float arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_PointF_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.IntPtr arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_RectangleF_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.RectangleF arg1, float arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioStreamBasicDescription (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioStreamBasicDescription_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioStreamBasicDescription arg1, System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_AudioTimeStamp_Double (System.IntPtr receiver, System.IntPtr selector, ref MonoMac.AudioToolbox.AudioTimeStamp arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_PointF_UInt32 (System.IntPtr receiver, System.IntPtr selector, ref System.Drawing.PointF arg1, uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector3_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector3_SCNVector3_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SCNVector4_Double (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, double arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SizeF_float (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, float arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SizeF_PointF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SizeF_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, uint arg2);
	public static void IntPtr_objc_msgSendSuper_stret (System.IntPtr retval, System.IntPtr receiver, System.IntPtr selector);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_Double_bool_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, bool arg3, System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt32_Double_UInt32_bool (System.IntPtr receiver, System.IntPtr selector, uint arg1, double arg2, uint arg3, bool arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_UInt64_Int64_Double (System.IntPtr receiver, System.IntPtr selector, ulong arg1, long arg2, double arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_Vector4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector4 arg1);
	public static void Matrix2_objc_msgSend_stret (out MonoMac.OpenGL.Matrix2 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Matrix2_objc_msgSendSuper_stret (out MonoMac.OpenGL.Matrix2 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Matrix3d_objc_msgSend_stret (out MonoMac.OpenGL.Matrix3d retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Matrix3d_objc_msgSendSuper_stret (out MonoMac.OpenGL.Matrix3d retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Matrix4_objc_msgSend_stret (out MonoMac.OpenGL.Matrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Matrix4_objc_msgSendSuper_stret (out MonoMac.OpenGL.Matrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void NSOperatingSystemVersion_objc_msgSend_stret (out MonoMac.Foundation.NSOperatingSystemVersion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void NSOperatingSystemVersion_objc_msgSendSuper_stret (out MonoMac.Foundation.NSOperatingSystemVersion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNMatrix4_objc_msgSend_stret (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNMatrix4_objc_msgSend_stret_SCNMatrix4_IntPtr (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1, System.IntPtr arg2);
	public static void SCNMatrix4_objc_msgSendSuper_stret (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNMatrix4_objc_msgSendSuper_stret_SCNMatrix4_IntPtr (out MonoMac.SceneKit.SCNMatrix4 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1, System.IntPtr arg2);
	public static void SCNQuaternion_objc_msgSend_stret (out MonoMac.SceneKit.SCNQuaternion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNQuaternion_objc_msgSendSuper_stret (out MonoMac.SceneKit.SCNQuaternion retval, System.IntPtr receiver, System.IntPtr selector);
	public static void SCNVector3_objc_msgSend_stret_SCNVector3 (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1);
	public static void SCNVector3_objc_msgSend_stret_SCNVector3_IntPtr (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, System.IntPtr arg2);
	public static void SCNVector3_objc_msgSendSuper_stret_SCNVector3 (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1);
	public static void SCNVector3_objc_msgSendSuper_stret_SCNVector3_IntPtr (out MonoMac.SceneKit.SCNVector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, System.IntPtr arg2);
	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_out_Boolean (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, out bool arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_out_Boolean (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, out bool arg4);
	public static ulong UInt64_objc_msgSend_Double (System.IntPtr receiver, System.IntPtr selector, double arg1);
	public static ulong UInt64_objc_msgSendSuper_Double (System.IntPtr receiver, System.IntPtr selector, double arg1);
	public static MonoMac.OpenGL.Vector2 Vector2_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static void Vector2_objc_msgSend_stret (out MonoMac.OpenGL.Vector2 retval, System.IntPtr receiver, System.IntPtr selector);
	public static MonoMac.OpenGL.Vector2 Vector2_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static void Vector2_objc_msgSendSuper_stret (out MonoMac.OpenGL.Vector2 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Vector3_objc_msgSend_stret (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Vector3_objc_msgSend_stret_Vector3 (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static void Vector3_objc_msgSendSuper_stret (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Vector3_objc_msgSendSuper_stret_Vector3 (out MonoMac.OpenGL.Vector3 retval, System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static void Vector4_objc_msgSend_stret (out MonoMac.OpenGL.Vector4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void Vector4_objc_msgSendSuper_stret (out MonoMac.OpenGL.Vector4 retval, System.IntPtr receiver, System.IntPtr selector);
	public static void void_objc_msgSend_AVAudio3DAngularOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DAngularOrientation arg1);
	public static void void_objc_msgSend_AVAudio3DVectorOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DVectorOrientation arg1);
	public static void void_objc_msgSend_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2);
	public static void void_objc_msgSend_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3);
	public static void void_objc_msgSend_byte_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3, byte arg4);
	public static void void_objc_msgSend_CGVector (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1);
	public static void void_objc_msgSend_CGVector_PointF (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
	public static void void_objc_msgSend_IntPtr_float_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, uint arg3);
	public static void void_objc_msgSend_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_Int64_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4);
	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4, long arg5);
	public static void void_objc_msgSend_IntPtr_IntPtr_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2);
	public static void void_objc_msgSend_Matrix2 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix2 arg1);
	public static void void_objc_msgSend_Matrix3d (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix3d arg1);
	public static void void_objc_msgSend_Matrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix4 arg1);
	public static void void_objc_msgSend_out_Int32_out_Int32_out_Int32_out_Int32_IntPtr (System.IntPtr receiver, System.IntPtr selector, out int arg1, out int arg2, out int arg3, out int arg4, System.IntPtr arg5);
	public static void void_objc_msgSend_PointF_PointF_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2, System.IntPtr arg3);
	public static void void_objc_msgSend_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static void void_objc_msgSend_SCNQuaternion (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNQuaternion arg1);
	public static void void_objc_msgSend_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, bool arg2);
	public static void void_objc_msgSend_SCNVector3_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, bool arg3);
	public static void void_objc_msgSend_SCNVector4_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, bool arg2);
	public static void void_objc_msgSend_UInt16_byte (System.IntPtr receiver, System.IntPtr selector, ushort arg1, byte arg2);
	public static void void_objc_msgSend_UInt32_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static void void_objc_msgSend_UInt32_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_Vector2 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector2 arg1);
	public static void void_objc_msgSend_Vector3 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static void void_objc_msgSend_Vector4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector4 arg1);
	public static void void_objc_msgSendSuper_AVAudio3DAngularOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DAngularOrientation arg1);
	public static void void_objc_msgSendSuper_AVAudio3DVectorOrientation (System.IntPtr receiver, System.IntPtr selector, MonoMac.AVFoundation.AVAudio3DVectorOrientation arg1);
	public static void void_objc_msgSendSuper_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2);
	public static void void_objc_msgSendSuper_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3);
	public static void void_objc_msgSendSuper_byte_byte_byte_byte (System.IntPtr receiver, System.IntPtr selector, byte arg1, byte arg2, byte arg3, byte arg4);
	public static void void_objc_msgSendSuper_CGVector (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1);
	public static void void_objc_msgSendSuper_CGVector_PointF (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
	public static void void_objc_msgSendSuper_IntPtr_float_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, float arg2, uint arg3);
	public static void void_objc_msgSendSuper_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_Int64_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, long arg2, uint arg3, System.IntPtr arg4, System.IntPtr arg5);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64_Int64 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, long arg3, long arg4, long arg5);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_UInt32_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.SceneKit.SCNMatrix4 arg2);
	public static void void_objc_msgSendSuper_Matrix2 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix2 arg1);
	public static void void_objc_msgSendSuper_Matrix3d (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix3d arg1);
	public static void void_objc_msgSendSuper_Matrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Matrix4 arg1);
	public static void void_objc_msgSendSuper_out_Int32_out_Int32_out_Int32_out_Int32_IntPtr (System.IntPtr receiver, System.IntPtr selector, out int arg1, out int arg2, out int arg3, out int arg4, System.IntPtr arg5);
	public static void void_objc_msgSendSuper_PointF_PointF_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2, System.IntPtr arg3);
	public static void void_objc_msgSendSuper_SCNMatrix4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNMatrix4 arg1);
	public static void void_objc_msgSendSuper_SCNQuaternion (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNQuaternion arg1);
	public static void void_objc_msgSendSuper_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, bool arg2);
	public static void void_objc_msgSendSuper_SCNVector3_SCNVector3_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector3 arg1, MonoMac.SceneKit.SCNVector3 arg2, bool arg3);
	public static void void_objc_msgSendSuper_SCNVector4_bool (System.IntPtr receiver, System.IntPtr selector, MonoMac.SceneKit.SCNVector4 arg1, bool arg2);
	public static void void_objc_msgSendSuper_UInt16_byte (System.IntPtr receiver, System.IntPtr selector, ushort arg1, byte arg2);
	public static void void_objc_msgSendSuper_UInt32_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static void void_objc_msgSendSuper_UInt32_UInt32_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, uint arg2, System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_Vector2 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector2 arg1);
	public static void void_objc_msgSendSuper_Vector3 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector3 arg1);
	public static void void_objc_msgSendSuper_Vector4 (System.IntPtr receiver, System.IntPtr selector, MonoMac.OpenGL.Vector4 arg1);
```

### Type Changed: MonoMac.ObjCRuntime.PlatformHelper

Removed method:

```
public static bool Is64BitOnlyOnCurrentPlatform (Platform platform);
```

## Namespace MonoMac.OpenGL

### Type Changed: MonoMac.OpenGL.MathHelper

Added fields:

```
public static double DTOR;
	public static float DTORF;
```

### New Type MonoMac.OpenGL.Matrix3d

```
[Serializable]
public struct Matrix3d, System.IEquatable<Matrix3d> {
	// constructors
	public Matrix3d (ref Matrix3d matrix);
	public Matrix3d (double r0c0, double r0c1, double r0c2, double r1c0, double r1c1, double r1c2, double r2c0, double r2c1, double r2c2);
	public Matrix3d (double[] doubleArray);
	public Matrix3d (Quaterniond quaternion);
	// fields
	public static Matrix3d Identity;
	public double R0C0;
	public double R0C1;
	public double R0C2;
	public double R1C0;
	public double R1C1;
	public double R1C2;
	public double R2C0;
	public double R2C1;
	public double R2C2;
	public static Matrix3d Zero;
	// properties
	public double Determinant { get; }
	public double Item { get; set; }
	public double Item { get; set; }
	// methods
	public static void Add (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public void Add (ref Matrix3d matrix, out Matrix3d result);
	public void Add (ref Matrix3d matrix);
	public static bool Equals (ref Matrix3d left, ref Matrix3d right);
	public virtual bool Equals (Matrix3d matrix);
	public bool Equals (ref Matrix3d matrix);
	public bool EqualsApprox (ref Matrix3d matrix, double tolerance);
	public static bool EqualsApprox (ref Matrix3d left, ref Matrix3d right, double tolerance);
	public override int GetHashCode ();
	public void Multiply (double scalar);
	public void Multiply (ref Matrix3d matrix);
	public void Multiply (double scalar, out Matrix3d result);
	public static void Multiply (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public static void Multiply (ref Matrix3d matrix, double scalar, out Matrix3d result);
	public void Multiply (ref Matrix3d matrix, out Matrix3d result);
	public static System.IntPtr op_Explicit (Matrix3d matrix);
	public static double* op_Explicit (Matrix3d matrix);
	public static double[] op_Explicit (Matrix3d matrix);
	public void Rotate (double angle);
	public void Rotate (double angle, out Matrix3d result);
	public static void Rotate (ref Matrix3d matrix, double angle, out Matrix3d result);
	public static void RotateMatrix (double angle, out Matrix3d result);
	public void Subtract (ref Matrix3d matrix);
	public static void Subtract (ref Matrix3d left, ref Matrix3d right, out Matrix3d result);
	public void Subtract (ref Matrix3d matrix, out Matrix3d result);
	public override string ToString ();
	public void Transform (ref Vector3d vector, out Vector3d result);
	public static void Transform (ref Matrix3d matrix, ref Vector3d vector);
	public static void Transform (ref Matrix3d matrix, ref Vector3d vector, out Vector3d result);
	public void Transform (ref Vector3d vector);
	public static void Transpose (ref Matrix3d matrix, out Matrix3d result);
	public void Transpose (out Matrix3d result);
	public void Transpose ();
}
```

## Namespace MonoMac.SceneKit

### Type Changed: MonoMac.SceneKit.SCNBox

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNCamera

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
```

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ProjectionTransform { get; set; }
```

Added properties:

```
public virtual float Aperture { get; set; }
	public virtual bool AutomaticallyAdjustsZRange { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float FocalBlurRadius { get; set; }
	public virtual float FocalDistance { get; set; }
	public virtual float FocalSize { get; set; }
	public virtual double OrthographicScale { get; set; }
	public virtual SCNMatrix4 ProjectionTransform { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNCapsule

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNCone

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNConstraint

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
```

Added property:

```
public virtual float InfluenceFactor { get; set; }
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNCylinder

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNFloor

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added property:

```
public virtual float ReflectionResolutionScaleFactor { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNGeometry

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added properties:

```
public virtual SCNGeometryElement EdgeCreasesElement { get; set; }
	public virtual SCNGeometrySource EdgeCreasesSource { get; set; }
	public virtual SCNLevelOfDetail[] LevelsOfDetail { get; set; }
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual uint SubdivisionLevel { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public static SCNGeometry Create ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNGeometryElement

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.SceneKit.SCNGeometrySource

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.SceneKit.SCNGeometrySourceSemantic

Added properties:

```
public static MonoMac.Foundation.NSString EdgeCrease { get; }
	public static MonoMac.Foundation.NSString VertexCrease { get; }
```

### Type Changed: MonoMac.SceneKit.SCNHitTest

Removed property:

```
public static MonoMac.Foundation.NSString IgnoreHiddenNodes { get; }
```

Added property:

```
public static MonoMac.Foundation.NSString IgnoreHiddenNodesKey { get; }
```

### Type Changed: MonoMac.SceneKit.SCNHitTestResult

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ModelTransform { get; }
```

Added property:

```
public virtual SCNMatrix4 ModelTransform { get; }
```

### Type Changed: MonoMac.SceneKit.SCNLayer

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
```

Added properties:

```
public virtual MonoMac.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNLevelOfDetail

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

### Type Changed: MonoMac.SceneKit.SCNLight

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
```

Removed property:

```
public virtual string LightType { get; set; }
```

Added properties:

```
public virtual float AttenuationEndDistance { get; set; }
	public virtual float AttenuationFalloffExponent { get; set; }
	public virtual float AttenuationStartDistance { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual SCNMaterialProperty Gobo { get; }
	public virtual MonoMac.Foundation.NSString LightType { get; set; }
	public virtual float OrthographicScale { get; set; }
	public virtual float ShadowBias { get; set; }
	public virtual System.Drawing.SizeF ShadowMapSize { get; set; }
	public virtual SCNShadowMode ShadowMode { get; set; }
	public virtual uint ShadowSampleCount { get; set; }
	public virtual float SpotInnerAngle { get; set; }
	public virtual float SpotOuterAngle { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual float ZFar { get; set; }
	public virtual float ZNear { get; set; }
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNLookAtConstraint

Removed constructor:

```
public SCNLookAtConstraint ();
```

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
```

### Type Changed: MonoMac.SceneKit.SCNMaterial

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNShadable
```

Added properties:

```
public virtual float FresnelExponent { get; set; }
	public virtual bool ReadsFromDepthBuffer { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNMaterialProperty

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
```

Removed property:

```
public virtual MonoMac.CoreAnimation.CATransform3D ContentsTransform { get; set; }
```

Added properties:

```
public MonoMac.AppKit.NSColor ContentColor { get; set; }
	public MonoMac.AppKit.NSImage ContentImage { get; set; }
	public MonoMac.AppKit.NSImage[] ContentImageCube { get; set; }
	public MonoMac.CoreAnimation.CALayer ContentLayer { get; set; }
	public MonoMac.Foundation.NSString ContentPath { get; set; }
	public MonoMac.SpriteKit.SKScene ContentScene { get; set; }
	public virtual SCNMatrix4 ContentsTransform { get; set; }
	public MonoMac.SpriteKit.SKTexture ContentTexture { get; set; }
	public MonoMac.Foundation.NSUrl ContentUrl { get; set; }
	public virtual float Intensity { get; set; }
	public virtual float MaxAnisotropy { get; set; }
```

Added methods:

```
public static SCNMaterialProperty Create (MonoMac.Foundation.NSObject contents);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNMorpher

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
```

Added methods:

```
public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
```

### Type Changed: MonoMac.SceneKit.SCNNode

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNActionable
	ISCNAnimatable
	ISCNBoundingVolume
```

Removed properties:

```
public virtual MonoMac.CoreAnimation.CATransform3D Pivot { get; set; }
	public virtual MonoMac.CoreAnimation.CATransform3D Transform { get; set; }
	public virtual MonoMac.CoreAnimation.CATransform3D WorldTransform { get; }
```

Added properties:

```
public virtual bool CastsShadow { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual SCNConstraint[] Constraints { get; set; }
	public virtual SCNVector3 EulerAngles { get; set; }
	public virtual MonoMac.CoreImage.CIFilter[] Filters { get; set; }
	public virtual SCNMorpher Morpher { get; set; }
	public virtual SCNQuaternion Orientation { get; set; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsBody PhysicsBody { get; set; }
	public virtual SCNPhysicsField PhysicsField { get; set; }
	public virtual SCNMatrix4 Pivot { get; set; }
	public virtual SCNSkinner Skinner { get; set; }
	public virtual SCNMatrix4 Transform { get; set; }
	public virtual SCNMatrix4 WorldTransform { get; }
```

Removed method:

```
public virtual SCNNode FindNodes (SCNNodePredicate predicate);
```

Added methods:

```
public void AddNodes (SCNNode[] nodes);
	public virtual void AddParticleSystem (SCNParticleSystem system);
	public virtual SCNVector3 ConvertPositionFromNode (SCNVector3 position, SCNNode node);
	public virtual SCNVector3 ConvertPositionToNode (SCNVector3 position, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformFromNode (SCNMatrix4 transform, SCNNode node);
	public virtual SCNMatrix4 ConvertTransformToNode (SCNMatrix4 transform, SCNNode node);
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);
	public virtual SCNNode[] FindNodes (SCNNodePredicate predicate);
	public virtual SCNNode FlattenedClone ();
	public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public virtual SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, MonoMac.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, SCNHitTestOptions options);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, string key);
```

### Type Changed: MonoMac.SceneKit.SCNNodeRendererDelegate

Added interface:

```
ISCNNodeRendererDelegate
```

### Type Changed: MonoMac.SceneKit.SCNPlane

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added properties:

```
public virtual float CornerRadius { get; set; }
	public virtual int CornerSegmentCount { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNProgram

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

Added properties:

```
public static MonoMac.Foundation.NSString MappingChannelKey { get; }
	public virtual bool Opaque { get; set; }
```

Added method:

```
public void SetSemantic (MonoMac.Foundation.NSString geometrySourceSemantic, string symbol, SCNProgramSemanticOptions options);
```

### Type Changed: MonoMac.SceneKit.SCNProgramDelegate

Added interface:

```
ISCNProgramDelegate
```

### Type Changed: MonoMac.SceneKit.SCNPyramid

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNRenderer

Removed constructor:

```
public SCNRenderer ();
```

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
```

Added properties:

```
public virtual double NextFrameTimeInSeconds { get; }
	public virtual MonoMac.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual void Render (double timeInSeconds);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNScene

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

Added properties:

```
public virtual SCNMaterialProperty Background { get; }
	public static MonoMac.Foundation.NSString EndTimeAttributeKey { get; }
	public virtual MonoMac.Foundation.NSObject FogColor { get; set; }
	public virtual float FogDensityExponent { get; set; }
	public virtual float FogEndDistance { get; set; }
	public virtual float FogStartDistance { get; set; }
	public static MonoMac.Foundation.NSString FrameRateAttributeKey { get; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsWorld PhysicsWorld { get; }
	public static MonoMac.Foundation.NSString StartTimeAttributeKey { get; }
	public static MonoMac.Foundation.NSString UpAxisAttributeKey { get; }
```

Added methods:

```
public virtual void AddParticleSystem (SCNParticleSystem system, SCNMatrix4 transform);
	public static SCNScene FromFile (string name, string directory, SCNSceneLoadingOptions options);
	public static SCNScene FromFile (string name, string directory, MonoMac.Foundation.NSDictionary options);
	public static SCNScene FromFile (string name);
	public static SCNScene FromUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options, out MonoMac.Foundation.NSError error);
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual bool WriteToUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
	public bool WriteToUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
```

### Type Changed: MonoMac.SceneKit.SCNSceneRendererDelegate

Added interface:

```
ISCNSceneRendererDelegate
```

Removed methods:

```
public virtual void DidRenderScene (MonoMac.Foundation.NSObject renderer, SCNScene scene, double time);
	public virtual void WillRenderScene (MonoMac.Foundation.NSObject renderer, SCNScene scene, double time);
```

Added methods:

```
public virtual void DidApplyAnimations (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

### Type Changed: MonoMac.SceneKit.SCNSceneSource

Added constructors:

```
public SCNSceneSource (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNSceneSource (MonoMac.Foundation.NSData data, SCNSceneLoadingOptions options);
```

Removed method:

```
public static MonoMac.Foundation.NSObject FromData (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options);
```

Added methods:

```
public virtual MonoMac.Foundation.NSObject[] EntriesPassingTest (SCNSceneSourceFilter predicate);
	public static SCNSceneSource FromData (MonoMac.Foundation.NSData data, SCNSceneLoadingOptions options);
	public static SCNSceneSource FromData (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options);
	public SCNSceneSource FromUrl (MonoMac.Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNScene SceneFromOptions (SCNSceneLoadingOptions options, SCNSceneSourceStatusHandler statusHandler);
	public SCNScene SceneWithOption (SCNSceneLoadingOptions options, out MonoMac.Foundation.NSError error);
```

### Type Changed: MonoMac.SceneKit.SCNSceneSourceLoading

Removed properties:

```
public static MonoMac.Foundation.NSString AssetDirectoryURLsKey { get; }
	public static MonoMac.Foundation.NSString OverrideAssetURLsKey { get; }
```

Added properties:

```
public static MonoMac.Foundation.NSString AnimationImportPolicyDoNotPlay { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyKey { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlay { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlayRepeatedly { get; }
	public static MonoMac.Foundation.NSString AnimationImportPolicyPlayUsingSceneTimeBase { get; }
	public static MonoMac.Foundation.NSString AssetDirectoryUrlsKey { get; }
	public static MonoMac.Foundation.NSString ConvertToYUpKey { get; }
	public static MonoMac.Foundation.NSString ConvertUnitsToMetersKey { get; }
	public static MonoMac.Foundation.NSString OverrideAssetUrlsKey { get; }
```

### Type Changed: MonoMac.SceneKit.SCNShaderModifiers

Added constructors:

```
public SCNShaderModifiers ();
	public SCNShaderModifiers (MonoMac.Foundation.NSDictionary dictionary);
```

Removed properties:

```
public static MonoMac.Foundation.NSString EntryPointFragment { get; }
	public static MonoMac.Foundation.NSString EntryPointGeometry { get; }
	public static MonoMac.Foundation.NSString EntryPointLightingModel { get; }
	public static MonoMac.Foundation.NSString EntryPointSurface { get; }
```

Added properties:

```
public string EntryPointFragment { get; set; }
	public string EntryPointGeometry { get; set; }
	public string EntryPointLightingModel { get; set; }
	public string EntryPointSurface { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNShape

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNSkinner

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
```

Added properties:

```
public virtual SCNGeometry BaseGeometry { get; set; }
	public virtual SCNMatrix4 BaseGeometryBindTransform { get; set; }
	public virtual SCNGeometrySource BoneIndices { get; }
	public SCNMatrix4[] BoneInverseBindTransforms { get; }
	public virtual SCNNode[] Bones { get; }
	public virtual SCNGeometrySource BoneWeights { get; }
```

Added method:

```
public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, SCNMatrix4[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
```

### Type Changed: MonoMac.SceneKit.SCNSphere

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNText

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added properties:

```
public virtual MonoMac.AppKit.NSBezierPath ChamferProfile { get; set; }
	public virtual float Flatness { get; set; }
```

### Type Changed: MonoMac.SceneKit.SCNTorus

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNTransformConstraint

Removed constructor:

```
public SCNTransformConstraint ();
```

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
```

### Type Changed: MonoMac.SceneKit.SCNTransformConstraintHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform, System.AsyncCallback callback, object object);
	public virtual MonoMac.CoreAnimation.CATransform3D EndInvoke (System.IAsyncResult result);
	public virtual MonoMac.CoreAnimation.CATransform3D Invoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, SCNMatrix4 transform, System.AsyncCallback callback, object object);
	public virtual SCNMatrix4 EndInvoke (System.IAsyncResult result);
	public virtual SCNMatrix4 Invoke (SCNNode node, SCNMatrix4 transform);
```

### Type Changed: MonoMac.SceneKit.SCNTube

Added interfaces:

```
MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: MonoMac.SceneKit.SCNVector3

Removed constructor:

```
public SCNVector3 (MonoMac.OpenGL.Vector3 vector);
```

Added constructors:

```
public SCNVector3 (MonoMac.OpenGL.Vector3 v);
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
	public MonoMac.OpenGL.Vector2 Xy { get; set; }
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

### Type Changed: MonoMac.SceneKit.SCNVector4

Removed constructor:

```
public SCNVector4 (MonoMac.OpenGL.Vector4 vector);
```

Added constructors:

```
public SCNVector4 (MonoMac.OpenGL.Vector2 v);
	public SCNVector4 (SCNVector3 v);
	public SCNVector4 (MonoMac.OpenGL.Vector3 v);
	public SCNVector4 (MonoMac.OpenGL.Vector4 v);
	public SCNVector4 (SCNVector3 v, float w);
	public SCNVector4 (SCNVector4 v);
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
	public MonoMac.OpenGL.Vector2 Xy { get; set; }
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

### Type Changed: MonoMac.SceneKit.SCNView

Added interface:

```
ISCNSceneRenderer
```

Added properties:

```
public virtual SCNAntialiasingMode AntialiasingMode { get; set; }
	public virtual MonoMac.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual MonoMac.AppKit.NSImage Snapshot ();
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: MonoMac.SceneKit.SCNWrapMode

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

### New Type MonoMac.SceneKit._SCNShaderModifiers

```
public static class _SCNShaderModifiers {
}
```

### New Type MonoMac.SceneKit.ISCNActionable

```
public interface ISCNActionable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNAnimatable

```
public interface ISCNAnimatable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNBoundingVolume

```
public interface ISCNBoundingVolume : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNNodeRendererDelegate

```
public interface ISCNNodeRendererDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNPhysicsContactDelegate

```
public interface ISCNPhysicsContactDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNProgramDelegate

```
public interface ISCNProgramDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNSceneExportDelegate

```
public interface ISCNSceneExportDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNSceneRenderer

```
public interface ISCNSceneRenderer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
}
```

### New Type MonoMac.SceneKit.ISCNSceneRendererDelegate

```
public interface ISCNSceneRendererDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNShadable

```
public interface ISCNShadable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SceneKit.ISCNTechniqueSupport

```
public interface ISCNTechniqueSupport : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNAction

```
public class SCNAction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAction ();
	public SCNAction (MonoMac.Foundation.NSCoder coder);
	public SCNAction (MonoMac.Foundation.NSObjectFlag t);
	public SCNAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DurationInSeconds { get; set; }
	public virtual float Speed { get; set; }
	public virtual SCNActionTimingMode TimingMode { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
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
	public static SCNAction Run (System.Action<SCNNode> handler, MonoMac.CoreFoundation.DispatchQueue queue);
	public static SCNAction Run (System.Action<SCNNode> handler);
	public static SCNAction ScaleBy (float scale, double durationInSeconds);
	public static SCNAction ScaleTo (float scale, double durationInSeconds);
	public static SCNAction Sequence (SCNAction[] actions);
	public virtual void SetTimingFunction (System.Action<float> timingFunction);
	public static SCNAction Wait (double durationInSeconds);
	public static SCNAction Wait (double durationInSeconds, double durationRange);
}
```

### New Type MonoMac.SceneKit.SCNActionable

```
public class SCNActionable : MonoMac.Foundation.NSObject, ISCNActionable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNActionable ();
	public SCNActionable (MonoMac.Foundation.NSCoder coder);
	public SCNActionable (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNActionable_Extensions

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

### New Type MonoMac.SceneKit.SCNActionNodeWithElapsedTimeHandler

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

### New Type MonoMac.SceneKit.SCNActionTimingMode

```
[Serializable]
public enum SCNActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type MonoMac.SceneKit.SCNAnimatable

```
public class SCNAnimatable : MonoMac.Foundation.NSObject, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAnimatable ();
	public SCNAnimatable (MonoMac.Foundation.NSCoder coder);
	public SCNAnimatable (MonoMac.Foundation.NSObjectFlag t);
	public SCNAnimatable (System.IntPtr handle);
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNAnimatable_Extensions

```
public static class SCNAnimatable_Extensions {
	// methods
	public static void AddAnimation (ISCNAnimatable This, MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public static MonoMac.CoreAnimation.CAAnimation GetAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static MonoMac.Foundation.NSString[] GetAnimationKeys (ISCNAnimatable This);
	public static bool IsAnimationPaused (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void PauseAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void RemoveAllAnimations (ISCNAnimatable This);
	public static void RemoveAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
	public static void RemoveAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key, float duration);
	public static void ResumeAnimation (ISCNAnimatable This, MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNAntialiasingMode

```
[Serializable]
public enum SCNAntialiasingMode {
	Multisampling16X = 4,
	Multisampling2X = 1,
	Multisampling4X = 2,
	Multisampling8X = 3,
	None = 0,
}
```

### New Type MonoMac.SceneKit.SCNBindingHandler

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

### New Type MonoMac.SceneKit.SCNBoundingVolume

```
public class SCNBoundingVolume : MonoMac.Foundation.NSObject, ISCNBoundingVolume, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNBoundingVolume ();
	public SCNBoundingVolume (MonoMac.Foundation.NSCoder coder);
	public SCNBoundingVolume (MonoMac.Foundation.NSObjectFlag t);
	public SCNBoundingVolume (System.IntPtr handle);
	// methods
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
}
```

### New Type MonoMac.SceneKit.SCNBoundingVolume_Extensions

```
public static class SCNBoundingVolume_Extensions {
	// methods
	public static bool GetBoundingBox (ISCNBoundingVolume This, ref SCNVector3 min, ref SCNVector3 max);
	public static bool GetBoundingSphere (ISCNBoundingVolume This, ref SCNVector3 center, ref float radius);
}
```

### New Type MonoMac.SceneKit.SCNFieldForceEvaluator

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

### New Type MonoMac.SceneKit.SCNHitTestOptions

```
public class SCNHitTestOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNHitTestOptions ();
	public SCNHitTestOptions (MonoMac.Foundation.NSDictionary dictionary);
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

### New Type MonoMac.SceneKit.SCNIKConstraint

```
public class SCNIKConstraint : MonoMac.SceneKit.SCNConstraint, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNIKConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNIKConstraint (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNJavaScript

```
public static class SCNJavaScript {
	// methods
	public static void ExportModule (MonoMac.JavaScriptCore.JSContext context);
}
```

### New Type MonoMac.SceneKit.SCNMatrix4

```
[Serializable]
public struct SCNMatrix4, System.IEquatable<SCNMatrix4> {
	// constructors
	public SCNMatrix4 (SCNVector4 row0, SCNVector4 row1, SCNVector4 row2, SCNVector4 row3);
	public SCNMatrix4 (float m00, float m01, float m02, float m03, float m10, float m11, float m12, float m13, float m20, float m21, float m22, float m23, float m30, float m31, float m32, float m33);
	public SCNMatrix4 (MonoMac.CoreAnimation.CATransform3D transform);
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
	public static void CreateFromAxisAngle (MonoMac.OpenGL.Vector3d axis, double angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateFromAxisAngle (SCNVector3 axis, float angle);
	public static void CreateFromAxisAngle (SCNVector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateFromAxisAngle (MonoMac.OpenGL.Vector3 axis, float angle, out SCNMatrix4 result);
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
	public static SCNMatrix4 Rotate (MonoMac.OpenGL.Quaternion q);
	public static SCNMatrix4 Rotate (MonoMac.OpenGL.Quaterniond q);

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

### New Type MonoMac.SceneKit.SCNNodeRendererDelegate_Extensions

```
public static class SCNNodeRendererDelegate_Extensions {
	// methods
	public static void Render (ISCNNodeRendererDelegate This, SCNNode node, SCNRenderer renderer, MonoMac.Foundation.NSDictionary arguments);
}
```

### New Type MonoMac.SceneKit.SCNParticleBirthDirection

```
[Serializable]
public enum SCNParticleBirthDirection {
	Constant = 0,
	Random = 2,
	SurfaceNormal = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleBirthLocation

```
[Serializable]
public enum SCNParticleBirthLocation {
	Surface = 0,
	Vertex = 2,
	Volume = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleBlendMode

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

### New Type MonoMac.SceneKit.SCNParticleEvent

```
[Serializable]
public enum SCNParticleEvent {
	Birth = 0,
	Collision = 2,
	Death = 1,
}
```

### New Type MonoMac.SceneKit.SCNParticleEventHandler

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

### New Type MonoMac.SceneKit.SCNParticleImageSequenceAnimationMode

```
[Serializable]
public enum SCNParticleImageSequenceAnimationMode {
	AutoReverse = 2,
	Clamp = 1,
	Repeat = 0,
}
```

### New Type MonoMac.SceneKit.SCNParticleInputMode

```
[Serializable]
public enum SCNParticleInputMode {
	OverDistance = 1,
	OverLife = 0,
	OverOtherProperty = 2,
}
```

### New Type MonoMac.SceneKit.SCNParticleModifierHandler

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

### New Type MonoMac.SceneKit.SCNParticleModifierStage

```
[Serializable]
public enum SCNParticleModifierStage {
	PostCollision = 3,
	PostDynamics = 1,
	PreCollision = 2,
	PreDynamics = 0,
}
```

### New Type MonoMac.SceneKit.SCNParticleOrientationMode

```
[Serializable]
public enum SCNParticleOrientationMode {
	BillboardScreenAligned = 0,
	BillboardViewAligned = 1,
	BillboardYAligned = 3,
	Free = 2,
}
```

### New Type MonoMac.SceneKit.SCNParticlePropertyController

```
public class SCNParticlePropertyController : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticlePropertyController (MonoMac.Foundation.NSCoder coder);
	public SCNParticlePropertyController (MonoMac.Foundation.NSObjectFlag t);
	public SCNParticlePropertyController (System.IntPtr handle);
	// properties
	public virtual MonoMac.CoreAnimation.CAAnimation Animation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float InputBias { get; set; }
	public virtual SCNParticleInputMode InputMode { get; set; }
	public virtual SCNNode InputOrigin { get; set; }
	public virtual MonoMac.Foundation.NSString InputProperty { get; set; }
	public virtual float InputScale { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNParticlePropertyController Create (MonoMac.CoreAnimation.CAAnimation animation);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNParticleSortingMode

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

### New Type MonoMac.SceneKit.SCNParticleSystem

```
public class SCNParticleSystem : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticleSystem (MonoMac.Foundation.NSCoder coder);
	public SCNParticleSystem (MonoMac.Foundation.NSObjectFlag t);
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
	public virtual MonoMac.AppKit.NSColor ParticleColor { get; set; }
	public virtual SCNVector4 ParticleColorVariation { get; set; }
	public virtual bool ParticleDiesOnCollision { get; set; }
	public virtual float ParticleFriction { get; set; }
	public virtual float ParticleFrictionVariation { get; set; }
	public virtual MonoMac.Foundation.NSObject ParticleImage { get; set; }
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
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual void AddModifier (MonoMac.Foundation.NSString[] properties, SCNParticleModifierStage stage, SCNParticleModifierHandler handler);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNParticleSystem Create ();
	public static SCNParticleSystem Create (string name, string directory);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleEvent (SCNParticleEvent evnt, MonoMac.Foundation.NSString[] properties, SCNParticleEventHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAllModifiers ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void RemoveModifiers (SCNParticleModifierStage stage);
	public virtual void Reset ();
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBallSocketJoint

```
public class SCNPhysicsBallSocketJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBallSocketJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBallSocketJoint (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNPhysicsBehavior

```
public class SCNPhysicsBehavior : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBehavior (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBehavior (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsBehavior (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBody

```
public class SCNPhysicsBody : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBody (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsBody (MonoMac.Foundation.NSObjectFlag t);
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
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsBody CreateBody (SCNPhysicsBodyType type, SCNPhysicsShape shape);
	public static SCNPhysicsBody CreateDynamicBody ();
	public static SCNPhysicsBody CreateKinematicBody ();
	public static SCNPhysicsBody CreateStaticBody ();
	protected override void Dispose (bool disposing);
	public virtual void ResetTransform ();
}
```

### New Type MonoMac.SceneKit.SCNPhysicsBodyType

```
[Serializable]
public enum SCNPhysicsBodyType {
	Dynamic = 1,
	Kinematic = 2,
	Static = 0,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContact

```
public class SCNPhysicsContact : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContact (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsContact (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNPhysicsContactDelegate

```
public class SCNPhysicsContactDelegate : MonoMac.Foundation.NSObject, ISCNPhysicsContactDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContactDelegate ();
	public SCNPhysicsContactDelegate (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsContactDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidEndContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidUpdateContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContactDelegate_Extensions

```
public static class SCNPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidEndContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidUpdateContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsContactEventArgs

```
public class SCNPhysicsContactEventArgs : System.EventArgs {
	// constructors
	public SCNPhysicsContactEventArgs (SCNPhysicsContact contact);
	// properties
	public SCNPhysicsContact Contact { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsField

```
public class SCNPhysicsField : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsField (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsField (MonoMac.Foundation.NSObjectFlag t);
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
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
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

### New Type MonoMac.SceneKit.SCNPhysicsFieldScope

```
[Serializable]
public enum SCNPhysicsFieldScope {
	InsideExtent = 0,
	OutsideExtent = 1,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsHingeJoint

```
public class SCNPhysicsHingeJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsHingeJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsHingeJoint (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNPhysicsSearchMode

```
[Serializable]
public enum SCNPhysicsSearchMode {
	All = 2,
	Any = 0,
	Closest = 1,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShape

```
public class SCNPhysicsShape : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsShape (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsShape (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsShape (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeOptions options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNPhysicsShape[] shapes, SCNVector3[] transforms);
	public static SCNPhysicsShape Create (SCNNode node, MonoMac.Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, MonoMac.Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeOptions options);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptions

```
public class SCNPhysicsShapeOptions {
	// constructors
	public SCNPhysicsShapeOptions ();
	// properties
	public bool? KeepAsCompound { get; set; }
	public SCNVector3? Scale { get; set; }
	public SCNPhysicsShapeType? ShapeType { get; set; }
	// methods
	public MonoMac.Foundation.NSDictionary ToDictionary ();
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptionsKeys

```
public static class SCNPhysicsShapeOptionsKeys {
	// properties
	public static MonoMac.Foundation.NSString KeepAsCompound { get; }
	public static MonoMac.Foundation.NSString Scale { get; }
	public static MonoMac.Foundation.NSString Type { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeOptionsTypes

```
public static class SCNPhysicsShapeOptionsTypes {
	// properties
	public static MonoMac.Foundation.NSString BoundingBox { get; }
	public static MonoMac.Foundation.NSString ConcavePolyhedron { get; }
	public static MonoMac.Foundation.NSString ConvexHull { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsShapeType

```
[Serializable]
public enum SCNPhysicsShapeType {
	BoundingBox = 1,
	ConcavePolyhedron = 2,
	ConvexHull = 0,
}
```

### New Type MonoMac.SceneKit.SCNPhysicsSliderJoint

```
public class SCNPhysicsSliderJoint : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsSliderJoint (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsSliderJoint (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNPhysicsTest

```
public class SCNPhysicsTest : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNPhysicsTest ();
	public SCNPhysicsTest (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public uint? CollisionBitMask { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsTestKeys

```
public static class SCNPhysicsTestKeys {
	// properties
	public static MonoMac.Foundation.NSString CollisionBitMaskKey { get; }
	public static MonoMac.Foundation.NSString SearchModeKey { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsTestSearchModeKeys

```
public static class SCNPhysicsTestSearchModeKeys {
	// properties
	public static MonoMac.Foundation.NSString All { get; }
	public static MonoMac.Foundation.NSString Any { get; }
	public static MonoMac.Foundation.NSString Closest { get; }
}
```

### New Type MonoMac.SceneKit.SCNPhysicsVehicle

```
public class SCNPhysicsVehicle : MonoMac.SceneKit.SCNPhysicsBehavior, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicle (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsVehicle (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.SceneKit.SCNPhysicsVehicleWheel

```
public class SCNPhysicsVehicleWheel : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicleWheel (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsVehicleWheel (MonoMac.Foundation.NSObjectFlag t);
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
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNPhysicsVehicleWheel Create (SCNNode node);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SceneKit.SCNPhysicsWorld

```
public class SCNPhysicsWorld : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsWorld (MonoMac.Foundation.NSCoder coder);
	public SCNPhysicsWorld (MonoMac.Foundation.NSObjectFlag t);
	public SCNPhysicsWorld (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBehavior[] AllBehaviors { get; }
	public override System.IntPtr ClassHandle { get; }
	public SCNPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual SCNVector3 Gravity { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeStep { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidBeginContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidEndContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidUpdateContact;
	// methods
	public virtual void AddBehavior (SCNPhysicsBehavior behavior);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, MonoMac.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, MonoMac.Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, SCNPhysicsTest options);
	public SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, MonoMac.Foundation.NSDictionary options);
	protected override void Dispose (bool disposing);
	public virtual SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, MonoMac.Foundation.NSDictionary options);
	public SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, SCNPhysicsTest options);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (SCNPhysicsBehavior behavior);
	public virtual void UpdateCollisionPairs ();
}
```

### New Type MonoMac.SceneKit.SCNProgramDelegate_Extensions

```
public static class SCNProgramDelegate_Extensions {
	// methods
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public static void HandleError (ISCNProgramDelegate This, SCNProgram program, MonoMac.Foundation.NSError error);
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
}
```

### New Type MonoMac.SceneKit.SCNProgramSemanticOptions

```
public class SCNProgramSemanticOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNProgramSemanticOptions ();
	public SCNProgramSemanticOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public uint? MappingChannel { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNQuaternion

```
[Serializable]
public struct SCNQuaternion, System.IEquatable<SCNQuaternion> {
	// constructors
	public SCNQuaternion (SCNVector3 v, float w);
	public SCNQuaternion (float x, float y, float z, float w);
	public SCNQuaternion (ref MonoMac.OpenGL.Matrix3d matrix);
	public SCNQuaternion (MonoMac.OpenGL.Quaternion openTkQuaternion);
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

### New Type MonoMac.SceneKit.SCNSceneExportDelegate

```
public class SCNSceneExportDelegate : MonoMac.Foundation.NSObject, ISCNSceneExportDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneExportDelegate ();
	public SCNSceneExportDelegate (MonoMac.Foundation.NSCoder coder);
	public SCNSceneExportDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SCNSceneExportDelegate (System.IntPtr handle);
	// methods
	public virtual MonoMac.Foundation.NSUrl WriteImage (MonoMac.AppKit.NSImage image, MonoMac.Foundation.NSUrl documentURL, MonoMac.Foundation.NSUrl originalImageURL);
}
```

### New Type MonoMac.SceneKit.SCNSceneExportDelegate_Extensions

```
public static class SCNSceneExportDelegate_Extensions {
	// methods
	public static MonoMac.Foundation.NSUrl WriteImage (ISCNSceneExportDelegate This, MonoMac.AppKit.NSImage image, MonoMac.Foundation.NSUrl documentURL, MonoMac.Foundation.NSUrl originalImageURL);
}
```

### New Type MonoMac.SceneKit.SCNSceneExportProgressHandler

```
public sealed delegate SCNSceneExportProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneExportProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (float totalProgress, MonoMac.Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (float totalProgress, MonoMac.Foundation.NSError error, out bool stop);
}
```

### New Type MonoMac.SceneKit.SCNSceneLoadingOptions

```
public class SCNSceneLoadingOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNSceneLoadingOptions ();
	public SCNSceneLoadingOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public MonoMac.Foundation.NSUrl[] AssetDirectoryUrls { get; set; }
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

### New Type MonoMac.SceneKit.SCNSceneRenderer

```
public abstract class SCNSceneRenderer : MonoMac.Foundation.NSObject, ISCNSceneRenderer, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneRenderer ();
	public SCNSceneRenderer (MonoMac.Foundation.NSCoder coder);
	public SCNSceneRenderer (MonoMac.Foundation.NSObjectFlag t);
	public SCNSceneRenderer (System.IntPtr handle);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public virtual System.IntPtr Context { get; }
	public virtual double CurrentTime { get; set; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual MonoMac.SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual bool Prepare (MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual void Prepare (MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
}
```

### New Type MonoMac.SceneKit.SCNSceneRenderer_Extensions

```
public static class SCNSceneRenderer_Extensions {
	// methods
	public static SCNHitTestResult[] HitTest (ISCNSceneRenderer This, System.Drawing.PointF thePoint, SCNHitTestOptions options);
	public static bool IsNodeInsideFrustum (ISCNSceneRenderer This, SCNNode node, SCNNode pointOfView);
	public static bool Prepare (ISCNSceneRenderer This, MonoMac.Foundation.NSObject obj, System.Func<bool> abortHandler);
	public static void Prepare (ISCNSceneRenderer This, MonoMac.Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public static SCNVector3 ProjectPoint (ISCNSceneRenderer This, SCNVector3 point);
	public static SCNVector3 UnprojectPoint (ISCNSceneRenderer This, SCNVector3 point);
}
```

### New Type MonoMac.SceneKit.SCNSceneRendererDelegate_Extensions

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

### New Type MonoMac.SceneKit.SCNSceneSourceFilter

```
public sealed delegate SCNSceneSourceFilter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneSourceFilter (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSObject entry, MonoMac.Foundation.NSString identifier, ref bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual bool Invoke (MonoMac.Foundation.NSObject entry, MonoMac.Foundation.NSString identifier, ref bool stop);
}
```

### New Type MonoMac.SceneKit.SCNShadable

```
public class SCNShadable : MonoMac.Foundation.NSObject, ISCNShadable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNShadable ();
	public SCNShadable (MonoMac.Foundation.NSCoder coder);
	public SCNShadable (MonoMac.Foundation.NSObjectFlag t);
	public SCNShadable (System.IntPtr handle);
	// properties
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakShaderModifiers { get; set; }
	// methods
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
}
```

### New Type MonoMac.SceneKit.SCNShadable_Extensions

```
public static class SCNShadable_Extensions {
	// methods
	public static void HandleBinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
	public static void HandleUnbinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
}
```

### New Type MonoMac.SceneKit.SCNShadowMode

```
[Serializable]
public enum SCNShadowMode {
	Deferred = 1,
	Forward = 0,
	Modulated = 2,
}
```

### New Type MonoMac.SceneKit.SCNTechnique

```
public class SCNTechnique : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, ISCNAnimatable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechnique (MonoMac.Foundation.NSCoder coder);
	public SCNTechnique (MonoMac.Foundation.NSObjectFlag t);
	public SCNTechnique (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDictionary DictionaryRepresentation { get; }
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNTechnique Create (MonoMac.Foundation.NSDictionary dictionary);
	public static SCNTechnique Create (SCNTechnique[] techniques);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (MonoMac.Foundation.NSString key);
	public virtual void PauseAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (MonoMac.Foundation.NSString key);
}
```

### New Type MonoMac.SceneKit.SCNTechniqueSupport

```
public abstract class SCNTechniqueSupport : MonoMac.Foundation.NSObject, ISCNTechniqueSupport, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechniqueSupport ();
	public SCNTechniqueSupport (MonoMac.Foundation.NSCoder coder);
	public SCNTechniqueSupport (MonoMac.Foundation.NSObjectFlag t);
	public SCNTechniqueSupport (System.IntPtr handle);
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type MonoMac.SceneKit.SCNTechniqueSupport_Extensions

```
public static class SCNTechniqueSupport_Extensions {
}
```

## Namespace MonoMac.StoreKit

### Type Changed: MonoMac.StoreKit.ISKProductsRequestDelegate

Added interface:

```
ISKRequestDelegate
```

### Type Changed: MonoMac.StoreKit.SKPaymentTransactionState

Added value:

```
Deferred = 4,
```

## Namespace MonoMac.WebKit

### New Type MonoMac.WebKit.IWKNavigationDelegate

```
public interface IWKNavigationDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.IWKScriptMessageHandler

```
public interface IWKScriptMessageHandler : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type MonoMac.WebKit.IWKUIDelegate

```
public interface IWKUIDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.WebKit.WKBackForwardList

```
public class WKBackForwardList : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardList (MonoMac.Foundation.NSCoder coder);
	public WKBackForwardList (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.WebKit.WKBackForwardListItem

```
public class WKBackForwardListItem : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardListItem (MonoMac.Foundation.NSCoder coder);
	public WKBackForwardListItem (MonoMac.Foundation.NSObjectFlag t);
	public WKBackForwardListItem (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSUrl InitialUrl { get; }
	public virtual string Title { get; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKErrorCode

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

### New Type MonoMac.WebKit.WKFrameInfo

```
public class WKFrameInfo : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKFrameInfo ();
	public WKFrameInfo (MonoMac.Foundation.NSCoder coder);
	public WKFrameInfo (MonoMac.Foundation.NSObjectFlag t);
	public WKFrameInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool MainFrame { get; }
	public virtual MonoMac.Foundation.NSUrlRequest Request { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKJavascriptEvaluationResult

```
public sealed delegate WKJavascriptEvaluationResult : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WKJavascriptEvaluationResult (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSObject result, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSObject result, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.WebKit.WKNavigation

```
public class WKNavigation : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigation ();
	public WKNavigation (MonoMac.Foundation.NSCoder coder);
	public WKNavigation (MonoMac.Foundation.NSObjectFlag t);
	public WKNavigation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSError Error { get; }
	public virtual MonoMac.Foundation.NSUrlRequest InitialRequest { get; }
	public virtual MonoMac.Foundation.NSUrlRequest Request { get; }
	public virtual MonoMac.Foundation.NSUrlResponse Response { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKNavigationAction

```
public class WKNavigationAction : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationAction ();
	public WKNavigationAction (MonoMac.Foundation.NSCoder coder);
	public WKNavigationAction (MonoMac.Foundation.NSObjectFlag t);
	public WKNavigationAction (System.IntPtr handle);
	// properties
	public virtual int ButtonNumber { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.AppKit.NSEventModifierMask ModifierFlags { get; }
	public virtual WKNavigationType NavigationType { get; }
	public virtual MonoMac.Foundation.NSUrlRequest Request { get; }
	public virtual WKFrameInfo SourceFrame { get; }
	public virtual WKFrameInfo TargetFrame { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKNavigationActionPolicy

```
[Serializable]
public enum WKNavigationActionPolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoMac.WebKit.WKNavigationDelegate

```
public class WKNavigationDelegate : MonoMac.Foundation.NSObject, IWKNavigationDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationDelegate ();
	public WKNavigationDelegate (MonoMac.Foundation.NSCoder coder);
	public WKNavigationDelegate (MonoMac.Foundation.NSObjectFlag t);
	public WKNavigationDelegate (System.IntPtr handle);
	// methods
	public virtual void DecidePolicy (WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public virtual void DecidePolicy (WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public virtual void DidCommitNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidFailNavigation (WKWebView webView, WKNavigation navigation, MonoMac.Foundation.NSError error);
	public virtual void DidFailProvisionalNavigation (WKWebView webView, WKNavigation navigation, MonoMac.Foundation.NSError error);
	public virtual void DidFinishNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidReceiveAuthenticationChallenge (WKWebView webView, MonoMac.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoMac.Foundation.NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public virtual void DidReceiveServerRedirectForProvisionalNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidStartProvisionalNavigation (WKWebView webView, WKNavigation navigation);
}
```

### New Type MonoMac.WebKit.WKNavigationDelegate_Extensions

```
public static class WKNavigationDelegate_Extensions {
	// methods
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public static void DidCommitNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidFailNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, MonoMac.Foundation.NSError error);
	public static void DidFailProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, MonoMac.Foundation.NSError error);
	public static void DidFinishNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidReceiveAuthenticationChallenge (IWKNavigationDelegate This, WKWebView webView, MonoMac.Foundation.NSUrlAuthenticationChallenge challenge, System.Action<MonoMac.Foundation.NSUrlSessionAuthChallengeDisposition,MonoMac.Foundation.NSUrlCredential> completionHandler);
	public static void DidReceiveServerRedirectForProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidStartProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
}
```

### New Type MonoMac.WebKit.WKNavigationResponse

```
public class WKNavigationResponse : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationResponse ();
	public WKNavigationResponse (MonoMac.Foundation.NSCoder coder);
	public WKNavigationResponse (MonoMac.Foundation.NSObjectFlag t);
	public WKNavigationResponse (System.IntPtr handle);
	// properties
	public virtual bool CanShowMimeType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsForMainFrame { get; }
	public virtual MonoMac.Foundation.NSUrlResponse Response { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKNavigationResponsePolicy

```
[Serializable]
public enum WKNavigationResponsePolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type MonoMac.WebKit.WKNavigationType

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

### New Type MonoMac.WebKit.WKPreferences

```
public class WKPreferences : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKPreferences ();
	public WKPreferences (MonoMac.Foundation.NSCoder coder);
	public WKPreferences (MonoMac.Foundation.NSObjectFlag t);
	public WKPreferences (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool JavaEnabled { get; set; }
	public virtual bool JavaScriptCanOpenWindowsAutomatically { get; set; }
	public virtual bool JavaScriptEnabled { get; set; }
	public virtual float MinimumFontSize { get; set; }
	public virtual bool PlugInsEnabled { get; set; }
}
```

### New Type MonoMac.WebKit.WKProcessPool

```
public class WKProcessPool : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKProcessPool ();
	public WKProcessPool (MonoMac.Foundation.NSCoder coder);
	public WKProcessPool (MonoMac.Foundation.NSObjectFlag t);
	public WKProcessPool (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.WebKit.WKScriptMessage

```
public class WKScriptMessage : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessage ();
	public WKScriptMessage (MonoMac.Foundation.NSCoder coder);
	public WKScriptMessage (MonoMac.Foundation.NSObjectFlag t);
	public WKScriptMessage (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSObject Body { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKFrameInfo FrameInfo { get; }
	public virtual string Name { get; }
	public virtual WKWebView WebView { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKScriptMessageHandler

```
public abstract class WKScriptMessageHandler : MonoMac.Foundation.NSObject, IWKScriptMessageHandler, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessageHandler ();
	public WKScriptMessageHandler (MonoMac.Foundation.NSCoder coder);
	public WKScriptMessageHandler (MonoMac.Foundation.NSObjectFlag t);
	public WKScriptMessageHandler (System.IntPtr handle);
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type MonoMac.WebKit.WKScriptMessageHandler_Extensions

```
public static class WKScriptMessageHandler_Extensions {
}
```

### New Type MonoMac.WebKit.WKSelectionGranularity

```
[Serializable]
public enum WKSelectionGranularity {
	Character = 1,
	Dynamic = 0,
}
```

### New Type MonoMac.WebKit.WKUIDelegate

```
public class WKUIDelegate : MonoMac.Foundation.NSObject, IWKUIDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUIDelegate ();
	public WKUIDelegate (MonoMac.Foundation.NSCoder coder);
	public WKUIDelegate (MonoMac.Foundation.NSObjectFlag t);
	public WKUIDelegate (System.IntPtr handle);
	// methods
	public virtual WKWebView CreateWebView (WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public virtual void RunJavaScriptAlertPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public virtual void RunJavaScriptConfirmPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public virtual void RunJavaScriptTextInputPanel (WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type MonoMac.WebKit.WKUIDelegate_Extensions

```
public static class WKUIDelegate_Extensions {
	// methods
	public static WKWebView CreateWebView (IWKUIDelegate This, WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public static void RunJavaScriptAlertPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public static void RunJavaScriptConfirmPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public static void RunJavaScriptTextInputPanel (IWKUIDelegate This, WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type MonoMac.WebKit.WKUserContentController

```
public class WKUserContentController : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserContentController ();
	public WKUserContentController (MonoMac.Foundation.NSCoder coder);
	public WKUserContentController (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.WebKit.WKUserScript

```
public class WKUserScript : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserScript (MonoMac.Foundation.NSCoder coder);
	public WKUserScript (MonoMac.Foundation.NSObjectFlag t);
	public WKUserScript (System.IntPtr handle);
	public WKUserScript (MonoMac.Foundation.NSString source, WKUserScriptInjectionTime injectionTime, bool isForMainFrameOnly);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKUserScriptInjectionTime InjectionTime { get; }
	public virtual bool IsForMainFrameOnly { get; }
	public virtual MonoMac.Foundation.NSString Source { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKUserScriptInjectionTime

```
[Serializable]
public enum WKUserScriptInjectionTime {
	AtDocumentEnd = 1,
	AtDocumentStart = 0,
}
```

### New Type MonoMac.WebKit.WKWebView

```
public class WKWebView : MonoMac.AppKit.NSView, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebView (MonoMac.Foundation.NSCoder coder);
	public WKWebView (MonoMac.Foundation.NSObjectFlag t);
	public WKWebView (System.IntPtr handle);
	public WKWebView (System.Drawing.RectangleF frame, WKWebViewConfiguration configuration);
	// properties
	public virtual bool AllowsBackForwardNavigationGestures { get; set; }
	public virtual bool AllowsMagnification { get; set; }
	public virtual WKBackForwardList BackForwardList { get; }
	public virtual bool CanGoBack { get; }
	public virtual bool CanGoForward { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKWebViewConfiguration Configuration { get; }
	public virtual double EstimatedProgress { get; }
	public virtual bool HasOnlySecureContent { get; }
	public virtual bool IsLoading { get; }
	public virtual float Magnification { get; set; }
	public WKNavigationDelegate NavigationDelegate { get; set; }
	public virtual string Title { get; }
	public WKUIDelegate UIDelegate { get; set; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
	public virtual MonoMac.Foundation.NSObject WeakNavigationDelegate { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakUIDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EvaluateJavaScript (MonoMac.Foundation.NSString javascript, WKJavascriptEvaluationResult completionHandler);
	public virtual System.Threading.Tasks.Task<MonoMac.Foundation.NSObject> EvaluateJavaScriptAsync (MonoMac.Foundation.NSString javascript);
	public virtual WKNavigation GoBack ();
	public virtual WKNavigation GoForward ();
	public virtual WKNavigation GoTo (WKBackForwardListItem item);
	public virtual WKNavigation LoadHtmlString (MonoMac.Foundation.NSString htmlString, MonoMac.Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadRequest (MonoMac.Foundation.NSUrlRequest request);
	public virtual WKNavigation Reload ();
	public virtual WKNavigation ReloadFromOrigin ();
	public virtual void SetMagnification (float magnification, System.Drawing.PointF centerPoint);
	public virtual void StopLoading ();
}
```

### New Type MonoMac.WebKit.WKWebViewConfiguration

```
public class WKWebViewConfiguration : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebViewConfiguration ();
	public WKWebViewConfiguration (MonoMac.Foundation.NSCoder coder);
	public WKWebViewConfiguration (MonoMac.Foundation.NSObjectFlag t);
	public WKWebViewConfiguration (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKPreferences Preferences { get; set; }
	public virtual WKProcessPool ProcessPool { get; set; }
	public virtual bool SuppressesIncrementalRendering { get; set; }
	public virtual WKUserContentController UserContentController { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.WebKit.WKWindowFeatures

```
public class WKWindowFeatures : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWindowFeatures ();
	public WKWindowFeatures (MonoMac.Foundation.NSCoder coder);
	public WKWindowFeatures (MonoMac.Foundation.NSObjectFlag t);
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

## New Namespace MonoMac.CloudKit

### New Type MonoMac.CloudKit.CKAccountStatus

```
[Serializable]
public enum CKAccountStatus {
	Available = 1,
	CouldNotDetermine = 0,
	NoAccount = 3,
	Restricted = 2,
}
```

### New Type MonoMac.CloudKit.CKApplicationPermissions

```
[Serializable]
[Flags]
public enum CKApplicationPermissions {
	UserDiscoverability = 1,
}
```

### New Type MonoMac.CloudKit.CKApplicationPermissionStatus

```
[Serializable]
public enum CKApplicationPermissionStatus {
	CouldNotComplete = 1,
	Denied = 2,
	Granted = 3,
	InitialState = 0,
}
```

### New Type MonoMac.CloudKit.CKAsset

```
public class CKAsset : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKAsset (MonoMac.Foundation.NSCoder coder);
	public CKAsset (MonoMac.Foundation.NSObjectFlag t);
	public CKAsset (System.IntPtr handle);
	public CKAsset (MonoMac.Foundation.NSUrl fileUrl);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSUrl FileUrl { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKContainer

```
public class CKContainer : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKContainer (MonoMac.Foundation.NSCoder coder);
	public CKContainer (MonoMac.Foundation.NSObjectFlag t);
	public CKContainer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public static CKContainer DefaultContainer { get; }
	public static MonoMac.Foundation.NSString OwnerDefaultName { get; }
	public virtual CKDatabase PrivateCloudDatabase { get; }
	public virtual CKDatabase PublicCloudDatabase { get; }
	// methods
	public virtual void AddOperation (CKOperation operation);
	public virtual void DiscoverAllContactUserInfos (System.Action<CKDiscoveredUserInfo[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo[]> DiscoverAllContactUserInfosAsync ();
	public virtual void DiscoverUserInfo (CKRecordID userRecordId, System.Action<CKDiscoveredUserInfo,MonoMac.Foundation.NSError> completionHandler);
	public virtual void DiscoverUserInfo (string email, System.Action<CKDiscoveredUserInfo,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (string email);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (CKRecordID userRecordId);
	protected override void Dispose (bool disposing);
	public virtual void FetchUserRecordId (System.Action<CKRecordID,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> FetchUserRecordIdAsync ();
	public static CKContainer FromIdentifier (string containerIdentifier);
	public virtual void GetAccountStatus (System.Action<CKAccountStatus,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKAccountStatus> GetAccountStatusAsync ();
	public virtual void RequestApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> RequestApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
	public virtual void StatusForApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> StatusForApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
}
```

### New Type MonoMac.CloudKit.CKDatabase

```
public class CKDatabase : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabase (MonoMac.Foundation.NSCoder coder);
	public CKDatabase (MonoMac.Foundation.NSObjectFlag t);
	public CKDatabase (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void AddOperation (CKDatabaseOperation operation);
	public virtual void DeleteRecord (CKRecordID recordId, System.Action<CKRecordID,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> DeleteRecordAsync (CKRecordID recordId);
	public virtual void DeleteRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZoneID,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZoneID> DeleteRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void DeleteSubscription (string subscriptionID, CKDatabaseDeleteSubscriptionHandler completionHandler);
	public virtual System.Threading.Tasks.Task<string> DeleteSubscriptionAsync (string subscriptionID);
	public virtual void FetchAllRecordZones (System.Action<CKRecordZone[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone[]> FetchAllRecordZonesAsync ();
	public virtual void FetchAllSubscriptions (System.Action<CKSubscription[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription[]> FetchAllSubscriptionsAsync ();
	public virtual void FetchRecord (CKRecordID recordId, System.Action<CKRecord,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> FetchRecordAsync (CKRecordID recordId);
	public virtual void FetchRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZone,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> FetchRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void FetchSubscription (string subscriptionId, System.Action<CKSubscription,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> FetchSubscriptionAsync (string subscriptionId);
	public virtual void PerformQuery (CKQuery query, CKRecordZoneID zoneId, System.Action<CKRecord[],MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord[]> PerformQueryAsync (CKQuery query, CKRecordZoneID zoneId);
	public virtual void SaveRecord (CKRecord record, System.Action<CKRecord,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> SaveRecordAsync (CKRecord record);
	public virtual void SaveRecordZone (CKRecordZone zone, System.Action<CKRecordZone,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> SaveRecordZoneAsync (CKRecordZone zone);
	public virtual void SaveSubscription (CKSubscription subscription, System.Action<CKSubscription,MonoMac.Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> SaveSubscriptionAsync (CKSubscription subscription);
}
```

### New Type MonoMac.CloudKit.CKDatabaseDeleteSubscriptionHandler

```
public sealed delegate CKDatabaseDeleteSubscriptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDatabaseDeleteSubscriptionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (string subscriptionId, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (string subscriptionId, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.CloudKit.CKDatabaseOperation

```
public class CKDatabaseOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabaseOperation (MonoMac.Foundation.NSCoder coder);
	public CKDatabaseOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKDatabaseOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKDatabase Database { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKDiscoverAllContactsOperation

```
public class CKDiscoverAllContactsOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverAllContactsOperation ();
	public CKDiscoverAllContactsOperation (MonoMac.Foundation.NSCoder coder);
	public CKDiscoverAllContactsOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKDiscoverAllContactsOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKDiscoveredUserInfo[],MonoMac.Foundation.NSError> DiscoverAllContactsHandler { get; set; }
}
```

### New Type MonoMac.CloudKit.CKDiscoveredUserInfo

```
public class CKDiscoveredUserInfo : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoveredUserInfo ();
	public CKDiscoveredUserInfo (MonoMac.Foundation.NSCoder coder);
	public CKDiscoveredUserInfo (MonoMac.Foundation.NSObjectFlag t);
	public CKDiscoveredUserInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string FirstName { get; }
	public virtual string LastName { get; }
	public virtual CKRecordID UserRecordId { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKDiscoverUserInfosCompletionHandler

```
public sealed delegate CKDiscoverUserInfosCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDiscoverUserInfosCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSDictionary emailsToUserInfos, MonoMac.Foundation.NSDictionary userRecordIdsToUserInfos, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSDictionary emailsToUserInfos, MonoMac.Foundation.NSDictionary userRecordIdsToUserInfos, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKDiscoverUserInfosOperation

```
public class CKDiscoverUserInfosOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverUserInfosOperation ();
	public CKDiscoverUserInfosOperation (MonoMac.Foundation.NSCoder coder);
	public CKDiscoverUserInfosOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKErrorCode

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

### New Type MonoMac.CloudKit.CKErrorFields

```
public static class CKErrorFields {
	// properties
	public static MonoMac.Foundation.NSString ErrorDomain { get; }
	public static MonoMac.Foundation.NSString ErrorRetryAfterKey { get; }
	public static MonoMac.Foundation.NSString PartialErrorsByItemIdKey { get; }
	public static MonoMac.Foundation.NSString RecordChangedErrorAncestorRecordKey { get; }
	public static MonoMac.Foundation.NSString RecordChangedErrorClientRecordKey { get; }
	public static MonoMac.Foundation.NSString RecordChangedErrorServerRecordKey { get; }
}
```

### New Type MonoMac.CloudKit.CKFetchNotificationChangesOperation

```
public class CKFetchNotificationChangesOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchNotificationChangesOperation ();
	public CKFetchNotificationChangesOperation (MonoMac.Foundation.NSCoder coder);
	public CKFetchNotificationChangesOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKFetchNotificationChangesOperation (System.IntPtr handle);
	public CKFetchNotificationChangesOperation (CKServerChangeToken previousServerChangeToken);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKServerChangeToken,MonoMac.Foundation.NSError> Completed { set; }
	public virtual bool MoreComing { get; }
	public virtual System.Action<CKNotification> NotificationChanged { set; }
	public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }
	public virtual uint ResultsLimit { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKFetchRecordChangesHandler

```
public sealed delegate CKFetchRecordChangesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordChangesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKServerChangeToken serverChangeToken, MonoMac.Foundation.NSData clientChangeTokenData, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKServerChangeToken serverChangeToken, MonoMac.Foundation.NSData clientChangeTokenData, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKFetchRecordChangesOperation

```
public class CKFetchRecordChangesOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordChangesOperation ();
	public CKFetchRecordChangesOperation (MonoMac.Foundation.NSCoder coder);
	public CKFetchRecordChangesOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKFetchRecordsCompletedHandler

```
public sealed delegate CKFetchRecordsCompletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordsCompletedHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSDictionary recordsByRecordId, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSDictionary recordsByRecordId, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.CloudKit.CKFetchRecordsOperation

```
public class CKFetchRecordsOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordsOperation ();
	public CKFetchRecordsOperation (MonoMac.Foundation.NSCoder coder);
	public CKFetchRecordsOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKFetchRecordsOperation (System.IntPtr handle);
	public CKFetchRecordsOperation (CKRecordID[] recordIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKFetchRecordsCompletedHandler Completed { set; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual System.Action<CKRecord,MonoMac.CloudKit.CKRecordID,MonoMac.Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecordID,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKFetchRecordsOperation FetchCurrentUserRecordOperation ();
}
```

### New Type MonoMac.CloudKit.CKFetchRecordZonesOperation

```
public class CKFetchRecordZonesOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordZonesOperation ();
	public CKFetchRecordZonesOperation (MonoMac.Foundation.NSCoder coder);
	public CKFetchRecordZonesOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKFetchSubscriptionsCompleteHandler

```
public sealed delegate CKFetchSubscriptionsCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchSubscriptionsCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSDictionary subscriptionsBySubscriptionId, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSDictionary subscriptionsBySubscriptionId, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKFetchSubscriptionsOperation

```
public class CKFetchSubscriptionsOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchSubscriptionsOperation ();
	public CKFetchSubscriptionsOperation (MonoMac.Foundation.NSCoder coder);
	public CKFetchSubscriptionsOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKLocationSortDescriptor

```
public class CKLocationSortDescriptor : MonoMac.Foundation.NSSortDescriptor, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCopying {
	// constructors
	public CKLocationSortDescriptor ();
	public CKLocationSortDescriptor (MonoMac.Foundation.NSCoder coder);
	public CKLocationSortDescriptor (MonoMac.Foundation.NSObjectFlag t);
	public CKLocationSortDescriptor (System.IntPtr handle);
	public CKLocationSortDescriptor (string key, MonoMac.CoreLocation.CLLocation relativeLocation);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreLocation.CLLocation RelativeLocation { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKMarkNotificationsReadHandler

```
public sealed delegate CKMarkNotificationsReadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKMarkNotificationsReadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKNotificationID[] notificationIDsMarkedRead, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKNotificationID[] notificationIDsMarkedRead, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKMarkNotificationsReadOperation

```
public class CKMarkNotificationsReadOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKMarkNotificationsReadOperation (MonoMac.Foundation.NSCoder coder);
	public CKMarkNotificationsReadOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKModifyBadgeOperation

```
public class CKModifyBadgeOperation : MonoMac.CloudKit.CKOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyBadgeOperation ();
	public CKModifyBadgeOperation (MonoMac.Foundation.NSCoder coder);
	public CKModifyBadgeOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKModifyBadgeOperation (System.IntPtr handle);
	public CKModifyBadgeOperation (uint badgeValue);
	// properties
	public virtual uint BadgeValue { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<MonoMac.Foundation.NSError> Completed { set; }
}
```

### New Type MonoMac.CloudKit.CKModifyRecordsOperation

```
public class CKModifyRecordsOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordsOperation ();
	public CKModifyRecordsOperation (MonoMac.Foundation.NSCoder coder);
	public CKModifyRecordsOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKModifyRecordsOperation (System.IntPtr handle);
	public CKModifyRecordsOperation (CKRecord[] records, CKRecordID[] recordIds);
	// properties
	public virtual bool Atomic { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSData ClientChangeTokenData { get; set; }
	public virtual CKModifyRecordsOperationHandler Completed { set; }
	public virtual System.Action<CKRecord,MonoMac.Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecord,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIdsToDelete { get; set; }
	public virtual CKRecord[] RecordsToSave { get; set; }
	public virtual CKRecordSavePolicy SavePolicy { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKModifyRecordsOperationHandler

```
public sealed delegate CKModifyRecordsOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordsOperationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKModifyRecordZonesHandler

```
public sealed delegate CKModifyRecordZonesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordZonesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKModifyRecordZonesOperation

```
public class CKModifyRecordZonesOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordZonesOperation ();
	public CKModifyRecordZonesOperation (MonoMac.Foundation.NSCoder coder);
	public CKModifyRecordZonesOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKModifySubscriptionsHandler

```
public sealed delegate CKModifySubscriptionsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifySubscriptionsHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKModifySubscriptionsOperation

```
public class CKModifySubscriptionsOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifySubscriptionsOperation ();
	public CKModifySubscriptionsOperation (MonoMac.Foundation.NSCoder coder);
	public CKModifySubscriptionsOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKNotification

```
public class CKNotification : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotification (MonoMac.Foundation.NSCoder coder);
	public CKNotification (MonoMac.Foundation.NSObjectFlag t);
	public CKNotification (System.IntPtr handle);
	// properties
	public virtual string AlertActionLocalizationKey { get; }
	public virtual string AlertBody { get; }
	public virtual string AlertLaunchImage { get; }
	public virtual string[] AlertLocalizationArgs { get; }
	public virtual string AlertLocalizationKey { get; }
	public virtual MonoMac.Foundation.NSNumber Badge { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public virtual bool IsPruned { get; }
	public virtual CKNotificationID NotificationId { get; }
	public virtual CKNotificationType NotificationType { get; }
	public virtual string SoundName { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKNotification FromRemoteNotificationDictionary (MonoMac.Foundation.NSDictionary notificationDictionary);
}
```

### New Type MonoMac.CloudKit.CKNotificationID

```
public class CKNotificationID : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationID ();
	public CKNotificationID (MonoMac.Foundation.NSCoder coder);
	public CKNotificationID (MonoMac.Foundation.NSObjectFlag t);
	public CKNotificationID (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.CloudKit.CKNotificationInfo

```
public class CKNotificationInfo : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationInfo ();
	public CKNotificationInfo (MonoMac.Foundation.NSCoder coder);
	public CKNotificationInfo (MonoMac.Foundation.NSObjectFlag t);
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
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.CloudKit.CKNotificationType

```
[Serializable]
public enum CKNotificationType {
	Query = 1,
	ReadNotification = 3,
	RecordZone = 2,
}
```

### New Type MonoMac.CloudKit.CKOperation

```
public class CKOperation : MonoMac.Foundation.NSOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKOperation (MonoMac.Foundation.NSCoder coder);
	public CKOperation (MonoMac.Foundation.NSObjectFlag t);
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

### New Type MonoMac.CloudKit.CKQuery

```
public class CKQuery : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQuery (MonoMac.Foundation.NSCoder coder);
	public CKQuery (MonoMac.Foundation.NSObjectFlag t);
	public CKQuery (System.IntPtr handle);
	public CKQuery (string recordType, MonoMac.Foundation.NSPredicate predicate);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual MonoMac.Foundation.NSSortDescriptor[] SortDescriptors { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKQueryCursor

```
public class CKQueryCursor : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryCursor (MonoMac.Foundation.NSCoder coder);
	public CKQueryCursor (MonoMac.Foundation.NSObjectFlag t);
	public CKQueryCursor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.CloudKit.CKQueryNotification

```
public class CKQueryNotification : MonoMac.CloudKit.CKNotification, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryNotification (MonoMac.Foundation.NSCoder coder);
	public CKQueryNotification (MonoMac.Foundation.NSObjectFlag t);
	public CKQueryNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsPublicDatabase { get; }
	public virtual CKQueryNotificationReason QueryNotificationReason { get; }
	public virtual MonoMac.Foundation.NSDictionary RecordFields { get; }
	public virtual CKRecordID RecordId { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKQueryNotificationReason

```
[Serializable]
public enum CKQueryNotificationReason {
	RecordCreated = 1,
	RecordDeleted = 3,
	RecordUpdated = 2,
}
```

### New Type MonoMac.CloudKit.CKQueryOperation

```
public class CKQueryOperation : MonoMac.CloudKit.CKDatabaseOperation, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryOperation ();
	public CKQueryOperation (MonoMac.Foundation.NSCoder coder);
	public CKQueryOperation (MonoMac.Foundation.NSObjectFlag t);
	public CKQueryOperation (System.IntPtr handle);
	public CKQueryOperation (CKQuery query);
	public CKQueryOperation (CKQueryCursor cursor);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKQueryCursor,MonoMac.Foundation.NSError> Completed { set; }
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

### New Type MonoMac.CloudKit.CKRecord

```
public class CKRecord : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecord (MonoMac.Foundation.NSCoder coder);
	public CKRecord (MonoMac.Foundation.NSObjectFlag t);
	public CKRecord (System.IntPtr handle);
	public CKRecord (string recordType);
	public CKRecord (string recordType, CKRecordID recordId);
	public CKRecord (string recordType, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDate CreationDate { get; }
	public virtual CKRecordID CreatorUserRecordId { get; }
	public MonoMac.Foundation.NSObject Item { get; set; }
	public virtual CKRecordID LastModifiedUserRecordId { get; }
	public virtual MonoMac.Foundation.NSDate ModificationDate { get; }
	public virtual string RecordChangeTag { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual string RecordType { get; }
	public static MonoMac.Foundation.NSString TypeUserRecord { get; }
	// methods
	public virtual string[] AllKeys ();
	public virtual string[] AllTokens ();
	public virtual string[] ChangedKeys ();
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeSystemFields (MonoMac.Foundation.NSCoder coder);
}
```

### New Type MonoMac.CloudKit.CKRecordID

```
public class CKRecordID : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordID ();
	public CKRecordID (MonoMac.Foundation.NSCoder coder);
	public CKRecordID (MonoMac.Foundation.NSObjectFlag t);
	public CKRecordID (System.IntPtr handle);
	public CKRecordID (string recordName);
	public CKRecordID (string recordName, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string RecordName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKRecordSavePolicy

```
[Serializable]
public enum CKRecordSavePolicy {
	SaveAllKeys = 2,
	SaveChangedKeys = 1,
	SaveIfServerRecordUnchanged = 0,
}
```

### New Type MonoMac.CloudKit.CKRecordValue

```
public class CKRecordValue : MonoMac.Foundation.NSObject, ICKRecordValue, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordValue ();
	public CKRecordValue (MonoMac.Foundation.NSCoder coder);
	public CKRecordValue (MonoMac.Foundation.NSObjectFlag t);
	public CKRecordValue (System.IntPtr handle);
}
```

### New Type MonoMac.CloudKit.CKRecordValue_Extensions

```
public static class CKRecordValue_Extensions {
}
```

### New Type MonoMac.CloudKit.CKRecordZone

```
public class CKRecordZone : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZone ();
	public CKRecordZone (MonoMac.Foundation.NSCoder coder);
	public CKRecordZone (MonoMac.Foundation.NSObjectFlag t);
	public CKRecordZone (System.IntPtr handle);
	public CKRecordZone (string zoneName);
	public CKRecordZone (CKRecordZoneID zoneId);
	// properties
	public virtual CKRecordZoneCapabilities Capabilities { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString DefaultName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static CKRecordZone DefaultRecordZone ();
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKRecordZoneCapabilities

```
[Serializable]
[Flags]
public enum CKRecordZoneCapabilities {
	Atomic = 2,
	FetchChanges = 1,
}
```

### New Type MonoMac.CloudKit.CKRecordZoneCompleteHandler

```
public sealed delegate CKRecordZoneCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKRecordZoneCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSDictionary recordZonesByZoneId, MonoMac.Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.Foundation.NSDictionary recordZonesByZoneId, MonoMac.Foundation.NSError operationError);
}
```

### New Type MonoMac.CloudKit.CKRecordZoneID

```
public class CKRecordZoneID : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneID ();
	public CKRecordZoneID (MonoMac.Foundation.NSCoder coder);
	public CKRecordZoneID (MonoMac.Foundation.NSObjectFlag t);
	public CKRecordZoneID (System.IntPtr handle);
	public CKRecordZoneID (string zoneName, string ownerName);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string OwnerName { get; }
	public virtual string ZoneName { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.CloudKit.CKRecordZoneNotification

```
public class CKRecordZoneNotification : MonoMac.CloudKit.CKNotification, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneNotification (MonoMac.Foundation.NSCoder coder);
	public CKRecordZoneNotification (MonoMac.Foundation.NSObjectFlag t);
	public CKRecordZoneNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordZoneID RecordZoneId { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKReference

```
public class CKReference : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKReference (MonoMac.Foundation.NSCoder coder);
	public CKReference (MonoMac.Foundation.NSObjectFlag t);
	public CKReference (System.IntPtr handle);
	public CKReference (CKRecordID recordId, CKReferenceAction action);
	public CKReference (CKRecord record, CKReferenceAction action);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual CKReferenceAction ReferenceAction { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKReferenceAction

```
[Serializable]
public enum CKReferenceAction {
	DeleteSelf = 1,
	None = 0,
}
```

### New Type MonoMac.CloudKit.CKServerChangeToken

```
public class CKServerChangeToken : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKServerChangeToken (MonoMac.Foundation.NSCoder coder);
	public CKServerChangeToken (MonoMac.Foundation.NSObjectFlag t);
	public CKServerChangeToken (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.CloudKit.CKSubscription

```
public class CKSubscription : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKSubscription (MonoMac.Foundation.NSCoder coder);
	public CKSubscription (MonoMac.Foundation.NSObjectFlag t);
	public CKSubscription (System.IntPtr handle);
	public CKSubscription (string recordType, MonoMac.Foundation.NSPredicate predicate, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (string recordType, MonoMac.Foundation.NSPredicate predicate, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKNotificationInfo NotificationInfo { get; set; }
	public virtual MonoMac.Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual string SubscriptionId { get; }
	public virtual CKSubscriptionOptions SubscriptionOptions { get; }
	public virtual CKSubscriptionType SubscriptionType { get; }
	public virtual CKRecordZoneID ZoneID { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.CloudKit.CKSubscriptionOptions

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

### New Type MonoMac.CloudKit.CKSubscriptionType

```
[Serializable]
public enum CKSubscriptionType {
	Query = 1,
	RecordZone = 2,
}
```

### New Type MonoMac.CloudKit.ICKRecordValue

```
public interface ICKRecordValue : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## New Namespace MonoMac.GLKit

### New Type MonoMac.GLKit.GLKBaseEffect

```
public class GLKBaseEffect : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKBaseEffect ();
	public GLKBaseEffect (MonoMac.Foundation.NSCoder coder);
	public GLKBaseEffect (MonoMac.Foundation.NSObjectFlag t);
	public GLKBaseEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ColorMaterialEnabled { get; set; }
	public virtual MonoMac.OpenGL.Vector4 ConstantColor { get; set; }
	public virtual GLKEffectPropertyFog Fog { get; }
	public virtual string Label { get; set; }
	public virtual GLKEffectPropertyLight Light0 { get; }
	public virtual GLKEffectPropertyLight Light1 { get; }
	public virtual GLKEffectPropertyLight Light2 { get; }
	public virtual GLKLightingType LightingType { get; set; }
	public virtual MonoMac.OpenGL.Vector4 LightModelAmbientColor { get; set; }
	public virtual bool LightModelTwoSided { get; set; }
	public virtual GLKEffectPropertyMaterial Material { get; }
	public virtual GLKEffectPropertyTexture Texture2d0 { get; }
	public virtual GLKEffectPropertyTexture Texture2d1 { get; }
	public virtual GLKEffectPropertyTexture[] TextureOrder { get; set; }
	public virtual GLKEffectPropertyTransform Transform { get; }
	public virtual bool UseConstantColor { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void PrepareToDraw ();
}
```

### New Type MonoMac.GLKit.GLKEffectProperty

```
public class GLKEffectProperty : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectProperty ();
	public GLKEffectProperty (MonoMac.Foundation.NSCoder coder);
	public GLKEffectProperty (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectProperty (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type MonoMac.GLKit.GLKEffectPropertyFog

```
public class GLKEffectPropertyFog : MonoMac.GLKit.GLKEffectProperty, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyFog ();
	public GLKEffectPropertyFog (MonoMac.Foundation.NSCoder coder);
	public GLKEffectPropertyFog (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectPropertyFog (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Vector4 Color { get; set; }
	public virtual float Density { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual float End { get; set; }
	public virtual GLKFogMode Mode { get; set; }
	public virtual float Start { get; set; }
}
```

### New Type MonoMac.GLKit.GLKEffectPropertyLight

```
public class GLKEffectPropertyLight : MonoMac.GLKit.GLKEffectProperty, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyLight ();
	public GLKEffectPropertyLight (MonoMac.Foundation.NSCoder coder);
	public GLKEffectPropertyLight (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectPropertyLight (System.IntPtr handle);
	// properties
	public virtual MonoMac.OpenGL.Vector4 AmbientColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float ConstantAttenuation { get; set; }
	public virtual MonoMac.OpenGL.Vector4 DiffuseColor { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual float LinearAttenuation { get; set; }
	public virtual MonoMac.OpenGL.Vector4 Position { get; set; }
	public virtual float QuadraticAttenuation { get; set; }
	public virtual MonoMac.OpenGL.Vector4 SpecularColor { get; set; }
	public virtual float SpotCutoff { get; set; }
	public virtual MonoMac.OpenGL.Vector3 SpotDirection { get; set; }
	public virtual float SpotExponent { get; set; }
	public virtual GLKEffectPropertyTransform Transform { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.GLKit.GLKEffectPropertyMaterial

```
public class GLKEffectPropertyMaterial : MonoMac.GLKit.GLKEffectProperty, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyMaterial ();
	public GLKEffectPropertyMaterial (MonoMac.Foundation.NSCoder coder);
	public GLKEffectPropertyMaterial (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectPropertyMaterial (System.IntPtr handle);
	// properties
	public virtual MonoMac.OpenGL.Vector4 AmbientColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Vector4 DiffuseColor { get; set; }
	public virtual MonoMac.OpenGL.Vector4 EmissiveColor { get; set; }
	public virtual float Shininess { get; set; }
	public virtual MonoMac.OpenGL.Vector4 SpecularColor { get; set; }
}
```

### New Type MonoMac.GLKit.GLKEffectPropertyTexture

```
public class GLKEffectPropertyTexture : MonoMac.GLKit.GLKEffectProperty, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyTexture ();
	public GLKEffectPropertyTexture (MonoMac.Foundation.NSCoder coder);
	public GLKEffectPropertyTexture (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectPropertyTexture (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual GLKTextureEnvMode EnvMode { get; set; }
	public virtual uint GLName { get; set; }
	public virtual GLKTextureTarget Target { get; set; }
}
```

### New Type MonoMac.GLKit.GLKEffectPropertyTransform

```
public class GLKEffectPropertyTransform : MonoMac.GLKit.GLKEffectProperty, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyTransform ();
	public GLKEffectPropertyTransform (MonoMac.Foundation.NSCoder coder);
	public GLKEffectPropertyTransform (MonoMac.Foundation.NSObjectFlag t);
	public GLKEffectPropertyTransform (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Matrix4 ModelViewMatrix { get; set; }
	public virtual MonoMac.OpenGL.Matrix3d NormalMatrix { get; }
	public virtual MonoMac.OpenGL.Matrix4 ProjectionMatrix { get; set; }
}
```

### New Type MonoMac.GLKit.GLKFogMode

```
[Serializable]
public enum GLKFogMode {
	Exp = 0,
	Exp2 = 1,
	Linear = 2,
}
```

### New Type MonoMac.GLKit.GLKLightingType

```
[Serializable]
public enum GLKLightingType {
	PerPixel = 1,
	PerVertex = 0,
}
```

### New Type MonoMac.GLKit.GLKNamedEffect

```
public abstract class GLKNamedEffect : MonoMac.Foundation.NSObject, IGLKNamedEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKNamedEffect ();
	public GLKNamedEffect (MonoMac.Foundation.NSCoder coder);
	public GLKNamedEffect (MonoMac.Foundation.NSObjectFlag t);
	public GLKNamedEffect (System.IntPtr handle);
	// methods
	public virtual void PrepareToDraw ();
}
```

### New Type MonoMac.GLKit.GLKNamedEffect_Extensions

```
public static class GLKNamedEffect_Extensions {
}
```

### New Type MonoMac.GLKit.GLKReflectionMapEffect

```
public class GLKReflectionMapEffect : MonoMac.GLKit.GLKBaseEffect, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKReflectionMapEffect ();
	public GLKReflectionMapEffect (MonoMac.Foundation.NSCoder coder);
	public GLKReflectionMapEffect (MonoMac.Foundation.NSObjectFlag t);
	public GLKReflectionMapEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Matrix3d Matrix { get; set; }
	public virtual GLKEffectPropertyTexture TextureCubeMap { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void PrepareToDraw ();
}
```

### New Type MonoMac.GLKit.GLKSkyboxEffect

```
public class GLKSkyboxEffect : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKSkyboxEffect ();
	public GLKSkyboxEffect (MonoMac.Foundation.NSCoder coder);
	public GLKSkyboxEffect (MonoMac.Foundation.NSObjectFlag t);
	public GLKSkyboxEffect (System.IntPtr handle);
	// properties
	public virtual MonoMac.OpenGL.Vector3 Center { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Label { get; set; }
	public virtual GLKEffectPropertyTexture TextureCubeMap { get; }
	public virtual GLKEffectPropertyTransform Transform { get; }
	public virtual float XSize { get; set; }
	public virtual float YSize { get; set; }
	public virtual float ZSize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Draw ();
	public virtual void PrepareToDraw ();
}
```

### New Type MonoMac.GLKit.GLKTextureEnvMode

```
[Serializable]
public enum GLKTextureEnvMode {
	Decal = 2,
	Modulate = 1,
	Replace = 0,
}
```

### New Type MonoMac.GLKit.GLKTextureInfo

```
public class GLKTextureInfo : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKTextureInfo ();
	public GLKTextureInfo (MonoMac.Foundation.NSCoder coder);
	public GLKTextureInfo (MonoMac.Foundation.NSObjectFlag t);
	public GLKTextureInfo (System.IntPtr handle);
	// properties
	public virtual GLKTextureInfoAlphaState AlphaState { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ContainsMipmaps { get; }
	public virtual int Height { get; }
	public virtual uint Name { get; }
	public virtual GLKTextureTarget Target { get; }
	public virtual GLKTextureInfoOrigin TextureOrigin { get; }
	public virtual int Width { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
}
```

### New Type MonoMac.GLKit.GLKTextureInfoAlphaState

```
[Serializable]
public enum GLKTextureInfoAlphaState {
	None = 0,
	NonPremultiplied = 1,
	Premultiplied = 2,
}
```

### New Type MonoMac.GLKit.GLKTextureInfoOrigin

```
[Serializable]
public enum GLKTextureInfoOrigin {
	BottomLeft = 2,
	TopLeft = 1,
	Unknown = 0,
}
```

### New Type MonoMac.GLKit.GLKTextureLoader

```
public class GLKTextureLoader : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKTextureLoader ();
	public GLKTextureLoader (MonoMac.Foundation.NSCoder coder);
	public GLKTextureLoader (MonoMac.Foundation.NSObjectFlag t);
	public GLKTextureLoader (System.IntPtr handle);
	// properties
	public static MonoMac.Foundation.NSString ApplyPremultiplication { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString ErrorDomain { get; }
	public static MonoMac.Foundation.NSString ErrorKey { get; }
	public static MonoMac.Foundation.NSString GenerateMipmaps { get; }
	public static MonoMac.Foundation.NSString GLErrorKey { get; }
	public static MonoMac.Foundation.NSString GrayscaleAsAlpha { get; }
	public static MonoMac.Foundation.NSString OriginBottomLeft { get; }
	public static MonoMac.Foundation.NSString SRGB { get; }
	// methods
	public virtual void BeginLoadCubeMap (string fileName, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (MonoMac.Foundation.NSUrl filePath, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string[] files, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (MonoMac.Foundation.NSUrl[] urls, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string[] files, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (MonoMac.Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string fileName, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginLoadCubeMap (MonoMac.Foundation.NSUrl filePath, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginLoadCubeMapAsync (MonoMac.Foundation.NSUrl filePath, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginLoadCubeMapAsync (string fileName, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public void BeginTextureLoad (MonoMac.CoreGraphics.CGImage image, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (MonoMac.Foundation.NSData data, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (MonoMac.Foundation.NSUrl filePath, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (MonoMac.Foundation.NSUrl filePath, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (string file, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (MonoMac.CoreGraphics.CGImage image, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (string file, GLKTextureOperations textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (string file, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (MonoMac.CoreGraphics.CGImage image, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (MonoMac.Foundation.NSUrl filePath, MonoMac.Foundation.NSDictionary textureOperations, MonoMac.CoreFoundation.DispatchQueue queue);
	public static GLKTextureInfo CubeMapFromFile (string path, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFile (string path, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFiles (string[] files, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFiles (string[] files, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrl (MonoMac.Foundation.NSUrl url, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrls (MonoMac.Foundation.NSUrl[] urls, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrls (MonoMac.Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromData (MonoMac.Foundation.NSData data, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromData (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromFile (string path, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromFile (string path, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromImage (MonoMac.CoreGraphics.CGImage cgImage, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromImage (MonoMac.CoreGraphics.CGImage cgImage, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary textureOperations, out MonoMac.Foundation.NSError error);
	public static GLKTextureInfo FromUrl (MonoMac.Foundation.NSUrl url, GLKTextureOperations textureOperations, out MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.GLKit.GLKTextureLoaderCallback

```
public sealed delegate GLKTextureLoaderCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GLKTextureLoaderCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (GLKTextureInfo textureInfo, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (GLKTextureInfo textureInfo, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.GLKit.GLKTextureLoaderError

```
[Serializable]
public enum GLKTextureLoaderError {
	AlphaPremultiplicationFailure = 16,
	CompressedTextureUpload = 7,
	CubeMapInvalidNumFiles = 6,
	DataPreprocessingFailure = 12,
	FileOrURLNotFound = 0,
	IncompatibleFormatSRGB = 18,
	InvalidCGImage = 2,
	InvalidEAGLContext = 17,
	InvalidNSData = 1,
	MipmapUnsupported = 13,
	PVRAtlasUnsupported = 5,
	ReorientationFailure = 15,
	UncompressedTextureUpload = 8,
	UnknownFileType = 4,
	UnknownPathType = 3,
	UnsupportedBitDepth = 10,
	UnsupportedCubeMapDimensions = 9,
	UnsupportedOrientation = 14,
	UnsupportedPVRFormat = 11,
}
```

### New Type MonoMac.GLKit.GLKTextureOperations

```
public class GLKTextureOperations : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public GLKTextureOperations ();
	public GLKTextureOperations (MonoMac.Foundation.NSDictionary options);
	// properties
	public bool? ApplyPremultiplication { get; set; }
	public bool? GenerateMipmaps { get; set; }
	public bool? GrayscaleAsAlpha { get; set; }
	public bool? OriginBottomLeft { get; set; }
	public bool? SRGB { get; set; }
}
```

### New Type MonoMac.GLKit.GLKTextureTarget

```
[Serializable]
public enum GLKTextureTarget {
	CubeMap = 34067,
	TargetCt = 2,
	Texture2D = 3553,
}
```

### New Type MonoMac.GLKit.GLKVertexAttrib

```
[Serializable]
public enum GLKVertexAttrib {
	Color = 2,
	Normal = 1,
	Position = 0,
	TexCoord0 = 3,
	TexCoord1 = 4,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableColorFormat

```
[Serializable]
public enum GLKViewDrawableColorFormat {
	RGB565 = 1,
	RGBA8888 = 0,
	SRGBA8888 = 2,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableDepthFormat

```
[Serializable]
public enum GLKViewDrawableDepthFormat {
	Format16 = 1,
	Format24 = 2,
	None = 0,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableMultisample

```
[Serializable]
public enum GLKViewDrawableMultisample {
	None = 0,
	Sample4x = 1,
}
```

### New Type MonoMac.GLKit.GLKViewDrawableStencilFormat

```
[Serializable]
public enum GLKViewDrawableStencilFormat {
	Format8 = 1,
	FormatNone = 0,
}
```

### New Type MonoMac.GLKit.IGLKNamedEffect

```
public interface IGLKNamedEffect : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void PrepareToDraw ();
}
```

## New Namespace MonoMac.JavaScriptCore

### New Type MonoMac.JavaScriptCore.IJSExport

```
public interface IJSExport : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.JavaScriptCore.JSClassAttributes

```
[Serializable]
[Flags]
public enum JSClassAttributes {
	NoAutomaticPrototype = 2,
	None = 0,
}
```

### New Type MonoMac.JavaScriptCore.JSContext

```
public class JSContext : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSContext (MonoMac.Foundation.NSCoder coder);
	public JSContext (MonoMac.Foundation.NSObjectFlag t);
	public JSContext (System.IntPtr handle);
	public JSContext ();
	public JSContext (JSVirtualMachine virtualMachine);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static JSValue[] CurrentArguments { get; }
	public static JSValue CurrentCallee { get; }
	public static JSContext CurrentContext { get; }
	public static JSValue CurrentThis { get; }
	public virtual JSValue Exception { get; set; }
	public virtual JSContextExceptionHandler ExceptionHandler { get; set; }
	public virtual JSValue GlobalObject { get; }
	public JSValue Item { get; set; }
	public virtual System.IntPtr JSGlobalContextRefPtr { get; }
	public virtual string Name { get; set; }
	public virtual JSVirtualMachine VirtualMachine { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual JSValue EvaluateScript (string script, MonoMac.Foundation.NSUrl sourceUrl);
	public virtual JSValue EvaluateScript (string script);
	public static JSContext FromJSGlobalContextRef (System.IntPtr nativeJsGlobalContextRef);
}
```

### New Type MonoMac.JavaScriptCore.JSContextExceptionHandler

```
public sealed delegate JSContextExceptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public JSContextExceptionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (JSContext context, JSValue exception, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (JSContext context, JSValue exception);
}
```

### New Type MonoMac.JavaScriptCore.JSExport

```
public class JSExport : MonoMac.Foundation.NSObject, IJSExport, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSExport ();
	public JSExport (MonoMac.Foundation.NSCoder coder);
	public JSExport (MonoMac.Foundation.NSObjectFlag t);
	public JSExport (System.IntPtr handle);
}
```

### New Type MonoMac.JavaScriptCore.JSExport_Extensions

```
public static class JSExport_Extensions {
}
```

### New Type MonoMac.JavaScriptCore.JSManagedValue

```
public class JSManagedValue : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSManagedValue ();
	public JSManagedValue (MonoMac.Foundation.NSCoder coder);
	public JSManagedValue (MonoMac.Foundation.NSObjectFlag t);
	public JSManagedValue (System.IntPtr handle);
	public JSManagedValue (JSValue value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual JSValue Value { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static JSManagedValue Get (JSValue value);
	public static JSManagedValue Get (JSValue value, MonoMac.Foundation.NSObject owner);
}
```

### New Type MonoMac.JavaScriptCore.JSPropertyAttributes

```
[Serializable]
[Flags]
public enum JSPropertyAttributes {
	DontDelete = 8,
	DontEnum = 4,
	None = 0,
	ReadOnly = 2,
}
```

### New Type MonoMac.JavaScriptCore.JSPropertyDescriptorKeys

```
public static class JSPropertyDescriptorKeys {
	// properties
	public static MonoMac.Foundation.NSString Configurable { get; }
	public static MonoMac.Foundation.NSString Enumerable { get; }
	public static MonoMac.Foundation.NSString Get { get; }
	public static MonoMac.Foundation.NSString Set { get; }
	public static MonoMac.Foundation.NSString Value { get; }
	public static MonoMac.Foundation.NSString Writable { get; }
}
```

### New Type MonoMac.JavaScriptCore.JSType

```
[Serializable]
public enum JSType {
	Boolean = 2,
	Null = 1,
	Number = 3,
	Object = 5,
	String = 4,
	Undefined = 0,
}
```

### New Type MonoMac.JavaScriptCore.JSValue

```
public class JSValue : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSValue (MonoMac.Foundation.NSCoder coder);
	public JSValue (MonoMac.Foundation.NSObjectFlag t);
	public JSValue (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual JSContext Context { get; }
	public virtual bool IsBoolean { get; }
	public virtual bool IsNull { get; }
	public virtual bool IsNumber { get; }
	public virtual bool IsObject { get; }
	public virtual bool IsString { get; }
	public virtual bool IsUndefined { get; }
	public JSValue Item { get; set; }
	public JSValue Item { get; set; }
	public virtual System.IntPtr JSValueRefPtr { get; }
	// methods
	public virtual JSValue Call (JSValue[] arguments);
	public virtual JSValue Construct (JSValue[] arguments);
	public static JSValue CreateArray (JSContext context);
	public static JSValue CreateError (string message, JSContext context);
	public static JSValue CreateObject (JSContext context);
	public static JSValue CreateRegularExpression (string pattern, string flags, JSContext context);
	public virtual void DefineProperty (string property, MonoMac.Foundation.NSObject descriptor);
	public virtual bool DeleteProperty (string property);
	protected override void Dispose (bool disposing);
	public static JSValue From (MonoMac.Foundation.NSRange range, JSContext context);
	public static JSValue From (System.Drawing.RectangleF rect, JSContext context);
	public static JSValue From (System.Drawing.SizeF size, JSContext context);
	public static JSValue From (string value, JSContext context);
	public static JSValue From (System.Drawing.PointF point, JSContext context);
	public static JSValue From (uint value, JSContext context);
	public static JSValue From (int value, JSContext context);
	public static JSValue From (double value, JSContext context);
	public static JSValue From (bool value, JSContext context);
	public static JSValue From (MonoMac.Foundation.NSObject value, JSContext context);
	public static JSValue FromJSJSValueRef (System.IntPtr nativeJsValueRefvalue, JSContext context);
	public virtual JSValue GetProperty (string property);
	public virtual JSValue GetValueAt (uint index);
	public virtual bool HasProperty (string property);
	public virtual JSValue Invoke (string method, JSValue[] arguments);
	public virtual bool IsEqualTo (MonoMac.Foundation.NSObject value);
	public virtual bool IsEqualWithTypeCoercionTo (MonoMac.Foundation.NSObject value);
	public virtual bool IsInstanceOf (MonoMac.Foundation.NSObject value);
	public static JSValue Null (JSContext context);
	public virtual void SetProperty (MonoMac.Foundation.NSObject value, string property);
	public virtual void SetValue (JSValue value, uint index);
	public virtual JSValue[] ToArray ();
	public virtual bool ToBool ();
	public virtual MonoMac.Foundation.NSDate ToDate ();
	public virtual MonoMac.Foundation.NSDictionary ToDictionary ();
	public virtual double ToDouble ();
	public virtual int ToInt32 ();
	public virtual MonoMac.Foundation.NSNumber ToNumber ();
	public virtual MonoMac.Foundation.NSObject ToObject ();
	public virtual MonoMac.Foundation.NSObject ToObject (MonoMac.ObjCRuntime.Class ofExpectedClass);
	public virtual System.Drawing.PointF ToPoint ();
	public virtual MonoMac.Foundation.NSRange ToRange ();
	public virtual System.Drawing.RectangleF ToRect ();
	public virtual System.Drawing.SizeF ToSize ();
	public override string ToString ();
	public virtual uint ToUInt32 ();
	public static JSValue Undefined (JSContext context);
}
```

### New Type MonoMac.JavaScriptCore.JSVirtualMachine

```
public class JSVirtualMachine : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public JSVirtualMachine (MonoMac.Foundation.NSCoder coder);
	public JSVirtualMachine (MonoMac.Foundation.NSObjectFlag t);
	public JSVirtualMachine (System.IntPtr handle);
	public JSVirtualMachine ();
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void AddManagedReference (MonoMac.Foundation.NSObject obj, MonoMac.Foundation.NSObject owner);
	public virtual void RemoveManagedReference (MonoMac.Foundation.NSObject obj, MonoMac.Foundation.NSObject owner);
}
```

## New Namespace MonoMac.LocalAuthentication

### New Type MonoMac.LocalAuthentication.LAContext

```
public class LAContext : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public LAContext ();
	public LAContext (MonoMac.Foundation.NSCoder coder);
	public LAContext (MonoMac.Foundation.NSObjectFlag t);
	public LAContext (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedFallbackTitle { get; set; }
	// methods
	public virtual bool CanEvaluatePolicy (LAPolicy policy, MonoMac.Foundation.NSError error);
	public virtual void EvaluatePolicy (LAPolicy policy, string localizedReason, LAContextReplyHandler reply);
	public virtual System.Threading.Tasks.Task<bool> EvaluatePolicyAsync (LAPolicy policy, string localizedReason);
}
```

### New Type MonoMac.LocalAuthentication.LAContextReplyHandler

```
public sealed delegate LAContextReplyHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public LAContextReplyHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool success, MonoMac.Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool success, MonoMac.Foundation.NSError error);
}
```

### New Type MonoMac.LocalAuthentication.LAPolicy

```
[Serializable]
public enum LAPolicy {
	DeviceOwnerAuthenticationWithBiometrics = 1,
}
```

### New Type MonoMac.LocalAuthentication.LAStatus

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

## New Namespace MonoMac.SpriteKit

### New Type MonoMac.SpriteKit.ISKPhysicsContactDelegate

```
public interface ISKPhysicsContactDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SpriteKit.ISKSceneDelegate

```
public interface ISKSceneDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.SpriteKit.SK3DNode

```
public class SK3DNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SK3DNode ();
	public SK3DNode (MonoMac.Foundation.NSCoder coder);
	public SK3DNode (MonoMac.Foundation.NSObjectFlag t);
	public SK3DNode (System.IntPtr handle);
	public SK3DNode (System.Drawing.SizeF viewportSize);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Loops { get; set; }
	public virtual bool Playing { get; set; }
	public virtual MonoMac.SceneKit.SCNNode PointOfView { get; set; }
	public virtual double SceneTime { get; set; }
	public virtual MonoMac.SceneKit.SCNScene ScnScene { get; set; }
	public virtual System.Drawing.SizeF ViewportSize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SK3DNode FromViewportSize (System.Drawing.SizeF viewportSize);
	public virtual MonoMac.SceneKit.SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
	public MonoMac.SceneKit.SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.SceneKit.SCNHitTestOptions options);
	public virtual MonoMac.OpenGL.Vector3 ProjectPoint (MonoMac.OpenGL.Vector3 point);
	public virtual MonoMac.OpenGL.Vector3 UnprojectPoint (MonoMac.OpenGL.Vector3 point);
}
```

### New Type MonoMac.SpriteKit.SKAction

```
public class SKAction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKAction (MonoMac.Foundation.NSCoder coder);
	public SKAction (MonoMac.Foundation.NSObjectFlag t);
	public SKAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double Duration { get; set; }
	public virtual SKAction ReversedAction { get; }
	public virtual float Speed { get; set; }
	public virtual SKActionTimingMode TimingMode { get; set; }
	// methods
	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec);
	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec, bool resize, bool restore);
	public static SKAction ColorizeWithColor (MonoMac.AppKit.NSColor color, float colorBlendFactor, double sec);
	public static SKAction ColorizeWithColorBlendFactor (float colorBlendFactor, double sec);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SKAction CustomActionWithDuration (double seconds, SKActionDurationHandler actionHandler);
	protected override void Dispose (bool disposing);
	public static SKAction FadeAlphaBy (float factor, double sec);
	public static SKAction FadeAlphaTo (float alpha, double sec);
	public static SKAction FadeInWithDuration (double sec);
	public static SKAction FadeOutWithDuration (double sec);
	public static SKAction Falloff (float to, double duration);
	public static SKAction FollowPath (MonoMac.CoreGraphics.CGPath path, bool offset, bool orient, float speed);
	public static SKAction FollowPath (MonoMac.CoreGraphics.CGPath path, float speed);
	public static SKAction FollowPath (MonoMac.CoreGraphics.CGPath path, bool offset, bool orient, double sec);
	public static SKAction FollowPath (MonoMac.CoreGraphics.CGPath path, double sec);
	public static SKAction Group (SKAction[] actions);
	public static SKAction Hide ();
	public static SKAction MoveBy (float deltaX, float deltaY, double sec);
	public static SKAction MoveBy (MonoMac.CoreGraphics.CGVector delta, double duration);
	public static SKAction MoveTo (System.Drawing.PointF location, double sec);
	public static SKAction MoveToX (float x, double sec);
	public static SKAction MoveToY (float y, double sec);
	public static SKAction PerformSelector (MonoMac.ObjCRuntime.Selector selector, MonoMac.Foundation.NSObject target);
	public static SKAction PlaySoundFileNamed (string soundFile, bool wait);
	public static SKAction ReachTo (System.Drawing.PointF position, SKNode rootNode, double secs);
	public static SKAction ReachTo (System.Drawing.PointF position, SKNode rootNode, float velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, float velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, double sec);
	public static SKAction RemoveFromParent ();
	public static SKAction RepeatAction (SKAction action, uint count);
	public static SKAction RepeatActionForever (SKAction action);
	public static SKAction ResizeByWidth (float width, float height, double duration);
	public static SKAction ResizeTo (float width, float height, double duration);
	public static SKAction ResizeTo (System.Drawing.SizeF size, double duration);
	public static SKAction ResizeToHeight (float height, double duration);
	public static SKAction ResizeToWidth (float width, double duration);
	public static SKAction RotateByAngle (float radians, double sec);
	public static SKAction RotateToAngle (float radians, double sec, bool shortedUnitArc);
	public static SKAction RotateToAngle (float radians, double sec);
	public static SKAction Run (System.Action block, MonoMac.CoreFoundation.DispatchQueue queue);
	public static SKAction Run (System.Action block);
	public static SKAction RunAction (SKAction action, string name);

	[Obsolete ("Use Run(Action) instead")]
	public static SKAction RunBlock (System.Action block);

	[Obsolete ("Use Run(Action,DispatchQueue) instead")]
	public static SKAction RunBlock (System.Action block, MonoMac.CoreFoundation.DispatchQueue queue);
	public static SKAction ScaleBy (float scale, double sec);
	public static SKAction ScaleBy (float xScale, float yScale, double sec);
	public static SKAction ScaleTo (float xScale, float yScale, double sec);
	public static SKAction ScaleTo (float scale, double sec);
	public static SKAction ScaleXTo (float scale, double sec);
	public static SKAction ScaleYTo (float scale, double sec);
	public static SKAction Sequence (SKAction[] actions);
	public static SKAction SetTexture (SKTexture texture);
	public static SKAction SetTexture (SKTexture texture, bool resize);
	public virtual void SetTimingFunction (SKActionTimingFunction timingFunction);
	public static SKAction SpeedBy (float speed, double sec);
	public static SKAction SpeedTo (float speed, double sec);
	public static SKAction StrengthBy (float strength, double sec);
	public static SKAction StrengthTo (float strength, double sec);
	public static SKAction Unhide ();
	public static SKAction WaitForDuration (double sec, double durationRange);
	public static SKAction WaitForDuration (double sec);
}
```

### New Type MonoMac.SpriteKit.SKActionDurationHandler

```
public sealed delegate SKActionDurationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKActionDurationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKNode node, float elapsedTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (SKNode node, float elapsedTime);
}
```

### New Type MonoMac.SpriteKit.SKActionTimingFunction

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

### New Type MonoMac.SpriteKit.SKActionTimingMode

```
[Serializable]
public enum SKActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type MonoMac.SpriteKit.SKBlendMode

```
[Serializable]
public enum SKBlendMode {
	Add = 1,
	Alpha = 0,
	Multiply = 3,
	MultiplyX2 = 4,
	Replace = 6,
	Screen = 5,
	Subtract = 2,
}
```

### New Type MonoMac.SpriteKit.SKConstraint

```
public class SKConstraint : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKConstraint ();
	public SKConstraint (MonoMac.Foundation.NSCoder coder);
	public SKConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SKConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual SKNode ReferenceNode { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
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

### New Type MonoMac.SpriteKit.SKCropNode

```
public class SKCropNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKCropNode ();
	public SKCropNode (MonoMac.Foundation.NSCoder coder);
	public SKCropNode (MonoMac.Foundation.NSObjectFlag t);
	public SKCropNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SKNode MaskNode { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKEffectNode

```
public class SKEffectNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKEffectNode ();
	public SKEffectNode (MonoMac.Foundation.NSCoder coder);
	public SKEffectNode (MonoMac.Foundation.NSObjectFlag t);
	public SKEffectNode (System.IntPtr handle);
	// properties
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreImage.CIFilter Filter { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual bool ShouldCenterFilter { get; set; }
	public virtual bool ShouldEnableEffects { get; set; }
	public virtual bool ShouldRasterize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKEmitterNode

```
public class SKEmitterNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKEmitterNode ();
	public SKEmitterNode (MonoMac.Foundation.NSCoder coder);
	public SKEmitterNode (MonoMac.Foundation.NSObjectFlag t);
	public SKEmitterNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float EmissionAngle { get; set; }
	public virtual float EmissionAngleRange { get; set; }
	public virtual uint FieldBitMask { get; set; }
	public virtual uint NumParticlesToEmit { get; set; }
	public virtual SKAction ParticleAction { get; set; }
	public virtual float ParticleAlpha { get; set; }
	public virtual float ParticleAlphaRange { get; set; }
	public virtual SKKeyframeSequence ParticleAlphaSequence { get; set; }
	public virtual float ParticleAlphaSpeed { get; set; }
	public virtual float ParticleBirthRate { get; set; }
	public virtual SKBlendMode ParticleBlendMode { get; set; }
	public virtual MonoMac.AppKit.NSColor ParticleColor { get; set; }
	public virtual float ParticleColorAlphaRange { get; set; }
	public virtual float ParticleColorAlphaSpeed { get; set; }
	public virtual float ParticleColorBlendFactor { get; set; }
	public virtual float ParticleColorBlendFactorRange { get; set; }
	public virtual SKKeyframeSequence ParticleColorBlendFactorSequence { get; set; }
	public virtual float ParticleColorBlendFactorSpeed { get; set; }
	public virtual float ParticleColorBlueRange { get; set; }
	public virtual float ParticleColorBlueSpeed { get; set; }
	public virtual float ParticleColorGreenRange { get; set; }
	public virtual float ParticleColorGreenSpeed { get; set; }
	public virtual float ParticleColorRedRange { get; set; }
	public virtual float ParticleColorRedSpeed { get; set; }
	public virtual SKKeyframeSequence ParticleColorSequence { get; set; }
	public virtual float ParticleLifetime { get; set; }
	public virtual float ParticleLifetimeRange { get; set; }
	public virtual System.Drawing.PointF ParticlePosition { get; set; }
	public virtual MonoMac.CoreGraphics.CGVector ParticlePositionRange { get; set; }
	public virtual float ParticleRotation { get; set; }
	public virtual float ParticleRotationRange { get; set; }
	public virtual float ParticleRotationSpeed { get; set; }
	public virtual float ParticleScale { get; set; }
	public virtual float ParticleScaleRange { get; set; }
	public virtual SKKeyframeSequence ParticleScaleSequence { get; set; }
	public virtual float ParticleScaleSpeed { get; set; }
	public virtual System.Drawing.SizeF ParticleSize { get; set; }
	public virtual float ParticleSpeed { get; set; }
	public virtual float ParticleSpeedRange { get; set; }
	public virtual SKTexture ParticleTexture { get; set; }
	public virtual float ParticleZPosition { get; set; }
	public virtual float ParticleZPositionRange { get; set; }
	public virtual float ParticleZPositionSpeed { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual SKNode TargetNode { get; set; }
	public virtual float XAcceleration { get; set; }
	public virtual float YAcceleration { get; set; }
	// methods
	public virtual void AdvanceSimulationTime (double sec);
	protected override void Dispose (bool disposing);
	public virtual void ResetSimulation ();
}
```

### New Type MonoMac.SpriteKit.SKFieldForceEvaluator

```
public sealed delegate SKFieldForceEvaluator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKFieldForceEvaluator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.OpenGL.Vector4 position, MonoMac.OpenGL.Vector4 velocity, float mass, float charge, double time, System.AsyncCallback callback, object object);
	public virtual MonoMac.OpenGL.Vector3 EndInvoke (System.IAsyncResult result);
	public virtual MonoMac.OpenGL.Vector3 Invoke (MonoMac.OpenGL.Vector4 position, MonoMac.OpenGL.Vector4 velocity, float mass, float charge, double time);
}
```

### New Type MonoMac.SpriteKit.SKFieldNode

```
public class SKFieldNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKFieldNode ();
	public SKFieldNode (MonoMac.Foundation.NSCoder coder);
	public SKFieldNode (MonoMac.Foundation.NSObjectFlag t);
	public SKFieldNode (System.IntPtr handle);
	// properties
	public virtual float AnimationSpeed { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Vector4 Direction { get; set; }
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
	public static SKFieldNode CreateLinearGravityField (MonoMac.OpenGL.Vector4 direction);
	public static SKFieldNode CreateMagneticField ();
	public static SKFieldNode CreateNoiseField (float smoothness, float speed);
	public static SKFieldNode CreateRadialGravityField ();
	public static SKFieldNode CreateSpringField ();
	public static SKFieldNode CreateTurbulenceField (float smoothness, float speed);
	public static SKFieldNode CreateVelocityField (MonoMac.OpenGL.Vector4 direction);
	public static SKFieldNode CreateVelocityField (SKTexture velocityTexture);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKInterpolationMode

```
[Serializable]
public enum SKInterpolationMode {
	Linear = 1,
	Spline = 2,
	Step = 3,
}
```

### New Type MonoMac.SpriteKit.SKKeyframeSequence

```
public class SKKeyframeSequence : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKKeyframeSequence ();
	public SKKeyframeSequence (MonoMac.Foundation.NSObject[] values, float[] times);
	public SKKeyframeSequence (MonoMac.Foundation.NSObject[] values, MonoMac.Foundation.NSNumber[] times);
	public SKKeyframeSequence (uint numItems);
	public SKKeyframeSequence (System.IntPtr handle);
	public SKKeyframeSequence (MonoMac.Foundation.NSObjectFlag t);
	public SKKeyframeSequence (MonoMac.Foundation.NSCoder coder);
	public SKKeyframeSequence (MonoMac.Foundation.NSObject[] values, double[] times);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual uint Count { get; }
	public virtual SKInterpolationMode InterpolationMode { get; set; }
	public virtual SKRepeatMode RepeatMode { get; set; }
	// methods
	public virtual void AddKeyframeValue (MonoMac.Foundation.NSObject value, float time);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual float GetKeyframeTime (uint index);
	public virtual MonoMac.Foundation.NSObject GetKeyframeValue (uint index);
	public virtual void RemoveKeyframe (uint index);
	public virtual void RemoveLastKeyframe ();
	public virtual MonoMac.Foundation.NSObject SampleAtTime (float time);
	public virtual void SetKeyframeTime (float time, uint index);
	public virtual void SetKeyframeValue (MonoMac.Foundation.NSObject value, uint index);
	public virtual void SetKeyframeValue (MonoMac.Foundation.NSObject value, float time, uint index);
}
```

### New Type MonoMac.SpriteKit.SKLabelHorizontalAlignmentMode

```
[Serializable]
public enum SKLabelHorizontalAlignmentMode {
	Center = 0,
	Left = 1,
	Right = 2,
}
```

### New Type MonoMac.SpriteKit.SKLabelNode

```
public class SKLabelNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKLabelNode ();
	public SKLabelNode (MonoMac.Foundation.NSCoder coder);
	public SKLabelNode (MonoMac.Foundation.NSObjectFlag t);
	public SKLabelNode (System.IntPtr handle);
	public SKLabelNode (string fontName);
	// properties
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.AppKit.NSColor Color { get; set; }
	public virtual float ColorBlendFactor { get; set; }
	public virtual MonoMac.AppKit.NSColor FontColor { get; set; }
	public virtual string FontName { get; set; }
	public virtual float FontSize { get; set; }
	public virtual SKLabelHorizontalAlignmentMode HorizontalAlignmentMode { get; set; }
	public virtual string Text { get; set; }
	public virtual SKLabelVerticalAlignmentMode VerticalAlignmentMode { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SKLabelNode FromFont (string fontName);
	public static SKLabelNode FromText (string text);
}
```

### New Type MonoMac.SpriteKit.SKLabelVerticalAlignmentMode

```
[Serializable]
public enum SKLabelVerticalAlignmentMode {
	Baseline = 0,
	Bottom = 3,
	Center = 1,
	Top = 2,
}
```

### New Type MonoMac.SpriteKit.SKLightNode

```
public class SKLightNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKLightNode ();
	public SKLightNode (MonoMac.Foundation.NSCoder coder);
	public SKLightNode (MonoMac.Foundation.NSObjectFlag t);
	public SKLightNode (System.IntPtr handle);
	// properties
	public virtual MonoMac.AppKit.NSColor AmbientColor { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual float Falloff { get; set; }
	public virtual MonoMac.AppKit.NSColor LightColor { get; set; }
	public virtual MonoMac.AppKit.NSColor ShadowColor { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKMutableTexture

```
public class SKMutableTexture : MonoMac.SpriteKit.SKTexture, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKMutableTexture (MonoMac.Foundation.NSCoder coder);
	public SKMutableTexture (MonoMac.Foundation.NSObjectFlag t);
	public SKMutableTexture (System.IntPtr handle);
	public SKMutableTexture (System.Drawing.SizeF size);
	public SKMutableTexture (System.Drawing.SizeF size, MonoMac.CoreVideo.CVPixelFormatType pixelFormat);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SKMutableTexture Create (System.Drawing.SizeF size);
	public virtual void ModifyPixelData (SKTextureModify modifyMethod);
}
```

### New Type MonoMac.SpriteKit.SKNode

```
public class SKNode : MonoMac.AppKit.NSResponder, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKNode ();
	public SKNode (MonoMac.Foundation.NSCoder coder);
	public SKNode (MonoMac.Foundation.NSObjectFlag t);
	public SKNode (System.IntPtr handle);
	// properties
	public virtual float Alpha { get; set; }
	public virtual SKNode[] Children { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SKConstraint[] Constraints { get; set; }
	public virtual System.Drawing.RectangleF Frame { get; }
	public virtual bool HasActions { get; }
	public virtual bool Hidden { get; set; }
	public virtual string Name { get; set; }
	public virtual SKNode Parent { get; }
	public virtual bool Paused { get; set; }
	public virtual SKPhysicsBody PhysicsBody { get; set; }
	public virtual System.Drawing.PointF Position { get; set; }
	public virtual SKReachConstraints ReachConstraints { get; set; }
	public virtual float Scale { set; }
	public virtual SKScene Scene { get; }
	public virtual float Speed { get; set; }
	public virtual MonoMac.Foundation.NSMutableDictionary UserData { get; set; }
	public virtual bool UserInteractionEnabled { get; set; }
	public virtual float XScale { get; set; }
	public virtual float YScale { get; set; }
	public virtual float ZPosition { get; set; }
	public virtual float ZRotation { get; set; }
	// methods
	public void Add (SKNode node);
	public virtual void AddChild (SKNode node);
	public void AddNodes (SKNode[] nodes);
	public virtual System.Drawing.RectangleF CalculateAccumulatedFrame ();
	public virtual bool ContainsPoint (System.Drawing.PointF point);
	public virtual System.Drawing.PointF ConvertPointFromNode (System.Drawing.PointF point, SKNode sourceNode);
	public virtual System.Drawing.PointF ConvertPointToNode (System.Drawing.PointF point, SKNode sourceNode);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SKNode Create ();
	protected override void Dispose (bool disposing);
	public virtual void EnumerateChildNodes (string name, SKNodeChildEnumeratorHandler enumerationHandler);
	public static SKNode FromFile (string file);
	public virtual SKAction GetActionForKey (string key);
	public virtual SKNode GetChildNode (string name);
	public virtual System.Collections.Generic.IEnumerator<SKNode> GetEnumerator ();
	public virtual SKNode GetNodeAtPoint (System.Drawing.PointF point);
	public virtual SKNode[] GetNodesAtPoint (System.Drawing.PointF point);
	public virtual SKNode GetObjectsMatching (string nameExpression);
	public virtual bool InParentHierarchy (SKNode node);
	public virtual void InsertChild (SKNode node, int index);
	public virtual bool IntersectsNode (SKNode node);
	public virtual void RemoveActionForKey (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllChildren ();
	public virtual void RemoveChildren (SKNode[] nodes);
	public virtual void RemoveFromParent ();
	public virtual void RunAction (SKAction action, string key);
	public virtual void RunAction (SKAction action);
	public virtual void RunAction (SKAction action, System.Action completionHandler);
}
```

### New Type MonoMac.SpriteKit.SKNodeChildEnumeratorHandler

```
public sealed delegate SKNodeChildEnumeratorHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKNodeChildEnumeratorHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKNode node, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (SKNode node, out bool stop);
}
```

### New Type MonoMac.SpriteKit.SKNodeEvent_NSEvent

```
public static class SKNodeEvent_NSEvent {
	// methods
	public static System.Drawing.PointF LocationInNode (MonoMac.AppKit.NSEvent This, SKNode node);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsBody

```
public class SKPhysicsBody : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsBody (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsBody (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsBody (System.IntPtr handle);
	// properties
	public virtual bool AffectedByGravity { get; set; }
	public virtual SKPhysicsBody[] AllContactedBodies { get; }
	public virtual bool AllowsRotation { get; set; }
	public virtual float AngularDamping { get; set; }
	public virtual float AngularVelocity { get; set; }
	public virtual float Area { get; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual float Charge { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint CollisionBitMask { get; set; }
	public virtual uint ContactTestBitMask { get; set; }
	public virtual float Density { get; set; }
	public virtual bool Dynamic { get; set; }
	public virtual uint FieldBitMask { get; set; }
	public virtual float Friction { get; set; }
	public virtual SKPhysicsJoint[] Joints { get; }
	public virtual float LinearDamping { get; set; }
	public virtual float Mass { get; set; }
	public virtual SKNode Node { get; }
	public virtual bool Pinned { get; set; }
	public virtual bool Resting { get; set; }
	public virtual float Restitution { get; set; }
	public virtual bool UsesPreciseCollisionDetection { get; set; }
	public virtual MonoMac.CoreGraphics.CGVector Velocity { get; set; }
	// methods
	public virtual void ApplyAngularImpulse (float impulse);
	public virtual void ApplyForce (MonoMac.CoreGraphics.CGVector force);
	public virtual void ApplyForce (MonoMac.CoreGraphics.CGVector force, System.Drawing.PointF point);
	public virtual void ApplyImpulse (MonoMac.CoreGraphics.CGVector impulse);
	public virtual void ApplyImpulse (MonoMac.CoreGraphics.CGVector impulse, System.Drawing.PointF point);
	public virtual void ApplyTorque (float torque);

	[Obsolete ("Use the method FromBodies instead")]
	public static SKPhysicsBody BodyWithBodies (SKPhysicsBody[] bodies);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius, System.Drawing.PointF center);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius);

	[Obsolete ("Use the CreateEdgeChain method instead")]
	public static SKPhysicsBody BodyWithEdgeChainFromPath (MonoMac.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdge method instead")]
	public static SKPhysicsBody BodyWithEdgeFromPoint (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromPath (MonoMac.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromRect (System.Drawing.RectangleF rect);

	[Obsolete ("Use the CreateBodyFromPath method instead")]
	public static SKPhysicsBody BodyWithPolygonFromPath (MonoMac.CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size, System.Drawing.PointF center);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SKPhysicsBody Create (SKTexture texture, float alphaThreshold, System.Drawing.SizeF size);
	public static SKPhysicsBody Create (SKTexture texture, System.Drawing.SizeF size);
	public static SKPhysicsBody CreateBodyFromPath (MonoMac.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateCircularBody (float radius, System.Drawing.PointF center);
	public static SKPhysicsBody CreateCircularBody (float radius);
	public static SKPhysicsBody CreateEdge (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);
	public static SKPhysicsBody CreateEdgeChain (MonoMac.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateEdgeLoop (System.Drawing.RectangleF rect);
	public static SKPhysicsBody CreateEdgeLoop (MonoMac.CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateRectangularBody (System.Drawing.SizeF size, System.Drawing.PointF center);
	public static SKPhysicsBody CreateRectangularBody (System.Drawing.SizeF size);
	protected override void Dispose (bool disposing);
	public static SKPhysicsBody FromBodies (SKPhysicsBody[] bodies);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsContact

```
public class SKPhysicsContact : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsContact (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsContact (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsContact (System.IntPtr handle);
	// properties
	public virtual SKPhysicsBody BodyA { get; }
	public virtual SKPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float CollisionImpulse { get; }
	public virtual MonoMac.CoreGraphics.CGVector ContactNormal { get; }
	public virtual System.Drawing.PointF ContactPoint { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsContactDelegate

```
public class SKPhysicsContactDelegate : MonoMac.Foundation.NSObject, ISKPhysicsContactDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsContactDelegate ();
	public SKPhysicsContactDelegate (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsContactDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SKPhysicsContact contact);
	public virtual void DidEndContact (SKPhysicsContact contact);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsContactDelegate_Extensions

```
public static class SKPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
	public static void DidEndContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJoint

```
public class SKPhysicsJoint : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJoint ();
	public SKPhysicsJoint (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJoint (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJoint (System.IntPtr handle);
	// properties
	public virtual SKPhysicsBody BodyA { get; set; }
	public virtual SKPhysicsBody BodyB { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreGraphics.CGVector ReactionForce { get; }
	public virtual float ReactionTorque { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJointFixed

```
public class SKPhysicsJointFixed : MonoMac.SpriteKit.SKPhysicsJoint, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointFixed (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJointFixed (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJointFixed (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SKPhysicsJointFixed Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJointLimit

```
public class SKPhysicsJointLimit : MonoMac.SpriteKit.SKPhysicsJoint, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointLimit (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJointLimit (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJointLimit (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float MaxLength { get; set; }
	// methods
	public static SKPhysicsJointLimit Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchorA, System.Drawing.PointF anchorB);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJointPin

```
public class SKPhysicsJointPin : MonoMac.SpriteKit.SKPhysicsJoint, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointPin (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJointPin (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJointPin (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float FrictionTorque { get; set; }
	public virtual float LowerAngleLimit { get; set; }
	public virtual float RotationSpeed { get; set; }
	public virtual bool ShouldEnableLimits { get; set; }
	public virtual float UpperAngleLimit { get; set; }
	// methods
	public static SKPhysicsJointPin Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJointSliding

```
public class SKPhysicsJointSliding : MonoMac.SpriteKit.SKPhysicsJoint, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointSliding (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJointSliding (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJointSliding (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float LowerDistanceLimit { get; set; }
	public virtual bool ShouldEnableLimits { get; set; }
	public virtual float UpperDistanceLimit { get; set; }
	// methods
	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor, MonoMac.CoreGraphics.CGVector axis);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsJointSpring

```
public class SKPhysicsJointSpring : MonoMac.SpriteKit.SKPhysicsJoint, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointSpring (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsJointSpring (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsJointSpring (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Damping { get; set; }
	public virtual float Frequency { get; set; }
	// methods
	public static SKPhysicsJointSpring Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchorA, System.Drawing.PointF anchorB);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsWorld

```
public class SKPhysicsWorld : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsWorld (MonoMac.Foundation.NSCoder coder);
	public SKPhysicsWorld (MonoMac.Foundation.NSObjectFlag t);
	public SKPhysicsWorld (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public SKPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual MonoMac.CoreGraphics.CGVector Gravity { get; set; }
	public virtual float Speed { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler DidBeginContact;
	public event System.EventHandler DidEndContact;
	// methods
	public virtual void AddJoint (SKPhysicsJoint joint);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateBodies (System.Drawing.RectangleF rect, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (System.Drawing.PointF start, System.Drawing.PointF end, SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (System.Drawing.PointF point, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual SKPhysicsBody GetBody (System.Drawing.PointF rayStart, System.Drawing.PointF rayEnd);
	public virtual SKPhysicsBody GetBody (System.Drawing.PointF point);
	public virtual SKPhysicsBody GetBody (System.Drawing.RectangleF rect);
	public virtual void RemoveAllJoints ();
	public virtual void RemoveJoint (SKPhysicsJoint joint);
	public virtual MonoMac.OpenGL.Vector3 SampleFields (MonoMac.OpenGL.Vector3 position);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler

```
public sealed delegate SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKPhysicsBody body, System.Drawing.PointF point, MonoMac.CoreGraphics.CGVector normal, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (SKPhysicsBody body, System.Drawing.PointF point, MonoMac.CoreGraphics.CGVector normal, out bool stop);
}
```

### New Type MonoMac.SpriteKit.SKPhysicsWorldBodiesEnumeratorHandler

```
public sealed delegate SKPhysicsWorldBodiesEnumeratorHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKPhysicsWorldBodiesEnumeratorHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKPhysicsBody body, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (SKPhysicsBody body, out bool stop);
}
```

### New Type MonoMac.SpriteKit.SKRange

```
public class SKRange : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRange ();
	public SKRange (MonoMac.Foundation.NSCoder coder);
	public SKRange (MonoMac.Foundation.NSObjectFlag t);
	public SKRange (System.IntPtr handle);
	public SKRange (float lowerLimit, float upperLimier);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float LowerLimit { get; set; }
	public virtual float UpperLimit { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SKRange Create (float lower, float upper);
	public static SKRange CreateConstant (float value);
	public static SKRange CreateUnlimited ();
	public static SKRange CreateWithLowerLimit (float lower);
	public static SKRange CreateWithUpperLimit (float upper);
	public static SKRange CreateWithVariance (float value, float variance);
}
```

### New Type MonoMac.SpriteKit.SKReachConstraints

```
public class SKReachConstraints : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKReachConstraints ();
	public SKReachConstraints (MonoMac.Foundation.NSCoder coder);
	public SKReachConstraints (MonoMac.Foundation.NSObjectFlag t);
	public SKReachConstraints (System.IntPtr handle);
	public SKReachConstraints (float lowerAngleLimit, float upperAngleLimit);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float LowerAngleLimit { get; set; }
	public virtual float UpperAngleLimit { get; set; }
}
```

### New Type MonoMac.SpriteKit.SKRegion

```
public class SKRegion : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRegion ();
	public SKRegion (MonoMac.Foundation.NSCoder coder);
	public SKRegion (MonoMac.Foundation.NSObjectFlag t);
	public SKRegion (System.IntPtr handle);
	public SKRegion (float radius);
	public SKRegion (System.Drawing.SizeF size);
	public SKRegion (MonoMac.CoreGraphics.CGPath path);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static SKRegion InfiniteRegion { get; }
	public virtual MonoMac.CoreGraphics.CGPath Path { get; }
	// methods
	public virtual bool ContainsPoint (System.Drawing.PointF point);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual SKRegion CreateDifference (SKRegion region);
	public virtual SKRegion CreateIntersection (SKRegion region);
	public virtual SKRegion CreateUnion (SKRegion region);
	public virtual SKRegion InverseRegion ();
}
```

### New Type MonoMac.SpriteKit.SKRepeatMode

```
[Serializable]
public enum SKRepeatMode {
	Clamp = 1,
	Loop = 2,
}
```

### New Type MonoMac.SpriteKit.SKScene

```
public class SKScene : MonoMac.SpriteKit.SKEffectNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKScene ();
	public SKScene (MonoMac.Foundation.NSCoder coder);
	public SKScene (MonoMac.Foundation.NSObjectFlag t);
	public SKScene (System.IntPtr handle);
	public SKScene (System.Drawing.SizeF size);
	// properties
	public virtual System.Drawing.PointF AnchorPoint { get; set; }
	public virtual MonoMac.AppKit.NSColor BackgroundColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public SKSceneDelegate Delegate { get; set; }
	public virtual SKPhysicsWorld PhysicsWorld { get; }
	public virtual SKSceneScaleMode ScaleMode { get; set; }
	public virtual System.Drawing.SizeF Size { get; set; }
	public virtual SKView View { get; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual System.Drawing.PointF ConvertPointFromView (System.Drawing.PointF point);
	public virtual System.Drawing.PointF ConvertPointToView (System.Drawing.PointF point);
	public virtual void DidApplyConstraints ();
	public virtual void DidChangeSize (System.Drawing.SizeF oldSize);
	public virtual void DidEvaluateActions ();
	public virtual void DidFinishUpdate ();
	public virtual void DidMoveToView (SKView view);
	public virtual void DidSimulatePhysics ();
	protected override void Dispose (bool disposing);
	public static SKScene FromSize (System.Drawing.SizeF size);
	public virtual void Update (double currentTime);
	public virtual void WillMoveFromView (SKView view);
}
```

### New Type MonoMac.SpriteKit.SKSceneDelegate

```
public class SKSceneDelegate : MonoMac.Foundation.NSObject, ISKSceneDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKSceneDelegate ();
	public SKSceneDelegate (MonoMac.Foundation.NSCoder coder);
	public SKSceneDelegate (MonoMac.Foundation.NSObjectFlag t);
	public SKSceneDelegate (System.IntPtr handle);
	// methods
	public virtual void DidApplyConstraints (SKScene scene);
	public virtual void DidEvaluateActions (SKScene scene);
	public virtual void DidFinishUpdate (SKScene scene);
	public virtual void DidSimulatePhysics (SKScene scene);
	public virtual void Update (double currentTime, SKScene scene);
}
```

### New Type MonoMac.SpriteKit.SKSceneDelegate_Extensions

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

### New Type MonoMac.SpriteKit.SKSceneScaleMode

```
[Serializable]
public enum SKSceneScaleMode {
	AspectFill = 1,
	AspectFit = 2,
	Fill = 0,
	ResizeFill = 3,
}
```

### New Type MonoMac.SpriteKit.SKShader

```
public class SKShader : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKShader ();
	public SKShader (MonoMac.Foundation.NSCoder coder);
	public SKShader (MonoMac.Foundation.NSObjectFlag t);
	public SKShader (System.IntPtr handle);
	public SKShader (string shaderSourceCode);
	public SKShader (string sharedSourceCode, SKUniform[] uniforms);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Source { get; set; }
	public virtual SKUniform[] Uniforms { get; set; }
	// methods
	public virtual void AddUniform (SKUniform uniform);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SKShader Create ();
	protected override void Dispose (bool disposing);
	public static SKShader FromFile (string name);
	public static SKShader FromShaderSourceCode (string source, SKUniform[] uniforms);
	public static SKShader FromShaderSourceCode (string source);
	public virtual SKUniform GetUniform (string uniformName);
	public virtual void RemoveUniform (string uniforName);
}
```

### New Type MonoMac.SpriteKit.SKShapeNode

```
public class SKShapeNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKShapeNode ();
	public SKShapeNode (MonoMac.Foundation.NSCoder coder);
	public SKShapeNode (MonoMac.Foundation.NSObjectFlag t);
	public SKShapeNode (System.IntPtr handle);
	// properties
	public virtual bool Antialiased { get; set; }
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.AppKit.NSColor FillColor { get; set; }
	public virtual SKShader FillShader { get; set; }
	public virtual SKTexture FillTexture { get; set; }
	public virtual float GlowWidth { get; set; }
	public virtual MonoMac.CoreGraphics.CGLineCap LineCap { get; set; }
	public virtual MonoMac.CoreGraphics.CGLineJoin LineJoin { get; set; }
	public virtual float LineLength { get; }
	public virtual float LineWidth { get; set; }
	public virtual float MiterLimit { get; set; }
	public virtual MonoMac.CoreGraphics.CGPath Path { get; set; }
	public virtual MonoMac.AppKit.NSColor StrokeColor { get; set; }
	public virtual SKShader StrokeShader { get; set; }
	public virtual SKTexture StrokeTexture { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SKShapeNode FromCircle (float radius);
	public static SKShapeNode FromEllipse (System.Drawing.SizeF size);
	public static SKShapeNode FromEllipse (System.Drawing.RectangleF rect);
	public static SKShapeNode FromPath (MonoMac.CoreGraphics.CGPath path);
	public static SKShapeNode FromPath (MonoMac.CoreGraphics.CGPath path, bool centered);
	public static SKShapeNode FromPoints (ref System.Drawing.PointF points, uint numPoints);
	public static SKShapeNode FromRect (System.Drawing.SizeF size);
	public static SKShapeNode FromRect (System.Drawing.RectangleF rect, float cornerRadius);
	public static SKShapeNode FromRect (System.Drawing.SizeF size, float cornerRadius);
	public static SKShapeNode FromRect (System.Drawing.RectangleF rect);
	public static SKShapeNode FromSplinePoints (ref System.Drawing.PointF points, uint numPoints);
}
```

### New Type MonoMac.SpriteKit.SKSpriteNode

```
public class SKSpriteNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKSpriteNode ();
	public SKSpriteNode (string name);
	public SKSpriteNode (SKTexture texture);
	public SKSpriteNode (SKTexture texture, MonoMac.AppKit.NSColor color, System.Drawing.SizeF size);
	public SKSpriteNode (System.IntPtr handle);
	public SKSpriteNode (MonoMac.Foundation.NSObjectFlag t);
	public SKSpriteNode (MonoMac.Foundation.NSCoder coder);
	public SKSpriteNode (MonoMac.AppKit.NSColor color, System.Drawing.SizeF size);
	// properties
	public virtual System.Drawing.PointF AnchorPoint { get; set; }
	public virtual SKBlendMode BlendMode { get; set; }
	public virtual System.Drawing.RectangleF CenterRect { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.AppKit.NSColor Color { get; set; }
	public virtual float ColorBlendFactor { get; set; }
	public virtual uint LightingBitMask { get; set; }
	public virtual SKTexture NormalTexture { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual uint ShadowCastBitMask { get; set; }
	public virtual uint ShadowedBitMask { get; set; }
	public virtual System.Drawing.SizeF Size { get; set; }
	public virtual SKTexture Texture { get; set; }
	// methods
	public static SKSpriteNode Create (SKTexture texture, SKTexture normalMap);
	public static SKSpriteNode Create (string imageName, bool generateNormalMap);
	protected override void Dispose (bool disposing);
	public static SKSpriteNode FromColor (MonoMac.AppKit.NSColor color, System.Drawing.SizeF size);
	public static SKSpriteNode FromImageNamed (string name);
	public static SKSpriteNode FromTexture (SKTexture texture, System.Drawing.SizeF size);
	public static SKSpriteNode FromTexture (SKTexture texture);
}
```

### New Type MonoMac.SpriteKit.SKTexture

```
public class SKTexture : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTexture (MonoMac.Foundation.NSCoder coder);
	public SKTexture (MonoMac.Foundation.NSObjectFlag t);
	public SKTexture (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SKTextureFilteringMode FilteringMode { get; set; }
	public virtual System.Drawing.SizeF Size { get; }
	public virtual System.Drawing.RectangleF TextureRect { get; }
	public virtual bool UsesMipmaps { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual SKTexture CreateTextureByGeneratingNormalMap ();
	public virtual SKTexture CreateTextureByGeneratingNormalMap (float smoothness, float contrast);
	public static SKTexture FromData (MonoMac.Foundation.NSData pixelData, System.Drawing.SizeF size, bool flipped);
	public static SKTexture FromData (MonoMac.Foundation.NSData pixelData, System.Drawing.SizeF size, uint rowLength, uint alignment);
	public static SKTexture FromData (MonoMac.Foundation.NSData pixelData, System.Drawing.SizeF size);
	public static SKTexture FromImage (MonoMac.CoreGraphics.CGImage image);
	public static SKTexture FromImage (MonoMac.AppKit.NSImage image);
	public static SKTexture FromImageNamed (string name);
	public static SKTexture FromRectangle (System.Drawing.RectangleF rect, SKTexture texture);
	public static SKTexture FromTextureNoise (float smoothness, System.Drawing.SizeF size, bool grayscale);
	public static SKTexture FromTextureVectorNoise (float smoothness, System.Drawing.SizeF size);
	public virtual void Preload (MonoMac.Foundation.NSAction completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public static void PreloadTextures (SKTexture[] textures, MonoMac.Foundation.NSAction completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
	public virtual SKTexture TextureByApplyingCIFilter (MonoMac.CoreImage.CIFilter filter);
}
```

### New Type MonoMac.SpriteKit.SKTextureAtlas

```
public class SKTextureAtlas : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTextureAtlas ();
	public SKTextureAtlas (MonoMac.Foundation.NSCoder coder);
	public SKTextureAtlas (MonoMac.Foundation.NSObjectFlag t);
	public SKTextureAtlas (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] TextureNames { get; }
	// methods
	public static SKTextureAtlas FromDictionary (MonoMac.Foundation.NSDictionary properties);
	public static SKTextureAtlas FromName (string name);
	public virtual void Preload (MonoMac.Foundation.NSAction completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public static void PreloadTextures (SKTextureAtlas[] textures, MonoMac.Foundation.NSAction completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTextureAtlas[] textures);
	public virtual SKTexture TextureNamed (string name);
}
```

### New Type MonoMac.SpriteKit.SKTextureFilteringMode

```
[Serializable]
public enum SKTextureFilteringMode {
	Linear = 1,
	Nearest = 0,
}
```

### New Type MonoMac.SpriteKit.SKTextureModify

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

### New Type MonoMac.SpriteKit.SKTransition

```
public class SKTransition : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTransition (MonoMac.Foundation.NSCoder coder);
	public SKTransition (MonoMac.Foundation.NSObjectFlag t);
	public SKTransition (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool PausesIncomingScene { get; set; }
	public virtual bool PausesOutgoingScene { get; set; }
	// methods
	public static SKTransition CrossFadeWithDuration (double sec);
	public static SKTransition DoorsCloseHorizontalWithDuration (double sec);
	public static SKTransition DoorsCloseVerticalWithDuration (double sec);
	public static SKTransition DoorsOpenHorizontalWithDuration (double sec);
	public static SKTransition DoorsOpenVerticalWithDuration (double sec);
	public static SKTransition DoorwayWithDuration (double sec);
	public static SKTransition FadeWithColor (MonoMac.AppKit.NSColor color, double sec);
	public static SKTransition FadeWithDuration (double sec);
	public static SKTransition FlipHorizontalWithDuration (double sec);
	public static SKTransition FlipVerticalWithDuration (double sec);
	public static SKTransition MoveInWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition PushWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition RevealWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition TransitionWithCIFilter (MonoMac.CoreImage.CIFilter filter, double sec);
}
```

### New Type MonoMac.SpriteKit.SKTransitionDirection

```
[Serializable]
public enum SKTransitionDirection {
	Down = 1,
	Left = 3,
	Right = 2,
	Up = 0,
}
```

### New Type MonoMac.SpriteKit.SKUniform

```
public class SKUniform : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKUniform ();
	public SKUniform (string name, MonoMac.OpenGL.Matrix3d value);
	public SKUniform (string name, MonoMac.OpenGL.Matrix2 value);
	public SKUniform (string name, MonoMac.OpenGL.Vector4 value);
	public SKUniform (string name, MonoMac.OpenGL.Vector3 value);
	public SKUniform (string name, MonoMac.OpenGL.Vector2 value);
	public SKUniform (string name, float value);
	public SKUniform (string name, SKTexture texture);
	public SKUniform (string name);
	public SKUniform (System.IntPtr handle);
	public SKUniform (MonoMac.Foundation.NSObjectFlag t);
	public SKUniform (MonoMac.Foundation.NSCoder coder);
	public SKUniform (string name, MonoMac.OpenGL.Matrix4 value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.OpenGL.Matrix2 FloatMatrix2Value { get; set; }
	public virtual MonoMac.OpenGL.Matrix3d FloatMatrix3Value { get; set; }
	public virtual MonoMac.OpenGL.Matrix4 FloatMatrix4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual MonoMac.OpenGL.Vector2 FloatVector2Value { get; set; }
	public virtual MonoMac.OpenGL.Vector3 FloatVector3Value { get; set; }
	public virtual MonoMac.OpenGL.Vector4 FloatVector4Value { get; set; }
	public virtual string Name { get; }
	public virtual SKTexture TextureValue { get; set; }
	public virtual SKUniformType UniformType { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type MonoMac.SpriteKit.SKUniformType

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

### New Type MonoMac.SpriteKit.SKVideoNode

```
public class SKVideoNode : MonoMac.SpriteKit.SKNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKVideoNode ();
	public SKVideoNode (MonoMac.Foundation.NSCoder coder);
	public SKVideoNode (MonoMac.Foundation.NSObjectFlag t);
	public SKVideoNode (System.IntPtr handle);
	public SKVideoNode (MonoMac.AVFoundation.AVPlayer player);
	public SKVideoNode (string videoFile);
	public SKVideoNode (MonoMac.Foundation.NSUrl url);
	// properties
	public virtual System.Drawing.PointF AnchorPoint { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Drawing.SizeF Size { get; set; }
	// methods
	public static SKVideoNode FromFile (string videoFile);
	public static SKVideoNode FromPlayer (MonoMac.AVFoundation.AVPlayer player);
	public static SKVideoNode FromUrl (MonoMac.Foundation.NSUrl videoURL);
	public virtual void Pause ();
	public virtual void Play ();
}
```

### New Type MonoMac.SpriteKit.SKView

```
public class SKView : MonoMac.AppKit.NSView, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKView ();
	public SKView (MonoMac.Foundation.NSCoder coder);
	public SKView (MonoMac.Foundation.NSObjectFlag t);
	public SKView (System.IntPtr handle);
	// properties
	public virtual bool AllowsTransparency { get; set; }
	public virtual bool Asynchronous { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual int FrameInterval { get; set; }
	public virtual bool IgnoresSiblingOrder { get; set; }
	public virtual bool Paused { get; set; }
	public virtual SKScene Scene { get; }
	public virtual bool ShouldCullNonVisibleNodes { get; set; }
	public virtual bool ShowsDrawCount { get; set; }
	public virtual bool ShowsFields { get; set; }
	public virtual bool ShowsFPS { get; set; }
	public virtual bool ShowsNodeCount { get; set; }
	public virtual bool ShowsPhysics { get; set; }
	public virtual bool ShowsQuadCount { get; set; }
	// methods
	public virtual System.Drawing.PointF ConvertPointFromScene (System.Drawing.PointF point, SKScene scene);
	public virtual System.Drawing.PointF ConvertPointToScene (System.Drawing.PointF point, SKScene scene);
	protected override void Dispose (bool disposing);
	public virtual void PresentScene (SKScene scene);
	public virtual void PresentScene (SKScene scene, SKTransition transition);
	public virtual SKTexture TextureFromNode (SKNode node);
	public virtual SKTexture TextureFromNode (SKNode node, System.Drawing.RectangleF crop);
}
```

## New Namespace MonoMac.VideoToolbox

### New Type MonoMac.VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString AllowFrameReordering { get; }
	public static MonoMac.Foundation.NSString AllowTemporalCompression { get; }
	public static MonoMac.Foundation.NSString AverageBitRate { get; }
	public static MonoMac.Foundation.NSString DataRateLimits { get; }
	public static MonoMac.Foundation.NSString H264EntropyMode { get; }
	public static MonoMac.Foundation.NSString MaxKeyFrameInterval { get; }
	public static MonoMac.Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static MonoMac.Foundation.NSString MoreFramesAfterEnd { get; }
	public static MonoMac.Foundation.NSString MoreFramesBeforeStart { get; }
	public static MonoMac.Foundation.NSString NumberOfPendingFrames { get; }
	public static MonoMac.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoMac.Foundation.NSString ProfileLevel { get; }
	public static MonoMac.Foundation.NSString Quality { get; }
	public static MonoMac.Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
}
```

### New Type MonoMac.VideoToolbox.VTCompressionPropertyKey_

```
public static class VTCompressionPropertyKey_ {
	// properties
	public static MonoMac.Foundation.NSString AspectRatio16x9 { get; }
	public static MonoMac.Foundation.NSString CABAC { get; }
	public static MonoMac.Foundation.NSString CAVLC { get; }
	public static MonoMac.Foundation.NSString CleanAperture { get; }
	public static MonoMac.Foundation.NSString ColorPrimaries { get; }
	public static MonoMac.Foundation.NSString Depth { get; }
	public static MonoMac.Foundation.NSString ExpectedDuration { get; }
	public static MonoMac.Foundation.NSString ExpectedFrameRate { get; }
	public static MonoMac.Foundation.NSString FieldCount { get; }
	public static MonoMac.Foundation.NSString FieldDetail { get; }
	public static MonoMac.Foundation.NSString ICCProfile { get; }
	public static MonoMac.Foundation.NSString MaxFrameDelayCount { get; }
	public static MonoMac.Foundation.NSString MaxH264SliceBytes { get; }
	public static MonoMac.Foundation.NSString MultiPassStorage { get; }
	public static MonoMac.Foundation.NSString PixelAspectRatio { get; }
	public static MonoMac.Foundation.NSString PixelTransferProperties { get; }
	public static MonoMac.Foundation.NSString ProgressiveScan { get; }
	public static MonoMac.Foundation.NSString RealTime { get; }
	public static MonoMac.Foundation.NSString SourceFrameCount { get; }
	public static MonoMac.Foundation.NSString TransferFunction { get; }
	public static MonoMac.Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static MonoMac.Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type MonoMac.VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type MonoMac.VideoToolbox.VTDecodeFrameFlags

```
[Serializable]
[Flags]
public enum VTDecodeFrameFlags {
	DoNotOutputFrame = 2,
	EnableAsynchronousDecompression = 1,
	EnableTemporalProcessing = 8,
	OneTimeRealTimePlayback = 4,
}
```

### New Type MonoMac.VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString ContentHasInterframeDependencies { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static MonoMac.Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static MonoMac.Foundation.NSString FieldMode { get; }
	public static MonoMac.Foundation.NSString FieldMode_BothFields { get; }
	public static MonoMac.Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static MonoMac.Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static MonoMac.Foundation.NSString FieldMode_SingleField { get; }
	public static MonoMac.Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static MonoMac.Foundation.NSString Height { get; }
	public static MonoMac.Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static MonoMac.Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static MonoMac.Foundation.NSString PixelBufferPool { get; }
	public static MonoMac.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoMac.Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static MonoMac.Foundation.NSString PixelTransferProperties { get; }
	public static MonoMac.Foundation.NSString RealTime { get; }
	public static MonoMac.Foundation.NSString ReducedCoefficientDecode { get; }
	public static MonoMac.Foundation.NSString ReducedFrameDelivery { get; }
	public static MonoMac.Foundation.NSString ReducedResolutionDecode { get; }
	public static MonoMac.Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
	public static MonoMac.Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static MonoMac.Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static MonoMac.Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static MonoMac.Foundation.NSString ThreadCount { get; }
	public static MonoMac.Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
	public static MonoMac.Foundation.NSString Width { get; }
}
```

### New Type MonoMac.VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static MonoMac.Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type MonoMac.VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type MonoMac.VideoToolbox.VTMultiPassStorageCreationOption

```
public static class VTMultiPassStorageCreationOption {
	// properties
	public static MonoMac.Foundation.NSString DoNotDelete { get; }
}
```

### New Type MonoMac.VideoToolbox.VTProfileLevel

```
public static class VTProfileLevel {
	// properties
	public static MonoMac.Foundation.NSString H263_Profile0_Level10 { get; }
	public static MonoMac.Foundation.NSString H263_Profile0_Level45 { get; }
	public static MonoMac.Foundation.NSString H263_Profile3_Level45 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_1_3 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_Extended_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Extended_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_High_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_AutoLevel { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L3 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L4 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L0 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L1 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type MonoMac.VideoToolbox.VTProperty

```
public static class VTProperty {
	// properties
	public static MonoMac.Foundation.NSString DocumentationKey { get; }
	public static MonoMac.Foundation.NSString ReadWriteStatus { get; }
	public static MonoMac.Foundation.NSString ShouldBeSerialized { get; }
	public static MonoMac.Foundation.NSString SupportedValueListKey { get; }
	public static MonoMac.Foundation.NSString SupportedValueMaximumKey { get; }
	public static MonoMac.Foundation.NSString SupportedValueMinimumKey { get; }
	public static MonoMac.Foundation.NSString Type { get; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyReadWriteStatus

```
public static class VTPropertyReadWriteStatus {
	// properties
	public static MonoMac.Foundation.NSString ReadOnly { get; }
	public static MonoMac.Foundation.NSString ReadWrite { get; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyType

```
public static class VTPropertyType {
	// properties
	public static MonoMac.Foundation.NSString Boolean { get; }
	public static MonoMac.Foundation.NSString Enumeration { get; }
	public static MonoMac.Foundation.NSString Number { get; }
}
```

### New Type MonoMac.VideoToolbox.VTStatus

```
[Serializable]
public enum VTStatus {
	AllocationFailed = -12904,
	ColorCorrectionPixelTransferFailed = -12212,
	ColorSyncTransformConvertFailed = -12919,
	CouldNotCreateColorCorrectionData = -12918,
	CouldNotCreateInstance = -12907,
	CouldNotFindTemporalFilter = -12217,
	CouldNotFindVideoDecoder = -12906,
	CouldNotFindVideoEncoder = -12908,
	FormatDescriptionChangeNotSupported = -12916,
	FrameSiloInvalidTimeRange = -12216,
	FrameSiloInvalidTimeStamp = -12215,
	ImageRotationNotSupported = -12914,
	InsufficientSourceColorData = -12917,
	InvalidSession = -12903,
	MultiPassStorageIdentifierMismatch = -12913,
	MultiPassStorageInvalid = -12214,
	Ok = 0,
	Parameter = -12902,
	PixelTransferNotPermitted = -12218,
	PixelTransferNotSupported = -12905,
	PropertyNotSupported = -12900,
	PropertyReadOnly = -12901,
	VideoDecoderAuthorization = -12210,
	VideoDecoderBadData = -12909,
	VideoDecoderMalfunction = -12911,
	VideoDecoderNotAvailableNow = -12913,
	VideoDecoderUnsupportedDataFormat = -12910,
	VideoEncoderAuthorization = -12211,
	VideoEncoderMalfunction = -12912,
	VideoEncoderNotAvailableNow = -12915,
}
```

### New Type MonoMac.VideoToolbox.VTVideoEncoderList

```
public static class VTVideoEncoderList {
	// properties
	public static MonoMac.Foundation.NSString CodecName { get; }
	public static MonoMac.Foundation.NSString CodecType { get; }
	public static MonoMac.Foundation.NSString DisplayName { get; }
	public static MonoMac.Foundation.NSString EncoderID { get; }
	public static MonoMac.Foundation.NSString EncoderName { get; }
}
```

### New Type MonoMac.VideoToolbox.VTVideoEncoderSpecification

```
public static class VTVideoEncoderSpecification {
	// properties
	public static MonoMac.Foundation.NSString EnableHardwareAcceleratedVideoEncoder { get; }
	public static MonoMac.Foundation.NSString RequireHardwareAcceleratedVideoEncoder { get; }
}
```
