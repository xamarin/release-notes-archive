---
id: D135DD7B-3D1C-4EA5-9133-463D3A2EF7B2
title: "From 2.0.0 to 2.3.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Modified fields:

```
public const string Version = "2.0.2" "2.3.0";
```

Added fields:

<pre style='color: green'>
	public static const string SdkVersion = "10.10";
	public static const string SearchKitLibrary = "/System/Library/Frameworks/CoreServices.framework/Frameworks/SearchKit.framework/SearchKit";
</pre>

## Namespace MonoMac.AppKit

### Type Changed: MonoMac.AppKit.NSAnimation

Added constructor:

<pre style='color: green'>
	public NSAnimation (double duration, NSAnimationCurve animationCurve);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual IntPtr Constant (double duration, NSAnimationCurve animationCurve);
```

### Type Changed: MonoMac.AppKit.NSApplication

Removed interface:

<pre style='color: red'>
	INSWindowRestoration
</pre>

Obsoleted methods:

```
[Obsolete ("This method does nothing"]
	public static void RestoreWindow (string identifier, MonoMac.Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
```

Added methods:

<pre style='color: green'>
	public virtual void CompleteStateRestoration ();
	public virtual void ExtendStateRestoration ();
	public virtual bool RestoreWindowWithIdentifier (string identifier, MonoMac.Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
</pre>

### Type Changed: MonoMac.AppKit.NSButton

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual int MaxAcceleratorLevel { get; set; }
	public virtual NSSegmentSwitchTracking TrackingMode { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual double GetValueForSelectedSegment ();
</pre>

### Type Changed: MonoMac.AppKit.NSButtonType

Added values:

<pre style='color: green'>
	Accelerator = 8,
	MultiLevelAccelerator = 9,
</pre>

### Type Changed: MonoMac.AppKit.NSColor

Obsoleted properties:

```
[Obsolete ("Use UnderPageBackgroundColor instead"]
	public static NSColor UnderPageBackground { get; }
```

### Type Changed: MonoMac.AppKit.NSComboBox

Added property:

<pre style='color: green'>
	public MonoMac.Foundation.NSObject Item { get; }
</pre>

Obsoleted methods:

```
[Obsolete ("Use GetItemObject instead"]
	public virtual NSComboBox GetItem (int index);
```

Added method:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSObject GetItemObject (int index);
</pre>

### Type Changed: MonoMac.AppKit.NSControlTextCompletion

Removed methods:

<pre style='color: red'>
	public virtual System.IAsyncResult BeginInvoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (System.IAsyncResult result);
	public virtual string[] Invoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added methods:

<pre style='color: green'>
	public virtual System.IAsyncResult BeginInvoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (ref int index, System.IAsyncResult result);
	public virtual string[] Invoke (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSControlTextEditingDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSControlTextEditingDelegate_Extensions

Removed method:

<pre style='color: red'>
	public static string[] GetCompletions (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public static string[] GetCompletions (INSControlTextEditingDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSEvent

Added properties:

<pre style='color: green'>
	public virtual NSEventMask AssociatedEventsMask { get; }
	public virtual int Stage { get; }
	public virtual float StageTransition { get; }
</pre>

### Type Changed: MonoMac.AppKit.NSEventMask

Added value:

<pre style='color: green'>
	Pressure = 17179869184,
</pre>

### Type Changed: MonoMac.AppKit.NSEventType

Added value:

<pre style='color: green'>
	Pressure = 34,
</pre>

### Type Changed: MonoMac.AppKit.NSGraphics

Added methods:

<pre style='color: green'>
	public static void DisableScreenUpdates ();
	public static void DrawWindowBackground (System.Drawing.RectangleF aRect);
	public static void EnableScreenUpdates ();
</pre>

### Type Changed: MonoMac.AppKit.NSMatrixDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSMatrixDelegate_Extensions

Removed method:

<pre style='color: red'>
	public static string[] GetCompletions (INSMatrixDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public static string[] GetCompletions (INSMatrixDelegate This, NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSOutlineViewDelegate

Obsoleted methods:

```
[Obsolete ("Use GetView instead"]
	public virtual NSView ViewForTableColumn (NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
```

### Type Changed: MonoMac.AppKit.NSOutlineViewDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use GetView instead"]
	public static NSView ViewForTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
```

### Type Changed: MonoMac.AppKit.NSPasteboard

Removed methods:

<pre style='color: red'>
	public virtual bool CanReadObjectForClasses (MonoMac.Foundation.NSObject[] classArray, MonoMac.Foundation.NSDictionary options);
	public virtual MonoMac.Foundation.NSObject[] ReadObjectsForClasses (INSPasteboardReading[] classArray, MonoMac.Foundation.NSDictionary options);
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool CanReadObjectForClasses (MonoMac.ObjCRuntime.Class[] classArray, MonoMac.Foundation.NSDictionary options);
	public virtual MonoMac.Foundation.NSObject[] ReadObjectsForClasses (MonoMac.ObjCRuntime.Class[] classArray, MonoMac.Foundation.NSDictionary options);
</pre>

### Type Changed: MonoMac.AppKit.NSPasteboardItem

Added interfaces:

<pre style='color: green'>
	INSPasteboardReading
	INSPasteboardWriting
</pre>

Added methods:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSObject GetPasteboardPropertyListForType (string type);
	public static string[] GetReadableTypesForPasteboard (NSPasteboard pasteboard);
	public static NSPasteboardReadingOptions GetReadingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual string[] GetWritableTypesForPasteboard (NSPasteboard pasteboard);
	public virtual NSPasteboardWritingOptions GetWritingOptionsForType (string type, NSPasteboard pasteboard);
	public virtual MonoMac.Foundation.NSObject InitWithPasteboardPropertyList (MonoMac.Foundation.NSObject propertyList, string type);
</pre>

### Type Changed: MonoMac.AppKit.NSPathControlItem


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.AppKit.NSObjectController</span></span>

 <span style='color:green'>MonoMac.Foundation.NSObject</span>

### Type Changed: MonoMac.AppKit.NSSegmentedControl

Added property:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSSegmentSwitchTracking

Added value:

<pre style='color: green'>
	MomentaryAccelerator = 3,
</pre>

### Type Changed: MonoMac.AppKit.NSTableViewSource

Removed interface:

<pre style='color: red'>
	INSTableViewSource
</pre>

### Type Changed: MonoMac.AppKit.NSTextView

Added interface:

<pre style='color: green'>
	INSTextInputClient
</pre>

Added properties:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSAttributedString AttributedString { get; }
	public virtual bool HasMarkedText { get; }
	public virtual MonoMac.Foundation.NSRange MarkedRange { get; }
	public virtual MonoMac.Foundation.NSRange SelectedRange { get; }
	public virtual MonoMac.Foundation.NSString[] ValidAttributesForMarkedText { get; }
	public virtual NSWindowLevel WindowLevel { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool DrawsVertically (uint charIndex);
	public virtual MonoMac.Foundation.NSAttributedString GetAttributedSubstring (MonoMac.Foundation.NSRange proposedRange, out MonoMac.Foundation.NSRange actualRange);
	public virtual float GetBaselineDelta (uint charIndex);
	public virtual uint GetCharacterIndex (System.Drawing.PointF point);
	public virtual System.Drawing.RectangleF GetFirstRect (MonoMac.Foundation.NSRange characterRange, out MonoMac.Foundation.NSRange actualRange);
	public virtual float GetFractionOfDistanceThroughGlyph (System.Drawing.PointF point);
	public virtual void InsertText (MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange replacementRange);
	public virtual void SetMarkedText (MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange selectedRange, MonoMac.Foundation.NSRange replacementRange);
	public virtual void UnmarkText ();
</pre>

### Type Changed: MonoMac.AppKit.NSTextViewCompletion

Removed methods:

<pre style='color: red'>
	public virtual System.IAsyncResult BeginInvoke (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (System.IAsyncResult result);
	public virtual string[] Invoke (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added methods:

<pre style='color: green'>
	public virtual System.IAsyncResult BeginInvoke (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index, System.AsyncCallback callback, object object);
	public virtual string[] EndInvoke (ref int index, System.IAsyncResult result);
	public virtual string[] Invoke (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSTextViewDelegate

Removed method:

<pre style='color: red'>
	public virtual string[] GetCompletions (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public virtual string[] GetCompletions (NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSTextViewDelegate_Extensions

Removed method:

<pre style='color: red'>
	public static string[] GetCompletions (INSTextViewDelegate This, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, int index);
</pre>

Added method:

<pre style='color: green'>
	public static string[] GetCompletions (INSTextViewDelegate This, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
</pre>

### Type Changed: MonoMac.AppKit.NSView

Modified methods:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes items, NSEvent evnt, NSDraggingSource source)
```

Added methods:

<pre style='color: green'>
	public virtual void BeginDocument ();
	public virtual void BeginPage (System.Drawing.RectangleF rect, System.Drawing.PointF placement);
	public virtual void EndDocument ();
	public virtual void EndPage ();
</pre>

### Type Changed: MonoMac.AppKit.NSWorkspace

Added method:

<pre style='color: green'>
	public virtual bool OpenUrls (MonoMac.Foundation.NSUrl[] urls, string bundleIdentifier, NSWorkspaceLaunchOptions options, MonoMac.Foundation.NSAppleEventDescriptor descriptor);
</pre>

### Removed Type  <span style='color: red'>MonoMac.AppKit.INSTableViewSource</span>

### Removed Type  <span style='color: red'>MonoMac.AppKit.NSTableViewSource_Extensions</span>

### New Type MonoMac.AppKit.INSTextInputClient

<pre style='color: green'>
public interface INSTextInputClient : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.NSStepperCell

<pre style='color: green'>
public class NSStepperCell : MonoMac.AppKit.NSActionCell, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSStepperCell ();
	public NSStepperCell (MonoMac.Foundation.NSCoder coder);
	public NSStepperCell (MonoMac.Foundation.NSObjectFlag t);
	public NSStepperCell (IntPtr handle);
	// properties
	public virtual bool Autorepeat { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual double Increment { get; set; }
	public virtual double MaxValue { get; set; }
	public virtual double MinValue { get; set; }
	public virtual bool ValueWraps { get; set; }
}
</pre>

### New Type MonoMac.AppKit.NSTextInputClient

<pre style='color: green'>
public class NSTextInputClient : MonoMac.Foundation.NSObject, INSTextInputClient, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public NSTextInputClient ();
	public NSTextInputClient (MonoMac.Foundation.NSCoder coder);
	public NSTextInputClient (MonoMac.Foundation.NSObjectFlag t);
	public NSTextInputClient (IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSAttributedString AttributedString { get; }
	public virtual bool HasMarkedText { get; }
	public virtual MonoMac.Foundation.NSRange MarkedRange { get; }
	public virtual MonoMac.Foundation.NSRange SelectedRange { get; }
	public virtual MonoMac.Foundation.NSString[] ValidAttributesForMarkedText { get; }
	public virtual NSWindowLevel WindowLevel { get; }
	// methods
	public virtual bool DrawsVertically (uint charIndex);
	public virtual MonoMac.Foundation.NSAttributedString GetAttributedSubstring (MonoMac.Foundation.NSRange proposedRange, out MonoMac.Foundation.NSRange actualRange);
	public virtual float GetBaselineDelta (uint charIndex);
	public virtual uint GetCharacterIndex (System.Drawing.PointF point);
	public virtual System.Drawing.RectangleF GetFirstRect (MonoMac.Foundation.NSRange characterRange, out MonoMac.Foundation.NSRange actualRange);
	public virtual float GetFractionOfDistanceThroughGlyph (System.Drawing.PointF point);
	public virtual void InsertText (MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange replacementRange);
	public virtual void SetMarkedText (MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange selectedRange, MonoMac.Foundation.NSRange replacementRange);
	public virtual void UnmarkText ();
}
</pre>

### New Type MonoMac.AppKit.NSTextInputClient_Extensions

<pre style='color: green'>
public static class NSTextInputClient_Extensions {
	// methods
	public static bool DrawsVertically (INSTextInputClient This, uint charIndex);
	public static MonoMac.Foundation.NSAttributedString GetAttributedString (INSTextInputClient This);
	public static MonoMac.Foundation.NSAttributedString GetAttributedSubstring (INSTextInputClient This, MonoMac.Foundation.NSRange proposedRange, out MonoMac.Foundation.NSRange actualRange);
	public static float GetBaselineDelta (INSTextInputClient This, uint charIndex);
	public static uint GetCharacterIndex (INSTextInputClient This, System.Drawing.PointF point);
	public static System.Drawing.RectangleF GetFirstRect (INSTextInputClient This, MonoMac.Foundation.NSRange characterRange, out MonoMac.Foundation.NSRange actualRange);
	public static float GetFractionOfDistanceThroughGlyph (INSTextInputClient This, System.Drawing.PointF point);
	public static bool GetHasMarkedText (INSTextInputClient This);
	public static MonoMac.Foundation.NSRange GetMarkedRange (INSTextInputClient This);
	public static MonoMac.Foundation.NSRange GetSelectedRange (INSTextInputClient This);
	public static MonoMac.Foundation.NSString[] GetValidAttributesForMarkedText (INSTextInputClient This);
	public static NSWindowLevel GetWindowLevel (INSTextInputClient This);
	public static void InsertText (INSTextInputClient This, MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange replacementRange);
	public static void SetMarkedText (INSTextInputClient This, MonoMac.Foundation.NSObject text, MonoMac.Foundation.NSRange selectedRange, MonoMac.Foundation.NSRange replacementRange);
	public static void UnmarkText (INSTextInputClient This);
}
</pre>

## Namespace MonoMac.AudioToolbox

### Type Changed: MonoMac.AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: MonoMac.AudioToolbox.SystemSound

Added constructor:

<pre style='color: green'>
	public SystemSound (uint soundId);
</pre>

## Namespace MonoMac.AudioUnit

### Type Changed: MonoMac.AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete ("Use SetFormat instead as it has the ability of returning a status code"]
	public void SetAudioFormat (MonoMac.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (MonoMac.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: MonoMac.AudioUnit.ExtAudioFile

Modified properties:

```
public MonoMac.AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVAsset

Added property:

<pre style='color: green'>
	public virtual int UnusedTrackId { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: MonoMac.AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVUrlAsset

Added constructor:

<pre style='color: green'>
	public AVUrlAsset (MonoMac.Foundation.NSUrl url);
</pre>

Added method:

<pre style='color: green'>
	public static AVUrlAsset Create (MonoMac.Foundation.NSUrl url);
</pre>

### New Type MonoMac.AVFoundation.AVErrorKeys

<pre style='color: green'>
public static class AVErrorKeys {
	// properties
	public static MonoMac.Foundation.NSString Device { get; }
	public static MonoMac.Foundation.NSString DiscontinuityFlags { get; }
	public static MonoMac.Foundation.NSString ErrorDomain { get; }
	public static MonoMac.Foundation.NSString FileSize { get; }
	public static MonoMac.Foundation.NSString FileType { get; }
	public static MonoMac.Foundation.NSString MediaSubType { get; }
	public static MonoMac.Foundation.NSString MediaType { get; }
	public static MonoMac.Foundation.NSString PersistentTrackID { get; }
	public static MonoMac.Foundation.NSString Pid { get; }
	public static MonoMac.Foundation.NSString PresentationTimeStamp { get; }
	public static MonoMac.Foundation.NSString RecordingSuccessfullyFinished { get; }
	public static MonoMac.Foundation.NSString Time { get; }
}
</pre>

## Namespace MonoMac.CoreAnimation

### Type Changed: MonoMac.CoreAnimation.CAAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

Added method:

<pre style='color: green'>
	public virtual void RunAction (string eventKey, MonoMac.Foundation.NSObject obj, MonoMac.Foundation.NSDictionary arguments);
</pre>

### Type Changed: MonoMac.CoreAnimation.CAAnimationGroup

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoMac.CoreAnimation.CABasicAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoMac.CoreAnimation.CAPropertyAnimation

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### Type Changed: MonoMac.CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

## Namespace MonoMac.CoreData

### Type Changed: MonoMac.CoreData.NSManagedObjectContext

Added method:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out MonoMac.Foundation.NSError error);
</pre>

## Namespace MonoMac.CoreFoundation

### Type Changed: MonoMac.CoreFoundation.CFNetwork

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString ErrorDomain { get; }
</pre>

### Type Changed: MonoMac.CoreFoundation.DispatchSource

Added method:

<pre style='color: green'>
	public void Suspend ();
</pre>

### Type Changed: MonoMac.CoreFoundation.DispatchSource.Timer

Added constructor:

<pre style='color: green'>
	public DispatchSource (bool strict, DispatchQueue queue);
</pre>

### Type Changed: MonoMac.CoreFoundation.DispatchTime

Modified constructors:

```
public DispatchTime (DispatchTime when, long delta deltaNanoseconds)
```

Added constructor:

<pre style='color: green'>
	public DispatchTime (DispatchTime when, System.TimeSpan delta);
</pre>

### New Type MonoMac.CoreFoundation.CFMessagePort

<pre style='color: green'>
public class CFMessagePort : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
	public CFMessagePortSendRequestStatus SendRequest (int msgid, MonoMac.Foundation.NSData data, double sendTimeout, double rcvTimeout, MonoMac.Foundation.NSString replyMode, out MonoMac.Foundation.NSData returnData);
	public void SetDispatchQueue (DispatchQueue queue);

	// inner types
	public sealed delegate CFMessagePortCallBack : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CFMessagePort (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (int type, MonoMac.Foundation.NSData data, System.AsyncCallback callback, object object);
		public virtual MonoMac.Foundation.NSData EndInvoke (System.IAsyncResult result);
		public virtual MonoMac.Foundation.NSData Invoke (int type, MonoMac.Foundation.NSData data);
	}
}
</pre>

### New Type MonoMac.CoreFoundation.CFMessagePortContext

<pre style='color: green'>
public class CFMessagePortContext {
	// constructors
	public CFMessagePortContext ();
	// properties
	public System.Func&lt;MonoMac.Foundation.NSString&gt; CopyDescription { get; set; }
	public System.Action Release { get; set; }
	public System.Func&lt;MonoMac.ObjCRuntime.INativeObject&gt; Retain { get; set; }
}
</pre>

### New Type MonoMac.CoreFoundation.CFMessagePortSendRequestStatus

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

### New Type MonoMac.CoreFoundation.CFNetworkErrors

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

## Namespace MonoMac.CoreGraphics

### Type Changed: MonoMac.CoreGraphics.CGColorSpace

Obsoleted fields:

```
[Obsolete ("Use a real `null` value instead of this managed wrapper over a null native instance"]
	public static CGColorSpace Null;
```

## Namespace MonoMac.CoreMedia

### Type Changed: MonoMac.CoreMedia.CMBlockBuffer

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

### Type Changed: MonoMac.CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: MonoMac.CoreMedia.CMVideoFormatDescription

Added methods:

<pre style='color: green'>
	public static CMVideoFormatDescription FromH264ParameterSets (System.Collections.Generic.List&lt;System.Byte[]&gt; parameterSets, int nalUnitHeaderLength, out CMFormatDescriptionError error);
	public byte[] GetH264ParameterSet (uint index, out uint parameterSetCount, out int nalUnitHeaderLength, out CMFormatDescriptionError error);
</pre>

### New Type MonoMac.CoreMedia.CMCustomBlockAllocator

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

## Namespace MonoMac.CoreServices

### Type Changed: MonoMac.CoreServices.FSEventStreamEventFlags

Added values:

<pre style='color: green'>
	ItemIsHardlink = 1048576,
	ItemIsLastHardlink = 2097152,
	OwnEvent = 524288,
</pre>

### New Type MonoMac.CoreServices.LaunchServices

<pre style='color: green'>
public static class LaunchServices {
	// methods
	public static bool CanUrlAcceptUrl (MonoMac.Foundation.NSUrl itemUrl, MonoMac.Foundation.NSUrl targetUrl, LSRoles roles, LSAcceptanceFlags acceptanceFlags);
	public static bool CanUrlAcceptUrl (MonoMac.Foundation.NSUrl itemUrl, MonoMac.Foundation.NSUrl targetUrl, LSRoles roles, LSAcceptanceFlags acceptanceFlags, out LSResult result);
	public static string[] GetAllHandlersForUrlScheme (string urlScheme);
	public static string[] GetAllRoleHandlersForContentType (string contentType, LSRoles roles);
	public static MonoMac.Foundation.NSUrl[] GetApplicationUrlsForBundleIdentifier (string bundleIdentifier);
	public static MonoMac.Foundation.NSUrl[] GetApplicationUrlsForUrl (MonoMac.Foundation.NSUrl url, LSRoles roles);
	public static MonoMac.Foundation.NSUrl GetDefaultApplicationUrlForContentType (string contentType, LSRoles roles);
	public static MonoMac.Foundation.NSUrl GetDefaultApplicationUrlForUrl (MonoMac.Foundation.NSUrl url, LSRoles roles);
	public static string GetDefaultHandlerForUrlScheme (string urlScheme);
	public static string GetDefaultRoleHandlerForContentType (string contentType, LSRoles roles);
	public static LSResult Open (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSUrl launchedUrl);
	public static LSResult Open (MonoMac.Foundation.NSUrl url);
	public static LSResult Register (MonoMac.Foundation.NSUrl url, bool update);
	public static LSResult SetDefaultHandlerForUrlScheme (string urlScheme, string handlerBundleId);
	public static LSResult SetDefaultRoleHandlerForContentType (string contentType, string handlerBundleId, LSRoles roles);
}
</pre>

### New Type MonoMac.CoreServices.LSAcceptanceFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum LSAcceptanceFlags {
	AllowLoginUI = 2,
	Default = 1,
}
</pre>

### New Type MonoMac.CoreServices.LSResult

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

### New Type MonoMac.CoreServices.LSRoles

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

## Namespace MonoMac.Foundation

### Type Changed: MonoMac.Foundation.NSAppleEventDescriptor

Added constructor:

<pre style='color: green'>
	public NSAppleEventDescriptor (NSAppleEventDescriptorType type);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual NSObject InitListDescriptor ();
	[Obsolete ("Use the constructor instead"]
	public virtual NSObject InitRecordDescriptor ();
```

### Type Changed: MonoMac.Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: MonoMac.Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public virtual IntPtr DecodeBytes (out uint length);
	public byte[] DecodeBytes ();
	public bool TryDecodeBool (string key, out bool result);
	public bool TryDecodeBytes (string key, out byte[] result);
	public bool TryDecodeDouble (string key, out double result);
	public bool TryDecodeFloat (string key, out float result);
	public bool TryDecodeInt (string key, out int result);
	public bool TryDecodeLong (string key, out long result);
	public bool TryDecodeObject (string key, out NSObject result);
</pre>

### Type Changed: MonoMac.Foundation.NSDate

Added methods:

<pre style='color: green'>
	public virtual NSComparisonResult Compare (NSDate other);
	public virtual NSDate EarlierDate (NSDate anotherDate);
	public virtual bool IsEqualToDate (NSDate other);
	public virtual NSDate LaterDate (NSDate anotherDate);
</pre>

### Type Changed: MonoMac.Foundation.NSDateFormatter

Added property:

<pre style='color: green'>
	public virtual bool DoesRelativeDateFormatting { get; set; }
</pre>

### Type Changed: MonoMac.Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, MonoMac.AppKit.NSStringAttributes attrs);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary attrs);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: MonoMac.Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSObject

Added method:

<pre style='color: green'>
	public virtual void PrepareForInterfaceBuilder ();
</pre>

### Type Changed: MonoMac.Foundation.NSOperation

Added property:

<pre style='color: green'>
	public virtual System.Action CompletionBlock { get; set; }
</pre>

Obsoleted methods:

```
[Obsolete ("Use WaitUntilFinished method"]
	public virtual void WaitUntilFinishedNS ();
```

Added method:

<pre style='color: green'>
	public virtual void WaitUntilFinished ();
</pre>

### Type Changed: MonoMac.Foundation.NSProcessInfo

Added properties:

<pre style='color: green'>
	public virtual NSProcessInfoThermalState ThermalState { get; }
	public static NSString ThermalStateDidChangeNotification { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSPurgeableData

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

### Type Changed: MonoMac.Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: MonoMac.Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (int seconds);
</pre>

### Type Changed: MonoMac.Foundation.NSUndoManager

Added method:

<pre style='color: green'>
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: MonoMac.Foundation.NSUrlError

Added values:

<pre style='color: green'>
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionUploadTask


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.Foundation.NSUrlSessionTask</span></span>

 <span style='color:green'>MonoMac.Foundation.NSUrlSessionDataTask</span>

### Type Changed: MonoMac.Foundation.NSValueTransformer

Added properties:

<pre style='color: green'>
	public static bool AllowsReverseTransformation { get; }
	public static NSString BooleanTransformerName { get; }
	public static NSString IsNilTransformerName { get; }
	public static NSString NSIsNotNilTransformerName { get; }
	public static NSString NSKeyedUnarchiveFromDataTransformerName { get; }
	public static MonoMac.ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSValueTransformer GetValueTransformer (string name);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
</pre>

### New Type MonoMac.Foundation.INSDiscardableContent

<pre style='color: green'>
public interface INSDiscardableContent : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual bool IsContentDiscarded { get; }
	// methods
	public virtual bool BeginContentAccess ();
	public virtual void DiscardContentIfPossible ();
	public virtual void EndContentAccess ();
}
</pre>

### New Type MonoMac.Foundation.NSAppleEventDescriptorType

<pre style='color: green'>
[Serializable]
public enum NSAppleEventDescriptorType {
	List = 1,
	Record = 0,
}
</pre>

### New Type MonoMac.Foundation.NSCondition

<pre style='color: green'>
public class NSCondition : MonoMac.Foundation.NSObject, INSLocking, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSCondition ();
	public NSCondition (NSCoder coder);
	public NSCondition (NSObjectFlag t);
	public NSCondition (IntPtr handle);
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

### New Type MonoMac.Foundation.NSConditionLock

<pre style='color: green'>
public class NSConditionLock : MonoMac.Foundation.NSObject, INSLocking, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSConditionLock ();
	public NSConditionLock (NSCoder coder);
	public NSConditionLock (NSObjectFlag t);
	public NSConditionLock (IntPtr handle);
	public NSConditionLock (int condition);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual int Condition { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual bool LockWhenCondition (int condition, NSDate limit);
	public virtual void LockWhenCondition (int condition);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (int condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (int condition);
}
</pre>

### New Type MonoMac.Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : MonoMac.Foundation.NSRegularExpression, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSDataDetector ();
	public NSDataDetector (NSCoder coder);
	public NSDataDetector (NSObjectFlag t);
	public NSDataDetector (IntPtr handle);
	// properties
	public virtual NSTextCheckingTypes CheckingTypes { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	public static NSDataDetector Create (NSTextCheckingTypes checkingTypes, out NSError error);
}
</pre>

### New Type MonoMac.Foundation.NSDiscardableContent_Extensions

<pre style='color: green'>
public static class NSDiscardableContent_Extensions {
}
</pre>

### New Type MonoMac.Foundation.NSLock

<pre style='color: green'>
public class NSLock : MonoMac.Foundation.NSObject, INSLocking, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSLock ();
	public NSLock (NSCoder coder);
	public NSLock (NSObjectFlag t);
	public NSLock (IntPtr handle);
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

### New Type MonoMac.Foundation.NSMatchEnumerator

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

### New Type MonoMac.Foundation.NSMatchingFlags

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

### New Type MonoMac.Foundation.NSMatchingOptions

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

### New Type MonoMac.Foundation.NSPredicateSupport_NSArray

<pre style='color: green'>
public static class NSPredicateSupport_NSArray {
	// methods
	public static NSArray FilterUsingPredicate (NSArray This, NSArray array);
}
</pre>

### New Type MonoMac.Foundation.NSPredicateSupport_NSMutableArray

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableArray {
	// methods
	public static void FilterUsingPredicate (NSMutableArray This, NSPredicate predicate);
}
</pre>

### New Type MonoMac.Foundation.NSPredicateSupport_NSMutableSet

<pre style='color: green'>
public static class NSPredicateSupport_NSMutableSet {
	// methods
	public static void FilterUsingPredicate (NSMutableSet This, NSPredicate predicate);
}
</pre>

### New Type MonoMac.Foundation.NSPredicateSupport_NSSet

<pre style='color: green'>
public static class NSPredicateSupport_NSSet {
	// methods
	public static NSSet FilterUsingPredicate (NSSet This, NSPredicate predicate);
}
</pre>

### New Type MonoMac.Foundation.NSProcessInfoThermalState

<pre style='color: green'>
[Serializable]
public enum NSProcessInfoThermalState {
	Critical = 3,
	Fair = 1,
	Nominal = 0,
	Serious = 2,
}
</pre>

### New Type MonoMac.Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : MonoMac.Foundation.NSObject, INSLocking, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSRecursiveLock ();
	public NSRecursiveLock (NSCoder coder);
	public NSRecursiveLock (NSObjectFlag t);
	public NSRecursiveLock (IntPtr handle);
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

### New Type MonoMac.Foundation.NSRegularExpression

<pre style='color: green'>
public class NSRegularExpression : MonoMac.Foundation.NSObject, INSCoding, INSCopying, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, INSObjectProtocol {
	// constructors
	public NSRegularExpression ();
	public NSRegularExpression (NSCoder coder);
	public NSRegularExpression (NSObjectFlag t);
	public NSRegularExpression (IntPtr handle);
	public NSRegularExpression (NSString pattern, NSRegularExpressionOptions options, out NSError error);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual uint NumberOfCaptureGroups { get; }
	public virtual NSRegularExpressionOptions Options { get; }
	public virtual NSString Pattern { get; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void EnumerateMatches (NSString str, NSMatchingOptions options, NSRange range, NSMatchEnumerator enumerator);
	public virtual NSTextCheckingResult FindFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public static NSString GetEscapedPattern (NSString str);
	public static NSString GetEscapedTemplate (NSString str);
	public virtual NSString[] GetMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual uint GetNumberOfMatches (NSString str, NSMatchingOptions options, NSRange range);
	public virtual NSRange GetRangeOfFirstMatch (string str, NSMatchingOptions options, NSRange range);
	public virtual NSString GetReplacementString (NSTextCheckingResult result, NSString str, int offset, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
}
</pre>

### New Type MonoMac.Foundation.NSRegularExpressionOptions

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

### New Type MonoMac.Foundation.ProtocolMemberAttribute

<pre style='color: green'>
public sealed class ProtocolMemberAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public ProtocolMemberAttribute ();
	// properties
	public MonoMac.ObjCRuntime.ArgumentSemantic ArgumentSemantic { get; set; }
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

## Namespace MonoMac.GameKit

### Type Changed: MonoMac.GameKit.GKAchievementViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.AppKit.NSViewController</span></span>

 <span style='color:green'>MonoMac.GameKit.GKGameCenterViewController</span>

### Type Changed: MonoMac.GameKit.GKLeaderboardViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.AppKit.NSViewController</span></span>

 <span style='color:green'>MonoMac.GameKit.GKGameCenterViewController</span>

### Type Changed: MonoMac.GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete ("Use SetMute(bool,string) method"]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

## Namespace MonoMac.ImageKit

### Type Changed: MonoMac.ImageKit.IKSlideshow

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString PhotosBundleIdentifier { get; }
</pre>

## Namespace MonoMac.MediaAccessibility

### New Type MonoMac.MediaAccessibility.MAAudibleMedia

<pre style='color: green'>
public static class MAAudibleMedia {
	// properties
	public static MonoMac.Foundation.NSString SettingsChangedNotification { get; }
	// methods
	public static string[] GetPreferredCharacteristics ();

	// inner types
	public static class Notifications {
		// methods
		public static MonoMac.Foundation.NSObject ObserveSettingsChanged (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MonoMac.MediaAccessibility.MAMediaCharacteristic

<pre style='color: green'>
public static class MAMediaCharacteristic {
	// properties
	public static MonoMac.Foundation.NSString DescribesMusicAndSoundForAccessibility { get; }
	public static MonoMac.Foundation.NSString DescribesVideoForAccessibility { get; }
	public static MonoMac.Foundation.NSString TranscribesSpokenDialogForAccessibility { get; }
}
</pre>

## Namespace MonoMac.ObjCRuntime

### Type Changed: MonoMac.ObjCRuntime.BlockDescriptor

Added field:

<pre style='color: green'>
	public IntPtr signature;
</pre>

### Type Changed: MonoMac.ObjCRuntime.BlockFlags

Added value:

<pre style='color: green'>
	BLOCK_HAS_SIGNATURE = 1073741824,
</pre>

### Type Changed: MonoMac.ObjCRuntime.BlockLiteral

Added method:

<pre style='color: green'>
	public static bool IsManagedBlock (IntPtr block);
</pre>

### Type Changed: MonoMac.ObjCRuntime.iOSAttribute

Added constructor:

<pre style='color: green'>
	public iOSAttribute (byte major, byte minor, byte subminor);
</pre>

### Type Changed: MonoMac.ObjCRuntime.MacAttribute

Added constructors:

<pre style='color: green'>
	public MacAttribute (byte major, byte minor);
	public MacAttribute (byte major, byte minor, byte subminor);
	public MacAttribute (byte major, byte minor, byte subminor, bool onlyOn64);
</pre>

### Type Changed: MonoMac.ObjCRuntime.Messaging

Removed methods:

<pre style='color: red'>
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, int arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, int arg4);
</pre>

Added methods:

<pre style='color: green'>
	public static bool bool_objc_msgSend_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoMac.Foundation.NSRange arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref IntPtr arg5);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoMac.Foundation.NSRange arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref IntPtr arg5);
	public static float float_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static float float_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, IntPtr arg15);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_NSRange_ref_Int32 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, ref int arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static IntPtr IntPtr_objc_msgSend_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSend_UInt16_bool_bool (IntPtr receiver, IntPtr selector, ushort arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSend_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, IntPtr arg15);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_NSRange_ref_Int32 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, ref int arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt16_bool_bool (IntPtr receiver, IntPtr selector, ushort arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSend_stret_IntPtr_UInt64_NSRange (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSendSuper_stret_IntPtr_UInt64_NSRange (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static void RectangleF_objc_msgSend_stret_NSRange_out_NSRange (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static void RectangleF_objc_msgSendSuper_stret_NSRange_out_NSRange (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSend_IntPtr_NSRange_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2, MonoMac.Foundation.NSRange arg3);
	public static void void_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_IntPtr_NSRange_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2, MonoMac.Foundation.NSRange arg3);
	public static void void_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
</pre>

### Type Changed: MonoMac.ObjCRuntime.Platform

Added value:

<pre style='color: green'>
	Mac_10_10_3 = 2825757768286208,
</pre>

## Namespace MonoMac.PdfKit

### Type Changed: MonoMac.PdfKit.PdfAreaOfInterest

Added value:

<pre style='color: green'>
	ImageArea = 256,
</pre>

### Type Changed: MonoMac.PdfKit.PdfView

Added interface:

<pre style='color: green'>
	MonoMac.AppKit.INSMenuDelegate
</pre>

Added methods:

<pre style='color: green'>
	public virtual System.Drawing.RectangleF ConfinementRectForMenu (MonoMac.AppKit.NSMenu menu, MonoMac.AppKit.NSScreen screen);
	public virtual PdfAreaOfInterest GetAreaOfInterest (System.Drawing.PointF point);
	public virtual bool HasKeyEquivalentForEvent (MonoMac.AppKit.NSMenu menu, MonoMac.AppKit.NSEvent theEvent, MonoMac.Foundation.NSObject target, MonoMac.ObjCRuntime.Selector action);
	public virtual void MenuDidClose (MonoMac.AppKit.NSMenu menu);
	public virtual int MenuItemCount (MonoMac.AppKit.NSMenu menu);
	public virtual void MenuWillHighlightItem (MonoMac.AppKit.NSMenu menu, MonoMac.AppKit.NSMenuItem item);
	public virtual void MenuWillOpen (MonoMac.AppKit.NSMenu menu);
	public virtual void NeedsUpdate (MonoMac.AppKit.NSMenu menu);
	public virtual bool UpdateItem (MonoMac.AppKit.NSMenu menu, MonoMac.AppKit.NSMenuItem item, int atIndex, bool shouldCancel);
</pre>

## Namespace MonoMac.QTKit

### Type Changed: MonoMac.QTKit.QTCaptureConnection

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

Removed method:

<pre style='color: red'>
	public virtual void SetAttribute (MonoMac.Foundation.NSObject attribute, string key);
</pre>

Modified methods:

```
public virtual MonoMac.Foundation.NSObject GetAttribute (string attributeKey)
```

Added methods:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSObject GetAttribute (MonoMac.Foundation.NSString attributeKey);
	public virtual void SetAttribute (MonoMac.Foundation.NSObject attribute, MonoMac.Foundation.NSString key);
</pre>

### Type Changed: MonoMac.QTKit.QTCaptureDevice

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString AVCTransportControlsAttribute { get; }
	public static MonoMac.Foundation.NSString AVCTransportControlsPlaybackModeKey { get; }
	public static MonoMac.Foundation.NSString AVCTransportControlsSpeedKey { get; }
	public static MonoMac.Foundation.NSString SuspendedAttribute { get; }
</pre>

### Type Changed: MonoMac.QTKit.QTCompressionOptions

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

Added method:

<pre style='color: green'>
	public string[] GetCompressionOptionsIdentifiers (QTMediaType forMediaType);
</pre>

### Type Changed: MonoMac.QTKit.QTFormatDescription

Added property:

<pre style='color: green'>
	public QTMediaType MediaTypeValue { get; }
</pre>

### Type Changed: MonoMac.QTKit.QTMedia

Added method:

<pre style='color: green'>
	public IntPtr Constructors (IntPtr quicktimeMedia, out MonoMac.Foundation.NSError error);
</pre>

### Type Changed: MonoMac.QTKit.QTMovie

Obsoleted constructors:

```
[Obsolete ("Use the MoveWithTimeRange method instead"]
	public QTMovie (QTTimeRange range, out MonoMac.Foundation.NSError error);
```

Added methods:

<pre style='color: green'>
	public QTMovie MovieWithTimeRange (QTTimeRange range, out MonoMac.Foundation.NSError error);
	public QTTrack[] TracksOfMediaType (QTMediaType mediaType);
</pre>

### New Type MonoMac.QTKit.QTErrorKey

<pre style='color: green'>
public static class QTErrorKey {
	// properties
	public static MonoMac.Foundation.NSString CaptureInput { get; }
	public static MonoMac.Foundation.NSString CaptureOutput { get; }
	public static MonoMac.Foundation.NSString Device { get; }
	public static MonoMac.Foundation.NSString Domain { get; }
	public static MonoMac.Foundation.NSString ExcludingDevice { get; }
	public static MonoMac.Foundation.NSString FileSize { get; }
	public static MonoMac.Foundation.NSString RecordingSuccesfullyFinished { get; }
	public static MonoMac.Foundation.NSString Time { get; }
}
</pre>

## Namespace MonoMac.SceneKit

### Type Changed: MonoMac.SceneKit.SCNParticleSystem

Added properties:

<pre style='color: green'>
	public SCNPropertyControllers PropertyControllers { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakPropertyControllers { get; set; }
</pre>

Modified methods:

```
public virtual void HandleEvent (SCNParticleEvent evnt, MonoMac.Foundation.NSString[] properties particleProperties, SCNParticleEventHandler handler)
```

### New Type MonoMac.SceneKit.SCNParticleProperty

<pre style='color: green'>
public static class SCNParticleProperty {
	// properties
	public static MonoMac.Foundation.NSString Angle { get; }
	public static MonoMac.Foundation.NSString AngularVelocity { get; }
	public static MonoMac.Foundation.NSString Bounce { get; }
	public static MonoMac.Foundation.NSString Charge { get; }
	public static MonoMac.Foundation.NSString Color { get; }
	public static MonoMac.Foundation.NSString Frame { get; }
	public static MonoMac.Foundation.NSString FrameRate { get; }
	public static MonoMac.Foundation.NSString Friction { get; }
	public static MonoMac.Foundation.NSString Life { get; }
	public static MonoMac.Foundation.NSString Opacity { get; }
	public static MonoMac.Foundation.NSString Position { get; }
	public static MonoMac.Foundation.NSString RotationAxis { get; }
	public static MonoMac.Foundation.NSString Size { get; }
	public static MonoMac.Foundation.NSString Velocity { get; }
}
</pre>

### New Type MonoMac.SceneKit.SCNPhysicsCollisionCategory

<pre style='color: green'>
[Serializable]
public enum SCNPhysicsCollisionCategory {
	All = 4294967295,
	Default = 1,
	None = 0,
	Static = 2,
}
</pre>

### New Type MonoMac.SceneKit.SCNPropertyControllers

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

## Namespace MonoMac.WebKit

### Type Changed: MonoMac.WebKit.DomEvent

Added constructor:

<pre style='color: green'>
	public DomEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
```

### Type Changed: MonoMac.WebKit.DomKeyboardEvent

Added constructors:

<pre style='color: green'>
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: MonoMac.WebKit.DomMouseEvent

Added constructor:

<pre style='color: green'>
	public DomMouseEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
```

### Type Changed: MonoMac.WebKit.DomOverflowEvent

Added constructor:

<pre style='color: green'>
	public DomOverflowEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
```

### Type Changed: MonoMac.WebKit.DomProcessingInstruction


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.WebKit.DomNode</span></span>

 <span style='color:green'>MonoMac.WebKit.DomCharacterData</span>

### Type Changed: MonoMac.WebKit.DomUIEvent

Added constructor:

<pre style='color: green'>
	public DomUIEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
```

### Type Changed: MonoMac.WebKit.DomWheelEvent

Added constructor:

<pre style='color: green'>
	public DomWheelEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead"]
	public virtual void InitEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

## New Namespace MonoMac.MapKit

### New Type MonoMac.MapKit.MKOverlayView

<pre style='color: green'>
public class MKOverlayView {
	// constructors
	public MKOverlayView ();
	// methods
	public static float MKRoadWidthAtZoomScale (float zoomScale);
}
</pre>

## New Namespace MonoMac.SearchKit

### New Type MonoMac.SearchKit.SKDocument

<pre style='color: green'>
public class SKDocument : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// constructors
	public SKDocument (string name, SKDocument parent, string scheme);
	public SKDocument (MonoMac.Foundation.NSUrl url);
	// properties
	public virtual IntPtr Handle { get; }
	public string Name { get; }
	public string Scheme { get; }
	public MonoMac.Foundation.NSUrl Url { get; }
	// methods
	protected override void ~SKDocument ();
	protected virtual void Dispose (bool disposing);
	public SKDocument GetParent ();
}
</pre>

### New Type MonoMac.SearchKit.SKIndex

<pre style='color: green'>
public class SKIndex : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// properties
	public SKTextAnalysis AnalysisProperties { get; }
	public int DocumentCount { get; }
	public virtual IntPtr Handle { get; }

	[Obsolete ("Apple recommends to use Flush instead of setting these parameters")]
	public int MaximumBytesBeforeFlush { get; set; }
	public int MaximumDocumentID { get; }
	public int MaximumTermID { get; }
	// methods
	protected override void ~SKIndex ();
	public bool AddDocument (SKDocument document, string mimeHint, bool canReplace);
	public bool AddDocumentWithText (SKDocument doc, string text, bool canReplace);
	public void Close ();
	public bool Compact ();
	public static SKIndex CreateWithMutableData (MonoMac.Foundation.NSMutableData data, string indexName, SKIndexType type, SKTextAnalysis analysisProperties);
	public static SKIndex CreateWithUrl (MonoMac.Foundation.NSUrl url, string indexName, SKIndexType type, SKTextAnalysis analysisProperties);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public bool Flush ();
	public static SKIndex FromData (MonoMac.Foundation.NSData data, string indexName);
	public static SKIndex FromMutableData (MonoMac.Foundation.NSMutableData data, string indexName);
	public static SKIndex FromUrl (MonoMac.Foundation.NSUrl url, string indexName, bool writeAccess);
	public SKDocument GetDocument (IntPtr documentId);
	public static void LoadDefaultExtractorPlugIns ();
	public bool MoveDocument (SKDocument document, SKDocument newParent);
	public bool RemoveDocument (SKDocument doc);
	public bool RenameDocument (SKDocument document, string newName);
	public SKSearch Search (string query, SKSearchOptions options);
	public void SetDocumentProperties (SKDocument document, MonoMac.Foundation.NSDictionary dict);
}
</pre>

### New Type MonoMac.SearchKit.SKIndexType

<pre style='color: green'>
[Serializable]
public enum SKIndexType {
	Inverted = 1,
	InvertedVector = 3,
	Unknown = 0,
	Vector = 2,
}
</pre>

### New Type MonoMac.SearchKit.SKSearch

<pre style='color: green'>
public class SKSearch : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~SKSearch ();
	public void Cancel ();
	protected virtual void Dispose (bool disposing);
	public bool FindMatches (int maxCount, ref IntPtr[] ids, double waitTime, out int foundCount);
	public bool FindMatches (int maxCount, ref IntPtr[] ids, ref float[] scores, double waitTime, out int foundCount);
}
</pre>

### New Type MonoMac.SearchKit.SKSearchOptions

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

### New Type MonoMac.SearchKit.SKSummary

<pre style='color: green'>
public class SKSummary : System.IDisposable, MonoMac.ObjCRuntime.INativeObject {
	// properties
	public virtual IntPtr Handle { get; }
	public int ParagraphCount { get; }
	public int SentenceCount { get; }
	// methods
	protected override void ~SKSummary ();
	public static SKSummary Create (string text);
	public static SKSummary Create (MonoMac.Foundation.NSString nsString);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public string GetParagraph (int idx);
	public string GetParagraphSummary (int maxParagraphs);
	public int GetParagraphSummaryInfo (int maxNumParagraphsInSummary, int[] rankOrderOfParagraphs, int[] paragraphIndexOfParagraphs);
	public string GetSentence (int idx);
	public string GetSentenceSummary (int maxSentences);
	public int GetSentenceSummaryInfo (int maxNumSentencesInSummary, int[] rankOrderOfSentences, int[] sentenceIndexOfSentences, int[] paragraphIndexOfSentences);
}
</pre>

### New Type MonoMac.SearchKit.SKTextAnalysis

<pre style='color: green'>
public class SKTextAnalysis : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SKTextAnalysis ();
	public SKTextAnalysis (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public string EndTermChars { get; set; }
	public MonoMac.Foundation.NSNumber MaximumTerms { get; set; }
	public int? MinTermLength { get; set; }
	public bool? ProximityIndexing { get; set; }
	public string StartTermChars { get; set; }
	public MonoMac.Foundation.NSSet StopWords { get; set; }
	public MonoMac.Foundation.NSDictionary Substitutions { get; set; }
	public string TermChars { get; set; }
}
</pre>

### New Type MonoMac.SearchKit.SKTextAnalysisKeys

<pre style='color: green'>
public static class SKTextAnalysisKeys {
	// properties
	public static MonoMac.Foundation.NSString EndTermCharsKey { get; }
	public static MonoMac.Foundation.NSString MaximumTermsKey { get; }
	public static MonoMac.Foundation.NSString MinTermLengthKey { get; }
	public static MonoMac.Foundation.NSString ProximityIndexingKey { get; }
	public static MonoMac.Foundation.NSString StartTermCharsKey { get; }
	public static MonoMac.Foundation.NSString StopWordsKey { get; }
	public static MonoMac.Foundation.NSString SubstitutionsKey { get; }
	public static MonoMac.Foundation.NSString TermCharsKey { get; }
}
</pre>
