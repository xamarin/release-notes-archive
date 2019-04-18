---
id: 07B06470-FF07-4879-A34F-369231BF8569
title: "From 6.9.6 to 6.9.7"
---

<html><head><title>Comparison between monotouch-6.9.6.dll and monotouch.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.9.6";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.7";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetTrack</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSString GetAssociatedTracksOfType (MonoTouch.Foundation.NSString avAssetTrackTrackAssociationType);
 	public virtual MonoTouch.CoreMedia.CMTime MinFrameDuration {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetTrackTrackAssociation</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString GetAssociatedTracksOfType (AVAssetTrack This, MonoTouch.Foundation.NSString avAssetTrackTrackAssociationType);
 	
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAudioMixInputParameters</h3>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
 		get;
 		set;
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVAuthorizationStatus</h3>
<pre>
[Serializable]
public enum AVAuthorizationStatus {
	NotDetermined,
	Restricted,
	Denied,
	Authorized
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureDevice</h3>
<p>Added:</p><pre>
 	public static AVAuthorizationStatus GetAuthorizationStatus (MonoTouch.Foundation.NSString avMediaTypeToken);
 	public static void RequestAccessForMediaType (MonoTouch.Foundation.NSString avMediaTypeToken, AVRequestAccessStatus completion);
 	public static System.Threading.Tasks.Task&lt;bool&gt; RequestAccessForMediaTypeAsync (MonoTouch.Foundation.NSString avMediaTypeToken);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureStillImageOutput</h3>
<p>Added:</p><pre>
 	public virtual bool AutomaticallyEnablesStillImageStabilizationWhenAvailable {
 		get;
 		set;
 	}
 	public virtual bool IsStillImageStabilizationActive {
 		get;
 	}
 	public virtual bool IsStillImageStabilizationSupported {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h3>
<p>Added:</p><pre>
 	public virtual System.Drawing.RectangleF MapToLayerCoordinates (System.Drawing.RectangleF rectInMetadataOutputCoordinates);
 	public virtual System.Drawing.RectangleF MapToMetadataOutputCoordinates (System.Drawing.RectangleF rectInLayerCoordinates);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMetadata</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyAlbumAndTrack {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyCollection {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyKeywordList {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyMediaClassification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyMediaRating {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyThumbnail {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString K3GPUserDataKeyUserRating {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString KFormatISOUserData {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString KKeySpaceISOUserData {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
</pre>
<p>Added:</p><pre>
 	protected override void Dispose (bool disposing);
 	public override MonoTouch.MediaToolbox.MTAudioProcessingTap AudioTapProcessor {
 		get;
 		set;
 	}
 	public override MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMutableVideoComposition</h3>
<p>Added:</p><pre>
 	public static AVMutableVideoComposition Create (AVAsset asset);
 	public override MonoTouch.ObjCRuntime.Class CustomVideoCompositorClass {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction</h3>
<p>Added:</p><pre>
 	public virtual void SetCrop (System.Drawing.RectangleF cropRectangle, MonoTouch.CoreMedia.CMTime time);
 	public virtual void SetCrop (System.Drawing.RectangleF startCropRectangle, System.Drawing.RectangleF endCropRectangle, MonoTouch.CoreMedia.CMTimeRange timeRange);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVOutputSettingsAssistant</h3>
<pre>
public class AVOutputSettingsAssistant : MonoTouch.Foundation.NSObject {
	
	public AVOutputSettingsAssistant (MonoTouch.Foundation.NSCoder coder);
	public AVOutputSettingsAssistant (MonoTouch.Foundation.NSObjectFlag t);
	public AVOutputSettingsAssistant (IntPtr handle);
	
	public static AVOutputSettingsAssistant FromPreset (string presetIdentifier);
	protected override void Dispose (bool disposing);
	
	public static string [] AvailableOutputSettingsPresets {
		get;
	}
	public AudioSettings AudioSettings {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public AVVideoSettingsCompressed CompressedVideoSettings {
		get;
	}
	public virtual string OutputFileType {
		get;
	}
	public AVOutputSettingsAssistant Preset1280x720 {
		get;
	}
	public AVOutputSettingsAssistant Preset1920x1080 {
		get;
	}
	public AVOutputSettingsAssistant Preset640x480 {
		get;
	}
	public AVOutputSettingsAssistant Preset960x540 {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMAudioFormatDescription SourceAudioFormat {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTime SourceVideoAverageFrameDuration {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMVideoFormatDescription SourceVideoFormat {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTime SourceVideoMinFrameDuration {
		get;
		set;
	}
	public AVVideoSettingsUncompressed UnCompressedVideoSettings {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary WeakAudioSettings {
		get;
	}
	public virtual MonoTouch.Foundation.NSDictionary WeakVideoSettings {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Added:</p><pre>
 	public AVPlayerItem (AVAsset asset, MonoTouch.Foundation.NSString[] automaticallyLoadedAssetKeys);
 	public static AVPlayerItem FromAsset (AVAsset asset, MonoTouch.Foundation.NSString[] automaticallyLoadedAssetKeys);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoTouch.Foundation.NSDate date, out bool result);
 	public virtual void SelectMediaOptionAutomaticallyInMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
 	public virtual MonoTouch.Foundation.NSString AudioTimePitchAlgorithm {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSString[] AutomaticallyLoadedAssetKeys {
 		get;
 	}
 	public virtual AVVideoCompositing CustomVideoCompositor {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent</h3>
<p>Removed:</p><pre>
 	public virtual int SegmentedDownloadedCount {
</pre>
<p>Added:</p><pre>
 	public virtual int DownloadOverdue {
 		get;
 	}
 	public virtual int MediaRequestsWWAN {
 		get;
 	}
 	public virtual double ObservedBitrateStandardDeviation {
 		get;
 	}
 	public virtual double ObservedMaxBitrate {
 		get;
 	}
 	public virtual double ObservedMinBitrate {
 		get;
 	}
 	public virtual string PlaybackType {
 		get;
 	}
 	[Obsolete("Deprecated in iOS7")]
	public virtual int SegmentedDownloadedCount {
 	public virtual double StartupTime {
 		get;
 	}
 	public virtual double SwitchBitrate {
 		get;
 	}
 	public virtual double TransferDuration {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemLegibleOutput</h3>
<pre>
public class AVPlayerItemLegibleOutput : AVPlayerItemOutput {
	
	public AVPlayerItemLegibleOutput ();
	public AVPlayerItemLegibleOutput (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemLegibleOutput (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemLegibleOutput (IntPtr handle);
	public AVPlayerItemLegibleOutput (MonoTouch.Foundation.NSNumber[] subtypesFourCCcodes);
	
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemLegibleOutputPushDelegate delegateObject, MonoTouch.CoreFoundation.DispatchQueue delegateQueue);
	
	public static MonoTouch.Foundation.NSString TextStylingResolutionDefault {
		get;
	}
	public static MonoTouch.Foundation.NSString TextStylingResolutionSourceAndRulesOnly {
		get;
	}
	public virtual double AdvanceIntervalForDelegateInvocation {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVPlayerItemLegibleOutputPushDelegate Delegate {
		get;
	}
	public virtual MonoTouch.CoreFoundation.DispatchQueue DelegateQueue {
		get;
	}
	public virtual MonoTouch.Foundation.NSString TextStylingResolution {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemLegibleOutputPushDelegate</h3>
<pre>
public class AVPlayerItemLegibleOutputPushDelegate : AVPlayerItemOutputPushDelegate, IAVPlayerItemLegibleOutputPushDelegate {
	
	public AVPlayerItemLegibleOutputPushDelegate ();
	public AVPlayerItemLegibleOutputPushDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemLegibleOutputPushDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemLegibleOutputPushDelegate (IntPtr handle);
	
	public virtual void DidOutputAttributedStrings (AVPlayerItemLegibleOutput output, MonoTouch.Foundation.NSAttributedString[] strings, MonoTouch.CoreMedia.CMSampleBuffer[] nativeSamples, MonoTouch.CoreMedia.CMTime itemTime);
	public override void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemLegibleOutputPushDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemLegibleOutputPushDelegate_Extensions {
	
	public static void DidOutputAttributedStrings (IAVPlayerItemLegibleOutputPushDelegate This, AVPlayerItemLegibleOutput output, MonoTouch.Foundation.NSAttributedString[] strings, MonoTouch.CoreMedia.CMSampleBuffer[] nativeSamples, MonoTouch.CoreMedia.CMTime itemTime);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemOutputPushDelegate</h3>
<pre>
public class AVPlayerItemOutputPushDelegate : MonoTouch.Foundation.NSObject, IAVPlayerItemOutputPushDelegate {
	
	public AVPlayerItemOutputPushDelegate ();
	public AVPlayerItemOutputPushDelegate (MonoTouch.Foundation.NSCoder coder);
	public AVPlayerItemOutputPushDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public AVPlayerItemOutputPushDelegate (IntPtr handle);
	
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVPlayerItemOutputPushDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemOutputPushDelegate_Extensions {
	
	public static void OutputSequenceWasFlushed (IAVPlayerItemOutputPushDelegate This, AVPlayerItemOutput output);
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVRequestAccessStatus</h3>
<pre>
[Serializable]
public delegate void AVRequestAccessStatus (bool accessGranted);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideo</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AllowFrameReorderingKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AverageNonDroppableFrameRateKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ExpectedSourceFrameRateKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString H264EntropyModeCABAC {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString H264EntropyModeCAVLC {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString H264EntropyModeKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MaxKeyFrameIntervalDurationKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCodecSettings</h3>
<p>Added:</p><pre>
 		get;
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCompositing</h3>
<p>Removed:</p><pre>
 public abstract class AVVideoCompositing : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class AVVideoCompositing : MonoTouch.Foundation.NSObject, IAVVideoCompositing {
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoCompositing_Extensions</h3>
<pre>
public static class AVVideoCompositing_Extensions {
	
	public static void CancelAllPendingVideoCompositionRequests (IAVVideoCompositing This);
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoComposition</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.ObjCRuntime.Class CustomVideoCompositorClass {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionCoreAnimationTool</h3>
<p>Added:</p><pre>
 	public static AVVideoCompositionCoreAnimationTool FromComposedVideoFrames (MonoTouch.CoreAnimation.CALayer[] videoLayers, MonoTouch.CoreAnimation.CALayer inAnimationlayer);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction</h3>
<p>Added:</p><pre>
 	public virtual bool GetCrop (MonoTouch.CoreMedia.CMTime time, ref System.Drawing.RectangleF startCropRectangle, ref System.Drawing.RectangleF endCropRectangle, ref MonoTouch.CoreMedia.CMTimeRange timeRange);
</pre>
<h3>New Type: MonoTouch.AVFoundation.AVVideoH264EntropyMode</h3>
<pre>
[Serializable]
public enum AVVideoH264EntropyMode {
	AdaptiveVariableLength,
	AdaptiveBinaryArithmetic
}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoProfileLevelH264</h3>
<p>Removed:</p><pre>
 	High41
</pre>
<p>Added:</p><pre>
 	High41,
 	BaselineAutoLevel,
 	MainAutoLevel,
 	HighAutoLevel
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVVideoSettingsCompressed</h3>
<p>Added:</p><pre>
 	public Nullable&lt;bool&gt; AllowFrameReordering {
 		get;
 		set;
 	}
 	public Nullable&lt;int&gt; AverageNonDroppableFrameRate {
 		get;
 		set;
 	}
 	public Nullable&lt;AVVideoH264EntropyMode&gt; EntropyEncoding {
 		get;
 		set;
 	}
 	public Nullable&lt;int&gt; ExpectedSourceFrameRate {
 		get;
 		set;
 	}
 	public Nullable&lt;double&gt; MaxKeyFrameIntervalDuration {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVPlayerItemLegibleOutputPushDelegate</h3>
<pre>
public interface IAVPlayerItemLegibleOutputPushDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVPlayerItemOutputPushDelegate</h3>
<pre>
public interface IAVPlayerItemOutputPushDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.AVFoundation.IAVVideoCompositing</h3>
<pre>
public interface IAVVideoCompositing : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void RenderContextChanged (AVVideoCompositionRenderContext newRenderContext);
	MonoTouch.Foundation.NSDictionary RequiredPixelBufferAttributesForRenderContext ();
	MonoTouch.Foundation.NSDictionary SourcePixelBufferAttributes ();
	void StartVideoCompositionRequest (AVAsynchronousVideoCompositionRequest asyncVideoCompositionRequest);
}
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate</h3>
<p>Removed:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.IUIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask SupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<h2>Namespace: MonoTouch.AudioUnit</h2>
<h3>Type Changed: MonoTouch.AudioUnit.AudioComponentFlag</h3>
<p>Removed:</p><pre>
 	Unsearchable
</pre>
<p>Added:</p><pre>
 	Unsearchable,
 	SandboxSafe
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioComponentType</h3>
<p>Removed:</p><pre>
 	Generator
</pre>
<p>Added:</p><pre>
 	Generator,
 	MIDIProcessor,
 	RemoteEffect,
 	RemoteGenerator,
 	RemoteInstrument,
 	RemoteMusicEffect
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioTypeConverter</h3>
<p>Removed:</p><pre>
 	AUiPodTime,
 	AUiPodTimeOther
</pre>
<p>Added:</p><pre>
 	AUiPodTimeOther,
 	AUiPodTime
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioUnit</h3>
<p>Added:</p><pre>
 	public AudioUnitStatus SetElementCount (AudioUnitScopeType scope, uint count);
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioUnitParameterType</h3>
<p>Removed:</p><pre>
 	Reverb2DryWetMix,
 	Reverb2Gain,
 	Reverb2MinDelayTime,
 	Reverb2MaxDelayTime,
 	Reverb2DecayTimeAt0Hz,
 	Reverb2DecayTimeAtNyquist,
 	Reverb2RandomizeReflections
</pre>
<p>Added:</p><pre>
 	Mixer3DAzimuth,
 	Mixer3DElevation,
 	Mixer3DDistance,
 	Mixer3DGain,
 	Mixer3DPlaybackRate,
 	Mixer3DEnable,
 	Mixer3DMinGain,
 	Mixer3DMaxGain,
 	Mixer3DReverbBlend,
 	Mixer3DGlobalReverbGain,
 	Mixer3DOcclusionAttenuation,
 	Mixer3DObstructionAttenuation,
 	RandomBoundA,
 	RandomBoundB,
 	RandomCurve
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType</h3>
<p>Added:</p><pre>
 	FrequencyResponse,
 	RemoteControlEventListener,
 	IsInterAppConnected,
 	PeerURL,
 	MIDICallbacks,
 	HostReceivesRemoteControlEvents,
 	RemoteControlToHost,
 	HostTransportState,
 	NodeComponentDescription,
</pre>
<h2>Namespace: MonoTouch.CoreBluetooth</h2>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBCentralManager</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use .ctor(CBCentralManagerDelegate,DispatchQueue) to create a valid CBCentralManager instance")]
	public CBCentralManager ();
</pre>
<p>Added:</p><pre>
 	public CBCentralManager ();
 	public CBCentralManager (MonoTouch.CoreFoundation.DispatchQueue dispatchQueue);
 	public void RetrievePeripherals (CBUUID peripheralUuid);
 	public void RetrievePeripherals (Guid peripheralUuid);
 	public void ScanForPeripherals (CBUUID serviceUuid);
 	public void ScanForPeripherals (CBUUID serviceUuid, MonoTouch.Foundation.NSDictionary options);
 	public void ScanForPeripherals (CBUUID[] peripheralUuids);
 	public void ScanForPeripherals (Guid serviceUuid);
 	public void ScanForPeripherals (Guid serviceUuid, MonoTouch.Foundation.NSDictionary options);
 	public void ScanForPeripherals (Guid [] serviceUuids);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheral</h3>
<p>Added:</p><pre>
 	public void DiscoverCharacteristics (CBService forService);
 	public void DiscoverServices ();
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<p>Added:</p><pre>
 	public virtual void StartAdvertising (MonoTouch.Foundation.NSDictionary options);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBUUID</h3>
<p>Removed:</p><pre>
 public class CBUUID : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class CBUUID : MonoTouch.Foundation.NSObject, IEquatable&lt;CBUUID&gt; {
 	public static CBUUID FromBytes (byte [] bytes);
 	public static CBUUID FromPartial (ushort servicePart);
 	public bool Equals (CBUUID obj);
 	public override bool Equals (object obj);
 	public override int GetHashCode ();
 	public static bool operator == (CBUUID a, CBUUID b);
 	public static bool operator != (CBUUID a, CBUUID b);
 	
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>Type Changed: MonoTouch.CoreData.NSFetchRequest</h3>
<p>Added:</p><pre>
 	public virtual uint FetchOffset {
 		get;
 		set;
 	}
 	public virtual bool IncludesPendingChanges {
 		get;
 		set;
 	}
 	public virtual NSPropertyDescription[] PropertiesToFetch {
 		get;
 		set;
 	}
 	public virtual bool ReturnsDistinctResults {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousTransitionTypeKey {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveStoresWillChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 		public static MonoTouch.Foundation.NSObject ObserveStoresWillChange (EventHandler&lt;NSPersistentStoreCoordinatorStoreChangeEventArgs&gt; handler);
</pre>
<h3>New Type: MonoTouch.CoreData.NSPersistentStoreCoordinatorStoreChangeEventArgs</h3>
<pre>
public class NSPersistentStoreCoordinatorStoreChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	
	public NSPersistentStoreCoordinatorStoreChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
	
	public NSPersistentStoreUbiquitousTransitionType EventType {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreGraphics</h2>
<h3>Type Changed: MonoTouch.CoreGraphics.CGImageProperties</h3>
<p>Removed:</p><pre>
 	public Nullable&lt;int&gt; DPIHeight {
 	public Nullable&lt;int&gt; DPIWidth {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use the DPIHeightF property")]
	public Nullable&lt;int&gt; DPIHeight {
 	public Nullable&lt;float&gt; DPIHeightF {
 		get;
 		set;
 	}
 	[Obsolete("Use the DPIWidthF property")]
	public Nullable&lt;int&gt; DPIWidth {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; DPIWidthF {
</pre>
<h3>New Type: MonoTouch.CoreGraphics.NSDictionaryExtensions</h3>
<pre>
public static class NSDictionaryExtensions {
	
	public static bool ToPoint (MonoTouch.Foundation.NSDictionary dictionary, out System.Drawing.PointF point);
}
</pre>
<h3>New Type: MonoTouch.CoreGraphics.PointFExtensions</h3>
<pre>
public static class PointFExtensions {
	
	public static MonoTouch.Foundation.NSDictionary ToDictionary (System.Drawing.PointF self);
}
</pre>
<h2>Namespace: MonoTouch.CoreImage</h2>
<h3>New Type: MonoTouch.CoreImage.CIBlendWithAlphaMask</h3>
<pre>
public class CIBlendWithAlphaMask : CIBlendWithMask {
	
	public CIBlendWithAlphaMask ();
	public CIBlendWithAlphaMask (IntPtr handle);
}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIBlendWithMask</h3>
<p>Added:</p><pre>
 	public CIBlendWithMask (string name);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIBumpDistortion</h3>
<pre>
public class CIBumpDistortion : CIDistortionFilter {
	
	public CIBumpDistortion ();
	public CIBumpDistortion (IntPtr handle);
	
	public float Scale {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIBumpDistortionLinear</h3>
<pre>
public class CIBumpDistortionLinear : CIDistortionFilter {
	
	public CIBumpDistortionLinear ();
	public CIBumpDistortionLinear (IntPtr handle);
	
	public float Angle {
		get;
		set;
	}
	public float Scale {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIColorClamp</h3>
<pre>
public class CIColorClamp : CIFilter {
	
	public CIColorClamp ();
	public CIColorClamp (IntPtr handle);
	
	public CIImage Image {
		get;
		set;
	}
	public CIVector InputMaxComponents {
		get;
		set;
	}
	public CIVector InputMinComponents {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIColorCrossPolynomial</h3>
<pre>
public class CIColorCrossPolynomial : CIFilter {
	
	public CIColorCrossPolynomial (string name);
	public CIColorCrossPolynomial ();
	public CIColorCrossPolynomial (IntPtr handle);
	
	public CIVector BlueCoefficients {
		get;
		set;
	}
	public CIVector GreenCoefficients {
		get;
		set;
	}
	public CIImage Image {
		get;
		set;
	}
	public CIVector RedCoefficients {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIColorCube</h3>
<p>Added:</p><pre>
 	public CIColorCube (string name);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIColorCubeWithColorSpace</h3>
<pre>
public class CIColorCubeWithColorSpace : CIColorCube {
	
	public CIColorCubeWithColorSpace ();
	public CIColorCubeWithColorSpace (IntPtr handle);
	
	public MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIColorPolynomial</h3>
<pre>
public class CIColorPolynomial : CIColorCrossPolynomial {
	
	public CIColorPolynomial ();
	public CIColorPolynomial (IntPtr handle);
	
	public CIVector AlphaCoefficients {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIContext</h3>
<p>Added:</p><pre>
 	public static CIContext FromContext (MonoTouch.OpenGLES.EAGLContext eaglContext, MonoTouch.Foundation.NSDictionary dictionary);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIConvolution3X3</h3>
<pre>
public class CIConvolution3X3 : CIConvolutionCore {
	
	public CIConvolution3X3 ();
	public CIConvolution3X3 (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIConvolution5X5</h3>
<pre>
public class CIConvolution5X5 : CIConvolutionCore {
	
	public CIConvolution5X5 ();
	public CIConvolution5X5 (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIConvolution9Horizontal</h3>
<pre>
public class CIConvolution9Horizontal : CIConvolutionCore {
	
	public CIConvolution9Horizontal ();
	public CIConvolution9Horizontal (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIConvolution9Vertical</h3>
<pre>
public class CIConvolution9Vertical : CIConvolutionCore {
	
	public CIConvolution9Vertical ();
	public CIConvolution9Vertical (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIConvolutionCore</h3>
<pre>
public class CIConvolutionCore : CIFilter {
	
	public CIConvolutionCore (string name);
	public CIConvolutionCore (IntPtr handle);
	
	public float Bias {
		get;
		set;
	}
	public CIImage Image {
		get;
		set;
	}
	public CIVector Weights {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CILinearGradient</h3>
<p>Added:</p><pre>
 	public CILinearGradient (string name);
</pre>
<h3>New Type: MonoTouch.CoreImage.CILinearToSRGBToneCurve</h3>
<pre>
public class CILinearToSRGBToneCurve : CIFilter {
	
	public CILinearToSRGBToneCurve ();
	public CILinearToSRGBToneCurve (IntPtr handle);
	
	public CIImage Image {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreImage.CIPerspectiveTransform</h3>
<p>Added:</p><pre>
 	public CIPerspectiveTransform (string name);
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPerspectiveTransformWithExtent</h3>
<pre>
public class CIPerspectiveTransformWithExtent : CIPerspectiveTransform {
	
	public CIPerspectiveTransformWithExtent ();
	public CIPerspectiveTransformWithExtent (IntPtr handle);
	
	public CIVector Extent {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffect</h3>
<pre>
public class CIPhotoEffect : CIFilter {
	
	public CIPhotoEffect (string name);
	public CIPhotoEffect (IntPtr handle);
	
	public CIImage Image {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectChrome</h3>
<pre>
public class CIPhotoEffectChrome : CIPhotoEffect {
	
	public CIPhotoEffectChrome ();
	public CIPhotoEffectChrome (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectFade</h3>
<pre>
public class CIPhotoEffectFade : CIPhotoEffect {
	
	public CIPhotoEffectFade ();
	public CIPhotoEffectFade (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectInstant</h3>
<pre>
public class CIPhotoEffectInstant : CIPhotoEffect {
	
	public CIPhotoEffectInstant ();
	public CIPhotoEffectInstant (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectMono</h3>
<pre>
public class CIPhotoEffectMono : CIPhotoEffect {
	
	public CIPhotoEffectMono ();
	public CIPhotoEffectMono (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectNoir</h3>
<pre>
public class CIPhotoEffectNoir : CIPhotoEffect {
	
	public CIPhotoEffectNoir ();
	public CIPhotoEffectNoir (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectProcess</h3>
<pre>
public class CIPhotoEffectProcess : CIPhotoEffect {
	
	public CIPhotoEffectProcess ();
	public CIPhotoEffectProcess (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectTonal</h3>
<pre>
public class CIPhotoEffectTonal : CIPhotoEffect {
	
	public CIPhotoEffectTonal ();
	public CIPhotoEffectTonal (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIPhotoEffectTransfer</h3>
<pre>
public class CIPhotoEffectTransfer : CIPhotoEffect {
	
	public CIPhotoEffectTransfer ();
	public CIPhotoEffectTransfer (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIQRCodeGenerator</h3>
<pre>
public class CIQRCodeGenerator : CIFilter {
	
	public CIQRCodeGenerator ();
	public CIQRCodeGenerator (IntPtr handle);
	
	public string CorrectionLevel {
		get;
		set;
	}
	public MonoTouch.Foundation.NSData Message {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CISRGBToneCurveToLinear</h3>
<pre>
public class CISRGBToneCurveToLinear : CIFilter {
	
	public CISRGBToneCurveToLinear ();
	public CISRGBToneCurveToLinear (IntPtr handle);
	
	public CIImage Image {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CISmoothLinearGradient</h3>
<pre>
public class CISmoothLinearGradient : CILinearGradient {
	
	public CISmoothLinearGradient ();
	public CISmoothLinearGradient (IntPtr handle);
}
</pre>
<h3>New Type: MonoTouch.CoreImage.CIVignetteEffect</h3>
<pre>
public class CIVignetteEffect : CIFilter {
	
	public CIVignetteEffect ();
	public CIVignetteEffect (IntPtr handle);
	
	public CIVector Center {
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
	public float Radius {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>Type Changed: MonoTouch.CoreMedia.CMFormatDescriptionError</h3>
<p>Removed:</p><pre>
 	AllocationFailed
</pre>
<p>Added:</p><pre>
 	AllocationFailed,
 	ValueNotAvailable
</pre>
<h2>Namespace: MonoTouch.CoreMidi</h2>
<h3>Type Changed: MonoTouch.CoreMidi.MidiClient</h3>
<p>Removed:</p><pre>
 	public MidiEndpoint CreateVirtualSource (string name);
</pre>
<p>Added:</p><pre>
 	[Obsolete("It is better to use CreateVirtualSource (string name, out MidiError statusCode) to flag errors")]
	public MidiEndpoint CreateVirtualSource (string name);
 	public MidiEndpoint CreateVirtualSource (string name, out MidiError statusCode);
</pre>
<h2>Namespace: MonoTouch.CoreMotion</h2>
<h3>New Type: MonoTouch.CoreMotion.CMMotionActivity</h3>
<pre>
public class CMMotionActivity : MonoTouch.Foundation.NSObject {
	
	public CMMotionActivity (MonoTouch.Foundation.NSCoder coder);
	public CMMotionActivity (MonoTouch.Foundation.NSObjectFlag t);
	public CMMotionActivity (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	
	public virtual bool Automotive {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual CMMotionActivityConfidence Confidence {
		get;
	}
	public virtual bool Running {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate StartDate {
		get;
	}
	public virtual bool Stationary {
		get;
	}
	public virtual bool Unknown {
		get;
	}
	public virtual bool Walking {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreMotion.CMMotionActivityConfidence</h3>
<pre>
[Serializable]
public enum CMMotionActivityConfidence {
	Low,
	Medium,
	High
}
</pre>
<h3>New Type: MonoTouch.CoreMotion.CMMotionActivityHandler</h3>
<pre>
[Serializable]
public delegate void CMMotionActivityHandler (CMMotionActivity activity);
</pre>
<h3>New Type: MonoTouch.CoreMotion.CMMotionActivityManager</h3>
<pre>
public class CMMotionActivityManager : MonoTouch.Foundation.NSObject {
	
	public CMMotionActivityManager ();
	public CMMotionActivityManager (MonoTouch.Foundation.NSCoder coder);
	public CMMotionActivityManager (MonoTouch.Foundation.NSObjectFlag t);
	public CMMotionActivityManager (IntPtr handle);
	
	public virtual void QueryActivity (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityHandler handler);
	public virtual System.Threading.Tasks.Task<cmmotionactivity> QueryActivityAsync (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue);
	public virtual void StartActivityUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityQueryHandler handler);
	public virtual void StopActivityUpdates ();
	
	public static bool IsActivityAvailable {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</cmmotionactivity></pre>
<h3>New Type: MonoTouch.CoreMotion.CMMotionActivityQueryHandler</h3>
<pre>
[Serializable]
public delegate void CMMotionActivityQueryHandler (CMMotionActivity[] activities, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.CoreMotion.CMStepCounter</h3>
<pre>
public class CMStepCounter : MonoTouch.Foundation.NSObject {
	
	public CMStepCounter ();
	public CMStepCounter (MonoTouch.Foundation.NSCoder coder);
	public CMStepCounter (MonoTouch.Foundation.NSObjectFlag t);
	public CMStepCounter (IntPtr handle);
	
	public virtual void QueryStepCount (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue, CMStepQueryHandler handler);
	public virtual System.Threading.Tasks.Task<int> QueryStepCountAsync (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue);
	public virtual void StartStepCountingUpdates (MonoTouch.Foundation.NSOperationQueue queue, int stepCounts, CMStepUpdateHandler handler);
	public virtual void StopStepCountingUpdates ();
	
	public static bool IsStepCountingAvailable {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
}
</int></pre>
<h3>New Type: MonoTouch.CoreMotion.CMStepQueryHandler</h3>
<pre>
[Serializable]
public delegate void CMStepQueryHandler (int numberOfSteps, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.CoreMotion.CMStepUpdateHandler</h3>
<pre>
[Serializable]
public delegate void CMStepUpdateHandler (int numberOfSteps, MonoTouch.Foundation.NSDate timestamp, MonoTouch.Foundation.NSError error);
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>Type Changed: MonoTouch.CoreText.CTFontManager</h3>
<p>Added:</p><pre>
 	
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveRegisteredFontsChanged (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVPixelFormatDescription</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSDictionary[] AllTypes {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSDictionary Create (CVPixelFormatType pixelFormat);
 	public static void Register (MonoTouch.Foundation.NSDictionary description, CVPixelFormatType pixelFormat);
 	public static MonoTouch.Foundation.NSNumber[] AllTypes {
</pre>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKEventStore</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;EKReminder[]&gt; FetchRemindersAsync (MonoTouch.Foundation.NSPredicate predicate, out IntPtr result);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.DictionaryContainer</h3>
<p>Added:</p><pre>
 	protected DictionaryContainer ();
 	protected DictionaryContainer (NSDictionary dictionary);
 	
</pre>
<h3>New Type: MonoTouch.Foundation.INSMachPortDelegate</h3>
<pre>
public interface INSMachPortDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSPortDelegate</h3>
<pre>
public interface INSPortDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlSessionDataDelegate</h3>
<pre>
public interface INSUrlSessionDataDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlSessionDelegate</h3>
<pre>
public interface INSUrlSessionDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlSessionDownloadDelegate</h3>
<pre>
public interface INSUrlSessionDownloadDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.INSUrlSessionTaskDelegate</h3>
<pre>
public interface INSUrlSessionTaskDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSActivityOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSActivityOptions : ulong {
	IdleDisplaySleepDisabled,
	IdleSystemSleepDisabled,
	SuddenTerminationDisabled,
	AutomaticTerminationDisabled,
	UserInitiated,
	Background,
	LatencyCritical
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Removed:</p><pre>
 	public NSAttributedString (NSUrl url, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary documentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, ref NSDictionary resultDocumentAttributes, ref NSError error);
 	public virtual NSDictionary GetAttributes (int location, out NSRange effectiveRange);
 	public virtual string Value {
</pre>
<p>Added:</p><pre>
 	public NSAttributedString (NSUrl url, ref NSError error);
 	public NSAttributedString (NSData data, ref NSError error);
 	public NSAttributedString (NSUrl url, NSDictionary options, out NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes options, out NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSDictionary options, out NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, out NSDictionary resultDocumentAttributes, ref NSError error);
 	public NSDictionary GetAttributes (int location, out NSRange effectiveRange);
 	public virtual IntPtr LowLevelGetAttributes (int location, out NSRange effectiveRange);
 	public virtual IntPtr LowLevelValue {
 		get;
 	}
 	public string Value {
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSBundle</h3>
<p>Added:</p><pre>
 	public static string [] GetPathsForResources (string fileExtension, string bundlePath);
 	public virtual string PathForResource (string name, string ofType, string subpath);
 	public string [] PathsForResources (string fileExtension);
 	public virtual string [] PathsForResources (string fileExtension, string subDirectory);
 	public virtual string [] PathsForResources (string fileExtension, string subDirectory, string localizationName);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSDocumentType</h3>
<p>Removed:</p><pre>
 	RTFD
</pre>
<p>Added:</p><pre>
 	RTFD,
 	HTML
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSError</h3>
<p>Added:</p><pre>
 	public static NSString NSUrlErrorDomain {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSExpression</h3>
<p>Added:</p><pre>
 	public static NSExpression FromAnyKey ();
 	public virtual void AllowEvaluation ();
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSExpressionType</h3>
<p>Added:</p><pre>
 	AnyKey,
</pre>
<h3>New Type: MonoTouch.Foundation.NSKeyValueSorting_NSMutableOrderedSet</h3>
<pre>
public static class NSKeyValueSorting_NSMutableOrderedSet {
	
	public static void SortUsingDescriptors (NSMutableOrderedSet This, NSSortDescriptor[] sortDescriptors);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSKeyValueSorting_NSOrderedSet</h3>
<pre>
public static class NSKeyValueSorting_NSOrderedSet {
	
	public static NSObject[] GetSortedArray (NSOrderedSet This, NSSortDescriptor[] sortDescriptors);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMachPortDelegate</h3>
<p>Removed:</p><pre>
 public class NSMachPortDelegate : NSPortDelegate {
</pre>
<p>Added:</p><pre>
 public class NSMachPortDelegate : NSPortDelegate, INSMachPortDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSMachPortDelegate_Extensions</h3>
<pre>
public static class NSMachPortDelegate_Extensions {
	
	public static void MachMessageReceived (INSMachPortDelegate This, IntPtr msgHeader);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMetadataQuery</h3>
<p>Added:</p><pre>
 	public virtual void EnumerateResultsUsingBlock (NSMetadataQueryEnumerationCallback callback);
 	public virtual void EnumerateResultsWithOptions (NSEnumerationOptions opts, NSMetadataQueryEnumerationCallback block);
 	public virtual NSOperationQueue OperationQueue {
 		get;
 		set;
 	}
 	public virtual NSObject[] SearchItems {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSMetadataQueryEnumerationCallback</h3>
<pre>
[Serializable]
public delegate void NSMetadataQueryEnumerationCallback (NSObject result, uint idx, ref bool stop);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSMutableAttributedString</h3>
<p>Removed:</p><pre>
 	public virtual void SetAttributes (NSDictionary attrs, NSRange range);
</pre>
<p>Added:</p><pre>
 	public void AddAttributes (MonoTouch.UIKit.UIStringAttributes attrs, NSRange range);
 	public virtual void LowLevelSetAttributes (IntPtr dictionaryAttrsHandle, NSRange range);
 	public void SetAttributes (NSDictionary attributes, NSRange range);
 	public void SetAttributes (MonoTouch.UIKit.UIStringAttributes attrs, NSRange range);
</pre>
<h3>New Type: MonoTouch.Foundation.NSMutableCharacterSet</h3>
<pre>
public class NSMutableCharacterSet : NSCharacterSet {
	
	public NSMutableCharacterSet ();
	public NSMutableCharacterSet (NSCoder coder);
	public NSMutableCharacterSet (NSObjectFlag t);
	public NSMutableCharacterSet (IntPtr handle);
	
	public virtual void AddCharacters (NSRange aRange);
	public virtual void AddCharacters (NSString str);
	public virtual void IntersectWith (NSCharacterSet otherSet);
	public virtual void Invert ();
	public virtual void RemoveCharacters (NSRange aRange);
	public virtual void RemoveCharacters (NSString str);
	public virtual void UnionWith (NSCharacterSet otherSet);
	
	public override IntPtr ClassHandle {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNotificationQueue</h3>
<p>Removed:</p><pre>
 	public static NSObject DefaultQueue {
</pre>
<p>Added:</p><pre>
 	public static NSNotificationQueue DefaultQueue {
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSNumber</h3>
<p>Removed:</p><pre>
 public class NSNumber : NSValue {
</pre>
<p>Added:</p><pre>
 public class NSNumber : NSValue, IComparable, IComparable&lt;NSNumber&gt; {
 	public int CompareTo (NSNumber other);
 	public int CompareTo (object obj);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSPortDelegate</h3>
<p>Removed:</p><pre>
 public class NSPortDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSPortDelegate : NSObject, INSPortDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSPortDelegate_Extensions</h3>
<pre>
public static class NSPortDelegate_Extensions {
	
	public static void MessageReceived (INSPortDelegate This, NSPortMessage message);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSPredicate</h3>
<p>Added:</p><pre>
 	public virtual void AllowEvaluation ();
</pre>
<h3>New Type: MonoTouch.Foundation.NSPredicateSupport_NSMutableOrderedSet</h3>
<pre>
public static class NSPredicateSupport_NSMutableOrderedSet {
	
	public static void FilterUsingPredicate (NSMutableOrderedSet This, NSPredicate p);
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSPredicateSupport_NSOrderedSet</h3>
<pre>
public static class NSPredicateSupport_NSOrderedSet {
	
	public static NSOrderedSet FilterUsingPredicate (NSOrderedSet This, NSPredicate p);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSProcessInfo</h3>
<p>Removed:</p><pre>
 	public virtual void DisableAutomaticTermination (string reason);
 	public virtual void DisableSuddenTermination ();
 	public virtual void EnableAutomaticTermination (string reason);
 	public virtual void EnableSuddenTermination ();
 	public virtual bool AutomaticTerminationSupportEnabled {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual NSObject BeginActivity (NSActivityOptions options, string reason);
 	public virtual void EndActivity (NSObject activity);
 	public virtual void PerformActivity (NSActivityOptions options, string reason, NSAction runCode);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSSortDescriptor</h3>
<p>Added:</p><pre>
 	public virtual void AllowEvaluation ();
</pre>
<h3>New Type: MonoTouch.Foundation.NSURLUtilities_NSString</h3>
<pre>
public static class NSURLUtilities_NSString {
	
	public static NSString CreateStringByAddingPercentEncoding (NSString This, NSCharacterSet allowedCharacters);
	public static NSString CreateStringByAddingPercentEscapes (NSString This, NSStringEncoding enc);
	public static NSString CreateStringByRemovingPercentEncoding (NSString This);
	public static NSString CreateStringByReplacingPercentEscapes (NSString This, NSStringEncoding enc);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrl</h3>
<p>Added:</p><pre>
 	public NSUrl (IntPtr ptrUtf8path, bool isDir, NSUrl baseURL);
 	public static NSUrl FromUTF8Pointer (IntPtr ptrUtf8path, bool isDir, NSUrl baseURL);
 	public virtual bool GetFileSystemRepresentation (IntPtr buffer, int maxBufferLength);
 	public virtual void RemoveAllCachedResourceValues ();
 	public virtual void RemoveCachedResourceValueForKey (NSString key);
 	public virtual void SetTemporaryResourceValue (NSObject value, NSString key);
 	public static NSString UbiquitousItemDownloadingErrorKey {
 		get;
 	}
 	public static NSString UbiquitousItemDownloadingStatusCurrent {
 		get;
 	}
 	public static NSString UbiquitousItemDownloadingStatusDownloaded {
 		get;
 	}
 	public static NSString UbiquitousItemDownloadingStatusKey {
 		get;
 	}
 	public static NSString UbiquitousItemDownloadingStatusNotDownloaded {
 		get;
 	}
 	public static NSString UbiquitousItemUploadingErrorKey {
 		get;
 	}
 	public virtual IntPtr GetFileSystemRepresentationAsUtf8Ptr {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlComponents</h3>
<pre>
public class NSUrlComponents : NSObject {
	
	public NSUrlComponents ();
	public NSUrlComponents (NSCoder coder);
	public NSUrlComponents (NSObjectFlag t);
	public NSUrlComponents (IntPtr handle);
	public NSUrlComponents (NSUrl url, bool resolveAgainstBaseUrl);
	public NSUrlComponents (string urlString);
	
	public static NSUrlComponents FromString (string urlString);
	public static NSUrlComponents FromUrl (NSUrl url, bool resolvingAgainstBaseUrl);
	protected override void Dispose (bool disposing);
	public virtual NSUrl GetRelativeUrl (NSUrl baseUrl);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string Fragment {
		get;
		set;
	}
	public virtual string Host {
		get;
		set;
	}
	public virtual string Password {
		get;
		set;
	}
	public virtual string Path {
		get;
		set;
	}
	public virtual string PercentEncodedFragment {
		get;
		set;
	}
	public virtual string PercentEncodedHost {
		get;
		set;
	}
	public virtual string PercentEncodedPassword {
		get;
		set;
	}
	public virtual string PercentEncodedPath {
		get;
		set;
	}
	public virtual string PercentEncodedQuery {
		get;
		set;
	}
	public virtual string PercentEncodedUser {
		get;
		set;
	}
	public virtual NSNumber Port {
		get;
		set;
	}
	public virtual string Query {
		get;
		set;
	}
	public virtual string Scheme {
		get;
		set;
	}
	public virtual NSUrl Url {
		get;
	}
	public virtual string User {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlCredentialPersistence</h3>
<p>Removed:</p><pre>
 	Permanent
</pre>
<p>Added:</p><pre>
 	Permanent,
 	Synchronizable
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlCredentialStorage</h3>
<p>Added:</p><pre>
 	public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace, NSDictionary options);
 	public static NSString ChangedNotification {
 		get;
 	}
 	public static NSString RemoveSynchronizableCredentials {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static NSObject ObserveChanged (EventHandler&lt;NSNotificationEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlErrorCancelledReason</h3>
<pre>
[Serializable]
public enum NSUrlErrorCancelledReason {
	UserForceQuitApplication,
	BackgroundUpdatesDisabled
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSession</h3>
<p>Removed:</p><pre>
 	public virtual NSUrlSessionDataTask DataTaskWithRequest (NSUrlRequest request);
 	public virtual NSUrlSessionDataTask DataTaskWithRequest (NSUrlRequest request, Action&lt;NSData,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; DataTaskWithRequestAsync (NSUrlRequest request);
 	public virtual NSUrlSessionDataTask DataTaskWithURL (NSUrl url);
 	public virtual NSUrlSessionDataTask DataTaskWithURL (NSUrl url, Action&lt;NSData,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; DataTaskWithURLAsync (NSUrl url);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithRequest (NSUrlRequest request);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithRequest (NSUrlRequest request, Action&lt;NSUrl,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; DownloadTaskWithRequestAsync (NSUrlRequest request);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithResumeData (NSData resumeData);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithResumeData (NSData resumeData, Action&lt;NSUrl,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; DownloadTaskWithResumeDataAsync (NSData resumeData);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithURL (NSUrl url);
 	public virtual NSUrlSessionDownloadTask DownloadTaskWithURL (NSUrl url, Action&lt;NSUrl,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; DownloadTaskWithURLAsync (NSUrl url);
 	public virtual void GetTasks (Action&lt;NSUrlSessionDataTask[],NSUrlSessionUploadTask[],NSUrlSessionDownloadTask[]&gt; completionHandler);
 	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSData bodyData);
 	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSData bodyData, Action&lt;NSData,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSUrl fileURL);
 	public virtual NSUrlSessionUploadTask UploadTaskWithRequest (NSUrlRequest request, NSUrl fileURL, Action&lt;NSData,NSUrlResponse,NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; UploadTaskWithRequestAsync (NSUrlRequest request, NSData bodyData);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; UploadTaskWithRequestAsync (NSUrlRequest request, NSUrl fileURL);
 	public virtual NSUrlSessionUploadTask UploadTaskWithStreamedRequest (NSUrlRequest request);
</pre>
<p>Added:</p><pre>
 	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url);
 	public virtual NSUrlSessionDataTask CreateDataTask (NSUrl url, NSUrlSessionResponse completionHandler);
 	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request);
 	public virtual NSUrlSessionDataTask CreateDataTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateDataTaskAsync (NSUrl url);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateDataTaskAsync (NSUrl url, out NSUrlSessionDataTask result);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateDataTaskAsync (NSUrlRequest request);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateDataTaskAsync (NSUrlRequest request, out NSUrlSessionDataTask result);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSData resumeData);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskAsync (NSUrl url);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskAsync (NSUrl url, out NSUrlSessionDownloadTask result);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskAsync (NSUrlRequest request);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskAsync (NSUrlRequest request, out NSUrlSessionDownloadTask result);
 	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskFromResumeDataAsync (NSData resumeData);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDownloadTaskRequest&gt; CreateDownloadTaskFromResumeDataAsync (NSData resumeData, out NSUrlSessionDownloadTask result);
 	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request);
 	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData);
 	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSData bodyData, NSUrlSessionResponse completionHandler);
 	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL);
 	public virtual NSUrlSessionUploadTask CreateUploadTask (NSUrlRequest request, NSUrl fileURL, NSUrlSessionResponse completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateUploadTaskAsync (NSUrlRequest request, NSData bodyData, out NSUrlSessionUploadTask result);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL);
 	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionDataTaskRequest&gt; CreateUploadTaskAsync (NSUrlRequest request, NSUrl fileURL, out NSUrlSessionUploadTask result);
 	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionActiveTasks</h3>
<p>Removed:</p><pre>
 	public NSUrlSessionActiveTasks (NSUrlSessionDataTask[] arg1, NSUrlSessionUploadTask[] arg2, NSUrlSessionDownloadTask[] arg3);
 	public NSUrlSessionDataTask[] Arg1 {
 	public NSUrlSessionUploadTask[] Arg2 {
 	public NSUrlSessionDownloadTask[] Arg3 {
</pre>
<p>Added:</p><pre>
 	public NSUrlSessionActiveTasks (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
 	public NSUrlSessionDataTask[] DataTasks {
 	public NSUrlSessionDownloadTask[] DownloadTasks {
 	public NSUrlSessionUploadTask[] UploadTasks {
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDataDelegate</h3>
<p>Removed:</p><pre>
 public class NSUrlSessionDataDelegate : NSUrlSessionTaskDelegate {
</pre>
<p>Added:</p><pre>
 public class NSUrlSessionDataDelegate : NSUrlSessionTaskDelegate, INSUrlSessionDataDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDataDelegate_Extensions</h3>
<pre>
public static class NSUrlSessionDataDelegate_Extensions {
	
	public static void DidBecomeDownloadTask (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionDownloadTask downloadTask);
	public static void DidReceiveData (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSData data);
	public static void DidReceiveResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlResponse response, Action<nsurlsessionresponsedisposition> completionHandler);
	public static void WillCacheResponse (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSCachedUrlResponse proposedResponse, Action<nscachedurlresponse> completionHandler);
}
</nscachedurlresponse></nsurlsessionresponsedisposition></pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDataTaskRequest</h3>
<p>Removed:</p><pre>
 	public NSUrlSessionDataTaskRequest (NSData arg1, NSUrlResponse arg2);
 	public NSData Arg1 {
 	public NSUrlResponse Arg2 {
</pre>
<p>Added:</p><pre>
 	public NSUrlSessionDataTaskRequest (NSData data, NSUrlResponse response);
 	public NSData Data {
 	public NSUrlResponse Response {
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDelegate</h3>
<p>Removed:</p><pre>
 public class NSUrlSessionDelegate : NSObject {
</pre>
<p>Added:</p><pre>
 public class NSUrlSessionDelegate : NSObject, INSUrlSessionDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDelegate_Extensions</h3>
<pre>
public static class NSUrlSessionDelegate_Extensions {
	
	public static void DidBecomeInvalid (INSUrlSessionDelegate This, NSUrlSession session, NSError error);
	public static void DidFinishEventsForBackgroundSession (INSUrlSessionDelegate This, NSUrlSession session);
	public static void DidReceiveChallenge (INSUrlSessionDelegate This, NSUrlSession session, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
}
</nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadDelegate</h3>
<p>Removed:</p><pre>
 public class NSUrlSessionDownloadDelegate : NSUrlSessionTaskDelegate {
</pre>
<p>Added:</p><pre>
 public class NSUrlSessionDownloadDelegate : NSUrlSessionTaskDelegate, INSUrlSessionDownloadDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionDownloadDelegate_Extensions</h3>
<pre>
public static class NSUrlSessionDownloadDelegate_Extensions {
	
	public static void DidFinishDownloading (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
	public static void DidResume (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long resumeFileOffset, long expectedTotalBytes);
	public static void DidWriteData (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, long bytesWritten, long totalBytesWritten, long totalBytesExpectedToWrite);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTask</h3>
<p>Added:</p><pre>
 	public virtual void Cancel (Action&lt;NSData&gt; resumeCallback);
 	
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTaskRequest</h3>
<p>Removed:</p><pre>
 	public NSUrlSessionDownloadTaskRequest (NSUrl arg1, NSUrlResponse arg2);
 	public NSUrl Arg1 {
 	public NSUrlResponse Arg2 {
</pre>
<p>Added:</p><pre>
 	public NSUrlSessionDownloadTaskRequest (NSData data, NSUrlResponse response);
 	public NSData Data {
 	public NSUrlResponse Response {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionPendingTasks</h3>
<pre>
[Serializable]
public delegate void NSUrlSessionPendingTasks (NSUrlSessionDataTask[] dataTasks, NSUrlSessionUploadTask[] uploadTasks, NSUrlSessionDownloadTask[] downloadTasks);
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionResponse</h3>
<pre>
[Serializable]
public delegate void NSUrlSessionResponse (NSData data, NSUrlResponse response, NSError error);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlSessionTaskDelegate</h3>
<p>Removed:</p><pre>
 public class NSUrlSessionTaskDelegate : NSUrlSessionDelegate {
</pre>
<p>Added:</p><pre>
 public class NSUrlSessionTaskDelegate : NSUrlSessionDelegate, INSUrlSessionTaskDelegate {
</pre>
<h3>New Type: MonoTouch.Foundation.NSUrlSessionTaskDelegate_Extensions</h3>
<pre>
public static class NSUrlSessionTaskDelegate_Extensions {
	
	public static void DidCompleteWithError (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSError error);
	public static void DidReceiveChallenge (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, Action<nsurlsessionauthchallengedisposition,nsurlcredential> completionHandler);
	public static void DidSendBodyData (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public static void NeedNewBodyStream (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, Action<nsinputstream> completionHandler);
	public static void WillPerformHttpRedirection (INSUrlSessionTaskDelegate This, NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, Action<nsurlrequest> completionHandler);
}
</nsurlrequest></nsinputstream></nsurlsessionauthchallengedisposition,nsurlcredential></pre>
<h3>New Type: MonoTouch.Foundation.NSUrlUtilities_NSCharacterSet</h3>
<pre>
public static class NSUrlUtilities_NSCharacterSet {
	
	public static NSCharacterSet UrlFragmentAllowedCharacterSet {
		get;
	}
	public static NSCharacterSet UrlHostAllowedCharacterSet {
		get;
	}
	public static NSCharacterSet UrlPasswordAllowedCharacterSet {
		get;
	}
	public static NSCharacterSet UrlPathAllowedCharacterSet {
		get;
	}
	public static NSCharacterSet UrlQueryAllowedCharacterSet {
		get;
	}
	public static NSCharacterSet UrlUserAllowedCharacterSet {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUserDefaults</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public NSUserDefaults (string username);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 and OSX 10.9")]
	public NSUserDefaults (string name);
 	public NSUserDefaults (string name, NSUserDefaultsType type);
</pre>
<h3>New Type: MonoTouch.Foundation.NSUserDefaultsType</h3>
<pre>
[Serializable]
public enum NSUserDefaultsType {
	UserName,
	SuiteName
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.ProtocolAttribute</h3>
<p>Added:</p><pre>
 	public string Name {
 		get;
 		set;
 	}
</pre>
<h2>Namespace: MonoTouch.GameController</h2>
<h3>Type Changed: MonoTouch.GameController.GCController</h3>
<p>Added:</p><pre>
 	public const int PlayerIndexUnset = -1;
 	
</pre>
<h3>New Type: MonoTouch.GameController.GCExtendedGamepadSnapShotDataV100</h3>
<pre>
public struct GCExtendedGamepadSnapShotDataV100 {
	
	public MonoTouch.Foundation.NSData ToNSData ();
	
	public ushort Version;
	public ushort Size;
	public float DPadX;
	public float DPadY;
	public float ButtonA;
	public float ButtonB;
	public float ButtonX;
	public float ButtonY;
	public float LeftShoulder;
	public float RightShoulder;
	public float LeftThumbstickX;
	public float LeftThumbstickY;
	public float RightThumbstickX;
	public float RightThumbstickY;
	public float LeftTrigger;
	public float RightTrigger;
}
</pre>
<h3>Type Changed: MonoTouch.GameController.GCExtendedGamepadSnapshot</h3>
<p>Removed:</p><pre>
 	public GCExtendedGamepadSnapshot ();
</pre>
<p>Added:</p><pre>
 	public static bool TryGetSnapShotData (MonoTouch.Foundation.NSData data, out GCExtendedGamepadSnapShotDataV100 snapshotData);
</pre>
<h3>Type Changed: MonoTouch.GameController.GCGamepad</h3>
<p>Removed:</p><pre>
 	public virtual GCControllerDirectionPad Dpad {
</pre>
<p>Added:</p><pre>
 	public virtual GCControllerDirectionPad DPad {
</pre>
<h3>New Type: MonoTouch.GameController.GCGamepadSnapShotDataV100</h3>
<pre>
public struct GCGamepadSnapShotDataV100 {
	
	public MonoTouch.Foundation.NSData ToNSData ();
	
	public ushort Version;
	public ushort Size;
	public float DPadX;
	public float DPadY;
	public float ButtonA;
	public float ButtonB;
	public float ButtonX;
	public float ButtonY;
	public float LeftShoulder;
	public float RightShoulder;
}
</pre>
<h3>Type Changed: MonoTouch.GameController.GCGamepadSnapshot</h3>
<p>Removed:</p><pre>
 	public GCGamepadSnapshot ();
</pre>
<p>Added:</p><pre>
 	public static bool TryGetSnapshotData (MonoTouch.Foundation.NSData data, out GCGamepadSnapShotDataV100 snapshotData);
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKAchievement</h3>
<p>Removed:</p><pre>
 	public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
 	public virtual void ReportAchievement (GKNotificationHandler completionHandler);
 	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();
</pre>
<p>Added:</p><pre>
 	public GKAchievement (string identifier, string playerId);
 	public static void ReportAchievements (GKAchievement[] achievements, GKChallenge[] challenges, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements, GKChallenge[] challenges);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual void ReportAchievement (GKNotificationHandler completionHandler);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();
 	public virtual string PlayerID {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeComposeHandler</h3>
<pre>
[Serializable]
public delegate void GKChallengeComposeHandler (MonoTouch.UIKit.UIViewController composeController, bool issuedChallenge, string [] sentPlayerIDs);
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeListener</h3>
<pre>
public class GKChallengeListener : MonoTouch.Foundation.NSObject, IGKChallengeListener {
	
	public GKChallengeListener ();
	public GKChallengeListener (MonoTouch.Foundation.NSCoder coder);
	public GKChallengeListener (MonoTouch.Foundation.NSObjectFlag t);
	public GKChallengeListener (IntPtr handle);
	
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKChallengeListener_Extensions</h3>
<pre>
public static class GKChallengeListener_Extensions {
	
	public static void DidCompleteChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void DidReceiveChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
	public static void IssuedChallengeWasCompleted (IGKChallengeListener This, GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public static void WantsToPlayChallenge (IGKChallengeListener This, GKPlayer player, GKChallenge challenge);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKError</h3>
<p>Removed:</p><pre>
 	TurnBasedInvalidState
</pre>
<p>Added:</p><pre>
 	TurnBasedInvalidState,
 	InvitationsDisabled
</pre>
<h3>New Type: MonoTouch.GameKit.GKIdentityVerificationSignatureHandler</h3>
<pre>
[Serializable]
public delegate void GKIdentityVerificationSignatureHandler (MonoTouch.Foundation.NSUrl publicKeyUrl, MonoTouch.Foundation.NSData signature, MonoTouch.Foundation.NSData salt, ulong timestamp, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.GameKit.GKInviteEventListener</h3>
<pre>
public class GKInviteEventListener : MonoTouch.Foundation.NSObject, IGKInviteEventListener {
	
	public GKInviteEventListener ();
	public GKInviteEventListener (MonoTouch.Foundation.NSCoder coder);
	public GKInviteEventListener (MonoTouch.Foundation.NSObjectFlag t);
	public GKInviteEventListener (IntPtr handle);
	
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidRequestMatch (GKPlayer player, string [] playerIDs);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKInviteEventListener_Extensions</h3>
<pre>
public static class GKInviteEventListener_Extensions {
	
	public static void DidAcceptInvite (IGKInviteEventListener This, GKPlayer player, GKInvite invite);
	public static void DidRequestMatch (IGKInviteEventListener This, GKPlayer player, string [] playerIDs);
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKInviteHandler</h3>
<p>Removed:</p><pre>
 public delegate void GKInviteHandler (GKInvite invite, string [] players);
</pre>
<p>Added:</p><pre>
 public delegate void GKInviteHandler (GKInvite invite, string [] playerIDs);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboard</h3>
<p>Removed:</p><pre>
 	public static void SetDefaultLeaderboard (string categoryID, GKNotificationHandler notificationHandler);
 	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string categoryID);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 7.0")]
	public static void SetDefaultLeaderboard (string leaderboardIdentifier, GKNotificationHandler notificationHandler);
 	[Obsolete("Deprecated in iOS 7.0")]
	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string leaderboardIdentifier);
 	public virtual void LoadImage (GKImageLoadedHandler completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.UIKit.UIImage&gt; LoadImageAsync ();
 	public virtual string Identifier {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.GameKit.GKLeaderboardSet</h3>
<pre>
public class GKLeaderboardSet : MonoTouch.Foundation.NSObject {
	
	public GKLeaderboardSet ();
	public GKLeaderboardSet (MonoTouch.Foundation.NSCoder coder);
	public GKLeaderboardSet (MonoTouch.Foundation.NSObjectFlag t);
	public GKLeaderboardSet (IntPtr handle);
	
	public static void LoadLeaderboardSets (GKLeaderboardSetsHandler completionHandler);
	public static System.Threading.Tasks.Task<gkleaderboardset[]> LoadLeaderboardSetsAsync ();
	public virtual void LoadImage (GKImageLoadedHandler completionHandler);
	public virtual System.Threading.Tasks.Task<monotouch.uikit.uiimage> LoadImageAsync ();
	public virtual void LoadLeaderboards (GKLeaderboardsHandler completionHandler);
	public virtual System.Threading.Tasks.Task<gkleaderboard[]> LoadLeaderboardsAsync ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string GroupIdentifier {
		get;
		set;
	}
	public virtual string Identifier {
		get;
		set;
	}
	public virtual string Title {
		get;
		set;
	}
}
</gkleaderboard[]></monotouch.uikit.uiimage></gkleaderboardset[]></pre>
<h3>New Type: MonoTouch.GameKit.GKLeaderboardSetsHandler</h3>
<pre>
[Serializable]
public delegate void GKLeaderboardSetsHandler (GKLeaderboardSet[] leaderboardSets, MonoTouch.Foundation.NSError error);
</pre>
<h3>New Type: MonoTouch.GameKit.GKLeaderboardsHandler</h3>
<pre>
[Serializable]
public delegate void GKLeaderboardsHandler (GKLeaderboard[] leaderboards, MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLocalPlayer</h3>
<p>Removed:</p><pre>
 	public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
</pre>
<p>Added:</p><pre>
 	public virtual void GenerateIdentityVerificationSignature (GKIdentityVerificationSignatureHandler completionHandler);
 	public virtual void LoadDefaultLeaderboardIdentifier (System.Action&lt;string,MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;string&gt; LoadDefaultLeaderboardIdentifierAsync ();
 	public virtual void RegisterListener (GKLocalPlayerListener listener);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual void SetDefaultLeaderboardCategoryID (string categoryID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
 	public virtual void SetDefaultLeaderboardIdentifier (string leaderboardIdentifier, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardIdentifierAsync (string leaderboardIdentifier);
 	public virtual void UnregisterAllListeners ();
 	public virtual void UnregisterListener (GKLocalPlayerListener listener);
</pre>
<h3>New Type: MonoTouch.GameKit.GKLocalPlayerListener</h3>
<pre>
public class GKLocalPlayerListener : MonoTouch.Foundation.NSObject, IGKChallengeListener, IGKInviteEventListener, IGKLocalPlayerListener, IGKTurnBasedEventListener {
	
	public GKLocalPlayerListener ();
	public GKLocalPlayerListener (MonoTouch.Foundation.NSCoder coder);
	public GKLocalPlayerListener (MonoTouch.Foundation.NSObjectFlag t);
	public GKLocalPlayerListener (IntPtr handle);
	
	public virtual void DidAcceptInvite (GKPlayer player, GKInvite invite);
	public virtual void DidCompleteChallenge (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void DidReceiveChallenge (GKPlayer player, GKChallenge challenge);
	public virtual void DidRequestMatch (GKPlayer player, string [] playerIDs);
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string [] playerIDsToInvite);
	public virtual void IssuedChallengeWasCompleted (GKPlayer player, GKChallenge challenge, GKPlayer friendPlayer);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
	public virtual void WantsToPlayChallenge (GKPlayer player, GKChallenge challenge);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKLocalPlayerListener_Extensions</h3>
<pre>
public static class GKLocalPlayerListener_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmakerViewController</h3>
<p>Removed:</p><pre>
 	public virtual string DefaultInvitationMessage {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual string DefaultInvitationMessage {
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Removed:</p><pre>
 	public GKScore (string category);
 	public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
 	public virtual void ReportScore (GKNotificationHandler errorHandler);
 	public virtual System.Threading.Tasks.Task ReportScoreAsync ();
 	public virtual string category {
</pre>
<p>Added:</p><pre>
 	public GKScore (string categoryOrIdentifier);
 	public GKScore (string identifier, string playerID);
 	public static void ReportScores (GKScore[] scores, GKChallenge[] challenges, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public static System.Threading.Tasks.Task ReportScoresAsync (GKScore[] scores, GKChallenge[] challenges);
 	public virtual MonoTouch.UIKit.UIViewController ChallengeComposeController (string [] playerIDs, string message, GKChallengeComposeHandler completionHandler);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual void IssueChallengeToPlayers (string [] playerIDs, string message);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual void ReportScore (GKNotificationHandler errorHandler);
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual System.Threading.Tasks.Task ReportScoreAsync ();
 	[Obsolete("Deprecated in iOS 7.0")]
	public virtual string category {
 	public virtual string LeaderboardIdentifier {
 		get;
 		set;
 	}
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedEventListener</h3>
<pre>
public class GKTurnBasedEventListener : MonoTouch.Foundation.NSObject, IGKTurnBasedEventListener {
	
	public GKTurnBasedEventListener ();
	public GKTurnBasedEventListener (MonoTouch.Foundation.NSCoder coder);
	public GKTurnBasedEventListener (MonoTouch.Foundation.NSObjectFlag t);
	public GKTurnBasedEventListener (IntPtr handle);
	
	public virtual void DidRequestMatchWithPlayers (GKPlayer player, string [] playerIDsToInvite);
	public virtual void MatchEnded (GKPlayer player, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeCancellation (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeReplies (GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedExchangeRequest (GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public virtual void ReceivedTurnEvent (GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedEventListener_Extensions</h3>
<pre>
public static class GKTurnBasedEventListener_Extensions {
	
	public static void DidRequestMatchWithPlayers (IGKTurnBasedEventListener This, GKPlayer player, string [] playerIDsToInvite);
	public static void MatchEnded (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
	public static void ReceivedExchangeCancellation (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeReplies (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchangeReply[] replies, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedExchangeRequest (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedExchange exchange, GKTurnBasedMatch match);
	public static void ReceivedTurnEvent (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match, bool becameActive);
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedExchange</h3>
<pre>
public class GKTurnBasedExchange : MonoTouch.Foundation.NSObject {
	
	public GKTurnBasedExchange ();
	public GKTurnBasedExchange (MonoTouch.Foundation.NSCoder coder);
	public GKTurnBasedExchange (MonoTouch.Foundation.NSObjectFlag t);
	public GKTurnBasedExchange (IntPtr handle);
	
	public virtual void Cancel (string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, System.Action<monotouch.foundation.nserror> completionHandler);
	public virtual System.Threading.Tasks.Task CancelAsync (string localizableMessage, MonoTouch.Foundation.NSObject[] arguments);
	protected override void Dispose (bool disposing);
	public virtual void Reply (string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, MonoTouch.Foundation.NSData data, System.Action<monotouch.foundation.nserror> completionHandler);
	public virtual System.Threading.Tasks.Task ReplyAsync (string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, MonoTouch.Foundation.NSData data);
	public override string ToString ();
	
	public static double TimeoutDefault {
		get;
	}
	public static double TimeoutNone {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate CompletionDate {
		get;
	}
	public virtual MonoTouch.Foundation.NSData Data {
		get;
	}
	public virtual string ExchangeID {
		get;
	}
	public virtual string Message {
		get;
	}
	public virtual GKTurnBasedParticipant[] Recipients {
		get;
	}
	public virtual GKTurnBasedExchangeReply[] Replies {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate SendDate {
		get;
	}
	public virtual GKTurnBasedParticipant Sender {
		get;
	}
	public virtual GKTurnBasedExchangeStatus Status {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate TimeoutDate {
		get;
	}
}
</monotouch.foundation.nserror></monotouch.foundation.nserror></pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedExchangeReply</h3>
<pre>
public class GKTurnBasedExchangeReply : MonoTouch.Foundation.NSObject {
	
	public GKTurnBasedExchangeReply ();
	public GKTurnBasedExchangeReply (MonoTouch.Foundation.NSCoder coder);
	public GKTurnBasedExchangeReply (MonoTouch.Foundation.NSObjectFlag t);
	public GKTurnBasedExchangeReply (IntPtr handle);
	
	protected override void Dispose (bool disposing);
	public override string ToString ();
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSData Data {
		get;
	}
	public virtual string Message {
		get;
	}
	public virtual GKTurnBasedParticipant Recipient {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.GameKit.GKTurnBasedExchangeStatus</h3>
<pre>
[Serializable]
public enum GKTurnBasedExchangeStatus : sbyte {
	Unknown,
	Active,
	Complete,
	Resolved,
	Canceled
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatch</h3>
<p>Added:</p><pre>
 	public virtual void EndMatchInTurn (MonoTouch.Foundation.NSData matchData, GKScore[] scores, GKAchievement[] achievements, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task EndMatchInTurnAsync (MonoTouch.Foundation.NSData matchData, GKScore[] scores, GKAchievement[] achievements);
 	public virtual void SaveMergedMatchData (MonoTouch.Foundation.NSData matchData, GKTurnBasedExchange[] exchanges, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task SaveMergedMatchDataAsync (MonoTouch.Foundation.NSData matchData, GKTurnBasedExchange[] exchanges);
 	public virtual void SendExchange (GKTurnBasedParticipant[] participants, MonoTouch.Foundation.NSData data, string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, double timeout, System.Action&lt;GKTurnBasedExchange,MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedExchange&gt; SendExchangeAsync (GKTurnBasedParticipant[] participants, MonoTouch.Foundation.NSData data, string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, double timeout);
 	public virtual void SendReminder (GKTurnBasedParticipant[] participants, string localizableMessage, MonoTouch.Foundation.NSObject[] arguments, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
 	public virtual System.Threading.Tasks.Task SendReminderAsync (GKTurnBasedParticipant[] participants, string localizableMessage, MonoTouch.Foundation.NSObject[] arguments);
 	public virtual void SetMessage (string localizableMessage, MonoTouch.Foundation.NSObject[] arguments);
 	public virtual GKTurnBasedExchange[] ActiveExchanges {
 		get;
 	}
 	public virtual GKTurnBasedExchange[] CompletedExchanges {
 		get;
 	}
 	public virtual uint ExchangeMaxInitiatedExchangesPerPlayer {
 		get;
 	}
 	public virtual GKTurnBasedExchange[] Exchanges {
 		get;
 	}
 	public virtual uint ExhangeDataMaximumSize {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKChallengeListener</h3>
<pre>
public interface IGKChallengeListener : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKInviteEventListener</h3>
<pre>
public interface IGKInviteEventListener : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKLocalPlayerListener</h3>
<pre>
public interface IGKLocalPlayerListener : IDisposable, IGKChallengeListener, IGKInviteEventListener, IGKTurnBasedEventListener, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.GameKit.IGKTurnBasedEventListener</h3>
<pre>
public interface IGKTurnBasedEventListener : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h2>Namespace: MonoTouch.ImageIO</h2>
<h3>Type Changed: MonoTouch.ImageIO.CGImageDestination</h3>
<p>Removed:</p><pre>
 	public bool CopyImageSource (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, CGImageDestinationOptions options, out MonoTouch.Foundation.NSError error);
 	public bool CopyImageSource (MonoTouch.CoreGraphics.CGImage image, CGImageMetadata meta, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
</pre>
<p>Added:</p><pre>
 	public bool CopyImageSource (CGImageSource image, CGImageDestinationOptions options, out MonoTouch.Foundation.NSError error);
 	public bool CopyImageSource (CGImageSource image, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGImageMetadataTag</h3>
<p>Removed:</p><pre>
 	public CGImageMetadataTag (MonoTouch.Foundation.NSString xmlns, MonoTouch.Foundation.NSString prefix, MonoTouch.Foundation.NSString name, CGImageMetadataType type, IntPtr typeId);
 	public IntPtr Value {
</pre>
<p>Added:</p><pre>
 	public CGImageMetadataTag (MonoTouch.Foundation.NSString xmlns, MonoTouch.Foundation.NSString prefix, MonoTouch.Foundation.NSString name, CGImageMetadataType type, MonoTouch.Foundation.NSObject value);
 	public CGImageMetadataTag (MonoTouch.Foundation.NSString xmlns, MonoTouch.Foundation.NSString prefix, MonoTouch.Foundation.NSString name, CGImageMetadataType type, bool value);
 	public MonoTouch.Foundation.NSObject Value {
</pre>
<h3>Type Changed: MonoTouch.ImageIO.CGMutableImageMetadata</h3>
<p>Removed:</p><pre>
 	public bool RemoveTag (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, MonoTouch.Foundation.NSString tag);
 	public bool SetValue (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, MonoTouch.CoreFoundation.CFType value);
 	public bool SetValue (MonoTouch.Foundation.NSString dictionaryName, MonoTouch.Foundation.NSString propertyName, MonoTouch.CoreFoundation.CFType value);
</pre>
<p>Added:</p><pre>
 	public bool RemoveTag (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path);
 	public bool SetValue (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, bool value);
 	public bool SetValue (CGImageMetadataTag parent, MonoTouch.Foundation.NSString path, MonoTouch.Foundation.NSObject value);
 	public bool SetValueMatchingImageProperty (MonoTouch.Foundation.NSString dictionaryName, MonoTouch.Foundation.NSString propertyName, bool value);
 	public bool SetValueMatchingImageProperty (MonoTouch.Foundation.NSString dictionaryName, MonoTouch.Foundation.NSString propertyName, MonoTouch.Foundation.NSObject value);
</pre>
<h2>Namespace: MonoTouch.JavaScriptCore</h2>
<h3>New Type: MonoTouch.JavaScriptCore.JSPropertyDescriptorKeys</h3>
<pre>
public static class JSPropertyDescriptorKeys {
	
	public static MonoTouch.Foundation.NSString Configurable {
		get;
	}
	public static MonoTouch.Foundation.NSString Enumerable {
		get;
	}
	public static MonoTouch.Foundation.NSString Get {
		get;
	}
	public static MonoTouch.Foundation.NSString Set {
		get;
	}
	public static MonoTouch.Foundation.NSString Value {
		get;
	}
	public static MonoTouch.Foundation.NSString Writable {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.JavaScriptCore.JSValue</h3>
<p>Removed:</p><pre>
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
 	public JSValue Get (string value, JSContext context);
 	public virtual JSValue Invoke (string method, MonoTouch.Foundation.NSObject[] arguments);
 	public virtual bool IsEqualToObject (MonoTouch.Foundation.NSObject value);
 	public virtual bool IsEqualWithTypeCoercionToObject (MonoTouch.Foundation.NSObject value);
 	public virtual void SetValueAt (MonoTouch.Foundation.NSObject value, uint index);
</pre>
<p>Added:</p><pre>
 	public static JSValue CreateError (string message, JSContext context);
 	public static JSValue CreateRegularExpression (string pattern, string flags, JSContext context);
 	public static JSValue From (bool value, JSContext context);
 	public static JSValue From (double value, JSContext context);
 	public static JSValue From (int value, JSContext context);
 	public static JSValue From (MonoTouch.Foundation.NSObject value, JSContext context);
 	public static JSValue From (MonoTouch.Foundation.NSRange range, JSContext context);
 	public static JSValue From (System.Drawing.PointF point, JSContext context);
 	public static JSValue From (System.Drawing.RectangleF rect, JSContext context);
 	public static JSValue From (System.Drawing.SizeF size, JSContext context);
 	public static JSValue From (string value, JSContext context);
 	public static JSValue From (uint value, JSContext context);
 	public static JSValue Null (JSContext context);
 	public static JSValue Undefined (JSContext context);
 	public virtual JSValue Call (params JSValue[] arguments);
 	public virtual JSValue Construct (params JSValue[] arguments);
 	public virtual JSValue Invoke (string method, params JSValue[] arguments);
 	public virtual bool IsEqualTo (MonoTouch.Foundation.NSObject value);
 	public virtual bool IsEqualWithTypeCoercionTo (MonoTouch.Foundation.NSObject value);
 	public virtual void SetValue (JSValue value, uint index);
</pre>
<h2>Namespace: MonoTouch.MapKit</h2>
<h3>Type Changed: MonoTouch.MapKit.MKMapSnapshotter</h3>
<p>Removed:</p><pre>
 	public virtual void Start (MonoTouch.Foundation.NSObject queue, MKMapSnapshotCompletionHandler completionHandler);
</pre>
<p>Added:</p><pre>
 	public virtual void Start (MonoTouch.CoreFoundation.DispatchQueue queue, MKMapSnapshotCompletionHandler completionHandler);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapView</h3>
<p>Removed:</p><pre>
 	public virtual void AddOverlay (MonoTouch.Foundation.NSObject overlay, MKOverlayLevel level);
 	public void AddOverlays (MKOverlay[] overlays, MKOverlayLevel level);
 	public virtual void AddOverlays (MonoTouch.Foundation.NSObject[] overlays, MKOverlayLevel level);
 	public virtual void ExchangeOverlay (MonoTouch.Foundation.NSObject overlay1, MonoTouch.Foundation.NSObject overlay2);
 	public virtual void InsertOverlay (MonoTouch.Foundation.NSObject overlay, uint index, MKOverlayLevel level);
 	public virtual MonoTouch.Foundation.NSObject[] OverlaysInLevel (MKOverlayLevel level);
 	public virtual MKOverlayRenderer RendererForOverlay (MonoTouch.Foundation.NSObject overlay);
 	public virtual void ShowAnnotations (MonoTouch.Foundation.NSObject[] annotations, bool animated);
 	public MKRendererForOverlayDelegate GetRendererForOverlay {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public virtual void AddOverlay (MKOverlay overlay, MKOverlayLevel level);
 	public virtual void AddOverlays (MKOverlay[] overlays, MKOverlayLevel level);
 	public virtual void ExchangeOverlay (MKOverlay overlay1, MKOverlay overlay2);
 	public virtual void InsertOverlay (MKOverlay overlay, uint index, MKOverlayLevel level);
 	public virtual MKOverlay[] OverlaysInLevel (MKOverlayLevel level);
 	public virtual MKOverlayRenderer RendererForOverlay (MKOverlay overlay);
 	public virtual void ShowAnnotations (MKAnnotation[] annotations, bool animated);
 	public MKRendererForOverlayDelegate OverlayRenderer {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Removed:</p><pre>
 	public virtual MKOverlayRenderer GetRendererForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 	public virtual MKOverlayRenderer OverlayRenderer (MKMapView mapView, MKOverlay overlay);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate_Extensions</h3>
<p>Removed:</p><pre>
 	public static MKOverlayRenderer GetRendererForOverlay (IMKMapViewDelegate This, MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 	public static MKOverlayRenderer OverlayRenderer (IMKMapViewDelegate This, MKMapView mapView, MKOverlay overlay);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKOverlayRenderer</h3>
<p>Removed:</p><pre>
 	public MKOverlayRenderer (MonoTouch.Foundation.NSObject overlay);
 	public virtual MonoTouch.Foundation.NSObject Overlay {
</pre>
<p>Added:</p><pre>
 	public MKOverlayRenderer (MKOverlay overlay);
 	public virtual MKOverlay Overlay {
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKRendererForOverlayDelegate</h3>
<p>Removed:</p><pre>
 public delegate MKOverlayRenderer MKRendererForOverlayDelegate (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
</pre>
<p>Added:</p><pre>
 public delegate MKOverlayRenderer MKRendererForOverlayDelegate (MKMapView mapView, MKOverlay overlay);
</pre>
<h2>Namespace: MonoTouch.MessageUI</h2>
<h3>Type Changed: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate</h3>
<p>Removed:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.IUIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask SupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<h2>Namespace: MonoTouch.MultipeerConnectivity</h2>
<h3>New Type: MonoTouch.MultipeerConnectivity.IMCAdvertiserAssistantDelegate</h3>
<pre>
public interface IMCAdvertiserAssistantDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.IMCBrowserViewControllerDelegate</h3>
<pre>
public interface IMCBrowserViewControllerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.IMCNearbyServiceAdvertiserDelegate</h3>
<pre>
public interface IMCNearbyServiceAdvertiserDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.IMCNearbyServiceBrowserDelegate</h3>
<pre>
public interface IMCNearbyServiceBrowserDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.IMCSessionDelegate</h3>
<pre>
public interface IMCSessionDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);
	void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
	void DidReceiveData (MCSession session, MonoTouch.Foundation.NSData data, MCPeerID peerID);
	void DidReceiveStream (MCSession session, MonoTouch.Foundation.NSInputStream stream, string streamName, MCPeerID peerID);
	void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSProgress progress);
}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistantDelegate</h3>
<p>Removed:</p><pre>
 public class MCAdvertiserAssistantDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MCAdvertiserAssistantDelegate : MonoTouch.Foundation.NSObject, IMCAdvertiserAssistantDelegate {
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCAdvertiserAssistantDelegate_Extensions</h3>
<pre>
public static class MCAdvertiserAssistantDelegate_Extensions {
	
	public static void DidDismissInvitation (IMCAdvertiserAssistantDelegate This, MCAdvertiserAssistant advertiserAssistant);
	public static void WillPresentInvitation (IMCAdvertiserAssistantDelegate This, MCAdvertiserAssistant advertiserAssistant);
}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCBrowserViewControllerDelegate</h3>
<p>Removed:</p><pre>
 public class MCBrowserViewControllerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MCBrowserViewControllerDelegate : MonoTouch.Foundation.NSObject, IMCBrowserViewControllerDelegate {
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCBrowserViewControllerDelegate_Extensions</h3>
<pre>
public static class MCBrowserViewControllerDelegate_Extensions {
	
	public static void DidFinish (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController);
	public static bool ShouldPresentNearbyPeer (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public static void WasCancelled (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController);
}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate</h3>
<p>Removed:</p><pre>
 public class MCNearbyServiceAdvertiserDelegate : MonoTouch.Foundation.NSObject {
 	public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, MonoTouch.Foundation.NSData context, Action&lt;bool,MCSession&gt; invitationHandler);
</pre>
<p>Added:</p><pre>
 public class MCNearbyServiceAdvertiserDelegate : MonoTouch.Foundation.NSObject, IMCNearbyServiceAdvertiserDelegate {
 	public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, MonoTouch.Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate_Extensions</h3>
<pre>
public static class MCNearbyServiceAdvertiserDelegate_Extensions {
	
	public static void DidNotStartAdvertisingPeer (IMCNearbyServiceAdvertiserDelegate This, MCNearbyServiceAdvertiser advertiser, MonoTouch.Foundation.NSError error);
	public static void DidReceiveInvitationFromPeer (IMCNearbyServiceAdvertiserDelegate This, MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, MonoTouch.Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);
}
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceAdvertiserInvitationHandler</h3>
<pre>
[Serializable]
public delegate void MCNearbyServiceAdvertiserInvitationHandler (bool accept, MCSession session);
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCNearbyServiceBrowserDelegate</h3>
<p>Removed:</p><pre>
 public class MCNearbyServiceBrowserDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class MCNearbyServiceBrowserDelegate : MonoTouch.Foundation.NSObject, IMCNearbyServiceBrowserDelegate {
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCNearbyServiceBrowserDelegate_Extensions</h3>
<pre>
public static class MCNearbyServiceBrowserDelegate_Extensions {
	
	public static void DidNotStartBrowsingForPeers (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, MonoTouch.Foundation.NSError error);
	public static void FoundPeer (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, MCPeerID peerID, MonoTouch.Foundation.NSDictionary info);
	public static void LostPeer (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, MCPeerID peerID);
}
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSession</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSObject SendResource (MonoTouch.Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSProgress SendResource (MonoTouch.Foundation.NSUrl resourceUrl, string resourceName, MCPeerID peerID, System.Action&lt;MonoTouch.Foundation.NSError&gt; completionHandler);
</pre>
<h3>Type Changed: MonoTouch.MultipeerConnectivity.MCSessionDelegate</h3>
<p>Removed:</p><pre>
 public abstract class MCSessionDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class MCSessionDelegate : MonoTouch.Foundation.NSObject, IMCSessionDelegate {
</pre>
<h3>New Type: MonoTouch.MultipeerConnectivity.MCSessionDelegate_Extensions</h3>
<pre>
public static class MCSessionDelegate_Extensions {
	
	public static bool DidReceiveCertificate (IMCSessionDelegate This, MCSession session, MonoTouch.Security.SecCertificate[] certificate, MCPeerID peerID, Action<bool> certificateHandler);
}
</bool></pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>New Type: MonoTouch.ObjCRuntime.BlockProxyAttribute</h3>
<pre>
public class BlockProxyAttribute : Attribute {
	
	public BlockProxyAttribute (Type t);
	
	public Type Type {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Removed:</p><pre>
 	public static bool bool_objc_msgSend_CMTime_out_CGAffineTransform_out_CGAffineTransform_out_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreGraphics.CGAffineTransform arg2, out MonoTouch.CoreGraphics.CGAffineTransform arg3, out MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_CMTime_out_Single_out_Single_out_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out float arg2, out float arg3, out MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_IntPtr_out_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, out bool arg2);
 	public static bool bool_objc_msgSendSuper_CMTime_out_CGAffineTransform_out_CGAffineTransform_out_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreGraphics.CGAffineTransform arg2, out MonoTouch.CoreGraphics.CGAffineTransform arg3, out MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_out_Single_out_Single_out_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out float arg2, out float arg3, out MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_out_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, out bool arg2);
 	public static IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_out_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, out MonoTouch.Foundation.NSRange arg3, out MonoTouch.Foundation.NSRange arg4);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_out_NSRange_out_NSRange_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, out MonoTouch.Foundation.NSRange arg3, out MonoTouch.Foundation.NSRange arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_out_NSPropertyListFormat_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, out MonoTouch.Foundation.NSPropertyListFormat arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, out MonoTouch.CoreMedia.CMTime arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_out_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, out MonoTouch.Foundation.NSRange arg3, out MonoTouch.Foundation.NSRange arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_out_NSRange_out_NSRange_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, out MonoTouch.Foundation.NSRange arg3, out MonoTouch.Foundation.NSRange arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_out_NSPropertyListFormat_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, out MonoTouch.Foundation.NSPropertyListFormat arg3, IntPtr arg4);
 	public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_float_out_Single_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, out float arg3, float arg4, int arg5);
 	public static System.Drawing.SizeF SizeF_objc_msgSend_PointF_float_IntPtr_float_out_Single_int_int (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, out float arg5, int arg6, int arg7);
 	public static void SizeF_objc_msgSend_stret_IntPtr_float_out_Single_float_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, out float arg3, float arg4, int arg5);
 	public static void SizeF_objc_msgSend_stret_PointF_float_IntPtr_float_out_Single_int_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, out float arg5, int arg6, int arg7);
 	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_float_out_Single_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, out float arg3, float arg4, int arg5);
 	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_PointF_float_IntPtr_float_out_Single_int_int (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, out float arg5, int arg6, int arg7);
 	public static void SizeF_objc_msgSendSuper_stret_IntPtr_float_out_Single_float_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, out float arg3, float arg4, int arg5);
 	public static void SizeF_objc_msgSendSuper_stret_PointF_float_IntPtr_float_out_Single_int_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, out float arg5, int arg6, int arg7);
 	public static ushort UInt16_objc_msgSend_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
 	public static ushort UInt16_objc_msgSendSuper_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
 	public static uint UInt32_objc_msgSend_PointF_IntPtr_out_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, out float arg3);
 	public static uint UInt32_objc_msgSendSuper_PointF_IntPtr_out_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, out float arg3);
 	public static void void_objc_msgSend_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_IntPtr_PointF_out_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, out System.Drawing.PointF arg3);
 	public static void void_objc_msgSend_out_UInt32_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1, out uint arg2);
 	public static void void_objc_msgSendSuper_IntPtr_out_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, out System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_PointF_out_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, out System.Drawing.PointF arg3);
 	public static void void_objc_msgSendSuper_out_UInt32_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1, out uint arg2);
</pre>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_CMTime_ref_CGAffineTransform_ref_CGAffineTransform_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref MonoTouch.CoreGraphics.CGAffineTransform arg2, ref MonoTouch.CoreGraphics.CGAffineTransform arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_CMTime_ref_RectangleF_ref_RectangleF_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref System.Drawing.RectangleF arg2, ref System.Drawing.RectangleF arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_CMTime_ref_Single_ref_Single_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref float arg2, ref float arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_IntPtr_ref_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, ref bool arg2);
 	public static bool bool_objc_msgSend_out_Single_out_Single (IntPtr receiver, IntPtr selector, out float arg1, out float arg2);
 	public static bool bool_objc_msgSendSuper_CMTime_ref_CGAffineTransform_ref_CGAffineTransform_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref MonoTouch.CoreGraphics.CGAffineTransform arg2, ref MonoTouch.CoreGraphics.CGAffineTransform arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_ref_RectangleF_ref_RectangleF_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref System.Drawing.RectangleF arg2, ref System.Drawing.RectangleF arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_ref_Single_ref_Single_ref_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref float arg2, ref float arg3, ref MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_ref_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, ref bool arg2);
 	public static bool bool_objc_msgSendSuper_out_Single_out_Single (IntPtr receiver, IntPtr selector, out float arg1, out float arg2);
 	public static IntPtr IntPtr_objc_msgSend_CMTime_ref_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref MonoTouch.CoreMedia.CMTime arg2);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSend_int_ref_NSRange (IntPtr receiver, IntPtr selector, int arg1, ref MonoTouch.Foundation.NSRange arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_NSPropertyListFormat_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, ref MonoTouch.Foundation.NSPropertyListFormat arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSend_UInt64_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CMTime_ref_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, ref MonoTouch.CoreMedia.CMTime arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, ref MonoTouch.Foundation.NSRange arg3, ref MonoTouch.Foundation.NSRange arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_ref_NSRange (IntPtr receiver, IntPtr selector, int arg1, ref MonoTouch.Foundation.NSRange arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_NSPropertyListFormat_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, ref MonoTouch.Foundation.NSPropertyListFormat arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_UInt64_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, IntPtr arg2);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_NSRange_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSend_stret_NSRange_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_NSRange_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static void NSRange_objc_msgSendSuper_stret_NSRange_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSRange arg1, IntPtr arg2);
 	public static void RectangleF_objc_msgSend_stret_UInt32_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static void RectangleF_objc_msgSendSuper_stret_UInt32_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_float_ref_Single_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, ref float arg3, float arg4, int arg5);
 	public static System.Drawing.SizeF SizeF_objc_msgSend_PointF_float_IntPtr_float_ref_Single_int_int (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, ref float arg5, int arg6, int arg7);
 	public static void SizeF_objc_msgSend_stret_IntPtr_float_ref_Single_float_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, ref float arg3, float arg4, int arg5);
 	public static void SizeF_objc_msgSend_stret_PointF_float_IntPtr_float_ref_Single_int_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, ref float arg5, int arg6, int arg7);
 	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_float_ref_Single_float_int (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, ref float arg3, float arg4, int arg5);
 	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_PointF_float_IntPtr_float_ref_Single_int_int (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, ref float arg5, int arg6, int arg7);
 	public static void SizeF_objc_msgSendSuper_stret_IntPtr_float_ref_Single_float_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, ref float arg3, float arg4, int arg5);
 	public static void SizeF_objc_msgSendSuper_stret_PointF_float_IntPtr_float_ref_Single_int_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, IntPtr arg3, float arg4, ref float arg5, int arg6, int arg7);
 	public static ushort UInt16_objc_msgSend_UInt32_ref_Boolean (IntPtr receiver, IntPtr selector, uint arg1, ref bool arg2);
 	public static ushort UInt16_objc_msgSendSuper_UInt32_ref_Boolean (IntPtr receiver, IntPtr selector, uint arg1, ref bool arg2);
 	public static uint UInt32_objc_msgSend_PointF_IntPtr_ref_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, ref float arg3);
 	public static uint UInt32_objc_msgSendSuper_PointF_IntPtr_ref_Single (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2, ref float arg3);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_CMTime (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, MonoTouch.CoreMedia.CMTime arg4);
 	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, double arg5, IntPtr arg6);
 	public static void void_objc_msgSend_IntPtr_IntPtr_UInt32_IntPtr_CGAffineTransform_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, IntPtr arg4, MonoTouch.CoreGraphics.CGAffineTransform arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSend_IntPtr_PointF_ref_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, ref System.Drawing.PointF arg3);
 	public static void void_objc_msgSend_IntPtr_ref_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_RectangleF_CMTime (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSend_RectangleF_RectangleF_CMTimeRange (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSend_ref_UInt32_ref_UInt32 (IntPtr receiver, IntPtr selector, ref uint arg1, ref uint arg2);
 	public static void void_objc_msgSend_UInt64_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, IntPtr arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_CMTime (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, MonoTouch.CoreMedia.CMTime arg4);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, double arg5, IntPtr arg6);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_UInt32_IntPtr_CGAffineTransform_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, uint arg3, IntPtr arg4, MonoTouch.CoreGraphics.CGAffineTransform arg5, IntPtr arg6, IntPtr arg7);
 	public static void void_objc_msgSendSuper_IntPtr_PointF_ref_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, ref System.Drawing.PointF arg3);
 	public static void void_objc_msgSendSuper_IntPtr_ref_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_RectangleF_CMTime (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.CoreMedia.CMTime arg2);
 	public static void void_objc_msgSendSuper_RectangleF_RectangleF_CMTimeRange (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, MonoTouch.CoreMedia.CMTimeRange arg3);
 	public static void void_objc_msgSendSuper_ref_UInt32_ref_UInt32 (IntPtr receiver, IntPtr selector, ref uint arg1, ref uint arg2);
 	public static void void_objc_msgSendSuper_UInt64_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, IntPtr arg2, IntPtr arg3);
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Runtime</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSObject GetNSObject (IntPtr ptr);
</pre>
<p>Added:</p><pre>
 	public static Delegate CreateBlockProxy (System.Reflection.MethodInfo method, IntPtr block);
 	public static System.Reflection.MethodInfo GetBlockWrapperCreator (System.Reflection.MethodInfo method, int parameter);
 	public static Delegate GetDelegateForBlock (IntPtr methodPtr, Type type);
 	public static MonoTouch.Foundation.NSObject GetNSObject (IntPtr ptr);
</pre>
<h2>Namespace: MonoTouch.SafariServices</h2>
<h3>Type Changed: MonoTouch.SafariServices.SSReadingList</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString ErrorDomain {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.SafariServices.SSReadingListError</h3>
<pre>
[Serializable]
public enum SSReadingListError {
	UrlSchemeNotAllowed
}
</pre>
<h2>Namespace: MonoTouch.Security</h2>
<h3>Type Changed: MonoTouch.Security.SecKey</h3>
<p>Added:</p><pre>
 	public SecStatusCode Encrypt (SecPadding padding, byte [] plainText, out byte [] cipherText);
 	public int BlockSize {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.Social</h2>
<h3>Type Changed: MonoTouch.Social.SLServiceKind</h3>
<p>Removed:</p><pre>
 	TencentWeibo,
 	LinkedIn
</pre>
<p>Added:</p><pre>
 	TencentWeibo
</pre>
<h3>Type Changed: MonoTouch.Social.SLServiceType</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString LinkedIn {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.SpriteKit</h2>
<h3>Type Changed: MonoTouch.SpriteKit.SKAction</h3>
<p>Removed:</p><pre>
 	public SKAction ();
 	public static SKAction AnimateWithTextures (MonoTouch.Foundation.NSObject[] textures, double sec);
 	public static SKAction AnimateWithTextures (MonoTouch.Foundation.NSObject[] textures, double sec, bool resize, bool restore);
 	public static SKAction Group (MonoTouch.Foundation.NSObject[] actions);
 	public static SKAction ResizeToWidth (float width, float height, double duration);
 	public static SKAction RunBlock (Action block, MonoTouch.Foundation.NSObject queue);
 	public static SKAction Sequence (MonoTouch.Foundation.NSObject[] actions);
</pre>
<p>Added:</p><pre>
 	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec);
 	public static SKAction AnimateWithTextures (SKTexture[] textures, double sec, bool resize, bool restore);
 	public static SKAction Group (params SKAction[] actions);
 	public static SKAction ResizeTo (float width, float height, double duration);
 	public static SKAction ResizeTo (System.Drawing.SizeF size, double duration);
 	public static SKAction RunBlock (Action block, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public static SKAction Sequence (params SKAction[] actions);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKKeyframeSequence</h3>
<p>Removed:</p><pre>
 	public SKKeyframeSequence (MonoTouch.Foundation.NSObject[] values, MonoTouch.Foundation.NSObject[] times);
 	public virtual float GetKeyframeTimeForIndex (uint index);
 	public virtual MonoTouch.Foundation.NSObject GetKeyframeValueForIndex (uint index);
 	public virtual void RemoveKeyframeAtIndex (uint index);
</pre>
<p>Added:</p><pre>
 	public SKKeyframeSequence (MonoTouch.Foundation.NSObject[] values, MonoTouch.Foundation.NSNumber[] times);
 	public SKKeyframeSequence (MonoTouch.Foundation.NSObject[] values, float [] times);
 	public SKKeyframeSequence (MonoTouch.Foundation.NSObject[] values, double [] times);
 	public virtual float GetKeyframeTime (uint index);
 	public virtual MonoTouch.Foundation.NSObject GetKeyframeValue (uint index);
 	public virtual void RemoveKeyframe (uint index);
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsBody</h3>
<p>Removed:</p><pre>
 	public SKPhysicsBody ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsContact</h3>
<p>Removed:</p><pre>
 	public SKPhysicsContact ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointFixed</h3>
<p>Removed:</p><pre>
 	public SKPhysicsJointFixed ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointLimit</h3>
<p>Removed:</p><pre>
 	public SKPhysicsJointLimit ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointPin</h3>
<p>Removed:</p><pre>
 	public SKPhysicsJointPin ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointSliding</h3>
<p>Removed:</p><pre>
 	public SKPhysicsJointSliding ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsJointSpring</h3>
<p>Removed:</p><pre>
 	public SKPhysicsJointSpring ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKPhysicsWorld</h3>
<p>Removed:</p><pre>
 	public SKPhysicsWorld ();
 	public virtual System.Drawing.PointF Gravity {
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.CoreGraphics.CGVector Gravity {
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKTexture</h3>
<p>Removed:</p><pre>
 	public SKTexture ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKTextureAtlas</h3>
<p>Removed:</p><pre>
 	public static void PreloadTextures (SKTexture[] textures, MonoTouch.Foundation.NSAction completion);
 	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTexture[] textures);
 	protected override void Dispose (bool disposing);
 	public virtual MonoTouch.Foundation.NSObject[] TextureNames {
</pre>
<p>Added:</p><pre>
 	public static void PreloadTextures (SKTextureAtlas[] textures, MonoTouch.Foundation.NSAction completion);
 	public static System.Threading.Tasks.Task PreloadTexturesAsync (SKTextureAtlas[] textures);
 	public virtual string [] TextureNames {
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKTransition</h3>
<p>Removed:</p><pre>
 	public SKTransition ();
</pre>
<h3>Type Changed: MonoTouch.SpriteKit.SKVideoNode</h3>
<p>Added:</p><pre>
 	public SKVideoNode (MonoTouch.AVFoundation.AVPlayer player);
 	public static SKVideoNode FromPlayer (MonoTouch.AVFoundation.AVPlayer player);
</pre>
<h2>Namespace: MonoTouch.StoreKit</h2>
<h3>New Type: MonoTouch.StoreKit.SKReceiptProperties</h3>
<pre>
public class SKReceiptProperties : MonoTouch.Foundation.DictionaryContainer {
	
	public SKReceiptProperties ();
	public SKReceiptProperties (MonoTouch.Foundation.NSDictionary dictionary);
	
	public bool IsExpired {
		get;
		set;
	}
	public bool IsRevoked {
		get;
		set;
	}
	public bool IsVolumePurchase {
		get;
		set;
	}
}
</pre>
<h3>Type Removed: MonoTouch.StoreKit.SKReceiptProperty</h3>
<h3>Type Changed: MonoTouch.StoreKit.SKReceiptRefreshRequest</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.Foundation.NSDictionary ReceiptProperties {
</pre>
<p>Added:</p><pre>
 	public SKReceiptRefreshRequest (SKReceiptProperties receiptProperties);
 	public SKReceiptProperties ReceiptProperties {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary WeakReceiptProperties {
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>New Type: MonoTouch.UIKit.INSLayoutManagerDelegate</h3>
<pre>
public interface INSLayoutManagerDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIBarPositioning</h3>
<pre>
public interface IUIBarPositioning : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIGuidedAccessRestriction</h3>
<pre>
public interface IUIGuidedAccessRestriction : MonoTouch.ObjCRuntime.INativeObject {
	
	string GetDetailTextForGuidedAccessRestriction (string restrictionIdentifier);
	string GetTextForGuidedAccessRestriction (string restrictionIdentifier);
	void GuidedAccessRestrictionChangedState (string restrictionIdentifier, UIGuidedAccessRestrictionState newRestrictionState);
	
	string [] GetGuidedAccessRestrictionIdentifiers {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIPercentDrivenInteractiveTransition</h3>
<pre>
public interface IUIPercentDrivenInteractiveTransition : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerAnimatedTransitioning</h3>
<pre>
public interface IUIViewControllerAnimatedTransitioning : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void AnimateTransition (IUIViewControllerContextTransitioning transitionContext);
	double TransitionDuration (IUIViewControllerContextTransitioning transitionContext);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerContextTransitioning</h3>
<pre>
public interface IUIViewControllerContextTransitioning : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void CancelInteractiveTransition ();
	void CompleteTransition (bool didComplete);
	void FinishInteractiveTransition ();
	System.Drawing.RectangleF GetFinalFrameForViewController (UIViewController vc);
	System.Drawing.RectangleF GetInitialFrameForViewController (UIViewController vc);
	UIViewController GetViewControllerForKey (MonoTouch.Foundation.NSString uiTransitionKey);
	void UpdateInteractiveTransition (float percentComplete);
	
	UIView ContainerView {
		get;
	}
	bool IsAnimated {
		get;
	}
	bool IsInteractive {
		get;
	}
	UIModalPresentationStyle PresentationStyle {
		get;
	}
	bool TransitionWasCancelled {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerInteractiveTransitioning</h3>
<pre>
public interface IUIViewControllerInteractiveTransitioning : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	void StartInteractiveTransition (IUIViewControllerContextTransitioning transitionContext);
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerTransitionCoordinator</h3>
<pre>
public interface IUIViewControllerTransitionCoordinator : IDisposable, MonoTouch.ObjCRuntime.INativeObject, IUIViewControllerTransitionCoordinatorContext {
	
	bool AnimateAlongsideTransition (Action<iuiviewcontrollertransitioncoordinatorcontext> animate, Action<iuiviewcontrollertransitioncoordinatorcontext> completion);
	bool AnimateAlongsideTransitionInView (UIView view, Action<iuiviewcontrollertransitioncoordinatorcontext> animation, Action<iuiviewcontrollertransitioncoordinatorcontext> completion);
	void NotifyWhenInteractionEndsUsingBlock (Action<iuiviewcontrollertransitioncoordinatorcontext> handler);
}
</iuiviewcontrollertransitioncoordinatorcontext></iuiviewcontrollertransitioncoordinatorcontext></iuiviewcontrollertransitioncoordinatorcontext></iuiviewcontrollertransitioncoordinatorcontext></iuiviewcontrollertransitioncoordinatorcontext></pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerTransitionCoordinatorContext</h3>
<pre>
public interface IUIViewControllerTransitionCoordinatorContext : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	UIViewController GetViewControllerForKey (MonoTouch.Foundation.NSString uiTransitionKey);
	
	UIViewAnimationCurve CompletionCurve {
		get;
	}
	float CompletionVelocity {
		get;
	}
	UIView ContainerView {
		get;
	}
	bool InitiallyInteractive {
		get;
	}
	bool IsAnimated {
		get;
	}
	bool IsCancelled {
		get;
	}
	bool IsInteractive {
		get;
	}
	float PercentComplete {
		get;
	}
	UIModalPresentationStyle PresentationStyle {
		get;
	}
	double TransitionDuration {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.IUIViewControllerTransitioningDelegate</h3>
<pre>
public interface IUIViewControllerTransitioningDelegate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSLayoutManager</h3>
<p>Removed:</p><pre>
 	public virtual uint GetGlyphs (MonoTouch.Foundation.NSRange glyphRange, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexBuffer, IntPtr bidiLevelBuffer);
 	public virtual void SetTextContainerForRange (NSTextContainer container, MonoTouch.Foundation.NSRange glyphRange);
</pre>
<p>Added:</p><pre>
 	public MonoTouch.Foundation.NSRange CharacterRangeForGlyphRange (MonoTouch.Foundation.NSRange charRange);
 	public MonoTouch.Foundation.NSRange CharacterRangeForGlyphRange (MonoTouch.Foundation.NSRange charRange, ref MonoTouch.Foundation.NSRange actualCharRange);
 	public virtual MonoTouch.Foundation.NSRange CharacterRangeForGlyphRangeInternal (MonoTouch.Foundation.NSRange glyphRange, IntPtr actualGlyphRange);
 	public uint GetGlyphs (MonoTouch.Foundation.NSRange glyphRange, short [] glyphBuffer, NSGlyphProperty[] props, uint [] charIndexBuffer, byte [] bidiLevelBuffer);
 	public MonoTouch.Foundation.NSRange GlyphRangeForCharacterRange (MonoTouch.Foundation.NSRange charRange);
 	public MonoTouch.Foundation.NSRange GlyphRangeForCharacterRange (MonoTouch.Foundation.NSRange charRange, ref MonoTouch.Foundation.NSRange actualCharRange);
 	public System.Drawing.RectangleF LineFragmentRectForGlyphAtIndex (uint glyphIndex);
 	public System.Drawing.RectangleF LineFragmentRectForGlyphAtIndex (uint glyphIndex, ref MonoTouch.Foundation.NSRange effectiveGlyphRange);
 	public System.Drawing.RectangleF LineFragmentUsedRectForGlyphAtIndex (uint glyphIndex);
 	public System.Drawing.RectangleF LineFragmentUsedRectForGlyphAtIndex (uint glyphIndex, ref MonoTouch.Foundation.NSRange effectiveGlyphRange);
 	public virtual void SetTextContainer (NSTextContainer container, MonoTouch.Foundation.NSRange glyphRange);
 	public void ShowCGGlyphs (short [] glyphs, System.Drawing.PointF [] positions, uint glyphCount, UIFont font, MonoTouch.CoreGraphics.CGAffineTransform textMatrix, MonoTouch.Foundation.NSDictionary attributes, MonoTouch.CoreGraphics.CGContext graphicsContext);
 	public NSTextContainer TextContainerForGlyphAtIndex (uint glyphIndex);
 	public NSTextContainer TextContainerForGlyphAtIndex (uint glyphIndex, ref MonoTouch.Foundation.NSRange effectiveGlyphRange);
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSLayoutManagerDelegate</h3>
<p>Removed:</p><pre>
 public class NSLayoutManagerDelegate : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class NSLayoutManagerDelegate : MonoTouch.Foundation.NSObject, INSLayoutManagerDelegate {
</pre>
<h3>New Type: MonoTouch.UIKit.NSLayoutManagerDelegate_Extensions</h3>
<pre>
public static class NSLayoutManagerDelegate_Extensions {
	
	public static System.Drawing.RectangleF BoundingBoxForControlGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, System.Drawing.RectangleF proposedRect, System.Drawing.PointF glyphPosition, uint charIndex);
	public static void DidChangeGeometry (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, float oldSize);
	public static void DidCompleteLayout (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, bool layoutFinishedFlag);
	public static void DidInvalidatedLayout (INSLayoutManagerDelegate This, NSLayoutManager sender);
	public static float LineSpacingAfterGlyphAtIndex (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static float ParagraphSpacingAfterGlyphAtIndex (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static float ParagraphSpacingBeforeGlyphAtIndex (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static bool ShouldBreakLineByHyphenatingBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static bool ShouldBreakLineByWordBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static uint ShouldGenerateGlyphs (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, UIFont aFont, MonoTouch.Foundation.NSRange glyphRange);
	public static NSControlCharacterAction ShouldUseAction (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.NSTextAttachment</h3>
<p>Added:</p><pre>
 	public virtual MonoTouch.Foundation.NSFileWrapper FileWrapper {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.TransitionCoordinator_UIViewController</h3>
<p>Removed:</p><pre>
 	public static UIViewControllerTransitionCoordinator GetTransitionCoordinator (UIViewController This);
</pre>
<p>Added:</p><pre>
 	public static IUIViewControllerTransitionCoordinator GetTransitionCoordinator (UIViewController This);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAccessibility</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;bool&gt; RequestGuidedAccessSessionAsync (bool enable);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAttachmentBehavior</h3>
<p>Removed:</p><pre>
 	public UIAttachmentBehavior (IUIDynamicItem item, MonoTouch.Foundation.NSObject attachedToItem);
 	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offsetFromCenter, MonoTouch.Foundation.NSObject attachedToItem, UIOffset attachOffsetFromCenter);
</pre>
<p>Added:</p><pre>
 	public UIAttachmentBehavior (IUIDynamicItem item, IUIDynamicItem attachedToItem);
 	public UIAttachmentBehavior (IUIDynamicItem item, UIOffset offsetFromCenter, IUIDynamicItem attachedToItem, UIOffset attachOffsetFromCenter);
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioning</h3>
<pre>
public class UIBarPositioning : MonoTouch.Foundation.NSObject, IUIBarPositioning {
	
	public UIBarPositioning ();
	public UIBarPositioning (MonoTouch.Foundation.NSCoder coder);
	public UIBarPositioning (MonoTouch.Foundation.NSObjectFlag t);
	public UIBarPositioning (IntPtr handle);
	
	public virtual UIBarPosition BarPosition {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarPositioningDelegate</h3>
<p>Removed:</p><pre>
 	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 	public virtual UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIBarPositioningDelegate_Extensions</h3>
<p>Removed:</p><pre>
 	public static UIBarPosition GetPositionForBar (IUIBarPositioningDelegate This, MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 	public static UIBarPosition GetPositionForBar (IUIBarPositioningDelegate This, IUIBarPositioning barPositioning);
</pre>
<h3>New Type: MonoTouch.UIKit.UIBarPositioning_Extensions</h3>
<pre>
public static class UIBarPositioning_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIButton</h3>
<p>Removed:</p><pre>
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionView</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SetCollectionViewLayoutAsync (UICollectionViewLayout layout, bool animated);
 	public virtual System.Threading.Tasks.Task&lt;UICollectionViewTransitionResult&gt; StartInteractiveTransitionAsync (UICollectionViewLayout newCollectionViewLayout);
 	public virtual System.Threading.Tasks.Task&lt;UICollectionViewTransitionResult&gt; StartInteractiveTransitionAsync (UICollectionViewLayout newCollectionViewLayout, out UICollectionViewTransitionLayout result);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutInteractiveTransitionCompletion</h3>
<p>Removed:</p><pre>
 public delegate void UICollectionViewLayoutInteractiveTransitionCompletion (bool completed, bool finish);
</pre>
<p>Added:</p><pre>
 public delegate void UICollectionViewLayoutInteractiveTransitionCompletion (bool completed, bool finished);
</pre>
<h3>New Type: MonoTouch.UIKit.UICollectionViewTransitionResult</h3>
<pre>
public class UICollectionViewTransitionResult {
	
	public UICollectionViewTransitionResult (bool completed, bool finished);
	
	public bool Completed {
		get;
		set;
	}
	public bool Finished {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollisionBehavior</h3>
<p>Removed:</p><pre>
 	public UICollisionBehavior (IUIDynamicItem[] items);
</pre>
<p>Added:</p><pre>
 	public UICollisionBehavior (params IUIDynamicItem[] items);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIColor</h3>
<p>Added:</p><pre>
 	public virtual bool GetWhite (out float white, out float alpha);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIContentSizeCategoryChangedEventArgs</h3>
<p>Removed:</p><pre>
 	public MonoTouch.Foundation.NSString NewValue {
</pre>
<p>Added:</p><pre>
 	public UIContentSizeCategory NewValue {
 		get;
 	}
 	public MonoTouch.Foundation.NSString WeakNewValue {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicAnimator</h3>
<p>Removed:</p><pre>
 public class UIDynamicAnimator : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public class UIDynamicAnimator : MonoTouch.Foundation.NSObject, System.Collections.IEnumerable {
 	public void Add (UIDynamicBehavior behavior);
 	public void AddBehaviors (params UIDynamicBehavior[] behaviors);
 	public void RemoveBehaviors (params UIDynamicBehavior[] behaviors);
 	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicItem</h3>
<p>Removed:</p><pre>
 [Obsolete]
public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject, IUIDynamicItem {
</pre>
<p>Added:</p><pre>
 public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject, IUIDynamicItem {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDynamicItemBehavior</h3>
<p>Removed:</p><pre>
 	public UIDynamicItemBehavior (IUIDynamicItem[] items);
</pre>
<p>Added:</p><pre>
 	public UIDynamicItemBehavior (params IUIDynamicItem[] items);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIEdgeInsets</h3>
<p>Added:</p><pre>
 	public static UIEdgeInsets FromString (string s);
 	public override bool Equals (object obj);
 	public bool Equals (UIEdgeInsets other);
 	public override int GetHashCode ();
 	public System.Drawing.RectangleF InsetRect (System.Drawing.RectangleF rect);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFont</h3>
<p>Removed:</p><pre>
 	public static UIFont PreferredFontForTextStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	public static UIFont PreferredFontForTextStyle (UIFontTextStyle textStyle);
 	public virtual UIFontDescriptor GetFontDescriptor ();
</pre>
<p>Added:</p><pre>
 	public static UIFont GetPreferredFontForTextStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	protected override void Dispose (bool disposing);
 	public static UIFont PreferredBody {
 		get;
 	}
 	public static UIFont PreferredCaption1 {
 		get;
 	}
 	public static UIFont PreferredCaption2 {
 		get;
 	}
 	public static UIFont PreferredFootnote {
 		get;
 	}
 	public static UIFont PreferredHeadline {
 		get;
 	}
 	public static UIFont PreferredSubheadline {
 		get;
 	}
 	public virtual UIFontDescriptor FontDescriptor {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontAttributes</h3>
<p>Removed:</p><pre>
 	public string SizeString {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public UIFontAttributes (params UIFontFeature[] features);
 	public UIFontFeature[] FeatureSettings {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIFontDescriptor</h3>
<p>Removed:</p><pre>
 	public static UIFontDescriptor PreferredForStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	public static UIFontDescriptor PreferredForStyle (UIFontTextStyle style);
 	public virtual UIFontDescriptor[] GetMatchingFontDescriptorsWithMandatoryKeys (MonoTouch.Foundation.NSSet mandatoryKeys);
 	public static MonoTouch.Foundation.NSString TextStyleBody {
 	public static MonoTouch.Foundation.NSString TextStyleCaption1 {
 	public static MonoTouch.Foundation.NSString TextStyleCaption2 {
 	public static MonoTouch.Foundation.NSString TextStyleFootnote {
 	public static MonoTouch.Foundation.NSString TextStyleHeadline {
 	public static MonoTouch.Foundation.NSString TextStyleSubheadline {
</pre>
<p>Added:</p><pre>
 	public static UIFontDescriptor GetPreferredDescriptorForTextStyle (MonoTouch.Foundation.NSString uiFontTextStyle);
 	public virtual UIFontDescriptor[] GetMatchingFontDescriptors (MonoTouch.Foundation.NSSet mandatoryKeys);
 	public UIFontDescriptor[] GetMatchingFontDescriptors (params UIFontDescriptorAttribute[] mandatoryKeys);
 	public static UIFontDescriptor PreferredBody {
 	public static UIFontDescriptor PreferredCaption1 {
 	public static UIFontDescriptor PreferredCaption2 {
 	public static UIFontDescriptor PreferredFootnote {
 	public static UIFontDescriptor PreferredHeadline {
 	public static UIFontDescriptor PreferredSubheadline {
 		get;
 	}
 	public UIFontDescriptor[] CascadeList {
 		get;
 	}
 	public MonoTouch.Foundation.NSCharacterSet CharacterSet {
 	public string Face {
 		get;
 	}
 	public string Family {
 		get;
 	}
 	public UIFontFeature[] FeatureSettings {
 		get;
 	}
 	public Nullable&lt;float&gt; FixedAdvance {
 		get;
 	}
 	public string Name {
 		get;
 	}
 	public Nullable&lt;float&gt; Size {
 		get;
 	}
 	public MonoTouch.Foundation.NSString TextStyle {
 		get;
 	}
 	public UIFontTraits Traits {
 		get;
 	}
 	public MonoTouch.Foundation.NSDictionary Variation {
 		get;
 	}
 	public string VisibleName {
 		get;
 	}
 	public MonoTouch.Foundation.NSDictionary[] WeakFeatureSettings {
 		get;
 	}
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontDescriptorAttribute</h3>
<pre>
[Serializable]
public enum UIFontDescriptorAttribute {
	Family,
	Face,
	Name,
	Size,
	VisibleName,
	Matrix,
	CharacterSet,
	CascadeList,
	Traits,
	FixedAdvance,
	FeatureSettings,
	TextStyle
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIFontFeature</h3>
<pre>
public class UIFontFeature : MonoTouch.ObjCRuntime.INativeObject {
	
	public UIFontFeature (CTFontFeatureAllTypographicFeatures.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureLigatures.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCursiveConnection.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureLetterCase.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureVerticalSubstitutionConnection.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureLinguisticRearrangementConnection.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureNumberSpacing.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureSmartSwash.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureDiacritics.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureVerticalPosition.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureFractions.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureOverlappingCharacters.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureTypographicExtras.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureMathematicalExtras.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureOrnamentSets.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCharacterAlternatives.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (int characterAlternatives);
	public UIFontFeature (CTFontFeatureDesignComplexity.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureStyleOptions.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCharacterShape.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureNumberCase.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureTextSpacing.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureTransliteration.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureAnnotation.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureKanaSpacing.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureIdeographicSpacing.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureUnicodeDecomposition.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureRubyKana.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCJKSymbolAlternatives.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureIdeographicAlternatives.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCJKVerticalRomanPlacement.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureItalicCJKRoman.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCaseSensitiveLayout.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureAlternateKana.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureStylisticAlternatives.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureContextualAlternates.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureLowerCase.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureUpperCase.MonoTouch.CoreText.Selector featureSelector);
	public UIFontFeature (CTFontFeatureCJKRomanSpacing.MonoTouch.CoreText.Selector featureSelector);
	
	public override string ToString ();
	
	public MonoTouch.CoreText.FontFeatureGroup FontFeature {
		get;
	}
	public object FontFeatureValue {
		get;
	}
	private IntPtr MonoTouch.ObjCRuntime.INativeObject.Handle {
		get;
	}
}
</pre>
<h3>Type Removed: MonoTouch.UIKit.UIFontTextStyle</h3>
<h3>Type Changed: MonoTouch.UIKit.UIGravityBehavior</h3>
<p>Removed:</p><pre>
 	public UIGravityBehavior (IUIDynamicItem[] items);
</pre>
<p>Added:</p><pre>
 	public UIGravityBehavior (params IUIDynamicItem[] items);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerController</h3>
<p>Removed:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,IUIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 	public Func&lt;UINavigationController,IUIViewControllerAnimatedTransitioning,IUIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImagePickerControllerDelegate</h3>
<p>Removed:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public override IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIInterpolatingMotionEffect</h3>
<p>Added:</p><pre>
 	public UIInterpolatingMotionEffect (string keyPath, UIInterpolatingMotionEffectType type);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UILabel</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0")]
	public virtual float MinimumFontSize {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 6.0 in favor of MinimumScaleFactor")]
	public virtual float MinimumFontSize {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBar</h3>
<p>Removed:</p><pre>
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationBarDelegate</h3>
<p>Removed:</p><pre>
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 	public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate_Extensions</h3>
<p>Removed:</p><pre>
 	public static UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (IUINavigationControllerDelegate This, UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public static UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUINavigationControllerDelegate This, UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUINavigationControllerDelegate This, UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public static IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (IUINavigationControllerDelegate This, UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public static IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUINavigationControllerDelegate This, UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
 	public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUINavigationControllerDelegate This, UINavigationController navigationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Removed:</p><pre>
 	public Func&lt;UIPageViewController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public Func&lt;UIPageViewController,UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIPageViewController pageViewController);
</pre>
<p>Added:</p><pre>
 	public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UIPageViewController pageViewController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate_Extensions</h3>
<p>Removed:</p><pre>
 	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);
</pre>
<p>Added:</p><pre>
 	public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUIPageViewControllerDelegate This, UIPageViewController pageViewController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPercentDrivenInteractiveTransition</h3>
<p>Removed:</p><pre>
 public class UIPercentDrivenInteractiveTransition : MonoTouch.Foundation.NSObject {
 	public virtual void StartInteractiveTransition (UIViewControllerContextTransitioning transitionContext);
</pre>
<p>Added:</p><pre>
 public class UIPercentDrivenInteractiveTransition : MonoTouch.Foundation.NSObject, IUIPercentDrivenInteractiveTransition {
 	public virtual void StartInteractiveTransition (IUIViewControllerContextTransitioning transitionContext);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPercentDrivenInteractiveTransition_Extensions</h3>
<pre>
public static class UIPercentDrivenInteractiveTransition_Extensions {
	
	public static void CancelInteractiveTransition (IUIPercentDrivenInteractiveTransition This);
	public static void FinishInteractiveTransition (IUIPercentDrivenInteractiveTransition This);
	public static void StartInteractiveTransition (IUIPercentDrivenInteractiveTransition This, IUIViewControllerContextTransitioning transitionContext);
	public static void UpdateInteractiveTransition (IUIPercentDrivenInteractiveTransition This, float percentComplete);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPushBehavior</h3>
<p>Added:</p><pre>
 	public UIPushBehavior (UIPushBehaviorMode mode, params IUIDynamicItem[] items);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIRefreshControl</h3>
<p>Removed:</p><pre>
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBar</h3>
<p>Removed:</p><pre>
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public System.Func&lt;MonoTouch.Foundation.NSObject,UIBarPosition&gt; GetPositionForBar {
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<p>Added:</p><pre>
 	public Func&lt;IUIBarPositioning,UIBarPosition&gt; GetPositionForBar {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISearchBarDelegate</h3>
<p>Removed:</p><pre>
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 	public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISegmentedControl</h3>
<p>Removed:</p><pre>
 	protected override void Dispose (bool disposing);
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISimpleTextPrintFormatter</h3>
<p>Added:</p><pre>
 	public UISimpleTextPrintFormatter (MonoTouch.Foundation.NSAttributedString text);
 	public virtual MonoTouch.Foundation.NSAttributedString AttributedText {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStepper</h3>
<p>Removed:</p><pre>
 	protected override void Dispose (bool disposing);
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributeKey</h3>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString TextAlternatives {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIStringAttributes</h3>
<p>Removed:</p><pre>
 	public MonoTouch.Foundation.NSObject TextAlternativesObject {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UISwitch</h3>
<p>Removed:</p><pre>
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBar</h3>
<p>Removed:</p><pre>
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarController</h3>
<p>Removed:</p><pre>
 	public Func&lt;UITabBarController,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForTransition {
 	public Func&lt;UITabBarController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UITabBarController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<p>Added:</p><pre>
 	public Func&lt;UITabBarController,UIViewController,UIViewController,IUIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForTransition {
 	public Func&lt;UITabBarController,IUIViewControllerAnimatedTransitioning,IUIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UITabBarController,UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarControllerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UITabBarController tabBarController);
</pre>
<p>Added:</p><pre>
 	public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UITabBarController tabBarController, IUIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientationMask SupportedInterfaceOrientations (UITabBarController tabBarController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITabBarControllerDelegate_Extensions</h3>
<p>Removed:</p><pre>
 	public static UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public static UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
 	public static UIInterfaceOrientationMask GetSupportedInterfaceOrientations (IUITabBarControllerDelegate This, UITabBarController tabBarController);
</pre>
<p>Added:</p><pre>
 	public static IUIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (IUITabBarControllerDelegate This, UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public static IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (IUITabBarControllerDelegate This, UITabBarController tabBarController, IUIViewControllerAnimatedTransitioning animationController);
 	public static UIInterfaceOrientationMask SupportedInterfaceOrientations (IUITabBarControllerDelegate This, UITabBarController tabBarController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView</h3>
<p>Removed:</p><pre>
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbar</h3>
<p>Removed:</p><pre>
 	public virtual UIBarPosition BarPosition {
 		get;
 	}
 	public virtual UIColor TintColor {
 		get;
 		set;
 	}
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIToolbarDelegate</h3>
<p>Removed:</p><pre>
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<p>Added:</p><pre>
 	public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorController</h3>
<p>Removed:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,UIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 	public Func&lt;UINavigationController,UIViewControllerAnimatedTransitioning,UIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
</pre>
<p>Added:</p><pre>
 	public Func&lt;UINavigationController,UINavigationControllerOperation,UIViewController,UIViewController,IUIViewControllerAnimatedTransitioning&gt; GetAnimationControllerForOperation {
 	public Func&lt;UINavigationController,IUIViewControllerAnimatedTransitioning,IUIViewControllerInteractiveTransitioning&gt; GetInteractionControllerForAnimationController {
 	public Func&lt;UINavigationController,UIInterfaceOrientationMask&gt; SupportedInterfaceOrientations {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIVideoEditorControllerDelegate</h3>
<p>Removed:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<p>Added:</p><pre>
 	public override IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateAsync (double duration, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateKeyframesAsync (double duration, double delay, UIViewKeyframeAnimationOptions options, MonoTouch.Foundation.NSAction animations);
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateNotifyAsync (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations);
 	public static System.Threading.Tasks.Task&lt;bool&gt; PerformSystemAnimationAsync (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction parallelAnimations);
 		public virtual UIColor TintColor {
 			get;
 			set;
 		}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewControllerAnimatedTransitioning</h3>
<p>Removed:</p><pre>
 public abstract class UIViewControllerAnimatedTransitioning : MonoTouch.Foundation.NSObject {
 	public abstract void AnimateTransition (UIViewControllerContextTransitioning transitionContext);
 	public abstract double TransitionDuration (UIViewControllerContextTransitioning transitionContext);
</pre>
<p>Added:</p><pre>
 public abstract class UIViewControllerAnimatedTransitioning : MonoTouch.Foundation.NSObject, IUIViewControllerAnimatedTransitioning {
 	public abstract void AnimateTransition (IUIViewControllerContextTransitioning transitionContext);
 	public abstract double TransitionDuration (IUIViewControllerContextTransitioning transitionContext);
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerAnimatedTransitioning_Extensions</h3>
<pre>
public static class UIViewControllerAnimatedTransitioning_Extensions {
	
	public static void AnimationEnded (IUIViewControllerAnimatedTransitioning This, bool transitionCompleted);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewControllerContextTransitioning</h3>
<p>Removed:</p><pre>
 public abstract class UIViewControllerContextTransitioning : MonoTouch.Foundation.NSObject {
</pre>
<p>Added:</p><pre>
 public abstract class UIViewControllerContextTransitioning : MonoTouch.Foundation.NSObject, IUIViewControllerContextTransitioning {
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerContextTransitioning_Extensions</h3>
<pre>
public static class UIViewControllerContextTransitioning_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewControllerInteractiveTransitioning</h3>
<p>Removed:</p><pre>
 public abstract class UIViewControllerInteractiveTransitioning : MonoTouch.Foundation.NSObject {
 	public abstract void StartInteractiveTransition (UIViewControllerContextTransitioning transitionContext);
</pre>
<p>Added:</p><pre>
 public abstract class UIViewControllerInteractiveTransitioning : MonoTouch.Foundation.NSObject, IUIViewControllerInteractiveTransitioning {
 	public abstract void StartInteractiveTransition (IUIViewControllerContextTransitioning transitionContext);
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerInteractiveTransitioning_Extensions</h3>
<pre>
public static class UIViewControllerInteractiveTransitioning_Extensions {
}
</pre>
<h3>Type Removed: MonoTouch.UIKit.UIViewControllerTransitionCoordinator</h3>
<h3>Type Removed: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext</h3>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitionCoordinatorContext_Extensions</h3>
<pre>
public static class UIViewControllerTransitionCoordinatorContext_Extensions {
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitionCoordinator_Extensions</h3>
<pre>
public static class UIViewControllerTransitionCoordinator_Extensions {
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIViewControllerTransitioningDelegate</h3>
<p>Removed:</p><pre>
 public class UIViewControllerTransitioningDelegate : MonoTouch.Foundation.NSObject {
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForDismissedController (UIViewController dismissed);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForDismissal (UIViewControllerAnimatedTransitioning animator);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForPresentation (UIViewControllerAnimatedTransitioning animator);
 	public virtual UIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
</pre>
<p>Added:</p><pre>
 public class UIViewControllerTransitioningDelegate : MonoTouch.Foundation.NSObject, IUIViewControllerTransitioningDelegate {
 	public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForDismissedController (UIViewController dismissed);
 	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForDismissal (IUIViewControllerAnimatedTransitioning animator);
 	public virtual IUIViewControllerInteractiveTransitioning GetInteractionControllerForPresentation (IUIViewControllerAnimatedTransitioning animator);
 	public virtual IUIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
</pre>
<h3>New Type: MonoTouch.UIKit.UIViewControllerTransitioningDelegate_Extensions</h3>
<pre>
public static class UIViewControllerTransitioningDelegate_Extensions {
	
	public static IUIViewControllerAnimatedTransitioning GetAnimationControllerForDismissedController (IUIViewControllerTransitioningDelegate This, UIViewController dismissed);
	public static IUIViewControllerInteractiveTransitioning GetInteractionControllerForDismissal (IUIViewControllerTransitioningDelegate This, IUIViewControllerAnimatedTransitioning animator);
	public static IUIViewControllerInteractiveTransitioning GetInteractionControllerForPresentation (IUIViewControllerTransitioningDelegate This, IUIViewControllerAnimatedTransitioning animator);
	public static IUIViewControllerAnimatedTransitioning PresentingController (IUIViewControllerTransitioningDelegate This, UIViewController presented, UIViewController presenting, UIViewController source);
}
</pre>
<h3>Type Removed: MonoTouch.UIKit._UIContentSizeCategory</h3>
</body>
</html>
