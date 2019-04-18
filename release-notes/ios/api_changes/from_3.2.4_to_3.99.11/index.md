---
id: 381D3311-90D9-4EC0-B2CF-F1F4AE852887
title: "From 3.2.4 to 3.99.11"
---

<html><head><title>Comparison between monotouch.dll and monotouch.dll</title></head>
<body>
<h1>Namespace: MonoTouch</h1>
<h2>Type Changed: MonoTouch.Constants</h2>
<p>Removed:</p><pre>
 	public const string Version = "3.2.4";
 	public const string AssetsLibraryLibrary = "/System/Library/Frameworks/AssetLibrary.framework/AssetLibrary";
</pre>
<p>Added:</p><pre>
 	public const string Version = "3.99.11";
 	public const string AssetsLibraryLibrary = "/System/Library/Frameworks/AssetsLibrary.framework/AssetsLibrary";
</pre>
<h1>Namespace: MonoTouch.AVFoundation</h1>
<h2>Type Changed: MonoTouch.AVFoundation.AVAsset</h2>
<p>Added:</p><pre>
 	public virtual AVMetadataItem[] ChapterMetadataGroups (MonoTouch.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
 	public virtual MonoTouch.Foundation.NSLocale[] AvailableChapterLocales {
 		get;
 	}
 	public virtual bool Composable {
 		get;
 	}
 	public virtual bool Exportable {
 		get;
 	}
 	public virtual bool Playable {
 		get;
 	}
 	public virtual bool Readable {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAssetExportSession</h2>
<p>Removed:</p><pre>
 	public virtual void ExportAsynchronously (AVErrorHandler errorHandler);
</pre>
<p>Added:</p><pre>
 	public virtual void ExportAsynchronously (AVCompletionHandler handler);
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAssetWriter</h2>
<p>Added:</p><pre>
 	public virtual int MovieTimeScale {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput</h2>
<p>Added:</p><pre>
 	public virtual int MediaTimeScale {
 		get;
 		set;
 	}
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVCompletionHandler</h2>
<pre>
[Serializable]
public delegate void AVCompletionHandler ();
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVError</h2>
<p>Added:</p><pre>
 	DecoderNotFound,
 	EncoderNotFound,
 	ContentIsNotAuthorized,
 	DeviceIsNotAvailableInBackground,
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVMetadataItem</h2>
<p>Added:</p><pre>
 	public virtual void LoadValuesAsynchronously (string [] keys, MonoTouch.Foundation.NSAction handler);
 	public virtual AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVMutableTimedMetadataGroup</h2>
<pre>
public class AVMutableTimedMetadataGroup : AVTimedMetadataGroup {
	
	public AVMutableTimedMetadataGroup ();
	public AVMutableTimedMetadataGroup (MonoTouch.Foundation.NSCoder coder);
	public AVMutableTimedMetadataGroup (MonoTouch.Foundation.NSObjectFlag t);
	public AVMutableTimedMetadataGroup (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVMetadataItem[] Items {
		get;
		set;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange Timerange {
		get;
		set;
	}
}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItem</h2>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString DidPLayToEndTimeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ItemFailedToPlayToEndTimeErrorKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ItemFailedToPlayToEndTimeNotification {
 		get;
 	}
 	public virtual AVPlayerItemAccessLog AccessLog {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDate CurrentDate {
 		get;
 	}
 	public virtual AVPlayerItemErrorLog ErrorLog {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLog</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVPlayerItemAccessLog
</pre>
<p>Added:</p><pre>
 public class AVPlayerItemAccessLog : MonoTouch.Foundation.NSObject {
 	
 	public AVPlayerItemAccessLog ();
 	public AVPlayerItemAccessLog (MonoTouch.Foundation.NSCoder coder);
 	public AVPlayerItemAccessLog (MonoTouch.Foundation.NSObjectFlag t);
 	public AVPlayerItemAccessLog (IntPtr handle);
 	
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public virtual AVPlayerItemAccessLogEvent[] Events {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSData ExtendedLogData {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
 		get;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent
</pre>
<p>Added:</p><pre>
 public class AVPlayerItemAccessLogEvent : MonoTouch.Foundation.NSObject {
 	
 	public AVPlayerItemAccessLogEvent ();
 	public AVPlayerItemAccessLogEvent (MonoTouch.Foundation.NSCoder coder);
 	public AVPlayerItemAccessLogEvent (MonoTouch.Foundation.NSObjectFlag t);
 	public AVPlayerItemAccessLogEvent (IntPtr handle);
 	
 	public virtual long BytesTransferred {
 		get;
 	}
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public virtual int DroppedVideoFrameCount {
 		get;
 	}
 	public virtual double DurationWatched {
 		get;
 	}
 	public virtual double IndicatedBitrate {
 		get;
 	}
 	public virtual double ObservedBitrate {
 		get;
 	}
 	public virtual string PlaybackSessionID {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSData PlaybackStartDate {
 		get;
 	}
 	public virtual double PlaybackStartOffset {
 		get;
 	}
 	public virtual int SegmentedDownloadedCount {
 		get;
 	}
 	public virtual double SegmentsDownloadedDuration {
 		get;
 	}
 	public virtual string ServerAddress {
 		get;
 	}
 	public virtual int ServerAddressChangeCount {
 		get;
 	}
 	public virtual int StallCount {
 		get;
 	}
 	public virtual string Uri {
 		get;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLog</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVPlayerItemErrorLog
</pre>
<p>Added:</p><pre>
 public class AVPlayerItemErrorLog : MonoTouch.Foundation.NSObject {
 	
 	public AVPlayerItemErrorLog ();
 	public AVPlayerItemErrorLog (MonoTouch.Foundation.NSCoder coder);
 	public AVPlayerItemErrorLog (MonoTouch.Foundation.NSObjectFlag t);
 	public AVPlayerItemErrorLog (IntPtr handle);
 	
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public virtual AVPlayerItemErrorLogEvent[] Events {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSData ExtendedLogData {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
 		get;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLogEvent</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.AVFoundation.AVPlayerItemErrorLogEvent
</pre>
<p>Added:</p><pre>
 public class AVPlayerItemErrorLogEvent : MonoTouch.Foundation.NSObject {
 	
 	public AVPlayerItemErrorLogEvent ();
 	public AVPlayerItemErrorLogEvent (MonoTouch.Foundation.NSCoder coder);
 	public AVPlayerItemErrorLogEvent (MonoTouch.Foundation.NSObjectFlag t);
 	public AVPlayerItemErrorLogEvent (IntPtr handle);
 	
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSDate Date {
 		get;
 	}
 	public virtual string ErrorComment {
 		get;
 	}
 	public virtual string ErrorDomain {
 		get;
 	}
 	public virtual int ErrorStatusCode {
 		get;
 	}
 	public virtual string PlaybackSessionID {
 		get;
 	}
 	public virtual string ServerAddress {
 		get;
 	}
 	public virtual string Uri {
 		get;
 	}
 }
</pre>
<h2>New Type: MonoTouch.AVFoundation.AVTimedMetadataGroup</h2>
<pre>
public class AVTimedMetadataGroup : MonoTouch.Foundation.NSObject {
	
	public AVTimedMetadataGroup ();
	public AVTimedMetadataGroup (MonoTouch.Foundation.NSCoder coder);
	public AVTimedMetadataGroup (MonoTouch.Foundation.NSObjectFlag t);
	public AVTimedMetadataGroup (IntPtr handle);
	public AVTimedMetadataGroup (AVMetadataItem[] items, MonoTouch.CoreMedia.CMTimeRange timeRange);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual AVMetadataItem[] Items {
		get;
	}
	public virtual MonoTouch.CoreMedia.CMTimeRange TimeRange {
		get;
	}
}
</pre>
<h1>Namespace: MonoTouch.AddressBook</h1>
<h1>Namespace: MonoTouch.AddressBookUI</h1>
<h1>Namespace: MonoTouch.AssetsLibrary</h1>
<h2>Type Changed: MonoTouch.AssetsLibrary.ALAssetsGroupType</h2>
<p>Added:</p><pre>
 	GroupPhotoStream,
</pre>
<h1>Namespace: MonoTouch.AudioToolbox</h1>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioQueue</h2>
<p>Added:</p><pre>
 	public AudioStreamPacketDescription AudioStreamPacketDescription {
 		get;
 	}
 	public AudioQueueLevelMeterState[] CurrentLevelMeter {
 		get;
 	}
 	public AudioQueueLevelMeterState[] CurrentLevelMeterDB {
 		get;
 	}
 	public int DecodeBufferSizeFrames {
 		get;
 	}
 	public bool EnableLevelMetering {
 		get;
 		set;
 	}
 	public int MaximumOutputPacketSize {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.AudioToolbox.AudioQueueLevelMeterState</h2>
<p>Removed:</p><pre>
 internal struct AudioQueueLevelMeterState {
</pre>
<p>Added:</p><pre>
 public struct AudioQueueLevelMeterState {
</pre>
<h1>Namespace: MonoTouch.AudioUnit</h1>
<h1>Namespace: MonoTouch.AudioUnitWrapper</h1>
<h1>Namespace: MonoTouch.CoreAnimation</h1>
<h2>Type Changed: MonoTouch.CoreAnimation.CAAnimation</h2>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString AnimationDescrete {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AnimationLinear {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AnimationPaced {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RotateModeAuto {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RotateModeAutoReverse {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.CoreAnimation.CAShapeLayer</h2>
<p>Removed:</p><pre>
 	public virtual string FillRule {
 	public virtual string LineCap {
 	public virtual string LineJoin {
</pre>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString CapButt {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString CapRound {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString CapSquare {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FilLRuleEvenOdd {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FillRuleNonZero {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString JoinBevel {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString JoinMiter {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString JoinRound {
 		get;
 	}
 	public virtual MonoTouch.Foundation.NSString FillRule {
 	public virtual MonoTouch.Foundation.NSString LineCap {
 	public virtual MonoTouch.Foundation.NSString LineJoin {
</pre>
<h1>Namespace: MonoTouch.CoreData</h1>
<h1>Namespace: MonoTouch.CoreFoundation</h1>
<h2>Type Changed: MonoTouch.CoreFoundation.CFRunLoop</h2>
<p>Added:</p><pre>
 	public void WakeUp ();
</pre>
<h1>Namespace: MonoTouch.CoreGraphics</h1>
<h2>Type Changed: MonoTouch.CoreGraphics.CGBitmapContext</h2>
<p>Added:</p><pre>
 	public CGBitmapContext (byte [] data, int width, int height, int bitsPerComponent, int bytesPerRow, CGColorSpace colorSpace, CGImageAlphaInfo bitmapInfo);
</pre>
<h2>Type Changed: MonoTouch.CoreGraphics.CGContext</h2>
<p>Added:</p><pre>
 	public void BeginTransparencyLayer ();
 	public void BeginTransparencyLayer (MonoTouch.Foundation.NSDictionary auxiliaryInfo);
 	public void BeginTransparencyLayer (System.Drawing.RectangleF rectangle);
 	public void BeginTransparencyLayer (System.Drawing.RectangleF rectangle, MonoTouch.Foundation.NSDictionary auxiliaryInfo);
 	public void EndTransparencyLayer ();
</pre>
<h2>Type Changed: MonoTouch.CoreGraphics.CGPath</h2>
<p>Added:</p><pre>
 	public void CGPathAddLineToPoint (CGAffineTransform transform, float x, float y);
 	public void CGPathAddLineToPoint (float x, float y);
</pre>
<h1>Namespace: MonoTouch.CoreLocation</h1>
<h1>Namespace: MonoTouch.CoreMedia</h1>
<h1>Namespace: MonoTouch.CoreMotion</h1>
<h1>Namespace: MonoTouch.CoreTelephony</h1>
<h1>Namespace: MonoTouch.CoreText</h1>
<h2>Type Changed: MonoTouch.CoreText.CTFontSymbolicTraits</h2>
<p>Removed:</p><pre>
 	UIOptimized
</pre>
<p>Added:</p><pre>
 	UIOptimized,
 	ColorGlyphs
</pre>
<h2>Type Changed: MonoTouch.CoreText.CTFontTable</h2>
<p>Added:</p><pre>
 	ExtendedKerning,
</pre>
<h2>Type Changed: MonoTouch.CoreText.CTFrameAttributeKey</h2>
<p>Added:</p><pre>
 	public static readonly MonoTouch.Foundation.NSString ClippingPaths;
 	public static readonly MonoTouch.Foundation.NSString PathClippingPath;
</pre>
<h2>Type Changed: MonoTouch.CoreText.CTParagraphStyleSettings</h2>
<p>Added:</p><pre>
 	public Nullable&lt;float&gt; LineSpacingAdjustment {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; MaximumLineSpacing {
 		get;
 		set;
 	}
 	public Nullable&lt;float&gt; MinimumLineSpacing {
 		get;
 		set;
 	}
</pre>
<h1>Namespace: MonoTouch.CoreVideo</h1>
<h2>New Type: MonoTouch.CoreVideo.CVAttachmentMode</h2>
<pre>
[Serializable]
public enum CVAttachmentMode : uint {
	ShouldNotPropagate,
	ShouldPropagate
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVBuffer</h2>
<pre>
public class CVBuffer : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	public MonoTouch.Foundation.NSObject GetAttachment (MonoTouch.Foundation.NSString key, out CVAttachmentMode attachmentMode);
	public MonoTouch.Foundation.NSDictionary GetAttachments (CVAttachmentMode attachmentMode);
	public void PropogateAttachments (CVBuffer destinationBuffer);
	public void RemoveAllAttachments ();
	public void RemoveAttachment (MonoTouch.Foundation.NSString key);
	public void SetAttachment (MonoTouch.Foundation.NSString key, MonoTouch.Foundation.NSObject value, CVAttachmentMode attachmentMode);
	public void SetAttachments (MonoTouch.Foundation.NSDictionary theAttachments, CVAttachmentMode attachmentMode);
	
	public IntPtr Handle {
		get;
	}
	
	public static readonly MonoTouch.Foundation.NSString MovieTimeKey;
	public static readonly MonoTouch.Foundation.NSString TimeValueKey;
	public static readonly MonoTouch.Foundation.NSString TimeScaleKey;
	public static readonly MonoTouch.Foundation.NSString PropagatedAttachmentsKey;
	public static readonly MonoTouch.Foundation.NSString NonPropagatedAttachmentsKey;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVFillExtendedPixelsCallBack</h2>
<pre>
[Serializable]
public delegate bool CVFillExtendedPixelsCallBack (IntPtr pixelBuffer, IntPtr refCon);
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVFillExtendedPixelsCallBackData</h2>
<pre>
public struct CVFillExtendedPixelsCallBackData {
	
	public int Version;
	public CVFillExtendedPixelsCallBack FillCallBack;
	public IntPtr UserInfo;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVImageBuffer</h2>
<pre>
public class CVImageBuffer : CVBuffer {
	
	public void Dispose ();
	protected override void Dispose (bool disposing);
	protected override void Finalize ();
	
	public System.Drawing.RectangleF CleanRect {
		get;
	}
	public System.Drawing.SizeF DisplaySize {
		get;
	}
	public System.Drawing.SizeF EncodedSize {
		get;
	}
	public IntPtr Handle {
		get;
	}
	
	public static readonly MonoTouch.Foundation.NSString CGColorSpaceKey;
	public static readonly MonoTouch.Foundation.NSString GammaLevelKey;
	public static readonly MonoTouch.Foundation.NSString CleanApertureKey;
	public static readonly MonoTouch.Foundation.NSString PreferredCleanApertureKey;
	public static readonly MonoTouch.Foundation.NSString CleanApertureWidthKey;
	public static readonly MonoTouch.Foundation.NSString CleanApertureHeightKey;
	public static readonly MonoTouch.Foundation.NSString CleanApertureHorizontalOffsetKey;
	public static readonly MonoTouch.Foundation.NSString CleanApertureVerticalOffsetKey;
	public static readonly MonoTouch.Foundation.NSString FieldCountKey;
	public static readonly MonoTouch.Foundation.NSString FieldDetailKey;
	public static readonly MonoTouch.Foundation.NSString FieldDetailTemporalTopFirst;
	public static readonly MonoTouch.Foundation.NSString FieldDetailTemporalBottomFirst;
	public static readonly MonoTouch.Foundation.NSString FieldDetailSpatialFirstLineEarly;
	public static readonly MonoTouch.Foundation.NSString FieldDetailSpatialFirstLineLate;
	public static readonly MonoTouch.Foundation.NSString PixelAspectRatioKey;
	public static readonly MonoTouch.Foundation.NSString PixelAspectRatioHorizontalSpacingKey;
	public static readonly MonoTouch.Foundation.NSString PixelAspectRatioVerticalSpacingKey;
	public static readonly MonoTouch.Foundation.NSString DisplayDimensionsKey;
	public static readonly MonoTouch.Foundation.NSString DisplayWidthKey;
	public static readonly MonoTouch.Foundation.NSString DisplayHeightKey;
	public static readonly MonoTouch.Foundation.NSString YCbCrMatrixKey;
	public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_ITU_R_709_2;
	public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_ITU_R_601_4;
	public static readonly MonoTouch.Foundation.NSString YCbCrMatrix_SMPTE_240M_1995;
	public static readonly MonoTouch.Foundation.NSString ChromaSubsamplingKey;
	public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_420;
	public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_422;
	public static readonly MonoTouch.Foundation.NSString ChromaSubsampling_411;
	public static readonly MonoTouch.Foundation.NSString TransferFunctionKey;
	public static readonly MonoTouch.Foundation.NSString TransferFunction_ITU_R_709_2;
	public static readonly MonoTouch.Foundation.NSString TransferFunction_SMPTE_240M_1995;
	public static readonly MonoTouch.Foundation.NSString TransferFunction_UseGamma;
	public static readonly MonoTouch.Foundation.NSString ChromaLocationTopFieldKey;
	public static readonly MonoTouch.Foundation.NSString ChromaLocationBottomFieldKey;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_Left;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_Center;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_TopLeft;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_Top;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_BottomLeft;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_Bottom;
	public static readonly MonoTouch.Foundation.NSString ChromaLocation_DV420;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVOptionFlags</h2>
<pre>
[Serializable]
public enum CVOptionFlags : long {
	None
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPixelBuffer</h2>
<pre>
public class CVPixelBuffer : CVBuffer {
	
	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
	
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CVReturn FillExtendedPixels ();
	protected override void Finalize ();
	public MonoTouch.Foundation.NSDictionary GetAttributes (MonoTouch.Foundation.NSDictionary[] attributes);
	public IntPtr GetBaseAddress (int planeIndex);
	public int GetBytesPerRowOfPlane (int planeIndex);
	public int GetHeightOfPlane (int planeIndex);
	public int GetWidthtOfPlane (int planeIndex);
	public CVReturn Lock (CVOptionFlags lockFlags);
	public CVReturn Unlock (CVOptionFlags unlockFlags);
	
	public IntPtr BaseAddress {
		get;
	}
	public int BytesPerRow {
		get;
	}
	public int DataSize {
		get;
	}
	public IntPtr Handle {
		get;
	}
	public int Height {
		get;
	}
	public bool IsPlanar {
		get;
	}
	public CVPixelFormatType PixelFormatType {
		get;
	}
	public int PlaneCount {
		get;
	}
	public int Width {
		get;
	}
	
	public static readonly MonoTouch.Foundation.NSString PixelFormatTypeKey;
	public static readonly MonoTouch.Foundation.NSString MemoryAllocatorKey;
	public static readonly MonoTouch.Foundation.NSString WidthKey;
	public static readonly MonoTouch.Foundation.NSString HeightKey;
	public static readonly MonoTouch.Foundation.NSString ExtendedPixelsLeftKey;
	public static readonly MonoTouch.Foundation.NSString ExtendedPixelsTopKey;
	public static readonly MonoTouch.Foundation.NSString ExtendedPixelsRightKey;
	public static readonly MonoTouch.Foundation.NSString ExtendedPixelsBottomKey;
	public static readonly MonoTouch.Foundation.NSString BytesPerRowAlignmentKey;
	public static readonly MonoTouch.Foundation.NSString CGBitmapContextCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString CGImageCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString OpenGLCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString IOSurfacePropertiesKey;
	public static readonly MonoTouch.Foundation.NSString PlaneAlignmentKey;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPixelBufferLock</h2>
<pre>
[Serializable]
[Flags]
public enum CVPixelBufferLock {
	ReadOnly
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPixelBufferPool</h2>
<pre>
public class CVPixelBufferPool : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
	
	public CVPixelBufferPool (MonoTouch.Foundation.NSDictionary poolAttributes, MonoTouch.Foundation.NSDictionary pixelBufferAttributes);
	
	public CVPixelBuffer CreatePixelBuffer ();
	public void Dispose ();
	protected virtual void Dispose (bool disposing);
	protected override void Finalize ();
	
	public MonoTouch.Foundation.NSDictionary Attributes {
		get;
	}
	public IntPtr Handle {
		get;
	}
	public MonoTouch.Foundation.NSDictionary PixelBufferAttributes {
		get;
	}
	public int TypeID {
		get;
	}
	
	public static readonly MonoTouch.Foundation.NSString MinimumBufferCountKey;
	public static readonly MonoTouch.Foundation.NSString MaximumBufferAgeKey;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPixelFormatDescription</h2>
<pre>
public static class CVPixelFormatDescription {
	
	public static MonoTouch.Foundation.NSDictionary Create (int pixelFormat);
	public static void Register (MonoTouch.Foundation.NSDictionary description, int pixelFormat);
	
	public static MonoTouch.Foundation.NSDictionary[] AllTypes {
		get;
	}
	
	public static readonly MonoTouch.Foundation.NSString NameKey;
	public static readonly MonoTouch.Foundation.NSString ConstantKey;
	public static readonly MonoTouch.Foundation.NSString CodecTypeKey;
	public static readonly MonoTouch.Foundation.NSString FourCCKey;
	public static readonly MonoTouch.Foundation.NSString PlanesKey;
	public static readonly MonoTouch.Foundation.NSString BlockWidthKey;
	public static readonly MonoTouch.Foundation.NSString BlockHeightKey;
	public static readonly MonoTouch.Foundation.NSString BitsPerBlockKey;
	public static readonly MonoTouch.Foundation.NSString BlockHorizontalAlignmentKey;
	public static readonly MonoTouch.Foundation.NSString BlockVerticalAlignmentKey;
	public static readonly MonoTouch.Foundation.NSString BlackBlockKey;
	public static readonly MonoTouch.Foundation.NSString HorizontalSubsamplingKey;
	public static readonly MonoTouch.Foundation.NSString VerticalSubsamplingKey;
	public static readonly MonoTouch.Foundation.NSString OpenGLFormatKey;
	public static readonly MonoTouch.Foundation.NSString OpenGLTypeKey;
	public static readonly MonoTouch.Foundation.NSString OpenGLInternalFormatKey;
	public static readonly MonoTouch.Foundation.NSString CGBitmapInfoKey;
	public static readonly MonoTouch.Foundation.NSString QDCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString CGBitmapContextCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString CGImageCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString OpenGLCompatibilityKey;
	public static readonly MonoTouch.Foundation.NSString FillExtendedPixelsCallbackKey;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPixelFormatType</h2>
<pre>
[Serializable]
public enum CVPixelFormatType : uint {
	CV1Monochrome,
	CV2Indexed,
	CV4Indexed,
	CV8Indexed,
	CV1IndexedGray_WhiteIsZero,
	CV2IndexedGray_WhiteIsZero,
	CV4IndexedGray_WhiteIsZero,
	CV8IndexedGray_WhiteIsZero,
	CV16BE555,
	CV24RGB,
	CV32ARGB,
	CV16LE555,
	CV16LE5551,
	CV16BE565,
	CV16LE565,
	CV24BGR,
	CV32BGRA,
	CV32ABGR,
	CV32RGBA,
	CV64ARGB,
	CV48RGB,
	CV32AlphaGray,
	CV16Gray,
	CV422YpCbCr8,
	CV4444YpCbCrA8,
	CV4444YpCbCrA8R,
	CV444YpCbCr8,
	CV422YpCbCr16,
	CV422YpCbCr10,
	CV444YpCbCr10,
	CV420YpCbCr8Planar,
	CV420YpCbCr8PlanarFullRange,
	CV422YpCbCr_4A_8BiPlanar,
	CV420YpCbCr8BiPlanarVideoRange,
	CV420YpCbCr8BiPlanarFullRange,
	CV422YpCbCr8_yuvs,
	CV422YpCbCr8FullRange,
	CV30RGB,
	CV4444AYpCbCr8,
	CV4444AYpCbCr16
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPlanarComponentInfo</h2>
<pre>
public struct CVPlanarComponentInfo {
	
	public int Offset;
	public uint RowBytes;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPlanarPixelBufferInfo</h2>
<pre>
public struct CVPlanarPixelBufferInfo {
	
	public CVPlanarComponentInfo[] ComponentInfo;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVPlanarPixelBufferInfo_YCbCrPlanar</h2>
<pre>
public struct CVPlanarPixelBufferInfo_YCbCrPlanar {
	
	public CVPlanarComponentInfo ComponentInfoY;
	public CVPlanarComponentInfo ComponentInfoCb;
	public CVPlanarComponentInfo ComponentInfoCr;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVReturn</h2>
<pre>
[Serializable]
public enum CVReturn {
	Success,
	First,
	Error,
	InvalidArgument,
	AllocationFailed,
	InvalidDisplay,
	DisplayLinkAlreadyRunning,
	DisplayLinkNotRunning,
	DisplayLinkCallbacksNotSet,
	InvalidPixelFormat,
	InvalidSize,
	InvalidPixelBufferAttributes,
	PixelBufferNotOpenGLCompatible,
	PoolAllocationFailed,
	InvalidPoolAttributes,
	Last
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVSMPTETime</h2>
<pre>
public struct CVSMPTETime {
	
	public short Subframes;
	public short SubframeDivisor;
	public uint Counter;
	public uint Type;
	public uint Flags;
	public short Hours;
	public short Minutes;
	public short Seconds;
	public short Frames;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVSMPTETimeFlags</h2>
<pre>
[Serializable]
[Flags]
public enum CVSMPTETimeFlags {
	Valid,
	Running
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVSMPTETimeType</h2>
<pre>
[Serializable]
public enum CVSMPTETimeType {
	Type24,
	Type25,
	Type30Drop,
	Type30,
	Type2997,
	Type2997Drop,
	Type60,
	Type5994
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVTime</h2>
<pre>
public struct CVTime {
	
	public static long GetCurrentHostTime ();
	public static double GetHostClockFrequency ();
	public static int GetHostClockMinimumTimeDelta ();
	public override bool Equals (object other);
	
	public static CVTime IndefiniteTime {
		get;
	}
	public static CVTime ZeroTime {
		get;
	}
	
	public long TimeValue;
	public long TimeScale;
	public int Flags;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVTimeFlags</h2>
<pre>
[Serializable]
[Flags]
public enum CVTimeFlags {
	IsIndefinite
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVTimeStamp</h2>
<pre>
public struct CVTimeStamp {
	
	public uint Version;
	public int VideoTimeScale;
	public long VideoTime;
	public ulong HostTime;
	public double RateScalar;
	public long VideoRefreshPeriod;
	public CVSMPTETime SMPTETime;
	public ulong Flags;
	public ulong Reserved;
}
</pre>
<h2>New Type: MonoTouch.CoreVideo.CVTimeStampFlags</h2>
<pre>
[Serializable]
[Flags]
public enum CVTimeStampFlags {
	VideoTimeValid,
	HostTimeValid,
	SMPTETimeValid,
	VideoRefreshPeriodValid,
	RateScalarValid,
	TopField,
	BottomField,
	VideoHostTimeValid,
	IsInterlaced
}
</pre>
<h1>Namespace: MonoTouch.EventKit</h1>
<h2>Type Changed: MonoTouch.EventKit.EKEventStore</h2>
<p>Removed:</p><pre>
 	public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, IntPtr ptrToNserror);
 	public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, IntPtr ptrToNsError);
</pre>
<p>Added:</p><pre>
 	public virtual bool RemoveEvents (EKEvent theEvent, EKSpan span, out MonoTouch.Foundation.NSError error);
 	public virtual bool SaveEvent (EKEvent theEvent, EKSpan span, out MonoTouch.Foundation.NSError error);
</pre>
<h1>Namespace: MonoTouch.EventKitUI</h1>
<h1>Namespace: MonoTouch.ExternalAccessory</h1>
<h1>Namespace: MonoTouch.Foundation</h1>
<h2>Type Changed: MonoTouch.Foundation.NSAttributedString</h2>
<p>Added:</p><pre>
 	public static NSString LigatureAttributeName {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.Foundation.NSFileAttributes</h2>
<pre>
public class NSFileAttributes {
	
	public NSFileAttributes ();
	
	public static NSFileAttributes FromDict (NSDictionary dict);
	
	public Nullable<bool> AppendOnly {
		get;
		set;
	}
	public Nullable<bool> Busy {
		get;
		set;
	}
	public NSDate CreationDate {
		get;
		set;
	}
	public Nullable<uint> DeviceIdentifier {
		get;
		set;
	}
	public Nullable<bool> FileExtensionHidden {
		get;
		set;
	}
	public Nullable<uint> FileGroupOwnerAccountID {
		get;
		set;
	}
	public Nullable<uint> FileOwnerAccountID {
		get;
		set;
	}
	public Nullable<uint> FileReferenceCount {
		get;
		set;
	}
	public Nullable<ulong> FileSize {
		get;
		set;
	}
	public Nullable<uint> FileSystemFileNumber {
		get;
		set;
	}
	public Nullable<nsfiletype> FileType {
		get;
		set;
	}
	public Nullable<uint> HfsTypeCode {
		get;
		set;
	}
	public Nullable<bool> Immutable {
		get;
		set;
	}
	public NSDate ModificationDate {
		get;
		set;
	}
	public string OwnerAccountName {
		get;
		set;
	}
	public Nullable<uint> PosixPermissions {
		get;
		set;
	}
}
</uint></bool></uint></nsfiletype></uint></ulong></uint></uint></uint></bool></uint></bool></bool></pre>
<h2>Type Changed: MonoTouch.Foundation.NSFileManager</h2>
<p>Removed:</p><pre>
 	public virtual NSDictionary GetAttributes (string path, out NSError error);
 	public static NSString HFSCreatorCode {
 	public static NSString HFSTypeCode {
</pre>
<p>Added:</p><pre>
 	public bool CreateDirectory (string path, bool createIntermediates, NSFileAttributes attributes);
 	public bool CreateDirectory (string path, bool createIntermediates, NSFileAttributes attributes, out NSError error);
 	public bool CreateFile (string path, NSData data, NSFileAttributes attributes);
 	public NSFileAttributes GetAttributes (string path);
 	public NSFileAttributes GetAttributes (string path, out NSError error);
 	public bool SetAttributes (NSFileAttributes attributes, string path);
 	public bool SetAttributes (NSFileAttributes attributes, string path, out NSError error);
 	public static NSString HfsCreatorCode {
 	public static NSString HfsTypeCode {
</pre>
<h2>New Type: MonoTouch.Foundation.NSFileType</h2>
<pre>
[Serializable]
public enum NSFileType {
	Directory,
	Regular,
	SymbolicLink,
	Socket,
	CharacterSpecial,
	BlockSpecial,
	Unknown
}
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSRunLoop</h2>
<p>Added:</p><pre>
 	public void Stop ();
 	public void WakeUp ();
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlConnection</h2>
<p>Added:</p><pre>
 	public static NSData SendSynchronousRequest (NSUrlRequest request, out NSUrlResponse response, out NSError error);
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocol</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocol
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocol : NSObject {
 	
 	public NSUrlProtocol ();
 	public NSUrlProtocol (NSCoder coder);
 	public NSUrlProtocol (NSObjectFlag t);
 	public NSUrlProtocol (IntPtr handle);
 	public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, NSUrlProtocolClient client);
 	
 	public static NSUrlRequest GetCanonicalRequest (NSUrlRequest forRequest);
 	public static NSObject GetProperty (string key, NSUrlRequest inRequest);
 	public static bool IsRequestCacheEquivalent (NSUrlRequest first, NSUrlRequest second);
 	public static bool RegisterClass (MonoTouch.ObjCRuntime.Class protocolClass);
 	public static void RemoveProperty (string propertyKey, NSMutableUrlRequest request);
 	public static void SetProperty (NSObject value, string key, NSMutableUrlRequest inRequest);
 	public static void UnregisterClass (MonoTouch.ObjCRuntime.Class protocolClass);
 	public virtual bool CanInitWithRequest (NSUrlRequest request);
 	public virtual void StartLoading ();
 	public virtual void StopLoading ();
 	
 	public virtual NSCachedUrlResponse CachedResponse {
 		get;
 	}
 	public override IntPtr ClassHandle {
 		get;
 	}
 	public NSUrlProtocolClient Client {
 		get;
 		set;
 	}
 	public virtual NSUrlRequest Request {
 		get;
 	}
 	public virtual NSObject WeakClient {
 		get;
 		set;
 	}
 	
 	public event EventHandler&lt;NSUrlProtocolCachedResponseEventArgs&gt; CachedResponseIsValid;
 	public event EventHandler&lt;NSUrlProtocolChallengeEventArgs&gt; CancelledAuthenticationChallenge;
 	public event EventHandler&lt;NSUrlProtocolDataEventArgs&gt; DataLoaded;
 	public event EventHandler&lt;NSUrlProtocolErrorEventArgs&gt; FailedWithError;
 	public event EventHandler FinishedLoading;
 	public event EventHandler&lt;NSUrlProtocolChallengeEventArgs&gt; ReceivedAuthenticationChallenge;
 	public event EventHandler&lt;NSUrlProtocolResponseEventArgs&gt; ReceivedResponse;
 	public event EventHandler&lt;NSUrlProtocolRedirectEventArgs&gt; Redirected;
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolCachedResponseEventArgs : EventArgs {
 	
 	public NSUrlProtocolCachedResponseEventArgs (NSCachedUrlResponse cachedResponse);
 	
 	public NSCachedUrlResponse CachedResponse {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolChallengeEventArgs : EventArgs {
 	
 	public NSUrlProtocolChallengeEventArgs (NSUrlAuthenticationChallenge challenge);
 	
 	public NSUrlAuthenticationChallenge Challenge {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolClient</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolClient
</pre>
<p>Added:</p><pre>
 public abstract class NSUrlProtocolClient : NSObject {
 	
 	public NSUrlProtocolClient ();
 	public NSUrlProtocolClient (NSCoder coder);
 	public NSUrlProtocolClient (NSObjectFlag t);
 	public NSUrlProtocolClient (IntPtr handle);
 	
 	public abstract void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
 	public abstract void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
 	public abstract void DataLoaded (NSUrlProtocol protocol, NSData data);
 	public abstract void FailedWithError (NSUrlProtocol protocol, NSError error);
 	public abstract void FinishedLoading (NSUrlProtocol protocol);
 	public abstract void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
 	public abstract void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
 	public abstract void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolDataEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolDataEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolDataEventArgs : EventArgs {
 	
 	public NSUrlProtocolDataEventArgs (NSData data);
 	
 	public NSData Data {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolErrorEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolErrorEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolErrorEventArgs : EventArgs {
 	
 	public NSUrlProtocolErrorEventArgs (NSError error);
 	
 	public NSError Error {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolRedirectEventArgs : EventArgs {
 	
 	public NSUrlProtocolRedirectEventArgs (NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
 	
 	public NSUrlRequest RedirectedToEequest {
 		get;
 		set;
 	}
 	public NSUrlResponse RedirectResponse {
 		get;
 		set;
 	}
 }
</pre>
<h2>Type Changed: MonoTouch.Foundation.NSUrlProtocolResponseEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.Foundation.NSUrlProtocolResponseEventArgs
</pre>
<p>Added:</p><pre>
 public class NSUrlProtocolResponseEventArgs : EventArgs {
 	
 	public NSUrlProtocolResponseEventArgs (NSUrlResponse response, NSUrlCacheStoragePolicy policy);
 	
 	public NSUrlCacheStoragePolicy Policy {
 		get;
 		set;
 	}
 	public NSUrlResponse Response {
 		get;
 		set;
 	}
 }
</pre>
<h1>Namespace: MonoTouch.GameKit</h1>
<h1>Namespace: MonoTouch.ImageIO</h1>
<h2>Type Changed: MonoTouch.ImageIO.CGImageDestination</h2>
<p>Removed:</p><pre>
 	public void Close ();
</pre>
<p>Added:</p><pre>
 	public bool Close ();
</pre>
<h1>Namespace: MonoTouch.MapKit</h1>
<h2>Type Changed: MonoTouch.MapKit.MKMapPoint</h2>
<p>Added:</p><pre>
 	public static MonoTouch.CoreLocation.CLLocationCoordinate2D ToCoordinate (MKMapPoint mapPoint);
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKMapRect</h2>
<p>Added:</p><pre>
 	public MKMapRect World {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKMapSize</h2>
<p>Added:</p><pre>
 	public static MKMapSize World {
 		get;
 	}
 	
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKPolygon</h2>
<p>Removed:</p><pre>
 	public virtual MKPolygon InteriorPolygons {
</pre>
<p>Added:</p><pre>
 	public virtual MKPolygon[] InteriorPolygons {
</pre>
<h2>Type Changed: MonoTouch.MapKit.MKPolyline</h2>
<p>Added:</p><pre>
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
</pre>
<h1>Namespace: MonoTouch.MediaPlayer</h1>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMediaItem</h2>
<p>Added:</p><pre>
 	public static bool CanFilterByProperty (MonoTouch.Foundation.NSString property);
 	public virtual MonoTouch.Foundation.NSObject ValueForProperty (MonoTouch.Foundation.NSString property);
 	public static MonoTouch.Foundation.NSString AlbumArtistPersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlbumArtistProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlbumPersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlbumTitleProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlbumTrackCountProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AlbumTrackNumberProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ArtistPersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ArtistProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ArtworkProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString AssetURLProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString BeatsPerMinuteProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString CommentsProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ComposerPersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ComposerProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DiscCountProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DiscNumberProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GenrePersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString GenreProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString IsCompilationProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LastPlayedDateProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LyricsProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString MediaTypeProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PlaybackDurationProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PlayCountProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PodcastPersistentIDProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PodcastTitleProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString RatingProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ReleaseDateProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SkipCountProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TitleProperty {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString UserGroupingProperty {
 		get;
 	}
</pre>
<h2>New Type: MonoTouch.MediaPlayer.MPMovieAccessLog</h2>
<pre>
public class MPMovieAccessLog : MonoTouch.Foundation.NSObject {
	
	public MPMovieAccessLog ();
	public MPMovieAccessLog (MonoTouch.Foundation.NSCoder coder);
	public MPMovieAccessLog (MonoTouch.Foundation.NSObjectFlag t);
	public MPMovieAccessLog (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MPMovieAccessLogEvent[] Events {
		get;
	}
	public virtual MonoTouch.Foundation.NSData ExtendedLogData {
		get;
	}
	public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MediaPlayer.MPMovieAccessLogEvent</h2>
<pre>
public class MPMovieAccessLogEvent : MonoTouch.Foundation.NSObject {
	
	public MPMovieAccessLogEvent ();
	public MPMovieAccessLogEvent (MonoTouch.Foundation.NSCoder coder);
	public MPMovieAccessLogEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPMovieAccessLogEvent (IntPtr handle);
	
	public virtual long BytesTransferred {
		get;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public virtual int DroppedVideoFrameCount {
		get;
	}
	public virtual double DurationWatched {
		get;
	}
	public virtual double IndicatedBitrate {
		get;
	}
	public virtual double ObservedBitrate {
		get;
	}
	public virtual string PlaybackSessionID {
		get;
	}
	public virtual MonoTouch.Foundation.NSData PlaybackStartDate {
		get;
	}
	public virtual double PlaybackStartOffset {
		get;
	}
	public virtual int SegmentedDownloadedCount {
		get;
	}
	public virtual double SegmentsDownloadedDuration {
		get;
	}
	public virtual string ServerAddress {
		get;
	}
	public virtual int ServerAddressChangeCount {
		get;
	}
	public virtual int StallCount {
		get;
	}
	public virtual string Uri {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MediaPlayer.MPMovieErrorLog</h2>
<pre>
public class MPMovieErrorLog : MonoTouch.Foundation.NSObject {
	
	public MPMovieErrorLog ();
	public MPMovieErrorLog (MonoTouch.Foundation.NSCoder coder);
	public MPMovieErrorLog (MonoTouch.Foundation.NSObjectFlag t);
	public MPMovieErrorLog (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MPMovieErrorLogEvent[] Events {
		get;
	}
	public virtual MonoTouch.Foundation.NSData ExtendedLogData {
		get;
	}
	public virtual MonoTouch.Foundation.NSStringEncoding ExtendedLogDataStringEncoding {
		get;
	}
}
</pre>
<h2>New Type: MonoTouch.MediaPlayer.MPMovieErrorLogEvent</h2>
<pre>
public class MPMovieErrorLogEvent : MonoTouch.Foundation.NSObject {
	
	public MPMovieErrorLogEvent ();
	public MPMovieErrorLogEvent (MonoTouch.Foundation.NSCoder coder);
	public MPMovieErrorLogEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPMovieErrorLogEvent (IntPtr handle);
	
	public override IntPtr ClassHandle {
		get;
	}
	public virtual MonoTouch.Foundation.NSDate Date {
		get;
	}
	public virtual string ErrorComment {
		get;
	}
	public virtual string ErrorDomain {
		get;
	}
	public virtual int ErrorStatusCode {
		get;
	}
	public virtual string PlaybackSessionID {
		get;
	}
	public virtual string ServerAddress {
		get;
	}
	public virtual string Uri {
		get;
	}
}
</pre>
<h2>Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController</h2>
<p>Added:</p><pre>
 	public static MonoTouch.Foundation.NSString DidEnterFullscreenNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DidExitFullscreenNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString DurationAvailableNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FullscreenAnimationCurveUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString FullscreenAnimationDurationUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString LoadStateDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString NaturalSizeAvailableNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString NowPlayingMovieDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PlaybackDidFinishNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PlaybackDidFinishReasonUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString PlaybackStateDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ScalingModeDidChangeNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString SourceTypeAvailableNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ThumbnailErrorKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ThumbnailImageKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ThumbnailImageRequestDidFinishNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString ThumbnailTimeKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataKeyDataType {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataKeyInfo {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataKeyLanguageCode {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataKeyMIMEType {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataKeyName {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataUpdatedNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TimedMetadataUserInfoKey {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString TypesAvailableNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillEnterFullscreenNotification {
 		get;
 	}
 	public static MonoTouch.Foundation.NSString WillExitFullscreenNotification {
 		get;
 	}
 	public virtual MPMovieAccessLog AccessLog {
 		get;
 	}
 	public virtual bool AllowsAirPlay {
 		get;
 	}
 	public virtual MPMovieErrorLog ErrorLog {
 		get;
 	}
</pre>
<h1>Namespace: MonoTouch.MessageUI</h1>
<h1>Namespace: MonoTouch.ObjCRuntime</h1>
<h2>Type Changed: MonoTouch.ObjCRuntime.BlockDescriptor</h2>
<p>Removed:</p><pre>
 	public int reserved;
 	public int size;
</pre>
<p>Added:</p><pre>
 	public IntPtr reserved;
 	public IntPtr size;
</pre>
<h2>New Type: MonoTouch.ObjCRuntime.Dlfcn</h2>
<pre>
public static class Dlfcn {
	
	public static int dlclose (IntPtr handle);
	public static string dlerror ();
	public static IntPtr dlopen (string path, int mode);
	public static double GetDouble (IntPtr handle, string symbol);
	public static IntPtr GetIndirect (IntPtr handle, string symbol);
	public static int GetInt32 (IntPtr handle, string symbol);
	public static IntPtr GetIntPtr (IntPtr handle, string symbol);
	public static MonoTouch.Foundation.NSNumber GetNSNumber (IntPtr handle, string symbol);
	public static MonoTouch.Foundation.NSString GetStringConstant (IntPtr handle, string symbol);
}
</pre>
<h2>Type Changed: MonoTouch.ObjCRuntime.Messaging</h2>
<p>Removed:</p><pre>
 	public static bool Boolean_objc_msgSend (IntPtr receiver, IntPtr selector);
 	public static bool Boolean_objc_msgSend_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static bool Boolean_objc_msgSend_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_Boolean_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSend_byte (IntPtr receiver, IntPtr selector, byte arg1);
 	public static bool Boolean_objc_msgSend_Char (IntPtr receiver, IntPtr selector, char arg1);
 	public static bool Boolean_objc_msgSend_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSend_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSend_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSend_Double (IntPtr receiver, IntPtr selector, double arg1);
 	public static bool Boolean_objc_msgSend_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSend_int (IntPtr receiver, IntPtr selector, int arg1);
 	public static bool Boolean_objc_msgSend_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static bool Boolean_objc_msgSend_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static bool Boolean_objc_msgSend_IntPtr_Boolean_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSend_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2);
 	public static bool Boolean_objc_msgSend_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
 	public static bool Boolean_objc_msgSend_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool Boolean_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool Boolean_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static bool Boolean_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSend_RectangleF_IntPtr_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static bool Boolean_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static bool Boolean_objc_msgSend_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static bool Boolean_objc_msgSendSuper_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static bool Boolean_objc_msgSendSuper_Boolean_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_Boolean_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper_byte (IntPtr receiver, IntPtr selector, byte arg1);
 	public static bool Boolean_objc_msgSendSuper_Char (IntPtr receiver, IntPtr selector, char arg1);
 	public static bool Boolean_objc_msgSendSuper_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool Boolean_objc_msgSendSuper_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool Boolean_objc_msgSendSuper_Double (IntPtr receiver, IntPtr selector, double arg1);
 	public static bool Boolean_objc_msgSendSuper_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper_int (IntPtr receiver, IntPtr selector, int arg1);
 	public static bool Boolean_objc_msgSendSuper_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_Boolean_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
 	public static bool Boolean_objc_msgSendSuper_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static bool Boolean_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool Boolean_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool Boolean_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static bool Boolean_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static bool Boolean_objc_msgSendSuper_RectangleF_IntPtr_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static bool Boolean_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static bool Boolean_objc_msgSendSuper_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static IntPtr IntPtr_objc_msgSend_Double_IntPtr_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSend_Int64_short_Boolean (IntPtr receiver, IntPtr selector, long arg1, short arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Double_IntPtr_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, bool arg6);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_Int64_short_Boolean (IntPtr receiver, IntPtr selector, long arg1, short arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double_IntPtr_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, bool arg6);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr_NSRange_int_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void NSRange_objc_msgSend_stret_IntPtr_NSRange_int_Boolean_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_NSRange_int_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void NSRange_objc_msgSendSuper_stret_IntPtr_NSRange_int_Boolean_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void void_objc_msgSend_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static void void_objc_msgSend_Boolean_Boolean (IntPtr receiver, IntPtr selector, bool arg1, bool arg2);
 	public static void void_objc_msgSend_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static void void_objc_msgSend_Boolean_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static void void_objc_msgSend_CLLocationCoordinate2D_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, bool arg2);
 	public static void void_objc_msgSend_float_Boolean (IntPtr receiver, IntPtr selector, float arg1, bool arg2);
 	public static void void_objc_msgSend_int_Boolean (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static void void_objc_msgSend_int_int_Boolean (IntPtr receiver, IntPtr selector, int arg1, int arg2, bool arg3);
 	public static void void_objc_msgSend_int_IntPtr_Boolean (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static void void_objc_msgSend_IntPtr_Boolean_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, int arg3);
 	public static void void_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static void void_objc_msgSend_IntPtr_int_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_UInt32_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static void void_objc_msgSend_MKCoordinateRegion_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateRegion arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSend_PointF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, bool arg2);
 	public static void void_objc_msgSend_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSend_RectangleF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static void void_objc_msgSend_RectangleF_IntPtr_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_RectangleF_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
 	public static void void_objc_msgSend_RectangleF_IntPtr_UInt32_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3, bool arg4);
 	public static void void_objc_msgSend_SizeF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_Boolean (IntPtr receiver, IntPtr selector, bool arg1);
 	public static void void_objc_msgSendSuper_Boolean_Boolean (IntPtr receiver, IntPtr selector, bool arg1, bool arg2);
 	public static void void_objc_msgSendSuper_Boolean_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static void void_objc_msgSendSuper_Boolean_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_CLLocationCoordinate2D_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, bool arg2);
 	public static void void_objc_msgSendSuper_float_Boolean (IntPtr receiver, IntPtr selector, float arg1, bool arg2);
 	public static void void_objc_msgSendSuper_int_Boolean (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static void void_objc_msgSendSuper_int_int_Boolean (IntPtr receiver, IntPtr selector, int arg1, int arg2, bool arg3);
 	public static void void_objc_msgSendSuper_int_IntPtr_Boolean (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static void void_objc_msgSendSuper_IntPtr_Boolean_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, int arg3);
 	public static void void_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_int_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_UInt32_Boolean (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static void void_objc_msgSendSuper_MKCoordinateRegion_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateRegion arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_UIEdgeInsets_Boolean (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSendSuper_PointF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_PointF_float_float_float_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSendSuper_RectangleF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_UInt32_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3, bool arg4);
 	public static void void_objc_msgSendSuper_SizeF_Boolean (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, bool arg2);
</pre>
<p>Added:</p><pre>
 	public static bool bool_objc_msgSend_bool (IntPtr receiver, IntPtr selector, bool arg1);
 	public static bool bool_objc_msgSend_bool_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool bool_objc_msgSend_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static bool bool_objc_msgSend_byte (IntPtr receiver, IntPtr selector, byte arg1);
 	public static bool bool_objc_msgSend_Char (IntPtr receiver, IntPtr selector, char arg1);
 	public static bool bool_objc_msgSend_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool bool_objc_msgSend_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool bool_objc_msgSend_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool bool_objc_msgSend_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSend_Double (IntPtr receiver, IntPtr selector, double arg1);
 	public static bool bool_objc_msgSend_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static bool bool_objc_msgSend_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2);
 	public static bool bool_objc_msgSend_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static bool bool_objc_msgSend_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static bool bool_objc_msgSend_IntPtr_bool_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
 	public static bool bool_objc_msgSend_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2);
 	public static bool bool_objc_msgSend_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
 	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
 	public static bool bool_objc_msgSend_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static bool bool_objc_msgSend_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool bool_objc_msgSend_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool bool_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static bool bool_objc_msgSend_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static bool bool_objc_msgSend_RectangleF_IntPtr_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static bool bool_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static bool bool_objc_msgSend_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
 	public static bool bool_objc_msgSendSuper_bool (IntPtr receiver, IntPtr selector, bool arg1);
 	public static bool bool_objc_msgSendSuper_bool_int_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, int arg2, IntPtr arg3);
 	public static bool bool_objc_msgSendSuper_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper_byte (IntPtr receiver, IntPtr selector, byte arg1);
 	public static bool bool_objc_msgSendSuper_Char (IntPtr receiver, IntPtr selector, char arg1);
 	public static bool bool_objc_msgSendSuper_CLLocationCoordinate2D (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1);
 	public static bool bool_objc_msgSendSuper_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1);
 	public static bool bool_objc_msgSendSuper_CMTime_CGAffineTransform_CGAffineTransform_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreGraphics.CGAffineTransform arg2, MonoTouch.CoreGraphics.CGAffineTransform arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_CMTime_CMTime_CMTime (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, MonoTouch.CoreMedia.CMTime arg2, MonoTouch.CoreMedia.CMTime arg3);
 	public static bool bool_objc_msgSendSuper_CMTime_float_float_CMTimeRange (IntPtr receiver, IntPtr selector, MonoTouch.CoreMedia.CMTime arg1, float arg2, float arg3, MonoTouch.CoreMedia.CMTimeRange arg4);
 	public static bool bool_objc_msgSendSuper_Double (IntPtr receiver, IntPtr selector, double arg1);
 	public static bool bool_objc_msgSendSuper_Double_IntPtr (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper_int_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1);
 	public static bool bool_objc_msgSendSuper_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3, IntPtr arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, IntPtr arg3);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, int arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
 	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
 	public static bool bool_objc_msgSendSuper_IntPtr_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, IntPtr arg3);
 	public static bool bool_objc_msgSendSuper_MKMapRect (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1);
 	public static bool bool_objc_msgSendSuper_MKMapRect_float (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, float arg2);
 	public static bool bool_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
 	public static bool bool_objc_msgSendSuper_PointF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, IntPtr arg2);
 	public static bool bool_objc_msgSendSuper_RectangleF_IntPtr_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static bool bool_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
 	public static bool bool_objc_msgSendSuper_UInt32_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, IntPtr arg2);
 	public static IntPtr IntPtr_objc_msgSend_bool (IntPtr receiver, IntPtr selector, bool arg1);
 	public static IntPtr IntPtr_objc_msgSend_Double_IntPtr_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSend_Int64_short_bool (IntPtr receiver, IntPtr selector, long arg1, short arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_Double_IntPtr_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, bool arg6);
 	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSend_PointF_float_float_float_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_bool (IntPtr receiver, IntPtr selector, bool arg1);
 	public static IntPtr IntPtr_objc_msgSendSuper_Double_IntPtr_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, double arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, bool arg5);
 	public static IntPtr IntPtr_objc_msgSendSuper_Int64_short_bool (IntPtr receiver, IntPtr selector, long arg1, short arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_CMTimeRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.CoreMedia.CMTimeRange arg2);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_Double_IntPtr_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, bool arg6);
 	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static IntPtr IntPtr_objc_msgSendSuper_PointF_float_float_float_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSend_IntPtr_NSRange_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void NSRange_objc_msgSend_stret_IntPtr_NSRange_int_bool_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static MonoTouch.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_NSRange_int_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void NSRange_objc_msgSendSuper_stret_IntPtr_NSRange_int_bool_IntPtr (out MonoTouch.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, bool arg4, IntPtr arg5);
 	public static void void_objc_msgSend_bool_bool (IntPtr receiver, IntPtr selector, bool arg1, bool arg2);
 	public static void void_objc_msgSend_bool_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static void void_objc_msgSend_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static void void_objc_msgSend_CLLocationCoordinate2D_bool (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, bool arg2);
 	public static void void_objc_msgSend_float_bool (IntPtr receiver, IntPtr selector, float arg1, bool arg2);
 	public static void void_objc_msgSend_int_bool (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static void void_objc_msgSend_int_int_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, bool arg3);
 	public static void void_objc_msgSend_int_IntPtr_bool (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static void void_objc_msgSend_IntPtr_bool_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, int arg3);
 	public static void void_objc_msgSend_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static void void_objc_msgSend_IntPtr_int_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static void void_objc_msgSend_MKCoordinateRegion_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateRegion arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSend_MKMapRect_UIEdgeInsets_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSend_PointF_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, bool arg2);
 	public static void void_objc_msgSend_PointF_float_float_float_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSend_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static void void_objc_msgSend_RectangleF_IntPtr_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSend_RectangleF_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
 	public static void void_objc_msgSend_RectangleF_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3, bool arg4);
 	public static void void_objc_msgSend_SizeF_bool (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_bool (IntPtr receiver, IntPtr selector, bool arg1);
 	public static void void_objc_msgSendSuper_bool_bool (IntPtr receiver, IntPtr selector, bool arg1, bool arg2);
 	public static void void_objc_msgSendSuper_bool_int (IntPtr receiver, IntPtr selector, bool arg1, int arg2);
 	public static void void_objc_msgSendSuper_bool_IntPtr (IntPtr receiver, IntPtr selector, bool arg1, IntPtr arg2);
 	public static void void_objc_msgSendSuper_CLLocationCoordinate2D_bool (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, bool arg2);
 	public static void void_objc_msgSendSuper_float_bool (IntPtr receiver, IntPtr selector, float arg1, bool arg2);
 	public static void void_objc_msgSendSuper_int_bool (IntPtr receiver, IntPtr selector, int arg1, bool arg2);
 	public static void void_objc_msgSendSuper_int_int_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, bool arg3);
 	public static void void_objc_msgSendSuper_int_IntPtr_bool (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2);
 	public static void void_objc_msgSendSuper_IntPtr_bool_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, int arg3);
 	public static void void_objc_msgSendSuper_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
 	public static void void_objc_msgSendSuper_IntPtr_int_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_IntPtr_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, bool arg3);
 	public static void void_objc_msgSendSuper_MKCoordinateRegion_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKCoordinateRegion arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, bool arg2);
 	public static void void_objc_msgSendSuper_MKMapRect_UIEdgeInsets_bool (IntPtr receiver, IntPtr selector, MonoTouch.MapKit.MKMapRect arg1, MonoTouch.UIKit.UIEdgeInsets arg2, bool arg3);
 	public static void void_objc_msgSendSuper_PointF_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_PointF_float_float_float_bool (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, float arg2, float arg3, float arg4, bool arg5);
 	public static void void_objc_msgSendSuper_RectangleF_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, bool arg2);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_bool_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
 	public static void void_objc_msgSendSuper_RectangleF_IntPtr_UInt32_bool (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3, bool arg4);
 	public static void void_objc_msgSendSuper_SizeF_bool (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, bool arg2);
</pre>
<h2>Type Changed: MonoTouch.ObjCRuntime.Runtime</h2>
<p>Added:</p><pre>
 	public static void ConnectMethod (System.Reflection.MethodInfo method, Selector selector);
</pre>
<h1>Namespace: MonoTouch.OpenGLES</h1>
<h1>Namespace: MonoTouch.QuickLook</h1>
<h1>Namespace: MonoTouch.Security</h1>
<h1>Namespace: MonoTouch.StoreKit</h1>
<h1>Namespace: MonoTouch.SystemConfiguration</h1>
<h1>Namespace: MonoTouch.UIKit</h1>
<h2>Type Changed: MonoTouch.UIKit.UIApplicationDelegate</h2>
<p>Removed:</p><pre>
 	public virtual void ProtectedDataDidBecomeUnavailable (UIApplication application);
</pre>
<p>Added:</p><pre>
 	public virtual void ProtectedDataDidBecomeAvailable (UIApplication application);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIButton</h2>
<p>Added:</p><pre>
 	public UIButton (UIButtonType type);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIControlEvent</h2>
<p>Added:</p><pre>
 [Flags]
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIFont</h2>
<p>Removed:</p><pre>
 	public virtual float LineHeight {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIGestureProbe</h2>
<p>Removed:</p><pre>
 public delegate bool UIGestureProbe (UIGestureRecognizer otherGestureRecognizer);
</pre>
<p>Added:</p><pre>
 public delegate bool UIGestureProbe (UIGestureRecognizer recognizer);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIGestureRecognizer</h2>
<p>Removed:</p><pre>
 	public UIGestureProbe ShouldRecognizeSimultaneously {
</pre>
<p>Added:</p><pre>
 	public Token AddTarget (MonoTouch.Foundation.NSAction action);
 	public void RemoveTarget (Token token);
 	public UIGesturesProbe ShouldRecognizeSimultaneously {
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIGestureRecognizerDelegate</h2>
<p>Removed:</p><pre>
 	public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer otherGestureRecognizer);
</pre>
<p>Added:</p><pre>
 	public virtual bool ShouldRecognizeSimultaneously (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
</pre>
<h2>New Type: MonoTouch.UIKit.UIGesturesProbe</h2>
<pre>
[Serializable]
public delegate bool UIGesturesProbe (UIGestureRecognizer gestureRecognizer, UIGestureRecognizer otherGestureRecognizer);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIScreen</h2>
<p>Added:</p><pre>
 	public virtual UIScreen MirroredScreen {
 		get;
 	}
 	public virtual UIScreenMode PreferredMode {
 		get;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIView</h2>
<p>Added:</p><pre>
 	public void AddSubviews (params UIView[] views);
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIViewController</h2>
<p>Added:</p><pre>
 	public virtual bool DisablesAutomaticKeyboardDismissal {
 		get;
 		set;
 	}
</pre>
<h2>Type Changed: MonoTouch.UIKit.UIWindow</h2>
<p>Added:</p><pre>
 		set;
</pre>
<h1>Namespace: MonoTouch.iAd</h1>
<h2>Type Changed: MonoTouch.iAd.ADError</h2>
<p>Removed:</p><pre>
 	BannerVisibleWithoutContent
</pre>
<p>Added:</p><pre>
 	BannerVisibleWithoutContent,
 	ApplicationInactive
</pre>
<h2>Type Changed: MonoTouch.iAd.ADErrorEventArgs</h2>
<p>Removed:</p><pre>
 Could not find MonoTouch.iAd.ADErrorEventArgs
</pre>
<p>Added:</p><pre>
 public class ADErrorEventArgs : EventArgs {
 	
 	public ADErrorEventArgs (MonoTouch.Foundation.NSError error);
 	
 	public MonoTouch.Foundation.NSError Error {
 		get;
 		set;
 	}
 }
</pre>
<h2>New Type: MonoTouch.iAd.ADInterstitialAd</h2>
<pre>
public class ADInterstitialAd : MonoTouch.Foundation.NSObject {
	
	public ADInterstitialAd ();
	public ADInterstitialAd (MonoTouch.Foundation.NSCoder coder);
	public ADInterstitialAd (MonoTouch.Foundation.NSObjectFlag t);
	public ADInterstitialAd (IntPtr handle);
	
	public virtual void CancelAction ();
	public virtual void PresentFromViewController (MonoTouch.UIKit.UIViewController viewController);
	public virtual bool PresentInView (MonoTouch.UIKit.UIView containerView);
	
	public virtual bool ActionInProgress {
		get;
	}
	public ADPredicate ActionShouldBegin {
		get;
		set;
	}
	public override IntPtr ClassHandle {
		get;
	}
	public ADInterstitialAdDelegate Delegate {
		get;
		set;
	}
	public virtual bool Loaded {
		get;
	}
	public virtual MonoTouch.Foundation.NSObject WeakDelegate {
		get;
		set;
	}
	
	public event EventHandler ActionFinished;
	public event EventHandler AdLoaded;
	public event EventHandler AdUnloaded;
	public event EventHandler<aderroreventargs> FailedToReceiveAd;
}
</aderroreventargs></pre>
<h2>New Type: MonoTouch.iAd.ADInterstitialAdDelegate</h2>
<pre>
public abstract class ADInterstitialAdDelegate : MonoTouch.Foundation.NSObject {
	
	public ADInterstitialAdDelegate ();
	public ADInterstitialAdDelegate (MonoTouch.Foundation.NSCoder coder);
	public ADInterstitialAdDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public ADInterstitialAdDelegate (IntPtr handle);
	
	public abstract void ActionFinished (ADInterstitialAd interstitialAd);
	public abstract bool ActionShouldBegin (ADInterstitialAd interstitialAd, bool willLeaveApplication);
	public abstract void AdLoaded (ADInterstitialAd interstitialAd);
	public abstract void AdUnloaded (ADInterstitialAd interstitialAd);
	public abstract void FailedToReceiveAd (ADInterstitialAd interstitialAd, MonoTouch.Foundation.NSError error);
}
</pre>
<h2>New Type: MonoTouch.iAd.ADPredicate</h2>
<pre>
[Serializable]
public delegate bool ADPredicate (ADInterstitialAd interstitialAd, bool willLeaveApplication);
</pre>
<h1>Namespace: System.Drawing</h1>
</body>
</html>
