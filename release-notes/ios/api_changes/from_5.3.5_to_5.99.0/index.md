---
id: A86E22A1-004F-4CE6-8F4A-089B56807092
title: "From 5.3.5 to 5.99.0"
---

<html><head>
<title>Monotouch 5.99.0: iOS 6.0 Beta 3 Support </title>
<link href="prettify.css" type="text/css" rel="stylesheet">
<style type="text/css">
body {
color: #333;
  min-width: 80em;
  max-width: 120em;
}

.release-notes {
}

.release-notes p {
margin-left: 1em;
margin-right: 1em;
}
pre {
background-color: #eee;
padding-top: .5em;
padding-bottom: .5em;
margin-left: 1em;
margin-right: 1em;
overflow: auto;
}

p {
    max-width: 40em;
}
</style>
<script type="text/javascript" src="prettify.js">
</script>
</head>

<body onload="prettyPrint()">
<h2>Overview</h2>

  <p>This document lists the changed between the Beta of
  MonoTouch 5.3.5 which is aimed at iOS 5.1 and MonoTouch 5.99.0
  which expands the support with the iOS 6.0 Beta 3 APIs.

  <p>The iOS 6.0 support contains all of the features available
  in the MonoTouch 5.3.xx series.

<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre class='prettyprint'>
   public const string Version = "5.3.5";
</pre>
<p>Added:</p><pre class='prettyprint'>
   public const string Version = "5.99.0";
   public const string StoreKitLibrary = "/System/Library/Frameworks/StoreKit.framework/StoreKit";
   public const string MediaToolboxLibrary = "/System/Library/Frameworks/MediaToolbox.framework/MediaToolbox";
   public const string PassKitLibrary = "/System/Library/Frameworks/PassKit.framework/PassKit";
   public const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Added:</p><pre class='prettyprint'>
   public virtual AVTimedMetadataGroup[] GetChapterMetadataGroupsBestMatchingPreferredLanguages (string [] preferredLanguages);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetExportSession</h3>
<p>Added:</p><pre class='prettyprint'>
   public static void DetermineCompatibilityOfExportPreset (string presetName, AVAsset asset, string outputFileType, Action&lt;bool&gt; isCompatibleResult);
   public static AVAssetExportSession FromAsset (AVAsset asset, string presetName);
   public virtual void DetermineCompatibleFileTypes (Action&lt;string []&gt; compatibleFileTypesHandler);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator</h3>
<p>Added:</p><pre class='prettyprint'>
   public virtual AVAsset Asset {
     get;
   }
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetResourceLoader</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetResourceLoaderDelegate</h3>
<pre class='prettyprint'>
public abstract class AVAssetResourceLoaderDelegate : MonoTouch.Foundation.NSObject {
  
  public AVAssetResourceLoaderDelegate ();
  public AVAssetResourceLoaderDelegate (MonoTouch.Foundation.NSCoder coder);
  public AVAssetResourceLoaderDelegate (MonoTouch.Foundation.NSObjectFlag t);
  public AVAssetResourceLoaderDelegate (IntPtr handle);
  
  public abstract bool ShouldWaitForLoadingOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAssetResourceLoadingRequest</h3>
<pre class='prettyprint'>
public class AVAssetResourceLoadingRequest : MonoTouch.Foundation.NSObject {
  
  public AVAssetResourceLoadingRequest ();
  public AVAssetResourceLoadingRequest (MonoTouch.Foundation.NSCoder coder);
  public AVAssetResourceLoadingRequest (MonoTouch.Foundation.NSObjectFlag t);
  public AVAssetResourceLoadingRequest (IntPtr handle);
  
  protected override void Dispose (bool disposing);
  public virtual void FinishLoading (MonoTouch.Foundation.NSUrlResponse usingResponse, MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSUrlRequest redirect);
  public virtual void FinishLoadingWithError (MonoTouch.Foundation.NSError error);
  public virtual MonoTouch.Foundation.NSData GetStreamingContentKey (MonoTouch.Foundation.NSData appIdentifier, MonoTouch.Foundation.NSData contentIdentifier, MonoTouch.Foundation.NSDictionary options, MonoTouch.Foundation.NSError outError);
  
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
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput</h3>
<p>Added:</p><pre class='prettyprint'>
   public AVAssetWriterInput (string mediaType, MonoTouch.Foundation.NSDictionary outputSettings, MonoTouch.CoreMedia.CMFormatDescription sourceFormatHint);
   public virtual MonoTouch.CoreMedia.CMFormatDescription SourceFormatHint {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioMixInputParameters</h3>
<p>Added:</p><pre class='prettyprint'>
   public virtual MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioPlayer</h3>
<p>Added:</p><pre class='prettyprint'>
   public virtual AVAudioSessionChannelDescription[] ChannelAssignments {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioRecorder</h3>
<p>Added:</p><pre class='prettyprint'>
   public virtual AVAudioSessionChannelDescription[] ChannelAssignments {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioSession</h3>
<p>Removed:</p><pre class='prettyprint'>
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
</pre>
<p>Added:</p><pre class='prettyprint'>
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
     
      public static MonoTouch.Foundation.NSObject ObserveInterruption (EventHandler&lt;AVAudioSessionInterruptionEventArgs&gt; handler);
      public static MonoTouch.Foundation.NSObject ObserveMediaServicesWereReset (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
      public static MonoTouch.Foundation.NSObject ObserveRouteChange (EventHandler&lt;AVAudioSessionRouteChangeEventArgs&gt; handler);
   }
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionCategoryOptions</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum AVAudioSessionCategoryOptions {
  MixWithOthers,
  DuckOthers,
  AllowBluetooth,
  DefaultToSpeaker
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionChannelDescription</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionDataSourceDescription</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionEventArgs</h3>
<pre class='prettyprint'>
public class AVAudioSessionInterruptionEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
  
   public AVAudioSessionInterruptionEventArgs (MonoTouch.Foundation.NSNotification notification);
  
   public AVAudioSessionInterruptionType InterruptionType {
    get;
  }
   public AVAudioSessionInterruptionOptions Option {
    get;
  }
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionOptions</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum AVAudioSessionInterruptionOptions {
  ShouldResume
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionInterruptionType</h3>
<pre class='prettyprint'>
[Serializable]
public enum AVAudioSessionInterruptionType {
  Ended,
  Began
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionPortDescription</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionPortOverride</h3>
<pre class='prettyprint'>
[Serializable]
public enum AVAudioSessionPortOverride {
  None,
  Speaker
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionRouteChangeEventArgs</h3>
<pre class='prettyprint'>
public class AVAudioSessionRouteChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
  
   public AVAudioSessionRouteChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
  
   public AVAudioSessionRouteDescription PreviousRoute {
    get;
  }
   public AVAudioSessionRouteChangeReason Reason {
    get;
  }
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionRouteChangeReason</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionRouteDescription</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAudioSessionSetActiveOptions</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum AVAudioSessionSetActiveOptions {
  NotifyOthersOnDeactivation
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void DidDropSampleBuffer (AVCaptureOutput captureOutput, MonoTouch.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureConnection</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureDevice</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool SetTorchModeLevel (float torchLevel, out MonoTouch.Foundation.NSError outError);
    public static float MaxAvailableTorchLevel {
     get;
   }
    public virtual bool TorchActive {
     get;
   }
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureDeviceTransportControlsPlaybackMode</h3>
<pre class='prettyprint'>
[Serializable]
public enum AVCaptureDeviceTransportControlsPlaybackMode {
  NotPlaying,
  Playing
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureMetadataOutput</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVCaptureMetadataOutputObjectsDelegate</h3>
<pre class='prettyprint'>
public class AVCaptureMetadataOutputObjectsDelegate : MonoTouch.Foundation.NSObject {
  
   public AVCaptureMetadataOutputObjectsDelegate ();
   public AVCaptureMetadataOutputObjectsDelegate (MonoTouch.Foundation.NSCoder coder);
   public AVCaptureMetadataOutputObjectsDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public AVCaptureMetadataOutputObjectsDelegate (IntPtr handle);
  
   public virtual void DidOutputMetadataObjects (AVCaptureMetadataOutput captureOutput, AVMetadataObject[] metadataObjects, AVCaptureConnection connection);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureOutput</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual AVMetadataObject GetTransformedMetadataObject (AVMetadataObject metadataObject, AVCaptureConnection connection);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual bool AutomaticallyAdjustsMirroring {
    public virtual bool Mirrored {
    public virtual bool MirroringSupported {
    public virtual AVCaptureVideoOrientation Orientation {
    public virtual bool OrientationSupported {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual System.Drawing.PointF CaptureDevicePointOfInterestForPoint (System.Drawing.PointF pointInLayer);
    public virtual AVMetadataObject GetTransformedMetadataObject (AVMetadataObject metadataObject);
    public virtual System.Drawing.PointF PointForCaptureDevicePointOfInterest (System.Drawing.PointF captureDevicePointOfInterest);
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool AutomaticallyAdjustsMirroring {
    public virtual AVCaptureConnection Connection {
     get;
   }
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool Mirrored {
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool MirroringSupported {
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual AVCaptureVideoOrientation Orientation {
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool OrientationSupported {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVError</h3>
<p>Removed:</p><pre class='prettyprint'>
   InvalidOutputURLPathExtension
</pre>
<p>Added:</p><pre class='prettyprint'>
   InvalidOutputURLPathExtension,
   ScreenCaptureFailed,
   DisplayWasDisabled,
   TorchLevelUnavailable,
   OperationInterrupted,
   IncompatibleAsset,
   FailedToLoadMediaData,
   ServerIncorrectlyConfigured
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaCharacteristic</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString EasyToRead {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaSelectionGroup</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (MonoTouch.Foundation.NSArray array, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (AVMediaSelectionOption[] source, MonoTouch.Foundation.NSString[] avmediaCharacteristics);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMediaType</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString Metadata {
     get;
   }
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVMetadataFaceObject</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadataItem</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static AVMetadataItem[] FilterWithKey (AVMetadataItem[] array, MonoTouch.Foundation.NSObject key, string keySpace);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static AVMetadataItem[] FilterFromPreferredLanguages (AVMetadataItem[] metadataItems, string [] preferredLanguages);
    public static AVMetadataItem[] FilterWithKey (AVMetadataItem[] metadataItems, MonoTouch.Foundation.NSObject key, string keySpace);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVMetadataObject</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayer</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void CancelPendingPrerolls ();
    public virtual void Preroll (float rate, AVCompletion onComplete);
    public virtual void Seek (MonoTouch.Foundation.NSDate date);
    public virtual void Seek (MonoTouch.Foundation.NSDate date, AVCompletion onComplete);
    public virtual void SetRate (float rate, MonoTouch.CoreMedia.CMTime itemTime, MonoTouch.CoreMedia.CMTime hostClockTime);
    public virtual MonoTouch.CoreMedia.CMClock MasterClock {
     get;
   }
    public virtual bool OutputObscuredDueToInsufficientExternalProtection {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Added:</p><pre class='prettyprint'>
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
      public static MonoTouch.Foundation.NSObject ObserveNewAccessLogEntry (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
      public static MonoTouch.Foundation.NSObject ObserveNewErrorLogEntry (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
      public static MonoTouch.Foundation.NSObject ObservePlaybackStalled (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual int NumberOfMediaRequests {
     get;
   }
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemOutput</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemOutputPullDelegate</h3>
<pre class='prettyprint'>
public class AVPlayerItemOutputPullDelegate : MonoTouch.Foundation.NSObject {
  
   public AVPlayerItemOutputPullDelegate ();
   public AVPlayerItemOutputPullDelegate (MonoTouch.Foundation.NSCoder coder);
   public AVPlayerItemOutputPullDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public AVPlayerItemOutputPullDelegate (IntPtr handle);
  
   public virtual void OutputMediaDataWillChange (AVPlayerItemOutput sender);
   public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemVideoOutput</h3>
<pre class='prettyprint'>
public class AVPlayerItemVideoOutput : AVPlayerItemOutput {
  
   public AVPlayerItemVideoOutput ();
   public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSCoder coder);
   public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSObjectFlag t);
   public AVPlayerItemVideoOutput (IntPtr handle);
   public AVPlayerItemVideoOutput (MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
  
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
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVTextStyleRule</h3>
<pre class='prettyprint'>
public class AVTextStyleRule : MonoTouch.Foundation.NSObject {
  
   public AVTextStyleRule ();
   public AVTextStyleRule (MonoTouch.Foundation.NSCoder coder);
   public AVTextStyleRule (MonoTouch.Foundation.NSObjectFlag t);
   public AVTextStyleRule (IntPtr handle);
   public AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
   public AVTextStyleRule (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
  
   public static AVTextStyleRule[] FromPropertyList (MonoTouch.Foundation.NSObject plist);
   public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.Foundation.NSDictionary textMarkupAttributes);
   public static AVTextStyleRule FromTextMarkupAttributes (MonoTouch.Foundation.NSDictionary textMarkupAttributes, string textSelector);
   public static MonoTouch.Foundation.NSObject ToPropertyList (AVTextStyleRule[] textStyleRules);
  protected override void Dispose (bool disposing);
  
   public override IntPtr ClassHandle {
    get;
  }
   public virtual MonoTouch.Foundation.NSDictionary TextMarkupAttributes {
    get;
  }
   public virtual string TextSelector {
    get;
  }
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVUrlAsset</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual AVAssetResourceLoader ResourceLoader {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString ProfileLevelH264High40 {
     get;
   }
    public static MonoTouch.Foundation.NSString ProfileLevelH264High41 {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoComposition</h3>
<p>Added:</p><pre class='prettyprint'>
    public static AVVideoComposition FromAssetProperties (AVAsset asset);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoFieldMode</h3>
<pre class='prettyprint'>
[Serializable]
public enum AVVideoFieldMode {
  Both,
  TopOnly,
  BottomOnly,
  Deinterlace
}
</pre>
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccountCredential</h3>
<p>Removed:</p><pre class='prettyprint'>
    public ACAccountCredential (string token, string secret);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public ACAccountCredential (string oauthToken, string tokenSecret);
    public ACAccountCredential (string oauth2Token, string refreshToken, MonoTouch.Foundation.NSDate expiryDate);
    public virtual string OAuthToken {
     get;
     set;
   }
</pre>
<h3>New Type: MonoTouch.Accounts.ACAccountCredentialRenewResult</h3>
<pre class='prettyprint'>
[Serializable]
public enum ACAccountCredentialRenewResult {
  Renewed,
  Rejected,
  Failed
}
</pre>
<h3>Type Changed: MonoTouch.Accounts.ACAccountStore</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void RenewCredentials (ACAccount account, System.Action&lt;ACAccountCredentialRenewResult,MonoTouch.Foundation.NSError&gt; completionHandler);
   [Obsolete("Obsolete in iOS 6.0")]
   public virtual void RequestAccess (ACAccountType accountType, ACRequestCompletionHandler completionHandler);
    public virtual void RequestAccessToAccount (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options, ACRequestCompletionHandler completion);
</pre>
<h3>Type Changed: MonoTouch.Accounts.ACAccountType</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString Facebook {
     get;
   }
    public static MonoTouch.Foundation.NSString SinaWeibo {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.Accounts.ACErrorCode</h3>
<p>Removed:</p><pre class='prettyprint'>
   PermissionDenied
</pre>
<p>Added:</p><pre class='prettyprint'>
   PermissionDenied,
   AccessInfoInvalid
</pre>
<h3>New Type: MonoTouch.Accounts.ACFacebook</h3>
<pre class='prettyprint'>
public class ACFacebook {
  
   public ACFacebook ();
  
   public static MonoTouch.Foundation.NSString AppIdKey {
    get;
  }
   public static MonoTouch.Foundation.NSString AppVersionKey {
    get;
  }
   public static MonoTouch.Foundation.NSString PermissionGroupKey {
    get;
  }
   public static MonoTouch.Foundation.NSString PermissionGroupRead {
    get;
  }
   public static MonoTouch.Foundation.NSString PermissionGroupReadWrite {
    get;
  }
   public static MonoTouch.Foundation.NSString PermissionGroupWrite {
    get;
  }
   public static MonoTouch.Foundation.NSString PermissionsKey {
    get;
  }
}
</pre>
<h2>Namespace: MonoTouch.AddressBook</h2>
<h3>Type Changed: MonoTouch.AddressBook.ABAddressBook</h3>
<p>Added:</p><pre class='prettyprint'>
    public static ABAddressBook FromOptions (MonoTouch.Foundation.NSDictionary dictionary, out MonoTouch.Foundation.NSError outError);
    public static ABAuthorizationStatus GetAuthorizationStatus ();
    public void RequestAccess (System.Action&lt;bool,MonoTouch.Foundation.NSError&gt; onCompleted);
</pre>
<h3>Type Changed: MonoTouch.AddressBook.ABAddressBookError</h3>
<p>Removed:</p><pre class='prettyprint'>
   OperationNotPermittedByStore
</pre>
<p>Added:</p><pre class='prettyprint'>
   OperationNotPermittedByStore,
   NotPermittedByUserError
</pre>
<h3>New Type: MonoTouch.AddressBook.ABAuthorizationStatus</h3>
<pre class='prettyprint'>
[Serializable]
public enum ABAuthorizationStatus {
  NotDetermined,
  Restricted,
  Denied,
  Authorized
}
</pre>
<h2>Namespace: MonoTouch.AssetsLibrary</h2>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAsset</h3>
<p>Added:</p><pre class='prettyprint'>
    public MonoTouch.Foundation.NSUrl AssetUrl {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.AssetsLibrary.ALAuthorizationStatus</h3>
<pre class='prettyprint'>
[Serializable]
public enum ALAuthorizationStatus {
  NotDetermined,
  Restricted,
  Denied,
  Authorized
}
</pre>
<h2>Namespace: MonoTouch.AudioUnit</h2>
<h3>Type Changed: MonoTouch.AudioUnit.AudioTypeConverter</h3>
<p>Removed:</p><pre class='prettyprint'>
   AUiPodTime
</pre>
<p>Added:</p><pre class='prettyprint'>
   Varispeed,
   DeferredRenderer,
   Splitter,
   Merger,
   NewTimePitch,
   AUiPodTime,
   AUiPodTimeOther
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioTypeEffect</h3>
<p>Removed:</p><pre class='prettyprint'>
   AUiPodEQ
</pre>
<p>Added:</p><pre class='prettyprint'>
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
   AUiPodEQ,
   Reverb2,
   NBandEq
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioTypeMixer</h3>
<p>Added:</p><pre class='prettyprint'>
   Matrix,
</pre>
<h2>Namespace: MonoTouch.CoreAnimation</h2>
<h3>Type Changed: MonoTouch.CoreAnimation.CALayer</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool DrawsAsynchronously {
     get;
     set;
   }
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>New Type: MonoTouch.CoreBluetooth.CBATTError</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBATTRequest</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBATTRequestEventArgs</h3>
<pre class='prettyprint'>
public class CBATTRequestEventArgs : EventArgs {
  
   public CBATTRequestEventArgs (CBATTRequest request);
  
   public CBATTRequest Request {
    get;
    set;
  }
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBATTRequestsEventArgs</h3>
<pre class='prettyprint'>
public class CBATTRequestsEventArgs : EventArgs {
  
   public CBATTRequestsEventArgs (CBATTRequest[] requests);
  
   public CBATTRequest[] Requests {
    get;
    set;
  }
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBAttributePermissions</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum CBAttributePermissions {
  Readable,
  Writeable,
  ReadEncryptionRequired,
  WriteEncryptionRequired
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBCentral</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Removed:</p><pre class='prettyprint'>
    public CBCentralManager (CBCentralManagerDelegate cbDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public CBCentralManager (CBCentralManagerDelegate centralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
    public static MonoTouch.Foundation.NSString OptionNotifyOnConnectionKey {
     get;
   }
    public static MonoTouch.Foundation.NSString OptionNotifyOnNotificationKey {
     get;
   }
   
    public event EventHandler&lt;CBPeripheralEventArgs&gt; ConnectedPeripheral;
    public event EventHandler&lt;CBPeripheralErrorEventArgs&gt; DisconnectedPeripheral;
    public event EventHandler&lt;CBDiscoveredPeripheralEventArgs&gt; DiscoveredPeripheral;
    public event EventHandler&lt;CBPeripheralErrorEventArgs&gt; FailedToConnectPeripheral;
    public event EventHandler&lt;CBPeripheralEventArgs&gt; RetrievedConnectedPeripherals;
    public event EventHandler&lt;CBPeripheralsEventArgs&gt; RetrievedPeripherals;
    public event EventHandler UpdatedState;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Removed:</p><pre class='prettyprint'>
    public abstract void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);
    public abstract void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
    public abstract void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
    public abstract void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
    public abstract void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
    public abstract void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void ConnectedPeripheral (CBCentralManager central, CBPeripheral peripheral);
    public virtual void DisconnectedPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
    public virtual void DiscoveredPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSDictionary advertisementData, MonoTouch.Foundation.NSNumber RSSI);
    public virtual void FailedToConnectPeripheral (CBCentralManager central, CBPeripheral peripheral, MonoTouch.Foundation.NSError error);
    public virtual void RetrievedConnectedPeripherals (CBCentralManager central, CBPeripheral peripherals);
    public virtual void RetrievedPeripherals (CBCentralManager central, CBPeripheral[] peripherals);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBCharacteristicEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCharacteristicProperties</h3>
<p>Removed:</p><pre class='prettyprint'>
   ExtendedProperties
</pre>
<p>Added:</p><pre class='prettyprint'>
   ExtendedProperties,
   NotifyEncryptionRequired,
   IndicateEncryptionRequired
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBDescriptorEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBDiscoveredPeripheralEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBError</h3>
<p>Removed:</p><pre class='prettyprint'>
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
</pre>
<p>Added:</p><pre class='prettyprint'>
   Unknown,
   InvalidParameters,
   NotConnected,
   OutOfSpace,
   OperationCancelled,
   ConnectionTimeout,
   PeripheralDisconnected,
   UUIDNotAllowed,
   AlreadyAdvertising
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBMutableCharacteristic</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBMutableDescriptor</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBMutableService</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void SetNotifyValue (bool notifyValue, CBCharacteristic characteristic);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void SetNotifyValue (bool enabled, CBCharacteristic characteristic);
   
    public event EventHandler&lt;CBServiceEventArgs&gt; DiscoverCharacteristic;
    public event EventHandler&lt;CBCharacteristicEventArgs&gt; DiscoveredDescriptor;
    public event EventHandler&lt;CBServiceEventArgs&gt; DiscoveredIncludedService;
    public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; DiscoveredService;
    public event EventHandler InvalidatedService;
    public event System.EventHandler&lt;MonoTouch.Foundation.NSErrorEventArgs&gt; RssiUpdated;
    public event EventHandler&lt;CBCharacteristicEventArgs&gt; UpdatedCharacterteristicValue;
    public event EventHandler UpdatedName;
    public event EventHandler&lt;CBCharacteristicEventArgs&gt; UpdatedNotificationState;
    public event EventHandler&lt;CBDescriptorEventArgs&gt; UpdatedValue;
    public event EventHandler&lt;CBCharacteristicEventArgs&gt; WroteCharacteristicValue;
    public event EventHandler&lt;CBDescriptorEventArgs&gt; WroteDescriptorValue;
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void InvalidatedService (CBPeripheral peripheral);
    public virtual void UpdatedName (CBPeripheral peripheral);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralErrorEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralEventArgs</h3>
<pre class='prettyprint'>
public class CBPeripheralEventArgs : EventArgs {
  
   public CBPeripheralEventArgs (CBPeripheral peripherals);
  
   public CBPeripheral Peripherals {
    get;
    set;
  }
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<pre class='prettyprint'>
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
   public virtual void StartAdvertising (MonoTouch.Foundation.NSDictionary advertisementData);
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
   public event EventHandler UpdatedState;
   public event EventHandler<cbattrequestseventargs> WriteRequestsReceived;
}
</cbattrequestseventargs></cbperipheralmanagerserviceeventargs></cbattrequesteventargs></cbperipheralmanagersubscriptioneventargs></cbperipheralmanagersubscriptioneventargs></monotouch.foundation.nserroreventargs></pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerConnectionLatency</h3>
<pre class='prettyprint'>
[Serializable]
public enum CBPeripheralManagerConnectionLatency {
  Low,
  Medium,
  High
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<pre class='prettyprint'>
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
   public abstract void UpdatedState (CBPeripheralManager peripheral);
   public virtual void WriteRequestsReceived (CBPeripheralManager peripheral, CBATTRequest[] requests);
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerServiceEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerState</h3>
<pre class='prettyprint'>
[Serializable]
public enum CBPeripheralManagerState {
  Unknown,
  Resetting,
  Unsupported,
  Unauthorized,
  PoweredOff,
  PoweredOn
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralManagerSubscriptionEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralsEventArgs</h3>
<pre class='prettyprint'>
public class CBPeripheralsEventArgs : EventArgs {
  
   public CBPeripheralsEventArgs (CBPeripheral[] peripherals);
  
   public CBPeripheral[] Peripherals {
    get;
    set;
  }
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBService</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool Primary {
     get;
   }
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBServiceEventArgs</h3>
<pre class='prettyprint'>
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
</pre>
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>New Type: MonoTouch.CoreFoundation.CFAllocator</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreFoundation.CFAllocatorFlags</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum CFAllocatorFlags : ulong {
  GCScannedMemory,
  GCObjectMemory
}
</pre>
<h2>Namespace: MonoTouch.CoreImage</h2>
<h3>Type Changed: MonoTouch.CoreImage.CIContext</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Use DrawImage (CIImage, RectangleF, RectangleF) instead")]
   public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIDetector</h3>
<p>Added:</p><pre class='prettyprint'>
    public static CIDetector CreateFaceDetector (CIContext context, bool highAccuracy, float minFeatureSize);
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFaceFeature</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFilter</h3>
<p>Added:</p><pre class='prettyprint'>
    public static CIFilter[] FromSerializedXMP (MonoTouch.Foundation.NSData xmpData, System.Drawing.RectangleF extent, out MonoTouch.Foundation.NSError error);
    public static MonoTouch.Foundation.NSData SerializedXMP (CIFilter[] filters, System.Drawing.RectangleF extent);
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIFilterInputKey</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString Versionkey {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIImage</h3>
<p>Removed:</p><pre class='prettyprint'>
    public CIImage (int glTextureName, System.Drawing.SizeF size, bool flag, MonoTouch.CoreGraphics.CGColorSpace cs);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public CIImage (int glTextureName, System.Drawing.SizeF size, bool flipped, MonoTouch.CoreGraphics.CGColorSpace cs);
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>New Type: MonoTouch.CoreLocation.CLActivityType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CLActivityType {
  Other,
  VehicularNavigation,
  Fitness
}
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLAuthorizationChangedEventArgs</h3>
<pre class='prettyprint'>
public class CLAuthorizationChangedEventArgs : EventArgs {
  
   public CLAuthorizationChangedEventArgs (CLAuthorizationStatus status);
  
   public CLAuthorizationStatus Status {
    get;
    set;
  }
}
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLAuthroziationChangedEventArgs</h3>
<p>Removed:</p><pre class='prettyprint'>
 public class CLAuthroziationChangedEventArgs : EventArgs {
   
    public CLAuthorizationStatus Status {
     get;
     set;
   }
</pre>
<p>Added:</p><pre class='prettyprint'>
 [Obsolete]
public class CLAuthroziationChangedEventArgs : CLAuthorizationChangedEventArgs {
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocation</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual double Distancefrom (CLLocation location);
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Replaced by DistanceFrom")]
   public virtual double Distancefrom (CLLocation location);
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLLocationDistance</h3>
<pre class='prettyprint'>
public static class CLLocationDistance {
  
   public static double FilterNone {
    get;
  }
   public static double MaxDistance {
    get;
  }
}
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
    public static bool RegionMonitoringEnabled {
    public virtual string Purpose {
    public event EventHandler&lt;CLAuthroziationChangedEventArgs&gt; AuthorizationChanged;
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual void StartMonitoring (CLRegion region, double desiredAccuracy);
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
    public event EventHandler&lt;CLAuthorizationChangedEventArgs&gt; AuthorizationChanged;
    public event EventHandler&lt;CLLocationsUpdatedEventArgs&gt; LocationsUpdated;
    public event EventHandler LocationUpdatesPaused;
    public event EventHandler LocationUpdatesResumed;
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void UpdatedLocation (CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void LocationsUpdated (CLLocationManager manager, CLLocation[] locations);
    public virtual void LocationUpdatesPaused (CLLocationManager manager);
    public virtual void LocationUpdatesResumed (CLLocationManager manager);
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual void UpdatedLocation (CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
</pre>
<h3>New Type: MonoTouch.CoreLocation.CLLocationsUpdatedEventArgs</h3>
<pre class='prettyprint'>
public class CLLocationsUpdatedEventArgs : EventArgs {
  
   public CLLocationsUpdatedEventArgs (CLLocation[] locations);
  
   public CLLocation[] Locations {
    get;
    set;
  }
}
</pre>
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>New Type: MonoTouch.CoreMedia.CMAudioFormatDescription</h3>
<pre class='prettyprint'>
public class CMAudioFormatDescription : CMFormatDescription {
}
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMBlockBuffer</h3>
<p>Removed:</p><pre class='prettyprint'>
    public int CopyDataBytes (uint offsetToData, uint dataLength, IntPtr destination);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static CMBlockBuffer CreateEmpty (uint subBlockCapacity, CMBlockBufferFlags flags, out CMBlockBufferError error);
    public CMBlockBufferError CopyDataBytes (uint offsetToData, uint dataLength, IntPtr destination);
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMBlockBufferError</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMBlockBufferFlags</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum CMBlockBufferFlags : uint {
  AssureMemoryNow,
  AlwaysCopyData,
  DontOptimizeDepth,
  PermitEmptyReference
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMClock</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMClockError</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMClockError {
  None,
  MissingRequiredParameter,
  InvalidParameter,
  AllocationFailed,
  UnsupportedOperation
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMClockOrTimebase</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMClosedCaptionFormatType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMClosedCaptionFormatType : uint {
  CEA608,
  CEA708,
  ATSC
}
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMFormatDescription</h3>
<p>Removed:</p><pre class='prettyprint'>
    public System.Drawing.RectangleF GetVideoCleanAperture (bool originIsAtTopLeft);
    public System.Drawing.SizeF GetVideoPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
    public uint MediaSubType {
    public System.Drawing.Size VideoDimensions {
</pre>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMFormatDescriptionError</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMFormatDescriptionError {
  None,
  InvalidParameter,
  AllocationFailed
}
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMMediaType</h3>
<p>Removed:</p><pre class='prettyprint'>
   TimedMetadata
</pre>
<p>Added:</p><pre class='prettyprint'>
   TimedMetadata,
   Metadata
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMMemoryPool</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMMetadataFormatType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMMetadataFormatType : uint {
  ICY,
  ID3,
  Boxed
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMMuxedStreamType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMMuxedStreamType : uint {
  MPEG1System,
  MPEG2Transport,
  MPEG2Program,
  DV
}
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMSampleBuffer</h3>
<p>Removed:</p><pre class='prettyprint'>
    public CMFormatDescription GetFormatDescription ();
    public MonoTouch.Foundation.NSMutableDictionary[] GetSampleAttachments (bool createIfNecessary);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static CMSampleBuffer CreateForImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, bool dataReady, CMVideoFormatDescription formatDescription, CMSampleTimingInfo sampleTiming, out CMSampleBufferError error);
    public static CMSampleBuffer CreateWithPacketDescriptions (CMBlockBuffer dataBuffer, CMFormatDescription formatDescription, int samplesCount, CMTime sampleTimestamp, MonoTouch.AudioToolbox.AudioStreamPacketDescription[] packetDescriptions, out CMSampleBufferError error);
    public CMAudioFormatDescription GetAudioFormatDescription ();
   [Obsolete("Use GetAudioFormatDescription or GetVideoFormatDescription")]
   public CMFormatDescription GetFormatDescription ();
    public CMSampleBufferAttachmentSettings[] GetSampleAttachments (bool createIfNecessary);
    public CMVideoFormatDescription GetVideoFormatDescription ();
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMSampleBufferAttachmentSettings</h3>
<pre class='prettyprint'>
public class CMSampleBufferAttachmentSettings {
  
   public Nullable<bool> DependedOnByOthers {
    get;
    set;
  }
   public Nullable<bool> DependsOnOthers {
    get;
    set;
  }
   public MonoTouch.Foundation.NSDictionary Dictionary {
    get;
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
</bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></bool></pre>
<h3>New Type: MonoTouch.CoreMedia.CMSampleBufferError</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMSampleTimingInfo</h3>
<pre class='prettyprint'>
public struct CMSampleTimingInfo {
  
   public CMTime Duration;
   public CMTime PresentationTimeStamp;
   public CMTime DecodeTimeStamp;
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMSubtitleFormatType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMSubtitleFormatType : uint {
  Text3G,
  WebVTT
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMSyncError</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMSyncError {
  None,
  MissingRequiredParameter,
  InvalidParameter,
  AllocationFailed,
  RateMustBeNonZero
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMTimeCodeFormatType</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMTimeCodeFormatType : uint {
  TimeCode32,
  TimeCode64,
  Counter32,
  Counter64
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMTimeScale</h3>
<pre class='prettyprint'>
public struct CMTimeScale {
  
   public CMTimeScale (int value);
  
   public static readonly CMTimeScale MaxValue;
   public int Value;
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMTimebase</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMTimebaseError</h3>
<pre class='prettyprint'>
[Serializable]
public enum CMTimebaseError {
  None,
  MissingRequiredParameter,
  InvalidParameter,
  AllocationFailed,
  TimerIntervalTooShort,
  ReadOnly
}
</pre>
<h3>New Type: MonoTouch.CoreMedia.CMVideoFormatDescription</h3>
<pre class='prettyprint'>
public class CMVideoFormatDescription : CMFormatDescription {
  
   public CMVideoFormatDescription (CMVideoCodecType codecType, System.Drawing.Size size);
  
   public static CMVideoFormatDescription CreateForImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, out CMFormatDescriptionError error);
   public System.Drawing.RectangleF GetCleanAperture (bool originIsAtTopLeft);
   public System.Drawing.SizeF GetPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
  
   public System.Drawing.Size Dimensions {
    get;
  }
}
</pre>
<h2>Namespace: MonoTouch.CoreMidi</h2>
<h3>Type Changed: MonoTouch.CoreMidi.MidiError</h3>
<p>Removed:</p><pre class='prettyprint'>
   IDNotUnique
</pre>
<p>Added:</p><pre class='prettyprint'>
   IDNotUnique,
   NotPermitted
</pre>
<h2>Namespace: MonoTouch.CoreTelephony</h2>
<h3>New Type: MonoTouch.CoreTelephony.CTErrorDomain</h3>
<pre class='prettyprint'>
[Serializable]
public enum CTErrorDomain {
  NoError,
  Posix,
  Mach
}
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>New Type: MonoTouch.CoreText.CTBaselineClass</h3>
<pre class='prettyprint'>
[Serializable]
public enum CTBaselineClass {
  Roman,
  IdeographicCentered,
  IdeographicLow,
  IdeographicHigh,
  Hanging,
  Math
}
</pre>
<h3>New Type: MonoTouch.CoreText.CTBaselineFont</h3>
<pre class='prettyprint'>
[Serializable]
public enum CTBaselineFont {
  Reference,
  Original
}
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFont</h3>
<p>Added:</p><pre class='prettyprint'>
    public System.Drawing.RectangleF GetOpticalBounds (ushort [] glyphs, System.Drawing.RectangleF [] boundingRects, int count, CTFontOptions options);
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFontSymbolicTraits</h3>
<p>Removed:</p><pre class='prettyprint'>
   ColorGlyphs
</pre>
<p>Added:</p><pre class='prettyprint'>
   ColorGlyphs,
   Composite,
   Mask
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTFontTable</h3>
<p>Removed:</p><pre class='prettyprint'>
   SExtendedBitmapData
</pre>
<p>Added:</p><pre class='prettyprint'>
   SExtendedBitmapData,
   AnchorPoints
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTLine</h3>
<p>Added:</p><pre class='prettyprint'>
    public System.Drawing.RectangleF GetBounds (CTLineBoundsOptions options);
</pre>
<h3>New Type: MonoTouch.CoreText.CTLineBoundsOptions</h3>
<pre class='prettyprint'>
[Serializable]
public enum CTLineBoundsOptions {
  ExcludeTypographicLeading,
  ExcludeTypographicShifts,
  UseHangingPunctuation,
  UseGlyphPathBounds,
  UseOpticalBounds
}
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTStringAttributes</h3>
<p>Added:</p><pre class='prettyprint'>
    public void SetBaselineInfo (CTBaselineClass baselineClass, double offset);
    public void SetBaselineReferenceInfo (CTBaselineClass baselineClass, double offset);
    public void SetWritingDirection (params CTWritingDirection[] writingDirections);
   
    public Nullable&lt;CTBaselineClass&gt; BaselineClass {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTTypesetterOptionKey</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete]
   public static readonly MonoTouch.Foundation.NSString DisableBidiProcessing;
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTTypesetterOptions</h3>
<p>Removed:</p><pre class='prettyprint'>
    public bool DisableBidiProcessing {
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete]
   public bool DisableBidiProcessing {
</pre>
<h3>Type Changed: MonoTouch.CoreText.CTWritingDirection</h3>
<p>Removed:</p><pre class='prettyprint'>
   RightToLeft
</pre>
<p>Added:</p><pre class='prettyprint'>
 [Flags]
   RightToLeft,
   Embedding,
   Override
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h3>
<p>Added:</p><pre class='prettyprint'>
    public bool IsFlipped {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.CoreVideo.CVPixelBuffer</h3>
<p>Added:</p><pre class='prettyprint'>
    public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormat);
    public static readonly MonoTouch.Foundation.NSString OpenGLESCompatibilityKey;
</pre>
<h3>Type Changed: MonoTouch.CoreVideo.CVPixelFormatType</h3>
<p>Removed:</p><pre class='prettyprint'>
   TwoComponent8
</pre>
<p>Added:</p><pre class='prettyprint'>
   TwoComponent8,
   OneComponent16Half,
   OneComponent32Float,
   TwoComponent16Half,
   TwoComponent32Float,
   CV64RGBAHalf,
   CV128RGBAFloat
</pre>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKAlarm</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual EKAlarmProximity Proximity {
     get;
     set;
   }
    public virtual EKStructuredLocation StructuredLocation {
     get;
     set;
   }
</pre>
<h3>New Type: MonoTouch.EventKit.EKAlarmProximity</h3>
<pre class='prettyprint'>
[Serializable]
public enum EKAlarmProximity {
  None,
  Enter,
  Leave
}
</pre>
<h3>New Type: MonoTouch.EventKit.EKAuthorizationStatus</h3>
<pre class='prettyprint'>
[Serializable]
public enum EKAuthorizationStatus {
  NotDetermined,
  Restricted,
  Denied,
  Authorized
}
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKCalendar</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static EKCalendar FromEventStore (EKEventStore eventStore);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static EKCalendar Create (EKEntityType entityType, EKEventStore eventStore);
   [Obsolete("Deprecated in iOS 6.0, use Create(EKEntityType, EKEventStore) instead")]
   public static EKCalendar FromEventStore (EKEventStore eventStore);
    public virtual EKEntityMask AllowedEntityTypes {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKCalendarItem</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual string UUID {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual string CalendarItemExternalIdentifier {
     get;
   }
    public virtual string CalendarItemIdentifier {
     get;
   }
   [Obsolete("Method obsoleted in iOS 6.0")]
   public virtual string UUID {
</pre>
<h3>New Type: MonoTouch.EventKit.EKEntityMask</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum EKEntityMask {
  Event,
  Reminder
}
</pre>
<h3>New Type: MonoTouch.EventKit.EKEntityType</h3>
<pre class='prettyprint'>
[Serializable]
public enum EKEntityType {
  Event,
  Reminder
}
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKErrorCode</h3>
<p>Removed:</p><pre class='prettyprint'>
   SourceDoesNotAllowCalendarAddDelete
</pre>
<p>Added:</p><pre class='prettyprint'>
   SourceDoesNotAllowCalendarAddDelete,
   RecurringReminderRequiresDueDate,
   StructuredLocationsNotSupported,
   ReminderLocationsNotSupported,
   AlarmProximityNotSupported,
   CalendarDoesNotAllowEvents,
   CalendarDoesNotAllowReminders,
   SourceDoesNotAllowReminders,
   PriorityIsInvalid,
   InvalidEntityType
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKEvent</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual EKRecurrenceRule RecurrenceRule {
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Removed in iOS 6.0")]
   public virtual EKRecurrenceRule RecurrenceRule {
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKEventStore</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual bool RemoveCalendarc (EKCalendar calendar, bool commit, out MonoTouch.Foundation.NSError error);
    public virtual EKCalendar[] Calendars {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public EKEventStore (EKEntityMask entityTypes);
    public virtual void CancelFetchRequest (IntPtr fetchIdentifier);
    public virtual IntPtr FetchReminders (MonoTouch.Foundation.NSPredicate predicate, Action&lt;EKReminder[]&gt; completion);
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
    public virtual void RequestAccess (EKEntityType entityType, System.Action&lt;bool,MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual bool SaveReminder (EKReminder reminder, bool commit, out MonoTouch.Foundation.NSError error);
   [Obsolete("Replaced by GetCalendars in iOS 6.0")]
   public virtual EKCalendar[] Calendars {
    public virtual EKCalendar DefaultCalendarForNewReminders {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKParticipant</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool IsCurrentUser {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKRecurrenceDayOfWeek</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek);
    public static MonoTouch.Foundation.NSObject FromDay (EKDay dayOfTheWeek, int weekNumber);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static EKRecurrenceDayOfWeek FromDay (EKDay dayOfTheWeek);
    public static EKRecurrenceDayOfWeek FromDay (EKDay dayOfTheWeek, int weekNumber);
</pre>
<h3>New Type: MonoTouch.EventKit.EKReminder</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKSource</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSSet Calendars {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSSet GetCalendars (EKEntityType entityType);
   [Obsolete("Replaced by GetCalendars in iOS 6.0")]
   public virtual MonoTouch.Foundation.NSSet Calendars {
</pre>
<h3>New Type: MonoTouch.EventKit.EKStructuredLocation</h3>
<pre class='prettyprint'>
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
</pre>
<h2>Namespace: MonoTouch.EventKitUI</h2>
<h3>Type Changed: MonoTouch.EventKitUI.EKCalendarChooser</h3>
<p>Added:</p><pre class='prettyprint'>
    public EKCalendarChooser (EKCalendarChooserSelectionStyle selectionStyle, EKCalendarChooserDisplayStyle displayStyle, MonoTouch.EventKit.EKEntityType entityType, MonoTouch.EventKit.EKEventStore eventStore);
</pre>
<h3>Type Changed: MonoTouch.EventKitUI.EKEventEditViewController</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void CancelEditing ();
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessory</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSData WakeToken {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryEventArgs</h3>
<p>Added:</p><pre class='prettyprint'>
    public EAAccessory Selected {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void ShowBluetoothAccessoryPicker (MonoTouch.Foundation.NSPredicate nameFilterPredicate, System.Action&lt;MonoTouch.Foundation.NSError&gt; completion);
    public virtual void WakeAccessoryWithToken (MonoTouch.Foundation.NSData wakeToken);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void DrawString (System.Drawing.PointF point);
    public virtual void DrawString (System.Drawing.RectangleF rect);
    public virtual void DrawString (System.Drawing.RectangleF rect, NSStringDrawingOptions options, NSStringDrawingContext context);
    public virtual System.Drawing.RectangleF GetBoundingRect (System.Drawing.SizeF size, NSStringDrawingOptions options, NSStringDrawingContext context);
    public static NSString BackgroundColorAttributeName {
     get;
   }
    public static NSString FontAttributeName {
     get;
   }
    public static NSString ForegroundColorAttributeName {
     get;
   }
    public static NSString KernAttributeName {
     get;
   }
    public static NSString LigatureAttributeName {
     get;
   }
    public static NSString ParagraphStyleAttributeName {
     get;
   }
    public static NSString ShadowAttributeName {
     get;
   }
    public static NSString StrikethroughStyleAttributeName {
     get;
   }
    public static NSString StrokeColorAttributeName {
     get;
   }
    public static NSString StrokeWidthAttributeName {
     get;
   }
    public static NSString UnderlineStyleAttributeName {
     get;
   }
    public static NSString VerticalGlyphFormAttributeName {
     get;
   }
    public virtual System.Drawing.SizeF Size {
     get;
   }
</pre>
<h3>New Type: MonoTouch.Foundation.NSByteCountFormatter</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.Foundation.NSByteCountFormatterCountStyle</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSByteCountFormatterCountStyle {
  File,
  Memory,
  Decimal,
  Binary
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSByteCountFormatterUnits</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSIndexPath</h3>
<p>Added:</p><pre class='prettyprint'>
    public static NSIndexPath FromItemSection (int item, int section);
</pre>
<h3>New Type: MonoTouch.Foundation.NSStringDrawingContext</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.Foundation.NSUnderlineStyle</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSUnderlineStyle {
  None,
  Single
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUuid</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSValue</h3>
<p>Added:</p><pre class='prettyprint'>
    public static NSValue FromMKCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D coordinate);
    public static NSValue FromMKCoordinateSpan (MonoTouch.MapKit.MKCoordinateSpan coordinateSpan);
    public virtual MonoTouch.MapKit.MKCoordinateSpan CoordinateSpanValue {
     get;
   }
    public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D CoordinateValue {
     get;
   }
</pre>
<h3>New Type: MonoTouch.Foundation.NSWritingDirection</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSWritingDirection {
  Natural,
  LeftToRight,
  RightToLeft
}
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievement</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static void ResetAchivements (GKNotificationHandler errorHandler);
    public virtual void ReportAchievement (GKNotificationHandler handler);
    public virtual bool Hidden {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
    public static void ResetAchivements (GKNotificationHandler completionHandler);
    public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
    public virtual void ReportAchievement (GKNotificationHandler completionHandler);
    public virtual void SelectChallengeablePlayerIDs (string [] playerIDs, System.Action&lt;string [],MonoTouch.Foundation.NSError&gt; completionHandler);
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool Hidden {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementDescription</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual string GroupIdentifier {
     get;
   }
    public virtual bool Replayable {
     get;
   }
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallenge</h3>
<pre class='prettyprint'>
public class GKChallenge : MonoTouch.Foundation.NSObject {
  
   public GKChallenge ();
   public GKChallenge (MonoTouch.Foundation.NSCoder coder);
   public GKChallenge (MonoTouch.Foundation.NSObjectFlag t);
   public GKChallenge (IntPtr handle);
  
   public static void LoadReceivedChallenges (System.Action<gkchallenge[],monotouch.foundation.nserror> completionHandler);
   public virtual void Decline ();
  protected override void Dispose (bool disposing);
   public virtual string ResolveBundleID ();
  
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
</gkchallenge[],monotouch.foundation.nserror></pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeEventHandler</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeEventHandlerDelegate</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengePredicate</h3>
<pre class='prettyprint'>
[Serializable]
public delegate bool GKChallengePredicate (GKChallenge challenge);
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeState</h3>
<pre class='prettyprint'>
[Serializable]
public enum GKChallengeState {
  Invalid,
  Pending,
  Completed,
  Declined
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKError</h3>
<p>Removed:</p><pre class='prettyprint'>
   UnexpectedConnection
</pre>
<p>Added:</p><pre class='prettyprint'>
   None,
   UnexpectedConnection,
   ChallengeInvalid,
   TurnBasedMatchDataTooLarge,
   TurnBasedTooManySessions,
   TurnBasedInvalidParticipant,
   TurnBasedInvalidTurn,
   TurnBasedInvalidState
</pre>
<h3>New Type: MonoTouch.GameKit.GKGameCenterControllerDelegate</h3>
<pre class='prettyprint'>
public class GKGameCenterControllerDelegate : MonoTouch.Foundation.NSObject {
  
   public GKGameCenterControllerDelegate ();
   public GKGameCenterControllerDelegate (MonoTouch.Foundation.NSCoder coder);
   public GKGameCenterControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public GKGameCenterControllerDelegate (IntPtr handle);
  
   public virtual void Finished (GKGameCenterViewController gameCenterViewController);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKGameCenterViewController</h3>
<pre class='prettyprint'>
public class GKGameCenterViewController : MonoTouch.UIKit.UINavigationController {
  
   public GKGameCenterViewController ();
   public GKGameCenterViewController (MonoTouch.Foundation.NSCoder coder);
   public GKGameCenterViewController (MonoTouch.Foundation.NSObjectFlag t);
   public GKGameCenterViewController (IntPtr handle);
  
  protected override void Dispose (bool disposing);
  
   public static GKGameCenterViewController Shared {
    get;
  }
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
</pre>
<h3>New Type: MonoTouch.GameKit.GKGameCenterViewControllerState</h3>
<pre class='prettyprint'>
[Serializable]
public enum GKGameCenterViewControllerState {
  Default,
  Leaderboards,
  Achievements,
  Challenges
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKInvite</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual uint PlayerAttributes {
     get;
   }
    public virtual int PlayerGroup {
     get;
   }
</pre>
<h3>New Type: MonoTouch.GameKit.GKInviteeResponse</h3>
<pre class='prettyprint'>
[Serializable]
public enum GKInviteeResponse {
  Accepted,
  Declined,
  Failed,
  Incompatible,
  UnableToConnect,
  NoAnswer
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboard</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static void LoadCategories (GKCategoryHandler categoryHandler);
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Deprecated iOS 6.0")]
   public static void LoadCategories (GKCategoryHandler categoryHandler);
    public static void LoadLeaderboards (System.Action&lt;GKLeaderboard[],MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual string GroupIdentifier {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLocalPlayer</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void Authenticate (GKNotificationHandler handler);
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Replaced by AuthenticateHandler in iOS 6.0")]
   public virtual void Authenticate (GKNotificationHandler handler);
    public virtual void LoadDefaultLeaderboardCategoryID (System.Action&lt;string,MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual System.Action&lt;MonoTouch.UIKit.UIViewController,MonoTouch.Foundation.NSError&gt; AuthenticateHandler {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatch</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void ChooseBestHostPlayer (Action&lt;string&gt; completionHandler);
    public virtual void Rematch (System.Action&lt;GKMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchRequest</h3>
<p>Added:</p><pre class='prettyprint'>
    public static int GetMaxPlayersAllowed (GKMatchType matchType);
   
    public virtual int DefaultNumberOfPlayers {
     get;
     set;
   }
    public virtual Action&lt;string,GKInviteeResponse&gt; InviteeResponseHandler {
     get;
     set;
   }
    public virtual string InviteMessage {
     get;
     set;
   }
</pre>
<h3>New Type: MonoTouch.GameKit.GKMatchType</h3>
<pre class='prettyprint'>
[Serializable]
public enum GKMatchType {
  PeerToPeer,
  Hosted,
  TurnBased
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmaker</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void QueryPlayerGroupActivity (uint playerGroup, GKQueryHandler completionHandler);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void CancelInvite (string playerID);
    public virtual void FinishMatchmaking (GKMatch match);
    public virtual void Match (GKInvite invite, System.Action&lt;GKMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual void QueryPlayerGroupActivity (int playerGroup, GKQueryHandler completionHandler);
    public virtual void StartBrowsingForNearbyPlayers (Action&lt;string,bool&gt; reachableHandler);
    public virtual void StopBrowsingForNearbyPlayers ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmakerViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
    public GKMatchmakerViewController ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKNotificationBanner</h3>
<p>Added:</p><pre class='prettyprint'>
    public static void Show (string title, string message, double durationSeconds, Action completionHandler);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKPlayer</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual string DisplayName {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSDate date {
     set;
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static void ReportScores (GKScore[] scores, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
    public virtual bool CanBeShared {
     get;
   }
   [Obsolete("Use Date property")]
   public virtual MonoTouch.Foundation.NSDate date {
</pre>
<h3>New Type: MonoTouch.GameKit.GKScoreChallenge</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedEventHandlerDelegate</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void HandleTurnEventForMatch (GKTurnBasedMatch match);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void HandleTurnEvent (GKTurnBasedMatch match, bool activated);
   [Obsolete("Replaced by HandleTurnEvent in iOS 6.0")]
   public virtual void HandleTurnEventForMatch (GKTurnBasedMatch match);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatch</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipatn, MonoTouch.Foundation.NSData matchData, GKNotificationHandler noCompletion);
    public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void EndTurn (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
   [Obsolete("Replaced by EndTurn in iOS 6.0")]
   public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler noCompletion);
   [Obsolete("Replaced by ParticipantQuitInTurn (GKTurnBasedMatchOutcome, GKTurnBasedParticipant[], double, NSData, Action&lt;NSError&gt;) in iOS 6.0")]
   public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData, GKNotificationHandler onCompletion);
    public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual void Rematch (System.Action&lt;GKTurnBasedMatch,MonoTouch.Foundation.NSError&gt; completionHandler);
    public virtual void SaveCurrentTurn (MonoTouch.Foundation.NSData matchData, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
    public static double DefaultTimeout {
     get;
   }
    public static double NoTimeout {
     get;
   }
    public virtual int MatchDataMaximumSize {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
    public GKTurnBasedMatchmakerViewController ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedParticipant</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSDate TimeoutDate {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKVoiceChatPlayerState</h3>
<p>Removed:</p><pre class='prettyprint'>
   Silent
</pre>
<p>Added:</p><pre class='prettyprint'>
   Silent,
   Connecting
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>New Type: MonoTouch.MapKit.MKDirectionsMode</h3>
<pre class='prettyprint'>
[Serializable]
public enum MKDirectionsMode {
  Driving,
  Walking
}
</pre>
<h3>New Type: MonoTouch.MapKit.MKDirectionsRequest</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.MapKit.MKLaunchOptions</h3>
<pre class='prettyprint'>
public class MKLaunchOptions {
  
   public MKLaunchOptions ();
  
   public Nullable<mkdirectionsmode> Directions;
   public Nullable<mkmaptype> MapType;
   public System.Nullable<monotouch.corelocation.cllocationcoordinate2d> MapCenter;
   public Nullable<mkcoordinatespan> MapSpan;
   public Nullable<bool> ShowsTraffic;
}
</bool></mkcoordinatespan></monotouch.corelocation.cllocationcoordinate2d></mkmaptype></mkdirectionsmode></pre>
<h3>New Type: MonoTouch.MapKit.MKMapItem</h3>
<pre class='prettyprint'>
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
</pre>
<h2>Namespace: MonoTouch.MediaPlayer</h2>
<h3>New Type: MonoTouch.MediaPlayer.MPMediaChapter</h3>
<pre class='prettyprint'>
public class MPMediaChapter : MonoTouch.Foundation.NSObject {
  
   public MPMediaChapter ();
   public MPMediaChapter (MonoTouch.Foundation.NSCoder coder);
   public MPMediaChapter (MonoTouch.Foundation.NSObjectFlag t);
   public MPMediaChapter (IntPtr handle);
  
  protected override void Dispose (bool disposing);
  
   public virtual MPMediaChapterType ChapterType {
    get;
  }
   public override IntPtr ClassHandle {
    get;
  }
   public virtual double PlaybackDuration {
    get;
  }
   public virtual double PlaybackTime {
    get;
  }
   public virtual MonoTouch.Foundation.NSObject Value {
    get;
  }
}
</pre>
<h3>New Type: MonoTouch.MediaPlayer.MPMediaChapterType</h3>
<pre class='prettyprint'>
[Serializable]
public enum MPMediaChapterType {
  PlaybackTime,
  Title,
  Artwork,
  Url,
  UrlDescription
}
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaItem</h3>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString BookmarkTimeProperty {
     get;
   }
    public static MonoTouch.Foundation.NSString ChaptersProperty {
     get;
   }
    public static MonoTouch.Foundation.NSString IsCloudItemProperty {
     get;
   }
    public double BookmarkTime {
     get;
   }
    public MPMediaChapter[] Chapters {
     get;
   }
    public bool IsCloudItem {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool ShowsCloudItems {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual MonoTouch.UIKit.UIColor BackgroundColor {
    public virtual bool UseApplicationAudioSession {
      public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static MonoTouch.Foundation.NSString MoviePlayerReadyForDisplayDidChangeNotification {
     get;
   }
   [Obsolete("Removed in iOS 3.2")]
   public virtual MonoTouch.UIKit.UIColor BackgroundColor {
    public virtual bool ReadyForDisplay {
     get;
   }
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool UseApplicationAudioSession {
      public static MonoTouch.Foundation.NSObject ObserveMoviePlayerReadyForDisplayDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
      public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void PrepareToPlay ();
    public virtual float CurrentPlaybackRate {
     get;
     set;
   }
    public virtual bool IsPreparedToPlay {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPVolumeView</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h2>Namespace: MonoTouch.MediaToolbox</h2>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTap</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapCallbacks</h3>
<pre class='prettyprint'>
public class MTAudioProcessingTapCallbacks {
  
   public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessCallback process);
  
   public void SetInitialize (MTAudioProcessingTapInitCallback callback, void * clientInfo);
  
   public Action<mtaudioprocessingtap> Finalize {
    get;
    set;
  }
   public MTAudioProcessingTapInitCallback Initialize {
    get;
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
</mtaudioprocessingtap></mtaudioprocessingtap></pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapCreationFlags</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum MTAudioProcessingTapCreationFlags : uint {
  PreEffects,
  PostEffects
}
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapError</h3>
<pre class='prettyprint'>
[Serializable]
public enum MTAudioProcessingTapError {
  None,
  InvalidArgument
}
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapFlags</h3>
<pre class='prettyprint'>
[Serializable]
[Flags]
public enum MTAudioProcessingTapFlags : uint {
  StartOfStream,
  EndOfStream
}
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapInitCallback</h3>
<pre class='prettyprint'>
[Serializable]
public delegate void MTAudioProcessingTapInitCallback (MTAudioProcessingTap tap, void * clientInfo, out void * tapStorage);
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapPrepareCallback</h3>
<pre class='prettyprint'>
[Serializable]
public delegate void MTAudioProcessingTapPrepareCallback (MTAudioProcessingTap tap, long maxFrames, ref MonoTouch.AudioToolbox.AudioStreamBasicDescription processingFormat);
</pre>
<h3>New Type: MonoTouch.MediaToolbox.MTAudioProcessingTapProcessCallback</h3>
<pre class='prettyprint'>
[Serializable]
public delegate void MTAudioProcessingTapProcessCallback (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, ref MonoTouch.AudioToolbox.AudioBufferList bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Dlfcn</h3>
<p>Added:</p><pre class='prettyprint'>
    public static System.Drawing.SizeF GetSizeF (IntPtr handle, string symbol);
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static void void_objc_msgSend_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
    public static void void_objc_msgSendSuper_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static bool bool_objc_msgSend_float_IntPtr (IntPtr receiver, IntPtr selector, float arg1, IntPtr arg2);
    public static bool bool_objc_msgSend_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1);
    public static bool bool_objc_msgSendSuper_float_IntPtr (IntPtr receiver, IntPtr selector, float arg1, IntPtr arg2);
    public static bool bool_objc_msgSendSuper_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1);
    public static void CMTime_objc_msgSend_stret_Double (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, double arg1);
    public static void CMTime_objc_msgSend_stret_Int64 (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, long arg1);
    public static void CMTime_objc_msgSendSuper_stret_Double (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, double arg1);
    public static void CMTime_objc_msgSendSuper_stret_Int64 (out MonoTouch.CoreMedia.CMTime retval, IntPtr receiver, IntPtr selector, long arg1);
    public static float float_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static float float_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2);
    public static IntPtr IntPtr_objc_msgSend_int_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, int arg3, IntPtr arg4);
    public static IntPtr IntPtr_objc_msgSend_Int64_int (IntPtr receiver, IntPtr selector, long arg1, int arg2);
    public static IntPtr IntPtr_objc_msgSend_IntPtr_int_int_IntPtr_int_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4, int arg5, float arg6, float arg7);
    public static IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, int arg4);
    public static IntPtr IntPtr_objc_msgSend_IntPtr_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
    public static IntPtr IntPtr_objc_msgSend_IntPtr_UIEdgeInsets_int_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIEdgeInsets arg2, int arg3, double arg4);
    public static IntPtr IntPtr_objc_msgSend_MKCoordinateSpan (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateSpan arg1);
    public static IntPtr IntPtr_objc_msgSend_UIEdgeInsets_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIEdgeInsets arg1, int arg2);
    public static IntPtr IntPtr_objc_msgSend_UInt32_int_int (IntPtr receiver, IntPtr selector, uint arg1, int arg2, int arg3);
    public static IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2);
    public static IntPtr IntPtr_objc_msgSendSuper_int_int_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, int arg3, IntPtr arg4);
    public static IntPtr IntPtr_objc_msgSendSuper_Int64_int (IntPtr receiver, IntPtr selector, long arg1, int arg2);
    public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_IntPtr_int_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, int arg3, IntPtr arg4, int arg5, float arg6, float arg7);
    public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3, int arg4);
    public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
    public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UIEdgeInsets_int_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.UIKit.UIEdgeInsets arg2, int arg3, double arg4);
    public static IntPtr IntPtr_objc_msgSendSuper_MKCoordinateSpan (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateSpan arg1);
    public static IntPtr IntPtr_objc_msgSendSuper_UIEdgeInsets_int (IntPtr receiver, IntPtr selector, MonoTouch.UIKit.UIEdgeInsets arg1, int arg2);
    public static IntPtr IntPtr_objc_msgSendSuper_UInt32_int_int (IntPtr receiver, IntPtr selector, uint arg1, int arg2, int arg3);
    public static void MKCoordinateSpan_objc_msgSend_stret (out MonoTouch.MapKit.MKCoordinateSpan retval, IntPtr receiver, IntPtr selector);
    public static void MKCoordinateSpan_objc_msgSendSuper_stret (out MonoTouch.MapKit.MKCoordinateSpan retval, IntPtr receiver, IntPtr selector);
    public static System.Drawing.PointF PointF_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
    public static System.Drawing.PointF PointF_objc_msgSend_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
    public static void PointF_objc_msgSend_stret_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
    public static void PointF_objc_msgSend_stret_PointF_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
    public static System.Drawing.PointF PointF_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
    public static System.Drawing.PointF PointF_objc_msgSendSuper_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
    public static void PointF_objc_msgSendSuper_stret_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
    public static void PointF_objc_msgSendSuper_stret_PointF_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
    public static void RectangleF_objc_msgSend_stret_SizeF_UInt32_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3);
    public static void RectangleF_objc_msgSendSuper_stret_SizeF_UInt32_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3);
    public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
    public static void SizeF_objc_msgSend_stret_IntPtr_IntPtr_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static void SizeF_objc_msgSend_stret_IntPtr_IntPtr_IntPtr (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
    public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
    public static void SizeF_objc_msgSendSuper_stret_IntPtr_IntPtr_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static void SizeF_objc_msgSendSuper_stret_IntPtr_IntPtr_IntPtr (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
    public static void UIEdgeInsets_objc_msgSend_stret_IntPtr_IntPtr_int (out MonoTouch.UIKit.UIEdgeInsets retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static void UIEdgeInsets_objc_msgSendSuper_stret_IntPtr_IntPtr_int (out MonoTouch.UIKit.UIEdgeInsets retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
    public static void void_objc_msgSend_float_CMTime_CMTime (IntPtr receiver, IntPtr selector, float arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
    public static void void_objc_msgSend_int_IntPtr_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, double arg3, IntPtr arg4, IntPtr arg5);
    public static void void_objc_msgSend_IntPtr_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4);
    public static void void_objc_msgSend_IntPtr_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, IntPtr arg4);
    public static void void_objc_msgSend_IntPtr_UInt32_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3, int arg4);
    public static void void_objc_msgSend_RectangleF_UInt32_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3);
    public static void void_objc_msgSendSuper_float_CMTime_CMTime (IntPtr receiver, IntPtr selector, float arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
    public static void void_objc_msgSendSuper_int_IntPtr_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, double arg3, IntPtr arg4, IntPtr arg5);
    public static void void_objc_msgSendSuper_IntPtr_Double_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4);
    public static void void_objc_msgSendSuper_IntPtr_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3, IntPtr arg4);
    public static void void_objc_msgSendSuper_IntPtr_UInt32_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3, int arg4);
    public static void void_objc_msgSendSuper_RectangleF_UInt32_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3);
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>New Type: MonoTouch.PassKit.PKAddPassesViewController</h3>
<pre class='prettyprint'>
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
  
   public event EventHandler DidFinish;
}
</pre>
<h3>New Type: MonoTouch.PassKit.PKAddPassesViewControllerDelegate</h3>
<pre class='prettyprint'>
public class PKAddPassesViewControllerDelegate : MonoTouch.Foundation.NSObject {
  
   public PKAddPassesViewControllerDelegate ();
   public PKAddPassesViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
   public PKAddPassesViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public PKAddPassesViewControllerDelegate (IntPtr handle);
  
   public virtual void DidFinish (PKAddPassesViewController controller);
}
</pre>
<h3>New Type: MonoTouch.PassKit.PKPass</h3>
<pre class='prettyprint'>
public class PKPass : MonoTouch.Foundation.NSObject {
  
   public PKPass ();
   public PKPass (MonoTouch.Foundation.NSCoder coder);
   public PKPass (MonoTouch.Foundation.NSObjectFlag t);
   public PKPass (IntPtr handle);
   public PKPass (MonoTouch.Foundation.NSData data, out MonoTouch.Foundation.NSError error);
  
  protected override void Dispose (bool disposing);
   public virtual MonoTouch.Foundation.NSObject LocalizedValueForFieldKey (MonoTouch.Foundation.NSString key);
  
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
</pre>
<h3>New Type: MonoTouch.PassKit.PKPassKitErrorCode</h3>
<pre class='prettyprint'>
[Serializable]
public enum PKPassKitErrorCode {
  Unknown,
  None,
  InvalidData,
  UnsupportedVersion,
  CertificateRevoked
}
</pre>
<h3>New Type: MonoTouch.PassKit.PKPassLibrary</h3>
<pre class='prettyprint'>
public class PKPassLibrary : MonoTouch.Foundation.NSObject {
  
   public PKPassLibrary ();
   public PKPassLibrary (MonoTouch.Foundation.NSCoder coder);
   public PKPassLibrary (MonoTouch.Foundation.NSObjectFlag t);
   public PKPassLibrary (IntPtr handle);
  
   public virtual bool Contains (PKPass pass);
   public virtual PKPass GetPass (string identifier, string serialnumber);
   public virtual PKPass[] GetPasses ();
   public virtual void Remove (PKPass pass);
   public virtual bool Replace (PKPass pass);
  
   public static MonoTouch.Foundation.NSString AddedPassesUserInfoKey {
    get;
  }
   public static MonoTouch.Foundation.NSString DidChangeNotification {
    get;
  }
   public static bool IsAvailable {
    get;
  }
   public static MonoTouch.Foundation.NSString RemovedPassesUserInfoKey {
    get;
  }
   public static MonoTouch.Foundation.NSString ReplacementPassesUserInfoKey {
    get;
  }
   public override IntPtr ClassHandle {
    get;
  }
}
</pre>
<h2>Namespace: MonoTouch.Security</h2>
<h3>Type Changed: MonoTouch.Security.SecPadding</h3>
<p>Removed:</p><pre class='prettyprint'>
   PKCS1SHA1
</pre>
<p>Added:</p><pre class='prettyprint'>
   PKCS1SHA1,
   PKCS1SHA224,
   PKCS1SHA256,
   PKCS1SHA384,
   PKCS1SHA512
</pre>
<h2>Namespace: MonoTouch.Social</h2>
<h3>New Type: MonoTouch.Social.SLComposeViewController</h3>
<pre class='prettyprint'>
public class SLComposeViewController : MonoTouch.UIKit.UIViewController {
  
   public SLComposeViewController ();
   public SLComposeViewController (MonoTouch.Foundation.NSCoder coder);
   public SLComposeViewController (MonoTouch.Foundation.NSObjectFlag t);
   public SLComposeViewController (IntPtr handle);
  
   public static SLComposeViewController FromServiceType (MonoTouch.Foundation.NSString serviceType);
   public virtual bool AddImage (MonoTouch.UIKit.UIImage image);
   public virtual bool AddURL (MonoTouch.Foundation.NSUrl url);
  protected override void Dispose (bool disposing);
   public virtual bool RemoveAllImages ();
   public virtual bool RemoveAllURLs ();
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
</slcomposeviewcontrollerresult></pre>
<h3>New Type: MonoTouch.Social.SLComposeViewControllerResult</h3>
<pre class='prettyprint'>
[Serializable]
public enum SLComposeViewControllerResult {
  Cancelled,
  Done
}
</pre>
<h3>New Type: MonoTouch.Social.SLRequest</h3>
<pre class='prettyprint'>
public class SLRequest : MonoTouch.Foundation.NSObject {
  
   public SLRequest (MonoTouch.Foundation.NSCoder coder);
   public SLRequest (MonoTouch.Foundation.NSObjectFlag t);
   public SLRequest (IntPtr handle);
  
   public static SLRequest Create (MonoTouch.Foundation.NSString slServiceType, SLRequestMethod requestMethod, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary parameters);
   public virtual void AddMultipartData (MonoTouch.Foundation.NSData data, string partName, string partType, string filename);
  protected override void Dispose (bool disposing);
   public virtual void PerformRequest (System.Action<monotouch.foundation.nsdata,monotouch.foundation.nshttpurlresponse,monotouch.foundation.nserror> handler);
   public virtual MonoTouch.Foundation.NSUrlRequest PreparedUrlRequest ();
  
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
   public virtual MonoTouch.Foundation.NSUrl URL {
    get;
  }
}
</monotouch.foundation.nsdata,monotouch.foundation.nshttpurlresponse,monotouch.foundation.nserror></pre>
<h3>New Type: MonoTouch.Social.SLRequestMethod</h3>
<pre class='prettyprint'>
[Serializable]
public enum SLRequestMethod {
  Get,
  Post,
  Delete
}
</pre>
<h3>New Type: MonoTouch.Social.SLServiceType</h3>
<pre class='prettyprint'>
public class SLServiceType {
  
   public SLServiceType ();
  
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
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>New Type: MonoTouch.StoreKit.SKDownload</h3>
<pre class='prettyprint'>
public class SKDownload : MonoTouch.Foundation.NSObject {
  
   public SKDownload ();
   public SKDownload (MonoTouch.Foundation.NSCoder coder);
   public SKDownload (MonoTouch.Foundation.NSObjectFlag t);
   public SKDownload (IntPtr handle);
  
  protected override void Dispose (bool disposing);
  
   public override IntPtr ClassHandle {
    get;
  }
   public virtual string ContentIdentifier {
    get;
  }
   public virtual long ContentLength {
    get;
  }
   public virtual MonoTouch.Foundation.NSUrl ContentURL {
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
</pre>
<h3>New Type: MonoTouch.StoreKit.SKDownloadState</h3>
<pre class='prettyprint'>
[Serializable]
public enum SKDownloadState {
  Waiting,
  Active,
  Paused,
  Finished,
  Failed,
  Cancelled
}
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKError</h3>
<p>Removed:</p><pre class='prettyprint'>
   PaymentNotAllowed
</pre>
<p>Added:</p><pre class='prettyprint'>
   PaymentNotAllowed,
   ProductNotAvailable
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentQueue</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void CancelDownloads (SKDownload[] downloads);
    public virtual void PauseDownloads (SKDownload[] downloads);
    public virtual void ResumeDownloads (SKDownload[] downloads);
    public virtual void StartDownloads (SKDownload[] downloads);
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentTransaction</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual SKDownload[] Downloads {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKPaymentTransactionObserver</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void PaymentQueueUpdatedDownloads (SKPaymentQueue queue, SKDownload[] downloads);
</pre>
<h3>Type Changed: MonoTouch.StoreKit.SKProduct</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool Downloadable {
     get;
   }
    public virtual MonoTouch.Foundation.NSNumber[] DownloadContentLengths {
     get;
   }
    public virtual string DownloadContentVersion {
     get;
   }
</pre>
<h3>New Type: MonoTouch.StoreKit.SKStoreProductViewController</h3>
<pre class='prettyprint'>
public class SKStoreProductViewController : MonoTouch.UIKit.UIViewController {
  
   public SKStoreProductViewController ();
   public SKStoreProductViewController (MonoTouch.Foundation.NSCoder coder);
   public SKStoreProductViewController (MonoTouch.Foundation.NSObjectFlag t);
   public SKStoreProductViewController (IntPtr handle);
  
  protected override void Dispose (bool disposing);
   public void LoadProduct (int iTunesItemIdentifier, System.Action<bool,monotouch.foundation.nserror> callback);
   public virtual void LoadProduct (MonoTouch.Foundation.NSDictionary parameters, System.Action<bool,monotouch.foundation.nserror> callback);
  
   public static MonoTouch.Foundation.NSString ParameterITunesItemIdentifier {
    get;
  }
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
  
   public event EventHandler DidFinish;
}
</bool,monotouch.foundation.nserror></bool,monotouch.foundation.nserror></pre>
<h3>New Type: MonoTouch.StoreKit.SKStoreProductViewControllerDelegate</h3>
<pre class='prettyprint'>
public class SKStoreProductViewControllerDelegate : MonoTouch.Foundation.NSObject {
  
   public SKStoreProductViewControllerDelegate ();
   public SKStoreProductViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
   public SKStoreProductViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public SKStoreProductViewControllerDelegate (IntPtr handle);
  
   public virtual void DidFinish (SKStoreProductViewController viewController);
}
</pre>
<h2>Namespace: MonoTouch.SystemConfiguration</h2>
<h3>Type Changed: MonoTouch.SystemConfiguration.StatusCode</h3>
<p>Removed:</p><pre class='prettyprint'>
   ConnectionNoService
</pre>
<p>Added:</p><pre class='prettyprint'>
   ConnectionNoService,
   ConnectionIgnore
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.NSLayoutAttribute</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutConstraint</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutFormatOptions</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutRelation</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSLayoutRelation {
  LessThanOrEqual,
  Equal,
  GreaterThanOrEqual
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSLineBreakMode</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSLineBreakMode {
  WordWrapping,
  CharWrapping,
  Clipping,
  TruncatingHead,
  TruncatingTail,
  TruncatingMiddle
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSShadow</h3>
<pre class='prettyprint'>
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
   public virtual MonoTouch.Foundation.NSObject ShadowColor {
    get;
    set;
  }
   public virtual System.Drawing.SizeF ShadowOffset {
    get;
    set;
  }
}
</pre>
<h3>New Type: MonoTouch.UIKit.NSTextAlignment</h3>
<pre class='prettyprint'>
[Serializable]
public enum NSTextAlignment {
  Left,
  Center,
  Right,
  Justified,
  Natural
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivity</h3>
<pre class='prettyprint'>
public class UIActivity : MonoTouch.Foundation.NSObject {
  
   public UIActivity ();
   public UIActivity (MonoTouch.Foundation.NSCoder coder);
   public UIActivity (MonoTouch.Foundation.NSObjectFlag t);
   public UIActivity (IntPtr handle);
  
   public virtual void ActivityDidFinish (bool completed);
   public virtual bool CanPerform (MonoTouch.Foundation.NSObject[] activityItems);
  protected override void Dispose (bool disposing);
   public virtual void PerformActivity ();
   public virtual void Prepare (MonoTouch.Foundation.NSObject[] activityItems);
  
   public static MonoTouch.Foundation.NSString TypeAssignToContact {
    get;
  }
   public static MonoTouch.Foundation.NSString TypeCopyToPasteboard {
    get;
  }
   public static MonoTouch.Foundation.NSString TypeMail {
    get;
  }
   public static MonoTouch.Foundation.NSString TypeMessage {
    get;
  }
   public static MonoTouch.Foundation.NSString TypePostToFacebook {
    get;
  }
   public static MonoTouch.Foundation.NSString TypePostToTwitter {
    get;
  }
   public static MonoTouch.Foundation.NSString TypePostToWeibo {
    get;
  }
   public static MonoTouch.Foundation.NSString TypePrint {
    get;
  }
   public static MonoTouch.Foundation.NSString TypeSaveToCameraRoll {
    get;
  }
   public virtual UIImage ActivityImage {
    get;
  }
   public virtual string ActivityTitle {
    get;
  }
   public virtual string ActivityType {
    get;
  }
   public virtual UIViewController ActivityViewController {
    get;
  }
   public override IntPtr ClassHandle {
    get;
  }
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityItemProvider</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityItemSource</h3>
<pre class='prettyprint'>
public abstract class UIActivityItemSource : MonoTouch.Foundation.NSObject {
  
   public UIActivityItemSource ();
   public UIActivityItemSource (MonoTouch.Foundation.NSCoder coder);
   public UIActivityItemSource (MonoTouch.Foundation.NSObjectFlag t);
   public UIActivityItemSource (IntPtr handle);
  
   public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, string activityType);
   public abstract MonoTouch.Foundation.NSObject GetPlaceholderData (UIActivityViewController activityViewController);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIActivityViewController</h3>
<pre class='prettyprint'>
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
</monotouch.foundation.nsstring,bool></pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void CompleteStateRestoration ();
    public virtual void ExtendStateRestoration ();
    public virtual UIInterfaceOrientationMask SupportedInterfaceOrientationsForWindow (UIWindow window);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void DidDecodeRestorableState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
    public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIApplication application, UIWindow forWindow);
    public virtual UIViewController GetViewController (UIApplication application, string [] restorationIdentifierComponents, MonoTouch.Foundation.NSCoder coder);
    public virtual bool ShouldRestoreApplicationState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
    public virtual bool ShouldSaveApplicationState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
    public virtual void WillEncodeRestorableState (UIApplication application, MonoTouch.Foundation.NSCoder coder);
    public virtual bool WillFinishLaunching (UIApplication application, MonoTouch.Foundation.NSDictionary launchOptions);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarButtonItem</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIImage GetBackgroundImage (UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
    public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
      public virtual UIImage GetBackgroundImage (UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
      public virtual void SetBackgroundImage (UIImage backgroundImage, UIControlState state, UIBarButtonItemStyle style, UIBarMetrics barMetrics);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBezierPath</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIBezierPath BezierPathByReversingPath ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIButton</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSAttributedString AttributedTitleForState (UIControlState state);
    public virtual void SetAttributedTitleforState (MonoTouch.Foundation.NSAttributedString title, UIControlState state);
    public virtual MonoTouch.Foundation.NSAttributedString CurrentAttributedTitle {
     get;
   }
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionElementCategory</h3>
<pre class='prettyprint'>
[Serializable]
public enum UICollectionElementCategory {
  Cell,
  SupplementaryView,
  DecorationView
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionReusableView</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionUpdateAction</h3>
<pre class='prettyprint'>
[Serializable]
public enum UICollectionUpdateAction {
  Insert,
  Delete,
  Reload,
  Move,
  None
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionView</h3>
<pre class='prettyprint'>
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
   public virtual MonoTouch.Foundation.NSObject DequeueReusableSupplementaryView (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSString identifier, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DeselectItem (MonoTouch.Foundation.NSIndexPath indexPath, bool animated);
  protected override void Dispose (bool disposing);
   public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForItem (MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryElement (MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual MonoTouch.Foundation.NSIndexPath IndexPathForCell (UICollectionViewCell cell);
   public virtual MonoTouch.Foundation.NSIndexPath IndexPathForItemAtPoint (System.Drawing.PointF point);
   public virtual MonoTouch.Foundation.NSIndexPath[] IndexPathsForSelectedItems ();
   public virtual void InsertItems (MonoTouch.Foundation.NSIndexPath[] indexPaths);
   public virtual void InsertSections (MonoTouch.Foundation.NSIndexSet sections);
   public virtual void MoveItem (MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSIndexPath newIndexPath);
   public virtual void MoveSectiontoSection (int section, int newSection);
   public virtual int NumberOfItemsInSection (int section);
   public virtual int NumberOfSections ();
   public virtual void PerformBatchUpdates (MonoTouch.Foundation.NSAction updates, UICompletionHandler completed);
   public void RegisterClassForCell (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
   public void RegisterClassForSupplementaryView (Type cellType, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSString reuseIdentifier);
   public virtual void RegisterNibForCell (UINib nib, MonoTouch.Foundation.NSString reuseIdentifier);
   public virtual void RegisterNibForSupplementaryView (UINib nib, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSString reuseIdentifier);
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewCell</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewController</h3>
<pre class='prettyprint'>
public class UICollectionViewController : UIViewController {
  
   public UICollectionViewController ();
   public UICollectionViewController (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewController (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewController (IntPtr handle);
   public UICollectionViewController (UICollectionViewLayout layout);
  
   public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
  protected override void Dispose (bool disposing);
   public virtual UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual int ItemsInSection (UICollectionView collectionView, int section);
   public virtual int NumberOfSections (UICollectionView collectionView);
   public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
  
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDataSource</h3>
<pre class='prettyprint'>
public abstract class UICollectionViewDataSource : MonoTouch.Foundation.NSObject {
  
   public UICollectionViewDataSource ();
   public UICollectionViewDataSource (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewDataSource (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewDataSource (IntPtr handle);
  
   public abstract UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public abstract int ItemsInSection (UICollectionView collectionView, int section);
   public virtual int NumberOfSections (UICollectionView collectionView);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDelegate</h3>
<pre class='prettyprint'>
public class UICollectionViewDelegate : MonoTouch.Foundation.NSObject {
  
   public UICollectionViewDelegate ();
   public UICollectionViewDelegate (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewDelegate (IntPtr handle);
  
   public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<pre class='prettyprint'>
public class UICollectionViewDelegateFlowLayout : UICollectionViewDelegate {
  
   public UICollectionViewDelegateFlowLayout ();
   public UICollectionViewDelegateFlowLayout (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewDelegateFlowLayout (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewDelegateFlowLayout (IntPtr handle);
  
   public override bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public override void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UIEdgeInsets GetInsetForItem (UICollectionView collectionView, UICollectionViewLayout layout, int section);
   public virtual float GetMinimumInteritemSpacingForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
   public virtual float GetMinimumLineSpacingForSection (UICollectionView collectionView, UICollectionViewLayout layout, int section);
   public virtual System.Drawing.SizeF GetReferenceSizeForFooter (UICollectionView collectionView, UICollectionViewLayout layout, int section);
   public virtual System.Drawing.SizeF GetReferenceSizeForHeader (UICollectionView collectionView, UICollectionViewLayout layout, int section);
   public virtual System.Drawing.SizeF GetSizeForItem (UICollectionView collectionView, UICollectionViewLayout layout, MonoTouch.Foundation.NSIndexPath indexPath);
   public override void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public override bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public override bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewFlowLayout</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewLayout</h3>
<pre class='prettyprint'>
public class UICollectionViewLayout : MonoTouch.Foundation.NSObject {
  
   public UICollectionViewLayout ();
   public UICollectionViewLayout (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewLayout (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewLayout (IntPtr handle);
  
  protected override void Dispose (bool disposing);
   public virtual void FinalizeAnimatedBoundsChange ();
   public virtual void FinalizeCollectionViewUpdates ();
   public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingDecorationElement (string elementKind, MonoTouch.Foundation.NSIndexPath decorationIndexPath);
   public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
   public virtual UICollectionViewLayoutAttributes FinalLayoutAttributesForDisappearingSupplementaryElement (string elementKind, MonoTouch.Foundation.NSIndexPath elementIndexPath);
   public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingDecorationElement (string elementKind, MonoTouch.Foundation.NSIndexPath decorationIndexPath);
   public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingItem (MonoTouch.Foundation.NSIndexPath itemIndexPath);
   public virtual UICollectionViewLayoutAttributes InitialLayoutAttributesForAppearingSupplementaryElement (string elementKind, MonoTouch.Foundation.NSIndexPath elementIndexPath);
   public virtual void InvalidateLayout ();
   public virtual UICollectionViewLayoutAttributes LayoutAttributesForDecorationView (string decorationViewKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionViewLayoutAttributes[] LayoutAttributesForElementsInRect (System.Drawing.RectangleF rect);
   public virtual UICollectionViewLayoutAttributes LayoutAttributesForItem (MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionViewLayoutAttributes LayoutAttributesForSupplementaryView (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void PrepareForAnimatedBoundsChange (System.Drawing.RectangleF oldBounds);
   public virtual void PrepareForCollectionViewUpdates (UICollectionViewUpdateItem[] updateItems);
   public virtual void PrepareLayout ();
   public void RegisterClassForDecorationView (Type viewType, MonoTouch.Foundation.NSString reuseIdentifier);
   public virtual void RegisterNibForDecorationView (UINib nib, MonoTouch.Foundation.NSString decorationViewKind);
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<pre class='prettyprint'>
public class UICollectionViewLayoutAttributes : MonoTouch.Foundation.NSObject {
  
   public UICollectionViewLayoutAttributes ();
   public UICollectionViewLayoutAttributes (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewLayoutAttributes (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewLayoutAttributes (IntPtr handle);
  
   public static UICollectionViewLayoutAttributes CreateForSupplementaryView (string elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public static UICollectionViewLayoutAttributes FromIndexPath (MonoTouch.Foundation.NSIndexPath indexPath);
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewScrollDirection</h3>
<pre class='prettyprint'>
[Serializable]
public enum UICollectionViewScrollDirection {
  Vertical,
  Horizontal
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewScrollPosition</h3>
<pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewSource</h3>
<pre class='prettyprint'>
public class UICollectionViewSource : MonoTouch.Foundation.NSObject {
  
   public UICollectionViewSource ();
   public UICollectionViewSource (MonoTouch.Foundation.NSCoder coder);
   public UICollectionViewSource (MonoTouch.Foundation.NSObjectFlag t);
   public UICollectionViewSource (IntPtr handle);
  
   public virtual bool CanPerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual void DidDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingCell (UICollectionView collectionView, UICollectionViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidEndDisplayingSupplementaryView (UICollectionView collectionView, UICollectionReusableView view, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual void DidUnhighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionViewCell GetCell (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual UICollectionReusableView GetViewForSupplementaryElement (UICollectionView collectionView, MonoTouch.Foundation.NSString elementKind, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual int ItemsInSection (UICollectionView collectionView, int section);
   public virtual int NumberOfSections (UICollectionView collectionView);
   public virtual void PerformAction (UICollectionView collectionView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
   public virtual bool ShouldDeselectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldHighlightItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldSelectItem (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
   public virtual bool ShouldShowMenu (UICollectionView collectionView, MonoTouch.Foundation.NSIndexPath indexPath);
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewUpdateItem</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDevice</h3>
<p>Added:</p><pre class='prettyprint'>
   protected override void Dispose (bool disposing);
    public virtual MonoTouch.Foundation.NSUuid IdentifierForAdvertising {
     get;
   }
    public virtual MonoTouch.Foundation.NSUuid IdentifierForVendor {
     get;
   }
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocumentInteractionControllerDelegate</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual bool CanPerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
    public virtual bool PerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
</pre>
<p>Added:</p><pre class='prettyprint'>
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool CanPerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
   [Obsolete("Deprecated in iOS 6.0")]
   public virtual bool PerformAction (UIDocumentInteractionController controller, MonoTouch.ObjCRuntime.Selector action);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UIImageResizingMode</h3>
<pre class='prettyprint'>
[Serializable]
public enum UIImageResizingMode {
  Tile,
  Stretch
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIInterfaceOrientationMask</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UILabel</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual float MinimumFontSize {
</pre>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>New Type: MonoTouch.UIKit.UILayoutConstraintAxis</h3>
<pre class='prettyprint'>
[Serializable]
public enum UILayoutConstraintAxis {
  Horizontal,
  Vertical
}
</pre>
<h3>New Type: MonoTouch.UIKit.UILayoutPriority</h3>
<pre class='prettyprint'>
[Serializable]
public enum UILayoutPriority {
  Required,
  DefaultHigh,
  DefaultLow,
  FittingSizeLevel
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBar</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIImage ShadowImage {
     get;
     set;
   }
      public virtual UIImage ShadowImage {
       get;
       set;
     }
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationController</h3>
<p>Added:</p><pre class='prettyprint'>
    public UINavigationController (Type navigationBarType, Type toolbarType);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageControl</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Added:</p><pre class='prettyprint'>
    public UIPageViewController (UIPageViewControllerTransitionStyle style, UIPageViewControllerNavigationOrientation navigationOrientation, UIPageViewControllerSpineLocation spineLocation, float interPageSpacing);
    public UIPageViewGetNumber GetPresentationCount {
     get;
     set;
   }
    public UIPageViewGetNumber GetPresentationIndex {
     get;
     set;
   }
    public event EventHandler&lt;UIPageViewControllerTransitionEventArgs&gt; WillTransition;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDataSource</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual int GetPresentationCount (UIPageViewController pageViewController);
    public virtual int GetPresentationIndex (UIPageViewController pageViewController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void WillTransition (UIPageViewController pageViewController, UIViewController[] pendingViewControllers);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPageViewControllerTransitionEventArgs</h3>
<pre class='prettyprint'>
public class UIPageViewControllerTransitionEventArgs : EventArgs {
  
   public UIPageViewControllerTransitionEventArgs (UIViewController[] pendingViewControllers);
  
   public UIViewController[] PendingViewControllers {
    get;
    set;
  }
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerTransitionStyle</h3>
<p>Removed:</p><pre class='prettyprint'>
   PageCurl
</pre>
<p>Added:</p><pre class='prettyprint'>
   PageCurl,
   Scroll
</pre>
<h3>New Type: MonoTouch.UIKit.UIPageViewGetNumber</h3>
<pre class='prettyprint'>
[Serializable]
public delegate int UIPageViewGetNumber (UIPageViewController pageViewController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPickerViewDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSAttributedString GetAttribytedTitle (UIPickerView pickerView, int row, int component);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView</h3>
<p>Added:</p><pre class='prettyprint'>
    public static bool WantsDefaultContentAppearance {
     get;
   }
</pre>
<h3>New Type: MonoTouch.UIKit.UIRefreshControl</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIResponder</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void ToggleBoldface (MonoTouch.Foundation.NSObject sender);
    public virtual void ToggleItalics (MonoTouch.Foundation.NSObject sender);
    public virtual void ToggleUnderline (MonoTouch.Foundation.NSObject sender);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStepper</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStoryboardSegue</h3>
<p>Added:</p><pre class='prettyprint'>
    public static UIStoryboardSegue Create (string identifier, UIViewController source, UIViewController destination, MonoTouch.Foundation.NSAction performHandler);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISwitch</h3>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBar</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIImage ShadowImage {
     get;
     set;
   }
      public virtual UIImage ShadowImage {
       get;
       set;
     }
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableView</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual MonoTouch.Foundation.NSObject DequeueReusableCell (MonoTouch.Foundation.NSString reuseIdentifier, MonoTouch.Foundation.NSIndexPath indexPath);
    public virtual MonoTouch.Foundation.NSObject DequeueReusableHeaderFooterView (MonoTouch.Foundation.NSString reuseIdentifier);
    public virtual UITableViewHeaderFooterView FooterViewForSection (int section);
    public virtual UITableViewHeaderFooterView HeaderViewForSection (int section);
    public void RegisterClassForCellReuse (Type cellType, MonoTouch.Foundation.NSString reuseIdentifier);
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewController</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIRefreshControl RefreshControl {
     get;
     set;
   }
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual void DidEndDisplayingCell (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
    public virtual void DidEndDisplayingFooterView (UITableView tableView, UIView footerView, int section);
    public virtual void DidEndDisplayingHeaderView (UITableView tableView, UIView headerView, int section);
    public virtual void DidHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
    public virtual void DidUnhighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
    public virtual bool ShouldHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
    public virtual void WillDisplayFooterView (UITableView tableView, UIView footerView, int section);
    public virtual void WillDisplayHeaderView (UITableView tableView, UIView headerView, int section);
</pre>
<h3>New Type: MonoTouch.UIKit.UITableViewHeaderFooterView</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextAlignment</h3>
<p>Removed:</p><pre class='prettyprint'>
   Right
</pre>
<p>Added:</p><pre class='prettyprint'>
   Right,
   Justified,
   Natural
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextField</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual System.Drawing.RectangleF GetFrameForDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder);
    public virtual MonoTouch.Foundation.NSObject InsertDictationResultPlaceholder ();
    public virtual void RemoveDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder, bool willInsertResult);
    public virtual UITextSelectionRect[] SelectionRectsForRange (UITextRange range);
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
</pre>
<h3>New Type: MonoTouch.UIKit.UITextSelectionRect</h3>
<pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextView</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual System.Drawing.RectangleF GetFrameForDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder);
    public virtual MonoTouch.Foundation.NSObject InsertDictationResultPlaceholder ();
    public virtual void RemoveDictationResultPlaceholder (MonoTouch.Foundation.NSObject placeholder, bool willInsertResult);
    public virtual UITextSelectionRect[] SelectionRectsForRange (UITextRange range);
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbar</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual UIImage GetShadowImage (UIToolbarPosition topOrBottom);
    public virtual void SetShadowImage (UIImage shadowImage, UIToolbarPosition topOrBottom);
      public virtual UIImage GetShadowImage (UIToolbarPosition topOrBottom);
      public virtual void SetShadowImage (UIImage shadowImage, UIToolbarPosition topOrBottom);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual System.Drawing.RectangleF ContentStretch {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public static bool RequiresConstraintBasedLayout ();
    public virtual void AddConstraint (NSLayoutConstraint constraint);
    public virtual void AddConstraints (NSLayoutConstraint[] constraints);
    public virtual System.Drawing.RectangleF AlignmentRectForFrame (System.Drawing.RectangleF frame);
    public virtual NSLayoutConstraint[] ConstraintsAffectingLayout (UILayoutConstraintAxis axis);
    public virtual UILayoutPriority ContentCompressionResistancePriority (UILayoutConstraintAxis axis);
    public virtual UILayoutPriority ContentHuggingPriority (UILayoutConstraintAxis axis);
    public virtual void DecodeRestorableState (MonoTouch.Foundation.NSCoder coder);
    public virtual void EncodeRestorableState (MonoTouch.Foundation.NSCoder coder);
    public virtual void ExerciseAmbiguityInLayout ();
    public virtual System.Drawing.RectangleF FrameForAlignmentRect (System.Drawing.RectangleF alignmentRect);
    public virtual bool GestureRecognizerShouldBegin (UIGestureRecognizer gestureRecognizer);
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre class='prettyprint'>
    public virtual void DismissModalViewControllerAnimated (bool animated);
    public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
    public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
    public virtual void ViewDidUnload ();
    public virtual void ViewWillUnload ();
    public virtual bool AutomaticallyForwardAppearanceAndRotationMethodsToChildViewControllers {
    public virtual UIViewController ModalViewController {
</pre>
<p>Added:</p><pre class='prettyprint'>
    public virtual void BeginAppearanceTransition (bool isAppearing, bool animated);
    public virtual bool CanPerformUnwind (MonoTouch.ObjCRuntime.Selector segueAction, UIViewController fromViewController, MonoTouch.Foundation.NSObject sender);
    public virtual void DecodeRestorableState (MonoTouch.Foundation.NSCoder coder);
   [Obsolete("Deprecated in iOS 6.0, use DismissViewController (bool, NSAction) instead.")]
   public virtual void DismissModalViewControllerAnimated (bool animated);
    public virtual void EncodeRestorableState (MonoTouch.Foundation.NSCoder coder);
    public virtual void EndAppearanceTransition ();
    public virtual UIStoryboardSegue GetSegueForUnwinding (UIViewController toViewController, UIViewController fromViewController, string identifier);
    public virtual UIViewController GetViewControllerForUnwind (MonoTouch.ObjCRuntime.Selector segueAction, UIViewController fromViewController, MonoTouch.Foundation.NSObject sender);
    public virtual UIInterfaceOrientation PreferredInterfaceOrientationForPresentation ();
   [Obsolete("Deprecated in iOS 6.0, use PresentViewController (UIViewController, bool, NSAction) instead.")]
   public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
    public virtual bool ShouldAutorotate ();
   [Obsolete("Derecated in IOS6")]
   public virtual bool ShouldAutorotateToInterfaceOrientation (UIInterfaceOrientation toInterfaceOrientation);
    public virtual bool ShouldPerformSegue (string segueIdentifier, MonoTouch.Foundation.NSObject sender);
    public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations ();
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
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIWebView</h3>
<p>Added:</p><pre class='prettyprint'>
    public virtual bool KeyboardDisplayRequiresUserAction {
     get;
     set;
   }
    public virtual bool SuppressesIncrementalRendering {
     get;
     set;
   }
</pre>
<h2>Namespace: MonoTouch.iAd</h2>
<h3>New Type: MonoTouch.iAd.ADAdType</h3>
<pre class='prettyprint'>
[Serializable]
public enum ADAdType {
  Banner,
  MediumRectangle
}
</pre>
<h3>Type Changed: MonoTouch.iAd.ADBannerView</h3>
<p>Removed:</p><pre class='prettyprint'>
    public static System.Drawing.SizeF SizeFromContentSizeIdentifier (string sizeIdentifier);
    public virtual string CurrentContentSizeIdentifier {
    public virtual MonoTouch.Foundation.NSSet RequiredContentSizeIdentifiers {
</pre>
<p>Added:</p><pre class='prettyprint'>
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
</pre>
<h3>Type Changed: MonoTouch.iAd.ADError</h3>
<p>Removed:</p><pre class='prettyprint'>
   ApplicationInactive
</pre>
<p>Added:</p><pre class='prettyprint'>
   ApplicationInactive,
   AdUnloaded
</pre>
</body>
</html>
