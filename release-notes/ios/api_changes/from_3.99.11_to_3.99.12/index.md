---
id: 12908DD2-4072-4656-8A44-7AB8CD43DA33
title: "From 3.99.11 to 3.99.12"
---

<html><head><title>Comparison between monotouch.dll and monotouch.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.99.11";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.99.12";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput</h2>
<p>Removed:</p><pre>
 	public virtual AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
 	public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
</pre>
<p>Added:</p><pre>
 	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
 	public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
 	public AVVideoSettings VideoSettings {
 	public virtual MonoTouch.Foundation.NSDictionary WeakVideoSettings {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceInput</h2>
<p>Removed:</p><pre>
 	public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr ptrToHandleToError);
 	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr ptrToHandleToError);
</pre>
<p>Added:</p><pre>
 	public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr handle);
 	public AVCaptureDeviceInput (AVCaptureDevice device, out MonoTouch.Foundation.NSError error);
 	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device);
 	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr handle);
 	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, out MonoTouch.Foundation.NSError error);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureSession</h2>
<p>Removed:</p><pre>
 	public virtual bool CanSetSessionPreset (string preset);
 	public virtual string SessionPreset {
</pre>
<p>Added:</p><pre>
 	public virtual bool CanSetSessionPreset (MonoTouch.Foundation.NSString preset);
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
 	public virtual MonoTouch.Foundation.NSString SessionPreset {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoDataOutput</h2>
<p>Removed:</p><pre>
 	public virtual IntPtr SampleBufferCallbackQueue {
 	public virtual MonoTouch.Foundation.NSDictionary VideoSettings {
</pre>
<p>Added:</p><pre>
 	public void SetSampleBufferDelegateAndQueue (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, MonoTouch.CoreFoundation.DispatchQueue queue);
 	public virtual MonoTouch.CoreFoundation.DispatchQueue SampleBufferCallbackQueue {
 	public AVVideoSettings VideoSettings {
 		get;
 		set;
 	}
 	public virtual MonoTouch.Foundation.NSDictionary WeakVideoSettings {
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVVideoSettings</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVVideoSettings
</pre>
<p>Added:</p><pre>
 public class AVVideoSettings {
 	
 	public AVVideoSettings ();
 	public AVVideoSettings (MonoTouch.CoreVideo.CVPixelFormatType formatType);
 	
 	public MonoTouch.Foundation.NSDictionary ToDictionary ();
 	
 	public System.Nullable&lt;MonoTouch.CoreVideo.CVPixelFormatType&gt; PixelFormat {
 		get;
 		set;
 	}
 }
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AssetsLibrary</h1>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h1>Namespace: MonoTouch.AudioUnit</h1>
<h1>Namespace: MonoTouch.AudioUnitWrapper</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>Type Changed: MonoTouch.CoreAnimation.CAShapeLayer</h2>
<p>Removed:</p><pre>
 	public static MonoTouch.Foundation.NSString FilLRuleEvenOdd {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString FillRuleEvenOdd {
</pre>
<h1>Namespace: MonoTouch.CoreData</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGBitmapContext</h2>
<p>Added:</p><pre>
 	public CGBitmapContext (IntPtr data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGBitmapFlags bitmapInfo);
 	public CGBitmapContext (byte [] data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGBitmapFlags bitmapInfo);
</pre>
<h2>Type Changed: MonoTouch.CoreGraphics.CGGradient</h2>
<p>Added:</p><pre>
 	public CGGradient (CGColorSpace colorspace, float [] components);
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h2>Type Changed: MonoTouch.CoreMedia.CMSampleBuffer</h2>
<p>Added:</p><pre>
 	public MonoTouch.CoreVideo.CVImageBuffer GetImageBuffer ();
</pre>
<h2>Type Changed: MonoTouch.CoreMedia.CMTime</h2>
<p>Removed:</p><pre>
 	public int TimeFlags;
</pre>
<p>Added:</p><pre>
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
</pre>
<h1>Namespace: MonoTouch.CoreMotion</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h1>Namespace: MonoTouch.CoreVideo</h1>
<h2>Type Changed: MonoTouch.CoreVideo.CVImageBuffer</h2>
<p>Removed:</p><pre>
 	public void Dispose ();
 	protected override void Dispose (bool disposing);
 	public IntPtr Handle {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.CoreVideo.CVPixelBuffer</h2>
<p>Removed:</p><pre>
 public class CVPixelBuffer : CVBuffer {
 	public void Dispose ();
 	protected virtual void Dispose (bool disposing);
 	protected override void Finalize ();
 	public IntPtr Handle {
 		get;
 	}
</pre>
<p>Added:</p><pre>
 public class CVPixelBuffer : CVImageBuffer {
 	public static readonly int CVImageBufferType;
</pre>
<h1>Namespace: MonoTouch.EventKit</h1>
<h1>Namespace: MonoTouch.EventKitUI</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>New Type: MonoTouch.Foundation.NSCalculationError</h2>
<pre>
[Serializable]
public enum NSCalculationError {
	None,
	PrecisionLoss,
	Underflow,
	Overflow,
	DivideByZero
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSDecimal</h2>
<pre>
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
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSDecimalNumber</h2>
<p>Added:</p><pre>
 	public NSDecimalNumber (NSDecimal dec);
 	public virtual NSDecimal NSDecimalValue {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.Foundation.NSDirectoryEnumerationOptions</h2>
<pre>
[Serializable]
[Flags]
public enum NSDirectoryEnumerationOptions {
	SkipsNone,
	SkipsSubdirectoryDescendants,
	SkipsPackageDescendants,
	SkipsHiddenFiles
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSFileManager</h2>
<p>Added:</p><pre>
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
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSFileManagerItemReplacementOptions</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSFileManagerItemReplacementOptions
</pre>
<p>Added:</p><pre>
 [Serializable]
 [Flags]
 public enum NSFileManagerItemReplacementOptions {
 	None,
 	UsingNewMetadataOnly,
 	WithoutDeletingBackupItem
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSNumber</h2>
<p>Added:</p><pre>
 	public virtual NSDecimal NSDecimalValue {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSObject</h2>
<p>Added:</p><pre>
 	public void SetValueForKeyPath (IntPtr handle, NSString keyPath);
</pre>
<h2>New Type: MonoTouch.Foundation.NSRoundingMode</h2>
<pre>
[Serializable]
public enum NSRoundingMode {
	Plain,
	Down,
	Up,
	Bankers
}
</pre>
<h2>New Type: MonoTouch.Foundation.NSSearchPathDirectory</h2>
<pre>
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
</pre>
<h2>New Type: MonoTouch.Foundation.NSSearchPathDomain</h2>
<pre>
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
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSStringDrawingOptions</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSStringDrawingOptions
</pre>
<p>Added:</p><pre>
 [Serializable]
 public enum NSStringDrawingOptions : uint {
 	UsesLineFragmentOrigin,
 	UsesFontLeading,
 	DisableScreenFontSubstitution,
 	UsesDeviceMetrics,
 	OneShot,
 	TruncatesLastVisibleLine
 }
</pre>
<h2>New Type: MonoTouch.Foundation.NSVolumeEnumerationOptions</h2>
<pre>
[Serializable]
[Flags]
public enum NSVolumeEnumerationOptions {
	None,
	SkipHiddenVolumes,
	ProduceFileReferenceUrls
}
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.ImageIO</h1>
<h1>Namespace: MonoTouch.MapKit</h1>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMediaItemArtwork</h2>
<p>Removed:</p><pre>
 	public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.RectangleF size);
</pre>
<p>Added:</p><pre>
 	public virtual MonoTouch.UIKit.UIImage ImageWithSize (System.Drawing.SizeF size);
</pre>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5, IntPtr arg6);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, int arg4, IntPtr arg5, IntPtr arg6);
 	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, bool arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSend_NSDecimal (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSDecimal arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, bool arg4, IntPtr arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_NSDecimal (IntPtr receiver, IntPtr selector, MonoTouch.Foundation.NSDecimal arg1);
 	public static void NSDecimal_objc_msgSend_stret (out MonoTouch.Foundation.NSDecimal retval, IntPtr receiver, IntPtr selector);
 	public static void NSDecimal_objc_msgSendSuper_stret (out MonoTouch.Foundation.NSDecimal retval, IntPtr receiver, IntPtr selector);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.Security</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h1>Namespace: MonoTouch.iAd</h1>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
