---
id: 81B3CED7-96E3-C759-4B63-97EA138BB17B
title: "From 4.2 to 5.0"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public const string Version = "4.2";
```

Added:

```
public const string Version = "5.0";
        public const string AccountsLibrary = "/System/Library/Frameworks/Accounts.framework/Accounts";
        public const string CoreDataLibrary = "/System/Library/Frameworks/CoreData.framework/CoreData";
        public const string CoreImageLibrary = "/System/Library/Frameworks/CoreImage.framework/CoreImage";
        public const string GLKitLibrary = "/System/Library/Frameworks/GLKit.framework/GLKit";
        public const string MessageUILibrary = "/System/Library/Frameworks/MessageUI.framework/MessageUI";
        public const string CoreBluetoothLibrary = "/System/Library/Frameworks/CoreBluetooth.framework/CoreBluetooth";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static AVAsset FromUrl (MonoTouch.Foundation.NSUrl url);
        public virtual AVMediaSelectionGroup MediaSelectionGroupForMediaCharacteristic (string avMediaCharacteristic);
        public virtual string [] AvailableMediaCharacteristicsWithMediaSelectionOptions {
                get;
        }
        public virtual bool CompatibleWithSavedPhotosAlbum {
                get;
        }
        public virtual AVMetadataItem CreationDate {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual AVAsset Asset {
                get;
        }
        public virtual long EstimatedOutputFileLength {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGenerator" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class AVAssetImageGenerator : MonoTouch.Foundation.NSObject {
        
        public AVAssetImageGenerator ();
        public AVAssetImageGenerator (MonoTouch.Foundation.NSCoder coder);
        public AVAssetImageGenerator (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetImageGenerator (IntPtr handle);
        public AVAssetImageGenerator (AVAsset asset);
        
        public static AVAssetImageGenerator FromAsset (AVAsset asset);
        public virtual void CancelAllCGImageGeneration ();
        public virtual MonoTouch.CoreGraphics.CGImage CopyCGImageAtTime (MonoTouch.CoreMedia.CMTime requestedTime, MonoTouch.CoreMedia.CMTime actualTime, MonoTouch.Foundation.NSError outError);
        protected override void Dispose (bool disposing);
        public virtual void GenerateCGImagesAsynchronously (MonoTouch.Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
        
        public static MonoTouch.Foundation.NSString ApertureModeCleanAperture {
                get;
        }
        public static MonoTouch.Foundation.NSString ApertureModeEncodedPixels {
                get;
        }
        public static MonoTouch.Foundation.NSString ApertureModeProductionAperture {
                get;
        }
        public virtual MonoTouch.Foundation.NSString ApertureMode {
                get;
                set;
        }
        public virtual bool AppliesPreferredTrackTransform {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Drawing.SizeF MaximumSize {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMTime RequestedTimeToleranceAfter {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMTime RequestedTimeToleranceBefore {
                get;
                set;
        }
        public virtual AVVideoComposition VideoComposition {
                get;
                set;
        }
 }
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGeneratorCompletionHandler 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void AVAssetImageGeneratorCompletionHandler (MonoTouch.CoreMedia.CMTime requestedTime, IntPtr imageRef, MonoTouch.CoreMedia.CMTime actualTime, AVAssetImageGeneratorResult result, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGeneratorResult" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGeneratorResult

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum AVAssetImageGeneratorResult {
        Succeeded,
        Failed,
        Cancelled
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool AlwaysCopiesSampleData {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReferenceRestrictions" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReferenceRestrictions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum AVAssetReferenceRestrictions {
        ForbidNone,
        ForbidRemoteReferenceToLocal,
        ForbidLocalReferenceToRemote,
        ForbidCrossSiteReference,
        ForbidLocalReferenceToLocal,
        ForbidAll
 }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetTrack

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool Playable {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

These changes are source-code compatible, but will promote the use of the
NSString APIs as they are really keys that happen to be stored in NSStrings.

Removed:

```
public bool SetCategory (string theCategory, MonoTouch.Foundation.NSError outError);
        public bool SetCategory (string theCategory, out MonoTouch.Foundation.NSError outError);
        public virtual string Category {
        public static MonoTouch.Foundation.NSString CategoryAmbient;
        public static MonoTouch.Foundation.NSString CategorySoloAmbient;
        public static MonoTouch.Foundation.NSString CategoryPlayback;
        public static MonoTouch.Foundation.NSString CategoryRecord;
        public static MonoTouch.Foundation.NSString CategoryPlayAndRecord;
        public static MonoTouch.Foundation.NSString CategoryAudioProcessing;
```

Added:

```
public bool SetCategory (MonoTouch.Foundation.NSString theCategory, MonoTouch.Foundation.NSError outError);
        public bool SetCategory (MonoTouch.Foundation.NSString theCategory, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetMode (MonoTouch.Foundation.NSString mode, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSString CategoryAmbient {
                get;
        }
        public static MonoTouch.Foundation.NSString CategoryAudioProcessing {
                get;
        }
        public static MonoTouch.Foundation.NSString CategoryPlayAndRecord {
                get;
        }
        public static MonoTouch.Foundation.NSString CategoryPlayback {
                get;
        }
        public static MonoTouch.Foundation.NSString CategoryRecord {
                get;
        }
        public static MonoTouch.Foundation.NSString CategorySoloAmbient {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeDefault {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeGameChat {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeMeasurement {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeVideoRecording {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeVoiceChat {
                get;
        }
        public virtual MonoTouch.Foundation.NSString Category {
        public virtual MonoTouch.Foundation.NSString Mode {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureConnection" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public bool SupportsVideoMaxFrameDuration {
                get;
        }
        public bool SupportsVideoMinFrameDuration {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTime VideoMaxFrameDuration {
                get;
                set;
        }
        public virtual float VideoMaxScaleAndCropFactor {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTime VideoMinFrameDuration {
                get;
                set;
        }
        public virtual float VideoScaleAndCropFactor {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString SubjectAreaDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WasConnectedNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString WasDisconnectedNotification {
                get;
        }
        public virtual bool FlashActive {
                get;
        }
        public virtual bool FlashAvailable {
                get;
        }
        public virtual bool TorchAvailable {
                get;
        }
        public virtual float TorchLevel {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual AVCaptureConnection ConnectionFromMediaType (MonoTouch.Foundation.NSString avMediaType);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString Preset352x288 {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetiFrame1280x720 {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetiFrame960x540 {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureStillImageOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool CapturingStillImage {
                get;
        }
                set;
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoDataOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public virtual void SetSampleBufferDelegatequeue (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, IntPtr sampleBufferCallbackQueue);
```

Added:

```
public virtual void SetSampleBufferDelegate (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, IntPtr sampleBufferCallbackQueue);
        public virtual MonoTouch.Foundation.NSString[] AvailableVideoCodecTypes {
                get;
        }
        public virtual MonoTouch.Foundation.NSNumber[] AvailableVideoCVPixelFormatTypes {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCompletion" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCompletion

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void AVCompletion (bool finished);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
OperationNotSupportedForAsset,
        DecoderTemporarilyUnavailable,
        EncoderTemporarilyUnavailable,
        InvalidVideoComposition,
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMediaCharacteristic" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMediaCharacteristic

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString ContainsOnlyForcedSubtitles {
                get;
        }
        public static MonoTouch.Foundation.NSString DescribesMusicAndSoundForAccessibility {
                get;
        }
        public static MonoTouch.Foundation.NSString DescribesVideoForAccessibility {
                get;
        }
        public static MonoTouch.Foundation.NSString IsAuxiliaryContent {
                get;
        }
        public static MonoTouch.Foundation.NSString IsMainProgramContent {
                get;
        }
        public static MonoTouch.Foundation.NSString TranscribesSpokenDialogForAccessibility {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMediaSelectionGroup" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMediaSelectionGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class AVMediaSelectionGroup : MonoTouch.Foundation.NSObject {
        
        public AVMediaSelectionGroup ();
        public AVMediaSelectionGroup (MonoTouch.Foundation.NSCoder coder);
        public AVMediaSelectionGroup (MonoTouch.Foundation.NSObjectFlag t);
        public AVMediaSelectionGroup (IntPtr handle);
        
        public static AVMediaSelectionOption[] MediaSelectionOptions (AVMediaSelectionOption[] source, MonoTouch.Foundation.NSLocale locale);
        public static AVMediaSelectionOption[] MediaSelectionOptions (AVMediaSelectionOption[] source, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
        public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (MonoTouch.Foundation.NSArray array, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
        public static AVMediaSelectionOption[] PlayableMediaSelectionOptions (AVMediaSelectionOption[] source);
        protected override void Dispose (bool disposing);
        public virtual AVMediaSelectionOption GetMediaSelectionOptionForPropertyList (MonoTouch.Foundation.NSObject propertyList);
        
        public virtual bool AllowsEmptySelection {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVMediaSelectionOption[] Options {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMediaSelectionOption" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMediaSelectionOption

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class AVMediaSelectionOption : MonoTouch.Foundation.NSObject {
        
        public AVMediaSelectionOption ();
        public AVMediaSelectionOption (MonoTouch.Foundation.NSCoder coder);
        public AVMediaSelectionOption (MonoTouch.Foundation.NSObjectFlag t);
        public AVMediaSelectionOption (IntPtr handle);
        
        public virtual AVMediaSelectionOption AssociatedMediaSelectionOptionInMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
        protected override void Dispose (bool disposing);
        public virtual AVMetadataItem[] GetMetadataForFormat (string format);
        public virtual bool HasMediaCharacteristic (string mediaCharacteristic);
        
        public virtual string [] AvailableMetadataFormats {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVMetadataItem[] CommonMetadata {
                get;
        }
        public virtual MonoTouch.Foundation.NSLocale Locale {
                get;
        }
        public virtual MonoTouch.Foundation.NSNumber[] MediaSubTypes {
                get;
        }
        public virtual string MediaType {
                get;
        }
        public virtual bool Playable {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject PropertyList {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool InsertTimeRanges (MonoTouch.Foundation.NSValue cmTimeRanges, AVAssetTrack[] tracks, MonoTouch.CoreMedia.CMTime startTime, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletionHandler completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
        public virtual bool AirPlayVideoActive {
                get;
        }
        public virtual bool AllowsAirPlayVideo {
                get;
                set;
        }
        public virtual bool UsesAirPlayVideoWhileAirPlayScreenIsActive {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void CancelPendingSeeks ();
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletion completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
        public virtual AVMediaSelectionOption SelectedMediaOption (AVMediaSelectionGroup inMediaSelectionGroup);
        public virtual void SelectMediaOption (AVMediaSelectionOption mediaSelectionOption, AVMediaSelectionGroup mediaSelectionGroup);
        public static MonoTouch.Foundation.NSString TimeJumpedNotification {
                get;
        }
        public virtual bool CanPlayFastForward {
                get;
        }
        public virtual bool CanPlayFastReverse {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVUrlAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVUrlAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static bool IsPlayable (string extendedMimeType);
        public static string [] AudiovisualMimeTypes {
                get;
        }
        public static string [] AudiovisualTypes {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideo" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString ProfileLevelH464Baseline41 {
                get;
        }
        public static MonoTouch.Foundation.NSString ProfileLevelH464Main32 {
                get;
        }
        public static MonoTouch.Foundation.NSString ProfileLevelH464Main41 {
                get;
        }
        public static MonoTouch.Foundation.NSString QualityKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideoComposition" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoComposition

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool IsValidForAsset (AVAsset asset, MonoTouch.CoreMedia.CMTimeRange timeRange, AVVideoCompositionValidationHandling validationDelegate);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoCompositionValidationHandling 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class AVVideoCompositionValidationHandling : MonoTouch.Foundation.NSObject {
        
        public AVVideoCompositionValidationHandling ();
        public AVVideoCompositionValidationHandling (MonoTouch.Foundation.NSCoder coder);
        public AVVideoCompositionValidationHandling (MonoTouch.Foundation.NSObjectFlag t);
        public AVVideoCompositionValidationHandling (IntPtr handle);
        
        public virtual bool ShouldContinueValidatingAfterFindingEmptyTimeRange (AVVideoComposition videoComposition, MonoTouch.CoreMedia.CMTimeRange timeRange);
        public virtual bool ShouldContinueValidatingAfterFindingInvalidTimeRangeInInstruction (AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction);
        public virtual bool ShouldContinueValidatingAfterFindingInvalidTrackIDInInstruction (AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction, AVVideoCompositionLayerInstruction layerInstruction, AVAsset asset);
        public virtual bool ShouldContinueValidatingAfterFindingInvalidValueForKey (AVVideoComposition videoComposition, string key);
 }
```

 <a name="Namespace:_MonoTouch.Accounts" class="injected"></a>


# Namespace: MonoTouch.Accounts

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.Accounts.ACAccount" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccount

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class ACAccount : MonoTouch.Foundation.NSObject {
        
        public ACAccount ();
        public ACAccount (MonoTouch.Foundation.NSCoder coder);
        public ACAccount (MonoTouch.Foundation.NSObjectFlag t);
        public ACAccount (IntPtr handle);
        public ACAccount (ACAccountType type);
        
        protected override void Dispose (bool disposing);
        
        public virtual string AccountDescription {
                get;
                set;
        }
        public virtual ACAccountType AccountType {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual ACAccountCredential Credential {
                get;
                set;
        }
        public virtual string ErrorDomain {
                get;
        }
        public virtual string Identifier {
                get;
        }
        public virtual string Username {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACAccountCredential" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccountCredential

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class ACAccountCredential : MonoTouch.Foundation.NSObject {
        
        public ACAccountCredential ();
        public ACAccountCredential (MonoTouch.Foundation.NSCoder coder);
        public ACAccountCredential (MonoTouch.Foundation.NSObjectFlag t);
        public ACAccountCredential (IntPtr handle);
        public ACAccountCredential (string token, string secret);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACAccountStore" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccountStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class ACAccountStore : MonoTouch.Foundation.NSObject {
        
        public ACAccountStore ();
        public ACAccountStore (MonoTouch.Foundation.NSCoder coder);
        public ACAccountStore (MonoTouch.Foundation.NSObjectFlag t);
        public ACAccountStore (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual ACAccount FindAccount (string identifier);
        public virtual ACAccount[] FindAccounts (ACAccountType accountType);
        public virtual ACAccountType FindAccountType (string typeIdentifier);
        public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
        public virtual void SaveAccount (ACAccount account, ACAccountStoreSaveCompletionHandler completionHandler);
        
        public static MonoTouch.Foundation.NSString ChangeNotification {
                get;
        }
        public virtual ACAccount[] Accounts {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACAccountStoreSaveCompletionHandler" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccountStoreSaveCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void ACAccountStoreSaveCompletionHandler (bool success, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.Accounts.ACAccountType" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccountType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class ACAccountType : MonoTouch.Foundation.NSObject {
        
        public ACAccountType ();
        public ACAccountType (MonoTouch.Foundation.NSCoder coder);
        public ACAccountType (MonoTouch.Foundation.NSObjectFlag t);
        public ACAccountType (IntPtr handle);
        
        public static MonoTouch.Foundation.NSString Twitter {
                get;
        }
        public virtual bool AccessGranted {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Description {
                get;
        }
        public virtual string Identifier {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACErrorCode" class="injected"></a>


## New Type: MonoTouch.Accounts.ACErrorCode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum ACErrorCode {
        Unknown,
        AccountMissingRequiredProperty,
        AccountAuthenticationFailed,
        AccountTypeInvalid,
        AccountAlreadyExits,
        AccountNotFound,
        PermissionDenied
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACRequestCompletionHandler" class="injected"></a>


## New Type: MonoTouch.Accounts.ACRequestCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void ACRequestCompletionHandler (bool granted, MonoTouch.Foundation.NSError error);
```

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


# Namespace: MonoTouch.AddressBook

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPerson" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPerson

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public ABMultiValue`1 GetSocialProfile ();
        public void SetSocialProfile (ABMultiValue`1 value);
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPersonProperty" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPersonProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
SocialProfile
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPersonSocialProfile" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPersonSocialProfile

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static class ABPersonSocialProfile {
 }
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABRecordType" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABRecordType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
Source
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAsset" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual MonoTouch.CoreGraphics.CGImage AspectRatioThumbnail ();
        public virtual void SetImageData (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void SetVideoAtPath (MonoTouch.Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteModifiedImageToSavedToPhotosAlbum (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual void WriteModifiedVideoToSavedPhotosAlbum (MonoTouch.Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
        public virtual bool Editable {
                get;
        }
        public virtual ALAsset OriginalAsset {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetRepresentation" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetRepresentation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual string Filename {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsGroup" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool AddAsset (ALAsset asset);
        public virtual bool Editable {
                get;
        }
        public MonoTouch.Foundation.NSUrl PropertyUrl {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void AddAssetsGroupAlbum (string name, ALAssetsLibraryGroupResult resultBlock, ALAssetsLibraryAccessFailure failureBlock);
        public virtual void GroupForUrl (MonoTouch.Foundation.NSUrl groupURL, ALAssetsLibraryGroupResult resultBlock, ALAssetsLibraryAccessFailure failureBlock);
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibraryAccessFailure" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryAccessFailure

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryAccessFailure (MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibraryGroupResult" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibraryGroupResult

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void ALAssetsLibraryGroupResult (ALAssetsGroup group);
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFile" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFile

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public int Write (long startingByte, byte [] buffer, int offset, int count, bool useCache, out int errorCode);
        public int WritePackets (bool useCache, long startingPacket, AudioStreamPacketDescription[] packetDescriptions, byte [] buffer, int offset, int count, out int errorCode);
        public int WritePackets (bool useCache, long inStartingPacket, AudioStreamPacketDescription[] inPacketDescriptions, IntPtr buffer, int count, out int errorCode);
        public MonoTouch.Foundation.NSData AlbumArtwork {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFileProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFileProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
SourceBitDepth,
        AlbumArtwork
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
// This was an abstract class with only two possible
        // implementations, so the public constructor has been
        // removed
        public AudioQueue ();
```

Added:

```
public uint ConverterError {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueueProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
DecodeBufferSizeFrames,
        ConverterError
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueStatus" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueueStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
RecordUnderrun,
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioSource" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public AudioSource ();
        protected void Initialize (AudioFileType inFileType, AudioStreamBasicDescription format);
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.CoreAnimation.CAEmitterCell" class="injected"></a>


## New Type: MonoTouch.CoreAnimation.CAEmitterCell

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CAEmitterCell : MonoTouch.Foundation.NSObject {
        
        public CAEmitterCell ();
        public CAEmitterCell (MonoTouch.Foundation.NSCoder coder);
        public CAEmitterCell (MonoTouch.Foundation.NSObjectFlag t);
        public CAEmitterCell (IntPtr handle);
        
        public static MonoTouch.Foundation.NSObject DefaultValueForKey (string key);
        public static CAEmitterCell EmitterCell ();
        protected override void Dispose (bool disposing);
        public virtual bool ShouldArchiveValueForKey (string key);
        
        public virtual float AccelerationX {
                get;
                set;
        }
        public virtual float AccelerationY {
                get;
                set;
        }
        public virtual float AccelerationZ {
                get;
                set;
        }
        public virtual float AlphaRange {
                get;
                set;
        }
        public virtual float AlphaSpeed {
                get;
                set;
        }
        public virtual float BirthRate {
                get;
                set;
        }
        public virtual float BlueRange {
                get;
                set;
        }
        public virtual float BlueSpeed {
                get;
                set;
        }
        public virtual CAEmitterCell[] Cells {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGColor Color {
                get;
                set;
        }
        public virtual MonoTouch.CoreGraphics.CGImage Contents {
                get;
                set;
        }
        public virtual System.Drawing.RectangleF ContentsRect {
                get;
                set;
        }
        public virtual float EmissionLatitude {
                get;
                set;
        }
        public virtual float EmissionLongitude {
                get;
                set;
        }
        public virtual float EmissionRange {
                get;
                set;
        }
        public virtual bool Enabled {
                get;
                set;
        }
        public virtual float GreenRange {
                get;
                set;
        }
        public virtual float GreenSpeed {
                get;
                set;
        }
        public virtual float LifeTime {
                get;
                set;
        }
        public virtual float LifetimeRange {
                get;
                set;
        }
        public virtual string MagnificationFilter {
                get;
                set;
        }
        public virtual string MinificationFilter {
                get;
                set;
        }
        public virtual float MinificationFilterBias {
                get;
                set;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual float RedRange {
                get;
                set;
        }
        public virtual float RedSpeed {
                get;
                set;
        }
        public virtual float Scale {
                get;
                set;
        }
        public virtual float ScaleRange {
                get;
                set;
        }
        public virtual float ScaleSpeed {
                get;
                set;
        }
        public virtual float Spin {
                get;
                set;
        }
        public virtual float SpinRange {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary Style {
                get;
                set;
        }
        public virtual float Velocity {
                get;
                set;
        }
        public virtual float VelocityRange {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakContents {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreAnimation.CAEmitterLayer" class="injected"></a>


## New Type: MonoTouch.CoreAnimation.CAEmitterLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CAEmitterLayer : CALayer {
        
        public CAEmitterLayer ();
        public CAEmitterLayer (MonoTouch.Foundation.NSCoder coder);
        public CAEmitterLayer (MonoTouch.Foundation.NSObjectFlag t);
        public CAEmitterLayer (IntPtr handle);
        
        public static CALayer Create ();
        protected override void Dispose (bool disposing);
        
        public static MonoTouch.Foundation.NSString ModeOutline {
                get;
        }
        public static MonoTouch.Foundation.NSString ModePoints {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeSurface {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeVolume {
                get;
        }
        public static MonoTouch.Foundation.NSString RenderAdditive {
                get;
        }
        public static MonoTouch.Foundation.NSString RenderBackToFront {
                get;
        }
        public static MonoTouch.Foundation.NSString RenderOldestFirst {
                get;
        }
        public static MonoTouch.Foundation.NSString RenderOldestLast {
                get;
        }
        public static MonoTouch.Foundation.NSString RenderUnordered {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapeCircle {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapeCuboid {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapeLine {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapePoint {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapeRectangle {
                get;
        }
        public static MonoTouch.Foundation.NSString ShapeSphere {
                get;
        }
        public virtual float BirthRate {
                get;
                set;
        }
        public virtual CAEmitterCell[] Cells {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float Depth {
                get;
                set;
        }
        public virtual float LifeTime {
                get;
                set;
        }
        public virtual string Mode {
                get;
                set;
        }
        public virtual System.Drawing.PointF Position {
                get;
                set;
        }
        public virtual bool PreservesDepth {
                get;
                set;
        }
        public virtual string RenderMode {
                get;
                set;
        }
        public virtual float Scale {
                get;
                set;
        }
        public virtual int Seed {
                get;
                set;
        }
        public virtual string Shape {
                get;
                set;
        }
        public virtual System.Drawing.SizeF Size {
                get;
                set;
        }
        public virtual float Spin {
                get;
                set;
        }
        public virtual float Velocity {
                get;
                set;
        }
        public virtual float ZPosition {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreBluetooth" class="injected"></a>


# Namespace: MonoTouch.CoreBluetooth

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBAdvertisement" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBAdvertisement

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBAdvertisement {
        
        public CBAdvertisement ();
        
        public static MonoTouch.Foundation.NSString DataLocalNameKey {
                get;
        }
        public static MonoTouch.Foundation.NSString DataManufacturerDataKey {
                get;
        }
        public static MonoTouch.Foundation.NSString DataServiceDataKey {
                get;
        }
        public static MonoTouch.Foundation.NSString DataServiceUUIDsKey {
                get;
        }
        public static MonoTouch.Foundation.NSString DataTxPowerLevelKey {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCentralManager" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCentralManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBCentralManager : MonoTouch.Foundation.NSObject {
        
        public CBCentralManager ();
        public CBCentralManager (MonoTouch.Foundation.NSCoder coder);
        public CBCentralManager (MonoTouch.Foundation.NSObjectFlag t);
        public CBCentralManager (IntPtr handle);
        public CBCentralManager (CBCentralManagerDelegate cbDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
        
        public virtual void CancelPeripheralConnection (CBPeripheral peripheral);
        public virtual void ConnectPeripheral (CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary options);
        protected override void Dispose (bool disposing);
        public virtual void RetrieveConnectedPeripherals ();
        public void RetrievePeripherals (Guid [] peripheralUuids);
        public void ScanForPeripherals (Guid [] serviceUuids, MonoTouch.Foundation.NSDictionary options);
        public virtual void StopScan ();
        
        public static MonoTouch.Foundation.NSString OptionNotifyOnDisconnectionKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ScanOptionAllowDuplicatesKey {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public CBCentralManagerDelegate Delegate {
                get;
                set;
        }
        public virtual CBCentralManagerState State {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCentralManagerDelegate" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCentralManagerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class CBCentralManagerDelegate : MonoTouch.Foundation.NSObject {
        
        public CBCentralManagerDelegate ();
        public CBCentralManagerDelegate (MonoTouch.Foundation.NSCoder coder);
        public CBCentralManagerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public CBCentralManagerDelegate (IntPtr handle);
        
        public abstract void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);
        public abstract void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public abstract void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
        public abstract void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public abstract void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
        public abstract void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
        public abstract void UpdatedState (CBCentralManager central);
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCentralManagerState" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCentralManagerState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum CBCentralManagerState {
        Unknown,
        Resetting,
        Unsupported,
        Unauthorized,
        PoweredOff,
        PoweredOn
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCharacteristic" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCharacteristic

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBCharacteristic : MonoTouch.Foundation.NSObject {
        
        public CBCharacteristic ();
        public CBCharacteristic (MonoTouch.Foundation.NSCoder coder);
        public CBCharacteristic (MonoTouch.Foundation.NSObjectFlag t);
        public CBCharacteristic (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CBDescriptor[] Descriptors {
                get;
        }
        public virtual bool IsBroadcasted {
                get;
        }
        public virtual bool IsNotifying {
                get;
        }
        public virtual CBCharacteristicProperties Properties {
                get;
        }
        public virtual CBService Service {
                get;
        }
        public virtual CBUUID UUID {
                get;
        }
        public virtual MonoTouch.Foundation.NSData Value {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCharacteristicProperties" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCharacteristicProperties

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum CBCharacteristicProperties {
        Broadcast,
        Read,
        WriteWithoutResponse,
        Write,
        Notify,
        Indicate,
        AuthenticatedSignedWrites,
        ExtendedProperties
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCharacteristicWriteType" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCharacteristicWriteType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum CBCharacteristicWriteType {
        WithResponse,
        WithoutResponse
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBDescriptor" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBDescriptor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBDescriptor : MonoTouch.Foundation.NSObject {
        
        public CBDescriptor ();
        public CBDescriptor (MonoTouch.Foundation.NSCoder coder);
        public CBDescriptor (MonoTouch.Foundation.NSObjectFlag t);
        public CBDescriptor (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual CBCharacteristic Characteristic {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CBUUID UUID {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject Value {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBError" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum CBError {
        None,
        InvalidHandle,
        ReadNotPermitted,
        WriteNotPermitted,
        InvalidPdu,
        InsufficientAuthentication,
        RequestNotSupported,
        InvalidOffset,
        InsufficientAuthorization,
        PrepareQueueFull,
        AttributeNotFound,
        AttributeNotLong,
        InsufficientEncryptionKeySize,
        InvalidAttributeValueLength,
        UnlikelyError,
        InsufficientEncryption,
        UnsupportedGroupType,
        InsufficientResources
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheral" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheral

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBPeripheral : MonoTouch.Foundation.NSObject {
        
        public CBPeripheral ();
        public CBPeripheral (MonoTouch.Foundation.NSCoder coder);
        public CBPeripheral (MonoTouch.Foundation.NSObjectFlag t);
        public CBPeripheral (IntPtr handle);
        
        public void DiscoverCharacteristics (Guid [] charactersticUUIDs, CBService forService);
        public virtual void DiscoverDescriptors (CBCharacteristic characteristic);
        public void DiscoverIncludedServices (Guid [] includedServiceUUIDs, CBService forService);
        public void DiscoverServices (Guid [] services);
        protected override void Dispose (bool disposing);
        public virtual void ReadRSSI ();
        public virtual void ReadValue (CBCharacteristic characteristic);
        public virtual void ReadValue (CBDescriptor descriptor);
        public virtual void SetNotifyValue (bool notifyValue, CBCharacteristic characteristic);
        public virtual void WriteValue (MonoTouch.Foundation.NSData data, CBCharacteristic characteristic, CBCharacteristicWriteType type);
        public virtual void WriteValue (MonoTouch.Foundation.NSData data, CBDescriptor descriptor);
        
        public override IntPtr ClassHandle {
                get;
        }
        public CBPeripheralDelegate Delegate {
                get;
                set;
        }
        public virtual bool IsConnected {
                get;
        }
        public virtual string Name {
                get;
        }
        public virtual MonoTouch.Foundation.NSNumber RSSI {
                get;
        }
        public virtual CBService[] Services {
                get;
        }
        public virtual IntPtr UUID {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralDelegate" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBPeripheralDelegate : MonoTouch.Foundation.NSObject {
        
        public CBPeripheralDelegate ();
        public CBPeripheralDelegate (MonoTouch.Foundation.NSCoder coder);
        public CBPeripheralDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public CBPeripheralDelegate (IntPtr handle);
        
        public virtual void DiscoverCharacteristic (CBPeripheral peripheral, CBService service, MonoTouch.Foundation.NSError error);
        public virtual void DiscoveredDescriptor (CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
        public virtual void DiscoveredIncludedService (CBPeripheral peripheral, CBService service, MonoTouch.Foundation.NSError error);
        public virtual void DiscoveredService (CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public virtual void RssiUpdated (CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public virtual void UpdatedCharacterteristicValue (CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
        public virtual void UpdatedNotificationState (CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
        public virtual void UpdatedValue (CBPeripheral peripheral, CBDescriptor descriptor, MonoTouch.Foundation.NSError error);
        public virtual void WroteCharacteristicValue (CBPeripheral peripheral, CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
        public virtual void WroteDescriptorValue (CBPeripheral peripheral, CBDescriptor descriptor, MonoTouch.Foundation.NSError error);
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBService" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBService

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBService : MonoTouch.Foundation.NSObject {
        
        public CBService ();
        public CBService (MonoTouch.Foundation.NSCoder coder);
        public CBService (MonoTouch.Foundation.NSObjectFlag t);
        public CBService (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual CBCharacteristic[] Characteristics {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CBService[] IncludedServices {
                get;
        }
        public virtual CBPeripheral Peripheral {
                get;
        }
        public virtual CBUUID UUID {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBUUID" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBUUID

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CBUUID : MonoTouch.Foundation.NSObject {
        
        public CBUUID ();
        public CBUUID (MonoTouch.Foundation.NSCoder coder);
        public CBUUID (MonoTouch.Foundation.NSObjectFlag t);
        public CBUUID (IntPtr handle);
        
        public static CBUUID FromCFUUID (IntPtr theUUID);
        public static CBUUID FromData (MonoTouch.Foundation.NSData theData);
        public static CBUUID FromString (string theString);
        protected override void Dispose (bool disposing);
        
        public static MonoTouch.Foundation.NSString AppearanceString {
                get;
        }
        public static MonoTouch.Foundation.NSString CharacteristicAggregateFormatString {
                get;
        }
        public static MonoTouch.Foundation.NSString CharacteristicExtendedPropertiesString {
                get;
        }
        public static MonoTouch.Foundation.NSString CharacteristicFormatString {
                get;
        }
        public static MonoTouch.Foundation.NSString CharacteristicUserDescriptionString {
                get;
        }
        public static MonoTouch.Foundation.NSString ClientCharacteristicConfigurationString {
                get;
        }
        public static MonoTouch.Foundation.NSString DeviceNameString {
                get;
        }
        public static MonoTouch.Foundation.NSString GenericAccessProfileString {
                get;
        }
        public static MonoTouch.Foundation.NSString GenericAttributeProfileString {
                get;
        }
        public static MonoTouch.Foundation.NSString PeripheralPreferredConnectionParametersString {
                get;
        }
        public static MonoTouch.Foundation.NSString PeripheralPrivacyFlagString {
                get;
        }
        public static MonoTouch.Foundation.NSString ReconnectionAddressString {
                get;
        }
        public static MonoTouch.Foundation.NSString ServerCharacteristicConfigurationString {
                get;
        }
        public static MonoTouch.Foundation.NSString ServiceChangedString {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSData Data {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.CoreData.NSAttributeDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSAttributeDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool AllowsExternalBinaryDataStorage {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSEntityDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSEntityDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual NSPropertyDescription[] CompoundIndexes {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSFetchRequest" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSFetchRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class NSFetchRequest : NSPersistentStoreRequest {
        public NSFetchRequest (string entityName);
        public static NSFetchRequest FromEntityName (string entityName);
        public virtual string EntityName {
                get;
        }
        public virtual int FetchBatchSize {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSPredicate HavingPredicate {
                get;
                set;
        }
        public virtual NSPropertyDescription[] PropertiesToGroupBy {
                get;
                set;
        }
        public virtual bool ShouldRefreshRefetchedObjects {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSFetchRequestResultType" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSFetchRequestResultType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Flags]
        DictionaryResultType,
        NSCountResultType
```

 <a name="New_Type:_MonoTouch.CoreData.NSIncrementalStore" class="injected"></a>


## New Type: MonoTouch.CoreData.NSIncrementalStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSIncrementalStore : NSPersistentStore {
        
        public NSIncrementalStore ();
        public NSIncrementalStore (MonoTouch.Foundation.NSCoder coder);
        public NSIncrementalStore (MonoTouch.Foundation.NSObjectFlag t);
        public NSIncrementalStore (IntPtr handle);
        
        public static MonoTouch.Foundation.NSObject IdentifierForNewStoreAtURL (MonoTouch.Foundation.NSUrl storeURL);
        public virtual MonoTouch.Foundation.NSObject ExecuteRequest (NSPersistentStoreRequest request, NSManagedObjectContext context, out MonoTouch.Foundation.NSError error);
        public virtual bool LoadMetadata (out MonoTouch.Foundation.NSError error);
        public virtual void ManagedObjectContextDidRegisterObjectsWithIds (MonoTouch.Foundation.NSObject[] objectIds);
        public virtual void ManagedObjectContextDidUnregisterObjectsWithIds (MonoTouch.Foundation.NSObject[] objectIds);
        public virtual NSManagedObjectID NewObjectIdFor (NSEntityDescription forEntity, MonoTouch.Foundation.NSObject referenceObject);
        public virtual MonoTouch.Foundation.NSObject NewValue (NSRelationshipDescription forRelationship, NSManagedObjectID forObjectI, NSManagedObjectContext context, out MonoTouch.Foundation.NSError error);
        public virtual NSIncrementalStoreNode NewValues (NSManagedObjectID forObjectId, NSManagedObjectContext context, out MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.Foundation.NSObject[] ObtainPermanentIds (MonoTouch.Foundation.NSObject[] array, out MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.Foundation.NSObject ReferenceObjectForObject (NSManagedObjectID objectId);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSIncrementalStoreNode" class="injected"></a>


## New Type: MonoTouch.CoreData.NSIncrementalStoreNode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSIncrementalStoreNode : MonoTouch.Foundation.NSObject {
        
        public NSIncrementalStoreNode ();
        public NSIncrementalStoreNode (MonoTouch.Foundation.NSCoder coder);
        public NSIncrementalStoreNode (MonoTouch.Foundation.NSObjectFlag t);
        public NSIncrementalStoreNode (IntPtr handle);
        public NSIncrementalStoreNode (NSManagedObjectID objectId, MonoTouch.Foundation.NSDictionary values, ulong version);
        
        protected override void Dispose (bool disposing);
        public virtual void Update (MonoTouch.Foundation.NSDictionary values, ulong version);
        public virtual MonoTouch.Foundation.NSObject ValueForPropertyDescription (NSPropertyDescription prop);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSManagedObjectID ObjectId {
                get;
        }
        public virtual long Version {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObject" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual MonoTouch.Foundation.NSDictionary ChangedValuesForCurrentEvent {
                get;
        }
        public virtual bool HasChanges {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObjectContext" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObjectContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public NSManagedObjectContext (NSManagedObjectContextConcurrencyType ct);
        public virtual void Perform (MonoTouch.Foundation.NSAction action);
        public virtual void PerformAndWait (MonoTouch.Foundation.NSAction action);
        public virtual NSManagedObjectContextConcurrencyType ConcurrencyType {
                get;
        }
        public virtual NSManagedObjectContext ParentContext {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSMutableDictionary UserInfo {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObjectContextConcurrencyType" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObjectContextConcurrencyType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum NSManagedObjectContextConcurrencyType {
        Confinement,
        PrivateQueue,
        MainQueue
 }
```

 <a name="New_Type:_MonoTouch.CoreData.NSMergeConflict" class="injected"></a>


## New Type: MonoTouch.CoreData.NSMergeConflict

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMergeConflict : MonoTouch.Foundation.NSObject {
        
        public NSMergeConflict ();
        public NSMergeConflict (MonoTouch.Foundation.NSCoder coder);
        public NSMergeConflict (MonoTouch.Foundation.NSObjectFlag t);
        public NSMergeConflict (IntPtr handle);
        public NSMergeConflict (NSManagedObject srcObject, uint newvers, uint oldvers, MonoTouch.Foundation.NSDictionary cachesnap, MonoTouch.Foundation.NSDictionary persnap);
        
        protected override void Dispose (bool disposing);
        
        public virtual MonoTouch.Foundation.NSDictionary CachedSnapshot {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual uint NewVersionNumber {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary ObjectSnapshot {
                get;
        }
        public virtual uint OldVersionNumber {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary PersistedSnapshot {
                get;
        }
        public virtual NSManagedObject SourceObject {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSMergePolicy" class="injected"></a>


## New Type: MonoTouch.CoreData.NSMergePolicy

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMergePolicy : MonoTouch.Foundation.NSObject {
        
        public NSMergePolicy ();
        public NSMergePolicy (MonoTouch.Foundation.NSCoder coder);
        public NSMergePolicy (MonoTouch.Foundation.NSObjectFlag t);
        public NSMergePolicy (IntPtr handle);
        public NSMergePolicy (NSMergePolicyType ty);
        
        public virtual bool ResolveConflictserror (NSMergeConflict[] list, out MonoTouch.Foundation.NSError error);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSMergePolicyType MergeType {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSMergePolicyType" class="injected"></a>


## New Type: MonoTouch.CoreData.NSMergePolicyType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum NSMergePolicyType {
        Error,
        PropertyStoreTrump,
        PropertyObjectTrump,
        Overwrite,
        RollbackMerge
}
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSMigrationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSMigrationManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool UsesStoreSpecificMigrationManager {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStore" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString SaveConflictsErrorKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreCoordinator" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The removals are source code compatible and encourage the use of NSStrings as
keys, instead of strings since the underlying API treats the values as keys that
happen to be stored as NSStrings.

Removed:

```
public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreOfType (string storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static void RegisterStoreClass (MonoTouch.ObjCRuntime.Class storeClass, string storeType);
        public static bool SetMetadata (MonoTouch.Foundation.NSDictionary metadata, string storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore AddPersistentStoreWithType (string storeType, string configuration, MonoTouch.Foundation.NSUrl storeURL, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore MigratePersistentStore (NSPersistentStore store, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options, string storeType, out MonoTouch.Foundation.NSError error);
```

Added:

```
public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreOfType (MonoTouch.Foundation.NSString storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static void RegisterStoreClass (MonoTouch.ObjCRuntime.Class storeClass, MonoTouch.Foundation.NSString storeType);
        public static bool SetMetadata (MonoTouch.Foundation.NSDictionary metadata, MonoTouch.Foundation.NSString storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore AddPersistentStoreWithType (MonoTouch.Foundation.NSString storeType, string configuration, MonoTouch.Foundation.NSUrl storeURL, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.Foundation.NSObject ExecuteRequestwithContexterror (NSPersistentStoreRequest request, NSManagedObjectContext context, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore MigratePersistentStore (NSPersistentStore store, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options, MonoTouch.Foundation.NSString storeType, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSString BinaryStoreType {
                get;
        }
        public static MonoTouch.Foundation.NSString DidImportUbiquitousContentChangesNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString InMemoryStoreType {
                get;
        }
        public static MonoTouch.Foundation.NSString SQLiteStoreType {
                get;
        }
        public static MonoTouch.Foundation.NSString StoresDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString StoreTypeKey {
                get;
        }
        public static MonoTouch.Foundation.NSString WillRemoveStoreNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString XMLStoreType {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreRequest" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class NSPersistentStoreRequest : MonoTouch.Foundation.NSObject {
        
        public NSPersistentStoreRequest ();
        public NSPersistentStoreRequest (MonoTouch.Foundation.NSCoder coder);
        public NSPersistentStoreRequest (MonoTouch.Foundation.NSObjectFlag t);
        public NSPersistentStoreRequest (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual NSPersistentStore[] AffectedStores {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSPersistentStoreRequestType RequestType {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreRequestType" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreRequestType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum NSPersistentStoreRequestType {
        Fetch,
        Save
 }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPropertyDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPropertyDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool IndexedBySpotlight {
                get;
                set;
        }
        public virtual bool StoredInExternalRecord {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSRelationshipDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSRelationshipDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool Ordered {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.CoreData.NSSaveChangesRequest" class="injected"></a>


## New Type: MonoTouch.CoreData.NSSaveChangesRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSSaveChangesRequest : NSPersistentStoreRequest {
        
        public NSSaveChangesRequest ();
        public NSSaveChangesRequest (MonoTouch.Foundation.NSCoder coder);
        public NSSaveChangesRequest (MonoTouch.Foundation.NSObjectFlag t);
        public NSSaveChangesRequest (IntPtr handle);
        public NSSaveChangesRequest (MonoTouch.Foundation.NSSet insertedObjects, MonoTouch.Foundation.NSSet updatedObjects, MonoTouch.Foundation.NSSet deletedObjects, MonoTouch.Foundation.NSSet lockedObjects);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet DeletedObjects {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet InsertedObjects {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet LockedObjects {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet UpdatedObjects {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGContextPDF" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGContextPDF

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public CGContextPDF (MonoTouch.Foundation.NSUrl url, CGPDFInfo info);
        public CGContextPDF (MonoTouch.Foundation.NSUrl url);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public CGPath (CGPath reference, CGAffineTransform transform);
        public static CGPath EllipseFromRect (System.Drawing.RectangleF boundingRect, CGAffineTransform transform);
        public static CGPath FromRect (System.Drawing.RectangleF rectangle);
        public static CGPath FromRect (System.Drawing.RectangleF rectangle, CGAffineTransform transform);
        public void AddRelativeArc (CGAffineTransform m, float x, float y, float radius, float startAngle, float delta);
        public void AddRelativeArc (float x, float y, float radius, float startAngle, float delta);
        public CGPath CopyByDashingPath (CGAffineTransform transform, float [] phase);
        public CGPath CopyByDashingPath (float [] phase);
        public CGPath CopyByStrokingPath (CGAffineTransform transform, float lineWidth, CGLineCap lineCap, CGLineJoin lineJoin, float miterLimit);
        public CGPath CopyByStrokingPath (float lineWidth, CGLineCap lineCap, CGLineJoin lineJoin, float miterLimit);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFArray" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFArray

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public bool GetDictionary (int idx, out CGPDFArray result);
```

Added:

```
public bool GetDictionary (int idx, out CGPDFDictionary result);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDictionary" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public void Apply (Action<string,object> callback);
        public bool GetString (string key, out string result);
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.CoreImage.CIAdditionCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAdditionCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIAdditionCompositing : CIFilter {
        
        public CIAdditionCompositing ();
        public CIAdditionCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIAffineTransform" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAffineTransform

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIAffineTransform : CIFilter {
        
        public CIAffineTransform ();
        public CIAffineTransform (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public MonoTouch.CoreGraphics.CGAffineTransform Transform {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIAutoAdjustmentFilterOptions" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIAutoAdjustmentFilterOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIAutoAdjustmentFilterOptions {
        
        public CIAutoAdjustmentFilterOptions ();
        
        public Nullable<bool> Enhance;
        public Nullable<bool> RedEye;
        public CIFeature[] Features;
        public Nullable<ciimageorientation> ImageOrientation;
}
</ciimageorientation></bool></bool>
```

 <a name="New_Type:_MonoTouch.CoreImage.CICheckerboardGenerator" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICheckerboardGenerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CICheckerboardGenerator : CIFilter {
        
        public CICheckerboardGenerator ();
        public CICheckerboardGenerator (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public float Sharpness {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColor" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColor : MonoTouch.Foundation.NSObject {
        
        public CIColor ();
        public CIColor (MonoTouch.Foundation.NSCoder coder);
        public CIColor (MonoTouch.Foundation.NSObjectFlag t);
        public CIColor (IntPtr handle);
        public CIColor (MonoTouch.CoreGraphics.CGColor c);
        public CIColor (MonoTouch.UIKit.UIColor color);
        
        public static CIColor FromCGColor (MonoTouch.CoreGraphics.CGColor c);
        public static CIColor FromRgb (float r, float g, float b);
        public static CIColor FromRgba (float r, float g, float b, float a);
        public static CIColor FromString (string representation);
        public virtual string StringRepresentation ();
        
        public virtual float Alpha {
                get;
        }
        public virtual float Blue {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                get;
        }
        public virtual float Green {
                get;
        }
        public virtual int NumberOfComponents {
                get;
        }
        public virtual float Red {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorBlendMode : CIFilter {
        
        public CIColorBlendMode ();
        public CIColorBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorBurnBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorBurnBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorBurnBlendMode : CIFilter {
        
        public CIColorBurnBlendMode ();
        public CIColorBurnBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorControls" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorControls

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorControls : CIFilter {
        
        public CIColorControls ();
        public CIColorControls (IntPtr handle);
        
        public float Brightness {
                get;
                set;
        }
        public float Contrast {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Saturation {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorCube" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorCube

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorCube : CIFilter {
        
        public CIColorCube ();
        public CIColorCube (IntPtr handle);
        
        public MonoTouch.Foundation.NSData CubeData {
                get;
                set;
        }
        public float CubeDimension {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorDodgeBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorDodgeBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorDodgeBlendMode : CIFilter {
        
        public CIColorDodgeBlendMode ();
        public CIColorDodgeBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorInvert" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorInvert

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorInvert : CIFilter {
        
        public CIColorInvert ();
        public CIColorInvert (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorMatrix" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorMatrix

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorMatrix : CIFilter {
        
        public CIColorMatrix ();
        public CIColorMatrix (IntPtr handle);
        
        public CIVector AVector {
                get;
                set;
        }
        public CIVector BiasVector {
                get;
                set;
        }
        public CIVector BVector {
                get;
                set;
        }
        public CIVector GVector {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public CIVector RVector {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIColorMonochrome" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIColorMonochrome

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIColorMonochrome : CIFilter {
        
        public CIColorMonochrome ();
        public CIColorMonochrome (IntPtr handle);
        
        public CIColor Color {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIConstantColorGenerator" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIConstantColorGenerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIConstantColorGenerator : CIFilter {
        
        public CIConstantColorGenerator ();
        public CIConstantColorGenerator (IntPtr handle);
        
        public CIColor Color {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIContext" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIContext : MonoTouch.Foundation.NSObject {
        
        public CIContext ();
        public CIContext (MonoTouch.Foundation.NSCoder coder);
        public CIContext (MonoTouch.Foundation.NSObjectFlag t);
        public CIContext (IntPtr handle);
        
        public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx);
        public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx, CIContextOptions options);
        public static CIContext FromContext (MonoTouch.OpenGLES.EAGLContext eaglContext);
        public static CIContext FromOptions (CIContextOptions options);
        public virtual MonoTouch.CoreGraphics.CGImage CreateCGImage (CIImage image, System.Drawing.RectangleF fromRectangle);
        public virtual MonoTouch.CoreGraphics.CGImage CreateCGImage (CIImage image, System.Drawing.RectangleF fromRect, int ciImageFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        public MonoTouch.CoreGraphics.CGLayer CreateCGLayer (System.Drawing.SizeF size);
        public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
        public virtual void DrawImage (CIImage image, System.Drawing.RectangleF inRectangle, System.Drawing.RectangleF fromRectangle);
        public virtual void Render (CIImage image, MonoTouch.CoreVideo.CVPixelBuffer buffer);
        public virtual void Render (CIImage image, MonoTouch.CoreVideo.CVPixelBuffer buffer, System.Drawing.RectangleF rectangle, MonoTouch.CoreGraphics.CGColorSpace cs);
        public virtual void RenderToBitmap (CIImage image, IntPtr bitmapPtr, int bytesPerRow, System.Drawing.RectangleF bounds, int bitmapFormat, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Drawing.SizeF InputImageMaximumSize {
                get;
        }
        public virtual System.Drawing.SizeF OutputImageMaximumSize {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIContextOptions" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIContextOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIContextOptions {
        
        public CIContextOptions ();
        
        public MonoTouch.CoreGraphics.CGColorSpace OutputColorSpace {
                get;
                set;
        }
        public bool UseSoftwareRenderer {
                get;
                set;
        }
        public MonoTouch.CoreGraphics.CGColorSpace WorkingColorSpace {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CICrop" class="injected"></a>


## New Type: MonoTouch.CoreImage.CICrop

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CICrop : CIFilter {
        
        public CICrop ();
        public CICrop (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public CIVector Rectangle {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDarkenBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDarkenBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIDarkenBlendMode : CIFilter {
        
        public CIDarkenBlendMode ();
        public CIDarkenBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDetector" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDetector

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIDetector : MonoTouch.Foundation.NSObject {
        
        public CIDetector ();
        public CIDetector (MonoTouch.Foundation.NSCoder coder);
        public CIDetector (MonoTouch.Foundation.NSObjectFlag t);
        public CIDetector (IntPtr handle);
        
        public static CIDetector CreateFaceDetector (CIContext context, bool highAccuracy);
        public virtual CIFeature[] FeaturesInImage (CIImage image);
        public CIFeature[] FeaturesInImage (CIImage image, CIImageOrientation orientation);
        public virtual CIFeature[] FeaturesInImage (CIImage image, MonoTouch.Foundation.NSDictionary options);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIDifferenceBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIDifferenceBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIDifferenceBlendMode : CIFilter {
        
        public CIDifferenceBlendMode ();
        public CIDifferenceBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIExclusionBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIExclusionBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIExclusionBlendMode : CIFilter {
        
        public CIExclusionBlendMode ();
        public CIExclusionBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIExposureAdjust" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIExposureAdjust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIExposureAdjust : CIFilter {
        
        public CIExposureAdjust ();
        public CIExposureAdjust (IntPtr handle);
        
        public float EV {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFaceBalance" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFaceBalance

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIFaceBalance : CIFilter {
        
        public CIFaceBalance (IntPtr handle);
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFaceFeature" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFaceFeature

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIFaceFeature : CIFeature {
        
        public CIFaceFeature ();
        public CIFaceFeature (MonoTouch.Foundation.NSCoder coder);
        public CIFaceFeature (MonoTouch.Foundation.NSObjectFlag t);
        public CIFaceFeature (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool HasLeftEyePosition {
                get;
        }
        public virtual bool HasMouthPosition {
                get;
        }
        public virtual bool HasRightEyePosition {
                get;
        }
        public virtual System.Drawing.PointF LeftEyePosition {
                get;
        }
        public virtual System.Drawing.PointF MouthPosition {
                get;
        }
        public virtual System.Drawing.PointF RightEyePosition {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFalseColor" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFalseColor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIFalseColor : CIFilter {
        
        public CIFalseColor ();
        public CIFalseColor (IntPtr handle);
        
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFeature" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFeature

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIFeature : MonoTouch.Foundation.NSObject {
        
        public CIFeature ();
        public CIFeature (MonoTouch.Foundation.NSCoder coder);
        public CIFeature (MonoTouch.Foundation.NSObjectFlag t);
        public CIFeature (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual System.Drawing.RectangleF Bounds {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSString Type {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFilter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIFilter : MonoTouch.Foundation.NSObject {
        
        public CIFilter ();
        public CIFilter (MonoTouch.Foundation.NSCoder coder);
        public CIFilter (MonoTouch.Foundation.NSObjectFlag t);
        public CIFilter (IntPtr handle);
        
        public static string [] FilterNamesInCategories (params string [] categories);
        public static string [] FilterNamesInCategory (string category);
        public static CIFilter FromName (string name);
        protected override void Dispose (bool disposing);
        public virtual void SetDefaults ();
        
        public virtual MonoTouch.Foundation.NSDictionary Attributes {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string [] InputKeys {
                get;
        }
        public MonoTouch.Foundation.NSObject this [MonoTouch.Foundation.NSString key] {
                get;
                set;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual CIImage OutputImage {
                get;
        }
        public virtual string [] OutputKeys {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFilterAttributes" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFilterAttributes

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public static class CIFilterAttributes {
        
        public static MonoTouch.Foundation.NSString Class {
                get;
        }
        public static MonoTouch.Foundation.NSString Default {
                get;
        }
        public static MonoTouch.Foundation.NSString DisplayName {
                get;
        }
        public static MonoTouch.Foundation.NSString FilterCategories {
                get;
        }
        public static MonoTouch.Foundation.NSString FilterDisplayName {
                get;
        }
        public static MonoTouch.Foundation.NSString FilterName {
                get;
        }
        public static MonoTouch.Foundation.NSString Identity {
                get;
        }
        public static MonoTouch.Foundation.NSString Max {
                get;
        }
        public static MonoTouch.Foundation.NSString Min {
                get;
        }
        public static MonoTouch.Foundation.NSString Name {
                get;
        }
        public static MonoTouch.Foundation.NSString SliderMax {
                get;
        }
        public static MonoTouch.Foundation.NSString SliderMin {
                get;
        }
        public static MonoTouch.Foundation.NSString Type {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeAngle {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeBoolean {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeCount {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeImage {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeInteger {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeOffset {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeOpaqueColor {
                get;
        }
        public static MonoTouch.Foundation.NSString TypePosition {
                get;
        }
        public static MonoTouch.Foundation.NSString TypePosition3 {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeRectangle {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeScalar {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeTime {
                get;
        }
        public static MonoTouch.Foundation.NSString TypeTransform {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFilterCategory" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFilterCategory

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public static class CIFilterCategory {
        
        public static MonoTouch.Foundation.NSString Blur {
                get;
        }
        public static MonoTouch.Foundation.NSString BuiltIn {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorAdjustment {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorEffect {
                get;
        }
        public static MonoTouch.Foundation.NSString CompositeOperation {
                get;
        }
        public static MonoTouch.Foundation.NSString DistortionEffect {
                get;
        }
        public static MonoTouch.Foundation.NSString Generator {
                get;
        }
        public static MonoTouch.Foundation.NSString GeometryAdjustment {
                get;
        }
        public static MonoTouch.Foundation.NSString Gradient {
                get;
        }
        public static MonoTouch.Foundation.NSString HalftoneEffect {
                get;
        }
        public static MonoTouch.Foundation.NSString HighDynamicRange {
                get;
        }
        public static MonoTouch.Foundation.NSString Interlaced {
                get;
        }
        public static MonoTouch.Foundation.NSString NonSquarePixels {
                get;
        }
        public static MonoTouch.Foundation.NSString Reduction {
                get;
        }
        public static MonoTouch.Foundation.NSString Sharpen {
                get;
        }
        public static MonoTouch.Foundation.NSString StillImage {
                get;
        }
        public static MonoTouch.Foundation.NSString Stylize {
                get;
        }
        public static MonoTouch.Foundation.NSString TileEffect {
                get;
        }
        public static MonoTouch.Foundation.NSString Transition {
                get;
        }
        public static MonoTouch.Foundation.NSString Video {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFilterInputKey" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFilterInputKey

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public static class CIFilterInputKey {
        
        public static MonoTouch.Foundation.NSString BackgroundImage {
                get;
        }
        public static MonoTouch.Foundation.NSString Image {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIFilterOutputKey" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIFilterOutputKey

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public static class CIFilterOutputKey {
        
        public static MonoTouch.Foundation.NSString Image {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIGammaAdjust" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIGammaAdjust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIGammaAdjust : CIFilter {
        
        public CIGammaAdjust ();
        public CIGammaAdjust (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Power {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIGaussianGradient" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIGaussianGradient

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIGaussianGradient : CIFilter {
        
        public CIGaussianGradient ();
        public CIGaussianGradient (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHardLightBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHardLightBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIHardLightBlendMode : CIFilter {
        
        public CIHardLightBlendMode ();
        public CIHardLightBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHighlightShadowAdjust" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHighlightShadowAdjust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIHighlightShadowAdjust : CIFilter {
        
        public CIHighlightShadowAdjust ();
        public CIHighlightShadowAdjust (IntPtr handle);
        
        public float HighlightAmount {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
        public float ShadowAmount {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHueAdjust" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHueAdjust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIHueAdjust : CIFilter {
        
        public CIHueAdjust ();
        public CIHueAdjust (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIHueBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIHueBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIHueBlendMode : CIFilter {
        
        public CIHueBlendMode ();
        public CIHueBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIImage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIImage : MonoTouch.Foundation.NSObject {
        
        public CIImage ();
        public CIImage (MonoTouch.Foundation.NSCoder coder);
        public CIImage (MonoTouch.Foundation.NSObjectFlag t);
        public CIImage (IntPtr handle);
        public CIImage (MonoTouch.CoreGraphics.CGImage image);
        public CIImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreGraphics.CGLayer layer);
        public CIImage (MonoTouch.Foundation.NSData data);
        public CIImage (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace c);
        public CIImage (int glTextureName, System.Drawing.SizeF size, bool flag, MonoTouch.CoreGraphics.CGColorSpace cs);
        public CIImage (MonoTouch.Foundation.NSUrl url);
        public CIImage (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
        public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer);
        public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);
        public CIImage (CIColor color);
        public CIImage (MonoTouch.UIKit.UIImage image);
        public CIImage (MonoTouch.UIKit.UIImage image, MonoTouch.Foundation.NSDictionary options);
        
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image);
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromData (MonoTouch.Foundation.NSData data);
        public static CIImage FromData (MonoTouch.Foundation.NSData bitmapData, int bpr, System.Drawing.SizeF size, int ciImageFormat, MonoTouch.CoreGraphics.CGColorSpace colorspace);
        public static CIImage FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer);
        public static CIImage FromImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);
        public static CIImage FromUrl (MonoTouch.Foundation.NSUrl url);
        public static CIImage FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary d);
        protected override void Dispose (bool disposing);
        public CIFilter[] GetAutoAdjustmentFilters ();
        public CIFilter[] GetAutoAdjustmentFilters (CIAutoAdjustmentFilterOptions options);
        public virtual CIImage ImageByApplyingTransform (MonoTouch.CoreGraphics.CGAffineTransform matrix);
        public virtual CIImage ImageByCroppingToRect (System.Drawing.RectangleF r);
        public virtual CIImage ImageWithColor (CIColor color);
        public virtual MonoTouch.Foundation.NSObject IntPtr (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        
        public static CIImage EmptyImage {
                get;
        }
        public static int FormatBGRA8 {
                get;
        }
        public static int FormatRGBA8 {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                get;
        }
        public virtual System.Drawing.RectangleF Extent {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIImageOrientation" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIImageOrientation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum CIImageOrientation {
        TopLeft,
        TopRight,
        BottomRight,
        BottomLeft,
        LeftTop,
        RightTop,
        RightBottom,
        LeftBottom
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CILightenBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILightenBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CILightenBlendMode : CIFilter {
        
        public CILightenBlendMode ();
        public CILightenBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CILinearGradient" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILinearGradient

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CILinearGradient : CIFilter {
        
        public CILinearGradient ();
        public CILinearGradient (IntPtr handle);
        
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public CIVector Point0 {
                get;
                set;
        }
        public CIVector Point1 {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CILuminosityBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CILuminosityBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CILuminosityBlendMode : CIFilter {
        
        public CILuminosityBlendMode ();
        public CILuminosityBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMaximumCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMaximumCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIMaximumCompositing : CIFilter {
        
        public CIMaximumCompositing ();
        public CIMaximumCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMinimumCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMinimumCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIMinimumCompositing : CIFilter {
        
        public CIMinimumCompositing ();
        public CIMinimumCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMultiplyBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMultiplyBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIMultiplyBlendMode : CIFilter {
        
        public CIMultiplyBlendMode ();
        public CIMultiplyBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIMultiplyCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIMultiplyCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIMultiplyCompositing : CIFilter {
        
        public CIMultiplyCompositing ();
        public CIMultiplyCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIOverlayBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIOverlayBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIOverlayBlendMode : CIFilter {
        
        public CIOverlayBlendMode ();
        public CIOverlayBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIRadialGradient" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIRadialGradient

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIRadialGradient : CIFilter {
        
        public CIRadialGradient ();
        public CIRadialGradient (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public float Radius0 {
                get;
                set;
        }
        public float Radius1 {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISaturationBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISaturationBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISaturationBlendMode : CIFilter {
        
        public CISaturationBlendMode ();
        public CISaturationBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIScreenBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIScreenBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIScreenBlendMode : CIFilter {
        
        public CIScreenBlendMode ();
        public CIScreenBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISepiaTone" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISepiaTone

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISepiaTone : CIFilter {
        
        public CISepiaTone ();
        public CISepiaTone (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISoftLightBlendMode" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISoftLightBlendMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISoftLightBlendMode : CIFilter {
        
        public CISoftLightBlendMode ();
        public CISoftLightBlendMode (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISourceAtopCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISourceAtopCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISourceAtopCompositing : CIFilter {
        
        public CISourceAtopCompositing ();
        public CISourceAtopCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISourceInCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISourceInCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISourceInCompositing : CIFilter {
        
        public CISourceInCompositing ();
        public CISourceInCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISourceOutCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISourceOutCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISourceOutCompositing : CIFilter {
        
        public CISourceOutCompositing ();
        public CISourceOutCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CISourceOverCompositing" class="injected"></a>


## New Type: MonoTouch.CoreImage.CISourceOverCompositing

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CISourceOverCompositing : CIFilter {
        
        public CISourceOverCompositing ();
        public CISourceOverCompositing (IntPtr handle);
        
        public CIImage BackgroundImage {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIStraightenFilter" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIStraightenFilter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIStraightenFilter : CIFilter {
        
        public CIStraightenFilter ();
        public CIStraightenFilter (IntPtr handle);
        
        public float Angle {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIStripesGenerator" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIStripesGenerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIStripesGenerator : CIFilter {
        
        public CIStripesGenerator ();
        public CIStripesGenerator (IntPtr handle);
        
        public CIVector Center {
                get;
                set;
        }
        public CIColor Color0 {
                get;
                set;
        }
        public CIColor Color1 {
                get;
                set;
        }
        public float Sharpness {
                get;
                set;
        }
        public float Width {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CITemperatureAndTint" class="injected"></a>


## New Type: MonoTouch.CoreImage.CITemperatureAndTint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CITemperatureAndTint : CIFilter {
        
        public CITemperatureAndTint ();
        public CITemperatureAndTint (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public CIVector Neutral {
                get;
                set;
        }
        public CIVector TargetNeutral {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIToneCurve" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIToneCurve

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIToneCurve : CIFilter {
        
        public CIToneCurve ();
        public CIToneCurve (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public CIVector Point0 {
                get;
                set;
        }
        public CIVector Point1 {
                get;
                set;
        }
        public CIVector Point2 {
                get;
                set;
        }
        public CIVector Point3 {
                get;
                set;
        }
        public CIVector Point4 {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIVector" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIVector

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIVector : MonoTouch.Foundation.NSObject {
        
        public CIVector (float [] values);
        public CIVector ();
        public CIVector (MonoTouch.Foundation.NSCoder coder);
        public CIVector (MonoTouch.Foundation.NSObjectFlag t);
        public CIVector (IntPtr handle);
        public CIVector (float x);
        public CIVector (float x, float y);
        public CIVector (float x, float y, float z);
        public CIVector (float x, float y, float z, float w);
        public CIVector (string representation);
        
        public static CIVector Create (MonoTouch.CoreGraphics.CGAffineTransform affineTransform);
        public static CIVector Create (System.Drawing.PointF point);
        public static CIVector Create (System.Drawing.RectangleF point);
        public static CIVector Create (float x);
        public static CIVector Create (float x, float y);
        public static CIVector Create (float x, float y, float z);
        public static CIVector Create (float x, float y, float z, float w);
        public static CIVector FromString (string representation);
        public static CIVector FromValues (float [] values);
        public override string ToString ();
        
        public virtual MonoTouch.CoreGraphics.CGAffineTransform AffineTransform {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int Count {
                get;
        }
        public virtual System.Drawing.PointF Point {
                get;
        }
        public virtual System.Drawing.RectangleF Rectangle {
                get;
        }
        public virtual float W {
                get;
        }
        public virtual float X {
                get;
        }
        public virtual float Y {
                get;
        }
        public virtual float Z {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIVibrance" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIVibrance

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIVibrance : CIFilter {
        
        public CIVibrance ();
        public CIVibrance (IntPtr handle);
        
        public float Amount {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIVignette" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIVignette

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIVignette : CIFilter {
        
        public CIVignette ();
        public CIVignette (IntPtr handle);
        
        public CIImage Image {
                get;
                set;
        }
        public float Intensity {
                get;
                set;
        }
        public float Radius {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreImage.CIWhitePointAdjust" class="injected"></a>


## New Type: MonoTouch.CoreImage.CIWhitePointAdjust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CIWhitePointAdjust : CIFilter {
        
        public CIWhitePointAdjust ();
        public CIWhitePointAdjust (IntPtr handle);
        
        public CIColor Color {
                get;
                set;
        }
        public CIImage Image {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.CoreLocation.CLGeocodeCompletionHandler" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLGeocodeCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void CLGeocodeCompletionHandler (CLPlacemark[] placemarks, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLGeocoder" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLGeocoder

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CLGeocoder : MonoTouch.Foundation.NSObject {
        
        public CLGeocoder ();
        public CLGeocoder (MonoTouch.Foundation.NSCoder coder);
        public CLGeocoder (MonoTouch.Foundation.NSObjectFlag t);
        public CLGeocoder (IntPtr handle);
        
        public virtual void CancelGeocode ();
        public virtual void GeocodeAddress (MonoTouch.Foundation.NSDictionary addressDictionary, CLGeocodeCompletionHandler completionHandler);
        public virtual void GeocodeAddress (string addressString, CLGeocodeCompletionHandler completionHandler);
        public virtual void GeocodeAddress (string addressString, CLRegion region, CLGeocodeCompletionHandler completionHandler);
        public virtual void ReverseGeocodeLocation (CLLocation location, CLGeocodeCompletionHandler completionHandler);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Geocoding {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocation" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString ErrorUserInfoAlternateRegionKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void StartMonitoring (CLRegion region);
        public event EventHandler DidStartMonitoringForRegion;
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void DidStartMonitoringForRegion (CLRegion region);
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLPlacemark" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLPlacemark

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CLPlacemark : MonoTouch.Foundation.NSObject {
        
        public CLPlacemark ();
        public CLPlacemark (MonoTouch.Foundation.NSCoder coder);
        public CLPlacemark (MonoTouch.Foundation.NSObjectFlag t);
        public CLPlacemark (IntPtr handle);
        public CLPlacemark (CLPlacemark placemark);
        
        protected override void Dispose (bool disposing);
        
        public virtual MonoTouch.Foundation.NSDictionary AddressDictionary {
                get;
        }
        public virtual string AdministrativeArea {
                get;
        }
        public virtual string [] AreasOfInterest {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Country {
                get;
        }
        public virtual string InlandWater {
                get;
        }
        public virtual string IsoCountryCode {
                get;
        }
        public virtual string Locality {
                get;
        }
        public virtual CLLocation Location {
                get;
        }
        public virtual string Name {
                get;
        }
        public virtual string Ocean {
                get;
        }
        public virtual string PostalCode {
                get;
        }
        public virtual CLRegion Region {
                get;
        }
        public virtual string SubAdministrativeArea {
                get;
        }
        public virtual string SubLocality {
                get;
        }
        public virtual string SubThoroughfare {
                get;
        }
        public virtual string Thoroughfare {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAttitudeReferenceFrame" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAttitudeReferenceFrame

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 [Flags]
 public enum CMAttitudeReferenceFrame {
        XArbitraryZVertical,
        XArbitraryCorrectedZVertical,
        XMagneticNorthZVertical,
        XTrueNorthZVertical
 }
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMCalibratedMagneticField" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMCalibratedMagneticField

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public struct CMCalibratedMagneticField {
        
        public override string ToString ();
        
        public CMMagneticField Field;
        public CMMagneticFieldCalibrationAccuracy Accuracy;
}
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMDeviceMotion" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMDeviceMotion

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual CMCalibratedMagneticField MagneticField {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMError" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
DeviceRequiresMovement,
        TrueNorthNotAvailable
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMMagneticField" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMMagneticField

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public struct CMMagneticField {
        
        public override string ToString ();
        
        public double X;
        public double Y;
        public double Z;
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMMagneticFieldCalibrationAccuracy" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMMagneticFieldCalibrationAccuracy

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum CMMagneticFieldCalibrationAccuracy {
        Uncalibrated,
        Low,
        Medium,
        High
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMMagnetometerData" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMMagnetometerData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class CMMagnetometerData : CMLogItem {
        
        public CMMagnetometerData ();
        public CMMagnetometerData (MonoTouch.Foundation.NSCoder coder);
        public CMMagnetometerData (MonoTouch.Foundation.NSObjectFlag t);
        public CMMagnetometerData (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CMMagneticField MagneticField {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMotion.CMMagnetometerHandler" class="injected"></a>


## New Type: MonoTouch.CoreMotion.CMMagnetometerHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void CMMagnetometerHandler (CMMagnetometerData magnetometerData, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMMotionManager" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMMotionManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame);
        public virtual void StartDeviceMotionUpdates (CMAttitudeReferenceFrame referenceFrame, MonoTouch.Foundation.NSOperationQueue queue, CMMagnetometerHandler handler);
        public virtual void StartMagnetometerUpdates ();
        public virtual void StartMagnetometerUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMMagnetometerHandler handler);
        public virtual void StopMagnetometerUpdates ();
        public static CMAttitudeReferenceFrame AvailableAttitudeReferenceFrames {
                get;
        }
        public virtual CMAttitudeReferenceFrame AttitudeReferenceFrame {
                get;
        }
        public virtual bool MagnetometerActive {
                get;
                set;
        }
        public virtual bool MagnetometerAvailable {
                get;
        }
        public virtual CMMagnetometerData MagnetometerData {
                get;
        }
        public virtual double MagnetometerUpdateInterval {
                get;
                set;
        }
        public virtual bool ShowsDeviceMovementDisplay {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.EventKit.EKAlarm" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKAlarm

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Changed:

```
public class EKAlarm : MonoTouch.Foundation.NSObject {
```

Added:

```
public class EKAlarm : EKObject {
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKCalendar" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKCalendar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The removals are part of Apple's refactoring of the class hierarchy.

Changed:

```
public class EKCalendar : MonoTouch.Foundation.NSObject {
```

Added:

```
public class EKCalendar : EKObject {
        public static EKCalendar FromEventStore (EKEventStore eventStore);
        protected override void Dispose (bool disposing);
        
        public virtual string CalendarIdentifier {
                get;
        }
        public virtual bool Immutable {
                get;
        }
        public virtual EKSource Source {
                get;
                set;
        }
        public virtual bool Subscribed {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKCalendarItem" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKCalendarItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class EKCalendarItem : EKObject {
        
        public EKCalendarItem ();
        public EKCalendarItem (MonoTouch.Foundation.NSCoder coder);
        public EKCalendarItem (MonoTouch.Foundation.NSObjectFlag t);
        public EKCalendarItem (IntPtr handle);
        
        public virtual void AddAlarm (EKAlarm alarm);
        public virtual void AddRecurrenceRule (EKRecurrenceRule rule);
        protected override void Dispose (bool disposing);
        public virtual void RemoveAlarm (EKAlarm alarm);
        public virtual void RemoveRecurrenceRule (EKRecurrenceRule rule);
        
        public virtual EKAlarm[] Alarms {
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
        public virtual MonoTouch.Foundation.NSDate CreationDate {
                get;
        }
        public virtual bool HasAlarms {
                get;
        }
        public virtual bool HasAttendees {
                get;
        }
        public virtual bool HasNotes {
                get;
        }
        public virtual bool HasRecurrenceRules {
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
        public virtual EKRecurrenceRule[] RecurrenceRules {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSTimeZone TimeZone {
                get;
                set;
        }
        public virtual string Title {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
                set;
        }
        public virtual string UUID {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKErrorCode" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKErrorCode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
CalendarHasNoSource,
        CalendarSourceCannotBeModified,
        CalendarIsImmutable,
        SourceDoesNotAllowCalendarAddDelete
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The changes to this class reflect Apple's source-code compatible refactoring
of the API.

Changed:

```
public class EKEvent : MonoTouch.Foundation.NSObject {
        public virtual void AddAlarm (EKAlarm alarm);
        public virtual void RemoveAlarm (EKAlarm alarm);
        public virtual EKAlarm[] Alarms {
                get;
                set;
        }
        public virtual EKParticipant[] Attendees {
                get;
        }
        public virtual EKCalendar Calendar {
                set;
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
        public virtual string Title {
                get;
                set;
        }
```

Added:

```
public class EKEvent : EKCalendarItem {
        public virtual int birthdayPersonID {
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool Commit (out MonoTouch.Foundation.NSError error);
        public virtual EKCalendar GetCalendar (string identifier);
        public virtual EKSource GetSource (string identifier);
        public virtual void RefreshSourcesIfNecessary ();
        public virtual bool RemoveCalendarc (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual bool RemoveEvent (EKEvent ekEvent, EKSpan span, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual void Reset ();
        public virtual bool SaveCalendar (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual bool SaveEvent (EKEvent ekEvent, EKSpan span, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual EKSource[] Sources {
                get;
        }
```

 <a name="New_Type:_MonoTouch.EventKit.EKObject" class="injected"></a>


## New Type: MonoTouch.EventKit.EKObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class EKObject : MonoTouch.Foundation.NSObject {
        
        public EKObject ();
        public EKObject (MonoTouch.Foundation.NSCoder coder);
        public EKObject (MonoTouch.Foundation.NSObjectFlag t);
        public EKObject (IntPtr handle);
        
        public virtual bool Refresh ();
        public virtual void Reset ();
        public virtual void Rollback ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool HasChanges {
                get;
        }
        public virtual bool IsNew {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKParticipant" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKParticipant

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The changes to this class reflect Apple's source-code compatible refactoring
of the API.

Removed:

```
public class EKParticipant : MonoTouch.Foundation.NSObject {
```

Added:

```
public class EKParticipant : EKObject {
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKRecurrenceDayOfWeek" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKRecurrenceDayOfWeek

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public EKRecurrenceDayOfWeek (int dayOfTheWeek, int weekNumber);
        public static EKRecurrenceDayOfWeek FromWeekDay (int dayOfWeek, int weekNumber);
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKRecurrenceRule" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKRecurrenceRule

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The changes to this class reflect Apple's source-code compatible refactoring
of the API.

Removed:

```
public class EKRecurrenceRule : MonoTouch.Foundation.NSObject {
        public virtual MonoTouch.Foundation.NSNumber[] daysOfTheYear {
        public virtual MonoTouch.Foundation.NSNumber[] monthsOfTheYear {
```

Added:

```
public class EKRecurrenceRule : EKObject {
        public virtual MonoTouch.Foundation.NSNumber[] DaysOfTheYear {
        public virtual MonoTouch.Foundation.NSNumber[] MonthsOfTheYear {
```

 <a name="New_Type:_MonoTouch.EventKit.EKSource" class="injected"></a>


## New Type: MonoTouch.EventKit.EKSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class EKSource : EKObject {
        
        public EKSource ();
        public EKSource (MonoTouch.Foundation.NSCoder coder);
        public EKSource (MonoTouch.Foundation.NSObjectFlag t);
        public EKSource (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual MonoTouch.Foundation.NSSet Calendars {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string SourceIdentifier {
                get;
        }
        public virtual EKSourceType SourceType {
                get;
        }
        public virtual string Title {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKSourceType" class="injected"></a>


## New Type: MonoTouch.EventKit.EKSourceType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum EKSourceType {
        Local,
        Exchange,
        CalDav,
        MobileMe,
        Subscribed,
        Birthdays
}
```

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


# Namespace: MonoTouch.EventKitUI

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.EventKitUI.EKCalendarChooser" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKCalendarChooser

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class EKCalendarChooser : MonoTouch.UIKit.UIViewController {
        
        public EKCalendarChooser ();
        public EKCalendarChooser (MonoTouch.Foundation.NSCoder coder);
        public EKCalendarChooser (MonoTouch.Foundation.NSObjectFlag t);
        public EKCalendarChooser (IntPtr handle);
        public EKCalendarChooser (EKCalendarChooserSelectionStyle selectionStyle, EKCalendarChooserDisplayStyle displayStyle, MonoTouch.EventKit.EKEventStore eventStore);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public EKCalendarChooserDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSet SelectedCalendars {
                get;
                set;
        }
        public virtual EKCalendarChooserSelectionStyle SelectionStyle {
                get;
        }
        public virtual bool ShowsCancelButton {
                get;
                set;
        }
        public virtual bool ShowsDoneButton {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler Cancelled;
        public event EventHandler Finished;
        public event EventHandler SelectionChanged;
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKCalendarChooserDelegate" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKCalendarChooserDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class EKCalendarChooserDelegate : MonoTouch.Foundation.NSObject {
        
        public EKCalendarChooserDelegate ();
        public EKCalendarChooserDelegate (MonoTouch.Foundation.NSCoder coder);
        public EKCalendarChooserDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public EKCalendarChooserDelegate (IntPtr handle);
        
        public virtual void Cancelled (EKCalendarChooser calendarChooser);
        public virtual void Finished (EKCalendarChooser calendarChooser);
        public virtual void SelectionChanged (EKCalendarChooser calendarChooser);
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKCalendarChooserDisplayStyle" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKCalendarChooserDisplayStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum EKCalendarChooserDisplayStyle {
        AllCalendars,
        WritableCalendarsOnly
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKCalendarChooserSelectionStyle" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKCalendarChooserSelectionStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum EKCalendarChooserSelectionStyle {
        Single,
        Multiple
}
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSCalendarUnit" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCalendarUnit

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The enumerations have been fixed for consistency.

Removed:

```
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
```

Added:

```
Era,
        Year,
        Month,
        Day,
        Hour,
        Minute,
        Second,
        Week,
        Weekday,
        WeekdayOrdinal,
        Quarter,
        WeekOfMonth,
        WeekOfYear,
        YearForWeakOfYear,
        Calendar,
        TimeZone
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataReadingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataReadingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
Coordinated,
        MappedAlways
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataWritingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataWritingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
NSDataWritingFileProtectionMask
```

Added:

```
Coordinated,
        FileProtectionMask,
        FileProtectionCompleteUnlessOpen,
        FileProtectionCompleteUntilFirstUserAuthentication
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDateComponents" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDateComponents

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual int WeekOfMonth {
                get;
                set;
        }
        public virtual int WeekOfYear {
                get;
                set;
        }
        public virtual int YearForWeekOfYear {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSExpression" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSExpression

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public static NSExpression FromFuction (string name, NSExpression[] parameters);
```

Added:

```
public static NSExpression FromFormat (string format, NSExpression[] parameters);
        public static NSExpression FromFunction (string name, NSExpression[] parameters);
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileCoordinator" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileCoordinator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSFileCoordinator : NSObject {
        
        public NSFileCoordinator ();
        public NSFileCoordinator (NSCoder coder);
        public NSFileCoordinator (NSObjectFlag t);
        public NSFileCoordinator (IntPtr handle);
        public NSFileCoordinator (NSFilePresenter filePresenterOrNil);
        
        public static void RemoveFilePresenter (NSFilePresenter filePresenter);
        public virtual void AddFilePresenter (NSFilePresenter filePresenter);
        public virtual void Cancel ();
        public virtual void CoordinateBatc (NSUrl[] readingURLs, NSFileCoordinatorReadingOptions readingOptions, NSUrl[] writingURLs, NSFileCoordinatorWritingOptions writingOptions, NSError error, NSAction batchHandler);
        public virtual void CoordinateRead (NSUrl itemUrl, NSFileCoordinatorReadingOptions options, out NSError error, NSFileCoordinatorWorker worker);
        public virtual void CoordinateReadWrite (NSUrl readingURL, NSFileCoordinatorReadingOptions readingOptions, NSUrl writingURL, NSFileCoordinatorWritingOptions writingOptions, out NSError error, NSFileCoordinatorWorkerRW readWriteWorker);
        public virtual void CoordinateWrite (NSUrl url, NSFileCoordinatorWritingOptions options, out NSError error, NSFileCoordinatorWorker worker);
        public virtual void ItemMoved (NSUrl fromUrl, NSUrl toUrl);
        
        public static NSFilePresenter[] FilePresenters {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileCoordinatorReadingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileCoordinatorReadingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSFileCoordinatorReadingOptions {
        WithoutChanges
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileCoordinatorWorker" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileCoordinatorWorker

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void NSFileCoordinatorWorker (NSUrl newUrl);
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileCoordinatorWorkerRW" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileCoordinatorWorkerRW

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void NSFileCoordinatorWorkerRW (NSUrl newReadingUrl, NSUrl newWritingUrl);
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileCoordinatorWritingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileCoordinatorWritingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSFileCoordinatorWritingOptions {
        ForDeleting,
        ForMoving,
        ForMerging
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool CreateDirectory (NSUrl url, bool createIntermediates, NSDictionary attributes, out NSError error);
        public virtual bool CreateSymbolicLink (NSUrl url, NSUrl destURL, out NSError error);
        public virtual bool EvictUbiquitous (NSUrl url, out NSError error);
        public virtual NSUrl GetUrlForPublishingUbiquitousItem (NSUrl url, out NSDate expirationDate, out NSError error);
        public virtual NSUrl GetUrlForUbiquityContainer (string containerIdentifier);
        public virtual bool IsUbiquitous (NSUrl url);
        public virtual bool SetUbiquitous (bool flag, NSUrl url, NSUrl destinationUrl, out NSError error);
        public virtual bool StartDownloadingUbiquitous (NSUrl url, out NSError error);
        public static NSString FileProtectionComplete {
                get;
        }
        public static NSString FileProtectionCompleteUnlessOpen {
                get;
        }
        public static NSString FileProtectionCompleteUntilFirstUserAuthentication {
                get;
        }
        public static NSString FileProtectionKey {
                get;
        }
        public static NSString FileProtectionNone {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSFilePresenter" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFilePresenter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class NSFilePresenter : NSObject {
        
        public NSFilePresenter ();
        public NSFilePresenter (NSCoder coder);
        public NSFilePresenter (NSObjectFlag t);
        public NSFilePresenter (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void PresentedItemChanged ();
        public virtual void PresentedItemGainedVersion (NSFileVersion version);
        public virtual void PresentedItemLostVersion (NSFileVersion version);
        public virtual void PresentedItemMoved (NSUrl newURL);
        public virtual void PresentedItemResolveConflictVersion (NSFileVersion version);
        public virtual void PresentedSubitemAppeared (NSUrl atUrl);
        public virtual void PresentedSubitemChanged (NSUrl url);
        public virtual void PresentedSubitemGainedVersion (NSUrl url, NSFileVersion version);
        public virtual void PresentedSubitemLostVersion (NSUrl url, NSFileVersion version);
        public virtual void PresentedSubitemMoved (NSUrl oldURL, NSUrl newURL);
        public virtual void PresentedSubitemResolvedConflictVersion (NSUrl url, NSFileVersion version);
        
        public virtual NSOperationQueue PesentedItemOperationQueue {
                get;
        }
        public abstract NSUrl PresentedItemURL {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileVersion" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileVersion

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSFileVersion : NSObject {
        
        public NSFileVersion ();
        public NSFileVersion (NSCoder coder);
        public NSFileVersion (NSObjectFlag t);
        public NSFileVersion (IntPtr handle);
        
        public static NSFileVersion GetCurrentVersion (NSUrl url);
        public static NSFileVersion[] GetOtherVersions (NSUrl url);
        public static NSFileVersion GetSpecificVersion (NSUrl url, NSObject persistentIdentifier);
        public static NSFileVersion[] GetUnresolvedConflictVersions (NSUrl url);
        public static bool RemoveOtherVersions (NSUrl url, out NSError outError);
        protected override void Dispose (bool disposing);
        public virtual bool Remove (out NSError outError);
        public virtual NSUrl ReplaceItem (NSUrl url, NSFileVersionReplacingOptions options, out NSError error);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Discardable {
                get;
                set;
        }
        public virtual bool IsConflict {
                get;
        }
        public virtual string LocalizedName {
                get;
        }
        public virtual string LocalizedNameOfSavingComputer {
                get;
        }
        public virtual NSDate ModificationDate {
                get;
        }
        public virtual NSObject PersistentIdentifier {
                get;
        }
        public virtual bool Resolved {
                get;
                set;
        }
        public virtual NSUrl Url {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileVersionAddingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileVersionAddingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum NSFileVersionAddingOptions {
        ByMoving
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSFileVersionReplacingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileVersionReplacingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSFileVersionReplacingOptions {
        ByMoving
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookieStorage" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookieStorage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual NSHttpCookie[] GetSortedCookies (NSSortDescriptor[] sortDescriptors);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpUrlResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpUrlResponse

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public NSHttpUrlResponse (NSUrl url, int statusCode, string httpVersion, NSDictionary headerFields);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSIndexSet" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSIndexSet

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void EnumerateRanges (NSRangeIterator iterator);
        public virtual void EnumerateRanges (NSEnumerationOptions opts, NSRangeIterator iterator);
        public virtual void EnumerateRanges (NSRange range, NSEnumerationOptions opts, NSRangeIterator iterator);
```

 <a name="New_Type:_MonoTouch.Foundation.NSJsonReadingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSJsonReadingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSJsonReadingOptions {
        MutableContainers,
        MutableLeaves,
        AllowFragments
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSJsonSerialization" class="injected"></a>


## New Type: MonoTouch.Foundation.NSJsonSerialization

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSJsonSerialization : NSObject {
        
        public NSJsonSerialization ();
        public NSJsonSerialization (NSCoder coder);
        public NSJsonSerialization (NSObjectFlag t);
        public NSJsonSerialization (IntPtr handle);
        
        public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, NSError error);
        public static NSObject Deserialize (NSInputStream stream, NSJsonReadingOptions opt, out NSError error);
        public static bool IsValidJSONObject (NSObject obj);
        public static NSData Serialize (NSObject obj, NSJsonWritingOptions opt, out NSError error);
        public static int Serialize (NSObject obj, NSOutputStream stream, NSJsonWritingOptions opt, out NSError error);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSJsonWritingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSJsonWritingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSJsonWritingOptions {
        PrettyPrinted
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSLinguisticTag" class="injected"></a>


## New Type: MonoTouch.Foundation.NSLinguisticTag

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSLinguisticTag {
        
        public NSLinguisticTag ();
        
        public static NSString Adjective {
                get;
        }
        public static NSString Adverb {
                get;
        }
        public static NSString Classifier {
                get;
        }
        public static NSString CloseParenthesis {
                get;
        }
        public static NSString CloseQuote {
                get;
        }
        public static NSString Conjunction {
                get;
        }
        public static NSString Dash {
                get;
        }
        public static NSString Determiner {
                get;
        }
        public static NSString Idiom {
                get;
        }
        public static NSString Interjection {
                get;
        }
        public static NSString Noun {
                get;
        }
        public static NSString Number {
                get;
        }
        public static NSString OpenParenthesis {
                get;
        }
        public static NSString OpenQuote {
                get;
        }
        public static NSString OrganizationName {
                get;
        }
        public static NSString Other {
                get;
        }
        public static NSString OtherPunctuation {
                get;
        }
        public static NSString OtherWhitespace {
                get;
        }
        public static NSString OtherWord {
                get;
        }
        public static NSString ParagraphBreak {
                get;
        }
        public static NSString Particle {
                get;
        }
        public static NSString PersonalName {
                get;
        }
        public static NSString PlaceName {
                get;
        }
        public static NSString Preposition {
                get;
        }
        public static NSString Pronoun {
                get;
        }
        public static NSString Punctuation {
                get;
        }
        public static NSString SchemeLanguage {
                get;
        }
        public static NSString SchemeLemma {
                get;
        }
        public static NSString SchemeLexicalClass {
                get;
        }
        public static NSString SchemeNameType {
                get;
        }
        public static NSString SchemeNameTypeOrLexicalClass {
                get;
        }
        public static NSString SchemeScript {
                get;
        }
        public static NSString SchemeTokenType {
                get;
        }
        public static NSString SentenceTerminator {
                get;
        }
        public static NSString Verb {
                get;
        }
        public static NSString Whitespace {
                get;
        }
        public static NSString Word {
                get;
        }
        public static NSString WordJoiner {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSLinguisticTagger" class="injected"></a>


## New Type: MonoTouch.Foundation.NSLinguisticTagger

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSLinguisticTagger : NSObject {
        
        public NSLinguisticTagger ();
        public NSLinguisticTagger (NSCoder coder);
        public NSLinguisticTagger (NSObjectFlag t);
        public NSLinguisticTagger (IntPtr handle);
        public NSLinguisticTagger (NSString[] tagSchemes, NSLinguisticTaggerOptions opts);
        
        public static NSString[] GetAvailableTagSchemesForLanguage (string language);
        protected override void Dispose (bool disposing);
        public virtual void EnumerateTagsInRange (NSRange range, NSString tagScheme, NSLinguisticTaggerOptions opts, NSLingusticEnumerator enumerator);
        public virtual NSRange GetSentenceRangeForRange (NSRange range);
        public virtual void SetOrthographyrange (NSOrthography orthography, NSRange range);
        public virtual void StringEditedInRange (NSRange newRange, int delta);
        
        public virtual string AnalysisString {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSString[] TagSchemes {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSLinguisticTaggerOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSLinguisticTaggerOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum NSLinguisticTaggerOptions {
        OmitWords,
        OmitPunctuation,
        OmitWhitespace,
        OmitOther,
        JoinNames
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSLingusticEnumerator" class="injected"></a>


## New Type: MonoTouch.Foundation.NSLingusticEnumerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void NSLingusticEnumerator (NSString tag, NSRange tokenRange, NSRange sentenceRange, ref bool stop);
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataItem" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMetadataItem : NSObject {
        
        public NSMetadataItem ();
        public NSMetadataItem (NSCoder coder);
        public NSMetadataItem (NSObjectFlag t);
        public NSMetadataItem (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual NSObject ValueForAttribute (string key);
        public virtual NSDictionary ValuesForAttributes (NSArray keys);
        
        public virtual NSObject[] Attributes {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQuery" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQuery

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMetadataQuery : NSObject {
        
        public NSMetadataQuery ();
        public NSMetadataQuery (NSCoder coder);
        public NSMetadataQuery (NSObjectFlag t);
        public NSMetadataQuery (IntPtr handle);
        
        public virtual void DisableUpdates ();
        protected override void Dispose (bool disposing);
        public virtual void EnableUpdates ();
        public virtual int IndexOfResult (NSObject result);
        public virtual NSObject ResultAtIndex (int idx);
        public virtual bool StartQuery ();
        public virtual void StopQuery ();
        public virtual NSObject ValueOfAttribute (string attribyteName, int atIndex);
        
        public static NSString DidFinishGatheringNotification {
                get;
        }
        public static NSString DidStartGatheringNotification {
                get;
        }
        public static NSString DidUpdateNotification {
                get;
        }
        public static NSString GatheringProgressNotification {
                get;
        }
        public static NSString ItemDisplayNameKey {
                get;
        }
        public static NSString ItemFSContentChangeDateKey {
                get;
        }
        public static NSString ItemFSCreationDateKey {
                get;
        }
        public static NSString ItemFSNameKey {
                get;
        }
        public static NSString ItemFSSizeKey {
                get;
        }
        public static NSString ItemIsUbiquitousKey {
                get;
        }
        public static NSString ItemPathKey {
                get;
        }
        public static NSString ItemURLKey {
                get;
        }
        public static NSString LocalComputerScope {
                get;
        }
        public static NSString QueryLocalDocumentsScope {
                get;
        }
        public static NSString QueryNetworkScope {
                get;
        }
        public static NSString QueryUbiquitousDataScope {
                get;
        }
        public static NSString QueryUbiquitousDocumentsScope {
                get;
        }
        public static NSString ResultContentRelevanceAttribute {
                get;
        }
        public static NSString UbiquitousItemHasUnresolvedConflictsKey {
                get;
        }
        public static NSString UbiquitousItemIsDownloadedKey {
                get;
        }
        public static NSString UbiquitousItemIsDownloadingKey {
                get;
        }
        public static NSString UbiquitousItemIsUploadedKey {
                get;
        }
        public static NSString UbiquitousItemIsUploadingKey {
                get;
        }
        public static NSString UbiquitousItemPercentDownloadedKey {
                get;
        }
        public static NSString UbiquitousItemPercentUploadedKey {
                get;
        }
        public static NSString UserHomeScope {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public NSMetadataQueryDelegate Delegate {
                get;
                set;
        }
        public virtual NSObject[] GroupedResults {
                get;
        }
        public virtual NSArray GroupingAttributes {
                get;
                set;
        }
        public virtual bool IsGathering {
                get;
        }
        public virtual bool IsStarted {
                get;
        }
        public virtual bool IsStopped {
                get;
        }
        public virtual double NotificationBatchingInterval {
                get;
                set;
        }
        public virtual NSPredicate Predicate {
                get;
                set;
        }
        public NSMetadataQueryObject ReplacementObjectForResultObject {
                get;
                set;
        }
        public NSMetadataQueryValue ReplacementValueForAttributevalue {
                get;
                set;
        }
        public virtual int ResultCount {
                get;
        }
        public virtual NSMetadataItem[] Results {
                get;
        }
        public virtual NSObject[] SearchScopes {
                get;
                set;
        }
        public virtual NSSortDescriptor[] SortDescriptors {
                get;
                set;
        }
        public virtual NSObject[] ValueListAttributes {
                get;
                set;
        }
        public virtual NSDictionary ValueLists {
                get;
        }
        public virtual NSMetadataQueryDelegate WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQueryAttributeValueTuple" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQueryAttributeValueTuple

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMetadataQueryAttributeValueTuple : NSObject {
        
        public NSMetadataQueryAttributeValueTuple ();
        public NSMetadataQueryAttributeValueTuple (NSCoder coder);
        public NSMetadataQueryAttributeValueTuple (NSObjectFlag t);
        public NSMetadataQueryAttributeValueTuple (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual string Attribute {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int Count {
                get;
        }
        public virtual NSObject Value {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQueryDelegate" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQueryDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMetadataQueryDelegate : NSObject {
        
        public NSMetadataQueryDelegate ();
        public NSMetadataQueryDelegate (NSCoder coder);
        public NSMetadataQueryDelegate (NSObjectFlag t);
        public NSMetadataQueryDelegate (IntPtr handle);
        
        public virtual NSObject ReplacementObjectForResultObject (NSMetadataQuery query, NSMetadataItem result);
        public virtual NSObject ReplacementValueForAttributevalue (NSMetadataQuery query, string attributeName, NSObject value);
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQueryObject" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQueryObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate NSObject NSMetadataQueryObject (NSMetadataQuery query, NSMetadataItem result);
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQueryResultGroup" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQueryResultGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSMetadataQueryResultGroup : NSObject {
        
        public NSMetadataQueryResultGroup ();
        public NSMetadataQueryResultGroup (NSCoder coder);
        public NSMetadataQueryResultGroup (NSObjectFlag t);
        public NSMetadataQueryResultGroup (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual NSObject ResultAtIndex (uint idx);
        
        public virtual string Attribute {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int ResultCount {
                get;
        }
        public virtual NSObject[] Results {
                get;
        }
        public virtual NSObject[] Subgroups {
                get;
        }
        public virtual NSObject Value {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSMetadataQueryValue" class="injected"></a>


## New Type: MonoTouch.Foundation.NSMetadataQueryValue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate NSObject NSMetadataQueryValue (NSMetadataQuery query, string attributeName, NSObject value);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool ConformsToProtocol (IntPtr protocol);
```

 <a name="New_Type:_MonoTouch.Foundation.NSOrthography" class="injected"></a>


## New Type: MonoTouch.Foundation.NSOrthography

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSOrthography : NSObject {
        
        public NSOrthography ();
        public NSOrthography (NSCoder coder);
        public NSOrthography (NSObjectFlag t);
        public NSOrthography (IntPtr handle);
        public NSOrthography (string dominantScript, NSDictionary languageMap);
        
        protected override void Dispose (bool disposing);
        public virtual string DominantLanguageForScript (string script);
        public virtual string [] LanguagesForScript (string script);
        
        public virtual string [] AllLanguages {
                get;
        }
        public virtual string [] AllScripts {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string DominantLanguage {
                get;
        }
        public virtual string DominantScript {
                get;
        }
        public virtual NSDictionary LanguageMap {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSProcessInfo" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSProcessInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public virtual uint ActiveProcessorCount {
        public virtual uint OperatingSystem {
        public virtual ulong PhysicalMemory {
        public virtual uint ProcessorCount {
```

Added:

```
public virtual int ActiveProcessorCount {
        public virtual int OperatingSystem {
        public virtual long PhysicalMemory {
        public virtual int ProcessorCount {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRangeIterator" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRangeIterator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void NSRangeIterator (NSRange range, ref bool stop);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStream" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStream

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public virtual NSObject PropertyForKey (string key);
        public virtual bool SetPropertyForKey (NSObject property, string key);
```

Added:

```
public static NSString DataWrittenToMemoryStreamKey {
                get;
        }
        public static NSString FileCurrentOffsetKey {
                get;
        }
        public static NSString NetworkServiceType {
                get;
        }
        public static NSString NetworkServiceTypeBackground {
                get;
        }
        public static NSString NetworkServiceTypeVideo {
                get;
        }
        public static NSString NetworkServiceTypeVoice {
                get;
        }
        public static NSString SocketSecurityLevelKey {
                get;
        }
        public static NSString SocketSecurityLevelNegotiatedSsl {
                get;
        }
        public static NSString SocketSecurityLevelNone {
                get;
        }
        public static NSString SocketSecurityLevelSslV2 {
                get;
        }
        public static NSString SocketSecurityLevelSslV3 {
                get;
        }
        public static NSString SocketSecurityLevelTlsV1 {
                get;
        }
        public static NSString SocketSslErrorDomain {
                get;
        }
        public static NSString SocksErrorDomain {
                get;
        }
        public static NSString SocksProxyConfigurationKey {
                get;
        }
        public static NSString SocksProxyHostKey {
                get;
        }
        public static NSString SocksProxyPasswordKey {
                get;
        }
        public static NSString SocksProxyPortKey {
                get;
        }
        public static NSString SocksProxyUserKey {
                get;
        }
        public static NSString SocksProxyVersion4 {
                get;
        }
        public static NSString SocksProxyVersion5 {
                get;
        }
        public static NSString SocksProxyVersionKey {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSUbiquitousKeyValueStore" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUbiquitousKeyValueStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NSUbiquitousKeyValueStore : NSObject {
        
        public NSUbiquitousKeyValueStore ();
        public NSUbiquitousKeyValueStore (NSCoder coder);
        public NSUbiquitousKeyValueStore (NSObjectFlag t);
        public NSUbiquitousKeyValueStore (IntPtr handle);
        
        public virtual NSDictionary DictionaryRepresentation ();
        public virtual NSObject[] GetArray (string aKey);
        public virtual bool GetBool (string aKey);
        public virtual NSData GetData (string aKey);
        public virtual NSDictionary GetDictionary (string aKey);
        public virtual double GetDouble (string aKey);
        public virtual long GetLong (string aKey);
        public virtual string GetString (string aKey);
        public virtual void Remove (string aKey);
        public void SetArray (string key, NSObject[] value);
        public void SetBool (string key, bool value);
        public void SetData (string key, NSData value);
        public void SetDictionary (string key, NSDictionary value);
        public void SetDouble (string key, double value);
        public void SetLong (string key, long value);
        public void SetString (string key, string value);
        public virtual bool Synchronize ();
        
        public static NSString ChangedKeysKey {
                get;
        }
        public static NSString ChangeReasonKey {
                get;
        }
        public static NSUbiquitousKeyValueStore DefaultStore {
                get;
        }
        public static NSString DidChangeExternallyNotification {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public NSObject this [NSString key] {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeReason" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeReason

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum NSUbiquitousKeyValueStoreChangeReason {
        ServerChange,
        InitialSyncChange,
        QuotaViolationChange
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUndoManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUndoManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void SetActionIsDiscardable (bool discardable);
        public static NSString DidCloseUndoGroupNotification {
                get;
        }
        public static NSString GroupIsDiscardableKey {
                get;
        }
        public virtual bool RedoActionIsDiscardable {
                get;
        }
        public virtual bool UndoActionIsDiscardable {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual NSUrl Append (string pathComponent, bool isDirectory);
        public virtual NSDictionary GetResourceValues (NSString[] keys, out NSError error);
        public bool SetResource (string key, NSObject value);
        public bool SetResource (string key, NSObject value, out NSError error);
        public bool TryGetResource (string key, out NSObject value);
        public bool TryGetResource (string key, out NSObject value, out NSError error);
        public static NSString AttributeModificationDateKey {
                get;
        }
        public static NSString ContentAccessDateKey {
                get;
        }
        public static NSString ContentModificationDateKey {
                get;
        }
        public static NSString CreationDateKey {
                get;
        }
        public static NSString CustomIconKey {
                get;
        }
        public static NSString EffectiveIconKey {
                get;
        }
        public static NSString FileAllocatedSizeKey {
                get;
        }
        public static NSString FileResourceIdentifierKey {
                get;
        }
        public static NSString FileResourceTypeBlockSpecial {
                get;
        }
        public static NSString FileResourceTypeCharacterSpecial {
                get;
        }
        public static NSString FileResourceTypeDirectory {
                get;
        }
        public static NSString FileResourceTypeKey {
                get;
        }
        public static NSString FileResourceTypeNamedPipe {
                get;
        }
        public static NSString FileResourceTypeRegular {
                get;
        }
        public static NSString FileResourceTypeSocket {
                get;
        }
        public static NSString FileResourceTypeSymbolicLink {
                get;
        }
        public static NSString FileResourceTypeUnknown {
                get;
        }
        public static NSString FileSecurityKey {
                get;
        }
        public static NSString FileSizeKey {
                get;
        }
        public static NSString HasHiddenExtensionKey {
                get;
        }
        public static NSString IsAliasFileKey {
                get;
        }
        public static NSString IsDirectoryKey {
                get;
        }
        public static NSString IsExecutableKey {
                get;
        }
        public static NSString IsHiddenKey {
                get;
        }
        public static NSString IsMountTriggerKey {
                get;
        }
        public static NSString IsPackageKey {
                get;
        }
        public static NSString IsReadableKey {
                get;
        }
        public static NSString IsRegularFileKey {
                get;
        }
        public static NSString IsSymbolicLinkKey {
                get;
        }
        public static NSString IsSystemImmutableKey {
                get;
        }
        public static NSString IsUbiquitousItemKey {
                get;
        }
        public static NSString IsUserImmutableKey {
                get;
        }
        public static NSString IsVolumeKey {
                get;
        }
        public static NSString IsWritableKey {
                get;
        }
        public static NSString KeysOfUnsetValuesKey {
                get;
        }
        public static NSString LabelColorKey {
                get;
        }
        public static NSString LabelNumberKey {
                get;
        }
        public static NSString LinkCountKey {
                get;
        }
        public static NSString LocalizedLabelKey {
                get;
        }
        public static NSString LocalizedNameKey {
                get;
        }
        public static NSString LocalizedTypeDescriptionKey {
                get;
        }
        public static NSString NameKey {
                get;
        }
        public static NSString ParentDirectoryURLKey {
                get;
        }
        public static NSString PreferredIOBlockSizeKey {
                get;
        }
        public static NSString TotalFileAllocatedSizeKey {
                get;
        }
        public static NSString TotalFileSizeKey {
                get;
        }
        public static NSString TypeIdentifierKey {
                get;
        }
        public static NSString UbiquitousItemHasUnresolvedConflictsKey {
                get;
        }
        public static NSString UbiquitousItemIsDownloadedKey {
                get;
        }
        public static NSString UbiquitousItemIsDownloadingKey {
                get;
        }
        public static NSString UbiquitousItemIsUploadedKey {
                get;
        }
        public static NSString UbiquitousItemIsUploadingKey {
                get;
        }
        public static NSString UbiquitousItemPercentDownloadedKey {
                get;
        }
        public static NSString UbiquitousItemPercentUploadedKey {
                get;
        }
        public static NSString VolumeAvailableCapacityKey {
                get;
        }
        public static NSString VolumeCreationDateKey {
                get;
        }
        public static NSString VolumeIdentifierKey {
                get;
        }
        public static NSString VolumeIsAutomountedKey {
                get;
        }
        public static NSString VolumeIsBrowsableKey {
                get;
        }
        public static NSString VolumeIsEjectableKey {
                get;
        }
        public static NSString VolumeIsInternalKey {
                get;
        }
        public static NSString VolumeIsJournalingKey {
                get;
        }
        public static NSString VolumeIsLocalKey {
                get;
        }
        public static NSString VolumeIsReadOnlyKey {
                get;
        }
        public static NSString VolumeIsRemovableKey {
                get;
        }
        public static NSString VolumeLocalizedFormatDescriptionKey {
                get;
        }
        public static NSString VolumeLocalizedNameKey {
                get;
        }
        public static NSString VolumeMaximumFileSizeKey {
                get;
        }
        public static NSString VolumeNameKey {
                get;
        }
        public static NSString VolumeResourceCountKey {
                get;
        }
        public static NSString VolumeSupportsAdvisoryFileLockingKey {
                get;
        }
        public static NSString VolumeSupportsCasePreservedNamesKey {
                get;
        }
        public static NSString VolumeSupportsCaseSensitiveNamesKey {
                get;
        }
        public static NSString VolumeSupportsExtendedSecurityKey {
                get;
        }
        public static NSString VolumeSupportsHardLinksKey {
                get;
        }
        public static NSString VolumeSupportsJournalingKey {
                get;
        }
        public static NSString VolumeSupportsPersistentIDsKey {
                get;
        }
        public static NSString VolumeSupportsRenamingKey {
                get;
        }
        public static NSString VolumeSupportsRootDirectoryDatesKey {
                get;
        }
        public static NSString VolumeSupportsSparseFilesKey {
                get;
        }
        public static NSString VolumeSupportsSymbolicLinksKey {
                get;
        }
        public static NSString VolumeSupportsVolumeSizesKey {
                get;
        }
        public static NSString VolumeSupportsZeroRunsKey {
                get;
        }
        public static NSString VolumeTotalCapacityKey {
                get;
        }
        public static NSString VolumeURLForRemountingKey {
                get;
        }
        public static NSString VolumeURLKey {
                get;
        }
        public static NSString VolumeUUIDStringKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlAuthenticationChallenge" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlAuthenticationChallenge

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void PejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
        public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnection" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static void SendAsynchronousRequest (NSUrlRequest request, NSOperationQueue queue, NSUrlConnectionDataResponse completionHandler);
        protected override void Dispose (bool disposing);
        public virtual void SetDelegateQueue (NSOperationQueue queue);
        public virtual NSUrlRequest CurrentRequest {
                get;
        }
        public virtual MonoTouch.NewsstandKit.NKAssetDownload NewsstandAssetDownload {
                get;
        }
        public virtual NSUrlRequest OriginalRequest {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnectionDataResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnectionDataResponse

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void NSUrlConnectionDataResponse (NSUrlResponse response, NSData data, NSError error);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnectionDownloadDelegate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnectionDownloadDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public abstract class NSUrlConnectionDownloadDelegate : NSUrlConnectionDelegate {
        
        public NSUrlConnectionDownloadDelegate ();
        public NSUrlConnectionDownloadDelegate (NSCoder coder);
        public NSUrlConnectionDownloadDelegate (NSObjectFlag t);
        public NSUrlConnectionDownloadDelegate (IntPtr handle);
        
        public override bool CanAuthenticateAgainstProtectionSpace (NSUrlConnection connection, NSUrlProtectionSpace protectionSpace);
        public override void CanceledAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
        public override bool ConnectionShouldUseCredentialStorage (NSUrlConnection connection);
        public override void FailedWithError (NSUrlConnection connection, NSError error);
        public abstract void FinishedDownloading (NSUrlConnection connection, NSUrl destinationUrl);
        public override void FinishedLoading (NSUrlConnection connection);
        public override NSInputStream NeedNewBodyStream (NSUrlConnection connection, NSUrlRequest request);
        public override void ReceivedAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
        public override void ReceivedData (NSUrlConnection connection, NSData data);
        public override void ReceivedResponse (NSUrlConnection connection, NSUrlResponse response);
        public virtual void ResumedDownloading (NSUrlConnection connection, long totalBytesWritten, long expectedTotalBytes);
        public override void SentBodyData (NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
        public override NSCachedUrlResponse WillCacheResponse (NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
        public override NSUrlRequest WillSendRequest (NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
        public virtual void WroteData (NSUrlConnection connection, long bytesWritten, long totalBytesWritten, long expectedTotalBytes);
 }
```

 <a name="Namespace:_MonoTouch.GLKit" class="injected"></a>


# Namespace: MonoTouch.GLKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.GLKit.GLKBaseEffect" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKBaseEffect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKBaseEffect : MonoTouch.Foundation.NSObject {
        
        public GLKBaseEffect ();
        public GLKBaseEffect (MonoTouch.Foundation.NSCoder coder);
        public GLKBaseEffect (MonoTouch.Foundation.NSObjectFlag t);
        public GLKBaseEffect (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void PrepareToDraw ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool ColorMaterialEnabled {
                get;
                set;
        }
        public virtual OpenTK.Vector4 ConstantColor {
                get;
                set;
        }
        public virtual GLKEffectPropertyFog Fog {
                get;
        }
        public virtual string Label {
                get;
                set;
        }
        public virtual GLKEffectPropertyLight Light0 {
                get;
        }
        public virtual GLKEffectPropertyLight Light1 {
                get;
        }
        public virtual GLKEffectPropertyLight Light2 {
                get;
        }
        public virtual GLKLightingType LightingType {
                get;
                set;
        }
        public virtual OpenTK.Vector4 LightModelAmbientColor {
                get;
                set;
        }
        public virtual bool LightModelTwoSided {
                get;
                set;
        }
        public virtual GLKEffectPropertyMaterial Material {
                get;
        }
        public virtual GLKEffectPropertyTexture Texture2d0 {
                get;
        }
        public virtual GLKEffectPropertyTexture Texture2d1 {
                get;
        }
        public virtual GLKEffectPropertyTexture[] TextureOrder {
                get;
                set;
        }
        public virtual GLKEffectPropertyTransform Transform {
                get;
        }
        public virtual bool UseConstantColor {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectProperty" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectProperty : MonoTouch.Foundation.NSObject {
        
        public GLKEffectProperty ();
        public GLKEffectProperty (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectProperty (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectProperty (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectPropertyFog" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectPropertyFog

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectPropertyFog : GLKEffectProperty {
        
        public GLKEffectPropertyFog ();
        public GLKEffectPropertyFog (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectPropertyFog (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectPropertyFog (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual OpenTK.Vector4 Color {
                get;
                set;
        }
        public virtual float Density {
                get;
                set;
        }
        public virtual bool Enabled {
                get;
                set;
        }
        public virtual float End {
                get;
                set;
        }
        public virtual GLKFogMode Mode {
                get;
                set;
        }
        public virtual float Start {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectPropertyLight" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectPropertyLight

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectPropertyLight : GLKEffectProperty {
        
        public GLKEffectPropertyLight ();
        public GLKEffectPropertyLight (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectPropertyLight (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectPropertyLight (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual OpenTK.Vector4 AmbientColor {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float ConstantAttenuation {
                get;
                set;
        }
        public virtual OpenTK.Vector4 DiffuseColor {
                get;
                set;
        }
        public virtual bool Enabled {
                get;
                set;
        }
        public virtual float LinearAttenuation {
                get;
                set;
        }
        public virtual OpenTK.Vector4 Position {
                get;
                set;
        }
        public virtual float QuadraticAttenuation {
                get;
                set;
        }
        public virtual OpenTK.Vector4 SpecularColor {
                get;
                set;
        }
        public virtual float SpotCutoff {
                get;
                set;
        }
        public virtual OpenTK.Vector3 SpotDirection {
                get;
                set;
        }
        public virtual float SpotExponent {
                get;
                set;
        }
        public virtual GLKEffectPropertyTransform Transform {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectPropertyMaterial" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectPropertyMaterial

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectPropertyMaterial : GLKEffectProperty {
        
        public GLKEffectPropertyMaterial ();
        public GLKEffectPropertyMaterial (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectPropertyMaterial (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectPropertyMaterial (IntPtr handle);
        
        public virtual OpenTK.Vector4 AmbientColor {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual OpenTK.Vector4 DiffuseColor {
                get;
                set;
        }
        public virtual OpenTK.Vector4 EmissiveColor {
                get;
                set;
        }
        public virtual float Shininess {
                get;
                set;
        }
        public virtual OpenTK.Vector4 SpecularColor {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectPropertyTexture" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectPropertyTexture

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectPropertyTexture : GLKEffectProperty {
        
        public GLKEffectPropertyTexture ();
        public GLKEffectPropertyTexture (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectPropertyTexture (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectPropertyTexture (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Enabled {
                get;
                set;
        }
        public virtual GLKTextureEnvMode EnvMode {
                get;
                set;
        }
        public virtual uint GLName {
                get;
                set;
        }
        public virtual GLKTextureTarget Target {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKEffectPropertyTransform" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKEffectPropertyTransform

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKEffectPropertyTransform : GLKEffectProperty {
        
        public GLKEffectPropertyTransform ();
        public GLKEffectPropertyTransform (MonoTouch.Foundation.NSCoder coder);
        public GLKEffectPropertyTransform (MonoTouch.Foundation.NSObjectFlag t);
        public GLKEffectPropertyTransform (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual OpenTK.Matrix4 ModelViewMatrix {
                get;
                set;
        }
        public virtual OpenTK.Matrix3 NormalMatrix {
                get;
        }
        public virtual OpenTK.Matrix4 ProjectionMatrix {
                get;
                set;
        }
        public virtual OpenTK.Matrix4 TextureMatrix {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKFogMode" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKFogMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKFogMode {
        Exp,
        Exp2,
        Linear
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKLightingType" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKLightingType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKLightingType {
        PerVertex,
        PerPixel
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKNamedEffect" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKNamedEffect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class GLKNamedEffect : MonoTouch.Foundation.NSObject {
        
        public GLKNamedEffect ();
        public GLKNamedEffect (MonoTouch.Foundation.NSCoder coder);
        public GLKNamedEffect (MonoTouch.Foundation.NSObjectFlag t);
        public GLKNamedEffect (IntPtr handle);
        
        public abstract void PrepareToDraw ();
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKReflectionMapEffect" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKReflectionMapEffect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKReflectionMapEffect : GLKBaseEffect {
        
        public GLKReflectionMapEffect ();
        public GLKReflectionMapEffect (MonoTouch.Foundation.NSCoder coder);
        public GLKReflectionMapEffect (MonoTouch.Foundation.NSObjectFlag t);
        public GLKReflectionMapEffect (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void PrepareToDraw ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual OpenTK.Matrix3 Matrix {
                get;
                set;
        }
        public virtual GLKEffectPropertyTexture TextureCubeMap {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKSkyboxEffect" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKSkyboxEffect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKSkyboxEffect : MonoTouch.Foundation.NSObject {
        
        public GLKSkyboxEffect ();
        public GLKSkyboxEffect (MonoTouch.Foundation.NSCoder coder);
        public GLKSkyboxEffect (MonoTouch.Foundation.NSObjectFlag t);
        public GLKSkyboxEffect (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void Draw ();
        public virtual void PrepareToDraw ();
        
        public virtual OpenTK.Vector3 Center {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Label {
                get;
                set;
        }
        public virtual GLKEffectPropertyTexture TextureCubeMap {
                get;
        }
        public virtual GLKEffectPropertyTransform Transform {
                get;
        }
        public virtual float XSize {
                get;
                set;
        }
        public virtual float YSize {
                get;
                set;
        }
        public virtual float ZSize {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureEnvMode" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureEnvMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKTextureEnvMode {
        Replace,
        Modulate,
        Decal
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureInfo" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKTextureInfo : MonoTouch.Foundation.NSObject {
        
        public GLKTextureInfo ();
        public GLKTextureInfo (MonoTouch.Foundation.NSCoder coder);
        public GLKTextureInfo (MonoTouch.Foundation.NSObjectFlag t);
        public GLKTextureInfo (IntPtr handle);
        
        public virtual GLKTextureInfoAlphaState AlphaState {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool ContainsMipmaps {
                get;
        }
        public virtual int Height {
                get;
        }
        public virtual uint Name {
                get;
        }
        public virtual GLKTextureTarget Target {
                get;
        }
        public virtual uint TextureName {
                get;
        }
        public virtual GLKTextureInfoOrigin TextureOrigin {
                get;
        }
        public virtual int Width {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureInfoAlphaState" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureInfoAlphaState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKTextureInfoAlphaState {
        None,
        NonPremultiplied,
        Premultiplied
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureInfoOrigin" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureInfoOrigin

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKTextureInfoOrigin {
        Unknown,
        TopLeft,
        BottomLeft
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureLoader" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureLoader

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKTextureLoader : MonoTouch.Foundation.NSObject {
        
        public GLKTextureLoader ();
        public GLKTextureLoader (MonoTouch.Foundation.NSCoder coder);
        public GLKTextureLoader (MonoTouch.Foundation.NSObjectFlag t);
        public GLKTextureLoader (IntPtr handle);
        
        public static GLKTextureInfo CubeMapFromFile (string path, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo CubeMapFromFiles (string [] files, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo CubeMapFromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo CubeMapFromUrls (MonoTouch.Foundation.NSUrl[] urls, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo FromData (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo FromFile (string path, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo FromImage (MonoTouch.CoreGraphics.CGImage cgImage, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public static GLKTextureInfo FromUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary textureOperations, out MonoTouch.Foundation.NSError error);
        public virtual void BeginLoadCubeMap (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public void BeginLoadCubeMap (MonoTouch.Foundation.NSUrl[] urls, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual void BeginLoadCubeMap (string fileName, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public void BeginLoadCubeMap (string [] files, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual void BeginTextureLoad (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual void BeginTextureLoad (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual void BeginTextureLoad (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual void BeginTextureLoad (string file, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue, GLKTextureLoaderCallback onComplete);
        public virtual IntPtr Constructors (MonoTouch.OpenGLES.EAGLSharegroup sharegroup);
        
        public static MonoTouch.Foundation.NSString ApplyPremultiplication {
                get;
        }
        public static MonoTouch.Foundation.NSString ErrorDomain {
                get;
        }
        public static MonoTouch.Foundation.NSString ErrorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString GenerateMipmaps {
                get;
        }
        public static MonoTouch.Foundation.NSString GLErrorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString GrayscaleAsAlpha {
                get;
        }
        public static MonoTouch.Foundation.NSString OriginBottomLeft {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureLoaderCallback" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureLoaderCallback

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void GLKTextureLoaderCallback (uint textureName, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureLoaderError" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureLoaderError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKTextureLoaderError {
        FileOrURLNotFound,
        InvalidNSData,
        InvalidCGImage,
        UnknownPathType,
        UnknownFileType,
        PVRAtlasUnsupported,
        CubeMapInvalidNumFiles,
        CompressedTextureUpload,
        UncompressedTextureUpload,
        UnsupportedCubeMapDimensions,
        UnsupportedBitDepth,
        UnsupportedPVRFormat,
        DataPreprocessingFailure,
        MipmapUnsupported,
        UnsupportedOrientation,
        ReorientationFailure,
        AlphaPremultiplicationFailure,
        InvalidEAGLContext
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKTextureTarget" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKTextureTarget

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKTextureTarget {
        Texture2D,
        CubeMap,
        TargetCt
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKVertexAttrib" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKVertexAttrib

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKVertexAttrib {
        Position,
        Normal,
        Color,
        TexCoord0,
        TexCoord1
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKView" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKView : MonoTouch.UIKit.UIView {
        
        public GLKView ();
        public GLKView (MonoTouch.Foundation.NSCoder coder);
        public GLKView (MonoTouch.Foundation.NSObjectFlag t);
        public GLKView (IntPtr handle);
        
        public static GLKViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void BindDrawable ();
        public virtual void DeleteDrawable ();
        public virtual void Display ();
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSObject InitWithFramecontext (System.Drawing.RectangleF frame, MonoTouch.OpenGLES.EAGLContext context);
        public virtual MonoTouch.UIKit.UIImage Snapshot ();
        
        public static GLKViewAppearance Appearance {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.OpenGLES.EAGLContext Context {
                get;
                set;
        }
        public GLKViewDelegate Delegate {
                get;
                set;
        }
        public virtual GLKViewDrawableColorFormat DrawableColorFormat {
                get;
                set;
        }
        public virtual GLKViewDrawableDepthFormat DrawableDepthFormat {
                get;
                set;
        }
        public virtual int DrawableHeight {
                get;
        }
        public virtual GLKViewDrawableMultisample DrawableMultisample {
                get;
                set;
        }
        public virtual GLKViewDrawableStencilFormat DrawableStencilFormat {
                get;
                set;
        }
        public virtual int DrawableWidth {
                get;
        }
        public virtual bool EnableSetNeedsDisplay {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public class GLKViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewController" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GLKViewController : MonoTouch.UIKit.UIViewController {
        
        public GLKViewController ();
        public GLKViewController (MonoTouch.Foundation.NSCoder coder);
        public GLKViewController (MonoTouch.Foundation.NSObjectFlag t);
        public GLKViewController (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public GLKViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual int FramesDisplayed {
                get;
        }
        public virtual int FramesPerSecond {
                get;
        }
        public virtual bool Paused {
                get;
                set;
        }
        public virtual bool PauseOnWillResignActive {
                get;
                set;
        }
        public virtual int PreferredFramesPerSecond {
                get;
                set;
        }
        public virtual bool ResumeOnDidBecomeActive {
                get;
                set;
        }
        public virtual double TimeSinceFirstResume {
                get;
        }
        public virtual double TimeSinceLastDraw {
                get;
        }
        public virtual double TimeSinceLastResume {
                get;
        }
        public virtual double TimeSinceLastUpdate {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class GLKViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GLKViewControllerDelegate ();
        public GLKViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GLKViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GLKViewControllerDelegate (IntPtr handle);
        
        public abstract void Update (GLKViewController controller);
        public virtual void WillPause (GLKViewController controller, bool pause);
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDelegate" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class GLKViewDelegate : MonoTouch.Foundation.NSObject {
        
        public GLKViewDelegate ();
        public GLKViewDelegate (MonoTouch.Foundation.NSCoder coder);
        public GLKViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GLKViewDelegate (IntPtr handle);
        
        public abstract void DrawInRect (GLKView view, System.Drawing.RectangleF rect);
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDrawableColorFormat" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDrawableColorFormat

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKViewDrawableColorFormat {
        RGBA8888,
        RGB565
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDrawableDepthFormat" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDrawableDepthFormat

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKViewDrawableDepthFormat {
        None,
        Format16,
        Format24
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDrawableMultisample" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDrawableMultisample

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKViewDrawableMultisample {
        None,
        Sample4x
}
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDrawableStencilFormat" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDrawableStencilFormat

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GLKViewDrawableStencilFormat {
        FormatNone,
        Format8
}
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool ShowsCompletionBanner {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboard

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static void SetDefaultLeaderboard (string categoryID, GKNotificationHandler notificationHandler);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatch

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public GKMatchReinvitation ShouldReinvitePlayer {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool ShouldReinvitePlayer (GKMatch match, string playerId);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void AddPlayersToMatch (GKMatch match);
        public virtual void SetHostedPlayerConnected (string playerID, bool connected);
        public virtual string DefaultInvitationMessage {
                get;
                set;
        }
        public event EventHandler<GKPlayerEventArgs> ReceivedAcceptFromHostedPlayer;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void ReceivedAcceptFromHostedPlayer (GKMatchmakerViewController viewController, string playerID);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchReinvitation" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchReinvitation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate bool GKMatchReinvitation (GKMatch match, string playerId);
```

 <a name="New_Type:_MonoTouch.GameKit.GKNotificationBanner" class="injected"></a>


## New Type: MonoTouch.GameKit.GKNotificationBanner

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKNotificationBanner : MonoTouch.Foundation.NSObject {
        
        public GKNotificationBanner ();
        public GKNotificationBanner (MonoTouch.Foundation.NSCoder coder);
        public GKNotificationBanner (MonoTouch.Foundation.NSObjectFlag t);
        public GKNotificationBanner (IntPtr handle);
        
        public static void Show (string title, string message, MonoTouch.Foundation.NSAction onCompleted);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKPhotoSize" class="injected"></a>


## New Type: MonoTouch.GameKit.GKPhotoSize

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GKPhotoSize {
        Small,
        Normal
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static void LoadPlayersForIdentifiers (string [] identifiers, GKPlayersHandler completionHandler);
        public virtual void LoadPhoto (GKPhotoSize size, GKPlayerPhotoLoaded onCompleted);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayerEventArgs" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayerEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public class GKPlayerEventArgs : EventArgs {
        
        public GKPlayerEventArgs (string playerID);
        
        public string PlayerID {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayerPhotoLoaded" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayerPhotoLoaded

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void GKPlayerPhotoLoaded (MonoTouch.UIKit.UIImage photo, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayersHandler" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayersHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate void GKPlayersHandler (GKPlayer[] players, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKScore" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKScore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual ulong Context {
                get;
                set;
        }
        public virtual bool ShouldSetDefaultLeaderboard {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedEventHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedEventHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKTurnBasedEventHandler : MonoTouch.Foundation.NSObject {
        
        public GKTurnBasedEventHandler ();
        public GKTurnBasedEventHandler (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedEventHandler (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedEventHandler (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public GKTurnBasedEventHandlerDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKTurnBasedEventHandlerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKTurnBasedEventHandlerDelegate ();
        public GKTurnBasedEventHandlerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedEventHandlerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedEventHandlerDelegate (IntPtr handle);
        
        public virtual void HandleInviteFromGameCenter (GKPlayer[] playersToInvite);
        public virtual void HandleMatchEnded (GKTurnBasedMatch match);
        public virtual void HandleTurnEventForMatch (GKTurnBasedMatch match);
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatch" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatch

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKTurnBasedMatch : MonoTouch.Foundation.NSObject {
        
        public GKTurnBasedMatch ();
        public GKTurnBasedMatch (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedMatch (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedMatch (IntPtr handle);
        
        public static void FindMatch (GKMatchRequest request, GKTurnBasedMatchRequest onCompletion);
        public static void LoadMatches (GKTurnBasedMatchesRequest onCompletion);
        protected override void Dispose (bool disposing);
        public virtual void EndMatchInTurn (MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
        public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipatn, MonoTouch.Foundation.NSData matchData, GKNotificationHandler noCompletion);
        public virtual void LoadMatchData (GKTurnBasedMatchData onCompletion);
        public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
        public virtual void ParticipantQuitOutOfTurn (GKTurnBasedMatchOutcome matchOutcome, GKNotificationHandler onCompletion);
        public virtual void Remove (GKNotificationHandler onCompletion);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate CreationDate {
                get;
        }
        public virtual GKTurnBasedParticipant CurrentParticipant {
                get;
        }
        public virtual MonoTouch.Foundation.NSData MatchData {
                get;
        }
        public virtual string MatchID {
                get;
        }
        public virtual string Message {
                get;
                set;
        }
        public virtual GKTurnBasedParticipant[] Participants {
                get;
        }
        public virtual GKTurnBasedMatchStatus Status {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchData" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchData

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void GKTurnBasedMatchData (MonoTouch.Foundation.NSData matchData, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchesRequest" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchesRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void GKTurnBasedMatchesRequest (GKTurnBasedMatch[] matches, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchmakerViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKTurnBasedMatchmakerViewController : MonoTouch.UIKit.UINavigationController {
        
        public GKTurnBasedMatchmakerViewController ();
        public GKTurnBasedMatchmakerViewController (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedMatchmakerViewController (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedMatchmakerViewController (IntPtr handle);
        public GKTurnBasedMatchmakerViewController (GKMatchRequest request);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public GKTurnBasedMatchmakerViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual bool ShowExistingMatches {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchmakerViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchmakerViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class GKTurnBasedMatchmakerViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKTurnBasedMatchmakerViewControllerDelegate ();
        public GKTurnBasedMatchmakerViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedMatchmakerViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedMatchmakerViewControllerDelegate (IntPtr handle);
        
        public abstract void FailedWithError (GKTurnBasedMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
        public abstract void FoundMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
        public abstract void PlayerQuitForMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
        public abstract void WasCancelled (GKTurnBasedMatchmakerViewController viewController);
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchOutcome" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchOutcome

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GKTurnBasedMatchOutcome {
        None,
        Quit,
        Won,
        Lost,
        Tied,
        TimeExpired,
        First,
        Second,
        Third,
        Fourth,
        CustomRange
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchRequest" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void GKTurnBasedMatchRequest (GKTurnBasedMatch match, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedMatchStatus" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedMatchStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GKTurnBasedMatchStatus {
        Unknown,
        Open,
        Ended,
        Matching
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedParticipant" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedParticipant

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class GKTurnBasedParticipant : MonoTouch.Foundation.NSObject {
        
        public GKTurnBasedParticipant ();
        public GKTurnBasedParticipant (MonoTouch.Foundation.NSCoder coder);
        public GKTurnBasedParticipant (MonoTouch.Foundation.NSObjectFlag t);
        public GKTurnBasedParticipant (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate LastTurnDate {
                get;
        }
        public virtual GKTurnBasedMatchOutcome MatchOutcome {
                get;
                set;
        }
        public virtual string PlayerID {
                get;
        }
        public virtual GKTurnBasedParticipantStatus Status {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKTurnBasedParticipantStatus" class="injected"></a>


## New Type: MonoTouch.GameKit.GKTurnBasedParticipantStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum GKTurnBasedParticipantStatus {
        Unknown,
        Invited,
        Declined,
        Matching,
        Active,
        Done
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKVoiceChat" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKVoiceChat

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual string [] PlayerIDs {
                get;
        }
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKAnnotationView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKAnnotationViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKAnnotationViewAppearance Appearance {
                get;
        }
        
        public class MKAnnotationViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKCircleView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKCircleView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKCircleViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKCircleViewAppearance Appearance {
                get;
        }
        
        public class MKCircleViewAppearance : MKOverlayPathViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

We now allow more than just MKAnnotations as parameters to RemoveAnnotations,
this change is source code compatible but allows for the refactoring that took
place in iOS5 to support the new CoreLocation role in the APIs.

Removed:

```
public virtual void RemoveAnnotation (MKAnnotation annotation);
        public virtual void RemoveAnnotations (MKAnnotation[] annotations);
        public virtual void SelectAnnotation (MKAnnotation annotation, bool animated);
```

Added:

```
public static MKMapViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void RemoveAnnotation (MonoTouch.Foundation.NSObject annotation);
        public virtual void RemoveAnnotations (MonoTouch.Foundation.NSObject[] annotations);
        public virtual void SelectAnnotation (MonoTouch.Foundation.NSObject annotation, bool animated);
        public virtual void SetUserTrackingMode (MKUserTrackingMode trackingMode, bool animated);
        public static MKMapViewAppearance Appearance {
                get;
        }
        public virtual MKUserTrackingMode UserTrackingMode {
                get;
                set;
        }
        public event EventHandler<MMapViewUserTrackingEventArgs> DidChageUserTrackingMode;
        
        public class MKMapViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void DidChageUserTrackingMode (MKMapView mapView, MKUserTrackingMode mode, bool animated);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKOverlayPathView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKOverlayPathView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKOverlayPathViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKOverlayPathViewAppearance Appearance {
                get;
        }
        
        public class MKOverlayPathViewAppearance : MKOverlayViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKOverlayView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKOverlayView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKOverlayViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKOverlayViewAppearance Appearance {
                get;
        }
        
        public class MKOverlayViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPinAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPinAnnotationView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKPinAnnotationViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        
        public static MKPinAnnotationViewAppearance Appearance {
                get;
        }
        
        public class MKPinAnnotationViewAppearance : MKAnnotationViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPlacemark" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPlacemark

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

The body of MKPlacemarks are now in CLPlacemark.

Removed:

```
public class MKPlacemark : MKAnnotation {
        protected override void Dispose (bool disposing);
        
        public virtual MonoTouch.Foundation.NSDictionary AddressDictionary {
                get;
        }
        public virtual string AdministrativeArea {
                get;
        }
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
        public virtual string Country {
                get;
        }
        public virtual string Locality {
                get;
        }
        public virtual string PostalCode {
                get;
        }
        public virtual string SubAdministrativeArea {
                get;
        }
        public virtual string SubLocality {
                get;
        }
        public virtual string SubThoroughfare {
                get;
        }
        public override string Subtitle {
                get;
        }
        public virtual string Thoroughfare {
        public override string Title {
```

Added:

```
public class MKPlacemark : MonoTouch.CoreLocation.CLPlacemark {
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
        public virtual string Subtitle {
        public virtual string Title {
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygonView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygonView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKPolygonViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKPolygonViewAppearance Appearance {
                get;
        }
        
        public class MKPolygonViewAppearance : MKOverlayPathViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolylineView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolylineView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MKPolylineViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MKPolylineViewAppearance Appearance {
                get;
        }
        
        public class MKPolylineViewAppearance : MKOverlayPathViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKUserLocation" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKUserLocation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
public class MKUserLocation : MKAnnotation {
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                set;
                set;
```

Added:

```
public class MKUserLocation : MonoTouch.Foundation.NSObject {
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
        public virtual MonoTouch.CoreLocation.CLHeading Heading {
                get;
        }
```

 <a name="New_Type:_MonoTouch.MapKit.MKUserTrackingBarButtonItem" class="injected"></a>


## New Type: MonoTouch.MapKit.MKUserTrackingBarButtonItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class MKUserTrackingBarButtonItem : MonoTouch.UIKit.UIBarButtonItem {
        
        public MKUserTrackingBarButtonItem ();
        public MKUserTrackingBarButtonItem (MonoTouch.Foundation.NSCoder coder);
        public MKUserTrackingBarButtonItem (MonoTouch.Foundation.NSObjectFlag t);
        public MKUserTrackingBarButtonItem (IntPtr handle);
        public MKUserTrackingBarButtonItem (MKMapView mapView);
        
        public static MKUserTrackingBarButtonItemAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        
        public static MKUserTrackingBarButtonItemAppearance Appearance {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MKMapView MapView {
                get;
                set;
        }
        
        public class MKUserTrackingBarButtonItemAppearance : UIBarButtonItem.MonoTouch.UIKit.UIBarButtonItemAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKUserTrackingMode" class="injected"></a>


## New Type: MonoTouch.MapKit.MKUserTrackingMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum MKUserTrackingMode {
        None,
        Follow,
        FollowWithHeading
}
```

 <a name="New_Type:_MonoTouch.MapKit.MMapViewUserTrackingEventArgs" class="injected"></a>


## New Type: MonoTouch.MapKit.MMapViewUserTrackingEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class MMapViewUserTrackingEventArgs : EventArgs {
        
        public MMapViewUserTrackingEventArgs (MKUserTrackingMode mode, bool animated);
        
        public bool Animated {
                get;
                set;
        }
        public MKUserTrackingMode Mode {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemArtwork" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemArtwork

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public MPMediaItemArtwork (MonoTouch.UIKit.UIImage image);
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaType" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Removed:

```
MPMediaTypeAny
```

Added:

```
Music,
        Podcast,
        AudioBook,
        AnyAudio,
        Movie,
        TVShow,
        VideoPodcast,
        MusicVideo,
        VideoITunesU,
        TypeAnyVideo,
        Any
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPNowPlayingInfo" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPNowPlayingInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class MPNowPlayingInfo {
        
        public MPNowPlayingInfo ();
        
        public Nullable<double> ElapsedPlaybackTime;
        public Nullable<double> PlaybackRate;
        public Nullable<int> PlaybackQueueIndex;
        public Nullable<int> PlaybackQueueCount;
        public Nullable<int> ChapterNumber;
        public Nullable<int> ChapterCount;
        public Nullable<int> AlbumTrackCount;
        public Nullable<int> AlbumTrackNumber;
        public Nullable<int> DiscCount;
        public Nullable<int> DiscNumber;
        public Nullable<ulong> PersistentID;
        public Nullable<double> PlaybackDuration;
        public string AlbumTitle;
        public string Artist;
        public MPMediaItemArtwork Artwork;
        public string Composer;
        public string Genre;
        public string Title;
}
</double></ulong></int></int></int></int></int></int></int></int></double></double>
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPNowPlayingInfoCenter" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPNowPlayingInfoCenter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class MPNowPlayingInfoCenter : MonoTouch.Foundation.NSObject {
        
        public MPNowPlayingInfoCenter ();
        public MPNowPlayingInfoCenter (MonoTouch.Foundation.NSCoder coder);
        public MPNowPlayingInfoCenter (MonoTouch.Foundation.NSObjectFlag t);
        public MPNowPlayingInfoCenter (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public static MPNowPlayingInfoCenter DefaultCenter {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public MPNowPlayingInfo NowPlaying {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPVolumeView" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPVolumeView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MPVolumeViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MPVolumeViewAppearance Appearance {
                get;
        }
        
        public class MPVolumeViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString TextMessageAvailabilityDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextMessageAvailabilityKey {
                get;
        }
```

 <a name="Namespace:_MonoTouch.NewsstandKit" class="injected"></a>


# Namespace: MonoTouch.NewsstandKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.NewsstandKit.NKAssetDownload" class="injected"></a>


## New Type: MonoTouch.NewsstandKit.NKAssetDownload

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NKAssetDownload : MonoTouch.Foundation.NSObject {
        
        public NKAssetDownload ();
        public NKAssetDownload (MonoTouch.Foundation.NSCoder coder);
        public NKAssetDownload (MonoTouch.Foundation.NSObjectFlag t);
        public NKAssetDownload (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSUrlConnection DownloadWithDelegate (MonoTouch.Foundation.NSUrlConnectionDownloadDelegate downloadDelegate);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Identifier {
                get;
        }
        public virtual NKIssue Issue {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrlRequest UrlRequest {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.NewsstandKit.NKIssue" class="injected"></a>


## New Type: MonoTouch.NewsstandKit.NKIssue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NKIssue : MonoTouch.Foundation.NSObject {
        
        public NKIssue ();
        public NKIssue (MonoTouch.Foundation.NSCoder coder);
        public NKIssue (MonoTouch.Foundation.NSObjectFlag t);
        public NKIssue (IntPtr handle);
        
        public virtual NKAssetDownload AddAsset (MonoTouch.Foundation.NSUrlRequest request);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl ContentUrl {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate Date {
                get;
        }
        public virtual NKAssetDownload[] DownloadingAssets {
                get;
        }
        public virtual string Name {
                get;
        }
        public virtual NKIssueContentStatus Status {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.NewsstandKit.NKIssueContentStatus" class="injected"></a>


## New Type: MonoTouch.NewsstandKit.NKIssueContentStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum NKIssueContentStatus {
        None,
        Downloading,
        Available
}
```

 <a name="New_Type:_MonoTouch.NewsstandKit.NKLibrary" class="injected"></a>


## New Type: MonoTouch.NewsstandKit.NKLibrary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class NKLibrary : MonoTouch.Foundation.NSObject {
        
        public NKLibrary ();
        public NKLibrary (MonoTouch.Foundation.NSCoder coder);
        public NKLibrary (MonoTouch.Foundation.NSObjectFlag t);
        public NKLibrary (IntPtr handle);
        
        public virtual NKIssue AddIssue (string name, MonoTouch.Foundation.NSDate date);
        protected override void Dispose (bool disposing);
        public virtual NKIssue GetIssue (string name);
        public virtual void RemoveIssue (NKIssue issue);
        
        public static NKLibrary SharedLibrary {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NKIssue CurrentlyReadingIssue {
                get;
                set;
        }
        public virtual NKAssetDownload[] DownloadingAssets {
                get;
        }
        public virtual NKIssue[] Issues {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.ObjCRuntime.AdoptsAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.AdoptsAttribute

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class AdoptsAttribute : Attribute {
        
        public AdoptsAttribute (string protocolType);
        
        public IntPtr ProtocolHandle {
                get;
        }
        public string ProtocolType {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.LionAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.LionAttribute

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class LionAttribute : Attribute {
        
        public LionAttribute ();
}
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static bool bool_objc_msgSend_bool_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static bool bool_objc_msgSend_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
        public static bool bool_objc_msgSend_IntPtr_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2);
        public static bool bool_objc_msgSend_IntPtr_CMTimeRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2, IntPtr arg3);
        public static bool bool_objc_msgSend_IntPtr_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, IntPtr arg4);
        public static bool bool_objc_msgSend_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
        public static bool bool_objc_msgSend_IntPtr_IntPtr_CMTime_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
        public static bool bool_objc_msgSend_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
        public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5);
        public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
        public static bool bool_objc_msgSendSuper_bool_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
        public static bool bool_objc_msgSendSuper_IntPtr_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2);
        public static bool bool_objc_msgSendSuper_IntPtr_CMTimeRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2, IntPtr arg3);
        public static bool bool_objc_msgSendSuper_IntPtr_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, IntPtr arg4);
        public static bool bool_objc_msgSendSuper_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3);
        public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_CMTime_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
        public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
        public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5);
        public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
        public static void CMCalibratedMagneticField_objc_msgSend_stret (out MonoTouch.CoreMotion.CMCalibratedMagneticField retval, IntPtr receiver, IntPtr selector);
        public static void CMCalibratedMagneticField_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMCalibratedMagneticField retval, IntPtr receiver, IntPtr selector);
        public static void CMMagneticField_objc_msgSend_stret (out MonoTouch.CoreMotion.CMMagneticField retval, IntPtr receiver, IntPtr selector);
        public static void CMMagneticField_objc_msgSendSuper_stret (out MonoTouch.CoreMotion.CMMagneticField retval, IntPtr receiver, IntPtr selector);
        public static int int_objc_msgSend_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_CMTime_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, IntPtr arg3);
        public static IntPtr IntPtr_objc_msgSend_float_float_float (IntPtr receiver, IntPtr selector, float arg1, float arg2, float arg3);
        public static IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSend_int_SizeF_bool_IntPtr (IntPtr receiver, IntPtr selector, int arg1, System.Drawing.SizeF arg2, bool arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_int_UInt32 (IntPtr receiver, IntPtr selector, int arg1, uint arg2);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_int_SizeF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, System.Drawing.SizeF arg3, int arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_UInt64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ulong arg3);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, int arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_UIEdgeInsets_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIEdgeInsets arg2, double arg3);
        public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSend_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
        public static IntPtr IntPtr_objc_msgSend_UInt32_int (IntPtr receiver, IntPtr selector, uint arg1, int arg2);
        public static IntPtr IntPtr_objc_msgSend_UInt32_UInt32 (IntPtr receiver, IntPtr selector, uint arg1, uint arg2);
        public static IntPtr IntPtr_objc_msgSend_UInt32_UInt32_int (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, int arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_CMTime_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, IntPtr arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_float_float_float (IntPtr receiver, IntPtr selector, float arg1, float arg2, float arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSendSuper_int_SizeF_bool_IntPtr (IntPtr receiver, IntPtr selector, int arg1, System.Drawing.SizeF arg2, bool arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSendSuper_int_UInt32 (IntPtr receiver, IntPtr selector, int arg1, uint arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, int arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_SizeF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, System.Drawing.SizeF arg3, int arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_UInt64 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ulong arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, int arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIEdgeInsets_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIEdgeInsets arg2, double arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, IntPtr arg4, IntPtr arg5);
        public static IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_UInt32_int (IntPtr receiver, IntPtr selector, uint arg1, int arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_UInt32_UInt32 (IntPtr receiver, IntPtr selector, uint arg1, uint arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_UInt32_UInt32_int (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, int arg3);
        public static void Matrix3_objc_msgSend_stret (out OpenTK.Matrix3 retval, IntPtr receiver, IntPtr selector);
        public static void Matrix3_objc_msgSendSuper_stret (out OpenTK.Matrix3 retval, IntPtr receiver, IntPtr selector);
        public static void Matrix4_objc_msgSend_stret (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector);
        public static void Matrix4_objc_msgSendSuper_stret (out OpenTK.Matrix4 retval, IntPtr receiver, IntPtr selector);
        public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1);
        public static void NSRange_objc_msgSend_stret_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1);
        public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_NSRange (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1);
        public static void NSRange_objc_msgSendSuper_stret_NSRange (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSend (IntPtr receiver, IntPtr selector);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSend_int (IntPtr receiver, IntPtr selector, int arg1);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSend_int_int (IntPtr receiver, IntPtr selector, int arg1, int arg2);
        public static void UIOffset_objc_msgSend_stret (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector);
        public static void UIOffset_objc_msgSend_stret_int (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, int arg1);
        public static void UIOffset_objc_msgSend_stret_int_int (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, int arg1, int arg2);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSendSuper_int (IntPtr receiver, IntPtr selector, int arg1);
        public static MonoTouch.UIKit.UIOffset UIOffset_objc_msgSendSuper_int_int (IntPtr receiver, IntPtr selector, int arg1, int arg2);
        public static void UIOffset_objc_msgSendSuper_stret (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector);
        public static void UIOffset_objc_msgSendSuper_stret_int (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, int arg1);
        public static void UIOffset_objc_msgSendSuper_stret_int_int (out MonoTouch.UIKit.UIOffset retval, IntPtr receiver, IntPtr selector, int arg1, int arg2);
        public static void Vector3_objc_msgSend_stret (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector);
        public static void Vector3_objc_msgSendSuper_stret (out OpenTK.Vector3 retval, IntPtr receiver, IntPtr selector);
        public static void Vector4_objc_msgSend_stret (out OpenTK.Vector4 retval, IntPtr receiver, IntPtr selector);
        public static void Vector4_objc_msgSendSuper_stret (out OpenTK.Vector4 retval, IntPtr receiver, IntPtr selector);
        public static void void_objc_msgSend_CMTime_CMTime_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
        public static void void_objc_msgSend_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2);
        public static void void_objc_msgSend_int_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static void void_objc_msgSend_IntPtr_bool_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, bool arg4);
        public static void void_objc_msgSend_IntPtr_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, IntPtr arg4);
        public static void void_objc_msgSend_IntPtr_int_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, int arg4, IntPtr arg5, IntPtr arg6);
        public static void void_objc_msgSend_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, IntPtr arg4);
        public static void void_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
        public static void void_objc_msgSend_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, long arg3);
        public static void void_objc_msgSend_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, long arg3, long arg4);
        public static void void_objc_msgSend_IntPtr_IntPtr_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5, IntPtr arg6);
        public static void void_objc_msgSend_IntPtr_IntPtr_int_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, System.Drawing.RectangleF arg4, int arg5, IntPtr arg6);
        public static void void_objc_msgSend_IntPtr_IntPtr_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.RectangleF arg3, IntPtr arg4);
        public static void void_objc_msgSend_IntPtr_PointF_out_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, out System.Drawing.PointF arg3);
        public static void void_objc_msgSend_IntPtr_PointF_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.RectangleF arg3);
        public static void void_objc_msgSend_IntPtr_RectangleF_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, System.Drawing.RectangleF arg3);
        public static void void_objc_msgSend_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3);
        public static void void_objc_msgSend_IntPtr_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3);
        public static void void_objc_msgSend_IntPtr_UInt32_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, int arg4);
        public static void void_objc_msgSend_IntPtr_UInt64 (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2);
        public static void void_objc_msgSend_Matrix3 (IntPtr receiver, IntPtr selector, OpenTK.Matrix3 arg1);
        public static void void_objc_msgSend_Matrix4 (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1);
        public static void void_objc_msgSend_NSRange_int (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2);
        public static void void_objc_msgSend_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, IntPtr arg3);
        public static void void_objc_msgSend_NSRange_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSend_UInt64 (IntPtr receiver, IntPtr selector, ulong arg1);
        public static void void_objc_msgSend_UIOffset (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1);
        public static void void_objc_msgSend_UIOffset_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, int arg2);
        public static void void_objc_msgSend_UIOffset_int_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, int arg2, int arg3);
        public static void void_objc_msgSend_Vector3 (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
        public static void void_objc_msgSend_Vector4 (IntPtr receiver, IntPtr selector, OpenTK.Vector4 arg1);
        public static void void_objc_msgSendSuper_CMTime_CMTime_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_CMTime_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, IntPtr arg2);
        public static void void_objc_msgSendSuper_int_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_IntPtr_bool_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, bool arg4);
        public static void void_objc_msgSendSuper_IntPtr_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, int arg4, IntPtr arg5, IntPtr arg6);
        public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
        public static void void_objc_msgSendSuper_IntPtr_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, long arg3);
        public static void void_objc_msgSendSuper_IntPtr_Int64_Int64_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, long arg3, long arg4);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, int arg4, IntPtr arg5, IntPtr arg6);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_int_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, System.Drawing.RectangleF arg4, int arg5, IntPtr arg6);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.RectangleF arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_IntPtr_PointF_out_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, out System.Drawing.PointF arg3);
        public static void void_objc_msgSendSuper_IntPtr_PointF_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.RectangleF arg3);
        public static void void_objc_msgSendSuper_IntPtr_RectangleF_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, System.Drawing.RectangleF arg3);
        public static void void_objc_msgSendSuper_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3);
        public static void void_objc_msgSendSuper_IntPtr_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3);
        public static void void_objc_msgSendSuper_IntPtr_UInt32_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, int arg4);
        public static void void_objc_msgSendSuper_IntPtr_UInt64 (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2);
        public static void void_objc_msgSendSuper_Matrix3 (IntPtr receiver, IntPtr selector, OpenTK.Matrix3 arg1);
        public static void void_objc_msgSendSuper_Matrix4 (IntPtr receiver, IntPtr selector, OpenTK.Matrix4 arg1);
        public static void void_objc_msgSendSuper_NSRange_int (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2);
        public static void void_objc_msgSendSuper_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, int arg2, IntPtr arg3);
        public static void void_objc_msgSendSuper_NSRange_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_UInt64 (IntPtr receiver, IntPtr selector, ulong arg1);
        public static void void_objc_msgSendSuper_UIOffset (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1);
        public static void void_objc_msgSendSuper_UIOffset_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, int arg2);
        public static void void_objc_msgSendSuper_UIOffset_int_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIOffset arg1, int arg2, int arg3);
        public static void void_objc_msgSendSuper_Vector3 (IntPtr receiver, IntPtr selector, OpenTK.Vector3 arg1);
        public static void void_objc_msgSendSuper_Vector4 (IntPtr receiver, IntPtr selector, OpenTK.Vector4 arg1);
```

 <a name="Namespace:_MonoTouch.Twitter" class="injected"></a>


# Namespace: MonoTouch.Twitter

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="New_Type:_MonoTouch.Twitter.TWRequest" class="injected"></a>


## New Type: MonoTouch.Twitter.TWRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class TWRequest : MonoTouch.Foundation.NSObject {
        
        public TWRequest ();
        public TWRequest (MonoTouch.Foundation.NSCoder coder);
        public TWRequest (MonoTouch.Foundation.NSObjectFlag t);
        public TWRequest (IntPtr handle);
        public TWRequest (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters, TWRequestMethod requestMethod);
        
        public virtual void AddMultiPartData (MonoTouch.Foundation.NSData data, string name, string type);
        protected override void Dispose (bool disposing);
        public virtual void PerformRequest (TWRequestHandler handler);
        
        public virtual MonoTouch.Accounts.ACAccount Account {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary Parameters {
                get;
        }
        public virtual TWRequestMethod RequestMethod {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrlRequest SignedUrlRequest {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Twitter.TWRequestHandler" class="injected"></a>


## New Type: MonoTouch.Twitter.TWRequestHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void TWRequestHandler (MonoTouch.Foundation.NSData responseData, MonoTouch.Foundation.NSHttpUrlResponse urlResponse, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.Twitter.TWRequestMethod" class="injected"></a>


## New Type: MonoTouch.Twitter.TWRequestMethod

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum TWRequestMethod {
        Get,
        Post,
        Delete
}
```

 <a name="New_Type:_MonoTouch.Twitter.TWTweetComposeHandler" class="injected"></a>


## New Type: MonoTouch.Twitter.TWTweetComposeHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void TWTweetComposeHandler (TWTweetComposeViewControllerResult result);
```

 <a name="New_Type:_MonoTouch.Twitter.TWTweetComposeViewController" class="injected"></a>


## New Type: MonoTouch.Twitter.TWTweetComposeViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class TWTweetComposeViewController : MonoTouch.UIKit.UIViewController {
        
        public TWTweetComposeViewController ();
        public TWTweetComposeViewController (MonoTouch.Foundation.NSCoder coder);
        public TWTweetComposeViewController (MonoTouch.Foundation.NSObjectFlag t);
        public TWTweetComposeViewController (IntPtr handle);
        
        public virtual bool AddImage (MonoTouch.UIKit.UIImage image);
        public virtual bool AddUrl (MonoTouch.Foundation.NSUrl url);
        public virtual bool RemoveAllImages ();
        public virtual bool RemoveAllUrls ();
        public virtual void SetCompletionHandler (TWTweetComposeHandler handler);
        public virtual bool SetInitialText (string text);
        
        public static bool CanSendTweet {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Twitter.TWTweetComposeViewControllerResult" class="injected"></a>


## New Type: MonoTouch.Twitter.TWTweetComposeViewControllerResult

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum TWTweetComposeViewControllerResult {
        Cancelled,
        Done
}
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIActionSheet" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIActionSheet

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIActionSheetAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIActionSheetAppearance Appearance {
                get;
        }
        
        public class UIActionSheetAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIActivityIndicatorView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIActivityIndicatorViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        public static UIActivityIndicatorViewAppearance Appearance {
                get;
        }
        public virtual UIColor Color {
                get;
                set;
        }
        
        public class UIActivityIndicatorViewAppearance : UIViewAppearance {
                
                public virtual UIColor Color {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIAlertViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UITextField GetTextField (int textFieldIndex);
        public static UIAlertViewAppearance Appearance {
                get;
        }
        public virtual UIAlertViewStyle AlertViewStyle {
                get;
                set;
        }
        public UIAlertViewPredicate ShouldEnableFirstOtherButton {
                get;
                set;
        }
        
        public class UIAlertViewAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool ShouldEnableFirstOtherButton (UIAlertView alertView);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertViewPredicate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertViewPredicate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public delegate bool UIAlertViewPredicate (UIAlertView alertView);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIAlertViewStyle" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAlertViewStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum UIAlertViewStyle {
        Default,
        SecureTextInput,
        PlainTextInput,
        LoginAndPasswordInput
 }
```

 <a name="New_Type:_MonoTouch.UIKit.UIAppearance" class="injected"></a>


## New Type: MonoTouch.UIKit.UIAppearance

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIAppearance : MonoTouch.Foundation.NSObject {
        
        public UIAppearance ();
        public UIAppearance (MonoTouch.Foundation.NSCoder coder);
        public UIAppearance (MonoTouch.Foundation.NSObjectFlag t);
        public UIAppearance (IntPtr handle);
        
        public static IntPtr GetAppearance (IntPtr class_ptr, params Type [] whenFoundIn);
        public override bool Equals (object other);
        public override int GetHashCode ();
        
        public static bool operator == (UIAppearance a, UIAppearance b);
        public static bool operator != (UIAppearance a, UIAppearance b);
        
        public override IntPtr ClassHandle {
                get;
        }
        
        public static IntPtr SelectorAppearance;
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void SetNewsstandIconImage (UIImage image);
        public static MonoTouch.Foundation.NSString LaunchOptionsNewsstandDownloadsKey {
                get;
        }
        public virtual UIUserInterfaceLayoutDirection UserInterfaceLayoutDirection {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
protected override void Dispose (bool disposing);
        
        public virtual UIWindow Window {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBarButtonItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public UIBarButtonItem (UIImage image, UIImage landscapeImagePhone, UIBarButtonItemStyle style, MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
        public static UIBarButtonItemAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UIImage GetBackButtonBackgroundImage (UIControlState forState, UIBarMetrics barMetrics);
        public virtual float GetBackButtonBackgroundVerticalPositionAdjustment (UIBarMetrics barMetrics);
        public virtual UIOffset GetBackButtonTitlePositionAdjustment (UIBarMetrics barMetrics);
        public virtual UIImage GetBackgroundImage (UIControlState state, UIBarMetrics barMetrics);
        public virtual float GetBackgroundVerticalPositionAdjustment (UIBarMetrics forBarMetrics);
        public virtual UIOffset GetTitlePositionAdjustment (UIBarMetrics barMetrics);
        public virtual void SetBackButtonBackgroundImage (UIImage backgroundImage, UIControlState forState, UIBarMetrics barMetrics);
        public virtual void SetBackButtonBackgroundVerticalPositionAdjustment (float adjustment, UIBarMetrics barMetrics);
        public virtual void SetBackButtonTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);
        public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarMetrics barMetrics);
        public virtual void SetBackgroundVerticalPositionAdjustment (float adjustment, UIBarMetrics forBarMetrics);
        public virtual void SetTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);
        public static UIBarButtonItemAppearance Appearance {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet PossibleTitles {
                get;
        }
        public virtual UIColor TintColor {
                get;
                set;
        }
        
        public class UIBarButtonItemAppearance : UIBarItemAppearance {
                
                public virtual UIImage GetBackButtonBackgroundImage (UIControlState forState, UIBarMetrics barMetrics);
                public virtual float GetBackButtonBackgroundVerticalPositionAdjustment (UIBarMetrics barMetrics);
                public virtual UIOffset GetBackButtonTitlePositionAdjustment (UIBarMetrics barMetrics);
                public virtual UIImage GetBackgroundImage (UIControlState state, UIBarMetrics barMetrics);
                public virtual float GetBackgroundVerticalPositionAdjustment (UIBarMetrics forBarMetrics);
                public virtual UIOffset GetTitlePositionAdjustment (UIBarMetrics barMetrics);
                public virtual void SetBackButtonBackgroundImage (UIImage backgroundImage, UIControlState forState, UIBarMetrics barMetrics);
                public virtual void SetBackButtonBackgroundVerticalPositionAdjustment (float adjustment, UIBarMetrics barMetrics);
                public virtual void SetBackButtonTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);
                public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarMetrics barMetrics);
                public virtual void SetBackgroundVerticalPositionAdjustment (float adjustment, UIBarMetrics forBarMetrics);
                public virtual void SetTitlePositionAdjustment (UIOffset adjustment, UIBarMetrics barMetrics);
                
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBarItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIBarItemAppearance AppearanceWhenContainedIn (params Type [] containers);
        public UITextAttributes GetTitleTextAttributes (UIControlState state);
        public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);
        public static UIBarItemAppearance Appearance {
                get;
        }
        public virtual UIImage LandscapeImagePhone {
                get;
                set;
        }
        public virtual UIEdgeInsets LandscapeImagePhoneInsets {
                get;
                set;
        }
        
        public class UIBarItemAppearance : UIAppearance {
                
                public virtual UITextAttributes GetTitleTextAttributes (UIControlState state);
                public virtual void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIBarMetrics" class="injected"></a>


## New Type: MonoTouch.UIKit.UIBarMetrics

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIBarMetrics {
        Default,
        LandscapePhone
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBezierPath

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIBezierPathAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIBezierPathAppearance Appearance {
                get;
        }
        
        public class UIBezierPathAppearance : UIControlAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIButtonAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIButtonAppearance Appearance {
                get;
        }
        public virtual UIColor TintColor {
                get;
                set;
        }
        
        public class UIButtonAppearance : UIControlAppearance {
                
                public virtual UIImage ImageForState (UIControlState state);
                public virtual void SetBackgroundImage (UIImage image, UIControlState forState);
                public virtual void SetImage (UIImage image, UIControlState forState);
                public virtual void SetTitleColor (UIColor color, UIControlState forState);
                public virtual void SetTitleShadowColor (UIColor color, UIControlState forState);
                public virtual UIColor TitleColor (UIControlState state);
                public virtual UIColor TitleShadowColor (UIControlState state);
                
                public virtual UIImage CurrentBackgroundImage {
                        get;
                }
                public virtual UIImage CurrentImage {
                        get;
                }
                public virtual UIColor CurrentTitleColor {
                        get;
                }
                public virtual UIColor CurrentTitleShadowColor {
                        get;
                }
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIColor" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIColor

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public UIColor (MonoTouch.CoreImage.CIColor ciColor);
        public static UIColor FromCIColor (MonoTouch.CoreImage.CIColor color);
        public static UIColor UnderPageBackgroundColor {
                get;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UICompletionHandler" class="injected"></a>


## New Type: MonoTouch.UIKit.UICompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void UICompletionHandler (bool finished);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIControl" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIControl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIControlAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIControlAppearance Appearance {
                get;
        }
        
        public class UIControlAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDatePicker" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDatePicker

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIDatePickerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIDatePickerAppearance Appearance {
                get;
        }
        
        public class UIDatePickerAppearance : UIControlAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public bool CheckSystemVersion (int major, int minor);
```

 <a name="New_Type:_MonoTouch.UIKit.UIDocument" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDocument

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIDocument : MonoTouch.Foundation.NSObject {
        
        public UIDocument ();
        public UIDocument (MonoTouch.Foundation.NSCoder coder);
        public UIDocument (MonoTouch.Foundation.NSObjectFlag t);
        public UIDocument (IntPtr handle);
        public UIDocument (MonoTouch.Foundation.NSUrl url);
        
        public virtual void AutoSave (UIOperationHandler completionHandler);
        public virtual MonoTouch.Foundation.NSObject ChangeCountTokenForSaveOperation (UIDocumentSaveOperation saveOperation);
        public virtual void Close (UIOperationHandler completionHandler);
        public virtual MonoTouch.Foundation.NSObject ContentsForType (string typeName, out MonoTouch.Foundation.NSError outError);
        public virtual void DisableEditing ();
        protected override void Dispose (bool disposing);
        public virtual void EnableEditing ();
        public virtual void FinishedHandlingError (MonoTouch.Foundation.NSError error, bool recovered);
        public virtual MonoTouch.Foundation.NSDictionary GetFileAttributesToWrite (MonoTouch.Foundation.NSUrl forUrl, UIDocumentSaveOperation saveOperation, out MonoTouch.Foundation.NSError outError);
        public virtual string GetFileNameExtension (string typeName, UIDocumentSaveOperation saveOperation);
        public virtual void HandleError (MonoTouch.Foundation.NSError error, bool userInteractionPermitted);
        public virtual bool LoadFromContents (MonoTouch.Foundation.NSObject contents, string typeName, out MonoTouch.Foundation.NSError outError);
        public virtual void Open (UIOperationHandler completionHandler);
        public virtual void PerformAsynchronousFileAccess (MonoTouch.Foundation.NSAction action);
        public virtual bool Read (MonoTouch.Foundation.NSUrl fromUrl, out MonoTouch.Foundation.NSError outError);
        public virtual void RevertToContentsOfUrl (MonoTouch.Foundation.NSUrl url, UIOperationHandler completionHandler);
        public virtual void Save (MonoTouch.Foundation.NSUrl url, UIDocumentSaveOperation saveOperation, UIOperationHandler completionHandler);
        public virtual void UpdateChangeCount (MonoTouch.Foundation.NSObject changeCountToken, UIDocumentSaveOperation saveOperation);
        public virtual void UpdateChangeCount (UIDocumentChangeKind change);
        public virtual void UserInteractionNoLongerPermittedForError (MonoTouch.Foundation.NSError error);
        public virtual bool WriteContents (MonoTouch.Foundation.NSObject contents, MonoTouch.Foundation.NSDictionary additionalFileAttributes, MonoTouch.Foundation.NSUrl url, UIDocumentSaveOperation saveOperation, out MonoTouch.Foundation.NSError outError);
        public virtual bool WriteContents (MonoTouch.Foundation.NSObject contents, MonoTouch.Foundation.NSUrl toUrl, UIDocumentSaveOperation saveOperation, MonoTouch.Foundation.NSUrl originalContentsURL, out MonoTouch.Foundation.NSError outError);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIDocumentState DocumentState {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate FileModificationDate {
                get;
                set;
        }
        public virtual string FileType {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl FileUrl {
                get;
        }
        public virtual bool HasUnsavedChanges {
                get;
        }
        public virtual string LocalizedName {
                get;
        }
        public virtual string SavingFileType {
                get;
        }
        public virtual MonoTouch.Foundation.NSUndoManager UndoManager {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIDocumentChangeKind" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDocumentChangeKind

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIDocumentChangeKind {
        Done,
        Undone,
        Redone,
        Cleared
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIDocumentSaveOperation" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDocumentSaveOperation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIDocumentSaveOperation {
        ForCreating,
        ForOverwriting
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIDocumentState" class="injected"></a>


## New Type: MonoTouch.UIKit.UIDocumentState

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
[Flags]
public enum UIDocumentState {
        Normal,
        Closed,
        InConflict,
        SavingError,
        EditingDisabled
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIEdgeInsets" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIEdgeInsets

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static readonly UIEdgeInsets Zero;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImage" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public UIImage (MonoTouch.CoreGraphics.CGImage cgImage);
        public UIImage (MonoTouch.CoreImage.CIImage ciImage);
        public UIImage (MonoTouch.CoreGraphics.CGImage cgImage, float scale, UIImageOrientation orientation);
        public UIImage (UIImage image);
        public UIImage (UIImage image, MonoTouch.Foundation.NSDictionary options);
        public static UIImage CreateAnimatedImage (string name, double duration);
        public static UIImage CreateAnimatedImage (UIImage[] images, double duration);
        public static UIImage CreateAnimatedImage (UIImage[] images, UIEdgeInsets capInsets, double duration);
        public virtual UIImage CreateResizableImage (UIEdgeInsets capInsets);
        protected override void Dispose (bool disposing);
        public virtual UIEdgeInsets CapInsets {
                get;
        }
        public virtual MonoTouch.CoreImage.CIImage CIImage {
                get;
        }
        public virtual double Duration {
                get;
        }
        public virtual UIImage[] Images {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerQualityType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerQualityType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
At1280x720,
        At960x540
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImageView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImageView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIImageViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIImageViewAppearance Appearance {
                get;
        }
        
        public class UIImageViewAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboardType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboardType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
Twitter
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILabel" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILabel

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UILabelAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UILabelAppearance Appearance {
                get;
        }
        
        public class UILabelAppearance : UIViewAppearance {
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIManagedDocument" class="injected"></a>


## New Type: MonoTouch.UIKit.UIManagedDocument

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIManagedDocument : UIDocument {
        
        public UIManagedDocument ();
        public UIManagedDocument (MonoTouch.Foundation.NSCoder coder);
        public UIManagedDocument (MonoTouch.Foundation.NSObjectFlag t);
        public UIManagedDocument (IntPtr handle);
        
        public virtual MonoTouch.Foundation.NSObject AdditionalContent (MonoTouch.Foundation.NSUrl absoluteURL, out MonoTouch.Foundation.NSError error);
        public virtual bool ConfigurePersistentStoreCoordinator (MonoTouch.Foundation.NSUrl storeURL, string fileType, string configuration, MonoTouch.Foundation.NSDictionary storeOptions, MonoTouch.Foundation.NSError error);
        protected override void Dispose (bool disposing);
        public virtual string GetPersistentStoreType (string fileType);
        public virtual bool ReadAdditionalContent (MonoTouch.Foundation.NSUrl absoluteURL, out MonoTouch.Foundation.NSError error);
        public virtual bool WriteAdditionalContent (MonoTouch.Foundation.NSObject content, MonoTouch.Foundation.NSUrl absoluteURL, MonoTouch.Foundation.NSUrl absoluteOriginalContentsURL, out MonoTouch.Foundation.NSError error);
        
        public static string PersistentStoreName {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreData.NSManagedObjectContext ManagedObjectContext {
                get;
        }
        public virtual MonoTouch.CoreData.NSManagedObjectModel ManagedObjectModel {
                get;
        }
        public virtual string ModelConfiguration {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary PersistentStoreOptions {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINavigationBar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UINavigationBarAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UIImage GetBackgroundImage (UIBarMetrics forBarMetrics);
        public UITextAttributes GetTitleTextAttributes ();
        public virtual float GetTitleVerticalPositionAdjustment (UIBarMetrics barMetrics);
        public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
        public void SetTitleTextAttributes (UITextAttributes attributes);
        public virtual void SetTitleVerticalPositionAdjustment (float adjustment, UIBarMetrics barMetrics);
        public static UINavigationBarAppearance Appearance {
                get;
        }
        
        public class UINavigationBarAppearance : UIViewAppearance {
                
                public virtual UIImage GetBackgroundImage (UIBarMetrics forBarMetrics);
                public virtual UITextAttributes GetTitleTextAttributes ();
                public virtual float GetTitleVerticalPositionAdjustment (UIBarMetrics barMetrics);
                public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
                public virtual void SetTitleTextAttributes (UITextAttributes attributes);
                public virtual void SetTitleVerticalPositionAdjustment (float adjustment, UIBarMetrics barMetrics);
                
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINavigationItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void SetLeftBarButtonItems (UIBarButtonItem[] items, bool animated);
        public virtual void SetRightBarButtonItems (UIBarButtonItem[] items, bool animated);
        public virtual UIBarButtonItem[] LeftBarButtonItems {
                get;
                set;
        }
        public virtual bool LeftItemsSupplementBackButton {
                get;
                set;
        }
        public virtual UIBarButtonItem[] RightBarButtonItems {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIOffset" class="injected"></a>


## New Type: MonoTouch.UIKit.UIOffset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public struct UIOffset {
        
        public UIOffset (float horizontal, float vertical);
        
        public override bool Equals (object obj);
        public override int GetHashCode ();
        
        public static bool operator == (UIOffset left, UIOffset right);
        public static bool operator != (UIOffset left, UIOffset right);
        
        public float Horizontal;
        public float Vertical;
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIOperationHandler" class="injected"></a>


## New Type: MonoTouch.UIKit.UIOperationHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate void UIOperationHandler (bool success);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageControl" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageControl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIPageControlAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIPageControlAppearance Appearance {
                get;
        }
        
        public class UIPageControlAppearance : UIControlAppearance {
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewController" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIPageViewController : UIViewController {
        
        public UIPageViewController (UIPageViewControllerTransitionStyle style, UIPageViewControllerNavigationOrientation navigationOrientation, UIPageViewControllerSpineLocation spineLocation);
        public UIPageViewController (UIPageViewControllerTransitionStyle style, UIPageViewControllerNavigationOrientation navigationOrientation);
        public UIPageViewController ();
        public UIPageViewController (MonoTouch.Foundation.NSCoder coder);
        public UIPageViewController (MonoTouch.Foundation.NSObjectFlag t);
        public UIPageViewController (IntPtr handle);
        public UIPageViewController (UIPageViewControllerTransitionStyle style, UIPageViewControllerNavigationOrientation navigationOrientation, MonoTouch.Foundation.NSDictionary options);
        
        protected override void Dispose (bool disposing);
        public virtual void SetViewControllers (UIViewController[] viewControllers, UIPageViewControllerNavigationDirection direction, bool animated, UICompletionHandler completionHandler);
        
        public static MonoTouch.Foundation.NSString OptionSpineLocationKey {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public UIPageViewControllerDataSource DataSource {
                get;
                set;
        }
        public UIPageViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual bool DoubleSided {
                get;
                set;
        }
        public virtual UIGestureRecognizer[] GestureRecognizers {
                get;
        }
        public UIPageViewGetViewController GetNextViewController {
                get;
                set;
        }
        public UIPageViewGetViewController GetPreviousViewController {
                get;
                set;
        }
        public UIPageViewSpineLocationCallback GetSpineLocation {
                get;
                set;
        }
        public virtual UIPageViewControllerNavigationOrientation NavigationOrientation {
                get;
        }
        public virtual UIPageViewControllerSpineLocation SpineLocation {
                get;
        }
        public virtual UIPageViewControllerTransitionStyle TransitionStyle {
                get;
        }
        public virtual UIViewController[] ViewControllers {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDataSource {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler<uipageviewfinishedanimationeventargs> DidFinishAnimating;
}
</uipageviewfinishedanimationeventargs>
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerDataSource" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerDataSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class UIPageViewControllerDataSource : MonoTouch.Foundation.NSObject {
        
        public UIPageViewControllerDataSource ();
        public UIPageViewControllerDataSource (MonoTouch.Foundation.NSCoder coder);
        public UIPageViewControllerDataSource (MonoTouch.Foundation.NSObjectFlag t);
        public UIPageViewControllerDataSource (IntPtr handle);
        
        public abstract UIViewController GetNextViewController (UIPageViewController pageViewController, UIViewController referenceViewController);
        public abstract UIViewController GetPreviousViewController (UIPageViewController pageViewController, UIViewController referenceViewController);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIPageViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public UIPageViewControllerDelegate ();
        public UIPageViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public UIPageViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public UIPageViewControllerDelegate (IntPtr handle);
        
        public virtual void DidFinishAnimating (UIPageViewController pageViewController, bool finished, UIViewController[] previousViewControllers, bool completed);
        public virtual UIPageViewControllerSpineLocation GetSpineLocation (UIPageViewController pageViewController, UIInterfaceOrientation orientation);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerNavigationDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerNavigationDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIPageViewControllerNavigationDirection {
        Forward,
        Reverse
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerNavigationOrientation" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerNavigationOrientation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIPageViewControllerNavigationOrientation {
        Horizontal,
        Vertical
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerSpineLocation" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerSpineLocation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIPageViewControllerSpineLocation {
        None,
        Min,
        Mid,
        Max
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerTransitionStyle" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerTransitionStyle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIPageViewControllerTransitionStyle {
        PageCurl
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewFinishedAnimationEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewFinishedAnimationEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIPageViewFinishedAnimationEventArgs : EventArgs {
        
        public UIPageViewFinishedAnimationEventArgs (bool finished, UIViewController[] previousViewControllers, bool completed);
        
        public bool Completed {
                get;
                set;
        }
        public bool Finished {
                get;
                set;
        }
        public UIViewController[] PreviousViewControllers {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewGetViewController" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewGetViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate UIViewController UIPageViewGetViewController (UIPageViewController pageViewController, UIViewController referenceViewController);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewSpineLocationCallback" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewSpineLocationCallback

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public delegate UIPageViewControllerSpineLocation UIPageViewSpineLocationCallback (UIPageViewController pageViewController, UIInterfaceOrientation orientation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIPickerViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIPickerViewAppearance Appearance {
                get;
        }
        
        public class UIPickerViewAppearance : UIViewAppearance {
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIPopoverBackgroundView" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPopoverBackgroundView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIPopoverBackgroundView : UIView {
        
        public UIPopoverBackgroundView ();
        public UIPopoverBackgroundView (MonoTouch.Foundation.NSCoder coder);
        public UIPopoverBackgroundView (MonoTouch.Foundation.NSObjectFlag t);
        public UIPopoverBackgroundView (IntPtr handle);
        public UIPopoverBackgroundView (System.Drawing.RectangleF frame);
        
        public static UIPopoverBackgroundViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static float GetArrowBase ();
        public static float GetArrowHeight ();
        public static UIEdgeInsets GetContentViewInsets ();
        
        public static UIPopoverBackgroundViewAppearance Appearance {
                get;
        }
        public virtual UIPopoverArrowDirection ArrowDirection {
                get;
                set;
        }
        public virtual float ArrowOffset {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        
        public class UIPopoverBackgroundViewAppearance : UIViewAppearance {
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIProgressView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIProgressView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIProgressViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        public virtual void SetProgress (float progress, bool animated);
        
        public static UIProgressViewAppearance Appearance {
                get;
        }
        public virtual UIImage ProgressImage {
                get;
                set;
        }
        public virtual UIColor ProgressTintColor {
                get;
                set;
        }
        public virtual UIImage TrackImage {
                get;
                set;
        }
        public virtual UIColor TrackTintColor {
                get;
                set;
        }
        
        public class UIProgressViewAppearance : UIViewAppearance {
                
                public virtual UIImage ProgressImage {
                        get;
                        set;
                }
                public virtual UIColor ProgressTintColor {
                        get;
                        set;
                }
                public virtual UIImage TrackImage {
                        get;
                        set;
                }
                public virtual UIColor TrackTintColor {
                        get;
                        set;
                }
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIReferenceLibraryViewController" class="injected"></a>


## New Type: MonoTouch.UIKit.UIReferenceLibraryViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIReferenceLibraryViewController : UIViewController {
        
        public UIReferenceLibraryViewController ();
        public UIReferenceLibraryViewController (MonoTouch.Foundation.NSCoder coder);
        public UIReferenceLibraryViewController (MonoTouch.Foundation.NSObjectFlag t);
        public UIReferenceLibraryViewController (IntPtr handle);
        public UIReferenceLibraryViewController (string term);
        
        public static bool DictionaryHasDefinitionForTerm (string term);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIRemoteNotificationType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIRemoteNotificationType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
NewsstandContentAvailability
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIResponder" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIResponder

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void Copy (MonoTouch.Foundation.NSObject sender);
        public virtual void Cut (MonoTouch.Foundation.NSObject sender);
        public virtual void Delete (MonoTouch.Foundation.NSObject sender);
        public virtual void Paste (MonoTouch.Foundation.NSObject sender);
        public virtual void Select (MonoTouch.Foundation.NSObject sender);
        public virtual void SelectAll (MonoTouch.Foundation.NSObject sender);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreen" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreen

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static MonoTouch.Foundation.NSString BrightnessDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidConnectNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidDisconnectNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeDidChangeNotification {
                get;
        }
        public virtual float Brightness {
                get;
                set;
        }
        public virtual UIScreenOverscanCompensation OverscanCompensation {
                get;
                set;
        }
        public virtual bool WantsSoftwareDimming {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreenOverscanCompensation" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreenOverscanCompensation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum UIScreenOverscanCompensation {
        Scale,
        InsetBounds,
        InsetApplicationFrame
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScrollView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScrollView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIScrollViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIScrollViewAppearance Appearance {
                get;
        }
        public virtual UIPanGestureRecognizer PanGestureRecognizer {
                get;
        }
        public virtual UIPinchGestureRecognizer PinchGestureRecognizer {
                get;
        }
        public event EventHandler<WillEndDraggingEventArgs> WillEndDragging;
        
        public class UIScrollViewAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScrollViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScrollViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UISearchBarAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UIImage GetImageForSearchBarIcon (UISearchBarIcon icon, UIControlState state);
        public virtual UIOffset GetPositionAdjustmentForSearchBarIcon (UISearchBarIcon icon);
        public virtual UIImage GetScopeBarButtonBackgroundImage (UIControlState state);
        public virtual UIImage GetScopeBarButtonDividerImage (UIControlState leftState, UIControlState rightState);
        public UITextAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);
        public virtual UIImage GetSearchFieldBackgroundImage (UIControlState state);
        public virtual void SetImageforSearchBarIcon (UIImage iconImage, UISearchBarIcon icon, UIControlState state);
        public virtual void SetPositionAdjustmentforSearchBarIcon (UIOffset adjustment, UISearchBarIcon icon);
        public virtual void SetScopeBarButtonBackgroundImage (UIImage backgroundImage, UIControlState state);
        public virtual void SetScopeBarButtonDividerImage (UIImage dividerImage, UIControlState leftState, UIControlState rightState);
        public void SetScopeBarButtonTitle (UITextAttributes attributes, UIControlState state);
        public virtual void SetSearchFieldBackgroundImage (UIImage backgroundImage, UIControlState state);
        public static UISearchBarAppearance Appearance {
                get;
        }
        public virtual UIImage BackgroundImage {
                get;
                set;
        }
        public virtual UIImage ScopeBarBackgroundImage {
                get;
                set;
        }
        public virtual UIOffset SearchFieldBackgroundPositionAdjustment {
                get;
                set;
        }
        public virtual UIOffset SearchTextPositionAdjustment {
                get;
                set;
        }
        
        public class UISearchBarAppearance : UIViewAppearance {
                
                public virtual UIImage GetImageForSearchBarIcon (UISearchBarIcon icon, UIControlState state);
                public virtual UIImage GetScopeBarButtonBackgroundImage (UIControlState state);
                public virtual UIImage GetScopeBarButtonDividerImage (UIControlState leftState, UIControlState rightState);
                public UITextAttributes GetScopeBarButtonTitleTextAttributes (UIControlState state);
                public virtual UIImage GetSearchFieldBackgroundImage (UIControlState state);
                public virtual void SetImageforSearchBarIcon (UIImage iconImage, UISearchBarIcon icon, UIControlState state);
                public virtual void SetScopeBarButtonBackgroundImage (UIImage backgroundImage, UIControlState state);
                public virtual void SetScopeBarButtonDividerImage (UIImage dividerImage, UIControlState leftState, UIControlState rightState);
                public void SetScopeBarButtonTitle (UITextAttributes attributes, UIControlState state);
                public virtual void SetSearchFieldBackgroundImage (UIImage backgroundImage, UIControlState state);
                
                public virtual UIImage BackgroundImage {
                        get;
                        set;
                }
                public virtual UIImage ScopeBarBackgroundImage {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarIcon" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarIcon

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum UISearchBarIcon {
        Search,
        Clear,
        Bookmark,
        ResultsList
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchDisplayController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchDisplayController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual string SearchResultsTitle {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISegmentedControl" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISegmentedControl

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UISegmentedControlAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UIOffset ContentPositionAdjustment (UISegmentedControlSegment leftCenterRightOrAlone, UIBarMetrics barMetrics);
        public virtual UIImage DividerImageForLeftSegmentStaterightSegmentStatebarMetrics (UIControlState leftState, UIControlState rightState, UIBarMetrics barMetrics);
        public virtual UIImage GetBackgroundImage (UIControlState state, UIBarMetrics barMetrics);
        public UITextAttributes GetTitleTextAttributes (UIControlState state);
        public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarMetrics barMetrics);
        public virtual void SetContentPositionAdjustment (UIOffset adjustment, UISegmentedControlSegment leftCenterRightOrAlone, UIBarMetrics barMetrics);
        public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftSegmentState, UIControlState rightSegmentState, UIBarMetrics barMetrics);
        public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);
        public static UISegmentedControlAppearance Appearance {
                get;
        }
        public virtual bool ApportionsSegmentWidthsByContent {
                get;
                set;
        }
        
        public class UISegmentedControlAppearance : UIControlAppearance {
                
                public virtual UIOffset ContentPositionAdjustment (UISegmentedControlSegment leftCenterRightOrAlone, UIBarMetrics barMetrics);
                public virtual UIImage DividerImageForLeftSegmentStaterightSegmentStatebarMetrics (UIControlState leftState, UIControlState rightState, UIBarMetrics barMetrics);
                public virtual UIImage GetBackgroundImage (UIControlState state, UIBarMetrics barMetrics);
                public UITextAttributes GetTitleTextAttributes (UIControlState state);
                public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarMetrics barMetrics);
                public virtual void SetContentPositionAdjustment (UIOffset adjustment, UISegmentedControlSegment leftCenterRightOrAlone, UIBarMetrics barMetrics);
                public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftSegmentState, UIControlState rightSegmentState, UIBarMetrics barMetrics);
                public void SetTitleTextAttributes (UITextAttributes attributes, UIControlState state);
                
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISegmentedControlSegment" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISegmentedControlSegment

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum UISegmentedControlSegment {
        Any,
        Left,
        Center,
        Right,
        Alone
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISlider" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISlider

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UISliderAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UISliderAppearance Appearance {
                get;
        }
        public virtual UIColor MaximumTrackTintColor {
                get;
                set;
        }
        public virtual UIColor MinimumTrackTintColor {
                get;
                set;
        }
        public virtual UIColor ThumbTintColor {
                get;
                set;
        }
        
        public class UISliderAppearance : UIControlAppearance {
                
                public virtual UIColor MaximumTrackTintColor {
                        get;
                        set;
                }
                public virtual UIColor MinimumTrackTintColor {
                        get;
                        set;
                }
                public virtual UIColor ThumbTintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISplitViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISplitViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool ShouldHideViewController (UISplitViewController svc, UIViewController viewController, UIInterfaceOrientation inOrientation);
```

 <a name="New_Type:_MonoTouch.UIKit.UIStepper" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStepper

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIStepper : UIControl {
        
        public UIStepper ();
        public UIStepper (MonoTouch.Foundation.NSCoder coder);
        public UIStepper (MonoTouch.Foundation.NSObjectFlag t);
        public UIStepper (IntPtr handle);
        
        public static UIStepperAppearance AppearanceWhenContainedIn (params Type [] containers);
        
        public static UIStepperAppearance Appearance {
                get;
        }
        public virtual bool AutoRepeat {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Continuous {
                get;
                set;
        }
        public virtual double MaximumValue {
                get;
                set;
        }
        public virtual double MinimumValue {
                get;
                set;
        }
        public virtual double StepValue {
                get;
                set;
        }
        public virtual double Value {
                get;
                set;
        }
        public virtual bool Wraps {
                get;
                set;
        }
        
        public class UIStepperAppearance : UIControlAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStoryboard" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStoryboard

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIStoryboard : MonoTouch.Foundation.NSObject {
        
        public UIStoryboard ();
        public UIStoryboard (MonoTouch.Foundation.NSCoder coder);
        public UIStoryboard (MonoTouch.Foundation.NSObjectFlag t);
        public UIStoryboard (IntPtr handle);
        
        public static UIStoryboard FromName (string name, MonoTouch.Foundation.NSBundle storyboardBundleOrNil);
        public virtual MonoTouch.Foundation.NSObject InstantiateInitialViewController ();
        public virtual MonoTouch.Foundation.NSObject InstantiateViewController (string identifier);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStoryboardPopoverSegue" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStoryboardPopoverSegue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIStoryboardPopoverSegue : UIStoryboardSegue {
        
        public UIStoryboardPopoverSegue ();
        public UIStoryboardPopoverSegue (MonoTouch.Foundation.NSCoder coder);
        public UIStoryboardPopoverSegue (MonoTouch.Foundation.NSObjectFlag t);
        public UIStoryboardPopoverSegue (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIPopoverController PopoverController {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStoryboardSegue" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStoryboardSegue

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UIStoryboardSegue : MonoTouch.Foundation.NSObject {
        
        public UIStoryboardSegue ();
        public UIStoryboardSegue (MonoTouch.Foundation.NSCoder coder);
        public UIStoryboardSegue (MonoTouch.Foundation.NSObjectFlag t);
        public UIStoryboardSegue (IntPtr handle);
        public UIStoryboardSegue (string identifier, UIViewController source, UIViewController destination);
        
        protected override void Dispose (bool disposing);
        public virtual void Perform ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIViewController DestinationViewController {
                get;
        }
        public virtual string Identifier {
                get;
        }
        public virtual UIViewController SourceViewController {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwitch" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwitch

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UISwitchAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        public static UISwitchAppearance Appearance {
                get;
        }
        public virtual UIColor OnTintColor {
                get;
        }
        
        public class UISwitchAppearance : UIControlAppearance {
                
                public virtual UIColor OnTintColor {
                        get;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITabBarAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UITabBarAppearance Appearance {
                get;
        }
        public virtual UIImage BackgroundImage {
                get;
                set;
        }
        public virtual UIColor SelectedImageTintColor {
                get;
                set;
        }
        public virtual UIImage SelectionIndicatorImage {
                get;
                set;
        }
        public virtual UIColor TintColor {
                get;
                set;
        }
        
        public class UITabBarAppearance : UIViewAppearance {
                
                public virtual UIImage BackgroundImage {
                        get;
                        set;
                }
                public virtual UIColor SelectedImageTintColor {
                        get;
                        set;
                }
                public virtual UIImage SelectionIndicatorImage {
                        get;
                        set;
                }
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITabBarItemAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void SetFinishedImages (UIImage selectedImage, UIImage unselectedImage);
        public static UITabBarItemAppearance Appearance {
                get;
        }
        public virtual UIImage FinishedSelectedImage {
                get;
        }
        public virtual UIImage FinishedUnselectedImage {
                get;
        }
        public virtual UIOffset TitlePositionAdjustment {
                get;
                set;
        }
        
        public class UITabBarItemAppearance : UIBarItemAppearance {
                
                public virtual UIOffset TitlePositionAdjustment {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITableViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void MoveRow (MonoTouch.Foundation.NSIndexPath fromIndexPath, MonoTouch.Foundation.NSIndexPath toIndexPath);
        public virtual void MoveSection (int fromSection, int toSection);
        public virtual void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
        public static UITableViewAppearance Appearance {
                get;
        }
        public static float AutomaticDimension {
                get;
        }
        public virtual bool AllowsMultipleSelection {
                get;
                set;
        }
        public virtual bool AllowsMultipleSelectionDuringEditing {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSIndexPath[] IndexPathsForSelectedRows {
                get;
        }
        
        public class UITableViewAppearance : UIScrollViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewCell" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewCell

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITableViewCellAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UITableViewCellAppearance Appearance {
                get;
        }
        public virtual UIView MultipleSelectionBackgroundView {
                get;
                set;
        }
        
        public class UITableViewCellAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool CanPerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual void PerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual bool ShouldShowMenu (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowAtindexPath);
        public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewRowAnimation" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewRowAnimation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
Automatic
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewSource" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual bool CanPerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual void PerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual bool ShouldShowMenu (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowAtindexPath);
        public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
```

 <a name="New_Type:_MonoTouch.UIKit.UITextAttributes" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextAttributes

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UITextAttributes {
        
        public UITextAttributes ();
        
        public UIFont Font;
        public UIColor TextColor;
        public UIColor TextShadowColor;
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextDirection {
        Forward,
        Backward,
        Right,
        Left,
        Up,
        Down
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITextFieldAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UITextFieldAppearance Appearance {
                get;
        }
        public static MonoTouch.Foundation.NSString CurrentInputModeDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextBackgroundColorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TextColorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TextFontKey {
                get;
        }
        public virtual UITextPosition BeginningOfDocument {
                get;
        }
        public virtual UITextPosition EndOfDocument {
                get;
        }
        public virtual bool HasText {
                get;
        }
        public UITextInputDelegate InputDelegate {
                get;
                set;
        }
        public virtual UITextRange MarkedTextRange {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary MarkedTextStyle {
                get;
                set;
        }
        public virtual UITextRange SelectedTextRange {
                get;
                set;
        }
        public virtual UITextStorageDirection SelectionAffinity {
                get;
                set;
        }
        public virtual UITextSpellCheckingType SpellCheckingType {
                get;
        }
        public virtual UIView TextInputView {
                get;
        }
        public UITextInputTokenizer Tokenizer {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakInputDelegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakTokenizer {
                get;
        }
        
        public class UITextFieldAppearance : UIControlAppearance {
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UITextGranularity" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextGranularity

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextGranularity {
        Character,
        Word,
        Sentence,
        Paragraph,
        Line,
        Document
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextInputDelegate" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextInputDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class UITextInputDelegate : MonoTouch.Foundation.NSObject {
        
        public UITextInputDelegate ();
        public UITextInputDelegate (MonoTouch.Foundation.NSCoder coder);
        public UITextInputDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public UITextInputDelegate (IntPtr handle);
        
        public abstract void SelectionDidChange (MonoTouch.Foundation.NSObject uiTextInput);
        public abstract void SelectionWillChange (MonoTouch.Foundation.NSObject uiTextInput);
        public abstract void TextDidChange (MonoTouch.Foundation.NSObject textInput);
        public abstract void TextWillChange (MonoTouch.Foundation.NSObject textInput);
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextInputMode" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextInputMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITextInputMode[] ActiveInputModes {
                get;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UITextInputStringTokenizer" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextInputStringTokenizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UITextInputStringTokenizer : UITextInputTokenizer {
        
        public UITextInputStringTokenizer ();
        public UITextInputStringTokenizer (MonoTouch.Foundation.NSCoder coder);
        public UITextInputStringTokenizer (MonoTouch.Foundation.NSObjectFlag t);
        public UITextInputStringTokenizer (IntPtr handle);
        public UITextInputStringTokenizer (MonoTouch.Foundation.NSObject textInput);
        
        public override UITextPosition GetPosition (UITextPosition fromPosition, UITextGranularity toBoundary, UITextDirection inDirection);
        public override UITextRange GetRangeEnclosingPosition (UITextPosition position, UITextGranularity granularity, UITextDirection direction);
        public override bool ProbeDirection (UITextPosition probePosition, UITextGranularity atBoundary, UITextDirection inDirection);
        public override bool ProbeDirectionWithinTextUnit (UITextPosition probePosition, UITextGranularity withinTextUnit, UITextDirection inDirection);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextInputTokenizer" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextInputTokenizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public abstract class UITextInputTokenizer : MonoTouch.Foundation.NSObject {
        
        public UITextInputTokenizer ();
        public UITextInputTokenizer (MonoTouch.Foundation.NSCoder coder);
        public UITextInputTokenizer (MonoTouch.Foundation.NSObjectFlag t);
        public UITextInputTokenizer (IntPtr handle);
        
        public abstract UITextPosition GetPosition (UITextPosition fromPosition, UITextGranularity toBoundary, UITextDirection inDirection);
        public abstract UITextRange GetRangeEnclosingPosition (UITextPosition position, UITextGranularity granularity, UITextDirection direction);
        public abstract bool ProbeDirection (UITextPosition probePosition, UITextGranularity atBoundary, UITextDirection inDirection);
        public abstract bool ProbeDirectionWithinTextUnit (UITextPosition probePosition, UITextGranularity withinTextUnit, UITextDirection inDirection);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextLayoutDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextLayoutDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextLayoutDirection {
        Right,
        Left,
        Up,
        Down
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextPosition" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextPosition

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UITextPosition : MonoTouch.Foundation.NSObject {
        
        public UITextPosition ();
        public UITextPosition (MonoTouch.Foundation.NSCoder coder);
        public UITextPosition (MonoTouch.Foundation.NSObjectFlag t);
        public UITextPosition (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextRange" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextRange

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class UITextRange : MonoTouch.Foundation.NSObject {
        
        public UITextRange ();
        public UITextRange (MonoTouch.Foundation.NSCoder coder);
        public UITextRange (MonoTouch.Foundation.NSObjectFlag t);
        public UITextRange (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UITextPosition end {
                get;
        }
        public virtual bool IsEmpty {
                get;
        }
        public virtual UITextPosition start {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextSpellCheckingType" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextSpellCheckingType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextSpellCheckingType {
        Default,
        No,
        Yes
}
```

 <a name="New_Type:_MonoTouch.UIKit.UITextStorageDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextStorageDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextStorageDirection {
        Forward,
        Backward
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UITextViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UITextViewAppearance Appearance {
                get;
        }
        public static MonoTouch.Foundation.NSString CurrentInputModeDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString TextBackgroundColorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TextColorKey {
                get;
        }
        public static MonoTouch.Foundation.NSString TextFontKey {
                get;
        }
        public virtual UITextPosition BeginningOfDocument {
                get;
        }
        public virtual UITextPosition EndOfDocument {
                get;
        }
        public UITextInputDelegate InputDelegate {
                get;
                set;
        }
        public virtual UITextRange MarkedTextRange {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary MarkedTextStyle {
                get;
                set;
        }
        public virtual UITextRange SelectedTextRange {
                get;
                set;
        }
        public virtual UITextStorageDirection SelectionAffinity {
                get;
                set;
        }
        public virtual UITextSpellCheckingType SpellCheckingType {
                get;
        }
        public virtual UIView TextInputView {
                get;
        }
        public UITextInputTokenizer Tokenizer {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakInputDelegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakTokenizer {
                get;
        }
        public event EventHandler<WillEndDraggingEventArgs> WillEndDragging;
        
        public class UITextViewAppearance : UIScrollViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
```

 <a name="New_Type:_MonoTouch.UIKit.UITextWritingDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextWritingDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UITextWritingDirection {
        Natural,
        LeftToRight,
        RightToLeft
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIToolbar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIToolbar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIToolbarAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UIImage GetBackgroundImage (UIToolbarPosition position, UIBarMetrics barMetrics);
        public virtual void SetBackgroundImage (UIImage backgroundImage, UIToolbarPosition position, UIBarMetrics barMetrics);
        public static UIToolbarAppearance Appearance {
                get;
        }
        
        public class UIToolbarAppearance : UIViewAppearance {
                
                public virtual UIImage GetBackgroundImage (UIToolbarPosition position, UIBarMetrics barMetrics);
                public virtual void SetBackgroundImage (UIImage backgroundImage, UIToolbarPosition position, UIBarMetrics barMetrics);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIToolbarPosition" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIToolbarPosition

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
[Serializable]
 public enum UIToolbarPosition {
        Any,
        Bottom,
        Top
 }
```

 <a name="New_Type:_MonoTouch.UIKit.UIUserInterfaceLayoutDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UIUserInterfaceLayoutDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
[Serializable]
public enum UIUserInterfaceLayoutDirection {
        LeftToRight,
        RightToLeft
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIViewAppearance Appearance {
                get;
        }
        
        public class UIViewAppearance : UIAppearance {
                
                public virtual UIColor BackgroundColor {
                        get;
                        set;
                }
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewAnimationOptions" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewAnimationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
TransitionCrossDissolve,
        TransitionFlipFromTop,
        TransitionFlipFromBottom
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static void AttemptRotationToDeviceOrientation ();
        public virtual void AddChildViewController (UIViewController childController);
        public virtual void DidMoveToParentViewController (UIViewController parent);
        public virtual void DismissViewController (bool animated, MonoTouch.Foundation.NSAction completionHandler);
        public virtual void PerformSegue (string identifier, MonoTouch.Foundation.NSObject sender);
        public virtual void PrepareForSegue (UIStoryboardSegue segue, MonoTouch.Foundation.NSObject sender);
        public virtual void PresentViewController (UIViewController viewControllerToPresent, bool animated, MonoTouch.Foundation.NSAction completionHandler);
        public virtual void RemoveFromParentViewController ();
        public virtual void Transition (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completionHandler);
        public virtual void ViewDidLayoutSubviews ();
        public virtual void ViewWillLayoutSubviews ();
        public virtual void ViewWillUnload ();
        public virtual void WillMoveToParentViewController (UIViewController parent);
        public virtual bool AutomaticallyForwardAppearanceAndRotationMethodsToChildViewControllers {
                get;
        }
        public virtual UIViewController[] ChildViewControllers {
                get;
        }
        public virtual bool DefinesPresentationContext {
                get;
                set;
        }
        public virtual bool IsBeingDismissed {
                get;
        }
        public virtual bool IsBeingPresented {
                get;
        }
        public virtual bool IsMovingFromParentViewController {
                get;
        }
        public virtual bool IsMovingToParentViewController {
                get;
        }
        public virtual UIViewController PresentedViewController {
                get;
        }
        public virtual UIViewController PresentingViewController {
                get;
        }
        public virtual bool ProvidesPresentationContextTransitionStyle {
                get;
                set;
        }
        public virtual UIStoryboard Storyboard {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWebView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWebView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIWebViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIWebViewAppearance Appearance {
                get;
        }
        public virtual bool MediaPlaybackAllowsAirPlay {
                get;
                set;
        }
        public virtual UIScrollView ScrollView {
                get;
        }
        
        public class UIWebViewAppearance : UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static UIWindowAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static UIWindowAppearance Appearance {
                get;
        }
        public static MonoTouch.Foundation.NSString KeyboardDidChangeFrameNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString KeyboardWillChangeFrameNotification {
                get;
        }
        
        public class UIWindowAppearance : UIViewAppearance {
        }
```

 <a name="New_Type:_MonoTouch.UIKit.WillEndDraggingEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.WillEndDraggingEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

```
public class WillEndDraggingEventArgs : EventArgs {
        
        public WillEndDraggingEventArgs (System.Drawing.PointF velocity, System.Drawing.PointF targetContentOffset);
        
        public System.Drawing.PointF TargetContentOffset {
                get;
                set;
        }
        public System.Drawing.PointF Velocity {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

 <a name="Type_Changed:_MonoTouch.iAd.ADBannerView" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADBannerView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public static ADBannerViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static ADBannerViewAppearance Appearance {
                get;
        }
        public event EventHandler WillLoad;
        
        public class ADBannerViewAppearance : UIView.MonoTouch.UIKit.UIViewAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.iAd.ADBannerViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADBannerViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void WillLoad (ADBannerView bannerView);
```

 <a name="Type_Changed:_MonoTouch.iAd.ADInterstitialAd" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADInterstitialAd

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public event EventHandler WillLoad;
```

 <a name="Type_Changed:_MonoTouch.iAd.ADInterstitialAdDelegate" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADInterstitialAdDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_4.2_to_5.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_5/API-diff-from-4.2#)

Added:

```
public virtual void WillLoad (ADInterstitialAd interstitialAd);
```
