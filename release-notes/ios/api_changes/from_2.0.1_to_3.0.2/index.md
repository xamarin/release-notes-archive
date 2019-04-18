---
id: 59CAC0C4-14FA-4C03-8785-15C34495D253
title: "From 2.0.1 to 3.0.2"
---

<html><head><title>Comparison between monotouch-2.0.1.dll and monotouch-302.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "2.0.1";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.0.0";
 	public const string FoundationLibrary = "/System/Library/Frameworks/Foundation.framework/Foundation";
 	public const string AdLibLibrary = "/System/Library/Frameworks/AdLib.framework/AdLib";
 	public const string CoreTelephonyLibrary = "/System/Library/Frameworks/CoreTelephony.framework/CoreTelephony";
 	public const string CoreMediaLibrary = "/System/Library/Frameworks/CoreMedia.framework/CoreMedia";
 	public const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>New Type: MonoTouch.AVFoundation.AVAsset</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAssetExportSession</h2>
<pre>
public class AVAssetExportSession : MonoTouch.Foundation.NSObject {
	
	public AVAssetExportSession ();
	public AVAssetExportSession (MonoTouch.Foundation.NSCoder coder);
	public AVAssetExportSession (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetExportSession (IntPtr handle);
	public AVAssetExportSession (AVAsset asset, string presetName);
	
	public static string [] ExportPresetsCompatibleWithAsset (AVAsset asset);
	public static string LocalizedNameForExportPreset (string presetName);
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
	public virtual string LocalizedExportSessionOutputSummary {
		get;
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
<h2>New Type: MonoTouch.AVFoundation.AVAssetExportSessionStatus</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAssetReader</h2>
<pre>
public class AVAssetReader : MonoTouch.Foundation.NSObject {
	
	public AVAssetReader ();
	public AVAssetReader (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReader (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReader (IntPtr handle);
	public AVAssetReader (AVAsset asset, IntPtr ptrToHandleToError);
	
	public virtual bool AddOutput (AVAssetReaderOutput output);
	public virtual bool CanAddOutput (AVAssetReaderOutput output);
	public virtual void CancelReading ();
	public virtual AVAssetReader FromAsset (AVAsset asset, IntPtr ptrToHandleToError);
	public virtual void StartReading ();
	
	public virtual AVAsset Asset {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSError Error {
		get;
	}
	public virtual MonoTouch.Foundation.NSArray outputs {
		get;
	}
	public virtual AVAssetReaderStatus Status {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput</h2>
<pre>
public class AVAssetReaderAudioMixOutput : AVAssetReaderOutput {
	
	public AVAssetReaderAudioMixOutput ();
	public AVAssetReaderAudioMixOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderAudioMixOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderAudioMixOutput (IntPtr handle);
	public AVAssetReaderAudioMixOutput (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
	
	public virtual AVAssetReaderAudioMixOutput FromAudioTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
	
	public virtual AVAudioMix AudioMix {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary AudioSettings {
		get;
	}
	public virtual AVAssetTrack[] AudioTracks {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderOutput</h2>
<pre>
public class AVAssetReaderOutput : MonoTouch.Foundation.NSObject {
	
	public AVAssetReaderOutput ();
	public AVAssetReaderOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderOutput (IntPtr handle);
	
	public virtual MonoTouch.CoreMedia.CMSampleBuffer CopyNextSampleBuffer ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string MediaType {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderStatus</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderTrackOutput</h2>
<pre>
public class AVAssetReaderTrackOutput : AVAssetReaderOutput {
	
	public AVAssetReaderTrackOutput ();
	public AVAssetReaderTrackOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderTrackOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderTrackOutput (IntPtr handle);
	public AVAssetReaderTrackOutput (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
	
	public static AVAssetReaderTrackOutput FromAssetTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
	
	public virtual AVAudioMixInputParameters AudioParameters {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary OutputSettings {
		get;
	}
	public virtual AVAssetTrack Track {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderUndecodedTrackOutput</h2>
<pre>
public class AVAssetReaderUndecodedTrackOutput : AVAssetReaderOutput {
	
	public AVAssetReaderUndecodedTrackOutput ();
	public AVAssetReaderUndecodedTrackOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderUndecodedTrackOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderUndecodedTrackOutput (IntPtr handle);
	public AVAssetReaderUndecodedTrackOutput (AVAssetTrack track);
	
	public static AVAssetReaderUndecodedTrackOutput FromTrack (AVAssetTrack track);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVAssetTrack Track {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput</h2>
<pre>
public class AVAssetReaderVideoCompositionOutput : AVAssetReaderOutput {
	
	public AVAssetReaderVideoCompositionOutput ();
	public AVAssetReaderVideoCompositionOutput (MonoTouch.Foundation.NSCoder coder);
	public AVAssetReaderVideoCompositionOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVAssetReaderVideoCompositionOutput (IntPtr handle);
	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
	
	public virtual AVAssetReaderVideoCompositionOutput FromVideoTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVVideoComposition VideoComposition {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
		get;
	}
	public virtual AVAssetTrack[] VideoTracks {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVAssetTrack</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAssetTrackSegment</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAudioMix</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVAudioMixInputParameters</h2>
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
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioPlayer</h2>
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
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate</h2>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioRecorder</h2>
<p>Removed:</p><pre>
 	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
</pre>
<p>Added:</p><pre>
 	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate</h2>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioRecorder recorder, AVAudioSessionInterruptionFlags flags);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioSession</h2>
<p>Added:</p><pre>
 	public bool SetActive (bool beActive, AVAudioSessionFlags flags, out MonoTouch.Foundation.NSError outError);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioSessionDelegate</h2>
<p>Removed:</p><pre>
 	public virtual void CategoryChanged (string category);
 	public virtual void CurrentHardwareInputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareOutputNumberOfChannelsChanged (int numberOfChannels);
 	public virtual void CurrentHardwareSampleRateChanged (double sampleRate);
</pre>
<p>Added:</p><pre>
 	public virtual void EndInterruption (AVAudioSessionInterruptionFlags flags);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioSessionFlags</h2>
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
<h2>Type Changed: MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureAudioChannel</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutput</h2>
<pre>
public class AVCaptureAudioDataOutput : AVCaptureOutput {
	
	public AVCaptureAudioDataOutput ();
	public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAudioDataOutput (IntPtr handle);
	
	public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, IntPtr sampleBufferCallbackDispatchQueue);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual IntPtr SampleBufferCallbackQueue {
		get;
	}
	public virtual AVCaptureAudioDataOutputSampleBufferDelegate SampleBufferDelegate {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate</h2>
<pre>
public class AVCaptureAudioDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
	
	public AVCaptureAudioDataOutputSampleBufferDelegate ();
	public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureAudioDataOutputSampleBufferDelegate (IntPtr handle);
	
	public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureCompletionHandler</h2>
<pre>
[Serializable]
public delegate void AVCaptureCompletionHandler (MonoTouch.CoreMedia.CMSampleBuffer imageDataSampleBuffer, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureConnection</h2>
<pre>
public class AVCaptureConnection : MonoTouch.Foundation.NSObject {
	
	public AVCaptureConnection ();
	public AVCaptureConnection (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureConnection (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureConnection (IntPtr handle);
	
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureDevice</h2>
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
	public virtual bool InUseByAnotherApplication {
		get;
	}
	public virtual string LocalizedName {
		get;
	}
	public virtual string ModelID {
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureDeviceInput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureExposureMode</h2>
<pre>
[Serializable]
public enum AVCaptureExposureMode {
	Locked,
	AutoExpose,
	ContinuousAutoExposure
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureFileOutput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureFlashMode</h2>
<pre>
[Serializable]
public enum AVCaptureFlashMode {
	Off,
	On,
	Auto
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureFocusMode</h2>
<pre>
[Serializable]
public enum AVCaptureFocusMode {
	ModeLocked,
	ModeAutoFocus,
	ModeContinuousAutoFocus
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureInput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureInputPort</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureMovieFileOutput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureOutput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureSession</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h2>
<pre>
public class AVCaptureStillImageOutput : AVCaptureOutput {
	
	public AVCaptureStillImageOutput ();
	public AVCaptureStillImageOutput (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureStillImageOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureStillImageOutput (IntPtr handle);
	
	public virtual void CaptureStillImageAsynchronously (AVCaptureConnection connection, AVCaptureCompletionHandler completionHandler);
	public virtual MonoTouch.Foundation.NSDictionary OutputSettings ();
	
	public virtual string [] AvailableImageDataFormatTypes {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureTorchMode</h2>
<pre>
[Serializable]
public enum AVCaptureTorchMode {
	Off,
	On,
	Auto
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutput</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate</h2>
<pre>
public class AVCaptureVideoDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
	
	public AVCaptureVideoDataOutputSampleBufferDelegate ();
	public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVCaptureVideoDataOutputSampleBufferDelegate (IntPtr handle);
	
	public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureVideoOrientation</h2>
<pre>
[Serializable]
public enum AVCaptureVideoOrientation {
	Portrait,
	PortraitUpsideDown,
	LandscapeLeft,
	LandscapeRight
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCaptureWhiteBalanceMode</h2>
<pre>
[Serializable]
public enum AVCaptureWhiteBalanceMode {
	Locked,
	AutoWhiteBalance
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCompositionTrack</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVCompositionTrackSegment</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVError</h2>
<pre>
[Serializable]
public enum AVError {
	Unknown,
	OutOfMemory,
	UnsupportedOperation,
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
	DeviceExcludedByAnotherDevice,
	DeviceLockedForConfigurationByAnotherProcess,
	SessionWasInterrupted,
	DecodeFailed,
	ExportFailed,
	FileAlreadyExists,
	InvalidSourceMedia,
	ServerDied
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVErrorHandler</h2>
<pre>
[Serializable]
public delegate void AVErrorHandler (MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMetadataItem</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVMutableAudioMix</h2>
<pre>
public class AVMutableAudioMix : AVAudioMix {
	
	public AVMutableAudioMix ();
	public AVMutableAudioMix (MonoTouch.Foundation.NSCoder coder);
	public AVMutableAudioMix (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableAudioMix (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVAudioMixInputParameters[] InputParameters {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters</h2>
<pre>
public class AVMutableAudioMixInputParameters : AVAudioMixInputParameters {
	
	public AVMutableAudioMixInputParameters ();
	public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSCoder coder);
	public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableAudioMixInputParameters (IntPtr handle);
	
	public static AVMutableAudioMixInputParameters MutableAudioMixInputParametersWithTrack (AVAssetTrack track);
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
<h2>New Type: MonoTouch.AVFoundation.AVMutableCompositionTrack</h2>
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
	public virtual AVCompositionTrackSegment[] Segments {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMutableMetadataItem</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVMutableVideoComposition</h2>
<pre>
public class AVMutableVideoComposition : AVVideoComposition {
	
	public AVMutableVideoComposition ();
	public AVMutableVideoComposition (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoComposition (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoComposition (IntPtr handle);
	
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
	public virtual System.Drawing.SizeF RenderSize {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction</h2>
<pre>
public class AVMutableVideoCompositionInstruction : AVVideoCompositionInstruction {
	
	public AVMutableVideoCompositionInstruction ();
	public AVMutableVideoCompositionInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoCompositionInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoCompositionInstruction (IntPtr handle);
	
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
<h2>New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction</h2>
<pre>
public class AVMutableVideoCompositionLayerInstruction : AVVideoCompositionLayerInstruction {
	
	public AVMutableVideoCompositionLayerInstruction ();
	public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSCoder coder);
	public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableVideoCompositionLayerInstruction (IntPtr handle);
	
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
<h2>New Type: MonoTouch.AVFoundation.AVPlayer</h2>
<pre>
public class AVPlayer : MonoTouch.Foundation.NSObject {
	
	public AVPlayer ();
	public AVPlayer (MonoTouch.Foundation.NSCoder coder);
	public AVPlayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayer (IntPtr handle);
	public AVPlayer (MonoTouch.Foundation.NSUrl URL);
	public AVPlayer (AVPlayerItem item);
	public AVPlayer (AVPlayerQueue queue);
	
	public static AVPlayer FromPlayerItem (AVPlayerItem item);
	public static AVPlayer FromPlayerQueue (AVPlayerQueue queue);
	public static AVPlayer FromUrl (MonoTouch.Foundation.NSUrl URL);
	public virtual MonoTouch.Foundation.NSObject AddBoundaryTimeObserver (MonoTouch.Foundation.NSValue[] times, MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSAction handler);
	public virtual MonoTouch.Foundation.NSObject AddPeriodicTimeObserver (MonoTouch.CoreMedia.CMTime interval, MonoTouch.CoreFoundation.DispatchQueue queue, AVTimeHandler handler);
	public virtual void AdvanceToNextItem ();
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
	public virtual bool Muted {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSDictionary PreferredLanguages {
		get;
		set;
	}
	public virtual AVPlayerQueue Queue {
		get;
	}
	public virtual float Rate {
		get;
		set;
	}
	public virtual bool SubtitleDisplayEnabled {
		get;
		set;
	}
	public virtual float Volume {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVPlayerActionAtItemEnd</h2>
<pre>
[Serializable]
public enum AVPlayerActionAtItemEnd {
	Advance,
	Pause,
	None
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVPlayerItem</h2>
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
	public virtual MonoTouch.CoreMedia.CMTime ForwardPlaybackEndTime {
		get;
		set;
	}
	public virtual System.Drawing.SizeF NaturalSize {
		get;
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
<h2>New Type: MonoTouch.AVFoundation.AVPlayerItemStatus</h2>
<pre>
[Serializable]
public enum AVPlayerItemStatus {
	Unknown,
	ReadyToPlay,
	FailedToBecomeReadyToPlay
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVPlayerItemTrack</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVPlayerLayer</h2>
<pre>
public class AVPlayerLayer : MonoTouch.CoreAnimation.CALayer {
	
	public AVPlayerLayer ();
	public AVPlayerLayer (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerLayer (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerLayer (IntPtr handle);
	
	public static AVPlayerLayer FromPlayer (AVPlayer player);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVPlayer Player {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVPlayerQueue</h2>
<pre>
public class AVPlayerQueue : MonoTouch.Foundation.NSObject {
	
	public AVPlayerQueue ();
	public AVPlayerQueue (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerQueue (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerQueue (IntPtr handle);
	public AVPlayerQueue (AVPlayerItem[] array);
	
	public static AVPlayerQueue PlayerQueueWithArray (AVPlayerItem[] array);
	public virtual void BeginModifications ();
	public virtual bool CanInsertItem (AVPlayerItem item, AVPlayerItem afterItem);
	public virtual void Clear ();
	public virtual void CommitModifications ();
	public virtual void InsertItem (AVPlayerItem item, AVPlayerItem afterItem);
	public virtual void RemoveItem (AVPlayerItem item);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVTimeHandler</h2>
<pre>
[Serializable]
public delegate void AVTimeHandler (MonoTouch.CoreMedia.CMTime time);
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVUrlAsset</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVVideoComposition</h2>
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
	public virtual System.Drawing.SizeF RenderSize {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVVideoCompositionCoreAnimationTool</h2>
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
<h2>New Type: MonoTouch.AVFoundation.AVVideoCompositionInstruction</h2>
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
	public virtual AVVideoCompositionLayerInstruction[] LayerInstructions {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction</h2>
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
<h1>Namespace: MonoTouch.AdLib</h1>
<h2>New Type: MonoTouch.AdLib.AdError</h2>
<pre>
[Serializable]
public enum AdError {
	Unknown,
	ServerFailure,
	LoadingThrottled,
	InventoryUnavailable
}
</pre>
<h2>New Type: MonoTouch.AdLib.AdManager</h2>
<pre>
public class AdManager {
	
	public AdManager ();
	
	public static readonly string ModalAdAvailabilityDidChangeNotification;
	public static readonly string ModalAdWasDismissedNotification;
	public static readonly string ErrorRetrievingModalAdNotification;
	public static readonly string ErrorKey;
	public static readonly string ErrorDomain;
}
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h2>Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController</h2>
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
<h2>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSNumber[] _DisplayedProperties {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AddressBookUI.ABPersonViewController</h2>
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
<h2>Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController</h2>
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
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayout</h2>
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
<h2>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayoutTag</h2>
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
<h2>Type Changed: MonoTouch.AudioToolbox.AudioFormatType</h2>
<p>Removed:</p><pre>
 	AES3
</pre>
<p>Added:</p><pre>
 	AES3,
 	MPEG4AAC_ELD
</pre>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioQueueParameter</h2>
<p>Removed:</p><pre>
 	Volume
</pre>
<p>Added:</p><pre>
 	Volume,
 	Pan,
 	VolumeRampTime
</pre>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioSession</h2>
<p>Added:</p><pre>
 	public static AudioSessionInterruptionType InterruptionType {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioSessionInterruptionType</h2>
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
<h2>Type Changed: MonoTouch.AudioToolbox.AudioSessionProperty</h2>
<p>Removed:</p><pre>
 	OverrideCategoryMixWithOthers
</pre>
<p>Added:</p><pre>
 	OverrideCategoryMixWithOthers,
 	InterruptionType
</pre>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>Type Changed: MonoTouch.CoreAnimation.CAAnimation</h2>
<p>Removed:</p><pre>
 	public virtual void DidChangeValueForKey (string key);
 	public virtual void WillChangeValueForKey (string key);
</pre>
<p>Added:</p><pre>
 	public virtual bool ShouldArchiveValueForKey (string key);
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CAGradientLayer</h2>
<p>Removed:</p><pre>
 	public virtual IntPtr _Colors {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual float ContentsScale {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation</h2>
<p>Removed:</p><pre>
 	public virtual IntPtr _Path {
 		get;
 		set;
 	}
 	public virtual string rotationMode {
</pre>
<p>Added:</p><pre>
 	public virtual string RotationMode {
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CALayer</h2>
<p>Removed:</p><pre>
 	public CALayer (CALayer other);
</pre>
<p>Added:</p><pre>
 	public CALayer (CALayer other);
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CATransaction</h2>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSAction CompletionBlock {
 		set;
 	}
</pre>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h2>New Type: MonoTouch.CoreFoundation.DispatchObject</h2>
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
<h2>New Type: MonoTouch.CoreFoundation.DispatchQueue</h2>
<pre>
public class DispatchQueue : DispatchObject {
	
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
<h2>New Type: MonoTouch.CoreFoundation.DispatchQueuePriority</h2>
<pre>
[Serializable]
public enum DispatchQueuePriority {
	High,
	Default,
	Low
}
</pre>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGContext</h2>
<p>Added:</p><pre>
 	public CGPath CopyPath ();
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h2>New Type: MonoTouch.CoreLocation.CLDeviceOrientation</h2>
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
<h2>Type Changed: MonoTouch.CoreLocation.CLError</h2>
<p>Removed:</p><pre>
 	HeadingFailure
</pre>
<p>Added:</p><pre>
 	HeadingFailure,
 	RegionMonitoringDenied,
 	RegionMonitoringFailure,
 	RegionMonitoringSetupDelayed
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationCoordinate2D</h2>
<p>Added:</p><pre>
 	public bool IsValid ();
 	
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h2>
<p>Added:</p><pre>
 	public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
 	public virtual void StartMonitoringSignificantLocationChanges ();
 	public virtual void StopMonitoring (CLRegion region);
 	public virtual void StopMonitoringSignificantLocationChanges ();
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
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h2>
<p>Added:</p><pre>
 	public virtual void MonitoringFailed (CLLocationManager manager, CLRegion region, MonoTouch.Foundation.NSError error);
 	public virtual void RegionEntered (CLLocationManager manager, CLRegion region);
 	public virtual void RegionLeft (CLLocationManager manager, CLRegion region);
</pre>
<h2>New Type: MonoTouch.CoreLocation.CLRegion</h2>
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
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h2>New Type: MonoTouch.CoreMedia.CMSampleBuffer</h2>
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
<h2>New Type: MonoTouch.CoreMedia.CMTime</h2>
<pre>
public struct CMTime {
	
	public long Value;
	public int TimeScale;
	public int TimeFlags;
	public long TimeEpoch;
}
</pre>
<h2>New Type: MonoTouch.CoreMedia.CMTimeMapping</h2>
<pre>
public struct CMTimeMapping {
	
	public CMTime Source;
	public CMTime Target;
}
</pre>
<h2>New Type: MonoTouch.CoreMedia.CMTimeRange</h2>
<pre>
public struct CMTimeRange {
	
	public CMTime Start;
	public CMTime Duration;
}
</pre>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h2>New Type: MonoTouch.CoreTelephony.CTCall</h2>
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
<h2>New Type: MonoTouch.CoreTelephony.CTCallCenter</h2>
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
<h2>New Type: MonoTouch.CoreTelephony.CTCallEventHandler</h2>
<pre>
[Serializable]
public delegate void CTCallEventHandler (CTCall call);
</pre>
<h2>New Type: MonoTouch.CoreTelephony.CTCarrier</h2>
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
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.EventKit</h1>
<h2>New Type: MonoTouch.EventKit.EKAlarm</h2>
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
<h2>New Type: MonoTouch.EventKit.EKCalendar</h2>
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
	public virtual string Title {
		get;
	}
	public virtual EKCalendarType Type {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKCalendarType</h2>
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
<h2>New Type: MonoTouch.EventKit.EKDay</h2>
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
<h2>New Type: MonoTouch.EventKit.EKErrorCode</h2>
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
<h2>New Type: MonoTouch.EventKit.EKEvent</h2>
<pre>
public class EKEvent : MonoTouch.Foundation.NSObject {
	
	public EKEvent ();
	public EKEvent (MonoTouch.Foundation.NSCoder coder);
	public EKEvent (MonoTouch.Foundation.NSObjectFlag t);
	public EKEvent (IntPtr handle);
	
	public static EKEvent Create ();
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
	public virtual string Title {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKEventEditEventArgs</h2>
<pre>
public class EKEventEditEventArgs : EventArgs {
	
	public EKEventEditEventArgs (EKEventEditViewAction action);
	
	public EKEventEditViewAction Action {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKEventEditViewAction</h2>
<pre>
[Serializable]
public enum EKEventEditViewAction {
	Canceled,
	Saved,
	Deleted
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKEventEditViewController</h2>
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
	public virtual EKEvent Event {
		get;
		set;
	}
	public virtual EKEventStore EventStore {
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
<h2>New Type: MonoTouch.EventKit.EKEventEditViewDelegate</h2>
<pre>
public abstract class EKEventEditViewDelegate : MonoTouch.Foundation.NSObject {
	
	public EKEventEditViewDelegate ();
	public EKEventEditViewDelegate (MonoTouch.Foundation.NSCoder coder);
	public EKEventEditViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventEditViewDelegate (IntPtr handle);
	
	public abstract void Completed (EKEventEditViewController controller, EKEventEditViewAction action);
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKEventSearchCallback</h2>
<pre>
[Serializable]
public delegate void EKEventSearchCallback (EKEvent theEvent, ref bool stop);
</pre>
<h2>New Type: MonoTouch.EventKit.EKEventStore</h2>
<pre>
public class EKEventStore : MonoTouch.Foundation.NSObject {
	
	public EKEventStore ();
	public EKEventStore (MonoTouch.Foundation.NSCoder coder);
	public EKEventStore (MonoTouch.Foundation.NSObjectFlag t);
	public EKEventStore (IntPtr handle);
	
	public static MonoTouch.Foundation.NSPredicate PredicateForEvents (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
	public virtual void EnumerateEvents (MonoTouch.Foundation.NSPredicate predicate, EKEventSearchCallback block);
	public virtual EKEvent EventFromIdentifier (string identifier);
	public virtual EKEvent[] EventsMatchin (MonoTouch.Foundation.NSPredicate predicate);
	public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, IntPtr ptrToNserror);
	public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, IntPtr ptrToNsError);
	
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
<h2>New Type: MonoTouch.EventKit.EKEventViewController</h2>
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
	public virtual EKEvent Event {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKParticipant</h2>
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
<h2>New Type: MonoTouch.EventKit.EKParticipantRole</h2>
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
<h2>New Type: MonoTouch.EventKit.EKParticipantStatus</h2>
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
<h2>New Type: MonoTouch.EventKit.EKParticipantType</h2>
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
<h2>New Type: MonoTouch.EventKit.EKRecurrenceDayOfWeek</h2>
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
<h2>New Type: MonoTouch.EventKit.EKRecurrenceEnd</h2>
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
<h2>New Type: MonoTouch.EventKit.EKRecurrenceFrequency</h2>
<pre>
[Serializable]
public enum EKRecurrenceFrequency {
	Daily,
	Weekly,
	Monthly,
	Yearly
}
</pre>
<h2>New Type: MonoTouch.EventKit.EKRecurrenceRule</h2>
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
<h2>New Type: MonoTouch.EventKit.EKSpan</h2>
<pre>
[Serializable]
public enum EKSpan {
	ThisEvent,
	FutureEvents
}
</pre>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessory</h2>
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
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessoryDelegate</h2>
<pre>
public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject {
	
	public EAAccessoryDelegate ();
	public EAAccessoryDelegate (MonoTouch.Foundation.NSCoder coder);
	public EAAccessoryDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public EAAccessoryDelegate (IntPtr handle);
	
	public virtual void Disconnected (EAAccessory accessory);
}
</pre>
<h2>New Type: MonoTouch.ExternalAccessory.EAAccessoryManager</h2>
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
<h2>New Type: MonoTouch.ExternalAccessory.EASession</h2>
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
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSAttributedString</h2>
<p>Removed:</p><pre>
 	public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<p>Added:</p><pre>
 	public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
 	public static string FontAttributeName {
 		get;
 	}
 	public static string ParagraphStyleAttributeName {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.Foundation.NSBlockOperation</h2>
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
<h2>New Type: MonoTouch.Foundation.NSCache</h2>
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
<h2>New Type: MonoTouch.Foundation.NSCacheDelegate</h2>
<pre>
public class NSCacheDelegate : NSObject {
	
	public NSCacheDelegate ();
	public NSCacheDelegate (NSCoder coder);
	public NSCacheDelegate (NSObjectFlag t);
	public NSCacheDelegate (IntPtr handle);
	
	public virtual void WillEvictObject (NSCache cache, NSObject obj);
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSCalendarUnit</h2>
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
<h2>Type Changed: MonoTouch.Foundation.NSData</h2>
<p>Added:</p><pre>
 	public bool Save (string file, NSDataWritingOptions options, out NSError error);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSDataWritingOptions</h2>
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
<h2>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h2>
<p>Removed:</p><pre>
 	public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<p>Added:</p><pre>
 	public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
</pre>
<h2>New Type: MonoTouch.Foundation.NSMutableSet</h2>
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
<h2>Type Changed: MonoTouch.Foundation.NSNotificationCenter</h2>
<p>Added:</p><pre>
 	public virtual void AddObserver (string name, NSObject obj, NSOperationQueue queue, NSNotificationHandler handler);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSNotificationHandler</h2>
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
<h2>New Type: MonoTouch.Foundation.NSOperation</h2>
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
<h2>New Type: MonoTouch.Foundation.NSOperationQueue</h2>
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
<h2>New Type: MonoTouch.Foundation.NSOperationQueuePriority</h2>
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
<h2>New Type: MonoTouch.Foundation.NSPredicate</h2>
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
<h2>New Type: MonoTouch.Foundation.NSPurgeableData</h2>
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
<h2>Type Changed: MonoTouch.Foundation.NSSetEnumerator</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSSetEnumerator
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate void NSSetEnumerator (NSObject obj, ref bool stop);
</pre>
<h2>New Type: MonoTouch.Foundation.NSSortDescriptor</h2>
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
<h2>Type Changed: MonoTouch.Foundation.NSString</h2>
<p>Added:</p><pre>
 	public string Format (MonoTouch.UIKit.UIFont withFont, float width, MonoTouch.UIKit.UILineBreakMode breakMode);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSTimer</h2>
<p>Removed:</p><pre>
 	public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
</pre>
<p>Added:</p><pre>
 	public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h2>New Type: MonoTouch.GameKit.GKDataEventArgs</h2>
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
<h2>New Type: MonoTouch.GameKit.GKError</h2>
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
	MatchRequestInvalid
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKErrorEventArgs</h2>
<pre>
public class GKErrorEventArgs : EventArgs {
	
	public GKErrorEventArgs (MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKFriendsHandler</h2>
<pre>
[Serializable]
public delegate void GKFriendsHandler (GKPlayer[] friends, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKInvite</h2>
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
<h2>New Type: MonoTouch.GameKit.GKInviteHandler</h2>
<pre>
[Serializable]
public delegate void GKInviteHandler (GKInvite invite);
</pre>
<h2>New Type: MonoTouch.GameKit.GKLeaderboard</h2>
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
<h2>New Type: MonoTouch.GameKit.GKLeaderboardPlayerScope</h2>
<pre>
[Serializable]
public enum GKLeaderboardPlayerScope {
	Global,
	FriendsOnly
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKLeaderboardTimeScope</h2>
<pre>
[Serializable]
public enum GKLeaderboardTimeScope {
	Today,
	Week,
	AllTime
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKLeaderboardViewController</h2>
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
<h2>New Type: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate</h2>
<pre>
public class GKLeaderboardViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public GKLeaderboardViewControllerDelegate ();
	public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public GKLeaderboardViewControllerDelegate (IntPtr handle);
	
	public virtual void LeaderboardDidPressDismiss ();
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKLocalPlayer</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatch</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatchDelegate</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatchEventArgs</h2>
<pre>
public class GKMatchEventArgs : EventArgs {
	
	public GKMatchEventArgs (GKMatch match);
	
	public GKMatch Match {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKMatchmaker</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatchmakerViewController</h2>
<pre>
public class GKMatchmakerViewController : MonoTouch.UIKit.UIViewController {
	
	public GKMatchmakerViewController ();
	public GKMatchmakerViewController (MonoTouch.Foundation.NSCoder coder);
	public GKMatchmakerViewController (MonoTouch.Foundation.NSObjectFlag t);
	public GKMatchmakerViewController (IntPtr handle);
	public GKMatchmakerViewController (GKMatchRequest request);
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
<h2>New Type: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatchRequest</h2>
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
<h2>New Type: MonoTouch.GameKit.GKMatchSendDataMode</h2>
<pre>
[Serializable]
public enum GKMatchSendDataMode {
	Reliable,
	Unreliable
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKNotificationHandler</h2>
<pre>
[Serializable]
public delegate void GKNotificationHandler (MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKNotificationMatch</h2>
<pre>
[Serializable]
public delegate void GKNotificationMatch (GKMatch match, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKPlayer</h2>
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
<h2>New Type: MonoTouch.GameKit.GKPlayerConnectionState</h2>
<pre>
[Serializable]
public enum GKPlayerConnectionState {
	Unknown,
	Connected,
	Disconnected
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKPlayerErrorEventArgs</h2>
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
<h2>New Type: MonoTouch.GameKit.GKPlayersEventArgs</h2>
<pre>
public class GKPlayersEventArgs : EventArgs {
	
	public GKPlayersEventArgs (GKPlayer[] players);
	
	public GKPlayer[] Players {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.GameKit.GKQueryHandler</h2>
<pre>
[Serializable]
public delegate void GKQueryHandler (int activity, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKScore</h2>
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
<h2>New Type: MonoTouch.GameKit.GKScoresLoadedHandler</h2>
<pre>
[Serializable]
public delegate void GKScoresLoadedHandler (GKScore[] scoreArray, MonoTouch.Foundation.NSError error);
</pre>
<h2>New Type: MonoTouch.GameKit.GKStateEventArgs</h2>
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
<h2>New Type: MonoTouch.GameKit.GKVoiceChat</h2>
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
<h2>New Type: MonoTouch.GameKit.GKVoiceChatPlayerState</h2>
<pre>
[Serializable]
public enum GKVoiceChatPlayerState {
	Connected,
	Disconnected,
	Speaking,
	Silent
}
</pre>
<h1>Namespace: MonoTouch.MapKit</h1>
<h2>Type Changed: MonoTouch.MapKit.MKAnnotation</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKAnnotationViewDragState</h2>
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
<h2>Type Changed: MonoTouch.MapKit.MKAnnotationViewEventArgs</h2>
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
<h2>New Type: MonoTouch.MapKit.MKCircle</h2>
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
<h2>New Type: MonoTouch.MapKit.MKCircleView</h2>
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
<h2>New Type: MonoTouch.MapKit.MKMapPoint</h2>
<pre>
public struct MKMapPoint {
	
	public MKMapPoint (double x, double y);
	
	public static bool operator == (MKMapPoint a, MKMapPoint b);
	public static bool operator != (MKMapPoint a, MKMapPoint b);
	
	public double X;
	public double Y;
}
</pre>
<h2>New Type: MonoTouch.MapKit.MKMapRect</h2>
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
<h2>New Type: MonoTouch.MapKit.MKMapSize</h2>
<pre>
public struct MKMapSize {
	
	public MKMapSize (double width, double height);
	
	public double Width;
	public double Height;
}
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKMapView</h2>
<p>Added:</p><pre>
 	public virtual void AddOverlay (MKOverlay overlay);
 	public virtual void AddOverlays (MKOverlay[] overlays);
 	public virtual void ExchangeOverlays (int index1, int index2);
 	public virtual void InsertOverlay (MKOverlay overlay, int index);
 	public virtual void InsertOverlayAbove (MKOverlay overlay, MKOverlay sibling);
 	public virtual void InsertOverlayBelow (MKOverlay overlay, MKOverlay sibling);
 	public virtual MKMapRect MapRectThatFits (MKMapRect mapRect);
 	public virtual MKMapRect MapRectThatFits (MKMapRect mapRect, MonoTouch.UIKit.UIEdgeInsets edgePadding);
 	public virtual void RemoveOverlay (MKOverlay overlay);
 	public virtual void RemoveOverlays (MKOverlay[] overlays);
 	public virtual void SetVisibleMapRect (MKMapRect mapRect, bool animate);
 	public virtual void SetVisibleMapRect (MKMapRect mapRect, MonoTouch.UIKit.UIEdgeInsets edgePadding, bool animate);
 	public virtual MKOverlayView ViewForOverlay (MKOverlay overlay);
 	public MKMapViewOverlay GetViewForOverlay {
 		get;
 		set;
 	}
 	public virtual MKOverlay[] Overlays {
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
<h2>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h2>
<p>Added:</p><pre>
 	public virtual void ChangedDragState (MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);
 	public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
 	public virtual void DidDeselectAnnotationView (MKMapView mapView, MKAnnotationView view);
 	public virtual void DidFailToLocateUser (MKMapView mapView, MonoTouch.Foundation.NSError error);
 	public virtual void DidSelectAnnotationView (MKMapView mapView, MKAnnotationView view);
 	public virtual void DidStopLocatingUser (MKMapView mapView);
 	public virtual void DidUpdateUserLocation (MKMapView mapView, MKUserLocation userLocation);
 	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MKOverlay overlay);
 	public virtual void WillStartLocatingUser (MKMapView mapView);
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKMapViewDragStateEventArgs</h2>
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
<h2>Type Changed: MonoTouch.MapKit.MKMapViewOverlay</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.MapKit.MKMapViewOverlay
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate MKOverlayView MKMapViewOverlay (MKMapView mapView, MKOverlay overlay);
</pre>
<h2>New Type: MonoTouch.MapKit.MKMultiPoint</h2>
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
<h2>New Type: MonoTouch.MapKit.MKOverlay</h2>
<pre>
public abstract class MKOverlay : MonoTouch.Foundation.NSObject {
	
	public MKOverlay ();
	public MKOverlay (MonoTouch.Foundation.NSCoder coder);
	public MKOverlay (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlay (IntPtr handle);
	
	public abstract bool IntersectsMapRect (MKMapRect mapRect);
	
	public abstract MKMapRect BoundingMapRect {
		get;
	}
	public abstract MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MapKit.MKOverlayPathView</h2>
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
<h2>New Type: MonoTouch.MapKit.MKOverlayView</h2>
<pre>
public class MKOverlayView : MonoTouch.UIKit.UIView {
	
	public MKOverlayView ();
	public MKOverlayView (MonoTouch.Foundation.NSCoder coder);
	public MKOverlayView (MonoTouch.Foundation.NSObjectFlag t);
	public MKOverlayView (IntPtr handle);
	public MKOverlayView (MKOverlay overlay);
	
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
	public virtual MKOverlay Overlay {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MapKit.MKOverlayViewsEventArgs</h2>
<pre>
public class MKOverlayViewsEventArgs : EventArgs {
	
	public MKOverlayViewsEventArgs (MKOverlayView overlayViews);
	
	public MKOverlayView OverlayViews {
		get;
		set;
	}
}
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKPinAnnotationView</h2>
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
<h2>New Type: MonoTouch.MapKit.MKPointAnnotation</h2>
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
<h2>New Type: MonoTouch.MapKit.MKPolygon</h2>
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
<h2>New Type: MonoTouch.MapKit.MKPolygonView</h2>
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
<h2>New Type: MonoTouch.MapKit.MKPolyline</h2>
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
<h2>New Type: MonoTouch.MapKit.MKPolylineView</h2>
<pre>
public class MKPolylineView : MKOverlayPathView {
	
	public MKPolylineView ();
	public MKPolylineView (MonoTouch.Foundation.NSCoder coder);
	public MKPolylineView (MonoTouch.Foundation.NSObjectFlag t);
	public MKPolylineView (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MKPolyline Polyline {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MapKit.MKShape</h2>
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
<h2>Type Changed: MonoTouch.MapKit.MKUserLocationEventArgs</h2>
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
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMediaItem</h2>
<p>Added:</p><pre>
 	public virtual void EnumerateValues (MonoTouch.Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);
</pre>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMediaItemEnumerator</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.MediaPlayer.MPMediaItemEnumerator
</pre>
<p>Added:</p><pre>
 [Serializable]
 public delegate void MPMediaItemEnumerator (string property, MonoTouch.Foundation.NSObject value, ref bool stop);
</pre>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty</h2>
<p>Added:</p><pre>
 	public const string BeatsPerMinute = "beatsPerMinute";
 	public const string Comments = "comments";
 	public const string AssetUrl = "assetURL";
 	public const string ReleaseDate = "releaseDate";
 	public const string UserGrouping = "userGrouping";
</pre>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h2>
<p>Added:</p><pre>
 	public virtual MPTimedMetadata[] TimedMetadata {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.MediaPlayer.MPTimedMetadata</h2>
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
<h1>Namespace: MonoTouch.MessageUI</h1>
<h2>New Type: MonoTouch.MessageUI.MessageComposeResult</h2>
<pre>
[Serializable]
public enum MessageComposeResult {
	Cancelled,
	Sent,
	Failed
}
</pre>
<h2>New Type: MonoTouch.MessageUI.MFMessageComposeViewController</h2>
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
<h2>New Type: MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate</h2>
<pre>
public abstract class MFMessageComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
	
	public MFMessageComposeViewControllerDelegate ();
	public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
	public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MFMessageComposeViewControllerDelegate (IntPtr handle);
	
	public abstract void Finished (MFMessageComposeViewController controller, MessageComposeResult result);
}
</pre>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>New Type: MonoTouch.ObjCRuntime.BlockDescriptor</h2>
<pre>
public struct BlockDescriptor {
	
	public int reserved;
	public int size;
	public IntPtr copy_helper;
	public IntPtr dispose;
}
</pre>
<h2>New Type: MonoTouch.ObjCRuntime.BlockLiteral</h2>
<pre>
public struct BlockLiteral {
	
	public static IntPtr CreateBlock (Delegate trampoline, Delegate userDelegate);
	
	public IntPtr isa;
	public int flags;
	public int reserved;
	public IntPtr invoke;
	public IntPtr block_descriptor;
	public IntPtr handle;
}
</pre>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Added:</p><pre>
 	public static bool Boolean_objc_msgSend_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSend_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSend_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool Boolean_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool Boolean_objc_msgSendSuper_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSendSuper_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool Boolean_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void CMTime_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector);
 	public static void CMTime_objc_msgSend_stret_CMTime (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void CMTime_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector);
 	public static void CMTime_objc_msgSendSuper_stret_CMTime (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static void CMTimeMapping_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTimeMapping retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeMapping_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTimeMapping retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeRange_objc_msgSend_stret (out MonoTouch.CoreMedia.CMTimeRange retval, IntPtr receiver, IntPtr selector);
 	public static void CMTimeRange_objc_msgSendSuper_stret (out MonoTouch.CoreMedia.CMTimeRange retval, IntPtr receiver, IntPtr selector);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static IntPtr IntPtr_objc_msgSend_CMTime_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8, IntPtr arg9);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.CoreMedia.CMTimeRange arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTimeRange arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8, IntPtr arg9);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_CMTimeRange_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, MonoTouch.CoreMedia.CMTimeRange arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
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
 	public static void void_objc_msgSend_IntPtr_IntPtr_Double_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5);
 	public static void void_objc_msgSend_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static void void_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void void_objc_msgSend_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void void_objc_msgSend_MKMapRect_float_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2, IntPtr arg3);
 	public static void void_objc_msgSend_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSend_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
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
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static void void_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static void void_objc_msgSendSuper_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_float_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSendSuper_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
</pre>
<h2>New Type: MonoTouch.ObjCRuntime.SinceAttribute</h2>
<pre>
public class SinceAttribute : Attribute {
	
	public SinceAttribute (byte major, byte minor);
	
	public byte Major;
	public byte Minor;
}
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h2>New Type: MonoTouch.QuickLook.QLOpenUrl</h2>
<pre>
[Serializable]
public delegate bool QLOpenUrl (QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
</pre>
<h2>New Type: MonoTouch.QuickLook.QLPreviewController</h2>
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
<h2>New Type: MonoTouch.QuickLook.QLPreviewControllerDataSource</h2>
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
<h2>New Type: MonoTouch.QuickLook.QLPreviewControllerDelegate</h2>
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
<h2>New Type: MonoTouch.QuickLook.QLPreviewItem</h2>
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
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIActionSheet</h2>
<p>Removed:</p><pre>
 	public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
 	public UIActionSheet (string title, UIActionSheetDelegate del);
 	public UIActionSheet (string title);
</pre>
<p>Added:</p><pre>
 	public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
 	public UIActionSheet (string title, UIActionSheetDelegate del);
 	public UIActionSheet (string title);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIAlertView</h2>
<p>Removed:</p><pre>
 	public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
</pre>
<p>Added:</p><pre>
 	public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIApplication</h2>
<p>Added:</p><pre>
 	public virtual int BeginBackgroundTask (MonoTouch.Foundation.NSAction backgroundTimeExpired);
 	public virtual void BeginReceivingRemoteControlEvents ();
 	public virtual void CancelAllLocalNotification (UILocalNotification notification);
 	public virtual void CancelLocalNotification (UILocalNotification notification);
 	public virtual void ClearKeepAliveTimeout ();
 	public virtual void EndBackgroundTask (int taskId);
 	public virtual void EndReceivingRemoteControlEvents ();
 	public virtual void PresentLocationNotificationNow (UILocalNotification notification);
 	public virtual void ScheduleLocalNotification (UILocalNotification notification);
 	public virtual bool SetKeepAliveTimout (double timeout, MonoTouch.Foundation.NSAction handler);
 	public static string DidBecomeActiveNotification {
 		get;
 	}
 	public static string DidChangeStatusBarFrameNotification {
 		get;
 	}
 	public static string DidChangeStatusBarOrientationNotification {
 		get;
 	}
 	public static string DidEnterBackgroundNotification {
 		get;
 	}
 	public static string DidFinishLaunchingNotification {
 		get;
 	}
 	public static string DidReceiveMemoryWarningNotification {
 		get;
 	}
 	public static int InvalidBackgroundTaskIdentifier {
 		get;
 	}
 	public static string LaunchOptionsAnnotationKey {
 		get;
 	}
 	public static string LaunchOptionsLocalNotificationKey {
 		get;
 	}
 	public static string LaunchOptionsLocationKey {
 		get;
 	}
 	public static string LaunchOptionsRemoteNotificationKey {
 		get;
 	}
 	public static string LaunchOptionsSourceApplicationKey {
 		get;
 	}
 	public static string LaunchOptionsUrlKey {
 		get;
 	}
 	public static double MinimumKeepAliveTimeout {
 		get;
 	}
 	public static string ProtectedDataDidBecomeAvailable {
 		get;
 	}
 	public static string ProtectedDataWillBecomeUnavailable {
 		get;
 	}
 	public static string SignificantTimeChangeNotification {
 		get;
 	}
 	public static string StatusBarFrameUserInfoKey {
 		get;
 	}
 	public static string StatusBarOrientationUserInfoKey {
 		get;
 	}
 	public static string WillChangeStatusBarFrameNotification {
 		get;
 	}
 	public static string WillChangeStatusBarOrientationNotification {
 		get;
 	}
 	public static string WillEnterForegroundNotification {
 		get;
 	}
 	public static string WillResignActiveNotification {
 		get;
 	}
 	public static string WillTerminateNotification {
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
<h2>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h2>
<p>Added:</p><pre>
 	public virtual void DidEnterBackground (UIApplication application);
 	public virtual void ProtectedDataDidBecomeUnavailable (UIApplication application);
 	public virtual void ProtectedDataWillBecomeUnavailable (UIApplication application);
 	public virtual void ReceivedLocalNotification (UIApplication application, UILocalNotification notification);
 	public virtual void WillEnterForeground (UIApplication application);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIApplicationState</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIBarButtonItem</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIBarButtonSystemItem</h2>
<p>Removed:</p><pre>
 	Redo
</pre>
<p>Added:</p><pre>
 	Redo,
 	PageCurl
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIBezierPath</h2>
<p>Added:</p><pre>
 	public virtual void AddArc (System.Drawing.PointF center, float radius, float startAngle, float endAngle, bool clockWise);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIColor</h2>
<p>Added:</p><pre>
 	public void GetHSBA (out float hue, out float saturation, out float brightness, out float alpha);
 	public void GetRGBA (out float red, out float green, out float blue, out float alpha);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIDataDetectorType</h2>
<p>Added:</p><pre>
 	Address,
 	CalendarEvent,
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIDevice</h2>
<p>Removed:</p><pre>
 	public virtual UIUserInterfaceIdiom _UserInterfaceIdiom {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 	public bool IsMultitaskingSupported {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIEventSubtype</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIEventType</h2>
<p>Removed:</p><pre>
 	Motion
</pre>
<p>Added:</p><pre>
 	Motion,
 	RemoteControl
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIFont</h2>
<p>Added:</p><pre>
 	public virtual float LineHeight {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIGraphics</h2>
<p>Added:</p><pre>
 	public static void BeginImageContextWithOptions (System.Drawing.SizeF size, bool opaque, float scale);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImage</h2>
<p>Added:</p><pre>
 	public UIImage (string filename);
 	public UIImage (MonoTouch.Foundation.NSData data);
 	public static UIImage FromBundle (string name);
 	public virtual float CurrentScale {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerController</h2>
<p>Added:</p><pre>
 	public virtual bool StartVideoCapture ();
 	public virtual bool StopVideoCapture ();
 	public virtual UIImagePickerControllerCameraCaptureMode CameraCaptureMode {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIImagePickerControllerQualityType</h2>
<p>Removed:</p><pre>
 	Low
</pre>
<p>Added:</p><pre>
 	Low,
 	At640x480
</pre>
<h2>New Type: MonoTouch.UIKit.UILocalNotification</h2>
<pre>
public class UILocalNotification : MonoTouch.Foundation.NSObject {
	
	public UILocalNotification ();
	public UILocalNotification (MonoTouch.Foundation.NSCoder coder);
	public UILocalNotification (MonoTouch.Foundation.NSObjectFlag t);
	public UILocalNotification (IntPtr handle);
	
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
<h2>New Type: MonoTouch.UIKit.UINib</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer</h2>
<p>Removed:</p><pre>
 	public virtual uint MaximumNumberOfTouchesRequired {
 	public virtual uint MinimumNumberOfTouchesRequired {
</pre>
<p>Added:</p><pre>
 	public virtual uint MaximumNumberOfTouches {
 	public virtual uint MinimumNumberOfTouches {
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIResponder</h2>
<p>Added:</p><pre>
 	public virtual void RemoteControlReceived (UIEvent theEvent);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIScreen</h2>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreAnimation.CADisplayLink DisplayLink (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector sel);
 	
 	public virtual float Scale {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISegmentedControl</h2>
<p>Removed:</p><pre>
 	public UISegmentedControl (object [] args);
</pre>
<p>Added:</p><pre>
 	public UISegmentedControl (object [] args);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UISegmentedControlStyle</h2>
<p>Removed:</p><pre>
 	Bar
</pre>
<p>Added:</p><pre>
 	Bar,
 	Bezeled
</pre>
<h2>Type Changed: MonoTouch.UIKit.UITableViewCell</h2>
<p>Removed:</p><pre>
 	public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
</pre>
<p>Added:</p><pre>
 	public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIView</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIViewAnimationOptions</h2>
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
<h2>Type Changed: MonoTouch.UIKit.UIWindow</h2>
<p>Added:</p><pre>
 	public virtual UIViewController RootViewController {
 		get;
 		set;
 	}
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h2>New Type: MonoTouch.iAd.AdAction</h2>
<pre>
[Serializable]
public delegate bool AdAction (ADBannerView banner, bool willLeaveApplication);
</pre>
<h2>New Type: MonoTouch.iAd.ADBannerView</h2>
<pre>
public class ADBannerView : MonoTouch.UIKit.UIView {
	
	public ADBannerView ();
	public ADBannerView (MonoTouch.Foundation.NSCoder coder);
	public ADBannerView (MonoTouch.Foundation.NSObjectFlag t);
	public ADBannerView (IntPtr handle);
	
	public virtual void CancelBannerViewAction ();
	
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
	public ADBannerViewDelegate Deleget {
		get;
		set;
	}
	public virtual MonoTouch.Foundation.NSSet RequiredContentSizes {
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
<h2>New Type: MonoTouch.iAd.ADBannerViewDelegate</h2>
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
<h2>New Type: MonoTouch.iAd.AdErrorEventArgs</h2>
<pre>
public class AdErrorEventArgs : EventArgs {
	
	public AdErrorEventArgs (MonoTouch.Foundation.NSError error);
	
	public MonoTouch.Foundation.NSError Error {
		get;
		set;
	}
}
</pre>
<h2>New Type: MonoTouch.iAd.ADManager</h2>
<pre>
public class ADManager : MonoTouch.Foundation.NSObject {
	
	public ADManager ();
	public ADManager (MonoTouch.Foundation.NSCoder coder);
	public ADManager (MonoTouch.Foundation.NSObjectFlag t);
	public ADManager (IntPtr handle);
	
	public static ADManager SharedAdManager ();
	public virtual void DismissModalAd ();
	public virtual void PresentModalAdFromViewController (MonoTouch.UIKit.UIViewController parentViewController);
	
	public virtual bool CanPresentModalAd {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual bool PresentingModalAd {
		get;
	}
	public virtual bool UsesModalAds {
		get;
		set;
	}
}
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
