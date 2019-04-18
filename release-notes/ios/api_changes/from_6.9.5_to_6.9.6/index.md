---
id: 9824960D-CE54-44E2-BB3F-229E0EEACCF1
title: "From 6.9.5 to 6.9.6"
---

<html><head><title>Comparison between monotouch-6.9.5.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.5";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.6";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Added:</p><pre>
 	public virtual AVAssetTrackGroup[] TrackGroups {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetExportSession</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
 		get;
 		set;
 	}
 	public virtual AVVideoCompositing CustomVideoCompositor {
 		get;
 	}
 	public virtual AVMetadataItemFilter MetadataItemFilter {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator</h3>
<p>Added:</p><pre>
 	public virtual AVVideoCompositing CustomVideoCompositor {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderTrackOutput</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput</h3>
<p>Added:</p><pre>
 	public virtual AVVideoCompositing CustomVideoCompositor {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate</h3>
<p>Removed:</p><pre>
 public abstract class AVAssetResourceLoaderDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class AVAssetResourceLoaderDelegate : MonoTouch.Foundation.NSObject, IAVAssetResourceLoaderDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate_Extensions</h3>
<pre>
public static class AVAssetResourceLoaderDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetTrack</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString[] AvailableTrackAssociationTypes {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetTrackGroup</h3>
<pre>
public class AVAssetTrackGroup : MonoTouch.Foundation.NSObject {
	
	public AVAssetTrackGroup ();
	public AVAssetTrackGroup (MonoTouch.Foundation.NSCoder coder);
	public AVAssetTrackGroup (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetTrackGroup (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] TrackIDs {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetTrackTrackAssociation</h3>
<pre>
public static class AVAssetTrackTrackAssociation {
	
	public static MonoTouch.Foundation.NSString GetAssociatedTracksOfType (AVAssetTrack This, MonoTouch.Foundation.NSString avAssetTrackTrackAssociationType);
	
	public static MonoTouch.Foundation.NSString AudioFallback {
		get;
	}
	public static MonoTouch.Foundation.NSString ChapterList {
		get;
	}
	public static MonoTouch.Foundation.NSString ForcedSubtitlesOnly {
		get;
	}
	public static MonoTouch.Foundation.NSString SelectionFollower {
		get;
	}
	public static MonoTouch.Foundation.NSString Timecode {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriter</h3>
<p>Added:</p><pre>
 	public virtual void AddInputGroup (AVAssetWriterInputGroup inputGroup);
 	public virtual bool CanAddInputGroup (AVAssetWriterInputGroup inputGroup);
 	public virtual AVAssetWriterInputGroup[] InputGroups {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput</h3>
<p>Added:</p><pre>
 	public virtual void AddTrackAssociationWithTrackOfInput (AVAssetWriterInput input, MonoTouch.Foundation.NSString trackAssociationType);
 	public virtual bool CanAddTrackAssociationWithTrackOfInput (AVAssetWriterInput input, MonoTouch.Foundation.NSString trackAssociationType);
 	public virtual string ExtendedLanguageTag {
 		get;
 		set;
 	}
 	public virtual string LanguageCode {
 		get;
 		set;
 	}
 	public virtual bool MarksOutputTrackAsEnabled {
 		get;
 		set;
 	}
 	public virtual System.Drawing.SizeF NaturalSize {
 		get;
 		set;
 	}
 	public virtual float PreferredVolume {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetWriterInputGroup</h3>
<pre>
public class AVAssetWriterInputGroup : AVMediaSelectionGroup {
	
	public AVAssetWriterInputGroup (MonoTouch.Foundation.NSCoder coder);
	public AVAssetWriterInputGroup (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetWriterInputGroup (IntPtr handle);
	public AVAssetWriterInputGroup (AVAssetWriterInput[] inputs, AVAssetWriterInput defaultInput);
	
	public static AVAssetWriterInputGroup Create (AVAssetWriterInput[] inputs, AVAssetWriterInput defaultInput);
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVAssetWriterInput DefaultInput {
		get;
	}
	public virtual AVAssetWriterInput[] Inputs {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading</h3>
<p>Removed:</p><pre>
 public abstract class AVAsynchronousKeyValueLoading : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class AVAsynchronousKeyValueLoading : MonoTouch.Foundation.NSObject, IAVAsynchronousKeyValueLoading {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading_Extensions</h3>
<pre>
public static class AVAsynchronousKeyValueLoading_Extensions {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAsynchronousVideoCompositionRequest</h3>
<pre>
public class AVAsynchronousVideoCompositionRequest : MonoTouch.Foundation.NSObject {
	
	public AVAsynchronousVideoCompositionRequest ();
	public AVAsynchronousVideoCompositionRequest (MonoTouch.Foundation.NSCoder coder);
	public AVAsynchronousVideoCompositionRequest (MonoTouch.Foundation.NSObjectFlag t);
	public AVAsynchronousVideoCompositionRequest (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual void FinishCancelledRequest ();
	public virtual void FinishWithComposedVideoFrame (MonoTouch.CoreVideo.CVPixelBuffer composedVideoFrame);
	public virtual void FinishWithError (MonoTouch.Foundation.NSError error);
	public virtual MonoTouch.CoreVideo.CVPixelBuffer SourceFrameByTrackID (int trackID);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime CompositionTime {
		get;
	}
	public virtual AVVideoCompositionRenderContext RenderContext {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] SourceTrackIDs {
		get;
	}
	public virtual AVVideoCompositionInstruction VideoCompositionInstruction {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioBitRateStrategy</h3>
<pre>
[Serializable]
public enum AVAudioBitRateStrategy {
	Constant,
	LongTermAverage,
	VariableConstrained,
	Variable
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayer</h3>
<p>Added:</p><pre>
 	public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, string fileTypeHint, out MonoTouch.Foundation.NSError outError);
 	public AVAudioPlayer (MonoTouch.Foundation.NSData data, string fileTypeHint, out MonoTouch.Foundation.NSError outError);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate</h3>
<p>Removed:</p><pre>
 public class AVAudioPlayerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVAudioPlayerDelegate : MonoTouch.Foundation.NSObject, IAVAudioPlayerDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioPlayerDelegate_Extensions</h3>
<pre>
public static class AVAudioPlayerDelegate_Extensions {
	
	public static void BeginInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player);
	public static void DecoderError (IAVAudioPlayerDelegate This, AVAudioPlayer player, MonoTouch.Foundation.NSError error);
	[Obsolete("Deprecated in iOS 6.0")]
	public static void EndInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player);
	public static void EndInterruption (IAVAudioPlayerDelegate This, AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
	public static void FinishedPlaying (IAVAudioPlayerDelegate This, AVAudioPlayer player, bool flag);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate</h3>
<p>Removed:</p><pre>
 public class AVAudioRecorderDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVAudioRecorderDelegate : MonoTouch.Foundation.NSObject, IAVAudioRecorderDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioRecorderDelegate_Extensions</h3>
<pre>
public static class AVAudioRecorderDelegate_Extensions {
	
	public static void BeginInterruption (IAVAudioRecorderDelegate This, AVAudioRecorder recorder);
	public static void EncoderError (IAVAudioRecorderDelegate This, AVAudioRecorder recorder, MonoTouch.Foundation.NSError error);
	[Obsolete("Deprecated in iOS 6.0")]
	public static void EndInterruption (IAVAudioRecorderDelegate This, AVAudioRecorder recorder);
	public static void EndInterruption (IAVAudioRecorderDelegate This, AVAudioRecorder recorder, AVAudioSessionInterruptionFlags flags);
	public static void FinishedRecording (IAVAudioRecorderDelegate This, AVAudioRecorder recorder, bool flag);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSession</h3>
<p>Added:</p><pre>
 	public virtual int GetPreferredInputNumberOfChannels ();
 	public virtual int GetPreferredOutputNumberOfChannels ();
 	public virtual void RequestRecordPermission (AVPermissionGranted responseCallback);
 	public virtual bool SetPreferredInput (AVAudioSessionPortDescription inPort, out MonoTouch.Foundation.NSError outError);
 	public virtual bool SetPreferredInputNumberOfChannels (int count, out MonoTouch.Foundation.NSError outError);
 	public virtual bool SetPreferredOutputNumberOfChannels (int count, out MonoTouch.Foundation.NSError outError);
 	public static MonoTouch.Foundation.NSString LocationLower {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LocationUpper {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MediaServicesWereLostNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ModeVideoChat {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OrientationBack {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OrientationBottom {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OrientationFront {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OrientationTop {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PolarPatternCardioid {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PolarPatternOmnidirectional {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PolarPatternSubcardioid {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PortBluetoothLE {
 		get;
 	}
 	public virtual AVAudioSessionPortDescription[] AvailableInputs {
 		get;
 	}
 	public virtual int MaximumInputNumberOfChannels {
 		get;
 	}
 	public virtual int MaximumOutputNumberOfChannels {
 		get;
 	}
 	public virtual AVAudioSessionPortDescription PreferredInput {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveMediaServicesWereLost (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSessionChannelDescription</h3>
<p>Added:</p><pre>
 	public virtual int ChannelLabel {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSessionDataSourceDescription</h3>
<p>Added:</p><pre>
 	public virtual bool SetPreferredPolarPattern (MonoTouch.Foundation.NSString pattern, out MonoTouch.Foundation.NSError outError);
 	public virtual string Location {
 		get;
 	}
 	public virtual string Orientation {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString PreferredPolarPattern {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString SelectedPolarPattern {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString[] SupportedPolarPatterns {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSessionDelegate</h3>
<p>Removed:</p><pre>
 public class AVAudioSessionDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVAudioSessionDelegate : MonoTouch.Foundation.NSObject, IAVAudioSessionDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionDelegate_Extensions</h3>
<pre>
public static class AVAudioSessionDelegate_Extensions {
	
	public static void BeginInterruption (IAVAudioSessionDelegate This);
	public static void EndInterruption (IAVAudioSessionDelegate This);
	public static void EndInterruption (IAVAudioSessionDelegate This, AVAudioSessionInterruptionFlags flags);
	public static void InputIsAvailableChanged (IAVAudioSessionDelegate This, bool isInputAvailable);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionErrorCode</h3>
<pre>
[Serializable]
public enum AVAudioSessionErrorCode {
	None,
	MediaServicesFailed,
	IsBusy,
	IncompatibleCategory,
	CannotInterruptOthers,
	MissingEntitlement,
	SiriIsRecording,
	CannotStartPlaying,
	BadParam,
	Unspecified
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSessionPortDescription</h3>
<p>Added:</p><pre>
 	public virtual bool SetPreferredDataSource (AVAudioSessionDataSourceDescription dataSource, out MonoTouch.Foundation.NSError outError);
 	public virtual AVAudioSessionChannelDescription[] DataSources {
 		get;
 	}
 	public virtual AVAudioSessionDataSourceDescription PreferredDataSource {
 		get;
 	}
 	public virtual AVAudioSessionDataSourceDescription SelectedDataSource {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSessionRouteChangeReason</h3>
<p>Removed:</p><pre>
 	NoSuitableRouteForCategory
</pre>
<p>Added:</p><pre>
 	NoSuitableRouteForCategory,
 	RouteConfigurationChange
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioTimePitchAlgorithm</h3>
<pre>
public static class AVAudioTimePitchAlgorithm {
	
	public static MonoTouch.Foundation.NSString LowQualityZeroLatency {
		get;
	}
	public static MonoTouch.Foundation.NSString Spectral {
		get;
	}
	public static MonoTouch.Foundation.NSString TimeDomain {
		get;
	}
	public static MonoTouch.Foundation.NSString Varispeed {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutput</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary GetRecommendedAudioSettingsForAssetWriter (string outputFileType);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate</h3>
<p>Removed:</p><pre>
 public class AVCaptureAudioDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVCaptureAudioDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject, IAVCaptureAudioDataOutputSampleBufferDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate_Extensions</h3>
<pre>
public static class AVCaptureAudioDataOutputSampleBufferDelegate_Extensions {
	
	public static void DidDropSampleBuffer (IAVCaptureAudioDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
	public static void DidOutputSampleBuffer (IAVCaptureAudioDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureAutoFocusRangeRestriction</h3>
<pre>
[Serializable]
public enum AVCaptureAutoFocusRangeRestriction {
	None,
	Near,
	Far
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureConnection</h3>
<p>Removed:</p><pre>
 	public bool SupportsVideoMaxFrameDuration {
 	public bool SupportsVideoMinFrameDuration {
 	public virtual MonoTouch.CoreMedia.CMTime VideoMaxFrameDuration {
 	public virtual MonoTouch.CoreMedia.CMTime VideoMinFrameDuration {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public bool SupportsVideoMaxFrameDuration {
 	[Obsolete("Deprecated in iOS7")]
	public bool SupportsVideoMinFrameDuration {
 	[Obsolete("Deprecated in iOS7")]
	public virtual MonoTouch.CoreMedia.CMTime VideoMaxFrameDuration {
 	[Obsolete("Deprecated in iOS7")]
	public virtual MonoTouch.CoreMedia.CMTime VideoMinFrameDuration {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureDevice</h3>
<p>Added:</p><pre>
 	public virtual void CancelVideoZoomRamp ();
 	protected override void Dispose (bool disposing);
 	public virtual void RampToVideoZoom (float factor, float rate);
 	public virtual AVCaptureDeviceFormat ActiveFormat {
 		get;
 		set;
 	}
 	public virtual MonoTouch.CoreMedia.CMTime ActiveVideoMaxFrameDuration {
 		get;
 		set;
 	}
 	public virtual MonoTouch.CoreMedia.CMTime ActiveVideoMinFrameDuration {
 		get;
 		set;
 	}
 	public virtual AVCaptureAutoFocusRangeRestriction AutoFocusRangeRestriction {
 		get;
 		set;
 	}
 	public virtual bool AutoFocusRangeRestrictionSupported {
 		get;
 	}
 	public virtual AVCaptureDeviceFormat[] Formats {
 		get;
 	}
 	public virtual bool RampingVideoZoom {
 		get;
 	}
 	public virtual bool SmoothAutoFocusEnabled {
 		get;
 		set;
 	}
 	public virtual bool SmoothAutoFocusSupported {
 		get;
 	}
 	public virtual float VideoZoomFactor {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureDeviceFormat</h3>
<pre>
public class AVCaptureDeviceFormat : MonoTouch.Foundation.NSObject {
	
	public AVCaptureDeviceFormat (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureDeviceFormat (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureDeviceFormat (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMFormatDescription FormatDescription {
		get;
	}
	public virtual MonoTouch.Foundation.NSString MediaType {
		get;
	}
	public virtual bool VideoBinned {
		get;
	}
	public virtual float VideoFieldOfView {
		get;
	}
	public virtual float VideoMaxZoomFactor {
		get;
	}
	public virtual bool VideoStabilizationSupported {
		get;
	}
	public virtual AVFrameRateRange[] VideoSupportedFrameRateRanges {
		get;
	}
	public virtual float VideoZoomFactorUpscaleThreshold {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate</h3>
<p>Removed:</p><pre>
 public class AVCaptureFileOutputRecordingDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVCaptureFileOutputRecordingDelegate : MonoTouch.Foundation.NSObject, IAVCaptureFileOutputRecordingDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions</h3>
<pre>
public static class AVCaptureFileOutputRecordingDelegate_Extensions {
	
	public static void DidStartRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections);
	public static void FinishedRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections, MonoTouch.Foundation.NSError error);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureInputPort</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreMedia.CMClock Clock {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureMetadataOutput</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSArray MetadataObjectTypes {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString[] MetadataObjectTypes {
 		get;
 		set;
 	}
 	public virtual System.Drawing.RectangleF RectOfInterest {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureMetadataOutputObjectsDelegate</h3>
<p>Removed:</p><pre>
 public class AVCaptureMetadataOutputObjectsDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVCaptureMetadataOutputObjectsDelegate : MonoTouch.Foundation.NSObject, IAVCaptureMetadataOutputObjectsDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureMetadataOutputObjectsDelegate_Extensions</h3>
<pre>
public static class AVCaptureMetadataOutputObjectsDelegate_Extensions {
	
	public static void DidOutputMetadataObjects (IAVCaptureMetadataOutputObjectsDelegate This, AVCaptureMetadataOutput captureOutput, AVMetadataObject[] metadataObjects, AVCaptureConnection connection);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureOutput</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF GetMetadataOutputRectOfInterestForRect (System.Drawing.RectangleF rectInOutputCoordinates);
 	public virtual System.Drawing.RectangleF GetRectForMetadataOutputRectOfInterest (System.Drawing.RectangleF rectInMetadataOutputCoordinates);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureSession</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString PresetInputPriority {
 		get;
 	}
 	public virtual bool AutomaticallyConfiguresApplicationAudioSession {
 		get;
 		set;
 	}
 	public virtual MonoTouch.CoreMedia.CMClock MasterClock {
 		get;
 	}
 	public virtual bool UsesApplicationAudioSession {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary GetRecommendedVideoSettingsForAssetWriter (string outputFileType);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate</h3>
<p>Removed:</p><pre>
 public class AVCaptureVideoDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVCaptureVideoDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject, IAVCaptureVideoDataOutputSampleBufferDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate_Extensions</h3>
<pre>
public static class AVCaptureVideoDataOutputSampleBufferDelegate_Extensions {
	
	public static void DidOutputSampleBuffer (IAVCaptureVideoDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVEdgeWidths</h3>
<pre>
public struct AVEdgeWidths {
	
	public AVEdgeWidths (float left, float top, float right, float bottom);
	
	public override bool Equals (object other);
	public override int GetHashCode ();
	public override string ToString ();
	
	public static bool operator == (AVEdgeWidths left, AVEdgeWidths right);
	public static bool operator != (AVEdgeWidths left, AVEdgeWidths right);
	
	public float Left;
	public float Top;
	public float Right;
	public float Bottom;
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVFileType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AC3 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MpegLayer3 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SunAU {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ThreeGpp2 {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVFrameRateRange</h3>
<pre>
public class AVFrameRateRange : MonoTouch.Foundation.NSObject {
	
	public AVFrameRateRange (MonoTouch.Foundation.NSCoder coder);
	public AVFrameRateRange (MonoTouch.Foundation.NSObjectFlag t);
	public AVFrameRateRange (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime MaxFrameDuration {
		get;
	}
	public virtual double MaxFrameRate {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime MinFrameDuration {
		get;
	}
	public virtual double MinFrameRate {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaSelectionOption</h3>
<p>Added:</p><pre>
 	public virtual string GetDisplayName (MonoTouch.Foundation.NSLocale locale);
 	public virtual string DisplayName {
 		get;
 	}
 	public virtual string ExtendedLanguageTag {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadataItem</h3>
<p>Added:</p><pre>
 	public static AVMetadataItem[] FilterWithItemFilter (AVMetadataItem[] metadataItems, AVMetadataItemFilter metadataItemFilter);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVMetadataItemFilter</h3>
<pre>
public class AVMetadataItemFilter : MonoTouch.Foundation.NSObject {
	
	public AVMetadataItemFilter ();
	public AVMetadataItemFilter (MonoTouch.Foundation.NSCoder coder);
	public AVMetadataItemFilter (MonoTouch.Foundation.NSObjectFlag t);
	public AVMetadataItemFilter (IntPtr handle);
	
	public static AVMetadataItemFilter ForSharing {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVMetadataMachineReadableCodeObject</h3>
<pre>
public class AVMetadataMachineReadableCodeObject : AVMetadataObject {
	
	public AVMetadataMachineReadableCodeObject ();
	public AVMetadataMachineReadableCodeObject (MonoTouch.Foundation.NSCoder coder);
	public AVMetadataMachineReadableCodeObject (MonoTouch.Foundation.NSObjectFlag t);
	public AVMetadataMachineReadableCodeObject (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary[] Corners {
		get;
	}
	public virtual string StringValue {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadataObject</h3>
<p>Removed:</p><pre>
 	public virtual string Type {
</pre>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	
 	public static MonoTouch.Foundation.NSString TypeAztecCode {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeCode128Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeCode39Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeCode39Mod43Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeCode93Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeEAN13Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeEAN8Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypePDF417Code {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeQRCode {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypeUPCECode {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString Type {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPermissionGranted</h3>
<pre>
[Serializable]
public delegate void AVPermissionGranted (bool granted);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPixelAspectRatio</h3>
<pre>
public struct AVPixelAspectRatio {
	
	public AVPixelAspectRatio (int horizontalSpacing, int verticalSpacing);
	
	public override bool Equals (object other);
	public override int GetHashCode ();
	public override string ToString ();
	
	public static bool operator == (AVPixelAspectRatio left, AVPixelAspectRatio right);
	public static bool operator != (AVPixelAspectRatio left, AVPixelAspectRatio right);
	
	public int HorizontalSpacing;
	public int VerticalSpacing;
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayer</h3>
<p>Added:</p><pre>
 	public virtual AVPlayerMediaSelectionCriteria MediaSelectionCriteriaForMediaCharacteristic (MonoTouch.Foundation.NSString avMediaCharacteristic);
 	public virtual void SetMediaSelectionCriteria (AVPlayerMediaSelectionCriteria criteria, MonoTouch.Foundation.NSString avMediaCharacteristic);
 	public virtual bool AppliesMediaSelectionCriteriaAutomatically {
 		get;
 		set;
 	}
 	public virtual bool Muted {
 		get;
 		set;
 	}
 	public virtual float Volume {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemOutputPullDelegate</h3>
<p>Removed:</p><pre>
 public class AVPlayerItemOutputPullDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVPlayerItemOutputPullDelegate : MonoTouch.Foundation.NSObject, IAVPlayerItemOutputPullDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemOutputPullDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemOutputPullDelegate_Extensions {
	
	public static void OutputMediaDataWillChange (IAVPlayerItemOutputPullDelegate This, AVPlayerItemOutput sender);
	public static void OutputSequenceWasFlushed (IAVPlayerItemOutputPullDelegate This, AVPlayerItemOutput output);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemTrack</h3>
<p>Added:</p><pre>
 	public virtual float CurrentVideoFrameRate {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF VideoRect {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerMediaSelectionCriteria</h3>
<pre>
public class AVPlayerMediaSelectionCriteria : MonoTouch.Foundation.NSObject {
	
	public AVPlayerMediaSelectionCriteria ();
	public AVPlayerMediaSelectionCriteria (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerMediaSelectionCriteria (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerMediaSelectionCriteria (IntPtr handle);
	public AVPlayerMediaSelectionCriteria (string [] preferredLanguages, MonoTouch.Foundation.NSString[] preferredMediaCharacteristics);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string [] PreferredLanguages {
		get;
	}
	public virtual MonoTouch.Foundation.NSString[] PreferredMediaCharacteristics {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSampleRateConverterAlgorithm</h3>
<pre>
[Serializable]
public enum AVSampleRateConverterAlgorithm {
	Normal,
	Mastering
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVSpeechSynthesizerDelegate</h3>
<p>Removed:</p><pre>
 public class AVSpeechSynthesizerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVSpeechSynthesizerDelegate : MonoTouch.Foundation.NSObject, IAVSpeechSynthesizerDelegate {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerDelegate_Extensions</h3>
<pre>
public static class AVSpeechSynthesizerDelegate_Extensions {
	
	public static void DidCancelSpeechUtterance (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public static void DidContinueSpeechUtterance (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public static void DidFinishSpeechUtterance (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public static void DidPauseSpeechUtterance (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public static void DidStartSpeechUtterance (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public static void WillSpeakRangeOfSpeechString (IAVSpeechSynthesizerDelegate This, AVSpeechSynthesizer synthesizer, MonoTouch.Foundation.NSRange characterRange, AVSpeechUtterance utterance);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCompositing</h3>
<pre>
public abstract class AVVideoCompositing : MonoTouch.Foundation.NSObject {
	
	public AVVideoCompositing ();
	public AVVideoCompositing (MonoTouch.Foundation.NSCoder coder);
	public AVVideoCompositing (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoCompositing (IntPtr handle);
	
	public virtual void CancelAllPendingVideoCompositionRequests ();
	public abstract void RenderContextChanged (AVVideoCompositionRenderContext newRenderContext);
	public abstract MonoTouch.Foundation.NSDictionary RequiredPixelBufferAttributesForRenderContext ();
	public abstract MonoTouch.Foundation.NSDictionary SourcePixelBufferAttributes ();
	public abstract void StartVideoCompositionRequest (AVAsynchronousVideoCompositionRequest asyncVideoCompositionRequest);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionInstruction</h3>
<p>Added:</p><pre>
 	public virtual bool ContainsTweening {
 		get;
 	}
 	public virtual int PassthroughTrackID {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSNumber[] RequiredSourceTrackIDs {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCompositionRenderContext</h3>
<pre>
public class AVVideoCompositionRenderContext : MonoTouch.Foundation.NSObject {
	
	public AVVideoCompositionRenderContext ();
	public AVVideoCompositionRenderContext (MonoTouch.Foundation.NSCoder coder);
	public AVVideoCompositionRenderContext (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoCompositionRenderContext (IntPtr handle);
	
	public virtual MonoTouch.CoreVideo.CVPixelBuffer CreatePixelBuffer ();
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVEdgeWidths EdgeWidths {
		get;
	}
	public virtual bool HighQualityRendering {
		get;
	}
	public virtual AVPixelAspectRatio PixelAspectRatio {
		get;
	}
	public virtual float RenderScale {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGAffineTransform RenderTransform {
		get;
	}
	public virtual System.Drawing.SizeF Size {
		get;
	}
	public virtual AVVideoComposition VideoComposition {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionValidationHandling</h3>
<p>Removed:</p><pre>
 public class AVVideoCompositionValidationHandling : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class AVVideoCompositionValidationHandling : MonoTouch.Foundation.NSObject, IAVVideoCompositionValidationHandling {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCompositionValidationHandling_Extensions</h3>
<pre>
public static class AVVideoCompositionValidationHandling_Extensions {
	
	public static bool ShouldContinueValidatingAfterFindingEmptyTimeRange (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, MonoTouch.CoreMedia.CMTimeRange timeRange);
	public static bool ShouldContinueValidatingAfterFindingInvalidTimeRangeInInstruction (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction);
	public static bool ShouldContinueValidatingAfterFindingInvalidTrackIDInInstruction (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction, AVVideoCompositionLayerInstruction layerInstruction, AVAsset asset);
	public static bool ShouldContinueValidatingAfterFindingInvalidValueForKey (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, string key);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AudioSettings</h3>
<p>Added:</p><pre>
 	public Nullable&lt;AVAudioBitRateStrategy&gt; BitRateStrategy {
 		get;
 		set;
 	}
 	public Nullable&lt;AVAudioQuality&gt; EncoderAudioQualityForVBR {
 		get;
 		set;
 	}
 	public Nullable&lt;AVSampleRateConverterAlgorithm&gt; SampleRateConverterAlgorithm {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVAssetResourceLoaderDelegate</h3>
<pre>
public interface IAVAssetResourceLoaderDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	bool ShouldWaitForLoadingOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVAsynchronousKeyValueLoading</h3>
<pre>
public interface IAVAsynchronousKeyValueLoading : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
	AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVAudioPlayerDelegate</h3>
<pre>
public interface IAVAudioPlayerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVAudioRecorderDelegate</h3>
<pre>
public interface IAVAudioRecorderDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVAudioSessionDelegate</h3>
<pre>
public interface IAVAudioSessionDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVCaptureAudioDataOutputSampleBufferDelegate</h3>
<pre>
public interface IAVCaptureAudioDataOutputSampleBufferDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVCaptureFileOutputRecordingDelegate</h3>
<pre>
public interface IAVCaptureFileOutputRecordingDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVCaptureMetadataOutputObjectsDelegate</h3>
<pre>
public interface IAVCaptureMetadataOutputObjectsDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVCaptureVideoDataOutputSampleBufferDelegate</h3>
<pre>
public interface IAVCaptureVideoDataOutputSampleBufferDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVPlayerItemOutputPullDelegate</h3>
<pre>
public interface IAVPlayerItemOutputPullDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVSpeechSynthesizerDelegate</h3>
<pre>
public interface IAVSpeechSynthesizerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVVideoCompositionValidationHandling</h3>
<pre>
public interface IAVVideoCompositionValidationHandling : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class ABNewPersonViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class ABNewPersonViewControllerDelegate : MonoTouch.Foundation.NSObject, IABNewPersonViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.AddressBookUI.ABNewPersonViewControllerDelegate_Extensions</h3>
<pre>
public static class ABNewPersonViewControllerDelegate_Extensions {
	
	public static void DidCompleteWithNewPerson (IABNewPersonViewControllerDelegate This, ABNewPersonViewController controller, IntPtr person);
}
</pre>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate</h3>
<p>Removed:</p><pre>
 public class ABPeoplePickerNavigationControllerDelegate : MonoTouch.UIKit.UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class ABPeoplePickerNavigationControllerDelegate : MonoTouch.UIKit.UINavigationControllerDelegate, IABPeoplePickerNavigationControllerDelegate {
</pre>
<h3>New Type: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions</h3>
<pre>
public static class ABPeoplePickerNavigationControllerDelegate_Extensions {
	
	public static void Cancelled (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson, int propertyId, int identifier);
}
</pre>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPersonViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class ABPersonViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class ABPersonViewControllerDelegate : MonoTouch.Foundation.NSObject, IABPersonViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.AddressBookUI.ABPersonViewControllerDelegate_Extensions</h3>
<pre>
public static class ABPersonViewControllerDelegate_Extensions {
	
	public static bool ShouldPerformDefaultActionForPerson (IABPersonViewControllerDelegate This, ABPersonViewController personViewController, IntPtr person, int propertyId, int identifier);
}
</pre>
<h3>Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class ABUnknownPersonViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class ABUnknownPersonViewControllerDelegate : MonoTouch.Foundation.NSObject, IABUnknownPersonViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.AddressBookUI.ABUnknownPersonViewControllerDelegate_Extensions</h3>
<pre>
public static class ABUnknownPersonViewControllerDelegate_Extensions {
	
	public static void DidResolveToPerson (IABUnknownPersonViewControllerDelegate This, ABUnknownPersonViewController unknownPersonView, IntPtr person);
	public static bool ShouldPerformDefaultActionForPerson (IABUnknownPersonViewControllerDelegate This, ABUnknownPersonViewController personViewController, IntPtr person, int propertyId, int identifier);
}
</pre>
<h3>New Type: MonoTouch.AddressBookUI.IABNewPersonViewControllerDelegate</h3>
<pre>
public interface IABNewPersonViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AddressBookUI.IABPeoplePickerNavigationControllerDelegate</h3>
<pre>
public interface IABPeoplePickerNavigationControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AddressBookUI.IABPersonViewControllerDelegate</h3>
<pre>
public interface IABPersonViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AddressBookUI.IABUnknownPersonViewControllerDelegate</h3>
<pre>
public interface IABUnknownPersonViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSession</h3>
<p>Removed:</p><pre>
 	public event EventHandler&lt;bool&gt; AudioInputBecameAvailable;
 	public event EventHandler&lt;float&gt; CurrentHardwareOutputVolumeChanged;
 	public event EventHandler&lt;bool&gt; InputGainBecameAvailable;
 	public event EventHandler&lt;float&gt; InputGainScalarChanged;
 	public event EventHandler&lt;AccessoryInfo[]&gt; InputSourcesChanged;
 	public event EventHandler&lt;AccessoryInfo[]&gt; OutputDestinationsChanged;
 	public event EventHandler&lt;bool&gt; ServerDied;
</pre>
<p>Added:</p><pre>
 	public event Action&lt;bool&gt; AudioInputBecameAvailable;
 	public event Action&lt;float&gt; CurrentHardwareOutputVolumeChanged;
 	public event Action&lt;bool&gt; InputGainBecameAvailable;
 	public event Action&lt;float&gt; InputGainScalarChanged;
 	public event Action&lt;AccessoryInfo[]&gt; InputSourcesChanged;
 	public event Action&lt;AccessoryInfo[]&gt; OutputDestinationsChanged;
 	public event Action&lt;bool&gt; ServerDied;
</pre>
<h2>Namespace: MonoTouch.CoreAnimation</h2>
<h3>Type Changed: MonoTouch.CoreAnimation.CAAction</h3>
<p>Removed:</p><pre>
 public class CAAction : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class CAAction : MonoTouch.Foundation.NSObject, ICAAction {
</pre>
<h3>New Type: MonoTouch.CoreAnimation.CAAction_Extensions</h3>
<pre>
public static class CAAction_Extensions {
	
	public static void RunAction (ICAAction This, string eventKey, MonoTouch.Foundation.NSObject obj, MonoTouch.Foundation.NSDictionary arguments);
}
</pre>
<h3>Type Changed: MonoTouch.CoreAnimation.CALayerDelegate</h3>
<p>Removed:</p><pre>
 public class CALayerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class CALayerDelegate : MonoTouch.Foundation.NSObject, ICALayerDelegate {
</pre>
<h3>New Type: MonoTouch.CoreAnimation.CALayerDelegate_Extensions</h3>
<pre>
public static class CALayerDelegate_Extensions {
	
	public static MonoTouch.Foundation.NSObject ActionForLayer (ICALayerDelegate This, CALayer layer, string eventKey);
	public static void DisplayLayer (ICALayerDelegate This, CALayer layer);
	public static void DrawLayer (ICALayerDelegate This, CALayer layer, MonoTouch.CoreGraphics.CGContext context);
	public static void LayoutSublayersOfLayer (ICALayerDelegate This, CALayer layer);
}
</pre>
<h3>New Type: MonoTouch.CoreAnimation.ICAAction</h3>
<pre>
public interface ICAAction : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.CoreAnimation.ICALayerDelegate</h3>
<pre>
public interface ICALayerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class CBCentralManagerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class CBCentralManagerDelegate : MonoTouch.Foundation.NSObject, ICBCentralManagerDelegate {
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBCentralManagerDelegate_Extensions</h3>
<pre>
public static class CBCentralManagerDelegate_Extensions {
	
	public static void ConnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral);
	public static void DisconnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
	public static void DiscoveredPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
	public static void FailedToConnectPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
	public static void RetrievedConnectedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);
	public static void RetrievedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);
	public static void WillRestoreState (ICBCentralManagerDelegate This, CBCentralManager central, MonoTouch.Foundation.NSDictionary dict);
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 public class CBPeripheralDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class CBPeripheralDelegate : MonoTouch.Foundation.NSObject, ICBPeripheralDelegate {
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralDelegate_Extensions</h3>
<pre>
public static class CBPeripheralDelegate_Extensions {
	
	public static void DiscoverCharacteristic (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, MonoTouch.Foundation.NSError error);
	public static void DiscoveredDescriptor (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
	public static void DiscoveredIncludedService (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, MonoTouch.Foundation.NSError error);
	public static void DiscoveredService (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
	[Obsolete("Deprecated in iOS7")]
	public static void InvalidatedService (ICBPeripheralDelegate This, CBPeripheral peripheral);
	public static void ModifiedServices (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService[] services);
	public static void RssiUpdated (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
	public static void UpdatedCharacterteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
	public static void UpdatedName (ICBPeripheralDelegate This, CBPeripheral peripheral);
	public static void UpdatedNotificationState (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
	public static void UpdatedValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, MonoTouch.Foundation.NSError error);
	public static void WroteCharacteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
	public static void WroteDescriptorValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, MonoTouch.Foundation.NSError error);
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class CBPeripheralManagerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class CBPeripheralManagerDelegate : MonoTouch.Foundation.NSObject, ICBPeripheralManagerDelegate {
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate_Extensions</h3>
<pre>
public static class CBPeripheralManagerDelegate_Extensions {
	
	public static void AdvertisingStarted (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, MonoTouch.Foundation.NSError error);
	public static void CharacteristicSubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public static void CharacteristicUnsubscribed (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
	public static void ReadRequestReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest request);
	public static void ReadyToUpdateSubscribers (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral);
	public static void ServiceAdded (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBService service, MonoTouch.Foundation.NSError error);
	public static void WillRestoreState (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, MonoTouch.Foundation.NSDictionary dict);
	public static void WriteRequestsReceived (ICBPeripheralManagerDelegate This, CBPeripheralManager peripheral, CBATTRequest[] requests);
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.ICBCentralManagerDelegate</h3>
<pre>
public interface ICBCentralManagerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void UpdatedState (CBCentralManager central);
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.ICBPeripheralDelegate</h3>
<pre>
public interface ICBPeripheralDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.ICBPeripheralManagerDelegate</h3>
<pre>
public interface ICBPeripheralManagerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void StateUpdated (CBPeripheralManager peripheral);
}
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>New Type: MonoTouch.CoreData.INSFetchedResultsControllerDelegate</h3>
<pre>
public interface INSFetchedResultsControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.CoreData.INSFetchedResultsSectionInfo</h3>
<pre>
public interface INSFetchedResultsSectionInfo : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.CoreData.NSFetchedResultsController</h3>
<p>Removed:</p><pre>
 	public virtual NSFetchedResultsSectionInfo[] Sections {
</pre>
<p>Added:</p><pre>
 	public virtual INSFetchedResultsSectionInfo[] Sections {
</pre>
<h3>Type Changed: MonoTouch.CoreData.NSFetchedResultsControllerDelegate</h3>
<p>Removed:</p><pre>
 public class NSFetchedResultsControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSFetchedResultsControllerDelegate : MonoTouch.Foundation.NSObject, INSFetchedResultsControllerDelegate {
</pre>
<h3>New Type: MonoTouch.CoreData.NSFetchedResultsControllerDelegate_Extensions</h3>
<pre>
public static class NSFetchedResultsControllerDelegate_Extensions {
	
	public static void DidChangeContent (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller);
	public static void DidChangeObject (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller, MonoTouch.Foundation.NSObject anObject, MonoTouch.Foundation.NSIndexPath indexPath, NSFetchedResultsChangeType type, MonoTouch.Foundation.NSIndexPath newIndexPath);
	public static void DidChangeSection (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller, NSFetchedResultsSectionInfo sectionInfo, uint sectionIndex, NSFetchedResultsChangeType type);
	public static string SectionFor (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller, string sectionName);
	public static void WillChangeContent (INSFetchedResultsControllerDelegate This, NSFetchedResultsController controller);
}
</pre>
<h3>Type Changed: MonoTouch.CoreData.NSFetchedResultsSectionInfo</h3>
<p>Removed:</p><pre>
 public class NSFetchedResultsSectionInfo : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSFetchedResultsSectionInfo : MonoTouch.Foundation.NSObject, INSFetchedResultsSectionInfo {
</pre>
<h3>New Type: MonoTouch.CoreData.NSFetchedResultsSectionInfo_Extensions</h3>
<pre>
public static class NSFetchedResultsSectionInfo_Extensions {
}
</pre>
<h2>Namespace: MonoTouch.CoreGraphics</h2>
<h3>New Type: MonoTouch.CoreGraphics.CGVector</h3>
<pre>
public struct CGVector {
	
	public CGVector (float dx, float dy);
	
	public override bool Equals (object other);
	public override int GetHashCode ();
	public override string ToString ();
	
	public static bool operator == (CGVector left, CGVector right);
	public static bool operator != (CGVector left, CGVector right);
	
	public float dx;
	public float dy;
}
</pre>
<h2>Namespace: MonoTouch.EventKitUI</h2>
<h3>Type Changed: MonoTouch.EventKitUI.EKCalendarChooserDelegate</h3>
<p>Removed:</p><pre>
 public class EKCalendarChooserDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class EKCalendarChooserDelegate : MonoTouch.Foundation.NSObject, IEKCalendarChooserDelegate {
</pre>
<h3>New Type: MonoTouch.EventKitUI.EKCalendarChooserDelegate_Extensions</h3>
<pre>
public static class EKCalendarChooserDelegate_Extensions {
	
	public static void Cancelled (IEKCalendarChooserDelegate This, EKCalendarChooser calendarChooser);
	public static void Finished (IEKCalendarChooserDelegate This, EKCalendarChooser calendarChooser);
	public static void SelectionChanged (IEKCalendarChooserDelegate This, EKCalendarChooser calendarChooser);
}
</pre>
<h3>Type Changed: MonoTouch.EventKitUI.EKEventEditViewDelegate</h3>
<p>Removed:</p><pre>
 public abstract class EKEventEditViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class EKEventEditViewDelegate : MonoTouch.Foundation.NSObject, IEKEventEditViewDelegate {
</pre>
<h3>New Type: MonoTouch.EventKitUI.EKEventEditViewDelegate_Extensions</h3>
<pre>
public static class EKEventEditViewDelegate_Extensions {
	
	public static MonoTouch.EventKit.EKCalendar GetDefaultCalendarForNewEvents (IEKEventEditViewDelegate This, EKEventEditViewController controller);
}
</pre>
<h3>Type Changed: MonoTouch.EventKitUI.EKEventViewDelegate</h3>
<p>Removed:</p><pre>
 public abstract class EKEventViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class EKEventViewDelegate : MonoTouch.Foundation.NSObject, IEKEventViewDelegate {
</pre>
<h3>New Type: MonoTouch.EventKitUI.EKEventViewDelegate_Extensions</h3>
<pre>
public static class EKEventViewDelegate_Extensions {
}
</pre>
<h3>New Type: MonoTouch.EventKitUI.IEKCalendarChooserDelegate</h3>
<pre>
public interface IEKCalendarChooserDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.EventKitUI.IEKEventEditViewDelegate</h3>
<pre>
public interface IEKEventEditViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void Completed (EKEventEditViewController controller, MonoTouch.EventKit.EKEventEditViewAction action);
}
</pre>
<h3>New Type: MonoTouch.EventKitUI.IEKEventViewDelegate</h3>
<pre>
public interface IEKEventViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void Completed (EKEventViewController controller, MonoTouch.EventKit.EKEventViewAction action);
}
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryDelegate</h3>
<p>Removed:</p><pre>
 public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject, IEAAccessoryDelegate {
</pre>
<h3>New Type: MonoTouch.ExternalAccessory.EAAccessoryDelegate_Extensions</h3>
<pre>
public static class EAAccessoryDelegate_Extensions {
	
	public static void Disconnected (IEAAccessoryDelegate This, EAAccessory accessory);
}
</pre>
<h3>New Type: MonoTouch.ExternalAccessory.IEAAccessoryDelegate</h3>
<pre>
public interface IEAAccessoryDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>New Type: MonoTouch.Foundation.INSCacheDelegate</h3>
<pre>
public interface INSCacheDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSFileManagerDelegate</h3>
<pre>
public interface INSFileManagerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSFilePresenter</h3>
<pre>
public interface INSFilePresenter : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	NSUrl PresentedItemURL {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSKeyedArchiverDelegate</h3>
<pre>
public interface INSKeyedArchiverDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSKeyedUnarchiverDelegate</h3>
<pre>
public interface INSKeyedUnarchiverDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSMetadataQueryDelegate</h3>
<pre>
public interface INSMetadataQueryDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSNetServiceBrowserDelegate</h3>
<pre>
public interface INSNetServiceBrowserDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSNetServiceDelegate</h3>
<pre>
public interface INSNetServiceDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSStreamDelegate</h3>
<pre>
public interface INSStreamDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlConnectionDelegate</h3>
<pre>
public interface INSUrlConnectionDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlConnectionDownloadDelegate</h3>
<pre>
public interface INSUrlConnectionDownloadDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void FinishedDownloading (NSUrlConnection connection, NSUrl destinationUrl);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSArray</h3>
<p>Removed:</p><pre>
 	public static T[] ArrayFromHandle&lt;T&gt; (IntPtr handle) where T : NSObject;
</pre>
<p>Added:</p><pre>
 	public static T[] ArrayFromHandle&lt;T&gt; (IntPtr handle) where T : class;
 	public static NSArray FromNSObjects (params MonoTouch.ObjCRuntime.INativeObject[] items);
 	public static NSArray FromNSObjects (int count, params MonoTouch.ObjCRuntime.INativeObject[] items);
 	public T GetItem&lt;T&gt; (int index) where T : class;
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSCacheDelegate</h3>
<p>Removed:</p><pre>
 public class NSCacheDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSCacheDelegate : NSObject, INSCacheDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSCacheDelegate_Extensions</h3>
<pre>
public static class NSCacheDelegate_Extensions {
	
	public static void WillEvictObject (INSCacheDelegate This, NSCache cache, NSObject obj);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSCalendar</h3>
<p>Removed:</p><pre>
 	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);
 	public virtual NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);
</pre>
<p>Added:</p><pre>
 	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSCalendarOptions opts);
 	public NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);
 	public virtual NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSCalendarOptions opts);
 	public NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);
</pre>
<h3>New Type: MonoTouch.Foundation.NSCalendarOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSCalendarOptions {
	None,
	WrapCalendarComponents,
	MatchStrictly,
	SearchBackwards,
	MatchPreviousTimePreservingSmallerUnits,
	MatchNextTimePreservingSmallerUnits,
	MatchNextTime,
	MatchFirst,
	MatchLast
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSData</h3>
<p>Added:</p><pre>
 	public NSData (IntPtr bytes, uint length, Action&lt;IntPtr,uint&gt; deallocator);
 	public static NSData FromBytesNoCopy (IntPtr bytes, uint size);
 	public static NSData FromBytesNoCopy (IntPtr bytes, uint size, bool freeWhenDone);
 	public virtual void EnumerateByteRange (NSDataByteRangeEnumerator enumerator);
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataByteRangeEnumerator</h3>
<pre>
[Serializable]
public delegate void NSDataByteRangeEnumerator (IntPtr bytes, NSRange range, ref bool stop);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDateComponentsWrappingBehavior</h3>
<p>Removed:</p><pre>
 	WrapCalendarComponents,
 	MatchStrictly,
 	SearchBackwards,
 	MatchPreviousTimePreservingSmallerUnits,
 	MatchNextTimePreservingSmallerUnits,
 	MatchNextTime,
 	MatchFirst,
 	MatchLast
</pre>
<p>Added:</p><pre>
 [Flags]
 	WrapCalendarComponents
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFileManagerDelegate</h3>
<p>Removed:</p><pre>
 public class NSFileManagerDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSFileManagerDelegate : NSObject, INSFileManagerDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSFileManagerDelegate_Extensions</h3>
<pre>
public static class NSFileManagerDelegate_Extensions {
	
	public static bool ShouldCopyItemAtPath (INSFileManagerDelegate This, NSFileManager fm, NSString srcPath, NSString dstPath);
	public static bool ShouldCopyItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldLinkItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldMoveItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldProceedAfterError (INSFileManagerDelegate This, NSFileManager fm, NSDictionary errorInfo);
	public static bool ShouldProceedAfterErrorCopyingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorLinkingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorMovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorRemovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string path);
	public static bool ShouldRemoveItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string path);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFilePresenter</h3>
<p>Removed:</p><pre>
 public abstract class NSFilePresenter : NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class NSFilePresenter : NSObject, INSFilePresenter {
</pre>
<h3>New Type: MonoTouch.Foundation.NSFilePresenter_Extensions</h3>
<pre>
public static class NSFilePresenter_Extensions {
	
	public static void PresentedItemChanged (INSFilePresenter This);
	public static void PresentedItemGainedVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedItemLostVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedItemMoved (INSFilePresenter This, NSUrl newURL);
	public static void PresentedItemResolveConflictVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedSubitemAppeared (INSFilePresenter This, NSUrl atUrl);
	public static void PresentedSubitemChanged (INSFilePresenter This, NSUrl url);
	public static void PresentedSubitemGainedVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
	public static void PresentedSubitemLostVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
	public static void PresentedSubitemMoved (INSFilePresenter This, NSUrl oldURL, NSUrl newURL);
	public static void PresentedSubitemResolvedConflictVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSKeyedArchiver</h3>
<p>Added:</p><pre>
 	public virtual void SetRequiresSecureCoding (bool requireSecureEncoding);
 	public static NSString RootObjectKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSKeyedArchiverDelegate</h3>
<p>Removed:</p><pre>
 public class NSKeyedArchiverDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSKeyedArchiverDelegate : NSObject, INSKeyedArchiverDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSKeyedArchiverDelegate_Extensions</h3>
<pre>
public static class NSKeyedArchiverDelegate_Extensions {
	
	public static void EncodedObject (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject obj);
	public static void Finished (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver);
	public static void Finishing (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver);
	public static void ReplacingObject (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject oldObject, NSObject newObject);
	public static NSObject WillEncode (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject obj);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSKeyedUnarchiver</h3>
<p>Added:</p><pre>
 	public virtual void SetRequiresSecureCoding (bool requireSecureEncoding);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSKeyedUnarchiverDelegate</h3>
<p>Removed:</p><pre>
 public class NSKeyedUnarchiverDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSKeyedUnarchiverDelegate : NSObject, INSKeyedUnarchiverDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSKeyedUnarchiverDelegate_Extensions</h3>
<pre>
public static class NSKeyedUnarchiverDelegate_Extensions {
	
	public static MonoTouch.ObjCRuntime.Class CannotDecodeClass (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, string klass, string [] classes);
	public static NSObject DecodedObject (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, NSObject obj);
	public static void Finished (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver);
	public static void Finishing (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver);
	public static void ReplacingObject (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, NSObject oldObject, NSObject newObject);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMetadataQueryDelegate</h3>
<p>Removed:</p><pre>
 public class NSMetadataQueryDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSMetadataQueryDelegate : NSObject, INSMetadataQueryDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSMetadataQueryDelegate_Extensions</h3>
<pre>
public static class NSMetadataQueryDelegate_Extensions {
	
	public static NSObject ReplacementObjectForResultObject (INSMetadataQueryDelegate This, NSMetadataQuery query, NSMetadataItem result);
	public static NSObject ReplacementValueForAttributevalue (INSMetadataQueryDelegate This, NSMetadataQuery query, string attributeName, NSObject value);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNetService</h3>
<p>Added:</p><pre>
 	public virtual bool IncludesPeerToPeer {
 		get;
 		set;
 	}
 	public event EventHandler&lt;NSNetServiceConnectionEventArgs&gt; DidAcceptConnection;
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNetServiceBrowser</h3>
<p>Added:</p><pre>
 	public virtual bool IncludesPeerToPeer {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNetServiceBrowserDelegate</h3>
<p>Removed:</p><pre>
 public class NSNetServiceBrowserDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSNetServiceBrowserDelegate : NSObject, INSNetServiceBrowserDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSNetServiceBrowserDelegate_Extensions</h3>
<pre>
public static class NSNetServiceBrowserDelegate_Extensions {
	
	public static void DomainRemoved (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, string domain, bool moreComing);
	public static void FoundDomain (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, string domain, bool moreComing);
	public static void FoundService (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSNetService service, bool moreComing);
	public static void NotSearched (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSDictionary errors);
	public static void SearchStarted (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender);
	public static void SearchStopped (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender);
	public static void ServiceRemoved (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSNetService service, bool moreComing);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSNetServiceConnectionEventArgs</h3>
<pre>
public class NSNetServiceConnectionEventArgs : EventArgs {
	
	public NSNetServiceConnectionEventArgs (NSInputStream inputStream, NSOutputStream outputStream);
	
	public NSInputStream InputStream {
		get;
		set;
	}
	public NSOutputStream OutputStream {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNetServiceDelegate</h3>
<p>Removed:</p><pre>
 public class NSNetServiceDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSNetServiceDelegate : NSObject, INSNetServiceDelegate {
 	public virtual void DidAcceptConnection (NSNetService sender, NSInputStream inputStream, NSOutputStream outputStream);
</pre>
<h3>New Type: MonoTouch.Foundation.NSNetServiceDelegate_Extensions</h3>
<pre>
public static class NSNetServiceDelegate_Extensions {
	
	public static void AddressResolved (INSNetServiceDelegate This, NSNetService sender);
	public static void DidAcceptConnection (INSNetServiceDelegate This, NSNetService sender, NSInputStream inputStream, NSOutputStream outputStream);
	public static void Published (INSNetServiceDelegate This, NSNetService sender);
	public static void PublishFailure (INSNetServiceDelegate This, NSNetService sender, NSDictionary errors);
	public static void ResolveFailure (INSNetServiceDelegate This, NSNetService sender, NSDictionary errors);
	public static void Stopped (INSNetServiceDelegate This, NSNetService sender);
	public static void UpdatedTxtRecordData (INSNetServiceDelegate This, NSNetService sender, NSData data);
	public static void WillPublish (INSNetServiceDelegate This, NSNetService sender);
	public static void WillResolve (INSNetServiceDelegate This, NSNetService sender);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNetServiceOptions</h3>
<p>Removed:</p><pre>
 	NoAutoRename
</pre>
<p>Added:</p><pre>
 [Flags]
 	NoAutoRename,
 	ListenForConnections
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSStreamDelegate</h3>
<p>Removed:</p><pre>
 public class NSStreamDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSStreamDelegate : NSObject, INSStreamDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSStreamDelegate_Extensions</h3>
<pre>
public static class NSStreamDelegate_Extensions {
	
	public static void HandleEvent (INSStreamDelegate This, NSStream theStream, NSStreamEvent streamEvent);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlConnectionDelegate</h3>
<p>Removed:</p><pre>
 public class NSUrlConnectionDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSUrlConnectionDelegate : NSObject, INSUrlConnectionDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlConnectionDelegate_Extensions</h3>
<pre>
public static class NSUrlConnectionDelegate_Extensions {
	
	public static bool CanAuthenticateAgainstProtectionSpace (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlProtectionSpace protectionSpace);
	public static void CanceledAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public static bool ConnectionShouldUseCredentialStorage (INSUrlConnectionDelegate This, NSUrlConnection connection);
	public static void FailedWithError (INSUrlConnectionDelegate This, NSUrlConnection connection, NSError error);
	public static void FinishedLoading (INSUrlConnectionDelegate This, NSUrlConnection connection);
	public static NSInputStream NeedNewBodyStream (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request);
	public static void ReceivedAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public static void ReceivedData (INSUrlConnectionDelegate This, NSUrlConnection connection, NSData data);
	public static void ReceivedResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlResponse response);
	public static void SentBodyData (INSUrlConnectionDelegate This, NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public static NSCachedUrlResponse WillCacheResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public static NSUrlRequest WillSendRequest (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlConnectionDownloadDelegate</h3>
<p>Removed:</p><pre>
 public abstract class NSUrlConnectionDownloadDelegate : NSUrlConnectionDelegate {
</pre>
<p>Added:</p><pre>
 public abstract class NSUrlConnectionDownloadDelegate : NSUrlConnectionDelegate, INSUrlConnectionDownloadDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlConnectionDownloadDelegate_Extensions</h3>
<pre>
public static class NSUrlConnectionDownloadDelegate_Extensions {
	
	public static void ResumedDownloading (INSUrlConnectionDownloadDelegate This, NSUrlConnection connection, long totalBytesWritten, long expectedTotalBytes);
	public static void WroteData (INSUrlConnectionDownloadDelegate This, NSUrlConnection connection, long bytesWritten, long totalBytesWritten, long expectedTotalBytes);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSession</h3>
<pre>
public class NSUrlSession : NSObject {
	
	public NSUrlSession ();
	public NSUrlSession (NSCoder coder);
	public NSUrlSession (NSObjectFlag t);
	public NSUrlSession (IntPtr handle);
	
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration);
	public static NSUrlSession FromConfiguration (NSUrlSessionConfiguration configuration, NSUrlSessionDelegate sessionDelegate, NSOperationQueue delegateQueue);
	public static NSUrlSession FromWeakConfiguration (NSUrlSessionConfiguration configuration, NSObject weakDelegate, NSOperationQueue delegateQueue);
	public virtual NSUrlSessionDataTask DataTaskWithRequest (NSUrlRequest request);
	public virtual NSUrlSessionDataTask DataTaskWithRequest (NSUrlRequest request, Action<nsdata,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondatataskrequest> DataTaskWithRequestAsync (NSUrlRequest request);
	public virtual NSUrlSessionDataTask DataTaskWithURL (NSUrl url);
	public virtual NSUrlSessionDataTask DataTaskWithURL (NSUrl url, Action<nsdata,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondatataskrequest> DataTaskWithURLAsync (NSUrl url);
	protected override void Dispose (bool disposing);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithRequest (NSUrlRequest request);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithRequest (NSUrlRequest request, Action<nsurl,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondownloadtaskrequest> DownloadTaskWithRequestAsync (NSUrlRequest request);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithResumeData (NSData resumeData);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithResumeData (NSData resumeData, Action<nsurl,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondownloadtaskrequest> DownloadTaskWithResumeDataAsync (NSData resumeData);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithURL (NSUrl url);
	public virtual NSUrlSessionDownloadTask DownloadTaskWithURL (NSUrl url, Action<nsurl,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondownloadtaskrequest> DownloadTaskWithURLAsync (NSUrl url);
	public virtual void FinishTasksAndInvalidate ();
	public virtual void Flush (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task FlushAsync ();
	public virtual void GetTasks (Action<nsurlsessiondatatask[],nsurlsessionuploadtask[],nsurlsessiondownloadtask[]> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessionactivetasks> GetTasksAsync ();
	public virtual void InvalidateAndCancel ();
	public virtual void Reset (NSAction completionHandler);
	public virtual System.Threading.Tasks.Task ResetAsync ();
	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSData bodyData);
	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSData bodyData, Action<nsdata,nsurlresponse,nserror> completionHandler);
	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSUrl fileURL);
	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSUrl fileURL, Action<nsdata,nsurlresponse,nserror> completionHandler);
	public virtual System.Threading.Tasks.Task<nsurlsessiondatataskrequest> UploadTaskWithRequestAsync (NSUrlRequest request, NSData bodyData);
	public virtual System.Threading.Tasks.Task<nsurlsessiondatataskrequest> UploadTaskWithRequestAsync (NSUrlRequest request, NSUrl fileURL);
	public virtual NSUrlSessionUploadTask UploadTaskWithStreamedRequest (NSUrlRequest request);
	
	public static NSUrlSession SharedSession {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSUrlSessionConfiguration Configuration {
		get;
	}
	public NSUrlSessionDelegate Delegate {
		get;
	}
	public virtual NSOperationQueue DelegateQueue {
		get;
	}
	public virtual string SessionDescription {
		get;
		set;
	}
	public virtual NSObject WeakDelegate {
		get;
	}
}
</nsurlsessiondatataskrequest></nsurlsessiondatataskrequest></nsdata,nsurlresponse,nserror></nsdata,nsurlresponse,nserror></nsurlsessionactivetasks></nsurlsessiondatatask[],nsurlsessionuploadtask[],nsurlsessiondownloadtask[]></nsurlsessiondownloadtaskrequest></nsurl,nsurlresponse,nserror></nsurlsessiondownloadtaskrequest></nsurl,nsurlresponse,nserror></nsurlsessiondownloadtaskrequest></nsurl,nsurlresponse,nserror></nsurlsessiondatataskrequest></nsdata,nsurlresponse,nserror></nsurlsessiondatataskrequest></nsdata,nsurlresponse,nserror></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionActiveTasks</h3>
<pre>
public class NSUrlSessionActiveTasks {
	
	public NSUrlSessionActiveTasks (NSUrlSessionDataTask[] arg1, NSUrlSessionUploadTask[] arg2, NSUrlSessionDownloadTask[] arg3);
	
	public NSUrlSessionDataTask[] Arg1 {
		get;
		set;
	}
	public NSUrlSessionUploadTask[] Arg2 {
		get;
		set;
	}
	public NSUrlSessionDownloadTask[] Arg3 {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionAuthChallengeDisposition</h3>
<pre>
[Serializable]
public enum NSUrlSessionAuthChallengeDisposition {
	UseCredential,
	PerformDefaultHandling,
	CancelAuthenticationChallenge,
	RejectProtectionSpace
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionConfiguration</h3>
<pre>
public class NSUrlSessionConfiguration : NSObject {
	
	public NSUrlSessionConfiguration ();
	public NSUrlSessionConfiguration (NSCoder coder);
	public NSUrlSessionConfiguration (NSObjectFlag t);
	public NSUrlSessionConfiguration (IntPtr handle);
	
	public static NSUrlSessionConfiguration BackgroundSessionConfiguration (string identifier);
	protected override void Dispose (bool disposing);
	
	public static NSUrlSessionConfiguration DefaultSessionConfiguration {
		get;
	}
	public static NSUrlSessionConfiguration EphemeralSessionConfiguration {
		get;
	}
	public virtual bool AllowsCellularAccess {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSDictionary ConnectionProxyDictionary {
		get;
		set;
	}
	public virtual bool Discretionary {
		get;
		set;
	}
	public virtual NSDictionary HttpAdditionalHeaders {
		get;
		set;
	}
	public virtual NSHttpCookieAcceptPolicy HttpCookieAcceptPolicy {
		get;
		set;
	}
	public virtual NSHttpCookieStorage HttpCookieStorage {
		get;
		set;
	}
	public virtual int HttpMaximumConnectionsPerHost {
		get;
		set;
	}
	public virtual bool HttpShouldSetCookies {
		get;
		set;
	}
	public virtual bool HttpShouldUsePipelining {
		get;
		set;
	}
	public virtual string Identifier {
		get;
	}
	public virtual NSUrlRequestNetworkServiceType NetworkServiceType {
		get;
		set;
	}
	public virtual NSUrlRequestCachePolicy RequestCachePolicy {
		get;
		set;
	}
	public virtual bool SessionSendsLaunchEvents {
		get;
		set;
	}
	public virtual double TimeoutIntervalForRequest {
		get;
		set;
	}
	public virtual double TimeoutIntervalForResource {
		get;
		set;
	}
	public virtual MonoTouch.Security.SslProtocol TLSMaximumSupportedProtocol {
		get;
		set;
	}
	public virtual MonoTouch.Security.SslProtocol TLSMinimumSupportedProtocol {
		get;
		set;
	}
	public virtual NSUrlCache URLCache {
		get;
		set;
	}
	public virtual NSUrlCredentialStorage URLCredentialStorage {
		get;
		set;
	}
	public virtual NSArray WeakProtocolClasses {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDataDelegate</h3>
<pre>
public class NSUrlSessionDataDelegate : NSUrlSessionTaskDelegate {
	
	public NSUrlSessionDataDelegate ();
	public NSUrlSessionDataDelegate (NSCoder coder);
	public NSUrlSessionDataDelegate (NSObjectFlag t);
	public NSUrlSessionDataDelegate (IntPtr handle);
	
	public virtual void DidBecomeDownloadTask (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public override void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
	public virtual void DidReceiveData (NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public virtual void DidReceiveResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, Action<nsurlsessionresponsedisposition> completionHandler);
	public override void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public override void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, Action<nsinputstream> completionHandler);
	public virtual void WillCacheResponse (NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, Action<nscachedurlresponse> completionHandler);
	public override void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, Action<nsurlrequest> completionHandler);
}
</nsurlrequest></nscachedurlresponse></nsinputstream></nsurlsessionresponsedisposition></nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDataTask</h3>
<pre>
public class NSUrlSessionDataTask : NSUrlSessionTask {
	
	public NSUrlSessionDataTask ();
	public NSUrlSessionDataTask (NSCoder coder);
	public NSUrlSessionDataTask (NSObjectFlag t);
	public NSUrlSessionDataTask (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDataTaskRequest</h3>
<pre>
public class NSUrlSessionDataTaskRequest {
	
	public NSUrlSessionDataTaskRequest (NSData arg1, NSUrlResponse arg2);
	
	public NSData Arg1 {
		get;
		set;
	}
	public NSUrlResponse Arg2 {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDelegate</h3>
<pre>
public class NSUrlSessionDelegate : NSObject {
	
	public NSUrlSessionDelegate ();
	public NSUrlSessionDelegate (NSCoder coder);
	public NSUrlSessionDelegate (NSObjectFlag t);
	public NSUrlSessionDelegate (IntPtr handle);
	
	public virtual void DidBecomeInvalid (NSUrlSession session, NSError error);
	public virtual void DidFinishEventsForBackgroundSession (NSUrlSession session);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
}
</nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDownloadDelegate</h3>
<pre>
public class NSUrlSessionDownloadDelegate : NSUrlSessionTaskDelegate {
	
	public NSUrlSessionDownloadDelegate ();
	public NSUrlSessionDownloadDelegate (NSCoder coder);
	public NSUrlSessionDownloadDelegate (NSObjectFlag t);
	public NSUrlSessionDownloadDelegate (IntPtr handle);
	
	public override void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public virtual void DidFinishDownloading (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
	public virtual void DidResume (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public override void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public virtual void DidWriteData (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
	public override void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, Action<nsinputstream> completionHandler);
	public override void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, Action<nsurlrequest> completionHandler);
	
	public static NSString TaskResumeDataKey {
		get;
	}
}
</nsurlrequest></nsinputstream></nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDownloadTask</h3>
<pre>
public class NSUrlSessionDownloadTask : NSUrlSessionTask {
	
	public NSUrlSessionDownloadTask ();
	public NSUrlSessionDownloadTask (NSCoder coder);
	public NSUrlSessionDownloadTask (NSObjectFlag t);
	public NSUrlSessionDownloadTask (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDownloadTaskRequest</h3>
<pre>
public class NSUrlSessionDownloadTaskRequest {
	
	public NSUrlSessionDownloadTaskRequest (NSUrl arg1, NSUrlResponse arg2);
	
	public NSUrl Arg1 {
		get;
		set;
	}
	public NSUrlResponse Arg2 {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionResponseDisposition</h3>
<pre>
[Serializable]
public enum NSUrlSessionResponseDisposition {
	Cancel,
	Allow,
	BecomeDownload
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionTask</h3>
<pre>
public class NSUrlSessionTask : NSObject {
	
	public NSUrlSessionTask ();
	public NSUrlSessionTask (NSCoder coder);
	public NSUrlSessionTask (NSObjectFlag t);
	public NSUrlSessionTask (IntPtr handle);
	
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void Resume ();
	public virtual void Suspend ();
	
	public static long TransferSizeUnknown {
		get;
	}
	public virtual long BytesExpectedToReceive {
		get;
	}
	public virtual long BytesExpectedToSend {
		get;
	}
	public virtual long BytesReceived {
		get;
	}
	public virtual long BytesSent {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSUrlRequest CurrentRequest {
		get;
	}
	public virtual NSError Error {
		get;
	}
	public virtual NSUrlRequest OriginalRequest {
		get;
	}
	public virtual NSUrlResponse Response {
		get;
	}
	public virtual NSUrlSessionTaskState State {
		get;
	}
	public virtual string TaskDescription {
		get;
		set;
	}
	public virtual uint TaskIdentifier {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionTaskDelegate</h3>
<pre>
public class NSUrlSessionTaskDelegate : NSUrlSessionDelegate {
	
	public NSUrlSessionTaskDelegate ();
	public NSUrlSessionTaskDelegate (NSCoder coder);
	public NSUrlSessionTaskDelegate (NSObjectFlag t);
	public NSUrlSessionTaskDelegate (IntPtr handle);
	
	public override void DidBecomeInvalid (NSUrlSession session, NSError error);
	public virtual void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public override void DidFinishEventsForBackgroundSession (NSUrlSession session);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
	public virtual void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
	public virtual void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public virtual void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, Action<nsinputstream> completionHandler);
	public virtual void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, Action<nsurlrequest> completionHandler);
}
</nsurlrequest></nsinputstream></nsurlsessionauthchallengedisposition,nsurlcredential></nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionTaskState</h3>
<pre>
[Serializable]
public enum NSUrlSessionTaskState {
	Running,
	Suspended,
	Canceling,
	Completed
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionUploadTask</h3>
<pre>
public class NSUrlSessionUploadTask : NSUrlSessionTask {
	
	public NSUrlSessionUploadTask ();
	public NSUrlSessionUploadTask (NSCoder coder);
	public NSUrlSessionUploadTask (NSObjectFlag t);
	public NSUrlSessionUploadTask (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.ProtocolAttribute</h3>
<p>Added:</p><pre>
 	
 	public Type WrapperType {
 		get;
 		set;
 	}
</pre>
<h2>Namespace: MonoTouch.GLKit</h2>
<h3>Type Changed: MonoTouch.GLKit.GLKNamedEffect</h3>
<p>Removed:</p><pre>
 public abstract class GLKNamedEffect : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GLKNamedEffect : MonoTouch.Foundation.NSObject, IGLKNamedEffect {
</pre>
<h3>New Type: MonoTouch.GLKit.GLKNamedEffect_Extensions</h3>
<pre>
public static class GLKNamedEffect_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.GLKit.GLKViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GLKViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GLKViewControllerDelegate : MonoTouch.Foundation.NSObject, IGLKViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GLKit.GLKViewControllerDelegate_Extensions</h3>
<pre>
public static class GLKViewControllerDelegate_Extensions {
	
	public static void WillPause (IGLKViewControllerDelegate This, GLKViewController controller, bool pause);
}
</pre>
<h3>Type Changed: MonoTouch.GLKit.GLKViewDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GLKViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GLKViewDelegate : MonoTouch.Foundation.NSObject, IGLKViewDelegate {
</pre>
<h3>New Type: MonoTouch.GLKit.GLKViewDelegate_Extensions</h3>
<pre>
public static class GLKViewDelegate_Extensions {
}
</pre>
<h3>New Type: MonoTouch.GLKit.IGLKNamedEffect</h3>
<pre>
public interface IGLKNamedEffect : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void PrepareToDraw ();
}
</pre>
<h3>New Type: MonoTouch.GLKit.IGLKViewControllerDelegate</h3>
<pre>
public interface IGLKViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void Update (GLKViewController controller);
}
</pre>
<h3>New Type: MonoTouch.GLKit.IGLKViewDelegate</h3>
<pre>
public interface IGLKViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DrawInRect (GLKView view, System.Drawing.RectangleF rect);
}
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class GKAchievementViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKAchievementViewControllerDelegate : MonoTouch.Foundation.NSObject, IGKAchievementViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKAchievementViewControllerDelegate_Extensions</h3>
<pre>
public static class GKAchievementViewControllerDelegate_Extensions {
	
	public static void DidFinish (IGKAchievementViewControllerDelegate This, GKAchievementViewController viewController);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKChallengeEventHandlerDelegate</h3>
<p>Removed:</p><pre>
 public class GKChallengeEventHandlerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKChallengeEventHandlerDelegate : MonoTouch.Foundation.NSObject, IGKChallengeEventHandlerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeEventHandlerDelegate_Extensions</h3>
<pre>
public static class GKChallengeEventHandlerDelegate_Extensions {
	
	public static void LocalPlayerCompletedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static void LocalPlayerReceivedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static void LocalPlayerSelectedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static void RemotePlayerCompletedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static bool ShouldShowBannerForLocallyCompletedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static bool ShouldShowBannerForLocallyReceivedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
	public static bool ShouldShowBannerForRemotelyCompletedChallenge (IGKChallengeEventHandlerDelegate This, GKChallenge challenge);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GKFriendRequestComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GKFriendRequestComposeViewControllerDelegate : MonoTouch.Foundation.NSObject, IGKFriendRequestComposeViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKFriendRequestComposeViewControllerDelegate_Extensions</h3>
<pre>
public static class GKFriendRequestComposeViewControllerDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKGameCenterControllerDelegate</h3>
<p>Removed:</p><pre>
 public class GKGameCenterControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKGameCenterControllerDelegate : MonoTouch.Foundation.NSObject, IGKGameCenterControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKGameCenterControllerDelegate_Extensions</h3>
<pre>
public static class GKGameCenterControllerDelegate_Extensions {
	
	public static void Finished (IGKGameCenterControllerDelegate This, GKGameCenterViewController controller);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class GKLeaderboardViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKLeaderboardViewControllerDelegate : MonoTouch.Foundation.NSObject, IGKLeaderboardViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate_Extensions</h3>
<pre>
public static class GKLeaderboardViewControllerDelegate_Extensions {
	
	public static void DidFinish (IGKLeaderboardViewControllerDelegate This, GKLeaderboardViewController viewController);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GKMatchDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GKMatchDelegate : MonoTouch.Foundation.NSObject, IGKMatchDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKMatchDelegate_Extensions</h3>
<pre>
public static class GKMatchDelegate_Extensions {
	
	[Obsolete("No longer on iOS")]
	public static void ConnectionFailed (IGKMatchDelegate This, GKMatch match, string playerId, MonoTouch.Foundation.NSError error);
	public static void Failed (IGKMatchDelegate This, GKMatch match, MonoTouch.Foundation.NSError error);
	public static bool ShouldReinvitePlayer (IGKMatchDelegate This, GKMatch match, string playerId);
	public static void StateChanged (IGKMatchDelegate This, GKMatch match, string playerId, GKPlayerConnectionState state);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GKMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GKMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject, IGKMatchmakerViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate_Extensions</h3>
<pre>
public static class GKMatchmakerViewControllerDelegate_Extensions {
	
	public static void ReceivedAcceptFromHostedPlayer (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, string playerID);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKPeerConnectionState</h3>
<p>Removed:</p><pre>
 public enum GKPeerConnectionState {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public enum GKPeerConnectionState {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKPeerPickerControllerDelegate</h3>
<p>Removed:</p><pre>
 public class GKPeerPickerControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKPeerPickerControllerDelegate : MonoTouch.Foundation.NSObject, IGKPeerPickerControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKPeerPickerControllerDelegate_Extensions</h3>
<pre>
public static class GKPeerPickerControllerDelegate_Extensions {
	
	public static void ConnectionTypeSelected (IGKPeerPickerControllerDelegate This, GKPeerPickerController picker, GKPeerPickerConnectionType type);
	public static void ControllerCancelled (IGKPeerPickerControllerDelegate This, GKPeerPickerController picker);
	public static GKSession GetSession (IGKPeerPickerControllerDelegate This, GKPeerPickerController picker, GKPeerPickerConnectionType forType);
	public static void PeerConnected (IGKPeerPickerControllerDelegate This, GKPeerPickerController picker, string peerId, GKSession toSession);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKSendDataMode</h3>
<p>Removed:</p><pre>
 public enum GKSendDataMode {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public enum GKSendDataMode {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKSessionDelegate</h3>
<p>Removed:</p><pre>
 public class GKSessionDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKSessionDelegate : MonoTouch.Foundation.NSObject, IGKSessionDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKSessionDelegate_Extensions</h3>
<pre>
public static class GKSessionDelegate_Extensions {
	
	public static void FailedWithError (IGKSessionDelegate This, GKSession session, MonoTouch.Foundation.NSError error);
	public static void PeerChangedState (IGKSessionDelegate This, GKSession session, string peerID, GKPeerConnectionState state);
	public static void PeerConnectionFailed (IGKSessionDelegate This, GKSession session, string peerID, MonoTouch.Foundation.NSError error);
	public static void PeerConnectionRequest (IGKSessionDelegate This, GKSession session, string peerID);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKSessionMode</h3>
<p>Removed:</p><pre>
 public enum GKSessionMode {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public enum GKSessionMode {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate</h3>
<p>Removed:</p><pre>
 public class GKTurnBasedEventHandlerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class GKTurnBasedEventHandlerDelegate : MonoTouch.Foundation.NSObject, IGKTurnBasedEventHandlerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate_Extensions</h3>
<pre>
public static class GKTurnBasedEventHandlerDelegate_Extensions {
	
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, GKPlayer[] playersToInvite);
	public static void HandleMatchEnded (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match);
	public static void HandleTurnEvent (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match, bool activated);
	[Obsolete("Replaced by HandleTurnEvent in iOS 6.0")]
	public static void HandleTurnEventForMatch (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class GKTurnBasedMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GKTurnBasedMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject, IGKTurnBasedMatchmakerViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedMatchmakerViewControllerDelegate_Extensions</h3>
<pre>
public static class GKTurnBasedMatchmakerViewControllerDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKVoiceChatClient</h3>
<p>Removed:</p><pre>
 public abstract class GKVoiceChatClient : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class GKVoiceChatClient : MonoTouch.Foundation.NSObject, IGKVoiceChatClient {
</pre>
<h3>New Type: MonoTouch.GameKit.GKVoiceChatClient_Extensions</h3>
<pre>
public static class GKVoiceChatClient_Extensions {
	
	public static void FailedToConnect (IGKVoiceChatClient This, GKVoiceChatService voiceChatService, string participantID, MonoTouch.Foundation.NSError error);
	public static void ReceivedInvitation (IGKVoiceChatClient This, GKVoiceChatService voiceChatService, string participantID, int callID);
	public static void SendRealTimeData (IGKVoiceChatClient This, GKVoiceChatService voiceChatService, MonoTouch.Foundation.NSData data, string participantID);
	public static void Started (IGKVoiceChatClient This, GKVoiceChatService voiceChatService, string participantID);
	public static void Stopped (IGKVoiceChatClient This, GKVoiceChatService voiceChatService, string participantID, MonoTouch.Foundation.NSError error);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKVoiceChatServiceError</h3>
<p>Removed:</p><pre>
 public enum GKVoiceChatServiceError {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public enum GKVoiceChatServiceError {
</pre>
<h3>New Type: MonoTouch.GameKit.IGKAchievementViewControllerDelegate</h3>
<pre>
public interface IGKAchievementViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKChallengeEventHandlerDelegate</h3>
<pre>
public interface IGKChallengeEventHandlerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKFriendRequestComposeViewControllerDelegate</h3>
<pre>
public interface IGKFriendRequestComposeViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DidFinish (GKFriendRequestComposeViewController viewController);
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKGameCenterControllerDelegate</h3>
<pre>
public interface IGKGameCenterControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKLeaderboardViewControllerDelegate</h3>
<pre>
public interface IGKLeaderboardViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKMatchDelegate</h3>
<pre>
public interface IGKMatchDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, string playerId);
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKMatchmakerViewControllerDelegate</h3>
<pre>
public interface IGKMatchmakerViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DidFailWithError (GKMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
	void DidFindMatch (GKMatchmakerViewController viewController, GKMatch match);
	void DidFindPlayers (GKMatchmakerViewController viewController, string [] playerIDs);
	void WasCancelled (GKMatchmakerViewController viewController);
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKPeerPickerControllerDelegate</h3>
<pre>
public interface IGKPeerPickerControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKSessionDelegate</h3>
<pre>
public interface IGKSessionDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKTurnBasedEventHandlerDelegate</h3>
<pre>
public interface IGKTurnBasedEventHandlerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKTurnBasedMatchmakerViewControllerDelegate</h3>
<pre>
public interface IGKTurnBasedMatchmakerViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void FailedWithError (GKTurnBasedMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
	void FoundMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
	void PlayerQuitForMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
	void WasCancelled (GKTurnBasedMatchmakerViewController viewController);
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKVoiceChatClient</h3>
<pre>
public interface IGKVoiceChatClient : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	string ParticipantID ();
	void SendData (GKVoiceChatService voiceChatService, MonoTouch.Foundation.NSData data, string toParticipant);
}
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>New Type: MonoTouch.MapKit.IMKAnnotation</h3>
<pre>
public interface IMKAnnotation : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKLocalSearch</h3>
<pre>
public interface IMKLocalSearch : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKLocalSearchRequest</h3>
<pre>
public interface IMKLocalSearchRequest : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKLocalSearchResponse</h3>
<pre>
public interface IMKLocalSearchResponse : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKMapViewDelegate</h3>
<pre>
public interface IMKMapViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKOverlay</h3>
<pre>
public interface IMKOverlay : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MapKit.IMKReverseGeocoderDelegate</h3>
<pre>
public interface IMKReverseGeocoderDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void FailedWithError (MKReverseGeocoder geocoder, MonoTouch.Foundation.NSError error);
	void FoundWithPlacemark (MKReverseGeocoder geocoder, MKPlacemark placemark);
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKAnnotation</h3>
<p>Removed:</p><pre>
 public abstract class MKAnnotation : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class MKAnnotation : MonoTouch.Foundation.NSObject, IMKAnnotation {
</pre>
<h3>New Type: MonoTouch.MapKit.MKAnnotation_Extensions</h3>
<pre>
public static class MKAnnotation_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKLocalSearch</h3>
<p>Removed:</p><pre>
 public class MKLocalSearch : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MKLocalSearch : MonoTouch.Foundation.NSObject, IMKLocalSearch {
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKLocalSearchRequest</h3>
<p>Removed:</p><pre>
 public class MKLocalSearchRequest : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MKLocalSearchRequest : MonoTouch.Foundation.NSObject, IMKLocalSearchRequest {
</pre>
<h3>New Type: MonoTouch.MapKit.MKLocalSearchRequest_Extensions</h3>
<pre>
public static class MKLocalSearchRequest_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKLocalSearchResponse</h3>
<p>Removed:</p><pre>
 public class MKLocalSearchResponse : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MKLocalSearchResponse : MonoTouch.Foundation.NSObject, IMKLocalSearchResponse {
</pre>
<h3>New Type: MonoTouch.MapKit.MKLocalSearchResponse_Extensions</h3>
<pre>
public static class MKLocalSearchResponse_Extensions {
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKLocalSearch_Extensions</h3>
<pre>
public static class MKLocalSearch_Extensions {
	
	public static void Cancel (IMKLocalSearch This);
	public static void Start (IMKLocalSearch This, MKLocalSearchCompletionHandler completionHandler);
	public static System.Threading.Tasks.Task<mklocalsearchresponse> StartAsync (IMKLocalSearch This);
}
</mklocalsearchresponse></pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Removed:</p><pre>
 public class MKMapViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MKMapViewDelegate : MonoTouch.Foundation.NSObject, IMKMapViewDelegate {
</pre>
<h3>New Type: MonoTouch.MapKit.MKMapViewDelegate_Extensions</h3>
<pre>
public static class MKMapViewDelegate_Extensions {
	
	public static void CalloutAccessoryControlTapped (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView view, MonoTouch.UIKit.UIControl control);
	public static void ChangedDragState (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);
	public static void DidAddAnnotationViews (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView[] views);
	public static void DidAddOverlayRenderers (IMKMapViewDelegate This, MKMapView mapView, MKOverlayRenderer[] renderers);
	[Obsolete("Since iOS 7 it is recommended that you use DidAddOverlayRenderers")]
	public static void DidAddOverlayViews (IMKMapViewDelegate This, MKMapView mapView, MKOverlayView overlayViews);
	public static void DidChageUserTrackingMode (IMKMapViewDelegate This, MKMapView mapView, MKUserTrackingMode mode, bool animated);
	public static void DidDeselectAnnotationView (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView view);
	public static void DidFailToLocateUser (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSError error);
	public static void DidFinishRenderingMap (IMKMapViewDelegate This, MKMapView mapView, bool fullyRendered);
	public static void DidSelectAnnotationView (IMKMapViewDelegate This, MKMapView mapView, MKAnnotationView view);
	public static void DidStopLocatingUser (IMKMapViewDelegate This, MKMapView mapView);
	public static void DidUpdateUserLocation (IMKMapViewDelegate This, MKMapView mapView, MKUserLocation userLocation);
	public static MKOverlayRenderer GetRendererForOverlay (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
	public static MKAnnotationView GetViewForAnnotation (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSObject annotation);
	[Obsolete("Since iOS 7 it is recommnended that you use GetRendererForOverlay")]
	public static MKOverlayView GetViewForOverlay (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
	public static void LoadingMapFailed (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSError error);
	public static void MapLoaded (IMKMapViewDelegate This, MKMapView mapView);
	public static void RegionChanged (IMKMapViewDelegate This, MKMapView mapView, bool animated);
	public static void RegionWillChange (IMKMapViewDelegate This, MKMapView mapView, bool animated);
	public static void WillStartLoadingMap (IMKMapViewDelegate This, MKMapView mapView);
	public static void WillStartLocatingUser (IMKMapViewDelegate This, MKMapView mapView);
	public static void WillStartRenderingMap (IMKMapViewDelegate This, MKMapView mapView);
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKOverlay</h3>
<p>Removed:</p><pre>
 public class MKOverlay : MKAnnotation {
</pre>
<p>Added:</p><pre>
 public class MKOverlay : MKAnnotation, IMKOverlay {
</pre>
<h3>New Type: MonoTouch.MapKit.MKOverlay_Extensions</h3>
<pre>
public static class MKOverlay_Extensions {
	
	public static bool Intersects (IMKOverlay This, MKMapRect rect);
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKPlacemark</h3>
<p>Removed:</p><pre>
 public class MKPlacemark : MonoTouch.CoreLocation.CLPlacemark {
</pre>
<p>Added:</p><pre>
 public class MKPlacemark : MonoTouch.CoreLocation.CLPlacemark, IMKAnnotation {
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKReverseGeocoderDelegate</h3>
<p>Removed:</p><pre>
 public abstract class MKReverseGeocoderDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class MKReverseGeocoderDelegate : MonoTouch.Foundation.NSObject, IMKReverseGeocoderDelegate {
</pre>
<h3>New Type: MonoTouch.MapKit.MKReverseGeocoderDelegate_Extensions</h3>
<pre>
public static class MKReverseGeocoderDelegate_Extensions {
}
</pre>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<h3>New Type: MonoTouch.MediaPlayer.IMPMediaPickerControllerDelegate</h3>
<pre>
public interface IMPMediaPickerControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaPickerControllerDelegate</h3>
<p>Removed:</p><pre>
 public class MPMediaPickerControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MPMediaPickerControllerDelegate : MonoTouch.Foundation.NSObject, IMPMediaPickerControllerDelegate {
</pre>
<h3>New Type: MonoTouch.MediaPlayer.MPMediaPickerControllerDelegate_Extensions</h3>
<pre>
public static class MPMediaPickerControllerDelegate_Extensions {
	
	public static void MediaItemsPicked (IMPMediaPickerControllerDelegate This, MPMediaPickerController sender, MPMediaItemCollection mediaItemCollection);
	public static void MediaPickerDidCancel (IMPMediaPickerControllerDelegate This, MPMediaPickerController sender);
}
</pre>
<h2>Namespace: MonoTouch.MessageUI</h2>
<h3>New Type: MonoTouch.MessageUI.IMFMailComposeViewControllerDelegate</h3>
<pre>
public interface IMFMailComposeViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MessageUI.IMFMessageComposeViewControllerDelegate</h3>
<pre>
public interface IMFMessageComposeViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void Finished (MFMessageComposeViewController controller, MessageComposeResult result);
}
</pre>
<h3>Type Changed: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class MFMailComposeViewControllerDelegate : MonoTouch.UIKit.UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class MFMailComposeViewControllerDelegate : MonoTouch.UIKit.UINavigationControllerDelegate, IMFMailComposeViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate_Extensions</h3>
<pre>
public static class MFMailComposeViewControllerDelegate_Extensions {
	
	public static void Finished (IMFMailComposeViewControllerDelegate This, MFMailComposeViewController controller, MFMailComposeResult result, MonoTouch.Foundation.NSError error);
}
</pre>
<h3>Type Changed: MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class MFMessageComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class MFMessageComposeViewControllerDelegate : MonoTouch.Foundation.NSObject, IMFMessageComposeViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate_Extensions</h3>
<pre>
public static class MFMessageComposeViewControllerDelegate_Extensions {
}
</pre>
<h2>Namespace: MonoTouch.MultipeerConnectivity</h2>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSession</h3>
<p>Removed:</p><pre>
 	public MCSession ();
 	public MCSession (MCPeerID myPeerID, MonoTouch.Foundation.NSObject[] identity, MCEncryptionPreference encryptionPreference);
 	public virtual MonoTouch.Foundation.NSObject[] SecurityIdentity {
</pre>
<p>Added:</p><pre>
 	public MCSession (MCPeerID myPeerID, MonoTouch.Security.SecIdentity identity, MCEncryptionPreference encryptionPreference);
 	public MCSession (MCPeerID myPeerID, MonoTouch.Security.SecIdentity identity, MonoTouch.Security.SecCertificate[] certificates, MCEncryptionPreference encryptionPreference);
 	public MCSession (MCPeerID myPeerID);
 	public virtual MonoTouch.Foundation.NSArray SecurityIdentity {
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSessionDelegate</h3>
<p>Removed:</p><pre>
 	public virtual bool DidReceiveCertificate (MCSession session, MonoTouch.Foundation.NSArray certificate, MCPeerID peerID, Action&lt;bool&gt; certificateHandler);
</pre>
<p>Added:</p><pre>
 	public virtual bool DidReceiveCertificate (MCSession session, MonoTouch.Security.SecCertificate[] certificate, MCPeerID peerID, Action&lt;bool&gt; certificateHandler);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static void AVEdgeWidths_objc_msgSend_stret (out MonoTouch.AVFoundation.AVEdgeWidths retval, IntPtr receiver, IntPtr selector);
 	public static void AVEdgeWidths_objc_msgSendSuper_stret (out MonoTouch.AVFoundation.AVEdgeWidths retval, IntPtr receiver, IntPtr selector);
 	public static MonoTouch.AVFoundation.AVPixelAspectRatio AVPixelAspectRatio_objc_msgSend (IntPtr receiver, IntPtr selector);
 	public static void AVPixelAspectRatio_objc_msgSend_stret (out MonoTouch.AVFoundation.AVPixelAspectRatio retval, IntPtr receiver, IntPtr selector);
 	public static MonoTouch.AVFoundation.AVPixelAspectRatio AVPixelAspectRatio_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static void AVPixelAspectRatio_objc_msgSendSuper_stret (out MonoTouch.AVFoundation.AVPixelAspectRatio retval, IntPtr receiver, IntPtr selector);
 	public static MonoTouch.CoreGraphics.CGVector CGVector_objc_msgSend (IntPtr receiver, IntPtr selector);
 	public static void CGVector_objc_msgSend_stret (out MonoTouch.CoreGraphics.CGVector retval, IntPtr receiver, IntPtr selector);
 	public static MonoTouch.CoreGraphics.CGVector CGVector_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static void CGVector_objc_msgSendSuper_stret (out MonoTouch.CoreGraphics.CGVector retval, IntPtr receiver, IntPtr selector);
 	public static IntPtr IntPtr_objc_msgSend_CGVector_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_float_Double_bool (IntPtr receiver, IntPtr selector, float arg1, double arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_CGVector (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, MonoTouch.CoreGraphics.CGVector arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_CGVector_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_Double_bool (IntPtr receiver, IntPtr selector, float arg1, double arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_CGVector (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, MonoTouch.CoreGraphics.CGVector arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static void void_objc_msgSend_CGVector (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1);
 	public static void void_objc_msgSend_CGVector_PointF (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4, long arg5);
 	public static void void_objc_msgSendSuper_CGVector (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1);
 	public static void void_objc_msgSendSuper_CGVector_PointF (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4, long arg5);
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Runtime</h3>
<p>Added:</p><pre>
 	public static T GetINativeObject&lt;T&gt; (IntPtr ptr, bool owns) where T : class;
 	public static T GetNSObject&lt;T&gt; (IntPtr ptr) where T : MonoTouch.Foundation.NSObject;
 	public static IntPtr GetProtocol (string protocol);
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>New Type: MonoTouch.PassKit.IPKAddPassesViewControllerDelegate</h3>
<pre>
public interface IPKAddPassesViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKAddPassesViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class PKAddPassesViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class PKAddPassesViewControllerDelegate : MonoTouch.Foundation.NSObject, IPKAddPassesViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.PassKit.PKAddPassesViewControllerDelegate_Extensions</h3>
<pre>
public static class PKAddPassesViewControllerDelegate_Extensions {
	
	public static void Finished (IPKAddPassesViewControllerDelegate This, PKAddPassesViewController controller);
}
</pre>
<h2>Namespace: MonoTouch.QuickLook</h2>
<h3>New Type: MonoTouch.QuickLook.IQLPreviewControllerDataSource</h3>
<pre>
public interface IQLPreviewControllerDataSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	QLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
	int PreviewItemCount (QLPreviewController controller);
}
</pre>
<h3>New Type: MonoTouch.QuickLook.IQLPreviewControllerDelegate</h3>
<pre>
public interface IQLPreviewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.QuickLook.IQLPreviewItem</h3>
<pre>
public interface IQLPreviewItem : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	string ItemTitle {
		get;
	}
	MonoTouch.Foundation.NSUrl ItemUrl {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.QuickLook.QLPreviewControllerDataSource</h3>
<p>Removed:</p><pre>
 public abstract class QLPreviewControllerDataSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class QLPreviewControllerDataSource : MonoTouch.Foundation.NSObject, IQLPreviewControllerDataSource {
</pre>
<h3>New Type: MonoTouch.QuickLook.QLPreviewControllerDataSource_Extensions</h3>
<pre>
public static class QLPreviewControllerDataSource_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.QuickLook.QLPreviewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class QLPreviewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class QLPreviewControllerDelegate : MonoTouch.Foundation.NSObject, IQLPreviewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.QuickLook.QLPreviewControllerDelegate_Extensions</h3>
<pre>
public static class QLPreviewControllerDelegate_Extensions {
	
	public static void DidDismiss (IQLPreviewControllerDelegate This, QLPreviewController controller);
	public static System.Drawing.RectangleF FrameForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, QLPreviewItem item, ref MonoTouch.UIKit.UIView view);
	public static bool ShouldOpenUrl (IQLPreviewControllerDelegate This, QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
	public static MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
	public static void WillDismiss (IQLPreviewControllerDelegate This, QLPreviewController controller);
}
</pre>
<h3>Type Changed: MonoTouch.QuickLook.QLPreviewItem</h3>
<p>Removed:</p><pre>
 public abstract class QLPreviewItem : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class QLPreviewItem : MonoTouch.Foundation.NSObject, IQLPreviewItem {
</pre>
<h3>New Type: MonoTouch.QuickLook.QLPreviewItem_Extensions</h3>
<pre>
public static class QLPreviewItem_Extensions {
}
</pre>
<h2>Namespace: MonoTouch.Security</h2>
<h3>Type Changed: MonoTouch.Security.SecIdentity</h3>
<p>Added:</p><pre>
 	public SecIdentity (IntPtr handle);
 	
 	public SecKey PrivateKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Security.SecPolicy</h3>
<p>Added:</p><pre>
 	public static SecPolicy CreatePolicy (MonoTouch.Foundation.NSString policyIdentifier, MonoTouch.Foundation.NSDictionary properties);
 	public static SecPolicy CreateRevocationPolicy (SecRevocation revocationFlags);
 	public MonoTouch.Foundation.NSDictionary GetProperties ();
</pre>
<h3>New Type: MonoTouch.Security.SecPolicyIdentifier</h3>
<pre>
public static class SecPolicyIdentifier {
	
	public static MonoTouch.Foundation.NSString AppleCodeSigning {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleEAP {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleIDValidation {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleIPsec {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleRevocation {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleSMIME {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleSSL {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleTimeStamping {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleX509Basic {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Security.SecPolicyPropertyKey</h3>
<pre>
public static class SecPolicyPropertyKey {
	
	public static MonoTouch.Foundation.NSString Client {
		get;
	}
	public static MonoTouch.Foundation.NSString Name {
		get;
	}
	public static MonoTouch.Foundation.NSString Oid {
		get;
	}
	public static MonoTouch.Foundation.NSString RevocationFlags {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Security.SecRecord</h3>
<p>Removed:</p><pre>
 	public MonoTouch.Foundation.NSObject ValueRef {
</pre>
<p>Added:</p><pre>
 	public T GetValueRef&lt;T&gt; () where T : class;
 	public void SetValueRef (MonoTouch.ObjCRuntime.INativeObject value);
 	[Obsolete("Use GetValueRef&lt;T&gt; and SetValueRef for INativeObject support")]
	public MonoTouch.Foundation.NSObject ValueRef {
</pre>
<h3>New Type: MonoTouch.Security.SecRevocation</h3>
<pre>
[Serializable]
[Flags]
public enum SecRevocation {
	None,
	OCSPMethod,
	CRLMethod,
	PreferCRL,
	RequirePositiveResponse,
	NetworkAccessDisabled,
	UseAnyAvailableMethod
}
</pre>
<h3>Type Changed: MonoTouch.Security.SecTrust</h3>
<p>Added:</p><pre>
 	public SecTrust (SecCertificate certificate, SecPolicy policy);
 	public SecCertificate[] GetCustomAnchorCertificates ();
 	public SecPolicy[] GetPolicies ();
 	public MonoTouch.Foundation.NSDictionary GetResult ();
 	public SecTrustResult GetTrustResult ();
 	public void SetOCSPResponse (System.Collections.Generic.IEnumerable&lt;MonoTouch.Foundation.NSData&gt; ocspResponses);
 	public void SetOCSPResponse (MonoTouch.Foundation.NSArray ocspResponses);
 	public void SetOCSPResponse (MonoTouch.Foundation.NSData ocspResponse);
 	public void SetPolicies (System.Collections.Generic.IEnumerable&lt;SecPolicy&gt; policies);
 	public void SetPolicies (MonoTouch.Foundation.NSArray policies);
 	public void SetPolicy (SecPolicy policy);
 	public bool NetworkFetchAllowed {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.Security.SecTrustPropertyKey</h3>
<pre>
public static class SecTrustPropertyKey {
	
	public static MonoTouch.Foundation.NSString Error {
		get;
	}
	public static MonoTouch.Foundation.NSString Title {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Security.SecTrustResultKey</h3>
<pre>
public static class SecTrustResultKey {
	
	public static MonoTouch.Foundation.NSString EvaluationDate {
		get;
	}
	public static MonoTouch.Foundation.NSString ExtendedValidation {
		get;
	}
	public static MonoTouch.Foundation.NSString OrganizationName {
		get;
	}
	public static MonoTouch.Foundation.NSString ResultValue {
		get;
	}
	public static MonoTouch.Foundation.NSString RevocationChecked {
		get;
	}
	public static MonoTouch.Foundation.NSString RevocationValidUntilDate {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Security.SslProtocol</h3>
<pre>
[Serializable]
public enum SslProtocol {
	Unknown,
	Ssl3_0,
	Tls_1_0,
	Tls_1_1,
	Tls_1_2,
	Dtls_1_0,
	Ssl_2_0,
	Ssl_3_0_only,
	Tls_1_0_only,
	All
}
</pre>
<h2>Namespace: MonoTouch.SpriteKit</h2>
<h3>New Type: MonoTouch.SpriteKit.ISKPhysicsContactDelegate</h3>
<pre>
public interface ISKPhysicsContactDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKAction</h3>
<p>Removed:</p><pre>
 	public static SKAction MoveByX (float deltaX, float deltaY, double sec);
 	public static SKAction ScaleXBy (float xScale, float yScale, double sec);
 	public static SKAction ScaleXTo (float xScale, float yScale, double sec);
</pre>
<p>Added:</p><pre>
 	public static SKAction MoveBy (MonoTouch.CoreGraphics.CGVector delta, double duration);
 	public static SKAction MoveBy (float deltaX, float deltaY, double sec);
 	public static SKAction RotateToAngle (float radians, double sec, bool shortedUnitArc);
 	public static SKAction ScaleBy (float xScale, float yScale, double sec);
 	public static SKAction ScaleTo (float xScale, float yScale, double sec);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKEmitterNode</h3>
<p>Removed:</p><pre>
 	public virtual System.Drawing.PointF ParticlePositionRange {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreGraphics.CGVector ParticlePositionRange {
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKNode</h3>
<p>Added:</p><pre>
 	public virtual bool InParentHierarchy (SKNode node);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsBody</h3>
<p>Removed:</p><pre>
 	public virtual void ApplyForce (System.Drawing.PointF force);
 	public virtual void ApplyForce (System.Drawing.PointF force, System.Drawing.PointF point);
 	public virtual void ApplyImpulse (System.Drawing.PointF impulse);
 	public virtual void ApplyImpulse (System.Drawing.PointF impulse, System.Drawing.PointF point);
 	public virtual MonoTouch.Foundation.NSObject[] Joints {
 	public virtual System.Drawing.PointF Velocity {
</pre>
<p>Added:</p><pre>
 	public virtual void ApplyForce (MonoTouch.CoreGraphics.CGVector force);
 	public virtual void ApplyForce (MonoTouch.CoreGraphics.CGVector force, System.Drawing.PointF point);
 	public virtual void ApplyImpulse (MonoTouch.CoreGraphics.CGVector impulse);
 	public virtual void ApplyImpulse (MonoTouch.CoreGraphics.CGVector impulse, System.Drawing.PointF point);
 	public virtual SKPhysicsJoint[] Joints {
 	public virtual MonoTouch.CoreGraphics.CGVector Velocity {
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsContactDelegate</h3>
<p>Removed:</p><pre>
 public class SKPhysicsContactDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class SKPhysicsContactDelegate : MonoTouch.Foundation.NSObject, ISKPhysicsContactDelegate {
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsContactDelegate_Extensions</h3>
<pre>
public static class SKPhysicsContactDelegate_Extensions {
	
	public static void DidBeginContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
	public static void DidEndContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
}
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointSliding</h3>
<p>Removed:</p><pre>
 	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor, System.Drawing.PointF axis);
</pre>
<p>Added:</p><pre>
 	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor, MonoTouch.CoreGraphics.CGVector axis);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler</h3>
<p>Removed:</p><pre>
 public delegate void SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (SKPhysicsBody body, System.Drawing.PointF point, System.Drawing.PointF normal, out bool stop);
</pre>
<p>Added:</p><pre>
 public delegate void SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (SKPhysicsBody body, System.Drawing.PointF point, MonoTouch.CoreGraphics.CGVector normal, out bool stop);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKTexture</h3>
<p>Removed:</p><pre>
 	public virtual void Preload ();
</pre>
<p>Added:</p><pre>
 	public static void PreloadTextures (SKTexture[] textures, MonoTouch.Foundation.NSAction completion);
 	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
 	public virtual void Preload (MonoTouch.Foundation.NSAction completion);
 	public virtual System.Threading.Tasks.Task PreloadAsync ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKTextureAtlas</h3>
<p>Removed:</p><pre>
 	public virtual void Preload ();
</pre>
<p>Added:</p><pre>
 	public static void PreloadTextures (SKTexture[] textures, MonoTouch.Foundation.NSAction completion);
 	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
 	public virtual void Preload (MonoTouch.Foundation.NSAction completion);
 	public virtual System.Threading.Tasks.Task PreloadAsync ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKView</h3>
<p>Added:</p><pre>
 	public virtual bool IgnoresSiblingOrder {
 		get;
 		set;
 	}
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>New Type: MonoTouch.StoreKit.ISKPaymentTransactionObserver</h3>
<pre>
public interface ISKPaymentTransactionObserver : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void UpdatedTransactions (SKPaymentQueue queue, SKPaymentTransaction[] transactions);
}
</pre>
<h3>New Type: MonoTouch.StoreKit.ISKProductsRequestDelegate</h3>
<pre>
public interface ISKProductsRequestDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void ReceivedResponse (SKProductsRequest request, SKProductsResponse response);
}
</pre>
<h3>New Type: MonoTouch.StoreKit.ISKRequestDelegate</h3>
<pre>
public interface ISKRequestDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.StoreKit.ISKStoreProductViewControllerDelegate</h3>
<pre>
public interface ISKStoreProductViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentTransactionObserver</h3>
<p>Removed:</p><pre>
 public abstract class SKPaymentTransactionObserver : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class SKPaymentTransactionObserver : MonoTouch.Foundation.NSObject, ISKPaymentTransactionObserver {
</pre>
<h3>New Type: MonoTouch.StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<pre>
public static class SKPaymentTransactionObserver_Extensions {
	
	public static void PaymentQueueRestoreCompletedTransactionsFinished (ISKPaymentTransactionObserver This, SKPaymentQueue queue);
	public static void RemovedTransactions (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKPaymentTransaction[] transactions);
	public static void RestoreCompletedTransactionsFailedWithError (ISKPaymentTransactionObserver This, SKPaymentQueue queue, MonoTouch.Foundation.NSError error);
	public static void UpdatedDownloads (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKDownload[] downloads);
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKProductsRequestDelegate</h3>
<p>Removed:</p><pre>
 public abstract class SKProductsRequestDelegate : SKRequestDelegate {
</pre>
<p>Added:</p><pre>
 public abstract class SKProductsRequestDelegate : SKRequestDelegate, ISKProductsRequestDelegate {
</pre>
<h3>New Type: MonoTouch.StoreKit.SKProductsRequestDelegate_Extensions</h3>
<pre>
public static class SKProductsRequestDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKRequestDelegate</h3>
<p>Removed:</p><pre>
 public class SKRequestDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class SKRequestDelegate : MonoTouch.Foundation.NSObject, ISKRequestDelegate {
</pre>
<h3>New Type: MonoTouch.StoreKit.SKRequestDelegate_Extensions</h3>
<pre>
public static class SKRequestDelegate_Extensions {
	
	public static void RequestFailed (ISKRequestDelegate This, SKRequest request, MonoTouch.Foundation.NSError error);
	public static void RequestFinished (ISKRequestDelegate This, SKRequest request);
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class SKStoreProductViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class SKStoreProductViewControllerDelegate : MonoTouch.Foundation.NSObject, ISKStoreProductViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.StoreKit.SKStoreProductViewControllerDelegate_Extensions</h3>
<pre>
public static class SKStoreProductViewControllerDelegate_Extensions {
	
	public static void Finished (ISKStoreProductViewControllerDelegate This, SKStoreProductViewController controller);
}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.INSTextAttachmentContainer</h3>
<pre>
public interface INSTextAttachmentContainer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.INSTextStorageDelegate</h3>
<pre>
public interface INSTextStorageDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIAccelerometerDelegate</h3>
<pre>
public interface IUIAccelerometerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIActionSheetDelegate</h3>
<pre>
public interface IUIActionSheetDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIActivityItemSource</h3>
<pre>
public interface IUIActivityItemSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	MonoTouch.Foundation.NSObject GetPlaceholderData (UIActivityViewController activityViewController);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIAlertViewDelegate</h3>
<pre>
public interface IUIAlertViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIAppearance</h3>
<pre>
public interface IUIAppearance : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIApplicationDelegate</h3>
<pre>
public interface IUIApplicationDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIBarPositioningDelegate</h3>
<pre>
public interface IUIBarPositioningDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUICollectionViewDataSource</h3>
<pre>
public interface IUICollectionViewDataSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	int GetItemsCount (UICollectionView collectionView, int section);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUICollectionViewDelegate</h3>
<pre>
public interface IUICollectionViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject, IUIScrollViewDelegate {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUICollectionViewDelegateFlowLayout</h3>
<pre>
public interface IUICollectionViewDelegateFlowLayout : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUICollectionViewSource</h3>
<pre>
public interface IUICollectionViewSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject, IUICollectionViewDataSource, IUICollectionViewDelegate, IUIScrollViewDelegate {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUICollisionBehaviorDelegate</h3>
<pre>
public interface IUICollisionBehaviorDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIDocumentInteractionControllerDelegate</h3>
<pre>
public interface IUIDocumentInteractionControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIDynamicAnimatorDelegate</h3>
<pre>
public interface IUIDynamicAnimatorDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DidPause (UIDynamicAnimator animator);
	void WillResume (UIDynamicAnimator animator);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIDynamicItem</h3>
<pre>
public interface IUIDynamicItem : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	System.Drawing.RectangleF Bounds {
		get;
	}
	System.Drawing.PointF Center {
		get;
		set;
	}
	MonoTouch.CoreGraphics.CGAffineTransform Transform {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIGestureRecognizerDelegate</h3>
<pre>
public interface IUIGestureRecognizerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIImagePickerControllerDelegate</h3>
<pre>
public interface IUIImagePickerControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUILayoutSupport</h3>
<pre>
public interface IUILayoutSupport : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUINavigationBarDelegate</h3>
<pre>
public interface IUINavigationBarDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUINavigationControllerDelegate</h3>
<pre>
public interface IUINavigationControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIObjectRestoration</h3>
<pre>
public interface IUIObjectRestoration : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPageViewControllerDataSource</h3>
<pre>
public interface IUIPageViewControllerDataSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	UIViewController GetNextViewController (UIPageViewController pageViewController, UIViewController referenceViewController);
	UIViewController GetPreviousViewController (UIPageViewController pageViewController, UIViewController referenceViewController);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPageViewControllerDelegate</h3>
<pre>
public interface IUIPageViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPickerViewDataSource</h3>
<pre>
public interface IUIPickerViewDataSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	int GetComponentCount (UIPickerView pickerView);
	int GetRowsInComponent (UIPickerView pickerView, int component);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPickerViewDelegate</h3>
<pre>
public interface IUIPickerViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPopoverControllerDelegate</h3>
<pre>
public interface IUIPopoverControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPrintInteractionControllerDelegate</h3>
<pre>
public interface IUIPrintInteractionControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIScrollViewDelegate</h3>
<pre>
public interface IUIScrollViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUISearchBarDelegate</h3>
<pre>
public interface IUISearchBarDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUISearchDisplayDelegate</h3>
<pre>
public interface IUISearchDisplayDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUISplitViewControllerDelegate</h3>
<pre>
public interface IUISplitViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIStateRestoring</h3>
<pre>
public interface IUIStateRestoring : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITabBarControllerDelegate</h3>
<pre>
public interface IUITabBarControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITabBarDelegate</h3>
<pre>
public interface IUITabBarDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITableViewDataSource</h3>
<pre>
public interface IUITableViewDataSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	UITableViewCell GetCell (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	int RowsInSection (UITableView tableView, int section);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITableViewDelegate</h3>
<pre>
public interface IUITableViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITextFieldDelegate</h3>
<pre>
public interface IUITextFieldDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITextInputDelegate</h3>
<pre>
public interface IUITextInputDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void SelectionDidChange (MonoTouch.Foundation.NSObject uiTextInput);
	void SelectionWillChange (MonoTouch.Foundation.NSObject uiTextInput);
	void TextDidChange (MonoTouch.Foundation.NSObject textInput);
	void TextWillChange (MonoTouch.Foundation.NSObject textInput);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITextInputTokenizer</h3>
<pre>
public interface IUITextInputTokenizer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	UITextPosition GetPosition (UITextPosition fromPosition, UITextGranularity toBoundary, UITextDirection inDirection);
	UITextRange GetRangeEnclosingPosition (UITextPosition position, UITextGranularity granularity, UITextDirection direction);
	bool ProbeDirection (UITextPosition probePosition, UITextGranularity atBoundary, UITextDirection inDirection);
	bool ProbeDirectionWithinTextUnit (UITextPosition probePosition, UITextGranularity withinTextUnit, UITextDirection inDirection);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUITextViewDelegate</h3>
<pre>
public interface IUITextViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIToolbarDelegate</h3>
<pre>
public interface IUIToolbarDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIVideoEditorControllerDelegate</h3>
<pre>
public interface IUIVideoEditorControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIWebViewDelegate</h3>
<pre>
public interface IUIWebViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSTextAttachment</h3>
<p>Removed:</p><pre>
 public class NSTextAttachment : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSTextAttachment : MonoTouch.Foundation.NSObject, INSTextAttachmentContainer {
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSTextAttachmentContainer</h3>
<p>Removed:</p><pre>
 public class NSTextAttachmentContainer : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSTextAttachmentContainer : MonoTouch.Foundation.NSObject, INSTextAttachmentContainer {
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextAttachmentContainer_Extensions</h3>
<pre>
public static class NSTextAttachmentContainer_Extensions {
	
	public static System.Drawing.RectangleF GetAttachmentBounds (INSTextAttachmentContainer This, NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public static UIImage GetImageForBounds (INSTextAttachmentContainer This, System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSTextStorageDelegate</h3>
<p>Removed:</p><pre>
 public class NSTextStorageDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSTextStorageDelegate : MonoTouch.Foundation.NSObject, INSTextStorageDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorageDelegate_Extensions</h3>
<pre>
public static class NSTextStorageDelegate_Extensions {
	
	public static void DidProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	public static void WillProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAccelerometerDelegate</h3>
<p>Removed:</p><pre>
 public class UIAccelerometerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIAccelerometerDelegate : MonoTouch.Foundation.NSObject, IUIAccelerometerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIAccelerometerDelegate_Extensions</h3>
<pre>
public static class UIAccelerometerDelegate_Extensions {
	
	public static void DidAccelerate (IUIAccelerometerDelegate This, UIAccelerometer accelerometer, UIAcceleration acceleration);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActionSheetDelegate</h3>
<p>Removed:</p><pre>
 public class UIActionSheetDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIActionSheetDelegate : MonoTouch.Foundation.NSObject, IUIActionSheetDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIActionSheetDelegate_Extensions</h3>
<pre>
public static class UIActionSheetDelegate_Extensions {
	
	public static void Canceled (IUIActionSheetDelegate This, UIActionSheet actionSheet);
	public static void Clicked (IUIActionSheetDelegate This, UIActionSheet actionSheet, int buttonIndex);
	public static void Dismissed (IUIActionSheetDelegate This, UIActionSheet actionSheet, int buttonIndex);
	public static void Presented (IUIActionSheetDelegate This, UIActionSheet actionSheet);
	public static void WillDismiss (IUIActionSheetDelegate This, UIActionSheet actionSheet, int buttonIndex);
	public static void WillPresent (IUIActionSheetDelegate This, UIActionSheet actionSheet);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActivityItemSource</h3>
<p>Removed:</p><pre>
 public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject, IUIActivityItemSource {
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityItemSource_Extensions</h3>
<pre>
public static class UIActivityItemSource_Extensions {
	
	public static string GetDataTypeIdentifierForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public static string GetSubjectForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public static UIImage GetThumbnailImageForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType, System.Drawing.SizeF suggestedSize);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAlertViewDelegate</h3>
<p>Removed:</p><pre>
 public class UIAlertViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIAlertViewDelegate : MonoTouch.Foundation.NSObject, IUIAlertViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIAlertViewDelegate_Extensions</h3>
<pre>
public static class UIAlertViewDelegate_Extensions {
	
	public static void Canceled (IUIAlertViewDelegate This, UIAlertView alertView);
	public static void Clicked (IUIAlertViewDelegate This, UIAlertView alertview, int buttonIndex);
	public static void Dismissed (IUIAlertViewDelegate This, UIAlertView alertView, int buttonIndex);
	public static void Presented (IUIAlertViewDelegate This, UIAlertView alertView);
	public static bool ShouldEnableFirstOtherButton (IUIAlertViewDelegate This, UIAlertView alertView);
	public static void WillDismiss (IUIAlertViewDelegate This, UIAlertView alertView, int buttonIndex);
	public static void WillPresent (IUIAlertViewDelegate This, UIAlertView alertView);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAppearance</h3>
<p>Removed:</p><pre>
 public class UIAppearance : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIAppearance : MonoTouch.Foundation.NSObject, IUIAppearance {
</pre>
<h3>New Type: MonoTouch.UIKit.UIAppearance_Extensions</h3>
<pre>
public static class UIAppearance_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Removed:</p><pre>
 	public static void RegisterObjectForStateRestoration (MonoTouch.Foundation.NSObject uistateRestoringObject, string restorationIdentifier);
</pre>
<p>Added:</p><pre>
 	public static void RegisterObjectForStateRestoration (IUIStateRestoring uistateRestoringObject, string restorationIdentifier);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Removed:</p><pre>
 public class UIApplicationDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIApplicationDelegate : MonoTouch.Foundation.NSObject, IUIApplicationDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIApplicationDelegate_Extensions</h3>
<pre>
public static class UIApplicationDelegate_Extensions {
	
	public static bool AccessibilityPerformMagicTap (IUIApplicationDelegate This);
	public static void ApplicationSignificantTimeChange (IUIApplicationDelegate This, UIApplication application);
	public static void ChangedStatusBarFrame (IUIApplicationDelegate This, UIApplication application, System.Drawing.RectangleF oldStatusBarFrame);
	public static void DidChangeStatusBarOrientation (IUIApplicationDelegate This, UIApplication application, UIInterfaceOrientation oldStatusBarOrientation);
	public static void DidDecodeRestorableState (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSCoder coder);
	public static void DidEnterBackground (IUIApplicationDelegate This, UIApplication application);
	public static void DidReceiveRemoteNotification (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSDictionary userInfo, Action<uibackgroundfetchresult> completionHandler);
	public static void FailedToRegisterForRemoteNotifications (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSError error);
	public static void FinishedLaunching (IUIApplicationDelegate This, UIApplication application);
	public static bool FinishedLaunching (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSDictionary launchOptions);
	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUIApplicationDelegate This, UIApplication application, UIWindow forWindow);
	public static UIViewController GetViewController (IUIApplicationDelegate This, UIApplication application, string [] restorationIdentifierComponents, MonoTouch.Foundation.NSCoder coder);
	public static void HandleEventsForBackgroundUrl (IUIApplicationDelegate This, UIApplication application, string sessionIdentifier, MonoTouch.Foundation.NSAction completionHandler);
	public static bool HandleOpenURL (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUrl url);
	public static void OnActivated (IUIApplicationDelegate This, UIApplication application);
	public static void OnResignActivation (IUIApplicationDelegate This, UIApplication application);
	public static bool OpenUrl (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
	public static void PerformFetch (IUIApplicationDelegate This, UIApplication application, Action<uibackgroundfetchresult> completionHandler);
	public static void ProtectedDataDidBecomeAvailable (IUIApplicationDelegate This, UIApplication application);
	public static void ProtectedDataWillBecomeUnavailable (IUIApplicationDelegate This, UIApplication application);
	public static void ReceivedLocalNotification (IUIApplicationDelegate This, UIApplication application, UILocalNotification notification);
	public static void ReceivedRemoteNotification (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSDictionary userInfo);
	public static void ReceiveMemoryWarning (IUIApplicationDelegate This, UIApplication application);
	public static void RegisteredForRemoteNotifications (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSData deviceToken);
	public static bool ShouldRestoreApplicationState (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSCoder coder);
	public static bool ShouldSaveApplicationState (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSCoder coder);
	public static void WillChangeStatusBarFrame (IUIApplicationDelegate This, UIApplication application, System.Drawing.RectangleF newStatusBarFrame);
	public static void WillChangeStatusBarOrientation (IUIApplicationDelegate This, UIApplication application, UIInterfaceOrientation newStatusBarOrientation, double duration);
	public static void WillEncodeRestorableState (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSCoder coder);
	public static void WillEnterForeground (IUIApplicationDelegate This, UIApplication application);
	public static bool WillFinishLaunching (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSDictionary launchOptions);
	public static void WillTerminate (IUIApplicationDelegate This, UIApplication application);
}
</uibackgroundfetchresult></uibackgroundfetchresult></pre>
<h3>Type Changed: MonoTouch.UIKit.UIAttachmentBehavior</h3>
<p>Removed:</p><pre>
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, UIOffset offset, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, MonoTouch.Foundation.NSObject attachedToItem);
 	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, UIOffset offsetFromCenter, MonoTouch.Foundation.NSObject attachedToItem, UIOffset attachOffsetFromCenter);
 	public virtual MonoTouch.Foundation.NSObject[] Items {
</pre>
<p>Added:</p><pre>
 	public UIAttachmentBehavior (IUIDynamicItem item, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offset, System.Drawing.PointF anchorPoint);
 	public UIAttachmentBehavior (IUIDynamicItem item, MonoTouch.Foundation.NSObject attachedToItem);
 	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offsetFromCenter, MonoTouch.Foundation.NSObject attachedToItem, UIOffset attachOffsetFromCenter);
 	public virtual IUIDynamicItem[] Items {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarPositioningDelegate</h3>
<p>Removed:</p><pre>
 public class UIBarPositioningDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIBarPositioningDelegate : MonoTouch.Foundation.NSObject, IUIBarPositioningDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioningDelegate_Extensions</h3>
<pre>
public static class UIBarPositioningDelegate_Extensions {
	
	public static UIBarPosition GetPositionForBar (IUIBarPositioningDelegate This, MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewController</h3>
<p>Removed:</p><pre>
 public class UICollectionViewController : UIViewController {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewController : UIViewController, IUICollectionViewDataSource, IUICollectionViewDelegate, IUICollectionViewSource, IUIScrollViewDelegate {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDataSource</h3>
<p>Removed:</p><pre>
 public abstract class UICollectionViewDataSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UICollectionViewDataSource : MonoTouch.Foundation.NSObject, IUICollectionViewDataSource {
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDataSource_Extensions</h3>
<pre>
public static class UICollectionViewDataSource_Extensions {
	
	public static UICollectionReusableView GetViewForSupplementaryElement (IUICollectionViewDataSource This, UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
	public static int NumberOfSections (IUICollectionViewDataSource This, UICollectionView collectionView);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegate</h3>
<p>Removed:</p><pre>
 public class UICollectionViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewDelegate : MonoTouch.Foundation.NSObject, IUICollectionViewDelegate, IUIScrollViewDelegate {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<p>Removed:</p><pre>
 public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate, IUICollectionViewDelegateFlowLayout {
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout_Extensions</h3>
<pre>
public static class UICollectionViewDelegateFlowLayout_Extensions {
	
	public static UIEdgeInsets GetInsetForSection (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, int section);
	public static float GetMinimumInteritemSpacingForSection (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, int section);
	public static float GetMinimumLineSpacingForSection (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, int section);
	public static System.Drawing.SizeF GetReferenceSizeForFooter (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, int section);
	public static System.Drawing.SizeF GetReferenceSizeForHeader (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, int section);
	public static System.Drawing.SizeF GetSizeForItem (IUICollectionViewDelegateFlowLayout This, UICollectionView collectionView, UICollectionViewLayout layout, MonoTouch.Foundation.NSIndexPath indexPath);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDelegate_Extensions</h3>
<pre>
public static class UICollectionViewDelegate_Extensions {
	
	public static bool CanPerformAction (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
	public static void CellDisplayingEnded (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void ItemDeselected (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void ItemHighlighted (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void ItemSelected (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void ItemUnhighlighted (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void PerformAction (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
	public static bool ShouldDeselectItem (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool ShouldHighlightItem (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool ShouldSelectItem (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool ShouldShowMenu (IUICollectionViewDelegate This, UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void SupplementaryViewDisplayingEnded (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
	public static UICollectionViewTransitionLayout TransitionLayout (IUICollectionViewDelegate This, UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Removed:</p><pre>
 public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject, IUIDynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewSource</h3>
<p>Removed:</p><pre>
 public class UICollectionViewSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewSource : MonoTouch.Foundation.NSObject, IUICollectionViewDataSource, IUICollectionViewDelegate, IUICollectionViewSource, IUIScrollViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewSource_Extensions</h3>
<pre>
public static class UICollectionViewSource_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBeganBoundaryContactEventArgs</h3>
<p>Removed:</p><pre>
 	public UICollisionBeganBoundaryContactEventArgs (MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
 	public MonoTouch.Foundation.NSObject DynamicItem {
</pre>
<p>Added:</p><pre>
 	public UICollisionBeganBoundaryContactEventArgs (IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
 	public IUIDynamicItem DynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBeganContactEventArgs</h3>
<p>Removed:</p><pre>
 	public UICollisionBeganContactEventArgs (MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem, System.Drawing.PointF atPoint);
 	public MonoTouch.Foundation.NSObject FirstItem {
 	public MonoTouch.Foundation.NSObject SecondItem {
</pre>
<p>Added:</p><pre>
 	public UICollisionBeganContactEventArgs (IUIDynamicItem firstItem, IUIDynamicItem secondItem, System.Drawing.PointF atPoint);
 	public IUIDynamicItem FirstItem {
 	public IUIDynamicItem SecondItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBehavior</h3>
<p>Removed:</p><pre>
 	public UICollisionBehavior (MonoTouch.Foundation.NSObject[] items);
 	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual MonoTouch.Foundation.NSObject[] Items {
</pre>
<p>Added:</p><pre>
 	public UICollisionBehavior (IUIDynamicItem[] items);
 	public virtual void AddItem (IUIDynamicItem dynamicItem);
 	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
 	public virtual IUIDynamicItem[] Items {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBehaviorDelegate</h3>
<p>Removed:</p><pre>
 public class UICollisionBehaviorDelegate : MonoTouch.Foundation.NSObject {
 	public virtual void BeganBoundaryContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
 	public virtual void BeganContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem, System.Drawing.PointF atPoint);
 	public virtual void EndedBoundaryContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
 	public virtual void EndedContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem);
</pre>
<p>Added:</p><pre>
 public class UICollisionBehaviorDelegate : MonoTouch.Foundation.NSObject, IUICollisionBehaviorDelegate {
 	public virtual void BeganBoundaryContact (UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
 	public virtual void BeganContact (UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem, System.Drawing.PointF atPoint);
 	public virtual void EndedBoundaryContact (UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
 	public virtual void EndedContact (UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem);
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBehaviorDelegate_Extensions</h3>
<pre>
public static class UICollisionBehaviorDelegate_Extensions {
	
	public static void BeganBoundaryContact (IUICollisionBehaviorDelegate This, UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
	public static void BeganContact (IUICollisionBehaviorDelegate This, UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem, System.Drawing.PointF atPoint);
	public static void EndedBoundaryContact (IUICollisionBehaviorDelegate This, UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
	public static void EndedContact (IUICollisionBehaviorDelegate This, UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionEndedBoundaryContactEventArgs</h3>
<p>Removed:</p><pre>
 	public UICollisionEndedBoundaryContactEventArgs (MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
 	public MonoTouch.Foundation.NSObject DynamicItem {
</pre>
<p>Added:</p><pre>
 	public UICollisionEndedBoundaryContactEventArgs (IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
 	public IUIDynamicItem DynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionEndedContactEventArgs</h3>
<p>Removed:</p><pre>
 	public UICollisionEndedContactEventArgs (MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem);
 	public MonoTouch.Foundation.NSObject FirstItem {
 	public MonoTouch.Foundation.NSObject SecondItem {
</pre>
<p>Added:</p><pre>
 	public UICollisionEndedContactEventArgs (IUIDynamicItem firstItem, IUIDynamicItem secondItem);
 	public IUIDynamicItem FirstItem {
 	public IUIDynamicItem SecondItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocumentInteractionControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIDocumentInteractionControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIDocumentInteractionControllerDelegate : MonoTouch.Foundation.NSObject, IUIDocumentInteractionControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIDocumentInteractionControllerDelegate_Extensions</h3>
<pre>
public static class UIDocumentInteractionControllerDelegate_Extensions {
	
	[Obsolete("Deprecated in iOS 6.0")]
	public static bool CanPerformAction (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
	public static void DidDismissOpenInMenu (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void DidDismissOptionsMenu (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void DidEndPreview (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void DidEndSendingToApplication (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller, string application);
	[Obsolete("Deprecated in iOS 6.0")]
	public static bool PerformAction (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
	public static System.Drawing.RectangleF RectangleForPreview (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static UIViewController ViewControllerForPreview (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static UIView ViewForPreview (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void WillBeginPreview (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void WillBeginSendingToApplication (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller, string application);
	public static void WillPresentOpenInMenu (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
	public static void WillPresentOptionsMenu (IUIDocumentInteractionControllerDelegate This, UIDocumentInteractionController controller);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicAnimator</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject[] GetDynamicItems (System.Drawing.RectangleF rect);
 	public virtual void UpdateItemUsingCurrentState (MonoTouch.Foundation.NSObject uiDynamicItem);
</pre>
<p>Added:</p><pre>
 	public virtual IUIDynamicItem[] GetDynamicItems (System.Drawing.RectangleF rect);
 	public virtual void UpdateItemUsingCurrentState (IUIDynamicItem uiDynamicItem);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicAnimatorDelegate</h3>
<p>Removed:</p><pre>
 public abstract class UIDynamicAnimatorDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UIDynamicAnimatorDelegate : MonoTouch.Foundation.NSObject, IUIDynamicAnimatorDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicAnimatorDelegate_Extensions</h3>
<pre>
public static class UIDynamicAnimatorDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicItem</h3>
<p>Removed:</p><pre>
 [Obsolete]
public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject, IUIDynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicItemBehavior</h3>
<p>Removed:</p><pre>
 	public UIDynamicItemBehavior (MonoTouch.Foundation.NSObject[] items);
 	public virtual void AddAngularVelocityForItem (float velocity, MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void AddLinearVelocityForItem (System.Drawing.PointF velocity, MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual float GetAngularVelocityForItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual System.Drawing.PointF GetLinearVelocityForItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual MonoTouch.Foundation.NSObject[] Items {
</pre>
<p>Added:</p><pre>
 	public UIDynamicItemBehavior (IUIDynamicItem[] items);
 	public virtual void AddAngularVelocityForItem (float velocity, IUIDynamicItem dynamicItem);
 	public virtual void AddItem (IUIDynamicItem dynamicItem);
 	public virtual void AddLinearVelocityForItem (System.Drawing.PointF velocity, IUIDynamicItem dynamicItem);
 	public virtual float GetAngularVelocityForItem (IUIDynamicItem dynamicItem);
 	public virtual System.Drawing.PointF GetLinearVelocityForItem (IUIDynamicItem dynamicItem);
 	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
 	public virtual IUIDynamicItem[] Items {
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicItem_Extensions</h3>
<pre>
public static class UIDynamicItem_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFont</h3>
<p>Added:</p><pre>
 	public static UIFont PreferredFontForTextStyle (UIFontTextStyle textStyle);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontDescriptor</h3>
<p>Added:</p><pre>
 	public static UIFontDescriptor PreferredForStyle (UIFontTextStyle style);
 	public static MonoTouch.Foundation.NSString TextStyleBody {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleCaption1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleCaption2 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleFootnote {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleHeadline {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextStyleSubheadline {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontTextStyle</h3>
<p>Removed:</p><pre>
 public static class UIFontTextStyle {
 	
 	public static MonoTouch.Foundation.NSString Body {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Caption1 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Caption2 {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Footnote {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Headline {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Subheadline {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIFontTextStyle {
 	Headline,
 	Body,
 	Subheadline,
 	Footnote,
 	Caption1,
 	Caption2
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate</h3>
<p>Removed:</p><pre>
 public class UIGestureRecognizerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIGestureRecognizerDelegate : MonoTouch.Foundation.NSObject, IUIGestureRecognizerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIGestureRecognizerDelegate_Extensions</h3>
<pre>
public static class UIGestureRecognizerDelegate_Extensions {
	
	public static bool ShouldBegin (IUIGestureRecognizerDelegate This, UIGestureRecognizer recognizer);
	public static bool ShouldBeRequiredToFailBy (IUIGestureRecognizerDelegate This, UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public static bool ShouldReceiveTouch (IUIGestureRecognizerDelegate This, UIGestureRecognizer recognizer, UITouch touch);
	public static bool ShouldRecognizeSimultaneously (IUIGestureRecognizerDelegate This, UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
	public static bool ShouldRequireFailureOf (IUIGestureRecognizerDelegate This, UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGravityBehavior</h3>
<p>Removed:</p><pre>
 	public UIGravityBehavior (MonoTouch.Foundation.NSObject[] items);
 	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual System.Drawing.SizeF GravityDirection {
 	public virtual MonoTouch.Foundation.NSObject[] Items {
</pre>
<p>Added:</p><pre>
 	public UIGravityBehavior (IUIDynamicItem[] items);
 	public virtual void AddItem (IUIDynamicItem dynamicItem);
 	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
 	public virtual MonoTouch.CoreGraphics.CGVector GravityDirection {
 	public virtual IUIDynamicItem[] Items {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIImagePickerControllerDelegate : UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class UIImagePickerControllerDelegate : UINavigationControllerDelegate, IUIImagePickerControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIImagePickerControllerDelegate_Extensions</h3>
<pre>
public static class UIImagePickerControllerDelegate_Extensions {
	
	public static void Canceled (IUIImagePickerControllerDelegate This, UIImagePickerController picker);
	public static void FinishedPickingImage (IUIImagePickerControllerDelegate This, UIImagePickerController picker, UIImage image, MonoTouch.Foundation.NSDictionary editingInfo);
	public static void FinishedPickingMedia (IUIImagePickerControllerDelegate This, UIImagePickerController picker, MonoTouch.Foundation.NSDictionary info);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UILayoutSupport</h3>
<pre>
public class UILayoutSupport : MonoTouch.Foundation.NSObject, IUILayoutSupport {
	
	public UILayoutSupport ();
	public UILayoutSupport (MonoTouch.Foundation.NSCoder coder);
	public UILayoutSupport (MonoTouch.Foundation.NSObjectFlag t);
	public UILayoutSupport (IntPtr handle);
	
	public virtual float Length {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UILayoutSupport_Extensions</h3>
<pre>
public static class UILayoutSupport_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBarDelegate</h3>
<p>Removed:</p><pre>
 public class UINavigationBarDelegate : UIBarPositioningDelegate {
</pre>
<p>Added:</p><pre>
 public class UINavigationBarDelegate : UIBarPositioningDelegate, IUINavigationBarDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UINavigationBarDelegate_Extensions</h3>
<pre>
public static class UINavigationBarDelegate_Extensions {
	
	public static void DidPopItem (IUINavigationBarDelegate This, UINavigationBar navigationBar, UINavigationItem item);
	public static void DidPushItem (IUINavigationBarDelegate This, UINavigationBar navigationBar, UINavigationItem item);
	public static bool ShouldPopItem (IUINavigationBarDelegate This, UINavigationBar navigationBar, UINavigationItem item);
	public static bool ShouldPushItem (IUINavigationBarDelegate This, UINavigationBar navigationBar, UINavigationItem item);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UINavigationControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UINavigationControllerDelegate : MonoTouch.Foundation.NSObject, IUINavigationControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UINavigationControllerDelegate_Extensions</h3>
<pre>
public static class UINavigationControllerDelegate_Extensions {
	
	public static void DidShowViewController (IUINavigationControllerDelegate This, UINavigationController navigationController, UIViewController viewController, bool animated);
	public static UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (IUINavigationControllerDelegate This, UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
	public static UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUINavigationControllerDelegate This, UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
	public static UIInterfaceOrientation GetPreferredInterfaceOrientation (IUINavigationControllerDelegate This, UINavigationController navigationController);
	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUINavigationControllerDelegate This, UINavigationController navigationController);
	public static void WillShowViewController (IUINavigationControllerDelegate This, UINavigationController navigationController, UIViewController viewController, bool animated);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIObjectRestoration</h3>
<p>Removed:</p><pre>
 public class UIObjectRestoration : MonoTouch.Foundation.NSObject {
 	public virtual MonoTouch.Foundation.NSObject GetStateRestorationObjectFromPath (MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
</pre>
<p>Added:</p><pre>
 public class UIObjectRestoration : MonoTouch.Foundation.NSObject, IUIObjectRestoration {
 	public virtual IUIStateRestoring GetStateRestorationObjectFromPath (MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
</pre>
<h3>New Type: MonoTouch.UIKit.UIObjectRestoration_Extensions</h3>
<pre>
public static class UIObjectRestoration_Extensions {
	
	public static IUIStateRestoring GetStateRestorationObjectFromPath (IUIObjectRestoration This, MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDataSource</h3>
<p>Removed:</p><pre>
 public abstract class UIPageViewControllerDataSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UIPageViewControllerDataSource : MonoTouch.Foundation.NSObject, IUIPageViewControllerDataSource {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPageViewControllerDataSource_Extensions</h3>
<pre>
public static class UIPageViewControllerDataSource_Extensions {
	
	public static int GetPresentationCount (IUIPageViewControllerDataSource This, UIPageViewController pageViewController);
	public static int GetPresentationIndex (IUIPageViewControllerDataSource This, UIPageViewController pageViewController);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIPageViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPageViewControllerDelegate : MonoTouch.Foundation.NSObject, IUIPageViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPageViewControllerDelegate_Extensions</h3>
<pre>
public static class UIPageViewControllerDelegate_Extensions {
	
	public static void DidFinishAnimating (IUIPageViewControllerDelegate This, UIPageViewController pageViewController, bool finished, UIViewController[] previousViewControllers, bool completed);
	public static UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);
	public static UIPageViewControllerSpineLocation GetSpineLocation (IUIPageViewControllerDelegate This, UIPageViewController pageViewController, UIInterfaceOrientation orientation);
	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);
	public static void WillTransition (IUIPageViewControllerDelegate This, UIPageViewController pageViewController, UIViewController[] pendingViewControllers);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPickerViewDataSource</h3>
<p>Removed:</p><pre>
 public abstract class UIPickerViewDataSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UIPickerViewDataSource : MonoTouch.Foundation.NSObject, IUIPickerViewDataSource {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPickerViewDataSource_Extensions</h3>
<pre>
public static class UIPickerViewDataSource_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPickerViewDelegate</h3>
<p>Removed:</p><pre>
 public class UIPickerViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPickerViewDelegate : MonoTouch.Foundation.NSObject, IUIPickerViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPickerViewDelegate_Extensions</h3>
<pre>
public static class UIPickerViewDelegate_Extensions {
	
	public static MonoTouch.Foundation.NSAttributedString GetAttributedTitle (IUIPickerViewDelegate This, UIPickerView pickerView, int row, int component);
	public static float GetComponentWidth (IUIPickerViewDelegate This, UIPickerView pickerView, int component);
	public static float GetRowHeight (IUIPickerViewDelegate This, UIPickerView pickerView, int component);
	public static string GetTitle (IUIPickerViewDelegate This, UIPickerView pickerView, int row, int component);
	public static UIView GetView (IUIPickerViewDelegate This, UIPickerView pickerView, int row, int component, UIView view);
	public static void Selected (IUIPickerViewDelegate This, UIPickerView pickerView, int row, int component);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIPopoverControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPopoverControllerDelegate : MonoTouch.Foundation.NSObject, IUIPopoverControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPopoverControllerDelegate_Extensions</h3>
<pre>
public static class UIPopoverControllerDelegate_Extensions {
	
	public static void DidDismiss (IUIPopoverControllerDelegate This, UIPopoverController popoverController);
	public static bool ShouldDismiss (IUIPopoverControllerDelegate This, UIPopoverController popoverController);
	public static void WillReposition (IUIPopoverControllerDelegate This, UIPopoverController popoverController, ref System.Drawing.RectangleF rect, ref UIView view);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIPrintInteractionControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPrintInteractionControllerDelegate : MonoTouch.Foundation.NSObject, IUIPrintInteractionControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIPrintInteractionControllerDelegate_Extensions</h3>
<pre>
public static class UIPrintInteractionControllerDelegate_Extensions {
	
	public static UIPrintPaper ChoosePaper (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController, UIPrintPaper[] paperList);
	public static float CutLengthForPaper (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController, UIPrintPaper paper);
	public static void DidDismissPrinterOptions (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static void DidFinishJob (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static void DidPresentPrinterOptions (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static UIViewController GetViewController (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static void WillDismissPrinterOptions (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static void WillPresentPrinterOptions (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
	public static void WillStartJob (IUIPrintInteractionControllerDelegate This, UIPrintInteractionController printInteractionController);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPushBehavior</h3>
<p>Removed:</p><pre>
 	public UIPushBehavior (MonoTouch.Foundation.NSObject[] items, UIPushBehaviorMode mode);
 	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual UIOffset GetTargetOffsetFromCenter (UIDynamicItem item);
 	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
 	public virtual void SetTargetOffset (UIOffset offset, UIDynamicItem item);
 	public virtual MonoTouch.Foundation.NSObject[] Items {
 	public virtual System.Drawing.SizeF PushDirection {
</pre>
<p>Added:</p><pre>
 	public UIPushBehavior (IUIDynamicItem[] items, UIPushBehaviorMode mode);
 	public virtual void AddItem (IUIDynamicItem dynamicItem);
 	public virtual UIOffset GetTargetOffsetFromCenter (IUIDynamicItem item);
 	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
 	public virtual void SetTargetOffset (UIOffset offset, IUIDynamicItem item);
 	public virtual IUIDynamicItem[] Items {
 	public virtual MonoTouch.CoreGraphics.CGVector PushDirection {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScrollViewDelegate</h3>
<p>Removed:</p><pre>
 public class UIScrollViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIScrollViewDelegate : MonoTouch.Foundation.NSObject, IUIScrollViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIScrollViewDelegate_Extensions</h3>
<pre>
public static class UIScrollViewDelegate_Extensions {
	
	public static void DecelerationEnded (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void DecelerationStarted (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void DidZoom (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void DraggingEnded (IUIScrollViewDelegate This, UIScrollView scrollView, bool willDecelerate);
	public static void DraggingStarted (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void ScrollAnimationEnded (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void Scrolled (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void ScrolledToTop (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static bool ShouldScrollToTop (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static UIView ViewForZoomingInScrollView (IUIScrollViewDelegate This, UIScrollView scrollView);
	public static void WillEndDragging (IUIScrollViewDelegate This, UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public static void ZoomingEnded (IUIScrollViewDelegate This, UIScrollView scrollView, UIView withView, float atScale);
	public static void ZoomingStarted (IUIScrollViewDelegate This, UIScrollView scrollView, UIView view);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBarDelegate</h3>
<p>Removed:</p><pre>
 public class UISearchBarDelegate : UIBarPositioningDelegate {
</pre>
<p>Added:</p><pre>
 public class UISearchBarDelegate : UIBarPositioningDelegate, IUISearchBarDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UISearchBarDelegate_Extensions</h3>
<pre>
public static class UISearchBarDelegate_Extensions {
	
	public static void BookmarkButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void CancelButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void ListButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void OnEditingStarted (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void OnEditingStopped (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void SearchButtonClicked (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void SelectedScopeButtonIndexChanged (IUISearchBarDelegate This, UISearchBar searchBar, int selectedScope);
	public static bool ShouldBeginEditing (IUISearchBarDelegate This, UISearchBar searchBar);
	public static bool ShouldChangeTextInRange (IUISearchBarDelegate This, UISearchBar searchBar, MonoTouch.Foundation.NSRange range, string text);
	public static bool ShouldEndEditing (IUISearchBarDelegate This, UISearchBar searchBar);
	public static void TextChanged (IUISearchBarDelegate This, UISearchBar searchBar, string searchText);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchDisplayDelegate</h3>
<p>Removed:</p><pre>
 public class UISearchDisplayDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UISearchDisplayDelegate : MonoTouch.Foundation.NSObject, IUISearchDisplayDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UISearchDisplayDelegate_Extensions</h3>
<pre>
public static class UISearchDisplayDelegate_Extensions {
	
	public static void DidBeginSearch (IUISearchDisplayDelegate This, UISearchDisplayController controller);
	public static void DidEndSearch (IUISearchDisplayDelegate This, UISearchDisplayController controller);
	public static void DidHideSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
	public static void DidLoadSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
	public static void DidShowSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
	public static bool ShouldReloadForSearchScope (IUISearchDisplayDelegate This, UISearchDisplayController controller, int forSearchOption);
	public static bool ShouldReloadForSearchString (IUISearchDisplayDelegate This, UISearchDisplayController controller, string forSearchString);
	public static void WillBeginSearch (IUISearchDisplayDelegate This, UISearchDisplayController controller);
	public static void WillEndSearch (IUISearchDisplayDelegate This, UISearchDisplayController controller);
	public static void WillHideSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
	public static void WillShowSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
	public static void WillUnloadSearchResults (IUISearchDisplayDelegate This, UISearchDisplayController controller, UITableView tableView);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISnapBehavior</h3>
<p>Removed:</p><pre>
 	public UISnapBehavior (MonoTouch.Foundation.NSObject dynamicItem, System.Drawing.PointF point);
</pre>
<p>Added:</p><pre>
 	public UISnapBehavior (IUIDynamicItem dynamicItem, System.Drawing.PointF point);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISplitViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UISplitViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UISplitViewControllerDelegate : MonoTouch.Foundation.NSObject, IUISplitViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UISplitViewControllerDelegate_Extensions</h3>
<pre>
public static class UISplitViewControllerDelegate_Extensions {
	
	public static bool ShouldHideViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);
	public static void WillHideViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController aViewController, UIBarButtonItem barButtonItem, UIPopoverController pc);
	public static void WillPresentViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIPopoverController pc, UIViewController aViewController);
	public static void WillShowViewController (IUISplitViewControllerDelegate This, UISplitViewController svc, UIViewController aViewController, UIBarButtonItem button);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStateRestoring</h3>
<p>Removed:</p><pre>
 public class UIStateRestoring : MonoTouch.Foundation.NSObject {
 	public virtual MonoTouch.Foundation.NSObject RestorationParent {
</pre>
<p>Added:</p><pre>
 public class UIStateRestoring : MonoTouch.Foundation.NSObject, IUIStateRestoring {
 	public virtual IUIStateRestoring RestorationParent {
</pre>
<h3>New Type: MonoTouch.UIKit.UIStateRestoring_Extensions</h3>
<pre>
public static class UIStateRestoring_Extensions {
	
	public static void ApplicationFinishedRestoringState (IUIStateRestoring This);
	public static void DecodeRestorableState (IUIStateRestoring This, MonoTouch.Foundation.NSCoder coder);
	public static void EncodeRestorableState (IUIStateRestoring This, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UITabBarControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UITabBarControllerDelegate : MonoTouch.Foundation.NSObject, IUITabBarControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITabBarControllerDelegate_Extensions</h3>
<pre>
public static class UITabBarControllerDelegate_Extensions {
	
	public static void FinishedCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);
	public static UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
	public static UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
	public static UIInterfaceOrientation GetPreferredInterfaceOrientation (IUITabBarControllerDelegate This, UITabBarController tabBarController);
	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUITabBarControllerDelegate This, UITabBarController tabBarController);
	public static void OnCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers);
	public static void OnEndCustomizingViewControllers (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController[] viewControllers, bool changed);
	public static bool ShouldSelectViewController (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController viewController);
	public static void ViewControllerSelected (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController viewController);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarDelegate</h3>
<p>Removed:</p><pre>
 public class UITabBarDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UITabBarDelegate : MonoTouch.Foundation.NSObject, IUITabBarDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITabBarDelegate_Extensions</h3>
<pre>
public static class UITabBarDelegate_Extensions {
	
	public static void DidBeginCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items);
	public static void DidEndCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items, bool changed);
	public static void ItemSelected (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem item);
	public static void WillBeginCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items);
	public static void WillEndCustomizingItems (IUITabBarDelegate This, UITabBar tabbar, UITabBarItem[] items, bool changed);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDataSource</h3>
<p>Removed:</p><pre>
 public abstract class UITableViewDataSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UITableViewDataSource : MonoTouch.Foundation.NSObject, IUITableViewDataSource {
</pre>
<h3>New Type: MonoTouch.UIKit.UITableViewDataSource_Extensions</h3>
<pre>
public static class UITableViewDataSource_Extensions {
	
	public static bool CanEditRow (IUITableViewDataSource This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool CanMoveRow (IUITableViewDataSource This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void CommitEditingStyle (IUITableViewDataSource This, UITableView tableView, UITableViewCellEditingStyle editingStyle, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void MoveRow (IUITableViewDataSource This, UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath destinationIndexPath);
	public static int NumberOfSections (IUITableViewDataSource This, UITableView tableView);
	public static int SectionFor (IUITableViewDataSource This, UITableView tableView, string title, int atIndex);
	public static string [] SectionIndexTitles (IUITableViewDataSource This, UITableView tableView);
	public static string TitleForFooter (IUITableViewDataSource This, UITableView tableView, int section);
	public static string TitleForHeader (IUITableViewDataSource This, UITableView tableView, int section);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Removed:</p><pre>
 public class UITableViewDelegate : UIScrollViewDelegate {
</pre>
<p>Added:</p><pre>
 public class UITableViewDelegate : UIScrollViewDelegate, IUITableViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITableViewDelegate_Extensions</h3>
<pre>
public static class UITableViewDelegate_Extensions {
	
	public static void AccessoryButtonTapped (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static UITableViewCellAccessory AccessoryForRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool CanPerformAction (IUITableViewDelegate This, UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
	public static void CellDisplayingEnded (IUITableViewDelegate This, UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public static MonoTouch.Foundation.NSIndexPath CustomizeMoveTarget (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath proposedIndexPath);
	public static void DidEndEditing (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static UITableViewCellEditingStyle EditingStyleForRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static float EstimatedHeight (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static float EstimatedHeightForFooter (IUITableViewDelegate This, UITableView tableView, int section);
	public static float EstimatedHeightForHeader (IUITableViewDelegate This, UITableView tableView, int section);
	public static void FooterViewDisplayingEnded (IUITableViewDelegate This, UITableView tableView, UIView footerView, int section);
	public static float GetHeightForFooter (IUITableViewDelegate This, UITableView tableView, int section);
	public static float GetHeightForHeader (IUITableViewDelegate This, UITableView tableView, int section);
	public static float GetHeightForRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static UIView GetViewForFooter (IUITableViewDelegate This, UITableView tableView, int section);
	public static UIView GetViewForHeader (IUITableViewDelegate This, UITableView tableView, int section);
	public static void HeaderViewDisplayingEnded (IUITableViewDelegate This, UITableView tableView, UIView headerView, int section);
	public static int IndentationLevel (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void PerformAction (IUITableViewDelegate This, UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
	public static void RowDeselected (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void RowHighlighted (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
	public static void RowSelected (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void RowUnhighlighted (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
	public static bool ShouldHighlightRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
	public static bool ShouldIndentWhileEditing (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static bool ShouldShowMenu (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath rowAtindexPath);
	public static string TitleForDeleteConfirmation (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void WillBeginEditing (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static MonoTouch.Foundation.NSIndexPath WillDeselectRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void WillDisplay (IUITableViewDelegate This, UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
	public static void WillDisplayFooterView (IUITableViewDelegate This, UITableView tableView, UIView footerView, int section);
	public static void WillDisplayHeaderView (IUITableViewDelegate This, UITableView tableView, UIView headerView, int section);
	public static MonoTouch.Foundation.NSIndexPath WillSelectRow (IUITableViewDelegate This, UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextFieldDelegate</h3>
<p>Removed:</p><pre>
 public class UITextFieldDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UITextFieldDelegate : MonoTouch.Foundation.NSObject, IUITextFieldDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITextFieldDelegate_Extensions</h3>
<pre>
public static class UITextFieldDelegate_Extensions {
	
	public static void EditingEnded (IUITextFieldDelegate This, UITextField textField);
	public static void EditingStarted (IUITextFieldDelegate This, UITextField textField);
	public static bool ShouldBeginEditing (IUITextFieldDelegate This, UITextField textField);
	public static bool ShouldChangeCharacters (IUITextFieldDelegate This, UITextField textField, MonoTouch.Foundation.NSRange range, string replacementString);
	public static bool ShouldClear (IUITextFieldDelegate This, UITextField textField);
	public static bool ShouldEndEditing (IUITextFieldDelegate This, UITextField textField);
	public static bool ShouldReturn (IUITextFieldDelegate This, UITextField textField);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextInputDelegate</h3>
<p>Removed:</p><pre>
 public abstract class UITextInputDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UITextInputDelegate : MonoTouch.Foundation.NSObject, IUITextInputDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITextInputDelegate_Extensions</h3>
<pre>
public static class UITextInputDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextInputTokenizer</h3>
<p>Removed:</p><pre>
 public abstract class UITextInputTokenizer : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UITextInputTokenizer : MonoTouch.Foundation.NSObject, IUITextInputTokenizer {
</pre>
<h3>New Type: MonoTouch.UIKit.UITextInputTokenizer_Extensions</h3>
<pre>
public static class UITextInputTokenizer_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextViewDelegate</h3>
<p>Removed:</p><pre>
 public class UITextViewDelegate : UIScrollViewDelegate {
</pre>
<p>Added:</p><pre>
 public class UITextViewDelegate : UIScrollViewDelegate, IUITextViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UITextViewDelegate_Extensions</h3>
<pre>
public static class UITextViewDelegate_Extensions {
	
	public static void Changed (IUITextViewDelegate This, UITextView textView);
	public static void EditingEnded (IUITextViewDelegate This, UITextView textView);
	public static void EditingStarted (IUITextViewDelegate This, UITextView textView);
	public static void SelectionChanged (IUITextViewDelegate This, UITextView textView);
	public static bool ShouldBeginEditing (IUITextViewDelegate This, UITextView textView);
	public static bool ShouldChangeText (IUITextViewDelegate This, UITextView textView, MonoTouch.Foundation.NSRange range, string text);
	public static bool ShouldEndEditing (IUITextViewDelegate This, UITextView textView);
	public static bool ShouldInteractWithTextAttachment (IUITextViewDelegate This, UITextView textView, NSTextAttachment textAttachment, MonoTouch.Foundation.NSRange characterRange);
	public static bool ShouldInteractWithUrl (IUITextViewDelegate This, UITextView textView, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSRange characterRange);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbarDelegate</h3>
<p>Removed:</p><pre>
 public class UIToolbarDelegate : UIBarPositioningDelegate {
</pre>
<p>Added:</p><pre>
 public class UIToolbarDelegate : UIBarPositioningDelegate, IUIToolbarDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIToolbarDelegate_Extensions</h3>
<pre>
public static class UIToolbarDelegate_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIVideoEditorControllerDelegate : UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class UIVideoEditorControllerDelegate : UINavigationControllerDelegate, IUIVideoEditorControllerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIVideoEditorControllerDelegate_Extensions</h3>
<pre>
public static class UIVideoEditorControllerDelegate_Extensions {
	
	public static void Failed (IUIVideoEditorControllerDelegate This, UIVideoEditorController editor, MonoTouch.Foundation.NSError error);
	public static void UserCancelled (IUIVideoEditorControllerDelegate This, UIVideoEditorController editor);
	public static void VideoSaved (IUIVideoEditorControllerDelegate This, UIVideoEditorController editor, string editedVideoPath);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre>
 public class UIView : UIResponder, System.Collections.IEnumerable {
</pre>
<p>Added:</p><pre>
 public class UIView : UIResponder, System.Collections.IEnumerable, IUIDynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject BottomLayoutGuide {
 	public virtual MonoTouch.Foundation.NSObject TopLayoutGuide {
</pre>
<p>Added:</p><pre>
 	public virtual IUILayoutSupport BottomLayoutGuide {
 	public virtual IUILayoutSupport TopLayoutGuide {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIWebViewDelegate</h3>
<p>Removed:</p><pre>
 public class UIWebViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIWebViewDelegate : MonoTouch.Foundation.NSObject, IUIWebViewDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIWebViewDelegate_Extensions</h3>
<pre>
public static class UIWebViewDelegate_Extensions {
	
	public static void LoadFailed (IUIWebViewDelegate This, UIWebView webView, MonoTouch.Foundation.NSError error);
	public static void LoadingFinished (IUIWebViewDelegate This, UIWebView webView);
	public static void LoadStarted (IUIWebViewDelegate This, UIWebView webView);
	public static bool ShouldStartLoad (IUIWebViewDelegate This, UIWebView webView, MonoTouch.Foundation.NSUrlRequest request, UIWebViewNavigationType navigationType);
}
</pre>
<h2>Namespace: MonoTouch.iAd</h2>
<h3>Type Changed: MonoTouch.iAd.ADBannerViewDelegate</h3>
<p>Removed:</p><pre>
 public class ADBannerViewDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class ADBannerViewDelegate : MonoTouch.Foundation.NSObject, IADBannerViewDelegate {
</pre>
<h3>New Type: MonoTouch.iAd.ADBannerViewDelegate_Extensions</h3>
<pre>
public static class ADBannerViewDelegate_Extensions {
	
	public static void ActionFinished (IADBannerViewDelegate This, ADBannerView banner);
	public static bool ActionShouldBegin (IADBannerViewDelegate This, ADBannerView banner, bool willLeaveApplication);
	public static void AdLoaded (IADBannerViewDelegate This, ADBannerView banner);
	public static void FailedToReceiveAd (IADBannerViewDelegate This, ADBannerView banner, MonoTouch.Foundation.NSError error);
	public static void WillLoad (IADBannerViewDelegate This, ADBannerView bannerView);
}
</pre>
<h3>Type Changed: MonoTouch.iAd.ADInterstitialAdDelegate</h3>
<p>Removed:</p><pre>
 public abstract class ADInterstitialAdDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class ADInterstitialAdDelegate : MonoTouch.Foundation.NSObject, IADInterstitialAdDelegate {
</pre>
<h3>New Type: MonoTouch.iAd.ADInterstitialAdDelegate_Extensions</h3>
<pre>
public static class ADInterstitialAdDelegate_Extensions {
	
	public static void WillLoad (IADInterstitialAdDelegate This, ADInterstitialAd interstitialAd);
}
</pre>
<h3>New Type: MonoTouch.iAd.IADBannerViewDelegate</h3>
<pre>
public interface IADBannerViewDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.iAd.IADInterstitialAdDelegate</h3>
<pre>
public interface IADInterstitialAdDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void ActionFinished (ADInterstitialAd interstitialAd);
	bool ActionShouldBegin (ADInterstitialAd interstitialAd, bool willLeaveApplication);
	void AdLoaded (ADInterstitialAd interstitialAd);
	void AdUnloaded (ADInterstitialAd interstitialAd);
	void FailedToReceiveAd (ADInterstitialAd interstitialAd, MonoTouch.Foundation.NSError error);
}
</pre>
</body>
</html>
