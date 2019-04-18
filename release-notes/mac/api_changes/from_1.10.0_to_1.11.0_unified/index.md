---
id: 74D81CDC-5816-42C9-BB6E-BBEF847151BA
title: "From 1.10.0 to 1.11.0 unified"
---

# Xamarin.Mac.dll

## Namespace AppKit

### Type Changed: AppKit.NSColor

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: AppKit.NSColorSpace

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: AppKit.NSComboBox

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

### Type Changed: AppKit.NSDocumentController

Removed property:

```
public static NSDocumentController SharedDocumentController { get; }
```

Added property:

```
public static Foundation.NSObject SharedDocumentController { get; }
```

### Type Changed: AppKit.NSEdgeInsets

Removed constructor:

```
public NSEdgeInsets (System.nfloat top, System.nfloat left, System.nfloat bottom, System.nfloat right);
```

Added constructor:

```
public NSEdgeInsets (float top, float left, float bottom, float right);
```

Removed fields:

```
public System.nfloat Bottom;
	public System.nfloat Left;
	public System.nfloat Right;
	public System.nfloat Top;
```

Added fields:

```
public float Bottom;
	public float Left;
	public float Right;
	public float Top;
```

### Type Changed: AppKit.NSGlyphInfo

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: AppKit.NSImage

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: AppKit.NSLayoutConstraint

Added method:

```
public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, object[] viewsAndMetrics);
```

### Type Changed: AppKit.NSTextStorage

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: AppKit.NSToolbar

Added constructor:

```
public NSToolbar ();
```

### Type Changed: AppKit.NSWindow

Added properties:

```
public virtual Foundation.NSObject ContentLayoutGuide { get; }
	public virtual CoreGraphics.CGRect ContentLayoutRect { get; }
	public virtual NSTitlebarAccessoryViewController[] TitlebarAccessoryViewControllers { get; set; }
	public virtual bool TitlebarAppearsTransparent { get; set; }
	public virtual NSWindowTitleVisibility TitleVisibility { get; set; }
```

Added methods:

```
public virtual void AddTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController);
	public static NSWindow GetWindowWithContentViewController (NSViewController contentViewController);
	public virtual void InsertTitlebarAccessoryViewController (NSTitlebarAccessoryViewController childViewController, System.nint index);
	public virtual void RemoveTitlebarAccessoryViewControllerAtIndex (System.nint index);
```

### Type Changed: AppKit.NSWindowController

Added property:

```
public virtual NSViewController ContentViewController { get; set; }
```

### Removed Type AppKit.INSComboBoxDelegate ### Removed Type AppKit.NSComboBoxDelegate ### Removed Type AppKit.NSComboBoxDelegate_Extensions ### New Type AppKit.NSTitlebarAccessoryViewController

```
public class NSTitlebarAccessoryViewController : AppKit.NSViewController, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTitlebarAccessoryViewController ();
	public NSTitlebarAccessoryViewController (Foundation.NSCoder coder);
	public NSTitlebarAccessoryViewController (Foundation.NSObjectFlag t);
	public NSTitlebarAccessoryViewController (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat FullScreenMinHeight { get; set; }
	public virtual NSLayoutAttribute LayoutAttribute { get; set; }
	// methods
	public virtual void ViewDidAppear ();
	public virtual void ViewDidDisappear ();
	public virtual void ViewWillAppear ();
}
```

### New Type AppKit.NSWindowTitleVisibility

```
[Serializable]
public enum NSWindowTitleVisibility {
	Hidden = 1,
	HiddenWhenActive = 2,
	Visible = 0,
}
```





## Namespace AudioToolbox



### Type Changed: AudioToolbox.AudioFile

Obsoleted method:

```
[Obsolete ("Use ReadPacketData instead")]
	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, System.IntPtr buffer);
```

### Type Changed: AudioToolbox.AudioFormatType

Added value:

```
AMRWideBand = 1935767394,
```

### Type Changed: AudioToolbox.AudioQueueStatus

Added value:

```
BufferEnqueuedTwice = -66666,
```

### Type Changed: AudioToolbox.AudioStreamBasicDescription

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

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioTypeMixer

Added value:

```
Spacial = 862217581,
```

Obsoleted field:

```
[Obsolete ("Replaced by Spacial")]
	ThreeD = 862219640,
```

### Type Changed: AudioUnit.AudioTypeMusicDevice

Added value:

```
MidiSynth = 1836284270,
```

### Type Changed: AudioUnit.AudioUnitParameterFlag

Added value:

```
OmitFromPresets = 8192,
```

### Type Changed: AudioUnit.AudioUnitParameterType

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

### Type Changed: AudioUnit.AudioUnitPropertyIDType

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

### New Type AudioUnit.ScheduledAudioSliceFlag

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

### New Type AudioUnit.SpatialMixerAttenuation

```
[Serializable]
public enum SpatialMixerAttenuation {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
```

### New Type AudioUnit.SpatialMixerRenderingFlags

```
[Serializable]
[Flags]
public enum SpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
```

## Namespace AVFoundation

### Type Changed: AVFoundation.AudioSettings

Removed property:

```
public float? SampleRate { get; set; }
```

Added property:

```
public double? SampleRate { get; set; }
```

### Type Changed: AVFoundation.AVAsset

Added property:

```
public virtual AVMetadataItem[] Metadata { get; }
```

### Type Changed: AVFoundation.AVAssetExportSession

Added properties:

```
public virtual bool CanPerformMultiplePassesOverSourceMediaData { get; set; }
	public virtual Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: AVFoundation.AVAssetReaderOutput

Added property:

```
public virtual bool SupportsRandomAccess { get; set; }
```

Added methods:

```
public virtual void MarkConfigurationAsFinal ();
	public virtual void ResetForReadingTimeRanges (Foundation.NSValue[] timeRanges);
```

### Type Changed: AVFoundation.AVAssetResourceLoader

Removed constructor:

```
public AVAssetResourceLoader ();
```

### Type Changed: AVFoundation.AVAssetResourceLoaderDelegate

Added methods:

```
public virtual void DidCancelAuthenticationChallenge (AVAssetResourceLoader resourceLoader, Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public virtual bool ShouldWaitForRenewalOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public virtual bool ShouldWaitForResponseToAuthenticationChallenge (AVAssetResourceLoader resourceLoader, Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added methods:

```
public static void DidCancelAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
	public static bool ShouldWaitForRenewalOfRequestedResource (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceRenewalRequest renewalRequest);
	public static bool ShouldWaitForResponseToAuthenticationChallenge (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, Foundation.NSUrlAuthenticationChallenge authenticationChallenge);
```

### Type Changed: AVFoundation.AVAssetResourceLoadingContentInformationRequest

Removed constructor:

```
public AVAssetResourceLoadingContentInformationRequest ();
```

Added property:

```
public virtual Foundation.NSDate RenewalDate { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: AVFoundation.AVAssetResourceLoadingDataRequest

Removed method:

```
public override string ToString ();
```

### Type Changed: AVFoundation.AVAssetResourceLoadingRequest

Removed constructor:

```
public AVAssetResourceLoadingRequest ();
```

### Type Changed: AVFoundation.AVAssetTrack

Added properties:

```
public virtual AVMetadataItem[] Metadata { get; }
	public virtual bool RequiresFrameReordering { get; }
```

### Type Changed: AVFoundation.AVAssetTrackTrackAssociation

Added property:

```
public static Foundation.NSString MetadataReferent { get; }
```

### Type Changed: AVFoundation.AVAssetWriter

Added properties:

```
public virtual Foundation.NSString[] AvailableMediaTypes { get; }
	public virtual Foundation.NSUrl DirectoryForTemporaryFiles { get; set; }
```

### Type Changed: AVFoundation.AVAssetWriterInput

Added properties:

```
public virtual bool CanPerformMultiplePasses { get; }
	public virtual AVAssetWriterInputPassDescription CurrentPassDescription { get; }
	public virtual bool PerformsMultiPassEncodingIfSupported { get; set; }
	public virtual System.nint PreferredMediaChunkAlignment { get; set; }
	public virtual CoreMedia.CMTime PreferredMediaChunkDuration { get; set; }
	public virtual Foundation.NSUrl SampleReferenceBaseUrl { get; set; }
```

Added methods:

```
public virtual void MarkCurrentPassAsFinished ();
	public virtual void SetPassHandler (CoreFoundation.DispatchQueue queue, System.Action passHandler);
```

### Type Changed: AVFoundation.AVAudioSessionErrorCode

Added value:

```
InsufficientPriority = 561017449,
```

### Type Changed: AVFoundation.AVCaptureConnection

Added constructors:

```
public AVCaptureConnection (AVCaptureInputPort[] inputPorts, AVCaptureOutput output);
	public AVCaptureConnection (AVCaptureInputPort inputPort, AVCaptureVideoPreviewLayer layer);
```

### Type Changed: AVFoundation.AVCaptureDevicePosition

Added value:

```
Unspecified = 0,
```

### Type Changed: AVFoundation.AVCaptureExposureMode

Added value:

```
Custom = 3,
```

### Type Changed: AVFoundation.AVCaptureFileOutput

Added method:

```
public void StartRecordingToOutputFile (Foundation.NSUrl outputFileUrl, System.Action<Foundation.NSObject[]> startRecordingFromConnections, System.Action<Foundation.NSObject[],Foundation.NSError> finishedRecording);
```

### Type Changed: AVFoundation.AVCaptureFocusMode

Removed values:

```
ModeAutoFocus = 1,
	ModeContinuousAutoFocus = 2,
	ModeLocked = 0,
```

Added values:

```
AutoFocus = 1,
	ContinuousAutoFocus = 2,
	Locked = 0,
```

### Type Changed: AVFoundation.AVCaptureSession

Added property:

```
public virtual CoreMedia.CMClock MasterClock { get; }
```

Added methods:

```
public virtual void AddConnection (AVCaptureConnection connection);
	public virtual void AddInputWithNoConnections (AVCaptureInput input);
	public virtual void AddOutputWithNoConnections (AVCaptureOutput output);
	public virtual bool CanAddConnection (AVCaptureConnection connection);
	public virtual void RemoveConnection (AVCaptureConnection connection);
```

### Type Changed: AVFoundation.AVCaptureVideoPreviewLayer

Added method:

```
public static AVCaptureVideoPreviewLayer CreateWithNoConnection (AVCaptureSession session);
```

### Type Changed: AVFoundation.AVError

Added values:

```
FailedToParse2 = -11853,
	FileTypeDoesNotSupportSampleReferences = -11854,
	UndecodableMediaData = -11855,
```

### Type Changed: AVFoundation.AVMediaSelectionGroup

Added property:

```
public virtual AVMediaSelectionOption DefaultOption { get; }
```

### Type Changed: AVFoundation.AVMetadata

Added properties:

```
public static Foundation.NSString FormatHlsMetadata { get; }
	public static Foundation.NSString IcyMetadataKeyStreamTitle { get; }
	public static Foundation.NSString IcyMetadataKeyStreamUrl { get; }
	public static Foundation.NSString IsoUserDataKeyTaggedCharacteristic { get; }
	public static Foundation.NSString KeySpaceIcy { get; }
```

### Type Changed: AVFoundation.AVMetadataItem

Removed properties:

```
public virtual CoreMedia.CMTime Duration { get; }
	public virtual Foundation.NSDictionary ExtraAttributes { get; }
	public virtual string KeySpace { get; }
	public virtual Foundation.NSLocale Locale { get; }
	public virtual CoreMedia.CMTime Time { get; }
	public virtual Foundation.NSObject Value { get; }
```

Added properties:

```
public virtual Foundation.NSString DataType { get; set; }
	public virtual CoreMedia.CMTime Duration { get; set; }
	public virtual string ExtendedLanguageTag { get; set; }
	public virtual Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual Foundation.NSLocale Locale { get; set; }
	public virtual Foundation.NSString MetadataIdentifier { get; set; }
	public virtual CoreMedia.CMTime Time { get; set; }
	public virtual Foundation.NSObject Value { get; set; }
```

Added methods:

```
public static AVMetadataItem[] FilterWithIdentifier (AVMetadataItem[] metadataItems, Foundation.NSString metadataIdentifer);
	public static Foundation.NSObject GetKeyForIdentifier (Foundation.NSString identifier);
	public static Foundation.NSString GetKeySpaceForIdentifier (Foundation.NSString identifier);
	public static Foundation.NSString GetMetadataIdentifier (Foundation.NSObject key, Foundation.NSString keySpace);
```

### Type Changed: AVFoundation.AVMutableMetadataItem

Removed properties:

```
public virtual CoreMedia.CMTime Duration { get; set; }
	public virtual Foundation.NSDictionary ExtraAttributes { get; set; }
	public virtual string KeySpace { get; set; }
	public virtual Foundation.NSLocale Locale { get; set; }
	public virtual CoreMedia.CMTime Time { get; set; }
	public virtual Foundation.NSObject Value { get; set; }
```

Added properties:

```
public override Foundation.NSString DataType { get; set; }
	public override CoreMedia.CMTime Duration { get; set; }
	public override string ExtendedLanguageTag { get; set; }
	public override Foundation.NSDictionary ExtraAttributes { get; set; }
	public override string KeySpace { get; set; }
	public override Foundation.NSLocale Locale { get; set; }
	public override Foundation.NSString MetadataIdentifier { get; set; }
	public override CoreMedia.CMTime Time { get; set; }
	public override Foundation.NSObject Value { get; set; }
```

### Type Changed: AVFoundation.AVPlayerItem

Added property:

```
public virtual double PreferredPeakBitRate { get; set; }
```

### Type Changed: AVFoundation.AVTimedMetadataGroup

Added constructor:

```
public AVTimedMetadataGroup (CoreMedia.CMSampleBuffer sampleBuffer);
```

Added method:

```
public virtual CoreMedia.CMFormatDescription CopyFormatDescription ();
```

### Type Changed: AVFoundation.AVUrlAsset

Removed constructor:

```
public AVUrlAsset (Foundation.NSUrl URL, Foundation.NSDictionary options);
```

Added constructor:

```
public AVUrlAsset (Foundation.NSUrl url, Foundation.NSDictionary options);
```

### Type Changed: AVFoundation.AVVideoCodecSettings

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

### Type Changed: AVFoundation.AVVideoSettingsCompressed

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

### Type Changed: AVFoundation.AVVideoSettingsUncompressed

Removed property:

```
public AVVideoScalingMode? ScalingMode { set; }
```

Added property:

```
public AVVideoScalingMode? ScalingMode { get; set; }
```

### Type Changed: AVFoundation.IAVPlayerItemLegibleOutputPushDelegate

Added interface:

```
IAVPlayerItemOutputPushDelegate
```

### New Type AVFoundation.AVAssetReaderOutputMetadataAdaptor

```
public class AVAssetReaderOutputMetadataAdaptor : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderOutputMetadataAdaptor (Foundation.NSObjectFlag t);
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

### New Type AVFoundation.AVAssetReaderSampleReferenceOutput

```
public class AVAssetReaderSampleReferenceOutput : AVFoundation.AVAssetReaderOutput, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetReaderSampleReferenceOutput (Foundation.NSObjectFlag t);
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

### New Type AVFoundation.AVAssetResourceRenewalRequest

```
public class AVAssetResourceRenewalRequest : AVFoundation.AVAssetResourceLoadingRequest, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceRenewalRequest (Foundation.NSObjectFlag t);
	public AVAssetResourceRenewalRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type AVFoundation.AVAssetWriterInputMetadataAdaptor

```
public class AVAssetWriterInputMetadataAdaptor : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputMetadataAdaptor (Foundation.NSObjectFlag t);
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

### New Type AVFoundation.AVAssetWriterInputPassDescription

```
public class AVAssetWriterInputPassDescription : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputPassDescription ();
	public AVAssetWriterInputPassDescription (Foundation.NSObjectFlag t);
	public AVAssetWriterInputPassDescription (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSValue[] SourceTimeRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type AVFoundation.AVAudio3DAngularOrientation

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

### New Type AVFoundation.AVAudio3DMixing

```
public abstract class AVAudio3DMixing : Foundation.NSObject, IAVAudio3DMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudio3DMixing ();
	public AVAudio3DMixing (Foundation.NSObjectFlag t);
	public AVAudio3DMixing (System.IntPtr handle);
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type AVFoundation.AVAudio3DMixing_Extensions

```
public static class AVAudio3DMixing_Extensions {
}
```

### New Type AVFoundation.AVAudio3DMixingRenderingAlgorithm

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

### New Type AVFoundation.AVAudio3DVectorOrientation

```
public struct AVAudio3DVectorOrientation {
	// constructors
	public AVAudio3DVectorOrientation (OpenGL.Vector3 forward, OpenGL.Vector3 up);
	// fields
	public OpenGL.Vector3 Forward;
	public OpenGL.Vector3 Up;
	// methods
	public override bool Equals (object obj);
	public bool Equals (AVAudio3DVectorOrientation other);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public static bool op_Inequality (AVAudio3DVectorOrientation left, AVAudio3DVectorOrientation right);
	public override string ToString ();
}
```

### New Type AVFoundation.AVAudioBuffer

```
public class AVAudioBuffer : Foundation.NSObject, Foundation.INSCopying, Foundation.INSMutableCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioBuffer (Foundation.NSObjectFlag t);
	public AVAudioBuffer (System.IntPtr handle);
	// properties
	public AudioToolbox.AudioBuffers AudioBufferList { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat Format { get; }
	public AudioToolbox.AudioBuffers MutableAudioBufferList { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual Foundation.NSObject MutableCopy (Foundation.NSZone zone);
}
```

### New Type AVFoundation.AVAudioChannelLayout

```
public class AVAudioChannelLayout : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioChannelLayout ();
	public AVAudioChannelLayout (Foundation.NSObjectFlag t);
	public AVAudioChannelLayout (System.IntPtr handle);
	public AVAudioChannelLayout (uint layoutTag);
	public AVAudioChannelLayout (AudioToolbox.AudioChannelLayout layout);
	// properties
	public virtual uint ChannelCount { get; }
	public override System.IntPtr ClassHandle { get; }
	public AudioToolbox.AudioChannelLayout Layout { get; }
	public virtual uint LayoutTag { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioChannelLayout a, AVAudioChannelLayout b);
	public static bool op_Inequality (AVAudioChannelLayout a, AVAudioChannelLayout b);
}
```

### New Type AVFoundation.AVAudioCommonFormat

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

### New Type AVFoundation.AVAudioEngine

```
public class AVAudioEngine : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEngine ();
	public AVAudioEngine (Foundation.NSObjectFlag t);
	public AVAudioEngine (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static Foundation.NSString ConfigurationChangeNotification { get; }
	public virtual AVAudioInputNode InputNode { get; }
	public virtual AVAudioMixerNode MainMixerNode { get; }
	public virtual AVAudioOutputNode OutputNode { get; }
	public virtual bool Running { get; }
	// methods
	public virtual void AttachNode (AVAudioNode node);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, System.nuint sourceBus, System.nuint targetBus, AVAudioFormat format);
	public virtual void Connect (AVAudioNode sourceNode, AVAudioNode targetNode, AVAudioFormat format);
	public virtual void DetachNode (AVAudioNode node);
	public virtual void DisconnectNodeInput (AVAudioNode node, System.nuint bus);
	public virtual void DisconnectNodeInput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node);
	public virtual void DisconnectNodeOutput (AVAudioNode node, System.nuint bus);
	protected override void Dispose (bool disposing);
	public virtual void Pause ();
	public virtual void Prepare ();
	public virtual void Reset ();
	public virtual bool StartAndReturnError (out Foundation.NSError outError);
	public virtual void Stop ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveConfigurationChange (System.EventHandler<Foundation.NSNotificationEventArgs> handler);
	}
}
```

### New Type AVFoundation.AVAudioEnvironmentDistanceAttenuationModel

```
[Serializable]
public enum AVAudioEnvironmentDistanceAttenuationModel {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
}
```

### New Type AVFoundation.AVAudioEnvironmentDistanceAttenuationParameters

```
public class AVAudioEnvironmentDistanceAttenuationParameters : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentDistanceAttenuationParameters (Foundation.NSObjectFlag t);
	public AVAudioEnvironmentDistanceAttenuationParameters (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationModel DistanceAttenuationModel { get; set; }
	public virtual float MaximumDistance { get; set; }
	public virtual float ReferenceDistance { get; set; }
	public virtual float RolloffFactor { get; set; }
}
```

### New Type AVFoundation.AVAudioEnvironmentNode

```
public class AVAudioEnvironmentNode : AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentNode ();
	public AVAudioEnvironmentNode (Foundation.NSObjectFlag t);
	public AVAudioEnvironmentNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEnvironmentDistanceAttenuationParameters DistanceAttenuationParameters { get; }
	public virtual AVAudio3DAngularOrientation ListenerAngularOrientation { get; set; }
	public virtual OpenGL.Vector3 ListenerPosition { get; set; }
	public virtual AVAudio3DVectorOrientation ListenerVectorOrientation { get; set; }
	public virtual System.nuint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual AVAudioEnvironmentReverbParameters ReverbParameters { get; }
	public virtual float Volume { get; set; }
	// methods
	public virtual Foundation.NSObject[] ApplicableRenderingAlgorithms ();
	protected override void Dispose (bool disposing);
}
```

### New Type AVFoundation.AVAudioEnvironmentReverbParameters

```
public class AVAudioEnvironmentReverbParameters : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioEnvironmentReverbParameters (Foundation.NSObjectFlag t);
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

### New Type AVFoundation.AVAudioFile

```
public class AVAudioFile : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFile ();
	public AVAudioFile (Foundation.NSObjectFlag t);
	public AVAudioFile (System.IntPtr handle);
	public AVAudioFile (Foundation.NSUrl fileUrl, out Foundation.NSError outError);
	public AVAudioFile (Foundation.NSUrl fileUrl, AVAudioCommonFormat format, bool interleaved, out Foundation.NSError outError);
	public AVAudioFile (Foundation.NSUrl fileUrl, AudioSettings settings, out Foundation.NSError outError);
	public AVAudioFile (Foundation.NSUrl fileUrl, AudioSettings settings, AVAudioCommonFormat format, bool interleaved, out Foundation.NSError outError);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioFormat FileFormat { get; }
	public virtual long FramePosition { get; set; }
	public virtual long Length { get; }
	public virtual AVAudioFormat ProcessingFormat { get; }
	public virtual Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, out Foundation.NSError outError);
	public virtual bool ReadIntoBuffer (AVAudioPcmBuffer buffer, uint frames, out Foundation.NSError outError);
	public virtual bool WriteFromBuffer (AVAudioPcmBuffer buffer, out Foundation.NSError outError);
}
```

### New Type AVFoundation.AVAudioFormat

```
public class AVAudioFormat : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioFormat ();
	public AVAudioFormat (Foundation.NSDictionary settings);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, bool interleaved, AVAudioChannelLayout layout);
	public AVAudioFormat (AVAudioCommonFormat format, double sampleRate, uint channels, bool interleaved);
	public AVAudioFormat (double sampleRate, AVAudioChannelLayout layout);
	public AVAudioFormat (double sampleRate, uint channels);
	public AVAudioFormat (ref AudioToolbox.AudioStreamBasicDescription description, AVAudioChannelLayout layout);
	public AVAudioFormat (ref AudioToolbox.AudioStreamBasicDescription description);
	public AVAudioFormat (System.IntPtr handle);
	public AVAudioFormat (Foundation.NSObjectFlag t);
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
	public virtual AudioToolbox.AudioStreamBasicDescription StreamDescription { get; }
	public virtual Foundation.NSDictionary WeakSettings { get; }
	// methods
	protected override void Dispose (bool disposing);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (AVAudioFormat a, AVAudioFormat b);
	public static bool op_Inequality (AVAudioFormat a, AVAudioFormat b);
}
```

### New Type AVFoundation.AVAudioInputNode

```
public class AVAudioInputNode : AVFoundation.AVAudioIONode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioInputNode (Foundation.NSObjectFlag t);
	public AVAudioInputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type AVFoundation.AVAudioIONode

```
public class AVAudioIONode : AVFoundation.AVAudioNode, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioIONode (Foundation.NSObjectFlag t);
	public AVAudioIONode (System.IntPtr handle);
	// properties
	public virtual AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual double PresentationLatency { get; }
}
```

### New Type AVFoundation.AVAudioMixerNode

```
public class AVAudioMixerNode : AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioMixerNode ();
	public AVAudioMixerNode (Foundation.NSObjectFlag t);
	public AVAudioMixerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nuint NextAvailableInputBus { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float OutputVolume { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type AVFoundation.AVAudioMixing_Extensions

```
public static class AVAudioMixing_Extensions {
}
```

### New Type AVFoundation.AVAudioNode

```
public class AVAudioNode : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioNode (Foundation.NSObjectFlag t);
	public AVAudioNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAudioEngine Engine { get; }
	public virtual AVAudioTime LastRenderTime { get; }
	public virtual System.nuint NumberOfInputs { get; }
	public virtual System.nuint NumberOfOutputs { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual AVAudioFormat GetBusInputFormat (System.nuint bus);
	public virtual AVAudioFormat GetBusOutputFormat (System.nuint bus);
	public virtual string GetNameForInputBus (System.nuint bus);
	public virtual string GetNameForOutputBus (System.nuint bus);
	public virtual void InstallTapOnBus (System.nuint bus, uint bufferSize, AVAudioFormat format, AVAudioNodeTapBlock tapBlock);
	public virtual void RemoveTapOnBus (System.nuint bus);
	public virtual void Reset ();
}
```

### New Type AVFoundation.AVAudioNodeTapBlock

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

### New Type AVFoundation.AVAudioOutputNode

```
public class AVAudioOutputNode : AVFoundation.AVAudioIONode, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioOutputNode (Foundation.NSObjectFlag t);
	public AVAudioOutputNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type AVFoundation.AVAudioPcmBuffer

```
public class AVAudioPcmBuffer : AVFoundation.AVAudioBuffer, Foundation.INSCopying, Foundation.INSMutableCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPcmBuffer (Foundation.NSObjectFlag t);
	public AVAudioPcmBuffer (System.IntPtr handle);
	public AVAudioPcmBuffer (AVAudioFormat format, uint frameCapacity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.IntPtr FloatChannelData { get; }
	public virtual uint FrameCapacity { get; }
	public virtual uint FrameLength { get; set; }
	public virtual System.IntPtr Int16ChannelData { get; }
	public virtual System.IntPtr Int32ChannelData { get; }
	public virtual System.nuint Stride { get; }
}
```

### New Type AVFoundation.AVAudioPlayerNode

```
public class AVAudioPlayerNode : AVFoundation.AVAudioNode, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioPlayerNode ();
	public AVAudioPlayerNode (Foundation.NSObjectFlag t);
	public AVAudioPlayerNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual bool Playing { get; }
	public virtual OpenGL.Vector3 Position { get; set; }
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

### New Type AVFoundation.AVAudioPlayerNodeBufferOptions

```
[Serializable]
[Flags]
public enum AVAudioPlayerNodeBufferOptions {
	Interrupts = 2,
	InterruptsAtLoop = 4,
	Loops = 1,
}
```

### New Type AVFoundation.AVAudioSessionRecordPermission

```
[Serializable]
public enum AVAudioSessionRecordPermission {
	Denied = 1684369017,
	Granted = 1735552628,
	Undetermined = 1970168948,
}
```

### New Type AVFoundation.AVAudioSessionSilenceSecondaryAudioHintType

```
[Serializable]
public enum AVAudioSessionSilenceSecondaryAudioHintType {
	Begin = 1,
	End = 0,
}
```

### New Type AVFoundation.AVAudioStereoMixing

```
public abstract class AVAudioStereoMixing : Foundation.NSObject, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioStereoMixing ();
	public AVAudioStereoMixing (Foundation.NSObjectFlag t);
	public AVAudioStereoMixing (System.IntPtr handle);
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type AVFoundation.AVAudioStereoMixing_Extensions

```
public static class AVAudioStereoMixing_Extensions {
}
```

### New Type AVFoundation.AVAudioTime

```
public class AVAudioTime : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioTime ();
	public AVAudioTime (Foundation.NSObjectFlag t);
	public AVAudioTime (System.IntPtr handle);
	public AVAudioTime (ref AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public AVAudioTime (ulong hostTime);
	public AVAudioTime (long sampleTime, double sampleRate);
	public AVAudioTime (ulong hostTime, long sampleTime, double sampleRate);
	// properties
	public virtual AudioToolbox.AudioTimeStamp AudioTimeStamp { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual ulong HostTime { get; }
	public virtual bool HostTimeValid { get; }
	public virtual double SampleRate { get; }
	public virtual long SampleTime { get; }
	public virtual bool SampleTimeValid { get; }
	// methods
	public virtual AVAudioTime ExtrapolateTimeFromAnchor (AVAudioTime anchorTime);
	public static AVAudioTime FromAudioTimeStamp (ref AudioToolbox.AudioTimeStamp timestamp, double sampleRate);
	public static AVAudioTime FromHostTime (ulong hostTime);
	public static AVAudioTime FromHostTime (ulong hostTime, long sampleTime, double sampleRate);
	public static AVAudioTime FromSampleTime (long sampleTime, double sampleRate);
	public static ulong HostTimeForSeconds (double seconds);
	public static double SecondsForHostTime (ulong hostTime);
}
```

### New Type AVFoundation.AVAudioUnit

```
public class AVAudioUnit : AVFoundation.AVAudioNode, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnit (Foundation.NSObjectFlag t);
	public AVAudioUnit (System.IntPtr handle);
	// properties
	public virtual AudioUnit.AudioUnit AudioUnit { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual System.nuint Version { get; }
	// methods
	public virtual bool LoadAudioUnitPreset (Foundation.NSUrl url, out Foundation.NSError error);
}
```

### New Type AVFoundation.AVAudioUnitDelay

```
public class AVAudioUnitDelay : AVFoundation.AVAudioUnitEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDelay ();
	public AVAudioUnitDelay (Foundation.NSObjectFlag t);
	public AVAudioUnitDelay (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DelayTime { get; set; }
	public virtual float Feedback { get; set; }
	public virtual float LowPassCutoff { get; set; }
	public virtual float WetDryMix { get; set; }
}
```

### New Type AVFoundation.AVAudioUnitDistortion

```
public class AVAudioUnitDistortion : AVFoundation.AVAudioUnitEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitDistortion ();
	public AVAudioUnitDistortion (Foundation.NSObjectFlag t);
	public AVAudioUnitDistortion (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PreGain { get; set; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitDistortionPreset preset);
}
```

### New Type AVFoundation.AVAudioUnitDistortionPreset

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

### New Type AVFoundation.AVAudioUnitEffect

```
public class AVAudioUnitEffect : AVFoundation.AVAudioUnit, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEffect (Foundation.NSObjectFlag t);
	public AVAudioUnitEffect (System.IntPtr handle);
	public AVAudioUnitEffect (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type AVFoundation.AVAudioUnitEQ

```
public class AVAudioUnitEQ : AVFoundation.AVAudioUnitEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQ ();
	public AVAudioUnitEQ (Foundation.NSObjectFlag t);
	public AVAudioUnitEQ (System.IntPtr handle);
	public AVAudioUnitEQ (System.nuint numberOfBands);
	// properties
	public virtual AVAudioUnitEQFilterParameters[] Bands { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalGain { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type AVFoundation.AVAudioUnitEQFilterParameters

```
public class AVAudioUnitEQFilterParameters : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitEQFilterParameters (Foundation.NSObjectFlag t);
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

### New Type AVFoundation.AVAudioUnitEQFilterType

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

### New Type AVFoundation.AVAudioUnitGenerator

```
public class AVAudioUnitGenerator : AVFoundation.AVAudioUnit, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitGenerator (Foundation.NSObjectFlag t);
	public AVAudioUnitGenerator (System.IntPtr handle);
	public AVAudioUnitGenerator (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
}
```

### New Type AVFoundation.AVAudioUnitMidiInstrument

```
public class AVAudioUnitMidiInstrument : AVFoundation.AVAudioUnit, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitMidiInstrument (Foundation.NSObjectFlag t);
	public AVAudioUnitMidiInstrument (System.IntPtr handle);
	public AVAudioUnitMidiInstrument (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void SendController (byte controller, byte value, byte channel);
	public virtual void SendMidiEvent (byte midiStatus, byte data1, byte data2);
	public virtual void SendMidiEvent (byte midiStatus, byte data1);
	public virtual void SendMidiSysExEvent (Foundation.NSData midiData);
	public virtual void SendPitchBend (ushort pitchbend, byte channel);
	public virtual void SendPressure (byte pressure, byte channel);
	public virtual void SendPressureForKey (byte key, byte value, byte channel);
	public virtual void SendProgramChange (byte program, byte channel);
	public virtual void SendProgramChange (byte program, byte bankMSB, byte bankLSB, byte channel);
	public virtual void StartNote (byte note, byte velocity, byte channel);
	public virtual void StopNote (byte note, byte channel);
}
```

### New Type AVFoundation.AVAudioUnitReverb

```
public class AVAudioUnitReverb : AVFoundation.AVAudioUnitEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitReverb ();
	public AVAudioUnitReverb (Foundation.NSObjectFlag t);
	public AVAudioUnitReverb (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float WetDryMix { get; set; }
	// methods
	public virtual void LoadFactoryPreset (AVAudioUnitReverbPreset preset);
}
```

### New Type AVFoundation.AVAudioUnitReverbPreset

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

### New Type AVFoundation.AVAudioUnitSampler

```
public class AVAudioUnitSampler : AVFoundation.AVAudioUnitMidiInstrument, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitSampler ();
	public AVAudioUnitSampler (Foundation.NSObjectFlag t);
	public AVAudioUnitSampler (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float GlobalTuning { get; set; }
	public virtual float MasterGain { get; set; }
	public virtual float StereoPan { get; set; }
	// methods
	public virtual bool LoadAudioFiles (Foundation.NSUrl[] audioFiles, out Foundation.NSError outError);
	public virtual bool LoadInstrument (Foundation.NSUrl instrumentUrl, out Foundation.NSError outError);
	public virtual bool LoadSoundBank (Foundation.NSUrl bankUrl, byte program, byte bankMSB, byte bankLSB, out Foundation.NSError outError);
}
```

### New Type AVFoundation.AVAudioUnitTimeEffect

```
public class AVAudioUnitTimeEffect : AVFoundation.AVAudioUnit, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimeEffect (Foundation.NSObjectFlag t);
	public AVAudioUnitTimeEffect (System.IntPtr handle);
	public AVAudioUnitTimeEffect (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public virtual bool Bypass { get; set; }
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type AVFoundation.AVAudioUnitTimePitch

```
public class AVAudioUnitTimePitch : AVFoundation.AVAudioUnitTimeEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitTimePitch ();
	public AVAudioUnitTimePitch (Foundation.NSObjectFlag t);
	public AVAudioUnitTimePitch (System.IntPtr handle);
	public AVAudioUnitTimePitch (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Overlap { get; set; }
	public virtual float Pitch { get; set; }
	public virtual float Rate { get; set; }
}
```

### New Type AVFoundation.AVAudioUnitVarispeed

```
public class AVAudioUnitVarispeed : AVFoundation.AVAudioUnitTimeEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitVarispeed ();
	public AVAudioUnitVarispeed (Foundation.NSObjectFlag t);
	public AVAudioUnitVarispeed (System.IntPtr handle);
	public AVAudioUnitVarispeed (AudioUnit.AudioComponentDescription audioComponentDescription);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rate { get; set; }
}
```

### New Type AVFoundation.AVCaptureBracketedStillImageSettings

```
public class AVCaptureBracketedStillImageSettings : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureBracketedStillImageSettings (Foundation.NSObjectFlag t);
	public AVCaptureBracketedStillImageSettings (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type AVFoundation.AVCaptureDeviceFormat

```
public class AVCaptureDeviceFormat : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVCaptureDeviceFormat (Foundation.NSObjectFlag t);
	public AVCaptureDeviceFormat (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreMedia.CMFormatDescription FormatDescription { get; }
	public virtual Foundation.NSString MediaType { get; }
	public virtual AVFrameRateRange[] VideoSupportedFrameRateRanges { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type AVFoundation.AVCaptureWhiteBalanceChromaticityValues

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

### New Type AVFoundation.AVCaptureWhiteBalanceGains

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

### New Type AVFoundation.AVCaptureWhiteBalanceTemperatureAndTintValues

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

### New Type AVFoundation.AVMetadataIdentifiers

```
public static class AVMetadataIdentifiers {

	// inner types
	public static class CommonIdentifier {
		// properties
		public static Foundation.NSString AlbumName { get; }
		public static Foundation.NSString Artist { get; }
		public static Foundation.NSString Artwork { get; }
		public static Foundation.NSString AssetIdentifier { get; }
		public static Foundation.NSString Author { get; }
		public static Foundation.NSString Contributor { get; }
		public static Foundation.NSString Copyrights { get; }
		public static Foundation.NSString CreationDate { get; }
		public static Foundation.NSString Creator { get; }
		public static Foundation.NSString Description { get; }
		public static Foundation.NSString Format { get; }
		public static Foundation.NSString Language { get; }
		public static Foundation.NSString LastModifiedDate { get; }
		public static Foundation.NSString Location { get; }
		public static Foundation.NSString Make { get; }
		public static Foundation.NSString Model { get; }
		public static Foundation.NSString Publisher { get; }
		public static Foundation.NSString Relation { get; }
		public static Foundation.NSString Software { get; }
		public static Foundation.NSString Source { get; }
		public static Foundation.NSString Subject { get; }
		public static Foundation.NSString Title { get; }
		public static Foundation.NSString Type { get; }
	}
	public static class QuickTime {
		// properties
		public static Foundation.NSString UserDataAlbum { get; }
		public static Foundation.NSString UserDataArranger { get; }
		public static Foundation.NSString UserDataArtist { get; }
		public static Foundation.NSString UserDataAuthor { get; }
		public static Foundation.NSString UserDataChapter { get; }
		public static Foundation.NSString UserDataComment { get; }
		public static Foundation.NSString UserDataComposer { get; }
		public static Foundation.NSString UserDataCopyright { get; }
		public static Foundation.NSString UserDataCreationDate { get; }
		public static Foundation.NSString UserDataCredits { get; }
		public static Foundation.NSString UserDataDescription { get; }
		public static Foundation.NSString UserDataDirector { get; }
		public static Foundation.NSString UserDataDisclaimer { get; }
		public static Foundation.NSString UserDataEncodedBy { get; }
		public static Foundation.NSString UserDataFullName { get; }
		public static Foundation.NSString UserDataGenre { get; }
		public static Foundation.NSString UserDataHostComputer { get; }
		public static Foundation.NSString UserDataInformation { get; }
		public static Foundation.NSString UserDataKeywords { get; }
		public static Foundation.NSString UserDataLocationISO6709 { get; }
		public static Foundation.NSString UserDataMake { get; }
		public static Foundation.NSString UserDataModel { get; }
		public static Foundation.NSString UserDataOriginalArtist { get; }
		public static Foundation.NSString UserDataOriginalFormat { get; }
		public static Foundation.NSString UserDataOriginalSource { get; }
		public static Foundation.NSString UserDataPerformers { get; }
		public static Foundation.NSString UserDataPhonogramRights { get; }
		public static Foundation.NSString UserDataProducer { get; }
		public static Foundation.NSString UserDataProduct { get; }
		public static Foundation.NSString UserDataPublisher { get; }
		public static Foundation.NSString UserDataSoftware { get; }
		public static Foundation.NSString UserDataSpecialPlaybackRequirements { get; }
		public static Foundation.NSString UserDataTaggedCharacteristic { get; }
		public static Foundation.NSString UserDataTrack { get; }
		public static Foundation.NSString UserDataTrackName { get; }
		public static Foundation.NSString UserDataUrlLink { get; }
		public static Foundation.NSString UserDataWarning { get; }
		public static Foundation.NSString UserDataWriter { get; }
	}
	public static class Iso {
		// properties
		public static Foundation.NSString UserDataCopyright { get; }
		public static Foundation.NSString UserDataTaggedCharacteristic { get; }
	}
	public static class ThreeGP {
		// properties
		public static Foundation.NSString UserDataAlbumAndTrack { get; }
		public static Foundation.NSString UserDataAuthor { get; }
		public static Foundation.NSString UserDataCollection { get; }
		public static Foundation.NSString UserDataCopyright { get; }
		public static Foundation.NSString UserDataDescription { get; }
		public static Foundation.NSString UserDataGenre { get; }
		public static Foundation.NSString UserDataKeywordList { get; }
		public static Foundation.NSString UserDataLocation { get; }
		public static Foundation.NSString UserDataMediaClassification { get; }
		public static Foundation.NSString UserDataMediaRating { get; }
		public static Foundation.NSString UserDataPerformer { get; }
		public static Foundation.NSString UserDataRecordingYear { get; }
		public static Foundation.NSString UserDataThumbnail { get; }
		public static Foundation.NSString UserDataTitle { get; }
		public static Foundation.NSString UserDataUserRating { get; }
	}
	public static class QuickTimeMetadata {
		// properties
		public static Foundation.NSString Album { get; }
		public static Foundation.NSString Arranger { get; }
		public static Foundation.NSString Artist { get; }
		public static Foundation.NSString Artwork { get; }
		public static Foundation.NSString Author { get; }
		public static Foundation.NSString CameraFrameReadoutTime { get; }
		public static Foundation.NSString CameraIdentifier { get; }
		public static Foundation.NSString CollectionUser { get; }
		public static Foundation.NSString Comment { get; }
		public static Foundation.NSString Composer { get; }
		public static Foundation.NSString Copyright { get; }
		public static Foundation.NSString CreationDate { get; }
		public static Foundation.NSString Credits { get; }
		public static Foundation.NSString Description { get; }
		public static Foundation.NSString DirectionFacing { get; }
		public static Foundation.NSString DirectionMotion { get; }
		public static Foundation.NSString Director { get; }
		public static Foundation.NSString DisplayName { get; }
		public static Foundation.NSString EncodedBy { get; }
		public static Foundation.NSString Genre { get; }
		public static Foundation.NSString Information { get; }
		public static Foundation.NSString iXML { get; }
		public static Foundation.NSString Keywords { get; }
		public static Foundation.NSString LocationBody { get; }
		public static Foundation.NSString LocationDate { get; }
		public static Foundation.NSString LocationISO6709 { get; }
		public static Foundation.NSString LocationName { get; }
		public static Foundation.NSString LocationNote { get; }
		public static Foundation.NSString LocationRole { get; }
		public static Foundation.NSString Make { get; }
		public static Foundation.NSString Model { get; }
		public static Foundation.NSString OriginalArtist { get; }
		public static Foundation.NSString Performer { get; }
		public static Foundation.NSString PhonogramRights { get; }
		public static Foundation.NSString PreferredAffineTransform { get; }
		public static Foundation.NSString Producer { get; }
		public static Foundation.NSString Publisher { get; }
		public static Foundation.NSString RatingUser { get; }
		public static Foundation.NSString Software { get; }
		public static Foundation.NSString Title { get; }
		public static Foundation.NSString Year { get; }
	}
	public static class iTunesMetadata {
		// properties
		public static Foundation.NSString AccountKind { get; }
		public static Foundation.NSString Acknowledgement { get; }
		public static Foundation.NSString Album { get; }
		public static Foundation.NSString AlbumArtist { get; }
		public static Foundation.NSString AppleID { get; }
		public static Foundation.NSString Arranger { get; }
		public static Foundation.NSString ArtDirector { get; }
		public static Foundation.NSString Artist { get; }
		public static Foundation.NSString ArtistID { get; }
		public static Foundation.NSString Author { get; }
		public static Foundation.NSString BeatsPerMin { get; }
		public static Foundation.NSString Composer { get; }
		public static Foundation.NSString Conductor { get; }
		public static Foundation.NSString ContentRating { get; }
		public static Foundation.NSString Copyright { get; }
		public static Foundation.NSString CoverArt { get; }
		public static Foundation.NSString Credits { get; }
		public static Foundation.NSString Description { get; }
		public static Foundation.NSString Director { get; }
		public static Foundation.NSString DiscCompilation { get; }
		public static Foundation.NSString DiscNumber { get; }
		public static Foundation.NSString EncodedBy { get; }
		public static Foundation.NSString EncodingTool { get; }
		public static Foundation.NSString EQ { get; }
		public static Foundation.NSString ExecProducer { get; }
		public static Foundation.NSString GenreID { get; }
		public static Foundation.NSString Grouping { get; }
		public static Foundation.NSString LinerNotes { get; }
		public static Foundation.NSString Lyrics { get; }
		public static Foundation.NSString OnlineExtras { get; }
		public static Foundation.NSString OriginalArtist { get; }
		public static Foundation.NSString Performer { get; }
		public static Foundation.NSString PhonogramRights { get; }
		public static Foundation.NSString PlaylistID { get; }
		public static Foundation.NSString PredefinedGenre { get; }
		public static Foundation.NSString Producer { get; }
		public static Foundation.NSString Publisher { get; }
		public static Foundation.NSString RecordCompany { get; }
		public static Foundation.NSString ReleaseDate { get; }
		public static Foundation.NSString Soloist { get; }
		public static Foundation.NSString SongID { get; }
		public static Foundation.NSString SongName { get; }
		public static Foundation.NSString SoundEngineer { get; }
		public static Foundation.NSString Thanks { get; }
		public static Foundation.NSString TrackNumber { get; }
		public static Foundation.NSString TrackSubTitle { get; }
		public static Foundation.NSString UserComment { get; }
		public static Foundation.NSString UserGenre { get; }
	}
	public static class ID3Metadata {
		// properties
		public static Foundation.NSString AlbumSortOrder { get; }
		public static Foundation.NSString AlbumTitle { get; }
		public static Foundation.NSString AttachedPicture { get; }
		public static Foundation.NSString AudioEncryption { get; }
		public static Foundation.NSString AudioSeekPointIndex { get; }
		public static Foundation.NSString Band { get; }
		public static Foundation.NSString BeatsPerMinute { get; }
		public static Foundation.NSString Comments { get; }
		public static Foundation.NSString CommercialInformation { get; }
		public static Foundation.NSString Commerical { get; }
		public static Foundation.NSString Composer { get; }
		public static Foundation.NSString Conductor { get; }
		public static Foundation.NSString ContentGroupDescription { get; }
		public static Foundation.NSString ContentType { get; }
		public static Foundation.NSString Copyright { get; }
		public static Foundation.NSString CopyrightInformation { get; }
		public static Foundation.NSString Date { get; }
		public static Foundation.NSString EncodedBy { get; }
		public static Foundation.NSString EncodedWith { get; }
		public static Foundation.NSString EncodingTime { get; }
		public static Foundation.NSString Encryption { get; }
		public static Foundation.NSString Equalization { get; }
		public static Foundation.NSString Equalization2 { get; }
		public static Foundation.NSString EventTimingCodes { get; }
		public static Foundation.NSString FileOwner { get; }
		public static Foundation.NSString FileType { get; }
		public static Foundation.NSString GeneralEncapsulatedObject { get; }
		public static Foundation.NSString GroupIdentifier { get; }
		public static Foundation.NSString InitialKey { get; }
		public static Foundation.NSString InternationalStandardRecordingCode { get; }
		public static Foundation.NSString InternetRadioStationName { get; }
		public static Foundation.NSString InternetRadioStationOwner { get; }
		public static Foundation.NSString InvolvedPeopleList_v23 { get; }
		public static Foundation.NSString InvolvedPeopleList_v24 { get; }
		public static Foundation.NSString Language { get; }
		public static Foundation.NSString LeadPerformer { get; }
		public static Foundation.NSString Length { get; }
		public static Foundation.NSString Link { get; }
		public static Foundation.NSString Lyricist { get; }
		public static Foundation.NSString MediaType { get; }
		public static Foundation.NSString ModifiedBy { get; }
		public static Foundation.NSString Mood { get; }
		public static Foundation.NSString MpegLocationLookupTable { get; }
		public static Foundation.NSString MusicCDIdentifier { get; }
		public static Foundation.NSString MusicianCreditsList { get; }
		public static Foundation.NSString OfficialArtistWebpage { get; }
		public static Foundation.NSString OfficialAudioFileWebpage { get; }
		public static Foundation.NSString OfficialAudioSourceWebpage { get; }
		public static Foundation.NSString OfficialInternetRadioStationHomepage { get; }
		public static Foundation.NSString OfficialPublisherWebpage { get; }
		public static Foundation.NSString OriginalAlbumTitle { get; }
		public static Foundation.NSString OriginalArtist { get; }
		public static Foundation.NSString OriginalFilename { get; }
		public static Foundation.NSString OriginalLyricist { get; }
		public static Foundation.NSString OriginalReleaseTime { get; }
		public static Foundation.NSString OriginalReleaseYear { get; }
		public static Foundation.NSString Ownership { get; }
		public static Foundation.NSString PartOfASet { get; }
		public static Foundation.NSString Payment { get; }
		public static Foundation.NSString PerformerSortOrder { get; }
		public static Foundation.NSString PlayCounter { get; }
		public static Foundation.NSString PlaylistDelay { get; }
		public static Foundation.NSString Popularimeter { get; }
		public static Foundation.NSString PositionSynchronization { get; }
		public static Foundation.NSString Private { get; }
		public static Foundation.NSString ProducedNotice { get; }
		public static Foundation.NSString Publisher { get; }
		public static Foundation.NSString RecommendedBufferSize { get; }
		public static Foundation.NSString RecordingDates { get; }
		public static Foundation.NSString RecordingTime { get; }
		public static Foundation.NSString RelativeVolumeAdjustment { get; }
		public static Foundation.NSString RelativeVolumeAdjustment2 { get; }
		public static Foundation.NSString ReleaseTime { get; }
		public static Foundation.NSString Reverb { get; }
		public static Foundation.NSString Seek { get; }
		public static Foundation.NSString SetSubtitle { get; }
		public static Foundation.NSString Signature { get; }
		public static Foundation.NSString Size { get; }
		public static Foundation.NSString SubTitle { get; }
		public static Foundation.NSString SynchronizedLyric { get; }
		public static Foundation.NSString SynchronizedTempoCodes { get; }
		public static Foundation.NSString TaggingTime { get; }
		public static Foundation.NSString TermsOfUse { get; }
		public static Foundation.NSString Time { get; }
		public static Foundation.NSString TitleDescription { get; }
		public static Foundation.NSString TitleSortOrder { get; }
		public static Foundation.NSString TrackNumber { get; }
		public static Foundation.NSString UniqueFileIdentifier { get; }
		public static Foundation.NSString UnsynchronizedLyric { get; }
		public static Foundation.NSString UserText { get; }
		public static Foundation.NSString UserUrl { get; }
		public static Foundation.NSString Year { get; }
	}
	public static class IcyMetadata {
		// properties
		public static Foundation.NSString StreamTitle { get; }
		public static Foundation.NSString StreamUrl { get; }
	}
}
```

### New Type AVFoundation.AVMidiPlayer

```
public class AVMidiPlayer : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMidiPlayer ();
	public AVMidiPlayer (Foundation.NSObjectFlag t);
	public AVMidiPlayer (System.IntPtr handle);
	public AVMidiPlayer (Foundation.NSUrl contentsUrl, Foundation.NSUrl soundBankUrl, out Foundation.NSError outError);
	public AVMidiPlayer (Foundation.NSData data, Foundation.NSUrl sounddBankUrl, out Foundation.NSError outError);
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

### New Type AVFoundation.AVPlayerItemMetadataOutput

```
public class AVPlayerItemMetadataOutput : AVFoundation.AVPlayerItemOutput, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutput ();
	public AVPlayerItemMetadataOutput (Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutput (System.IntPtr handle);
	public AVPlayerItemMetadataOutput (Foundation.NSString[] metadataIdentifiers);
	// properties
	public virtual double AdvanceIntervalForDelegateInvocation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public AVPlayerItemMetadataOutputPushDelegate Delegate { get; }
	public virtual CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual Foundation.NSObject WeakDelegate { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemMetadataOutputPushDelegate pushDelegate, CoreFoundation.DispatchQueue delegateQueue);
}
```

### New Type AVFoundation.AVPlayerItemMetadataOutputPushDelegate

```
public class AVPlayerItemMetadataOutputPushDelegate : Foundation.NSObject, IAVPlayerItemMetadataOutputPushDelegate, IAVPlayerItemOutputPushDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemMetadataOutputPushDelegate ();
	public AVPlayerItemMetadataOutputPushDelegate (Foundation.NSObjectFlag t);
	public AVPlayerItemMetadataOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void DidOutputTimedMetadataGroups (AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
```

### New Type AVFoundation.AVPlayerItemMetadataOutputPushDelegate_Extensions

```
public static class AVPlayerItemMetadataOutputPushDelegate_Extensions {
	// methods
	public static void DidOutputTimedMetadataGroups (IAVPlayerItemMetadataOutputPushDelegate This, AVPlayerItemMetadataOutput output, AVTimedMetadataGroup[] groups, AVPlayerItemTrack track);
}
```

### New Type AVFoundation.AVQueuedSampleBufferRenderingStatus

```
[Serializable]
public enum AVQueuedSampleBufferRenderingStatus {
	Failed = 2,
	Rendering = 1,
	Unknown = 0,
}
```

### New Type AVFoundation.AVSampleBufferDisplayLayer

```
public class AVSampleBufferDisplayLayer : CoreAnimation.CALayer, CoreAnimation.ICAMediaTiming, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVSampleBufferDisplayLayer ();
	public AVSampleBufferDisplayLayer (Foundation.NSCoder coder);
	public AVSampleBufferDisplayLayer (Foundation.NSObjectFlag t);
	public AVSampleBufferDisplayLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreMedia.CMTimebase ControlTimebase { get; set; }
	public virtual Foundation.NSError Error { get; }
	public virtual bool ReadyForMoreMediaData { get; }
	public virtual AVQueuedSampleBufferRenderingStatus Status { get; }
	public virtual string VideoGravity { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EnqueueSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer);
	public virtual void Flush ();
	public virtual void FlushAndRemoveImage ();
	public virtual void RequestMediaDataWhenReadyOnQueue (CoreFoundation.DispatchQueue queue, System.Action enqueuer);
	public virtual void StopRequestingMediaData ();
}
```

### New Type AVFoundation.AVUtilities

```
public static class AVUtilities {
	// methods
	public static CoreGraphics.CGRect WithAspectRatio (CoreGraphics.CGRect self, CoreGraphics.CGSize aspectRatio);
}
```

### New Type AVFoundation.IAVAudio3DMixing

```
public interface IAVAudio3DMixing : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
}
```

### New Type AVFoundation.IAVAudioMixing

```
public interface IAVAudioMixing : ObjCRuntime.INativeObject, System.IDisposable, IAVAudio3DMixing, IAVAudioStereoMixing {
	// properties
	public virtual float Volume { get; set; }
}
```

### New Type AVFoundation.IAVAudioStereoMixing

```
public interface IAVAudioStereoMixing : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual float Pan { get; set; }
}
```

### New Type AVFoundation.IAVPlayerItemMetadataOutputPushDelegate

```
public interface IAVPlayerItemMetadataOutputPushDelegate : ObjCRuntime.INativeObject, System.IDisposable, IAVPlayerItemOutputPushDelegate {
}
```

## Namespace CoreAnimation

### Type Changed: CoreAnimation.CAAnimation

Added properties:

```
public virtual SceneKit.SCNAnimationEvent[] AnimationEvents { get; set; }
	public virtual System.nfloat FadeInDuration { get; set; }
	public virtual System.nfloat FadeOutDuration { get; set; }
```

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Added properties:

```
public virtual Foundation.NSNumber[] BiasValues { get; set; }
	public virtual Foundation.NSNumber[] ContinuityValues { get; set; }
	public virtual Foundation.NSNumber[] TensionValues { get; set; }
```

Added method:

```
public static CAKeyFrameAnimation GetFromKeyPath (string path);
```

### Type Changed: CoreAnimation.CALayer

Added properties:

```
public virtual CoreImage.CIFilter[] BackgroundFilters { get; set; }
	public virtual Foundation.NSObject CompositingFilter { get; set; }
	public virtual float MinificationFilterBias { get; set; }
	public virtual Foundation.NSDictionary Style { get; set; }
```

### Type Changed: CoreAnimation.CATransition

Removed property:

```
public virtual Foundation.NSObject filter { get; set; }
```

Added property:

```
public virtual Foundation.NSObject Filter { get; set; }
```

## Namespace CoreBluetooth

### Type Changed: CoreBluetooth.CBAdvertisement

Removed properties:

```
public static Foundation.NSString DataOverflowServiceUUIDsKey { get; }
	public static Foundation.NSString DataSolicitedServiceUUIDsKey { get; }
	public static Foundation.NSString IsConnectable { get; }
```

### Type Changed: CoreBluetooth.CBCentralManager

Removed constructor:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);
```

Removed properties:

```
public static Foundation.NSString OptionShowPowerAlertKey { get; }
	public static Foundation.NSString ScanOptionSolicitedServiceUUIDsKey { get; }
```

Removed methods:

```
public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);
	public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (Foundation.NSUuid[] identifiers);
```

### Type Changed: CoreBluetooth.CBCharacteristic

Removed property:

```
public virtual CBUUID UUID { get; set; }
```

Added property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: CoreBluetooth.CBPeripheral

Removed property:

```
[Obsolete ("Deprecated in iOS7")]
	public virtual System.IntPtr UUID { get; }
```

### Type Changed: CoreBluetooth.CBService

Removed property:

```
public virtual bool Primary { get; }
```

### Removed Type CoreBluetooth.CBATTRequest ### Removed Type CoreBluetooth.CBATTRequestEventArgs ### Removed Type CoreBluetooth.CBATTRequestsEventArgs ### Removed Type CoreBluetooth.CBCentral ### Removed Type CoreBluetooth.CBMutableCharacteristic ### Removed Type CoreBluetooth.CBMutableDescriptor ### Removed Type CoreBluetooth.CBMutableService ### Removed Type CoreBluetooth.CBPeripheralManager ### Removed Type CoreBluetooth.CBPeripheralManagerDelegate ### Removed Type CoreBluetooth.CBPeripheralManagerDelegate_Extensions ### Removed Type CoreBluetooth.CBPeripheralManagerServiceEventArgs ### Removed Type CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs ### Removed Type CoreBluetooth.ICBPeripheralManagerDelegate 



## Namespace CoreData



### Type Changed: CoreData.NSManagedObjectContext

Added property:

```
public virtual string Name { get; set; }
```

Added method:

```
public virtual NSPersistentStoreResult ExecuteRequest (NSPersistentStoreRequest request, out Foundation.NSError error);
```

### Type Changed: CoreData.NSPersistentStoreCoordinator

Removed constructor:

```
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

### Type Changed: CoreData.NSPersistentStoreRequestType

Added value:

```
BatchUpdate = 6,
```

### New Type CoreData.NSAsynchronousFetchRequest

```
public class NSAsynchronousFetchRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchRequest ();
	public NSAsynchronousFetchRequest (Foundation.NSObjectFlag t);
	public NSAsynchronousFetchRequest (System.IntPtr handle);
	public NSAsynchronousFetchRequest (NSFetchRequest request, System.Action<NSAsynchronousFetchResult> completion);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nint EstimatedResultCount { get; set; }
	public virtual NSFetchRequest FetchRequest { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CoreData.NSAsynchronousFetchResult

```
public class NSAsynchronousFetchResult : CoreData.NSPersistentStoreAsynchronousResult, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAsynchronousFetchResult ();
	public NSAsynchronousFetchResult (Foundation.NSObjectFlag t);
	public NSAsynchronousFetchResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSAsynchronousFetchRequest FetchRequest { get; }
	public virtual Foundation.NSObject[] FinalResult { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CoreData.NSBatchUpdateRequest

```
public class NSBatchUpdateRequest : CoreData.NSPersistentStoreRequest, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateRequest ();
	public NSBatchUpdateRequest (Foundation.NSObjectFlag t);
	public NSBatchUpdateRequest (System.IntPtr handle);
	public NSBatchUpdateRequest (string entityName);
	public NSBatchUpdateRequest (NSEntityDescription entity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSEntityDescription Entity { get; }
	public virtual string EntityName { get; }
	public virtual bool IncludesSubentities { get; set; }
	public virtual Foundation.NSPredicate Predicate { get; set; }
	public virtual Foundation.NSDictionary PropertiesToUpdate { get; set; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; set; }
	// methods
	public static NSBatchUpdateRequest BatchUpdateRequestWithEntityName (string entityName);
	protected override void Dispose (bool disposing);
}
```

### New Type CoreData.NSBatchUpdateRequestResultType

```
[Serializable]
public enum NSBatchUpdateRequestResultType {
	StatusOnly = 0,
	UpdatedObjectIDs = 1,
	UpdatedObjectsCount = 2,
}
```

### New Type CoreData.NSBatchUpdateResult

```
public class NSBatchUpdateResult : CoreData.NSPersistentStoreResult, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchUpdateResult ();
	public NSBatchUpdateResult (Foundation.NSObjectFlag t);
	public NSBatchUpdateResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject Result { get; }
	public virtual NSBatchUpdateRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CoreData.NSPersistentStoreAsynchronousResult

```
public class NSPersistentStoreAsynchronousResult : CoreData.NSPersistentStoreResult, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreAsynchronousResult ();
	public NSPersistentStoreAsynchronousResult (Foundation.NSObjectFlag t);
	public NSPersistentStoreAsynchronousResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual NSManagedObjectContext ManagedObjectContext { get; }
	public virtual Foundation.NSError OperationError { get; }
	public virtual Foundation.NSProgress Progress { get; }
	// methods
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
}
```

### New Type CoreData.NSPersistentStoreResult

```
public class NSPersistentStoreResult : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersistentStoreResult ();
	public NSPersistentStoreResult (Foundation.NSObjectFlag t);
	public NSPersistentStoreResult (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

## Namespace CoreGraphics



### Type Changed: CoreGraphics.CGVector

Removed method:

```
public override string ToString ();
```

## Namespace CoreImage



### Type Changed: CoreImage.CIAutoAdjustmentFilterOptions

Added fields:

```
public bool? AutoAdjustCrop;
	public bool? AutoAdjustLevel;
```

### Type Changed: CoreImage.CIColor

Added property:

```
public float[] Components { get; }
```

### Type Changed: CoreImage.CIContextOptions

Added properties:

```
public int? CIImageFormat { get; set; }
	public bool? PriorityRequestLow { get; set; }
```

### Type Changed: CoreImage.CIDetector

Added properties:

```
public static Foundation.NSString AspectRatio { get; }
	public static Foundation.NSString FocalLength { get; }
	public static Foundation.NSString TypeQRCode { get; }
	public static Foundation.NSString TypeRectangle { get; }
```

Added methods:

```
public static CIDetector CreateQRDetector (CIContext context, CIDetectorOptions detectorOptions);
	public static CIDetector CreateRectangleDetector (CIContext context, CIDetectorOptions detectorOptions);
```

### Type Changed: CoreImage.CIDetectorOptions

Added properties:

```
public float? AspectRatio { get; set; }
	public float? FocalLength { get; set; }
```

### Type Changed: CoreImage.CIFilter

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
public static CIFilter GetFilter (string name, Foundation.NSDictionary inputParameters);
```

### Type Changed: CoreImage.CIImage

Added methods:

```
public virtual CIImage CreateByClampingToExtent ();
	public virtual CIImage CreateByCompositingOverImage (CIImage dest);
	public virtual CIImage CreateByFiltering (string filterName, Foundation.NSDictionary inputParameters);
	public virtual CIImage CreateWithOrientation (CIImageOrientation orientation);
	public virtual CoreGraphics.CGAffineTransform GetImageTransform (CIImageOrientation orientation);
```

### Type Changed: CoreImage.CIKernel

Removed method:

```
public static CIKernel[] FromProgram (string coreImageShaderProgram);
```

Added methods:

```
public static CIKernel FromProgram (string coreImageShaderProgram);
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
```

### Type Changed: CoreImage.CIVector

Added constructors:

```
public CIVector (CoreGraphics.CGAffineTransform r);
	public CIVector (CoreGraphics.CGRect r);
	public CIVector (CoreGraphics.CGPoint p);
```

### New Type CoreImage.CIAccordionFoldTransition

```
public class CIAccordionFoldTransition : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAccordionFoldTransition ();
	public CIAccordionFoldTransition (System.IntPtr handle);
}
```

### New Type CoreImage.CIAreaHistogram

```
public class CIAreaHistogram : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAreaHistogram ();
	public CIAreaHistogram (System.IntPtr handle);
	// properties
	public float Count { get; set; }
	public CIVector Extent { get; set; }
	public float Scale { get; set; }
}
```

### New Type CoreImage.CIAztecCodeGenerator

```
public class CIAztecCodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIAztecCodeGenerator ();
	public CIAztecCodeGenerator (System.IntPtr handle);
}
```

### New Type CoreImage.CIBarcodeFeature

```
public class CIBarcodeFeature : CoreImage.CIFeature, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIBarcodeFeature ();
	public CIBarcodeFeature (Foundation.NSObjectFlag t);
	public CIBarcodeFeature (System.IntPtr handle);
	// properties
	public virtual CoreGraphics.CGPoint BottomLeft { get; }
	public virtual CoreGraphics.CGPoint BottomRight { get; }
	public virtual CoreGraphics.CGRect Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSData CodeRawData { get; }
	public virtual string CodeString { get; }
	public virtual string CodeType { get; }
	public virtual Foundation.NSNumber ErrorCorrectionLevel { get; }
	public virtual CoreGraphics.CGPoint TopLeft { get; }
	public virtual CoreGraphics.CGPoint TopRight { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CoreImage.CICode128BarcodeGenerator

```
public class CICode128BarcodeGenerator : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CICode128BarcodeGenerator ();
	public CICode128BarcodeGenerator (System.IntPtr handle);
}
```

### New Type CoreImage.CIDivideBlendMode

```
public class CIDivideBlendMode : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIDivideBlendMode ();
	public CIDivideBlendMode (System.IntPtr handle);
}
```

### New Type CoreImage.CIGlassDistortion

```
public class CIGlassDistortion : CoreImage.CIDistortionFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIGlassDistortion ();
	public CIGlassDistortion (System.IntPtr handle);
	// properties
	public float Scale { get; set; }
	public CIImage Texture { get; set; }
}
```

### New Type CoreImage.CIHistogramDisplayFilter

```
public class CIHistogramDisplayFilter : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIHistogramDisplayFilter ();
	public CIHistogramDisplayFilter (System.IntPtr handle);
	// properties
	public float Height { get; set; }
	public float HighLimit { get; set; }
	public float LowLimit { get; set; }
}
```

### New Type CoreImage.CILinearBurnBlendMode

```
public class CILinearBurnBlendMode : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearBurnBlendMode ();
	public CILinearBurnBlendMode (System.IntPtr handle);
}
```

### New Type CoreImage.CILinearDodgeBlendMode

```
public class CILinearDodgeBlendMode : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILinearDodgeBlendMode ();
	public CILinearDodgeBlendMode (System.IntPtr handle);
}
```

### New Type CoreImage.CIPinLightBlendMode

```
public class CIPinLightBlendMode : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPinLightBlendMode ();
	public CIPinLightBlendMode (System.IntPtr handle);
}
```

### New Type CoreImage.CIRectangleFeature

```
public class CIRectangleFeature : CoreImage.CIFeature, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIRectangleFeature ();
	public CIRectangleFeature (Foundation.NSObjectFlag t);
	public CIRectangleFeature (System.IntPtr handle);
	// properties
	public virtual CoreGraphics.CGPoint BottomLeft { get; }
	public virtual CoreGraphics.CGPoint BottomRight { get; }
	public virtual CoreGraphics.CGRect Bounds { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGPoint TopLeft { get; }
	public virtual CoreGraphics.CGPoint TopRight { get; }
}
```

### New Type CoreImage.CISubtractBlendMode

```
public class CISubtractBlendMode : CoreImage.CIFilter, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CISubtractBlendMode ();
	public CISubtractBlendMode (System.IntPtr handle);
}
```

## Namespace CoreLocation



### Type Changed: CoreLocation.CLLocationManagerDelegate

Removed interface:

```
ICLLocationManagerDelegate
```

### Removed Type CoreLocation.CLLocationManagerDelegate_Extensions ### Removed Type CoreLocation.ICLLocationManagerDelegate 



## Namespace CoreMedia



### Type Changed: CoreMedia.CMFormatDescription

Added method:

```
public Foundation.NSObject GetExtension (string extensionKey);
```

### Type Changed: CoreMedia.CMSampleBuffer

Added methods:

```
public CMSampleBufferError CallForEachSample (System.Func<CMSampleBuffer,System.Int32,CoreMedia.CMSampleBufferError> callback);
	public static CMSampleBuffer CreateReady (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMSampleTimingInfo[] sampleTimingArray, System.nuint[] sampleSizeArray, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithImageBuffer (CoreVideo.CVImageBuffer imageBuffer, CMFormatDescription formatDescription, CMSampleTimingInfo[] sampleTiming, out CMSampleBufferError error);
	public static CMSampleBuffer CreateReadyWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
	public CMSampleBufferError SetInvalidateCallback (System.Action<CMSampleBuffer> invalidateHandler);
```

### Type Changed: CoreMedia.CMTime

Added properties:

```
public bool HasBeenRounded { get; }
	public bool IsNumeric { get; }
```

## Namespace CoreText



### Type Changed: CoreText.CTLineBoundsOptions

Added value:

```
IncludeLanguageExtents = 32,
```

## Namespace CoreVideo



### Type Changed: CoreVideo.CVImageBuffer

Added property:

```
public static Foundation.NSString AlphaChannelIsOpaque { get; }
```

### Type Changed: CoreVideo.CVPixelBufferAttributes

Added property:

```
public bool? AllocateWithIOSurface { get; set; }
```

### Type Changed: CoreVideo.CVPixelBufferPool

Added property:

```
public static Foundation.NSString AlphaChannelIsOpaque { get; }
```

### Type Changed: CoreVideo.CVPixelFormatDescription

Added fields:

```
public static Foundation.NSString ContainsRgb;
	public static Foundation.NSString ContainsYCbCr;
```

### Type Changed: CoreVideo.CVReturn

Added value:

```
PixelBufferNotMetalCompatible = -6684,
```

## Namespace CoreWlan



### Type Changed: CoreWlan.CWChannel

Removed property:

```
public virtual System.nuint ChannelNumber { get; }
```

Added property:

```
public virtual System.nint ChannelNumber { get; }
```

### Type Changed: CoreWlan.CWInterface

Removed property:

```
public virtual System.nuint TransmitPower { get; }
```

Added property:

```
public virtual System.nint TransmitPower { get; }
```

Removed method:

```
public virtual bool SetWEPKey (Foundation.NSData key, CWCipherKeyFlags flags, System.nuint index, out Foundation.NSError error);
```

Added method:

```
public virtual bool SetWEPKey (Foundation.NSData key, CWCipherKeyFlags flags, System.nint index, out Foundation.NSError error);
```

### Type Changed: CoreWlan.CWNetwork

Removed property:

```
public virtual System.nuint BeaconInterval { get; }
```

Added property:

```
public virtual System.nint BeaconInterval { get; }
```

## Namespace Foundation



### Type Changed: Foundation.DictionaryContainer

Added methods:

```
protected uint? GetUInt32Value (NSString key);
	protected void SetArrayValue<T> (NSString key, T[] values);
```

### Type Changed: Foundation.INSMachPortDelegate

Added interface:

```
INSPortDelegate
```

### Type Changed: Foundation.INSUrlConnectionDownloadDelegate

Added interface:

```
INSUrlConnectionDelegate
```

### Type Changed: Foundation.INSUrlSessionDataDelegate

Added interfaces:

```
INSUrlSessionTaskDelegate
	INSUrlSessionDelegate
```

### Type Changed: Foundation.INSUrlSessionDownloadDelegate

Added interfaces:

```
INSUrlSessionTaskDelegate
	INSUrlSessionDelegate
```

### Type Changed: Foundation.INSUrlSessionTaskDelegate

Added interface:

```
INSUrlSessionDelegate
```

### Type Changed: Foundation.NSAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: Foundation.NSBundle

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

### Type Changed: Foundation.NSByteCountFormatter

Added property:

```
public virtual NSFormattingContext FormattingContext { get; set; }
```

### Type Changed: Foundation.NSCachedUrlResponse

Added interface:

```
INSSecureCoding
```

### Type Changed: Foundation.NSCalendar

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
	public virtual NSDate Date (System.nint era, System.nint year, System.nint month, System.nint date, System.nint hour, System.nint minute, System.nint second, System.nint nanosecond);
	public virtual NSDate DateByAddingUnit (NSCalendarUnit unit, System.nint value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingsHour (System.nint hour, System.nint minute, System.nint second, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateBySettingUnit (NSCalendarUnit unit, System.nint value, NSDate date, NSCalendarOptions options);
	public virtual NSDate DateForWeekOfYear (System.nint era, System.nint year, System.nint week, System.nint weekday, System.nint hour, System.nint minute, System.nint second, System.nint nanosecond);
	public virtual void EnumerateDatesStartingAfterDate (NSDate start, NSDateComponents matchingComponents, NSCalendarOptions options, EnumerateDatesCallback callback);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSDateComponents components, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, NSCalendarUnit unit, System.nint value, NSCalendarOptions options);
	public virtual NSDate FindNextDateAfterDateMatching (NSDate date, System.nint hour, System.nint minute, System.nint second, NSCalendarOptions options);
	public virtual bool FindNextWeekend (out NSDate date, out double interval, NSCalendarOptions options, NSDate afterDate);
	public virtual System.nint GetComponentFromDate (NSCalendarUnit unit, NSDate date);
	public virtual void GetComponentsFromDate (out System.nint era, out System.nint year, out System.nint month, out System.nint day, NSDate date);
	public virtual void GetComponentsFromDateForWeekOfYear (out System.nint era, out System.nint year, out System.nint weekOfYear, out System.nint weekday, NSDate date);
	public virtual void GetHourComponentsFromDate (out System.nint hour, out System.nint minute, out System.nint second, out System.nint nanosecond, NSDate date);
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

### Type Changed: Foundation.NSCalendarType

Added values:

```
Coptic = 11,
	EthiopicAmeteAlem = 12,
	EthiopicAmeteMihret = 13,
	IslamicTabular = 14,
	IslamicUmmAlQura = 15,
```

### Type Changed: Foundation.NSCalendarUnit

Added value:

```
Nanosecond = 32768,
```

### Type Changed: Foundation.NSData

Added methods:

```
public virtual bool Save (string path, bool atomically);
	public virtual bool Save (NSUrl url, bool atomically);
```

### Type Changed: Foundation.NSDateComponents

Added properties:

```
public virtual bool IsValidDate { get; }
	public virtual System.nint Nanosecond { get; set; }
```

Added methods:

```
public virtual System.nint GetValueForComponent (NSCalendarUnit unit);
	public virtual bool IsValidDateInCalendar (NSCalendar calendar);
	public virtual void SetValueForComponent (System.nint value, NSCalendarUnit unit);
```

### Type Changed: Foundation.NSDateFormatter

Added method:

```
public virtual void SetLocalizedDateFormatFromTemplate (string dateFormatTemplate);
```

### Type Changed: Foundation.NSError

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

### Type Changed: Foundation.NSFileCoordinator

Added property:

```
public virtual string PurposeIdentifier { get; set; }
```

Added method:

```
public virtual void CoordinateAccessWithIntents (NSFileAccessIntent[] intents, NSOperationQueue queue, System.Action<NSError> accessor);
```

### Type Changed: Foundation.NSFileCoordinatorReadingOptions

Added values:

```
ForUploading = 8,
	ImmediatelyAvailableMetadataOnly = 4,
	ResolvesSymbolicLink = 2,
```

### Type Changed: Foundation.NSFileManager

Added methods:

```
public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
```

### Type Changed: Foundation.NSFilePresenter

Added methods:

```
public virtual void AccommodatePresentedItemDeletion (System.Action<NSError> completionHandler);
	public virtual void AccommodatePresentedSubitemDeletion (NSUrl url, System.Action<NSError> completionHandler);
	public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
	public virtual void SavePresentedItemChanges (System.Action<NSError> completionHandler);
```

### Type Changed: Foundation.NSFilePresenter_Extensions

Added methods:

```
public static void AccommodatePresentedItemDeletion (INSFilePresenter This, System.Action<NSError> completionHandler);
	public static void AccommodatePresentedSubitemDeletion (INSFilePresenter This, NSUrl url, System.Action<NSError> completionHandler);
	public static void RelinquishPresentedItemToReader (INSFilePresenter This, NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, NSFilePresenterReacquirer writerAction);
	public static void SavePresentedItemChanges (INSFilePresenter This, System.Action<NSError> completionHandler);
```

### Type Changed: Foundation.NSHttpCookieStorage

Added methods:

```
public virtual void GetCookiesForTask (NSUrlSessionTask task, System.Action<NSHttpCookie[]> completionHandler);
	public virtual void RemoveCookiesSinceDate (NSDate date);
	public virtual void StoreCookies (NSHttpCookie[] cookies, NSUrlSessionTask task);
```

### Type Changed: Foundation.NSIndexPath

Added interface:

```
INSSecureCoding
```

### Type Changed: Foundation.NSIndexSet

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

### Type Changed: Foundation.NSInputStream

Removed method:

```
public System.nint Read (byte[] buffer, int offset, System.nuint len);
```

### Type Changed: Foundation.NSMachPort

Added constructors:

```
public NSMachPort (uint machPort);
	public NSMachPort (uint machPort, NSMachPortRights options);
```

### Type Changed: Foundation.NSMetadataQuery

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

### Type Changed: Foundation.NSMethodSignature

Added property:

```
public virtual System.IntPtr MethodReturnType { get; }
```

Added methods:

```
public static NSMethodSignature FromObjcTypes (System.IntPtr utf8objctypes);
	public virtual System.IntPtr GetArgumentType (System.nuint index);
```

### Type Changed: Foundation.NSMutableArray

Added methods:

```
public static NSMutableArray FromFile (string path);
	public static NSMutableArray FromUrl (NSUrl url);
```

### Type Changed: Foundation.NSMutableAttributedString

Added interface:

```
INSSecureCoding
```

### Type Changed: Foundation.NSMutableIndexSet

Added interface:

```
INSSecureCoding
```

Added methods:

```
public virtual void AddIndexesInRange (NSRange range);
	public virtual void EncodeTo (NSCoder encoder);
	public virtual void RemoveIndexesInRange (NSRange range);
```

### Type Changed: Foundation.NSObject

Removed method:

```
public static bool IsNewRefcountEnabled ();
```

Added method:

```
public virtual void RemoveObserver (NSObject observer, NSString keyPath, System.IntPtr context);
```

### Type Changed: Foundation.NSOperation

Added properties:

```
public virtual bool Asynchronous { get; }
	public virtual string Name { get; set; }
	public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: Foundation.NSOperationQueue

Added properties:

```
public virtual NSQualityOfService QualityOfService { get; set; }
	public virtual CoreFoundation.DispatchQueue UnderlyingQueue { get; set; }
```

### Type Changed: Foundation.NSOutputStream

Removed methods:

```
public System.nint Write (byte[] buffer);
	public System.nint Write (byte[] buffer, int offset, System.nuint len);
```

### Type Changed: Foundation.NSPort

Added methods:

```
public virtual void RemoveFromRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual void ScheduleInRunLoop (NSRunLoop runLoop, NSString runLoopMode);
	public virtual bool SendBeforeDate (NSDate limitDate, NSMutableArray components, NSPort receivePort, System.nuint headerSpaceReserved);
	public virtual bool SendBeforeDate (NSDate limitDate, System.nuint msgID, NSMutableArray components, NSPort receivePort, System.nuint headerSpaceReserved);
```

### Type Changed: Foundation.NSProcessInfo

Added property:

```
public virtual NSOperatingSystemVersion OperatingSystemVersion { get; }
```

Added method:

```
public virtual bool IsOperatingSystemAtLeastVersion (NSOperatingSystemVersion version);
```

### Type Changed: Foundation.NSSet

Added method:

```
public virtual NSObject LookupMember (NSObject probe);
```

### Type Changed: Foundation.NSStream

Added methods:

```
public static void GetBoundStreams (System.nuint bufferSize, out NSInputStream inputStream, out NSOutputStream outputStream);
	public static void GetStreamsToHost (string hostname, System.nint port, out NSInputStream inputStream, out NSOutputStream outputStream);
```

### Type Changed: Foundation.NSString

Added methods:

```
public virtual bool Contains (NSString str);
	public static System.nuint DetectStringEncoding (NSData rawData, NSDictionary options, out string convertedString, out bool usedLossyConversion);
	public static System.nuint DetectStringEncoding (NSData rawData, EncodingDetectionOptions options, out string convertedString, out bool usedLossyConversion);
	public virtual bool LocalizedCaseInsensitiveContains (NSString str);
```

### Type Changed: Foundation.NSThread

Added property:

```
public virtual NSQualityOfService QualityOfService { get; set; }
```

### Type Changed: Foundation.NSUrl

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

Removed methods:

```
public bool SetResource (string key, NSObject value, out NSError error);
	public bool SetResource (string key, NSObject value);
	public bool TryGetResource (string key, out NSObject value, out NSError error);
	public bool TryGetResource (string key, out NSObject value);
```

Added methods:

```
public virtual NSUrl AppendPathExtension (string extension);
	public static NSUrl CreateFileUrl (string[] pathComponents);
	public virtual NSUrl RemoveLastPathComponent ();
	public virtual NSUrl RemovePathExtension ();
	public static NSUrl ResolveAlias (NSUrl aliasFileUrl, NSUrlBookmarkResolutionOptions options, out NSError error);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value);
	public bool SetResource (NSString nsUrlResourceKey, NSObject value, out NSError error);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value, out NSError error);
	public bool TryGetResource (NSString nsUrlResourceKey, out NSObject value);
```

### Type Changed: Foundation.NSUrlCache

Added methods:

```
public virtual void GetCachedResponse (NSUrlSessionDataTask dataTask, System.Action<NSCachedUrlResponse> completionHandler);
	public virtual System.Threading.Tasks.Task<NSCachedUrlResponse> GetCachedResponseAsync (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponse (NSUrlSessionDataTask dataTask);
	public virtual void RemoveCachedResponsesSinceDate (NSDate date);
	public virtual void StoreCachedResponse (NSCachedUrlResponse cachedResponse, NSUrlSessionDataTask dataTask);
```

### Type Changed: Foundation.NSUrlComponents

Added property:

```
public virtual NSUrlQueryItem[] QueryItems { get; set; }
```

Added method:

```
public virtual string AsString ();
```

### Type Changed: Foundation.NSUrlProtocol

Removed constructor:

```
public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, NSUrlProtocolClient client);
```

Added constructor:

```
public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, INSUrlProtocolClient client);
```

Added property:

```
public INSUrlProtocolClient Client { get; }
```

### Type Changed: Foundation.NSUrlSession

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

### Type Changed: Foundation.NSUrlSessionDataTask

Removed constructor:

```
public NSUrlSessionDataTask (NSCoder coder);
```

Removed interface:

```
INSCoding
```

### Type Changed: Foundation.NSUrlSessionDownloadTask

Removed constructor:

```
public NSUrlSessionDownloadTask (NSCoder coder);
```

Removed interface:

```
INSCoding
```

### Type Changed: Foundation.NSUrlSessionDownloadTaskRequest

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

### Type Changed: Foundation.NSUrlSessionTask

Removed constructor:

```
public NSUrlSessionTask (NSCoder coder);
```

Removed interface:

```
INSCoding
```

Added property:

```
public virtual float Priority { get; set; }
```

Removed method:

```
public virtual void EncodeTo (NSCoder encoder);
```

### Type Changed: Foundation.NSUrlSessionUploadTask

Removed constructor:

```
public NSUrlSessionUploadTask (NSCoder coder);
```

Removed interface:

```
INSCoding
```

### Type Changed: Foundation.NSValue

Added properties:

```
public virtual CoreAnimation.CATransform3D CATransform3DValue { get; }
	public virtual SceneKit.SCNMatrix4 SCNMatrix4Value { get; }
```

Added methods:

```
public static NSValue FromCATransform3D (CoreAnimation.CATransform3D transform);
	public static NSValue FromSCNMatrix4 (SceneKit.SCNMatrix4 matrix);
```

### Removed Type Foundation.NSUrlProtocolClient ### New Type Foundation.EncodingDetectionOptions

```
public class EncodingDetectionOptions : Foundation.DictionaryContainer {
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

### New Type Foundation.EnumerateDatesCallback

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

### New Type Foundation.EnumerateIndexSetCallback

```
public sealed delegate EnumerateIndexSetCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public EnumerateIndexSetCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.nuint idx, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (System.nuint idx, ref bool stop);
}
```

### New Type Foundation.INSExtensionRequestHandling

```
public interface INSExtensionRequestHandling : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
}
```

### New Type Foundation.INSUrlProtocolClient

```
public interface INSUrlProtocolClient : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
	public virtual void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
	public virtual void DataLoaded (NSUrlProtocol protocol, NSData data);
	public virtual void FailedWithError (NSUrlProtocol protocol, NSError error);
	public virtual void FinishedLoading (NSUrlProtocol protocol);
	public virtual void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
	public virtual void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
	public virtual void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
}
```

### New Type Foundation.INSUserActivityDelegate

```
public interface INSUserActivityDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type Foundation.NSAppleScript

```
public class NSAppleScript : Foundation.NSObject, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
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

### New Type Foundation.NSCocoaError

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

### New Type Foundation.NSDateComponentsFormatter

```
public class NSDateComponentsFormatter : Foundation.NSFormatter, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual System.nint MaximumUnitCount { get; set; }
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

### New Type Foundation.NSDateComponentsFormatterUnitsStyle

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

### New Type Foundation.NSDateComponentsFormatterZeroFormattingBehavior

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

### New Type Foundation.NSDateIntervalFormatter

```
public class NSDateIntervalFormatter : Foundation.NSFormatter, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type Foundation.NSDateIntervalFormatterStyle

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

### New Type Foundation.NSEnergyFormatter

```
public class NSEnergyFormatter : Foundation.NSFormatter, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type Foundation.NSEnergyFormatterUnit

```
[Serializable]
public enum NSEnergyFormatterUnit {
	Calorie = 1793,
	Joule = 11,
	Kilocalorie = 1794,
	Kilojoule = 14,
}
```

### New Type Foundation.NSExtensionContext

```
public class NSExtensionContext : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionContext ();
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

### New Type Foundation.NSExtensionItem

```
public class NSExtensionItem : Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual void EncodeTo (NSCoder encoder);
}
```

### New Type Foundation.NSExtensionRequestHandling

```
public abstract class NSExtensionRequestHandling : Foundation.NSObject, INSExtensionRequestHandling, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSExtensionRequestHandling ();
	public NSExtensionRequestHandling (NSObjectFlag t);
	public NSExtensionRequestHandling (System.IntPtr handle);
	// methods
	public virtual void BeginRequestWithExtensionContext (NSExtensionContext context);
}
```

### New Type Foundation.NSExtensionRequestHandling_Extensions

```
public static class NSExtensionRequestHandling_Extensions {
}
```

### New Type Foundation.NSFileAccessIntent

```
public class NSFileAccessIntent : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
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

### New Type Foundation.NSFilePresenterReacquirer

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

### New Type Foundation.NSFormattingContext

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

### New Type Foundation.NSFormattingUnitStyle

```
[Serializable]
public enum NSFormattingUnitStyle {
	Long = 3,
	Medium = 2,
	Short = 1,
}
```

### New Type Foundation.NSItemProvider

```
public class NSItemProvider : Foundation.NSObject, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSItemProvider ();
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
	public virtual void LoadItem (string typeIdentifier, NSDictionary options, System.Action<NSObject,Foundation.NSError> completionHandler);
	public virtual void LoadPreviewImage (NSDictionary options, System.Action<NSObject,Foundation.NSError> completionHandler);
	public virtual void RegisterItemForTypeIdentifier (string typeIdentifier, NSItemProviderLoadHandler loadHandler);
	public virtual void SetPreviewImageHandler (NSItemProviderLoadHandler handler);
}
```

### New Type Foundation.NSItemProviderCompletionHandler

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

### New Type Foundation.NSItemProviderErrorCode

```
[Serializable]
public enum NSItemProviderErrorCode {
	ItemUnavailable = -1000,
	None = 0,
	UnexpectedValueClass = -1100,
	Unknown = -1,
}
```

### New Type Foundation.NSItemProviderLoadHandler

```
public sealed delegate NSItemProviderLoadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSItemProviderLoadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSItemProviderCompletionHandler completionHandler, ObjCRuntime.Class expectedValueClass, NSDictionary options, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSItemProviderCompletionHandler completionHandler, ObjCRuntime.Class expectedValueClass, NSDictionary options);
}
```

### New Type Foundation.NSLengthFormatter

```
public class NSLengthFormatter : Foundation.NSFormatter, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type Foundation.NSLengthFormatterUnit

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

### New Type Foundation.NSMassFormatter

```
public class NSMassFormatter : Foundation.NSFormatter, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type Foundation.NSMassFormatterUnit

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

### New Type Foundation.NSOperatingSystemVersion

```
public struct NSOperatingSystemVersion {
	// constructors
	public NSOperatingSystemVersion (System.nint major, System.nint minor, System.nint patchVersion);
	// fields
	public System.nint Major;
	public System.nint Minor;
	public System.nint PatchVersion;
	// methods
	public override string ToString ();
}
```

### New Type Foundation.NSQualityOfService

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

### New Type Foundation.NSUrl_PromisedItems

```
public static class NSUrl_PromisedItems {
	// methods
	public static bool CheckPromisedItemIsReachable (NSUrl This, out NSError error);
	public static bool GetPromisedItemResourceValue (NSUrl This, NSObject value, NSString key, out NSError error);
	public static NSDictionary GetPromisedItemResourceValues (NSUrl This, NSString[] keys, out NSError error);
}
```

### New Type Foundation.NSUrlProtocolClient_Extensions

```
public static class NSUrlProtocolClient_Extensions {
}
```

### New Type Foundation.NSUrlQueryItem

```
public class NSUrlQueryItem : Foundation.NSObject, INSCoding, INSCopying, INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual void EncodeTo (NSCoder encoder);
}
```

### New Type Foundation.NSURLRelationship

```
[Serializable]
public enum NSURLRelationship {
	Contains = 0,
	Other = 2,
	Same = 1,
}
```

### New Type Foundation.NSUrlSessionDownloadResponse

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

### New Type Foundation.NSURLSessionTaskPriority

```
public static class NSURLSessionTaskPriority {
	// properties
	public static float Default { get; }
	public static float High { get; }
	public static float Low { get; }
}
```

### New Type Foundation.NSUserActivity

```
public class NSUserActivity : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUserActivity ();
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
	public virtual void GetContinuationStreams (System.Action<NSInputStream,Foundation.NSOutputStream,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<NSUserActivityContinuation> GetContinuationStreamsAsync ();
	public virtual void Invalidate ();
}
```

### New Type Foundation.NSUserActivityContinuation

```
public class NSUserActivityContinuation {
	// constructors
	public NSUserActivityContinuation (NSInputStream arg1, NSOutputStream arg2);
	// properties
	public NSInputStream Arg1 { get; set; }
	public NSOutputStream Arg2 { get; set; }
}
```

### New Type Foundation.NSUserActivityDelegate

```
public class NSUserActivityDelegate : Foundation.NSObject, INSUserActivityDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUserActivityDelegate ();
	public NSUserActivityDelegate (NSObjectFlag t);
	public NSUserActivityDelegate (System.IntPtr handle);
	// methods
	public virtual void UserActivityReceivedData (NSUserActivity userActivity, NSInputStream inputStream, NSOutputStream outputStream);
	public virtual void UserActivityWasContinued (NSUserActivity userActivity);
	public virtual void UserActivityWillSave (NSUserActivity userActivity);
}
```

### New Type Foundation.NSUserActivityDelegate_Extensions

```
public static class NSUserActivityDelegate_Extensions {
	// methods
	public static void UserActivityReceivedData (INSUserActivityDelegate This, NSUserActivity userActivity, NSInputStream inputStream, NSOutputStream outputStream);
	public static void UserActivityWasContinued (INSUserActivityDelegate This, NSUserActivity userActivity);
	public static void UserActivityWillSave (INSUserActivityDelegate This, NSUserActivity userActivity);
}
```

### New Type Foundation.NSUserActivityType

```
public static class NSUserActivityType {
	// properties
	public static NSString BrowsingWeb { get; }
}
```



## Namespace GameKit



### Type Changed: GameKit.GKAchievement

Added constructor:

```
public GKAchievement (string identifier, GKPlayer player);
```

Added interface:

```
Foundation.INSSecureCoding
```

Added property:

```
public virtual GKPlayer Player { get; }
```

Added methods:

```
public virtual AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
	public virtual void IssueChallengeToPlayers (string[] playerIDs, string message);
	public static void ReportAchievements (GKAchievement[] achievements, GKChallenge[] challenges, System.Action<Foundation.NSError> completionHandler);
	public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements);
	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements, GKChallenge[] challenges);
	public virtual void SelectChallengeablePlayerIDs (string[] playerIDs, System.Action<System.String[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<System.String[]> SelectChallengeablePlayerIDsAsync (string[] playerIDs);
	public virtual void SelectChallengeablePlayers (GKPlayer[] players, System.Action<GKPlayer[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> SelectChallengeablePlayersAsync (GKPlayer[] players);
```

### Type Changed: GameKit.GKAchievementChallenge

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: GameKit.GKAchievementDescription

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: GameKit.GKChallenge

Added interface:

```
Foundation.INSSecureCoding
```

Added properties:

```
public virtual GKPlayer IssuingPlayer { get; }
	public virtual GKPlayer ReceivingPlayer { get; }
```

### Type Changed: GameKit.GKFriendRequestComposeViewController

Added method:

```
public virtual void AddRecipientPlayers (GKPlayer[] players);
```

### Type Changed: GameKit.GKInvite

Added properties:

```
public virtual uint PlayerAttributes { get; }
	public virtual System.nint PlayerGroup { get; }
	public virtual GKPlayer Sender { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: GameKit.GKLeaderboard

Added constructor:

```
public GKLeaderboard (GKPlayer[] players);
```

### Type Changed: GameKit.GKLocalPlayer

Added property:

```
public virtual System.Action<AppKit.NSViewController,Foundation.NSError> AuthenticateHandler { get; set; }
```

Added methods:

```
public virtual void DeleteSavedGamesWithName (string name, System.Action<Foundation.NSError> handler);
	public virtual void FetchSavedGamesWithCompletionHandler (System.Action<Foundation.NSArray,Foundation.NSError> handler);
	public virtual void GenerateIdentityVerificationSignature (GKIdentityVerificationSignatureHandler completionHandler);
	public virtual void LoadDefaultLeaderboardCategoryID (System.Action<System.String,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardCategoryIDAsync ();
	public virtual void LoadDefaultLeaderboardIdentifier (System.Action<System.String,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<string> LoadDefaultLeaderboardIdentifierAsync ();
	public virtual void LoadFriendPlayers (System.Action<GKPlayer[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> LoadFriendPlayersAsync ();
	public virtual void RegisterListener (GKLocalPlayerListener listener);
	public virtual void ResolveConflictingSavedGames (Foundation.NSObject[] conflictingSavedGames, Foundation.NSData data, System.Action<Foundation.NSArray,Foundation.NSError> handler);
	public virtual void SaveGameData (Foundation.NSData data, string name, System.Action<GKSavedGame,Foundation.NSError> handler);
	public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action<Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
	public virtual void SetDefaultLeaderboardIdentifier (string leaderboardIdentifier, System.Action<Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardIdentifierAsync (string leaderboardIdentifier);
	public virtual void UnregisterAllListeners ();
	public virtual void UnregisterListener (GKLocalPlayerListener listener);
```

### Type Changed: GameKit.GKMatch

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
	public virtual bool SendData (Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, out Foundation.NSError error);
```

### Type Changed: GameKit.GKMatchDelegate

Added methods:

```
public virtual void ChangedConnectionState (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public virtual void ReceivedDataFromRemotePlayer (GKMatch match, Foundation.NSData data, GKPlayer player);
	public virtual bool ShouldReinviteDisconnectedPlayer (GKMatch match, GKPlayer player);
```

### Type Changed: GameKit.GKMatchDelegate_Extensions

Added methods:

```
public static void ChangedConnectionState (IGKMatchDelegate This, GKMatch match, GKPlayer player, GKPlayerConnectionState state);
	public static void ReceivedDataFromRemotePlayer (IGKMatchDelegate This, GKMatch match, Foundation.NSData data, GKPlayer player);
	public static bool ShouldReinviteDisconnectedPlayer (IGKMatchDelegate This, GKMatch match, GKPlayer player);
```

### Type Changed: GameKit.GKMatchmaker

Added methods:

```
public virtual void CancelPendingInvite (GKPlayer player);
	public virtual void FindPlayersForHostedRequest (GKMatchRequest request, System.Action<GKPlayer[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<GKPlayer[]> FindPlayersForHostedRequestAsync (GKMatchRequest request);
	public virtual void StartBrowsingForNearbyPlayersWithHandler (System.Action<GKPlayer,System.Boolean> reachableHandler);
```

### Type Changed: GameKit.GKMatchmakerViewController

Added events:

```
public event System.EventHandler<GKMatchmakingPlayersEventArgs> DidFindHostedPlayers;
	public event System.EventHandler<GKMatchmakingPlayerEventArgs> HostedPlayerDidAccept;
```

Added method:

```
public virtual void SetHostedPlayerDidConnect (GKPlayer playerID, bool connected);
```

### Type Changed: GameKit.GKMatchmakerViewControllerDelegate

Added methods:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
	public virtual void HostedPlayerDidAccept (GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: GameKit.GKMatchmakerViewControllerDelegate_Extensions

Added method:

```
public static void HostedPlayerDidAccept (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, GKPlayer playerID);
```

### Type Changed: GameKit.GKMatchRequest

Added properties:

```
public virtual System.Action<GKPlayer,GameKit.GKInviteRecipientResponse> RecipientResponseHandler { get; set; }
	public virtual GKPlayer[] Recipients { get; set; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: GameKit.GKScore

Added constructor:

```
public GKScore (string identifier, GKPlayer player);
```

Added interface:

```
Foundation.INSSecureCoding
```

Removed property:

```
public virtual string Player { get; }
```

Added property:

```
public virtual GKPlayer Player { get; }
```

Added method:

```
public virtual AppKit.NSViewController ChallengeComposeController (string message, GKPlayer[] players, GKChallengeComposeHandler completionHandler);
```

### Type Changed: GameKit.GKScoreChallenge

Added interface:

```
Foundation.INSSecureCoding
```

### Type Changed: GameKit.GKTurnBasedExchange

Added constructors:

```
public GKTurnBasedExchange (Foundation.NSObjectFlag t);
	public GKTurnBasedExchange (System.IntPtr handle);
```

Added interfaces:

```
ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSDate CompletionDate { get; }
	public virtual Foundation.NSData Data { get; }
	public virtual string ExchangeID { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant[] Recipients { get; }
	public virtual GKTurnBasedExchangeReply[] Replies { get; }
	public virtual Foundation.NSDate SendDate { get; }
	public virtual GKTurnBasedParticipant Sender { get; }
	public virtual GKTurnBasedExchangeStatus Status { get; }
	public virtual Foundation.NSDate TimeoutDate { get; }
	public static double TimeoutDefault { get; }
	public static double TimeoutNone { get; }
```

Added methods:

```
public virtual void Cancel (string localizableMessage, Foundation.NSObject[] arguments, System.Action<Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task CancelAsync (string localizableMessage, Foundation.NSObject[] arguments);
	protected override void Dispose (bool disposing);
	public virtual void Reply (string localizableMessage, Foundation.NSObject[] arguments, Foundation.NSData data, System.Action<Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task ReplyAsync (string localizableMessage, Foundation.NSObject[] arguments, Foundation.NSData data);
```

### Type Changed: GameKit.GKTurnBasedExchangeReply

Added constructors:

```
public GKTurnBasedExchangeReply (Foundation.NSObjectFlag t);
	public GKTurnBasedExchangeReply (System.IntPtr handle);
```

Added interfaces:

```
ObjCRuntime.INativeObject
	System.IDisposable
```

Added properties:

```
public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSData Data { get; }
	public virtual string Message { get; }
	public virtual GKTurnBasedParticipant Recipient { get; }
	public virtual Foundation.NSDate ReplyDate { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: GameKit.GKTurnBasedParticipant

Added property:

```
public virtual GKPlayer Player { get; }
```

### Type Changed: GameKit.GKVoiceChat

Added properties:

```
public virtual GKPlayer[] Players { get; }
	public virtual System.Action<GKPlayer,GameKit.GKVoiceChatPlayerState> PlayerVoiceChatStateDidChangeHandler { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void SetMuteStatus (GKPlayer player, bool isMuted);
```

### Type Changed: GameKit.IGKMatchmakerViewControllerDelegate

Added method:

```
public virtual void DidFindHostedPlayers (GKMatchmakerViewController viewController, GKPlayer[] playerIDs);
```

### New Type GameKit.GKChallengeComposeHandler

```
public sealed delegate GKChallengeComposeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKChallengeComposeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs);
}
```

### New Type GameKit.GKChallengeListener

```
public class GKChallengeListener : Foundation.NSObject, IGKChallengeListener, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKChallengeListener ();
	public GKChallengeListener (Foundation.NSObjectFlag t);
	public GKChallengeListener (System.IntPtr handle);
	// methods
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
```

### New Type GameKit.GKChallengeListener_Extensions

```
public static class GKChallengeListener_Extensions {
	// methods
	public static void DidCompleteChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void DidReceiveChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
	public static void IssuedChallengeWasCompleted (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void WantsToPlayChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
}
```

### New Type GameKit.GKGameCenterControllerDelegate

```
public class GKGameCenterControllerDelegate : Foundation.NSObject, IGKGameCenterControllerDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKGameCenterControllerDelegate ();
	public GKGameCenterControllerDelegate (Foundation.NSObjectFlag t);
	public GKGameCenterControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void Finished (GKGameCenterViewController controller);
}
```

### New Type GameKit.GKGameCenterControllerDelegate_Extensions

```
public static class GKGameCenterControllerDelegate_Extensions {
	// methods
	public static void Finished (IGKGameCenterControllerDelegate This, GKGameCenterViewController controller);
}
```

### New Type GameKit.GKGameCenterViewController

```
public class GKGameCenterViewController : AppKit.NSViewController, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKGameCenterViewController ();
	public GKGameCenterViewController (Foundation.NSCoder coder);
	public GKGameCenterViewController (Foundation.NSObjectFlag t);
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
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler Finished;
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type GameKit.GKIdentityVerificationSignatureHandler

```
public sealed delegate GKIdentityVerificationSignatureHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GKIdentityVerificationSignatureHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSUrl publicKeyUrl, Foundation.NSData signature, Foundation.NSData salt, ulong timestamp, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSUrl publicKeyUrl, Foundation.NSData signature, Foundation.NSData salt, ulong timestamp, Foundation.NSError error);
}
```

### New Type GameKit.GKInviteEventListener

```
public class GKInviteEventListener : Foundation.NSObject, IGKInviteEventListener, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKInviteEventListener ();
	public GKInviteEventListener (Foundation.NSObjectFlag t);
	public GKInviteEventListener (System.IntPtr handle);
	// methods
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidRequestMatch (GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type GameKit.GKInviteEventListener_Extensions

```
public static class GKInviteEventListener_Extensions {
	// methods
	public static void DidAcceptInvite (IGKInviteEventListener This, GKPlayer player, GKInvite invite);
	public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, GKPlayer[] recipientPlayers);
}
```

### New Type GameKit.GKInviteRecipientResponse

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

### New Type GameKit.GKLocalPlayerListener

```
public class GKLocalPlayerListener : Foundation.NSObject, IGKLocalPlayerListener, IGKChallengeListener, IGKInviteEventListener, IGKTurnBasedEventListener, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKLocalPlayerListener ();
	public GKLocalPlayerListener (Foundation.NSObjectFlag t);
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

### New Type GameKit.GKLocalPlayerListener_Extensions

```
public static class GKLocalPlayerListener_Extensions {
}
```

### New Type GameKit.GKMatchConnectionChangedEventArgs

```
public class GKMatchConnectionChangedEventArgs : System.EventArgs {
	// constructors
	public GKMatchConnectionChangedEventArgs (GKPlayer player, GKPlayerConnectionState state);
	// properties
	public GKPlayer Player { get; set; }
	public GKPlayerConnectionState State { get; set; }
}
```

### New Type GameKit.GKMatchmakingPlayerEventArgs

```
public class GKMatchmakingPlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayerEventArgs (GKPlayer playerID);
	// properties
	public GKPlayer PlayerID { get; set; }
}
```

### New Type GameKit.GKMatchmakingPlayersEventArgs

```
public class GKMatchmakingPlayersEventArgs : System.EventArgs {
	// constructors
	public GKMatchmakingPlayersEventArgs (GKPlayer[] playerIDs);
	// properties
	public GKPlayer[] PlayerIDs { get; set; }
}
```

### New Type GameKit.GKMatchReceivedDataFromRemotePlayerEventArgs

```
public class GKMatchReceivedDataFromRemotePlayerEventArgs : System.EventArgs {
	// constructors
	public GKMatchReceivedDataFromRemotePlayerEventArgs (Foundation.NSData data, GKPlayer player);
	// properties
	public Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
}
```

### New Type GameKit.GKMatchReinvitationForDisconnectedPlayer

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

### New Type GameKit.GKSavedGame

```
public class GKSavedGame : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGame ();
	public GKSavedGame (Foundation.NSObjectFlag t);
	public GKSavedGame (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string DeviceName { get; }
	public virtual Foundation.NSDate ModificationDate { get; }
	public virtual string Name { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void LoadDataWithCompletionHandler (System.Action<Foundation.NSData,Foundation.NSError> handler);
}
```

### New Type GameKit.GKSavedGameListener

```
public class GKSavedGameListener : Foundation.NSObject, IGKSavedGameListener, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKSavedGameListener ();
	public GKSavedGameListener (Foundation.NSObjectFlag t);
	public GKSavedGameListener (System.IntPtr handle);
	// methods
	public virtual void DidModifySavedGame (GKPlayer player, GKSavedGame savedGame);
	public virtual void HasConflictingSavedGames (GKPlayer player, Foundation.NSObject[] savedGames);
}
```

### New Type GameKit.GKSavedGameListener_Extensions

```
public static class GKSavedGameListener_Extensions {
	// methods
	public static void DidModifySavedGame (IGKSavedGameListener This, GKPlayer player, GKSavedGame savedGame);
	public static void HasConflictingSavedGames (IGKSavedGameListener This, GKPlayer player, Foundation.NSObject[] savedGames);
}
```

### New Type GameKit.GKTurnBasedEventListener

```
public class GKTurnBasedEventListener : Foundation.NSObject, IGKTurnBasedEventListener, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKTurnBasedEventListener ();
	public GKTurnBasedEventListener (Foundation.NSObjectFlag t);
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

### New Type GameKit.GKTurnBasedEventListener_Extensions

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

### New Type GameKit.IGKChallengeListener

```
public interface IGKChallengeListener : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type GameKit.IGKGameCenterControllerDelegate

```
public interface IGKGameCenterControllerDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type GameKit.IGKInviteEventListener

```
public interface IGKInviteEventListener : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type GameKit.IGKLocalPlayerListener

```
public interface IGKLocalPlayerListener : ObjCRuntime.INativeObject, System.IDisposable, IGKChallengeListener, IGKInviteEventListener, IGKTurnBasedEventListener {
}
```

### New Type GameKit.IGKSavedGameListener

```
public interface IGKSavedGameListener : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type GameKit.IGKTurnBasedEventListener

```
public interface IGKTurnBasedEventListener : ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace ImageIO



### Type Changed: ImageIO.CGImageDestinationOptions

Added properties:

```
public bool EmbedThumbnail { get; set; }
	public int? ImageMaxPixelSize { get; set; }
	public bool ShouldExcludeGPS { get; set; }
```

### Type Changed: ImageIO.CGImageProperties

Added properties:

```
public static Foundation.NSString GPSHPositioningError { get; }
	public static Foundation.NSString PNGDelayTime { get; }
	public static Foundation.NSString PNGLoopCount { get; }
	public static Foundation.NSString PNGUnclampedDelayTime { get; }
```

### New Type ImageIO.CGImagePropertyOrientation

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

## Namespace JavaScriptCore

### Type Changed: JavaScriptCore.JSContext

Added properties:

```
public static JSValue CurrentCallee { get; }
	public JSValue Item { get; set; }
	public virtual System.IntPtr JSGlobalContextRefPtr { get; }
	public virtual string Name { get; set; }
```

Added methods:

```
public virtual JSValue EvaluateScript (string script, Foundation.NSUrl sourceUrl);
	public static JSContext FromJSGlobalContextRef (System.IntPtr nativeJsGlobalContextRef);
```

### Type Changed: JavaScriptCore.JSManagedValue

Added method:

```
public static JSManagedValue Get (JSValue value, Foundation.NSObject owner);
```

### Type Changed: JavaScriptCore.JSValue

Added properties:

```
public JSValue Item { get; set; }
	public JSValue Item { get; set; }
	public virtual System.IntPtr JSValueRefPtr { get; }
```

Added methods:

```
public static JSValue From (string value, JSContext context);
	public static JSValue FromJSJSValueRef (System.IntPtr nativeJsValueRefvalue, JSContext context);
	public override string ToString ();
```

## Namespace MobileCoreServices

### Type Changed: MobileCoreServices.UTType

Removed fields:

```
public static Foundation.NSString AliasFile;
	public static Foundation.NSString AliasRecord;
	public static Foundation.NSString AppleICNS;
	public static Foundation.NSString AppleProtectedMPEG4Audio;
	public static Foundation.NSString Application;
	public static Foundation.NSString ApplicationBundle;
	public static Foundation.NSString ApplicationFile;
	public static Foundation.NSString Archive;
	public static Foundation.NSString Audio;
	public static Foundation.NSString AudiovisualContent;
	public static Foundation.NSString BMP;
	public static Foundation.NSString Bundle;
	public static Foundation.NSString CHeader;
	public static Foundation.NSString CompositeContent;
	public static Foundation.NSString ConformsToKey;
	public static Foundation.NSString Contact;
	public static Foundation.NSString Content;
	public static Foundation.NSString CPlusPlusHeader;
	public static Foundation.NSString CPlusPlusSource;
	public static Foundation.NSString CSource;
	public static Foundation.NSString Data;
	public static Foundation.NSString DescriptionKey;
	public static Foundation.NSString Directory;
	public static Foundation.NSString DiskImage;
	public static Foundation.NSString ExportedTypeDeclarationsKey;
	public static Foundation.NSString FileURL;
	public static Foundation.NSString FlatRTFD;
	public static Foundation.NSString Folder;
	public static Foundation.NSString Framework;
	public static Foundation.NSString GIF;
	public static Foundation.NSString HTML;
	public static Foundation.NSString ICO;
	public static Foundation.NSString IconFileKey;
	public static Foundation.NSString IdentifierKey;
	public static Foundation.NSString Image;
	public static Foundation.NSString ImportedTypeDeclarationsKey;
	public static Foundation.NSString InkText;
	public static Foundation.NSString Item;
	public static Foundation.NSString JavaSource;
	public static Foundation.NSString JPEG;
	public static Foundation.NSString JPEG2000;
	public static Foundation.NSString Message;
	public static Foundation.NSString MountPoint;
	public static Foundation.NSString Movie;
	public static Foundation.NSString MP3;
	public static Foundation.NSString MPEG;
	public static Foundation.NSString MPEG4;
	public static Foundation.NSString MPEG4Audio;
	public static Foundation.NSString ObjectiveCPlusPlusSource;
	public static Foundation.NSString ObjectiveCSource;
	public static Foundation.NSString Package;
	public static Foundation.NSString PDF;
	public static Foundation.NSString PICT;
	public static Foundation.NSString PlainText;
	public static Foundation.NSString PNG;
	public static Foundation.NSString QuickTimeImage;
	public static Foundation.NSString QuickTimeMovie;
	public static Foundation.NSString ReferenceURLKey;
	public static Foundation.NSString Resolvable;
	public static Foundation.NSString RTF;
	public static Foundation.NSString RTFD;
	public static Foundation.NSString SourceCode;
	public static Foundation.NSString SymLink;
	public static Foundation.NSString TagClassFilenameExtension;
	public static Foundation.NSString TagClassMIMEType;
	public static Foundation.NSString TagClassNSPboardType;
	public static Foundation.NSString TagClassOSType;
	public static Foundation.NSString TagSpecificationKey;
	public static Foundation.NSString Text;
	public static Foundation.NSString TIFF;
	public static Foundation.NSString TXNTextAndMultimediaData;
	public static Foundation.NSString URL;
	public static Foundation.NSString UTF16ExternalPlainText;
	public static Foundation.NSString UTF16PlainText;
	public static Foundation.NSString UTF8PlainText;
	public static Foundation.NSString VCard;
	public static Foundation.NSString VersionKey;
	public static Foundation.NSString Video;
	public static Foundation.NSString Volume;
	public static Foundation.NSString WebArchive;
	public static Foundation.NSString XML;
```

Added properties:

```
public static Foundation.NSString AliasFile { get; }
	public static Foundation.NSString AliasRecord { get; }
	public static Foundation.NSString AppleICNS { get; }
	public static Foundation.NSString AppleProtectedMPEG4Audio { get; }
	public static Foundation.NSString AppleProtectedMPEG4Video { get; }
	public static Foundation.NSString AppleScript { get; }
	public static Foundation.NSString Application { get; }
	public static Foundation.NSString ApplicationBundle { get; }
	public static Foundation.NSString ApplicationFile { get; }
	public static Foundation.NSString Archive { get; }
	public static Foundation.NSString AssemblyLanguageSource { get; }
	public static Foundation.NSString Audio { get; }
	public static Foundation.NSString AudioInterchangeFileFormat { get; }
	public static Foundation.NSString AudiovisualContent { get; }
	public static Foundation.NSString AVIMovie { get; }
	public static Foundation.NSString BinaryPropertyList { get; }
	public static Foundation.NSString BMP { get; }
	public static Foundation.NSString Bookmark { get; }
	public static Foundation.NSString Bundle { get; }
	public static Foundation.NSString Bzip2Archive { get; }
	public static Foundation.NSString CalendarEvent { get; }
	public static Foundation.NSString CHeader { get; }
	public static Foundation.NSString CommaSeparatedText { get; }
	public static Foundation.NSString CompositeContent { get; }
	public static Foundation.NSString ConformsToKey { get; }
	public static Foundation.NSString Contact { get; }
	public static Foundation.NSString Content { get; }
	public static Foundation.NSString CPlusPlusHeader { get; }
	public static Foundation.NSString CPlusPlusSource { get; }
	public static Foundation.NSString CSource { get; }
	public static Foundation.NSString Data { get; }
	public static Foundation.NSString Database { get; }
	public static Foundation.NSString DelimitedText { get; }
	public static Foundation.NSString DescriptionKey { get; }
	public static Foundation.NSString Directory { get; }
	public static Foundation.NSString DiskImage { get; }
	public static Foundation.NSString ElectronicPublication { get; }
	public static Foundation.NSString EmailMessage { get; }
	public static Foundation.NSString Executable { get; }
	public static Foundation.NSString ExportedTypeDeclarationsKey { get; }
	public static Foundation.NSString FileURL { get; }
	public static Foundation.NSString FlatRTFD { get; }
	public static Foundation.NSString Folder { get; }
	public static Foundation.NSString Font { get; }
	public static Foundation.NSString Framework { get; }
	public static Foundation.NSString GIF { get; }
	public static Foundation.NSString GNUZipArchive { get; }
	public static Foundation.NSString HTML { get; }
	public static Foundation.NSString ICO { get; }
	public static Foundation.NSString IconFileKey { get; }
	public static Foundation.NSString IdentifierKey { get; }
	public static Foundation.NSString Image { get; }
	public static Foundation.NSString ImportedTypeDeclarationsKey { get; }
	public static Foundation.NSString InkText { get; }
	public static Foundation.NSString InternetLocation { get; }
	public static Foundation.NSString Item { get; }
	public static Foundation.NSString JavaArchive { get; }
	public static Foundation.NSString JavaClass { get; }
	public static Foundation.NSString JavaScript { get; }
	public static Foundation.NSString JavaSource { get; }
	public static Foundation.NSString JPEG { get; }
	public static Foundation.NSString JPEG2000 { get; }
	public static Foundation.NSString JSON { get; }
	public static Foundation.NSString Log { get; }
	public static Foundation.NSString M3UPlaylist { get; }
	public static Foundation.NSString Message { get; }
	public static Foundation.NSString MIDIAudio { get; }
	public static Foundation.NSString MountPoint { get; }
	public static Foundation.NSString Movie { get; }
	public static Foundation.NSString MP3 { get; }
	public static Foundation.NSString MPEG { get; }
	public static Foundation.NSString MPEG2TransportStream { get; }
	public static Foundation.NSString MPEG2Video { get; }
	public static Foundation.NSString MPEG4 { get; }
	public static Foundation.NSString MPEG4Audio { get; }
	public static Foundation.NSString ObjectiveCPlusPlusSource { get; }
	public static Foundation.NSString ObjectiveCSource { get; }
	public static Foundation.NSString OSAScript { get; }
	public static Foundation.NSString OSAScriptBundle { get; }
	public static Foundation.NSString Package { get; }
	public static Foundation.NSString PDF { get; }
	public static Foundation.NSString PerlScript { get; }
	public static Foundation.NSString PHPScript { get; }
	public static Foundation.NSString PICT { get; }
	public static Foundation.NSString PKCS12 { get; }
	public static Foundation.NSString PlainText { get; }
	public static Foundation.NSString Playlist { get; }
	public static Foundation.NSString PluginBundle { get; }
	public static Foundation.NSString PNG { get; }
	public static Foundation.NSString Presentation { get; }
	public static Foundation.NSString PropertyList { get; }
	public static Foundation.NSString PythonScript { get; }
	public static Foundation.NSString QuickLookGenerator { get; }
	public static Foundation.NSString QuickTimeImage { get; }
	public static Foundation.NSString QuickTimeMovie { get; }
	public static Foundation.NSString RawImage { get; }
	public static Foundation.NSString ReferenceURLKey { get; }
	public static Foundation.NSString Resolvable { get; }
	public static Foundation.NSString RTF { get; }
	public static Foundation.NSString RTFD { get; }
	public static Foundation.NSString RubyScript { get; }
	public static Foundation.NSString ScalableVectorGraphics { get; }
	public static Foundation.NSString Script { get; }
	public static Foundation.NSString ShellScript { get; }
	public static Foundation.NSString SourceCode { get; }
	public static Foundation.NSString SpotlightImporter { get; }
	public static Foundation.NSString Spreadsheet { get; }
	public static Foundation.NSString SymLink { get; }
	public static Foundation.NSString SystemPreferencesPane { get; }
	public static Foundation.NSString TabSeparatedText { get; }
	public static Foundation.NSString TagClassFilenameExtension { get; }
	public static Foundation.NSString TagClassMIMEType { get; }
	public static Foundation.NSString TagClassNSPboardType { get; }
	public static Foundation.NSString TagClassOSType { get; }
	public static Foundation.NSString TagSpecificationKey { get; }
	public static Foundation.NSString Text { get; }
	public static Foundation.NSString ThreeDContent { get; }
	public static Foundation.NSString TIFF { get; }
	public static Foundation.NSString ToDoItem { get; }
	public static Foundation.NSString TXNTextAndMultimediaData { get; }
	public static Foundation.NSString UnixExecutable { get; }
	public static Foundation.NSString URL { get; }
	public static Foundation.NSString URLBookmarkData { get; }
	public static Foundation.NSString UTF16ExternalPlainText { get; }
	public static Foundation.NSString UTF16PlainText { get; }
	public static Foundation.NSString UTF8PlainText { get; }
	public static Foundation.NSString UTF8TabSeparatedText { get; }
	public static Foundation.NSString VCard { get; }
	public static Foundation.NSString VersionKey { get; }
	public static Foundation.NSString Video { get; }
	public static Foundation.NSString Volume { get; }
	public static Foundation.NSString WaveformAudio { get; }
	public static Foundation.NSString WebArchive { get; }
	public static Foundation.NSString WindowsExecutable { get; }
	public static Foundation.NSString X509Certificate { get; }
	public static Foundation.NSString XML { get; }
	public static Foundation.NSString XMLPropertyList { get; }
	public static Foundation.NSString XPCService { get; }
	public static Foundation.NSString ZipArchive { get; }
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

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Class

Removed method:

```
public static System.IntPtr GetHandleIntrinsic (string name);
```

Added method:

```
public static bool IsCustomType (System.Type type);
```

### Type Changed: ObjCRuntime.Constants

Added fields:

```
public static const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
```

### Type Changed: ObjCRuntime.PlatformHelper

Removed method:

```
public static bool Is64BitOnlyOnCurrentPlatform (Platform platform);
```

### Removed Type ObjCRuntime.RuntimeException ### New Type ObjCRuntime.MethodDescription

```
public struct MethodDescription {
	// constructors
	public MethodDescription (System.Reflection.MethodBase method, ArgumentSemantic semantic);
	// fields
	public System.Reflection.MethodBase method;
	public ArgumentSemantic semantic;
}
```



## Namespace OpenGL

### Type Changed: OpenGL.MathHelper

Added fields:

```
public static double DTOR;
	public static float DTORF;
```

### New Type OpenGL.Matrix3d

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

## Namespace SceneKit

### Type Changed: SceneKit.SCNBox

Added constructor:

```
public SCNBox (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNCamera

Added constructor:

```
public SCNCamera (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
```

Removed property:

```
public virtual CoreAnimation.CATransform3D ProjectionTransform { get; set; }
```

Added properties:

```
public virtual System.nfloat Aperture { get; set; }
	public virtual bool AutomaticallyAdjustsZRange { get; set; }
	public virtual System.nuint CategoryBitMask { get; set; }
	public virtual System.nfloat FocalBlurRadius { get; set; }
	public virtual System.nfloat FocalDistance { get; set; }
	public virtual System.nfloat FocalSize { get; set; }
	public virtual double OrthographicScale { get; set; }
	public virtual SCNMatrix4 ProjectionTransform { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNCapsule

Added constructor:

```
public SCNCapsule (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNCone

Added constructor:

```
public SCNCone (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNConstraint

Added constructor:

```
public SCNConstraint (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
```

Added property:

```
public virtual System.nfloat InfluenceFactor { get; set; }
```

Added methods:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNCylinder

Added constructor:

```
public SCNCylinder (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNFloor

Added constructor:

```
public SCNFloor (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added property:

```
public virtual System.nfloat ReflectionResolutionScaleFactor { get; set; }
```

### Type Changed: SceneKit.SCNGeometry

Added constructor:

```
public SCNGeometry (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
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
	public virtual System.nuint SubdivisionLevel { get; set; }
	public virtual Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public static SCNGeometry Create ();
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNGeometryElement

Added constructor:

```
public SCNGeometryElement (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
```

Added method:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
```

### Type Changed: SceneKit.SCNGeometrySource

Added constructor:

```
public SCNGeometrySource (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
```

Added method:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
```

### Type Changed: SceneKit.SCNGeometrySourceSemantic

Added properties:

```
public static Foundation.NSString EdgeCrease { get; }
	public static Foundation.NSString VertexCrease { get; }
```

### Type Changed: SceneKit.SCNHitTest

Removed property:

```
public static Foundation.NSString IgnoreHiddenNodes { get; }
```

Added property:

```
public static Foundation.NSString IgnoreHiddenNodesKey { get; }
```

### Type Changed: SceneKit.SCNHitTestResult

Removed property:

```
public virtual CoreAnimation.CATransform3D ModelTransform { get; }
```

Added property:

```
public virtual SCNMatrix4 ModelTransform { get; }
```

### Type Changed: SceneKit.SCNLayer

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
```

Added properties:

```
public virtual SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: SceneKit.SCNLevelOfDetail

Added constructor:

```
public SCNLevelOfDetail (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
```

Added method:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
```

### Type Changed: SceneKit.SCNLight

Added constructor:

```
public SCNLight (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNTechniqueSupport
```

Removed property:

```
public virtual string LightType { get; set; }
```

Added properties:

```
public virtual System.nfloat AttenuationEndDistance { get; set; }
	public virtual System.nfloat AttenuationFalloffExponent { get; set; }
	public virtual System.nfloat AttenuationStartDistance { get; set; }
	public virtual System.nuint CategoryBitMask { get; set; }
	public virtual SCNMaterialProperty Gobo { get; }
	public virtual Foundation.NSString LightType { get; set; }
	public virtual System.nfloat OrthographicScale { get; set; }
	public virtual System.nfloat ShadowBias { get; set; }
	public virtual CoreGraphics.CGSize ShadowMapSize { get; set; }
	public virtual SCNShadowMode ShadowMode { get; set; }
	public virtual System.nuint ShadowSampleCount { get; set; }
	public virtual System.nfloat SpotInnerAngle { get; set; }
	public virtual System.nfloat SpotOuterAngle { get; set; }
	public virtual SCNTechnique Technique { get; set; }
	public virtual System.nfloat ZFar { get; set; }
	public virtual System.nfloat ZNear { get; set; }
```

Added methods:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNLookAtConstraint

Added constructor:

```
public SCNLookAtConstraint (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
```

### Type Changed: SceneKit.SCNMaterial

Added constructor:

```
public SCNMaterial (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNShadable
```

Added properties:

```
public virtual System.nfloat FresnelExponent { get; set; }
	public virtual bool ReadsFromDepthBuffer { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual Foundation.NSDictionary WeakShaderModifiers { get; set; }
```

Added methods:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNMaterialProperty

Added constructor:

```
public SCNMaterialProperty (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
```

Removed property:

```
public virtual CoreAnimation.CATransform3D ContentsTransform { get; set; }
```

Added properties:

```
public AppKit.NSColor ContentColor { get; set; }
	public AppKit.NSImage ContentImage { get; set; }
	public AppKit.NSImage[] ContentImageCube { get; set; }
	public CoreAnimation.CALayer ContentLayer { get; set; }
	public Foundation.NSString ContentPath { get; set; }
	public SpriteKit.SKScene ContentScene { get; set; }
	public virtual SCNMatrix4 ContentsTransform { get; set; }
	public SpriteKit.SKTexture ContentTexture { get; set; }
	public Foundation.NSUrl ContentUrl { get; set; }
	public virtual System.nfloat Intensity { get; set; }
	public virtual System.nfloat MaxAnisotropy { get; set; }
```

Added methods:

```
public static SCNMaterialProperty Create (Foundation.NSObject contents);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNMorpher

Added constructor:

```
public SCNMorpher (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
```

Added methods:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.SCNNode

Added constructor:

```
public SCNNode (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNActionable
	ISCNAnimatable
	ISCNBoundingVolume
```

Removed properties:

```
public virtual CoreAnimation.CATransform3D Pivot { get; set; }
	public virtual CoreAnimation.CATransform3D Transform { get; set; }
	public virtual CoreAnimation.CATransform3D WorldTransform { get; }
```

Added properties:

```
public virtual bool CastsShadow { get; set; }
	public virtual System.nuint CategoryBitMask { get; set; }
	public virtual SCNConstraint[] Constraints { get; set; }
	public virtual SCNVector3 EulerAngles { get; set; }
	public virtual CoreImage.CIFilter[] Filters { get; set; }
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
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void EnumerateChildNodes (SCNNodePredicate predicate);
	public virtual SCNNode[] FindNodes (SCNNodePredicate predicate);
	public virtual SCNNode FlattenedClone ();
	public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public virtual SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (SCNVector3 pointA, SCNVector3 pointB, SCNHitTestOptions options);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual void ResumeAnimation (Foundation.NSString key);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
	public virtual void RunAction (SCNAction action);
```

### Type Changed: SceneKit.SCNNodeRendererDelegate

Added interface:

```
ISCNNodeRendererDelegate
```

### Type Changed: SceneKit.SCNPlane

Added constructor:

```
public SCNPlane (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Added properties:

```
public virtual System.nfloat CornerRadius { get; set; }
	public virtual System.nint CornerSegmentCount { get; set; }
```

### Type Changed: SceneKit.SCNProgram

Added constructor:

```
public SCNProgram (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
```

Added properties:

```
public static Foundation.NSString MappingChannelKey { get; }
	public virtual bool Opaque { get; set; }
```

Added methods:

```
public virtual void EncodeTo (Foundation.NSCoder encoder);
	public void SetSemantic (Foundation.NSString geometrySourceSemantic, string symbol, SCNProgramSemanticOptions options);
```

### Type Changed: SceneKit.SCNProgramDelegate

Added interface:

```
ISCNProgramDelegate
```

### Type Changed: SceneKit.SCNPyramid

Added constructor:

```
public SCNPyramid (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNRenderer

Added interfaces:

```
ISCNSceneRenderer
	ISCNTechniqueSupport
```

Added properties:

```
public virtual double NextFrameTimeInSeconds { get; }
	public virtual SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual SCNTechnique Technique { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual void Render (double timeInSeconds);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: SceneKit.SCNScene

Added constructor:

```
public SCNScene (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
```

Added properties:

```
public virtual SCNMaterialProperty Background { get; }
	public static Foundation.NSString EndTimeAttributeKey { get; }
	public virtual Foundation.NSObject FogColor { get; set; }
	public virtual System.nfloat FogDensityExponent { get; set; }
	public virtual System.nfloat FogEndDistance { get; set; }
	public virtual System.nfloat FogStartDistance { get; set; }
	public static Foundation.NSString FrameRateAttributeKey { get; }
	public virtual SCNParticleSystem[] ParticleSystems { get; }
	public virtual bool Paused { get; set; }
	public virtual SCNPhysicsWorld PhysicsWorld { get; }
	public static Foundation.NSString StartTimeAttributeKey { get; }
	public static Foundation.NSString UpAxisAttributeKey { get; }
```

Added methods:

```
public virtual void AddParticleSystem (SCNParticleSystem system, SCNMatrix4 transform);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SCNScene FromFile (string name, string directory, SCNSceneLoadingOptions options);
	public static SCNScene FromFile (string name, string directory, Foundation.NSDictionary options);
	public static SCNScene FromFile (string name);
	public static SCNScene FromUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, out Foundation.NSError error);
	public virtual void RemoveAllParticleSystems ();
	public virtual void RemoveParticleSystem (SCNParticleSystem system);
	public virtual bool WriteToUrl (Foundation.NSUrl url, Foundation.NSDictionary options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
	public bool WriteToUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options, SCNSceneExportDelegate handler, SCNSceneExportProgressHandler exportProgressHandler);
```

### Type Changed: SceneKit.SCNSceneRendererDelegate

Added interface:

```
ISCNSceneRendererDelegate
```

Removed methods:

```
public virtual void DidRenderScene (Foundation.NSObject renderer, SCNScene scene, double time);
	public virtual void WillRenderScene (Foundation.NSObject renderer, SCNScene scene, double time);
```

Added methods:

```
public virtual void DidApplyAnimations (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

### Type Changed: SceneKit.SCNSceneSource

Added constructors:

```
public SCNSceneSource (Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNSceneSource (Foundation.NSData data, SCNSceneLoadingOptions options);
```

Removed method:

```
public static Foundation.NSObject FromData (Foundation.NSData data, Foundation.NSDictionary options);
```

Added methods:

```
public virtual Foundation.NSObject[] EntriesPassingTest (SCNSceneSourceFilter predicate);
	public static SCNSceneSource FromData (Foundation.NSData data, SCNSceneLoadingOptions options);
	public static SCNSceneSource FromData (Foundation.NSData data, Foundation.NSDictionary options);
	public SCNSceneSource FromUrl (Foundation.NSUrl url, SCNSceneLoadingOptions options);
	public SCNScene SceneFromOptions (SCNSceneLoadingOptions options, SCNSceneSourceStatusHandler statusHandler);
	public SCNScene SceneWithOption (SCNSceneLoadingOptions options, out Foundation.NSError error);
```

### Type Changed: SceneKit.SCNSceneSourceLoading

Removed properties:

```
public static Foundation.NSString AssetDirectoryURLsKey { get; }
	public static Foundation.NSString OverrideAssetURLsKey { get; }
```

Added properties:

```
public static Foundation.NSString AnimationImportPolicyDoNotPlay { get; }
	public static Foundation.NSString AnimationImportPolicyKey { get; }
	public static Foundation.NSString AnimationImportPolicyPlay { get; }
	public static Foundation.NSString AnimationImportPolicyPlayRepeatedly { get; }
	public static Foundation.NSString AnimationImportPolicyPlayUsingSceneTimeBase { get; }
	public static Foundation.NSString AssetDirectoryUrlsKey { get; }
	public static Foundation.NSString ConvertToYUpKey { get; }
	public static Foundation.NSString ConvertUnitsToMetersKey { get; }
	public static Foundation.NSString OverrideAssetUrlsKey { get; }
```

### Type Changed: SceneKit.SCNShaderModifiers

Added constructors:

```
public SCNShaderModifiers ();
	public SCNShaderModifiers (Foundation.NSDictionary dictionary);
```

Removed properties:

```
public static Foundation.NSString EntryPointFragment { get; }
	public static Foundation.NSString EntryPointGeometry { get; }
	public static Foundation.NSString EntryPointLightingModel { get; }
	public static Foundation.NSString EntryPointSurface { get; }
```

Added properties:

```
public string EntryPointFragment { get; set; }
	public string EntryPointGeometry { get; set; }
	public string EntryPointLightingModel { get; set; }
	public string EntryPointSurface { get; set; }
```

### Type Changed: SceneKit.SCNShape

Added constructor:

```
public SCNShape (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNSkinner

Added constructor:

```
public SCNSkinner (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
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

Added methods:

```
public static SCNSkinner Create (SCNGeometry baseGeometry, SCNNode[] bones, SCNMatrix4[] boneInverseBindTransforms, SCNGeometrySource boneWeights, SCNGeometrySource boneIndices);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
```

### Type Changed: SceneKit.SCNSphere

Added constructor:

```
public SCNSphere (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNText

Added constructor:

```
public SCNText (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

Removed property:

```
public virtual System.nint ChamferSegmentCount { get; set; }
```

Added properties:

```
public virtual AppKit.NSBezierPath ChamferProfile { get; set; }
	public virtual System.nfloat Flatness { get; set; }
```

### Type Changed: SceneKit.SCNTorus

Added constructor:

```
public SCNTorus (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNTransformConstraint

Removed constructor:

```
public SCNTransformConstraint ();
```

Added constructor:

```
public SCNTransformConstraint (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
```

### Type Changed: SceneKit.SCNTransformConstraintHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, CoreAnimation.CATransform3D transform, System.AsyncCallback callback, object object);
	public virtual CoreAnimation.CATransform3D EndInvoke (System.IAsyncResult result);
	public virtual CoreAnimation.CATransform3D Invoke (SCNNode node, CoreAnimation.CATransform3D transform);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (SCNNode node, SCNMatrix4 transform, System.AsyncCallback callback, object object);
	public virtual SCNMatrix4 EndInvoke (System.IAsyncResult result);
	public virtual SCNMatrix4 Invoke (SCNNode node, SCNMatrix4 transform);
```

### Type Changed: SceneKit.SCNTube

Added constructor:

```
public SCNTube (Foundation.NSCoder coder);
```

Added interfaces:

```
Foundation.INSCoding
	Foundation.INSSecureCoding
	ISCNAnimatable
	ISCNBoundingVolume
	ISCNShadable
```

### Type Changed: SceneKit.SCNVector3

Removed constructor:

```
public SCNVector3 (OpenGL.Vector3 vector);
```

Added constructors:

```
public SCNVector3 (OpenGL.Vector3 v);
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
public System.nfloat Length { get; }
	public System.nfloat LengthFast { get; }
	public System.nfloat LengthSquared { get; }
	public OpenGL.Vector2 Xy { get; set; }
```

Added methods:

```
[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector3 right);
	public static void Add (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Add (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector3 right);
	public static SCNVector3 BaryCentric (SCNVector3 a, SCNVector3 b, SCNVector3 c, System.nfloat u, System.nfloat v);
	public static void BaryCentric (ref SCNVector3 a, ref SCNVector3 b, ref SCNVector3 c, System.nfloat u, System.nfloat v, out SCNVector3 result);
	public static System.nfloat CalculateAngle (SCNVector3 first, SCNVector3 second);
	public static void CalculateAngle (ref SCNVector3 first, ref SCNVector3 second, out System.nfloat result);
	public static void Clamp (ref SCNVector3 vec, ref SCNVector3 min, ref SCNVector3 max, out SCNVector3 result);
	public static SCNVector3 Clamp (SCNVector3 vec, SCNVector3 min, SCNVector3 max);
	public static SCNVector3 ComponentMax (SCNVector3 a, SCNVector3 b);
	public static void ComponentMax (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 ComponentMin (SCNVector3 a, SCNVector3 b);
	public static void ComponentMin (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);
	public static SCNVector3 Cross (SCNVector3 left, SCNVector3 right);
	public static void Cross (ref SCNVector3 left, ref SCNVector3 right, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static void Div (ref SCNVector3 a, System.nfloat f, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static SCNVector3 Div (SCNVector3 a, System.nfloat f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (System.nfloat f);
	public static SCNVector3 Divide (SCNVector3 vector, System.nfloat scale);
	public static void Divide (ref SCNVector3 vector, System.nfloat scale, out SCNVector3 result);
	public static SCNVector3 Divide (SCNVector3 vector, SCNVector3 scale);
	public static void Divide (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static System.nfloat Dot (SCNVector3 left, SCNVector3 right);
	public static void Dot (ref SCNVector3 left, ref SCNVector3 right, out System.nfloat result);
	public virtual bool Equals (SCNVector3 other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static SCNVector3 Lerp (SCNVector3 a, SCNVector3 b, System.nfloat blend);
	public static void Lerp (ref SCNVector3 a, ref SCNVector3 b, System.nfloat blend, out SCNVector3 result);
	public static SCNVector3 Max (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 Min (SCNVector3 left, SCNVector3 right);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (System.nfloat f);

	[Obsolete ("Use static Multiply() method instead.")]
	public static void Mult (ref SCNVector3 a, System.nfloat f, out SCNVector3 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public static SCNVector3 Mult (SCNVector3 a, System.nfloat f);
	public static SCNVector3 Multiply (SCNVector3 vector, SCNVector3 scale);
	public static SCNVector3 Multiply (SCNVector3 vector, System.nfloat scale);
	public static void Multiply (ref SCNVector3 vector, System.nfloat scale, out SCNVector3 result);
	public static void Multiply (ref SCNVector3 vector, ref SCNVector3 scale, out SCNVector3 result);
	public static SCNVector3 Normalize (SCNVector3 vec);
	public static void Normalize (ref SCNVector3 vec, out SCNVector3 result);
	public void Normalize ();
	public void NormalizeFast ();
	public static SCNVector3 NormalizeFast (SCNVector3 vec);
	public static void NormalizeFast (ref SCNVector3 vec, out SCNVector3 result);
	public static SCNVector3 op_Addition (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Division (SCNVector3 vec, System.nfloat scale);
	public static bool op_Equality (SCNVector3 left, SCNVector3 right);
	public static bool op_Inequality (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_Multiply (SCNVector3 vec, System.nfloat scale);
	public static SCNVector3 op_Multiply (System.nfloat scale, SCNVector3 vec);
	public static SCNVector3 op_Subtraction (SCNVector3 left, SCNVector3 right);
	public static SCNVector3 op_UnaryNegation (SCNVector3 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (System.nfloat sx, System.nfloat sy, System.nfloat sz);

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

### Type Changed: SceneKit.SCNVector4

Removed constructor:

```
public SCNVector4 (OpenGL.Vector4 vector);
```

Added constructors:

```
public SCNVector4 (OpenGL.Vector2 v);
	public SCNVector4 (SCNVector3 v);
	public SCNVector4 (OpenGL.Vector3 v);
	public SCNVector4 (OpenGL.Vector4 v);
	public SCNVector4 (SCNVector3 v, System.nfloat w);
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
public System.nfloat Length { get; }
	public System.nfloat LengthFast { get; }
	public System.nfloat LengthSquared { get; }
	public OpenGL.Vector2 Xy { get; set; }
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
	public static SCNVector4 BaryCentric (SCNVector4 a, SCNVector4 b, SCNVector4 c, System.nfloat u, System.nfloat v);
	public static void BaryCentric (ref SCNVector4 a, ref SCNVector4 b, ref SCNVector4 c, System.nfloat u, System.nfloat v, out SCNVector4 result);
	public static void Clamp (ref SCNVector4 vec, ref SCNVector4 min, ref SCNVector4 max, out SCNVector4 result);
	public static SCNVector4 Clamp (SCNVector4 vec, SCNVector4 min, SCNVector4 max);
	public static void Div (ref SCNVector4 a, System.nfloat f, out SCNVector4 result);
	public static SCNVector4 Div (SCNVector4 a, System.nfloat f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (System.nfloat f);
	public static SCNVector4 Divide (SCNVector4 vector, SCNVector4 scale);
	public static void Divide (ref SCNVector4 vector, System.nfloat scale, out SCNVector4 result);
	public static void Divide (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Divide (SCNVector4 vector, System.nfloat scale);
	public static System.nfloat Dot (SCNVector4 left, SCNVector4 right);
	public static void Dot (ref SCNVector4 left, ref SCNVector4 right, out System.nfloat result);
	public override bool Equals (object obj);
	public virtual bool Equals (SCNVector4 other);
	public override int GetHashCode ();
	public static void Lerp (ref SCNVector4 a, ref SCNVector4 b, System.nfloat blend, out SCNVector4 result);
	public static SCNVector4 Lerp (SCNVector4 a, SCNVector4 b, System.nfloat blend);
	public static SCNVector4 Max (SCNVector4 a, SCNVector4 b);
	public static void Max (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static void Min (ref SCNVector4 a, ref SCNVector4 b, out SCNVector4 result);
	public static SCNVector4 Min (SCNVector4 a, SCNVector4 b);
	public static SCNVector4 Mult (SCNVector4 a, System.nfloat f);
	public static void Mult (ref SCNVector4 a, System.nfloat f, out SCNVector4 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (System.nfloat f);
	public static void Multiply (ref SCNVector4 vector, ref SCNVector4 scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, SCNVector4 scale);
	public static void Multiply (ref SCNVector4 vector, System.nfloat scale, out SCNVector4 result);
	public static SCNVector4 Multiply (SCNVector4 vector, System.nfloat scale);
	public void Normalize ();
	public static SCNVector4 Normalize (SCNVector4 vec);
	public static void Normalize (ref SCNVector4 vec, out SCNVector4 result);
	public void NormalizeFast ();
	public static void NormalizeFast (ref SCNVector4 vec, out SCNVector4 result);
	public static SCNVector4 NormalizeFast (SCNVector4 vec);
	public static SCNVector4 op_Addition (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Division (SCNVector4 vec, System.nfloat scale);
	public static bool op_Equality (SCNVector4 left, SCNVector4 right);
	public static System.nfloat* op_Explicit (SCNVector4 v);
	public static System.IntPtr op_Explicit (SCNVector4 v);
	public static bool op_Inequality (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_Multiply (System.nfloat scale, SCNVector4 vec);
	public static SCNVector4 op_Multiply (SCNVector4 vec, System.nfloat scale);
	public static SCNVector4 op_Subtraction (SCNVector4 left, SCNVector4 right);
	public static SCNVector4 op_UnaryNegation (SCNVector4 vec);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (System.nfloat sx, System.nfloat sy, System.nfloat sz, System.nfloat sw);

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

### Type Changed: SceneKit.SCNView

Added interface:

```
ISCNSceneRenderer
```

Removed properties:

```
public virtual System.IntPtr Context { get; }
	public virtual AppKit.NSOpenGLContext OpenGLContext { get; set; }
```

Added properties:

```
public virtual SCNAntialiasingMode AntialiasingMode { get; set; }
	public virtual AppKit.NSOpenGLContext Context { get; set; }
	public virtual SpriteKit.SKScene OverlayScene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
```

Added methods:

```
public SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual AppKit.NSImage Snapshot ();
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: SceneKit.SCNWrapMode

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

### New Type SceneKit._SCNShaderModifiers

```
public static class _SCNShaderModifiers {
}
```

### New Type SceneKit.ISCNActionable

```
public interface ISCNActionable : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNAnimatable

```
public interface ISCNAnimatable : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNBoundingVolume

```
public interface ISCNBoundingVolume : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNNodeRendererDelegate

```
public interface ISCNNodeRendererDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNPhysicsContactDelegate

```
public interface ISCNPhysicsContactDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNProgramDelegate

```
public interface ISCNProgramDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNSceneExportDelegate

```
public interface ISCNSceneExportDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNSceneRenderer

```
public interface ISCNSceneRenderer : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, Foundation.NSDictionary options);
}
```

### New Type SceneKit.ISCNSceneRendererDelegate

```
public interface ISCNSceneRendererDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNShadable

```
public interface ISCNShadable : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SceneKit.ISCNTechniqueSupport

```
public interface ISCNTechniqueSupport : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type SceneKit.SCNAction

```
public class SCNAction : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAction ();
	public SCNAction (Foundation.NSCoder coder);
	public SCNAction (Foundation.NSObjectFlag t);
	public SCNAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double DurationInSeconds { get; set; }
	public virtual System.nfloat Speed { get; set; }
	public virtual SCNActionTimingMode TimingMode { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNAction CustomAction (double seconds, SCNActionNodeWithElapsedTimeHandler handler);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SCNAction FadeIn (double durationInSeconds);
	public static SCNAction FadeOpacityBy (System.nfloat factor, double durationInSeconds);
	public static SCNAction FadeOpacityTo (System.nfloat opacity, double durationInSeconds);
	public static SCNAction FadeOut (double durationInSeconds);
	public static SCNAction FromJavascript (string script, double seconds);
	public static SCNAction Group (SCNAction[] actions);
	public static SCNAction MoveBy (SCNVector3 delta, double durationInSeconds);
	public static SCNAction MoveBy (System.nfloat deltaX, System.nfloat deltaY, System.nfloat deltaZ, double durationInSeconds);
	public static SCNAction MoveTo (SCNVector3 location, double durationInSeconds);
	public static SCNAction RemoveFromParentNode ();
	public static SCNAction RepeatAction (SCNAction action, System.nuint count);
	public static SCNAction RepeatActionForever (SCNAction action);
	public virtual SCNAction ReversedAction ();
	public static SCNAction RotateBy (System.nfloat angle, SCNVector3 axis, double durationInSeconds);
	public static SCNAction RotateBy (System.nfloat xAngle, System.nfloat yAngle, System.nfloat zAngle, double durationInSeconds);
	public static SCNAction RotateTo (System.nfloat xAngle, System.nfloat yAngle, System.nfloat zAngle, double durationInSeconds);
	public static SCNAction RotateTo (System.nfloat xAngle, System.nfloat yAngle, System.nfloat zAngle, double durationInSeconds, bool shortestUnitArc);
	public static SCNAction RotateTo (SCNVector4 axisAngle, double durationInSeconds);
	public static SCNAction Run (System.Action<SCNNode> handler, CoreFoundation.DispatchQueue queue);
	public static SCNAction Run (System.Action<SCNNode> handler);
	public static SCNAction ScaleBy (System.nfloat scale, double durationInSeconds);
	public static SCNAction ScaleTo (System.nfloat scale, double durationInSeconds);
	public static SCNAction Sequence (SCNAction[] actions);
	public virtual void SetTimingFunction (System.Action<float> timingFunction);
	public static SCNAction Wait (double durationInSeconds);
	public static SCNAction Wait (double durationInSeconds, double durationRange);
}
```

### New Type SceneKit.SCNActionable

```
public class SCNActionable : Foundation.NSObject, ISCNActionable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNActionable ();
	public SCNActionable (Foundation.NSObjectFlag t);
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

### New Type SceneKit.SCNActionable_Extensions

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

### New Type SceneKit.SCNActionNodeWithElapsedTimeHandler

```
public sealed delegate SCNActionNodeWithElapsedTimeHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNActionNodeWithElapsedTimeHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, System.nfloat elapsedTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (SCNNode node, System.nfloat elapsedTime);
}
```

### New Type SceneKit.SCNActionTimingMode

```
[Serializable]
public enum SCNActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type SceneKit.SCNAnimatable

```
public class SCNAnimatable : Foundation.NSObject, ISCNAnimatable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAnimatable ();
	public SCNAnimatable (Foundation.NSObjectFlag t);
	public SCNAnimatable (System.IntPtr handle);
	// methods
	public virtual void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key);
	public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);
	public virtual Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
}
```

### New Type SceneKit.SCNAnimatable_Extensions

```
public static class SCNAnimatable_Extensions {
	// methods
	public static void AddAnimation (ISCNAnimatable This, CoreAnimation.CAAnimation animation, Foundation.NSString key);
	public static CoreAnimation.CAAnimation GetAnimation (ISCNAnimatable This, Foundation.NSString key);
	public static Foundation.NSString[] GetAnimationKeys (ISCNAnimatable This);
	public static bool IsAnimationPaused (ISCNAnimatable This, Foundation.NSString key);
	public static void PauseAnimation (ISCNAnimatable This, Foundation.NSString key);
	public static void RemoveAllAnimations (ISCNAnimatable This);
	public static void RemoveAnimation (ISCNAnimatable This, Foundation.NSString key);
	public static void RemoveAnimation (ISCNAnimatable This, Foundation.NSString key, System.nfloat duration);
	public static void ResumeAnimation (ISCNAnimatable This, Foundation.NSString key);
}
```

### New Type SceneKit.SCNAntialiasingMode

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

### New Type SceneKit.SCNBindingHandler

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

### New Type SceneKit.SCNBoundingVolume

```
public class SCNBoundingVolume : Foundation.NSObject, ISCNBoundingVolume, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNBoundingVolume ();
	public SCNBoundingVolume (Foundation.NSObjectFlag t);
	public SCNBoundingVolume (System.IntPtr handle);
	// methods
	public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref System.nfloat radius);
}
```

### New Type SceneKit.SCNBoundingVolume_Extensions

```
public static class SCNBoundingVolume_Extensions {
	// methods
	public static bool GetBoundingBox (ISCNBoundingVolume This, ref SCNVector3 min, ref SCNVector3 max);
	public static bool GetBoundingSphere (ISCNBoundingVolume This, ref SCNVector3 center, ref System.nfloat radius);
}
```

### New Type SceneKit.SCNFieldForceEvaluator

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

### New Type SceneKit.SCNHitTestOptions

```
public class SCNHitTestOptions : Foundation.DictionaryContainer {
	// constructors
	public SCNHitTestOptions ();
	public SCNHitTestOptions (Foundation.NSDictionary dictionary);
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

### New Type SceneKit.SCNIKConstraint

```
public class SCNIKConstraint : SceneKit.SCNConstraint, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ISCNAnimatable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNIKConstraint (Foundation.NSCoder coder);
	public SCNIKConstraint (Foundation.NSObjectFlag t);
	public SCNIKConstraint (System.IntPtr handle);
	// properties
	public virtual SCNNode ChainRootNode { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 TargetPosition { get; set; }
	// methods
	public static SCNIKConstraint Create (SCNNode chainRootNode);
	protected override void Dispose (bool disposing);
	public virtual System.nfloat GetMaxAllowedRotationAngle (SCNNode node);
	public virtual void SetMaxAllowedRotationAnglet (System.nfloat angle, SCNNode node);
}
```

### New Type SceneKit.SCNJavaScript

```
public static class SCNJavaScript {
	// methods
	public static void ExportModule (JavaScriptCore.JSContext context);
}
```

### New Type SceneKit.SCNMatrix4

```
[Serializable]
public struct SCNMatrix4, System.IEquatable<SCNMatrix4> {
	// constructors
	public SCNMatrix4 (SCNVector4 row0, SCNVector4 row1, SCNVector4 row2, SCNVector4 row3);
	public SCNMatrix4 (System.nfloat m00, System.nfloat m01, System.nfloat m02, System.nfloat m03, System.nfloat m10, System.nfloat m11, System.nfloat m12, System.nfloat m13, System.nfloat m20, System.nfloat m21, System.nfloat m22, System.nfloat m23, System.nfloat m30, System.nfloat m31, System.nfloat m32, System.nfloat m33);
	public SCNMatrix4 (CoreAnimation.CATransform3D transform);
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
	public System.nfloat Determinant { get; }
	public System.nfloat M11 { get; set; }
	public System.nfloat M12 { get; set; }
	public System.nfloat M13 { get; set; }
	public System.nfloat M14 { get; set; }
	public System.nfloat M21 { get; set; }
	public System.nfloat M22 { get; set; }
	public System.nfloat M23 { get; set; }
	public System.nfloat M24 { get; set; }
	public System.nfloat M31 { get; set; }
	public System.nfloat M32 { get; set; }
	public System.nfloat M33 { get; set; }
	public System.nfloat M34 { get; set; }
	public System.nfloat M41 { get; set; }
	public System.nfloat M42 { get; set; }
	public System.nfloat M43 { get; set; }
	public System.nfloat M44 { get; set; }
	// methods
	public static void CreateFromAxisAngle (OpenGL.Vector3d axis, double angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateFromAxisAngle (SCNVector3 axis, System.nfloat angle);
	public static void CreateFromAxisAngle (SCNVector3 axis, System.nfloat angle, out SCNMatrix4 result);
	public static void CreateFromAxisAngle (OpenGL.Vector3 axis, float angle, out SCNMatrix4 result);
	public static void CreateOrthographic (System.nfloat width, System.nfloat height, System.nfloat zNear, System.nfloat zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographic (System.nfloat width, System.nfloat height, System.nfloat zNear, System.nfloat zFar);
	public static void CreateOrthographicOffCenter (System.nfloat left, System.nfloat right, System.nfloat bottom, System.nfloat top, System.nfloat zNear, System.nfloat zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreateOrthographicOffCenter (System.nfloat left, System.nfloat right, System.nfloat bottom, System.nfloat top, System.nfloat zNear, System.nfloat zFar);
	public static void CreatePerspectiveFieldOfView (System.nfloat fovy, System.nfloat aspect, System.nfloat zNear, System.nfloat zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveFieldOfView (System.nfloat fovy, System.nfloat aspect, System.nfloat zNear, System.nfloat zFar);
	public static void CreatePerspectiveOffCenter (System.nfloat left, System.nfloat right, System.nfloat bottom, System.nfloat top, System.nfloat zNear, System.nfloat zFar, out SCNMatrix4 result);
	public static SCNMatrix4 CreatePerspectiveOffCenter (System.nfloat left, System.nfloat right, System.nfloat bottom, System.nfloat top, System.nfloat zNear, System.nfloat zFar);
	public static void CreateRotationX (System.nfloat angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationX (System.nfloat angle);
	public static SCNMatrix4 CreateRotationY (System.nfloat angle);
	public static void CreateRotationY (System.nfloat angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateRotationZ (System.nfloat angle);
	public static void CreateRotationZ (System.nfloat angle, out SCNMatrix4 result);
	public static SCNMatrix4 CreateTranslation (SCNVector3 vector);
	public static SCNMatrix4 CreateTranslation (System.nfloat x, System.nfloat y, System.nfloat z);
	public static void CreateTranslation (System.nfloat x, System.nfloat y, System.nfloat z, out SCNMatrix4 result);
	public static void CreateTranslation (ref SCNVector3 vector, out SCNMatrix4 result);
	public virtual bool Equals (SCNMatrix4 other);
	public override bool Equals (object obj);

	[Obsolete ("Use CreatePerspectiveOffCenter instead.")]
	public static SCNMatrix4 Frustum (System.nfloat left, System.nfloat right, System.nfloat bottom, System.nfloat top, System.nfloat near, System.nfloat far);
	public override int GetHashCode ();
	public static SCNMatrix4 Invert (SCNMatrix4 mat);
	public void Invert ();
	public static SCNMatrix4 LookAt (SCNVector3 eye, SCNVector3 target, SCNVector3 up);
	public static SCNMatrix4 LookAt (System.nfloat eyeX, System.nfloat eyeY, System.nfloat eyeZ, System.nfloat targetX, System.nfloat targetY, System.nfloat targetZ, System.nfloat upX, System.nfloat upY, System.nfloat upZ);
	public static SCNMatrix4 Mult (SCNMatrix4 left, SCNMatrix4 right);
	public static void Mult (ref SCNMatrix4 left, ref SCNMatrix4 right, out SCNMatrix4 result);
	public static bool op_Equality (SCNMatrix4 left, SCNMatrix4 right);
	public static bool op_Inequality (SCNMatrix4 left, SCNMatrix4 right);
	public static SCNMatrix4 op_Multiply (SCNMatrix4 left, SCNMatrix4 right);

	[Obsolete ("Use CreatePerspectiveFieldOfView instead.")]
	public static SCNMatrix4 Perspective (System.nfloat fovy, System.nfloat aspect, System.nfloat near, System.nfloat far);

	[Obsolete ("Use CreateFromAxisAngle instead.")]
	public static SCNMatrix4 Rotate (SCNVector3 axis, System.nfloat angle);
	public static SCNMatrix4 Rotate (OpenGL.Quaternion q);
	public static SCNMatrix4 Rotate (OpenGL.Quaterniond q);

	[Obsolete ("Use CreateRotationX instead.")]
	public static SCNMatrix4 RotateX (System.nfloat angle);

	[Obsolete ("Use CreateRotationY instead.")]
	public static SCNMatrix4 RotateY (System.nfloat angle);

	[Obsolete ("Use CreateRotationZ instead.")]
	public static SCNMatrix4 RotateZ (System.nfloat angle);
	public static SCNMatrix4 Scale (System.nfloat x, System.nfloat y, System.nfloat z);
	public static SCNMatrix4 Scale (SCNVector3 scale);
	public static SCNMatrix4 Scale (System.nfloat scale);
	public override string ToString ();

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (SCNVector3 trans);

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (System.nfloat x, System.nfloat y, System.nfloat z);
	public static void Transpose (ref SCNMatrix4 mat, out SCNMatrix4 result);
	public void Transpose ();
	public static SCNMatrix4 Transpose (SCNMatrix4 mat);
}
```

### New Type SceneKit.SCNNodeRendererDelegate_Extensions

```
public static class SCNNodeRendererDelegate_Extensions {
	// methods
	public static void Render (ISCNNodeRendererDelegate This, SCNNode node, SCNRenderer renderer, Foundation.NSDictionary arguments);
}
```

### New Type SceneKit.SCNParticleBirthDirection

```
[Serializable]
public enum SCNParticleBirthDirection {
	Constant = 0,
	Random = 2,
	SurfaceNormal = 1,
}
```

### New Type SceneKit.SCNParticleBirthLocation

```
[Serializable]
public enum SCNParticleBirthLocation {
	Surface = 0,
	Vertex = 2,
	Volume = 1,
}
```

### New Type SceneKit.SCNParticleBlendMode

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

### New Type SceneKit.SCNParticleEvent

```
[Serializable]
public enum SCNParticleEvent {
	Birth = 0,
	Collision = 2,
	Death = 1,
}
```

### New Type SceneKit.SCNParticleEventHandler

```
public sealed delegate SCNParticleEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, System.nint count, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, System.IntPtr indices, System.nint count);
}
```

### New Type SceneKit.SCNParticleImageSequenceAnimationMode

```
[Serializable]
public enum SCNParticleImageSequenceAnimationMode {
	AutoReverse = 2,
	Clamp = 1,
	Repeat = 0,
}
```

### New Type SceneKit.SCNParticleInputMode

```
[Serializable]
public enum SCNParticleInputMode {
	OverDistance = 1,
	OverLife = 0,
	OverOtherProperty = 2,
}
```

### New Type SceneKit.SCNParticleModifierHandler

```
public sealed delegate SCNParticleModifierHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNParticleModifierHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr data, System.IntPtr dataStride, System.nint start, System.nint end, float deltaTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr data, System.IntPtr dataStride, System.nint start, System.nint end, float deltaTime);
}
```

### New Type SceneKit.SCNParticleModifierStage

```
[Serializable]
public enum SCNParticleModifierStage {
	PostCollision = 3,
	PostDynamics = 1,
	PreCollision = 2,
	PreDynamics = 0,
}
```

### New Type SceneKit.SCNParticleOrientationMode

```
[Serializable]
public enum SCNParticleOrientationMode {
	BillboardScreenAligned = 0,
	BillboardViewAligned = 1,
	BillboardYAligned = 3,
	Free = 2,
}
```

### New Type SceneKit.SCNParticlePropertyController

```
public class SCNParticlePropertyController : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticlePropertyController (Foundation.NSCoder coder);
	public SCNParticlePropertyController (Foundation.NSObjectFlag t);
	public SCNParticlePropertyController (System.IntPtr handle);
	// properties
	public virtual CoreAnimation.CAAnimation Animation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat InputBias { get; set; }
	public virtual SCNParticleInputMode InputMode { get; set; }
	public virtual SCNNode InputOrigin { get; set; }
	public virtual Foundation.NSString InputProperty { get; set; }
	public virtual System.nfloat InputScale { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNParticlePropertyController Create (CoreAnimation.CAAnimation animation);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SceneKit.SCNParticleSortingMode

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

### New Type SceneKit.SCNParticleSystem

```
public class SCNParticleSystem : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ISCNAnimatable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNParticleSystem (Foundation.NSCoder coder);
	public SCNParticleSystem (Foundation.NSObjectFlag t);
	public SCNParticleSystem (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Acceleration { get; set; }
	public virtual bool AffectedByGravity { get; set; }
	public virtual bool AffectedByPhysicsFields { get; set; }
	public virtual SCNParticleBirthDirection BirthDirection { get; set; }
	public virtual SCNParticleBirthLocation BirthLocation { get; set; }
	public virtual System.nfloat BirthRate { get; set; }
	public virtual System.nfloat BirthRateVariation { get; set; }
	public virtual bool BlackPassEnabled { get; set; }
	public virtual SCNParticleBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNNode[] ColliderNodes { get; set; }
	public virtual System.nfloat DampingFactor { get; set; }
	public virtual System.nfloat EmissionDuration { get; set; }
	public virtual System.nfloat EmissionDurationVariation { get; set; }
	public virtual SCNGeometry EmitterShape { get; set; }
	public virtual SCNVector3 EmittingDirection { get; set; }
	public virtual System.nfloat FresnelExponent { get; set; }
	public virtual System.nfloat IdleDuration { get; set; }
	public virtual System.nfloat IdleDurationVariation { get; set; }
	public virtual SCNParticleImageSequenceAnimationMode ImageSequenceAnimationMode { get; set; }
	public virtual System.nuint ImageSequenceColumnCount { get; set; }
	public virtual System.nfloat ImageSequenceFrameRate { get; set; }
	public virtual System.nfloat ImageSequenceFrameRateVariation { get; set; }
	public virtual System.nfloat ImageSequenceInitialFrame { get; set; }
	public virtual System.nfloat ImageSequenceInitialFrameVariation { get; set; }
	public virtual System.nuint ImageSequenceRowCount { get; set; }
	public virtual bool LightingEnabled { get; set; }
	public virtual bool Local { get; set; }
	public virtual bool Loops { get; set; }
	public virtual SCNParticleOrientationMode OrientationMode { get; set; }
	public virtual System.nfloat ParticleAngle { get; set; }
	public virtual System.nfloat ParticleAngleVariation { get; set; }
	public virtual System.nfloat ParticleAngularVelocity { get; set; }
	public virtual System.nfloat ParticleAngularVelocityVariation { get; set; }
	public virtual System.nfloat ParticleBounce { get; set; }
	public virtual System.nfloat ParticleBounceVariation { get; set; }
	public virtual System.nfloat ParticleCharge { get; set; }
	public virtual System.nfloat ParticleChargeVariation { get; set; }
	public virtual AppKit.NSColor ParticleColor { get; set; }
	public virtual SCNVector4 ParticleColorVariation { get; set; }
	public virtual bool ParticleDiesOnCollision { get; set; }
	public virtual System.nfloat ParticleFriction { get; set; }
	public virtual System.nfloat ParticleFrictionVariation { get; set; }
	public virtual Foundation.NSObject ParticleImage { get; set; }
	public virtual System.nfloat ParticleLifeSpan { get; set; }
	public virtual System.nfloat ParticleLifeSpanVariation { get; set; }
	public virtual System.nfloat ParticleMass { get; set; }
	public virtual System.nfloat ParticleMassVariation { get; set; }
	public virtual System.nfloat ParticleSize { get; set; }
	public virtual System.nfloat ParticleSizeVariation { get; set; }
	public virtual System.nfloat ParticleVelocity { get; set; }
	public virtual System.nfloat ParticleVelocityVariation { get; set; }
	public virtual SCNParticleSortingMode SortingMode { get; set; }
	public virtual System.nfloat SpeedFactor { get; set; }
	public virtual System.nfloat SpreadingAngle { get; set; }
	public virtual System.nfloat StretchFactor { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnCollision { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnDying { get; set; }
	public virtual SCNParticleSystem SystemSpawnedOnLiving { get; set; }
	public virtual System.nfloat WarmupDuration { get; set; }
	// methods
	public virtual void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key);
	public virtual void AddModifier (Foundation.NSString[] properties, SCNParticleModifierStage stage, SCNParticleModifierHandler handler);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNParticleSystem Create ();
	public static SCNParticleSystem Create (string name, string directory);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);
	public virtual Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleEvent (SCNParticleEvent evnt, Foundation.NSString[] properties, SCNParticleEventHandler handler);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAllModifiers ();
	public virtual void RemoveAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void RemoveModifiers (SCNParticleModifierStage stage);
	public virtual void Reset ();
	public virtual void ResumeAnimation (Foundation.NSString key);
}
```

### New Type SceneKit.SCNPhysicsBallSocketJoint

```
public class SCNPhysicsBallSocketJoint : SceneKit.SCNPhysicsBehavior, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBallSocketJoint (Foundation.NSCoder coder);
	public SCNPhysicsBallSocketJoint (Foundation.NSObjectFlag t);
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

### New Type SceneKit.SCNPhysicsBehavior

```
public class SCNPhysicsBehavior : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBehavior (Foundation.NSCoder coder);
	public SCNPhysicsBehavior (Foundation.NSObjectFlag t);
	public SCNPhysicsBehavior (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SceneKit.SCNPhysicsBody

```
public class SCNPhysicsBody : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsBody (Foundation.NSCoder coder);
	public SCNPhysicsBody (Foundation.NSObjectFlag t);
	public SCNPhysicsBody (System.IntPtr handle);
	// properties
	public virtual bool AllowsResting { get; set; }
	public virtual System.nfloat AngularDamping { get; set; }
	public virtual SCNVector4 AngularVelocity { get; set; }
	public virtual SCNVector3 AngularVelocityFactor { get; set; }
	public virtual System.nuint CategoryBitMask { get; set; }
	public virtual System.nfloat Charge { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nuint CollisionBitMask { get; set; }
	public virtual System.nfloat Damping { get; set; }
	public virtual System.nfloat Friction { get; set; }
	public virtual bool IsResting { get; }
	public virtual System.nfloat Mass { get; set; }
	public virtual SCNPhysicsShape PhysicsShape { get; set; }
	public virtual System.nfloat Restitution { get; set; }
	public virtual System.nfloat RollingFriction { get; set; }
	public virtual SCNPhysicsBodyType Type { get; set; }
	public virtual SCNVector3 Velocity { get; set; }
	public virtual SCNVector3 VelocityFactor { get; set; }
	// methods
	public virtual void ApplyForce (SCNVector3 direction, bool impulse);
	public virtual void ApplyForce (SCNVector3 direction, SCNVector3 position, bool impulse);
	public virtual void ApplyTorque (SCNVector4 torque, bool impulse);
	public virtual void ClearAllForces ();
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNPhysicsBody CreateBody (SCNPhysicsBodyType type, SCNPhysicsShape shape);
	public static SCNPhysicsBody CreateDynamicBody ();
	public static SCNPhysicsBody CreateKinematicBody ();
	public static SCNPhysicsBody CreateStaticBody ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void ResetTransform ();
}
```

### New Type SceneKit.SCNPhysicsBodyType

```
[Serializable]
public enum SCNPhysicsBodyType {
	Dynamic = 1,
	Kinematic = 2,
	Static = 0,
}
```

### New Type SceneKit.SCNPhysicsContact

```
public class SCNPhysicsContact : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContact (Foundation.NSObjectFlag t);
	public SCNPhysicsContact (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat CollisionImpulse { get; }
	public virtual SCNVector3 ContactNormal { get; }
	public virtual SCNVector3 ContactPoint { get; }
	public virtual SCNNode NodeA { get; }
	public virtual SCNNode NodeB { get; }
	public virtual System.nfloat PenetrationDistance { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type SceneKit.SCNPhysicsContactDelegate

```
public class SCNPhysicsContactDelegate : Foundation.NSObject, ISCNPhysicsContactDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsContactDelegate ();
	public SCNPhysicsContactDelegate (Foundation.NSObjectFlag t);
	public SCNPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidEndContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
	public virtual void DidUpdateContact (SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type SceneKit.SCNPhysicsContactDelegate_Extensions

```
public static class SCNPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidEndContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
	public static void DidUpdateContact (ISCNPhysicsContactDelegate This, SCNPhysicsWorld world, SCNPhysicsContact contact);
}
```

### New Type SceneKit.SCNPhysicsContactEventArgs

```
public class SCNPhysicsContactEventArgs : System.EventArgs {
	// constructors
	public SCNPhysicsContactEventArgs (SCNPhysicsContact contact);
	// properties
	public SCNPhysicsContact Contact { get; set; }
}
```

### New Type SceneKit.SCNPhysicsField

```
public class SCNPhysicsField : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsField (Foundation.NSCoder coder);
	public SCNPhysicsField (Foundation.NSObjectFlag t);
	public SCNPhysicsField (System.IntPtr handle);
	// properties
	public virtual bool Active { get; set; }
	public virtual System.nuint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 Direction { get; set; }
	public virtual bool Exclusive { get; set; }
	public virtual System.nfloat FalloffExponent { get; set; }
	public virtual SCNVector3 HalfExtent { get; set; }
	public virtual System.nfloat MinimumDistance { get; set; }
	public virtual SCNVector3 Offset { get; set; }
	public virtual SCNPhysicsFieldScope Scope { get; set; }
	public virtual System.nfloat Strength { get; set; }
	public virtual bool UsesEllipsoidalExtent { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNPhysicsField CreateDragField ();
	public static SCNPhysicsField CreateElectricField ();
	public static SCNPhysicsField CreateLinearGravityField ();
	public static SCNPhysicsField CreateMagneticField ();
	public static SCNPhysicsField CreateNoiseField (System.nfloat smoothness, System.nfloat speed);
	public static SCNPhysicsField CreateRadialGravityField ();
	public static SCNPhysicsField CreateSpringField ();
	public static SCNPhysicsField CreateTurbulenceField (System.nfloat smoothness, System.nfloat speed);
	public static SCNPhysicsField CreateVortexField ();
	public static SCNPhysicsField CustomField (SCNFieldForceEvaluator evaluator);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SceneKit.SCNPhysicsFieldScope

```
[Serializable]
public enum SCNPhysicsFieldScope {
	InsideExtent = 0,
	OutsideExtent = 1,
}
```

### New Type SceneKit.SCNPhysicsHingeJoint

```
public class SCNPhysicsHingeJoint : SceneKit.SCNPhysicsBehavior, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsHingeJoint (Foundation.NSCoder coder);
	public SCNPhysicsHingeJoint (Foundation.NSObjectFlag t);
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

### New Type SceneKit.SCNPhysicsSearchMode

```
[Serializable]
public enum SCNPhysicsSearchMode {
	All = 2,
	Any = 0,
	Closest = 1,
}
```

### New Type SceneKit.SCNPhysicsShape

```
public class SCNPhysicsShape : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsShape (Foundation.NSCoder coder);
	public SCNPhysicsShape (Foundation.NSObjectFlag t);
	public SCNPhysicsShape (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeOptions options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, SCNPhysicsShapeType? shapeType, bool? keepAsCompound, SCNVector3? scale);
	public static SCNPhysicsShape Create (SCNPhysicsShape[] shapes, SCNVector3[] transforms);
	public static SCNPhysicsShape Create (SCNNode node, Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNGeometry geometry, Foundation.NSDictionary options);
	public static SCNPhysicsShape Create (SCNNode node, SCNPhysicsShapeOptions options);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SceneKit.SCNPhysicsShapeOptions

```
public class SCNPhysicsShapeOptions {
	// constructors
	public SCNPhysicsShapeOptions ();
	// properties
	public bool? KeepAsCompound { get; set; }
	public SCNVector3? Scale { get; set; }
	public SCNPhysicsShapeType? ShapeType { get; set; }
	// methods
	public Foundation.NSDictionary ToDictionary ();
}
```

### New Type SceneKit.SCNPhysicsShapeOptionsKeys

```
public static class SCNPhysicsShapeOptionsKeys {
	// properties
	public static Foundation.NSString KeepAsCompound { get; }
	public static Foundation.NSString Scale { get; }
	public static Foundation.NSString Type { get; }
}
```

### New Type SceneKit.SCNPhysicsShapeOptionsTypes

```
public static class SCNPhysicsShapeOptionsTypes {
	// properties
	public static Foundation.NSString BoundingBox { get; }
	public static Foundation.NSString ConcavePolyhedron { get; }
	public static Foundation.NSString ConvexHull { get; }
}
```

### New Type SceneKit.SCNPhysicsShapeType

```
[Serializable]
public enum SCNPhysicsShapeType {
	BoundingBox = 1,
	ConcavePolyhedron = 2,
	ConvexHull = 0,
}
```

### New Type SceneKit.SCNPhysicsSliderJoint

```
public class SCNPhysicsSliderJoint : SceneKit.SCNPhysicsBehavior, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsSliderJoint (Foundation.NSCoder coder);
	public SCNPhysicsSliderJoint (Foundation.NSObjectFlag t);
	public SCNPhysicsSliderJoint (System.IntPtr handle);
	// properties
	public virtual SCNVector3 AnchorA { get; set; }
	public virtual SCNVector3 AnchorB { get; set; }
	public virtual SCNVector3 AxisA { get; set; }
	public virtual SCNVector3 AxisB { get; set; }
	public virtual SCNPhysicsBody BodyA { get; }
	public virtual SCNPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat MaximumAngularLimit { get; set; }
	public virtual System.nfloat MaximumLinearLimit { get; set; }
	public virtual System.nfloat MinimumAngularLimit { get; set; }
	public virtual System.nfloat MinimumLinearLimit { get; set; }
	public virtual System.nfloat MotorMaximumForce { get; set; }
	public virtual System.nfloat MotorMaximumTorque { get; set; }
	public virtual System.nfloat MotorTargetAngularVelocity { get; set; }
	public virtual System.nfloat MotorTargetLinearVelocity { get; set; }
	// methods
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody bodyA, SCNVector3 axisA, SCNVector3 anchorA, SCNPhysicsBody bodyB, SCNVector3 axisB, SCNVector3 anchorB);
	public static SCNPhysicsSliderJoint Create (SCNPhysicsBody body, SCNVector3 axis, SCNVector3 anchor);
	protected override void Dispose (bool disposing);
}
```

### New Type SceneKit.SCNPhysicsTest

```
public class SCNPhysicsTest : Foundation.DictionaryContainer {
	// constructors
	public SCNPhysicsTest ();
	public SCNPhysicsTest (Foundation.NSDictionary dictionary);
	// properties
	public System.nuint? CollisionBitMask { get; set; }
}
```

### New Type SceneKit.SCNPhysicsTestKeys

```
public static class SCNPhysicsTestKeys {
	// properties
	public static Foundation.NSString CollisionBitMaskKey { get; }
	public static Foundation.NSString SearchModeKey { get; }
}
```

### New Type SceneKit.SCNPhysicsTestSearchModeKeys

```
public static class SCNPhysicsTestSearchModeKeys {
	// properties
	public static Foundation.NSString All { get; }
	public static Foundation.NSString Any { get; }
	public static Foundation.NSString Closest { get; }
}
```

### New Type SceneKit.SCNPhysicsVehicle

```
public class SCNPhysicsVehicle : SceneKit.SCNPhysicsBehavior, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicle (Foundation.NSCoder coder);
	public SCNPhysicsVehicle (Foundation.NSObjectFlag t);
	public SCNPhysicsVehicle (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBody ChassisBody { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat SpeedInKilometersPerHour { get; }
	public virtual SCNPhysicsVehicleWheel[] Wheels { get; }
	// methods
	public virtual void ApplyBrakingForce (System.nfloat value, System.nint index);
	public virtual void ApplyEngineForce (System.nfloat value, System.nint index);
	public static SCNPhysicsVehicle Create (SCNPhysicsBody chassisBody, SCNPhysicsVehicleWheel[] wheels);
	protected override void Dispose (bool disposing);
	public virtual void SetSteeringAngle (System.nfloat value, System.nint index);
}
```

### New Type SceneKit.SCNPhysicsVehicleWheel

```
public class SCNPhysicsVehicleWheel : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsVehicleWheel (Foundation.NSCoder coder);
	public SCNPhysicsVehicleWheel (Foundation.NSObjectFlag t);
	public SCNPhysicsVehicleWheel (System.IntPtr handle);
	// properties
	public virtual SCNVector3 Axle { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNVector3 ConnectionPosition { get; set; }
	public virtual System.nfloat FrictionSlip { get; set; }
	public virtual System.nfloat MaximumSuspensionForce { get; set; }
	public virtual System.nfloat MaximumSuspensionTravel { get; set; }
	public virtual SCNNode Node { get; }
	public virtual System.nfloat Radius { get; set; }
	public virtual SCNVector3 SteeringAxis { get; set; }
	public virtual System.nfloat SuspensionCompression { get; set; }
	public virtual System.nfloat SuspensionDamping { get; set; }
	public virtual System.nfloat SuspensionRestLength { get; set; }
	public virtual System.nfloat SuspensionStiffness { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNPhysicsVehicleWheel Create (SCNNode node);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SceneKit.SCNPhysicsWorld

```
public class SCNPhysicsWorld : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNPhysicsWorld (Foundation.NSCoder coder);
	public SCNPhysicsWorld (Foundation.NSObjectFlag t);
	public SCNPhysicsWorld (System.IntPtr handle);
	// properties
	public virtual SCNPhysicsBehavior[] AllBehaviors { get; }
	public override System.IntPtr ClassHandle { get; }
	public SCNPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual SCNVector3 Gravity { get; set; }
	public virtual System.nfloat Speed { get; set; }
	public virtual double TimeStep { get; set; }
	public virtual Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidBeginContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidEndContact;
	public event System.EventHandler<SCNPhysicsContactEventArgs> DidUpdateContact;
	// methods
	public virtual void AddBehavior (SCNPhysicsBehavior behavior);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody bodyA, SCNPhysicsBody bodyB, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, Foundation.NSDictionary options);
	public SCNPhysicsContact[] ContactTest (SCNPhysicsBody body, SCNPhysicsTest options);
	public SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, SCNPhysicsTest options);
	public virtual SCNPhysicsContact[] ConvexSweepTest (SCNPhysicsShape shape, SCNMatrix4 from, SCNMatrix4 to, Foundation.NSDictionary options);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, Foundation.NSDictionary options);
	public SCNHitTestResult[] RayTestWithSegmentFromPoint (SCNVector3 origin, SCNVector3 dest, SCNPhysicsTest options);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (SCNPhysicsBehavior behavior);
	public virtual void UpdateCollisionPairs ();
}
```

### New Type SceneKit.SCNProgramDelegate_Extensions

```
public static class SCNProgramDelegate_Extensions {
	// methods
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
	public static void HandleError (ISCNProgramDelegate This, SCNProgram program, Foundation.NSError error);
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
}
```

### New Type SceneKit.SCNProgramSemanticOptions

```
public class SCNProgramSemanticOptions : Foundation.DictionaryContainer {
	// constructors
	public SCNProgramSemanticOptions ();
	public SCNProgramSemanticOptions (Foundation.NSDictionary dictionary);
	// properties
	public System.nuint? MappingChannel { get; set; }
}
```

### New Type SceneKit.SCNQuaternion

```
[Serializable]
public struct SCNQuaternion, System.IEquatable<SCNQuaternion> {
	// constructors
	public SCNQuaternion (SCNVector3 v, System.nfloat w);
	public SCNQuaternion (System.nfloat x, System.nfloat y, System.nfloat z, System.nfloat w);
	public SCNQuaternion (ref OpenGL.Matrix3d matrix);
	public SCNQuaternion (OpenGL.Quaternion openTkQuaternion);
	// fields
	public static SCNQuaternion Identity;
	// properties
	public float Length { get; }
	public float LengthSquared { get; }
	public System.nfloat W { get; set; }
	public System.nfloat X { get; set; }
	public SCNVector3 Xyz { get; set; }

	[Obsolete ("Use Xyz property instead.")]
	public SCNVector3 XYZ { get; set; }
	public System.nfloat Y { get; set; }
	public System.nfloat Z { get; set; }
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
	public void ToAxisAngle (out SCNVector3 axis, out System.nfloat angle);
	public override string ToString ();
}
```

### New Type SceneKit.SCNSceneExportDelegate

```
public class SCNSceneExportDelegate : Foundation.NSObject, ISCNSceneExportDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneExportDelegate ();
	public SCNSceneExportDelegate (Foundation.NSObjectFlag t);
	public SCNSceneExportDelegate (System.IntPtr handle);
	// methods
	public virtual Foundation.NSUrl WriteImage (AppKit.NSImage image, Foundation.NSUrl documentURL, Foundation.NSUrl originalImageURL);
}
```

### New Type SceneKit.SCNSceneExportDelegate_Extensions

```
public static class SCNSceneExportDelegate_Extensions {
	// methods
	public static Foundation.NSUrl WriteImage (ISCNSceneExportDelegate This, AppKit.NSImage image, Foundation.NSUrl documentURL, Foundation.NSUrl originalImageURL);
}
```

### New Type SceneKit.SCNSceneExportProgressHandler

```
public sealed delegate SCNSceneExportProgressHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneExportProgressHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (float totalProgress, Foundation.NSError error, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (float totalProgress, Foundation.NSError error, out bool stop);
}
```

### New Type SceneKit.SCNSceneLoadingOptions

```
public class SCNSceneLoadingOptions : Foundation.DictionaryContainer {
	// constructors
	public SCNSceneLoadingOptions ();
	public SCNSceneLoadingOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSUrl[] AssetDirectoryUrls { get; set; }
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

### New Type SceneKit.SCNSceneRenderer

```
public abstract class SCNSceneRenderer : Foundation.NSObject, ISCNSceneRenderer, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSceneRenderer ();
	public SCNSceneRenderer (Foundation.NSObjectFlag t);
	public SCNSceneRenderer (System.IntPtr handle);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public virtual System.IntPtr Context { get; }
	public virtual double CurrentTime { get; set; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public SCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual Foundation.NSObject WeakSceneRendererDelegate { get; set; }
	// methods
	public virtual SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, Foundation.NSDictionary options);
	public SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);
	public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
}
```

### New Type SceneKit.SCNSceneRenderer_Extensions

```
public static class SCNSceneRenderer_Extensions {
	// methods
	public static SCNHitTestResult[] HitTest (ISCNSceneRenderer This, CoreGraphics.CGPoint thePoint, SCNHitTestOptions options);
	public static bool IsNodeInsideFrustum (ISCNSceneRenderer This, SCNNode node, SCNNode pointOfView);
	public static bool Prepare (ISCNSceneRenderer This, Foundation.NSObject obj, System.Func<bool> abortHandler);
	public static void Prepare (ISCNSceneRenderer This, Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public static SCNVector3 ProjectPoint (ISCNSceneRenderer This, SCNVector3 point);
	public static SCNVector3 UnprojectPoint (ISCNSceneRenderer This, SCNVector3 point);
}
```

### New Type SceneKit.SCNSceneRendererDelegate_Extensions

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

### New Type SceneKit.SCNSceneSourceFilter

```
public sealed delegate SCNSceneSourceFilter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNSceneSourceFilter (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject entry, Foundation.NSString identifier, ref bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual bool Invoke (Foundation.NSObject entry, Foundation.NSString identifier, ref bool stop);
}
```

### New Type SceneKit.SCNShadable

```
public class SCNShadable : Foundation.NSObject, ISCNShadable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNShadable ();
	public SCNShadable (Foundation.NSObjectFlag t);
	public SCNShadable (System.IntPtr handle);
	// properties
	public virtual SCNProgram Program { get; set; }
	public SCNShaderModifiers ShaderModifiers { get; set; }
	public virtual Foundation.NSDictionary WeakShaderModifiers { get; set; }
	// methods
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual void HandleUnbinding (string symbol, SCNBindingHandler handler);
}
```

### New Type SceneKit.SCNShadable_Extensions

```
public static class SCNShadable_Extensions {
	// methods
	public static void HandleBinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
	public static void HandleUnbinding (ISCNShadable This, string symbol, SCNBindingHandler handler);
}
```

### New Type SceneKit.SCNShadowMode

```
[Serializable]
public enum SCNShadowMode {
	Deferred = 1,
	Forward = 0,
	Modulated = 2,
}
```

### New Type SceneKit.SCNTechnique

```
public class SCNTechnique : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ISCNAnimatable, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechnique (Foundation.NSCoder coder);
	public SCNTechnique (Foundation.NSObjectFlag t);
	public SCNTechnique (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSDictionary DictionaryRepresentation { get; }
	// methods
	public virtual void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SCNTechnique Create (Foundation.NSDictionary dictionary);
	public static SCNTechnique Create (SCNTechnique[] techniques);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);
	public virtual Foundation.NSString[] GetAnimationKeys ();
	public virtual void HandleBinding (string symbol, SCNBindingHandler handler);
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, System.nfloat duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
}
```

### New Type SceneKit.SCNTechniqueSupport

```
public abstract class SCNTechniqueSupport : Foundation.NSObject, ISCNTechniqueSupport, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTechniqueSupport ();
	public SCNTechniqueSupport (Foundation.NSObjectFlag t);
	public SCNTechniqueSupport (System.IntPtr handle);
	// properties
	public virtual SCNTechnique Technique { get; set; }
}
```

### New Type SceneKit.SCNTechniqueSupport_Extensions

```
public static class SCNTechniqueSupport_Extensions {
}
```

## Namespace StoreKit

### Type Changed: StoreKit.ISKProductsRequestDelegate

Added interface:

```
ISKRequestDelegate
```

### Type Changed: StoreKit.SKPaymentTransactionState

Added value:

```
Deferred = 4,
```

## Namespace WebKit

### New Type WebKit.IWKNavigationDelegate

```
public interface IWKNavigationDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type WebKit.IWKScriptMessageHandler

```
public interface IWKScriptMessageHandler : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type WebKit.IWKUIDelegate

```
public interface IWKUIDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type WebKit.WKBackForwardList

```
public class WKBackForwardList : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardList (Foundation.NSObjectFlag t);
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
	public virtual WKBackForwardListItem ItemAtIndex (System.nint index);
}
```

### New Type WebKit.WKBackForwardListItem

```
public class WKBackForwardListItem : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKBackForwardListItem (Foundation.NSObjectFlag t);
	public WKBackForwardListItem (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSUrl InitialUrl { get; }
	public virtual string Title { get; }
	public virtual Foundation.NSUrl Url { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKErrorCode

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

### New Type WebKit.WKFrameInfo

```
public class WKFrameInfo : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKFrameInfo ();
	public WKFrameInfo (Foundation.NSObjectFlag t);
	public WKFrameInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool MainFrame { get; }
	public virtual Foundation.NSUrlRequest Request { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKJavascriptEvaluationResult

```
public sealed delegate WKJavascriptEvaluationResult : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public WKJavascriptEvaluationResult (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSObject result, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSObject result, Foundation.NSError error);
}
```

### New Type WebKit.WKNavigation

```
public class WKNavigation : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigation ();
	public WKNavigation (Foundation.NSObjectFlag t);
	public WKNavigation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSError Error { get; }
	public virtual Foundation.NSUrlRequest InitialRequest { get; }
	public virtual Foundation.NSUrlRequest Request { get; }
	public virtual Foundation.NSUrlResponse Response { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKNavigationAction

```
public class WKNavigationAction : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationAction ();
	public WKNavigationAction (Foundation.NSObjectFlag t);
	public WKNavigationAction (System.IntPtr handle);
	// properties
	public virtual System.nint ButtonNumber { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AppKit.NSEventModifierMask ModifierFlags { get; }
	public virtual WKNavigationType NavigationType { get; }
	public virtual Foundation.NSUrlRequest Request { get; }
	public virtual WKFrameInfo SourceFrame { get; }
	public virtual WKFrameInfo TargetFrame { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKNavigationActionPolicy

```
[Serializable]
public enum WKNavigationActionPolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type WebKit.WKNavigationDelegate

```
public class WKNavigationDelegate : Foundation.NSObject, IWKNavigationDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationDelegate ();
	public WKNavigationDelegate (Foundation.NSObjectFlag t);
	public WKNavigationDelegate (System.IntPtr handle);
	// methods
	public virtual void DecidePolicy (WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public virtual void DecidePolicy (WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public virtual void DidCommitNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidFailNavigation (WKWebView webView, WKNavigation navigation, Foundation.NSError error);
	public virtual void DidFailProvisionalNavigation (WKWebView webView, WKNavigation navigation, Foundation.NSError error);
	public virtual void DidFinishNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidReceiveAuthenticationChallenge (WKWebView webView, Foundation.NSUrlAuthenticationChallenge challenge, System.Action<Foundation.NSUrlSessionAuthChallengeDisposition,Foundation.NSUrlCredential> completionHandler);
	public virtual void DidReceiveServerRedirectForProvisionalNavigation (WKWebView webView, WKNavigation navigation);
	public virtual void DidStartProvisionalNavigation (WKWebView webView, WKNavigation navigation);
}
```

### New Type WebKit.WKNavigationDelegate_Extensions

```
public static class WKNavigationDelegate_Extensions {
	// methods
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationAction navigationAction, System.Action<WKNavigationActionPolicy> decisionHandler);
	public static void DecidePolicy (IWKNavigationDelegate This, WKWebView webView, WKNavigationResponse navigationResponse, System.Action<WKNavigationResponsePolicy> decisionHandler);
	public static void DidCommitNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidFailNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, Foundation.NSError error);
	public static void DidFailProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation, Foundation.NSError error);
	public static void DidFinishNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidReceiveAuthenticationChallenge (IWKNavigationDelegate This, WKWebView webView, Foundation.NSUrlAuthenticationChallenge challenge, System.Action<Foundation.NSUrlSessionAuthChallengeDisposition,Foundation.NSUrlCredential> completionHandler);
	public static void DidReceiveServerRedirectForProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
	public static void DidStartProvisionalNavigation (IWKNavigationDelegate This, WKWebView webView, WKNavigation navigation);
}
```

### New Type WebKit.WKNavigationResponse

```
public class WKNavigationResponse : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKNavigationResponse ();
	public WKNavigationResponse (Foundation.NSObjectFlag t);
	public WKNavigationResponse (System.IntPtr handle);
	// properties
	public virtual bool CanShowMimeType { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsForMainFrame { get; }
	public virtual Foundation.NSUrlResponse Response { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKNavigationResponsePolicy

```
[Serializable]
public enum WKNavigationResponsePolicy {
	Allow = 1,
	Cancel = 0,
}
```

### New Type WebKit.WKNavigationType

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

### New Type WebKit.WKPreferences

```
public class WKPreferences : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKPreferences ();
	public WKPreferences (Foundation.NSObjectFlag t);
	public WKPreferences (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool JavaEnabled { get; set; }
	public virtual bool JavaScriptCanOpenWindowsAutomatically { get; set; }
	public virtual bool JavaScriptEnabled { get; set; }
	public virtual System.nfloat MinimumFontSize { get; set; }
	public virtual bool PlugInsEnabled { get; set; }
}
```

### New Type WebKit.WKProcessPool

```
public class WKProcessPool : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKProcessPool ();
	public WKProcessPool (Foundation.NSObjectFlag t);
	public WKProcessPool (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type WebKit.WKScriptMessage

```
public class WKScriptMessage : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessage ();
	public WKScriptMessage (Foundation.NSObjectFlag t);
	public WKScriptMessage (System.IntPtr handle);
	// properties
	public virtual Foundation.NSObject Body { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual WKFrameInfo FrameInfo { get; }
	public virtual string Name { get; }
	public virtual WKWebView WebView { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKScriptMessageHandler

```
public abstract class WKScriptMessageHandler : Foundation.NSObject, IWKScriptMessageHandler, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKScriptMessageHandler ();
	public WKScriptMessageHandler (Foundation.NSObjectFlag t);
	public WKScriptMessageHandler (System.IntPtr handle);
	// methods
	public virtual void DidReceiveScriptMessage (WKUserContentController userContentController, WKScriptMessage message);
}
```

### New Type WebKit.WKScriptMessageHandler_Extensions

```
public static class WKScriptMessageHandler_Extensions {
}
```

### New Type WebKit.WKSelectionGranularity

```
[Serializable]
public enum WKSelectionGranularity {
	Character = 1,
	Dynamic = 0,
}
```

### New Type WebKit.WKUIDelegate

```
public class WKUIDelegate : Foundation.NSObject, IWKUIDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUIDelegate ();
	public WKUIDelegate (Foundation.NSObjectFlag t);
	public WKUIDelegate (System.IntPtr handle);
	// methods
	public virtual WKWebView CreateWebView (WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public virtual void RunJavaScriptAlertPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public virtual void RunJavaScriptConfirmPanel (WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public virtual void RunJavaScriptTextInputPanel (WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type WebKit.WKUIDelegate_Extensions

```
public static class WKUIDelegate_Extensions {
	// methods
	public static WKWebView CreateWebView (IWKUIDelegate This, WKWebView webView, WKWebViewConfiguration configuration, WKNavigationAction navigationAction, WKWindowFeatures windowFeatures);
	public static void RunJavaScriptAlertPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action completionHandler);
	public static void RunJavaScriptConfirmPanel (IWKUIDelegate This, WKWebView webView, string message, WKFrameInfo frame, System.Action<bool> completionHandler);
	public static void RunJavaScriptTextInputPanel (IWKUIDelegate This, WKWebView webView, string prompt, string defaultText, WKFrameInfo frame, System.Action<string> completionHandler);
}
```

### New Type WebKit.WKUserContentController

```
public class WKUserContentController : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserContentController ();
	public WKUserContentController (Foundation.NSObjectFlag t);
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

### New Type WebKit.WKUserScript

```
public class WKUserScript : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKUserScript (Foundation.NSObjectFlag t);
	public WKUserScript (System.IntPtr handle);
	public WKUserScript (Foundation.NSString source, WKUserScriptInjectionTime injectionTime, bool isForMainFrameOnly);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKUserScriptInjectionTime InjectionTime { get; }
	public virtual bool IsForMainFrameOnly { get; }
	public virtual Foundation.NSString Source { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKUserScriptInjectionTime

```
[Serializable]
public enum WKUserScriptInjectionTime {
	AtDocumentEnd = 1,
	AtDocumentStart = 0,
}
```

### New Type WebKit.WKWebView

```
public class WKWebView : AppKit.NSView, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebView (Foundation.NSCoder coder);
	public WKWebView (Foundation.NSObjectFlag t);
	public WKWebView (System.IntPtr handle);
	public WKWebView (CoreGraphics.CGRect frame, WKWebViewConfiguration configuration);
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
	public virtual System.nfloat Magnification { get; set; }
	public WKNavigationDelegate NavigationDelegate { get; set; }
	public virtual string Title { get; }
	public WKUIDelegate UIDelegate { get; set; }
	public virtual Foundation.NSUrl Url { get; }
	public virtual Foundation.NSObject WeakNavigationDelegate { get; set; }
	public virtual Foundation.NSObject WeakUIDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EvaluateJavaScript (Foundation.NSString javascript, WKJavascriptEvaluationResult completionHandler);
	public virtual System.Threading.Tasks.Task<Foundation.NSObject> EvaluateJavaScriptAsync (Foundation.NSString javascript);
	public virtual WKNavigation GoBack ();
	public virtual WKNavigation GoForward ();
	public virtual WKNavigation GoTo (WKBackForwardListItem item);
	public virtual WKNavigation LoadHtmlString (Foundation.NSString htmlString, Foundation.NSUrl baseUrl);
	public virtual WKNavigation LoadRequest (Foundation.NSUrlRequest request);
	public virtual WKNavigation Reload ();
	public virtual WKNavigation ReloadFromOrigin ();
	public virtual void SetMagnification (System.nfloat magnification, CoreGraphics.CGPoint centerPoint);
	public virtual void StopLoading ();
}
```

### New Type WebKit.WKWebViewConfiguration

```
public class WKWebViewConfiguration : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWebViewConfiguration ();
	public WKWebViewConfiguration (Foundation.NSObjectFlag t);
	public WKWebViewConfiguration (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual WKPreferences Preferences { get; set; }
	public virtual WKProcessPool ProcessPool { get; set; }
	public virtual bool SuppressesIncrementalRendering { get; set; }
	public virtual WKUserContentController UserContentController { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
```

### New Type WebKit.WKWindowFeatures

```
public class WKWindowFeatures : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public WKWindowFeatures ();
	public WKWindowFeatures (Foundation.NSObjectFlag t);
	public WKWindowFeatures (System.IntPtr handle);
	// properties
	public bool? AllowsResizing { get; }
	public override System.IntPtr ClassHandle { get; }
	public System.nfloat? Height { get; }
	public bool? MenuBarVisibility { get; }
	public bool? StatusBarVisibility { get; }
	public bool? ToolbarsVisibility { get; }
	public System.nfloat? Width { get; }
	public System.nfloat? X { get; }
	public System.nfloat? Y { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

## New Namespace CloudKit

### New Type CloudKit.CKAccountStatus

```
[Serializable]
public enum CKAccountStatus {
	Available = 1,
	CouldNotDetermine = 0,
	NoAccount = 3,
	Restricted = 2,
}
```

### New Type CloudKit.CKApplicationPermissions

```
[Serializable]
[Flags]
public enum CKApplicationPermissions {
	UserDiscoverability = 1,
}
```

### New Type CloudKit.CKApplicationPermissionStatus

```
[Serializable]
public enum CKApplicationPermissionStatus {
	CouldNotComplete = 1,
	Denied = 2,
	Granted = 3,
	InitialState = 0,
}
```

### New Type CloudKit.CKAsset

```
public class CKAsset : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKAsset (Foundation.NSCoder coder);
	public CKAsset (Foundation.NSObjectFlag t);
	public CKAsset (System.IntPtr handle);
	public CKAsset (Foundation.NSUrl fileUrl);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSUrl FileUrl { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKContainer

```
public class CKContainer : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKContainer (Foundation.NSObjectFlag t);
	public CKContainer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public static CKContainer DefaultContainer { get; }
	public static Foundation.NSString OwnerDefaultName { get; }
	public virtual CKDatabase PrivateCloudDatabase { get; }
	public virtual CKDatabase PublicCloudDatabase { get; }
	// methods
	public virtual void AddOperation (CKOperation operation);
	public virtual void DiscoverAllContactUserInfos (System.Action<CKDiscoveredUserInfo[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo[]> DiscoverAllContactUserInfosAsync ();
	public virtual void DiscoverUserInfo (CKRecordID userRecordId, System.Action<CKDiscoveredUserInfo,Foundation.NSError> completionHandler);
	public virtual void DiscoverUserInfo (string email, System.Action<CKDiscoveredUserInfo,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (string email);
	public virtual System.Threading.Tasks.Task<CKDiscoveredUserInfo> DiscoverUserInfoAsync (CKRecordID userRecordId);
	protected override void Dispose (bool disposing);
	public virtual void FetchUserRecordId (System.Action<CKRecordID,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> FetchUserRecordIdAsync ();
	public static CKContainer FromIdentifier (string containerIdentifier);
	public virtual void GetAccountStatus (System.Action<CKAccountStatus,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKAccountStatus> GetAccountStatusAsync ();
	public virtual void RequestApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> RequestApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
	public virtual void StatusForApplicationPermission (CKApplicationPermissions applicationPermission, System.Action<CKApplicationPermissionStatus,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKApplicationPermissionStatus> StatusForApplicationPermissionAsync (CKApplicationPermissions applicationPermission);
}
```

### New Type CloudKit.CKDatabase

```
public class CKDatabase : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabase (Foundation.NSObjectFlag t);
	public CKDatabase (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void AddOperation (CKDatabaseOperation operation);
	public virtual void DeleteRecord (CKRecordID recordId, System.Action<CKRecordID,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordID> DeleteRecordAsync (CKRecordID recordId);
	public virtual void DeleteRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZoneID,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZoneID> DeleteRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void DeleteSubscription (string subscriptionID, CKDatabaseDeleteSubscriptionHandler completionHandler);
	public virtual System.Threading.Tasks.Task<string> DeleteSubscriptionAsync (string subscriptionID);
	public virtual void FetchAllRecordZones (System.Action<CKRecordZone[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone[]> FetchAllRecordZonesAsync ();
	public virtual void FetchAllSubscriptions (System.Action<CKSubscription[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription[]> FetchAllSubscriptionsAsync ();
	public virtual void FetchRecord (CKRecordID recordId, System.Action<CKRecord,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> FetchRecordAsync (CKRecordID recordId);
	public virtual void FetchRecordZone (CKRecordZoneID zoneId, System.Action<CKRecordZone,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> FetchRecordZoneAsync (CKRecordZoneID zoneId);
	public virtual void FetchSubscription (string subscriptionId, System.Action<CKSubscription,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> FetchSubscriptionAsync (string subscriptionId);
	public virtual void PerformQuery (CKQuery query, CKRecordZoneID zoneId, System.Action<CKRecord[],Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord[]> PerformQueryAsync (CKQuery query, CKRecordZoneID zoneId);
	public virtual void SaveRecord (CKRecord record, System.Action<CKRecord,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecord> SaveRecordAsync (CKRecord record);
	public virtual void SaveRecordZone (CKRecordZone zone, System.Action<CKRecordZone,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKRecordZone> SaveRecordZoneAsync (CKRecordZone zone);
	public virtual void SaveSubscription (CKSubscription subscription, System.Action<CKSubscription,Foundation.NSError> completionHandler);
	public virtual System.Threading.Tasks.Task<CKSubscription> SaveSubscriptionAsync (CKSubscription subscription);
}
```

### New Type CloudKit.CKDatabaseDeleteSubscriptionHandler

```
public sealed delegate CKDatabaseDeleteSubscriptionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDatabaseDeleteSubscriptionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (string subscriptionId, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (string subscriptionId, Foundation.NSError error);
}
```

### New Type CloudKit.CKDatabaseOperation

```
public class CKDatabaseOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDatabaseOperation (Foundation.NSObjectFlag t);
	public CKDatabaseOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKDatabase Database { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CloudKit.CKDiscoverAllContactsOperation

```
public class CKDiscoverAllContactsOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverAllContactsOperation ();
	public CKDiscoverAllContactsOperation (Foundation.NSObjectFlag t);
	public CKDiscoverAllContactsOperation (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKDiscoveredUserInfo[],Foundation.NSError> DiscoverAllContactsHandler { get; set; }
}
```

### New Type CloudKit.CKDiscoveredUserInfo

```
public class CKDiscoveredUserInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoveredUserInfo ();
	public CKDiscoveredUserInfo (Foundation.NSCoder coder);
	public CKDiscoveredUserInfo (Foundation.NSObjectFlag t);
	public CKDiscoveredUserInfo (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string FirstName { get; }
	public virtual string LastName { get; }
	public virtual CKRecordID UserRecordId { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKDiscoverUserInfosCompletionHandler

```
public sealed delegate CKDiscoverUserInfosCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKDiscoverUserInfosCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary emailsToUserInfos, Foundation.NSDictionary userRecordIdsToUserInfos, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSDictionary emailsToUserInfos, Foundation.NSDictionary userRecordIdsToUserInfos, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKDiscoverUserInfosOperation

```
public class CKDiscoverUserInfosOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKDiscoverUserInfosOperation ();
	public CKDiscoverUserInfosOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKErrorCode

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

### New Type CloudKit.CKErrorFields

```
public static class CKErrorFields {
	// properties
	public static Foundation.NSString ErrorDomain { get; }
	public static Foundation.NSString ErrorRetryAfterKey { get; }
	public static Foundation.NSString PartialErrorsByItemIdKey { get; }
	public static Foundation.NSString RecordChangedErrorAncestorRecordKey { get; }
	public static Foundation.NSString RecordChangedErrorClientRecordKey { get; }
	public static Foundation.NSString RecordChangedErrorServerRecordKey { get; }
}
```

### New Type CloudKit.CKFetchNotificationChangesOperation

```
public class CKFetchNotificationChangesOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchNotificationChangesOperation ();
	public CKFetchNotificationChangesOperation (Foundation.NSObjectFlag t);
	public CKFetchNotificationChangesOperation (System.IntPtr handle);
	public CKFetchNotificationChangesOperation (CKServerChangeToken previousServerChangeToken);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKServerChangeToken,Foundation.NSError> Completed { set; }
	public virtual bool MoreComing { get; }
	public virtual System.Action<CKNotification> NotificationChanged { set; }
	public virtual CKServerChangeToken PreviousServerChangeToken { get; set; }
	public virtual System.nuint ResultsLimit { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CloudKit.CKFetchRecordChangesHandler

```
public sealed delegate CKFetchRecordChangesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordChangesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKServerChangeToken serverChangeToken, Foundation.NSData clientChangeTokenData, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKFetchRecordChangesOperation

```
public class CKFetchRecordChangesOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordChangesOperation ();
	public CKFetchRecordChangesOperation (Foundation.NSObjectFlag t);
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
	public virtual System.nuint ResultsLimit { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CloudKit.CKFetchRecordsCompletedHandler

```
public sealed delegate CKFetchRecordsCompletedHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchRecordsCompletedHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary recordsByRecordId, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSDictionary recordsByRecordId, Foundation.NSError error);
}
```

### New Type CloudKit.CKFetchRecordsOperation

```
public class CKFetchRecordsOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordsOperation ();
	public CKFetchRecordsOperation (Foundation.NSObjectFlag t);
	public CKFetchRecordsOperation (System.IntPtr handle);
	public CKFetchRecordsOperation (CKRecordID[] recordIds);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKFetchRecordsCompletedHandler Completed { set; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual System.Action<CKRecord,CloudKit.CKRecordID,Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecordID,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIds { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static CKFetchRecordsOperation FetchCurrentUserRecordOperation ();
}
```

### New Type CloudKit.CKFetchRecordZonesOperation

```
public class CKFetchRecordZonesOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchRecordZonesOperation ();
	public CKFetchRecordZonesOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKFetchSubscriptionsCompleteHandler

```
public sealed delegate CKFetchSubscriptionsCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKFetchSubscriptionsCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary subscriptionsBySubscriptionId, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSDictionary subscriptionsBySubscriptionId, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKFetchSubscriptionsOperation

```
public class CKFetchSubscriptionsOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKFetchSubscriptionsOperation ();
	public CKFetchSubscriptionsOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKLocationSortDescriptor

```
public class CKLocationSortDescriptor : Foundation.NSSortDescriptor, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSCopying {
	// constructors
	public CKLocationSortDescriptor ();
	public CKLocationSortDescriptor (Foundation.NSCoder coder);
	public CKLocationSortDescriptor (Foundation.NSObjectFlag t);
	public CKLocationSortDescriptor (System.IntPtr handle);
	public CKLocationSortDescriptor (string key, CoreLocation.CLLocation relativeLocation);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreLocation.CLLocation RelativeLocation { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKMarkNotificationsReadHandler

```
public sealed delegate CKMarkNotificationsReadHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKMarkNotificationsReadHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKNotificationID[] notificationIDsMarkedRead, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKNotificationID[] notificationIDsMarkedRead, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKMarkNotificationsReadOperation

```
public class CKMarkNotificationsReadOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKMarkNotificationsReadOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKModifyBadgeOperation

```
public class CKModifyBadgeOperation : CloudKit.CKOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyBadgeOperation ();
	public CKModifyBadgeOperation (Foundation.NSObjectFlag t);
	public CKModifyBadgeOperation (System.IntPtr handle);
	public CKModifyBadgeOperation (System.nuint badgeValue);
	// properties
	public virtual System.nuint BadgeValue { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<Foundation.NSError> Completed { set; }
}
```

### New Type CloudKit.CKModifyRecordsOperation

```
public class CKModifyRecordsOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordsOperation ();
	public CKModifyRecordsOperation (Foundation.NSObjectFlag t);
	public CKModifyRecordsOperation (System.IntPtr handle);
	public CKModifyRecordsOperation (CKRecord[] records, CKRecordID[] recordIds);
	// properties
	public virtual bool Atomic { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSData ClientChangeTokenData { get; set; }
	public virtual CKModifyRecordsOperationHandler Completed { set; }
	public virtual System.Action<CKRecord,Foundation.NSError> PerRecordCompletion { set; }
	public virtual System.Action<CKRecord,System.Double> PerRecordProgress { set; }
	public virtual CKRecordID[] RecordIdsToDelete { get; set; }
	public virtual CKRecord[] RecordsToSave { get; set; }
	public virtual CKRecordSavePolicy SavePolicy { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CloudKit.CKModifyRecordsOperationHandler

```
public sealed delegate CKModifyRecordsOperationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordsOperationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecord[] savedRecords, CKRecordID[] deletedRecordIds, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKModifyRecordZonesHandler

```
public sealed delegate CKModifyRecordZonesHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifyRecordZonesHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKRecordZone[] savedRecordZones, CKRecordZoneID[] deletedRecordZoneIds, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKModifyRecordZonesOperation

```
public class CKModifyRecordZonesOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifyRecordZonesOperation ();
	public CKModifyRecordZonesOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKModifySubscriptionsHandler

```
public sealed delegate CKModifySubscriptionsHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKModifySubscriptionsHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (CKSubscription[] savedSubscriptions, string[] deletedSubscriptionIds, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKModifySubscriptionsOperation

```
public class CKModifySubscriptionsOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKModifySubscriptionsOperation ();
	public CKModifySubscriptionsOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKNotification

```
public class CKNotification : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotification (Foundation.NSCoder coder);
	public CKNotification (Foundation.NSObjectFlag t);
	public CKNotification (System.IntPtr handle);
	// properties
	public virtual string AlertActionLocalizationKey { get; }
	public virtual string AlertBody { get; }
	public virtual string AlertLaunchImage { get; }
	public virtual string[] AlertLocalizationArgs { get; }
	public virtual string AlertLocalizationKey { get; }
	public virtual Foundation.NSNumber Badge { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string ContainerIdentifier { get; }
	public virtual bool IsPruned { get; }
	public virtual CKNotificationID NotificationId { get; }
	public virtual CKNotificationType NotificationType { get; }
	public virtual string SoundName { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static CKNotification FromRemoteNotificationDictionary (Foundation.NSDictionary notificationDictionary);
}
```

### New Type CloudKit.CKNotificationID

```
public class CKNotificationID : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationID ();
	public CKNotificationID (Foundation.NSCoder coder);
	public CKNotificationID (Foundation.NSObjectFlag t);
	public CKNotificationID (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKNotificationInfo

```
public class CKNotificationInfo : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKNotificationInfo ();
	public CKNotificationInfo (Foundation.NSCoder coder);
	public CKNotificationInfo (Foundation.NSObjectFlag t);
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
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKNotificationType

```
[Serializable]
public enum CKNotificationType {
	Query = 1,
	ReadNotification = 3,
	RecordZone = 2,
}
```

### New Type CloudKit.CKOperation

```
public class CKOperation : Foundation.NSOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKOperation (Foundation.NSObjectFlag t);
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

### New Type CloudKit.CKQuery

```
public class CKQuery : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQuery (Foundation.NSCoder coder);
	public CKQuery (Foundation.NSObjectFlag t);
	public CKQuery (System.IntPtr handle);
	public CKQuery (string recordType, Foundation.NSPredicate predicate);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual Foundation.NSSortDescriptor[] SortDescriptors { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKQueryCursor

```
public class CKQueryCursor : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryCursor (Foundation.NSCoder coder);
	public CKQueryCursor (Foundation.NSObjectFlag t);
	public CKQueryCursor (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKQueryNotification

```
public class CKQueryNotification : CloudKit.CKNotification, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryNotification (Foundation.NSCoder coder);
	public CKQueryNotification (Foundation.NSObjectFlag t);
	public CKQueryNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool IsPublicDatabase { get; }
	public virtual CKQueryNotificationReason QueryNotificationReason { get; }
	public virtual Foundation.NSDictionary RecordFields { get; }
	public virtual CKRecordID RecordId { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKQueryNotificationReason

```
[Serializable]
public enum CKQueryNotificationReason {
	RecordCreated = 1,
	RecordDeleted = 3,
	RecordUpdated = 2,
}
```

### New Type CloudKit.CKQueryOperation

```
public class CKQueryOperation : CloudKit.CKDatabaseOperation, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKQueryOperation ();
	public CKQueryOperation (Foundation.NSObjectFlag t);
	public CKQueryOperation (System.IntPtr handle);
	public CKQueryOperation (CKQuery query);
	public CKQueryOperation (CKQueryCursor cursor);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.Action<CKQueryCursor,Foundation.NSError> Completed { set; }
	public virtual CKQueryCursor Cursor { get; set; }
	public virtual string[] DesiredKeys { get; set; }
	public virtual CKQuery Query { get; set; }
	public virtual System.Action<CKRecord> RecordFetched { set; }
	public virtual System.nuint ResultsLimit { get; set; }
	public virtual CKRecordZoneID ZoneId { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type CloudKit.CKRecord

```
public class CKRecord : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecord (Foundation.NSCoder coder);
	public CKRecord (Foundation.NSObjectFlag t);
	public CKRecord (System.IntPtr handle);
	public CKRecord (string recordType);
	public CKRecord (string recordType, CKRecordID recordId);
	public CKRecord (string recordType, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual Foundation.NSDate CreationDate { get; }
	public virtual CKRecordID CreatorUserRecordId { get; }
	public Foundation.NSObject Item { get; set; }
	public virtual CKRecordID LastModifiedUserRecordId { get; }
	public virtual Foundation.NSDate ModificationDate { get; }
	public virtual string RecordChangeTag { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual string RecordType { get; }
	public static Foundation.NSString TypeUserRecord { get; }
	// methods
	public virtual string[] AllKeys ();
	public virtual string[] AllTokens ();
	public virtual string[] ChangedKeys ();
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeSystemFields (Foundation.NSCoder coder);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKRecordID

```
public class CKRecordID : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordID ();
	public CKRecordID (Foundation.NSCoder coder);
	public CKRecordID (Foundation.NSObjectFlag t);
	public CKRecordID (System.IntPtr handle);
	public CKRecordID (string recordName);
	public CKRecordID (string recordName, CKRecordZoneID zoneId);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string RecordName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKRecordSavePolicy

```
[Serializable]
public enum CKRecordSavePolicy {
	SaveAllKeys = 2,
	SaveChangedKeys = 1,
	SaveIfServerRecordUnchanged = 0,
}
```

### New Type CloudKit.CKRecordValue

```
public class CKRecordValue : Foundation.NSObject, ICKRecordValue, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordValue ();
	public CKRecordValue (Foundation.NSObjectFlag t);
	public CKRecordValue (System.IntPtr handle);
}
```

### New Type CloudKit.CKRecordValue_Extensions

```
public static class CKRecordValue_Extensions {
}
```

### New Type CloudKit.CKRecordZone

```
public class CKRecordZone : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZone ();
	public CKRecordZone (Foundation.NSCoder coder);
	public CKRecordZone (Foundation.NSObjectFlag t);
	public CKRecordZone (System.IntPtr handle);
	public CKRecordZone (string zoneName);
	public CKRecordZone (CKRecordZoneID zoneId);
	// properties
	public virtual CKRecordZoneCapabilities Capabilities { get; }
	public override System.IntPtr ClassHandle { get; }
	public static Foundation.NSString DefaultName { get; }
	public virtual CKRecordZoneID ZoneId { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static CKRecordZone DefaultRecordZone ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKRecordZoneCapabilities

```
[Serializable]
[Flags]
public enum CKRecordZoneCapabilities {
	Atomic = 2,
	FetchChanges = 1,
}
```

### New Type CloudKit.CKRecordZoneCompleteHandler

```
public sealed delegate CKRecordZoneCompleteHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CKRecordZoneCompleteHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (Foundation.NSDictionary recordZonesByZoneId, Foundation.NSError operationError, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (Foundation.NSDictionary recordZonesByZoneId, Foundation.NSError operationError);
}
```

### New Type CloudKit.CKRecordZoneID

```
public class CKRecordZoneID : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneID ();
	public CKRecordZoneID (Foundation.NSCoder coder);
	public CKRecordZoneID (Foundation.NSObjectFlag t);
	public CKRecordZoneID (System.IntPtr handle);
	public CKRecordZoneID (string zoneName, string ownerName);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string OwnerName { get; }
	public virtual string ZoneName { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKRecordZoneNotification

```
public class CKRecordZoneNotification : CloudKit.CKNotification, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKRecordZoneNotification (Foundation.NSCoder coder);
	public CKRecordZoneNotification (Foundation.NSObjectFlag t);
	public CKRecordZoneNotification (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordZoneID RecordZoneId { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKReference

```
public class CKReference : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKReference (Foundation.NSCoder coder);
	public CKReference (Foundation.NSObjectFlag t);
	public CKReference (System.IntPtr handle);
	public CKReference (CKRecordID recordId, CKReferenceAction action);
	public CKReference (CKRecord record, CKReferenceAction action);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKRecordID RecordId { get; }
	public virtual CKReferenceAction ReferenceAction { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKReferenceAction

```
[Serializable]
public enum CKReferenceAction {
	DeleteSelf = 1,
	None = 0,
}
```

### New Type CloudKit.CKServerChangeToken

```
public class CKServerChangeToken : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKServerChangeToken (Foundation.NSCoder coder);
	public CKServerChangeToken (Foundation.NSObjectFlag t);
	public CKServerChangeToken (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKSubscription

```
public class CKSubscription : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CKSubscription (Foundation.NSCoder coder);
	public CKSubscription (Foundation.NSObjectFlag t);
	public CKSubscription (System.IntPtr handle);
	public CKSubscription (string recordType, Foundation.NSPredicate predicate, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (string recordType, Foundation.NSPredicate predicate, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, CKSubscriptionOptions subscriptionOptions);
	public CKSubscription (CKRecordZoneID zoneId, string subscriptionId, CKSubscriptionOptions subscriptionOptions);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CKNotificationInfo NotificationInfo { get; set; }
	public virtual Foundation.NSPredicate Predicate { get; }
	public virtual string RecordType { get; }
	public virtual string SubscriptionId { get; }
	public virtual CKSubscriptionOptions SubscriptionOptions { get; }
	public virtual CKSubscriptionType SubscriptionType { get; }
	public virtual CKRecordZoneID ZoneID { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type CloudKit.CKSubscriptionOptions

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

### New Type CloudKit.CKSubscriptionType

```
[Serializable]
public enum CKSubscriptionType {
	Query = 1,
	RecordZone = 2,
}
```

### New Type CloudKit.ICKRecordValue

```
public interface ICKRecordValue : ObjCRuntime.INativeObject, System.IDisposable {
}
```

## New Namespace GLKit

### New Type GLKit.GLKBaseEffect

```
public class GLKBaseEffect : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKBaseEffect ();
	public GLKBaseEffect (Foundation.NSObjectFlag t);
	public GLKBaseEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool ColorMaterialEnabled { get; set; }
	public virtual OpenGL.Vector4 ConstantColor { get; set; }
	public virtual GLKEffectPropertyFog Fog { get; }
	public virtual string Label { get; set; }
	public virtual GLKEffectPropertyLight Light0 { get; }
	public virtual GLKEffectPropertyLight Light1 { get; }
	public virtual GLKEffectPropertyLight Light2 { get; }
	public virtual GLKLightingType LightingType { get; set; }
	public virtual OpenGL.Vector4 LightModelAmbientColor { get; set; }
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

### New Type GLKit.GLKEffectProperty

```
public class GLKEffectProperty : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectProperty ();
	public GLKEffectProperty (Foundation.NSObjectFlag t);
	public GLKEffectProperty (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
}
```

### New Type GLKit.GLKEffectPropertyFog

```
public class GLKEffectPropertyFog : GLKit.GLKEffectProperty, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyFog ();
	public GLKEffectPropertyFog (Foundation.NSObjectFlag t);
	public GLKEffectPropertyFog (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Vector4 Color { get; set; }
	public virtual float Density { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual float End { get; set; }
	public virtual GLKFogMode Mode { get; set; }
	public virtual float Start { get; set; }
}
```

### New Type GLKit.GLKEffectPropertyLight

```
public class GLKEffectPropertyLight : GLKit.GLKEffectProperty, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyLight ();
	public GLKEffectPropertyLight (Foundation.NSObjectFlag t);
	public GLKEffectPropertyLight (System.IntPtr handle);
	// properties
	public virtual OpenGL.Vector4 AmbientColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float ConstantAttenuation { get; set; }
	public virtual OpenGL.Vector4 DiffuseColor { get; set; }
	public virtual bool Enabled { get; set; }
	public virtual float LinearAttenuation { get; set; }
	public virtual OpenGL.Vector4 Position { get; set; }
	public virtual float QuadraticAttenuation { get; set; }
	public virtual OpenGL.Vector4 SpecularColor { get; set; }
	public virtual float SpotCutoff { get; set; }
	public virtual OpenGL.Vector3 SpotDirection { get; set; }
	public virtual float SpotExponent { get; set; }
	public virtual GLKEffectPropertyTransform Transform { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type GLKit.GLKEffectPropertyMaterial

```
public class GLKEffectPropertyMaterial : GLKit.GLKEffectProperty, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyMaterial ();
	public GLKEffectPropertyMaterial (Foundation.NSObjectFlag t);
	public GLKEffectPropertyMaterial (System.IntPtr handle);
	// properties
	public virtual OpenGL.Vector4 AmbientColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Vector4 DiffuseColor { get; set; }
	public virtual OpenGL.Vector4 EmissiveColor { get; set; }
	public virtual float Shininess { get; set; }
	public virtual OpenGL.Vector4 SpecularColor { get; set; }
}
```

### New Type GLKit.GLKEffectPropertyTexture

```
public class GLKEffectPropertyTexture : GLKit.GLKEffectProperty, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyTexture ();
	public GLKEffectPropertyTexture (Foundation.NSObjectFlag t);
	public GLKEffectPropertyTexture (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual GLKTextureEnvMode EnvMode { get; set; }
	public virtual uint GLName { get; set; }
	public virtual GLKTextureTarget Target { get; set; }
}
```

### New Type GLKit.GLKEffectPropertyTransform

```
public class GLKEffectPropertyTransform : GLKit.GLKEffectProperty, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKEffectPropertyTransform ();
	public GLKEffectPropertyTransform (Foundation.NSObjectFlag t);
	public GLKEffectPropertyTransform (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Matrix4 ModelViewMatrix { get; set; }
	public virtual OpenGL.Matrix3d NormalMatrix { get; }
	public virtual OpenGL.Matrix4 ProjectionMatrix { get; set; }
}
```

### New Type GLKit.GLKFogMode

```
[Serializable]
public enum GLKFogMode {
	Exp = 0,
	Exp2 = 1,
	Linear = 2,
}
```

### New Type GLKit.GLKLightingType

```
[Serializable]
public enum GLKLightingType {
	PerPixel = 1,
	PerVertex = 0,
}
```

### New Type GLKit.GLKNamedEffect

```
public abstract class GLKNamedEffect : Foundation.NSObject, IGLKNamedEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKNamedEffect ();
	public GLKNamedEffect (Foundation.NSObjectFlag t);
	public GLKNamedEffect (System.IntPtr handle);
	// methods
	public virtual void PrepareToDraw ();
}
```

### New Type GLKit.GLKNamedEffect_Extensions

```
public static class GLKNamedEffect_Extensions {
}
```

### New Type GLKit.GLKReflectionMapEffect

```
public class GLKReflectionMapEffect : GLKit.GLKBaseEffect, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKReflectionMapEffect ();
	public GLKReflectionMapEffect (Foundation.NSObjectFlag t);
	public GLKReflectionMapEffect (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Matrix3d Matrix { get; set; }
	public virtual GLKEffectPropertyTexture TextureCubeMap { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void PrepareToDraw ();
}
```

### New Type GLKit.GLKSkyboxEffect

```
public class GLKSkyboxEffect : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKSkyboxEffect ();
	public GLKSkyboxEffect (Foundation.NSObjectFlag t);
	public GLKSkyboxEffect (System.IntPtr handle);
	// properties
	public virtual OpenGL.Vector3 Center { get; set; }
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

### New Type GLKit.GLKTextureEnvMode

```
[Serializable]
public enum GLKTextureEnvMode {
	Decal = 2,
	Modulate = 1,
	Replace = 0,
}
```

### New Type GLKit.GLKTextureInfo

```
public class GLKTextureInfo : Foundation.NSObject, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKTextureInfo ();
	public GLKTextureInfo (Foundation.NSObjectFlag t);
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
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
}
```

### New Type GLKit.GLKTextureInfoAlphaState

```
[Serializable]
public enum GLKTextureInfoAlphaState {
	None = 0,
	NonPremultiplied = 1,
	Premultiplied = 2,
}
```

### New Type GLKit.GLKTextureInfoOrigin

```
[Serializable]
public enum GLKTextureInfoOrigin {
	BottomLeft = 2,
	TopLeft = 1,
	Unknown = 0,
}
```

### New Type GLKit.GLKTextureLoader

```
public class GLKTextureLoader : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GLKTextureLoader ();
	public GLKTextureLoader (Foundation.NSObjectFlag t);
	public GLKTextureLoader (System.IntPtr handle);
	// properties
	public static Foundation.NSString ApplyPremultiplication { get; }
	public override System.IntPtr ClassHandle { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public static Foundation.NSString ErrorKey { get; }
	public static Foundation.NSString GenerateMipmaps { get; }
	public static Foundation.NSString GLErrorKey { get; }
	public static Foundation.NSString GrayscaleAsAlpha { get; }
	public static Foundation.NSString OriginBottomLeft { get; }
	public static Foundation.NSString SRGB { get; }
	// methods
	public virtual void BeginLoadCubeMap (string fileName, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (Foundation.NSUrl filePath, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string[] files, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (Foundation.NSUrl[] urls, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string[] files, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginLoadCubeMap (string fileName, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginLoadCubeMap (Foundation.NSUrl filePath, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginLoadCubeMapAsync (Foundation.NSUrl filePath, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginLoadCubeMapAsync (string fileName, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public void BeginTextureLoad (CoreGraphics.CGImage image, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (Foundation.NSData data, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (Foundation.NSUrl filePath, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (Foundation.NSUrl filePath, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (string file, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (CoreGraphics.CGImage image, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public void BeginTextureLoad (string file, GLKTextureOperations textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual void BeginTextureLoad (Foundation.NSData data, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (string file, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (Foundation.NSData data, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (CoreGraphics.CGImage image, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public virtual System.Threading.Tasks.Task<GLKTextureInfo> BeginTextureLoadAsync (Foundation.NSUrl filePath, Foundation.NSDictionary textureOperations, CoreFoundation.DispatchQueue queue);
	public static GLKTextureInfo CubeMapFromFile (string path, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFile (string path, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFiles (string[] files, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromFiles (string[] files, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrl (Foundation.NSUrl url, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrl (Foundation.NSUrl url, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrls (Foundation.NSUrl[] urls, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo CubeMapFromUrls (Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromData (Foundation.NSData data, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromData (Foundation.NSData data, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromFile (string path, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromFile (string path, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromImage (CoreGraphics.CGImage cgImage, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromImage (CoreGraphics.CGImage cgImage, GLKTextureOperations textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromUrl (Foundation.NSUrl url, Foundation.NSDictionary textureOperations, out Foundation.NSError error);
	public static GLKTextureInfo FromUrl (Foundation.NSUrl url, GLKTextureOperations textureOperations, out Foundation.NSError error);
}
```

### New Type GLKit.GLKTextureLoaderCallback

```
public sealed delegate GLKTextureLoaderCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public GLKTextureLoaderCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (GLKTextureInfo textureInfo, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (GLKTextureInfo textureInfo, Foundation.NSError error);
}
```

### New Type GLKit.GLKTextureLoaderError

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

### New Type GLKit.GLKTextureOperations

```
public class GLKTextureOperations : Foundation.DictionaryContainer {
	// constructors
	public GLKTextureOperations ();
	public GLKTextureOperations (Foundation.NSDictionary options);
	// properties
	public bool? ApplyPremultiplication { get; set; }
	public bool? GenerateMipmaps { get; set; }
	public bool? GrayscaleAsAlpha { get; set; }
	public bool? OriginBottomLeft { get; set; }
	public bool? SRGB { get; set; }
}
```

### New Type GLKit.GLKTextureTarget

```
[Serializable]
public enum GLKTextureTarget {
	CubeMap = 34067,
	TargetCt = 2,
	Texture2D = 3553,
}
```

### New Type GLKit.GLKVertexAttrib

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

### New Type GLKit.GLKViewDrawableColorFormat

```
[Serializable]
public enum GLKViewDrawableColorFormat {
	RGB565 = 1,
	RGBA8888 = 0,
	SRGBA8888 = 2,
}
```

### New Type GLKit.GLKViewDrawableDepthFormat

```
[Serializable]
public enum GLKViewDrawableDepthFormat {
	Format16 = 1,
	Format24 = 2,
	None = 0,
}
```

### New Type GLKit.GLKViewDrawableMultisample

```
[Serializable]
public enum GLKViewDrawableMultisample {
	None = 0,
	Sample4x = 1,
}
```

### New Type GLKit.GLKViewDrawableStencilFormat

```
[Serializable]
public enum GLKViewDrawableStencilFormat {
	Format8 = 1,
	FormatNone = 0,
}
```

### New Type GLKit.IGLKNamedEffect

```
public interface IGLKNamedEffect : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void PrepareToDraw ();
}
```

## New Namespace LocalAuthentication

### New Type LocalAuthentication.LAContext

```
public class LAContext : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public LAContext ();
	public LAContext (Foundation.NSObjectFlag t);
	public LAContext (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public virtual string LocalizedFallbackTitle { get; set; }
	// methods
	public virtual bool CanEvaluatePolicy (LAPolicy policy, Foundation.NSError error);
	public virtual void EvaluatePolicy (LAPolicy policy, string localizedReason, LAContextReplyHandler reply);
	public virtual System.Threading.Tasks.Task<bool> EvaluatePolicyAsync (LAPolicy policy, string localizedReason);
}
```

### New Type LocalAuthentication.LAContextReplyHandler

```
public sealed delegate LAContextReplyHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public LAContextReplyHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool success, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool success, Foundation.NSError error);
}
```

### New Type LocalAuthentication.LAPolicy

```
[Serializable]
public enum LAPolicy {
	DeviceOwnerAuthenticationWithBiometrics = 1,
}
```

### New Type LocalAuthentication.LAStatus

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

## New Namespace SpriteKit

### New Type SpriteKit.ISKPhysicsContactDelegate

```
public interface ISKPhysicsContactDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SpriteKit.ISKSceneDelegate

```
public interface ISKSceneDelegate : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type SpriteKit.SK3DNode

```
public class SK3DNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SK3DNode ();
	public SK3DNode (Foundation.NSCoder coder);
	public SK3DNode (Foundation.NSObjectFlag t);
	public SK3DNode (System.IntPtr handle);
	public SK3DNode (CoreGraphics.CGSize viewportSize);
	// properties
	public virtual bool AutoenablesDefaultLighting { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Loops { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SceneKit.SCNNode PointOfView { get; set; }
	public virtual double SceneTime { get; set; }
	public virtual SceneKit.SCNScene ScnScene { get; set; }
	public virtual CoreGraphics.CGSize ViewportSize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SK3DNode FromViewportSize (CoreGraphics.CGSize viewportSize);
	public virtual SceneKit.SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, Foundation.NSDictionary options);
	public SceneKit.SCNHitTestResult[] HitTest (CoreGraphics.CGPoint thePoint, SceneKit.SCNHitTestOptions options);
	public virtual OpenGL.Vector3 ProjectPoint (OpenGL.Vector3 point);
	public virtual OpenGL.Vector3 UnprojectPoint (OpenGL.Vector3 point);
}
```

### New Type SpriteKit.SKAction

```
public class SKAction : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKAction (Foundation.NSCoder coder);
	public SKAction (Foundation.NSObjectFlag t);
	public SKAction (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double Duration { get; set; }
	public virtual SKAction ReversedAction { get; }
	public virtual System.nfloat Speed { get; set; }
	public virtual SKActionTimingMode TimingMode { get; set; }
	// methods
	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec);
	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec, bool resize, bool restore);
	public static SKAction ColorizeWithColor (AppKit.NSColor color, System.nfloat colorBlendFactor, double sec);
	public static SKAction ColorizeWithColorBlendFactor (System.nfloat colorBlendFactor, double sec);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKAction CustomActionWithDuration (double seconds, SKActionDurationHandler actionHandler);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SKAction FadeAlphaBy (System.nfloat factor, double sec);
	public static SKAction FadeAlphaTo (System.nfloat alpha, double sec);
	public static SKAction FadeInWithDuration (double sec);
	public static SKAction FadeOutWithDuration (double sec);
	public static SKAction Falloff (float to, double duration);
	public static SKAction FollowPath (CoreGraphics.CGPath path, bool offset, bool orient, System.nfloat speed);
	public static SKAction FollowPath (CoreGraphics.CGPath path, System.nfloat speed);
	public static SKAction FollowPath (CoreGraphics.CGPath path, bool offset, bool orient, double sec);
	public static SKAction FollowPath (CoreGraphics.CGPath path, double sec);
	public static SKAction Group (SKAction[] actions);
	public static SKAction Hide ();
	public static SKAction MoveBy (System.nfloat deltaX, System.nfloat deltaY, double sec);
	public static SKAction MoveBy (CoreGraphics.CGVector delta, double duration);
	public static SKAction MoveTo (CoreGraphics.CGPoint location, double sec);
	public static SKAction MoveToX (System.nfloat x, double sec);
	public static SKAction MoveToY (System.nfloat y, double sec);
	public static SKAction PerformSelector (ObjCRuntime.Selector selector, Foundation.NSObject target);
	public static SKAction PlaySoundFileNamed (string soundFile, bool wait);
	public static SKAction ReachTo (CoreGraphics.CGPoint position, SKNode rootNode, double secs);
	public static SKAction ReachTo (CoreGraphics.CGPoint position, SKNode rootNode, System.nfloat velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, System.nfloat velocity);
	public static SKAction ReachToNode (SKNode node, SKNode rootNode, double sec);
	public static SKAction RemoveFromParent ();
	public static SKAction RepeatAction (SKAction action, System.nuint count);
	public static SKAction RepeatActionForever (SKAction action);
	public static SKAction ResizeByWidth (System.nfloat width, System.nfloat height, double duration);
	public static SKAction ResizeTo (System.nfloat width, System.nfloat height, double duration);
	public static SKAction ResizeTo (CoreGraphics.CGSize size, double duration);
	public static SKAction ResizeToHeight (System.nfloat height, double duration);
	public static SKAction ResizeToWidth (System.nfloat width, double duration);
	public static SKAction RotateByAngle (System.nfloat radians, double sec);
	public static SKAction RotateToAngle (System.nfloat radians, double sec, bool shortedUnitArc);
	public static SKAction RotateToAngle (System.nfloat radians, double sec);
	public static SKAction Run (System.Action block, CoreFoundation.DispatchQueue queue);
	public static SKAction Run (System.Action block);
	public static SKAction RunAction (SKAction action, string name);

	[Obsolete ("Use Run(Action) instead")]
	public static SKAction RunBlock (System.Action block);

	[Obsolete ("Use Run(Action,DispatchQueue) instead")]
	public static SKAction RunBlock (System.Action block, CoreFoundation.DispatchQueue queue);
	public static SKAction ScaleBy (System.nfloat scale, double sec);
	public static SKAction ScaleBy (System.nfloat xScale, System.nfloat yScale, double sec);
	public static SKAction ScaleTo (System.nfloat xScale, System.nfloat yScale, double sec);
	public static SKAction ScaleTo (System.nfloat scale, double sec);
	public static SKAction ScaleXTo (System.nfloat scale, double sec);
	public static SKAction ScaleYTo (System.nfloat scale, double sec);
	public static SKAction Sequence (SKAction[] actions);
	public static SKAction SetTexture (SKTexture texture);
	public static SKAction SetTexture (SKTexture texture, bool resize);
	public virtual void SetTimingFunction (SKActionTimingFunction timingFunction);
	public static SKAction SpeedBy (System.nfloat speed, double sec);
	public static SKAction SpeedTo (System.nfloat speed, double sec);
	public static SKAction StrengthBy (float strength, double sec);
	public static SKAction StrengthTo (float strength, double sec);
	public static SKAction Unhide ();
	public static SKAction WaitForDuration (double sec, double durationRange);
	public static SKAction WaitForDuration (double sec);
}
```

### New Type SpriteKit.SKActionDurationHandler

```
public sealed delegate SKActionDurationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKActionDurationHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKNode node, System.nfloat elapsedTime, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (SKNode node, System.nfloat elapsedTime);
}
```

### New Type SpriteKit.SKActionTimingFunction

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

### New Type SpriteKit.SKActionTimingMode

```
[Serializable]
public enum SKActionTimingMode {
	EaseIn = 1,
	EaseInEaseOut = 3,
	EaseOut = 2,
	Linear = 0,
}
```

### New Type SpriteKit.SKBlendMode

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

### New Type SpriteKit.SKConstraint

```
public class SKConstraint : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKConstraint ();
	public SKConstraint (Foundation.NSCoder coder);
	public SKConstraint (Foundation.NSObjectFlag t);
	public SKConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual SKNode ReferenceNode { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKConstraint CreateDistance (SKRange range, SKNode node);
	public static SKConstraint CreateDistance (SKRange range, CoreGraphics.CGPoint point);
	public static SKConstraint CreateDistance (SKRange range, CoreGraphics.CGPoint point, SKNode node);
	public static SKConstraint CreateOrientToNode (SKNode node, SKRange radians);
	public static SKConstraint CreateOrientToPoint (CoreGraphics.CGPoint point, SKNode node, SKRange radians);
	public static SKConstraint CreateOrientToPoint (CoreGraphics.CGPoint point, SKRange radians);
	public static SKConstraint CreateRestriction (SKRange xRange, SKRange yRange);
	public static SKConstraint CreateXRestriction (SKRange range);
	public static SKConstraint CreateYRestriction (SKRange range);
	public static SKConstraint CreateZRotation (SKRange zRange);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SpriteKit.SKCropNode

```
public class SKCropNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKCropNode ();
	public SKCropNode (Foundation.NSCoder coder);
	public SKCropNode (Foundation.NSObjectFlag t);
	public SKCropNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SKNode MaskNode { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type SpriteKit.SKEffectNode

```
public class SKEffectNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKEffectNode ();
	public SKEffectNode (Foundation.NSCoder coder);
	public SKEffectNode (Foundation.NSObjectFlag t);
	public SKEffectNode (System.IntPtr handle);
	// properties
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreImage.CIFilter Filter { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual bool ShouldCenterFilter { get; set; }
	public virtual bool ShouldEnableEffects { get; set; }
	public virtual bool ShouldRasterize { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type SpriteKit.SKEmitterNode

```
public class SKEmitterNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKEmitterNode ();
	public SKEmitterNode (Foundation.NSCoder coder);
	public SKEmitterNode (Foundation.NSObjectFlag t);
	public SKEmitterNode (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat EmissionAngle { get; set; }
	public virtual System.nfloat EmissionAngleRange { get; set; }
	public virtual uint FieldBitMask { get; set; }
	public virtual System.nuint NumParticlesToEmit { get; set; }
	public virtual SKAction ParticleAction { get; set; }
	public virtual System.nfloat ParticleAlpha { get; set; }
	public virtual System.nfloat ParticleAlphaRange { get; set; }
	public virtual SKKeyframeSequence ParticleAlphaSequence { get; set; }
	public virtual System.nfloat ParticleAlphaSpeed { get; set; }
	public virtual System.nfloat ParticleBirthRate { get; set; }
	public virtual SKBlendMode ParticleBlendMode { get; set; }
	public virtual AppKit.NSColor ParticleColor { get; set; }
	public virtual System.nfloat ParticleColorAlphaRange { get; set; }
	public virtual System.nfloat ParticleColorAlphaSpeed { get; set; }
	public virtual System.nfloat ParticleColorBlendFactor { get; set; }
	public virtual System.nfloat ParticleColorBlendFactorRange { get; set; }
	public virtual SKKeyframeSequence ParticleColorBlendFactorSequence { get; set; }
	public virtual System.nfloat ParticleColorBlendFactorSpeed { get; set; }
	public virtual System.nfloat ParticleColorBlueRange { get; set; }
	public virtual System.nfloat ParticleColorBlueSpeed { get; set; }
	public virtual System.nfloat ParticleColorGreenRange { get; set; }
	public virtual System.nfloat ParticleColorGreenSpeed { get; set; }
	public virtual System.nfloat ParticleColorRedRange { get; set; }
	public virtual System.nfloat ParticleColorRedSpeed { get; set; }
	public virtual SKKeyframeSequence ParticleColorSequence { get; set; }
	public virtual System.nfloat ParticleLifetime { get; set; }
	public virtual System.nfloat ParticleLifetimeRange { get; set; }
	public virtual CoreGraphics.CGPoint ParticlePosition { get; set; }
	public virtual CoreGraphics.CGVector ParticlePositionRange { get; set; }
	public virtual System.nfloat ParticleRotation { get; set; }
	public virtual System.nfloat ParticleRotationRange { get; set; }
	public virtual System.nfloat ParticleRotationSpeed { get; set; }
	public virtual System.nfloat ParticleScale { get; set; }
	public virtual System.nfloat ParticleScaleRange { get; set; }
	public virtual SKKeyframeSequence ParticleScaleSequence { get; set; }
	public virtual System.nfloat ParticleScaleSpeed { get; set; }
	public virtual CoreGraphics.CGSize ParticleSize { get; set; }
	public virtual System.nfloat ParticleSpeed { get; set; }
	public virtual System.nfloat ParticleSpeedRange { get; set; }
	public virtual SKTexture ParticleTexture { get; set; }
	public virtual System.nfloat ParticleZPosition { get; set; }
	public virtual System.nfloat ParticleZPositionRange { get; set; }
	public virtual System.nfloat ParticleZPositionSpeed { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual SKNode TargetNode { get; set; }
	public virtual System.nfloat XAcceleration { get; set; }
	public virtual System.nfloat YAcceleration { get; set; }
	// methods
	public virtual void AdvanceSimulationTime (double sec);
	protected override void Dispose (bool disposing);
	public virtual void ResetSimulation ();
}
```

### New Type SpriteKit.SKFieldForceEvaluator

```
public sealed delegate SKFieldForceEvaluator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKFieldForceEvaluator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (OpenGL.Vector4 position, OpenGL.Vector4 velocity, float mass, float charge, double time, System.AsyncCallback callback, object object);
	public virtual OpenGL.Vector3 EndInvoke (System.IAsyncResult result);
	public virtual OpenGL.Vector3 Invoke (OpenGL.Vector4 position, OpenGL.Vector4 velocity, float mass, float charge, double time);
}
```

### New Type SpriteKit.SKFieldNode

```
public class SKFieldNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKFieldNode ();
	public SKFieldNode (Foundation.NSCoder coder);
	public SKFieldNode (Foundation.NSObjectFlag t);
	public SKFieldNode (System.IntPtr handle);
	// properties
	public virtual float AnimationSpeed { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Vector4 Direction { get; set; }
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
	public static SKFieldNode CreateLinearGravityField (OpenGL.Vector4 direction);
	public static SKFieldNode CreateMagneticField ();
	public static SKFieldNode CreateNoiseField (System.nfloat smoothness, System.nfloat speed);
	public static SKFieldNode CreateRadialGravityField ();
	public static SKFieldNode CreateSpringField ();
	public static SKFieldNode CreateTurbulenceField (System.nfloat smoothness, System.nfloat speed);
	public static SKFieldNode CreateVelocityField (OpenGL.Vector4 direction);
	public static SKFieldNode CreateVelocityField (SKTexture velocityTexture);
	protected override void Dispose (bool disposing);
}
```

### New Type SpriteKit.SKInterpolationMode

```
[Serializable]
public enum SKInterpolationMode {
	Linear = 1,
	Spline = 2,
	Step = 3,
}
```

### New Type SpriteKit.SKKeyframeSequence

```
public class SKKeyframeSequence : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKKeyframeSequence ();
	public SKKeyframeSequence (Foundation.NSObject[] values, float[] times);
	public SKKeyframeSequence (Foundation.NSObject[] values, Foundation.NSNumber[] times);
	public SKKeyframeSequence (System.nuint numItems);
	public SKKeyframeSequence (System.IntPtr handle);
	public SKKeyframeSequence (Foundation.NSObjectFlag t);
	public SKKeyframeSequence (Foundation.NSCoder coder);
	public SKKeyframeSequence (Foundation.NSObject[] values, double[] times);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nuint Count { get; }
	public virtual SKInterpolationMode InterpolationMode { get; set; }
	public virtual SKRepeatMode RepeatMode { get; set; }
	// methods
	public virtual void AddKeyframeValue (Foundation.NSObject value, System.nfloat time);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual System.nfloat GetKeyframeTime (System.nuint index);
	public virtual Foundation.NSObject GetKeyframeValue (System.nuint index);
	public virtual void RemoveKeyframe (System.nuint index);
	public virtual void RemoveLastKeyframe ();
	public virtual Foundation.NSObject SampleAtTime (System.nfloat time);
	public virtual void SetKeyframeTime (System.nfloat time, System.nuint index);
	public virtual void SetKeyframeValue (Foundation.NSObject value, System.nuint index);
	public virtual void SetKeyframeValue (Foundation.NSObject value, System.nfloat time, System.nuint index);
}
```

### New Type SpriteKit.SKLabelHorizontalAlignmentMode

```
[Serializable]
public enum SKLabelHorizontalAlignmentMode {
	Center = 0,
	Left = 1,
	Right = 2,
}
```

### New Type SpriteKit.SKLabelNode

```
public class SKLabelNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKLabelNode ();
	public SKLabelNode (Foundation.NSCoder coder);
	public SKLabelNode (Foundation.NSObjectFlag t);
	public SKLabelNode (System.IntPtr handle);
	public SKLabelNode (string fontName);
	// properties
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AppKit.NSColor Color { get; set; }
	public virtual System.nfloat ColorBlendFactor { get; set; }
	public virtual AppKit.NSColor FontColor { get; set; }
	public virtual string FontName { get; set; }
	public virtual System.nfloat FontSize { get; set; }
	public virtual SKLabelHorizontalAlignmentMode HorizontalAlignmentMode { get; set; }
	public virtual string Text { get; set; }
	public virtual SKLabelVerticalAlignmentMode VerticalAlignmentMode { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SKLabelNode FromFont (string fontName);
	public static SKLabelNode FromText (string text);
}
```

### New Type SpriteKit.SKLabelVerticalAlignmentMode

```
[Serializable]
public enum SKLabelVerticalAlignmentMode {
	Baseline = 0,
	Bottom = 3,
	Center = 1,
	Top = 2,
}
```

### New Type SpriteKit.SKLightNode

```
public class SKLightNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKLightNode ();
	public SKLightNode (Foundation.NSCoder coder);
	public SKLightNode (Foundation.NSObjectFlag t);
	public SKLightNode (System.IntPtr handle);
	// properties
	public virtual AppKit.NSColor AmbientColor { get; set; }
	public virtual uint CategoryBitMask { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	public virtual System.nfloat Falloff { get; set; }
	public virtual AppKit.NSColor LightColor { get; set; }
	public virtual AppKit.NSColor ShadowColor { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type SpriteKit.SKMutableTexture

```
public class SKMutableTexture : SpriteKit.SKTexture, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKMutableTexture (Foundation.NSCoder coder);
	public SKMutableTexture (Foundation.NSObjectFlag t);
	public SKMutableTexture (System.IntPtr handle);
	public SKMutableTexture (CoreGraphics.CGSize size);
	public SKMutableTexture (CoreGraphics.CGSize size, CoreVideo.CVPixelFormatType pixelFormat);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SKMutableTexture Create (CoreGraphics.CGSize size);
	public virtual void ModifyPixelData (SKTextureModify modifyMethod);
}
```

### New Type SpriteKit.SKNode

```
public class SKNode : AppKit.NSResponder, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKNode ();
	public SKNode (Foundation.NSCoder coder);
	public SKNode (Foundation.NSObjectFlag t);
	public SKNode (System.IntPtr handle);
	// properties
	public virtual System.nfloat Alpha { get; set; }
	public virtual SKNode[] Children { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SKConstraint[] Constraints { get; set; }
	public virtual CoreGraphics.CGRect Frame { get; }
	public virtual bool HasActions { get; }
	public virtual bool Hidden { get; set; }
	public virtual string Name { get; set; }
	public virtual SKNode Parent { get; }
	public virtual bool Paused { get; set; }
	public virtual SKPhysicsBody PhysicsBody { get; set; }
	public virtual CoreGraphics.CGPoint Position { get; set; }
	public virtual SKReachConstraints ReachConstraints { get; set; }
	public virtual System.nfloat Scale { set; }
	public virtual SKScene Scene { get; }
	public virtual System.nfloat Speed { get; set; }
	public virtual Foundation.NSMutableDictionary UserData { get; set; }
	public virtual bool UserInteractionEnabled { get; set; }
	public virtual System.nfloat XScale { get; set; }
	public virtual System.nfloat YScale { get; set; }
	public virtual System.nfloat ZPosition { get; set; }
	public virtual System.nfloat ZRotation { get; set; }
	// methods
	public void Add (SKNode node);
	public virtual void AddChild (SKNode node);
	public void AddNodes (SKNode[] nodes);
	public virtual CoreGraphics.CGRect CalculateAccumulatedFrame ();
	public virtual bool ContainsPoint (CoreGraphics.CGPoint point);
	public virtual CoreGraphics.CGPoint ConvertPointFromNode (CoreGraphics.CGPoint point, SKNode sourceNode);
	public virtual CoreGraphics.CGPoint ConvertPointToNode (CoreGraphics.CGPoint point, SKNode sourceNode);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKNode Create ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void EnumerateChildNodes (string name, SKNodeChildEnumeratorHandler enumerationHandler);
	public static SKNode FromFile (string file);
	public virtual SKAction GetActionForKey (string key);
	public virtual SKNode GetChildNode (string name);
	public virtual System.Collections.Generic.IEnumerator<SKNode> GetEnumerator ();
	public virtual SKNode GetNodeAtPoint (CoreGraphics.CGPoint point);
	public virtual SKNode[] GetNodesAtPoint (CoreGraphics.CGPoint point);
	public virtual SKNode GetObjectsMatching (string nameExpression);
	public virtual bool InParentHierarchy (SKNode node);
	public virtual void InsertChild (SKNode node, System.nint index);
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

### New Type SpriteKit.SKNodeChildEnumeratorHandler

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

### New Type SpriteKit.SKNodeEvent_NSEvent

```
public static class SKNodeEvent_NSEvent {
	// methods
	public static CoreGraphics.CGPoint LocationInNode (AppKit.NSEvent This, SKNode node);
}
```

### New Type SpriteKit.SKPhysicsBody

```
public class SKPhysicsBody : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsBody (Foundation.NSCoder coder);
	public SKPhysicsBody (Foundation.NSObjectFlag t);
	public SKPhysicsBody (System.IntPtr handle);
	// properties
	public virtual bool AffectedByGravity { get; set; }
	public virtual SKPhysicsBody[] AllContactedBodies { get; }
	public virtual bool AllowsRotation { get; set; }
	public virtual System.nfloat AngularDamping { get; set; }
	public virtual System.nfloat AngularVelocity { get; set; }
	public virtual System.nfloat Area { get; }
	public virtual uint CategoryBitMask { get; set; }
	public virtual System.nfloat Charge { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual uint CollisionBitMask { get; set; }
	public virtual uint ContactTestBitMask { get; set; }
	public virtual System.nfloat Density { get; set; }
	public virtual bool Dynamic { get; set; }
	public virtual uint FieldBitMask { get; set; }
	public virtual System.nfloat Friction { get; set; }
	public virtual SKPhysicsJoint[] Joints { get; }
	public virtual System.nfloat LinearDamping { get; set; }
	public virtual System.nfloat Mass { get; set; }
	public virtual SKNode Node { get; }
	public virtual bool Pinned { get; set; }
	public virtual bool Resting { get; set; }
	public virtual System.nfloat Restitution { get; set; }
	public virtual bool UsesPreciseCollisionDetection { get; set; }
	public virtual CoreGraphics.CGVector Velocity { get; set; }
	// methods
	public virtual void ApplyAngularImpulse (System.nfloat impulse);
	public virtual void ApplyForce (CoreGraphics.CGVector force);
	public virtual void ApplyForce (CoreGraphics.CGVector force, CoreGraphics.CGPoint point);
	public virtual void ApplyImpulse (CoreGraphics.CGVector impulse);
	public virtual void ApplyImpulse (CoreGraphics.CGVector impulse, CoreGraphics.CGPoint point);
	public virtual void ApplyTorque (System.nfloat torque);

	[Obsolete ("Use the method FromBodies instead")]
	public static SKPhysicsBody BodyWithBodies (SKPhysicsBody[] bodies);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (System.nfloat radius, CoreGraphics.CGPoint center);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (System.nfloat radius);

	[Obsolete ("Use the CreateEdgeChain method instead")]
	public static SKPhysicsBody BodyWithEdgeChainFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdge method instead")]
	public static SKPhysicsBody BodyWithEdgeFromPoint (CoreGraphics.CGPoint fromPoint, CoreGraphics.CGPoint toPoint);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromRect (CoreGraphics.CGRect rect);

	[Obsolete ("Use the CreateBodyFromPath method instead")]
	public static SKPhysicsBody BodyWithPolygonFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (CoreGraphics.CGSize size);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (CoreGraphics.CGSize size, CoreGraphics.CGPoint center);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKPhysicsBody Create (SKTexture texture, float alphaThreshold, CoreGraphics.CGSize size);
	public static SKPhysicsBody Create (SKTexture texture, CoreGraphics.CGSize size);
	public static SKPhysicsBody CreateBodyFromPath (CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateCircularBody (System.nfloat radius, CoreGraphics.CGPoint center);
	public static SKPhysicsBody CreateCircularBody (System.nfloat radius);
	public static SKPhysicsBody CreateEdge (CoreGraphics.CGPoint fromPoint, CoreGraphics.CGPoint toPoint);
	public static SKPhysicsBody CreateEdgeChain (CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateEdgeLoop (CoreGraphics.CGPath path);
	public static SKPhysicsBody CreateEdgeLoop (CoreGraphics.CGRect rect);
	public static SKPhysicsBody CreateRectangularBody (CoreGraphics.CGSize size, CoreGraphics.CGPoint center);
	public static SKPhysicsBody CreateRectangularBody (CoreGraphics.CGSize size);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SKPhysicsBody FromBodies (SKPhysicsBody[] bodies);
}
```

### New Type SpriteKit.SKPhysicsContact

```
public class SKPhysicsContact : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsContact (Foundation.NSObjectFlag t);
	public SKPhysicsContact (System.IntPtr handle);
	// properties
	public virtual SKPhysicsBody BodyA { get; }
	public virtual SKPhysicsBody BodyB { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat CollisionImpulse { get; }
	public virtual CoreGraphics.CGVector ContactNormal { get; }
	public virtual CoreGraphics.CGPoint ContactPoint { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type SpriteKit.SKPhysicsContactDelegate

```
public class SKPhysicsContactDelegate : Foundation.NSObject, ISKPhysicsContactDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsContactDelegate ();
	public SKPhysicsContactDelegate (Foundation.NSObjectFlag t);
	public SKPhysicsContactDelegate (System.IntPtr handle);
	// methods
	public virtual void DidBeginContact (SKPhysicsContact contact);
	public virtual void DidEndContact (SKPhysicsContact contact);
}
```

### New Type SpriteKit.SKPhysicsContactDelegate_Extensions

```
public static class SKPhysicsContactDelegate_Extensions {
	// methods
	public static void DidBeginContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
	public static void DidEndContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
}
```

### New Type SpriteKit.SKPhysicsJoint

```
public class SKPhysicsJoint : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJoint ();
	public SKPhysicsJoint (Foundation.NSCoder coder);
	public SKPhysicsJoint (Foundation.NSObjectFlag t);
	public SKPhysicsJoint (System.IntPtr handle);
	// properties
	public virtual SKPhysicsBody BodyA { get; set; }
	public virtual SKPhysicsBody BodyB { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGVector ReactionForce { get; }
	public virtual System.nfloat ReactionTorque { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SpriteKit.SKPhysicsJointFixed

```
public class SKPhysicsJointFixed : SpriteKit.SKPhysicsJoint, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointFixed (Foundation.NSCoder coder);
	public SKPhysicsJointFixed (Foundation.NSObjectFlag t);
	public SKPhysicsJointFixed (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SKPhysicsJointFixed Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, CoreGraphics.CGPoint anchor);
}
```

### New Type SpriteKit.SKPhysicsJointLimit

```
public class SKPhysicsJointLimit : SpriteKit.SKPhysicsJoint, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointLimit (Foundation.NSCoder coder);
	public SKPhysicsJointLimit (Foundation.NSObjectFlag t);
	public SKPhysicsJointLimit (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat MaxLength { get; set; }
	// methods
	public static SKPhysicsJointLimit Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, CoreGraphics.CGPoint anchorA, CoreGraphics.CGPoint anchorB);
}
```

### New Type SpriteKit.SKPhysicsJointPin

```
public class SKPhysicsJointPin : SpriteKit.SKPhysicsJoint, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointPin (Foundation.NSCoder coder);
	public SKPhysicsJointPin (Foundation.NSObjectFlag t);
	public SKPhysicsJointPin (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat FrictionTorque { get; set; }
	public virtual System.nfloat LowerAngleLimit { get; set; }
	public virtual System.nfloat RotationSpeed { get; set; }
	public virtual bool ShouldEnableLimits { get; set; }
	public virtual System.nfloat UpperAngleLimit { get; set; }
	// methods
	public static SKPhysicsJointPin Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, CoreGraphics.CGPoint anchor);
}
```

### New Type SpriteKit.SKPhysicsJointSliding

```
public class SKPhysicsJointSliding : SpriteKit.SKPhysicsJoint, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointSliding (Foundation.NSCoder coder);
	public SKPhysicsJointSliding (Foundation.NSObjectFlag t);
	public SKPhysicsJointSliding (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat LowerDistanceLimit { get; set; }
	public virtual bool ShouldEnableLimits { get; set; }
	public virtual System.nfloat UpperDistanceLimit { get; set; }
	// methods
	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, CoreGraphics.CGPoint anchor, CoreGraphics.CGVector axis);
}
```

### New Type SpriteKit.SKPhysicsJointSpring

```
public class SKPhysicsJointSpring : SpriteKit.SKPhysicsJoint, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsJointSpring (Foundation.NSCoder coder);
	public SKPhysicsJointSpring (Foundation.NSObjectFlag t);
	public SKPhysicsJointSpring (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat Damping { get; set; }
	public virtual System.nfloat Frequency { get; set; }
	// methods
	public static SKPhysicsJointSpring Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, CoreGraphics.CGPoint anchorA, CoreGraphics.CGPoint anchorB);
}
```

### New Type SpriteKit.SKPhysicsWorld

```
public class SKPhysicsWorld : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKPhysicsWorld (Foundation.NSCoder coder);
	public SKPhysicsWorld (Foundation.NSObjectFlag t);
	public SKPhysicsWorld (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public SKPhysicsContactDelegate ContactDelegate { get; set; }
	public virtual CoreGraphics.CGVector Gravity { get; set; }
	public virtual System.nfloat Speed { get; set; }
	public virtual Foundation.NSObject WeakContactDelegate { get; set; }
	// events
	public event System.EventHandler DidBeginContact;
	public event System.EventHandler DidEndContact;
	// methods
	public virtual void AddJoint (SKPhysicsJoint joint);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void EnumerateBodies (CoreGraphics.CGPoint point, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (CoreGraphics.CGRect rect, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (CoreGraphics.CGPoint start, CoreGraphics.CGPoint end, SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler enumeratorHandler);
	public virtual SKPhysicsBody GetBody (CoreGraphics.CGPoint rayStart, CoreGraphics.CGPoint rayEnd);
	public virtual SKPhysicsBody GetBody (CoreGraphics.CGRect rect);
	public virtual SKPhysicsBody GetBody (CoreGraphics.CGPoint point);
	public virtual void RemoveAllJoints ();
	public virtual void RemoveJoint (SKPhysicsJoint joint);
	public virtual OpenGL.Vector3 SampleFields (OpenGL.Vector3 position);
}
```

### New Type SpriteKit.SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler

```
public sealed delegate SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SKPhysicsBody body, CoreGraphics.CGPoint point, CoreGraphics.CGVector normal, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (SKPhysicsBody body, CoreGraphics.CGPoint point, CoreGraphics.CGVector normal, out bool stop);
}
```

### New Type SpriteKit.SKPhysicsWorldBodiesEnumeratorHandler

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

### New Type SpriteKit.SKRange

```
public class SKRange : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRange ();
	public SKRange (Foundation.NSCoder coder);
	public SKRange (Foundation.NSObjectFlag t);
	public SKRange (System.IntPtr handle);
	public SKRange (System.nfloat lowerLimit, System.nfloat upperLimier);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat LowerLimit { get; set; }
	public virtual System.nfloat UpperLimit { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKRange Create (System.nfloat lower, System.nfloat upper);
	public static SKRange CreateConstant (System.nfloat value);
	public static SKRange CreateUnlimited ();
	public static SKRange CreateWithLowerLimit (System.nfloat lower);
	public static SKRange CreateWithUpperLimit (System.nfloat upper);
	public static SKRange CreateWithVariance (System.nfloat value, System.nfloat variance);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SpriteKit.SKReachConstraints

```
public class SKReachConstraints : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKReachConstraints ();
	public SKReachConstraints (Foundation.NSCoder coder);
	public SKReachConstraints (Foundation.NSObjectFlag t);
	public SKReachConstraints (System.IntPtr handle);
	public SKReachConstraints (System.nfloat lowerAngleLimit, System.nfloat upperAngleLimit);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nfloat LowerAngleLimit { get; set; }
	public virtual System.nfloat UpperAngleLimit { get; set; }
	// methods
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SpriteKit.SKRegion

```
public class SKRegion : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKRegion ();
	public SKRegion (Foundation.NSCoder coder);
	public SKRegion (Foundation.NSObjectFlag t);
	public SKRegion (System.IntPtr handle);
	public SKRegion (float radius);
	public SKRegion (CoreGraphics.CGSize size);
	public SKRegion (CoreGraphics.CGPath path);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static SKRegion InfiniteRegion { get; }
	public virtual CoreGraphics.CGPath Path { get; }
	// methods
	public virtual bool ContainsPoint (CoreGraphics.CGPoint point);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual SKRegion CreateDifference (SKRegion region);
	public virtual SKRegion CreateIntersection (SKRegion region);
	public virtual SKRegion CreateUnion (SKRegion region);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual SKRegion InverseRegion ();
}
```

### New Type SpriteKit.SKRepeatMode

```
[Serializable]
public enum SKRepeatMode {
	Clamp = 1,
	Loop = 2,
}
```

### New Type SpriteKit.SKScene

```
public class SKScene : SpriteKit.SKEffectNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKScene ();
	public SKScene (Foundation.NSCoder coder);
	public SKScene (Foundation.NSObjectFlag t);
	public SKScene (System.IntPtr handle);
	public SKScene (CoreGraphics.CGSize size);
	// properties
	public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }
	public virtual AppKit.NSColor BackgroundColor { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public SKSceneDelegate Delegate { get; set; }
	public virtual SKPhysicsWorld PhysicsWorld { get; }
	public virtual SKSceneScaleMode ScaleMode { get; set; }
	public virtual CoreGraphics.CGSize Size { get; set; }
	public virtual SKView View { get; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual CoreGraphics.CGPoint ConvertPointFromView (CoreGraphics.CGPoint point);
	public virtual CoreGraphics.CGPoint ConvertPointToView (CoreGraphics.CGPoint point);
	public virtual void DidApplyConstraints ();
	public virtual void DidChangeSize (CoreGraphics.CGSize oldSize);
	public virtual void DidEvaluateActions ();
	public virtual void DidFinishUpdate ();
	public virtual void DidMoveToView (SKView view);
	public virtual void DidSimulatePhysics ();
	protected override void Dispose (bool disposing);
	public static SKScene FromSize (CoreGraphics.CGSize size);
	public virtual void Update (double currentTime);
	public virtual void WillMoveFromView (SKView view);
}
```

### New Type SpriteKit.SKSceneDelegate

```
public class SKSceneDelegate : Foundation.NSObject, ISKSceneDelegate, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKSceneDelegate ();
	public SKSceneDelegate (Foundation.NSObjectFlag t);
	public SKSceneDelegate (System.IntPtr handle);
	// methods
	public virtual void DidApplyConstraints (SKScene scene);
	public virtual void DidEvaluateActions (SKScene scene);
	public virtual void DidFinishUpdate (SKScene scene);
	public virtual void DidSimulatePhysics (SKScene scene);
	public virtual void Update (double currentTime, SKScene scene);
}
```

### New Type SpriteKit.SKSceneDelegate_Extensions

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

### New Type SpriteKit.SKSceneScaleMode

```
[Serializable]
public enum SKSceneScaleMode {
	AspectFill = 1,
	AspectFit = 2,
	Fill = 0,
	ResizeFill = 3,
}
```

### New Type SpriteKit.SKShader

```
public class SKShader : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKShader ();
	public SKShader (Foundation.NSCoder coder);
	public SKShader (Foundation.NSObjectFlag t);
	public SKShader (System.IntPtr handle);
	public SKShader (string shaderSourceCode);
	public SKShader (string sharedSourceCode, SKUniform[] uniforms);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Source { get; set; }
	public virtual SKUniform[] Uniforms { get; set; }
	// methods
	public virtual void AddUniform (SKUniform uniform);
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public static SKShader Create ();
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SKShader FromFile (string name);
	public static SKShader FromShaderSourceCode (string source);
	public static SKShader FromShaderSourceCode (string source, SKUniform[] uniforms);
	public virtual SKUniform GetUniform (string uniformName);
	public virtual void RemoveUniform (string uniforName);
}
```

### New Type SpriteKit.SKShapeNode

```
public class SKShapeNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKShapeNode ();
	public SKShapeNode (Foundation.NSCoder coder);
	public SKShapeNode (Foundation.NSObjectFlag t);
	public SKShapeNode (System.IntPtr handle);
	// properties
	public virtual bool Antialiased { get; set; }
	public virtual SKBlendMode BlendMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AppKit.NSColor FillColor { get; set; }
	public virtual SKShader FillShader { get; set; }
	public virtual SKTexture FillTexture { get; set; }
	public virtual System.nfloat GlowWidth { get; set; }
	public virtual CoreGraphics.CGLineCap LineCap { get; set; }
	public virtual CoreGraphics.CGLineJoin LineJoin { get; set; }
	public virtual System.nfloat LineLength { get; }
	public virtual System.nfloat LineWidth { get; set; }
	public virtual System.nfloat MiterLimit { get; set; }
	public virtual CoreGraphics.CGPath Path { get; set; }
	public virtual AppKit.NSColor StrokeColor { get; set; }
	public virtual SKShader StrokeShader { get; set; }
	public virtual SKTexture StrokeTexture { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static SKShapeNode FromCircle (System.nfloat radius);
	public static SKShapeNode FromEllipse (CoreGraphics.CGSize size);
	public static SKShapeNode FromEllipse (CoreGraphics.CGRect rect);
	public static SKShapeNode FromPath (CoreGraphics.CGPath path);
	public static SKShapeNode FromPath (CoreGraphics.CGPath path, bool centered);
	public static SKShapeNode FromPoints (ref CoreGraphics.CGPoint points, System.nuint numPoints);
	public static SKShapeNode FromRect (CoreGraphics.CGSize size);
	public static SKShapeNode FromRect (CoreGraphics.CGRect rect, System.nfloat cornerRadius);
	public static SKShapeNode FromRect (CoreGraphics.CGSize size, System.nfloat cornerRadius);
	public static SKShapeNode FromRect (CoreGraphics.CGRect rect);
	public static SKShapeNode FromSplinePoints (ref CoreGraphics.CGPoint points, System.nuint numPoints);
}
```

### New Type SpriteKit.SKSpriteNode

```
public class SKSpriteNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKSpriteNode ();
	public SKSpriteNode (string name);
	public SKSpriteNode (SKTexture texture);
	public SKSpriteNode (SKTexture texture, AppKit.NSColor color, CoreGraphics.CGSize size);
	public SKSpriteNode (System.IntPtr handle);
	public SKSpriteNode (Foundation.NSObjectFlag t);
	public SKSpriteNode (Foundation.NSCoder coder);
	public SKSpriteNode (AppKit.NSColor color, CoreGraphics.CGSize size);
	// properties
	public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }
	public virtual SKBlendMode BlendMode { get; set; }
	public virtual CoreGraphics.CGRect CenterRect { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AppKit.NSColor Color { get; set; }
	public virtual System.nfloat ColorBlendFactor { get; set; }
	public virtual uint LightingBitMask { get; set; }
	public virtual SKTexture NormalTexture { get; set; }
	public virtual SKShader Shader { get; set; }
	public virtual uint ShadowCastBitMask { get; set; }
	public virtual uint ShadowedBitMask { get; set; }
	public virtual CoreGraphics.CGSize Size { get; set; }
	public virtual SKTexture Texture { get; set; }
	// methods
	public static SKSpriteNode Create (SKTexture texture, SKTexture normalMap);
	public static SKSpriteNode Create (string imageName, bool generateNormalMap);
	protected override void Dispose (bool disposing);
	public static SKSpriteNode FromColor (AppKit.NSColor color, CoreGraphics.CGSize size);
	public static SKSpriteNode FromImageNamed (string name);
	public static SKSpriteNode FromTexture (SKTexture texture, CoreGraphics.CGSize size);
	public static SKSpriteNode FromTexture (SKTexture texture);
}
```

### New Type SpriteKit.SKTexture

```
public class SKTexture : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTexture (Foundation.NSCoder coder);
	public SKTexture (Foundation.NSObjectFlag t);
	public SKTexture (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SKTextureFilteringMode FilteringMode { get; set; }
	public virtual CoreGraphics.CGSize Size { get; }
	public virtual CoreGraphics.CGRect TextureRect { get; }
	public virtual bool UsesMipmaps { get; set; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	public virtual SKTexture CreateTextureByGeneratingNormalMap ();
	public virtual SKTexture CreateTextureByGeneratingNormalMap (System.nfloat smoothness, System.nfloat contrast);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SKTexture FromData (Foundation.NSData pixelData, CoreGraphics.CGSize size);
	public static SKTexture FromData (Foundation.NSData pixelData, CoreGraphics.CGSize size, uint rowLength, uint alignment);
	public static SKTexture FromData (Foundation.NSData pixelData, CoreGraphics.CGSize size, bool flipped);
	public static SKTexture FromImage (AppKit.NSImage image);
	public static SKTexture FromImage (CoreGraphics.CGImage image);
	public static SKTexture FromImageNamed (string name);
	public static SKTexture FromRectangle (CoreGraphics.CGRect rect, SKTexture texture);
	public static SKTexture FromTextureNoise (System.nfloat smoothness, CoreGraphics.CGSize size, bool grayscale);
	public static SKTexture FromTextureVectorNoise (System.nfloat smoothness, CoreGraphics.CGSize size);
	public virtual void Preload (System.Action completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public static void PreloadTextures (SKTexture[] textures, System.Action completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
	public virtual SKTexture TextureByApplyingCIFilter (CoreImage.CIFilter filter);
}
```

### New Type SpriteKit.SKTextureAtlas

```
public class SKTextureAtlas : Foundation.NSObject, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTextureAtlas ();
	public SKTextureAtlas (Foundation.NSCoder coder);
	public SKTextureAtlas (Foundation.NSObjectFlag t);
	public SKTextureAtlas (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string[] TextureNames { get; }
	// methods
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public static SKTextureAtlas FromDictionary (Foundation.NSDictionary properties);
	public static SKTextureAtlas FromName (string name);
	public virtual void Preload (System.Action completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public static void PreloadTextures (SKTextureAtlas[] textures, System.Action completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTextureAtlas[] textures);
	public virtual SKTexture TextureNamed (string name);
}
```

### New Type SpriteKit.SKTextureFilteringMode

```
[Serializable]
public enum SKTextureFilteringMode {
	Linear = 1,
	Nearest = 0,
}
```

### New Type SpriteKit.SKTextureModify

```
public sealed delegate SKTextureModify : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SKTextureModify (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr pixelData, System.nuint lengthInBytes, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr pixelData, System.nuint lengthInBytes);
}
```

### New Type SpriteKit.SKTransition

```
public class SKTransition : Foundation.NSObject, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKTransition (Foundation.NSObjectFlag t);
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
	public static SKTransition FadeWithColor (AppKit.NSColor color, double sec);
	public static SKTransition FadeWithDuration (double sec);
	public static SKTransition FlipHorizontalWithDuration (double sec);
	public static SKTransition FlipVerticalWithDuration (double sec);
	public static SKTransition MoveInWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition PushWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition RevealWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition TransitionWithCIFilter (CoreImage.CIFilter filter, double sec);
}
```

### New Type SpriteKit.SKTransitionDirection

```
[Serializable]
public enum SKTransitionDirection {
	Down = 1,
	Left = 3,
	Right = 2,
	Up = 0,
}
```

### New Type SpriteKit.SKUniform

```
public class SKUniform : Foundation.NSObject, Foundation.INSCoding, Foundation.INSCopying, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKUniform ();
	public SKUniform (string name, OpenGL.Matrix3d value);
	public SKUniform (string name, OpenGL.Matrix2 value);
	public SKUniform (string name, OpenGL.Vector4 value);
	public SKUniform (string name, OpenGL.Vector3 value);
	public SKUniform (string name, OpenGL.Vector2 value);
	public SKUniform (string name, float value);
	public SKUniform (string name, SKTexture texture);
	public SKUniform (string name);
	public SKUniform (System.IntPtr handle);
	public SKUniform (Foundation.NSObjectFlag t);
	public SKUniform (Foundation.NSCoder coder);
	public SKUniform (string name, OpenGL.Matrix4 value);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual OpenGL.Matrix2 FloatMatrix2Value { get; set; }
	public virtual OpenGL.Matrix3d FloatMatrix3Value { get; set; }
	public virtual OpenGL.Matrix4 FloatMatrix4Value { get; set; }
	public virtual float FloatValue { get; set; }
	public virtual OpenGL.Vector2 FloatVector2Value { get; set; }
	public virtual OpenGL.Vector3 FloatVector3Value { get; set; }
	public virtual OpenGL.Vector4 FloatVector4Value { get; set; }
	public virtual string Name { get; }
	public virtual SKTexture TextureValue { get; set; }
	public virtual SKUniformType UniformType { get; }
	// methods
	public virtual Foundation.NSObject Copy (Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
}
```

### New Type SpriteKit.SKUniformType

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

### New Type SpriteKit.SKVideoNode

```
public class SKVideoNode : SpriteKit.SKNode, Foundation.INSCoding, Foundation.INSCopying, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<SKNode>, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKVideoNode ();
	public SKVideoNode (Foundation.NSCoder coder);
	public SKVideoNode (Foundation.NSObjectFlag t);
	public SKVideoNode (System.IntPtr handle);
	public SKVideoNode (AVFoundation.AVPlayer player);
	public SKVideoNode (string videoFile);
	public SKVideoNode (Foundation.NSUrl url);
	// properties
	public virtual CoreGraphics.CGPoint AnchorPoint { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual CoreGraphics.CGSize Size { get; set; }
	// methods
	public static SKVideoNode FromFile (string videoFile);
	public static SKVideoNode FromPlayer (AVFoundation.AVPlayer player);
	public static SKVideoNode FromUrl (Foundation.NSUrl videoURL);
	public virtual void Pause ();
	public virtual void Play ();
}
```

### New Type SpriteKit.SKView

```
public class SKView : AppKit.NSView, Foundation.INSCoding, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKView ();
	public SKView (Foundation.NSCoder coder);
	public SKView (Foundation.NSObjectFlag t);
	public SKView (System.IntPtr handle);
	// properties
	public virtual bool AllowsTransparency { get; set; }
	public virtual bool Asynchronous { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual System.nint FrameInterval { get; set; }
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
	public virtual CoreGraphics.CGPoint ConvertPointFromScene (CoreGraphics.CGPoint point, SKScene scene);
	public virtual CoreGraphics.CGPoint ConvertPointToScene (CoreGraphics.CGPoint point, SKScene scene);
	protected override void Dispose (bool disposing);
	public virtual void PresentScene (SKScene scene);
	public virtual void PresentScene (SKScene scene, SKTransition transition);
	public virtual SKTexture TextureFromNode (SKNode node);
	public virtual SKTexture TextureFromNode (SKNode node, CoreGraphics.CGRect crop);
}
```

## New Namespace VideoToolbox

### New Type VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static Foundation.NSString AllowFrameReordering { get; }
	public static Foundation.NSString AllowTemporalCompression { get; }
	public static Foundation.NSString AverageBitRate { get; }
	public static Foundation.NSString DataRateLimits { get; }
	public static Foundation.NSString H264EntropyMode { get; }
	public static Foundation.NSString MaxKeyFrameInterval { get; }
	public static Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static Foundation.NSString MoreFramesAfterEnd { get; }
	public static Foundation.NSString MoreFramesBeforeStart { get; }
	public static Foundation.NSString NumberOfPendingFrames { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString ProfileLevel { get; }
	public static Foundation.NSString Quality { get; }
	public static Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
}
```

### New Type VideoToolbox.VTCompressionPropertyKey_

```
public static class VTCompressionPropertyKey_ {
	// properties
	public static Foundation.NSString AspectRatio16x9 { get; }
	public static Foundation.NSString CABAC { get; }
	public static Foundation.NSString CAVLC { get; }
	public static Foundation.NSString CleanAperture { get; }
	public static Foundation.NSString ColorPrimaries { get; }
	public static Foundation.NSString Depth { get; }
	public static Foundation.NSString ExpectedDuration { get; }
	public static Foundation.NSString ExpectedFrameRate { get; }
	public static Foundation.NSString FieldCount { get; }
	public static Foundation.NSString FieldDetail { get; }
	public static Foundation.NSString ICCProfile { get; }
	public static Foundation.NSString MaxFrameDelayCount { get; }
	public static Foundation.NSString MaxH264SliceBytes { get; }
	public static Foundation.NSString MultiPassStorage { get; }
	public static Foundation.NSString PixelAspectRatio { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString ProgressiveScan { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString SourceFrameCount { get; }
	public static Foundation.NSString TransferFunction { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type VideoToolbox.VTDecodeFrameFlags

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

### New Type VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static Foundation.NSString ContentHasInterframeDependencies { get; }
	public static Foundation.NSString DeinterlaceMode { get; }
	public static Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static Foundation.NSString FieldMode { get; }
	public static Foundation.NSString FieldMode_BothFields { get; }
	public static Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static Foundation.NSString FieldMode_SingleField { get; }
	public static Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static Foundation.NSString Height { get; }
	public static Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static Foundation.NSString OnlyTheseFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static Foundation.NSString PixelBufferPool { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString ReducedCoefficientDecode { get; }
	public static Foundation.NSString ReducedFrameDelivery { get; }
	public static Foundation.NSString ReducedResolutionDecode { get; }
	public static Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
	public static Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static Foundation.NSString ThreadCount { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
	public static Foundation.NSString Width { get; }
}
```

### New Type VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type VideoToolbox.VTMultiPassStorageCreationOption

```
public static class VTMultiPassStorageCreationOption {
	// properties
	public static Foundation.NSString DoNotDelete { get; }
}
```

### New Type VideoToolbox.VTProfileLevel

```
public static class VTProfileLevel {
	// properties
	public static Foundation.NSString H263_Profile0_Level10 { get; }
	public static Foundation.NSString H263_Profile0_Level45 { get; }
	public static Foundation.NSString H263_Profile3_Level45 { get; }
	public static Foundation.NSString H264_Baseline_1_3 { get; }
	public static Foundation.NSString H264_Baseline_3_0 { get; }
	public static Foundation.NSString H264_Baseline_3_1 { get; }
	public static Foundation.NSString H264_Baseline_3_2 { get; }
	public static Foundation.NSString H264_Baseline_4_0 { get; }
	public static Foundation.NSString H264_Baseline_4_1 { get; }
	public static Foundation.NSString H264_Baseline_4_2 { get; }
	public static Foundation.NSString H264_Baseline_5_0 { get; }
	public static Foundation.NSString H264_Baseline_5_1 { get; }
	public static Foundation.NSString H264_Baseline_5_2 { get; }
	public static Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static Foundation.NSString H264_Extended_5_0 { get; }
	public static Foundation.NSString H264_Extended_AutoLevel { get; }
	public static Foundation.NSString H264_High_3_0 { get; }
	public static Foundation.NSString H264_High_3_1 { get; }
	public static Foundation.NSString H264_High_3_2 { get; }
	public static Foundation.NSString H264_High_4_0 { get; }
	public static Foundation.NSString H264_High_4_1 { get; }
	public static Foundation.NSString H264_High_4_2 { get; }
	public static Foundation.NSString H264_High_5_0 { get; }
	public static Foundation.NSString H264_High_5_1 { get; }
	public static Foundation.NSString H264_High_5_2 { get; }
	public static Foundation.NSString H264_High_AutoLevel { get; }
	public static Foundation.NSString H264_Main_3_0 { get; }
	public static Foundation.NSString H264_Main_3_1 { get; }
	public static Foundation.NSString H264_Main_3_2 { get; }
	public static Foundation.NSString H264_Main_4_0 { get; }
	public static Foundation.NSString H264_Main_4_1 { get; }
	public static Foundation.NSString H264_Main_4_2 { get; }
	public static Foundation.NSString H264_Main_5_0 { get; }
	public static Foundation.NSString H264_Main_5_1 { get; }
	public static Foundation.NSString H264_Main_5_2 { get; }
	public static Foundation.NSString H264_Main_AutoLevel { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static Foundation.NSString MP4V_Main_L2 { get; }
	public static Foundation.NSString MP4V_Main_L3 { get; }
	public static Foundation.NSString MP4V_Main_L4 { get; }
	public static Foundation.NSString MP4V_Simple_L0 { get; }
	public static Foundation.NSString MP4V_Simple_L1 { get; }
	public static Foundation.NSString MP4V_Simple_L2 { get; }
	public static Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type VideoToolbox.VTProperty

```
public static class VTProperty {
	// properties
	public static Foundation.NSString DocumentationKey { get; }
	public static Foundation.NSString ReadWriteStatus { get; }
	public static Foundation.NSString ShouldBeSerialized { get; }
	public static Foundation.NSString SupportedValueListKey { get; }
	public static Foundation.NSString SupportedValueMaximumKey { get; }
	public static Foundation.NSString SupportedValueMinimumKey { get; }
	public static Foundation.NSString Type { get; }
}
```

### New Type VideoToolbox.VTPropertyReadWriteStatus

```
public static class VTPropertyReadWriteStatus {
	// properties
	public static Foundation.NSString ReadOnly { get; }
	public static Foundation.NSString ReadWrite { get; }
}
```

### New Type VideoToolbox.VTPropertyType

```
public static class VTPropertyType {
	// properties
	public static Foundation.NSString Boolean { get; }
	public static Foundation.NSString Enumeration { get; }
	public static Foundation.NSString Number { get; }
}
```

### New Type VideoToolbox.VTStatus

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

### New Type VideoToolbox.VTVideoEncoderList

```
public static class VTVideoEncoderList {
	// properties
	public static Foundation.NSString CodecName { get; }
	public static Foundation.NSString CodecType { get; }
	public static Foundation.NSString DisplayName { get; }
	public static Foundation.NSString EncoderID { get; }
	public static Foundation.NSString EncoderName { get; }
}
```

### New Type VideoToolbox.VTVideoEncoderSpecification

```
public static class VTVideoEncoderSpecification {
	// properties
	public static Foundation.NSString EnableHardwareAcceleratedVideoEncoder { get; }
	public static Foundation.NSString RequireHardwareAcceleratedVideoEncoder { get; }
}
```
