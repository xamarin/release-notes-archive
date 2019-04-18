---
id: 488EA81F-EF84-4F84-B895-F226A5C69BFA
title: "From 1.8.1 to 1.10.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Added fields:

```
public static const string AccountsLibrary = "/System/Library/Frameworks/Accounts.framework/Accounts";
	public static const string CloudKitLibrary = "/System/Library/Frameworks/CloudKit.framework/CloudKit";
	public static const string EventKitLibrary = "/System/Library/Frameworks/EventKit.framework/EventKit";
	public static const string GLKitLibrary = "/System/Library/Frameworks/GLKit.framework/GLKit";
	public static const string JavaScriptCoreLibrary = "/System/Library/Frameworks/JavaScriptCore.framework/JavaScriptCore";
	public static const string LocalAuthenticationLibrary = "/System/Library/Frameworks/LocalAuthentication.framework/LocalAuthentication";
	public static const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";
```

### New Type MonoMac.RuntimeException

```
public class RuntimeException : System.Exception, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	public RuntimeException (string message, object[] args);
	public RuntimeException (int code, string message, object[] args);
	public RuntimeException (int code, bool error, string message, object[] args);
	public RuntimeException (int code, bool error, System.Exception innerException, string message, object[] args);
	// properties
	public int Code { get; }
	public bool Error { get; }
}
```

## Namespace MonoMac.Accelerate

### Type Changed: MonoMac.Accelerate.vImage

Added methods:

```
public static vImageError ConvolveMultiKernelARGB8888 (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, short[][] kernels, uint kernel_height, uint kernel_width, int[] divisors, int[] biases, Pixel8888 backgroundColor, vImageFlags flags);
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[][] kernels, uint kernel_height, uint kernel_width, float[] biases, PixelFFFF backgroundColor, vImageFlags flags);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with 'short[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGB8888 (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, short[] kernels, uint kernel_height, uint kernel_width, int[] divisors, int[] biases, Pixel8888 backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, ref PixelFFFF backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, System.IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, PixelFFFF backgroundColor, vImageFlags flags);
```

## Namespace MonoMac.AppKit

### Type Changed: MonoMac.AppKit.NSComboBox

Added property:

```
public NSComboBoxDelegate Delegate { get; set; }
```

Added events:

```
public event System.EventHandler SelectionChanged;
	public event System.EventHandler SelectionIsChanging;
	public event System.EventHandler WillDismiss;
	public event System.EventHandler WillPopUp;
```

### Type Changed: MonoMac.AppKit.NSDocumentController

Removed property:

```
public static MonoMac.Foundation.NSObject SharedDocumentController { get; }
```

Added property:

```
public static NSDocumentController SharedDocumentController { get; }
```

### Type Changed: MonoMac.AppKit.NSGradient

Added constructors:

```
public NSGradient (NSColor[] colors, double[] locations);
	public NSGradient (NSColor[] colors, double[] locations, NSColorSpace colorSpace);
```

### New Type MonoMac.AppKit.INSComboBoxDelegate

```
public interface INSComboBoxDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.AppKit.NSComboBoxDelegate

```
public class NSComboBoxDelegate : MonoMac.AppKit.NSTextFieldDelegate, INSComboBoxDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSComboBoxDelegate ();
	public NSComboBoxDelegate (MonoMac.Foundation.NSCoder coder);
	public NSComboBoxDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSComboBoxDelegate (System.IntPtr handle);
	// methods
	public virtual void SelectionChanged (MonoMac.Foundation.NSNotification notification);
	public virtual void SelectionIsChanging (MonoMac.Foundation.NSNotification notification);
	public virtual void WillDismiss (MonoMac.Foundation.NSNotification notification);
	public virtual void WillPopUp (MonoMac.Foundation.NSNotification notification);
}
```

### New Type MonoMac.AppKit.NSComboBoxDelegate_Extensions

```
public static class NSComboBoxDelegate_Extensions {
	// methods
	public static void SelectionChanged (INSComboBoxDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void SelectionIsChanging (INSComboBoxDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillDismiss (INSComboBoxDelegate This, MonoMac.Foundation.NSNotification notification);
	public static void WillPopUp (INSComboBoxDelegate This, MonoMac.Foundation.NSNotification notification);
}
```

## Namespace MonoMac.AudioUnit

### Type Changed: MonoMac.AudioUnit.AudioUnit

Added method:

```
public uint GetElementCount (AudioUnitScopeType scope);
```

### Type Changed: MonoMac.AudioUnit.AUGraph

Added methods:

```
public AudioUnitStatus AddRenderNotify (RenderDelegate callback);
	public AudioUnitStatus RemoveRenderNotify (RenderDelegate callback);
	public AUGraphError SetNodeInputCallback (int destNode, uint destInputNumber, RenderDelegate renderDelegate);
```

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVAssetImageGenerator

Obsoleted method:

```
[Obsolete ("Use the overload that takes NSValue[] instead")]
	public virtual void GenerateCGImagesAsynchronously (MonoMac.Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate

Added method:

```
public virtual void DidCancelLoadingRequest (AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoaderDelegate_Extensions

Added method:

```
public static void DidCancelLoadingRequest (IAVAssetResourceLoaderDelegate This, AVAssetResourceLoader resourceLoader, AVAssetResourceLoadingRequest loadingRequest);
```

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoadingRequest

Added properties:

```
public virtual AVAssetResourceLoadingContentInformationRequest ContentInformationRequest { get; }
	public virtual AVAssetResourceLoadingDataRequest DataRequest { get; }
	public virtual bool IsCancelled { get; }
	public virtual MonoMac.Foundation.NSUrlRequest Redirect { get; set; }
	public virtual MonoMac.Foundation.NSUrlResponse Response { get; set; }
```

Added method:

```
public virtual void FinishLoading ();
```

Obsoleted method:

```
[Obsolete ("Use instead the Response, Redirect properties and the AVAssetResourceLoadingDataRequest.Responds and AVAssetResourceLoadingRequest.FinishLoading methods")]
	public virtual void FinishLoading (MonoMac.Foundation.NSUrlResponse usingResponse, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSUrlRequest redirect);
```

### Type Changed: MonoMac.AVFoundation.AVAudioSessionErrorCode

Added value:

```
CannotStartRecording = 561145187,
```

### Type Changed: MonoMac.AVFoundation.AVError

Added value:

```
ApplicationIsNotAuthorizedToUseDevice = 11852,
```

### Type Changed: MonoMac.AVFoundation.AVPlayerActionAtItemEnd

Added value:

```
Advance = 0,
```

### New Type MonoMac.AVFoundation.AVAssetResourceLoadingContentInformationRequest

```
public class AVAssetResourceLoadingContentInformationRequest : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingContentInformationRequest ();
	public AVAssetResourceLoadingContentInformationRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoadingContentInformationRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingContentInformationRequest (System.IntPtr handle);
	// properties
	public virtual bool ByteRangeAccessSupported { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual long ContentLength { get; set; }
	public virtual string ContentType { get; set; }
}
```

### New Type MonoMac.AVFoundation.AVAssetResourceLoadingDataRequest

```
public class AVAssetResourceLoadingDataRequest : MonoMac.Foundation.NSObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAssetResourceLoadingDataRequest (MonoMac.Foundation.NSCoder coder);
	public AVAssetResourceLoadingDataRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAssetResourceLoadingDataRequest (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual long CurrentOffset { get; }
	public virtual int RequestedLength { get; }
	public virtual long RequestedOffset { get; }
	// methods
	public virtual void Respond (MonoMac.Foundation.NSData responseData);
	public override string ToString ();
}
```

## Namespace MonoMac.CoreAnimation

### Type Changed: MonoMac.CoreAnimation.CAAnimation

Added properties:

```
public static MonoMac.Foundation.NSString AnimationCubic { get; }
	public static MonoMac.Foundation.NSString AnimationCubicPaced { get; }
```

### Type Changed: MonoMac.CoreAnimation.CAFillMode

Removed fields:

```
public static const string Backwards = "backwards";
	public static const string Both = "both";
	public static const string Forwards = "forwards";
	public static const string Frozen = "frozen";
	public static const string Removed = "removed";
```

Added properties:

```
public static MonoMac.Foundation.NSString Backwards { get; }
	public static MonoMac.Foundation.NSString Both { get; }
	public static MonoMac.Foundation.NSString Forwards { get; }
	public static MonoMac.Foundation.NSString Frozen { get; }
	public static MonoMac.Foundation.NSString Removed { get; }
```

## Namespace MonoMac.CoreBluetooth

### Type Changed: MonoMac.CoreBluetooth.CBError

Added value:

```
ConnectionFailed = 10,
```

## Namespace MonoMac.CoreData

### Type Changed: MonoMac.CoreData.NSAttributeType

Added value:

```
ObjectID = 2000,
```

## Namespace MonoMac.CoreFoundation

### Type Changed: MonoMac.CoreFoundation.CFAllocator

Added method:

```
public static int GetTypeID ();
```

### Type Changed: MonoMac.CoreFoundation.CFReadStream

Removed method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
```

Added method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
```

### Type Changed: MonoMac.CoreFoundation.CFStream

Removed method:

```
protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
```

Added method:

```
protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
```

### Type Changed: MonoMac.CoreFoundation.CFWriteStream

Removed method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, System.IntPtr context);
```

Added method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, System.IntPtr context);
```

### Type Changed: MonoMac.CoreFoundation.DispatchQueuePriority

Added value:

```
Background = -32768,
```

## Namespace MonoMac.CoreGraphics

### Type Changed: MonoMac.CoreGraphics.CGAffineTransform

Added methods:

```
public static CGAffineTransform Rotate (CGAffineTransform transform, float angle);
	public static CGAffineTransform Scale (CGAffineTransform transform, float sx, float sy);
	public static CGAffineTransform Translate (CGAffineTransform transform, float tx, float ty);
```

### Type Changed: MonoMac.CoreGraphics.CGDataConsumer

Added constructor:

```
public CGDataConsumer (MonoMac.Foundation.NSUrl url);
```

### Type Changed: MonoMac.CoreGraphics.CGEvent

Added constructors:

```
public CGEvent (CGEventSource eventSource);
	public CGEvent (System.IntPtr handle);
	public CGEvent (CGEventSource source, CGEventType mouseType, System.Drawing.PointF mouseCursorPosition, CGMouseButton mouseButton);
	public CGEvent (CGEventSource source, ushort virtualKey, bool keyDown);
	public CGEvent (CGEventSource source, CGScrollEventUnit units, int[] wheel);
```

Removed properties:

```
public CGEventFlags Flags { get; }
	public System.Drawing.PointF Location { get; }
```

Added properties:

```
public CGEventType EventType { get; set; }
	public CGEventFlags Flags { get; set; }
	public System.Drawing.PointF Location { get; set; }
	public ulong Timestampe { get; set; }
	public System.Drawing.PointF UnflippedLocation { get; }
```

Added methods:

```
public CGEventSource CreateEventSource ();
	public static MonoMac.CoreFoundation.CFMachPort CreateTap (System.IntPtr processSerialNumber, CGEventTapLocation location, CGEventTapPlacement place, CGEventTapOptions options, CGEventMask mask, CGEvent.CGEventTapCallback cback, System.IntPtr data);
	public CGEventTapInformation[] GetEventTapList ();
	public string GetUnicodeString ();
	public static bool IsTapEnabled (MonoMac.CoreFoundation.CFMachPort machPort);
	public static void Post (CGEvent evt, CGEventTapLocation location);
	public static void PostToPSN (CGEvent evt, System.IntPtr processSerialNumber);
	public void SetEventSource (CGEventSource eventSource);
	public void SetUnicodeString (string value);
	public static void TapDisable (MonoMac.CoreFoundation.CFMachPort machPort);
	public static void TapEnable (MonoMac.CoreFoundation.CFMachPort machPort);
	public static void TapPostEven (System.IntPtr tapProxyEvent, CGEvent evt);
```

### Type Changed: MonoMac.CoreGraphics.CGEvent.CGEventTapCallback

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo, System.AsyncCallback callback, object object);
	public virtual System.IntPtr Invoke (System.IntPtr proxy, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (System.IntPtr tapProxyEvent, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo, System.AsyncCallback callback, object object);
	public virtual System.IntPtr Invoke (System.IntPtr tapProxyEvent, CGEventType eventType, System.IntPtr eventRef, System.IntPtr userInfo);
```

### Type Changed: MonoMac.CoreGraphics.CGPath

Added constructor:

```
public CGPath (CGPath reference, CGAffineTransform transform);
```

Added methods:

```
public void AddEllipseInRect (System.Drawing.RectangleF rect);
	public CGPath CopyByDashingPath (float[] lengths, float phase);
	public CGPath CopyByDashingPath (CGAffineTransform transform, float[] lengths);
	public CGPath CopyByDashingPath (float[] lengths);
	public CGPath CopyByDashingPath (CGAffineTransform transform, float[] lengths, float phase);
	public CGPath CopyByStrokingPath (CGAffineTransform transform, float lineWidth, CGLineCap lineCap, CGLineJoin lineJoin, float miterLimit);
	public CGPath CopyByStrokingPath (float lineWidth, CGLineCap lineCap, CGLineJoin lineJoin, float miterLimit);
	public static CGPath EllipseFromRect (System.Drawing.RectangleF boundingRect);
	public static CGPath EllipseFromRect (System.Drawing.RectangleF boundingRect, CGAffineTransform transform);
	public static CGPath FromRect (System.Drawing.RectangleF rectangle);
	public static CGPath FromRect (System.Drawing.RectangleF rectangle, CGAffineTransform transform);
```

Obsoleted method:

```
[Obsolete ("Use AddEllipseInRect instead")]
	public void AddElipseInRect (System.Drawing.RectangleF rect);
```

### Type Changed: MonoMac.CoreGraphics.CGPDFDictionary

Added method:

```
public void Apply (System.Action<System.String,MonoMac.CoreGraphics.CGPDFObject> callback);
```

Obsoleted method:

```
[Obsolete ("Use the Apply(Action method")]
	public void Apply (System.Action<System.String,System.Object> callback);
```

### Type Changed: MonoMac.CoreGraphics.CGPDFStream

Obsoleted property:

```
[Obsolete ("Use GetData(out CGPDFDataFormat) instead")]
	public MonoMac.Foundation.NSData Data { get; }
```

Added method:

```
public MonoMac.Foundation.NSData GetData (out CGPDFDataFormat format);
```

### New Type MonoMac.CoreGraphics.CGColorSpaceNames

```
public static class CGColorSpaceNames {
	// properties
	public static MonoMac.Foundation.NSString AdobeRGB1998 { get; }
	public static MonoMac.Foundation.NSString GenericCMYK { get; }
	public static MonoMac.Foundation.NSString GenericGray { get; }
	public static MonoMac.Foundation.NSString GenericGrayGamma2_2 { get; }
	public static MonoMac.Foundation.NSString GenericRGB { get; }
	public static MonoMac.Foundation.NSString GenericRGBLinear { get; }
	public static MonoMac.Foundation.NSString SRGB { get; }
}
```

### New Type MonoMac.CoreGraphics.CGEventTapInformation

```
public struct CGEventTapInformation {
	// fields
	public float AvgUsecLatency;
	public bool Enabled;
	public CGEventMask EventsOfInterest;
	public uint EventTapID;
	public float MaxUsecLatency;
	public float MinUsecLatency;
	public CGEventTapOptions Options;
	public int ProcessBeingTapped;
	public int TappingProcess;
	public CGEventTapLocation TapPoint;
}
```

### New Type MonoMac.CoreGraphics.CGPDFContentStream

```
public class CGPDFContentStream : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFContentStream (System.IntPtr handle);
	public CGPDFContentStream (CGPDFPage page);
	public CGPDFContentStream (CGPDFStream stream, MonoMac.Foundation.NSDictionary streamResources, CGPDFContentStream parent);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGPDFContentStream ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CGPDFObject GetResource (string category, string name);
	public CGPDFStream[] GetStreams ();
}
```

### New Type MonoMac.CoreGraphics.CGPDFDataFormat

```
[Serializable]
public enum CGPDFDataFormat {
	JPEG2000 = 2,
	JPEGEncoded = 1,
	Raw = 0,
}
```

### New Type MonoMac.CoreGraphics.CGPDFObject

```
public class CGPDFObject : MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public CGPDFObject (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public bool IsNull { get; }
	public CGPDFObjectType Type { get; }
	// methods
	public bool TryGetName (out string name);
	public bool TryGetValue (out CGPDFStream value);
	public bool TryGetValue (out CGPDFDictionary value);
	public bool TryGetValue (out CGPDFArray value);
	public bool TryGetValue (out bool value);
	public bool TryGetValue (out float value);
	public bool TryGetValue (out int value);
	public bool TryGetValue (out string value);
}
```

### New Type MonoMac.CoreGraphics.CGPDFObjectType

```
[Serializable]
public enum CGPDFObjectType {
	Array = 7,
	Boolean = 2,
	Dictionary = 8,
	Integer = 3,
	Name = 5,
	Null = 1,
	Real = 4,
	Stream = 9,
	String = 6,
}
```

### New Type MonoMac.CoreGraphics.CGPDFOperatorTable

```
public class CGPDFOperatorTable : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFOperatorTable ();
	public CGPDFOperatorTable (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	// methods
	protected override void ~CGPDFOperatorTable ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public static CGPDFScanner GetScannerFromInfo (System.IntPtr gchandle);
	public void SetCallback (string name, System.Action<CGPDFScanner,System.Object> callback);
	public void SetCallback (string name, System.Action<System.IntPtr,System.IntPtr> callback);
}
```

### New Type MonoMac.CoreGraphics.CGPDFScanner

```
public class CGPDFScanner : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CGPDFScanner (CGPDFContentStream cs, CGPDFOperatorTable table, object userInfo);
	public CGPDFScanner (System.IntPtr handle);
	// properties
	public virtual System.IntPtr Handle { get; }
	public object UserInfo { get; }
	// methods
	protected override void ~CGPDFScanner ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public CGPDFContentStream GetContentStream ();
	public bool Scan ();
	public bool TryPop (out CGPDFDictionary value);
	public bool TryPop (out CGPDFArray value);
	public bool TryPop (out string value);
	public bool TryPop (out float value);
	public bool TryPop (out int value);
	public bool TryPop (out bool value);
	public bool TryPop (out CGPDFObject value);
	public bool TryPop (out CGPDFStream value);
	public bool TryPopName (out string name);
}
```

## Namespace MonoMac.CoreImage

### Type Changed: MonoMac.CoreImage.CIAffineFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIBlendFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIBloom

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorClamp

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorControls

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorCrossPolynomial

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorCube

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorInvert

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMap

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMatrix

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorMonochrome

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIColorPosterize

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CICompositingFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIConvolutionCore

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CICrop

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDepthOfField

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIDistortionFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIExposureAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIFalseColor

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIFilter

Added property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIGammaAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIGaussianBlur

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIGloom

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIHighlightShadowAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIHueAdjust

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CILanczosScaleTransform

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMaskToAlpha

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMaximumComponent

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIMinimumComponent

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPerspectiveTile

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPerspectiveTransform

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPhotoEffect

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIPixellate

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIScreenFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CISepiaTone

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CISharpenLuminance

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIStarShineGenerator

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIStraightenFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITemperatureAndTint

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITileFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIToneCurve

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CITransitionFilter

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIUnsharpMask

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIVibrance

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIVignetteEffect

Removed property:

```
public CIImage Image { get; set; }
```

### Type Changed: MonoMac.CoreImage.CIWhitePointAdjust

Removed property:

```
public CIImage Image { get; set; }
```

## Namespace MonoMac.CoreLocation

### Type Changed: MonoMac.CoreLocation.CLLocationManagerDelegate

Added interface:

```
ICLLocationManagerDelegate
```

### New Type MonoMac.CoreLocation.CLLocationManagerDelegate_Extensions

```
public static class CLLocationManagerDelegate_Extensions {
	// methods
	public static void AuthorizationChanged (ICLLocationManagerDelegate This, CLLocationManager manager, CLAuthorizationStatus status);
	public static void DeferredUpdatesFinished (ICLLocationManagerDelegate This, CLLocationManager manager, MonoMac.Foundation.NSError error);
	public static void Failed (ICLLocationManagerDelegate This, CLLocationManager manager, MonoMac.Foundation.NSError error);
	public static void LocationsUpdated (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation[] locations);
	public static void LocationUpdatesPaused (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static void LocationUpdatesResumed (ICLLocationManagerDelegate This, CLLocationManager manager);
	public static bool ShouldDisplayHeadingCalibration (ICLLocationManagerDelegate This, CLLocationManager manager);

	[Obsolete ("Deprecated in iOS 6.0")]
	public static void UpdatedLocation (ICLLocationManagerDelegate This, CLLocationManager manager, CLLocation newLocation, CLLocation oldLocation);
}
```

### New Type MonoMac.CoreLocation.ICLLocationManagerDelegate

```
public interface ICLLocationManagerDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoMac.CoreMedia

### Type Changed: MonoMac.CoreMedia.CMBufferQueue

Added methods:

```
public static CMBufferQueue FromCallbacks (int count, CMBufferGetTime getDecodeTimeStamp, CMBufferGetTime getPresentationTimeStamp, CMBufferGetTime getDuration, CMBufferGetBool isDataReady, CMBufferCompare compare, MonoMac.Foundation.NSString dataBecameReadyNotification, CMBufferGetSize getTotalSize);
	public int GetTotalSize ();
```

### Type Changed: MonoMac.CoreMedia.CMMediaType

Removed value:

```
Metadata = 1953326452,
```

Added value:

```
Metadata = 1835365473,
```

Obsoleted field:

```
[Obsolete ("Use Metadata instead")]
	TimedMetadata = 1953326452,
```

### Type Changed: MonoMac.CoreMedia.CMTime

Added method:

```
public static CMTime Multiply (CMTime time, int multiplier, int divisor);
```

### New Type MonoMac.CoreMedia.CMBufferGetSize

```
public sealed delegate CMBufferGetSize : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferGetSize (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoMac.ObjCRuntime.INativeObject buffer, System.AsyncCallback callback, object object);
	public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (MonoMac.ObjCRuntime.INativeObject buffer);
}
```

## Namespace MonoMac.CoreMidi

### Type Changed: MonoMac.CoreMidi.MidiObject

Added constructor:

```
public MidiObject (int handle);
```

Obsoleted constructor:

```
[Obsolete ("Use the (int) overload instead")]
	public MidiObject (System.IntPtr handle);
```

### Type Changed: MonoMac.CoreMidi.MidiPacket

Added interface:

```
System.IDisposable
```

Added method:

```
public virtual void Dispose ();
```

### Type Changed: MonoMac.CoreMidi.MidiPacketsEventArgs

Added interface:

```
System.IDisposable
```

Added method:

```
public virtual void Dispose ();
```

## Namespace MonoMac.CoreServices

### Type Changed: MonoMac.CoreServices.CFHTTPStream

Added method:

```
public void SetProxy (MonoMac.CoreFoundation.CFProxySettings proxySettings);
```

## Namespace MonoMac.CoreText

### Type Changed: MonoMac.CoreText.CTParagraphStyleSettings

Added property:

```
public CTLineBoundsOptions? LineBoundsOptions { get; set; }
```

## Namespace MonoMac.CoreVideo

### Type Changed: MonoMac.CoreVideo.CVImageBuffer

Added method:

```
public static MonoMac.CoreGraphics.CGColorSpace CreateFrom (MonoMac.Foundation.NSDictionary attachments);
```

### Type Changed: MonoMac.CoreVideo.CVPixelBuffer

Added constructors:

```
public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormat);
	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);
```

Removed method:

```
public int GetWidthtOfPlane (int planeIndex);
```

Added methods:

```
public static int GetTypeID ();
	public int GetWidthOfPlane (int planeIndex);
```

### Type Changed: MonoMac.CoreVideo.CVPixelBufferAttributes

Added constructor:

```
public CVPixelBufferAttributes (CVPixelFormatType pixelFormatType, int width, int height);
```

## Namespace MonoMac.Foundation

### Type Changed: MonoMac.Foundation.DictionaryContainer

Added methods:

```
protected int? GetNIntValue (NSString key);
	protected uint? GetNUIntValue (NSString key);
```

### Type Changed: MonoMac.Foundation.ExportAttribute

Obsoleted constructor:

```
[Obsolete ("Every exported selector must include a name")]
	public ExportAttribute ();
```

### Type Changed: MonoMac.Foundation.INSMutableCopying

Added interface:

```
INSCopying
```

### Type Changed: MonoMac.Foundation.INSSecureCoding

Added interface:

```
INSCoding
```

### Type Changed: MonoMac.Foundation.NSData

Added methods:

```
public bool Save (NSUrl url, NSDataWritingOptions options, out NSError error);
	public byte[] ToArray ();
```

### Type Changed: MonoMac.Foundation.NSDecimal

Added methods:

```
public static double op_Explicit (NSDecimal value);
	public static float op_Explicit (NSDecimal value);
	public static System.Decimal op_Explicit (NSDecimal value);
	public static NSDecimal op_Implicit (System.Decimal value);
	public static NSDecimal op_Implicit (double value);
	public static NSDecimal op_Implicit (float value);
```

### Type Changed: MonoMac.Foundation.NSDecimalNumber

Added interface:

```
System.IEquatable<NSNumber>
```

### Type Changed: MonoMac.Foundation.NSInputStream

Added method:

```
public int Read (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoMac.Foundation.NSMetadataQuery

Removed property:

```
public virtual NSMetadataQueryDelegate WeakDelegate { get; set; }
```

Added property:

```
public virtual NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoMac.Foundation.NSMutableArray

Removed constructor:

```
public NSMutableArray (int capacity);
```

Added constructor:

```
public NSMutableArray (uint capacity);
```

### Type Changed: MonoMac.Foundation.NSNumber

Added interface:

```
System.IEquatable<NSNumber>
```

Added properties:

```
public virtual int LongValue { get; }
	public float NFloatValue { get; }
	public virtual uint UnsignedLongValue { get; }
```

Added methods:

```
public override bool Equals (object other);
	public virtual bool Equals (NSNumber other);
	public static NSNumber FromLong (int value);
	public static NSNumber FromUnsignedLong (uint value);
	public override int GetHashCode ();
```

### Type Changed: MonoMac.Foundation.NSObject

Removed method:

```
public virtual void PerformSelector (MonoMac.ObjCRuntime.Selector sel, NSObject obj, double delay);
```

Added methods:

```
public static bool IsNewRefcountEnabled ();
	public virtual void PerformSelector (MonoMac.ObjCRuntime.Selector selector, NSObject withObject, double delay);
```

### Type Changed: MonoMac.Foundation.NSOutputStream

Removed method:

```
public static NSObject OutputStreamToMemory ();
```

Added methods:

```
public static NSOutputStream OutputStreamToMemory ();
	public int Write (byte[] buffer);
	public int Write (byte[] buffer, int offset, uint len);
```

### Type Changed: MonoMac.Foundation.NSPredicate

Added methods:

```
public static NSPredicate FromFormat (string predicateFormat, NSObject argument);
	public static NSPredicate FromFormat (string predicateFormat);
```

### Type Changed: MonoMac.Foundation.NSStream

Added properties:

```
public NSData DataWrittenToMemoryStream { get; }
	public NSNumber FileCurrentOffset { get; }
	public NSStreamServiceType ServiceType { get; set; }
	public NSStreamSocketSecurityLevel SocketSecurityLevel { get; set; }
	public NSStreamSocksOptions SocksOptions { get; set; }
```

### Type Changed: MonoMac.Foundation.NSTimeZone

Added method:

```
public virtual string GetLocalizedName (NSTimeZoneNameStyle style, NSLocale locale);
```

### Type Changed: MonoMac.Foundation.NSWritingDirection

Removed value:

```
RightToLeft = -1,
```

Added value:

```
RightToLeft = 1,
```

### New Type MonoMac.Foundation.NSStreamServiceType

```
[Serializable]
public enum NSStreamServiceType {
	Background = 3,
	Default = 0,
	Video = 2,
	Voice = 4,
	VoIP = 1,
}
```

### New Type MonoMac.Foundation.NSStreamSocketSecurityLevel

```
[Serializable]
public enum NSStreamSocketSecurityLevel {
	NegotiatedSsl = 4,
	None = 0,
	SslV2 = 1,
	SslV3 = 2,
	TlsV1 = 3,
	Unknown = 5,
}
```

### New Type MonoMac.Foundation.NSStreamSocksOptions

```
public class NSStreamSocksOptions {
	// constructors
	public NSStreamSocksOptions ();
	// fields
	public string HostName;
	public int HostPort;
	public string Password;
	public string Username;
	public int Version;
}
```

### New Type MonoMac.Foundation.NSTimeZoneNameStyle

```
[Serializable]
public enum NSTimeZoneNameStyle {
	DaylightSaving = 2,
	Generic = 4,
	ShortDaylightSaving = 3,
	ShortGeneric = 5,
	ShortStandard = 1,
	Standard = 0,
}
```

## Namespace MonoMac.GameKit

### Type Changed: MonoMac.GameKit.GKTurnBasedEventHandlerDelegate

Added method:

```
public virtual void HandleInviteFromGameCenter (MonoMac.Foundation.NSString[] playersToInvite);
```

Obsoleted method:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public virtual void HandleInviteFromGameCenter (GKPlayer[] playersToInvite);
```

### Type Changed: MonoMac.GameKit.GKTurnBasedEventHandlerDelegate_Extensions

Added method:

```
public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, MonoMac.Foundation.NSString[] playersToInvite);
```

Obsoleted method:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, GKPlayer[] playersToInvite);
```

## Namespace MonoMac.ImageIO

### Type Changed: MonoMac.ImageIO.CGImageDestination

Added method:

```
public static CGImageDestination Create (MonoMac.CoreGraphics.CGDataConsumer consumer, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
```

### Type Changed: MonoMac.ImageIO.CGImageMetadata

Removed method:

```
public MonoMac.Foundation.NSString GetTag (CGImageMetadata parent, MonoMac.Foundation.NSString path);
```

Added method:

```
public CGImageMetadataTag GetTag (CGImageMetadata parent, MonoMac.Foundation.NSString path);
```

### Type Changed: MonoMac.ImageIO.CGImageSource

Added method:

```
public void UpdateDataProvider (MonoMac.CoreGraphics.CGDataProvider provider, bool final);
```

Obsoleted method:

```
[Obsolete ("Use UpdateDataProvider(CGDataProvider,bool)")]
	public void UpdateDataProvider (MonoMac.CoreGraphics.CGDataProvider provider);
```

## Namespace MonoMac.ObjCRuntime

### Type Changed: MonoMac.ObjCRuntime.BlockLiteral

Added property:

```
public object Target { get; }
```

Added method:

```
public T GetDelegateForBlock<T> ();
```

### Type Changed: MonoMac.ObjCRuntime.Class

Added method:

```
public static System.IntPtr GetHandleIntrinsic (string name);
```

### Type Changed: MonoMac.ObjCRuntime.Messaging

Added methods:

```
public static bool bool_objc_msgSend_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_int_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_out_Boolean_out_Boolean_out_Boolean_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_IntPtr_SecIdentity_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Security.SecIdentity arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSend_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSend_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSend_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_bool_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_CMTimeRange_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTimeRange arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_int_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, uint arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, MonoMac.CoreMedia.CMTime arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_int_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, System.IntPtr arg5, System.IntPtr arg6, System.IntPtr arg7, ref System.IntPtr arg8);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_out_Boolean_out_Boolean_out_Boolean_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out bool arg2, out bool arg3, out bool arg4, ref System.IntPtr arg5, ref System.IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static bool bool_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_IntPtr_SecIdentity_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Security.SecIdentity arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static bool bool_objc_msgSendSuper_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static bool bool_objc_msgSendSuper_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, uint arg1, ref System.IntPtr arg2);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, int arg4, ref System.IntPtr arg5);
	public static int int_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static int int_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_NSRange_UInt64_IntPtr_int_ref_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, ref System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSend_QTTime_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSend_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSend_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static System.IntPtr IntPtr_objc_msgSendSuper_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, bool arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_CMTime_out_CMTime_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.CoreMedia.CMTime arg1, out MonoMac.CoreMedia.CMTime arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, int arg2, System.IntPtr arg3, bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_ref_NSRange_ref_NSRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, int arg1, System.IntPtr arg2, ref MonoMac.Foundation.NSRange arg3, ref MonoMac.Foundation.NSRange arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, bool arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_IntPtr_out_Boolean_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, out bool arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_ref_NSPropertyListFormat_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref MonoMac.Foundation.NSPropertyListFormat arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, System.IntPtr arg4, ref System.IntPtr arg5);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, System.IntPtr arg2, ref System.IntPtr arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_NSRange_UInt64_IntPtr_int_ref_IntPtr_out_Int32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.Foundation.NSRange arg2, ulong arg3, System.IntPtr arg4, int arg5, ref System.IntPtr arg6, out int arg7);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_out_UInt32 (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, out uint arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, MonoMac.QTKit.QTTimeRange arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_ref_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, uint arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_int_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.Foundation.NSRange arg1, System.IntPtr arg2, int arg3, ref System.IntPtr arg4);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTime_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTime arg1, System.IntPtr arg2, ref System.IntPtr arg3);
	public static System.IntPtr IntPtr_objc_msgSendSuper_QTTimeRange_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, MonoMac.QTKit.QTTimeRange arg1, ref System.IntPtr arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1);
	public static uint UInt32_objc_msgSend_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static uint UInt32_objc_msgSendSuper_IntPtr_ref_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2);
	public static void void_objc_msgSend_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSend_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_ref_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, double arg3);
	public static void void_objc_msgSend_ref_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out float arg2, int arg3);
	public static void void_objc_msgSendSuper_IntPtr_int_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, System.IntPtr arg3, int arg4, ref System.IntPtr arg5, System.IntPtr arg6);
	public static void void_objc_msgSendSuper_IntPtr_int_ref_IntPtr_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, int arg2, ref System.IntPtr arg3, System.IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_ref_IntPtr_Double (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1, ref System.IntPtr arg2, double arg3);
	public static void void_objc_msgSendSuper_ref_IntPtr_out_Single_int (System.IntPtr receiver, System.IntPtr selector, ref System.IntPtr arg1, out float arg2, int arg3);
	public static float xamarin_float_objc_msgSend (System.IntPtr receiver, System.IntPtr selector);
	public static float xamarin_float_objc_msgSendSuper (System.IntPtr receiver, System.IntPtr selector);
	public static System.IntPtr xamarin_IntPtr_objc_msgSend_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
	public static System.IntPtr xamarin_IntPtr_objc_msgSendSuper_IntPtr (System.IntPtr receiver, System.IntPtr selector, System.IntPtr arg1);
```

### Type Changed: MonoMac.ObjCRuntime.PlatformHelper

Added method:

```
public static bool Is64BitOnlyOnCurrentPlatform (Platform platform);
```

### New Type MonoMac.ObjCRuntime.BaseWrapper

```
public abstract class BaseWrapper : INativeObject, System.IDisposable {
	// constructors
	public BaseWrapper (System.IntPtr handle, bool owns);
	// properties
	protected override System.IntPtr Handle { get; set; }
	// methods
	protected override void ~BaseWrapper ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

### New Type MonoMac.ObjCRuntime.ReleaseAttribute

```
public class ReleaseAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public ReleaseAttribute ();
}
```

## Namespace MonoMac.OpenGL

### New Type MonoMac.OpenGL.Matrix2

```
[Serializable]
public struct Matrix2, System.IEquatable<Matrix2> {
	// constructors
	public Matrix2 (ref Matrix2 matrix);
	public Matrix2 (float r0c0, float r0c1, float r1c0, float r1c1);
	public Matrix2 (float[] floatArray);
	// fields
	public static Matrix2 Identity;
	public float R0C0;
	public float R0C1;
	public float R1C0;
	public float R1C1;
	public static Matrix2 Zero;
	// properties
	public float Determinant { get; }
	public float Item { get; set; }
	public float Item { get; set; }
	// methods
	public static void Add (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public void Add (ref Matrix2 matrix, out Matrix2 result);
	public void Add (ref Matrix2 matrix);
	public static bool Equals (ref Matrix2 left, ref Matrix2 right);
	public virtual bool Equals (Matrix2 matrix);
	public bool Equals (ref Matrix2 matrix);
	public bool EqualsApprox (ref Matrix2 matrix, float tolerance);
	public static bool EqualsApprox (ref Matrix2 left, ref Matrix2 right, float tolerance);
	public override int GetHashCode ();
	public void Multiply (float scalar);
	public void Multiply (ref Matrix2 matrix);
	public void Multiply (float scalar, out Matrix2 result);
	public static void Multiply (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public static void Multiply (ref Matrix2 matrix, float scalar, out Matrix2 result);
	public void Multiply (ref Matrix2 matrix, out Matrix2 result);
	public static System.IntPtr op_Explicit (Matrix2 matrix);
	public static float* op_Explicit (Matrix2 matrix);
	public static float[] op_Explicit (Matrix2 matrix);
	public void Rotate (float angle);
	public void Rotate (float angle, out Matrix2 result);
	public static void Rotate (ref Matrix2 matrix, float angle, out Matrix2 result);
	public static void RotateMatrix (float angle, out Matrix2 result);
	public void Subtract (ref Matrix2 matrix);
	public static void Subtract (ref Matrix2 left, ref Matrix2 right, out Matrix2 result);
	public void Subtract (ref Matrix2 matrix, out Matrix2 result);
	public override string ToString ();
	public void Transform (ref Vector2 vector, out Vector2 result);
	public static void Transform (ref Matrix2 matrix, ref Vector2 vector);
	public static void Transform (ref Matrix2 matrix, ref Vector2 vector, out Vector2 result);
	public void Transform (ref Vector2 vector);
	public static void Transpose (ref Matrix2 matrix, out Matrix2 result);
	public void Transpose (out Matrix2 result);
	public void Transpose ();
}
```

## Namespace MonoMac.WebKit

### Type Changed: MonoMac.WebKit.IDomEventTarget

Added interface:

```
MonoMac.Foundation.INSCopying
```

## Removed Namespace MonoMac.AddressBook

### Removed Type MonoMac.AddressBook.ABAddressBook ### Removed Type MonoMac.AddressBook.ABAddressBookError ### Removed Type MonoMac.AddressBook.ABAuthorizationStatus ### Removed Type MonoMac.AddressBook.ABGroup ### Removed Type MonoMac.AddressBook.ABLabel ### Removed Type MonoMac.AddressBook.ABMultiValue`1 ### Removed Type MonoMac.AddressBook.ABMultiValueEntry`1 ### Removed Type MonoMac.AddressBook.ABMutableDateMultiValue ### Removed Type MonoMac.AddressBook.ABMutableDictionaryMultiValue ### Removed Type MonoMac.AddressBook.ABMutableMultiValue`1 ### Removed Type MonoMac.AddressBook.ABMutableStringMultiValue ### Removed Type MonoMac.AddressBook.ABPerson ### Removed Type MonoMac.AddressBook.ABPersonAddressKey ### Removed Type MonoMac.AddressBook.ABPersonCompositeNameFormat ### Removed Type MonoMac.AddressBook.ABPersonDateLabel ### Removed Type MonoMac.AddressBook.ABPersonImageFormat ### Removed Type MonoMac.AddressBook.ABPersonInstantMessageKey ### Removed Type MonoMac.AddressBook.ABPersonInstantMessageService ### Removed Type MonoMac.AddressBook.ABPersonKind ### Removed Type MonoMac.AddressBook.ABPersonPhoneLabel ### Removed Type MonoMac.AddressBook.ABPersonProperty ### Removed Type MonoMac.AddressBook.ABPersonRelatedNamesLabel ### Removed Type MonoMac.AddressBook.ABPersonSocialProfileService ### Removed Type MonoMac.AddressBook.ABPersonSortBy ### Removed Type MonoMac.AddressBook.ABPersonUrlLabel ### Removed Type MonoMac.AddressBook.ABPropertyType ### Removed Type MonoMac.AddressBook.ABRecord ### Removed Type MonoMac.AddressBook.ABRecordType ### Removed Type MonoMac.AddressBook.ABSource ### Removed Type MonoMac.AddressBook.ABSourceProperty ### Removed Type MonoMac.AddressBook.ABSourceType ### Removed Type MonoMac.AddressBook.ExternalChangeEventArgs ### Removed Type MonoMac.AddressBook.InstantMessageService ### Removed Type MonoMac.AddressBook.PersonAddress ### Removed Type MonoMac.AddressBook.SocialProfile
