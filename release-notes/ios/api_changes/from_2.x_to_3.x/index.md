---
id: 5F32754E-C721-2620-6198-9F473148882F
title: "From 2.x to 3.x"
---

<a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "2.0.0";
```

Added:

```
public const string Version = "3.0.8";

        public const string FoundationLibrary = 
"/System/Library/Frameworks/Foundation.framework/Foundation";

        public const string CoreAnimationLibrary = 
"/System/Library/Frameworks/QuartzCore.framework/QuartzCore";

        public const string iAdLibrary = 
"/System/Library/Frameworks/AdLib.framework/AdLib";

        public const string CoreTelephonyLibrary = 
"/System/Library/Frameworks/CoreTelephony.framework/CoreTelephony";

        public const string CoreMediaLibrary = 
"/System/Library/Frameworks/CoreMedia.framework/CoreMedia";

        public const string MapKitLibrary = 
"/System/Library/Frameworks/MapKit.framework/MapKit";

        public const string EventKitLibrary = 
"/System/Library/Frameworks/EventKit.framework/EventKit";
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAsset

```
public class AVAsset : MonoTouch.Foundation.NSObject {
        
        public AVAsset ();
        public AVAsset (MonoTouch.Foundation.NSCoder coder);
        public AVAsset (MonoTouch.Foundation.NSObjectFlag t);
        public AVAsset (IntPtr handle);
        
        public virtual void CancelLoading ();
        public virtual AVMetadataItem[] MetadataForFormat (string format);
        public virtual AVAssetTrack[] TracksWithMediaCharacteristic 
            (string mediaCharacteristic);
        public virtual AVAssetTrack[] TracksWithMediaType 
            (string mediaType);
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetExportSession

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetExportSessionStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetExportSessionStatus

```
[Serializable]
public enum AVAssetExportSessionStatus {
        Unknown,
        Exporting,
        Completed,
        Failed,
        Cancelled
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReaderStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReaderStatus

```
[Serializable]
public enum AVAssetReaderStatus {
        Unknown,
        Reading,
        Completed,
        Failed,
        Cancelled
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetTrack" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetTrack

```
public class AVAssetTrack : MonoTouch.Foundation.NSObject {

public AVAssetTrack ();
public AVAssetTrack (MonoTouch.Foundation.NSCoder coder);
public AVAssetTrack (MonoTouch.Foundation.NSObjectFlag t);
public AVAssetTrack (IntPtr handle); 

public virtual bool HasMediaCharacteristic (string mediaCharacteristic);
public virtual AVMetadataItem[] MetadataForFormat (string format);
public virtual MonoTouch.CoreMedia.CMTime 
    SamplePresentationTimeForTrackTime (MonoTouch.CoreMedia.CMTime trackTime);
public virtual AVAssetTrackSegment SegmentForTrackTime 
    (MonoTouch.CoreMedia.CMTime trackTime);

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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetTrackSegment" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetTrackSegment

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAsynchronousKeyValueLoading

```
public abstract class AVAsynchronousKeyValueLoading : MonoTouch.Foundation.NSObject { 
public AVAsynchronousKeyValueLoading (); 
public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSCoder coder); 
public AVAsynchronousKeyValueLoading (MonoTouch.Foundation.NSObjectFlag t); 
public AVAsynchronousKeyValueLoading (IntPtr handle); 
public abstract void LoadValuesAsynchronously     
    (string [] keys, MonoTouch.Foundation.NSAction handler); 
public abstract AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError); }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioMix" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioMix

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioMixInputParameters" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioMixInputParameters

```
public class AVAudioMixInputParameters : MonoTouch.Foundation.NSObject {
        
        public AVAudioMixInputParameters ();
        public AVAudioMixInputParameters (MonoTouch.Foundation.NSCoder coder);
        public AVAudioMixInputParameters (MonoTouch.Foundation.NSObjectFlag t);
        public AVAudioMixInputParameters (IntPtr handle);
        
        public virtual bool GetVolumeRamp (MonoTouch.CoreMedia.CMTime forTime, 
            float startVolume, float endVolume, MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int TrackID {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed:

```
public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSError error);
        public AVAudioPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSError error);
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayerDelegate" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate

Added:

```
public virtual void EndInterruption (AVAudioPlayer player, AVAudioSessionInterruptionFlags flags);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioRecorder" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioRecorder

Removed:

```
public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, 
            MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
```

Added:

```
public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, 
            MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioRecorderDelegate" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate

Added:

```
public virtual void EndInterruption (AVAudioRecorder recorder, AVAudioSessionInterruptionFlags flags);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSession

Added:

```
public bool SetActive (bool beActive, AVAudioSessionFlags flags, out MonoTouch.Foundation.NSError outError);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSessionDelegate" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSessionDelegate

Removed:

```
public virtual void CategoryChanged (string category);
        public virtual void CurrentHardwareInputNumberOfChannelsChanged (int numberOfChannels);
        public virtual void CurrentHardwareOutputNumberOfChannelsChanged (int numberOfChannels);
        public virtual void CurrentHardwareSampleRateChanged (double sampleRate);
```

Added:

```
public virtual void EndInterruption (AVAudioSessionInterruptionFlags flags);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSessionFlags" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSessionFlags

Removed:

```
Could not find MonoTouch.AVFoundation.AVAudioSessionFlags
```

Added:

```
[Serializable]
 [Flags]
 public enum AVAudioSessionFlags {
        NotifyOthersOnDeactivation
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags

Removed:

```
Could not find MonoTouch.AVFoundation.AVAudioSessionInterruptionFlags
```

Added:

```
[Serializable]
 [Flags]
 public enum AVAudioSessionInterruptionFlags {
        ShouldResume
 }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureAudioChannel" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureAudioChannel

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureAudioDataOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutput

```
public class AVCaptureAudioDataOutput : AVCaptureOutput {
        
        public AVCaptureAudioDataOutput ();
        public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureAudioDataOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureAudioDataOutput (IntPtr handle);
        
        public virtual void SetSampleBufferDelegatequeue 
            (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate,
            MonoTouch.CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
        
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
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate 

```
public class AVCaptureAudioDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
        
        public AVCaptureAudioDataOutputSampleBufferDelegate ();
        public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureAudioDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureAudioDataOutputSampleBufferDelegate (IntPtr handle);
        
        public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, 
            MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureCompletionHandler" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureCompletionHandler

```
[Serializable]
public delegate void AVCaptureCompletionHandler (MonoTouch.CoreMedia.CMSampleBuffer 
    imageDataSampleBuffer, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureConnection" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureConnection

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureDevice

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureDeviceInput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureDeviceInput

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureDevicePosition" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureDevicePosition

```
[Serializable]
public enum AVCaptureDevicePosition {
        Back,
        Front
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureExposureMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureExposureMode

```
[Serializable]
public enum AVCaptureExposureMode {
        Locked,
        AutoExpose,
        ContinuousAutoExposure
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureFileOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureFileOutput

```
public class AVCaptureFileOutput : AVCaptureOutput {
        
        public AVCaptureFileOutput ();
        public AVCaptureFileOutput (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureFileOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureFileOutput (IntPtr handle);
        
        public virtual void StartRecordingToOutputFile (MonoTouch.Foundation.NSUrl outputFileUrl, 
            AVCaptureFileOutputRecordingDelegate recordingDelegate);
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureFileOutputRecordingDelegate

```
public class AVCaptureFileOutputRecordingDelegate : MonoTouch.Foundation.NSObject {
        
        public AVCaptureFileOutputRecordingDelegate ();
        public AVCaptureFileOutputRecordingDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureFileOutputRecordingDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureFileOutputRecordingDelegate (IntPtr handle);
        
        public virtual void DidStartRecording (AVCaptureFileOutput captureOutput, 
            MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections);
        public virtual void FinishedRecording (AVCaptureFileOutput captureOutput, 
            MonoTouch.Foundation.NSUrl outputFileUrl, MonoTouch.Foundation.NSObject[] connections, 
            MonoTouch.Foundation.NSError error);
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureFlashMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureFlashMode

```
[Serializable]
public enum AVCaptureFlashMode {
        Off,
        On,
        Auto
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureFocusMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureFocusMode

```
[Serializable]
public enum AVCaptureFocusMode {
        ModeLocked,
        ModeAutoFocus,
        ModeContinuousAutoFocus
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureInput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureInput

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureInputPort" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureInputPort

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureMovieFileOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureMovieFileOutput

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureOutput

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureSession" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureSession

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureStillImageOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureStillImageOutput

```
public class AVCaptureStillImageOutput : AVCaptureOutput {
        
        public AVCaptureStillImageOutput ();
        public AVCaptureStillImageOutput (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureStillImageOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureStillImageOutput (IntPtr handle);
        
        public static MonoTouch.Foundation.NSData JpegStillToNSData (MonoTouch.CoreMedia.CMSampleBuffer buffer);
        public virtual void CaptureStillImageAsynchronously (AVCaptureConnection connection, 
            AVCaptureCompletionHandler completionHandler);
        
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureTorchMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureTorchMode

```
[Serializable]
public enum AVCaptureTorchMode {
        Off,
        On,
        Auto
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureVideoDataOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutput

```
public class AVCaptureVideoDataOutput : AVCaptureOutput {
        
        public AVCaptureVideoDataOutput ();
        public AVCaptureVideoDataOutput (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureVideoDataOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureVideoDataOutput (IntPtr handle);
        
        public virtual void SetSampleBufferDelegatequeue 
            (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, 
            IntPtr sampleBufferCallbackQueue);
        
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
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate 

```
public class AVCaptureVideoDataOutputSampleBufferDelegate : MonoTouch.Foundation.NSObject {
        
        public AVCaptureVideoDataOutputSampleBufferDelegate ();
        public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureVideoDataOutputSampleBufferDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureVideoDataOutputSampleBufferDelegate (IntPtr handle);
        
        public virtual void DidOutputSampleBuffer (AVCaptureOutput captureOutput, 
            MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureVideoOrientation" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureVideoOrientation

```
[Serializable]
public enum AVCaptureVideoOrientation {
        Portrait,
        PortraitUpsideDown,
        LandscapeLeft,
        LandscapeRight
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureWhiteBalanceMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureWhiteBalanceMode

```
[Serializable]
public enum AVCaptureWhiteBalanceMode {
        Locked,
        AutoWhiteBalance,
        ContinuousAutoWhiteBalance
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCompositionTrack" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCompositionTrack

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCompositionTrackSegment" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCompositionTrackSegment

```
public class AVCompositionTrackSegment : AVAssetTrackSegment {
        
        public AVCompositionTrackSegment ();
        public AVCompositionTrackSegment (MonoTouch.Foundation.NSCoder coder);
        public AVCompositionTrackSegment (MonoTouch.Foundation.NSObjectFlag t);
        public AVCompositionTrackSegment (IntPtr handle);
        public AVCompositionTrackSegment (MonoTouch.Foundation.NSUrl URL, int trackID, 
            MonoTouch.CoreMedia.CMTimeRange sourceTimeRange, MonoTouch.CoreMedia.CMTimeRange targetTimeRange);
        public AVCompositionTrackSegment (MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public static IntPtr FromTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
        public static IntPtr FromUrl (MonoTouch.Foundation.NSUrl url, int trackID, 
            MonoTouch.CoreMedia.CMTimeRange sourceTimeRange, MonoTouch.CoreMedia.CMTimeRange targetTimeRange);
        
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVError

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVErrorHandler" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVErrorHandler

```
[Serializable]
public delegate void AVErrorHandler (MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVFileType" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVFileType

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVKeyValueStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVKeyValueStatus

```
[Serializable]
public enum AVKeyValueStatus {
        Unknown,
        Loading,
        Loaded,
        Failed,
        Cancelled
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMediaCharacteristic" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMediaCharacteristic

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMediaType" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMediaType

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMetadataItem" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMetadataItem

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableAudioMix" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableAudioMix

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableAudioMixInputParameters" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters

```
public class AVMutableAudioMixInputParameters : AVAudioMixInputParameters {
        
        public AVMutableAudioMixInputParameters ();
        public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSCoder coder);
        public AVMutableAudioMixInputParameters (MonoTouch.Foundation.NSObjectFlag t);
        public AVMutableAudioMixInputParameters (IntPtr handle);
        
        public static AVMutableAudioMixInputParameters Create ();
        public static AVMutableAudioMixInputParameters FromTrack (AVAssetTrack track);
        public virtual void SetVolume (float volume, MonoTouch.CoreMedia.CMTime atTime);
        public virtual void SetVolumeRamp (float startVolume, float endVolume, 
            MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int TrackID {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableCompositionTrack" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableCompositionTrack

```
public class AVMutableCompositionTrack : AVCompositionTrack {
        
        public AVMutableCompositionTrack ();
        public AVMutableCompositionTrack (MonoTouch.Foundation.NSCoder coder);
        public AVMutableCompositionTrack (MonoTouch.Foundation.NSObjectFlag t);
        public AVMutableCompositionTrack (IntPtr handle);
        
        public virtual void InsertEmptyTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
        public virtual void RemoveTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange);
        public virtual void ScaleTimeRange (MonoTouch.CoreMedia.CMTimeRange timeRange, 
            MonoTouch.CoreMedia.CMTime duration);
        
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableMetadataItem" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableMetadataItem

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableVideoComposition" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableVideoComposition

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction

```
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
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction 

```
public class AVMutableVideoCompositionLayerInstruction : AVVideoCompositionLayerInstruction {
        
        public AVMutableVideoCompositionLayerInstruction ();
        public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSCoder coder);
        public AVMutableVideoCompositionLayerInstruction (MonoTouch.Foundation.NSObjectFlag t);
        public AVMutableVideoCompositionLayerInstruction (IntPtr handle);
        
        public static AVMutableVideoCompositionLayerInstruction Create ();
        public static AVMutableVideoCompositionLayerInstruction FromAssetTrack (AVAssetTrack track);
        public virtual void SetOpacity (float opacity, MonoTouch.CoreMedia.CMTime time);
        public virtual void SetOpacityRamp (float startOpacity, float endOpacity, 
            MonoTouch.CoreMedia.CMTimeRange timeRange);
        public virtual void SetTransform (MonoTouch.CoreGraphics.CGAffineTransform transform, 
            MonoTouch.CoreMedia.CMTime atTime);
        public virtual void SetTransformRamp (MonoTouch.CoreGraphics.CGAffineTransform startTransform, 
            MonoTouch.CoreGraphics.CGAffineTransform endTransform, MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int TrackID {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayer" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayer

```
public class AVPlayer : MonoTouch.Foundation.NSObject {
        
        public AVPlayer ();
        public AVPlayer (MonoTouch.Foundation.NSCoder coder);
        public AVPlayer (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayer (IntPtr handle);
        public AVPlayer (MonoTouch.Foundation.NSUrl URL);
        public AVPlayer (AVPlayerItem item);
        
        public static AVPlayer FromPlayerItem (AVPlayerItem item);
        public static AVPlayer FromUrl (MonoTouch.Foundation.NSUrl URL);
        public virtual MonoTouch.Foundation.NSObject AddBoundaryTimeObserver 
            (MonoTouch.Foundation.NSValue[] times, MonoTouch.CoreFoundation.DispatchQueue queue, 
            MonoTouch.Foundation.NSAction handler);
        public virtual MonoTouch.Foundation.NSObject AddPeriodicTimeObserver 
            (MonoTouch.CoreMedia.CMTime interval, MonoTouch.CoreFoundation.DispatchQueue queue, 
            AVTimeHandler handler);
        public virtual void Pause ();
        public virtual void Play ();
        public virtual void RemoveTimeObserver (MonoTouch.Foundation.NSObject observer);
        public virtual void ReplaceCurrentItemWithPlayerItem (AVPlayerItem item);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime toTime);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime toTime, 
            MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
        
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerActionAtItemEnd" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerActionAtItemEnd

```
[Serializable]
public enum AVPlayerActionAtItemEnd {
        Pause,
        None
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItem

```
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
        public virtual bool SeekToDate (MonoTouch.CoreMedia.CMTime time, 
            MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter);
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemStatus

```
[Serializable]
public enum AVPlayerItemStatus {
        Unknown,
        ReadyToPlay,
        Failed
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemTrack" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemTrack

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerLayer" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerLayer

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerStatus

```
[Serializable]
public enum AVPlayerStatus {
        Unknown,
        ReadyToPlay,
        Failed
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVTimeHandler" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVTimeHandler

```
[Serializable]
public delegate void AVTimeHandler (MonoTouch.CoreMedia.CMTime time);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVUrlAsset" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVUrlAsset

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideo" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideo

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoComposition" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoComposition

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCompositionCoreAnimationTool" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCompositionCoreAnimationTool

```
public class AVVideoCompositionCoreAnimationTool : MonoTouch.Foundation.NSObject {
        
        public AVVideoCompositionCoreAnimationTool ();
        public AVVideoCompositionCoreAnimationTool (MonoTouch.Foundation.NSCoder coder);
        public AVVideoCompositionCoreAnimationTool (MonoTouch.Foundation.NSObjectFlag t);
        public AVVideoCompositionCoreAnimationTool (IntPtr handle);
        
        public static AVVideoCompositionCoreAnimationTool FromLayer (MonoTouch.CoreAnimation.CALayer videoLayer, 
            MonoTouch.CoreAnimation.CALayer animationLayer);
        public static AVVideoCompositionCoreAnimationTool FromLayer (MonoTouch.CoreAnimation.CALayer layer, int trackID);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCompositionInstruction" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCompositionInstruction

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction

```
public class AVVideoCompositionLayerInstruction : MonoTouch.Foundation.NSObject {
        
        public AVVideoCompositionLayerInstruction ();
        public AVVideoCompositionLayerInstruction (MonoTouch.Foundation.NSCoder coder);
        public AVVideoCompositionLayerInstruction (MonoTouch.Foundation.NSObjectFlag t);
        public AVVideoCompositionLayerInstruction (IntPtr handle);
        
        public virtual bool GetOpacityRamp (MonoTouch.CoreMedia.CMTime time, 
            float startOpacity, float endOpacity, MonoTouch.CoreMedia.CMTimeRange timeRange);
        public virtual bool GetTransformRamp (MonoTouch.CoreMedia.CMTime time, 
            MonoTouch.CoreGraphics.CGAffineTransform startTransform, 
            MonoTouch.CoreGraphics.CGAffineTransform endTransform, MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int TrackID {
                get;
        }
}
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController 

Removed:

```
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
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController 

Removed:

```
public virtual MonoTouch.Foundation.NSNumber[] _DisplayedProperties {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AddressBookUI.ABPersonViewController" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABPersonViewController

Removed:

```
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
```

 <a name="Type_Changed:_MonoTouch.AddressBookUI.ABUnknownPersonViewController" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController

Removed:

```
public virtual IntPtr _AddressBook {
                get;
                set;
        }
        public virtual IntPtr _DisplayedPerson {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioChannelLayout" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioChannelLayout

Removed:

```
public int Tag;
```

Added:

```
public int Tag {
                get;
                set;
        }
        
        public AudioChannelLayoutTag AudioTag;
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioChannelLayoutTag" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioChannelLayoutTag

Removed:

```
Could not find MonoTouch.AudioToolbox.AudioChannelLayoutTag
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormatType" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Removed:

```
AES3
```

Added:

```
AES3,
        MPEG4AAC_ELD
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added:

```
public AudioTimeStamp GetNearestStartTime (AudioTimeStamp requestedStartTime);
        public AudioTimeStamp TranslateTime (AudioTimeStamp timeToTranslate);
        public AudioTimeStamp CurrentTime {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueParameter" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueueParameter

Removed:

```
Volume
```

Added:

```
Volume,
        Pan,
        VolumeRampTime
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSession" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSession

Added:

```
public static AudioSessionInterruptionType InterruptionType {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionInterruptionType" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionInterruptionType

Removed:

```
Could not find MonoTouch.AudioToolbox.AudioSessionInterruptionType
```

Added:

```
[Serializable]
 public enum AudioSessionInterruptionType {
        ShouldResume,
        ShouldNotResume
 }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSessionProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSessionProperty

Removed:

```
OverrideCategoryMixWithOthers
```

Added:

```
OverrideCategoryMixWithOthers,
        InterruptionType
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.CoreAnimation.CAAnimation

Removed:

```
public virtual CAAnimation CreateAnimation ();
        public virtual double CFTimeInterval {
```

Added:

```
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
        public event EventHandler<CAAnimationStateEventArgs> AnimationStopped;
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAAnimationGroup" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAAnimationGroup

Added:

```
public static CAAnimationGroup CreateAnimation ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAAnimationStateEventArgs" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAAnimationStateEventArgs

Removed:

```
Could not find MonoTouch.CoreAnimation.CAAnimationStateEventArgs
```

Added:

```
public class CAAnimationStateEventArgs : EventArgs {
        
        public CAAnimationStateEventArgs (bool finished);
        
        public bool Finished {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CABasicAnimation" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CABasicAnimation

Removed:

```
public virtual MonoTouch.Foundation.NSNumber By {
        public virtual MonoTouch.Foundation.NSNumber From {
        public virtual MonoTouch.Foundation.NSNumber To {
```

Added:

```
public virtual MonoTouch.Foundation.NSObject By {
        public virtual MonoTouch.Foundation.NSObject From {
        public virtual MonoTouch.Foundation.NSObject To {
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAGradientLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAGradientLayer

Removed:

```
public virtual IntPtr _Colors {
                set;
```

Added:

```
public static MonoTouch.Foundation.NSString GradientLayerAxial {
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAKeyFrameAnimation" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Removed:

```
public virtual IntPtr _Path {
                get;
                set;
        }
        public virtual string rotationMode {
        public virtual MonoTouch.Foundation.NSNumber[] Values {
```

Added:

```
public static CAPropertyAnimation FromKeyPath (string path);
        
        public virtual string RotationMode {
        public virtual MonoTouch.Foundation.NSObject[] Values {
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Removed:

```
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
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.CoreAnimation.CAScrollLayer" class="injected"></a>


## New Type: MonoTouch.CoreAnimation.CAScrollLayer

```
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
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATextLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATextLayer

Added:

```
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
```

 <a name="New_Type:_MonoTouch.CoreAnimation.CATiledLayer" class="injected"></a>


## New Type: MonoTouch.CoreAnimation.CATiledLayer

```
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
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATransaction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATransaction

Removed:

```
public static void SetValueForKey 
            (MonoTouch.Foundation.NSObject anObject, string key);

        public static MonoTouch.Foundation.NSObject ValueForKey (string key);
```

Added:

```
public static void SetValueForKey 
            (MonoTouch.Foundation.NSObject anObject, MonoTouch.Foundation.NSString key);

        public static MonoTouch.Foundation.NSObject ValueForKey 
            (MonoTouch.Foundation.NSString key);

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
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATransform3D" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATransform3D

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CATransition" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CATransition

Added:

```
public static CATransition CreateAnimation ();
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAValueFunction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAValueFunction

Removed:

```
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
```

Added:

```
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
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.CoreFoundation.CFRunLoop

Added:

```
public void Stop ();
```

 <a name="New_Type:_MonoTouch.CoreFoundation.DispatchObject" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.DispatchObject

```
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
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.DispatchQueue [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.DispatchQueuePriority [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum DispatchQueuePriority {
        High,
        Default,
        Low
}
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.CoreGraphics.CGContext

Added:

```
public CGPath CopyPath ();
        public void DrawLayer (CGLayer layer, System.Drawing.PointF point);
        public void DrawLayer (CGLayer layer, System.Drawing.RectangleF rect);
        public void SetAllowsFontSmoothing (bool allows);
        public void SetAllowsFontSubpixelQuantization (bool allows);
        public void SetAllowsSubpixelPositioning (bool allows);
        public void SetShouldSubpixelPositionFonts (bool shouldSubpixelPositionFonts);
        public void ShouldSubpixelQuantizeFonts (bool shouldSubpixelQuantizeFonts);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGInterpolationQuality" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGInterpolationQuality

Removed:

```
High
```

Added:

```
High,
        Medium
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGLayer [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public CGContext Context {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

Added:

```
public System.Drawing.RectangleF PathBoundingBox {
                get;
        }
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.CoreLocation.CLDeviceOrientation [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLError [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
HeadingFailure
```

Added:

```
HeadingFailure,
        RegionMonitoringDenied,
        RegionMonitoringFailure,
        RegionMonitoringSetupDelayed
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs

Removed:

```
Could not find MonoTouch.CoreLocation.CLHeadingUpdatedEventArgs
```

Added:

```
public class CLHeadingUpdatedEventArgs : EventArgs {
        
        public CLHeadingUpdatedEventArgs (CLHeading newHeading);
        
        public CLHeading NewHeading {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationCoordinate2D" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationCoordinate2D

Added:

```
public bool IsValid ();
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

Removed:

```
public virtual bool LocationServicesEnabled {
```

Added:

```
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
        
        public event System.EventHandler<MonoTouch.Foundation.NSErrorEventArgs> Failed;
        public event EventHandler<CLRegionErrorEventArgs> MonitoringFailed;
        public event EventHandler<CLRegionEventArgs> RegionEntered;
        public event EventHandler<CLRegionEventArgs> RegionLeft;
        public event EventHandler<CLHeadingUpdatedEventArgs> UpdatedHeading;
        public event EventHandler<CLLocationUpdatedEventArgs> UpdatedLocation;
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

Added:

```
public virtual void MonitoringFailed (CLLocationManager manager, 
            CLRegion region, MonoTouch.Foundation.NSError error);
        public virtual void RegionEntered (CLLocationManager manager, CLRegion region);
        public virtual void RegionLeft (CLLocationManager manager, CLRegion region);
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManagerEventArgs" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManagerEventArgs

Removed:

```
Could not find MonoTouch.CoreLocation.CLLocationManagerEventArgs
```

Added:

```
[Serializable]
 public delegate bool CLLocationManagerEventArgs (CLLocationManager manager);
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationUpdatedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationUpdatedEventArgs

Removed:

```
Could not find MonoTouch.CoreLocation.CLLocationUpdatedEventArgs
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLRegion" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLRegion

```
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
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLRegionErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLRegionErrorEventArgs

```
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
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLRegionEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLRegionEventArgs

```
public class CLRegionEventArgs : EventArgs {
        
        public CLRegionEventArgs (CLRegion region);
        
        public CLRegion Region {
                get;
                set;
        }
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.CoreMedia.CMSampleBuffer

```
public class CMSampleBuffer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTime" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTime

```
public struct CMTime {
        
        public long Value;
        public int TimeScale;
        public int TimeFlags;
        public long TimeEpoch;
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTimeMapping" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimeMapping

```
public struct CMTimeMapping {
        
        public CMTime Source;
        public CMTime Target;
}
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimeRange [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public struct CMTimeRange {
        
        public CMTime Start;
        public CMTime Duration;
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.CoreMotion.CMAcceleration

```
public struct CMAcceleration {
        
        public CMAcceleration (double x, double y, double z);
        
        public double X;
        public double Y;
        public double Z;
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMAccelerometerData" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMAccelerometerData

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMAccelerometerHandler" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMAccelerometerHandler

```
[Serializable]
public delegate void CMAccelerometerHandler (CMAccelerometerData data, 
        MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMAttitude" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMAttitude

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMDeviceMotion" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMDeviceMotion

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMDeviceMotionHandler" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMDeviceMotionHandler

```
[Serializable]
public delegate void CMDeviceMotionHandler (CMDeviceMotion motion, 
    MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMError" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMError

```
[Serializable]
public enum CMError {
        Null
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMGyroData" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMGyroData

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMGyroHandler" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMGyroHandler

```
[Serializable]
public delegate void CMGyroHandler (CMGyroData gyroData, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMLogItem" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMLogItem

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMMotionManager" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMMotionManager

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMQuaternion" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMQuaternion

```
public struct CMQuaternion {
        
        public CMQuaternion (double x, double y, double z, double w);
        
        public double x;
        public double y;
        public double z;
        public double w;
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMRotationMatrix" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMRotationMatrix

```
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
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMRotationRate" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMRotationRate

```
public struct CMRotationRate {
        
        public CMRotationRate (double x, double y, double z);
        
        public double x;
        public double y;
        public double z;
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.CoreTelephony.CTCall [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.CoreTelephony.CTCallCenter" class="injected"></a>


## New Type: MonoTouch.CoreTelephony.CTCallCenter

```
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
```

 <a name="New_Type:_MonoTouch.CoreTelephony.CTCallEventHandler" class="injected"></a>


## New Type: MonoTouch.CoreTelephony.CTCallEventHandler

```
[Serializable]
public delegate void CTCallEventHandler (CTCall call);
```

 <a name="New_Type:_MonoTouch.CoreTelephony.CTCarrier" class="injected"></a>


## New Type: MonoTouch.CoreTelephony.CTCarrier

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKAlarm" class="injected"></a>


# New Type: MonoTouch.EventKit.EKAlarm

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKCalendar" class="injected"></a>


## New Type: MonoTouch.EventKit.EKCalendar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKCalendarEventAvailability" class="injected"></a>


## New Type: MonoTouch.EventKit.EKCalendarEventAvailability

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
[Flags]
public enum EKCalendarEventAvailability {
        None,
        Busy,
        Free,
        Tentative,
        Unavailable
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKCalendarType" class="injected"></a>


## New Type: MonoTouch.EventKit.EKCalendarType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKCalendarType {
        Local,
        CalDav,
        Exchange,
        Subscription,
        Birthday
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKDay" class="injected"></a>


## New Type: MonoTouch.EventKit.EKDay

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKErrorCode" class="injected"></a>


## New Type: MonoTouch.EventKit.EKErrorCode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKEventAvailability" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEventAvailability

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKEventAvailability {
        NotSupported,
        Busy,
        Free,
        Tentative,
        Unavailable
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKEventEditViewAction" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEventEditViewAction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKEventEditViewAction {
        Canceled,
        Saved,
        Deleted
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKEventSearchCallback" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEventSearchCallback

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void EKEventSearchCallback (EKEvent theEvent, ref bool stop);
```

 <a name="New_Type:_MonoTouch.EventKit.EKEventStatus" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEventStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKEventStatus {
        None,
        Confirmed,
        Tentative,
        Cancelled
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEventStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKParticipant" class="injected"></a>


## New Type: MonoTouch.EventKit.EKParticipant

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKParticipantRole" class="injected"></a>


## New Type: MonoTouch.EventKit.EKParticipantRole

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKParticipantRole {
        Unknown,
        Required,
        Optional,
        Chair,
        NonParticipant
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKParticipantStatus" class="injected"></a>


## New Type: MonoTouch.EventKit.EKParticipantStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKParticipantType" class="injected"></a>


## New Type: MonoTouch.EventKit.EKParticipantType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKParticipantType {
        Unknown,
        Person,
        Room,
        Resource,
        Group
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKRecurrenceDayOfWeek" class="injected"></a>


## New Type: MonoTouch.EventKit.EKRecurrenceDayOfWeek

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKRecurrenceEnd" class="injected"></a>


## New Type: MonoTouch.EventKit.EKRecurrenceEnd

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKRecurrenceFrequency" class="injected"></a>


## New Type: MonoTouch.EventKit.EKRecurrenceFrequency

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKRecurrenceFrequency {
        Daily,
        Weekly,
        Monthly,
        Yearly
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKRecurrenceRule" class="injected"></a>


## New Type: MonoTouch.EventKit.EKRecurrenceRule

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.EventKit.EKSpan" class="injected"></a>


## New Type: MonoTouch.EventKit.EKSpan

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum EKSpan {
        ThisEvent,
        FutureEvents
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.EventKitUI.EKEventEditController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate MonoTouch.EventKit.EKCalendar EKEventEditController (EKEventEditViewController controller);
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventEditEventArgs" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventEditEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class EKEventEditEventArgs : EventArgs {
        
        public EKEventEditEventArgs (MonoTouch.EventKit.EKEventEditViewAction action);
        
        public MonoTouch.EventKit.EKEventEditViewAction Action {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventEditViewController" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventEditViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
        
        public event EventHandler<ekeventediteventargs> Completed; } </ekeventediteventargs>
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventEditViewDelegate" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventEditViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public abstract class EKEventEditViewDelegate : MonoTouch.Foundation.NSObject {
        
        public EKEventEditViewDelegate ();
        public EKEventEditViewDelegate (MonoTouch.Foundation.NSCoder coder);
        public EKEventEditViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public EKEventEditViewDelegate (IntPtr handle);
        
        public abstract void Completed (EKEventEditViewController controller, MonoTouch.EventKit.EKEventEditViewAction action);
        public virtual MonoTouch.EventKit.EKCalendar GetDefaultCalendarForNewEvents (EKEventEditViewController controller);
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventViewController" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.ExternalAccessory.EAAccessory

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.ExternalAccessory.EAAccessoryDelegate" class="injected"></a>


## New Type: MonoTouch.ExternalAccessory.EAAccessoryDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class EAAccessoryDelegate : MonoTouch.Foundation.NSObject {
        
        public EAAccessoryDelegate ();
        public EAAccessoryDelegate (MonoTouch.Foundation.NSCoder coder);
        public EAAccessoryDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public EAAccessoryDelegate (IntPtr handle);
        
        public virtual void Disconnected (EAAccessory accessory);
}
```

 <a name="New_Type:_MonoTouch.ExternalAccessory.EAAccessoryManager" class="injected"></a>


## New Type: MonoTouch.ExternalAccessory.EAAccessoryManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.ExternalAccessory.EASession" class="injected"></a>


## New Type: MonoTouch.ExternalAccessory.EASession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.Foundation.NSAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
```

Added:

```
public NSAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
        public static NSString FontAttributeName {
                get;
        }
        public static NSString ParagraphStyleAttributeName {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSBlockOperation" class="injected"></a>


## New Type: MonoTouch.Foundation.NSBlockOperation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSCache" class="injected"></a>


## New Type: MonoTouch.Foundation.NSCache

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
        
        public event EventHandler<nsobjecteventargs> WillEvictObject; } </nsobjecteventargs>
```

 <a name="New_Type:_MonoTouch.Foundation.NSCacheDelegate" class="injected"></a>


## New Type: MonoTouch.Foundation.NSCacheDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class NSCacheDelegate : NSObject {
        
        public NSCacheDelegate ();
        public NSCacheDelegate (NSCoder coder);
        public NSCacheDelegate (NSObjectFlag t);
        public NSCacheDelegate (IntPtr handle);
        
        public virtual void WillEvictObject (NSCache cache, NSObject obj);
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCalendarUnit" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCalendarUnit

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSCalendarUnit
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSData" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual NSRange Find (NSData dataToFind, NSDataSearchOptions searchOptions, NSRange searchRange);
        public bool Save (string file, NSDataWritingOptions options, out NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataSearchOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataSearchOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSDataSearchOptions
```

Added:

```
[Serializable]
 [Flags]
 public enum NSDataSearchOptions {
        SearchBackwards,
        SearchAnchored
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataWritingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataWritingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSDataWritingOptions
```

Added:

```
[Serializable]
 [Flags]
 public enum NSDataWritingOptions : uint {
        Atomic,
        FileProtectionNone,
        FileProtectionComplete,
        NSDataWritingFileProtectionMask
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDateComponents" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDateComponents

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSDateComponents
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
```

Added:

```
public NSMutableAttributedString (string str, MonoTouch.CoreText.CTStringAttributes attributes);
```

 <a name="New_Type:_MonoTouch.Foundation.NSMutableSet" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMutableSet

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotificationCenter" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotificationCenter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void AddObserver (string name, NSObject obj, NSOperationQueue queue, NSNotificationHandler handler);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotificationCoalescing" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotificationCoalescing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSNotificationCoalescing
```

Added:

```
[Serializable]
 [Flags]
 public enum NSNotificationCoalescing {
        NoCoalescing,
        CoalescingOnName,
        CoalescingOnSender
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotificationHandler" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotificationHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
internal class NSNotificationHandler : NSObject {
        
        public NSNotificationHandler (Action<NSNotification> notify);
        
        public void Post (NSNotification s);
 }
```

Added:

```
[Serializable]
 public delegate void NSNotificationHandler (NSNotification notification);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotificationQueue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotificationQueue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSNotificationQueue
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSNull" class="injected"></a>


## New Type: MonoTouch.Foundation.NSNull

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSOperation" class="injected"></a>


## New Type: MonoTouch.Foundation.NSOperation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSOperationQueue" class="injected"></a>


## New Type: MonoTouch.Foundation.NSOperationQueue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSOperationQueuePriority" class="injected"></a>


## New Type: MonoTouch.Foundation.NSOperationQueuePriority

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum NSOperationQueuePriority {
        VeryLow,
        Low,
        Normal,
        High,
        VeryHigh
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSPostingStyle" class="injected"></a>


## New Type: MonoTouch.Foundation.NSPostingStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum NSPostingStyle {
        PostWhenIdle,
        PostASAP,
        Now
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSPredicate" class="injected"></a>


## New Type: MonoTouch.Foundation.NSPredicate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.Foundation.NSPurgeableData" class="injected"></a>


## New Type: MonoTouch.Foundation.NSPurgeableData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class NSPurgeableData : NSMutableData {
        
        public NSPurgeableData ();
        public NSPurgeableData (NSCoder coder);
        public NSPurgeableData (NSObjectFlag t);
        public NSPurgeableData (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRange" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRange

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public const int NotFound = 2147483647;
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSSetEnumerator" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSSetEnumerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSSetEnumerator
```

Added:

```
[Serializable]
 public delegate void NSSetEnumerator (NSObject obj, ref bool stop);
```

 <a name="New_Type:_MonoTouch.Foundation.NSSortDescriptor" class="injected"></a>


## New Type: MonoTouch.Foundation.NSSortDescriptor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimer" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
```

Added:

```
public NSTimer (NSDate date, TimeSpan when, NSAction action, bool repeats);
        public static NSTimer CreateRepeatingScheduledTimer (double seconds, NSAction action);
        public static NSTimer CreateRepeatingTimer (double seconds, NSAction action);
        public static NSTimer CreateScheduledTimer (double seconds, NSAction action);
        public static NSTimer CreateTimer (double seconds, NSAction action);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSValue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSValue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public static NSValue FromCATransform3D (MonoTouch.CoreAnimation.CATransform3D transform);
        public virtual MonoTouch.CoreAnimation.CATransform3D CATransform3DValue {
                get;
        }
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.GameKit.GKAchievement

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## New Type: MonoTouch.GameKit.GKAchievementDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKAchievementDescriptionHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKAchievementDescriptionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKAchievementDescriptionHandler (GKAchievementDescription[] descriptions, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKAchievementViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKAchievementViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKAchievementViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKAchievementViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class GKAchievementViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKAchievementViewControllerDelegate ();
        public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKAchievementViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKAchievementViewControllerDelegate (IntPtr handle);
        
        public virtual void DidPressDismiss ();
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKCompletionHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKCompletionHandler (GKAchievement[] achivements, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKDataEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKDataEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKError" class="injected"></a>


## New Type: MonoTouch.GameKit.GKError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class GKErrorEventArgs : EventArgs {
        
        public GKErrorEventArgs (MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKFriendsHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKFriendsHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKFriendsHandler (GKPlayer[] friends, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKImageLoadedHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKImageLoadedHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKImageLoadedHandler (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKInvite" class="injected"></a>


## New Type: MonoTouch.GameKit.GKInvite

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKInviteHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKInviteHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKInviteHandler (GKInvite invite);
```

 <a name="New_Type:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLeaderboard

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKLeaderboardPlayerScope" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLeaderboardPlayerScope

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum GKLeaderboardPlayerScope {
        Global,
        FriendsOnly
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKLeaderboardTimeScope" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLeaderboardTimeScope

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum GKLeaderboardTimeScope {
        Today,
        Week,
        AllTime
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKLeaderboardViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLeaderboardViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKLeaderboardViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class GKLeaderboardViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKLeaderboardViewControllerDelegate ();
        public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKLeaderboardViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKLeaderboardViewControllerDelegate (IntPtr handle);
        
        public virtual void LeaderboardDidPressDismiss ();
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKLocalPlayer" class="injected"></a>


## New Type: MonoTouch.GameKit.GKLocalPlayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatch

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
        
        public event EventHandler<gkplayererroreventargs> ConnectionFailed;       public event EventHandler<gkdataeventargs> DataReceived;  public event EventHandler<gkerroreventargs> Failed;       public event EventHandler<gkstateeventargs> StateChanged; } </gkstateeventargs></gkerroreventargs></gkdataeventargs></gkplayererroreventargs>
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class GKMatchEventArgs : EventArgs {
        
        public GKMatchEventArgs (GKMatch match);
        
        public GKMatch Match {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchmaker" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchmaker

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchmakerViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
        public event EventHandler<gkerroreventargs> Failed;       public event EventHandler<gkmatcheventargs> MatchCreated;         public event EventHandler<gkplayerseventargs> PlayersFound; } </gkplayerseventargs></gkmatcheventargs></gkerroreventargs>
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchmakerViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchRequest" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchSendDataMode" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchSendDataMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum GKMatchSendDataMode {
        Reliable,
        Unreliable
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKNotificationHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKNotificationHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKNotificationHandler (MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKNotificationMatch" class="injected"></a>


## New Type: MonoTouch.GameKit.GKNotificationMatch

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKNotificationMatch (GKMatch match, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## New Type: MonoTouch.GameKit.GKPlayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKPlayerConnectionState" class="injected"></a>


## New Type: MonoTouch.GameKit.GKPlayerConnectionState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum GKPlayerConnectionState {
        Unknown,
        Connected,
        Disconnected
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKPlayerErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKPlayerErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKPlayersEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKPlayersEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class GKPlayersEventArgs : EventArgs {
        
        public GKPlayersEventArgs (GKPlayer[] players);
        
        public GKPlayer[] Players {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKQueryHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKQueryHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKQueryHandler (int activity, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKScore" class="injected"></a>


## New Type: MonoTouch.GameKit.GKScore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKScoresLoadedHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKScoresLoadedHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate void GKScoresLoadedHandler (GKScore[] scoreArray, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKSessionDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKSessionDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual void PeerConnectionFailed (GKSession session, MonoTouch.Foundation.NSError error);
```

Added:

```
public virtual void PeerConnectionFailed (GKSession session, string peerID, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKStateEventArgs" class="injected"></a>


## New Type: MonoTouch.GameKit.GKStateEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKVoiceChat" class="injected"></a>


## New Type: MonoTouch.GameKit.GKVoiceChat

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.GameKit.GKVoiceChatPlayerState" class="injected"></a>


## New Type: MonoTouch.GameKit.GKVoiceChatPlayerState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum GKVoiceChatPlayerState {
        Connected,
        Disconnected,
        Speaking,
        Silent
}
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.MapKit.MKAnnotation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKAnnotationViewDragState" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKAnnotationViewDragState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MapKit.MKAnnotationViewDragState
```

Added:

```
[Serializable]
 public enum MKAnnotationViewDragState {
        None,
        Starting,
        Dragging,
        Canceling,
        Ending
 }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKAnnotationViewEventArgs" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKAnnotationViewEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MapKit.MKAnnotationViewEventArgs
```

Added:

```
public class MKAnnotationViewEventArgs : EventArgs {
        
        public MKAnnotationViewEventArgs (MKAnnotationView view);
        
        public MKAnnotationView View {
                get;
                set;
        }
 }
```

 <a name="New_Type:_MonoTouch.MapKit.MKCircle" class="injected"></a>


## New Type: MonoTouch.MapKit.MKCircle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKCircleView" class="injected"></a>


## New Type: MonoTouch.MapKit.MKCircleView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKMapPoint" class="injected"></a>


## New Type: MonoTouch.MapKit.MKMapPoint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public struct MKMapPoint {
        
        public MKMapPoint (double x, double y);
        
        public override bool Equals (object other);
        public override int GetHashCode ();
        
        public static bool operator == (MKMapPoint a, MKMapPoint b);
        public static bool operator != (MKMapPoint a, MKMapPoint b);
        
        public double X;
        public double Y;
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKMapRect" class="injected"></a>


## New Type: MonoTouch.MapKit.MKMapRect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKMapSize" class="injected"></a>


## New Type: MonoTouch.MapKit.MKMapSize

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public struct MKMapSize {
        
        public MKMapSize (double width, double height);
        
        public double Width;
        public double Height;
}
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
        public event EventHandler<MKMapViewDragStateEventArgs> ChangedDragState;
        public event EventHandler<MKOverlayViewsEventArgs> DidAddOverlayViews;
        public event EventHandler<MKAnnotationViewEventArgs> DidDeselectAnnotationView;
        public event System.EventHandler<MonoTouch.Foundation.NSErrorEventArgs> DidFailToLocateUser;
        public event EventHandler<MKAnnotationViewEventArgs> DidSelectAnnotationView;
        public event EventHandler DidStopLocatingUser;
        public event EventHandler<MKUserLocationEventArgs> DidUpdateUserLocation;
        public event EventHandler WillStartLocatingUser;
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void ChangedDragState (MKMapView mapView, MKAnnotationView annotationView, MKAnnotationViewDragState newState, MKAnnotationViewDragState oldState);
        public virtual void DidAddOverlayViews (MKMapView mapView, MKOverlayView overlayViews);
        public virtual void DidDeselectAnnotationView (MKMapView mapView, MKAnnotationView view);
        public virtual void DidFailToLocateUser (MKMapView mapView, MonoTouch.Foundation.NSError error);
        public virtual void DidSelectAnnotationView (MKMapView mapView, MKAnnotationView view);
        public virtual void DidStopLocatingUser (MKMapView mapView);
        public virtual void DidUpdateUserLocation (MKMapView mapView, MKUserLocation userLocation);
        public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
        public virtual void WillStartLocatingUser (MKMapView mapView);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapViewDragStateEventArgs" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapViewDragStateEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MapKit.MKMapViewDragStateEventArgs
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapViewOverlay" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapViewOverlay

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MapKit.MKMapViewOverlay
```

Added:

```
[Serializable]
 public delegate MKOverlayView MKMapViewOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
```

 <a name="New_Type:_MonoTouch.MapKit.MKMultiPoint" class="injected"></a>


## New Type: MonoTouch.MapKit.MKMultiPoint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKOverlayPathView" class="injected"></a>


## New Type: MonoTouch.MapKit.MKOverlayPathView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKOverlayView" class="injected"></a>


## New Type: MonoTouch.MapKit.MKOverlayView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKOverlayViewsEventArgs" class="injected"></a>


## New Type: MonoTouch.MapKit.MKOverlayViewsEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class MKOverlayViewsEventArgs : EventArgs {
        
        public MKOverlayViewsEventArgs (MKOverlayView overlayViews);
        
        public MKOverlayView OverlayViews {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPinAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPinAnnotationView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual bool Draggable {
                get;
                set;
        }
        public virtual MKAnnotationViewDragState DragState {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.MapKit.MKPointAnnotation" class="injected"></a>


## New Type: MonoTouch.MapKit.MKPointAnnotation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKPolygon" class="injected"></a>


## New Type: MonoTouch.MapKit.MKPolygon

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKPolygonView" class="injected"></a>


## New Type: MonoTouch.MapKit.MKPolygonView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKPolyline" class="injected"></a>


## New Type: MonoTouch.MapKit.MKPolyline

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKPolylineView" class="injected"></a>


## New Type: MonoTouch.MapKit.MKPolylineView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MapKit.MKShape" class="injected"></a>


## New Type: MonoTouch.MapKit.MKShape

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKUserLocationEventArgs" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKUserLocationEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MapKit.MKUserLocationEventArgs
```

Added:

```
public class MKUserLocationEventArgs : EventArgs {
        
        public MKUserLocationEventArgs (MKUserLocation userLocation);
        
        public MKUserLocation UserLocation {
                get;
                set;
        }
 }
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.MediaPlayer.ItemsPickedEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void EnumerateValues (MonoTouch.Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemEnumerator" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemEnumerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.MediaPlayer.MPMediaItemEnumerator
```

Added:

```
[Serializable]
 public delegate void MPMediaItemEnumerator (string property, MonoTouch.Foundation.NSObject value, ref bool stop);
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemProperty" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public const string BeatsPerMinute = "beatsPerMinute";
        public const string Comments = "comments";
        public const string AssetUrl = "assetURL";
        public const string ReleaseDate = "releaseDate";
        public const string UserGrouping = "userGrouping";
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual MPTimedMetadata[] TimedMetadata {
                get;
        }
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPTimedMetadata" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPTimedMetadata

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.MessageUI.MessageComposeResult

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum MessageComposeResult {
        Cancelled,
        Sent,
        Failed
}
```

 <a name="New_Type:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## New Type: MonoTouch.MessageUI.MFMessageComposeViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.MessageUI.MFMessageComposeViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public abstract class MFMessageComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public MFMessageComposeViewControllerDelegate ();
        public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public MFMessageComposeViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public MFMessageComposeViewControllerDelegate (IntPtr handle);
        
        public abstract void Finished (MFMessageComposeViewController controller, MessageComposeResult result);
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.ObjCRuntime.BlockDescriptor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public struct BlockDescriptor {
        
        public int reserved;
        public int size;
        public IntPtr copy_helper;
        public IntPtr dispose;
}
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.BlockFlags" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.BlockFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.BlockLiteral" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.BlockLiteral

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public static bool Boolean_objc_msgSend_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
        public static bool Boolean_objc_msgSendSuper_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.SinceAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.SinceAttribute

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class SinceAttribute : Attribute {
        
        public SinceAttribute (byte major, byte minor);
        
        public byte Major;
        public byte Minor;
}
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.QuickLook.QLOpenUrl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate bool QLOpenUrl (QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
```

 <a name="New_Type:_MonoTouch.QuickLook.QLPreviewController" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLPreviewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.QuickLook.QLPreviewControllerDataSource" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLPreviewControllerDataSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public abstract class QLPreviewControllerDataSource : MonoTouch.Foundation.NSObject {
        
        public QLPreviewControllerDataSource ();
        public QLPreviewControllerDataSource (MonoTouch.Foundation.NSCoder coder);
        public QLPreviewControllerDataSource (MonoTouch.Foundation.NSObjectFlag t);
        public QLPreviewControllerDataSource (IntPtr handle);
        
        public abstract QLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
        public abstract int PreviewItemCount (QLPreviewController controller);
}
```

 <a name="New_Type:_MonoTouch.QuickLook.QLPreviewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLPreviewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class QLPreviewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public QLPreviewControllerDelegate ();
        public QLPreviewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public QLPreviewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public QLPreviewControllerDelegate (IntPtr handle);
        
        public virtual void DidDismiss (QLPreviewController controller);
        public virtual bool ShouldOpenUrl (QLPreviewController controller, MonoTouch.Foundation.NSUrl url, QLPreviewItem item);
        public virtual void WillDismiss (QLPreviewController controller);
}
```

 <a name="New_Type:_MonoTouch.QuickLook.QLPreviewItem" class="injected"></a>


## New Type: MonoTouch.QuickLook.QLPreviewItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.StoreKit.SKPaymentTransactionObserver 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual void RemovedTransactions (SKPaymentTransaction[] transactions);
        public virtual void RestoreCompletedTransactionsFailedWithError (MonoTouch.Foundation.NSError error);
```

Added:

```
public virtual void RemovedTransactions (SKPaymentQueue queue, SKPaymentTransaction[] transactions);
        public virtual void RestoreCompletedTransactionsFailedWithError (SKPaymentQueue queue, MonoTouch.Foundation.NSError error);
```

 <a name="" class="injected"></a>


##    
   
Type Changed: MonoTouch.UIKit.UIActionSheet

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
        public UIActionSheet (string title, UIActionSheetDelegate del);
        public UIActionSheet (string title);
                set;
```

Added:

```
public UIActionSheet (string title, UIActionSheetDelegate del, string cancelTitle, string destroy, params string [] other);
        public UIActionSheet (string title, UIActionSheetDelegate del);
        public UIActionSheet (string title);
        public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
        public virtual void ShowFrom (UIBarButtonItem item, bool animated);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
        public virtual void ShowFrom (System.Drawing.RectangleF rect, UIView inView, bool animated);
        public virtual void ShowFrom (UIBarButtonItem item);
        public virtual void ShowFrom (UIBarButtonItem item, bool animated);
                set;
```

Added:

```
public UIAlertView (string title, string message, UIAlertViewDelegate del, string cancelButtonTitle, params string [] otherButtons);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual bool SetStatusBarHidden (bool state, UIStatusBarAnimation animation);
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void DidEnterBackground (UIApplication application);
        public virtual void ProtectedDataDidBecomeUnavailable (UIApplication application);
        public virtual void ProtectedDataWillBecomeUnavailable (UIApplication application);
        public virtual void ReceivedLocalNotification (UIApplication application, UILocalNotification notification);
        public virtual void WillEnterForeground (UIApplication application);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationState" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIApplicationState
```

Added:

```
[Serializable]
 public enum UIApplicationState {
        Active,
        Inactive,
        Background
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBarButtonItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public UIBarButtonItem (UIImage image, UIBarButtonItemStyle style, EventHandler handler);
        public UIBarButtonItem (string title, UIBarButtonItemStyle style, EventHandler handler);
        public UIBarButtonItem (UIBarButtonSystemItem systemItem, EventHandler handler);
        public UIBarButtonItem (UIBarButtonSystemItem systemItem);
```

Added:

```
public UIBarButtonItem (UIImage image, UIBarButtonItemStyle style, EventHandler handler);
        public UIBarButtonItem (string title, UIBarButtonItemStyle style, EventHandler handler);
        public UIBarButtonItem (UIBarButtonSystemItem systemItem, EventHandler handler);
        public UIBarButtonItem (UIBarButtonSystemItem systemItem);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonSystemItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBarButtonSystemItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Redo
```

Added:

```
Redo,
        PageCurl
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBezierPath

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void AddArc (System.Drawing.PointF center, float radius, float startAngle, float endAngle, bool clockWise);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual UIEdgeInsets imageEdgeInsets {
```

Added:

```
public virtual UIEdgeInsets ImageEdgeInsets {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIColor" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIColor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public void GetHSBA (out float hue, out float saturation, out float brightness, out float alpha);
        public void GetRGBA (out float red, out float green, out float blue, out float alpha);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIControlState" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIControlState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
[Flags]
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDataDetectorType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDataDetectorType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
Address,
        CalendarEvent,
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual UIUserInterfaceIdiom _UserInterfaceIdiom {
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIEventSubtype" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIEventSubtype

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
MotionShake
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIEventType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIEventType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Motion
```

Added:

```
Motion,
        RemoteControl
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIFont" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIFont

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public override string ToString ();
        public virtual float LineHeight {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual bool DelaysTouchesBegain {
```

Added:

```
public virtual bool DelaysTouchesBegan {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGraphics" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGraphics

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public static void BeginImageContextWithOptions (System.Drawing.SizeF size, bool opaque, float scale);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImage" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UIImage (string filename);
        public UIImage (MonoTouch.Foundation.NSData data);
        public static UIImage FromBundle (string name);
        public static UIImage FromResource (System.Reflection.Assembly assembly, string name);
        public UIImage Scale (System.Drawing.SizeF newSize);
        public virtual float CurrentScale {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIImagePickerControllerCameraCaptureMode
```

Added:

```
[Serializable]
 public enum UIImagePickerControllerCameraCaptureMode {
        Photo,
        Video
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerCameraDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIImagePickerControllerCameraDevice
```

Added:

```
[Serializable]
 public enum UIImagePickerControllerCameraDevice {
        Rear,
        Front
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIImagePickerControllerCameraFlashMode
```

Added:

```
[Serializable]
 public enum UIImagePickerControllerCameraFlashMode {
        Off,
        Auto,
        On
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerQualityType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerQualityType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Low
```

Added:

```
Low,
        At640x480
```

 <a name="New_Type:_MonoTouch.UIKit.UILocalNotification" class="injected"></a>


## New Type: MonoTouch.UIKit.UILocalNotification

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILongPressGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILongPressGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UILongPressGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIMenuController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIMenuController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
```

 <a name="New_Type:_MonoTouch.UIKit.UINib" class="injected"></a>


## New Type: MonoTouch.UIKit.UINib

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPanGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
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
```

Added:

```
public UIPanGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
        
        public virtual void SetTranslation (System.Drawing.PointF translation, UIView view);
        public virtual System.Drawing.PointF TranslationInView (UIView view);
        public virtual System.Drawing.PointF VelocityInView (UIView view);
        public virtual uint MaximumNumberOfTouches {
        public virtual uint MinimumNumberOfTouches {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPasteboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPasteboard

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public virtual void Remove (string name);
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UIPickerViewDelegate Delegate {
                get;
                set;
        }
        public UIPickerViewModel Source {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerViewDataSource" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerViewDataSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIPickerViewDataSource
```

Added:

```
public abstract class UIPickerViewDataSource : MonoTouch.Foundation.NSObject {
        
        public UIPickerViewDataSource ();
        public UIPickerViewDataSource (MonoTouch.Foundation.NSCoder coder);
        public UIPickerViewDataSource (MonoTouch.Foundation.NSObjectFlag t);
        public UIPickerViewDataSource (IntPtr handle);
        
        public abstract int GetComponentCount (UIPickerView pickerView);
        public abstract int GetRowsInComponent (UIPickerView pickerView, int component);
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIPickerViewDelegate
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPinchGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPinchGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UIPinchGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPopoverController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPopoverController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
set;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIResponder" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIResponder

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual void RemoteControlReceived (UIEvent theEvent);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIRotationGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIRotationGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UIRotationGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreen" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreen

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual MonoTouch.CoreAnimation.CADisplayLink DisplayLink (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector sel);
        
        public virtual float Scale {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
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
        public event EventHandler<UISearchBarTextChangedEventArgs> TextChanged;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarPredicate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarPredicate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UISearchBarPredicate
```

Added:

```
[Serializable]
 public delegate bool UISearchBarPredicate (UISearchBar searchBar);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarRangeEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarRangeEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UISearchBarRangeEventArgs
```

Added:

```
[Serializable]
 public delegate bool UISearchBarRangeEventArgs (UISearchBar searchBar, MonoTouch.Foundation.NSRange range, string text);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarTextChangedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarTextChangedEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UISearchBarTextChangedEventArgs
```

Added:

```
public class UISearchBarTextChangedEventArgs : EventArgs {
        
        public UISearchBarTextChangedEventArgs (string searchText);
        
        public string SearchText {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISegmentedControl" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISegmentedControl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public UISegmentedControl (object [] args);
```

Added:

```
public UISegmentedControl (object [] args);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISegmentedControlStyle" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISegmentedControlStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Bar
```

Added:

```
Bar,
        Bezeled
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwipeGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwipeGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UISwipeGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UITabBarSelection ShouldSelectViewController {
                get;
                set;
        }
        
        public event EventHandler<UITabBarCustomizeChangeEventArgs> FinishedCustomizingViewControllers;
        public event EventHandler<UITabBarCustomizeEventArgs> OnCustomizingViewControllers;
        public event EventHandler<UITabBarCustomizeChangeEventArgs> OnEndCustomizingViewControllers;
        public event EventHandler<UITabBarSelectionEventArgs> ViewControllerSelected;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UITabBarCustomizeChangeEventArgs
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarCustomizeEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarCustomizeEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UITabBarCustomizeEventArgs
```

Added:

```
public class UITabBarCustomizeEventArgs : EventArgs {
        
        public UITabBarCustomizeEventArgs (UIViewController[] viewControllers);
        
        public UIViewController[] ViewControllers {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarSelection" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarSelection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UITabBarSelection
```

Added:

```
[Serializable]
 public delegate bool UITabBarSelection (UITabBarController tabBarController, UIViewController viewController);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarSelectionEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarSelectionEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UITabBarSelectionEventArgs
```

Added:

```
public class UITabBarSelectionEventArgs : EventArgs {
        
        public UITabBarSelectionEventArgs (UIViewController viewController);
        
        public UIViewController ViewController {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewCell" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewCell

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
```

Added:

```
public UITableViewCell (UITableViewCellStyle style, string reuseIdentifier);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITapGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITapGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public UITapGestureRecognizer (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public static MonoTouch.Foundation.NSString TextDidBeginEditingNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextDidEndEditingNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextFieldTextDidChangeNotification {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public static MonoTouch.Foundation.NSString TextDidBeginEditingNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextDidEndEditingNotification {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public static void Animate (double duration, MonoTouch.Foundation.NSAction animation);
        public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, MonoTouch.Foundation.NSAction completion);
        public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction completion);
        public virtual float ContentScaleFactor {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewAnimationOptions" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewAnimationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Removed:

```
Could not find MonoTouch.UIKit.UIViewAnimationOptions
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWebView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWebView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
public virtual bool AllowsInlineMediaPlayback {
                get;
                set;
        }
        public virtual bool MediaPlaybackRequiresUserAction {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

Added:

```
set;
```

 <a name="" class="injected"></a>


##    
   
New Type: MonoTouch.iAd.AdAction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public delegate bool AdAction (ADBannerView banner, bool willLeaveApplication);
```

 <a name="New_Type:_MonoTouch.iAd.ADBannerView" class="injected"></a>


## New Type: MonoTouch.iAd.ADBannerView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
        public event EventHandler<aderroreventargs> FailedToReceiveAd; } </aderroreventargs>
```

 <a name="New_Type:_MonoTouch.iAd.ADBannerViewDelegate" class="injected"></a>


## New Type: MonoTouch.iAd.ADBannerViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
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
```

 <a name="New_Type:_MonoTouch.iAd.AdError" class="injected"></a>


## New Type: MonoTouch.iAd.AdError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
[Serializable]
public enum AdError {
        Unknown,
        ServerFailure,
        LoadingThrottled,
        InventoryUnavailable
}
```

 <a name="New_Type:_MonoTouch.iAd.AdErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.iAd.AdErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class AdErrorEventArgs : EventArgs {
        
        public AdErrorEventArgs (MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.iAd.ADManager" class="injected"></a>


## New Type: MonoTouch.iAd.ADManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_2.x_to_3.x/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/API_Changes/2.0_to_3.0#)

```
public class ADManager : MonoTouch.Foundation.NSObject {
        
        public ADManager ();
        public ADManager (MonoTouch.Foundation.NSCoder coder);
        public ADManager (MonoTouch.Foundation.NSObjectFlag t);
        public ADManager (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```
