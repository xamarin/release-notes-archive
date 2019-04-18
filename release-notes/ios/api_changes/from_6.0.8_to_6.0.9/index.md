---
id: (GUID)
title: "From 6.0.8 to 6.0.9"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


## Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


### Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "6.0.8";
```

Added:

```
public const string Version = "6.0.9";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


### Namespace: MonoTouch.AVFoundation

We had previously used [Obsolete] to point developers to better strongly-typed versions of the APIs. &nbsp; We have dropped that, and instead are now using a milder "Advice" attribute that will be integrated into future versions of the IDE, since the APIs were not really obsolete, they were just not as good.

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetTrack" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Added:

```
public MonoTouch.CoreMedia.CMFormatDescription[] FormatDescriptions {
 		get;
 	}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioMixInputParameter" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVAudioMixInputParameter

Removed:

```
public virtual bool GetVolumeRamp (MonoTouch.CoreMedia.CMTime forTime, float startVolume, float endVolume, MonoTouch.CoreMedia.CMTimeRange timeRange);
```

Added:

```
public virtual bool GetVolumeRamp (MonoTouch.CoreMedia.CMTime forTime, ref float startVolume, ref float endVolume, ref MonoTouch.CoreMedia.CMTimeRange timeRange);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableComposition" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVMutableComposition

Added:

```
[Obsolete("Deprecated in iOS 5.0 and OS X 10.8")]
	public override System.Drawing.SizeF NaturalSize {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableMetadataItem" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVMutableMetadataItem

Added:

```
set;
 		set;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableTimedMetadataGroup" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVMutableTimedMetadataGroup

Removed:

```
public virtual AVMetadataItem[] Items {
 	public virtual MonoTouch.CoreMedia.CMTimeRange Timerange {
```

Added:

```
public override AVMetadataItem[] Items {
 	public override MonoTouch.CoreMedia.CMTimeRange TimeRange {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVTimedMetadataGroup" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVTimedMetadataGroup

Added:

```
set;
 		set;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideoCompositionLayerInstruct" class="injected"></a>


### Type Changed: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruct

Removed:

```
public virtual bool GetOpacityRamp (MonoTouch.CoreMedia.CMTime time, float startOpacity, float endOpacity, MonoTouch.CoreMedia.CMTimeRange timeRange);
 	public virtual bool GetTransformRamp (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreGraphics.CGAffineTransform startTransform, MonoTouch.CoreGraphics.CGAffineTransform endTransform, MonoTouch.CoreMedia.CMTimeRange timeRange);
```

Added:

```
public virtual bool GetOpacityRamp (MonoTouch.CoreMedia.CMTime time, ref float startOpacity, ref float endOpacity, ref MonoTouch.CoreMedia.CMTimeRange timeRange);
 	public virtual bool GetTransformRamp (MonoTouch.CoreMedia.CMTime time, ref MonoTouch.CoreGraphics.CGAffineTransform startTransform, ref MonoTouch.CoreGraphics.CGAffineTransform endTransform, ref MonoTouch.CoreMedia.CMTimeRange timeRange);
```

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


## Namespace: MonoTouch.AddressBook

 <a name="Type_Changed:_MonoTouch.AddressBook.ABAddressBook" class="injected"></a>


### Type Changed: MonoTouch.AddressBook.ABAddressBook

Removed:

```
[Obsolete("Use static Create method in iOS 6.0")]
	public ABAddressBook ();
```

Added:

```
[Obsolete("Deprecated in iOS 6.0. Use static Create method instead")]
	public ABAddressBook ();
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPerson" class="injected"></a>


### Type Changed: MonoTouch.AddressBook.ABPerson

Removed:

```
[Obsolete("Use GetAllAddresses")]
	public ABMultiValue`1 GetAddresses ();
 	[Obsolete("Use GetInstantMessageServices")]
	public ABMultiValue`1 GetInstantMessages ();
 	[Obsolete("Use GetSocialProfiles")]
	public ABMultiValue`1 GetSocialProfile ();
```

Added:

```
public ABMultiValue`1 GetAddresses ();
 	public ABMultiValue`1 GetInstantMessages ();
 	public ABMultiValue`1 GetSocialProfile ();
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABSource" class="injected"></a>


### Type Changed: MonoTouch.AddressBook.ABSource

Removed:

```
[Obsolete("Use ABSourceType.SearchableMask")]
	public const int SearchableMask = 16777216;
```

Added:

```
public const int SearchableMask = 16777216;
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


## Namespace: MonoTouch.AudioToolbox

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioBalanceFade" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioBalanceFade

```
public class AudioBalanceFade {
	
	public AudioBalanceFade (AudioChannelLayout channelLayout);
	
	public float [] GetBalanceFade ();
	
	public float BackFrontFade {
		get;
		set;
	}
	public AudioChannelLayout ChannelLayout {
		get;
	}
	public float LeftRightBalance {
		get;
		set;
	}
	public AudioBalanceFadeType Type {
		get;
		set;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioBalanceFadeType" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioBalanceFadeType

```
[Serializable]
public enum AudioBalanceFadeType {
	MaxUnityGain,
	EqualPower
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioBufferList" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioBufferList

Use "AudioBuffers" instead, which can cope with more scenarios.

Added:

```
[Obsolete]
public class AudioBufferList {
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioBuffers" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioBuffers

```
public class AudioBuffers : IDisposable {
	
	public AudioBuffers (IntPtr address);
	public AudioBuffers (IntPtr address, bool owns);
	public AudioBuffers (int count);
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public void SetData (int index, IntPtr data);
	public void SetData (int index, IntPtr data, int dataByteSize);
	
	public static explicit operator IntPtr (AudioBuffers audioBuffers);
	
	public int Count {
		get;
	}
	public AudioBuffer this [int index] {
		get;
		set;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioChannelBit" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioChannelBit

```
[Serializable]
[Flags]
public enum AudioChannelBit {
	Left,
	Right,
	Center,
	LFEScreen,
	LeftSurround,
	RightSurround,
	LeftCenter,
	RightCenter,
	CenterSurround,
	LeftSurroundDirect,
	RightSurroundDirect,
	TopCenterSurround,
	VerticalHeightLeft,
	VerticalHeightCenter,
	VerticalHeightRight,
	TopBackLeft,
	TopBackCenter,
	TopBackRight
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioChannelDescription" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioChannelDescription

Removed:

```
public class AudioChannelDescription {
 	
 	public AudioChannelDescription ();
```

Added:

```
public struct AudioChannelDescription {
 	public string Name {
 		get;
 	}
 	public string ShortName {
 		get;
 	}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioChannelLayout" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioChannelLayout

Added:

```
public static AudioChannelLayout FromAudioChannelBitmap (AudioChannelBit channelBitmap);
 	public static AudioChannelLayout FromAudioChannelLayoutTag (AudioChannelLayoutTag channelLayoutTag);
 	public static int [] GetChannelMap (AudioChannelLayout inputLayout, AudioChannelLayout outputLayout);
 	public static float [] GetMatrixMixMap (AudioChannelLayout inputLayout, AudioChannelLayout outputLayout);
 	public static Nullable<int> GetNumberOfChannels (AudioChannelLayout layout);
 	public static Nullable<AudioChannelLayoutTag> GetTagForChannelLayout (AudioChannelLayout layout);
 	public static AudioChannelLayoutTag[] GetTagsForNumberOfChannels (int count);
 	public static AudioFormatError Validate (AudioChannelLayout layout);
 	public string Name {
 		get;
 	}
 	public string SimpleName {
 		get;
 	}
 	public AudioChannelBit ChannelUsage;
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioChannelLayoutTagExtensions" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioChannelLayoutTagExtensions

```
public static class AudioChannelLayoutTagExtensions {
	
	public static Nullable<audiochannelbit> ToAudioChannel (AudioChannelLayoutTag layoutTag);
}
</audiochannelbit>
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFile" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioFile

Added:

```
public AudioFileChunkType[] ChunkIDs {
 		get;
 	}
 	public Nullable<AudioStreamBasicDescription> DataFormat {
 		get;
 	}
 	public byte [] ID3Tag {
 		get;
 	}
 	public AudioFileInfoDictionary InfoDictionary {
 		get;
 	}
 	public AudioFileMarkerList MarkerList {
 		get;
 	}
 	public Nullable<AudioFilePacketTableInfo> PacketTableInfo {
 		get;
 	}
 	public AudioFileRegionList RegionList {
 		get;
 	}
 	public double ReserveDuration {
 		get;
 	}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileChunkType" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileChunkType

```
[Serializable]
public enum AudioFileChunkType : uint {
	CAFStreamDescription,
	CAFAudioData,
	CAFChannelLayout,
	CAFFiller,
	CAFMarker,
	CAFRegion,
	CAFInstrument,
	CAFMagicCookieID,
	CAFInfoStrings,
	CAFEditComments,
	CAFPacketTable,
	CAFStrings,
	CAFUUID,
	CAFPeak,
	CAFOverview,
	CAFMIDI,
	CAFUMID,
	CAFFormatListID,
	CAFiXML
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileGlobalInfo" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileGlobalInfo

```
public static class AudioFileGlobalInfo {
	
	public static AudioFormatType[] GetAvailableFormats (AudioFileType fileType);
	public static AudioStreamBasicDescription[] GetAvailableStreamDescriptions (AudioFileType fileType, AudioFormatType formatType);
	public static string [] GetExtensions (AudioFileType fileType);
	public static string GetFileTypeName (AudioFileType fileType);
	public static string [] GetMIMETypes (AudioFileType fileType);
	public static string [] GetUTIs (AudioFileType fileType);
	
	public static string [] AllExtensions {
		get;
	}
	public static string [] AllMIMETypes {
		get;
	}
	public static string [] AllUTIs {
		get;
	}
	public static AudioFileType[] ReadableTypes {
		get;
	}
	public static AudioFileType[] WritableTypes {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileInfoDictionary" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileInfoDictionary

```
public class AudioFileInfoDictionary : MonoTouch.Foundation.DictionaryContainer {
	
	public string Album {
		get;
	}
	public string ApproximateDurationInSeconds {
		get;
	}
	public string Artist {
		get;
	}
	public string ChannelLayout {
		get;
	}
	public string Comments {
		get;
	}
	public string Composer {
		get;
	}
	public string Copyright {
		get;
	}
	public string EncodingApplication {
		get;
	}
	public string Genre {
		get;
	}
	public string ISRC {
		get;
	}
	public string KeySignature {
		get;
	}
	public string Lyricist {
		get;
	}
	public string NominalBitRate {
		get;
	}
	public string RecordedDate {
		get;
	}
	public string SourceBitDepth {
		get;
	}
	public string SourceEncoder {
		get;
	}
	public string SubTitle {
		get;
	}
	public string Tempo {
		get;
	}
	public string TimeSignature {
		get;
	}
	public string Title {
		get;
	}
	public string TrackNumber {
		get;
	}
	public string Year {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileMarker" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileMarker

```
public struct AudioFileMarker {
	
	public string Name {
		get;
	}
	
	public double FramePosition;
	public int MarkerID;
	public AudioFileSmpteTime SmpteTime;
	public AudioFileMarkerType Type;
	public ushort Reserved;
	public ushort Channel;
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileMarkerList" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileMarkerList

```
public class AudioFileMarkerList : IDisposable {
	
	public AudioFileMarkerList (IntPtr ptr, bool owns);
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	
	public uint Count {
		get;
	}
	public AudioFileMarker this [int index] {
		get;
	}
	public SmpteTimeType SmpteTimeType {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileMarkerType" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileMarkerType

```
[Serializable]
public enum AudioFileMarkerType : uint {
	Generic,
	CAFProgramStart,
	CAFProgramEnd,
	CAFTrackStart,
	CAFTrackEnd,
	CAFIndex,
	CAFRegionStart,
	CAFRegionEnd,
	CAFRegionSyncPoint,
	CAFSelectionStart,
	CAFSelectionEnd,
	CAFEditSourceBegin,
	CAFEditSourceEnd,
	CAFEditDestinationBegin,
	CAFEditDestinationEnd,
	CAFSustainLoopStart,
	CAFSustainLoopEnd,
	CAFReleaseLoopStart,
	CAFReleaseLoopEnd,
	CAFSavedPlayPosition,
	CAFTempo,
	CAFTimeSignature,
	CAFKeySignature
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFilePacketTableInfo" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFilePacketTableInfo

```
public struct AudioFilePacketTableInfo {
	
	public long ValidFrames;
	public int PrimingFrames;
	public int RemainderFrames;
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileRegion" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileRegion

```
public struct AudioFileRegion {
	
	public AudioFileRegion (IntPtr ptr);
	
	public int Count {
		get;
	}
	public AudioFileRegionFlags Flags {
		get;
	}
	public AudioFileMarker this [int index] {
		get;
	}
	public string Name {
		get;
	}
	public uint RegionID {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileRegionFlags" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileRegionFlags

```
[Serializable]
[Flags]
public enum AudioFileRegionFlags : uint {
	LoopEnable,
	PlayForward,
	PlayBackward
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileRegionList" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileRegionList

```
public class AudioFileRegionList : IDisposable {
	
	public AudioFileRegionList (IntPtr ptr, bool owns);
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	
	public uint Count {
		get;
	}
	public AudioFileRegion this [int index] {
		get;
	}
	public SmpteTimeType SmpteTimeType {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFileSmpteTime" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFileSmpteTime

```
public struct AudioFileSmpteTime {
	
	public sbyte Hours;
	public byte Minutes;
	public byte Seconds;
	public byte Frames;
	public uint SubFrameSampleOffset;
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFileStream" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioFileStream

Added:

```
public AudioStreamBasicDescription DataFormat {
 		get;
 	}
 	public AudioFormat[] FormatList {
 		get;
 	}
 	public Nullable<AudioFilePacketTableInfo> PacketTableInfo {
 		get;
 	}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFileType" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioFileType

Added:

```
M4B,
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormat" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioFormat

Added:

```
public static Nullable<AudioFormat> GetFirstPlayableFormat (AudioFormat[] formatList);
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFormatError" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioFormatError

```
[Serializable]
public enum AudioFormatError {
	None,
	Unspecified,
	UnsupportedProperty,
	BadPropertySize,
	BadSpecifierSize,
	UnsupportedDataFormat,
	UnknownFormat
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioPanningInfo" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioPanningInfo

```
public class AudioPanningInfo {
	
	public AudioPanningInfo (AudioChannelLayout outputChannelMap);
	
	public float [] GetPanningMatrix ();
	
	public AudioChannelFlags CoordinateFlags {
		get;
		set;
	}
	public float [] Coordinates {
		get;
	}
	public float GainScale {
		get;
		set;
	}
	public AudioChannelLayout OutputChannelMap {
		get;
	}
	public PanningMode PanningMode {
		get;
		set;
	}
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueBuffer" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueueBuffer

Added:

```
public void CopyToAudioData (IntPtr source, int size);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueProcessingTap" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioQueueProcessingTap

Added:

```
public AudioQueueStatus GetSourceAudio (uint numberOfFrames, ref AudioTimeStamp timeStamp, out AudioQueueProcessingTapFlags flags, out uint parentNumberOfFrames, AudioBuffers data);
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueProcessingTapDelegate" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioQueueProcessingTapDelegate

```
[Serializable]
public delegate uint AudioQueueProcessingTapDelegate (AudioQueueProcessingTap audioQueueTap, uint numberOfFrames, ref AudioTimeStamp timeStamp, ref AudioQueueProcessingTapFlags flags, AudioBuffers data);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioStreamBasicDescription" class="injected"></a>


### Type Changed: MonoTouch.AudioToolbox.AudioStreamBasicDescription

Removed:

```
public static AudioStreamBasicDescription CreateLinearPCM (double sampleRate, uint channelsPerFrame, uint bitsPerChannel);
```

Added:

```
public static AudioStreamBasicDescription CreateLinearPCM (double sampleRate, uint channelsPerFrame, uint bitsPerChannel, bool bigEndian);
 	public static AudioChannelLayoutTag[] GetAvailableEncodeChannelLayoutTags (AudioStreamBasicDescription format);
 	public static int [] GetAvailableEncodeNumberChannels (AudioStreamBasicDescription format);
 	public static AudioFormatError GetFormatInfo (ref AudioStreamBasicDescription format);
 	public AudioFormat[] GetFormatList (byte [] magicCookie);
 	public AudioFormat[] GetOutputFormatList (byte [] magicCookie);
 	public string FormatName {
 		get;
 	}
 	public bool IsEncrypted {
 		get;
 	}
 	public bool IsExternallyFramed {
 		get;
 	}
 	public bool IsVariableBitrate {
 		get;
 	}
 	
 	public static readonly AudioFormatFlags AudioFormatFlagsAudioUnitCanonical;
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioValueRange" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.AudioValueRange

```
public struct AudioValueRange {
	
	public double Minimum;
	public double Maximum;
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.PanningMode" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.PanningMode

```
[Serializable]
public enum PanningMode {
	SoundField,
	VectorBasedPanning
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.SmpteTimeType" class="injected"></a>


### New Type: MonoTouch.AudioToolbox.SmpteTimeType

```
[Serializable]
public enum SmpteTimeType {
	None,
	Type24,
	Type25,
	Type30Drop,
	Type30,
	Type2997,
	Type2997Drop,
	Type60,
	Type5994,
	Type60Drop,
	Type5994Drop,
	Type50,
	Type2398
}
```

 <a name="Namespace:_MonoTouch.AudioUnit" class="injected"></a>


## Namespace: MonoTouch.AudioUnit

 <a name="Type_Changed:_MonoTouch.AudioUnit.AUGraph" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AUGraph

Added:

```
public AUGraphError ClearConnections ();
 	public AUGraphError DisconnectNodeInput (int destNode, uint destInputNumber);
 	public AUGraphError GetCPULoad (out float averageCPULoad);
 	public AUGraphError GetMaxCPULoad (out float maxCPULoad);
 	public AUGraphError GetNode (uint index, out int node);
 	public AUGraphError GetNodeCount (out int count);
 	public AUGraphError GetNumberOfInteractions (int node, out uint interactionsCount);
 	public AUGraphError GetNumberOfInteractions (out uint interactionsCount);
 	public AUGraphError RemoveNode (int node);
 	public AUGraphError Start ();
 	public AUGraphError Stop ();
 	public bool Update ();
 	public IntPtr Handle {
 		get;
 	}
 	public bool IsInitialized {
 		get;
 	}
 	public bool IsOpen {
 		get;
 	}
 	public bool IsRunning {
 		get;
 	}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AUGraphError" class="injected"></a>


### New Type: MonoTouch.AudioUnit.AUGraphError

```
[Serializable]
public enum AUGraphError {
	OK,
	NodeNotFound,
	InvalidConnection,
	OutputNodeError,
	CannotDoInCurrentContext,
	InvalidAudioUnit,
	FormatNotSupported,
	InvalidElement
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioCodecManufacturer" class="injected"></a>


### New Type: MonoTouch.AudioUnit.AudioCodecManufacturer

```
[Serializable]
public enum AudioCodecManufacturer : uint {
	AppleSoftware,
	AppleHardware
}
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioComponentManufacturerType" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioComponentManufacturerType

Removed:

```
public enum AudioComponentManufacturerType {
```

Added:

```
public enum AudioComponentManufacturerType : uint {
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioComponentType" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioComponentType

Removed:

```
public enum AudioComponentType {
```

Added:

```
public enum AudioComponentType : uint {
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioGraphEventArgs" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioGraphEventArgs

Removed:

```
public class AudioGraphEventArgs : AudioUnitEventArgs {
```

Added:

```
[Obsolete]
public class AudioGraphEventArgs : AudioUnitEventArgs {
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioTypeGenerator&nbsp;" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioTypeGenerator&nbsp;

Added:

```
ScheduledSoundPlayer,
 	AudioFilePlayer
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioTypeMusicDevice" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioTypeMusicDevice

Added:

```
Sampler
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnit" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnit

Added:

```
public AudioUnitStatus Render (ref AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, MonoTouch.AudioToolbox.AudioBuffers data);
 	public AudioUnitStatus SetMaximumFramesPerSlice (uint value, AudioUnitScopeType scope, uint audioUnitElement);
 	public AudioUnitStatus SetParameter (AudioUnitParameterType type, float value, AudioUnitScopeType scope, uint audioUnitElement);
 	public AudioUnitStatus SetRenderCallback (RenderDelegate renderDelegate, AudioUnitScopeType scope, uint audioUnitElement);
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitEventArgs" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnitEventArgs

Removed:

```
public class AudioUnitEventArgs : EventArgs {
```

Added:

```
[Obsolete]
public class AudioUnitEventArgs : EventArgs {
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitParameterType" class="injected"></a>


### New Type: MonoTouch.AudioUnit.AudioUnitParameterType

```
[Serializable]
public enum AudioUnitParameterType {
	ReverbFilterFrequency,
	ReverbFilterBandwidth,
	ReverbFilterGain,
	MultiChannelMixerVolume,
	MultiChannelMixerEnable,
	MultiChannelMixerPan,
	MatrixMixerVolume,
	MatrixMixerEnable,
	HALOutputVolume,
	TimePitchRate,
	NewTimePitchRate,
	NewTimePitchPitch,
	NewTimePitchOverlap,
	NewTimePitchEnablePeakLocking,
	AUSamplerGain,
	AUSamplerCoarseTuning,
	AUSamplerFineTuning,
	AUSamplerPan,
	BandpassCenterFrequency,
	BandpassBandwidth,
	HipassCutoffFrequency,
	HipassResonance,
	LowPassCutoffFrequency,
	LowPassResonance,
	HighShelfCutOffFrequency,
	HighShelfGain,
	AULowShelfCutoffFrequency,
	AULowShelfGain,
	AUDCFilterDecayTime,
	ParametricEQCenterFreq,
	ParametricEQQ,
	ParametricEQGain,
	LimiterAttackTime,
	LimiterDecayTime,
	LimiterPreGain,
	DynamicsProcessorThreshold,
	DynamicsProcessorHeadRoom,
	DynamicsProcessorExpansionRatio,
	DynamicsProcessorExpansionThreshold,
	DynamicsProcessorAttackTime,
	DynamicsProcessorReleaseTime,
	DynamicsProcessorMasterGain,
	DynamicsProcessorCompressionAmount,
	DynamicsProcessorInputAmplitude,
	DynamicsProcessorOutputAmplitude,
	VarispeedPlaybackRate,
	VarispeedPlaybackCents,
	DistortionDelay,
	DistortionDecay,
	DistortionDelayMix,
	DistortionDecimation,
	DistortionRounding,
	DistortionDecimationMix,
	DistortionLinearTerm,
	DistortionSquaredTerm,
	DistortionCubicTerm,
	DistortionPolynomialMix,
	DistortionRingModFreq1,
	DistortionRingModFreq2,
	DistortionRingModBalance,
	DistortionRingModMix,
	DistortionSoftClipGain,
	DistortionFinalMix,
	DelayWetDryMix,
	DelayTime,
	DelayFeedback,
	DelayLopassCutoff,
	AUNBandEQGlobalGain,
	AUNBandEQBypassBand,
	AUNBandEQFilterType,
	AUNBandEQFrequency,
	AUNBandEQGain,
	AUNBandEQBandwidth,
	Reverb2DryWetMix,
	Reverb2Gain,
	Reverb2MinDelayTime,
	Reverb2MaxDelayTime,
	Reverb2DecayTimeAt0Hz,
	Reverb2DecayTimeAtNyquist,
	Reverb2RandomizeReflections
}
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitPropertyIDType" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added:

```
IsRunning,
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitRenderActionFlags" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnitRenderActionFlags

Added:

```
DoNotCheckRenderArgs
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitScopeType" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnitScopeType

Added:

```
Group,
 	Part,
 	Note,
 	Layer,
 	LayerItem
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitStatus" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.AudioUnitStatus

Added:

```
OK,
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.ExtAudioFile" class="injected"></a>


### Type Changed: MonoTouch.AudioUnit.ExtAudioFile

Added:

```
public static ExtAudioFileError WrapAudioFileID (IntPtr audioFileID, bool forWriting, out ExtAudioFile outAudioFile);
 	protected virtual void Dispose (bool disposing);
 	protected override void Finalize ();
 	public uint Read (uint numberFrames, MonoTouch.AudioToolbox.AudioBuffers audioBufferList, out ExtAudioFileError status);
 	public ExtAudioFileError Write (uint numberFrames, MonoTouch.AudioToolbox.AudioBuffers audioBufferList);
;
 	public ExtAudioFileError WriteAsync (uint numberFrames, MonoTouch.AudioToolbox.AudioBuffers audioBufferList);
 	public Nullable<IntPtr> AudioFile {
 		get;
 	}
 	public Nullable<uint> ClientMaxPacketSize {
 		get;
 	}
 	public Nullable<uint> FileMaxPacketSize {
 		get;
 	}
```

 <a name="New_Type:_MonoTouch.AudioUnit.ExtAudioFileError" class="injected"></a>


### New Type: MonoTouch.AudioUnit.ExtAudioFileError

```
[Serializable]
public enum ExtAudioFileError {
	OK,
	CodecUnavailableInputConsumed,
	CodecUnavailableInputNotConsumed,
	InvalidProperty,
	InvalidPropertySize,
	NonPCMClientFormat,
	InvalidChannelMap,
	InvalidOperationOrder,
	InvalidDataFormat,
	MaxPacketSizeUnknown,
	InvalidSeek,
	AsyncWriteTooLarge,
	AsyncWriteBufferOverflow,
	NotOpenError,
	EndOfFileError,
	PositionError,
	FileNotFoundError
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.RenderDelegate" class="injected"></a>


### New Type: MonoTouch.AudioUnit.RenderDelegate

```
[Serializable]
public delegate AudioUnitStatus RenderDelegate (AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, MonoTouch.AudioToolbox.AudioBuffers data);
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


## Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CADisplayLink" class="injected"></a>


### Type Changed: MonoTouch.CoreAnimation.CADisplayLink

Added:

```
public virtual double Duration {
 		get;
 	}
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAKeyFrameAnimation" class="injected"></a>


### Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Changed from:

```
public MonoTouch.CoreGraphics.CGPath Path {
```

To:

```
public virtual MonoTouch.CoreGraphics.CGPath Path {
```

 <a name="Namespace:_MonoTouch.CoreBluetooth" class="injected"></a>


## Namespace: MonoTouch.CoreBluetooth

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBATTRequest" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBATTRequest

Removed:

```
public CBATTRequest ();
```

Added:

```
[Obsolete("This type is not meant to be created by user code.")]
	public CBATTRequest ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentral" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBCentral

Added:

```
[Obsolete("This type is not meant to be created by user code.")]
	public CBCentral ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentralManager" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Removed:

```
public CBCentralManager ();
```

Added:

```
[Obsolete("Use .ctor(CBCentralManagerDelegate,DispatchQueue) to create a valid CBCentralManager instance")]
	public CBCentralManager ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCharacteristic" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBCharacteristic

Removed:

```
public CBCharacteristic ();
```

Added:

```
[Obsolete("This type is not meant to be created by user code. Use CBMutableCharacteristic")]
	public CBCharacteristic ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBDescriptor" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBDescriptor

Removed:

```
public CBDescriptor ();
```

Added:

```
[Obsolete("This type is not meant to be created by user code. Use CBMutableDescriptor")]
	public CBDescriptor ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBMutableCharacteristic" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBMutableCharacteristic

Removed:

```
public CBMutableCharacteristic ();
```

Added:

```
[Obsolete("Use .ctor(CBUUID,CBCharacteristicProperties,NSData,CBAttributePermissions)")]
	public CBMutableCharacteristic ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBMutableDescriptor" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBMutableDescriptor

Removed:

```
public CBMutableDescriptor ();
 	public CBMutableDescriptor (CBUUID uuid, IntPtr descriptorValue);
```

Added:

```
[Obsolete("Use .ctor(CBUUID,NSObject)")]
	public CBMutableDescriptor ();
 	public CBMutableDescriptor (CBUUID uuid, MonoTouch.Foundation.NSObject descriptorValue);
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBMutableService" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBMutableService

Removed:

```
public CBMutableService ();
```

Added:

```
[Obsolete("Use .ctor (CBUUID,bool)")]
	public CBMutableService ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBPeripheral" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Removed:

```
public CBPeripheral ();
```

Added:

```
[Obsolete("This type is not meant to be created by user code.")]
	public CBPeripheral ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBPeripheralManager" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager

Removed:

```
public CBPeripheralManager ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBService" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBService

Removed:

```
public CBService ();
```

Added:

```
[Obsolete("This type is not meant to be created by user code. Use CBMutableService")]
	public CBService ();
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBUUID" class="injected"></a>


### Type Changed: MonoTouch.CoreBluetooth.CBUUID

Removed:

```
public CBUUID ();
```

Added:

```
[Obsolete("Use FromString or FromData to create a valid CBUUID instance")]
	public CBUUID ();
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


## Namespace: MonoTouch.CoreData

 <a name="Type_Changed:_MonoTouch.CoreData.NSAttributeDescription" class="injected"></a>


### Type Changed: MonoTouch.CoreData.NSAttributeDescription

Removed:

```
public virtual NSAttributeDescription DefaultValue {
```

Added:

```
public virtual MonoTouch.Foundation.NSObject DefaultValue {
 		set;
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


## Namespace: MonoTouch.CoreFoundation

 <a name="New_Type:_MonoTouch.CoreFoundation.DispatchGroup" class="injected"></a>


### New Type: MonoTouch.CoreFoundation.DispatchGroup

```
public class DispatchGroup : DispatchObject {
	
	public static DispatchGroup Create ();
	public void DispatchAsync (DispatchQueue queue, MonoTouch.Foundation.NSAction action);
	public void Enter ();
	public void Leave ();
	public bool Wait (DispatchTime timeout);
}
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.DispatchObject" class="injected"></a>


### Type Changed: MonoTouch.CoreFoundation.DispatchObject

Changed from:

```
public class DispatchObject : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
 	public void Resume ();
 	public void Suspend ();
 	public IntPtr Context {
 		get;
 		set;
 	}
```

To:

```
public abstract class DispatchObject : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
 	protected void Check ();
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.DispatchQueue" class="injected"></a>


### Type Changed: MonoTouch.CoreFoundation.DispatchQueue

Removed:

```
public static DispatchQueue CurrentQueue {
```

Added:

```
public void Resume ();
 	public void Suspend ();
 	[Obsolete("Deprecated in iOS 6.0")]
	public static DispatchQueue CurrentQueue {
 	public IntPtr Context {
 		get;
 		set;
 	}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.DispatchTime" class="injected"></a>


### New Type: MonoTouch.CoreFoundation.DispatchTime

```
public struct DispatchTime {
	
	public DispatchTime (ulong nanoseconds);
	
	public ulong Nanoseconds {
		get;
	}
	
	public static readonly DispatchTime Now;
	public static readonly DispatchTime Forever;
}
```

 <a name="Namespace:_MonoTouch.CoreMedia" class="injected"></a>


## Namespace: MonoTouch.CoreMedia

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMFormatDescription" class="injected"></a>


### Type Changed: MonoTouch.CoreMedia.CMFormatDescription

Added:

```
public static CMFormatDescription Create (IntPtr handle, bool owns);
 	public MonoTouch.AudioToolbox.AudioFormatType AudioFormatType {
 		get;
 	}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMTimeMapping" class="injected"></a>


### Type Changed: MonoTouch.CoreMedia.CMTimeMapping

Removed:

```
public CMTime Source;
 	public CMTime Target;
```

Added:

```
public CMTimeRange Source;
 	public CMTimeRange Target;
```

 <a name="Namespace:_MonoTouch.CoreVideo" class="injected"></a>


## Namespace: MonoTouch.CoreVideo

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVTime" class="injected"></a>


### Type Changed: MonoTouch.CoreVideo.CVTime

Removed:

```
public int Flags;
```

Added:

```
public int Flags {
 		get;
 		set;
 	}
 	public CVTimeFlags TimeFlags;
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


## Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


### Type Changed: MonoTouch.EventKit.EKEvent

Removed:

```
public virtual int birthdayPersonID {
```

Added:

```
public virtual int BirthdayPersonID {
```

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


## Namespace: MonoTouch.EventKitUI

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKCalendarChooser" class="injected"></a>


### Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added:

```
set;
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


## Namespace: MonoTouch.Foundation

 <a name="New_Type:_MonoTouch.Foundation.AdviceAttribute" class="injected"></a>


### New Type: MonoTouch.Foundation.AdviceAttribute

```
public sealed class AdviceAttribute : Attribute {
	
	public AdviceAttribute (string message);
	
	public string Message {
		get;
	}
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.DictionaryContainer" class="injected"></a>


### Type Changed: MonoTouch.Foundation.DictionaryContainer

Added:

```
protected string GetStringValue (string key);
```

 <a name="New_Type:_MonoTouch.Foundation.LinkerSafeAttribute" class="injected"></a>


### New Type: MonoTouch.Foundation.LinkerSafeAttribute

```
public sealed class LinkerSafeAttribute : Attribute {
	
	public LinkerSafeAttribute ();
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSBundle

Removed:

```
public virtual void Load ();
 	public virtual void Unload ();
```

Added:

```
public virtual bool Load ();
 	public virtual bool Unload ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSData" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSData

Added:

```
public static NSData FromData (NSData source);
 		set;
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDecimalNumber" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSDecimalNumber

Removed:

```
public virtual NSDecimalNumber MultiplyPowerOf10 (NSDecimalNumber d);
 	public virtual NSDecimalNumber MultiplyPowerOf10 (NSDecimalNumber d, NSObject Behavior);
 	public virtual NSDecimalNumber RaiseTo (NSDecimalNumber d);
 	public virtual NSDecimalNumber RaiseTo (NSDecimalNumber d, NSObject Behavior);
```

Added:

```
public virtual NSDecimalNumber MultiplyPowerOf10 (short power);
 	public virtual NSDecimalNumber MultiplyPowerOf10 (short power, NSObject Behavior);
 	public virtual NSDecimalNumber RaiseTo (uint power);
 	public virtual NSDecimalNumber RaiseTo (uint power, NSObject Behavior);
```

 <a name="New_Type:_MonoTouch.Foundation.NSEnumerateErrorHandler" class="injected"></a>


### New Type: MonoTouch.Foundation.NSEnumerateErrorHandler

```
[Serializable]
public delegate bool NSEnumerateErrorHandler (NSUrl url, NSError error);
```

 <a name="&nbsp;" class="injected"></a>


### &nbsp;

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileManager" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSFileManager

Removed:

```
public virtual bool FileExists (string path, bool isDirectory);
 	public virtual NSDirectoryEnumerator GetEnumerator (NSUrl url, NSArray properties, NSDirectoryEnumerationOptions options, out NSError error);
 	public virtual string CurrentDirectory {
```

Added:

```
public virtual bool ChangeCurrentDirectory (string path);
 	public virtual bool FileExists (string path, ref bool isDirectory);
 	public virtual string GetCurrentDirectory ();
 	public virtual NSDirectoryEnumerator GetEnumerator (NSUrl url, NSArray properties, NSDirectoryEnumerationOptions options, NSEnumerateErrorHandler handler);
 	public string CurrentDirectory {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSInputStream" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSInputStream

Added:

```
public NSInputStream (NSData data);
 	public NSInputStream (NSUrl url);
 	public static NSInputStream FromUrl (NSUrl url);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLinguisticTagger" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSLinguisticTagger

Added:

```
public virtual NSOrthography GetOrthography (int charIndex, ref NSRange effectiveRange);
 	public virtual string GetTag (int charIndex, NSString tagScheme, ref NSRange tokenRange, ref NSRange sentenceRange);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableData" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSMutableData

Added:

```
public override uint Length {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableIndexSet" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSMutableIndexSet

Removed:

```
public virtual void ShiftIndexes (uint startIndex, uint delta);
```

Added:

```
public virtual void ShiftIndexes (uint startIndex, int delta);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNetService" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSNetService

Added:

```
public virtual NSData GetTxtRecordData ();
 	public virtual bool SetTxtRecordData (NSData data);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSObject

Added:

```
public static void CancelPreviousPerformRequest (NSObject aTarget);
 	public static void CancelPreviousPerformRequest (NSObject aTarget, MonoTouch.ObjCRuntime.Selector selector, NSObject argument);
 	public virtual void Invoke (NSAction action, double delay);
 	public virtual void Invoke (NSAction action, TimeSpan delay);
 	public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector selector, NSObject withObject, double afterDelay, NSString[] nsRunLoopModes);
 	public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector selector, NSThread onThread, NSObject withObject, bool waitUntilDone);
 	public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector selector, NSThread onThread, NSObject withObject, bool waitUntilDone, NSString[] nsRunLoopModes);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSProcessInfo" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSProcessInfo

Removed:

```
public virtual long PhysicalMemory {
```

Added:

```
public virtual ulong PhysicalMemory {
```

 <a name="New_Type:_MonoTouch.Foundation.NSPropertyListMutabilityOptions" class="injected"></a>


### New Type: MonoTouch.Foundation.NSPropertyListMutabilityOptions

```
[Serializable]
public enum NSPropertyListMutabilityOptions {
	Immutable,
	MutableContainers,
	MutableContainersAndLeaves
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSPropertyListReadOptions" class="injected"></a>


### New Type: MonoTouch.Foundation.NSPropertyListReadOptions

```
[Serializable]
public enum NSPropertyListReadOptions {
	Immutable,
	MutableContainers,
	MutableContainersAndLeaves
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSPropertyListSerialization" class="injected"></a>


### New Type: MonoTouch.Foundation.NSPropertyListSerialization

```
public class NSPropertyListSerialization : NSObject {
	
	public NSPropertyListSerialization (NSCoder coder);
	public NSPropertyListSerialization (NSObjectFlag t);
	public NSPropertyListSerialization (IntPtr handle);
	
	public static NSData DataWithPropertyList (NSObject plist, NSPropertyListFormat format, NSPropertyListWriteOptions options, out NSError error);
	public static bool IsValidForFormat (NSObject plist, NSPropertyListFormat format);
	public static NSObject PropertyListWithData (NSData data, NSPropertyListReadOptions options, ref NSPropertyListFormat format, out NSError error);
	public static NSObject PropertyListWithStream (NSInputStream stream, NSPropertyListReadOptions options, ref NSPropertyListFormat format, out NSError error);
	public static int WritePropertyList (NSObject plist, NSOutputStream stream, NSPropertyListFormat format, NSPropertyListWriteOptions options, out NSError error);
	
	public override IntPtr ClassHandle {
		get;
	}
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSPropertyListWriteOptions" class="injected"></a>


### New Type: MonoTouch.Foundation.NSPropertyListWriteOptions

```
[Serializable]
public enum NSPropertyListWriteOptions {
	Immutable,
	MutableContainers,
	MutableContainersAndLeaves
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlAuthenticationChallenge" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSUrlAuthenticationChallenge

Removed:

```
public virtual void PejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
 	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnection" class="injected"></a>


### Type Changed: MonoTouch.Foundation.NSUrlConnection

Removed:

```
public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate del);
 	public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate del, bool startImmediately);
 	public static NSUrlConnection FromRequest (NSUrlRequest request, NSUrlConnectionDelegate del);
```

Added:

```
public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate);
 	public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate, bool startImmediately);
 	public static NSUrlConnection FromRequest (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate);
 	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
 	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge); Namespace: MonoTouch.GLKit
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKTextureLoader" class="injected"></a>


### Type Changed: MonoTouch.GLKit.GLKTextureLoader

Removed:

```
public virtual IntPtr Constructors (MonoTouch.OpenGLES.EAGLSharegroup sharegroup);
```

Added:

```
public GLKTextureLoader (MonoTouch.OpenGLES.EAGLSharegroup sharegroup);
 	public static GLKTextureInfo CubeMapFromFile (string path, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo CubeMapFromFiles (string [] files, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo CubeMapFromUrl (MonoTouch.Foundation.NSUrl url, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo CubeMapFromUrls (MonoTouch.Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo FromData (MonoTouch.Foundation.NSData data, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo FromFile (string path, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo FromImage (MonoTouch.CoreGraphics.CGImage cgImage, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public static GLKTextureInfo FromUrl (MonoTouch.Foundation.NSUrl url, GLKTextureOperations textureOperations, out MonoTouch.Foundation.NSError error);
 	public void BeginLoadCubeMap (MonoTouch.Foundation.NSUrl filePath, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginLoadCubeMap (MonoTouch.Foundation.NSUrl[] urls, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginLoadCubeMap (string fileName, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginLoadCubeMap (string [] files, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginTextureLoad (MonoTouch.CoreGraphics.CGImage image, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginTextureLoad (MonoTouch.Foundation.NSData data, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginTextureLoad (MonoTouch.Foundation.NSUrl filePath, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
 	public void BeginTextureLoad (string file, GLKTextureOperations textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKTextureLoaderCallback" class="injected"></a>


### Type Changed: MonoTouch.GLKit.GLKTextureLoaderCallback

Removed:

```
public delegate void GLKTextureLoaderCallback (uint textureName, MonoTouch.Foundation.NSError error);
```

Added:

```
public delegate void GLKTextureLoaderCallback (GLKTextureInfo textureInfo, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureOperations" class="injected"></a>


### New Type: MonoTouch.GLKit.GLKTextureOperations

```
public class GLKTextureOperations : MonoTouch.Foundation.DictionaryContainer {
	
	public GLKTextureOperations ();
	public GLKTextureOperations (MonoTouch.Foundation.NSDictionary options);
	
	public Nullable<bool> ApplyPremultiplication {
		get;
		set;
	}
	public Nullable<bool> GenerateMipmaps {
		get;
		set;
	}
	public Nullable<bool> GrayscaleAsAlpha {
		get;
		set;
	}
	public Nullable<bool> OriginBottomLeft {
		get;
		set;
	}
}
</bool></bool></bool></bool>
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


## Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>


### Type Changed: MonoTouch.GameKit.GKLeaderboard

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKVoiceChat" class="injected"></a>


### Type Changed: MonoTouch.GameKit.GKVoiceChat

&nbsp;

Added:

```
public virtual GKPlayerStateUpdateHandler PlayerStateUpdateHandler {
 		get;
 		set;
 	}
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


## Namespace: MonoTouch.ImageIO

 <a name="&nbsp;" class="injected"></a>


### &nbsp;

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


## Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

Added:

```
set;
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
```

 <a name="Namespace:_MonoTouch.MediaToolbox" class="injected"></a>


## Namespace: MonoTouch.MediaToolbox

 <a name="Type_Changed:_MonoTouch.MediaToolbox.MTAudioProcessingTap" class="injected"></a>


### Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTap

Added:

```
public MTAudioProcessingTapError GetSourceAudio (long frames, MonoTouch.AudioToolbox.AudioBuffers bufferList, out MTAudioProcessingTapFlags flags, out MonoTouch.CoreMedia.CMTimeRange timeRange, long framesProvided);
```

 <a name="Type_Changed:_MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks" class="injected"></a>


### Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks

Removed:

```
public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessCallback process);
 	public MTAudioProcessingTapProcessCallback Process {
```

Added:

```
[Obsolete("Use constructor with MTAudioProcessingTapProcessDelegate")]
	public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessCallback process);
 	public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessDelegate process);
 	[Obsolete("Use Processing property instead")]
	public MTAudioProcessingTapProcessCallback Process {
 		get;
 	}
 	public MTAudioProcessingTapProcessDelegate Processing {
```

 <a name="Type_Changed:_MonoTouch.MediaToolbox.MTAudioProcessingTapProcessCallback" class="injected"></a>


### Type Changed: MonoTouch.MediaToolbox.MTAudioProcessingTapProcessCallback

Removed:

```
public delegate void MTAudioProcessingTapProcessCallback (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, ref MonoTouch.AudioToolbox.AudioBufferList bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

Added:

```
[Obsolete]
public delegate void MTAudioProcessingTapProcessCallback (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, ref MonoTouch.AudioToolbox.AudioBufferList bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapProcessDelegate" class="injected"></a>


### New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapProcessDelegate

```
[Serializable]
public delegate void MTAudioProcessingTapProcessDelegate (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, MonoTouch.AudioToolbox.AudioBuffers bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


## Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


### Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added:

```
public static void SetArray (IntPtr handle, string symbol, MonoTouch.Foundation.NSArray array);
 	public static void SetString (IntPtr handle, string symbol, MonoTouch.Foundation.NSString value);
 	public static void SetString (IntPtr handle, string symbol, string value);
```

 <a name="Namespace:_MonoTouch.Security" class="injected"></a>


## Namespace: MonoTouch.Security

 <a name="Type_Changed:_MonoTouch.Security.SecKey" class="injected"></a>


### Type Changed: MonoTouch.Security.SecKey

Added:

```
public SecKey (IntPtr handle);
 	public SecKey (IntPtr handle, bool owns);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


## Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.NSLayoutConstraint" class="injected"></a>


### Type Changed: MonoTouch.UIKit.NSLayoutConstraint

Removed:

```
public virtual UILayoutPriority Priority {
```

Added:

```
public virtual float Priority {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIApplication

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonItem" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIBezierPath

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIImagePickerController

Removed:

```
public virtual bool StopVideoCapture ();
```

Added:

```
public virtual void StopVideoCapture ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationBar" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UINavigationBar

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIResponder" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIResponder

Removed:

```
public virtual void MakeTextWritingDirectionLeftToRight ();
 	public virtual void MakeTextWritingDirectionRightToLeft ();
```

Added:

```
public virtual void MakeTextWritingDirectionLeftToRight (MonoTouch.Foundation.NSObject sender);
 	public virtual void MakeTextWritingDirectionRightToLeft (MonoTouch.Foundation.NSObject sender);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBar" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UISearchBar

Added:

```
public virtual UIView InputAccessoryView {
 		get;
 		set;
 	}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UITableView

Removed:

```
public virtual MonoTouch.Foundation.NSObject DequeueReusableCell (MonoTouch.Foundation.NSString reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual MonoTouch.Foundation.NSObject DequeueReusableHeaderFooterView (MonoTouch.Foundation.NSString reuseIdentifier);
```

Added:

```
public virtual UITableViewCell DequeueReusableCell (MonoTouch.Foundation.NSString reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UITableViewHeaderFooterView DequeueReusableHeaderFooterView (MonoTouch.Foundation.NSString reuseIdentifier);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewHeaderFooterView" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added:

```
set;
 			set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UITextField

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UITextView

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIView

Removed:

```
public virtual UILayoutPriority ContentCompressionResistancePriority (UILayoutConstraintAxis axis);
 	public virtual UILayoutPriority ContentHuggingPriority (UILayoutConstraintAxis axis);
 	public virtual void SetContentCompressionResistancePriority (UILayoutPriority priority, UILayoutConstraintAxis axis);
 	public virtual void SetContentHuggingPriority (UILayoutPriority priority, UILayoutConstraintAxis axis);
```

Added:

```
public virtual float ContentCompressionResistancePriority (UILayoutConstraintAxis axis);
 	public virtual float ContentHuggingPriority (UILayoutConstraintAxis axis);
 	public virtual void SetContentCompressionResistancePriority (float priority, UILayoutConstraintAxis axis);
 	public virtual void SetContentHuggingPriority (float priority, UILayoutConstraintAxis axis);
 		set;
 		set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


### Type Changed: MonoTouch.UIKit.UIViewController

Added:

```
set;
```
