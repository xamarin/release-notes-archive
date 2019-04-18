---
id: B5472587-3A5D-4D31-8154-960EAF14F19F
title: "From 6.4.3 to 6.9.6"
---

<html><head><title>Comparison between monotouch-6.4.3.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.4.3";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.6";
 	public const string JavaScriptCoreLibrary = "/System/Library/Frameworks/JavaScriptCore.framework/JavaScriptCore";
 	public const string GameControllerLibrary = "/System/Library/Frameworks/GameController.framework/GameController";
 	public const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";
 	public const string SpriteKitLibrary = "/System/Library/Frameworks/SpriteKit.framework/SpriteKit";
 	public const string SafariServicesLibrary = "/System/Library/Frameworks/SafariServices.framework/SafariServices";
 	public const string MediaAccessibilityLibrary = "/System/Library/Frameworks/MediaAccessibility.framework/MediaAccessibility";
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
<h3>New Type: MonoTouch.AVFoundation.AVSpeechBoundary</h3>
<pre>
[Serializable]
public enum AVSpeechBoundary {
	Immediate,
	Word
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesisVoice</h3>
<pre>
public class AVSpeechSynthesisVoice : MonoTouch.Foundation.NSObject {
	
	public AVSpeechSynthesisVoice ();
	public AVSpeechSynthesisVoice (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesisVoice (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesisVoice (IntPtr handle);
	
	public static AVSpeechSynthesisVoice FromLanguage (string language);
	public static AVSpeechSynthesisVoice[] GetSpeechVoices ();
	
	public static string CurrentLanguageCode {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Language {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizer</h3>
<pre>
public class AVSpeechSynthesizer : MonoTouch.Foundation.NSObject {
	
	public AVSpeechSynthesizer ();
	public AVSpeechSynthesizer (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesizer (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesizer (IntPtr handle);
	
	public virtual bool ContinueSpeaking ();
	protected override void Dispose (bool disposing);
	public virtual bool PauseSpeaking (AVSpeechBoundary boundary);
	public virtual void SpeakUtterance (AVSpeechUtterance utterance);
	public virtual bool StopSpeaking (AVSpeechBoundary boundary);
	
	public override IntPtr ClassHandle {
		get;
	}
	public AVSpeechSynthesizerDelegate Delegate {
		get;
		set;
	}
	public virtual bool Paused {
		get;
	}
	public virtual bool Speaking {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidCancelSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidContinueSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidFinishSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidPauseSpeechUtterance;
	public event EventHandler<avspeechsynthesizeruteranceeventargs> DidStartSpeechUtterance;
	public event EventHandler<avspeechsynthesizerwillspeakeventargs> WillSpeakRangeOfSpeechString;
}
</avspeechsynthesizerwillspeakeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></avspeechsynthesizeruteranceeventargs></pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerDelegate</h3>
<pre>
public class AVSpeechSynthesizerDelegate : MonoTouch.Foundation.NSObject, IAVSpeechSynthesizerDelegate {
	
	public AVSpeechSynthesizerDelegate ();
	public AVSpeechSynthesizerDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechSynthesizerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechSynthesizerDelegate (IntPtr handle);
	
	public virtual void DidCancelSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidContinueSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidFinishSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidPauseSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void DidStartSpeechUtterance (AVSpeechSynthesizer synthesizer, AVSpeechUtterance utterance);
	public virtual void WillSpeakRangeOfSpeechString (AVSpeechSynthesizer synthesizer, MonoTouch.Foundation.NSRange characterRange, AVSpeechUtterance utterance);
}
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
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerUteranceEventArgs</h3>
<pre>
public class AVSpeechSynthesizerUteranceEventArgs : EventArgs {
	
	public AVSpeechSynthesizerUteranceEventArgs (AVSpeechUtterance utterance);
	
	public AVSpeechUtterance Utterance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechSynthesizerWillSpeakEventArgs</h3>
<pre>
public class AVSpeechSynthesizerWillSpeakEventArgs : EventArgs {
	
	public AVSpeechSynthesizerWillSpeakEventArgs (MonoTouch.Foundation.NSRange characterRange, AVSpeechUtterance utterance);
	
	public MonoTouch.Foundation.NSRange CharacterRange {
		get;
		set;
	}
	public AVSpeechUtterance Utterance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVSpeechUtterance</h3>
<pre>
public class AVSpeechUtterance : MonoTouch.Foundation.NSObject {
	
	public AVSpeechUtterance ();
	public AVSpeechUtterance (MonoTouch.Foundation.NSCoder coder);
	public AVSpeechUtterance (MonoTouch.Foundation.NSObjectFlag t);
	public AVSpeechUtterance (IntPtr handle);
	public AVSpeechUtterance (string speechString);
	
	public static AVSpeechUtterance FromString (string speechString);
	protected override void Dispose (bool disposing);
	
	public static float DefaultSpeechRate {
		get;
	}
	public static float MaximumSpeechRate {
		get;
	}
	public static float MinimumSpeechRate {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float PitchMultiplier {
		get;
		set;
	}
	public virtual double PostUtteranceDelay {
		get;
		set;
	}
	public virtual double PreUtteranceDelay {
		get;
		set;
	}
	public virtual float Rate {
		get;
		set;
	}
	public virtual string SpeechString {
		get;
	}
	public virtual AVSpeechSynthesisVoice Voice {
		get;
		set;
	}
	public virtual float Volume {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ProfileLevelH264BaselineAutoLevel {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProfileLevelH264HighAutoLevel {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProfileLevelH264MainAutoLevel {
 		get;
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
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccount</h3>
<p>Added:</p><pre>
 	public virtual string UserFullName {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Accounts.ACAccountType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString TencentWeibo {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Accounts.ACErrorCode</h3>
<p>Removed:</p><pre>
 	AccessInfoInvalid
</pre>
<p>Added:</p><pre>
 	AccessInfoInvalid,
 	ClientPermissionDenied,
 	AccessDeniedByProtectionPolicy,
 	CredentialNotFound,
 	FetchCredentialFailed,
 	StoreCredentialFailed,
 	RemoveCredentialFailed,
 	UpdatingNonexistentAccount,
 	InvalidClientBundleID
</pre>
<h3>New Type: MonoTouch.Accounts.ACTencentWeiboKey</h3>
<pre>
public static class ACTencentWeiboKey {
	
	public static MonoTouch.Foundation.NSString AppId {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Accounts.AccountStoreOptions</h3>
<p>Added:</p><pre>
 	public string TencentWeiboAppId {
 		get;
 		set;
 	}
</pre>
<h2>Namespace: MonoTouch.AddressBook</h2>
<h3>Type Changed: MonoTouch.AddressBook.ABPerson</h3>
<p>Removed:</p><pre>
 	public static ABPersonCompositeNameFormat CompositeNameFormat {
</pre>
<p>Added:</p><pre>
 	public static string GetCompositeNameDelimiter (ABRecord record);
 	public static ABPersonCompositeNameFormat GetCompositeNameFormat (ABRecord record);
 	[Obsolete("Deprecated in iOS 7.0 in favor of GetCompositeNameFormat(null)")]
	public static ABPersonCompositeNameFormat CompositeNameFormat {
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
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (MonoTouch.UIKit.UINavigationController navigationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
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
<h3>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayoutTag</h3>
<p>Added:</p><pre>
 	AAC_7_1_B,
 	AAC_7_1_C,
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioFileProperty</h3>
<p>Removed:</p><pre>
 	AverageBytesPerPacket
</pre>
<p>Added:</p><pre>
 	AverageBytesPerPacket,
 	AudioTrackCount,
 	UseAudioTrack
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioFileStreamProperty</h3>
<p>Removed:</p><pre>
 	BitRate
</pre>
<p>Added:</p><pre>
 	BitRate,
 	InfoDictionary
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioQueueParameter</h3>
<p>Added:</p><pre>
 	PlayRate,
 	Pitch,
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioQueueProperty</h3>
<p>Added:</p><pre>
 	EnableTimePitch,
 	TimePitchAlgorithm,
 	TimePitchBypass,
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioQueueTimePitchAlgorithm</h3>
<pre>
[Serializable]
public enum AudioQueueTimePitchAlgorithm : uint {
	Spectral,
	TimeDomain,
	LowQualityZeroLatency,
	Varispeed
}
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSession</h3>
<p>Removed:</p><pre>
 	public static AudioSessionErrors AddListener (AudioSessionProperty property, PropertyListener listener);
 	public static void Initialize ();
 	public static void SetActive (bool active);
 	public static AudioSessionErrors SetActive (bool active, AudioSessionActiveFlags flags);
 	public static bool AudioInputAvailable {
 	public static bool AudioShouldDuck {
 	public static AudioSessionCategory Category {
 	public static float CurrentHardwareInputLatency {
 	public static int CurrentHardwareInputNumberChannels {
 	public static float CurrentHardwareIOBufferDuration {
 	public static float CurrentHardwareOutputLatency {
 	public static int CurrentHardwareOutputNumberChannels {
 	public static float CurrentHardwareOutputVolume {
 	public static double CurrentHardwareSampleRate {
 	public static bool InputGainAvailable {
 	public static float InputGainScalar {
 	public static AudioSessionInterruptionType InterruptionType {
 	public static AudioSessionMode Mode {
 	public static bool OtherAudioIsPlaying {
 	public static bool OverrideCategoryDefaultToSpeaker {
 	public static bool OverrideCategoryEnableBluetoothInput {
 	public static bool OverrideCategoryMixWithOthers {
 	public static float PreferredHardwareIOBufferDuration {
 	public static double PreferredHardwareSampleRate {
 	public static AudioSessionRoutingOverride RoutingOverride {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public static AudioSessionErrors AddListener (AudioSessionProperty property, PropertyListener listener);
 	[Obsolete("Deprecated in iOS7")]
	public static void Initialize ();
 	[Obsolete("Deprecated in iOS7")]
	public static void SetActive (bool active);
 	[Obsolete("Deprecated in iOS7")]
	public static AudioSessionErrors SetActive (bool active, AudioSessionActiveFlags flags);
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool AudioInputAvailable {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool AudioShouldDuck {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionCategory Category {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareInputLatency {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static int CurrentHardwareInputNumberChannels {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareIOBufferDuration {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareOutputLatency {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static int CurrentHardwareOutputNumberChannels {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareOutputVolume {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static double CurrentHardwareSampleRate {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool InputGainAvailable {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float InputGainScalar {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionInterruptionType InterruptionType {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionMode Mode {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OtherAudioIsPlaying {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryDefaultToSpeaker {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryEnableBluetoothInput {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryMixWithOthers {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float PreferredHardwareIOBufferDuration {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static double PreferredHardwareSampleRate {
 	[Obsolete("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionRoutingOverride RoutingOverride {
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSessionRouteChangeEventArgs</h3>
<p>Removed:</p><pre>
 	public AudioSessionRouteChangeReason Reason {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public AudioSessionRouteChangeReason Reason {
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSessionRouteChangeReason</h3>
<p>Removed:</p><pre>
 	NoSuitableRouteForCategory
</pre>
<p>Added:</p><pre>
 	NoSuitableRouteForCategory,
 	RouteConfigurationChange
</pre>
<h3>New Type: MonoTouch.AudioToolbox.InstrumentInfo</h3>
<pre>
public class InstrumentInfo {
	
	public MonoTouch.Foundation.NSDictionary Dictionary {
		get;
	}
	public int LSB {
		get;
	}
	public int MSB {
		get;
	}
	public string Name {
		get;
	}
	public int Program {
		get;
	}
	
	public const string NameKey = "name";
	public const string MSBKey = "MSB";
	public const string LSBKey = "LSB";
	public const string ProgramKey = "program";
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.SoundBank</h3>
<pre>
public class SoundBank {
	
	public SoundBank ();
	
	public static InstrumentInfo[] GetInstrumentInfo (MonoTouch.Foundation.NSUrl url);
	public static string GetName (MonoTouch.Foundation.NSUrl url);
}
</pre>
<h2>Namespace: MonoTouch.AudioUnit</h2>
<h3>Type Changed: MonoTouch.AudioUnit.ExtAudioFileError</h3>
<p>Removed:</p><pre>
 	FileNotFoundError
</pre>
<p>Added:</p><pre>
 	FileNotFoundError,
 	BadFilePathError,
 	FilePermissionError,
 	TooManyFilesOpenError
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
<h3>New Type: MonoTouch.CoreAnimation.CAEmitterBehavior</h3>
<pre>
public class CAEmitterBehavior : MonoTouch.Foundation.NSObject {
	
	public CAEmitterBehavior ();
	public CAEmitterBehavior (MonoTouch.Foundation.NSCoder coder);
	public CAEmitterBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public CAEmitterBehavior (IntPtr handle);
	public CAEmitterBehavior (MonoTouch.Foundation.NSString type);
	
	public static CAEmitterBehavior Create (MonoTouch.Foundation.NSString type);
	
	public static MonoTouch.Foundation.NSString AlignToMotion {
		get;
	}
	public static MonoTouch.Foundation.NSString Attractor {
		get;
	}
	public static MonoTouch.Foundation.NSString[] BehaviorTypes {
		get;
	}
	public static MonoTouch.Foundation.NSString ColorOverLife {
		get;
	}
	public static MonoTouch.Foundation.NSString Drag {
		get;
	}
	public static MonoTouch.Foundation.NSString Light {
		get;
	}
	public static MonoTouch.Foundation.NSString ValueOverLife {
		get;
	}
	public static MonoTouch.Foundation.NSString Wave {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Enabled {
		get;
		set;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual string Type {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreAnimation.CALayer</h3>
<p>Added:</p><pre>
 	public virtual bool AllowsEdgeAntialiasing {
 		get;
 		set;
 	}
 	public virtual bool AllowsGroupOpacity {
 		get;
 		set;
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
<h3>Type Changed: MonoTouch.CoreBluetooth.CBAdvertisement</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString DataSolicitedServiceUUIDsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString IsConnectable {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentral</h3>
<p>Removed:</p><pre>
 	public virtual IntPtr UUID {
</pre>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	
 	public virtual MonoTouch.Foundation.NSUuid Identifier {
 		get;
 	}
 	public virtual uint MaximumUpdateValueLength {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual IntPtr UUID {
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Removed:</p><pre>
 	public virtual void RetrieveConnectedPeripherals ();
 	public void RetrievePeripherals (CBUUID[] peripheralUuids);
</pre>
<p>Added:</p><pre>
 	public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSDictionary options);
 	[Obsolete("Deprecated in iOS7")]
	public virtual void RetrieveConnectedPeripherals ();
 	public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);
 	[Obsolete("Deprecated in iOS7")]
	public void RetrievePeripherals (CBUUID[] peripheralUuids);
 	public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (CBUUID[] identifiers);
 	public static MonoTouch.Foundation.NSString OptionRestoreIdentifierKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OptionShowPowerAlertKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RestoredStatePeripheralsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RestoredStateScanOptionsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RestoredStateScanServicesKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ScanOptionSolicitedServiceUUIDsKey {
 		get;
 	}
 	public event EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class CBCentralManagerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class CBCentralManagerDelegate : MonoTouch.Foundation.NSObject, ICBCentralManagerDelegate {
 	public virtual void WillRestoreState (CBCentralManager central, MonoTouch.Foundation.NSDictionary dict);
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
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCharacteristic</h3>
<p>Added:</p><pre>
 	public virtual CBCentral[] SubscribedCentrals {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Removed:</p><pre>
 	public virtual bool IsConnected {
 	public virtual IntPtr UUID {
 	public event EventHandler InvalidatedService;
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSUuid Identifier {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual bool IsConnected {
 	public virtual CBPeripheralState State {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual IntPtr UUID {
 	[Obsolete("Deprecated in iOS7")]
	public event EventHandler InvalidatedService;
 	public event EventHandler&lt;CBPeripheralServicesEventArgs&gt; ModifiedServices;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 public class CBPeripheralDelegate : MonoTouch.Foundation.NSObject {
 	public virtual void InvalidatedService (CBPeripheral peripheral);
</pre>
<p>Added:</p><pre>
 public class CBPeripheralDelegate : MonoTouch.Foundation.NSObject, ICBPeripheralDelegate {
 	[Obsolete("Deprecated in iOS7")]
	public virtual void InvalidatedService (CBPeripheral peripheral);
 	public virtual void ModifiedServices (CBPeripheral peripheral, CBService[] services);
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
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<p>Added:</p><pre>
 	public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSDictionary options);
 	public static CBPeripheralManagerAuthorizationStatus AuthorizationStatus {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OptionRestoreIdentifierKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OptionShowPowerAlertKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RestoredStateAdvertisementDataKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RestoredStateServicesKey {
 		get;
 	}
 	public event EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerAuthorizationStatus</h3>
<pre>
[Serializable]
public enum CBPeripheralManagerAuthorizationStatus {
	NotDetermined,
	Restricted,
	Denied,
	Authorized
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<p>Removed:</p><pre>
 public abstract class CBPeripheralManagerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class CBPeripheralManagerDelegate : MonoTouch.Foundation.NSObject, ICBPeripheralManagerDelegate {
 	public virtual void WillRestoreState (CBPeripheralManager peripheral, MonoTouch.Foundation.NSDictionary dict);
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
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralServicesEventArgs</h3>
<pre>
public class CBPeripheralServicesEventArgs : EventArgs {
	
	public CBPeripheralServicesEventArgs (CBService[] services);
	
	public CBService[] Services {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralState</h3>
<pre>
[Serializable]
public enum CBPeripheralState {
	Disconnected,
	Connecting,
	Connected
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBUUID</h3>
<p>Added:</p><pre>
 	public static CBUUID FromNSUuid (MonoTouch.Foundation.NSUuid theUUID);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBWillRestoreEventArgs</h3>
<pre>
public class CBWillRestoreEventArgs : EventArgs {
	
	public CBWillRestoreEventArgs (MonoTouch.Foundation.NSDictionary dict);
	
	public MonoTouch.Foundation.NSDictionary Dict {
		get;
		set;
	}
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
<h3>Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator</h3>
<p>Added:</p><pre>
 	public static bool RemoveUbiquitousContentAndPersistentStore (MonoTouch.Foundation.NSUrl storeUrl, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
 	public static MonoTouch.Foundation.NSString eUbiquitousContainerIdentifierKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousPeerTokenOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousTransitionTypeKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RebuildFromUbiquitousContentOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RemoveUbiquitousMetadataOption {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StoresWillChangeNotification {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveDidImportUbiquitousContentChanges (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveStoresDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveStoresWillChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveWillRemoveStore (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoTouch.CoreData.NSPersistentStoreUbiquitousTransitionType</h3>
<pre>
[Serializable]
public enum NSPersistentStoreUbiquitousTransitionType {
	AccountAdded,
	AccountRemoved,
	ContentRemoved,
	InitialImportCompleted
}
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.CFStream</h3>
<p>Added:</p><pre>
 	public DispatchQueue ReadDispatchQueue {
 		get;
 		set;
 	}
 	public DispatchQueue WriteDispatchQueue {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.CFUrl</h3>
<p>Added:</p><pre>
 	public bool IsFileReference {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchQueue</h3>
<p>Removed:</p><pre>
 public class DispatchQueue : DispatchObject {
</pre>
<p>Added:</p><pre>
 public sealed class DispatchQueue : DispatchObject {
 	public override bool Equals (object other);
 	public override int GetHashCode ();
 	public static bool operator == (DispatchQueue left, DispatchQueue right);
 	public static bool operator != (DispatchQueue left, DispatchQueue right);
 	
 	public static string CurrentQueueLabel {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.CoreGraphics</h2>
<h3>Type Changed: MonoTouch.CoreGraphics.CGColorSpace</h3>
<p>Added:</p><pre>
 	public static CGColorSpace CreateICCProfile (MonoTouch.Foundation.NSData data);
 	public static CGColorSpace CreateICCProfile (float [] range, CGDataProvider profile, CGColorSpace alternate);
 	public MonoTouch.Foundation.NSData GetICCProfile ();
</pre>
<h3>Type Changed: MonoTouch.CoreGraphics.CGContext</h3>
<p>Removed:</p><pre>
 	public void SelectFont (string name, float size, CGTextEncoding textEncoding);
 	public void ShowGlyphs (ushort [] glyphs);
 	public void ShowGlyphs (ushort [] glyphs, int count);
 	public void ShowGlyphsAtPoint (float x, float y, ushort [] glyphs);
 	public void ShowGlyphsAtPoint (float x, float y, ushort [] glyphs, int count);
 	public void ShowGlyphsWithAdvances (ushort [] glyphs, System.Drawing.SizeF [] advances, int count);
 	public void ShowText (byte [] bytes);
 	public void ShowText (byte [] bytes, int count);
 	public void ShowText (string str);
 	public void ShowText (string str, int count);
 	public void ShowTextAtPoint (float x, float y, string str);
 	public void ShowTextAtPoint (float x, float y, string str, int length);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void SelectFont (string name, float size, CGTextEncoding textEncoding);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphs (ushort [] glyphs);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphs (ushort [] glyphs, int count);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsAtPoint (float x, float y, ushort [] glyphs);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsAtPoint (float x, float y, ushort [] glyphs, int count);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsWithAdvances (ushort [] glyphs, System.Drawing.SizeF [] advances, int count);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (byte [] bytes);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (byte [] bytes, int count);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (string str);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (string str, int count);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowTextAtPoint (float x, float y, string str);
 	[Obsolete("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowTextAtPoint (float x, float y, string str, int length);
</pre>
<h3>Type Changed: MonoTouch.CoreGraphics.CGPath</h3>
<p>Added:</p><pre>
 	public static CGPath FromRoundedRect (System.Drawing.RectangleF rectangle, float cornerWidth, float cornerHeight);
 	public static CGPath FromRoundedRect (System.Drawing.RectangleF rectangle, float cornerWidth, float cornerHeight, CGAffineTransform transform);
 	public void AddRoundedRect (CGAffineTransform transform, System.Drawing.RectangleF rect, float cornerWidth, float cornerHeight);
 	public void AddRoundedRect (System.Drawing.RectangleF rect, float cornerWidth, float cornerHeight);
</pre>
<h3>Type Changed: MonoTouch.CoreGraphics.CGTextEncoding</h3>
<p>Removed:</p><pre>
 public enum CGTextEncoding {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public enum CGTextEncoding {
</pre>
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
<h2>Namespace: MonoTouch.CoreImage</h2>
<h3>Type Changed: MonoTouch.CoreImage.CIDetector</h3>
<p>Added:</p><pre>
 	public static CIDetector CreateFaceDetector (CIContext context, CIDetectorOptions detectorOptions);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIDetectorKeys</h3>
<pre>
public static class CIDetectorKeys {
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIDetectorOptions</h3>
<pre>
public class CIDetectorOptions {
	
	public CIDetectorOptions ();
	
	public Nullable<facedetectoraccuracy> Accuracy {
		get;
		set;
	}
	public Nullable<bool> EyeBlink {
		get;
		set;
	}
	public Nullable<float> MinFeatureSize {
		get;
		set;
	}
	public Nullable<bool> Smile {
		get;
		set;
	}
	public Nullable<bool> TrackingEnabled {
		get;
		set;
	}
}
</bool></bool></float></bool></facedetectoraccuracy></pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFaceFeature</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF Bounds {
 		get;
 	}
 	public virtual float FaceAngle {
 		get;
 	}
 	public virtual bool HasFaceAngle {
 		get;
 	}
 	public virtual bool HasSmile {
 		get;
 	}
 	public virtual bool LeftEyeClosed {
 		get;
 	}
 	public virtual bool RightEyeClosed {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFilterInputKey</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Angle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AspectRatio {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Brightness {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Center {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Color {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Contrast {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString EV {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Extent {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Intensity {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MaskImage {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Radius {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Saturation {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Scale {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Sharpness {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TargetImage {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Time {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Transform {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Width {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIImage</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF GetRegionOfInterest (CIImage im, System.Drawing.RectangleF r);
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>New Type: MonoTouch.CoreLocation.CLBeacon</h3>
<pre>
public class CLBeacon : MonoTouch.Foundation.NSObject {
	
	public CLBeacon ();
	public CLBeacon (MonoTouch.Foundation.NSCoder coder);
	public CLBeacon (MonoTouch.Foundation.NSObjectFlag t);
	public CLBeacon (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual double Accuracy {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber Major {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber Minor {
		get;
	}
	public virtual CLProximity Proximity {
		get;
	}
	public virtual MonoTouch.Foundation.NSUuid ProximityUuid {
		get;
	}
	public virtual int Rssi {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLBeaconRegion</h3>
<pre>
public class CLBeaconRegion : CLRegion {
	
	public CLBeaconRegion ();
	public CLBeaconRegion (MonoTouch.Foundation.NSCoder coder);
	public CLBeaconRegion (MonoTouch.Foundation.NSObjectFlag t);
	public CLBeaconRegion (IntPtr handle);
	public CLBeaconRegion (MonoTouch.Foundation.NSUuid proximityUuid, string identifier);
	public CLBeaconRegion (MonoTouch.Foundation.NSUuid proximityUuid, ushort major, string identifier);
	public CLBeaconRegion (MonoTouch.Foundation.NSUuid proximityUuid, ushort major, ushort minor, string identifier);
	
	protected override void Dispose (bool disposing);
	public virtual MonoTouch.Foundation.NSMutableDictionary GetPeripheralData (MonoTouch.Foundation.NSNumber measuredPower);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber Major {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber Minor {
		get;
	}
	public virtual bool NotifyEntryStateOnDisplay {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSUuid ProximityUuid {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLCircularRegion</h3>
<pre>
public class CLCircularRegion : CLRegion {
	
	public CLCircularRegion ();
	public CLCircularRegion (MonoTouch.Foundation.NSCoder coder);
	public CLCircularRegion (MonoTouch.Foundation.NSObjectFlag t);
	public CLCircularRegion (IntPtr handle);
	public CLCircularRegion (CLLocationCoordinate2D center, double radius, string identifier);
	
	public virtual bool ContainsCoordinate (CLLocationCoordinate2D coordinate);
	
	public virtual CLLocationCoordinate2D Center {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Radius {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLError</h3>
<p>Removed:</p><pre>
 	DeferredCanceled
</pre>
<p>Added:</p><pre>
 	DeferredCanceled,
 	RangingFailure,
 	RangingUnavailable
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h3>
<p>Removed:</p><pre>
 	public static bool RegionMonitoringAvailable {
</pre>
<p>Added:</p><pre>
 	public static bool IsMonitoringAvailable (MonoTouch.ObjCRuntime.Class regionClass);
 	public virtual void RequestState (CLRegion region);
 	public virtual void StartRangingBeacons (CLBeaconRegion region);
 	public virtual void StopRangingBeacons (CLBeaconRegion region);
 	[Obsolete("Deprecated in iOS7 in favor of IsMonitoringAvailable")]
	public static bool RegionMonitoringAvailable {
 	public virtual MonoTouch.Foundation.NSSet RangedRegions {
 		get;
 	}
 	public event EventHandler&lt;CLRegionStateDeterminedEventArgs&gt; DidDetermineState;
 	public event EventHandler&lt;CLRegionBeaconsRangedEventArgs&gt; DidRangeBeacons;
 	public event EventHandler&lt;CLRegionBeaconsFailedEventArgs&gt; RangingBeaconsDidFailForRegion;
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DidDetermineState (CLLocationManager manager, CLRegionState state, CLRegion region);
 	public virtual void DidRangeBeacons (CLLocationManager manager, CLBeacon[] beacons, CLBeaconRegion region);
 	public virtual void RangingBeaconsDidFailForRegion (CLLocationManager manager, CLBeaconRegion region, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLProximity</h3>
<pre>
[Serializable]
public enum CLProximity {
	Unknown,
	Immediate,
	Near,
	Far
}
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLRegion</h3>
<p>Removed:</p><pre>
 	public CLRegion (CLLocationCoordinate2D center, double radius, string identifier);
 	public virtual bool Contains (CLLocationCoordinate2D coordinate);
 	public virtual CLLocationCoordinate2D Center {
 	public virtual double Radius {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of CLCircularRegion")]
	public CLRegion (CLLocationCoordinate2D center, double radius, string identifier);
 	[Obsolete("Deprecated in iOS7 in favor of CLCircularRegion")]
	public virtual bool Contains (CLLocationCoordinate2D coordinate);
 	[Obsolete("Deprecated in iOS7 in favor of CLCircularRegion")]
	public virtual CLLocationCoordinate2D Center {
 	public virtual bool NotifyOnEntry {
 		get;
 		set;
 	}
 	public virtual bool NotifyOnExit {
 		get;
 		set;
 	}
 	[Obsolete("Deprecated in iOS7 in favor of CLCircularRegion")]
	public virtual double Radius {
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLRegionBeaconsFailedEventArgs</h3>
<pre>
public class CLRegionBeaconsFailedEventArgs : EventArgs {
	
	public CLRegionBeaconsFailedEventArgs (CLBeaconRegion region, MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
	public CLBeaconRegion Region {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLRegionBeaconsRangedEventArgs</h3>
<pre>
public class CLRegionBeaconsRangedEventArgs : EventArgs {
	
	public CLRegionBeaconsRangedEventArgs (CLBeacon[] beacons, CLBeaconRegion region);
	
	public CLBeacon[] Beacons {
		get;
		set;
	}
	public CLBeaconRegion Region {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLRegionState</h3>
<pre>
[Serializable]
public enum CLRegionState {
	Unknown,
	Inside,
	Outside
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLRegionStateDeterminedEventArgs</h3>
<pre>
public class CLRegionStateDeterminedEventArgs : EventArgs {
	
	public CLRegionStateDeterminedEventArgs (CLRegionState state, CLRegion region);
	
	public CLRegion Region {
		get;
		set;
	}
	public CLRegionState State {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreMotion</h2>
<h3>Type Changed: MonoTouch.CoreMotion.CMError</h3>
<p>Removed:</p><pre>
 	TrueNorthNotAvailable
</pre>
<p>Added:</p><pre>
 	TrueNorthNotAvailable,
 	Unknown,
 	MotionActivityNotAvailable,
 	MotionActivityNotAuthorized,
 	MotionActivityNotEntitled,
 	InvalidParameter
</pre>
<h2>Namespace: MonoTouch.CoreServices</h2>
<h3>Type Changed: MonoTouch.CoreServices.CFHTTPMessage</h3>
<p>Removed:</p><pre>
 		Digest
</pre>
<p>Added:</p><pre>
 		Digest,
 		OAuth1
</pre>
<h2>Namespace: MonoTouch.CoreTelephony</h2>
<h3>New Type: MonoTouch.CoreTelephony.CTRadioAccessTechnology</h3>
<pre>
public static class CTRadioAccessTechnology {
	
	public static MonoTouch.Foundation.NSString CDMA1x {
		get;
	}
	public static MonoTouch.Foundation.NSString CDMAEVDORev0 {
		get;
	}
	public static MonoTouch.Foundation.NSString CDMAEVDORevA {
		get;
	}
	public static MonoTouch.Foundation.NSString CDMAEVDORevB {
		get;
	}
	public static MonoTouch.Foundation.NSString Edge {
		get;
	}
	public static MonoTouch.Foundation.NSString EHRPD {
		get;
	}
	public static MonoTouch.Foundation.NSString GPRS {
		get;
	}
	public static MonoTouch.Foundation.NSString HSDPA {
		get;
	}
	public static MonoTouch.Foundation.NSString HSUPA {
		get;
	}
	public static MonoTouch.Foundation.NSString LTE {
		get;
	}
	public static MonoTouch.Foundation.NSString WCDMA {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreTelephony.CTSubscriber</h3>
<pre>
public class CTSubscriber : MonoTouch.Foundation.NSObject {
	
	public CTSubscriber ();
	public CTSubscriber (MonoTouch.Foundation.NSCoder coder);
	public CTSubscriber (MonoTouch.Foundation.NSObjectFlag t);
	public CTSubscriber (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual MonoTouch.Foundation.NSData CarrierToken {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreTelephony.CTSubscriberInfo</h3>
<pre>
public class CTSubscriberInfo : MonoTouch.Foundation.NSObject {
	
	public CTSubscriberInfo ();
	public CTSubscriberInfo (MonoTouch.Foundation.NSCoder coder);
	public CTSubscriberInfo (MonoTouch.Foundation.NSObjectFlag t);
	public CTSubscriberInfo (IntPtr handle);
	
	public static CTSubscriber Subscriber {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreTelephony.CTTelephonyNetworkInfo</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString CurrentRadioAccessTechnology {
 		get;
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
<h3>Type Changed: MonoTouch.Foundation.DictionaryContainer</h3>
<p>Removed:</p><pre>
 	protected string GetNSStringValue (NSString key);
</pre>
<p>Added:</p><pre>
 	protected NSString GetNSStringValue (NSString key);
</pre>
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
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Added:</p><pre>
 	public NSAttributedString (NSUrl url, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSData GetDataFromRange (NSRange range, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public virtual NSData GetDataFromRange (NSRange range, NSDictionary attributes, ref NSError error);
 	public NSFileWrapper GetFileWrapperFromRange (NSRange range, NSAttributedStringDocumentAttributes documentAttributes, ref NSError error);
 	public virtual NSFileWrapper GetFileWrapperFromRange (NSRange range, NSDictionary attributes, ref NSError error);
</pre>
<h3>New Type: MonoTouch.Foundation.NSAttributedStringDocumentAttributes</h3>
<pre>
public class NSAttributedStringDocumentAttributes : DictionaryContainer {
	
	public NSAttributedStringDocumentAttributes ();
	public NSAttributedStringDocumentAttributes (NSDictionary dictionary);
	
	public MonoTouch.UIKit.UIColor BackgroundColor {
		get;
		set;
	}
	public Nullable<float> DefaultTabInterval {
		get;
		set;
	}
	public NSDocumentType DocumentType {
		get;
		set;
	}
	public Nullable<float> HyphenationFactor {
		get;
		set;
	}
	public System.Nullable<monotouch.uikit.uiedgeinsets> PaperMargin {
		get;
		set;
	}
	public System.Nullable<system.drawing.sizef> PaperSize {
		get;
		set;
	}
	public bool ReadOnly {
		get;
		set;
	}
	public Nullable<nsstringencoding> StringEncoding {
		get;
		set;
	}
	public Nullable<nsdocumentviewmode> ViewMode {
		get;
		set;
	}
	public System.Nullable<system.drawing.sizef> ViewSize {
		get;
		set;
	}
	public Nullable<float> ViewZoom {
		get;
		set;
	}
	public NSDictionary WeakDefaultAttributes {
		get;
		set;
	}
	public NSString WeakDocumentType {
		get;
		set;
	}
}
</float></system.drawing.sizef></nsdocumentviewmode></nsstringencoding></system.drawing.sizef></monotouch.uikit.uiedgeinsets></float></float></pre>
<h3>Type Changed: MonoTouch.Foundation.NSBundle</h3>
<p>Added:</p><pre>
 	public virtual NSUrl AppStoreReceiptUrl {
 		get;
 	}
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
 	public NSData (string base64String, NSDataBase64DecodingOptions options);
 	public NSData (NSData base64Data, NSDataBase64DecodingOptions options);
 	public NSData (IntPtr bytes, uint length, Action&lt;IntPtr,uint&gt; deallocator);
 	public static NSData FromBytesNoCopy (IntPtr bytes, uint size);
 	public static NSData FromBytesNoCopy (IntPtr bytes, uint size, bool freeWhenDone);
 	public virtual void EnumerateByteRange (NSDataByteRangeEnumerator enumerator);
 	public virtual NSData GetBase64EncodedData (NSDataBase64EncodingOptions options);
 	public virtual string GetBase64EncodedString (NSDataBase64EncodingOptions options);
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataBase64DecodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64DecodingOptions {
	None,
	IgnoreUnknownCharacters
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataBase64EncodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64EncodingOptions {
	None,
	SixtyFourCharacterLineLength,
	SeventySixCharacterLineLength,
	EndLineWithCarriageReturn,
	EndLineWithLineFeed
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSDataByteRangeEnumerator</h3>
<pre>
[Serializable]
public delegate void NSDataByteRangeEnumerator (IntPtr bytes, NSRange range, ref bool stop);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDateComponentsWrappingBehavior</h3>
<p>Added:</p><pre>
 [Flags]
</pre>
<h3>New Type: MonoTouch.Foundation.NSDocumentType</h3>
<pre>
[Serializable]
public enum NSDocumentType {
	Unknown,
	PlainText,
	RTF,
	RTFD
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSDocumentViewMode</h3>
<pre>
[Serializable]
public enum NSDocumentViewMode {
	Normal,
	PageLayout
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSFileManager</h3>
<p>Added:</p><pre>
 	public virtual NSUrl GetContainerUrl (string securityApplicationGroupIdentifier);
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
<h3>Type Changed: MonoTouch.Foundation.NSLocale</h3>
<p>Added:</p><pre>
 	public static NSLocale FromLocaleIdentifier (string ident);
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
<h3>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h3>
<p>Added:</p><pre>
 	public bool ReadFromData (NSData data, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);
 	public virtual bool ReadFromData (NSData data, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);
 	public bool ReadFromFile (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);
 	public virtual bool ReadFromFile (NSUrl url, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);
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
<h3>Type Changed: MonoTouch.Foundation.NSOrderedSet</h3>
<p>Added:</p><pre>
 	public override bool Equals (object other);
 	public override int GetHashCode ();
</pre>
<h3>New Type: MonoTouch.Foundation.NSProgress</h3>
<pre>
public class NSProgress : NSObject {
	
	public NSProgress ();
	public NSProgress (NSCoder coder);
	public NSProgress (NSObjectFlag t);
	public NSProgress (IntPtr handle);
	public NSProgress (NSProgress parentProgress, NSDictionary userInfo);
	
	public static NSProgress FromTotalUnitCount (long unitCount);
	public virtual void BecomeCurrent (long pendingUnitCount);
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public virtual void Pause ();
	public virtual void ResignCurrent ();
	public virtual void SetCancellationHandler (NSAction handler);
	public virtual void SetPauseHandler (NSAction handler);
	public virtual void SetUserInfo (NSObject obj, NSString key);
	
	public static NSProgress CurrentProgress {
		get;
	}
	public static NSString EstimatedTimeRemainingKey {
		get;
	}
	public static NSString FileCompletedCountKey {
		get;
	}
	public static NSString FileOperationKindCopying {
		get;
	}
	public static NSString FileOperationKindDecompressingAfterDownloading {
		get;
	}
	public static NSString FileOperationKindDownloading {
		get;
	}
	public static NSString FileOperationKindKey {
		get;
	}
	public static NSString FileOperationKindReceiving {
		get;
	}
	public static NSString FileTotalCountKey {
		get;
	}
	public static NSString FileURLKey {
		get;
	}
	public static NSString KindFile {
		get;
	}
	public static NSString ThroughputKey {
		get;
	}
	public virtual bool Cancellable {
		get;
		set;
	}
	public virtual bool Cancelled {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual long CompletedUnitCount {
		get;
		set;
	}
	public virtual double FractionCompleted {
		get;
	}
	public virtual bool Indeterminate {
		get;
	}
	public virtual NSString Kind {
		get;
		set;
	}
	public virtual string LocalizedAdditionalDescription {
		get;
		set;
	}
	public virtual string LocalizedDescription {
		get;
		set;
	}
	public virtual bool Pausable {
		get;
		set;
	}
	public virtual bool Paused {
		get;
	}
	public virtual long TotalUnitCount {
		get;
		set;
	}
	public virtual NSDictionary UserInfo {
		get;
	}
}
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
<h3>Type Changed: MonoTouch.Foundation.NSStringDrawingContext</h3>
<p>Removed:</p><pre>
 	public virtual float ActualTrackingAdjustment {
 	public virtual float MinimumTrackingAdjustment {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual float ActualTrackingAdjustment {
 	[Obsolete("Deprecated in iOS7")]
	public virtual float MinimumTrackingAdjustment {
</pre>
<h3>New Type: MonoTouch.Foundation.NSTextWritingDirection</h3>
<pre>
[Serializable]
[Flags]
public enum NSTextWritingDirection {
	Embedding,
	Override
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSTimer</h3>
<p>Added:</p><pre>
 	public virtual double Tolerance {
 		get;
 		set;
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
<h3>Type Changed: MonoTouch.Foundation.NSUserDefaults</h3>
<p>Removed:</p><pre>
 	public NSUserDefaults (string username);
 	public virtual string [] PersistentDomainNames ();
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public NSUserDefaults (string username);
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public virtual string [] PersistentDomainNames ();
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
<h3>Type Changed: MonoTouch.GLKit.GLKTextureLoader</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString SRGB {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.GLKit.GLKTextureLoaderError</h3>
<p>Removed:</p><pre>
 	InvalidEAGLContext
</pre>
<p>Added:</p><pre>
 	InvalidEAGLContext,
 	IncompatibleFormatSRGB
</pre>
<h3>Type Changed: MonoTouch.GLKit.GLKTextureOperations</h3>
<p>Added:</p><pre>
 	public Nullable&lt;bool&gt; SRGB {
 		get;
 		set;
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
<h2>Namespace: MonoTouch.GameController</h2>
<h3>New Type: MonoTouch.GameController.GCController</h3>
<pre>
public class GCController : MonoTouch.Foundation.NSObject {
	
	public GCController ();
	public GCController (MonoTouch.Foundation.NSCoder coder);
	public GCController (MonoTouch.Foundation.NSObjectFlag t);
	public GCController (IntPtr handle);
	
	public static void StartWirelessControllerDiscovery (Action completionHandler);
	public static void StopWirelessControllerDiscovery ();
	protected override void Dispose (bool disposing);
	
	public static GCController[] Controllers {
		get;
	}
	public static MonoTouch.Foundation.NSString DidConnectNotification {
		get;
	}
	public static MonoTouch.Foundation.NSString DidDisconnectNotification {
		get;
	}
	public virtual bool AttachedToDevice {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GCControllerPausedHandler ControllerPausedHandler {
		get;
		set;
	}
	public virtual GCExtendedGamepad ExtendedGamepad {
		get;
	}
	public virtual GCGamepad Gamepad {
		get;
	}
	public virtual int PlayerIndex {
		get;
		set;
	}
	public virtual string VendorName {
		get;
	}
	
	public static class Notifications {
		
		public static MonoTouch.Foundation.NSObject ObserveDidConnect (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
		public static MonoTouch.Foundation.NSObject ObserveDidDisconnect (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
	}
}
</monotouch.foundation.nsnotificationeventargs></monotouch.foundation.nsnotificationeventargs></pre>
<h3>New Type: MonoTouch.GameController.GCControllerAxisInput</h3>
<pre>
public class GCControllerAxisInput : GCControllerElement {
	
	public GCControllerAxisInput ();
	public GCControllerAxisInput (MonoTouch.Foundation.NSCoder coder);
	public GCControllerAxisInput (MonoTouch.Foundation.NSObjectFlag t);
	public GCControllerAxisInput (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Value {
		get;
	}
	public virtual GCControllerAxisValueChangedHandler ValueChangedHandler {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerAxisValueChangedHandler</h3>
<pre>
[Serializable]
public delegate void GCControllerAxisValueChangedHandler (GCControllerAxisInput axis, float value);
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerButtonInput</h3>
<pre>
public class GCControllerButtonInput : GCControllerElement {
	
	public GCControllerButtonInput ();
	public GCControllerButtonInput (MonoTouch.Foundation.NSCoder coder);
	public GCControllerButtonInput (MonoTouch.Foundation.NSObjectFlag t);
	public GCControllerButtonInput (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool IsPressed {
		get;
	}
	public virtual float Value {
		get;
	}
	public virtual GCControllerButtonValueChangedHandler ValueChangedHandler {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerButtonValueChangedHandler</h3>
<pre>
[Serializable]
public delegate void GCControllerButtonValueChangedHandler (GCControllerButtonInput button, float value, bool isPressed);
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerDirectionPad</h3>
<pre>
public class GCControllerDirectionPad : GCControllerElement {
	
	public GCControllerDirectionPad ();
	public GCControllerDirectionPad (MonoTouch.Foundation.NSCoder coder);
	public GCControllerDirectionPad (MonoTouch.Foundation.NSObjectFlag t);
	public GCControllerDirectionPad (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GCControllerButtonInput Down {
		get;
	}
	public virtual GCControllerButtonInput Left {
		get;
	}
	public virtual GCControllerButtonInput Right {
		get;
	}
	public virtual GCControllerButtonInput Up {
		get;
	}
	public virtual GCControllerDirectionPadValueChangedHandler ValueChangedHandler {
		get;
		set;
	}
	public virtual GCControllerAxisInput XAxis {
		get;
	}
	public virtual GCControllerAxisInput YAxis {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerDirectionPadValueChangedHandler</h3>
<pre>
[Serializable]
public delegate void GCControllerDirectionPadValueChangedHandler (GCControllerDirectionPad dpad, float xValue, float yValue);
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerElement</h3>
<pre>
public class GCControllerElement : MonoTouch.Foundation.NSObject {
	
	public GCControllerElement ();
	public GCControllerElement (MonoTouch.Foundation.NSCoder coder);
	public GCControllerElement (MonoTouch.Foundation.NSObjectFlag t);
	public GCControllerElement (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GCControllerElement Collection {
		get;
	}
	public virtual bool IsAnalog {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCControllerPausedHandler</h3>
<pre>
[Serializable]
public delegate void GCControllerPausedHandler (GCController controller);
</pre>
<h3>New Type: MonoTouch.GameController.GCExtendedGamepad</h3>
<pre>
public class GCExtendedGamepad : MonoTouch.Foundation.NSObject {
	
	public GCExtendedGamepad ();
	public GCExtendedGamepad (MonoTouch.Foundation.NSCoder coder);
	public GCExtendedGamepad (MonoTouch.Foundation.NSObjectFlag t);
	public GCExtendedGamepad (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual GCExtendedGamepadSnapshot SaveSnapshot ();
	
	public virtual GCControllerButtonInput ButtonA {
		get;
	}
	public virtual GCControllerButtonInput ButtonB {
		get;
	}
	public virtual GCControllerButtonInput ButtonX {
		get;
	}
	public virtual GCControllerButtonInput ButtonY {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GCController Controller {
		get;
	}
	public virtual GCControllerDirectionPad DPad {
		get;
	}
	public virtual GCControllerButtonInput LeftShoulder {
		get;
	}
	public virtual GCControllerDirectionPad LeftThumbstick {
		get;
	}
	public virtual GCControllerButtonInput LeftTrigger {
		get;
	}
	public virtual GCControllerButtonInput RightShoulder {
		get;
	}
	public virtual GCControllerDirectionPad RightThumbstick {
		get;
	}
	public virtual GCControllerButtonInput RightTrigger {
		get;
	}
	public virtual GCExtendedGamepadValueChangedHandler ValueChangedHandler {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCExtendedGamepadSnapshot</h3>
<pre>
public class GCExtendedGamepadSnapshot : GCExtendedGamepad {
	
	public GCExtendedGamepadSnapshot ();
	public GCExtendedGamepadSnapshot (MonoTouch.Foundation.NSCoder coder);
	public GCExtendedGamepadSnapshot (MonoTouch.Foundation.NSObjectFlag t);
	public GCExtendedGamepadSnapshot (IntPtr handle);
	public GCExtendedGamepadSnapshot (MonoTouch.Foundation.NSData data);
	public GCExtendedGamepadSnapshot (GCController controller, MonoTouch.Foundation.NSData data);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSData SnapshotData {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCExtendedGamepadValueChangedHandler</h3>
<pre>
[Serializable]
public delegate void GCExtendedGamepadValueChangedHandler (GCExtendedGamepad gamepad, GCControllerElement element);
</pre>
<h3>New Type: MonoTouch.GameController.GCGamepad</h3>
<pre>
public class GCGamepad : MonoTouch.Foundation.NSObject {
	
	public GCGamepad ();
	public GCGamepad (MonoTouch.Foundation.NSCoder coder);
	public GCGamepad (MonoTouch.Foundation.NSObjectFlag t);
	public GCGamepad (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual GCControllerButtonInput ButtonA {
		get;
	}
	public virtual GCControllerButtonInput ButtonB {
		get;
	}
	public virtual GCControllerButtonInput ButtonX {
		get;
	}
	public virtual GCControllerButtonInput ButtonY {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GCController Controller {
		get;
	}
	public virtual GCControllerDirectionPad Dpad {
		get;
	}
	public virtual GCControllerButtonInput LeftShoulder {
		get;
	}
	public virtual GCControllerButtonInput RightShoulder {
		get;
	}
	public virtual GCGamepadSnapshot SaveSnapshot {
		get;
	}
	public virtual GCGamepadValueChangedHandler ValueChangedHandler {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCGamepadSnapshot</h3>
<pre>
public class GCGamepadSnapshot : GCGamepad {
	
	public GCGamepadSnapshot ();
	public GCGamepadSnapshot (MonoTouch.Foundation.NSCoder coder);
	public GCGamepadSnapshot (MonoTouch.Foundation.NSObjectFlag t);
	public GCGamepadSnapshot (IntPtr handle);
	public GCGamepadSnapshot (MonoTouch.Foundation.NSData data);
	public GCGamepadSnapshot (GCController controller, MonoTouch.Foundation.NSData data);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSData SnapshotData {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.GameController.GCGamepadValueChangedHandler</h3>
<pre>
[Serializable]
public delegate void GCGamepadValueChangedHandler (GCGamepad gamepad, GCControllerElement element);
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
<h3>Type Changed: MonoTouch.GameKit.GKGameCenterViewController</h3>
<p>Removed:</p><pre>
 	public virtual string LeaderboardCategory {
 	public virtual GKLeaderboardTimeScope LeaderboardTimeScope {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use LeaderboardIdentifier instead")]
	public virtual string LeaderboardCategory {
 	public virtual string LeaderboardIdentifier {
 		get;
 		set;
 	}
 	[Obsolete("This class no longer support Leaderboard Time Scopes, will always default to AllTime")]
	public virtual GKLeaderboardTimeScope LeaderboardTimeScope {
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
<h2>Namespace: MonoTouch.ImageIO</h2>
<h3>Type Changed: MonoTouch.ImageIO.CGImageDestination</h3>
<p>Added:</p><pre>
 	public void AddImageAndMetadata (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, CGImageDestinationOptions options);
 	public void AddImageAndMetadata (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, MonoTouch.Foundation.NSDictionary options);
 	public bool CopyImageSource (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, CGImageDestinationOptions options, out MonoTouch.Foundation.NSError error);
 	public bool CopyImageSource (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageDestinationOptions</h3>
<p>Added:</p><pre>
 	public Nullable&lt;DateTime&gt; DateTime {
 		get;
 		set;
 	}
 	public bool MergeMetadata {
 		get;
 		set;
 	}
 	public CGImageMetadata Metadata {
 		get;
 		set;
 	}
 	public Nullable&lt;int&gt; Orientation {
 		get;
 		set;
 	}
 	public bool ShouldExcludeXMP {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadata</h3>
<pre>
public class CGImageMetadata : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public CGImageMetadata (IntPtr handle);
	public CGImageMetadata (MonoTouch.Foundation.NSData data);
	
	public static int GetTypeID ();
	public CGImageMetadataTag CopyTagMatchingImageProperty (MonoTouch.Foundation.NSString dictionaryName, MonoTouch.Foundation.NSString propertyName);
	public MonoTouch.Foundation.NSData CreateXMPData ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void EnumerateTags (MonoTouch.Foundation.NSString rootPath, CGImageMetadataEnumerateOptions options, CGImageMetadataTagBlock block);
	protected override void Finalize ();
	public MonoTouch.Foundation.NSString GetStringValue (CGImageMetadata parent, MonoTouch.Foundation.NSString path);
	public MonoTouch.Foundation.NSString GetTag (CGImageMetadata parent, MonoTouch.Foundation.NSString path);
	public CGImageMetadataTag[] GetTags ();
	
	public IntPtr Handle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataEnumerateOptions</h3>
<pre>
public class CGImageMetadataEnumerateOptions {
	
	public CGImageMetadataEnumerateOptions ();
	
	public bool Recursive {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataErrors</h3>
<pre>
[Serializable]
public enum CGImageMetadataErrors {
	Unknown,
	UnsupportedFormat,
	BadArgument,
	ConflictingArguments,
	PrefixConflict
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataTag</h3>
<pre>
public class CGImageMetadataTag : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public CGImageMetadataTag (IntPtr handle);
	public CGImageMetadataTag (MonoTouch.Foundation.NSString xmlns, MonoTouch.Foundation.NSString prefix, MonoTouch.Foundation.NSString name, CGImageMetadataType type, IntPtr typeId);
	
	public static int GetTypeID ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public CGImageMetadataTag[] GetQualifiers ();
	
	public IntPtr Handle {
		get;
	}
	public MonoTouch.Foundation.NSString Name {
		get;
	}
	public MonoTouch.Foundation.NSString Namespace {
		get;
	}
	public MonoTouch.Foundation.NSString Prefix {
		get;
	}
	public CGImageMetadataType Type {
		get;
	}
	public IntPtr Value {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataTagBlock</h3>
<pre>
[Serializable]
public delegate bool CGImageMetadataTagBlock (MonoTouch.Foundation.NSString path, CGImageMetadataTag tag);
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataTagNamespaces</h3>
<pre>
public static class CGImageMetadataTagNamespaces {
	
	public static MonoTouch.Foundation.NSString DublinCore {
		get;
	}
	public static MonoTouch.Foundation.NSString Exif {
		get;
	}
	public static MonoTouch.Foundation.NSString ExifAux {
		get;
	}
	public static MonoTouch.Foundation.NSString ExifEx {
		get;
	}
	public static MonoTouch.Foundation.NSString IPTCCore {
		get;
	}
	public static MonoTouch.Foundation.NSString Photoshop {
		get;
	}
	public static MonoTouch.Foundation.NSString TIFF {
		get;
	}
	public static MonoTouch.Foundation.NSString XMPBasic {
		get;
	}
	public static MonoTouch.Foundation.NSString XMPRights {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataTagPrefixes</h3>
<pre>
public static class CGImageMetadataTagPrefixes {
	
	public static MonoTouch.Foundation.NSString DublinCore {
		get;
	}
	public static MonoTouch.Foundation.NSString Exif {
		get;
	}
	public static MonoTouch.Foundation.NSString ExifAux {
		get;
	}
	public static MonoTouch.Foundation.NSString ExifEx {
		get;
	}
	public static MonoTouch.Foundation.NSString IPTCCore {
		get;
	}
	public static MonoTouch.Foundation.NSString Photoshop {
		get;
	}
	public static MonoTouch.Foundation.NSString TIFF {
		get;
	}
	public static MonoTouch.Foundation.NSString XMPBasic {
		get;
	}
	public static MonoTouch.Foundation.NSString XMPRights {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.ImageIO.CGImageMetadataType</h3>
<pre>
[Serializable]
public enum CGImageMetadataType {
	Invalid,
	Default,
	String,
	ArrayUnordered,
	ArrayOrdered,
	AlternateArray,
	AlternateText,
	Structure
}
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageOptions</h3>
<p>Added:</p><pre>
 	public bool ShouldCacheImmediately {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageProperties</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ExifISOSpeed {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExifISOSpeedLatitudeYyy {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExifISOSpeedLatitudeZzz {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExifRecommendedExposureIndex {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExifSensitivityType {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExifStandardOutputSensitivity {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MakerAppleDictionary {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageSource</h3>
<p>Added:</p><pre>
 	public CGImageMetadata CopyMetadata (int index, CGImageOptions options);
 	public CGImageMetadata CopyMetadata (int index, MonoTouch.Foundation.NSDictionary options);
 	public void RemoveCache (int index);
</pre>
<h3>New Type: MonoTouch.ImageIO.CGMutableImageMetadata</h3>
<pre>
public class CGMutableImageMetadata : CGImageMetadata {
	
	public CGMutableImageMetadata ();
	public CGMutableImageMetadata (CGImageMetadata metadata);
	
	public bool RegisterNamespace (MonoTouch.Foundation.NSString xmlns, MonoTouch.Foundation.NSString prefix, out MonoTouch.Foundation.NSError error);
	public bool RemoveTag (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, MonoTouch.Foundation.NSString tag);
	public bool SetTag (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, CGImageMetadataTag tag);
	public bool SetValue (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, MonoTouch.CoreFoundation.CFType value);
	public bool SetValue (MonoTouch.Foundation.NSString dictionaryName, MonoTouch.Foundation.NSString propertyName, MonoTouch.CoreFoundation.CFType value);
}
</pre>
<h2>Namespace: MonoTouch.JavaScriptCore</h2>
<h3>New Type: MonoTouch.JavaScriptCore.JSClassAttributes</h3>
<pre>
[Serializable]
public enum JSClassAttributes : uint {
	None,
	NoAutomaticPrototype
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSContext</h3>
<pre>
public class JSContext : MonoTouch.Foundation.NSObject {
	
	public JSContext (MonoTouch.Foundation.NSCoder coder);
	public JSContext (MonoTouch.Foundation.NSObjectFlag t);
	public JSContext (IntPtr handle);
	public JSContext ();
	public JSContext (JSVirtualMachine virtualMachine);
	
	protected override void Dispose (bool disposing);
	public virtual JSValue EvaluateScript (string script);
	
	public static JSValue[] CurrentArguments {
		get;
	}
	public static JSContext CurrentContext {
		get;
	}
	public static JSValue CurrentThis {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual JSValue Exception {
		get;
		set;
	}
	public virtual JSContextExceptionHandler ExceptionHandler {
		get;
		set;
	}
	public virtual JSValue GlobalObject {
		get;
	}
	public JSValue this [MonoTouch.Foundation.NSObject key] {
		get;
		set;
	}
	public virtual JSVirtualMachine VirtualMachine {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSContextExceptionHandler</h3>
<pre>
[Serializable]
public delegate void JSContextExceptionHandler (JSContext context, JSValue exception);
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSManagedValue</h3>
<pre>
public class JSManagedValue : MonoTouch.Foundation.NSObject {
	
	public JSManagedValue ();
	public JSManagedValue (MonoTouch.Foundation.NSCoder coder);
	public JSManagedValue (MonoTouch.Foundation.NSObjectFlag t);
	public JSManagedValue (IntPtr handle);
	public JSManagedValue (JSValue value);
	
	public static JSManagedValue Get (JSValue value);
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual JSValue Value {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSPropertyAttributes</h3>
<pre>
[Serializable]
public enum JSPropertyAttributes : uint {
	None,
	ReadOnly,
	DontEnum,
	DontDelete
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSType</h3>
<pre>
[Serializable]
public enum JSType {
	Undefined,
	Null,
	Boolean,
	Number,
	String,
	Object
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSValue</h3>
<pre>
public class JSValue : MonoTouch.Foundation.NSObject {
	
	public JSValue (MonoTouch.Foundation.NSCoder coder);
	public JSValue (MonoTouch.Foundation.NSObjectFlag t);
	public JSValue (IntPtr handle);
	
	public static JSValue CreateArray (JSContext context);
	public static JSValue CreateObject (JSContext context);
	public static JSValue Get (bool value, JSContext context);
	public static JSValue Get (double value, JSContext context);
	public static JSValue Get (int value, JSContext context);
	public static JSValue Get (MonoTouch.Foundation.NSObject value, JSContext context);
	public static JSValue Get (MonoTouch.Foundation.NSRange range, JSContext context);
	public static JSValue Get (System.Drawing.PointF point, JSContext context);
	public static JSValue Get (System.Drawing.RectangleF rect, JSContext context);
	public static JSValue Get (System.Drawing.SizeF size, JSContext context);
	public static JSValue Get (uint value, JSContext context);
	public static JSValue GetError (string message, JSContext context);
	public static JSValue GetNull (JSContext context);
	public static JSValue GetRegularExpression (string pattern, string flags, JSContext context);
	public static JSValue GetUndefined (JSContext context);
	public virtual JSValue Call (MonoTouch.Foundation.NSObject[] arguments);
	public virtual JSValue Construct (MonoTouch.Foundation.NSObject[] arguments);
	public virtual void DefineProperty (string property, MonoTouch.Foundation.NSObject descriptor);
	public virtual bool DeleteProperty (string property);
	protected override void Dispose (bool disposing);
	public JSValue Get (string value, JSContext context);
	public virtual JSValue GetProperty (string property);
	public virtual JSValue GetValueAt (uint index);
	public virtual bool HasProperty (string property);
	public virtual JSValue Invoke (string method, MonoTouch.Foundation.NSObject[] arguments);
	public virtual bool IsEqualToObject (MonoTouch.Foundation.NSObject value);
	public virtual bool IsEqualWithTypeCoercionToObject (MonoTouch.Foundation.NSObject value);
	public virtual bool IsInstanceOf (MonoTouch.Foundation.NSObject value);
	public virtual void SetProperty (MonoTouch.Foundation.NSObject value, string property);
	public virtual void SetValueAt (MonoTouch.Foundation.NSObject value, uint index);
	public virtual JSValue[] ToArray ();
	public virtual bool ToBool ();
	public virtual MonoTouch.Foundation.NSDate ToDate ();
	public virtual MonoTouch.Foundation.NSDictionary ToDictionary ();
	public virtual double ToDouble ();
	public virtual int ToInt32 ();
	public virtual MonoTouch.Foundation.NSNumber ToNumber ();
	public virtual MonoTouch.Foundation.NSObject ToObject ();
	public virtual MonoTouch.Foundation.NSObject ToObject (MonoTouch.ObjCRuntime.Class ofExpectedClass);
	public virtual System.Drawing.PointF ToPoint ();
	public virtual MonoTouch.Foundation.NSRange ToRange ();
	public virtual System.Drawing.RectangleF ToRect ();
	public virtual System.Drawing.SizeF ToSize ();
	public override string ToString ();
	public virtual uint ToUInt32 ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual JSContext Context {
		get;
	}
	public virtual bool IsBoolean {
		get;
	}
	public virtual bool IsNull {
		get;
	}
	public virtual bool IsNumber {
		get;
	}
	public virtual bool IsObject {
		get;
	}
	public virtual bool IsString {
		get;
	}
	public virtual bool IsUndefined {
		get;
	}
	public JSValue this [MonoTouch.Foundation.NSObject key] {
		get;
		set;
	}
	public JSValue this [uint index] {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.JavaScriptCore.JSVirtualMachine</h3>
<pre>
public class JSVirtualMachine : MonoTouch.Foundation.NSObject {
	
	public JSVirtualMachine (MonoTouch.Foundation.NSCoder coder);
	public JSVirtualMachine (MonoTouch.Foundation.NSObjectFlag t);
	public JSVirtualMachine (IntPtr handle);
	public JSVirtualMachine ();
	
	public virtual void AddManagedReference (MonoTouch.Foundation.NSObject obj, MonoTouch.Foundation.NSObject owner);
	public virtual void RemoveManagedReference (MonoTouch.Foundation.NSObject obj, MonoTouch.Foundation.NSObject owner);
	
	public override IntPtr ClassHandle {
		get;
	}
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
<h3>New Type: MonoTouch.MapKit.MKCircleRenderer</h3>
<pre>
public class MKCircleRenderer : MKOverlayPathRenderer {
	
	public MKCircleRenderer ();
	public MKCircleRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKCircleRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKCircleRenderer (IntPtr handle);
	public MKCircleRenderer (MKCircle circle);
	
	protected override void Dispose (bool disposing);
	
	public virtual MKCircle Circle {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDidAddOverlayRenderersEventArgs</h3>
<pre>
public class MKDidAddOverlayRenderersEventArgs : EventArgs {
	
	public MKDidAddOverlayRenderersEventArgs (MKOverlayRenderer[] renderers);
	
	public MKOverlayRenderer[] Renderers {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDidFinishRenderingMapEventArgs</h3>
<pre>
public class MKDidFinishRenderingMapEventArgs : EventArgs {
	
	public MKDidFinishRenderingMapEventArgs (bool fullyRendered);
	
	public bool FullyRendered {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDirections</h3>
<pre>
public class MKDirections : MonoTouch.Foundation.NSObject {
	
	public MKDirections ();
	public MKDirections (MonoTouch.Foundation.NSCoder coder);
	public MKDirections (MonoTouch.Foundation.NSObjectFlag t);
	public MKDirections (IntPtr handle);
	public MKDirections (MKDirectionsRequest request);
	
	public virtual void CalculateDirections (MKDirectionsHandler completionHandler);
	public virtual void CalculateETA (MKETAHandler completionHandler);
	public virtual void Cancel ();
	
	public virtual bool Calculating {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDirectionsHandler</h3>
<pre>
[Serializable]
public delegate void MKDirectionsHandler (MKDirectionsResponse response, MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKDirectionsRequest</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDate ArrivalDate {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDate DepartureDate {
 		get;
 		set;
 	}
 		set;
 	}
 	public virtual bool RequestsAlternateRoutes {
 		get;
 		set;
 		set;
 	}
 	public virtual MKDirectionsTransportType TransportType {
 		get;
 		set;
</pre>
<h3>New Type: MonoTouch.MapKit.MKDirectionsResponse</h3>
<pre>
public class MKDirectionsResponse : MonoTouch.Foundation.NSObject {
	
	public MKDirectionsResponse ();
	public MKDirectionsResponse (MonoTouch.Foundation.NSCoder coder);
	public MKDirectionsResponse (MonoTouch.Foundation.NSObjectFlag t);
	public MKDirectionsResponse (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKMapItem Destination {
		get;
	}
	public virtual MKRoute[] Routes {
		get;
	}
	public virtual MKMapItem Source {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDirectionsTransportType</h3>
<pre>
[Serializable]
public enum MKDirectionsTransportType {
	Automobile,
	Walking,
	Any
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDistanceFormatter</h3>
<pre>
public class MKDistanceFormatter : MonoTouch.Foundation.NSFormatter {
	
	public MKDistanceFormatter ();
	public MKDistanceFormatter (MonoTouch.Foundation.NSCoder coder);
	public MKDistanceFormatter (MonoTouch.Foundation.NSObjectFlag t);
	public MKDistanceFormatter (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual double DistanceFromString (string distance);
	public virtual string StringFromDistance (double distance);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSLocale Locale {
		get;
		set;
	}
	public virtual MKDistanceFormatterUnits Units {
		get;
		set;
	}
	public virtual MKDistanceFormatterUnitStyle UnitStyle {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDistanceFormatterUnitStyle</h3>
<pre>
[Serializable]
public enum MKDistanceFormatterUnitStyle {
	Default,
	Abbreviated,
	Full
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDistanceFormatterUnits</h3>
<pre>
[Serializable]
public enum MKDistanceFormatterUnits {
	Default,
	Metric,
	Imperial,
	ImperialWithYards
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKETAHandler</h3>
<pre>
[Serializable]
public delegate void MKETAHandler (MKETAResponse response, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.MapKit.MKETAResponse</h3>
<pre>
public class MKETAResponse : MonoTouch.Foundation.NSObject {
	
	public MKETAResponse ();
	public MKETAResponse (MonoTouch.Foundation.NSCoder coder);
	public MKETAResponse (MonoTouch.Foundation.NSObjectFlag t);
	public MKETAResponse (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKMapItem Destination {
		get;
	}
	public virtual double ExpectedTravelTime {
		get;
	}
	public virtual MKMapItem Source {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKErrorCode</h3>
<pre>
[Serializable]
public enum MKErrorCode {
	Unknown,
	ServerFailure,
	LoadingThrottled,
	PlacemarkNotFound,
	DirectionsNotFound
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKGeodesicPolyline</h3>
<pre>
public class MKGeodesicPolyline : MKPolyline {
	
	public MKGeodesicPolyline ();
	public MKGeodesicPolyline (MonoTouch.Foundation.NSCoder coder);
	public MKGeodesicPolyline (MonoTouch.Foundation.NSObjectFlag t);
	public MKGeodesicPolyline (IntPtr handle);
	
	public static MKGeodesicPolyline FromCoordinates (MonoTouch.CoreLocation.CLLocationCoordinate2D[] coords);
	public static MKGeodesicPolyline FromPoints (MKMapPoint[] points);
	
	public override IntPtr ClassHandle {
		get;
	}
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
<h3>New Type: MonoTouch.MapKit.MKMapCamera</h3>
<pre>
public class MKMapCamera : MonoTouch.Foundation.NSObject {
	
	public MKMapCamera ();
	public MKMapCamera (MonoTouch.Foundation.NSCoder coder);
	public MKMapCamera (MonoTouch.Foundation.NSObjectFlag t);
	public MKMapCamera (IntPtr handle);
	
	public static MKMapCamera CameraLookingAtCenterCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D centerCoordinate, MonoTouch.CoreLocation.CLLocationCoordinate2D eyeCoordinate, double eyeAltitude);
	
	public static MKMapCamera Camera {
		get;
	}
	public virtual double Altitude {
		get;
		set;
	}
	public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D CenterCoordinate {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Heading {
		get;
		set;
	}
	public virtual float Pitch {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKMapSnapshot</h3>
<pre>
public class MKMapSnapshot : MonoTouch.Foundation.NSObject {
	
	public MKMapSnapshot ();
	public MKMapSnapshot (MonoTouch.Foundation.NSCoder coder);
	public MKMapSnapshot (MonoTouch.Foundation.NSObjectFlag t);
	public MKMapSnapshot (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.PointF PointForCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D coordinate);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.UIKit.UIImage Image {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKMapSnapshotCompletionHandler</h3>
<pre>
[Serializable]
public delegate void MKMapSnapshotCompletionHandler (MKMapSnapshot snapshot, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.MapKit.MKMapSnapshotOptions</h3>
<pre>
public class MKMapSnapshotOptions : MonoTouch.Foundation.NSObject {
	
	public MKMapSnapshotOptions ();
	public MKMapSnapshotOptions (MonoTouch.Foundation.NSCoder coder);
	public MKMapSnapshotOptions (MonoTouch.Foundation.NSObjectFlag t);
	public MKMapSnapshotOptions (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual MKMapCamera Camera {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKMapRect MapRect {
		get;
		set;
	}
	public virtual MKMapType MapType {
		get;
		set;
	}
	public virtual MKCoordinateRegion Region {
		get;
		set;
	}
	public virtual float Scale {
		get;
		set;
	}
	public virtual bool ShowsBuildings {
		get;
		set;
	}
	public virtual bool ShowsPointsOfInterest {
		get;
		set;
	}
	public virtual System.Drawing.SizeF Size {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKMapSnapshotter</h3>
<pre>
public class MKMapSnapshotter : MonoTouch.Foundation.NSObject {
	
	public MKMapSnapshotter ();
	public MKMapSnapshotter (MonoTouch.Foundation.NSCoder coder);
	public MKMapSnapshotter (MonoTouch.Foundation.NSObjectFlag t);
	public MKMapSnapshotter (IntPtr handle);
	public MKMapSnapshotter (MKMapSnapshotOptions options);
	
	public virtual void Cancel ();
	public virtual void Start (MKMapSnapshotCompletionHandler completionHandler);
	public virtual void Start (MonoTouch.Foundation.NSObject queue, MKMapSnapshotCompletionHandler completionHandler);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Loading {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Removed:</p><pre>
 	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
</pre>
<p>Added:</p><pre>
 	public virtual void AddOverlay (MonoTouch.Foundation.NSObject overlay, MKOverlayLevel level);
 	public void AddOverlays (MKOverlay[] overlays, MKOverlayLevel level);
 	public virtual void AddOverlays (MonoTouch.Foundation.NSObject[] overlays, MKOverlayLevel level);
 	public virtual void ExchangeOverlay (MonoTouch.Foundation.NSObject overlay1, MonoTouch.Foundation.NSObject overlay2);
 	public virtual void InsertOverlay (MonoTouch.Foundation.NSObject overlay, uint index, MKOverlayLevel level);
 	public virtual MonoTouch.Foundation.NSObject[] OverlaysInLevel (MKOverlayLevel level);
 	public virtual MKOverlayRenderer RendererForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual void SetCamera (MKMapCamera camera, bool animated);
 	public virtual void ShowAnnotations (MonoTouch.Foundation.NSObject[] annotations, bool animated);
 	[Obsolete("Starting with iOS 7 it is recommnended to use RendererForOverlay")]
	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual MKMapCamera Camera {
 		get;
 		set;
 	}
 	public MKRendererForOverlayDelegate GetRendererForOverlay {
 		get;
 		set;
 	}
 	public virtual bool PitchEnabled {
 		get;
 		set;
 	}
 	public virtual bool RotateEnabled {
 		get;
 		set;
 	}
 	public virtual bool ShowsBuildings {
 		get;
 		set;
 	}
 	public virtual bool ShowsPointsOfInterest {
 		get;
 		set;
 	}
 	public event EventHandler&lt;MKDidAddOverlayRenderersEventArgs&gt; DidAddOverlayRenderers;
 	[Obsolete("Since iOS 7 it is recommended that you use DidAddOverlayRenderers")]
	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
 	public event EventHandler&lt;MKDidFinishRenderingMapEventArgs&gt; DidFinishRenderingMap;
 	public event EventHandler WillStartRenderingMap;
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Removed:</p><pre>
 public class MKMapViewDelegate : MonoTouch.Foundation.NSObject {
 	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 public class MKMapViewDelegate : MonoTouch.Foundation.NSObject, IMKMapViewDelegate {
 	public virtual void DidAddOverlayRenderers (MKMapView mapView, MKOverlayRenderer[] renderers);
 	[Obsolete("Since iOS 7 it is recommended that you use DidAddOverlayRenderers")]
	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	public virtual void DidFinishRenderingMap (MKMapView mapView, bool fullyRendered);
 	public virtual MKOverlayRenderer GetRendererForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
 	[Obsolete("Since iOS 7 it is recommnended that you use GetRendererForOverlay")]
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
 	public virtual void WillStartRenderingMap (MKMapView mapView);
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
 	public virtual bool CanReplaceMapContent {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.MapKit.MKOverlayLevel</h3>
<pre>
[Serializable]
public enum MKOverlayLevel {
	AboveRoads,
	AboveLabels
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKOverlayPathRenderer</h3>
<pre>
public class MKOverlayPathRenderer : MKOverlayRenderer {
	
	public MKOverlayPathRenderer ();
	public MKOverlayPathRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKOverlayPathRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlayPathRenderer (IntPtr handle);
	
	public virtual void ApplyFillPropertiesToContext (MonoTouch.CoreGraphics.CGContext context, float zoomScale);
	public virtual void ApplyStrokePropertiesToContext (MonoTouch.CoreGraphics.CGContext context, float zoomScale);
	public virtual void CreatePath ();
	protected override void Dispose (bool disposing);
	public virtual void FillPath (MonoTouch.CoreGraphics.CGPath path, MonoTouch.CoreGraphics.CGContext context);
	public virtual void InvalidatePath ();
	public virtual void StrokePath (MonoTouch.CoreGraphics.CGPath path, MonoTouch.CoreGraphics.CGContext context);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.UIKit.UIColor FillColor {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGLineCap LineCap {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSNumber[] LineDashPattern {
		get;
		set;
	}
	public virtual float LineDashPhase {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGLineJoin LineJoin {
		get;
		set;
	}
	public virtual float LineWidth {
		get;
		set;
	}
	public virtual float MiterLimit {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGPath Path {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIColor StrokeColor {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKOverlayRenderer</h3>
<pre>
public class MKOverlayRenderer : MonoTouch.Foundation.NSObject {
	
	public MKOverlayRenderer ();
	public MKOverlayRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKOverlayRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlayRenderer (IntPtr handle);
	public MKOverlayRenderer (MonoTouch.Foundation.NSObject overlay);
	
	public virtual bool CanDrawMapRect (MKMapRect mapRect, float zoomScale);
	protected override void Dispose (bool disposing);
	public virtual void DrawMapRect (MKMapRect mapRect, float zoomScale, MonoTouch.CoreGraphics.CGContext context);
	public virtual MKMapPoint MapPointForPoint (System.Drawing.PointF point);
	public virtual MKMapRect MapRectForRect (System.Drawing.RectangleF rect);
	public virtual System.Drawing.PointF PointForMapPoint (MKMapPoint mapPoint);
	public virtual System.Drawing.RectangleF RectForMapRect (MKMapRect mapRect);
	public virtual void SetNeedsDisplay ();
	public virtual void SetNeedsDisplay (MKMapRect mapRect);
	public virtual void SetNeedsDisplay (MKMapRect mapRect, float zoomScale);
	
	public virtual float Alpha {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float ContentScaleFactor {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject Overlay {
		get;
	}
}
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
<h3>New Type: MonoTouch.MapKit.MKPolygonRenderer</h3>
<pre>
public class MKPolygonRenderer : MKOverlayPathRenderer {
	
	public MKPolygonRenderer ();
	public MKPolygonRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKPolygonRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolygonRenderer (IntPtr handle);
	public MKPolygonRenderer (MKPolygon polygon);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolygon Polygon {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKPolylineRenderer</h3>
<pre>
public class MKPolylineRenderer : MKOverlayPathRenderer {
	
	public MKPolylineRenderer ();
	public MKPolylineRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKPolylineRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolylineRenderer (IntPtr handle);
	public MKPolylineRenderer (MKPolyline polyline);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolyline Polyline {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKRendererForOverlayDelegate</h3>
<pre>
[Serializable]
public delegate MKOverlayRenderer MKRendererForOverlayDelegate (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
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
<h3>New Type: MonoTouch.MapKit.MKRoute</h3>
<pre>
public class MKRoute : MonoTouch.Foundation.NSObject {
	
	public MKRoute ();
	public MKRoute (MonoTouch.Foundation.NSCoder coder);
	public MKRoute (MonoTouch.Foundation.NSObjectFlag t);
	public MKRoute (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual string [] AdvisoryNotices {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Distance {
		get;
	}
	public virtual double ExpectedTravelTime {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual MKPolyline Polyline {
		get;
	}
	public virtual MKRouteStep[] Steps {
		get;
	}
	public virtual MKDirectionsTransportType TransportType {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKRouteStep</h3>
<pre>
public class MKRouteStep : MonoTouch.Foundation.NSObject {
	
	public MKRouteStep ();
	public MKRouteStep (MonoTouch.Foundation.NSCoder coder);
	public MKRouteStep (MonoTouch.Foundation.NSObjectFlag t);
	public MKRouteStep (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Distance {
		get;
	}
	public virtual string Instructions {
		get;
	}
	public virtual string Notice {
		get;
	}
	public virtual MKPolyline Polyline {
		get;
	}
	public virtual MKDirectionsTransportType TransportType {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKTileOverlay</h3>
<pre>
public class MKTileOverlay : MKOverlay {
	
	public MKTileOverlay ();
	public MKTileOverlay (MonoTouch.Foundation.NSCoder coder);
	public MKTileOverlay (MonoTouch.Foundation.NSObjectFlag t);
	public MKTileOverlay (IntPtr handle);
	public MKTileOverlay (string URLTemplate);
	
	public override bool Intersects (MKMapRect rect);
	public virtual void LoadTileAtPath (MKTileOverlayPath path, MKTileOverlayLoadTileCompletionHandler result);
	public virtual MonoTouch.Foundation.NSUrl URLForTilePath (MKTileOverlayPath path);
	
	public override MKMapRect BoundingMapRect {
		get;
	}
	public virtual bool CanReplaceMapContent {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool GeometryFlipped {
		get;
		set;
	}
	public virtual int MaximumZ {
		get;
		set;
	}
	public virtual int MinimumZ {
		get;
		set;
	}
	public virtual System.Drawing.SizeF TileSize {
		get;
		set;
	}
	public virtual string URLTemplate {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKTileOverlayLoadTileCompletionHandler</h3>
<pre>
[Serializable]
public delegate void MKTileOverlayLoadTileCompletionHandler (MonoTouch.Foundation.NSData tileData, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.MapKit.MKTileOverlayPath</h3>
<pre>
public struct MKTileOverlayPath {
	
	public int X;
	public int Y;
	public int Z;
	public float ContentScaleFactor;
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKTileOverlayRenderer</h3>
<pre>
public class MKTileOverlayRenderer : MKOverlayRenderer {
	
	public MKTileOverlayRenderer ();
	public MKTileOverlayRenderer (MonoTouch.Foundation.NSCoder coder);
	public MKTileOverlayRenderer (MonoTouch.Foundation.NSObjectFlag t);
	public MKTileOverlayRenderer (IntPtr handle);
	public MKTileOverlayRenderer (MKTileOverlay overlay);
	
	public virtual void ReloadData ();
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.MediaAccessibility</h2>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearance</h3>
<pre>
public static class MACaptionAppearance {
	
	public static bool AddSelectedLanguage (MACaptionAppearanceDomain domain, string language);
	public static MonoTouch.CoreGraphics.CGColor GetBackgroundColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetBackgroundOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MACaptionAppearanceDisplayType GetDisplayType (MACaptionAppearanceDomain domain);
	public static MonoTouch.CoreText.CTFontDescriptor GetFontDescriptor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior, MACaptionAppearanceFontStyle fontStyle);
	public static MonoTouch.CoreGraphics.CGColor GetForegroundColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetForegroundOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MonoTouch.Foundation.NSString[] GetPreferredCaptioningMediaCharacteristics (MACaptionAppearanceDomain domain);
	public static float GetRelativeCharacterSize (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static string [] GetSelectedLanguages (MACaptionAppearanceDomain domain);
	public static MACaptionAppearanceTextEdgeStyle GetTextEdgeStyle (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static MonoTouch.CoreGraphics.CGColor GetWindowColor (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetWindowOpacity (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static float GetWindowRoundedCornerRadius (MACaptionAppearanceDomain domain, ref MACaptionAppearanceBehavior behavior);
	public static void SetDisplayType (MACaptionAppearanceDomain domain, MACaptionAppearanceDisplayType displayType);
	
	public static readonly MonoTouch.Foundation.NSString SettingsChangedNotification;
	public static readonly MonoTouch.Foundation.NSString MediaCharacteristicDescribesMusicAndSoundForAccessibility;
	public static readonly MonoTouch.Foundation.NSString MediaCharacteristicTranscribesSpokenDialogForAccessibility;
}
</pre>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearanceBehavior</h3>
<pre>
[Serializable]
public enum MACaptionAppearanceBehavior {
	UseValue,
	UseContentIfAvailable
}
</pre>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearanceDisplayType</h3>
<pre>
[Serializable]
public enum MACaptionAppearanceDisplayType {
	ForcedOnly,
	Automatic,
	AlwaysOn
}
</pre>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearanceDomain</h3>
<pre>
[Serializable]
public enum MACaptionAppearanceDomain {
	Default,
	User
}
</pre>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearanceFontStyle</h3>
<pre>
[Serializable]
public enum MACaptionAppearanceFontStyle {
	Default,
	MonospacedWithSerif,
	ProportionalWithSerif,
	MonospacedWithoutSerif,
	ProportionalWithoutSerif,
	Casual,
	Cursive,
	SmallCapital
}
</pre>
<h3>New Type: MonoTouch.MediaAccessibility.MACaptionAppearanceTextEdgeStyle</h3>
<pre>
[Serializable]
public enum MACaptionAppearanceTextEdgeStyle {
	Undefined,
	None,
	Raised,
	Depressed,
	Uniform,
	DropShadow
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
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaType</h3>
<p>Added:</p><pre>
 	HomeVideo,
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.UIKit.UIImage ThumbnailImageAt (double time, MPMovieTimeOption timeOption);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of RequestThumbnails")]
	public virtual MonoTouch.UIKit.UIImage ThumbnailImageAt (double time, MPMovieTimeOption timeOption);
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController</h3>
<p>Removed:</p><pre>
 	public virtual bool ShouldAutorotateToInterfaceOrientation (MonoTouch.UIKit.UIInterfaceOrientation orientation);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations ();
 	public virtual bool ShouldAutorotate ();
 	[Obsolete("Removed in iOS7 in favor of ShouldAutorotate and SupportedInterfaceOrientations")]
	public virtual bool ShouldAutorotateToInterfaceOrientation (MonoTouch.UIKit.UIInterfaceOrientation orientation);
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController</h3>
<p>Removed:</p><pre>
 	public virtual float Volume {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of MPVolumeView")]
	public virtual float Volume {
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPVolumeView</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	public static MonoTouch.Foundation.NSString WirelessRouteActiveDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WirelessRoutesAvailableDidChangeNotification {
 		get;
 	}
 	public virtual bool AreWirelessRoutesAvailable {
 		get;
 	}
 	public virtual bool IsWirelessRouteActive {
 		get;
 	}
 	public virtual MonoTouch.UIKit.UIImage VolumeWarningSliderImage {
 		get;
 		set;
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
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (MonoTouch.UIKit.UINavigationController navigationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<h3>New Type: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate_Extensions</h3>
<pre>
public static class MFMailComposeViewControllerDelegate_Extensions {
	
	public static void Finished (IMFMailComposeViewControllerDelegate This, MFMailComposeViewController controller, MFMailComposeResult result, MonoTouch.Foundation.NSError error);
}
</pre>
<h3>Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController</h3>
<p>Added:</p><pre>
 	public static bool IsSupportedAttachment (string uti);
 	public virtual bool AddAttachment (MonoTouch.Foundation.NSData attachmentData, string uti, string filename);
 	public virtual bool AddAttachment (MonoTouch.Foundation.NSUrl attachmentURL, string alternateFilename);
 	public virtual void DisableUserAttachments ();
 	public virtual MonoTouch.Foundation.NSDictionary[] GetAttachments ();
 	public static MonoTouch.Foundation.NSString AttachmentAlternateFilename {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AttachmentURL {
 		get;
 	}
 	public static bool CanSendAttachments {
 		get;
 	}
 	public static bool CanSendSubject {
 		get;
 	}
 	public virtual string Subject {
 		get;
 		set;
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
<h3>New Type: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistant</h3>
<pre>
public class MCAdvertiserAssistant : MonoTouch.Foundation.NSObject {
	
	public MCAdvertiserAssistant ();
	public MCAdvertiserAssistant (MonoTouch.Foundation.NSCoder coder);
	public MCAdvertiserAssistant (MonoTouch.Foundation.NSObjectFlag t);
	public MCAdvertiserAssistant (IntPtr handle);
	public MCAdvertiserAssistant (string serviceType, MonoTouch.Foundation.NSDictionary info, MCSession session);
	
	protected override void Dispose (bool disposing);
	public virtual void Start ();
	public virtual void Stop ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public MCAdvertiserAssistantDelegate Delegate {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary DiscoveryInfo {
		get;
	}
	public virtual string ServiceType {
		get;
	}
	public virtual MCSession Session {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistantDelegate</h3>
<pre>
public class MCAdvertiserAssistantDelegate : MonoTouch.Foundation.NSObject {
	
	public MCAdvertiserAssistantDelegate ();
	public MCAdvertiserAssistantDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCAdvertiserAssistantDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCAdvertiserAssistantDelegate (IntPtr handle);
	
	public virtual void DidDismissInvitation (MCAdvertiserAssistant advertiserAssistant);
	public virtual void WillPresentInvitation (MCAdvertiserAssistant advertiserAssistant);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCBrowserViewController</h3>
<pre>
public class MCBrowserViewController : MonoTouch.UIKit.UIViewController {
	
	public MCBrowserViewController (MonoTouch.Foundation.NSCoder coder);
	public MCBrowserViewController (MonoTouch.Foundation.NSObjectFlag t);
	public MCBrowserViewController (IntPtr handle);
	public MCBrowserViewController (MCNearbyServiceBrowser browser, MCSession session);
	public MCBrowserViewController (string serviceType, MCSession session);
	
	protected override void Dispose (bool disposing);
	
	public virtual MCNearbyServiceBrowser Browser {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public MCBrowserViewControllerDelegate Delegate {
		get;
		set;
	}
	public virtual uint MaximumNumberOfPeers {
		get;
		set;
	}
	public virtual uint MinimumNumberOfPeers {
		get;
		set;
	}
	public virtual MCSession Session {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCBrowserViewControllerDelegate</h3>
<pre>
public class MCBrowserViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public MCBrowserViewControllerDelegate ();
	public MCBrowserViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCBrowserViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCBrowserViewControllerDelegate (IntPtr handle);
	
	public virtual void DidFinish (MCBrowserViewController browserViewController);
	public virtual bool ShouldPresentNearbyPeer (MCBrowserViewController browserViewController, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public virtual void WasCancelled (MCBrowserViewController browserViewController);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCEncryptionPreference</h3>
<pre>
[Serializable]
public enum MCEncryptionPreference {
	Optional,
	Required,
	None
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCError</h3>
<pre>
[Serializable]
public enum MCError {
	Unknown,
	NotConnected,
	InvalidParameter,
	Unsupported,
	TimedOut,
	Cancelled,
	Unavailable
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiser</h3>
<pre>
public class MCNearbyServiceAdvertiser : MonoTouch.Foundation.NSObject {
	
	public MCNearbyServiceAdvertiser (MonoTouch.Foundation.NSCoder coder);
	public MCNearbyServiceAdvertiser (MonoTouch.Foundation.NSObjectFlag t);
	public MCNearbyServiceAdvertiser (IntPtr handle);
	public MCNearbyServiceAdvertiser (MCPeerID myPeerID, MonoTouch.Foundation.NSDictionary info, string serviceType);
	
	protected override void Dispose (bool disposing);
	public virtual void StartAdvertisingPeer ();
	public virtual void StopAdvertisingPeer ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public MCNearbyServiceAdvertiserDelegate Delegate {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary DiscoveryInfo {
		get;
	}
	public virtual MCPeerID MyPeerID {
		get;
	}
	public virtual string ServiceType {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate</h3>
<pre>
public class MCNearbyServiceAdvertiserDelegate : MonoTouch.Foundation.NSObject {
	
	public MCNearbyServiceAdvertiserDelegate ();
	public MCNearbyServiceAdvertiserDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCNearbyServiceAdvertiserDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCNearbyServiceAdvertiserDelegate (IntPtr handle);
	
	public virtual void DidNotStartAdvertisingPeer (MCNearbyServiceAdvertiser advertiser, MonoTouch.Foundation.NSError error);
	public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, MonoTouch.Foundation.NSData context, Action<bool,mcsession> invitationHandler);
}
</bool,mcsession></pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceBrowser</h3>
<pre>
public class MCNearbyServiceBrowser : MonoTouch.Foundation.NSObject {
	
	public MCNearbyServiceBrowser (MonoTouch.Foundation.NSCoder coder);
	public MCNearbyServiceBrowser (MonoTouch.Foundation.NSObjectFlag t);
	public MCNearbyServiceBrowser (IntPtr handle);
	public MCNearbyServiceBrowser (MCPeerID myPeerID, string serviceType);
	
	protected override void Dispose (bool disposing);
	public virtual void InvitePeer (MCPeerID peerID, MCSession session, MonoTouch.Foundation.NSData context, double timeout);
	public virtual void StartBrowsingForPeers ();
	public virtual void StopBrowsingForPeers ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public MCNearbyServiceBrowserDelegate Delegate {
		get;
		set;
	}
	public virtual MCPeerID MyPeerID {
		get;
	}
	public virtual string ServiceType {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceBrowserDelegate</h3>
<pre>
public class MCNearbyServiceBrowserDelegate : MonoTouch.Foundation.NSObject {
	
	public MCNearbyServiceBrowserDelegate ();
	public MCNearbyServiceBrowserDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCNearbyServiceBrowserDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCNearbyServiceBrowserDelegate (IntPtr handle);
	
	public virtual void DidNotStartBrowsingForPeers (MCNearbyServiceBrowser browser, MonoTouch.Foundation.NSError error);
	public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCPeerID</h3>
<pre>
public class MCPeerID : MonoTouch.Foundation.NSObject {
	
	public MCPeerID ();
	public MCPeerID (MonoTouch.Foundation.NSCoder coder);
	public MCPeerID (MonoTouch.Foundation.NSObjectFlag t);
	public MCPeerID (IntPtr handle);
	public MCPeerID (string myDisplayName);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string DisplayName {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSession</h3>
<pre>
public class MCSession : MonoTouch.Foundation.NSObject {
	
	public MCSession (MCPeerID myPeerID, MonoTouch.Security.SecIdentity identity, MCEncryptionPreference encryptionPreference);
	public MCSession (MCPeerID myPeerID, MonoTouch.Security.SecIdentity identity, MonoTouch.Security.SecCertificate[] certificates, MCEncryptionPreference encryptionPreference);
	public MCSession (MonoTouch.Foundation.NSCoder coder);
	public MCSession (MonoTouch.Foundation.NSObjectFlag t);
	public MCSession (IntPtr handle);
	public MCSession (MCPeerID myPeerID);
	
	public virtual void CancelConnectPeer (MCPeerID peerID);
	public virtual void ConnectPeer (MCPeerID peerID, MonoTouch.Foundation.NSData data);
	public virtual void Disconnect ();
	protected override void Dispose (bool disposing);
	public virtual void NearbyConnectionDataForPeer (MCPeerID peerID, MCSessionNearbyConnectionDataForPeerCompletionHandler completionHandler);
	public virtual bool SendData (MonoTouch.Foundation.NSData data, MCPeerID[] peerIDs, MCSessionSendDataMode mode, out MonoTouch.Foundation.NSError error);
	public virtual MonoTouch.Foundation.NSObject SendResource (MonoTouch.Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, System.Action<monotouch.foundation.nserror> completionHandler);
	public virtual MonoTouch.Foundation.NSOutputStream StartStream (string streamName, MCPeerID peerID, out MonoTouch.Foundation.NSError error);
	
	public static int MaximumNumberOfPeers {
		get;
	}
	public static int MinimumNumberOfPeers {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MCPeerID[] ConnectedPeers {
		get;
	}
	public MCSessionDelegate Delegate {
		get;
		set;
	}
	public virtual MCEncryptionPreference EncryptionPreference {
		get;
	}
	public virtual MCPeerID MyPeerID {
		get;
	}
	public virtual MonoTouch.Foundation.NSArray SecurityIdentity {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</monotouch.foundation.nserror></pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSessionDelegate</h3>
<pre>
public abstract class MCSessionDelegate : MonoTouch.Foundation.NSObject {
	
	public MCSessionDelegate ();
	public MCSessionDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCSessionDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCSessionDelegate (IntPtr handle);
	
	public abstract void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);
	public abstract void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
	public virtual bool DidReceiveCertificate (MCSession session, MonoTouch.Security.SecCertificate[] certificate, MCPeerID peerID, Action<bool> certificateHandler);
	public abstract void DidReceiveData (MCSession session, MonoTouch.Foundation.NSData data, MCPeerID peerID);
	public abstract void DidReceiveStream (MCSession session, MonoTouch.Foundation.NSInputStream stream, string streamName, MCPeerID peerID);
	public abstract void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSProgress progress);
}
</bool></pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSessionNearbyConnectionDataForPeerCompletionHandler</h3>
<pre>
[Serializable]
public delegate void MCSessionNearbyConnectionDataForPeerCompletionHandler (MonoTouch.Foundation.NSData connectionData, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSessionSendDataMode</h3>
<pre>
[Serializable]
public enum MCSessionSendDataMode {
	Reliable,
	Unreliable
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSessionState</h3>
<pre>
[Serializable]
public enum MCSessionState {
	NotConnected,
	Connecting,
	Connected
}
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
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.Foundation.NSRange arg3);
 	public static bool bool_objc_msgSend_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static bool bool_objc_msgSend_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.Foundation.NSRange arg3);
 	public static bool bool_objc_msgSendSuper_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static bool bool_objc_msgSendSuper_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static MonoTouch.CoreGraphics.CGVector CGVector_objc_msgSend (IntPtr receiver, IntPtr selector);
 	public static void CGVector_objc_msgSend_stret (out MonoTouch.CoreGraphics.CGVector retval, IntPtr receiver, IntPtr selector);
 	public static MonoTouch.CoreGraphics.CGVector CGVector_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static void CGVector_objc_msgSendSuper_stret (out MonoTouch.CoreGraphics.CGVector retval, IntPtr receiver, IntPtr selector);
 	public static float float_objc_msgSend_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static float float_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static float float_objc_msgSendSuper_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static float float_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static int int_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static int int_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static int int_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static int int_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static IntPtr IntPtr_objc_msgSend_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_CGVector_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, MonoTouch.CoreLocation.CLLocationCoordinate2D arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_float_Double (IntPtr receiver, IntPtr selector, float arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_float_Double_bool (IntPtr receiver, IntPtr selector, float arg1, double arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_float_float_Double (IntPtr receiver, IntPtr selector, float arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_int_Double (IntPtr receiver, IntPtr selector, int arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_int_float_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, double arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_CGAffineTransform (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Double_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, bool arg3, bool arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_CGVector (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, MonoTouch.CoreGraphics.CGVector arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_SizeF_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt16_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, ushort arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UIOffset_IntPtr_UIOffset (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, IntPtr arg3, MonoTouch.UIKit.UIOffset arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UIOffset_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_MKTileOverlayPath (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1);
 	public static IntPtr IntPtr_objc_msgSend_PointF_Double (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_bool_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2, MonoTouch.UIKit.UIEdgeInsets arg3);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CGVector_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, MonoTouch.CoreLocation.CLLocationCoordinate2D arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_Double (IntPtr receiver, IntPtr selector, float arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_Double_bool (IntPtr receiver, IntPtr selector, float arg1, double arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_float_Double (IntPtr receiver, IntPtr selector, float arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_Double (IntPtr receiver, IntPtr selector, int arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_float_IntPtr (IntPtr receiver, IntPtr selector, int arg1, float arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, double arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_CGAffineTransform (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, bool arg3, bool arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_CGVector (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, MonoTouch.CoreGraphics.CGVector arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt16_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, ushort arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIOffset_IntPtr_UIOffset (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, IntPtr arg3, MonoTouch.UIKit.UIOffset arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIOffset_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIOffset arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_MKTileOverlayPath (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_Double (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_bool_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2, MonoTouch.UIKit.UIEdgeInsets arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSend_stret_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void NSRange_objc_msgSend_stret_RectangleF_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSend_stret_UInt32 (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSendSuper_stret_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void NSRange_objc_msgSendSuper_stret_RectangleF_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSendSuper_stret_UInt32 (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.PointF PointF_objc_msgSend_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static void PointF_objc_msgSend_stret_CLLocationCoordinate2D (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static void PointF_objc_msgSend_stret_UInt32 (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.PointF PointF_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.PointF PointF_objc_msgSendSuper_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static void PointF_objc_msgSendSuper_stret_CLLocationCoordinate2D (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static void PointF_objc_msgSendSuper_stret_UInt32 (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.PointF PointF_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static void RectangleF_objc_msgSend_stret_IntPtr_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2);
 	public static void RectangleF_objc_msgSend_stret_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, System.Drawing.PointF arg3, uint arg4);
 	public static void RectangleF_objc_msgSend_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
 	public static void RectangleF_objc_msgSend_stret_NSRange_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static void RectangleF_objc_msgSend_stret_RectangleF_UInt32_int_out_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, int arg3, out System.Drawing.RectangleF arg4);
 	public static void RectangleF_objc_msgSend_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2);
 	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, System.Drawing.PointF arg3, uint arg4);
 	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
 	public static void RectangleF_objc_msgSendSuper_stret_NSRange_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static void RectangleF_objc_msgSendSuper_stret_RectangleF_UInt32_int_out_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, int arg3, out System.Drawing.RectangleF arg4);
 	public static void RectangleF_objc_msgSendSuper_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void SizeF_objc_msgSend_stret_UInt32 (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.SizeF SizeF_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static void SizeF_objc_msgSendSuper_stret_UInt32 (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, uint arg1);
 	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static ushort UInt16_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static ushort UInt16_objc_msgSend_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
 	public static ushort UInt16_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static ushort UInt16_objc_msgSendSuper_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
 	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoTouch.Foundation.NSRange arg6);
 	public static uint UInt32_objc_msgSend_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static uint UInt32_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static uint UInt32_objc_msgSend_PointF_IntPtr_out_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, out float arg3);
 	public static uint UInt32_objc_msgSend_UInt32_bool_bool_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5);
 	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoTouch.Foundation.NSRange arg6);
 	public static uint UInt32_objc_msgSendSuper_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static uint UInt32_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static uint UInt32_objc_msgSendSuper_PointF_IntPtr_out_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, out float arg3);
 	public static uint UInt32_objc_msgSendSuper_UInt32_bool_bool_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5);
 	public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void UIOffset_objc_msgSend_stret_IntPtr (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void UIOffset_objc_msgSendSuper_stret_IntPtr (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static void void_objc_msgSend_bool_UInt32 (IntPtr receiver, IntPtr selector, bool arg1, uint arg2);
 	public static void void_objc_msgSend_CGVector (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1);
 	public static void void_objc_msgSend_CGVector_PointF (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSend_Double_Double_float_float_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, float arg3, float arg4, int arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSend_Double_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, IntPtr arg3);
 	public static void void_objc_msgSend_Double_Double_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, uint arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_float_float (IntPtr receiver, IntPtr selector, float arg1, float arg2);
 	public static void void_objc_msgSend_float_UInt32 (IntPtr receiver, IntPtr selector, float arg1, uint arg2);
 	public static void void_objc_msgSend_int_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_int_NSRange_int (IntPtr receiver, IntPtr selector, int arg1, MonoTouch.Foundation.NSRange arg2, int arg3);
 	public static void void_objc_msgSend_IntPtr_float_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, uint arg3);
 	public static void void_objc_msgSend_IntPtr_int_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3, int arg4);
 	public static void void_objc_msgSend_IntPtr_int_NSRange_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3, int arg4, MonoTouch.Foundation.NSRange arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4, long arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, double arg4);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, MonoTouch.Foundation.NSRange arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static void void_objc_msgSend_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static void void_objc_msgSend_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static void void_objc_msgSend_MKTileOverlayPath_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1, IntPtr arg2);
 	public static void void_objc_msgSend_NSRange_int_float_RectangleF_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, float arg3, System.Drawing.RectangleF arg4, MonoTouch.Foundation.NSRange arg5, System.Drawing.PointF arg6);
 	public static void void_objc_msgSend_NSRange_int_out_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, out MonoTouch.Foundation.NSRange arg3);
 	public static void void_objc_msgSend_NSRange_int_RectangleF_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, System.Drawing.RectangleF arg3, MonoTouch.Foundation.NSRange arg4, System.Drawing.PointF arg5);
 	public static void void_objc_msgSend_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSend_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, out MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSend_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSend_out_UInt32_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1, out uint arg2);
 	public static void void_objc_msgSend_PointF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSend_PointF_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_RectangleF_NSRange_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.Foundation.NSRange arg2, System.Drawing.RectangleF arg3);
 	public static void void_objc_msgSend_RectangleF_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSend_SizeF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSend_UIOffset_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_bool_UInt32 (IntPtr receiver, IntPtr selector, bool arg1, uint arg2);
 	public static void void_objc_msgSendSuper_CGVector (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1);
 	public static void void_objc_msgSendSuper_CGVector_PointF (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGVector arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSendSuper_Double_Double_float_float_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, float arg3, float arg4, int arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSendSuper_Double_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_Double_Double_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, uint arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_float_float (IntPtr receiver, IntPtr selector, float arg1, float arg2);
 	public static void void_objc_msgSendSuper_float_UInt32 (IntPtr receiver, IntPtr selector, float arg1, uint arg2);
 	public static void void_objc_msgSendSuper_int_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_int_NSRange_int (IntPtr receiver, IntPtr selector, int arg1, MonoTouch.Foundation.NSRange arg2, int arg3);
 	public static void void_objc_msgSendSuper_IntPtr_float_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, uint arg3);
 	public static void void_objc_msgSendSuper_IntPtr_int_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3, int arg4);
 	public static void void_objc_msgSendSuper_IntPtr_int_NSRange_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3, int arg4, MonoTouch.Foundation.NSRange arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, long arg3, long arg4, long arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, double arg4);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, MonoTouch.Foundation.NSRange arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static void void_objc_msgSendSuper_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static void void_objc_msgSendSuper_MKTileOverlayPath_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_NSRange_int_float_RectangleF_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, float arg3, System.Drawing.RectangleF arg4, MonoTouch.Foundation.NSRange arg5, System.Drawing.PointF arg6);
 	public static void void_objc_msgSendSuper_NSRange_int_out_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, out MonoTouch.Foundation.NSRange arg3);
 	public static void void_objc_msgSendSuper_NSRange_int_RectangleF_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, System.Drawing.RectangleF arg3, MonoTouch.Foundation.NSRange arg4, System.Drawing.PointF arg5);
 	public static void void_objc_msgSendSuper_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, out MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSendSuper_NSRange_PointF (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, System.Drawing.PointF arg2);
 	public static void void_objc_msgSendSuper_out_UInt32_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1, out uint arg2);
 	public static void void_objc_msgSendSuper_PointF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSendSuper_PointF_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_RectangleF_NSRange_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.Foundation.NSRange arg2, System.Drawing.RectangleF arg3);
 	public static void void_objc_msgSendSuper_RectangleF_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_SizeF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSendSuper_UIOffset_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, IntPtr arg2);
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
<h3>Type Changed: MonoTouch.PassKit.PKAddPassesViewController</h3>
<p>Added:</p><pre>
 	public PKAddPassesViewController (PKPass[] pass);
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
<h3>New Type: MonoTouch.PassKit.PKErrorCode</h3>
<pre>
[Serializable]
public enum PKErrorCode {
	None,
	Unknown,
	NotEntitled,
	PermissionDenied
}
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKPass</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary UserInfo {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKPassKitErrorCode</h3>
<p>Removed:</p><pre>
 	CertificateRevoked
</pre>
<p>Added:</p><pre>
 	CertificateRevoked,
 	InvalidSignature
</pre>
<h3>Type Changed: MonoTouch.PassKit.PKPassLibrary</h3>
<p>Added:</p><pre>
 	public virtual void AddPasses (PKPass[] passes, Action&lt;PKPassLibraryAddPassesStatus&gt; completion);
</pre>
<h3>New Type: MonoTouch.PassKit.PKPassLibraryAddPassesStatus</h3>
<pre>
[Serializable]
public enum PKPassLibraryAddPassesStatus {
	DidAddPasses,
	ShouldReviewPasses,
	DidCancelAddPasses
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
<h2>Namespace: MonoTouch.SafariServices</h2>
<h3>New Type: MonoTouch.SafariServices.SSReadingList</h3>
<pre>
public class SSReadingList : MonoTouch.Foundation.NSObject {
	
	public SSReadingList (MonoTouch.Foundation.NSCoder coder);
	public SSReadingList (MonoTouch.Foundation.NSObjectFlag t);
	public SSReadingList (IntPtr handle);
	
	public static bool SupportsUrl (MonoTouch.Foundation.NSUrl url);
	public virtual bool Add (MonoTouch.Foundation.NSUrl url, string title, string previewText, out MonoTouch.Foundation.NSError error);
	
	public static SSReadingList DefaultReadingList {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
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
 	public bool Synchronizable {
 		get;
 		set;
 	}
 	public bool SynchronizableAny {
 		get;
 		set;
 	}
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
<h3>Type Changed: MonoTouch.Security.SecStatusCode</h3>
<p>Removed:</p><pre>
 	AuthFailed,
 	Decode
</pre>
<p>Added:</p><pre>
 	IO,
 	OpWr,
 	UserCanceled,
 	BadReq,
 	InternalComponent,
 	Decode,
 	AuthFailed
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
<h2>Namespace: MonoTouch.Social</h2>
<h3>Type Changed: MonoTouch.Social.SLRequestMethod</h3>
<p>Removed:</p><pre>
 	Delete
</pre>
<p>Added:</p><pre>
 	Delete,
 	Put
</pre>
<h3>Type Changed: MonoTouch.Social.SLServiceKind</h3>
<p>Removed:</p><pre>
 	SinaWeibo
</pre>
<p>Added:</p><pre>
 	SinaWeibo,
 	TencentWeibo,
 	LinkedIn
</pre>
<h3>Type Changed: MonoTouch.Social.SLServiceType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString LinkedIn {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TencentWeibo {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.SpriteKit</h2>
<h3>New Type: MonoTouch.SpriteKit.ISKPhysicsContactDelegate</h3>
<pre>
public interface ISKPhysicsContactDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKAction</h3>
<pre>
public class SKAction : MonoTouch.Foundation.NSObject {
	
	public SKAction ();
	public SKAction (MonoTouch.Foundation.NSCoder coder);
	public SKAction (MonoTouch.Foundation.NSObjectFlag t);
	public SKAction (IntPtr handle);
	
	public static SKAction AnimateWithTextures (MonoTouch.Foundation.NSObject[] textures, double sec);
	public static SKAction AnimateWithTextures (MonoTouch.Foundation.NSObject[] textures, double sec, bool resize, bool restore);
	public static SKAction ColorizeWithColor (MonoTouch.UIKit.UIColor color, float colorBlendFactor, double sec);
	public static SKAction ColorizeWithColorBlendFactor (float colorBlendFactor, double sec);
	public static SKAction CustomActionWithDuration (double seconds, SKActionDurationHandler actionHandler);
	public static SKAction FadeAlphaBy (float factor, double sec);
	public static SKAction FadeAlphaTo (float alpha, double sec);
	public static SKAction FadeInWithDuration (double sec);
	public static SKAction FadeOutWithDuration (double sec);
	public static SKAction FollowPath (MonoTouch.CoreGraphics.CGPath path, bool offset, bool orient, double sec);
	public static SKAction FollowPath (MonoTouch.CoreGraphics.CGPath path, double sec);
	public static SKAction Group (MonoTouch.Foundation.NSObject[] actions);
	public static SKAction MoveBy (MonoTouch.CoreGraphics.CGVector delta, double duration);
	public static SKAction MoveBy (float deltaX, float deltaY, double sec);
	public static SKAction MoveTo (System.Drawing.PointF location, double sec);
	public static SKAction MoveToX (float x, double sec);
	public static SKAction MoveToY (float y, double sec);
	public static SKAction PerformSelector (MonoTouch.ObjCRuntime.Selector selector, MonoTouch.Foundation.NSObject target);
	public static SKAction PlaySoundFileNamed (string soundFile, bool wait);
	public static SKAction RemoveFromParent ();
	public static SKAction RepeatAction (SKAction action, uint count);
	public static SKAction RepeatActionForever (SKAction action);
	public static SKAction ResizeByWidth (float width, float height, double duration);
	public static SKAction ResizeToHeight (float height, double duration);
	public static SKAction ResizeToWidth (float width, double duration);
	public static SKAction ResizeToWidth (float width, float height, double duration);
	public static SKAction RotateByAngle (float radians, double sec);
	public static SKAction RotateToAngle (float radians, double sec);
	public static SKAction RotateToAngle (float radians, double sec, bool shortedUnitArc);
	public static SKAction RunAction (SKAction action, string name);
	public static SKAction RunBlock (Action block);
	public static SKAction RunBlock (Action block, MonoTouch.Foundation.NSObject queue);
	public static SKAction ScaleBy (float scale, double sec);
	public static SKAction ScaleBy (float xScale, float yScale, double sec);
	public static SKAction ScaleTo (float scale, double sec);
	public static SKAction ScaleTo (float xScale, float yScale, double sec);
	public static SKAction ScaleXTo (float scale, double sec);
	public static SKAction ScaleYTo (float scale, double sec);
	public static SKAction Sequence (MonoTouch.Foundation.NSObject[] actions);
	public static SKAction SetTexture (SKTexture texture);
	public static SKAction SpeedBy (float speed, double sec);
	public static SKAction SpeedTo (float speed, double sec);
	public static SKAction WaitForDuration (double sec);
	public static SKAction WaitForDuration (double sec, double durationRange);
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Duration {
		get;
		set;
	}
	public virtual SKAction ReversedAction {
		get;
	}
	public virtual float Speed {
		get;
		set;
	}
	public virtual SKActionTimingMode TimingMode {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKActionDurationHandler</h3>
<pre>
[Serializable]
public delegate void SKActionDurationHandler (SKNode node, float elapsedTime);
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKActionTimingMode</h3>
<pre>
[Serializable]
public enum SKActionTimingMode {
	Linear,
	EaseIn,
	EaseOut,
	EaseInEaseOut
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKBlendMode</h3>
<pre>
[Serializable]
public enum SKBlendMode {
	Alpha,
	Add,
	Subtract,
	Multiply,
	MultiplyX2,
	Screen,
	Replace
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKCropNode</h3>
<pre>
public class SKCropNode : SKNode {
	
	public SKCropNode ();
	public SKCropNode (MonoTouch.Foundation.NSCoder coder);
	public SKCropNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKCropNode (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual SKNode MaskNode {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKEffectNode</h3>
<pre>
public class SKEffectNode : SKNode {
	
	public SKEffectNode ();
	public SKEffectNode (MonoTouch.Foundation.NSCoder coder);
	public SKEffectNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKEffectNode (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual SKBlendMode BlendMode {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreImage.CIFilter Filter {
		get;
		set;
	}
	public virtual bool ShouldCenterFilter {
		get;
		set;
	}
	public virtual bool ShouldEnableEffects {
		get;
		set;
	}
	public virtual bool ShouldRasterize {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKEmitterNode</h3>
<pre>
public class SKEmitterNode : SKNode {
	
	public SKEmitterNode ();
	public SKEmitterNode (MonoTouch.Foundation.NSCoder coder);
	public SKEmitterNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKEmitterNode (IntPtr handle);
	
	public virtual void AdvanceSimulationTime (double sec);
	protected override void Dispose (bool disposing);
	public virtual void ResetSimulation ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float EmissionAngle {
		get;
		set;
	}
	public virtual float EmissionAngleRange {
		get;
		set;
	}
	public virtual uint NumParticlesToEmit {
		get;
		set;
	}
	public virtual SKAction ParticleAction {
		get;
		set;
	}
	public virtual float ParticleAlpha {
		get;
		set;
	}
	public virtual float ParticleAlphaRange {
		get;
		set;
	}
	public virtual SKKeyframeSequence ParticleAlphaSequence {
		get;
		set;
	}
	public virtual float ParticleAlphaSpeed {
		get;
		set;
	}
	public virtual float ParticleBirthRate {
		get;
		set;
	}
	public virtual SKBlendMode ParticleBlendMode {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIColor ParticleColor {
		get;
		set;
	}
	public virtual float ParticleColorAlphaRange {
		get;
		set;
	}
	public virtual float ParticleColorAlphaSpeed {
		get;
		set;
	}
	public virtual float ParticleColorBlendFactor {
		get;
		set;
	}
	public virtual float ParticleColorBlendFactorRange {
		get;
		set;
	}
	public virtual SKKeyframeSequence ParticleColorBlendFactorSequence {
		get;
		set;
	}
	public virtual float ParticleColorBlendFactorSpeed {
		get;
		set;
	}
	public virtual float ParticleColorBlueRange {
		get;
		set;
	}
	public virtual float ParticleColorBlueSpeed {
		get;
		set;
	}
	public virtual float ParticleColorGreenRange {
		get;
		set;
	}
	public virtual float ParticleColorGreenSpeed {
		get;
		set;
	}
	public virtual float ParticleColorRedRange {
		get;
		set;
	}
	public virtual float ParticleColorRedSpeed {
		get;
		set;
	}
	public virtual SKKeyframeSequence ParticleColorSequence {
		get;
		set;
	}
	public virtual float ParticleLifetime {
		get;
		set;
	}
	public virtual float ParticleLifetimeRange {
		get;
		set;
	}
	public virtual System.Drawing.PointF ParticlePosition {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGVector ParticlePositionRange {
		get;
		set;
	}
	public virtual float ParticleRotation {
		get;
		set;
	}
	public virtual float ParticleRotationRange {
		get;
		set;
	}
	public virtual float ParticleRotationSpeed {
		get;
		set;
	}
	public virtual float ParticleScale {
		get;
		set;
	}
	public virtual float ParticleScaleRange {
		get;
		set;
	}
	public virtual SKKeyframeSequence ParticleScaleSequence {
		get;
		set;
	}
	public virtual float ParticleScaleSpeed {
		get;
		set;
	}
	public virtual System.Drawing.SizeF ParticleSize {
		get;
		set;
	}
	public virtual float ParticleSpeed {
		get;
		set;
	}
	public virtual float ParticleSpeedRange {
		get;
		set;
	}
	public virtual SKTexture ParticleTexture {
		get;
		set;
	}
	public virtual float ParticleZPosition {
		get;
		set;
	}
	public virtual float ParticleZPositionRange {
		get;
		set;
	}
	public virtual SKNode TargetNode {
		get;
		set;
	}
	public virtual float XAcceleration {
		get;
		set;
	}
	public virtual float YAcceleration {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKInterpolationMode</h3>
<pre>
[Serializable]
public enum SKInterpolationMode {
	Linear,
	Spline,
	Step
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKKeyframeSequence</h3>
<pre>
public class SKKeyframeSequence : MonoTouch.Foundation.NSObject {
	
	public SKKeyframeSequence ();
	public SKKeyframeSequence (MonoTouch.Foundation.NSCoder coder);
	public SKKeyframeSequence (MonoTouch.Foundation.NSObjectFlag t);
	public SKKeyframeSequence (IntPtr handle);
	public SKKeyframeSequence (MonoTouch.Foundation.NSObject[] values, MonoTouch.Foundation.NSObject[] times);
	public SKKeyframeSequence (uint numItems);
	
	public virtual void AddKeyframeValue (MonoTouch.Foundation.NSObject value, float time);
	public virtual float GetKeyframeTimeForIndex (uint index);
	public virtual MonoTouch.Foundation.NSObject GetKeyframeValueForIndex (uint index);
	public virtual void RemoveKeyframeAtIndex (uint index);
	public virtual void RemoveLastKeyframe ();
	public virtual MonoTouch.Foundation.NSObject SampleAtTime (float time);
	public virtual void SetKeyframeTime (float time, uint index);
	public virtual void SetKeyframeValue (MonoTouch.Foundation.NSObject value, float time, uint index);
	public virtual void SetKeyframeValue (MonoTouch.Foundation.NSObject value, uint index);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint Count {
		get;
	}
	public virtual SKInterpolationMode InterpolationMode {
		get;
		set;
	}
	public virtual SKRepeatMode RepeatMode {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKLabelHorizontalAlignmentMode</h3>
<pre>
[Serializable]
public enum SKLabelHorizontalAlignmentMode {
	Center,
	Left,
	Right
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKLabelNode</h3>
<pre>
public class SKLabelNode : SKNode {
	
	public SKLabelNode ();
	public SKLabelNode (MonoTouch.Foundation.NSCoder coder);
	public SKLabelNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKLabelNode (IntPtr handle);
	public SKLabelNode (string fontName);
	
	public static SKLabelNode FromFont (string fontName);
	protected override void Dispose (bool disposing);
	
	public virtual SKBlendMode BlendMode {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.UIKit.UIColor Color {
		get;
		set;
	}
	public virtual float ColorBlendFactor {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIColor FontColor {
		get;
		set;
	}
	public virtual string FontName {
		get;
		set;
	}
	public virtual float FontSize {
		get;
		set;
	}
	public virtual SKLabelHorizontalAlignmentMode HorizontalAlignmentMode {
		get;
		set;
	}
	public virtual string Text {
		get;
		set;
	}
	public virtual SKLabelVerticalAlignmentMode VerticalAlignmentMode {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKLabelVerticalAlignmentMode</h3>
<pre>
[Serializable]
public enum SKLabelVerticalAlignmentMode {
	Baseline,
	Center,
	Top,
	Bottom
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKNode</h3>
<pre>
public class SKNode : MonoTouch.UIKit.UIResponder {
	
	public SKNode ();
	public SKNode (MonoTouch.Foundation.NSCoder coder);
	public SKNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKNode (IntPtr handle);
	
	public static SKNode Create ();
	public virtual void AddChild (SKNode node);
	public virtual System.Drawing.RectangleF CalculateAccumulatedFrame ();
	public virtual bool ContainsPoint (System.Drawing.PointF point);
	public virtual System.Drawing.PointF ConvertPointFromNode (System.Drawing.PointF point, SKNode sourceNode);
	public virtual System.Drawing.PointF ConvertPointToNode (System.Drawing.PointF point, SKNode sourceNode);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateChildNodes (string name, SKNodeChildEnumeratorHandler enumerationHandler);
	public virtual SKAction GetActionForKey (string key);
	public virtual SKNode GetChildNode (string name);
	public virtual SKNode GetNodeAtPoint (System.Drawing.PointF point);
	public virtual SKNode[] GetNodesAtPoint (System.Drawing.PointF point);
	public virtual bool InParentHierarchy (SKNode node);
	public virtual void InsertChild (SKNode node, int index);
	public virtual bool IntersectsNode (SKNode node);
	public virtual void RemoveActionForKey (string key);
	public virtual void RemoveAllActions ();
	public virtual void RemoveAllChildren ();
	public virtual void RemoveChildren (SKNode[] nodes);
	public virtual void RemoveFromParent ();
	public virtual void RunAction (SKAction action);
	public virtual void RunAction (SKAction action, Action completionHandler);
	public virtual void RunAction (SKAction action, string key);
	
	public virtual float Alpha {
		get;
		set;
	}
	public virtual SKNode[] Children {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual System.Drawing.RectangleF Frame {
		get;
	}
	public virtual bool HasActions {
		get;
	}
	public virtual bool Hidden {
		get;
		set;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual SKNode Parent {
		get;
	}
	public virtual bool Paused {
		get;
		set;
	}
	public virtual SKPhysicsBody PhysicsBody {
		get;
		set;
	}
	public virtual System.Drawing.PointF Position {
		get;
		set;
	}
	public virtual float Scale {
		set;
	}
	public virtual SKScene Scene {
		get;
	}
	public virtual float Speed {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSMutableDictionary UserData {
		get;
		set;
	}
	public virtual bool UserInteractionEnabled {
		get;
		set;
	}
	public virtual float XScale {
		get;
		set;
	}
	public virtual float YScale {
		get;
		set;
	}
	public virtual float ZPosition {
		get;
		set;
	}
	public virtual float ZRotation {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKNodeChildEnumeratorHandler</h3>
<pre>
[Serializable]
public delegate void SKNodeChildEnumeratorHandler (SKNode node, out bool stop);
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKNodeTouches_UITouch</h3>
<pre>
public static class SKNodeTouches_UITouch {
	
	public static System.Drawing.PointF LocationInNode (MonoTouch.UIKit.UITouch This, SKNode node);
	public static System.Drawing.PointF PreviousLocationInNode (MonoTouch.UIKit.UITouch This, SKNode node);
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsBody</h3>
<pre>
public class SKPhysicsBody : MonoTouch.Foundation.NSObject {
	
	public SKPhysicsBody ();
	public SKPhysicsBody (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsBody (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsBody (IntPtr handle);
	
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius);
	public static SKPhysicsBody BodyWithEdgeChainFromPath (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody BodyWithEdgeFromPoint (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);
	public static SKPhysicsBody BodyWithEdgeLoopFromPath (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody BodyWithEdgeLoopFromRect (System.Drawing.RectangleF rect);
	public static SKPhysicsBody BodyWithPolygonFromPath (MonoTouch.CoreGraphics.CGPath path);
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size);
	public virtual void ApplyAngularImpulse (float impulse);
	public virtual void ApplyForce (MonoTouch.CoreGraphics.CGVector force);
	public virtual void ApplyForce (MonoTouch.CoreGraphics.CGVector force, System.Drawing.PointF point);
	public virtual void ApplyImpulse (MonoTouch.CoreGraphics.CGVector impulse);
	public virtual void ApplyImpulse (MonoTouch.CoreGraphics.CGVector impulse, System.Drawing.PointF point);
	public virtual void ApplyTorque (float torque);
	protected override void Dispose (bool disposing);
	
	public virtual bool AffectedByGravity {
		get;
		set;
	}
	public virtual SKPhysicsBody[] AllContactedBodies {
		get;
	}
	public virtual bool AllowsRotation {
		get;
		set;
	}
	public virtual float AngularDamping {
		get;
		set;
	}
	public virtual float AngularVelocity {
		get;
		set;
	}
	public virtual float Area {
		get;
	}
	public virtual uint CategoryBitMask {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint CollisionBitMask {
		get;
		set;
	}
	public virtual uint ContactTestBitMask {
		get;
		set;
	}
	public virtual float Density {
		get;
		set;
	}
	public virtual bool Dynamic {
		get;
		set;
	}
	public virtual float Friction {
		get;
		set;
	}
	public virtual SKPhysicsJoint[] Joints {
		get;
	}
	public virtual float LinearDamping {
		get;
		set;
	}
	public virtual float Mass {
		get;
		set;
	}
	public virtual SKNode Node {
		get;
	}
	public virtual bool Resting {
		get;
		set;
	}
	public virtual float Restitution {
		get;
		set;
	}
	public virtual bool UsesPreciseCollisionDetection {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGVector Velocity {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsContact</h3>
<pre>
public class SKPhysicsContact : MonoTouch.Foundation.NSObject {
	
	public SKPhysicsContact ();
	public SKPhysicsContact (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsContact (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsContact (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual SKPhysicsBody BodyA {
		get;
	}
	public virtual SKPhysicsBody BodyB {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float CollisionImpulse {
		get;
	}
	public virtual System.Drawing.PointF ContactPoint {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsContactDelegate</h3>
<pre>
public class SKPhysicsContactDelegate : MonoTouch.Foundation.NSObject, ISKPhysicsContactDelegate {
	
	public SKPhysicsContactDelegate ();
	public SKPhysicsContactDelegate (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsContactDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsContactDelegate (IntPtr handle);
	
	public virtual void DidBeginContact (SKPhysicsContact contact);
	public virtual void DidEndContact (SKPhysicsContact contact);
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsContactDelegate_Extensions</h3>
<pre>
public static class SKPhysicsContactDelegate_Extensions {
	
	public static void DidBeginContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
	public static void DidEndContact (ISKPhysicsContactDelegate This, SKPhysicsContact contact);
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJoint</h3>
<pre>
public class SKPhysicsJoint : MonoTouch.Foundation.NSObject {
	
	public SKPhysicsJoint ();
	public SKPhysicsJoint (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJoint (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJoint (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual SKPhysicsBody BodyA {
		get;
		set;
	}
	public virtual SKPhysicsBody BodyB {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJointFixed</h3>
<pre>
public class SKPhysicsJointFixed : SKPhysicsJoint {
	
	public SKPhysicsJointFixed ();
	public SKPhysicsJointFixed (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJointFixed (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJointFixed (IntPtr handle);
	
	public static SKPhysicsJointFixed Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJointLimit</h3>
<pre>
public class SKPhysicsJointLimit : SKPhysicsJoint {
	
	public SKPhysicsJointLimit ();
	public SKPhysicsJointLimit (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJointLimit (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJointLimit (IntPtr handle);
	
	public static SKPhysicsJointLimit Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchorA, System.Drawing.PointF anchorB);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float MaxLength {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJointPin</h3>
<pre>
public class SKPhysicsJointPin : SKPhysicsJoint {
	
	public SKPhysicsJointPin ();
	public SKPhysicsJointPin (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJointPin (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJointPin (IntPtr handle);
	
	public static SKPhysicsJointPin Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float FrictionTorque {
		get;
		set;
	}
	public virtual float LowerAngleLimit {
		get;
		set;
	}
	public virtual bool ShouldEnableLimits {
		get;
		set;
	}
	public virtual float UpperAngleLimit {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJointSliding</h3>
<pre>
public class SKPhysicsJointSliding : SKPhysicsJoint {
	
	public SKPhysicsJointSliding ();
	public SKPhysicsJointSliding (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJointSliding (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJointSliding (IntPtr handle);
	
	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor, MonoTouch.CoreGraphics.CGVector axis);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float LowerDistanceLimit {
		get;
		set;
	}
	public virtual bool ShouldEnableLimits {
		get;
		set;
	}
	public virtual float UpperDistanceLimit {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsJointSpring</h3>
<pre>
public class SKPhysicsJointSpring : SKPhysicsJoint {
	
	public SKPhysicsJointSpring ();
	public SKPhysicsJointSpring (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsJointSpring (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsJointSpring (IntPtr handle);
	
	public static SKPhysicsJointSpring Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchorA, System.Drawing.PointF anchorB);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Damping {
		get;
		set;
	}
	public virtual float Frequency {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsWorld</h3>
<pre>
public class SKPhysicsWorld : MonoTouch.Foundation.NSObject {
	
	public SKPhysicsWorld ();
	public SKPhysicsWorld (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsWorld (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsWorld (IntPtr handle);
	
	public virtual void AddJoint (SKPhysicsJoint joint);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateBodies (System.Drawing.PointF point, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (System.Drawing.PointF start, System.Drawing.PointF end, SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler enumeratorHandler);
	public virtual void EnumerateBodies (System.Drawing.RectangleF rect, SKPhysicsWorldBodiesEnumeratorHandler enumeratorHandler);
	public virtual SKPhysicsBody GetBody (System.Drawing.PointF point);
	public virtual SKPhysicsBody GetBody (System.Drawing.PointF rayStart, System.Drawing.PointF rayEnd);
	public virtual SKPhysicsBody GetBody (System.Drawing.RectangleF rect);
	public virtual void RemoveAllJoints ();
	public virtual void RemoveJoint (SKPhysicsJoint joint);
	
	public override IntPtr ClassHandle {
		get;
	}
	public SKPhysicsContactDelegate ContactDelegate {
		get;
		set;
	}
	public virtual System.Drawing.PointF Gravity {
		get;
		set;
	}
	public virtual float Speed {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakContactDelegate {
		get;
		set;
	}
	
	public event EventHandler DidBeginContact;
	public event EventHandler DidEndContact;
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler</h3>
<pre>
[Serializable]
public delegate void SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (SKPhysicsBody body, System.Drawing.PointF point, MonoTouch.CoreGraphics.CGVector normal, out bool stop);
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKPhysicsWorldBodiesEnumeratorHandler</h3>
<pre>
[Serializable]
public delegate void SKPhysicsWorldBodiesEnumeratorHandler (SKPhysicsBody body, out bool stop);
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKRepeatMode</h3>
<pre>
[Serializable]
public enum SKRepeatMode {
	Clamp,
	Loop
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKScene</h3>
<pre>
public class SKScene : SKEffectNode {
	
	public SKScene ();
	public SKScene (MonoTouch.Foundation.NSCoder coder);
	public SKScene (MonoTouch.Foundation.NSObjectFlag t);
	public SKScene (IntPtr handle);
	public SKScene (System.Drawing.SizeF size);
	
	public static SKScene FromSize (System.Drawing.SizeF size);
	public virtual System.Drawing.PointF ConvertPointFromView (System.Drawing.PointF point);
	public virtual System.Drawing.PointF ConvertPointToView (System.Drawing.PointF point);
	public virtual void DidChangeSize (System.Drawing.SizeF oldSize);
	public virtual void DidEvaluateActions ();
	public virtual void DidMoveToView (SKView view);
	public virtual void DidSimulatePhysics ();
	protected override void Dispose (bool disposing);
	public virtual void Update (double currentTime);
	public virtual void WillMoveFromView (SKView view);
	
	public virtual System.Drawing.PointF AnchorPoint {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIColor BackgroundColor {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual SKPhysicsWorld PhysicsWorld {
		get;
	}
	public virtual SKSceneScaleMode ScaleMode {
		get;
		set;
	}
	public virtual System.Drawing.SizeF Size {
		get;
		set;
	}
	public virtual SKView View {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKSceneScaleMode</h3>
<pre>
[Serializable]
public enum SKSceneScaleMode {
	Fill,
	AspectFill,
	AspectFit,
	ResizeFill
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKShapeNode</h3>
<pre>
public class SKShapeNode : SKNode {
	
	public SKShapeNode ();
	public SKShapeNode (MonoTouch.Foundation.NSCoder coder);
	public SKShapeNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKShapeNode (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual bool Antialiased {
		get;
		set;
	}
	public virtual SKBlendMode BlendMode {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.UIKit.UIColor FillColor {
		get;
		set;
	}
	public virtual float GlowWidth {
		get;
		set;
	}
	public virtual float LineWidth {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGPath Path {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIColor StrokeColor {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKSpriteNode</h3>
<pre>
public class SKSpriteNode : SKNode {
	
	public SKSpriteNode ();
	public SKSpriteNode (MonoTouch.Foundation.NSCoder coder);
	public SKSpriteNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKSpriteNode (IntPtr handle);
	public SKSpriteNode (SKTexture texture, MonoTouch.UIKit.UIColor color, System.Drawing.SizeF size);
	public SKSpriteNode (SKTexture texture);
	public SKSpriteNode (string name);
	public SKSpriteNode (MonoTouch.UIKit.UIColor color, System.Drawing.SizeF size);
	
	public static SKSpriteNode FromColor (MonoTouch.UIKit.UIColor color, System.Drawing.SizeF size);
	public static SKSpriteNode FromImageNamed (string name);
	public static SKSpriteNode FromTexture (SKTexture texture);
	public static SKSpriteNode FromTexture (SKTexture texture, System.Drawing.SizeF size);
	protected override void Dispose (bool disposing);
	
	public virtual System.Drawing.PointF AnchorPoint {
		get;
		set;
	}
	public virtual SKBlendMode BlendMode {
		get;
		set;
	}
	public virtual System.Drawing.RectangleF CenterRect {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.UIKit.UIColor Color {
		get;
		set;
	}
	public virtual float ColorBlendFactor {
		get;
		set;
	}
	public virtual System.Drawing.SizeF Size {
		get;
		set;
	}
	public virtual SKTexture Texture {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKTexture</h3>
<pre>
public class SKTexture : MonoTouch.Foundation.NSObject {
	
	public SKTexture ();
	public SKTexture (MonoTouch.Foundation.NSCoder coder);
	public SKTexture (MonoTouch.Foundation.NSObjectFlag t);
	public SKTexture (IntPtr handle);
	
	public static SKTexture FromData (MonoTouch.Foundation.NSData pixelData, System.Drawing.SizeF size);
	public static SKTexture FromData (MonoTouch.Foundation.NSData pixelData, System.Drawing.SizeF size, uint rowLength, uint alignment);
	public static SKTexture FromImage (MonoTouch.CoreGraphics.CGImage image);
	public static SKTexture FromImage (MonoTouch.UIKit.UIImage image);
	public static SKTexture FromImageNamed (string name);
	public static SKTexture FromRectangle (System.Drawing.RectangleF rect, SKTexture texture);
	public static void PreloadTextures (SKTexture[] textures, MonoTouch.Foundation.NSAction completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
	public virtual void Preload (MonoTouch.Foundation.NSAction completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public virtual SKTexture TextureByApplyingCIFilter (MonoTouch.CoreImage.CIFilter filter);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual SKTextureFilteringMode FilteringMode {
		get;
		set;
	}
	public virtual System.Drawing.SizeF Size {
		get;
	}
	public virtual System.Drawing.RectangleF TextureRect {
		get;
	}
	public virtual bool UsesMipmaps {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKTextureAtlas</h3>
<pre>
public class SKTextureAtlas : MonoTouch.Foundation.NSObject {
	
	public SKTextureAtlas ();
	public SKTextureAtlas (MonoTouch.Foundation.NSCoder coder);
	public SKTextureAtlas (MonoTouch.Foundation.NSObjectFlag t);
	public SKTextureAtlas (IntPtr handle);
	
	public static SKTextureAtlas FromName (string name);
	public static void PreloadTextures (SKTexture[] textures, MonoTouch.Foundation.NSAction completion);
	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
	protected override void Dispose (bool disposing);
	public virtual void Preload (MonoTouch.Foundation.NSAction completion);
	public virtual System.Threading.Tasks.Task PreloadAsync ();
	public virtual SKTexture TextureNamed (string name);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] TextureNames {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKTextureFilteringMode</h3>
<pre>
[Serializable]
public enum SKTextureFilteringMode {
	Nearest,
	Linear
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKTransition</h3>
<pre>
public class SKTransition : MonoTouch.Foundation.NSObject {
	
	public SKTransition ();
	public SKTransition (MonoTouch.Foundation.NSCoder coder);
	public SKTransition (MonoTouch.Foundation.NSObjectFlag t);
	public SKTransition (IntPtr handle);
	
	public static SKTransition CrossFadeWithDuration (double sec);
	public static SKTransition DoorsCloseHorizontalWithDuration (double sec);
	public static SKTransition DoorsCloseVerticalWithDuration (double sec);
	public static SKTransition DoorsOpenHorizontalWithDuration (double sec);
	public static SKTransition DoorsOpenVerticalWithDuration (double sec);
	public static SKTransition DoorwayWithDuration (double sec);
	public static SKTransition FadeWithColor (MonoTouch.UIKit.UIColor color, double sec);
	public static SKTransition FadeWithDuration (double sec);
	public static SKTransition FlipHorizontalWithDuration (double sec);
	public static SKTransition FlipVerticalWithDuration (double sec);
	public static SKTransition MoveInWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition PushWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition RevealWithDirection (SKTransitionDirection direction, double sec);
	public static SKTransition TransitionWithCIFilter (MonoTouch.CoreImage.CIFilter filter, double sec);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool PausesIncomingScene {
		get;
		set;
	}
	public virtual bool PausesOutgoingScene {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKTransitionDirection</h3>
<pre>
[Serializable]
public enum SKTransitionDirection {
	Up,
	Down,
	Right,
	Left
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKVideoNode</h3>
<pre>
public class SKVideoNode : SKNode {
	
	public SKVideoNode ();
	public SKVideoNode (MonoTouch.Foundation.NSCoder coder);
	public SKVideoNode (MonoTouch.Foundation.NSObjectFlag t);
	public SKVideoNode (IntPtr handle);
	public SKVideoNode (string videoFile);
	public SKVideoNode (MonoTouch.Foundation.NSUrl url);
	
	public static SKVideoNode FromFile (string videoFile);
	public static SKVideoNode FromUrl (MonoTouch.Foundation.NSUrl videoURL);
	public virtual void Pause ();
	public virtual void Play ();
	
	public virtual System.Drawing.PointF AnchorPoint {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual System.Drawing.SizeF Size {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.SpriteKit.SKView</h3>
<pre>
public class SKView : MonoTouch.UIKit.UIView {
	
	public SKView ();
	public SKView (MonoTouch.Foundation.NSCoder coder);
	public SKView (MonoTouch.Foundation.NSObjectFlag t);
	public SKView (IntPtr handle);
	
	public static SKViewAppearance AppearanceWhenContainedIn (params Type [] containers);
	public static SKViewAppearance GetAppearance<t> ();
	public virtual System.Drawing.PointF ConvertPointFromScene (System.Drawing.PointF point, SKScene scene);
	public virtual System.Drawing.PointF ConvertPointToScene (System.Drawing.PointF point, SKScene scene);
	protected override void Dispose (bool disposing);
	public virtual void PresentScene (SKScene scene);
	public virtual void PresentScene (SKScene scene, SKTransition transition);
	public virtual SKTexture TextureFromNode (SKNode node);
	
	public static SKViewAppearance Appearance {
		get;
	}
	public virtual bool Asynchronous {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int FrameInterval {
		get;
		set;
	}
	public virtual bool IgnoresSiblingOrder {
		get;
		set;
	}
	public virtual bool Paused {
		get;
		set;
	}
	public virtual SKScene Scene {
		get;
	}
	public virtual bool ShowsDrawCount {
		get;
		set;
	}
	public virtual bool ShowsFPS {
		get;
		set;
	}
	public virtual bool ShowsNodeCount {
		get;
		set;
	}
	
	public class SKViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
	}
}
</t></pre>
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
<h3>Type Changed: MonoTouch.StoreKit.SKMutablePayment</h3>
<p>Added:</p><pre>
 	public virtual string ApplicationUsername {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPayment</h3>
<p>Added:</p><pre>
 	public virtual string ApplicationUsername {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentQueue</h3>
<p>Added:</p><pre>
 	public virtual void RestoreCompletedTransactions (string username);
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentTransaction</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSData TransactionReceipt {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual MonoTouch.Foundation.NSData TransactionReceipt {
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
<h3>New Type: MonoTouch.StoreKit.SKReceiptProperty</h3>
<pre>
public static class SKReceiptProperty {
	
	public static MonoTouch.Foundation.NSString IsExpired {
		get;
	}
	public static MonoTouch.Foundation.NSString IsRevoked {
		get;
	}
	public static MonoTouch.Foundation.NSString IsVolumePurchase {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.StoreKit.SKReceiptRefreshRequest</h3>
<pre>
public class SKReceiptRefreshRequest : SKRequest {
	
	public SKReceiptRefreshRequest ();
	public SKReceiptRefreshRequest (MonoTouch.Foundation.NSCoder coder);
	public SKReceiptRefreshRequest (MonoTouch.Foundation.NSObjectFlag t);
	public SKReceiptRefreshRequest (IntPtr handle);
	public SKReceiptRefreshRequest (MonoTouch.Foundation.NSDictionary properties);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary ReceiptProperties {
		get;
	}
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
<h3>New Type: MonoTouch.UIKit.NSAttributedStringAttachmentConveniences</h3>
<pre>
public static class NSAttributedStringAttachmentConveniences {
	
	public static MonoTouch.Foundation.NSAttributedString FromTextAttachment (MonoTouch.Foundation.NSAttributedString This, NSTextAttachment attachment);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSControlCharacterAction</h3>
<pre>
[Serializable]
public enum NSControlCharacterAction {
	ZeroAdvancementAction,
	WhitespaceAction,
	HorizontalTabAction,
	LineBreakAction,
	ParagraphBreakAction,
	ContainerBreakAction
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSExtendedStringDrawing</h3>
<pre>
public static class NSExtendedStringDrawing {
	
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSStringDrawingOptions options, UIStringAttributes attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static System.Drawing.RectangleF GetBoundingRect (MonoTouch.Foundation.NSString This, System.Drawing.SizeF size, MonoTouch.Foundation.NSStringDrawingOptions options, UIStringAttributes attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSStringDrawingOptions options, MonoTouch.Foundation.NSDictionary attributes, MonoTouch.Foundation.NSStringDrawingContext context);
	public static System.Drawing.RectangleF WeakGetBoundingRect (MonoTouch.Foundation.NSString This, System.Drawing.SizeF size, MonoTouch.Foundation.NSStringDrawingOptions options, MonoTouch.Foundation.NSDictionary attributes, MonoTouch.Foundation.NSStringDrawingContext context);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSGlyphProperty</h3>
<pre>
[Serializable]
public enum NSGlyphProperty {
	Null,
	ControlCharacter,
	Elastic,
	NonBaseCharacter
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutManager</h3>
<pre>
public class NSLayoutManager : MonoTouch.Foundation.NSObject {
	
	public NSLayoutManager ();
	public NSLayoutManager (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutManager (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutManager (IntPtr handle);
	
	public virtual void AddTextContainer (NSTextContainer container);
	public virtual System.Drawing.SizeF AttachmentSizeForGlyphAtIndex (uint glyphIndex);
	public virtual System.Drawing.RectangleF BoundingRectForGlyphRange (MonoTouch.Foundation.NSRange glyphRange, NSTextContainer container);
	public virtual uint CharacterIndexForGlyphAtIndex (uint glyphIndex);
	public virtual uint CharacterIndexForPoint (System.Drawing.PointF point, NSTextContainer container, ref float partialFraction);
	protected override void Dispose (bool disposing);
	public virtual void DrawBackgroundForGlyphRange (MonoTouch.Foundation.NSRange glyphsToShow, System.Drawing.PointF origin);
	public virtual void DrawGlyphs (MonoTouch.Foundation.NSRange glyphsToShow, System.Drawing.PointF origin);
	public virtual bool DrawsOutsideLineFragmentForGlyphAtIndex (uint glyphIndex);
	public virtual void DrawStrikethrough (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSUnderlineStyle strikethroughVal, float baselineOffset, System.Drawing.RectangleF lineRect, MonoTouch.Foundation.NSRange lineGlyphRange, System.Drawing.PointF containerOrigin);
	public virtual void DrawUnderline (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSUnderlineStyle underlineVal, float baselineOffset, System.Drawing.RectangleF lineRect, MonoTouch.Foundation.NSRange lineGlyphRange, System.Drawing.PointF containerOrigin);
	public virtual void EnsureGlyphsForCharacterRange (MonoTouch.Foundation.NSRange charRange);
	public virtual void EnsureGlyphsForGlyphRange (MonoTouch.Foundation.NSRange glyphRange);
	public virtual void EnsureLayoutForBoundingRect (System.Drawing.RectangleF bounds, NSTextContainer container);
	public virtual void EnsureLayoutForCharacterRange (MonoTouch.Foundation.NSRange charRange);
	public virtual void EnsureLayoutForGlyphRange (MonoTouch.Foundation.NSRange glyphRange);
	public virtual void EnsureLayoutForTextContainer (NSTextContainer container);
	public virtual void EnumerateEnclosingRects (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSRange selectedRange, NSTextContainer textContainer, NSTextLayoutEnumerateEnclosingRects callback);
	public virtual void EnumerateLineFragments (MonoTouch.Foundation.NSRange glyphRange, NSTextLayoutEnumerateLineFragments callback);
	public virtual float FractionOfDistanceThroughGlyphForPoint (System.Drawing.PointF point, NSTextContainer container);
	public virtual void GetFirstUnlaidCharacterIndex (ref uint charIndex, ref uint glyphIndex);
	public virtual MonoTouch.Foundation.NSRange GetGlyphRange (NSTextContainer container);
	public virtual uint GetGlyphs (MonoTouch.Foundation.NSRange glyphRange, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexBuffer, IntPtr bidiLevelBuffer);
	public virtual uint GetLineFragmentInsertionPoints (uint charIndex, bool alternatePosition, bool inDisplayOrder, IntPtr positions, IntPtr charIndexes);
	public virtual System.Drawing.RectangleF GetUsedRectForTextContainer (NSTextContainer container);
	public virtual ushort GlyphAtIndex (uint glyphIndex);
	public virtual ushort GlyphAtIndex (uint glyphIndex, ref bool isValidIndex);
	public virtual uint GlyphIndexForCharacterAtIndex (uint charIndex);
	public virtual uint GlyphIndexForPoint (System.Drawing.PointF point, NSTextContainer container);
	public virtual uint GlyphIndexForPoint (System.Drawing.PointF point, NSTextContainer container, ref float partialFraction);
	public virtual MonoTouch.Foundation.NSRange GlyphRangeForBoundingRect (System.Drawing.RectangleF bounds, NSTextContainer container);
	public virtual MonoTouch.Foundation.NSRange GlyphRangeForBoundingRectWithoutAdditionalLayout (System.Drawing.RectangleF bounds, NSTextContainer container);
	public virtual void InsertTextContainer (NSTextContainer container, int index);
	public virtual void InvalidateDisplayForCharacterRange (MonoTouch.Foundation.NSRange charRange);
	public virtual void InvalidateDisplayForGlyphRange (MonoTouch.Foundation.NSRange glyphRange);
	public virtual void InvalidateGlyphs (MonoTouch.Foundation.NSRange charRange, int delta, out MonoTouch.Foundation.NSRange actualCharRange);
	public virtual void InvalidateLayout (MonoTouch.Foundation.NSRange charRange, out MonoTouch.Foundation.NSRange actualCharRange);
	public virtual bool IsValidGlyphIndex (uint glyphIndex);
	public virtual System.Drawing.PointF LocationForGlyphAtIndex (uint glyphIndex);
	public virtual bool NotShownAttributeForGlyphAtIndex (uint glyphIndex);
	public virtual void ProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editMask, MonoTouch.Foundation.NSRange newCharRange, int delta, MonoTouch.Foundation.NSRange invalidatedCharRange);
	public virtual NSGlyphProperty PropertyForGlyphAtIndex (uint glyphIndex);
	public virtual MonoTouch.Foundation.NSRange RangeOfNominallySpacedGlyphsContainingIndex (uint glyphIndex);
	public virtual void RemoveTextContainer (int index);
	public virtual void SetAttachmentSize (System.Drawing.SizeF attachmentSize, MonoTouch.Foundation.NSRange glyphRange);
	public virtual void SetDrawsOutsideLineFragment (bool flag, uint glyphIndex);
	public virtual void SetExtraLineFragmentRect (System.Drawing.RectangleF fragmentRect, System.Drawing.RectangleF usedRect, NSTextContainer container);
	public virtual void SetGlyphs (IntPtr glyphs, IntPtr props, IntPtr charIndexes, UIFont aFont, MonoTouch.Foundation.NSRange glyphRange);
	public virtual void SetLineFragmentRect (System.Drawing.RectangleF fragmentRect, MonoTouch.Foundation.NSRange glyphRange, System.Drawing.RectangleF usedRect);
	public virtual void SetLocation (System.Drawing.PointF location, MonoTouch.Foundation.NSRange glyphRange);
	public virtual void SetNotShownAttribute (bool flag, uint glyphIndex);
	public virtual void SetTextContainerForRange (NSTextContainer container, MonoTouch.Foundation.NSRange glyphRange);
	public virtual void Strikethrough (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSUnderlineStyle strikethroughVal, System.Drawing.RectangleF lineRect, MonoTouch.Foundation.NSRange lineGlyphRange, System.Drawing.PointF containerOrigin);
	public virtual void TextContainerChangedGeometry (NSTextContainer container);
	public virtual MonoTouch.Foundation.NSRange TruncatedGlyphRangeInLineFragmentForGlyphAtIndex (uint glyphIndex);
	public virtual void Underline (MonoTouch.Foundation.NSRange glyphRange, MonoTouch.Foundation.NSUnderlineStyle underlineVal, System.Drawing.RectangleF lineRect, MonoTouch.Foundation.NSRange lineGlyphRange, System.Drawing.PointF containerOrigin);
	
	public virtual bool AllowsNonContiguousLayout {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public NSLayoutManagerDelegate Delegate {
		get;
		set;
	}
	public virtual System.Drawing.RectangleF ExtraLineFragmentRect {
		get;
	}
	public virtual NSTextContainer ExtraLineFragmentTextContainer {
		get;
	}
	public virtual System.Drawing.RectangleF ExtraLineFragmentUsedRect {
		get;
	}
	public virtual uint FirstUnlaidCharacterIndex {
		get;
	}
	public virtual uint FirstUnlaidGlyphIndex {
		get;
	}
	public virtual bool HasNonContiguousLayout {
		get;
	}
	public virtual float HyphenationFactor {
		get;
		set;
	}
	public virtual uint NumberOfGlyphs {
		get;
	}
	public virtual bool ShowsControlCharacters {
		get;
		set;
	}
	public virtual bool ShowsInvisibleCharacters {
		get;
		set;
	}
	public virtual NSTextContainer[] TextContainers {
		get;
	}
	public virtual NSTextStorage TextStorage {
		get;
		set;
	}
	public virtual bool UsesFontLeading {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutManagerDelegate</h3>
<pre>
public class NSLayoutManagerDelegate : MonoTouch.Foundation.NSObject {
	
	public NSLayoutManagerDelegate ();
	public NSLayoutManagerDelegate (MonoTouch.Foundation.NSCoder coder);
	public NSLayoutManagerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public NSLayoutManagerDelegate (IntPtr handle);
	
	public virtual System.Drawing.RectangleF BoundingBoxForControlGlyph (NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, System.Drawing.RectangleF proposedRect, System.Drawing.PointF glyphPosition, uint charIndex);
	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, float oldSize);
	public virtual void DidCompleteLayout (NSLayoutManager layoutManager, NSTextContainer textContainer, bool layoutFinishedFlag);
	public virtual void DidInvalidatedLayout (NSLayoutManager sender);
	public virtual float LineSpacingAfterGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual float ParagraphSpacingAfterGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual float ParagraphSpacingBeforeGlyphAtIndex (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual bool ShouldBreakLineByHyphenatingBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual bool ShouldBreakLineByWordBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual uint ShouldGenerateGlyphs (NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, UIFont aFont, MonoTouch.Foundation.NSRange glyphRange);
	public virtual NSControlCharacterAction ShouldUseAction (NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSMutableAttributedStringKitAdditions</h3>
<pre>
public static class NSMutableAttributedStringKitAdditions {
	
	public static void FixAttributesInRange (MonoTouch.Foundation.NSMutableAttributedString This, MonoTouch.Foundation.NSRange range);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSMutableParagraphStyle</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	
 	public override float DefaultTabInterval {
 		get;
 		set;
 	}
 	public override NSTextTab TabStops {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSParagraphStyle</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	public virtual float DefaultTabInterval {
 		get;
 		set;
 	}
 	public virtual NSTextTab TabStops {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.NSStringDrawing</h3>
<pre>
public static class NSStringDrawing {
	
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, UIStringAttributes attributes);
	public static void DrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, UIStringAttributes attributes);
	public static System.Drawing.SizeF GetSizeUsingAttributes (MonoTouch.Foundation.NSString This, UIStringAttributes attributes);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.PointF point, MonoTouch.Foundation.NSDictionary attributes);
	public static void WeakDrawString (MonoTouch.Foundation.NSString This, System.Drawing.RectangleF rect, MonoTouch.Foundation.NSDictionary attributes);
	public static System.Drawing.SizeF WeakGetSizeUsingAttributes (MonoTouch.Foundation.NSString This, MonoTouch.Foundation.NSDictionary attributes);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextAttachment</h3>
<pre>
public class NSTextAttachment : MonoTouch.Foundation.NSObject, INSTextAttachmentContainer {
	
	public NSTextAttachment ();
	public NSTextAttachment (MonoTouch.Foundation.NSCoder coder);
	public NSTextAttachment (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextAttachment (IntPtr handle);
	public NSTextAttachment (MonoTouch.Foundation.NSData contentData, string uti);
	
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public virtual UIImage GetImageForBounds (System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
	
	public virtual System.Drawing.RectangleF Bounds {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSData Contents {
		get;
		set;
	}
	public virtual string FileType {
		get;
		set;
	}
	public virtual UIImage Image {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextAttachmentContainer</h3>
<pre>
public class NSTextAttachmentContainer : MonoTouch.Foundation.NSObject, INSTextAttachmentContainer {
	
	public NSTextAttachmentContainer ();
	public NSTextAttachmentContainer (MonoTouch.Foundation.NSCoder coder);
	public NSTextAttachmentContainer (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextAttachmentContainer (IntPtr handle);
	
	public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public virtual UIImage GetImageForBounds (System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextAttachmentContainer_Extensions</h3>
<pre>
public static class NSTextAttachmentContainer_Extensions {
	
	public static System.Drawing.RectangleF GetAttachmentBounds (INSTextAttachmentContainer This, NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public static UIImage GetImageForBounds (INSTextAttachmentContainer This, System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextContainer</h3>
<pre>
public class NSTextContainer : MonoTouch.Foundation.NSObject {
	
	public NSTextContainer ();
	public NSTextContainer (MonoTouch.Foundation.NSCoder coder);
	public NSTextContainer (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextContainer (IntPtr handle);
	public NSTextContainer (System.Drawing.SizeF size);
	
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.RectangleF GetLineFragmentRect (System.Drawing.RectangleF proposedRect, uint characterIndex, MonoTouch.Foundation.NSWritingDirection baseWritingDirection, out System.Drawing.RectangleF remainingRect);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIBezierPath[] ExclusionPaths {
		get;
		set;
	}
	public virtual bool HeightTracksTextView {
		get;
		set;
	}
	public virtual NSLayoutManager LayoutManager {
		get;
		set;
	}
	public virtual NSTextLayoutOrientation LayoutOrientation {
		get;
		set;
	}
	public virtual UILineBreakMode LineBreakMode {
		get;
		set;
	}
	public virtual float LineFragmentPadding {
		get;
		set;
	}
	public virtual uint MaximumNumberOfLines {
		get;
		set;
	}
	public virtual System.Drawing.SizeF Size {
		get;
		set;
	}
	public virtual bool WidthTracksTextView {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextEffect</h3>
<pre>
[Serializable]
public enum NSTextEffect {
	None,
	LetterPressStyle,
	UnknownUseWeakEffect
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextLayoutEnumerateEnclosingRects</h3>
<pre>
[Serializable]
public delegate void NSTextLayoutEnumerateEnclosingRects (System.Drawing.RectangleF rect, ref bool stop);
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextLayoutEnumerateLineFragments</h3>
<pre>
[Serializable]
public delegate void NSTextLayoutEnumerateLineFragments (System.Drawing.RectangleF rect, System.Drawing.RectangleF usedRectangle, NSTextContainer textContainer, MonoTouch.Foundation.NSRange glyphRange, ref bool stop);
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextLayoutOrientation</h3>
<pre>
[Serializable]
public enum NSTextLayoutOrientation {
	Horizontal,
	Vertical
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorage</h3>
<pre>
public class NSTextStorage : MonoTouch.Foundation.NSMutableAttributedString {
	
	public NSTextStorage ();
	public NSTextStorage (MonoTouch.Foundation.NSCoder coder);
	public NSTextStorage (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextStorage (IntPtr handle);
	
	public virtual void AddLayoutManager (NSLayoutManager aLayoutManager);
	protected override void Dispose (bool disposing);
	public virtual void Edited (NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	public virtual void EnsureAttributesAreFixed (MonoTouch.Foundation.NSRange range);
	public virtual void InvalidateAttributes (MonoTouch.Foundation.NSRange range);
	public virtual void ProcessEditing ();
	public virtual void RemoveLayoutManager (NSLayoutManager aLayoutManager);
	
	public virtual int ChangeInLength {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public NSTextStorageDelegate Delegate {
		get;
		set;
	}
	public virtual NSTextStorageEditActions EditedMask {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSRange EditedRange {
		get;
		set;
	}
	public virtual bool FixesAttributesLazily {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] LayoutManagers {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler<nstextstorageeventargs> DidProcessEditing;
	public event EventHandler<nstextstorageeventargs> WillProcessEditing;
	
	public static class Notifications {
		
		public static MonoTouch.Foundation.NSObject ObserveDidProcessEditing (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
		public static MonoTouch.Foundation.NSObject ObserveWillProcessEditing (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
	}
}
</monotouch.foundation.nsnotificationeventargs></monotouch.foundation.nsnotificationeventargs></nstextstorageeventargs></nstextstorageeventargs></pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorageDelegate</h3>
<pre>
public class NSTextStorageDelegate : MonoTouch.Foundation.NSObject, INSTextStorageDelegate {
	
	public NSTextStorageDelegate ();
	public NSTextStorageDelegate (MonoTouch.Foundation.NSCoder coder);
	public NSTextStorageDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextStorageDelegate (IntPtr handle);
	
	public virtual void DidProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	public virtual void WillProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorageDelegate_Extensions</h3>
<pre>
public static class NSTextStorageDelegate_Extensions {
	
	public static void DidProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	public static void WillProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorageEditActions</h3>
<pre>
[Serializable]
[Flags]
public enum NSTextStorageEditActions {
	Attributes,
	Characters
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextStorageEventArgs</h3>
<pre>
public class NSTextStorageEventArgs : EventArgs {
	
	public NSTextStorageEventArgs (NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	
	public int Delta {
		get;
		set;
	}
	public NSTextStorageEditActions EditedMask {
		get;
		set;
	}
	public MonoTouch.Foundation.NSRange EditedRange {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextTab</h3>
<pre>
public class NSTextTab : MonoTouch.Foundation.NSObject {
	
	public NSTextTab ();
	public NSTextTab (MonoTouch.Foundation.NSCoder coder);
	public NSTextTab (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextTab (IntPtr handle);
	public NSTextTab (UITextAlignment alignment, float location, MonoTouch.Foundation.NSDictionary options);
	
	public static MonoTouch.Foundation.NSCharacterSet GetColumnTerminators (MonoTouch.Foundation.NSLocale locale);
	protected override void Dispose (bool disposing);
	
	public static MonoTouch.Foundation.NSString ColumnTerminatorsAttributeName {
		get;
	}
	public virtual UITextAlignment Alignment {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Location {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary Options {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.TransitionCoordinator_UIViewController</h3>
<pre>
public static class TransitionCoordinator_UIViewController {
	
	public static UIViewControllerTransitionCoordinator GetTransitionCoordinator (UIViewController This);
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
<h3>Type Changed: MonoTouch.UIKit.UIAccessibility</h3>
<p>Added:</p><pre>
 	public static System.Drawing.RectangleF ConvertFrameToScreenCoordinates (System.Drawing.RectangleF rect, UIView view);
 	public static UIBezierPath ConvertPathToScreenCoordinates (UIBezierPath path, UIView view);
 	public static void RequestGuidedAccessSession (bool enable, Action&lt;bool&gt; completionHandler);
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
<h3>Type Changed: MonoTouch.UIKit.UIActivity</h3>
<p>Added:</p><pre>
 	public static UIActivityCategory Category {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityCategory</h3>
<pre>
[Serializable]
public enum UIActivityCategory {
	Action,
	Share
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActivityItemSource</h3>
<p>Removed:</p><pre>
 public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject {
 	public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, string activityType);
</pre>
<p>Added:</p><pre>
 public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject, IUIActivityItemSource {
 	public virtual string GetDataTypeIdentifierForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public virtual string GetSubjectForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public virtual UIImage GetThumbnailImageForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType, System.Drawing.SizeF suggestedSize);
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityItemSource_Extensions</h3>
<pre>
public static class UIActivityItemSource_Extensions {
	
	public static string GetDataTypeIdentifierForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public static string GetSubjectForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
	public static UIImage GetThumbnailImageForActivity (IUIActivityItemSource This, UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType, System.Drawing.SizeF suggestedSize);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIActivityType</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AddToReadingList {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AirDrop {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PostToFlickr {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PostToTencentWeibo {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PostToVimeo {
 		get;
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
<p>Added:</p><pre>
 	public static void RegisterObjectForStateRestoration (IUIStateRestoring uistateRestoringObject, string restorationIdentifier);
 	public virtual int BeginBackgroundTask (string taskName, MonoTouch.Foundation.NSAction expirationHandler);
 	public virtual void IgnoreSnapshotOnNextApplicationLaunch ();
 	public virtual void SetMinimumBackgroundFetchInterval (double minimumBackgroundFetchInterval);
 	public static double BackgroundFetchIntervalMinimum {
 		get;
 	}
 	public static double BackgroundFetchIntervalNever {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BackgroundRefreshStatusDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ContentSizeCategoryChangedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsBluetoothCentralsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsBluetoothPeripheralsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StateRestorationSystemVersionKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StateRestorationTimestampKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UserDidTakeScreenshotNotification {
 		get;
 	}
 	public virtual UIBackgroundRefreshStatus BackgroundRefreshStatus {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString PreferredContentSizeCategory {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveContentSizeCategoryChanged (EventHandler&lt;UIContentSizeCategoryChangedEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveUserDidTakeScreenshot (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Removed:</p><pre>
 public class UIApplicationDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIApplicationDelegate : MonoTouch.Foundation.NSObject, IUIApplicationDelegate {
 	public virtual void DidReceiveRemoteNotification (UIApplication application, MonoTouch.Foundation.NSDictionary userInfo, Action&lt;UIBackgroundFetchResult&gt; completionHandler);
 	public virtual void HandleEventsForBackgroundUrl (UIApplication application, string sessionIdentifier, MonoTouch.Foundation.NSAction completionHandler);
 	public virtual void PerformFetch (UIApplication application, Action&lt;UIBackgroundFetchResult&gt; completionHandler);
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
<h3>New Type: MonoTouch.UIKit.UIAttachmentBehavior</h3>
<pre>
public class UIAttachmentBehavior : UIDynamicBehavior {
	
	public UIAttachmentBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIAttachmentBehavior (IntPtr handle);
	public UIAttachmentBehavior (IUIDynamicItem item, System.Drawing.PointF anchorPoint);
	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offset, System.Drawing.PointF anchorPoint);
	public UIAttachmentBehavior (IUIDynamicItem item, MonoTouch.Foundation.NSObject attachedToItem);
	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offsetFromCenter, MonoTouch.Foundation.NSObject attachedToItem, UIOffset attachOffsetFromCenter);
	
	protected override void Dispose (bool disposing);
	
	public virtual System.Drawing.PointF AnchorPoint {
		get;
		set;
	}
	public virtual UIAttachmentBehaviorType AttachedBehaviorType {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Damping {
		get;
		set;
	}
	public virtual float Frequency {
		get;
		set;
	}
	public virtual IUIDynamicItem[] Items {
		get;
	}
	public virtual float Length {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIAttachmentBehaviorType</h3>
<pre>
[Serializable]
public enum UIAttachmentBehaviorType {
	Items,
	Anchor
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIBackgroundFetchResult</h3>
<pre>
[Serializable]
public enum UIBackgroundFetchResult {
	NewData,
	NoData,
	Failed
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIBackgroundRefreshStatus</h3>
<pre>
[Serializable]
public enum UIBackgroundRefreshStatus {
	Restricted,
	Denied,
	Available
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarMetrics</h3>
<p>Removed:</p><pre>
 	LandscapePhone
</pre>
<p>Added:</p><pre>
 	LandscapePhone,
 	DefaultPrompt,
 	LandscapePhonePrompt
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPosition</h3>
<pre>
[Serializable]
public enum UIBarPosition {
	Any,
	Bottom,
	Top,
	TopAttached
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioningDelegate</h3>
<pre>
public class UIBarPositioningDelegate : MonoTouch.Foundation.NSObject, IUIBarPositioningDelegate {
	
	public UIBarPositioningDelegate ();
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIBarPositioningDelegate (IntPtr handle);
	
	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioningDelegate_Extensions</h3>
<pre>
public static class UIBarPositioningDelegate_Extensions {
	
	public static UIBarPosition GetPositionForBar (IUIBarPositioningDelegate This, MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIButtonType</h3>
<p>Removed:</p><pre>
 	ContactAdd
</pre>
<p>Added:</p><pre>
 	ContactAdd,
 	System
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Added:</p><pre>
 	public virtual void CancelInteractiveTransition ();
 	public virtual void FinishInteractiveTransition ();
 	public virtual void SetCollectionViewLayout (UICollectionViewLayout layout, bool animated, UICompletionHandler completion);
 	public virtual UICollectionViewTransitionLayout StartInteractiveTransition (UICollectionViewLayout newCollectionViewLayout, UICollectionViewLayoutInteractiveTransitionCompletion completion);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewController</h3>
<p>Removed:</p><pre>
 public class UICollectionViewController : UIViewController {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewController : UIViewController, IUICollectionViewDataSource, IUICollectionViewDelegate, IUICollectionViewSource, IUIScrollViewDelegate {
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
 	public virtual UICollectionViewLayout Layout {
 		get;
 	}
 	public virtual bool UseLayoutToLayoutNavigationTransitions {
 		get;
 		set;
 	}
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
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<p>Removed:</p><pre>
 public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate, IUICollectionViewDelegateFlowLayout {
 	public override UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
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
<h3>New Type: MonoTouch.UIKit.UICollectionViewFlowLayoutInvalidationContext</h3>
<pre>
public class UICollectionViewFlowLayoutInvalidationContext : UICollectionViewLayoutInvalidationContext {
	
	public UICollectionViewFlowLayoutInvalidationContext ();
	public UICollectionViewFlowLayoutInvalidationContext (MonoTouch.Foundation.NSCoder coder);
	public UICollectionViewFlowLayoutInvalidationContext (MonoTouch.Foundation.NSObjectFlag t);
	public UICollectionViewFlowLayoutInvalidationContext (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool InvalidateFlowLayoutAttributes {
		get;
		set;
	}
	public virtual bool InvalidateFlowLayoutDelegateMetrics {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayout</h3>
<p>Added:</p><pre>
 	public static MonoTouch.ObjCRuntime.Class InvalidationContextClass ();
 	public virtual void FinalizeLayoutTransition ();
 	public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsToDeleteForDecorationViewOfKind (MonoTouch.Foundation.NSString kind);
 	public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsToDeleteForSupplementaryView (MonoTouch.Foundation.NSString kind);
 	public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsToInsertForDecorationView (MonoTouch.Foundation.NSString kind);
 	public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsToInsertForSupplementaryView (MonoTouch.Foundation.NSString kind);
 	public virtual UICollectionViewLayoutInvalidationContext GetInvalidationContextForBoundsChange (System.Drawing.RectangleF newBounds);
 	public virtual void InvalidateLayout (UICollectionViewLayoutInvalidationContext context);
 	public virtual void PrepareForTransitionFromLayout (UICollectionViewLayout oldLayout);
 	public virtual void PrepareForTransitionToLayout (UICollectionViewLayout newLayout);
 	public virtual System.Drawing.PointF TargetContentOffsetForProposedContentOffset (System.Drawing.PointF proposedContentOffset);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Removed:</p><pre>
 public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject, IUIDynamicItem {
 	public virtual System.Drawing.RectangleF Bounds {
 		get;
 		set;
 	}
 	public virtual MonoTouch.CoreGraphics.CGAffineTransform Transform {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewLayoutInteractiveTransitionCompletion</h3>
<pre>
[Serializable]
public delegate void UICollectionViewLayoutInteractiveTransitionCompletion (bool completed, bool finish);
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewLayoutInvalidationContext</h3>
<pre>
public class UICollectionViewLayoutInvalidationContext : MonoTouch.Foundation.NSObject {
	
	public UICollectionViewLayoutInvalidationContext ();
	public UICollectionViewLayoutInvalidationContext (MonoTouch.Foundation.NSCoder coder);
	public UICollectionViewLayoutInvalidationContext (MonoTouch.Foundation.NSObjectFlag t);
	public UICollectionViewLayoutInvalidationContext (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool InvalidateDataSourceCounts {
		get;
	}
	public virtual bool InvalidateEverything {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewSource</h3>
<p>Removed:</p><pre>
 public class UICollectionViewSource : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UICollectionViewSource : MonoTouch.Foundation.NSObject, IUICollectionViewDataSource, IUICollectionViewDelegate, IUICollectionViewSource, IUIScrollViewDelegate {
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewSource_Extensions</h3>
<pre>
public static class UICollectionViewSource_Extensions {
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewTransitionLayout</h3>
<pre>
public class UICollectionViewTransitionLayout : UICollectionViewLayout {
	
	public UICollectionViewTransitionLayout ();
	public UICollectionViewTransitionLayout (MonoTouch.Foundation.NSCoder coder);
	public UICollectionViewTransitionLayout (MonoTouch.Foundation.NSObjectFlag t);
	public UICollectionViewTransitionLayout (IntPtr handle);
	public UICollectionViewTransitionLayout (UICollectionViewLayout currentLayout, UICollectionViewLayout newLayout);
	
	protected override void Dispose (bool disposing);
	public virtual float GetValueForAnimatedKey (string animatedKey);
	public virtual void UpdateValue (float value, string animatedKey);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UICollectionViewLayout CurrentLayout {
		get;
	}
	public virtual UICollectionViewLayout NextLayout {
		get;
	}
	public virtual float TransitionProgress {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBeganBoundaryContactEventArgs</h3>
<pre>
public class UICollisionBeganBoundaryContactEventArgs : EventArgs {
	
	public UICollisionBeganBoundaryContactEventArgs (IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
	
	public System.Drawing.PointF AtPoint {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject BoundaryIdentifier {
		get;
		set;
	}
	public IUIDynamicItem DynamicItem {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBeganContactEventArgs</h3>
<pre>
public class UICollisionBeganContactEventArgs : EventArgs {
	
	public UICollisionBeganContactEventArgs (IUIDynamicItem firstItem, IUIDynamicItem secondItem, System.Drawing.PointF atPoint);
	
	public System.Drawing.PointF AtPoint {
		get;
		set;
	}
	public IUIDynamicItem FirstItem {
		get;
		set;
	}
	public IUIDynamicItem SecondItem {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBehavior</h3>
<pre>
public class UICollisionBehavior : UIDynamicBehavior {
	
	public UICollisionBehavior ();
	public UICollisionBehavior (MonoTouch.Foundation.NSCoder coder);
	public UICollisionBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UICollisionBehavior (IntPtr handle);
	public UICollisionBehavior (IUIDynamicItem[] items);
	
	public virtual void AddBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);
	public virtual void AddBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier, UIBezierPath bezierPath);
	public virtual void AddItem (IUIDynamicItem dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual UIBezierPath GetBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void RemoveAllBoundaries ();
	public virtual void RemoveBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
	public virtual void SetTranslatesReferenceBoundsIntoBoundaryWithInsets (UIEdgeInsets insets);
	
	public virtual MonoTouch.Foundation.NSObject[] BoundaryIdentifiers {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public UICollisionBehaviorDelegate CollisionDelegate {
		get;
		set;
	}
	public virtual UICollisionBehaviorMode CollisionMode {
		get;
		set;
	}
	public virtual IUIDynamicItem[] Items {
		get;
	}
	public virtual bool TranslatesReferenceBoundsIntoBoundary {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakCollisionDelegate {
		get;
		set;
	}
	
	public event EventHandler<uicollisionbeganboundarycontacteventargs> BeganBoundaryContact;
	public event EventHandler<uicollisionbegancontacteventargs> BeganContact;
	public event EventHandler<uicollisionendedboundarycontacteventargs> EndedBoundaryContact;
	public event EventHandler<uicollisionendedcontacteventargs> EndedContact;
}
</uicollisionendedcontacteventargs></uicollisionendedboundarycontacteventargs></uicollisionbegancontacteventargs></uicollisionbeganboundarycontacteventargs></pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBehaviorDelegate</h3>
<pre>
public class UICollisionBehaviorDelegate : MonoTouch.Foundation.NSObject, IUICollisionBehaviorDelegate {
	
	public UICollisionBehaviorDelegate ();
	public UICollisionBehaviorDelegate (MonoTouch.Foundation.NSCoder coder);
	public UICollisionBehaviorDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UICollisionBehaviorDelegate (IntPtr handle);
	
	public virtual void BeganBoundaryContact (UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
	public virtual void BeganContact (UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem, System.Drawing.PointF atPoint);
	public virtual void EndedBoundaryContact (UICollisionBehavior behavior, IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void EndedContact (UICollisionBehavior behavior, IUIDynamicItem firstItem, IUIDynamicItem secondItem);
}
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
<h3>New Type: MonoTouch.UIKit.UICollisionBehaviorMode</h3>
<pre>
[Serializable]
[Flags]
public enum UICollisionBehaviorMode : uint {
	Items,
	Boundaries,
	Everything
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionEndedBoundaryContactEventArgs</h3>
<pre>
public class UICollisionEndedBoundaryContactEventArgs : EventArgs {
	
	public UICollisionEndedBoundaryContactEventArgs (IUIDynamicItem dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
	
	public MonoTouch.Foundation.NSObject BoundaryIdentifier {
		get;
		set;
	}
	public IUIDynamicItem DynamicItem {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionEndedContactEventArgs</h3>
<pre>
public class UICollisionEndedContactEventArgs : EventArgs {
	
	public UICollisionEndedContactEventArgs (IUIDynamicItem firstItem, IUIDynamicItem secondItem);
	
	public IUIDynamicItem FirstItem {
		get;
		set;
	}
	public IUIDynamicItem SecondItem {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIColor</h3>
<p>Removed:</p><pre>
 	public static UIColor ScrollViewTexturedBackgroundColor {
 	public static UIColor UnderPageBackgroundColor {
 	public static UIColor ViewFlipsideBackgroundColor {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor ScrollViewTexturedBackgroundColor {
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor UnderPageBackgroundColor {
 	[Obsolete("Deprecated in iOS7")]
	public static UIColor ViewFlipsideBackgroundColor {
</pre>
<h3>New Type: MonoTouch.UIKit.UIContentSizeCategory</h3>
<pre>
[Serializable]
public enum UIContentSizeCategory {
	ExtraSmall,
	Small,
	Medium,
	Large,
	ExtraLarge,
	ExtraExtraLarge
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIContentSizeCategoryChangedEventArgs</h3>
<pre>
public class UIContentSizeCategoryChangedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	
	public UIContentSizeCategoryChangedEventArgs (MonoTouch.Foundation.NSNotification notification);
	
	public MonoTouch.Foundation.NSString NewValue {
		get;
	}
}
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
<h3>New Type: MonoTouch.UIKit.UIDynamicAnimator</h3>
<pre>
public class UIDynamicAnimator : MonoTouch.Foundation.NSObject {
	
	public UIDynamicAnimator ();
	public UIDynamicAnimator (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicAnimator (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicAnimator (IntPtr handle);
	public UIDynamicAnimator (UIView referenceView);
	public UIDynamicAnimator (UICollectionViewLayout layout);
	
	public virtual void AddBehavior (UIDynamicBehavior behavior);
	protected override void Dispose (bool disposing);
	public virtual IUIDynamicItem[] GetDynamicItems (System.Drawing.RectangleF rect);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForCell (MonoTouch.Foundation.NSIndexPath cellIndexPath);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForDecorationView (MonoTouch.Foundation.NSString viewKind, MonoTouch.Foundation.NSIndexPath viewIndexPath);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryView (MonoTouch.Foundation.NSString viewKind, MonoTouch.Foundation.NSIndexPath viewIndexPath);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (UIDynamicBehavior behavior);
	public virtual void UpdateItemUsingCurrentState (IUIDynamicItem uiDynamicItem);
	
	public virtual UIDynamicBehavior[] Behaviors {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public UIDynamicAnimatorDelegate Delegate {
		get;
		set;
	}
	public virtual double ElapsedTime {
		get;
	}
	public virtual UIView ReferenceView {
		get;
	}
	public virtual bool Running {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicAnimatorDelegate</h3>
<pre>
public abstract class UIDynamicAnimatorDelegate : MonoTouch.Foundation.NSObject, IUIDynamicAnimatorDelegate {
	
	public UIDynamicAnimatorDelegate ();
	public UIDynamicAnimatorDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicAnimatorDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicAnimatorDelegate (IntPtr handle);
	
	public abstract void DidPause (UIDynamicAnimator animator);
	public abstract void WillResume (UIDynamicAnimator animator);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicAnimatorDelegate_Extensions</h3>
<pre>
public static class UIDynamicAnimatorDelegate_Extensions {
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicBehavior</h3>
<pre>
public class UIDynamicBehavior : MonoTouch.Foundation.NSObject {
	
	public UIDynamicBehavior ();
	public UIDynamicBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicBehavior (IntPtr handle);
	
	public virtual void AddChildBehavior (UIDynamicBehavior behavior);
	protected override void Dispose (bool disposing);
	public virtual void RemoveChildBehavior (UIDynamicBehavior behavior);
	public virtual void WillMoveToAnimator (UIDynamicAnimator targetAnimator);
	
	public virtual MonoTouch.Foundation.NSAction Action {
		get;
		set;
	}
	public virtual UIDynamicBehavior[] ChildBehaviors {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIDynamicAnimator DynamicAnimator {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicItem</h3>
<pre>
[Obsolete]
public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject, IUIDynamicItem {
	
	public UIDynamicItem ();
	public UIDynamicItem (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicItem (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicItem (IntPtr handle);
	
	public abstract System.Drawing.RectangleF Bounds {
		get;
	}
	public abstract System.Drawing.PointF Center {
		get;
		set;
	}
	public abstract MonoTouch.CoreGraphics.CGAffineTransform Transform {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicItemBehavior</h3>
<pre>
public class UIDynamicItemBehavior : UIDynamicBehavior {
	
	public UIDynamicItemBehavior ();
	public UIDynamicItemBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicItemBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicItemBehavior (IntPtr handle);
	public UIDynamicItemBehavior (IUIDynamicItem[] items);
	
	public virtual void AddAngularVelocityForItem (float velocity, IUIDynamicItem dynamicItem);
	public virtual void AddItem (IUIDynamicItem dynamicItem);
	public virtual void AddLinearVelocityForItem (System.Drawing.PointF velocity, IUIDynamicItem dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual float GetAngularVelocityForItem (IUIDynamicItem dynamicItem);
	public virtual System.Drawing.PointF GetLinearVelocityForItem (IUIDynamicItem dynamicItem);
	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
	
	public virtual bool AllowsRotation {
		get;
		set;
	}
	public virtual float AngularResistance {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Density {
		get;
		set;
	}
	public virtual float Elasticity {
		get;
		set;
	}
	public virtual float Friction {
		get;
		set;
	}
	public virtual IUIDynamicItem[] Items {
		get;
	}
	public virtual float Resistance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicItem_Extensions</h3>
<pre>
public static class UIDynamicItem_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFont</h3>
<p>Removed:</p><pre>
 	public UIFont ();
</pre>
<p>Added:</p><pre>
 	[Obsolete("This constructor does not return a valid, default, instance")]
	public UIFont ();
 	public static UIFont FromDescriptor (UIFontDescriptor descriptor, float pointSize);
 	public static UIFont PreferredFontForTextStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	public static UIFont PreferredFontForTextStyle (UIFontTextStyle textStyle);
 	public virtual UIFontDescriptor GetFontDescriptor ();
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontAttributes</h3>
<pre>
public class UIFontAttributes : MonoTouch.Foundation.DictionaryContainer {
	
	public UIFontAttributes ();
	public UIFontAttributes (MonoTouch.Foundation.NSDictionary dictionary);
	
	public UIFontDescriptor[] CascadeList {
		get;
		set;
	}
	public MonoTouch.Foundation.NSCharacterSet CharacterSet {
		get;
		set;
	}
	public string Face {
		get;
		set;
	}
	public string Family {
		get;
		set;
	}
	public Nullable<float> FixedAdvance {
		get;
		set;
	}
	public System.Nullable<monotouch.coregraphics.cgaffinetransform> Matrix {
		get;
		set;
	}
	public string Name {
		get;
		set;
	}
	public Nullable<float> Size {
		get;
		set;
	}
	public string SizeString {
		get;
		set;
	}
	public MonoTouch.Foundation.NSString TextStyle {
		get;
		set;
	}
	public UIFontTraits Traits {
		get;
		set;
	}
	public MonoTouch.Foundation.NSDictionary Variation {
		get;
		set;
	}
	public string VisibleName {
		get;
		set;
	}
	public MonoTouch.Foundation.NSDictionary[] WeakFeatureSettings {
		get;
		set;
	}
}
</float></monotouch.coregraphics.cgaffinetransform></float></pre>
<h3>New Type: MonoTouch.UIKit.UIFontDescriptor</h3>
<pre>
public class UIFontDescriptor : MonoTouch.Foundation.NSObject {
	
	public UIFontDescriptor ();
	public UIFontDescriptor (MonoTouch.Foundation.NSCoder coder);
	public UIFontDescriptor (MonoTouch.Foundation.NSObjectFlag t);
	public UIFontDescriptor (IntPtr handle);
	public UIFontDescriptor (MonoTouch.Foundation.NSDictionary attributes);
	public UIFontDescriptor (UIFontAttributes attributes);
	
	public static UIFontDescriptor FromAttributes (MonoTouch.Foundation.NSDictionary attributes);
	public static UIFontDescriptor FromAttributes (UIFontAttributes attributes);
	public static UIFontDescriptor FromName (string fontName, MonoTouch.CoreGraphics.CGAffineTransform matrix);
	public static UIFontDescriptor FromName (string fontName, float size);
	public static UIFontDescriptor PreferredForStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
	public static UIFontDescriptor PreferredForStyle (UIFontTextStyle style);
	public virtual UIFontDescriptor CreateWithAttributes (MonoTouch.Foundation.NSDictionary attributes);
	public UIFontDescriptor CreateWithAttributes (UIFontAttributes attributes);
	public virtual UIFontDescriptor CreateWithFace (string newFace);
	public virtual UIFontDescriptor CreateWithFamily (string newFamily);
	public virtual UIFontDescriptor CreateWithMatrix (MonoTouch.CoreGraphics.CGAffineTransform matrix);
	public virtual UIFontDescriptor CreateWithSize (float newPointSize);
	public virtual UIFontDescriptor CreateWithTraits (UIFontDescriptorSymbolicTraits symbolicTraits);
	protected override void Dispose (bool disposing);
	public virtual UIFontDescriptor[] GetMatchingFontDescriptorsWithMandatoryKeys (MonoTouch.Foundation.NSSet mandatoryKeys);
	public virtual MonoTouch.Foundation.NSObject GetObject (MonoTouch.Foundation.NSString anAttribute);
	
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
	public override IntPtr ClassHandle {
		get;
	}
	public UIFontAttributes FontAttributes {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGAffineTransform Matrix {
		get;
	}
	public virtual float PointSize {
		get;
	}
	public virtual string PostscriptName {
		get;
	}
	public virtual UIFontDescriptorSymbolicTraits SymbolicTraits {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary WeakFontAttributes {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontDescriptorSymbolicTraits</h3>
<pre>
[Serializable]
[Flags]
public enum UIFontDescriptorSymbolicTraits : uint {
	Italic,
	Bold,
	Expanded,
	Condensed,
	MonoSpace,
	Vertical,
	UIOptimized,
	TightLeading,
	LooseLeading,
	ClassMask,
	ClassUnknown,
	ClassOldStyleSerifs,
	ClassTransitionalSerifs,
	ClassModernSerifs,
	ClassClarendonSerifs,
	ClassSlabSerifs,
	ClassFreeformSerifs,
	ClassSansSerif,
	ClassOrnamentals,
	ClassScripts,
	ClassSymbolic
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontTextStyle</h3>
<pre>
[Serializable]
public enum UIFontTextStyle {
	Headline,
	Body,
	Subheadline,
	Footnote,
	Caption1,
	Caption2
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontTraits</h3>
<pre>
public class UIFontTraits : MonoTouch.Foundation.DictionaryContainer {
	
	public UIFontTraits ();
	public UIFontTraits (MonoTouch.Foundation.NSDictionary dictionary);
	
	public Nullable<float> Slant {
		get;
		set;
	}
	public Nullable<uifontdescriptorsymbolictraits> SymbolicTrait {
		get;
		set;
	}
	public Nullable<float> Weight {
		get;
		set;
	}
	public Nullable<float> Width {
		get;
		set;
	}
}
</float></float></uifontdescriptorsymbolictraits></float></pre>
<h3>Type Changed: MonoTouch.UIKit.UIGestureRecognizer</h3>
<p>Added:</p><pre>
 	public UIGesturesProbe ShouldBeRequiredToFailBy {
 		get;
 		set;
 	}
 	public UIGesturesProbe ShouldRequireFailureOf {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate</h3>
<p>Removed:</p><pre>
 public class UIGestureRecognizerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIGestureRecognizerDelegate : MonoTouch.Foundation.NSObject, IUIGestureRecognizerDelegate {
 	public virtual bool ShouldBeRequiredToFailBy (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
 	public virtual bool ShouldRequireFailureOf (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
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
<h3>New Type: MonoTouch.UIKit.UIGravityBehavior</h3>
<pre>
public class UIGravityBehavior : UIDynamicBehavior {
	
	public UIGravityBehavior ();
	public UIGravityBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIGravityBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIGravityBehavior (IntPtr handle);
	public UIGravityBehavior (IUIDynamicItem[] items);
	
	public virtual void AddItem (IUIDynamicItem dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
	public virtual void SetAngleAndMagnitude (float angle, float magnitude);
	
	public virtual float Angle {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGVector GravityDirection {
		get;
		set;
	}
	public virtual IUIDynamicItem[] Items {
		get;
	}
	public virtual float Magnitude {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIGuidedAccessRestriction</h3>
<pre>
public static class UIGuidedAccessRestriction {
	
	public static UIGuidedAccessRestrictionState GetState (string restrictionIdentifier);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIGuidedAccessRestrictionState</h3>
<pre>
[Serializable]
public enum UIGuidedAccessRestrictionState {
	Allow,
	Deny
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Added:</p><pre>
 	public virtual UIImage ImageWithRenderingMode (UIImageRenderingMode renderingMode);
 	public virtual UIImageRenderingMode RenderingMode {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerController</h3>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIImagePickerControllerDelegate : UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class UIImagePickerControllerDelegate : UINavigationControllerDelegate, IUIImagePickerControllerDelegate {
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<h3>New Type: MonoTouch.UIKit.UIImagePickerControllerDelegate_Extensions</h3>
<pre>
public static class UIImagePickerControllerDelegate_Extensions {
	
	public static void Canceled (IUIImagePickerControllerDelegate This, UIImagePickerController picker);
	public static void FinishedPickingImage (IUIImagePickerControllerDelegate This, UIImagePickerController picker, UIImage image, MonoTouch.Foundation.NSDictionary editingInfo);
	public static void FinishedPickingMedia (IUIImagePickerControllerDelegate This, UIImagePickerController picker, MonoTouch.Foundation.NSDictionary info);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIImageRenderingMode</h3>
<pre>
[Serializable]
public enum UIImageRenderingMode {
	Automatic,
	AlwaysOriginal,
	AlwaysTemplate
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIInputView</h3>
<pre>
public class UIInputView : UIView {
	
	public UIInputView ();
	public UIInputView (MonoTouch.Foundation.NSCoder coder);
	public UIInputView (MonoTouch.Foundation.NSObjectFlag t);
	public UIInputView (IntPtr handle);
	public UIInputView (System.Drawing.RectangleF frame, UIInputViewStyle inputViewStyle);
	
	public static UIInputViewAppearance AppearanceWhenContainedIn (params Type [] containers);
	public static UIInputViewAppearance GetAppearance<t> ();
	
	public static UIInputViewAppearance Appearance {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIInputViewStyle InputViewStyle {
		get;
	}
	
	public class UIInputViewAppearance : UIViewAppearance {
	}
}
</t></pre>
<h3>New Type: MonoTouch.UIKit.UIInputViewStyle</h3>
<pre>
[Serializable]
public enum UIInputViewStyle {
	Default,
	Keyboard
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIInterpolatingMotionEffect</h3>
<pre>
public class UIInterpolatingMotionEffect : UIMotionEffect {
	
	public UIInterpolatingMotionEffect ();
	public UIInterpolatingMotionEffect (MonoTouch.Foundation.NSCoder coder);
	public UIInterpolatingMotionEffect (MonoTouch.Foundation.NSObjectFlag t);
	public UIInterpolatingMotionEffect (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string KeyPath {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject MaximumRelativeValue {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject MinimumRelativeValue {
		get;
		set;
	}
	public virtual UIInterpolatingMotionEffectType Type {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIInterpolatingMotionEffectType</h3>
<pre>
[Serializable]
public enum UIInterpolatingMotionEffectType {
	TiltAlongHorizontalAxis,
	TiltAlongVerticalAxis
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIKeyCommand</h3>
<pre>
public class UIKeyCommand : MonoTouch.Foundation.NSObject {
	
	public UIKeyCommand ();
	public UIKeyCommand (MonoTouch.Foundation.NSCoder coder);
	public UIKeyCommand (MonoTouch.Foundation.NSObjectFlag t);
	public UIKeyCommand (IntPtr handle);
	
	public static UIKeyCommand Create (MonoTouch.Foundation.NSString keyCommandInput, UIKeyModifierFlags modifierFlags, MonoTouch.ObjCRuntime.Selector action);
	protected override void Dispose (bool disposing);
	
	public static MonoTouch.Foundation.NSString DownArrow {
		get;
	}
	public static MonoTouch.Foundation.NSString Escape {
		get;
	}
	public static MonoTouch.Foundation.NSString LeftArrow {
		get;
	}
	public static MonoTouch.Foundation.NSString RightArrow {
		get;
	}
	public static MonoTouch.Foundation.NSString UpArrow {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSString Input {
		get;
	}
	public virtual UIKeyModifierFlags ModifierFlags {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIKeyModifierFlags</h3>
<pre>
[Serializable]
[Flags]
public enum UIKeyModifierFlags {
	AlphaShift,
	Shift,
	Control,
	Alternate,
	Command,
	NumericPad
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIKeyboardAppearance</h3>
<p>Removed:</p><pre>
 	Alert
</pre>
<p>Added:</p><pre>
 	Alert,
 	Dark,
 	Light
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIKeyboardType</h3>
<p>Removed:</p><pre>
 	Twitter
</pre>
<p>Added:</p><pre>
 	Twitter,
 	WebSearch
</pre>
<h3>Type Changed: MonoTouch.UIKit.UILabel</h3>
<p>Removed:</p><pre>
 	public virtual bool AdjustsLetterSpacingToFitWidth {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of NSKernAttributeName")]
	public virtual bool AdjustsLetterSpacingToFitWidth {
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
<h3>Type Changed: MonoTouch.UIKit.UIModalPresentationStyle</h3>
<p>Removed:</p><pre>
 	CurrentContext
</pre>
<p>Added:</p><pre>
 	CurrentContext,
 	Custom,
 	None
</pre>
<h3>New Type: MonoTouch.UIKit.UIMotionEffect</h3>
<pre>
public class UIMotionEffect : MonoTouch.Foundation.NSObject {
	
	public UIMotionEffect ();
	public UIMotionEffect (MonoTouch.Foundation.NSCoder coder);
	public UIMotionEffect (MonoTouch.Foundation.NSObjectFlag t);
	public UIMotionEffect (IntPtr handle);
	
	public virtual MonoTouch.Foundation.NSDictionary ComputeKeyPathsAndRelativeValues (UIOffset viewerOffset);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIMotionEffectGroup</h3>
<pre>
public class UIMotionEffectGroup : UIMotionEffect {
	
	public UIMotionEffectGroup ();
	public UIMotionEffectGroup (MonoTouch.Foundation.NSCoder coder);
	public UIMotionEffectGroup (MonoTouch.Foundation.NSObjectFlag t);
	public UIMotionEffectGroup (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIMotionEffect[] MotionEffects {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBar</h3>
<p>Added:</p><pre>
 	public virtual UIImage GetBackgroundImage (UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual UIImage BackIndicatorImage {
 		get;
 		set;
 	}
 	public virtual UIImage BackIndicatorTransitionMaskImage {
 		get;
 		set;
 	}
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 		public virtual UIImage GetBackgroundImage (UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual UIImage BackIndicatorImage {
 			get;
 			set;
 		}
 		public virtual UIImage BackIndicatorTransitionMaskImage {
 			get;
 			set;
 		}
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBarDelegate</h3>
<p>Removed:</p><pre>
 public class UINavigationBarDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UINavigationBarDelegate : UIBarPositioningDelegate, IUINavigationBarDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
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
<h3>Type Changed: MonoTouch.UIKit.UINavigationController</h3>
<p>Added:</p><pre>
 	public virtual UIGestureRecognizer InteractivePopGestureRecognizer {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UINavigationControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UINavigationControllerDelegate : MonoTouch.Foundation.NSObject, IUINavigationControllerDelegate {
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
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
<h3>New Type: MonoTouch.UIKit.UINavigationControllerOperation</h3>
<pre>
[Serializable]
public enum UINavigationControllerOperation {
	None,
	Push,
	Pop
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIObjectRestoration</h3>
<pre>
public class UIObjectRestoration : MonoTouch.Foundation.NSObject, IUIObjectRestoration {
	
	public UIObjectRestoration ();
	public UIObjectRestoration (MonoTouch.Foundation.NSCoder coder);
	public UIObjectRestoration (MonoTouch.Foundation.NSObjectFlag t);
	public UIObjectRestoration (IntPtr handle);
	
	public virtual IUIStateRestoring GetStateRestorationObjectFromPath (MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIObjectRestoration_Extensions</h3>
<pre>
public static class UIObjectRestoration_Extensions {
	
	public static IUIStateRestoring GetStateRestorationObjectFromPath (IUIObjectRestoration This, MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Added:</p><pre>
 	public Func&lt;UIPageViewController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientationForPresentation {
 		get;
 		set;
 	}
 	public Func&lt;UIPageViewController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
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
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (UIPageViewController pageViewController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIPageViewController pageViewController);
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
<h3>New Type: MonoTouch.UIKit.UIPercentDrivenInteractiveTransition</h3>
<pre>
public class UIPercentDrivenInteractiveTransition : MonoTouch.Foundation.NSObject {
	
	public UIPercentDrivenInteractiveTransition ();
	public UIPercentDrivenInteractiveTransition (MonoTouch.Foundation.NSCoder coder);
	public UIPercentDrivenInteractiveTransition (MonoTouch.Foundation.NSObjectFlag t);
	public UIPercentDrivenInteractiveTransition (IntPtr handle);
	
	public virtual void CancelInteractiveTransition ();
	public virtual void FinishInteractiveTransition ();
	public virtual void StartInteractiveTransition (UIViewControllerContextTransitioning transitionContext);
	public virtual void UpdateInteractiveTransition (float percentComplete);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIViewAnimationCurve CompletionCurve {
		get;
		set;
	}
	public virtual float CompletionSpeed {
		get;
		set;
	}
	public virtual float Duration {
		get;
	}
	public virtual float PercentComplete {
		get;
	}
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
<h3>Type Changed: MonoTouch.UIKit.UIPopoverController</h3>
<p>Added:</p><pre>
 	public virtual UIColor BackgroundColor {
 		get;
 		set;
 	}
 	public event EventHandler&lt;UIPopoverControllerRepositionEventArgs&gt; WillReposition;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIPopoverControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPopoverControllerDelegate : MonoTouch.Foundation.NSObject, IUIPopoverControllerDelegate {
 	public virtual void WillReposition (UIPopoverController popoverController, ref System.Drawing.RectangleF rect, ref UIView view);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPopoverControllerDelegate_Extensions</h3>
<pre>
public static class UIPopoverControllerDelegate_Extensions {
	
	public static void DidDismiss (IUIPopoverControllerDelegate This, UIPopoverController popoverController);
	public static bool ShouldDismiss (IUIPopoverControllerDelegate This, UIPopoverController popoverController);
	public static void WillReposition (IUIPopoverControllerDelegate This, UIPopoverController popoverController, ref System.Drawing.RectangleF rect, ref UIView view);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIPopoverControllerRepositionEventArgs</h3>
<pre>
public class UIPopoverControllerRepositionEventArgs : EventArgs {
	
	public UIPopoverControllerRepositionEventArgs (System.Drawing.RectangleF rect, UIView view);
	
	public System.Drawing.RectangleF Rect {
		get;
		set;
	}
	public UIView View {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintFormatter</h3>
<p>Added:</p><pre>
 	public UIPrintFormatter (string text);
 	public UIPrintFormatter (MonoTouch.Foundation.NSAttributedString attributedText);
 	public virtual MonoTouch.Foundation.NSAttributedString AttributedText {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInfoOutputType</h3>
<p>Removed:</p><pre>
 	Grayscale
</pre>
<p>Added:</p><pre>
 	Grayscale,
 	PhotoGrayscale
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionController</h3>
<p>Added:</p><pre>
 	public Func&lt;UIPrintInteractionController,UIPrintPaper,float&gt; CutLengthForPaper {
 		get;
 		set;
 	}
 	public virtual bool ShowsNumberOfCopies {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPrintInteractionControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIPrintInteractionControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIPrintInteractionControllerDelegate : MonoTouch.Foundation.NSObject, IUIPrintInteractionControllerDelegate {
 	public virtual float CutLengthForPaper (UIPrintInteractionController printInteractionController, UIPrintPaper paper);
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
<h3>New Type: MonoTouch.UIKit.UIPushBehavior</h3>
<pre>
public class UIPushBehavior : UIDynamicBehavior {
	
	public UIPushBehavior ();
	public UIPushBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIPushBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIPushBehavior (IntPtr handle);
	public UIPushBehavior (IUIDynamicItem[] items, UIPushBehaviorMode mode);
	
	public virtual void AddItem (IUIDynamicItem dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual UIOffset GetTargetOffsetFromCenter (IUIDynamicItem item);
	public virtual void RemoveItem (IUIDynamicItem dynamicItem);
	public virtual void SetAngleAndMagnitude (float angle, float magnitude);
	public virtual void SetTargetOffset (UIOffset offset, IUIDynamicItem item);
	
	public virtual bool Active {
		get;
		set;
	}
	public virtual float Angle {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual IUIDynamicItem[] Items {
		get;
	}
	public virtual float Magnitude {
		get;
		set;
	}
	public virtual UIPushBehaviorMode Mode {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGVector PushDirection {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIPushBehaviorMode</h3>
<pre>
[Serializable]
public enum UIPushBehaviorMode {
	Continuous,
	Instantaneous
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIRectEdge</h3>
<pre>
[Serializable]
public enum UIRectEdge {
	None,
	Top,
	Left,
	Bottom,
	Right,
	All
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIResponder</h3>
<p>Added:</p><pre>
 	public static void ClearTextInputContextIdentifier (MonoTouch.Foundation.NSString identifier);
 	public virtual MonoTouch.Foundation.NSObject GetTargetForAction (MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSObject sender);
 	public virtual UIKeyCommand[] KeyCommands {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString TextInputContextIdentifier {
 		get;
 	}
 	public virtual UITextInputMode TextInputMode {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UIResponder_NSObjectExtension</h3>
<pre>
public static class UIResponder_NSObjectExtension {
	
	public static void DecreaseSize (UIResponder This, MonoTouch.Foundation.NSObject sender);
	public static void IncreaseSize (UIResponder This, MonoTouch.Foundation.NSObject sender);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScreen</h3>
<p>Added:</p><pre>
 	public virtual UIView SnapshotView (bool afterScreenUpdates);
</pre>
<h3>New Type: MonoTouch.UIKit.UIScreenEdgePanGestureRecognizer</h3>
<pre>
public class UIScreenEdgePanGestureRecognizer : UIPanGestureRecognizer {
	
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSAction action);
	public UIScreenEdgePanGestureRecognizer (Action<uiscreenedgepangesturerecognizer> action);
	public UIScreenEdgePanGestureRecognizer ();
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSCoder coder);
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSObjectFlag t);
	public UIScreenEdgePanGestureRecognizer (IntPtr handle);
	public UIScreenEdgePanGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual UIRectEdge Edges {
		get;
		set;
	}
}
</uiscreenedgepangesturerecognizer></pre>
<h3>Type Changed: MonoTouch.UIKit.UIScrollView</h3>
<p>Added:</p><pre>
 	public virtual UIScrollViewKeyboardDismissMode KeyboardDismissMode {
 		get;
 		set;
 	}
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
<h3>New Type: MonoTouch.UIKit.UIScrollViewKeyboardDismissMode</h3>
<pre>
[Serializable]
public enum UIScrollViewKeyboardDismissMode {
	None,
	OnDrag,
	Interactive
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Added:</p><pre>
 	public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
 	public virtual UIImage BackgroundImageForBarPosition (UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
 	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 	public System.Func&lt;MonoTouch.Foundation.NSObject,UIBarPosition&gt; GetPositionForBar {
 		get;
 		set;
 	}
 	public virtual UISearchBarStyle SearchBarStyle {
 		get;
 		set;
 	}
 		public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
 		public virtual UIImage BackgroundImageForBarPosition (UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
 		public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarPosition barPosition, UIBarMetrics barMetrics);
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBarDelegate</h3>
<p>Removed:</p><pre>
 public class UISearchBarDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UISearchBarDelegate : UIBarPositioningDelegate, IUISearchBarDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
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
<h3>New Type: MonoTouch.UIKit.UISearchBarStyle</h3>
<pre>
[Serializable]
public enum UISearchBarStyle : uint {
	Default,
	Prominent,
	Minimal
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchDisplayController</h3>
<p>Added:</p><pre>
 	public virtual bool DisplaysSearchBarInNavigationBar {
 		get;
 		set;
 	}
 	public virtual UINavigationItem NavigationItem {
 		get;
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
<h3>Type Changed: MonoTouch.UIKit.UISegmentedControl</h3>
<p>Removed:</p><pre>
 	public virtual UISegmentedControlStyle ControlStyle {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual UISegmentedControlStyle ControlStyle {
</pre>
<h3>New Type: MonoTouch.UIKit.UISnapBehavior</h3>
<pre>
public class UISnapBehavior : UIDynamicBehavior {
	
	public UISnapBehavior (MonoTouch.Foundation.NSCoder coder);
	public UISnapBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UISnapBehavior (IntPtr handle);
	public UISnapBehavior (IUIDynamicItem dynamicItem, System.Drawing.PointF point);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float Damping {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISplitViewController</h3>
<p>Added:</p><pre>
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UISplitViewController splitViewController);
 	public virtual UIInterfaceOrientation PreferredInterfaceOrientationForPresentation (UISplitViewController splitViewController);
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
<h3>New Type: MonoTouch.UIKit.UIStateRestoring</h3>
<pre>
public class UIStateRestoring : MonoTouch.Foundation.NSObject, IUIStateRestoring {
	
	public UIStateRestoring ();
	public UIStateRestoring (MonoTouch.Foundation.NSCoder coder);
	public UIStateRestoring (MonoTouch.Foundation.NSObjectFlag t);
	public UIStateRestoring (IntPtr handle);
	
	public virtual void ApplicationFinishedRestoringState ();
	public virtual void DecodeRestorableState (MonoTouch.Foundation.NSCoder coder);
	public virtual void EncodeRestorableState (MonoTouch.Foundation.NSCoder coder);
	
	public virtual MonoTouch.ObjCRuntime.Class ObjectRestorationClass {
		get;
	}
	public virtual IUIStateRestoring RestorationParent {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIStateRestoring_Extensions</h3>
<pre>
public static class UIStateRestoring_Extensions {
	
	public static void ApplicationFinishedRestoringState (IUIStateRestoring This);
	public static void DecodeRestorableState (IUIStateRestoring This, MonoTouch.Foundation.NSCoder coder);
	public static void EncodeRestorableState (IUIStateRestoring This, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStatusBarStyle</h3>
<p>Added:</p><pre>
 	LightContent,
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributeKey</h3>
<p>Removed:</p><pre>
 	public static readonly MonoTouch.Foundation.NSString Font;
 	public static readonly MonoTouch.Foundation.NSString ForegroundColor;
 	public static readonly MonoTouch.Foundation.NSString BackgroundColor;
 	public static readonly MonoTouch.Foundation.NSString StrikethroughStyle;
 	public static readonly MonoTouch.Foundation.NSString StrokeColor;
 	public static readonly MonoTouch.Foundation.NSString Shadow;
 	public static readonly MonoTouch.Foundation.NSString ParagraphStyle;
 	public static readonly MonoTouch.Foundation.NSString Ligature;
 	public static readonly MonoTouch.Foundation.NSString KerningAdjustment;
 	public static readonly MonoTouch.Foundation.NSString UnderlineStyle;
 	public static readonly MonoTouch.Foundation.NSString StrokeWidth;
 	public static readonly MonoTouch.Foundation.NSString VerticalGlyphForm;
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString Attachment {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BackgroundColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BaselineOffset {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Expansion {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Font {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ForegroundColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString KerningAdjustment {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Ligature {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Link {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Obliqueness {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ParagraphStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Shadow {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrikethroughColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrikethroughStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrokeColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StrokeWidth {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextAlternatives {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextEffect {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UnderlineColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UnderlineStyle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString VerticalGlyphForm {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WritingDirection {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributes</h3>
<p>Added:</p><pre>
 	public Nullable&lt;float&gt; BaselineOffset {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; Expansion {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSUrl Link {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; Obliqueness {
 		get;
 		set;
 	}
 	public UIColor StrikethroughColor {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSObject TextAlternativesObject {
 		get;
 		set;
 	}
 	public NSTextAttachment TextAttachment {
 		get;
 		set;
 	}
 	public NSTextEffect TextEffect {
 		get;
 		set;
 	}
 	public UIColor UnderlineColor {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSString WeakTextEffect {
 		get;
 		set;
 	}
 	public MonoTouch.Foundation.NSNumber[] WritingDirectionInt {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UISystemAnimation</h3>
<pre>
[Serializable]
public enum UISystemAnimation {
	Delete
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBar</h3>
<p>Added:</p><pre>
 	public virtual UIBarStyle BarStyle {
 		get;
 		set;
 	}
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 	public virtual UITabBarItemPositioning ItemPositioning {
 		get;
 		set;
 	}
 	public virtual float ItemSpacing {
 		get;
 		set;
 	}
 	public virtual float ItemWidth {
 		get;
 		set;
 	}
 	public virtual bool Translucent {
 		get;
 		set;
 	}
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarController</h3>
<p>Added:</p><pre>
 	public Func&lt;UITabBarController,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForTransition {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 		get;
 		set;
 	}
 	public Func&lt;UITabBarController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UITabBarControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UITabBarControllerDelegate : MonoTouch.Foundation.NSObject, IUITabBarControllerDelegate {
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UITabBarController tabBarController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UITabBarController tabBarController);
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
<h3>Type Changed: MonoTouch.UIKit.UITabBarItem</h3>
<p>Removed:</p><pre>
 	public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);
 	public virtual UIImage FinishedSelectedImage {
 	public virtual UIImage FinishedUnselectedImage {
</pre>
<p>Added:</p><pre>
 	public UITabBarItem (string title, UIImage image, UIImage selectedImage);
 	[Obsolete("Deprecated in iOS7")]
	public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);
 	[Obsolete("Deprecated in iOS7")]
	public virtual UIImage FinishedSelectedImage {
 	[Obsolete("Deprecated in iOS7")]
	public virtual UIImage FinishedUnselectedImage {
 	public virtual UIImage SelectedImage {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UITabBarItemPositioning</h3>
<pre>
[Serializable]
public enum UITabBarItemPositioning {
	Automatic,
	Fill,
	Centered
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Added:</p><pre>
 	public virtual float EstimatedRowHeight {
 		get;
 		set;
 	}
 	public virtual float EstimatedSectionFooterHeight {
 		get;
 		set;
 	}
 	public virtual float EstimatedSectionHeaderHeight {
 		get;
 		set;
 	}
 	public virtual UIColor SectionIndexBackgroundColor {
 		get;
 		set;
 	}
 	public virtual UIEdgeInsets SeparatorInset {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCell</h3>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets SeparatorInset {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCellAccessory</h3>
<p>Removed:</p><pre>
 	Checkmark
</pre>
<p>Added:</p><pre>
 	Checkmark,
 	DetailButton
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewCellSelectionStyle</h3>
<p>Removed:</p><pre>
 	Gray
</pre>
<p>Added:</p><pre>
 	Gray,
 	Default
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewController</h3>
<p>Added:</p><pre>
 	public virtual float EstimatedHeight (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float EstimatedHeightForFooter (UITableView tableView, int section);
 	public virtual float EstimatedHeightForHeader (UITableView tableView, int section);
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
 	public virtual float EstimatedHeight (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float EstimatedHeightForFooter (UITableView tableView, int section);
 	public virtual float EstimatedHeightForHeader (UITableView tableView, int section);
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
<h3>Type Changed: MonoTouch.UIKit.UITableViewSource</h3>
<p>Added:</p><pre>
 	public virtual float EstimatedHeight (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float EstimatedHeightForFooter (UITableView tableView, int section);
 	public virtual float EstimatedHeightForHeader (UITableView tableView, int section);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextField</h3>
<p>Removed:</p><pre>
 	public virtual UITextStorageDirection SelectionAffinity {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary WeakDefaultTextAttributes {
 		get;
 		set;
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
<h3>Type Changed: MonoTouch.UIKit.UITextInputMode</h3>
<p>Removed:</p><pre>
 	public static UITextInputMode CurrentInputMode {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in IOS7")]
	public static UITextInputMode CurrentInputMode {
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
<h3>Type Changed: MonoTouch.UIKit.UITextView</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSRange SelectedRange {
 	public virtual UITextRange SelectedTextRange {
 	public virtual UITextStorageDirection SelectionAffinity {
</pre>
<p>Added:</p><pre>
 	public UITextView (System.Drawing.RectangleF frame, NSTextContainer textContainer);
 	public virtual NSLayoutManager LayoutManager {
 		get;
 	}
 	public virtual bool Selectable {
 	public virtual MonoTouch.Foundation.NSRange SelectedRange {
 	public virtual UITextRange SelectedTextRange {
 	public System.Func&lt;UITextView,NSTextAttachment,MonoTouch.Foundation.NSRange,bool&gt; ShouldInteractWithTextAttachment {
 		get;
 		set;
 	}
 	public System.Func&lt;UITextView,MonoTouch.Foundation.NSUrl,MonoTouch.Foundation.NSRange,bool&gt; ShouldInteractWithUrl {
 		get;
 		set;
 	}
 	public virtual NSTextContainer TextContainer {
 		get;
 	}
 	public virtual UIEdgeInsets TextContainerInset {
 		get;
 		set;
 	}
 	public virtual NSTextStorage TextStorage {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary WeakLinkTextAttributes {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextViewDelegate</h3>
<p>Removed:</p><pre>
 public class UITextViewDelegate : UIScrollViewDelegate {
</pre>
<p>Added:</p><pre>
 public class UITextViewDelegate : UIScrollViewDelegate, IUITextViewDelegate {
 	public virtual bool ShouldInteractWithTextAttachment (UITextView textView, NSTextAttachment textAttachment, MonoTouch.Foundation.NSRange characterRange);
 	public virtual bool ShouldInteractWithUrl (UITextView textView, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSRange characterRange);
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
<h3>Type Changed: MonoTouch.UIKit.UIToolbar</h3>
<p>Added:</p><pre>
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public virtual UIColor BarTintColor {
 		get;
 		set;
 	}
 	public UIToolbarDelegate Delegate {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
 		get;
 		set;
 	}
 		public virtual UIColor BarTintColor {
 			get;
 			set;
 		}
</pre>
<h3>New Type: MonoTouch.UIKit.UIToolbarDelegate</h3>
<pre>
public class UIToolbarDelegate : UIBarPositioningDelegate, IUIToolbarDelegate {
	
	public UIToolbarDelegate ();
	public UIToolbarDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIToolbarDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIToolbarDelegate (IntPtr handle);
	
	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIToolbarDelegate_Extensions</h3>
<pre>
public static class UIToolbarDelegate_Extensions {
}
</pre>
<h3>New Type: MonoTouch.UIKit.UITransitionContext</h3>
<pre>
public static class UITransitionContext {
	
	public static MonoTouch.Foundation.NSString FromViewControllerKey {
		get;
	}
	public static MonoTouch.Foundation.NSString ToViewControllerKey {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorController</h3>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientation {
 		get;
 		set;
 	}
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorControllerDelegate</h3>
<p>Removed:</p><pre>
 public class UIVideoEditorControllerDelegate : UINavigationControllerDelegate {
</pre>
<p>Added:</p><pre>
 public class UIVideoEditorControllerDelegate : UINavigationControllerDelegate, IUIVideoEditorControllerDelegate {
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
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
 	public static void AddKeyframeWithRelativeStartTime (double frameStartTime, double frameDuration, MonoTouch.Foundation.NSAction animations);
 	public static void AnimateKeyframes (double duration, double delay, UIViewKeyframeAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completion);
 	public static void AnimateNotify (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completion);
 	public static void PerformSystemAnimation (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction parallelAnimations, UICompletionHandler completion);
 	public static void PerformWithoutAnimation (MonoTouch.Foundation.NSAction actionsWithoutAnimation);
 	public virtual bool AccessibilityActivate ();
 	public virtual void AddMotionEffect (UIMotionEffect effect);
 	public virtual bool DrawViewHierarchy (System.Drawing.RectangleF rect, bool afterScreenUpdates);
 	public virtual void RemoveMotionEffect (UIMotionEffect effect);
 	public virtual UIView ResizableSnapshotView (System.Drawing.RectangleF rect, bool afterScreenUpdates, UIEdgeInsets capInsets);
 	public virtual UIView SnapshotView (bool afterScreenUpdates);
 	public virtual void TintColorDidChange ();
 	public static MonoTouch.Foundation.NSString SpeechAttributeLanguage {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SpeechAttributePitch {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SpeechAttributePunctuation {
 		get;
 	}
 	public virtual UIBezierPath AccessibilityPath {
 		get;
 		set;
 	}
 	public virtual UIMotionEffect[] MotionEffects {
 		get;
 		set;
 	}
 	public virtual UIViewTintAdjustmentMode TintAdjustmentMode {
 		get;
 		set;
 	}
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewAnimationOptions</h3>
<p>Added:</p><pre>
 	OverrideInheritedOptions,
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	public virtual System.Drawing.SizeF ContentSizeForViewInPopover {
 	public virtual bool WantsFullScreenLayout {
</pre>
<p>Added:</p><pre>
 	public virtual void ApplicationFinishedRestoringState ();
 	public virtual UIViewController ChildViewControllerForStatusBarHidden ();
 	public virtual UIViewController ChildViewControllerForStatusBarStyle ();
 	public virtual UIStatusBarStyle PreferredStatusBarStyle ();
 	public virtual bool PrefersStatusBarHidden ();
 	public virtual void SetNeedsStatusBarAppearanceUpdate ();
 	public virtual bool AutomaticallyAdjustsScrollViewInsets {
 		get;
 		set;
 	}
 	public virtual IUILayoutSupport BottomLayoutGuide {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7 in favor of PreferredContentSize")]
	public virtual System.Drawing.SizeF ContentSizeForViewInPopover {
 	public virtual UIRectEdge EdgesForExtendedLayout {
 		get;
 		set;
 	}
 	public virtual bool ExtendedLayoutIncludesOpaqueBars {
 		get;
 		set;
 	}
 	public virtual bool ModalPresentationCapturesStatusBarAppearance {
 		get;
 		set;
 	}
 	public virtual System.Drawing.SizeF PreferredContentSize {
 		get;
 		set;
 	}
 	public virtual UIStatusBarAnimation PreferredStatusBarUpdateAnimation {
 		get;
 	}
 	public virtual IUILayoutSupport TopLayoutGuide {
 		get;
 	}
 	public UIViewControllerTransitioningDelegate TransitioningDelegate {
 		get;
 		set;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual bool WantsFullScreenLayout {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSObject WeakTransitioningDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerAnimatedTransitioning</h3>
<pre>
public abstract class UIViewControllerAnimatedTransitioning : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerAnimatedTransitioning ();
	public UIViewControllerAnimatedTransitioning (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerAnimatedTransitioning (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerAnimatedTransitioning (IntPtr handle);
	
	public abstract void AnimateTransition (UIViewControllerContextTransitioning transitionContext);
	public virtual void AnimationEnded (bool transitionCompleted);
	public abstract double TransitionDuration (UIViewControllerContextTransitioning transitionContext);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerContextTransitioning</h3>
<pre>
public abstract class UIViewControllerContextTransitioning : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerContextTransitioning ();
	public UIViewControllerContextTransitioning (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerContextTransitioning (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerContextTransitioning (IntPtr handle);
	
	public abstract void CancelInteractiveTransition ();
	public abstract void CompleteTransition (bool didComplete);
	public abstract void FinishInteractiveTransition ();
	public abstract System.Drawing.RectangleF GetFinalFrameForViewController (UIViewController vc);
	public abstract System.Drawing.RectangleF GetInitialFrameForViewController (UIViewController vc);
	public abstract UIViewController GetViewControllerForKey (MonoTouch.Foundation.NSString uiTransitionKey);
	public abstract void UpdateInteractiveTransition (float percentComplete);
	
	public abstract UIView ContainerView {
		get;
	}
	public abstract bool IsAnimated {
		get;
	}
	public abstract bool IsInteractive {
		get;
	}
	public abstract UIModalPresentationStyle PresentationStyle {
		get;
	}
	public abstract bool TransitionWasCancelled {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerInteractiveTransitioning</h3>
<pre>
public abstract class UIViewControllerInteractiveTransitioning : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerInteractiveTransitioning ();
	public UIViewControllerInteractiveTransitioning (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerInteractiveTransitioning (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerInteractiveTransitioning (IntPtr handle);
	
	public abstract void StartInteractiveTransition (UIViewControllerContextTransitioning transitionContext);
	
	public virtual UIViewAnimationCurve CompletionCurve {
		get;
	}
	public virtual float CompletionSpeed {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitionCoordinator</h3>
<pre>
public abstract class UIViewControllerTransitionCoordinator : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerTransitionCoordinator ();
	public UIViewControllerTransitionCoordinator (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerTransitionCoordinator (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerTransitionCoordinator (IntPtr handle);
	
	public abstract bool AnimateAlongsideTransition (Action<uiviewcontrollertransitioncoordinatorcontext> animate, Action<uiviewcontrollertransitioncoordinatorcontext> completion);
	public abstract bool AnimateAlongsideTransitionInView (UIView view, Action<uiviewcontrollertransitioncoordinatorcontext> animation, Action<uiviewcontrollertransitioncoordinatorcontext> completion);
	public virtual UIViewController GetViewControllerForKey (MonoTouch.Foundation.NSString uiTransitionKey);
	public abstract void NotifyWhenInteractionEndsUsingBlock (Action<uiviewcontrollertransitioncoordinatorcontext> handler);
	
	public virtual UIViewAnimationCurve CompletionCurve {
		get;
	}
	public virtual float CompletionVelocity {
		get;
	}
	public virtual UIView ContainerView {
		get;
	}
	public virtual bool InitiallyInteractive {
		get;
	}
	public virtual bool IsAnimated {
		get;
	}
	public virtual bool IsCancelled {
		get;
	}
	public virtual bool IsInteractive {
		get;
	}
	public virtual float PercentComplete {
		get;
	}
	public virtual UIModalPresentationStyle PresentationStyle {
		get;
	}
	public virtual double TransitionDuration {
		get;
	}
}
</uiviewcontrollertransitioncoordinatorcontext></uiviewcontrollertransitioncoordinatorcontext></uiviewcontrollertransitioncoordinatorcontext></uiviewcontrollertransitioncoordinatorcontext></uiviewcontrollertransitioncoordinatorcontext></pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext</h3>
<pre>
public abstract class UIViewControllerTransitionCoordinatorContext : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerTransitionCoordinatorContext ();
	public UIViewControllerTransitionCoordinatorContext (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerTransitionCoordinatorContext (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerTransitionCoordinatorContext (IntPtr handle);
	
	public abstract UIViewController GetViewControllerForKey (MonoTouch.Foundation.NSString uiTransitionKey);
	
	public abstract UIViewAnimationCurve CompletionCurve {
		get;
	}
	public abstract float CompletionVelocity {
		get;
	}
	public abstract UIView ContainerView {
		get;
	}
	public abstract bool InitiallyInteractive {
		get;
	}
	public abstract bool IsAnimated {
		get;
	}
	public abstract bool IsCancelled {
		get;
	}
	public abstract bool IsInteractive {
		get;
	}
	public abstract float PercentComplete {
		get;
	}
	public abstract UIModalPresentationStyle PresentationStyle {
		get;
	}
	public abstract double TransitionDuration {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitioningDelegate</h3>
<pre>
public class UIViewControllerTransitioningDelegate : MonoTouch.Foundation.NSObject {
	
	public UIViewControllerTransitioningDelegate ();
	public UIViewControllerTransitioningDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIViewControllerTransitioningDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIViewControllerTransitioningDelegate (IntPtr handle);
	
	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForDismissedController (UIViewController dismissed);
	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForDismissal (UIViewControllerAnimatedTransitioning animator);
	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForPresentation (UIViewControllerAnimatedTransitioning animator);
	public virtual UIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewKeyframeAnimationOptions</h3>
<pre>
[Serializable]
public enum UIViewKeyframeAnimationOptions : uint {
	LayoutSubviews,
	AllowUserInteraction,
	BeginFromCurrentState,
	Repeat,
	Autoreverse,
	OverrideInheritedDuration,
	OverrideInheritedOptions,
	CalculationModeLinear,
	CalculationModeDiscrete,
	CalculationModePaced,
	CalculationModeCubic,
	CalculationModeCubicPaced
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewTintAdjustmentMode</h3>
<pre>
[Serializable]
public enum UIViewTintAdjustmentMode {
	Automatic,
	Normal,
	Dimmed
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIWebPaginationBreakingMode</h3>
<pre>
[Serializable]
public enum UIWebPaginationBreakingMode {
	Page,
	Column
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIWebPaginationMode</h3>
<pre>
[Serializable]
public enum UIWebPaginationMode {
	Unpaginated,
	LeftToRight,
	TopToBottom,
	BottomToTop,
	RightToLeft
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIWebView</h3>
<p>Added:</p><pre>
 	public virtual float GapBetweenPages {
 		get;
 		set;
 	}
 	public virtual int PageCount {
 		get;
 	}
 	public virtual float PageLength {
 		get;
 		set;
 	}
 	public virtual UIWebPaginationBreakingMode PaginationBreakingMode {
 		get;
 		set;
 	}
 	public virtual UIWebPaginationMode PaginationMode {
 		get;
 		set;
 	}
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
<h3>New Type: MonoTouch.UIKit._UIContentSizeCategory</h3>
<pre>
public static class _UIContentSizeCategory {
	
	public static MonoTouch.Foundation.NSString AccessibilityExtraExtraExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString AccessibilityExtraExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString AccessibilityExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString AccessibilityLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString AccessibilityMedium {
		get;
	}
	public static MonoTouch.Foundation.NSString ExtraExtraExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString ExtraExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString ExtraLarge {
		get;
	}
	public static MonoTouch.Foundation.NSString ExtraSmall {
		get;
	}
	public static MonoTouch.Foundation.NSString Large {
		get;
	}
	public static MonoTouch.Foundation.NSString Medium {
		get;
	}
	public static MonoTouch.Foundation.NSString Small {
		get;
	}
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
<h3>Type Changed: MonoTouch.iAd.ADInterstitialAd</h3>
<p>Removed:</p><pre>
 	public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Obsolete in iOS 7. Use extension method UIViewController.requestInterstitialAdPresentation instead")]
	public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
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
<h3>New Type: MonoTouch.iAd.ADInterstitialPresentationPolicy</h3>
<pre>
[Serializable]
public enum ADInterstitialPresentationPolicy {
	None,
	Automatic,
	Manual
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
<h3>New Type: MonoTouch.iAd.IAdAdditions</h3>
<pre>
public static class IAdAdditions {
	
	public static bool DisplayingBannerAd (MonoTouch.UIKit.UIViewController This);
	public static bool GetCanDisplayBannerAds (MonoTouch.UIKit.UIViewController This);
	public static ADInterstitialPresentationPolicy GetInterstitialPresentationPolicy (MonoTouch.UIKit.UIViewController This);
	public static MonoTouch.UIKit.UIView GetOriginalContentView (MonoTouch.UIKit.UIViewController This);
	public static void PrepareInterstitialAds (MonoTouch.UIKit.UIViewController This);
	public static bool PresentingFullScreenAd (MonoTouch.UIKit.UIViewController This);
	public static bool RequestInterstitialAdPresentation (MonoTouch.UIKit.UIViewController This);
	public static void SetCanDisplayBannerAds (MonoTouch.UIKit.UIViewController This, bool value);
	public static void SetInterstitialPresentationPolicy (MonoTouch.UIKit.UIViewController This, ADInterstitialPresentationPolicy policy);
	public static bool ShouldPresentInterstitialAd (MonoTouch.UIKit.UIViewController This);
}
</pre>
<h3>New Type: MonoTouch.iAd.IAdPreroll</h3>
<pre>
public static class IAdPreroll {
	
	public static void PlayPrerollAd (MonoTouch.MediaPlayer.MPMoviePlayerController This, PlayPrerollAdCompletionHandler completionHandler);
	public static void PreparePrerollAds (MonoTouch.MediaPlayer.MPMoviePlayerController This);
}
</pre>
<h3>New Type: MonoTouch.iAd.PlayPrerollAdCompletionHandler</h3>
<pre>
[Serializable]
public delegate void PlayPrerollAdCompletionHandler (MonoTouch.Foundation.NSError error);
</pre>
</body>
</html>
