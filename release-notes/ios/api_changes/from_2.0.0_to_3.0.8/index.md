---
id: 80FC9961-2625-40A2-9B01-E11D940155E7
title: "From 2.0.0 to 3.0.8"
---

<html><head><title>Comparison between mt-200 and mt-308.6843</title></head>
<body>
<h3>Namespace: MonoTouch</h3>
<h4>Type Changed: MonoTouch.Constants</h4>
<p>Removed:</p><pre>
 	public const string Version = "2.0.0";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.8";
 	public const string FoundationLibrary = "/System/Library/Frameworks/Foundation.framework/Foundation";
 	public const string CoreAnimationLibrary = "/System/Library/Frameworks/QuartzCore.framework/QuartzCore";
 	public const string iAdLibrary = "/System/Library/Frameworks/AdLib.framework/AdLib";
 	public const string CoreTelephonyLibrary = "/System/Library/Frameworks/CoreTelephony.framework/CoreTelephony";
 	public const string CoreMediaLibrary = "/System/Library/Frameworks/CoreMedia.framework/CoreMedia";
 	public const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
 	public const string EventKitLibrary = "/System/Library/Frameworks/EventKit.framework/EventKit";
</pre>
<h3>Namespace: MonoTouch.AVFoundation</h3>
<h4>New Type: MonoTouch.AVFoundation.AVAsset</h4>
<pre>
public class AVAsset : MonoTouch.Foundation.NSObject {
	
	public AVAsset ();
	public AVAsset (MonoTouch.Foundation.NSCoder coder);
	public AVAsset (MonoTouch.Foundation.NSObjectFlag t);
	public AVAsset (IntPtr handle);
	
	public virtual void CancelLoading ();
	public virtual AVMetadataItem[] MetadataForFormat (string format);
	public virtual AVAssetTrack[] TracksWithMediaCharacteristic (string mediaCharacteristic);
	public virtual AVAssetTrack[] TracksWithMediaType (string mediaType);
	public virtual AVAssetTrack TrackWithTrackID (int trackID);
	
	public virtual string [] AvailableMetadataFormats {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVMetadataItem[] CommonMetadata {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime Duration {
		get;
	}
	public virtual string Lyrics {
		get;
	}
	public virtual System.Drawing.SizeF NaturalSize {
		get;
	}
	public virtual float PreferredRate {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGAffineTransform PreferredTransform {
		get;
	}
	public virtual float PreferredVolume {
		get;
	}
	public virtual bool ProvidesPreciseDurationAndTiming {
		get;
	}
	public virtual AVAssetTrack[] Tracks {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAssetExportSession</h4>
<pre>
public class AVAssetExportSession : MonoTouch.Foundation.NSObject {
	
	public AVAssetExportSession ();
	public AVAssetExportSession (MonoTouch.Foundation.NSCoder coder);
	public AVAssetExportSession (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetExportSession (IntPtr handle);
	public AVAssetExportSession (AVAsset asset, string presetName);
	
	public static string [] ExportPresetsCompatibleWithAsset (AVAsset asset);
	public virtual void CancelExport ();
	public virtual void ExportAsynchronously (AVErrorHandler errorHandler);
	
	public virtual string [] AllExportPresets {
		get;
	}
	public virtual AVAudioMix AudioMix {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual long FileLengthLimit {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTime MaxDuration {
		get;
	}
	public virtual AVMetadataItem[] Metadata {
		get;
		set;
	}
	public virtual string OutputFileType {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSUrl OutputUrl {
		get;
		set;
	}
	public virtual string PresetName {
		get;
	}
	public virtual float Progress {
		get;
	}
	public virtual bool ShouldOptimizeForNetworkUse {
		get;
		set;
	}
	public virtual AVAssetExportSessionStatus Status {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] SupportedFileTypes {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
		set;
	}
	public virtual AVVideoComposition VideoComposition {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAssetExportSessionStatus</h4>
<pre>
[Serializable]
public enum AVAssetExportSessionStatus {
	Unknown,
	Exporting,
	Completed,
	Failed,
	Cancelled
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAssetReaderStatus</h4>
<pre>
[Serializable]
public enum AVAssetReaderStatus {
	Unknown,
	Reading,
	Completed,
	Failed,
	Cancelled
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAssetTrack</h4>
<pre>
public class AVAssetTrack : MonoTouch.Foundation.NSObject {
	
	public AVAssetTrack ();
	public AVAssetTrack (MonoTouch.Foundation.NSCoder coder);
	public AVAssetTrack (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetTrack (IntPtr handle);
	
	public virtual bool HasMediaCharacteristic (string mediaCharacteristic);
	public virtual AVMetadataItem[] MetadataForFormat (string format);
	public virtual MonoTouch.CoreMedia.CMTime SamplePresentationTimeForTrackTime (MonoTouch.CoreMedia.CMTime trackTime);
	public virtual AVAssetTrackSegment SegmentForTrackTime (MonoTouch.CoreMedia.CMTime trackTime);
	
	public virtual AVAsset Asset {
		get;
	}
	public virtual string [] AvailableMetadataFormats {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVMetadataItem[] CommonMetadata {
		get;
	}
	public virtual bool Enabled {
		get;
	}
	public virtual float EstimatedDataRate {
		get;
	}
	public virtual string ExtendedLanguageTag {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] FormatDescriptionsAsObjects {
		get;
	}
	public virtual string LanguageCode {
		get;
	}
	public virtual string MediaType {
		get;
	}
	public virtual System.Drawing.SizeF NaturalSize {
		get;
	}
	public virtual int NaturalTimeScale {
		get;
	}
	public virtual float NominalFrameRate {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGAffineTransform PreferredTransform {
		get;
	}
	public virtual float PreferredVolume {
		get;
	}
	public virtual AVAssetTrackSegment[] Segments {
		get;
	}
	public virtual bool SelfContained {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
	}
	public virtual long TotalSampleDataLength {
		get;
	}
	public virtual int TrackID {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAssetTrackSegment</h4>
<pre>
public class AVAssetTrackSegment : MonoTouch.Foundation.NSObject {
	
	public AVAssetTrackSegment ();
	public AVAssetTrackSegment (MonoTouch.Foundation.NSCoder coder);
	public AVAssetTrackSegment (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetTrackSegment (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Empty {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeMapping TimeMapping {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading</h4>
<pre>
public abstract class AVAsynchronousKeyValueLoading : MonoTouch.Foundation.NSObject {
	
	public AVAsynchronousKeyValueLoading ();
	public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSCoder coder);
	public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSObjectFlag t);
	public AVAsynchronousKeyValueLoading (IntPtr handle);
	
	public abstract void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
	public abstract AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAudioMix</h4>
<pre>
public class AVAudioMix : MonoTouch.Foundation.NSObject {
	
	public AVAudioMix ();
	public AVAudioMix (MonoTouch.Foundation.NSCoder coder);
	public AVAudioMix (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioMix (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVAudioMixInputParameters[] InputParameters {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVAudioMixInputParameters</h4>
<pre>
public class AVAudioMixInputParameters : MonoTouch.Foundation.NSObject {
	
	public AVAudioMixInputParameters ();
	public AVAudioMixInputParameters (MonoTouch.Foundation.NSCoder coder);
	public AVAudioMixInputParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVAudioMixInputParameters (IntPtr handle);
	
	public virtual bool GetVolumeRamp (MonoTouch.CoreMedia.CMTime forTime, float startVolume, float endVolume, MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int TrackID {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioPlayer</h4>
<p>Removed:</p><pre>
 	public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSError error);
 	public AVAudioPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSError error);
 	public AVAudioPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSError error);
 	public virtual bool PlayAtTimetime (double time);
 	public virtual double DeviceCurrentTime {
 		get;
 	}
 	public virtual float Pan {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary Settings {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate</h4>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioRecorder</h4>
<p>Removed:</p><pre>
 	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
</pre>
<p>Added:</p><pre>
 	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate</h4>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioRecorder recorder, AVAudioSessionInterruptionFlags flags);
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioSession</h4>
<p>Added:</p><pre>
 	public bool SetActive (bool beActive, AVAudioSessionFlags flags, out MonoTouch.Foundation.NSError outError);
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioSessionDelegate</h4>
<p>Removed:</p><pre>
 	public virtual void CategoryChanged (string category);
 	public virtual void CurrentHardwareInputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareOutputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareSampleRateChanged (double sampleRate);
</pre>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioSessionInterruptionFlags flags);
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioSessionFlags</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVAudioSessionFlags
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum AVAudioSessionFlags {
 	NotifyOthersOnDeactivation
 }
</pre>
<h4>Type Changed: MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum AVAudioSessionInterruptionFlags {
 	ShouldResume
 }
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureAudioChannel</h4>
<pre>
public class AVCaptureAudioChannel : MonoTouch.Foundation.NSObject {
	
	public AVCaptureAudioChannel ();
	public AVCaptureAudioChannel (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAudioChannel (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAudioChannel (IntPtr handle);
	
	public virtual float AveragePowerLevel {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual float PeakHoldLevel {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutput</h4>
<pre>
public class AVCaptureAudioDataOutput : AVCaptureOutput {
	
	public AVCaptureAudioDataOutput ();
	public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAudioDataOutput (IntPtr handle);
	
	public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreFoundation.DispatchQueue SampleBufferCallbackQueue {
		get;
	}
	public virtual AVCaptureAudioDataOutputSampleBufferDelegate SampleBufferDelegate {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate</h4>
<pre>
public class AVCaptureAudioDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
	
	public AVCaptureAudioDataOutputSampleBufferDelegate ();
	public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAudioDataOutputSampleBufferDelegate (IntPtr handle);
	
	public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureCompletionHandler</h4>
<pre>
[Serializable]
public delegate void AVCaptureCompletionHandler (MonoTouch.CoreMedia.CMSampleBuffer imageDataSampleBuffer, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureConnection</h4>
<pre>
public class AVCaptureConnection : MonoTouch.Foundation.NSObject {
	
	public AVCaptureConnection ();
	public AVCaptureConnection (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureConnection (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureConnection (IntPtr handle);
	
	public virtual bool Active {
		get;
	}
	public virtual AVCaptureAudioChannel AudioChannels {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Enabled {
		get;
		set;
	}
	public virtual AVCaptureInputPort[] inputPorts {
		get;
	}
	public virtual AVCaptureOutput Output {
		get;
	}
	public virtual bool SupportsVideoMirroring {
		get;
	}
	public virtual bool SupportsVideoOrientation {
		get;
	}
	public virtual bool VideoMirrored {
		get;
		set;
	}
	public virtual AVCaptureVideoOrientation VideoOrientation {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureDevice</h4>
<pre>
public class AVCaptureDevice : MonoTouch.Foundation.NSObject {
	
	public AVCaptureDevice ();
	public AVCaptureDevice (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureDevice (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureDevice (IntPtr handle);
	
	public static AVCaptureDevice DefaultDeviceWithMediaType (string mediaType);
	public static AVCaptureDevice[] DevicesWithMediaType (string mediaType);
	public static AVCaptureDevice DeviceWithUniqueID (string deviceUniqueID);
	public virtual bool HasMediaType (string mediaType);
	public virtual bool IsFlashModeSupported (AVCaptureFlashMode flashMode);
	public virtual bool IsTorchModeSupported (AVCaptureTorchMode torchMode);
	public virtual bool LockForConfiguration (IntPtr ptrToHandleToError);
	public virtual bool SupportsAVCaptureSessionPreset (string preset);
	public virtual void UnlockForConfiguration ();
	
	public static AVCaptureDevice[] Devices {
		get;
	}
	public virtual bool AdjustingExposure {
		get;
	}
	public virtual bool AdjustingFocus {
		get;
	}
	public virtual bool AdjustingWhiteBalance {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Connected {
		get;
	}
	public virtual AVCaptureExposureMode ExposureMode {
		get;
		set;
	}
	public virtual System.Drawing.PointF ExposurePointOfInterest {
		get;
		set;
	}
	public virtual bool ExposurePointOfInterestSupported {
		get;
	}
	public virtual AVCaptureFlashMode FlashMode {
		get;
		set;
	}
	public virtual AVCaptureFocusMode FocusMode {
		get;
		set;
	}
	public virtual System.Drawing.PointF FocusPointOfInterest {
		get;
		set;
	}
	public virtual bool FocusPointOfInterestSupported {
		get;
	}
	public virtual string LocalizedName {
		get;
	}
	public virtual string ModelID {
		get;
	}
	public virtual AVCaptureDevicePosition Position {
		get;
	}
	public virtual AVCaptureTorchMode TorchMode {
		get;
		set;
	}
	public virtual string UniqueID {
		get;
	}
	public virtual AVCaptureWhiteBalanceMode WhiteBalanceMode {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureDeviceInput</h4>
<pre>
public class AVCaptureDeviceInput : AVCaptureInput {
	
	public AVCaptureDeviceInput ();
	public AVCaptureDeviceInput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureDeviceInput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureDeviceInput (IntPtr handle);
	public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr ptrToHandleToError);
	
	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr ptrToHandleToError);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVCaptureDevice Device {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureDevicePosition</h4>
<pre>
[Serializable]
public enum AVCaptureDevicePosition {
	Back,
	Front
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureExposureMode</h4>
<pre>
[Serializable]
public enum AVCaptureExposureMode {
	Locked,
	AutoExpose,
	ContinuousAutoExposure
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureFileOutput</h4>
<pre>
public class AVCaptureFileOutput : AVCaptureOutput {
	
	public AVCaptureFileOutput ();
	public AVCaptureFileOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureFileOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureFileOutput (IntPtr handle);
	
	public virtual void StartRecordingToOutputFile (MonoTouch.Foundation.NSUrl outputFileUrl, AVCaptureFileOutputRecordingDelegate recordingDelegate);
	public virtual void StopRecording ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime MaxRecordedDuration {
		get;
		set;
	}
	public virtual long MaxRecordedFileSize {
		get;
		set;
	}
	public virtual long MinFreeDiskSpaceLimit {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSUrl OutputFileURL {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime RecordedDuration {
		get;
	}
	public virtual long RecordedFileSize {
		get;
	}
	public virtual bool Recording {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate</h4>
<pre>
public class AVCaptureFileOutputRecordingDelegate : MonoTouch.Foundation.NSObject {
	
	public AVCaptureFileOutputRecordingDelegate ();
	public AVCaptureFileOutputRecordingDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureFileOutputRecordingDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureFileOutputRecordingDelegate (IntPtr handle);
	
	public virtual void DidStartRecording (AVCaptureFileOutput captureOutput, MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections);
	public virtual void FinishedRecording (AVCaptureFileOutput captureOutput, MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections, MonoTouch.Foundation.NSError error);
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureFlashMode</h4>
<pre>
[Serializable]
public enum AVCaptureFlashMode {
	Off,
	On,
	Auto
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureFocusMode</h4>
<pre>
[Serializable]
public enum AVCaptureFocusMode {
	ModeLocked,
	ModeAutoFocus,
	ModeContinuousAutoFocus
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureInput</h4>
<pre>
public class AVCaptureInput : MonoTouch.Foundation.NSObject {
	
	public AVCaptureInput ();
	public AVCaptureInput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureInput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureInput (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVCaptureInputPort[] Ports {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureInputPort</h4>
<pre>
public class AVCaptureInputPort : MonoTouch.Foundation.NSObject {
	
	public AVCaptureInputPort ();
	public AVCaptureInputPort (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureInputPort (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureInputPort (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Enabled {
		get;
		set;
	}
	public virtual AVCaptureInput Input {
		get;
	}
	public virtual string MediaType {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureMovieFileOutput</h4>
<pre>
public class AVCaptureMovieFileOutput : AVCaptureFileOutput {
	
	public AVCaptureMovieFileOutput ();
	public AVCaptureMovieFileOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureMovieFileOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureMovieFileOutput (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVMetadataItem[] Metadata {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTime MovieFragmentInterval {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureOutput</h4>
<pre>
public class AVCaptureOutput : MonoTouch.Foundation.NSObject {
	
	public AVCaptureOutput ();
	public AVCaptureOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureOutput (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] Connections {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureSession</h4>
<pre>
public class AVCaptureSession : MonoTouch.Foundation.NSObject {
	
	public AVCaptureSession ();
	public AVCaptureSession (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureSession (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureSession (IntPtr handle);
	
	public virtual void AddInput (AVCaptureInput input);
	public virtual void AddOutput (AVCaptureOutput output);
	public virtual void BeginConfiguration ();
	public virtual bool CanAddInput (AVCaptureInput input);
	public virtual bool CanAddOutput (AVCaptureOutput output);
	public virtual bool CanSetSessionPreset (string preset);
	public virtual void CommitConfiguration ();
	public virtual void RemoveInput (AVCaptureInput input);
	public virtual void RemoveOutput (AVCaptureOutput output);
	public virtual void StartRunning ();
	public virtual void StopRunning ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVCaptureInput[] Inputs {
		get;
	}
	public virtual bool Interrupted {
		get;
	}
	public virtual AVCaptureOutput[] Outputs {
		get;
	}
	public virtual bool Running {
		get;
	}
	public virtual string SessionPreset {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h4>
<pre>
public class AVCaptureStillImageOutput : AVCaptureOutput {
	
	public AVCaptureStillImageOutput ();
	public AVCaptureStillImageOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureStillImageOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureStillImageOutput (IntPtr handle);
	
	public static MonoTouch.Foundation.NSData JpegStillToNSData (MonoTouch.CoreMedia.CMSampleBuffer buffer);
	public virtual void CaptureStillImageAsynchronously (AVCaptureConnection connection, AVCaptureCompletionHandler completionHandler);
	
	public virtual string [] AvailableImageDataCodecTypes {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] AvailableImageDataCVPixelFormatTypes {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary OutputSettings {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureTorchMode</h4>
<pre>
[Serializable]
public enum AVCaptureTorchMode {
	Off,
	On,
	Auto
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutput</h4>
<pre>
public class AVCaptureVideoDataOutput : AVCaptureOutput {
	
	public AVCaptureVideoDataOutput ();
	public AVCaptureVideoDataOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureVideoDataOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureVideoDataOutput (IntPtr handle);
	
	public virtual void SetSampleBufferDelegatequeue (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, IntPtr sampleBufferCallbackQueue);
	
	public virtual bool AlwaysDiscardsLateVideoFrames {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime MinFrameDuration {
		get;
		set;
	}
	public virtual IntPtr SampleBufferCallbackQueue {
		get;
	}
	public virtual AVCaptureVideoDataOutputSampleBufferDelegate SampleBufferDelegate {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate</h4>
<pre>
public class AVCaptureVideoDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
	
	public AVCaptureVideoDataOutputSampleBufferDelegate ();
	public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureVideoDataOutputSampleBufferDelegate (IntPtr handle);
	
	public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureVideoOrientation</h4>
<pre>
[Serializable]
public enum AVCaptureVideoOrientation {
	Portrait,
	PortraitUpsideDown,
	LandscapeLeft,
	LandscapeRight
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h4>
<pre>
public class AVCaptureVideoPreviewLayer : MonoTouch.CoreAnimation.CALayer {
	
	public AVCaptureVideoPreviewLayer ();
	public AVCaptureVideoPreviewLayer (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureVideoPreviewLayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureVideoPreviewLayer (IntPtr handle);
	public AVCaptureVideoPreviewLayer (AVCaptureSession session);
	
	public static AVCaptureVideoPreviewLayer FromSession (AVCaptureSession session);
	
	public virtual bool AutomaticallyAdjustsMirroring {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Mirrored {
		get;
		set;
	}
	public virtual bool MirroringSupported {
		get;
	}
	public virtual AVCaptureVideoOrientation Orientation {
		get;
		set;
	}
	public virtual bool OrientationSupported {
		get;
	}
	public virtual AVCaptureSession Session {
		get;
		set;
	}
	public virtual string VideoGravity {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCaptureWhiteBalanceMode</h4>
<pre>
[Serializable]
public enum AVCaptureWhiteBalanceMode {
	Locked,
	AutoWhiteBalance,
	ContinuousAutoWhiteBalance
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCompositionTrack</h4>
<pre>
public class AVCompositionTrack : AVAssetTrack {
	
	public AVCompositionTrack ();
	public AVCompositionTrack (MonoTouch.Foundation.NSCoder coder);
	public AVCompositionTrack (MonoTouch.Foundation.NSObjectFlag t);
	public AVCompositionTrack (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVCompositionTrackSegment[] Segments {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVCompositionTrackSegment</h4>
<pre>
public class AVCompositionTrackSegment : AVAssetTrackSegment {
	
	public AVCompositionTrackSegment ();
	public AVCompositionTrackSegment (MonoTouch.Foundation.NSCoder coder);
	public AVCompositionTrackSegment (MonoTouch.Foundation.NSObjectFlag t);
	public AVCompositionTrackSegment (IntPtr handle);
	public AVCompositionTrackSegment (MonoTouch.Foundation.NSUrl URL, int trackID, MonoTouch.CoreMedia.CMTimeRange sourceTimeRange, MonoTouch.CoreMedia.CMTimeRange targetTimeRange);
	public AVCompositionTrackSegment (MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public static IntPtr FromTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
	public static IntPtr FromUrl (MonoTouch.Foundation.NSUrl url, int trackID, MonoTouch.CoreMedia.CMTimeRange sourceTimeRange, MonoTouch.CoreMedia.CMTimeRange targetTimeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int SourceTrackID {
		get;
	}
	public virtual MonoTouch.Foundation.NSUrl SourceUrl {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVError</h4>
<pre>
[Serializable]
public enum AVError {
	Unknown,
	OutOfMemory,
	SessionNotRunning,
	DeviceAlreadyUsedByAnotherSession,
	NoDataCaptured,
	SessionConfigurationChanged,
	DiskFull,
	DeviceWasDisconnected,
	MediaChanged,
	MaximumDurationReached,
	MaximumFileSizeReached,
	MediaDiscontinuity,
	MaximumNumberOfSamplesForFileFormatReached,
	DeviceNotConnected,
	DeviceInUseByAnotherApplication,
	DeviceLockedForConfigurationByAnotherProcess,
	SessionWasInterrupted,
	DecodeFailed,
	ExportFailed,
	FileAlreadyExists,
	InvalidSourceMedia,
	CompositionTrackSegmentsNotContiguous,
	ContentIsProtected,
	FailedToParse,
	FormatNotRecognized,
	InvalidCompositionTrackSegmentDuration,
	InvalidCompositionTrackSegmentSourceStartTime,
	InvalidCompositionTrackSegmentSourceDuration,
	MaximumStillImageCaptureRequestsExceeded,
	NoImageAtTime,
	MediaServicesWereReset
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVErrorHandler</h4>
<pre>
[Serializable]
public delegate void AVErrorHandler (MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVFileType</h4>
<pre>
public class AVFileType {
	
	public AVFileType ();
	
	public static MonoTouch.Foundation.NSString Aifc {
		get;
	}
	public static MonoTouch.Foundation.NSString Aiff {
		get;
	}
	public static MonoTouch.Foundation.NSString Amr {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleM4A {
		get;
	}
	public static MonoTouch.Foundation.NSString AppleM4V {
		get;
	}
	public static MonoTouch.Foundation.NSString CoreAudioFormat {
		get;
	}
	public static MonoTouch.Foundation.NSString Mpeg4 {
		get;
	}
	public static MonoTouch.Foundation.NSString QuickTimeMovie {
		get;
	}
	public static MonoTouch.Foundation.NSString ThreeGpp {
		get;
	}
	public static MonoTouch.Foundation.NSString Wave {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVKeyValueStatus</h4>
<pre>
[Serializable]
public enum AVKeyValueStatus {
	Unknown,
	Loading,
	Loaded,
	Failed,
	Cancelled
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMediaCharacteristic</h4>
<pre>
public class AVMediaCharacteristic {
	
	public AVMediaCharacteristic ();
	
	public static MonoTouch.Foundation.NSString Audible {
		get;
	}
	public static MonoTouch.Foundation.NSString FrameBased {
		get;
	}
	public static MonoTouch.Foundation.NSString Legible {
		get;
	}
	public static MonoTouch.Foundation.NSString Visual {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMediaType</h4>
<pre>
public class AVMediaType {
	
	public AVMediaType ();
	
	public static MonoTouch.Foundation.NSString Audio {
		get;
	}
	public static MonoTouch.Foundation.NSString ClosedCaption {
		get;
	}
	public static MonoTouch.Foundation.NSString Muxed {
		get;
	}
	public static MonoTouch.Foundation.NSString Subtitle {
		get;
	}
	public static MonoTouch.Foundation.NSString Text {
		get;
	}
	public static MonoTouch.Foundation.NSString Timecode {
		get;
	}
	public static MonoTouch.Foundation.NSString TimedMetadata {
		get;
	}
	public static MonoTouch.Foundation.NSString Video {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMetadataItem</h4>
<pre>
public class AVMetadataItem : MonoTouch.Foundation.NSObject {
	
	public AVMetadataItem ();
	public AVMetadataItem (MonoTouch.Foundation.NSCoder coder);
	public AVMetadataItem (MonoTouch.Foundation.NSObjectFlag t);
	public AVMetadataItem (IntPtr handle);
	
	public static AVMetadataItem[] FilterWithKey (AVMetadataItem[] array, MonoTouch.Foundation.NSObject key, string keySpace);
	public static AVMetadataItem[] FilterWithLocale (AVMetadataItem[] arrayToFilter, MonoTouch.Foundation.NSLocale locale);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string CommonKey {
		get;
	}
	public virtual MonoTouch.Foundation.NSData DataValue {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate DateValue {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary ExtraAttributes {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject Key {
		get;
	}
	public virtual string KeySpace {
		get;
	}
	public virtual MonoTouch.Foundation.NSLocale Locale {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber NumberValue {
		get;
	}
	public virtual string StringValue {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime Time {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject Value {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableAudioMix</h4>
<pre>
public class AVMutableAudioMix : AVAudioMix {
	
	public AVMutableAudioMix ();
	public AVMutableAudioMix (MonoTouch.Foundation.NSCoder coder);
	public AVMutableAudioMix (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableAudioMix (IntPtr handle);
	
	public static AVMutableAudioMix Create ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVAudioMixInputParameters[] InputParameters {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters</h4>
<pre>
public class AVMutableAudioMixInputParameters : AVAudioMixInputParameters {
	
	public AVMutableAudioMixInputParameters ();
	public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSCoder coder);
	public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableAudioMixInputParameters (IntPtr handle);
	
	public static AVMutableAudioMixInputParameters Create ();
	public static AVMutableAudioMixInputParameters FromTrack (AVAssetTrack track);
	public virtual void SetVolume (float volume, MonoTouch.CoreMedia.CMTime atTime);
	public virtual void SetVolumeRamp (float startVolume, float endVolume, MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int TrackID {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableCompositionTrack</h4>
<pre>
public class AVMutableCompositionTrack : AVCompositionTrack {
	
	public AVMutableCompositionTrack ();
	public AVMutableCompositionTrack (MonoTouch.Foundation.NSCoder coder);
	public AVMutableCompositionTrack (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableCompositionTrack (IntPtr handle);
	
	public virtual void InsertEmptyTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
	public virtual void RemoveTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
	public virtual void ScaleTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange, MonoTouch.CoreMedia.CMTime duration);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string ExtendedLanguageTag {
		get;
		set;
	}
	public virtual string LanguageCode {
		get;
		set;
	}
	public virtual int NaturalTimeScale {
		get;
		set;
	}
	public virtual MonoTouch.CoreGraphics.CGAffineTransform PreferredTransform {
		get;
		set;
	}
	public virtual float PreferredVolume {
		get;
		set;
	}
	public virtual AVCompositionTrackSegment[] Segments {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableMetadataItem</h4>
<pre>
public class AVMutableMetadataItem : AVMetadataItem {
	
	public AVMutableMetadataItem ();
	public AVMutableMetadataItem (MonoTouch.Foundation.NSCoder coder);
	public AVMutableMetadataItem (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableMetadataItem (IntPtr handle);
	
	public static AVMutableMetadataItem Create ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary ExtraAttributes {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject Key {
		get;
	}
	public virtual string KeySpace {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSLocale Locale {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTime Time {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject Value {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableVideoComposition</h4>
<pre>
public class AVMutableVideoComposition : AVVideoComposition {
	
	public AVMutableVideoComposition ();
	public AVMutableVideoComposition (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoComposition (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoComposition (IntPtr handle);
	
	public static AVMutableVideoComposition Create ();
	
	public virtual AVVideoCompositionCoreAnimationTool AnimationTool {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime FrameDuration {
		get;
		set;
	}
	public virtual AVVideoCompositionInstruction[] Instructions {
		get;
		set;
	}
	public virtual float RenderScale {
		get;
	}
	public virtual System.Drawing.SizeF RenderSize {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction</h4>
<pre>
public class AVMutableVideoCompositionInstruction : AVVideoCompositionInstruction {
	
	public AVMutableVideoCompositionInstruction ();
	public AVMutableVideoCompositionInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoCompositionInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoCompositionInstruction (IntPtr handle);
	
	public static AVVideoCompositionInstruction Create ();
	
	public virtual MonoTouch.CoreGraphics.CGColor BackgroundColor {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction</h4>
<pre>
public class AVMutableVideoCompositionLayerInstruction : AVVideoCompositionLayerInstruction {
	
	public AVMutableVideoCompositionLayerInstruction ();
	public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoCompositionLayerInstruction (IntPtr handle);
	
	public static AVMutableVideoCompositionLayerInstruction Create ();
	public static AVMutableVideoCompositionLayerInstruction FromAssetTrack (AVAssetTrack track);
	public virtual void SetOpacity (float opacity, MonoTouch.CoreMedia.CMTime time);
	public virtual void SetOpacityRamp (float startOpacity, float endOpacity, MonoTouch.CoreMedia.CMTimeRange timeRange);
	public virtual void SetTransform (MonoTouch.CoreGraphics.CGAffineTransform transform, MonoTouch.CoreMedia.CMTime atTime);
	public virtual void SetTransformRamp (MonoTouch.CoreGraphics.CGAffineTransform startTransform, MonoTouch.CoreGraphics.CGAffineTransform endTransform, MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int TrackID {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayer</h4>
<pre>
public class AVPlayer : MonoTouch.Foundation.NSObject {
	
	public AVPlayer ();
	public AVPlayer (MonoTouch.Foundation.NSCoder coder);
	public AVPlayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayer (IntPtr handle);
	public AVPlayer (MonoTouch.Foundation.NSUrl URL);
	public AVPlayer (AVPlayerItem item);
	
	public static AVPlayer FromPlayerItem (AVPlayerItem item);
	public static AVPlayer FromUrl (MonoTouch.Foundation.NSUrl URL);
	public virtual MonoTouch.Foundation.NSObject AddBoundaryTimeObserver (MonoTouch.Foundation.NSValue[] times, MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSAction handler);
	public virtual MonoTouch.Foundation.NSObject AddPeriodicTimeObserver (MonoTouch.CoreMedia.CMTime interval, MonoTouch.CoreFoundation.DispatchQueue queue, AVTimeHandler handler);
	public virtual void Pause ();
	public virtual void Play ();
	public virtual void RemoveTimeObserver (MonoTouch.Foundation.NSObject observer);
	public virtual void ReplaceCurrentItemWithPlayerItem (AVPlayerItem item);
	public virtual void Seek (MonoTouch.CoreMedia.CMTime toTime);
	public virtual void Seek (MonoTouch.CoreMedia.CMTime toTime, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
	
	public virtual AVPlayerActionAtItemEnd ActionAtItemEnd {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool ClosedCaptionDisplayEnabled {
		get;
		set;
	}
	public virtual AVPlayerItem CurrentItem {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime CurrentTime {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSError Error {
		get;
	}
	public virtual float Rate {
		get;
		set;
	}
	public virtual AVPlayerStatus Status {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerActionAtItemEnd</h4>
<pre>
[Serializable]
public enum AVPlayerActionAtItemEnd {
	Pause,
	None
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerItem</h4>
<pre>
public class AVPlayerItem : MonoTouch.Foundation.NSObject {
	
	public AVPlayerItem ();
	public AVPlayerItem (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItem (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItem (IntPtr handle);
	public AVPlayerItem (MonoTouch.Foundation.NSUrl URL);
	public AVPlayerItem (AVAsset asset);
	
	public static AVPlayerItem FromAsset (AVAsset asset);
	public static AVPlayerItem FromUrl (MonoTouch.Foundation.NSUrl URL);
	public virtual bool Seek (MonoTouch.CoreMedia.CMTime time);
	public virtual bool Seek (MonoTouch.Foundation.NSDate date);
	public virtual bool SeekToDate (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
	public virtual void StepByCount (int stepCount);
	
	public virtual AVAsset Asset {
		get;
	}
	public virtual AVAudioMix AudioMix {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime CurrentTime {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSError Error {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime ForwardPlaybackEndTime {
		get;
		set;
	}
	public virtual bool PlaybackBufferEmpty {
		get;
	}
	public virtual bool PlaybackBufferFull {
		get;
	}
	public virtual bool PlaybackLikelyToKeepUp {
		get;
	}
	public virtual System.Drawing.SizeF PresentationSize {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime ReversePlaybackEndTime {
		get;
		set;
	}
	public virtual AVPlayerItemStatus Status {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] TimedMetadata {
		get;
	}
	public virtual AVPlayerItem[] Tracks {
		get;
	}
	public virtual AVVideoComposition VideoComposition {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerItemStatus</h4>
<pre>
[Serializable]
public enum AVPlayerItemStatus {
	Unknown,
	ReadyToPlay,
	Failed
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerItemTrack</h4>
<pre>
public class AVPlayerItemTrack : MonoTouch.Foundation.NSObject {
	
	public AVPlayerItemTrack ();
	public AVPlayerItemTrack (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemTrack (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemTrack (IntPtr handle);
	
	public virtual AVAssetTrack AssetTrack {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Enabled {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerLayer</h4>
<pre>
public class AVPlayerLayer : MonoTouch.CoreAnimation.CALayer {
	
	public AVPlayerLayer ();
	public AVPlayerLayer (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerLayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerLayer (IntPtr handle);
	
	public static AVPlayerLayer FromPlayer (AVPlayer player);
	
	public static MonoTouch.Foundation.NSString GravityResize {
		get;
	}
	public static MonoTouch.Foundation.NSString GravityResizeAspect {
		get;
	}
	public static MonoTouch.Foundation.NSString GravityResizeAspectFill {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVPlayer Player {
		get;
		set;
	}
	public virtual bool ReadyForDisplay {
		get;
	}
	public virtual string VideoGravity {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVPlayerStatus</h4>
<pre>
[Serializable]
public enum AVPlayerStatus {
	Unknown,
	ReadyToPlay,
	Failed
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVTimeHandler</h4>
<pre>
[Serializable]
public delegate void AVTimeHandler (MonoTouch.CoreMedia.CMTime time);
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVUrlAsset</h4>
<pre>
public class AVUrlAsset : AVAsset {
	
	public AVUrlAsset ();
	public AVUrlAsset (MonoTouch.Foundation.NSCoder coder);
	public AVUrlAsset (MonoTouch.Foundation.NSObjectFlag t);
	public AVUrlAsset (IntPtr handle);
	public AVUrlAsset (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
	
	public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
	public virtual AVAssetTrack CompatibleTrack (AVCompositionTrack forCompositionTrack);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSUrl Url {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVVideo</h4>
<pre>
public class AVVideo {
	
	public AVVideo ();
	
	public static MonoTouch.Foundation.NSString AverageBitRateKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureHeightKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureHorizontalOffsetKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureVerticalOffsetKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CleanApertureWidthKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecH264 {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecJPEG {
		get;
	}
	public static MonoTouch.Foundation.NSString CodecKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CompressionPropertiesKey {
		get;
	}
	public static MonoTouch.Foundation.NSString HeightKey {
		get;
	}
	public static MonoTouch.Foundation.NSString MaxKeyFrameIntervalKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioHorizontalSpacingKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioKey {
		get;
	}
	public static MonoTouch.Foundation.NSString PixelAspectRatioVerticalSpacingKey {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Baseline30 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Baseline31 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Main30 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelH264Main31 {
		get;
	}
	public static MonoTouch.Foundation.NSString ProfileLevelKey {
		get;
	}
	public static MonoTouch.Foundation.NSString WidthKey {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVVideoComposition</h4>
<pre>
public class AVVideoComposition : MonoTouch.Foundation.NSObject {
	
	public AVVideoComposition ();
	public AVVideoComposition (MonoTouch.Foundation.NSCoder coder);
	public AVVideoComposition (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoComposition (IntPtr handle);
	
	public virtual AVVideoCompositionCoreAnimationTool AnimationTool {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTime FrameDuration {
		get;
	}
	public virtual AVVideoCompositionInstruction[] Instructions {
		get;
	}
	public virtual float RenderScale {
		get;
		set;
	}
	public virtual System.Drawing.SizeF RenderSize {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVVideoCompositionCoreAnimationTool</h4>
<pre>
public class AVVideoCompositionCoreAnimationTool : MonoTouch.Foundation.NSObject {
	
	public AVVideoCompositionCoreAnimationTool ();
	public AVVideoCompositionCoreAnimationTool (MonoTouch.Foundation.NSCoder coder);
	public AVVideoCompositionCoreAnimationTool (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoCompositionCoreAnimationTool (IntPtr handle);
	
	public static AVVideoCompositionCoreAnimationTool FromLayer (MonoTouch.CoreAnimation.CALayer videoLayer, MonoTouch.CoreAnimation.CALayer animationLayer);
	public static AVVideoCompositionCoreAnimationTool FromLayer (MonoTouch.CoreAnimation.CALayer layer, int trackID);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVVideoCompositionInstruction</h4>
<pre>
public class AVVideoCompositionInstruction : MonoTouch.Foundation.NSObject {
	
	public AVVideoCompositionInstruction ();
	public AVVideoCompositionInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVVideoCompositionInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoCompositionInstruction (IntPtr handle);
	
	public virtual MonoTouch.CoreGraphics.CGColor BackgroundColor {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool EnablePostProcessing {
		get;
	}
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction</h4>
<pre>
public class AVVideoCompositionLayerInstruction : MonoTouch.Foundation.NSObject {
	
	public AVVideoCompositionLayerInstruction ();
	public AVVideoCompositionLayerInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVVideoCompositionLayerInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVVideoCompositionLayerInstruction (IntPtr handle);
	
	public virtual bool GetOpacityRamp (MonoTouch.CoreMedia.CMTime time, float startOpacity, float endOpacity, MonoTouch.CoreMedia.CMTimeRange timeRange);
	public virtual bool GetTransformRamp (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreGraphics.CGAffineTransform startTransform, MonoTouch.CoreGraphics.CGAffineTransform endTransform, MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int TrackID {
		get;
	}
}
</pre>
<h3>Namespace: MonoTouch.AddressBookUI</h3>
<h4>Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController</h4>
<p>Removed:</p><pre>
 	public virtual IntPtr _AddressBook {
 		get;
 		set;
 	}
 	public virtual IntPtr _DisplayedPerson {
 		get;
 		set;
 	}
 	public virtual IntPtr _ParentGroup {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController</h4>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSNumber[] _DisplayedProperties {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.AddressBookUI.ABPersonViewController</h4>
<p>Removed:</p><pre>
 	public virtual IntPtr _AddressBook {
 		get;
 		set;
 	}
 	public virtual IntPtr _DisplayedPerson {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSNumber[] _DisplayedProperties {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController</h4>
<p>Removed:</p><pre>
 	public virtual IntPtr _AddressBook {
 		get;
 		set;
 	}
 	public virtual IntPtr _DisplayedPerson {
 		get;
 		set;
 	}
</pre>
<h3>Namespace: MonoTouch.AudioToolbox</h3>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayout</h4>
<p>Removed:</p><pre>
 	public int Tag;
</pre>
<p>Added:</p><pre>
 	public int Tag {
 		get;
 		set;
 	}
 	
 	public AudioChannelLayoutTag AudioTag;
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayoutTag</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.AudioToolbox.AudioChannelLayoutTag
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum AudioChannelLayoutTag {
 	UseChannelDescriptions,
 	UseChannelBitmap,
 	Mono,
 	Stereo,
 	StereoHeadphones,
 	MatrixStereo,
 	MidSide,
 	XY,
 	Binaural,
 	Ambisonic_B_Format,
 	Quadraphonic,
 	Pentagonal,
 	Hexagonal,
 	Octagonal,
 	Cube,
 	MPEG_1_0,
 	MPEG_2_0,
 	MPEG_3_0_A,
 	MPEG_3_0_B,
 	MPEG_4_0_A,
 	MPEG_4_0_B,
 	MPEG_5_0_A,
 	MPEG_5_0_B,
 	MPEG_5_0_C,
 	MPEG_5_0_D,
 	MPEG_5_1_A,
 	MPEG_5_1_B,
 	MPEG_5_1_C,
 	MPEG_5_1_D,
 	MPEG_6_1_A,
 	MPEG_7_1_A,
 	MPEG_7_1_B,
 	MPEG_7_1_C,
 	Emagic_Default_7_1,
 	SMPTE_DTV,
 	ITU_1_0,
 	ITU_2_0,
 	ITU_2_1,
 	ITU_2_2,
 	ITU_3_0,
 	ITU_3_1,
 	ITU_3_2,
 	ITU_3_2_1,
 	ITU_3_4_1,
 	DVD_0,
 	DVD_1,
 	DVD_2,
 	DVD_3,
 	DVD_4,
 	DVD_5,
 	DVD_6,
 	DVD_7,
 	DVD_8,
 	DVD_9,
 	DVD_10,
 	DVD_11,
 	DVD_12,
 	DVD_13,
 	DVD_14,
 	DVD_15,
 	DVD_16,
 	DVD_17,
 	DVD_18,
 	DVD_19,
 	DVD_20,
 	AudioUnit_4,
 	AudioUnit_5,
 	AudioUnit_6,
 	AudioUnit_8,
 	AudioUnit_5_0,
 	AudioUnit_6_0,
 	AudioUnit_7_0,
 	AudioUnit_7_0_Front,
 	AudioUnit_5_1,
 	AudioUnit_6_1,
 	AudioUnit_7_1,
 	AudioUnit_7_1_Front,
 	AAC_3_0,
 	AAC_Quadraphonic,
 	AAC_4_0,
 	AAC_5_0,
 	AAC_5_1,
 	AAC_6_0,
 	AAC_6_1,
 	AAC_7_0,
 	AAC_7_1,
 	AAC_Octagonal,
 	TMH_10_2_std,
 	TMH_10_2_full,
 	AC3_1_0_1,
 	AC3_3_0,
 	AC3_3_1,
 	AC3_3_0_1,
 	AC3_2_1_1,
 	AC3_3_1_1,
 	EAC_6_0_A,
 	EAC_7_0_A,
 	EAC3_6_1_A,
 	EAC3_6_1_B,
 	EAC3_6_1_C,
 	EAC3_7_1_A,
 	EAC3_7_1_B,
 	EAC3_7_1_C,
 	EAC3_7_1_D,
 	EAC3_7_1_E,
 	EAC3_7_1_F,
 	EAC3_7_1_G,
 	EAC3_7_1_H,
 	DTS_3_1,
 	DTS_4_1,
 	DTS_6_0_A,
 	DTS_6_0_B,
 	DTS_6_0_C,
 	DTS_6_1_A,
 	DTS_6_1_B,
 	DTS_6_1_C,
 	DTS_7_0,
 	DTS_7_1,
 	DTS_8_0_A,
 	DTS_8_0_B,
 	DTS_8_1_A,
 	DTS_8_1_B,
 	DTS_6_1_D,
 	DiscreteInOrder,
 	Unknown
 }
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioFormatType</h4>
<p>Removed:</p><pre>
 	AES3
</pre>
<p>Added:</p><pre>
 	AES3,
 	MPEG4AAC_ELD
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioQueue</h4>
<p>Added:</p><pre>
 	public AudioTimeStamp GetNearestStartTime (AudioTimeStamp requestedStartTime);
 	public AudioTimeStamp TranslateTime (AudioTimeStamp timeToTranslate);
 	public AudioTimeStamp CurrentTime {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioQueueParameter</h4>
<p>Removed:</p><pre>
 	Volume
</pre>
<p>Added:</p><pre>
 	Volume,
 	Pan,
 	VolumeRampTime
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioSession</h4>
<p>Added:</p><pre>
 	public static AudioSessionInterruptionType InterruptionType {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioSessionInterruptionType</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.AudioToolbox.AudioSessionInterruptionType
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum AudioSessionInterruptionType {
 	ShouldResume,
 	ShouldNotResume
 }
</pre>
<h4>Type Changed: MonoTouch.AudioToolbox.AudioSessionProperty</h4>
<p>Removed:</p><pre>
 	OverrideCategoryMixWithOthers
</pre>
<p>Added:</p><pre>
 	OverrideCategoryMixWithOthers,
 	InterruptionType
</pre>
<h3>Namespace: MonoTouch.CoreAnimation</h3>
<h4>Type Changed: MonoTouch.CoreAnimation.CAAnimation</h4>
<p>Removed:</p><pre>
 	public virtual CAAnimation CreateAnimation ();
 	public virtual double CFTimeInterval {
</pre>
<p>Added:</p><pre>
 	public static CAAnimation CreateAnimation ();
 	public virtual bool ShouldArchiveValueForKey (string key);
 	public static MonoTouch.Foundation.NSString TransitionFade {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionFromBottom {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionFromLeft {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionFromRight {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionFromTop {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionMoveIn {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionPush {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TransitionReveal {
 		get;
 	}
 	public virtual double BeginTime {
 		get;
 		set;
 	}
 	public double CFTimeInterval {
 	
 	public event EventHandler AnimationStarted;
 	public event EventHandler&lt;CAAnimationStateEventArgs&gt; AnimationStopped;
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CAAnimationGroup</h4>
<p>Added:</p><pre>
 	public static CAAnimationGroup CreateAnimation ();
 	
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CAAnimationStateEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreAnimation.CAAnimationStateEventArgs
</pre>
<p>Added:</p><pre>
 public class CAAnimationStateEventArgs : EventArgs {
 	
 	public CAAnimationStateEventArgs (bool finished);
 	
 	public bool Finished {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CABasicAnimation</h4>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSNumber By {
 	public virtual MonoTouch.Foundation.NSNumber From {
 	public virtual MonoTouch.Foundation.NSNumber To {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject By {
 	public virtual MonoTouch.Foundation.NSObject From {
 	public virtual MonoTouch.Foundation.NSObject To {
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CAGradientLayer</h4>
<p>Removed:</p><pre>
 	public virtual IntPtr _Colors {
 		set;
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString GradientLayerAxial {
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation</h4>
<p>Removed:</p><pre>
 	public virtual IntPtr _Path {
 		get;
 		set;
 	}
 	public virtual string rotationMode {
 	public virtual MonoTouch.Foundation.NSNumber[] Values {
</pre>
<p>Added:</p><pre>
 	public static CAPropertyAnimation FromKeyPath (string path);
 	
 	public virtual string RotationMode {
 	public virtual MonoTouch.Foundation.NSObject[] Values {
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CALayer</h4>
<p>Removed:</p><pre>
 	public CALayer (CALayer other);
 	public virtual double CFTimeInterval {
 	
 	public static readonly MonoTouch.Foundation.NSString GravityCenter;
 	public static readonly MonoTouch.Foundation.NSString GravityTop;
 	public static readonly MonoTouch.Foundation.NSString GravityBottom;
 	public static readonly MonoTouch.Foundation.NSString GravityLeft;
 	public static readonly MonoTouch.Foundation.NSString GravityRight;
 	public static readonly MonoTouch.Foundation.NSString GravityTopLeft;
 	public static readonly MonoTouch.Foundation.NSString GravityTopRight;
 	public static readonly MonoTouch.Foundation.NSString GravityBottomLeft;
 	public static readonly MonoTouch.Foundation.NSString GravityBottomRight;
 	public static readonly MonoTouch.Foundation.NSString GravityResize;
 	public static readonly MonoTouch.Foundation.NSString GravityResizeAspect;
 	public static readonly MonoTouch.Foundation.NSString GravityResizeAspectFill;
 	public static readonly MonoTouch.Foundation.NSString FilterNearest;
 	public static readonly MonoTouch.Foundation.NSString FilterLinear;
 	public static readonly MonoTouch.Foundation.NSString FilterTrilinear;
 	public static readonly MonoTouch.Foundation.NSString OnOrderIn;
 	public static readonly MonoTouch.Foundation.NSString OnOrderOut;
</pre>
<p>Added:</p><pre>
 	public CALayer (CALayer other);
 	public virtual void ScrollPoint (System.Drawing.PointF p);
 	public virtual void ScrollRectToVisible (System.Drawing.RectangleF r);
 	public static MonoTouch.Foundation.NSString FilterLinear {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FilterNearest {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FilterTrilinear {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityBottom {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityBottomLeft {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityBottomRight {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityCenter {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityLeft {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityResize {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityResizeAspect {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityResizeAspectFill {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityRight {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityTop {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityTopLeft {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GravityTopRight {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OnOrderIn {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OnOrderOut {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Transition {
 		get;
 	}
 	public virtual double BeginTime {
 		get;
 		set;
 	}
 	public double CFTimeInterval {
 	public virtual System.Drawing.RectangleF VisibleRect {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.CoreAnimation.CAScrollLayer</h4>
<pre>
public class CAScrollLayer : CALayer {
	
	public CAScrollLayer ();
	public CAScrollLayer (MonoTouch.Foundation.NSCoder coder);
	public CAScrollLayer (MonoTouch.Foundation.NSObjectFlag t);
	public CAScrollLayer (IntPtr handle);
	
	public virtual void ScrollToPoint (System.Drawing.PointF p);
	public virtual void ScrollToRect (System.Drawing.RectangleF r);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string scrollMode {
		get;
		set;
	}
}
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CATextLayer</h4>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AlignmentCenter {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlignmentJustified {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlignmentLeft {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlignmentNatural {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlignmentRight {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TruncantionEnd {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TruncantionMiddle {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TruncantionStart {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TruncationNone {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.CoreAnimation.CATiledLayer</h4>
<pre>
public class CATiledLayer : CALayer {
	
	public CATiledLayer ();
	public CATiledLayer (MonoTouch.Foundation.NSCoder coder);
	public CATiledLayer (MonoTouch.Foundation.NSObjectFlag t);
	public CATiledLayer (IntPtr handle);
	
	public static double FadeDuration {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int LevelsOfDetail {
		get;
		set;
	}
	public virtual int LevelsOfDetailBias {
		get;
		set;
	}
	public virtual System.Drawing.SizeF TileSize {
		get;
		set;
	}
}
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CATransaction</h4>
<p>Removed:</p><pre>
 	public static void SetValueForKey (MonoTouch.Foundation.NSObject anObject, string key);
 	public static MonoTouch.Foundation.NSObject ValueForKey (string key);
</pre>
<p>Added:</p><pre>
 	public static void SetValueForKey (MonoTouch.Foundation.NSObject anObject, MonoTouch.Foundation.NSString key);
 	public static MonoTouch.Foundation.NSObject ValueForKey (MonoTouch.Foundation.NSString key);
 	public static MonoTouch.Foundation.NSString AnimationDurationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSAction CompletionBlock {
 		set;
 	}
 	public static MonoTouch.Foundation.NSString CompletionBlockKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DisableActionsKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimingFunctionKey {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CATransform3D</h4>
<p>Added:</p><pre>
 	public override string ToString ();
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CATransition</h4>
<p>Added:</p><pre>
 	public static CATransition CreateAnimation ();
 	
</pre>
<h4>Type Changed: MonoTouch.CoreAnimation.CAValueFunction</h4>
<p>Removed:</p><pre>
 	
 	public static readonly MonoTouch.Foundation.NSString RotateX;
 	public static readonly MonoTouch.Foundation.NSString RotateY;
 	public static readonly MonoTouch.Foundation.NSString RotateZ;
 	public static readonly MonoTouch.Foundation.NSString Scale;
 	public static readonly MonoTouch.Foundation.NSString ScaleX;
 	public static readonly MonoTouch.Foundation.NSString ScaleY;
 	public static readonly MonoTouch.Foundation.NSString ScaleZ;
 	public static readonly MonoTouch.Foundation.NSString Translate;
 	public static readonly MonoTouch.Foundation.NSString TranslateX;
 	public static readonly MonoTouch.Foundation.NSString TranslateY;
 	public static readonly MonoTouch.Foundation.NSString TranslateZ;
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString RotateX {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RotateY {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RotateZ {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Scale {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ScaleX {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ScaleY {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ScaleZ {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString Translate {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TranslateX {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TranslateY {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TranslateZ {
 		get;
 	}
</pre>
<h3>Namespace: MonoTouch.CoreFoundation</h3>
<h4>Type Changed: MonoTouch.CoreFoundation.CFRunLoop</h4>
<p>Added:</p><pre>
 	public void Stop ();
</pre>
<h4>New Type: MonoTouch.CoreFoundation.DispatchObject</h4>
<pre>
public class DispatchObject : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public override bool Equals (object other);
	protected override void Finalize ();
	public override int GetHashCode ();
	public void Resume ();
	public void Suspend ();
	
	public static bool operator == (DispatchObject a, DispatchObject b);
	public static bool operator != (DispatchObject a, DispatchObject b);
	
	public IntPtr Context {
		get;
		set;
	}
	public IntPtr Handle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreFoundation.DispatchQueue</h4>
<pre>
public class DispatchQueue : DispatchObject {
	
	public DispatchQueue (IntPtr handle);
	public DispatchQueue (string label);
	
	public static DispatchQueue GetGlobalQueue (DispatchQueuePriority priority);
	public void DispatchAsync (MonoTouch.Foundation.NSAction action);
	public void DispatchSync (MonoTouch.Foundation.NSAction action);
	
	public static DispatchQueue CurrentQueue {
		get;
	}
	public static DispatchQueue DefaultGlobalQueue {
		get;
	}
	public static DispatchQueue MainQueue {
		get;
	}
	public string Label {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreFoundation.DispatchQueuePriority</h4>
<pre>
[Serializable]
public enum DispatchQueuePriority {
	High,
	Default,
	Low
}
</pre>
<h3>Namespace: MonoTouch.CoreGraphics</h3>
<h4>Type Changed: MonoTouch.CoreGraphics.CGContext</h4>
<p>Added:</p><pre>
 	public CGPath CopyPath ();
 	public void DrawLayer (CGLayer layer, System.Drawing.PointF point);
 	public void DrawLayer (CGLayer layer, System.Drawing.RectangleF rect);
 	public void SetAllowsFontSmoothing (bool allows);
 	public void SetAllowsFontSubpixelQuantization (bool allows);
 	public void SetAllowsSubpixelPositioning (bool allows);
 	public void SetShouldSubpixelPositionFonts (bool shouldSubpixelPositionFonts);
 	public void ShouldSubpixelQuantizeFonts (bool shouldSubpixelQuantizeFonts);
</pre>
<h4>Type Changed: MonoTouch.CoreGraphics.CGInterpolationQuality</h4>
<p>Removed:</p><pre>
 	High
</pre>
<p>Added:</p><pre>
 	High,
 	Medium
</pre>
<h4>Type Changed: MonoTouch.CoreGraphics.CGLayer</h4>
<p>Added:</p><pre>
 	public CGContext Context {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.CoreGraphics.CGPath</h4>
<p>Added:</p><pre>
 	public System.Drawing.RectangleF PathBoundingBox {
 		get;
 	}
</pre>
<h3>Namespace: MonoTouch.CoreLocation</h3>
<h4>New Type: MonoTouch.CoreLocation.CLDeviceOrientation</h4>
<pre>
[Serializable]
public enum CLDeviceOrientation {
	Unknown,
	Portrait,
	PortraitUpsideDown,
	LandscapeLeft,
	LandscapeRight,
	FaceUp,
	FaceDown
}
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLError</h4>
<p>Removed:</p><pre>
 	HeadingFailure
</pre>
<p>Added:</p><pre>
 	HeadingFailure,
 	RegionMonitoringDenied,
 	RegionMonitoringFailure,
 	RegionMonitoringSetupDelayed
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs
</pre>
<p>Added:</p><pre>
 public class CLHeadingUpdatedEventArgs : EventArgs {
 	
 	public CLHeadingUpdatedEventArgs (CLHeading newHeading);
 	
 	public CLHeading NewHeading {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLLocationCoordinate2D</h4>
<p>Added:</p><pre>
 	public bool IsValid ();
 	
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h4>
<p>Removed:</p><pre>
 	public virtual bool LocationServicesEnabled {
</pre>
<p>Added:</p><pre>
 	public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
 	public virtual void StartMonitoringSignificantLocationChanges ();
 	public virtual void StopMonitoring (CLRegion region);
 	public virtual void StopMonitoringSignificantLocationChanges ();
 	public static bool LocationServicesEnabled {
 		get;
 	}
 	public static bool RegionMonitoringAvailable {
 		get;
 	}
 	public static bool RegionMonitoringEnabled {
 		get;
 	}
 	public static bool SignificantLocationChangeMonitoringAvailable {
 		get;
 	}
 	public virtual CLHeading Heading {
 		get;
 	}
 	public virtual CLDeviceOrientation HeadingOrientation {
 		get;
 		set;
 	}
 	public virtual double MaximumRegionMonitoringDistance {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSSet MonitoredRegions {
 	public CLLocationManagerEventArgs ShouldDisplayHeadingCalibration {
 		get;
 		set;
 	}
 	
 	public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; Failed;
 	public event EventHandler&lt;CLRegionErrorEventArgs&gt; MonitoringFailed;
 	public event EventHandler&lt;CLRegionEventArgs&gt; RegionEntered;
 	public event EventHandler&lt;CLRegionEventArgs&gt; RegionLeft;
 	public event EventHandler&lt;CLHeadingUpdatedEventArgs&gt; UpdatedHeading;
 	public event EventHandler&lt;CLLocationUpdatedEventArgs&gt; UpdatedLocation;
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h4>
<p>Added:</p><pre>
 	public virtual void MonitoringFailed (CLLocationManager manager, CLRegion region, MonoTouch.Foundation.NSError error);
 	public virtual void RegionEntered (CLLocationManager manager, CLRegion region);
 	public virtual void RegionLeft (CLLocationManager manager, CLRegion region);
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLLocationManagerEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLLocationManagerEventArgs
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool CLLocationManagerEventArgs (CLLocationManager manager);
</pre>
<h4>Type Changed: MonoTouch.CoreLocation.CLLocationUpdatedEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.CoreLocation.CLLocationUpdatedEventArgs
</pre>
<p>Added:</p><pre>
 public class CLLocationUpdatedEventArgs : EventArgs {
 	
 	public CLLocationUpdatedEventArgs (CLLocation newLocation, CLLocation oldLocation);
 	
 	public CLLocation NewLocation {
 		get;
 		set;
 	}
 	public CLLocation OldLocation {
 		get;
 		set;
 	}
 }
</pre>
<h4>New Type: MonoTouch.CoreLocation.CLRegion</h4>
<pre>
public class CLRegion : MonoTouch.Foundation.NSObject {
	
	public CLRegion ();
	public CLRegion (MonoTouch.Foundation.NSCoder coder);
	public CLRegion (MonoTouch.Foundation.NSObjectFlag t);
	public CLRegion (IntPtr handle);
	public CLRegion (CLLocationCoordinate2D center, double radius, string identifier);
	
	public virtual bool Contains (CLLocationCoordinate2D coordinate);
	
	public virtual CLLocationCoordinate2D Center {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Identifier {
		get;
	}
	public virtual double Radius {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreLocation.CLRegionErrorEventArgs</h4>
<pre>
public class CLRegionErrorEventArgs : EventArgs {
	
	public CLRegionErrorEventArgs (CLRegion region, MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
	public CLRegion Region {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreLocation.CLRegionEventArgs</h4>
<pre>
public class CLRegionEventArgs : EventArgs {
	
	public CLRegionEventArgs (CLRegion region);
	
	public CLRegion Region {
		get;
		set;
	}
}
</pre>
<h3>Namespace: MonoTouch.CoreMedia</h3>
<h4>New Type: MonoTouch.CoreMedia.CMSampleBuffer</h4>
<pre>
public class CMSampleBuffer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	
	public IntPtr Handle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMedia.CMTime</h4>
<pre>
public struct CMTime {
	
	public long Value;
	public int TimeScale;
	public int TimeFlags;
	public long TimeEpoch;
}
</pre>
<h4>New Type: MonoTouch.CoreMedia.CMTimeMapping</h4>
<pre>
public struct CMTimeMapping {
	
	public CMTime Source;
	public CMTime Target;
}
</pre>
<h4>New Type: MonoTouch.CoreMedia.CMTimeRange</h4>
<pre>
public struct CMTimeRange {
	
	public CMTime Start;
	public CMTime Duration;
}
</pre>
<h3>Namespace: MonoTouch.CoreMotion</h3>
<h4>New Type: MonoTouch.CoreMotion.CMAcceleration</h4>
<pre>
public struct CMAcceleration {
	
	public CMAcceleration (double x, double y, double z);
	
	public double X;
	public double Y;
	public double Z;
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMAccelerometerData</h4>
<pre>
public class CMAccelerometerData : CMLogItem {
	
	public CMAccelerometerData ();
	public CMAccelerometerData (MonoTouch.Foundation.NSCoder coder);
	public CMAccelerometerData (MonoTouch.Foundation.NSObjectFlag t);
	public CMAccelerometerData (IntPtr handle);
	
	public virtual CMAcceleration Acceleration {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMAccelerometerHandler</h4>
<pre>
[Serializable]
public delegate void CMAccelerometerHandler (CMAccelerometerData data, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMAttitude</h4>
<pre>
public class CMAttitude : MonoTouch.Foundation.NSObject {
	
	public CMAttitude ();
	public CMAttitude (MonoTouch.Foundation.NSCoder coder);
	public CMAttitude (MonoTouch.Foundation.NSObjectFlag t);
	public CMAttitude (IntPtr handle);
	
	public virtual void MultiplyByInverseOfAttitude (CMAttitude attitude);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Pitch {
		get;
	}
	public virtual CMQuaternion Quaternion {
		get;
	}
	public virtual double Roll {
		get;
	}
	public virtual CMRotationMatrix RotationMatrix {
		get;
	}
	public virtual double Yaw {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMDeviceMotion</h4>
<pre>
public class CMDeviceMotion : CMLogItem {
	
	public CMDeviceMotion ();
	public CMDeviceMotion (MonoTouch.Foundation.NSCoder coder);
	public CMDeviceMotion (MonoTouch.Foundation.NSObjectFlag t);
	public CMDeviceMotion (IntPtr handle);
	
	public virtual CMAttitude Attitude {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMAcceleration Gravity {
		get;
	}
	public virtual CMRotationRate RotationRate {
		get;
	}
	public virtual CMAcceleration UserAcceleration {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMDeviceMotionHandler</h4>
<pre>
[Serializable]
public delegate void CMDeviceMotionHandler (CMDeviceMotion motion, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMError</h4>
<pre>
[Serializable]
public enum CMError {
	Null
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMGyroData</h4>
<pre>
public class CMGyroData : CMLogItem {
	
	public CMGyroData ();
	public CMGyroData (MonoTouch.Foundation.NSCoder coder);
	public CMGyroData (MonoTouch.Foundation.NSObjectFlag t);
	public CMGyroData (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMRotationRate RotationRate {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMGyroHandler</h4>
<pre>
[Serializable]
public delegate void CMGyroHandler (CMGyroData gyroData, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMLogItem</h4>
<pre>
public class CMLogItem : MonoTouch.Foundation.NSObject {
	
	public CMLogItem ();
	public CMLogItem (MonoTouch.Foundation.NSCoder coder);
	public CMLogItem (MonoTouch.Foundation.NSObjectFlag t);
	public CMLogItem (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double Timestamp {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMMotionManager</h4>
<pre>
public class CMMotionManager : MonoTouch.Foundation.NSObject {
	
	public CMMotionManager ();
	public CMMotionManager (MonoTouch.Foundation.NSCoder coder);
	public CMMotionManager (MonoTouch.Foundation.NSObjectFlag t);
	public CMMotionManager (IntPtr handle);
	
	public virtual void StartAccelerometerUpdates ();
	public virtual void StartAccelerometerUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMAccelerometerHandler handler);
	public virtual void StartDeviceMotionUpdates ();
	public virtual void StartDeviceMotionUpdates (MonoTouch.Foundation.NSOperationQueue toQueue, CMDeviceMotionHandler handler);
	public virtual void StartGyroUpdates ();
	public virtual void StartGyroUpdates (MonoTouch.Foundation.NSOperationQueue toQueue, CMGyroHandler handler);
	public virtual void StopAccelerometerUpdates ();
	public virtual void StopDeviceMotionUpdates ();
	public virtual void StopGyroUpdates ();
	
	public virtual bool AccelerometerActive {
		get;
	}
	public virtual bool AccelerometerAvailable {
		get;
	}
	public virtual CMAccelerometerData AccelerometerData {
		get;
	}
	public virtual double AccelerometerUpdateInterval {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMDeviceMotion DeviceMotion {
		get;
	}
	public virtual bool DeviceMotionActive {
		get;
	}
	public virtual bool DeviceMotionAvailable {
		get;
	}
	public virtual double DeviceMotionUpdateInterval {
		get;
		set;
	}
	public virtual bool GyroActive {
		get;
	}
	public virtual bool GyroAvailable {
		get;
	}
	public virtual CMGyroData GyroData {
		get;
	}
	public virtual double GyroUpdateInterval {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMQuaternion</h4>
<pre>
public struct CMQuaternion {
	
	public CMQuaternion (double x, double y, double z, double w);
	
	public double x;
	public double y;
	public double z;
	public double w;
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMRotationMatrix</h4>
<pre>
public struct CMRotationMatrix {
	
	public double m11;
	public double m12;
	public double m13;
	public double m21;
	public double m22;
	public double m23;
	public double m31;
	public double m32;
	public double m33;
}
</pre>
<h4>New Type: MonoTouch.CoreMotion.CMRotationRate</h4>
<pre>
public struct CMRotationRate {
	
	public CMRotationRate (double x, double y, double z);
	
	public double x;
	public double y;
	public double z;
}
</pre>
<h3>Namespace: MonoTouch.CoreTelephony</h3>
<h4>New Type: MonoTouch.CoreTelephony.CTCall</h4>
<pre>
public class CTCall : MonoTouch.Foundation.NSObject {
	
	public CTCall ();
	public CTCall (MonoTouch.Foundation.NSCoder coder);
	public CTCall (MonoTouch.Foundation.NSObjectFlag t);
	public CTCall (IntPtr handle);
	
	public virtual string CallID {
		get;
	}
	public virtual string CallState {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public string StateConnected {
		get;
	}
	public string StateDialing {
		get;
	}
	public string StateDisconnected {
		get;
	}
	public string StateIncoming {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreTelephony.CTCallCenter</h4>
<pre>
public class CTCallCenter : MonoTouch.Foundation.NSObject {
	
	public CTCallCenter ();
	public CTCallCenter (MonoTouch.Foundation.NSCoder coder);
	public CTCallCenter (MonoTouch.Foundation.NSObjectFlag t);
	public CTCallCenter (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSSet CurrentCalls {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.CoreTelephony.CTCallEventHandler</h4>
<pre>
[Serializable]
public delegate void CTCallEventHandler (CTCall call);
</pre>
<h4>New Type: MonoTouch.CoreTelephony.CTCarrier</h4>
<pre>
public class CTCarrier : MonoTouch.Foundation.NSObject {
	
	public CTCarrier ();
	public CTCarrier (MonoTouch.Foundation.NSCoder coder);
	public CTCarrier (MonoTouch.Foundation.NSObjectFlag t);
	public CTCarrier (IntPtr handle);
	
	public virtual bool AllowsVoip {
		get;
	}
	public virtual string CarrierName {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string IsoCountryCode {
		get;
	}
	public virtual string MobileCountryCode {
		get;
	}
	public virtual string MobileNetworkCode {
		get;
	}
}
</pre>
<h3>Namespace: MonoTouch.EventKit</h3>
<h4>New Type: MonoTouch.EventKit.EKAlarm</h4>
<pre>
public class EKAlarm : MonoTouch.Foundation.NSObject {
	
	public EKAlarm ();
	public EKAlarm (MonoTouch.Foundation.NSCoder coder);
	public EKAlarm (MonoTouch.Foundation.NSObjectFlag t);
	public EKAlarm (IntPtr handle);
	
	public static EKAlarm FromDate (MonoTouch.Foundation.NSDate date);
	public static EKAlarm FromTimeInterval (double offsetSeconds);
	
	public virtual MonoTouch.Foundation.NSDate AbsoluteDate {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual double RelativeOffset {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKCalendar</h4>
<pre>
public class EKCalendar : MonoTouch.Foundation.NSObject {
	
	public EKCalendar ();
	public EKCalendar (MonoTouch.Foundation.NSCoder coder);
	public EKCalendar (MonoTouch.Foundation.NSObjectFlag t);
	public EKCalendar (IntPtr handle);
	
	public virtual bool AllowsContentModifications {
		get;
	}
	public virtual MonoTouch.CoreGraphics.CGColor CGColor {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual EKCalendarEventAvailability SupportedEventAvailabilities {
		get;
	}
	public virtual string Title {
		get;
	}
	public virtual EKCalendarType Type {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKCalendarEventAvailability</h4>
<pre>
[Serializable]
[Flags]
public enum EKCalendarEventAvailability {
	None,
	Busy,
	Free,
	Tentative,
	Unavailable
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKCalendarType</h4>
<pre>
[Serializable]
public enum EKCalendarType {
	Local,
	CalDav,
	Exchange,
	Subscription,
	Birthday
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKDay</h4>
<pre>
[Serializable]
public enum EKDay {
	NotSet,
	Sunday,
	Monday,
	Tuesday,
	Wednesday,
	Thursday,
	Friday,
	Saturday
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKErrorCode</h4>
<pre>
[Serializable]
public enum EKErrorCode {
	EventNotMutable,
	NoCalendar,
	NoStartDate,
	NoEndDate,
	DatesInverted,
	InternalFailure,
	CalendarReadOnly,
	DurationGreaterThanRecurrence,
	AlarmGreaterThanRecurrence,
	StartDateTooFarInFuture,
	StartDateCollidesWithOtherOccurrence,
	ObjectBelongsToDifferentStore,
	InvitesCannotBeMoved
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKEvent</h4>
<pre>
public class EKEvent : MonoTouch.Foundation.NSObject {
	
	public EKEvent ();
	public EKEvent (MonoTouch.Foundation.NSCoder coder);
	public EKEvent (MonoTouch.Foundation.NSObjectFlag t);
	public EKEvent (IntPtr handle);
	
	public static EKEvent FromStore (EKEventStore eventStore);
	public virtual void AddAlarm (EKAlarm alarm);
	public virtual MonoTouch.Foundation.NSComparisonResult CompareStartDateWithEvent (EKEvent other);
	public virtual bool Refresh ();
	public virtual void RemoveAlarm (EKAlarm alarm);
	
	public virtual EKAlarm[] Alarms {
		get;
		set;
	}
	public virtual bool AllDay {
		get;
		set;
	}
	public virtual EKParticipant[] Attendees {
		get;
	}
	public virtual EKEventAvailability Availability {
		get;
		set;
	}
	public virtual EKCalendar Calendar {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate EndDate {
		get;
		set;
	}
	public virtual string EventIdentifier {
		get;
	}
	public virtual bool IsDetached {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate LastModifiedDate {
		get;
	}
	public virtual string Location {
		get;
		set;
	}
	public virtual string Notes {
		get;
		set;
	}
	public virtual EKParticipant Organizer {
		get;
	}
	public virtual EKRecurrenceRule RecurrenceRule {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDate StartDate {
		get;
		set;
	}
	public virtual EKEventStatus Status {
		get;
	}
	public virtual string Title {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKEventAvailability</h4>
<pre>
[Serializable]
public enum EKEventAvailability {
	NotSupported,
	Busy,
	Free,
	Tentative,
	Unavailable
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKEventEditViewAction</h4>
<pre>
[Serializable]
public enum EKEventEditViewAction {
	Canceled,
	Saved,
	Deleted
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKEventSearchCallback</h4>
<pre>
[Serializable]
public delegate void EKEventSearchCallback (EKEvent theEvent, ref bool stop);
</pre>
<h4>New Type: MonoTouch.EventKit.EKEventStatus</h4>
<pre>
[Serializable]
public enum EKEventStatus {
	None,
	Confirmed,
	Tentative,
	Cancelled
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKEventStore</h4>
<pre>
public class EKEventStore : MonoTouch.Foundation.NSObject {
	
	public EKEventStore ();
	public EKEventStore (MonoTouch.Foundation.NSCoder coder);
	public EKEventStore (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventStore (IntPtr handle);
	
	public virtual void EnumerateEvents (MonoTouch.Foundation.NSPredicate predicate, EKEventSearchCallback block);
	public virtual EKEvent EventFromIdentifier (string identifier);
	public virtual EKEvent[] EventsMatchin (MonoTouch.Foundation.NSPredicate predicate);
	public virtual MonoTouch.Foundation.NSPredicate PredicateForEvents (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
	public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, IntPtr ptrToNserror);
	public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, IntPtr ptrToNsError);
	
	public static MonoTouch.Foundation.NSString ChangedNotification {
		get;
	}
	public virtual EKCalendar[] Calendars {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual EKCalendar DefaultCalendarForNewEvents {
		get;
	}
	public virtual string EventStoreIdentifier {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKParticipant</h4>
<pre>
public class EKParticipant : MonoTouch.Foundation.NSObject {
	
	public EKParticipant ();
	public EKParticipant (MonoTouch.Foundation.NSCoder coder);
	public EKParticipant (MonoTouch.Foundation.NSObjectFlag t);
	public EKParticipant (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual EKParticipantRole ParticipantRole {
		get;
	}
	public virtual EKParticipantStatus ParticipantStatus {
		get;
	}
	public virtual EKParticipantType ParticipantType {
		get;
	}
	public virtual MonoTouch.Foundation.NSUrl Url {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKParticipantRole</h4>
<pre>
[Serializable]
public enum EKParticipantRole {
	Unknown,
	Required,
	Optional,
	Chair,
	NonParticipant
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKParticipantStatus</h4>
<pre>
[Serializable]
public enum EKParticipantStatus {
	Unknown,
	Pending,
	Accepted,
	Declined,
	Tentative,
	Delegated,
	Completed,
	InProcess
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKParticipantType</h4>
<pre>
[Serializable]
public enum EKParticipantType {
	Unknown,
	Person,
	Room,
	Resource,
	Group
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKRecurrenceDayOfWeek</h4>
<pre>
public class EKRecurrenceDayOfWeek : MonoTouch.Foundation.NSObject {
	
	public EKRecurrenceDayOfWeek ();
	public EKRecurrenceDayOfWeek (MonoTouch.Foundation.NSCoder coder);
	public EKRecurrenceDayOfWeek (MonoTouch.Foundation.NSObjectFlag t);
	public EKRecurrenceDayOfWeek (IntPtr handle);
	
	public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek);
	public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek, int weekNumber);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int DayOfTheWeek {
		get;
	}
	public virtual int WeekNumber {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKRecurrenceEnd</h4>
<pre>
public class EKRecurrenceEnd : MonoTouch.Foundation.NSObject {
	
	public EKRecurrenceEnd ();
	public EKRecurrenceEnd (MonoTouch.Foundation.NSCoder coder);
	public EKRecurrenceEnd (MonoTouch.Foundation.NSObjectFlag t);
	public EKRecurrenceEnd (IntPtr handle);
	
	public static EKRecurrenceEnd FromEndDate (MonoTouch.Foundation.NSDate endDate);
	public static EKRecurrenceEnd FromOccurrenceCount (int occurrenceCount);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate EndDate {
		get;
	}
	public virtual int OccurrenceCount {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKRecurrenceFrequency</h4>
<pre>
[Serializable]
public enum EKRecurrenceFrequency {
	Daily,
	Weekly,
	Monthly,
	Yearly
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKRecurrenceRule</h4>
<pre>
public class EKRecurrenceRule : MonoTouch.Foundation.NSObject {
	
	public EKRecurrenceRule ();
	public EKRecurrenceRule (MonoTouch.Foundation.NSCoder coder);
	public EKRecurrenceRule (MonoTouch.Foundation.NSObjectFlag t);
	public EKRecurrenceRule (IntPtr handle);
	public EKRecurrenceRule (EKRecurrenceFrequency type, int interval, EKRecurrenceEnd end);
	public EKRecurrenceRule (EKRecurrenceFrequency type, int interval, EKRecurrenceDayOfWeek[] days, MonoTouch.Foundation.NSNumber[] monthDays, MonoTouch.Foundation.NSNumber[] months, MonoTouch.Foundation.NSNumber[] weeksOfTheYear, MonoTouch.Foundation.NSNumber[] daysOfTheYear, MonoTouch.Foundation.NSNumber[] setPositions, EKRecurrenceEnd end);
	
	public virtual string CalendarIdentifier {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] DaysOfTheMonth {
		get;
	}
	public virtual EKRecurrenceDayOfWeek[] DaysOfTheWeek {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] daysOfTheYear {
		get;
	}
	public virtual EKDay FirstDayOfTheWeek {
		get;
	}
	public virtual EKRecurrenceFrequency Frequency {
		get;
	}
	public virtual int Interval {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] monthsOfTheYear {
		get;
	}
	public virtual EKRecurrenceEnd RecurrenceEnd {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject[] SetPositions {
		get;
	}
	public virtual MonoTouch.Foundation.NSNumber[] WeeksOfTheYear {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKit.EKSpan</h4>
<pre>
[Serializable]
public enum EKSpan {
	ThisEvent,
	FutureEvents
}
</pre>
<h3>Namespace: MonoTouch.EventKitUI</h3>
<h4>New Type: MonoTouch.EventKitUI.EKEventEditController</h4>
<pre>
[Serializable]
public delegate MonoTouch.EventKit.EKCalendar EKEventEditController (EKEventEditViewController controller);
</pre>
<h4>New Type: MonoTouch.EventKitUI.EKEventEditEventArgs</h4>
<pre>
public class EKEventEditEventArgs : EventArgs {
	
	public EKEventEditEventArgs (MonoTouch.EventKit.EKEventEditViewAction action);
	
	public MonoTouch.EventKit.EKEventEditViewAction Action {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.EventKitUI.EKEventEditViewController</h4>
<pre>
public class EKEventEditViewController : MonoTouch.UIKit.UINavigationController {
	
	public EKEventEditViewController ();
	public EKEventEditViewController (MonoTouch.Foundation.NSCoder coder);
	public EKEventEditViewController (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventEditViewController (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public EKEventEditViewDelegate EditViewDelegate {
		get;
		set;
	}
	public virtual MonoTouch.EventKit.EKEvent Event {
		get;
		set;
	}
	public virtual MonoTouch.EventKit.EKEventStore EventStore {
		get;
		set;
	}
	public EKEventEditController GetDefaultCalendarForNewEvents {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakEditViewDelegate {
		get;
		set;
	}
	
	public event EventHandler<ekeventediteventargs> Completed;
}
</ekeventediteventargs></pre>
<h4>New Type: MonoTouch.EventKitUI.EKEventEditViewDelegate</h4>
<pre>
public abstract class EKEventEditViewDelegate : MonoTouch.Foundation.NSObject {
	
	public EKEventEditViewDelegate ();
	public EKEventEditViewDelegate (MonoTouch.Foundation.NSCoder coder);
	public EKEventEditViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventEditViewDelegate (IntPtr handle);
	
	public abstract void Completed (EKEventEditViewController controller, MonoTouch.EventKit.EKEventEditViewAction action);
	public virtual MonoTouch.EventKit.EKCalendar GetDefaultCalendarForNewEvents (EKEventEditViewController controller);
}
</pre>
<h4>New Type: MonoTouch.EventKitUI.EKEventViewController</h4>
<pre>
public class EKEventViewController : MonoTouch.UIKit.UIViewController {
	
	public EKEventViewController ();
	public EKEventViewController (MonoTouch.Foundation.NSCoder coder);
	public EKEventViewController (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventViewController (IntPtr handle);
	
	public virtual bool AllowsCalendarPreview {
		get;
		set;
	}
	public virtual bool AllowsEditing {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.EventKit.EKEvent Event {
		get;
		set;
	}
}
</pre>
<h3>Namespace: MonoTouch.ExternalAccessory</h3>
<h4>New Type: MonoTouch.ExternalAccessory.EAAccessory</h4>
<pre>
public class EAAccessory : MonoTouch.Foundation.NSObject {
	
	public EAAccessory ();
	public EAAccessory (MonoTouch.Foundation.NSCoder coder);
	public EAAccessory (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessory (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Connected {
		get;
	}
	public virtual uint ConnectionID {
		get;
	}
	public EAAccessoryDelegate Delegate {
		get;
		set;
	}
	public virtual string FirmwareRevision {
		get;
	}
	public virtual string HardwareRevision {
		get;
	}
	public virtual string Manufacturer {
		get;
	}
	public virtual string ModelNumber {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual string [] ProtocolStrings {
		get;
	}
	public virtual string SerialNumber {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler Disconnected;
}
</pre>
<h4>New Type: MonoTouch.ExternalAccessory.EAAccessoryDelegate</h4>
<pre>
public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject {
	
	public EAAccessoryDelegate ();
	public EAAccessoryDelegate (MonoTouch.Foundation.NSCoder coder);
	public EAAccessoryDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessoryDelegate (IntPtr handle);
	
	public virtual void Disconnected (EAAccessory accessory);
}
</pre>
<h4>New Type: MonoTouch.ExternalAccessory.EAAccessoryManager</h4>
<pre>
public class EAAccessoryManager : MonoTouch.Foundation.NSObject {
	
	public EAAccessoryManager ();
	public EAAccessoryManager (MonoTouch.Foundation.NSCoder coder);
	public EAAccessoryManager (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessoryManager (IntPtr handle);
	
	public virtual void RegisterForLocalNotifications ();
	public virtual void UnregisterForLocalNotifications ();
	
	public static EAAccessoryManager SharedAccessoryManager {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual EAAccessory[] ConnectedAccessories {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.ExternalAccessory.EASession</h4>
<pre>
public class EASession : MonoTouch.Foundation.NSObject {
	
	public EASession ();
	public EASession (MonoTouch.Foundation.NSCoder coder);
	public EASession (MonoTouch.Foundation.NSObjectFlag t);
	public EASession (IntPtr handle);
	public EASession (EAAccessory accessory, string protocol);
	
	public virtual EAAccessory Accessory {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSInputStream InputStream {
		get;
	}
	public virtual MonoTouch.Foundation.NSOutputStream OutputStream {
		get;
	}
	public virtual string ProtocolString {
		get;
	}
}
</pre>
<h3>Namespace: MonoTouch.Foundation</h3>
<h4>Type Changed: MonoTouch.Foundation.NSAttributedString</h4>
<p>Removed:</p><pre>
 	public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<p>Added:</p><pre>
 	public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
 	public static NSString FontAttributeName {
 		get;
 	}
 	public static NSString ParagraphStyleAttributeName {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.Foundation.NSBlockOperation</h4>
<pre>
public class NSBlockOperation : NSOperation {
	
	public NSBlockOperation ();
	public NSBlockOperation (NSCoder coder);
	public NSBlockOperation (NSObjectFlag t);
	public NSBlockOperation (IntPtr handle);
	
	public static NSBlockOperation Create (NSAction method);
	public virtual void AddExecutionBlock (NSAction method);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSObject[] ExecutionBlocks {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSBundle</h4>
<p>Added:</p><pre>
 	public NSBundle (NSUrl url);
 	public static NSBundle FromUrl (NSUrl url);
 	public virtual NSUrl UrlForAuxiliaryExecutable (string executable);
 	public virtual NSUrl BuiltInPluginsUrl {
 		get;
 	}
 	public virtual NSUrl BundleUrl {
 		get;
 	}
 	public virtual NSUrl ExecutableUrl {
 		get;
 	}
 	public virtual NSUrl PrivateFrameworksUrl {
 		get;
 	}
 	public virtual NSUrl ResourceUrl {
 		get;
 	}
 	public virtual NSUrl SharedFrameworksUrl {
 		get;
 	}
 	public virtual NSUrl SharedSupportUrl {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.Foundation.NSCache</h4>
<pre>
public class NSCache : NSObject {
	
	public NSCache ();
	public NSCache (NSCoder coder);
	public NSCache (NSObjectFlag t);
	public NSCache (IntPtr handle);
	
	public virtual NSObject ObjectForKey (NSObject key);
	public virtual void RemoveAllObjects ();
	public virtual void RemoveObjectForKey (NSObject key);
	public virtual void SetCost (NSObject obj, NSObject key, uint cost);
	public virtual void SetObjectforKey (NSObject obj, NSObject key);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual uint CountLimit {
		get;
		set;
	}
	public NSCacheDelegate Delegate {
		get;
		set;
	}
	public virtual bool EvictsObjectsWithDiscardedContent {
		get;
		set;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual uint TotalCostLimit {
		get;
		set;
	}
	public virtual NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler<nsobjecteventargs> WillEvictObject;
}
</nsobjecteventargs></pre>
<h4>New Type: MonoTouch.Foundation.NSCacheDelegate</h4>
<pre>
public class NSCacheDelegate : NSObject {
	
	public NSCacheDelegate ();
	public NSCacheDelegate (NSCoder coder);
	public NSCacheDelegate (NSObjectFlag t);
	public NSCacheDelegate (IntPtr handle);
	
	public virtual void WillEvictObject (NSCache cache, NSObject obj);
}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSCalendarUnit</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSCalendarUnit
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSCalendarUnit {
 	NSEra,
 	NSYear,
 	NSMonth,
 	NSDay,
 	NSHour,
 	NSMinute,
 	NSSecond,
 	NSWeek,
 	NSWeekday,
 	NSWeekdayOrdinal,
 	NSQuarter,
 	NSCalendar,
 	NSTimeZone
 }
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSData</h4>
<p>Added:</p><pre>
 	public virtual NSRange Find (NSData dataToFind, NSDataSearchOptions searchOptions, NSRange searchRange);
 	public bool Save (string file, NSDataWritingOptions options, out NSError error);
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSDataSearchOptions</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSDataSearchOptions
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSDataSearchOptions {
 	SearchBackwards,
 	SearchAnchored
 }
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSDataWritingOptions</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSDataWritingOptions
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSDataWritingOptions : uint {
 	Atomic,
 	FileProtectionNone,
 	FileProtectionComplete,
 	NSDataWritingFileProtectionMask
 }
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSDateComponents</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSDateComponents
</pre>
<p>Added:</p><pre>
 public class NSDateComponents : NSObject {
 	
 	public NSDateComponents ();
 	public NSDateComponents (NSCoder coder);
 	public NSDateComponents (NSObjectFlag t);
 	public NSDateComponents (IntPtr handle);
 	
 	public virtual NSCalendar Calendar {
 		get;
 		set;
 	}
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public virtual NSDate Date {
 		get;
 	}
 	public virtual int Day {
 		get;
 		set;
 	}
 	public virtual int Era {
 		get;
 		set;
 	}
 	public virtual int Hour {
 		get;
 		set;
 	}
 	public virtual int Minute {
 		get;
 		set;
 	}
 	public virtual int Month {
 		get;
 		set;
 	}
 	public virtual int Quarter {
 		get;
 		set;
 	}
 	public virtual int Second {
 		get;
 		set;
 	}
 	public virtual NSTimeZone TimeZone {
 		get;
 		set;
 	}
 	public virtual int Week {
 		get;
 		set;
 	}
 	public virtual int Weekday {
 		get;
 		set;
 	}
 	public virtual int WeekdayOrdinal {
 		get;
 		set;
 	}
 	public virtual int Year {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h4>
<p>Removed:</p><pre>
 	public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<p>Added:</p><pre>
 	public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<h4>New Type: MonoTouch.Foundation.NSMutableSet</h4>
<pre>
public class NSMutableSet : NSSet {
	
	public NSMutableSet ();
	public NSMutableSet (NSCoder coder);
	public NSMutableSet (NSObjectFlag t);
	public NSMutableSet (IntPtr handle);
	
	public virtual void Add (NSObject nso);
	public virtual void Remove (NSObject nso);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSNotificationCenter</h4>
<p>Added:</p><pre>
 	public virtual void AddObserver (string name, NSObject obj, NSOperationQueue queue, NSNotificationHandler handler);
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSNotificationCoalescing</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSNotificationCoalescing
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSNotificationCoalescing {
 	NoCoalescing,
 	CoalescingOnName,
 	CoalescingOnSender
 }
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSNotificationHandler</h4>
<p>Removed:</p><pre>
 internal class NSNotificationHandler : NSObject {
 	
 	public NSNotificationHandler (Action&lt;NSNotification&gt; notify);
 	
 	public void Post (NSNotification s);
 }
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate void NSNotificationHandler (NSNotification notification);
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSNotificationQueue</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSNotificationQueue
</pre>
<p>Added:</p><pre>
 public class NSNotificationQueue : NSObject {
 	
 	public NSNotificationQueue ();
 	public NSNotificationQueue (NSCoder coder);
 	public NSNotificationQueue (NSObjectFlag t);
 	public NSNotificationQueue (IntPtr handle);
 	public NSNotificationQueue (NSNotificationCenter notificationCenter);
 	
 	public virtual void DequeueNotificationsMatchingcoalesceMask (NSNotification notification, NSNotificationCoalescing coalesceMask);
 	public virtual void EnqueueNotification (NSNotification notification, NSPostingStyle postingStyle);
 	public virtual void EnqueueNotification (NSNotification notification, NSPostingStyle postingStyle, NSNotificationCoalescing coalesceMask, string [] modes);
 	
 	public static NSObject DefaultQueue {
 		get;
 	}
 	public override IntPtr ClassHandle {
 		get;
 	}
 }
</pre>
<h4>New Type: MonoTouch.Foundation.NSNull</h4>
<pre>
public class NSNull : NSObject {
	
	public NSNull ();
	public NSNull (NSCoder coder);
	public NSNull (NSObjectFlag t);
	public NSNull (IntPtr handle);
	
	public static NSNull Null {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSOperation</h4>
<pre>
public class NSOperation : NSObject {
	
	public NSOperation ();
	public NSOperation (NSCoder coder);
	public NSOperation (NSObjectFlag t);
	public NSOperation (IntPtr handle);
	
	public virtual void AddDependency (NSOperation op);
	public virtual void Cancel ();
	public virtual void Main ();
	public virtual void RemoveDependency (NSOperation op);
	public virtual void Start ();
	public virtual void WaitUntilFinishedNS ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSOperation[] Dependencies {
		get;
	}
	public virtual bool IsCancelled {
		get;
	}
	public virtual bool IsConcurrent {
		get;
	}
	public virtual bool IsExecuting {
		get;
	}
	public virtual bool IsFinished {
		get;
	}
	public virtual bool IsReady {
		get;
	}
	public virtual NSOperationQueuePriority QueuePriority {
		get;
		set;
	}
	public virtual double ThreadPriority {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSOperationQueue</h4>
<pre>
public class NSOperationQueue : NSObject {
	
	public NSOperationQueue ();
	public NSOperationQueue (NSCoder coder);
	public NSOperationQueue (NSObjectFlag t);
	public NSOperationQueue (IntPtr handle);
	
	public virtual void AddOperation (NSAction operation);
	public virtual void AddOperation (NSOperation op);
	public virtual void AddOperations (NSOperation[] operations, bool waitUntilFinished);
	public virtual void CancelAllOperations ();
	public virtual void WaitUntilAllOperationsAreFinished ();
	
	public static NSOperationQueue CurrentQueue {
		get;
	}
	public static NSOperationQueue MainQueue {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int MaxConcurrentOperationCount {
		get;
		set;
	}
	public virtual string Name {
		get;
		set;
	}
	public virtual int OperationCount {
		get;
	}
	public virtual NSOperation[] Operations {
		get;
	}
	public virtual bool Suspended {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSOperationQueuePriority</h4>
<pre>
[Serializable]
public enum NSOperationQueuePriority {
	VeryLow,
	Low,
	Normal,
	High,
	VeryHigh
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSPostingStyle</h4>
<pre>
[Serializable]
public enum NSPostingStyle {
	PostWhenIdle,
	PostASAP,
	Now
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSPredicate</h4>
<pre>
public class NSPredicate : NSObject {
	
	public NSPredicate ();
	public NSPredicate (NSCoder coder);
	public NSPredicate (NSObjectFlag t);
	public NSPredicate (IntPtr handle);
	
	public virtual bool EvaluateWithObject (NSObject obj);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.Foundation.NSPurgeableData</h4>
<pre>
public class NSPurgeableData : NSMutableData {
	
	public NSPurgeableData ();
	public NSPurgeableData (NSCoder coder);
	public NSPurgeableData (NSObjectFlag t);
	public NSPurgeableData (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSRange</h4>
<p>Added:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSSetEnumerator</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSSetEnumerator
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate void NSSetEnumerator (NSObject obj, ref bool stop);
</pre>
<h4>New Type: MonoTouch.Foundation.NSSortDescriptor</h4>
<pre>
public class NSSortDescriptor : NSObject {
	
	public NSSortDescriptor ();
	public NSSortDescriptor (NSCoder coder);
	public NSSortDescriptor (NSObjectFlag t);
	public NSSortDescriptor (IntPtr handle);
	public NSSortDescriptor (string key, bool ascending);
	public NSSortDescriptor (string key, bool ascending, MonoTouch.ObjCRuntime.Selector selector);
	
	public virtual NSComparisonResult Compare (NSObject object1, NSObject object2);
	
	public virtual bool Ascending {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Key {
		get;
	}
	public virtual NSObject ReversedSortDescriptor {
		get;
	}
	public virtual MonoTouch.ObjCRuntime.Selector Selector {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSTimer</h4>
<p>Removed:</p><pre>
 	public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
</pre>
<p>Added:</p><pre>
 	public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
 	public static NSTimer CreateRepeatingScheduledTimer (double seconds, NSAction action);
 	public static NSTimer CreateRepeatingTimer (double seconds, NSAction action);
 	public static NSTimer CreateScheduledTimer (double seconds, NSAction action);
 	public static NSTimer CreateTimer (double seconds, NSAction action);
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSTimeZone</h4>
<p>Added:</p><pre>
 	public NSTimeZone (string name);
 	public static NSTimeZone FromAbbreviation (string abbreviation);
 	public static NSTimeZone FromName (string timeZoneName);
 	public static void ResetSystemTimeZone ();
 	public static NSTimeZone DefaultTimeZone {
 		get;
 		set;
 	}
 	public static NSTimeZone LocalTimeZone {
 		get;
 		set;
 	}
 	public static NSTimeZone SystemTimeZone {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSUrl</h4>
<p>Added:</p><pre>
 	public override string ToString ();
</pre>
<h4>Type Changed: MonoTouch.Foundation.NSValue</h4>
<p>Added:</p><pre>
 	public static NSValue FromCATransform3D (MonoTouch.CoreAnimation.CATransform3D transform);
 	public virtual MonoTouch.CoreAnimation.CATransform3D CATransform3DValue {
 		get;
 	}
</pre>
<h3>Namespace: MonoTouch.GameKit</h3>
<h4>New Type: MonoTouch.GameKit.GKAchievement</h4>
<pre>
public class GKAchievement : MonoTouch.Foundation.NSObject {
	
	public GKAchievement ();
	public GKAchievement (MonoTouch.Foundation.NSCoder coder);
	public GKAchievement (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievement (IntPtr handle);
	public GKAchievement (string identifier);
	
	public static void LoadAchievements (GKCompletionHandler completionHandler);
	public virtual void ReportAchievement (GKNotificationHandler handler);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Completed {
		get;
		set;
	}
	public virtual string Identifier {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDate LastReportedDate {
		get;
		set;
	}
	public virtual double PercentComplete {
		get;
		set;
	}
	public virtual int Points {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKAchievementDescription</h4>
<pre>
public class GKAchievementDescription : MonoTouch.Foundation.NSObject {
	
	public GKAchievementDescription ();
	public GKAchievementDescription (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementDescription (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementDescription (IntPtr handle);
	
	public static void LoadAchievementDescriptions (GKAchievementDescriptionHandler handler);
	public virtual void LoadImage (GKImageLoadedHandler imageLoadedHandler);
	
	public static MonoTouch.UIKit.UIImage PlaceholderCompletedAchievementImage {
		get;
	}
	public virtual string AchievedDescription {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Identifier {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIImage Image {
		get;
		set;
	}
	public virtual MonoTouch.UIKit.UIImage IncompleteAchievementImage {
		get;
	}
	public virtual int MaximumPoints {
		get;
		set;
	}
	public virtual bool ShouldDisplayIfNotStarted {
		get;
		set;
	}
	public virtual string Title {
		get;
		set;
	}
	public virtual string UnachievedDescription {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKAchievementDescriptionHandler</h4>
<pre>
[Serializable]
public delegate void GKAchievementDescriptionHandler (GKAchievementDescription[] descriptions, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKAchievementViewController</h4>
<pre>
public class GKAchievementViewController : MonoTouch.UIKit.UINavigationController {
	
	public GKAchievementViewController ();
	public GKAchievementViewController (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementViewController (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementViewController (IntPtr handle);
	
	public virtual void SetDelegate (GKAchievementViewControllerDelegate target);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKAchievementViewControllerDelegate</h4>
<pre>
public class GKAchievementViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public GKAchievementViewControllerDelegate ();
	public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKAchievementViewControllerDelegate (IntPtr handle);
	
	public virtual void DidPressDismiss ();
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKCompletionHandler</h4>
<pre>
[Serializable]
public delegate void GKCompletionHandler (GKAchievement[] achivements, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKDataEventArgs</h4>
<pre>
public class GKDataEventArgs : EventArgs {
	
	public GKDataEventArgs (MonoTouch.Foundation.NSData data, GKPlayer player);
	
	public MonoTouch.Foundation.NSData Data {
		get;
		set;
	}
	public GKPlayer Player {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKError</h4>
<pre>
[Serializable]
public enum GKError {
	Unknown,
	Cancelled,
	CommunicationsFailure,
	UserDenied,
	InvalidCredentials,
	NotAuthenticated,
	InvalidPlayer,
	ScoreNotSet,
	ParentalControlsBlocked,
	PlayerStatusExceedsMaximumLength,
	PlayerStatusInvalid,
	MatchRequestInvalid,
	FeatureNotAvailableInPreview
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKErrorEventArgs</h4>
<pre>
public class GKErrorEventArgs : EventArgs {
	
	public GKErrorEventArgs (MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKFriendsHandler</h4>
<pre>
[Serializable]
public delegate void GKFriendsHandler (GKPlayer[] friends, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKImageLoadedHandler</h4>
<pre>
[Serializable]
public delegate void GKImageLoadedHandler (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKInvite</h4>
<pre>
public class GKInvite : MonoTouch.Foundation.NSObject {
	
	public GKInvite ();
	public GKInvite (MonoTouch.Foundation.NSCoder coder);
	public GKInvite (MonoTouch.Foundation.NSObjectFlag t);
	public GKInvite (IntPtr handle);
	
	public virtual bool Cancelled {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool Hosted {
		get;
	}
	public virtual GKPlayer Inviter {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKInviteHandler</h4>
<pre>
[Serializable]
public delegate void GKInviteHandler (GKInvite invite);
</pre>
<h4>New Type: MonoTouch.GameKit.GKLeaderboard</h4>
<pre>
public class GKLeaderboard : MonoTouch.Foundation.NSObject {
	
	public GKLeaderboard ();
	public GKLeaderboard (MonoTouch.Foundation.NSCoder coder);
	public GKLeaderboard (MonoTouch.Foundation.NSObjectFlag t);
	public GKLeaderboard (IntPtr handle);
	public GKLeaderboard (GKPlayer[] players);
	
	public virtual void LoadScores (GKScoresLoadedHandler scoresLoadedHandler);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GKScore LocalPlayerScore {
		get;
	}
	public virtual int MaxRange {
		get;
	}
	public virtual GKLeaderboardPlayerScope PlayerScope {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSRange Range {
		get;
		set;
	}
	public virtual GKScore[] Scores {
		get;
	}
	public virtual GKLeaderboardTimeScope TimeScope {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKLeaderboardPlayerScope</h4>
<pre>
[Serializable]
public enum GKLeaderboardPlayerScope {
	Global,
	FriendsOnly
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKLeaderboardTimeScope</h4>
<pre>
[Serializable]
public enum GKLeaderboardTimeScope {
	Today,
	Week,
	AllTime
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKLeaderboardViewController</h4>
<pre>
public class GKLeaderboardViewController : MonoTouch.UIKit.UINavigationController {
	
	public GKLeaderboardViewController ();
	public GKLeaderboardViewController (MonoTouch.Foundation.NSCoder coder);
	public GKLeaderboardViewController (MonoTouch.Foundation.NSObjectFlag t);
	public GKLeaderboardViewController (IntPtr handle);
	public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);
	
	public virtual void SetLeaderboardDelegate (GKLeaderboardViewController ldel);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate</h4>
<pre>
public class GKLeaderboardViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public GKLeaderboardViewControllerDelegate ();
	public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKLeaderboardViewControllerDelegate (IntPtr handle);
	
	public virtual void LeaderboardDidPressDismiss ();
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKLocalPlayer</h4>
<pre>
public class GKLocalPlayer : GKPlayer {
	
	public GKLocalPlayer ();
	public GKLocalPlayer (MonoTouch.Foundation.NSCoder coder);
	public GKLocalPlayer (MonoTouch.Foundation.NSObjectFlag t);
	public GKLocalPlayer (IntPtr handle);
	
	public virtual void Authenticate (GKNotificationHandler handler);
	public virtual void LoadFriends (GKFriendsHandler handler);
	public virtual void SetStatus (string status, GKNotificationHandler errorHandler);
	
	public virtual bool Authenticated {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual GKPlayer[] Friends {
		get;
	}
	public virtual GKLocalPlayer LocalPlayer {
		get;
	}
	public virtual string Status {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatch</h4>
<pre>
public class GKMatch : MonoTouch.Foundation.NSObject {
	
	public GKMatch ();
	public GKMatch (MonoTouch.Foundation.NSCoder coder);
	public GKMatch (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatch (IntPtr handle);
	
	public virtual void Disconnect ();
	public virtual bool SendData (MonoTouch.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, MonoTouch.Foundation.NSError error);
	public virtual bool SendDataToAllPlayerswithDataModeerror (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, IntPtr ptrToNSErrorHandle);
	public virtual GKVoiceChat VoiceChatWithName (string name);
	
	public override IntPtr ClassHandle {
		get;
	}
	public GKMatchDelegate Delegate {
		get;
		set;
	}
	public virtual int ExpectedPlayerCount {
		get;
	}
	public virtual GKPlayer[] Players {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler<gkplayererroreventargs> ConnectionFailed;
	public event EventHandler<gkdataeventargs> DataReceived;
	public event EventHandler<gkerroreventargs> Failed;
	public event EventHandler<gkstateeventargs> StateChanged;
}
</gkstateeventargs></gkerroreventargs></gkdataeventargs></gkplayererroreventargs></pre>
<h4>New Type: MonoTouch.GameKit.GKMatchDelegate</h4>
<pre>
public abstract class GKMatchDelegate : MonoTouch.Foundation.NSObject {
	
	public GKMatchDelegate ();
	public GKMatchDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKMatchDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchDelegate (IntPtr handle);
	
	public abstract void ConnectionFailed (GKMatch match, GKPlayer player, MonoTouch.Foundation.NSError error);
	public abstract void DataReceived (GKMatch match, MonoTouch.Foundation.NSData data, GKPlayer player);
	public abstract void Failed (GKMatch match, MonoTouch.Foundation.NSError error);
	public abstract void StateChanged (GKMatch match, GKPlayer player, GKPlayerConnectionState state);
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatchEventArgs</h4>
<pre>
public class GKMatchEventArgs : EventArgs {
	
	public GKMatchEventArgs (GKMatch match);
	
	public GKMatch Match {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatchmaker</h4>
<pre>
public class GKMatchmaker : MonoTouch.Foundation.NSObject {
	
	public GKMatchmaker ();
	public GKMatchmaker (MonoTouch.Foundation.NSCoder coder);
	public GKMatchmaker (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchmaker (IntPtr handle);
	
	public virtual void AddPlayers (GKMatch toMatch, GKMatchRequest matchRequest, GKNotificationHandler completionHandler);
	public virtual void Cancel ();
	public virtual void CreateMatch (GKMatchRequest request, GKNotificationMatch completionHandler);
	public virtual void FindPlayers (GKMatchRequest request, GKFriendsHandler handler);
	public virtual void QueryPlayerGroupActivity (int playerGroup, GKQueryHandler handler);
	public virtual void SetInviteHandler (GKInviteHandler handler);
	
	public static GKMatchmaker SharedMatchmaker {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatchmakerViewController</h4>
<pre>
public class GKMatchmakerViewController : MonoTouch.UIKit.UIViewController {
	
	public GKMatchmakerViewController ();
	public GKMatchmakerViewController (MonoTouch.Foundation.NSCoder coder);
	public GKMatchmakerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchmakerViewController (IntPtr handle);
	public GKMatchmakerViewController (GKMatchRequest request);
	public GKMatchmakerViewController (GKMatchRequest request, GKPlayer[] players);
	public GKMatchmakerViewController (GKInvite invite);
	
	public virtual void SetHostedPlayerReady (GKPlayer player);
	
	public override IntPtr ClassHandle {
		get;
	}
	public GKMatchmakerViewControllerDelegate Delegate {
		get;
		set;
	}
	public virtual bool Hosted {
		get;
		set;
	}
	public virtual GKMatchRequest MatchRequest {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler Cancelled;
	public event EventHandler<gkerroreventargs> Failed;
	public event EventHandler<gkmatcheventargs> MatchCreated;
	public event EventHandler<gkplayerseventargs> PlayersFound;
}
</gkplayerseventargs></gkmatcheventargs></gkerroreventargs></pre>
<h4>New Type: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate</h4>
<pre>
public abstract class GKMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public GKMatchmakerViewControllerDelegate ();
	public GKMatchmakerViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKMatchmakerViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchmakerViewControllerDelegate (IntPtr handle);
	
	public abstract void Cancelled (GKMatchmakerViewController viewController);
	public abstract void Failed (GKMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
	public abstract void MatchCreated (GKMatchmakerViewController viewController, GKMatch match);
	public abstract void PlayersFound (GKMatchmakerViewController viewController, GKPlayer[] players);
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatchRequest</h4>
<pre>
public class GKMatchRequest : MonoTouch.Foundation.NSObject {
	
	public GKMatchRequest ();
	public GKMatchRequest (MonoTouch.Foundation.NSCoder coder);
	public GKMatchRequest (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchRequest (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int MaxPlayers {
		get;
		set;
	}
	public virtual int PlayerGroup {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKMatchSendDataMode</h4>
<pre>
[Serializable]
public enum GKMatchSendDataMode {
	Reliable,
	Unreliable
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKNotificationHandler</h4>
<pre>
[Serializable]
public delegate void GKNotificationHandler (MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKNotificationMatch</h4>
<pre>
[Serializable]
public delegate void GKNotificationMatch (GKMatch match, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKPlayer</h4>
<pre>
public class GKPlayer : MonoTouch.Foundation.NSObject {
	
	public GKPlayer ();
	public GKPlayer (MonoTouch.Foundation.NSCoder coder);
	public GKPlayer (MonoTouch.Foundation.NSObjectFlag t);
	public GKPlayer (IntPtr handle);
	
	public virtual string Alias {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool IsFriend {
		get;
	}
	public virtual string PlayerID {
		get;
	}
	public virtual string Status {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKPlayerConnectionState</h4>
<pre>
[Serializable]
public enum GKPlayerConnectionState {
	Unknown,
	Connected,
	Disconnected
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKPlayerErrorEventArgs</h4>
<pre>
public class GKPlayerErrorEventArgs : EventArgs {
	
	public GKPlayerErrorEventArgs (GKPlayer player, MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
	public GKPlayer Player {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKPlayersEventArgs</h4>
<pre>
public class GKPlayersEventArgs : EventArgs {
	
	public GKPlayersEventArgs (GKPlayer[] players);
	
	public GKPlayer[] Players {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKQueryHandler</h4>
<pre>
[Serializable]
public delegate void GKQueryHandler (int activity, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKScore</h4>
<pre>
public class GKScore : MonoTouch.Foundation.NSObject {
	
	public GKScore ();
	public GKScore (MonoTouch.Foundation.NSCoder coder);
	public GKScore (MonoTouch.Foundation.NSObjectFlag t);
	public GKScore (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate Date {
		get;
		set;
	}
	public virtual string FormattedValue {
		get;
	}
	public virtual GKPlayer Player {
		get;
	}
	public virtual int Rank {
		get;
	}
	public virtual int Value {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKScoresLoadedHandler</h4>
<pre>
[Serializable]
public delegate void GKScoresLoadedHandler (GKScore[] scoreArray, MonoTouch.Foundation.NSError error);
</pre>
<h4>Type Changed: MonoTouch.GameKit.GKSessionDelegate</h4>
<p>Removed:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public virtual void PeerConnectionFailed (GKSession session, string peerID, MonoTouch.Foundation.NSError error);
</pre>
<h4>New Type: MonoTouch.GameKit.GKStateEventArgs</h4>
<pre>
public class GKStateEventArgs : EventArgs {
	
	public GKStateEventArgs (GKPlayer player, GKPlayerConnectionState state);
	
	public GKPlayer Player {
		get;
		set;
	}
	public GKPlayerConnectionState State {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKVoiceChat</h4>
<pre>
public class GKVoiceChat : MonoTouch.Foundation.NSObject {
	
	public GKVoiceChat ();
	public GKVoiceChat (MonoTouch.Foundation.NSCoder coder);
	public GKVoiceChat (MonoTouch.Foundation.NSObjectFlag t);
	public GKVoiceChat (IntPtr handle);
	
	public virtual void SetMute (bool isMuted, GKPlayer player);
	public virtual void Start ();
	public virtual void Stop ();
	
	public virtual bool Active {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Name {
		get;
	}
	public virtual float Volume {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.GameKit.GKVoiceChatPlayerState</h4>
<pre>
[Serializable]
public enum GKVoiceChatPlayerState {
	Connected,
	Disconnected,
	Speaking,
	Silent
}
</pre>
<h3>Namespace: MonoTouch.MapKit</h3>
<h4>Type Changed: MonoTouch.MapKit.MKAnnotation</h4>
<p>Added:</p><pre>
 		set;
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKAnnotationViewDragState</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKAnnotationViewDragState
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum MKAnnotationViewDragState {
 	None,
 	Starting,
 	Dragging,
 	Canceling,
 	Ending
 }
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKAnnotationViewEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKAnnotationViewEventArgs
</pre>
<p>Added:</p><pre>
 public class MKAnnotationViewEventArgs : EventArgs {
 	
 	public MKAnnotationViewEventArgs (MKAnnotationView view);
 	
 	public MKAnnotationView View {
 		get;
 		set;
 	}
 }
</pre>
<h4>New Type: MonoTouch.MapKit.MKCircle</h4>
<pre>
public class MKCircle : MKShape {
	
	public MKCircle ();
	public MKCircle (MonoTouch.Foundation.NSCoder coder);
	public MKCircle (MonoTouch.Foundation.NSObjectFlag t);
	public MKCircle (IntPtr handle);
	
	public static MKCircle Circle (MonoTouch.CoreLocation.CLLocationCoordinate2D withcenterCoordinate, double radius);
	public static MKCircle CircleWithMapRect (MKMapRect mapRect);
	
	public virtual MKMapRect BoundingMap {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
		get;
	}
	public virtual double Radius {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKCircleView</h4>
<pre>
public class MKCircleView : MKOverlayPathView {
	
	public MKCircleView ();
	public MKCircleView (MonoTouch.Foundation.NSCoder coder);
	public MKCircleView (MonoTouch.Foundation.NSObjectFlag t);
	public MKCircleView (IntPtr handle);
	public MKCircleView (MKCircle circle);
	
	public virtual MKCircle Circle {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKMapPoint</h4>
<pre>
public struct MKMapPoint {
	
	public MKMapPoint (double x, double y);
	
	public override bool Equals (object other);
	public override int GetHashCode ();
	
	public static bool operator == (MKMapPoint a, MKMapPoint b);
	public static bool operator != (MKMapPoint a, MKMapPoint b);
	
	public double X;
	public double Y;
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKMapRect</h4>
<pre>
public struct MKMapRect {
	
	public MKMapRect (MKMapPoint origin, MKMapSize size);
	public MKMapRect (double x, double y, double width, double height);
	
	public double Height {
		get;
	}
	public bool IsEmpty {
		get;
	}
	public bool IsNull {
		get;
	}
	public double MaxX {
		get;
	}
	public double MaxY {
		get;
	}
	public double MidX {
		get;
	}
	public double MidY {
		get;
	}
	public double MinX {
		get;
	}
	public double MinY {
		get;
	}
	public double Width {
		get;
	}
	
	public MKMapPoint Origin;
	public MKMapSize Size;
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKMapSize</h4>
<pre>
public struct MKMapSize {
	
	public MKMapSize (double width, double height);
	
	public double Width;
	public double Height;
}
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKMapView</h4>
<p>Added:</p><pre>
 	public virtual void AddOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual void AddOverlays (MonoTouch.Foundation.NSObject[] overlays);
 	public virtual void ExchangeOverlays (int index1, int index2);
 	public virtual void InsertOverlay (MonoTouch.Foundation.NSObject overlay, int index);
 	public virtual void InsertOverlayAbove (MonoTouch.Foundation.NSObject overlay, MonoTouch.Foundation.NSObject sibling);
 	public virtual void InsertOverlayBelow (MonoTouch.Foundation.NSObject overlay, MonoTouch.Foundation.NSObject sibling);
 	public virtual MKMapRect MapRectThatFits (MKMapRect mapRect);
 	public virtual MKMapRect MapRectThatFits (MKMapRect mapRect, MonoTouch.UIKit.UIEdgeInsets edgePadding);
 	public virtual void RemoveOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual void RemoveOverlays (MonoTouch.Foundation.NSObject[] overlays);
 	public virtual void SetVisibleMapRect (MKMapRect mapRect, bool animate);
 	public virtual void SetVisibleMapRect (MKMapRect mapRect, MonoTouch.UIKit.UIEdgeInsets edgePadding, bool animate);
 	public virtual MKOverlayView ViewForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public MKMapViewOverlay GetViewForOverlay {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSObject[] Overlays {
 		get;
 	}
 	public virtual MKMapRect visibleMapRect {
 		get;
 		set;
 	}
 	public event EventHandler&lt;MKMapViewDragStateEventArgs&gt; ChangedDragState;
 	public event EventHandler&lt;MKOverlayViewsEventArgs&gt; DidAddOverlayViews;
 	public event EventHandler&lt;MKAnnotationViewEventArgs&gt; DidDeselectAnnotationView;
 	public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; DidFailToLocateUser;
 	public event EventHandler&lt;MKAnnotationViewEventArgs&gt; DidSelectAnnotationView;
 	public event EventHandler DidStopLocatingUser;
 	public event EventHandler&lt;MKUserLocationEventArgs&gt; DidUpdateUserLocation;
 	public event EventHandler WillStartLocatingUser;
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h4>
<p>Added:</p><pre>
 	public virtual void ChangedDragState (MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);
 	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	public virtual void DidDeselectAnnotationView (MKMapView mapView, MKAnnotationView view);
 	public virtual void DidFailToLocateUser (MKMapView mapView, MonoTouch.Foundation.NSError error);
 	public virtual void DidSelectAnnotationView (MKMapView mapView, MKAnnotationView view);
 	public virtual void DidStopLocatingUser (MKMapView mapView);
 	public virtual void DidUpdateUserLocation (MKMapView mapView, MKUserLocation userLocation);
 	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
 	public virtual void WillStartLocatingUser (MKMapView mapView);
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKMapViewDragStateEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKMapViewDragStateEventArgs
</pre>
<p>Added:</p><pre>
 public class MKMapViewDragStateEventArgs : EventArgs {
 	
 	public MKMapViewDragStateEventArgs (MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);
 	
 	public MKAnnotationView AnnotationView {
 		get;
 		set;
 	}
 	public MKAnnotationViewDragState NewState {
 		get;
 		set;
 	}
 	public MKAnnotationViewDragState OldState {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKMapViewOverlay</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKMapViewOverlay
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate MKOverlayView MKMapViewOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<h4>New Type: MonoTouch.MapKit.MKMultiPoint</h4>
<pre>
public class MKMultiPoint : MKShape {
	
	public MKMultiPoint ();
	public MKMultiPoint (MonoTouch.Foundation.NSCoder coder);
	public MKMultiPoint (MonoTouch.Foundation.NSObjectFlag t);
	public MKMultiPoint (IntPtr handle);
	
	public MonoTouch.CoreLocation.CLLocationCoordinate2D[] GetCoordinates (int first, int count);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int PointCount {
		get;
	}
	public MKMapPoint[] Points {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKOverlayPathView</h4>
<pre>
public class MKOverlayPathView : MKOverlayView {
	
	public MKOverlayPathView ();
	public MKOverlayPathView (MonoTouch.Foundation.NSCoder coder);
	public MKOverlayPathView (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlayPathView (IntPtr handle);
	
	public virtual void ApplyFillProperties (MonoTouch.CoreGraphics.CGContext context, float zoomScale);
	public virtual void ApplyStrokeProperties (MonoTouch.CoreGraphics.CGContext context, float zoomScale);
	public virtual void CreatePath ();
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
	public virtual MonoTouch.CoreGraphics.CGLineCap Linecap {
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
<h4>New Type: MonoTouch.MapKit.MKOverlayView</h4>
<pre>
public class MKOverlayView : MonoTouch.UIKit.UIView {
	
	public MKOverlayView ();
	public MKOverlayView (MonoTouch.Foundation.NSCoder coder);
	public MKOverlayView (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlayView (IntPtr handle);
	public MKOverlayView (MonoTouch.Foundation.NSObject overlay);
	
	public static float MKRoadWidthAtZoomScale (float zoomScale);
	public virtual bool CanDrawMapRect (MKMapRect mapRect, float zoomScale);
	public virtual void DrawMapRect (MKMapRect mapRect, float zoomScale, MonoTouch.CoreGraphics.CGContext context);
	public virtual MKMapPoint MapPointForPoint (System.Drawing.PointF point);
	public virtual MKMapRect MapRectForRect (System.Drawing.RectangleF rect);
	public virtual System.Drawing.PointF PointForMapPoint (MKMapPoint mapPoint);
	public virtual System.Drawing.RectangleF RectForMapRect (MKMapRect mapRect);
	public virtual void SetNeedsDisplay (MKMapRect mapRect);
	public virtual void SetNeedsDisplay (MKMapRect mapRect, float zoomScale);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject Overlay {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKOverlayViewsEventArgs</h4>
<pre>
public class MKOverlayViewsEventArgs : EventArgs {
	
	public MKOverlayViewsEventArgs (MKOverlayView overlayViews);
	
	public MKOverlayView OverlayViews {
		get;
		set;
	}
}
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKPinAnnotationView</h4>
<p>Added:</p><pre>
 	public virtual bool Draggable {
 		get;
 		set;
 	}
 	public virtual MKAnnotationViewDragState DragState {
 		get;
 		set;
 	}
</pre>
<h4>New Type: MonoTouch.MapKit.MKPointAnnotation</h4>
<pre>
public class MKPointAnnotation : MKShape {
	
	public MKPointAnnotation ();
	public MKPointAnnotation (MonoTouch.Foundation.NSCoder coder);
	public MKPointAnnotation (MonoTouch.Foundation.NSObjectFlag t);
	public MKPointAnnotation (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKPolygon</h4>
<pre>
public class MKPolygon : MKMultiPoint {
	
	public MKPolygon ();
	public MKPolygon (MonoTouch.Foundation.NSCoder coder);
	public MKPolygon (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolygon (IntPtr handle);
	
	public static MKPolygon _FromPoints (IntPtr points, int count, MKPolygon[] interiorPolygons);
	public static MKPolygon FromCoordinates (MonoTouch.CoreLocation.CLLocationCoordinate2D[] coords);
	public static MKPolygon FromCoordinates (MonoTouch.CoreLocation.CLLocationCoordinate2D[] coords, MKPolygon[] interiorPolygons);
	public static MKPolygon FromPoints (MKMapPoint[] points);
	public static MKPolygon FromPoints (MKMapPoint[] points, MKPolygon[] interiorPolygons);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolygon InteriorPolygons {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKPolygonView</h4>
<pre>
public class MKPolygonView : MKOverlayPathView {
	
	public MKPolygonView ();
	public MKPolygonView (MonoTouch.Foundation.NSCoder coder);
	public MKPolygonView (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolygonView (IntPtr handle);
	public MKPolygonView (MKPolygon polygon);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolygon Polygon {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKPolyline</h4>
<pre>
public class MKPolyline : MKMultiPoint {
	
	public MKPolyline ();
	public MKPolyline (MonoTouch.Foundation.NSCoder coder);
	public MKPolyline (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolyline (IntPtr handle);
	
	public static MKPolyline FromCoordinates (MonoTouch.CoreLocation.CLLocationCoordinate2D[] coords);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKPolylineView</h4>
<pre>
public class MKPolylineView : MKOverlayPathView {
	
	public MKPolylineView ();
	public MKPolylineView (MonoTouch.Foundation.NSCoder coder);
	public MKPolylineView (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolylineView (IntPtr handle);
	public MKPolylineView (MKPolyline polyline);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolyline Polyline {
		get;
	}
}
</pre>
<h4>New Type: MonoTouch.MapKit.MKShape</h4>
<pre>
public class MKShape : MonoTouch.Foundation.NSObject {
	
	public MKShape ();
	public MKShape (MonoTouch.Foundation.NSCoder coder);
	public MKShape (MonoTouch.Foundation.NSObjectFlag t);
	public MKShape (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Subtitle {
		get;
		set;
	}
	public virtual string Title {
		get;
		set;
	}
}
</pre>
<h4>Type Changed: MonoTouch.MapKit.MKUserLocationEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKUserLocationEventArgs
</pre>
<p>Added:</p><pre>
 public class MKUserLocationEventArgs : EventArgs {
 	
 	public MKUserLocationEventArgs (MKUserLocation userLocation);
 	
 	public MKUserLocation UserLocation {
 		get;
 		set;
 	}
 }
</pre>
<h3>Namespace: MonoTouch.MediaPlayer</h3>
<h4>Type Changed: MonoTouch.MediaPlayer.ItemsPickedEventArgs</h4>
<p>Added:</p><pre>
 		set;
</pre>
<h4>Type Changed: MonoTouch.MediaPlayer.MPMediaItem</h4>
<p>Added:</p><pre>
 	public virtual void EnumerateValues (MonoTouch.Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);
</pre>
<h4>Type Changed: MonoTouch.MediaPlayer.MPMediaItemEnumerator</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.MediaPlayer.MPMediaItemEnumerator
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate void MPMediaItemEnumerator (string property, MonoTouch.Foundation.NSObject value, ref bool stop);
</pre>
<h4>Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty</h4>
<p>Added:</p><pre>
 	public const string BeatsPerMinute = "beatsPerMinute";
 	public const string Comments = "comments";
 	public const string AssetUrl = "assetURL";
 	public const string ReleaseDate = "releaseDate";
 	public const string UserGrouping = "userGrouping";
</pre>
<h4>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h4>
<p>Added:</p><pre>
 	public virtual MPTimedMetadata[] TimedMetadata {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.MediaPlayer.MPTimedMetadata</h4>
<pre>
public class MPTimedMetadata : MonoTouch.Foundation.NSObject {
	
	public MPTimedMetadata ();
	public MPTimedMetadata (MonoTouch.Foundation.NSCoder coder);
	public MPTimedMetadata (MonoTouch.Foundation.NSObjectFlag t);
	public MPTimedMetadata (IntPtr handle);
	
	public virtual MonoTouch.Foundation.NSDictionary AllMetadata {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Key {
		get;
	}
	public virtual string Keyspace {
		get;
	}
	public virtual double Timestamp {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject value {
		get;
	}
}
</pre>
<h3>Namespace: MonoTouch.MessageUI</h3>
<h4>New Type: MonoTouch.MessageUI.MessageComposeResult</h4>
<pre>
[Serializable]
public enum MessageComposeResult {
	Cancelled,
	Sent,
	Failed
}
</pre>
<h4>New Type: MonoTouch.MessageUI.MFMessageComposeViewController</h4>
<pre>
public class MFMessageComposeViewController : MonoTouch.UIKit.UINavigationController {
	
	public MFMessageComposeViewController ();
	public MFMessageComposeViewController (MonoTouch.Foundation.NSCoder coder);
	public MFMessageComposeViewController (MonoTouch.Foundation.NSObjectFlag t);
	public MFMessageComposeViewController (IntPtr handle);
	
	public static bool CanSendText {
		get;
	}
	public virtual string Body {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public MFMessageComposeViewControllerDelegate MessageComposeDelegate {
		get;
		set;
	}
	public virtual string [] Recipients {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakMessageComposeDelegate {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate</h4>
<pre>
public abstract class MFMessageComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public MFMessageComposeViewControllerDelegate ();
	public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MFMessageComposeViewControllerDelegate (IntPtr handle);
	
	public abstract void Finished (MFMessageComposeViewController controller, MessageComposeResult result);
}
</pre>
<h3>Namespace: MonoTouch.ObjCRuntime</h3>
<h4>New Type: MonoTouch.ObjCRuntime.BlockDescriptor</h4>
<pre>
public struct BlockDescriptor {
	
	public int reserved;
	public int size;
	public IntPtr copy_helper;
	public IntPtr dispose;
}
</pre>
<h4>New Type: MonoTouch.ObjCRuntime.BlockFlags</h4>
<pre>
[Serializable]
[Flags]
public enum BlockFlags {
	BLOCK_REFCOUNT_MASK,
	BLOCK_NEEDS_FREE,
	BLOCK_HAS_COPY_DISPOSE,
	BLOCK_HAS_CTOR,
	BLOCK_IS_GC,
	BLOCK_IS_GLOBAL,
	BLOCK_HAS_DESCRIPTOR
}
</pre>
<h4>New Type: MonoTouch.ObjCRuntime.BlockLiteral</h4>
<pre>
public struct BlockLiteral {
	
	public void CleanupBlock ();
	public void SetupBlock (Delegate trampoline, Delegate userDelegate);
	
	public IntPtr isa;
	public BlockFlags flags;
	public int reserved;
	public IntPtr invoke;
	public IntPtr block_descriptor;
	public IntPtr local_handle;
	public IntPtr global_handle;
}
</pre>
<h4>Type Changed: MonoTouch.ObjCRuntime.Messaging</h4>
<p>Removed:</p><pre>
 	public static bool Boolean_objc_msgSend_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static bool Boolean_objc_msgSendSuper_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
</pre>
<p>Added:</p><pre>
 	public static bool Boolean_objc_msgSend_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSend_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSend_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool Boolean_objc_msgSendSuper_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSendSuper_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void CMAcceleration_objc_msgSend_stret (out MonoTouch.CoreMotion.CMAcceleration retval, IntPtr receiver, IntPtr selector);
 	public static void CMAcceleration_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMAcceleration retval, IntPtr receiver, IntPtr selector);
 	public static void CMQuaternion_objc_msgSend_stret (out MonoTouch.CoreMotion.CMQuaternion retval, IntPtr receiver, IntPtr selector);
 	public static void CMQuaternion_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMQuaternion retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationMatrix_objc_msgSend_stret (out MonoTouch.CoreMotion.CMRotationMatrix retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationMatrix_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMRotationMatrix retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationRate_objc_msgSend_stret (out MonoTouch.CoreMotion.CMRotationRate retval, IntPtr receiver, IntPtr selector);
 	public static void CMRotationRate_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMRotationRate retval, IntPtr receiver, IntPtr selector);
 	public static void CMTime_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector);
 	public static void CMTime_objc_msgSend_stret_CMTime (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void CMTime_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector);
 	public static void CMTime_objc_msgSendSuper_stret_CMTime (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void CMTimeMapping_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTimeMapping retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeMapping_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTimeMapping retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeRange_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTimeRange retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeRange_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTimeRange retval, IntPtr receiver, IntPtr selector);
 	public static IntPtr IntPtr_objc_msgSend_CATransform3D (IntPtr receiver, IntPtr selector, MonoTouch.CoreAnimation.CATransform3D arg1);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static IntPtr IntPtr_objc_msgSend_CMTime_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8, IntPtr arg9);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.CoreMedia.CMTimeRange arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CATransform3D (IntPtr receiver, IntPtr selector, MonoTouch.CoreAnimation.CATransform3D arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8, IntPtr arg9);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.CoreMedia.CMTimeRange arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void MKMapPoint_objc_msgSend_stret_PointF (out MonoTouch.MapKit.MKMapPoint retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static void MKMapPoint_objc_msgSendSuper_stret_PointF (out MonoTouch.MapKit.MKMapPoint retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static void MKMapRect_objc_msgSend_stret (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector);
 	public static void MKMapRect_objc_msgSend_stret_MKMapRect (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void MKMapRect_objc_msgSend_stret_MKMapRect_UIEdgeInsets (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
 	public static void MKMapRect_objc_msgSend_stret_RectangleF (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1);
 	public static void MKMapRect_objc_msgSendSuper_stret (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector);
 	public static void MKMapRect_objc_msgSendSuper_stret_MKMapRect (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void MKMapRect_objc_msgSendSuper_stret_MKMapRect_UIEdgeInsets (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
 	public static void MKMapRect_objc_msgSendSuper_stret_RectangleF (out MonoTouch.MapKit.MKMapRect retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3);
 	public static void NSRange_objc_msgSend_stret_IntPtr_int_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3);
 	public static void NSRange_objc_msgSendSuper_stret_IntPtr_int_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.Foundation.NSRange arg3);
 	public static System.Drawing.PointF PointF_objc_msgSend_MKMapPoint (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapPoint arg1);
 	public static void PointF_objc_msgSend_stret_MKMapPoint (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapPoint arg1);
 	public static System.Drawing.PointF PointF_objc_msgSendSuper_MKMapPoint (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapPoint arg1);
 	public static void PointF_objc_msgSendSuper_stret_MKMapPoint (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapPoint arg1);
 	public static void RectangleF_objc_msgSend_stret_MKMapRect (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void RectangleF_objc_msgSendSuper_stret_MKMapRect (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void void_objc_msgSend_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGAffineTransform arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSend_CGAffineTransform_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGAffineTransform arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void void_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static void void_objc_msgSend_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static void void_objc_msgSend_CMTimeRange_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSend_Double_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3);
 	public static void void_objc_msgSend_float_CMTime (IntPtr receiver, IntPtr selector, float arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSend_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, float arg1, float arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSend_Int64 (IntPtr receiver, IntPtr selector, long arg1);
 	public static void void_objc_msgSend_IntPtr_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSend_IntPtr_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2);
 	public static void void_objc_msgSend_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
 	public static void void_objc_msgSend_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Double_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static void void_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void void_objc_msgSend_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void void_objc_msgSend_MKMapRect_float_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2, IntPtr arg3);
 	public static void void_objc_msgSend_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSend_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGAffineTransform arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSendSuper_CGAffineTransform_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreGraphics.CGAffineTransform arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void void_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static void void_objc_msgSendSuper_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static void void_objc_msgSendSuper_CMTimeRange_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSendSuper_Double_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, double arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_float_CMTime (IntPtr receiver, IntPtr selector, float arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSendSuper_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, float arg1, float arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSendSuper_Int64 (IntPtr receiver, IntPtr selector, long arg1);
 	public static void void_objc_msgSendSuper_IntPtr_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, int arg3, IntPtr arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_IntPtr_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2);
 	public static void void_objc_msgSendSuper_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
 	public static void void_objc_msgSendSuper_IntPtr_int_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static void void_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void void_objc_msgSendSuper_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_float_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSendSuper_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
</pre>
<h4>New Type: MonoTouch.ObjCRuntime.SinceAttribute</h4>
<pre>
public class SinceAttribute : Attribute {
	
	public SinceAttribute (byte major, byte minor);
	
	public byte Major;
	public byte Minor;
}
</pre>
<h3>Namespace: MonoTouch.QuickLook</h3>
<h4>New Type: MonoTouch.QuickLook.QLOpenUrl</h4>
<pre>
[Serializable]
public delegate bool QLOpenUrl (QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
</pre>
<h4>New Type: MonoTouch.QuickLook.QLPreviewController</h4>
<pre>
public class QLPreviewController : MonoTouch.UIKit.UIViewController {
	
	public QLPreviewController ();
	public QLPreviewController (MonoTouch.Foundation.NSCoder coder);
	public QLPreviewController (MonoTouch.Foundation.NSObjectFlag t);
	public QLPreviewController (IntPtr handle);
	
	public static bool CanPreviewItem (QLPreviewItem item);
	public virtual void RefreshCurrentPreviewItem ();
	public virtual void ReloadData ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual QLPreviewItem CurrentPreviewItem {
		get;
	}
	public virtual int CurrentPreviewItemIndex {
		get;
		set;
	}
	public QLPreviewControllerDataSource DataSource {
		get;
		set;
	}
	public QLPreviewControllerDelegate Delegate {
		get;
		set;
	}
	public QLOpenUrl ShouldOpenUrl {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDataSource {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler DidDismiss;
	public event EventHandler WillDismiss;
}
</pre>
<h4>New Type: MonoTouch.QuickLook.QLPreviewControllerDataSource</h4>
<pre>
public abstract class QLPreviewControllerDataSource : MonoTouch.Foundation.NSObject {
	
	public QLPreviewControllerDataSource ();
	public QLPreviewControllerDataSource (MonoTouch.Foundation.NSCoder coder);
	public QLPreviewControllerDataSource (MonoTouch.Foundation.NSObjectFlag t);
	public QLPreviewControllerDataSource (IntPtr handle);
	
	public abstract QLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
	public abstract int PreviewItemCount (QLPreviewController controller);
}
</pre>
<h4>New Type: MonoTouch.QuickLook.QLPreviewControllerDelegate</h4>
<pre>
public class QLPreviewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public QLPreviewControllerDelegate ();
	public QLPreviewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public QLPreviewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public QLPreviewControllerDelegate (IntPtr handle);
	
	public virtual void DidDismiss (QLPreviewController controller);
	public virtual bool ShouldOpenUrl (QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
	public virtual void WillDismiss (QLPreviewController controller);
}
</pre>
<h4>New Type: MonoTouch.QuickLook.QLPreviewItem</h4>
<pre>
public abstract class QLPreviewItem : MonoTouch.Foundation.NSObject {
	
	public QLPreviewItem ();
	public QLPreviewItem (MonoTouch.Foundation.NSCoder coder);
	public QLPreviewItem (MonoTouch.Foundation.NSObjectFlag t);
	public QLPreviewItem (IntPtr handle);
	
	public abstract string ItemTitle {
		get;
	}
	public abstract MonoTouch.Foundation.NSUrl ItemUrl {
		get;
	}
}
</pre>
<h3>Namespace: MonoTouch.StoreKit</h3>
<h4>Type Changed: MonoTouch.StoreKit.SKPaymentTransactionObserver</h4>
<p>Removed:</p><pre>
 	public virtual void RemovedTransactions (SKPaymentTransaction[] transactions);
 	public virtual void RestoreCompletedTransactionsFailedWithError (MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public virtual void RemovedTransactions (SKPaymentQueue queue, SKPaymentTransaction[] transactions);
 	public virtual void RestoreCompletedTransactionsFailedWithError (SKPaymentQueue queue, MonoTouch.Foundation.NSError error);
</pre>
<h3>Namespace: MonoTouch.UIKit</h3>
<h4>Type Changed: MonoTouch.UIKit.UIActionSheet</h4>
<p>Removed:</p><pre>
 	public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
 	public UIActionSheet (string title, UIActionSheetDelegate del);
 	public UIActionSheet (string title);
 		set;
</pre>
<p>Added:</p><pre>
 	public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
 	public UIActionSheet (string title, UIActionSheetDelegate del);
 	public UIActionSheet (string title);
 	public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
 	public virtual void ShowFrom (UIBarButtonItem item, bool animated);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIAlertView</h4>
<p>Removed:</p><pre>
 	public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
 	public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
 	public virtual void ShowFrom (UIBarButtonItem item);
 	public virtual void ShowFrom (UIBarButtonItem item, bool animated);
 		set;
</pre>
<p>Added:</p><pre>
 	public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIApplication</h4>
<p>Removed:</p><pre>
 	public virtual bool SetStatusBarHidden (bool state, UIStatusBarAnimation animation);
</pre>
<p>Added:</p><pre>
 	public virtual int BeginBackgroundTask (MonoTouch.Foundation.NSAction backgroundTimeExpired);
 	public virtual void BeginReceivingRemoteControlEvents ();
 	public virtual void CancelAllLocalNotifications ();
 	public virtual void CancelLocalNotification (UILocalNotification notification);
 	public virtual void ClearKeepAliveTimeout ();
 	public virtual void EndBackgroundTask (int taskId);
 	public virtual void EndReceivingRemoteControlEvents ();
 	public virtual void PresentLocationNotificationNow (UILocalNotification notification);
 	public virtual void ScheduleLocalNotification (UILocalNotification notification);
 	public virtual bool SetKeepAliveTimout (double timeout, MonoTouch.Foundation.NSAction handler);
 	public virtual void SetStatusBarHidden (bool state, UIStatusBarAnimation animation);
 	public static MonoTouch.Foundation.NSString BackgroundTaskInvalid {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidBecomeActiveNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidChangeStatusBarFrameNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidChangeStatusBarOrientationNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidEnterBackgroundNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidFinishLaunchingNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidReceiveMemoryWarningNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsAnnotationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsLocalNotificationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsLocationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsRemoteNotificationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsSourceApplicationKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LaunchOptionsUrlKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MinimumKeepAliveTimeout {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProtectedDataDidBecomeAvailable {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProtectedDataWillBecomeUnavailable {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SignificantTimeChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StatusBarFrameUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StatusBarOrientationUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillChangeStatusBarFrameNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillChangeStatusBarOrientationNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillEnterForegroundNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillResignActiveNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillTerminateNotification {
 		get;
 	}
 	public virtual UIApplicationState ApplicationState {
 		get;
 	}
 	public virtual double BackgroundTimeRemaining {
 		get;
 	}
 	public virtual bool ProtectedDataAvailable {
 		get;
 		set;
 	}
 	public virtual UILocalNotification[] ScheduledLocalNotifications {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h4>
<p>Added:</p><pre>
 	public virtual void DidEnterBackground (UIApplication application);
 	public virtual void ProtectedDataDidBecomeUnavailable (UIApplication application);
 	public virtual void ProtectedDataWillBecomeUnavailable (UIApplication application);
 	public virtual void ReceivedLocalNotification (UIApplication application, UILocalNotification notification);
 	public virtual void WillEnterForeground (UIApplication application);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIApplicationState</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIApplicationState
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIApplicationState {
 	Active,
 	Inactive,
 	Background
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIBarButtonItem</h4>
<p>Removed:</p><pre>
 	public UIBarButtonItem (UIImage image, UIBarButtonItemStyle style, EventHandler handler);
 	public UIBarButtonItem (string title, UIBarButtonItemStyle style, EventHandler handler);
 	public UIBarButtonItem (UIBarButtonSystemItem systemItem, EventHandler handler);
 	public UIBarButtonItem (UIBarButtonSystemItem systemItem);
</pre>
<p>Added:</p><pre>
 	public UIBarButtonItem (UIImage image, UIBarButtonItemStyle style, EventHandler handler);
 	public UIBarButtonItem (string title, UIBarButtonItemStyle style, EventHandler handler);
 	public UIBarButtonItem (UIBarButtonSystemItem systemItem, EventHandler handler);
 	public UIBarButtonItem (UIBarButtonSystemItem systemItem);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIBarButtonSystemItem</h4>
<p>Removed:</p><pre>
 	Redo
</pre>
<p>Added:</p><pre>
 	Redo,
 	PageCurl
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIBezierPath</h4>
<p>Added:</p><pre>
 	public virtual void AddArc (System.Drawing.PointF center, float radius, float startAngle, float endAngle, bool clockWise);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIButton</h4>
<p>Removed:</p><pre>
 	public virtual UIEdgeInsets imageEdgeInsets {
</pre>
<p>Added:</p><pre>
 	public virtual UIEdgeInsets ImageEdgeInsets {
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIColor</h4>
<p>Added:</p><pre>
 	public void GetHSBA (out float hue, out float saturation, out float brightness, out float alpha);
 	public void GetRGBA (out float red, out float green, out float blue, out float alpha);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIControlState</h4>
<p>Added:</p><pre>
 [Flags]
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIDataDetectorType</h4>
<p>Added:</p><pre>
 	Address,
 	CalendarEvent,
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIDevice</h4>
<p>Removed:</p><pre>
 	public virtual UIUserInterfaceIdiom _UserInterfaceIdiom {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString BatteryLevelDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BatteryStateDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString OrientationDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ProximityStateDidChangeNotification {
 	public bool IsMultitaskingSupported {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIEventSubtype</h4>
<p>Removed:</p><pre>
 	MotionShake
</pre>
<p>Added:</p><pre>
 	MotionShake,
 	RemoteControlPlay,
 	RemoteControlPause,
 	RemoteControlStop,
 	RemoteControlTogglePlayPause,
 	RemoteControlNextTrack,
 	RemoteControlPreviousTrack,
 	RemoteControlBeginSeekingBackward,
 	RemoteControlEndSeekingBackward,
 	RemoteControlBeginSeekingForward,
 	RemoteControlEndSeekingForward
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIEventType</h4>
<p>Removed:</p><pre>
 	Motion
</pre>
<p>Added:</p><pre>
 	Motion,
 	RemoteControl
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIFont</h4>
<p>Added:</p><pre>
 	public override string ToString ();
 	public virtual float LineHeight {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIGestureRecognizer</h4>
<p>Removed:</p><pre>
 	public virtual bool DelaysTouchesBegain {
</pre>
<p>Added:</p><pre>
 	public virtual bool DelaysTouchesBegan {
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIGraphics</h4>
<p>Added:</p><pre>
 	public static void BeginImageContextWithOptions (System.Drawing.SizeF size, bool opaque, float scale);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImage</h4>
<p>Added:</p><pre>
 	public UIImage (string filename);
 	public UIImage (MonoTouch.Foundation.NSData data);
 	public static UIImage FromBundle (string name);
 	public static UIImage FromResource (System.Reflection.Assembly assembly, string name);
 	public UIImage Scale (System.Drawing.SizeF newSize);
 	public virtual float CurrentScale {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImagePickerController</h4>
<p>Added:</p><pre>
 	public static bool IsCameraDeviceAvailable (UIImagePickerControllerCameraDevice cameraDevice);
 	public static bool IsFlashAvailableForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
 	public virtual MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
 	public virtual bool StartVideoCapture ();
 	public virtual bool StopVideoCapture ();
 	public virtual UIImagePickerControllerCameraCaptureMode CameraCaptureMode {
 		get;
 		set;
 	}
 	public virtual UIImagePickerControllerCameraDevice CameraDevice {
 		get;
 		set;
 	}
 	public virtual UIImagePickerControllerCameraFlashMode CameraFlashMode {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIImagePickerControllerCameraCaptureMode {
 	Photo,
 	Video
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraDevice</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIImagePickerControllerCameraDevice
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIImagePickerControllerCameraDevice {
 	Rear,
 	Front
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum UIImagePickerControllerCameraFlashMode {
 	Off,
 	Auto,
 	On
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIImagePickerControllerQualityType</h4>
<p>Removed:</p><pre>
 	Low
</pre>
<p>Added:</p><pre>
 	Low,
 	At640x480
</pre>
<h4>New Type: MonoTouch.UIKit.UILocalNotification</h4>
<pre>
public class UILocalNotification : MonoTouch.Foundation.NSObject {
	
	public UILocalNotification ();
	public UILocalNotification (MonoTouch.Foundation.NSCoder coder);
	public UILocalNotification (MonoTouch.Foundation.NSObjectFlag t);
	public UILocalNotification (IntPtr handle);
	
	public static MonoTouch.Foundation.NSString DefaultSoundName {
		get;
	}
	public virtual string AlertAction {
		get;
		set;
	}
	public virtual string AlertBody {
		get;
		set;
	}
	public virtual string AlertLaunchImage {
		get;
		set;
	}
	public virtual int ApplicationIconBadgeNumber {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate FireDate {
		get;
		set;
	}
	public virtual bool HasAction {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSCalendar RepeatCalendar {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSCalendarUnit RepeatInterval {
		get;
		set;
	}
	public virtual string SoundName {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSTimeZone TimeZone {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary UserInfo {
		get;
		set;
	}
}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UILongPressGestureRecognizer</h4>
<p>Added:</p><pre>
 	public UILongPressGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIMenuController</h4>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString DidHideMenuNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidShowMenuNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillHideMenuNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillShowMenuNotification {
 		get;
 	}
</pre>
<h4>New Type: MonoTouch.UIKit.UINib</h4>
<pre>
public class UINib : MonoTouch.Foundation.NSObject {
	
	public UINib ();
	public UINib (MonoTouch.Foundation.NSCoder coder);
	public UINib (MonoTouch.Foundation.NSObjectFlag t);
	public UINib (IntPtr handle);
	
	public static UINib FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSBundle bundleOrNil);
	public static UINib FromName (string name, MonoTouch.Foundation.NSBundle bundleOrNil);
	public virtual MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer</h4>
<p>Removed:</p><pre>
 	public virtual uint MaximumNumberOfTouchesRequired {
 		get;
 		set;
 	}
 	public virtual uint MinimumNumberOfTouchesRequired {
 		get;
 		set;
 	}
 	public virtual System.Drawing.PointF Translation {
 	public virtual System.Drawing.PointF Velocity {
</pre>
<p>Added:</p><pre>
 	public UIPanGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
 	
 	public virtual void SetTranslation (System.Drawing.PointF translation, UIView view);
 	public virtual System.Drawing.PointF TranslationInView (UIView view);
 	public virtual System.Drawing.PointF VelocityInView (UIView view);
 	public virtual uint MaximumNumberOfTouches {
 	public virtual uint MinimumNumberOfTouches {
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPasteboard</h4>
<p>Removed:</p><pre>
 	public virtual void Remove (string name);
</pre>
<p>Added:</p><pre>
 	public static void Remove (string name);
 	public virtual void AddItems (MonoTouch.Foundation.NSDictionary[] items);
 	public virtual bool Contains (string [] pasteboadTypes, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSData DataForPasteboardType (string pasteboardType);
 	public virtual MonoTouch.Foundation.NSData[] GetDataForPasteboardType (string pasteboardType, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSData[] GetValuesForPasteboardType (string pasteboardType, MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual MonoTouch.Foundation.NSIndexSet ItemSetWithPasteboardTypes (string [] pasteboardTypes);
 	public virtual MonoTouch.Foundation.NSArray[] PasteBoardTypesForSet (MonoTouch.Foundation.NSIndexSet itemSet);
 	public virtual void SetData (MonoTouch.Foundation.NSData data, string forPasteboardType);
 	public static MonoTouch.Foundation.NSString ChangedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ChangedTypesAddedKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ChangedTypesRemovedKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RemovedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSArray TypeListColor {
 		get;
 	}
 	public static MonoTouch.Foundation.NSArray TypeListImage {
 		get;
 	}
 	public static MonoTouch.Foundation.NSArray TypeListString {
 		get;
 	}
 	public static MonoTouch.Foundation.NSArray TypeListURL {
 		get;
 	}
 	public virtual UIColor Color {
 		get;
 		set;
 	}
 	public virtual UIColor[] Colors {
 		get;
 		set;
 	}
 	public virtual UIImage Image {
 		get;
 		set;
 	}
 	public virtual UIImage[] Images {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary[] Items {
 		get;
 		set;
 	}
 	public virtual string String {
 		get;
 		set;
 	}
 	public virtual string [] Strings {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSUrl Url {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSUrl[] Urls {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPickerView</h4>
<p>Added:</p><pre>
 	public UIPickerViewDelegate Delegate {
 		get;
 		set;
 	}
 	public UIPickerViewModel Source {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPickerViewDataSource</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIPickerViewDataSource
</pre>
<p>Added:</p><pre>
 public abstract class UIPickerViewDataSource : MonoTouch.Foundation.NSObject {
 	
 	public UIPickerViewDataSource ();
 	public UIPickerViewDataSource (MonoTouch.Foundation.NSCoder coder);
 	public UIPickerViewDataSource (MonoTouch.Foundation.NSObjectFlag t);
 	public UIPickerViewDataSource (IntPtr handle);
 	
 	public abstract int GetComponentCount (UIPickerView pickerView);
 	public abstract int GetRowsInComponent (UIPickerView pickerView, int component);
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPickerViewDelegate</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIPickerViewDelegate
</pre>
<p>Added:</p><pre>
 public class UIPickerViewDelegate : MonoTouch.Foundation.NSObject {
 	
 	public UIPickerViewDelegate ();
 	public UIPickerViewDelegate (MonoTouch.Foundation.NSCoder coder);
 	public UIPickerViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
 	public UIPickerViewDelegate (IntPtr handle);
 	
 	public virtual float GetComponentWidth (UIPickerView pickerView, int component);
 	public virtual float GetRowHeight (UIPickerView pickerView, int component);
 	public virtual string GetTitle (UIPickerView pickerView, int row, int component);
 	public virtual string GetView (UIPickerView pickerView, int row, int component, UIView view);
 	public virtual void Selected (UIPickerView pickerView, int row, int component);
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPinchGestureRecognizer</h4>
<p>Added:</p><pre>
 	public UIPinchGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIPopoverController</h4>
<p>Added:</p><pre>
 		set;
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIResponder</h4>
<p>Added:</p><pre>
 	public virtual void RemoteControlReceived (UIEvent theEvent);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIRotationGestureRecognizer</h4>
<p>Added:</p><pre>
 	public UIRotationGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIScreen</h4>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreAnimation.CADisplayLink DisplayLink (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector sel);
 	
 	public virtual float Scale {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISearchBar</h4>
<p>Added:</p><pre>
 	public UISearchBarPredicate ShouldBeginEditing {
 		get;
 		set;
 	}
 	public UISearchBarRangeEventArgs ShouldChangeTextInRange {
 		get;
 		set;
 	}
 	public UISearchBarPredicate ShouldEndEditing {
 		get;
 		set;
 	}
 	
 	public event EventHandler BookmarkButtonClicked;
 	public event EventHandler CancelButtonClicked;
 	public event EventHandler ListButtonClicked;
 	public event EventHandler OnEditingStarted;
 	public event EventHandler OnEditingStopped;
 	public event EventHandler SearchButtonClicked;
 	public event EventHandler&lt;UISearchBarTextChangedEventArgs&gt; TextChanged;
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISearchBarPredicate</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarPredicate
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UISearchBarPredicate (UISearchBar searchBar);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISearchBarRangeEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarRangeEventArgs
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UISearchBarRangeEventArgs (UISearchBar searchBar, MonoTouch.Foundation.NSRange range, string text);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISearchBarTextChangedEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UISearchBarTextChangedEventArgs
</pre>
<p>Added:</p><pre>
 public class UISearchBarTextChangedEventArgs : EventArgs {
 	
 	public UISearchBarTextChangedEventArgs (string searchText);
 	
 	public string SearchText {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISegmentedControl</h4>
<p>Removed:</p><pre>
 	public UISegmentedControl (object [] args);
</pre>
<p>Added:</p><pre>
 	public UISegmentedControl (object [] args);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISegmentedControlStyle</h4>
<p>Removed:</p><pre>
 	Bar
</pre>
<p>Added:</p><pre>
 	Bar,
 	Bezeled
</pre>
<h4>Type Changed: MonoTouch.UIKit.UISwipeGestureRecognizer</h4>
<p>Added:</p><pre>
 	public UISwipeGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITabBarController</h4>
<p>Added:</p><pre>
 	public UITabBarSelection ShouldSelectViewController {
 		get;
 		set;
 	}
 	
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; FinishedCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeEventArgs&gt; OnCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarCustomizeChangeEventArgs&gt; OnEndCustomizingViewControllers;
 	public event EventHandler&lt;UITabBarSelectionEventArgs&gt; ViewControllerSelected;
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeChangeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeChangeEventArgs (UIViewController[] viewControllers, bool changed);
 	
 	public bool Changed {
 		get;
 		set;
 	}
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITabBarCustomizeEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarCustomizeEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarCustomizeEventArgs : EventArgs {
 	
 	public UITabBarCustomizeEventArgs (UIViewController[] viewControllers);
 	
 	public UIViewController[] ViewControllers {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITabBarSelection</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelection
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate bool UITabBarSelection (UITabBarController tabBarController, UIViewController viewController);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITabBarSelectionEventArgs</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UITabBarSelectionEventArgs
</pre>
<p>Added:</p><pre>
 public class UITabBarSelectionEventArgs : EventArgs {
 	
 	public UITabBarSelectionEventArgs (UIViewController viewController);
 	
 	public UIViewController ViewController {
 		get;
 		set;
 	}
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITableViewCell</h4>
<p>Removed:</p><pre>
 	public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
</pre>
<p>Added:</p><pre>
 	public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITapGestureRecognizer</h4>
<p>Added:</p><pre>
 	public UITapGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITextField</h4>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString TextDidBeginEditingNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextDidEndEditingNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextFieldTextDidChangeNotification {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UITextView</h4>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString TextDidBeginEditingNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TextDidEndEditingNotification {
 		get;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIView</h4>
<p>Added:</p><pre>
 	public static void Animate (double duration, MonoTouch.Foundation.NSAction animation);
 	public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
 	public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
 	public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
 	public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction completion);
 	public virtual float ContentScaleFactor {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIViewAnimationOptions</h4>
<p>Removed:</p><pre>
 Could not find MonoTouch.UIKit.UIViewAnimationOptions
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum UIViewAnimationOptions {
 	LayoutSubviews,
 	AllowUserInteraction,
 	BeginFromCurrentState,
 	Repeat,
 	Autoreverse,
 	OverrideInheritedDuration,
 	OverrideInheritedCurve,
 	AllowAnimatedContent,
 	ShowHideTransitionViews,
 	CurveEaseInOut,
 	CurveEaseIn,
 	CurveEaseOut,
 	CurveLinear,
 	TransitionNone,
 	TransitionFlipFromLeft,
 	TransitionFlipFromRight,
 	TransitionCurlUp,
 	TransitionCurlDown
 }
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIWebView</h4>
<p>Added:</p><pre>
 	public virtual bool AllowsInlineMediaPlayback {
 		get;
 		set;
 	}
 	public virtual bool MediaPlaybackRequiresUserAction {
 		get;
 		set;
 	}
</pre>
<h4>Type Changed: MonoTouch.UIKit.UIWindow</h4>
<p>Added:</p><pre>
 		set;
</pre>
<h3>Namespace: MonoTouch.iAd</h3>
<h4>New Type: MonoTouch.iAd.AdAction</h4>
<pre>
[Serializable]
public delegate bool AdAction (ADBannerView banner, bool willLeaveApplication);
</pre>
<h4>New Type: MonoTouch.iAd.ADBannerView</h4>
<pre>
public class ADBannerView : MonoTouch.UIKit.UIView {
	
	public ADBannerView ();
	public ADBannerView (MonoTouch.Foundation.NSCoder coder);
	public ADBannerView (MonoTouch.Foundation.NSObjectFlag t);
	public ADBannerView (IntPtr handle);
	
	public static System.Drawing.SizeF SizeFromContentSizeIdentifier (string sizeIdentifier);
	public virtual void CancelBannerViewAction ();
	
	public static MonoTouch.Foundation.NSString SizeIdentifier320x50 {
		get;
	}
	public static MonoTouch.Foundation.NSString SizeIdentifier480x32 {
		get;
	}
	public AdAction ActionShouldBegin {
		get;
		set;
	}
	public virtual string AdvertisingSection {
		get;
		set;
	}
	public virtual bool BannerLoaded {
		get;
	}
	public virtual bool BannerViewActionInProgress {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string CurrentContentSizeIdentifier {
		get;
	}
	public ADBannerViewDelegate Delegate {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSSet RequiredContentSizeIdentifiers {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler ActionFinished;
	public event EventHandler AdLoaded;
	public event EventHandler<aderroreventargs> FailedToReceiveAd;
}
</aderroreventargs></pre>
<h4>New Type: MonoTouch.iAd.ADBannerViewDelegate</h4>
<pre>
public class ADBannerViewDelegate : MonoTouch.Foundation.NSObject {
	
	public ADBannerViewDelegate ();
	public ADBannerViewDelegate (MonoTouch.Foundation.NSCoder coder);
	public ADBannerViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public ADBannerViewDelegate (IntPtr handle);
	
	public virtual void ActionFinished (ADBannerView banner);
	public virtual bool ActionShouldBegin (ADBannerView banner, bool willLeaveApplication);
	public virtual void AdLoaded (ADBannerView banner);
	public virtual void FailedToReceiveAd (ADBannerView banner, MonoTouch.Foundation.NSError error);
}
</pre>
<h4>New Type: MonoTouch.iAd.AdError</h4>
<pre>
[Serializable]
public enum AdError {
	Unknown,
	ServerFailure,
	LoadingThrottled,
	InventoryUnavailable
}
</pre>
<h4>New Type: MonoTouch.iAd.AdErrorEventArgs</h4>
<pre>
public class AdErrorEventArgs : EventArgs {
	
	public AdErrorEventArgs (MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
}
</pre>
<h4>New Type: MonoTouch.iAd.ADManager</h4>
<pre>
public class ADManager : MonoTouch.Foundation.NSObject {
	
	public ADManager ();
	public ADManager (MonoTouch.Foundation.NSCoder coder);
	public ADManager (MonoTouch.Foundation.NSObjectFlag t);
	public ADManager (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
</body>
</html>
