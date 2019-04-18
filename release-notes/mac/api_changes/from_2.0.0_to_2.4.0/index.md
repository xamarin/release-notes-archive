---
id: 375D1482-AF0A-4487-8161-AC3A4C0CCA8C
title: "From 2.0.0 to 2.4.0"
---

# XamMac.dll

## Namespace MonoMac

### Type Changed: MonoMac.Constants

Modified fields:

```
public const string Version = "2.0.2" "2.4.0";
```

Added fields:

<pre style='color: green'>
	public static const string ContactsLibrary = "/System/Library/Frameworks/Contacts.framework/Contacts";
	public static const string CoreAudioKitLibrary = "/System/Library/Frameworks/CoreAudioKit.framework/CoreAudioKit";
	public static const string GameplayKitLibrary = "/System/Library/Frameworks/GameplayKit.framework/GameplayKit";
	public static const string MediaToolboxLibrary = "/System/Library/Frameworks/MediaToolbox.framework/MediaToolbox";
	public static const string MetalKitLibrary = "/System/Library/Frameworks/MetalKit.framework/MetalKit";
	public static const string MetalLibrary = "/System/Library/Frameworks/Metal.framework/Metal";
	public static const string ModelIOLibrary = "/System/Library/Frameworks/ModelIO.framework/ModelIO";
	public static const string NetworkExtensionLibrary = "/System/Library/Frameworks/NetworkExtension.framework/NetworkExtension";
	public static const string SdkVersion = "10.11";
	public static const string SearchKitLibrary = "/System/Library/Frameworks/CoreServices.framework/Frameworks/SearchKit.framework/SearchKit";
</pre>

## Namespace MonoMac.Accounts

### Type Changed: MonoMac.Accounts.ACErrorCode

Added values:

<pre style='color: green'>
	CredentialItemNotExpired = 23,
	CredentialItemNotFound = 22,
</pre>

## Namespace MonoMac.AppKit

### Type Changed: MonoMac.AppKit.NSAnimation

Added constructor:

<pre style='color: green'>
	public NSAnimation (double duration, NSAnimationCurve animationCurve);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
	public virtual IntPtr Constant (double duration, NSAnimationCurve animationCurve);
```

### Type Changed: MonoMac.AppKit.NSApplication

Removed interface:

<pre style='color: red'>
	INSWindowRestoration
</pre>

Obsoleted methods:

```
[Obsolete ("This method does nothing")]
	public static void RestoreWindow (string identifier, MonoMac.Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
```

Added methods:

<pre style='color: green'>
	public virtual void CompleteStateRestoration ();
	public virtual void ExtendStateRestoration ();
	public virtual bool RestoreWindowWithIdentifier (string identifier, MonoMac.Foundation.NSCoder state, NSWindowCompletionHandler onCompletion);
</pre>

### Type Changed: MonoMac.AppKit.NSApplicationActivationOptions

Added value:

<pre style='color: green'>
	Default = 0,
</pre>

### Type Changed: MonoMac.AppKit.NSButton

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual int MaxAcceleratorLevel { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSButtonType

Added values:

<pre style='color: green'>
	Accelerator = 8,
	MultiLevelAccelerator = 9,
</pre>

### Type Changed: MonoMac.AppKit.NSCollectionView

Added properties:

<pre style='color: green'>
	public virtual bool AllowsEmptySelection { get; set; }
	public virtual NSView BackgroundView { get; set; }
	public virtual NSCollectionViewLayout CollectionViewLayout { get; set; }
	public virtual NSCollectionViewDataSource DataSource { get; set; }
	public virtual MonoMac.Foundation.NSSet IndexPathsForVisibleItems { get; }
	public virtual int NumberOfSections { get; }
	public virtual MonoMac.Foundation.NSSet SelectionIndexPaths { get; set; }
	public virtual NSCollectionViewItem[] VisibleItems { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void DeleteItems (MonoMac.Foundation.NSSet indexPaths);
	public virtual void DeleteSections (MonoMac.Foundation.NSIndexSet sections);
	public virtual void DeselectAll (MonoMac.Foundation.NSObject sender);
	public virtual void DeselectItems (MonoMac.Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent, ref System.Drawing.PointF dragImageOffset);
	public virtual MonoMac.Foundation.NSIndexPath GetIndexPath (NSCollectionViewItem item);
	public virtual MonoMac.Foundation.NSIndexPath GetIndexPath (System.Drawing.PointF point);
	public virtual MonoMac.Foundation.NSSet GetIndexPaths (string elementKind);
	public virtual NSCollectionViewItem GetItem (MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributes (MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributest (string kind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual int GetNumberOfItems (int section);
	public virtual INSCollectionViewElement GetSupplementaryView (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual INSCollectionViewElement[] GetVisibleSupplementaryViews (MonoMac.Foundation.NSString elementKind);
	public virtual void InsertItems (MonoMac.Foundation.NSSet indexPaths);
	public virtual void InsertSections (MonoMac.Foundation.NSIndexSet sections);
	public virtual NSCollectionViewItem MakeItem (string identifier, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSView MakeSupplementaryView (MonoMac.Foundation.NSString elementKind, string identifier, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void MoveItem (MonoMac.Foundation.NSIndexPath indexPath, MonoMac.Foundation.NSIndexPath newIndexPath);
	public virtual void MoveSection (int section, int newSection);
	public virtual void PerformBatchUpdates (System.Action updates, System.Action&lt;bool&gt; completionHandler);
	public void RegisterClassForItem (System.Type itemClass, string identifier);
	public void RegisterClassForSupplementaryView (System.Type viewClass, MonoMac.Foundation.NSString kind, string identifier);
	public virtual void RegisterNib (NSNib nib, string identifier);
	public virtual void RegisterNib (NSNib nib, MonoMac.Foundation.NSString kind, string identifier);
	public virtual void ReloadData ();
	public virtual void ReloadItems (MonoMac.Foundation.NSSet indexPaths);
	public virtual void ReloadSections (MonoMac.Foundation.NSIndexSet sections);
	public virtual void ScrollToItems (MonoMac.Foundation.NSSet indexPaths, NSCollectionViewScrollPosition scrollPosition);
	public virtual void SelectAll (MonoMac.Foundation.NSObject sender);
	public virtual void SelectItems (MonoMac.Foundation.NSSet indexPaths, NSCollectionViewScrollPosition scrollPosition);
</pre>

### Type Changed: MonoMac.AppKit.NSCollectionViewDelegate

Added methods:

<pre style='color: green'>
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, MonoMac.Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public virtual bool CanDragItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent);
	public virtual void DisplayingItemEnded (NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void DisplayingSupplementaryViewEnded (NSCollectionView collectionView, NSView view, string elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession session, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent, ref System.Drawing.PointF dragImageOffset);
	public virtual string[] GetNamesOfPromisedFiles (NSCollectionView collectionView, MonoMac.Foundation.NSUrl dropURL, MonoMac.Foundation.NSSet indexPaths);
	public virtual INSPasteboardWriting GetPasteboardWriter (NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void ItemsChanged (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual void ItemsDeselected (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual void ItemsSelected (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual MonoMac.Foundation.NSSet ShouldChangeItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual MonoMac.Foundation.NSSet ShouldDeselectItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual MonoMac.Foundation.NSSet ShouldSelectItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual NSCollectionViewTransitionLayout TransitionLayout (NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out MonoMac.Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public virtual void WillDisplayItem (NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (NSCollectionView collectionView, NSView view, MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual bool WriteItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSPasteboard pasteboard);
</pre>

### Type Changed: MonoMac.AppKit.NSCollectionViewDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static bool AcceptDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, MonoMac.Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public static bool CanDragItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent);
	public static void DisplayingItemEnded (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public static void DisplayingSupplementaryViewEnded (INSCollectionViewDelegate This, NSCollectionView collectionView, NSView view, string elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public static void DraggingSessionWillBegin (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingSession session, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSSet indexPaths);
	public static NSImage GetDraggingImage (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent, ref System.Drawing.PointF dragImageOffset);
	public static string[] GetNamesOfPromisedFiles (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSUrl dropURL, MonoMac.Foundation.NSSet indexPaths);
	public static INSPasteboardWriting GetPasteboardWriter (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath indexPath);
	public static void ItemsChanged (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public static void ItemsDeselected (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public static void ItemsSelected (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public static MonoMac.Foundation.NSSet ShouldChangeItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public static MonoMac.Foundation.NSSet ShouldDeselectItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public static MonoMac.Foundation.NSSet ShouldSelectItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public static NSCollectionViewTransitionLayout TransitionLayout (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public static NSDragOperation ValidateDrop (INSCollectionViewDelegate This, NSCollectionView collectionView, NSDraggingInfo draggingInfo, out MonoMac.Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public static void WillDisplayItem (INSCollectionViewDelegate This, NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public static void WillDisplaySupplementaryView (INSCollectionViewDelegate This, NSCollectionView collectionView, NSView view, MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public static bool WriteItems (INSCollectionViewDelegate This, NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSPasteboard pasteboard);
</pre>

### Type Changed: MonoMac.AppKit.NSCollectionViewItem

Added property:

<pre style='color: green'>
	public virtual NSCollectionViewItemHighlightState HighlightState { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSColor

Obsoleted properties:

```
[Obsolete ("Use UnderPageBackgroundColor instead")]
	public static NSColor UnderPageBackground { get; }
```

### Type Changed: MonoMac.AppKit.NSColorList

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.AppKit.NSComboBox

Added property:

<pre style='color: green'>
	public MonoMac.Foundation.NSObject Item { get; }
</pre>

Obsoleted methods:

```
[Obsolete ("Use GetItemObject instead")]
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

### Type Changed: MonoMac.AppKit.NSDraggingInfo

Added property:

<pre style='color: green'>
	public virtual NSSpringLoadingHighlight SpringLoadingHighlight { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ResetSpringLoading ();
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

### Type Changed: MonoMac.AppKit.NSFont

Added methods:

<pre style='color: green'>
	public static NSFont MonospacedDigitSystemFontOfSize (float fontSize, float weight);
	public static NSFont SystemFontOfSize (float fontSize, float weight);
</pre>

### Type Changed: MonoMac.AppKit.NSGestureEvent

Modified methods:

```
public virtual System.IAsyncResult BeginInvoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent theEvent, System.AsyncCallback callback, object object)
	public virtual bool Invoke (NSGestureRecognizer gestureRecognizer, NSEvent gestureEvent theEvent)
```

### Type Changed: MonoMac.AppKit.NSGestureRecognizer

Added properties:

<pre style='color: green'>
	public virtual NSPressureConfiguration PressureConfiguration { get; set; }
	public NSGestureEvent ShouldAttemptToRecognize { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSGestureRecognizerDelegate

Added method:

<pre style='color: green'>
	public virtual bool ShouldAttemptToRecognize (NSGestureRecognizer gestureRecognizer, NSEvent theEvent);
</pre>

### Type Changed: MonoMac.AppKit.NSGestureRecognizerDelegate_Extensions

Added method:

<pre style='color: green'>
	public static bool ShouldAttemptToRecognize (INSGestureRecognizerDelegate This, NSGestureRecognizer gestureRecognizer, NSEvent theEvent);
</pre>

### Type Changed: MonoMac.AppKit.NSGraphics

Added methods:

<pre style='color: green'>
	public static void DisableScreenUpdates ();
	public static void DrawWindowBackground (System.Drawing.RectangleF aRect);
	public static void EnableScreenUpdates ();
</pre>

### Type Changed: MonoMac.AppKit.NSLayoutAttribute

Added values:

<pre style='color: green'>
	FirstBaseline = 12,
	LastBaseline = 11,
</pre>

### Type Changed: MonoMac.AppKit.NSLayoutFormatOptions

Added values:

<pre style='color: green'>
	AlignAllFirstBaseline = 4096,
	AlignAllLastBaseline = 2048,
</pre>

### Type Changed: MonoMac.AppKit.NSLayoutManager

Added methods:

<pre style='color: green'>
	public virtual void EnumerateEnclosingRects (MonoMac.Foundation.NSRange glyphRange, MonoMac.Foundation.NSRange selectedRange, NSTextContainer textContainer, NSTextLayoutEnumerateEnclosingRects callback);
	public virtual void EnumerateLineFragments (MonoMac.Foundation.NSRange glyphRange, NSTextLayoutEnumerateLineFragments callback);
	public virtual ushort GetCGGlyph (uint glyphIndex);
	public virtual ushort GetCGGlyph (uint glyphIndex, out bool isValidIndex);
	public virtual NSGlyphProperty GetProperty (uint glyphIndex);
	public virtual MonoMac.Foundation.NSRange GetTruncatedGlyphRangeInLineFragment (uint glyphIndex);
	public virtual void ProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editMask, MonoMac.Foundation.NSRange newCharRange, int delta, MonoMac.Foundation.NSRange invalidatedCharRange);
	public virtual void SetGlyphs (IntPtr glyphs, IntPtr props, IntPtr charIndexes, NSFont aFont, MonoMac.Foundation.NSRange glyphRange);
</pre>

### Type Changed: MonoMac.AppKit.NSLayoutManagerDelegate

Added methods:

<pre style='color: green'>
	public virtual void DidChangeGeometry (NSLayoutManager layoutManager, NSTextContainer textContainer, System.Drawing.SizeF oldSize);
	public virtual System.Drawing.RectangleF GetBoundingBox (NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, System.Drawing.RectangleF proposedRect, System.Drawing.PointF glyphPosition, uint charIndex);
	public virtual float GetLineSpacingAfterGlyph (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual float GetParagraphSpacingAfterGlyph (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual float GetParagraphSpacingBeforeGlyph (NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public virtual bool ShouldBreakLineByHyphenatingBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual bool ShouldBreakLineByWordBeforeCharacter (NSLayoutManager layoutManager, uint charIndex);
	public virtual uint ShouldGenerateGlyphs (NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, NSFont aFont, MonoMac.Foundation.NSRange glyphRange);
	public virtual NSControlCharacterAction ShouldUseAction (NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
</pre>

### Type Changed: MonoMac.AppKit.NSLayoutManagerDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void DidChangeGeometry (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSTextContainer textContainer, System.Drawing.SizeF oldSize);
	public static System.Drawing.RectangleF GetBoundingBox (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, NSTextContainer textContainer, System.Drawing.RectangleF proposedRect, System.Drawing.PointF glyphPosition, uint charIndex);
	public static float GetLineSpacingAfterGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static float GetParagraphSpacingAfterGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static float GetParagraphSpacingBeforeGlyph (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint glyphIndex, System.Drawing.RectangleF rect);
	public static bool ShouldBreakLineByHyphenatingBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static bool ShouldBreakLineByWordBeforeCharacter (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, uint charIndex);
	public static uint ShouldGenerateGlyphs (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, IntPtr glyphBuffer, IntPtr props, IntPtr charIndexes, NSFont aFont, MonoMac.Foundation.NSRange glyphRange);
	public static NSControlCharacterAction ShouldUseAction (INSLayoutManagerDelegate This, NSLayoutManager layoutManager, NSControlCharacterAction action, uint charIndex);
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

### Type Changed: MonoMac.AppKit.NSMenu

Added property:

<pre style='color: green'>
	public virtual NSUserInterfaceLayoutDirection UserInterfaceLayoutDirection { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSMutableParagraphStyle

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSOutlineView

Added method:

<pre style='color: green'>
	public virtual int GetChildIndex (MonoMac.Foundation.NSObject item);
</pre>

### Type Changed: MonoMac.AppKit.NSOutlineViewDelegate

Obsoleted methods:

```
[Obsolete ("Use GetView instead")]
	public virtual NSView ViewForTableColumn (NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
```

### Type Changed: MonoMac.AppKit.NSOutlineViewDelegate_Extensions

Obsoleted methods:

```
[Obsolete ("Use GetView instead")]
	public static NSView ViewForTableColumn (INSOutlineViewDelegate This, NSOutlineView outlineView, NSTableColumn tableColumn, MonoMac.Foundation.NSObject item);
```

### Type Changed: MonoMac.AppKit.NSParagraphStyle

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; }
</pre>

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

### Type Changed: MonoMac.AppKit.NSPopover

Added property:

<pre style='color: green'>
	public virtual bool Detached { get; }
</pre>

### Type Changed: MonoMac.AppKit.NSPopoverDelegate

Added method:

<pre style='color: green'>
	public virtual void DidDetach (NSPopover popover);
</pre>

### Type Changed: MonoMac.AppKit.NSPopoverDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DidDetach (INSPopoverDelegate This, NSPopover popover);
</pre>

### Type Changed: MonoMac.AppKit.NSSearchField

Added properties:

<pre style='color: green'>
	public virtual bool CentersPlaceholder { get; set; }
	public NSSearchFieldDelegate Delegate { get; set; }
	public virtual MonoMac.Foundation.NSObject WeakDelegate { get; set; }
</pre>

Added events:

<pre style='color: green'>
	public event System.EventHandler SearchingEnded;
	public event System.EventHandler SearchingStarted;
</pre>

Added methods:

<pre style='color: green'>
	public virtual System.Drawing.RectangleF GetRectForCancelButton (bool isCentered);
	public virtual System.Drawing.RectangleF GetRectForSearchButton (bool isCentered);
	public virtual System.Drawing.RectangleF GetRectForSearchText (bool isCentered);
</pre>

### Type Changed: MonoMac.AppKit.NSSegmentedControl

Added properties:

<pre style='color: green'>
	public virtual bool IsSpringLoaded { get; set; }
	public virtual NSSegmentSwitchTracking TrackingMode { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual double GetValueForSelectedSegment ();
</pre>

### Type Changed: MonoMac.AppKit.NSSegmentSwitchTracking

Added value:

<pre style='color: green'>
	MomentaryAccelerator = 3,
</pre>

### Type Changed: MonoMac.AppKit.NSSplitView

Added properties:

<pre style='color: green'>
	public virtual NSView[] ArrangedSubviews { get; }
	public virtual bool ArrangesAllSubviews { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddArrangedSubview (NSView view);
	public virtual void InsertArrangedSubview (NSView view, int index);
	public virtual void RemoveArrangedSubview (NSView view);
</pre>

### Type Changed: MonoMac.AppKit.NSSplitViewController

Added properties:

<pre style='color: green'>
	public static float AutomaticDimension { get; }
	public virtual float MinimumThicknessForInlineSidebars { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void ToggleSidebar (MonoMac.Foundation.NSObject sender);
</pre>

### Type Changed: MonoMac.AppKit.NSSplitViewItem

Added properties:

<pre style='color: green'>
	public virtual float AutomaticMaximumThickness { get; set; }
	public virtual NSSplitViewItemBehavior Behavior { get; }
	public virtual float MaximumThickness { get; set; }
	public virtual float MinimumThickness { get; set; }
	public virtual float PreferredThicknessFraction { get; set; }
	public virtual bool SpringLoaded { get; set; }
	public static float UnspecifiedDimension { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSSplitViewItem CreateContentList (NSViewController viewController);
	public static NSSplitViewItem CreateSidebar (NSViewController viewController);
</pre>

### Type Changed: MonoMac.AppKit.NSStackView

Added properties:

<pre style='color: green'>
	public virtual NSView[] ArrangedSubviews { get; }
	public virtual bool DetachesHiddenViews { get; set; }
	public virtual NSStackViewDistribution Distribution { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddArrangedSubview (NSView view);
	public virtual void InsertArrangedSubview (NSView view, int index);
	public virtual void RemoveArrangedSubview (NSView view);
</pre>

### Type Changed: MonoMac.AppKit.NSTableView

Added properties:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSIndexSet HiddenRowIndexes { get; }
	public NSTableViewRowActionsGetter RowActions { get; set; }
	public virtual bool RowActionsVisible { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void HideRows (MonoMac.Foundation.NSIndexSet indexes, NSTableViewAnimation rowAnimation);
	public virtual void UnhideRows (MonoMac.Foundation.NSIndexSet indexes, NSTableViewAnimation rowAnimation);
</pre>

### Type Changed: MonoMac.AppKit.NSTableViewDelegate

Added method:

<pre style='color: green'>
	public virtual NSTableViewRowAction[] RowActions (NSTableView tableView, int row, NSTableRowActionEdge edge);
</pre>

### Type Changed: MonoMac.AppKit.NSTableViewDelegate_Extensions

Added method:

<pre style='color: green'>
	public static NSTableViewRowAction[] RowActions (INSTableViewDelegate This, NSTableView tableView, int row, NSTableRowActionEdge edge);
</pre>

### Type Changed: MonoMac.AppKit.NSTableViewSource

Removed interface:

<pre style='color: red'>
	INSTableViewSource
</pre>

### Type Changed: MonoMac.AppKit.NSTextAttachment

Added constructor:

<pre style='color: green'>
	public NSTextAttachment (MonoMac.Foundation.NSData contentData, string uti);
</pre>

Added properties:

<pre style='color: green'>
	public virtual System.Drawing.RectangleF Bounds { get; set; }
	public virtual MonoMac.Foundation.NSData Contents { get; set; }
	public virtual string FileType { get; set; }
	public virtual NSImage Image { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSTextContainer

Added properties:

<pre style='color: green'>
	public virtual NSBezierPath[] ExclusionPaths { get; set; }
	public virtual NSLineBreakMode LineBreakMode { get; set; }
	public virtual uint MaximumNumberOfLines { get; set; }
	public virtual System.Drawing.SizeF Size { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSTextContainer FromContainerSize (System.Drawing.SizeF containerSize);
	public static NSTextContainer FromSize (System.Drawing.SizeF size);
	public virtual System.Drawing.RectangleF GetLineFragmentRect (System.Drawing.RectangleF proposedRect, uint characterIndex, NSWritingDirection baseWritingDirection, ref System.Drawing.RectangleF remainingRect);
</pre>

### Type Changed: MonoMac.AppKit.NSTextField

Added properties:

<pre style='color: green'>
	public virtual bool AllowsDefaultTighteningForTruncation { get; set; }
	public virtual int MaximumNumberOfLines { get; set; }
</pre>

### Type Changed: MonoMac.AppKit.NSTextStorage

Added events:

<pre style='color: green'>
	public event System.EventHandler&lt;NSTextStorageEventArgs&gt; DidProcessEditing;
	public event System.EventHandler&lt;NSTextStorageEventArgs&gt; WillProcessEditing;
</pre>

### Type Changed: MonoMac.AppKit.NSTextStorageDelegate

Added methods:

<pre style='color: green'>
	public virtual void DidProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoMac.Foundation.NSRange editedRange, int delta);
	public virtual void WillProcessEditing (NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoMac.Foundation.NSRange editedRange, int delta);
</pre>

### Type Changed: MonoMac.AppKit.NSTextStorageDelegate_Extensions

Added methods:

<pre style='color: green'>
	public static void DidProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoMac.Foundation.NSRange editedRange, int delta);
	public static void WillProcessEditing (INSTextStorageDelegate This, NSTextStorage textStorage, NSTextStorageEditActions editedMask, MonoMac.Foundation.NSRange editedRange, int delta);
</pre>

### Type Changed: MonoMac.AppKit.NSTextTab

Added method:

<pre style='color: green'>
	public static MonoMac.Foundation.NSCharacterSet GetColumnTerminators (MonoMac.Foundation.NSLocale locale);
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

### Type Changed: MonoMac.AppKit.NSUnderlineStyle

Added values:

<pre style='color: green'>
	ByWord = 32768,
	PatternDash = 512,
	PatternDashDot = 768,
	PatternDashDotDot = 1024,
	PatternDot = 256,
	PatternSolid = 0,
</pre>

### Type Changed: MonoMac.AppKit.NSView

Added properties:

<pre style='color: green'>
	public virtual float FirstBaselineOffsetFromTop { get; }
	public virtual float LastBaselineOffsetFromBottom { get; }
	public virtual NSLayoutGuide[] LayoutGuides { get; }
	public static float NoIntrinsicMetric { get; }
	public virtual NSPressureConfiguration PressureConfiguration { get; set; }
</pre>

Modified methods:

```
public virtual NSDraggingSession BeginDraggingSession (NSDraggingItem[] itmes items, NSEvent evnt, NSDraggingSource source)
```

Added methods:

<pre style='color: green'>
	public virtual void AddLayoutGuide (NSLayoutGuide guide);
	public virtual void BeginDocument ();
	public virtual void BeginPage (System.Drawing.RectangleF rect, System.Drawing.PointF placement);
	public virtual void DidCloseMenu (NSMenu menu, NSEvent theEvent);
	public virtual void EndDocument ();
	public virtual void EndPage ();
	public virtual void RemoveLayoutGuide (NSLayoutGuide guide);
	public virtual void WillOpenMenu (NSMenu menu, NSEvent theEvent);
</pre>

### Type Changed: MonoMac.AppKit.NSWindow

Added properties:

<pre style='color: green'>
	public virtual System.Drawing.SizeF MaxFullScreenContentSize { get; set; }
	public virtual System.Drawing.SizeF MinFullScreenContentSize { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void PerformWindowDrag (NSEvent theEvent);
</pre>

### Type Changed: MonoMac.AppKit.NSWindowCollectionBehavior

Added values:

<pre style='color: green'>
	FullScreenAllowsTiling = 2048,
	FullScreenDisallowsTiling = 4096,
</pre>

### Type Changed: MonoMac.AppKit.NSWorkspace

Added method:

<pre style='color: green'>
	public virtual bool OpenUrls (MonoMac.Foundation.NSUrl[] urls, string bundleIdentifier, NSWorkspaceLaunchOptions options, MonoMac.Foundation.NSAppleEventDescriptor descriptor);
</pre>

### Removed Type  <span style='color: red'>MonoMac.AppKit.INSTableViewSource</span>

### Removed Type  <span style='color: red'>MonoMac.AppKit.NSTableViewSource_Extensions</span>

### New Type MonoMac.AppKit.INSAlignmentFeedbackToken

<pre style='color: green'>
public interface INSAlignmentFeedbackToken : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.INSCollectionViewDataSource

<pre style='color: green'>
public interface INSCollectionViewDataSource : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual NSCollectionViewItem GetItem (NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual int GetNumberofItems (NSCollectionView collectionView, int section);
}
</pre>

### New Type MonoMac.AppKit.INSCollectionViewDelegateFlowLayout

<pre style='color: green'>
public interface INSCollectionViewDelegateFlowLayout : INSCollectionViewDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.INSCollectionViewElement

<pre style='color: green'>
public interface INSCollectionViewElement : INSUserInterfaceItemIdentification, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.INSHapticFeedbackPerformer

<pre style='color: green'>
public interface INSHapticFeedbackPerformer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void PerformFeedback (NSHapticFeedbackPattern pattern, NSHapticFeedbackPerformanceTime performanceTime);
}
</pre>

### New Type MonoMac.AppKit.INSSearchFieldDelegate

<pre style='color: green'>
public interface INSSearchFieldDelegate : INSTextFieldDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.INSSpringLoadingDestination

<pre style='color: green'>
public interface INSSpringLoadingDestination : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Activated (bool activated, NSDraggingInfo draggingInfo);
	public virtual void HighlightChanged (NSDraggingInfo draggingInfo);
}
</pre>

### New Type MonoMac.AppKit.INSTextAttachmentContainer

<pre style='color: green'>
public interface INSTextAttachmentContainer : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF lineFrag, System.Drawing.PointF position, uint charIndex);
	public virtual NSImage GetImage (System.Drawing.RectangleF imageBounds, NSTextContainer textContainer, uint charIndex);
}
</pre>

### New Type MonoMac.AppKit.INSTextInputClient

<pre style='color: green'>
public interface INSTextInputClient : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.AppKit.NSAlignmentFeedbackFilter

<pre style='color: green'>
public class NSAlignmentFeedbackFilter : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAlignmentFeedbackFilter ();
	public NSAlignmentFeedbackFilter (MonoMac.Foundation.NSCoder coder);
	public NSAlignmentFeedbackFilter (MonoMac.Foundation.NSObjectFlag t);
	public NSAlignmentFeedbackFilter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static NSEventMask InputEventMask { get; }
	// methods
	public virtual INSAlignmentFeedbackToken GetTokenForHorizontalMovement (NSView view, float previousX, float alignedX, float defaultX);
	public virtual INSAlignmentFeedbackToken GetTokenForMovement (NSView view, System.Drawing.PointF previousPoint, System.Drawing.PointF alignedPoint, System.Drawing.PointF defaultPoint);
	public virtual INSAlignmentFeedbackToken GetTokenForVerticalMovement (NSView view, float previousY, float alignedY, float defaultY);
	public virtual void PerformFeedback (INSAlignmentFeedbackToken[] tokens, NSHapticFeedbackPerformanceTime performanceTime);
	public virtual void Update (NSEvent theEvent);
	public virtual void Update (NSPanGestureRecognizer panRecognizer);
}
</pre>

### New Type MonoMac.AppKit.NSAlignmentFeedbackToken

<pre style='color: green'>
public class NSAlignmentFeedbackToken : MonoMac.Foundation.NSObject, INSAlignmentFeedbackToken, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSAlignmentFeedbackToken ();
	public NSAlignmentFeedbackToken (MonoMac.Foundation.NSCoder coder);
	public NSAlignmentFeedbackToken (MonoMac.Foundation.NSObjectFlag t);
	public NSAlignmentFeedbackToken (IntPtr handle);
}
</pre>

### New Type MonoMac.AppKit.NSAlignmentFeedbackToken_Extensions

<pre style='color: green'>
public static class NSAlignmentFeedbackToken_Extensions {
}
</pre>

### New Type MonoMac.AppKit.NSAttributedString_NSExtendedStringDrawing

<pre style='color: green'>
public static class NSAttributedString_NSExtendedStringDrawing {
	// methods
	public static System.Drawing.RectangleF BoundingRectWithSize (MonoMac.Foundation.NSAttributedString This, System.Drawing.SizeF size, MonoMac.Foundation.NSStringDrawingOptions options, NSStringDrawingContext context);
	public static void DrawWithRect (MonoMac.Foundation.NSAttributedString This, System.Drawing.RectangleF rect, MonoMac.Foundation.NSStringDrawingOptions options, NSStringDrawingContext context);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionElementCategory

<pre style='color: green'>
[Serializable]
public enum NSCollectionElementCategory {
	DecorationView = 2,
	InterItemGap = 3,
	Item = 0,
	SupplementaryView = 1,
}
</pre>

### New Type MonoMac.AppKit.NSCollectionElementKind

<pre style='color: green'>
public static class NSCollectionElementKind {
	// properties
	public static MonoMac.Foundation.NSString InterItemGapIndicator { get; }
	public static MonoMac.Foundation.NSString SectionFooter { get; }
	public static MonoMac.Foundation.NSString SectionHeader { get; }
}
</pre>

### New Type MonoMac.AppKit.NSCollectionUpdateAction

<pre style='color: green'>
[Serializable]
public enum NSCollectionUpdateAction {
	Delete = 1,
	Insert = 0,
	Move = 3,
	None = 4,
	Reload = 2,
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewDataSource

<pre style='color: green'>
public abstract class NSCollectionViewDataSource : MonoMac.Foundation.NSObject, INSCollectionViewDataSource, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewDataSource ();
	public NSCollectionViewDataSource (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewDataSource (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewDataSource (IntPtr handle);
	// methods
	public virtual NSCollectionViewItem GetItem (NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual int GetNumberofItems (NSCollectionView collectionView, int section);
	public virtual int GetNumberOfSections (NSCollectionView collectionView);
	public virtual NSView GetView (NSCollectionView collectionView, MonoMac.Foundation.NSString kind, MonoMac.Foundation.NSIndexPath indexPath);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewDataSource_Extensions

<pre style='color: green'>
public static class NSCollectionViewDataSource_Extensions {
	// methods
	public static int GetNumberOfSections (INSCollectionViewDataSource This, NSCollectionView collectionView);
	public static NSView GetView (INSCollectionViewDataSource This, NSCollectionView collectionView, MonoMac.Foundation.NSString kind, MonoMac.Foundation.NSIndexPath indexPath);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewDelegateFlowLayout

<pre style='color: green'>
public class NSCollectionViewDelegateFlowLayout : MonoMac.Foundation.NSObject, INSCollectionViewDelegate, INSCollectionViewDelegateFlowLayout, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewDelegateFlowLayout ();
	public NSCollectionViewDelegateFlowLayout (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewDelegateFlowLayout (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewDelegateFlowLayout (IntPtr handle);
	// methods
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, MonoMac.Foundation.NSIndexPath indexPath, NSCollectionViewDropOperation dropOperation);
	public virtual bool AcceptDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, int index, NSCollectionViewDropOperation dropOperation);
	public virtual bool CanDragItems (NSCollectionView collectionView, MonoMac.Foundation.NSIndexSet indexes, NSEvent evt);
	public virtual bool CanDragItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent);
	public virtual void DisplayingItemEnded (NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void DisplayingSupplementaryViewEnded (NSCollectionView collectionView, NSView view, string elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void DraggingSessionEnded (NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, NSDragOperation dragOperation);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession draggingSession, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSIndexSet indexes);
	public virtual void DraggingSessionWillBegin (NSCollectionView collectionView, NSDraggingSession session, System.Drawing.PointF screenPoint, MonoMac.Foundation.NSSet indexPaths);
	public virtual NSImage GetDraggingImage (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSEvent theEvent, ref System.Drawing.PointF dragImageOffset);
	public virtual string[] GetNamesOfPromisedFiles (NSCollectionView collectionView, MonoMac.Foundation.NSUrl dropURL, MonoMac.Foundation.NSSet indexPaths);
	public virtual INSPasteboardWriting GetPasteboardWriter (NSCollectionView collectionView, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSEdgeInsets InsetForSection (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public virtual void ItemsChanged (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual void ItemsDeselected (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual void ItemsSelected (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual float MinimumInteritemSpacingForSection (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public virtual float MinimumLineSpacing (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public virtual string[] NamesOfPromisedFilesDroppedAtDestination (NSCollectionView collectionView, MonoMac.Foundation.NSUrl dropUrl, MonoMac.Foundation.NSIndexSet indexes);
	public virtual NSPasteboardWriting PasteboardWriterForItemAtIndex (NSCollectionView collectionView, uint index);
	public virtual System.Drawing.SizeF ReferenceSizeForFooter (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public virtual System.Drawing.SizeF ReferenceSizeForHeader (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public virtual MonoMac.Foundation.NSSet ShouldChangeItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSCollectionViewItemHighlightState highlightState);
	public virtual MonoMac.Foundation.NSSet ShouldDeselectItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual MonoMac.Foundation.NSSet ShouldSelectItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths);
	public virtual System.Drawing.SizeF SizeForItem (NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewTransitionLayout TransitionLayout (NSCollectionView collectionView, NSCollectionViewLayout fromLayout, NSCollectionViewLayout toLayout);
	public virtual void UpdateDraggingItemsForDrag (NSCollectionView collectionView, NSDraggingInfo draggingInfo);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, out MonoMac.Foundation.NSIndexPath proposedDropIndexPath, out NSCollectionViewDropOperation proposedDropOperation);
	public virtual NSDragOperation ValidateDrop (NSCollectionView collectionView, NSDraggingInfo draggingInfo, ref int dropIndex, NSCollectionViewDropOperation dropOperation);
	public virtual void WillDisplayItem (NSCollectionView collectionView, NSCollectionViewItem item, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual void WillDisplaySupplementaryView (NSCollectionView collectionView, NSView view, MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual bool WriteItems (NSCollectionView collectionView, MonoMac.Foundation.NSIndexSet indexes, NSPasteboard toPasteboard);
	public virtual bool WriteItems (NSCollectionView collectionView, MonoMac.Foundation.NSSet indexPaths, NSPasteboard pasteboard);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewDelegateFlowLayout_Extensions

<pre style='color: green'>
public static class NSCollectionViewDelegateFlowLayout_Extensions {
	// methods
	public static NSEdgeInsets InsetForSection (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public static float MinimumInteritemSpacingForSection (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public static float MinimumLineSpacing (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public static System.Drawing.SizeF ReferenceSizeForFooter (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public static System.Drawing.SizeF ReferenceSizeForHeader (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, int section);
	public static System.Drawing.SizeF SizeForItem (INSCollectionViewDelegateFlowLayout This, NSCollectionView collectionView, NSCollectionViewLayout collectionViewLayout, MonoMac.Foundation.NSIndexPath indexPath);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewElement

<pre style='color: green'>
public class NSCollectionViewElement : MonoMac.Foundation.NSObject, INSCollectionViewElement, INSUserInterfaceItemIdentification, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewElement ();
	public NSCollectionViewElement (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewElement (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewElement (IntPtr handle);
	// properties
	public virtual string Identifier { get; set; }
	// methods
	public virtual void ApplyLayoutAttributes (NSCollectionViewLayoutAttributes layoutAttributes);
	public virtual void DidTransition (NSCollectionViewLayout oldLayout, NSCollectionViewLayout newLayout);
	public virtual NSCollectionViewLayoutAttributes GetPreferredLayoutAttributes (NSCollectionViewLayoutAttributes layoutAttributes);
	public virtual void PrepareForReuse ();
	public virtual void WillTransition (NSCollectionViewLayout oldLayout, NSCollectionViewLayout newLayout);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewElement_Extensions

<pre style='color: green'>
public static class NSCollectionViewElement_Extensions {
	// methods
	public static void ApplyLayoutAttributes (INSCollectionViewElement This, NSCollectionViewLayoutAttributes layoutAttributes);
	public static void DidTransition (INSCollectionViewElement This, NSCollectionViewLayout oldLayout, NSCollectionViewLayout newLayout);
	public static NSCollectionViewLayoutAttributes GetPreferredLayoutAttributes (INSCollectionViewElement This, NSCollectionViewLayoutAttributes layoutAttributes);
	public static void PrepareForReuse (INSCollectionViewElement This);
	public static void WillTransition (INSCollectionViewElement This, NSCollectionViewLayout oldLayout, NSCollectionViewLayout newLayout);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewFlowLayout

<pre style='color: green'>
public class NSCollectionViewFlowLayout : MonoMac.AppKit.NSCollectionViewLayout, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewFlowLayout ();
	public NSCollectionViewFlowLayout (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewFlowLayout (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewFlowLayout (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.SizeF EstimatedItemSize { get; set; }
	public virtual System.Drawing.SizeF FooterReferenceSize { get; set; }
	public virtual System.Drawing.SizeF HeaderReferenceSize { get; set; }
	public virtual System.Drawing.SizeF ItemSize { get; set; }
	public virtual float MinimumInteritemSpacing { get; set; }
	public virtual float MinimumLineSpacing { get; set; }
	public virtual NSCollectionViewScrollDirection ScrollDirection { get; set; }
	public virtual NSEdgeInsets SectionInset { get; set; }
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewFlowLayoutInvalidationContext

<pre style='color: green'>
public class NSCollectionViewFlowLayoutInvalidationContext : MonoMac.AppKit.NSCollectionViewLayoutInvalidationContext, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewFlowLayoutInvalidationContext ();
	public NSCollectionViewFlowLayoutInvalidationContext (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewFlowLayoutInvalidationContext (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewFlowLayoutInvalidationContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool InvalidateFlowLayoutAttributes { get; set; }
	public virtual bool InvalidateFlowLayoutDelegateMetrics { get; set; }
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewGridLayout

<pre style='color: green'>
public class NSCollectionViewGridLayout : MonoMac.AppKit.NSCollectionViewLayout, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewGridLayout ();
	public NSCollectionViewGridLayout (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewGridLayout (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewGridLayout (IntPtr handle);
	// properties
	public virtual NSColor[] BackgroundColors { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual NSEdgeInsets Margins { get; set; }
	public virtual System.Drawing.SizeF MaximumItemSize { get; set; }
	public virtual uint MaximumNumberOfColumns { get; set; }
	public virtual uint MaximumNumberOfRows { get; set; }
	public virtual float MinimumInteritemSpacing { get; set; }
	public virtual System.Drawing.SizeF MinimumItemSize { get; set; }
	public virtual float MinimumLineSpacing { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewItemHighlightState

<pre style='color: green'>
[Serializable]
public enum NSCollectionViewItemHighlightState {
	AsDropTarget = 3,
	ForDeselection = 2,
	ForSelection = 1,
	None = 0,
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewLayout

<pre style='color: green'>
public class NSCollectionViewLayout : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewLayout ();
	public NSCollectionViewLayout (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewLayout (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewLayout (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSCollectionView CollectionView { get; }
	public virtual System.Drawing.SizeF CollectionViewContentSize { get; }
	public static MonoMac.ObjCRuntime.Class InvalidationContextClass { get; }
	public static MonoMac.ObjCRuntime.Class LayoutAttributesClass { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void FinalizeAnimatedBoundsChange ();
	public virtual void FinalizeCollectionViewUpdates ();
	public virtual void FinalizeLayoutTransition ();
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingDecorationElement (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath decorationIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingItem (MonoMac.Foundation.NSIndexPath itemIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetFinalLayoutAttributesForDisappearingSupplementaryElement (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath elementIndexPath);
	public virtual MonoMac.Foundation.NSSet GetIndexPathsToDeleteForDecorationView (MonoMac.Foundation.NSString elementKind);
	public virtual MonoMac.Foundation.NSSet GetIndexPathsToDeleteForSupplementaryView (MonoMac.Foundation.NSString elementKind);
	public virtual MonoMac.Foundation.NSSet GetIndexPathsToInsertForDecorationView (MonoMac.Foundation.NSString elementKind);
	public virtual MonoMac.Foundation.NSSet GetIndexPathsToInsertForSupplementaryView (MonoMac.Foundation.NSString elementKind);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingDecorationElement (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath decorationIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingItem (MonoMac.Foundation.NSIndexPath itemIndexPath);
	public virtual NSCollectionViewLayoutAttributes GetInitialLayoutAttributesForAppearingSupplementaryElement (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath elementIndexPath);
	public virtual NSCollectionViewLayoutInvalidationContext GetInvalidationContext (System.Drawing.RectangleF newBounds);
	public virtual NSCollectionViewLayoutInvalidationContext GetInvalidationContext (NSCollectionViewLayoutAttributes preferredAttributes, NSCollectionViewLayoutAttributes originalAttributes);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForDecorationView (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForDropTarget (System.Drawing.PointF pointInCollectionView);
	public virtual NSCollectionViewLayoutAttributes[] GetLayoutAttributesForElements (System.Drawing.RectangleF rect);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForInterItemGap (MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForItem (MonoMac.Foundation.NSIndexPath indexPath);
	public virtual NSCollectionViewLayoutAttributes GetLayoutAttributesForSupplementaryView (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	public virtual System.Drawing.PointF GetTargetContentOffset (System.Drawing.PointF proposedContentOffset);
	public virtual System.Drawing.PointF GetTargetContentOffset (System.Drawing.PointF proposedContentOffset, System.Drawing.PointF velocity);
	public virtual void InvalidateLayout ();
	public virtual void InvalidateLayout (NSCollectionViewLayoutInvalidationContext context);
	public virtual void PrepareForAnimatedBoundsChange (System.Drawing.RectangleF oldBounds);
	public virtual void PrepareForCollectionViewUpdates (NSCollectionViewUpdateItem[] updateItems);
	public virtual void PrepareForTransitionFromLayout (NSCollectionViewLayout oldLayout);
	public virtual void PrepareForTransitionToLayout (NSCollectionViewLayout newLayout);
	public virtual void PrepareLayout ();
	public void RegisterClassForDecorationView (System.Type itemClass, MonoMac.Foundation.NSString elementKind);
	public virtual void RegisterNib (NSNib nib, MonoMac.Foundation.NSString elementKind);
	public virtual bool ShouldInvalidateLayout (System.Drawing.RectangleF newBounds);
	public virtual bool ShouldInvalidateLayout (NSCollectionViewLayoutAttributes preferredAttributes, NSCollectionViewLayoutAttributes originalAttributes);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewLayoutAttributes

<pre style='color: green'>
public class NSCollectionViewLayoutAttributes : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewLayoutAttributes ();
	public NSCollectionViewLayoutAttributes (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewLayoutAttributes (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewLayoutAttributes (IntPtr handle);
	// properties
	public virtual float Alpha { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF Frame { get; set; }
	public virtual bool Hidden { get; set; }
	public virtual MonoMac.Foundation.NSIndexPath IndexPath { get; set; }
	public virtual NSCollectionElementCategory RepresentedElementCategory { get; }
	public virtual string RepresentedElementKind { get; }
	public virtual System.Drawing.SizeF Size { get; set; }
	public virtual int ZIndex { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static NSCollectionViewLayoutAttributes CreateForDecorationView (MonoMac.Foundation.NSString decorationViewKind, MonoMac.Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForInterItemGap (MonoMac.Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForItem (MonoMac.Foundation.NSIndexPath indexPath);
	public static NSCollectionViewLayoutAttributes CreateForSupplementaryView (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSIndexPath indexPath);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewLayoutInvalidationContext

<pre style='color: green'>
public class NSCollectionViewLayoutInvalidationContext : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewLayoutInvalidationContext ();
	public NSCollectionViewLayoutInvalidationContext (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewLayoutInvalidationContext (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewLayoutInvalidationContext (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.PointF ContentOffsetAdjustment { get; set; }
	public virtual System.Drawing.SizeF ContentSizeAdjustment { get; set; }
	public virtual bool InvalidateDataSourceCounts { get; }
	public virtual MonoMac.Foundation.NSDictionary InvalidatedDecorationIndexPaths { get; }
	public virtual MonoMac.Foundation.NSSet InvalidatedItemIndexPaths { get; }
	public virtual MonoMac.Foundation.NSDictionary InvalidatedSupplementaryIndexPaths { get; }
	public virtual bool InvalidateEverything { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void InvalidateDecorationElements (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSSet indexPaths);
	public virtual void InvalidateItems (MonoMac.Foundation.NSSet indexPaths);
	public virtual void InvalidateSupplementaryElements (MonoMac.Foundation.NSString elementKind, MonoMac.Foundation.NSSet indexPaths);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewScrollDirection

<pre style='color: green'>
[Serializable]
public enum NSCollectionViewScrollDirection {
	Horizontal = 1,
	Vertical = 0,
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewScrollPosition

<pre style='color: green'>
[Serializable]
public enum NSCollectionViewScrollPosition {
	Bottom = 4,
	CenteredHorizontally = 16,
	CenteredVertically = 2,
	LeadingEdge = 64,
	Left = 8,
	NearestHorizontalEdge = 512,
	NearestVerticalEdge = 256,
	None = 0,
	Right = 32,
	Top = 1,
	TrailingEdge = 128,
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewTransitionLayout

<pre style='color: green'>
public class NSCollectionViewTransitionLayout : MonoMac.AppKit.NSCollectionViewLayout, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewTransitionLayout ();
	public NSCollectionViewTransitionLayout (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewTransitionLayout (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewTransitionLayout (IntPtr handle);
	public NSCollectionViewTransitionLayout (NSCollectionViewLayout currentLayout, NSCollectionViewLayout newLayout);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSCollectionViewLayout CurrentLayout { get; }
	public virtual NSCollectionViewLayout NextLayout { get; }
	public virtual float TransitionProgress { get; set; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual float GetValue (string key);
	public virtual void UpdateValue (float value, string key);
}
</pre>

### New Type MonoMac.AppKit.NSCollectionViewUpdateItem

<pre style='color: green'>
public class NSCollectionViewUpdateItem : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCollectionViewUpdateItem ();
	public NSCollectionViewUpdateItem (MonoMac.Foundation.NSCoder coder);
	public NSCollectionViewUpdateItem (MonoMac.Foundation.NSObjectFlag t);
	public NSCollectionViewUpdateItem (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSIndexPath IndexPathAfterUpdate { get; }
	public virtual MonoMac.Foundation.NSIndexPath IndexPathBeforeUpdate { get; }
	public virtual NSCollectionUpdateAction UpdateAction { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSControlCharacterAction

<pre style='color: green'>
[Serializable]
public enum NSControlCharacterAction {
	ContainerBreak = 32,
	HorizontalTab = 4,
	LineBreak = 8,
	ParagraphBreak = 16,
	Whitespace = 2,
	ZeroAdvancement = 1,
}
</pre>

### New Type MonoMac.AppKit.NSDataAsset

<pre style='color: green'>
public class NSDataAsset : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSDataAsset (MonoMac.Foundation.NSCoder coder);
	public NSDataAsset (MonoMac.Foundation.NSObjectFlag t);
	public NSDataAsset (IntPtr handle);
	public NSDataAsset (string name);
	public NSDataAsset (string name, MonoMac.Foundation.NSBundle bundle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSData Data { get; }
	public virtual string Name { get; }
	public virtual MonoMac.Foundation.NSString TypeIdentifier { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSDictionaryController

<pre style='color: green'>
public class NSDictionaryController : MonoMac.AppKit.NSArrayController, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSDictionaryController ();
	public NSDictionaryController (MonoMac.Foundation.NSCoder coder);
	public NSDictionaryController (MonoMac.Foundation.NSObjectFlag t);
	public NSDictionaryController (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string[] ExcludedKeys { get; set; }
	public virtual string[] IncludedKeys { get; set; }
	public virtual string InitialKey { get; set; }
	public virtual MonoMac.Foundation.NSObject InitialValue { get; set; }
	public virtual MonoMac.Foundation.NSDictionary LocalizedKeyDictionary { get; set; }
	public virtual string LocalizedKeyTable { get; set; }
	public virtual NSDictionaryControllerKeyValuePair NewObject { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSDictionaryControllerKeyValuePair

<pre style='color: green'>
public class NSDictionaryControllerKeyValuePair : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSDictionaryControllerKeyValuePair (MonoMac.Foundation.NSCoder coder);
	public NSDictionaryControllerKeyValuePair (MonoMac.Foundation.NSObjectFlag t);
	public NSDictionaryControllerKeyValuePair (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool ExplicitlyIncluded { get; }
	public virtual string Key { get; set; }
	public virtual string LocalizedKey { get; set; }
	public virtual MonoMac.Foundation.NSObject Value { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSExtendedStringDrawing

<pre style='color: green'>
public static class NSExtendedStringDrawing {
	// methods
	public static void DrawString (MonoMac.Foundation.NSString This, System.Drawing.RectangleF rect, MonoMac.Foundation.NSStringDrawingOptions options, NSStringAttributes attributes, NSStringDrawingContext context);
	public static System.Drawing.RectangleF GetBoundingRect (MonoMac.Foundation.NSString This, System.Drawing.SizeF size, MonoMac.Foundation.NSStringDrawingOptions options, NSStringAttributes attributes, NSStringDrawingContext context);
	public static void WeakDrawString (MonoMac.Foundation.NSString This, System.Drawing.RectangleF rect, MonoMac.Foundation.NSStringDrawingOptions options, MonoMac.Foundation.NSDictionary attributes, NSStringDrawingContext context);
	public static System.Drawing.RectangleF WeakGetBoundingRect (MonoMac.Foundation.NSString This, System.Drawing.SizeF size, MonoMac.Foundation.NSStringDrawingOptions options, MonoMac.Foundation.NSDictionary attributes, NSStringDrawingContext context);
}
</pre>

### New Type MonoMac.AppKit.NSFontWeight

<pre style='color: green'>
public static class NSFontWeight {
	// properties
	public static float Black { get; }
	public static float Bold { get; }
	public static float Heavy { get; }
	public static float Light { get; }
	public static float Medium { get; }
	public static float Regular { get; }
	public static float Semibold { get; }
	public static float Thin { get; }
	public static float UltraLight { get; }
}
</pre>

### New Type MonoMac.AppKit.NSGlyphProperty

<pre style='color: green'>
[Serializable]
public enum NSGlyphProperty {
	ControlCharacter = 2,
	Elastic = 4,
	NonBaseCharacter = 8,
	Null = 1,
}
</pre>

### New Type MonoMac.AppKit.NSHapticFeedbackManager

<pre style='color: green'>
public class NSHapticFeedbackManager : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSHapticFeedbackManager ();
	public NSHapticFeedbackManager (MonoMac.Foundation.NSCoder coder);
	public NSHapticFeedbackManager (MonoMac.Foundation.NSObjectFlag t);
	public NSHapticFeedbackManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static INSHapticFeedbackPerformer DefaultPerformer { get; }
}
</pre>

### New Type MonoMac.AppKit.NSHapticFeedbackPattern

<pre style='color: green'>
[Serializable]
public enum NSHapticFeedbackPattern {
	Alignment = 1,
	Generic = 0,
	LevelChange = 2,
}
</pre>

### New Type MonoMac.AppKit.NSHapticFeedbackPerformanceTime

<pre style='color: green'>
[Serializable]
public enum NSHapticFeedbackPerformanceTime {
	Default = 0,
	DrawCompleted = 2,
	Now = 1,
}
</pre>

### New Type MonoMac.AppKit.NSHapticFeedbackPerformer

<pre style='color: green'>
public abstract class NSHapticFeedbackPerformer : MonoMac.Foundation.NSObject, INSHapticFeedbackPerformer, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSHapticFeedbackPerformer ();
	public NSHapticFeedbackPerformer (MonoMac.Foundation.NSCoder coder);
	public NSHapticFeedbackPerformer (MonoMac.Foundation.NSObjectFlag t);
	public NSHapticFeedbackPerformer (IntPtr handle);
	// methods
	public virtual void PerformFeedback (NSHapticFeedbackPattern pattern, NSHapticFeedbackPerformanceTime performanceTime);
}
</pre>

### New Type MonoMac.AppKit.NSHapticFeedbackPerformer_Extensions

<pre style='color: green'>
public static class NSHapticFeedbackPerformer_Extensions {
}
</pre>

### New Type MonoMac.AppKit.NSLayoutGuide

<pre style='color: green'>
public class NSLayoutGuide : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSLayoutGuide ();
	public NSLayoutGuide (MonoMac.Foundation.NSCoder coder);
	public NSLayoutGuide (MonoMac.Foundation.NSObjectFlag t);
	public NSLayoutGuide (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual System.Drawing.RectangleF Frame { get; }
	public virtual string Identifier { get; set; }
	public virtual NSView OwningView { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AppKit.NSPressureBehavior

<pre style='color: green'>
[Serializable]
public enum NSPressureBehavior {
	PrimaryAccelerator = 3,
	PrimaryClick = 1,
	PrimaryDeepClick = 5,
	PrimaryDeepDrag = 6,
	PrimaryDefault = 0,
	PrimaryGeneric = 2,
	Unknown = -1,
}
</pre>

### New Type MonoMac.AppKit.NSPressureConfiguration

<pre style='color: green'>
public class NSPressureConfiguration : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPressureConfiguration ();
	public NSPressureConfiguration (NSPressureBehavior pressureBehavior);
	public NSPressureConfiguration (MonoMac.Foundation.NSCoder coder);
	public NSPressureConfiguration (MonoMac.Foundation.NSObjectFlag t);
	public NSPressureConfiguration (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSPressureBehavior PressureBehavior { get; }
	// methods
	public virtual void Set ();
}
</pre>

### New Type MonoMac.AppKit.NSSearchFieldDelegate

<pre style='color: green'>
public class NSSearchFieldDelegate : MonoMac.Foundation.NSObject, INSSearchFieldDelegate, INSTextFieldDelegate, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSSearchFieldDelegate ();
	public NSSearchFieldDelegate (MonoMac.Foundation.NSCoder coder);
	public NSSearchFieldDelegate (MonoMac.Foundation.NSObjectFlag t);
	public NSSearchFieldDelegate (IntPtr handle);
	// methods
	public virtual void Changed (MonoMac.Foundation.NSNotification notification);
	public virtual bool DidFailToFormatString (NSControl control, string str, string error);
	public virtual void DidFailToValidatePartialString (NSControl control, string str, string error);
	public virtual bool DoCommandBySelector (NSControl control, NSTextView textView, MonoMac.ObjCRuntime.Selector commandSelector);
	public virtual void EditingBegan (MonoMac.Foundation.NSNotification notification);
	public virtual void EditingEnded (MonoMac.Foundation.NSNotification notification);
	public virtual string[] GetCompletions (NSControl control, NSTextView textView, string[] words, MonoMac.Foundation.NSRange charRange, ref int index);
	public virtual bool IsValidObject (NSControl control, MonoMac.Foundation.NSObject objectToValidate);
	public virtual void SearchingEnded (NSSearchField sender);
	public virtual void SearchingStarted (NSSearchField sender);
	public virtual bool TextShouldBeginEditing (NSControl control, NSText fieldEditor);
	public virtual bool TextShouldEndEditing (NSControl control, NSText fieldEditor);
}
</pre>

### New Type MonoMac.AppKit.NSSearchFieldDelegate_Extensions

<pre style='color: green'>
public static class NSSearchFieldDelegate_Extensions {
	// methods
	public static void SearchingEnded (INSSearchFieldDelegate This, NSSearchField sender);
	public static void SearchingStarted (INSSearchFieldDelegate This, NSSearchField sender);
}
</pre>

### New Type MonoMac.AppKit.NSSplitViewItemBehavior

<pre style='color: green'>
[Serializable]
public enum NSSplitViewItemBehavior {
	ContentList = 2,
	Default = 0,
	Sidebar = 1,
}
</pre>

### New Type MonoMac.AppKit.NSSpringLoadingDestination

<pre style='color: green'>
public abstract class NSSpringLoadingDestination : MonoMac.Foundation.NSObject, INSSpringLoadingDestination, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSSpringLoadingDestination ();
	public NSSpringLoadingDestination (MonoMac.Foundation.NSCoder coder);
	public NSSpringLoadingDestination (MonoMac.Foundation.NSObjectFlag t);
	public NSSpringLoadingDestination (IntPtr handle);
	// methods
	public virtual void Activated (bool activated, NSDraggingInfo draggingInfo);
	public virtual void DraggingEnded (NSDraggingInfo draggingInfo);
	public virtual NSSpringLoadingOptions Entered (NSDraggingInfo draggingInfo);
	public virtual void Exited (NSDraggingInfo draggingInfo);
	public virtual void HighlightChanged (NSDraggingInfo draggingInfo);
	public virtual NSSpringLoadingOptions Updated (NSDraggingInfo draggingInfo);
}
</pre>

### New Type MonoMac.AppKit.NSSpringLoadingDestination_Extensions

<pre style='color: green'>
public static class NSSpringLoadingDestination_Extensions {
	// methods
	public static void DraggingEnded (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static NSSpringLoadingOptions Entered (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static void Exited (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
	public static NSSpringLoadingOptions Updated (INSSpringLoadingDestination This, NSDraggingInfo draggingInfo);
}
</pre>

### New Type MonoMac.AppKit.NSSpringLoadingHighlight

<pre style='color: green'>
[Serializable]
public enum NSSpringLoadingHighlight {
	Emphasized = 2,
	None = 0,
	Standard = 1,
}
</pre>

### New Type MonoMac.AppKit.NSSpringLoadingOptions

<pre style='color: green'>
[Serializable]
public enum NSSpringLoadingOptions {
	ContinuousActivation = 2,
	Disabled = 0,
	Enabled = 1,
	NoHover = 8,
}
</pre>

### New Type MonoMac.AppKit.NSStackViewDistribution

<pre style='color: green'>
[Serializable]
public enum NSStackViewDistribution {
	EqualCentering = 4,
	EqualSpacing = 3,
	Fill = 0,
	FillEqually = 1,
	FillProportionally = 2,
	GravityAreas = -1,
}
</pre>

### New Type MonoMac.AppKit.NSStepperCell

<pre style='color: green'>
public class NSStepperCell : MonoMac.AppKit.NSActionCell, INSUserInterfaceItemIdentification, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.AppKit.NSStringDrawingContext

<pre style='color: green'>
public class NSStringDrawingContext : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSStringDrawingContext ();
	public NSStringDrawingContext (MonoMac.Foundation.NSCoder coder);
	public NSStringDrawingContext (MonoMac.Foundation.NSObjectFlag t);
	public NSStringDrawingContext (IntPtr handle);
	// properties
	public virtual float ActualScaleFactor { get; }
	public override IntPtr ClassHandle { get; }
	public virtual float MinimumScaleFactor { get; set; }
	public virtual System.Drawing.RectangleF TotalBounds { get; }
}
</pre>

### New Type MonoMac.AppKit.NSTableRowActionEdge

<pre style='color: green'>
[Serializable]
public enum NSTableRowActionEdge {
	Leading = 0,
	Trailing = 1,
}
</pre>

### New Type MonoMac.AppKit.NSTableViewRowAction

<pre style='color: green'>
public class NSTableViewRowAction : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTableViewRowAction ();
	public NSTableViewRowAction (MonoMac.Foundation.NSCoder coder);
	public NSTableViewRowAction (MonoMac.Foundation.NSObjectFlag t);
	public NSTableViewRowAction (IntPtr handle);
	// properties
	public virtual NSColor BackgroundColor { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual NSTableViewRowActionStyle Style { get; }
	public virtual string Title { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public static NSTableViewRowAction FromStyle (NSTableViewRowActionStyle style, string title, System.Action&lt;NSTableViewRowAction,System.Int32&gt; handler);
}
</pre>

### New Type MonoMac.AppKit.NSTableViewRowActionsGetter

<pre style='color: green'>
public sealed delegate NSTableViewRowActionsGetter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTableViewRowActionsGetter (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSTableView tableView, int row, NSTableRowActionEdge edge, System.AsyncCallback callback, object object);
	public virtual NSTableViewRowAction[] EndInvoke (System.IAsyncResult result);
	public virtual NSTableViewRowAction[] Invoke (NSTableView tableView, int row, NSTableRowActionEdge edge);
}
</pre>

### New Type MonoMac.AppKit.NSTableViewRowActionStyle

<pre style='color: green'>
[Serializable]
public enum NSTableViewRowActionStyle {
	Destructive = 1,
	Regular = 0,
}
</pre>

### New Type MonoMac.AppKit.NSTextAttachmentContainer

<pre style='color: green'>
public abstract class NSTextAttachmentContainer : MonoMac.Foundation.NSObject, INSTextAttachmentContainer, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSTextAttachmentContainer ();
	public NSTextAttachmentContainer (MonoMac.Foundation.NSCoder coder);
	public NSTextAttachmentContainer (MonoMac.Foundation.NSObjectFlag t);
	public NSTextAttachmentContainer (IntPtr handle);
	// methods
	public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF lineFrag, System.Drawing.PointF position, uint charIndex);
	public virtual NSImage GetImage (System.Drawing.RectangleF imageBounds, NSTextContainer textContainer, uint charIndex);
}
</pre>

### New Type MonoMac.AppKit.NSTextAttachmentContainer_Extensions

<pre style='color: green'>
public static class NSTextAttachmentContainer_Extensions {
}
</pre>

### New Type MonoMac.AppKit.NSTextInputClient

<pre style='color: green'>
public class NSTextInputClient : MonoMac.Foundation.NSObject, INSTextInputClient, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.AppKit.NSTextLayoutEnumerateEnclosingRects

<pre style='color: green'>
public sealed delegate NSTextLayoutEnumerateEnclosingRects : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTextLayoutEnumerateEnclosingRects (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.Drawing.RectangleF rect, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (System.Drawing.RectangleF rect, out bool stop);
}
</pre>

### New Type MonoMac.AppKit.NSTextLayoutEnumerateLineFragments

<pre style='color: green'>
public sealed delegate NSTextLayoutEnumerateLineFragments : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSTextLayoutEnumerateLineFragments (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.Drawing.RectangleF rect, System.Drawing.RectangleF usedRectangle, NSTextContainer textContainer, MonoMac.Foundation.NSRange glyphRange, out bool stop, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out bool stop, System.IAsyncResult result);
	public virtual void Invoke (System.Drawing.RectangleF rect, System.Drawing.RectangleF usedRectangle, NSTextContainer textContainer, MonoMac.Foundation.NSRange glyphRange, out bool stop);
}
</pre>

### New Type MonoMac.AppKit.NSTextStorageEditActions

<pre style='color: green'>
[Serializable]
public enum NSTextStorageEditActions {
	Attributes = 1,
	Characters = 2,
}
</pre>

### New Type MonoMac.AppKit.NSTextStorageEventArgs

<pre style='color: green'>
public class NSTextStorageEventArgs : System.EventArgs {
	// constructors
	public NSTextStorageEventArgs (NSTextStorageEditActions editedMask, MonoMac.Foundation.NSRange editedRange, int delta);
	// properties
	public int Delta { get; set; }
	public NSTextStorageEditActions EditedMask { get; set; }
	public MonoMac.Foundation.NSRange EditedRange { get; set; }
}
</pre>

## Namespace MonoMac.AudioToolbox

### Type Changed: MonoMac.AudioToolbox.AudioChannelLayoutTagExtensions

Added method:

<pre style='color: green'>
	public static uint GetNumberOfChannels (AudioChannelLayoutTag inLayoutTag);
</pre>

### Type Changed: MonoMac.AudioToolbox.AudioFormatFlags

Added values:

<pre style='color: green'>
	CafIsFloat = 1,
	CafIsLittleEndian = 2,
</pre>

### Type Changed: MonoMac.AudioToolbox.AudioFormatType

Added value:

<pre style='color: green'>
	EnhancedAES3 = 1700998451,
</pre>

### Type Changed: MonoMac.AudioToolbox.AudioQueue

Added method:

<pre style='color: green'>
	public AudioQueueStatus EnqueueBuffer (IntPtr audioQueueBuffer, AudioStreamPacketDescription[] desc);
</pre>

### Type Changed: MonoMac.AudioToolbox.AudioTimeStamp

### Type Changed: MonoMac.AudioToolbox.AudioTimeStamp.AtsFlags

Added field:

<pre style='color: green'>
	public static const AudioTimeStamp.AtsFlags NothingValid;
</pre>

### Type Changed: MonoMac.AudioToolbox.SmpteTime

Added properties:

<pre style='color: green'>
	public SmpteTimeFlags FlagsStrong { get; set; }
	public SmpteTimeType TypeStrong { get; set; }
</pre>

### Type Changed: MonoMac.AudioToolbox.SystemSound

Added constructor:

<pre style='color: green'>
	public SystemSound (uint soundId);
</pre>

Added methods:

<pre style='color: green'>
	public void PlayAlertSound (System.Action onCompletion);
	public System.Threading.Tasks.Task PlayAlertSoundAsync ();
	public void PlaySystemSound (System.Action onCompletion);
	public System.Threading.Tasks.Task PlaySystemSoundAsync ();
</pre>

### New Type MonoMac.AudioToolbox.MPEG4ObjectID

<pre style='color: green'>
[Serializable]
public enum MPEG4ObjectID {
	AacLc = 2,
	AacLtp = 4,
	AacMain = 1,
	AacSbr = 5,
	AacScalable = 6,
	AacSsr = 3,
	Celp = 8,
	Hvxc = 9,
	TwinVq = 7,
}
</pre>

### New Type MonoMac.AudioToolbox.SmpteTimeFlags

<pre style='color: green'>
[Serializable]
[Flags]
public enum SmpteTimeFlags {
	TimeRunning = 2,
	TimeValid = 1,
	Unknown = 0,
}
</pre>

## Namespace MonoMac.AudioUnit

### Type Changed: MonoMac.AudioUnit.AudioComponent

Added method:

<pre style='color: green'>
	public MonoMac.AppKit.NSImage GetIcon ();
</pre>

### Type Changed: MonoMac.AudioUnit.AudioComponentFlag

Added values:

<pre style='color: green'>
	CanLoadInProcess = 16,
	IsV3AudioUnit = 4,
	RequiresAsyncInstantiation = 8,
</pre>

### Type Changed: MonoMac.AudioUnit.AudioTypeConverter

Added value:

<pre style='color: green'>
	MultiSplitter = 1836281964,
</pre>

### Type Changed: MonoMac.AudioUnit.AudioUnit

Obsoleted methods:

```
[Obsolete ("Use SetFormat instead as it has the ability of returning a status code")]
	public void SetAudioFormat (MonoMac.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
```

Added method:

<pre style='color: green'>
	public AudioUnitStatus SetFormat (MonoMac.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
</pre>

### Type Changed: MonoMac.AudioUnit.AudioUnitPropertyIDType

Added values:

<pre style='color: green'>
	ParametersForOverview = 57,
	RequestViewController = 56,
</pre>

### Type Changed: MonoMac.AudioUnit.ExtAudioFile

Modified properties:

```
public MonoMac.AudioToolbox.AudioStreamBasicDescription ClientDataFormat { get; set; }
```

### New Type MonoMac.AudioUnit.AU3DMixerAttenuationCurve

<pre style='color: green'>
[Serializable]
public enum AU3DMixerAttenuationCurve {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
</pre>

### New Type MonoMac.AudioUnit.AU3DMixerRenderingFlags

<pre style='color: green'>
[Serializable]
public enum AU3DMixerRenderingFlags {
	ConstantReverbBlend = 64,
	DistanceAttenuation = 4,
	DistanceDiffusion = 16,
	DistanceFilter = 8,
	DopplerShift = 2,
	InterAuralDelay = 1,
	LinearDistanceAttenuation = 32,
}
</pre>

### New Type MonoMac.AudioUnit.AUAudioUnitBusType

<pre style='color: green'>
[Serializable]
public enum AUAudioUnitBusType {
	Input = 1,
	Output = 2,
}
</pre>

### New Type MonoMac.AudioUnit.AudioComponentConfigurationInfo

<pre style='color: green'>
public static class AudioComponentConfigurationInfo {
	// fields
	public static MonoMac.Foundation.NSString ValidationResult;
}
</pre>

### New Type MonoMac.AudioUnit.AudioComponentInstantiationOptions

<pre style='color: green'>
[Serializable]
public enum AudioComponentInstantiationOptions {
	InProcess = 2,
	OutOfProcess = 1,
}
</pre>

### New Type MonoMac.AudioUnit.AudioComponentValidationParameter

<pre style='color: green'>
public static class AudioComponentValidationParameter {
	// fields
	public static MonoMac.Foundation.NSString ForceValidation;
	public static MonoMac.Foundation.NSString TimeOut;
}
</pre>

### New Type MonoMac.AudioUnit.AudioComponentValidationResult

<pre style='color: green'>
[Serializable]
public enum AudioComponentValidationResult {
	Failed = 2,
	Passed = 1,
	TimedOut = 3,
	UnauthorizedErrorInit = 5,
	UnauthorizedErrorOpen = 4,
	Unknown = 0,
}
</pre>

### New Type MonoMac.AudioUnit.AudioUnitBusType

<pre style='color: green'>
[Serializable]
public enum AudioUnitBusType {
	Input = 1,
	Output = 2,
}
</pre>

### New Type MonoMac.AudioUnit.AudioUnitConfigurationInfo

<pre style='color: green'>
public static class AudioUnitConfigurationInfo {
	// fields
	public static MonoMac.Foundation.NSString BusCountWritable;
	public static MonoMac.Foundation.NSString ChannelConfigurations;
	public static MonoMac.Foundation.NSString HasCustomView;
	public static MonoMac.Foundation.NSString IconUrl;
	public static MonoMac.Foundation.NSString InitialInputs;
	public static MonoMac.Foundation.NSString SupportedChannelLayoutTags;
}
</pre>

### New Type MonoMac.AudioUnit.AudioUnitParameterOptions

<pre style='color: green'>
[Serializable]
public enum AudioUnitParameterOptions {
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
	OmitFromPresets = 8192,
	PlotHistory = 16384,
	ValuesHaveStrings = 2097152,
}
</pre>

### New Type MonoMac.AudioUnit.AudioUnitSubType

<pre style='color: green'>
[Serializable]
public enum AudioUnitSubType {
	AUConverter = 1668247158,
	AudioFilePlayer = 1634103404,
	AUFilter = 1718185076,
	AUiPodTimeOther = 1768977519,
	BandPassFilter = 1651532147,
	DefaultOutput = 1684366880,
	DeferredRenderer = 1684366962,
	Delay = 1684368505,
	Distortion = 1684632436,
	DLSSynth = 1684828960,
	DynamicsProcessor = 1684237680,
	GenericOutput = 1734700658,
	GraphicEQ = 1735550321,
	HALOutput = 1634230636,
	HighPassFilter = 1752195443,
	HighShelfFilter = 1752393830,
	HRTFPanner = 1752331366,
	LowPassFilter = 1819304307,
	LowShelfFilter = 1819502694,
	MatrixMixer = 1836608888,
	MatrixReverb = 1836213622,
	Merger = 1835364967,
	MidiSynth = 1836284270,
	MultiBandCompressor = 1835232624,
	MultiChannelMixer = 1835232632,
	MultiSplitter = 1836281964,
	NBandEQ = 1851942257,
	NetReceive = 1852990326,
	NetSend = 1853058660,
	NewTimePitch = 1853191280,
	ParametricEQ = 1886217585,
	PeakLimiter = 1819112562,
	Pitch = 1953329268,
	RogerBeep = 1919903602,
	RoundTripAac = 1918984547,
	SampleDelay = 1935961209,
	Sampler = 1935764848,
	ScheduledSoundPlayer = 1936945260,
	SoundFieldPanner = 1634558569,
	SpatialMixer = 862217581,
	SphericalHeadPanner = 1936746610,
	Splitter = 1936747636,
	StereoMixer = 1936554098,
	SystemOutput = 1937339168,
	TimePitch = 1953329268,
	Varispeed = 1986097769,
	VectorPanner = 1986158963,
	VoiceProcessingIO = 1987078511,
}
</pre>

### New Type MonoMac.AudioUnit.AUEventSampleTime

<pre style='color: green'>
[Serializable]
public enum AUEventSampleTime {
	Immediate = 0,
}
</pre>

### New Type MonoMac.AudioUnit.AUHostTransportStateFlags

<pre style='color: green'>
[Serializable]
public enum AUHostTransportStateFlags {
	Changed = 1,
	Cycling = 8,
	Moving = 2,
	Recording = 4,
}
</pre>

### New Type MonoMac.AudioUnit.AURenderEventType

<pre style='color: green'>
[Serializable]
public enum AURenderEventType {
	Midi = 8,
	MidiSysEx = 9,
	Parameter = 1,
	ParameterRamp = 2,
}
</pre>

### New Type MonoMac.AudioUnit.AUReverbRoomType

<pre style='color: green'>
[Serializable]
public enum AUReverbRoomType {
	Cathedral = 8,
	LargeChamber = 7,
	LargeHall = 4,
	LargeHall2 = 12,
	LargeRoom = 2,
	LargeRoom2 = 9,
	MediumChamber = 6,
	MediumHall = 3,
	MediumHall2 = 10,
	MediumHall3 = 11,
	MediumRoom = 1,
	Plate = 5,
	SmallRoom = 0,
}
</pre>

### New Type MonoMac.AudioUnit.AUScheduledAudioSliceFlags

<pre style='color: green'>
[Serializable]
public enum AUScheduledAudioSliceFlags {
	BeganToRender = 2,
	BeganToRenderLate = 4,
	Complete = 1,
	Interrupt = 16,
	InterruptAtLoop = 32,
	Loop = 8,
}
</pre>

### New Type MonoMac.AudioUnit.AUSpatializationAlgorithm

<pre style='color: green'>
[Serializable]
public enum AUSpatializationAlgorithm {
	EqualPowerPanning = 0,
	Hrtf = 2,
	SoundField = 3,
	SphericalHead = 1,
	StereoPassThrough = 5,
	VectorBasedPanning = 4,
}
</pre>

### New Type MonoMac.AudioUnit.AUSpatialMixerAttenuationCurve

<pre style='color: green'>
[Serializable]
public enum AUSpatialMixerAttenuationCurve {
	Exponential = 1,
	Inverse = 2,
	Linear = 3,
	Power = 0,
}
</pre>

### New Type MonoMac.AudioUnit.AUSpatialMixerRenderingFlags

<pre style='color: green'>
[Serializable]
public enum AUSpatialMixerRenderingFlags {
	DistanceAttenuation = 4,
	InterAuralDelay = 1,
}
</pre>

## Namespace MonoMac.AVFoundation

### Type Changed: MonoMac.AVFoundation.AVAsset

Added properties:

<pre style='color: green'>
	public virtual bool CanContainFragments { get; }
	public static MonoMac.Foundation.NSString ChapterMetadataGroupsDidChangeNotification { get; }
	public virtual bool CompatibleWithAirPlayVideo { get; }
	public virtual bool ContainsFragments { get; }
	public static MonoMac.Foundation.NSString ContainsFragmentsDidChangeNotification { get; }
	public static MonoMac.Foundation.NSString DurationDidChangeNotification { get; }
	public static MonoMac.Foundation.NSString MediaSelectionGroupsDidChangeNotification { get; }
	public virtual AVMediaSelection PreferredMediaSelection { get; }
	public virtual int UnusedTrackId { get; }
	public static MonoMac.Foundation.NSString WasDefragmentedNotification { get; }
</pre>

Obsoleted methods:

```
[Obsolete ("Use GetChapterMetadataGroups")]
	public virtual AVMetadataItem[] ChapterMetadataGroups (MonoMac.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
```

Added method:

<pre style='color: green'>
	public virtual AVTimedMetadataGroup[] GetChapterMetadataGroups (MonoMac.Foundation.NSLocale forLocale, AVMetadataItem[] commonKeys);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAssetExportSession

Added properties:

<pre style='color: green'>
	public virtual AVMetadataItemFilter MetadataItemFilter { get; set; }
	public static MonoMac.Foundation.NSString Preset1920x1080 { get; }
	public static MonoMac.Foundation.NSString Preset3840x2160 { get; }
	public static MonoMac.Foundation.NSString PresetHighestQuality { get; }
	public static MonoMac.Foundation.NSString PresetLowQuality { get; }
	public static MonoMac.Foundation.NSString PresetMediumQuality { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoader

Added property:

<pre style='color: green'>
	public virtual bool PreloadsEligibleContentKeys { get; set; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVAssetResourceLoadingDataRequest

Added property:

<pre style='color: green'>
	public virtual bool RequestsAllDataToEndOfResource { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVAssetTrack

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString SegmentsDidChangeNotification { get; }
	public static MonoMac.Foundation.NSString TimeRangeDidChangeNotification { get; }
	public static MonoMac.Foundation.NSString TrackAssociationsDidChangeNotification { get; }
</pre>

Obsoleted methods:

```
[Obsolete ("Use GetAssociatedTracks")]
	public virtual MonoMac.Foundation.NSString GetAssociatedTracksOfType (MonoMac.Foundation.NSString avAssetTrackTrackAssociationType);
```

Added method:

<pre style='color: green'>
	public virtual AVAssetTrack[] GetAssociatedTracks (MonoMac.Foundation.NSString avAssetTrackTrackAssociationType);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAssetWriter

Added properties:

<pre style='color: green'>
	public virtual AVAssetWriterInputGroup[] InputGroups { get; }
	public virtual MonoMac.CoreMedia.CMTime OverallDurationHint { get; set; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioChannelLayout

Added interfaces:

<pre style='color: green'>
	MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioEngine

Added methods:

<pre style='color: green'>
	public virtual void Connect (AVAudioNode sourceNode, AVAudioConnectionPoint[] destNodes, uint sourceBus, AVAudioFormat format);
	public virtual AVAudioConnectionPoint InputConnectionPoint (AVAudioNode node, uint bus);
	public virtual AVAudioConnectionPoint[] OutputConnectionPoints (AVAudioNode node, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioEnvironmentNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioFormat

Added constructor:

<pre style='color: green'>
	public AVAudioFormat (MonoMac.CoreMedia.CMAudioFormatDescription formatDescription);
</pre>

Added interfaces:

<pre style='color: green'>
	MonoMac.Foundation.INSCoding
	MonoMac.Foundation.INSSecureCoding
</pre>

Added property:

<pre style='color: green'>
	public virtual MonoMac.CoreMedia.CMAudioFormatDescription FormatDescription { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioInputNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioMixerNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioMixing_Extensions

Added method:

<pre style='color: green'>
	public static AVAudioMixingDestination DestinationForMixer (IAVAudioMixing This, AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioMixInputParameters

Added property:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSString AudioTimePitchAlgorithm { get; set; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioPlayerNode

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioSessionCategoryOptions

Added value:

<pre style='color: green'>
	InterruptSpokenAudioAndMixWithOthers = 17,
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioSessionErrorCode

Added value:

<pre style='color: green'>
	CodeResourceNotAvailable = 561145203,
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioUnitGenerator

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioUnitMidiInstrument

Added interfaces:

<pre style='color: green'>
	IAVAudio3DMixing
	IAVAudioMixing
	IAVAudioStereoMixing
</pre>

Added properties:

<pre style='color: green'>
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
</pre>

### Type Changed: MonoMac.AVFoundation.AVAudioUnitSampler

Added interfaces:

<pre style='color: green'>
	IAVAudio3DMixing
	IAVAudioMixing
	IAVAudioStereoMixing
</pre>

### Type Changed: MonoMac.AVFoundation.AVCaptureVideoStabilizationMode

Modified fields:

```
Auto = 3 -1
```

### Type Changed: MonoMac.AVFoundation.AVComposition

Added property:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSDictionary UrlAssetInitializationOptions { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVCompositionTrackSegment

Added property:

<pre style='color: green'>
	public virtual bool Empty { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVError

Added value:

<pre style='color: green'>
	VideoCompositorFailed = -11858,
</pre>

### Type Changed: MonoMac.AVFoundation.AVFileType

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString EnhancedAC3 { get; }
	public static MonoMac.Foundation.NSString ThreeGpp2 { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMediaCharacteristic

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString DubbedTranslation { get; }
	public static MonoMac.Foundation.NSString LanguageTranslation { get; }
	public static MonoMac.Foundation.NSString VoiceOverTranslation { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMediaSelectionGroup

Added method:

<pre style='color: green'>
	public static AVMediaSelectionOption[] MediaSelectionOptionsFilteredAndSorted (AVMediaSelectionOption[] mediaSelectionOptions, string[] preferredLanguages);
</pre>

### Type Changed: MonoMac.AVFoundation.AVMetadata

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString ID3MetadataKeyCommercial { get; }
	public static MonoMac.Foundation.NSString QuickTimeMetadataKeyContentIdentifier { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMetadataIdentifiers

### Type Changed: MonoMac.AVFoundation.AVMetadataIdentifiers.QuickTimeMetadata

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString ContentIdentifier { get; }
	public static MonoMac.Foundation.NSString DetectedFace { get; }
	public static MonoMac.Foundation.NSString VideoOrientation { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMetadataIdentifiers.ID3Metadata

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString Commercial { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMetadataItem

Added property:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSDate StartDate { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public static AVMetadataItem GetMetadataItem (AVMetadataItem metadataItem, System.Action&lt;AVMetadataItemValueRequest&gt; handler);
</pre>

### Type Changed: MonoMac.AVFoundation.AVMutableComposition

Added method:

<pre style='color: green'>
	public static AVMutableComposition FromOptions (MonoMac.Foundation.NSDictionary urlAssetInitializationOptions);
</pre>

### Type Changed: MonoMac.AVFoundation.AVMutableCompositionTrack

Obsoleted methods:

```
[Obsolete ("Use InsertTimeRanges overload accepting an NSValue array")]
	public virtual bool InsertTimeRanges (MonoMac.Foundation.NSValue cmTimeRanges, AVAssetTrack[] tracks, MonoMac.CoreMedia.CMTime startTime, out MonoMac.Foundation.NSError error);
```

Added method:

<pre style='color: green'>
	public virtual bool InsertTimeRanges (MonoMac.Foundation.NSValue[] cmTimeRanges, AVAssetTrack[] tracks, MonoMac.CoreMedia.CMTime startTime, out MonoMac.Foundation.NSError error);
</pre>

### Type Changed: MonoMac.AVFoundation.AVMutableMetadataItem

Added property:

<pre style='color: green'>
	public override MonoMac.Foundation.NSDate StartDate { get; set; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVMutableTimedMetadataGroup

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSMutableCopying
</pre>

### Type Changed: MonoMac.AVFoundation.AVMutableVideoComposition

Added method:

<pre style='color: green'>
	public static AVMutableVideoComposition GetVideoComposition (AVAsset asset, System.Action&lt;AVAsynchronousCIImageFilteringRequest&gt; applier);
</pre>

### Type Changed: MonoMac.AVFoundation.AVPlayer

Added properties:

<pre style='color: green'>
	public virtual bool AllowsExternalPlayback { get; set; }
	public virtual string AudioOutputDeviceUniqueID { get; set; }
	public virtual bool ExternalPlaybackActive { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVPlayerItem

Added properties:

<pre style='color: green'>
	public virtual bool CanUseNetworkResourcesForLiveStreamingWhilePaused { get; set; }
	public virtual AVMediaSelection CurrentMediaSelection { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVPlayerItemTrack

Added properties:

<pre style='color: green'>
	public virtual string VideoFieldMode { get; set; }
	public static MonoMac.Foundation.NSString VideoFieldModeDeinterlaceFields { get; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVPlayerLayer

Added properties:

<pre style='color: green'>
	public MonoMac.CoreVideo.CVPixelBufferAttributes PixelBufferAttributes { get; set; }
	public virtual MonoMac.Foundation.NSDictionary WeakPixelBufferAttributes { get; set; }
</pre>

### Type Changed: MonoMac.AVFoundation.AVTextStyleRule

Obsoleted constructors:

```
[Obsolete ("iOS9 does not allow creating an empty instance")]
	public AVTextStyleRule ();
```

### Type Changed: MonoMac.AVFoundation.AVTimedMetadataGroup


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.Foundation.NSObject</span></span>

 <span style='color:green'>MonoMac.AVFoundation.AVMetadataGroup</span>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSMutableCopying
</pre>

Added method:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
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

### Type Changed: MonoMac.AVFoundation.AVVideoComposition

Added method:

<pre style='color: green'>
	public static AVVideoComposition CreateVideoComposition (AVAsset asset, System.Action&lt;AVAsynchronousCIImageFilteringRequest&gt; applier);
</pre>

### New Type MonoMac.AVFoundation.AVAsynchronousCIImageFilteringRequest

<pre style='color: green'>
public class AVAsynchronousCIImageFilteringRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAsynchronousCIImageFilteringRequest ();
	public AVAsynchronousCIImageFilteringRequest (MonoMac.Foundation.NSCoder coder);
	public AVAsynchronousCIImageFilteringRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVAsynchronousCIImageFilteringRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.CoreMedia.CMTime CompositionTime { get; }
	public virtual System.Drawing.SizeF RenderSize { get; }
	public virtual MonoMac.CoreImage.CIImage SourceImage { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual void Finish (MonoMac.Foundation.NSError error);
	public virtual void Finish (MonoMac.CoreImage.CIImage filteredImage, MonoMac.CoreImage.CIContext context);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioCompressedBuffer

<pre style='color: green'>
public class AVAudioCompressedBuffer : MonoMac.AVFoundation.AVAudioBuffer, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioCompressedBuffer (MonoMac.Foundation.NSCoder coder);
	public AVAudioCompressedBuffer (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioCompressedBuffer (IntPtr handle);
	public AVAudioCompressedBuffer (AVAudioFormat format, uint packetCapacity);
	public AVAudioCompressedBuffer (AVAudioFormat format, uint packetCapacity, int maximumPacketSize);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual IntPtr Data { get; }
	public virtual int MaximumPacketSize { get; }
	public virtual uint PacketCapacity { get; }
	public virtual uint PacketCount { get; set; }
	public virtual MonoMac.AudioToolbox.AudioStreamPacketDescription PacketDescriptions { get; }
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConnectionPoint

<pre style='color: green'>
public class AVAudioConnectionPoint : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioConnectionPoint ();
	public AVAudioConnectionPoint (MonoMac.Foundation.NSCoder coder);
	public AVAudioConnectionPoint (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioConnectionPoint (IntPtr handle);
	public AVAudioConnectionPoint (AVAudioNode node, uint bus);
	// properties
	public virtual uint Bus { get; }
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioNode Node { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverter

<pre style='color: green'>
public class AVAudioConverter : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioConverter (MonoMac.Foundation.NSCoder coder);
	public AVAudioConverter (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioConverter (IntPtr handle);
	public AVAudioConverter (AVAudioFormat fromFormat, AVAudioFormat toFormat);
	// properties
	public virtual MonoMac.Foundation.NSNumber[] ApplicableEncodeBitRates { get; }
	public virtual MonoMac.Foundation.NSNumber[] ApplicableEncodeSampleRates { get; }
	public virtual MonoMac.Foundation.NSNumber[] AvailableEncodeBitRates { get; }
	public virtual MonoMac.Foundation.NSNumber[] AvailableEncodeChannelLayoutTags { get; }
	public virtual MonoMac.Foundation.NSNumber[] AvailableEncodeSampleRates { get; }
	public virtual int BitRate { get; set; }
	public virtual string BitRateStrategy { get; set; }
	public virtual MonoMac.Foundation.NSNumber[] ChannelMap { get; set; }
	public override IntPtr ClassHandle { get; }
	public virtual bool Dither { get; set; }
	public virtual bool Downmix { get; set; }
	public virtual AVAudioFormat InputFormat { get; }
	public virtual MonoMac.Foundation.NSData MagicCookie { get; set; }
	public virtual int MaximumOutputPacketSize { get; }
	public virtual AVAudioFormat OutputFormat { get; }
	public virtual AVAudioConverterPrimeInfo PrimeInfo { get; set; }
	public virtual AVAudioConverterPrimeMethod PrimeMethod { get; set; }
	public virtual string SampleRateConverterAlgorithm { get; set; }
	public virtual int SampleRateConverterQuality { get; set; }
	// methods
	public virtual AVAudioConverterOutputStatus ConvertToBuffer (AVAudioBuffer outputBuffer, out MonoMac.Foundation.NSError outError, AVAudioConverterInputHandler inputHandler);
	public virtual bool ConvertToBuffer (AVAudioPcmBuffer outputBuffer, AVAudioPcmBuffer inputBuffer, out MonoMac.Foundation.NSError outError);
	protected override void Dispose (bool disposing);
	public virtual void Reset ();
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverterInputHandler

<pre style='color: green'>
public sealed delegate AVAudioConverterInputHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public AVAudioConverterInputHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (uint inNumberOfPackets, out AVAudioConverterInputStatus outStatus, System.AsyncCallback callback, object object);
	public virtual AVAudioBuffer EndInvoke (out AVAudioConverterInputStatus outStatus, System.IAsyncResult result);
	public virtual AVAudioBuffer Invoke (uint inNumberOfPackets, out AVAudioConverterInputStatus outStatus);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverterInputStatus

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterInputStatus {
	EndOfStream = 2,
	HaveData = 0,
	NoDataNow = 1,
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverterOutputStatus

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterOutputStatus {
	EndOfStream = 2,
	Error = 3,
	HaveData = 0,
	InputRanDry = 1,
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverterPrimeInfo

<pre style='color: green'>
public struct AVAudioConverterPrimeInfo {
	// fields
	public uint LeadingFrames;
	public uint TrailingFrames;
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioConverterPrimeMethod

<pre style='color: green'>
[Serializable]
public enum AVAudioConverterPrimeMethod {
	None = 2,
	Normal = 1,
	Pre = 0,
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioMixingDestination

<pre style='color: green'>
public class AVAudioMixingDestination : MonoMac.Foundation.NSObject, IAVAudio3DMixing, IAVAudioMixing, IAVAudioStereoMixing, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioMixingDestination (MonoMac.Foundation.NSCoder coder);
	public AVAudioMixingDestination (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioMixingDestination (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioConnectionPoint ConnectionPoint { get; }
	public virtual float Obstruction { get; set; }
	public virtual float Occlusion { get; set; }
	public virtual float Pan { get; set; }
	public virtual MonoMac.OpenGL.Vector3 Position { get; set; }
	public virtual float Rate { get; set; }
	public virtual AVAudio3DMixingRenderingAlgorithm RenderingAlgorithm { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual float Volume { get; set; }
	// methods
	public virtual AVAudioMixingDestination DestinationForMixer (AVAudioNode mixer, uint bus);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioSequencer

<pre style='color: green'>
public class AVAudioSequencer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioSequencer ();
	public AVAudioSequencer (AVAudioEngine engine);
	public AVAudioSequencer (MonoMac.Foundation.NSCoder coder);
	public AVAudioSequencer (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioSequencer (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual double CurrentPositionInBeats { get; set; }
	public virtual double CurrentPositionInSeconds { get; set; }
	public virtual bool Playing { get; }
	public virtual float Rate { get; set; }
	public virtual AVMusicTrack TempoTrack { get; }
	public virtual AVMusicTrack[] Tracks { get; }
	public virtual MonoMac.Foundation.NSDictionary UserInfo { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual double GetBeats (double seconds);
	public virtual double GetBeats (ulong inHostTime, out MonoMac.Foundation.NSError outError);
	public virtual MonoMac.Foundation.NSData GetData (int smpteResolution, out MonoMac.Foundation.NSError outError);
	public virtual ulong GetHostTime (double inBeats, out MonoMac.Foundation.NSError outError);
	public virtual double GetSeconds (double beats);
	public virtual bool Load (MonoMac.Foundation.NSData data, AVMusicSequenceLoadOptions options, out MonoMac.Foundation.NSError outError);
	public virtual bool Load (MonoMac.Foundation.NSUrl fileUrl, AVMusicSequenceLoadOptions options, out MonoMac.Foundation.NSError outError);
	public virtual void PrepareToPlay ();
	public virtual bool Start (out MonoMac.Foundation.NSError outError);
	public virtual void Stop ();
	public virtual bool Write (MonoMac.Foundation.NSUrl fileUrl, int resolution, bool replace, out MonoMac.Foundation.NSError outError);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioUnitComponent

<pre style='color: green'>
public class AVAudioUnitComponent : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitComponent ();
	public AVAudioUnitComponent (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitComponent (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitComponent (IntPtr handle);
	// properties
	public virtual string[] AllTagNames { get; }
	public virtual MonoMac.AudioUnit.AudioComponent AudioComponent { get; }
	public virtual MonoMac.Foundation.NSNumber[] AvailableArchitectures { get; }
	public override IntPtr ClassHandle { get; }
	public virtual bool HasCustomView { get; }
	public virtual bool HasMidiInput { get; }
	public virtual bool HasMidiOutput { get; }
	public virtual MonoMac.AppKit.NSImage Icon { get; }
	public virtual MonoMac.Foundation.NSUrl IconUrl { get; }
	public virtual string LocalizedTypeName { get; }
	public virtual string ManufacturerName { get; }
	public virtual string Name { get; }
	public virtual bool PassesAUVal { get; }
	public virtual bool SandboxSafe { get; }
	public static MonoMac.Foundation.NSString TagsDidChangeNotification { get; }
	public virtual string TypeName { get; }
	public virtual string[] UserTagNames { get; set; }
	public virtual uint Version { get; }
	public virtual string VersionString { get; }
	public virtual MonoMac.Foundation.NSDictionary WeakConfigurationDictionary { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual bool SupportsNumberInputChannels (int numInputChannels, int numOutputChannels);

	// inner types
	public static class Notifications {
		// methods
		public static MonoMac.Foundation.NSObject ObserveTagsDidChange (System.EventHandler&lt;MonoMac.Foundation.NSNotificationEventArgs&gt; handler);
	}
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioUnitComponentFilter

<pre style='color: green'>
public sealed delegate AVAudioUnitComponentFilter : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public AVAudioUnitComponentFilter (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (AVAudioUnitComponent comp, ref bool stop, System.AsyncCallback callback, object object);
	public virtual bool EndInvoke (ref bool stop, System.IAsyncResult result);
	public virtual bool Invoke (AVAudioUnitComponent comp, ref bool stop);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioUnitComponentManager

<pre style='color: green'>
public class AVAudioUnitComponentManager : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVAudioUnitComponentManager ();
	public AVAudioUnitComponentManager (MonoMac.Foundation.NSCoder coder);
	public AVAudioUnitComponentManager (MonoMac.Foundation.NSObjectFlag t);
	public AVAudioUnitComponentManager (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public static AVAudioUnitComponentManager SharedInstance { get; }
	public virtual string[] StandardLocalizedTagNames { get; }
	public virtual string[] TagNames { get; }
	// methods
	public virtual AVAudioUnitComponent[] GetComponents (AVAudioUnitComponentFilter testHandler);
	public virtual AVAudioUnitComponent[] GetComponents (MonoMac.Foundation.NSPredicate predicate);
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioUnitManufacturerName

<pre style='color: green'>
public static class AVAudioUnitManufacturerName {
	// properties
	public static MonoMac.Foundation.NSString Apple { get; }
}
</pre>

### New Type MonoMac.AVFoundation.AVAudioUnitType

<pre style='color: green'>
public static class AVAudioUnitType {
	// properties
	public static MonoMac.Foundation.NSString Effect { get; }
	public static MonoMac.Foundation.NSString FormatConverter { get; }
	public static MonoMac.Foundation.NSString Generator { get; }
	public static MonoMac.Foundation.NSString MidiProcessor { get; }
	public static MonoMac.Foundation.NSString Mixer { get; }
	public static MonoMac.Foundation.NSString MusicDevice { get; }
	public static MonoMac.Foundation.NSString MusicEffect { get; }
	public static MonoMac.Foundation.NSString OfflineEffect { get; }
	public static MonoMac.Foundation.NSString Output { get; }
	public static MonoMac.Foundation.NSString Panner { get; }
}
</pre>

### New Type MonoMac.AVFoundation.AVBeatRange

<pre style='color: green'>
public struct AVBeatRange {
	// constructors
	public AVBeatRange (double startBeat, double lengthInBeats);
	// fields
	public double Length;
	public double Start;
}
</pre>

### New Type MonoMac.AVFoundation.AVComposition_AVCompositionTrackInspection

<pre style='color: green'>
public static class AVComposition_AVCompositionTrackInspection {
	// methods
	public static AVCompositionTrack GetTrack (AVComposition This, int trackID);
	public static AVCompositionTrack[] GetTracks (AVComposition This, string mediaType);
	public static AVCompositionTrack[] GetTracksWithMediaCharacteristic (AVComposition This, string mediaCharacteristic);
}
</pre>

### New Type MonoMac.AVFoundation.AVDateRangeMetadataGroup

<pre style='color: green'>
public class AVDateRangeMetadataGroup : MonoMac.AVFoundation.AVMetadataGroup, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVDateRangeMetadataGroup ();
	public AVDateRangeMetadataGroup (MonoMac.Foundation.NSCoder coder);
	public AVDateRangeMetadataGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVDateRangeMetadataGroup (IntPtr handle);
	public AVDateRangeMetadataGroup (AVMetadataItem[] items, MonoMac.Foundation.NSDate startDate, MonoMac.Foundation.NSDate endDate);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSDate EndDate { get; set; }
	public virtual AVMetadataItem[] Items { get; set; }
	public virtual MonoMac.Foundation.NSDate StartDate { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	protected override void Dispose (bool disposing);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
}
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

### New Type MonoMac.AVFoundation.AVFragmentedAsset

<pre style='color: green'>
public class AVFragmentedAsset : MonoMac.AVFoundation.AVUrlAsset, IAVFragmentMinding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVFragmentedAsset (MonoMac.Foundation.NSCoder coder);
	public AVFragmentedAsset (MonoMac.Foundation.NSObjectFlag t);
	public AVFragmentedAsset (IntPtr handle);
	public AVFragmentedAsset (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVFragmentedAssetTrack[] Tracks { get; }
	// methods
	protected override void Dispose (bool disposing);
	public static AVFragmentedAsset FromUrl (MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
	public virtual bool IsAssociatedWithFragmentMinder ();
}
</pre>

### New Type MonoMac.AVFoundation.AVFragmentedAsset_AVFragmentedAssetTrackInspection

<pre style='color: green'>
public static class AVFragmentedAsset_AVFragmentedAssetTrackInspection {
	// methods
	public static AVFragmentedAssetTrack GetTrack (AVFragmentedAsset This, int trackID);
	public static AVFragmentedAssetTrack[] GetTracks (AVFragmentedAsset This, string mediaType);
	public static AVFragmentedAssetTrack[] GetTracksWithMediaCharacteristic (AVFragmentedAsset This, string mediaCharacteristic);
}
</pre>

### New Type MonoMac.AVFoundation.AVFragmentedAssetMinder

<pre style='color: green'>
public class AVFragmentedAssetMinder : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVFragmentedAssetMinder ();
	public AVFragmentedAssetMinder (MonoMac.Foundation.NSCoder coder);
	public AVFragmentedAssetMinder (MonoMac.Foundation.NSObjectFlag t);
	public AVFragmentedAssetMinder (IntPtr handle);
	// properties
	public virtual AVAsset[] Assets { get; }
	public override IntPtr ClassHandle { get; }
	public virtual double MindingInterval { get; set; }
	// methods
	public virtual void AddFragmentedAsset (AVAsset asset);
	protected override void Dispose (bool disposing);
	public static AVFragmentedAssetMinder FromAsset (AVAsset asset, double mindingInterval);
	public virtual void RemoveFragmentedAsset (AVAsset asset);
}
</pre>

### New Type MonoMac.AVFoundation.AVFragmentedAssetTrack

<pre style='color: green'>
public class AVFragmentedAssetTrack : MonoMac.AVFoundation.AVAssetTrack, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVFragmentedAssetTrack (MonoMac.Foundation.NSCoder coder);
	public AVFragmentedAssetTrack (MonoMac.Foundation.NSObjectFlag t);
	public AVFragmentedAssetTrack (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
}
</pre>

### New Type MonoMac.AVFoundation.AVFragmentMinding_Extensions

<pre style='color: green'>
public static class AVFragmentMinding_Extensions {
	// methods
	public static bool IsAssociatedWithFragmentMinder (IAVFragmentMinding This);
}
</pre>

### New Type MonoMac.AVFoundation.AVMediaSelection

<pre style='color: green'>
public class AVMediaSelection : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMediaSelection ();
	public AVMediaSelection (MonoMac.Foundation.NSCoder coder);
	public AVMediaSelection (MonoMac.Foundation.NSObjectFlag t);
	public AVMediaSelection (IntPtr handle);
	// properties
	public virtual AVAsset Asset { get; }
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public virtual bool CriteriaCanBeAppliedAutomaticallyToMediaSelectionGroup (AVMediaSelectionGroup mediaSelectionGroup);
	protected override void Dispose (bool disposing);
	public virtual AVMediaSelectionOption GetSelectedMediaOption (AVMediaSelectionGroup mediaSelectionGroup);
	public virtual MonoMac.Foundation.NSObject MutableCopy (MonoMac.Foundation.NSZone zone);
}
</pre>

### New Type MonoMac.AVFoundation.AVMetadataExtraAttribute

<pre style='color: green'>
public static class AVMetadataExtraAttribute {
	// properties
	public static MonoMac.Foundation.NSString BaseUriKey { get; }
	public static MonoMac.Foundation.NSString InfoKey { get; }
	public static MonoMac.Foundation.NSString ValueUriKey { get; }
}
</pre>

### New Type MonoMac.AVFoundation.AVMetadataGroup

<pre style='color: green'>
public class AVMetadataGroup : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMetadataGroup ();
	public AVMetadataGroup (MonoMac.Foundation.NSCoder coder);
	public AVMetadataGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVMetadataGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVMetadataItem[] Items { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AVFoundation.AVMetadataItemValueRequest

<pre style='color: green'>
public class AVMetadataItemValueRequest : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMetadataItemValueRequest ();
	public AVMetadataItemValueRequest (MonoMac.Foundation.NSCoder coder);
	public AVMetadataItemValueRequest (MonoMac.Foundation.NSObjectFlag t);
	public AVMetadataItemValueRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVMetadataItem MetadataItem { get; }
	// methods
	protected override void Dispose (bool disposing);
	public virtual void Respond (MonoMac.Foundation.NSError error);
	public virtual void Respond (MonoMac.Foundation.NSObject value);
}
</pre>

### New Type MonoMac.AVFoundation.AVMusicSequenceLoadOptions

<pre style='color: green'>
[Serializable]
public enum AVMusicSequenceLoadOptions {
	ChannelsToTracks = 1,
	PreserveTracks = 0,
}
</pre>

### New Type MonoMac.AVFoundation.AVMusicTrack

<pre style='color: green'>
public class AVMusicTrack : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMusicTrack (MonoMac.Foundation.NSCoder coder);
	public AVMusicTrack (MonoMac.Foundation.NSObjectFlag t);
	public AVMusicTrack (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual AVAudioUnit DestinationAudioUnit { get; set; }
	public virtual uint DestinationMidiEndpoint { get; set; }
	public virtual double LengthInBeats { get; set; }
	public virtual double LengthInSeconds { get; set; }
	public virtual bool LoopingEnabled { get; set; }
	public virtual AVBeatRange LoopRange { get; set; }
	public virtual bool Muted { get; set; }
	public virtual int NumberOfLoops { get; set; }
	public virtual double OffsetTime { get; set; }
	public virtual bool Soloed { get; set; }
	public virtual uint TimeResolution { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AVFoundation.AVMutableComposition_AVMutableCompositionTrackInspection

<pre style='color: green'>
public static class AVMutableComposition_AVMutableCompositionTrackInspection {
	// methods
	public static AVMutableCompositionTrack GetTrack (AVMutableComposition This, int trackID);
	public static AVMutableCompositionTrack[] GetTracks (AVMutableComposition This, string mediaType);
	public static AVMutableCompositionTrack[] GetTracksWithMediaCharacteristic (AVMutableComposition This, string mediaCharacteristic);
}
</pre>

### New Type MonoMac.AVFoundation.AVMutableDateRangeMetadataGroup

<pre style='color: green'>
public class AVMutableDateRangeMetadataGroup : MonoMac.AVFoundation.AVDateRangeMetadataGroup, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMutableDateRangeMetadataGroup ();
	public AVMutableDateRangeMetadataGroup (MonoMac.Foundation.NSCoder coder);
	public AVMutableDateRangeMetadataGroup (MonoMac.Foundation.NSObjectFlag t);
	public AVMutableDateRangeMetadataGroup (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public override MonoMac.Foundation.NSDate EndDate { get; set; }
	public override AVMetadataItem[] Items { get; set; }
	public override MonoMac.Foundation.NSDate StartDate { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.AVFoundation.AVMutableMediaSelection

<pre style='color: green'>
public class AVMutableMediaSelection : MonoMac.AVFoundation.AVMediaSelection, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public AVMutableMediaSelection ();
	public AVMutableMediaSelection (MonoMac.Foundation.NSCoder coder);
	public AVMutableMediaSelection (MonoMac.Foundation.NSObjectFlag t);
	public AVMutableMediaSelection (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void SelectMediaOption (AVMediaSelectionOption mediaSelectionOption, AVMediaSelectionGroup mediaSelectionGroup);
}
</pre>

### New Type MonoMac.AVFoundation.AVStreamingKeyDelivery

<pre style='color: green'>
public static class AVStreamingKeyDelivery {
	// properties
	public static MonoMac.Foundation.NSString ContentKeyType { get; }
	public static MonoMac.Foundation.NSString PersistentContentKeyType { get; }
}
</pre>

### New Type MonoMac.AVFoundation.IAVFragmentMinding

<pre style='color: green'>
public interface IAVFragmentMinding : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

## Namespace MonoMac.AVKit

### New Type MonoMac.AVKit.AVKitError

<pre style='color: green'>
[Serializable]
public enum AVKitError {
	None = 0,
	PictureInPictureStartFailed = -1001,
	Unknown = -1000,
}
</pre>

## Namespace MonoMac.CloudKit

### New Type MonoMac.CloudKit.CKRecordID

<pre style='color: green'>
public class CKRecordID {
	// constructors

	[Obsolete ("iOS9 does not allow creating an empty instance")]
	public CKRecordID ();
}
</pre>

### New Type MonoMac.CloudKit.CKRecordZoneID

<pre style='color: green'>
public class CKRecordZoneID {
	// constructors

	[Obsolete ("iOS9 does not allow creating an empty instance")]
	public CKRecordZoneID ();
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

### Type Changed: MonoMac.CoreAnimation.CAEmitterCell

Added property:

<pre style='color: green'>
	public virtual float ContentsScale { get; set; }
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

### Type Changed: MonoMac.CoreAnimation.CATextLayer

Added property:

<pre style='color: green'>
	public virtual bool AllowsFontSubpixelQuantization { get; set; }
</pre>

### Type Changed: MonoMac.CoreAnimation.CATransition

Added interface:

<pre style='color: green'>
	ICAAction
</pre>

### New Type MonoMac.CoreAnimation.CASpringAnimation

<pre style='color: green'>
public class CASpringAnimation : MonoMac.CoreAnimation.CABasicAnimation, ICAAction, ICAMediaTiming, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSMutableCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CASpringAnimation ();
	public CASpringAnimation (MonoMac.Foundation.NSCoder coder);
	public CASpringAnimation (MonoMac.Foundation.NSObjectFlag t);
	public CASpringAnimation (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual float Damping { get; set; }
	public virtual float InitialVelocity { get; set; }
	public virtual float Mass { get; set; }
	public virtual double SettlingDuration { get; }
	public virtual float Stiffness { get; set; }
	// methods
	public static CABasicAnimation FromKeyPath (string path);
}
</pre>

## Namespace MonoMac.CoreBluetooth

### Type Changed: MonoMac.CoreBluetooth.CBError

Added value:

<pre style='color: green'>
	ConnectionLimitReached = 11,
</pre>

### Type Changed: MonoMac.CoreBluetooth.CBPeripheralState

Added value:

<pre style='color: green'>
	Disconnecting = 3,
</pre>

## Namespace MonoMac.CoreData

### Type Changed: MonoMac.CoreData.NSEntityDescription

Added property:

<pre style='color: green'>
	public MonoMac.Foundation.NSObject[][] UniquenessConstraints { get; set; }
</pre>

### Type Changed: MonoMac.CoreData.NSIncrementalStore

Added constructor:

<pre style='color: green'>
	public NSIncrementalStore (NSPersistentStoreCoordinator root, string name, MonoMac.Foundation.NSUrl url, MonoMac.Foundation.NSDictionary options);
</pre>

### Type Changed: MonoMac.CoreData.NSManagedObject

Added property:

<pre style='color: green'>
	public virtual bool HasPersistentChangedValues { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual NSManagedObjectID[] GetObjectIDs (string relationshipName);
</pre>

### Type Changed: MonoMac.CoreData.NSManagedObjectContext

Added property:

<pre style='color: green'>
	public virtual bool ShouldDeleteInaccessibleFaults { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual NSManagedObject GetExistingObject (NSManagedObjectID objectID, out MonoMac.Foundation.NSError error);
	public static void MergeChangesFromRemoteContextSave (MonoMac.Foundation.NSDictionary changeNotificationData, NSManagedObjectContext[] contexts);
	public virtual void RefreshAllObjects ();
	public virtual bool ShouldHandleInaccessibleFault (NSManagedObject fault, NSManagedObjectID oid, NSPropertyDescription property);
</pre>

### Type Changed: MonoMac.CoreData.NSMergeConflict

Obsoleted constructors:

```
[Obsolete ("Default constructor is not available")]
	public NSMergeConflict ();
```

### Type Changed: MonoMac.CoreData.NSMergePolicy

Obsoleted constructors:

```
[Obsolete ("Default constructor is not available")]
	public NSMergePolicy ();
```

Added methods:

<pre style='color: green'>
	public virtual bool ResolveConstraintConflicts (NSConstraintConflict[] list, out MonoMac.Foundation.NSError error);
	public virtual bool ResolveOptimisticLockingVersionConflicts (NSMergeConflict[] list, out MonoMac.Foundation.NSError error);
</pre>

### Type Changed: MonoMac.CoreData.NSPersistentStore

Obsoleted constructors:

```
[Obsolete ("Default constructor is not available")]
	public NSPersistentStore ();
```

### Type Changed: MonoMac.CoreData.NSPersistentStoreCoordinator

Added methods:

<pre style='color: green'>
	public virtual bool DestroyPersistentStore (MonoMac.Foundation.NSUrl url, string storeType, MonoMac.Foundation.NSDictionary options, out MonoMac.Foundation.NSError error);
	public virtual bool ReplacePersistentStore (MonoMac.Foundation.NSUrl destinationURL, MonoMac.Foundation.NSDictionary destinationOptions, MonoMac.Foundation.NSUrl sourceURL, MonoMac.Foundation.NSDictionary sourceOptions, string storeType, out MonoMac.Foundation.NSError error);
</pre>

### Type Changed: MonoMac.CoreData.NSPersistentStoreRequestType

Added value:

<pre style='color: green'>
	BatchDelete = 7,
</pre>

### New Type MonoMac.CoreData.NSBatchDeleteRequest

<pre style='color: green'>
public class NSBatchDeleteRequest : MonoMac.CoreData.NSPersistentStoreRequest, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchDeleteRequest (NSFetchRequest fetch);
	public NSBatchDeleteRequest (NSManagedObjectID[] objects);
	public NSBatchDeleteRequest (MonoMac.Foundation.NSCoder coder);
	public NSBatchDeleteRequest (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchDeleteRequest (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSFetchRequest FetchRequest { get; }
	public virtual NSBatchDeleteRequestResultType ResultType { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.CoreData.NSBatchDeleteRequestResultType

<pre style='color: green'>
[Serializable]
public enum NSBatchDeleteRequestResultType {
	Count = 2,
	ObjectIDs = 1,
	StatusOnly = 0,
}
</pre>

### New Type MonoMac.CoreData.NSBatchDeleteResult

<pre style='color: green'>
public class NSBatchDeleteResult : MonoMac.CoreData.NSPersistentStoreResult, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSBatchDeleteResult ();
	public NSBatchDeleteResult (MonoMac.Foundation.NSCoder coder);
	public NSBatchDeleteResult (MonoMac.Foundation.NSObjectFlag t);
	public NSBatchDeleteResult (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual MonoMac.Foundation.NSObject Result { get; }
	public virtual NSBatchDeleteRequestResultType ResultType { get; }
	// methods
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.CoreData.NSConstraintConflict

<pre style='color: green'>
public class NSConstraintConflict : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSConstraintConflict ();
	public NSConstraintConflict (MonoMac.Foundation.NSCoder coder);
	public NSConstraintConflict (MonoMac.Foundation.NSObjectFlag t);
	public NSConstraintConflict (IntPtr handle);
	public NSConstraintConflict (string[] contraint, NSManagedObject databaseObject, MonoMac.Foundation.NSDictionary databaseSnapshot, NSManagedObject[] conflictingObjects, MonoMac.Foundation.NSObject[] conflictingSnapshots);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual NSManagedObject[] ConflictingObjects { get; }
	public virtual MonoMac.Foundation.NSDictionary[] ConflictingSnapshots { get; }
	public virtual string[] Constraint { get; }
	public virtual MonoMac.Foundation.NSDictionary ConstraintValues { get; }
	public virtual NSManagedObject DatabaseObject { get; }
	public virtual MonoMac.Foundation.NSDictionary DatabaseSnapshot { get; }
	// methods
	protected override void Dispose (bool disposing);
}
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
	public virtual IntPtr Handle { get; }
	public System.Action InvalidationCallback { get; set; }
	public bool IsRemote { get; }
	public bool IsValid { get; }
	public string Name { get; set; }
	// methods
	protected override void ~CFMessagePort ();
	protected void Check ();
	public static CFMessagePort CreateLocalPort (string name, CFMessagePort.CFMessagePortCallBack callback, CFAllocator allocator);
	public static CFMessagePort CreateRemotePort (CFAllocator allocator, string name);
	public CFRunLoopSource CreateRunLoopSource ();
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
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
	AppTransportSecurityRequiresSecureConnection = -1022,
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
[Obsolete ("Use a real `null` value instead of this managed wrapper over a null native instance")]
	public static CGColorSpace Null;
```

Obsoleted methods:

```
[Obsolete ("This method has been renamed CreateDeviceCmyk()")]
	public static CGColorSpace CreateDeviceCMYK ();
```

Added methods:

<pre style='color: green'>
	public static CGColorSpace CreateAcesCGLinear ();
	public static CGColorSpace CreateAdobeRgb1988 ();
	public static CGColorSpace CreateDeviceCmyk ();
	public static CGColorSpace CreateGenericCmyk ();
	public static CGColorSpace CreateGenericGray ();
	public static CGColorSpace CreateGenericGrayGamma2_2 ();
	public static CGColorSpace CreateGenericRgb ();
	public static CGColorSpace CreateGenericRgbLinear ();
	public static CGColorSpace CreateGenericXyz ();
	public static CGColorSpace CreateItuR_2020 ();
	public static CGColorSpace CreateItuR_709 ();
	public static CGColorSpace CreateRommRgb ();
	public static CGColorSpace CreateSrgb ();
</pre>

### Type Changed: MonoMac.CoreGraphics.CGColorSpaceNames

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString AcesCGLinear { get; }
	public static MonoMac.Foundation.NSString AdobeRgb1998 { get; }
	public static MonoMac.Foundation.NSString GenericCmyk { get; }
	public static MonoMac.Foundation.NSString GenericRgb { get; }
	public static MonoMac.Foundation.NSString GenericRgbLinear { get; }
	public static MonoMac.Foundation.NSString GenericXyz { get; }
	public static MonoMac.Foundation.NSString ItuR_2020 { get; }
	public static MonoMac.Foundation.NSString ItuR_709 { get; }
	public static MonoMac.Foundation.NSString RommRgb { get; }
	public static MonoMac.Foundation.NSString Srgb { get; }
</pre>

### Type Changed: MonoMac.CoreGraphics.CGDataProvider

Added constructors:

<pre style='color: green'>
	public CGDataProvider (MonoMac.Foundation.NSData data);
	public CGDataProvider (MonoMac.Foundation.NSUrl url);
</pre>

### Type Changed: MonoMac.CoreGraphics.CGImage

Added property:

<pre style='color: green'>
	public MonoMac.Foundation.NSString UTType { get; }
</pre>

## Namespace MonoMac.CoreImage

### Type Changed: MonoMac.CoreImage.CIAccordionFoldTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAdditionCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAffineClamp

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAffineFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAffineTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAffineTransform

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaAverage

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaHistogram

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaMaximum

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaMaximumAlpha

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaMinimum

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAreaMinimumAlpha

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIAztecCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoMac.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoMac.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CIBarsSwipeTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBlendFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBlendWithAlphaMask

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBlendWithMask

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBloom

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBoxBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBumpDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIBumpDistortionLinear

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICheckerboardGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICircleSplashDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICircularScreen

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICircularWrap

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICMYKHalftone


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoMac.CoreImage.CICmykHalftone</span>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Removed properties:

<pre style='color: red'>
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float GrayComponentReplacement { get; set; }
	public float InputSharpness { get; set; }
	public float UnderColorRemoval { get; set; }
	public float Width { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CICode128BarcodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoMac.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoMac.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CIColor

Added constructors:

<pre style='color: green'>
	public CIColor (float red, float green, float blue);
	public CIColor (float red, float green, float blue, float alpha);
</pre>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorBurnBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorClamp

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorControls

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorCrossPolynomial

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorCube

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorCubeWithColorSpace

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorDodgeBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorInvert

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorMap

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorMatrix

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorMonochrome

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorPolynomial

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColorPosterize

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIColumnAverage

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIComicEffect

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICompositingFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConstantColorGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIContext

Added properties:

<pre style='color: green'>
	public static int OfflineGPUCount { get; }
	public virtual MonoMac.CoreGraphics.CGColorSpace WorkingColorSpace { get; }
</pre>

Added method:

<pre style='color: green'>
	public static CIContext FromOfflineGpu (int gpuIndex);
</pre>

### Type Changed: MonoMac.CoreImage.CIContextOptions

Added property:

<pre style='color: green'>
	public bool? HighQualityDownsample { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolution3X3

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolution5X5

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolution7X7

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolution9Horizontal

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolution9Vertical

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIConvolutionCore

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICopyMachineTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICrop

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CICrystallize

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDarkenBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDepthOfField

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDetector

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString NumberOfAngles { get; }
	public static MonoMac.Foundation.NSString ReturnSubFeatures { get; }
	public static MonoMac.Foundation.NSString TypeText { get; }
</pre>

Added method:

<pre style='color: green'>
	public static CIDetector CreateTextDetector (CIContext context, CIDetectorOptions detectorOptions);
</pre>

### Type Changed: MonoMac.CoreImage.CIDetectorOptions

Added properties:

<pre style='color: green'>
	public float? NumberOfAngles { get; set; }
	public bool? ReturnSubFeatures { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CIDifferenceBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDiscBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDisintegrateWithMaskTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDisplacementDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDissolveTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDistortionFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDivideBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDotScreen

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIDroste

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIEdges

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIEdgeWork

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIEightfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIExclusionBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIExposureAdjust

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFaceBalance

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFalseColor

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFeature

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString TypeQRCode { get; }
	public static MonoMac.Foundation.NSString TypeRectangle { get; }
	public static MonoMac.Foundation.NSString TypeText { get; }
</pre>

### Type Changed: MonoMac.CoreImage.CIFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFilterAttributes

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString Available_iOS { get; }
	public static MonoMac.Foundation.NSString Available_Mac { get; }
	public static MonoMac.Foundation.NSString TypeColor { get; }
	public static MonoMac.Foundation.NSString TypeImage { get; }
	public static MonoMac.Foundation.NSString TypeTransform { get; }
</pre>

### Type Changed: MonoMac.CoreImage.CIFilterGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFilterInputKey

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString BiasKey { get; }
	public static MonoMac.Foundation.NSString Version { get; }
	public static MonoMac.Foundation.NSString WeightsKey { get; }
</pre>

### Type Changed: MonoMac.CoreImage.CIFilterShape

Removed method:

<pre style='color: red'>
	public virtual CIFilterShape IntersectWithRect (System.Drawing.RectangleF rectangle);
</pre>

Added method:

<pre style='color: green'>
	public virtual CIFilterShape Intersect (System.Drawing.RectangleF rectangle);
</pre>

### Type Changed: MonoMac.CoreImage.CIFlashTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFormat

Obsoleted fields:

```
[Obsolete ("This value can not be shared across Mac/iOS binaries, future proof with kRGBAf instead")]
	RGBAf = 3,
```

Added values:

<pre style='color: green'>
	A16 = 12,
	A8 = 11,
	ABGR8 = 7,
	Af = 14,
	Ah = 13,
	kBGRA8 = 5,
	kRGBA8 = 6,
	kRGBAf = 4,
	R16 = 16,
	R8 = 15,
	Rf = 18,
	RG16 = 20,
	RG8 = 19,
	RGf = 22,
	RGh = 21,
	Rh = 17,
</pre>

### Type Changed: MonoMac.CoreImage.CIFourfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFourfoldRotatedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIFourfoldTranslatedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGammaAdjust

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGaussianBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGaussianGradient

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGlassDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGlassLozenge

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGlideReflectedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIGloom

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHardLightBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHatchedScreen

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHeightFieldFromMask

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHexagonalPixellate

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHighlightShadowAdjust

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHistogramDisplayFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHoleDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHueAdjust

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIHueBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIImage

Added constructor:

<pre style='color: green'>
	public CIImage (ICIImageProvider provider, uint width, uint height, CIFormat pixelFormat, MonoMac.CoreGraphics.CGColorSpace colorSpace, CIImageProviderOptions options);
</pre>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Added properties:

<pre style='color: green'>
	public static int FormatA16 { get; }
	public static int FormatA8 { get; }
	public static int FormatABGR8 { get; }
	public static int FormatAf { get; }
	public static int FormatAh { get; }
	public static int FormatBGRA8 { get; }
	public static int FormatR16 { get; }
	public static int FormatR8 { get; }
	public static int FormatRf { get; }
	public static int FormatRG16 { get; }
	public static int FormatRG8 { get; }
	public static int FormatRGBA8 { get; }
	public static int FormatRGf { get; }
	public static int FormatRGh { get; }
	public static int FormatRh { get; }
	public virtual MonoMac.Foundation.NSUrl Url { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static CIImage FromImageBuffer (MonoMac.CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);
	public static CIImage FromProvider (ICIImageProvider provider, uint width, uint height, CIFormat pixelFormat, MonoMac.CoreGraphics.CGColorSpace colorSpace, CIImageProviderOptions options);
</pre>

### Type Changed: MonoMac.CoreImage.CIKaleidoscope

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILanczosScaleTransform

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILenticularHaloGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILightenBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILinearBurnBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILinearDodgeBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILinearGradient

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILinearToSRGBToneCurve

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILineOverlay

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILineScreen

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CILuminosityBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMaskedVariableBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMaskToAlpha

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMaximumComponent

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMaximumCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMedianFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMinimumComponent

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMinimumCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIModTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMotionBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMultiplyBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIMultiplyCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CINoiseReduction

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIOpTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIOverlayBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPageCurlTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPageCurlWithShadowTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIParallelogramTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPerspectiveCorrection

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPerspectiveTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPerspectiveTransform

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffect

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectChrome

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectFade

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectInstant

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectMono

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectNoir

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectProcess

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectTonal

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPhotoEffectTransfer

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPinchDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPinLightBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPixellate

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIPointillize

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIQRCodeGenerator


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.CoreImage.CIFilter</span></span>

 <span style='color:green'>MonoMac.CoreImage.CICodeGenerator</span>

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

Removed property:

<pre style='color: red'>
	public MonoMac.Foundation.NSData Message { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CIRadialGradient

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIRandomGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIRippleTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIRowAverage

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISampler

Obsoleted constructors:

```
[Obsolete ("This default constructor does not provide a valid instance")]
	public CISampler ();
```

### Type Changed: MonoMac.CoreImage.CISamplerOptions

Added property:

<pre style='color: green'>
	public MonoMac.CoreGraphics.CGColorSpace ColorSpace { get; set; }
</pre>

### Type Changed: MonoMac.CoreImage.CISaturationBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIScreenBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIScreenFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISepiaTone

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIShadedMaterial

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISharpenLuminance

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISixfoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISixfoldRotatedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISoftLightBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISourceAtopCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISourceInCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISourceOutCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISourceOverCompositing

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISpotColor

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISpotLight

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISRGBToneCurveToLinear

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIStarShineGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIStraightenFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIStretchCrop

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIStripesGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISubtractBlendMode

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISunbeamsGenerator

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CISwipeTransition

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITemperatureAndTint

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITileFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIToneCurve

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITorusLensDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITransitionFilter

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITriangleTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITwelvefoldReflectedTile

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CITwirlDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIUnsharpMask

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIVector

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIVibrance

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIVignette

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIVignetteEffect

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIVortexDistortion

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIWhitePointAdjust

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### Type Changed: MonoMac.CoreImage.CIZoomBlur

Added interface:

<pre style='color: green'>
	MonoMac.Foundation.INSSecureCoding
</pre>

### New Type MonoMac.CoreImage.CICmykHalftone

<pre style='color: green'>
public class CICmykHalftone : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CICmykHalftone ();
	public CICmykHalftone (IntPtr handle);
	// properties
	public float Angle { get; set; }
	public CIVector Center { get; set; }
	public float GrayComponentReplacement { get; set; }
	public float InputSharpness { get; set; }
	public float UnderColorRemoval { get; set; }
	public float Width { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CICodeGenerator

<pre style='color: green'>
public abstract class CICodeGenerator : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CICodeGenerator (IntPtr handle);
	public CICodeGenerator (string name);
	// properties
	public MonoMac.Foundation.NSData Message { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CIColorKernel

<pre style='color: green'>
public class CIColorKernel : MonoMac.CoreImage.CIKernel, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIColorKernel (MonoMac.Foundation.NSCoder coder);
	public CIColorKernel (MonoMac.Foundation.NSObjectFlag t);
	public CIColorKernel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (System.Drawing.RectangleF extent, MonoMac.Foundation.NSObject[] args);
	public static CIColorKernel FromProgramSingle (string coreImageShaderProgram);
}
</pre>

### New Type MonoMac.CoreImage.CIFilterConstructor_Extensions

<pre style='color: green'>
public static class CIFilterConstructor_Extensions {
}
</pre>

### New Type MonoMac.CoreImage.CIImageProvider_Extensions

<pre style='color: green'>
public static class CIImageProvider_Extensions {
}
</pre>

### New Type MonoMac.CoreImage.CIImageProviderOptions

<pre style='color: green'>
public class CIImageProviderOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public CIImageProviderOptions ();
	public CIImageProviderOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public MonoMac.Foundation.NSObject TileSize { get; set; }
	public MonoMac.Foundation.NSObject UserInfo { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CIKernelRoiCallback

<pre style='color: green'>
public sealed delegate CIKernelRoiCallback : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CIKernelRoiCallback (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (int index, System.Drawing.RectangleF rect, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF EndInvoke (System.IAsyncResult result);
	public virtual System.Drawing.RectangleF Invoke (int index, System.Drawing.RectangleF rect);
}
</pre>

### New Type MonoMac.CoreImage.CILightTunnel

<pre style='color: green'>
public class CILightTunnel : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CILightTunnel ();
	public CILightTunnel (IntPtr handle);
	// properties
	public CIVector Center { get; set; }
	public float Radius { get; set; }
	public float Rotation { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CIPdf417BarcodeGenerator

<pre style='color: green'>
public class CIPdf417BarcodeGenerator : MonoMac.CoreImage.CICodeGenerator, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPdf417BarcodeGenerator ();
	public CIPdf417BarcodeGenerator (IntPtr handle);
	// properties
	public int CompactionMode { get; set; }
	public bool CompactStyle { get; set; }
	public int CorrectionLevel { get; set; }
	public int DataColumns { get; set; }
	public float MaxHeight { get; set; }
	public float MaxWidth { get; set; }
	public float MinWidth { get; set; }
	public float PreferredAspectRatio { get; set; }
	public int Rows { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CIPerspectiveTransformWithExtent

<pre style='color: green'>
public class CIPerspectiveTransformWithExtent : MonoMac.CoreImage.CIPerspectiveTransform, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIPerspectiveTransformWithExtent ();
	public CIPerspectiveTransformWithExtent (IntPtr handle);
	// properties
	public CIVector Extent { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CISmoothLinearGradient

<pre style='color: green'>
public class CISmoothLinearGradient : MonoMac.CoreImage.CILinearGradient, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CISmoothLinearGradient ();
	public CISmoothLinearGradient (IntPtr handle);
}
</pre>

### New Type MonoMac.CoreImage.CITriangleKaleidoscope

<pre style='color: green'>
public class CITriangleKaleidoscope : MonoMac.CoreImage.CIFilter, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CITriangleKaleidoscope ();
	public CITriangleKaleidoscope (IntPtr handle);
	// properties
	public float Decay { get; set; }
	public CIVector Point { get; set; }
	public float Rotation { get; set; }
	public float Size { get; set; }
}
</pre>

### New Type MonoMac.CoreImage.CIWarpKernel

<pre style='color: green'>
public class CIWarpKernel : MonoMac.CoreImage.CIKernel, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CIWarpKernel (MonoMac.Foundation.NSCoder coder);
	public CIWarpKernel (MonoMac.Foundation.NSObjectFlag t);
	public CIWarpKernel (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual CIImage ApplyWithExtent (System.Drawing.RectangleF extent, CIKernelRoiCallback callback, CIImage image, MonoMac.Foundation.NSObject[] args);
	public static CIWarpKernel FromProgramSingle (string coreImageShaderProgram);
}
</pre>

### New Type MonoMac.CoreImage.ICIFilterConstructor

<pre style='color: green'>
public interface ICIFilterConstructor : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual CIFilter FilterWithName (string name);
}
</pre>

### New Type MonoMac.CoreImage.ICIImageProvider

<pre style='color: green'>
public interface ICIImageProvider : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void ProvideImageData (IntPtr data, uint rowbytes, uint x, uint y, uint width, uint height, MonoMac.Foundation.NSObject info);
}
</pre>

## Namespace MonoMac.CoreLocation

### Type Changed: MonoMac.CoreLocation.CLPlacemark

Added property:

<pre style='color: green'>
	public virtual MonoMac.Foundation.NSTimeZone TimeZone { get; }
</pre>

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
	public CMBlockBufferError FillDataBytes (byte fillByte, uint offsetIntoDestination, uint dataLength);
	public static CMBlockBuffer FromBuffer (CMBlockBuffer targetBuffer, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public static CMBlockBuffer FromMemoryBlock (IntPtr memoryBlock, uint blockLength, CMCustomBlockAllocator customBlockSource, uint offsetToData, uint dataLength, CMBlockBufferFlags flags, out CMBlockBufferError error);
	public CMBlockBufferError GetDataPointer (uint offset, out uint lengthAtOffset, out uint totalLength, ref IntPtr dataPointer);
	public bool IsRangeContiguous (uint offset, uint length);
	public CMBlockBufferError ReplaceDataBytes (IntPtr sourceBytes, uint offsetIntoDestination, uint dataLength);
</pre>

### Type Changed: MonoMac.CoreMedia.CMBlockBufferError

Added value:

<pre style='color: green'>
	InsufficientSpace = -12708,
</pre>

### Type Changed: MonoMac.CoreMedia.CMTimebase

Added methods:

<pre style='color: green'>
	public CMClockOrTimebase CopyMaster ();
	public CMClock CopyMasterClock ();
	public CMTimebase CopyMasterTimebase ();
	public CMClock CopyUltimateMasterClock ();
</pre>

### Type Changed: MonoMac.CoreMedia.CMTimeMapping

Added property:

<pre style='color: green'>
	public string Description { get; }
</pre>

Added methods:

<pre style='color: green'>
	public MonoMac.Foundation.NSDictionary AsDictionary ();
	public static CMTimeMapping Create (CMTimeRange source, CMTimeRange target);
	public static CMTimeMapping CreateEmpty (CMTimeRange target);
	public static CMTimeMapping CreateFromDictionary (MonoMac.Foundation.NSDictionary dict);
</pre>

### Type Changed: MonoMac.CoreMedia.CMTimeRange

Obsoleted fields:

```
[Obsolete ("Use InvalidRange")]
	public static CMTimeRange Invalid;
```

Added fields:

<pre style='color: green'>
	public static CMTimeRange InvalidMapping;
	public static CMTimeRange InvalidRange;
</pre>

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString TimeMappingSourceKey { get; }
	public static MonoMac.Foundation.NSString TimeMappingTargetKey { get; }
</pre>

### Type Changed: MonoMac.CoreMedia.CMVideoCodecType

Added value:

<pre style='color: green'>
	Hevc = 1752589105,
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

### New Type MonoMac.CoreMedia.LensStabilizationStatus

<pre style='color: green'>
[Serializable]
public enum LensStabilizationStatus {
	Active = 0,
	None = 4,
	Off = 3,
	OutOfRange = 1,
	Unavailable = 2,
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
	public static LSResult Open (MonoMac.Foundation.NSUrl url);
	public static LSResult Open (MonoMac.Foundation.NSUrl url, out MonoMac.Foundation.NSUrl launchedUrl);
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

## Namespace MonoMac.CoreText

### Type Changed: MonoMac.CoreText.CTFont

Added method:

<pre style='color: green'>
	public string GetLocalizedName (CTFontNameKey nameKey, out string actualLanguage);
</pre>

### Type Changed: MonoMac.CoreText.CTLine

Added method:

<pre style='color: green'>
	public void EnumerateCaretOffsets (CTLine.CaretEdgeEnumerator enumerator);
</pre>

## Namespace MonoMac.CoreVideo

### Type Changed: MonoMac.CoreVideo.CVPixelBuffer

Added method:

<pre style='color: green'>
	public void GetExtendedPixels (ref uint extraColumnsOnLeft, ref uint extraColumnsOnRight, ref uint extraRowsOnTop, ref uint extraRowsOnBottom);
</pre>

### Type Changed: MonoMac.CoreVideo.CVPixelBufferPool

Added method:

<pre style='color: green'>
	public void Flush (CVPixelBufferPoolFlushFlags options);
</pre>

### Type Changed: MonoMac.CoreVideo.CVPixelFormatDescription

Added fields:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString ComponentRangeFullRangeKey;
	public static MonoMac.Foundation.NSString ComponentRangeKey;
	public static MonoMac.Foundation.NSString ComponentRangeVideoRangeKey;
	public static MonoMac.Foundation.NSString ComponentRangeWideRangeKey;
</pre>

### Type Changed: MonoMac.CoreVideo.CVReturn

Added value:

<pre style='color: green'>
	Unsupported = -6663,
</pre>

### New Type MonoMac.CoreVideo.CVPixelBufferPoolFlushFlags

<pre style='color: green'>
[Serializable]
public enum CVPixelBufferPoolFlushFlags {
	FlushExcessBuffers = 1,
}
</pre>

## Namespace MonoMac.EventKit

### Type Changed: MonoMac.EventKit.EKErrorCode

Added values:

<pre style='color: green'>
	EventStoreNotAuthorized = 29,
	InvalidEntityType = 27,
	OSNotSupported = 30,
	PriorityIsInvalid = 26,
	ProcedureAlarmsNotMutable = 28,
</pre>

### New Type MonoMac.EventKit.EKParticipantScheduleStatus

<pre style='color: green'>
[Serializable]
public enum EKParticipantScheduleStatus {
	CannotDeliver = 7,
	Delivered = 3,
	DeliveryFailed = 6,
	None = 0,
	NoPrivileges = 5,
	Pending = 1,
	RecipientNotAllowed = 8,
	RecipientNotRecognized = 4,
	Sent = 2,
}
</pre>

### New Type MonoMac.EventKit.EKReminderPriority

<pre style='color: green'>
[Serializable]
public enum EKReminderPriority {
	High = 1,
	Low = 9,
	Medium = 5,
	None = 0,
}
</pre>

### New Type MonoMac.EventKit.EKWeekday

<pre style='color: green'>
[Serializable]
public enum EKWeekday {
	Friday = 6,
	Monday = 2,
	NotSet = 0,
	Saturday = 7,
	Sunday = 1,
	Thursday = 5,
	Tuesday = 3,
	Wednesday = 4,
}
</pre>

## Namespace MonoMac.Foundation

### Type Changed: MonoMac.Foundation.NSAffineTransform

Added interface:

<pre style='color: green'>
	INSSecureCoding
</pre>

### Type Changed: MonoMac.Foundation.NSAppleEventDescriptor

Added constructor:

<pre style='color: green'>
	public NSAppleEventDescriptor (NSAppleEventDescriptorType type);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
	public virtual NSObject InitListDescriptor ();
	[Obsolete ("Use the constructor instead")]
	public virtual NSObject InitRecordDescriptor ();
```

### Type Changed: MonoMac.Foundation.NSArray

Added methods:

<pre style='color: green'>
	public virtual bool Contains (NSObject anObject);
	public static NSArray From (NSObject[][] items);
	public static NSObject[][] FromArrayOfArray (NSArray weakArray);
	public virtual uint IndexOf (NSObject anObject);
</pre>

### Type Changed: MonoMac.Foundation.NSAttributedString

Added method:

<pre style='color: green'>
	public virtual bool ContainsAttachmentsInRange (NSRange range);
</pre>

### Type Changed: MonoMac.Foundation.NSBundle

Added method:

<pre style='color: green'>
	public virtual bool LoadNibNamed (string nibName, NSObject owner, out NSArray topLevelObjects);
</pre>

### Type Changed: MonoMac.Foundation.NSCocoaError

Added values:

<pre style='color: green'>
	BundleErrorMaximum = 5119,
	BundleErrorMinimum = 4992,
	BundleOnDemandResourceExceededMaximumSizeError = 4993,
	BundleOnDemandResourceInvalidTagError = 4994,
	BundleOnDemandResourceOutOfSpaceError = 4992,
	CoderErrorMaximum = 4991,
	CoderErrorMinimum = 4864,
	CoderReadCorruptError = 4864,
	CoderValueNotFoundError = 4865,
</pre>

### Type Changed: MonoMac.Foundation.NSCoder

Added methods:

<pre style='color: green'>
	public byte[] DecodeBytes ();
	public virtual IntPtr DecodeBytes (out uint length);
	public virtual IntPtr DecodeBytes (string key, out uint length);
	public virtual NSObject DecodeTopLevelObject (out NSError error);
	public virtual NSObject DecodeTopLevelObject (string key, out NSError error);
	public virtual NSObject DecodeTopLevelObject (NSSet setOfClasses, string key, out NSError error);
	public virtual NSObject DecodeTopLevelObject (MonoMac.ObjCRuntime.Class klass, string key, out NSError error);
	public NSObject DecodeTopLevelObject (System.Type type, string key, out NSError error);
	public NSObject DecodeTopLevelObject (System.Type[] types, string key, out NSError error);
	public virtual void Fail (NSError error);
	public bool TryDecode (string key, out NSObject result);
	public bool TryDecode (string key, out bool result);
	public bool TryDecode (string key, out byte[] result);
	public bool TryDecode (string key, out double result);
	public bool TryDecode (string key, out int result);
	public bool TryDecode (string key, out long result);
	public bool TryDecode (string key, out float result);
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

### Type Changed: MonoMac.Foundation.NSDictionary

Added methods:

<pre style='color: green'>
	public bool ContainsKey (MonoMac.ObjCRuntime.INativeObject key);
	public MonoMac.ObjCRuntime.INativeObject ObjectForKey (MonoMac.ObjCRuntime.INativeObject obj);
</pre>

### Type Changed: MonoMac.Foundation.NSError

Added property:

<pre style='color: green'>
	public static NSString CFNetworkErrorDomain { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSErrorUserInfoValueProvider GetUserInfoValueProvider (string errorDomain);
	public static void SetUserInfoValueProvider (string errorDomain, NSErrorUserInfoValueProvider provider);
</pre>

### Type Changed: MonoMac.Foundation.NSExpression

Added properties:

<pre style='color: green'>
	public virtual NSExpression FalseExpression { get; }
	public virtual NSExpression TrueExpression { get; }
</pre>

Added method:

<pre style='color: green'>
	public static NSExpression FromConditional (NSPredicate predicate, NSExpression trueExpression, NSExpression falseExpression);
</pre>

### Type Changed: MonoMac.Foundation.NSExpressionType

Added value:

<pre style='color: green'>
	Conditional = 20,
</pre>

### Type Changed: MonoMac.Foundation.NSFormatter

Added methods:

<pre style='color: green'>
	public NSAttributedString GetAttributedString (NSObject obj, MonoMac.AppKit.NSStringAttributes defaultAttributes);
	public virtual NSAttributedString GetAttributedString (NSObject obj, NSDictionary defaultAttributes);
	public virtual bool GetObjectValue (out NSObject obj, string str, out NSString error);
	public virtual bool IsPartialStringValid (string partialString, out string newString, out NSString error);
	public virtual bool IsPartialStringValid (out string partialString, out NSRange proposedSelRange, string origString, NSRange origSelRange, out NSString error);
</pre>

### Type Changed: MonoMac.Foundation.NSHttpCookieStorage

Added method:

<pre style='color: green'>
	public static NSHttpCookieStorage GetSharedCookieStorage (string groupContainerIdentifier);
</pre>

### Type Changed: MonoMac.Foundation.NSHttpUrlResponse

Added constructor:

<pre style='color: green'>
	public NSHttpUrlResponse (NSUrl url, string mimetype, int expectedContentLength, string textEncodingName);
</pre>

### Type Changed: MonoMac.Foundation.NSIndexPath

Added properties:

<pre style='color: green'>
	public virtual int Item { get; }
	public virtual int Section { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSIndexPath FromItemSection (int item, int section);
	public uint[] GetIndexes (NSRange range);
</pre>

### Type Changed: MonoMac.Foundation.NSItemProviderErrorCode

Added value:

<pre style='color: green'>
	UnavailableCoercion = -1200,
</pre>

### Type Changed: MonoMac.Foundation.NSKeyedArchiver

Added property:

<pre style='color: green'>
	public bool RequiresSecureCoding { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual bool GetRequiresSecureCoding ();
</pre>

### Type Changed: MonoMac.Foundation.NSKeyedUnarchiver

Added property:

<pre style='color: green'>
	public bool RequiresSecureCoding { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual bool GetRequiresSecureCoding ();
	public static NSObject UnarchiveTopLevelObject (NSData data, out NSError error);
</pre>

### Type Changed: MonoMac.Foundation.NSMetadataQuery

Added properties:

<pre style='color: green'>
	public static NSString QueryUpdateAddedItemsKey { get; }
	public static NSString QueryUpdateChangedItemsKey { get; }
	public static NSString QueryUpdateRemovedItemsKey { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSMutableAttributedString

Added methods:

<pre style='color: green'>
	public bool ReadFromUrl (NSUrl url, NSAttributedStringDocumentAttributes options, ref NSDictionary returnOptions, ref NSError error);
	public virtual bool ReadFromUrl (NSUrl url, NSDictionary options, ref NSDictionary returnOptions, ref NSError error);
</pre>

### Type Changed: MonoMac.Foundation.NSMutableDictionary

Added property:

<pre style='color: green'>
	public MonoMac.ObjCRuntime.INativeObject Item { get; set; }
</pre>

Added methods:

<pre style='color: green'>
	public void Add (MonoMac.ObjCRuntime.INativeObject key, MonoMac.ObjCRuntime.INativeObject value);
	public bool Remove (MonoMac.ObjCRuntime.INativeObject key);
	public void SetObject (MonoMac.ObjCRuntime.INativeObject value, MonoMac.ObjCRuntime.INativeObject key);
	public bool TryGetValue (MonoMac.ObjCRuntime.INativeObject key, out MonoMac.ObjCRuntime.INativeObject value);
</pre>

### Type Changed: MonoMac.Foundation.NSMutableString

Added methods:

<pre style='color: green'>
	public virtual bool ApplyTransform (NSString transform, bool reverse, NSRange range, out NSRange resultingRange);
	public bool ApplyTransform (NSStringTransform transform, bool reverse, NSRange range, out NSRange resultingRange);
	public virtual void ReplaceCharactersInRange (NSRange range, NSString aString);
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
[Obsolete ("Use WaitUntilFinished method")]
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

### Type Changed: MonoMac.Foundation.NSProgress

Added methods:

<pre style='color: green'>
	public virtual void AddChild (NSProgress child, long pendingUnitCount);
	public static NSProgress FromTotalUnitCount (long unitCount, NSProgress parent, long portionOfParentTotalUnitCount);
	public static NSProgress GetDiscreteProgress (long unitCount);
	public virtual void Resume ();
	public virtual void SetResumingHandler (NSAction handler);
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

### Type Changed: MonoMac.Foundation.NSSet

Modified methods:

```
public NSSet MakeNSObjectSet<T : NSObject T : MonoMac.ObjCRuntime.INativeObject> (T[] values)
	public T[] ToArray<T : NSObject T : MonoMac.ObjCRuntime.INativeObject> ()
```

### Type Changed: MonoMac.Foundation.NSSortDescriptor

Added constructor:

<pre style='color: green'>
	public NSSortDescriptor (string key, bool ascending, NSComparator comparator);
</pre>

### Type Changed: MonoMac.Foundation.NSString

Added properties:

<pre style='color: green'>
	public virtual NSString LocalizedCapitalizedString { get; }
	public virtual NSString LocalizedLowercaseString { get; }
	public virtual NSString LocalizedUppercaseString { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual NSString CommonPrefix (NSString aString, NSStringCompareOptions options);
	public virtual NSString GetVariantFittingPresentationWidth (int width);
	public virtual bool HasPrefix (NSString prefix);
	public virtual bool HasSuffix (NSString suffix);
	public virtual bool LocalizedStandardContainsString (NSString str);
	public virtual NSRange LocalizedStandardRangeOfString (NSString str);
	public virtual NSString TransliterateString (NSString transform, bool reverse);
	public NSString TransliterateString (NSStringTransform transform, bool reverse);
</pre>

### Type Changed: MonoMac.Foundation.NSTimeZone

Added method:

<pre style='color: green'>
	public static NSTimeZone FromGMT (int seconds);
</pre>

### Type Changed: MonoMac.Foundation.NSUndoManager

Added methods:

<pre style='color: green'>
	public virtual void RegisterUndo (NSObject target, System.Action&lt;NSObject&gt; undoHandler);
	public virtual void SetActionName (string actionName);
</pre>

### Type Changed: MonoMac.Foundation.NSUrl

Added constructor:

<pre style='color: green'>
	public NSUrl (string path, bool isDir, NSUrl relativeToUrl);
</pre>

Added properties:

<pre style='color: green'>
	public virtual NSData DataRepresentation { get; }
	public virtual bool HasDirectoryPath { get; }
	public static NSString IsApplicationKey { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSUrl CreateAbsoluteUrlWithDataRepresentation (NSData data, NSUrl relativeToUrl);
	public static NSUrl CreateFileUrl (string path, NSUrl relativeToUrl);
	public static NSUrl CreateFileUrl (string path, bool isDir, NSUrl relativeToUrl);
	public static NSUrl CreateWithDataRepresentation (NSData data, NSUrl relativeToUrl);
</pre>

### Type Changed: MonoMac.Foundation.NSUrlComponents

Added properties:

<pre style='color: green'>
	public virtual NSRange RangeOfFragment { get; }
	public virtual NSRange RangeOfHost { get; }
	public virtual NSRange RangeOfPassword { get; }
	public virtual NSRange RangeOfPath { get; }
	public virtual NSRange RangeOfPort { get; }
	public virtual NSRange RangeOfQuery { get; }
	public virtual NSRange RangeOfScheme { get; }
	public virtual NSRange RangeOfUser { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSUrlError

Added values:

<pre style='color: green'>
	AppTransportSecurityRequiresSecureConnection = -1022,
	CallIsActive = -1019,
	ClientCertificateRequired = -1206,
	DataNotAllowed = -1020,
	InternationalRoamingOff = -1018,
	RequestBodyStreamExhausted = -1021,
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSession

Added methods:

<pre style='color: green'>
	public virtual NSUrlSessionStreamTask CreateBidirectionalStream (NSNetService service);
	public virtual NSUrlSessionStreamTask CreateBidirectionalStream (string hostname, int port);
	public virtual void GetAllTasks (NSUrlSessionAllPendingTasks completionHandler);
	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionTask[]&gt; GetAllTasksAsync ();
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionConfiguration

Added property:

<pre style='color: green'>
	public virtual bool ShouldUseExtendedBackgroundIdleMode { get; }
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionDataDelegate

Added method:

<pre style='color: green'>
	public virtual void DidBecomeStreamTask (NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionStreamTask streamTask);
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionDataDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DidBecomeStreamTask (INSUrlSessionDataDelegate This, NSUrlSession session, NSUrlSessionDataTask dataTask, NSUrlSessionStreamTask streamTask);
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionResponseDisposition

Added value:

<pre style='color: green'>
	BecomeStream = 3,
</pre>

### Type Changed: MonoMac.Foundation.NSUrlSessionTask

Removed property:

<pre style='color: red'>
	public virtual float Priority { get; set; }
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
	public static NSString IsNotNilTransformerName { get; }
	public static NSString KeyedUnarchiveFromDataTransformerName { get; }
	public static MonoMac.ObjCRuntime.Class TransformedValueClass { get; }
	public static NSString UnarchiveFromDataTransformerName { get; }
	public static string[] ValueTransformerNames { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static NSValueTransformer GetValueTransformer (string name);
	public static void SetValueTransformer (NSValueTransformer transformer, string name);
</pre>

### Type Changed: MonoMac.Foundation.RegisterAttribute

Added property:

<pre style='color: green'>
	public bool SkipRegistration { get; set; }
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

### New Type MonoMac.Foundation.INSProgressReporting

<pre style='color: green'>
public interface INSProgressReporting : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
}
</pre>

### New Type MonoMac.Foundation.INSUrlSessionStreamDelegate

<pre style='color: green'>
public interface INSUrlSessionStreamDelegate : INSUrlSessionDelegate, INSUrlSessionTaskDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
public class NSCondition : MonoMac.Foundation.NSObject, INSLocking, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
public class NSConditionLock : MonoMac.Foundation.NSObject, INSLocking, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSConditionLock ();
	public NSConditionLock (NSCoder coder);
	public NSConditionLock (NSObjectFlag t);
	public NSConditionLock (int condition);
	public NSConditionLock (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual int Condition { get; }
	public virtual string Name { get; set; }
	// methods
	public virtual void Lock ();
	public virtual bool LockBeforeDate (NSDate limit);
	public virtual void LockWhenCondition (int condition);
	public virtual bool LockWhenCondition (int condition, NSDate limit);
	public virtual bool TryLock ();
	public virtual bool TryLockWhenCondition (int condition);
	public virtual void Unlock ();
	public virtual void UnlockWithCondition (int condition);
}
</pre>

### New Type MonoMac.Foundation.NSDataDetector

<pre style='color: green'>
public class NSDataDetector : MonoMac.Foundation.NSRegularExpression, INSCoding, INSCopying, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSErrorUserInfoValueProvider

<pre style='color: green'>
public sealed delegate NSErrorUserInfoValueProvider : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSErrorUserInfoValueProvider (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSError error, NSString userInfoKey, System.AsyncCallback callback, object object);
	public virtual NSObject EndInvoke (System.IAsyncResult result);
	public virtual NSObject Invoke (NSError error, NSString userInfoKey);
}
</pre>

### New Type MonoMac.Foundation.NSFileManagerUnmountOptions

<pre style='color: green'>
[Serializable]
public enum NSFileManagerUnmountOptions {
	AllPartitionsAndEjectDisk = 1,
	WithoutUI = 2,
}
</pre>

### New Type MonoMac.Foundation.NSLock

<pre style='color: green'>
public class NSLock : MonoMac.Foundation.NSObject, INSLocking, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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

### New Type MonoMac.Foundation.NSPersonNameComponent

<pre style='color: green'>
public static class NSPersonNameComponent {
	// properties
	public static NSString ComponentKey { get; }
	public static NSString Delimiter { get; }
	public static NSString FamilyName { get; }
	public static NSString GivenName { get; }
	public static NSString MiddleName { get; }
	public static NSString Nickname { get; }
	public static NSString Prefix { get; }
	public static NSString Suffix { get; }
}
</pre>

### New Type MonoMac.Foundation.NSPersonNameComponents

<pre style='color: green'>
public class NSPersonNameComponents : MonoMac.Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersonNameComponents ();
	public NSPersonNameComponents (NSCoder coder);
	public NSPersonNameComponents (NSObjectFlag t);
	public NSPersonNameComponents (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual string FamilyName { get; set; }
	public virtual string GivenName { get; set; }
	public virtual string MiddleName { get; set; }
	public virtual string NamePrefix { get; set; }
	public virtual string NameSuffix { get; set; }
	public virtual string Nickname { get; set; }
	public virtual NSPersonNameComponents PhoneticRepresentation { get; set; }
	// methods
	public virtual NSObject Copy (NSZone zone);
	protected override void Dispose (bool disposing);
}
</pre>

### New Type MonoMac.Foundation.NSPersonNameComponentsFormatter

<pre style='color: green'>
public class NSPersonNameComponentsFormatter : MonoMac.Foundation.NSFormatter, INSCoding, INSCopying, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSPersonNameComponentsFormatter ();
	public NSPersonNameComponentsFormatter (NSCoder coder);
	public NSPersonNameComponentsFormatter (NSObjectFlag t);
	public NSPersonNameComponentsFormatter (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Phonetic { get; set; }
	public virtual NSPersonNameComponentsFormatterStyle Style { get; set; }
	// methods
	public virtual NSAttributedString GetAnnotatedString (NSPersonNameComponents components);
	public static string GetLocalizedString (NSPersonNameComponents components, NSPersonNameComponentsFormatterStyle nameFormatStyle, NSPersonNameComponentsFormatterOptions nameOptions);
	public virtual bool GetObjectValue (out NSObject result, string str, out string errorDescription);
	public virtual string GetString (NSPersonNameComponents components);
}
</pre>

### New Type MonoMac.Foundation.NSPersonNameComponentsFormatterOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum NSPersonNameComponentsFormatterOptions {
	Phonetic = 2,
}
</pre>

### New Type MonoMac.Foundation.NSPersonNameComponentsFormatterStyle

<pre style='color: green'>
[Serializable]
public enum NSPersonNameComponentsFormatterStyle {
	Abbreviated = 4,
	Default = 0,
	Long = 3,
	Medium = 2,
	Short = 1,
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

### New Type MonoMac.Foundation.NSProgressReporting_Extensions

<pre style='color: green'>
public static class NSProgressReporting_Extensions {
	// methods
	public static NSProgress GetProgress (INSProgressReporting This);
}
</pre>

### New Type MonoMac.Foundation.NSRecursiveLock

<pre style='color: green'>
public class NSRecursiveLock : MonoMac.Foundation.NSObject, INSLocking, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
public class NSRegularExpression : MonoMac.Foundation.NSObject, INSCoding, INSCopying, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
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
	public virtual uint ReplaceMatches (NSMutableString mutableString, NSMatchingOptions options, NSRange range, NSString template);
	public virtual string ReplaceMatches (string sourceString, NSMatchingOptions options, NSRange range, string template);
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

### New Type MonoMac.Foundation.NSStringTransform

<pre style='color: green'>
[Serializable]
public enum NSStringTransform {
	FullwidthToHalfwidth = 11,
	HiraganaToKatakana = 10,
	LatinToArabic = 3,
	LatinToCyrillic = 6,
	LatinToGreek = 7,
	LatinToHangul = 2,
	LatinToHebrew = 4,
	LatinToHiragana = 1,
	LatinToKatakana = 0,
	LatinToThai = 5,
	MandarinToLatin = 9,
	StripCombiningMarks = 14,
	StripDiacritics = 15,
	ToLatin = 8,
	ToUnicodeName = 13,
	ToXmlHex = 12,
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionAllPendingTasks

<pre style='color: green'>
public sealed delegate NSUrlSessionAllPendingTasks : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionAllPendingTasks (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSUrlSessionTask[] tasks, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSUrlSessionTask[] tasks);
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionCombinedTasks

<pre style='color: green'>
public class NSUrlSessionCombinedTasks {
	// constructors
	public NSUrlSessionCombinedTasks (NSUrlSessionTask[] tasks);
	// properties
	public NSUrlSessionTask[] Tasks { get; set; }
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionDataRead

<pre style='color: green'>
public sealed delegate NSUrlSessionDataRead : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSUrlSessionDataRead (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (NSData data, bool atEof, NSError error, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (NSData data, bool atEof, NSError error);
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionStreamDataRead

<pre style='color: green'>
public class NSUrlSessionStreamDataRead {
	// constructors
	public NSUrlSessionStreamDataRead (NSData data, bool atEof);
	// properties
	public bool AtEof { get; set; }
	public NSData Data { get; set; }
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionStreamDelegate

<pre style='color: green'>
public class NSUrlSessionStreamDelegate : MonoMac.Foundation.NSUrlSessionTaskDelegate, INSObjectProtocol, INSUrlSessionDelegate, INSUrlSessionStreamDelegate, INSUrlSessionTaskDelegate, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionStreamDelegate ();
	public NSUrlSessionStreamDelegate (NSCoder coder);
	public NSUrlSessionStreamDelegate (NSObjectFlag t);
	public NSUrlSessionStreamDelegate (IntPtr handle);
	// methods
	public virtual void BetterRouteDiscovered (NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public virtual void CompletedTaskCaptureStreams (NSUrlSession session, NSUrlSessionStreamTask streamTask, NSInputStream inputStream, NSOutputStream outputStream);
	public virtual void ReadClosed (NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public virtual void WriteClosed (NSUrlSession session, NSUrlSessionStreamTask streamTask);
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionStreamDelegate_Extensions

<pre style='color: green'>
public static class NSUrlSessionStreamDelegate_Extensions {
	// methods
	public static void BetterRouteDiscovered (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public static void CompletedTaskCaptureStreams (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask, NSInputStream inputStream, NSOutputStream outputStream);
	public static void ReadClosed (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
	public static void WriteClosed (INSUrlSessionStreamDelegate This, NSUrlSession session, NSUrlSessionStreamTask streamTask);
}
</pre>

### New Type MonoMac.Foundation.NSUrlSessionStreamTask

<pre style='color: green'>
public class NSUrlSessionStreamTask : MonoMac.Foundation.NSUrlSessionTask, INSCopying, INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSUrlSessionStreamTask (NSCoder coder);
	public NSUrlSessionStreamTask (NSObjectFlag t);
	public NSUrlSessionStreamTask (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public virtual void CaptureStreams ();
	public virtual void CloseRead ();
	public virtual void CloseWrite ();
	public virtual void ReadData (uint minBytes, uint maxBytes, double timeout, NSUrlSessionDataRead completionHandler);
	public virtual System.Threading.Tasks.Task&lt;NSUrlSessionStreamDataRead&gt; ReadDataAsync (uint minBytes, uint maxBytes, double timeout);
	public virtual void StartSecureConnection ();
	public virtual void StopSecureConnection ();
	public virtual void WriteData (NSData data, double timeout, System.Action&lt;NSError&gt; completionHandler);
	public virtual System.Threading.Tasks.Task WriteDataAsync (NSData data, double timeout);
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

## Namespace MonoMac.GameController

### New Type MonoMac.GameController.GCControllerPlayerIndex

<pre style='color: green'>
[Serializable]
public enum GCControllerPlayerIndex {
	Index1 = 0,
	Index2 = 1,
	Index3 = 2,
	Index4 = 3,
	Unset = -1,
}
</pre>

## Namespace MonoMac.GameKit

### Type Changed: MonoMac.GameKit.GKAchievementViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.AppKit.NSViewController</span></span>

 <span style='color:green'>MonoMac.GameKit.GKGameCenterViewController</span>

### Type Changed: MonoMac.GameKit.GKLeaderboardViewController


Modified base type: <span style='text-decoration: line-through'><span style='color:red'>MonoMac.AppKit.NSViewController</span></span>

 <span style='color:green'>MonoMac.GameKit.GKGameCenterViewController</span>

### Type Changed: MonoMac.GameKit.GKLocalPlayerListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: MonoMac.GameKit.GKMatch

Added event:

<pre style='color: green'>
	public event System.EventHandler&lt;GKDataReceivedForRecipientEventArgs&gt; DataReceivedForRecipient;
</pre>

### Type Changed: MonoMac.GameKit.GKMatchDelegate

Added method:

<pre style='color: green'>
	public virtual void DataReceivedForRecipient (GKMatch match, MonoMac.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: MonoMac.GameKit.GKMatchDelegate_Extensions

Added method:

<pre style='color: green'>
	public static void DataReceivedForRecipient (IGKMatchDelegate This, GKMatch match, MonoMac.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
</pre>

### Type Changed: MonoMac.GameKit.GKPlayer

Added property:

<pre style='color: green'>
	public virtual string GuestIdentifier { get; }
</pre>

Added method:

<pre style='color: green'>
	public static GKPlayer GetAnonymousGuestPlayer (string guestIdentifier);
</pre>

### Type Changed: MonoMac.GameKit.GKTurnBasedEventListener

Added method:

<pre style='color: green'>
	public virtual void WantsToQuitMatch (GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: MonoMac.GameKit.GKTurnBasedEventListener_Extensions

Added method:

<pre style='color: green'>
	public static void WantsToQuitMatch (IGKTurnBasedEventListener This, GKPlayer player, GKTurnBasedMatch match);
</pre>

### Type Changed: MonoMac.GameKit.GKVoiceChat

Obsoleted methods:

```
[Obsolete ("Use SetMute(bool,string) method")]
	public virtual void SetMute (bool isMuted, GKPlayer player);
```

Added method:

<pre style='color: green'>
	public virtual void SetMute (bool isMuted, string playerID);
</pre>

### New Type MonoMac.GameKit.GKDataReceivedForRecipientEventArgs

<pre style='color: green'>
public class GKDataReceivedForRecipientEventArgs : System.EventArgs {
	// constructors
	public GKDataReceivedForRecipientEventArgs (MonoMac.Foundation.NSData data, GKPlayer recipient, GKPlayer player);
	// properties
	public MonoMac.Foundation.NSData Data { get; set; }
	public GKPlayer Player { get; set; }
	public GKPlayer Recipient { get; set; }
}
</pre>

## Namespace MonoMac.ImageIO

### Type Changed: MonoMac.ImageIO.CGImageProperties

Added properties:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString PNGCompressionFilter { get; }
	public static MonoMac.Foundation.NSString TIFFTileLength { get; }
	public static MonoMac.Foundation.NSString TIFFTileWidth { get; }
</pre>

### Type Changed: MonoMac.ImageIO.CGImageThumbnailOptions

Added property:

<pre style='color: green'>
	public int? SubsampleFactor { get; set; }
</pre>

### New Type MonoMac.ImageIO.CGImagePropertyPngFilters

<pre style='color: green'>
[Serializable]
[Flags]
public enum CGImagePropertyPngFilters {
	Average = 64,
	No = 0,
	None = 8,
	Paeth = 128,
	Sub = 16,
	Up = 32,
}
</pre>

## Namespace MonoMac.ImageKit

### Type Changed: MonoMac.ImageKit.IKSlideshow

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString PhotosBundleIdentifier { get; }
</pre>

## Namespace MonoMac.LocalAuthentication

### Type Changed: MonoMac.LocalAuthentication.LAPolicy

Added value:

<pre style='color: green'>
	DeviceOwnerAuthentication = 2,
</pre>

### Type Changed: MonoMac.LocalAuthentication.LAStatus

Added values:

<pre style='color: green'>
	AppCancel = -9,
	InvalidContext = -10,
	TouchIDLockout = -8,
</pre>

### New Type MonoMac.LocalAuthentication.LAAccessControlOperation

<pre style='color: green'>
[Serializable]
public enum LAAccessControlOperation {
	CreateItem = 0,
	CreateKey = 2,
	UseItem = 1,
	UseKeySign = 3,
}
</pre>

### New Type MonoMac.LocalAuthentication.LACredentialType

<pre style='color: green'>
[Serializable]
public enum LACredentialType {
	ApplicationPassword = 0,
}
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

## Namespace MonoMac.MobileCoreServices

### Type Changed: MonoMac.MobileCoreServices.UTType

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString SwiftSource { get; }
</pre>

Added methods:

<pre style='color: green'>
	public static MonoMac.Foundation.NSDictionary GetDeclaration (string uti);
	public static MonoMac.Foundation.NSUrl GetDeclaringBundleURL (string uti);
	public static string GetPreferredTag (string uti, string tagClass);
</pre>

## Namespace MonoMac.NetworkExtension

### Type Changed: MonoMac.NetworkExtension.NEOnDemandRuleInterfaceType

Added value:

<pre style='color: green'>
	Any = 0,
</pre>

### Type Changed: MonoMac.NetworkExtension.NEVpnError

Added values:

<pre style='color: green'>
	ConfigurationReadWriteFailed = 5,
	ConfigurationUnknown = 6,
</pre>

### New Type MonoMac.NetworkExtension.NEAppProxyFlowError

<pre style='color: green'>
[Serializable]
public enum NEAppProxyFlowError {
	Aborted = 5,
	HostUnreachable = 3,
	Internal = 8,
	InvalidArgument = 4,
	None = 0,
	NotConnected = 1,
	PeerReset = 2,
	Refused = 6,
	TimedOut = 7,
}
</pre>

### New Type MonoMac.NetworkExtension.NEFilterManagerError

<pre style='color: green'>
[Serializable]
public enum NEFilterManagerError {
	CannotBeRemoved = 4,
	Disabled = 2,
	Invalid = 1,
	None = 0,
	Stale = 3,
}
</pre>

### New Type MonoMac.NetworkExtension.NEProviderStopReason

<pre style='color: green'>
[Serializable]
public enum NEProviderStopReason {
	AuthenticationCanceled = 6,
	ConfigurationDisabled = 9,
	ConfigurationFailed = 7,
	ConfigurationRemoved = 10,
	ConnectionFailed = 14,
	IdleTimeout = 8,
	None = 0,
	NoNetworkAvailable = 3,
	ProviderDisabled = 5,
	ProviderFailed = 2,
	Superseded = 11,
	UnrecoverableNetworkChange = 4,
	UserInitiated = 1,
	UserLogout = 12,
	UserSwitch = 13,
}
</pre>

### New Type MonoMac.NetworkExtension.NETunnelProviderError

<pre style='color: green'>
[Serializable]
public enum NETunnelProviderError {
	Canceled = 2,
	Failed = 3,
	Invalid = 1,
	None = 0,
}
</pre>

### New Type MonoMac.NetworkExtension.NETunnelProviderRoutingMethod

<pre style='color: green'>
[Serializable]
public enum NETunnelProviderRoutingMethod {
	DestinationIP = 1,
	SourceApplication = 2,
}
</pre>

### New Type MonoMac.NetworkExtension.NWPathStatus

<pre style='color: green'>
[Serializable]
public enum NWPathStatus {
	Invalid = 0,
	Satisfiable = 3,
	Satisfied = 1,
	Unsatisfied = 2,
}
</pre>

### New Type MonoMac.NetworkExtension.NWTcpConnectionState

<pre style='color: green'>
[Serializable]
public enum NWTcpConnectionState {
	Cancelled = 5,
	Connected = 3,
	Connecting = 1,
	Disconnected = 4,
	Invalid = 0,
	Waiting = 2,
}
</pre>

### New Type MonoMac.NetworkExtension.NWUdpSessionState

<pre style='color: green'>
[Serializable]
public enum NWUdpSessionState {
	Cancelled = 5,
	Failed = 4,
	Invalid = 0,
	Preparing = 2,
	Ready = 3,
	Waiting = 1,
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

### Type Changed: MonoMac.ObjCRuntime.Class

Added method:

<pre style='color: green'>
	public static System.Type Lookup (Class class);
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

Added methods:

<pre style='color: green'>
	public static void AudioStreamPacketDescription_objc_msgSend_stret (out MonoMac.AudioToolbox.AudioStreamPacketDescription retval, IntPtr receiver, IntPtr selector);
	public static void AudioStreamPacketDescription_objc_msgSendSuper_stret (out MonoMac.AudioToolbox.AudioStreamPacketDescription retval, IntPtr receiver, IntPtr selector);
	public static MonoMac.AVFoundation.AVAudioConverterPrimeInfo AVAudioConverterPrimeInfo_objc_msgSend (IntPtr receiver, IntPtr selector);
	public static void AVAudioConverterPrimeInfo_objc_msgSend_stret (out MonoMac.AVFoundation.AVAudioConverterPrimeInfo retval, IntPtr receiver, IntPtr selector);
	public static MonoMac.AVFoundation.AVAudioConverterPrimeInfo AVAudioConverterPrimeInfo_objc_msgSendSuper (IntPtr receiver, IntPtr selector);
	public static void AVAudioConverterPrimeInfo_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVAudioConverterPrimeInfo retval, IntPtr receiver, IntPtr selector);
	public static void AVBeatRange_objc_msgSend_stret (out MonoMac.AVFoundation.AVBeatRange retval, IntPtr receiver, IntPtr selector);
	public static void AVBeatRange_objc_msgSendSuper_stret (out MonoMac.AVFoundation.AVBeatRange retval, IntPtr receiver, IntPtr selector);
	public static bool bool_objc_msgSend_int_int (IntPtr receiver, IntPtr selector, int arg1, int arg2);
	public static bool bool_objc_msgSend_IntPtr_bool_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, MonoMac.Foundation.NSRange arg3, out MonoMac.Foundation.NSRange arg4);
	public static bool bool_objc_msgSend_IntPtr_int_bool_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, ref IntPtr arg4);
	public static bool bool_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, ref IntPtr arg6);
	public static bool bool_objc_msgSend_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static bool bool_objc_msgSend_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1);
	public static bool bool_objc_msgSend_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoMac.Foundation.NSRange arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref IntPtr arg5);
	public static bool bool_objc_msgSendSuper_int_int (IntPtr receiver, IntPtr selector, int arg1, int arg2);
	public static bool bool_objc_msgSendSuper_IntPtr_bool_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, MonoMac.Foundation.NSRange arg3, out MonoMac.Foundation.NSRange arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_int_bool_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, bool arg3, ref IntPtr arg4);
	public static bool bool_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, ref IntPtr arg6);
	public static bool bool_objc_msgSendSuper_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2);
	public static bool bool_objc_msgSendSuper_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1);
	public static bool bool_objc_msgSendSuper_ref_IntPtr_out_NSRange_IntPtr_NSRange_ref_IntPtr (IntPtr receiver, IntPtr selector, ref IntPtr arg1, out MonoMac.Foundation.NSRange arg2, IntPtr arg3, MonoMac.Foundation.NSRange arg4, ref IntPtr arg5);
	public static double Double_objc_msgSend_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static double Double_objc_msgSendSuper_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static float float_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static float float_objc_msgSend_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
	public static float float_objc_msgSend_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static float float_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static float float_objc_msgSendSuper_IntPtr_UInt32_RectangleF (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, System.Drawing.RectangleF arg3);
	public static float float_objc_msgSendSuper_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1);
	public static int int_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
	public static int int_objc_msgSend_IntPtr_ref_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, IntPtr arg3);
	public static int int_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
	public static int int_objc_msgSendSuper_IntPtr_ref_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ref IntPtr arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSend_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_int_ref_IntPtr (IntPtr receiver, IntPtr selector, int arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSend_Int64_IntPtr_Int64 (IntPtr receiver, IntPtr selector, long arg1, IntPtr arg2, long arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, IntPtr arg15);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_float_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, float arg3, float arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_NSRange_ref_Int32 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, ref int arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_ref_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref System.Drawing.PointF arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_PointF_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt32_UInt32_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, int arg4, IntPtr arg5, IntPtr arg6);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static IntPtr IntPtr_objc_msgSend_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSend_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, int arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSend_RectangleF_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSend_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
	public static IntPtr IntPtr_objc_msgSend_UInt16_bool_bool (IntPtr receiver, IntPtr selector, ushort arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSend_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_int_int_IntPtr_int_int_int_int_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, int arg1, int arg2, IntPtr arg3, int arg4, int arg5, int arg6, int arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSendSuper_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_int_ref_IntPtr (IntPtr receiver, IntPtr selector, int arg1, ref IntPtr arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_Int64_IntPtr_Int64 (IntPtr receiver, IntPtr selector, long arg1, IntPtr arg2, long arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_int_int_int_int_int_bool_bool_bool_bool_UInt16_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, int arg5, int arg6, int arg7, int arg8, int arg9, bool arg10, bool arg11, bool arg12, bool arg13, ushort arg14, IntPtr arg15);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_bool_bool_IntPtr_IntPtr_UInt32_bool_bool_bool_bool_bool (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, bool arg3, IntPtr arg4, IntPtr arg5, uint arg6, bool arg7, bool arg8, bool arg9, bool arg10, bool arg11);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_float_float_float (IntPtr receiver, IntPtr selector, IntPtr arg1, float arg2, float arg3, float arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_int_UInt32 (IntPtr receiver, IntPtr selector, IntPtr arg1, int arg2, uint arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_NSRange_ref_Int32 (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, MonoMac.Foundation.NSRange arg3, ref int arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_ref_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref System.Drawing.PointF arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_PointF_PointF_PointF (IntPtr receiver, IntPtr selector, IntPtr arg1, System.Drawing.PointF arg2, System.Drawing.PointF arg3, System.Drawing.PointF arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, int arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt32_UInt32_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, int arg4, IntPtr arg5, IntPtr arg6);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, ref IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_NSRange_out_NSRange (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static IntPtr IntPtr_objc_msgSendSuper_out_UInt32 (IntPtr receiver, IntPtr selector, out uint arg1);
	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_int_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, int arg2, IntPtr arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4);
	public static IntPtr IntPtr_objc_msgSendSuper_RectangleF_IntPtr_UInt32 (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, uint arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt16_bool_bool (IntPtr receiver, IntPtr selector, ushort arg1, bool arg2, bool arg3);
	public static IntPtr IntPtr_objc_msgSendSuper_UInt64_ref_IntPtr (IntPtr receiver, IntPtr selector, ulong arg1, ref IntPtr arg2);
	public static void NSEdgeInsets_objc_msgSend_stret_IntPtr_IntPtr_int (out MonoMac.AppKit.NSEdgeInsets retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static void NSEdgeInsets_objc_msgSendSuper_stret_IntPtr_IntPtr_int (out MonoMac.AppKit.NSEdgeInsets retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSend_stret_IntPtr_UInt64_NSRange (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static MonoMac.Foundation.NSRange NSRange_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static void NSRange_objc_msgSendSuper_stret_IntPtr_UInt64_NSRange (out MonoMac.Foundation.NSRange retval, IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static System.Drawing.PointF PointF_objc_msgSend_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
	public static void PointF_objc_msgSend_stret_PointF_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
	public static System.Drawing.PointF PointF_objc_msgSendSuper_PointF_PointF (IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
	public static void PointF_objc_msgSendSuper_stret_PointF_PointF (out System.Drawing.PointF retval, IntPtr receiver, IntPtr selector, System.Drawing.PointF arg1, System.Drawing.PointF arg2);
	public static void RectangleF_objc_msgSend_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
	public static void RectangleF_objc_msgSend_stret_NSRange_out_NSRange (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static void RectangleF_objc_msgSend_stret_RectangleF_UInt32_int_ref_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, int arg3, ref System.Drawing.RectangleF arg4);
	public static void RectangleF_objc_msgSend_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static void RectangleF_objc_msgSendSuper_stret_IntPtr_UInt32_IntPtr_RectangleF_PointF_UInt32 (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3, System.Drawing.RectangleF arg4, System.Drawing.PointF arg5, uint arg6);
	public static void RectangleF_objc_msgSendSuper_stret_NSRange_out_NSRange (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, out MonoMac.Foundation.NSRange arg2);
	public static void RectangleF_objc_msgSendSuper_stret_RectangleF_UInt32_int_ref_RectangleF (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, int arg3, ref System.Drawing.RectangleF arg4);
	public static void RectangleF_objc_msgSendSuper_stret_SizeF_UInt32_IntPtr_IntPtr (out System.Drawing.RectangleF retval, IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static System.Drawing.SizeF SizeF_objc_msgSend_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
	public static void SizeF_objc_msgSend_stret_IntPtr_IntPtr_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static void SizeF_objc_msgSend_stret_IntPtr_IntPtr_IntPtr (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_IntPtr_int (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static System.Drawing.SizeF SizeF_objc_msgSendSuper_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
	public static void SizeF_objc_msgSendSuper_stret_IntPtr_IntPtr_int (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3);
	public static void SizeF_objc_msgSendSuper_stret_IntPtr_IntPtr_IntPtr (out System.Drawing.SizeF retval, IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3);
	public static ushort UInt16_objc_msgSend_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
	public static ushort UInt16_objc_msgSend_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
	public static ushort UInt16_objc_msgSendSuper_UInt32 (IntPtr receiver, IntPtr selector, uint arg1);
	public static ushort UInt16_objc_msgSendSuper_UInt32_out_Boolean (IntPtr receiver, IntPtr selector, uint arg1, out bool arg2);
	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoMac.Foundation.NSRange arg6);
	public static uint UInt32_objc_msgSend_IntPtr_IntPtr_ref_IntPtr_out_NSCollectionViewDropOperation (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref IntPtr arg3, out MonoMac.AppKit.NSCollectionViewDropOperation arg4);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static uint UInt32_objc_msgSend_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, MonoMac.Foundation.NSRange arg6);
	public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr_ref_IntPtr_out_NSCollectionViewDropOperation (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, ref IntPtr arg3, out MonoMac.AppKit.NSCollectionViewDropOperation arg4);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3);
	public static uint UInt32_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static uint UInt32_objc_msgSendSuper_NSRange_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5);
	public static ulong UInt64_objc_msgSend_Double_ref_IntPtr (IntPtr receiver, IntPtr selector, double arg1, ref IntPtr arg2);
	public static ulong UInt64_objc_msgSendSuper_Double_ref_IntPtr (IntPtr receiver, IntPtr selector, double arg1, ref IntPtr arg2);
	public static void void_objc_msgSend_AVAudioConverterPrimeInfo (IntPtr receiver, IntPtr selector, MonoMac.AVFoundation.AVAudioConverterPrimeInfo arg1);
	public static void void_objc_msgSend_AVBeatRange (IntPtr receiver, IntPtr selector, MonoMac.AVFoundation.AVBeatRange arg1);
	public static void void_objc_msgSend_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3);
	public static void void_objc_msgSend_IntPtr_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2);
	public static void void_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, MonoMac.Foundation.NSRange arg5);
	public static void void_objc_msgSend_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
	public static void void_objc_msgSend_IntPtr_NSRange_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2, MonoMac.Foundation.NSRange arg3);
	public static void void_objc_msgSend_IntPtr_UInt32_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, MonoMac.Foundation.NSRange arg3, int arg4);
	public static void void_objc_msgSend_IntPtr_UInt32_NSRange_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, MonoMac.Foundation.NSRange arg3, int arg4, MonoMac.Foundation.NSRange arg5);
	public static void void_objc_msgSend_IntPtr_UInt32_UInt32_UInt32_UInt32_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, uint arg4, uint arg5, uint arg6, IntPtr arg7);
	public static void void_objc_msgSend_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSend_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, MonoMac.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
	public static void void_objc_msgSend_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static void void_objc_msgSend_UInt32_UInt32_Double_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, double arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_AVAudioConverterPrimeInfo (IntPtr receiver, IntPtr selector, MonoMac.AVFoundation.AVAudioConverterPrimeInfo arg1);
	public static void void_objc_msgSendSuper_AVBeatRange (IntPtr receiver, IntPtr selector, MonoMac.AVFoundation.AVBeatRange arg1);
	public static void void_objc_msgSendSuper_IntPtr_Double_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, double arg2, IntPtr arg3);
	public static void void_objc_msgSendSuper_IntPtr_Int64 (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, MonoMac.Foundation.NSRange arg5);
	public static void void_objc_msgSendSuper_IntPtr_IntPtr_SizeF (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, System.Drawing.SizeF arg3);
	public static void void_objc_msgSendSuper_IntPtr_NSRange_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoMac.Foundation.NSRange arg2, MonoMac.Foundation.NSRange arg3);
	public static void void_objc_msgSendSuper_IntPtr_UInt32_NSRange_int (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, MonoMac.Foundation.NSRange arg3, int arg4);
	public static void void_objc_msgSendSuper_IntPtr_UInt32_NSRange_int_NSRange (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, MonoMac.Foundation.NSRange arg3, int arg4, MonoMac.Foundation.NSRange arg5);
	public static void void_objc_msgSendSuper_IntPtr_UInt32_UInt32_UInt32_UInt32_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, uint arg3, uint arg4, uint arg5, uint arg6, IntPtr arg7);
	public static void void_objc_msgSendSuper_IntPtr_UInt64_NSRange_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, ulong arg2, MonoMac.Foundation.NSRange arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_NSRange_NSRange_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, MonoMac.Foundation.NSRange arg1, MonoMac.Foundation.NSRange arg2, IntPtr arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_RectangleF_UInt32_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, uint arg2, IntPtr arg3, IntPtr arg4);
	public static void void_objc_msgSendSuper_UInt32_UInt32_Double_IntPtr (IntPtr receiver, IntPtr selector, uint arg1, uint arg2, double arg3, IntPtr arg4);
</pre>

### Type Changed: MonoMac.ObjCRuntime.Platform

Added values:

<pre style='color: green'>
	iOS_9_0 = 589824,
	Mac_10_10_3 = 2825757768286208,
	Mac_10_11 = 2826844395012096,
</pre>

### Type Changed: MonoMac.ObjCRuntime.PlatformHelper

Added method:

<pre style='color: green'>
	public static bool CheckSystemVersion (int major, int minor);
</pre>

### New Type MonoMac.ObjCRuntime.DesignatedInitializerAttribute

<pre style='color: green'>
public class DesignatedInitializerAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public DesignatedInitializerAttribute ();
}
</pre>

## Namespace MonoMac.OpenGL

### Type Changed: MonoMac.OpenGL.MonoMacGameView

Added constructor:

<pre style='color: green'>
	public MonoMacGameView (MonoMac.Foundation.NSCoder coder);
</pre>

### New Type MonoMac.OpenGL.Vector2i

<pre style='color: green'>
[Serializable]
public struct Vector2i, System.IEquatable&lt;Vector2i&gt; {
	// constructors
	public Vector2i (int x, int y);
	// fields
	public static Vector2i One;
	public static int SizeInBytes;
	public static Vector2i UnitX;
	public static Vector2i UnitY;
	public int X;
	public int Y;
	public static Vector2i Zero;
	// methods
	public static Vector2i Add (Vector2i a, Vector2i b);
	public static void Add (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public static Vector2i Clamp (Vector2i vec, Vector2i min, Vector2i max);
	public static void Clamp (ref Vector2i vec, ref Vector2i min, ref Vector2i max, out Vector2i result);
	public virtual bool Equals (Vector2i other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static Vector2i op_Addition (Vector2i left, Vector2i right);
	public static bool op_Equality (Vector2i left, Vector2i right);
	public static bool op_Inequality (Vector2i left, Vector2i right);
	public static Vector2i op_Subtraction (Vector2i left, Vector2i right);
	public static Vector2i op_UnaryNegation (Vector2i vec);
	public static Vector2i Subtract (Vector2i a, Vector2i b);
	public static void Subtract (ref Vector2i a, ref Vector2i b, out Vector2i result);
	public override string ToString ();
}
</pre>

### New Type MonoMac.OpenGL.Vector3i

<pre style='color: green'>
[Serializable]
public struct Vector3i, System.IEquatable&lt;Vector3i&gt; {
	// constructors
	public Vector3i (Vector2i v);
	public Vector3i (Vector3i v);
	public Vector3i (int x, int y, int z);
	// fields
	public static Vector3i One;
	public static int SizeInBytes;
	public static Vector3i UnitX;
	public static Vector3i UnitY;
	public static Vector3i UnitZ;
	public int X;
	public int Y;
	public int Z;
	public static Vector3i Zero;
	// properties
	public Vector2i Xy { get; set; }
	// methods
	public static Vector3i Add (Vector3i a, Vector3i b);
	public static void Add (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static Vector3i Clamp (Vector3i vec, Vector3i min, Vector3i max);
	public static void Clamp (ref Vector3i vec, ref Vector3i min, ref Vector3i max, out Vector3i result);
	public static Vector3i ComponentMax (Vector3i a, Vector3i b);
	public static void ComponentMax (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public static Vector3i ComponentMin (Vector3i a, Vector3i b);
	public static void ComponentMin (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public virtual bool Equals (Vector3i other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static Vector3i op_Addition (Vector3i left, Vector3i right);
	public static bool op_Equality (Vector3i left, Vector3i right);
	public static bool op_Inequality (Vector3i left, Vector3i right);
	public static Vector3i op_Subtraction (Vector3i left, Vector3i right);
	public static Vector3i op_UnaryNegation (Vector3i vec);
	public static Vector3i Subtract (Vector3i a, Vector3i b);
	public static void Subtract (ref Vector3i a, ref Vector3i b, out Vector3i result);
	public override string ToString ();
}
</pre>

### New Type MonoMac.OpenGL.Vector4i

<pre style='color: green'>
[Serializable]
public struct Vector4i, System.IEquatable&lt;Vector4i&gt; {
	// constructors
	public Vector4i (Vector2i v);
	public Vector4i (Vector3i v);
	public Vector4i (Vector4i v);
	public Vector4i (Vector3i v, int w);
	public Vector4i (int x, int y, int z, int w);
	// fields
	public static Vector4i One;
	public static int SizeInBytes;
	public static Vector4i UnitW;
	public static Vector4i UnitX;
	public static Vector4i UnitY;
	public static Vector4i UnitZ;
	public int W;
	public int X;
	public int Y;
	public int Z;
	public static Vector4i Zero;
	// properties
	public Vector2i Xy { get; set; }
	public Vector3i Xyz { get; set; }
	// methods
	public static Vector4i Add (Vector4i a, Vector4i b);
	public static void Add (ref Vector4i a, ref Vector4i b, out Vector4i result);
	public static Vector4i Clamp (Vector4i vec, Vector4i min, Vector4i max);
	public static void Clamp (ref Vector4i vec, ref Vector4i min, ref Vector4i max, out Vector4i result);
	public virtual bool Equals (Vector4i other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static Vector4i Max (Vector4i a, Vector4i b);
	public static void Max (ref Vector4i a, ref Vector4i b, out Vector4i result);
	public static Vector4i Min (Vector4i a, Vector4i b);
	public static void Min (ref Vector4i a, ref Vector4i b, out Vector4i result);
	public static Vector4i op_Addition (Vector4i left, Vector4i right);
	public static bool op_Equality (Vector4i left, Vector4i right);
	public static IntPtr op_Explicit (Vector4i v);
	public static bool op_Inequality (Vector4i left, Vector4i right);
	public static Vector4i op_Subtraction (Vector4i left, Vector4i right);
	public static Vector4i op_UnaryNegation (Vector4i vec);
	public static Vector4i Sub (Vector4i a, Vector4i b);
	public static void Sub (ref Vector4i a, ref Vector4i b, out Vector4i result);
	public static Vector4i Subtract (Vector4i a, Vector4i b);
	public static void Subtract (ref Vector4i a, ref Vector4i b, out Vector4i result);
	public override string ToString ();
}
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

Modified methods:

```
public virtual MonoMac.Foundation.NSObject GetAttribute (string attributeKey)
	public virtual void SetAttribute (MonoMac.Foundation.NSObject attribute, string key)
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
[Obsolete ("Use the MoveWithTimeRange method instead")]
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

### Type Changed: MonoMac.SceneKit.SCNAction

Added methods:

<pre style='color: green'>
	public static SCNAction Hide ();
	public static SCNAction PlayAudioSource (SCNAudioSource source, bool wait);
	public static SCNAction Unhide ();
</pre>

### Type Changed: MonoMac.SceneKit.SCNActionable

Added property:

<pre style='color: green'>
	public virtual string[] ActionKeys { get; }
</pre>

### Type Changed: MonoMac.SceneKit.SCNActionable_Extensions

Added method:

<pre style='color: green'>
	public static string[] GetActionKeys (ISCNActionable This);
</pre>

### Type Changed: MonoMac.SceneKit.SCNGeometry

Added properties:

<pre style='color: green'>
	public virtual SCNGeometryElement[] GeometryElements { get; }
	public virtual SCNGeometrySource[] GeometrySources { get; }
</pre>

### Type Changed: MonoMac.SceneKit.SCNGeometrySource

Modified methods:

```
public SCNGeometrySource FromData (MonoMac.Foundation.NSData data, SCNGeometrySourceSemantics geometrySourceSemantic semantic, int vectorCount, bool floatComponents, int componentsPerVector, int bytesPerComponent, int offset, int stride)
```

### Type Changed: MonoMac.SceneKit.SCNIKConstraint

Added constructor:

<pre style='color: green'>
	public SCNIKConstraint (SCNNode chainRootNode);
</pre>

### Type Changed: MonoMac.SceneKit.SCNLayer

Added properties:

<pre style='color: green'>
	public virtual MonoMac.AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual MonoMac.AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual SCNRenderingApi RenderingApi { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
</pre>

### Type Changed: MonoMac.SceneKit.SCNMaterial

Added properties:

<pre style='color: green'>
	public virtual SCNMaterialProperty AmbientOcclusion { get; }
	public virtual SCNBlendMode BlendMode { get; set; }
	public virtual SCNMaterialProperty SelfIllumination { get; }
</pre>

### Type Changed: MonoMac.SceneKit.SCNNode

Added properties:

<pre style='color: green'>
	public virtual string[] ActionKeys { get; }
	public virtual SCNAudioPlayer[] AudioPlayers { get; }
</pre>

Added methods:

<pre style='color: green'>
	public virtual void AddAudioPlayer (SCNAudioPlayer player);
	public virtual void RemoveAllAudioPlayers ();
	public virtual void RemoveAudioPlayer (SCNAudioPlayer player);
</pre>

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

### Type Changed: MonoMac.SceneKit.SCNPhysicsBody

Added properties:

<pre style='color: green'>
	public virtual bool AffectedByGravity { get; set; }
	public virtual uint ContactTestBitMask { get; set; }
	public virtual SCNVector3 MomentOfInertia { get; set; }
	public virtual bool UsesDefaultMomentOfInertia { get; set; }
</pre>

### Type Changed: MonoMac.SceneKit.SCNPhysicsShape

Added properties:

<pre style='color: green'>
	public SCNPhysicsShapeOptions Options { get; }
	public virtual MonoMac.Foundation.NSObject SourceObject { get; }
	public virtual MonoMac.Foundation.NSValue[] Transforms { get; }
</pre>

Added method:

<pre style='color: green'>
	protected override void Dispose (bool disposing);
</pre>

### Type Changed: MonoMac.SceneKit.SCNProgram

Added properties:

<pre style='color: green'>
	public virtual string FragmentFunctionName { get; set; }
	public virtual string VertexFunctionName { get; set; }
</pre>

Added method:

<pre style='color: green'>
	public virtual void HandleBinding (string name, SCNBufferFrequency frequency, SCNBufferBindingHandler handler);
</pre>

### Type Changed: MonoMac.SceneKit.SCNRenderer

Added properties:

<pre style='color: green'>
	public virtual MonoMac.AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual MonoMac.AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual SCNRenderingApi RenderingApi { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
</pre>

### Type Changed: MonoMac.SceneKit.SCNSceneRenderer

Added properties:

<pre style='color: green'>
	public virtual MonoMac.AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual MonoMac.AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual SCNRenderingApi RenderingApi { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
</pre>

### Type Changed: MonoMac.SceneKit.SCNSceneRenderer_Extensions

Added methods:

<pre style='color: green'>
	public static MonoMac.AVFoundation.AVAudioEngine GetAudioEngine (ISCNSceneRenderer This);
	public static MonoMac.AVFoundation.AVAudioEnvironmentNode GetAudioEnvironmentNode (ISCNSceneRenderer This);
	public static SCNNode GetAudioListener (ISCNSceneRenderer This);
	public static SCNDebugOptions GetDebugOptions (ISCNSceneRenderer This);
	public static SCNNode[] GetNodesInsideFrustum (ISCNSceneRenderer This, SCNNode pointOfView);
	public static SCNRenderingApi GetRenderingApi (ISCNSceneRenderer This);
	public static void SetAudioListener (ISCNSceneRenderer This, SCNNode value);
	public static void SetDebugOptions (ISCNSceneRenderer This, SCNDebugOptions value);
</pre>

### Type Changed: MonoMac.SceneKit.SCNTechnique

Added property:

<pre style='color: green'>
	public MonoMac.Foundation.NSObject Item { get; set; }
</pre>

### Type Changed: MonoMac.SceneKit.SCNView

Added constructor:

<pre style='color: green'>
	public SCNView (System.Drawing.RectangleF frame, SCNRenderingOptions options);
</pre>

Added properties:

<pre style='color: green'>
	public virtual MonoMac.AVFoundation.AVAudioEngine AudioEngine { get; }
	public virtual MonoMac.AVFoundation.AVAudioEnvironmentNode AudioEnvironmentNode { get; }
	public virtual SCNNode AudioListener { get; set; }
	public virtual SCNDebugOptions DebugOptions { get; set; }
	public virtual SCNRenderingApi RenderingApi { get; }
</pre>

Added method:

<pre style='color: green'>
	public virtual SCNNode[] GetNodesInsideFrustum (SCNNode pointOfView);
</pre>

### New Type MonoMac.SceneKit.ISCNBufferStream

<pre style='color: green'>
public interface ISCNBufferStream : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void Length (IntPtr bytes, uint length);
}
</pre>

### New Type MonoMac.SceneKit.SCNAudioPlayer

<pre style='color: green'>
public class SCNAudioPlayer : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSObjectProtocol, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAudioPlayer (MonoMac.AVFoundation.AVAudioNode audioNode);
	public SCNAudioPlayer (MonoMac.Foundation.NSCoder coder);
	public SCNAudioPlayer (MonoMac.Foundation.NSObjectFlag t);
	public SCNAudioPlayer (SCNAudioSource source);
	public SCNAudioPlayer (IntPtr handle);
	// properties
	public virtual MonoMac.AVFoundation.AVAudioNode AudioNode { get; }
	public virtual SCNAudioSource AudioSource { get; }
	public override IntPtr ClassHandle { get; }
	public virtual System.Action DidFinishPlayback { get; set; }
	public virtual System.Action WillStartPlayback { get; set; }
	// methods
	public static SCNAudioPlayer AVAudioNode (MonoMac.AVFoundation.AVAudioNode audioNode);
	protected override void Dispose (bool disposing);
	public static SCNAudioPlayer FromSource (SCNAudioSource source);
}
</pre>

### New Type MonoMac.SceneKit.SCNAudioSource

<pre style='color: green'>
public class SCNAudioSource : MonoMac.Foundation.NSObject, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SCNAudioSource (MonoMac.Foundation.NSCoder coder);
	public SCNAudioSource (MonoMac.Foundation.NSObjectFlag t);
	public SCNAudioSource (MonoMac.Foundation.NSUrl url);
	public SCNAudioSource (IntPtr handle);
	public SCNAudioSource (string filename);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Loops { get; set; }
	public virtual bool Positional { get; set; }
	public virtual float Rate { get; set; }
	public virtual float ReverbBlend { get; set; }
	public virtual bool ShouldStream { get; set; }
	public virtual float Volume { get; set; }
	// methods
	public virtual MonoMac.Foundation.NSObject Copy (MonoMac.Foundation.NSZone zone);
	public static SCNAudioSource FromFile (string fileName);
	public virtual void Load ();
}
</pre>

### New Type MonoMac.SceneKit.SCNBillboardAxis

<pre style='color: green'>
[Serializable]
public enum SCNBillboardAxis {
	All = 7,
	X = 1,
	Y = 2,
	Z = 4,
}
</pre>

### New Type MonoMac.SceneKit.SCNBillboardConstraint

<pre style='color: green'>
public class SCNBillboardConstraint : MonoMac.SceneKit.SCNConstraint, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, ISCNAnimatable, System.IDisposable {
	// constructors
	public SCNBillboardConstraint ();
	public SCNBillboardConstraint (MonoMac.Foundation.NSCoder coder);
	public SCNBillboardConstraint (MonoMac.Foundation.NSObjectFlag t);
	public SCNBillboardConstraint (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual SCNBillboardAxis FreeAxes { get; set; }
	// methods
	public static SCNBillboardConstraint Create ();
}
</pre>

### New Type MonoMac.SceneKit.SCNBlendMode

<pre style='color: green'>
[Serializable]
public enum SCNBlendMode {
	Add = 1,
	Alpha = 0,
	Multiply = 3,
	Replace = 5,
	Screen = 4,
	Subtract = 2,
}
</pre>

### New Type MonoMac.SceneKit.SCNBufferBindingHandler

<pre style='color: green'>
public sealed delegate SCNBufferBindingHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public SCNBufferBindingHandler (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (ISCNBufferStream buffer, SCNNode node, SCNShadable shadable, SCNRenderer renderer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (ISCNBufferStream buffer, SCNNode node, SCNShadable shadable, SCNRenderer renderer);
}
</pre>

### New Type MonoMac.SceneKit.SCNBufferFrequency

<pre style='color: green'>
[Serializable]
public enum SCNBufferFrequency {
	Frame = 0,
	Node = 1,
	Shadable = 2,
}
</pre>

### New Type MonoMac.SceneKit.SCNBufferStream_Extensions

<pre style='color: green'>
public static class SCNBufferStream_Extensions {
}
</pre>

### New Type MonoMac.SceneKit.SCNDebugOptions

<pre style='color: green'>
[Serializable]
[Flags]
public enum SCNDebugOptions {
	None = 0,
	ShowBoundingBoxes = 2,
	ShowLightExtents = 8,
	ShowLightInfluences = 4,
	ShowPhysicsFields = 16,
	ShowPhysicsShapes = 1,
	ShowWireframe = 32,
}
</pre>

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

### New Type MonoMac.SceneKit.SCNReferenceLoadingPolicy

<pre style='color: green'>
[Serializable]
public enum SCNReferenceLoadingPolicy {
	Immediate = 0,
	OnDemand = 1,
}
</pre>

### New Type MonoMac.SceneKit.SCNReferenceNode

<pre style='color: green'>
public class SCNReferenceNode : MonoMac.SceneKit.SCNNode, MonoMac.Foundation.INSCoding, MonoMac.Foundation.INSCopying, MonoMac.Foundation.INSObjectProtocol, MonoMac.Foundation.INSSecureCoding, MonoMac.ObjCRuntime.INativeObject, ISCNActionable, ISCNAnimatable, ISCNBoundingVolume, System.Collections.Generic.IEnumerable&lt;SCNNode&gt;, System.Collections.IEnumerable, System.IDisposable {
	// constructors
	public SCNReferenceNode (MonoMac.Foundation.NSCoder coder);
	public SCNReferenceNode (MonoMac.Foundation.NSObjectFlag t);
	public SCNReferenceNode (MonoMac.Foundation.NSUrl referenceUrl);
	public SCNReferenceNode (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	public virtual bool Loaded { get; }
	public virtual SCNReferenceLoadingPolicy LoadingPolicy { get; set; }
	public virtual MonoMac.Foundation.NSUrl ReferenceUrl { get; set; }
	// methods
	public static SCNReferenceNode CreateFromUrl (MonoMac.Foundation.NSUrl referenceUrl);
	protected override void Dispose (bool disposing);
	public virtual void Load ();
	public virtual void Unload ();
}
</pre>

### New Type MonoMac.SceneKit.SCNRenderingApi

<pre style='color: green'>
[Serializable]
public enum SCNRenderingApi {
	Metal = 0,
	OpenGLCore32 = 2,
	OpenGLCore41 = 3,
	OpenGLLegacy = 1,
}
</pre>

### New Type MonoMac.SceneKit.SCNRenderingOptions

<pre style='color: green'>
public class SCNRenderingOptions : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public SCNRenderingOptions ();
	public SCNRenderingOptions (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public bool? LowPowerDevice { get; set; }
	public SCNRenderingApi? RenderingApi { get; set; }
}
</pre>

## Namespace MonoMac.ScriptingBridge

### Type Changed: MonoMac.ScriptingBridge.SBElementArray

Added constructor:

<pre style='color: green'>
	public SBElementArray (uint capacity);
</pre>

## Namespace MonoMac.Security

### Type Changed: MonoMac.Security.SecAccessControl

Added interfaces:

<pre style='color: green'>
	MonoMac.ObjCRuntime.INativeObject
	System.IDisposable
</pre>

Added property:

<pre style='color: green'>
	public virtual IntPtr Handle { get; }
</pre>

Added methods:

<pre style='color: green'>
	protected override void ~SecAccessControl ();
	public virtual void Dispose ();
	public virtual void Dispose (bool disposing);
</pre>

### Type Changed: MonoMac.Security.SecAccessControlCreateFlags

Added values:

<pre style='color: green'>
	And = 32768,
	ApplicationPassword = -2147483648,
	DevicePasscode = 16,
	Or = 16384,
	PrivateKeyUsage = 1073741824,
	TouchIDAny = 2,
	TouchIDCurrentSet = 8,
</pre>

### Type Changed: MonoMac.Security.SecPolicyIdentifier

Added property:

<pre style='color: green'>
	public static MonoMac.Foundation.NSString ApplePayIssuerEncryption { get; }
</pre>

### Type Changed: MonoMac.Security.SecRecord

Added property:

<pre style='color: green'>
	public SecAuthenticationUI AuthenticationUI { get; set; }
</pre>

### Type Changed: MonoMac.Security.SslCipherSuite

Added values:

<pre style='color: green'>
	TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 = 158,
	TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 = 159,
	TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 = 49197,
	TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 = 49198,
	TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 = 49201,
	TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 = 49202,
	TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 = 49195,
	TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 = 49196,
	TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 = 49199,
	TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 = 49200,
	TLS_RSA_WITH_AES_128_GCM_SHA256 = 156,
	TLS_RSA_WITH_AES_256_GCM_SHA384 = 157,
</pre>

### Type Changed: MonoMac.Security.SslContext

Added method:

<pre style='color: green'>
	public SslStatus SetSessionStrengthPolicy (SslSessionStrengthPolicy policyStrength);
</pre>

### Type Changed: MonoMac.Security.SslSessionOption

Added values:

<pre style='color: green'>
	AllowServerIdentityChange = 5,
	BreakOnClientHello = 7,
</pre>

### Type Changed: MonoMac.Security.SslStatus

Added values:

<pre style='color: green'>
	SSLClientHelloReceived = -9851,
	SSLWeakPeerEphemeralDHKey = -9850,
</pre>

### New Type MonoMac.Security.SecAuthenticationUI

<pre style='color: green'>
[Serializable]
public enum SecAuthenticationUI {
	Allow = 0,
	Fail = 1,
	NotSet = -1,
	Skip = 2,
}
</pre>

### New Type MonoMac.Security.SslSessionStrengthPolicy

<pre style='color: green'>
[Serializable]
public enum SslSessionStrengthPolicy {
	ATSv1 = 1,
	Default = 0,
}
</pre>

## Namespace MonoMac.SpriteKit

### New Type MonoMac.SpriteKit.SKParticleRenderOrder

<pre style='color: green'>
[Serializable]
public enum SKParticleRenderOrder {
	DontCare = 2,
	OldestFirst = 1,
	OldestLast = 0,
}
</pre>

## Namespace MonoMac.VideoToolbox

### Type Changed: MonoMac.VideoToolbox.VTDecompressionProperties

Added property:

<pre style='color: green'>
	public VTPixelTransferProperties PixelTransferSettings { get; set; }
</pre>

### New Type MonoMac.VideoToolbox.VTDownsamplingMode

<pre style='color: green'>
[Serializable]
public enum VTDownsamplingMode {
	Average = 2,
	Decimate = 1,
	Unset = 0,
}
</pre>

### New Type MonoMac.VideoToolbox.VTPixelTransferProperties

<pre style='color: green'>
public class VTPixelTransferProperties : MonoMac.Foundation.DictionaryContainer {
	// constructors
	public VTPixelTransferProperties ();
	public VTPixelTransferProperties (MonoMac.Foundation.NSDictionary dictionary);
	// properties
	public MonoMac.AVFoundation.AVVideoCleanApertureSettings DestinationCleanAperture { get; set; }
	public MonoMac.Foundation.NSData DestinationICCProfile { get; set; }
	public MonoMac.AVFoundation.AVVideoPixelAspectRatioSettings DestinationPixelAspectRatio { get; set; }
	public VTTransferFunction DestinationTransferFunction { get; set; }
	public VTYCbCrMatrix DestinationYCbCrMatrix { get; set; }
	public VTDownsamplingMode DownsamplingMode { get; set; }
	public VTScalingMode ScalingMode { get; set; }
}
</pre>

### New Type MonoMac.VideoToolbox.VTPixelTransferPropertyKeys

<pre style='color: green'>
public static class VTPixelTransferPropertyKeys {
	// properties
	public static MonoMac.Foundation.NSString DestinationCleanAperture { get; }
	public static MonoMac.Foundation.NSString DestinationColorPrimaries { get; }
	public static MonoMac.Foundation.NSString DestinationICCProfile { get; }
	public static MonoMac.Foundation.NSString DestinationPixelAspectRatio { get; }
	public static MonoMac.Foundation.NSString DestinationTransferFunction { get; }
	public static MonoMac.Foundation.NSString DestinationYCbCrMatrix { get; }
	public static MonoMac.Foundation.NSString DownsamplingMode { get; }
	public static MonoMac.Foundation.NSString DownsamplingMode_Average { get; }
	public static MonoMac.Foundation.NSString DownsamplingMode_Decimate { get; }
	public static MonoMac.Foundation.NSString ScalingMode { get; }
	public static MonoMac.Foundation.NSString ScalingMode_CropSourceToCleanAperture { get; }
	public static MonoMac.Foundation.NSString ScalingMode_Letterbox { get; }
	public static MonoMac.Foundation.NSString ScalingMode_Normal { get; }
	public static MonoMac.Foundation.NSString ScalingMode_Trim { get; }
}
</pre>

### New Type MonoMac.VideoToolbox.VTScalingMode

<pre style='color: green'>
[Serializable]
public enum VTScalingMode {
	CropSourceToCleanAperture = 2,
	Letterbox = 3,
	Normal = 1,
	Trim = 4,
	Unset = 0,
}
</pre>

### New Type MonoMac.VideoToolbox.VTUtilities

<pre style='color: green'>
public static class VTUtilities {
	// methods
	public static VTStatus ToCGImage (MonoMac.CoreVideo.CVPixelBuffer pixelBuffer, out MonoMac.CoreGraphics.CGImage image);
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
[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (string eventTypeArg, bool canBubbleArg, bool cancelableArg);
```

### Type Changed: MonoMac.WebKit.DomKeyboardEvent

Added constructors:

<pre style='color: green'>
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
	public DomKeyboardEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, bool altGraphKey);
	[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, string keyIdentifier, DomKeyLocation keyLocation, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: MonoMac.WebKit.DomMouseEvent

Added constructor:

<pre style='color: green'>
	public DomMouseEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail, int screenX, int screenY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey, ushort button, DomEventTarget relatedTarget);
```

### Type Changed: MonoMac.WebKit.DomOverflowEvent

Added constructor:

<pre style='color: green'>
	public DomOverflowEvent (ushort orient, bool hasHorizontalOverflow, bool hasVerticalOverflow);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
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
[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (string eventType, bool canBubble, bool cancelable, DomAbstractView view, int detail);
```

### Type Changed: MonoMac.WebKit.DomWheelEvent

Added constructor:

<pre style='color: green'>
	public DomWheelEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
</pre>

Obsoleted methods:

```
[Obsolete ("Use the constructor instead")]
	public virtual void InitEvent (int wheelDeltaX, int wheelDeltaY, DomAbstractView view, int screenX, int screnY, int clientX, int clientY, bool ctrlKey, bool altKey, bool shiftKey, bool metaKey);
```

### Type Changed: MonoMac.WebKit.WKErrorCode

Added value:

<pre style='color: green'>
	JavaScriptResultTypeIsUnsupported = 5,
</pre>

## Removed Namespace MonoMac.GLKit

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKFogMode</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKLightingType</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKNamedEffect</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKNamedEffect_Extensions</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKTextureEnvMode</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKTextureInfoAlphaState</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKTextureInfoOrigin</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKTextureLoaderError</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKTextureTarget</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKVertexAttrib</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKViewDrawableColorFormat</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKViewDrawableDepthFormat</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKViewDrawableMultisample</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.GLKViewDrawableStencilFormat</span>

### Removed Type  <span style='color: red'>MonoMac.GLKit.IGLKNamedEffect</span>

## New Namespace MonoMac.GameplayKit

### New Type MonoMac.GameplayKit.GKGameModel

<pre style='color: green'>
public class GKGameModel {
	// constructors
	public GKGameModel ();
	// fields
	public static const int MaxScore;
	public static const int MinScore;
}
</pre>

## New Namespace MonoMac.MapKit

### New Type MonoMac.MapKit.MKDirections

<pre style='color: green'>
public class MKDirections {
	// constructors

	[Obsolete ("iOS9 does not allow creating an empty instance")]
	public MKDirections ();
}
</pre>

### New Type MonoMac.MapKit.MKOverlayView

<pre style='color: green'>
public class MKOverlayView {
	// constructors
	public MKOverlayView ();
	// methods
	public static float MKRoadWidthAtZoomScale (float zoomScale);
}
</pre>

## New Namespace MonoMac.MediaToolbox

### New Type MonoMac.MediaToolbox.MTFormatNames

<pre style='color: green'>
public static class MTFormatNames {
	// methods
	public static string GetLocalizedName (MonoMac.CoreMedia.CMMediaType mediaType);
	public static string GetLocalizedName (MonoMac.CoreMedia.CMMediaType mediaType, uint mediaSubType);
}
</pre>

## New Namespace MonoMac.SearchKit

### New Type MonoMac.SearchKit.SKDocument

<pre style='color: green'>
public class SKDocument : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public SKDocument (MonoMac.Foundation.NSUrl url);
	public SKDocument (string name, SKDocument parent, string scheme);
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
public class SKIndex : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public SKTextAnalysis AnalysisProperties { get; }
	public int DocumentCount { get; }
	public virtual IntPtr Handle { get; }
	public int MaximumBytesBeforeFlush { get; set; }
	public int MaximumDocumentID { get; }
	public int MaximumTermID { get; }
	// methods
	protected override void ~SKIndex ();
	public bool AddDocument (SKDocument document, string mimeHint, bool canReplace);
	public bool AddDocumentWithText (SKDocument document, string text, bool canReplace);
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
	public SKDocument GetDocument (int documentId);
	public static void LoadDefaultExtractorPlugIns ();
	public bool MoveDocument (SKDocument document, SKDocument newParent);
	public bool RemoveDocument (SKDocument document);
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
public class SKSearch : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IntPtr Handle { get; }
	// methods
	protected override void ~SKSearch ();
	public void Cancel ();
	protected virtual void Dispose (bool disposing);
	public bool FindMatches (int maxCount, ref int[] ids, double waitTime, out int foundCount);
	public bool FindMatches (int maxCount, ref int[] ids, ref float[] scores, double waitTime, out int foundCount);
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
public class SKSummary : MonoMac.ObjCRuntime.INativeObject, System.IDisposable {
	// properties
	public virtual IntPtr Handle { get; }
	public int ParagraphCount { get; }
	public int SentenceCount { get; }
	// methods
	protected override void ~SKSummary ();
	public static SKSummary Create (MonoMac.Foundation.NSString nsString);
	public static SKSummary Create (string text);
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
