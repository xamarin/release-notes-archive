---
id: E0AAA474-B270-4344-B742-34E30770CB13
title: "From 1.6 to 1.8"
---

<html>
<head>
<title>Comparison between XamMac.dll (1.6.27) and XamMac.dll (1.8.0.6)</title>
</head>
<body>

<h1>XamMac.dll</h1>
<h2>Namespace MonoMac</h2>
<h3>Type Changed: MonoMac.Constants</h3>
<p>Added fields:</p><pre>
	public static const string AccelerateImageLibrary = "/System/Library/Frameworks/Accelerate.framework/Frameworks/vImage.framework/vImage";
	public static const string ApplicationServicesCoreGraphicsLibrary = "/System/Library/Frameworks/ApplicationServices.framework/Frameworks/CoreGraphics.framework/CoreGraphics";
</pre>


<h2>Namespace MonoMac.AddressBook</h2>
<h3>Type Changed: MonoMac.AddressBook.ABPerson</h3>
<p>Removed properties:</p><pre>
	public static ABPersonCompositeNameFormat CompositeNameFormat { get; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0 in favor of GetCompositeNameFormat(null)")]
	public static ABPersonCompositeNameFormat CompositeNameFormat { get; }

</pre>
<p>Added methods:</p><pre>
	public static string GetCompositeNameDelimiter (ABRecord record);
	public static ABPersonCompositeNameFormat GetCompositeNameFormat (ABRecord record);
</pre>


<h2>Namespace MonoMac.AppKit</h2>
<h3>Type Changed: MonoMac.AppKit.NSApplication</h3>
<p>Removed events:</p><pre>
	public event System.EventHandler&lt;NSErrorEventArgs&gt; FailedToRegisterForRemoteNotifications;
</pre>
<p>Added events:</p><pre>
	public event System.EventHandler&lt;MonoMac.Foundation.NSErrorEventArgs&gt; FailedToRegisterForRemoteNotifications;
</pre>

<h3>Type Changed: MonoMac.AppKit.NSBitmapImageRep</h3>
<p>Added methods:</p><pre>
	public MonoMac.Foundation.NSData RepresentationUsingTypeProperties (NSBitmapImageFileType storageType);
</pre>

<h3>Type Changed: MonoMac.AppKit.NSCoderEventArgs</h3>
<p>Removed constructors:</p><pre>
	public NSCoderEventArgs (MonoMac.Foundation.NSCoder encoder);
</pre>
<p>Added constructors:</p><pre>
	public NSCoderEventArgs (MonoMac.Foundation.NSCoder state);
</pre>
<p>Removed properties:</p><pre>
	public MonoMac.Foundation.NSCoder Encoder { get; set; }
</pre>
<p>Added properties:</p><pre>
	public MonoMac.Foundation.NSCoder State { get; set; }
</pre>

<h3>Type Changed: MonoMac.AppKit.NSComboBoxCell</h3>
<p>Removed constructors:</p><pre>
	public NSComboBoxCell (System.Drawing.RectangleF frameRect);
</pre>
<p>Added constructors:</p><pre>
	[Obsolete ("")]
	public NSComboBoxCell (System.Drawing.RectangleF frameRect);

</pre>

<h3>Type Changed: MonoMac.AppKit.NSDocumentChangeType</h3>
<p>Removed values:</p><pre>
	Autosaved = 5,
	ReadOtherContents = 4,
	Redone = 3,
</pre>
<p>Added values:</p><pre>
	Autosaved = 4,
	Discardable = 256,
	ReadOtherContents = 3,
	Redone = 5,
</pre>

<h3>Type Changed: MonoMac.AppKit.NSEventMask</h3>
<p>Added values:</p><pre>
	SmartMagnify = 4294967296,
</pre>

<h3>Type Changed: MonoMac.AppKit.NSFont</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString CascadeListAttribute { get; }
	public static MonoMac.Foundation.NSString CharacterSetAttribute { get; }
	public static MonoMac.Foundation.NSString FaceAttribute { get; }
	public static MonoMac.Foundation.NSString FamilyAttribute { get; }
	public static MonoMac.Foundation.NSString FeatureSelectorIdentifierKey { get; }
	public static MonoMac.Foundation.NSString FeatureSettingsAttribute { get; }
	public static MonoMac.Foundation.NSString FeatureTypeIdentifierKey { get; }
	public static MonoMac.Foundation.NSString FixedAdvanceAttribute { get; }
	public static MonoMac.Foundation.NSString MatrixAttribute { get; }
	public static MonoMac.Foundation.NSString NameAttribute { get; }
	public static MonoMac.Foundation.NSString SizeAttribute { get; }
	public static MonoMac.Foundation.NSString SlantTrait { get; }
	public static MonoMac.Foundation.NSString SymbolicTrait { get; }
	public static MonoMac.Foundation.NSString TraitsAttribute { get; }
	public static MonoMac.Foundation.NSString VariationAttribute { get; }
	public static MonoMac.Foundation.NSString VariationAxisDefaultValueKey { get; }
	public static MonoMac.Foundation.NSString VariationAxisIdentifierKey { get; }
	public static MonoMac.Foundation.NSString VariationAxisMaximumValueKey { get; }
	public static MonoMac.Foundation.NSString VariationAxisMinimumValueKey { get; }
	public static MonoMac.Foundation.NSString VariationAxisNameKey { get; }
	public static MonoMac.Foundation.NSString VisibleNameAttribute { get; }
	public static MonoMac.Foundation.NSString WeightTrait { get; }
	public static MonoMac.Foundation.NSString WidthTrait { get; }
</pre>

<h3>Type Changed: MonoMac.AppKit.NSTextField</h3>
<p>Added properties:</p><pre>
	public NSTextFieldCell Cell { get; set; }
</pre>

<h3>Type Changed: MonoMac.AppKit.NSTreeController</h3>
<p>Removed properties:</p><pre>
	public virtual NSTreeController Content { get; set; }
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSObject Content { get; set; }
</pre>

<h3>Type Changed: MonoMac.AppKit.NSTreeNode</h3>
<p>Removed properties:</p><pre>
	public virtual NSTreeNode RepresentedObject { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSObject RepresentedObject { get; }
</pre>

<h3>Removed Type MonoMac.AppKit.NSErrorEventArgs
<h3>New Type MonoMac.AppKit.INSPageControllerDelegate</h3>
<pre>
public interface INSPageControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AppKit.NSPageController</h3>
<pre>
public class NSPageController : MonoMac.AppKit.NSViewController, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPageController ();
	public NSPageController (MonoMac.Foundation.NSCoder coder);
	public NSPageController (MonoMac.Foundation.NSObjectFlag t);
	public NSPageController (System.IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSDictionary Animations { get; set; }
	public virtual MonoMac.Foundation.NSObject Animator { get; }
	public virtual MonoMac.Foundation.NSObject[] ArrangedObjects { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public NSPageControllerDelegate Delegate { get; set; }
	public virtual int SelectedIndex { get; set; }
	public virtual NSViewController SelectedViewController { get; }
	public virtual NSPageControllerTransitionStyle TransitionStyle { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// events
	public event System.EventHandler DidEndLiveTransition;
	public event System.EventHandler&lt;NSPageControllerTransitionEventArgs&gt; DidTransition;
	public event System.EventHandler WillStartLiveTransition;
	// methods
	public virtual MonoMac.Foundation.NSObject AnimationFor (MonoMac.Foundation.NSString key);
	public virtual void CompleteTransition ();
	public static MonoMac.Foundation.NSObject DefaultAnimationFor (MonoMac.Foundation.NSString key);
	protected override void Dispose (bool disposing);
	public virtual void NavigateBack (MonoMac.Foundation.NSObject sender);
	public virtual void NavigateForward (MonoMac.Foundation.NSObject sender);
	public virtual void NavigateForwardTo (MonoMac.Foundation.NSObject target);
	public virtual void NavigateTo (MonoMac.Foundation.NSObject sender);
}
</pre>
<h3>New Type MonoMac.AppKit.NSPageControllerDelegate</h3>
<pre>
public class NSPageControllerDelegate : MonoMac.Foundation.NSObject, INSPageControllerDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPageControllerDelegate ();
	public NSPageControllerDelegate (MonoMac.Foundation.NSCoder coder);
	public NSPageControllerDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSPageControllerDelegate (System.IntPtr handle);
	// methods
	public virtual void DidEndLiveTransition (NSPageController pageController);
	public virtual void DidTransition (NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public virtual void WillStartLiveTransition (NSPageController pageController);
}
</pre>
<h3>New Type MonoMac.AppKit.NSPageControllerDelegate_Extensions</h3>
<pre>
public static class NSPageControllerDelegate_Extensions {
	// methods
	public static void DidEndLiveTransition (INSPageControllerDelegate This, NSPageController pageController);
	public static void DidTransition (INSPageControllerDelegate This, NSPageController pageController, MonoMac.Foundation.NSObject targetObject);
	public static void WillStartLiveTransition (INSPageControllerDelegate This, NSPageController pageController);
}
</pre>
<h3>New Type MonoMac.AppKit.NSPageControllerTransitionEventArgs</h3>
<pre>
public class NSPageControllerTransitionEventArgs : System.EventArgs {
	// constructors
	public NSPageControllerTransitionEventArgs (MonoMac.Foundation.NSObject targetObject);
	// properties
	public MonoMac.Foundation.NSObject TargetObject { get; set; }
}
</pre>
<h3>New Type MonoMac.AppKit.NSPageControllerTransitionStyle</h3>
<pre>
[Serializable]
public enum NSPageControllerTransitionStyle {
	HorizontalStrip = 2,
	StackBook = 1,
	StackHistory = 0,
}
</pre>

</h3><h2>Namespace MonoMac.AudioToolbox</h2>
<h3>Type Changed: MonoMac.AudioToolbox.AudioChannelLayoutTag</h3>
<p>Added values:</p><pre>
	AAC_7_1_B = 11993096,
	AAC_7_1_C = 12058632,
</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioFileProperty</h3>
<p>Added values:</p><pre>
	AudioTrackCount = 1635017588,
	UseAudioTrack = 1969321067,
</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioFileStreamProperty</h3>
<p>Added values:</p><pre>
	InfoDictionary = 1768842863,
</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioQueueParameter</h3>
<p>Added values:</p><pre>
	Pitch = 3,
	PlayRate = 2,
</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioQueueProperty</h3>
<p>Removed values:</p><pre>
	EnableTimePitch = 1633645680,
	TimePitchAlgorithm = 1635020897,
	TimePitchBypass = 1635020898,
</pre>
<p>Added values:</p><pre>
	EnableTimePitch = 1902081136,
	TimePitchAlgorithm = 1903456353,
	TimePitchBypass = 1903456354,
</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioSession</h3>
<p>Removed properties:</p><pre>
	public static bool AudioInputAvailable { get; }
	public static bool AudioShouldDuck { get; set; }
	public static AudioSessionCategory Category { get; set; }
	public static float CurrentHardwareInputLatency { get; }
	public static int CurrentHardwareInputNumberChannels { get; }
	public static float CurrentHardwareIOBufferDuration { get; }
	public static float CurrentHardwareOutputLatency { get; }
	public static int CurrentHardwareOutputNumberChannels { get; }
	public static float CurrentHardwareOutputVolume { get; }
	public static double CurrentHardwareSampleRate { get; }
	public static bool InputGainAvailable { get; }
	public static float InputGainScalar { get; set; }
	public static AudioSessionInterruptionType InterruptionType { get; }
	public static AudioSessionMode Mode { get; set; }
	public static bool OtherAudioIsPlaying { get; }
	public static bool OverrideCategoryDefaultToSpeaker { get; set; }
	public static bool OverrideCategoryEnableBluetoothInput { get; set; }
	public static bool OverrideCategoryMixWithOthers { get; set; }
	public static float PreferredHardwareIOBufferDuration { get; set; }
	public static double PreferredHardwareSampleRate { get; set; }
	public static AudioSessionRoutingOverride RoutingOverride { set; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool AudioInputAvailable { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool AudioShouldDuck { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionCategory Category { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareInputLatency { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static int CurrentHardwareInputNumberChannels { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareIOBufferDuration { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareOutputLatency { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static int CurrentHardwareOutputNumberChannels { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float CurrentHardwareOutputVolume { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static double CurrentHardwareSampleRate { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool InputGainAvailable { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float InputGainScalar { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionInterruptionType InterruptionType { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionMode Mode { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OtherAudioIsPlaying { get; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryDefaultToSpeaker { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryEnableBluetoothInput { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static bool OverrideCategoryMixWithOthers { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static float PreferredHardwareIOBufferDuration { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static double PreferredHardwareSampleRate { get; set; }

	[Obsolete ("AudioSession[Get|Set]Property are deprecated in iOS7")]
	public static AudioSessionRoutingOverride RoutingOverride { set; }

</pre>
<p>Removed methods:</p><pre>
	public static AudioSessionErrors AddListener (AudioSessionProperty property, AudioSession.PropertyListener listener);
	public static void Initialize ();
	public static void SetActive (bool active);
	public static AudioSessionErrors SetActive (bool active, AudioSessionActiveFlags flags);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS7")]
	public static AudioSessionErrors AddListener (AudioSessionProperty property, AudioSession.PropertyListener listener);

	[Obsolete ("Deprecated in iOS7")]
	public static void Initialize ();

	[Obsolete ("Deprecated in iOS7")]
	public static void SetActive (bool active);

	[Obsolete ("Deprecated in iOS7")]
	public static AudioSessionErrors SetActive (bool active, AudioSessionActiveFlags flags);

</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioSessionRouteChangeEventArgs</h3>
<p>Removed properties:</p><pre>
	public AudioSessionRouteChangeReason Reason { get; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in iOS7")]
	public AudioSessionRouteChangeReason Reason { get; }

</pre>

<h3>Type Changed: MonoMac.AudioToolbox.AudioSessionRouteChangeReason</h3>
<p>Added values:</p><pre>
	RouteConfigurationChange = 8,
</pre>

<h3>New Type MonoMac.AudioToolbox.AudioQueueTimePitchAlgorithm</h3>
<pre>
[Serializable]
public enum AudioQueueTimePitchAlgorithm {
	Spectral = 1936745827,
	TimeDomain = 1953064047,
	Varispeed = 1987276900,
}
</pre>
<h3>New Type MonoMac.AudioToolbox.InstrumentInfo</h3>
<pre>
public class InstrumentInfo {
	// fields
	public static const string LSBKey = "LSB";
	public static const string MSBKey = "MSB";
	public static const string NameKey = "name";
	public static const string ProgramKey = "program";
	// properties
	public MonoMac.Foundation.NSDictionary Dictionary { get; }
	public int LSB { get; }
	public int MSB { get; }
	public string Name { get; }
	public int Program { get; }
}
</pre>
<h3>New Type MonoMac.AudioToolbox.SoundBank</h3>
<pre>
public class SoundBank {
	// constructors
	public SoundBank ();
	// methods
	public static InstrumentInfo[] GetInstrumentInfo (MonoMac.Foundation.NSUrl url);
	public static string GetName (MonoMac.Foundation.NSUrl url);
}
</pre>

<h2>Namespace MonoMac.AudioUnit</h2>
<h3>Type Changed: MonoMac.AudioUnit.AudioComponentFlag</h3>
<p>Added values:</p><pre>
	SandboxSafe = 2,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioComponentType</h3>
<p>Added values:</p><pre>
	MIDIProcessor = 1635085673,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioTypeConverter</h3>
<p>Added values:</p><pre>
	AUiPodTimeOther = 1768977519,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioTypeEffect</h3>
<p>Removed values:</p><pre>
	DCFilter = 1684235884,
</pre>
<p>Added values:</p><pre>
	[Obsolete ("Removed in iOS 7")]
	DCFilter = 1684235884,

	NBandEq = 1851942257,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioUnit</h3>
<p>Added methods:</p><pre>
	public ClassInfoDictionary GetClassInfo (AudioUnitScopeType scope, uint audioUnitElement);
	public uint GetMaximumFramesPerSlice (AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitParameterInfo[] GetParameterList (AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus LoadInstrument (SamplerInstrumentData instrumentData, AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus MakeConnection (AudioUnit sourceAudioUnit, uint sourceOutputNumber, uint destInputNumber);
	public AudioUnitStatus MusicDeviceMIDIEvent (uint status, uint data1, uint data2, uint offsetSampleFrame);
	public AudioUnitStatus SetClassInfo (ClassInfoDictionary preset, AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus SetElementCount (AudioUnitScopeType scope, uint count);
	public AudioUnitStatus SetInputCallback (InputDelegate inputDelegate, AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus SetSampleRate (double sampleRate, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioUnitParameterType</h3>
<p>Removed values:</p><pre>
	AUDCFilterDecayTime = 0,
</pre>
<p>Added values:</p><pre>
	[Obsolete ("Removed in iOS 7")]
	AUDCFilterDecayTime = 0,

	AUNBandEQBandwidth = 5000,
	AUNBandEQBypassBand = 1000,
	AUNBandEQFilterType = 2000,
	AUNBandEQFrequency = 3000,
	AUNBandEQGain = 4000,
	AUNBandEQGlobalGain = 0,
	Mixer3DAzimuth = 0,
	Mixer3DDistance = 2,
	Mixer3DElevation = 1,
	Mixer3DGain = 3,
	Mixer3DGlobalReverbGain = 6,
	Mixer3DMaxGain = 10,
	Mixer3DMinGain = 9,
	Mixer3DObstructionAttenuation = 8,
	Mixer3DOcclusionAttenuation = 7,
	Mixer3DPlaybackRate = 4,
	Mixer3DPostAveragePower = 3000,
	Mixer3DPostPeakHoldLevel = 4000,
	Mixer3DPreAveragePower = 1000,
	Mixer3DPrePeakHoldLevel = 2000,
	Mixer3DReverbBlend = 5,
	RandomBoundA = 0,
	RandomBoundB = 1,
	RandomCurve = 2,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioUnitPropertyIDType</h3>
<p>Added values:</p><pre>
	BiquadCoefficients = 2203,
	BypassVoiceProcessing = 2100,
	LoadAudioFiles = 4101,
	LoadInstrument = 4102,
	MaxNumberOfBands = 2201,
	MuteOutput = 2104,
	NumberOfBands = 2200,
	VoiceProcessingEnableAGC = 2101,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.AudioUnitStatus</h3>
<p>Added values:</p><pre>
	FileNotFound = -43,
</pre>

<h3>Type Changed: MonoMac.AudioUnit.ExtAudioFileError</h3>
<p>Added values:</p><pre>
	BadFilePathError = 561017960,
	FilePermissionError = -54,
	TooManyFilesOpenError = -42,
</pre>

<h3>New Type MonoMac.AudioUnit.AudioComponentStatus</h3>
<pre>
[Serializable]
public enum AudioComponentStatus {
	DuplicateDescription = -66752,
	InitializationTimedOut = -66747,
	InstanceInvalidated = -66749,
	InvalidFormat = -66746,
	NotPermitted = -66748,
	OK = 0,
	TooManyInstances = -66750,
	UnsupportedType = -66751,
}
</pre>
<h3>New Type MonoMac.AudioUnit.AudioUnitClumpID</h3>
<pre>
[Serializable]
public enum AudioUnitClumpID {
	System = 0,
}
</pre>
<h3>New Type MonoMac.AudioUnit.AudioUnitParameterFlag</h3>
<pre>
[Serializable]
[Flags]
public enum AudioUnitParameterFlag {
	CanRamp = 33554432,
	CFNameRelease = 16,
	DisplayCubed = 196608,
	DisplayCubeRoot = 262144,
	DisplayExponential = 327680,
	DisplayLogarithmic = 4194304,
	DisplayMask = 4653056,
	DisplaySquared = 131072,
	DisplaySquareRoot = 65536,
	ExpertMode = 67108864,
	HasCFNameString = 134217728,
	HasClump = 1048576,
	IsElementMeta = 536870912,
	IsGlobalMeta = 268435456,
	IsHighResolution = 8388608,
	IsReadable = 1073741824,
	IsWritable = 2147483648,
	MeterReadOnly = 32768,
	NonRealTime = 16777216,
	PlotHistory = 16384,
	ValuesHaveStrings = 2097152,
}
</pre>
<h3>New Type MonoMac.AudioUnit.AudioUnitParameterInfo</h3>
<pre>
public class AudioUnitParameterInfo {
	// constructors
	public AudioUnitParameterInfo ();
	// properties
	public AudioUnitClumpID ClumpID { get; }
	public float DefaultValue { get; }
	public AudioUnitParameterFlag Flags { get; }
	public float MaxValue { get; }
	public float MinValue { get; }
	public string Name { get; }
	public AudioUnitParameterType Type { get; }
	public AudioUnitParameterUnit Unit { get; }
	public string UnitName { get; }
}
</pre>
<h3>New Type MonoMac.AudioUnit.AudioUnitParameterUnit</h3>
<pre>
[Serializable]
public enum AudioUnitParameterUnit {
	AbsoluteCents = 20,
	Beats = 23,
	Boolean = 2,
	BPM = 22,
	Cents = 9,
	CustomUnit = 26,
	Decibels = 13,
	Degrees = 15,
	EqualPowerCrossfade = 16,
	Generic = 0,
	Hertz = 8,
	Indexed = 1,
	LinearGain = 14,
	Meters = 19,
	MIDIController = 12,
	MIDINoteNumber = 11,
	Milliseconds = 24,
	MixerFaderCurve1 = 17,
	Octaves = 21,
	Pan = 18,
	Percent = 3,
	Phase = 6,
	Rate = 7,
	Ratio = 25,
	RelativeSemiTones = 10,
	SampleFrames = 5,
	Seconds = 4,
}
</pre>
<h3>New Type MonoMac.AudioUnit.AudioUnitRemoteControlEvent</h3>
<pre>
[Serializable]
public enum AudioUnitRemoteControlEvent {
	Rewind = 3,
	TogglePlayPause = 1,
	ToggleRecord = 2,
}
</pre>
<h3>New Type MonoMac.AudioUnit.ClassInfoDictionary</h3>
<pre>
public class ClassInfoDictionary : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public ClassInfoDictionary ();
	public ClassInfoDictionary (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public MonoMac.AudioUnit.AudioComponentManufacturerType? Manufacturer { get; }
	public string Name { get; }
	public MonoMac.AudioUnit.AudioComponentType? Type { get; }
}
</pre>
<h3>New Type MonoMac.AudioUnit.InputDelegate</h3>
<pre>
public sealed delegate InputDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public InputDelegate (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AudioUnitRenderActionFlags actionFlags, MonoMac.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, AudioUnit audioUnit, System.AsyncCallback callback, object object);
	public virtual AudioUnitStatus EndInvoke (System.IAsyncResult result);
	public virtual AudioUnitStatus Invoke (AudioUnitRenderActionFlags actionFlags, MonoMac.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, AudioUnit audioUnit);
}
</pre>
<h3>New Type MonoMac.AudioUnit.InstrumentType</h3>
<pre>
[Serializable]
public enum InstrumentType {
	Audiofile = 3,
	AUPreset = 2,
	DLSPreset = 1,
	EXS24 = 4,
	SF2Preset = 1,
}
</pre>
<h3>New Type MonoMac.AudioUnit.SamplerInstrumentData</h3>
<pre>
public class SamplerInstrumentData {
	// constructors
	public SamplerInstrumentData (MonoMac.CoreFoundation.CFUrl fileUrl, InstrumentType instrumentType);
	// fields
	public static const byte DefaultBankLSB;
	public static const byte DefaultMelodicBankMSB;
	public static const byte DefaultPercussionBankMSB;
	// properties
	public byte BankLSB { get; set; }
	public byte BankMSB { get; set; }
	public MonoMac.CoreFoundation.CFUrl FileUrl { get; }
	public InstrumentType InstrumentType { get; }
	public byte PresetID { get; set; }
}
</pre>

<h2>Namespace MonoMac.AVFoundation</h2>
<h3>Type Changed: MonoMac.AVFoundation.AudioSettings</h3>
<p>Added properties:</p><pre>
	public MonoMac.AVFoundation.AVAudioBitRateStrategy? BitRateStrategy { get; set; }
	public MonoMac.AVFoundation.AVAudioQuality? EncoderAudioQualityForVBR { get; set; }
	public MonoMac.AVFoundation.AVSampleRateConverterAlgorithm? SampleRateConverterAlgorithm { get; set; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetExportSession</h3>
<p>Added methods:</p><pre>
	public static void DetermineCompatibilityOfExportPreset (string presetName, AVAsset asset, string outputFileType, System.Action&lt;bool&gt; isCompatibleResult);
	public static System.Threading.Tasks.Task&lt;bool&gt; DetermineCompatibilityOfExportPresetAsync (string presetName, AVAsset asset, string outputFileType);
	public virtual void DetermineCompatibleFileTypes (System.Action&lt;System.String[]&gt; compatibleFileTypesHandler);
	public virtual System.Threading.Tasks.Task&lt;System.String[]&gt; DetermineCompatibleFileTypesAsync ();
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetImageGenerator</h3>
<p>Added methods:</p><pre>
	public virtual void GenerateCGImagesAsynchronously (MonoMac.Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetReaderAudioMixOutput</h3>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSString AudioTimePitchAlgorithm { get; set; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetReaderVideoCompositionOutput</h3>
<p>Added properties:</p><pre>
	public virtual AVVideoCompositing CustomVideoCompositor { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetTrack</h3>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSString[] AvailableTrackAssociationTypes { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual MonoMac.Foundation.NSString GetAssociatedTracksOfType (MonoMac.Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAssetWriterInput</h3>
<p>Added constructors:</p><pre>
	public AVAssetWriterInput (string mediaType, AVVideoSettingsCompressed outputSettings, MonoMac.CoreMedia.CMFormatDescription sourceFormatHint);
	public AVAssetWriterInput (string mediaType, AudioSettings outputSettings, MonoMac.CoreMedia.CMFormatDescription sourceFormatHint);
	protected AVAssetWriterInput (string mediaType, MonoMac.Foundation.NSDictionary outputSettings, MonoMac.CoreMedia.CMFormatDescription sourceFormatHint);
</pre>
<p>Added properties:</p><pre>
	public virtual string ExtendedLanguageTag { get; set; }
	public virtual string LanguageCode { get; set; }
	public virtual bool MarksOutputTrackAsEnabled { get; set; }
	public virtual System.Drawing.SizeF NaturalSize { get; set; }
	public virtual float PreferredVolume { get; set; }
	public virtual MonoMac.CoreMedia.CMFormatDescription SourceFormatHint { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual void AddTrackAssociationWithTrackOfInput (AVAssetWriterInput input, MonoMac.Foundation.NSString trackAssociationType);
	public virtual bool CanAddTrackAssociationWithTrackOfInput (AVAssetWriterInput input, MonoMac.Foundation.NSString trackAssociationType);
	public static AVAssetWriterInput Create (string mediaType, AVVideoSettingsCompressed outputSettings, MonoMac.CoreMedia.CMFormatDescription sourceFormatHint);
	public static AVAssetWriterInput Create (string mediaType, AudioSettings outputSettings, MonoMac.CoreMedia.CMFormatDescription sourceFormatHint);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVAudioSessionRouteChangeReason</h3>
<p>Removed values:</p><pre>
	NoSuitableRouteForCategory = 6,
	WakeFromSleep = 5,
</pre>
<p>Added values:</p><pre>
	NoSuitableRouteForCategory = 7,
	RouteConfigurationChange = 8,
	WakeFromSleep = 6,
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVCaptureConnection</h3>
<p>Removed properties:</p><pre>
	public bool SupportsVideoMaxFrameDuration { get; }
	public bool SupportsVideoMinFrameDuration { get; }
	public virtual MonoMac.CoreMedia.CMTime VideoMinFrameDuration { get; set; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in iOS7")]
	public bool SupportsVideoMaxFrameDuration { get; }

	[Obsolete ("Deprecated in iOS7")]
	public bool SupportsVideoMinFrameDuration { get; }

	[Obsolete ("Deprecated in iOS7")]
	public virtual MonoMac.CoreMedia.CMTime VideoMinFrameDuration { get; set; }

</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVCaptureInputPort</h3>
<p>Added properties:</p><pre>
	public virtual MonoMac.CoreMedia.CMClock Clock { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVCaptureVideoDataOutput</h3>
<p>Added methods:</p><pre>
	public void SetSampleBufferDelegateQueue (IAVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, MonoMac.CoreFoundation.DispatchQueue sampleBufferCallbackQueue);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate</h3>
<p>Added interfaces:</p><pre>
	IAVCaptureVideoDataOutputSampleBufferDelegate
</pre>
<p>Added methods:</p><pre>
	public virtual void DidDropSampleBuffer (AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVFileType</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString AC3 { get; }
	public static MonoMac.Foundation.NSString MpegLayer3 { get; }
	public static MonoMac.Foundation.NSString SunAU { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVMetadata</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString K3GPUserDataKeyAlbumAndTrack { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyCollection { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyKeywordList { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyMediaClassification { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyMediaRating { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyThumbnail { get; }
	public static MonoMac.Foundation.NSString K3GPUserDataKeyUserRating { get; }
	public static MonoMac.Foundation.NSString KFormatISOUserData { get; }
	public static MonoMac.Foundation.NSString KKeySpaceISOUserData { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVMutableVideoComposition</h3>
<p>Added properties:</p><pre>
	public override MonoMac.ObjCRuntime.Class CustomVideoCompositorClass { get; set; }
</pre>
<p>Added methods:</p><pre>
	public static AVMutableVideoComposition Create (AVAsset asset);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVMutableVideoCompositionLayerInstruction</h3>
<p>Added methods:</p><pre>
	public virtual void SetCrop (System.Drawing.RectangleF cropRectangle, MonoMac.CoreMedia.CMTime time);
	public virtual void SetCrop (System.Drawing.RectangleF startCropRectangle, System.Drawing.RectangleF endCropRectangle, MonoMac.CoreMedia.CMTimeRange timeRange);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVPlayer</h3>
<p>Added properties:</p><pre>
	public virtual bool Muted { get; set; }
	public virtual float Volume { get; set; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItem</h3>
<p>Added constructors:</p><pre>
	public AVPlayerItem (AVAsset asset, MonoMac.Foundation.NSString[] automaticallyLoadedAssetKeys);
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSString AudioTimePitchAlgorithm { get; set; }
	public virtual MonoMac.Foundation.NSString[] AutomaticallyLoadedAssetKeys { get; }
	public virtual AVVideoCompositing CustomVideoCompositor { get; }
	public static MonoMac.Foundation.NSString NewAccessLogEntryNotification { get; }
	public static MonoMac.Foundation.NSString NewErrorLogEntryNotification { get; }
	public static MonoMac.Foundation.NSString PlaybackStalledNotification { get; }
	public virtual bool SeekingWaitsForVideoCompositionRendering { get; set; }
	public virtual AVTextStyleRule[] TextStyleRules { get; set; }
</pre>
<p>Added methods:</p><pre>
	public static AVPlayerItem FromAsset (AVAsset asset, MonoMac.Foundation.NSString[] automaticallyLoadedAssetKeys);
	public virtual bool Seek (MonoMac.Foundation.NSDate date, AVCompletion completion);
	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.Foundation.NSDate date, System.Boolean& result);
	public virtual System.Threading.Tasks.Task&lt;bool&gt; SeekAsync (MonoMac.Foundation.NSDate date);
	public virtual AVMediaSelectionOption SelectedMediaOption (AVMediaSelectionGroup inMediaSelectionGroup);
	public virtual void SelectMediaOption (AVMediaSelectionOption mediaSelectionOption, AVMediaSelectionGroup mediaSelectionGroup);
	public virtual void SelectMediaOptionAutomaticallyInMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
</pre>
<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItem.Notifications</h3>
<p>Added methods:</p><pre>
	public static MonoMac.Foundation.NSObject ObserveNewAccessLogEntry (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
	public static MonoMac.Foundation.NSObject ObserveNewErrorLogEntry (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
	public static MonoMac.Foundation.NSObject ObservePlaybackStalled (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
</pre>


<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItemAccessLogEvent</h3>
<p>Removed properties:</p><pre>
	public virtual int SegmentedDownloadedCount { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual int DownloadOverdue { get; }
	public virtual int MediaRequestsWWAN { get; }
	public virtual int NumberOfMediaRequests { get; }
	public virtual double ObservedBitrateStandardDeviation { get; }
	public virtual double ObservedMaxBitrate { get; }
	public virtual double ObservedMinBitrate { get; }
	public virtual string PlaybackType { get; }
	[Obsolete ("Deprecated in iOS7")]
	public virtual int SegmentedDownloadedCount { get; }

	public virtual double StartupTime { get; }
	public virtual double SwitchBitrate { get; }
	public virtual double TransferDuration { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVPlayerItemTrack</h3>
<p>Added properties:</p><pre>
	public virtual float CurrentVideoFrameRate { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVPlayerLayer</h3>
<p>Added properties:</p><pre>
	public virtual System.Drawing.RectangleF VideoRect { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVUrlAsset</h3>
<p>Added properties:</p><pre>
	public virtual AVAssetResourceLoader ResourceLoader { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideo</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString MaxKeyFrameIntervalDurationKey { get; }
	public static MonoMac.Foundation.NSString ProfileLevelH264BaselineAutoLevel { get; }
	public static MonoMac.Foundation.NSString ProfileLevelH264High40 { get; }
	public static MonoMac.Foundation.NSString ProfileLevelH264High41 { get; }
	public static MonoMac.Foundation.NSString ProfileLevelH264HighAutoLevel { get; }
	public static MonoMac.Foundation.NSString ProfileLevelH264MainAutoLevel { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoCodecSettings</h3>
<p>Removed properties:</p><pre>
	public MonoMac.AVFoundation.AVVideoProfileLevelH264? ProfileLevelH264 { set; }
</pre>
<p>Added properties:</p><pre>
	public MonoMac.AVFoundation.AVVideoProfileLevelH264? ProfileLevelH264 { get; set; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoComposition</h3>
<p>Added properties:</p><pre>
	public virtual MonoMac.ObjCRuntime.Class CustomVideoCompositorClass { get; set; }
</pre>
<p>Added methods:</p><pre>
	public static AVVideoComposition FromAssetProperties (AVAsset asset);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoCompositionCoreAnimationTool</h3>
<p>Added methods:</p><pre>
	public static AVVideoCompositionCoreAnimationTool FromComposedVideoFrames (MonoMac.CoreAnimation.CALayer[] videoLayers, MonoMac.CoreAnimation.CALayer inAnimationlayer);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoCompositionInstruction</h3>
<p>Added properties:</p><pre>
	public virtual bool ContainsTweening { get; }
	public virtual int PassthroughTrackID { get; }
	public virtual MonoMac.Foundation.NSNumber[] RequiredSourceTrackIDs { get; }
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoCompositionLayerInstruction</h3>
<p>Added methods:</p><pre>
	public virtual bool GetCrop (MonoMac.CoreMedia.CMTime time, System.Drawing.RectangleF& startCropRectangle, System.Drawing.RectangleF& endCropRectangle, MonoMac.CoreMedia.CMTimeRange& timeRange);
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoProfileLevelH264</h3>
<p>Added values:</p><pre>
	BaselineAutoLevel = 10,
	High40 = 8,
	High41 = 9,
	HighAutoLevel = 12,
	MainAutoLevel = 11,
</pre>

<h3>Type Changed: MonoMac.AVFoundation.AVVideoSettingsCompressed</h3>
<p>Added properties:</p><pre>
	public System.Double? MaxKeyFrameIntervalDuration { get; set; }
</pre>

<h3>New Type MonoMac.AVFoundation.AVAssetResourceLoader</h3>
<pre>
public class AVAssetResourceLoader : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoader ();
	public AVAssetResourceLoader (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoader (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoader (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAssetResourceLoaderDelegate Delegate { get; }
	public virtual MonoMac.CoreFoundation.DispatchQueue DelegateQueue { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVAssetResourceLoaderDelegate resourceLoaderDelegate, MonoMac.CoreFoundation.DispatchQueue delegateQueue);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetResourceLoaderDelegate</h3>
<pre>
public abstract class AVAssetResourceLoaderDelegate : MonoMac.Foundation.NSObject, IAVAssetResourceLoaderDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoaderDelegate ();
	public AVAssetResourceLoaderDelegate (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoaderDelegate (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoaderDelegate (System.IntPtr handle);
	// methods
	public virtual bool ShouldWaitForLoadingOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetResourceLoaderDelegate_Extensions</h3>
<pre>
public static class AVAssetResourceLoaderDelegate_Extensions {
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetResourceLoadingRequest</h3>
<pre>
public class AVAssetResourceLoadingRequest : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingRequest ();
	public AVAssetResourceLoadingRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoadingRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Finished { get; }
	public virtual MonoMac.Foundation.NSUrlRequest Request { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void FinishLoading (MonoMac.Foundation.NSUrlResponse usingResponse, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSUrlRequest redirect);
	public virtual void FinishLoadingWithError (MonoMac.Foundation.NSError error);
	public virtual MonoMac.Foundation.NSData GetStreamingContentKey (MonoMac.Foundation.NSData appIdentifier, MonoMac.Foundation.NSData contentIdentifier, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSError& error);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetTrackGroup</h3>
<pre>
public class AVAssetTrackGroup : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetTrackGroup ();
	public AVAssetTrackGroup (MonoMac.Foundation.NSCoder coder);
	public AVAssetTrackGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetTrackGroup (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSNumber[] TrackIDs { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetTrackTrackAssociation</h3>
<pre>
public static class AVAssetTrackTrackAssociation {
	// properties
	public static MonoMac.Foundation.NSString AudioFallback { get; }
	public static MonoMac.Foundation.NSString ChapterList { get; }
	public static MonoMac.Foundation.NSString ForcedSubtitlesOnly { get; }
	public static MonoMac.Foundation.NSString SelectionFollower { get; }
	public static MonoMac.Foundation.NSString Timecode { get; }
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAssetWriterInputGroup</h3>
<pre>
public class AVAssetWriterInputGroup : MonoMac.AVFoundation.AVMediaSelectionGroup, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetWriterInputGroup (MonoMac.Foundation.NSCoder coder);
	public AVAssetWriterInputGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetWriterInputGroup (System.IntPtr handle);
	public AVAssetWriterInputGroup (AVAssetWriterInput[] inputs, AVAssetWriterInput defaultInput);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVAssetWriterInput DefaultInput { get; }
	public virtual AVAssetWriterInput[] Inputs { get; }
	// methods
	public static AVAssetWriterInputGroup Create (AVAssetWriterInput[] inputs, AVAssetWriterInput defaultInput);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAsynchronousKeyValueLoading_Extensions</h3>
<pre>
public static class AVAsynchronousKeyValueLoading_Extensions {
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAsynchronousVideoCompositionRequest</h3>
<pre>
public class AVAsynchronousVideoCompositionRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAsynchronousVideoCompositionRequest ();
	public AVAsynchronousVideoCompositionRequest (MonoMac.Foundation.NSCoder coder);
	public AVAsynchronousVideoCompositionRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAsynchronousVideoCompositionRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMTime CompositionTime { get; }
	public virtual AVVideoCompositionRenderContext RenderContext { get; }
	public virtual MonoMac.Foundation.NSNumber[] SourceTrackIDs { get; }
	public virtual AVVideoCompositionInstruction VideoCompositionInstruction { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void FinishCancelledRequest ();
	public virtual void FinishWithComposedVideoFrame (MonoMac.CoreVideo.CVPixelBuffer composedVideoFrame);
	public virtual void FinishWithError (MonoMac.Foundation.NSError error);
	public virtual MonoMac.CoreVideo.CVPixelBuffer SourceFrameByTrackID (int trackID);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAudioBitRateStrategy</h3>
<pre>
[Serializable]
public enum AVAudioBitRateStrategy {
	Constant = 0,
	LongTermAverage = 1,
	Variable = 3,
	VariableConstrained = 2,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAudioPlayerDelegate_Extensions</h3>
<pre>
public static class AVAudioPlayerDelegate_Extensions {
	// methods
	public static void DecoderError (IAVAudioPlayerDelegate This, AVAudioPlayer player, MonoMac.Foundation.NSError error);
	public static void FinishedPlaying (IAVAudioPlayerDelegate This, AVAudioPlayer player, bool flag);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAudioRecorderDelegate_Extensions</h3>
<pre>
public static class AVAudioRecorderDelegate_Extensions {
	// methods
	public static void EncoderError (IAVAudioRecorderDelegate This, AVAudioRecorder recorder, MonoMac.Foundation.NSError error);
	public static void FinishedRecording (IAVAudioRecorderDelegate This, AVAudioRecorder recorder, bool flag);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAudioSessionErrorCode</h3>
<pre>
[Serializable]
public enum AVAudioSessionErrorCode {
	BadParam = -50,
	CannotInterruptOthers = 560557684,
	CannotStartPlaying = 561015905,
	CannotStartRecording = 561145187,
	IncompatibleCategory = 560161140,
	IsBusy = 560030580,
	MediaServicesFailed = 1836282486,
	MissingEntitlement = 1701737535,
	None = 0,
	SiriIsRecording = 1936290409,
	Unspecified = 2003329396,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVAuthorizationStatus</h3>
<pre>
[Serializable]
public enum AVAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate_Extensions</h3>
<pre>
public static class AVCaptureAudioDataOutputSampleBufferDelegate_Extensions {
	// methods
	public static void DidDropSampleBuffer (IAVCaptureAudioDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
	public static void DidOutputSampleBuffer (IAVCaptureAudioDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVCaptureAutoFocusRangeRestriction</h3>
<pre>
[Serializable]
public enum AVCaptureAutoFocusRangeRestriction {
	Far = 2,
	Near = 1,
	None = 0,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions</h3>
<pre>
public static class AVCaptureFileOutputRecordingDelegate_Extensions {
	// methods
	public static void DidStartRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, MonoMac.Foundation.NSObject[] connections);
	public static void FinishedRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, MonoMac.Foundation.NSUrl outputFileUrl, MonoMac.Foundation.NSObject[] connections, MonoMac.Foundation.NSError error);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate_Extensions</h3>
<pre>
public static class AVCaptureVideoDataOutputSampleBufferDelegate_Extensions {
	// methods
	public static void DidDropSampleBuffer (IAVCaptureVideoDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
	public static void DidOutputSampleBuffer (IAVCaptureVideoDataOutputSampleBufferDelegate This, AVCaptureOutput captureOutput, MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, AVCaptureConnection connection);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVEdgeWidths</h3>
<pre>
public struct AVEdgeWidths {
	// constructors
	public AVEdgeWidths (float left, float top, float right, float bottom);
	// fields
	public float Bottom;
	public float Left;
	public float Right;
	public float Top;
	// methods
	public override bool Equals (object other);
	public override int GetHashCode ();
	public static bool op_Equality (AVEdgeWidths left, AVEdgeWidths right);
	public static bool op_Inequality (AVEdgeWidths left, AVEdgeWidths right);
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVFrameRateRange</h3>
<pre>
public class AVFrameRateRange : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVFrameRateRange (MonoMac.Foundation.NSCoder coder);
	public AVFrameRateRange (MonoMac.Foundation.NSObjectFlag t);
	public AVFrameRateRange (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMTime MaxFrameDuration { get; }
	public virtual double MaxFrameRate { get; }
	public virtual MonoMac.CoreMedia.CMTime MinFrameDuration { get; }
	public virtual double MinFrameRate { get; }
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVMediaSelectionGroup</h3>
<pre>
public class AVMediaSelectionGroup : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMediaSelectionGroup ();
	public AVMediaSelectionGroup (MonoMac.Foundation.NSCoder coder);
	public AVMediaSelectionGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVMediaSelectionGroup (System.IntPtr handle);
	// properties
	public virtual bool AllowsEmptySelection { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVMediaSelectionOption[] Options { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual AVMediaSelectionOption GetMediaSelectionOptionForPropertyList (MonoMac.Foundation.NSObject propertyList);
	public static AVMediaSelectionOption[] MediaSelectionOptions (AVMediaSelectionOption[] source, MonoMac.Foundation.NSLocale locale);
	public static AVMediaSelectionOption[] MediaSelectionOptions (AVMediaSelectionOption[] source, MonoMac.Foundation.NSString[] avmediaCharacteristics);
	public static AVMediaSelectionOption[] MediaSelectionOptionsExcludingCharacteristics (AVMediaSelectionOption[] source, MonoMac.Foundation.NSString[] avmediaCharacteristics);
	public static AVMediaSelectionOption[] PlayableMediaSelectionOptions (AVMediaSelectionOption[] source);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVMediaSelectionOption</h3>
<pre>
public class AVMediaSelectionOption : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMediaSelectionOption ();
	public AVMediaSelectionOption (MonoMac.Foundation.NSCoder coder);
	public AVMediaSelectionOption (MonoMac.Foundation.NSObjectFlag t);
	public AVMediaSelectionOption (System.IntPtr handle);
	// properties
	public virtual System.String[] AvailableMetadataFormats { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVMetadataItem[] CommonMetadata { get; }
	public virtual string DisplayName { get; }
	public virtual string ExtendedLanguageTag { get; }
	public virtual MonoMac.Foundation.NSLocale Locale { get; }
	public virtual MonoMac.Foundation.NSNumber[] MediaSubTypes { get; }
	public virtual string MediaType { get; }
	public virtual bool Playable { get; }
	public virtual MonoMac.Foundation.NSObject PropertyList { get; }
	// methods
	public virtual AVMediaSelectionOption AssociatedMediaSelectionOptionInMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual string GetDisplayName (MonoMac.Foundation.NSLocale locale);
	public virtual AVMetadataItem[] GetMetadataForFormat (string format);
	public virtual bool HasMediaCharacteristic (string mediaCharacteristic);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVMetadataItemFilter</h3>
<pre>
public class AVMetadataItemFilter : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMetadataItemFilter (MonoMac.Foundation.NSCoder coder);
	public AVMetadataItemFilter (MonoMac.Foundation.NSObjectFlag t);
	public AVMetadataItemFilter (System.IntPtr handle);
	[Obsolete ("Please use the static ForSharing factory method as this type is not meant to be created directly")]
	public AVMetadataItemFilter ();

	// properties
	public override System.IntPtr ClassHandle { get; }
	public static AVMetadataItemFilter ForSharing { get; }
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPixelAspectRatio</h3>
<pre>
public struct AVPixelAspectRatio {
	// constructors
	public AVPixelAspectRatio (int horizontalSpacing, int verticalSpacing);
	// fields
	public int HorizontalSpacing;
	public int VerticalSpacing;
	// methods
	public override bool Equals (object other);
	public override int GetHashCode ();
	public static bool op_Equality (AVPixelAspectRatio left, AVPixelAspectRatio right);
	public static bool op_Inequality (AVPixelAspectRatio left, AVPixelAspectRatio right);
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemLegibleOutput</h3>
<pre>
public class AVPlayerItemLegibleOutput : MonoMac.AVFoundation.AVPlayerItemOutput, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemLegibleOutput ();
	public AVPlayerItemLegibleOutput (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemLegibleOutput (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemLegibleOutput (System.IntPtr handle);
	public AVPlayerItemLegibleOutput (MonoMac.Foundation.NSNumber[] subtypesFourCCcodes);
	// properties
	public virtual double AdvanceIntervalForDelegateInvocation { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual AVPlayerItemLegibleOutputPushDelegate Delegate { get; }
	public virtual MonoMac.CoreFoundation.DispatchQueue DelegateQueue { get; }
	public virtual MonoMac.Foundation.NSString TextStylingResolution { get; set; }
	public static MonoMac.Foundation.NSString TextStylingResolutionDefault { get; }
	public static MonoMac.Foundation.NSString TextStylingResolutionSourceAndRulesOnly { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void SetDelegate (AVPlayerItemLegibleOutputPushDelegate delegateObject, MonoMac.CoreFoundation.DispatchQueue delegateQueue);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemLegibleOutputPushDelegate</h3>
<pre>
public class AVPlayerItemLegibleOutputPushDelegate : MonoMac.AVFoundation.AVPlayerItemOutputPushDelegate, IAVPlayerItemLegibleOutputPushDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, IAVPlayerItemOutputPushDelegate {
	// constructors
	public AVPlayerItemLegibleOutputPushDelegate ();
	public AVPlayerItemLegibleOutputPushDelegate (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemLegibleOutputPushDelegate (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemLegibleOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void DidOutputAttributedStrings (AVPlayerItemLegibleOutput output, MonoMac.Foundation.NSAttributedString[] strings, MonoMac.CoreMedia.CMSampleBuffer[] nativeSamples, MonoMac.CoreMedia.CMTime itemTime);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemLegibleOutputPushDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemLegibleOutputPushDelegate_Extensions {
	// methods
	public static void DidOutputAttributedStrings (IAVPlayerItemLegibleOutputPushDelegate This, AVPlayerItemLegibleOutput output, MonoMac.Foundation.NSAttributedString[] strings, MonoMac.CoreMedia.CMSampleBuffer[] nativeSamples, MonoMac.CoreMedia.CMTime itemTime);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemOutputPullDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemOutputPullDelegate_Extensions {
	// methods
	public static void OutputMediaDataWillChange (IAVPlayerItemOutputPullDelegate This, AVPlayerItemOutput sender);
	public static void OutputSequenceWasFlushed (IAVPlayerItemOutputPullDelegate This, AVPlayerItemOutput output);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemOutputPushDelegate</h3>
<pre>
public class AVPlayerItemOutputPushDelegate : MonoMac.Foundation.NSObject, IAVPlayerItemOutputPushDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerItemOutputPushDelegate ();
	public AVPlayerItemOutputPushDelegate (MonoMac.Foundation.NSCoder coder);
	public AVPlayerItemOutputPushDelegate (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerItemOutputPushDelegate (System.IntPtr handle);
	// methods
	public virtual void OutputSequenceWasFlushed (AVPlayerItemOutput output);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerItemOutputPushDelegate_Extensions</h3>
<pre>
public static class AVPlayerItemOutputPushDelegate_Extensions {
	// methods
	public static void OutputSequenceWasFlushed (IAVPlayerItemOutputPushDelegate This, AVPlayerItemOutput output);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVPlayerMediaSelectionCriteria</h3>
<pre>
public class AVPlayerMediaSelectionCriteria : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVPlayerMediaSelectionCriteria ();
	public AVPlayerMediaSelectionCriteria (MonoMac.Foundation.NSCoder coder);
	public AVPlayerMediaSelectionCriteria (MonoMac.Foundation.NSObjectFlag t);
	public AVPlayerMediaSelectionCriteria (System.IntPtr handle);
	public AVPlayerMediaSelectionCriteria (System.String[] preferredLanguages, MonoMac.Foundation.NSString[] preferredMediaCharacteristics);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual System.String[] PreferredLanguages { get; }
	public virtual MonoMac.Foundation.NSString[] PreferredMediaCharacteristics { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVSampleRateConverterAlgorithm</h3>
<pre>
[Serializable]
public enum AVSampleRateConverterAlgorithm {
	Mastering = 1,
	Normal = 0,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVSpeechBoundary</h3>
<pre>
[Serializable]
public enum AVSpeechBoundary {
	Immediate = 0,
	Word = 1,
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVSynchronizedLayer</h3>
<pre>
public class AVSynchronizedLayer : MonoMac.CoreAnimation.CALayer, MonoMac.CoreAnimation.ICAMediaTiming, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVSynchronizedLayer ();
	public AVSynchronizedLayer (MonoMac.Foundation.NSCoder coder);
	public AVSynchronizedLayer (MonoMac.Foundation.NSObjectFlag t);
	public AVSynchronizedLayer (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVPlayerItem PlayerItem { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public static AVSynchronizedLayer FromPlayerItem (AVPlayerItem playerItem);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVTextStyleRule</h3>
<pre>
public class AVTextStyleRule : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVTextStyleRule ();
	protected AVTextStyleRule (MonoMac.Foundation.NSDictionary textMarkupAttributes, string textSelector);
	public AVTextStyleRule (MonoMac.CoreMedia.CMTextMarkupAttributes attributes);
	protected AVTextStyleRule (MonoMac.Foundation.NSDictionary textMarkupAttributes);
	public AVTextStyleRule (System.IntPtr handle);
	public AVTextStyleRule (MonoMac.Foundation.NSObjectFlag t);
	public AVTextStyleRule (MonoMac.Foundation.NSCoder coder);
	public AVTextStyleRule (MonoMac.CoreMedia.CMTextMarkupAttributes attributes, string textSelector);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MonoMac.CoreMedia.CMTextMarkupAttributes TextMarkupAttributes { get; }
	public virtual string TextSelector { get; }
	protected virtual MonoMac.Foundation.NSDictionary WeakTextMarkupAttributes { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static AVTextStyleRule[] FromPropertyList (MonoMac.Foundation.NSObject plist);
	public static AVTextStyleRule FromTextMarkupAttributes (MonoMac.CoreMedia.CMTextMarkupAttributes textMarkupAttributes);
	public static AVTextStyleRule FromTextMarkupAttributes (MonoMac.CoreMedia.CMTextMarkupAttributes textMarkupAttributes, string textSelector);
	public static MonoMac.Foundation.NSObject ToPropertyList (AVTextStyleRule[] textStyleRules);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVVideoCompositing</h3>
<pre>
public abstract class AVVideoCompositing : MonoMac.Foundation.NSObject, IAVVideoCompositing, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVVideoCompositing ();
	public AVVideoCompositing (MonoMac.Foundation.NSCoder coder);
	public AVVideoCompositing (MonoMac.Foundation.NSObjectFlag t);
	public AVVideoCompositing (System.IntPtr handle);
	// methods
	public virtual void CancelAllPendingVideoCompositionRequests ();
	public virtual void RenderContextChanged (AVVideoCompositionRenderContext newRenderContext);
	public virtual MonoMac.Foundation.NSDictionary RequiredPixelBufferAttributesForRenderContext ();
	public virtual MonoMac.Foundation.NSDictionary SourcePixelBufferAttributes ();
	public virtual void StartVideoCompositionRequest (AVAsynchronousVideoCompositionRequest asyncVideoCompositionRequest);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVVideoCompositing_Extensions</h3>
<pre>
public static class AVVideoCompositing_Extensions {
	// methods
	public static void CancelAllPendingVideoCompositionRequests (IAVVideoCompositing This);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVVideoCompositionRenderContext</h3>
<pre>
public class AVVideoCompositionRenderContext : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVVideoCompositionRenderContext ();
	public AVVideoCompositionRenderContext (MonoMac.Foundation.NSCoder coder);
	public AVVideoCompositionRenderContext (MonoMac.Foundation.NSObjectFlag t);
	public AVVideoCompositionRenderContext (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual AVEdgeWidths EdgeWidths { get; }
	public virtual bool HighQualityRendering { get; }
	public virtual AVPixelAspectRatio PixelAspectRatio { get; }
	public virtual float RenderScale { get; }
	public virtual MonoMac.CoreGraphics.CGAffineTransform RenderTransform { get; }
	public virtual System.Drawing.SizeF Size { get; }
	public virtual AVVideoComposition VideoComposition { get; }
	// methods
	public virtual MonoMac.CoreVideo.CVPixelBuffer CreatePixelBuffer ();
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.AVFoundation.AVVideoCompositionValidationHandling_Extensions</h3>
<pre>
public static class AVVideoCompositionValidationHandling_Extensions {
	// methods
	public static bool ShouldContinueValidatingAfterFindingEmptyTimeRange (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, MonoMac.CoreMedia.CMTimeRange timeRange);
	public static bool ShouldContinueValidatingAfterFindingInvalidTimeRangeInInstruction (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction);
	public static bool ShouldContinueValidatingAfterFindingInvalidTrackIDInInstruction (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, AVVideoCompositionInstruction videoCompositionInstruction, AVVideoCompositionLayerInstruction layerInstruction, AVAsset asset);
	public static bool ShouldContinueValidatingAfterFindingInvalidValueForKey (IAVVideoCompositionValidationHandling This, AVVideoComposition videoComposition, string key);
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVAssetResourceLoaderDelegate</h3>
<pre>
public interface IAVAssetResourceLoaderDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual bool ShouldWaitForLoadingOfRequestedResource (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVAsynchronousKeyValueLoading</h3>
<pre>
public interface IAVAsynchronousKeyValueLoading : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void LoadValuesAsynchronously (System.String[] keys, MonoMac.Foundation.NSAction handler);
	public virtual AVKeyValueStatus StatusOfValueForKeyerror (string key, System.IntPtr outError);
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVAudioPlayerDelegate</h3>
<pre>
public interface IAVAudioPlayerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVAudioRecorderDelegate</h3>
<pre>
public interface IAVAudioRecorderDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVCaptureAudioDataOutputSampleBufferDelegate</h3>
<pre>
public interface IAVCaptureAudioDataOutputSampleBufferDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVCaptureFileOutputRecordingDelegate</h3>
<pre>
public interface IAVCaptureFileOutputRecordingDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVCaptureVideoDataOutputSampleBufferDelegate</h3>
<pre>
public interface IAVCaptureVideoDataOutputSampleBufferDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVPlayerItemLegibleOutputPushDelegate</h3>
<pre>
public interface IAVPlayerItemLegibleOutputPushDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVPlayerItemOutputPullDelegate</h3>
<pre>
public interface IAVPlayerItemOutputPullDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVPlayerItemOutputPushDelegate</h3>
<pre>
public interface IAVPlayerItemOutputPushDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVVideoCompositing</h3>
<pre>
public interface IAVVideoCompositing : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void RenderContextChanged (AVVideoCompositionRenderContext newRenderContext);
	public virtual MonoMac.Foundation.NSDictionary RequiredPixelBufferAttributesForRenderContext ();
	public virtual MonoMac.Foundation.NSDictionary SourcePixelBufferAttributes ();
	public virtual void StartVideoCompositionRequest (AVAsynchronousVideoCompositionRequest asyncVideoCompositionRequest);
}
</pre>
<h3>New Type MonoMac.AVFoundation.IAVVideoCompositionValidationHandling</h3>
<pre>
public interface IAVVideoCompositionValidationHandling : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

<h2>Namespace MonoMac.CoreAnimation</h2>
<h3>Type Changed: MonoMac.CoreAnimation.CAAction</h3>
<p>Added interfaces:</p><pre>
	ICAAction
</pre>

<h3>Type Changed: MonoMac.CoreAnimation.CAEmitterCell</h3>
<p>Added properties:</p><pre>
	public virtual bool AutoReverses { get; set; }
	public virtual double BeginTime { get; set; }
	public virtual double Duration { get; set; }
	public virtual string FillMode { get; set; }
	public virtual float RepeatCount { get; set; }
	public virtual double RepeatDuration { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeOffset { get; set; }
</pre>

<h3>Type Changed: MonoMac.CoreAnimation.CALayer</h3>
<p>Added properties:</p><pre>
	public virtual bool AllowsEdgeAntialiasing { get; set; }
	public virtual bool AllowsGroupOpacity { get; set; }
</pre>

<h3>New Type MonoMac.CoreAnimation.CAAction_Extensions</h3>
<pre>
public static class CAAction_Extensions {
	// methods
	public static void RunAction (ICAAction This, string eventKey, MonoMac.Foundation.NSObject obj, MonoMac.Foundation.NSDictionary arguments);
}
</pre>
<h3>New Type MonoMac.CoreAnimation.CAEmitterBehavior</h3>
<pre>
public class CAEmitterBehavior : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAEmitterBehavior ();
	public CAEmitterBehavior (MonoMac.Foundation.NSCoder coder);
	public CAEmitterBehavior (MonoMac.Foundation.NSObjectFlag t);
	public CAEmitterBehavior (System.IntPtr handle);
	public CAEmitterBehavior (MonoMac.Foundation.NSString type);
	// properties
	public static MonoMac.Foundation.NSString AlignToMotion { get; }
	public static MonoMac.Foundation.NSString Attractor { get; }
	public static MonoMac.Foundation.NSString[] BehaviorTypes { get; }
	public override System.IntPtr ClassHandle { get; }
	public static MonoMac.Foundation.NSString ColorOverLife { get; }
	public static MonoMac.Foundation.NSString Drag { get; }
	public virtual bool Enabled { get; set; }
	public static MonoMac.Foundation.NSString Light { get; }
	public virtual string Name { get; set; }
	public virtual string Type { get; }
	public static MonoMac.Foundation.NSString ValueOverLife { get; }
	public static MonoMac.Foundation.NSString Wave { get; }
	// methods
	public static CAEmitterBehavior Create (MonoMac.Foundation.NSString type);
}
</pre>
<h3>New Type MonoMac.CoreAnimation.CALayerDelegate_Extensions</h3>
<pre>
public static class CALayerDelegate_Extensions {
	// methods
	public static MonoMac.Foundation.NSObject ActionForLayer (ICALayerDelegate This, CALayer layer, string eventKey);
	public static void DisplayLayer (ICALayerDelegate This, CALayer layer);
	public static void DrawLayer (ICALayerDelegate This, CALayer layer, MonoMac.CoreGraphics.CGContext context);
	public static void LayoutSublayersOfLayer (ICALayerDelegate This, CALayer layer);
}
</pre>
<h3>New Type MonoMac.CoreAnimation.CAMediaTiming</h3>
<pre>
public class CAMediaTiming : MonoMac.Foundation.NSObject, ICAMediaTiming, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAMediaTiming ();
	public CAMediaTiming (MonoMac.Foundation.NSCoder coder);
	public CAMediaTiming (MonoMac.Foundation.NSObjectFlag t);
	public CAMediaTiming (System.IntPtr handle);
	// properties
	public virtual bool AutoReverses { get; set; }
	public virtual double BeginTime { get; set; }
	public virtual double Duration { get; set; }
	public virtual string FillMode { get; set; }
	public virtual float RepeatCount { get; set; }
	public virtual double RepeatDuration { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeOffset { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreAnimation.CAMediaTiming_Extensions</h3>
<pre>
public static class CAMediaTiming_Extensions {
}
</pre>
<h3>New Type MonoMac.CoreAnimation.ICAAction</h3>
<pre>
public interface ICAAction : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.CoreAnimation.ICALayerDelegate</h3>
<pre>
public interface ICALayerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.CoreAnimation.ICAMediaTiming</h3>
<pre>
public interface ICAMediaTiming : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

<h2>Namespace MonoMac.CoreBluetooth</h2>
<h3>Type Changed: MonoMac.CoreBluetooth.CBCentralManager</h3>
<p>Added events:</p><pre>
	public event System.EventHandler&lt;CBWillRestoreEventArgs&gt; WillRestoreState;
</pre>
<p>Removed methods:</p><pre>
	public virtual void RetrieveConnectedPeripherals ();
	public void RetrievePeripherals (System.Guid[] peripheralUuids);
	public void RetrievePeripherals (System.Guid peripheralUuid);
	public void RetrievePeripherals (CBUUID[] peripheralUuids);
	public void ScanForPeripherals (System.Guid[] serviceUuids, MonoMac.Foundation.NSDictionary options);
	public void ScanForPeripherals (System.Guid[] serviceUuids, PeripheralScanningOptions options);
	public void ScanForPeripherals (System.Guid[] serviceUuids);
	public void ScanForPeripherals (System.Guid serviceUuid, MonoMac.Foundation.NSDictionary options);
	public void ScanForPeripherals (System.Guid serviceUuid);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS7")]
	public virtual void RetrieveConnectedPeripherals ();

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid[] peripheralUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid peripheralUuid);

	[Obsolete ("Deprecated in iOS7")]
	public void RetrievePeripherals (CBUUID[] peripheralUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid, MonoMac.Foundation.NSDictionary options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, PeripheralScanningOptions options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, MonoMac.Foundation.NSDictionary options);

</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBCentralManagerDelegate</h3>
<p>Added methods:</p><pre>
	public virtual void WillRestoreState (CBCentralManager central, MonoMac.Foundation.NSDictionary dict);
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBError</h3>
<p>Added values:</p><pre>
	ConnectionFailed = 10,
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBPeripheral</h3>
<p>Removed properties:</p><pre>
	public virtual bool IsConnected { get; }
	public virtual System.IntPtr UUID { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.Foundation.NSUuid Identifier { get; }
	[Obsolete ("Deprecated in iOS7")]
	public virtual bool IsConnected { get; }

	public virtual CBPeripheralState State { get; }
	[Obsolete ("Deprecated in iOS7")]
	public virtual System.IntPtr UUID { get; }

</pre>
<p>Removed events:</p><pre>
	public event System.EventHandler&lt;MonoMac.Foundation.NSErrorEventArgs&gt; DiscoveredService;
	public event System.EventHandler InvalidatedService;
	public event System.EventHandler&lt;MonoMac.Foundation.NSErrorEventArgs&gt; RssiUpdated;
</pre>
<p>Added events:</p><pre>
	public event System.EventHandler&lt;NSErrorEventArgs&gt; DiscoveredService;
	[Obsolete ("Deprecated in iOS7")]
	public event System.EventHandler InvalidatedService;
	public event System.EventHandler&lt;CBPeripheralServicesEventArgs&gt; ModifiedServices;
	public event System.EventHandler&lt;NSErrorEventArgs&gt; RssiUpdated;
</pre>
<p>Removed methods:</p><pre>
	public void DiscoverCharacteristics (System.Guid[] charactersticUUIDs, CBService forService);
	public void DiscoverIncludedServices (System.Guid[] includedServiceUUIDs, CBService forService);
	public void DiscoverServices (System.Guid[] services);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverCharacteristics (System.Guid[] charactersticUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverIncludedServices (System.Guid[] includedServiceUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverServices (System.Guid[] services);

</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBPeripheralDelegate</h3>
<p>Removed methods:</p><pre>
	public virtual void InvalidatedService (CBPeripheral peripheral);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS7")]
	public virtual void InvalidatedService (CBPeripheral peripheral);

	public virtual void ModifiedServices (CBPeripheral peripheral, CBService[] services);
</pre>

<h3>Type Changed: MonoMac.CoreBluetooth.CBUUID</h3>
<p>Added methods:</p><pre>
	public static CBUUID FromNSUuid (MonoMac.Foundation.NSUuid theUUID);
</pre>

<h3>New Type MonoMac.CoreBluetooth.CBCentralManagerDelegate_Extensions</h3>
<pre>
public static class CBCentralManagerDelegate_Extensions {
	// methods
	public static void ConnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral);
	public static void DisconnectedPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoMac.Foundation.NSError error);
	public static void DiscoveredPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoMac.Foundation.NSDictionary advertisementData, MonoMac.Foundation.NSNumber RSSI);
	public static void FailedToConnectPeripheral (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral peripheral, MonoMac.Foundation.NSError error);
	public static void RetrievedConnectedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);
	public static void RetrievedPeripherals (ICBCentralManagerDelegate This, CBCentralManager central, CBPeripheral[] peripherals);
	public static void WillRestoreState (ICBCentralManagerDelegate This, CBCentralManager central, MonoMac.Foundation.NSDictionary dict);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralDelegate_Extensions</h3>
<pre>
public static class CBPeripheralDelegate_Extensions {
	// methods
	public static void DiscoverCharacteristic (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, MonoMac.Foundation.NSError error);
	public static void DiscoveredDescriptor (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoMac.Foundation.NSError error);
	public static void DiscoveredIncludedService (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, MonoMac.Foundation.NSError error);
	public static void DiscoveredService (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoMac.Foundation.NSError error);
	[Obsolete ("Deprecated in iOS7")]
	public static void InvalidatedService (ICBPeripheralDelegate This, CBPeripheral peripheral);

	public static void ModifiedServices (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService[] services);
	public static void RssiUpdated (ICBPeripheralDelegate This, CBPeripheral peripheral, MonoMac.Foundation.NSError error);
	public static void UpdatedCharacterteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoMac.Foundation.NSError error);
	public static void UpdatedName (ICBPeripheralDelegate This, CBPeripheral peripheral);
	public static void UpdatedNotificationState (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoMac.Foundation.NSError error);
	public static void UpdatedValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, MonoMac.Foundation.NSError error);
	public static void WroteCharacteristicValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBCharacteristic characteristic, MonoMac.Foundation.NSError error);
	public static void WroteDescriptorValue (ICBPeripheralDelegate This, CBPeripheral peripheral, CBDescriptor descriptor, MonoMac.Foundation.NSError error);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralManagerAuthorizationStatus</h3>
<pre>
[Serializable]
public enum CBPeripheralManagerAuthorizationStatus {
	Authorized = 3,
	Denied = 2,
	NotDetermined = 0,
	Restricted = 1,
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralServicesEventArgs</h3>
<pre>
public class CBPeripheralServicesEventArgs : System.EventArgs {
	// constructors
	public CBPeripheralServicesEventArgs (CBService[] services);
	// properties
	public CBService[] Services { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBPeripheralState</h3>
<pre>
[Serializable]
public enum CBPeripheralState {
	Connected = 2,
	Connecting = 1,
	Disconnected = 0,
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.CBWillRestoreEventArgs</h3>
<pre>
public class CBWillRestoreEventArgs : System.EventArgs {
	// constructors
	public CBWillRestoreEventArgs (MonoMac.Foundation.NSDictionary dict);
	// properties
	public MonoMac.Foundation.NSDictionary Dict { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.ICBCentralManagerDelegate</h3>
<pre>
public interface ICBCentralManagerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void UpdatedState (CBCentralManager central);
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.ICBPeripheralDelegate</h3>
<pre>
public interface ICBPeripheralDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.CoreBluetooth.NSErrorEventArgs</h3>
<pre>
public class NSErrorEventArgs : System.EventArgs {
	// constructors
	public NSErrorEventArgs (MonoMac.Foundation.NSError error);
	// properties
	public MonoMac.Foundation.NSError Error { get; set; }
}
</pre>

<h2>Namespace MonoMac.CoreData</h2>
<h3>Type Changed: MonoMac.CoreData.NSAttributeDescription</h3>
<p>Added methods:</p><pre>
	[Obsolete ("Use the DefaultValue property")]
	public virtual void SetDefaultValue (MonoMac.Foundation.NSObject value);

</pre>

<h3>Type Changed: MonoMac.CoreData.NSFetchRequest</h3>
<p>Added properties:</p><pre>
	public virtual uint FetchOffset { get; set; }
	public virtual bool IncludesPendingChanges { get; set; }
	public virtual NSPropertyDescription[] PropertiesToFetch { get; set; }
	public virtual bool ReturnsDistinctResults { get; set; }
</pre>

<h3>Type Changed: MonoMac.CoreData.NSManagedObject</h3>
<p>Removed methods:</p><pre>
	public virtual bool ValidateValue (MonoMac.Foundation.NSObject value, string key, MonoMac.Foundation.NSError& error);
</pre>
<p>Added methods:</p><pre>
	public virtual void PrepareForDeletion ();
	public virtual bool ValidateValue (MonoMac.Foundation.NSObject& value, string key, MonoMac.Foundation.NSError& error);
</pre>

<h3>Type Changed: MonoMac.CoreData.NSManagedObjectContext</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString DidSaveNotification { get; }
	public static MonoMac.Foundation.NSString ObjectsDidChangeNotification { get; }
	public static MonoMac.Foundation.NSString WillSaveNotification { get; }
</pre>

<h3>Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString eUbiquitousContainerIdentifierKey { get; }
	public static MonoMac.Foundation.NSString PersistentStoreUbiquitousPeerTokenOption { get; }
	public static MonoMac.Foundation.NSString RebuildFromUbiquitousContentOption { get; }
	public static MonoMac.Foundation.NSString RemoveUbiquitousMetadataOption { get; }
	public static MonoMac.Foundation.NSString StoresWillChangeNotification { get; }
</pre>
<p>Added methods:</p><pre>
	public static bool RemoveUbiquitousContentAndPersistentStore (MonoMac.Foundation.NSUrl storeUrl, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSError& error);
</pre>

<h3>New Type MonoMac.CoreData.NSManagedObjectChangeEventArgs</h3>
<pre>
public class NSManagedObjectChangeEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	// constructors
	public NSManagedObjectChangeEventArgs (MonoMac.Foundation.NSNotification notification);
	// properties
	public MonoMac.Foundation.NSSet DeletedObjects { get; }
	public MonoMac.Foundation.NSSet InsertedObjects { get; }
	public bool InvalidatedAllObjects { get; }
	public MonoMac.Foundation.NSSet InvalidatedObjects { get; }
	public MonoMac.Foundation.NSSet RefreshedObjects { get; }
	public MonoMac.Foundation.NSSet UpdatedObjects { get; }
}
</pre>
<h3>New Type MonoMac.CoreData.NSPersistentStoreCoordinatorStoreChangeEventArgs</h3>
<pre>
public class NSPersistentStoreCoordinatorStoreChangeEventArgs : MonoMac.Foundation.NSNotificationEventArgs {
	// constructors
	public NSPersistentStoreCoordinatorStoreChangeEventArgs (MonoMac.Foundation.NSNotification notification);
	// properties
	public NSPersistentStoreUbiquitousTransitionType EventType { get; }
}
</pre>
<h3>New Type MonoMac.CoreData.NSPersistentStoreUbiquitousTransitionType</h3>
<pre>
[Serializable]
public enum NSPersistentStoreUbiquitousTransitionType {
	AccountAdded = 1,
	AccountRemoved = 2,
	ContentRemoved = 3,
	InitialImportCompleted = 4,
}
</pre>

<h2>Namespace MonoMac.CoreFoundation</h2>
<h3>Type Changed: MonoMac.CoreFoundation.CFRunLoopSource</h3>
<p>Added constructors:</p><pre>
	public CFRunLoopSource (System.IntPtr handle);
	public CFRunLoopSource (System.IntPtr handle, bool ownsHandle);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFStream</h3>
<p>Added properties:</p><pre>
	public DispatchQueue ReadDispatchQueue { get; set; }
	public DispatchQueue WriteDispatchQueue { get; set; }
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFType</h3>
<p>Added methods:</p><pre>
	public static bool Equal (System.IntPtr cf1, System.IntPtr cf2);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.CFUrl</h3>
<p>Added properties:</p><pre>
	public bool IsFileReference { get; }
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.DispatchGroup</h3>
<p>Added methods:</p><pre>
	public void Notify (DispatchQueue queue, MonoMac.Foundation.NSAction action);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.DispatchQueue</h3>
<p>Added properties:</p><pre>
	public static string CurrentQueueLabel { get; }
</pre>
<p>Added methods:</p><pre>
	public void DispatchAfter (DispatchTime when, MonoMac.Foundation.NSAction action);
	public override bool Equals (object other);
	public override int GetHashCode ();
	public static bool op_Equality (DispatchQueue left, DispatchQueue right);
	public static bool op_Inequality (DispatchQueue left, DispatchQueue right);
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.DispatchQueuePriority</h3>
<p>Added values:</p><pre>
	Background = -32768,
</pre>

<h3>Type Changed: MonoMac.CoreFoundation.DispatchTime</h3>
<p>Added constructors:</p><pre>
	public DispatchTime (DispatchTime when, long delta);
</pre>

<h3>New Type MonoMac.CoreFoundation.CFMachPort</h3>
<pre>
public class CFMachPort : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CFMachPort (System.IntPtr handle);
	public CFMachPort (System.IntPtr handle, bool ownsHandle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public bool IsValid { get; }
	public System.IntPtr MachPort { get; }
	// methods
	protected override void ~CFMachPort ();
	public CFRunLoopSource CreateRunLoopSource ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
	public void Invalidate ();
}
</pre>
<h3>New Type MonoMac.CoreFoundation.CFNetwork</h3>
<pre>
public static class CFNetwork {
	// methods
	public static System.Net.IWebProxy GetDefaultProxy ();
	public static CFProxy[] GetProxiesForAutoConfigurationScript (MonoMac.Foundation.NSString proxyAutoConfigurationScript, MonoMac.Foundation.NSUrl targetURL);
	public static CFProxy[] GetProxiesForAutoConfigurationScript (MonoMac.Foundation.NSString proxyAutoConfigurationScript, System.Uri targetUri);
	public static CFProxy[] GetProxiesForUri (System.Uri uri, CFProxySettings proxySettings);
	public static CFProxy[] GetProxiesForURL (MonoMac.Foundation.NSUrl url, CFProxySettings proxySettings);
	public static CFProxySettings GetSystemProxySettings ();
}
</pre>
<h3>New Type MonoMac.CoreFoundation.CFProxy</h3>
<pre>
public class CFProxy {
	// properties
	public MonoMac.Foundation.NSString AutoConfigurationJavaScript { get; }
	public MonoMac.Foundation.NSUrl AutoConfigurationUrl { get; }
	public string HostName { get; }
	public string Password { get; }
	public int Port { get; }
	public CFProxyType ProxyType { get; }
	public string Username { get; }
}
</pre>
<h3>New Type MonoMac.CoreFoundation.CFProxySettings</h3>
<pre>
public class CFProxySettings {
	// properties
	public MonoMac.Foundation.NSDictionary Dictionary { get; }
	public bool HTTPEnable { get; }
	public int HTTPPort { get; }
	public string HTTPProxy { get; }
	public bool ProxyAutoConfigEnable { get; }
	public string ProxyAutoConfigURLString { get; }
}
</pre>
<h3>New Type MonoMac.CoreFoundation.CFProxyType</h3>
<pre>
[Serializable]
public enum CFProxyType {
	AutoConfigurationJavaScript = 2,
	AutoConfigurationUrl = 1,
	FTP = 3,
	HTTP = 4,
	HTTPS = 5,
	None = 0,
	SOCKS = 6,
}
</pre>

<h2>Namespace MonoMac.CoreGraphics</h2>
<h3>Type Changed: MonoMac.CoreGraphics.CGColorSpace</h3>
<p>Added methods:</p><pre>
	public static CGColorSpace CreateICCProfile (System.Single[] range, CGDataProvider profile, CGColorSpace alternate);
	public static CGColorSpace CreateICCProfile (MonoMac.Foundation.NSData data);
	public MonoMac.Foundation.NSData GetICCProfile ();
</pre>

<h3>Type Changed: MonoMac.CoreGraphics.CGContext</h3>
<p>Removed methods:</p><pre>
	public void SelectFont (string name, float size, CGTextEncoding textEncoding);
	public void ShowGlyphs (System.UInt16[] glyphs);
	public void ShowGlyphs (System.UInt16[] glyphs, int count);
	public void ShowGlyphsAtPoint (float x, float y, System.UInt16[] glyphs, int count);
	public void ShowGlyphsAtPoint (float x, float y, System.UInt16[] glyphs);
	public void ShowGlyphsWithAdvances (System.UInt16[] glyphs, System.Drawing.SizeF[] advances, int count);
	public void ShowText (string str, int count);
	public void ShowText (string str);
	public void ShowText (System.Byte[] bytes, int count);
	public void ShowText (System.Byte[] bytes);
	public void ShowTextAtPoint (float x, float y, string str, int length);
	public void ShowTextAtPoint (float x, float y, string str);
</pre>
<p>Added methods:</p><pre>
	public CGBitmapContext AsBitmapContext ();
	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void SelectFont (string name, float size, CGTextEncoding textEncoding);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphs (System.UInt16[] glyphs);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphs (System.UInt16[] glyphs, int count);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsAtPoint (float x, float y, System.UInt16[] glyphs, int count);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsAtPoint (float x, float y, System.UInt16[] glyphs);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowGlyphsWithAdvances (System.UInt16[] glyphs, System.Drawing.SizeF[] advances, int count);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (System.Byte[] bytes);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (System.Byte[] bytes, int count);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (string str, int count);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowText (string str);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowTextAtPoint (float x, float y, string str);

	[Obsolete ("Deprecated in OSX 10.9 and iOS 7.0 in favor of CoreText")]
	public void ShowTextAtPoint (float x, float y, string str, int length);

</pre>

<h3>Type Changed: MonoMac.CoreGraphics.CGContextPDF</h3>
<p>Added constructors:</p><pre>
	public CGContextPDF (CGDataConsumer dataConsumer, System.Drawing.RectangleF mediaBox, CGPDFInfo info);
</pre>

<h3>Type Changed: MonoMac.CoreGraphics.CGImageProperties</h3>
<p>Removed properties:</p><pre>
	public System.Int32? DPIHeight { get; set; }
	public System.Int32? DPIWidth { get; set; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Use the DPIHeightF property")]
	public System.Int32? DPIHeight { get; set; }

	public System.Single? DPIHeightF { get; set; }
	[Obsolete ("Use the DPIWidthF property")]
	public System.Int32? DPIWidth { get; set; }

	public System.Single? DPIWidthF { get; set; }
</pre>

<h3>Type Changed: MonoMac.CoreGraphics.CGPath</h3>
<p>Added methods:</p><pre>
	public void AddRoundedRect (System.Drawing.RectangleF rect, float cornerWidth, float cornerHeight);
	public void AddRoundedRect (CGAffineTransform transform, System.Drawing.RectangleF rect, float cornerWidth, float cornerHeight);
	public static CGPath FromRoundedRect (System.Drawing.RectangleF rectangle, float cornerWidth, float cornerHeight, CGAffineTransform transform);
	public static CGPath FromRoundedRect (System.Drawing.RectangleF rectangle, float cornerWidth, float cornerHeight);
</pre>

<h3>New Type MonoMac.CoreGraphics.CGDataConsumer</h3>
<pre>
public class CGDataConsumer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGDataConsumer (System.IntPtr handle);
	public CGDataConsumer (MonoMac.Foundation.NSMutableData data);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGDataConsumer ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEvent</h3>
<pre>
public sealed class CGEvent : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public CGEvent (MonoMac.Foundation.NSData source);
	// properties
	public CGEventFlags Flags { get; }
	public virtual System.IntPtr Handle { get; }
	public System.Drawing.PointF Location { get; }
	public long MouseEventButtonNumber { get; }
	public long MouseEventClickState { get; }
	public long MouseEventDeltaX { get; }
	public long MouseEventDeltaY { get; }
	public bool MouseEventInstantMouser { get; }
	public long MouseEventNumber { get; }
	public double MouseEventPressure { get; }
	public long MouseEventSubtype { get; }
	// methods
	protected override void ~CGEvent ();
	public static System.IntPtr CGEventTapCreate (CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
	public CGEvent Copy ();
	public static MonoMac.CoreFoundation.CFMachPort CreateTap (CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
	public void Dispose (bool disposing);
	public virtual void Dispose ();
	public static CGEventFlags GetFlags (System.IntPtr eventHandle);
	public MonoMac.Foundation.NSData ToData ();

	// inner types
	public sealed delegate CGEventTapCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CGEvent (object object, System.IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo, System.AsyncCallback callback, object object);
		public virtual System.IntPtr EndInvoke (System.IAsyncResult result);
		public virtual System.IntPtr Invoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo);
	}
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventFlags</h3>
<pre>
[Serializable]
[Flags]
public enum CGEventFlags {
	AlphaShift = 65536,
	Alternate = 524288,
	Command = 1048576,
	Control = 262144,
	Help = 4194304,
	NonCoalesced = 256,
	NumericPad = 2097152,
	SecondaryFn = 8388608,
	Shift = 131072,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventMask</h3>
<pre>
[Serializable]
[Flags]
public enum CGEventMask {
	FlagsChanged = 4096,
	KeyDown = 1024,
	KeyUp = 2048,
	LeftMouseDown = 2,
	LeftMouseDragged = 64,
	LeftMouseUp = 4,
	MouseMoved = 32,
	Null = 1,
	OtherMouseDown = 33554432,
	OtherMouseDragged = 134217728,
	OtherMouseUp = 67108864,
	RightMouseDown = 8,
	RightMouseDragged = 128,
	RightMouseUp = 16,
	ScrollWheel = 4194304,
	TabletPointer = 8388608,
	TabletProximity = 16777216,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventMouseSubtype</h3>
<pre>
[Serializable]
public enum CGEventMouseSubtype {
	Default = 0,
	TabletPoint = 1,
	TabletProximity = 2,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapLocation</h3>
<pre>
[Serializable]
public enum CGEventTapLocation {
	AnnotatedSession = 2,
	HID = 0,
	Session = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapOptions</h3>
<pre>
[Serializable]
public enum CGEventTapOptions {
	Default = 0,
	ListenOnly = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventTapPlacement</h3>
<pre>
[Serializable]
public enum CGEventTapPlacement {
	HeadInsert = 0,
	TailAppend = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGEventType</h3>
<pre>
[Serializable]
public enum CGEventType {
	FlagsChanged = 12,
	KeyDown = 10,
	KeyUp = 11,
	LeftMouseDown = 1,
	LeftMouseDragged = 6,
	LeftMouseUp = 2,
	MouseMoved = 5,
	Null = 0,
	OtherMouseDown = 25,
	OtherMouseDragged = 27,
	OtherMouseUp = 26,
	RightMouseDown = 3,
	RightMouseDragged = 7,
	RightMouseUp = 4,
	ScrollWheel = 22,
	TabletPointer = 23,
	TabletProximity = 24,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGMouseButton</h3>
<pre>
[Serializable]
public enum CGMouseButton {
	Center = 2,
	Left = 0,
	Right = 1,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGScrollEventUnit</h3>
<pre>
[Serializable]
public enum CGScrollEventUnit {
	Line = 1,
	Pixel = 0,
}
</pre>
<h3>New Type MonoMac.CoreGraphics.CGVector</h3>
<pre>
public struct CGVector {
	// constructors
	public CGVector (float dx, float dy);
	// fields
	public float dx;
	public float dy;
	// methods
	public override bool Equals (object other);
	public override int GetHashCode ();
	public static bool op_Equality (CGVector left, CGVector right);
	public static bool op_Inequality (CGVector left, CGVector right);
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.CoreGraphics.NSDictionaryExtensions</h3>
<pre>
public static class NSDictionaryExtensions {
	// methods
	public static bool ToPoint (MonoMac.Foundation.NSDictionary dictionary, System.Drawing.PointF& point);
}
</pre>
<h3>New Type MonoMac.CoreGraphics.PointFExtensions</h3>
<pre>
public static class PointFExtensions {
	// methods
	public static MonoMac.Foundation.NSDictionary ToDictionary (System.Drawing.PointF self);
}
</pre>

<h2>Namespace MonoMac.CoreImage</h2>
<h3>Type Changed: MonoMac.CoreImage.CIBlendWithMask</h3>
<p>Added constructors:</p><pre>
	public CIBlendWithMask (string name);
</pre>

<h3>Type Changed: MonoMac.CoreImage.CIColorCube</h3>
<p>Added constructors:</p><pre>
	public CIColorCube (string name);
</pre>

<h3>Type Changed: MonoMac.CoreImage.CIContext</h3>
<p>Removed methods:</p><pre>
	[Obsolete ("Deprecated in iOS 6.0. Use DrawImage (CIImage, RectangleF, RectangleF) instead")]
	public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);

</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS 6.0. Use DrawImage (CIImage, CGRect, CGRect) instead")]
	public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);

</pre>

<h3>Type Changed: MonoMac.CoreImage.CIDetector</h3>
<p>Added methods:</p><pre>
	public static CIDetector CreateFaceDetector (CIContext context, CIDetectorOptions detectorOptions);
</pre>

<h3>Type Changed: MonoMac.CoreImage.CIFaceFeature</h3>
<p>Added properties:</p><pre>
	public virtual System.Drawing.RectangleF Bounds { get; }
	public virtual float FaceAngle { get; }
	public virtual bool HasFaceAngle { get; }
	public virtual bool HasSmile { get; }
	public virtual bool LeftEyeClosed { get; }
	public virtual bool RightEyeClosed { get; }
</pre>

<h3>Type Changed: MonoMac.CoreImage.CILinearGradient</h3>
<p>Added constructors:</p><pre>
	public CILinearGradient (string name);
</pre>

<h3>Type Changed: MonoMac.CoreImage.CIPerspectiveTransform</h3>
<p>Added constructors:</p><pre>
	public CIPerspectiveTransform (string name);
</pre>

<h3>New Type MonoMac.CoreImage.CIBlendWithAlphaMask</h3>
<pre>
public class CIBlendWithAlphaMask : MonoMac.CoreImage.CIBlendWithMask, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIBlendWithAlphaMask ();
	public CIBlendWithAlphaMask (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIBumpDistortion</h3>
<pre>
public class CIBumpDistortion : MonoMac.CoreImage.CIDistortionFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIBumpDistortion ();
	public CIBumpDistortion (System.IntPtr handle);
	// properties
	public float Scale { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIBumpDistortionLinear</h3>
<pre>
public class CIBumpDistortionLinear : MonoMac.CoreImage.CIDistortionFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIBumpDistortionLinear ();
	public CIBumpDistortionLinear (System.IntPtr handle);
	// properties
	public float Angle { get; set; }
	public float Scale { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIColorClamp</h3>
<pre>
public class CIColorClamp : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorClamp ();
	public CIColorClamp (System.IntPtr handle);
	// properties
	public CIImage Image { get; set; }
	public CIVector InputMaxComponents { get; set; }
	public CIVector InputMinComponents { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIColorCrossPolynomial</h3>
<pre>
public class CIColorCrossPolynomial : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorCrossPolynomial (string name);
	public CIColorCrossPolynomial ();
	public CIColorCrossPolynomial (System.IntPtr handle);
	// properties
	public CIVector BlueCoefficients { get; set; }
	public CIVector GreenCoefficients { get; set; }
	public CIImage Image { get; set; }
	public CIVector RedCoefficients { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIColorCubeWithColorSpace</h3>
<pre>
public class CIColorCubeWithColorSpace : MonoMac.CoreImage.CIColorCube, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorCubeWithColorSpace ();
	public CIColorCubeWithColorSpace (System.IntPtr handle);
	// properties
	public MonoMac.CoreGraphics.CGColorSpace ColorSpace { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIColorPolynomial</h3>
<pre>
public class CIColorPolynomial : MonoMac.CoreImage.CIColorCrossPolynomial, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorPolynomial ();
	public CIColorPolynomial (System.IntPtr handle);
	// properties
	public CIVector AlphaCoefficients { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIConvolution3X3</h3>
<pre>
public class CIConvolution3X3 : MonoMac.CoreImage.CIConvolutionCore, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIConvolution3X3 ();
	public CIConvolution3X3 (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIConvolution5X5</h3>
<pre>
public class CIConvolution5X5 : MonoMac.CoreImage.CIConvolutionCore, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIConvolution5X5 ();
	public CIConvolution5X5 (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIConvolution9Horizontal</h3>
<pre>
public class CIConvolution9Horizontal : MonoMac.CoreImage.CIConvolutionCore, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIConvolution9Horizontal ();
	public CIConvolution9Horizontal (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIConvolution9Vertical</h3>
<pre>
public class CIConvolution9Vertical : MonoMac.CoreImage.CIConvolutionCore, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIConvolution9Vertical ();
	public CIConvolution9Vertical (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIConvolutionCore</h3>
<pre>
public class CIConvolutionCore : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIConvolutionCore (string name);
	public CIConvolutionCore (System.IntPtr handle);
	// properties
	public float Bias { get; set; }
	public CIImage Image { get; set; }
	public CIVector Weights { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIDetectorOptions</h3>
<pre>
public class CIDetectorOptions {
	// constructors
	public CIDetectorOptions ();
	// properties
	public MonoMac.CoreImage.FaceDetectorAccuracy? Accuracy { get; set; }
	public System.Boolean? EyeBlink { get; set; }
	public System.Single? MinFeatureSize { get; set; }
	public System.Boolean? Smile { get; set; }
	public System.Boolean? TrackingEnabled { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffect</h3>
<pre>
public class CIPhotoEffect : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffect (string name);
	public CIPhotoEffect (System.IntPtr handle);
	// properties
	public CIImage Image { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectChrome</h3>
<pre>
public class CIPhotoEffectChrome : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectChrome ();
	public CIPhotoEffectChrome (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectFade</h3>
<pre>
public class CIPhotoEffectFade : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectFade ();
	public CIPhotoEffectFade (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectInstant</h3>
<pre>
public class CIPhotoEffectInstant : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectInstant ();
	public CIPhotoEffectInstant (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectMono</h3>
<pre>
public class CIPhotoEffectMono : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectMono ();
	public CIPhotoEffectMono (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectNoir</h3>
<pre>
public class CIPhotoEffectNoir : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectNoir ();
	public CIPhotoEffectNoir (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectProcess</h3>
<pre>
public class CIPhotoEffectProcess : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectProcess ();
	public CIPhotoEffectProcess (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectTonal</h3>
<pre>
public class CIPhotoEffectTonal : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectTonal ();
	public CIPhotoEffectTonal (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIPhotoEffectTransfer</h3>
<pre>
public class CIPhotoEffectTransfer : MonoMac.CoreImage.CIPhotoEffect, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPhotoEffectTransfer ();
	public CIPhotoEffectTransfer (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.CoreImage.CIQRCodeGenerator</h3>
<pre>
public class CIQRCodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIQRCodeGenerator ();
	public CIQRCodeGenerator (System.IntPtr handle);
	// properties
	public string CorrectionLevel { get; set; }
	public MonoMac.Foundation.NSData Message { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreImage.CIVignetteEffect</h3>
<pre>
public class CIVignetteEffect : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIVignetteEffect ();
	public CIVignetteEffect (System.IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public CIImage Image { get; set; }
	public float Intensity { get; set; }
	public float Radius { get; set; }
}
</pre>

<h2>Namespace MonoMac.CoreLocation</h2>
<h3>Type Changed: MonoMac.CoreLocation.CLError</h3>
<p>Added values:</p><pre>
	RangingFailure = 16,
	RangingUnavailable = 17,
</pre>

<h3>New Type MonoMac.CoreLocation.CLLocationDistance</h3>
<pre>
public static class CLLocationDistance {
	// properties
	public static double FilterNone { get; }
	public static double MaxDistance { get; }
}
</pre>
<h3>New Type MonoMac.CoreLocation.CLProximity</h3>
<pre>
[Serializable]
public enum CLProximity {
	Far = 3,
	Immediate = 1,
	Near = 2,
	Unknown = 0,
}
</pre>
<h3>New Type MonoMac.CoreLocation.CLRegionState</h3>
<pre>
[Serializable]
public enum CLRegionState {
	Inside = 1,
	Outside = 2,
	Unknown = 0,
}
</pre>

<h2>Namespace MonoMac.CoreMedia</h2>
<h3>Type Changed: MonoMac.CoreMedia.CMFormatDescriptionError</h3>
<p>Added values:</p><pre>
	ValueNotAvailable = -12718,
</pre>

<h3>Type Changed: MonoMac.CoreMedia.CMSampleBuffer</h3>
<p>Added methods:</p><pre>
	public CMSampleBufferError CopyPCMDataIntoAudioBufferList (int frameOffset, int numFrames, MonoMac.AudioToolbox.AudioBuffers bufferList);
</pre>

<h3>Type Changed: MonoMac.CoreMedia.CMTime</h3>
<p>Added methods:</p><pre>
	public static CMTime Multiply (CMTime time, int multiplier, int divisor);
</pre>

<h3>New Type MonoMac.CoreMedia.CMBufferCompare</h3>
<pre>
public sealed delegate CMBufferCompare : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferCompare (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.ObjCRuntime.INativeObject first, MonoMac.ObjCRuntime.INativeObject second, System.AsyncCallback callback, object object);
	public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (MonoMac.ObjCRuntime.INativeObject first, MonoMac.ObjCRuntime.INativeObject second);
}
</pre>
<h3>New Type MonoMac.CoreMedia.CMBufferGetBool</h3>
<pre>
public sealed delegate CMBufferGetBool : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferGetBool (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.ObjCRuntime.INativeObject buffer, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (MonoMac.ObjCRuntime.INativeObject buffer);
}
</pre>
<h3>New Type MonoMac.CoreMedia.CMBufferGetSize</h3>
<pre>
public sealed delegate CMBufferGetSize : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferGetSize (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.ObjCRuntime.INativeObject buffer, System.AsyncCallback callback, object object);
	public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (MonoMac.ObjCRuntime.INativeObject buffer);
}
</pre>
<h3>New Type MonoMac.CoreMedia.CMBufferGetTime</h3>
<pre>
public sealed delegate CMBufferGetTime : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferGetTime (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.ObjCRuntime.INativeObject buffer, System.AsyncCallback callback, object object);
	public virtual CMTime EndInvoke (System.IAsyncResult result);
	public virtual CMTime Invoke (MonoMac.ObjCRuntime.INativeObject buffer);
}
</pre>
<h3>New Type MonoMac.CoreMedia.CMBufferQueue</h3>
<pre>
public class CMBufferQueue : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CMBufferQueue ();
	public static CMBufferQueue CreateUnsorted (int count);
	public MonoMac.ObjCRuntime.INativeObject Dequeue ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void Enqueue (MonoMac.ObjCRuntime.INativeObject cftypeBuffer);
	public static CMBufferQueue FromCallbacks (int count, CMBufferGetTime getDecodeTimeStamp, CMBufferGetTime getPresentationTimeStamp, CMBufferGetTime getDuration, CMBufferGetBool isDataReady, CMBufferCompare compare, MonoMac.Foundation.NSString dataBecameReadyNotification, CMBufferGetSize getTotalSize);
	public static CMBufferQueue FromCallbacks (int count, CMBufferGetTime getDecodeTimeStamp, CMBufferGetTime getPresentationTimeStamp, CMBufferGetTime getDuration, CMBufferGetBool isDataReady, CMBufferCompare compare, MonoMac.Foundation.NSString dataBecameReadyNotification);
	public int GetTotalSize ();
}
</pre>

<h2>Namespace MonoMac.CoreMidi</h2>
<h3>Type Changed: MonoMac.CoreMidi.MidiClient</h3>
<p>Removed methods:</p><pre>
	public MidiEndpoint CreateVirtualSource (string name);
</pre>
<p>Added methods:</p><pre>
	public MidiEndpoint CreateVirtualDestination (string name, MidiError& status);
	[Obsolete ("It is better to use CreateVirtualSource (string name, out MidiError statusCode) to flag errors")]
	public MidiEndpoint CreateVirtualSource (string name);

	public MidiEndpoint CreateVirtualSource (string name, MidiError& statusCode);
</pre>


<h2>Namespace MonoMac.CoreServices</h2>
<h3>Type Changed: MonoMac.CoreServices.CFHTTPMessage</h3>
<h3>Type Changed: MonoMac.CoreServices.CFHTTPMessage.AuthenticationScheme</h3>
<p>Added fields:</p><pre>
	public static const CFHTTPMessage.AuthenticationScheme OAuth1;
</pre>



<h2>Namespace MonoMac.CoreVideo</h2>
<h3>Type Changed: MonoMac.CoreVideo.CVPixelFormatDescription</h3>
<p>Removed properties:</p><pre>
	public static MonoMac.Foundation.NSDictionary[] AllTypes { get; }
</pre>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSNumber[] AllTypes { get; }
</pre>
<p>Added methods:</p><pre>
	public static MonoMac.Foundation.NSDictionary Create (CVPixelFormatType pixelFormat);
	public static void Register (MonoMac.Foundation.NSDictionary description, CVPixelFormatType pixelFormat);
</pre>


<h2>Namespace MonoMac.CoreWlan</h2>
<h3>Type Changed: MonoMac.CoreWlan.CWConfiguration</h3>
<p>Added constructors:</p><pre>
	public CWConfiguration (CWConfiguration configuration);
</pre>
<p>Removed properties:</p><pre>
	public virtual bool AlwaysRememberNetworks { get; set; }
	public virtual bool DisconnectOnLogout { get; set; }
	public virtual CWWirelessProfile[] PreferredNetworks { get; set; }
	public virtual MonoMac.Foundation.NSSet RememberedNetworks { get; set; }
	public virtual bool RequireAdminForIBSSCreation { get; set; }
	public virtual bool RequireAdminForNetworkChange { get; set; }
	public virtual bool RequireAdminForPowerChange { get; set; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool AlwaysRememberNetworks { get; set; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool DisconnectOnLogout { get; set; }

	public CWNetworkProfile[] NetworkProfiles { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual CWWirelessProfile[] PreferredNetworks { get; set; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSSet RememberedNetworks { get; set; }

	public virtual bool RememberJoinedNetworks { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool RequireAdminForIBSSCreation { get; set; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool RequireAdminForNetworkChange { get; set; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool RequireAdminForPowerChange { get; set; }

	public virtual bool RequireAdministratorForAssociation { get; }
	public virtual bool RequireAdministratorForIbssMode { get; }
	public virtual bool RequireAdministratorForPower { get; }
</pre>

<h3>Type Changed: MonoMac.CoreWlan.CWInterface</h3>
<p>Removed properties:</p><pre>
	public virtual MonoMac.Foundation.NSData BssidData { get; }
	public virtual MonoMac.Foundation.NSNumber Channel { get; }
	public virtual MonoMac.Foundation.NSNumber InterfaceState { get; }
	public static CWInterface MainInterface { get; }
	public virtual string Name { get; }
	public virtual MonoMac.Foundation.NSNumber Noise { get; }
	public virtual MonoMac.Foundation.NSNumber OpMode { get; }
	public virtual MonoMac.Foundation.NSNumber PhyMode { get; }
	public virtual bool Power { get; }
	public virtual bool PowerSave { get; }
	public virtual MonoMac.Foundation.NSNumber Rssi { get; }
	public virtual MonoMac.Foundation.NSNumber SecurityMode { get; }
	public virtual MonoMac.Foundation.NSNumber[] SupportedChannels { get; }
	public static System.String[] SupportedInterfaces { get; }
	public virtual MonoMac.Foundation.NSNumber[] SupportedPhyModes { get; }
	public virtual bool SupportsAesCcm { get; }
	public virtual bool SupportsHostAP { get; }
	public virtual bool SupportsIbss { get; }
	public virtual bool SupportsMonitorMode { get; }
	public virtual bool SupportsPmgt { get; }
	public virtual bool SupportsShortGI20MHz { get; }
	public virtual bool SupportsShortGI40MHz { get; }
	public virtual bool SupportsTkip { get; }
	public virtual bool SupportsTsn { get; }
	public virtual bool SupportsWep { get; }
	public virtual bool SupportsWme { get; }
	public virtual bool SupportsWow { get; }
	public virtual bool SupportsWpa { get; }
	public virtual bool SupportsWpa2 { get; }
	public virtual MonoMac.Foundation.NSNumber TxPower { get; }
	public virtual MonoMac.Foundation.NSNumber TxRate { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual CWPhyMode ActivePHYMode { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSData BssidData { get; }

	public CWNetwork[] CachedScanResults { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Channel { get; }

	public virtual bool DeviceAttached { get; }
	public virtual string HardwareAddress { get; }
	public virtual CWInterfaceMode InterfaceMode { get; }
	public virtual string InterfaceName { get; }
	public static System.String[] InterfaceNames { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber InterfaceState { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public static CWInterface MainInterface { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual string Name { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Noise { get; }

	public virtual int NoiseMeasurement { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber OpMode { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber PhyMode { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool Power { get; }

	public virtual bool PowerOn { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool PowerSave { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Rssi { get; }

	public virtual int RssiValue { get; }
	public virtual CWSecurity Security { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber SecurityMode { get; }

	public virtual bool ServiceActive { get; }
	public virtual MonoMac.Foundation.NSData SsidData { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber[] SupportedChannels { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public static System.String[] SupportedInterfaces { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber[] SupportedPhyModes { get; }

	public CWChannel[] SupportedWlanChannels { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsAesCcm { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsHostAP { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsIbss { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsMonitorMode { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsPmgt { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsShortGI20MHz { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsShortGI40MHz { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsTkip { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsTsn { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsWep { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsWme { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsWow { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsWpa { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SupportsWpa2 { get; }

	public virtual uint TransmitPower { get; }
	public virtual double TransmitRate { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber TxPower { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber TxRate { get; }

	public virtual CWChannel WlanChannel { get; }
</pre>
<p>Removed methods:</p><pre>
	public virtual bool AssociateToNetwork (CWNetwork network, MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);
	public virtual bool CommitConfiguration (CWConfiguration config, MonoMac.Foundation.NSError& error);
	public virtual bool EnableIBSSWithParameters (MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);
	public static CWInterface FromName (string name);
	public virtual bool IsEqualToInterface (CWInterface intface);
	public virtual CWNetwork[] ScanForNetworksWithParameters (MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);
	public virtual bool SetChannel (uint channel, MonoMac.Foundation.NSError& error);
</pre>
<p>Added methods:</p><pre>
	public virtual bool AssociateToEnterpriseNetwork (CWNetwork network, MonoMac.Security.SecIdentity identity, string username, string password, MonoMac.Foundation.NSError& error);
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool AssociateToNetwork (CWNetwork network, MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);

	public virtual bool AssociateToNetwork (CWNetwork network, string password, MonoMac.Foundation.NSError& error);
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool CommitConfiguration (CWConfiguration config, MonoMac.Foundation.NSError& error);

	public virtual bool CommitConfiguration (CWConfiguration configuration, MonoMac.Foundation.NSObject authorization, MonoMac.Foundation.NSError& error);
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool EnableIBSSWithParameters (MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public static CWInterface FromName (string name);

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool IsEqualToInterface (CWInterface intface);

	public CWNetwork[] ScanForNetworksWithName (string networkName, MonoMac.Foundation.NSError& error);
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual CWNetwork[] ScanForNetworksWithParameters (MonoMac.Foundation.NSDictionary parameters, MonoMac.Foundation.NSError& error);

	public CWNetwork[] ScanForNetworksWithSsid (MonoMac.Foundation.NSData ssid, MonoMac.Foundation.NSError& error);
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool SetChannel (uint channel, MonoMac.Foundation.NSError& error);

	public virtual bool SetPairwiseMasterKey (MonoMac.Foundation.NSData key, MonoMac.Foundation.NSError& error);
	public virtual bool SetWEPKey (MonoMac.Foundation.NSData key, CWCipherKeyFlags flags, uint index, MonoMac.Foundation.NSError& error);
	public virtual bool SetWlanChannel (CWChannel channel, MonoMac.Foundation.NSError& error);
	public virtual bool StartIbssModeWithSsid (MonoMac.Foundation.NSData ssidData, CWIbssModeSecurity security, uint channel, string password, MonoMac.Foundation.NSError& error);
</pre>

<h3>Type Changed: MonoMac.CoreWlan.CWNetwork</h3>
<p>Removed properties:</p><pre>
	public virtual MonoMac.Foundation.NSData BssidData { get; }
	public virtual MonoMac.Foundation.NSNumber Channel { get; }
	public virtual MonoMac.Foundation.NSData IeData { get; }
	public virtual bool IsIBSS { get; }
	public virtual MonoMac.Foundation.NSNumber Noise { get; }
	public virtual MonoMac.Foundation.NSNumber PhyMode { get; }
	public virtual MonoMac.Foundation.NSNumber Rssi { get; }
	public virtual MonoMac.Foundation.NSNumber SecurityMode { get; }
	public virtual CWWirelessProfile WirelessProfile { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual uint BeaconInterval { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSData BssidData { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Channel { get; }

	public virtual string CountryCode { get; }
	public virtual bool Ibss { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSData IeData { get; }

	public virtual MonoMac.Foundation.NSData InformationElementData { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual bool IsIBSS { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Noise { get; }

	public virtual int NoiseMeasurement { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber PhyMode { get; }

	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber Rssi { get; }

	public virtual int RssiValue { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual MonoMac.Foundation.NSNumber SecurityMode { get; }

	public virtual MonoMac.Foundation.NSData SsidData { get; }
	[Obsolete ("Deprecated in Mac OS X 10.7, removed in Mac OS X 10.9")]
	public virtual CWWirelessProfile WirelessProfile { get; }

	public virtual CWChannel WlanChannel { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual bool SupportsPhyMode (CWPhyMode phyMode);
	public virtual bool SupportsSecurity (CWSecurity security);
</pre>

<h3>New Type MonoMac.CoreWlan.CWChannel</h3>
<pre>
public class CWChannel : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CWChannel ();
	public CWChannel (MonoMac.Foundation.NSCoder coder);
	public CWChannel (MonoMac.Foundation.NSObjectFlag t);
	public CWChannel (System.IntPtr handle);
	// properties
	public virtual CWChannelBand ChannelBand { get; }
	public virtual uint ChannelNumber { get; }
	public virtual CWChannelWidth ChannelWidth { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual bool IsEqualToChannel (CWChannel channel);
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWChannelBand</h3>
<pre>
[Serializable]
public enum CWChannelBand {
	FiveGHz = 2,
	TwoGHz = 1,
	Unknown = 0,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWChannelWidth</h3>
<pre>
[Serializable]
public enum CWChannelWidth {
	EightyMHz = 3,
	FourtyMHz = 2,
	OneHundredSixtyMHz = 4,
	TwentyMHz = 1,
	Unknown = 0,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWCipherKeyFlags</h3>
<pre>
[Serializable]
public enum CWCipherKeyFlags {
	Multicast = 4,
	None = 0,
	Rx = 16,
	Tx = 8,
	Unicast = 2,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWIbssModeSecurity</h3>
<pre>
[Serializable]
public enum CWIbssModeSecurity {
	None = 0,
	WEP104 = 2,
	WEP40 = 1,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWInterfaceMode</h3>
<pre>
[Serializable]
public enum CWInterfaceMode {
	HostAP = 3,
	Ibss = 2,
	None = 0,
	Station = 1,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWKeychainDomain</h3>
<pre>
[Serializable]
public enum CWKeychainDomain {
	None = 0,
	System = 2,
	User = 1,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWMutableConfiguration</h3>
<pre>
public class CWMutableConfiguration : MonoMac.CoreWlan.CWConfiguration, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CWMutableConfiguration ();
	public CWMutableConfiguration (MonoMac.Foundation.NSCoder coder);
	public CWMutableConfiguration (MonoMac.Foundation.NSObjectFlag t);
	public CWMutableConfiguration (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool RememberJoinedNetworks { get; set; }
	public virtual bool RequireAdministratorForIbssMode { get; set; }
	public virtual bool RequireAdministratorForPower { get; set; }
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWMutableNetworkProfile</h3>
<pre>
public class CWMutableNetworkProfile : MonoMac.CoreWlan.CWNetworkProfile, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CWMutableNetworkProfile ();
	public CWMutableNetworkProfile (MonoMac.Foundation.NSCoder coder);
	public CWMutableNetworkProfile (MonoMac.Foundation.NSObjectFlag t);
	public CWMutableNetworkProfile (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWNetworkProfile</h3>
<pre>
public class CWNetworkProfile : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CWNetworkProfile ();
	public CWNetworkProfile (MonoMac.Foundation.NSCoder coder);
	public CWNetworkProfile (MonoMac.Foundation.NSObjectFlag t);
	public CWNetworkProfile (System.IntPtr handle);
	public CWNetworkProfile (CWNetworkProfile networkProfile);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual CWSecurity Security { get; }
	public virtual string Ssid { get; }
	public virtual MonoMac.Foundation.NSData SsidData { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual bool IsEqualToNetworkProfile (CWNetworkProfile networkProfile);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
	public static MonoMac.Foundation.NSObject NetworkProfile ();
	public static MonoMac.Foundation.NSObject NetworkProfileWithNetworkProfile (CWNetworkProfile networkProfile);
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWPhyMode</h3>
<pre>
[Serializable]
public enum CWPhyMode {
	A = 1,
	AC = 5,
	B = 2,
	G = 3,
	N = 4,
	None = 0,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWSecurity</h3>
<pre>
[Serializable]
public enum CWSecurity {
	DynamicWEP = 6,
	Enterprise = 10,
	None = 0,
	Personal = 5,
	Unknown = 2147483647,
	WEP = 1,
	WPA2Enterprise = 9,
	WPA2Personal = 4,
	WPAEnterprise = 7,
	WPAEnterpriseMixed = 8,
	WPAPersonal = 2,
	WPAPersonalMixed = 3,
}
</pre>
<h3>New Type MonoMac.CoreWlan.CWStatus</h3>
<pre>
[Serializable]
public enum CWStatus {
	APFull = -3913,
	AssociationDenied = -3909,
	AuthenticationAlgorithmUnsupported = -3910,
	ChallengeFailure = -3912,
	CipherSuiteRejected = -3923,
	DSSSOFDMUnsupported = -3916,
	EAPOL = 1,
	HTFeaturesNotSupported = -3926,
	InvalidAKMP = -3920,
	InvalidAuthenticationSequenceNumber = -3911,
	InvalidFormat = -3904,
	InvalidGroupCipher = -3918,
	InvalidInformationElement = -3917,
	InvalidPairwiseCipher = -3919,
	InvalidParameter = -3900,
	InvalidPMK = -3924,
	InvalidRSNCapabilities = -3922,
	IPCFailure = -3929,
	NoMemory = -3901,
	NotSupported = -3903,
	Ok = 0,
	OperationNotPermitted = -3930,
	PCOTransitionTimeNotSupported = -3927,
	ReassociationDenied = -3908,
	ReferenceNotBound = -3928,
	ShortSlotUnsupported = -3915,
	Status = -3931,
	SupplicantTimeout = -3925,
	Timeout = -3905,
	Unknown = -3902,
	UnspecifiedFailure = -3906,
	UnsupportedCapabilities = -3907,
	UnsupportedRateSet = -3914,
	UnsupportedRSNVersion = -3921,
}
</pre>

<h2>Namespace MonoMac.Foundation</h2>
<h3>Type Changed: MonoMac.Foundation.DictionaryContainer</h3>
<p>Added constructors:</p><pre>
	protected DictionaryContainer ();
	protected DictionaryContainer (NSDictionary dictionary);
</pre>
<p>Removed methods:</p><pre>
	protected string GetNSStringValue (NSString key);
</pre>
<p>Added methods:</p><pre>
	protected NSString GetNSStringValue (NSString key);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSAlignmentOptions</h3>
<p>Removed values:</p><pre>
	RectFlipped = -2147483648,
</pre>
<p>Added values:</p><pre>
	RectFlipped = -9223372036854775808,
</pre>

<h3>Type Changed: MonoMac.Foundation.NSArray</h3>
<p>Added methods:</p><pre>
	public static NSArray FromNSObjects (int count, MonoMac.ObjCRuntime.INativeObject[] items);
	public static NSArray FromNSObjects (MonoMac.ObjCRuntime.INativeObject[] items);
	public T GetItem&lt;T&gt; (int index);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSAttributedString</h3>
<p>Removed properties:</p><pre>
	public virtual string Value { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual System.IntPtr LowLevelValue { get; }
	public string Value { get; }
</pre>
<p>Removed methods:</p><pre>
	public virtual NSDictionary GetAttributes (int location, NSRange& effectiveRange);
</pre>
<p>Added methods:</p><pre>
	public NSDictionary GetAttributes (int location, NSRange& effectiveRange);
	public virtual System.IntPtr LowLevelGetAttributes (int location, NSRange& effectiveRange);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSCalendar</h3>
<p>Removed methods:</p><pre>
	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);
	public virtual NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);
</pre>
<p>Added methods:</p><pre>
	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSCalendarOptions opts);
	public NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);
	public virtual NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSCalendarOptions opts);
	public NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSData</h3>
<p>Added constructors:</p><pre>
	public NSData (string base64String, NSDataBase64DecodingOptions options);
	public NSData (NSData base64Data, NSDataBase64DecodingOptions options);
	public NSData (System.IntPtr bytes, uint length, System.Action&lt;System.IntPtr,System.UInt32&gt; deallocator);
</pre>
<p>Added methods:</p><pre>
	public virtual void EnumerateByteRange (NSDataByteRangeEnumerator enumerator);
	public static NSData FromBytesNoCopy (System.IntPtr bytes, uint size, bool freeWhenDone);
	public static NSData FromBytesNoCopy (System.IntPtr bytes, uint size);
	public virtual NSData GetBase64EncodedData (NSDataBase64EncodingOptions options);
	public virtual string GetBase64EncodedString (NSDataBase64EncodingOptions options);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSDate</h3>
<p>Added methods:</p><pre>
	public virtual string DescriptionWithLocale (NSLocale locale);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSDateFormatter</h3>
<p>Added methods:</p><pre>
	public static string GetDateFormatFromTemplate (string template, uint options, NSLocale locale);
	public static string ToLocalizedString (NSDate date, NSDateFormatterStyle dateStyle, NSDateFormatterStyle timeStyle);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSDecimal</h3>
<p>Added interfaces:</p><pre>
	System.IEquatable&lt;NSDecimal&gt;
</pre>
<p>Added methods:</p><pre>
	public virtual bool Equals (NSDecimal other);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSDecimalNumber</h3>
<p>Added interfaces:</p><pre>
	System.IComparable
	System.IComparable&lt;NSNumber&gt;
</pre>

<h3>Type Changed: MonoMac.Foundation.NSError</h3>
<p>Added properties:</p><pre>
	public static NSString NSUrlErrorDomain { get; }
</pre>

<h3>Type Changed: MonoMac.Foundation.NSException</h3>
<p>Added properties:</p><pre>
	public virtual System.String[] CallStackSymbols { get; }
</pre>

<h3>Type Changed: MonoMac.Foundation.NSExpression</h3>
<p>Added methods:</p><pre>
	public virtual void AllowEvaluation ();
	public static NSExpression FromAnyKey ();
</pre>

<h3>Type Changed: MonoMac.Foundation.NSExpressionType</h3>
<p>Added values:</p><pre>
	AnyKey = 15,
</pre>

<h3>Type Changed: MonoMac.Foundation.NSFileManager</h3>
<p>Added methods:</p><pre>
	public virtual NSUrl GetContainerUrl (string securityApplicationGroupIdentifier);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSKeyedArchiver</h3>
<p>Added properties:</p><pre>
	public static NSString RootObjectKey { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual void SetRequiresSecureCoding (bool requireSecureEncoding);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSKeyedUnarchiver</h3>
<p>Added methods:</p><pre>
	public virtual void SetRequiresSecureCoding (bool requireSecureEncoding);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSLocale</h3>
<p>Added methods:</p><pre>
	public static NSLocale FromLocaleIdentifier (string ident);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSMetadataQuery</h3>
<p>Added properties:</p><pre>
	public virtual NSOperationQueue OperationQueue { get; set; }
	public virtual NSObject[] SearchItems { get; set; }
</pre>
<p>Added methods:</p><pre>
	public virtual void EnumerateResultsUsingBlock (NSMetadataQueryEnumerationCallback callback);
	public virtual void EnumerateResultsWithOptions (NSEnumerationOptions opts, NSMetadataQueryEnumerationCallback block);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSMutableAttributedString</h3>
<p>Removed methods:</p><pre>
	public virtual void SetAttributes (NSDictionary attrs, NSRange range);
</pre>
<p>Added methods:</p><pre>
	public virtual void LowLevelSetAttributes (System.IntPtr dictionaryAttrsHandle, NSRange range);
	public void SetAttributes (NSDictionary attributes, NSRange range);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSMutableData</h3>
<p>Removed constructors:</p><pre>
	public NSMutableData (uint len);
</pre>
<p>Added constructors:</p><pre>
	public NSMutableData (uint capacity);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNetService</h3>
<p>Added properties:</p><pre>
	public virtual NSData TxtRecordData { get; set; }
</pre>
<p>Added events:</p><pre>
	public event System.EventHandler&lt;NSNetServiceConnectionEventArgs&gt; DidAcceptConnection;
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNetServiceDelegate</h3>
<p>Added methods:</p><pre>
	public virtual void DidAcceptConnection (NSNetService sender, NSInputStream inputStream, NSOutputStream outputStream);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNetServiceOptions</h3>
<p>Added values:</p><pre>
	ListenForConnections = 2,
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNotificationQueue</h3>
<p>Removed properties:</p><pre>
	public static NSObject DefaultQueue { get; }
</pre>
<p>Added properties:</p><pre>
	public static NSNotificationQueue DefaultQueue { get; }
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNull</h3>
<p>Added methods:</p><pre>
	public virtual NSObject Copy (NSZone zone);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSNumber</h3>
<p>Added interfaces:</p><pre>
	System.IComparable
	System.IComparable&lt;NSNumber&gt;
</pre>
<p>Added methods:</p><pre>
	public virtual int CompareTo (NSNumber other);
	public virtual int CompareTo (object obj);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSObject</h3>
<p>Removed methods:</p><pre>
	public NSObject Autorelease ();
	public void Release ();
	public NSObject Retain ();
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousAutorelease to avoid this warning")]
	public NSObject Autorelease ();

	public NSObject DangerousAutorelease ();
	public void DangerousRelease ();
	public NSObject DangerousRetain ();
	protected void InitializeHandle (System.IntPtr handle, string initSelector);
	protected void InitializeHandle (System.IntPtr handle);
	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Release method on the underlying object;  Use DangerousRelease to avoid this warning")]
	public void Release ();

	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousRetain to avoid this warning")]
	public NSObject Retain ();

</pre>

<h3>Type Changed: MonoMac.Foundation.NSOrderedSet</h3>
<p>Added methods:</p><pre>
	public override bool Equals (object other);
	public override int GetHashCode ();
</pre>

<h3>Type Changed: MonoMac.Foundation.NSPredicate</h3>
<p>Added methods:</p><pre>
	public virtual void AllowEvaluation ();
	public static NSPredicate FromMetadataQueryString (string query);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSProcessInfo</h3>
<p>Added methods:</p><pre>
	public virtual NSObject BeginActivity (NSActivityOptions options, string reason);
	public virtual void EndActivity (NSObject activity);
	public virtual void PerformActivity (NSActivityOptions options, string reason, NSAction runCode);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSPurgeableData</h3>
<p>Added methods:</p><pre>
	public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSSortDescriptor</h3>
<p>Added methods:</p><pre>
	public virtual void AllowEvaluation ();
</pre>

<h3>Type Changed: MonoMac.Foundation.NSString</h3>
<p>Added constructors:</p><pre>
	public NSString (NSData data, NSStringEncoding encoding);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSTextCheckingResult</h3>
<p>Added methods:</p><pre>
	public virtual NSObject Copy (NSZone zone);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSTimer</h3>
<p>Added properties:</p><pre>
	public virtual double Tolerance { get; set; }
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrl</h3>
<p>Added constructors:</p><pre>
	public NSUrl (System.IntPtr ptrUtf8path, bool isDir, NSUrl baseURL);
</pre>
<p>Added properties:</p><pre>
	public virtual System.IntPtr GetFileSystemRepresentationAsUtf8Ptr { get; }
	public static NSString UbiquitousItemDownloadingErrorKey { get; }
	public static NSString UbiquitousItemDownloadingStatusCurrent { get; }
	public static NSString UbiquitousItemDownloadingStatusDownloaded { get; }
	public static NSString UbiquitousItemDownloadingStatusKey { get; }
	public static NSString UbiquitousItemDownloadingStatusNotDownloaded { get; }
	public static NSString UbiquitousItemUploadingErrorKey { get; }
</pre>
<p>Added methods:</p><pre>
	public static NSUrl FromUTF8Pointer (System.IntPtr ptrUtf8path, bool isDir, NSUrl baseURL);
	public virtual bool GetFileSystemRepresentation (System.IntPtr buffer, int maxBufferLength);
	public virtual void RemoveAllCachedResourceValues ();
	public virtual void RemoveCachedResourceValueForKey (NSString key);
	public virtual void SetTemporaryResourceValue (NSObject value, NSString key);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlConnectionDelegate</h3>
<p>Added methods:</p><pre>
	public virtual void WillSendRequestForAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlCredential</h3>
<p>Removed constructors:</p><pre>
	public NSUrlCredential (System.IntPtr trust, bool ignored);
</pre>
<p>Added constructors:</p><pre>
	[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public NSUrlCredential (System.IntPtr trust, bool ignored);

	public NSUrlCredential (MonoMac.Security.SecTrust trust);
	public NSUrlCredential (MonoMac.Security.SecIdentity identity, MonoMac.Security.SecCertificate[] certificates, NSUrlCredentialPersistence persistence);
</pre>
<p>Removed properties:</p><pre>
	public virtual System.IntPtr Identity { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.Security.SecCertificate[] Certificates { get; }
	[Obsolete ("Use SecIdentity property")]
	public virtual System.IntPtr Identity { get; }

	public MonoMac.Security.SecIdentity SecIdentity { get; }
</pre>
<p>Removed methods:</p><pre>
	public static NSUrlCredential FromTrust (System.IntPtr SecTrustRef_trust);
</pre>
<p>Added methods:</p><pre>
	public static NSUrlCredential FromIdentityCertificatesPersistance (MonoMac.Security.SecIdentity identity, MonoMac.Security.SecCertificate[] certificates, NSUrlCredentialPersistence persistence);
	[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public static NSUrlCredential FromTrust (System.IntPtr trust);

	public static NSUrlCredential FromTrust (MonoMac.Security.SecTrust trust);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlCredentialPersistence</h3>
<p>Added values:</p><pre>
	Synchronizable = 3,
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlCredentialStorage</h3>
<p>Added properties:</p><pre>
	public static NSString ChangedNotification { get; }
	public static NSString RemoveSynchronizableCredentials { get; }
</pre>
<p>Added methods:</p><pre>
	public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace, NSDictionary options);
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlDownload</h3>
<p>Added methods:</p><pre>
	public override string ToString ();
</pre>

<h3>Type Changed: MonoMac.Foundation.NSUrlProtectionSpace</h3>
<p>Added constructors:</p><pre>
	public NSUrlProtectionSpace (string host, int port, string protocol, string realm, string authenticationMethod, bool useProxy);
</pre>
<p>Removed properties:</p><pre>
	public static NSString AuthenticationMethodNegotiat { get; }
	public static NSString AuthenticationMethodNTL { get; }
	public static NSString AuthenticationMethodServerTrus { get; }
	public virtual System.IntPtr ServerTrust { get; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Use AuthenticationMethodNegotiate")]
	public static NSString AuthenticationMethodNegotiat { get; }

	public static NSString AuthenticationMethodNegotiate { get; }
	[Obsolete ("Use AuthenticationMethodNTLM")]
	public static NSString AuthenticationMethodNTL { get; }

	public static NSString AuthenticationMethodNTLM { get; }
	[Obsolete ("Use AuthenticationMethodServerTrust")]
	public static NSString AuthenticationMethodServerTrus { get; }

	public static NSString AuthenticationMethodServerTrust { get; }
	public MonoMac.Security.SecTrust ServerSecTrust { get; }
	[Obsolete ("Use ServerSecTrust")]
	public virtual System.IntPtr ServerTrust { get; }

</pre>

<h3>Type Changed: MonoMac.Foundation.NSUserDefaults</h3>
<p>Removed constructors:</p><pre>
	public NSUserDefaults (string username);
</pre>
<p>Added constructors:</p><pre>
	[Obsolete ("Deprecated in iOS7 and OSX 10.9")]
	public NSUserDefaults (string name);

	public NSUserDefaults (string name, NSUserDefaultsType type);
</pre>
<p>Removed methods:</p><pre>
	public virtual System.String[] PersistentDomainNames ();
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS7 and OSX 10.9")]
	public virtual System.String[] PersistentDomainNames ();

</pre>

<h3>Type Changed: MonoMac.Foundation.NSValue</h3>
<p>Removed properties:</p><pre>
	public virtual System.Drawing.PointF PointFValue { get; }
	public virtual System.Drawing.RectangleF RectangleFValue { get; }
	public virtual System.Drawing.SizeF SizeFValue { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual System.Drawing.PointF CGPointValue { get; }
	public virtual System.Drawing.RectangleF CGRectValue { get; }
	public virtual System.Drawing.SizeF CGSizeValue { get; }
	public System.Drawing.PointF PointFValue { get; }
	public System.Drawing.RectangleF RectangleFValue { get; }
	public System.Drawing.SizeF SizeFValue { get; }
</pre>
<p>Added methods:</p><pre>
	public static NSValue FromCGPoint (System.Drawing.PointF point);
	public static NSValue FromCGRect (System.Drawing.RectangleF rect);
	public static NSValue FromCGSize (System.Drawing.SizeF size);
</pre>

<h3>Type Changed: MonoMac.Foundation.ProtocolAttribute</h3>
<p>Added properties:</p><pre>
	public string Name { get; set; }
	public System.Type WrapperType { get; set; }
</pre>

<h3>New Type MonoMac.Foundation.INSCacheDelegate</h3>
<pre>
public interface INSCacheDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSCoding</h3>
<pre>
public interface INSCoding : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSCopying</h3>
<pre>
public interface INSCopying : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSFileManagerDelegate</h3>
<pre>
public interface INSFileManagerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSFilePresenter</h3>
<pre>
public interface INSFilePresenter : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual NSUrl PresentedItemURL { get; }
}
</pre>
<h3>New Type MonoMac.Foundation.INSKeyedArchiverDelegate</h3>
<pre>
public interface INSKeyedArchiverDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSKeyedUnarchiverDelegate</h3>
<pre>
public interface INSKeyedUnarchiverDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSMachPortDelegate</h3>
<pre>
public interface INSMachPortDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSMetadataQueryDelegate</h3>
<pre>
public interface INSMetadataQueryDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSMutableCopying</h3>
<pre>
public interface INSMutableCopying : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSNetServiceBrowserDelegate</h3>
<pre>
public interface INSNetServiceBrowserDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSNetServiceDelegate</h3>
<pre>
public interface INSNetServiceDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSPortDelegate</h3>
<pre>
public interface INSPortDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSSecureCoding</h3>
<pre>
public interface INSSecureCoding : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSStreamDelegate</h3>
<pre>
public interface INSStreamDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSUrlConnectionDelegate</h3>
<pre>
public interface INSUrlConnectionDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.Foundation.INSUrlConnectionDownloadDelegate</h3>
<pre>
public interface INSUrlConnectionDownloadDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void FinishedDownloading (NSUrlConnection connection, NSUrl destinationUrl);
}
</pre>
<h3>New Type MonoMac.Foundation.NSActivityOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSActivityOptions {
	AutomaticTerminationDisabled = 32768,
	Background = 255,
	IdleDisplaySleepDisabled = 256,
	IdleSystemSleepDisabled = 1048576,
	LatencyCritical = 1095216660480,
	SuddenTerminationDisabled = 16384,
	UserInitiated = 16777215,
}
</pre>
<h3>New Type MonoMac.Foundation.NSCacheDelegate_Extensions</h3>
<pre>
public static class NSCacheDelegate_Extensions {
	// methods
	public static void WillEvictObject (INSCacheDelegate This, NSCache cache, NSObject obj);
}
</pre>
<h3>New Type MonoMac.Foundation.NSCalendarOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSCalendarOptions {
	MatchFirst = 4096,
	MatchLast = 8192,
	MatchNextTime = 1024,
	MatchNextTimePreservingSmallerUnits = 512,
	MatchPreviousTimePreservingSmallerUnits = 256,
	MatchStrictly = 2,
	None = 0,
	SearchBackwards = 4,
	WrapCalendarComponents = 1,
}
</pre>
<h3>New Type MonoMac.Foundation.NSCoding</h3>
<pre>
public class NSCoding : MonoMac.Foundation.NSObject, INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCoding ();
	public NSCoding (NSCoder coder);
	public NSCoding (NSObjectFlag t);
	public NSCoding (System.IntPtr handle);
}
</pre>
<h3>New Type MonoMac.Foundation.NSCoding_Extensions</h3>
<pre>
public static class NSCoding_Extensions {
}
</pre>
<h3>New Type MonoMac.Foundation.NSCopying</h3>
<pre>
public class NSCopying : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCopying ();
	public NSCopying (NSCoder coder);
	public NSCopying (NSObjectFlag t);
	public NSCopying (System.IntPtr handle);
	// methods
	public virtual NSObject Copy (NSZone zone);
}
</pre>
<h3>New Type MonoMac.Foundation.NSCopying_Extensions</h3>
<pre>
public static class NSCopying_Extensions {
	// methods
	public static NSObject Copy (INSCopying This, NSZone zone);
}
</pre>
<h3>New Type MonoMac.Foundation.NSDataBase64DecodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64DecodingOptions {
	IgnoreUnknownCharacters = 1,
	None = 0,
}
</pre>
<h3>New Type MonoMac.Foundation.NSDataBase64EncodingOptions</h3>
<pre>
[Serializable]
[Flags]
public enum NSDataBase64EncodingOptions {
	EndLineWithCarriageReturn = 16,
	EndLineWithLineFeed = 32,
	None = 0,
	SeventySixCharacterLineLength = 2,
	SixtyFourCharacterLineLength = 1,
}
</pre>
<h3>New Type MonoMac.Foundation.NSDataByteRangeEnumerator</h3>
<pre>
public sealed delegate NSDataByteRangeEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSDataByteRangeEnumerator (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.IntPtr bytes, NSRange range, System.Boolean& stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.Boolean& stop, System.IAsyncResult result);
	public virtual void Invoke (System.IntPtr bytes, NSRange range, System.Boolean& stop);
}
</pre>
<h3>New Type MonoMac.Foundation.NSFileManagerDelegate_Extensions</h3>
<pre>
public static class NSFileManagerDelegate_Extensions {
	// methods
	public static bool ShouldCopyItemAtPath (INSFileManagerDelegate This, NSFileManager fm, NSString srcPath, NSString dstPath);
	public static bool ShouldCopyItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldLinkItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldMoveItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string srcPath, string dstPath);
	public static bool ShouldProceedAfterError (INSFileManagerDelegate This, NSFileManager fm, NSDictionary errorInfo);
	public static bool ShouldProceedAfterErrorCopyingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorLinkingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorMovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string srcPath, string dstPath);
	public static bool ShouldProceedAfterErrorRemovingItem (INSFileManagerDelegate This, NSFileManager fileManager, NSError error, string path);
	public static bool ShouldRemoveItemAtPath (INSFileManagerDelegate This, NSFileManager fileManager, string path);
}
</pre>
<h3>New Type MonoMac.Foundation.NSFilePresenter_Extensions</h3>
<pre>
public static class NSFilePresenter_Extensions {
	// methods
	public static void PresentedItemChanged (INSFilePresenter This);
	public static void PresentedItemGainedVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedItemLostVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedItemMoved (INSFilePresenter This, NSUrl newURL);
	public static void PresentedItemResolveConflictVersion (INSFilePresenter This, NSFileVersion version);
	public static void PresentedSubitemAppeared (INSFilePresenter This, NSUrl atUrl);
	public static void PresentedSubitemChanged (INSFilePresenter This, NSUrl url);
	public static void PresentedSubitemGainedVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
	public static void PresentedSubitemLostVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
	public static void PresentedSubitemMoved (INSFilePresenter This, NSUrl oldURL, NSUrl newURL);
	public static void PresentedSubitemResolvedConflictVersion (INSFilePresenter This, NSUrl url, NSFileVersion version);
}
</pre>
<h3>New Type MonoMac.Foundation.NSHost</h3>
<pre>
public class NSHost : MonoMac.Foundation.NSObject, System.IEquatable&lt;NSHost&gt;, System.Collections.Generic.IEnumerable&lt;System.Net.IPAddress&gt;, System.Collections.IEnumerable, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSHost (NSCoder coder);
	public NSHost (NSObjectFlag t);
	public NSHost (System.IntPtr handle);
	// properties
	public System.Net.IPAddress Address { get; }
	public System.Net.IPAddress[] Addresses { get; }
	public override System.IntPtr ClassHandle { get; }
	public static NSHost Current { get; }
	public virtual string LocalizedName { get; }
	public virtual string Name { get; }
	public virtual System.String[] Names { get; }
	// methods
	public virtual bool Equals (NSHost host);
	public override bool Equals (object obj);
	public static NSHost FromAddress (string address);
	public static NSHost FromAddress (System.Net.IPAddress address);
	public static NSHost FromIPHostEntry (System.Net.IPHostEntry hostEntry);
	public static NSHost FromName (string name);
	public virtual System.Collections.Generic.IEnumerator&lt;System.Net.IPAddress&gt; GetEnumerator ();
	public override int GetHashCode ();
	public static System.Net.IPHostEntry op_Explicit (NSHost host);
	public static NSHost op_Explicit (System.Net.IPAddress address);
	public static System.Net.IPAddress op_Explicit (NSHost host);
	public static NSHost op_Explicit (System.Net.IPHostEntry hostEntry);
	public System.Net.IPHostEntry ToIPHostEntry ();
}
</pre>
<h3>New Type MonoMac.Foundation.NSKeyedArchiverDelegate_Extensions</h3>
<pre>
public static class NSKeyedArchiverDelegate_Extensions {
	// methods
	public static void EncodedObject (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject obj);
	public static void Finished (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver);
	public static void Finishing (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver);
	public static void ReplacingObject (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject oldObject, NSObject newObject);
	public static NSObject WillEncode (INSKeyedArchiverDelegate This, NSKeyedArchiver archiver, NSObject obj);
}
</pre>
<h3>New Type MonoMac.Foundation.NSKeyedUnarchiverDelegate_Extensions</h3>
<pre>
public static class NSKeyedUnarchiverDelegate_Extensions {
	// methods
	public static MonoMac.ObjCRuntime.Class CannotDecodeClass (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, string klass, System.String[] classes);
	public static NSObject DecodedObject (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, NSObject obj);
	public static void Finished (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver);
	public static void Finishing (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver);
	public static void ReplacingObject (INSKeyedUnarchiverDelegate This, NSKeyedUnarchiver unarchiver, NSObject oldObject, NSObject newObject);
}
</pre>
<h3>New Type MonoMac.Foundation.NSKeyValueSorting_NSMutableOrderedSet</h3>
<pre>
public static class NSKeyValueSorting_NSMutableOrderedSet {
	// methods
	public static void SortUsingDescriptors (NSMutableOrderedSet This, NSSortDescriptor[] sortDescriptors);
}
</pre>
<h3>New Type MonoMac.Foundation.NSKeyValueSorting_NSOrderedSet</h3>
<pre>
public static class NSKeyValueSorting_NSOrderedSet {
	// methods
	public static NSObject[] GetSortedArray (NSOrderedSet This, NSSortDescriptor[] sortDescriptors);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMachPortDelegate_Extensions</h3>
<pre>
public static class NSMachPortDelegate_Extensions {
	// methods
	public static void MachMessageReceived (INSMachPortDelegate This, System.IntPtr msgHeader);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMetadataQueryDelegate_Extensions</h3>
<pre>
public static class NSMetadataQueryDelegate_Extensions {
	// methods
	public static NSObject ReplacementObjectForResultObject (INSMetadataQueryDelegate This, NSMetadataQuery query, NSMetadataItem result);
	public static NSObject ReplacementValueForAttributevalue (INSMetadataQueryDelegate This, NSMetadataQuery query, string attributeName, NSObject value);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMetadataQueryEnumerationCallback</h3>
<pre>
public sealed delegate NSMetadataQueryEnumerationCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSMetadataQueryEnumerationCallback (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSObject result, uint idx, System.Boolean& stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.Boolean& stop, System.IAsyncResult result);
	public virtual void Invoke (NSObject result, uint idx, System.Boolean& stop);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMutableCopying</h3>
<pre>
public class NSMutableCopying : MonoMac.Foundation.NSObject, INSMutableCopying, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSMutableCopying ();
	public NSMutableCopying (NSCoder coder);
	public NSMutableCopying (NSObjectFlag t);
	public NSMutableCopying (System.IntPtr handle);
	// methods
	public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMutableCopying_Extensions</h3>
<pre>
public static class NSMutableCopying_Extensions {
	// methods
	public static NSObject MutableCopy (INSMutableCopying This, NSZone zone);
}
</pre>
<h3>New Type MonoMac.Foundation.NSMutableString</h3>
<pre>
public class NSMutableString : MonoMac.Foundation.NSString, INSCoding, INSCopying, INSMutableCopying, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSMutableString ();
	public NSMutableString (NSCoder coder);
	public NSMutableString (NSObjectFlag t);
	public NSMutableString (System.IntPtr handle);
	public NSMutableString (int capacity);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void Append (NSString str);
	public virtual void DeleteCharacters (NSRange range);
	public virtual void Insert (NSString str, int index);
	public virtual uint ReplaceOcurrences (NSString target, NSString replacement, NSStringCompareOptions options, NSRange range);
	public virtual void SetString (NSString str);
}
</pre>
<h3>New Type MonoMac.Foundation.NSNetServiceBrowserDelegate_Extensions</h3>
<pre>
public static class NSNetServiceBrowserDelegate_Extensions {
	// methods
	public static void DomainRemoved (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, string domain, bool moreComing);
	public static void FoundDomain (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, string domain, bool moreComing);
	public static void FoundService (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSNetService service, bool moreComing);
	public static void NotSearched (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSDictionary errors);
	public static void SearchStarted (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender);
	public static void SearchStopped (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender);
	public static void ServiceRemoved (INSNetServiceBrowserDelegate This, NSNetServiceBrowser sender, NSNetService service, bool moreComing);
}
</pre>
<h3>New Type MonoMac.Foundation.NSNetServiceConnectionEventArgs</h3>
<pre>
public class NSNetServiceConnectionEventArgs : System.EventArgs {
	// constructors
	public NSNetServiceConnectionEventArgs (NSInputStream inputStream, NSOutputStream outputStream);
	// properties
	public NSInputStream InputStream { get; set; }
	public NSOutputStream OutputStream { get; set; }
}
</pre>
<h3>New Type MonoMac.Foundation.NSNetServiceDelegate_Extensions</h3>
<pre>
public static class NSNetServiceDelegate_Extensions {
	// methods
	public static void AddressResolved (INSNetServiceDelegate This, NSNetService sender);
	public static void DidAcceptConnection (INSNetServiceDelegate This, NSNetService sender, NSInputStream inputStream, NSOutputStream outputStream);
	public static void Published (INSNetServiceDelegate This, NSNetService sender);
	public static void PublishFailure (INSNetServiceDelegate This, NSNetService sender, NSDictionary errors);
	public static void ResolveFailure (INSNetServiceDelegate This, NSNetService sender, NSDictionary errors);
	public static void Stopped (INSNetServiceDelegate This, NSNetService sender);
	public static void UpdatedTxtRecordData (INSNetServiceDelegate This, NSNetService sender, NSData data);
	public static void WillPublish (INSNetServiceDelegate This, NSNetService sender);
	public static void WillResolve (INSNetServiceDelegate This, NSNetService sender);
}
</pre>
<h3>New Type MonoMac.Foundation.NSPortDelegate_Extensions</h3>
<pre>
public static class NSPortDelegate_Extensions {
	// methods
	public static void MessageReceived (INSPortDelegate This, NSPortMessage message);
}
</pre>
<h3>New Type MonoMac.Foundation.NSPredicateSupport_NSMutableOrderedSet</h3>
<pre>
public static class NSPredicateSupport_NSMutableOrderedSet {
	// methods
	public static void FilterUsingPredicate (NSMutableOrderedSet This, NSPredicate p);
}
</pre>
<h3>New Type MonoMac.Foundation.NSPredicateSupport_NSOrderedSet</h3>
<pre>
public static class NSPredicateSupport_NSOrderedSet {
	// methods
	public static NSOrderedSet FilterUsingPredicate (NSOrderedSet This, NSPredicate p);
}
</pre>
<h3>New Type MonoMac.Foundation.NSProgress</h3>
<pre>
public class NSProgress : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSProgress ();
	public NSProgress (NSCoder coder);
	public NSProgress (NSObjectFlag t);
	public NSProgress (System.IntPtr handle);
	public NSProgress (NSProgress parentProgress, NSDictionary userInfo);
	// properties
	public virtual bool Cancellable { get; set; }
	public virtual bool Cancelled { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual long CompletedUnitCount { get; set; }
	public static NSProgress CurrentProgress { get; }
	public static NSString EstimatedTimeRemainingKey { get; }
	public static NSString FileAnimationImageKey { get; }
	public static NSString FileAnimationImageOriginalRectKey { get; }
	public static NSString FileCompletedCountKey { get; }
	public static NSString FileIconKey { get; }
	public static NSString FileOperationKindCopying { get; }
	public static NSString FileOperationKindDecompressingAfterDownloading { get; }
	public static NSString FileOperationKindDownloading { get; }
	public static NSString FileOperationKindKey { get; }
	public static NSString FileOperationKindReceiving { get; }
	public static NSString FileTotalCountKey { get; }
	public static NSString FileURLKey { get; }
	public virtual double FractionCompleted { get; }
	public virtual bool Indeterminate { get; }
	public virtual NSString Kind { get; set; }
	public static NSString KindFile { get; }
	public virtual string LocalizedAdditionalDescription { get; set; }
	public virtual string LocalizedDescription { get; set; }
	public virtual bool Old { get; }
	public virtual bool Pausable { get; set; }
	public virtual bool Paused { get; }
	public static NSString ThroughputKey { get; }
	public virtual long TotalUnitCount { get; set; }
	public virtual NSDictionary UserInfo { get; }
	// methods
	public virtual void AcknowledgeWithSuccess (bool success);
	public static NSObject AddSubscriberForFile (NSUrl url, System.Action&lt;NSProgress&gt; publishingHandler);
	public virtual void BecomeCurrent (long pendingUnitCount);
	public virtual void Cancel ();
	protected override void Dispose (bool disposing);
	public static NSProgress FromTotalUnitCount (long unitCount);
	public virtual void Pause ();
	public virtual void Publish ();
	public static void RemoveSubscriber (NSObject subscriber);
	public virtual void ResignCurrent ();
	public virtual void SetAcknowledgementHandler (System.Action&lt;bool&gt; acknowledgementHandler, string appBundleIdentifier);
	public virtual void SetCancellationHandler (NSAction handler);
	public virtual void SetPauseHandler (NSAction handler);
	public virtual void SetUserInfo (NSObject obj, NSString key);
	public virtual void Unpublish ();
}
</pre>
<h3>New Type MonoMac.Foundation.NSSecureCoding</h3>
<pre>
public class NSSecureCoding {
	// constructors
	public NSSecureCoding ();
	// methods
	public static bool SupportsSecureCoding (System.Type type);
	public static bool SupportsSecureCoding (MonoMac.ObjCRuntime.Class klass);
}
</pre>
<h3>New Type MonoMac.Foundation.NSSecureCoding_Extensions</h3>
<pre>
public static class NSSecureCoding_Extensions {
}
</pre>
<h3>New Type MonoMac.Foundation.NSSortDescriptorSorting_NSMutableArray</h3>
<pre>
public static class NSSortDescriptorSorting_NSMutableArray {
	// methods
	public static void SortUsingDescriptors (NSMutableArray This, NSSortDescriptor[] sortDescriptors);
}
</pre>
<h3>New Type MonoMac.Foundation.NSStreamDelegate_Extensions</h3>
<pre>
public static class NSStreamDelegate_Extensions {
	// methods
	public static void HandleEvent (INSStreamDelegate This, NSStream theStream, NSStreamEvent streamEvent);
}
</pre>
<h3>New Type MonoMac.Foundation.NSTextWritingDirection</h3>
<pre>
[Serializable]
[Flags]
public enum NSTextWritingDirection {
	Embedding = 0,
	Override = 2,
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlComponents</h3>
<pre>
public class NSUrlComponents : MonoMac.Foundation.NSObject, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlComponents ();
	public NSUrlComponents (NSCoder coder);
	public NSUrlComponents (NSObjectFlag t);
	public NSUrlComponents (System.IntPtr handle);
	public NSUrlComponents (NSUrl url, bool resolveAgainstBaseUrl);
	public NSUrlComponents (string urlString);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual string Fragment { get; set; }
	public virtual string Host { get; set; }
	public virtual string Password { get; set; }
	public virtual string Path { get; set; }
	public virtual string PercentEncodedFragment { get; set; }
	public virtual string PercentEncodedHost { get; set; }
	public virtual string PercentEncodedPassword { get; set; }
	public virtual string PercentEncodedPath { get; set; }
	public virtual string PercentEncodedQuery { get; set; }
	public virtual string PercentEncodedUser { get; set; }
	public virtual NSNumber Port { get; set; }
	public virtual string Query { get; set; }
	public virtual string Scheme { get; set; }
	public virtual NSUrl Url { get; }
	public virtual string User { get; set; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public static NSUrlComponents FromString (string urlString);
	public static NSUrlComponents FromUrl (NSUrl url, bool resolvingAgainstBaseUrl);
	public virtual NSUrl GetRelativeUrl (NSUrl baseUrl);
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlConnectionDelegate_Extensions</h3>
<pre>
public static class NSUrlConnectionDelegate_Extensions {
	// methods
	public static bool CanAuthenticateAgainstProtectionSpace (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlProtectionSpace protectionSpace);
	public static void CanceledAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public static bool ConnectionShouldUseCredentialStorage (INSUrlConnectionDelegate This, NSUrlConnection connection);
	public static void FailedWithError (INSUrlConnectionDelegate This, NSUrlConnection connection, NSError error);
	public static void FinishedLoading (INSUrlConnectionDelegate This, NSUrlConnection connection);
	public static NSInputStream NeedNewBodyStream (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request);
	public static void ReceivedAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public static void ReceivedData (INSUrlConnectionDelegate This, NSUrlConnection connection, NSData data);
	public static void ReceivedResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlResponse response);
	public static void SentBodyData (INSUrlConnectionDelegate This, NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public static NSCachedUrlResponse WillCacheResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public static NSUrlRequest WillSendRequest (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
	public static void WillSendRequestForAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlConnectionDownloadDelegate_Extensions</h3>
<pre>
public static class NSUrlConnectionDownloadDelegate_Extensions {
	// methods
	public static void ResumedDownloading (INSUrlConnectionDownloadDelegate This, NSUrlConnection connection, long totalBytesWritten, long expectedTotalBytes);
	public static void WroteData (INSUrlConnectionDownloadDelegate This, NSUrlConnection connection, long bytesWritten, long totalBytesWritten, long expectedTotalBytes);
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlErrorCancelledReason</h3>
<pre>
[Serializable]
public enum NSUrlErrorCancelledReason {
	BackgroundUpdatesDisabled = 1,
	UserForceQuitApplication = 0,
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlSessionAuthChallengeDisposition</h3>
<pre>
[Serializable]
public enum NSUrlSessionAuthChallengeDisposition {
	CancelAuthenticationChallenge = 2,
	PerformDefaultHandling = 1,
	RejectProtectionSpace = 3,
	UseCredential = 0,
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlSessionResponseDisposition</h3>
<pre>
[Serializable]
public enum NSUrlSessionResponseDisposition {
	Allow = 1,
	BecomeDownload = 2,
	Cancel = 0,
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlSessionTaskState</h3>
<pre>
[Serializable]
public enum NSUrlSessionTaskState {
	Canceling = 2,
	Completed = 3,
	Running = 0,
	Suspended = 1,
}
</pre>
<h3>New Type MonoMac.Foundation.NSUrlUtilities_NSCharacterSet</h3>
<pre>
public static class NSUrlUtilities_NSCharacterSet {
	// properties
	public static NSCharacterSet UrlFragmentAllowedCharacterSet { get; }
	public static NSCharacterSet UrlHostAllowedCharacterSet { get; }
	public static NSCharacterSet UrlPasswordAllowedCharacterSet { get; }
	public static NSCharacterSet UrlPathAllowedCharacterSet { get; }
	public static NSCharacterSet UrlQueryAllowedCharacterSet { get; }
	public static NSCharacterSet UrlUserAllowedCharacterSet { get; }
}
</pre>
<h3>New Type MonoMac.Foundation.NSURLUtilities_NSString</h3>
<pre>
public static class NSURLUtilities_NSString {
	// methods
	public static NSString CreateStringByAddingPercentEncoding (NSString This, NSCharacterSet allowedCharacters);
	public static NSString CreateStringByAddingPercentEscapes (NSString This, NSStringEncoding enc);
	public static NSString CreateStringByRemovingPercentEncoding (NSString This);
	public static NSString CreateStringByReplacingPercentEscapes (NSString This, NSStringEncoding enc);
}
</pre>
<h3>New Type MonoMac.Foundation.NSUserDefaultsType</h3>
<pre>
[Serializable]
public enum NSUserDefaultsType {
	SuiteName = 1,
	UserName = 0,
}
</pre>
<h3>New Type MonoMac.Foundation.NSZone</h3>
<pre>
public class NSZone : MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public NSZone (System.IntPtr handle);
	// fields
	public static NSZone Default;
	// properties
	public virtual System.IntPtr Handle { get; }
	public string Name { get; set; }
}
</pre>

<h2>Namespace MonoMac.GameKit</h2>
<h3>Type Changed: MonoMac.GameKit.GKAchievement</h3>
<p>Removed methods:</p><pre>
	public virtual void ReportAchievement (GKNotificationHandler completionHandler);
	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual void ReportAchievement (GKNotificationHandler completionHandler);

	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual System.Threading.Tasks.Task ReportAchievementAsync ();

</pre>

<h3>Type Changed: MonoMac.GameKit.GKAchievementDescription</h3>
<p>Removed properties:</p><pre>
	public virtual MonoMac.AppKit.NSImage Image { get; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual MonoMac.AppKit.NSImage Image { get; }

</pre>

<h3>Type Changed: MonoMac.GameKit.GKError</h3>
<p>Removed values:</p><pre>
	Offline = 19,
</pre>
<p>Added values:</p><pre>
	ChallengeInvalid = 19,
	Offline = 25,
	TurnBasedInvalidParticipant = 22,
	TurnBasedInvalidState = 24,
	TurnBasedInvalidTurn = 23,
	TurnBasedMatchDataTooLarge = 20,
	TurnBasedTooManySessions = 21,
</pre>

<h3>Type Changed: MonoMac.GameKit.GKInviteHandler</h3>
<p>Removed methods:</p><pre>
	public virtual System.IAsyncResult BeginInvoke (GKInvite invite, System.String[] players, System.AsyncCallback callback, object object);
	public virtual void Invoke (GKInvite invite, System.String[] players);
</pre>
<p>Added methods:</p><pre>
	public virtual System.IAsyncResult BeginInvoke (GKInvite invite, System.String[] playerIDs, System.AsyncCallback callback, object object);
	public virtual void Invoke (GKInvite invite, System.String[] playerIDs);
</pre>

<h3>Type Changed: MonoMac.GameKit.GKLeaderboard</h3>
<p>Removed methods:</p><pre>
	public static void SetDefaultLeaderboard (string categoryID, GKNotificationHandler notificationHandler);
	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string categoryID);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0")]
	public static void SetDefaultLeaderboard (string leaderboardIdentifier, GKNotificationHandler notificationHandler);

	[Obsolete ("Deprecated in iOS 7.0")]
	public static System.Threading.Tasks.Task SetDefaultLeaderboardAsync (string leaderboardIdentifier);

</pre>

<h3>Type Changed: MonoMac.GameKit.GKLeaderboardViewController</h3>
<p>Removed constructors:</p><pre>
	public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);
</pre>
<p>Added constructors:</p><pre>
	[Obsolete ("Apple never shipped the `initWithTimeScope:playerScope:` selector. Use the default constructor.")]
	public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);

</pre>

<h3>Type Changed: MonoMac.GameKit.GKScore</h3>
<p>Removed constructors:</p><pre>
	public GKScore (string category);
</pre>
<p>Removed properties:</p><pre>
	public virtual string category { get; set; }
</pre>
<p>Added properties:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual string category { get; set; }

</pre>
<p>Removed methods:</p><pre>
	public virtual void IssueChallengeToPlayers (System.String[] playerIDs, string message);
	public virtual void ReportScore (GKNotificationHandler errorHandler);
	public virtual System.Threading.Tasks.Task ReportScoreAsync ();
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual void IssueChallengeToPlayers (System.String[] playerIDs, string message);

	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual void ReportScore (GKNotificationHandler errorHandler);

	[Obsolete ("Deprecated in iOS 7.0")]
	public virtual System.Threading.Tasks.Task ReportScoreAsync ();

</pre>

<h3>New Type MonoMac.GameKit.GKAchievementChallenge</h3>
<pre>
public class GKAchievementChallenge : MonoMac.GameKit.GKChallenge, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKAchievementChallenge ();
	public GKAchievementChallenge (MonoMac.Foundation.NSCoder coder);
	public GKAchievementChallenge (MonoMac.Foundation.NSObjectFlag t);
	public GKAchievementChallenge (System.IntPtr handle);
	// properties
	public virtual GKAchievement Achievement { get; }
	public override System.IntPtr ClassHandle { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.GameKit.GKAchievementViewControllerDelegate_Extensions</h3>
<pre>
public static class GKAchievementViewControllerDelegate_Extensions {
	// methods
	public static void DidFinish (IGKAchievementViewControllerDelegate This, GKAchievementViewController viewController);
}
</pre>
<h3>New Type MonoMac.GameKit.GKChallenge</h3>
<pre>
public class GKChallenge : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKChallenge ();
	public GKChallenge (MonoMac.Foundation.NSCoder coder);
	public GKChallenge (MonoMac.Foundation.NSObjectFlag t);
	public GKChallenge (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDate CompletionDate { get; }
	public virtual MonoMac.Foundation.NSDate IssueDate { get; }
	public virtual string IssuingPlayerID { get; }
	public virtual string Message { get; }
	public virtual string ReceivingPlayerID { get; }
	public virtual GKChallengeState State { get; }
	// methods
	public virtual void Decline ();
	protected override void Dispose (bool disposing);
	public static void LoadReceivedChallenges (System.Action&lt;GKChallenge[],MonoMac.Foundation.NSError&gt; completionHandler);
	public static System.Threading.Tasks.Task&lt;GKChallenge[]&gt; LoadReceivedChallengesAsync ();
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.GameKit.GKChallengeState</h3>
<pre>
[Serializable]
public enum GKChallengeState {
	Completed = 2,
	Declined = 3,
	Invalid = 0,
	Pending = 1,
}
</pre>
<h3>New Type MonoMac.GameKit.GKFriendRequestComposeViewControllerDelegate_Extensions</h3>
<pre>
public static class GKFriendRequestComposeViewControllerDelegate_Extensions {
}
</pre>
<h3>New Type MonoMac.GameKit.GKLeaderboardViewControllerDelegate_Extensions</h3>
<pre>
public static class GKLeaderboardViewControllerDelegate_Extensions {
	// methods
	public static void DidFinish (IGKLeaderboardViewControllerDelegate This, GKLeaderboardViewController viewController);
}
</pre>
<h3>New Type MonoMac.GameKit.GKMatchDelegate_Extensions</h3>
<pre>
public static class GKMatchDelegate_Extensions {
	// methods
	public static void ConnectionFailed (IGKMatchDelegate This, GKMatch match, string playerId, MonoMac.Foundation.NSError error);
	public static void Failed (IGKMatchDelegate This, GKMatch match, MonoMac.Foundation.NSError error);
	public static bool ShouldReinvitePlayer (IGKMatchDelegate This, GKMatch match, string playerId);
	public static void StateChanged (IGKMatchDelegate This, GKMatch match, string playerId, GKPlayerConnectionState state);
}
</pre>
<h3>New Type MonoMac.GameKit.GKMatchmakerViewControllerDelegate_Extensions</h3>
<pre>
public static class GKMatchmakerViewControllerDelegate_Extensions {
	// methods
	public static void ReceivedAcceptFromHostedPlayer (IGKMatchmakerViewControllerDelegate This, GKMatchmakerViewController viewController, string playerID);
}
</pre>
<h3>New Type MonoMac.GameKit.GKScoreChallenge</h3>
<pre>
public class GKScoreChallenge : MonoMac.GameKit.GKChallenge, MonoMac.Foundation.INSCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public GKScoreChallenge ();
	public GKScoreChallenge (MonoMac.Foundation.NSCoder coder);
	public GKScoreChallenge (MonoMac.Foundation.NSObjectFlag t);
	public GKScoreChallenge (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual GKScore Score { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.GameKit.GKTurnBasedEventHandlerDelegate_Extensions</h3>
<pre>
public static class GKTurnBasedEventHandlerDelegate_Extensions {
	// methods
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, GKPlayer[] playersToInvite);
	public static void HandleMatchEnded (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match);
	public static void HandleTurnEventForMatch (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match);
}
</pre>
<h3>New Type MonoMac.GameKit.GKTurnBasedExchange</h3>
<pre>
public class GKTurnBasedExchange {
	// constructors
	public GKTurnBasedExchange ();
	// methods
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.GameKit.GKTurnBasedExchangeReply</h3>
<pre>
public class GKTurnBasedExchangeReply {
	// constructors
	public GKTurnBasedExchangeReply ();
	// methods
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.GameKit.GKTurnBasedExchangeStatus</h3>
<pre>
[Serializable]
public enum GKTurnBasedExchangeStatus {
	Active = 1,
	Canceled = 4,
	Complete = 2,
	Resolved = 3,
	Unknown = 0,
}
</pre>
<h3>New Type MonoMac.GameKit.GKTurnBasedMatchmakerViewControllerDelegate_Extensions</h3>
<pre>
public static class GKTurnBasedMatchmakerViewControllerDelegate_Extensions {
}
</pre>
<h3>New Type MonoMac.GameKit.IGKAchievementViewControllerDelegate</h3>
<pre>
public interface IGKAchievementViewControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.GameKit.IGKFriendRequestComposeViewControllerDelegate</h3>
<pre>
public interface IGKFriendRequestComposeViewControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidFinish (GKFriendRequestComposeViewController viewController);
}
</pre>
<h3>New Type MonoMac.GameKit.IGKLeaderboardViewControllerDelegate</h3>
<pre>
public interface IGKLeaderboardViewControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.GameKit.IGKMatchDelegate</h3>
<pre>
public interface IGKMatchDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DataReceived (GKMatch match, MonoMac.Foundation.NSData data, string playerId);
}
</pre>
<h3>New Type MonoMac.GameKit.IGKMatchmakerViewControllerDelegate</h3>
<pre>
public interface IGKMatchmakerViewControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void DidFailWithError (GKMatchmakerViewController viewController, MonoMac.Foundation.NSError error);
	public virtual void DidFindMatch (GKMatchmakerViewController viewController, GKMatch match);
	public virtual void DidFindPlayers (GKMatchmakerViewController viewController, System.String[] playerIDs);
	public virtual void WasCancelled (GKMatchmakerViewController viewController);
}
</pre>
<h3>New Type MonoMac.GameKit.IGKTurnBasedEventHandlerDelegate</h3>
<pre>
public interface IGKTurnBasedEventHandlerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.GameKit.IGKTurnBasedMatchmakerViewControllerDelegate</h3>
<pre>
public interface IGKTurnBasedMatchmakerViewControllerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void FailedWithError (GKTurnBasedMatchmakerViewController viewController, MonoMac.Foundation.NSError error);
	public virtual void FoundMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
	public virtual void PlayerQuitForMatch (GKTurnBasedMatchmakerViewController viewController, GKTurnBasedMatch match);
	public virtual void WasCancelled (GKTurnBasedMatchmakerViewController viewController);
}
</pre>

<h2>Namespace MonoMac.ImageIO</h2>
<h3>Type Changed: MonoMac.ImageIO.CGImageDestination</h3>
<p>Added methods:</p><pre>
	public void AddImageAndMetadata (MonoMac.CoreGraphics.CGImage image, CGImageMetadata meta, MonoMac.Foundation.NSDictionary options);
	public void AddImageAndMetadata (MonoMac.CoreGraphics.CGImage image, CGImageMetadata meta, CGImageDestinationOptions options);
	public bool CopyImageSource (CGImageSource image, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSError& error);
	public bool CopyImageSource (CGImageSource image, CGImageDestinationOptions options, MonoMac.Foundation.NSError& error);
</pre>

<h3>Type Changed: MonoMac.ImageIO.CGImageDestinationOptions</h3>
<p>Added properties:</p><pre>
	public System.DateTime? DateTime { get; set; }
	public bool MergeMetadata { get; set; }
	public CGImageMetadata Metadata { get; set; }
	public System.Int32? Orientation { get; set; }
	public bool ShouldExcludeXMP { get; set; }
</pre>

<h3>Type Changed: MonoMac.ImageIO.CGImageOptions</h3>
<p>Added properties:</p><pre>
	public bool ShouldCacheImmediately { get; set; }
</pre>

<h3>Type Changed: MonoMac.ImageIO.CGImageProperties</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString ExifISOSpeed { get; }
	public static MonoMac.Foundation.NSString ExifISOSpeedLatitudeYyy { get; }
	public static MonoMac.Foundation.NSString ExifISOSpeedLatitudeZzz { get; }
	public static MonoMac.Foundation.NSString ExifRecommendedExposureIndex { get; }
	public static MonoMac.Foundation.NSString ExifSensitivityType { get; }
	public static MonoMac.Foundation.NSString ExifStandardOutputSensitivity { get; }
</pre>

<h3>New Type MonoMac.ImageIO.CGImageMetadata</h3>
<pre>
public class CGImageMetadata : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGImageMetadata (System.IntPtr handle);
	public CGImageMetadata (MonoMac.Foundation.NSData data);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGImageMetadata ();
	public CGImageMetadataTag CopyTagMatchingImageProperty (MonoMac.Foundation.NSString dictionaryName, MonoMac.Foundation.NSString propertyName);
	public MonoMac.Foundation.NSData CreateXMPData ();
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public void EnumerateTags (MonoMac.Foundation.NSString rootPath, CGImageMetadataEnumerateOptions options, CGImageMetadataTagBlock block);
	public MonoMac.Foundation.NSString GetStringValue (CGImageMetadata parent, MonoMac.Foundation.NSString path);
	public MonoMac.Foundation.NSString GetTag (CGImageMetadata parent, MonoMac.Foundation.NSString path);
	public CGImageMetadataTag[] GetTags ();
	public static int GetTypeID ();
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataEnumerateOptions</h3>
<pre>
public class CGImageMetadataEnumerateOptions {
	// constructors
	public CGImageMetadataEnumerateOptions ();
	// properties
	public bool Recursive { get; set; }
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataErrors</h3>
<pre>
[Serializable]
public enum CGImageMetadataErrors {
	BadArgument = 2,
	ConflictingArguments = 3,
	PrefixConflict = 4,
	Unknown = 0,
	UnsupportedFormat = 1,
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataTag</h3>
<pre>
public class CGImageMetadataTag : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGImageMetadataTag (System.IntPtr handle);
	public CGImageMetadataTag (MonoMac.Foundation.NSString xmlns, MonoMac.Foundation.NSString prefix, MonoMac.Foundation.NSString name, CGImageMetadataType type, MonoMac.Foundation.NSObject value);
	public CGImageMetadataTag (MonoMac.Foundation.NSString xmlns, MonoMac.Foundation.NSString prefix, MonoMac.Foundation.NSString name, CGImageMetadataType type, bool value);
	// properties
	public virtual System.IntPtr Handle { get; }
	public MonoMac.Foundation.NSString Name { get; }
	public MonoMac.Foundation.NSString Namespace { get; }
	public MonoMac.Foundation.NSString Prefix { get; }
	public CGImageMetadataType Type { get; }
	public MonoMac.Foundation.NSObject Value { get; }
	// methods
	protected override void ~CGImageMetadataTag ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CGImageMetadataTag[] GetQualifiers ();
	public static int GetTypeID ();
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataTagBlock</h3>
<pre>
public sealed delegate CGImageMetadataTagBlock : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CGImageMetadataTagBlock (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.Foundation.NSString path, CGImageMetadataTag tag, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (System.IAsyncResult result);
	public virtual bool Invoke (MonoMac.Foundation.NSString path, CGImageMetadataTag tag);
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataTagNamespaces</h3>
<pre>
public static class CGImageMetadataTagNamespaces {
	// properties
	public static MonoMac.Foundation.NSString DublinCore { get; }
	public static MonoMac.Foundation.NSString Exif { get; }
	public static MonoMac.Foundation.NSString ExifAux { get; }
	public static MonoMac.Foundation.NSString ExifEx { get; }
	public static MonoMac.Foundation.NSString IPTCCore { get; }
	public static MonoMac.Foundation.NSString Photoshop { get; }
	public static MonoMac.Foundation.NSString TIFF { get; }
	public static MonoMac.Foundation.NSString XMPBasic { get; }
	public static MonoMac.Foundation.NSString XMPRights { get; }
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataTagPrefixes</h3>
<pre>
public static class CGImageMetadataTagPrefixes {
	// properties
	public static MonoMac.Foundation.NSString DublinCore { get; }
	public static MonoMac.Foundation.NSString Exif { get; }
	public static MonoMac.Foundation.NSString ExifAux { get; }
	public static MonoMac.Foundation.NSString ExifEx { get; }
	public static MonoMac.Foundation.NSString IPTCCore { get; }
	public static MonoMac.Foundation.NSString Photoshop { get; }
	public static MonoMac.Foundation.NSString TIFF { get; }
	public static MonoMac.Foundation.NSString XMPBasic { get; }
	public static MonoMac.Foundation.NSString XMPRights { get; }
}
</pre>
<h3>New Type MonoMac.ImageIO.CGImageMetadataType</h3>
<pre>
[Serializable]
public enum CGImageMetadataType {
	AlternateArray = 4,
	AlternateText = 5,
	ArrayOrdered = 3,
	ArrayUnordered = 2,
	Default = 0,
	Invalid = -1,
	String = 1,
	Structure = 6,
}
</pre>
<h3>New Type MonoMac.ImageIO.CGMutableImageMetadata</h3>
<pre>
public class CGMutableImageMetadata : MonoMac.ImageIO.CGImageMetadata, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGMutableImageMetadata ();
	public CGMutableImageMetadata (CGImageMetadata metadata);
	// methods
	public bool RegisterNamespace (MonoMac.Foundation.NSString xmlns, MonoMac.Foundation.NSString prefix, MonoMac.Foundation.NSError& error);
	public bool RemoveTag (CGImageMetadataTag parent, MonoMac.Foundation.NSString path);
	public bool SetTag (CGImageMetadataTag parent, MonoMac.Foundation.NSString path, CGImageMetadataTag tag);
	public bool SetValue (CGImageMetadataTag parent, MonoMac.Foundation.NSString path, MonoMac.Foundation.NSObject value);
	public bool SetValue (CGImageMetadataTag parent, MonoMac.Foundation.NSString path, bool value);
	public bool SetValueMatchingImageProperty (MonoMac.Foundation.NSString dictionaryName, MonoMac.Foundation.NSString propertyName, MonoMac.Foundation.NSObject value);
	public bool SetValueMatchingImageProperty (MonoMac.Foundation.NSString dictionaryName, MonoMac.Foundation.NSString propertyName, bool value);
}
</pre>

<h2>Namespace MonoMac.ImageKit</h2>
<h3>Type Changed: MonoMac.ImageKit.IKFilterBrowserPanel</h3>
<p>Removed constructors:</p><pre>
	public IKFilterBrowserPanel (IKFilterBrowserPanelStyleMask styleMask);
</pre>
<p>Added methods:</p><pre>
	public static IKFilterBrowserPanel Create (IKFilterBrowserPanelStyleMask styleMask);
</pre>


<h2>Namespace MonoMac.ObjCRuntime</h2>
<h3>Type Changed: MonoMac.ObjCRuntime.ArgumentSemantic</h3>
<p>Added values:</p><pre>
	Strong = 2,
	UnsafeUnretained = 0,
	Weak = 3,
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.LionAttribute</h3>
<p>Added methods:</p><pre>
	public override string ToString ();
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.MountainLionAttribute</h3>
<p>Added methods:</p><pre>
	public override string ToString ();
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.Runtime</h3>
<p>Added methods:</p><pre>
	public static System.Delegate GetDelegateForBlock (System.IntPtr methodPtr, System.Type type);
	public static T GetNSObject&lt;T&gt; (System.IntPtr ptr);
	public static System.IntPtr GetProtocol (string protocol);
</pre>

<h3>Type Changed: MonoMac.ObjCRuntime.SinceAttribute</h3>
<p>Added methods:</p><pre>
	public override string ToString ();
</pre>

<h3>New Type MonoMac.ObjCRuntime.AvailabilityAttribute</h3>
<pre>
public class AvailabilityAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public AvailabilityAttribute ();
	public AvailabilityAttribute (Platform introduced, Platform deprecated, Platform obsoleted, Platform unavailable);
	// properties
	public bool AlwaysAvailable { get; }
	public Platform Deprecated { get; set; }
	public Platform Introduced { get; set; }
	public string Message { get; set; }
	public Platform Obsoleted { get; set; }
	public Platform Unavailable { get; set; }
	// methods
	public static AvailabilityAttribute Get (System.Reflection.MemberInfo member);
	public static AvailabilityAttribute Merge (System.Collections.Generic.IEnumerable&lt;object&gt; attrs);
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.BlockProxyAttribute</h3>
<pre>
public class BlockProxyAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public BlockProxyAttribute (System.Type t);
	// properties
	public System.Type Type { get; set; }
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.LinkTarget</h3>
<pre>
[Serializable]
[Flags]
public enum LinkTarget {
	Arm64 = 32,
	ArmV6 = 2,
	ArmV7 = 4,
	ArmV7s = 16,
	Simulator = 1,
	Simulator64 = 64,
	Thumb = 8,
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.LinkWithAttribute</h3>
<pre>
public class LinkWithAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public LinkWithAttribute (string libraryName, LinkTarget target, string linkerFlags);
	public LinkWithAttribute (string libraryName, LinkTarget target);
	public LinkWithAttribute (string libraryName);
	// properties
	public bool ForceLoad { get; set; }
	public string Frameworks { get; set; }
	public bool IsCxx { get; set; }
	public string LibraryName { get; }
	public string LinkerFlags { get; set; }
	public LinkTarget LinkTarget { get; set; }
	public bool NeedsGccExceptionHandling { get; set; }
	public bool SmartLink { get; set; }
	public string WeakFrameworks { get; set; }
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.MavericksAttribute</h3>
<pre>
public sealed class MavericksAttribute : MonoMac.ObjCRuntime.AvailabilityAttribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public MavericksAttribute ();
	// methods
	public override string ToString ();
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.NativeAttribute</h3>
<pre>
public sealed class NativeAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public NativeAttribute ();
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.NSStringStruct</h3>
<pre>
public struct NSStringStruct {
	// fields
	public System.IntPtr ClassPtr;
	public int Flags;
	public int Length;
	public static System.IntPtr ReferencePtr;
	public System.Char* UnicodePtr;
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.Platform</h3>
<pre>
[Serializable]
[Flags]
public enum Platform {
	iOS = 4294967295,
	iOS_2_0 = 131072,
	iOS_3_0 = 196608,
	iOS_3_2 = 197120,
	iOS_4_0 = 262144,
	iOS_4_1 = 262400,
	iOS_4_2 = 262656,
	iOS_4_3 = 262912,
	iOS_5_0 = 327680,
	iOS_5_1 = 327936,
	iOS_6_0 = 393216,
	iOS_6_1 = 393472,
	iOS_7_0 = 458752,
	iOS_7_1 = 459008,
	Mac = 18446744069414584320,
	Mac_10_10 = 2825744883384320,
	Mac_10_6 = 2821346836873216,
	Mac_10_7 = 2822446348500992,
	Mac_10_8 = 2823545860128768,
	Mac_10_9 = 2824645371756544,
	None = 0,
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.PlatformHelper</h3>
<pre>
public static class PlatformHelper {
	// methods
	public static int CompareIos (Platform a, Platform b);
	public static int CompareMac (Platform a, Platform b);
	public static Platform GetHostApiPlatform ();
	public static bool IsIos (Platform platform);
	public static bool IsMac (Platform platform);
	public static bool IsValid (Platform platform);
	public static Platform ParseApiPlatform (string productName, string productVersion);
	public static Platform ToIos (Platform platform);
	public static Platform ToMac (Platform platform);
}
</pre>
<h3>New Type MonoMac.ObjCRuntime.TransientAttribute</h3>
<pre>
public class TransientAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public TransientAttribute ();
}
</pre>

<h2>Namespace MonoMac.PdfKit</h2>
<h3>Type Changed: MonoMac.PdfKit.PdfAction</h3>
<p>Added methods:</p><pre>
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
</pre>


<h2>Namespace MonoMac.SceneKit</h2>
<h3>Type Changed: MonoMac.SceneKit.SCNBox</h3>
<p>Added constructors:</p><pre>
	public SCNBox ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNCamera</h3>
<p>Added constructors:</p><pre>
	public SCNCamera ();
</pre>
<p>Removed properties:</p><pre>
	public virtual MonoMac.CoreAnimation.CATransform3D ProjectionTransform { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual MonoMac.CoreAnimation.CATransform3D ProjectionTransform { get; set; }
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNCapsule</h3>
<p>Added constructors:</p><pre>
	public SCNCapsule ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNCone</h3>
<p>Added constructors:</p><pre>
	public SCNCone ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNCylinder</h3>
<p>Added constructors:</p><pre>
	public SCNCylinder ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNFloor</h3>
<p>Added constructors:</p><pre>
	public SCNFloor ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNGeometryElement</h3>
<p>Added constructors:</p><pre>
	public SCNGeometryElement ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNGeometrySource</h3>
<p>Added constructors:</p><pre>
	public SCNGeometrySource ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNHitTest</h3>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString IgnoreHiddenNodes { get; }
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNLayer</h3>
<p>Removed methods:</p><pre>
	public virtual MonoMac.Foundation.NSArray HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>
<p>Added methods:</p><pre>
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNLight</h3>
<p>Added constructors:</p><pre>
	public SCNLight ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNMaterial</h3>
<p>Added constructors:</p><pre>
	public SCNMaterial ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNNode</h3>
<p>Added constructors:</p><pre>
	public SCNNode ();
</pre>
<p>Added interfaces:</p><pre>
	System.Collections.Generic.IEnumerable&lt;SCNNode&gt;
	System.Collections.IEnumerable
</pre>
<p>Removed methods:</p><pre>
	public virtual void AddChildNodechild (SCNNode child);
	public virtual MonoMac.Foundation.NSObject Clone ();
</pre>
<p>Added methods:</p><pre>
	public void Add (SCNNode node);
	public virtual void AddChildNode (SCNNode child);
	[Obsolete ("Use SCNNode.AddChildNode instead")]
	public void AddChildNodechild (SCNNode child);

	public virtual SCNNode Clone ();
	public virtual System.Collections.Generic.IEnumerator&lt;SCNNode&gt; GetEnumerator ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNNodeRendererDelegate</h3>
<p>Removed methods:</p><pre>
	public virtual void RenderNoderendererarguments (SCNNode node, SCNRenderer renderer, MonoMac.Foundation.NSDictionary arguments);
</pre>
<p>Added methods:</p><pre>
	public virtual void Render (SCNNode node, SCNRenderer renderer, MonoMac.Foundation.NSDictionary arguments);
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNPlane</h3>
<p>Added constructors:</p><pre>
	public SCNPlane ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNProgram</h3>
<p>Added constructors:</p><pre>
	public SCNProgram ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNPyramid</h3>
<p>Added constructors:</p><pre>
	public SCNPyramid ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNRenderer</h3>
<p>Added constructors:</p><pre>
	public SCNRenderer ();
</pre>
<p>Removed methods:</p><pre>
	public virtual MonoMac.Foundation.NSArray HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>
<p>Added methods:</p><pre>
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNScene</h3>
<p>Added constructors:</p><pre>
	public SCNScene ();
</pre>
<p>Added interfaces:</p><pre>
	System.Collections.Generic.IEnumerable&lt;SCNNode&gt;
	System.Collections.IEnumerable
</pre>
<p>Added properties:</p><pre>
	public static MonoMac.Foundation.NSString ExportDestinationUrl { get; }
</pre>
<p>Added methods:</p><pre>
	public void Add (SCNNode node);
	public virtual System.Collections.Generic.IEnumerator&lt;SCNNode&gt; GetEnumerator ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNTube</h3>
<p>Added constructors:</p><pre>
	public SCNTube ();
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNVector3</h3>
<p>Added constructors:</p><pre>
	public SCNVector3 (float x, float y, float z);
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNVector4</h3>
<p>Added constructors:</p><pre>
	public SCNVector4 (float x, float y, float z, float w);
</pre>

<h3>Type Changed: MonoMac.SceneKit.SCNView</h3>
<p>Removed methods:</p><pre>
	public virtual MonoMac.Foundation.NSArray HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>
<p>Added methods:</p><pre>
	public virtual SCNHitTestResult[] HitTest (System.Drawing.PointF thePoint, MonoMac.Foundation.NSDictionary options);
</pre>

<h3>New Type MonoMac.SceneKit.SCNAnimationEvent</h3>
<pre>
public class SCNAnimationEvent : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAnimationEvent (MonoMac.Foundation.NSCoder coder);
	public SCNAnimationEvent (MonoMac.Foundation.NSObjectFlag t);
	public SCNAnimationEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNAnimationEvent Create (float keyTime, SCNAnimationEventHandler eventHandler);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNAnimationEventHandler</h3>
<pre>
public sealed delegate SCNAnimationEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNAnimationEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSObject animatedObject, bool playingBackward, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSObject animatedObject, bool playingBackward);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNChamferMode</h3>
<pre>
[Serializable]
public enum SCNChamferMode {
	Back = 2,
	Both = 0,
	Front = 1,
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNConstraint</h3>
<pre>
public class SCNConstraint : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SCNConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNLevelOfDetail</h3>
<pre>
public class SCNLevelOfDetail : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNLevelOfDetail (MonoMac.Foundation.NSCoder coder);
	public SCNLevelOfDetail (MonoMac.Foundation.NSObjectFlag t);
	public SCNLevelOfDetail (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNGeometry Geometry { get; }
	public virtual float ScreenSpaceRadius { get; }
	public virtual float WorldSpaceDistance { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNLevelOfDetail CreateWithScreenSpaceRadius (SCNGeometry geometry, float screenSpaceRadius);
	public static SCNLevelOfDetail CreateWithWorldSpaceDistance (SCNGeometry geometry, float worldSpaceDistance);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNLookAtConstraint</h3>
<pre>
public class SCNLookAtConstraint : MonoMac.SceneKit.SCNConstraint, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNLookAtConstraint ();
	public SCNLookAtConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNLookAtConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SCNLookAtConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool GimbalLockEnabled { get; set; }
	public virtual SCNNode Target { get; }
	// methods
	public static SCNLookAtConstraint Create (SCNNode target);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNMorpher</h3>
<pre>
public class SCNMorpher : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNMorpher ();
	public SCNMorpher (MonoMac.Foundation.NSCoder coder);
	public SCNMorpher (MonoMac.Foundation.NSObjectFlag t);
	public SCNMorpher (System.IntPtr handle);
	// properties
	public virtual SCNMorpherCalculationMode CalculationMode { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNGeometry[] Targets { get; set; }
	// methods
	public virtual void AddAnimation (MonoMac.CoreAnimation.CAAnimation animation, MonoMac.Foundation.NSString key);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.CoreAnimation.CAAnimation GetAnimation (MonoMac.Foundation.NSString key);
	public virtual MonoMac.Foundation.NSString[] GetAnimationKeys ();
	public virtual float GetWeight (uint targetIndex);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (MonoMac.Foundation.NSString key);
	public virtual void SetWeight (float weight, uint targetIndex);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNMorpherCalculationMode</h3>
<pre>
[Serializable]
public enum SCNMorpherCalculationMode {
	Additive = 1,
	Normalized = 0,
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNSceneSourceLoadErrors</h3>
<pre>
public static class SCNSceneSourceLoadErrors {
	// properties
	public static MonoMac.Foundation.NSString ConsistencyElementIDErrorKey { get; }
	public static MonoMac.Foundation.NSString ConsistencyElementTypeErrorKey { get; }
	public static MonoMac.Foundation.NSString ConsistencyLineNumberErrorKey { get; }
	public static MonoMac.Foundation.NSString DetailedErrorsKey { get; }
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNSceneSourceProperties</h3>
<pre>
public static class SCNSceneSourceProperties {
	// properties
	public static MonoMac.Foundation.NSString AssetContributorsKey { get; }
	public static MonoMac.Foundation.NSString AssetCreatedDateKey { get; }
	public static MonoMac.Foundation.NSString AssetModifiedDateKey { get; }
	public static MonoMac.Foundation.NSString AssetUnitKey { get; }
	public static MonoMac.Foundation.NSString AssetUpAxisKey { get; }
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNShaderModifiers</h3>
<pre>
public static class SCNShaderModifiers {
	// properties
	public static MonoMac.Foundation.NSString EntryPointFragment { get; }
	public static MonoMac.Foundation.NSString EntryPointGeometry { get; }
	public static MonoMac.Foundation.NSString EntryPointLightingModel { get; }
	public static MonoMac.Foundation.NSString EntryPointSurface { get; }
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNShape</h3>
<pre>
public class SCNShape : MonoMac.SceneKit.SCNGeometry, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNShape ();
	public SCNShape (MonoMac.Foundation.NSCoder coder);
	public SCNShape (MonoMac.Foundation.NSObjectFlag t);
	public SCNShape (System.IntPtr handle);
	// properties
	public virtual SCNChamferMode ChamferMode { get; set; }
	public virtual MonoMac.AppKit.NSBezierPath ChamferProfile { get; set; }
	public virtual float ChamferRadius { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual float ExtrusionDepth { get; set; }
	public virtual MonoMac.AppKit.NSBezierPath Path { get; set; }
	// methods
	public static SCNShape Create (MonoMac.AppKit.NSBezierPath path, float extrusionDepth);
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNSkinner</h3>
<pre>
public class SCNSkinner : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNSkinner (MonoMac.Foundation.NSCoder coder);
	public SCNSkinner (MonoMac.Foundation.NSObjectFlag t);
	public SCNSkinner (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual SCNNode Skeleton { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNTransformConstraint</h3>
<pre>
public class SCNTransformConstraint : MonoMac.SceneKit.SCNConstraint, MonoMac.Foundation.INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNTransformConstraint ();
	public SCNTransformConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNTransformConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SCNTransformConstraint (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	// methods
	public static SCNTransformConstraint Create (bool inWorldSpace, SCNTransformConstraintHandler transformHandler);
}
</pre>
<h3>New Type MonoMac.SceneKit.SCNTransformConstraintHandler</h3>
<pre>
public sealed delegate SCNTransformConstraintHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNTransformConstraintHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform, System.AsyncCallback callback, object object);
	public virtual MonoMac.CoreAnimation.CATransform3D EndInvoke (System.IAsyncResult result);
	public virtual MonoMac.CoreAnimation.CATransform3D Invoke (SCNNode node, MonoMac.CoreAnimation.CATransform3D transform);
}
</pre>

<h2>Namespace MonoMac.Security</h2>
<h3>Type Changed: MonoMac.Security.SecCertificate</h3>
<p>Added constructors:</p><pre>
	public SecCertificate (System.IntPtr handle);
</pre>
<p>Added methods:</p><pre>
	public System.Security.Cryptography.X509Certificates.X509Certificate ToX509Certificate ();
	public System.Security.Cryptography.X509Certificates.X509Certificate2 ToX509Certificate2 ();
</pre>

<h3>Type Changed: MonoMac.Security.SecIdentity</h3>
<p>Added constructors:</p><pre>
	public SecIdentity (System.IntPtr handle);
</pre>
<p>Added properties:</p><pre>
	public SecKey PrivateKey { get; }
</pre>

<h3>Type Changed: MonoMac.Security.SecKey</h3>
<p>Added properties:</p><pre>
	public int BlockSize { get; }
</pre>
<p>Added methods:</p><pre>
	public SecStatusCode Encrypt (SecPadding padding, System.Byte[] plainText, System.Byte[]& cipherText);
</pre>

<h3>Type Changed: MonoMac.Security.SecPolicy</h3>
<p>Added constructors:</p><pre>
	public SecPolicy (System.IntPtr handle);
</pre>
<p>Added methods:</p><pre>
	public static SecPolicy CreatePolicy (MonoMac.Foundation.NSString policyIdentifier, MonoMac.Foundation.NSDictionary properties);
	public static SecPolicy CreateRevocationPolicy (SecRevocation revocationFlags);
	public MonoMac.Foundation.NSDictionary GetProperties ();
</pre>

<h3>Type Changed: MonoMac.Security.SecRecord</h3>
<p>Added properties:</p><pre>
	public bool Synchronizable { get; set; }
	public bool SynchronizableAny { get; set; }
</pre>

<h3>Type Changed: MonoMac.Security.SecStatusCode</h3>
<p>Added values:</p><pre>
	BadReq = -909,
	InternalComponent = -2070,
	IO = -36,
	OpWr = -49,
	UserCanceled = -128,
</pre>

<h3>Type Changed: MonoMac.Security.SecTrust</h3>
<p>Added constructors:</p><pre>
	public SecTrust (System.IntPtr handle);
	public SecTrust (SecCertificate certificate, SecPolicy policy);
</pre>
<p>Added properties:</p><pre>
	public bool NetworkFetchAllowed { get; set; }
</pre>
<p>Added methods:</p><pre>
	public SecCertificate[] GetCustomAnchorCertificates ();
	public SecPolicy[] GetPolicies ();
	public MonoMac.Foundation.NSDictionary GetResult ();
	public SecTrustResult GetTrustResult ();
	public void SetOCSPResponse (System.Collections.Generic.IEnumerable&lt;MonoMac.Foundation.NSData&gt; ocspResponses);
	public void SetOCSPResponse (MonoMac.Foundation.NSData ocspResponse);
	public void SetOCSPResponse (MonoMac.Foundation.NSArray ocspResponses);
	public void SetPolicies (System.Collections.Generic.IEnumerable&lt;SecPolicy&gt; policies);
	public void SetPolicies (MonoMac.Foundation.NSArray policies);
	public void SetPolicy (SecPolicy policy);
</pre>

<h3>Type Changed: MonoMac.Security.SecTrustResult</h3>
<p>Removed values:</p><pre>
	Confirm = 2,
</pre>
<p>Added values:</p><pre>
	[Obsolete ("Obsoleted in iOS 7")]
	Confirm = 2,

</pre>

<h3>New Type MonoMac.Security.SecImportExport</h3>
<pre>
public class SecImportExport {
	// constructors
	public SecImportExport ();
	// properties
	public static MonoMac.Foundation.NSString CertChain { get; }
	public static MonoMac.Foundation.NSString Identity { get; }
	public static MonoMac.Foundation.NSString KeyId { get; }
	public static MonoMac.Foundation.NSString Label { get; }
	public static MonoMac.Foundation.NSString Passphrase { get; }
	public static MonoMac.Foundation.NSString Trust { get; }
	// methods
	public static SecStatusCode ImportPkcs12 (System.Byte[] buffer, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSDictionary[]& array);
	public static SecStatusCode ImportPkcs12 (MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options, MonoMac.Foundation.NSDictionary[]& array);
}
</pre>
<h3>New Type MonoMac.Security.SecPolicyIdentifier</h3>
<pre>
public static class SecPolicyIdentifier {
	// properties
	public static MonoMac.Foundation.NSString AppleCodeSigning { get; }
	public static MonoMac.Foundation.NSString AppleEAP { get; }
	public static MonoMac.Foundation.NSString AppleIDValidation { get; }
	public static MonoMac.Foundation.NSString AppleIPsec { get; }
	public static MonoMac.Foundation.NSString ApplePKINITClient { get; }
	public static MonoMac.Foundation.NSString ApplePKINITServer { get; }
	public static MonoMac.Foundation.NSString AppleRevocation { get; }
	public static MonoMac.Foundation.NSString AppleSMIME { get; }
	public static MonoMac.Foundation.NSString AppleSSL { get; }
	public static MonoMac.Foundation.NSString AppleTimeStamping { get; }
	public static MonoMac.Foundation.NSString AppleX509Basic { get; }
	public static MonoMac.Foundation.NSString MacAppStoreReceipt { get; }
}
</pre>
<h3>New Type MonoMac.Security.SecPolicyPropertyKey</h3>
<pre>
public static class SecPolicyPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString Client { get; }
	public static MonoMac.Foundation.NSString Name { get; }
	public static MonoMac.Foundation.NSString Oid { get; }
	public static MonoMac.Foundation.NSString RevocationFlags { get; }
}
</pre>
<h3>New Type MonoMac.Security.SecRevocation</h3>
<pre>
[Serializable]
[Flags]
public enum SecRevocation {
	CRLMethod = 2,
	NetworkAccessDisabled = 16,
	None = 0,
	OCSPMethod = 1,
	PreferCRL = 4,
	RequirePositiveResponse = 8,
	UseAnyAvailableMethod = 3,
}
</pre>
<h3>New Type MonoMac.Security.SecTrustPropertyKey</h3>
<pre>
public static class SecTrustPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString Error { get; }
	public static MonoMac.Foundation.NSString Title { get; }
}
</pre>
<h3>New Type MonoMac.Security.SecTrustResultKey</h3>
<pre>
public static class SecTrustResultKey {
	// properties
	public static MonoMac.Foundation.NSString EvaluationDate { get; }
	public static MonoMac.Foundation.NSString ExtendedValidation { get; }
	public static MonoMac.Foundation.NSString OrganizationName { get; }
	public static MonoMac.Foundation.NSString ResultValue { get; }
	public static MonoMac.Foundation.NSString RevocationChecked { get; }
	public static MonoMac.Foundation.NSString RevocationValidUntilDate { get; }
}
</pre>
<h3>New Type MonoMac.Security.SslProtocol</h3>
<pre>
[Serializable]
public enum SslProtocol {
	All = 6,
	Dtls_1_0 = 9,
	Ssl_2_0 = 1,
	Ssl_3_0_only = 3,
	Ssl3_0 = 2,
	Tls_1_0 = 4,
	Tls_1_0_only = 5,
	Tls_1_1 = 7,
	Tls_1_2 = 8,
	Unknown = 0,
}
</pre>

<h2>Namespace MonoMac.StoreKit</h2>
<h3>Type Changed: MonoMac.StoreKit.SKMutablePayment</h3>
<p>Removed methods:</p><pre>
	public static SKMutablePayment PaymentWithProduct (string identifier);
</pre>
<p>Added methods:</p><pre>
	[Obsolete ("Deprecated in iOS 5.0. Use PaymentWithProduct(SKProduct) after fetching the list of available products from SKProductRequest")]
	public static SKMutablePayment PaymentWithProduct (string identifier);

</pre>

<h3>New Type MonoMac.StoreKit.ISKPaymentTransactionObserver</h3>
<pre>
public interface ISKPaymentTransactionObserver : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void UpdatedTransactions (SKPaymentQueue queue, SKPaymentTransaction[] transactions);
}
</pre>
<h3>New Type MonoMac.StoreKit.ISKProductsRequestDelegate</h3>
<pre>
public interface ISKProductsRequestDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ReceivedResponse (SKProductsRequest request, SKProductsResponse response);
}
</pre>
<h3>New Type MonoMac.StoreKit.ISKRequestDelegate</h3>
<pre>
public interface ISKRequestDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>
<h3>New Type MonoMac.StoreKit.SKPaymentTransactionObserver_Extensions</h3>
<pre>
public static class SKPaymentTransactionObserver_Extensions {
	// methods
	public static void PaymentQueueRestoreCompletedTransactionsFinished (ISKPaymentTransactionObserver This, SKPaymentQueue queue);
	public static void RemovedTransactions (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKPaymentTransaction[] transactions);
	public static void RestoreCompletedTransactionsFailedWithError (ISKPaymentTransactionObserver This, SKPaymentQueue queue, MonoMac.Foundation.NSError error);
	public static void UpdatedDownloads (ISKPaymentTransactionObserver This, SKPaymentQueue queue, SKDownload[] downloads);
}
</pre>
<h3>New Type MonoMac.StoreKit.SKProductsRequestDelegate_Extensions</h3>
<pre>
public static class SKProductsRequestDelegate_Extensions {
}
</pre>
<h3>New Type MonoMac.StoreKit.SKRequestDelegate_Extensions</h3>
<pre>
public static class SKRequestDelegate_Extensions {
	// methods
	public static void RequestFailed (ISKRequestDelegate This, SKRequest request, MonoMac.Foundation.NSError error);
	public static void RequestFinished (ISKRequestDelegate This, SKRequest request);
}
</pre>

<h2>Namespace MonoMac.WebKit</h2>
<h3>Type Changed: MonoMac.WebKit.DomHtmlInputElement</h3>
<p>Removed properties:</p><pre>
	public virtual DomFileList Files { get; }
</pre>
<p>Added properties:</p><pre>
	public virtual DomFileList Files { get; set; }
</pre>

<h3>Type Changed: MonoMac.WebKit.DomObject</h3>
<p>Added methods:</p><pre>
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
</pre>


<h2>New Namespace MonoMac.Accelerate</h2>

<h3>New Type MonoMac.Accelerate.Pixel8888</h3>
<pre>
public struct Pixel8888 {
	// fields
	public byte A;
	public byte B;
	public byte G;
	public byte R;
	public static Pixel8888 Zero;
}
</pre>
<h3>New Type MonoMac.Accelerate.PixelARGB16S</h3>
<pre>
public struct PixelARGB16S {
	// fields
	public short A;
	public short B;
	public short G;
	public short R;
	public static PixelARGB16S Zero;
}
</pre>
<h3>New Type MonoMac.Accelerate.PixelARGB16U</h3>
<pre>
public struct PixelARGB16U {
	// fields
	public ushort A;
	public ushort B;
	public ushort G;
	public ushort R;
	public static PixelARGB16U Zero;
}
</pre>
<h3>New Type MonoMac.Accelerate.PixelFFFF</h3>
<pre>
public struct PixelFFFF {
	// fields
	public float A;
	public float B;
	public float G;
	public float R;
	public static PixelFFFF Zero;
}
</pre>
<h3>New Type MonoMac.Accelerate.vImage</h3>
<pre>
public static class vImage {
	// methods
	public static vImageError BoxConvolveARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, uint kernel_height, uint kernel_width, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError BoxConvolveARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, uint kernel_height, uint kernel_width, Pixel8888* backgroundColor, vImageFlags flags);
	public static vImageError BoxConvolvePlanar8 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, uint kernel_height, uint kernel_width, byte backgroundColor, vImageFlags flags);
	public static vImageError ConvolveARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, uint kernel_height, uint kernel_width, int divisor, Pixel8888* backgroundColor, vImageFlags flags);
	public static vImageError ConvolveARGBFFFF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, uint kernel_height, uint kernel_width, PixelFFFF backgroundColor, vImageFlags flags);
	public static vImageError ConvolveMultiKernelARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16[] kernels, uint kernel_height, uint kernel_width, System.Int32[] divisors, System.Int32[] biases, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError ConvolveMultiKernelARGBFFFF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single[] kernels, uint kernel_height, uint kernel_width, System.Single[] biases, PixelFFFF& backgroundColor, vImageFlags flags);
	public static vImageError ConvolveMultiKernelARGBFFFF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single[] kernels, uint kernel_height, uint kernel_width, System.Single[] biases, PixelFFFF backgroundColor, vImageFlags flags);
	public static vImageError ConvolvePlanar8 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, uint kernel_height, uint kernel_width, int divisor, byte backgroundColor, vImageFlags flags);
	public static vImageError ConvolvePlanarF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, uint kernel_height, uint kernel_width, float backgroundColor, vImageFlags flags);
	public static vImageError ConvolveWithBiasARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, uint kernel_height, uint kernel_width, int divisor, int bias, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError ConvolveWithBiasARGBFFFF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, uint kernel_height, uint kernel_width, float bias, PixelFFFF backgroundColor, vImageFlags flags);
	public static vImageError ConvolveWithBiasPlanar8 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, uint kernel_height, uint kernel_width, int divisor, int bias, byte backgroundColor, vImageFlags flags);
	public static vImageError ConvolveWithBiasPlanarF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, uint kernel_height, uint kernel_width, float bias, float backgroundColor, vImageFlags flags);
	public static vImageError MatrixMultiplyARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.Int16[] matrix, int divisor, System.Int16[] pre_bias, System.Int32[] post_bias, vImageFlags flags);
	public static vImageError RichardsonLucyDeConvolveARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, System.Int16* kernel2, uint kernel_height, uint kernel_width, uint kernel_height2, uint kernel_width2, int divisor, int divisor2, Pixel8888 backgroundColor, uint iterationCount, vImageFlags flags);
	public static vImageError RichardsonLucyDeConvolveARGBFFFF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, System.Single* kernel2, uint kernel_height, uint kernel_width, uint kernel_height2, uint kernel_width2, PixelFFFF backgroundColor, uint iterationCount, vImageFlags flags);
	public static vImageError RichardsonLucyDeConvolvePlanar8 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Int16* kernel, System.Int16* kernel2, uint kernel_height, uint kernel_width, uint kernel_height2, uint kernel_width2, int divisor, int divisor2, byte backgroundColor, uint iterationCount, vImageFlags flags);
	public static vImageError RichardsonLucyDeConvolvePlanarF (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, System.Single* kernel, System.Single* kernel2, uint kernel_height, uint kernel_width, uint kernel_height2, uint kernel_width2, float backgroundColor, uint iterationCount, vImageFlags flags);
	public static vImageError TentConvolveARGB8888 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, uint kernel_height, uint kernel_width, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError TentConvolvePlanar8 (vImageBuffer& src, vImageBuffer& dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, uint kernel_height, uint kernel_width, byte backgroundColor, vImageFlags flags);
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageAffineTransformDouble</h3>
<pre>
public struct vImageAffineTransformDouble {
	// fields
	public double a;
	public double b;
	public double c;
	public double d;
	public double tx;
	public double ty;
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageAffineTransformFloat</h3>
<pre>
public struct vImageAffineTransformFloat {
	// fields
	public float a;
	public float b;
	public float c;
	public float d;
	public float tx;
	public float ty;
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageBuffer</h3>
<pre>
public struct vImageBuffer {
	// properties
	public int BytesPerRow { get; set; }
	public System.IntPtr Data { get; set; }
	public int Height { get; set; }
	public int Width { get; set; }
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageError</h3>
<pre>
[Serializable]
public enum vImageError {
	BufferSizeMismatch = -21774,
	ColorSyncIsAbsent = -21779,
	InternalError = -21776,
	InvalidEdgeStyle = -21768,
	InvalidImageFormat = -21778,
	InvalidKernelSize = -21767,
	InvalidOffsetX = -21769,
	InvalidOffsetY = -21770,
	InvalidParameter = -21773,
	InvalidRowBytes = -21777,
	MemoryAllocationError = -21771,
	NoError = 0,
	NullPointerArgument = -21772,
	OutOfPlaceOperationRequired = -21780,
	RoiLargerThanInputBuffer = -21766,
	UnknownFlagsBit = -21775,
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageFlags</h3>
<pre>
[Serializable]
[Flags]
public enum vImageFlags {
	BackgroundColorFill = 4,
	CopyInPlace = 2,
	DoNotTile = 16,
	EdgeExtend = 8,
	GetTempBufferSize = 128,
	HighQualityResampling = 32,
	LeaveAlphaUnchanged = 1,
	NoAllocate = 512,
	NoFlags = 0,
	PrintDiagnosticsToConsole = 256,
	TruncateKernel = 64,
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageGamma</h3>
<pre>
[Serializable]
public enum vImageGamma {
	k11ove_5_HalfPrecision = 5,
	k11over9_HalfPrecision = 8,
	k5over11_HalfPrecision = 4,
	k5over9_HalfPrecision = 2,
	k9over11_HalfPrecision = 9,
	k9over5_HalfPrecision = 3,
	kBT709_ForwardHalfPrecision = 10,
	kBT709_ReverseHalfPrecision = 11,
	ksRGB_ForwardHalfPrecision = 6,
	ksRGB_ReverseHalfPrecision = 7,
	kUseGammaValue = 0,
	kUseGammaValueHalfPrecision = 1,
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageInterpolationMethod</h3>
<pre>
[Serializable]
public enum vImageInterpolationMethod {
	Full = 1,
	Half = 2,
	None = 0,
}
</pre>
<h3>New Type MonoMac.Accelerate.vImageMDTableUsageHint</h3>
<pre>
[Serializable]
public enum vImageMDTableUsageHint {
	k16Q12 = 1,
	kFloat = 2,
}
</pre>

<h2>New Namespace MonoMac.MobileCoreServices</h2>

<h3>New Type MonoMac.MobileCoreServices.UTType</h3>
<pre>
public class UTType {
	// constructors
	public UTType ();
	// fields
	public static MonoMac.Foundation.NSString AliasFile;
	public static MonoMac.Foundation.NSString AliasRecord;
	public static MonoMac.Foundation.NSString AppleICNS;
	public static MonoMac.Foundation.NSString AppleProtectedMPEG4Audio;
	public static MonoMac.Foundation.NSString Application;
	public static MonoMac.Foundation.NSString ApplicationBundle;
	public static MonoMac.Foundation.NSString ApplicationFile;
	public static MonoMac.Foundation.NSString Archive;
	public static MonoMac.Foundation.NSString Audio;
	public static MonoMac.Foundation.NSString AudiovisualContent;
	public static MonoMac.Foundation.NSString BMP;
	public static MonoMac.Foundation.NSString Bundle;
	public static MonoMac.Foundation.NSString CHeader;
	public static MonoMac.Foundation.NSString CompositeContent;
	public static MonoMac.Foundation.NSString ConformsToKey;
	public static MonoMac.Foundation.NSString Contact;
	public static MonoMac.Foundation.NSString Content;
	public static MonoMac.Foundation.NSString CPlusPlusHeader;
	public static MonoMac.Foundation.NSString CPlusPlusSource;
	public static MonoMac.Foundation.NSString CSource;
	public static MonoMac.Foundation.NSString Data;
	public static MonoMac.Foundation.NSString DescriptionKey;
	public static MonoMac.Foundation.NSString Directory;
	public static MonoMac.Foundation.NSString DiskImage;
	public static MonoMac.Foundation.NSString ExportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString FileURL;
	public static MonoMac.Foundation.NSString FlatRTFD;
	public static MonoMac.Foundation.NSString Folder;
	public static MonoMac.Foundation.NSString Framework;
	public static MonoMac.Foundation.NSString GIF;
	public static MonoMac.Foundation.NSString HTML;
	public static MonoMac.Foundation.NSString ICO;
	public static MonoMac.Foundation.NSString IconFileKey;
	public static MonoMac.Foundation.NSString IdentifierKey;
	public static MonoMac.Foundation.NSString Image;
	public static MonoMac.Foundation.NSString ImportedTypeDeclarationsKey;
	public static MonoMac.Foundation.NSString InkText;
	public static MonoMac.Foundation.NSString Item;
	public static MonoMac.Foundation.NSString JavaSource;
	public static MonoMac.Foundation.NSString JPEG;
	public static MonoMac.Foundation.NSString JPEG2000;
	public static MonoMac.Foundation.NSString Message;
	public static MonoMac.Foundation.NSString MountPoint;
	public static MonoMac.Foundation.NSString Movie;
	public static MonoMac.Foundation.NSString MP3;
	public static MonoMac.Foundation.NSString MPEG;
	public static MonoMac.Foundation.NSString MPEG4;
	public static MonoMac.Foundation.NSString MPEG4Audio;
	public static MonoMac.Foundation.NSString ObjectiveCPlusPlusSource;
	public static MonoMac.Foundation.NSString ObjectiveCSource;
	public static MonoMac.Foundation.NSString Package;
	public static MonoMac.Foundation.NSString PDF;
	public static MonoMac.Foundation.NSString PICT;
	public static MonoMac.Foundation.NSString PlainText;
	public static MonoMac.Foundation.NSString PNG;
	public static MonoMac.Foundation.NSString QuickTimeImage;
	public static MonoMac.Foundation.NSString QuickTimeMovie;
	public static MonoMac.Foundation.NSString ReferenceURLKey;
	public static MonoMac.Foundation.NSString Resolvable;
	public static MonoMac.Foundation.NSString RTF;
	public static MonoMac.Foundation.NSString RTFD;
	public static MonoMac.Foundation.NSString SourceCode;
	public static MonoMac.Foundation.NSString SymLink;
	public static MonoMac.Foundation.NSString TagClassFilenameExtension;
	public static MonoMac.Foundation.NSString TagClassMIMEType;
	public static MonoMac.Foundation.NSString TagClassNSPboardType;
	public static MonoMac.Foundation.NSString TagClassOSType;
	public static MonoMac.Foundation.NSString TagSpecificationKey;
	public static MonoMac.Foundation.NSString Text;
	public static MonoMac.Foundation.NSString TIFF;
	public static MonoMac.Foundation.NSString TXNTextAndMultimediaData;
	public static MonoMac.Foundation.NSString URL;
	public static MonoMac.Foundation.NSString UTF16ExternalPlainText;
	public static MonoMac.Foundation.NSString UTF16PlainText;
	public static MonoMac.Foundation.NSString UTF8PlainText;
	public static MonoMac.Foundation.NSString VCard;
	public static MonoMac.Foundation.NSString VersionKey;
	public static MonoMac.Foundation.NSString Video;
	public static MonoMac.Foundation.NSString Volume;
	public static MonoMac.Foundation.NSString WebArchive;
	public static MonoMac.Foundation.NSString XML;
}
</pre>
</body>
</html>
