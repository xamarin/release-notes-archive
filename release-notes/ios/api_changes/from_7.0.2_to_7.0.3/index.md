---
id: 0EFBB53D-82F3-49FE-90A1-25CCD20B65F8
title: "From 7.0.2 to 7.0.3"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.0.2";
```

Added fields:

```
public static const string AccelerateImageLibrary = "/System/Library/Frameworks/Accelerate.framework/Frameworks/vImage.framework/vImage";
	public static const string Version = "7.0.3";
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioComponent

Added properties:

```
public double LastActiveTime { get; }
```

Added methods:

```
public MonoTouch.UIKit.UIImage GetIcon (float desiredPointSize);
```

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Added methods:

```
public AudioComponentStatus AudioOutputUnitPublish (AudioComponentDescription description, string name, uint version);
	public MonoTouch.UIKit.UIImage GetHostIcon (float desiredPointSize);
	public AudioUnitParameterInfo[] GetParameterList (AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus MakeConnection (AudioUnit sourceAudioUnit, uint sourceOutputNumber, uint destInputNumber);
	public AudioUnitStatus MusicDeviceMIDIEvent (uint status, uint data1, uint data2, uint offsetSampleFrame);
	public AudioUnitStatus SetInputCallback (InputDelegate inputDelegate, AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus SetSampleRate (double sampleRate, AudioUnitScopeType scope, uint audioUnitElement);
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitParameterType

Added values:

```
Reverb2DecayTimeAt0Hz = 4,
	Reverb2DecayTimeAtNyquist = 5,
	Reverb2DryWetMix = 0,
	Reverb2Gain = 1,
	Reverb2MaxDelayTime = 3,
	Reverb2MinDelayTime = 2,
	Reverb2RandomizeReflections = 6,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added values:

```
BiquadCoefficients = 2203,
	BypassVoiceProcessing = 2100,
	MaxNumberOfBands = 2201,
	MuteOutput = 2104,
	NumberOfBands = 2200,
	VoiceProcessingEnableAGC = 2101,
```

### New Type MonoTouch.AudioUnit.AudioComponentStatus

```
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
```

### New Type MonoTouch.AudioUnit.AudioUnitClumpID

```
[Serializable]
public enum AudioUnitClumpID {
	System = 0,
}
```

### New Type MonoTouch.AudioUnit.AudioUnitParameterFlag

```
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
```

### New Type MonoTouch.AudioUnit.AudioUnitParameterInfo

```
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
```

### New Type MonoTouch.AudioUnit.AudioUnitParameterUnit

```
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
```

### New Type MonoTouch.AudioUnit.AudioUnitRemoteControlEvent

```
[Serializable]
public enum AudioUnitRemoteControlEvent {
	Rewind = 3,
	TogglePlayPause = 1,
	ToggleRecord = 2,
}
```

### New Type MonoTouch.AudioUnit.InputDelegate

```
public sealed delegate InputDelegate : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public InputDelegate (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, AudioUnit audioUnit, System.AsyncCallback callback, object object);
	public virtual AudioUnitStatus EndInvoke (System.IAsyncResult result);
	public virtual AudioUnitStatus Invoke (AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, uint busNumber, uint numberFrames, AudioUnit audioUnit);
}
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed constructors:

```
[Obsolete ("This method had an invalid signature in MonoTouch 1.0.3, use AVAudioPlayer.FromUrl instead")]
	public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSError error);

	[Obsolete ("This method had an invalid signature in MonoTouch 1.0.3, use AVAudioPlayer.FromData instead")]
	public AVAudioPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSError error);
```

Added constructors:

```
[Obsolete ("This method had an invalid signature in MonoMac 1.0.3, use AVAudioPlayer.FromUrl instead")]
	public AVAudioPlayer (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSError error);

	[Obsolete ("This method had an invalid signature in MonoMac 1.0.3, use AVAudioPlayer.FromData instead")]
	public AVAudioPlayer (MonoTouch.Foundation.NSData data, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioRecorder

Removed constructors:

```
[Obsolete ("Use static Create method as this method had an invalid signature up to MonoTouch 1.4.4")]
	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
```

Added constructors:

```
[Obsolete ("Use static Create method as this method had an invalid signature up to MonoMac 1.4.4")]
	public AVAudioRecorder (MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary settings, MonoTouch.Foundation.NSError outError);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Removed constructors:

```
public AVAudioSession ();
```

Added constructors:

```
[Obsolete ("Please use the static SharedInstance property as this type is not meant to be created")]
	public AVAudioSession ();
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Added properties:

```
public virtual bool HasFlash { get; }
	public virtual bool HasTorch { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVMetadataItemFilter

Removed constructors:

```
public AVMetadataItemFilter ();
```

Added constructors:

```
[Obsolete ("Please use the static ForSharing factory method as this type is not meant to be created directly")]
	public AVMetadataItemFilter ();
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Removed methods:

```
public void RetrievePeripherals (System.Guid peripheralUuid);
	public void RetrievePeripherals (System.Guid[] peripheralUuids);
	public void ScanForPeripherals (System.Guid[] serviceUuids, MonoTouch.Foundation.NSDictionary options);
	public void ScanForPeripherals (System.Guid[] serviceUuids, PeripheralScanningOptions options);
	public void ScanForPeripherals (System.Guid[] serviceUuids);
	public void ScanForPeripherals (System.Guid serviceUuid, MonoTouch.Foundation.NSDictionary options);
	public void ScanForPeripherals (System.Guid serviceUuid);
```

Added methods:

```
[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid peripheralUuid);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid[] peripheralUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, MonoTouch.Foundation.NSDictionary options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, PeripheralScanningOptions options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid, MonoTouch.Foundation.NSDictionary options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid);
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Removed methods:

```
public void DiscoverCharacteristics (System.Guid[] charactersticUUIDs, CBService forService);
	public void DiscoverIncludedServices (System.Guid[] includedServiceUUIDs, CBService forService);
	public void DiscoverServices (System.Guid[] services);
```

Added methods:

```
[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverCharacteristics (System.Guid[] charactersticUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverIncludedServices (System.Guid[] includedServiceUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverServices (System.Guid[] services);
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.INSFetchedResultsSectionInfo

Added properties:

```
public virtual int Count { get; }
	public virtual string IndexTitle { get; }
	public virtual string Name { get; }
	public virtual MonoTouch.Foundation.NSObject[] Objects { get; }
```

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added properties:

```
public static MonoTouch.Foundation.NSString DidSaveNotification { get; }
	public static MonoTouch.Foundation.NSString ObjectsDidChangeNotification { get; }
	public static MonoTouch.Foundation.NSString WillSaveNotification { get; }
```

### New Type MonoTouch.CoreData.NSManagedObjectChangeEventArgs

```
public class NSManagedObjectChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
	// constructors
	public NSManagedObjectChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
	// properties
	public MonoTouch.Foundation.NSSet DeletedObjects { get; }
	public MonoTouch.Foundation.NSSet InsertedObjects { get; }
	public bool InvalidatedAllObjects { get; }
	public MonoTouch.Foundation.NSSet InvalidatedObjects { get; }
	public MonoTouch.Foundation.NSSet RefreshedObjects { get; }
	public MonoTouch.Foundation.NSSet UpdatedObjects { get; }
}
```

## Namespace MonoTouch.CoreFoundation

### Type Changed: MonoTouch.CoreFoundation.DispatchQueue

Added methods:

```
public void DispatchAfter (DispatchTime when, MonoTouch.Foundation.NSAction action);
```

### Type Changed: MonoTouch.CoreFoundation.DispatchTime

Added constructors:

```
public DispatchTime (DispatchTime when, long delta);
```

## Namespace MonoTouch.CoreGraphics

### Type Changed: MonoTouch.CoreGraphics.CGContext

Added methods:

```
public CGBitmapContext AsBitmapContext ();
```

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLLocationManager

Added methods:

```
public static bool IsMonitoringAvailable (System.Type t);
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMSampleBuffer

Added methods:

```
public CMSampleBufferError CopyPCMDataIntoAudioBufferList (int frameOffset, int numFrames, MonoTouch.AudioToolbox.AudioBuffers bufferList);
```

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMMotionActivityManager

Removed methods:

```
public virtual void QueryActivity (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityHandler handler);
	public virtual System.Threading.Tasks.Task<CMMotionActivity> QueryActivityAsync (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue);
	public virtual void StartActivityUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityQueryHandler handler);
```

Added methods:

```
public virtual void QueryActivity (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityQueryHandler handler);
	public virtual System.Threading.Tasks.Task<CMMotionActivity[]> QueryActivityAsync (MonoTouch.Foundation.NSDate start, MonoTouch.Foundation.NSDate end, MonoTouch.Foundation.NSOperationQueue queue);
	public virtual void StartActivityUpdates (MonoTouch.Foundation.NSOperationQueue queue, CMMotionActivityHandler handler);
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSException

Added properties:

```
public virtual System.String[] CallStackSymbols { get; }
```

### Type Changed: MonoTouch.Foundation.NSString

Added constructors:

```
public NSString (NSData data, NSStringEncoding encoding);
```

### New Type MonoTouch.Foundation.NSMutableString

```
public class NSMutableString : MonoTouch.Foundation.NSString, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
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
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static uint UInt32_objc_msgSend_IntPtr_IntPtr_UInt32_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, MonoTouch.Foundation.NSRange arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_UInt32_NSRange (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, uint arg3, MonoTouch.Foundation.NSRange arg4);
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.IUILayoutSupport

Added properties:

```
public virtual float Length { get; }
```

### Type Changed: MonoTouch.UIKit.UIBezierPath

Removed interfaces:

```
System.Collections.IEnumerable
	IUIDynamicItem
```

Removed properties:

```
public static UIBezierPath.UIBezierPathAppearance Appearance { get; }
```

Removed methods:

```
public static UIBezierPath.UIBezierPathAppearance AppearanceWhenContainedIn (System.Type[] containers);
	public static UIBezierPath.UIBezierPathAppearance GetAppearance<T> ();
```

### Removed Type MonoTouch.UIKit.UIBezierPath.UIBezierPathAppearance ### Type Changed: MonoTouch.UIKit.UIViewController

Removed methods:

```
[Obsolete ("Deprecated in iOS 6.0, use PresentViewController (UIViewController, bool, NSAction) instead.")]
	public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
```

Added methods:

```
[Obsolete ("Deprecated in iOS 6.0, use PresentViewController (UIViewController, bool, NSAction) instead and set the ModalViewController property to true.")]
	public virtual void PresentModalViewController (UIViewController modalViewController, bool animated);
```



## New Namespace MonoTouch.Accelerate

### New Type MonoTouch.Accelerate.Pixel8888

```
public struct Pixel8888 {
	// fields
	public byte A;
	public byte B;
	public byte G;
	public byte R;
	public static Pixel8888 Zero;
}
```

### New Type MonoTouch.Accelerate.PixelARGB16S

```
public struct PixelARGB16S {
	// fields
	public short A;
	public short B;
	public short G;
	public short R;
	public static PixelARGB16S Zero;
}
```

### New Type MonoTouch.Accelerate.PixelARGB16U

```
public struct PixelARGB16U {
	// fields
	public ushort A;
	public ushort B;
	public ushort G;
	public ushort R;
	public static PixelARGB16U Zero;
}
```

### New Type MonoTouch.Accelerate.PixelFFFF

```
public struct PixelFFFF {
	// fields
	public float A;
	public float B;
	public float G;
	public float R;
	public static PixelFFFF Zero;
}
```

### New Type MonoTouch.Accelerate.vImage

```
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
```

### New Type MonoTouch.Accelerate.vImageAffineTransformDouble

```
public struct vImageAffineTransformDouble {
	// fields
	public double a;
	public double b;
	public double c;
	public double d;
	public double tx;
	public double ty;
}
```

### New Type MonoTouch.Accelerate.vImageAffineTransformFloat

```
public struct vImageAffineTransformFloat {
	// fields
	public float a;
	public float b;
	public float c;
	public float d;
	public float tx;
	public float ty;
}
```

### New Type MonoTouch.Accelerate.vImageBuffer

```
public struct vImageBuffer {
	// properties
	public int BytesPerRow { get; set; }
	public System.IntPtr Data { get; set; }
	public int Height { get; set; }
	public int Width { get; set; }
}
```

### New Type MonoTouch.Accelerate.vImageError

```
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
```

### New Type MonoTouch.Accelerate.vImageFlags

```
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
```

### New Type MonoTouch.Accelerate.vImageGamma

```
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
```

### New Type MonoTouch.Accelerate.vImageInterpolationMethod

```
[Serializable]
public enum vImageInterpolationMethod {
	Full = 1,
	Half = 2,
	None = 0,
}
```

### New Type MonoTouch.Accelerate.vImageMDTableUsageHint

```
[Serializable]
public enum vImageMDTableUsageHint {
	k16Q12 = 1,
	kFloat = 2,
}
```

   


 <hr>

# mscorlib.dll

## Namespace System.Runtime.InteropServices

### Type Changed: System.Runtime.InteropServices.Marshal

Added methods:

```
public static System.IntPtr CreateAggregatedObject<T> (System.IntPtr pOuter, T o);
	public static void DestroyStructure<T> (System.IntPtr ptr);
	public static System.Delegate GetDelegateForFunctionPointer<T> (System.IntPtr ptr);
	public static System.IntPtr GetFunctionPointerForDelegate<TDelegate> (TDelegate d);
	public static System.IntPtr OffsetOf<T> (string fieldName);
	public static object PtrToStructure<T> (System.IntPtr ptr);
	public static void PtrToStructure<T> (System.IntPtr ptr, T structure);
	public static int SizeOf<T> (T structure);
	public static int SizeOf<T> ();
	public static void StructureToPtr<T> (T structure, System.IntPtr ptr, bool fDeleteOld);
	public static System.IntPtr UnsafeAddrOfPinnedArrayElement<T> (T[] arr, int index);
```

   


 <hr>

# System.dll

## Namespace System.IO.Compression

### Type Changed: System.IO.Compression.CompressionLevel

Removed values:

```
Optional = 0,
```

Added values:

```
Optimal = 0,
```

   


 <hr>

# System.Core.dll

## Namespace System.Linq.Expressions

### Type Changed: System.Linq.Expressions.Expression

Removed properties:

```
public ExpressionType NodeType { get; }
	public System.Type Type { get; }
```

Added properties:

```
public virtual ExpressionType NodeType { get; }
	public virtual System.Type Type { get; }
```

   


 <hr>

# MonoTouch.NUnitLite.dll

## Namespace MonoTouch.NUnit

### New Type MonoTouch.NUnit.NUnitOutputTextWriter

```
public class NUnitOutputTextWriter : System.IO.TextWriter, System.IDisposable {
	// constructors
	public NUnitOutputTextWriter (UI.TouchRunner runner, System.IO.TextWriter baseWriter, NUnitLite.Runner.OutputWriter xmlWriter);
	// properties
	public System.IO.TextWriter BaseWriter { get; }
	public override System.Text.Encoding Encoding { get; }
	public UI.TouchRunner Runner { get; }
	public NUnitLite.Runner.OutputWriter XmlOutputWriter { get; }
	// methods
	public override void Close ();
	public override void Write (char value);
	public override void Write (string value);
}
```

   


 <hr>
