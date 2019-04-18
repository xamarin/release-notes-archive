---
id: 254BECC9-F55E-4BDD-8C55-D175091430C0
title: "From 6.2.7 to 6.9.3"
---

<html><head><title>Comparison between monotouch-6.2.7.dll and monotouch-6.9.3.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.2.7";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.9.3";
 	public const string JavaScriptCoreLibrary = "/System/Library/Frameworks/JavaScriptCore.framework/JavaScriptCore";
 	public const string GameControllerLibrary = "/System/Library/Frameworks/GameController.framework/GameController";
 	public const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";
 	public const string SpriteKitLibrary = "/System/Library/Frameworks/SpriteKit.framework/SpriteKit";
 	public const string SafariServicesLibrary = "/System/Library/Frameworks/SafariServices.framework/SafariServices";
 	public const string MediaAccessibilityLibrary = "/System/Library/Frameworks/MediaAccessibility.framework/MediaAccessibility";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h3>
<p>Removed:</p><pre>
 	public virtual AVPlayerItemOutput Outputs {
</pre>
<p>Added:</p><pre>
 	public virtual AVPlayerItemOutput[] Outputs {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerItemVideoOutput</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
</pre>
<p>Added:</p><pre>
 	public MonoTouch.CoreVideo.CVPixelBuffer CopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
 	protected virtual IntPtr WeakCopyPixelBuffer (MonoTouch.CoreMedia.CMTime itemTime, ref MonoTouch.CoreMedia.CMTime outItemTimeForDisplay);
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
public class AVSpeechSynthesizerDelegate : MonoTouch.Foundation.NSObject {
	
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
<h2>Namespace: MonoTouch.Accounts</h2>
<h3>Type Changed: MonoTouch.Accounts.ACAccountStore</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;ACAccountCredentialRenewResult&gt; RenewCredentialsAsync (ACAccount account);
 	[Obsolete("Obsolete in iOS 6.0. Use overload with options instead")]
	public virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType);
 	public System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType, AccountStoreOptions options);
 	protected virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (ACAccountType accountType, MonoTouch.Foundation.NSDictionary options);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SaveAccountAsync (ACAccount account);
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
 	public void SetAddresses (ABMultiValue`1 addresses);
 	public void SetInstantMessages (ABMultiValue`1 value);
 	public void SetSocialProfile (ABMultiValue`1 value);
 	public static ABPersonCompositeNameFormat CompositeNameFormat {
</pre>
<p>Added:</p><pre>
 	public static string GetCompositeNameDelimiter (ABRecord record);
 	public static ABPersonCompositeNameFormat GetCompositeNameFormat (ABRecord record);
 	public void SetAddresses (ABMultiValue`1 addresses);
 	public void SetInstantMessages (ABMultiValue`1 value);
 	public void SetSocialProfile (ABMultiValue`1 value);
 	[Obsolete("Deprecated in iOS 7.0 in favor of GetCompositeNameFormat(null)")]
	public static ABPersonCompositeNameFormat CompositeNameFormat {
</pre>
<h2>Namespace: MonoTouch.AddressBookUI</h2>
<h3>Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate</h3>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (MonoTouch.UIKit.UINavigationController navigationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
</pre>
<h2>Namespace: MonoTouch.AssetsLibrary</h2>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAsset</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; SetImageDataAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; SetVideoAtPathAsync (MonoTouch.Foundation.NSUrl videoPathURL);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteModifiedImageToSavedToPhotosAlbumAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteModifiedVideoToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSUrl videoPathURL);
</pre>
<h3>Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.CoreGraphics.CGImage imageData, ALAssetOrientation orientation);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.CoreGraphics.CGImage imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteImageToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSData imageData, MonoTouch.Foundation.NSDictionary metadata);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSUrl&gt; WriteVideoToSavedPhotosAlbumAsync (MonoTouch.Foundation.NSUrl videoPathURL);
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
 	public static void AddListener (AudioSessionProperty property, PropertyListener listener);
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
	public static void AddListener (AudioSessionProperty property, PropertyListener listener);
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
<h3>Type Changed: MonoTouch.AudioToolbox.AudioStreamBasicDescription</h3>
<p>Removed:</p><pre>
 	public const double AudioStreamAnyRate = 0;
</pre>
<p>Added:</p><pre>
 	public const double AudioStreamAnyRate = 0;
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
 	public void ConnectPeripheral (CBPeripheral peripheral, PeripheralConnectionOptions options);
 	[Obsolete("Deprecated in iOS7")]
	public virtual void RetrieveConnectedPeripherals ();
 	public virtual CBPeripheral[] RetrieveConnectedPeripherals (CBUUID[] serviceUUIDs);
 	[Obsolete("Deprecated in iOS7")]
	public void RetrievePeripherals (CBUUID[] peripheralUuids);
 	public virtual CBPeripheral[] RetrievePeripheralsWithIdentifiers (CBUUID[] identifiers);
 	public void ScanForPeripherals (CBUUID[] peripheralUuids, PeripheralScanningOptions options);
 	public void ScanForPeripherals (Guid [] serviceUuids, PeripheralScanningOptions options);
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
<p>Added:</p><pre>
 	public virtual void WillRestoreState (CBCentralManager central, MonoTouch.Foundation.NSDictionary dict);
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
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralAuthorizationStatus</h3>
<pre>
[Serializable]
public enum CBPeripheralAuthorizationStatus {
	NotDetermined,
	Restricted,
	Denied,
	Authorized
}
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void InvalidatedService (CBPeripheral peripheral);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7")]
	public virtual void InvalidatedService (CBPeripheral peripheral);
 	public virtual void ModifiedServices (CBPeripheral peripheral, MonoTouch.Foundation.NSArray services);
</pre>
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManager</h3>
<p>Added:</p><pre>
 	public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, MonoTouch.CoreFoundation.DispatchQueue queue, MonoTouch.Foundation.NSDictionary options);
 	public static CBPeripheralAuthorizationStatus AuthorizationStatus {
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
<h3>Type Changed: MonoTouch.CoreBluetooth.CBPeripheralManagerDelegate</h3>
<p>Added:</p><pre>
 	public virtual void WillRestoreState (CBPeripheralManager peripheral, MonoTouch.Foundation.NSDictionary dict);
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.CBPeripheralServicesEventArgs</h3>
<pre>
public class CBPeripheralServicesEventArgs : EventArgs {
	
	public CBPeripheralServicesEventArgs (MonoTouch.Foundation.NSArray services);
	
	public MonoTouch.Foundation.NSArray Services {
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
<h3>New Type: MonoTouch.CoreBluetooth.PeripheralConnectionOptions</h3>
<pre>
public class PeripheralConnectionOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public PeripheralConnectionOptions ();
	public PeripheralConnectionOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public bool NotifyOnConnectionKey {
		set;
	}
	public bool NotifyOnDisconnectionKey {
		set;
	}
	public bool NotifyOnNotificationKey {
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreBluetooth.PeripheralScanningOptions</h3>
<pre>
public class PeripheralScanningOptions : MonoTouch.Foundation.DictionaryContainer {
	
	public PeripheralScanningOptions ();
	public PeripheralScanningOptions (MonoTouch.Foundation.NSDictionary dictionary);
	
	public bool AllowDuplicatesKey {
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator</h3>
<p>Added:</p><pre>
 	public static bool RemoveUbiquitousContentAndPersistentStore (MonoTouch.Foundation.NSUrl storeUrl, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
 	public static MonoTouch.Foundation.NSString eUbiquitousContainerIdentifierKey {
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
<h2>Namespace: MonoTouch.CoreFoundation</h2>
<h3>Type Changed: MonoTouch.CoreFoundation.DispatchQueue</h3>
<p>Added:</p><pre>
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
<h2>Namespace: MonoTouch.CoreMedia</h2>
<h3>Type Changed: MonoTouch.CoreMedia.CMSampleBuffer</h3>
<p>Added:</p><pre>
 	public static CMSampleBuffer CreateWithNewTiming (CMSampleBuffer original, CMSampleTimingInfo[] timing);
 	public static CMSampleBuffer CreateWithNewTiming (CMSampleBuffer original, CMSampleTimingInfo[] timing, out int status);
 	public CMSampleTimingInfo[] GetSampleTimingInfo ();
 	public CMSampleTimingInfo[] GetSampleTimingInfo (out int status);
</pre>
<h3>Type Changed: MonoTouch.CoreMedia.CMTime</h3>
<p>Removed:</p><pre>
 	public const int MaxTimeScale = 2147483647;
</pre>
<p>Added:</p><pre>
 	public const int MaxTimeScale = 2147483647;
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
	
	public virtual void AuthenticateWithInfo (MonoTouch.Foundation.NSDictionary info, SimAuthenticationCallback callback);
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
<h3>New Type: MonoTouch.CoreTelephony.CTSubscriberSimAuthentication</h3>
<pre>
public static class CTSubscriberSimAuthentication {
	
	public static MonoTouch.Foundation.NSString AutnKey {
		get;
	}
	public static MonoTouch.Foundation.NSString AutsKey {
		get;
	}
	public static MonoTouch.Foundation.NSString CkKey {
		get;
	}
	public static MonoTouch.Foundation.NSString IkKey {
		get;
	}
	public static MonoTouch.Foundation.NSString KcKey {
		get;
	}
	public static MonoTouch.Foundation.NSString RandKey {
		get;
	}
	public static MonoTouch.Foundation.NSString ResKey {
		get;
	}
	public static MonoTouch.Foundation.NSString SresKey {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreTelephony.CTSubscriberSimAuthenticationType</h3>
<pre>
public static class CTSubscriberSimAuthenticationType {
	
	public static MonoTouch.Foundation.NSString EAPAKA {
		get;
	}
	public static MonoTouch.Foundation.NSString EAPSIM {
		get;
	}
	public static MonoTouch.Foundation.NSString Key {
		get;
	}
}
</pre>
<h3>Type Changed: MonoTouch.CoreTelephony.CTTelephonyNetworkInfo</h3>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString CellIdDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SignalStrengthDidChangeNotification {
 		get;
 	}
 	public virtual string CellId {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString CurrentRadioAccessTechnology {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary SignalStrength {
 		get;
 	}
 	
 	public static class Notifications {
 		
 		public static MonoTouch.Foundation.NSObject ObserveCellIdDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveSignalStrengthDidChange (EventHandler&lt;SignalStrengthChangedEventArgs&gt; handler);
 	}
</pre>
<h3>New Type: MonoTouch.CoreTelephony.SignalStrengthChangedEventArgs</h3>
<pre>
public class SignalStrengthChangedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	
	public SignalStrengthChangedEventArgs (MonoTouch.Foundation.NSNotification notification);
	
	public MonoTouch.Foundation.NSNumber Bars {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.CoreTelephony.SimAuthenticationCallback</h3>
<pre>
[Serializable]
public delegate void SimAuthenticationCallback (MonoTouch.Foundation.NSDictionary dictionary);
</pre>
<h2>Namespace: MonoTouch.CoreText</h2>
<h3>Type Changed: MonoTouch.CoreText.CTFontDescriptor</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated")]
	public CTFontDescriptor WithFeature (Selector featureSelector);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated")]
	public CTFontDescriptor WithFeature (Selector featureSelector);
</pre>
<h2>Namespace: MonoTouch.CoreVideo</h2>
<h3>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h3>
<p>Removed:</p><pre>
 	protected override void Finalize ();
 	
</pre>
<h2>Namespace: MonoTouch.EventKit</h2>
<h3>Type Changed: MonoTouch.EventKit.EKEventStore</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;EKReminder[]&gt; FetchRemindersAsync (MonoTouch.Foundation.NSPredicate predicate);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; RequestAccessAsync (EKEntityType entityType);
</pre>
<h3>Type Changed: MonoTouch.EventKit.EKSource</h3>
<p>Added:</p><pre>
 	public static EKSource Create (EKEventStore eventStore);
</pre>
<h2>Namespace: MonoTouch.ExternalAccessory</h2>
<h3>Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task ShowBluetoothAccessoryPickerAsync (MonoTouch.Foundation.NSPredicate predicate);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.DictionaryContainer</h3>
<p>Removed:</p><pre>
 	protected string GetNSStringValue (NSString key);
</pre>
<p>Added:</p><pre>
 	protected NSString GetNSStringValue (NSString key);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSAttributedString</h3>
<p>Added:</p><pre>
 	public NSAttributedString (NSData data, NSDictionary options, ref NSDictionary documentAttributes, out NSError error);
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
<h3>Type Changed: MonoTouch.Foundation.NSComparisonPredicateOptions</h3>
<p>Removed:</p><pre>
 	DiacriticInsensitive
</pre>
<p>Added:</p><pre>
 	DiacriticInsensitive,
 	Normalized
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSData</h3>
<p>Added:</p><pre>
 	public NSData (string base64String, NSDataBase64DecodingOptions options);
 	public NSData (NSData base64Data, NSDataBase64DecodingOptions options);
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
<h3>Type Changed: MonoTouch.Foundation.NSDateComponentsWrappingBehavior</h3>
<p>Removed:</p><pre>
 	WrapCalendarComponents
</pre>
<p>Added:</p><pre>
 	WrapCalendarComponents,
 	MatchStrictly,
 	SearchBackwards,
 	MatchPreviousTimePreservingSmallerUnits,
 	MatchNextTimePreservingSmallerUnits,
 	MatchNextTime,
 	MatchFirst,
 	MatchLast
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
<h3>Type Changed: MonoTouch.Foundation.NSLocale</h3>
<p>Added:</p><pre>
 	public static NSLocale FromLocaleIdentifier (string ident);
</pre>
<h3>New Type: MonoTouch.Foundation.NSMutableOrderedSet</h3>
<pre>
public class NSMutableOrderedSet : NSOrderedSet {
	
	public NSMutableOrderedSet (params NSObject[] objs);
	public NSMutableOrderedSet (params object [] objs);
	public NSMutableOrderedSet (params string [] strings);
	public NSMutableOrderedSet ();
	public NSMutableOrderedSet (NSCoder coder);
	public NSMutableOrderedSet (NSObjectFlag t);
	public NSMutableOrderedSet (IntPtr handle);
	public NSMutableOrderedSet (NSObject start);
	public NSMutableOrderedSet (NSSet source);
	public NSMutableOrderedSet (NSOrderedSet source);
	public NSMutableOrderedSet (int capacity);
	
	public virtual void Add (NSObject obj);
	public virtual void AddObjects (NSObject[] source);
	public virtual void ExchangeObject (int first, int second);
	public virtual void Insert (NSObject obj, int atIndex);
	public virtual void InsertObjects (NSObject[] objects, NSIndexSet atIndexes);
	public virtual void Intersect (NSOrderedSet intersectWith);
	public virtual void MoveObjects (NSIndexSet indexSet, int destination);
	public virtual void Remove (int index);
	public virtual void RemoveAllObjects ();
	public virtual void RemoveObject (NSObject obj);
	public virtual void RemoveObjects (NSIndexSet indexSet);
	public virtual void RemoveObjects (NSObject[] objects);
	public virtual void RemoveObjects (NSRange range);
	public virtual void Replace (int objectAtIndex, NSObject newObject);
	public virtual void ReplaceObjects (NSIndexSet indexSet, NSObject[] replacementObjects);
	public virtual void SetObject (NSObject obj, int index);
	public virtual void Sort (NSComparator comparator);
	public virtual void Sort (NSSortOptions sortOptions, NSComparator comparator);
	public virtual void SortRange (NSRange range, NSSortOptions sortOptions, NSComparator comparator);
	
	public override IntPtr ClassHandle {
		get;
	}
	public NSObject this [int idx] {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSOrderedSet</h3>
<pre>
public class NSOrderedSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<nsobject> {
	
	public NSOrderedSet (params NSObject[] objs);
	public NSOrderedSet (params object [] objs);
	public NSOrderedSet (params string [] strings);
	public NSOrderedSet ();
	public NSOrderedSet (NSCoder coder);
	public NSOrderedSet (NSObjectFlag t);
	public NSOrderedSet (IntPtr handle);
	public NSOrderedSet (NSObject start);
	public NSOrderedSet (NSSet source);
	public NSOrderedSet (NSOrderedSet source);
	
	public static NSOrderedSet MakeNSOrderedSet<t> (T[] values) where T : NSObject;
	public virtual NSSet AsSet ();
	public virtual bool Contains (NSObject obj);
	public bool Contains (object obj);
	public virtual NSObject FirstObject ();
	public System.Collections.Generic.IEnumerator<nsobject> GetEnumerator ();
	public virtual NSOrderedSet GetReverseOrderedSet ();
	public virtual int IndexOf (NSObject obj);
	public virtual bool Intersects (NSOrderedSet other);
	public virtual bool Intersects (NSSet other);
	public virtual bool IsEqualToOrderedSet (NSOrderedSet other);
	public virtual bool IsSubset (NSOrderedSet other);
	public virtual bool IsSubset (NSSet other);
	public virtual NSObject LastObject ();
	System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
	public T[] ToArray<t> () where T : NSObject;
	
	public static NSOrderedSet operator + (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSOrderedSet second);
	public static NSOrderedSet operator - (NSOrderedSet first, NSSet second);
	public static bool operator == (NSOrderedSet first, NSOrderedSet second);
	public static bool operator != (NSOrderedSet first, NSOrderedSet second);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int Count {
		get;
	}
	public NSObject this [int idx] {
		get;
	}
}
</t></nsobject></t></nsobject></pre>
<h3>Type Changed: MonoTouch.Foundation.NSRange</h3>
<p>Removed:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<p>Added:</p><pre>
 	public const int NotFound = 2147483647;
</pre>
<h3>New Type: MonoTouch.Foundation.NSSortOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSSortOptions {
	Concurrent,
	Stable
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSTimer</h3>
<p>Added:</p><pre>
 	public virtual double Tolerance {
 		get;
 		set;
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
 	public static NSString ArgumentDomain {
 		get;
 	}
 	public static NSString GlobalDomain {
 		get;
 	}
 	public static NSString RegistrationDomain {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.GLKit</h2>
<h3>Type Changed: MonoTouch.GLKit.GLKTextureLoader</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginLoadCubeMapAsync (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginLoadCubeMapAsync (string fileName, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (MonoTouch.Foundation.NSUrl filePath, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual System.Threading.Tasks.Task&lt;GLKTextureInfo&gt; BeginTextureLoadAsync (string file, MonoTouch.Foundation.NSDictionary textureOperations, MonoTouch.CoreFoundation.DispatchQueue queue);
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
<h3>Type Changed: MonoTouch.GameKit.GKAchievement</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKAchievement[]&gt; LoadAchievementsAsync ();
 	public static System.Threading.Tasks.Task ReportAchievementsAsync (GKAchievement[] achievements);
 	public static System.Threading.Tasks.Task ResetAchivementsAsync ();
 	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; SelectChallengeablePlayerIDsAsync (string [] playerIDs);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKAchievementDescription</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKAchievementDescription[]&gt; LoadAchievementDescriptionsAsync ();
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.UIKit.UIImage&gt; LoadImageAsync ();
</pre>
<h3>New Type: MonoTouch.GameKit.GKCategoryResult</h3>
<pre>
public class GKCategoryResult {
	
	public GKCategoryResult (string [] categories, string [] titles);
	
	public string [] Categories {
		get;
		set;
	}
	public string [] Titles {
		get;
		set;
	}
}
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKChallenge</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKChallenge[]&gt; LoadReceivedChallengesAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLeaderboard</h3>
<p>Added:</p><pre>
 	[Obsolete("Deprecated iOS 6.0, use loadLeaderboardsWithCompletionHandler")]
	public static System.Threading.Tasks.Task&lt;GKCategoryResult&gt; LoadCategoriesAsync ();
 	public static System.Threading.Tasks.Task&lt;GKLeaderboard[]&gt; LoadLeaderboardsAsync ();
 	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string categoryID);
 	public virtual System.Threading.Tasks.Task&lt;GKScore[]&gt; LoadScoresAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKLocalPlayer</h3>
<p>Added:</p><pre>
 	[Obsolete("Replaced by AuthenticateHandler in iOS 6.0")]
	public virtual System.Threading.Tasks.Task AuthenticateAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string&gt; LoadDefaultLeaderboardCategoryIDAsync ();
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; LoadFriendsAsync ();
 	public virtual System.Threading.Tasks.Task SetDefaultLeaderboardCategoryIDAsync (string categoryID);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatch</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;string&gt; ChooseBestHostPlayerAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; RematchAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKMatchmaker</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task AddPlayersAsync (GKMatch toMatch, GKMatchRequest matchRequest);
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; FindMatchAsync (GKMatchRequest request);
 	public virtual System.Threading.Tasks.Task&lt;string []&gt; FindPlayersAsync (GKMatchRequest request);
 	public virtual System.Threading.Tasks.Task&lt;GKMatch&gt; MatchAsync (GKInvite invite);
 	public virtual System.Threading.Tasks.Task&lt;int&gt; QueryActivityAsync ();
 	public virtual System.Threading.Tasks.Task&lt;int&gt; QueryPlayerGroupActivityAsync (int playerGroup);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKNotificationBanner</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task ShowAsync (string title, string message);
 	public static System.Threading.Tasks.Task ShowAsync (string title, string message, double durationSeconds);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKPlayer</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKPlayer[]&gt; LoadPlayersForIdentifiersAsync (string [] identifiers);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.UIKit.UIImage&gt; LoadPhotoAsync (GKPhotoSize size);
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task ReportScoresAsync (GKScore[] scores);
 	public virtual System.Threading.Tasks.Task ReportScoreAsync ();
</pre>
<h3>Type Changed: MonoTouch.GameKit.GKTurnBasedMatch</h3>
<p>Added:</p><pre>
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; FindMatchAsync (GKMatchRequest request);
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; LoadMatchAsync (string matchId);
 	public static System.Threading.Tasks.Task&lt;GKTurnBasedMatch[]&gt; LoadMatchesAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; AcceptInviteAsync ();
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; DeclineInviteAsync ();
 	public virtual System.Threading.Tasks.Task EndMatchInTurnAsync (MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task EndTurnAsync (GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData);
 	[Obsolete("Replaced by EndTurn in iOS 6.0")]
	public virtual System.Threading.Tasks.Task EndTurnWithNextParticipantAsync (GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task&lt;MonoTouch.Foundation.NSData&gt; LoadMatchDataAsync ();
 	[Obsolete("Replaced by ParticipantQuitInTurn (GKTurnBasedMatchOutcome, GKTurnBasedParticipant[], double, NSData, Action&lt;NSError&gt;) in iOS 6.0")]
	public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task ParticipantQuitInTurnAsync (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant[] nextParticipants, double timeoutSeconds, MonoTouch.Foundation.NSData matchData);
 	public virtual System.Threading.Tasks.Task ParticipantQuitOutOfTurnAsync (GKTurnBasedMatchOutcome matchOutcome);
 	public virtual System.Threading.Tasks.Task&lt;GKTurnBasedMatch&gt; RematchAsync ();
 	public virtual System.Threading.Tasks.Task RemoveAsync ();
 	public virtual System.Threading.Tasks.Task SaveCurrentTurnAsync (MonoTouch.Foundation.NSData matchData);
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
 	public virtual bool RequestsAlternateRoutes {
 		get;
 		set;
 	}
 	public virtual MKDirectionsTransportType TransportType {
 		get;
 		set;
 	}
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
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;MKLocalSearchResponse&gt; StartAsync ();
 	public virtual System.Threading.Tasks.Task&lt;MKLocalSearchResponse&gt; StartAsync (System.Threading.CancellationToken token);
</pre>
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
 	public event EventHandler&lt;MKDidAddOverlayRenderersEventArgs&gt; DidAddOverlayRenderers;
 	public event EventHandler&lt;MKDidFinishRenderingMapEventArgs&gt; DidFinishRenderingMap;
 	public event EventHandler WillStartRenderingMap;
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKMapViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DidAddOverlayRenderers (MKMapView mapView, MKOverlayRenderer[] renderers);
 	public virtual void DidFinishRenderingMap (MKMapView mapView, bool fullyRendered);
 	public virtual MKOverlayRenderer GetRendererForOverlay (MKMapView mapView, MonoTouch.Foundation.NSObject overlay);
 	public virtual void WillStartRenderingMap (MKMapView mapView);
</pre>
<h3>Type Changed: MonoTouch.MapKit.MKOverlay</h3>
<p>Added:</p><pre>
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
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty</h3>
<p>Removed:</p><pre>
 public static class MPMediaItemProperty {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public static class MPMediaItemProperty {
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMediaType</h3>
<p>Added:</p><pre>
 	HomeVideo,
</pre>
<h3>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.UIKit.UIImage ThumbnailImageAt (double time, MPMovieTimeOption timeOption);
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler&lt;MPMoviePlayerFullScreenEventArgs&gt; handler);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS7 in favor of RequestThumbnails")]
	public virtual MonoTouch.UIKit.UIImage ThumbnailImageAt (double time, MPMovieTimeOption timeOption);
 		public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
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
<h3>Type Changed: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate</h3>
<p>Added:</p><pre>
 	public override MonoTouch.UIKit.UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UINavigationControllerOperation operation, MonoTouch.UIKit.UIViewController fromViewController, MonoTouch.UIKit.UIViewController toViewController);
 	public override MonoTouch.UIKit.UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewControllerAnimatedTransitioning animationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (MonoTouch.UIKit.UINavigationController navigationController);
 	public override MonoTouch.UIKit.UIInterfaceOrientationMask GetSupportedInterfaceOrientations (MonoTouch.UIKit.UINavigationController navigationController);
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
	
	public virtual void DidDismissInvitaiton (MCAdvertiserAssistant advertiserAssistant);
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
	Cancelled
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
	
	public MCSession ();
	public MCSession (MonoTouch.Foundation.NSCoder coder);
	public MCSession (MonoTouch.Foundation.NSObjectFlag t);
	public MCSession (IntPtr handle);
	public MCSession (MCPeerID myPeerID, MonoTouch.Foundation.NSObject[] identity, MCEncryptionPreference encryptionPreference);
	
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
	public virtual MonoTouch.Foundation.NSObject[] SecurityIdentity {
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
public class MCSessionDelegate : MonoTouch.Foundation.NSObject {
	
	public MCSessionDelegate ();
	public MCSessionDelegate (MonoTouch.Foundation.NSCoder coder);
	public MCSessionDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MCSessionDelegate (IntPtr handle);
	
	public virtual void DidChangeState (MCSession session, MCPeerID peerID, MCSessionState state);
	public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, out MonoTouch.Foundation.NSError error);
	public virtual bool DidReceiveCertificate (MCSession session, MonoTouch.Foundation.NSArray certificate, MCPeerID peerID, Action<bool> certificateHandler);
	public virtual void DidReceiveData (MCSession session, MonoTouch.Foundation.NSData data, MCPeerID peerID);
	public virtual void DidReceiveStream (MCSession session, MonoTouch.Foundation.NSInputStream stream, string streamName, MCPeerID peerID);
	public virtual void DidStartReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSObject progress);
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
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.Foundation.NSRange arg3);
 	public static bool bool_objc_msgSend_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoTouch.Foundation.NSRange arg3);
 	public static bool bool_objc_msgSendSuper_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
 	public static float float_objc_msgSend_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static float float_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static float float_objc_msgSendSuper_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
 	public static float float_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static int int_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static int int_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static int int_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
 	public static int int_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static IntPtr IntPtr_objc_msgSend_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, MonoTouch.CoreLocation.CLLocationCoordinate2D arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_float_Double (IntPtr receiver, IntPtr selector, float arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_float_float_Double (IntPtr receiver, IntPtr selector, float arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_int_Double (IntPtr receiver, IntPtr selector, int arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, double arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_CGAffineTransform (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Double_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, bool arg3, bool arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_SizeF_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt16_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, ushort arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSend_MKTileOverlayPath (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1);
 	public static IntPtr IntPtr_objc_msgSend_PointF_Double (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSend_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static IntPtr IntPtr_objc_msgSend_RectangleF_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_CLLocationCoordinate2D_Double (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, MonoTouch.CoreLocation.CLLocationCoordinate2D arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_Double (IntPtr receiver, IntPtr selector, float arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_float_float_Double (IntPtr receiver, IntPtr selector, float arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_Double (IntPtr receiver, IntPtr selector, int arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, double arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_CGAffineTransform (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, bool arg3, bool arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_Double (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, double arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_IntPtr_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, IntPtr arg3, System.Drawing.PointF arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_SizeF_UInt32_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.SizeF arg2, uint arg3, uint arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt16_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ushort arg2, ushort arg3, IntPtr arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_MKTileOverlayPath (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKTileOverlayPath arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_Double (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, double arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_UIEdgeInsets (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.UIKit.UIEdgeInsets arg2);
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
 	public static void void_objc_msgSend_bool_UInt32 (IntPtr receiver, IntPtr selector, bool arg1, uint arg2);
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
 	public static void void_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static void void_objc_msgSend_RectangleF_NSRange_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.Foundation.NSRange arg2, System.Drawing.RectangleF arg3);
 	public static void void_objc_msgSend_RectangleF_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSend_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSend_SizeF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, MonoTouch.Foundation.NSRange arg2);
 	public static void void_objc_msgSendSuper_bool_UInt32 (IntPtr receiver, IntPtr selector, bool arg1, uint arg2);
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
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
 	public static void void_objc_msgSendSuper_RectangleF_NSRange_RectangleF (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, MonoTouch.Foundation.NSRange arg2, System.Drawing.RectangleF arg3);
 	public static void void_objc_msgSendSuper_RectangleF_RectangleF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, System.Drawing.RectangleF arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_SizeF_NSRange (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, MonoTouch.Foundation.NSRange arg2);
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Selector</h3>
<p>Added:</p><pre>
 	public static Selector FromHandle (IntPtr sel);
</pre>
<h2>Namespace: MonoTouch.PassKit</h2>
<h3>Type Changed: MonoTouch.PassKit.PKAddPassesViewController</h3>
<p>Added:</p><pre>
 	public PKAddPassesViewController (PKPass[] pass);
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
	ShouldReviewPasses
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
	public static SKAction MoveByX (float deltaX, float deltaY, double sec);
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
	public static SKAction RunAction (SKAction action, string name);
	public static SKAction RunBlock (Action block);
	public static SKAction RunBlock (Action block, MonoTouch.Foundation.NSObject queue);
	public static SKAction ScaleBy (float scale, double sec);
	public static SKAction ScaleTo (float scale, double sec);
	public static SKAction ScaleXBy (float xScale, float yScale, double sec);
	public static SKAction ScaleXTo (float scale, double sec);
	public static SKAction ScaleXTo (float xScale, float yScale, double sec);
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
	public virtual System.Drawing.PointF ParticlePositionRange {
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
	public virtual void ApplyForce (System.Drawing.PointF force);
	public virtual void ApplyForce (System.Drawing.PointF force, System.Drawing.PointF point);
	public virtual void ApplyImpulse (System.Drawing.PointF impulse);
	public virtual void ApplyImpulse (System.Drawing.PointF impulse, System.Drawing.PointF point);
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
	public virtual MonoTouch.Foundation.NSObject[] Joints {
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
	public virtual System.Drawing.PointF Velocity {
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
public class SKPhysicsContactDelegate : MonoTouch.Foundation.NSObject {
	
	public SKPhysicsContactDelegate ();
	public SKPhysicsContactDelegate (MonoTouch.Foundation.NSCoder coder);
	public SKPhysicsContactDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public SKPhysicsContactDelegate (IntPtr handle);
	
	public virtual void DidBeginContact (SKPhysicsContact contact);
	public virtual void DidEndContact (SKPhysicsContact contact);
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
	
	public static SKPhysicsJointSliding Create (SKPhysicsBody bodyA, SKPhysicsBody bodyB, System.Drawing.PointF anchor, System.Drawing.PointF axis);
	
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
public delegate void SKPhysicsWorldBodiesAlongRayStartEnumeratorHandler (SKPhysicsBody body, System.Drawing.PointF point, System.Drawing.PointF normal, out bool stop);
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
	public virtual void Preload ();
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
	protected override void Dispose (bool disposing);
	public virtual void Preload ();
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
<h3>Type Changed: MonoTouch.StoreKit.SKStoreProductViewController</h3>
<p>Added:</p><pre>
 	public System.Threading.Tasks.Task&lt;bool&gt; LoadProductAsync (StoreProductParameters parameters);
</pre>
<h2>Namespace: MonoTouch.SystemConfiguration</h2>
<h3>Type Changed: MonoTouch.SystemConfiguration.NetworkReachability</h3>
<p>Added:</p><pre>
 	public bool Schedule ();
 	public bool SetDispatchQueue (MonoTouch.CoreFoundation.DispatchQueue queue);
 	public bool Unschedule ();
</pre>
<h2>Namespace: MonoTouch.Twitter</h2>
<h3>Type Changed: MonoTouch.Twitter.TWRequest</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;TWRequestResult&gt; PerformRequestAsync ();
</pre>
<h3>New Type: MonoTouch.Twitter.TWRequestResult</h3>
<pre>
public class TWRequestResult {
	
	public TWRequestResult (MonoTouch.Foundation.NSData responseData, MonoTouch.Foundation.NSHttpUrlResponse urlResponse);
	
	public MonoTouch.Foundation.NSData ResponseData {
		get;
		set;
	}
	public MonoTouch.Foundation.NSHttpUrlResponse UrlResponse {
		get;
		set;
	}
}
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
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
	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, MonoTouch.Foundation.NSObject textContainer, float oldSize);
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
public class NSTextAttachment : MonoTouch.Foundation.NSObject {
	
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
public class NSTextAttachmentContainer : MonoTouch.Foundation.NSObject {
	
	public NSTextAttachmentContainer ();
	public NSTextAttachmentContainer (MonoTouch.Foundation.NSCoder coder);
	public NSTextAttachmentContainer (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextAttachmentContainer (IntPtr handle);
	
	public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public virtual UIImage GetImageForBounds (System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
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
public class NSTextStorageDelegate : MonoTouch.Foundation.NSObject {
	
	public NSTextStorageDelegate ();
	public NSTextStorageDelegate (MonoTouch.Foundation.NSCoder coder);
	public NSTextStorageDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public NSTextStorageDelegate (IntPtr handle);
	
	public virtual void DidProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
	public virtual void WillProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoTouch.Foundation.NSRange editedRange, int delta);
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
<h3>New Type: MonoTouch.UIKit.TransitionCoordinator_UIViewController</h3>
<pre>
public static class TransitionCoordinator_UIViewController {
	
	public static UIViewControllerTransitionCoordinator GetTransitionCoordinator (UIViewController This);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIAccessibility</h3>
<p>Added:</p><pre>
 	public static System.Drawing.RectangleF ConvertFrameToScreenCoordinates (System.Drawing.RectangleF rect, UIView view);
 	public static UIBezierPath ConvertPathToScreenCoordinates (UIBezierPath path, UIView view);
 	public static void RequestGuidedAccessSession (bool enable, Action&lt;bool&gt; completionHandler);
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
 	public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, string activityType);
</pre>
<p>Added:</p><pre>
 	public virtual string GetDataTypeIdentifierForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public abstract MonoTouch.Foundation.NSObject GetItemForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public virtual string GetSubjectForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType);
 	public virtual UIImage GetThumbnailImageForActivity (UIActivityViewController activityViewController, MonoTouch.Foundation.NSString activityType, System.Drawing.SizeF suggestedSize);
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
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Added:</p><pre>
 	public static void RegisterObjectForStateRestoration (MonoTouch.Foundation.NSObject uistateRestoringObject, string restorationIdentifier);
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
 	public virtual UIBackgroundRefreshStatus BackgroundRefreshStatus {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString PreferredContentSizeCategory {
 		get;
 	}
 		public static MonoTouch.Foundation.NSObject ObserveBackgroundRefreshStatusDidChange (System.EventHandler&lt;MonoTouch.Foundation.NSNotificationEventArgs&gt; handler);
 		public static MonoTouch.Foundation.NSObject ObserveContentSizeCategoryChanged (EventHandler&lt;UIContentSizeCategoryChangedEventArgs&gt; handler);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h3>
<p>Added:</p><pre>
 	public virtual void DidReceiveRemoteNotification (UIApplication application, MonoTouch.Foundation.NSDictionary userInfo, Action&lt;UIBackgroundFetchResult&gt; completionHandler);
 	public virtual void HandleEventsForBackgroundUrl (UIApplication application, string sessionIdentifier, MonoTouch.Foundation.NSAction completionHandler);
 	public virtual void PerformFetch (UIApplication application, Action&lt;UIBackgroundFetchResult&gt; completionHandler);
</pre>
<h3>New Type: MonoTouch.UIKit.UIAttachmentBehavior</h3>
<pre>
public class UIAttachmentBehavior : UIDynamicBehavior {
	
	public UIAttachmentBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIAttachmentBehavior (IntPtr handle);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF anchorPoint);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF point, System.Drawing.PointF anchorPoint);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, MonoTouch.Foundation.NSObject attachedToItem);
	public UIAttachmentBehavior (MonoTouch.Foundation.NSObject item, System.Drawing.PointF point, MonoTouch.Foundation.NSObject attachedToItem, System.Drawing.PointF attachedPoint);
	
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
	public virtual MonoTouch.Foundation.NSObject[] Items {
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
public class UIBarPositioningDelegate : MonoTouch.Foundation.NSObject {
	
	public UIBarPositioningDelegate ();
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIBarPositioningDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIBarPositioningDelegate (IntPtr handle);
	
	public virtual UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
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
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; PerformBatchUpdatesAsync (MonoTouch.Foundation.NSAction updates);
 	public virtual void SetCollectionViewLayout (UICollectionViewLayout layout, bool animated, UICompletionHandler completion);
 	public virtual UICollectionViewTransitionLayout StartInteractiveTransition (UICollectionViewLayout newCollectionViewLayout, UICollectionViewLayoutInteractiveTransitionCompletion completion);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewController</h3>
<p>Added:</p><pre>
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
 	public virtual UICollectionViewLayout Layout {
 		get;
 	}
 	public virtual bool UseLayoutToLayoutNavigationTransitions {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewDelegateFlowLayout</h3>
<p>Added:</p><pre>
 	public override UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
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
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForDecorationView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
</pre>
<p>Added:</p><pre>
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForDecorationView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
 	public static T CreateForSupplementaryView&lt;T&gt; (MonoTouch.Foundation.NSString kind, MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
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
<p>Added:</p><pre>
 	public virtual UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
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
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBeganBoundaryContactEventArgs</h3>
<pre>
public class UICollisionBeganBoundaryContactEventArgs : EventArgs {
	
	public UICollisionBeganBoundaryContactEventArgs (MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
	
	public System.Drawing.PointF AtPoint {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject BoundaryIdentifier {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject DynamicItem {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionBeganContactEventArgs</h3>
<pre>
public class UICollisionBeganContactEventArgs : EventArgs {
	
	public UICollisionBeganContactEventArgs (MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem, System.Drawing.PointF atPoint);
	
	public System.Drawing.PointF AtPoint {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject FirstItem {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject SecondItem {
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
	public UICollisionBehavior (MonoTouch.Foundation.NSObject[] items);
	
	public virtual void AddBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);
	public virtual void AddBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier, UIBezierPath bezierPath);
	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual UIBezierPath GetBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void RemoveAllBoundaries ();
	public virtual void RemoveBoundary (MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
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
	public virtual MonoTouch.Foundation.NSObject[] Items {
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
public class UICollisionBehaviorDelegate : MonoTouch.Foundation.NSObject {
	
	public UICollisionBehaviorDelegate ();
	public UICollisionBehaviorDelegate (MonoTouch.Foundation.NSCoder coder);
	public UICollisionBehaviorDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UICollisionBehaviorDelegate (IntPtr handle);
	
	public virtual void BeganBoundaryContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier, System.Drawing.PointF atPoint);
	public virtual void BeganContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem, System.Drawing.PointF atPoint);
	public virtual void EndedBoundaryContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
	public virtual void EndedContact (UICollisionBehavior behavior, MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem);
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
	
	public UICollisionEndedBoundaryContactEventArgs (MonoTouch.Foundation.NSObject dynamicItem, MonoTouch.Foundation.NSObject boundaryIdentifier);
	
	public MonoTouch.Foundation.NSObject BoundaryIdentifier {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject DynamicItem {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UICollisionEndedContactEventArgs</h3>
<pre>
public class UICollisionEndedContactEventArgs : EventArgs {
	
	public UICollisionEndedContactEventArgs (MonoTouch.Foundation.NSObject firstItem, MonoTouch.Foundation.NSObject secondItem);
	
	public MonoTouch.Foundation.NSObject FirstItem {
		get;
		set;
	}
	public MonoTouch.Foundation.NSObject SecondItem {
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
<h3>Type Changed: MonoTouch.UIKit.UIDevice</h3>
<p>Removed:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0")]
	public virtual string UniqueIdentifier {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in iOS 5.0. Apple now reject application using it the selector is removed and an empty string is returned")]
	public virtual string UniqueIdentifier {
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIDocument</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; AutoSaveAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; CloseAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; OpenAsync ();
 	public virtual System.Threading.Tasks.Task PerformAsynchronousFileAccessAsync ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; RevertToContentsOfUrlAsync (MonoTouch.Foundation.NSUrl url);
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SaveAsync (MonoTouch.Foundation.NSUrl url, UIDocumentSaveOperation saveOperation);
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
	public virtual MonoTouch.Foundation.NSObject[] GetDynamicItems (System.Drawing.RectangleF rect);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForCell (MonoTouch.Foundation.NSIndexPath cellIndexPath);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForDecorationView (MonoTouch.Foundation.NSString viewKind, MonoTouch.Foundation.NSIndexPath viewIndexPath);
	public virtual UICollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryView (MonoTouch.Foundation.NSString viewKind, MonoTouch.Foundation.NSIndexPath viewIndexPath);
	public virtual void RemoveAllBehaviors ();
	public virtual void RemoveBehavior (UIDynamicBehavior behavior);
	public virtual void UpdateItemFromCurrentState (MonoTouch.Foundation.NSObject uiDynamicItem);
	
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
public abstract class UIDynamicAnimatorDelegate : MonoTouch.Foundation.NSObject {
	
	public UIDynamicAnimatorDelegate ();
	public UIDynamicAnimatorDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIDynamicAnimatorDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIDynamicAnimatorDelegate (IntPtr handle);
	
	public abstract void DidPause (UIDynamicAnimator animator);
	public abstract void WillResume (UIDynamicAnimator animator);
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
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIDynamicItem</h3>
<pre>
[Obsolete]
public abstract class UIDynamicItem : MonoTouch.Foundation.NSObject {
	
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
	public UIDynamicItemBehavior (MonoTouch.Foundation.NSObject[] items);
	
	public virtual void AddAngularVelocityForItem (float velocity, MonoTouch.Foundation.NSObject dynamicItem);
	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
	public virtual void AddLinearVelocityForItem (System.Drawing.PointF velocity, MonoTouch.Foundation.NSObject dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual float GetAngularVelocityForItem (MonoTouch.Foundation.NSObject dynamicItem);
	public virtual System.Drawing.PointF GetLinearVelocityForItem (MonoTouch.Foundation.NSObject dynamicItem);
	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
	
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
	public virtual MonoTouch.Foundation.NSObject[] Items {
		get;
	}
	public virtual float Resistance {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIExtendedEdge</h3>
<pre>
[Serializable]
public enum UIExtendedEdge {
	None,
	Top,
	Left,
	Bottom,
	Right,
	All
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
	public MonoTouch.Foundation.NSDictionary[] FeatureSettings {
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
public static class UIFontTextStyle {
	
	public static MonoTouch.Foundation.NSString Body {
		get;
	}
	public static MonoTouch.Foundation.NSString Caption1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Caption2 {
		get;
	}
	public static MonoTouch.Foundation.NSString Footnote {
		get;
	}
	public static MonoTouch.Foundation.NSString Headline1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Headline2 {
		get;
	}
	public static MonoTouch.Foundation.NSString Subheadline1 {
		get;
	}
	public static MonoTouch.Foundation.NSString Subheadline2 {
		get;
	}
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
<h3>New Type: MonoTouch.UIKit.UIGravityBehavior</h3>
<pre>
public class UIGravityBehavior : UIDynamicBehavior {
	
	public UIGravityBehavior ();
	public UIGravityBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIGravityBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIGravityBehavior (IntPtr handle);
	public UIGravityBehavior (MonoTouch.Foundation.NSObject[] items);
	
	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
	public virtual void SetComponents (float xComponent, float yComponent);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject[] Items {
		get;
	}
	public virtual float XComponent {
		get;
		set;
	}
	public virtual float YComponent {
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
<p>Removed:</p><pre>
 	public UIImage (UIImage image);
 	public UIImage (UIImage image, MonoTouch.Foundation.NSDictionary options);
</pre>
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
<p>Added:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
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
 public class UINavigationBarDelegate : UIBarPositioningDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationController</h3>
<p>Added:</p><pre>
 	public virtual UIGestureRecognizer InteractivePopGestureRecognizer {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UINavigationControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
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
public class UIObjectRestoration : MonoTouch.Foundation.NSObject {
	
	public UIObjectRestoration ();
	public UIObjectRestoration (MonoTouch.Foundation.NSCoder coder);
	public UIObjectRestoration (MonoTouch.Foundation.NSObjectFlag t);
	public UIObjectRestoration (IntPtr handle);
	
	public virtual MonoTouch.Foundation.NSObject GetStateRestorationObjectFromPath (MonoTouch.Foundation.NSString[] identifierComponents, MonoTouch.Foundation.NSCoder coder);
}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewController</h3>
<p>Added:</p><pre>
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; SetViewControllersAsync (UIViewController[] viewControllers, UIPageViewControllerNavigationDirection direction, bool animated);
 	public Func&lt;UIPageViewController,UIInterfaceOrientation&gt; GetPreferredInterfaceOrientationForPresentation {
 		get;
 		set;
 	}
 	public Func&lt;UIPageViewController,UIInterfaceOrientationMask&gt; GetSupportedInterfaceOrientations {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPageViewControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientationForPresentation (UIPageViewController pageViewController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UIPageViewController pageViewController);
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
<h3>Type Changed: MonoTouch.UIKit.UIPopoverController</h3>
<p>Added:</p><pre>
 	public virtual void PresentPopover (System.Drawing.RectangleF rect, UIView targetView, UIPopoverPreferredPresentationDirection preferredPresentationDirections);
 	public virtual void PresentPopover (UIBarButtonItem barButtonItem);
 	public event EventHandler&lt;UIPopoverControllerRepositionEventArgs&gt; WillReposition;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIPopoverControllerDelegate</h3>
<p>Added:</p><pre>
 	public virtual void WillReposition (UIPopoverController popoverController, ref System.Drawing.RectangleF rect, ref UIView view);
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
<h3>New Type: MonoTouch.UIKit.UIPopoverPreferredPresentationDirection</h3>
<pre>
[Serializable]
[Flags]
public enum UIPopoverPreferredPresentationDirection : uint {
	Below,
	Above,
	Right,
	Left,
	Any,
	Unknown
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
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentAsync (bool animated);
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentFromBarButtonItemAsync (UIBarButtonItem item, bool animated);
 	public virtual System.Threading.Tasks.Task&lt;UIPrintInteractionResult&gt; PresentFromRectInViewAsync (System.Drawing.RectangleF rect, UIView view, bool animated);
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
<p>Added:</p><pre>
 	public virtual float CutLengthForPaper (UIPrintInteractionController printInteractionController, UIPrintPaper paper);
</pre>
<h3>New Type: MonoTouch.UIKit.UIPrintInteractionResult</h3>
<pre>
public class UIPrintInteractionResult {
	
	public UIPrintInteractionResult (UIPrintInteractionController printInteractionController, bool completed);
	
	public bool Completed {
		get;
		set;
	}
	public UIPrintInteractionController PrintInteractionController {
		get;
		set;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIPushBehavior</h3>
<pre>
public class UIPushBehavior : UIDynamicBehavior {
	
	public UIPushBehavior ();
	public UIPushBehavior (MonoTouch.Foundation.NSCoder coder);
	public UIPushBehavior (MonoTouch.Foundation.NSObjectFlag t);
	public UIPushBehavior (IntPtr handle);
	public UIPushBehavior (MonoTouch.Foundation.NSObject[] items, UIPushBehaviorMode mode);
	
	public virtual void AddItem (MonoTouch.Foundation.NSObject dynamicItem);
	protected override void Dispose (bool disposing);
	public virtual System.Drawing.PointF GetTargetPoint (UIDynamicItem item);
	public virtual void RemoveItem (MonoTouch.Foundation.NSObject dynamicItem);
	public virtual void SetAngleAndMagnitude (float angle, float magnitude);
	public virtual void SetComponents (float x, float y);
	public virtual void SetTargetPoint (System.Drawing.PointF point, UIDynamicItem item);
	
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
	public virtual MonoTouch.Foundation.NSObject[] Items {
		get;
	}
	public virtual float Magnitude {
		get;
		set;
	}
	public virtual UIPushBehaviorMode Mode {
		get;
	}
	public virtual float XComponent {
		get;
		set;
	}
	public virtual float YComponent {
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
 	public virtual UIView SnapshotView ();
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIScrollView</h3>
<p>Added:</p><pre>
 	public virtual UIScrollViewKeyboardDismissMode KeyboardDismissMode {
 		get;
 		set;
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
 public class UISearchBarDelegate : UIBarPositioningDelegate {
 	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
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
	public UISnapBehavior (MonoTouch.Foundation.NSObject dynamicItem, System.Drawing.PointF point);
	
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
<h3>New Type: MonoTouch.UIKit.UIStateRestoring</h3>
<pre>
public class UIStateRestoring : MonoTouch.Foundation.NSObject {
	
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
	public virtual MonoTouch.Foundation.NSObject RestorationParent {
		get;
	}
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
 	public virtual UIImage DividerImageForLeftItemState (UIControlState leftItemState, UIControlState rightItemState);
 	public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftItemState, UIControlState rightItemState);
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
 		public virtual UIImage DividerImageForLeftItemState (UIControlState leftItemState, UIControlState rightItemState);
 		public virtual void SetDividerImage (UIImage dividerImage, UIControlState leftItemState, UIControlState rightItemState);
 		
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
<p>Added:</p><pre>
 	public virtual UIViewControllerAnimatedTransitioning GetAnimationControllerForTransition (UITabBarController tabBarController, UIViewController fromViewController, UIViewController toViewController);
 	public virtual UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UITabBarController tabBarController, UIViewControllerAnimatedTransitioning animationController);
 	public virtual UIInterfaceOrientation GetPreferredInterfaceOrientation (UITabBarController tabBarController);
 	public virtual UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UITabBarController tabBarController);
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
<h3>Type Changed: MonoTouch.UIKit.UITableViewController</h3>
<p>Added:</p><pre>
 	public virtual float EstimatedHeight (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float EstimatedHeightForFooter (UITableView tableView, int section);
 	public virtual float EstimatedHeightForHeader (UITableView tableView, int section);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual float EstimatedHeight (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float EstimatedHeightForFooter (UITableView tableView, int section);
 	public virtual float EstimatedHeightForHeader (UITableView tableView, int section);
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
<h3>Type Changed: MonoTouch.UIKit.UITextInputMode</h3>
<p>Removed:</p><pre>
 	public static UITextInputMode CurrentInputMode {
</pre>
<p>Added:</p><pre>
 	[Obsolete("Deprecated in IOS7")]
	public static UITextInputMode CurrentInputMode {
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
 	public virtual NSTextStorage TextStorage {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary WeakLinkTextAttributes {
 		get;
 		set;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITextViewDelegate</h3>
<p>Added:</p><pre>
 	public virtual bool ShouldInteractWithTextAttachment (UITextView textView, NSTextAttachment textAttachment, MonoTouch.Foundation.NSRange characterRange);
 	public virtual bool ShouldInteractWithUrl (UITextView textView, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSRange characterRange);
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
public class UIToolbarDelegate : UIBarPositioningDelegate {
	
	public UIToolbarDelegate ();
	public UIToolbarDelegate (MonoTouch.Foundation.NSCoder coder);
	public UIToolbarDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public UIToolbarDelegate (IntPtr handle);
	
	public override UIBarPosition GetPositionForBar (MonoTouch.Foundation.NSObject barPositioning);
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
<p>Added:</p><pre>
 	public override UIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
 	public override UIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, UIViewControllerAnimatedTransitioning animationController);
 	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
 	public override UIInterfaceOrientationMask GetSupportedInterfaceOrientations (UINavigationController navigationController);
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIView</h3>
<p>Added:</p><pre>
 	public static void AddKeyframeWithRelativeStartTime (double frameStartTime, double frameDuration, MonoTouch.Foundation.NSAction animations);
 	public static void AnimateKeyframes (double duration, double delay, UIViewKeyframeAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completion);
 	public static void AnimateNotify (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations, UICompletionHandler completion);
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateNotifyAsync (double duration, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; AnimateNotifyAsync (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation);
 	public static void PerformSystemAnimation (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction parallelAnimations, UICompletionHandler completion);
 	public static void PerformWithoutAnimation (MonoTouch.Foundation.NSAction actionsWithoutAnimation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; TransitionNotifyAsync (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation);
 	public static System.Threading.Tasks.Task&lt;bool&gt; TransitionNotifyAsync (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options);
 	public virtual bool AccessibilityActivate ();
 	public virtual void AddMotionEffect (UIMotionEffect effect);
 	public virtual bool DrawViewHierarchy (System.Drawing.RectangleF rect);
 	public virtual UIBezierPath OutlinePath ();
 	public virtual void RemoveMotionEffect (UIMotionEffect effect);
 	public virtual UIView ResizableSnapshotView (System.Drawing.RectangleF rect, UIEdgeInsets capInsets);
 	public virtual UIView SnapshotView ();
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
<h3>Type Changed: MonoTouch.UIKit.UIViewController</h3>
<p>Removed:</p><pre>
 	public virtual bool WantsFullScreenLayout {
</pre>
<p>Added:</p><pre>
 	public virtual void ApplicationFinishedRestoringState ();
 	public virtual UIViewController ChildViewControllerForStatusBarHidden ();
 	public virtual UIViewController ChildViewControllerForStatusBarStyle ();
 	public virtual System.Threading.Tasks.Task DismissViewControllerAsync (bool animated);
 	public virtual UIStatusBarStyle PreferredStatusBarStyle ();
 	public virtual bool PrefersStatusBarHidden ();
 	public virtual System.Threading.Tasks.Task PresentViewControllerAsync (UIViewController viewControllerToPresent, bool animated);
 	public virtual void SetNeedsStatusBarAppearanceUpdate ();
 	public virtual System.Threading.Tasks.Task&lt;bool&gt; TransitionAsync (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animations);
 	public virtual bool AutomaticallyAdjustsScrollViewInsets {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSObject BottomLayoutGuide {
 		get;
 	}
 	public virtual UIExtendedEdge EdgesForExtendedLayout {
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
 	public virtual MonoTouch.Foundation.NSObject TopLayoutGuide {
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
<h3>New Type: MonoTouch.iAd.ADInterstitialPresentationPolicy</h3>
<pre>
[Serializable]
public enum ADInterstitialPresentationPolicy {
	None,
	Automatic,
	Manual
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
