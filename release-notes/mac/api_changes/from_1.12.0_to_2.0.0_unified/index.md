---
id: 4FEF24BC-AF7B-4CA7-86F2-1C9A4364243F
title: "From 1.12.0 to 2.0.0 unified"
---

# Xamarin.Mac.dll

## Namespace Accounts

### Type Changed: Accounts.ACErrorCode

Obsoleted fields:

```
[Obsolete ("Use MissingTransportMessageId"]
	MissingMessageID = 21,
```

Added value:

```
MissingTransportMessageId = 21,
```

## Namespace AppKit

### Type Changed: AppKit.NSAlert

Modified properties:

```
public virtual NSAlertDelegate INSAlertDelegate Delegate { get; set; }
```

Added property:

```
public virtual Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: AppKit.NSAnimation

Modified properties:

```
public virtual NSAnimationDelegate INSAnimationDelegate Delegate { get; set; }
```

Added property:

```
public virtual Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: AppKit.NSApplication

Added field:

```
public static bool CheckForEventAndDelegateMismatches;
```

Modified properties:

```
public NSApplicationDelegate INSApplicationDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSBrowser

Modified properties:

```
public NSBrowserDelegate INSBrowserDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSBrowserDelegate

Removed method:

```
public virtual NSDragOperation ValidateDrop (NSBrowser browser, NSDraggingInfo info, ref nint row, ref nint column, NSBrowserDropOperation dropOperation);
```

Added method:

```
public virtual NSDragOperation ValidateDrop (NSBrowser browser, NSDraggingInfo info, ref nint row, ref nint column, ref NSBrowserDropOperation dropOperation);
```

### Type Changed: AppKit.NSBrowserDelegate_Extensions

Removed method:

```
public static NSDragOperation ValidateDrop (INSBrowserDelegate This, NSBrowser browser, NSDraggingInfo info, ref nint row, ref nint column, NSBrowserDropOperation dropOperation);
```

Added method:

```
public static NSDragOperation ValidateDrop (INSBrowserDelegate This, NSBrowser browser, NSDraggingInfo info, ref nint row, ref nint column, ref NSBrowserDropOperation dropOperation);
```

### Type Changed: AppKit.NSCollectionView

Modified properties:

```
public NSCollectionViewDelegate INSCollectionViewDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSCollectionViewDelegate

Removed methods:

```
public virtual NSPasteboardWriting PasteboardWriterForItemAtIndex (NSCollectionView collectionView, uint index);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref nint dropIndex, NSCollectionViewDropOperation dropOperation);
```

Added methods:

```
public virtual INSPasteboardWriting PasteboardWriterForItem (NSCollectionView collectionView, uint index);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref nint dropIndex, ref NSCollectionViewDropOperation dropOperation);
```

### Type Changed: AppKit.NSCollectionViewDelegate_Extensions

Removed methods:

```
public static NSPasteboardWriting PasteboardWriterForItemAtIndex (INSCollectionViewDelegate This, NSCollectionView collectionView, uint index);
	public static NSDragOperation ValidateDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref nint dropIndex, NSCollectionViewDropOperation dropOperation);
```

Added methods:

```
public static INSPasteboardWriting PasteboardWriterForItem (INSCollectionViewDelegate This, NSCollectionView collectionView, uint index);
	public static NSDragOperation ValidateDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref nint dropIndex, ref NSCollectionViewDropOperation dropOperation);
```

### Type Changed: AppKit.NSComboBox

Modified properties:

```
public virtual NSComboBoxDataSource INSComboBoxDataSource DataSource { get; set; }
	public NSComboBoxDelegate INSComboBoxDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSComboBoxCell

Modified properties:

```
public virtual NSComboBoxCellDataSource INSComboBoxCellDataSource DataSource { get; set; }
```

### Type Changed: AppKit.NSDatePicker

Modified properties:

```
public NSDatePickerCellDelegate INSDatePickerCellDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSDatePickerCell

Modified properties:

```
public NSDatePickerCellDelegate INSDatePickerCellDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSDrawer

Modified properties:

```
public NSDrawerDelegate INSDrawerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSEventPhase

Added value:

```
MayBegin = 32,
```

### Type Changed: AppKit.NSGestureRecognizer

Modified properties:

```
public NSGestureRecognizerDelegate INSGestureRecognizerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSImage

Modified properties:

```
public NSImageDelegate INSImageDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSKey

Removed values:

```
Begin = 63274,
	Break = 63282,
	ClearDisplay = 63290,
	ClearLine = 63289,
	DeleteChar = 63294,
	DeleteLine = 63292,
	Execute = 63298,
	F17 = 63252,
	F21 = 63256,
	F22 = 63257,
	F23 = 63258,
	F24 = 63259,
	F25 = 63260,
	F26 = 63261,
	F27 = 63262,
	F28 = 63263,
	F29 = 63264,
	F30 = 63265,
	F31 = 63266,
	F32 = 63267,
	F33 = 63268,
	F34 = 63269,
	F35 = 63270,
	Find = 63301,
	Insert = 63271,
	InsertChar = 63293,
	InsertLine = 63291,
	Menu = 63285,
	ModeSwitch = 63303,
	Next = 63296,
	Pause = 63280,
	Prev = 63295,
	Print = 63288,
	PrintScreen = 63278,
	Redo = 63300,
	Reset = 63283,
	ScrollLock = 63279,
	Select = 63297,
	Stop = 63284,
	SysReq = 63281,
	System = 63287,
	Undo = 63299,
	User = 63286,
```

Modified fields:

```
DownArrow = 63233 125
	End = 63275 119
	F1 = 63236 122
	F10 = 63245 109
	F11 = 63246 103
	F12 = 63247 111
	F13 = 63248 105
	F14 = 63249 107
	F15 = 63250 113
	F16 = 63251 106
	F18 = 63253 79
	F19 = 63254 80
	F2 = 63237 120
	F20 = 63255 90
	F3 = 63238 99
	F4 = 63239 118
	F5 = 63240 96
	F6 = 63241 97
	F7 = 63242 98
	F8 = 63243 100
	F9 = 63244 101
	Help = 63302 114
	Home = 63273 115
	LeftArrow = 63234 123
	PageDown = 63277 121
	PageUp = 63276 116
	RightArrow = 63235 124
	UpArrow = 63232 126
```

Added values:

```
ISOSection = 10,
	JISEisu = 102,
	JISKana = 104,
	JISKeypadComma = 95,
	JISUnderscore = 94,
	JISYen = 93,
```

### Type Changed: AppKit.NSLayoutManager

Modified properties:

```
public NSLayoutManagerDelegate INSLayoutManagerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSMatrix

Modified properties:

```
public NSMatrixDelegate INSMatrixDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSMenu

Modified properties:

```
public NSMenuDelegate INSMenuDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSModalResponse

Added values:

```
Cancel = 0,
	OK = 1,
```

### Type Changed: AppKit.NSObjectController

Modified properties:

```
public virtual NSObjectController Foundation.NSObject NewObject { get; }
```

### Type Changed: AppKit.NSOutlineView

Modified properties:

```
public NSOutlineViewDataSource INSOutlineViewDataSource DataSource { get; set; }
	public NSOutlineViewDelegate INSOutlineViewDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSOutlineViewDataSource

Removed method:

```
public virtual NSPasteboardWriting PasteboardWriterForItem (NSOutlineView outlineView, Foundation.NSObject item);
```

Added method:

```
public virtual INSPasteboardWriting PasteboardWriterForItem (NSOutlineView outlineView, Foundation.NSObject item);
```

### Type Changed: AppKit.NSOutlineViewDataSource_Extensions

Removed method:

```
public static NSPasteboardWriting PasteboardWriterForItem (INSOutlineViewDataSource This, NSOutlineView outlineView, Foundation.NSObject item);
```

Added method:

```
public static INSPasteboardWriting PasteboardWriterForItem (INSOutlineViewDataSource This, NSOutlineView outlineView, Foundation.NSObject item);
```

### Type Changed: AppKit.NSPageController

Modified properties:

```
public NSPageControllerDelegate INSPageControllerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSPasteboardItem

Removed method:

```
public virtual bool SetDataProviderForTypes (NSPasteboardItemDataProvider dataProvider, string[] types);
```

Added method:

```
public virtual bool SetDataProviderForTypes (INSPasteboardItemDataProvider dataProvider, string[] types);
```

### Type Changed: AppKit.NSPathCell

Modified properties:

```
public NSPathCellDelegate INSPathCellDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSPathControl

Modified properties:

```
public NSPathControlDelegate INSPathControlDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSPopover

Modified properties:

```
public NSPopoverDelegate INSPopoverDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSRuleEditor

Modified properties:

```
public NSRuleEditorDelegate INSRuleEditorDelegate Delegate { get; set; }
	public virtual NSRuleEditorDelegate Foundation.NSObject WeakDelegate { get; set; }
```

### Type Changed: AppKit.NSSavePanel

Modified properties:

```
public NSOpenSavePanelDelegate INSOpenSavePanelDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSharingService

Modified properties:

```
public NSSharingServiceDelegate INSSharingServiceDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSharingServicePicker

Modified properties:

```
public NSSharingServicePickerDelegate INSSharingServicePickerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSharingServicePickerDelegate

Removed method:

```
public virtual NSSharingServiceDelegate DelegateForSharingService (NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

Added method:

```
public virtual INSSharingServiceDelegate DelegateForSharingService (NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

### Type Changed: AppKit.NSSharingServicePickerDelegate_Extensions

Removed method:

```
public static NSSharingServiceDelegate DelegateForSharingService (INSSharingServicePickerDelegate This, NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

Added method:

```
public static INSSharingServiceDelegate DelegateForSharingService (INSSharingServicePickerDelegate This, NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

### Type Changed: AppKit.NSSharingServicePickerDelegateForSharingService

Removed methods:

```
public virtual NSSharingServiceDelegate EndInvoke (System.IAsyncResult result);
	public virtual NSSharingServiceDelegate Invoke (NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

Added methods:

```
public virtual INSSharingServiceDelegate EndInvoke (System.IAsyncResult result);
	public virtual INSSharingServiceDelegate Invoke (NSSharingServicePicker sharingServicePicker, NSSharingService sharingService);
```

### Type Changed: AppKit.NSSound

Modified properties:

```
public NSSoundDelegate INSSoundDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSpeechRecognizer

Modified properties:

```
public NSSpeechRecognizerDelegate INSSpeechRecognizerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSpeechSynthesizer

Modified properties:

```
public NSSpeechSynthesizerDelegate INSSpeechSynthesizerDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSSplitView

Modified properties:

```
public NSSplitViewDelegate INSSplitViewDelegate Delegate { get; set; }
```

Removed method:

```
public virtual float HoldingPriorityForSubviewAtIndex (nint subviewIndex);
```

Added method:

```
public virtual float HoldingPriorityForSubview (nint subviewIndex);
```

### Type Changed: AppKit.NSStackView

Modified properties:

```
public NSStackViewDelegate INSStackViewDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSStringDrawing

Added methods:

```
public static void DrawAtPoint (string This, CoreGraphics.CGPoint point, NSStringAttributes attributes);
	public static void DrawInRect (string This, CoreGraphics.CGRect rect, NSStringAttributes attributes);
	public static CoreGraphics.CGSize StringSize (string This, NSStringAttributes attributes);
```

### Type Changed: AppKit.NSStringDrawing_NSString

Added methods:

```
public static void DrawAtPoint (Foundation.NSString This, CoreGraphics.CGPoint point, NSStringAttributes attributes);
	public static void DrawInRect (Foundation.NSString This, CoreGraphics.CGRect rect, NSStringAttributes attributes);
	public static CoreGraphics.CGSize StringSize (Foundation.NSString This, NSStringAttributes attributes);
```

### Type Changed: AppKit.NSTableView

Modified properties:

```
public NSTableViewDataSource INSTableViewDataSource DataSource { get; set; }
	public NSTableViewDelegate INSTableViewDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSTableViewDataSource

Removed method:

```
public virtual NSPasteboardWriting GetPasteboardWriterForRow (NSTableView tableView, nint row);
```

Added method:

```
public virtual INSPasteboardWriting GetPasteboardWriterForRow (NSTableView tableView, nint row);
```

### Type Changed: AppKit.NSTableViewDataSource_Extensions

Removed method:

```
public static NSPasteboardWriting GetPasteboardWriterForRow (INSTableViewDataSource This, NSTableView tableView, nint row);
```

Added method:

```
public static INSPasteboardWriting GetPasteboardWriterForRow (INSTableViewDataSource This, NSTableView tableView, nint row);
```

### Type Changed: AppKit.NSTableViewSource

Removed method:

```
public virtual NSPasteboardWriting GetPasteboardWriterForRow (NSTableView tableView, nint row);
```

Added method:

```
public virtual INSPasteboardWriting GetPasteboardWriterForRow (NSTableView tableView, nint row);
```

### Type Changed: AppKit.NSTableViewSource_Extensions

Removed method:

```
public static NSPasteboardWriting GetPasteboardWriterForRow (INSTableViewSource This, NSTableView tableView, nint row);
```

Added method:

```
public static INSPasteboardWriting GetPasteboardWriterForRow (INSTableViewSource This, NSTableView tableView, nint row);
```

### Type Changed: AppKit.NSTabView

Modified properties:

```
public virtual NSTabViewDelegate INSTabViewDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSText

Modified properties:

```
public NSTextDelegate INSTextDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSTextField

Modified properties:

```
public NSTextFieldDelegate INSTextFieldDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSTextFinder

Modified properties:

```
public virtual NSTextFinderClient INSTextFinderClient Client { set; }
	public virtual NSTextFinderBarContainer INSTextFinderBarContainer FindBarContainer { set; }
```

### Type Changed: AppKit.NSTextFinderBarContainer

Added property:

```
public virtual NSView ContentView { get; }
```

### Type Changed: AppKit.NSTextStorage

Added constructors:

```
public NSTextStorage (Foundation.NSAttributedString other);
	public NSTextStorage (string str, Foundation.NSDictionary attributes);
	public NSTextStorage (string str, CoreText.CTStringAttributes attributes);
```

Modified properties:

```
public NSTextStorageDelegate INSTextStorageDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSTextView

Modified properties:

```
public NSTextViewDelegate INSTextViewDelegate Delegate { get; set; }
```

Added method:

```
public virtual void ToggleQuickLookPreviewPanel (Foundation.NSObject sender);
```

### Type Changed: AppKit.NSTokenField

Modified properties:

```
public NSTokenFieldDelegate INSTokenFieldDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSToolbar

Modified properties:

```
public NSToolbarDelegate INSToolbarDelegate Delegate { get; set; }
```

### Type Changed: AppKit.NSView

Removed method:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes, NSEvent evnt, NSDraggingSource source);
```

Added method:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes, NSEvent evnt, INSDraggingSource source);
```

### Type Changed: AppKit.NSViewController

Removed method:

```
public virtual void PresentViewController (NSViewController viewController, NSViewControllerPresentationAnimator animator);
```

Added method:

```
public virtual void PresentViewController (NSViewController viewController, INSViewControllerPresentationAnimator animator);
```

### Type Changed: AppKit.NSWindow

Modified properties:

```
public NSWindowDelegate INSWindowDelegate Delegate { get; set; }
```

### New Type AppKit.NSCoderAppKitAddons

```
public static class NSCoderAppKitAddons {
	// methods
	public static NSColor DecodeNXColor (Foundation.NSCoder This);
}
```

### New Type AppKit.NSFunctionKey

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

### New Type AppKit.NSMutableAttributedStringAppKitAddons

```
public static class NSMutableAttributedStringAppKitAddons {
	// methods
	public static void ApplyFontTraits (Foundation.NSMutableAttributedString This, NSFontTraitMask traitMask, Foundation.NSRange range);
	public static void FixAttachmentAttributeInRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static void FixFontAttributeInRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static void FixParagraphStyleAttributeInRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static bool ReadFromData (Foundation.NSMutableAttributedString This, Foundation.NSData data, Foundation.NSAttributedStringDocumentAttributes options, out Foundation.NSDictionary returnOptions);
	public static bool ReadFromData (Foundation.NSMutableAttributedString This, Foundation.NSData data, Foundation.NSDictionary options, out Foundation.NSDictionary dict);
	public static bool ReadFromData (Foundation.NSMutableAttributedString This, Foundation.NSData data, Foundation.NSAttributedStringDocumentAttributes options, out Foundation.NSDictionary returnOptions, out Foundation.NSError error);
	public static bool ReadFromData (Foundation.NSMutableAttributedString This, Foundation.NSData data, Foundation.NSDictionary options, out Foundation.NSDictionary returnOptions, out Foundation.NSError error);
	public static bool ReadFromURL (Foundation.NSMutableAttributedString This, Foundation.NSUrl url, Foundation.NSAttributedStringDocumentAttributes options, out Foundation.NSDictionary returnOptions);
	public static bool ReadFromURL (Foundation.NSMutableAttributedString This, Foundation.NSUrl url, Foundation.NSDictionary options, out Foundation.NSDictionary returnOptions);
	public static bool ReadFromURL (Foundation.NSMutableAttributedString This, Foundation.NSUrl url, Foundation.NSAttributedStringDocumentAttributes options, out Foundation.NSDictionary returnOptions, out Foundation.NSError error);
	public static bool ReadFromURL (Foundation.NSMutableAttributedString This, Foundation.NSUrl url, Foundation.NSDictionary options, out Foundation.NSDictionary returnOptions, out Foundation.NSError error);
	public static void SetAlignment (Foundation.NSMutableAttributedString This, NSTextAlignment alignment, Foundation.NSRange range);
	public static void SetBaseWritingDirection (Foundation.NSMutableAttributedString This, NSWritingDirection writingDirection, Foundation.NSRange range);
	public static void SubscriptRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static void SuperscriptRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static void UnscriptRange (Foundation.NSMutableAttributedString This, Foundation.NSRange range);
	public static void UpdateAttachmentsFromPath (Foundation.NSMutableAttributedString This, string path);
}
```

### New Type AppKit.NSStringAttributeKey

```
public static class NSStringAttributeKey {
	// properties
	public static Foundation.NSString Attachment { get; }
	public static Foundation.NSString BackgroundColor { get; }
	public static Foundation.NSString BaselineOffset { get; }
	public static Foundation.NSString CharacterShape { get; }
	public static Foundation.NSString Cursor { get; }
	public static Foundation.NSString Expansion { get; }
	public static Foundation.NSString Font { get; }
	public static Foundation.NSString ForegroundColor { get; }
	public static Foundation.NSString GlyphInfo { get; }
	public static Foundation.NSString KerningAdjustment { get; }
	public static Foundation.NSString Ligature { get; }
	public static Foundation.NSString Link { get; }
	public static Foundation.NSString MarkedClauseSegment { get; }
	public static Foundation.NSString Obliqueness { get; }
	public static Foundation.NSString ParagraphStyle { get; }
	public static Foundation.NSString Shadow { get; }
	public static Foundation.NSString SpellingState { get; }
	public static Foundation.NSString StrikethroughColor { get; }
	public static Foundation.NSString StrikethroughStyle { get; }
	public static Foundation.NSString StrokeColor { get; }
	public static Foundation.NSString StrokeWidth { get; }
	public static Foundation.NSString Superscript { get; }
	public static Foundation.NSString TextAlternatives { get; }
	public static Foundation.NSString TextEffect { get; }
	public static Foundation.NSString ToolTip { get; }
	public static Foundation.NSString UnderlineColor { get; }
	public static Foundation.NSString UnderlineStyle { get; }
	public static Foundation.NSString VerticalGlyphForm { get; }
	public static Foundation.NSString WritingDirection { get; }
}
```

### New Type AppKit.NSTextFinderBarContainer_Extensions

```
public static class NSTextFinderBarContainer_Extensions {
	// methods
	public static NSView GetContentView (INSTextFinderBarContainer This);
}
```

## Namespace AudioToolbox

### Type Changed: AudioToolbox.AudioConverterError

Added value:

```
AudioFormatUnsupported = 560226676,
```

### Removed Type AudioToolbox.AccessoryInfo ### Removed Type AudioToolbox.AudioSession ### Removed Type AudioToolbox.AudioSessionException ### Removed Type AudioToolbox.AudioSessionPropertyEventArgs ### Removed Type AudioToolbox.AudioSessionRouteChangeEventArgs ### Removed Type AudioToolbox.InputSourceInfo 



## Namespace AVFoundation



### Type Changed: AVFoundation.AVCaptureAudioFileOutput

Removed method:

```
public virtual void StartRecording (Foundation.NSUrl outputFileUrl, string fileType, AVCaptureFileOutputRecordingDelegate recordingDelegate);
```

Added method:

```
public virtual void StartRecording (Foundation.NSUrl outputFileUrl, string fileType, IAVCaptureFileOutputRecordingDelegate recordingDelegate);
```

### Type Changed: AVFoundation.AVCaptureConnection

Obsoleted properties:

```
[Obsolete ("Use AvailableAudioChannels property instead."]
	public virtual AVCaptureAudioChannel AudioChannels { get; }
```

Added property:

```
public virtual AVCaptureAudioChannel[] AvailableAudioChannels { get; }
```

### Type Changed: AVFoundation.AVError

Added values:

```
AirPlayControllerRequiresInternet = -11856,
	AirPlayReceiverRequiresInternet = -11857,
```

## Namespace CoreAnimation



### Type Changed: CoreAnimation.CABasicAnimation

Added methods:

```
public T GetByAs<T> ();
	public T GetFromAs<T> ();
	public T GetToAs<T> ();
	public void SetBy (ObjCRuntime.INativeObject value);
	public void SetFrom (ObjCRuntime.INativeObject value);
	public void SetTo (ObjCRuntime.INativeObject value);
```

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Added methods:

```
public T[] GetValuesAs<T> ();
	public void SetValues (ObjCRuntime.INativeObject[] value);
```

### Type Changed: CoreAnimation.CALayer

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
	public void SetContents (Foundation.NSObject value);
```

## Namespace CoreBluetooth



### Type Changed: CoreBluetooth.CBUUID

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
```

## Namespace CoreFoundation



### Type Changed: CoreFoundation.CFStream

Added method:

```
public static CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (CoreServices.CFHTTPMessage request, Foundation.NSInputStream body);
```

### Type Changed: CoreFoundation.DispatchQueue

Added constructor:

```
public DispatchQueue (string label, bool concurrent);
```

Added methods:

```
public void DispatchBarrierAsync (System.Action action);
	public void Submit (System.Action<int> action, long times);
```

### New Type CoreFoundation.CFNotificationCenter

```
public class CFNotificationCenter : ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public static CFNotificationCenter Darwin { get; }
	public static CFNotificationCenter Distributed { get; }
	public virtual IntPtr Handle { get; }
	public static CFNotificationCenter Local { get; }
	// methods
	protected override void ~CFNotificationCenter ();
	public CFNotificationObserverToken AddObserver (string name, ObjCRuntime.INativeObject objectToObserve, System.Action<System.String,Foundation.NSDictionary> notificationHandler, CFNotificationSuspensionBehavior suspensionBehavior);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public void PostNotification (string notification, ObjCRuntime.INativeObject objectToObserve, Foundation.NSDictionary userInfo, bool deliverImmediately, bool postOnAllSessions);
	public void RemoveEveryObserver ();
	public void RemoveObserver (CFNotificationObserverToken token);
}
```

### New Type CoreFoundation.CFNotificationObserverToken

```
public class CFNotificationObserverToken {
}
```

### New Type CoreFoundation.CFNotificationSuspensionBehavior

```
[Serializable]
public enum CFNotificationSuspensionBehavior {
	Coalesce = 2,
	DeliverImmediately = 4,
	Drop = 1,
	Hold = 3,
}
```

### New Type CoreFoundation.DispatchSource

```
public class DispatchSource : CoreFoundation.DispatchObject, ObjCRuntime.INativeObject, System.IDisposable {
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
	public class Data : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public IntPtr PendingData { get; }
		// methods
		public void MergeData (IntPtr value);
	}
	public class DataAdd : CoreFoundation.DispatchSource+Data, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class DataOr : CoreFoundation.DispatchSource+Data, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
	}
	public class Mach : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// properties
		public int MachPort { get; }
	}
	public class MachSend : CoreFoundation.DispatchSource+Mach, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, bool sendDead, DispatchQueue queue);
		// properties
		public bool SendRightsDestroyed { get; }
	}
	public class MachReceive : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int machPort, DispatchQueue queue);
	}
	public class MemoryPressure : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (MemoryPressureFlags monitorFlags, DispatchQueue queue);
		// properties
		public MemoryPressureFlags PressureFlags { get; }
	}
	public class ProcessMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int processId, ProcessMonitorFlags monitorKind, DispatchQueue queue);
		// properties
		public ProcessMonitorFlags MonitorFlags { get; }
		public int ProcessId { get; }
	}
	public class ReadMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int fileDescriptor, DispatchQueue queue);
		// properties
		public int BytesAvailable { get; }
		public int FileDescriptor { get; }
	}
	public class SignalMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (int signalNumber, DispatchQueue queue);
		// properties
		public int SignalNumber { get; }
		public int SignalsDelivered { get; }
	}
	public class Timer : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
		// constructors
		public DispatchSource (IntPtr handle, bool owns);
		public DispatchSource (IntPtr handle);
		public DispatchSource (DispatchQueue queue);
		// properties
		public int TimerFiredCount { get; }
		// methods
		public void SetTimer (DispatchTime time, long nanosecondInterval, long nanosecondLeeway);
	}
	public class VnodeMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
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
	public class WriteMonitor : CoreFoundation.DispatchSource, ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type CoreFoundation.MemoryPressureFlags

```
[Serializable]
[Flags]
public enum MemoryPressureFlags {
	Critical = 4,
	Normal = 1,
	Warn = 2,
}
```

### New Type CoreFoundation.ProcessMonitorFlags

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

### New Type CoreFoundation.VnodeMonitorKind

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

## Namespace CoreGraphics

### Type Changed: CoreGraphics.CGBitmapContext

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: CoreGraphics.CGGradientDrawingOptions

Added value:

```
None = 0,
```

### Type Changed: CoreGraphics.CGPoint

Added constructor:

```
public CGPoint (double x, double y);
```

### Type Changed: CoreGraphics.CGRect

Added constructor:

```
public CGRect (double x, double y, double width, double height);
```

### Type Changed: CoreGraphics.CGSize

Added constructor:

```
public CGSize (double width, double height);
```

## Namespace CoreImage

### Type Changed: CoreImage.CIColor

Added constructor:

```
public CIColor (AppKit.NSColor color);
```

## Namespace CoreMedia

### Type Changed: CoreMedia.CMClock

Removed method:

```
public static CMClock CreateAudioClock (out CMClockError clockError);
```

### Type Changed: CoreMedia.CMTimeRange

Added fields:

```
public static CMTimeRange Invalid;
	public static CMTimeRange Zero;
```

### New Type CoreMedia.CMPixelFormat

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

## Namespace CoreVideo

### Type Changed: CoreVideo.CVImageBuffer

Added properties:

```
public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }
	public static Foundation.NSString ColorPrimaries_P22 { get; }
	public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }
	public static Foundation.NSString ColorPrimariesKey { get; }
```

### Type Changed: CoreVideo.CVPixelBufferPool

Added properties:

```
public static Foundation.NSString ColorPrimaries_EBU_3213 { get; }
	public static Foundation.NSString ColorPrimaries_ITU_R_709_2 { get; }
	public static Foundation.NSString ColorPrimaries_P22 { get; }
	public static Foundation.NSString ColorPrimaries_SMPTE_C { get; }
	public static Foundation.NSString ColorPrimariesKey { get; }
```

### New Type CoreVideo.CVDisplayLink

```
public class CVDisplayLink : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CVDisplayLink (IntPtr handle);
	public CVDisplayLink ();
	// properties
	public double ActualOutputVideoRefreshPeriod { get; }
	public virtual IntPtr Handle { get; }
	public bool IsRunning { get; }
	public CVTime NominalOutputVideoRefreshPeriod { get; }
	public CVTime OutputVideoLatency { get; }
	// methods
	protected override void ~CVDisplayLink ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public int GetCurrentDisplay ();
	public CVReturn GetCurrentTime (out CVTimeStamp outTime);
	public CVReturn SetCurrentDisplay (OpenGL.CGLContext cglContext, OpenGL.CGLPixelFormat cglPixelFormat);
	public CVReturn SetCurrentDisplay (int displayId);
	public CVReturn SetOutputCallback (CVDisplayLink.DisplayLinkOutputCallback callback);
	public CVReturn Start ();
	public CVReturn Stop ();

	// inner types
	public sealed delegate DisplayLinkOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public CVDisplayLink (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (CVDisplayLink displayLink, ref CVTimeStamp inNow, ref CVTimeStamp inOutputTime, CVOptionFlags flagsIn, ref CVOptionFlags flagsOut, System.AsyncCallback callback, object object);
		public virtual CVReturn EndInvoke (ref CVTimeStamp inNow, ref CVTimeStamp inOutputTime, ref CVOptionFlags flagsOut, System.IAsyncResult result);
		public virtual CVReturn Invoke (CVDisplayLink displayLink, ref CVTimeStamp inNow, ref CVTimeStamp inOutputTime, CVOptionFlags flagsIn, ref CVOptionFlags flagsOut);
	}
}
```

## Namespace Foundation

### Type Changed: Foundation.NSAppleScript

Added property:

```
public virtual NSAttributedString RichTextSource { get; }
```

Added method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: Foundation.NSArray

Added method:

```
public static T[] FromArrayNative<T> (NSArray weakArray);
```

### Type Changed: Foundation.NSAttributedString

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

Removed properties:

```
public static NSString AttachmentAttributeName { get; }
	public static NSString BackgroundColorAttributeName { get; }
	public static NSString BaselineOffsetAttributeName { get; }
	public static NSString CharacterShapeAttributeName { get; }
	public static NSString CursorAttributeName { get; }
	public static NSString ExpansionAttributeName { get; }
	public static NSString FontAttributeName { get; }
	public static NSString ForegroundColorAttributeName { get; }
	public static NSString GlyphInfoAttributeName { get; }
	public static NSString KernAttributeName { get; }
	public static NSString LigatureAttributeName { get; }
	public static NSString LinkAttributeName { get; }
	public static NSString MarkedClauseSegmentAttributeName { get; }
	public static NSString ObliquenessAttributeName { get; }
	public static NSString ParagraphStyleAttributeName { get; }
	public static NSString ShadowAttributeName { get; }
	public static NSString SpellingStateAttributeName { get; }
	public static NSString StrikethroughColorAttributeName { get; }
	public static NSString StrikethroughStyleAttributeName { get; }
	public static NSString StrokeColorAttributeName { get; }
	public static NSString StrokeWidthAttributeName { get; }
	public static NSString SuperscriptAttributeName { get; }
	public static NSString TextAlternativesAttributeName { get; }
	public static NSString ToolTipAttributeName { get; }
	public static NSString UnderlineColorAttributeName { get; }
	public static NSString UnderlineStyleAttributeName { get; }
	public static NSString VerticalGlyphFormAttributeName { get; }
	public static NSString WritingDirectionAttributeName { get; }
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
	public virtual nint GetItemNumber (AppKit.NSTextList textList, uint index);
	public virtual uint GetLineBreak (uint beforeIndex, NSRange aRange);
	public virtual uint GetLineBreakByHyphenating (uint beforeIndex, NSRange aRange);
	public virtual uint GetNextWord (uint fromIndex, bool isForward);
	public virtual NSRange GetRange (AppKit.NSTextTable textTable, uint index);
	public virtual NSRange GetRange (AppKit.NSTextBlock textBlock, uint index);
	public virtual NSRange GetRange (AppKit.NSTextList textList, uint index);
	public virtual NSData GetRtf (NSRange range, NSDictionary options);
	public NSData GetRtf (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSData GetRtfd (NSRange range, NSDictionary options);
	public NSData GetRtfd (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSFileWrapper GetRtfdFileWrapper (NSRange range, NSDictionary options);
	public NSFileWrapper GetRtfdFileWrapper (NSRange range, NSAttributedStringDocumentAttributes options);
	public virtual NSDictionary GetRulerAttributes (NSRange range);
	public virtual NSUrl GetUrl (uint index, out NSRange effectiveRange);
```

### Type Changed: Foundation.NSBundle

Added methods:

```
public virtual NSAttributedString GetContextHelp (string key);
	public virtual NSUrl GetUrlForImageResource (string resource);
```

### Type Changed: Foundation.NSConnection

Modified properties:

```
public NSConnectionDelegate INSConnectionDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSFileManager

Added method:

```
public NSUrl[] GetMountedVolumes (NSString[] properties, NSVolumeEnumerationOptions options);
```

### Type Changed: Foundation.NSFileWrapper

Added property:

```
public virtual AppKit.NSImage Icon { get; set; }
```

### Type Changed: Foundation.NSIndexSet

Added constructor:

```
public NSIndexSet (nint value);
```

### Type Changed: Foundation.NSStream

Added methods:

```
public static void CreateBoundPair (out NSInputStream readStream, out NSOutputStream writeStream, nint bufferSize);
	public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocket (CoreFoundation.CFSocket socket, out NSInputStream readStream, out NSOutputStream writeStream);
	public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out NSInputStream readStream, out NSOutputStream writeStream);
```

### Type Changed: Foundation.NSTextCheckingResult

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
	public virtual NSTextCheckingResult ResultByAdjustingRanges (nint offset);
	public static NSTextCheckingResult SpellCheckingResult (NSRange range);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSDictionary components);
	public static NSTextCheckingResult TransitInformationCheckingResult (NSRange range, NSTextCheckingTransitComponents components);
```

### Type Changed: Foundation.NSTextCheckingType

Added values:

```
PhoneNumber = 2048,
	RegularExpression = 1024,
	TransitInformation = 4096,
```

### Type Changed: Foundation.NSUrl

Added property:

```
public virtual string PathExtension { get; }
```

### Type Changed: Foundation.NSUrlSession

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

### Type Changed: Foundation.NSUserNotificationCenter

Modified properties:

```
public NSUserNotificationCenterDelegate INSUserNotificationCenterDelegate Delegate { get; set; }
```

### Type Changed: Foundation.PreserveAttribute

Added constructor:

```
public PreserveAttribute (System.Type type);
```

### Type Changed: Foundation.ProtocolAttribute

Added property:

```
public bool IsInformal { get; set; }
```

### New Type Foundation.NSAttributedStringDocumentAttributes

```
public class NSAttributedStringDocumentAttributes : Foundation.DictionaryContainer {
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
	public WebKit.WebPreferences WebPreferences { get; set; }
	public NSObject WebResourceLoadDelegate { get; set; }
}
```

### New Type Foundation.NSDocumentType

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

### New Type Foundation.NSTextChecking

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

### New Type Foundation.NSTextCheckingAddressComponents

```
public class NSTextCheckingAddressComponents : Foundation.DictionaryContainer {
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

### New Type Foundation.NSTextCheckingTransitComponents

```
public class NSTextCheckingTransitComponents : Foundation.DictionaryContainer {
	// constructors
	public NSTextCheckingTransitComponents ();
	public NSTextCheckingTransitComponents (NSDictionary dictionary);
	// properties
	public string Airline { get; }
	public string Flight { get; }
}
```

### New Type Foundation.NSUrlSessionActiveTasks2

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

### New Type Foundation.NSUrlSessionPendingTasks2

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

## Namespace ImageIO

### Type Changed: ImageIO.CGImageDestinationOptions

Removed property:

```
public Foundation.NSDictionary GidfDictionary { get; set; }
```

Added property:

```
public Foundation.NSDictionary GifDictionary { get; set; }
```

## Namespace ImageKit

### Type Changed: ImageKit.IIKImageBrowserDataSource

Removed method:

```
public virtual IKImageBrowserItem GetItem (IKImageBrowserView aBrowser, nint index);
```

Added method:

```
public virtual IIKImageBrowserItem GetItem (IKImageBrowserView aBrowser, nint index);
```

### Type Changed: ImageKit.IKCameraDeviceView

Modified properties:

```
public IKCameraDeviceViewDelegate IIKCameraDeviceViewDelegate Delegate { get; set; }
```

### Type Changed: ImageKit.IKDeviceBrowserView

Modified properties:

```
public IKDeviceBrowserViewDelegate IIKDeviceBrowserViewDelegate Delegate { get; set; }
```

### Type Changed: ImageKit.IKImageBrowserDataSource

Removed method:

```
public virtual IKImageBrowserItem GetItem (IKImageBrowserView aBrowser, nint index);
```

Added method:

```
public virtual IIKImageBrowserItem GetItem (IKImageBrowserView aBrowser, nint index);
```

### Type Changed: ImageKit.IKImageBrowserView

Modified properties:

```
public IKImageBrowserDataSource IIKImageBrowserDataSource DataSource { get; set; }
	public IKImageBrowserDelegate IIKImageBrowserDelegate Delegate { get; set; }
	public virtual AppKit.NSDraggingDestination AppKit.INSDraggingDestination DraggingDestinationDelegate { get; set; }
```

Removed method:

```
public virtual IKImageBrowserCell NewCell (IKImageBrowserItem representedItem);
```

Added method:

```
public virtual IKImageBrowserCell NewCell (IIKImageBrowserItem representedItem);
```

### Type Changed: ImageKit.IKImageEditPanel

Modified properties:

```
public virtual IKImageEditPanelDataSource IIKImageEditPanelDataSource DataSource { get; set; }
```

### Type Changed: ImageKit.IKSaveOptions

Modified properties:

```
public IKSaveOptionsDelegate IIKSaveOptionsDelegate Delegate { get; set; }
```

### Type Changed: ImageKit.IKScannerDeviceView

Modified properties:

```
public IKScannerDeviceViewDelegate IIKScannerDeviceViewDelegate Delegate { get; set; }
```

### Type Changed: ImageKit.IKSlideshow

Removed method:

```
public virtual void RunSlideshow (IKSlideshowDataSource dataSource, string slideshowMode, Foundation.NSDictionary slideshowOptions);
```

Added method:

```
public virtual void RunSlideshow (IIKSlideshowDataSource dataSource, string slideshowMode, Foundation.NSDictionary slideshowOptions);
```

## Namespace MapKit

### Type Changed: MapKit.MKPointAnnotation

Added property:

```
public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

## Namespace NetworkExtension

### Type Changed: NetworkExtension.NEVpnIke2DiffieHellman

Added values:

```
Group19 = 19,
	Group20 = 20,
	Group21 = 21,
```

### Type Changed: NetworkExtension.NEVpnIke2EncryptionAlgorithm

Added values:

```
AES128GCM = 5,
	AES256GCM = 6,
```

### New Type NetworkExtension.NEVpnIke2CertificateType

```
[Serializable]
public enum NEVpnIke2CertificateType {
	ECDSA256 = 2,
	ECDSA384 = 3,
	ECDSA521 = 4,
	RSA = 1,
}
```

## Namespace ObjCRuntime

### Type Changed: ObjCRuntime.Constants

Modified fields:

```
public const string Version = "1.12.0" "2.0.0";
```

Added field:

```
public static const string QuickLookUILibrary = "/System/Library/Frameworks/Quartz.framework/Frameworks/QuickLookUI.framework/QuickLookUI";
```

### Type Changed: ObjCRuntime.Dlfcn

Added method:

```
public static IntPtr dlsym (Dlfcn.RTLD lookupType, string symbol);
```

### Type Changed: ObjCRuntime.Platform

Added value:

```
iOS_8_3 = 525056,
```

### Type Changed: ObjCRuntime.Runtime

Added methods:

```
public static void ConnectMethod (System.Type type, System.Reflection.MethodInfo method, Foundation.ExportAttribute export);
	public static void ConnectMethod (System.Type type, System.Reflection.MethodInfo method, Selector selector);
```

### Type Changed: ObjCRuntime.ThreadSafeAttribute

Added constructor:

```
public ThreadSafeAttribute (bool safe);
```

Added property:

```
public bool Safe { get; }
```

### New Type ObjCRuntime.CategoryAttribute

```
public class CategoryAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public CategoryAttribute (System.Type type);
	// properties
	public string Name { get; set; }
	public System.Type Type { get; set; }
}
```

### New Type ObjCRuntime.Protocol

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

## Namespace PdfKit

### Type Changed: PdfKit.PdfDocument

Modified properties:

```
public PdfDocumentDelegate IPdfDocumentDelegate Delegate { get; set; }
```

### Type Changed: PdfKit.PdfView

Modified properties:

```
public PdfViewDelegate IPdfViewDelegate Delegate { get; set; }
```

## Namespace QTKit

### Type Changed: QTKit.QTCaptureDecompressedVideoOutput

Modified properties:

```
public QTCaptureDecompressedVideoOutputDelegate IQTCaptureDecompressedVideoOutputDelegate Delegate { get; set; }
```

### Type Changed: QTKit.QTCaptureFileOutput

Modified properties:

```
public QTCaptureFileOutputDelegate IQTCaptureFileOutputDelegate Delegate { get; set; }
```

### Type Changed: QTKit.QTCaptureView

Modified properties:

```
public QTCaptureViewDelegate IQTCaptureViewDelegate Delegate { get; set; }
```

### Type Changed: QTKit.QTMovieView

Modified properties:

```
public QTMovieViewDelegate IQTMovieViewDelegate Delegate { get; set; }
```

## Namespace SceneKit

### Type Changed: SceneKit.SCNGeometry

Obsoleted methods:

```
[Obsolete ("Use the Create(SCNGeometrySource[], SCNGeometryElement[]) method instead, as it has a strongly typed return"]
	public static Foundation.NSObject FromSources (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

Added method:

```
public static SCNGeometry Create (SCNGeometrySource[] sources, SCNGeometryElement[] elements);
```

## Namespace ScriptingBridge

### Type Changed: ScriptingBridge.SBApplication

Modified properties:

```
public SBApplicationDelegate ISBApplicationDelegate Delegate { get; set; }
```

Added methods:

```
public static T FromBundleIdentifier<T> (string ident);
	public static T FromProcessIdentifier<T> (int pid);
	public static T FromURL<T> (Foundation.NSUrl url);
```

### New Type ScriptingBridge.SBElementArray

```
public class SBElementArray : Foundation.NSMutableArray, Foundation.INSCoding, Foundation.INSCopying, Foundation.INSMutableCopying, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable<Foundation.NSObject> {
	// constructors
	public SBElementArray (Foundation.NSCoder coder);
	protected SBElementArray (Foundation.NSObjectFlag t);
	protected SBElementArray (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual Foundation.NSObject[] ArrayByApplyingSelector (ObjCRuntime.Selector selector);
	public virtual Foundation.NSObject[] ArrayByApplyingSelector (ObjCRuntime.Selector aSelector, Foundation.NSObject argument);
	public virtual Foundation.NSObject[] Get ();
	public virtual Foundation.NSObject ObjectAtLocation (Foundation.NSObject location);
	public virtual Foundation.NSObject ObjectWithID (Foundation.NSObject identifier);
	public virtual Foundation.NSObject ObjectWithName (string name);
}
```

## Namespace Security

### Type Changed: Security.SecPadding

Added value:

```
Raw = 16384,
```

### Type Changed: Security.SecRecord

Added constructor:

```
public SecRecord ();
```

Removed properties:

```
public bool UseNoAuthenticationUI { get; set; }
	public string UseOperationPrompt { get; set; }
```

### Type Changed: Security.SecStatusCode

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

## Namespace StoreKit

### Type Changed: StoreKit.SKMutablePayment

Added property:

```
public virtual string ApplicationUsername { get; set; }
```

### Type Changed: StoreKit.SKPayment

Added property:

```
public virtual string ApplicationUsername { get; }
```

### Type Changed: StoreKit.SKPaymentQueue

Added method:

```
public virtual void RestoreCompletedTransactions (string username);
```

### Type Changed: StoreKit.SKReceiptRefreshRequest

Removed method:

```
public static void TerminateForInvalidReceipt ();
```

## Namespace System

### Type Changed: System.nfloat

Added constructors:

```
public nfloat (float v);
	public nfloat (double v);
```

### Type Changed: System.nint

Added constructors:

```
public nint (int v);
	public nint (long v);
```

### Type Changed: System.nuint

Added constructors:

```
public nuint (uint v);
	public nuint (ulong v);
```

## Namespace WebKit

### Type Changed: WebKit.DomEvent

Modified properties:

```
public virtual DomEventTarget IDomEventTarget CurrentTarget { get; }
	public virtual DomEventTarget IDomEventTarget SourceElement { get; }
	public virtual DomEventTarget IDomEventTarget Target { get; }
```

### Type Changed: WebKit.DomEventTarget

Removed methods:

```
public virtual void AddEventListener (string type, DomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, DomEventListener listener, bool useCapture);
```

Added methods:

```
public virtual void AddEventListener (string type, IDomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, IDomEventListener listener, bool useCapture);
```

### Type Changed: WebKit.DomMouseEvent

Modified properties:

```
public virtual DomEventTarget IDomEventTarget RelatedTarget { get; }
```

Removed method:

```
public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
```

Added method:

```
public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, IDomEventTarget relatedTarget);
```

### Type Changed: WebKit.DomNode

Removed methods:

```
public virtual void AddEventListener (string type, DomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, DomEventListener listener, bool useCapture);
```

Added methods:

```
public virtual void AddEventListener (string type, IDomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, IDomEventListener listener, bool useCapture);
```

### Type Changed: WebKit.IDomEventTarget

Removed methods:

```
public virtual void AddEventListener (string type, DomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, DomEventListener listener, bool useCapture);
```

Added methods:

```
public virtual void AddEventListener (string type, IDomEventListener listener, bool useCapture);
	public virtual void RemoveEventListener (string type, IDomEventListener listener, bool useCapture);
```

### Type Changed: WebKit.WebDataSource

Modified properties:

```
public virtual WebDocumentRepresentation IWebDocumentRepresentation Representation { get; }
```

### Type Changed: WebKit.WebUIDelegate

Removed method:

```
public virtual void UIRunOpenPanelForFileButton (WebView sender, WebOpenPanelResultListener resultListener);
```

Added method:

```
public virtual void UIRunOpenPanelForFileButton (WebView sender, IWebOpenPanelResultListener resultListener);
```

### Type Changed: WebKit.WebUIDelegate_Extensions

Removed method:

```
public static void UIRunOpenPanelForFileButton (IWebUIDelegate This, WebView sender, WebOpenPanelResultListener resultListener);
```

Added method:

```
public static void UIRunOpenPanelForFileButton (IWebUIDelegate This, WebView sender, IWebOpenPanelResultListener resultListener);
```

### Type Changed: WebKit.WebView

Modified properties:

```
public WebDownloadDelegate IWebDownloadDelegate DownloadDelegate { get; set; }
	public WebFrameLoadDelegate IWebFrameLoadDelegate FrameLoadDelegate { get; set; }
	public WebPolicyDelegate IWebPolicyDelegate PolicyDelegate { get; set; }
	public WebResourceLoadDelegate IWebResourceLoadDelegate ResourceLoadDelegate { get; set; }
	public WebUIDelegate IWebUIDelegate UIDelegate { get; set; }
```

### Type Changed: WebKit.WebViewRunOpenPanelEventArgs

Removed constructor:

```
public WebViewRunOpenPanelEventArgs (WebOpenPanelResultListener resultListener);
```

Added constructor:

```
public WebViewRunOpenPanelEventArgs (IWebOpenPanelResultListener resultListener);
```

Modified properties:

```
public WebOpenPanelResultListener IWebOpenPanelResultListener ResultListener { get; set; }
```

## New Namespace QuickLookUI

### New Type QuickLookUI.IQLPreviewItem

```
public interface IQLPreviewItem : ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type QuickLookUI.IQLPreviewPanelDataSource

```
public interface IQLPreviewPanelDataSource : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual nint NumberOfPreviewItemsInPreviewPanel (QLPreviewPanel panel);
	public virtual IQLPreviewItem PreviewItemAtIndex (QLPreviewPanel panel, nint index);
}
```

### New Type QuickLookUI.IQLPreviewPanelDelegate

```
public interface IQLPreviewPanelDelegate : ObjCRuntime.INativeObject, System.IDisposable, AppKit.INSWindowDelegate {
}
```

### New Type QuickLookUI.QLPreviewItem

```
public class QLPreviewItem : Foundation.NSObject, IQLPreviewItem, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable<Foundation.NSObject> {
	// constructors
	public QLPreviewItem ();
	protected QLPreviewItem (Foundation.NSObjectFlag t);
	protected QLPreviewItem (IntPtr handle);
	// properties
	public virtual Foundation.NSObject PreviewItemDisplayState { get; }
	public virtual string PreviewItemTitle { get; }
	public virtual Foundation.NSUrl PreviewItemURL { get; }
}
```

### New Type QuickLookUI.QLPreviewItem_Extensions

```
public static class QLPreviewItem_Extensions {
	// methods
	public static Foundation.NSObject GetPreviewItemDisplayState (IQLPreviewItem This);
	public static string GetPreviewItemTitle (IQLPreviewItem This);
	public static Foundation.NSUrl GetPreviewItemURL (IQLPreviewItem This);
}
```

### New Type QuickLookUI.QLPreviewPanel

```
public class QLPreviewPanel : AppKit.NSPanel, AppKit.INSAppearanceCustomization, AppKit.INSUserInterfaceItemIdentification, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSCoding, Foundation.INSObjectProtocol, System.IEquatable<Foundation.NSObject> {
	// constructors
	public QLPreviewPanel ();
	public QLPreviewPanel (Foundation.NSCoder coder);
	protected QLPreviewPanel (Foundation.NSObjectFlag t);
	protected QLPreviewPanel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual Foundation.NSObject CurrentController { get; }
	public virtual IQLPreviewItem CurrentPreviewItem { get; }
	public virtual nint CurrentPreviewItemIndex { get; set; }
	public IQLPreviewPanelDataSource DataSource { get; set; }
	public IQLPreviewPanelDelegate Delegate { get; set; }
	public virtual Foundation.NSObject DisplayState { get; set; }
	public virtual bool InFullScreenMode { get; }
	public virtual Foundation.NSObject WeakDataSource { get; set; }
	public virtual Foundation.NSObject WeakDelegate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool EnterFullScreenMode (AppKit.NSScreen screen, Foundation.NSDictionary options);
	public bool EnterFullScreenMode ();
	public void ExitFullScreenModeWithOptions ();
	public virtual void ExitFullScreenModeWithOptions (Foundation.NSDictionary options);
	public virtual void RefreshCurrentPreviewItem ();
	public virtual void ReloadData ();
	public static QLPreviewPanel SharedPreviewPanel ();
	public static bool SharedPreviewPanelExists ();
	public virtual void UpdateController ();
}
```

### New Type QuickLookUI.QLPreviewPanelController

```
public static class QLPreviewPanelController {
	// methods
	public static bool AcceptsPreviewPanelControl (Foundation.NSObject This, QLPreviewPanel panel);
	public static void BeginPreviewPanelControl (Foundation.NSObject This, QLPreviewPanel panel);
	public static void EndPreviewPanelControl (Foundation.NSObject This, QLPreviewPanel panel);
}
```

### New Type QuickLookUI.QLPreviewPanelDataSource

```
public abstract class QLPreviewPanelDataSource : Foundation.NSObject, IQLPreviewPanelDataSource, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable<Foundation.NSObject> {
	// constructors
	protected QLPreviewPanelDataSource ();
	protected QLPreviewPanelDataSource (Foundation.NSObjectFlag t);
	protected QLPreviewPanelDataSource (IntPtr handle);
	// methods
	public virtual nint NumberOfPreviewItemsInPreviewPanel (QLPreviewPanel panel);
	public virtual IQLPreviewItem PreviewItemAtIndex (QLPreviewPanel panel, nint index);
}
```

### New Type QuickLookUI.QLPreviewPanelDelegate

```
public class QLPreviewPanelDelegate : Foundation.NSObject, IQLPreviewPanelDelegate, AppKit.INSWindowDelegate, ObjCRuntime.INativeObject, System.IDisposable, Foundation.INSObjectProtocol, System.IEquatable<Foundation.NSObject> {
	// constructors
	public QLPreviewPanelDelegate ();
	protected QLPreviewPanelDelegate (Foundation.NSObjectFlag t);
	protected QLPreviewPanelDelegate (IntPtr handle);
	// methods
	public virtual AppKit.NSWindow[] CustomWindowsToEnterFullScreen (AppKit.NSWindow window);
	public virtual AppKit.NSWindow[] CustomWindowsToExitFullScreen (AppKit.NSWindow window);
	public virtual void DidBecomeKey (Foundation.NSNotification notification);
	public virtual void DidBecomeMain (Foundation.NSNotification notification);
	public virtual void DidChangeBackingProperties (Foundation.NSNotification notification);
	public virtual void DidChangeScreen (Foundation.NSNotification notification);
	public virtual void DidChangeScreenProfile (Foundation.NSNotification notification);
	public virtual void DidDecodeRestorableState (AppKit.NSWindow window, Foundation.NSCoder coder);
	public virtual void DidDeminiaturize (Foundation.NSNotification notification);
	public virtual void DidEndLiveResize (Foundation.NSNotification notification);
	public virtual void DidEndSheet (Foundation.NSNotification notification);
	public virtual void DidEnterFullScreen (Foundation.NSNotification notification);
	public virtual void DidEnterVersionBrowser (Foundation.NSNotification notification);
	public virtual void DidExitFullScreen (Foundation.NSNotification notification);
	public virtual void DidExitVersionBrowser (Foundation.NSNotification notification);
	public virtual void DidExpose (Foundation.NSNotification notification);
	public virtual void DidFailToEnterFullScreen (AppKit.NSWindow window);
	public virtual void DidFailToExitFullScreen (AppKit.NSWindow window);
	public virtual void DidMiniaturize (Foundation.NSNotification notification);
	public virtual void DidMove (Foundation.NSNotification notification);
	public virtual void DidResignKey (Foundation.NSNotification notification);
	public virtual void DidResignMain (Foundation.NSNotification notification);
	public virtual void DidResize (Foundation.NSNotification notification);
	public virtual void DidUpdate (Foundation.NSNotification notification);
	public virtual bool HandleEvent (QLPreviewPanel panel, AppKit.NSEvent theEvent);
	public virtual bool ShouldDragDocumentWithEvent (AppKit.NSWindow window, AppKit.NSEvent theEvent, CoreGraphics.CGPoint dragImageLocation, AppKit.NSPasteboard withPasteboard);
	public virtual bool ShouldPopUpDocumentPathMenu (AppKit.NSWindow window, AppKit.NSMenu menu);
	public virtual bool ShouldZoom (AppKit.NSWindow window, CoreGraphics.CGRect newFrame);
	public virtual CoreGraphics.CGRect SourceFrameOnScreenForPreviewItem (QLPreviewPanel panel, IQLPreviewItem item);
	public virtual void StartCustomAnimationToEnterFullScreen (AppKit.NSWindow window, double duration);
	public virtual void StartCustomAnimationToExitFullScreen (AppKit.NSWindow window, double duration);
	public virtual Foundation.NSObject TransitionImageForPreviewItem (QLPreviewPanel panel, IQLPreviewItem item, CoreGraphics.CGRect contentRect);
	public virtual void WillBeginSheet (Foundation.NSNotification notification);
	public virtual void WillClose (Foundation.NSNotification notification);
	public virtual void WillEncodeRestorableState (AppKit.NSWindow window, Foundation.NSCoder coder);
	public virtual void WillEnterFullScreen (Foundation.NSNotification notification);
	public virtual void WillEnterVersionBrowser (Foundation.NSNotification notification);
	public virtual void WillExitFullScreen (Foundation.NSNotification notification);
	public virtual void WillExitVersionBrowser (Foundation.NSNotification notification);
	public virtual void WillMiniaturize (Foundation.NSNotification notification);
	public virtual void WillMove (Foundation.NSNotification notification);
	public virtual CoreGraphics.CGRect WillPositionSheet (AppKit.NSWindow window, AppKit.NSWindow sheet, CoreGraphics.CGRect usingRect);
	public virtual CoreGraphics.CGSize WillResize (AppKit.NSWindow sender, CoreGraphics.CGSize toFrameSize);
	public virtual CoreGraphics.CGSize WillResizeForVersionBrowser (AppKit.NSWindow window, CoreGraphics.CGSize maxPreferredSize, CoreGraphics.CGSize maxAllowedSize);
	public virtual Foundation.NSObject WillReturnFieldEditor (AppKit.NSWindow sender, Foundation.NSObject client);
	public virtual Foundation.NSUndoManager WillReturnUndoManager (AppKit.NSWindow window);
	public virtual void WillStartLiveResize (Foundation.NSNotification notification);
	public virtual CoreGraphics.CGSize WillUseFullScreenContentSize (AppKit.NSWindow window, CoreGraphics.CGSize proposedSize);
	public virtual AppKit.NSApplicationPresentationOptions WillUseFullScreenPresentationOptions (AppKit.NSWindow window, AppKit.NSApplicationPresentationOptions proposedOptions);
	public virtual CoreGraphics.CGRect WillUseStandardFrame (AppKit.NSWindow window, CoreGraphics.CGRect newFrame);
	public virtual bool WindowShouldClose (Foundation.NSObject sender);
}
```

### New Type QuickLookUI.QLPreviewPanelDelegate_Extensions

```
public static class QLPreviewPanelDelegate_Extensions {
	// methods
	public static bool HandleEvent (IQLPreviewPanelDelegate This, QLPreviewPanel panel, AppKit.NSEvent theEvent);
	public static CoreGraphics.CGRect SourceFrameOnScreenForPreviewItem (IQLPreviewPanelDelegate This, QLPreviewPanel panel, IQLPreviewItem item);
	public static Foundation.NSObject TransitionImageForPreviewItem (IQLPreviewPanelDelegate This, QLPreviewPanel panel, IQLPreviewItem item, CoreGraphics.CGRect contentRect);
}
```

## New Namespace VideoToolbox

### New Type VideoToolbox.VTColorPrimaries

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

### New Type VideoToolbox.VTCompressionProperties

```
public class VTCompressionProperties : Foundation.DictionaryContainer {
	// constructors
	public VTCompressionProperties ();
	public VTCompressionProperties (Foundation.NSDictionary dictionary);
	// properties
	public bool? AllowFrameReordering { get; set; }
	public bool? AllowTemporalCompression { get; set; }
	public bool? AspectRatio16x9 { get; set; }
	public int? AverageBitRate { get; set; }
	public Foundation.NSDictionary CleanAperture { get; set; }
	public VTColorPrimaries ColorPrimaries { get; set; }
	public System.Collections.Generic.List<VTDataRateLimit> DataRateLimits { get; set; }
	public CoreMedia.CMPixelFormat? Depth { get; set; }
	public double? ExpectedDuration { get; set; }
	public double? ExpectedFrameRate { get; set; }
	public VTFieldCount? FieldCount { get; set; }
	public VTFieldDetail FieldDetail { get; set; }
	public VTH264EntropyMode H264EntropyMode { get; set; }
	public Foundation.NSData ICCProfile { get; set; }
	public int? MaxFrameDelayCount { get; set; }
	public int? MaxH264SliceBytes { get; set; }
	public int? MaxKeyFrameInterval { get; set; }
	public double? MaxKeyFrameIntervalDuration { get; set; }
	public bool? MoreFramesAfterEnd { get; set; }
	public bool? MoreFramesBeforeStart { get; set; }
	public VTMultiPassStorage MultiPassStorage { get; set; }
	public int? NumberOfPendingFrames { get; }
	public Foundation.NSDictionary PixelAspectRatio { get; set; }
	public bool? PixelBufferPoolIsShared { get; }
	public Foundation.NSDictionary PixelTransferProperties { get; set; }
	public VTProfileLevel ProfileLevel { get; set; }
	public bool? ProgressiveScan { get; set; }
	public float? Quality { get; set; }
	public bool? RealTime { get; set; }
	public uint? SourceFrameCount { get; set; }
	public VTTransferFunction TransferFunction { get; set; }
	public bool? UsingHardwareAcceleratedVideoEncoder { get; }
	public Foundation.NSDictionary VideoEncoderPixelBufferAttributes { get; }
	public VTYCbCrMatrix YCbCrMatrix { get; set; }
}
```

### New Type VideoToolbox.VTCompressionPropertyKey

```
public static class VTCompressionPropertyKey {
	// properties
	public static Foundation.NSString AllowFrameReordering { get; }
	public static Foundation.NSString AllowTemporalCompression { get; }
	public static Foundation.NSString AspectRatio16x9 { get; }
	public static Foundation.NSString AverageBitRate { get; }
	public static Foundation.NSString CleanAperture { get; }
	public static Foundation.NSString ColorPrimaries { get; }
	public static Foundation.NSString DataRateLimits { get; }
	public static Foundation.NSString Depth { get; }
	public static Foundation.NSString ExpectedDuration { get; }
	public static Foundation.NSString ExpectedFrameRate { get; }
	public static Foundation.NSString FieldCount { get; }
	public static Foundation.NSString FieldDetail { get; }
	public static Foundation.NSString H264EntropyMode { get; }
	public static Foundation.NSString ICCProfile { get; }
	public static Foundation.NSString MaxFrameDelayCount { get; }
	public static Foundation.NSString MaxH264SliceBytes { get; }
	public static Foundation.NSString MaxKeyFrameInterval { get; }
	public static Foundation.NSString MaxKeyFrameIntervalDuration { get; }
	public static Foundation.NSString MoreFramesAfterEnd { get; }
	public static Foundation.NSString MoreFramesBeforeStart { get; }
	public static Foundation.NSString MultiPassStorage { get; }
	public static Foundation.NSString NumberOfPendingFrames { get; }
	public static Foundation.NSString PixelAspectRatio { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString ProfileLevel { get; }
	public static Foundation.NSString ProgressiveScan { get; }
	public static Foundation.NSString Quality { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString SourceFrameCount { get; }
	public static Foundation.NSString TransferFunction { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoEncoder { get; }
	public static Foundation.NSString VideoEncoderPixelBufferAttributes { get; }
	public static Foundation.NSString YCbCrMatrix { get; }
}
```

### New Type VideoToolbox.VTCompressionSession

```
public class VTCompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTCompressionSession (IntPtr handle);
	// methods
	protected override void ~VTCompressionSession ();
	public VTStatus BeginPass (VTCompressionSessionOptionFlags flags);
	public VTStatus CompleteFrames (CoreMedia.CMTime completeUntilPresentationTimeStamp);
	public static VTCompressionSession Create (int width, int height, CoreMedia.CMVideoCodecType codecType, VTCompressionSession.VTCompressionOutputCallback compressionOutputCallback, VTVideoEncoderSpecification encoderSpecification, Foundation.NSDictionary sourceImageBufferAttributes);
	public void Dispose ();
	protected override void Dispose (bool disposing);
	public VTStatus EncodeFrame (CoreVideo.CVImageBuffer imageBuffer, CoreMedia.CMTime presentationTimestampe, CoreMedia.CMTime duration, Foundation.NSDictionary frameProperties, IntPtr sourceFrame, out VTEncodeInfoFlags infoFlags);
	public VTStatus EndPass (out bool furtherPassesRequested);
	public VTStatus EndPassAsFinal ();
	public CoreVideo.CVPixelBufferPool GetPixelBufferPool ();
	public VTStatus GetTimeRangesForNextPass (out CoreMedia.CMTimeRange[] timeRanges);
	public VTStatus PrepareToEncodeFrames ();
	public VTStatus SetCompressionProperties (VTCompressionProperties options);

	// inner types
	public sealed delegate VTCompressionOutputCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
		// constructors
		public VTCompressionSession (object object, IntPtr method);
		// methods
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTEncodeInfoFlags flags, CoreMedia.CMSampleBuffer buffer);
	}
}
```

### New Type VideoToolbox.VTCompressionSessionOptionFlags

```
[Serializable]
[Flags]
public enum VTCompressionSessionOptionFlags {
	BeginFinalPass = 1,
}
```

### New Type VideoToolbox.VTDataRateLimit

```
public struct VTDataRateLimit {
	// constructors
	public VTDataRateLimit (uint numberOfBytes, double seconds);
	// properties
	public uint NumberOfBytes { get; set; }
	public double Seconds { get; set; }
}
```

### New Type VideoToolbox.VTDecodeFrameFlags

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

### New Type VideoToolbox.VTDecodeInfoFlags

```
[Serializable]
[Flags]
public enum VTDecodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
	ImageBufferModifiable = 4,
}
```

### New Type VideoToolbox.VTDecompressionProperties

```
public class VTDecompressionProperties : Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionProperties ();
	public VTDecompressionProperties (Foundation.NSDictionary dictionary);
	// properties
	public bool? ContentHasInterframeDependencies { get; }
	public VTDeinterlaceMode DeinterlaceMode { get; set; }
	public VTFieldMode FieldMode { get; set; }
	public Foundation.NSDictionary MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public Foundation.NSDictionary MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public uint? NumberOfFramesBeingDecoded { get; }
	public VTOnlyTheseFrames OnlyTheseFrames { get; set; }
	public uint? OutputPoolRequestedMinimumBufferCount { get; set; }
	public CoreVideo.CVPixelBufferPool PixelBufferPool { get; }
	public bool? PixelBufferPoolIsShared { get; }
	public CoreMedia.CMPixelFormat[] PixelFormatsWithReducedResolutionSupport { get; }
	public Foundation.NSDictionary PixelTransferProperties { get; set; }
	public bool? RealTime { get; set; }
	public uint? ReducedCoefficientDecode { get; set; }
	public float? ReducedFrameDelivery { get; set; }
	public VTDecompressionResolutionOptions ReducedResolutionDecode { get; set; }
	public Foundation.NSDictionary[] SuggestedQualityOfServiceTiers { get; }
	public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByPerformance { get; }
	public CoreMedia.CMPixelFormat[] SupportedPixelFormatsOrderedByQuality { get; }
	public uint? ThreadCount { get; set; }
	public bool? UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTDecompressionPropertyKey

```
public static class VTDecompressionPropertyKey {
	// properties
	public static Foundation.NSString ContentHasInterframeDependencies { get; }
	public static Foundation.NSString DeinterlaceMode { get; }
	public static Foundation.NSString DeinterlaceMode_Temporal { get; }
	public static Foundation.NSString DeinterlaceMode_VerticalFilter { get; }
	public static Foundation.NSString FieldMode { get; }
	public static Foundation.NSString FieldMode_BothFields { get; }
	public static Foundation.NSString FieldMode_BottomFieldOnly { get; }
	public static Foundation.NSString FieldMode_DeinterlaceFields { get; }
	public static Foundation.NSString FieldMode_SingleField { get; }
	public static Foundation.NSString FieldMode_TopFieldOnly { get; }
	public static Foundation.NSString MaxOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString MinOutputPresentationTimeStampOfFramesBeingDecoded { get; }
	public static Foundation.NSString NumberOfFramesBeingDecoded { get; }
	public static Foundation.NSString OnlyTheseFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_AllFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_IFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_KeyFrames { get; }
	public static Foundation.NSString OnlyTheseFrames_NonDroppableFrames { get; }
	public static Foundation.NSString OutputPoolRequestedMinimumBufferCount { get; }
	public static Foundation.NSString PixelBufferPool { get; }
	public static Foundation.NSString PixelBufferPoolIsShared { get; }
	public static Foundation.NSString PixelFormatsWithReducedResolutionSupport { get; }
	public static Foundation.NSString PixelTransferProperties { get; }
	public static Foundation.NSString RealTime { get; }
	public static Foundation.NSString ReducedCoefficientDecode { get; }
	public static Foundation.NSString ReducedFrameDelivery { get; }
	public static Foundation.NSString ReducedResolutionDecode { get; }
	public static Foundation.NSString SuggestedQualityOfServiceTiers { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByPerformance { get; }
	public static Foundation.NSString SupportedPixelFormatsOrderedByQuality { get; }
	public static Foundation.NSString ThreadCount { get; }
	public static Foundation.NSString UsingHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTDecompressionResolutionKeys

```
public static class VTDecompressionResolutionKeys {
	// properties
	public static Foundation.NSString Height { get; }
	public static Foundation.NSString Width { get; }
}
```

### New Type VideoToolbox.VTDecompressionResolutionOptions

```
public class VTDecompressionResolutionOptions : Foundation.DictionaryContainer {
	// constructors
	public VTDecompressionResolutionOptions ();
	public VTDecompressionResolutionOptions (Foundation.NSDictionary dictionary);
	// properties
	public float? Height { get; set; }
	public float? Width { get; set; }
}
```

### New Type VideoToolbox.VTDecompressionSession

```
public class VTDecompressionSession : VideoToolbox.VTSession, ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTDecompressionSession (IntPtr handle);
	// methods
	protected override void ~VTDecompressionSession ();
	public VTStatus CanAcceptFormatDescriptor (CoreMedia.CMFormatDescription newDescriptor);
	public VTStatus CopyBlackPixelBuffer (out CoreVideo.CVPixelBuffer pixelBuffer);
	public static VTDecompressionSession Create (VTDecompressionSession.VTDecompressionOutputCallback outputCallback, CoreMedia.CMVideoFormatDescription formatDescription, VTVideoDecoderSpecification decoderSpecification, Foundation.NSDictionary destinationImageBufferAttributes);
	public VTStatus DecodeFrame (CoreMedia.CMSampleBuffer sampleBuffer, VTDecodeFrameFlags decodeFlags, IntPtr sourceFrame, out VTDecodeInfoFlags infoFlags);
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
		public virtual System.IAsyncResult BeginInvoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration, System.AsyncCallback callback, object object);
		public virtual void EndInvoke (System.IAsyncResult result);
		public virtual void Invoke (IntPtr sourceFrame, VTStatus status, VTDecodeInfoFlags flags, CoreVideo.CVImageBuffer buffer, CoreMedia.CMTime presentationTimeStamp, CoreMedia.CMTime presentationDuration);
	}
}
```

### New Type VideoToolbox.VTDeinterlaceMode

```
[Serializable]
public enum VTDeinterlaceMode {
	Temporal = 2,
	Unset = 0,
	VerticalFilter = 1,
}
```

### New Type VideoToolbox.VTEncodeFrameOptionKey

```
public static class VTEncodeFrameOptionKey {
	// properties
	public static Foundation.NSString ForceKeyFrame { get; }
}
```

### New Type VideoToolbox.VTEncodeFrameOptions

```
public class VTEncodeFrameOptions : Foundation.DictionaryContainer {
	// constructors
	public VTEncodeFrameOptions ();
	public VTEncodeFrameOptions (Foundation.NSDictionary dictionary);
	// properties
	public bool? ForceKeyFrame { get; set; }
}
```

### New Type VideoToolbox.VTEncodeInfoFlags

```
[Serializable]
[Flags]
public enum VTEncodeInfoFlags {
	Asynchronous = 1,
	FrameDropped = 2,
}
```

### New Type VideoToolbox.VTFieldCount

```
[Serializable]
public enum VTFieldCount {
	Interlaced = 2,
	Progressive = 1,
}
```

### New Type VideoToolbox.VTFieldDetail

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

### New Type VideoToolbox.VTFieldMode

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

### New Type VideoToolbox.VTFrameSilo

```
public class VTFrameSilo : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTFrameSilo (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTFrameSilo ();
	public VTStatus AddSampleBuffer (CoreMedia.CMSampleBuffer sampleBuffer);
	public static VTFrameSilo Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	public VTStatus ForEach (System.Func<CoreMedia.CMSampleBuffer,VideoToolbox.VTStatus> callback, CoreMedia.CMTimeRange? range);
	public VTStatus GetProgressOfCurrentPass (out float progress);
	public VTStatus SetTimeRangesForNextPass (CoreMedia.CMTimeRange[] ranges);
}
```

### New Type VideoToolbox.VTH264EntropyMode

```
[Serializable]
public enum VTH264EntropyMode {
	Cabac = 2,
	Cavlc = 1,
	Unset = 0,
}
```

### New Type VideoToolbox.VTH264EntropyModeKeys

```
public static class VTH264EntropyModeKeys {
	// properties
	public static Foundation.NSString CABAC { get; }
	public static Foundation.NSString CAVLC { get; }
}
```

### New Type VideoToolbox.VTMultiPassStorage

```
public class VTMultiPassStorage : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTMultiPassStorage (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTMultiPassStorage ();
	public VTStatus Close ();
	public static VTMultiPassStorage Create (VTMultiPassStorageCreationOptions options, Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange);
	public static VTMultiPassStorage Create (Foundation.NSUrl fileUrl, CoreMedia.CMTimeRange? timeRange, Foundation.NSDictionary options);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
}
```

### New Type VideoToolbox.VTMultiPassStorageCreationOptionKeys

```
public static class VTMultiPassStorageCreationOptionKeys {
	// properties
	public static Foundation.NSString DoNotDelete { get; }
}
```

### New Type VideoToolbox.VTMultiPassStorageCreationOptions

```
public class VTMultiPassStorageCreationOptions : Foundation.DictionaryContainer {
	// constructors
	public VTMultiPassStorageCreationOptions ();
	public VTMultiPassStorageCreationOptions (Foundation.NSDictionary dictionary);
	// properties
	public bool? DoNotDelete { get; set; }
}
```

### New Type VideoToolbox.VTOnlyTheseFrames

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

### New Type VideoToolbox.VTProfileLevel

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

### New Type VideoToolbox.VTProfileLevelKeys

```
public static class VTProfileLevelKeys {
	// properties
	public static Foundation.NSString H263_Profile0_Level10 { get; }
	public static Foundation.NSString H263_Profile0_Level45 { get; }
	public static Foundation.NSString H263_Profile3_Level45 { get; }
	public static Foundation.NSString H264_Baseline_1_3 { get; }
	public static Foundation.NSString H264_Baseline_3_0 { get; }
	public static Foundation.NSString H264_Baseline_3_1 { get; }
	public static Foundation.NSString H264_Baseline_3_2 { get; }
	public static Foundation.NSString H264_Baseline_4_0 { get; }
	public static Foundation.NSString H264_Baseline_4_1 { get; }
	public static Foundation.NSString H264_Baseline_4_2 { get; }
	public static Foundation.NSString H264_Baseline_5_0 { get; }
	public static Foundation.NSString H264_Baseline_5_1 { get; }
	public static Foundation.NSString H264_Baseline_5_2 { get; }
	public static Foundation.NSString H264_Baseline_AutoLevel { get; }
	public static Foundation.NSString H264_Extended_5_0 { get; }
	public static Foundation.NSString H264_Extended_AutoLevel { get; }
	public static Foundation.NSString H264_High_3_0 { get; }
	public static Foundation.NSString H264_High_3_1 { get; }
	public static Foundation.NSString H264_High_3_2 { get; }
	public static Foundation.NSString H264_High_4_0 { get; }
	public static Foundation.NSString H264_High_4_1 { get; }
	public static Foundation.NSString H264_High_4_2 { get; }
	public static Foundation.NSString H264_High_5_0 { get; }
	public static Foundation.NSString H264_High_5_1 { get; }
	public static Foundation.NSString H264_High_5_2 { get; }
	public static Foundation.NSString H264_High_AutoLevel { get; }
	public static Foundation.NSString H264_Main_3_0 { get; }
	public static Foundation.NSString H264_Main_3_1 { get; }
	public static Foundation.NSString H264_Main_3_2 { get; }
	public static Foundation.NSString H264_Main_4_0 { get; }
	public static Foundation.NSString H264_Main_4_1 { get; }
	public static Foundation.NSString H264_Main_4_2 { get; }
	public static Foundation.NSString H264_Main_5_0 { get; }
	public static Foundation.NSString H264_Main_5_1 { get; }
	public static Foundation.NSString H264_Main_5_2 { get; }
	public static Foundation.NSString H264_Main_AutoLevel { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L0 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L1 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L2 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L3 { get; }
	public static Foundation.NSString MP4V_AdvancedSimple_L4 { get; }
	public static Foundation.NSString MP4V_Main_L2 { get; }
	public static Foundation.NSString MP4V_Main_L3 { get; }
	public static Foundation.NSString MP4V_Main_L4 { get; }
	public static Foundation.NSString MP4V_Simple_L0 { get; }
	public static Foundation.NSString MP4V_Simple_L1 { get; }
	public static Foundation.NSString MP4V_Simple_L2 { get; }
	public static Foundation.NSString MP4V_Simple_L3 { get; }
}
```

### New Type VideoToolbox.VTPropertyKeys

```
public static class VTPropertyKeys {
	// properties
	public static Foundation.NSString DocumentationKey { get; }
	public static Foundation.NSString ReadWriteStatus { get; }
	public static Foundation.NSString ShouldBeSerialized { get; }
	public static Foundation.NSString SupportedValueListKey { get; }
	public static Foundation.NSString SupportedValueMaximumKey { get; }
	public static Foundation.NSString SupportedValueMinimumKey { get; }
	public static Foundation.NSString Type { get; }
}
```

### New Type VideoToolbox.VTPropertyOptions

```
public class VTPropertyOptions : Foundation.DictionaryContainer {
	// constructors
	public VTPropertyOptions ();
	public VTPropertyOptions (Foundation.NSDictionary dictionary);
	// properties
	public Foundation.NSString Documentation { get; set; }
	public VTReadWriteStatus ReadWriteStatus { get; set; }
	public bool? ShouldBeSerialized { get; set; }
	public Foundation.NSNumber[] SupportedValueList { get; set; }
	public Foundation.NSNumber SupportedValueMaximum { get; set; }
	public Foundation.NSNumber SupportedValueMinimum { get; set; }
	public VTPropertyType Type { get; set; }
}
```

### New Type VideoToolbox.VTPropertyReadWriteStatusKeys

```
public static class VTPropertyReadWriteStatusKeys {
	// properties
	public static Foundation.NSString ReadOnly { get; }
	public static Foundation.NSString ReadWrite { get; }
}
```

### New Type VideoToolbox.VTPropertyType

```
[Serializable]
public enum VTPropertyType {
	Boolean = 2,
	Enumeration = 1,
	Number = 3,
	Unset = 0,
}
```

### New Type VideoToolbox.VTPropertyTypeKeys

```
public static class VTPropertyTypeKeys {
	// properties
	public static Foundation.NSString Boolean { get; }
	public static Foundation.NSString Enumeration { get; }
	public static Foundation.NSString Number { get; }
}
```

### New Type VideoToolbox.VTReadWriteStatus

```
[Serializable]
public enum VTReadWriteStatus {
	ReadOnly = 1,
	ReadWrite = 2,
	Unset = 0,
}
```

### New Type VideoToolbox.VTSession

```
public class VTSession : ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	protected VTSession (IntPtr handle);
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~VTSession ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public VTPropertyOptions GetProperties ();
	public Foundation.NSObject GetProperty (Foundation.NSString propertyKey);
	public Foundation.NSDictionary GetSerializableProperties ();
	public Foundation.NSDictionary GetSupportedProperties ();
	public VTStatus SetProperties (VTPropertyOptions options);
	public VTStatus SetProperty (Foundation.NSString propertyKey, Foundation.NSObject value);
}
```

### New Type VideoToolbox.VTStatus

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

### New Type VideoToolbox.VTTransferFunction

```
[Serializable]
public enum VTTransferFunction {
	ItuR7092 = 1,
	Smpte240M1955 = 2,
	Unset = 0,
	UseGamma = 3,
}
```

### New Type VideoToolbox.VTVideoDecoderSpecification

```
public class VTVideoDecoderSpecification : Foundation.DictionaryContainer {
	// constructors
	public VTVideoDecoderSpecification ();
	public VTVideoDecoderSpecification (Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoDecoder { get; set; }
	public bool? RequireHardwareAcceleratedVideoDecoder { get; set; }
}
```

### New Type VideoToolbox.VTVideoDecoderSpecificationKeys

```
public static class VTVideoDecoderSpecificationKeys {
	// properties
	public static Foundation.NSString EnableHardwareAcceleratedVideoDecoder { get; }
	public static Foundation.NSString RequireHardwareAcceleratedVideoDecoder { get; }
}
```

### New Type VideoToolbox.VTVideoEncoder

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

### New Type VideoToolbox.VTVideoEncoderSpecification

```
public class VTVideoEncoderSpecification : Foundation.DictionaryContainer {
	// constructors
	public VTVideoEncoderSpecification ();
	public VTVideoEncoderSpecification (Foundation.NSDictionary dictionary);
	// properties
	public bool? EnableHardwareAcceleratedVideoEncoder { get; set; }
	public string EncoderID { get; set; }
	public bool? RequireHardwareAcceleratedVideoEncoder { get; set; }
}
```

### New Type VideoToolbox.VTVideoEncoderSpecificationKeys

```
public static class VTVideoEncoderSpecificationKeys {
	// properties
	public static Foundation.NSString EnableHardwareAcceleratedVideoEncoder { get; }
	public static Foundation.NSString EncoderID { get; }
	public static Foundation.NSString RequireHardwareAcceleratedVideoEncoder { get; }
}
```

### New Type VideoToolbox.VTYCbCrMatrix

```
[Serializable]
public enum VTYCbCrMatrix {
	ItuR6014 = 2,
	ItuR7092 = 1,
	Smpte240M1955 = 3,
	Unset = 0,
}
```
