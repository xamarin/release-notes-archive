---
id: 58B3BD6F-4439-4185-A1B6-AE1463E56C92
title: "From 5.99.3 to 5.99.4"
---

<html><head><title>Comparison between monotouch-5.99.3.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "5.99.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "5.99.4";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Removed:</p><pre>
 	public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string [] preferredLanguages);
</pre>
<p>Added:</p><pre>
 	public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string [] languages);
 	public virtual AVAssetReferenceRestrictions ReferenceRestrictions {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput</h3>
<p>Removed:</p><pre>
 	public static AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
 	public virtual MonoTouch.Foundation.NSDictionary AudioSettings {
</pre>
<p>Added:</p><pre>
 	public AVAssetReaderAudioMixOutput (AVAssetTrack[] audioTracks, AudioSettings settings);
 	[Obsolete("Use Create method")]
	public static AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
 	public AVAssetReaderAudioMixOutput Create (AVAssetTrack[] audioTracks, AudioSettings settings);
 	[Obsolete("Use Settings property")]
	public virtual MonoTouch.Foundation.NSDictionary AudioSettings {
 	public AudioSettings Settings {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderTrackOutput</h3>
<p>Removed:</p><pre>
 	public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
</pre>
<p>Added:</p><pre>
 	public AVAssetReaderTrackOutput (AVAssetTrack track, AudioSettings settings);
 	public AVAssetReaderTrackOutput (AVAssetTrack track, AVVideoSettingsUncompressed settings);
 	public static AVAssetReaderTrackOutput Create (AVAssetTrack track, AudioSettings settings);
 	public static AVAssetReaderTrackOutput Create (AVAssetTrack track, AVVideoSettingsUncompressed settings);
 	[Obsolete("Use Create method")]
	public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput</h3>
<p>Removed:</p><pre>
 	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
 	public AVVideoSettings VideoSettings {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use overload with PixelBufferAttributes")]
	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, MonoTouch.CoreVideo.CVPixelBufferAttributes settings);
 	public AVAssetReaderVideoCompositionOutput Create (AVAssetTrack[] videoTracks, MonoTouch.CoreVideo.CVPixelBufferAttributes settings);
 	[Obsolete("Use Create method or constructor")]
	public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	[Obsolete("Use Create method")]
	public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
 	public MonoTouch.CoreVideo.CVPixelBufferAttributes UncompressedVideoSettings {
 		get;
 	}
 	[Obsolete("Use UncompressedVideoSettings property")]
	public AVVideoSettings VideoSettings {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoadingRequest</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSData GetStreamingContentKey (MonoTouch.Foundation.NSData appIdentifier, MonoTouch.Foundation.NSData contentIdentifier, MonoTouch.Foundation.NSDictionary options, MonoTouch.Foundation.NSError outError);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSData GetStreamingContentKey (MonoTouch.Foundation.NSData appIdentifier, MonoTouch.Foundation.NSData contentIdentifier, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriter</h3>
<p>Removed:</p><pre>
 	public virtual bool CanApplyOutputSettings (MonoTouch.Foundation.NSDictionary outputSettings, string toMediaType);
</pre>
<p>Added:</p><pre>
 	public bool CanApplyOutputSettings (AudioSettings outputSettings, string mediaType);
 	public bool CanApplyOutputSettings (AVVideoSettingsCompressed outputSettings, string mediaType);
 	public virtual bool CanApplyOutputSettings (MonoTouch.Foundation.NSDictionary outputSettings, string mediaType);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput</h3>
<p>Removed:</p><pre>
 	public AVAssetWriterInput (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public static AVAssetWriterInput Create (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public static AVAssetWriterInput FromType (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings);
</pre>
<p>Added:</p><pre>
 	protected AVAssetWriterInput (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public AVAssetWriterInput (string mediaType, AudioSettings outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public AVAssetWriterInput (string mediaType, AVVideoSettingsCompressed outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public AVAssetWriterInput (string mediaType, AudioSettings outputSettings);
 	public AVAssetWriterInput (string mediaType, AVVideoSettingsCompressed outputSettings);
 	public static AVAssetWriterInput Create (string mediaType, AudioSettings outputSettings);
 	public static AVAssetWriterInput Create (string mediaType, AudioSettings outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	public static AVAssetWriterInput Create (string mediaType, AVVideoSettingsCompressed outputSettings);
 	public static AVAssetWriterInput Create (string mediaType, AVVideoSettingsCompressed outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
 	[Obsolete("Use constructor or Create method")]
	public static AVAssetWriterInput FromType (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor</h3>
<p>Removed:</p><pre>
 	public static AVAssetWriterInputPixelBufferAdaptor FromInput (AVAssetWriterInput input, MonoTouch.Foundation.NSDictionary sourcePixelBufferAttributes);
</pre>
<p>Added:</p><pre>
 	public AVAssetWriterInputPixelBufferAdaptor (AVAssetWriterInput input, MonoTouch.CoreVideo.CVPixelBufferAttributes attributes);
 	public static AVAssetWriterInputPixelBufferAdaptor Create (AVAssetWriterInput input, MonoTouch.CoreVideo.CVPixelBufferAttributes attributes);
 	[Obsolete("Use Create method")]
	public static AVAssetWriterInputPixelBufferAdaptor FromInput (AVAssetWriterInput input, MonoTouch.Foundation.NSDictionary sourcePixelBufferAttributes);
 	public MonoTouch.CoreVideo.CVPixelBufferAttributes Attributes {
 		get;
 	}
 	public virtual MonoTouch.CoreVideo.CVPixelBufferPool PixelBufferPool {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayer</h3>
<p>Removed:</p><pre>
 	public AVAudioPlayerSettings Settings {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use SoundSettings")]
	public AVAudioPlayerSettings Settings {
 		get;
 	}
 	public AudioSettings SoundSetting {
 	protected virtual MonoTouch.Foundation.NSDictionary WeakSettings {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS6")]
	public virtual void EndInterruption (AVAudioPlayer player);
 	[Obsolete("Deprecated in iOS6")]
	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0")]
	public virtual void EndInterruption (AVAudioPlayer player);
 	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioRecorder</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use the factory AVAudioRecorder.ToUrl as this method had an invalid signature up to MonoTouch 1.4.4")]
	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
 	public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, AVAudioRecorderSettings settings, out MonoTouch.Foundation.NSError error);
 	public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, out MonoTouch.Foundation.NSError error);
 	public virtual MonoTouch.Foundation.NSDictionary Settings {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use static Create method as this method had an invalid signature up to MonoTouch 1.4.4")]
	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
 	public static AVAudioRecorder Create (MonoTouch.Foundation.NSUrl url, AudioSettings settings, out MonoTouch.Foundation.NSError error);
 	[Obsolete("Use Create method")]
	public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, AVAudioRecorderSettings settings, out MonoTouch.Foundation.NSError error);
 	[Obsolete("Use Create method")]
	public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, out MonoTouch.Foundation.NSError error);
 	public AudioSettings AudioSettings {
 		get;
 	}
 	[Obsolete("Use AudioSettings")]
	public virtual MonoTouch.Foundation.NSDictionary Settings {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void EndInterruption (AVAudioRecorder recorder);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0")]
	public virtual void EndInterruption (AVAudioRecorder recorder);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureDevice</h3>
<p>Added:</p><pre>
 	public virtual bool AutomaticallyEnablesLowLightBoostWhenAvailable {
 		get;
 		set;
 	}
 	public virtual bool LowLightBoostEnabled {
 		get;
 	}
 	public virtual bool LowLightBoostSupported {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureInputPort</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreMedia.CMFormatDescription FormatDescription {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h3>
<p>Added:</p><pre>
 	public AVVideoSettingsCompressed CompressedVideoSetting {
 		get;
 		set;
 	}
 	public AVVideoSettingsUncompressed UncompressedVideoSetting {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Removed:</p><pre>
 	public AVVideoSettings VideoSettings {
</pre>
<p>Added:</p><pre>
 	public AVVideoSettingsCompressed CompressedVideoSetting {
 		get;
 		set;
 	}
 	public AVVideoSettingsUncompressed UncompressedVideoSetting {
 		get;
 		set;
 	}
 	[Obsolete("Use Compressed or Uncompressed property")]
	public AVVideoSettings VideoSettings {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h3>
<p>Removed:</p><pre>
 	public virtual string VideoGravity {
</pre>
<p>Added:</p><pre>
 	public AVLayerVideoGravity LayerVideoGravity {
 		get;
 		set;
 	}
 	[Obsolete("Use LayerVideoGravity")]
	public virtual string VideoGravity {
 		get;
 		set;
 	}
 	protected virtual MonoTouch.Foundation.NSString WeakVideoGravity {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVError</h3>
<p>Removed:</p><pre>
 	DecodeFailed,
 	FileAlreadyExists,
 	ContentIsProtected,
 	FailedToParse,
 	FormatNotRecognized,
 	MediaServicesWereReset,
</pre>
<p>Added:</p><pre>
 	MediaServicesWereReset,
 	DecodeFailed,
 	FileAlreadyExists,
 	FormatNotRecognized,
 	FailedToParse,
 	ContentIsProtected,
 	ApplicationIsNotAuthorized,
 	ReferenceForbiddenByReferencePolicy,
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVLayerVideoGravity</h3>
<pre>
[Serializable]
public enum AVLayerVideoGravity {
	ResizeAspect,
	ResizeAspectFill,
	Resize
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayer</h3>
<p>Removed:</p><pre>
 	public virtual bool AirPlayVideoActive {
 	public virtual bool AllowsAirPlayVideo {
 	public virtual bool UsesAirPlayVideoWhileAirPlayScreenIsActive {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Obsoleted in iOS6, use ExternalPlaybackActive")]
	public virtual bool AirPlayVideoActive {
 	[Obsolete("Obsoleted in iOS6, use AllowsExternalPlayback")]
	public virtual bool AllowsAirPlayVideo {
 		get;
 		set;
 	}
 	public virtual bool AllowsExternalPlayback {
 	public virtual bool ExternalPlaybackActive {
 		get;
 	}
 	public Nullable&lt;AVLayerVideoGravity&gt; ExternalPlaybackVideoGravity {
 		get;
 		set;
 	}
 	[Obsolete("Obsoleted in iOS6, use UsesExternalPlaybackWhileExternalScreenIsActive")]
	public virtual bool UsesAirPlayVideoWhileAirPlayScreenIsActive {
 		get;
 		set;
 	}
 	public virtual bool UsesExternalPlaybackWhileExternalScreenIsActive {
 		get;
 		set;
 	}
 	protected virtual MonoTouch.Foundation.NSString WeakExternalPlaybackVideoGravity {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreMedia.CMTime Duration {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemVideoOutput</h3>
<p>Removed:</p><pre>
 	public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
</pre>
<p>Added:</p><pre>
 	protected AVPlayerItemVideoOutput (MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
 	public AVPlayerItemVideoOutput (MonoTouch.CoreVideo.CVPixelBufferAttributes attributes);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h3>
<p>Removed:</p><pre>
 	public virtual string VideoGravity {
</pre>
<p>Added:</p><pre>
 	public AVLayerVideoGravity LayerVideoGravity {
 		get;
 		set;
 	}
 	[Obsolete("Use LayerVideoGravity")]
	public virtual string VideoGravity {
 		get;
 		set;
 	}
 	protected virtual MonoTouch.Foundation.NSString WeakVideoGravity {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVTextStyleRule</h3>
<p>Removed:</p><pre>
 	public AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
 	public AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
 	public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
 	public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
 	public virtual MonoTouch.Foundation.NSDictionary TextMarkupAttributes {
</pre>
<p>Added:</p><pre>
 	protected AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
 	public AVTextStyleRule (MonoTouch.CoreMedia.CMTextMarkupAttributes attributes);
 	protected AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
 	public AVTextStyleRule (MonoTouch.CoreMedia.CMTextMarkupAttributes attributes, string textSelector);
 	public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.CoreMedia.CMTextMarkupAttributes textMarkupAttributes);
 	public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.CoreMedia.CMTextMarkupAttributes textMarkupAttributes, string textSelector);
 	public MonoTouch.CoreMedia.CMTextMarkupAttributes TextMarkupAttributes {
 	protected virtual MonoTouch.Foundation.NSDictionary WeakTextMarkupAttributes {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVUrlAsset</h3>
<p>Removed:</p><pre>
 	public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
</pre>
<p>Added:</p><pre>
 	public AVUrlAsset (MonoTouch.Foundation.NSUrl url, AVUrlAssetOptions options);
 	public static AVUrlAsset Create (MonoTouch.Foundation.NSUrl url, AVUrlAssetOptions options);
 	[Obsolete("Use Create or constructor")]
	public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVUrlAssetOptions</h3>
<pre>
public class AVUrlAssetOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public AVUrlAssetOptions ();
	public AVUrlAssetOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<bool> PreferPreciseDurationAndTiming {
		get;
		set;
	}
	public Nullable<avassetreferencerestrictions> ReferenceRestrictions {
		get;
		set;
	}
}
</avassetreferencerestrictions></bool></pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ScalingModeKey {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCleanApertureSettings</h3>
<pre>
public class AVVideoCleanApertureSettings : MonoTouch.Foundation.DictionaryContainer {
	
	public AVVideoCleanApertureSettings ();
	public AVVideoCleanApertureSettings (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<int> Height {
		get;
		set;
	}
	public Nullable<int> HorizontalOffset {
		get;
		set;
	}
	public Nullable<int> VerticalOffset {
		get;
		set;
	}
	public Nullable<int> Width {
		get;
		set;
	}
}
</int></int></int></int></pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCodec</h3>
<pre>
[Serializable]
public enum AVVideoCodec {
	H264,
	JPEG
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCodecSettings</h3>
<pre>
public class AVVideoCodecSettings : MonoTouch.Foundation.DictionaryContainer {
	
	public AVVideoCodecSettings ();
	public AVVideoCodecSettings (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<int> AverageBitRate {
		get;
		set;
	}
	public Nullable<float> JPEGQuality {
		get;
		set;
	}
	public Nullable<int> MaxKeyFrameInterval {
		get;
		set;
	}
	public AVVideoPixelAspectRatioSettings PixelAspectRatio {
		set;
	}
	public Nullable<avvideoprofilelevelh264> ProfileLevelH264 {
		set;
	}
	public AVVideoCleanApertureSettings VideoCleanAperture {
		set;
	}
}
</avvideoprofilelevelh264></int></float></int></pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoPixelAspectRatioSettings</h3>
<pre>
public class AVVideoPixelAspectRatioSettings : MonoTouch.Foundation.DictionaryContainer {
	
	public AVVideoPixelAspectRatioSettings ();
	public AVVideoPixelAspectRatioSettings (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<int> HorizontalSpacing {
		get;
		set;
	}
	public Nullable<int> VerticalSpacing {
		get;
		set;
	}
}
</int></int></pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoProfileLevelH264</h3>
<pre>
[Serializable]
public enum AVVideoProfileLevelH264 {
	Baseline30,
	Baseline31,
	Baseline41,
	Main30,
	Main31,
	Main32,
	Main41,
	High40,
	High41
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoScalingMode</h3>
<pre>
[Serializable]
public enum AVVideoScalingMode {
	Fit,
	Resize,
	ResizeAspect,
	ResizeAspectFill
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoScalingModeKey</h3>
<pre>
public static class AVVideoScalingModeKey {
	
	public static MonoTouch.Foundation.NSString Fit {
		get;
	}
	public static MonoTouch.Foundation.NSString Resize {
		get;
	}
	public static MonoTouch.Foundation.NSString ResizeAspect {
		get;
	}
	public static MonoTouch.Foundation.NSString ResizeAspectFill {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoSettings</h3>
<p>Removed:</p><pre>
 	public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
 	public MonoTouch.Foundation.NSDictionary ToDictionary ();
 	public System.Nullable&lt;MonoTouch.CoreVideo.CVPixelFormatType&gt; PixelFormat {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use PixelBufferAttributes")]
	public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
 	[Obsolete("Use PixelBufferAttributes")]
	public MonoTouch.Foundation.NSDictionary ToDictionary ();
 	[Obsolete("Use PixelBufferAttributes")]
	public System.Nullable&lt;MonoTouch.CoreVideo.CVPixelFormatType&gt; PixelFormat {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoSettingsCompressed</h3>
<pre>
public class AVVideoSettingsCompressed : MonoTouch.Foundation.DictionaryContainer {
	
	public AVVideoSettingsCompressed ();
	public AVVideoSettingsCompressed (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<avvideocodec> Codec {
		set;
	}
	public AVVideoCodecSettings CodecSettings {
		set;
	}
	public Nullable<int> Height {
		get;
		set;
	}
	public Nullable<avvideoscalingmode> ScalingMode {
		set;
	}
	public Nullable<int> Width {
		get;
		set;
	}
}
</int></avvideoscalingmode></int></avvideocodec></pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoSettingsUncompressed</h3>
<pre>
public class AVVideoSettingsUncompressed : MonoTouch.CoreVideo.CVPixelBufferAttributes {
	
	public AVVideoSettingsUncompressed ();
	public AVVideoSettingsUncompressed (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<avvideoscalingmode> ScalingMode {
		set;
	}
}
</avvideoscalingmode></pre>
<h3>New Type: MonoTouch.AVFoundation.AudioSettings</h3>
<pre>
public class AudioSettings : MonoTouch.Foundation.DictionaryContainer {
	
	public AudioSettings ();
	public AudioSettings (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<avaudioquality> AudioQuality {
		get;
		set;
	}
	public MonoTouch.AudioToolbox.AudioChannelLayout ChannelLayout {
		set;
	}
	public Nullable<int> EncoderBitDepthHint {
		get;
		set;
	}
	public Nullable<int> EncoderBitRate {
		get;
		set;
	}
	public Nullable<int> EncoderBitRatePerChannel {
		get;
		set;
	}
	public System.Nullable<monotouch.audiotoolbox.audioformattype> Format {
		get;
		set;
	}
	public Nullable<bool> LinearPcmBigEndian {
		get;
		set;
	}
	public Nullable<int> LinearPcmBitDepth {
		get;
		set;
	}
	public Nullable<bool> LinearPcmFloat {
		get;
		set;
	}
	public Nullable<bool> LinearPcmNonInterleaved {
		get;
		set;
	}
	public Nullable<int> NumberChannels {
		get;
		set;
	}
	public Nullable<float> SampleRate {
		get;
		set;
	}
	public Nullable<avaudioquality> SampleRateConverterAudioQuality {
		get;
		set;
	}
}
</avaudioquality></float></int></bool></bool></int></bool></monotouch.audiotoolbox.audioformattype></int></int></int></avaudioquality></pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccountStore</h3>
<p>Removed:</p><pre>
 	[Obsolete("Obsolete in iOS 6.0")]
	public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
 	public virtual void RequestAccessToAccount (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options, ACRequestCompletionHandler completion);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Obsolete in iOS 6.0. Use overload with options instead")]
	public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
 	public void RequestAccess (ACAccountType accountType, AccountStoreOptions options, ACRequestCompletionHandler completion);
 	protected virtual void RequestAccess (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options, ACRequestCompletionHandler completion);
</pre>
<h3>Type Removed: MonoTouch.Accounts.ACFacebook</h3>
<h3>Type Changed: MonoTouch.Accounts.ACFacebookAudience</h3>
<p>Removed:</p><pre>
 public static class ACFacebookAudience {
 	
 	public static MonoTouch.Foundation.NSString Everyone {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Friends {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OnlyMe {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum ACFacebookAudience {
 	Everyone,
 	Friends,
 	OnlyMe
</pre>
<h3>New Type: MonoTouch.Accounts.ACFacebookAudienceValue</h3>
<pre>
public static class ACFacebookAudienceValue {
	
	public static MonoTouch.Foundation.NSString Everyone {
		get;
	}
	public static MonoTouch.Foundation.NSString Friends {
		get;
	}
	public static MonoTouch.Foundation.NSString OnlyMe {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Accounts.ACFacebookKey</h3>
<pre>
public static class ACFacebookKey {
	
	public static MonoTouch.Foundation.NSString AppId {
		get;
	}
	public static MonoTouch.Foundation.NSString Audience {
		get;
	}
	public static MonoTouch.Foundation.NSString Permissions {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Accounts.AccountStoreOptions</h3>
<pre>
public class AccountStoreOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public AccountStoreOptions ();
	public AccountStoreOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public void SetPermissions (ACFacebookAudience audience, params string [] permissions);
	
	public string FacebookAppId {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.AdSupport</h2>
<h3>New Type: MonoTouch.AdSupport.ASIdentifierManager</h3>
<pre>
public class ASIdentifierManager : MonoTouch.Foundation.NSObject {
	
	public ASIdentifierManager (MonoTouch.Foundation.NSCoder coder);
	public ASIdentifierManager (MonoTouch.Foundation.NSObjectFlag t);
	public ASIdentifierManager (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public static ASIdentifierManager SharedManager {
		get;
	}
	public virtual MonoTouch.Foundation.NSUuid AdvertisingIdentifier {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool IsAdvertisingTrackingEnabled {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.AddressBook</h2>
<h3>Type Changed: MonoTouch.AddressBook.ABAddressBookError</h3>
<p>Removed:</p><pre>
 	NotPermittedByUserError
</pre>
<p>Added:</p><pre>
 	OperationNotPermittedByUserError
</pre>
<h3>Type Removed: MonoTouch.AddressBook.DictionaryContainer</h3>
<h3>Type Changed: MonoTouch.AddressBook.InstantMessageService</h3>
<p>Removed:</p><pre>
 public class InstantMessageService : DictionaryContainer {
</pre>
<p>Added:</p><pre>
 public class InstantMessageService : MonoTouch.Foundation.DictionaryContainer {
</pre>
<h3>Type Changed: MonoTouch.AddressBook.PersonAddress</h3>
<p>Removed:</p><pre>
 public class PersonAddress : DictionaryContainer {
</pre>
<p>Added:</p><pre>
 public class PersonAddress : MonoTouch.Foundation.DictionaryContainer {
</pre>
<h3>Type Changed: MonoTouch.AddressBook.SocialProfile</h3>
<p>Removed:</p><pre>
 public class SocialProfile : DictionaryContainer {
</pre>
<p>Added:</p><pre>
 public class SocialProfile : MonoTouch.Foundation.DictionaryContainer {
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioFormatType</h3>
<p>Removed:</p><pre>
 	AES3,
 	MPEG4AAC_ELD,
 	MPEG4AAC_ELD_V2
</pre>
<p>Added:</p><pre>
 	MPEG4AAC_ELD,
 	MPEG4AAC_ELD_SBR,
 	MPEG4AAC_ELD_V2,
 	AES3
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Removed:</p><pre>
 	public event EventHandler&lt;CBPeripheralEventArgs&gt; RetrievedConnectedPeripherals;
</pre>
<p>Added:</p><pre>
 	public event EventHandler&lt;CBPeripheralsEventArgs&gt; RetrievedConnectedPeripherals;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
</pre>
<p>Added:</p><pre>
 	public virtual void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralEventArgs</h3>
<p>Removed:</p><pre>
 	public CBPeripheralEventArgs (CBPeripheral peripherals);
 	public CBPeripheral Peripherals {
</pre>
<p>Added:</p><pre>
 	public CBPeripheralEventArgs (CBPeripheral peripheral);
 	public CBPeripheral Peripheral {
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<p>Removed:</p><pre>
 	public virtual void StartAdvertising (MonoTouch.Foundation.NSDictionary advertisementData);
 	public event EventHandler UpdatedState;
</pre>
<p>Added:</p><pre>
 	public void StartAdvertising (StartAdvertisingOptions options);
 	public event EventHandler StateUpdated;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<p>Removed:</p><pre>
 	public abstract void UpdatedState (CBPeripheralManager peripheral);
</pre>
<p>Added:</p><pre>
 	public abstract void StateUpdated (CBPeripheralManager peripheral);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.StartAdvertisingOptions</h3>
<pre>
public class StartAdvertisingOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public StartAdvertisingOptions ();
	public StartAdvertisingOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public string LocalName {
		get;
		set;
	}
	public CBUUID[] ServicesUUID {
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreGraphics</h2>
<h3>Type Changed: MonoTouch.CoreGraphics.CGPDFPage</h3>
<p>Added:</p><pre>
 	public CGPDFPage (IntPtr handle);
 	
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>Type Changed: MonoTouch.CoreLocation.CLError</h3>
<p>Removed:</p><pre>
 	GeocodeCanceled
</pre>
<p>Added:</p><pre>
 	GeocodeCanceled,
 	DeferredFailed,
 	DeferredNotUpdatingLocation,
 	DeferredAccuracyTooLow,
 	DeferredDistanceFiltered,
 	DeferredCanceled
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h3>
<p>Added:</p><pre>
 	public virtual void AllowDeferredLocationUpdatesUntil (double distance, double timeout);
 	public virtual void DisallowDeferredLocationUpdates ();
 	public static bool DeferredLocationUpdatesAvailable {
 		get;
 	}
 	public static double MaxTimeInterval {
 		get;
 	}
 	public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; DeferredUpdatesFinished;
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DeferredUpdatesFinished (CLLocationManager manager, MonoTouch.Foundation.NSError error);
</pre>
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>Type Changed: MonoTouch.CoreMedia.CMSampleBufferAttachmentSettings</h3>
<p>Removed:</p><pre>
 public class CMSampleBufferAttachmentSettings {
 	public MonoTouch.Foundation.NSDictionary Dictionary {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 public class CMSampleBufferAttachmentSettings : MonoTouch.Foundation.DictionaryContainer {
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMTextMarkupAttributes</h3>
<pre>
public class CMTextMarkupAttributes : MonoTouch.Foundation.DictionaryContainer {
	
	public CMTextMarkupAttributes ();
	public CMTextMarkupAttributes (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<textmarkupcolor> BackgroundColor {
		get;
		set;
	}
	public Nullable<bool> Bold {
		get;
		set;
	}
	public string FontFamilyName {
		get;
		set;
	}
	public Nullable<textmarkupcolor> ForegroundColor {
		get;
		set;
	}
	public Nullable<bool> Italic {
		get;
		set;
	}
	public Nullable<int> RelativeFontSize {
		get;
		set;
	}
	public Nullable<bool> Underline {
		get;
		set;
	}
}
</bool></int></bool></textmarkupcolor></bool></textmarkupcolor></pre>
<h3>New Type: MonoTouch.CoreMedia.TextMarkupColor</h3>
<pre>
public struct TextMarkupColor {
	
	public TextMarkupColor (float red, float green, float blue, float alpha);
	
	public float Alpha {
		get;
	}
	public float Blue {
		get;
	}
	public float Green {
		get;
	}
	public float Red {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVPixelBuffer</h3>
<p>Removed:</p><pre>
 	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
</pre>
<p>Added:</p><pre>
 	public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);
 	[Obsolete("Use constructor with CVPixelBufferAttributes")]
	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
</pre>
<h3>New Type: MonoTouch.CoreVideo.CVPixelBufferAttributes</h3>
<pre>
public class CVPixelBufferAttributes : MonoTouch.Foundation.DictionaryContainer {
	
	public CVPixelBufferAttributes ();
	public CVPixelBufferAttributes (MonoTouch.Foundation.NSDictionary dictionary);
	public CVPixelBufferAttributes (CVPixelFormatType pixelFormatType, System.Drawing.Size size);
	
	public Nullable<int> BytesPerRowAlignment {
		get;
		set;
	}
	public Nullable<bool> CGBitmapContextCompatibility {
		get;
		set;
	}
	public Nullable<bool> CGImageCompatibility {
		get;
		set;
	}
	public Nullable<int> ExtendedPixelsBottom {
		get;
		set;
	}
	public Nullable<int> ExtendedPixelsLeft {
		get;
		set;
	}
	public Nullable<int> ExtendedPixelsRight {
		get;
		set;
	}
	public Nullable<int> ExtendedPixelsTop {
		get;
		set;
	}
	public Nullable<int> Height {
		get;
		set;
	}
	public MonoTouch.CoreFoundation.CFAllocator MemoryAllocator {
		set;
	}
	public Nullable<bool> OpenGLCompatibility {
		get;
		set;
	}
	public Nullable<bool> OpenGLESCompatibility {
		get;
		set;
	}
	public Nullable<cvpixelformattype> PixelFormatType {
		get;
		set;
	}
	public Nullable<int> PlaneAlignment {
		get;
		set;
	}
	public Nullable<int> Width {
		get;
		set;
	}
}
</int></int></cvpixelformattype></bool></bool></int></int></int></int></int></bool></bool></int></pre>
<h3>Type Changed: MonoTouch.CoreVideo.CVReturn</h3>
<p>Added:</p><pre>
 	WouldExceedAllocationThreshold,
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessory</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSData WakeToken {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager</h3>
<p>Removed:</p><pre>
 	public virtual void ShowBluetoothAccessoryPicker (MonoTouch.Foundation.NSPredicate nameFilterPredicate, System.Action&lt;MonoTouch.Foundation.NSError&gt; completion);
 	public virtual void WakeAccessoryWithToken (MonoTouch.Foundation.NSData wakeToken);
</pre>
<p>Added:</p><pre>
 	public virtual void ShowBluetoothAccessoryPicker (MonoTouch.Foundation.NSPredicate predicate, System.Action&lt;MonoTouch.Foundation.NSError&gt; completion);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>New Type: MonoTouch.Foundation.DictionaryContainer</h3>
<pre>
public abstract class DictionaryContainer {
	
	protected T[] GetArray<t> (NSString key) where T : NSObject;
	protected Nullable<bool> GetBoolValue (NSString key);
	protected Nullable<double> GetDoubleValue (NSString key);
	protected Nullable<float> GetFloatValue (NSString key);
	protected Nullable<int> GetInt32Value (NSString key);
	protected Nullable<long> GetLongValue (NSString key);
	protected string GetStringValue (NSString key);
	protected Nullable<uint> GetUIntValue (NSString key);
	protected void RemoveValue (NSString key);
	protected void SetArrayValue (NSString key, MonoTouch.ObjCRuntime.INativeObject[] values);
	protected void SetArrayValue (NSString key, NSNumber[] values);
	protected void SetArrayValue (NSString key, string [] values);
	protected void SetBooleanValue (NSString key, Nullable<bool> value);
	protected void SetNativeValue (NSString key, MonoTouch.ObjCRuntime.INativeObject value);
	protected void SetNumberValue (NSString key, Nullable<double> value);
	protected void SetNumberValue (NSString key, Nullable<float> value);
	protected void SetNumberValue (NSString key, Nullable<uint> value);
	protected void SetNumberValue (NSString key, Nullable<int> value);
	protected void SetNumberValue (NSString key, Nullable<long> value);
	protected void SetStringValue (NSString key, NSString value);
	protected void SetStringValue (NSString key, string value);
	
	public NSDictionary Dictionary {
		get;
	}
}
</long></int></uint></float></double></bool></uint></long></int></float></double></bool></t></pre>
<h3>Type Changed: MonoTouch.Foundation.NSCalendar</h3>
<p>Removed:</p><pre>
 	public NSCalendar (string identifier);
</pre>
<p>Added:</p><pre>
 	public NSCalendar (NSCalendarType calendarType);
 	public NSCalendar (NSString identifier);
</pre>
<h3>New Type: MonoTouch.Foundation.NSCalendarType</h3>
<pre>
[Serializable]
public enum NSCalendarType {
	Gregorian,
	Buddhist,
	Chinese,
	Hebrew,
	Islamic,
	IslamicCivil,
	Japanese,
	RepublicOfChina,
	Persian,
	Indian,
	ISO8601
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSTimer</h3>
<p>Added:</p><pre>
 	[Obsolete("This instance of NSTimer would be unusable. Symbol kept for binary compatibility")]
	public NSTimer ();
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatch</h3>
<p>Added:</p><pre>
 	public static void LoadMatch (string matchId, System.Action&lt;GKTurnBasedMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual void AcceptInvite (System.Action&lt;GKTurnBasedMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual void DeclineInvite (System.Action&lt;GKTurnBasedMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>
<h3>Type Removed: MonoTouch.MediaPlayer.MPMediaChapter</h3>
<h3>Type Removed: MonoTouch.MediaPlayer.MPMediaChapterType</h3>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaItem</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString ChaptersProperty {
 		get;
 	}
 	public MPMediaChapter[] Chapters {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static void void_objc_msgSend_Double_Double (IntPtr receiver, IntPtr selector, double arg1, double arg2);
 	public static void void_objc_msgSendSuper_Double_Double (IntPtr receiver, IntPtr selector, double arg1, double arg2);
</pre>
<h3>New Type: MonoTouch.ObjCRuntime.MountainLionAttribute</h3>
<pre>
public class MountainLionAttribute : Attribute {
	
	public MountainLionAttribute ();
}
</pre>
<h2>Namespace: MonoTouch.Social</h2>
<h3>Type Changed: MonoTouch.Social.SLComposeViewController</h3>
<p>Removed:</p><pre>
 	public static SLComposeViewController FromServiceType (MonoTouch.Foundation.NSString serviceType);
</pre>
<p>Added:</p><pre>
 	public static SLComposeViewController FromService (MonoTouch.Foundation.NSString serviceType);
 	public static SLComposeViewController FromService (SLServiceKind serviceKind);
 	public static bool IsAvailable (MonoTouch.Foundation.NSString serviceType);
 	public static bool IsAvailable (SLServiceKind serviceKind);
</pre>
<h3>Type Changed: MonoTouch.Social.SLRequest</h3>
<p>Added:</p><pre>
 	public static SLRequest Create (SLServiceKind serviceKind, SLRequestMethod method, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
</pre>
<h3>New Type: MonoTouch.Social.SLServiceKind</h3>
<pre>
[Serializable]
public enum SLServiceKind {
	Facebook,
	Twitter,
	SinaWeibo
}
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>Type Changed: MonoTouch.StoreKit.SKDownload</h3>
<p>Added:</p><pre>
 	public static double TimeRemainingUnknown {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.StoreKit.SKStoreProductParameterKey</h3>
<pre>
public static class SKStoreProductParameterKey {
	
	public static MonoTouch.Foundation.NSString ITunesItemIdentifier {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewController</h3>
<p>Removed:</p><pre>
 	public void LoadProduct (int iTunesItemIdentifier, System.Action&lt;bool,MonoTouch.Foundation.NSError&gt; callback);
 	public virtual void LoadProduct (MonoTouch.Foundation.NSDictionary parameters, System.Action&lt;bool,MonoTouch.Foundation.NSError&gt; callback);
 	public static MonoTouch.Foundation.NSString ITunesItemIdentifier {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public void LoadProduct (StoreProductParameters parameters, System.Action&lt;bool,MonoTouch.Foundation.NSError&gt; callback);
</pre>
<h3>New Type: MonoTouch.StoreKit.StoreProductParameters</h3>
<pre>
public class StoreProductParameters : MonoTouch.Foundation.DictionaryContainer {
	
	public StoreProductParameters ();
	public StoreProductParameters (MonoTouch.Foundation.NSDictionary dictionary);
	public StoreProductParameters (int iTunesItemIdentifier);
	
	public Nullable<int> ITunesItemIdentifier {
		get;
		set;
	}
}
</int></pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.NSMutableParagraphStyle</h3>
<p>Added:</p><pre>
 	public override float ParagraphSpacing {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSParagraphStyle</h3>
<p>Added:</p><pre>
 		set;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Removed:</p><pre>
 	public virtual void MoveSectiontoSection (int section, int newSection);
</pre>
<p>Added:</p><pre>
 	public virtual void MoveSection (int section, int newSection);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<p>Removed:</p><pre>
 	public virtual UIEdgeInsets GetInsetForItem (UICollectionView collectionView, UICollectionViewLayout layout, int section);
</pre>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets GetInsetForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Added:</p><pre>
 	public static UICollectionViewLayoutAttributes CreateForDecorationView (string decorationViewKind, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDevice</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSUuid IdentifierForAdvertising {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributes</h3>
<p>Removed:</p><pre>
 public class UIStringAttributes {
 	public MonoTouch.Foundation.NSDictionary Dictionary {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 public class UIStringAttributes : MonoTouch.Foundation.DictionaryContainer {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Removed:</p><pre>
 	public virtual void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
</pre>
<p>Added:</p><pre>
 	public void RegisterClassForHeaderFooterViewReuse (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
 	[Obsolete("Use RegisterNibForCellReuse")]
	public void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
 	public virtual void RegisterNibForCellReuse (UINib nib, string reuseIdentifier);
 	public virtual void RegisterNibForHeaderFooterViewReuse (UINib nib, string identifier);
</pre>
</body>
</html>
