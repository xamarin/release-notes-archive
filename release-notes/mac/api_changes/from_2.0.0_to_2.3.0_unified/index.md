---
id: 592F140A-767D-4432-8168-79A5F481AA3F
title: "From 2.0.0 to 2.3.0 unified"
---

# Xamarin.Mac.dll

## Namespace AppKit

### Type Changed: AppKit.NSAnimation

Added constructor:

<pre style='color: green'>
	public NSAnimation (double duration, NSAnimationCurve animationCurve);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual IntPtr Constant (double duration, NSAnimationCurve animationCurve);
```

### Type Changed: AppKit.NSApplication

Removed interface:

<pre style='color: red'>
	INSWindowRestoration
</pre>

Obsoleted methods:

```
[Obsolete (]
	public static void RestoreWindow (string identifier, Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
```

Added methods:

<pre style='color: green'>
	public virtual void CompleteStateRestoration ();
	public virtual void ExtendStateRestoration ();
	public virtual bool RestoreWindowWithIdentifier (string identifier, Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
</pre>

### Type Changed: AppKit.NSButton

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual nint MaxAcceleratorLevel { get; set; }
	public virtual NSSegmentSwitchTracking TrackingMode { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual double GetValueForSelectedSegment ();
</pre>

### Type Changed: AppKit.NSButtonType

Added values:

<pre style='color: green'>
	Accelerator = 8,
	MultiLevelAccelerator = 9,
</pre>

### Type Changed: AppKit.NSColor

Obsoleted properties:

```
[Obsolete (]
	public static NSColor UnderPageBackground { get; }
```

### Type Changed: AppKit.NSComboBox

Added property:

<pre style='color: green'>
	public Foundation.NSObject Item { get; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual NSComboBox GetItem (nint index);
```

Added method:

<pre style='color: green'>
	public virtual Foundation.NSObject GetItemObject (nint index);
</pre>

### Type Changed: AppKit.NSControlTextEditingDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSControlTextEditingDelegate_Extensions

Removed method:

<pre style='color: red'>
	public static string[] GetCompletions (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added method:

<pre style='color: green'>
	public static string[] GetCompletions (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSEvent

Added properties:

<pre style='color: green'>
	public virtual NSEventMask AssociatedEventsMask { get; }
	public virtual nint Stage { get; }
	public virtual nfloat StageTransition { get; }
</pre>

### Type Changed: AppKit.NSEventMask

Added value:

<pre style='color: green'>
	Pressure = 17179869184,
</pre>

### Type Changed: AppKit.NSEventType

Added value:

<pre style='color: green'>
	Pressure = 34,
</pre>

### Type Changed: AppKit.NSFontPanel

Removed property:

<pre style='color: red'>
	public virtual bool WorksWhenModal { get; }
</pre>

### Type Changed: AppKit.NSGestureRecognizer

Added method:

<pre style='color: green'>
	public virtual void PressureChange (NSEvent pressureChangeEvent);
</pre>

### Type Changed: AppKit.NSGraphics

Added methods:

<pre style='color: green'>
	public static void DisableScreenUpdates ();
	public static void DrawWindowBackground (CoreGraphics.CGRect aRect);
	public static void EnableScreenUpdates ();
</pre>

### Type Changed: AppKit.NSMatrixDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSOutlineViewDelegate

Obsoleted methods:

```
[Obsolete (]
	public virtual NSView ViewForTableColumn (NSOutlineView outlineView, NSTableColumn tableColumn, Foundation.NSObject item);
```

### Type Changed: AppKit.NSOutlineViewDelegate_Extensions

Obsoleted methods:

```
[Obsolete (]
	public static NSView ViewForTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, Foundation.NSObject item);
```

### Type Changed: AppKit.NSPasteboard

Removed methods:

<pre style='color: red'>
	public virtual bool CanReadObjectForClasses (Foundation.NSObject[] classArray, Foundation.NSDictionary options);
	public virtual Foundation.NSObject[] ReadObjectsForClasses (INSPasteboardReading[] classArray, Foundation.NSDictionary options);
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanReadObjectForClasses (ObjCRuntime.Class[] classArray, Foundation.NSDictionary options);
	public virtual Foundation.NSObject[] ReadObjectsForClasses (ObjCRuntime.Class[] classArray, Foundation.NSDictionary options);
</pre>

### Type Changed: AppKit.NSPasteboardItem

Added interfaces:

<pre style='color: green'>
	INSPasteboardReading
	INSPasteboardWriting
</pre>

Added methods:

<pre style='color: green'>
	public virtual Foundation.NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual Foundation.NSObject InitWithPasteboardPropertyList (Foundation.NSObject propertyList, string type);
</pre>

### Type Changed: AppKit.NSPathControlItem


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>AppKit.NSObjectController</span></span>

 <span style='color:green'>Foundation.NSObject</span>

Added method:

<pre style='color: green'>
	public virtual void EncodeTo (Foundation.NSCoder coder);
</pre>

### Type Changed: AppKit.NSResponder

Added method:

<pre style='color: green'>
	public virtual void PressureChange (NSEvent pressureChangeEvent);
</pre>

### Type Changed: AppKit.NSSegmentedControl

Added property:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
</pre>

### Type Changed: AppKit.NSSegmentSwitchTracking

Added value:

<pre style='color: green'>
	MomentaryAccelerator = 3,
</pre>

### Type Changed: AppKit.NSTableViewSource

Removed interface:

<pre style='color: red'>
	INSTableViewSource
</pre>

### Type Changed: AppKit.NSTextView

Added interface:

<pre style='color: green'>
	INSTextInputClient
</pre>

Added properties:

<pre style='color: green'>
	public virtual Foundation.NSAttributedString AttributedString { get; }
	public virtual bool HasMarkedText { get; }
	public virtual Foundation.NSRange MarkedRange { get; }
	public virtual Foundation.NSString[] ValidAttributesForMarkedText { get; }
	public virtual NSWindowLevel WindowLevel { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool DrawsVertically (uint charIndex);
	public virtual Foundation.NSAttributedString GetAttributedSubstring (Foundation.NSRange proposedRange, out Foundation.NSRange actualRange);
	public virtual nfloat GetBaselineDelta (uint charIndex);
	public virtual uint GetCharacterIndex (CoreGraphics.CGPoint point);
	public virtual CoreGraphics.CGRect GetFirstRect (Foundation.NSRange characterRange, out Foundation.NSRange actualRange);
	public virtual nfloat GetFractionOfDistanceThroughGlyph (CoreGraphics.CGPoint point);
	public virtual void InsertText (Foundation.NSObject text, Foundation.NSRange replacementRange);
	public virtual void SetMarkedText (Foundation.NSObject text, Foundation.NSRange selectedRange, Foundation.NSRange replacementRange);
	public virtual void UnmarkText ();
</pre>

### Type Changed: AppKit.NSTextViewCompletion

Removed methods:

<pre style='color: red'>
	public virtual System.IAsyncResult BeginInvoke (NSTextView textView, string[] words, Foundation.NSRange charRange, nint index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (System.IAsyncResult result);
	public virtual string[] Invoke (NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added methods:

<pre style='color: green'>
	public virtual System.IAsyncResult BeginInvoke (NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (ref nint index, System.IAsyncResult result);
	public virtual string[] Invoke (NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSTextViewDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSTextViewDelegate_Extensions

Removed method:

<pre style='color: red'>
	public static string[] GetCompletions (INSTextViewDelegate This, NSTextView textView, string[] words, Foundation.NSRange charRange, nint index);
</pre>

Added method:

<pre style='color: green'>
	public static string[] GetCompletions (INSTextViewDelegate This, NSTextView textView, string[] words, Foundation.NSRange charRange, ref nint index);
</pre>

### Type Changed: AppKit.NSTreeController

Removed property:

<pre style='color: red'>
	public virtual Foundation.NSObject[] SelectedObjects { get; }
</pre>

### Type Changed: AppKit.NSView

Modified methods:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes items, NSEvent evnt, INSDraggingSource source)
```

Added methods:

<pre style='color: green'>
	public virtual void BeginDocument ();
	public virtual void BeginPage (CoreGraphics.CGRect rect, CoreGraphics.CGPoint placement);
	public virtual void EndDocument ();
	public virtual void EndPage ();
</pre>

### Type Changed: AppKit.NSWorkspace

Added method:

<pre style='color: green'>
	public virtual bool OpenUrls (Foundation.NSUrl[] urls, string bundleIdentifier, NSWorkspaceLaunchOptions options, Foundation.NSAppleEventDescriptor descriptor);
</pre>

### Removed Type  <span style='color: red'>AppKit.INSTableViewSource</span>

### Removed Type  <span style='color: red'>AppKit.NSTableViewSource_Extensions</span>

### New Type AppKit.INSTextInputClient

<pre style='color: green'>
public interface INSTextInputClient : ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type AppKit.NSStepperCell

<pre style='color: green'>
public class NSStepperCell : AppKit.NSActionCell, Foundation.INSCoding, Foundation.INSCopying, INSUserInterfaceItemIdentification, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSStepperCell ();
	public NSStepperCell (Foundation.NSCoder coder);
	protected NSStepperCell (Foundation.NSObjectFlag t);
	protected NSStepperCell (IntPtr handle);
	// properties
	public virtual bool Autorepeat { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual double Increment { get; set; }
	public virtual double MaxValue { get; set; }
	public virtual double MinValue { get; set; }
	public virtual bool ValueWraps { get; set; }
}
</pre>

### New Type AppKit.NSTextInputClient

<pre style='color: green'>
public class NSTextInputClient : Foundation.NSObject, INSTextInputClient, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable&lt;Foundation.NSObject&gt; {
	// constructors
	public NSTextInputClient ();
	protected NSTextInputClient (Foundation.NSObjectFlag t);
	protected NSTextInputClient (IntPtr handle);
	// properties
	public virtual Foundation.NSAttributedString AttributedString { get; }
	public virtual bool HasMarkedText { get; }
	public virtual Foundation.NSRange MarkedRange { get; }
	public virtual Foundation.NSRange SelectedRange { get; }
	public virtual Foundation.NSString[] ValidAttributesForMarkedText { get; }
	public virtual NSWindowLevel WindowLevel { get; }
	// methods
	public virtual bool DrawsVertically (uint charIndex);
	public virtual Foundation.NSAttributedString GetAttributedSubstring (Foundation.NSRange proposedRange, out Foundation.NSRange actualRange);
	public virtual nfloat GetBaselineDelta (uint charIndex);
	public virtual uint GetCharacterIndex (CoreGraphics.CGPoint point);
	public virtual CoreGraphics.CGRect GetFirstRect (Foundation.NSRange characterRange, out Foundation.NSRange actualRange);
	public virtual nfloat GetFractionOfDistanceThroughGlyph (CoreGraphics.CGPoint point);
	public virtual void InsertText (Foundation.NSObject text, Foundation.NSRange replacementRange);
	public virtual void SetMarkedText (Foundation.NSObject text, Foundation.NSRange selectedRange, Foundation.NSRange replacementRange);
	public virtual void UnmarkText ();
}
</pre>

### New Type AppKit.NSTextInputClient_Extensions

<pre style='color: green'>
public static class NSTextInputClient_Extensions {
	// methods
	public static bool DrawsVertically (INSTextInputClient This, uint charIndex);
	public static Foundation.NSAttributedString GetAttributedString (INSTextInputClient This);
	public static Foundation.NSAttributedString GetAttributedSubstring (INSTextInputClient This, Foundation.NSRange proposedRange, out Foundation.NSRange actualRange);
	public static nfloat GetBaselineDelta (INSTextInputClient This, uint charIndex);
	public static uint GetCharacterIndex (INSTextInputClient This, CoreGraphics.CGPoint point);
	public static CoreGraphics.CGRect GetFirstRect (INSTextInputClient This, Foundation.NSRange characterRange, out Foundation.NSRange actualRange);
	public static nfloat GetFractionOfDistanceThroughGlyph (INSTextInputClient This, CoreGraphics.CGPoint point);
	public static bool GetHasMarkedText (INSTextInputClient This);
	public static Foundation.NSRange GetMarkedRange (INSTextInputClient This);
	public static Foundation.NSRange GetSelectedRange (INSTextInputClient This);
	public static Foundation.NSString[] GetValidAttributesForMarkedText (INSTextInputClient This);
	public static NSWindowLevel GetWindowLevel (INSTextInputClient This);
	public static void InsertText (INSTextInputClient This, Foundation.NSObject text, Foundation.NSRange replacementRange);
	public static void SetMarkedText (INSTextInputClient This, Foundation.NSObject text, Foundation.NSRange selectedRange, Foundation.NSRange replacementRange);
	public static void UnmarkText (INSTextInputClient This);
}
</pre>

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: AudioToolbox.SystemSound

Added constructor:

<pre style='color: green'>
	public SystemSound (uint soundId);
</pre>

## Namespace AudioUnit

### Type Changed: AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete (]
	public void SetAudioFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: AudioUnit.ExtAudioFile

Modified properties:

```
public AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

## Namespace AVFoundation

### Type Changed: AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

### Type Changed: AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: AVFoundation.AVUrlAsset

Added constructor:

<pre style='color: green'>
	public AVUrlAsset (Foundation.NSUrl url);
</pre>

Added method:

<pre style='color: green'>
	public static AVUrlAsset Create (Foundation.NSUrl url);
</pre>

### New Type AVFoundation.AVErrorKeys

<pre style='color: green'>
public static class AVErrorKeys {
	// properties
	public static Foundation.NSString Device { get; }
	public static Foundation.NSString DiscontinuityFlags { get; }
	public static Foundation.NSString ErrorDomain { get; }
	public static Foundation.NSString FileSize { get; }
	public static Foundation.NSString FileType { get; }
	public static Foundation.NSString MediaSubType { get; }
	public static Foundation.NSString MediaType { get; }
	public static Foundation.NSString PersistentTrackID { get; }
	public static Foundation.NSString Pid { get; }
	public static Foundation.NSString PresentationTimeStamp { get; }
	public static Foundation.NSString RecordingSuccessfullyFinished { get; }
	public static Foundation.NSString Time { get; }
}
</pre>

## Namespace CoreAnimation

### Type Changed: CoreAnimation.CAAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

Added method:

<pre style='color: green'>
	public virtual void RunAction (string eventKey, Foundation.NSObject obj, Foundation.NSDictionary arguments);
</pre>

### Type Changed: CoreAnimation.CAAnimationGroup

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CABasicAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CAPropertyAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

## Namespace CoreData

### Type Changed: CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out Foundation.NSError error);
</pre>

## Namespace CoreFoundation

### Type Changed: CoreFoundation.CFNetwork

Added property:

<pre style='color: green'>
	public static Foundation.NSString ErrorDomain { get; }
</pre>

### Type Changed: CoreFoundation.DispatchSource

Added method:

<pre style='color: green'>
	public void Suspend ();
</pre>

### Type Changed: CoreFoundation.DispatchSource.Timer

Added constructor:

<pre style='color: green'>
	public DispatchSource (bool strict, DispatchQueue queue);
</pre>

### Type Changed: CoreFoundation.DispatchTime

Modified constructors:

```
public DispatchTime (DispatchTime when, long delta deltaNanoseconds)
```

Added constructor:

<pre style='color: green'>
	public DispatchTime (DispatchTime when, System.TimeSpan delta);
</pre>

### New Type CoreFoundation.CFMessagePort

<pre style='color: green'>
public class CFMessagePort : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public CFMessagePortContext Context { get; }
	public virtual IntPtr Handle { get; }
	public System.Action InvalidationCallback { get; set; }
	public bool IsRemote { get; }
	public bool IsValid { get; }
	public string Name { get; set; }
	// methods
	protected override void ~CFMessagePort ();
	protected void Check ();
	public static CFMessagePort CreateLocalPort (CFAllocator allocator, string name, CFMessagePort.CFMessagePortCallBack callback, CFMessagePortContext context);
	public static CFMessagePort CreateRemotePort (CFAllocator allocator, string name);
	public CFRunLoopSource CreateRunLoopSource ();
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public void Invalidate ();
	public CFMessagePortSendRequestStatus SendRequest (int msgid, Foundation.NSData data, double sendTimeout, double rcvTimeout, Foundation.NSString replyMode, out Foundation.NSData returnData);
	public void SetDispatchQueue (DispatchQueue queue);

	// inner types
	public sealed delegate CFMessagePortCallBack : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CFMessagePort (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (int type, Foundation.NSData data, System.AsyncCallback callback, object object);
		public virtual Foundation.NSData EndInvoke (System.IAsyncResult result);
		public virtual Foundation.NSData Invoke (int type, Foundation.NSData data);
	}
}
</pre>

### New Type CoreFoundation.CFMessagePortContext

<pre style='color: green'>
public class CFMessagePortContext {
	// constructors
	public CFMessagePortContext ();
	// properties
	public System.Func&lt;Foundation.NSString&gt; CopyDescription { get; set; }
	public System.Action Release { get; set; }
	public System.Func&lt;ObjCRuntime.INativeObject&gt; Retain { get; set; }
}
</pre>

### New Type CoreFoundation.CFMessagePortSendRequestStatus

<pre style='color: green'>
[Serializable]
public enum CFMessagePortSendRequestStatus {
	BecameInvalidError = -5,
	IsInvalid = -3,
	ReceiveTimeout = -2,
	SendTimeout = -1,
	Success = 0,
	TransportError = -4,
}
</pre>

### New Type CoreFoundation.CFNetworkErrors

<pre style='color: green'>
[Serializable]
public enum CFNetworkErrors {
	BackgroundSessionInUseByAnotherProcess = -996,
	BackgroundSessionWasDisconnected = -997,
	BadServerResponse = -1011,
	BadURL = -1000,
	CallIsActive = -1019,
	Cancelled = -999,
	CannotCloseFile = -3002,
	CannotConnectToHost = -1004,
	CannotCreateFile = -3000,
	CannotDecodeContentData = -1016,
	CannotDecodeRawData = -1015,
	CannotFindHost = -1003,
	CannotLoadFromNetwork = -2000,
	CannotMoveFile = -3005,
	CannotOpenFile = -3001,
	CannotParseCookieFile = -4000,
	CannotParseResponse = -1017,
	CannotRemoveFile = -3004,
	CannotWriteToFile = -3003,
	ClientCertificateRejected = -1205,
	ClientCertificateRequired = -1206,
	DataLengthExceedsMaximum = -1103,
	DataNotAllowed = -1020,
	DNSLookupFailed = -1006,
	DownloadDecodingFailedMidStream = -3006,
	DownloadDecodingFailedToComplete = -3007,
	FileDoesNotExist = -1100,
	FileIsDirectory = -1101,
	FtpUnexpectedStatusCode = 200,
	HostNotFound = 1,
	HostUnknown = 2,
	HttpAuthenticationTypeUnsupported = 300,
	HttpBadCredentials = 301,
	HttpBadProxyCredentials = 307,
	HttpBadURL = 305,
	HttpConnectionLost = 302,
	HttpParseFailure = 303,
	HttpProxyConnectionFailure = 306,
	HttpRedirectionLoopDetected = 304,
	HttpsProxyConnectionFailure = 310,
	HttpsProxyFailureUnexpectedResponseToConnectMethod = 311,
	HTTPTooManyRedirects = -1007,
	InternationalRoamingOff = -1018,
	NetServiceBadArgument = -72004,
	NetServiceCancel = -72005,
	NetServiceCollision = -72001,
	NetServiceDnsServiceFailure = -73000,
	NetServiceInProgress = -72003,
	NetServiceInvalid = -72006,
	NetServiceNotFound = -72002,
	NetServiceTimeout = -72007,
	NetServiceUnknown = -72000,
	NetworkConnectionLost = -1005,
	NoPermissionsToReadFile = -1102,
	NotConnectedToInternet = -1009,
	PacFileAuth = 309,
	PacFileError = 308,
	RedirectToNonExistentLocation = -1010,
	RequestBodyStreamExhausted = -1021,
	ResourceUnavailable = -1008,
	SecureConnectionFailed = -1200,
	ServerCertificateHasBadDate = -1201,
	ServerCertificateHasUnknownRoot = -1203,
	ServerCertificateNotYetValid = -1204,
	ServerCertificateUntrusted = -1202,
	Socks4IdConflict = 112,
	Socks4IdentdFailed = 111,
	Socks4RequestFailed = 110,
	Socks4UnknownStatusCode = 113,
	Socks5BadCredentials = 122,
	Socks5BadResponseAddr = 121,
	Socks5BadState = 120,
	Socks5NoAcceptableMethod = 124,
	Socks5UnsupportedNegotiationMethod = 123,
	SocksUnknownClientVersion = 100,
	SocksUnsupportedServerVersion = 101,
	TimedOut = -1001,
	Unknown = -998,
	UnsupportedURL = -1002,
	UserAuthenticationRequired = -1013,
	UserCancelledAuthentication = -1012,
	ZeroByteResource = -1014,
}
</pre>

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGColorSpace

Obsoleted fields:

```
[Obsolete (]
	public static CGColorSpace Null;
```

## Namespace CoreMedia

### Type Changed: CoreMedia.CMBlockBuffer

Added property:

<pre style='color: green'>
	public bool IsEmpty { get; }
</pre>

Added methods:

<pre style='color: green'>
	public CMBlockBufferError AccessDataBytes (uint offset, uint length, IntPtr temporaryBlock, ref IntPtr returnedPointer);
	public CMBlockBufferError AppendBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AppendMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags);
	public CMBlockBufferError AssureBlockMemory ();
	public static CMBlockBuffer CreateContiguous (CMBlockBuffer sourceBuffer, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer CreateFromMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public CMBlockBufferError FillDataBytes (byte fillByte, uint offsetIntoDestination, uint dataLength);
	public CMBlockBufferError GetDataPointer (uint offset, out uint lengthAtOffset, out uint totalLength, ref IntPtr dataPointer);
	public bool IsRangeContiguous (uint offset, uint length);
	public CMBlockBufferError ReplaceDataBytes (IntPtr sourceBytes, uint offsetIntoDestination, uint dataLength);
</pre>

### Type Changed: CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: CoreMedia.CMVideoFormatDescription

Added methods:

<pre style='color: green'>
	public static CMVideoFormatDescription FromH264ParameterSets (System.Collections.Generic.List&lt;System.Byte[]&gt; parameterSets, int nalUnitHeaderLength, out CMFormatDescriptionError error);
	public byte[] GetH264ParameterSet (uint index, out uint parameterSetCount, out int nalUnitHeaderLength, out CMFormatDescriptionError error);
</pre>

### New Type CoreMedia.CMCustomBlockAllocator

<pre style='color: green'>
public class CMCustomBlockAllocator : System.IDisposable {
	// constructors
	public CMCustomBlockAllocator ();
	// methods
	protected override void ~CMCustomBlockAllocator ();
	public virtual IntPtr Allocate (uint sizeInBytes);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual void Free (IntPtr doomedMemoryBlock, uint sizeInBytes);
}
</pre>

## Namespace CoreServices

### Type Changed: CoreServices.FSEventStreamEventFlags

Added values:

<pre style='color: green'>
	ItemIsHardlink = 1048576,
	ItemIsLastHardlink = 2097152,
	OwnEvent = 524288,
</pre>

### New Type CoreServices.LaunchServices

<pre style='color: green'>
public static class LaunchServices {
	// methods
	public static bool CanUrlAcceptUrl (Foundation.NSUrl itemUrl, Foundation.NSUrl targetUrl, LSRoles roles, LSAcceptanceFlags acceptanceFlags);
	public static bool CanUrlAcceptUrl (Foundation.NSUrl itemUrl, Foundation.NSUrl targetUrl, LSRoles roles, LSAcceptanceFlags acceptanceFlags, out LSResult result);
	public static string[] GetAllHandlersForUrlScheme (string urlScheme);
	public static string[] GetAllRoleHandlersForContentType (string contentType, LSRoles roles);
	public static Foundation.NSUrl[] GetApplicationUrlsForBundleIdentifier (string bundleIdentifier);
	public static Foundation.NSUrl[] GetApplicationUrlsForUrl (Foundation.NSUrl url, LSRoles roles);
	public static Foundation.NSUrl GetDefaultApplicationUrlForContentType (string contentType, LSRoles roles);
	public static Foundation.NSUrl GetDefaultApplicationUrlForUrl (Foundation.NSUrl url, LSRoles roles);
	public static string GetDefaultHandlerForUrlScheme (string urlScheme);
	public static string GetDefaultRoleHandlerForContentType (string contentType, LSRoles roles);
	public static LSResult Open (Foundation.NSUrl url, out Foundation.NSUrl launchedUrl);
	public static LSResult Open (Foundation.NSUrl url);
	public static LSResult Register (Foundation.NSUrl url, bool update);
	public static LSResult SetDefaultHandlerForUrlScheme (string urlScheme, string handlerBundleId);
	public static LSResult SetDefaultRoleHandlerForContentType (string contentType, string handlerBundleId, LSRoles roles);
}
</pre>

### New Type CoreServices.LSAcceptanceFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum LSAcceptanceFlags {
	AllowLoginUI = 2,
	Default = 1,
}
</pre>

### New Type CoreServices.LSResult

<pre style='color: green'>
[Serializable]
public enum LSResult {
	AppDoesNotClaimType = -10820,
	AppDoesNotSupportSchemeWarning = -10821,
	AppInTrash = -10660,
	ApplicationNotFound = -10814,
	AttributeNotFound = -10662,
	AttributeNotSettable = -10663,
	CannotSetInfo = -10823,
	Data = -10817,
	DataTooOld = -10816,
	DataUnavailable = -10813,
	ExecutableIncorrectFormat = -10661,
	IncompatibleApplicationVersion = -10664,
	IncompatibleSystemVersion = -10825,
	LaunchInProgress = -10818,
	MultipleSessionsNotSupported = -10829,
	NoClassicEnvironment = -10828,
	NoExecutable = -10827,
	NoLaunchPermission = -10826,
	NoRegistrationInfo = -10824,
	NoRosettaEnvironment = -10665,
	NotAnApplication = -10811,
	NotInitialized = -10812,
	NotRegistered = -10819,
	ServerCommunication = -10822,
	Success = 0,
	Unknown = -10810,
	UnknownType = -10815,
}
</pre>

### New Type CoreServices.LSRoles

<pre style='color: green'>
[Serializable]
[Flags]
public enum LSRoles {
	All = 4294967295,
	Editor = 4,
	None = 1,
	Shell = 8,
	Viewer = 2,
}
</pre>

## Namespace Foundation

### Type Changed: Foundation.NSAppleEventDescriptor

Added constructor:

<pre style='color: green'>
	public NSAppleEventDescriptor (NSAppleEventDescriptorType type);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual NSObject InitListDescriptor ();
	[Obsolete (]
	public virtual NSObject InitRecordDescriptor ();
```

### Type Changed: Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public byte[] DecodeBytes ();
	public virtual IntPtr DecodeBytes (out uint length);
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public bool TryDecodeBool (string key, out bool result);
	public bool TryDecodeBytes (string key, out byte[] result);
	public bool TryDecodeDouble (string key, out double result);
	public bool TryDecodeFloat (string key, out float result);
	public bool TryDecodeInt (string key, out int result);
	public bool TryDecodeLong (string key, out long result);
	public bool TryDecodeNInt (string key, out nint result);
	public bool TryDecodeObject (string key, out NSObject result);
</pre>

### Type Changed: Foundation.NSData

Removed method:

<pre style='color: red'>
	public virtual void GetBytes (IntPtr buffer, uint length);
</pre>

Added method:

<pre style='color: green'>
	public virtual void GetBytes (IntPtr buffer, uint length);
</pre>

### Type Changed: Foundation.NSDate

Added methods:

<pre style='color: green'>
	public virtual NSComparisonResult Compare (NSDate other);
	public virtual NSDate EarlierDate (NSDate anotherDate);
	public virtual bool IsEqualToDate (NSDate other);
	public virtual NSDate LaterDate (NSDate anotherDate);
</pre>

### Type Changed: Foundation.NSDateFormatter

Added property:

<pre style='color: green'>
	public virtual bool DoesRelativeDateFormatting { get; set; }
</pre>

### Type Changed: Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

### Type Changed: Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, AppKit.NSStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: Foundation.NSItemProvider

Added properties:

<pre style='color: green'>
	public virtual CoreGraphics.CGRect ContainerFrame { get; }
	public virtual CoreGraphics.CGSize PreferredPresentationSize { get; }
	public virtual CoreGraphics.CGRect SourceFrame { get; }
</pre>

### Type Changed: Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: Foundation.NSMutableData

Removed method:

<pre style='color: red'>
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
</pre>

Added method:

<pre style='color: green'>
	public virtual void ReplaceBytes (NSRange range, IntPtr buffer, uint length);
</pre>

### Type Changed: Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
</pre>

### Type Changed: Foundation.NSOperation

Added property:

<pre style='color: green'>
	public virtual System.Action CompletionBlock { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void WaitUntilFinishedNS ();
```

Added method:

<pre style='color: green'>
	public virtual void WaitUntilFinished ();
</pre>

### Type Changed: Foundation.NSProcessInfo

Added properties:

<pre style='color: green'>
	public virtual NSProcessInfoThermalState ThermalState { get; }
	public static NSString ThermalStateDidChangeNotification { get; }
</pre>

### Type Changed: Foundation.NSPurgeableData

Added interface:

<pre style='color: green'>
	INSDiscardableContent
</pre>

Added property:

<pre style='color: green'>
	public virtual bool IsContentDiscarded { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
</pre>

### Type Changed: Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (nint seconds);
</pre>

### Type Changed: Foundation.NSUndoManager

Added method:

<pre style='color: green'>
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: Foundation.NSUrlError

Added values:

<pre style='color: green'>
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>Foundation.NSUrlSessionDataTask</span>

### Type Changed: Foundation.NSValueTransformer

Modified constructors:

```
public protected NSValueTransformer ()
```

Added properties:

<pre style='color: green'>
	public static bool AllowsReverseTransformation { get; }
	public static NSString BooleanTransformerName { get; }
	public static NSString IsNilTransformerName { get; }
	public static NSString NSIsNotNilTransformerName { get; }
	public static NSString NSKeyedUnarchiveFromDataTransformerName { get; }
	public static ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSValueTransformer GetValueTransformer (string name);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
</pre>

### New Type Foundation.INSDiscardableContent

<pre style='color: green'>
public interface INSDiscardableContent : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool IsContentDiscarded { get; }
	// methods
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
}
</pre>

### New Type Foundation.NSAppleEventDescriptorType

<pre style='color: green'>
[Serializable]
public enum NSAppleEventDescriptorType {
	List = 1,
	Record = 0,
}
</pre>

### New Type Foundation.NSCondition

<pre style='color: green'>
public class NSCondition : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSCondition ();
	protected NSCondition (NSObjectFlag t);
	protected NSCondition (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Broadcast ();
	public virtual void Lock ();
	public virtual void Signal ();
	public virtual void Unlock ();
	public virtual void Wait ();
	public virtual bool WaitUntilDate (NSDate limit);
}
</pre>

### New Type Foundation.NSConditionLock

<pre style='color: green'>
public class NSConditionLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSConditionLock ();
	protected NSConditionLock (NSObjectFlag t);
	protected NSConditionLock (IntPtr handle);
	public NSConditionLock (nint condition);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual nint Condition { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool LockWhenCondition (nint condition, NSDate limit);
	public virtual void LockWhenCondition (nint condition);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (nint condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (nint condition);
}
</pre>

### New Type Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : Foundation.NSRegularExpression, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSDataDetector ();
	public NSDataDetector (NSCoder coder);
	protected NSDataDetector (NSObjectFlag t);
	protected NSDataDetector (IntPtr handle);
	// properties
	public virtual NSTextCheckingTypes CheckingTypes { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	public static NSDataDetector Create (NSTextCheckingTypes checkingTypes, out NSError error);
	public virtual void EncodeTo (NSCoder encoder);
}
</pre>

### New Type Foundation.NSExtension

<pre style='color: green'>
public static class NSExtension {
	// properties
	public static NSString JavaScriptFinalizeArgumentKey { get; }
	public static NSString JavaScriptPreprocessingResultsKey { get; }
}
</pre>

### New Type Foundation.NSLock

<pre style='color: green'>
public class NSLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSLock ();
	protected NSLock (NSObjectFlag t);
	protected NSLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type Foundation.NSMatchEnumerator

<pre style='color: green'>
public sealed delegate NSMatchEnumerator : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSMatchEnumerator (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual void Invoke (NSTextCheckingResult result, NSMatchingFlags flags, ref bool stop);
}
</pre>

### New Type Foundation.NSMatchingFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingFlags {
	Completed = 2,
	HitEnd = 4,
	InternalError = 16,
	Progress = 1,
	RequiredEnd = 8,
}
</pre>

### New Type Foundation.NSMatchingOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSMatchingOptions {
	Anchored = 4,
	ReportCompletion = 2,
	ReportProgress = 1,
	WithoutAnchoringBounds = 16,
	WithTransparentBounds = 8,
}
</pre>

### New Type Foundation.NSPredicateSupport_NSArray

<pre style='color: green'>
public static class NSPredicateSupport_NSArray {
	// methods
	public static NSArray FilterUsingPredicate (NSArray This, NSArray array);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSMutableArray

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableArray {
	// methods
	public static void FilterUsingPredicate (NSMutableArray This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSMutableSet

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableSet {
	// methods
	public static void FilterUsingPredicate (NSMutableSet This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSPredicateSupport_NSSet

<pre style='color: green'>
public static class NSPredicateSupport_NSSet {
	// methods
	public static NSSet FilterUsingPredicate (NSSet This, NSPredicate predicate);
}
</pre>

### New Type Foundation.NSProcessInfoThermalState

<pre style='color: green'>
[Serializable]
public enum NSProcessInfoThermalState {
	Critical = 3,
	Fair = 1,
	Nominal = 0,
	Serious = 2,
}
</pre>

### New Type Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : Foundation.NSObject, INSLocking, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSRecursiveLock ();
	protected NSRecursiveLock (NSObjectFlag t);
	protected NSRecursiveLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool TryLock ();
	public virtual void Unlock ();
}
</pre>

### New Type Foundation.NSRegularExpression

<pre style='color: green'>
public class NSRegularExpression : Foundation.NSObject, INSCoding, INSCopying, ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol, System.IEquatable&lt;NSObject&gt; {
	// constructors
	public NSRegularExpression ();
	public NSRegularExpression (NSCoder coder);
	protected NSRegularExpression (NSObjectFlag t);
	protected NSRegularExpression (IntPtr handle);
	public NSRegularExpression (NSString pattern, NSRegularExpressionOptions options, out NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint NumberOfCaptureGroups { get; }
	public virtual NSRegularExpressionOptions Options { get; }
	public virtual NSString Pattern { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EncodeTo (NSCoder encoder);
	public virtual void EnumerateMatches (NSString str, NSMatchingOptions options, NSRange range, NSMatchEnumerator enumerator);
	public virtual NSTextCheckingResult FindFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public static NSString GetEscapedPattern (NSString str);
	public static NSString GetEscapedTemplate (NSString str);
	public virtual NSString[] GetMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual uint GetNumberOfMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual NSRange GetRangeOfFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public virtual NSString GetReplacementString (NSTextCheckingResult result, NSString str, nint offset, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
}
</pre>

### New Type Foundation.NSRegularExpressionOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSRegularExpressionOptions {
	AllowCommentsAndWhitespace = 2,
	AnchorsMatchLines = 16,
	CaseInsensitive = 1,
	DotMatchesLineSeparators = 8,
	IgnoreMetacharacters = 4,
	UseUnicodeWordBoundaries = 64,
}
</pre>

### New Type Foundation.ProtocolMemberAttribute

<pre style='color: green'>
public sealed class ProtocolMemberAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public ProtocolMemberAttribute ();
	// properties
	public ObjCRuntime.ArgumentSemantic ArgumentSemantic { get; set; }
	public string GetterSelector { get; set; }
	public bool IsProperty { get; set; }
	public bool IsRequired { get; set; }
	public bool IsStatic { get; set; }
	public bool IsVariadic { get; set; }
	public string Name { get; set; }
	public bool[] ParameterByRef { get; set; }
	public System.Type[] ParameterType { get; set; }
	public System.Type PropertyType { get; set; }
	public System.Type ReturnType { get; set; }
	public string Selector { get; set; }
	public string SetterSelector { get; set; }
}
</pre>

## Namespace GameKit

### Type Changed: GameKit.GKAchievementViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>AppKit.NSViewController</span></span>

 <span style='color:green'>GameKit.GKGameCenterViewController</span>

### Type Changed: GameKit.GKLeaderboardViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>AppKit.NSViewController</span></span>

 <span style='color:green'>GameKit.GKGameCenterViewController</span>

### Type Changed: GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete (]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

## Namespace GLKit

### Type Changed: GLKit.GLKBaseEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: GLKit.GLKReflectionMapEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

### Type Changed: GLKit.GLKSkyboxEffect

Added interface:

<pre style='color: green'>
	IGLKNamedEffect
</pre>

## Namespace ImageKit

### Type Changed: ImageKit.IKSlideshow

Added property:

<pre style='color: green'>
	public static Foundation.NSString PhotosBundleIdentifier { get; }
</pre>

## Namespace MapKit

### New Type MapKit.MKOverlayView

<pre style='color: green'>
public class MKOverlayView {
	// constructors
	public MKOverlayView ();
	// methods
	public static nfloat MKRoadWidthAtZoomScale (nfloat zoomScale);
}
</pre>

## Namespace MediaAccessibility

### New Type MediaAccessibility.MAAudibleMedia

<pre style='color: green'>
public static class MAAudibleMedia {
	// properties
	public static Foundation.NSString SettingsChangedNotification { get; }
	// methods
	public static string[] GetPreferredCharacteristics ();

	// inner types
	public static class Notifications {
		// methods
		public static Foundation.NSObject ObserveSettingsChanged (System.EventHandler&lt;Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MediaAccessibility.MAMediaCharacteristic

<pre style='color: green'>
public static class MAMediaCharacteristic {
	// properties
	public static Foundation.NSString DescribesMusicAndSoundForAccessibility { get; }
	public static Foundation.NSString DescribesVideoForAccessibility { get; }
	public static Foundation.NSString TranscribesSpokenDialogForAccessibility { get; }
}
</pre>

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_SIGNATURE = 1073741824,
</pre>

### Type Changed: ObjCRuntime.BlockLiteral

Added method:

<pre style='color: green'>
	public static bool IsManagedBlock (IntPtr block);
</pre>

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "2.0.2" "2.3.0";
```

Added fields:

<pre style='color: green'>
	public static const string SdkVersion = "10.10";
	public static const string SearchKitLibrary = "/System/Library/Frameworks/CoreServices.framework/Frameworks/SearchKit.framework/SearchKit";
</pre>

### Type Changed: ObjCRuntime.iOSAttribute

Added constructor:

<pre style='color: green'>
	public iOSAttribute (byte major, byte minor, byte subminor);
</pre>

### Type Changed: ObjCRuntime.MacAttribute

Added constructors:

<pre style='color: green'>
	public MacAttribute (byte major, byte minor);
	public MacAttribute (byte major, byte minor, byte subminor);
	public MacAttribute (byte major, byte minor, byte subminor, bool onlyOn64);
</pre>

### Type Changed: ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	Mac_10_10_3 = 2825757768286208,
</pre>

## Namespace PdfKit

### Type Changed: PdfKit.PdfAreaOfInterest

Added value:

<pre style='color: green'>
	ImageArea = 256,
</pre>

### Type Changed: PdfKit.PdfView

Added interface:

<pre style='color: green'>
	AppKit.INSMenuDelegate
</pre>

Added methods:

<pre style='color: green'>
	public virtual CoreGraphics.CGRect ConfinementRectForMenu (AppKit.NSMenu menu, AppKit.NSScreen screen);
	public virtual PdfAreaOfInterest GetAreaOfInterest (CoreGraphics.CGPoint point);
	public virtual bool HasKeyEquivalentForEvent (AppKit.NSMenu menu, AppKit.NSEvent theEvent, Foundation.NSObject target, ObjCRuntime.Selector action);
	public virtual void MenuDidClose (AppKit.NSMenu menu);
	public virtual nint MenuItemCount (AppKit.NSMenu menu);
	public virtual void MenuWillHighlightItem (AppKit.NSMenu menu, AppKit.NSMenuItem item);
	public virtual void MenuWillOpen (AppKit.NSMenu menu);
	public virtual void NeedsUpdate (AppKit.NSMenu menu);
	public virtual bool UpdateItem (AppKit.NSMenu menu, AppKit.NSMenuItem item, nint atIndex, bool shouldCancel);
</pre>

## Namespace QTKit

### Type Changed: QTKit.QTCaptureConnection

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

Removed method:

<pre style='color: red'>
	public virtual void SetAttribute (Foundation.NSObject attribute, string key);
</pre>

Modified methods:

```
public virtual Foundation.NSObject GetAttribute (string attributeKey)
```

Added methods:

<pre style='color: green'>
	public virtual Foundation.NSObject GetAttribute (Foundation.NSString attributeKey);
	public virtual void SetAttribute (Foundation.NSObject attribute, Foundation.NSString key);
</pre>

### Type Changed: QTKit.QTCaptureDevice

Added properties:

<pre style='color: green'>
	public static Foundation.NSString AVCTransportControlsAttribute { get; }
	public static Foundation.NSString AVCTransportControlsPlaybackModeKey { get; }
	public static Foundation.NSString AVCTransportControlsSpeedKey { get; }
	public static Foundation.NSString SuspendedAttribute { get; }
</pre>

### Type Changed: QTKit.QTCompressionOptions

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

Added method:

<pre style='color: green'>
	public string[] GetCompressionOptionsIdentifiers (QTMediaType forMediaType);
</pre>

### Type Changed: QTKit.QTFormatDescription

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

### Type Changed: QTKit.QTMedia

Added method:

<pre style='color: green'>
	public IntPtr Constructors (IntPtr quicktimeMedia, out Foundation.NSError error);
</pre>

### Type Changed: QTKit.QTMovie

Obsoleted constructors:

```
[Obsolete (]
	public QTMovie (QTTimeRange range, out Foundation.NSError error);
```

Added methods:

<pre style='color: green'>
	public QTMovie MovieWithTimeRange (QTTimeRange range, out Foundation.NSError error);
	public QTTrack[] TracksOfMediaType (QTMediaType mediaType);
</pre>

### New Type QTKit.QTErrorKey

<pre style='color: green'>
public static class QTErrorKey {
	// properties
	public static Foundation.NSString CaptureInput { get; }
	public static Foundation.NSString CaptureOutput { get; }
	public static Foundation.NSString Device { get; }
	public static Foundation.NSString Domain { get; }
	public static Foundation.NSString ExcludingDevice { get; }
	public static Foundation.NSString FileSize { get; }
	public static Foundation.NSString RecordingSuccesfullyFinished { get; }
	public static Foundation.NSString Time { get; }
}
</pre>

## Namespace SceneKit

### Type Changed: SceneKit.SCNParticleSystem

Added properties:

<pre style='color: green'>
	public SCNPropertyControllers PropertyControllers { get; set; }
	public virtual Foundation.NSDictionary WeakPropertyControllers { get; set; }
</pre>

Modified methods:

```
public virtual void HandleEvent (SCNParticleEvent evnt, Foundation.NSString[] properties particleProperties, SCNParticleEventHandler handler)
```

### New Type SceneKit.SCNParticleProperty

<pre style='color: green'>
public static class SCNParticleProperty {
	// properties
	public static Foundation.NSString Angle { get; }
	public static Foundation.NSString AngularVelocity { get; }
	public static Foundation.NSString Bounce { get; }
	public static Foundation.NSString Charge { get; }
	public static Foundation.NSString Color { get; }
	public static Foundation.NSString Frame { get; }
	public static Foundation.NSString FrameRate { get; }
	public static Foundation.NSString Friction { get; }
	public static Foundation.NSString Life { get; }
	public static Foundation.NSString Opacity { get; }
	public static Foundation.NSString Position { get; }
	public static Foundation.NSString RotationAxis { get; }
	public static Foundation.NSString Size { get; }
	public static Foundation.NSString Velocity { get; }
}
</pre>

### New Type SceneKit.SCNPhysicsCollisionCategory

<pre style='color: green'>
[Serializable]
public enum SCNPhysicsCollisionCategory {
	All = 18446744073709551615,
	Default = 1,
	None = 0,
	Static = 2,
}
</pre>

### New Type SceneKit.SCNPropertyControllers

<pre style='color: green'>
public class SCNPropertyControllers {
	// constructors
	public SCNPropertyControllers ();
	// properties
	public SCNParticlePropertyController Angle { get; set; }
	public SCNParticlePropertyController AngularVelocity { get; set; }
	public SCNParticlePropertyController Bounce { get; set; }
	public SCNParticlePropertyController Charge { get; set; }
	public SCNParticlePropertyController Color { get; set; }
	public SCNParticlePropertyController Frame { get; set; }
	public SCNParticlePropertyController FrameRate { get; set; }
	public SCNParticlePropertyController Friction { get; set; }
	public SCNParticlePropertyController Life { get; set; }
	public SCNParticlePropertyController Opacity { get; set; }
	public SCNParticlePropertyController Position { get; set; }
	public SCNParticlePropertyController RotationAxis { get; set; }
	public SCNParticlePropertyController Size { get; set; }
	public SCNParticlePropertyController Velocity { get; set; }
}
</pre>

## Namespace SpriteKit

### Type Changed: SpriteKit.SKFieldNode

Obsoleted methods:

```
[Obsolete (]
	public static SKFieldNode CraeteVortexField ();
```

Added method:

<pre style='color: green'>
	public static SKFieldNode CreateVortexField ();
</pre>

## Namespace WebKit

### Type Changed: WebKit.DomEvent

Added constructor:

<pre style='color: green'>
	public DomEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
```

### Type Changed: WebKit.DomKeyboardEvent

Added constructors:

<pre style='color: green'>
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	[Obsolete (]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: WebKit.DomMouseEvent

Added constructor:

<pre style='color: green'>
	public DomMouseEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, IDomEventTarget relatedTarget);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, IDomEventTarget relatedTarget);
```

### Type Changed: WebKit.DomOverflowEvent

Added constructor:

<pre style='color: green'>
	public DomOverflowEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
```

### Type Changed: WebKit.DomProcessingInstruction


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>WebKit.DomNode</span></span>

 <span style='color:green'>WebKit.DomCharacterData</span>

### Type Changed: WebKit.DomUIEvent

Added constructor:

<pre style='color: green'>
	public DomUIEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
```

### Type Changed: WebKit.DomWheelEvent

Added constructor:

<pre style='color: green'>
	public DomWheelEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete (]
	public virtual void InitEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

## New Namespace SearchKit

### New Type SearchKit.SKDocument

<pre style='color: green'>
public class SKDocument : System.IDisposable, ObjCRuntime.INativeObject {
	// constructors
	public SKDocument (string name, SKDocument parent, string scheme);
	public SKDocument (Foundation.NSUrl url);
	// properties
	public virtual IntPtr Handle { get; }
	public string Name { get; }
	public string Scheme { get; }
	public Foundation.NSUrl Url { get; }
	// methods
	protected override void ~SKDocument ();
	protected virtual void Dispose (bool disposing);
	public SKDocument GetParent ();
}
</pre>

### New Type SearchKit.SKIndex

<pre style='color: green'>
public class SKIndex : System.IDisposable, ObjCRuntime.INativeObject {
	// properties
	public SKTextAnalysis AnalysisProperties { get; }
	public nint DocumentCount { get; }
	public virtual IntPtr Handle { get; }

	[Obsolete]
	public nint MaximumBytesBeforeFlush { get; set; }
	public nint MaximumDocumentID { get; }
	public nint MaximumTermID { get; }
	// methods
	protected override void ~SKIndex ();
	public bool AddDocument (SKDocument document, string mimeHint, bool canReplace);
	public bool AddDocumentWithText (SKDocument doc, string text, bool canReplace);
	public void Close ();
	public bool Compact ();
	public static SKIndex CreateWithMutableData (Foundation.NSMutableData data, string indexName, SKIndexType type, SKTextAnalysis analysisProperties);
	public static SKIndex CreateWithUrl (Foundation.NSUrl url, string indexName, SKIndexType type, SKTextAnalysis analysisProperties);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public bool Flush ();
	public static SKIndex FromData (Foundation.NSData data, string indexName);
	public static SKIndex FromMutableData (Foundation.NSMutableData data, string indexName);
	public static SKIndex FromUrl (Foundation.NSUrl url, string indexName, bool writeAccess);
	public SKDocument GetDocument (IntPtr documentId);
	public static void LoadDefaultExtractorPlugIns ();
	public bool MoveDocument (SKDocument document, SKDocument newParent);
	public bool RemoveDocument (SKDocument doc);
	public bool RenameDocument (SKDocument document, string newName);
	public SKSearch Search (string query, SKSearchOptions options);
	public void SetDocumentProperties (SKDocument document, Foundation.NSDictionary dict);
}
</pre>

### New Type SearchKit.SKIndexType

<pre style='color: green'>
[Serializable]
public enum SKIndexType {
	Inverted = 1,
	InvertedVector = 3,
	Unknown = 0,
	Vector = 2,
}
</pre>

### New Type SearchKit.SKSearch

<pre style='color: green'>
public class SKSearch : System.IDisposable, ObjCRuntime.INativeObject {
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~SKSearch ();
	public void Cancel ();
	protected virtual void Dispose (bool disposing);
	public bool FindMatches (nint maxCount, ref IntPtr[] ids, double waitTime, out nint foundCount);
	public bool FindMatches (nint maxCount, ref IntPtr[] ids, ref float[] scores, double waitTime, out nint foundCount);
}
</pre>

### New Type SearchKit.SKSearchOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum SKSearchOptions {
	Default = 0,
	FindSimilar = 4,
	NoRelevanceScores = 1,
	SpaceMeansOr = 2,
}
</pre>

### New Type SearchKit.SKSummary

<pre style='color: green'>
public class SKSummary : System.IDisposable, ObjCRuntime.INativeObject {
	// properties
	public virtual IntPtr Handle { get; }
	public nint ParagraphCount { get; }
	public nint SentenceCount { get; }
	// methods
	protected override void ~SKSummary ();
	public static SKSummary Create (string text);
	public static SKSummary Create (Foundation.NSString nsString);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public string GetParagraph (nint idx);
	public string GetParagraphSummary (int maxParagraphs);
	public nint GetParagraphSummaryInfo (nint maxNumParagraphsInSummary, nint[] rankOrderOfParagraphs, nint[] paragraphIndexOfParagraphs);
	public string GetSentence (nint idx);
	public string GetSentenceSummary (int maxSentences);
	public nint GetSentenceSummaryInfo (int maxNumSentencesInSummary, nint[] rankOrderOfSentences, nint[] sentenceIndexOfSentences, nint[] paragraphIndexOfSentences);
}
</pre>

### New Type SearchKit.SKTextAnalysis

<pre style='color: green'>
public class SKTextAnalysis : Foundation.DictionaryContainer {
	// constructors
	public SKTextAnalysis ();
	public SKTextAnalysis (Foundation.NSDictionary dictionary);
	// properties
	public string EndTermChars { get; set; }
	public Foundation.NSNumber MaximumTerms { get; set; }
	public int? MinTermLength { get; set; }
	public bool? ProximityIndexing { get; set; }
	public string StartTermChars { get; set; }
	public Foundation.NSSet StopWords { get; set; }
	public Foundation.NSDictionary Substitutions { get; set; }
	public string TermChars { get; set; }
}
</pre>

### New Type SearchKit.SKTextAnalysisKeys

<pre style='color: green'>
public static class SKTextAnalysisKeys {
	// properties
	public static Foundation.NSString EndTermCharsKey { get; }
	public static Foundation.NSString MaximumTermsKey { get; }
	public static Foundation.NSString MinTermLengthKey { get; }
	public static Foundation.NSString ProximityIndexingKey { get; }
	public static Foundation.NSString StartTermCharsKey { get; }
	public static Foundation.NSString StopWordsKey { get; }
	public static Foundation.NSString SubstitutionsKey { get; }
	public static Foundation.NSString TermCharsKey { get; }
}
</pre>
