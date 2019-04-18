---
id: 599F4B1F-F4B4-4EAD-ABB2-79F6C080AABE
title: "From 6.2.0 to 6.2.1"
---

<html><head><title>Comparison between monotouch-6.2.0.dll and monotouch-6.2.1.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.2.0";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.2.1";
</pre>
<h2>Namespace: MonoTouch.AVFoundation</h2>
<h3>Type Changed: MonoTouch.AVFoundation.AVAsset</h3>
<p>Removed:</p><pre>
 	public virtual AVAssetResourceLoader ResourceLoader {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput</h3>
<p>Removed:</p><pre>
 	public AVAssetReaderVideoCompositionOutput Create (AVAssetTrack[] videoTracks, MonoTouch.CoreVideo.CVPixelBufferAttributes settings);
 	public virtual AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
</pre>
<p>Added:</p><pre>
 	public static AVAssetReaderVideoCompositionOutput Create (AVAssetTrack[] videoTracks, MonoTouch.CoreVideo.CVPixelBufferAttributes settings);
 	public static AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, MonoTouch.Foundation.NSDictionary videoSettings);
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer</h3>
<p>Removed:</p><pre>
 	public virtual string VideoGravity {
</pre>
<p>Added:</p><pre>
 	public string VideoGravity {
</pre>
<h3>Type Changed: MonoTouch.AVFoundation.AVPlayerLayer</h3>
<p>Removed:</p><pre>
 	public virtual string VideoGravity {
</pre>
<p>Added:</p><pre>
 	public string VideoGravity {
</pre>
<h2>Namespace: MonoTouch.AudioToolbox</h2>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioChannelLayoutTag</h3>
<p>Removed:</p><pre>
 public enum AudioChannelLayoutTag {
</pre>
<p>Added:</p><pre>
 public enum AudioChannelLayoutTag : uint {
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverter</h3>
<pre>
public class AudioConverter : IDisposable {
	
	public static AudioConverter Create (AudioStreamBasicDescription sourceFormat, AudioStreamBasicDescription destinationFormat);
	public static AudioConverter Create (AudioStreamBasicDescription sourceFormat, AudioStreamBasicDescription destinationFormat, AudioClassDescription[] descriptions);
	public static AudioConverter Create (AudioStreamBasicDescription sourceFormat, AudioStreamBasicDescription destinationFormat, out AudioConverterError error);
	public AudioConverterError ConvertBuffer (byte [] input, byte [] output);
	public AudioConverterError ConvertComplexBuffer (int numberPCMFrames, AudioBuffers inputData, AudioBuffers outputData);
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public AudioConverterError FillComplexBuffer (ref int outputDataPacketSize, AudioBuffers outputData, AudioStreamPacketDescription[] packetDescription);
	protected override void Finalize ();
	public AudioConverterError Reset ();
	
	public static AudioFormatType[] DecodeFormats {
		get;
	}
	public static AudioFormatType[] EncodeFormats {
		get;
	}
	public AudioValueRange[] ApplicableEncodeBitRates {
		get;
	}
	public AudioValueRange[] ApplicableEncodeSampleRates {
		get;
	}
	public AudioValueRange[] AvailableEncodeBitRates {
		get;
	}
	public AudioChannelLayoutTag[] AvailableEncodeChannelLayoutTags {
		get;
	}
	public AudioValueRange[] AvailableEncodeSampleRates {
		get;
	}
	public int BitDepthHint {
		get;
		set;
	}
	public uint CalculateInputBufferSize {
		get;
	}
	public uint CalculateOutputBufferSize {
		get;
	}
	public bool CanResumeFromInterruption {
		get;
	}
	public int [] ChannelMap {
		get;
	}
	public AudioConverterQuality CodecQuality {
		get;
		set;
	}
	public byte [] CompressionMagicCookie {
		get;
		set;
	}
	public AudioStreamBasicDescription CurrentInputStreamDescription {
		get;
	}
	public AudioStreamBasicDescription CurrentOutputStreamDescription {
		get;
	}
	public byte [] DecompressionMagicCookie {
		get;
		set;
	}
	public double EncodeAdjustableSampleRate {
		get;
		set;
	}
	public uint EncodeBitRate {
		get;
		set;
	}
	public AudioFormat[] FormatList {
		get;
	}
	public AudioChannelLayout InputChannelLayout {
		get;
	}
	public uint MaximumInputPacketSize {
		get;
	}
	public uint MaximumOutputPacketSize {
		get;
	}
	public uint MinimumInputBufferSize {
		get;
	}
	public uint MinimumOutputBufferSize {
		get;
	}
	public AudioChannelLayout OutputChannelLayout {
		get;
	}
	public AudioConverterPrimeInfo PrimeInfo {
		get;
	}
	public AudioConverterPrimeMethod PrimeMethod {
		get;
		set;
	}
	public AudioConverterSampleRateConverterComplexity SampleRateConverterComplexity {
		get;
	}
	public double SampleRateConverterInitialPhase {
		get;
		set;
	}
	public AudioConverterQuality SampleRateConverterQuality {
		get;
	}
	
	public event AudioConverterComplexInputData InputData;
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterComplexInputData</h3>
<pre>
[Serializable]
public delegate AudioConverterError AudioConverterComplexInputData (ref int numberDataPackets, AudioBuffers data, ref AudioStreamPacketDescription[] dataPacketDescription);
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterError</h3>
<pre>
[Serializable]
public enum AudioConverterError {
	None,
	FormatNotSupported,
	OperationNotSupported,
	PropertyNotSupported,
	InvalidInputSize,
	InvalidOutputSize,
	UnspecifiedError,
	BadPropertySizeError,
	RequiresPacketDescriptionsError,
	InputSampleRateOutOfRange,
	OutputSampleRateOutOfRange,
	HardwareInUse,
	NoHardwarePermission
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterPrimeInfo</h3>
<pre>
public struct AudioConverterPrimeInfo {
	
	public int LeadingFrames;
	public int TrailingFrames;
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterPrimeMethod</h3>
<pre>
[Serializable]
public enum AudioConverterPrimeMethod {
	Pre,
	Normal,
	None
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterQuality</h3>
<pre>
[Serializable]
public enum AudioConverterQuality {
	Max,
	High,
	Medium,
	Low,
	Min
}
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioConverterSampleRateConverterComplexity</h3>
<pre>
[Serializable]
public enum AudioConverterSampleRateConverterComplexity {
	Linear,
	Normal,
	Mastering
}
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioFile</h3>
<p>Removed:</p><pre>
 	public int WritePackets (bool useCache, long inStartingPacket, AudioStreamPacketDescription[] inPacketDescriptions, IntPtr buffer, int count);
 	public int WritePackets (bool useCache, long inStartingPacket, AudioStreamPacketDescription[] inPacketDescriptions, IntPtr buffer, int count, out int errorCode);
 	public int WritePackets (bool useCache, long inStartingPacket, int numPackets, IntPtr buffer, int count);
</pre>
<p>Added:</p><pre>
 	public bool IsPropertyWritable (AudioFileProperty property);
 	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, IntPtr buffer);
 	public AudioFileError WritePackets (bool useCache, int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, IntPtr buffer);
 	public int WritePackets (bool useCache, long startingPacket, AudioStreamPacketDescription[] packetDescriptions, IntPtr buffer, int count);
 	public int WritePackets (bool useCache, long startingPacket, AudioStreamPacketDescription[] packetDescriptions, IntPtr buffer, int count, out int errorCode);
 	public int WritePackets (bool useCache, long startingPacket, int numPackets, IntPtr buffer, int count);
 		set;
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioFileError</h3>
<pre>
[Serializable]
public enum AudioFileError {
	Unspecified,
	UnsupportedFileType,
	UnsupportedDataFormat,
	UnsupportedProperty,
	BadPropertySize,
	Permissions,
	NotOptimized,
	InvalidChunk,
	DoesNotAllow64BitDataSize,
	InvalidPacketOffset,
	InvalidFile,
	FileNotOpen,
	EndOfFile,
	FileNotFound,
	FilePosition
}
</pre>
<h3>Type Changed: MonoTouch.AudioToolbox.AudioSession</h3>
<p>Added:</p><pre>
 	public event EventHandler&lt;AudioSessionRouteChangeEventArgs&gt; AudioRouteChanged;
</pre>
<h3>New Type: MonoTouch.AudioToolbox.AudioSessionRouteChangeEventArgs</h3>
<pre>
public class AudioSessionRouteChangeEventArgs : EventArgs {
	
	public AudioSessionRouteChangeEventArgs (IntPtr dictHandle);
	
	public AudioSessionInputRouteKind CurrentInputRoute {
		get;
	}
	public AudioSessionOutputRouteKind[] CurrentOutputRoutes {
		get;
	}
	public MonoTouch.Foundation.NSDictionary Dictionary {
		get;
	}
	public AudioSessionInputRouteKind PreviousInputRoute {
		get;
	}
	public AudioSessionOutputRouteKind[] PreviousOutputRoutes {
		get;
	}
	public AudioSessionRouteChangeReason Reason {
		get;
	}
}
</pre>
<h2>Namespace: MonoTouch.AudioUnit</h2>
<h3>Type Changed: MonoTouch.AudioUnit.AudioComponentDescription</h3>
<p>Removed:</p><pre>
 	public int ComponentFlags;
</pre>
<p>Added:</p><pre>
 	public AudioComponentFlag ComponentFlags;
</pre>
<h3>New Type: MonoTouch.AudioUnit.AudioComponentFlag</h3>
<pre>
[Serializable]
[Flags]
public enum AudioComponentFlag {
	Unsearchable
}
</pre>
<h3>Type Changed: MonoTouch.AudioUnit.ExtAudioFile</h3>
<p>Added:</p><pre>
 	public ExtAudioFileError SynchronizeAudioConverter ();
 	public MonoTouch.AudioToolbox.AudioConverter AudioConverter {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.AudioUnitWrapper</h2>
<h3>Type Changed: MonoTouch.AudioUnitWrapper._AudioConverter</h3>
<p>Removed:</p><pre>
 public class _AudioConverter : IDisposable {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public class _AudioConverter : IDisposable {
</pre>
<h3>Type Changed: MonoTouch.AudioUnitWrapper._AudioConverterEventArgs</h3>
<p>Removed:</p><pre>
 public class _AudioConverterEventArgs : EventArgs {
</pre>
<p>Added:</p><pre>
 [Obsolete]
public class _AudioConverterEventArgs : EventArgs {
</pre>
<h2>Namespace: MonoTouch.CoreAnimation</h2>
<h3>Type Changed: MonoTouch.CoreAnimation.CAEmitterCell</h3>
<p>Removed:</p><pre>
 	public virtual MonoTouch.CoreGraphics.CGImage Contents {
</pre>
<p>Added:</p><pre>
 	public MonoTouch.CoreGraphics.CGImage Contents {
</pre>
<h2>Namespace: MonoTouch.CoreData</h2>
<h3>Type Changed: MonoTouch.CoreData.NSAttributeDescription</h3>
<p>Removed:</p><pre>
 	public virtual void SetDefaultValue (MonoTouch.Foundation.NSObject value);
</pre>
<p>Added:</p><pre>
 	[Obsolete("Use the DefaultValue property")]
	public virtual void SetDefaultValue (MonoTouch.Foundation.NSObject value);
</pre>
<h3>Type Changed: MonoTouch.CoreData.NSManagedObjectModel</h3>
<p>Removed:</p><pre>
 	public virtual IntPtr Init {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.CoreLocation</h2>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManager</h3>
<p>Removed:</p><pre>
 	public event EventHandler DidStartMonitoringForRegion;
</pre>
<p>Added:</p><pre>
 	public event EventHandler&lt;CLRegionEventArgs&gt; DidStartMonitoringForRegion;
</pre>
<h3>Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate</h3>
<p>Removed:</p><pre>
 	public virtual void DidStartMonitoringForRegion (CLRegion region);
</pre>
<p>Added:</p><pre>
 	public virtual void DidStartMonitoringForRegion (CLLocationManager manager, CLRegion region);
 	[Obsolete("Do not override this method, override the (CLLocationManager, CLRegion) overload instead.")]
	public virtual void DidStartMonitoringForRegion (CLRegion region);
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSCalendar</h3>
<p>Added:</p><pre>
 	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate);
 	public virtual NSDateComponents Components (NSCalendarUnit unitFlags, NSDate fromDate, NSDate toDate, NSDateComponentsWrappingBehavior opts);
 	public virtual NSDate DateByAddingComponents (NSDateComponents comps, NSDate date, NSDateComponentsWrappingBehavior opts);
 	public virtual NSDate DateFromComponents (NSDateComponents comps);
</pre>
<h3>New Type: MonoTouch.Foundation.NSDateComponentsWrappingBehavior</h3>
<pre>
[Serializable]
public enum NSDateComponentsWrappingBehavior {
	None,
	WrapCalendarComponents
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSFileHandle</h3>
<pre>
public class NSFileHandle : NSObject {
	
	public NSFileHandle (NSCoder coder);
	public NSFileHandle (NSObjectFlag t);
	public NSFileHandle (IntPtr handle);
	public NSFileHandle (int fd, bool closeOnDealloc);
	public NSFileHandle (int fd);
	
	public static NSFileHandle FromNullDevice ();
	public static NSFileHandle FromStandardError ();
	public static NSFileHandle FromStandardInput ();
	public static NSFileHandle FromStandardOutput ();
	public static NSFileHandle OpenRead (string path);
	public static NSFileHandle OpenReadUrl (NSUrl url, out NSError error);
	public static NSFileHandle OpenUpdate (string path);
	public static NSFileHandle OpenUpdateUrl (NSUrl url, out NSError error);
	public static NSFileHandle OpenWrite (string path);
	public static NSFileHandle OpenWriteUrl (NSUrl url, out NSError error);
	public virtual void AcceptConnectionInBackground ();
	public virtual void AcceptConnectionInBackground (NSString[] notifyRunLoopModes);
	public virtual NSData AvailableData ();
	public virtual void CloseFile ();
	public virtual ulong OffsetInFile ();
	public virtual NSData ReadDataOfLength (uint length);
	public virtual NSData ReadDataToEndOfFile ();
	public virtual void ReadInBackground ();
	public virtual void ReadInBackground (NSString[] notifyRunLoopModes);
	public virtual void ReadToEndOfFileInBackground ();
	public virtual void ReadToEndOfFileInBackground (NSString[] notifyRunLoopModes);
	public virtual ulong SeekToEndOfFile ();
	public virtual void SeekToFileOffset (ulong offset);
	public virtual void SetReadabilityHandler (NSFileHandleUpdateHandler readCallback);
	public virtual void SetWriteabilityHandle (NSFileHandleUpdateHandler writeCallback);
	public virtual void SynchronizeFile ();
	public virtual void TruncateFileAtOffset (ulong offset);
	public virtual void WaitForDataInBackground ();
	public virtual void WaitForDataInBackground (NSString[] notifyRunLoopModes);
	public virtual void WriteData (NSData data);
	
	public static NSString ConnectionAcceptedNotification {
		get;
	}
	public static NSString DataAvailableNotification {
		get;
	}
	public static NSString OperationException {
		get;
	}
	public static NSString ReadCompletionNotification {
		get;
	}
	public static NSString ReadToEndOfFileCompletionNotification {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int FileDescriptor {
		get;
	}
	
	public static class Notifications {
		
		public static NSObject ObserveConnectionAccepted (EventHandler<nsfilehandleconnectionacceptedeventargs> handler);
		public static NSObject ObserveDataAvailable (EventHandler<nsnotificationeventargs> handler);
		public static NSObject ObserveReadCompletion (EventHandler<nsfilehandlereadeventargs> handler);
		public static NSObject ObserveReadToEndOfFileCompletion (EventHandler<nsfilehandlereadeventargs> handler);
	}
}
</nsfilehandlereadeventargs></nsfilehandlereadeventargs></nsnotificationeventargs></nsfilehandleconnectionacceptedeventargs></pre>
<h3>New Type: MonoTouch.Foundation.NSFileHandleConnectionAcceptedEventArgs</h3>
<pre>
public class NSFileHandleConnectionAcceptedEventArgs : NSNotificationEventArgs {
	
	public NSFileHandleConnectionAcceptedEventArgs (NSNotification notification);
	
	public NSFileHandle NearSocketConnection {
		get;
	}
	public int UnixErrorCode {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSFileHandleReadEventArgs</h3>
<pre>
public class NSFileHandleReadEventArgs : NSNotificationEventArgs {
	
	public NSFileHandleReadEventArgs (NSNotification notification);
	
	public NSData AvailableData {
		get;
	}
	public int UnixErrorCode {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSFileHandleUpdateHandler</h3>
<pre>
[Serializable]
public delegate void NSFileHandleUpdateHandler (NSFileHandle handle);
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSInputStream</h3>
<p>Removed:</p><pre>
 	public NSInputStream ();
</pre>
<p>Added:</p><pre>
 	protected NSInputStream ();
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSObject</h3>
<p>Added:</p><pre>
 	public NSObject (IntPtr handle, bool alloced);
 	public static void InvokeInBackground (NSAction action);
</pre>
<h3>New Type: MonoTouch.Foundation.NSPipe</h3>
<pre>
public class NSPipe : NSObject {
	
	public NSPipe ();
	public NSPipe (NSCoder coder);
	public NSPipe (NSObjectFlag t);
	public NSPipe (IntPtr handle);
	
	public static NSPipe Create ();
	protected override void Dispose (bool disposing);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual NSFileHandle ReadHandle {
		get;
	}
	public virtual NSFileHandle WriteHandle {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.Foundation.NSSearchPath</h3>
<pre>
public static class NSSearchPath {
	
	public static string [] GetDirectories (NSSearchPathDirectory directory, NSSearchPathDomain domainMask, bool expandTilde);
}
</pre>
<h3>Type Changed: MonoTouch.Foundation.NSUrlProtocol</h3>
<p>Removed:</p><pre>
 		set;
</pre>
<h2>Namespace: MonoTouch.GameKit</h2>
<h3>Type Changed: MonoTouch.GameKit.GKScore</h3>
<p>Removed:</p><pre>
 	[Obsolete("Use Date property")]
	public virtual MonoTouch.Foundation.NSDate date {
 		get;
 	}
</pre>
<h2>Namespace: MonoTouch.ObjCRuntime</h2>
<h3>Type Changed: MonoTouch.ObjCRuntime.Class</h3>
<p>Added:</p><pre>
 	public static IntPtr GetHandleIntrinsic (string name);
 	
 	public static bool ThrowOnInitFailure;
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Messaging</h3>
<p>Added:</p><pre>
 	public static IntPtr IntPtr_objc_msgSend_int_bool (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, int arg4);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_bool (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3, int arg4);
 	public static void void_objc_msgSend_intptr_intptr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
</pre>
<h3>Type Changed: MonoTouch.ObjCRuntime.Selector</h3>
<p>Added:</p><pre>
 	public bool Equals (Selector right);
</pre>
<h2>Namespace: MonoTouch.Security</h2>
<h3>Type Changed: MonoTouch.Security.SecKey</h3>
<p>Added:</p><pre>
 	public SecKey (IntPtr handle);
 	public SecKey (IntPtr handle, bool owns);
 	
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.UIApplication</h3>
<p>Removed:</p><pre>
 	public virtual void SetStatusBarHidden (bool hiddent, bool animated);
</pre>
<p>Added:</p><pre>
 	public virtual void SetStatusBarHidden (bool hidden, bool animated);
 	public static MonoTouch.Foundation.NSString StateRestorationBundleVersionKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString StateRestorationUserInterfaceIdiomKey {
 		get;
 	}
</pre>
<h3>Type Changed: MonoTouch.UIKit.UIImage</h3>
<p>Removed:</p><pre>
 	public UIImage (UIEdgeInsets capInsets, UIImageResizingMode resizingMode);
</pre>
<p>Added:</p><pre>
 	public virtual UIImage CreateResizableImage (UIEdgeInsets capInsets, UIImageResizingMode resizingMode);
</pre>
<h3>New Type: MonoTouch.UIKit.UILocalizedIndexedCollation</h3>
<pre>
public class UILocalizedIndexedCollation : MonoTouch.Foundation.NSObject {
	
	public UILocalizedIndexedCollation ();
	public UILocalizedIndexedCollation (MonoTouch.Foundation.NSCoder coder);
	public UILocalizedIndexedCollation (MonoTouch.Foundation.NSObjectFlag t);
	public UILocalizedIndexedCollation (IntPtr handle);
	
	public static UILocalizedIndexedCollation CurrentCollation ();
	public virtual int GetSectionForObject (MonoTouch.Foundation.NSObject obj, MonoTouch.ObjCRuntime.Selector collationStringSelector);
	public virtual int GetSectionForSectionIndexTitle (int indexTitleIndex);
	public virtual MonoTouch.Foundation.NSObject[] SortedArrayFromArraycollationStringSelector (MonoTouch.Foundation.NSObject[] array, MonoTouch.ObjCRuntime.Selector collationStringSelector);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual string [] SectionIndexTitles {
		get;
	}
	public virtual string [] SectionTitles {
		get;
	}
}
</pre>
<h3>New Type: MonoTouch.UIKit.UIStateRestoration</h3>
<pre>
public static class UIStateRestoration {
	
	public static MonoTouch.Foundation.NSString ViewControllerStoryboardKey {
		get;
	}
}
</pre>
</body>
</html>
