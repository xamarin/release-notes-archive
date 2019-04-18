---
id: EAF9E5E3-8FE2-496B-EDDF-E315F7140CFF
title: "From 3.0.12 to 3.1.0"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "3.0.12";
```

Added:

```
public const string Version = "3.1.0";
        public const string GameKitLibrary = "/System/Library/Framew`orks/GameKit.framework/GameKit";
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReader" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReader

```
public class AVAssetReader : MonoTouch.Foundation.NSObject {
        
        public AVAssetReader ();
        public AVAssetReader (MonoTouch.Foundation.NSCoder coder);
        public AVAssetReader (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetReader (IntPtr handle);
        public AVAssetReader (AVAsset asset, IntPtr ptrToNsError);
        
        public static AVAssetReader _FromAsset (AVAsset asset, IntPtr ptrToNsError);
        public virtual void AddOutput (AVAssetReaderOutput output);
        public virtual bool CanAddOutput (AVAssetReaderOutput output);
        public virtual void CancelReading ();
        public virtual bool StartReading ();
        
        public virtual AVAsset Asset {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSError Error {
                get;
        }
        public virtual AVAssetReaderOutput[] Outputs {
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
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="public_class_AVAssetReaderAudioMixOutput_:_AVAssetReaderOutput_{" class="injected"></a>


## public class AVAssetReaderAudioMixOutput : AVAssetReaderOutput {

```
public AVAssetReaderAudioMixOutput ();
        public AVAssetReaderAudioMixOutput (MonoTouch.Foundation.NSCoder coder);
        public AVAssetReaderAudioMixOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetReaderAudioMixOutput (IntPtr handle);
        public AVAssetReaderAudioMixOutput (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
        
        public virtual AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
        
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
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReaderOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReaderOutput

public class AVAssetReaderOutput : MonoTouch.Foundation.NSObject {

```
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
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReaderTrackOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReaderTrackOutput

public class AVAssetReaderTrackOutput : AVAssetReaderOutput {

```
public AVAssetReaderTrackOutput ();
        public AVAssetReaderTrackOutput (MonoTouch.Foundation.NSCoder coder);
        public AVAssetReaderTrackOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetReaderTrackOutput (IntPtr handle);
        public AVAssetReaderTrackOutput (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
        
        public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
        
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
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput

public class AVAssetReaderVideoCompositionOutput : AVAssetReaderOutput {

```
public AVAssetReaderVideoCompositionOutput ();
        public AVAssetReaderVideoCompositionOutput (MonoTouch.Foundation.NSCoder coder);
        public AVAssetReaderVideoCompositionOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetReaderVideoCompositionOutput (IntPtr handle);
        public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
        
        public virtual AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
        
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
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetWriter" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetWriter

public class AVAssetWriter : MonoTouch.Foundation.NSObject {

```
public AVAssetWriter ();
        public AVAssetWriter (MonoTouch.Foundation.NSCoder coder);
        public AVAssetWriter (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetWriter (IntPtr handle);
        public AVAssetWriter (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, IntPtr ptrToNSError);
        
        public static AVAssetWriter FromUrl (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, IntPtr ptrToNSError);
        public virtual void AddInput (AVAssetWriterInput input);
        public virtual bool CanAddInput (AVAssetWriterInput input);
        public virtual bool CanApplyOutputSettings (MonoTouch.Foundation.NSDictionary outputSettings, string toMediaType);
        public virtual void CancelWriting ();
        public virtual void EndSessionAtSourceTime (MonoTouch.CoreMedia.CMTime endTime);
        public virtual bool FinishWriting ();
        public virtual void StartSessionAtSourceTime (MonoTouch.CoreMedia.CMTime startTime);
        public virtual bool StartWriting ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSError Error {
                get;
        }
        public virtual AVAssetWriterInput[] inputs {
                get;
        }
        public virtual AVMetadataItem[] Metadata {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMTime MovieFragmentInterval {
                get;
                set;
        }
        public virtual string OutputFileType {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl OutputURL {
                get;
        }
        public virtual bool ShouldOptimizeForNetworkUse {
                get;
                set;
        }
        public virtual AVAssetWriterStatus Status {
                get;
        }
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetWriterInput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetWriterInput

Added:

```
public class AVAssetWriterInput : MonoTouch.Foundation.NSObject {
        
        public AVAssetWriterInput ();
        public AVAssetWriterInput (MonoTouch.Foundation.NSCoder coder);
        public AVAssetWriterInput (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetWriterInput (IntPtr handle);
        public AVAssetWriterInput (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings);
        
        public static AVAssetWriterInput FromType (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings);
        public virtual bool AppendSampleBuffer (MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer);
        public virtual void MarkAsFinished ();
        public virtual void RequestMediaData (MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSAction action);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool ExpectsMediaDataInRealTime {
                get;
                set;
        }
        public virtual string MediaType {
                get;
        }
        public virtual AVMetadataItem[] Metadata {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary OutputSettings {
                get;
        }
        public virtual bool ReadyForMoreMediaData {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGAffineTransform Transform {
                get;
                set;
        }
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor

Added:

```
public class AVAssetWriterInputPixelBufferAdaptor : MonoTouch.Foundation.NSObject {
        
        public AVAssetWriterInputPixelBufferAdaptor ();
        public AVAssetWriterInputPixelBufferAdaptor (MonoTouch.Foundation.NSCoder coder);
        public AVAssetWriterInputPixelBufferAdaptor (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetWriterInputPixelBufferAdaptor (IntPtr handle);
        public AVAssetWriterInputPixelBufferAdaptor (AVAssetWriterInput input, MonoTouch.Foundation.NSDictionary sourcePixelBufferAttributes);
        
        public virtual AVAssetWriterInputPixelBufferAdaptor FromInput (AVAssetWriterInput input, MonoTouch.Foundation.NSDictionary sourcePixelBufferAttributes);
        
        public virtual AVAssetWriterInput AssetWriterInput {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary SourcePixelBufferAttributes {
                get;
        }
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetWriterStatus" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetWriterStatus

Added:

```
[Serializable]
 public enum AVAssetWriterStatus {
        Unknown,
        Writing,
        Completed,
        Failed,
        Cancelled
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AVFoundation.AVQueuePlayer" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVQueuePlayer

```
public class AVQueuePlayer : AVPlayer {
        
        public AVQueuePlayer ();
        public AVQueuePlayer (MonoTouch.Foundation.NSCoder coder);
        public AVQueuePlayer (MonoTouch.Foundation.NSObjectFlag t);
        public AVQueuePlayer (IntPtr handle);
        public AVQueuePlayer (AVPlayerItem[] items);
        
        public static AVQueuePlayer FromItems (AVPlayerItem[] items);
        public virtual void AdvanceToNextItem ();
        public virtual bool CanInsert (AVPlayerItem item, AVPlayerItem afterItem);
        public virtual void InsertItem (AVPlayerItem item, AVPlayerItem afterItem);
        public virtual void RemoveAllItems ();
        public virtual void RemoveItem (AVPlayerItem item);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVPlayerItem[] Items {
                get;
        }
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


# Namespace: MonoTouch.AddressBook

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AddressBook.ABPersonImageFormat" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABPersonImageFormat

```
[Serializable]
 public enum ABPersonImageFormat {
        Thumbnail,
        OriginalSize
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added:

```
public AudioQueueTimeline CreateTimeline ();
        public AudioQueueStatus GetCurrentTime (AudioQueueTimeline timeline, ref AudioTimeStamp time, ref bool timelineDiscontinuty);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueueStatus" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueueStatus

Added:

```
QueueStopped
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioQueueTimeline" class="injected"></a>


## New Type: MonoTouch.AudioToolbox.AudioQueueTimeline

Added:

```
public class AudioQueueTimeline : IDisposable {
        
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        IntPtr timelineHandle;
        IntPtr queueHandle;
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioTimeStamp" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioTimeStamp

Added:

```
public struct AudioTimeStamp {
        public override string ToString ();
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.AudioToolbox.SmpteTime" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.SmpteTime

Added:

```
public override string ToString ();
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.CoreGraphics.CGFunction" class="injected"></a>


## New Type: MonoTouch.CoreGraphics.CGFunction

```
public class CGFunction : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CGFunction (float [] domain, float [] range, CGFunctionEvaluate callback);
        
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public IntPtr Handle {
                get;
        }
        
        [Serializable]
        public delegate void CGFunctionEvaluate (float * data, float * outData);
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.CoreGraphics.CGShading" class="injected"></a>


## New Type: MonoTouch.CoreGraphics.CGShading

```
public class CGShading : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CGShading CreateAxial (CGColorSpace colorspace, System.Drawing.PointF start, System.Drawing.PointF end, CGFunction function, bool extendStart, bool extendEnd);
        public static CGShading CreateRadial (CGColorSpace colorspace, System.Drawing.PointF start, float startRadius, System.Drawing.PointF end, float endRadius, CGFunction function, bool extendStart, bool extendEnd);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

Removed:

```
public static bool _HeadingAvailable {
```

Added:

```
public static bool HeadingAvailable {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.CoreText" class="injected"></a>


# Namespace: MonoTouch.CoreText

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontManager" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontManager

Removed:

```
Could not find MonoTouch.CoreText.CTFontManager
```

Added:

```
public class CTFontManager {
        
        public CTFontManager ();
        
        public static bool IsFontSupported (MonoTouch.Foundation.NSUrl url);
        public static MonoTouch.Foundation.NSError RegisterFontsForUrl (MonoTouch.Foundation.NSUrl fontUrl, CTFontManagerScope scope);
        public static MonoTouch.Foundation.NSError[] RegisterFontsForUrl (MonoTouch.Foundation.NSUrl[] fontUrls, CTFontManagerScope scope);
        public static MonoTouch.Foundation.NSError UnregisterFontsForUrl (MonoTouch.Foundation.NSUrl fontUrl, CTFontManagerScope scope);
        public static MonoTouch.Foundation.NSError[] UnregisterFontsForUrl (MonoTouch.Foundation.NSUrl[] fontUrls, CTFontManagerScope scope);
        
        public static readonly MonoTouch.Foundation.NSString ErrorDomain;
        public static readonly MonoTouch.Foundation.NSString ErrorFontUrlsKey;
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontManagerAutoActivation" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontManagerAutoActivation

Removed:

```
Could not find MonoTouch.CoreText.CTFontManagerAutoActivation
```

Added:

```
[Serializable]
 public enum CTFontManagerAutoActivation {
        Default,
        Disabled,
        Enabled,
        PromptUser
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontManagerError" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontManagerError

Removed:

```
Could not find MonoTouch.CoreText.CTFontManagerError
```

Added:

```
[Serializable]
 public enum CTFontManagerError {
        None,
        FileNotFount,
        InsufficientPermissions,
        UnrecognizedFormat,
        InvalidFontData,
        AlreadyRegistered,
        NotRegistered,
        InUse,
        SystemRequired
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontManagerScope" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontManagerScope

Removed:

```
Could not find MonoTouch.CoreText.CTFontManagerScope
```

Added:

```
[Serializable]
 public enum CTFontManagerScope {
        None,
        Process,
        User,
        Session
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSCachedUrlResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Removed:

```
Could not find MonoTouch.Foundation.NSCachedUrlResponse
```

Added:

```
public class NSCachedUrlResponse : NSObject {
        
        public NSCachedUrlResponse ();
        public NSCachedUrlResponse (NSCoder coder);
        public NSCachedUrlResponse (NSObjectFlag t);
        public NSCachedUrlResponse (IntPtr handle);
        public NSCachedUrlResponse (NSUrlResponse response, NSData data, NSDictionary userInfo, NSUrlCacheStoragePolicy storagePolicy);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSData Data {
                get;
        }
        public virtual NSUrlResponse Response {
                get;
        }
        public virtual NSUrlCacheStoragePolicy StoragePolicy {
                get;
        }
        public virtual NSDictionary UserInfo {
                get;
        }
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSCoder" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCoder

Added:

```
public byte [] DecodeBytes (string key);
        public void Encode (byte [] buffer, int offset, int count, string key);
        public void Encode (byte [] buffer, string key);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSDirectoryEnumerator" class="injected"></a>


## New Type: MonoTouch.Foundation.NSDirectoryEnumerator

```
public class NSDirectoryEnumerator : NSEnumerator {
        
        public NSDirectoryEnumerator ();
        public NSDirectoryEnumerator (NSCoder coder);
        public NSDirectoryEnumerator (NSObjectFlag t);
        public NSDirectoryEnumerator (IntPtr handle);
        
        public virtual void SkipDescendents ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSDictionary DirectoryAttributes {
                get;
        }
        public virtual NSDictionary FileAttributes {
                get;
        }
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSFileManager" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileManager

```
public class NSFileManager : NSObject {
        
        public NSFileManager ();
        public NSFileManager (NSCoder coder);
        public NSFileManager (NSObjectFlag t);
        public NSFileManager (IntPtr handle);
        
        public virtual string [] ComponentsToDisplay (string path);
        public virtual NSData Contents (string path);
        public virtual bool ContentsEqual (string path1, string path2);
        public virtual bool Copy (string srcPath, string dstPath, out NSError error);
        public virtual bool CopyPath (string src, string dest, IntPtr handler);
        public virtual bool CreateDirectory (string path, bool createIntermediates, NSDictionary attributes, out NSError error);
        public virtual bool CreateFile (string path, NSData data, NSDictionary attr);
        public virtual bool CreateSymbolicLink (string path, string destPath, out NSError error);
        public virtual string DisplayName (string path);
        public virtual bool FileExists (string path);
        public virtual bool FileExists (string path, bool isDirectory);
        public virtual NSDictionary GetAttributes (string path, out NSError error);
        public virtual string [] GetDirectoryContent (string path, out NSError error);
        public virtual string [] GetDirectoryContentRecursive (string path, out NSError error);
        public virtual NSDirectoryEnumerator GetEnumerator (string path);
        public virtual NSDictionary GetFileSystemAttributes (string path, out NSError error);
        public virtual string GetSymbolicLinkDestination (string path, out NSError error);
        public virtual bool IsDeletableFile (string path);
        public virtual bool IsExecutableFile (string path);
        public virtual bool IsReadableFile (string path);
        public virtual bool IsWritableFile (string path);
        public virtual bool Link (string srcPath, string dstPath, out NSError error);
        public virtual bool LinkPath (string src, string dest, IntPtr handler);
        public virtual bool Move (string srcPath, string dstPath, out NSError error);
        public virtual bool MovePath (string src, string dest, IntPtr handler);
        public virtual bool Remove (string path, out NSError error);
        public virtual bool RemoveFileAtPath (string path, IntPtr handler);
        public virtual bool SetAttributes (NSDictionary attributes, string path, out NSError error);
        public virtual string [] Subpaths (string path);
        
        public static NSString AppendOnly {
                get;
        }
        public static NSString Busy {
                get;
        }
        public static NSString CreationDate {
                get;
        }
        public static NSFileManager DefaultManager {
                get;
        }
        public static NSString DeviceIdentifier {
                get;
        }
        public static NSString ExtensionHidden {
                get;
        }
        public static NSString GroupOwnerAccountID {
                get;
        }
        public static NSString GroupOwnerAccountName {
                get;
        }
        public static NSString HFSCreatorCode {
                get;
        }
        public static NSString HFSTypeCode {
                get;
        }
        public static NSString Immutable {
                get;
        }
        public static NSString ModificationDate {
                get;
        }
        public static NSString NSFileType {
                get;
        }
        public static NSString OwnerAccountID {
                get;
        }
        public static NSString OwnerAccountName {
                get;
        }
        public static NSString PosixPermissions {
                get;
        }
        public static NSString ReferenceCount {
                get;
        }
        public static NSString Size {
                get;
        }
        public static NSString SystemFileNumber {
                get;
        }
        public static NSString SystemFreeNodes {
                get;
        }
        public static NSString SystemFreeSize {
                get;
        }
        public static NSString SystemNodes {
                get;
        }
        public static NSString SystemNumber {
                get;
        }
        public static NSString SystemSize {
                get;
        }
        public static NSString TypeBlockSpecial {
                get;
        }
        public static NSString TypeCharacterSpecial {
                get;
        }
        public static NSString TypeDirectory {
                get;
        }
        public static NSString TypeRegular {
                get;
        }
        public static NSString TypeSocket {
                get;
        }
        public static NSString TypeSymbolicLink {
                get;
        }
        public static NSString TypeUnknown {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string CurrentDirectory {
                get;
                set;
        }
        public NSFileManagerDelegate Delegate {
                get;
                set;
        }
        public virtual NSObject WeakDelegate {
                get;
                set;
        }
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSFileManagerDelegate" class="injected"></a>


## New Type: MonoTouch.Foundation.NSFileManagerDelegate

```
public class NSFileManagerDelegate : NSObject {
        
        public NSFileManagerDelegate ();
        public NSFileManagerDelegate (NSCoder coder);
        public NSFileManagerDelegate (NSObjectFlag t);
        public NSFileManagerDelegate (IntPtr handle);
        
        public virtual bool ShouldCopyItemAtPath (NSFileManager fm, NSString srcPath, NSString dstPath);
        public virtual bool ShouldCopyItemAtPath (NSFileManager fileManager, string srcPath, string dstPath);
        public virtual bool ShouldLinkItemAtPath (NSFileManager fileManager, string srcPath, string dstPath);
        public virtual bool ShouldMoveItemAtPath (NSFileManager fileManager, string srcPath, string dstPath);
        public virtual bool ShouldProceedAfterError (NSFileManager fm, NSDictionary errorInfo);
        public virtual bool ShouldProceedAfterErrorCopyingItem (NSFileManager fileManager, NSError error, string srcPath, string dstPath);
        public virtual bool ShouldProceedAfterErrorLinkingItem (NSFileManager fileManager, NSError error, string srcPath, string dstPath);
        public virtual bool ShouldProceedAfterErrorMovingItem (NSFileManager fileManager, NSError error, string srcPath, string dstPath);
        public virtual bool ShouldProceedAfterErrorRemovingItem (NSFileManager fileManager, NSError error, string path);
        public virtual bool ShouldRemoveItemAtPath (NSFileManager fileManager, string path);
}
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSUrlCache" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlCache

public class NSUrlCache : NSObject {

```
public NSUrlCache ();
        public NSUrlCache (NSCoder coder);
        public NSUrlCache (NSObjectFlag t);
        public NSUrlCache (IntPtr handle);
        public NSUrlCache (uint memoryCapacity, uint diskCapacity, string diskPath);
        
        public virtual NSCachedUrlResponse CachedResponseForRequest (NSUrlRequest request);
        public virtual void RemoveAllCachedResponses ();
        public virtual void RemoveCachedResponse (NSUrlRequest request);
        public virtual void StoreCachedResponse (NSCachedUrlResponse cachedResponse, NSUrlRequest forRequest);
        
        public static NSUrlCache SharedCache {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual uint CurrentDiskUsage {
                get;
        }
        public virtual uint CurrentMemoryUsage {
                get;
        }
        public virtual uint DiskCapacity {
                get;
                set;
        }
        public virtual uint MemoryCapacity {
                get;
                set;
        }
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSUrlCacheStoragePolicy" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlCacheStoragePolicy

```
[Serializable]
 public enum NSUrlCacheStoragePolicy {
        Allowed,
        AllowedInMemoryOnly,
        NotAllowed
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlConnectionDelegate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlConnectionDelegate

Added:

```
public virtual NSCachedUrlResponse WillCacheResponse (NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.Foundation.NSUrlError" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlError

```
[Serializable]
 public enum NSUrlError {
        Unknown,
        Cancelled,
        BadURL,
        TimedOut,
        UnsupportedURL,
        CannotFindHost,
        CannotConnectToHost,
        NetworkConnectionLost,
        DNSLookupFailed,
        HTTPTooManyRedirects,
        ResourceUnavailable,
        NotConnectedToInternet,
        RedirectToNonExistentLocation,
        BadServerResponse,
        UserCancelledAuthentication,
        UserAuthenticationRequired,
        ZeroByteResource,
        CannotDecodeRawData,
        CannotDecodeContentData,
        CannotParseResponse,
        FileDoesNotExist,
        FileIsDirectory,
        NoPermissionsToReadFile,
        DataLengthExceedsMaximum,
        SecureConnectionFailed,
        ServerCertificateHasBadDate,
        ServerCertificateUntrusted,
        ServerCertificateHasUnknownRoot,
        ServerCertificateNotYetValid,
        ClientCertificateRejected,
        CannotLoadFromNetwork,
        CannotCreateFile,
        CannotOpenFile,
        CannotCloseFile,
        CannotWriteToFile,
        CannotRemoveFile,
        CannotMoveFile,
        DownloadDecodingFailedMidStream,
        DownloadDecodingFailedToComplete
 }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

Removed:

```
public virtual int Points {
                get;
                set;
        }
```

Added:

```
public static void ResetAchivements (GKNotificationHandler errorHandler);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementDescription

Removed:

```
public virtual bool ShouldDisplayIfNotStarted {
                get;
                set;
        }
```

Added:

```
public virtual bool Hidden {
                get;
                set;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementViewController

Removed:

```
public virtual void SetDelegate (GKAchievementViewControllerDelegate target);
```

Added:

```
public GKAchievementViewControllerDelegate Delegat {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler DidFinish;
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementViewControllerDelegate

Removed:

```
public virtual void DidPressDismiss ();
```

Added:

```
public virtual void DidFinish (GKAchievementViewController viewController);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.GameKit.GKCategoryHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKCategoryHandler

```
[Serializable]
public delegate void GKCategoryHandler (string [] categories, string [] titles, MonoTouch.Foundation.NSError error);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKError" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKError

Removed:

```
FeatureNotAvailableInPreview
```

Added:

```
Underage,
        GameUnrecognized,
        NotSupported
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKFriendsHandler" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKFriendsHandler

Removed:

```
public delegate void GKFriendsHandler (GKPlayer[] friends, MonoTouch.Foundation.NSError error);
```

Added:

```
public delegate void GKFriendsHandler (string [] friends, MonoTouch.Foundation.NSError error);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKInvite" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKInvite

Removed:

```
public virtual bool Cancelled {
                get;
        }
        public virtual GKPlayer Inviter {
```

Added:

```
public virtual string Inviter {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKInviteHandler" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKInviteHandler

Removed:

```
public delegate void GKInviteHandler (GKInvite invite);
```

Added:

```
public delegate void GKInviteHandler (GKInvite invite, string [] players);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboard

Removed:

```
public GKLeaderboard (GKPlayer[] players);
```

Added:

```
public GKLeaderboard (string [] players);
        public static void LoadCategories (GKCategoryHandler categoryHandler);
        public virtual string Category {
                get;
                set;
        }
        public virtual string Title {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboardViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Removed:

```
public virtual void SetLeaderboardDelegate (GKLeaderboardViewController ldel);
```

Added:

```
public virtual string Category {
                get;
                set;
        }
        public GKLeaderboardViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual GKLeaderboardTimeScope TimeScope {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler DidFinish;
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboardViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboardViewControllerDelegate

Removed:

```
public virtual void LeaderboardDidPressDismiss ();
```

Added:

```
public virtual void DidFinish (GKLeaderboardViewController viewController);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKLocalPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLocalPlayer

Removed:

```
public virtual void SetStatus (string status, GKNotificationHandler errorHandler);
        public virtual bool Authenticated {
        public override IntPtr ClassHandle {
        public virtual GKPlayer[] Friends {
        public virtual GKLocalPlayer LocalPlayer {
        public virtual string Status {
                set;
```

Added:

```
public static MonoTouch.Foundation.NSString AuthenticationDidChangeNotificationName {
        public static GKLocalPlayer LocalPlayer {
                get;
        }
        public virtual bool Authenticated {
        public override IntPtr ClassHandle {
        public virtual string [] Friends {
        public virtual bool IsUnderage {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatch

Removed:

```
public virtual bool SendData (MonoTouch.Foundation.NSData data, GKPlayer[] players, GKMatchSendDataMode mode, MonoTouch.Foundation.NSError error);
        public virtual bool SendDataToAllPlayerswithDataModeerror (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, IntPtr ptrToNSErrorHandle);
        public virtual GKPlayer[] Players {
```

Added:

```
public virtual bool SendData (MonoTouch.Foundation.NSData data, string [] players, GKMatchSendDataMode mode, MonoTouch.Foundation.NSError error);
        public virtual bool SendDataToAllPlayers (MonoTouch.Foundation.NSData data, GKMatchSendDataMode mode, IntPtr ptrToNSErrorHandle);
        public virtual string [] PlayersIDs {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmaker" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmaker

Removed:

```
public virtual void CreateMatch (GKMatchRequest request, GKNotificationMatch completionHandler);
        public virtual void FindPlayers (GKMatchRequest request, GKFriendsHandler handler);
        public virtual void QueryPlayerGroupActivity (int playerGroup, GKQueryHandler handler);
```

Added:

```
public virtual void FindMatch (GKMatchRequest request, GKNotificationMatch matchHandler);
        public virtual void FindPlayers (GKMatchRequest request, GKFriendsHandler playerHandler);
        public virtual void QueryActivity (GKQueryHandler completionHandler);
        public virtual void QueryPlayerGroupActivity (uint playerGroup, GKQueryHandler completionHandler);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Removed:

```
public GKMatchmakerViewController (GKMatchRequest request, GKPlayer[] players);
        public virtual void SetHostedPlayerReady (GKPlayer player);
        public event EventHandler Cancelled;
        public event EventHandler<GKErrorEventArgs> Failed;
        public event EventHandler<GKMatchEventArgs> MatchCreated;
        public event EventHandler<GKPlayersEventArgs> PlayersFound;
```

Added:

```
public virtual void SetHostedPlayerReady (string playerID);
        public event EventHandler<GKErrorEventArgs> DidFailWithError;
        public event EventHandler<GKMatchEventArgs> DidFindMatch;
        public event EventHandler<GKPlayersEventArgs> DidFindPlayers;
        public event EventHandler WasCancelled;
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewControllerDelegate

Removed:

```
public abstract void Cancelled (GKMatchmakerViewController viewController);
        public abstract void Failed (GKMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
        public abstract void MatchCreated (GKMatchmakerViewController viewController, GKMatch match);
        public abstract void PlayersFound (GKMatchmakerViewController viewController, GKPlayer[] players);
```

Added:

```
public abstract void DidFailWithError (GKMatchmakerViewController viewController, MonoTouch.Foundation.NSError error);
        public abstract void DidFindMatch (GKMatchmakerViewController viewController, GKMatch match);
        public abstract void DidFindPlayers (GKMatchmakerViewController viewController, string [] playerIDs);
        public abstract void WasCancelled (GKMatchmakerViewController viewController);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchRequest" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchRequest

Added:

```
public virtual int MinPlayers {
                get;
                set;
        }
        public virtual uint PlayerAttributes {
                get;
                set;
        }
        public virtual string [] PlayersToInvite {
                get;
                set;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayer

Removed:

```
public virtual string Status {
                get;
        }
```

Added:

```
public static MonoTouch.Foundation.NSString DidChangeNotificationName {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayersEventArgs" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayersEventArgs

Removed:

```
public GKPlayersEventArgs (GKPlayer[] players);
        public GKPlayer[] Players {
```

Added:

```
public GKPlayersEventArgs (string [] playerIDs);
        public string [] PlayerIDs {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayerStateUpdateHandler" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayerStateUpdateHandler

Removed:

```
Could not find MonoTouch.GameKit.GKPlayerStateUpdateHandler
```

Added:

```
[Serializable]
 public delegate void GKPlayerStateUpdateHandler (string playerId, GKVoiceChatPlayerState state);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKScore" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKScore

Removed:

```
public virtual GKPlayer Player {
        public virtual int Value {
```

Added:

```
public GKScore (string category);
        public virtual void ReportScore (GKNotificationHandler errorHandler);
        
        public virtual string category {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDate date {
                get;
        }
        public virtual string Player {
        public virtual long Value {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKVoiceChat" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKVoiceChat

Added:

```
public static bool IsVoIPAllowed ();
        public virtual void SetPlayerStateUpdateHandler (GKPlayerStateUpdateHandler handler);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKVoiceChatService" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKVoiceChatService

Added:

```
public static bool IsVoIPAllowed {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKCircle" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKCircle

Added:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
                set;
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKCoordinateRegion" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKCoordinateRegion

Added:

```
public static MKCoordinateRegion FromDistance (MonoTouch.CoreLocation.CLLocationCoordinate2D center, double latitudinalMeters, double longitudinalMeters);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygon" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygon

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

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolyline" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolyline

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

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static bool Boolean_objc_msgSend_IntPtr_Boolean_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
        public static bool Boolean_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
        public static bool Boolean_objc_msgSendSuper_IntPtr_Boolean_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
        public static bool Boolean_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
        public static IntPtr IntPtr_objc_msgSend_UInt32_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, IntPtr arg3);
        public static IntPtr IntPtr_objc_msgSendSuper_UInt32_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, IntPtr arg3);
        public static void void_objc_msgSend_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
        public static void void_objc_msgSendSuper_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>


# Namespace: MonoTouch.StoreKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProductsResponse" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProductsResponse

Removed:

```
public virtual SKProduct[] InvalidProducts {
```

Added:

```
public virtual string [] InvalidProducts {
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIEvent" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIEvent

Added:

```
public virtual UIEventSubtype Subtype {
                get;
        }
        public virtual UIEventType Type {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizer

Added:

```
public virtual bool CanBePreventedByGestureRecognizer (UIGestureRecognizer preventingGestureRecognizer);
        public virtual bool CanPreventGestureRecognizer (UIGestureRecognizer preventedGestureRecognizer);
        public virtual void IgnoreTouch (UITouch touch, UIEvent forEvent);
        public virtual void Reset ();
        public virtual void TouchesBegan (MonoTouch.Foundation.NSSet touches, UIEvent evt);
        public virtual void TouchesCancelled (MonoTouch.Foundation.NSSet touches, UIEvent evt);
        public virtual void TouchesEnded (MonoTouch.Foundation.NSSet touches, UIEvent evt);
        public virtual void TouchesMoved (MonoTouch.Foundation.NSSet touches, UIEvent evt);
                set;
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerController

Added:

```
public static MonoTouch.Foundation.NSString MediaMetadata {
                get;
        }
        public static MonoTouch.Foundation.NSString ReferenceUrl {
                get;
        }
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboardType" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboardType

Removed:

```
EmailAddress
```

Added:

```
EmailAddress,
        DecimalPad
```

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.12_to_3.1.0/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.1.0#)

 <a name="New_Type:_MonoTouch.iAd.ADError" class="injected"></a>


## New Type: MonoTouch.iAd.ADError

```
[Serializable]
public enum ADError {
        Unknown,
        ServerFailure,
        LoadingThrottled,
        InventoryUnavailable,
        ConfigurationError,
        BannerVisibleWithoutContent
}
```
