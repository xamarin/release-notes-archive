---
id: 1FA7B106-F053-45CE-A50E-893C288C0B73
title: "From 1.12.0 to 2.0.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Modified fields:

```
public const string Version = "1.12.0" "2.0.0";
```

Added field:

```
public static const string QuickLookUILibrary = "/System/Library/Frameworks/Quartz.framework/Frameworks/QuickLookUI.framework/QuickLookUI";
```

## Namespace MonoMac.Accounts

### Type Changed: MonoMac.Accounts.ACErrorCode

Obsoleted fields:

```
[Obsolete ("Use MissingTransportMessageId"]
	MissingMessageID = 21,
```

Added value:

```
MissingTransportMessageId = 21,
```

## Namespace MonoMac.AppKit

### Type Changed: MonoMac.AppKit.NSAlert

Modified properties:

```
public virtual NSAlertDelegate Delegate { get; set; }
```

Added property:

```
public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoMac.AppKit.NSAnimation

Modified properties:

```
public virtual NSAnimationDelegate Delegate { get; set; }
```

Added property:

```
public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoMac.AppKit.NSApplication

Added field:

```
public static bool CheckForEventAndDelegateMismatches;
```

### Type Changed: MonoMac.AppKit.NSEventPhase

Added value:

```
MayBegin = 32,
```

### Type Changed: MonoMac.AppKit.NSKey

Added values:

```
ISOSection = 10,
	JISEisu = 102,
	JISKana = 104,
	JISKeypadComma = 95,
	JISUnderscore = 94,
	JISYen = 93,
```

### Type Changed: MonoMac.AppKit.NSModalResponse

Added values:

```
Cancel = 0,
	OK = 1,
```

### Type Changed: MonoMac.AppKit.NSObjectController

Modified properties:

```
public virtual NSObjectController MonoMac.Foundation.NSObject NewObject { get; }
```

### Type Changed: MonoMac.AppKit.NSStringDrawing

Added methods:

```
public static void DrawAtPoint (string This, System.Drawing.PointF point, NSStringAttributes attributes);
	public static void DrawInRect (string This, System.Drawing.RectangleF rect, NSStringAttributes attributes);
	public static System.Drawing.SizeF StringSize (string This, NSStringAttributes attributes);
```

### Type Changed: MonoMac.AppKit.NSStringDrawing_NSString

Added methods:

```
public static void DrawAtPoint (MonoMac.Foundation.NSString This, System.Drawing.PointF point, NSStringAttributes attributes);
	public static void DrawInRect (MonoMac.Foundation.NSString This, System.Drawing.RectangleF rect, NSStringAttributes attributes);
	public static System.Drawing.SizeF StringSize (MonoMac.Foundation.NSString This, NSStringAttributes attributes);
```

### Type Changed: MonoMac.AppKit.NSTextFinderBarContainer

Added property:

```
public virtual NSView ContentView { get; }
```

### Type Changed: MonoMac.AppKit.NSTextFinderBarContainer_Extensions

Added method:

```
public static NSView GetContentView (INSTextFinderBarContainer This);
```

### Type Changed: MonoMac.AppKit.NSTextStorage

Added constructors:

```
public NSTextStorage (MonoMac.Foundation.NSAttributedString other);
	public NSTextStorage (string str, MonoMac.Foundation.NSDictionary attributes);
	public NSTextStorage (string str, MonoMac.CoreText.CTStringAttributes attributes);
```

### Type Changed: MonoMac.AppKit.NSTextView

Added method:

```
public virtual void ToggleQuickLookPreviewPanel (MonoMac.Foundation.NSObject sender);
```

### New Type MonoMac.AppKit.NSCoderAppKitAddons

```
public static class NSCoderAppKitAddons {
	// methods
	public static NSColor DecodeNXColor (MonoMac.Foundation.NSCoder This);
}
```

### New Type MonoMac.AppKit.NSFunctionKey

```
[Serializable]
public enum NSFunctionKey {
	Begin = 63274,
	Break = 63282,
	ClearDisplay = 63290,
	ClearLine = 63289,
	Delete = 63272,
	DeleteChar = 63294,
	DeleteLine = 63292,
	DownArrow = 63233,
	End = 63275,
	Execute = 63298,
	F1 = 63236,
	F10 = 63245,
	F11 = 63246,
	F12 = 63247,
	F13 = 63248,
	F14 = 63249,
	F15 = 63250,
	F16 = 63251,
	F17 = 63252,
	F18 = 63253,
	F19 = 63254,
	F2 = 63237,
	F20 = 63255,
	F21 = 63256,
	F22 = 63257,
	F23 = 63258,
	F24 = 63259,
	F25 = 63260,
	F26 = 63261,
	F27 = 63262,
	F28 = 63263,
	F29 = 63264,
	F3 = 63238,
	F30 = 63265,
	F31 = 63266,
	F32 = 63267,
	F33 = 63268,
	F34 = 63269,
	F35 = 63270,
	F4 = 63239,
	F5 = 63240,
	F6 = 63241,
	F7 = 63242,
	F8 = 63243,
	F9 = 63244,
	Find = 63301,
	Help = 63302,
	Home = 63273,
	Insert = 63271,
	InsertChar = 63293,
	InsertLine = 63291,
	LeftArrow = 63234,
	Menu = 63285,
	ModeSwitch = 63303,
	Next = 63296,
	PageDown = 63277,
	PageUp = 63276,
	Pause = 63280,
	Prev = 63295,
	Print = 63288,
	PrintScreen = 63278,
	Redo = 63300,
	Reset = 63283,
	RightArrow = 63235,
	ScrollLock = 63279,
	Select = 63297,
	Stop = 63284,
	SysReq = 63281,
	System = 63287,
	Undo = 63299,
	UpArrow = 63232,
	User = 63286,
}
```

### New Type MonoMac.AppKit.NSMutableAttributedStringAppKitAddons

```
public static class NSMutableAttributedStringAppKitAddons {
	// methods
	public static void ApplyFontTraits (MonoMac.Foundation.NSMutableAttributedString This, NSFontTraitMask traitMask, MonoMac.Foundation.NSRange range);
	public static void FixAttachmentAttributeInRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static void FixFontAttributeInRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static void FixParagraphStyleAttributeInRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static bool ReadFromData (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSAttributedStringDocumentAttributes options, out MonoMac.Foundation.NSDictionary returnOptions);
	public static bool ReadFromData (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options, out MonoMac.Foundation.NSDictionary dict);
	public static bool ReadFromData (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSAttributedStringDocumentAttributes options, out MonoMac.Foundation.NSDictionary returnOptions, out MonoMac.Foundation.NSError error);
	public static bool ReadFromData (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSData data, MonoMac.Foundation.NSDictionary options, out MonoMac.Foundation.NSDictionary returnOptions, out MonoMac.Foundation.NSError error);
	public static bool ReadFromURL (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSAttributedStringDocumentAttributes options, out MonoMac.Foundation.NSDictionary returnOptions);
	public static bool ReadFromURL (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options, out MonoMac.Foundation.NSDictionary returnOptions);
	public static bool ReadFromURL (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSAttributedStringDocumentAttributes options, out MonoMac.Foundation.NSDictionary returnOptions, out MonoMac.Foundation.NSError error);
	public static bool ReadFromURL (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options, out MonoMac.Foundation.NSDictionary returnOptions, out MonoMac.Foundation.NSError error);
	public static void SetAlignment (MonoMac.Foundation.NSMutableAttributedString This, NSTextAlignment alignment, MonoMac.Foundation.NSRange range);
	public static void SetBaseWritingDirection (MonoMac.Foundation.NSMutableAttributedString This, NSWritingDirection writingDirection, MonoMac.Foundation.NSRange range);
	public static void SubscriptRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static void SuperscriptRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static void UnscriptRange (MonoMac.Foundation.NSMutableAttributedString This, MonoMac.Foundation.NSRange range);
	public static void UpdateAttachmentsFromPath (MonoMac.Foundation.NSMutableAttributedString This, string path);
}
```

### New Type MonoMac.AppKit.NSStringAttributeKey

```
public static class NSStringAttributeKey {
	// properties
	public static MonoMac.Foundation.NSString Attachment { get; }
	public static MonoMac.Foundation.NSString BackgroundColor { get; }
	public static MonoMac.Foundation.NSString BaselineOffset { get; }
	public static MonoMac.Foundation.NSString CharacterShape { get; }
	public static MonoMac.Foundation.NSString Cursor { get; }
	public static MonoMac.Foundation.NSString Expansion { get; }
	public static MonoMac.Foundation.NSString Font { get; }
	public static MonoMac.Foundation.NSString ForegroundColor { get; }
	public static MonoMac.Foundation.NSString GlyphInfo { get; }
	public static MonoMac.Foundation.NSString KerningAdjustment { get; }
	public static MonoMac.Foundation.NSString Ligature { get; }
	public static MonoMac.Foundation.NSString Link { get; }
	public static MonoMac.Foundation.NSString MarkedClauseSegment { get; }
	public static MonoMac.Foundation.NSString Obliqueness { get; }
	public static MonoMac.Foundation.NSString ParagraphStyle { get; }
	public static MonoMac.Foundation.NSString Shadow { get; }
	public static MonoMac.Foundation.NSString SpellingState { get; }
	public static MonoMac.Foundation.NSString StrikethroughColor { get; }
	public static MonoMac.Foundation.NSString StrikethroughStyle { get; }
	public static MonoMac.Foundation.NSString StrokeColor { get; }
	public static MonoMac.Foundation.NSString StrokeWidth { get; }
	public static MonoMac.Foundation.NSString Superscript { get; }
	public static MonoMac.Foundation.NSString TextAlternatives { get; }
	public static MonoMac.Foundation.NSString TextEffect { get; }
	public static MonoMac.Foundation.NSString ToolTip { get; }
	public static MonoMac.Foundation.NSString UnderlineColor { get; }
	public static MonoMac.Foundation.NSString UnderlineStyle { get; }
	public static MonoMac.Foundation.NSString VerticalGlyphForm { get; }
	public static MonoMac.Foundation.NSString WritingDirection { get; }
}
```

## Namespace MonoMac.AudioToolbox

### Type Changed: MonoMac.AudioToolbox.AudioConverterError

Added value:

```
AudioFormatUnsupported = 560226676,
```

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVCaptureConnection

Obsoleted properties:

```
[Obsolete ("Use AvailableAudioChannels property instead."]
	public virtual AVCaptureAudioChannel AudioChannels { get; }
```

Added property:

```
public virtual AVCaptureAudioChannel[] AvailableAudioChannels { get; }
```

### Type Changed: MonoMac.AVFoundation.AVError

Added values:

```
AirPlayControllerRequiresInternet = -11856,
	AirPlayReceiverRequiresInternet = -11857,
```

## Namespace MonoMac.CoreAnimation

### Type Changed: MonoMac.CoreAnimation.CABasicAnimation

Added methods:

```
public T GetByAs<T> ();
	public T GetFromAs<T> ();
	public T GetToAs<T> ();
	public void SetBy (MonoMac.ObjCRuntime.INativeObject value);
	public void SetFrom (MonoMac.ObjCRuntime.INativeObject value);
	public void SetTo (MonoMac.ObjCRuntime.INativeObject value);
```

### Type Changed: MonoMac.CoreAnimation.CAKeyFrameAnimation

Added methods:

```
public T[] GetValuesAs<T> ();
	public void SetValues (MonoMac.ObjCRuntime.INativeObject[] value);
```

### Type Changed: MonoMac.CoreAnimation.CALayer

Obsoleted properties:

```
[Obsolete ("Use AutoresizingMask instead"]
	public virtual CAAutoresizingMask AutoresizinMask { get; set; }
```

Added property:

```
public virtual CAAutoresizingMask AutoresizingMask { get; set; }
```

Added methods:

```
public T GetContentsAs<T> ();
	public void SetContents (MonoMac.Foundation.NSObject value);
```

## Namespace MonoMac.CoreFoundation

### Type Changed: MonoMac.CoreFoundation.CFStream

Added method:

```
public static MonoMac.CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (MonoMac.CoreServices.CFHTTPMessage request, MonoMac.Foundation.NSInputStream body);
```

### Type Changed: MonoMac.CoreFoundation.DispatchQueue

Added constructor:

```
public DispatchQueue (string label, bool concurrent);
```

Added methods:

```
public void DispatchBarrierAsync (MonoMac.Foundation.NSAction action);
	public void Submit (System.Action<int> action, long times);
```

### New Type MonoMac.CoreFoundation.CFNotificationCenter

```
public class CFNotificationCenter : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public static CFNotificationCenter Darwin { get; }
	public static CFNotificationCenter Distributed { get; }
	public virtual IntPtr Handle { get; }
	public static CFNotificationCenter Local { get; }
	// methods
	protected override void ~CFNotificationCenter ();
	public CFNotificationObserverToken AddObserver (string name, MonoMac.ObjCRuntime.INativeObject objectToObserve, System.Action<System.String,MonoMac.Foundation.NSDictionary> notificationHandler, CFNotificationSuspensionBehavior suspensionBehavior);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void PostNotification (string notification, MonoMac.ObjCRuntime.INativeObject objectToObserve, MonoMac.Foundation.NSDictionary userInfo, bool deliverImmediately, bool postOnAllSessions);
	public void RemoveEveryObserver ();
	public void RemoveObserver (CFNotificationObserverToken token);
}
```

### New Type MonoMac.CoreFoundation.CFNotificationObserverToken

```
public class CFNotificationObserverToken {
}
```

### New Type MonoMac.CoreFoundation.CFNotificationSuspensionBehavior

```
[Serializable]
public enum CFNotificationSuspensionBehavior {
	Coalesce = 2,
	DeliverImmediately = 4,
	Drop = 1,
	Hold = 3,
}
```

### New Type MonoMac.CoreFoundation.DispatchSource

```
public class DispatchSource : MonoMac.CoreFoundation.DispatchObject, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public bool IsCanceled { get; }
	// methods
	public void Cancel ();
	protected override void Dispose (bool disposing);
	public void Resume ();
	public void SetCancelHandler (System.Action handler);
	public void SetEventHandler (System.Action handler);
	public void SetRegistrationHandler (System.Action handler);

	// inner types
	public class Data : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public IntPtr PendingData { get; }
		// methods
		public void MergeData (IntPtr value);
	}
	public class DataAdd : MonoMac.CoreFoundation.DispatchSource+Data, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class DataOr : MonoMac.CoreFoundation.DispatchSource+Data, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class Mach : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public int MachPort { get; }
	}
	public class MachSend : MonoMac.CoreFoundation.DispatchSource+Mach, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, bool sendDead, DispatchQueue queue);
		// properties
		public bool SendRightsDestroyed { get; }
	}
	public class MachReceive : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, DispatchQueue queue);
	}
	public class MemoryPressure : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (MemoryPressureFlags monitorFlags, DispatchQueue queue);
		// properties
		public MemoryPressureFlags PressureFlags { get; }
	}
	public class ProcessMonitor : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int processId, ProcessMonitorFlags monitorKind, DispatchQueue queue);
		// properties
		public ProcessMonitorFlags MonitorFlags { get; }
		public int ProcessId { get; }
	}
	public class ReadMonitor : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BytesAvailable { get; }
		public int FileDescriptor { get; }
	}
	public class SignalMonitor : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int signalNumber, DispatchQueue queue);
		// properties
		public int SignalNumber { get; }
		public int SignalsDelivered { get; }
	}
	public class Timer : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
		// properties
		public int TimerFiredCount { get; }
		// methods
		public void SetTimer (DispatchTime time, long nanosecondInterval, long nanosecondLeeway);
	}
	public class VnodeMonitor : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		public DispatchSource (string path, VnodeMonitorKind vnodeKind, DispatchQueue queue);
		// properties
		public int FileDescriptor { get; }
		public VnodeMonitorKind ObservedEvents { get; }
		// methods
		protected override void Dispose (bool disposing);
	}
	public class WriteMonitor : MonoMac.CoreFoundation.DispatchSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BufferSpaceAvailable { get; }
		public int FileDescriptor { get; }
	}
}
```

### New Type MonoMac.CoreFoundation.MemoryPressureFlags

```
[Serializable]
[Flags]
public enum MemoryPressureFlags {
	Critical = 4,
	Normal = 1,
	Warn = 2,
}
```

### New Type MonoMac.CoreFoundation.ProcessMonitorFlags

```
[Serializable]
[Flags]
public enum ProcessMonitorFlags {
	Exec = 536870912,
	Exit = 2147483648,
	Fork = 1073741824,
	Signal = 134217728,
}
```

### New Type MonoMac.CoreFoundation.VnodeMonitorKind

```
[Serializable]
[Flags]
public enum VnodeMonitorKind {
	Attrib = 8,
	Delete = 1,
	Extend = 4,
	Link = 16,
	Rename = 32,
	Revoke = 64,
	Write = 2,
}
```

## Namespace MonoMac.CoreGraphics

### Type Changed: MonoMac.CoreGraphics.CGBitmapContext

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.CoreGraphics.CGGradientDrawingOptions

Added value:

```
None = 0,
```

## Namespace MonoMac.CoreImage

### Type Changed: MonoMac.CoreImage.CIColor

Added constructor:

```
public CIColor (MonoMac.AppKit.NSColor color);
```

## Namespace MonoMac.CoreMedia

### Type Changed: MonoMac.CoreMedia.CMClock

Obsoleted methods:

```
[Obsolete ("The CMAudioClockCreate API is only available on iOS"]
	public static CMClock CreateAudioClock (out CMClockError clockError);
```

### Type Changed: MonoMac.CoreMedia.CMTimeRange

Added fields:

```
public static CMTimeRange Invalid;
	public static CMTimeRange Zero;
```

### New Type MonoMac.CoreMedia.CMPixelFormat

```
[Serializable]
public enum CMPixelFormat {
	AlphaRedGreenBlue32bits = 32,
	BigEndian555_16bits = 16,
	BigEndian565_16bits = 1110783541,
	BlueGreenRedAlpha32bits = 1111970369,
	IndexedGrayWhiteIsZero_8bits = 40,
	LittleEndian555_16bits = 1278555445,
	LittleEndian5551_16bits = 892679473,
	LittleEndian565_16bits = 1278555701,
	RedGreenBlue24bits = 24,
	YpCbCr422_10bits = 1983000880,
	YpCbCr422_16bits = 1983000886,
	YpCbCr422_8bits = 846624121,
	YpCbCr422yuvs_8bits = 2037741171,
	YpCbCr444_10bits = 1983131952,
	YpCbCr444_8bits = 1983066168,
	YpCbCrA4444_8bits = 1983131704,
}
```

## Namespace MonoMac.Foundation

### Type Changed: MonoMac.Foundation.NSAppleScript

Added property:

```
public virtual NSAttributedString RichTextSource { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: MonoMac.Foundation.NSArray

Added method:

```
public static T[] FromArrayNative<T> (NSArray weakArray);
```

### Type Changed: MonoMac.Foundation.NSAttributedString

Added constructors:

```
public NSAttributedString (NSUrl url, NSAttributedStringDocumentAttributes options, out NSDictionary resultDocumentAttributes, out NSError error);
	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, out NSDictionary resultDocumentAttributes, out NSError error);
	public NSAttributedString (string path, out NSDictionary resultDocumentAttributes);
	public NSAttributedString (NSUrl url, out NSDictionary resultDocumentAttributes);
	public NSAttributedString (NSData data, NSDictionary options, out NSDictionary resultDocumentAttributes);
	public NSAttributedString (NSData data, NSAttributedStringDocumentAttributes options, out NSDictionary resultDocumentAttributes);
	public NSAttributedString (NSFileWrapper wrapper, out NSDictionary resultDocumentAttributes);
	public NSAttributedString (NSUrl url, NSDictionary options, out NSDictionary resultDocumentAttributes, out NSError error);
```

Added property:

```
public virtual bool ContainsAttachments { get; }
```

Added methods:

```
public static NSAttributedString CreateWithDocFormat (NSData wordDocFormat, out NSDictionary docAttributes);
	public static NSAttributedString CreateWithHTML (NSData htmlData, out NSDictionary resultDocumentAttributes);
	public static NSAttributedString CreateWithRTF (NSData rtfData, out NSDictionary resultDocumentAttributes);
	public static NSAttributedString CreateWithRTFD (NSData rtfdData, out NSDictionary resultDocumentAttributes);
	public virtual NSRange DoubleClick (uint index);
	public virtual NSData GetData (NSRange range, NSDictionary options, out NSError error);
	public NSData GetData (NSRange range, NSAttributedStringDocumentAttributes options, out NSError error);
	public virtual NSData GetDocFormat (NSRange range, NSDictionary options);
	public NSData GetDocFormat (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSFileWrapper GetFileWrapper (NSRange range, NSDictionary options, out NSError error);
	public NSFileWrapper GetFileWrapper (NSRange range, NSAttributedStringDocumentAttributes options, out NSError error);
	public virtual NSDictionary GetFontAttributes (NSRange range);
	public virtual int GetItemNumber (MonoMac.AppKit.NSTextList textList, uint index);
	public virtual uint GetLineBreak (uint beforeIndex, NSRange aRange);
	public virtual uint GetLineBreakByHyphenating (uint beforeIndex, NSRange aRange);
	public virtual uint GetNextWord (uint fromIndex, bool isForward);
	public virtual NSRange GetRange (MonoMac.AppKit.NSTextList textList, uint index);
	public virtual NSRange GetRange (MonoMac.AppKit.NSTextBlock textBlock, uint index);
	public virtual NSRange GetRange (MonoMac.AppKit.NSTextTable textTable, uint index);
	public virtual NSData GetRtf (NSRange range, NSDictionary options);
	public NSData GetRtf (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSData GetRtfd (NSRange range, NSDictionary options);
	public NSData GetRtfd (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSFileWrapper GetRtfdFileWrapper (NSRange range, NSDictionary options);
	public NSFileWrapper GetRtfdFileWrapper (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSDictionary GetRulerAttributes (NSRange range);
	public virtual NSUrl GetUrl (uint index, out NSRange effectiveRange);
```

### Type Changed: MonoMac.Foundation.NSBundle

Added methods:

```
public virtual NSAttributedString GetContextHelp (string key);
	public virtual NSUrl GetUrlForImageResource (string resource);
```

### Type Changed: MonoMac.Foundation.NSFileManager

Added method:

```
public NSUrl[] GetMountedVolumes (NSString[] properties, NSVolumeEnumerationOptions options);
```

### Type Changed: MonoMac.Foundation.NSFileWrapper

Added property:

```
public virtual MonoMac.AppKit.NSImage Icon { get; set; }
```

### Type Changed: MonoMac.Foundation.NSStream

Added methods:

```
public static void CreateBoundPair (out NSInputStream readStream, out NSOutputStream writeStream, int bufferSize);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocket (MonoMac.CoreFoundation.CFSocket socket, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
```

### Type Changed: MonoMac.Foundation.NSTextCheckingResult

Added properties:

```
public NSTextCheckingAddressComponents AddressComponents { get; }
	public virtual string[] AlternativeStrings { get; }
	public NSTextCheckingTransitComponents Components { get; }
	public virtual NSDate Date { get; }
	public virtual string[] GrammarDetails { get; }
	public virtual uint NumberOfRanges { get; }
	public virtual NSOrthography Orthography { get; }
	public virtual string PhoneNumber { get; }
	public virtual string ReplacementString { get; }
	public virtual double TimeInterval { get; }
	public virtual NSTimeZone TimeZone { get; }
	public virtual NSUrl Url { get; }
	public virtual NSDictionary WeakAddressComponents { get; }
	public virtual NSDictionary WeakComponents { get; }
```

Added methods:

```
public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult AddressCheckingResult (NSRange range, NSTextCheckingAddressComponents components);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString, string[] alternativeStrings);
	public static NSTextCheckingResult CorrectionCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DashCheckingResult (NSRange range, string replacementString);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date);
	public static NSTextCheckingResult DateCheckingResult (NSRange range, NSDate date, NSTimeZone timezone, double duration);
	protected override void Dispose (bool disposing);
	public static NSTextCheckingResult GrammarCheckingResult (NSRange range, string[] details);
	public static NSTextCheckingResult LinkCheckingResult (NSRange range, NSUrl url);
	public static NSTextCheckingResult OrthographyCheckingResult (NSRange range, NSOrthography ortography);
	public static NSTextCheckingResult PhoneNumberCheckingResult (NSRange range, string phoneNumber);
	public static NSTextCheckingResult QuoteCheckingResult (NSRange range, NSString replacementString);
	public virtual NSRange RangeAtIndex (uint idx);
	public static NSTextCheckingResult ReplacementCheckingResult (NSRange range, string replacementString);
	public virtual NSTextCheckingResult ResultByAdjustingRanges (int offset);
	public static NSTextCheckingResult SpellCheckingResult (NSRange range);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSTextCheckingTransitComponents components);
```

### Type Changed: MonoMac.Foundation.NSTextCheckingType

Added values:

```
PhoneNumber = 2048,
	RegularExpression = 1024,
	TransitInformation = 4096,
```

### Type Changed: MonoMac.Foundation.NSUrl

Added property:

```
public virtual string PathExtension { get; }
```

### Type Changed: MonoMac.Foundation.NSUrlSession

Obsoleted methods:

```
[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual void GetTasks (NSUrlSessionPendingTasks completionHandler);
	[Obsolete ("Use GetTasks2 instead. This method may throw spurious InvalidCastExceptions, in particular for backgrounded tasks."]
	public virtual System.Threading.Tasks.Task<NSUrlSessionActiveTasks> GetTasksAsync ();
```

Added methods:

```
public void GetTasks2 (NSUrlSessionPendingTasks2 completionHandler);
	public System.Threading.Tasks.Task<NSUrlSessionActiveTasks2> GetTasks2Async ();
```

### Type Changed: MonoMac.Foundation.PreserveAttribute

Added constructor:

```
public PreserveAttribute (System.Type type);
```

### Type Changed: MonoMac.Foundation.ProtocolAttribute

Added property:

```
public bool IsInformal { get; set; }
```

### New Type MonoMac.Foundation.NSAttributedStringDocumentAttributes

```
public class NSAttributedStringDocumentAttributes : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public NSAttributedStringDocumentAttributes ();
	public NSAttributedStringDocumentAttributes (NSDictionary dictionary);
	// properties
	public NSUrl BaseUrl { get; set; }
	public NSDocumentType DocumentType { get; set; }
	public NSStringEncoding? StringEncoding { get; set; }
	public string TextEncodingName { get; set; }
	public float? TextSizeMultiplier { get; set; }
	public float? Timeout { get; set; }
	public NSDictionary WeakDefaultAttributes { get; set; }
	public NSString WeakDocumentType { get; set; }
	public MonoMac.WebKit.WebPreferences WebPreferences { get; set; }
	public NSObject WebResourceLoadDelegate { get; set; }
}
```

### New Type MonoMac.Foundation.NSDocumentType

```
[Serializable]
public enum NSDocumentType {
	DocFormat = 5,
	HTML = 3,
	MacSimpleText = 4,
	OfficeOpenXml = 7,
	OpenDocument = 9,
	PlainText = 0,
	RTF = 1,
	RTFD = 2,
	Unknown = -1,
	WebArchive = 8,
	WordML = 6,
}
```

### New Type MonoMac.Foundation.NSTextChecking

```
public static class NSTextChecking {
	// properties
	public static NSString AirlineKey { get; }
	public static NSString CityKey { get; }
	public static NSString CountryKey { get; }
	public static NSString FlightKey { get; }
	public static NSString JobTitleKey { get; }
	public static NSString NameKey { get; }
	public static NSString OrganizationKey { get; }
	public static NSString PhoneKey { get; }
	public static NSString StateKey { get; }
	public static NSString StreetKey { get; }
	public static NSString ZipKey { get; }
}
```

### New Type MonoMac.Foundation.NSTextCheckingAddressComponents

```
public class NSTextCheckingAddressComponents : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingAddressComponents ();
	public NSTextCheckingAddressComponents (NSDictionary dictionary);
	// properties
	public string City { get; }
	public string Country { get; }
	public string JobTitle { get; }
	public string Name { get; }
	public string Organization { get; }
	public string Phone { get; }
	public string State { get; }
	public string Street { get; }
	public string ZIP { get; }
}
```

### New Type MonoMac.Foundation.NSTextCheckingTransitComponents

```
public class NSTextCheckingTransitComponents : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingTransitComponents ();
	public NSTextCheckingTransitComponents (NSDictionary dictionary);
	// properties
	public string Airline { get; }
	public string Flight { get; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionActiveTasks2

```
public class NSUrlSessionActiveTasks2 {
	// constructors
	public NSUrlSessionActiveTasks2 (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
	// properties
	public NSUrlSessionTask[] DataTasks { get; set; }
	public NSUrlSessionTask[] DownloadTasks { get; set; }
	public NSUrlSessionTask[] UploadTasks { get; set; }
}
```

### New Type MonoMac.Foundation.NSUrlSessionPendingTasks2

```
public sealed delegate NSUrlSessionPendingTasks2 : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionPendingTasks2 (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionTask[] dataTasks, NSUrlSessionTask[] uploadTasks, NSUrlSessionTask[] downloadTasks);
}
```

## Namespace MonoMac.NetworkExtension

### Type Changed: MonoMac.NetworkExtension.NEVpnIke2DiffieHellman

Added values:

```
Group19 = 19,
	Group20 = 20,
	Group21 = 21,
```

### Type Changed: MonoMac.NetworkExtension.NEVpnIke2EncryptionAlgorithm

Added values:

```
AES128GCM = 5,
	AES256GCM = 6,
```

### New Type MonoMac.NetworkExtension.NEVpnIke2CertificateType

```
[Serializable]
public enum NEVpnIke2CertificateType {
	ECDSA256 = 2,
	ECDSA384 = 3,
	ECDSA521 = 4,
	RSA = 1,
}
```

## Namespace MonoMac.ObjCRuntime

### Type Changed: MonoMac.ObjCRuntime.Dlfcn

Added method:

```
public static IntPtr dlsym (Dlfcn.RTLD lookupType, string symbol);
```

### Type Changed: MonoMac.ObjCRuntime.Messaging

Added methods:

```
public static bool bool_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref IntPtr arg3, ref IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref IntPtr arg3, ref IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, double arg4);
	public static IntPtr IntPtr_objc_msgSend_NSRange_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_UInt32_out_NSRange (IntPtr receiver, IntPtr selector, uint arg1, out MonoMac.Foundation.NSRange arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_IntPtr_Double (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, double arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_NSRange_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt32_out_NSRange (IntPtr receiver, IntPtr selector, uint arg1, out MonoMac.Foundation.NSRange arg2);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSend_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static void NSRange_objc_msgSend_stret_IntPtr_UInt32 (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static void NSRange_objc_msgSend_stret_UInt32 (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, uint arg1);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static void NSRange_objc_msgSendSuper_stret_IntPtr_UInt32 (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static void NSRange_objc_msgSendSuper_stret_UInt32 (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, uint arg1);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
	public static uint UInt32_objc_msgSend_UInt32_bool (IntPtr receiver, IntPtr selector, uint arg1, bool arg2);
	public static uint UInt32_objc_msgSend_UInt32_NSRange (IntPtr receiver, IntPtr selector, uint arg1, MonoMac.Foundation.NSRange arg2);
	public static uint UInt32_objc_msgSendSuper_UInt32_bool (IntPtr receiver, IntPtr selector, uint arg1, bool arg2);
	public static uint UInt32_objc_msgSendSuper_UInt32_NSRange (IntPtr receiver, IntPtr selector, uint arg1, MonoMac.Foundation.NSRange arg2);
```

### Type Changed: MonoMac.ObjCRuntime.Platform

Added value:

```
iOS_8_3 = 525056,
```

### Type Changed: MonoMac.ObjCRuntime.Runtime

Added methods:

```
public static void ConnectMethod (System.Type type, System.Reflection.MethodInfo method, MonoMac.Foundation.ExportAttribute export);
	public static void ConnectMethod (System.Type type, System.Reflection.MethodInfo method, Selector selector);
```

### Type Changed: MonoMac.ObjCRuntime.ThreadSafeAttribute

Added constructor:

```
public ThreadSafeAttribute (bool safe);
```

Added property:

```
public bool Safe { get; }
```

### New Type MonoMac.ObjCRuntime.CategoryAttribute

```
public class CategoryAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public CategoryAttribute (System.Type type);
	// properties
	public string Name { get; set; }
	public System.Type Type { get; set; }
}
```

### New Type MonoMac.ObjCRuntime.Protocol

```
public class Protocol : INativeObject {
	// constructors
	public Protocol (string name);
	public Protocol (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	public string Name { get; }
	// methods
	public static IntPtr GetHandle (string name);
}
```

## Namespace MonoMac.SceneKit

### Type Changed: MonoMac.SceneKit.SCNGeometry

Obsoleted methods:

```
[Obsolete ("Use the Create(SCNGeometrySource[], SCNGeometryElement[]) method instead, as it has a strongly typed return"]
	public static MonoMac.Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

Added method:

```
public static SCNGeometry Create (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

## Namespace MonoMac.ScriptingBridge

### Type Changed: MonoMac.ScriptingBridge.SBApplication

Added methods:

```
public static T FromBundleIdentifier<T> (string ident);
	public static T FromProcessIdentifier<T> (int pid);
	public static T FromURL<T> (MonoMac.Foundation.NSUrl url);
```

### New Type MonoMac.ScriptingBridge.SBElementArray

```
public class SBElementArray : MonoMac.Foundation.NSMutableArray, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public SBElementArray (MonoMac.Foundation.NSCoder coder);
	public SBElementArray (MonoMac.Foundation.NSObjectFlag t);
	public SBElementArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject[] ArrayByApplyingSelector (MonoMac.ObjCRuntime.Selector selector);
	public virtual MonoMac.Foundation.NSObject[] ArrayByApplyingSelector (MonoMac.ObjCRuntime.Selector aSelector, MonoMac.Foundation.NSObject argument);
	public virtual MonoMac.Foundation.NSObject[] Get ();
	public virtual MonoMac.Foundation.NSObject ObjectAtLocation (MonoMac.Foundation.NSObject location);
	public virtual MonoMac.Foundation.NSObject ObjectWithID (MonoMac.Foundation.NSObject identifier);
	public virtual MonoMac.Foundation.NSObject ObjectWithName (string name);
}
```

## Namespace MonoMac.Security

### Type Changed: MonoMac.Security.SecPadding

Added value:

```
Raw = 16384,
```

### Type Changed: MonoMac.Security.SecRecord

Added constructor:

```
public SecRecord ();
```

### Type Changed: MonoMac.Security.SecStatusCode

Added values:

```
ACLAddFailed = -67698,
	ACLChangeFailed = -67699,
	ACLDeleteFailed = -67696,
	ACLNotSimple = -25240,
	ACLReplaceFailed = -67697,
	AddinLoadFailed = -67711,
	AddinUnloadFailed = -67714,
	AlgorithmMismatch = -67730,
	AlreadyLoggedIn = -67814,
	AppleAddAppACLSubject = -67589,
	AppleInvalidKeyEndDate = -67593,
	AppleInvalidKeyStartDate = -67592,
	ApplePublicKeyIncomplete = -67590,
	AppleSignatureMismatch = -67591,
	AppleSSLv2Rollback = -67595,
	AttachHandleBusy = -67728,
	AttributeNotInContext = -67720,
	BlockSizeMismatch = -67810,
	BufferTooSmall = -25301,
	CallbackFailed = -67695,
	CertificateCannotOperate = -67817,
	CertificateExpired = -67818,
	CertificateNotValidYet = -67819,
	CertificateRevoked = -67820,
	CertificateSuspended = -67821,
	CodeSigningBadCertChainLength = -67647,
	CodeSigningBadPathLengthConstraint = -67649,
	CodeSigningDevelopment = -67651,
	CodeSigningNoBasicConstraints = -67648,
	CodeSigningNoExtendedKeyUsage = -67650,
	ConversionError = -67594,
	CoreFoundationUnknown = -4960,
	CreateChainFailed = -25318,
	CRLAlreadySigned = -67684,
	CRLBadURI = -67617,
	CRLExpired = -67613,
	CRLNotFound = -67615,
	CRLNotTrusted = -67620,
	CRLNotValidYet = -67614,
	CRLPolicyFailed = -67621,
	CRLServerDown = -67616,
	DatabaseLocked = -67869,
	DataNotAvailable = -25316,
	DataNotModifiable = -25317,
	DatastoreIsOpen = -67870,
	DataTooLarge = -25302,
	DeviceError = -67727,
	DeviceFailed = -67588,
	DeviceReset = -67587,
	DeviceVerifyFailed = -67812,
	DiskFull = -34,
	DuplicateCallback = -25297,
	EMMLoadFailed = -67709,
	EMMUnloadFailed = -67710,
	EndOfData = -67634,
	EventNotificationCallbackNotFound = -67723,
	ExtendedKeyUsageNotCritical = -67881,
	FieldSpecifiedMultiple = -67866,
	FileTooBig = -67597,
	FunctionFailed = -67677,
	FunctionIntegrityFail = -67670,
	HostNameMismatch = -67602,
	IDPFailure = -67622,
	IncompatibleDatabaseBlob = -67600,
	IncompatibleFieldFormat = -67867,
	IncompatibleKeyBlob = -67601,
	IncompatibleVersion = -67704,
	IncompleteCertRevocationCheck = -67635,
	InDarkWake = -25320,
	InputLengthError = -67724,
	InsufficientClientID = -67586,
	InsufficientCredentials = -67822,
	InteractionRequired = -25315,
	InternalError = -67671,
	InvaldCRLAuthority = -67827,
	InvalidAccessCredentials = -67700,
	InvalidAccessRequest = -67876,
	InvalidACL = -67702,
	InvalidAction = -67823,
	InvalidAddinFunctionTable = -67716,
	InvalidAlgorithm = -67747,
	InvalidAlgorithmParms = -67770,
	InvalidAttributeAccessCredentials = -67796,
	InvalidAttributeBase = -67788,
	InvalidAttributeBlockSize = -67764,
	InvalidAttributeDLDBHandle = -67794,
	InvalidAttributeEffectiveBits = -67778,
	InvalidAttributeEndDate = -67782,
	InvalidAttributeInitVector = -67750,
	InvalidAttributeIterationCount = -67792,
	InvalidAttributeKey = -67748,
	InvalidAttributeKeyLength = -67762,
	InvalidAttributeKeyType = -67774,
	InvalidAttributeLabel = -67772,
	InvalidAttributeMode = -67776,
	InvalidAttributeOutputSize = -67766,
	InvalidAttributePadding = -67754,
	InvalidAttributePassphrase = -67760,
	InvalidAttributePrime = -67786,
	InvalidAttributePrivateKeyFormat = -67800,
	InvalidAttributePublicKeyFormat = -67798,
	InvalidAttributeRandom = -67756,
	InvalidAttributeRounds = -67768,
	InvalidAttributeSalt = -67752,
	InvalidAttributeSeed = -67758,
	InvalidAttributeStartDate = -67780,
	InvalidAttributeSubprime = -67790,
	InvalidAttributeSymmetricKeyFormat = -67802,
	InvalidAttributeVersion = -67784,
	InvalidAttributeWrappedKeyFormat = -67804,
	InvalidAuthority = -67824,
	InvalidAuthorityKeyID = -67606,
	InvalidBaseACLs = -67851,
	InvalidBundleInfo = -67857,
	InvalidCallback = -25298,
	InvalidCertAuthority = -67826,
	InvalidCertificateGroup = -67691,
	InvalidCertificateRef = -67690,
	InvalidContext = -67746,
	InvalidCRL = -67830,
	InvalidCRLEncoding = -67828,
	InvalidCRLGroup = -67816,
	InvalidCRLIndex = -67858,
	InvalidCRLType = -67829,
	InvalidData = -67673,
	InvalidDatabaseBlob = -67598,
	InvalidDBList = -67681,
	InvalidDBLocation = -67875,
	InvalidDigestAlgorithm = -67815,
	InvalidEncoding = -67853,
	InvalidExtendedKeyUsage = -67609,
	InvalidFormType = -67831,
	InvalidGUID = -67679,
	InvalidHandle = -67680,
	InvalidHandleUsage = -67668,
	InvalidID = -67832,
	InvalidIdentifier = -67833,
	InvalidIDLinkage = -67610,
	InvalidIndex = -67834,
	InvalidIndexInfo = -67877,
	InvalidInputVector = -67744,
	InvalidItemRef = -25304,
	InvalidKeyAttributeMask = -67738,
	InvalidKeyBlob = -67599,
	InvalidKeyFormat = -67742,
	InvalidKeyHierarchy = -67713,
	InvalidKeyLabel = -67740,
	InvalidKeyRef = -67712,
	InvalidKeyUsageForPolicy = -67608,
	InvalidKeyUsageMask = -67736,
	InvalidLoginName = -67813,
	InvalidModifyMode = -67879,
	InvalidName = -67689,
	InvalidNetworkAddress = -67683,
	InvalidNewOwner = -67878,
	InvalidNumberOfFields = -67685,
	InvalidOutputVector = -67745,
	InvalidOwnerEdit = -25244,
	InvalidParsingModule = -67868,
	InvalidPassthroughID = -67682,
	InvalidPasswordRef = -25261,
	InvalidPointer = -67675,
	InvalidPolicyIdentifiers = -67835,
	InvalidPrefsDomain = -25319,
	InvalidPVC = -67708,
	InvalidQuery = -67693,
	InvalidReason = -67837,
	InvalidRecord = -67701,
	InvalidRequestInputs = -67838,
	InvalidRequestor = -67855,
	InvalidResponseVector = -67839,
	InvalidRoot = -67612,
	InvalidSampleValue = -67703,
	InvalidScope = -67706,
	InvalidSearchRef = -25305,
	InvalidServiceMask = -67717,
	InvalidSignature = -67688,
	InvalidStopOnPolicy = -67840,
	InvalidSubjectKeyID = -67607,
	InvalidSubjectName = -67655,
	InvalidSubServiceID = -67719,
	InvalidTimeString = -67836,
	InvalidTrustSetting = -25242,
	InvalidTrustSettings = -25262,
	InvalidTuple = -67841,
	InvalidTupleCredendtials = -67852,
	InvalidTupleGroup = -67850,
	InvalidValidityPeriod = -67854,
	InvalidValue = -67694,
	KeyBlobTypeIncorrect = -67732,
	KeyHeaderInconsistent = -67733,
	KeyIsSensitive = -25258,
	KeySizeNotAllowed = -25311,
	KeyUsageIncorrect = -67731,
	LibraryReferenceNotFound = -67715,
	MDSError = -67674,
	MemoryError = -67672,
	MissingAlgorithmParms = -67771,
	MissingAttributeAccessCredentials = -67797,
	MissingAttributeBase = -67789,
	MissingAttributeBlockSize = -67765,
	MissingAttributeDLDBHandle = -67795,
	MissingAttributeEffectiveBits = -67779,
	MissingAttributeEndDate = -67783,
	MissingAttributeInitVector = -67751,
	MissingAttributeIterationCount = -67793,
	MissingAttributeKey = -67749,
	MissingAttributeKeyLength = -67763,
	MissingAttributeKeyType = -67775,
	MissingAttributeLabel = -67773,
	MissingAttributeMode = -67777,
	MissingAttributeOutputSize = -67767,
	MissingAttributePadding = -67755,
	MissingAttributePassphrase = -67761,
	MissingAttributePrime = -67787,
	MissingAttributePrivateKeyFormat = -67801,
	MissingAttributePublicKeyFormat = -67799,
	MissingAttributeRandom = -67757,
	MissingAttributeRounds = -67769,
	MissingAttributeSalt = -67753,
	MissingAttributeSeed = -67759,
	MissingAttributeStartDate = -67781,
	MissingAttributeSubprime = -67791,
	MissingAttributeSymmetricKeyFormat = -67803,
	MissingAttributeVersion = -67785,
	MissingAttributeWrappedKeyFormat = -67805,
	MissingRequiredExtension = -67880,
	MissingValue = -67871,
	MobileMeCSRVerifyFailure = -67665,
	MobileMeFailedConsistencyCheck = -67666,
	MobileMeNoRequestPending = -67664,
	MobileMeRequestAlreadyPending = -67663,
	MobileMeRequestQueued = -67657,
	MobileMeRequestRedirected = -67658,
	MobileMeServerAlreadyExists = -67661,
	MobileMeServerError = -67659,
	MobileMeServerNotAvailable = -67660,
	MobileMeServerServiceErr = -67662,
	ModuleManagerInitializeFailed = -67721,
	ModuleManagerNotFound = -67722,
	ModuleManifestVerifyFailed = -67678,
	ModuleNotLoaded = -67718,
	MultiplePrivateKeys = -25259,
	MultipleValuesUnsupported = -67842,
	NetworkFailure = -67636,
	NoAccessForItem = -25243,
	NoBasicConstraints = -67604,
	NoBasicConstraintsCA = -67605,
	NoCertificateModule = -25313,
	NoDefaultAuthority = -67844,
	NoDefaultKeychain = -25307,
	NoFieldValues = -67859,
	NoPolicyModule = -25314,
	NoStorageModule = -25312,
	NoSuchAttribute = -25303,
	NoSuchClass = -25306,
	NotInitialized = -67667,
	NotLoggedIn = -67729,
	NoTrustSettings = -25263,
	NotSigner = -26267,
	NotTrusted = -67843,
	OCSPBadRequest = -67631,
	OCSPBadResponse = -67630,
	OCSPNoSigner = -67640,
	OCSPNotTrustedToAnchor = -67637,
	OCSPResponderInternalError = -67642,
	OCSPResponderMalformedReq = -67641,
	OCSPResponderSignatureRequired = -67644,
	OCSPResponderTryLater = -67643,
	OCSPResponderUnauthorized = -67645,
	OCSPResponseNonceMismatch = -67646,
	OCSPSignatureError = -67639,
	OCSPStatusUnrecognized = -67633,
	OCSPUnavailable = -67632,
	OutputLengthError = -67725,
	PassphraseRequired = -25260,
	PathLengthConstraintExceeded = -67611,
	Pkcs12VerifyFailure = -25264,
	PolicyNotFound = -25241,
	PrivilegeNotGranted = -67705,
	PrivilegeNotSupported = -67726,
	PublicKeyInconsistent = -67811,
	PVCAlreadyConfigured = -67707,
	PVCReferentNotFound = -67669,
	QuerySizeUnknown = -67809,
	QuotaExceeded = -67596,
	ReadOnlyAttribute = -25309,
	RecordModified = -67638,
	RejectedForm = -67845,
	RequestDescriptor = -67856,
	RequestLost = -67846,
	RequestRejected = -67847,
	ResourceSignBadCertChainLength = -67652,
	ResourceSignBadExtKeyUsage = -67653,
	SelfCheckFailed = -67676,
	ServiceNotAvailable = -67585,
	SigningTimeMissing = -67894,
	SMIMEBadExtendedKeyUsage = -67624,
	SMIMEBadKeyUsage = -67625,
	SMIMEEmailAddressesNotFound = -67623,
	SMIMEKeyUsageNotCritical = -67626,
	SMIMENoEmailAddress = -67627,
	SMIMESubjAltNameNotCritical = -67628,
	SSLBadExtendedKeyUsage = -67629,
	StagedOperationInProgress = -67806,
	StagedOperationNotStarted = -67807,
	TagNotFound = -67692,
	TimestampAddInfoNotAvailable = -67892,
	TimestampBadAlg = -67886,
	TimestampBadDataFormat = -67888,
	TimestampBadRequest = -67887,
	TimestampInvalid = -67883,
	TimestampMissing = -67882,
	TimestampNotTrusted = -67884,
	TimestampRejection = -67895,
	TimestampRevocationNotification = -67898,
	TimestampRevocationWarning = -67897,
	TimestampServiceNotAvailable = -67885,
	TimestampSystemFailure = -67893,
	TimestampTimeNotAvailable = -67889,
	TimestampUnacceptedExtension = -67891,
	TimestampUnacceptedPolicy = -67890,
	TimestampWaiting = -67896,
	TrustNotAvailable = -25245,
	TrustSettingDeny = -67654,
	UnknownCertExtension = -67618,
	UnknownCriticalExtensionFlag = -67603,
	UnknownCRLExtension = -67619,
	UnknownFormat = -25257,
	UnknownQualifiedCertStatement = -67656,
	UnknownTag = -67687,
	UnsupportedAddressType = -67848,
	UnsupportedFieldFormat = -67860,
	UnsupportedFormat = -25256,
	UnsupportedIndexInfo = -67861,
	UnsupportedKeyAttributeMask = -67739,
	UnsupportedKeyFormat = -67734,
	UnsupportedKeyLabel = -67741,
	UnsupportedKeySize = -67735,
	UnsupportedKeyUsageMask = -67737,
	UnsupportedLocality = -67862,
	UnsupportedNumAttributes = -67863,
	UnsupportedNumIndexes = -67864,
	UnsupportedNumRecordTypes = -67865,
	UnsupportedNumSelectionPreds = -67873,
	UnsupportedOperator = -67874,
	UnsupportedQueryLimits = -67872,
	UnsupportedService = -67849,
	UnsupportedVectorOfBuffers = -67743,
	VerificationFailure = -67686,
	VerifyActionFailed = -67825,
	VerifyFailed = -67808,
	WritePermissions = -61,
	WrongSecVersion = -25310,
```

## Namespace MonoMac.StoreKit

### Type Changed: MonoMac.StoreKit.SKMutablePayment

Added property:

```
public virtual string ApplicationUsername { get; set; }
```

### Type Changed: MonoMac.StoreKit.SKPayment

Added property:

```
public virtual string ApplicationUsername { get; }
```

### Type Changed: MonoMac.StoreKit.SKPaymentQueue

Added method:

```
public virtual void RestoreCompletedTransactions (string username);
```

## New Namespace MonoMac.QuickLookUI

### New Type MonoMac.QuickLookUI.IQLPreviewItem

```
public interface IQLPreviewItem : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoMac.QuickLookUI.IQLPreviewPanelDataSource

```
public interface IQLPreviewPanelDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual int NumberOfPreviewItemsInPreviewPanel (QLPreviewPanel panel);
	public virtual QLPreviewItem PreviewItemAtIndex (QLPreviewPanel panel, int index);
}
```

### New Type MonoMac.QuickLookUI.IQLPreviewPanelDelegate

```
public interface IQLPreviewPanelDelegate : MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.AppKit.INSWindowDelegate {
}
```

### New Type MonoMac.QuickLookUI.QLPreviewItem

```
public class QLPreviewItem : MonoMac.Foundation.NSObject, IQLPreviewItem, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public QLPreviewItem ();
	public QLPreviewItem (MonoMac.Foundation.NSCoder coder);
	public QLPreviewItem (MonoMac.Foundation.NSObjectFlag t);
	public QLPreviewItem (IntPtr handle);
	// properties
	public virtual MonoMac.Foundation.NSObject PreviewItemDisplayState { get; }
	public virtual string PreviewItemTitle { get; }
	public virtual MonoMac.Foundation.NSUrl PreviewItemURL { get; }
}
```

### New Type MonoMac.QuickLookUI.QLPreviewItem_Extensions

```
public static class QLPreviewItem_Extensions {
	// methods
	public static MonoMac.Foundation.NSObject GetPreviewItemDisplayState (IQLPreviewItem This);
	public static string GetPreviewItemTitle (IQLPreviewItem This);
	public static MonoMac.Foundation.NSUrl GetPreviewItemURL (IQLPreviewItem This);
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanel

```
public class QLPreviewPanel : MonoMac.AppKit.NSPanel, MonoMac.AppKit.INSAppearanceCustomization, MonoMac.AppKit.INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public QLPreviewPanel ();
	public QLPreviewPanel (MonoMac.Foundation.NSCoder coder);
	public QLPreviewPanel (MonoMac.Foundation.NSObjectFlag t);
	public QLPreviewPanel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSObject CurrentController { get; }
	public virtual QLPreviewItem CurrentPreviewItem { get; }
	public virtual int CurrentPreviewItemIndex { get; set; }
	public QLPreviewPanelDataSource DataSource { get; set; }
	public QLPreviewPanelDelegate Delegate { get; set; }
	public virtual MonoMac.Foundation.NSObject DisplayState { get; set; }
	public virtual bool InFullScreenMode { get; }
	public virtual MonoMac.Foundation.NSObject WeakDataSource { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool EnterFullScreenMode (MonoMac.AppKit.NSScreen screen, MonoMac.Foundation.NSDictionary options);
	public bool EnterFullScreenMode ();
	public void ExitFullScreenModeWithOptions ();
	public virtual void ExitFullScreenModeWithOptions (MonoMac.Foundation.NSDictionary options);
	public virtual void RefreshCurrentPreviewItem ();
	public virtual void ReloadData ();
	public static QLPreviewPanel SharedPreviewPanel ();
	public static bool SharedPreviewPanelExists ();
	public virtual void UpdateController ();
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanelController

```
public static class QLPreviewPanelController {
	// methods
	public static bool AcceptsPreviewPanelControl (MonoMac.Foundation.NSObject This, QLPreviewPanel panel);
	public static void BeginPreviewPanelControl (MonoMac.Foundation.NSObject This, QLPreviewPanel panel);
	public static void EndPreviewPanelControl (MonoMac.Foundation.NSObject This, QLPreviewPanel panel);
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanelDataSource

```
public abstract class QLPreviewPanelDataSource : MonoMac.Foundation.NSObject, IQLPreviewPanelDataSource, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public QLPreviewPanelDataSource ();
	public QLPreviewPanelDataSource (MonoMac.Foundation.NSCoder coder);
	public QLPreviewPanelDataSource (MonoMac.Foundation.NSObjectFlag t);
	public QLPreviewPanelDataSource (IntPtr handle);
	// methods
	public virtual int NumberOfPreviewItemsInPreviewPanel (QLPreviewPanel panel);
	public virtual QLPreviewItem PreviewItemAtIndex (QLPreviewPanel panel, int index);
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanelDataSource_Extensions

```
public static class QLPreviewPanelDataSource_Extensions {
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanelDelegate

```
public class QLPreviewPanelDelegate : MonoMac.Foundation.NSObject, IQLPreviewPanelDelegate, MonoMac.AppKit.INSWindowDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable, MonoMac.Foundation.INSObjectProtocol {
	// constructors
	public QLPreviewPanelDelegate ();
	public QLPreviewPanelDelegate (MonoMac.Foundation.NSCoder coder);
	public QLPreviewPanelDelegate (MonoMac.Foundation.NSObjectFlag t);
	public QLPreviewPanelDelegate (IntPtr handle);
	// methods
	public virtual MonoMac.AppKit.NSWindow[] CustomWindowsToEnterFullScreen (MonoMac.AppKit.NSWindow window);
	public virtual MonoMac.AppKit.NSWindow[] CustomWindowsToExitFullScreen (MonoMac.AppKit.NSWindow window);
	public virtual void DidBecomeKey (MonoMac.Foundation.NSNotification notification);
	public virtual void DidBecomeMain (MonoMac.Foundation.NSNotification notification);
	public virtual void DidChangeBackingProperties (MonoMac.Foundation.NSNotification notification);
	public virtual void DidChangeScreen (MonoMac.Foundation.NSNotification notification);
	public virtual void DidChangeScreenProfile (MonoMac.Foundation.NSNotification notification);
	public virtual void DidDecodeRestorableState (MonoMac.AppKit.NSWindow window, MonoMac.Foundation.NSCoder coder);
	public virtual void DidDeminiaturize (MonoMac.Foundation.NSNotification notification);
	public virtual void DidEndLiveResize (MonoMac.Foundation.NSNotification notification);
	public virtual void DidEndSheet (MonoMac.Foundation.NSNotification notification);
	public virtual void DidEnterFullScreen (MonoMac.Foundation.NSNotification notification);
	public virtual void DidEnterVersionBrowser (MonoMac.Foundation.NSNotification notification);
	public virtual void DidExitFullScreen (MonoMac.Foundation.NSNotification notification);
	public virtual void DidExitVersionBrowser (MonoMac.Foundation.NSNotification notification);
	public virtual void DidExpose (MonoMac.Foundation.NSNotification notification);
	public virtual void DidFailToEnterFullScreen (MonoMac.AppKit.NSWindow window);
	public virtual void DidFailToExitFullScreen (MonoMac.AppKit.NSWindow window);
	public virtual void DidMiniaturize (MonoMac.Foundation.NSNotification notification);
	public virtual void DidMoved (MonoMac.Foundation.NSNotification notification);
	public virtual void DidResignKey (MonoMac.Foundation.NSNotification notification);
	public virtual void DidResignMain (MonoMac.Foundation.NSNotification notification);
	public virtual void DidResize (MonoMac.Foundation.NSNotification notification);
	public virtual void DidUpdate (MonoMac.Foundation.NSNotification notification);
	public virtual bool HandleEvent (QLPreviewPanel panel, MonoMac.AppKit.NSEvent theEvent);
	public virtual bool ShouldDragDocumentWithEvent (MonoMac.AppKit.NSWindow window, MonoMac.AppKit.NSEvent theEvent, System.Drawing.PointF dragImageLocation, MonoMac.AppKit.NSPasteboard withPasteboard);
	public virtual bool ShouldPopUpDocumentPathMenu (MonoMac.AppKit.NSWindow window, MonoMac.AppKit.NSMenu menu);
	public virtual bool ShouldZoom (MonoMac.AppKit.NSWindow window, System.Drawing.RectangleF newFrame);
	public virtual System.Drawing.RectangleF SourceFrameOnScreenForPreviewItem (QLPreviewPanel panel, QLPreviewItem item);
	public virtual void StartCustomAnimationToEnterFullScreen (MonoMac.AppKit.NSWindow window, double duration);
	public virtual void StartCustomAnimationToExitFullScreen (MonoMac.AppKit.NSWindow window, double duration);
	public virtual MonoMac.Foundation.NSObject TransitionImageForPreviewItem (QLPreviewPanel panel, QLPreviewItem item, System.Drawing.RectangleF contentRect);
	public virtual void WillBeginSheet (MonoMac.Foundation.NSNotification notification);
	public virtual void WillClose (MonoMac.Foundation.NSNotification notification);
	public virtual void WillEncodeRestorableState (MonoMac.AppKit.NSWindow window, MonoMac.Foundation.NSCoder coder);
	public virtual void WillEnterFullScreen (MonoMac.Foundation.NSNotification notification);
	public virtual void WillEnterVersionBrowser (MonoMac.Foundation.NSNotification notification);
	public virtual void WillExitFullScreen (MonoMac.Foundation.NSNotification notification);
	public virtual void WillExitVersionBrowser (MonoMac.Foundation.NSNotification notification);
	public virtual void WillMiniaturize (MonoMac.Foundation.NSNotification notification);
	public virtual void WillMove (MonoMac.Foundation.NSNotification notification);
	public virtual System.Drawing.RectangleF WillPositionSheet (MonoMac.AppKit.NSWindow window, MonoMac.AppKit.NSWindow sheet, System.Drawing.RectangleF usingRect);
	public virtual System.Drawing.SizeF WillResize (MonoMac.AppKit.NSWindow sender, System.Drawing.SizeF toFrameSize);
	public virtual System.Drawing.SizeF WillResizeForVersionBrowser (MonoMac.AppKit.NSWindow window, System.Drawing.SizeF maxPreferredSize, System.Drawing.SizeF maxAllowedSize);
	public virtual MonoMac.Foundation.NSObject WillReturnFieldEditor (MonoMac.AppKit.NSWindow sender, MonoMac.Foundation.NSObject client);
	public virtual MonoMac.Foundation.NSUndoManager WillReturnUndoManager (MonoMac.AppKit.NSWindow window);
	public virtual void WillStartLiveResize (MonoMac.Foundation.NSNotification notification);
	public virtual System.Drawing.SizeF WillUseFullScreenContentSize (MonoMac.AppKit.NSWindow window, System.Drawing.SizeF proposedSize);
	public virtual MonoMac.AppKit.NSApplicationPresentationOptions WillUseFullScreenPresentationOptions (MonoMac.AppKit.NSWindow window, MonoMac.AppKit.NSApplicationPresentationOptions proposedOptions);
	public virtual System.Drawing.RectangleF WillUseStandardFrame (MonoMac.AppKit.NSWindow window, System.Drawing.RectangleF newFrame);
	public virtual bool WindowShouldClose (MonoMac.Foundation.NSObject sender);
}
```

### New Type MonoMac.QuickLookUI.QLPreviewPanelDelegate_Extensions

```
public static class QLPreviewPanelDelegate_Extensions {
	// methods
	public static bool HandleEvent (IQLPreviewPanelDelegate This, QLPreviewPanel panel, MonoMac.AppKit.NSEvent theEvent);
	public static System.Drawing.RectangleF SourceFrameOnScreenForPreviewItem (IQLPreviewPanelDelegate This, QLPreviewPanel panel, QLPreviewItem item);
	public static MonoMac.Foundation.NSObject TransitionImageForPreviewItem (IQLPreviewPanelDelegate This, QLPreviewPanel panel, QLPreviewItem item, System.Drawing.RectangleF contentRect);
}
```

## New Namespace MonoMac.VideoToolbox

### New Type MonoMac.VideoToolbox.VTColorPrimaries

```
[Serializable]
public enum VTColorPrimaries {
	Ebu3213 = 2,
	ItuR7092 = 1,
	P22 = 4,
	SmpteC = 3,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTCompressionProperties

```
public class VTCompressionProperties : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTCompressionProperties ();
	public VTCompressionProperties (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? AllowFrameReordering { get; set; }
	public bool? AllowTemporalCompression { get; set; }
	public bool? AspectRatio16x9 { get; set; }
	public int? AverageBitRate { get; set; }
	public MonoMac.Foundation.NSDictionary CleanAperture { get; set; }
	public System.Collections.Generic.List<VTDataRateLimit> DataRateLimits { get; set; }
	public MonoMac.CoreMedia.CMPixelFormat? Depth { get; set; }
	public double? ExpectedDuration { get; set; }
	public double? ExpectedFrameRate { get; set; }
	public VTFieldCount? FieldCount { get; set; }
	public VTFieldDetail FieldDetail { get; set; }
	public VTH264EntropyMode H264EntropyMode { get; set; }
	public MonoMac.Foundation.NSData ICCProfile { get; set; }
	public int? MaxFrameDelayCount { get; set; }
	public int? MaxH264SliceBytes { get; set; }
	public int? MaxKeyFrameInterval { get; set; }
	public double? MaxKeyFrameIntervalDuration { get; set; }
	public bool? MoreFramesAfterEnd { get; set; }
	public bool? MoreFramesBeforeStart { get; set; }
	public VTMultiPassStorage MultiPassStorage { get; set; }
	public int? NumberOfPendingFrames { get; }
	public MonoMac.Foundation.NSDictionary PixelAspectRatio { get; set; }
	public bool? PixelBufferPoolIsShared { get; }
	public MonoMac.Foundation.NSDictionary PixelTransferProperties { get; set; }
	public VTProfileLevel ProfileLevel { get; set; }
	public bool? ProgressiveScan { get; set; }
	public float? Quality { get; set; }
	public bool? RealTime { get; set; }
	public uint? SourceFrameCount { get; set; }
	public VTTransferFunction TransferFunction { get; set; }
	public bool? UsingHardwareAcceleratedVideoEncoder { get; }
	public MonoMac.Foundation.NSDictionary VideoEncoderPixelBufferAttributes { get; }
	public VTYCbCrMatrix YCbCrMatrix { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString AllowFrameReordering { get; }
	public static MonoMac.Foundation.NSString AllowTemporalCompression { get; }
	public static MonoMac.Foundation.NSString AspectRatio16x9 { get; }
	public static MonoMac.Foundation.NSString AverageBitRate { get; }
	public static MonoMac.Foundation.NSString CleanAperture { get; }
	public static MonoMac.Foundation.NSString ColorPrimaries { get; }
	public static MonoMac.Foundation.NSString DataRateLimits { get; }
	public static MonoMac.Foundation.NSString Depth { get; }
	public static MonoMac.Foundation.NSString ExpectedDuration { get; }
	public static MonoMac.Foundation.NSString ExpectedFrameRate { get; }
	public static MonoMac.Foundation.NSString FieldCount { get; }
	public static MonoMac.Foundation.NSString FieldDetail { get; }
	public static MonoMac.Foundation.NSString H264EntropyMode { get; }
	public static MonoMac.Foundation.NSString ICCProfile { get; }
	public static MonoMac.Foundation.NSString MaxFrameDelayCount { get; }
	public static MonoMac.Foundation.NSString MaxH264SliceBytes { get; }
	public static MonoMac.Foundation.NSString MaxKeyFrameInterval { get; }
	public static MonoMac.Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static MonoMac.Foundation.NSString MoreFramesAfterEnd { get; }
	public static MonoMac.Foundation.NSString MoreFramesBeforeStart { get; }
	public static MonoMac.Foundation.NSString MultiPassStorage { get; }
	public static MonoMac.Foundation.NSString NumberOfPendingFrames { get; }
	public static MonoMac.Foundation.NSString PixelAspectRatio { get; }
	public static MonoMac.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoMac.Foundation.NSString PixelTransferProperties { get; }
	public static MonoMac.Foundation.NSString ProfileLevel { get; }
	public static MonoMac.Foundation.NSString ProgressiveScan { get; }
	public static MonoMac.Foundation.NSString Quality { get; }
	public static MonoMac.Foundation.NSString RealTime { get; }
	public static MonoMac.Foundation.NSString SourceFrameCount { get; }
	public static MonoMac.Foundation.NSString TransferFunction { get; }
	public static MonoMac.Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static MonoMac.Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
	public static MonoMac.Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type MonoMac.VideoToolbox.VTCompressionSession

```
public class VTCompressionSession : MonoMac.VideoToolbox.VTSession, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTCompressionSession (IntPtr handle);
	// methods
	protected override void ~VTCompressionSession ();
	public VTStatus BeginPass (VTCompressionSessionOptionFlags flags);
	public VTStatus CompleteFrames (MonoMac.CoreMedia.CMTime completeUntilPresentationTimeStamp);
	public static VTCompressionSession Create (int width, int height, MonoMac.CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, MonoMac.Foundation.NSDictionary sourceImageBufferAttributes);
	public void Dispose ();
	protected override void Dispose (bool disposing);
	public VTStatus EncodeFrame (MonoMac.CoreVideo.CVImageBuffer imageBuffer, MonoMac.CoreMedia.CMTime presentationTimestampe, MonoMac.CoreMedia.CMTime duration, MonoMac.Foundation.NSDictionary frameProperties, IntPtr sourceFrame, out VTEncodeInfoFlags infoFlags);
	public VTStatus EndPass (out bool furtherPassesRequested);
	public VTStatus EndPassAsFinal ();
	public MonoMac.CoreVideo.CVPixelBufferPool GetPixelBufferPool ();
	public VTStatus GetTimeRangesForNextPass (out MonoMac.CoreMedia.CMTimeRange[] timeRanges);
	public VTStatus PrepareToEncodeFrames ();
	public VTStatus SetCompressionProperties (VTCompressionProperties options);

	// inner types
	public sealed delegate VTCompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTCompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, MonoMac.CoreMedia.CMSampleBuffer buffer, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, MonoMac.CoreMedia.CMSampleBuffer buffer);
	}
}
```

### New Type MonoMac.VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type MonoMac.VideoToolbox.VTDataRateLimit

```
public struct VTDataRateLimit {
	// constructors
	public VTDataRateLimit (uint numberOfBytes, double seconds);
	// properties
	public uint NumberOfBytes { get; set; }
	public double Seconds { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTDecodeFrameFlags

```
[Serializable]
[Flags]
public enum VTDecodeFrameFlags {
	DoNotOutputFrame = 2,
	EnableAsynchronousDecompression = 1,
	EnableTemporalProcessing = 8,
	OneTimeRealTimePlayback = 4,
}
```

### New Type MonoMac.VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionProperties

```
public class VTDecompressionProperties : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionProperties ();
	public VTDecompressionProperties (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? ContentHasInterframeDependencies { get; }
	public VTDeinterlaceMode DeinterlaceMode { get; set; }
	public VTFieldMode FieldMode { get; set; }
	public MonoMac.Foundation.NSDictionary MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public MonoMac.Foundation.NSDictionary MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public uint? NumberOfFramesBeingDecoded { get; }
	public VTOnlyTheseFrames OnlyTheseFrames { get; set; }
	public uint? OutputPoolRequestedMinimumBufferCount { get; set; }
	public MonoMac.CoreVideo.CVPixelBufferPool PixelBufferPool { get; }
	public bool? PixelBufferPoolIsShared { get; }
	public MonoMac.CoreMedia.CMPixelFormat[] PixelFormatsWithReducedResolutionSupport { get; }
	public MonoMac.Foundation.NSDictionary PixelTransferProperties { get; set; }
	public bool? RealTime { get; set; }
	public uint? ReducedCoefficientDecode { get; set; }
	public float? ReducedFrameDelivery { get; set; }
	public VTDecompressionResolutionOptions ReducedResolutionDecode { get; set; }
	public MonoMac.Foundation.NSDictionary[] SuggestedQualityOfServiceTiers { get; }
	public MonoMac.CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByPerformance { get; }
	public MonoMac.CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByQuality { get; }
	public uint? ThreadCount { get; set; }
	public bool? UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static MonoMac.Foundation.NSString ContentHasInterframeDependencies { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static MonoMac.Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static MonoMac.Foundation.NSString FieldMode { get; }
	public static MonoMac.Foundation.NSString FieldMode_BothFields { get; }
	public static MonoMac.Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static MonoMac.Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static MonoMac.Foundation.NSString FieldMode_SingleField { get; }
	public static MonoMac.Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static MonoMac.Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static MonoMac.Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static MonoMac.Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static MonoMac.Foundation.NSString PixelBufferPool { get; }
	public static MonoMac.Foundation.NSString PixelBufferPoolIsShared { get; }
	public static MonoMac.Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static MonoMac.Foundation.NSString PixelTransferProperties { get; }
	public static MonoMac.Foundation.NSString RealTime { get; }
	public static MonoMac.Foundation.NSString ReducedCoefficientDecode { get; }
	public static MonoMac.Foundation.NSString ReducedFrameDelivery { get; }
	public static MonoMac.Foundation.NSString ReducedResolutionDecode { get; }
	public static MonoMac.Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static MonoMac.Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static MonoMac.Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static MonoMac.Foundation.NSString ThreadCount { get; }
	public static MonoMac.Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionResolutionKeys

```
public static class VTDecompressionResolutionKeys {
	// properties
	public static MonoMac.Foundation.NSString Height { get; }
	public static MonoMac.Foundation.NSString Width { get; }
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionResolutionOptions

```
public class VTDecompressionResolutionOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionResolutionOptions ();
	public VTDecompressionResolutionOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public float? Height { get; set; }
	public float? Width { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTDecompressionSession

```
public class VTDecompressionSession : MonoMac.VideoToolbox.VTSession, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTDecompressionSession (IntPtr handle);
	// methods
	protected override void ~VTDecompressionSession ();
	public VTStatus CanAcceptFormatDescriptor (MonoMac.CoreMedia.CMFormatDescription newDescriptor);
	public VTStatus CopyBlackPixelBuffer (out MonoMac.CoreVideo.CVPixelBuffer pixelBuffer);
	public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, MonoMac.CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, MonoMac.Foundation.NSDictionary destinationImageBufferAttributes);
	public VTStatus DecodeFrame (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer, VTDecodeFrameFlags decodeFlags, IntPtr sourceFrame, out VTDecodeInfoFlags infoFlags);
	protected override void Dispose (bool disposing);
	public void Dispose ();
	public VTStatus FinishDelayedFrames ();
	public VTStatus SetDecompressionProperties (VTDecompressionProperties options);
	public VTStatus WaitForAsynchronousFrames ();

	// inner types
	public sealed delegate VTDecompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTDecompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, MonoMac.CoreVideo.CVImageBuffer buffer, MonoMac.CoreMedia.CMTime presentationTimeStamp, MonoMac.CoreMedia.CMTime presentationDuration, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, MonoMac.CoreVideo.CVImageBuffer buffer, MonoMac.CoreMedia.CMTime presentationTimeStamp, MonoMac.CoreMedia.CMTime presentationDuration);
	}
}
```

### New Type MonoMac.VideoToolbox.VTDeinterlaceMode

```
[Serializable]
public enum VTDeinterlaceMode {
	Temporal = 2,
	Unset = 0,
	VerticalFilter = 1,
}
```

### New Type MonoMac.VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static MonoMac.Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type MonoMac.VideoToolbox.VTEncodeFrameOptions

```
public class VTEncodeFrameOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTEncodeFrameOptions ();
	public VTEncodeFrameOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? ForceKeyFrame { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type MonoMac.VideoToolbox.VTFieldCount

```
[Serializable]
public enum VTFieldCount {
	Interlaced = 2,
	Progressive = 1,
}
```

### New Type MonoMac.VideoToolbox.VTFieldDetail

```
[Serializable]
public enum VTFieldDetail {
	SpatialFirstLineEarly = 3,
	SpatialFirstLineLate = 4,
	TemporalBottomFirst = 2,
	TemporalTopFirst = 1,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTFieldMode

```
[Serializable]
public enum VTFieldMode {
	BothFields = 1,
	BottomFieldOnly = 3,
	DeinterlaceFields = 5,
	SingleField = 4,
	TopFieldOnly = 2,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTFrameSilo

```
public class VTFrameSilo : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTFrameSilo (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTFrameSilo ();
	public VTStatus AddSampleBuffer (MonoMac.CoreMedia.CMSampleBuffer sampleBuffer);
	public static VTFrameSilo Create (MonoMac.Foundation.NSUrl fileUrl, MonoMac.CoreMedia.CMTimeRange? timeRange);
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public VTStatus ForEach (System.Func<MonoMac.CoreMedia.CMSampleBuffer,MonoMac.VideoToolbox.VTStatus> callback, MonoMac.CoreMedia.CMTimeRange? range);
	public VTStatus GetProgressOfCurrentPass (out float progress);
	public VTStatus SetTimeRangesForNextPass (MonoMac.CoreMedia.CMTimeRange[] ranges);
}
```

### New Type MonoMac.VideoToolbox.VTH264EntropyMode

```
[Serializable]
public enum VTH264EntropyMode {
	Cabac = 2,
	Cavlc = 1,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTH264EntropyModeKeys

```
public static class VTH264EntropyModeKeys {
	// properties
	public static MonoMac.Foundation.NSString CABAC { get; }
	public static MonoMac.Foundation.NSString CAVLC { get; }
}
```

### New Type MonoMac.VideoToolbox.VTMultiPassStorage

```
public class VTMultiPassStorage : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTMultiPassStorage (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTMultiPassStorage ();
	public VTStatus Close ();
	public static VTMultiPassStorage Create (VTMultiPassStorageCreationOptions options, MonoMac.Foundation.NSUrl fileUrl, MonoMac.CoreMedia.CMTimeRange? timeRange);
	public static VTMultiPassStorage Create (MonoMac.Foundation.NSUrl fileUrl, MonoMac.CoreMedia.CMTimeRange? timeRange, MonoMac.Foundation.NSDictionary options);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

### New Type MonoMac.VideoToolbox.VTMultiPassStorageCreationOptionKeys

```
public static class VTMultiPassStorageCreationOptionKeys {
	// properties
	public static MonoMac.Foundation.NSString DoNotDelete { get; }
}
```

### New Type MonoMac.VideoToolbox.VTMultiPassStorageCreationOptions

```
public class VTMultiPassStorageCreationOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTMultiPassStorageCreationOptions ();
	public VTMultiPassStorageCreationOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? DoNotDelete { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTOnlyTheseFrames

```
[Serializable]
public enum VTOnlyTheseFrames {
	AllFrames = 1,
	IFrames = 3,
	KeyFrames = 4,
	NonDroppableFrames = 2,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTProfileLevel

```
[Serializable]
public enum VTProfileLevel {
	H263Profile0Level10 = 46,
	H263Profile0Level45 = 47,
	H263Profile3Level45 = 48,
	H264Baseline13 = 1,
	H264Baseline30 = 2,
	H264Baseline31 = 3,
	H264Baseline32 = 4,
	H264Baseline40 = 5,
	H264Baseline41 = 6,
	H264Baseline42 = 7,
	H264Baseline50 = 8,
	H264Baseline51 = 9,
	H264Baseline52 = 10,
	H264BaselineAutoLevel = 11,
	H264Extended50 = 22,
	H264ExtendedAutoLevel = 23,
	H264High30 = 24,
	H264High31 = 25,
	H264High32 = 26,
	H264High40 = 27,
	H264High41 = 28,
	H264High42 = 29,
	H264High50 = 30,
	H264High51 = 31,
	H264High52 = 32,
	H264HighAutoLevel = 33,
	H264Main30 = 12,
	H264Main31 = 13,
	H264Main32 = 14,
	H264Main40 = 15,
	H264Main41 = 16,
	H264Main42 = 17,
	H264Main50 = 18,
	H264Main51 = 19,
	H264Main52 = 20,
	H264MainAutoLevel = 21,
	MP4VAdvancedSimpleL0 = 41,
	MP4VAdvancedSimpleL1 = 42,
	MP4VAdvancedSimpleL2 = 43,
	MP4VAdvancedSimpleL3 = 44,
	MP4VAdvancedSimpleL4 = 45,
	MP4VMainL2 = 38,
	MP4VMainL3 = 39,
	MP4VMainL4 = 40,
	MP4VSimpleL0 = 34,
	MP4VSimpleL1 = 35,
	MP4VSimpleL2 = 36,
	MP4VSimpleL3 = 37,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTProfileLevelKeys

```
public static class VTProfileLevelKeys {
	// properties
	public static MonoMac.Foundation.NSString H263_Profile0_Level10 { get; }
	public static MonoMac.Foundation.NSString H263_Profile0_Level45 { get; }
	public static MonoMac.Foundation.NSString H263_Profile3_Level45 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_1_3 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_Extended_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Extended_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_High_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_High_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_High_AutoLevel { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_3_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_4_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_0 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_1 { get; }
	public static MonoMac.Foundation.NSString H264_Main_5_2 { get; }
	public static MonoMac.Foundation.NSString H264_Main_AutoLevel { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static MonoMac.Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L3 { get; }
	public static MonoMac.Foundation.NSString MP4V_Main_L4 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L0 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L1 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L2 { get; }
	public static MonoMac.Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyKeys

```
public static class VTPropertyKeys {
	// properties
	public static MonoMac.Foundation.NSString DocumentationKey { get; }
	public static MonoMac.Foundation.NSString ReadWriteStatus { get; }
	public static MonoMac.Foundation.NSString ShouldBeSerialized { get; }
	public static MonoMac.Foundation.NSString SupportedValueListKey { get; }
	public static MonoMac.Foundation.NSString SupportedValueMaximumKey { get; }
	public static MonoMac.Foundation.NSString SupportedValueMinimumKey { get; }
	public static MonoMac.Foundation.NSString Type { get; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyOptions

```
public class VTPropertyOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTPropertyOptions ();
	public VTPropertyOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public MonoMac.Foundation.NSString Documentation { get; set; }
	public VTReadWriteStatus ReadWriteStatus { get; set; }
	public bool? ShouldBeSerialized { get; set; }
	public MonoMac.Foundation.NSNumber[] SupportedValueList { get; set; }
	public MonoMac.Foundation.NSNumber SupportedValueMaximum { get; set; }
	public MonoMac.Foundation.NSNumber SupportedValueMinimum { get; set; }
	public VTPropertyType Type { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyReadWriteStatusKeys

```
public static class VTPropertyReadWriteStatusKeys {
	// properties
	public static MonoMac.Foundation.NSString ReadOnly { get; }
	public static MonoMac.Foundation.NSString ReadWrite { get; }
}
```

### New Type MonoMac.VideoToolbox.VTPropertyType

```
[Serializable]
public enum VTPropertyType {
	Boolean = 2,
	Enumeration = 1,
	Number = 3,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTPropertyTypeKeys

```
public static class VTPropertyTypeKeys {
	// properties
	public static MonoMac.Foundation.NSString Boolean { get; }
	public static MonoMac.Foundation.NSString Enumeration { get; }
	public static MonoMac.Foundation.NSString Number { get; }
}
```

### New Type MonoMac.VideoToolbox.VTReadWriteStatus

```
[Serializable]
public enum VTReadWriteStatus {
	ReadOnly = 1,
	ReadWrite = 2,
	Unset = 0,
}
```

### New Type MonoMac.VideoToolbox.VTSession

```
public class VTSession : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTSession (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTSession ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public VTPropertyOptions GetProperties ();
	public MonoMac.Foundation.NSObject GetProperty (MonoMac.Foundation.NSString propertyKey);
	public MonoMac.Foundation.NSDictionary GetSerializableProperties ();
	public MonoMac.Foundation.NSDictionary GetSupportedProperties ();
	public VTStatus SetProperties (VTPropertyOptions options);
	public VTStatus SetProperty (MonoMac.Foundation.NSString propertyKey, MonoMac.Foundation.NSObject value);
}
```

### New Type MonoMac.VideoToolbox.VTStatus

```
[Serializable]
public enum VTStatus {
	AllocationFailed = -12904,
	ColorCorrectionPixelTransferFailed = -12212,
	ColorSyncTransformConvertFailed = -12919,
	CouldNotCreateColorCorrectionData = -12918,
	CouldNotCreateInstance = -12907,
	CouldNotFindTemporalFilter = -12217,
	CouldNotFindVideoDecoder = -12906,
	CouldNotFindVideoEncoder = -12908,
	FormatDescriptionChangeNotSupported = -12916,
	FrameSiloInvalidTimeRange = -12216,
	FrameSiloInvalidTimeStamp = -12215,
	ImageRotationNotSupported = -12914,
	InsufficientSourceColorData = -12917,
	InvalidSession = -12903,
	MultiPassStorageIdentifierMismatch = -12913,
	MultiPassStorageInvalid = -12214,
	Ok = 0,
	Parameter = -12902,
	PixelTransferNotPermitted = -12218,
	PixelTransferNotSupported = -12905,
	PropertyNotSupported = -12900,
	PropertyReadOnly = -12901,
	VideoDecoderAuthorization = -12210,
	VideoDecoderBadData = -12909,
	VideoDecoderMalfunction = -12911,
	VideoDecoderNotAvailableNow = -12913,
	VideoDecoderUnsupportedDataFormat = -12910,
	VideoEncoderAuthorization = -12211,
	VideoEncoderMalfunction = -12912,
	VideoEncoderNotAvailableNow = -12915,
}
```

### New Type MonoMac.VideoToolbox.VTTransferFunction

```
[Serializable]
public enum VTTransferFunction {
	ItuR7092 = 1,
	Smpte240M1955 = 2,
	Unset = 0,
	UseGamma = 3,
}
```

### New Type MonoMac.VideoToolbox.VTVideoDecoderSpecification

```
public class VTVideoDecoderSpecification : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTVideoDecoderSpecification ();
	public VTVideoDecoderSpecification (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoDecoder { get; set; }
	public bool? RequireHardwareAcceleratedVideoDecoder { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTVideoDecoderSpecificationKeys

```
public static class VTVideoDecoderSpecificationKeys {
	// properties
	public static MonoMac.Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static MonoMac.Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type MonoMac.VideoToolbox.VTVideoEncoder

```
public class VTVideoEncoder {
	// properties
	public string CodecName { get; }
	public int CodecType { get; }
	public string DisplayName { get; }
	public string EncoderId { get; }
	public string EncoderName { get; }
	// methods
	public static VTVideoEncoder[] GetEncoderList ();
}
```

### New Type MonoMac.VideoToolbox.VTVideoEncoderSpecification

```
public class VTVideoEncoderSpecification : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTVideoEncoderSpecification ();
	public VTVideoEncoderSpecification (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoEncoder { get; set; }
	public string EncoderID { get; set; }
	public bool? RequireHardwareAcceleratedVideoEncoder { get; set; }
}
```

### New Type MonoMac.VideoToolbox.VTVideoEncoderSpecificationKeys

```
public static class VTVideoEncoderSpecificationKeys {
	// properties
	public static MonoMac.Foundation.NSString EnableHardwareAcceleratedVideoEncoder { get; }
	public static MonoMac.Foundation.NSString EncoderID { get; }
	public static MonoMac.Foundation.NSString RequireHardwareAcceleratedVideoEncoder { get; }
}
```

### New Type MonoMac.VideoToolbox.VTYCbCrMatrix

```
[Serializable]
public enum VTYCbCrMatrix {
	ItuR6014 = 2,
	ItuR7092 = 1,
	Smpte240M1955 = 3,
	Unset = 0,
}
```
