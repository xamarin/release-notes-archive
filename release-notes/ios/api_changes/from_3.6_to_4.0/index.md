---
id: 1A1A52DD-7CA8-85E1-8BE5-9483811C5963
title: "From 3.6 to 4.0"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public const string Version = "3.2.6";

Added:
```

```
public const string Version = "4.0.0";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual AVMetadataItem[] ChapterMetadataGroups (MonoTouch.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
        public virtual MonoTouch.Foundation.NSLocale[] AvailableChapterLocales {
                get;
        }
        public virtual bool Composable {
                get;
        }
        public virtual bool Exportable {
                get;
        }
        public virtual bool Playable {
                get;
        }
        public virtual bool Readable {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual void ExportAsynchronously (AVErrorHandler errorHandler);
```

Added:

```
public virtual void ExportAsynchronously (AVCompletionHandler handler);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
        public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
```

Added:

```
public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
        public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
        public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
        public AVVideoSettings VideoSettings {
        public virtual MonoTouch.Foundation.NSDictionary WeakVideoSettings {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriter" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual int MovieTimeScale {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriterInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual int MediaTimeScale {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDeviceInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceInput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr ptrToHandleToError);
        public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr ptrToHandleToError);
```

Added:

```
public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr handle);
        public AVCaptureDeviceInput (AVCaptureDevice device, out MonoTouch.Foundation.NSError error);
        public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device);
        public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr handle);
        public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.Foundation.NSString DidStartRunningNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidStopRunningNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ErrorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString InterruptionEndedNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString Preset1280x720 {
                get;
        }
        public static MonoTouch.Foundation.NSString Preset640x480 {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetHigh {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetLow {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetMedium {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetPhoto {
                get;
        }
        public static MonoTouch.Foundation.NSString RuntimeErrorNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WasInterruptedNotification {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoDataOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual IntPtr SampleBufferCallbackQueue {
        public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
```

Added:

```
public void SetSampleBufferDelegateAndQueue (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
        public virtual MonoTouch.CoreFoundation.DispatchQueue SampleBufferCallbackQueue {
        public AVVideoSettings VideoSettings {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary WeakVideoSettings {
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCompletionHandler" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public delegate void AVCompletionHandler ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
DecoderNotFound,
        EncoderNotFound,
        ContentIsNotAuthorized,
        DeviceIsNotAvailableInBackground,
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMetadataItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMetadataItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
        public virtual AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMutableTimedMetadataGroup" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMutableTimedMetadataGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class AVMutableTimedMetadataGroup : AVTimedMetadataGroup {
        
        public AVMutableTimedMetadataGroup ();
        public AVMutableTimedMetadataGroup (MonoTouch.Foundation.NSCoder coder);
        public AVMutableTimedMetadataGroup (MonoTouch.Foundation.NSObjectFlag t);
        public AVMutableTimedMetadataGroup (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVMetadataItem[] Items {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMTimeRange Timerange {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.Foundation.NSString DidPLayToEndTimeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ItemFailedToPlayToEndTimeErrorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ItemFailedToPlayToEndTimeNotification {
                get;
        }
        public virtual AVPlayerItemAccessLog AccessLog {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate CurrentDate {
                get;
        }
        public virtual AVPlayerItemErrorLog ErrorLog {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemAccessLog" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLog

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class AVPlayerItemAccessLog : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemAccessLog ();
        public AVPlayerItemAccessLog (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemAccessLog (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemAccessLog (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVPlayerItemAccessLogEvent[] Events {
                get;
        }
        public virtual MonoTouch.Foundation.NSData ExtendedLogData {
                get;
        }
        public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class AVPlayerItemAccessLogEvent : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemAccessLogEvent ();
        public AVPlayerItemAccessLogEvent (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemAccessLogEvent (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemAccessLogEvent (IntPtr handle);
        
        public virtual long BytesTransferred {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int DroppedVideoFrameCount {
                get;
        }
        public virtual double DurationWatched {
                get;
        }
        public virtual double IndicatedBitrate {
                get;
        }
        public virtual double ObservedBitrate {
                get;
        }
        public virtual string PlaybackSessionID {
                get;
        }
        public virtual MonoTouch.Foundation.NSData PlaybackStartDate {
                get;
        }
        public virtual double PlaybackStartOffset {
                get;
        }
        public virtual int SegmentedDownloadedCount {
                get;
        }
        public virtual double SegmentsDownloadedDuration {
                get;
        }
        public virtual string ServerAddress {
                get;
        }
        public virtual int ServerAddressChangeCount {
                get;
        }
        public virtual int StallCount {
                get;
        }
        public virtual string Uri {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemErrorLog" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLog

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class AVPlayerItemErrorLog : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemErrorLog ();
        public AVPlayerItemErrorLog (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemErrorLog (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemErrorLog (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVPlayerItemErrorLogEvent[] Events {
                get;
        }
        public virtual MonoTouch.Foundation.NSData ExtendedLogData {
                get;
        }
        public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemErrorLogEvent" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLogEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class AVPlayerItemErrorLogEvent : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemErrorLogEvent ();
        public AVPlayerItemErrorLogEvent (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemErrorLogEvent (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemErrorLogEvent (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate Date {
                get;
        }
        public virtual string ErrorComment {
                get;
        }
        public virtual string ErrorDomain {
                get;
        }
        public virtual int ErrorStatusCode {
                get;
        }
        public virtual string PlaybackSessionID {
                get;
        }
        public virtual string ServerAddress {
                get;
        }
        public virtual string Uri {
                get;
        }
 }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVTimedMetadataGroup" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVTimedMetadataGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class AVTimedMetadataGroup : MonoTouch.Foundation.NSObject {
        
        public AVTimedMetadataGroup ();
        public AVTimedMetadataGroup (MonoTouch.Foundation.NSCoder coder);
        public AVTimedMetadataGroup (MonoTouch.Foundation.NSObjectFlag t);
        public AVTimedMetadataGroup (IntPtr handle);
        public AVTimedMetadataGroup (AVMetadataItem[] items, MonoTouch.CoreMedia.CMTimeRange timeRange);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVMetadataItem[] Items {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideoSettings" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoSettings

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
Could not find MonoTouch.AVFoundation.AVVideoSettings
```

Added:

```
public class AVVideoSettings {
        
        public AVVideoSettings ();
        public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
        
        public MonoTouch.Foundation.NSDictionary ToDictionary ();
        
        public System.Nullable<MonoTouch.CoreVideo.CVPixelFormatType> PixelFormat {
                get;
                set;
        }
 }
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsGroupType" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsGroupType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
GroupPhotoStream,
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public AudioStreamPacketDescription AudioStreamPacketDescription {
                get;
        }
        public AudioQueueLevelMeterState[] CurrentLevelMeter {
                get;
        }
        public AudioQueueLevelMeterState[] CurrentLevelMeterDB {
                get;
        }
        public int DecodeBufferSizeFrames {
                get;
        }
        public bool EnableLevelMetering {
                get;
                set;
        }
        public int MaximumOutputPacketSize {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueLevelMeterState" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueueLevelMeterState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public struct AudioQueueLevelMeterState {
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAAnimation" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAAnimation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.Foundation.NSString AnimationDescrete {
                get;
        }
        public static MonoTouch.Foundation.NSString AnimationLinear {
                get;
        }
        public static MonoTouch.Foundation.NSString AnimationPaced {
                get;
        }
        public static MonoTouch.Foundation.NSString RotateModeAuto {
                get;
        }
        public static MonoTouch.Foundation.NSString RotateModeAutoReverse {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAShapeLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAShapeLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.Foundation.NSString CapButt {
                get;
        }
        public static MonoTouch.Foundation.NSString CapRound {
                get;
        }
        public static MonoTouch.Foundation.NSString CapSquare {
                get;
        }
        public static MonoTouch.Foundation.NSString FilLRuleEvenOdd {
                get;
        }
        public static MonoTouch.Foundation.NSString FillRuleNonZero {
                get;
        }
        public static MonoTouch.Foundation.NSString JoinBevel {
                get;
        }
        public static MonoTouch.Foundation.NSString JoinMiter {
                get;
        }
        public static MonoTouch.Foundation.NSString JoinRound {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFRunLoop" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFRunLoop

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void WakeUp ();
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGBitmapContext" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGBitmapContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public CGBitmapContext (byte [] data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGImageAlphaInfo bitmapInfo);
        public CGBitmapContext (IntPtr data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGBitmapFlags bitmapInfo);
        public CGBitmapContext (byte [] data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGBitmapFlags bitmapInfo);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGContext" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void BeginTransparencyLayer ();
        public void BeginTransparencyLayer (MonoTouch.Foundation.NSDictionary auxiliaryInfo);
        public void BeginTransparencyLayer (System.Drawing.RectangleF rectangle);
        public void BeginTransparencyLayer (System.Drawing.RectangleF rectangle, MonoTouch.Foundation.NSDictionary auxiliaryInfo);
        public void EndTransparencyLayer ();
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGGradient" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGGradient

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public CGGradient (CGColorSpace colorspace, float [] components);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void CGPathAddLineToPoint (CGAffineTransform transform, float x, float y);
        public void CGPathAddLineToPoint (float x, float y);
```


&lt;h0 class="editable"&gt;Namespace: MonoTouch.CoreMedia&lt;/h0&gt; <a name="Type_Changed:_MonoTouch.CoreMedia.CMSampleBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMSampleBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public MonoTouch.CoreVideo.CVImageBuffer GetImageBuffer ();
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMTime" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMTime

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public int TimeFlags;
```

Added:

```
public CMTime (long value, int timescale);
        
        public bool IsIndefinite {
                get;
        }
        public bool IsInvalid {
                get;
        }
        public bool IsNegativeInfinity {
                get;
        }
        public bool IsPositiveInfinity {
                get;
        }
        
        public const int MaxTimeScale = 2147483647;
        public static CMTime Invalid;
        public static CMTime Indefinite;
        public static CMTime PositiveInfinity;
        public static CMTime NegativeInfinity;
        public static CMTime Zero;
        public Flags TimeFlags;
        
        [Serializable]
        [Flags]
        public enum Flags {
                Valid,
                HasBeenRounded,
                PositiveInfinity,
                NegativeInfinity,
                Indefinite,
                ImpliedValueFlagsMask
        }
```

 <a name="Namespace:_MonoTouch.CoreText" class="injected"></a>


# Namespace: MonoTouch.CoreText

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontSymbolicTraits" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontSymbolicTraits

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
ColorGlyphs
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontTable" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontTable

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
ExtendedKerning,
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFrameAttributeKey" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFrameAttributeKey

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static readonly MonoTouch.Foundation.NSString ClippingPaths;
        public static readonly MonoTouch.Foundation.NSString PathClippingPath;
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTParagraphStyleSettings" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTParagraphStyleSettings

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public Nullable<float> LineSpacingAdjustment {
                get;
                set;
        }
        public Nullable<float> MaximumLineSpacing {
                get;
                set;
        }
        public Nullable<float> MinimumLineSpacing {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.CoreVideo" class="injected"></a>


# Namespace: MonoTouch.CoreVideo

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="New_Type:_MonoTouch.CoreVideo.CVAttachmentMode" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVAttachmentMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum CVAttachmentMode : uint {
        ShouldNotPropagate,
        ShouldPropagate
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVBuffer" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class CVBuffer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public MonoTouch.Foundation.NSObject GetAttachment (MonoTouch.Foundation.NSString key, out CVAttachmentMode attachmentMode);
        public MonoTouch.Foundation.NSDictionary GetAttachments (CVAttachmentMode attachmentMode);
        public void PropogateAttachments (CVBuffer destinationBuffer);
        public void RemoveAllAttachments ();
        public void RemoveAttachment (MonoTouch.Foundation.NSString key);
        public void SetAttachment (MonoTouch.Foundation.NSString key, MonoTouch.Foundation.NSObject value, CVAttachmentMode attachmentMode);
        public void SetAttachments (MonoTouch.Foundation.NSDictionary theAttachments, CVAttachmentMode attachmentMode);
        
        public IntPtr Handle {
                get;
        }
        
        public static readonly MonoTouch.Foundation.NSString MovieTimeKey;
        public static readonly MonoTouch.Foundation.NSString TimeValueKey;
        public static readonly MonoTouch.Foundation.NSString TimeScaleKey;
        public static readonly MonoTouch.Foundation.NSString PropagatedAttachmentsKey;
        public static readonly MonoTouch.Foundation.NSString NonPropagatedAttachmentsKey;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVFillExtendedPixelsCallBack" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVFillExtendedPixelsCallBack

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public delegate bool CVFillExtendedPixelsCallBack (IntPtr pixelBuffer, IntPtr refCon);
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVFillExtendedPixelsCallBackData" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVFillExtendedPixelsCallBackData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVFillExtendedPixelsCallBackData {
        
        public int Version;
        public CVFillExtendedPixelsCallBack FillCallBack;
        public IntPtr UserInfo;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVImageBuffer" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVImageBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class CVImageBuffer : CVBuffer {
        
        public void Dispose ();
        protected override void Dispose (bool disposing);
        
        public System.Drawing.RectangleF CleanRect {
                get;
        }
        public System.Drawing.SizeF DisplaySize {
                get;
        }
        public System.Drawing.SizeF EncodedSize {
                get;
        }
        public IntPtr Handle {
                get;
        }
        
        public static readonly MonoTouch.Foundation.NSString CGColorSpaceKey;
        public static readonly MonoTouch.Foundation.NSString GammaLevelKey;
        public static readonly MonoTouch.Foundation.NSString CleanApertureKey;
        public static readonly MonoTouch.Foundation.NSString PreferredCleanApertureKey;
        public static readonly MonoTouch.Foundation.NSString CleanApertureWidthKey;
        public static readonly MonoTouch.Foundation.NSString CleanApertureHeightKey;
        public static readonly MonoTouch.Foundation.NSString CleanApertureHorizontalOffsetKey;
        public static readonly MonoTouch.Foundation.NSString CleanApertureVerticalOffsetKey;
        public static readonly MonoTouch.Foundation.NSString FieldCountKey;
        public static readonly MonoTouch.Foundation.NSString FieldDetailKey;
        public static readonly MonoTouch.Foundation.NSString FieldDetailTemporalTopFirst;
        public static readonly MonoTouch.Foundation.NSString FieldDetailTemporalBottomFirst;
        public static readonly MonoTouch.Foundation.NSString FieldDetailSpatialFirstLineEarly;
        public static readonly MonoTouch.Foundation.NSString FieldDetailSpatialFirstLineLate;
        public static readonly MonoTouch.Foundation.NSString PixelAspectRatioKey;
        public static readonly MonoTouch.Foundation.NSString PixelAspectRatioHorizontalSpacingKey;
        public static readonly MonoTouch.Foundation.NSString PixelAspectRatioVerticalSpacingKey;
        public static readonly MonoTouch.Foundation.NSString DisplayDimensionsKey;
        public static readonly MonoTouch.Foundation.NSString DisplayWidthKey;
        public static readonly MonoTouch.Foundation.NSString DisplayHeightKey;
        public static readonly MonoTouch.Foundation.NSString YCbCrMatrixKey;
        public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_ITU_R_709_2;
        public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_ITU_R_601_4;
        public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_SMPTE_240M_1995;
        public static readonly MonoTouch.Foundation.NSString ChromaSubsamplingKey;
        public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_420;
        public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_422;
        public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_411;
        public static readonly MonoTouch.Foundation.NSString TransferFunctionKey;
        public static readonly MonoTouch.Foundation.NSString TransferFunction_ITU_R_709_2;
        public static readonly MonoTouch.Foundation.NSString TransferFunction_SMPTE_240M_1995;
        public static readonly MonoTouch.Foundation.NSString TransferFunction_UseGamma;
        public static readonly MonoTouch.Foundation.NSString ChromaLocationTopFieldKey;
        public static readonly MonoTouch.Foundation.NSString ChromaLocationBottomFieldKey;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_Left;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_Center;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_TopLeft;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_Top;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_BottomLeft;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_Bottom;
        public static readonly MonoTouch.Foundation.NSString ChromaLocation_DV420;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVOptionFlags" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVOptionFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum CVOptionFlags : long {
        None
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelBuffer" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class CVPixelBuffer : CVImageBuffer {
        public static readonly int CVImageBufferType;
        
        public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
        
        public CVReturn FillExtendedPixels ();
        public MonoTouch.Foundation.NSDictionary GetAttributes (MonoTouch.Foundation.NSDictionary[] attributes);
        public IntPtr GetBaseAddress (int planeIndex);
        public int GetBytesPerRowOfPlane (int planeIndex);
        public int GetHeightOfPlane (int planeIndex);
        public int GetWidthtOfPlane (int planeIndex);
        public CVReturn Lock (CVOptionFlags lockFlags);
        public CVReturn Unlock (CVOptionFlags unlockFlags);
        
        public IntPtr BaseAddress {
                get;
        }
        public int BytesPerRow {
                get;
        }
        public int DataSize {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public int Height {
                get;
        }
        public bool IsPlanar {
                get;
        }
        public CVPixelFormatType PixelFormatType {
                get;
        }
        public int PlaneCount {
                get;
        }
        public int Width {
                get;
        }
        
        public static readonly MonoTouch.Foundation.NSString PixelFormatTypeKey;
        public static readonly MonoTouch.Foundation.NSString MemoryAllocatorKey;
        public static readonly MonoTouch.Foundation.NSString WidthKey;
        public static readonly MonoTouch.Foundation.NSString HeightKey;
        public static readonly MonoTouch.Foundation.NSString ExtendedPixelsLeftKey;
        public static readonly MonoTouch.Foundation.NSString ExtendedPixelsTopKey;
        public static readonly MonoTouch.Foundation.NSString ExtendedPixelsRightKey;
        public static readonly MonoTouch.Foundation.NSString ExtendedPixelsBottomKey;
        public static readonly MonoTouch.Foundation.NSString BytesPerRowAlignmentKey;
        public static readonly MonoTouch.Foundation.NSString CGBitmapContextCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString CGImageCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString OpenGLCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString IOSurfacePropertiesKey;
        public static readonly MonoTouch.Foundation.NSString PlaneAlignmentKey;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelBufferLock" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelBufferLock

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum CVPixelBufferLock {
        ReadOnly
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelBufferPool" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelBufferPool

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class CVPixelBufferPool : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CVPixelBufferPool (MonoTouch.Foundation.NSDictionary poolAttributes, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
        
        public CVPixelBuffer CreatePixelBuffer ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public MonoTouch.Foundation.NSDictionary Attributes {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public MonoTouch.Foundation.NSDictionary PixelBufferAttributes {
                get;
        }
        public int TypeID {
                get;
        }
        
        public static readonly MonoTouch.Foundation.NSString MinimumBufferCountKey;
        public static readonly MonoTouch.Foundation.NSString MaximumBufferAgeKey;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelFormatDescription" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelFormatDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public static class CVPixelFormatDescription {
        
        public static MonoTouch.Foundation.NSDictionary Create (int pixelFormat);
        public static void Register (MonoTouch.Foundation.NSDictionary description, int pixelFormat);
        
        public static MonoTouch.Foundation.NSDictionary[] AllTypes {
                get;
        }
        
        public static readonly MonoTouch.Foundation.NSString NameKey;
        public static readonly MonoTouch.Foundation.NSString ConstantKey;
        public static readonly MonoTouch.Foundation.NSString CodecTypeKey;
        public static readonly MonoTouch.Foundation.NSString FourCCKey;
        public static readonly MonoTouch.Foundation.NSString PlanesKey;
        public static readonly MonoTouch.Foundation.NSString BlockWidthKey;
        public static readonly MonoTouch.Foundation.NSString BlockHeightKey;
        public static readonly MonoTouch.Foundation.NSString BitsPerBlockKey;
        public static readonly MonoTouch.Foundation.NSString BlockHorizontalAlignmentKey;
        public static readonly MonoTouch.Foundation.NSString BlockVerticalAlignmentKey;
        public static readonly MonoTouch.Foundation.NSString BlackBlockKey;
        public static readonly MonoTouch.Foundation.NSString HorizontalSubsamplingKey;
        public static readonly MonoTouch.Foundation.NSString VerticalSubsamplingKey;
        public static readonly MonoTouch.Foundation.NSString OpenGLFormatKey;
        public static readonly MonoTouch.Foundation.NSString OpenGLTypeKey;
        public static readonly MonoTouch.Foundation.NSString OpenGLInternalFormatKey;
        public static readonly MonoTouch.Foundation.NSString CGBitmapInfoKey;
        public static readonly MonoTouch.Foundation.NSString QDCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString CGBitmapContextCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString CGImageCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString OpenGLCompatibilityKey;
        public static readonly MonoTouch.Foundation.NSString FillExtendedPixelsCallbackKey;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelFormatType" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelFormatType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum CVPixelFormatType : uint {
        CV1Monochrome,
        CV2Indexed,
        CV4Indexed,
        CV8Indexed,
        CV1IndexedGray_WhiteIsZero,
        CV2IndexedGray_WhiteIsZero,
        CV4IndexedGray_WhiteIsZero,
        CV8IndexedGray_WhiteIsZero,
        CV16BE555,
        CV24RGB,
        CV32ARGB,
        CV16LE555,
        CV16LE5551,
        CV16BE565,
        CV16LE565,
        CV24BGR,
        CV32BGRA,
        CV32ABGR,
        CV32RGBA,
        CV64ARGB,
        CV48RGB,
        CV32AlphaGray,
        CV16Gray,
        CV422YpCbCr8,
        CV4444YpCbCrA8,
        CV4444YpCbCrA8R,
        CV444YpCbCr8,
        CV422YpCbCr16,
        CV422YpCbCr10,
        CV444YpCbCr10,
        CV420YpCbCr8Planar,
        CV420YpCbCr8PlanarFullRange,
        CV422YpCbCr_4A_8BiPlanar,
        CV420YpCbCr8BiPlanarVideoRange,
        CV420YpCbCr8BiPlanarFullRange,
        CV422YpCbCr8_yuvs,
        CV422YpCbCr8FullRange,
        CV30RGB,
        CV4444AYpCbCr8,
        CV4444AYpCbCr16
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPlanarComponentInfo" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPlanarComponentInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVPlanarComponentInfo {
        
        public int Offset;
        public uint RowBytes;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPlanarPixelBufferInfo" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPlanarPixelBufferInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVPlanarPixelBufferInfo {
        
        public CVPlanarComponentInfo[] ComponentInfo;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPlanarPixelBufferInfo_YCbCrPlanar" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPlanarPixelBufferInfo_YCbCrPlanar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVPlanarPixelBufferInfo_YCbCrPlanar {
        
        public CVPlanarComponentInfo ComponentInfoY;
        public CVPlanarComponentInfo ComponentInfoCb;
        public CVPlanarComponentInfo ComponentInfoCr;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVReturn" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVReturn

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum CVReturn {
        Success,
        First,
        Error,
        InvalidArgument,
        AllocationFailed,
        InvalidDisplay,
        DisplayLinkAlreadyRunning,
        DisplayLinkNotRunning,
        DisplayLinkCallbacksNotSet,
        InvalidPixelFormat,
        InvalidSize,
        InvalidPixelBufferAttributes,
        PixelBufferNotOpenGLCompatible,
        PoolAllocationFailed,
        InvalidPoolAttributes,
        Last
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVSMPTETime" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVSMPTETime

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVSMPTETime {
        
        public short Subframes;
        public short SubframeDivisor;
        public uint Counter;
        public uint Type;
        public uint Flags;
        public short Hours;
        public short Minutes;
        public short Seconds;
        public short Frames;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVSMPTETimeFlags" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVSMPTETimeFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum CVSMPTETimeFlags {
        Valid,
        Running
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVSMPTETimeType" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVSMPTETimeType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum CVSMPTETimeType {
        Type24,
        Type25,
        Type30Drop,
        Type30,
        Type2997,
        Type2997Drop,
        Type60,
        Type5994
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVTime" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVTime

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVTime {
        
        public static long GetCurrentHostTime ();
        public static double GetHostClockFrequency ();
        public static int GetHostClockMinimumTimeDelta ();
        public override bool Equals (object other);
        
        public static CVTime IndefiniteTime {
                get;
        }
        public static CVTime ZeroTime {
                get;
        }
        
        public long TimeValue;
        public long TimeScale;
        public int Flags;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVTimeFlags" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVTimeFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum CVTimeFlags {
        IsIndefinite
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVTimeStamp" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVTimeStamp

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct CVTimeStamp {
        
        public uint Version;
        public int VideoTimeScale;
        public long VideoTime;
        public ulong HostTime;
        public double RateScalar;
        public long VideoRefreshPeriod;
        public CVSMPTETime SMPTETime;
        public ulong Flags;
        public ulong Reserved;
}
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVTimeStampFlags" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVTimeStampFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum CVTimeStampFlags {
        VideoTimeValid,
        HostTimeValid,
        SMPTETimeValid,
        VideoRefreshPeriodValid,
        RateScalarValid,
        TopField,
        BottomField,
        VideoHostTimeValid,
        IsInterlaced
}
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, IntPtr ptrToNserror);
        public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, IntPtr ptrToNsError);
```

Added:

```
public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, out MonoTouch.Foundation.NSError error);
        public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, out MonoTouch.Foundation.NSError error);
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static NSString LigatureAttributeName {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSCalculationError" class="injected"></a>


## New Type: MonoTouch.Foundation.NSCalculationError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum NSCalculationError {
        None,
        PrecisionLoss,
        Underflow,
        Overflow,
        DivideByZero
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSDecimal" class="injected"></a>


## New Type: MonoTouch.Foundation.NSDecimal

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public struct NSDecimal {
        
        public static NSCalculationError Add (out NSDecimal result, ref NSDecimal left, ref NSDecimal right, NSRoundingMode mode);
        public static NSComparisonResult Compare (ref NSDecimal left, ref NSDecimal right);
        public static NSCalculationError Divide (out NSDecimal result, ref NSDecimal left, ref NSDecimal right, NSRoundingMode mode);
        public static NSCalculationError Multiply (out NSDecimal result, ref NSDecimal left, ref NSDecimal right, NSRoundingMode mode);
        public static NSComparisonResult MultiplyByPowerOf10 (out NSDecimal result, ref NSDecimal number, short power10, NSRoundingMode mode);
        public static NSCalculationError Normalize (ref NSDecimal number1, ref NSDecimal number2);
        public static NSComparisonResult Power (out NSDecimal result, ref NSDecimal number, int power, NSRoundingMode mode);
        public static void Round (out NSDecimal result, ref NSDecimal number, int scale, NSRoundingMode mode);
        public static NSCalculationError Subtract (out NSDecimal result, ref NSDecimal left, ref NSDecimal right, NSRoundingMode mode);
        public override string ToString ();
        
        public static NSDecimal operator + (NSDecimal left, NSDecimal right);
        public static NSDecimal operator - (NSDecimal left, NSDecimal right);
        public static NSDecimal operator * (NSDecimal left, NSDecimal right);
        public static NSDecimal operator / (NSDecimal left, NSDecimal right);
        public static bool operator == (NSDecimal left, NSDecimal right);
        public static bool operator != (NSDecimal left, NSDecimal right);
        public static implicit operator NSDecimal (int value);
        public static explicit operator int (NSDecimal value);
        
        public int fields;
        public short m1;
        public short m2;
        public short m3;
        public short m4;
        public short m5;
        public short m6;
        public short m7;
        public short m8;
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDecimalNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDecimalNumber

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public NSDecimalNumber (NSDecimal dec);
        public virtual NSDecimal NSDecimalValue {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSDirectoryEnumerationOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSDirectoryEnumerationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum NSDirectoryEnumerationOptions {
        SkipsNone,
        SkipsSubdirectoryDescendants,
        SkipsPackageDescendants,
        SkipsHiddenFiles
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileAttributes" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileAttributes

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class NSFileAttributes {
Type Changed: MonoTouch.Foundation.NSFileManager
```

Removed:

```
public virtual NSDictionary GetAttributes (string path, out NSError error);
```

Added:

```
public bool CreateDirectory (string path, bool createIntermediates, NSFileAttributes attributes);
        public bool CreateDirectory (string path, bool createIntermediates, NSFileAttributes attributes, out NSError error);
        public bool CreateFile (string path, NSData data, NSFileAttributes attributes);
        public NSFileAttributes GetAttributes (string path);
        public NSFileAttributes GetAttributes (string path, out NSError error);
        public bool SetAttributes (NSFileAttributes attributes, string path);
        public bool SetAttributes (NSFileAttributes attributes, string path, out NSError error);
        public virtual bool Copy (NSUrl srcUrl, NSUrl dstUrl, out NSError error);
        public virtual NSUrl[] GetDirectoryContent (NSUrl url, NSArray properties, NSDirectoryEnumerationOptions options, out NSError error);
        public virtual NSDirectoryEnumerator GetEnumerator (NSUrl url, NSArray properties, NSDirectoryEnumerationOptions options, out NSError error);
        public virtual NSUrl[] GetMountedVolumes (NSArray properties, NSVolumeEnumerationOptions options);
        public virtual NSUrl GetUrl (NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl url, bool shouldCreate, out NSError error);
        public virtual NSUrl[] GetUrls (NSSearchPathDirectory directory, NSSearchPathDomain domains);
        public virtual bool Link (NSUrl srcUrl, NSUrl dstUrl, out NSError error);
        public virtual bool Move (NSUrl srcUrl, NSUrl dstUrl, out NSError error);
        public virtual bool Remove (NSUrl url, out NSError error);
        public virtual bool Replace (NSUrl originalItem, NSUrl newItem, string backupItemName, NSFileManagerItemReplacementOptions options, out NSUrl resultingURL, out NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileManagerItemReplacementOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileManagerItemReplacementOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSFileManagerItemReplacementOptions
```

Added:

```
[Serializable]
 [Flags]
 public enum NSFileManagerItemReplacementOptions {
        None,
        UsingNewMetadataOnly,
        WithoutDeletingBackupItem
 }
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileType" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum NSFileType {
        Directory,
        Regular,
        SymbolicLink,
        Socket,
        CharacterSpecial,
        BlockSpecial,
        Unknown
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumber

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual NSDecimal NSDecimalValue {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void SetValueForKeyPath (IntPtr handle, NSString keyPath);
```

 <a name="New_Type:_MonoTouch.Foundation.NSRoundingMode" class="injected"></a>


## New Type: MonoTouch.Foundation.NSRoundingMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum NSRoundingMode {
        Plain,
        Down,
        Up,
        Bankers
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void Stop ();
        public void WakeUp ();
```

 <a name="New_Type:_MonoTouch.Foundation.NSSearchPathDirectory" class="injected"></a>


## New Type: MonoTouch.Foundation.NSSearchPathDirectory

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public enum NSSearchPathDirectory {
        ApplicationDirectory,
        DemoApplicationDirectory,
        DeveloperApplicationDirectory,
        AdminApplicationDirectory,
        LibraryDirectory,
        DeveloperDirectory,
        UserDirectory,
        DocumentationDirectory,
        DocumentDirectory,
        CoreServiceDirectory,
        AutosavedInformationDirectory,
        DesktopDirectory,
        CachesDirectory,
        ApplicationSupportDirectory,
        DownloadsDirectory,
        InputMethodsDirectory,
        MoviesDirectory,
        MusicDirectory,
        PicturesDirectory,
        PrinterDescriptionDirectory,
        SharedPublicDirectory,
        PreferencePanesDirectory,
        ItemReplacementDirectory,
        AllApplicationsDirectory,
        AllLibrariesDirectory
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSSearchPathDomain" class="injected"></a>


## New Type: MonoTouch.Foundation.NSSearchPathDomain

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum NSSearchPathDomain {
        None,
        User,
        Local,
        Network,
        System,
        All
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStringDrawingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStringDrawingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
Could not find MonoTouch.Foundation.NSStringDrawingOptions
```

Added:

```
[Serializable]
 public enum NSStringDrawingOptions : uint {
        UsesLineFragmentOrigin,
        UsesFontLeading,
        DisableScreenFontSubstitution,
        UsesDeviceMetrics,
        OneShot,
        TruncatesLastVisibleLine
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnection" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static NSData SendSynchronousRequest (NSUrlRequest request, out NSUrlResponse response, out NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocol" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocol

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocol : NSObject {
        
        public NSUrlProtocol ();
        public NSUrlProtocol (NSCoder coder);
        public NSUrlProtocol (NSObjectFlag t);
        public NSUrlProtocol (IntPtr handle);
        public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, NSUrlProtocolClient client);
        
        public static NSUrlRequest GetCanonicalRequest (NSUrlRequest forRequest);
        public static NSObject GetProperty (string key, NSUrlRequest inRequest);
        public static bool IsRequestCacheEquivalent (NSUrlRequest first, NSUrlRequest second);
        public static bool RegisterClass (MonoTouch.ObjCRuntime.Class protocolClass);
        public static void RemoveProperty (string propertyKey, NSMutableUrlRequest request);
        public static void SetProperty (NSObject value, string key, NSMutableUrlRequest inRequest);
        public static void UnregisterClass (MonoTouch.ObjCRuntime.Class protocolClass);
        public virtual bool CanInitWithRequest (NSUrlRequest request);
        public virtual void StartLoading ();
        public virtual void StopLoading ();
        
        public virtual NSCachedUrlResponse CachedResponse {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public NSUrlProtocolClient Client {
                get;
                set;
        }
        public virtual NSUrlRequest Request {
                get;
        }
        public virtual NSObject WeakClient {
                get;
                set;
        }
        
        public event EventHandler<NSUrlProtocolCachedResponseEventArgs> CachedResponseIsValid;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> CancelledAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolDataEventArgs> DataLoaded;
        public event EventHandler<NSUrlProtocolErrorEventArgs> FailedWithError;
        public event EventHandler FinishedLoading;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> ReceivedAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolResponseEventArgs> ReceivedResponse;
        public event EventHandler<NSUrlProtocolRedirectEventArgs> Redirected;
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolCachedResponseEventArgs : EventArgs {
        
        public NSUrlProtocolCachedResponseEventArgs (NSCachedUrlResponse cachedResponse);
        
        public NSCachedUrlResponse CachedResponse {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolChallengeEventArgs : EventArgs {
        
        public NSUrlProtocolChallengeEventArgs (NSUrlAuthenticationChallenge challenge);
        
        public NSUrlAuthenticationChallenge Challenge {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolClient" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolClient

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public abstract class NSUrlProtocolClient : NSObject {
        
        public NSUrlProtocolClient ();
        public NSUrlProtocolClient (NSCoder coder);
        public NSUrlProtocolClient (NSObjectFlag t);
        public NSUrlProtocolClient (IntPtr handle);
        
        public abstract void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
        public abstract void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void DataLoaded (NSUrlProtocol protocol, NSData data);
        public abstract void FailedWithError (NSUrlProtocol protocol, NSError error);
        public abstract void FinishedLoading (NSUrlProtocol protocol);
        public abstract void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        public abstract void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolDataEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolDataEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolDataEventArgs : EventArgs {
        
        public NSUrlProtocolDataEventArgs (NSData data);
        
        public NSData Data {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolErrorEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolErrorEventArgs : EventArgs {
        
        public NSUrlProtocolErrorEventArgs (NSError error);
        
        public NSError Error {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolRedirectEventArgs : EventArgs {
        
        public NSUrlProtocolRedirectEventArgs (NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
        
        public NSUrlRequest RedirectedToEequest {
                get;
                set;
        }
        public NSUrlResponse RedirectResponse {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolResponseEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolResponseEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public class NSUrlProtocolResponseEventArgs : EventArgs {
        
        public NSUrlProtocolResponseEventArgs (NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        
        public NSUrlCacheStoragePolicy Policy {
                get;
                set;
        }
        public NSUrlResponse Response {
                get;
                set;
        }
 }
```

 <a name="New_Type:_MonoTouch.Foundation.NSVolumeEnumerationOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSVolumeEnumerationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
[Flags]
public enum NSVolumeEnumerationOptions {
        None,
        SkipHiddenVolumes,
        ProduceFileReferenceUrls
}
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


# Namespace: MonoTouch.ImageIO

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.ImageIO.CGImageDestination" class="injected"></a>


## Type Changed: MonoTouch.ImageIO.CGImageDestination

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public void Close ();
```

Added:

```
public bool Close ();
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapPoint" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapPoint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.CoreLocation.CLLocationCoordinate2D ToCoordinate (MKMapPoint mapPoint);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapRect" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapRect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public MKMapRect World {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapSize" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapSize

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MKMapSize World {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygon" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygon

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual MKPolygon InteriorPolygons {
```

Added:

```
public virtual MKPolygon[] InteriorPolygons {
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolyline" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolyline

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
        }
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static bool CanFilterByProperty (MonoTouch.Foundation.NSString property);
        public virtual MonoTouch.Foundation.NSObject ValueForProperty (MonoTouch.Foundation.NSString property);
        public static MonoTouch.Foundation.NSString AlbumArtistPersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AlbumArtistProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AlbumPersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AlbumTitleProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AlbumTrackCountProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AlbumTrackNumberProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ArtistPersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ArtistProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ArtworkProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString AssetURLProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString BeatsPerMinuteProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString CommentsProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ComposerPersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ComposerProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString DiscCountProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString DiscNumberProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString GenrePersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString GenreProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString IsCompilationProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString LastPlayedDateProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString LyricsProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString MediaTypeProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackDurationProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString PlayCountProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString PodcastPersistentIDProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString PodcastTitleProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString RatingProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString ReleaseDateProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString SkipCountProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString TitleProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString UserGroupingProperty {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemArtwork" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemArtwork

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.RectangleF size);
```

Added:

```
public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.SizeF size);
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMovieAccessLog" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMovieAccessLog

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class MPMovieAccessLog : MonoTouch.Foundation.NSObject {
        
        public MPMovieAccessLog ();
        public MPMovieAccessLog (MonoTouch.Foundation.NSCoder coder);
        public MPMovieAccessLog (MonoTouch.Foundation.NSObjectFlag t);
        public MPMovieAccessLog (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MPMovieAccessLogEvent[] Events {
                get;
        }
        public virtual MonoTouch.Foundation.NSData ExtendedLogData {
                get;
        }
        public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMovieAccessLogEvent" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMovieAccessLogEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class MPMovieAccessLogEvent : MonoTouch.Foundation.NSObject {
        
        public MPMovieAccessLogEvent ();
        public MPMovieAccessLogEvent (MonoTouch.Foundation.NSCoder coder);
        public MPMovieAccessLogEvent (MonoTouch.Foundation.NSObjectFlag t);
        public MPMovieAccessLogEvent (IntPtr handle);
        
        public virtual long BytesTransferred {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int DroppedVideoFrameCount {
                get;
        }
        public virtual double DurationWatched {
                get;
        }
        public virtual double IndicatedBitrate {
                get;
        }
        public virtual double ObservedBitrate {
                get;
        }
        public virtual string PlaybackSessionID {
                get;
        }
        public virtual MonoTouch.Foundation.NSData PlaybackStartDate {
                get;
        }
        public virtual double PlaybackStartOffset {
                get;
        }
        public virtual int SegmentedDownloadedCount {
                get;
        }
        public virtual double SegmentsDownloadedDuration {
                get;
        }
        public virtual string ServerAddress {
                get;
        }
        public virtual int ServerAddressChangeCount {
                get;
        }
        public virtual int StallCount {
                get;
        }
        public virtual string Uri {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMovieErrorLog" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMovieErrorLog

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class MPMovieErrorLog : MonoTouch.Foundation.NSObject {
        
        public MPMovieErrorLog ();
        public MPMovieErrorLog (MonoTouch.Foundation.NSCoder coder);
        public MPMovieErrorLog (MonoTouch.Foundation.NSObjectFlag t);
        public MPMovieErrorLog (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MPMovieErrorLogEvent[] Events {
                get;
        }
        public virtual MonoTouch.Foundation.NSData ExtendedLogData {
                get;
        }
        public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMovieErrorLogEvent" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMovieErrorLogEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class MPMovieErrorLogEvent : MonoTouch.Foundation.NSObject {
        
        public MPMovieErrorLogEvent ();
        public MPMovieErrorLogEvent (MonoTouch.Foundation.NSCoder coder);
        public MPMovieErrorLogEvent (MonoTouch.Foundation.NSObjectFlag t);
        public MPMovieErrorLogEvent (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate Date {
                get;
        }
        public virtual string ErrorComment {
                get;
        }
        public virtual string ErrorDomain {
                get;
        }
        public virtual int ErrorStatusCode {
                get;
        }
        public virtual string PlaybackSessionID {
                get;
        }
        public virtual string ServerAddress {
                get;
        }
        public virtual string Uri {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static MonoTouch.Foundation.NSString DidEnterFullscreenNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidExitFullscreenNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DurationAvailableNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString FullscreenAnimationCurveUserInfoKey {
                get;
        }
        public static MonoTouch.Foundation.NSString FullscreenAnimationDurationUserInfoKey {
                get;
        }
        public static MonoTouch.Foundation.NSString LoadStateDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString NaturalSizeAvailableNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString NowPlayingMovieDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackDidFinishNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackDidFinishReasonUserInfoKey {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackStateDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ScalingModeDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString SourceTypeAvailableNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ThumbnailErrorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ThumbnailImageKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ThumbnailImageRequestDidFinishNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ThumbnailTimeKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataKeyDataType {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataKeyInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataKeyLanguageCode {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataKeyMIMEType {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataKeyName {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataUpdatedNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TimedMetadataUserInfoKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TypesAvailableNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WillEnterFullscreenNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WillExitFullscreenNotification {
                get;
        }
        public virtual MPMovieAccessLog AccessLog {
                get;
        }
        public virtual bool AllowsAirPlay {
                get;
        }
        public virtual MPMovieErrorLog ErrorLog {
                get;
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.BlockDescriptor" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.BlockDescriptor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public int reserved;
        public int size;
```

Added:

```
public IntPtr reserved;
        public IntPtr size;
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.Dlfcn

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public static class Dlfcn {
        
        public static int dlclose (IntPtr handle);
        public static string dlerror ();
        public static IntPtr dlopen (string path, int mode);
        public static double GetDouble (IntPtr handle, string symbol);
        public static IntPtr GetIndirect (IntPtr handle, string symbol);
        public static int GetInt32 (IntPtr handle, string symbol);
        public static IntPtr GetIntPtr (IntPtr handle, string symbol);
        public static MonoTouch.Foundation.NSNumber GetNSNumber (IntPtr handle, string symbol);
        public static MonoTouch.Foundation.NSString GetStringConstant (IntPtr handle, string symbol);
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Runtime" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Runtime

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public static void ConnectMethod (System.Reflection.MethodInfo method, Selector selector);
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual void ProtectedDataDidBecomeUnavailable (UIApplication application);
```

Added:

```
public virtual void ProtectedDataDidBecomeAvailable (UIApplication application);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public UIButton (UIButtonType type);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIControlEvent" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIControlEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
[Flags]
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIFont" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIFont

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual float LineHeight {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureProbe" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureProbe

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public delegate bool UIGestureProbe (UIGestureRecognizer otherGestureRecognizer);
```

Added:

```
public delegate bool UIGestureProbe (UIGestureRecognizer recognizer);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public Token AddTarget (MonoTouch.Foundation.NSAction action);
        public void RemoveTarget (Token token);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer otherGestureRecognizer);
```

Added:

```
public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
```

 <a name="New_Type:_MonoTouch.UIKit.UIGesturesProbe" class="injected"></a>


## New Type: MonoTouch.UIKit.UIGesturesProbe

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public delegate bool UIGesturesProbe (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreen" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreen

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual UIScreen MirroredScreen {
                get;
        }
        public virtual UIScreenMode PreferredMode {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public void AddSubviews (params UIView[] views);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
public virtual bool DisablesAutomaticKeyboardDismissal {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Added:

```
set;
```

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

 <a name="Type_Changed:_MonoTouch.iAd.ADError" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
BannerVisibleWithoutContent
```

Added:

```
BannerVisibleWithoutContent,
        ApplicationInactive
```

 <a name="Type_Changed:_MonoTouch.iAd.ADErrorEventArgs" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

Removed:

```
Could not find MonoTouch.iAd.ADErrorEventArgs
```

Added:

```
public class ADErrorEventArgs : EventArgs {
        
        public ADErrorEventArgs (MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
 }
```

 <a name="New_Type:_MonoTouch.iAd.ADInterstitialAd" class="injected"></a>


## New Type: MonoTouch.iAd.ADInterstitialAd

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public class ADInterstitialAd : MonoTouch.Foundation.NSObject {
        
        public ADInterstitialAd ();
        public ADInterstitialAd (MonoTouch.Foundation.NSCoder coder);
        public ADInterstitialAd (MonoTouch.Foundation.NSObjectFlag t);
        public ADInterstitialAd (IntPtr handle);
        
        public virtual void CancelAction ();
        public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
        public virtual bool PresentInView (MonoTouch.UIKit.UIView containerView);
        
        public virtual bool ActionInProgress {
                get;
        }
        public ADPredicate ActionShouldBegin {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public ADInterstitialAdDelegate Delegate {
                get;
                set;
        }
        public virtual bool Loaded {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler ActionFinished;
        public event EventHandler AdLoaded;
        public event EventHandler AdUnloaded;
        public event EventHandler<aderroreventargs> FailedToReceiveAd; } </aderroreventargs>
```

 <a name="New_Type:_MonoTouch.iAd.ADInterstitialAdDelegate" class="injected"></a>


## New Type: MonoTouch.iAd.ADInterstitialAdDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
public abstract class ADInterstitialAdDelegate : MonoTouch.Foundation.NSObject {
        
        public ADInterstitialAdDelegate ();
        public ADInterstitialAdDelegate (MonoTouch.Foundation.NSCoder coder);
        public ADInterstitialAdDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public ADInterstitialAdDelegate (IntPtr handle);
        
        public abstract void ActionFinished (ADInterstitialAd interstitialAd);
        public abstract bool ActionShouldBegin (ADInterstitialAd interstitialAd, bool willLeaveApplication);
        public abstract void AdLoaded (ADInterstitialAd interstitialAd);
        public abstract void AdUnloaded (ADInterstitialAd interstitialAd);
        public abstract void FailedToReceiveAd (ADInterstitialAd interstitialAd, MonoTouch.Foundation.NSError error);
}
```

 <a name="New_Type:_MonoTouch.iAd.ADPredicate" class="injected"></a>


## New Type: MonoTouch.iAd.ADPredicate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.6_to_4.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_4/MonoTouch_4.0.0#)

```
[Serializable]
public delegate bool ADPredicate (ADInterstitialAd interstitialAd, bool willLeaveApplication);
```
