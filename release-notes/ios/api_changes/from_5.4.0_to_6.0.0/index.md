---
id: EBB6AABB-735F-FE70-BD19-C76566A34F51
title: "From 5.4.0 to 6.0.0"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.4.0";
```

Added:

```
public const string Version = "6.0.0";
        public const string StoreKitLibrary = "/System/Library/Frameworks/StoreKit.framework/StoreKit";
        public const string MediaToolboxLibrary = "/System/Library/Frameworks/MediaToolbox.framework/MediaToolbox";
        public const string PassKitLibrary = "/System/Library/Frameworks/PassKit.framework/PassKit";
        public const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

Added:

```
public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string [] languages);
        public virtual AVAssetReferenceRestrictions ReferenceRestrictions {
                get;
        }
        public virtual AVAssetResourceLoader ResourceLoader {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

Added:

```
public static void DetermineCompatibilityOfExportPreset (string presetName, AVAsset asset, string outputFileType, Action<bool> isCompatibleResult);
        public static AVAssetExportSession FromAsset (AVAsset asset, string presetName);
        public virtual void DetermineCompatibleFileTypes (Action<string []> compatibleFileTypesHandler);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGenerator" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

Added:

```
public virtual AVAsset Asset {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput

Removed:

```
public static AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
        public virtual MonoTouch.Foundation.NSDictionary AudioSettings {
```

Added:

```
public AVAssetReaderAudioMixOutput (AVAssetTrack[] audioTracks, AudioSettings settings);
        [Obsolete("Use Create method")]
        public static AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, MonoTouch.Foundation.NSDictionary audioSettings);
        public AVAssetReaderAudioMixOutput Create (AVAssetTrack[] audioTracks, AudioSettings settings);
        [Obsolete("Use Settings property")]
        public virtual MonoTouch.Foundation.NSDictionary AudioSettings {
        public AudioSettings Settings {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderTrackOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderTrackOutput

Removed:

```
public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
```

Added:

```
public AVAssetReaderTrackOutput (AVAssetTrack track, AudioSettings settings);
        public AVAssetReaderTrackOutput (AVAssetTrack track, AVVideoSettingsUncompressed settings);
        public static AVAssetReaderTrackOutput Create (AVAssetTrack track, AudioSettings settings);
        public static AVAssetReaderTrackOutput Create (AVAssetTrack track, AVVideoSettingsUncompressed settings);
        [Obsolete("Use Create method")]
        public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, MonoTouch.Foundation.NSDictionary outputSettings);
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput 

Removed:

```
public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
        public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
        public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
        public AVVideoSettings VideoSettings {
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetResourceLoader" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetResourceLoader

```
public class AVAssetResourceLoader : MonoTouch.Foundation.NSObject {
        
        public AVAssetResourceLoader ();
        public AVAssetResourceLoader (MonoTouch.Foundation.NSCoder coder);
        public AVAssetResourceLoader (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetResourceLoader (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void SetDelegate (AVAssetResourceLoaderDelegate resourceLoaderDelegate, MonoTouch.CoreFoundation.DispatchQueue delegateQueue);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVAssetResourceLoaderDelegate Delegate {
                get;
        }
        public virtual MonoTouch.CoreFoundation.DispatchQueue DelegateQueue {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate

```
public abstract class AVAssetResourceLoaderDelegate : MonoTouch.Foundation.NSObject {
        
        public AVAssetResourceLoaderDelegate ();
        public AVAssetResourceLoaderDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVAssetResourceLoaderDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetResourceLoaderDelegate (IntPtr handle);
        
        public abstract bool ShouldWaitForLoadingOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAssetResourceLoadingRequest" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAssetResourceLoadingRequest

```
public class AVAssetResourceLoadingRequest : MonoTouch.Foundation.NSObject {
        
        public AVAssetResourceLoadingRequest ();
        public AVAssetResourceLoadingRequest (MonoTouch.Foundation.NSCoder coder);
        public AVAssetResourceLoadingRequest (MonoTouch.Foundation.NSObjectFlag t);
        public AVAssetResourceLoadingRequest (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void FinishLoading (MonoTouch.Foundation.NSUrlResponse usingResponse, MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSUrlRequest redirect);
        public virtual void FinishLoadingWithError (MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.Foundation.NSData GetStreamingContentKey (MonoTouch.Foundation.NSData appIdentifier, MonoTouch.Foundation.NSData contentIdentifier, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Finished {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrlRequest Request {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriter" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriter

Removed:

```
public virtual bool CanApplyOutputSettings (MonoTouch.Foundation.NSDictionary outputSettings, string toMediaType);
        public virtual bool FinishWriting ();
```

Added:

```
public bool CanApplyOutputSettings (AudioSettings outputSettings, string mediaType);
        public bool CanApplyOutputSettings (AVVideoSettingsCompressed outputSettings, string mediaType);
        public virtual bool CanApplyOutputSettings (MonoTouch.Foundation.NSDictionary outputSettings, string mediaType);
        [Obsolete("This is a synchronous methods, use the asynchronous FinishWriting(NSAction completionHandler) instead")]
        public virtual bool FinishWriting ();
        public virtual void FinishWriting (MonoTouch.Foundation.NSAction completionHandler);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriterInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

Removed:

```
public static AVAssetWriterInput FromType (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings);
```

Added:

```
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
        public virtual MonoTouch.CoreMedia.CMFormatDescription SourceFormatHint {
                get;
        }
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor 

Removed:

```
public static AVAssetWriterInputPixelBufferAdaptor FromInput (AVAssetWriterInput input, MonoTouch.Foundation.NSDictionary sourcePixelBufferAttributes);
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioMixInputParameters" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioMixInputParameters

Added:

```
public virtual MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed:

```
public AVAudioPlayerSettings Settings {
```

Added:

```
public virtual AVAudioSessionChannelDescription[] ChannelAssignments {
                get;
                set;
        }
        [Obsolete("Use SoundSettings")]
        public AVAudioPlayerSettings Settings {
                get;
        }
        public AudioSettings SoundSetting {
        protected virtual MonoTouch.Foundation.NSDictionary WeakSettings {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayerDelegate" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayerDelegate

Removed:

```
public virtual void EndInterruption (AVAudioPlayer player);
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public virtual void EndInterruption (AVAudioPlayer player);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioRecorder" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioRecorder

Removed:

```
[Obsolete("Use the factory AVAudioRecorder.ToUrl as this method had an invalid signature up to MonoTouch 1.4.4")]
        public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
        public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, AVAudioRecorderSettings settings, out MonoTouch.Foundation.NSError error);
        public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, out MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.Foundation.NSDictionary Settings {
```

Added:

```
[Obsolete("Use static Create method as this method had an invalid signature up to MonoTouch 1.4.4")]
        public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
        public static AVAudioRecorder Create (MonoTouch.Foundation.NSUrl url, AudioSettings settings, out MonoTouch.Foundation.NSError error);
        [Obsolete("Use Create method")]
        public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, AVAudioRecorderSettings settings, out MonoTouch.Foundation.NSError error);
        [Obsolete("Use Create method")]
        public static AVAudioRecorder ToUrl (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, out MonoTouch.Foundation.NSError error);
        public virtual void RecordAt (double time);
        public virtual void RecordAt (double time, float duration);
        public AudioSettings AudioSettings {
                get;
        }
        public virtual AVAudioSessionChannelDescription[] ChannelAssignments {
                get;
                set;
        }
        public virtual double DeviceCurrentTime {
                get;
        }
        [Obsolete("Use AudioSettings")]
        public virtual MonoTouch.Foundation.NSDictionary Settings {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioRecorderDelegate" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioRecorderDelegate

Removed:

```
public virtual void EndInterruption (AVAudioRecorder recorder);
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public virtual void EndInterruption (AVAudioRecorder recorder);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSession

Removed:

```
public bool SetActive (bool beActive, AVAudioSessionFlags flags, out MonoTouch.Foundation.NSError outError);
        public bool SetActive (bool beActive, out MonoTouch.Foundation.NSError outError);
        public bool SetCategory (MonoTouch.Foundation.NSString theCategory, out MonoTouch.Foundation.NSError outError);
        [Obsolete("Use SetPreferredHardwareSampleRate(bool, out NSError) instead")]
        public bool SetPreferredHardwareSampleRate (double sampleRate, MonoTouch.Foundation.NSError outError);
        public bool SetPreferredHardwareSampleRate (double sampleRate, out MonoTouch.Foundation.NSError outError);
        public bool SetPreferredIOBufferDuration (double duration, out MonoTouch.Foundation.NSError outError);
        public virtual int currentHardwareInputNumberOfChannels {
        public virtual int CurrentHardwareOutputNumberOfChannels {
        public virtual double CurrentHardwareSampleRate {
        public AVAudioSessionDelegate Delegate {
        public virtual bool InputIsAvailable {
        public virtual double PreferredHardwareSampleRate {
```

Added:

```
public virtual bool OverrideOutputAudioPort (AVAudioSessionPortOverride portOverride, out MonoTouch.Foundation.NSError outError);
        [Obsolete("Obsolete in iOS 6.0, use SetActive (bool, AVAudioSessionSetActiveOptions, out NSError) instead")]
        public virtual bool SetActive (bool beActive, AVAudioSessionFlags flags, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetActive (bool active, AVAudioSessionSetActiveOptions options, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetActive (bool beActive, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetCategory (MonoTouch.Foundation.NSString theCategory, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetCategory (string category, AVAudioSessionCategoryOptions options, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetInputDataSource (AVAudioSessionDataSourceDescription dataSource, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetInputGain (float gain, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetOutputDataSource (AVAudioSessionDataSourceDescription dataSource, out MonoTouch.Foundation.NSError outError);
        [Obsolete("Use SetPreferredSampleRate(bool, out NSError) on iOS 6.0 instead")]
        public bool SetPreferredHardwareSampleRate (double sampleRate, MonoTouch.Foundation.NSError outError);
        [Obsolete("Obsoleted in iOS 6.0, use SetPreferredSampleRate")]
        public virtual bool SetPreferredHardwareSampleRate (double sampleRate, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetPreferredIOBufferDuration (double duration, out MonoTouch.Foundation.NSError outError);
        public virtual bool SetPreferredSampleRate (double sampleRate, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSString CategoryMultiRoute {
                get;
        }
        public static MonoTouch.Foundation.NSString InterruptionNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString MediaServicesWereResetNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString ModeMoviePlayback {
                get;
        }
        public static MonoTouch.Foundation.NSString PortAirPlay {
                get;
        }
        public static MonoTouch.Foundation.NSString PortBluetoothA2DP {
                get;
        }
        public static MonoTouch.Foundation.NSString PortBluetoothHfp {
                get;
        }
        public static MonoTouch.Foundation.NSString PortBuiltInMic {
                get;
        }
        public static MonoTouch.Foundation.NSString PortBuiltInReceiver {
                get;
        }
        public static MonoTouch.Foundation.NSString PortBuiltInSpeaker {
                get;
        }
        public static MonoTouch.Foundation.NSString PortHdmi {
                get;
        }
        public static MonoTouch.Foundation.NSString PortHeadphones {
                get;
        }
        public static MonoTouch.Foundation.NSString PortHeadsetMic {
                get;
        }
        public static MonoTouch.Foundation.NSString PortLineIn {
                get;
        }
        public static MonoTouch.Foundation.NSString PortLineOut {
                get;
        }
        public static MonoTouch.Foundation.NSString PortUsbAudio {
                get;
        }
        public static MonoTouch.Foundation.NSString RouteChangeNotification {
                get;
        }
        public virtual AVAudioSessionCategoryOptions CategoryOptions {
                get;
        }
        [Obsolete("Deprecated in iOS 6.0, use InputNumberOfChannels instead")]
        public virtual int CurrentHardwareInputNumberOfChannels {
        [Obsolete("Deprecated in iOS 6.0, use OutputNumberOfChannels instead")]
        public virtual int CurrentHardwareOutputNumberOfChannels {
        [Obsolete("Deprecated in iOS 6.0, use SampleRate instead")]
        public virtual double CurrentHardwareSampleRate {
        public virtual AVAudioSessionRouteDescription CurrentRoute {
                get;
        }
        [Obsolete("AVAudioSession.Delegate is deprecated on iOS 6.0, use AVAudioSession.Notification.Observe* methods instead")]
        public AVAudioSessionDelegate Delegate {
        public virtual bool InputAvailable {
                get;
        }
        public virtual AVAudioSessionDataSourceDescription InputDataSource {
                get;
        }
        public virtual AVAudioSessionDataSourceDescription[] InputDataSources {
                get;
        }
        public virtual float InputGain {
                get;
        }
        public virtual bool InputGainSettable {
                get;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool InputIsAvailable {
                get;
        }
        public virtual double InputLatency {
                get;
        }
        public virtual int InputNumberOfChannels {
                get;
        }
        public virtual double IOBufferDuration {
        public virtual bool OtherAudioPlaying {
                get;
        }
        public virtual AVAudioSessionDataSourceDescription OutputDataSource {
                get;
        }
        public virtual AVAudioSessionDataSourceDescription[] OutputDataSources {
                get;
        }
        public virtual double OutputLatency {
                get;
        }
        public virtual int OutputNumberOfChannels {
                get;
        }
        public virtual float OutputVolume {
                get;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual double PreferredHardwareSampleRate {
        public virtual double PreferredSampleRate {
                get;
        }
        public virtual double SampleRate {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveInterruption (EventHandler<AVAudioSessionInterruptionEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveMediaServicesWereReset (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveRouteChange (EventHandler<AVAudioSessionRouteChangeEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionCategoryOptions" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionCategoryOptions

```
[Serializable]
[Flags]
public enum AVAudioSessionCategoryOptions {
        MixWithOthers,
        DuckOthers,
        AllowBluetooth,
        DefaultToSpeaker
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionChannelDescription" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionChannelDescription

```
public class AVAudioSessionChannelDescription : MonoTouch.Foundation.NSObject {
        
        public AVAudioSessionChannelDescription ();
        public AVAudioSessionChannelDescription (MonoTouch.Foundation.NSCoder coder);
        public AVAudioSessionChannelDescription (MonoTouch.Foundation.NSObjectFlag t);
        public AVAudioSessionChannelDescription (IntPtr handle);
        
        public virtual string ChannelName {
                get;
        }
        public virtual int ChannelNumber {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string OwningPortUID {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionDataSourceDescription" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionDataSourceDescription

```
public class AVAudioSessionDataSourceDescription : MonoTouch.Foundation.NSObject {
        
        public AVAudioSessionDataSourceDescription ();
        public AVAudioSessionDataSourceDescription (MonoTouch.Foundation.NSCoder coder);
        public AVAudioSessionDataSourceDescription (MonoTouch.Foundation.NSObjectFlag t);
        public AVAudioSessionDataSourceDescription (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSNumber DataSourceID {
                get;
        }
        public virtual string DataSourceName {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionInterruptionEventArgs" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionEventArgs

```
public class AVAudioSessionInterruptionEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVAudioSessionInterruptionEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public AVAudioSessionInterruptionType InterruptionType {
                get;
        }
        public AVAudioSessionInterruptionOptions Option {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionInterruptionOptions" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionOptions

```
[Serializable]
[Flags]
public enum AVAudioSessionInterruptionOptions {
        ShouldResume
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionInterruptionType" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionType

```
[Serializable]
public enum AVAudioSessionInterruptionType {
        Ended,
        Began
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionPortDescription" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionPortDescription

```
public class AVAudioSessionPortDescription : MonoTouch.Foundation.NSObject {
        
        public AVAudioSessionPortDescription ();
        public AVAudioSessionPortDescription (MonoTouch.Foundation.NSCoder coder);
        public AVAudioSessionPortDescription (MonoTouch.Foundation.NSObjectFlag t);
        public AVAudioSessionPortDescription (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual AVAudioSessionChannelDescription[] Channels {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string PortName {
                get;
        }
        public virtual MonoTouch.Foundation.NSString PortType {
                get;
        }
        public virtual string UID {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionPortOverride" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionPortOverride

```
[Serializable]
public enum AVAudioSessionPortOverride {
        None,
        Speaker
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionRouteChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionRouteChangeEventArgs

```
public class AVAudioSessionRouteChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVAudioSessionRouteChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public AVAudioSessionRouteDescription PreviousRoute {
                get;
        }
        public AVAudioSessionRouteChangeReason Reason {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionRouteChangeReason" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionRouteChangeReason

```
[Serializable]
public enum AVAudioSessionRouteChangeReason {
        Unknown,
        NewDeviceAvailable,
        OldDeviceUnavailable,
        CategoryChange,
        Override,
        WakeFromSleep,
        NoSuitableRouteForCategory
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionRouteDescription" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionRouteDescription

```
public class AVAudioSessionRouteDescription : MonoTouch.Foundation.NSObject {
        
        public AVAudioSessionRouteDescription ();
        public AVAudioSessionRouteDescription (MonoTouch.Foundation.NSCoder coder);
        public AVAudioSessionRouteDescription (MonoTouch.Foundation.NSObjectFlag t);
        public AVAudioSessionRouteDescription (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVAudioSessionPortDescription[] Inputs {
                get;
        }
        public virtual AVAudioSessionPortDescription[] Outputs {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVAudioSessionSetActiveOptions" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVAudioSessionSetActiveOptions

```
[Serializable]
[Flags]
public enum AVAudioSessionSetActiveOptions {
        NotifyOthersOnDeactivation
}
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate 

Added:

```
public virtual void DidDropSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureConnection" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureConnection

Added:

```
public virtual bool AutomaticallyAdjustsVideoMirroring {
                get;
                set;
        }
        public virtual bool EnablesVideoStabilizationWhenAvailable {
                get;
                set;
        }
        public virtual bool SupportsVideoStabilization {
                get;
        }
        public virtual AVCaptureVideoPreviewLayer VideoPreviewLayer {
                get;
        }
        public virtual bool VideoStabilizationEnabled {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added:

```
public virtual bool SetTorchModeLevel (float torchLevel, out MonoTouch.Foundation.NSError outError);
        public static float MaxAvailableTorchLevel {
                get;
        }
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
        public virtual bool TorchActive {
                get;
        }
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureDeviceTransportControlsPlaybackMode 

```
[Serializable]
public enum AVCaptureDeviceTransportControlsPlaybackMode {
        NotPlaying,
        Playing
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureInputPort" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureInputPort

Added:

```
public virtual MonoTouch.CoreMedia.CMFormatDescription FormatDescription {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureMetadataOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureMetadataOutput

```
public class AVCaptureMetadataOutput : AVCaptureOutput {
        
        public AVCaptureMetadataOutput ();
        public AVCaptureMetadataOutput (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureMetadataOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureMetadataOutput (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void SetDelegate (AVCaptureMetadataOutputObjectsDelegate objectsDelegate, MonoTouch.CoreFoundation.DispatchQueue objectsCallbackQueue);
        
        public virtual MonoTouch.Foundation.NSString[] AvailableMetadataObjectTypes {
                get;
        }
        public virtual MonoTouch.CoreFoundation.DispatchQueue CallbackQueue {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual AVCaptureMetadataOutputObjectsDelegate Delegate {
                get;
        }
        public virtual MonoTouch.Foundation.NSArray MetadataObjectTypes {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureMetadataOutputObjectsDelegate" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureMetadataOutputObjectsDelegate

```
public class AVCaptureMetadataOutputObjectsDelegate : MonoTouch.Foundation.NSObject {
        
        public AVCaptureMetadataOutputObjectsDelegate ();
        public AVCaptureMetadataOutputObjectsDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVCaptureMetadataOutputObjectsDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVCaptureMetadataOutputObjectsDelegate (IntPtr handle);
        
        public virtual void DidOutputMetadataObjects (AVCaptureMetadataOutput captureOutput, AVMetadataObject[] metadataObjects, AVCaptureConnection connection);
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureOutput

Added:

```
public virtual AVMetadataObject GetTransformedMetadataObject (AVMetadataObject metadataObject, AVCaptureConnection connection);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureStillImageOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput

Added:

```
public AVVideoSettingsCompressed CompressedVideoSetting {
                get;
                set;
        }
        public AVVideoSettingsUncompressed UncompressedVideoSetting {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoDataOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput

Removed:

```
public AVVideoSettings VideoSettings {
```

Added:

```
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
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer

Removed:

```
public virtual bool AutomaticallyAdjustsMirroring {
        public virtual bool Mirrored {
        public virtual bool MirroringSupported {
        public virtual AVCaptureVideoOrientation Orientation {
        public virtual bool OrientationSupported {
        public virtual string VideoGravity {
```

Added:

```
public virtual System.Drawing.PointF CaptureDevicePointOfInterestForPoint (System.Drawing.PointF pointInLayer);
        public virtual AVMetadataObject GetTransformedMetadataObject (AVMetadataObject metadataObject);
        public virtual System.Drawing.PointF PointForCaptureDevicePointOfInterest (System.Drawing.PointF captureDevicePointOfInterest);
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool AutomaticallyAdjustsMirroring {
        public virtual AVCaptureConnection Connection {
                get;
        }
        public AVLayerVideoGravity LayerVideoGravity {
                get;
                set;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool Mirrored {
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool MirroringSupported {
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual AVCaptureVideoOrientation Orientation {
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool OrientationSupported {
        [Obsolete("Use LayerVideoGravity")]
        public virtual string VideoGravity {
                get;
                set;
        }
        protected virtual MonoTouch.Foundation.NSString WeakVideoGravity {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVError" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVError

Added:

```
ApplicationIsNotAuthorized,
        ReferenceForbiddenByReferencePolicy,
        ScreenCaptureFailed,
        DisplayWasDisabled,
        TorchLevelUnavailable,
        OperationInterrupted,
        IncompatibleAsset,
        FailedToLoadMediaData,
        ServerIncorrectlyConfigured
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVFileType" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVFileType

Removed:

```
public class AVFileType {
        
        public AVFileType ();
```

Added:

```
public static class AVFileType {
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVLayerVideoGravity" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVLayerVideoGravity

```
[Serializable]
public enum AVLayerVideoGravity {
        ResizeAspect,
        ResizeAspectFill,
        Resize
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMediaCharacteristic" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMediaCharacteristic

Removed:

```
public class AVMediaCharacteristic {
        
        public AVMediaCharacteristic ();
```

Added:

```
public static class AVMediaCharacteristic {
        public static MonoTouch.Foundation.NSString EasyToRead {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMediaSelectionGroup" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMediaSelectionGroup

Removed:

```
public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (MonoTouch.Foundation.NSArray array, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
```

Added:

```
public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (AVMediaSelectionOption[] source, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMediaType" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMediaType

Removed:

```
public class AVMediaType {
        
        public AVMediaType ();
```

Added:

```
public static class AVMediaType {
        public static MonoTouch.Foundation.NSString Metadata {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMetadata" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMetadata

Removed:

```
public class AVMetadata {
        
        public AVMetadata ();
```

Added:

```
public static class AVMetadata {
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMetadataFaceObject" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMetadataFaceObject

```
public class AVMetadataFaceObject : AVMetadataObject {
        
        public AVMetadataFaceObject ();
        public AVMetadataFaceObject (MonoTouch.Foundation.NSCoder coder);
        public AVMetadataFaceObject (MonoTouch.Foundation.NSObjectFlag t);
        public AVMetadataFaceObject (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int FaceID {
                get;
        }
        public virtual bool HasRollAngle {
                get;
        }
        public virtual bool HasYawAngle {
                get;
        }
        public virtual float RollAngle {
                get;
        }
        public virtual float YawAngle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMetadataItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMetadataItem

Removed:

```
public static AVMetadataItem[] FilterWithKey (AVMetadataItem[] array, MonoTouch.Foundation.NSObject key, string keySpace);
```

Added:

```
public static AVMetadataItem[] FilterFromPreferredLanguages (AVMetadataItem[] metadataItems, string [] preferredLanguages);
        public static AVMetadataItem[] FilterWithKey (AVMetadataItem[] metadataItems, MonoTouch.Foundation.NSObject key, string keySpace);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMetadataObject" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMetadataObject

```
public class AVMetadataObject : MonoTouch.Foundation.NSObject {
        
        public AVMetadataObject (MonoTouch.Foundation.NSCoder coder);
        public AVMetadataObject (MonoTouch.Foundation.NSObjectFlag t);
        public AVMetadataObject (IntPtr handle);
        
        public static MonoTouch.Foundation.NSString TypeFace {
                get;
        }
        public virtual System.Drawing.RectangleF Bounds {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTime Duration {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTime Time {
                get;
        }
        public virtual string Type {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableAudioMixInputParameters" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters

Added:

```
public virtual MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayer

Removed:

```
public virtual bool AirPlayVideoActive {
        public virtual bool AllowsAirPlayVideo {
        public virtual bool UsesAirPlayVideoWhileAirPlayScreenIsActive {
```

Added:

```
public virtual void CancelPendingPrerolls ();
        public virtual void Preroll (float rate, AVCompletion onComplete);
        public virtual void Seek (MonoTouch.Foundation.NSDate date);
        public virtual void Seek (MonoTouch.Foundation.NSDate date, AVCompletion onComplete);
        public virtual void SetRate (float rate, MonoTouch.CoreMedia.CMTime itemTime, MonoTouch.CoreMedia.CMTime hostClockTime);
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
        public Nullable<AVLayerVideoGravity> ExternalPlaybackVideoGravity {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMClock MasterClock {
                get;
        }
        public virtual bool OutputObscuredDueToInsufficientExternalProtection {
                get;
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
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Added:

```
public virtual void AddOutput (AVPlayerItemOutput output);
        public virtual void RemoveOutput (AVPlayerItemOutput output);
        public virtual bool Seek (MonoTouch.Foundation.NSDate date, AVCompletion completion);
        public static MonoTouch.Foundation.NSString NewAccessLogEntryNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString NewErrorLogEntryNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackStalledNotification {
                get;
        }
        public virtual bool CanPlayReverse {
                get;
        }
        public virtual bool CanPlaySlowForward {
                get;
        }
        public virtual bool CanPlaySlowReverse {
                get;
        }
        public virtual bool CanStepBackward {
                get;
        }
        public virtual bool CanStepForward {
                get;
        }
        public virtual MonoTouch.CoreMedia.CMTime Duration {
                get;
        }
        public virtual AVPlayerItemOutput Outputs {
                get;
        }
        public virtual bool SeekingWaitsForVideoCompositionRendering {
                get;
                set;
        }
        public virtual AVTextStyleRule[] TextStyleRules {
                get;
                set;
        }
        public virtual MonoTouch.CoreMedia.CMTimebase Timebase {
                get;
        }
                public static MonoTouch.Foundation.NSObject ObserveNewAccessLogEntry (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNewErrorLogEntry (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackStalled (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent

Added:

```
public virtual int NumberOfMediaRequests {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemOutput

```
public class AVPlayerItemOutput : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemOutput (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemOutput (IntPtr handle);
        
        public virtual MonoTouch.CoreMedia.CMTime GetItemTime (double hostTimeInSeconds);
        public virtual MonoTouch.CoreMedia.CMTime GetItemTime (long machAbsoluteTime);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool SuppressesPlayerRendering {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemOutputPullDelegate" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemOutputPullDelegate

```
public class AVPlayerItemOutputPullDelegate : MonoTouch.Foundation.NSObject {
        
        public AVPlayerItemOutputPullDelegate ();
        public AVPlayerItemOutputPullDelegate (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemOutputPullDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemOutputPullDelegate (IntPtr handle);
        
        public virtual void OutputMediaDataWillChange (AVPlayerItemOutput sender);
        public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemVideoOutput" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemVideoOutput

```
public class AVPlayerItemVideoOutput : AVPlayerItemOutput {
        
        public AVPlayerItemVideoOutput ();
        public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSCoder coder);
        public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSObjectFlag t);
        public AVPlayerItemVideoOutput (IntPtr handle);
        protected AVPlayerItemVideoOutput (MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
        public AVPlayerItemVideoOutput (MonoTouch.CoreVideo.CVPixelBufferAttributes attributes);
        
        public virtual MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
        protected override void Dispose (bool disposing);
        public virtual bool HasNewPixelBufferForItemTime (MonoTouch.CoreMedia.CMTime itemTime);
        public virtual void RequestNotificationOfMediaDataChange (double advanceInterval);
        public virtual void SetDelegate (AVPlayerItemOutputPullDelegate delegateClass, MonoTouch.CoreFoundation.DispatchQueue delegateQueue);
        
        public override IntPtr ClassHandle {
                get;
        }
        public AVPlayerItemOutputPullDelegate Delegate {
                get;
        }
        public virtual MonoTouch.CoreFoundation.DispatchQueue DelegateQueue {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerLayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerLayer

Removed:

```
public virtual string VideoGravity {
```

Added:

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVTextStyleRule" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVTextStyleRule

```
public class AVTextStyleRule : MonoTouch.Foundation.NSObject {
        
        public AVTextStyleRule ();
        public AVTextStyleRule (MonoTouch.Foundation.NSCoder coder);
        public AVTextStyleRule (MonoTouch.Foundation.NSObjectFlag t);
        public AVTextStyleRule (IntPtr handle);
        protected AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
        public AVTextStyleRule (MonoTouch.CoreMedia.CMTextMarkupAttributes attributes);
        protected AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
        public AVTextStyleRule (MonoTouch.CoreMedia.CMTextMarkupAttributes attributes, string textSelector);
        
        public static AVTextStyleRule[] FromPropertyList (MonoTouch.Foundation.NSObject plist);
        public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.CoreMedia.CMTextMarkupAttributes textMarkupAttributes);
        public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.CoreMedia.CMTextMarkupAttributes textMarkupAttributes, string textSelector);
        public static MonoTouch.Foundation.NSObject ToPropertyList (AVTextStyleRule[] textStyleRules);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public MonoTouch.CoreMedia.CMTextMarkupAttributes TextMarkupAttributes {
                get;
        }
        public virtual string TextSelector {
                get;
        }
        protected virtual MonoTouch.Foundation.NSDictionary WeakTextMarkupAttributes {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVUrlAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Removed:

```
public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
```

Added:

```
public AVUrlAsset (MonoTouch.Foundation.NSUrl url, AVUrlAssetOptions options);
        public static AVUrlAsset Create (MonoTouch.Foundation.NSUrl url, AVUrlAssetOptions options);
        [Obsolete("Use Create or constructor")]
        public static AVUrlAsset FromUrl (MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options);
        public static MonoTouch.Foundation.NSString ReferenceRestrictionsKey {
                get;
        }
        public virtual AVAssetResourceLoader ResourceLoader {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVUrlAssetOptions" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVUrlAssetOptions

```
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
</avassetreferencerestrictions></bool>
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideo" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideo

Removed:

```
public class AVVideo {
        
        public AVVideo ();
```

Added:

```
public static class AVVideo {
        public static MonoTouch.Foundation.NSString ProfileLevelH264High40 {
                get;
        }
        public static MonoTouch.Foundation.NSString ProfileLevelH264High41 {
                get;
        }
        public static MonoTouch.Foundation.NSString ScalingModeKey {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCleanApertureSettings" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCleanApertureSettings

```
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
</int></int></int></int>
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCodec" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCodec

```
[Serializable]
public enum AVVideoCodec {
        H264,
        JPEG
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoCodecSettings" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoCodecSettings

```
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
</avvideoprofilelevelh264></int></float></int>
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideoComposition" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoComposition

Added:

```
public static AVVideoComposition FromAssetProperties (AVAsset asset);
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoFieldMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoFieldMode

```
[Serializable]
public enum AVVideoFieldMode {
        Both,
        TopOnly,
        BottomOnly,
        Deinterlace
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoPixelAspectRatioSettings" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoPixelAspectRatioSettings

```
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
</int></int>
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoProfileLevelH264" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoProfileLevelH264

```
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
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoScalingMode" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoScalingMode

```
[Serializable]
public enum AVVideoScalingMode {
        Fit,
        Resize,
        ResizeAspect,
        ResizeAspectFill
}
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoScalingModeKey" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoScalingModeKey

```
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
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVVideoSettings" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoSettings

Removed:

```
public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
        public MonoTouch.Foundation.NSDictionary ToDictionary ();
        public System.Nullable<MonoTouch.CoreVideo.CVPixelFormatType> PixelFormat {
```

Added:

```
[Obsolete("Use PixelBufferAttributes")]
        public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
        [Obsolete("Use PixelBufferAttributes")]
        public MonoTouch.Foundation.NSDictionary ToDictionary ();
        [Obsolete("Use PixelBufferAttributes")]
        public System.Nullable<MonoTouch.CoreVideo.CVPixelFormatType> PixelFormat {
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoSettingsCompressed" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoSettingsCompressed

```
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
</int></avvideoscalingmode></int></avvideocodec>
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVVideoSettingsUncompressed" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVVideoSettingsUncompressed

```
public class AVVideoSettingsUncompressed : MonoTouch.CoreVideo.CVPixelBufferAttributes {
        
        public AVVideoSettingsUncompressed ();
        public AVVideoSettingsUncompressed (MonoTouch.Foundation.NSDictionary dictionary);
        
        public Nullable<avvideoscalingmode> ScalingMode {
                set;
        }
}
</avvideoscalingmode>
```

 <a name="New_Type:_MonoTouch.AVFoundation.AudioSettings" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AudioSettings

```
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
</avaudioquality></float></int></bool></bool></int></bool></monotouch.audiotoolbox.audioformattype></int></int></int></avaudioquality>
```

 <a name="Namespace:_MonoTouch.Accounts" class="injected"></a>


# Namespace: MonoTouch.Accounts

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccountCredential" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccountCredential

Removed:

```
public ACAccountCredential (string token, string secret);
```

Added:

```
public ACAccountCredential (string oauthToken, string tokenSecret);
        public ACAccountCredential (string oauth2Token, string refreshToken, MonoTouch.Foundation.NSDate expiryDate);
        public virtual string OAuthToken {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.Accounts.ACAccountCredentialRenewResult" class="injected"></a>


## New Type: MonoTouch.Accounts.ACAccountCredentialRenewResult

```
[Serializable]
public enum ACAccountCredentialRenewResult {
        Renewed,
        Rejected,
        Failed
}
```

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccountStore" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccountStore

Removed:

```
public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
```

Added:

```
public virtual void RenewCredentials (ACAccount account, System.Action<ACAccountCredentialRenewResult,MonoTouch.Foundation.NSError> completionHandler);
        [Obsolete("Obsolete in iOS 6.0. Use overload with options instead")]
        public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
        public void RequestAccess (ACAccountType accountType, AccountStoreOptions options, ACRequestCompletionHandler completion);
        protected virtual void RequestAccess (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options, ACRequestCompletionHandler completion);
```

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccountType" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccountType

Added:

```
public static MonoTouch.Foundation.NSString Facebook {
                get;
        }
        public static MonoTouch.Foundation.NSString SinaWeibo {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Accounts.ACErrorCode" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACErrorCode

Added:

```
AccessInfoInvalid
```

 <a name="New_Type:_MonoTouch.Accounts.ACFacebookAudience" class="injected"></a>


## New Type: MonoTouch.Accounts.ACFacebookAudience

```
[Serializable]
public enum ACFacebookAudience {
        Everyone,
        Friends,
        OnlyMe
}
```

 <a name="New_Type:_MonoTouch.Accounts.ACFacebookAudienceValue" class="injected"></a>


## New Type: MonoTouch.Accounts.ACFacebookAudienceValue

```
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
```

 <a name="New_Type:_MonoTouch.Accounts.ACFacebookKey" class="injected"></a>


## New Type: MonoTouch.Accounts.ACFacebookKey

```
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
```

 <a name="New_Type:_MonoTouch.Accounts.AccountStoreOptions" class="injected"></a>


## New Type: MonoTouch.Accounts.AccountStoreOptions

```
public class AccountStoreOptions : MonoTouch.Foundation.DictionaryContainer {
        
        public AccountStoreOptions ();
        public AccountStoreOptions (MonoTouch.Foundation.NSDictionary dictionary);
        
        public void SetPermissions (ACFacebookAudience audience, params string [] permissions);
        
        public string FacebookAppId {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.AdSupport" class="injected"></a>


# Namespace: MonoTouch.AdSupport

 <a name="New_Type:_MonoTouch.AdSupport.ASIdentifierManager" class="injected"></a>


## New Type: MonoTouch.AdSupport.ASIdentifierManager

```
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
```

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


# Namespace: MonoTouch.AddressBook

 <a name="Type_Changed:_MonoTouch.AddressBook.ABAddressBook" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABAddressBook

Removed:

```
public ABAddressBook ();
```

Added:

```
[Obsolete("Use static Create method in iOS 6.0")]
        public ABAddressBook ();
        public static ABAddressBook Create (out MonoTouch.Foundation.NSError error);
        public static ABAuthorizationStatus GetAuthorizationStatus ();
        public void RequestAccess (System.Action<bool,MonoTouch.Foundation.NSError> onCompleted);
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABAddressBookError" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABAddressBookError

Added:

```
OperationNotPermittedByUserError
```

 <a name="New_Type:_MonoTouch.AddressBook.ABAuthorizationStatus" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABAuthorizationStatus

```
[Serializable]
public enum ABAuthorizationStatus {
        NotDetermined,
        Restricted,
        Denied,
        Authorized
}
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPerson" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPerson

Removed:

```
public ABMultiValue`1 GetAddresses ();
        public ABMultiValue`1 GetInstantMessages ();
        public ABMultiValue`1 GetSocialProfile ();
```

Added:

```
[Obsolete("Use GetAllAddresses")]
        public ABMultiValue`1 GetAddresses ();
        public ABMultiValue`1 GetAllAddresses ();
        [Obsolete("Use GetInstantMessageServices")]
        public ABMultiValue`1 GetInstantMessages ();
        public ABMultiValue`1 GetInstantMessageServices ();
        [Obsolete("Use GetSocialProfiles")]
        public ABMultiValue`1 GetSocialProfile ();
        public ABMultiValue`1 GetSocialProfiles ();
        public void SetAddresses (ABMultiValue`1 addresses);
        public void SetInstantMessages (ABMultiValue`1 services);
        public void SetSocialProfile (ABMultiValue`1 profiles);
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPersonInstantMessageService" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPersonInstantMessageService

Added:

```
public static MonoTouch.Foundation.NSString Facebook {
                get;
        }
        public static MonoTouch.Foundation.NSString GaduGadu {
                get;
        }
        public static MonoTouch.Foundation.NSString GoogleTalk {
                get;
        }
        public static MonoTouch.Foundation.NSString QQ {
                get;
        }
        public static MonoTouch.Foundation.NSString Skype {
                get;
        }
```

 <a name="Type_Removed:_MonoTouch.AddressBook.ABPersonSocialProfile" class="injected"></a>


## Type Removed: MonoTouch.AddressBook.ABPersonSocialProfile

 <a name="New_Type:_MonoTouch.AddressBook.ABPersonSocialProfileService" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABPersonSocialProfileService

```
public static class ABPersonSocialProfileService {
        
        public static readonly MonoTouch.Foundation.NSString Twitter;
        public static readonly MonoTouch.Foundation.NSString GameCenter;
        public static readonly MonoTouch.Foundation.NSString Facebook;
        public static readonly MonoTouch.Foundation.NSString Myspace;
        public static readonly MonoTouch.Foundation.NSString LinkedIn;
        public static readonly MonoTouch.Foundation.NSString Flickr;
        public static readonly MonoTouch.Foundation.NSString SinaWeibo;
}
```

 <a name="New_Type:_MonoTouch.AddressBook.InstantMessageService" class="injected"></a>


## New Type: MonoTouch.AddressBook.InstantMessageService

```
public class InstantMessageService : MonoTouch.Foundation.DictionaryContainer {
        
        public InstantMessageService ();
        public InstantMessageService (MonoTouch.Foundation.NSDictionary dictionary);
        
        public MonoTouch.Foundation.NSString Service {
                set;
        }
        public string ServiceName {
                get;
                set;
        }
        public string Username {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AddressBook.PersonAddress" class="injected"></a>


## New Type: MonoTouch.AddressBook.PersonAddress

```
public class PersonAddress : MonoTouch.Foundation.DictionaryContainer {
        
        public PersonAddress ();
        public PersonAddress (MonoTouch.Foundation.NSDictionary dictionary);
        
        public string City {
                get;
                set;
        }
        public string Country {
                get;
                set;
        }
        public string CountryCode {
                get;
                set;
        }
        public string State {
                get;
                set;
        }
        public string Street {
                get;
                set;
        }
        public string Zip {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.AddressBook.SocialProfile" class="injected"></a>


## New Type: MonoTouch.AddressBook.SocialProfile

```
public class SocialProfile : MonoTouch.Foundation.DictionaryContainer {
        
        public SocialProfile ();
        public SocialProfile (MonoTouch.Foundation.NSDictionary dictionary);
        
        public MonoTouch.Foundation.NSString Service {
                set;
        }
        public string ServiceName {
                get;
                set;
        }
        public string Url {
                get;
                set;
        }
        public string UserIdentifier {
                get;
                set;
        }
        public string Username {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAsset" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAsset

Added:

```
public MonoTouch.Foundation.NSUrl AssetUrl {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

Added:

```
public static void DisableSharedPhotoStreamsSupport ();
        public static ALAuthorizationStatus AuthorizationStatus {
                get;
        }
        public static MonoTouch.Foundation.NSString DeletedAssetGroupsKey {
                get;
        }
        public static MonoTouch.Foundation.NSString InsertedAssetGroupsKey {
                get;
        }
        public static MonoTouch.Foundation.NSString UpdatedAssetGroupsKey {
                get;
        }
        public static MonoTouch.Foundation.NSString UpdatedAssetsKey {
                get;
        }
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAuthorizationStatus" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAuthorizationStatus

```
[Serializable]
public enum ALAuthorizationStatus {
        NotDetermined,
        Restricted,
        Denied,
        Authorized
}
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFormatType" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFormatType

Added:

```
MPEG4AAC_ELD_SBR
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

Added:

```
public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, ref AudioTimeStamp startTime, out AudioTimeStamp actualStartTime);
        public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, int bytes, AudioStreamPacketDescription[] desc, int trimFramesAtStart, int trimFramesAtEnd, AudioQueueParameterEvent[] parameterEvents, ref AudioTimeStamp startTime, out AudioTimeStamp actualStartTime);
```

 <a name="Namespace:_MonoTouch.AudioUnit" class="injected"></a>


# Namespace: MonoTouch.AudioUnit

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioTypeConverter" class="injected"></a>


## Type Changed: MonoTouch.AudioUnit.AudioTypeConverter

Added:

```
Varispeed,
        DeferredRenderer,
        Splitter,
        Merger,
        NewTimePitch,
        AUiPodTimeOther
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioTypeEffect" class="injected"></a>


## Type Changed: MonoTouch.AudioUnit.AudioTypeEffect

Added:

```
PeakLimiter,
        DynamicsProcessor,
        LowPassFilter,
        HighPassFilter,
        HighShelfFilter,
        LowShelfFilter,
        DCFilter,
        ParametricEQ,
        Delay,
        Distortion,
        BandPassFilter,
        Reverb2,
        NBandEq
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioTypeMixer" class="injected"></a>


## Type Changed: MonoTouch.AudioUnit.AudioTypeMixer

Added:

```
Matrix,
```

 <a name="Type_Changed:_MonoTouch.AudioUnit.AudioUnitPropertyIDType" class="injected"></a>


## Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added:

```
CPULoad,
        ParameterValueStrings,
        HostCallbacks,
        OfflineRender,
        DependentParameters,
        InputSampleInOutput,
        ParameterHistoryInfo,
        Nickname,
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

Added:

```
public virtual bool DrawsAsynchronously {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.CoreBluetooth" class="injected"></a>


# Namespace: MonoTouch.CoreBluetooth

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBATTError" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBATTError

```
[Serializable]
public enum CBATTError {
        Success,
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

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBATTRequest" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBATTRequest

```
public class CBATTRequest : MonoTouch.Foundation.NSObject {
        
        public CBATTRequest ();
        public CBATTRequest (MonoTouch.Foundation.NSCoder coder);
        public CBATTRequest (MonoTouch.Foundation.NSObjectFlag t);
        public CBATTRequest (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual CBCentral Central {
                get;
        }
        public virtual CBCharacteristic Characteristic {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int Offset {
                get;
        }
        public virtual MonoTouch.Foundation.NSData Value {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBATTRequestEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBATTRequestEventArgs

```
public class CBATTRequestEventArgs : EventArgs {
        
        public CBATTRequestEventArgs (CBATTRequest request);
        
        public CBATTRequest Request {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBATTRequestsEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBATTRequestsEventArgs

```
public class CBATTRequestsEventArgs : EventArgs {
        
        public CBATTRequestsEventArgs (CBATTRequest[] requests);
        
        public CBATTRequest[] Requests {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBAdvertisement" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBAdvertisement

Removed:

```
public class CBAdvertisement {
        
        public CBAdvertisement ();
```

Added:

```
public static class CBAdvertisement {
        public static MonoTouch.Foundation.NSString DataOverflowServiceUUIDsKey {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBAttributePermissions" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBAttributePermissions

```
[Serializable]
[Flags]
public enum CBAttributePermissions {
        Readable,
        Writeable,
        ReadEncryptionRequired,
        WriteEncryptionRequired
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCentral" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCentral

```
public class CBCentral : MonoTouch.Foundation.NSObject {
        
        public CBCentral (MonoTouch.Foundation.NSCoder coder);
        public CBCentral (MonoTouch.Foundation.NSObjectFlag t);
        public CBCentral (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual IntPtr UUID {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentralManager" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Removed:

```
public CBCentralManager (CBCentralManagerDelegate cbDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
```

Added:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
        public static MonoTouch.Foundation.NSString OptionNotifyOnConnectionKey {
                get;
        }
        public static MonoTouch.Foundation.NSString OptionNotifyOnNotificationKey {
                get;
        }
        
        public event EventHandler<CBPeripheralEventArgs> ConnectedPeripheral;
        public event EventHandler<CBPeripheralErrorEventArgs> DisconnectedPeripheral;
        public event EventHandler<CBDiscoveredPeripheralEventArgs> DiscoveredPeripheral;
        public event EventHandler<CBPeripheralErrorEventArgs> FailedToConnectPeripheral;
        public event EventHandler<CBPeripheralsEventArgs> RetrievedConnectedPeripherals;
        public event EventHandler<CBPeripheralsEventArgs> RetrievedPeripherals;
        public event EventHandler UpdatedState;
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentralManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate

Removed:

```
public abstract void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);
        public abstract void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public abstract void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
        public abstract void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public abstract void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
        public abstract void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
```

Added:

```
public virtual void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);
        public virtual void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public virtual void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
        public virtual void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        public virtual void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
        public virtual void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBCharacteristicEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBCharacteristicEventArgs

```
public class CBCharacteristicEventArgs : EventArgs {
        
        public CBCharacteristicEventArgs (CBCharacteristic characteristic, MonoTouch.Foundation.NSError error);
        
        public CBCharacteristic Characteristic {
                get;
                set;
        }
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCharacteristicProperties" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBCharacteristicProperties

Added:

```
NotifyEncryptionRequired,
        IndicateEncryptionRequired
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBDescriptorEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBDescriptorEventArgs

```
public class CBDescriptorEventArgs : EventArgs {
        
        public CBDescriptorEventArgs (CBDescriptor descriptor, MonoTouch.Foundation.NSError error);
        
        public CBDescriptor Descriptor {
                get;
                set;
        }
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBDiscoveredPeripheralEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBDiscoveredPeripheralEventArgs

```
public class CBDiscoveredPeripheralEventArgs : EventArgs {
        
        public CBDiscoveredPeripheralEventArgs (CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
        
        public MonoTouch.Foundation.NSDictionary AdvertisementData {
                get;
                set;
        }
        public CBPeripheral Peripheral {
                get;
                set;
        }
        public MonoTouch.Foundation.NSNumber RSSI {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBError" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBError

Removed:

```
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
```

Added:

```
Unknown,
        InvalidParameters,
        NotConnected,
        OutOfSpace,
        OperationCancelled,
        ConnectionTimeout,
        PeripheralDisconnected,
        UUIDNotAllowed,
        AlreadyAdvertising
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBMutableCharacteristic" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBMutableCharacteristic

```
public class CBMutableCharacteristic : CBCharacteristic {
        
        public CBMutableCharacteristic ();
        public CBMutableCharacteristic (MonoTouch.Foundation.NSCoder coder);
        public CBMutableCharacteristic (MonoTouch.Foundation.NSObjectFlag t);
        public CBMutableCharacteristic (IntPtr handle);
        public CBMutableCharacteristic (CBUUID uuid, CBCharacteristicProperties properties, MonoTouch.Foundation.NSData value, CBAttributePermissions permissions);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CBDescriptor[] Descriptors {
                get;
                set;
        }
        public virtual CBAttributePermissions Permissions {
                get;
                set;
        }
        public virtual CBCharacteristicProperties Properties {
                get;
                set;
        }
        public virtual CBUUID UUID {
                get;
        }
        public virtual MonoTouch.Foundation.NSData Value {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBMutableDescriptor" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBMutableDescriptor

```
public class CBMutableDescriptor : CBDescriptor {
        
        public CBMutableDescriptor ();
        public CBMutableDescriptor (MonoTouch.Foundation.NSCoder coder);
        public CBMutableDescriptor (MonoTouch.Foundation.NSObjectFlag t);
        public CBMutableDescriptor (IntPtr handle);
        public CBMutableDescriptor (CBUUID uuid, IntPtr descriptorValue);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBMutableService" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBMutableService

```
public class CBMutableService : CBService {
        
        public CBMutableService ();
        public CBMutableService (MonoTouch.Foundation.NSCoder coder);
        public CBMutableService (MonoTouch.Foundation.NSObjectFlag t);
        public CBMutableService (IntPtr handle);
        public CBMutableService (CBUUID uuid, bool primary);
        
        protected override void Dispose (bool disposing);
        
        public virtual CBCharacteristic[] Characteristics {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual CBService[] IncludedServices {
                get;
                set;
        }
        public virtual bool Primary {
                get;
                set;
        }
        public virtual CBUUID UUID {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBPeripheral" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Removed:

```
public virtual void SetNotifyValue (bool notifyValue, CBCharacteristic characteristic);
```

Added:

```
public virtual void SetNotifyValue (bool enabled, CBCharacteristic characteristic);
        
        public event EventHandler<CBServiceEventArgs> DiscoverCharacteristic;
        public event EventHandler<CBCharacteristicEventArgs> DiscoveredDescriptor;
        public event EventHandler<CBServiceEventArgs> DiscoveredIncludedService;
        public event System.EventHandler<MonoTouch.Foundation.NSErrorEventArgs> DiscoveredService;
        public event EventHandler InvalidatedService;
        public event System.EventHandler<MonoTouch.Foundation.NSErrorEventArgs> RssiUpdated;
        public event EventHandler<CBCharacteristicEventArgs> UpdatedCharacterteristicValue;
        public event EventHandler UpdatedName;
        public event EventHandler<CBCharacteristicEventArgs> UpdatedNotificationState;
        public event EventHandler<CBDescriptorEventArgs> UpdatedValue;
        public event EventHandler<CBCharacteristicEventArgs> WroteCharacteristicValue;
        public event EventHandler<CBDescriptorEventArgs> WroteDescriptorValue;
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBPeripheralDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate

Added:

```
public virtual void InvalidatedService (CBPeripheral peripheral);
        public virtual void UpdatedName (CBPeripheral peripheral);
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralErrorEventArgs

```
public class CBPeripheralErrorEventArgs : EventArgs {
        
        public CBPeripheralErrorEventArgs (CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
        public CBPeripheral Peripheral {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralEventArgs

```
public class CBPeripheralEventArgs : EventArgs {
        
        public CBPeripheralEventArgs (CBPeripheral peripheral);
        
        public CBPeripheral Peripheral {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralManager" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManager

```
public class CBPeripheralManager : MonoTouch.Foundation.NSObject {
        
        public CBPeripheralManager ();
        public CBPeripheralManager (MonoTouch.Foundation.NSCoder coder);
        public CBPeripheralManager (MonoTouch.Foundation.NSObjectFlag t);
        public CBPeripheralManager (IntPtr handle);
        public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
        
        public virtual void AddService (CBMutableService service);
        protected override void Dispose (bool disposing);
        public virtual void RemoveAllServices ();
        public virtual void RemoveService (CBMutableService service);
        public virtual void RespondToRequest (CBATTRequest request, CBATTError result);
        public virtual void SetDesiredConnectionLatency (CBPeripheralManagerConnectionLatency latency, CBCentral connectedCentral);
        public void StartAdvertising (StartAdvertisingOptions options);
        public virtual void StopAdvertising ();
        public virtual bool UpdateValue (MonoTouch.Foundation.NSData value, CBMutableCharacteristic characteristic, CBCentral[] subscribedCentrals);
        
        public virtual bool Advertising {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public CBPeripheralManagerDelegate Delegate {
                get;
                set;
        }
        public virtual CBPeripheralManagerState State {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event System.EventHandler<monotouch.foundation.nserroreventargs> AdvertisingStarted;
        public event EventHandler<cbperipheralmanagersubscriptioneventargs> CharacteristicSubscribed;
        public event EventHandler<cbperipheralmanagersubscriptioneventargs> CharacteristicUnsubscribed;
        public event EventHandler<cbattrequesteventargs> ReadRequestReceived;
        public event EventHandler ReadyToUpdateSubscribers;
        public event EventHandler<cbperipheralmanagerserviceeventargs> ServiceAdded;
        public event EventHandler StateUpdated;
        public event EventHandler<cbattrequestseventargs> WriteRequestsReceived;
}
</cbattrequestseventargs></cbperipheralmanagerserviceeventargs></cbattrequesteventargs></cbperipheralmanagersubscriptioneventargs></cbperipheralmanagersubscriptioneventargs></monotouch.foundation.nserroreventargs>
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralManagerConnectionLatency" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerConnectionLatency

```
[Serializable]
public enum CBPeripheralManagerConnectionLatency {
        Low,
        Medium,
        High
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate

```
public abstract class CBPeripheralManagerDelegate : MonoTouch.Foundation.NSObject {
        
        public CBPeripheralManagerDelegate ();
        public CBPeripheralManagerDelegate (MonoTouch.Foundation.NSCoder coder);
        public CBPeripheralManagerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public CBPeripheralManagerDelegate (IntPtr handle);
        
        public virtual void AdvertisingStarted (CBPeripheralManager peripheral, MonoTouch.Foundation.NSError error);
        public virtual void CharacteristicSubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
        public virtual void CharacteristicUnsubscribed (CBPeripheralManager peripheral, CBCentral central, CBCharacteristic characteristic);
        public virtual void ReadRequestReceived (CBPeripheralManager peripheral, CBATTRequest request);
        public virtual void ReadyToUpdateSubscribers (CBPeripheralManager peripheral);
        public virtual void ServiceAdded (CBPeripheralManager peripheral, CBService service, MonoTouch.Foundation.NSError error);
        public abstract void StateUpdated (CBPeripheralManager peripheral);
        public virtual void WriteRequestsReceived (CBPeripheralManager peripheral, CBATTRequest[] requests);
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralManagerServiceEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerServiceEventArgs

```
public class CBPeripheralManagerServiceEventArgs : EventArgs {
        
        public CBPeripheralManagerServiceEventArgs (CBService service, MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
        public CBService Service {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralManagerState" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerState

```
[Serializable]
public enum CBPeripheralManagerState {
        Unknown,
        Resetting,
        Unsupported,
        Unauthorized,
        PoweredOff,
        PoweredOn
}
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs 

```
public class CBPeripheralManagerSubscriptionEventArgs : EventArgs {
        
        public CBPeripheralManagerSubscriptionEventArgs (CBCentral central, CBCharacteristic characteristic);
        
        public CBCentral Central {
                get;
                set;
        }
        public CBCharacteristic Characteristic {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBPeripheralsEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBPeripheralsEventArgs

```
public class CBPeripheralsEventArgs : EventArgs {
        
        public CBPeripheralsEventArgs (CBPeripheral[] peripherals);
        
        public CBPeripheral[] Peripherals {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBService" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBService

Added:

```
public virtual bool Primary {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.CBServiceEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.CBServiceEventArgs

```
public class CBServiceEventArgs : EventArgs {
        
        public CBServiceEventArgs (CBService service, MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
        public CBService Service {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreBluetooth.StartAdvertisingOptions" class="injected"></a>


## New Type: MonoTouch.CoreBluetooth.StartAdvertisingOptions

```
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
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="New_Type:_MonoTouch.CoreFoundation.CFAllocator" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFAllocator

```
public class CFAllocator : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CFAllocator (IntPtr handle);
        public CFAllocator (IntPtr handle, bool owns);
        
        public IntPtr Allocate (long size, CFAllocatorFlags hint);
        public void Deallocate (IntPtr ptr);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public static CFAllocator Default {
                get;
        }
        public static CFAllocator Malloc {
                get;
        }
        public static CFAllocator MallocZone {
                get;
        }
        public static CFAllocator Null {
                get;
        }
        public static CFAllocator SystemDefault {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFAllocatorFlags" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFAllocatorFlags

```
[Serializable]
[Flags]
public enum CFAllocatorFlags : ulong {
        GCScannedMemory,
        GCObjectMemory
}
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFPage" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFPage

Added:

```
public CGPDFPage (IntPtr handle);
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIContext" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIContext

Removed:

```
public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
```

Added:

```
[Obsolete("Use DrawImage (CIImage, RectangleF, RectangleF) instead")]
        public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIDetector" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIDetector

Added:

```
public static CIDetector CreateFaceDetector (CIContext context, bool highAccuracy, float minFeatureSize);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFaceFeature" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFaceFeature

Added:

```
public virtual bool HasTrackingFrameCount {
                get;
        }
        public virtual bool HasTrackingId {
                get;
        }
        public virtual int TrackingFrameCount {
                get;
        }
        public virtual int TrackingId {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilter" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilter

Added:

```
public static CIFilter[] FromSerializedXMP (MonoTouch.Foundation.NSData xmpData, System.Drawing.RectangleF extent, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSData SerializedXMP (CIFilter[] filters, System.Drawing.RectangleF extent);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilterInputKey" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilterInputKey

Added:

```
public static MonoTouch.Foundation.NSString Version {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIImage

Removed:

```
public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace c);
        public CIImage (int glTextureName, System.Drawing.SizeF size, bool flag, MonoTouch.CoreGraphics.CGColorSpace cs);
```

Added:

```
public CIImage (MonoTouch.Foundation.NSData d, int bpr, System.Drawing.SizeF size, int f, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        public CIImage (int glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="New_Type:_MonoTouch.CoreLocation.CLActivityType" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLActivityType

```
[Serializable]
public enum CLActivityType {
        Other,
        AutomotiveNavigation,
        Fitness,
        OtherNavigation
}
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLAuthorizationChangedEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLAuthorizationChangedEventArgs

```
public class CLAuthorizationChangedEventArgs : EventArgs {
        
        public CLAuthorizationChangedEventArgs (CLAuthorizationStatus status);
        
        public CLAuthorizationStatus Status {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLAuthroziationChangedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLAuthroziationChangedEventArgs

Removed:

```
public class CLAuthroziationChangedEventArgs : EventArgs {
```

Added:

```
[Obsolete]
public class CLAuthroziationChangedEventArgs : CLAuthorizationChangedEventArgs {
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLError" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLError

Added:

```
DeferredFailed,
        DeferredNotUpdatingLocation,
        DeferredAccuracyTooLow,
        DeferredDistanceFiltered,
        DeferredCanceled
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocation" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocation

Removed:

```
public virtual double Distancefrom (CLLocation location);
```

Added:

```
[Obsolete("Replaced by DistanceFrom")]
        public virtual double Distancefrom (CLLocation location);
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLLocationDistance" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLLocationDistance

```
public static class CLLocationDistance {
        
        public static double FilterNone {
                get;
        }
        public static double MaxDistance {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

Removed:

```
public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
        public static bool RegionMonitoringEnabled {
        public virtual string Purpose {
        public event EventHandler<CLAuthroziationChangedEventArgs> AuthorizationChanged;
```

Added:

```
public virtual void AllowDeferredLocationUpdatesUntil (double distance, double timeout);
        public virtual void DisallowDeferredLocationUpdates ();
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
        public static bool DeferredLocationUpdatesAvailable {
                get;
        }
        public static double MaxTimeInterval {
                get;
        }
        [Obsolete("Replaced by RegionMonitoringAvailable in iOS 6.0")]
        public static bool RegionMonitoringEnabled {
        public virtual CLActivityType ActivityType {
                get;
                set;
        }
        public virtual bool PausesLocationUpdatesAutomatically {
                get;
                set;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual string Purpose {
        public event EventHandler<CLAuthorizationChangedEventArgs> AuthorizationChanged;
        public event System.EventHandler<MonoTouch.Foundation.NSErrorEventArgs> DeferredUpdatesFinished;
        public event EventHandler<CLLocationsUpdatedEventArgs> LocationsUpdated;
        public event EventHandler LocationUpdatesPaused;
        public event EventHandler LocationUpdatesResumed;
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

Removed:

```
public virtual void UpdatedLocation (CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
```

Added:

```
public virtual void DeferredUpdatesFinished (CLLocationManager manager, MonoTouch.Foundation.NSError error);
        public virtual void LocationsUpdated (CLLocationManager manager, CLLocation[] locations);
        public virtual void LocationUpdatesPaused (CLLocationManager manager);
        public virtual void LocationUpdatesResumed (CLLocationManager manager);
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual void UpdatedLocation (CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLLocationsUpdatedEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLLocationsUpdatedEventArgs

```
public class CLLocationsUpdatedEventArgs : EventArgs {
        
        public CLLocationsUpdatedEventArgs (CLLocation[] locations);
        
        public CLLocation[] Locations {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreMedia" class="injected"></a>


# Namespace: MonoTouch.CoreMedia

 <a name="New_Type:_MonoTouch.CoreMedia.CMAudioFormatDescription" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMAudioFormatDescription

```
public class CMAudioFormatDescription : CMFormatDescription {
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMBlockBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMBlockBuffer

Removed:

```
public int CopyDataBytes (uint offsetToData, uint dataLength, IntPtr destination);
```

Added:

```
public static CMBlockBuffer CreateEmpty (uint subBlockCapacity, CMBlockBufferFlags flags, out CMBlockBufferError error);
        public CMBlockBufferError CopyDataBytes (uint offsetToData, uint dataLength, IntPtr destination);
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMBlockBufferError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBlockBufferError

```
[Serializable]
public enum CMBlockBufferError {
        None,
        StructureAllocationFailed,
        BlockAllocationFailed,
        BadCustomBlockSource,
        BadOffsetParameter,
        BadLengthParameter,
        BadPointerParameter,
        EmptyBlockBuffer,
        UnallocatedBlock
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMBlockBufferFlags" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBlockBufferFlags

```
[Serializable]
[Flags]
public enum CMBlockBufferFlags : uint {
        AssureMemoryNow,
        AlwaysCopyData,
        DontOptimizeDepth,
        PermitEmptyReference
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMClock" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMClock

```
public class CMClock : CMClockOrTimebase {
        
        public CMClock (IntPtr handle);
        
        public static ulong ConvertHostTimeToSystemUnits (CMTime hostTime);
        public static CMClock CreateAudioClock (out CMClockError clockError);
        public static CMTime CreateHostTimeFromSystemUnits (ulong hostTime);
        public CMClockError GetAnchorTime (out CMTime clockTime, out CMTime referenceClockTime);
        public void Invalidate ();
        public bool MightDrift (CMClock otherClock);
        
        public static CMClock HostTimeClock {
                get;
        }
        public CMTime CurrentTime {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMClockError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMClockError

```
[Serializable]
public enum CMClockError {
        None,
        MissingRequiredParameter,
        InvalidParameter,
        AllocationFailed,
        UnsupportedOperation
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMClockOrTimebase" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMClockOrTimebase

```
public class CMClockOrTimebase : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CMClockOrTimebase (IntPtr handle);
        
        public static CMTime ConvertTime (CMTime time, CMClockOrTimebase from, CMClockOrTimebase to);
        public static double GetRelativeRate (CMClockOrTimebase clockOrTimebaseA, CMClockOrTimebase clockOrTimebaseB);
        public static CMSyncError GetRelativeRateAndAnchorTime (CMClockOrTimebase clockOrTimebaseA, CMClockOrTimebase clockOrTimebaseB, out double relativeRate, out CMTime timeA, out CMTime timeB);
        public static bool MightDrift (CMClockOrTimebase clockOrTimebaseA, CMClockOrTimebase clockOrTimebaseB);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public IntPtr Handle {
                get;
        }
        public CMTime Time {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMClosedCaptionFormatType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMClosedCaptionFormatType

```
[Serializable]
public enum CMClosedCaptionFormatType : uint {
        CEA608,
        CEA708,
        ATSC
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMFormatDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMFormatDescription

Removed:

```
public System.Drawing.RectangleF GetVideoCleanAperture (bool originIsAtTopLeft);
        public System.Drawing.SizeF GetVideoPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
        public uint MediaSubType {
        public System.Drawing.Size VideoDimensions {
```

Added:

```
public static CMFormatDescription Create (CMMediaType mediaType, uint mediaSubtype, out CMFormatDescriptionError error);
        [Obsolete("Use CMVideoFormatDescription")]
        public System.Drawing.RectangleF GetVideoCleanAperture (bool originIsAtTopLeft);
        [Obsolete("Use CMVideoFormatDescription")]
        public System.Drawing.SizeF GetVideoPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
        public CMClosedCaptionFormatType ClosedCaptionFormatType {
                get;
        }
        [Obsolete("Use specific SubType property")]
        public uint MediaSubType {
        public CMMetadataFormatType MetadataFormatType {
                get;
        }
        public CMMuxedStreamType MuxedStreamType {
                get;
        }
        public CMSubtitleFormatType SubtitleFormatType {
                get;
        }
        public CMTimeCodeFormatType TimeCodeFormatType {
                get;
        }
        public CMVideoCodecType VideoCodecType {
                get;
        }
        [Obsolete("Use CMVideoFormatDescription")]
        public System.Drawing.Size VideoDimensions {
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMFormatDescriptionError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMFormatDescriptionError

```
[Serializable]
public enum CMFormatDescriptionError {
        None,
        InvalidParameter,
        AllocationFailed
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMMediaType" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMMediaType

Added:

```
Metadata
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMMemoryPool" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMMemoryPool

```
public class CMMemoryPool : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CMMemoryPool ();
        public CMMemoryPool (TimeSpan ageOutPeriod);
        
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public void Flush ();
        public MonoTouch.CoreFoundation.CFAllocator GetAllocator ();
        public void Invalidate ();
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMMetadataFormatType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMMetadataFormatType

```
[Serializable]
public enum CMMetadataFormatType : uint {
        ICY,
        ID3,
        Boxed
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMMuxedStreamType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMMuxedStreamType

```
[Serializable]
public enum CMMuxedStreamType : uint {
        MPEG1System,
        MPEG2Transport,
        MPEG2Program,
        DV
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMSampleBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMSampleBuffer

Removed:

```
public CMFormatDescription GetFormatDescription ();
        public MonoTouch.Foundation.NSMutableDictionary[] GetSampleAttachments (bool createIfNecessary);
```

Added:

```
public static CMSampleBuffer CreateForImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, bool dataReady, CMVideoFormatDescription formatDescription, CMSampleTimingInfo sampleTiming, out CMSampleBufferError error);
        public static CMSampleBuffer CreateWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, MonoTouch.AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
        public CMAudioFormatDescription GetAudioFormatDescription ();
        [Obsolete("Use GetAudioFormatDescription or GetVideoFormatDescription")]
        public CMFormatDescription GetFormatDescription ();
        public CMSampleBufferAttachmentSettings[] GetSampleAttachments (bool createIfNecessary);
        public CMVideoFormatDescription GetVideoFormatDescription ();
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMSampleBufferAttachmentSettings" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMSampleBufferAttachmentSettings

```
public class CMSampleBufferAttachmentSettings : MonoTouch.Foundation.DictionaryContainer {
        
        public Nullable<bool> DependedOnByOthers {
                get;
                set;
        }
        public Nullable<bool> DependsOnOthers {
                get;
                set;
        }
        public Nullable<bool> DisplayEmptyMediaImmediately {
                get;
                set;
        }
        public Nullable<bool> DisplayImmediately {
                get;
                set;
        }
        public Nullable<bool> DoNotDisplay {
                get;
                set;
        }
        public Nullable<bool> DrainAfterDecoding {
                get;
                set;
        }
        public string DroppedFrameReason {
                get;
        }
        public Nullable<bool> EarlierDisplayTimesAllowed {
                get;
                set;
        }
        public Nullable<bool> EmptyMedia {
                get;
                set;
        }
        public Nullable<bool> EndsPreviousSampleDuration {
                get;
                set;
        }
        public Nullable<bool> FillDiscontinuitiesWithSilence {
                get;
                set;
        }
        public Nullable<bool> NotSync {
                get;
                set;
        }
        public Nullable<bool> PartialSync {
                get;
                set;
        }
        public Nullable<bool> PermanentEmptyMedia {
                get;
                set;
        }
        public Nullable<bool> RedundantCoding {
                get;
                set;
        }
        public Nullable<bool> ResetDecoderBeforeDecoding {
                get;
                set;
        }
        public Nullable<bool> Reverse {
                get;
                set;
        }
}
</bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool>
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMSampleBufferError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMSampleBufferError

```
[Serializable]
public enum CMSampleBufferError {
        None,
        AllocationFailed,
        RequiredParameterMissing,
        AlreadyHasDataBuffer,
        BufferNotReady,
        SampleIndexOutOfRange,
        BufferHasNoSampleSizes,
        BufferHasNoSampleTimingInfo,
        ArrayTooSmall,
        InvalidEntryCount,
        CannotSubdivide,
        SampleTimingInfoInvalid,
        InvalidMediaTypeForOperation,
        InvalidSampleData,
        InvalidMediaFormat,
        Invalidated
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMSampleTimingInfo" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMSampleTimingInfo

```
public struct CMSampleTimingInfo {
        
        public CMTime Duration;
        public CMTime PresentationTimeStamp;
        public CMTime DecodeTimeStamp;
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMSubtitleFormatType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMSubtitleFormatType

```
[Serializable]
public enum CMSubtitleFormatType : uint {
        Text3G,
        WebVTT
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMSyncError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMSyncError

```
[Serializable]
public enum CMSyncError {
        None,
        MissingRequiredParameter,
        InvalidParameter,
        AllocationFailed,
        RateMustBeNonZero
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTextMarkupAttributes" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTextMarkupAttributes

```
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
</bool></int></bool></textmarkupcolor></bool></textmarkupcolor>
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTimeCodeFormatType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimeCodeFormatType

```
[Serializable]
public enum CMTimeCodeFormatType : uint {
        TimeCode32,
        TimeCode64,
        Counter32,
        Counter64
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTimeScale" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimeScale

```
public struct CMTimeScale {
        
        public CMTimeScale (int value);
        
        public static readonly CMTimeScale MaxValue;
        public int Value;
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTimebase" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimebase

```
public class CMTimebase : CMClockOrTimebase {
        
        public CMTimebase (IntPtr handle);
        public CMTimebase (CMClock masterClock);
        public CMTimebase (CMTimebase masterTimebase);
        
        public CMTimebaseError AddTimer (MonoTouch.Foundation.NSTimer timer, MonoTouch.Foundation.NSRunLoop runloop);
        public CMClockOrTimebase GetMaster ();
        public CMClock GetMasterClock ();
        public CMTimebase GetMasterTimebase ();
        public CMTime GetTime (CMTimeScale timeScale, CMTimeRoundingMethod roundingMethod);
        public CMTimebaseError GetTimeAndRate (out CMTime time, out double rate);
        public CMClock GetUltimateMasterClock ();
        public CMTimebaseError NotificationBarrier ();
        public CMTimebaseError RemoveTimer (MonoTouch.Foundation.NSTimer timer);
        public CMTimebaseError SetAnchorTime (CMTime timebaseTime, CMTime immediateMasterTime);
        public CMTimebaseError SetRateAndAnchorTime (double rate, CMTime timebaseTime, CMTime immediateMasterTime);
        public CMTimebaseError SetTimerNextFireTime (MonoTouch.Foundation.NSTimer timer, CMTime fireTime);
        public CMTimebaseError SetTimerToFireImmediately (MonoTouch.Foundation.NSTimer timer);
        
        public double EffectiveRate {
                get;
        }
        public double Rate {
                get;
                set;
        }
        public CMTime Time {
                get;
                set;
        }
        
        public const double VeryLongTimeInterval = 8073216000;
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMTimebaseError" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMTimebaseError

```
[Serializable]
public enum CMTimebaseError {
        None,
        MissingRequiredParameter,
        InvalidParameter,
        AllocationFailed,
        TimerIntervalTooShort,
        ReadOnly
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMVideoFormatDescription" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMVideoFormatDescription

```
public class CMVideoFormatDescription : CMFormatDescription {
        
        public CMVideoFormatDescription (CMVideoCodecType codecType, System.Drawing.Size size);
        
        public static CMVideoFormatDescription CreateForImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, out CMFormatDescriptionError error);
        public System.Drawing.RectangleF GetCleanAperture (bool originIsAtTopLeft);
        public System.Drawing.SizeF GetPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
        
        public System.Drawing.Size Dimensions {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMedia.TextMarkupColor" class="injected"></a>


## New Type: MonoTouch.CoreMedia.TextMarkupColor

```
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
```

 <a name="Namespace:_MonoTouch.CoreMidi" class="injected"></a>


# Namespace: MonoTouch.CoreMidi

 <a name="Type_Changed:_MonoTouch.CoreMidi.MidiError" class="injected"></a>


## Type Changed: MonoTouch.CoreMidi.MidiError

Added:

```
NotPermitted
```

 <a name="Namespace:_MonoTouch.CoreTelephony" class="injected"></a>


# Namespace: MonoTouch.CoreTelephony

 <a name="New_Type:_MonoTouch.CoreTelephony.CTErrorDomain" class="injected"></a>


## New Type: MonoTouch.CoreTelephony.CTErrorDomain

```
[Serializable]
public enum CTErrorDomain {
        NoError,
        Posix,
        Mach
}
```

 <a name="Namespace:_MonoTouch.CoreText" class="injected"></a>


# Namespace: MonoTouch.CoreText

 <a name="New_Type:_MonoTouch.CoreText.CTBaselineClass" class="injected"></a>


## New Type: MonoTouch.CoreText.CTBaselineClass

```
[Serializable]
public enum CTBaselineClass {
        Roman,
        IdeographicCentered,
        IdeographicLow,
        IdeographicHigh,
        Hanging,
        Math
}
```

 <a name="New_Type:_MonoTouch.CoreText.CTBaselineFont" class="injected"></a>


## New Type: MonoTouch.CoreText.CTBaselineFont

```
[Serializable]
public enum CTBaselineFont {
        Reference,
        Original
}
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFont" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFont

Added:

```
public CTFontDescriptor[] GetDefaultCascadeList (string [] languages);
        public System.Drawing.RectangleF GetOpticalBounds (ushort [] glyphs, System.Drawing.RectangleF [] boundingRects, int count, CTFontOptions options);
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontDescriptor" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontDescriptor

Added:

```
public static bool MatchFontDescriptors (CTFontDescriptor[] descriptors, MonoTouch.Foundation.NSSet mandatoryAttributes, Func<CTFontDescriptorMatchingState,IntPtr,bool> progressHandler);
```

 <a name="New_Type:_MonoTouch.CoreText.CTFontDescriptorMatchingState" class="injected"></a>


## New Type: MonoTouch.CoreText.CTFontDescriptorMatchingState

```
[Serializable]
public enum CTFontDescriptorMatchingState : uint {
        Started,
        Finished,
        WillBeginQuerying,
        Stalled,
        WillBeginDownloading,
        Downloading,
        DownloadingFinished,
        Matched,
        FailedWithError
}
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontManager" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontManager

Added:

```
public static bool RegisterGraphicsFont (MonoTouch.CoreGraphics.CGFont font, out MonoTouch.Foundation.NSError error);
        public static bool UnregisterGraphicsFont (MonoTouch.CoreGraphics.CGFont font, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontSymbolicTraits" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontSymbolicTraits

Added:

```
Composite,
        Mask
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontTable" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontTable

Added:

```
AnchorPoints
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTLine" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTLine

Added:

```
public System.Drawing.RectangleF GetBounds (CTLineBoundsOptions options);
```

 <a name="New_Type:_MonoTouch.CoreText.CTLineBoundsOptions" class="injected"></a>


## New Type: MonoTouch.CoreText.CTLineBoundsOptions

```
[Serializable]
public enum CTLineBoundsOptions {
        ExcludeTypographicLeading,
        ExcludeTypographicShifts,
        UseHangingPunctuation,
        UseGlyphPathBounds,
        UseOpticalBounds
}
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTStringAttributes" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTStringAttributes

Added:

```
public void SetBaselineInfo (CTBaselineClass baselineClass, double offset);
        public void SetBaselineReferenceInfo (CTBaselineClass baselineClass, double offset);
        public void SetWritingDirection (params CTWritingDirection[] writingDirections);
        
        public Nullable<CTBaselineClass> BaselineClass {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTTypesetterOptionKey" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTTypesetterOptionKey

Removed:

```
public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTTypesetterOptions" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTTypesetterOptions

Removed:

```
public bool DisableBidiProcessing {
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public bool DisableBidiProcessing {
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTWritingDirection" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTWritingDirection

Added:

```
[Flags]
        Embedding,
        Override
```

 <a name="Namespace:_MonoTouch.CoreVideo" class="injected"></a>


# Namespace: MonoTouch.CoreVideo

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVImageBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVImageBuffer

Added:

```
public MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                get;
        }
        public bool IsFlipped {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVPixelBuffer" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVPixelBuffer

Removed:

```
public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
```

Added:

```
public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormat);
        public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);
        [Obsolete("Use constructor with CVPixelBufferAttributes")]
        public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
        public static readonly MonoTouch.Foundation.NSString OpenGLESCompatibilityKey;
```

 <a name="New_Type:_MonoTouch.CoreVideo.CVPixelBufferAttributes" class="injected"></a>


## New Type: MonoTouch.CoreVideo.CVPixelBufferAttributes

```
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
</int></int></cvpixelformattype></bool></bool></int></int></int></int></int></bool></bool></int>
```

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVPixelFormatType" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVPixelFormatType

Added:

```
OneComponent16Half,
        OneComponent32Float,
        TwoComponent16Half,
        TwoComponent32Float,
        CV64RGBAHalf,
        CV128RGBAFloat
```

 <a name="Type_Changed:_MonoTouch.CoreVideo.CVReturn" class="injected"></a>


## Type Changed: MonoTouch.CoreVideo.CVReturn

Added:

```
WouldExceedAllocationThreshold,
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKAlarm" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKAlarm

Added:

```
public virtual EKAlarmProximity Proximity {
                get;
                set;
        }
        public virtual EKStructuredLocation StructuredLocation {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.EventKit.EKAlarmProximity" class="injected"></a>


## New Type: MonoTouch.EventKit.EKAlarmProximity

```
[Serializable]
public enum EKAlarmProximity {
        None,
        Enter,
        Leave
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKAuthorizationStatus" class="injected"></a>


## New Type: MonoTouch.EventKit.EKAuthorizationStatus

```
[Serializable]
public enum EKAuthorizationStatus {
        NotDetermined,
        Restricted,
        Denied,
        Authorized
}
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKCalendar" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKCalendar

Removed:

```
public static EKCalendar FromEventStore (EKEventStore eventStore);
```

Added:

```
public static EKCalendar Create (EKEntityType entityType, EKEventStore eventStore);
        [Obsolete("Deprecated in iOS 6.0, use Create(EKEntityType, EKEventStore) instead")]
        public static EKCalendar FromEventStore (EKEventStore eventStore);
        public virtual EKEntityMask AllowedEntityTypes {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKCalendarItem" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKCalendarItem

Removed:

```
public virtual string UUID {
```

Added:

```
public virtual string CalendarItemExternalIdentifier {
                get;
        }
        public virtual string CalendarItemIdentifier {
                get;
        }
        [Obsolete("Method obsoleted in iOS 6.0")]
        public virtual string UUID {
```

 <a name="New_Type:_MonoTouch.EventKit.EKEntityMask" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEntityMask

```
[Serializable]
[Flags]
public enum EKEntityMask {
        Event,
        Reminder
}
```

 <a name="New_Type:_MonoTouch.EventKit.EKEntityType" class="injected"></a>


## New Type: MonoTouch.EventKit.EKEntityType

```
[Serializable]
public enum EKEntityType {
        Event,
        Reminder
}
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKErrorCode" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKErrorCode

Added:

```
RecurringReminderRequiresDueDate,
        StructuredLocationsNotSupported,
        ReminderLocationsNotSupported,
        AlarmProximityNotSupported,
        CalendarDoesNotAllowEvents,
        CalendarDoesNotAllowReminders,
        SourceDoesNotAllowReminders,
        PriorityIsInvalid,
        InvalidEntityType
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEvent

Removed:

```
public virtual EKRecurrenceRule RecurrenceRule {
```

Added:

```
[Obsolete("Removed in iOS 6.0")]
        public virtual EKRecurrenceRule RecurrenceRule {
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

Removed:

```
public virtual bool RemoveCalendarc (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual EKCalendar[] Calendars {
```

Added:

```
public static EKAuthorizationStatus GetAuthorizationStatus (EKEntityType entityType);
        public virtual void CancelFetchRequest (IntPtr fetchIdentifier);
        public virtual IntPtr FetchReminders (MonoTouch.Foundation.NSPredicate predicate, Action<EKReminder[]> completion);
        public virtual EKCalendarItem GetCalendarItem (string identifier);
        public virtual EKCalendarItem[] GetCalendarItems (string externalIdentifier);
        public virtual EKCalendar[] GetCalendars (EKEntityType entityType);
        public virtual MonoTouch.Foundation.NSPredicate PredicateForCompleteReminders (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
        public virtual MonoTouch.Foundation.NSPredicate PredicateForIncompleteReminders (MonoTouch.Foundation.NSDate startDate, MonoTouch.Foundation.NSDate endDate, EKCalendar[] calendars);
        public virtual MonoTouch.Foundation.NSPredicate PredicateForReminders (EKCalendar[] calendars);
        public virtual bool RemoveCalendar (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
        [Obsolete("Replaced by RemoveCalendar")]
        public bool RemoveCalendarc (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual bool RemoveReminder (EKReminder reminder, bool commit, out MonoTouch.Foundation.NSError error);
        public virtual void RequestAccess (EKEntityType entityType, System.Action<bool,MonoTouch.Foundation.NSError> completionHandler);
        public virtual bool SaveReminder (EKReminder reminder, bool commit, out MonoTouch.Foundation.NSError error);
        [Obsolete("Replaced by GetCalendars in iOS 6.0")]
        public virtual EKCalendar[] Calendars {
        public virtual EKCalendar DefaultCalendarForNewReminders {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKParticipant" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKParticipant

Added:

```
public virtual bool IsCurrentUser {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKRecurrenceDayOfWeek" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKRecurrenceDayOfWeek

Removed:

```
public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek);
        public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek, int weekNumber);
```

Added:

```
public static EKRecurrenceDayOfWeek FromDay (EKDay dayOfTheWeek);
        public static EKRecurrenceDayOfWeek FromDay (EKDay dayOfTheWeek, int weekNumber);
```

 <a name="New_Type:_MonoTouch.EventKit.EKReminder" class="injected"></a>


## New Type: MonoTouch.EventKit.EKReminder

```
public class EKReminder : EKCalendarItem {
        
        public EKReminder ();
        public EKReminder (MonoTouch.Foundation.NSCoder coder);
        public EKReminder (MonoTouch.Foundation.NSObjectFlag t);
        public EKReminder (IntPtr handle);
        
        public static EKReminder Create (EKEventStore eventStore);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Completed {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDate CompletionDate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDateComponents DueDateComponents {
                get;
                set;
        }
        public virtual int Priority {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDateComponents StartDateComponents {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKSource" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKSource

Removed:

```
public virtual MonoTouch.Foundation.NSSet Calendars {
```

Added:

```
public virtual MonoTouch.Foundation.NSSet GetCalendars (EKEntityType entityType);
        [Obsolete("Replaced by GetCalendars in iOS 6.0")]
        public virtual MonoTouch.Foundation.NSSet Calendars {
```

 <a name="New_Type:_MonoTouch.EventKit.EKStructuredLocation" class="injected"></a>


## New Type: MonoTouch.EventKit.EKStructuredLocation

```
public class EKStructuredLocation : EKObject {
        
        public EKStructuredLocation ();
        public EKStructuredLocation (MonoTouch.Foundation.NSCoder coder);
        public EKStructuredLocation (MonoTouch.Foundation.NSObjectFlag t);
        public EKStructuredLocation (IntPtr handle);
        
        public static EKStructuredLocation FromTitle (string title);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocation GeoLocation {
                get;
                set;
        }
        public virtual double Radius {
                get;
                set;
        }
        public virtual string Title {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


# Namespace: MonoTouch.EventKitUI

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKCalendarChooser" class="injected"></a>


## Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added:

```
public EKCalendarChooser (EKCalendarChooserSelectionStyle selectionStyle, EKCalendarChooserDisplayStyle displayStyle, MonoTouch.EventKit.EKEntityType entityType, MonoTouch.EventKit.EKEventStore eventStore);
```

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKEventEditViewController" class="injected"></a>


## Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added:

```
public virtual void CancelEditing ();
```

 <a name="Namespace:_MonoTouch.ExternalAccessory" class="injected"></a>


# Namespace: MonoTouch.ExternalAccessory

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryEventArgs" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryEventArgs

Added:

```
public EAAccessory Selected {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryManager" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager

Added:

```
public virtual void ShowBluetoothAccessoryPicker (MonoTouch.Foundation.NSPredicate predicate, System.Action<MonoTouch.Foundation.NSError> completion);
        public static MonoTouch.Foundation.NSString BluetoothAccessoryPickerErrorDomain {
                get;
        }
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="New_Type:_MonoTouch.Foundation.DictionaryContainer" class="injected"></a>


## New Type: MonoTouch.Foundation.DictionaryContainer

```
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
</long></int></uint></float></double></bool></uint></long></int></float></double></bool></t>
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSArray" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSArray

Added:

```
public static NSArray FromNSObjects (int count, params NSObject[] items);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

Added:

```
public NSAttributedString (string str, MonoTouch.UIKit.UIStringAttributes attributes);
        public NSAttributedString (string str, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UIColor foregroundColor, MonoTouch.UIKit.UIColor backgroundColor, MonoTouch.UIKit.UIColor strokeColor, MonoTouch.UIKit.NSParagraphStyle paragraphStyle, NSLigatureType ligatures, float kerning, NSUnderlineStyle underlineStyle, MonoTouch.UIKit.NSShadow shadow, float strokeWidth, NSUnderlineStyle strikethroughStyle);
        public virtual void DrawString (System.Drawing.PointF point);
        public virtual void DrawString (System.Drawing.RectangleF rect);
        public virtual void DrawString (System.Drawing.RectangleF rect, NSStringDrawingOptions options, NSStringDrawingContext context);
        public virtual System.Drawing.RectangleF GetBoundingRect (System.Drawing.SizeF size, NSStringDrawingOptions options, NSStringDrawingContext context);
        public MonoTouch.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange effectiveRange);
        public MonoTouch.CoreText.CTStringAttributes GetCoreTextAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
        public MonoTouch.UIKit.UIStringAttributes GetUIKitAttributes (int location, out NSRange effectiveRange);
        public MonoTouch.UIKit.UIStringAttributes GetUIKitAttributes (int location, out NSRange longestEffectiveRange, NSRange rangeLimit);
        public virtual System.Drawing.SizeF Size {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSByteCountFormatter" class="injected"></a>


## New Type: MonoTouch.Foundation.NSByteCountFormatter

```
public class NSByteCountFormatter : NSFormatter {
        
        public NSByteCountFormatter ();
        public NSByteCountFormatter (NSCoder coder);
        public NSByteCountFormatter (NSObjectFlag t);
        public NSByteCountFormatter (IntPtr handle);
        
        public static string Format (long byteCount, NSByteCountFormatterCountStyle countStyle);
        public virtual string Format (long byteCount);
        
        public virtual bool Adaptive {
                get;
                set;
        }
        public virtual NSByteCountFormatterUnits AllowedUnits {
                get;
                set;
        }
        public virtual bool AllowsNonnumericFormatting {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSByteCountFormatterCountStyle CountStyle {
                get;
                set;
        }
        public virtual bool IncludesActualByteCount {
                get;
                set;
        }
        public virtual bool IncludesCount {
                get;
                set;
        }
        public virtual bool IncludesUnit {
                get;
                set;
        }
        public virtual bool ZeroPadsFractionDigits {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSByteCountFormatterCountStyle" class="injected"></a>


## New Type: MonoTouch.Foundation.NSByteCountFormatterCountStyle

```
[Serializable]
public enum NSByteCountFormatterCountStyle {
        File,
        Memory,
        Decimal,
        Binary
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSByteCountFormatterUnits" class="injected"></a>


## New Type: MonoTouch.Foundation.NSByteCountFormatterUnits

```
[Serializable]
[Flags]
public enum NSByteCountFormatterUnits {
        UseDefault,
        UseBytes,
        UseKB,
        UseMB,
        UseGB,
        UseTB,
        UsePB,
        UseEB,
        UseZB,
        UseYBOrHigher,
        UseAll
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCalendar" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCalendar

Removed:

```
public NSCalendar (string identifier);
```

Added:

```
public NSCalendar (NSCalendarType calendarType);
        public NSCalendar (NSString identifier);
```

 <a name="New_Type:_MonoTouch.Foundation.NSCalendarType" class="injected"></a>


## New Type: MonoTouch.Foundation.NSCalendarType

```
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
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCoder" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCoder

Added:

```
protected override void Dispose (bool disposing);
        public virtual bool RequiresSecureCoding ();
        public virtual NSSet AllowedClasses {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDataWritingOptions" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDataWritingOptions

Added:

```
WithoutOverwriting,
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDateComponents" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDateComponents

Added:

```
public virtual bool IsLeapMonth {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDictionary

Added:

```
public NSDictionary (NSObject first, NSObject second, params NSObject[] args);
        public NSDictionary (object first, object second, params object [] args);
        public static NSObject GetSharedKeySetForKeys (NSObject[] keys);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileCoordinator" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileCoordinator

Added:

```
public virtual void WillMove (NSUrl oldUrl, NSUrl newUrl);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileManager

Added:

```
public static NSString UbiquityIdentityDidChangeNotification {
                get;
        }
        public virtual NSObject UbiquityIdentityToken {
                get;
        }
        
        public static class Notifications {
                
                public static NSObject ObserveUbiquityIdentityDidChange (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSIndexPath" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSIndexPath

Added:

```
public static NSIndexPath FromItemSection (int item, int section);
```

 <a name="New_Type:_MonoTouch.Foundation.NSLigatureType" class="injected"></a>


## New Type: MonoTouch.Foundation.NSLigatureType

```
[Serializable]
public enum NSLigatureType {
        None,
        Default,
        All
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLinguisticTag" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLinguisticTag

Removed:

```
public class NSLinguisticTag {
        
        public NSLinguisticTag ();
```

Added:

```
public static class NSLinguisticTag {
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableAttributedString

Added:

```
public NSMutableAttributedString (string str, MonoTouch.UIKit.UIStringAttributes attributes);
        public NSMutableAttributedString (string str, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UIColor foregroundColor, MonoTouch.UIKit.UIColor backgroundColor, MonoTouch.UIKit.UIColor strokeColor, MonoTouch.UIKit.NSParagraphStyle paragraphStyle, NSLigatureType ligatures, float kerning, NSUnderlineStyle underlineStyle, MonoTouch.UIKit.NSShadow shadow, float strokeWidth, NSUnderlineStyle strikethroughStyle);
        public void Append (NSAttributedString first, params object [] rest);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableDictionary

Added:

```
public static NSDictionary FromSharedKeySet (NSObject sharedKeyToken);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableSet" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableSet

Added:

```
public NSMutableSet (NSObject[] objs);
        public NSMutableSet (params string [] strings);
        public NSMutableSet (NSArray other);
        public NSMutableSet (NSSet other);
        public NSMutableSet (int capacity);
        public virtual void AddObjects (NSObject[] objects);
        public virtual void RemoveAll ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableUrlRequest" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableUrlRequest

Added:

```
public virtual bool AllowsCellularAccess {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

Removed:

```
[Obsolete("Use AcceptInputForMode (NSString, NSDate)")]
        public void AcceptInputForMode (string mode, NSDate limitDate);
        [Obsolete("Use AddTimer (NSTimer, NSString)")]
        public void AddTimer (NSTimer timer, string forMode);
        [Obsolete("Use LimitDateForMode (NSString) instead")]
        public NSDate LimitDateForMode (string mode);
```

Added:

```
[Obsolete("Use AcceptInputForMode (NSRunLoopMode, NSDate)")]
        public void AcceptInputForMode (string mode, NSDate limitDate);
        [Obsolete("Use AddTimer (NSTimer, NSRunLoopMode)")]
        public void AddTimer (NSTimer timer, string forMode);
        [Obsolete("Use LimitDateForMode (NSRunLoopMode) instead")]
        public NSDate LimitDateForMode (string mode);
        public bool RunUntil (NSRunLoopMode mode, NSDate limitDate);
        public static NSString UITrackingRunLoopMode {
                get;
        }
        public NSRunLoopMode CurrentRunLoopMode {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoopMode" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoopMode

Added:

```
UITracking,
        Other
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSSearchPathDirectory" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSSearchPathDirectory

Added:

```
ApplicationScriptsDirectory,
        TrashDirectory
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSSet" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSSet

Removed:

```
public NSSet (NSObject[] objs);
```

Added:

```
public NSSet (params NSObject[] objs);
        public NSSet (params object [] objs);
        public NSSet (NSSet other);
        public bool Contains (object obj);
        public virtual bool IntersectsSet (NSSet other);
        public static NSSet operator + (NSSet first, NSSet second);
        public static NSSet operator - (NSSet first, NSSet second);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

Added:

```
public virtual string Capitalize (NSLocale locale);
        public virtual string ToLower (NSLocale locale);
        public virtual string ToUpper (NSLocale locale);
```

 <a name="New_Type:_MonoTouch.Foundation.NSStringDrawingContext" class="injected"></a>


## New Type: MonoTouch.Foundation.NSStringDrawingContext

```
public class NSStringDrawingContext : NSObject {
        
        public NSStringDrawingContext ();
        public NSStringDrawingContext (NSCoder coder);
        public NSStringDrawingContext (NSObjectFlag t);
        public NSStringDrawingContext (IntPtr handle);
        
        public virtual float ActualScaleFactor {
                get;
        }
        public virtual float ActualTrackingAdjustment {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float MinimumScaleFactor {
                get;
                set;
        }
        public virtual float MinimumTrackingAdjustment {
                get;
                set;
        }
        public virtual System.Drawing.RectangleF TotalBounds {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimer" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimer

Added:

```
[Obsolete("This instance of NSTimer would be unusable. Symbol kept for binary compatibility")]
        public NSTimer ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeReason 

Added:

```
AccountChange
```

 <a name="New_Type:_MonoTouch.Foundation.NSUnderlineStyle" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUnderlineStyle

```
[Serializable]
public enum NSUnderlineStyle {
        None,
        Single
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Added:

```
public NSUrl (NSData bookmarkData, NSUrlBookmarkResolutionOptions resolutionOptions, NSUrl relativeUrl, out bool bookmarkIsStale, out NSError error);
        public virtual NSData CreateBookmarkData (NSUrlBookmarkCreationOptions options, string [] resourceValues, NSUrl relativeUrl, out NSError error);
        public static NSString PathKey {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSUrlBookmarkCreationOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlBookmarkCreationOptions

```
[Serializable]
[Flags]
public enum NSUrlBookmarkCreationOptions {
        PreferFileIDResolution,
        MinimalBookmark,
        SuitableForBookmarkFile,
        WithSecurityScope,
        SecurityScopeAllowOnlyReadAccess
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSUrlBookmarkResolutionOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlBookmarkResolutionOptions

```
[Serializable]
[Flags]
public enum NSUrlBookmarkResolutionOptions {
        WithoutUI,
        WithoutMounting,
        WithSecurityScope
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSUuid" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUuid

```
public class NSUuid : NSObject {
        
        public NSUuid (byte [] bytes);
        public NSUuid ();
        public NSUuid (NSCoder coder);
        public NSUuid (NSObjectFlag t);
        public NSUuid (IntPtr handle);
        public NSUuid (string str);
        
        public virtual string AsString ();
        public byte [] GetBytes ();
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSValue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSValue

Added:

```
public static NSValue FromMKCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D coordinate);
        public static NSValue FromMKCoordinateSpan (MonoTouch.MapKit.MKCoordinateSpan coordinateSpan);
        public virtual MonoTouch.MapKit.MKCoordinateSpan CoordinateSpanValue {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D CoordinateValue {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSWritingDirection" class="injected"></a>


## New Type: MonoTouch.Foundation.NSWritingDirection

```
[Serializable]
public enum NSWritingDirection {
        Natural,
        LeftToRight,
        RightToLeft
}
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

Removed:

```
public static void ResetAchivements (GKNotificationHandler errorHandler);
        public virtual void ReportAchievement (GKNotificationHandler handler);
        public virtual bool Hidden {
```

Added:

```
public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
        public static void ResetAchivements (GKNotificationHandler completionHandler);
        public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
        public virtual void ReportAchievement (GKNotificationHandler completionHandler);
        public virtual void SelectChallengeablePlayerIDs (string [] playerIDs, System.Action<string [],MonoTouch.Foundation.NSError> completionHandler);
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool Hidden {
```

 <a name="New_Type:_MonoTouch.GameKit.GKAchievementChallenge" class="injected"></a>


## New Type: MonoTouch.GameKit.GKAchievementChallenge

```
public class GKAchievementChallenge : GKChallenge {
        
        public GKAchievementChallenge ();
        public GKAchievementChallenge (MonoTouch.Foundation.NSCoder coder);
        public GKAchievementChallenge (MonoTouch.Foundation.NSObjectFlag t);
        public GKAchievementChallenge (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public virtual GKAchievement Achievement {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementDescription

Added:

```
public virtual string GroupIdentifier {
                get;
        }
        public virtual bool Replayable {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementViewController

Removed:

```
public class GKAchievementViewController : MonoTouch.UIKit.UINavigationController {
```

Added:

```
public class GKAchievementViewController : GKGameCenterViewController {
```

 <a name="New_Type:_MonoTouch.GameKit.GKChallenge" class="injected"></a>


## New Type: MonoTouch.GameKit.GKChallenge

```
public class GKChallenge : MonoTouch.Foundation.NSObject {
        
        public GKChallenge ();
        public GKChallenge (MonoTouch.Foundation.NSCoder coder);
        public GKChallenge (MonoTouch.Foundation.NSObjectFlag t);
        public GKChallenge (IntPtr handle);
        
        public static void LoadReceivedChallenges (System.Action<gkchallenge[],monotouch.foundation.nserror> completionHandler);
        public virtual void Decline ();
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate CompletionDate {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate IssueDate {
                get;
        }
        public virtual string IssuingPlayerID {
                get;
        }
        public virtual string Message {
                get;
        }
        public virtual string ReceivingPlayerID {
                get;
        }
        public virtual GKChallengeState State {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKChallengeEventHandler" class="injected"></a>


## New Type: MonoTouch.GameKit.GKChallengeEventHandler

```
public class GKChallengeEventHandler : MonoTouch.Foundation.NSObject {
        
        public GKChallengeEventHandler (MonoTouch.Foundation.NSCoder coder);
        public GKChallengeEventHandler (MonoTouch.Foundation.NSObjectFlag t);
        public GKChallengeEventHandler (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public static GKChallengeEventHandler Instance {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public GKChallengeEventHandlerDelegate Delegate {
                get;
                set;
        }
        public GKChallengePredicate ShouldShowBannerForLocallyCompletedChallenge {
                get;
                set;
        }
        public GKChallengePredicate ShouldShowBannerForLocallyReceivedChallenge {
                get;
                set;
        }
        public GKChallengePredicate ShouldShowBannerForRemotelyCompletedChallenge {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler LocalPlayerCompletedChallenge;
        public event EventHandler LocalPlayerReceivedChallenge;
        public event EventHandler LocalPlayerSelectedChallenge;
        public event EventHandler RemotePlayerCompletedChallenge;
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKChallengeEventHandlerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKChallengeEventHandlerDelegate

```
public class GKChallengeEventHandlerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKChallengeEventHandlerDelegate ();
        public GKChallengeEventHandlerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKChallengeEventHandlerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKChallengeEventHandlerDelegate (IntPtr handle);
        
        public virtual void LocalPlayerCompletedChallenge (GKChallenge challenge);
        public virtual void LocalPlayerReceivedChallenge (GKChallenge challenge);
        public virtual void LocalPlayerSelectedChallenge (GKChallenge challenge);
        public virtual void RemotePlayerCompletedChallenge (GKChallenge challenge);
        public virtual bool ShouldShowBannerForLocallyCompletedChallenge (GKChallenge challenge);
        public virtual bool ShouldShowBannerForLocallyReceivedChallenge (GKChallenge challenge);
        public virtual bool ShouldShowBannerForRemotelyCompletedChallenge (GKChallenge challenge);
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKChallengePredicate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKChallengePredicate

```
[Serializable]
public delegate bool GKChallengePredicate (GKChallenge challenge);
```

 <a name="New_Type:_MonoTouch.GameKit.GKChallengeState" class="injected"></a>


## New Type: MonoTouch.GameKit.GKChallengeState

```
[Serializable]
public enum GKChallengeState {
        Invalid,
        Pending,
        Completed,
        Declined
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKError" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKError

Added:

```
None,
        ChallengeInvalid,
        TurnBasedMatchDataTooLarge,
        TurnBasedTooManySessions,
        TurnBasedInvalidParticipant,
        TurnBasedInvalidTurn,
        TurnBasedInvalidState
```

 <a name="New_Type:_MonoTouch.GameKit.GKGameCenterControllerDelegate" class="injected"></a>


## New Type: MonoTouch.GameKit.GKGameCenterControllerDelegate

```
public class GKGameCenterControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKGameCenterControllerDelegate ();
        public GKGameCenterControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKGameCenterControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKGameCenterControllerDelegate (IntPtr handle);
        
        public virtual void Finished (GKGameCenterViewController controller);
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKGameCenterViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKGameCenterViewController

```
public class GKGameCenterViewController : MonoTouch.UIKit.UINavigationController {
        
        public GKGameCenterViewController ();
        public GKGameCenterViewController (MonoTouch.Foundation.NSCoder coder);
        public GKGameCenterViewController (MonoTouch.Foundation.NSObjectFlag t);
        public GKGameCenterViewController (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public GKGameCenterControllerDelegate Delegate {
                get;
                set;
        }
        public virtual string LeaderboardCategory {
                get;
                set;
        }
        public virtual GKLeaderboardTimeScope LeaderboardTimeScope {
                get;
                set;
        }
        public virtual GKGameCenterViewControllerState ViewState {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler Finished;
}
```

 <a name="New_Type:_MonoTouch.GameKit.GKGameCenterViewControllerState" class="injected"></a>


## New Type: MonoTouch.GameKit.GKGameCenterViewControllerState

```
[Serializable]
public enum GKGameCenterViewControllerState {
        Default,
        Leaderboards,
        Achievements,
        Challenges
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKInvite" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKInvite

Added:

```
public virtual uint PlayerAttributes {
                get;
        }
        public virtual int PlayerGroup {
                get;
        }
```

 <a name="New_Type:_MonoTouch.GameKit.GKInviteeResponse" class="injected"></a>


## New Type: MonoTouch.GameKit.GKInviteeResponse

```
[Serializable]
public enum GKInviteeResponse {
        Accepted,
        Declined,
        Failed,
        Incompatible,
        UnableToConnect,
        NoAnswer
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboard" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboard

Removed:

```
public static void LoadCategories (GKCategoryHandler categoryHandler);
```

Added:

```
[Obsolete("Deprecated iOS 6.0")]
        public static void LoadCategories (GKCategoryHandler categoryHandler);
        public static void LoadLeaderboards (System.Action<GKLeaderboard[],MonoTouch.Foundation.NSError> completionHandler);
        public virtual string GroupIdentifier {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboardViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Removed:

```
public class GKLeaderboardViewController : MonoTouch.UIKit.UINavigationController {
```

Added:

```
public class GKLeaderboardViewController : GKGameCenterViewController {
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLocalPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLocalPlayer

Removed:

```
public virtual void Authenticate (GKNotificationHandler handler);
```

Added:

```
[Obsolete("Replaced by AuthenticateHandler in iOS 6.0")]
        public virtual void Authenticate (GKNotificationHandler handler);
        public virtual void LoadDefaultLeaderboardCategoryID (System.Action<string,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action<MonoTouch.Foundation.NSError> completionHandler);
        public virtual System.Action<MonoTouch.UIKit.UIViewController,MonoTouch.Foundation.NSError> AuthenticateHandler {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatch

Added:

```
public virtual void ChooseBestHostPlayer (Action<string> completionHandler);
        public virtual void Rematch (System.Action<GKMatch,MonoTouch.Foundation.NSError> completionHandler);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchRequest" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchRequest

Added:

```
public static int GetMaxPlayersAllowed (GKMatchType matchType);
        
        public virtual int DefaultNumberOfPlayers {
                get;
                set;
        }
        public virtual Action<string,GKInviteeResponse> InviteeResponseHandler {
                get;
                set;
        }
        public virtual string InviteMessage {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.GameKit.GKMatchType" class="injected"></a>


## New Type: MonoTouch.GameKit.GKMatchType

```
[Serializable]
public enum GKMatchType {
        PeerToPeer,
        Hosted,
        TurnBased
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmaker" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmaker

Removed:

```
public virtual void QueryPlayerGroupActivity (uint playerGroup, GKQueryHandler completionHandler);
```

Added:

```
public virtual void CancelInvite (string playerID);
        public virtual void FinishMatchmaking (GKMatch match);
        public virtual void Match (GKInvite invite, System.Action<GKMatch,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void QueryPlayerGroupActivity (int playerGroup, GKQueryHandler completionHandler);
        public virtual void StartBrowsingForNearbyPlayers (Action<string,bool> reachableHandler);
        public virtual void StopBrowsingForNearbyPlayers ();
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Removed:

```
public GKMatchmakerViewController ();
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKNotificationBanner" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKNotificationBanner

Added:

```
public static void Show (string title, string message, double durationSeconds, Action completionHandler);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayer

Added:

```
public virtual string DisplayName {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKScore" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKScore

Removed:

```
public virtual MonoTouch.Foundation.NSDate date {
                set;
```

Added:

```
public static void ReportScores (GKScore[] scores, System.Action<MonoTouch.Foundation.NSError> completionHandler);
        public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
        [Obsolete("Use Date property")]
        public virtual MonoTouch.Foundation.NSDate date {
```

 <a name="New_Type:_MonoTouch.GameKit.GKScoreChallenge" class="injected"></a>


## New Type: MonoTouch.GameKit.GKScoreChallenge

```
public class GKScoreChallenge : GKChallenge {
        
        public GKScoreChallenge ();
        public GKScoreChallenge (MonoTouch.Foundation.NSCoder coder);
        public GKScoreChallenge (MonoTouch.Foundation.NSObjectFlag t);
        public GKScoreChallenge (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual GKScore Score {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate

Removed:

```
public virtual void HandleTurnEventForMatch (GKTurnBasedMatch match);
```

Added:

```
public virtual void HandleTurnEvent (GKTurnBasedMatch match, bool activated);
        [Obsolete("Replaced by HandleTurnEvent in iOS 6.0")]
        public virtual void HandleTurnEventForMatch (GKTurnBasedMatch match);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedMatch

Removed:

```
public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipatn, MonoTouch.Foundation.NSData matchData, GKNotificationHandler noCompletion);
        public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
```

Added:

```
public static void LoadMatch (string matchId, System.Action<GKTurnBasedMatch,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void AcceptInvite (System.Action<GKTurnBasedMatch,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void DeclineInvite (System.Action<GKTurnBasedMatch,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void EndTurn (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData, System.Action<MonoTouch.Foundation.NSError> completionHandler);
        [Obsolete("Replaced by EndTurn in iOS 6.0")]
        public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler noCompletion);
        [Obsolete("Replaced by ParticipantQuitInTurn (GKTurnBasedMatchOutcome, GKTurnBasedParticipant[], double, NSData, Action<NSError>) in iOS 6.0")]
        public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
        public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData, System.Action<MonoTouch.Foundation.NSError> completionHandler);
        public virtual void Rematch (System.Action<GKTurnBasedMatch,MonoTouch.Foundation.NSError> completionHandler);
        public virtual void SaveCurrentTurn (MonoTouch.Foundation.NSData matchData, System.Action<MonoTouch.Foundation.NSError> completionHandler);
        public static double DefaultTimeout {
                get;
        }
        public static double NoTimeout {
                get;
        }
        public virtual int MatchDataMaximumSize {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Removed:

```
public GKTurnBasedMatchmakerViewController ();
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedParticipant" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedParticipant

Added:

```
public virtual MonoTouch.Foundation.NSDate TimeoutDate {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKVoiceChatPlayerState" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKVoiceChatPlayerState

Added:

```
Connecting
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


# Namespace: MonoTouch.ImageIO

 <a name="Type_Changed:_MonoTouch.ImageIO.CGImageProperties" class="injected"></a>


## Type Changed: MonoTouch.ImageIO.CGImageProperties

Removed:

```
public class CGImageProperties {
        
        public CGImageProperties ();
```

Added:

```
public static class CGImageProperties {
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="New_Type:_MonoTouch.MapKit.MKDirectionsMode" class="injected"></a>


## New Type: MonoTouch.MapKit.MKDirectionsMode

```
[Serializable]
public enum MKDirectionsMode {
        Driving,
        Walking
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKDirectionsRequest" class="injected"></a>


## New Type: MonoTouch.MapKit.MKDirectionsRequest

```
public class MKDirectionsRequest : MonoTouch.Foundation.NSObject {
        
        public MKDirectionsRequest ();
        public MKDirectionsRequest (MonoTouch.Foundation.NSCoder coder);
        public MKDirectionsRequest (MonoTouch.Foundation.NSObjectFlag t);
        public MKDirectionsRequest (IntPtr handle);
        public MKDirectionsRequest (MonoTouch.Foundation.NSUrl url);
        
        public static bool IsDirectionsRequestUrl (MonoTouch.Foundation.NSUrl url);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MKMapItem Destination {
                get;
        }
        public virtual MKMapItem Source {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MapKit.MKLaunchOptions" class="injected"></a>


## New Type: MonoTouch.MapKit.MKLaunchOptions

```
public class MKLaunchOptions {
        
        public MKLaunchOptions ();
        
        public Nullable<mkdirectionsmode> DirectionsMode {
                get;
                set;
        }
        public System.Nullable<monotouch.corelocation.cllocationcoordinate2d> MapCenter {
                get;
                set;
        }
        public Nullable<mkcoordinatespan> MapSpan {
                get;
                set;
        }
        public Nullable<mkmaptype> MapType {
                get;
                set;
        }
        public Nullable<bool> ShowTraffic {
                get;
                set;
        }
}
</bool></mkmaptype></mkcoordinatespan></monotouch.corelocation.cllocationcoordinate2d></mkdirectionsmode>
```

 <a name="New_Type:_MonoTouch.MapKit.MKMapItem" class="injected"></a>


## New Type: MonoTouch.MapKit.MKMapItem

```
public class MKMapItem : MonoTouch.Foundation.NSObject {
        
        public MKMapItem ();
        public MKMapItem (MonoTouch.Foundation.NSCoder coder);
        public MKMapItem (MonoTouch.Foundation.NSObjectFlag t);
        public MKMapItem (IntPtr handle);
        public MKMapItem (MKPlacemark placemark);
        
        public static MKMapItem MapItemForCurrentLocation ();
        public static bool OpenMaps (MKMapItem[] mapItems, MKLaunchOptions launchOptions);
        protected override void Dispose (bool disposing);
        public void OpenInMaps (MKLaunchOptions launchOptions);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool IsCurrentLocation {
                get;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual string PhoneNumber {
                get;
                set;
        }
        public virtual MKPlacemark Placemark {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added:

```
public static MonoTouch.Foundation.NSString BookmarkTimeProperty {
                get;
        }
        public static MonoTouch.Foundation.NSString IsCloudItemProperty {
                get;
        }
        public double BookmarkTime {
                get;
        }
        public bool IsCloudItem {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaPickerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added:

```
public virtual bool ShowsCloudItems {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public virtual bool UseApplicationAudioSession {
```

Added:

```
public static MonoTouch.Foundation.NSString MoviePlayerReadyForDisplayDidChangeNotification {
                get;
        }
        public virtual bool ReadyForDisplay {
                get;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool UseApplicationAudioSession {
                public static MonoTouch.Foundation.NSObject ObserveMoviePlayerReadyForDisplayDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMusicPlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added:

```
public virtual void PrepareToPlay ();
        public virtual float CurrentPlaybackRate {
                get;
                set;
        }
        public virtual bool IsPreparedToPlay {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPVolumeView" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added:

```
public virtual MonoTouch.UIKit.UIImage GetMaximumVolumeSliderImage (MonoTouch.UIKit.UIControlState state);
        public virtual MonoTouch.UIKit.UIImage GetMinimumVolumeSliderImage (MonoTouch.UIKit.UIControlState state);
        public virtual MonoTouch.UIKit.UIImage GetRouteButtonImage (MonoTouch.UIKit.UIControlState state);
        public virtual System.Drawing.RectangleF GetRouteButtonRect (System.Drawing.RectangleF bounds);
        public virtual System.Drawing.RectangleF GetVolumeSliderRect (System.Drawing.RectangleF bounds);
        public virtual MonoTouch.UIKit.UIImage GetVolumeThumbImage (MonoTouch.UIKit.UIControlState state);
        public virtual System.Drawing.RectangleF GetVolumeThumbRect (System.Drawing.RectangleF bounds, System.Drawing.RectangleF columeSliderRect, float value);
        public virtual void SetMaximumVolumeSliderImage (MonoTouch.UIKit.UIImage image, MonoTouch.UIKit.UIControlState state);
        public virtual void SetMinimumVolumeSliderImage (MonoTouch.UIKit.UIImage image, MonoTouch.UIKit.UIControlState state);
        public virtual void SetRouteButtonImage (MonoTouch.UIKit.UIImage image, MonoTouch.UIKit.UIControlState state);
        public virtual void SetVolumeThumbImage (MonoTouch.UIKit.UIImage image, MonoTouch.UIKit.UIControlState state);
```

 <a name="Namespace:_MonoTouch.MediaToolbox" class="injected"></a>


# Namespace: MonoTouch.MediaToolbox

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTap" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTap

```
public class MTAudioProcessingTap : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public MTAudioProcessingTap (MTAudioProcessingTapCallbacks callbacks, MTAudioProcessingTapCreationFlags flags);
        
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public MTAudioProcessingTapError GetSourceAudio (long frames, ref MonoTouch.AudioToolbox.AudioBufferList bufferList, out MTAudioProcessingTapFlags flags, out MonoTouch.CoreMedia.CMTimeRange timeRange, long framesProvided);
        public void * GetStorage ();
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks

```
public class MTAudioProcessingTapCallbacks {
        
        public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessCallback process);
        
        public Action<mtaudioprocessingtap> Finalize {
                get;
                set;
        }
        public MTAudioProcessingTapInitCallback Initialize {
                get;
                set;
        }
        public MTAudioProcessingTapPrepareCallback Prepare {
                get;
                set;
        }
        public MTAudioProcessingTapProcessCallback Process {
                get;
        }
        public Action<mtaudioprocessingtap> Unprepare {
                get;
                set;
        }
}
</mtaudioprocessingtap></mtaudioprocessingtap>
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapCreationFlags" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapCreationFlags

```
[Serializable]
[Flags]
public enum MTAudioProcessingTapCreationFlags : uint {
        PreEffects,
        PostEffects
}
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapError" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapError

```
[Serializable]
public enum MTAudioProcessingTapError {
        None,
        InvalidArgument
}
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapFlags" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapFlags

```
[Serializable]
[Flags]
public enum MTAudioProcessingTapFlags : uint {
        StartOfStream,
        EndOfStream
}
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapInitCallback" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapInitCallback

```
[Serializable]
public delegate void MTAudioProcessingTapInitCallback (MTAudioProcessingTap tap, out void * tapStorage);
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapPrepareCallback" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapPrepareCallback

```
[Serializable]
public delegate void MTAudioProcessingTapPrepareCallback (MTAudioProcessingTap tap, long maxFrames, ref MonoTouch.AudioToolbox.AudioStreamBasicDescription processingFormat);
```

 <a name="New_Type:_MonoTouch.MediaToolbox.MTAudioProcessingTapProcessCallback" class="injected"></a>


## New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapProcessCallback

```
[Serializable]
public delegate void MTAudioProcessingTapProcessCallback (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, ref MonoTouch.AudioToolbox.AudioBufferList bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Dlfcn" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added:

```
public static System.Drawing.SizeF GetSizeF (IntPtr handle, string symbol);
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="New_Type:_MonoTouch.ObjCRuntime.MountainLionAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.MountainLionAttribute

```
public class MountainLionAttribute : Attribute {
        
        public MountainLionAttribute ();
}
```

 <a name="Namespace:_MonoTouch.PassKit" class="injected"></a>


# Namespace: MonoTouch.PassKit

 <a name="New_Type:_MonoTouch.PassKit.PKAddPassesViewController" class="injected"></a>


## New Type: MonoTouch.PassKit.PKAddPassesViewController

```
public class PKAddPassesViewController : MonoTouch.UIKit.UIViewController {
        
        public PKAddPassesViewController (MonoTouch.Foundation.NSCoder coder);
        public PKAddPassesViewController (MonoTouch.Foundation.NSObjectFlag t);
        public PKAddPassesViewController (IntPtr handle);
        public PKAddPassesViewController (PKPass pass);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public PKAddPassesViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler Finished;
}
```

 <a name="New_Type:_MonoTouch.PassKit.PKAddPassesViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.PassKit.PKAddPassesViewControllerDelegate

```
public class PKAddPassesViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public PKAddPassesViewControllerDelegate ();
        public PKAddPassesViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public PKAddPassesViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public PKAddPassesViewControllerDelegate (IntPtr handle);
        
        public virtual void Finished (PKAddPassesViewController controller);
}
```

 <a name="New_Type:_MonoTouch.PassKit.PKPass" class="injected"></a>


## New Type: MonoTouch.PassKit.PKPass

```
public class PKPass : MonoTouch.Foundation.NSObject {
        
        public PKPass ();
        public PKPass (MonoTouch.Foundation.NSCoder coder);
        public PKPass (MonoTouch.Foundation.NSObjectFlag t);
        public PKPass (IntPtr handle);
        public PKPass (MonoTouch.Foundation.NSData data, out MonoTouch.Foundation.NSError error);
        
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSObject GetLocalizedValue (MonoTouch.Foundation.NSString key);
        
        public static MonoTouch.Foundation.NSString ErrorDomain {
                get;
        }
        public virtual string AuthenticationToken {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.UIKit.UIImage Icon {
                get;
        }
        public virtual string LocalizedDescription {
                get;
        }
        public virtual string LocalizedName {
                get;
        }
        public virtual string OrganizationName {
                get;
        }
        public virtual string PassTypeIdentifier {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl PassUrl {
                get;
        }
        public virtual MonoTouch.Foundation.NSDate RelevantDate {
                get;
        }
        public virtual string SerialNumber {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl WebServiceUrl {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.PassKit.PKPassKitErrorCode" class="injected"></a>


## New Type: MonoTouch.PassKit.PKPassKitErrorCode

```
[Serializable]
public enum PKPassKitErrorCode {
        Unknown,
        None,
        InvalidData,
        UnsupportedVersion,
        CertificateRevoked
}
```

 <a name="New_Type:_MonoTouch.PassKit.PKPassLibrary" class="injected"></a>


## New Type: MonoTouch.PassKit.PKPassLibrary

```
public class PKPassLibrary : MonoTouch.Foundation.NSObject {
        
        public PKPassLibrary ();
        public PKPassLibrary (MonoTouch.Foundation.NSCoder coder);
        public PKPassLibrary (MonoTouch.Foundation.NSObjectFlag t);
        public PKPassLibrary (IntPtr handle);
        
        public virtual bool Contains (PKPass pass);
        public virtual PKPass GetPass (string identifier, string serialNumber);
        public virtual PKPass[] GetPasses ();
        public virtual void Remove (PKPass pass);
        public virtual bool Replace (PKPass pass);
        
        public static MonoTouch.Foundation.NSString DidChangeNotification {
                get;
        }
        public static bool IsAvailable {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChange (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
        }
}
</monotouch.foundation.nsnotificationeventargs>
```

 <a name="New_Type:_MonoTouch.PassKit.PKPassLibraryUserInfoKey" class="injected"></a>


## New Type: MonoTouch.PassKit.PKPassLibraryUserInfoKey

```
public static class PKPassLibraryUserInfoKey {
        
        public static MonoTouch.Foundation.NSString AddedPasses {
                get;
        }
        public static MonoTouch.Foundation.NSString PassTypeIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString RemovedPassInfos {
                get;
        }
        public static MonoTouch.Foundation.NSString ReplacementPasses {
                get;
        }
        public static MonoTouch.Foundation.NSString SerialNumber {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.QuickLook" class="injected"></a>


# Namespace: MonoTouch.QuickLook

 <a name="Type_Changed:_MonoTouch.QuickLook.QLFrame" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLFrame

Removed:

```
public delegate System.Drawing.RectangleF QLFrame (QLPreviewItem item, MonoTouch.UIKit.UIView view);
```

Added:

```
public delegate System.Drawing.RectangleF QLFrame (QLPreviewController controller, QLPreviewItem item, ref MonoTouch.UIKit.UIView view);
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLPreviewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLPreviewControllerDelegate

Removed:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewItem item, MonoTouch.UIKit.UIView view);
        public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

Added:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewController controller, QLPreviewItem item, ref MonoTouch.UIKit.UIView view);
        public virtual MonoTouch.UIKit.UIImage TransitionImageForPreviewItem (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="Type_Changed:_MonoTouch.QuickLook.QLTransition" class="injected"></a>


## Type Changed: MonoTouch.QuickLook.QLTransition

Removed:

```
public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

Added:

```
public delegate MonoTouch.UIKit.UIImage QLTransition (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

 <a name="Namespace:_MonoTouch.Security" class="injected"></a>


# Namespace: MonoTouch.Security

 <a name="Type_Changed:_MonoTouch.Security.SecPadding" class="injected"></a>


## Type Changed: MonoTouch.Security.SecPadding

Added:

```
PKCS1SHA224,
        PKCS1SHA256,
        PKCS1SHA384,
        PKCS1SHA512
```

 <a name="Namespace:_MonoTouch.Social" class="injected"></a>


# Namespace: MonoTouch.Social

 <a name="New_Type:_MonoTouch.Social.SLComposeViewController" class="injected"></a>


## New Type: MonoTouch.Social.SLComposeViewController

```
public class SLComposeViewController : MonoTouch.UIKit.UIViewController {
        
        public SLComposeViewController (MonoTouch.Foundation.NSCoder coder);
        public SLComposeViewController (MonoTouch.Foundation.NSObjectFlag t);
        public SLComposeViewController (IntPtr handle);
        
        public static SLComposeViewController FromService (MonoTouch.Foundation.NSString serviceType);
        public static SLComposeViewController FromService (SLServiceKind serviceKind);
        public static bool IsAvailable (MonoTouch.Foundation.NSString serviceType);
        public static bool IsAvailable (SLServiceKind serviceKind);
        public virtual bool AddImage (MonoTouch.UIKit.UIImage image);
        public virtual bool AddUrl (MonoTouch.Foundation.NSUrl url);
        protected override void Dispose (bool disposing);
        public virtual bool RemoveAllImages ();
        public virtual bool RemoveAllUrls ();
        public virtual bool SetInitialText (string text);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual Action<slcomposeviewcontrollerresult> CompletionHandler {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSString ServiceType {
                get;
        }
}
</slcomposeviewcontrollerresult>
```

 <a name="New_Type:_MonoTouch.Social.SLComposeViewControllerResult" class="injected"></a>


## New Type: MonoTouch.Social.SLComposeViewControllerResult

```
[Serializable]
public enum SLComposeViewControllerResult {
        Cancelled,
        Done
}
```

 <a name="New_Type:_MonoTouch.Social.SLRequest" class="injected"></a>


## New Type: MonoTouch.Social.SLRequest

```
public class SLRequest : MonoTouch.Foundation.NSObject {
        
        public SLRequest (MonoTouch.Foundation.NSCoder coder);
        public SLRequest (MonoTouch.Foundation.NSObjectFlag t);
        public SLRequest (IntPtr handle);
        
        public static SLRequest Create (MonoTouch.Foundation.NSString serviceType, SLRequestMethod requestMethod, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
        public static SLRequest Create (SLServiceKind serviceKind, SLRequestMethod method, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
        public virtual void AddMultipartData (MonoTouch.Foundation.NSData data, string partName, string partType, string filename);
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSUrlRequest GetPreparedUrlRequest ();
        public virtual void PerformRequest (System.Action<monotouch.foundation.nsdata,monotouch.foundation.nshttpurlresponse,monotouch.foundation.nserror> handler);
        
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
        public virtual SLRequestMethod RequestMethod {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Social.SLRequestMethod" class="injected"></a>


## New Type: MonoTouch.Social.SLRequestMethod

```
[Serializable]
public enum SLRequestMethod {
        Get,
        Post,
        Delete
}
```

 <a name="New_Type:_MonoTouch.Social.SLServiceKind" class="injected"></a>


## New Type: MonoTouch.Social.SLServiceKind

```
[Serializable]
public enum SLServiceKind {
        Facebook,
        Twitter,
        SinaWeibo
}
```

 <a name="New_Type:_MonoTouch.Social.SLServiceType" class="injected"></a>


## New Type: MonoTouch.Social.SLServiceType

```
public static class SLServiceType {
        
        public static MonoTouch.Foundation.NSString Facebook {
                get;
        }
        public static MonoTouch.Foundation.NSString SinaWeibo {
                get;
        }
        public static MonoTouch.Foundation.NSString Twitter {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>


# Namespace: MonoTouch.StoreKit

 <a name="New_Type:_MonoTouch.StoreKit.SKDownload" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKDownload

```
public class SKDownload : MonoTouch.Foundation.NSObject {
        
        public SKDownload ();
        public SKDownload (MonoTouch.Foundation.NSCoder coder);
        public SKDownload (MonoTouch.Foundation.NSObjectFlag t);
        public SKDownload (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public static double TimeRemainingUnknown {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string ContentIdentifier {
                get;
        }
        public virtual long ContentLength {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl ContentUrl {
                get;
        }
        public virtual string ContentVersion {
                get;
        }
        public virtual SKDownloadState DownloadState {
                get;
        }
        public virtual MonoTouch.Foundation.NSError Error {
                get;
        }
        public virtual float Progress {
                get;
        }
        public virtual double TimeRemaining {
                get;
        }
        public virtual SKPaymentTransaction Transaction {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.StoreKit.SKDownloadState" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKDownloadState

```
[Serializable]
public enum SKDownloadState {
        Waiting,
        Active,
        Paused,
        Finished,
        Failed,
        Cancelled
}
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKError" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKError

Added:

```
ProductNotAvailable
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKPaymentQueue" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKPaymentQueue

Added:

```
public virtual void CancelDownloads (SKDownload[] downloads);
        public virtual void PauseDownloads (SKDownload[] downloads);
        public virtual void ResumeDownloads (SKDownload[] downloads);
        public virtual void StartDownloads (SKDownload[] downloads);
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKPaymentTransaction" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKPaymentTransaction

Added:

```
public virtual SKDownload[] Downloads {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKPaymentTransactionObserver" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKPaymentTransactionObserver

Added:

```
public virtual void UpdatedDownloads (SKPaymentQueue queue, SKDownload[] downloads);
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProduct" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProduct

Added:

```
public virtual bool Downloadable {
                get;
        }
        public virtual MonoTouch.Foundation.NSNumber[] DownloadContentLengths {
                get;
        }
        public virtual string DownloadContentVersion {
                get;
        }
```

 <a name="New_Type:_MonoTouch.StoreKit.SKStoreProductParameterKey" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKStoreProductParameterKey

```
public static class SKStoreProductParameterKey {
        
        public static MonoTouch.Foundation.NSString ITunesItemIdentifier {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.StoreKit.SKStoreProductViewController" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKStoreProductViewController

```
public class SKStoreProductViewController : MonoTouch.UIKit.UIViewController {
        
        public SKStoreProductViewController ();
        public SKStoreProductViewController (MonoTouch.Foundation.NSCoder coder);
        public SKStoreProductViewController (MonoTouch.Foundation.NSObjectFlag t);
        public SKStoreProductViewController (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public void LoadProduct (StoreProductParameters parameters, System.Action<bool,monotouch.foundation.nserror> callback);
        
        public override IntPtr ClassHandle {
                get;
        }
        public SKStoreProductViewControllerDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler Finished;
}
```

 <a name="New_Type:_MonoTouch.StoreKit.SKStoreProductViewControllerDelegate" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKStoreProductViewControllerDelegate

```
public class SKStoreProductViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public SKStoreProductViewControllerDelegate ();
        public SKStoreProductViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public SKStoreProductViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public SKStoreProductViewControllerDelegate (IntPtr handle);
        
        public virtual void Finished (SKStoreProductViewController controller);
}
```

 <a name="New_Type:_MonoTouch.StoreKit.StoreProductParameters" class="injected"></a>


## New Type: MonoTouch.StoreKit.StoreProductParameters

```
public class StoreProductParameters : MonoTouch.Foundation.DictionaryContainer {
        
        public StoreProductParameters ();
        public StoreProductParameters (MonoTouch.Foundation.NSDictionary dictionary);
        public StoreProductParameters (int iTunesItemIdentifier);
        
        public Nullable<int> ITunesItemIdentifier {
                get;
                set;
        }
}
</int>
```

 <a name="Namespace:_MonoTouch.SystemConfiguration" class="injected"></a>


# Namespace: MonoTouch.SystemConfiguration

 <a name="Type_Changed:_MonoTouch.SystemConfiguration.StatusCode" class="injected"></a>


## Type Changed: MonoTouch.SystemConfiguration.StatusCode

Added:

```
ConnectionIgnore
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="New_Type:_MonoTouch.UIKit.NSLayoutAttribute" class="injected"></a>


## New Type: MonoTouch.UIKit.NSLayoutAttribute

```
[Serializable]
public enum NSLayoutAttribute {
        NoAttribute,
        Left,
        Right,
        Top,
        Bottom,
        Leading,
        Trailing,
        Width,
        Height,
        CenterX,
        CenterY,
        Baseline
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSLayoutConstraint" class="injected"></a>


## New Type: MonoTouch.UIKit.NSLayoutConstraint

```
public class NSLayoutConstraint : MonoTouch.Foundation.NSObject {
        
        public NSLayoutConstraint ();
        public NSLayoutConstraint (MonoTouch.Foundation.NSCoder coder);
        public NSLayoutConstraint (MonoTouch.Foundation.NSObjectFlag t);
        public NSLayoutConstraint (IntPtr handle);
        
        public static NSLayoutConstraint Create (MonoTouch.Foundation.NSObject view1, NSLayoutAttribute attribute1, NSLayoutRelation relation, MonoTouch.Foundation.NSObject view2, NSLayoutAttribute attribute2, float multiplier, float constant);
        public static NSLayoutConstraint[] FromVisualFormat (string format, NSLayoutFormatOptions formatOptions, MonoTouch.Foundation.NSDictionary metrics, MonoTouch.Foundation.NSDictionary views);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float Constant {
                get;
                set;
        }
        public virtual NSLayoutAttribute FirstAttribute {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject FirstItem {
                get;
        }
        public virtual float Multiplier {
                get;
        }
        public virtual UILayoutPriority Priority {
                get;
                set;
        }
        public virtual NSLayoutRelation Relation {
                get;
        }
        public virtual NSLayoutAttribute SecondAttribute {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject SecondItem {
                get;
        }
        public virtual bool ShouldBeArchived {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSLayoutFormatOptions" class="injected"></a>


## New Type: MonoTouch.UIKit.NSLayoutFormatOptions

```
[Serializable]
public enum NSLayoutFormatOptions {
        AlignAllLeft,
        AlignAllRight,
        AlignAllTop,
        AlignAllBottom,
        AlignAllLeading,
        AlignAllTrailing,
        AlignAllCenterX,
        AlignAllCenterY,
        AlignAllBaseline,
        AlignmentMask,
        DirectionLeadingToTrailing,
        DirectionLeftToRight,
        DirectionRightToLeft,
        DirectionMask
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSLayoutRelation" class="injected"></a>


## New Type: MonoTouch.UIKit.NSLayoutRelation

```
[Serializable]
public enum NSLayoutRelation {
        LessThanOrEqual,
        Equal,
        GreaterThanOrEqual
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSMutableParagraphStyle" class="injected"></a>


## New Type: MonoTouch.UIKit.NSMutableParagraphStyle

```
public class NSMutableParagraphStyle : NSParagraphStyle {
        
        public NSMutableParagraphStyle ();
        public NSMutableParagraphStyle (MonoTouch.Foundation.NSCoder coder);
        public NSMutableParagraphStyle (MonoTouch.Foundation.NSObjectFlag t);
        public NSMutableParagraphStyle (IntPtr handle);
        
        public override UITextAlignment Alignment {
                get;
                set;
        }
        public override MonoTouch.Foundation.NSWritingDirection BaseWritingDirection {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public override float FirstLineHeadIndent {
                get;
                set;
        }
        public override float HeadIndent {
                get;
                set;
        }
        public override float HyphenationFactor {
                get;
                set;
        }
        public override UILineBreakMode LineBreakMode {
                get;
                set;
        }
        public override float LineHeightMultiple {
                get;
                set;
        }
        public override float LineSpacing {
                get;
                set;
        }
        public override float MaximumLineHeight {
                get;
                set;
        }
        public override float MinimumLineHeight {
                get;
                set;
        }
        public override float ParagraphSpacing {
                get;
                set;
        }
        public override float ParagraphSpacingBefore {
                get;
                set;
        }
        public override float TailIndent {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSParagraphStyle" class="injected"></a>


## New Type: MonoTouch.UIKit.NSParagraphStyle

```
public class NSParagraphStyle : MonoTouch.Foundation.NSObject {
        
        public NSParagraphStyle ();
        public NSParagraphStyle (MonoTouch.Foundation.NSCoder coder);
        public NSParagraphStyle (MonoTouch.Foundation.NSObjectFlag t);
        public NSParagraphStyle (IntPtr handle);
        
        public static MonoTouch.Foundation.NSWritingDirection GetDefaultWritingDirection (string languageName);
        
        public static NSParagraphStyle Default {
                get;
        }
        public virtual UITextAlignment Alignment {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSWritingDirection BaseWritingDirection {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float FirstLineHeadIndent {
                get;
                set;
        }
        public virtual float HeadIndent {
                get;
                set;
        }
        public virtual float HyphenationFactor {
                get;
                set;
        }
        public virtual UILineBreakMode LineBreakMode {
                get;
                set;
        }
        public virtual float LineHeightMultiple {
                get;
                set;
        }
        public virtual float LineSpacing {
                get;
                set;
        }
        public virtual float MaximumLineHeight {
                get;
                set;
        }
        public virtual float MinimumLineHeight {
                get;
                set;
        }
        public virtual float ParagraphSpacing {
                get;
                set;
        }
        public virtual float ParagraphSpacingBefore {
                get;
                set;
        }
        public virtual float TailIndent {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.NSShadow" class="injected"></a>


## New Type: MonoTouch.UIKit.NSShadow

```
public class NSShadow : MonoTouch.Foundation.NSObject {
        
        public NSShadow ();
        public NSShadow (MonoTouch.Foundation.NSCoder coder);
        public NSShadow (MonoTouch.Foundation.NSObjectFlag t);
        public NSShadow (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float ShadowBlurRadius {
                get;
                set;
        }
        public virtual UIColor ShadowColor {
                get;
                set;
        }
        public virtual System.Drawing.SizeF ShadowOffset {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIActivity" class="injected"></a>


## New Type: MonoTouch.UIKit.UIActivity

```
public class UIActivity : MonoTouch.Foundation.NSObject {
        
        public UIActivity ();
        public UIActivity (MonoTouch.Foundation.NSCoder coder);
        public UIActivity (MonoTouch.Foundation.NSObjectFlag t);
        public UIActivity (IntPtr handle);
        
        public virtual bool CanPerform (MonoTouch.Foundation.NSObject[] activityItems);
        protected override void Dispose (bool disposing);
        public virtual void Finished (bool completed);
        public virtual void Perform ();
        public virtual void Prepare (MonoTouch.Foundation.NSObject[] activityItems);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIImage Image {
                get;
        }
        public virtual string Title {
                get;
        }
        public virtual MonoTouch.Foundation.NSString Type {
                get;
        }
        public virtual UIViewController ViewController {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIActivityItemProvider" class="injected"></a>


## New Type: MonoTouch.UIKit.UIActivityItemProvider

```
public class UIActivityItemProvider : MonoTouch.Foundation.NSOperation {
        
        public UIActivityItemProvider ();
        public UIActivityItemProvider (MonoTouch.Foundation.NSCoder coder);
        public UIActivityItemProvider (MonoTouch.Foundation.NSObjectFlag t);
        public UIActivityItemProvider (IntPtr handle);
        public UIActivityItemProvider (MonoTouch.Foundation.NSObject placeholderItem);
        
        protected override void Dispose (bool disposing);
        
        public virtual MonoTouch.Foundation.NSString ActivityType {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject Item {
                get;
        }
        public virtual MonoTouch.Foundation.NSObject PlaceholderItem {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIActivityItemSource" class="injected"></a>


## New Type: MonoTouch.UIKit.UIActivityItemSource

```
public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject {
        
        public UIActivityItemSource ();
        public UIActivityItemSource (MonoTouch.Foundation.NSCoder coder);
        public UIActivityItemSource (MonoTouch.Foundation.NSObjectFlag t);
        public UIActivityItemSource (IntPtr handle);
        
        public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, string activityType);
        public abstract MonoTouch.Foundation.NSObject GetPlaceholderData (UIActivityViewController activityViewController);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIActivityType" class="injected"></a>


## New Type: MonoTouch.UIKit.UIActivityType

```
public static class UIActivityType {
        
        public static MonoTouch.Foundation.NSString AssignToContact {
                get;
        }
        public static MonoTouch.Foundation.NSString CopyToPasteboard {
                get;
        }
        public static MonoTouch.Foundation.NSString Mail {
                get;
        }
        public static MonoTouch.Foundation.NSString Message {
                get;
        }
        public static MonoTouch.Foundation.NSString PostToFacebook {
                get;
        }
        public static MonoTouch.Foundation.NSString PostToTwitter {
                get;
        }
        public static MonoTouch.Foundation.NSString PostToWeibo {
                get;
        }
        public static MonoTouch.Foundation.NSString Print {
                get;
        }
        public static MonoTouch.Foundation.NSString SaveToCameraRoll {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIActivityViewController" class="injected"></a>


## New Type: MonoTouch.UIKit.UIActivityViewController

```
public class UIActivityViewController : UIViewController {
        
        public UIActivityViewController ();
        public UIActivityViewController (MonoTouch.Foundation.NSCoder coder);
        public UIActivityViewController (MonoTouch.Foundation.NSObjectFlag t);
        public UIActivityViewController (IntPtr handle);
        public UIActivityViewController (MonoTouch.Foundation.NSObject[] activityItems, UIActivity[] applicationActivities);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Action<monotouch.foundation.nsstring,bool> CompletionHandler {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSString[] ExcludedActivityTypes {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Added:

```
public virtual void CompleteStateRestoration ();
        public virtual void ExtendStateRestoration ();
        public virtual UIInterfaceOrientationMask SupportedInterfaceOrientationsForWindow (UIWindow window);
        public static MonoTouch.Foundation.NSString UITrackingRunLoopMode {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Added:

```
public virtual void DidDecodeRestorableState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
        public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIApplication application, UIWindow forWindow);
        public virtual UIViewController GetViewController (UIApplication application, string [] restorationIdentifierComponents, MonoTouch.Foundation.NSCoder coder);
        public virtual bool ShouldRestoreApplicationState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
        public virtual bool ShouldSaveApplicationState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
        public virtual void WillEncodeRestorableState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
        public virtual bool WillFinishLaunching (UIApplication application, MonoTouch.Foundation.NSDictionary launchOptions);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBarButtonItem" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added:

```
public virtual UIImage GetBackgroundImage (UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
        public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
                public virtual UIImage GetBackgroundImage (UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
                public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBezierPath

Added:

```
public virtual UIBezierPath BezierPathByReversingPath ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

Added:

```
public virtual MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIControlState state);
        public virtual void SetAttributedTitle (MonoTouch.Foundation.NSAttributedString title, UIControlState state);
        public virtual MonoTouch.Foundation.NSAttributedString CurrentAttributedTitle {
                get;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionElementCategory" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionElementCategory

```
[Serializable]
public enum UICollectionElementCategory {
        Cell,
        SupplementaryView,
        DecorationView
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionElementKindSection" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionElementKindSection

```
[Serializable]
public enum UICollectionElementKindSection {
        Header,
        Footer
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionElementKindSectionKey" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionElementKindSectionKey

```
public static class UICollectionElementKindSectionKey {
        
        public static MonoTouch.Foundation.NSString Footer {
                get;
        }
        public static MonoTouch.Foundation.NSString Header {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionReusableView" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionReusableView

```
public class UICollectionReusableView : UIView {
        
        public UICollectionReusableView ();
        public UICollectionReusableView (MonoTouch.Foundation.NSCoder coder);
        public UICollectionReusableView (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionReusableView (IntPtr handle);
        public UICollectionReusableView (System.Drawing.RectangleF frame);
        
        public static UICollectionReusableViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void ApplyLayoutAttributes (UICollectionViewLayoutAttributes layoutAttributes);
        public virtual void DidTransition (UICollectionViewLayout oldLayout, UICollectionViewLayout newLayout);
        protected override void Dispose (bool disposing);
        public virtual void PrepareForReuse ();
        public virtual void WillTransition (UICollectionViewLayout oldLayout, UICollectionViewLayout newLayout);
        
        public static UICollectionReusableViewAppearance Appearance {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSString ReuseIdentifier {
                get;
        }
        
        public class UICollectionReusableViewAppearance : UIViewAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionUpdateAction" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionUpdateAction

```
[Serializable]
public enum UICollectionUpdateAction {
        Insert,
        Delete,
        Reload,
        Move,
        None
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionView" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionView

```
public class UICollectionView : UIScrollView {
        
        public UICollectionView (MonoTouch.Foundation.NSCoder coder);
        public UICollectionView (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionView (IntPtr handle);
        public UICollectionView (System.Drawing.RectangleF frame, UICollectionViewLayout layout);
        
        public static UICollectionViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual UICollectionViewCell CellForItem (MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void DeleteItems (MonoTouch.Foundation.NSIndexPath[] indexPaths);
        public virtual void DeleteSections (MonoTouch.Foundation.NSIndexSet sections);
        public virtual MonoTouch.Foundation.NSObject DequeueReusableCell (MonoTouch.Foundation.NSString reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual MonoTouch.Foundation.NSObject DequeueReusableSupplementaryView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString identifier, MonoTouch.Foundation.NSIndexPath indexPath);
        public MonoTouch.Foundation.NSObject DequeueReusableSupplementaryView (UICollectionElementKindSection section, MonoTouch.Foundation.NSString identifier, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void DeselectItem (MonoTouch.Foundation.NSIndexPath indexPath, bool animated);
        protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSIndexPath[] GetIndexPathsForSelectedItems ();
        public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForItem (MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual MonoTouch.Foundation.NSIndexPath IndexPathForCell (UICollectionViewCell cell);
        public virtual MonoTouch.Foundation.NSIndexPath IndexPathForItemAtPoint (System.Drawing.PointF point);
        public virtual void InsertItems (MonoTouch.Foundation.NSIndexPath[] indexPaths);
        public virtual void InsertSections (MonoTouch.Foundation.NSIndexSet sections);
        public virtual void MoveItem (MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSIndexPath newIndexPath);
        public virtual void MoveSection (int section, int newSection);
        public virtual int NumberOfItemsInSection (int section);
        public virtual int NumberOfSections ();
        public virtual void PerformBatchUpdates (MonoTouch.Foundation.NSAction updates, UICompletionHandler completed);
        public void RegisterClassForCell (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
        protected virtual void RegisterClassForSupplementaryView (IntPtr viewClass, MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString reuseIdentifier);
        public void RegisterClassForSupplementaryView (Type cellType, UICollectionElementKindSection section, MonoTouch.Foundation.NSString reuseIdentifier);
        public virtual void RegisterNibForCell (UINib nib, MonoTouch.Foundation.NSString reuseIdentifier);
        protected virtual void RegisterNibForSupplementaryView (UINib nib, MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSString reuseIdentifier);
        public void RegisterNibForSupplementaryView (UINib nib, UICollectionElementKindSection section, MonoTouch.Foundation.NSString reuseIdentifier);
        public virtual void ReloadData ();
        public virtual void ReloadItems (MonoTouch.Foundation.NSIndexPath[] indexPaths);
        public virtual void ReloadSections (MonoTouch.Foundation.NSIndexSet sections);
        public virtual void ScrollToItem (MonoTouch.Foundation.NSIndexPath indexPath, UICollectionViewScrollPosition scrollPosition, bool animated);
        public virtual void SelectItem (MonoTouch.Foundation.NSIndexPath indexPath, bool animated, UICollectionViewScrollPosition scrollPosition);
        public virtual void SetCollectionViewLayout (UICollectionViewLayout layout, bool animated);
        
        public static UICollectionViewAppearance Appearance {
                get;
        }
        public virtual bool AllowsMultipleSelection {
                get;
                set;
        }
        public virtual bool AllowsSelection {
                get;
                set;
        }
        public virtual UIView BackgroundView {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UICollectionViewLayout CollectionViewLayout {
                get;
                set;
        }
        public UICollectionViewDataSource DataSource {
                get;
                set;
        }
        public UICollectionViewDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSIndexPath[] IndexPathsForVisibleItems {
                get;
        }
        public UICollectionViewSource Source {
                get;
                set;
        }
        public virtual UICollectionViewCell[] VisibleCells {
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
        
        public class UICollectionViewAppearance : UIScrollViewAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewCell" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewCell

```
public class UICollectionViewCell : UICollectionReusableView {
        
        public UICollectionViewCell ();
        public UICollectionViewCell (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewCell (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewCell (IntPtr handle);
        public UICollectionViewCell (System.Drawing.RectangleF frame);
        
        public static UICollectionViewCellAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        
        public static UICollectionViewCellAppearance Appearance {
                get;
        }
        public virtual UIView BackgroundView {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIView ContentView {
                get;
        }
        public virtual bool Highlighted {
                get;
                set;
        }
        public virtual bool Selected {
                get;
                set;
        }
        public virtual UIView SelectedBackgroundView {
                get;
                set;
        }
        
        public class UICollectionViewCellAppearance : UICollectionReusableViewAppearance {
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewController" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewController

```
public class UICollectionViewController : UIViewController {
        
        public UICollectionViewController ();
        public UICollectionViewController (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewController (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewController (IntPtr handle);
        public UICollectionViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
        public UICollectionViewController (UICollectionViewLayout layout);
        
        public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
        protected override void Dispose (bool disposing);
        public virtual UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual int GetItemsCount (UICollectionView collectionView, int section);
        public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual int NumberOfSections (UICollectionView collectionView);
        public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool ClearsSelectionOnViewWillAppear {
                get;
                set;
        }
        public virtual UICollectionView CollectionView {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewDataSource" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewDataSource

```
public abstract class UICollectionViewDataSource : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewDataSource ();
        public UICollectionViewDataSource (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewDataSource (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewDataSource (IntPtr handle);
        
        public abstract UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public abstract int GetItemsCount (UICollectionView collectionView, int section);
        public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual int NumberOfSections (UICollectionView collectionView);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewDelegate" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewDelegate

```
public class UICollectionViewDelegate : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewDelegate ();
        public UICollectionViewDelegate (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewDelegate (IntPtr handle);
        
        public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewDelegateFlowLayout" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout

```
public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate {
        
        public UICollectionViewDelegateFlowLayout ();
        public UICollectionViewDelegateFlowLayout (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewDelegateFlowLayout (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewDelegateFlowLayout (IntPtr handle);
        
        public override bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public override void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual UIEdgeInsets GetInsetForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
        public virtual float GetMinimumInteritemSpacingForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
        public virtual float GetMinimumLineSpacingForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
        public virtual System.Drawing.SizeF GetReferenceSizeForFooter (UICollectionView collectionView, UICollectionViewLayout layout, int section);
        public virtual System.Drawing.SizeF GetReferenceSizeForHeader (UICollectionView collectionView, UICollectionViewLayout layout, int section);
        public virtual System.Drawing.SizeF GetSizeForItem (UICollectionView collectionView, UICollectionViewLayout layout, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public override bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public override void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewFlowLayout" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewFlowLayout

```
public class UICollectionViewFlowLayout : UICollectionViewLayout {
        
        public UICollectionViewFlowLayout ();
        public UICollectionViewFlowLayout (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewFlowLayout (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewFlowLayout (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Drawing.SizeF FooterReferenceSize {
                get;
                set;
        }
        public virtual System.Drawing.SizeF HeaderReferenceSize {
                get;
                set;
        }
        public virtual System.Drawing.SizeF ItemSize {
                get;
                set;
        }
        public virtual float MinimumInteritemSpacing {
                get;
                set;
        }
        public virtual float MinimumLineSpacing {
                get;
                set;
        }
        public virtual UICollectionViewScrollDirection ScrollDirection {
                get;
                set;
        }
        public virtual UIEdgeInsets SectionInset {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewLayout" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewLayout

```
public class UICollectionViewLayout : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewLayout ();
        public UICollectionViewLayout (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewLayout (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewLayout (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual void FinalizeAnimatedBoundsChange ();
        public virtual void FinalizeCollectionViewUpdates ();
        public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDeletedSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingDecorationElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath decorationIndexPath);
        public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath elementIndexPath);
        public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingDecorationElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath decorationIndexPath);
        public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath elementIndexPath);
        public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForInsertedSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath itemIndexPath);
        public virtual void InvalidateLayout ();
        public virtual UICollectionViewLayoutAttributes LayoutAttributesForDecorationView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual UICollectionViewLayoutAttributes[] LayoutAttributesForElementsInRect (System.Drawing.RectangleF rect);
        public virtual UICollectionViewLayoutAttributes LayoutAttributesForItem (MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual UICollectionViewLayoutAttributes LayoutAttributesForSupplementaryView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath);
        public UICollectionViewLayoutAttributes LayoutAttributesForSupplementaryView (UICollectionElementKindSection section, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void PrepareForAnimatedBoundsChange (System.Drawing.RectangleF oldBounds);
        public virtual void PrepareForCollectionViewUpdates (UICollectionViewUpdateItem[] updateItems);
        public virtual void PrepareLayout ();
        public void RegisterClassForDecorationView (Type viewType, MonoTouch.Foundation.NSString kind);
        public virtual void RegisterNibForDecorationView (UINib nib, MonoTouch.Foundation.NSString kind);
        public virtual bool ShouldInvalidateLayoutForBoundsChange (System.Drawing.RectangleF newBounds);
        public virtual System.Drawing.PointF TargetContentOffset (System.Drawing.PointF proposedContentOffset, System.Drawing.PointF scrollingVelocity);
        
        public static MonoTouch.ObjCRuntime.Class LayoutAttributesClass {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UICollectionView CollectionView {
                get;
        }
        public virtual System.Drawing.SizeF CollectionViewContentSize {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewLayoutAttributes" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewLayoutAttributes

```
public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewLayoutAttributes ();
        public UICollectionViewLayoutAttributes (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewLayoutAttributes (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewLayoutAttributes (IntPtr handle);
        
        public static UICollectionViewLayoutAttributes CreateForCell (MonoTouch.Foundation.NSIndexPath indexPath);
        public static UICollectionViewLayoutAttributes CreateForDecorationView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath);
        public static UICollectionViewLayoutAttributes CreateForSupplementaryView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath);
        public static UICollectionViewLayoutAttributes CreateForSupplementaryView (UICollectionElementKindSection section, MonoTouch.Foundation.NSIndexPath indexPath);
        protected override void Dispose (bool disposing);
        
        public virtual float Alpha {
                get;
                set;
        }
        public virtual System.Drawing.PointF Center {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Drawing.RectangleF Frame {
                get;
                set;
        }
        public virtual bool Hidden {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSIndexPath IndexPath {
                get;
                set;
        }
        public virtual UICollectionElementCategory RepresentedElementCategory {
                get;
        }
        public virtual string RepresentedElementKind {
                get;
        }
        public virtual System.Drawing.SizeF Size {
                get;
                set;
        }
        public virtual MonoTouch.CoreAnimation.CATransform3D Transform3D {
                get;
                set;
        }
        public virtual int ZIndex {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewScrollDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewScrollDirection

```
[Serializable]
public enum UICollectionViewScrollDirection {
        Vertical,
        Horizontal
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewScrollPosition" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewScrollPosition

```
[Serializable]
[Flags]
public enum UICollectionViewScrollPosition {
        None,
        Top,
        CenteredVertically,
        Bottom,
        Left,
        CenteredHorizontally,
        Right
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewSource" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewSource

```
public class UICollectionViewSource : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewSource ();
        public UICollectionViewSource (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewSource (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewSource (IntPtr handle);
        
        public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual int GetItemsCount (UICollectionView collectionView, int section);
        public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemDeselected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemHighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemSelected (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void ItemUnhighlighted (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual int NumberOfSections (UICollectionView collectionView);
        public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
        public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UICollectionViewUpdateItem" class="injected"></a>


## New Type: MonoTouch.UIKit.UICollectionViewUpdateItem

```
public class UICollectionViewUpdateItem : MonoTouch.Foundation.NSObject {
        
        public UICollectionViewUpdateItem ();
        public UICollectionViewUpdateItem (MonoTouch.Foundation.NSCoder coder);
        public UICollectionViewUpdateItem (MonoTouch.Foundation.NSObjectFlag t);
        public UICollectionViewUpdateItem (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSIndexPath IndexPathAfterUpdate {
                get;
        }
        public virtual MonoTouch.Foundation.NSIndexPath IndexPathBeforeUpdate {
                get;
        }
        public virtual UICollectionUpdateAction UpdateAction {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDatePicker" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDatePicker

Removed:

```
[Obsolete("Deprecated in iOS 5.0")]
        public virtual MonoTouch.Foundation.NSLocale Locale {
```

Added:

```
public virtual MonoTouch.Foundation.NSLocale Locale {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

Added:

```
protected override void Dispose (bool disposing);
        public virtual MonoTouch.Foundation.NSUuid IdentifierForVendor {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocumentInteractionControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocumentInteractionControllerDelegate

Removed:

```
public virtual bool CanPerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
        public virtual bool PerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
```

Added:

```
[Obsolete("Deprecated in iOS 6.0")]
        public virtual bool CanPerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool PerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImage" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImage

Added:

```
public UIImage (MonoTouch.Foundation.NSData data, float scale);
        public UIImage (MonoTouch.CoreImage.CIImage ciImage, float scale, UIImageOrientation orientation);
        public UIImage (UIEdgeInsets capInsets, UIImageResizingMode resizingMode);
        public static UIImage CreateAnimatedImage (string name, UIEdgeInsets capInsets, UIImageResizingMode resizingMode, double duration);
        public static UIImage FromImage (MonoTouch.CoreImage.CIImage ciImage, float scale, UIImageOrientation orientation);
        public static UIImage LoadFromData (MonoTouch.Foundation.NSData data, float scale);
        public virtual UIImage ImageWithAlignmentRectInsets (UIEdgeInsets alignmentInsets);
        public virtual UIEdgeInsets AlignmentRectInsets {
                get;
        }
        public virtual UIImageResizingMode ResizingMode {
                get;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIImageResizingMode" class="injected"></a>


## New Type: MonoTouch.UIKit.UIImageResizingMode

```
[Serializable]
public enum UIImageResizingMode {
        Tile,
        Stretch
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIInterfaceOrientationMask" class="injected"></a>


## New Type: MonoTouch.UIKit.UIInterfaceOrientationMask

```
[Serializable]
[Flags]
public enum UIInterfaceOrientationMask {
        Portrait,
        LandscapeLeft,
        LandscapeRight,
        PortraitUpsideDown,
        Landscape,
        All,
        AllButUpsideDown
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboard

Removed:

```
public class UIKeyboard {
        
        public UIKeyboard ();
```

Added:

```
public static class UIKeyboard {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILabel" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILabel

Removed:

```
public virtual float MinimumFontSize {
```

Added:

```
public virtual bool AdjustsLetterSpacingToFitWidth {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSAttributedString AttributedText {
                get;
                set;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual float MinimumFontSize {
                get;
                set;
        }
        public virtual float MinimumScaleFactor {
                get;
                set;
        }
        public virtual float PreferredMaxLayoutWidth {
```

 <a name="New_Type:_MonoTouch.UIKit.UILayoutConstraintAxis" class="injected"></a>


## New Type: MonoTouch.UIKit.UILayoutConstraintAxis

```
[Serializable]
public enum UILayoutConstraintAxis {
        Horizontal,
        Vertical
}
```

 <a name="New_Type:_MonoTouch.UIKit.UILayoutPriority" class="injected"></a>


## New Type: MonoTouch.UIKit.UILayoutPriority

```
[Serializable]
public enum UILayoutPriority {
        Required,
        DefaultHigh,
        DefaultLow,
        FittingSizeLevel
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINavigationBar

Added:

```
public virtual UIImage ShadowImage {
                get;
                set;
        }
                public virtual UIImage ShadowImage {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINavigationController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINavigationController

Added:

```
public UINavigationController (Type navigationBarType, Type toolbarType);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINib" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINib

Added:

```
public static MonoTouch.Foundation.NSString ExternalObjectsKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageControl" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageControl

Added:

```
protected override void Dispose (bool disposing);
        public virtual UIColor CurrentPageIndicatorTintColor {
                get;
                set;
        }
        public virtual UIColor PageIndicatorTintColor {
                get;
                set;
        }
                
                public virtual UIColor CurrentPageIndicatorTintColor {
                        get;
                        set;
                }
                public virtual UIColor PageIndicatorTintColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageViewController

Added:

```
public UIPageViewController (UIPageViewControllerTransitionStyle style, UIPageViewControllerNavigationOrientation navigationOrientation, UIPageViewControllerSpineLocation spineLocation, float interPageSpacing);
        public UIPageViewGetNumber GetPresentationCount {
                get;
                set;
        }
        public UIPageViewGetNumber GetPresentationIndex {
                get;
                set;
        }
        public event EventHandler<UIPageViewControllerTransitionEventArgs> WillTransition;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageViewControllerDataSource" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageViewControllerDataSource

Added:

```
public virtual int GetPresentationCount (UIPageViewController pageViewController);
        public virtual int GetPresentationIndex (UIPageViewController pageViewController);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate

Added:

```
public virtual void WillTransition (UIPageViewController pageViewController, UIViewController[] pendingViewControllers);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewControllerTransitionEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewControllerTransitionEventArgs

```
public class UIPageViewControllerTransitionEventArgs : EventArgs {
        
        public UIPageViewControllerTransitionEventArgs (UIViewController[] pendingViewControllers);
        
        public UIViewController[] PendingViewControllers {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageViewControllerTransitionStyle" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageViewControllerTransitionStyle

Added:

```
Scroll
```

 <a name="New_Type:_MonoTouch.UIKit.UIPageViewGetNumber" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPageViewGetNumber

```
[Serializable]
public delegate int UIPageViewGetNumber (UIPageViewController pageViewController);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerViewDelegate

Added:

```
public virtual MonoTouch.Foundation.NSAttributedString GetAttributedTitle (UIPickerView pickerView, int row, int component);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPopoverBackgroundView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added:

```
public static bool WantsDefaultContentAppearance {
                get;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIRefreshControl" class="injected"></a>


## New Type: MonoTouch.UIKit.UIRefreshControl

```
public class UIRefreshControl : UIControl {
        
        public UIRefreshControl ();
        public UIRefreshControl (MonoTouch.Foundation.NSCoder coder);
        public UIRefreshControl (MonoTouch.Foundation.NSObjectFlag t);
        public UIRefreshControl (IntPtr handle);
        
        public static UIRefreshControlAppearance AppearanceWhenContainedIn (params Type [] containers);
        public virtual void BeginRefreshing ();
        protected override void Dispose (bool disposing);
        public virtual void EndRefreshing ();
        
        public static UIRefreshControlAppearance Appearance {
                get;
        }
        public virtual MonoTouch.Foundation.NSAttributedString AttributedTitle {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool Refreshing {
                get;
        }
        public virtual UIColor TintColor {
                get;
                set;
        }
        
        public class UIRefreshControlAppearance : UIControlAppearance {
                
                public virtual MonoTouch.Foundation.NSAttributedString AttributedTitle {
                        get;
                        set;
                }
                public virtual UIColor TintColor {
                        get;
                        set;
                }
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIResponder" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIResponder

Added:

```
public virtual void ToggleBoldface (MonoTouch.Foundation.NSObject sender);
        public virtual void ToggleItalics (MonoTouch.Foundation.NSObject sender);
        public virtual void ToggleUnderline (MonoTouch.Foundation.NSObject sender);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIStepper" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIStepper

Added:

```
public virtual UIImage BackgroundImage (UIControlState state);
        protected override void Dispose (bool disposing);
        public virtual UIImage GetDecrementImage (UIControlState state);
        public virtual UIImage GetDividerImage (UIControlState leftState, UIControlState rightState);
        public virtual UIImage GetIncrementImage (UIControlState state);
        public virtual void SetBackgroundImage (UIImage image, UIControlState state);
        public virtual void SetDecrementImage (UIImage image, UIControlState state);
        public virtual void SetDividerImage (UIImage image, UIControlState leftState, UIControlState rightState);
        public virtual void SetIncrementImage (UIImage image, UIControlState state);
        public virtual UIColor TintColor {
                get;
                set;
        }
                
                public virtual UIImage BackgroundImage (UIControlState state);
                public virtual UIImage GetDecrementImage (UIControlState state);
                public virtual UIImage GetDividerImage (UIControlState leftState, UIControlState rightState);
                public virtual UIImage GetIncrementImage (UIControlState state);
                public virtual void SetBackgroundImage (UIImage image, UIControlState state);
                public virtual void SetDecrementImage (UIImage image, UIControlState state);
                public virtual void SetDividerImage (UIImage image, UIControlState leftState, UIControlState rightState);
                public virtual void SetIncrementImage (UIImage image, UIControlState state);
                
                public virtual UIColor TintColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIStoryboardSegue" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIStoryboardSegue

Added:

```
public static UIStoryboardSegue Create (string identifier, UIViewController source, UIViewController destination, MonoTouch.Foundation.NSAction performHandler);
```

 <a name="New_Type:_MonoTouch.UIKit.UIStringAttributeKey" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStringAttributeKey

```
public static class UIStringAttributeKey {
        
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
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStringAttributes" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStringAttributes

```
public class UIStringAttributes : MonoTouch.Foundation.DictionaryContainer {
        
        public UIStringAttributes ();
        public UIStringAttributes (MonoTouch.Foundation.NSDictionary dictionary);
        
        public UIColor BackgroundColor {
                get;
                set;
        }
        public UIFont Font {
                get;
                set;
        }
        public UIColor ForegroundColor {
                get;
                set;
        }
        public Nullable<float> KerningAdjustment {
                get;
                set;
        }
        public System.Nullable<monotouch.foundation.nsligaturetype> Ligature {
                get;
                set;
        }
        public NSParagraphStyle ParagraphStyle {
                get;
                set;
        }
        public NSShadow Shadow {
                get;
                set;
        }
        public System.Nullable<monotouch.foundation.nsunderlinestyle> StrikethroughStyle {
                get;
                set;
        }
        public UIColor StrokeColor {
                get;
                set;
        }
        public Nullable<float> StrokeWidth {
                get;
                set;
        }
        public System.Nullable<monotouch.foundation.nsunderlinestyle> UnderlineStyle {
                get;
                set;
        }
}
</monotouch.foundation.nsunderlinestyle></float></monotouch.foundation.nsunderlinestyle></monotouch.foundation.nsligaturetype></float>
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwitch" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwitch

Added:

```
public virtual UIImage OffImage {
                get;
                set;
        }
        public virtual UIImage OnImage {
                get;
                set;
        }
        public virtual UIColor ThumbTintColor {
                get;
                set;
        }
        public virtual UIColor TintColor {
                get;
                set;
        }
                public virtual UIImage OffImage {
                        get;
                        set;
                }
                public virtual UIImage OnImage {
                        get;
                        set;
                }
                public virtual UIColor ThumbTintColor {
                        get;
                        set;
                }
                public virtual UIColor TintColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBar

Added:

```
public virtual UIImage ShadowImage {
                get;
                set;
        }
                public virtual UIImage ShadowImage {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableView

Removed:

```
public virtual void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
```

Added:

```
public virtual MonoTouch.Foundation.NSObject DequeueReusableCell (MonoTouch.Foundation.NSString reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual MonoTouch.Foundation.NSObject DequeueReusableHeaderFooterView (MonoTouch.Foundation.NSString reuseIdentifier);
        public virtual UITableViewHeaderFooterView GetFooterView (int section);
        public virtual UITableViewHeaderFooterView GetHeaderView (int section);
        public void RegisterClassForCellReuse (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
        public void RegisterClassForHeaderFooterViewReuse (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
        [Obsolete("Use RegisterNibForCellReuse")]
        public void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
        public virtual void RegisterNibForCellReuse (UINib nib, string reuseIdentifier);
        public virtual void RegisterNibForHeaderFooterViewReuse (UINib nib, string identifier);
        public virtual UIColor SectionIndexColor {
                get;
                set;
        }
        public virtual UIColor SectionIndexTrackingBackgroundColor {
                get;
                set;
        }
                
                public virtual UIColor SectionIndexColor {
                        get;
                        set;
                }
                public virtual UIColor SectionIndexTrackingBackgroundColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewController

Added:

```
public virtual UIRefreshControl RefreshControl {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewDelegate

Added:

```
public virtual void CellDisplayingEnded (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
        public virtual void FooterViewDisplayingEnded (UITableView tableView, UIView footerView, int section);
        public virtual void HeaderViewDisplayingEnded (UITableView tableView, UIView headerView, int section);
        public virtual void RowHighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
        public virtual void RowUnhighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
        public virtual bool ShouldHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
        public virtual void WillDisplayFooterView (UITableView tableView, UIView footerView, int section);
        public virtual void WillDisplayHeaderView (UITableView tableView, UIView headerView, int section);
```

 <a name="New_Type:_MonoTouch.UIKit.UITableViewHeaderFooterView" class="injected"></a>


## New Type: MonoTouch.UIKit.UITableViewHeaderFooterView

```
public class UITableViewHeaderFooterView : UIView {
        
        public UITableViewHeaderFooterView ();
        public UITableViewHeaderFooterView (MonoTouch.Foundation.NSCoder coder);
        public UITableViewHeaderFooterView (MonoTouch.Foundation.NSObjectFlag t);
        public UITableViewHeaderFooterView (IntPtr handle);
        public UITableViewHeaderFooterView (System.Drawing.RectangleF frame);
        public UITableViewHeaderFooterView (MonoTouch.Foundation.NSString reuseIdentifier);
        
        public static UITableViewHeaderFooterViewAppearance AppearanceWhenContainedIn (params Type [] containers);
        protected override void Dispose (bool disposing);
        public virtual void PrepareForReuse ();
        
        public static UITableViewHeaderFooterViewAppearance Appearance {
                get;
        }
        public virtual UIView BackgroundView {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIView ContentView {
                get;
        }
        public virtual UILabel DetailTextLabel {
                get;
        }
        public virtual MonoTouch.Foundation.NSString ReuseIdentifier {
                get;
        }
        public virtual UILabel TextLabel {
                get;
        }
        public virtual UIColor TintColor {
                get;
        }
        
        public class UITableViewHeaderFooterViewAppearance : UIViewAppearance {
                
                public virtual UIColor TintColor {
                        get;
                }
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextAlignment" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextAlignment

Added:

```
Justified,
        Natural
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

Added:

```
public virtual System.Drawing.RectangleF GetFrameForDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder);
        public virtual UITextSelectionRect[] GetSelectionRects (UITextRange range);
        public virtual MonoTouch.Foundation.NSObject InsertDictationResultPlaceholder ();
        public virtual void RemoveDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder, bool willInsertResult);
        public virtual bool ShouldChangeTextInRange (UITextRange inRange, string replacementText);
        public virtual bool AllowsEditingTextAttributes {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSAttributedString AttributedPlaceholder {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSAttributedString AttributedText {
                get;
                set;
        }
        public virtual bool ClearsOnInsertion {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary TypingAttributes {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UITextSelectionRect" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextSelectionRect

```
public class UITextSelectionRect : MonoTouch.Foundation.NSObject {
        
        public UITextSelectionRect ();
        public UITextSelectionRect (MonoTouch.Foundation.NSCoder coder);
        public UITextSelectionRect (MonoTouch.Foundation.NSObjectFlag t);
        public UITextSelectionRect (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual bool ContainsEnd {
                get;
        }
        public virtual bool ContainsStart {
                get;
        }
        public virtual bool IsVertical {
                get;
        }
        public virtual System.Drawing.RectangleF Rect {
                get;
        }
        public virtual UITextWritingDirection WritingDirection {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

Added:

```
public virtual System.Drawing.RectangleF GetFrameForDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder);
        public virtual UITextSelectionRect[] GetSelectionRects (UITextRange range);
        public virtual MonoTouch.Foundation.NSObject InsertDictationResultPlaceholder ();
        public virtual void RemoveDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder, bool willInsertResult);
        public virtual bool ShouldChangeTextInRange (UITextRange inRange, string replacementText);
        public virtual bool AllowsEditingTextAttributes {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSAttributedString AttributedText {
                get;
                set;
        }
        public virtual bool ClearsOnInsertion {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary TypingAttributes {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIToolbar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIToolbar

Added:

```
public virtual UIImage GetShadowImage (UIToolbarPosition topOrBottom);
        public virtual void SetShadowImage (UIImage shadowImage, UIToolbarPosition topOrBottom);
                public virtual UIImage GetShadowImage (UIToolbarPosition topOrBottom);
                public virtual void SetShadowImage (UIImage shadowImage, UIToolbarPosition topOrBottom);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Removed:

```
public static void BeginAnimations (string s, IntPtr context);
        public virtual System.Drawing.RectangleF ContentStretch {
```

Added:

```
public static void BeginAnimations (string animationID, IntPtr context);
        public static bool RequiresConstraintBasedLayout ();
        public virtual void AddConstraint (NSLayoutConstraint constraint);
        public virtual void AddConstraints (NSLayoutConstraint[] constraints);
        public virtual System.Drawing.RectangleF AlignmentRectForFrame (System.Drawing.RectangleF frame);
        public virtual UILayoutPriority ContentCompressionResistancePriority (UILayoutConstraintAxis axis);
        public virtual UILayoutPriority ContentHuggingPriority (UILayoutConstraintAxis axis);
        public virtual void DecodeRestorableState (MonoTouch.Foundation.NSCoder coder);
        public virtual void EncodeRestorableState (MonoTouch.Foundation.NSCoder coder);
        public virtual void ExerciseAmbiguityInLayout ();
        public virtual System.Drawing.RectangleF FrameForAlignmentRect (System.Drawing.RectangleF alignmentRect);
        public virtual bool GestureRecognizerShouldBegin (UIGestureRecognizer gestureRecognizer);
        public virtual NSLayoutConstraint[] GetConstraintsAffectingLayout (UILayoutConstraintAxis axis);
        public virtual void InvalidateIntrinsicContentSize ();
        public virtual bool NeedsUpdateConstraints ();
        public virtual void RemoveConstraint (NSLayoutConstraint constraint);
        public virtual void RemoveConstraints (NSLayoutConstraint[] constraints);
        public virtual void SetContentCompressionResistancePriority (UILayoutPriority priority, UILayoutConstraintAxis axis);
        public virtual void SetContentHuggingPriority (UILayoutPriority priority, UILayoutConstraintAxis axis);
        public virtual void SetNeedsUpdateConstraints ();
        public virtual System.Drawing.SizeF SystemLayoutSizeFittingSize (System.Drawing.SizeF size);
        public virtual void UpdateConstraints ();
        public virtual void UpdateConstraintsIfNeeded ();
        public static float NoIntrinsicMetric {
                get;
        }
        public static System.Drawing.SizeF UILayoutFittingCompressedSize {
                get;
        }
        public static System.Drawing.SizeF UILayoutFittingExpandedSize {
                get;
        }
        public virtual UIEdgeInsets AlignmentRectInsets {
                get;
        }
        public virtual NSLayoutConstraint[] Constraints {
                get;
        }
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual System.Drawing.RectangleF ContentStretch {
        public virtual bool HasAmbiguousLayout {
                get;
        }
        public virtual System.Drawing.SizeF IntrinsicContentSize {
                get;
        }
        public virtual string RestorationIdentifier {
                get;
        }
        public virtual bool TranslatesAutoresizingMaskIntoConstrainst {
                get;
                set;
        }
        public virtual UIView ViewForBaselineLayout {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

Removed:

```
public virtual void DismissModalViewControllerAnimated (bool animated);
        public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
        public virtual void ViewDidUnload ();
        public virtual void ViewWillUnload ();
        public virtual bool AutomaticallyForwardAppearanceAndRotationMethodsToChildViewControllers {
        public virtual UIViewController ModalViewController {
```

Added:

```
public virtual void BeginAppearanceTransition (bool isAppearing, bool animated);
        public virtual bool CanPerformUnwind (MonoTouch.ObjCRuntime.Selector segueAction, UIViewController fromViewController, MonoTouch.Foundation.NSObject sender);
        public virtual void DecodeRestorableState (MonoTouch.Foundation.NSCoder coder);
        [Obsolete("Deprecated in iOS 6.0, use DismissViewController (bool, NSAction) instead.")]
        public virtual void DismissModalViewControllerAnimated (bool animated);
        public virtual void EncodeRestorableState (MonoTouch.Foundation.NSCoder coder);
        public virtual void EndAppearanceTransition ();
        public virtual UIStoryboardSegue GetSegueForUnwinding (UIViewController toViewController, UIViewController fromViewController, string identifier);
        public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations ();
        public virtual UIViewController GetViewControllerForUnwind (MonoTouch.ObjCRuntime.Selector segueAction, UIViewController fromViewController, MonoTouch.Foundation.NSObject sender);
        public virtual UIInterfaceOrientation PreferredInterfaceOrientationForPresentation ();
        [Obsolete("Deprecated in iOS 6.0, use PresentViewController (UIViewController, bool, NSAction) instead.")]
        public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
        public virtual bool ShouldAutorotate ();
        [Obsolete("Derecated in IOS6")]
        public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
        public virtual bool ShouldPerformSegue (string segueIdentifier, MonoTouch.Foundation.NSObject sender);
        public virtual void UpdateViewConstraints ();
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual void ViewDidUnload ();
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual void ViewWillUnload ();
        [Obsolete("Deprecated in iOS 6.0")]
        public virtual bool AutomaticallyForwardAppearanceAndRotationMethodsToChildViewControllers {
        [Obsolete("Deprecated in iOS 6.0, PresentedViewController")]
        public virtual UIViewController ModalViewController {
        public virtual MonoTouch.ObjCRuntime.Class RestorationClass {
                get;
                set;
        }
        public virtual string RestorationIdentifier {
                get;
        }
        public virtual bool ShouldAutomaticallyForwardAppearanceMethods {
                get;
        }
        public virtual bool ShouldAutomaticallyForwardRotationMethods {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWebView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWebView

Added:

```
public virtual bool KeyboardDisplayRequiresUserAction {
                get;
                set;
        }
        public virtual bool SuppressesIncrementalRendering {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="New_Type:_MonoTouch.iAd.ADAdType" class="injected"></a>


## New Type: MonoTouch.iAd.ADAdType

```
[Serializable]
public enum ADAdType {
        Banner,
        MediumRectangle
}
```

 <a name="Type_Changed:_MonoTouch.iAd.ADBannerView" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADBannerView

Removed:

```
public static System.Drawing.SizeF SizeFromContentSizeIdentifier (string sizeIdentifier);
        public virtual string CurrentContentSizeIdentifier {
        public virtual MonoTouch.Foundation.NSSet RequiredContentSizeIdentifiers {
```

Added:

```
public ADBannerView (ADAdType type);
        [Obsolete("Obsolete in iOS 6.0")]
        public static System.Drawing.SizeF SizeFromContentSizeIdentifier (string sizeIdentifier);
        public virtual ADAdType AdType {
                get;
        }
        [Obsolete("Obsolete in iOS 6.0")]
        public virtual string CurrentContentSizeIdentifier {
        [Obsolete("Obsolete in iOS 6.0")]
        public virtual MonoTouch.Foundation.NSSet RequiredContentSizeIdentifiers {
```

 <a name="Type_Changed:_MonoTouch.iAd.ADError" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADError

Added:

```
AdUnloaded
```

&lt;/body&gt;&lt;/html&gt;
